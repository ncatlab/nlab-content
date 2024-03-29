
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Projective and injective resolutions
* table of contents
{: toc}

## Idea

In the context of [[homological algebra]] a _projective/injective_ [[resolution]] of an [[object]] or [[chain complex]] in an [[abelian category]] is a [[resolution]] by a [[quasi-isomorphism|quasi-isomorphic]] chain complex that consists of [[projective objects]] or [[injective objects]], respectively.

Under suitable conditions these are precisely the [[cofibrant resolution]] or [[fibrant resolution]] with respect to a standard [[model structure on chain complexes]].

For instance for non-negatively graded chain complexes of abelian groups there is a model structure with [[weak equivalences]] are the quasi-isomorphisms and the [[fibrations]] are the positive-degreewise surjections. Here every object is a [[fibrant object]] and hence no [[fibrant resolution]] is necessary; while the [[cofibrant resolutions]] are precisely the projective resolutions.

Dually, for non-negatively graded chain complexes of abelian groups there is a model structure with [[weak equivalences]] are the quasi-isomorphisms and the [[cofibrations]] the positive-degreewise injections. Here every object is a [[cofibrant object]] and hence no [[cofibrant resolution]] is necessary; while the [[fibrant resolutions]] are precisely the projective resolutions.

## Definition

We first discuss, as is traditional, projective/injective resolutions of single objects, and then the general cases of projective/injective resolutions of chain complexes. This subsumes the previous case by regarding an object as a chain complex concentrated in degree 0.

### Resolution of an object
 {#ResolutionOfObject}

Let $\mathcal{A}$ be an [[abelian category]].

+-- {: .num_defn #InjectiveResolution}
###### Definition

For $X \in \mathcal{A}$ an [[object]], an **injective resolution** of $X$ is a [[cochain complex]] $J^\bullet \in Ch^\bullet(\mathcal{A})$ (in non-negative degree) equipped with a [[quasi-isomorphism]]

$$
  i : X \stackrel{\sim}{\to} J^\bullet
$$

such that $J^n \in \mathcal{A}$ is an [[injective object]] for all $n \in \mathbb{N}$.

=--

+-- {: .num_remark #InjectiveResolutionInComponents}
###### Remark

In components the quasi-isomorphism of def. \ref{InjectiveResolution}
is a [[chain map]] of the form

$$
  \array{
    X &\to& 0 &\to& \cdots &\to& 0 &\to& \cdots
    \\
    \downarrow^{\mathrlap{i^0}} && \downarrow && && \downarrow
    \\
    J^0 &\stackrel{d^0}{\to}& J^1 &\stackrel{d^1}{\to}& \cdots &\to&
    J^n &\stackrel{d^n}{\to}&\cdots 
  }
  \,.
$$

Since the top complex is concentrated in degree 0, this being a [[quasi-isomorphism]] happens to be equivalent to the sequence

$$
  0 \to X \stackrel{i^0}{\to} J^0 \stackrel{d^0}{\to} J^1 \stackrel{d^1}{\to}
  J^2 \stackrel{d^2}{\to}
  \cdots
$$

being an [[exact sequence]]. In this form one often finds the definition of injective resolution in the literature.

=--

+-- {: .num_defn #ProjectiveResolution}
###### Definition

For $X \in \mathcal{A}$ an [[object]], a **projective resolution** of $X$ is a [[chain complex]] $J_\bullet \in Ch_\bullet(\mathcal{A})$ (in non-negative degree) equipped with a [[quasi-isomorphism]]

$$
  p : J_\bullet \stackrel{\sim}{\to} X
$$

such that $J_n \in \mathcal{A}$ is a [[projective object]] for all $n \in \mathbb{N}$.

=--

+-- {: .num_remark #ProjectiveResolutionInComponents}
###### Remark

In components the quasi-isomorphism of def. \ref{ProjectiveResolution}
is a [[chain map]] of the form

$$
  \array{
    \cdots &\stackrel{\partial_n}{\to}& J_n &\stackrel{\partial_{n-1}}{\to}&
    \cdots &\to& J_1 &\stackrel{\partial_0}{\to}& J_0
    \\
    && \downarrow && && \downarrow && \downarrow^{\mathrlap{p_0}}
    \\
    \cdots &\to& 0 &\to& \cdots &\to& 0 &\to& X
  }
  \,.
$$

Since the bottom complex is concentrated in degree 0, this being a [[quasi-isomorphism]] happens to be equivalent to the sequence

$$
  \cdots J_2 \stackrel{\partial_1}{\to} J_1 \stackrel{\partial_0}{\to} J_0 \stackrel{p_0}{\to}
  X \to 0
$$

being an [[exact sequence]]. In this form one often finds the definition of projective resolution in the literature.

=--

### $F$-Resolutions of an object
 {#FResolutions}

Projective and injective resolutions are typically used for computing the [[derived functor]] of some [[additive functor]] $F \colon \mathcal{A} \to \mathcal{B}$; see at _[[derived functor in homological algebra]]_. While projective resolutions in $\mathcal{A}$ are _sufficient_ for computing _every_ [[left derived functor]] on $Ch_\bullet(\mathcal{A})$ and injective resolutions are sufficient for computing _every_ [[right derived functor]] on $Ch^\bullet(\mathcal{A})$, if one is interested just in a single functor $F$ then such resolutions may be more than _necessary_. A weaker kind of resolution which is still sufficient is then often more convenient for applications. These _$F$-projective resolutions_ and _$F$-injective resolutions_, respectively, we discuss here. A special case of both are _$F$-[[acyclic resolutions]]_.

$\,$

Let $\mathcal{A}, \mathcal{B}$ be [[abelian categories]] and let $F \colon \mathcal{A} \to \mathcal{B}$ be an [[additive functor]]. 

+-- {: .num_defn #FInjectives}
###### Definition

Assume that $F$ is [[left exact functor|left exact]]. An [[additive category|additive]] [[full subcategory]] $\mathcal{I} \subset \mathcal{A}$ is called **$F$-injective** (or: consisting of $F$-injective objects) if

1. for every object $A \in \mathcal{A}$ there is a [[monomorphism]] $A \to \tilde A$ into an object $\tilde A \in \mathcal{I} \subset \mathcal{A}$;

1. for every [[short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $A, B \in \mathcal{I} \subset \mathcal{A}$ also $C \in \mathcal{I} \subset \mathcal{A}$;

1. for every [[short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $A\in \mathcal{I} \subset \mathcal{A}$ also $0 \to F(A) \to F(B) \to F(C) \to 0$ is a short exact sequence in $\mathcal{B}$. 

=--

And dually:

+-- {: .num_defn #FProjectives}
###### Definition

Assume that $F$ is [[right exact functor|right exact]]. An [[additive category|additive]] [[full subcategory]] $\mathcal{P} \subset \mathcal{A}$ is called **$F$-projective** (or: consisting of $F$-projective objects) if

1. for every object $A \in \mathcal{A}$ there is an [[epimorphism]] $\tilde A \to A$ from an object $\tilde A \in \mathcal{P} \subset \mathcal{A}$;

1. for every [[short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $B, C \in \mathcal{P} \subset \mathcal{A}$ also $A \in \mathcal{P} \subset \mathcal{A}$;

1. for every [[short exact sequence]] $0 \to A \to B \to C \to 0$ in $\mathcal{A}$ with $C\in \mathcal{P} \subset \mathcal{A}$ also $0 \to F(A) \to F(B) \to F(C) \to 0$ is a short exact sequence in $\mathcal{B}$. 

=--

For instance ([Schapira, def. 4.6.5](#Schapira)).

With the $\mathcal{I},\mathcal{P}\subset \mathcal{A}$ as above, we say:

+-- {: .num_defn #FProjectivesResolution}
###### Definition

For $A \in \mathcal{A}$, 

* an **$F$-injective resolution** of $A$ is a [[cochain complex]] $I^\bullet \in Ch^\bullet(\mathcal{I}) \subset Ch^\bullet(\mathcal{A})$ and a [[quasi-isomorphism]]

  $$
    A \stackrel{\simeq_{qi}}{\to} I^\bullet
  $$ 

* an **$F$-projective resolution** of $A$ is a [[chain complex]] $Q_\bullet \in Ch_\bullet(\mathcal{P}) \subset Ch^\bullet(\mathcal{A})$ and a [[quasi-isomorphism]]

  $$
    Q_\bullet \stackrel{\simeq_{qi}}{\to} A
    \,.
  $$ 

=--

Let now $\mathcal{A}$ have enough projectives / enough injectives, respectively.

+-- {: .num_example #FAcyclicObjectsAreFProjectiveObjects}
###### Example

For $F \colon \mathcal{A} \to \mathcal{B}$ an [[additive functor]],
let $Ac \subset \mathcal{A}$ be the [[full subcategory]] on the $F$-[[acyclic objects]]. Then

* if $F$ is [[left exact functor|left exact]], then $\mathcal{I} \coloneqq Ac$ is a subcategory of $F$-injective objects;

* if $F$ is [[right exact functor|right exact]], then $\mathcal{P} \coloneqq Ac$ is a subcategory of $F$-projective objects.

=--

+-- {: .proof}
###### Proof

Consider the case that $F$ is left exact. The other case works dually.

The first condition of def. \ref{FInjectives} is satisfied because every [[injective object]] is an $F$-[[acyclic object]] and by assumption there are enough of these. 

For the second and third condition of def. \ref{FInjectives} use that there is the [[long exact sequence]] of [[derived functors]] prop. \ref{LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence}

$$
  0 \to A \to B \to C \to R^1 F(A) \to R^1 F(B) \to R^1 F(C) \to R^2 F(A) \to R^2 F(B) \to R^2 F(C) \to \cdot
  \,.
$$

For the second condition, by assumption on $A$ and $B$ and definition of $F$-[[acyclic object]] we have $R^n F(A) \simeq 0$ and $R^n F(B) \simeq 0$ for $n \geq 1$ and hence short exact sequences

$$
  0 \to 0 \to R^n F(C) \to 0
$$

which imply that $R^n F(C)\simeq 0$ for all $n \geq 1$, hence that $C$ is acyclic. 

Similarly, the third condition is equivalent to $R^1 F(A) \simeq 0$. 

=--

+-- {: .num_example #FAcyclicResolution}
###### Example

The $F$-projective/injective resolutions by [[acyclic objects]] as in example \ref{FAcyclicObjectsAreFProjectiveObjects} are called **$F$-acyclic resolutions**.

=--

### Resolution of a chain complex
 {#ResolutionOfAChainComplex}

The above definition \ref{ProjectiveResolution} of a projective resolution of an object has an immediate generalization to resolutions of chain complexes.

+-- {: .num_defn #ProjectiveResolutionOfChainComplex}
###### Definition

For $C_\bullet \in Ch_\bullet(\mathcal{A})$ a [[chain complex]], a **projective resolution** of $C$ is an [[exact sequence]] of chain complexes

$$
  \cdots 
  \to Q_{\bullet,2} 
  \to Q_{\bullet,1} 
  \to  Q_{\bullet,0} 
  \to C_\bullet 
  \to 0
$$

such that for each $n \in \mathbb{N}$ the component $Q_{n,\bullet} \to C_n$ is a projective resolution of the object $C_n$, according to def. \ref{ProjectiveResolution}.

=--

+-- {: .num_remark }
###### Remark

A projective resolution as above may in particular also be regarded as a [[double complex]] $Q_{\bullet, \bullet}$ equipped with a morphism of double complex to $C_\bullet$ regarded as a vertically constant double complex.

=--

For purposes of computations one is often interested in the following stronger notion.

For any chain complex $C_\bullet$, write $Z_\bullet$, $B_\bullet$, and $H_\bullet$ for the graded objects of [[cycles]], [[boundaries]] and [[homology groups]], respectively, regarded as chain complexes with vanishing [[differentials]].
 
+-- {: .num_defn #FullyProjectiveResolutionOfChainComplex}
###### Definition

A projective resolution $Q_{\bullet,\bullet} \to C_\bullet$ of a chain complex $C_\bullet$, def. \ref{ProjectiveResolutionOfChainComplex}, is called **fully projective** (or **proper**) if furthermore for all $n \in \mathbb{N}$ the induced sequence of (horizontal) [[cycles]]

$$
  \cdots 
   \to 
  Z_{\bullet,2} 
   \to 
  Z_{\bullet,1}  
   \to 
  Z_{\bullet,0} 
   \to 
  Z(C)_\bullet
   \to 
  0
$$

and (horizontal) [[boundaries]]

$$
  \cdots 
   \to 
  B_{\bullet,2} 
   \to 
  B_{\bullet,1}  
   \to 
  B_{\bullet,0} 
   \to 
  B(C)_\bullet
   \to 
  0
$$

and (horizontal) [[homology groups]]

$$
  \cdots 
   \to 
  H_{\bullet,2} 
   \to 
  H_{\bullet,1}  
   \to 
  H_{\bullet,0} 
   \to 
  H(C)_\bullet
   \to 
  0
$$

are each projective resolutions, def. \ref{ProjectiveResolution}, themselves.

=--

## Properties

### Existence and construction of resolutions for objects
 {#ExistenceAndConstruction}

We first discuss the existence of injective/projective resolutions, and then the [[functor|functoriality]] of their constructions.

+-- {: .num_prop #ExistenceOfInjectiveResolutions}
###### Proposition

Let $\mathcal{A}$ be an [[abelian category]] with [[injective object|enough injectives]] (such as $R$[[Mod]] for some [[ring]] $R$).

Then every object $X \in \mathcal{A}$ has an [[injective resolution]], 
def. \ref{InjectiveResolution}.

=--

+-- {: .proof}
###### Proof

Let $X \in \mathcal{A}$ be the given object. 
By remark \ref{InjectiveResolutionInComponents} we need to 
construct an [[exact sequence]] of the form

$$
  0 \to X \to J^0 \stackrel{d^0}{\to} J^1 \stackrel{d^1}{\to}
  J^2 \stackrel{d^2}{\to} \cdots \to J^n \to \cdots 
$$

such that all the $J^\cdot$ are [[injective objects]].

This we now construct by [[induction]] on the degree $n \in \mathbb{N}$.

In the first step, by the assumption of enough enjectives we find an injective object $J^0$ and a [[monomorphism]]

$$
  X \hookrightarrow J^0
$$

hence an [[exact sequence]]

$$
  0 \to X \to J^0
  \,.
$$

Assume then by induction hypothesis that for $n \in \mathbb{N}$ an [[exact sequence]]

$$
  X \to J^0 \stackrel{d^0}{\to} \cdots \to J^{n-1} \stackrel{d^{n-1}}{\to} J^n
$$

has been constructed, where all the $J^\cdot$ are injective objects. Forming the [[cokernel]] of $d^{n-1}$ yields the [[short exact sequence]]

$$
  0 \to J^{n-1} \stackrel{d^{n-1}}{\to} J^n \stackrel{p}{\to} J^n/J^{n-1} \to 0
  \,.
$$

By the assumption that there are enough injectives in $\mathcal{A}$ we may now again find a monomorphism $J^n/J^{n-1} \stackrel{i}{\hookrightarrow} J^{n+1}$ into an injective object $J^{n+1}$. This being a monomorphism means that 

$$
  J^{n-1} \stackrel{d^{n-1}}{\to} J^n \stackrel{d^n \coloneqq i \circ p}{\longrightarrow} J^{n+1}
$$

is [[exact sequence|exact]] in the middle term. Therefore we now have an [[exact sequence]]

$$
  0 \to X \to J^0 \to \cdots \to J^{n-1} \stackrel{d^{n-1}}{\to} J^n \stackrel{d^{n}}{\to} J^{n+1}
$$

which completes the [[induction]] step.

=--

The following proposition is  [[duality|formally dual]] to prop. \ref{ExistenceOfInjectiveResolutions}. 

+-- {: .num_prop #ExistenceOfInjectiveResolutions}
###### Proposition

Let $\mathcal{A}$ be an [[abelian category]] with [[projective object|enough projectives]] (such as $R$[[Mod]] for some [[ring]] $R$).

Then every object $X \in \mathcal{A}$ has a [[projective resolution]], 
def. \ref{ProjectiveResolution}.

=--

+-- {: .proof}
###### Proof

Let $X \in \mathcal{A}$ be the given object. 
By remark \ref{ProjectiveResolutionInComponents} we need to 
construct an [[exact sequence]] of the form

$$
  \cdots \stackrel{\partial_2}{\to}
  J_2 \stackrel{\partial_1}{\to}
  J_1 \stackrel{\partial_0}{\to}
  J_0 \to X \to 0
$$

such that all the $J_\cdot$ are [[projective objects]]. 

This we we now construct by [[induction]] on the degree $n \in \mathbb{N}$.

In the first step, by the assumption of enough projectives we find a projective object $J_0$ and an [[epimorphism]]

$$
  J_0 \to X
$$

hence an [[exact sequence]]

$$
  J_0 \to X \to 0
  \,.
$$

Assume then by induction hypothesis that for $n \in \mathbb{N}$ an [[exact sequence]]

$$
  J_n \stackrel{\partial_{n-1}}{\to}
  J_{n-1}
  \to 
  \cdots
  \stackrel{\partial_0}{\to}
  J_0
  \to 
  X
  \to 
  0
$$

has been constructed, where all the $J_\cdot$ are projective objects. Forming the [[kernel]] of $\partial_{n-1}$ yields the [[short exact sequence]]

$$
  0 \to ker(\partial_{n-1})
  \stackrel{i}{\to}
   J_n \stackrel{\partial_{n-1}}{\to}
  J_{n-1}
  \to 
  0
  \,.
$$

By the assumption that there are enough projectives in $\mathcal{A}$ we may now again find an epimorphism 
$ p : J_{n+1} \to ker(\partial_{n-1})$ out of a projective object $J_{n+1}$. This being an epimorphism means that 

$$
  J_{n+1} \stackrel{\partial_{n} \coloneqq i\circ p}{\to}
  J_n \stackrel{\partial_{n-1}}{\to}
$$

is [[exact sequence|exact]] in the middle term. Therefore we now have an [[exact sequence]]

$$
  J_{n+1} 
    \stackrel{\partial_n}{\to}
  J_n
    \stackrel{\partial_{n-1}}{\to}
  \cdots
   \stackrel{\partial_0}{\to}
  J_0
  \to 
  X
  \to 
  0
  \,,
$$

which completes the [[induction]] step.

=--

+-- {: .num_prop #MapsOutOfExactIntoInjectiveAreNullHomotopic}
###### Proposition

Let $f^\bullet : X^\bullet \to J^\bullet$ be a [[chain map]] of cochain complexes in non-negative degree, out of an [[exact sequence|exact complex]] $0 \simeq_{qi} X^\bullet$ to a degreewise injective complex $J^\bullet$. Then there is a [[null homotopy]] 

$$
  \eta : 0 \Rightarrow f^\bullet
$$

=--

+-- {: .proof}
###### Proof

By definition of [[chain homotopy]] we need to construct a sequence of morphisms $(\eta^{n+1} : X^{n+1} \to J^{n})_{n \in \mathbb{N}}$ such that 

$$
  f^n = \eta^{n+1} \circ d^n_X + d^{n-1}_J \circ \eta^n
  \,.
$$

for all $n$. We now construct this by [[induction]] over $n$, where we take $\eta^0 \coloneqq 0$.

Then in the induction step assume that for given $n \in \mathbb{N}$ we have constructed $\eta^{\bullet \leq n}$ satisfying the above conditions. 

First define now 

$$
  g^n \coloneqq f^n - d_J^{n-1} \circ \eta^n
$$

and observe that

$$
  \begin{aligned}
    g^n \circ d_X^{n-1} 
    & =
    f^n \circ d^{n-1}_X - d^{n-1}_J \circ \eta^n \circ d^{n-1}_X
    \\
    & = f^n \circ d^{n-1}_X - d^{n-1}_J \circ f^{n-1} 
        + d^{n-1}_J \circ d^{n-2}_J \circ \eta^{n-1}
    \\
    & = 0 + 0
    \\
    & 0
  \end{aligned}
  \,.
$$

This means that $g^n$ factors as 

$$
  X^n \to X^n / im(d^{n-1}_X) \stackrel{g^n}{\to} J^n
  \,,
$$ 

where the first map is the [[projection]] to the [[quotient]].

Observe then that by exactness of $X^\bullet$ the morphism
$X^n / im(d^{n-1}_X) \stackrel{d^n_X}{\to} X^{n+1}$ is a [[monomorphism]]. Together this gives us a diagram of the form


$$
  \array{
    X^n / im(d^{n-1}_X) &\stackrel{d^n_X}{\to}& X^{n+1}
   \\
    \downarrow^{\mathrlap{g^n}} & \swarrow_{\mathrlap{\eta^{n+1}}}
    \\
    J^n   }
  \,,
$$ 


where the morphism $\eta^{n+1}$ may be found due to the defining [[right lifting property]] of the [[injective object]] $J^n$ against the top monomorphism.

Observing that the [[commuting diagram|commutativity]] of this diagram is the chain homotopy condition involving $\eta^n$ and $\eta^{n+1}$, this completes the induction step.

=--

+-- {: .num_remark }
###### Remark

Without the assumption above that $J^\bullet$ is injective, such a null-homotopy indeed need not exist. Basic counterexamples are discussed in the section [Chain homotopies that ought to exist but do not](homotopy+category+of+chain+complexes#ChainHomotopiesThatOughtToExistButDoNot) at _[[homotopy category of chain complexes]]_.

=--

The formally dual statement of prop \ref{MapsOutOfExactIntoInjectiveAreNullHomotopic} is the following.

+-- {: .num_prop #MapsProjectiveIntoExactAreNullHomotopic}
###### Lemma

Let $f_\bullet : P_\bullet \to Y_\bullet$ be a [[chain map]] of [[chain complexes]] in non-negative degree, into an [[exact sequence|exact complex]] $0 \simeq_{qi} Y_\bullet$ from a degreewise [[projective object|projective]] complex $P^\bullet$. Then there is a [[null homotopy]] 

$$
  \eta : 0 \Rightarrow f_\bullet
$$

=--

+-- {: .proof}
###### Proof

This is formally dual to the proof of prop. \ref{MapsOutOfExactIntoInjectiveAreNullHomotopic}.

=--

The following proposition says that, when injectively resolving objects, the morphisms between these objects lift to the resolutions, uniquely up to chain homotopy.

+-- {: .num_prop #InjectiveResolutionOfCodomainRespectsMorphisms}
###### Proposition

Let $f : X \to Y$ be a morphism in $\mathcal{A}$. Let

$$
  i_Y : Y \stackrel{\sim}{\to} Y^\bullet
$$

be an injective resolution of $Y$ and 

$$
  i_X : X \stackrel{\sim}{\to} X^\bullet
$$

any [[monomorphism|monomorphism]] that is a [[quasi-isomorphism]] (possibly but not necessarily an injective resolution). Then there is a [[chain map]] $f^\bullet : X^\bullet \to Y^\bullet$ giving a [[commuting diagram]]

$$
  \array{
    X &\stackrel{\sim}{\to}& X^\bullet
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{f^\bullet}}
    \\
    Y &\stackrel{\sim}{\to}& Y^\bullet
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition of [[chain map]] we need to construct
[[morphisms]] $(f^n : X^n \to Y^n)_{n \in \mathbb{N}}$ such that 
for all $n \in \mathbb{N}$ the [[diagrams]]

$$
  \array{
    X^{n} &\stackrel{d^n_X}{\to}& X^{n+1}
    \\
    \downarrow^{\mathrlap{f^n}} && \downarrow^{\mathrlap{f^{n+1}}}
    \\
    Y^{n} &\stackrel{d^n_Y}{\to}& Y^{n+1}
  }
$$

[[commuting diagram|commute]] (the defining condition on a [[chain map]]) and such that the diagram

$$
  \array{
    X &\stackrel{i_X}{\to}& X^0
    \\
    \downarrow^{f} && \downarrow^{\mathrlap{f^0}}
    \\
    Y &\stackrel{i_Y}{\to}& Y^0
  }
$$

commutes in $\mathcal{A}$ (which makes the full diagram in $Ch^\bullet(\mathcal{A})$ commute).

We construct these $f^\bullet = (f^n)_{n \in \mathbb{N}}$ by [[induction]].


To start the induction, the morphism $f^0$ in the first diagram above can be found by the defining [[right lifting property]] of the [[injective object]] $Y^0$ against the [[monomorphism]] $i_X$.

Assume then that for some $n \in \mathbb{N}$ component maps $f^{\bullet \leq n}$ have been obtained such that $d^k_Y\circ f^k = f^{k+1}\circ d^k_X$ for all $0 \leq k \lt n$ . In order to construct $f^{n+1}$ consider the following diagram, which we will describe/construct stepwise from left to right:

$$
  \array{
    X^n &\stackrel{}{\to}& X^n/im(d^{n-1}_X) &\stackrel{d^n_X}{\hookrightarrow}& X^{n+1}
    \\
    {}^{\mathllap{f^n}}\downarrow & \searrow^{\mathrlap{g^n}}
    & \downarrow^{\mathrlap{h^n}} & \swarrow_{\mathrlap{f^{n+1}}}
    \\
    Y^n &\underset{d^n_Y}{\to}& Y^{n+1}
  }
  \,.
$$

Here the morphism $f^n$ on the left is given by induction assumption and we define the diagonal morphism to be the composite

$$
 g^n \coloneqq d^n_Y \circ f^n
 \,.
$$

Observe then that by the chain map property of the $f^{\bullet \leq n}$ we have

$$
  d^n_Y \circ f^n \circ d^{n-1}_X = d^n_Y \circ d^{n-1}_Y \circ f^{n-1} = 0
$$

and therefore $g^n$ factors through $X^n/im(d^{n-1}_X)$ via some $h^n$ as indicated in the middle of the above diagram. Finally the morphism on the top right is a monomorphism by the fact that $X^{\bullet}$ is [[exact sequence|exact]] in positive degrees (being [[quasi-isomorphism|quasi-isomorphic]] to a complex concentrated in degree 0) and so a lift $f^{n+1}$ as shown on the far right of the diagram exists by the defining lifting property of the injective object $Y^{n+1}$. 

The total outer diagram now commutes, being built from commuting sub-diagrams, and this is the required chain map property of $f^{\bullet \leq n+1}$ This completes the induction step. 


=--

+-- {: .num_prop #HomotopyUniquenessOfResolutionOfMorphism}
###### Proposition

The morphism $f_\bullet$ in prop. \ref{InjectiveResolutionOfCodomainRespectsMorphisms} is the unique one up to [[chain homotopy]] making the given diagram commute.

=--

+-- {: .proof}
###### Proof

Given two chain maps $g_1^\bullet, g^2_\bullet$ making the diagram commute, a [[chain homotopy]] $g_1^\bullet \Rightarrow g_2^\bullet$ is equivalently a [[null homotopy]] $0 \Rightarrow g_2^\bullet - g_1^\bullet$ of the difference, which sits in a square of the form

$$
  \array{
    X &\underoverset{h^\bullet}{\sim}{\to}& X^\bullet
    \\
    \downarrow^{\mathrlap{0}} && \downarrow^{\mathrlap{f^\bullet \coloneqq g_2^\bullet - g_1^\bullet}}
    \\
    Y &\stackrel{\sim}{\to}& Y^\bullet
  }
$$

with the left vertical morphism being the [[zero morphism]]
(and the bottom an injective resolution). Hence we have to show that in such a diagram $f^\bullet$ is null-homotopic.

This we may reduce to the statement of prop. \ref{MapsOutOfExactIntoInjectiveAreNullHomotopic}
by considering instead of $f^\bullet$ the induced chain map of augmented complexes


$$
  \array{
     0 
       &\stackrel{}{\to}& 
     X 
       &\stackrel{h^0}{\to}& 
     X^0 
       &\stackrel{d^0_X}{\to}& 
     X^1 
       &\to&
    \cdots
     \\
     \downarrow^{\mathrlap{f^{-2} = 0}}
     &&
     \downarrow^{\mathrlap{f^{-1} = 0}}
     &&
     \downarrow^{f^0}
     &&
     \downarrow^{f^1}
     \\
     0 
       &\to& 
     Y 
       &\to& 
     Y^0 
       &\stackrel{d^0_J}{\to}& 
     Y^1 
       &\to& 
     \cdots  
  }
  \,,
$$

where the second square from the left commutes due to the commutativity of the original square of chain complexes in degree 0.

Since $h^\bullet$ is a [[quasi-isomorphism]], the top chain complex is [[exact sequence|exact]], by remark \ref{InjectiveResolutionInComponents}. Morover the bottom complex consists of [[injective objects]] from the second degree on (the former degree 0). Hence 
the induction in the proof of prop \ref{MapsOutOfExactIntoInjectiveAreNullHomotopic} implies the existence of a [[null homotopy]]


$$
  \array{
     0 
       &\stackrel{}{\to}& 
     X 
       &\stackrel{}{\to}&
     X^0 
       &\stackrel{d^0_X}{\to}&
     X^1 
       &\to& 
     \cdots
     \\
     \downarrow^{\mathrlap{f^{-2} = 0}}
       &\swarrow_{\mathrlap{\eta^{-1} = 0}}&
     \downarrow^{\mathrlap{f^{-1} = 0}}
       &\swarrow_{\mathrlap{\eta^0 = 0} }&
     \downarrow^{f^0}
       &\swarrow_{\mathrlap{\eta^1}}&
     \downarrow^{f^1}
     \\
     0 &\to& Y &\to& Y^0 &\stackrel{d^0_Y}{\to}& Y^1 &\to& \cdots  
  }
$$

starting with $\eta^{-1} = 0$ and $\eta^{0 } = 0$ (notice that the proof prop. \ref{MapsOutOfExactIntoInjectiveAreNullHomotopic} was formulated exactly this way), which works because $f^{-1} = 0$. The de-augmentation $\{f^{\bullet \geq 0}\}$ of this is the desired [[null homotopy]] of $f^\bullet$.

=--

Sometimes one needs to construct resolutions of sequences of morphisms in a more controled way, for instance such that some degreewise exactness is preserved:

+-- {: .num_lemma #ProjectiveResolutionOfExactSequenceByExactSequence}
###### Lemma

For $0 \to A \stackrel{i}{\to} B \stackrel{p}{\to} C \to 0$ a [[short exact sequence]]
in an [[abelian category]] with [[projective object|enough projectives]], 
there exists a [[commuting diagram]] of [[chain complexes]]

$$
  \array{
    0 &\to& A_\bullet &\to& B_\bullet &\to& C_\bullet &\to& 0
    \\
      && 
    \downarrow^{\mathrlap{f_\bullet}}
      && 
    \downarrow^{\mathrlap{g_\bullet}}
      && 
    \downarrow^{\mathrlap{h_\bullet}}
    \\
    0 &\to& A &\stackrel{i}{\to}& B &\stackrel{p}{\to}& C &\to& 0
  }
$$

where 

* each vertical morphism is a projective resolution;

and in addition

* the top row is again a short exact sequence of chain complexes.

=--

This appears for instance in ([May, lemma 3.4](#May)) or ([Murfet, cor. 33](#Murfet)).

+-- {: .proof}
###### Proof

By prop. \ref{ExistenceOfInjectiveResolutions} we can choose $f_\bullet$ and $h_\bullet$. The task is now to construct the third resolution $g_\bullet$ such as to obtain a short exact sequence of chain complexes, hence degreewise a short exact sequence, in the two row.

To construct this, let for each $n \in \mathbb{N}$

$$
  B_n \coloneqq A_n \oplus C:n
$$

be the [[direct sum]] and let the top horizontal morphisms be the canonical inclusion and projection maps of the direct sum.

Let then furthermore (in [[matrix calculus]] notation)

$$
  g_0 = 
   \left(
     \array{
        (j_0)_A  
        & 
        (j_0)_B
      }
  \right)
 : A_0 \oplus C_0 \to B
$$

be given in the first component by the given composite

$$
 (g_0)_A : A_0 \oplus C_0 \stackrel{}{\to} A_0 \stackrel{f_0}{\to} A \stackrel{i}{\hookrightarrow} B
$$

and in the second component we take

$$
  (j_0)_C : A_0 \oplus C_0 \to C_0 \stackrel{\zeta}{\to} B
$$

to be given by a lift in

$$
  \array{
    && B
    \\
    & {}^{\mathllap{\zeta}}\nearrow & \downarrow^{\mathrlap{p}}
    \\
    C_0 &\stackrel{h_0}{\to}& C
  }
  \,,
$$

which exists by the [[left lifting property]] of the [[projective object]]
$C_0$ (since $C_\bullet$ is a projective resolution) against the [[epimorphism]] $p : B \to C$ of the [[short exact sequence]].

In total this gives in degree 0

$$
  \array{
    A_0 &\hookrightarrow& A_0 \oplus C_0 &\to& C_0
    \\
    \downarrow^{\mathrlap{f_0}} && {}^{\mathllap{((g_0)_A, (g_0)_C)}}\downarrow &\swarrow_{\zeta}& \downarrow^{\mathrlap{h_0}}
    \\
    A &\stackrel{i}{\hookrightarrow}& B &\stackrel{p}{\to}& C
  }
  \,.
$$

Let then the [[differentials]] of $B_\bullet$ be given by

$$
  d_k^{B_\bullet} 
    = 
  \left(
    \array{
      d_k^{A_\bullet} & (-1)^k e_k
      \\
      0 & d_k^{C_\bullet}
    }
  \right)
  : 
  A_{k+1} \oplus C_{k+1}
  \to
  A_k \oplus C_k
  \,,
$$

where the $\{e_k\}$ are constructed by [[induction]] as follows. Let $e_0$ be a lift in 

$$
  \array{   
    & && A_0
    \\
    & & {}^{\mathllap{e_0}}\nearrow & \downarrow^{\mathrlap{f_0}}
    \\
    \zeta \circ d^{C_\bullet}_0 \colon & C_1 &\stackrel{}{\to}& A &\hookrightarrow B&
  }
$$

which exists since $C_1$ is a [[projective object]] and $A_0 \to A$ is an epimorphism by $A_\bullet$ being a projective resolution. Here we are using that by exactness the bottom morphism indeed factors through $A$ as indicated, because the definition of $\zeta$ and  the chain complex property of $C_\bullet$ gives 

$$
  \begin{aligned}
    p \circ \zeta \circ d^{C_\bullet}_0 
    &= 
    h_0 \circ d^{C_\bullet}_0
    \\
    & = 0 \circ h_1
    \\
    & = 0 
  \end{aligned}
  \,.
$$ 

Now in the induction step, assuming that $e_{n-1}$ has been been found satisfying the chain complex property, let $e_n$ be a lift in

$$
  \array{
    & && A_n
    \\
    & & {}^{\mathllap{e_{n}}}\nearrow & \downarrow^{\mathrlap{d^{A_\bullet}_{n-1}}}
    \\
    e_{n-1}\circ d_n^{C_\bullet} \colon & C_{n+1} &\stackrel{}{\hookrightarrow}& ker(d^{A_\bullet}_{n-1}) = im(d^{A_\bullet}_{n-1})) &\to& A_{n-1}
  }
  \,,
$$


which again exists since $C_{n+1}$ is projective. That the bottom morphism factors as indicated is the chain complex property of $e_{n-1}$ inside $d^{B_\bullet}_{n-1}$.

To see that the $d^{B_\bullet}$ defines this way indeed squares to 0 notice that

$$
  d^{B_\bullet}_{n}
  \circ
  d^{B_\bullet}_{n+1}
  = 
  \left(
    \array{
       0 &  (-1)^{n}\left(e_{n} \circ d^{C_\bullet}_{n+1} - d^{A_\bullet}_n \circ e_{n+1} \right) 
       \\
       0 & 0
     }
  \right)
  \,.
$$

This vanishes by the very commutativity of the above diagram.


This establishes $g_\bullet$ such that the above diagram commutes and the bottom row is degreewise a short exact sequence, in fact a [[split exact sequence]], by construction. 

To see that $g_\bullet$ is indeed a quasi-isomorphism, consider the [[homology long exact sequence]] associated to the short exact sequence of cochain complexes $0 \to A_\bullet \to B_\bullet \to C_\bullet \to 0$. In positive degrees it implies that the chain homology of $B_\bullet$ indeed vanishes. In degree 0 it gives the short sequence $0 \to A \to H_0(B_\bullet) \to B\to 0$ sitting in a commuting diagram

$$
  \array{
    0 &\to& A &\hookrightarrow& H_0(B_\bullet) &\to& C &\to& 0
    \\
    \downarrow && \downarrow^{\mathrlap{=}} && \downarrow && \downarrow^{\mathrlap{=}} && \downarrow
    \\
    0 &\to& A &\hookrightarrow& B &\to& C &\to& 0 
    \,,
  }
$$

where both rows are exact. That the middle vertical morphism is an [[isomorphism]] then follows by the [[five lemma]].

=--



The formally dual statement to lemma \ref{ProjectiveResolutionOfExactSequenceByExactSequence} is the following.

+-- {: .num_lemma #InjectiveResolutionOfExactSequenceByExactSequence}
###### Lemma

For $0 \to A \to B \to C \to 0$ a [[short exact sequence]]
in an [[abelian category]] with [[injective object|enough injectives]], 
there exists a [[commuting diagram]] of cochain complexes

$$
  \array{
    0 &\to& A &\to& B &\to& C &\to& 0
    \\
      && 
    \downarrow^{\mathrlap{}}
      && 
    \downarrow^{\mathrlap{}}
      && 
    \downarrow^{\mathrlap{}}
    \\
    0 &\to& A^\bullet &\to& B^\bullet &\to& C^\bullet &\to& 0
  }
$$

where 

* each vertical morphism is an injective resolution;

and in addition

* the bottom row is again a short exact sequence of cochain complexes.

=--

+-- {: .proof}
###### Proof

To construct this, let for each $n \in \mathbb{N}$

$$
  B^n \coloneqq A^n \oplus C^n
$$

be the [[direct sum]] and let the bottom horizontal morphisms be the canonical inclusion and projection maps of the direct sum.

Let then furthermore (in [[matrix calculus]] notation)

$$
  j^0 = 
   \left(
     \array{
        j^0_A  
        \\ 
        j^0_B
      }
  \right)
 : B \to A^0 \oplus C^0
$$

be given in the second component by the given composite

$$
  j^0_B : B \to C \to C^0
$$

and in the first component we take

$$
  j^0_A : B \to A^0
$$

to be given by a lift in

$$
  \array{
     A &\to& A^0
     \\
     \downarrow & \nearrow_{\mathrlap{j^0_A}}
     \\
     B
  }
  \,,
$$

which exists by the [[right lifting property]] of the [[injective object]]
$A^0$ (since $A^\bullet$ is an injective resolution) against the [[monomorphism]] $A \to B$ of the [[short exact sequence]].

Let the differentials be given by (...).

This establishes $j^\bullet$ such that the above diagram commutes and the bottom row is degreewise a short exact sequence, in fact a [[split exact sequence]], by construction. 

To see that $j^\bullet$ is indeed a quasi-isomorphism, consider the [[homology long exact sequence]] associated to the short exact sequence of cochain complexes $0 \to A^\bullet \to B^\bullet \to C^\bullet \to 0$ (...).


=--


### Existence and construction of resolutions of complexes
 {#ExistenceAndConstructionOfResolutionsOfComplexes}


+-- {: .num_defn }
###### Definition

If $\mathcal{A}$ has [[projective object|enough projectives]], then every chain complex $C_\bullet \in Ch_\bullet(\mathcal{A})$ has a fully projective (proper) resolution, def. \ref{FullyProjectiveResolutionOfChainComplex}.

=--

+-- {: .proof}
###### Proof

Notice that for each $n \in \mathbb{N}$ we have [[short exact sequences]] of [[chains]], [[cycles]], [[boundaries]] and [[homology groups]] as

$$
  0 \to B_n(C) \to Z_n(C) \to H_n(C) \to 0
$$

$$
  0 \to Z_n(C) \to C_n \to B_{n-1}(C) \to 0
  \,.
$$

Now by prop. \ref{ExistenceOfInjectiveResolutions} we find for each $n \in \mathbb{N}$ projective resolutions of the objects $H_n(C)$ and $B_n(C)$:

$$
  H_{n,\bullet} \stackrel{\simeq_{qi}}{\to} H_n(C)
$$

$$
  B_{n,\bullet} \stackrel{\simeq_{qi}}{\to} B_n(C)
  \,.
$$

Moreover, by prop. \ref{ProjectiveResolutionOfExactSequenceByExactSequence} we find for each $n \in \mathbb{N}$ a projective resolution $Z_{p,\bullet}(C) \stackrel{\simeq_{qi}}{\to} Z_n(C)$ of the object $Z_p(C)$ such that its fits into a [[short exact sequence]] of chain complexes with the previous two chosen resolutions:

$$
  0 \to B_{n,\bullet}(C) \to Z_{n,\bullet}(C) \to H_{n,0}(C) \to 0
  \,.
$$

Analogously, we find for each $n$ a projective resolution $C_{n,\bullet} \to C_n$ that sits in a short exact sequence

$$
  0 \to Z_{n,\bullet} \to C_{n,\bullet} \to B_{n+1,\bullet} \to 0
  \,.
$$

Using the exactness of these sequences one checks now that

1. The $\{C_{n,\bullet}\}_{n \in \mathbb{N}}$ arrange into a [[double complex]] by taking the horizontal differential to be the composite

   $$
     C_{n,k} \to B_{n+1,k} \hookrightarrow Z_{n+1,k} \to C_{n+1,k}
     \,;
   $$

1.  this [[double complex]] $C_{\bullet,\bullet}$ is indeed a fully projective resolution of $C_\bullet$.

=--

### Functorial resolutions and derived functors
 {#FunctorialResolutions}


We discuss how the injective/projective resolutions constructed in _[Existence and construction](#ExistenceAndConstruction)_ are [[functor|functorial]] if regarded in the [[homotopy category of chain complexes]] and how this yields the construction of _[[derived functors in homological algebra]]_.

Write 

$$
  \mathcal{K}^{+}(\mathcal{A}) \hookrightarrow \mathcal{K}(\mathcal{A})
$$ 

for the [[full subcategory]] of the [[homotopy category of chain complexes]] on the one bounded above or bounded below, respectively.
Write 

$$
  \mathcal{K}^+(\mathcal{I}_{\mathcal{A}})
    \hookrightarrow
  \mathcal{K}^+(\mathcal{A})
$$


for the [[full subcategory]] on the degreewise [[injective object|injective]] complexes, and 

$$
  \mathcal{K}^-(\mathcal{P}_{\mathcal{A}})
    \hookrightarrow
  \mathcal{K}^-(\mathcal{A})
$$

for the full subcategory on the degreewise [[projective object|projective]] objects.



+-- {: .num_theorem #InjectiveResolutionFunctors}
###### Theorem

If $\mathcal{A}$ has [enough injectives](injective+object#EnoughInjectives) then there exists a [[functor]]

$$
  P : \mathcal{A} \to \mathcal{K}^+(\mathcal{I}_{\mathcal{A}})
$$

together with a [[natural isomorphisms]]

$$
  H^0(-) \circ P \simeq id_{\mathcal{A}}
$$

and

$$
  H^{n \geq 1}(-) \circ P \simeq 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{ExistenceOfInjectiveResolutions} every object $X^\bullet \in Ch^\bullet(\mathcal{A})$ has an injective resolution. 
Proposition \ref{InjectiveResolutionOfCodomainRespectsMorphisms} says that for $X \to X^\bullet$ and $X \to \tilde X^\bullet$ two resolutions the there is a morphism $X^\bullet \to \tilde X^\bullet$ in $\mathcal{K}^+()$ and prop. \ref{HomotopyUniquenessOfResolutionOfMorphism} says that this morphism is unique in $\mathcal{K}^+(\mathcal{A})$. In particular it is therefore an [[isomorphism]] in $\mathcal{K}^+(\mathcal{A})$ (since the composite with the reverse lifted morphism, also being unique, has to be the identity). 

So choose one such injective resolution $P(X)^\bullet$ for each $X^\bullet$.

Then for $f : X \to Y$ any morphism in $\mathcal{A}$, 
proposition \ref{ExistenceOfInjectiveResolutions} again says that it can be lifted to a morphism between $P(X)^\bullet$ and $P(Y)^\bullet$ and proposition \ref{InjectiveResolutionOfCodomainRespectsMorphisms} says that there is a unique such image in $\mathcal{K}^+(\mathcal{A})$ for morphism making the given diagram commute. 

This implies that this assignment of morphisms is [[functor|functorial]], since then also the composites are unique. 

=--

Dually we have:

+-- {: .num_theorem #ProjectiveResolutionFunctors}
###### Theorem

If $\mathcal{A}$ has [enough projectives](projectice+object#EnoughInjectives) then there exists a [[functor]]

$$
  Q : \mathcal{A} \to \mathcal{K}^-(\mathcal{P}_{\mathcal{A}})
$$

together with a [[natural isomorphisms]]

$$
  H_0(-) \circ P \simeq id_{\mathcal{A}}
$$

and

$$
  H_{n \geq 1}(-) \circ P \simeq 0
  \,.
$$

=--

This is sufficient for the definition and construction of (non-total) [[derived functors]] in the next definition \ref{RightDerivedFunctorOfLeftExactFunctor}. But since that definition is but a model and just for a special case of derived functors, the reader might want to keep the following definition and remark in mind, for conceptual orientation.

+-- {: .num_defn }
###### Definition

Given an [[additive functor]] $F : \mathcal{A} \to \mathcal{A}'$, it canonically induces a functor 

$$
  Ch_\bullet(F) \colon Ch_\bullet(\mathcal{A}) \to Ch_\bullet(\mathcal{A}')
$$

between [[categories of chain complexes]] (its "prolongation") by applying it to each [[chain complex]] and to all the diagrams in the definition of a [[chain map]]. Similarly it preserves [[chain homotopies]] and hence it passes to the quotient given by the strong [[homotopy category of chain complexes]]

$$
  \mathcal{K}(F) \colon \mathcal{K}(\mathcal{A}) \to \mathcal{K}(\mathcal{A}')
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

If $\mathcal{A}$ and $\mathcal{A}'$ have [[projective object|enough projectives]], then their [[derived categories]] are

$$
  \mathcal{D}_\bullet(\mathcal{A}) 
   \simeq 
  \mathcal{K}_\bullet(\mathcal{P}_{\mathcal{A}})
$$

and 

$$
  \mathcal{D}^\bullet(\mathcal{A}) \simeq \mathcal{K}^\bullet(\mathcal{I}_{\mathcal{A}})
$$

etc. One wants to accordingly _derive_ from $F$ a functor $\mathcal{D}_\bullet(\mathcal{A}) \to \mathcal{D}_\bullet(\mathcal{A})$ between these derived categories. It is immediate to achive this on the domain category, there we can simply precompose and form

$$
  \mathcal{A}  
    \to 
  \mathcal{D}_\bullet(\mathcal{A})
   \simeq
  \mathcal{K}(\mathcal{P}_{\mathcal{A}}) 
   \hookrightarrow
  \mathcal{K}(\mathcal{A})
   \stackrel{\mathcal{K}(F)}{\to}
  \mathcal{K}(\mathcal{A}')
  \,.
$$
But the resulting composite lands in $\mathcal{K}(\mathcal{A}')$ and in general does not factor through the inclusion $\mathcal{D}_\bullet(\mathcal{A}') = \mathcal{K}(\mathcal{P}_{\mathcal{A}'}) \hookrightarrow \mathcal{K}(\mathcal{A}')$.

By applying a projective resolution functor _on chain complexes_, one can enforce this factorization. However, by definition of [[resolution]], the resulting chain complex is [[quasi-isomorphism|quasi-isomorphic]] to the one obtained by the above composite. 

This means that if one is only interested in the "weak chain homology type" of the chain complex in the image of a [[derived functor]], then forming [[chain homology]] groups of the chain complexes in the images of the above composite gives the desired information. This is what def. \ref{RightDerivedFunctorOfLeftExactFunctor} and def. \ref{LeftDerivedFunctorOfRightExactFunctor} below do.

=--

+-- {: .num_defn #RightDerivedFunctorOfLeftExactFunctor}
###### Definition

Let 

$$
  F : \mathcal{A} \to \mathcal{A}'
$$

be a [[left exact functor]] between [[abelian categories]] such that $\mathcal{A}$ has [enough injectives](inhective+object#EnoughInjectives). For $n \in \mathbb{N}$ the **$n$th [[right derived functor]]** of $F$ is the composite

$$
  R^n F : 
  \mathcal{A}
   \stackrel{P}{\to}
  K^+(\mathcal{I}_{\mathcal{A}})
   \stackrel{\mathcal{K}(F)}{\to}
  \mathcal{K}^+(\mathcal{A}')
    \stackrel{H^n(-)}{\to}
  \mathcal{A}'
  \,,
$$

where

* $P$ is the injective resolution functor of theorem \ref{InjectiveResolutionFunctors};

* $\mathcal{K}(F)$ is the evident prolongation of $F$ to $\mathcal{K}^+(\mathcal{A})$;

* $H^n(-)$ is the $n$-[[chain homology]] functor. Hence

$$
  (R^n F)(X^\bullet) \coloneqq H^n(F(P(X)^\bullet))
  \,.
$$

=--

Dually:

+-- {: .num_defn #LeftDerivedFunctorOfRightExactFunctor}
###### Definition

Let 

$$
  F : \mathcal{A} \to \mathcal{A}'
$$

be a [[right exact functor]] between [[abelian categories]] such that $\mathcal{A}$ has [enough projectives](projective+object#EnoughProjectives). For $n \in \mathbb{N}$ the **$n$th [[left derived functor]]** of $F$ is the composite

$$
  L_n F : 
  \mathcal{A}
   \stackrel{Q}{\to}
  K^-(\mathcal{P}_{\mathcal{A}})
   \stackrel{\mathcal{K}(F)}{\to}
  \mathcal{K}^-(\mathcal{A}')
    \stackrel{H_n(-)}{\to}
  \mathcal{A}'
  \,,
$$

where

* $Q$ is the projective resolution functor of theorem \ref{ProjectiveResolutionFunctors};

* $\mathcal{K}(F)$ is the evident prolongation of $F$ to $\mathcal{K}^+(\mathcal{A})$;

* $H_n(-)$ is the $n$-[[chain homology]] functor. Hence

$$
  (L_n F)(X_\bullet) \coloneqq H_n(F(Q(X)_\bullet))
  \,.
$$

=--

We discuss now the basic general properties of such derived functors.

+-- {: .num_prop #BasicPropertiesOfDerivedFunctors}
###### Proposition

Let $F \colon \mathcal{A} \to \mathcal{B}$ a [[left exact functor]] in the presence of [[injective object|enough injectives]]. Then for all $X \in \mathcal{A}$ there is a [[natural isomorphism]]

$$
  R^0F(X) \simeq F(X)
  \,.
$$

Dually, of $F$ is a [[right exact functor]] in the presence of [[projective object|enough projectives]], then 

$$
  L_0 F(X) \simeq F(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We discuss the first statement, the second is formally dual. 

By remark \ref{InjectiveResolutionInComponents} an injective resolution $X \stackrel{\simeq_{qi}}{\to} X^\bullet$ is equivalently an [[exact sequence]] of the form

$$
  0 \to X \hookrightarrow X^0 \to X^1 \to \cdots
  \,.
$$

If $F$ is left exact then it preserves this excact sequence by definition of left exactness, and hence 

$$
  0 \to F(X) \hookrightarrow F(X^0) \to F(X^1) \to \cdots
$$

is an exact sequence. But this means that 

$$
  R^0 F(X) \coloneqq ker(F(X^0) \to F(X^1)) \simeq F(X)
  \,.
$$

=--


+-- {: .num_prop #LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence}
###### Proposition

Let $\mathcal{A}, \mathcal{B}$ be [[abelian categories]] and assume that $\mathcal{A}$ has [[injective object|enough injectives]].

Let $F : \mathcal{A} \to \mathcal{B}$ be a [[left exact functor]] and let

$$
  0 \to A \to B \to C \to 0
$$

be a [[short exact sequence]] in $\mathcal{A}$.  

Then there is a [[long exact sequence]] of images of these objects under the right derived functors $R^\bullet F(-)$ of def. \ref{RightDerivedFunctorOfLeftExactFunctor}

$$
  \array{
    0 &\to& R^0F (A)  &\to&  R^0 F(B)  &\to&  R^0 F(C) 
     &\stackrel{\delta_0}{\to}& 
    R^1 F(A) &\to& R^1 F(B) &\to& R^1F(C)
     &\stackrel{\delta_1}{\to}&
    R^2 F(A) &\to& \cdots
    \\
    && \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    0 &\to& F(A) &\to& F(B) &\to& F(C)
  }
$$

in $\mathcal{B}$.

=--

+-- {: .proof}
###### Proof

By lemma \ref{InjectiveResolutionOfExactSequenceByExactSequence} we can find an injective resolution

$$
  0 \to A^\bullet \to B^\bullet \to C^\bullet \to 0
$$

of the given exact sequence which is itself again an exact sequence of cochain complexes.

Since $A^n$ is an [[injective object]] for all $n$, its component sequences $0 \to A^n \to B^n \to C^n \to 0$ are indeed [[split exact sequences]] (see the discussion there). Splitness is preserved by a functor $F$ and so it follows that

$$
  0 \to F(\tilde A^\bullet) \to F(\tilde B^\bullet) \to F(\tilde C^\bullet) \to 0
$$

is a again short exact sequence of cochain complexes, now in $\mathcal{B}$. Hence we have the corresponding [[homology long exact sequence]]


$$
  \cdots
   \to
  H^{n-1}(F(A^\bullet)) \to H^{n-1}(F(B^\bullet)) \to H^{n-1}(F(C^\bullet))
    \stackrel{\delta}{\to}
  H^n(F(A^\bullet)) \to H^n(F(B^\bullet)) \to H^n(F(C^\bullet))
    \stackrel{\delta}{\to}
  H^{n+1}(F(A^\bullet)) \to H^{n+1}(F(B^\bullet)) \to H^{n+1}(F(C^\bullet))
   \to
  \cdots
  \,.
$$

But by construction of the resolutions and by def. \ref{RightDerivedFunctorOfLeftExactFunctor} this is equal to

$$
  \cdots
   \to
  R^{n-1}F(A) \to R^{n-1}F(B) \to R^{n-1}F(C) 
   \stackrel{\delta}{\to}
  R^{n}F(A) \to R^{n}F(B) \to R^{n}F(C) 
    \stackrel{\delta}{\to}
  R^{n+1}F(A) \to R^{n+1}F(B) \to R^{n+1}F(C) 
   \to
  \cdots
  \,.
$$

Finally the equivalence of the first three terms with $F(A) \to F(B) \to F(C)$ is given by prop. \ref{BasicPropertiesOfDerivedFunctors}.

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence} implies that one way to interpret $R^1 F(A)$ is as a "measure for how a [[left exact functor]] $F$ fails to be an [[exact functor]]". For, with $A \to B \to C$ any [[short exact sequence]], this proposition gives the exact sequence

$$
  0 \to F(A) \to F(B) \to F(C) \to R^1 F(A)
$$

and hence $0 \to F(A) \to F(B) \to F(C) \to $ is a short exact sequence itself precisely if $R^1 F(A) \simeq 0$.

=--

In fact we even have the following.

+-- {: .num_prop }

Let $F$ be an [[additive functor]] which is an [[exact functor]]. Then 

$$
  R^{\geq 1} F = 0 
$$

and

$$  
  L_{\geq 1} F = 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because an [[exact functor]] preserves all [[exact sequences]]. If $Y_\bullet \to A$ is a projective resolution then also $F(Y)_\bullet$ is exact in all positive degrees, and hence $L_{n\geq 1} F(A) ) H_{n \geq}(F(Y)) = 0$. Dually for $R^n F$.

=--


We now discuss how the derived functor of an additive functor $F$ may also be computed not necessarily with genuine injective/projective resolutions, but with (just) $F$-injective/$F$-projective resolutions, such as $F$-acyclic resolutions, as defined [above](#FResolutions).

Let $\mathcal{A}$ be an [[abelian category]] with [[injective object|enough injectives]].
Let $F \colon \mathcal{A} \to \mathcal{B}$ be an [[additive functor|additive]] [[left exact functor]] with [[right derived functor]] $R_\bullet F$, def. \ref{RightDerivedFunctorOfLeftExactFunctor}. Finally let $\mathcal{I} \subset \mathcal{A}$ be a subcategory of $F$-injective objects, def. \ref{FInjectives}.


+-- {: .num_lemma #FPreservesNullnessOfFInjectiveComplexes}
###### Lemma

If a [[cochain complex]] $A^\bullet \in Ch^\bullet(\mathcal{I}) \subset Ch^\bullet(\mathcal{A})$ is [[quasi-isomorphism|quasi-isomorphic]] to 0, 

$$
  X^\bullet \stackrel{\simeq_{qi}}{\to} 0
$$

then also $F(X^\bullet) \in Ch^\bullet(\mathcal{B})$ is quasi-isomorphic to 0

$$
  F(X^\bullet) \stackrel{\simeq_{qi}}{\to} 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the following collection of [[short exact sequences]] obtained from the [[long exact sequence]] $X^\bullet$:

$$
  0 \to X^0 \stackrel{d^0}{\to} X^1 \stackrel{d^1}{\to} im(d^1) \to 0
$$

$$
  0 \to im(d^1) \to X^2 \stackrel{d^2}{\to} im(d^2) \to 0
$$

$$
  0 \to im(d^2) \to X^3 \stackrel{d^3}{\to} im(d^3) \to 0
$$

and so on. Going by [[induction]] through this list and using the second condition in def. \ref{FInjectives} we have that all the $im(d^n)$ are in $\mathcal{I}$. Then the third condition in def. \ref{FInjectives} says that all the sequences

$$
  0 \to F(im(d^n)) \to F(X^n+1) \to F(im(d^{n+1})) \to 0
$$

are [[short exact sequence|exact]]. But this means that 

$$
  0 \to F(X^0)\to F(X^1) \to F(X^2) \to \cdots
$$

is exact, hence that $F(X^\bullet)$ is quasi-isomorphic to 0.


=--


+-- {: .num_theorem #DerivedFFromFInjectiveResolution}
###### Theorem

For $A \in \mathcal{A}$ an object with $F$-injective resolution $A \stackrel{\simeq_{qi}}{\to} I_F^\bullet$, def. \ref{FProjectivesResolution}, we have for each $n \in \mathbb{N}$ an [[isomorphism]]

$$  
  R^n F(A) \simeq H^n(F(I_F^\bullet))
$$

between the $n$th right derived functor, def. \ref{RightDerivedFunctorOfLeftExactFunctor} of $F$ evaluated on $A$ and the [[cochain cohomology]] of $F$ applied to the $F$-injective resolution $I_F^\bullet$.

=--

+-- {: .proof}
###### Proof

By prop. \ref{ExistenceOfInjectiveResolutions} we can also find an injective resolution $A \stackrel{\simeq_{qi}}{\to} I^\bullet$. By prop. \ref{InjectiveResolutionOfCodomainRespectsMorphisms} there is a lift of the identity on $A$ to a [[chain map]] $I^\bullet_F \to I^\bullet$ such that the [[diagram]]

$$
  \array{
     A &\stackrel{\simeq_{qi}}{\to}& I_F^\bullet
     \\
     \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{f}}
     \\
     A &\stackrel{\simeq_{qi}}{\to}& I^\bullet
  }
$$

[[commuting diagram|commutes]] in $Ch^\bullet(\mathcal{A})$. Therefore by the [[2-out-of-3]] property of [[quasi-isomorphisms]] it follows that $f$ is a quasi-isomorphism

Let $Cone(f) \in Ch^\bullet(\mathcal{A})$ be the [[mapping cone]] of $f$ and let $I^\bullet \to Cone(f)$ be the canonical [[chain map]] into it. By the explicit formulas for mapping cones, we have that 

1. there is an [[isomorphism]] $F(Cone(f)) \simeq Cone(F(f))$;

1. $Cone(f) \in Ch^\bullet(\mathcal{I})\subset Ch^\bullet(\mathcal{A})$ (because $F$-injective objects are closed under [[direct sum]]).

The first implies that we have a [[homology exact sequence]]

$$
  \cdots \to H^n(I^\bullet) \to H^n(I_F^\bullet) \to H^n(Cone(f)^\bullet)
   \to H^{n+1}(I^\bullet) \to H^{n+1}(I_F^\bullet) \to H^{n+1}(Cone(f)^\bullet) \to \cdots
  \,.
$$

Observe that with $f^\bullet$ a quasi-isomorphism $Cone(f^\bullet)$ is quasi-isomorphic to 0. Therefore 
The second item above implies with lemma \ref{FPreservesNullnessOfFInjectiveComplexes} that also $F(Cone(f))$ is quasi-isomorphic to 0. This finally means that the above homology exact sequences consists of exact pieces of the form

$$
  0 \to (R^n F(A)\coloneqq H^n(I^\bullet) \stackrel{\simeq}{\to} H^n(I_F^\bullet) \to 0
  \,.
$$

=--


### Derived Hom-functor/$Ext$-functor and extensions
 {#DerivedHomFunctor}

Consider the [[derived functor]] of the [[hom functor]].


+-- {: .num_defn #ExtFunctorAsRightDerivedContravariantHom}
###### Definition

For $A \in \mathcal{A}$, write

$$
  Ext^n(-,A) \coloneqq R^n Hom(-,A)
$$

for the [[right derived functor]], def. \ref{RightDerivedFunctorOfLeftExactFunctor}.

=--

We discuss the use of projective resolutions in the computation of [[Ext]]-functors and [[group extensions]].


+-- {: .num_defn #Extensions}
###### Definition

Given $A, G \in \mathcal{A}$, an **[[extension]]** of $G$ by $A$
is a [[short exact sequence]] of the form

$$ 
  0 \to A \to \hat G \to G \to 0
  \,.
$$

Two extensions $\hat G_1$ and $\hat G_2$ are called _equivalent_ if there is a morphism $f : \hat G_1 \to \hat G_2$ in $\mathcal{A}$ such that we have a [[commuting diagram]]

$$
  \array{
     && \hat G_1
     \\
     & \nearrow && \searrow
    \\
    A &&\downarrow^{\mathrlap{f}}&& G
    \\
    & \searrow && \nearrow
    \\
    && \hat G_2
  }
  \,.
$$

Write $Ext(G,A)$ for the set of [[equivalence classes]] of extensions of $G$ by $A$.

=--

+-- {: .num_remark #MorphismOfExtensionIsIsomorphism}
###### Remark

By the [[short five lemma]] a morphism $f$ as above is necessarily an [[isomorphism]] and hence we indeed have an [[equivalence relation]].

=--


+-- {: .num_defn #MapFromExtensionsToExtGroup}
###### Definition

If $\mathcal{A}$ has [[projective object|enough projectives]], define a function

$$
  Extr \colon Ext(G,A) \to Ext^1(G,A)
$$

from the group of extensions, def. \ref{Extensions}, to the first [[Ext functor]] group as follows. Choose any projective resolution $Y_\bullet \stackrel{\simeq_{qi}}{\to} G$, which exists by prop. \ref{ExistenceOfInjectiveResolutions}. Regard then $A \to \hat G \to G\to 0$ as a resolution

$$
  \array{
     \cdots &\to& 0 &\to& 0 &\to& A &\to& \hat G
     \\
     && \downarrow && \downarrow && \downarrow && \downarrow
     \\
     \cdots &\to& 0 &\to& 0 &\to& 0 &\to& G    
  }
$$

of $G$, by remark \ref{ProjectiveResolutionInComponents}. By prop. \ref{InjectiveResolutionOfCodomainRespectsMorphisms} there exists then a [[commuting diagram]] of the form

$$
  \array{
     Y_2 &\to& 0 
     \\
     \downarrow^{\mathrlap{\partial_1^{Y}}} && \downarrow
     \\
     Y_1 &\stackrel{c}{\to}& A
     \\
     \downarrow^{\mathrlap{\partial_0^Y}} && \downarrow
     \\
     Y_0 &\to& \hat G
     \\
     \downarrow && \downarrow
     \\
     G &\stackrel{id}{\to}& G
  }
$$

lifting the identity map on $G$ to a [[chain map]] between the two resolutions.

By the commutativity of the top square, the morphism $c$ is 1-[[cocycle]] in $Hom(Y_\bullet,N)$, hence defines an element in $Ext^1(G,A) \coloneqq H^1(Hom(Y_\bullet,N))$. 

=--

+-- {: .num_prop }
###### Proposition

The construction of def. \ref{MapFromExtensionsToExtGroup} is indeed well defined in that it is independent of the choice of projective resolution as well as of the choice of chain map between the projective resolutions.

=--

+-- {: .proof}
###### Proof

First consider the same projective resolution but another lift $\tilde c$ of the identity.
By prop. \ref{HomotopyUniquenessOfResolutionOfMorphism} any other choice $\tilde c$ fitting into a commuting diagram as above is related by a [[chain homotopy]] to $c$.

$$
  \array{
     Y_2 &\to& 0 
     \\
     \downarrow^{\mathrlap{\partial_1^{Y}}} &\nearrow_{\eta_1 = 0}& \downarrow
     \\
     Y_1 &\stackrel{c - \tilde c}{\to}& A
     \\
     \downarrow^{\mathrlap{\partial_0^Y}} &\nearrow_{\eta_0}& \downarrow
     \\
     Y_0 &\to& \hat G
     \\
     \downarrow &\nearrow_{}& \downarrow
     \\
     G &\to& G
  }
  \,.
$$

The chain homotopy condition here says that 

$$
  c - \tilde c = \eta_0 \circ \partial^{Y}_0 
$$

and hence that in $Hom(Y_\bullet,N)$ we have that $d \eta_0 = c - \tilde c$ is a [[coboundary]]. Therefore for the given choice of resolution $Y_\bullet$ we have obtained a well-defined map

$$
  Ext(G,A) \to Ext^1(G,A)
  \,.
$$

If moreover $Y'_\bullet \stackrel{\simeq_{qi}}{\to} G$ is another projective resolution, with respect to which we define such a map as above, then lifting the identity map on $G$ to a chain map between these resolutions in both directions, by prop. \ref{InjectiveResolutionOfCodomainRespectsMorphisms}, establishes an isomorphism between the resulting maps, and hence the construction is independent also of the choice of resolution.

=--

+-- {: .num_prop #ExtensionFromAnElementOfExt1}
###### Definition

Define a function 

$$
  Rec \colon Ext^1(G,A) \to Ext(G,A)
$$ 

as follows. For $Y_\bullet \to G$ a projective resolution of $G$ and $[c] \in Ext^1(G,A) \simeq H^1(Hom_{\mathcal{A}}(F_\bullet,A))$ an element of the $Ext$-group, let

$$
  \array{
    Y_2 &\to& 0
    \\
    \downarrow && \downarrow
    \\
    Y_1 &\stackrel{c}{\to}& A
    \\
    \downarrow
    \\
    Y_0
    \\
    \downarrow
    \\
    G
  }
$$

be a representative. By the commutativity of the top square this restricts to a morphism

$$
  \array{
     Y_1/Y_2 &\stackrel{c}{\to}& A
     \\
     \downarrow 
     \\
     Y_0
     \\
     \downarrow
     \\
     G
  }
  \,,
$$

where now the left column is itself an extension of $G$ by the [[cokernel]] $Y_1/Y_2$ (because by exactness the kernel of $Y_1 \to Y_0$ is the image of $Y_2$ so that the kernel of $Y_1/Y_2 \to Y_0$ is zero). Form then the [[pushout]] of the horizontal map along the two vertical maps. This yields

$$
  \array{
    Y_1/Y_2 &\stackrel{c}{\to}& A
    \\
    \downarrow && \downarrow
    \\
    Y_0 &\to& Y_0 \coprod_{Y_1/Y_2} A
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{id}{\to}& G
  }
  \,.
$$

Here the bottom right is indeed $G$, by the [[pasting law]] for pushouts and using that the left vertical composite is the [[zero morphism]]. Moreover, the top right morphism is indeed a monomorphism as it is the pushout of a map of modules along an [[injection]]. Similarly the bottom right morphism is an epimorphism. 

Hence $A \to Y_0 \coprod_{Y_1/Y_2} Y_0 \to G$ is an element in $Ext(G,A)$ which we assign to $c$.

=--

+-- {: .num_prop }
###### Proposition

The construction of def. \ref{ExtensionFromAnElementOfExt1} is indeed well defined in that it is independent of the choice of projective resolution as well as of the choice of representative of the $Ext$-element.

=--

+-- {: .proof}
###### Proof

The coproduct $Y_0 \coprod_{Y_1/Y_2} A$ is equivalently 

$$
  coker(Y_1/Y_2 \stackrel{(incl,-c)}{\to} Y_0 \oplus A)
  \,.
$$

For a different representative $\tilde c$ of $[c]$ there is by construction a

$$
  \array{
     Y_1 &\stackrel{\tilde c - c}{\to}& A
     \\
     {}^{\mathllap{\partial_0}}\downarrow & \nearrow_{\lambda}
     \\
     Y_0
  }
  \,.
$$

Define from this a map between the two cokernels induced by the [[commuting diagram]]

$$
  \array{
    Y_1/Y_2 &\stackrel{id}{\to}& Y_1/Y_2
    \\
    \downarrow^{\mathrlap{(id,-c)}} && \downarrow^{\mathrlap{(id,-\tilde c)}}
    \\
    Y_0 \oplus A 
      &\stackrel{\left(\array{ id & 0 \\ \lambda & id }\right)}{\to}& 
    Y_0 \oplus A
  }
  \,.
$$

By construction this respects the inclusion of 
$A \stackrel{(0,id)}{\hookrightarrow} Y_0 \oplus A \to Y_0 \coprod_{Y_1/Y_2} A$. It also manifestly respects the projection to $G$. Therefore this defines a morphism and hence by remark \ref{MorphismOfExtensionIsIsomorphism} even an isomorphism of extensions.


=--


+-- {: .num_prop }
###### Proposition

The functions

$$
  Extr \colon Ext(G,A) \leftrightarrow Ext^1(G,A) \colon Rec
$$

from def. \ref{MapFromExtensionsToExtGroup} to def. \ref{ExtensionFromAnElementOfExt1} are [[inverses]] of each other and hence exhibit a [[bijection]] between extensions of $G$ by $A$ and $Ext^1(G,A)$.

=--

+-- {: .proof}
###### Proof

By straightforward unwinding of the definitions.

In one direction, starting with a $c \in Ext^1(G,A)$ and constructing the extension by pushout, the resulting pushout diagram

$$
  \array{
     Y_1 &\stackrel{c}{\to}& A
     \\
     \downarrow && \downarrow
     \\
     Y_0 &\to& Y_0 \coprod^c_{Y_1/Y_2} A
     \\
     \downarrow && \downarrow
     \\
     G &\stackrel{id}{\to}& G
  }
$$

at the same time exhibits $c$ as the cocycle extracted from the extension $A \to Y_0 \coprod^c_{Y_1/Y_2} A \to G$. 

Conversely, when starting with an extension $A \to \hat G \to G$ then extracting a $c$ by a choice of projective resolution and constructing from that another extension by pushout, the [[universal property]] of the pushout yields a morphism of exensions, which by remark \ref{MorphismOfExtensionIsIsomorphism} is an isomorphism of extensions, hence an equality in $Ext(G,A)$.

=--


### Relation to syzygies

(...) [[syzygy]] (...)


## Examples

### Length-1 resolutions
 {#Lenght1ResolutionsOfAbelianGroups}

+-- {: .num_prop }
###### Proposition

Assuming the [[axiom of choice]],
over $R = \mathbb{Z}$ hence in $R Mod = $ [[Ab]] every object $A$ has a [[projective resolution]], even a  [[free resolution]], of length 1, hence a [[short exact sequence]]

$$
  0 \to F_1 \to F_0 \to A \to 0
$$ 

with $F_1$ and $F_0$ being [[free abelian groups]].

=--

+-- {: .proof}
###### Proof

By the discussion at [free modules - submodules of free modules](free+module#SubmodulesOfFreeModules) a [[subgroup]] of a [[free abelian group]] is again free. Therefore for $p \colon F_0 \to A$ the surjection out of the free group $F_0 \coloneqq F(U(A))$ on the underlying set of $A$, setting $F_1 \coloneqq ker(p)$ yields the desired short exact sequence.

=--

The same argument holds true for $R$ any [[principal ideal domain]].

### Projective resolutions adapted to abelian group cocycles
 {#ProjectiveResolutionsForGroupCocycles}

(...)

### Projective resolutions adapted to general group cohomology {#ProjectiveResolutionsForGroupCohomology}

Let $G$ be a [[discrete group]]. Write $\mathbb{Z}[G]$ for the [[group ring]] over $G$. Notice from _[module -- Abelian groups with G-action as modules over the group ring](module#AbelianGroupsWithGAction)_ that linear $G$-[[actions]] on [[abelian groups]] $A$ are equivalently $\mathbb{Z}[G]$-[[module]] structures in $A$.

We discuss how [[cocycles]] in the [[group cohomology]] of $G$ with [[coefficients]] in such a [[module]] $A$ are naturally encoded in morphisms out of projective resolutions of the trivial $\mathbb{Z}[G]$-module.

+-- {: .num_defn #AugmentationMap}
###### Definition

Write

$$
  \epsilon \colon \mathbb{Z}[G] \to \mathbb{Z}
$$

for the [[homomorphism]] of [[abelian groups]] which forms the sum of $R$-[[coefficients]] of the [[formal linear combinations]] that constitute the group ring

$$
  \epsilon \colon r \mapsto \sum_{g \in G} r_g
  \,. 
$$

This is called the [[augmentation]] map.

=--

+-- {: .num_defn #ProjectiveResolutionForZAsZGModule}
###### Definition

For $n \in \mathbb{N}$ let 

$$
  Q^u_n \coloneqq F(U(G)^{\times^{n}})
$$ 

be the [[free module]] over the [[group ring]] $\mathbb{Z}[G]$ on $n$-[[tuples]] of elements of $G$ (hence $Q^u_0 \simeq \mathbb{Z}[G]$ is the free module on a single generator).

For $n \geq 1$ let $\partial_{n-1} \colon Q^u_n \to Q^u_{n-1}$ be given on [[basis]] elements by

$$
  \partial_{n-1} (g_1, \cdots, g_n)
  \coloneqq 
  g_1 [g_2, \cdots, g_n]
  + 
  \sum_{i = 1}^{n-1} (-1)^i [g_1, \cdots, g_i g_{i+1}, g_{i+2}, \cdots, g_n]
  + 
  (-1)^n [g_1, \cdots, g_{n-1}]
  \,,
$$

where in the first summand we have the coefficient $g_1 \in G \hookrightarrow \mathbb{Z}[G]$ times the basis element $[g_2, \cdots, g_n]$ in $F(U(G)^{n-1})$.

In particular

$$
  \partial_0 \colon [g] \mapsto g[*] - [*] =  g-e \in \mathbb{Z}[G]
  \,.
  \,.
$$

Write furthermore $Q_n$ for the [[quotient]] module $Q^u_n \to Q^n$ which is the [[cokernel]] of the inclusion of those elements for which one of the $g_i$ is the unit element.


=--

+-- {: .num_prop }
###### Proposition

The construction in def. \ref{ProjectiveResolutionForZAsZGModule} defines [[chain complexes]] $Q^u_\bullet$ and $Q_\bullet$ of $\mathbb{Z}[G]$-modules. 
Moreover, with the augmentation map of def. \ref{AugmentationMap} these are projective resolutions

$$
  \epsilon \colon Q^u_\bullet \stackrel{\simeq_{qi}}{\to} \mathbb{Z}
$$

$$
  \epsilon \colon Q_\bullet \stackrel{\simeq_{qi}}{\to} \mathbb{Z}
$$

of $\mathbb{Z}$ equipped with the trivial $\mathbb{Z}[G]$-module structure in $\mathbb{Z}[G]$[[Mod]].

=--

+-- {: .proof} 
###### Proof 

The proof that we have indeed a chain complex is much like the proof of the existence of the [[alternating face map complex]] of a [[simplicial group]], because writing

$$
  \partial^0_n [g_1, \cdots, g_n] \coloneqq g_1 [g_2, \cdots, g_n]
$$

$$
  \partial^i_n [g_1, \cdots, g_n] \coloneqq [g_1, \cdots, g_i g_{i+1}, g_{i+2}, \cdots, g_n]
  \;\;
  for 1 \leq i \leq n-1
$$

$$
  \partial_n [g_1, \cdots, g_n] \coloneqq [g_1, \cdots, g_{n-1}]
$$

one finds that these satisfy the [[simplicial identities]] and that $\partial_n = \sum_{i = 0}^n (-1)^i \partial^i_n$.

That the augmentation map is a [[quasi-isomorphism]] is equivalent, by remark \ref{ProjectiveResolutionInComponents}, to the [[augmentation]]

$$
  \cdots 
  \stackrel{\partial_2}{\to} \mathbb{Z}[G]^2 
  \stackrel{\partial_1}{\to}  
  \mathbb{Z}[G] \stackrel{\epsilon}{\to} \mathbb{Z} \to 0
$$

being an [[exact sequence]]. In fact we show that it is a [[split exact sequence]] by constructing for the canonical chain map to the 0-complex a [[null homotopy]] $s_\bullet$.
To that end, let 

$$
  s_{-1} \colon \mathbb{Z} \to Q^u_0
$$

be given by sending $1 \in \mathbb{Z}$ to the single basis element in $Q^u_0 \coloneqq \mathbb{Z}[G][*] \simeq \mathbb{Z}[G]$, and let for $n \in \mathbb{N}$

$$
  s_n \colon Q^u_n \to Q^u_{n+1}
$$

be given on basis elements by 

$$
  s_n(g[g_1, \cdots, g_n]) \coloneqq [g, g_1, \cdots, g_n]
  \,.
$$

In the lowest degrees we have

$$
  \epsilon \circ s_{-1} = id_{\mathbb{Z}}
$$

because 

$$
  \epsilon(s_{-1}(1)) = \epsilon([*]) = \epsilon(e) = 1
$$

and

$$
  \partial_0 \circ s_0 + s_{-1}\circ \epsilon = id_{Q^u_0}
$$

because for all $g \in G$ we have

$$
  \begin{aligned}
    \partial_0 (s_0(g[*])) + s_{-1}(\epsilon(g[*]))
    & = 
    \partial_0( [g] ) + s_{-1}(1)
    \\
    & = g[*] - [*] + [*]
    \\
    & = 
    g[*]
  \end{aligned}
  \,.
$$

For all remaining $n \geq 1$ we find

$$
  \partial_n \circ  s_n + s_{n-1} \circ \partial_{n-1}
  = 
  id_{Q^u_n}
$$

by a lengthy but straightforward computation. This shows that every cycle is a boundary, hence that we have a resolution.

Finally, since the chain complex $Q^u_\bullet$ consists by construction degreewise of [[free modules]] hence in particular of a [[projective module]], it is a projective resolution.

=--

+-- {: .num_prop }
###### Propoition

For $A$ an [[abelian group]] equipped with a linear $G$-[[action]] and for $n \in \mathbb{N}$, the degree-$n$ [[group cohomology]] $H^n_{grp}(G, A)$ of $G$ with [[coefficients]] in $A$ is equivalently given by

$$
  \begin{aligned}
    H^n_{Grp}(G,A) & \simeq Ext^n_{\mathbb{Z}[G]}(\mathbb{Z}, A)
    \\
    & \simeq H^n(Hom_{\mathbb{Z}[G]}(Q^u_n, A))
    \\
    & \simeq H^n(Hom_{\mathbb{Z}[G]}(Q_n, A))
    \,.
  \end{aligned}
  \,,
$$

where on the right we canonically regard $A \in \mathbb{Z}[G]$[[Mod]].

=--

+-- {: .proof} 
###### Proof 

By the [[free functor]] [[adjunction]] we have that 

$$
  Hom_{\mathbb{Z}[G]}(F^u_n, A)  
  \simeq
  Hom_{Set}(U(G)^{\times n}, U(A))
$$

is the set of [[functions]] from $n$-tuples of elements of $G$ to elements of $A$. It is immediate to check that these are in the [[kernel]] of $Hom_{\mathbb{Z}[G]}(\partial_{n}, A)$ precisely if they are [[cocycles]] in the [[group cohomology]] (by comparison with the explicit formulas there) and that they are group cohomology [[coboundaries]] precisely if they are in the [[image]] of $Hom_{\mathbb{Z}[G]}(\partial_{n-1}, A)$. This establishes the first equivalences.

Similarly one finds that $H^n(Hom(F_n, A)))$ is the sub-group of _normalized_ cocycles. By the discussion at _[[group cohomology]]_ these already support the entire group cohomology (every cocycle is comologous to a normalized one).

=--

### Cohomology of cyclic groups 
 {#CohomologyOfCyclicGroups}

Let $G = C_k$ be a [[cyclic group]] of finite [[order]] $k$, with generator $g$. We discuss the [[group cohomology]] of $G$, as discussed at _[group cohomology - In terms of homological algebra](http://ncatlab.org/nlab/show/group+cohomology#InTermsOfHomologicalAlgebra)_.

Define special elements in the [[group algebra]] $\mathbb{Z}G$: 

$$N \coloneqq 1 + g + g^2 + \ldots + g^{k-1}$$ 

$$\,$$ 

$$D \coloneqq g - 1,$$

and denote the corresponding multiplications by these elements by the same letters $N, D \colon \mathbb{Z}G \to \mathbb{Z}G$. 

Then a very simple and useful projective resolution of the trivial $\mathbb{Z}G$-module $\mathbb{Z}$ is based on an [[exact sequence]] of $\mathbb{Z}G$-[[modules]]

$$\ldots \stackrel{N}{\to} \mathbb{Z}G \stackrel{D}{\to} \mathbb{Z}G \stackrel{N}{\to} \mathbb{Z}G \stackrel{D}{\to} \mathbb{Z}G \to \mathbb{Z} \to 0$$ 

where the last map $\mathbb{Z}G \to \mathbb{Z}$ is induced from the trivial group homomorphism $G \to 1$, hence is the map that forms the sum of all [[coefficients]] of all group elements.

It follows from this resolution that the [[cochain cohomology|cohomology groups]] $H^n(C_k, A)$ for a $C_k$-[[module]] $A$ are periodic of order 2: 

$$
  H^{n+2}(C_k, A) \cong H^n(C_k, A)
$$ 

for $n \geq 1$. More precisely, 

+-- {: .num_prop} 
###### Proposition 
For $G = C_k$, we have 

* $H^0(G, A) = A^G = \ker(D) \colon A \to A$, 

* $H^{2 j + 1}(G, A) = \ker(N)/im(D)$ for $j \geq 0$, 

* $H^{2 j}(G, A) = \ker(D)/im(N)$ for $j \geq 1$. 
=-- 

A well-known calculation in the cohomology of cyclic groups is **[[Hilbert's Theorem 90]]**. 

+-- {: .num_theorem} 
###### Theorem 
Suppose $K$ be a finite [[Galois extension]] of a [[field]] $k$, with a cyclic [[Galois group]] $G = \langle g \rangle$ of order $n$. Regard the [[multiplicative group]] $K^\ast$ as a $G$-module. Then $H^1(G, K^\ast) = 0$. 

=-- 

+-- {: .proof} 
###### Proof 

Let $\sigma \in \mathbb{Z}G$, and denote the action of $\sigma$ on an element $\beta \in K$ by exponential notation $\beta^\sigma$. The action of the element $N \in \mathbb{Z}G$ is 

$$\beta^N = \beta^{1 + g + \ldots + g^{n-1}} = \beta \cdot \beta^g \cdot \ldots \beta^{g^{n-1}}$$ 

which is precisely the _norm_ $N(\beta)$. We are to show that if $N(\beta) = 1$, then there exists $\alpha \in K$ such that $\beta = \alpha/g(\alpha)$. 
By the lemma that follows, the homomorphisms $1, g, \ldots, g^{n-1}: K^\ast \to K^\ast$ are, when considered as elements in a vector space of $K$-valued functions, $K$-linearly independent. It follows in particular that 

$$1 + \beta g + \beta^{1+g}g^2 + \ldots + \beta^{1 + g + \ldots + g^{n-2}}g^{n-1}$$ 

is not identically zero, and therefore there exists $\theta \in K^\ast$ such that the element 

$$\alpha = \theta + \beta \theta^g + \beta^{1+g}\theta^{g^2} + \ldots + \beta^{1 + g + \ldots + g^{n-2}}\theta^{g^{n-1}}$$ 

is non-zero. Using the fact that $N(\beta) = 1$, one may easily calculate that $\beta \alpha^g = \alpha$, as was to be shown. 
=-- 

The next result may be thought of as establishing "independence of characters" (where "[[group character|characters]]" are valued in the [[multiplicative group]] of a field): 

+-- {: .num_lemma} 
###### Lemma 

Let $K$ be a [[field]], let $G$ be a [[monoid]], and let $\chi_1, \ldots, \chi_n \colon G \to K^\ast$ be distinct monoid [[homomorphisms]]. Then the [[functions]] $\chi_i$, considered as functions valued in $K$, are $K$-[[linear independence|linearly independent]]. 

=-- 

+-- {: .proof} 
###### Proof 
A single $\chi \colon G \to K^\ast$ obviously forms a linearly independent set. Now suppose we have an equation 

\[a_1 \chi_1 + \ldots + a_n \chi_n = 0\]

where $a_i \in K$, and assume $n$ is as small as possible. In particular, no $a_i$ is equal to $0$, and $n \geq 2$. Choose $g \in G$ such that $\chi_1(g) \neq \chi_2(g)$. Then for all $h \in G$ we have 

$$a_1 \chi_1(g h) + \ldots + a_n \chi_n(g h) = 0$$ 

so that 

\[a_1 \chi_1(g) \chi_1 + \ldots + a_n \chi_n(g)\chi_n = 0.\] 

Dividing equation 2 by $\chi_1(g)$ and subtracting from it equation 1, the first term cancels, and we are left with a shorter relation 

$$(a_2\frac{\chi_2(g)}{\chi_1(g)} - a_2)\chi_2 + \ldots = 0$$ 

which is a [[contradiction]]. 

=-- 

## Related concepts
 {#RelatedConcepts}

* [[projective object]], [[projective presentation]], [[projective cover]], **projective resolution**

  * [[projective module]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]

## References

* {#HiltonStammbach71} [[Peter Hilton]],  [[Urs Stammbach]], p. 129 of: _A course in homological algebra_, Springer-Verlag, New York, 1971, Graduate Texts in Mathematics, Vol. 4 ([doi:10.1007/978-1-4419-8566-8](https://link.springer.com/book/10.1007/978-1-4419-8566-8), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/hilton-stammbach.pdf))


* {#Schapira} [[Pierre Schapira]], section 4.5 of: _Categories and homological algebra_ (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))
 

* {#May} [[Peter May]], sections 3.1 and 4.2 in: _Notes on Tor and Ext_ ([pdf](http://www.math.uchicago.edu/~may/MISC/TorExt.pdf))
 

* {#Murfet} [[Daniel Murfet]], section 4 of: _Derived functors_ ([pdf](http://therisingsea.org/notes/DerivedFunctors.pdf))
 

[[!redirects projective resolutions]]

[[!redirects injective resolution]]
[[!redirects injective resolutions]]

[[!redirects acyclic resolution]]
[[!redirects acyclic resolutions]]

