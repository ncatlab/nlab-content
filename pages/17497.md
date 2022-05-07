

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***

_We give an introduction to the [[stable homotopy category]] and to its key computational tool, the [[Adams spectral sequence]]. To that end we introduce the modern tools, such as [[model categories]] and [[highly structured ring spectra]]. In the accompanying [[Introduction to Stable homotopy theory -- S|seminar]] we consider applications to [[cobordism theory]] and [[complex oriented cohomology]] such as to converge in the end to a glimpse of the modern picture of [[chromatic homotopy theory]]._

***

Lecture notes.

Main page: _[[Introduction to Stable homotopy theory]]_.

Previous section: _[[Introduction to Stable homotopy theory -- P|Prelude -- Classical homotopy theory]]_

This section: _[[Introduction to Stable homotopy theory -- 1|Part 1 -- Stable homotopy theory]]_

Previous subsection: _[[Introduction to Stable homotopy theory -- 1|Part 1.1 -- Stable homotopy theory -- Sequential spectra]]_

This subsection: **Part 1.2 - Stable homotopy theory -- Structured spectra**

Next section: _[[Introduction to Stable homotopy theory -- 2|Part 2 -- Adams spectral sequences]]_

***

<br/>


#Stable homotopy theory -- Structured spectra#
* table of contents
{:toc}

$\,$

The key result of [[Introduction to Stable homotopy theory -- 1-1|part 1.1]] was ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory)) the construction of a [[stable homotopy theory]] of [[spectra]], embodied by a stable [[model structure on topological sequential spectra]] $SeqSpec(Top_{cg})_{stable}$ ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentialSpectraIsModelCategory)) with its corresponding [[stable homotopy category]] $Ho(Spectra)$, which stabilizes the canonical looping/suspension adjunction on [[pointed topological spaces]] in that it fits into a diagram of (Quillen-)adjunctions of the form

$$
  \array{
     (Top_{cg}^{\ast/})_{Quillen}
      &
      \underoverset{\underoverset{\Omega}{\bot}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{}
      &
     (Top^{\ast/}_{cg})_{Quillen}
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     SeqSpec(Top_{cg})_{stable}
     &
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\simeq_{\mathrlap{Q}}}
     &
     SeqSpec(Top_{cg})_{stable}
  }
  \;\;\;\;\;\;\;\;\;\;\;
    \overset{\gamma}{\longrightarrow}
  \;\;\;\;\;\;\;\;\;\;\;
  \array{
    Ho(Top^{\ast/})
    &
      \underoverset
        {\underset{\Omega}{\longrightarrow}}
        {\overset{\Sigma}{\longleftarrow}}
        {\bot}
    &
    Ho(Top^{\ast/})
    \\
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
    &&
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
    \\
    Ho(Spectra)
    &
      \underoverset
        {\underset{\Omega}{\longrightarrow}}
        {\overset{\Sigma}{\longleftarrow}}
        {\simeq}
    &
    Ho(Spectra)
  }
  \,.
$$

But fitting into such a diagram does not yet uniquely characterize the stable homotopy category. For instance the trivial category on a single object would also form such a diagram. On the other hand, there is more canonical structure on the category of pointed topological spaces which is not yet reflected here.

Namely the [[smash product]]

$$
  \wedge \;\colon\; Ho(Top^{\ast/}) \longrightarrow Ho(Top^{\ast/})
$$

of [[pointed topological spaces]] gives it the structure of a [[monoidal category]] (def. \ref{MonoidalCategory} below), and so it is natural to ask that the above stabilization diagram reflects and respects that extra structure. This means that there should be a [[smash product of spectra]]

$$
  \wedge \;\colon\; Ho(Spectra) \longrightarrow Ho(Spectra)
$$

such that $(\Sigma^\infty \dashv \Omega^\infty)$ is compatible, in that

$$
  \Sigma^\infty (X\wedge Y) \simeq (\Sigma^\infty X) \wedge (\Sigma^\infty Y)
$$

(a "[[strong monoidal functor]]", def. \ref{LaxMonoidalFunctor} below).

We had already seen [in part 1.1](Introduction+to+Stable+homotopy+theory+--+1-1#Additivity) that $Ho(Spectra)$ is an [[additive category]], where [[wedge sum]] of spectra is a [[direct sum]] operation $\oplus$. We discuss here that the [[smash product of spectra]] is the corresponding operation analogous to a [[tensor product of abelian groups]].


| [[abelian groups]] | [[spectra]] |
|--------------------|-------------|
| $\oplus$ [[direct sum]]  | $\vee$ [[wedge sum]]  |
| $\otimes$ [[tensor product of abelian groups|tensor product]] | $\wedge$ [[smash product of spectra|smash product]] |

This further strenghtens the statement that [[spectra]] are the analog in [[homotopy theory]] of [[abelian groups]]. In particular, with respect to the smash product of spectra, the [[sphere spectrum]] becomes a [[ring spectrum]] that is the coresponding analog of the ring of [[integers]].

With the analog of the tensor product in hand, we may consider doing [[algebra]] -- the theory of [[rings]] and their [[modules]] -- [[internalization|internal]] to spectra. This "[[higher algebra]]" accordingly is the theory of _[[ring spectra]]_ and _[[module spectra]]_.

[[!include homological and higher algebra -- table]]

Where a [[ring]] is equivalently a [[monoid]] with respect to the [[tensor product of abelian groups]], we are after a corresponding [[tensor product]] of [[spectra]]. This is to be the [[smash product of spectra]], induced by the [[smash product]] on [[pointed topological spaces]].

In particular the [[sphere spectrum]] becomes a [[ring spectrum]] with respect to this smash product and plays the role analogous to the ring of [[integers]] in abelian groups

| [[abelian groups]] | [[spectra]] |
|--------------------|-------------|
| $\mathbb{Z}$ [[integers]] | $\mathbb{S}$ [[sphere spectrum]] |

Using this structure there is finally a full characterization of [[stable homotopy theory]], we state (without proof) this _Schwede-Shipley uniqueness_ as theorem \ref{CharacterizationOfStableHomotopyTheory} below.

There is a key point to be dealt with here: the [[smash product of spectra]] has to exhibit a certain _graded commutativity_. Informally, there are two ways to see this:

First, we have seen above that under the [[Dold-Kan correspondence]] [[chain complexes]] yield examples of spectra. But the [[tensor product of chain complexes]] is graded commutative.

Second, more fundamentally, we see in the discussion of the [[Brown representability theorem]] ([here](#BrownRepresentabilityTheorem)) that every ([[sequential spectrum|sequential]]) [[spectrum]] $A$ induces a [[generalized homology theory]] given by the formula $X \mapsto \pi_\bullet(E \wedge X)$ (where the smash product is just the degreewise smash of pointed objects). By the [[suspension isomorphism]] this is such that for $X = S^n$ the [[n-sphere]], then $\pi_{\bullet\geq 0}(E \wedge S^n) \simeq \pi_{\bullet \geq 0}(E_n)$. This means that instead of thinking of a [[sequential spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#SequentialSpectra)) as indexed on the [[natural numbers]] equipped with [[addition]] $(\mathbb{N},+)$, it may be more natural to think of sequential spectra as indexed on the [[n-spheres]] equipped with their smash product of pointed spaces $(\{S^n\}_n, \wedge)$.


+-- {: .num_prop #GradedCommutativityOfSmashOfSpheres}
###### Proposition

There are [[homeomorphisms]] between [[n-spheres]] and their [[smash products]]

$$
  \phi_{n_1,n_2}
  \;\colon\;
  S^{n_1} \wedge S^{n_2}
  \stackrel{\simeq}{\longrightarrow}
  S^{n_1 + n_2}
$$

such that in [[Ho(Top)]] there are [[commuting diagrams]] like so:

$$
  \array{
    (S^{n_1} \wedge S^{n_2}) \wedge S^{n_3}
    &&\stackrel{\simeq}{\longrightarrow}&&
    S^{n_1} \wedge (S^{n_2} \wedge S^{n_3})
    \\
    {}^{\mathllap{\phi_{n_1,n_2} \wedge id}}\downarrow
    && && \downarrow^{\mathrlap{id \wedge \phi_{n_2,n_3}}}
    \\
    S^{n_1+n_2} \wedge S^{n_3}
    && &&
    S^{n_1}\wedge S^{n_2 + }
    \\
    & {}_{\mathllap{\phi_{n_1+n_2, n_3}}}\searrow && \swarrow_{\mathrlap{\phi_{n_1,n_2+n_3}}}
    \\
    &&
    S^{n_1+n_2 + n_3}
  }
  \,.
$$

and

$$
  \array{
    S^{n_1} \wedge S^{n_2}
    &\stackrel{b_{n_1,n_2}}{\longrightarrow}&
    S^{n_2} \wedge S^{n_1}
    \\
    {}^{\mathllap{\phi_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\phi_{n_2,n_1}}}
    \\
    S^{n_1 + n_2}
    &\stackrel{(-1)^{n_1 n_2}}{\longrightarrow}&
    S^{n_1 + n_2}
  }
  \,,
$$

where here $(-1)^n \colon S^n \to S^n$ denotes the homotopy class of a [[continuous function]] of [[degree of a continuous function|degree]] $(-1)^n \in \mathbb{Z} \simeq [S^n, S^n]$.


=--


+-- {: .proof}
###### Proof

With the [[n-sphere]] $S^n$ realized as the [[one-point compactification]] of the [[Cartesian space]] $\mathbb{R}^n$, then $\phi_{n_1,n_2}$ is given by the identity on [[coordinates]] and the [[braiding]] homeomorphism

$$
  b_{n_1,n_2}
  \;\colon\;
  S^{n_1} \wedge S^{n_2}
  \stackrel{\sigma}{\longrightarrow}
  S^{n_2} \wedge S^{n_1}
$$

is given by permuting the [[coordinates]]:

$$
  (x_1, \cdots, x_{n_1}, y_1, \cdots, y_{n_2})
  \mapsto
  (y_1, \cdots, y_{n_2}, x_1, \cdots, x_{n_1})
  \,.
$$

This has [[degree of a continuous map|degree]] $(-1)^{n_1 n_2}$ .

=--


This phenomenon suggests that as we "[[categorify]]" the [[natural numbers]] to the [[n-spheres]], hence the [[integers]] to the [[sphere spectrum]], and as we think of the $n$th component space of a [[sequential spectrum]] as being the value assigned to the [[n-sphere]]

$$
  E_n \simeq E(S^n)
$$

then there should be a possibly non-trivial [[action]] of the [[symmetric group]] $\Sigma_n$ on $E_n$, due to the fact that there is such an action of $S^n$ which is non-trivial according to prop. \ref{GradedCommutativityOfSmashOfSpheres}.

We discuss two ways of making this precise below in  _[Symmetric and orthogonal spectra](#SymmetricSpectra)_, and we discuss how these are unified by a concept of [[module objects]] over a [[monoid object]] representing the [[sphere spectrum]] below in _[S-modules](#SModules)_.

The general abstract theory for handling this is _[[monoidal category|monoidal]] and [[enriched category theory]]_. We first develop the relevant basics in _[Categorical algebra](#MonoidalAndEnrichedCategories)_.



## Categorical algebra
 {#MonoidalAndEnrichedCategories}

When defining a [[commutative ring]] as an [[abelian group]] $A$ equipped with an [[associativity|associative]], commutative and [[unit|untial]] [[bilinear map|bilinear]] pairing

$$
  A \otimes_{\mathbb{Z}} A \overset{(-)\cdot (-)}{\longrightarrow} A
$$

one evidently makes crucial use of the [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$. That tensor product itself gives the [[category]] [[Ab]] of all abelian groups a structure similar to that of a ring, namely it equips it with a pairing

$$
  Ab \times Ab
    \overset{(-)\otimes_{\mathbb{Z}}(-)}{\longrightarrow}
  Ab
$$

that is a [[functor]] out of the [[product category]] of [[Ab]] with itself, satisfying category-theoretic analogs of the properties of associativity, commutativity and unitality.

One says that a ring $A$ is a _[[commutative monoid]]_ in the category [[Ab]] of abelian groups, and that this concept makes sense since $Ab$ itself is a _[[symmetric monoidal category]]_.

Now in [[stable homotopy theory]], as we have seen [above](#StableHomotopyCategory), the category [[Ab]] is improved to the [[stable homotopy category]] $Ho(Spectra)$ (def. \ref{TheStableHomotopyCategory}), or rather to any [[stable model category|stable]] [[model structure on spectra|model structure on spectra]] presenting it. Hence in order to correspondingly refine commutative monoids in [[Ab]] (namely [[commutative rings]]) to commutative monoids in [[Ho(Spectra)]] (namely [[commutative ring spectra]]), there needs to be a suitable [[symmetric monoidal category]] structure on the category of spectra. Its analog of the [[tensor product of abelian groups]] is to be called the _[[symmetric monoidal smash product of spectra]]_. The problem is how to construct it.

The theory for handling such a problem is _[[categorical algebra]]_. Here we discuss the minimum of categorical algebra that will allow us to elegantly construct the [[symmetric monoidal smash product of spectra]].





### Monoidal topological categories

We want to lift the concepts of _[[ring]]_ and _[[module]]_ from _[[abelian groups]]_ to _[[spectra]]_. This requires a general idea of what it means to generalize these concepts at all. The abstract theory of such generalizations is that of _[[monoid in a monoidal category]]_.

We recall the basic definitions of [[monoidal categories]] and of [[monoid in a monoidal category|monoids]] and [[module object|modules]] [[internalization|internal]] to monoidal categories. We list archetypical examples at the end of this section, starting with example \ref{TopAsASymmetricMonoidalCategory} below. These examples are all fairly immediate. The point of the present discussion is to construct the non-trivial example of [[Day convolution]] monoidal stuctures [below](#TopologicalDayConvolution).


+-- {: .num_defn #MonoidalCategory}
###### Definition

A **(pointed) [[topologically enriched category|topologically enriched]] [[monoidal category]]** is a (pointed) [[topologically enriched category]] $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) equipped with

1. a (pointed) [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

   $$
      \otimes
        \;\colon\;
      \mathcal{C} \times \mathcal{C}
       \longrightarrow
      \mathcal{C}
   $$

   out of the (pointed) topologival [[product category]] of $\mathcal{C}$ with itself (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), called the **[[tensor product]]**,

1. an object

   $$
     1 \in \mathcal{C}
   $$

   called the **[[unit object]]** or **[[tensor unit]]**,

1. a [[natural isomorphism]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor))

   $$
     a
       \;\colon\;
     ((-)\otimes (-)) \otimes (-)
       \overset{\simeq}{\longrightarrow}
     (-) \otimes ((-)\otimes(-))
   $$

   called the **[[associator]]**,

1. {#MonoidalCategoryUnitors} a [[natural isomorphism]]

   $$
     \ell
       \;\colon\;
     (1 \otimes (-))
       \overset{\simeq}{\longrightarrow}
     (-)
   $$

   called the **[[left unitor]]**, and a natural isomorphism

   $$
     r \;\colon\; (-) \otimes 1 \overset{\simeq}{\longrightarrow} (-)
   $$

   called the **[[right unitor]]**,

such that the following two kinds of [[commuting diagram|diagrams commute]], for all objects involved:

1. **triangle identity**:

   $$
     \array{
        & (x \otimes 1) \otimes y &\stackrel{a_{x,1,y}}{\longrightarrow} & x \otimes (1 \otimes y)
         \\
         & {}_{\rho_x \otimes 1_y}\searrow
         && \swarrow_{1_x \otimes \lambda_y}
         &
        \\
        &&
        x \otimes y
        &&
     }
   $$


1. the **[[pentagon identity]]**:

   $$
     \array{
       && (w \otimes x) \otimes (y \otimes z)
       \\
       & {}^{\mathllap{\alpha_{w \otimes x, y, z}}}\nearrow
        &&
       \searrow^{\mathrlap{\alpha_{w,x,y \otimes z}}}
       \\
       ((w \otimes x ) \otimes y) \otimes z
        && &&
       (w \otimes (x \otimes (y \otimes z)))
       \\
       {}^{\mathllap{\alpha_{w,x,y}} \otimes id_z }\downarrow
        && &&
       \uparrow^{\mathrlap{ id_w \otimes \alpha_{x,y,z} }}
       \\
       (w \otimes (x \otimes y)) \otimes z
         && \underset{\alpha_{w,x \otimes y, z}}{\longrightarrow} &&
       w \otimes ( (x \otimes y) \otimes z )
     }
   $$


=--


+-- {: .num_lemma #kel1}
###### Lemma
**([Kelly 64](monoidal+category#Kelly))**

Let $(\mathcal{C}, \otimes, 1)$ be a [[monoidal category]], def. \ref{MonoidalCategory}. Then the left and right [[unitors]] $\ell$ and $r$ satisfy the following conditions:

1. $\ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1$;

1. for all objects $x,y \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]:

   $$
     \array{
       (1 \otimes x) \otimes y  & &
       \\
       {}^\mathllap{\alpha_{1, x, y}} \downarrow
       & \searrow^\mathrlap{\ell_x \otimes id_y} &
       \\
       1 \otimes (x \otimes y)
       & \underset{\ell_{x \otimes y}}{\longrightarrow} & x \otimes y
     }
     \,;
   $$

   and

   $$
     \array{
       x \otimes (y \otimes 1) & &
       \\
       {}^\mathllap{\alpha^{-1}_{1, x, y}} \downarrow
       & \searrow^\mathrlap{id_x \otimes r_y} &
       \\
       (x \otimes y) \otimes 1
         &
           \underset{r_{x \otimes y}}{\longrightarrow}
         &
       x \otimes y
     }
     \,;
   $$

=--

For **proof** see at _[[monoidal category]]_ [this lemma](monoidal+category#kel1) and [this lemma](monoidal+category#kel2).

+-- {: .num_remark #CoherenceForMonoidalCategories}
###### Remark

Just as for an [[associative algebra]] it is sufficient to demand $1 a = a$ and $a 1 = a$ and $(a b) c = a (b c)$ in order to have that expressions of arbitrary length may be re-bracketed at will, so there is a _[[coherence theorem for monoidal categories]]_ which states that all ways of freely composing the [[unitors]] and [[associators]] in a [[monoidal category]] (def. \ref{MonoidalCategory}) to go from one expression to another will coincide. Accordingly, much as one may drop the notation for the bracketing in an [[associative algebra]] altogether, so one may, with due care, reason about monoidal categories without always making all unitors and associators explicit.

(Here the qualifier "freely" means informally that we must not use any non-formal identification between objects, and formally it means that the diagram in question must be in the image of a [[strong monoidal functor]] from a _free_ monoidal category. For example if in a particular monoidal category it so happens that the object $X \otimes (Y \otimes Z)$ is actually _equal_ to $(X \otimes Y)\otimes Z$, then the various ways of going from one expression to another using only associators _and_ this equality no longer need to coincide.)

=--

+-- {: .num_defn #BraidedMonoidalCategory}
###### Definition

A **(pointed) [[topologically enriched category|topological]] [[braided monoidal category]]**, is a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $\mathcal{C}$ (def. \ref{MonoidalCategory}) equipped with a [[natural isomorphism]]

$$
  \tau_{x,y} \colon x \otimes y \to y \otimes x
$$

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved ("hexagon identities"):

$$
  \array{
   (x \otimes y) \otimes z
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{\tau_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{\tau_{x,y}\otimes Id}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{Id \otimes \tau_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

and

$$
  \array{
   x \otimes (y \otimes z)
   &\stackrel{a^{-1}_{x,y,z}}{\to}&
   (x \otimes y) \otimes z
   &\stackrel{\tau_{x \otimes y, z}}{\to}&
   z \otimes (x \otimes y)
   \\
   \downarrow^{Id \otimes \tau_{y,z}}
   &&&&
   \downarrow^{a^{-1}_{z,x,y}}
   \\
   x \otimes (z \otimes y)
   &\stackrel{a^{-1}_{x,z,y}}{\to}&
   (x \otimes z) \otimes y
   &\stackrel{\tau_{x,z} \otimes Id}{\to}&
   (z \otimes x) \otimes y
  }
  \,,
$$

where $a_{x,y,z} \colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ denotes the components of the [[associator]] of $\mathcal{C}^\otimes$.

=--

+-- {: .num_defn #SymmetricMonoidalCategory}
###### Definition

A **(pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]]** is a (pointed) topological [[braided monoidal category]] (def. \ref{BraidedMonoidalCategory}) for which the [[braiding]]

$$
   \tau_{x,y} \colon x \otimes y \to y \otimes x
$$

satisfies the condition:

$$
  \tau_{y,x} \circ \tau_{x,y} = 1_{x \otimes y}
$$

for all objects $x, y$

=--

+-- {: .num_remark #SymmetricMonoidalCategoriesCoherenceTheorem}
###### Remark

In analogy to the [[coherence theorem for monoidal categories]] (remark \ref{CoherenceForMonoidalCategories}) there is a [[coherence theorem for symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}), saying that every diagram built freely (see remark \ref{SymmetricMonoidalCategoriesCoherenceTheorem}) from [[associators]], [[unitors]] and [[braidings]] such that both sides of the diagram correspond to the same [[permutation]] of objects, coincide.

=--


+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[symmetric monoidal category]] $\mathcal{C}$ with [[tensor product]] $\otimes$ (def. \ref{SymmetricMonoidalCategory}) it is called a **[[closed monoidal category]]** if for each $Y \in \mathcal{C}$ the functor $Y \otimes(-)\simeq (-)\otimes Y$ has a [[right adjoint]], denoted $hom(Y,-)$

$$
  \mathcal{C}
    \underoverset
      {\underset{hom(Y,-)}{\longrightarrow}}
      {\overset{(-) \otimes Y}{\longleftarrow}}
      {\bot}
  \mathcal{C}
  \,,
$$

hence if there are [[natural bijections]]

$$
  Hom_{\mathcal{C}}(X \otimes Y, Z)
   \;\simeq\;
  Hom_{\mathcal{C}}{C}(X, hom(Y,Z))
$$

for all objects $X,Z \in \mathcal{C}$.

Since for the case that $X = 1$ is the [[tensor unit]] of $\mathcal{C}$ this means that

$$
  Hom_{\mathcal{C}}(1,hom(Y,Z)) \simeq Hom_{\mathcal{C}}(Y,Z)
  \,,
$$

the object $hom(Y,Z) \in \mathcal{C}$ is an enhancement of the ordinary [[hom-set]] $Hom_{\mathcal{C}}(Y,Z)$ to an object in $\mathcal{C}$.
Accordingly, it is also called the **[[internal hom]]** between $Y$ and $Z$.

=--


In a [[closed monoidal category]], the adjunction isomorphism between [[tensor product]] and [[internal hom]] even holds internally:

+-- {: .num_prop #TensorHomAdjunctionIsoInternally}
###### Proposition

In a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) there are [[natural isomorphisms]]

$$
  hom(X \otimes Y, Z)
   \;\simeq\;
  hom(X, hom(Y,Z))
$$

whose image under $Hom_{\mathcal{C}}(1,-)$ are the defining [[natural bijections]] of def. \ref{ClosedMonoidalCategory}.

=--

+-- {: .proof}
###### Proof

Let $A \in \mathcal{C}$ be any object. By applying the defining natural bijections twice, there are composite natural bijections

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(A , hom(X \otimes Y, Z))
    & \simeq
    Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}((A \otimes X)\otimes Y, Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}(A \otimes X, hom(Y,Z))
    \\
    & \simeq
    Hom_{\mathcal{C}}(A, hom(X,hom(Y,Z)))
  \end{aligned}
  \,.
$$

Since this holds for all $A$, the [[Yoneda lemma]] (the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]]) says that there is an isomorphism $hom(X\otimes Y, Z) \simeq hom(X,hom(Y,Z))$. Moreover, by taking $A = 1$ in the above and using the left [[unitor]] isomorphisms $A \otimes (X \otimes Y) \simeq X \otimes Y$ and $A\otimes X \simeq X$  we get a [[commuting diagram]]

$$
  \array{
    Hom_{\mathcal{C}}(1,hom(X\otimes Y, Z))
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(1,hom(X,hom(Y,Z)))
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\mathcal{C}}(X \otimes Y, Z)
     &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(X, hom(Y,Z))
  }
  \,.
$$

=--



+-- {: .num_example #TopAsASymmetricMonoidalCategory}
###### Example

The category [[Set]] of [[sets]] and [[functions]] between them, regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] according to def. \ref{SymmetricMonoidalCategory} with [[tensor product]] the [[Cartesian product]] $\times$ of sets. The [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident (almost unnoticable but nevertheless nontrivial) canonical identifications.

Similarly the category $Top_{cg}$ of [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#kTop)) becomes a [[symmetric monoidal category]] with [[tensor product]] the corresponding [[Cartesian products]], hence the operation of forming k-ified ([cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) [[product topological spaces]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#ProductTopologicalSpace)). The underlying functions of the [[associator]], [[unitor]] and [[braiding]] isomorphisms are just those of the underlying sets, as above.

Symmetric monoidal categories, such as these, for which the tensor product is the [[Cartesian product]] are called _[[Cartesian monoidal categories]]_.

Both examples are [[closed monoidal categories]] (def. \ref{ClosedMonoidalCategory}), with [[internal hom]] the [[mapping spaces]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#MappingTopologicalSpaceIsExponentialObject)).

=--

+-- {: .num_example #PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}
###### Example

The category $Top_{cg}^{\ast/}$ of [[pointed topological space|pointed]] [[compactly generated topological spaces]] with [[tensor product]] the  [[smash product]] $\wedge$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductOfPointedObjects))

$$
  X \wedge Y \coloneqq \frac{X\times Y}{X\vee Y}
$$

is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) with [[unit object]] the pointed [[0-sphere]] $S^0$.

The components of the [[associator]], the [[unitors]] and the [[braiding]] are those of [[Top]] as in example \ref{TopAsASymmetricMonoidalCategory}, descended to the [[quotient topological spaces]] which appear in the definition of the [[smash product]]. This works for pointed [[compactly generated spaces]] (but not for general pointed topological spaces) by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#SmashProductInTopcgIsAssociative).

The category $Top^{\ast/}_{cg}$ is also a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}), with [[internal hom]] the pointed [[mapping space]] $Maps(-,-)_\ast$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace))

=--


+-- {: .num_example #ExampleAbelianGroupsOfMonoidalCategory}
###### Example

The category [[Ab]] of [[abelian groups]], regarded as enriched in [[discrete topological spaces]], becomes a [[symmetric monoidal category]] with tensor product the actual [[tensor product of abelian groups]] $\otimes_{\mathbb{Z}}$ and with [[tensor unit]] the additive group $\mathbb{Z}$ of [[integers]]. Again the [[associator]], [[unitor]] and [[braiding]] isomorphism are the evident ones coming from the underlying sets, as in example \ref{TopAsASymmetricMonoidalCategory}.

This is a [[closed monoidal category]] with [[internal hom]] $hom(A,B)$ being the set of [[homomorphisms]] $Hom_{Ab}(A,B)$ equipped with the pointwise group structure for $\phi_1, \phi_2 \in Hom_{Ab}(A,B)$ then $(\phi_1 + \phi_2)(a) \coloneqq \phi_1(a) + \phi_2(b) \; \in B$.

This is the archetypical case that motivates the notation "$\otimes$" for the pairing operation in a [[monoidal category]]:

=--

+-- {: .num_example #SymmetricMonoidalCategoryOfChainComplexes}
###### Example

The category [[category of chain complexes]] $Ch_\bullet$, equipped with the [[tensor product of chain complexes]] is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}).

In this case the [[braiding]] has a genuinely non-trivial aspect to it, beyond just the swapping of coordinates as in examples \ref{TopAsASymmetricMonoidalCategory}, \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory} and def. \ref{ExampleAbelianGroupsOfMonoidalCategory}, namely for $X, Y \in Ch_\bullet$ then

$$
  (X \otimes Y)_n
  =
  \underset{n_1 + n_2 = n}{\otimes}
  X_{n_1} \otimes_{\mathbb{Z}} X_{n_2}
$$

and in these components the braiding isomorphism is that of [[Ab]], but with a minus sign thrown in whener two odd-graded components are commuted.

This is a first shadow of the graded-commutativity that also exhibited by spectra.

=--

(e.g. [Hovey 99, prop. 4.2.13](#Hovey99))





### Algebras and modules
 {#AlgebrasAndModules}


+-- {: .num_defn #MonoidsInMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, then a **[[monoid in a monoidal category|monoid internal to]]** $(\mathcal{C}, \otimes, 1)$ is

1. an [[object]] $A \in \mathcal{C}$;

1. a morphism $e \;\colon\; 1 \longrightarrow A$ (called the _[[unit]]_)

1. a morphism $\mu \;\colon\; A \otimes A \longrightarrow A$ (called the _product_);

such that

1. ([[associativity]]) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes A
         &\underoverset{\simeq}{a_{A,A,A}}{\longrightarrow}&
       A \otimes (A \otimes A)
         &\overset{A \otimes \mu}{\longrightarrow}&
       A \otimes A
       \\
       {}^{\mathllap{\mu \otimes A}}\downarrow
         && &&
       \downarrow^{\mathrlap{\mu}}
       \\
       A \otimes A
         &\longrightarrow&
         &\overset{\mu}{\longrightarrow}&
       A
     }
     \,,
   $$

   where $a$ is the associator isomorphism of $\mathcal{C}$;

1. {#UnitalityMonoid} ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes A
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes A
         &\overset{id \otimes e}{\longleftarrow}&
       A \otimes 1
       \\
       & {}_{\mathllap{\ell}}\searrow
       & \downarrow^{\mathrlap{\mu}} &
       & \swarrow_{\mathrlap{r}}
       \\
       && A
     }
     \,,
   $$

   where $\ell$ and $r$ are the left and right unitor isomorphisms of $\mathcal{C}$.

Moreover, if $(\mathcal{C}, \otimes , 1)$ has the structure of a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}) $(\mathcal{C}, \otimes, 1, B)$ with symmetric [[braiding]] $\tau$, then a monoid $(A,\mu, e)$ as above is called a **[[commutative monoid in a symmetric monoidal category|commutative monoid in]]** $(\mathcal{C}, \otimes, 1, B)$ if in addition

* (commutativity) the following [[commuting diagram|diagram commutes]]

  $$
    \array{
      A \otimes A
        && \underoverset{\simeq}{\tau_{A,A}}{\longrightarrow} &&
      A \otimes A
      \\
      & {}_{\mathllap{\mu}}\searrow && \swarrow_{\mathrlap{\mu}}
      \\
      && A
    }
    \,.
  $$

A [[homomorphism]] of monoids $(A_1, \mu_1, e_1)\longrightarrow (A_2, \mu_2, f_2)$ is a morphism

$$
  f \;\colon\; A_1 \longrightarrow A_2
$$

in $\mathcal{C}$, such that the following two [[commuting diagram|diagrams commute]]

$$
  \array{
    A_1 \otimes A_1
      &\overset{f \otimes f}{\longrightarrow}&
    A_2 \otimes A_2
    \\
    {}^{\mathllap{\mu_1}}\downarrow && \downarrow^{\mathrlap{\mu_2}}
    \\
    A_1 &\underset{f}{\longrightarrow}& A_2
  }
$$

and

$$
  \array{
    1_{\mathcal{c}} &\overset{e_1}{\longrightarrow}& A_1
    \\
    & {}_{\mathllap{e_2}}\searrow & \downarrow^{\mathrlap{f}}
    \\
    && A_2
  }
  \,.
$$

Write $Mon(\mathcal{C}, \otimes,1)$ for the **[[category of monoids]]** in $\mathcal{C}$, and $CMon(\mathcal{C}, \otimes, 1)$ for its subcategory of commutative monoids.


=--

+-- {: .num_example #MonoidGivenByTensorUnit}
###### Example

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$, then the [[tensor unit]] $1$ is a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}) with product given by either the left or right [[unitor]]

$$
  \ell_1 = r_1 \;\colon\; 1 \otimes 1 \overset{\simeq}{\longrightarrow} 1
  \,.
$$

By lemma \ref{kel1}, these two morphisms coincide and define an [[associativity|associative]] product with unit the identity $id \colon 1 \to 1$.

If $(\mathcal{C}, \otimes , 1)$ is a [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}), then this monoid is a [[commutative monoid in a symmetric monoidal category|commutative monoid]].

=--

+-- {: .num_example #TensorProductOfTwoCommutativeMonoids}
###### Example

Given a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}), and given two [[commutative monoid in a symmetric monoidal category|commutative monoids]] $(E_i, \mu_i, e_i)$ $i \in \{1,2\}$ (def. \ref{MonoidsInMonoidalCategory}), then the [[tensor product]] $E_1 \otimes E_2$ becomes itself a commutative monoid with unit morphism

$$
  e \;\colon\;
  1
    \overset{\simeq}{\longrightarrow}
  1 \otimes 1
    \overset{e_1 \otimes e_2}{\longrightarrow}
  E_1 \otimes E_2
$$

(where the first isomorphism is, $\ell_1^{-1} = r_1^{-1}$ (lemma \ref{kel1})) and with product morphism given by

$$
  E_1 \otimes E_2
   \otimes
  E_1 \otimes E_2
   \overset{id \otimes \tau_{E_2, E_1} \otimes id}{\longrightarrow}
  E_1 \otimes E_1 \otimes E_2 \otimes E_2
   \overset{\mu_1 \otimes \mu_2}{\longrightarrow}
  E_1 \otimes E_2
$$

(where we are notationally suppressing the [[associators]] and where $\tau$ denotes the [[braiding]] of $\mathcal{C}$).

That this definition indeed satisfies associativity and commutativity follows from the corresponding properties of $(E_i,\mu_i, e_i)$, and from the hexagon identities for the braiding (def. \ref{BraidedMonoidalCategory}) and from symmetry of the braiding.

Similarly one checks that for $E_1 = E_2 = E$ then the unit maps

$$
  E \simeq E \otimes 1
    \overset{id \otimes e}{\longrightarrow}
  E \otimes E
$$

$$
  E \simeq 1 \otimes E
    \overset{e \otimes 1}{\longrightarrow}
  E \otimes E
$$

and the product map

$$
  \mu
    \;\colon\;
  E \otimes E
    \longrightarrow
  E
$$

and the braiding

$$
  \tau_{E,E}
    \;\colon\;
  E \otimes E
    \longrightarrow
  E \otimes E
$$

are monoid homomorphisms, with $E \otimes E$ equipped with the above monoid structure.


=--


+-- {: .num_defn #ModulesInMonoidalCategory}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidalCategory}), and given $(A,\mu,e)$ a [[monoid in a monoidal category|monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), then a **left [[module object]]** in $(\mathcal{C}, \otimes, 1)$ over $(A,\mu,e)$ is

1. an [[object]] $N \in \mathcal{C}$;

1. a [[morphism]] $\rho \;\colon\; A \otimes N \longrightarrow N$ (called the _[[action]]_);

such that

1. ([[unitality]]) the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       1 \otimes N
         &\overset{e \otimes id}{\longrightarrow}&
       A \otimes N
       \\
       & {}_{\mathllap{\ell}}\searrow
       & \downarrow^{\mathrlap{\rho}}
       \\
       && N
     }
     \,,
   $$

   where $\ell$ is the left unitor isomorphism of $\mathcal{C}$.


1. (action property) the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (A\otimes A) \otimes N
         &\underoverset{\simeq}{a_{A,A,N}}{\longrightarrow}&
       A \otimes (A \otimes N)
         &\overset{A \otimes \rho}{\longrightarrow}&
       A \otimes N
       \\
       {}^{\mathllap{\mu \otimes N}}\downarrow
         && &&
       \downarrow^{\mathrlap{\rho}}
       \\
       A \otimes N
         &\longrightarrow&
         &\overset{\rho}{\longrightarrow}&
       N
     }
     \,,
   $$

A [[homomorphism]] of left $A$-module objects

$$
  (N_1, \rho_1) \longrightarrow (N_2, \rho_2)
$$

is a morphism

$$
  f\;\colon\; N_1 \longrightarrow N_2
$$

in $\mathcal{C}$, such that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    A\otimes N_1 &\overset{A \otimes f}{\longrightarrow}& A\otimes N_2
    \\
    {}^{\mathllap{\rho_1}}\downarrow
      &&
    \downarrow^{\mathrlap{\rho_2}}
    \\
    N_1 &\underset{f}{\longrightarrow}& N_2
  }
  \,.
$$

For the resulting **[[category of modules]]** of left $A$-modules in $\mathcal{C}$ with $A$-module homomorphisms between them, we write

$$
  A Mod(\mathcal{C})
  \,.
$$

This is naturally a (pointed) [[topologically enriched category]] itself.

=--

+-- {: .num_example #EveryObjectIsModuleOverTensorUnit}
###### Example

Given a [[monoidal category]] $(\mathcal{C},\otimes, 1)$ (def. \ref{MonoidalCategory}) with the [[tensor unit]] $1$ regarded as a [[monoid in a monoidal category]] via example \ref{MonoidGivenByTensorUnit}, then the left [[unitor]]

$$
  \ell_C
    \;\colon\;
  1\otimes C \longrightarrow C
$$

makes every object $C \in \mathcal{C}$ into a left module, according to def. \ref{ModulesInMonoidalCategory}, over $C$. The action property holds due to lemma \ref{kel1}. This gives an [[equivalence of categories]]

$$
  \mathcal{C} \simeq 1 Mod(\mathcal{C})
$$

of $\mathcal{C}$ with the [[category of modules]] over its tensor unit.


=--

+-- {: .num_example #RingsAreMonoidsInAb}
###### Example

The archetypical case in which all these abstract concepts reduce to the basic familiar ones is the symmetric monoidal category [[Ab]] of [[abelian groups]] from example \ref{ExampleAbelianGroupsOfMonoidalCategory}.

1. A [[monoid in a monoidal category|monoid in]] $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[ring]].

1. A [[commutative monoid in a symmetric monoidal category|commutative monoid in]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{MonoidsInMonoidalCategory}) is equivalently a [[commutative ring]] $R$.

1. An $R$-[[module object]] in $(Ab, \otimes_{\mathbb{Z}}, \mathbb{Z})$ (def. \ref{ModulesInMonoidalCategory}) is equivalently an $R$-[[module]];

1. The tensor product of $R$-module objects (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[tensor product of modules]].

1. The [[category of modules|category of module objects]] $R Mod(Ab)$ (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) is the standard [[category of modules]] $R Mod$.

=--

+-- {: .num_example #dgAlgebraAreMonoidsInChainComplexes}
###### Example

Closely related to the example \ref{RingsAreMonoidsInAb}, but closer to the structure we will see below for spectra, are [[monoid in a monoidal category|monoids]] in the [[category of chain complexes]] $(Ch_\bullet, \otimes, \mathbb{Z})$ from example \ref{SymmetricMonoidalCategoryOfChainComplexes}. These monoids are equivalently [[differential graded algebras]].


=--



+-- {: .num_prop #MonoidModuleOverItself}
###### Proposition

In the situation of def. \ref{ModulesInMonoidalCategory}, the monoid $(A,\mu, e)$ canonically becomes a left module over itself by setting $\rho \coloneqq \mu$. More generally, for $C \in \mathcal{C}$ any object, then $A \otimes C$ naturally becomes a left $A$-module by setting:

$$
  \rho
  \;\colon\;
  A \otimes (A \otimes C)
   \underoverset{\simeq}{a^{-1}_{A,A,C}}{\longrightarrow}
  (A \otimes A) \otimes C
    \overset{\mu \otimes id}{\longrightarrow}
  A \otimes C
  \,.
$$

The $A$-modules of this form are called **[[free modules]]**.

The [[free functor]] $F$ constructing free $A$-modules is [[left adjoint]] to the [[forgetful functor]] $U$ which sends a module $(N,\rho)$ to the underlying object $U(N,\rho) \coloneqq N$.

$$
  A Mod(\mathcal{C})
    \underoverset
     {\underset{U}{\longrightarrow}}
     {\overset{F}{\longleftarrow}}
     {\bot}
  \mathcal{C}
  \,.
$$

=--

+-- {: .proof}
###### Proof

A homomorphism out of a free $A$-module is a morphism in $\mathcal{C}$ of the form

$$
  f \;\colon\; A\otimes C \longrightarrow N
$$

fitting into the diagram (where we are notationally suppressing the [[associator]])

$$
  \array{
    A \otimes A \otimes C
      &\overset{A \otimes f}{\longrightarrow}&
    A \otimes N
    \\
    {}^{\mathllap{\mu \otimes id}}\downarrow
      &&
    \downarrow^{\mathrlap{\rho}}
    \\
    A \otimes C
      &\underset{f}{\longrightarrow}&
    N
  }
  \,.
$$

Consider the composite

$$
  \tilde f
    \;\colon\;
  C
    \underoverset{\simeq}{\ell_C}{\longrightarrow}
  1 \otimes C
    \overset{e\otimes id}{\longrightarrow}
  A \otimes C
    \overset{f}{\longrightarrow}
  N
  \,,
$$

i.e. the restriction of $f$ to the unit "in" $A$. By definition, this fits into a [[commuting square]] of the form (where we are now notationally suppressing the [[associator]] and the [[unitor]])

$$
  \array{
   A \otimes C
     &\overset{id \otimes \tilde f}{\longrightarrow}&
   A \otimes N
   \\
   {}^{\mathllap{id \otimes e \otimes id}}\downarrow
     &&
   \downarrow^{\mathrlap{=}}
   \\
   A \otimes A \otimes C
    &\underset{id \otimes f}{\longrightarrow}&
   A \otimes N
  }
  \,.
$$

Pasting this square onto the top of the previous one yields

$$
  \array{
   A \otimes C
     &\overset{id \otimes \tilde f}{\longrightarrow}&
   A \otimes N
   \\
   {}^{\mathllap{id \otimes e \otimes id}}\downarrow
     &&
   \downarrow^{\mathrlap{=}}
    \\
    A \otimes A \otimes C
      &\overset{A \otimes f}{\longrightarrow}&
    A \otimes N
    \\
    {}^{\mathllap{\mu \otimes id}}\downarrow
      &&
    \downarrow^{\mathrlap{\rho}}
    \\
    A \otimes C
      &\underset{f}{\longrightarrow}&
    N
  }
  \,,
$$

where now the left vertical composite is the identity, by the unit law in $A$. This shows that $f$ is uniquely determined by $\tilde f$ via the relation

$$
  f = \rho \circ (id_A \otimes \tilde f)
  \,.
$$

This natural bijection between $f$ and $\tilde f$ establishes the adjunction.


=--

+-- {: .num_defn #TensorProductOfModulesOverCommutativeMonoidObject}
###### Definition

Given a (pointed) [[topologically enriched category|topological]] [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}, def. \ref{ClosedMonoidalCategory}), given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}), and given $(N_1, \rho_1)$ and $(N_2, \rho_2)$ two left $A$-[[module objects]] (def.\ref{MonoidsInMonoidalCategory}), then

1. the **[[tensor product of modules]]** $N_1 \otimes_A N_2$ is, if it exists, the [[coequalizer]]

   $$
     N_1 \otimes A \otimes N_2
     \underoverset
       {\underset{\rho_{1}\circ (\tau_{N_1,A} \otimes N_2)}{\longrightarrow}}
       {\overset{N_1 \otimes \rho_2}{\longrightarrow}}
       {\phantom{AAAA}}
     N_1 \otimes N_1
       \overset{coeq}{\longrightarrow}
     N_1 \otimes_A N_2
   $$

   and if $A \otimes (-)$ preserves these coequalizers, then this is equipped with the left $A$-action induced from the left $A$-action on $N_1$

1. the **function module** $hom_A(N_1,N_2)$ is, if it exists, the [[equalizer]]

   $$
     hom_A(N_1, N_2)
       \overset{equ}{\longrightarrow}
     hom(N_1, N_2)
       \underoverset
         {\underset{hom(A \otimes N_1, \rho_2)\circ (A \otimes(-))}{\longrightarrow}}
         {\overset{hom(\rho_1,N_2)}{\longrightarrow}}
         {\phantom{AAAAAA}}
       hom(A \otimes N_1, N_2)
     \,.
   $$

   equipped with the left $A$-action that is induced by the left $A$-action on $N_2$ via

   $$
     \frac{
       A \otimes hom(X,N_2) \longrightarrow hom(X,N_2)
     }{
      A \otimes hom(X,N_2) \otimes X
        \overset{id \otimes ev}{\longrightarrow}
      A \otimes N_2 \overset{\rho_2}{\longrightarrow} N_2
     }
     \,.
   $$

=--

(e.g. [Hovey-Shipley-Smith 00, lemma 2.2.2 and lemma 2.2.8](#HoveyShipleySmith00))



+-- {: .num_prop #MonoidalCategoryOfModules}
###### Proposition

Given a (pointed) [[topologically enriched category|topological]] [[closed monoidal category|closed]] [[symmetric monoidal category]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{SymmetricMonoidalCategory}, def. \ref{ClosedMonoidalCategory}), and given $(A,\mu,e)$ a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] $(\mathcal{C}, \otimes, 1)$ (def. \ref{MonoidsInMonoidalCategory}). If all [[coequalizers]] exist in $\mathcal{C}$, then the [[tensor product of modules]] $\otimes_A$ from def. \ref{TensorProductOfModulesOverCommutativeMonoidObject} makes the [[category of modules]] $A Mod(\mathcal{C})$ into a [[symmetric monoidal category]], $(A Mod, \otimes_A, A)$ with [[tensor unit]] the object $A$ itself, regarded as an $A$-module via prop. \ref{MonoidModuleOverItself}.

If moreover all [[equalizers]] exist, then this is a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) with [[internal hom]] given by the function modules $hom_A$ of def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}.

=--

(e.g. [Hovey-Shipley-Smith 00, lemma 2.2.2, lemma 2.2.8](#HoveyShipleySmith00))

+-- {: .proof}
###### Proof sketch

The associators and braiding for $\otimes_{A}$ are induced directly from those of $\otimes$ and the [[universal property]] of [[coequalizers]]. That $A$ is the tensor unit for $\otimes_{A}$ follows with the same kind of argument that we give in the proof of example \ref{FreeModulesTensorProduct} below.

=--

+-- {: .num_example #FreeModulesTensorProduct}
###### Example

For $(A,\mu,e)$ a [[monoid in a monoidal category|monoid]] (def. \ref{MonoidsInMonoidalCategory}) in a [[symmetric monoidal category]] $(\mathcal{C},\otimes, 1)$ (def. \ref{MonoidalCategory}), the [[tensor product of modules]] (def. \ref{TensorProductOfModulesOverCommutativeMonoidObject}) of two [[free modules]] (def. \ref{MonoidModuleOverItself}) $A\otimes C_1$ and $A \otimes C_2$ always exists and is the free module over the tensor product in $\mathcal{C}$ of the two generators:

$$
  (A \otimes C_1) \otimes_A (A \otimes C_2)
  \simeq
  A \otimes (C_1 \otimes C_2)
  \,.
$$

Hence if $\mathcal{C}$ has all [[coequalizers]], so that the [[category of modules]] is a [[monoidal category]] $(A Mod, \otimes_A, A)$ (prop. \ref{MonoidalCategoryOfModules}) then the free module functor (def. \ref{MonoidModuleOverItself}) is a [[strong monoidal functor]] (def. \ref{LaxMonoidalFunctor})

$$
  F
    \;\colon\;
  (\mathcal{C}, \otimes, 1)
    \longrightarrow
  (A Mod, \otimes_A, A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is sufficient to show that the diagram

$$
  A \otimes A \otimes A
   \underoverset
    {\underset{id \otimes \mu}{\longrightarrow}}
    {\overset{\mu \otimes id}{\longrightarrow}}
    {\phantom{AAAA}}
  A \otimes A
    \overset{\mu}{\longrightarrow}
  A
$$

is a [[coequalizer]] diagram (we are notationally suppressing the [[associators]]), hence that $A \otimes_A A \simeq A$, hence that the claim holds for $C_1 = 1$ and $C_2 = 1$.

To that end, we check the [[universal property]] of the [[coequalizer]]:

First observe that $\mu$ indeed coequalizes $id \otimes \mu$ with $\mu \otimes id$, since this is just the [[associativity]] clause in def. \ref{MonoidsInMonoidalCategory}. So for $f \colon A \otimes A \longrightarrow Q$ any other morphism with this property, we need to show that there is a unique morphism $\phi \colon A \longrightarrow Q$ which makes this [[commuting diagram|diagram commute]]:

$$
  \array{
    A \otimes A &\overset{\mu}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow & \swarrow_{\mathrlap{\phi}}
    \\
    Q
  }
  \,.
$$

We claim that

$$
  \phi
    \;\colon\;
  A
    \underoverset{\simeq}{r^{-1}}{\longrightarrow}
  A \otimes 1
    \overset{id \otimes e}{\longrightarrow}
  A \otimes A
    \overset{f}{\longrightarrow}
  Q
  \,,
$$

where the first morphism is the inverse of the right [[unitor]] of $\mathcal{C}$.

First to see that this does make the required triangle commute, consider the following pasting composite of [[commuting diagrams]]

$$
  \array{
    A \otimes A &\overset{\mu}{\longrightarrow}& A
    \\
    {}^{\mathllap{id \otimes r^{-1}}}_{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{r^{-1}}}_{\simeq}
    \\
    A \otimes A \otimes 1
      &\overset{\mu \otimes id}{\longrightarrow}&
    A \otimes 1
    \\
    {}^{\mathllap{id \otimes e}}\downarrow
      &&
    \downarrow^{\mathrlap{id \otimes e} }
    \\
    A \otimes A \otimes A
      &\overset{\mu \otimes id}{\longrightarrow}&
    A \otimes A
    \\
    {}^{\mathllap{id \otimes \mu}}\downarrow
      &&
    \downarrow^{\mathrlap{f}}
    \\
    A \otimes A
      &\underset{f}{\longrightarrow}&
    Q
  }
  \,.
$$

Here the the top square is the [[natural transformation|naturality]] of the right [[unitor]], the middle square commutes by the functoriality of the tensor product $\otimes \;\colon\; \mathcal{C}\times \mathcal{C} \longrightarrow \mathcal{C}$ and the definition of the [[product category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), while the commutativity of the bottom square is the assumption that $f$ coequalizes $id \otimes \mu$ with $\mu \otimes id$.

Here the right vertical composite is $\phi$,  while, by [unitality](#UnitalityMonoid) of $(A,\mu ,e)$, the left vertical composite is the identity on $A$, Hence the diagram says that $\phi \circ \mu = f$, which we needed to show.

It remains to see that $\phi$ is the unique morphism with this property for given $f$. For that let $q \colon A \to Q$ be any other morphism with $ q\circ \mu = f$. Then consider the [[commuting diagram]]

$$
  \array{
    A \otimes 1 &\overset{\simeq}{\longleftarrow}& A
    \\
    {}^{\mathllap{id\otimes e}}\downarrow & \searrow^{\simeq}
    & \downarrow^{\mathrlap{=}}
    \\
    A \otimes A &\overset{\mu}{\longrightarrow}& A
    \\
    {}^{\mathllap{f}}\downarrow & \swarrow_{\mathrlap{q}}
    \\
    Q
  }
  \,,
$$

where the top left triangle is the [unitality](#UnitalityMonoid) condition and the two isomorphisms are the right [[unitor]] and its inverse. The commutativity of this diagram says that $q = \phi$.


=--



+-- {: .num_defn #AAlgebra}
###### Definition

Given a [[monoidal category|monoidal]] [[category of modules]] $(A Mod , \otimes_A , A)$ as in prop. \ref{MonoidalCategoryOfModules}, then a [[monoid in a monoidal category|monoid]] $(E, \mu, e)$ in  $(A Mod , \otimes_A , A)$ (def. \ref{MonoidsInMonoidalCategory}) is called an **$A$-[[associative algebra|algebra]]**.

=--

+-- {: .num_prop #AlgebrasOverAAreMonoidsUnderA}
###### Proposition

Given a [[monoidal category|monoidal]] [[category of modules]] $(A Mod , \otimes_A , A)$ in a [[monoidal category]] $(\mathcal{C},\otimes, 1)$ as in prop. \ref{MonoidalCategoryOfModules}, and an $A$-algebra $(E,\mu,e)$ (def. \ref{AAlgebra}), then there is an [[equivalence of categories]]

$$
  A Alg_{comm}(\mathcal{C})
    \coloneqq
  CMon(A Mod)
   \simeq
  CMon(\mathcal{C})^{A/}
$$

between the [[category of commutative monoids]] in $A Mod$ and the [[coslice category]] of commutative monoids in $\mathcal{C}$ under $A$, hence between commutative $A$-algebras in $\mathcal{C}$ and commutative monoids $E$ in $\mathcal{C}$ that are equipped with a homomorphism of monoids $A \longrightarrow E$.

=--

(e.g. [EKMM 97, VII lemma 1.3](#EKMM97))

+-- {: .proof}
###### Proof

In one direction, consider a $A$-algebra $E$ with unit $e_E \;\colon\; A \longrightarrow E$ and product $\mu_{E/A} \colon E \otimes_A E \longrightarrow E$. There is the underlying product $\mu_E$

$$
  \array{
    E \otimes A \otimes E
    &
    \underoverset
      {\underset{}{\longrightarrow}}
      {\overset{}{\longrightarrow}}
      {\phantom{AAA}}
    &
    E \otimes E
     &\overset{coeq}{\longrightarrow}&
    E \otimes_A E
    \\
    && & {}_{\mathllap{\mu_E}}\searrow & \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    && && E
  }
  \,.
$$

By considering a diagram of such coequalizer diagrams with middle vertical morphism $e_E\circ e_A$, one find that this is a unit for $\mu_E$ and that $(E, \mu_E, e_E \circ e_A)$ is a commutative monoid in $(\mathcal{C}, \otimes, 1)$.

Then consider the two conditions on the unit $e_E \colon A \longrightarrow E$. First of all this is an $A$-module homomorphism, which means that

$$
  (\star)
  \;\;\;\;\;
  \;\;\;\;\;
  \array{
    A \otimes A &\overset{id \otimes e_E}{\longrightarrow}& A \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow && \downarrow^{\mathrlap{\rho}}
    \\
    A &\underset{e_E}{\longrightarrow}& E
  }
$$

[[commuting diagram|commutes]]. Moreover it satisfies the unit property

$$
  \array{
    A \otimes_A E
      &\overset{e_A \otimes id}{\longrightarrow}&
    E \otimes_A E
    \\
    & {}_{\mathllap{\simeq}}\searrow & \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    && E
  }
  \,.
$$

By forgetting the tensor product over $A$, the latter gives

$$
  \array{
    A \otimes E
      &\overset{e \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    \downarrow && \downarrow^{\mathrlap{}}
    \\
    A \otimes_A E
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes_A E
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_{E/A}}}
    \\
    E &=& E
  }
  \;\;\;\;\;\;\;\;
   \simeq
  \;\;\;\;\;\;\;\;
  \array{
    A \otimes E
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\rho}}\downarrow && \downarrow^{\mathrlap{\mu_{E}}}
    \\
    E &\underset{id}{\longrightarrow}& E
  }
  \,,
$$

where the top vertical morphisms on the left the canonical coequalizers, which identifies the vertical composites on the right as shown. Hence this may be [[pasting|pasted]] to the square $(\star)$ above, to yield a [[commuting square]]

$$
  \array{
    A \otimes A
     &\overset{id\otimes e_E}{\longrightarrow}&
    A \otimes E
      &\overset{e_E \otimes id}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow
      &&
    {}^{\mathllap{\rho}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_{E}}}
    \\
    A &\underset{e_E}{\longrightarrow}& E &\underset{id}{\longrightarrow}& E
  }
  \;\;\;\;\;\;\;\;\;\;
   =
  \;\;\;\;\;\;\;\;\;\;
  \array{
    A \otimes A
     &\overset{e_E \otimes e_E}{\longrightarrow}&
    E \otimes E
    \\
    {}^{\mathllap{\mu_A}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_E}}
    \\
    A &\underset{e_E}{\longrightarrow}& E
  }
  \,.
$$

This shows that the unit $e_A$ is a homomorphism of monoids $(A,\mu_A, e_A) \longrightarrow (E, \mu_E, e_E\circ e_A)$.

Now for the converse direction, assume that $(A,\mu_A, e_A)$ and $(E, \mu_E, e'_E)$ are two commutative monoids in $(\mathcal{C}, \otimes, 1)$ with $e_E \;\colon\; A  \to E$ a monoid homomorphism. Then $E$ inherits a left $A$-[[module]] structure by

$$
  \rho
    \;\colon\;
  A \otimes E
    \overset{e_A \otimes id}{\longrightarrow}
  E \otimes E
    \overset{\mu_E}{\longrightarrow}
  E
  \,.
$$

By commutativity and associativity it follows that $\mu_E$ coequalizes the two induced morphisms $E \otimes A \otimes E \underoverset{\longrightarrow}{\longrightarrow}{\phantom{AA}} E \otimes E$. Hence the [[universal property]] of the [[coequalizer]] gives a factorization through some $\mu_{E/A}\colon E \otimes_A E \longrightarrow E$. This shows that $(E, \mu_{E/A}, e_E)$ is a commutative $A$-algebra.

Finally one checks that these two constructions are inverses to each other, up to isomorphism.

=--






### Topological ends and coends
 {#TopologicalEndsAndCoends}

For working with pointed [[topologically enriched functors]], a certain shape of [[limits]]/[[colimits]] is particularly relevant: these are called (pointed topological enriched) _[[ends]]_ and _[[coends]]_. We here introduce these and then derive some of their basic properties, such as notably the expression for topological [[left Kan extension]] in terms of [[coends]] (prop. \ref{TopologicalLeftKanExtensionBCoend} below). Further below it is via left Kan extension along the ordinary smash product of pointed topological spaces ("[[Day convolution]]") that the [[symmetric monoidal smash product of spectra]] is induced.

+-- {: .num_defn #OppositeAndProductOfPointedTopologicallyEnrichedCategory}
###### Definition

Let $\mathcal{C}, \mathcal{D}$ be pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)), i.e. [[enriched categories]] over $(Top_{cg}^{\ast/}, \wedge, S^0)$ from example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}.

1. The **pointed topologically enriched [[opposite category]]** $\mathcal{C}^{op}$ is the [[topologically enriched category]] with the same [[objects]] as $\mathcal{C}$, with [[hom-spaces]]

   $$
     \mathcal{C}^{op}(X,Y)
     \coloneqq
     \mathcal{C}(Y,X)
   $$

   and with [[composition]] given by [[braiding]] followed by the composition in $\mathcal{C}$:

   $$
     \mathcal{C}^{op}(X,Y)
     \wedge
     \mathcal{C}^{op}(Y,Z)
     =
     \mathcal{C}(Y,X)\wedge \mathcal{C}(Z,Y)
     \underoverset{\simeq}{\tau}{\longrightarrow}
     \mathcal{C}(Z,Y) \wedge \mathcal{C}(Y,X)
       \overset{\circ_{Z,Y,X}}{\longrightarrow}
     \mathcal{C}(Z,X)
     =
     \mathcal{C}^{op}(X,Z)
     \,.
   $$

1. the **pointed topological [[product category]]** $\mathcal{C} \times \mathcal{D}$ is the [[topologically enriched category]] whose [[objects]] are [[pairs]] of objects $(c,d)$ with $c \in \mathcal{C}$ and $d\in \mathcal{D}$, whose [[hom-spaces]] are the [[smash product]] of the separate hom-spaces

   $$
     (\mathcal{C}\times \mathcal{D})((c_1,d_1),\;(c_2,d_2) )
       \coloneqq
     \mathcal{C}(c_1,c_2)\wedge \mathcal{D}(d_1,d_2)
   $$

   and whose [[composition]] operation is the [[braiding]] followed by the [[smash product]] of the separate composition operations:

   $$
     \array{
       (\mathcal{C}\times \mathcal{D})((c_1,d_1), \; (c_2,d_2))
         \wedge
       (\mathcal{C}\times \mathcal{D})((c_2,d_2), \; (c_3,d_3))
       \\
       {}^{\mathllap{=}}\downarrow
       \\
       \left(\mathcal{C}(c_1,c_2) \wedge \mathcal{D}(d_1,d_2)\right)
         \wedge
       \left(\mathcal{C}(c_2,c_3) \wedge \mathcal{D}(d_2,d_3)\right)
       \\
       \downarrow^{\mathrlap{\tau}}_{\mathrlap{\simeq}}
       \\
       \left(\mathcal{C}(c_1,c_2)\wedge \mathcal{C}(c_2,c_3)\right)
         \wedge
       \left( \mathcal{D}(d_1,d_2)\wedge \mathcal{D}(d_2,d_3)\right)
         &\overset{
             (\circ_{c_1,c_2,c_3})\wedge (\circ_{d_1,d_2,d_3})
           }{\longrightarrow}
         &
       \mathcal{C}(c_1,c_3)\wedge \mathcal{D}(d_1,d_3)
       \\
       && \downarrow^{\mathrlap{=}}
       \\
       && (\mathcal{C}\times \mathcal{D})((c_1,d_1),\; (c_3,d_3))
     }
    \,.
   $$

=--

+-- {: .num_example #PointedTopologicalFunctorOnProductCategory}
###### Example

A pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) into $Top^{\ast/}_{cg}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) out of a pointed topological [[product category]] as in def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}

$$
  F
    \;\colon\;
  \mathcal{C} \times \mathcal{D}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

(a "pointed topological [[bifunctor]]") has component maps of the form

$$
  F_{(c_1,d_1),(c_2,d_2)}
    \;\colon\;
  \mathcal{C}(c_1,c_2)
  \wedge
  \mathcal{D}(d_1,d_2)
    \longrightarrow
  Maps(F_0((c_1,d_1)),F_0((c_2,d_2)))_\ast
  \,.
$$

By functoriality and under passing to [[adjuncts]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)) this is equivalent to two commuting _[[actions]]_


$$
  \rho_{c_1,c_2}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \wedge F_0((c_1,d))
    \longrightarrow
  F_0((c_2,d))
$$

and

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{D}(d_1,d_2) \wedge F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$

In the special case of a functor out of the [[product category]] of some $\mathcal{C}$ with its [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory})

$$
  F
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

then this takes the form of a "pullback action" in the first variable

$$
  \rho_{c_2,c_1}(d)
   \;\colon\;
  \mathcal{C}(c_1,c_2) \wedge F_0((c_2,d))
    \longrightarrow
  F_0((c_1,d))
$$

and a "pushforward action" in the second variable

$$
  \rho_{d_1,d_2}(c)
    \;\colon\;
  \mathcal{C}(d_1,d_2) \wedge F_0((c,d_1))
    \longrightarrow
  F_0((c,d_2))
  \,.
$$


=--


+-- {: .num_defn #EndAndCoendInTopcgSmash}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)), i.e. an [[enriched category]] over $(Top_{cg}^{\ast/}, \wedge, S^0)$ from example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}. Let

$$
  F
    \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$$

be a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) out of the pointed topological [[product category]] of $\mathcal{C}$ with its [[opposite category]], according to def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}.


1. The  **[[coend]]** of $F$, denoted $\overset{c \in \mathcal{C}}{\int} F(c,c)$, is the [[coequalizer]] in $Top_{cg}^{\ast}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#CoequalizerInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c,d \in \mathcal{C}}{\coprod} \mathcal{C}(c,d) \wedge F(d,c)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \rho_{(d,c)}(c) }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \rho_{(c,d)}(d) }{\longrightarrow}}
        {\phantom{AAAAAAAA}}
     \underset{c \in \mathcal{C}}{\coprod} F(c,c)
      \overset{coeq}{\longrightarrow}
     \overset{c\in \mathcal{C}}{\int} F(c,c)
     \,.
   $$

1. The **[[end]]** of $F$, denoted $\underset{c\in \mathcal{C}}{\int} F(c,c)$, is the **[[equalizer]]** in $Top_{cg}^{\ast/}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#EqualizerInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [cor.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)) of the [[adjuncts]] of the two actions encoded in $F$ via example \ref{PointedTopologicalFunctorOnProductCategory}:

   $$
     \underset{c\in \mathcal{C}}{\int} F(c,c)
       \overset{\;\;equ\;\;}{\longrightarrow}
     \underset{c \in \mathcal{C}}{\prod} F(c,c)
      \underoverset
        {\underset{\underset{c,d}{\sqcup} \tilde \rho_{(c,d)}(c)  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} \tilde\rho_{d,c}(d)}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
      \underset{c\in \mathcal{C}}{\prod}
      Maps\left( \mathcal{C}\left(c,d\right), \;  F\left(c,d\right) \right)_\ast
     \,.
   $$

=--

+-- {: .num_example #CoendGivesQuotientByDiagonalGroupAction}
###### Example

Let $G$ be a [[topological group]]. Write $\mathbf{B}(G_+)$ for the pointed [[topologically enriched category]] that has a single object $\ast$, whose single [[hom-space]] is $G_+$ ($G$ with a basepoint freely adjoined ([def.](Introduction+to+Stable+homotopy+theory+--+P#BasePointAdjoined)))

$$
  \mathbf{B}(G_+)(\ast,\ast) \coloneqq G_+
$$

and whose composition operation is the product operation $(-)\cdot(-)$ in $G$ under adjoining basepoints ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#WedgeAndSmashOfBasePointAdjoinedTopologicalSpaces))

$$
  G_+ \wedge G_+
   \simeq
  (G \times G)_+
    \overset{((-)\cdot (-))_+}{\longrightarrow}
   G_+
  \,.
$$

Then a [[topologically enriched functor]]

$$
  (X,\rho_l) \;\colon\; \mathbf{B}(G_+) \longrightarrow Top^{\ast/}_{cg}
$$

is a pointed topological space $X \coloneqq F(\ast)$ equipped with a continuous function

$$
  \rho_l \;\colon\; G_+ \wedge X \longrightarrow X
$$

satisfying the [[action]] property. Hence this is equivalently a continuous and basepoint-preserving left [[action]] (non-linear [[representation]]) of $G$ on $X$.

The [[opposite category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) $(\mathbf{B}(G_+))^{op}$ comes from the [[opposite group]]

$$
  (\mathbf{B}(G_+))^{op}
  =
  \mathbf{B}(G^{op}_+)
  \,.
$$

(The canonical continuous isomorphism $G \simeq G^{op}$ induces a canonical euqivalence of topologically enriched categories $(\mathbf{B}(G_+))^{op} \simeq \mathbf{B}(G_+)$.)

So a topologically enriched functor

$$
  (Y,\rho_r) \;\colon\; (\mathbf{B}(G_+))^{op} \longrightarrow Top^{\ast}_{cg}
$$

is equivalently a basepoint preserving continuous _right_ action of $G$.

Therefore the [[coend]] of two such functors (def. \ref{EndAndCoendInTopcgSmash}) coequalizes the relation

$$
  (x g,\;y)
   \sim
  (x,\; g y)
$$

(where juxtaposition denotes left/right action) and hence is equivalently the canonical smash product of a right $G$-action with a left $G$-action, hence the [[quotient topological space|quotient]] of the plain smash product by the [[diagonal action]] of the group $G$:

$$
  \overset{\ast \in \mathbf{B}(G_+)}{\int}
   (Y,\rho_r)(\ast) \,\wedge\, (X,\rho_l)(\ast)
  \;\simeq\;
  Y \wedge_G X
  \,.
$$


=--

+-- {: .num_example #NaturalTransformationsViaEnds}
###### Example

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For
$
  F,G
  \;\colon\;
  \mathcal{C}
    \longrightarrow
  Top^{\ast/}_{cg}
$
two pointed [[topologically enriched functors]], then the [[end]] (def. \ref{EndAndCoendInTopcgSmash}) of $Maps(F(-),G(-))_\ast$ is a topological space whose underlying [[pointed set]] is the pointed set of [[natural transformations]] $F\to G$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)):

$$
  U
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \;\simeq\;
  Hom_{[\mathcal{C},Top^{\ast/}_{cg}]}(F,G)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The underlying pointed set functor $U\colon Top^{\ast/}_{cg}\to Set^{\ast/}$ [[preserved limit|preserves]] all [[limits]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [prop.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)). Therefore there is an [[equalizer]] diagram in $Set^{\ast/}$ of the form

$$
  U
  \left(
    \underset{c\in \mathcal{C}}{\int}
    Maps(F(c),G(c))_\ast
  \right)
    \overset{equ}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod} Hom_{Top^{\ast/}_{cg}}(F(c),G(c))
      \underoverset
        {\underset{\underset{c,d}{\sqcup} U(\tilde \rho_{(c,d)}(c))  }{\longrightarrow}}
        {\overset{\underset{c,d}{\sqcup} U(\tilde\rho_{d,c}(d))}{\longrightarrow}}
        {\phantom{AAAAAAAA}}
   \underset{c,d\in \mathcal{C}}{\prod}
    Hom_{Top^{\ast/}_{cg}}(
      \mathcal{C}(c,d),
      Maps(F(c),G(d))_\ast
    )
  \,.
$$

Here the object in the middle is just the set of collections of component morphisms $\left\{ F(c)\overset{\eta_c}{\to} G(c)\right\}_{c\in \mathcal{C}}$. The two parallel maps in the equalizer diagram take such a collection to the functions which send any $c \overset{f}{\to} d$ to the result of precomposing

$$
  \array{
    F(c)
    \\
    {}^{\mathllap{f(f)}}\downarrow
    \\
    F(d) &\underset{\eta_d}{\longrightarrow}& G(d)
  }
$$

and of postcomposing

$$
  \array{
    F(c) &\overset{\eta_c}{\longrightarrow}& G(c)
    \\
    && \downarrow^{\mathrlap{G(f)}}
    \\
    && G(d)
  }
$$

each component in such a collection, respectively. These two functions being equal, hence the collection $\{\eta_c\}_{c\in \mathcal{C}}$ being in the equalizer, means precisley that for all $c,d$ and all $f\colon c \to d$ the square

$$
  \array{
    F(c) &\overset{\eta_c}{\longrightarrow}& G(c)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{G(f)}}
    \\
    F(d) &\underset{\eta_d}{\longrightarrow}& G(g)
  }
$$

is a [[commuting square]]. This is precisley the condition that the collection $\{\eta_c\}_{c\in \mathcal{C}}$ be a [[natural transformation]].

=--

Conversely, example \ref{NaturalTransformationsViaEnds} says that [[ends]] over [[bifunctors]] of the form $Maps(F(-),G(-)))_\ast$ constitute [[hom-spaces]] between pointed [[topologically enriched functors]]:


+-- {: .num_defn #PointedTopologicalFunctorCategory}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). Define the structure of a pointed [[topologically enriched category]] on the category $[\mathcal{C}, Top_{cg}^{\ast/}]$ of pointed [[topologically enriched functors]] to $Top^{\ast/}_{cg}$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) by taking the [[hom-spaces]] to be given by the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) of example \ref{NaturalTransformationsViaEnds}:

$$
  [\mathcal{C},Top^{\ast/}_{cg}](F,G)
    \;\coloneqq\;
  \int_{c\in \mathcal{C}} Maps(F(c),G(c))_\ast
$$

The [[composition]] operation on these is defined to be the one induced by the composite maps

$$
  \left(
    \underset{c\in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \wedge
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(G(c),H(c))_\ast
  \right)
    \overset{}{\longrightarrow}
  \underset{c\in \mathcal{C}}{\prod}
    Maps(F(c),G(c))_\ast \wedge Maps(G(c),H(c))_\ast
  \overset{(\circ_{F(c),G(c),H(c)})_{c\in \mathcal{C}}}{\longrightarrow}
  \underset{c \in \mathcal{C}}{\prod}
    Maps(F(c),H(c))_\ast
  \,,
$$

where the first, morphism is degreewise given by projection out of the limits that defined the ends. This composite evidently equalizes the two relevant adjunct actions (as in the proof of example \ref{NaturalTransformationsViaEnds}) and hence defines a map into the end

$$
    \left(
    \underset{c\in \mathcal{C}}{\int} Maps(F(c),G(c))_\ast
  \right)
  \wedge
  \left(
    \underset{c \in \mathcal{C}}{\int} Maps(G(c),H(c))_\ast
  \right)
  \longrightarrow
  \underset{c\in \mathcal{C}}{\int} Maps(F(c),H(c))_\ast
  \,.
$$


The resulting pointed [[topologically enriched category]] $[\mathcal{C},Top^{\ast/}_{cg}]$ is also called the **$Top^{\ast/}_{cg}$-[[enriched functor category]]** over $\mathcal{C}$ with coefficients in $Top^{\ast/}_{cg}$.

=--

This yields an equivalent formulation in terms of ends of the pointed topologically [[enriched Yoneda lemma]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedYonedaLemma)):

+-- {: .num_prop #YonedaReductionTopological}
###### Proposition
**(topologically [[enriched Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

$$
  [\mathcal{C}, Top^{\ast/}_{cg}](\mathcal{C}(c,-),\; F)
  \;\simeq\;
  F(c)
$$

between the [[hom-space]] of the pointed topological functor category, according to def. \ref{PointedTopologicalFunctorCategory}, from the [[representable functor|functor represented]] by $c$ to $F$, and the value of $F$ on $c$.

In terms of the [[ends]] (def. \ref{EndAndCoendInTopcgSmash}) defining these [[hom-spaces]], this means that

$$
  \underset{d\in \mathcal{C}}{\int} Maps(\mathcal{C}(c,d), F(d))_\ast
    \;\simeq\;
  F(c)
  \,.
$$

In this form the statement is also known as **[[Yoneda reduction]]**.

=--

The **proof** of prop. \ref{YonedaReductionTopological} is [[formal dual|formally dual]] to the proof of the next prop. \ref{TopologicalCoYonedaLemma}.

Now that [[natural transformations]] are expressed in terms of [[ends]] (example \ref{NaturalTransformationsViaEnds}), as is the Yoneda lemma (prop. \ref{YonedaReductionTopological}), it is natural to consider the [[formal duality|dual]] statement involving [[coends]]:

+-- {: .num_prop #TopologicalCoYonedaLemma}
###### Proposition
**([[co-Yoneda lemma]])**

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)). For $F \colon \mathcal{C}\to Top^{\ast/}_{cg}$ a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) and for $c\in \mathcal{C}$ an object, there is a [[natural isomorphism]]

$$
  F(-)
    \simeq
  \overset{c \in \mathcal{C}}{\int}
  \mathcal{C}(c,-) \wedge F(c)
  \,.
$$

Moreover, the morphism that hence exhibits $F(c)$ as the [[coequalizer]] of the two morphisms in def. \ref{EndAndCoendInTopcgSmash} is componentwise the canonical action

$$
  \mathcal{C}(c,d) \wedge F(c)
   \longrightarrow
  F(d)
$$

which is [[adjunct]] to the component map $\mathcal{C}(d,c) \to Maps(F(c),F(d))_{\ast}$ of the [[topologically enriched functor]] $F$.

=--

(e.g. [MMSS 00, lemma 1.6](#MMSS00))

+-- {: .proof}
###### Proof

The coequalizer of pointed topological spaces that we need to consider has underlying it a coequalizer of underlying pointed sets  ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop), [prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects), [prop.](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)). That in turn is the colimit over the diagram of underlying sets with the basepointe adjoined to the diagram ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LimitsAndColimitsOfPointedObjects)). For a coequalizer diagram adding that extra point to the diagram clearly does not change the colimit, and so we need to consider the plain coequalizer of sets.

That is just the set of [[equivalence classes]] of [[pairs]]

$$
  ( c \overset{}{\to} c_0,\; x  )
  \;\;
   \in
   \mathcal{C}(c,c_0) \wedge F(c)
  \,,
$$

where two such pairs

$$
  ( c \overset{f}{\to} c_0,\; x \in F(c) )
  \,,\;\;\;\;
  ( d \overset{g}{\to} c_0,\; y \in F(d) )
$$

are regarded as equivalent if there exists

$$
  c \overset{\phi}{\to} d
$$

such that

$$
  f = g \circ \phi
  \,,
  \;\;\;\;\;and\;\;\;\;\;
  y = \phi(x)
  \,.
$$

(Because then the two pairs are the two images of the pair $(g,x)$ under the two morphisms being coequalized.)

But now considering the case that $d = c_0$ and $g = id_{c_0}$, so that $f = \phi$ shows that any pair

$$
  ( c \overset{\phi}{\to} c_0, \; x \in F(c))
$$

is identified, in the coequalizer, with the pair

$$
  (id_{c_0},\; \phi(x) \in F(c_0))
  \,,
$$

hence with $\phi(x)\in F(c_0)$.

This shows the claim at the level of the underlying sets. To conclude it is now sufficient ([prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop)) to show that the topology on $F(c_0) \in Top^{\ast/}_{cg}$ is the [[final topology]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#InitialAndFinalTopologies)) of the system of component morphisms

$$
  \mathcal{C}(d,c) \wedge F(c)
    \longrightarrow
  \overset{c}{\int} \mathcal{C}(c,c_0) \wedge F(c)
$$

which we just found. But that system includes

$$
  \mathcal{C}(c,c) \wedge F(c) \longrightarrow F(c)
$$

which is a [[retraction]]

$$
  id \;\colon\; F(c) \longrightarrow \mathcal{C}(c,c) \wedge F(c)
  \longrightarrow F(c)
$$

and so if all the preimages of a given subset of the coequalizer under these component maps is open, it must have already been open in $F(c)$.


=--


+-- {: .num_remark}
###### Remark

The statement of the [[co-Yoneda lemma]] in prop. \ref{TopologicalCoYonedaLemma} is a kind of [[categorification]] of the following statement in [[analysis]] (whence the notation with the integral signs):

For $X$ a [[topological space]], $f \colon X \to\mathbb{R}$ a [[continuous function]] and $\delta(-,x_0)$ denoting the [[Dirac distribution]], then

$$
  \int_{x \in X} \delta(x,x_0) f(x)
  =
  f(x_0)
  \,.
$$

=--

It is this analogy that gives the name to the following statement:

+-- {: .num_prop #CoendsCommuteWithEachOther}
###### Proposition
**([[Fubini theorem]] for (co)-ends)**

For $F$ a pointed topologically enriched [[bifunctor]] on a small pointed topological [[product category]] $\mathcal{C}_1 \times \mathcal{C}_2$ (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}), i.e.

$$
   F
  \;\colon\;
  \left(
    \mathcal{C}_1\times\mathcal{C}_2
  \right)^{op}
  \times
  (\mathcal{C}_1 \times\mathcal{C}_2)
  \longrightarrow
  Top^{\ast/}_{cg}
$$

then its [[end]] and [[coend]] (def. \ref{EndAndCoendInTopcgSmash}) is equivalently formed consecutively over each variable, in either order:

$$
  \overset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_1}{\int}
  \overset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \overset{c_2}{\int}
  \overset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
$$

and

$$
  \underset{(c_1,c_2)}{\int} F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_1}{\int}
  \underset{c_2}{\int}
  F((c_1,c_2), (c_1,c_2))
  \simeq
  \underset{c_2}{\int}
  \underset{c_1}{\int}
  F((c_1,c_2), (c_1,c_2))
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because [[limits]] commute with limits, and [[colimits]] commute with colimits.

=--



+-- {: .num_remark #MappingSpacePreservesEnds}
###### Remark

Since the pointed compactly generated [[mapping space]] functor ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace))

$$
  Maps(-,-)_\ast
  \;\colon\;
  \left(Top^{\ast/}_{cg}\right)^{op}
  \times
  Top^{\ast/}_{cg}
  \longrightarrow
  Top^{\ast/}_{cg}
$$

takes [[colimits]] in the first argument and [[limits]] in the second argument to limits ([cor.](Introduction+to+Stable+homotopy+theory+--+P#MappingSpacesSendsColimitsInFirstArgumentToLimits)), it in particular takes [[coends]] in the first argument and [[ends]] in the second argument, to ends (def. \ref{EndAndCoendInTopcgSmash}):

$$
  Maps( X, \; \int_{c} F(c,c))_\ast
  \simeq
  \int_c Maps(X, F(c,c)_\ast)
$$

and

$$
  Maps( \int^{c} F(c,c),\; Y  )_\ast
  \simeq
  \underset{c}{\int} Maps( F(c,c),\; Y )_\ast
  \,.
$$

=--

With this [[coend]] calculus in hand, there is an elegant proof of the defining [[universal property]] of the smash [[tensoring]]  of [[topologically enriched functors]] $[\mathcal{C},Top^{\ast}_{cg}]$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TensoringAndPoweringOfTopologicallyEnrichedCopresheaves))


+-- {: .num_prop #UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg}
###### Proposition

For $\mathcal{C}$ a pointed [[topologically enriched category]], there are [[natural isomorphisms]]

$$
  [\mathcal{C},Top^{\ast/}_{cg}]( X \wedge K ,\, Y )
    \;\simeq\;
  Maps(K,\; [\mathcal{C},Top^{\ast/}_{cg}](X,Y))_\ast
$$

and

$$
  [\mathcal{C},Top^{\ast/}_{cg}](X,\, Maps(K,Y)_\ast)
    \;\simeq\;
  Maps(K,\; [\mathcal{C},Top^{\ast/}_{cg}](X,Y))
$$

for all $X,Y \in [\mathcal{C},Top^{\ast/}_{cg}]$ and all $K \in Top^{\ast/}_{cg}$.

In particular there is the combined natural isomorphism

$$
  [\mathcal{C}, Top^{\ast/}_{cg}](X\wedge K, Y)
   \;\simeq\;
  [\mathcal{C}, Top^{\ast/}_{cg}](X, Maps(K,Y)_\ast)
$$

exhibiting a pair of [[adjoint functors]]

$$
  [\mathcal{C}, Top^{\ast/}_{cg}]
    \underoverset
      {\underset{Maps(K,-)_\ast}{\longrightarrow}}
      {\overset{(-)\wedge K}{\longleftarrow}}
      {\bot}
  [\mathcal{C}, Top^{\ast}_{cg}]
  \,.
$$

=--

+-- {: .proof}
###### Proof

Via the [[end]]-expression for $[\mathcal{C},Top^{\ast/}_{cg}](-,-)$ from def. \ref{PointedTopologicalFunctorCategory} and the fact (remark \ref{MappingSpacePreservesEnds}) that the pointed mapping space construction $Maps(-,-)_\ast$ preserves ends in the second variable, this reduces to the fact that $Maps(-,-)_\ast$ is the [[internal hom]] in the [[closed monoidal category]] $Top^{\ast/}_{cg}$ (example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}) and hence satisfies the internal tensor/hom-adjunction isomorphism (prop. \ref{TensorHomAdjunctionIsoInternally}):

$$
  \begin{aligned}
    [\mathcal{C},Top^{\ast/}_{cg}](X \wedge K, Y)
    & =
    \underset{c}{\int}
    Maps(
      (X \wedge K)(c),
      Y(c)
    )_\ast
    \\
    & \simeq
    \underset{c}{\int}
      Maps(X(c) \wedge K, Y(x))_\ast
    \\
    & \simeq
    \underset{c}{\int}
      Maps(K,Maps(X(c), Y(c))_\ast)_\ast
    \\
    & \simeq
    Maps(K, \underset{c}{\int} Maps(X(c),Y(c)))_\ast
    \\
    & =
    Maps(K,[\mathcal{C},Top^{\ast/}_{cg}](X,Y))_\ast
  \end{aligned}
$$

and

$$
  \begin{aligned}
    [\mathcal{C},Top^{\ast/}_{cg}](X, Maps(K,Y)_\ast)
    & =
    \underset{c}{\int}
      Maps(X(c), (Maps(K,Y)_\ast)(c))_\ast
    \\
    & \simeq
    \underset{c}{\int}
     Maps(X(c), Maps(K,Y(c))_\ast)_\ast
    \\
    & \simeq
    \underset{c}{\int} Maps(X(c) \wedge K, Y(c))_\ast
    \\
    & \simeq
    \underset{c}{\int} Maps(K, Maps(X(c),Y(c))_\ast)_\ast
    \\
    & \simeq
    Maps(K, \underset{c}{\int} Maps(X(c),Y(c))_\ast)_\ast
    \\
    & \simeq
    Maps(K, [\mathcal{C},Top^{\ast/}_{cg}](X,Y))_\ast
    \,.
  \end{aligned}
$$

=--



+-- {: .num_prop #TopologicalLeftKanExtensionBCoend}
###### Proposition
**(left Kan extension via coends)**

Let $\mathcal{C}, \mathcal{D}$ be [[small category|small]] pointed [[topologically enriched categories]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) and let

$$
  p \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

be a pointed [[topologically enriched functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)). Then precomposition with $p$ constitutes a functor

$$
  p^\ast
  \;\colon\;
  [\mathcal{D}, Top^{\ast/}_{cg}]
  \longrightarrow
  [\mathcal{C}, Top^{\ast/}_{cg}]
$$

$G\mapsto G\circ p$. This functor has a [[left adjoint]] $Lan_p$, called **left [[Kan extension]]** along $p$

$$
  [\mathcal{D}, Top^{\ast/}_{cg}]
    \underoverset
      {\underset{p^\ast}{\longrightarrow}}
      {\overset{Lan_p }{\longleftarrow}}
      {\bot}
  [\mathcal{C}, Top^{\ast/}_{cg}]
$$

which is given objectwise by a [[coend]] (def. \ref{EndAndCoendInTopcgSmash}):

$$
  (Lan_p F)
  \;\colon\;
  d
  \;\mapsto \;
  \overset{c\in \mathcal{C}}{\int}
   \mathcal{D}(p(c),d) \wedge F(c)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Use the expression of natural transformations in terms of ends (example \ref{NaturalTransformationsViaEnds} and def. \ref{PointedTopologicalFunctorCategory}), then use the respect of $Maps(-,-)_\ast$ for ends/coends (remark \ref{MappingSpacePreservesEnds}),  use the smash/mapping space adjunction ([cor.](Introduction+to+Stable+homotopy+theory+--+P#SmashHomAdjunctionOnPointedCompactlyGeneratedTopologicalSpaces)), use the [[Fubini theorem]] (prop. \ref{CoendsCommuteWithEachOther}) and finally use [[Yoneda reduction]] (prop. \ref{YonedaReductionTopological}) to obtain a sequence of [[natural isomorphisms]] as follows:

$$
  \begin{aligned}
    [\mathcal{D},Top^{\ast/}_{cg}]( Lan_p F, \, G )
    & =
   \underset{d \in \mathcal{D}}{\int}
    Maps( (Lan_p F)(d), \, G(d) )_\ast
   \\
   & =
   \underset{d\in \mathcal{D}}{\int}
   Maps\left(
     \overset{c \in \mathcal{C}}{\int} \mathcal{D}(p(c),d) \wedge F(c)
     ,\;
     G(d)
   \right)_\ast
    \\
  &\simeq
  \underset{d \in \mathcal{D}}{\int}
  \underset{c \in \mathcal{C}}{\int}
  Maps(
    \mathcal{D}(p(c),d)\wedge F(c) \,,\; G(d)
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  \underset{d\in \mathcal{D}}{\int}
  Maps(F(c),
    Maps(
     \mathcal{D}(p(c),d) , \, G(d)
    )_\ast
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  Maps(F(c),
   \underset{d\in \mathcal{D}}{\int}
   Maps(
    \mathcal{D}(p(c),d) , \, G(d)
   )_\ast
  )_\ast
  \\
  & \simeq
  \underset{c\in \mathcal{C}}{\int}
  Maps(F(c), G(p(c))
  )_\ast
  \\
  & =
  [\mathcal{C}, Top^{\ast/}_{cg}](F,p^\ast G)
  \end{aligned}
  \,.
$$

=--






### Topological Day convolution
 {#TopologicalDayConvolution}


Given two [[functions]] $f_1, f_2 \colon G \longrightarrow \mathbb{C}$ on a [[group]] (or just a [[monoid]]) $G$, then their [[convolution product]] is, whenever well defined, given by the sum

$$
  f_1 \star f_2
   \;\colon\;
  g \mapsto
   \underset{g_1 \cdot g_2 = g}{\sum} f_1(g_1) \cdot f_2(g_2)
  \,.
$$

The operation of _[[Day convolution]]_ is the [[categorification]] of this situation where functions are replaced by [[functors]] and [[monoids]] by [[monoidal categories]]. Further [below](#OnPreExcisiveFunctors) we find the [[symmetric monoidal smash product of spectra]] as the Day convolution of topologically enriched functors over the monoidal category of finite pointed CW-complexes, or over sufficiently rich subcategories thereof.

+-- {: .num_defn #TopologicalDayConvolutionProduct}
###### Definition

Let $(\mathcal{C}, \otimes, 1)$ be a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}).

Then the **[[Day convolution]] tensor product** on the pointed topological [[enriched functor category]] $[\mathcal{C},Top^{\ast/}_{cg}]$ (def. \ref{PointedTopologicalFunctorCategory}) is the [[functor]]

$$
  \otimes_{Day}
    \;\colon\;
  [\mathcal{C},Top^{\ast/}_{cg}] \times [\mathcal{C},Top^{\ast/}_{cg}]
    \longrightarrow
  [\mathcal{C},Top^{\ast/}_{cg}]
$$

out of the pointed topological [[product category]] (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) given by the following [[coend]] (def. \ref{EndAndCoendInTopcgSmash})

$$
  X \otimes_{Day} Y
    \;\colon\;
  c
    \;\mapsto\;
  \overset{(c_1,c_2)\in \mathcal{C}\times \mathcal{C}}{\int}
    \mathcal{C}(c_1 \otimes c_2, c) \wedge X(c_1) \wedge Y(c_2)
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $Seq$ denote the category with objects the [[natural numbers]], and only the [[zero morphisms]] and [[identity morphisms]] on these objects (we consider this in a braoder context below in def. \ref{TopologicalDiagramCategoriesForSpectra}):

$$
  Seq(n_1,n_2)
  \coloneqq
  \left\{
    \array{
      S^0 & if\; n_1 = n_2
      \\
      \ast & otherwise
    }
  \right.
  \,.
$$

Regard this as a pointed topologically enriched category in the unique way. The operation of addition of natural numbers $\otimes = +$ makes this a monoidal category.

An object $X_\bullet \in [Seq, Top_{cg}^{\ast/}]$ is an $\mathbb{N}$-sequence of pointed topological spaces. Given two such, then their Day convolution according to def. \ref{TopologicalDayConvolutionProduct} is

$$
  \begin{aligned}
    (X \otimes_{Day} Y)_n
    & =
    \overset{(n_1,n_2)}{\int}
     Seq(n_1 + n_2 , n)
     \wedge
     X_{n_1} \wedge X_{n_2}
    \\
    & = \underset{{n_1+n_2} \atop {= n}}{\coprod} \left(X_{n_1}\wedge X_{n_2}\right)
  \end{aligned}
  \,.
$$

=--


We observe now that [[Day convolution]] is equivalently a [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}). This will be key for understanding [[monoids]] and [[modules]] with respect to Day convolution.

+-- {: .num_defn #ExternalTensorProduct}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] pointed [[topologically enriched category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)).  Its **[[external tensor product]]** is the pointed [[topologically enriched functor]]

$$
  \overline{\wedge}
   \;\colon\;
  [\mathcal{C},Top^{\ast/}_{cg}]
    \times
  [\mathcal{C},Top^{\ast/}_{cg}]
    \longrightarrow
  [\mathcal{C}\times \mathcal{C}, Top^{\ast/}_{cg}]
$$

from pairs of [[topologically enriched functors]] over $\mmathcal{C}$ to topologically enriched functors over the [[product category]] $\mathcal{C} \times \mathcal{C}$ (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) given by

$$
  X \overline{\wedge} Y
    \;\coloneqq\;
  \wedge \circ (X,Y)
  \,,
$$

i.e.

$$
  (X \overline\wedge Y)(c_1,c_2)
  =
  X(c_1)\wedge X(c_2)
  \,.
$$

=--


+-- {: .num_prop #DayConvolutionViaKanExtensionOfExternalTensorAlongTensor}
###### Proposition

For $(\mathcal{C}, \otimes 1)$ a pointed [[topologically enriched category|topologically enriched]] [[monoidal category]] (def. \ref{MonoidalCategory}) the [[Day convolution]] product (def. \ref{TopologicalDayConvolutionProduct}) of two functors is equivalently the [[left Kan extension]] (def. \ref{TopologicalLeftKanExtensionBCoend}) of their external tensor product (def. \ref{ExternalTensorProduct}) along the tensor product $\otimes \colon \mathcal{C} \times \mathcal{C}$: there is a [[natural isomorphism]]

$$
  X \otimes_{Day} Y
  \simeq
  Lan_{\otimes} (X \overline{\wedge} Y)
  \,.
$$

Hence the [[adjunction unit]] is a [[natural transformation]] of the form

$$
  \array{
    \mathcal{C} \times \mathcal{C}
    &&
      \overset{X \overline{\wedge} Y}{\longrightarrow}
    &&
      Top^{\ast/}_{cg}
    \\
    & {}^{\mathllap{\otimes}}\searrow
     &\Downarrow&
    \nearrow_{\mathrlap{X \otimes_{Day} Y}}
    \\
    && \mathcal{C}
  }
  \,.
$$

=--

This perspective is highlighted in ([MMSS 00, p. 60](#MMSS00)).

+-- {: .proof}
###### Proof

By prop. \ref{TopologicalLeftKanExtensionBCoend} we may compute the left Kan extension as the following [[coend]]:

$$
  \begin{aligned}
     Lan_{\otimes_{\mathcal{C}}} (X\overline{\wedge} Y)(c)
     &
     \simeq
      \overset{(c_1,c_2)}{\int}
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c )
      \wedge
      (X\overline{\wedge}Y)(c_1,c_2)
     \\
    & =
    \overset{(c_1,c_2)}{\int}
    \mathcal{C}(c_1\otimes c_2, c)
    \wedge
     X(c_1)\wedge X(c_2)
  \end{aligned}
  \,.
$$


=--

Proposition \ref{DayConvolutionViaKanExtensionOfExternalTensorAlongTensor} implies the following fact, which is the key for the identification of "[[functors with smash product]]" [below](#FunctorsWithSmashProduct) and then for the description of [[ring spectra]] [further below](#HomotopyRingSpectra).

+-- {: .num_cor #DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}
###### Corollary

The operation of [[Day convolution]] $\otimes_{Day}$ (def. \ref{TopologicalDayConvolutionProduct}) is universally characterized by the property that there are [[natural isomorphisms]]

$$
  [\mathcal{C},Top^{\ast/}_{cg}](X \otimes_{Day} Y, Z)
    \simeq
  [\mathcal{C}\times \mathcal{C},Top^{\ast/}_{cg}](
    X \overline{\wedge} Y,\; Z \circ \otimes
  )
  \,,
$$

where $\overline{\wedge}$ is the external product of def. \ref{ExternalTensorProduct}, hence that [[natural transformations]] of functors on $\mathcal{C}$ of the form

$$
  (X \otimes_{Day} Y)(c)
    \longrightarrow
  Z(c)
$$

are in [[natural bijection]] with natural transformations of functors on the [[product category]] $\mmathcal{C}\times \mathcal{C}$ (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) of the form

$$
  X(c_1) \wedge Y(c_2)
   \longrightarrow
  Z(c_1 \otimes c_2)
  \,.
$$

=--


Write

$$
  y \;\colon\; \mathcal{C}^{op} \longrightarrow [\mathcal{C}, Top^{\ast/}_{cg}]
$$

for the $Top^{\ast/}_{cg}$-[[Yoneda embedding]], so that for $c\in \mathcal{C}$ any [[object]], $y(c)$ is the [[representable functor|corepresented functor]] $y(c)\colon d \mapsto \mathcal{C}(c,d)$.


+-- {: .num_prop #DayConvolutionYieldsMonoidalCategoryStructure}
###### Proposition

For $(\mathcal{C},\otimes, 1)$ a [[small category|small]] pointed [[topologically enriched category|topological]] [[monoidal category]] (def. \ref{MonoidalCategory}), the [[Day convolution]] tensor product $\otimes_{Day}$ of def. \ref{TopologicalDayConvolutionProduct} makes the pointed topologically [[enriched functor category]]

$$
  ( [\mathcal{C}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1))
$$

into a pointed topological [[monoidal category]] (def. \ref{MonoidalCategory}) with [[tensor unit]] $y(1)$ [[representable functor|co-represented]] by the tensor unit $1$ of $\mathcal{C}$.

Moreover, if $(\mathcal{C}, \otimes, 1)$ is equipped with a (symmetric) [[braiding]] $\tau^{\mathcal{C}}$ (def. \ref{BraidedMonoidalCategory}), then so is $([\mathcal{C}, Top^{\ast/}_{cg}],\otimes_{Day}, y(1))$.



=--

+-- {: .proof}
###### Proof

Regarding [[associativity]], observe that

$$
  \begin{aligned}
    (X \otimes_{Day} ( Y \otimes_{Day} Z ))(c)
    & \simeq
    \overset{(c_1,c_2)}{\int}
      \mathcal{C}(c_1 \otimes c_2, \,c)
        \wedge
      X(c_1)
       \wedge
      \overset{(d_1,d_2)}{\int}
       \mathcal{C}(d_1 \otimes d_2, c_2 )
       (Y(d_1) \wedge Z(d_2))
    \\
    &\simeq \overset{c_1, d_1, d_2}{\int}
    \underset{\simeq \mathcal{C}(c_1 \otimes (d_1 \otimes_{\mathcal{C}} d_2), c )}{
      \underbrace{
       \overset{c_2}{\int}
         \mathcal{C}(c_1 \otimes c_2 , c)
           \wedge
         \mathcal{C}(d_1 \otimes d_2, c_2 )
      }
    }
    \wedge
    (X(c_1) \wedge (Y(d_1) \wedge Z(d_2)))
    \\
    &\simeq
    \overset{c_1, d_1, d_2}{\int}
     \mathcal{C}(c_1\otimes  ( d_1 \otimes  d_2), c )
       \wedge
     (X(c_1) \wedge (Y(d_1) \wedge Z(d_2)))
    \\
    & \simeq
    \overset{c_1, c_2, c_3}{\int}
     \mathcal{C}(c_1\otimes  ( c_2 \otimes  c_3), c )
       \wedge
     (X(c_1) \wedge (Y(c_2) \wedge Z(c_3)))
  \end{aligned}
  \,,
$$

where we used the [[Fubini theorem]] for [[coends]] (prop. \ref{CoendsCommuteWithEachOther}) and then twice the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}). Similarly

$$
  \begin{aligned}
    (( X \otimes_{Day} Y ) \otimes_{Day} Z)(c)
    & \simeq
    \overset{(c_1,c_2)}{\int}
     \mathcal{C}(c_1 \otimes c_2, c)
     \wedge
    \overset{(d_1,d_2)}{\int}
    \mathcal{C}(d_1 \otimes d_2, c_1)
     \wedge
     (X(d_1) \wedge Y(d_2))
    \wedge
    Y(c_2)
   \\
   & \simeq
   \overset{c_2,d_1,d_2}{\int}
   \underset{\simeq \mathcal{C}((d_1 \otimes d_2) \otimes c_2) }{
   \underbrace{
     \overset{c_1}{\int}
     \mathcal{C}(c_1\otimes c_2, c)
     \wedge
     \mathcal{C}(d_1 \otimes d_2, c_1)
   }}
   \wedge
   ((X(d_1) \wedge Y(d_2)) \wedge Z(c_2))
   \\
   & \simeq
   \overset{c_2,d_1,d_2}{\int}
   \mathcal{C}((d_1 \otimes d_2) \otimes c_2)
   \wedge
   ((X(d_1) \wedge Y(d_2)) \wedge Z(c_2))
   \\
    &\simeq
   \overset{c_1,c_2, c_3}{\int}
   \mathcal{C}((c_1 \otimes c_2) \otimes c_3)
   \wedge
   ((X(c_1) \wedge Y(c_2)) \wedge Z(c_3))
  \end{aligned}
  \,.
$$

So we obtain an [[associator]] by combining, in the integrand, the associator $\alpha^{\mathcal{C}}$ of $(\mathcal{C}, \otimes, 1)$ and $\tau^{Top_{cg}^{\ast/}}$ of $(Top^{\ast/}_{cg}, \wedge, S^0)$ (example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}):

$$
  \array{
    ((X \otimes_{Day} Y) \otimes_{Day} Z)(c)
     &\simeq&
     \overset{c_1,c_2, c_3}{\int}
     \mathcal{C}((c_1 \otimes c_2) \otimes c_3)
     \wedge
    ((X(c_1) \wedge Y(c_2)) \wedge Z(c_3))
    \\
    {}^{\mathllap{
      \alpha^{Day}_{X,Y,Z}(c)
    }}\downarrow
      &&
    \downarrow^{\mathrlap{
      \overset{c_1,c_2,c_3}{\int}
       \mathcal{C}( \alpha^{\mathcal{C}}_{c_1,c_2,c_3} , c )
        \wedge
       \alpha^{Top^{\ast/}_{cg}}_{X(c_1), X(c_2), X(c_3)}
    }}
   \\
   (X \otimes_{Day} (Y \otimes_{Day} Z) )(c)
   &\simeq&
    \overset{c_1, c_2, c_3}{\int}
     \mathcal{C}(c_1\otimes  ( c_2 \otimes  c_3), c )
       \wedge
     (X(c_1) \wedge (Y(c_2) \wedge Z(c_3)))
  }
  \,.
$$

It is clear that this satisfies the [[pentagon identity]], since $\tau^{\mathcal{C}}$ and $\tau^{Top^{\ast/}_{cg}}$ do.

To see that $y(1)$ is the tensor unit for $\otimes_{Day}$,
use the [[Fubini theorem]] for [[coends]] (prop. \ref{CoendsCommuteWithEachOther}) and then twice the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}) to get for any $X \in [\mathcal{C},Top^{\ast/}_{cg}]$ that

$$
  \begin{aligned}
     X \otimes_{Day} y(1)
     &
     =
     \overset{c_1,c_2 \in \mathcal{C}}{\int}
      \mathcal{C}(c_1\otimes_{\mathcal{D}} c_2,-)
      \wedge
     X(c_1) \wedge \mathcal{C}(1,c_2)
     \\
     & \simeq
     \overset{c_1\in \mathcal{C}}{\int}
      \overset{c_2 \in \mathcal{C}}{\int}
        \mathcal{C}(c_1\otimes_{\mathcal{C}} c_2,-)
        \wedge
        \mathcal{C}(1,c_2)
      \wedge X(c_1)
    \\
    & \simeq
      \overset{c_1\in \mathcal{C}}{\int}
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} 1, -)
      \wedge
      X(c_1)
    \\
    & \simeq
      \overset{c_1\in \mathcal{C}}{\int}
      \mathcal{C}(c_1, -)
      \wedge X(c_1)
    \\
    & \simeq
    X(-)
    \\
    & \simeq
    X
  \end{aligned}
  \,.
$$

Hence the right [[unitor]] of Day convolution comes from the unitor of $\mathcal{C}$ under the integral sign:

$$
  \array{
    (X \otimes_{Day} y(1))(c)
    &\simeq&
    \overset{c_1}{\int} \mathcal{C}(c_1 \otimes 1, c) \wedge X(c_1)
    \\
    {}^{\mathllap{r^{Day}_{X}(c) } }\downarrow
      &&
    \downarrow^{\mathrlap{
      \overset{c_1}{\int} \mathcal{C}(r^{\mathcal{C}}_{c_1},c) \wedge X(c_1)
    }}
    \\
    X(c) &\simeq& \overset{c_1}{\int} \mathcal{C}(c_1,c) \wedge X(c_1)
  }
  \,.
$$

Analogously for the left unitor. Hence the triangle identity for $\otimes_{Day}$ follows from the triangle identity in $\mathcal{C}$ under the integral sign.


Similarly, if $\mathcal{C}$ has a [[braiding]] $\tau^{\mathcal{C}}$, it induces a braiding $\tau^{Day}$ under the integral sign:

$$
  \array{
    (X \otimes_{Day} Y)(c)
    & = &
    \overset{c_1,c_2}{\int}
     \mathcal{C}(c_1 \otimes c_2, c) \wedge X(c_1) \wedge Y(c_2)
    \\
    {}^{\mathllap{\tau}^{Day}_{X,Y}(c)}\downarrow
    &&
    \downarrow^{\mathrlap{\overset{c_1,c_2}{\int} \mathcal{C}(\tau^{\mathcal{C}}_{c_1,c_2}, c  ) \wedge \tau^{Top^{\ast/}}_{X(c(1)), X(c_2)}  }}
    \\
    (Y \otimes_{Day} X)(c)
    & = &
    \overset{c_1,c_2}{\int}
     \mathcal{C}(c_2 \otimes c_1, c) \wedge Y(c_2) \wedge X(c_1)
  }
$$

and the hexagon identity for $\tau^{Day}$ follows from that for $\tau^{\mathcal{C}}$ and $\tau^{Top^{\ast/}_{cg}}$



=--

Moreover:


+-- {: .num_prop #DayMonoidalStructureIsClosed}
###### Proposition

For $(\mathcal{C}, \otimes ,1 )$ a [[small category|small]] pointed [[topologically enriched category|topological]] [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory}), the [[monoidal category]] with [[Day convolution]] $([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1))$ from def. \ref{DayConvolutionYieldsMonoidalCategoryStructure} is a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}). Its [[internal hom]] $[-,-]_{Day}$ is given by the [[end]] (def. \ref{EndAndCoendInTopcgSmash})

$$
  [X,Y]_{Day}(c)
  \simeq
   \underset{c_1,c_2}{\int}
      Maps\left(
        \mathcal{C}(c \otimes c_1,c_2),
        \;
        Maps(X(c_1) ,  Y(c_2))_\ast
      \right)_\ast
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using the [[Fubini theorem]] (def. \ref{CoendsCommuteWithEachOther}) and the [[co-Yoneda lemma]] (def. \ref{TopologicalCoYonedaLemma}) and in view of definition \ref{PointedTopologicalFunctorCategory} of the [[enriched functor category]], there is the following sequence of [[natural isomorphisms]]:

$$
  \begin{aligned}
     [\mathcal{C},V]( X, [Y,Z]_{Day} )
       & \simeq
     \underset{c}{\int}
     Maps\left(
        X(c),
        \underset{c_1,c_2}{\int}
        Maps\left(
          \mathcal{C}(c \otimes c_1 , c_2),
          Maps(Y(c_1), Z(c_2))_\ast
        \right)_\ast
     \right)_\ast
     \\
     &
     \simeq
     \underset{c}{\int}
     \underset{c_1,c_2}{\int}
     Maps\left(
       \mathcal{C}(c \otimes c_1, c_2)
         \wedge
       X(c)
         \wedge
       Y(c_1)
       ,\;
       Z(c_2)
     \right)_\ast
     \\
     & \simeq
     \underset{c_2}{\int}
     Maps\left(
       \overset{c,c_1}{\int}
       \mathcal{C}(c \otimes c_1, c_2)
         \wedge
       X(c)
         \wedge
       Y(c_1)
       ,\;
       Z(c_2)
     \right)_\ast
     \\
     &\simeq
     \underset{c_2}{\int}
       Maps\left(
         (X \otimes_{Day} Y)(c_2),
         Z(c_2)
       \right)_\ast
     \\
     &\simeq
     [\mathcal{C},V](X \otimes_{Day} Y, Z)
  \end{aligned}
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

In the situation of def. \ref{DayConvolutionYieldsMonoidalCategoryStructure}, the [[Yoneda embedding]] $c\mapsto \mathcal{C}(c,-)$  constitutes a  [[strong monoidal functor]] (def. \ref{LaxMonoidalFunctor})

$$
  (\mathcal{C},\otimes, 1) \hookrightarrow ([\mathcal{C},V], \otimes_{Day}, y(1))
  \,.
$$

=--

+-- {: .proof}
###### Proof

That the [[tensor unit]] is respected is part of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure}. To see that the [[tensor product]] is respected, apply the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}) twice to get the following natural isomorphism

$$
  \begin{aligned}
    (y(c_1) \otimes_{Day} y(c_2))(c)
    &
    \simeq
    \overset{d_1, d_2}{\int}
      \mathcal{C}(d_1 \otimes d_2, c )
    \wedge
      \mathcal{C}(c_1,d_1)
    \wedge
      \mathcal{C}(c_2,d_2)
    \\
    & \simeq \mathcal{C}(c_1\otimes c_2 , c )
    \\
    &
    = y(c_1 \otimes c_2 )(c)
  \end{aligned}
  \,.
$$

=--







### Functors with smash product
 {#FunctorsWithSmashProduct}

Since the [[symmetric monoidal smash product of spectra]] discussed [below](#OnPreExcisiveFunctors) is an instance of [[Day convolution]] (def. \ref{TopologicalDayConvolutionProduct}), and since [[ring spectra]] are going to be the [[monoids]] (def. \ref{MonoidsInMonoidalCategory}) with respect to this tensor product, we are interested in characterizing the [[monoid in a monoidal category|monoids]] with respect to Day convolution. These turn out to have a particularly transparent expression as what is called _[[functors with smash product]]_, namely [[lax monoidal functors]] from the base monoidal category to $Top^{\ast/}_{cg}$. Their components are pairing maps of the form

$$
  R_{n_1} \wedge R_{n_2} \longrightarrow R_{n_1 + n_2}
$$

satisfying suitable conditions. This is the form in which the structure of [[ring spectra]] usually appears in examples. It is directly analogous to how a [[dg-algebra]], which is equivalently a monoid with respect to the [[tensor product of chain complexes]] (example \ref{dgAlgebraAreMonoidsInChainComplexes}), is given in components .

Here we introduce the concepts of monoidal functors and of [[functors with smash product]] and prove that they are equivalently the monoids with respect to Day convolution.


+-- {: .num_defn #LaxMonoidalFunctor}
###### Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two (pointed) [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}). A topologically enriched **[[lax monoidal functor]]** between them is

1. a [[topologically enriched functor]]

   $$
     F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,,
   $$

1. a morphism

   $$
     \epsilon \;\colon\; 1_{\mathcal{D}} \longrightarrow F(1_{\mathcal{C}})
   $$

1. a [[natural transformation]]

   $$
     \mu_{x,y}
       \;\colon\;
     F(x) \otimes_{\mathcal{D}} F(y)
       \longrightarrow
     F(x \otimes_{\mathcal{C}} y)
   $$

   for all $x,y \in \mathcal{C}$

satisfying the following conditions:

1. **([[associativity]])** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} F(z)
         &\underoverset{\simeq}{a^{\mathcal{D}}_{F(x),F(y),F(z)}}{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}( F(y)\otimes_{\mathcal{D}} F(z) )
       \\
       {}^{\mathllap{\mu_{x,y} \otimes id}}\downarrow
         &&
       \downarrow^{\mathrlap{id\otimes \mu_{y,z}}}
       \\
       F(x \otimes_{\mathcal{C}} y) \otimes_{\mathcal{D}} F(z)
        &&
       F(x) \otimes_{\mathcal{D}} ( F(x \otimes_{\mathcal{C}} y) )
       \\
       {}^{\mathllap{\mu_{x \otimes_{\mathcal{C}} y , z} } }\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{ x, y \otimes_{\mathcal{C}} z  }}}
       \\
       F( ( x \otimes_{\mathcal{C}} y ) \otimes_{\mathcal{C}} z  )
         &\underset{F(a^{\mathcal{C}}_{x,y,z})}{\longrightarrow}&
       F( x \otimes_{\mathcal{C}} ( y \otimes_{\mathcal{C}} z ) )
     }
     \,,
   $$

   where $a^{\mathcal{C}}$ and $a^{\mathcal{D}}$ denote the [[associators]] of the monoidal categories;


1. **([[unitality]])** For all $x \in \mathcal{C}$ the following [[commuting diagram|diagrams commutes]]

   $$
     \array{
       1_{\mathcal{D}} \otimes_{\mathcal{D}} F(x)
         &\overset{\epsilon \otimes id}{\longrightarrow}&
       F(1_{\mathcal{C}}) \otimes_{\mathcal{D}} F(x)
       \\
       {}^{\mathllap{\ell^{\mathcal{D}}_{F(x)}}}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{1_{\mathcal{C}}, x }}}
       \\
       F(x)
         &\overset{F(\ell^{\mathcal{C}}_x )}{\longleftarrow}&
       F(1 \otimes_{\mathcal{C}} x  )
     }
   $$

   and

   $$
     \array{
       F(x) \otimes_{\mathcal{D}}  1_{\mathcal{D}}
         &\overset{id \otimes \epsilon }{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}  F(1_{\mathcal{C}})
       \\
       {}^{\mathllap{r^{\mathcal{D}}_{F(x)}}}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{x, 1_{\mathcal{C}} }}}
       \\
       F(x)
         &\overset{F(r^{\mathcal{C}}_x )}{\longleftarrow}&
       F(x \otimes_{\mathcal{C}} 1  )
     }
     \,,
   $$

   where $\ell^{\mathcal{C}}$, $\ell^{\mathcal{D}}$, $r^{\mathcal{C}}$, $r^{\mathcal{D}}$ denote the left and right [[unitors]] of the two monoidal categories, respectively.

If $\epsilon$ and alll $\mu_{x,y}$ are [[isomorphisms]], then $F$ is called a **strong monoidal functor**.

If moreover $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are equipped with the structure of [[braided monoidal categories]] (def. \ref{BraidedMonoidalCategory}) with [[braidings]] $\tau^{\mathcal{C}}$ and $\tau^{\mathcal{D}}$, respectively, then the lax monoidal functor $F$ is called a **[[braided monoidal functor]]** if in addition the following [[commuting diagram|diagram commutes]] for all objects $x,y \in \mathcal{C}$

$$
  \array{
    F(x) \otimes_{\mathcal{C}} F(y)
      &\overset{\tau^{\mathcal{D}}_{F(x), F(y)}}{\longrightarrow}&
    F(y) \otimes_{\mathcal{D}} F(x)
    \\
    {}^{\mathllap{\mu_{x,y}}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_{y,x}}}
    \\
    F(x \otimes_{\mathcal{C}} y )
      &\underset{F(\tau^{\mathcal{C}}_{x,y}  )}{\longrightarrow}&
    F( y \otimes_{\mathcal{C}} x )
  }
  \,.
$$

A [[homomorphism]] $f\;\colon\; (F_1,\mu_1, \epsilon_1) \longrightarrow (F_2, \mu_2, \epsilon_2)$ between two (braided) lax monoidal functors is a **[[monoidal natural transformation]]**, in that it is a [[natural transformation]] $f_x \;\colon\; F_1(x) \longrightarrow F_2(x)$ of the underlying functors

compatible with the product and the unit in that the following [[commuting diagram|diagrams commute]] for all objects $x,y \in \mathcal{C}$:

$$
  \array{
    F_1(x) \otimes_{\mathcal{D}} F_1(y)
      &\overset{f(x)\otimes_{\mathcal{D}} f(y)}{\longrightarrow}&
    F_2(x) \otimes_{\mathcal{D}} F_2(y)
    \\
    {}^{\mathllap{(\mu_1)_{x,y}}}\downarrow
     &&
    \downarrow^{\mathrlap{(\mu_2)_{x,y}}}
    \\
    F_1(x\otimes_{\mathcal{C}} y)
     &\underset{f(x \otimes_{\mathcal{C}} y ) }{\longrightarrow}&
    F_2(x \otimes_{\mathcal{C}} y)
  }
$$

and

$$
  \array{
    && 1_{\mathcal{D}}
    \\
    & {}^{\mathllap{\epsilon_1}}\swarrow && \searrow^{\mathrlap{\epsilon_2}}
    \\
    F_1(1_{\mathcal{C}})
     &&\underset{f(1_{\mathcal{C}})}{\longrightarrow}&&
    F_2(1_{\mathcal{C}})
  }
  \,.
$$

We write $MonFun(\mathcal{C},\mathcal{D})$ for the resulting [[category]] of lax monoidal functors between monoidal categories $\mathcal{C}$ and $\mathcal{D}$, similarly $BraidMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[braided monoidal categories]], and $SymMonFun(\mathcal{C},\mathcal{D})$ for the category of braided monoidal functors between [[symmetric monoidal categories]].

=--

+-- {: .num_remark #SymmetricMonoidalFunctor}
###### Remark

In the literature the term "monoidal functor" often refers by default to what in def. \ref{LaxMonoidalFunctor} is called a _strong monoidal functor_.  But for the purpose of the discussion of [[functors with smash product]] [below](#FunctorsWithSmashProduct), it is crucial to admit the generality of lax monoidal functors.

If $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) then a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between them  is often called a **[[symmetric monoidal functor]]**.

=--

+-- {: .num_prop #MonoidalFunctorComp}
###### Proposition

For $\mathcal{C} \overset{F}{\longrightarrow} \mathcal{D} \overset{G}{\longrightarrow} \mathcal{E}$ two composable [[lax monoidal functors]] (def. \ref{LaxMonoidalFunctor}) between [[monoidal categories]], then their composite $F \circ G$ becomes a lax monoidal functor with structure morphisms

$$
  \epsilon^{G\circ F}
    \;\colon\;
  1_{\mathcal{E}}
    \overset{\epsilon^G}{\longrightarrow}
  G(1_{\mathcal{D}})
    \overset{G(\epsilon^F)}{\longrightarrow}
  G(F(1_{\mathcal{C}}))
$$

and

$$
  \mu^{G \circ F}_{c_1,c_2}
  \;\colon\;
  G(F(c_1)) \otimes_{\mathcal{E}} G(F(c_2))
   \overset{\mu^{G}_{F(c_1), F(c_2)}}{\longrightarrow}
  G( F(c_1) \otimes_{\mathcal{D}} F(c_2) )
    \overset{G(\mu^F_{c_1,c_2})}{\longrightarrow}
  G(F( c_1 \otimes_{\mathcal{C}} c_2 ))
  \,.
$$

=--


+-- {: .num_prop #MonoidsPreservedByLaxMonoidalFunctor}
###### Proposition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D}, \otimes_{\mathcal{D}},1_{\mathcal{D}})$ be two [[monoidal categories]] (def. \ref{MonoidalCategory}) and let $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[lax monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between them.

Then for $(A,\mu_A,e_A)$ a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}), its image $F(A) \in \mathcal{D}$ becomes a monoid $(F(A), \mu_{F(A)}, e_{F(A)})$ by setting

$$
  \mu_{F(A)}
   \;\colon\;
  F(A) \otimes_{\mathcal{C}} F(A)
    \overset{}{\longrightarrow}
  F(A \otimes_{\mathcal{C}} A)
    \overset{F(\mu_A)}{\longrightarrow}
  F(A)
$$

(where the first morphism is the structure morphism of $F$) and setting

$$
  e_{F(A)}
    \;\colon\;
  1_{\mathcal{D}}
    \longrightarrow
  F(1_{\mathcal{C}})
    \overset{F(e_A)}{\longrightarrow}
  F(A)
$$

(where again the first morphism is the corresponding structure morphism of $F$).

This construction extends to a functor

$$
  Mon(F)
   \;\colon\;
  Mon(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})
    \longrightarrow
  Mon(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}})
$$

from the [[category of monoids]] of $\mathcal{C}$ (def. \ref{MonoidsInMonoidalCategory}) to that of $\mathcal{D}$.

Moreover, if $\mathcal{C}$ and $\mathcal{D}$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) and $F$ is a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}) and $A$ is a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}) then so is $F(A)$, and this construction extends to a functor

$$
  CMon(F)
   \;\colon\;
  CMon(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})
    \longrightarrow
  CMon(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}})
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows immediately from combining the associativity and unitality (and symmetry) constraints of $F$ with those of $A$.

=--


+-- {: .num_defn #ModuleOverAMonoidalFunctor}
###### Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}} )$ be two (pointed) [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}), and let $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[topologically enriched functor|topologically enriched]] [[lax monoidal functor]] between them, with product operation $\mu$.

Then a left **[[module over a monoidal functor|module over the lax monoidal functor]]** is

1. a [[topologically enriched functor]]

   $$
     G \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
     \,;
   $$

1. a [[natural transformation]]

   $$
     \rho_{x,y}
       \;\colon\;
     F(x) \otimes_{\mathcal{D}} G(y)
      \longrightarrow
    G(x \otimes_{\mathcal{C}} y )
   $$

such that

* **(action property)** For all objects $x,y,z \in \mathcal{C}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (F(x) \otimes_{\mathcal{D}} F(y)) \otimes_{\mathcal{D}} G(z)
         &\underoverset{\simeq}{a^{\mathcal{D}}_{F(x),F(y),F(z)}}{\longrightarrow}&
       F(x) \otimes_{\mathcal{D}}( F(y)\otimes_{\mathcal{D}} G(z) )
       \\
       {}^{\mathllap{\mu_{x,y} \otimes id}}\downarrow
         &&
       \downarrow^{\mathrlap{id\otimes \rho_{y,z}}}
       \\
       F(x \otimes_{\mathcal{C}} y) \otimes_{\mathcal{D}} G(z)
        &&
       F(x) \otimes_{\mathcal{D}} ( G(x \otimes_{\mathcal{C}} y) )
       \\
       {}^{\mathllap{\rho_{x \otimes_{\mathcal{C}} y , z} } }\downarrow
         &&
       \downarrow^{\mathrlap{\rho_{ x, y \otimes_{\mathcal{C}} z  }}}
       \\
       G( ( x \otimes_{\mathcal{C}} y ) \otimes_{\mathcal{C}} z  )
         &\underset{F(a^{\mathcal{C}}_{x,y,z})}{\longrightarrow}&
       G( x \otimes_{\mathcal{C}} ( y \otimes_{\mathcal{C}} z ) )
     }
     \,,
   $$

A [[homomorphism]] $f\;\colon\; (G_1, \rho_1) \longrightarrow (G_2,\rho_2)$ between two modules over a monoidal functor $(F,\mu,\epsilon)$ is

* a [[natural transformation]] $f_x \;\colon\; G_1(x) \longrightarrow G_2(x)$ of the underlying functors

compatible with the action in that the following [[commuting diagram|diagram commutes]] for all objects $x,y \in \mathcal{C}$:

$$
  \array{
    F(x) \otimes_{\mathcal{D}} G_1(y)
      &\overset{id \otimes_{\mathcal{D}} f(y)}{\longrightarrow}&
    F(x) \otimes_{\mathcal{D}} G_2(y)
    \\
    {}^{\mathllap{(\rho_1)_{x,y}}}\downarrow
     &&
    \downarrow^{\mathrlap{(\rhi_2)_{x,y}}}
    \\
    G_1(x\otimes_{\mathcal{C}} y)
     &\underset{f(x \otimes_{\mathcal{C}} y ) }{\longrightarrow}&
    G_2(x \otimes_{\mathcal{C}} y)
  }
$$

We write $F Mod$ for the resulting category of modules over the monoidal functor $F$.

=--

Now we may finally state the main proposition on _[[functors with smash product]]_:

+-- {: .num_prop #DayMonoidsAreLaxMonoidalFunctorsOnTheSite}
###### Proposition

Let $(\mathcal{C},\otimes, 1)$ be a pointed [[topologically enriched category|topologically enriched]] ([[symmetric monoidal category|symmetric]]) [[monoidal category]] (def. \ref{MonoidalCategory}). Regard $(Top_{cg}^{\ast/}, \wedge , S^0)$ as a topological [[symmetric monoidal category]] as in example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}.

Then ([[commutative monoid in a symmetric monoidal category|commutative]]) [[monoid in a monoidal category|monoids in]] (def. \ref{MonoidsInMonoidalCategory}) the [[Day convolution]] monoidal category $([\mathcal{C}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))$ of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} are equivalent to ([[braided monoidal functor|braided]]) [[lax monoidal functors]] (def. \ref{LaxMonoidalFunctor}) of the form

$$
  (\mathcal{C},\otimes, 1) \longrightarrow (Top^{\ast}_{cg}, \wedge, S^0)
  \,,
$$

called **[[functors with smash products]]** on $\mathcal{C}$, i.e. there are [[equivalences of categories]] of the form

$$
  \begin{aligned}
    Mon([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))
      &\simeq
    MonFunc(\mathcal{C},Top^{\ast/}_{cg})
    \\
    CMon([\mathcal{C},Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{C}}))
      &\simeq
    SymMonFunc(\mathcal{C},Top^{\ast/}_{cg})
  \end{aligned}
  \,.
$$

Moreover, [[module objects]] over these monoid objects are equivalent to the corresponding [[modules over monoidal functors]] (def. \ref{ModuleOverAMonoidalFunctor}).

=--

This is stated in some form in ([Day 70, example 3.2.2](Day+convolution#Day70)). It is highlighted again in ([MMSS 00, prop. 22.1](#MMSS00)).

+-- {: .proof}
###### Proof

By definition \ref{LaxMonoidalFunctor}, a [[lax monoidal functor]] $F \colon \mathcal{C} \to Top^{\ast/}_{cg}$ is a topologically enriched functor equipped with a morphism of [[pointed topological spaces]] of the form

$$
  S^0 \longrightarrow F(1_{\mathcal{C}})
$$

and equipped with a [[natural transformation|natural]] system of maps of pointed topological spaces of the form

$$
  F(c_1) \wedge F(c_2) \longrightarrow F(c_1 \otimes_{\mathcal{C}} c_2)
$$

for all $c_1,c_2 \in \mathcal{C}$.

Under the [[Yoneda lemma]] (prop. \ref{YonedaReductionTopological}) the first of these is equivalently a morphism in $[\mathcal{C}, Top^{\ast/}_{cg}]$ of the form

$$
  y(S^0) \longrightarrow F
  \,.
$$

Moreover, under the [[natural isomorphism]] of corollary \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor} the second of these is equivalently a morphism in $[\mathcal{C}, Top^{\ast/}_{cg}]$ of the form

$$
  F \otimes_{Day} F \longrightarrow F
  \,.
$$

Translating the conditions of def. \ref{LaxMonoidalFunctor} satisfied by a [[lax monoidal functor]] through these identifications gives precisely the conditions of def. \ref{MonoidsInMonoidalCategory} on a ([[commutative monoid in a symmetric monoidal category|commutative]]) [[monoid in a monoidal category|monoid in]] object $F$ under $\otimes_{Day}$.

Similarly for [[module objects]] and [[modules over monoidal functors]].

=--


+-- {: .num_prop #PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution}
###### Proposition

Let $f \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ be a [[lax monoidal functor]] (def. \ref{LaxMonoidalFunctor}) between pointed [[topologically enriched category|topologically enriched]] [[monoidal categories]] (def. \ref{MonoidalCategory}). Then the induced functor

$$
  f^\ast
    \;\colon\;
  [\mathcal{D}, Top^{\ast/}_{cg}]
    \longrightarrow
  [\mathcal{C}, Top_{cg}^{\ast}]
$$

given by $(f^\ast X)(c)\coloneqq X(f(c))$ preserves [[monoid in a monoidal category|monoids]] under [[Day convolution]]

$$
  f^\ast
    \;\colon\;
  Mon([\mathcal{D}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{D}}))
    \longrightarrow
  Mon([\mathcal{C}, Top_{cg}^{\ast}], \otimes_{Day}, y(1_{\mathcal{C}})
$$


Moreover, if $\mathcal{C}$ and $\mathcal{D}$ are [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}) and $f$ is a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}), then $f^\ast$ also preserves [[commutative monoids in a symmetric monoidal category|commutative monoids]]

$$
  f^\ast
    \;\colon\;
  CMon([\mathcal{D}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{D}}))
    \longrightarrow
  CMon([\mathcal{C}, Top_{cg}^{\ast}], \otimes_{Day}, y(1_{\mathcal{C}})
  \,.
$$

Similarly, for

$$
   A
    \in
   Mon([\mathcal{D}, Top^{\ast/}_{cg}], \otimes_{Day}, y(1_{\mathcal{D}}))
$$

any fixed monoid, then $f^\ast$ sends $A$-[[module object|modules]] to $f^\ast(A)$-modules

$$
  f^\ast
    \;\colon\;
  A Mod(\mathcal{D})
    \longrightarrow
  (f^\ast A)Mod(\mathcal{C})
  \,.
$$




=--

+-- {: .proof}
###### Proof

This is an immediate corollary of prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite}, since the composite of two (braided) lax monoidal functors is itself canonically a (braided) lax monoidal functor by prop. \ref{MonoidalFunctorComp}.

=--







## $\mathbb{S}$-Modules
 {#SModules}

We give a unified discussion of the categories of

1. [[sequential spectra]]

1. [[symmetric spectra]]

1. [[orthogonal spectra]]

1. pre-[[excisive functors]]

(all in [[topological spaces]]) as [[categories of modules]] with respect to [[Day convolution]] monoidal structures on [[Top]]-[[enriched functor categories]] over restrictions to [[faithful functor|faithful]] sub-[[sites]] of the canonical representative of the [[sphere spectrum]] as a pre-excisive functor on $Top^{\ast/}_{fin}$.

This approach is due to ([Mandell-May-Schwede-Shipley 00](#MMSS00)) following ([Hovey-Shipley-Smith 00](HoveyShipleySmith00)).






### Pre-Excisive functors
 {#OnPreExcisiveFunctors}

We consider an almost tautological construction of a pointed topologically enriched category equipped with a closed symmetric monoidal product: the category of _[[pre-excisive functors]]_. Then we show that this tautological category restricts, in a certain sense, to the category of [[sequential spectra]]. However, under this restriction the symmetric monoidal product breaks, witnessing the lack of a functorial [[smash product of spectra]] on sequential spectra. However from inspection of this failure we see that there are categories of [[structured spectra]] "in between" those of all pre-excisive functors and plain sequential spectra, notably the categories of _[[orthogonal spectra]]_ and of _[[symmetric spectra]]_. These intermediate categories retain the concrete tractable nature of sequential spectra, but are rich enough to also retain the symmetric monoidal product inherited from pre-excisive functors: this is the _[[symmetric monoidal smash product of spectra]]_ that we are after.

**Literature** ([MMSS 00, Part I and Part III](#MMSS00))

$\,$

+-- {: .num_defn #FinitePointedCWComplexes}
###### Definition

Write

$$
  \iota_{fin}\;\colon\; Top^{\ast/}_{cg,fin} \hookrightarrow Top^{\ast/}_{cg}
$$

for the [[full subcategory]] of [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#Top)) on those that admit the structure of a [[finite CW-complex]] (a [[CW-complex]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCellComplex)) with a [[finite number]] of cells).

We say that the pointed topological [[enriched functor category]] (def. \ref{PointedTopologicalFunctorCategory})

$$
  Exc(Top_{cg})
   \coloneqq
  [Top^{\ast/}_{cg,fin}, Top^{\ast/}_{cg}]
$$

is the category of **[[pre-excisive functors]]**. (We had previewed this in [[Introduction to Stable homotopy theory -- P|Part P]], [this example](Introduction+to+Stable+homotopy+theory+--+P#PreExcisiveFunctors)).


Write

$$
  \mathbb{S}_{exc}
    \coloneqq
  y(S^0)
  \coloneqq
  Top^{\ast/}_{cg,fin}(S^0,-)
$$

for the [[representable functor|functor co-represented]] by [[0-sphere]]. This is equivalently the inclusion $\iota_{fin}$ itself:

$$
  \mathbb{S}_{exc} = \iota_{fin}
    \;\colon\;
  K \mapsto K
  \,.
$$

We call this the standard incarnation of the **[[sphere spectrum]]** as a pre-excisive functor.

By prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} the [[smash product]] of [[pointed topological spaces|pointed]] [[compactly generated topological spaces]] induces the structure of a [[closed monoidal category|closed]] (def. \ref{ClosedMonoidalCategory}) [[symmetric monoidal category]] (def. \ref{SymmetricMonoidalCategory})

$$
  \left(
    Exc(Top_{cg})
    ,\;
    \wedge \coloneqq \otimes_{Day}
    ,\;
   \mathbb{S}_{exc}
  \right)
$$

with

1. [[tensor unit]] the [[sphere spectrum]] $\mathbb{S}_{exc}$;

1. [[tensor product]] the [[Day convolution product]] $\otimes_{Day}$ from def. \ref{TopologicalDayConvolutionProduct},

   called the **[[symmetric monoidal smash product of spectra]]** for the model of pre-excisive functors;

1. [[internal hom]] the dual operation $[-,-]_{Day}$ from prop. \ref{DayMonoidalStructureIsClosed},

   called the **[[mapping spectrum]]** construction for pre-excisive functors.

=--


+-- {: .num_remark #EveryPreExcisiveFunctorIsSModule}
###### Remark

By example \ref{MonoidGivenByTensorUnit} the [[sphere spectrum]] incarnated as a pre-excisive functor $\mathbb{S}_{exc}$ (according to def. \ref{FinitePointedCWComplexes}) is canonically a [[commutative monoid in a symmetric monoidal category|commutative monoid in]] the category of pre-excisive functors  (def. \ref{MonoidsInMonoidalCategory}).

Moreover, by example \ref{EveryObjectIsModuleOverTensorUnit}, every object of $Exc(Top_{cg})$ (def. \ref{FinitePointedCWComplexes}) is canonically a [[module object]] over $\mathbb{S}_{exc}$. We may therefore tautologically identify the category of pre-excisive functors with the [[module category]] over the sphere spectrum:

$$
  Exc(Top_{cg})
    \simeq
  \mathbb{S}_{exc}Mod
  \,.
$$

=--

+-- {: .num_lemma #FSPExcisiveSphere}
###### Lemma

Identified as a [[functor with smash product]] under prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite}, the pre-excisive [[sphere spectrum]] $\mathbb{S}_{exc}$ from def. \ref{FinitePointedCWComplexes} is given by the identity natural transformation

$$
  \mu_{(K_1,K_2)}
    \;\colon\;
  \mathbb{S}_{exc}(K_1) \wedge \mathbb{S}_{exc}(K_2)
  =
  K_1 \wedge K_2
    \overset{=}{\longrightarrow}
  K_1 \wedge K_2
  =
  \mathbb{S}_{exc}(K_1 \wedge K_2)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We claim that this is in fact the unique structure of a [[monoidal functor]] that may be imposed on the canonical inclusion $\iota \;\colon\; Top^{\ast/}_{cg,fin} \hookrightarrow Top^{\ast/}_{cg}$, hence it must be the one in question. To see the uniqueness, observe that naturality of the matural transformation $\mu$ in particular says that there are commuting squares of the form

$$
  \array{
    S^0 \wedge S^0 &\overset{=}{\longrightarrow}& S^0 \wedge S^0
    \\
    {}^{\mathllap{x_1,x_2}}\downarrow && \downarrow^{\mathrlap{x_1,x_2}}
    \\
    K_1 \wedge K_2
      &\underset{\mu_{K_1, K_2}}{\longrightarrow}&
    K_1 \wedge K_2
  }
  \,,
$$

where the vertical morphisms pick any two points in $K_1$ and $K_2$, respectively, and where the top morphism is necessarily the canonical identification since there is only one single isomorphism $S^0 \to S^0$, namely the identity. This shows that the bottom horizontal morphism has to be the identity on all points, hence has to be the identity.

=--


We now consider restricting the domain of the pre-excisive functors of def. \ref{FinitePointedCWComplexes}.

+-- {: .num_defn #TopologicalDiagramCategoriesForSpectra}
###### Definition

Define the following [[pointed topologically enriched categories|pointed topologically enriched]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopEnrichedCategory)) [[symmetric monoidal categories]] (def. \ref{SymmetricMonoidalCategory}):

1. $Seq$ is the category whose objects are the [[natural numbers]] and which has only identity morphisms and [[zero morphisms]] on these objects, hence the [[hom-spaces]] are

   $$
     Seq(n_1,n_2)
       \;\coloneqq\;
     \left\{
       \array{
          S^0 & for\; n_1 = n_2
          \\
          \ast & otherwise
       }
    \right.
   $$

   The tensor product is the addition of natural numbers, $\otimes = +$, and the [[tensor unit]] is 0. The [[braiding]] is, necessarily, the identity.

1. $Sym$ is the standard [[skeletal category|skeleton]] of the [[core]] of [[FinSet]] with [[zero morphisms]] adjoined: its [[objects]] are the [[finite sets]] $\overline{n} \coloneqq \{1, \cdots,n\}$ for $n \in \mathbb{N}$ (hence $\overline{0}$ is the [[empty set]]), all non-[[zero morphism|zero]] morphisms are [[automorphisms]] and the [[automorphism group]] of $\{1,\cdots,n\}$ is the [[symmetric group]] $\Sigma(n)$ on $n$ elements, hence the [[hom-spaces]] are the following [[discrete topological spaces]]:

   $$
     Sym(n_1, n_2)
      \;\coloneqq\;
     \left\{
       \array{
          (\Sigma(n_1))_+ & for \; n_1 = n_2
          \\
          \ast & otherwise
       }
     \right.
   $$

   The [[tensor product]] is the [[disjoint union]] of sets, tensor unit is the [[empty set]]. The [[braiding]]

   $$
     \tau^{Sym}_{n_1 , n_2}
     \;\colon\;
     \overline{n_1} \cup \overline{n_2}
       \overset{}{\longrightarrow}
     \overline{n_2} \cup \overline{n_1}
   $$

   is given by the canonical [[permutation]] in $\Sigma(n_1+n_2)$ that [[shuffle|shuffles]] the first $n_1$ elements past the remaining $n_2$ elements.

   ([MMSS 00, example 4.2](#MMSS00))


1. $Orth$ has as objects the finite dimenional real linear [[inner product spaces]] $(\mathbb{R}^n, \langle -,-\rangle)$ and as non-zero morphisms the [[linear map|linear]] [[isometry|isometric]] [[isomorphisms]] between these; hence the [[automorphism group]] of the object $(\mathbb{R}^n, \langle -,-\rangle)$ is the [[orthogonal group]] $O(n)$; the monoidal product is [[direct sum]] of linear spaces, the tensor unit is the 0-vector space; again we turn this into a $Top^{\ast/}_{cg}$-enriched category by adjoining a basepoint to the hom-spaces;

   $$
     Orth(V_1,V_2)
       \;\coloneqq\;
     \left\{
        \array{
          O(V_1)_+ & for \; dim(V_1) = dim(V_2)
          \\
          \ast & otherwise
        }
     \right.
   $$

   The [[tensor product]] is the [[direct sum]] of linear inner product spaces, tensor unit is the 0-vector space. The [[braiding]]

   $$
     \tau^{Orth}_{V_1,V_2}
     \;\colon\;
     V_1 \oplus V_2
     \longrightarrow
     V_2 \oplus V_1
   $$

   is the canonical orthogonal transformation that switches the summands.

   ([MMSS 00, example 4.4](#MMSS00))


Notice that in the notation of example \ref{CoendGivesQuotientByDiagonalGroupAction}

1. the [[full subcategory]] of $Orth$ on $V$ is $\mathbf{B}(O(V)_+)$;

1. the [[full subcategory]] of $Sym$ on $\{1,\cdots,n\}$ is $\mathbf{B}(\Sigma(n)_+)$;

1. the [[full subcategory]] of $Seq$ on $n$ is $\mathbf{B}(1_+)$.

Moreover, after discarding the [[zero morphisms]], then these categories are the disjoint union of categories of the form $\mathbf{B}O(n)$, $\mathbf{B}\Sigma(n)$ and $\mathbf{B}1 = \ast$, respectively.

There is a sequence of canonical [[faithful functor|faithful]] pointed topological [[subcategory]] inclusions

$$
 \array{
   Seq
     &\stackrel{seq}{\hookrightarrow}&
   Sym
    &\stackrel{sym}{\hookrightarrow}&
   Orth
     &\stackrel{orth}{\hookrightarrow}&
   Top_{cg,fin}^{\ast/}
   \\
   n
    &\mapsto&
   \{1,\cdots, n\}
     &\mapsto&
   \mathbb{R}^n
    &\mapsto&
   S^n
  }
  \,,
$$

into the pointed topological category of pointed compactly generated topological spaces of finite CW-type (def. \ref{FinitePointedCWComplexes}).

Here $S^V$ denotes the [[one-point compactification]] of $V$. On morphisms $sym \colon (\Sigma_n)_+ \hookrightarrow (O(n))_+$ is the canonical inclusion of [[permutation]] matrices into [[orthogonal group|orthogonal]] matrices and $orth \colon O(V)_+ \hookrightarrow Aut(S^V)$ is on $O(V)$ the [[topological subspace]] inclusions of the pointed [[homeomorphisms]] $S^V \to S^V$ that are induced under forming [[one-point compactification]] from linear isometries of $V$ ("[[representation spheres]]").

Below we will often use these identifications to write just "$n$" for any of these objects, leaving implicit the identifications $n \mapsto \{1, \cdots, n\} \mapsto S^n$.

Consider the pointed topological diagram categries  (def. \ref{PointedTopologicalFunctorCategory}, [exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk)) over these categories:

* $[Seq,Top^{\ast/}_{cg}]$ is called the category of **sequences** of pointed topological spaces (e.g. [HSS 00, def. 2.3.1](#HoveyShipleySmith00));

* $[Sym,Top^{\ast/}_{cg}]$ is called the category of **[[symmetric sequences]]** (e.g. [HSS 00, def. 2.1.1](#HoveyShipleySmith00));

* $[Orth, Top^{\ast/}_{cg}]$ is called the category of **orthogonal sequences**.

Consider the sequence of restrictions of topological diagram categories, according to prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution} along the above inclusions:

$$
  Exc(Top_{cg})
    \overset{orth^\ast}{\longrightarrow}
  [Orth,Top^{\ast/}_{cg}]
    \overset{sym^\ast}{\longrightarrow}
  [Sym,Top^{\ast/}_{cg}]
    \overset{seq^\ast}{\longrightarrow}
  [Seq,Top^{\ast/}_{cg}]
  \,.
$$

Write

$$
  \mathbb{S}_{orth} \coloneqq orth^\ast \mathbb{S}_{exc}
  \,,
  \;\;\;\;\;\;\;\;
  \mathbb{S}_{sym} \coloneqq sym^\ast \mathbb{S}_{orth}
  \,,
  \;\;\;\;\;\;\;\;
  \mathbb{S}_{seq} \coloneqq seq^\ast \mathbb{S}_{sym}
$$

for the restriction of the excisive functor incarnation of the [[sphere spectrum]] (from def. \ref{FinitePointedCWComplexes}) along these inclusions.

=--

+-- {: .num_prop #BraidedFunctorsOrthAndSym}
###### Proposition

The functors $seq$, $sym$ and $orth$ in def. \ref{TopologicalDiagramCategoriesForSpectra} become [[strong monoidal functors]] (def. \ref{LaxMonoidalFunctor}) when equipped with the canonical isomorphisms

$$
  seq(n_1) \cup seq(n_2)
   =
  \{1,\cdots, n_1\} \cup \{1, \cdots, n_2\}
  \simeq
   \{1, \cdots, n_1+ n_2\}
  =
  seq(n_1 + n_2)
$$

and

$$
  sym(\{1,\cdots,n_1\}) \oplus sym(\{1,\cdots,n_2\})
  =
  \mathbb{R}^{n_1} \oplus \mathbb{R}^{n_2}
  \simeq
  \mathbb{R}^{n_1 + n_2}
  =
  sym(\{1,\cdots, n_1\} \cup \{1,\cdots, n_2\})
$$

and

$$
  orth(V_1) \wedge orth(V_2)
  =
  S^{V_1} \wedge S^{V_2}
  \simeq
  S^{V_1 \oplus V_2}
  =
  orth(V_1 \oplus V_2)
  \,.
$$

Moreover, $orth$ and $sym$ are [[braided monoidal functors]] (def. \ref{LaxMonoidalFunctor}) (hence [[symmetric monoidal functors]], remark \ref{SymmetricMonoidalFunctor}). But $seq$ is _not_ braided monoidal.

=--

+-- {: .proof}
###### Proof

The first statement is clear from inspection.

For the second statement it is sufficient to observe that all the nontrivial braiding of [[n-spheres]] in $Top^{\ast/}_{cg}$ is given by the maps induced from exchanging coordinates in the realization of $n$-spheres as [[one-point compactifications]] of [[Cartesian spaces]] $S^n \simeq (\mathbb{R}^n)^\ast$. This corresponds precisely to the action of the [[symmetric group]] inside the [[orthogonal group]] acting via the canonical action of the orthogonal group on $\mathbb{R}^n$. This shows that $sym$ and $orth$ are braided, for they include precisely these objects (the $n$-spheres) with these braidings on them. Finally it is clear that $seq$ is not braided, because the braiding on $Seq$ is trivial, while that on $Sym$ is not, so $seq$ necessrily fails to preserve precisely these non-trivial isomorphisms.

=--


+-- {: .num_remark #RestrictionsOfExcisiveSphere}
###### Remark


Since the standard excisive incarnation $\mathbb{S}_{exc}$ of the [[sphere spectrum]] (def. \ref{FinitePointedCWComplexes}) is the [[tensor unit]] with repect to the [[Day convolution]] product on pre-excisive functors, and since it is therefore canonically a [[commutative monoid]], by example \ref{MonoidGivenByTensorUnit},
prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution}
says that the restricted sphere spectra $\mathbb{S}_{orth}$, $\mathbb{S}_{sym}$ and $\mathbb{S}_{seq}$ are still [[monoid object|monoids]], and that under restriction every [[pre-excisive functor]], regarded as a $\mathbb{S}_{exc}$-[[module object|module]] via remark \ref{EveryPreExcisiveFunctorIsSModule}, canonically becomes a [[module object|module]] under the restricted sphere spectrum:

$$
  \begin{aligned}
    orth^\ast
    & \colon\;
  Exc(Top_{cg})
  \simeq
  \mathbb{S}_{exc} Mod
   \longrightarrow
  \mathbb{S}_{orth} Mod
  \\
  sym^\ast
   &\colon\;
  Exc(Top_{cg})
  \simeq
  \mathbb{S}_{exc} Mod
   \longrightarrow
  \mathbb{S}_{sym} Mod
  \\
  seq^\ast
   &\colon\;
  Exc(Top_{cg})
  \simeq
  \mathbb{S}_{exc} Mod
   \longrightarrow
  \mathbb{S}_{seq} Mod
  \end{aligned}
  \,.
$$

Since all three functors $orth$, $sym$ and $seq$ are strong monoidal functors by prop. \ref{BraidedFunctorsOrthAndSym}, all three restricted sphere spectra $\mathbb{S}_{orth}$, $\mathbb{S}_{sym}$ and $\mathbb{S}_{seq}$ canonically are [[monoids]], by prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution}.
Moreover, according to prop. \ref{BraidedFunctorsOrthAndSym}, $orth$ and $sym$ are [[braided monoidal functors]], while functor $seq$ is not braided, therefore prop. \ref{PullbackAlongLaxMonoidalFunctorPreservesMonoidsForDayConvolution} furthermore gives that $\mathbb{S}_{orth}$ and $\mathbb{S}_{sym}$ are [[commutative monoid in a symmetric monoidal category|commutative monoids]], while $\mathbb{S}_{seq}$ is not commutative:


| [[sphere spectrum]] | $\mathbb{S}_{exc}$ | $\mathbb{S}_{orth}$ | $\mathbb{S}_{sym}$ | $\mathbb{S}_{seq}$ |
|--|--------------|---------------------|--------------------|-------------------|
| [[monoid in a monoidal category|monoid]] | yes | yes | yes | yes |
| [[commutative monoid in a symmetric monoidal category|commutative monoid]] | yes | yes | yes | no |
| [[tensor unit]] | yes | no | no | no |

=--

Explicitly:

+-- {: .num_lemma #FSPStructuredSphereSpectra}
###### Lemma

The monoids $\mathbb{S}_{dia}$ from def. \ref{TopologicalDiagramCategoriesForSpectra} are, when identified as [[functors with smash product]] via prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} given by assigning

$$
  \mathbb{S}_{seq} \;\colon\; n \mapsto S^{n}
$$

$$
  \mathbb{S}_{sym} \;\colon\; \overline{n} \mapsto S^n
$$

$$
  \mathbb{S}_{orth} \;\colon\; V \mapsto S^V
  \,,
$$

respectively, with product given by the canonical isomorphisms

$$
  S^{V_1} \wedge S^{V_2} \longrightarrow S^{V_1 \oplus V_2}
  \,.
$$


=--

+-- {: .proof}
###### Proof

By construction these functors with smash products are the composites, according to prop. \ref{MonoidalFunctorComp}, of the monoidal functors $seq$, $sym$, $orth$, respectively, with the lax monoidal functor corresponding to $\mathbb{S}_{exc}$. The former have as structure maps the canonical identifications by definition, and the latter has as structure map the canonical identifications by lemmma \ref{FSPExcisiveSphere}.

=--




+-- {: .num_prop #SseqModulesAreSequentialSpectra}
###### Proposition

There is an [[equivalence of categories]]

$$
  (-)^{seq}
  \;\colon\;
  \mathbb{S}_{seq} Mod
    \overset{}{\longrightarrow}
  SeqSpec(Top_{cg})
$$

which identifies the [[category of modules]] (def. \ref{ModulesInMonoidalCategory}) over the [[monoid object|monoid]] $\mathbb{S}_{seq}$ (remark \ref{RestrictionsOfExcisiveSphere}) in the [[Day convolution]] monoidal structure (prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure}) over the topological functor category $[Seq,Top^{\ast/}_{cg}]$ from def. \ref{TopologicalDiagramCategoriesForSpectra} with the category of [[sequential spectra]] ([def.](Introduction+to+Stable+homotopy+theory+--+1#SequentialSpectra))

Under this equivalence, an $\mathbb{S}_{seq}$-module $X$ is taken to the sequential pre-spectrum $X^{seq}$ whose component spaces are the values of the [[pre-excisive functor]] $X$ on the standard [[n-sphere]] $S^n = (S^1)^{\wedge n}$

$$
  (X^{seq})_n \coloneqq X(seq(n)) = X(S^n)
$$

and whose structure maps are the images of the action morphisms

$$
  \mathbb{S}_{seq} \otimes_{Day} X
    \longrightarrow
  X
$$

under the isomorphism of corollary \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}

$$
  \mathbb{S}_{seq}(n_1) \wedge X(n_1) \longrightarrow X_{n_1 + n_2}
$$

evaluated at $n_1 = 1$

$$
  \array{
    \mathbb{S}_{seq}(1) \wedge X(n)
      &\longrightarrow&
    X_{n+1}
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    S^1 \wedge X_n &\longrightarrow& X_{n+1}
  }
  \,.
$$



=--

([Hovey-Shipley-Smith 00, prop. 2.3.4](#HoveyShipleySmith00))

+-- {: .proof}
###### Proof

After unwinding the definitions, the only point to observe is that due to the action property,

$$
  \array{
    \mathbb{S}_{seq} \otimes_{Day} \mathbb{S}_{seq} \otimes_{Day} X
      &\overset{id \otimes_{Day} \rho}{\longrightarrow}&
    \mathbb{S}_{seq} \otimes_{Day} X
    \\
    {}^{\mathllap{\mu \otimes_{Day} id } }\downarrow
      &&
    \downarrow^{\mathrlap{\rho}}
    \\
    \mathbb{S}_{seq} \otimes_{Day} X
      &\underset{\rho}{\longrightarrow}&
    X
  }
$$

any $\mathbb{S}_{seq}$-action

$$
  \rho
  \;\colon\;
  \mathbb{S}_{seq} \otimes_{Day} X \longrightarrow X
$$

is indeed uniquely fixed by the components of the form

$$
  \mathbb{S}_{seq}(1) \wedge X(n) \longrightarrow X(n)
  \,.
$$

This is because under corollary \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor} the action property is identified with the componentwise property

$$
  \array{
    S^{n_1} \wedge S^{n_2} \wedge X_{n_3}
      &\overset{id \wedge \rho_{n_2,n_3}}{\longrightarrow}&
    S^{n_1} \wedge X_{n_2 + n_3}
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\rho_{n_1,n_2+n_3}}}
    \\
    S^{n_1 + n_2} \wedge X_{n_3}
     &\underset{\rho_{n_1+n_2,n_3}}{\longrightarrow}&
    X_{n_1 + n_2 + n_3}
  }
  \,,
$$

where the left vertical morphism is an isomorphism by the nature of $\mathbb{S}_{seq}$. Hence this fixes the components $\rho_{n',n}$ to be the $n'$-fold composition of the structure maps $\sigma_n \coloneqq \rho(1,n)$.

=--

However, since, by remark \ref{SseqModulesAreSequentialSpectra}, $\mathbb{S}_{seq}$ is not commutative, there is no tensor product induced on $SeqSpec(Top_{cg})$ under the identification in prop. \ref{SseqModulesAreSequentialSpectra}. But since $\mathbb{S}_{orth}$ and $\mathbb{S}_{sym}$ are commutative monoids by remark \ref{SseqModulesAreSequentialSpectra}, it makes sense to consider the following definition.


+-- {: .num_defn #SsymModuleSymmetricSpectra}
###### Definition

In the terminology of remark \ref{RestrictionsOfExcisiveSphere} we say that

$$
  OrthSpec(Top_{cg})
   \coloneqq
  \mathbb{S}_{orth} Mod
$$

is the **[[category]] of [[orthogonal spectra]]**; and that

$$
  SymSpec(Top_{cg})
   \coloneqq
  \mathbb{S}_{sym} Mod
$$

is the **[[category]] of [[symmetric spectra]]**.

By remark \ref{RestrictionsOfExcisiveSphere} and by prop. \ref{MonoidalCategoryOfModules} these categories canonically carry a [[symmetric monoidal category|symmetric monoidal]] [[tensor product]] $\otimes_{\mathbb{S}_{orth}}$ and $\otimes_{\mathbb{S}_{seq}}$, respectively. This we call the **[[symmetric monoidal smash product of spectra]]**. We usually just write for short

$$
  \wedge
    \coloneqq
  \otimes_{\mathbb{S}_{orth}}
  \;\colon\;
  OrthSpec(Top_{cg}) \times OrthSpec(Top_{cg})
   \longrightarrow
  OrthSpec(Top_{cg})
$$

and

$$
  \wedge
    \coloneqq
  \otimes_{\mathbb{S}_{sym}}
  \;\colon\;
  SymSpec(Top_{cg}) \times SymSpec(Top_{cg})
   \longrightarrow
  SymSpec(Top_{cg})
$$


=--

In the next section we work out what these symmetric monoidal categories of orthogonal and of symmetric spectra look like more explicitly.







### Symmetric and orthogonal spectra
 {#SymmetricSpectra}


We now define [[symmetric spectra]] and [[orthogonal spectra]] and their symmetric monoidal smash product. We proceed by giving the explicit definitions and then checking that these are equivalent to the abstract definition \ref{SsymModuleSymmetricSpectra} from above.

**Literature.** ( [Hovey-Shipley-Smith 00, section 1, section 2](#HoveyShipleySmith00), [Schwede 12, chapter I](#Schwede12))

$\,$

+-- {: .num_defn #SymmetricSpectrum}
###### Definition

A topological **[[symmetric spectrum]]** $X$  is

1. a sequence $\{X_n  \in Top_{cg}^{\ast/}\;\vert\; n \in \mathbb{N}\}$ of [[pointed topological space|pointed]] [[compactly generated topological spaces]];

1. a basepoint preserving continuous right [[action]] of the [[symmetric group]] $\Sigma(n)$ on $X_n$;

1. a sequence of morphisms  $\sigma_n \colon S^1 \wedge X_n  \longrightarrow X_{n+1}$

such that

* for all $n, k \in \mathbb{N}$ the [[composition|composite]]

  $$
    S^{k} \wedge X_n
     \simeq
    S^{k-1} \wedge S^1 \wedge X_n
      \stackrel{id \wedge \sigma_n }{\longrightarrow}
    S^{k-1} \wedge X_{n+1}
      \simeq
    S^{k-2}\wedge S^1 \wedge X_{n+2}
      \stackrel{id \wedge \sigma_{n+1}}{\longrightarrow}
    \cdots
    \stackrel{\sigma_{n+k-1}}{\longrightarrow} X_{n+k}
  $$

  [[intertwiner|intertwines]] the $\Sigma(n) \times \Sigma(k)$-[[action]].

A [[homomorphism]] of symmetric spectra $f\colon X \longrightarrow Y$ is

* a sequence of maps $f_n \colon X_n \longrightarrow Y_n$

such that

1. each $f_n$ [[intertwiner|intetwines]] the $\Sigma(n)$-[[action]];

1. the following [[commuting diagram|diagrams commute]]

   $$
     \array{
        S^1 \wedge X_n
          &\stackrel{f_n \wedge id}{\longrightarrow}&
        S^1 \wedge Y_n
        \\
        \downarrow^{\mathrlap{\sigma^X_n}} && \downarrow^{\mathrlap{\sigma^Y_n}}
        \\
        X_{n+1} &\stackrel{f_{n+1}}{\longrightarrow}& Y_{n+1}
     }
     \,.
   $$

We write $SymSpec(Top_{cg})$ for the resulting [[category]] of symmetric spectra.

=--

([Hovey-Shipley-Smith 00, def. 1.2.2](#HoveyShipleySmith00), [Schwede 12, I, def. 1.1](#Schwede12))

The definition of orthogonal spectra has the same structure, just with the  [[symmetric groups]] replaced by the [[orthogonal groups]].


+-- {: .num_defn #OrthogonalSpectrum}
###### Definition

A topological **[[orthogonal spectrum]]** $X$  is

1. a sequence $\{X_n  \in Top_{cg}^{\ast/}\;\vert\; n \in \mathbb{N}\}$ of [[pointed topological space|pointed]] [[compactly generated topological spaces]];

1. a basepoint preserving continuous right [[action]] of the [[orthogonal group]] $O(n)$ on $X_n$;

1. a sequence of morphisms  $\sigma_n \colon S^1 \wedge X_n  \longrightarrow X_{n+1}$

such that

* for all $n, k \in \mathbb{N}$ the [[composition|composite]]

  $$
    S^{k} \wedge X_n
     \simeq
    S^{k-1} \wedge S^1 \wedge X_n
      \stackrel{id \wedge \sigma_n }{\longrightarrow}
    S^{k-1} \wedge X_{n+1}
      \simeq
    S^{k-2}\wedge S^1 \wedge X_{n+2}
      \stackrel{id \wedge \sigma_{n+1}}{\longrightarrow}
    \cdots
    \stackrel{\sigma_{n+k-1}}{\longrightarrow} X_{n+k}
  $$

  [[intertwiner|intertwines]] the $O(n) \times O(k)$-[[action]].

A [[homomorphism]] of orthogonal spectra $f\colon X \longrightarrow Y$ is

* a sequence of maps $f_n \colon X_n \longrightarrow Y_n$

such that

1. each $f_n$ [[intertwiner|intetwines]] the $O(n)$-[[action]];

1. the following [[commuting diagram|diagrams commute]]

   $$
     \array{
        S^1 \wedge X_n
          &\stackrel{f_n \wedge id}{\longrightarrow}&
        S^1 \wedge Y_n
        \\
        \downarrow^{\mathrlap{\sigma^X_n}} && \downarrow^{\mathrlap{\sigma^Y_n}}
        \\
        X_{n+1} &\stackrel{f_{n+1}}{\longrightarrow}& Y_{n+1}
     }
     \,.
   $$

We write $OrthSpec(Top_{cg})$ for the resulting [[category]] of orthogonal spectra.

=--

(e.g. [Schwede 12, I, def. 7.2](#Schwede12))

+-- {: .num_prop #DiagramSpectraGiveSymmetricAndOrthogonalSpectra}
###### Proposition

Definitions \ref{SymmetricSpectrum} and \ref{OrthogonalSpectrum}
are indeed equivalent to def. \ref{SsymModuleSymmetricSpectra}:

orthogonal spectra are euqivalently the [[module objects]] over the incarnation $\mathbb{S}_{orth}$ of the sphere spectrum

$$
  OrthSpec(Top_{cg})
   \simeq
  \mathbb{S}_{orth} Mod
$$

and symmetric spectra sre equivalently the module objects over the incarnation $\mathbb{S}_{sym}$ of the sphere spectrum

$$
  SymSpec(Top_{cg})
   \simeq
  \mathbb{S}_{sym} Mod
  \,.
$$

=--

([Hovey-Shipley-Smith 00, prop. 2.2.1](#HoveyShipleySmith00))

+-- {: .proof}
###### Proof

We discuss this for symmetric spectra. The proof for orthogonal spectra is of the same form.

First of all, by example \ref{CoendGivesQuotientByDiagonalGroupAction} an object in $[Sym, Top^{\ast/}_{cg}]$ is equivalently a "symmetric sequence", namely a sequence of pointed topological spaces $X_k$, for $k \in \mathbb{N}$, equipped with an [[action]] of $\Sigma(k)$ (def. \ref{TopologicalDiagramCategoriesForSpectra}).

By corollary \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor} and lemma \ref{FSPStructuredSphereSpectra}, the structure morphism of an $\mathbb{S}_{sym}$-[[module object]] on $X$

$$
  \mathbb{S}_{sym} \otimes_{Day} X \longrightarrow X
$$

is equivalently (as a [[functor with smash products]]) a natural transformation

$$
  S^{n_1} \wedge X_{n_2} \longrightarrow X_{n_1 + n_2}
$$

over $Sym \times Sym$. This means equivalently that there is such a morphism for all $n_1, n_2 \in \mathbb{N}$ and that it is $\Sigma(n_1) \times \Sigma(n_2)$-equivariant.

Hence it only remains to see that these natural transformations are uniquely fixed once the one for $n_1 = 1$ is given. To that end, observe that lemma \ref{FSPStructuredSphereSpectra} says that in the following [[commuting squares]] (exhibiting the action property on the level of functors with smash product, where we are notationally suppressing the [[associators]]) the left vertical morphisms are [[isomorphisms]]:

$$
  \array{
    S^{n_1}\wedge S^{n_2} \wedge X_{n_3}
      &\longrightarrow&
    S^{n_1} \wedge X_{n_2 + n_3}
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow
    \\
    S^{n_1+ n_2} \wedge X_{n_3}
      &\longrightarrow&
    X_{n_1 + n_2 + n_3}
  }
  \,.
$$

This says exactly that the action of $S^{n_1 + n_2}$ has to be the composite of the actions of $S^{n_2}$ followed by that of $S^{n_1}$. Hence the statement follows by [[induction]].

Finally, the definition of [[homomorphisms]] on both sides of the equivalence are just so as to preserve precisely this structure, hence they conincide under this identification.

=--

+-- {: .num_defn #SmashProductOfSymmetricSpectra}
###### Definition

Given $X,Y \in SymSpec(Top_{cg})$ two [[symmetric spectra]], def. \ref{SymmetricSpectrum}, then their **[[smash product of spectra]]** is the symmetric spectrum

$$
  X \wedge Y
   \; \in SymSpec(Top_{cg})
$$

with component spaces the [[coequalizer]]

$$
  \underset{p+1+q = n}{\bigvee}
  \Sigma(p+1+q)_+
    \underset{\Sigma_p \times \Sigma_1 \times \Sigma_q}{\wedge}
  X_p \wedge S^1 \wedge Y_q
  \underoverset
   {\underset{r}{\longrightarrow}}
   {\overset{\ell}{\longrightarrow}}
   {\phantom{AAAA}}
  \underset{p+q=n}{\bigvee}
   \Sigma(p+q)_+
   \underset{\Sigma_p \times \Sigma_q}{\wedge}
   X_p \wedge Y_q
  \overset{coeq}{\longrightarrow}
  (X \wedge Y)(n)
$$

where $\ell$ has components given by the structure maps

$$
  X_p \wedge S^1 \wedge Y_q
    \overset{id \wedge \sigma_{q}}{\longrightarrow}
  X_p \wedge Y_q
$$

while $r$ has components given by the structure maps conjugated by the [[braiding]] in $Top^{\ast/}_{cg}$ and the [[permutation]] [[action]] $\chi_{p,1}$ (that [[shuffle|shuffles]] the element on the right to the left)

{#ShuffleActionInCoequalizerForSmashProductOfSpectra}
$$
  X_p \wedge S^1 \wedge X_q
    \overset{\tau^{Top^{\ast/}_{cg}}_{X_p,S^1} \wedge id}{\longrightarrow}
  S^1 \wedge X_p \wedge X_q
    \overset{\sigma_p\wedge id}{\longrightarrow}
  X_{p+1} \wedge X_q
    \overset{\chi_{p,1} \wedge id}{\longrightarrow}
  X_{1+p} \wedge X_q
  \,.
$$

Finally The structure maps of $X \wedge Y$ are those induced under the coequalizer by

$$
  S^1 \wedge (X_p \wedge Y_q \wedge)
  \simeq
  (S^1 \wedge X_p) \wedge Y_q
    \overset{\sigma^X_{p} \wedge id}{\longrightarrow}
  X_{p+1} \wedge Y_{q}
  \,.
$$

Analogously for orthogonal spectra.

=--

([Schwede 12, p. 82](#Schwede12))

+-- {: .num_prop #AbstractFormulaGivesSmashProductOfSymmetricSpectra}
###### Proposition

Under the identification of prop. \ref{DiagramSpectraGiveSymmetricAndOrthogonalSpectra}, the explicit [[smash product of spectra]] in def. \ref{SmashProductOfSymmetricSpectra} is equivalent to the abstractly defined tensor product in def. \ref{SsymModuleSymmetricSpectra}:

in the case of [[symmetric spectra]]:

$$
  \wedge \simeq \otimes_{\mathbb{S}_{sym}}
$$

in the case of [[orthogonal spectra]]:

$$
  \wedge \simeq \otimes_{\mathbb{S}_{orth}}
  \,.
$$

=--

([Schwede 12, E.1.16](#Schwede12))

+-- {: .proof}
###### Proof

By def. \ref{TensorProductOfModulesOverCommutativeMonoidObject} the abstractly defined tensor product of two $\mathbb{S}_{sym}$-modules $X$ and $Y$ is the [[coequalizer]]

$$
  X \otimes_{Day} \mathbb{S}_{sym} \otimes_{Day} Y
  \underoverset
    {\underset{\rho_{1}\circ (\tau^{Day}_{X, \mathbb{S}_{sym}} \otimes id)}{\longrightarrow}}
    {\overset{X \otimes \rho_2}{\longrightarrow}}
    {\phantom{AAAA}}
  X \otimes Y
    \overset{coeq}{\longrightarrow}
  X \otimes_{\mathbb{S}_{sym}} Y
  \,.
$$

The [[Day convolution]] product appearing here is over the category $Sym$ from def. \ref{TopologicalDiagramCategoriesForSpectra}. By example \ref{CoendGivesQuotientByDiagonalGroupAction} and unwinding the definitions, this is for any two symmetric spectra $A$ and $B$ given degreewise by the [[wedge sum]] of component spaces summing to that total degree, smashed with the symmetric group with basepoint adjoined and then quotiented by the diagonal action of the symmetric group acting on the degrees separately:

$$
  \begin{aligned}
    (A \otimes_{Day} B)(n)
    & =
    \overset{n_1,n_2}{\int}
     \underset{
      = \left\{
          \array{
             \Sigma(n_1 + n_2,n)_+ & if \; n_1+n_2 = n
             \\
             \ast_+ & otherwise
           }
      \right.
     }{
       \underbrace{
         \Sigma(n_1 + n_2, n)_+
       }
     }
      \wedge
     A_{n_1}
      \wedge
     B_{n_1}
    \\
    & \simeq
    \underset{n_1 + n_2 = n}{\bigvee}
     \Sigma(n_1+n_2)_+
     \underset{O(n_1) \times O(n_2) }{\wedge}
     \left(
       A_{n_1}
         \wedge
       B_{n_2}
     \right)
  \end{aligned}
  \,.
$$

This establishes the form of the coequalizer diagram. It remains to see that under this identification the two abstractly defined morphisms are the ones given in def. \ref{SmashProductOfSymmetricSpectra}.

To see this, we apply the adjunction isomorphism between the [[Day convolution product]] and the [[external tensor product]] (cor. \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}) twice, to find the following sequence of equivalent incarnations of morphisms:

$$
  \array{
  \arrayopts{\rowlines{solid}}
    (X \otimes_{Day} ( \mathbb{S}_{orth} \otimes_{Day} Y ))(n)
      &\longrightarrow&
    (X \otimes_{Day} Y)(n)
      &\longrightarrow&
    Z_n
    \\
    X_{n_1} \wedge (\mathbb{S}_{sym} \otimes_{Day} Y)(n'_2)
      &\longrightarrow&
    X_{n_1}\wedge Y(n'_2)
      &\longrightarrow&
    Z_{n_1 + n'_2}
    \\
    (\mathbb{S}_{sym} \otimes_{Day} Y)(n'_2)
      &\longrightarrow&
    Y(n'_2)
      &\longrightarrow&
    Maps(X_{n_1}, Z_{n_1 + n'_2})
    \\
    S^{n_2} \wedge Y_{n_3}
      &\longrightarrow&
    Y_{n_2 + n_3}
      &\longrightarrow&
    Maps(X_{n_1}, Z_{n_1 + n_2 + n_3})
    \\
    X_{n_1} \wedge S^{n_2} \wedge Y_{n_3}
      &\longrightarrow&
    X_{n_1} \wedge Y_{n_2 + n_3}
      &\longrightarrow&
    Z_{n_1 + n_2 + n_3}
  }
  \,.
$$

This establishes the form of the morphism $\ell$. By the same reasoning as in the proof of prop. \ref{DiagramSpectraGiveSymmetricAndOrthogonalSpectra}, we may restrict the coequalizer to $n_2 = 1$ without changing it.

The form of the morphism $r$ is obtained by the analogous sequence of identifications of morphisms, now with the parenthesis to the left. That it involves $\tau^{Top^{\ast/}_{cg}}$ and the permutation action $\tau^{sym}$ as shown [above](#ShuffleActionInCoequalizerForSmashProductOfSpectra) follows from the formula for the braiding of the Day convolution tensor product from the proof of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure}:


$$
  \tau^{Day}_{A,B}(n)
  =
  \overset{n_1,n_2}{\int}
   Sym( \tau^{Sym}_{n_1,n_2}, n )
    \wedge
   \tau^{Top^{\ast/}_{cg}}_{A_{n_1}, B_{n_2}}
$$

by translating it to the components of the precomposition

$$
  X \otimes_{Day} \mathbb{S}_{sym}
   \overset{\tau^{Day}_{X,\mathbb{S}_{sym}}}{\longrightarrow}
  \mathbb{S}_{sym} \otimes_{Day} X
  \overset{}{\longrightarrow}
  X
$$

via the formula from the proof of prop. \ref{TopologicalLeftKanExtensionBCoend} for the [[left Kan extension]] $A \otimes_{Day} B \simeq Lan_{\otimes} A \overline{\wedge} B$ (prop. \ref{DayConvolutionViaKanExtensionOfExternalTensorAlongTensor}):

$$
  \begin{aligned}
    [Sym, Top^{\ast/}_{cg}]( \tau^{Day}_{X,\mathbb{S}_{sym}}, X)
    &
    \simeq
    \underset{n}{\int}
    Maps(
      \overset{n_1, n_2}{\int}
      Sym( \tau^{sym}_{n_1,n_2}, n )
       \wedge
      \tau^{Top^{\ast/}_{cg}}_{X_{n_1}, S^{n_2}}
      ,
      X(n)
    )_\ast
    \\
    &
    \simeq
    \underset{n_1,n_2}{\int}
    Maps(
      \tau_{X_{n_1}, S^{n_2} }^{Top^{\ast/}_{cg}}
      ,
      X( \tau^{sym}_{n_1,n_2} )
    )_\ast
  \end{aligned}
  \,.
$$

This last expression is the function on morphisms which precomposes components under the coend with the braiding $\tau_{X_{n_1}, S^{n_2} }^{Top^{\ast/}_{cg}}$ in topological spaces and postcomposes them with the image of the functor $X$ of the braiding in $Sym$. But the braiding in $Sym$ is, by def. \ref{TopologicalDiagramCategoriesForSpectra}, given by the respective shuffle permutations $\tau^{sym}_{n_1,n_2} = \chi_{n_1,n_2}$, and by prop. \ref{DiagramSpectraGiveSymmetricAndOrthogonalSpectra} the image of these under $X$ is via the given $\Sigma_{n_1+n_2}$-action on $X_{n_1+n_2}$.

Finally to see that the structure map is as claimed: By prop. \ref{DiagramSpectraGiveSymmetricAndOrthogonalSpectra} the structure morphisms are the degree-1 components of the $\mathbb{S}_{sym}$-action, and by prop. \ref{TensorProductOfModulesOverCommutativeMonoidObject} the $\mathbb{S}_{sym}$-action on a tensor product of $\mathbb{S}_{sym}$-modules is induced via the action on the left tensor factor.


=--

+-- {: .num_defn #RingSpectrumInSymmetricAndOrthogonalSpectra}
###### Definition

A **commutative [[symmetric ring spectrum]]** $E$ is

1. a sequence of component spaces $E_n \in Top^{\ast/}_{cg}$ for $n \in \mathbb{N}$;

1. a basepoint preserving continuous left [[action]] of the [[symmetric group]] $\Sigma(n)$ on $E_n$;

1. for all $n_1,n_2\in \mathbb{N}$ a _multiplication map_

   $$
     \mu_{n_1,n_2}
       \;\colon\;
      E_{n_1} \wedge E_{n_2} \longrightarrow E_{n_1 + n_2}
   $$

   (a morphism in $Top^{\ast/}_{cg}$)

1. two _unit maps_

   $$
     \iota_0 \;\colon\; S^0 \longrightarrow E_0
   $$

   $$
     \iota_1 \;\colon\; S^1 \longrightarrow E_1
   $$

such that

1. (equivariance) $\mu_{n_1,n_2}$ [[intertwiner|intertwines]] the $\Sigma(n_1) \times \Sigma(n_2)$-action;

1. (associativity) for all $n_1, n_2, n_3 \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]] (where we are notationally suppressing the [[associators]] of $(Top^{\ast/}_{cg}, \wedge, S^0)$)

   $$
     \array{
       E_{n_1} \wedge E_{n_2} \wedge E_{n_3}
         &\overset{id \wedge \mu_{n_2,n_3}}{\longrightarrow}&
       E_{n_1} \wedge E_{n_2 + n_3}
       \\
       {}^{\mathllap{\mu_{n_1,n_2}\wedge id }}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{n_1, n_2 + n_3}}}
       \\
       E_{n_1 + n_2} \wedge E_{n_3}
         &\underset{\mu_{n_1 + n_2, n_3}}{\longrightarrow}&
       E_{n_1 + n_2 + n_3}
     }
     \,;
   $$

1. (unitality) for all $n \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       S^0 \wedge E_n
         &\overset{\iota_0 \wedge id}{\longrightarrow}&
       E_0 \wedge E_n
       \\
       &{}_{\mathllap{\ell^{Top^{\ast/}_{cg}}_{E_n}}}\searrow& \downarrow^{\mathrlap{\mu_{0,n}}}
       \\
       && E_n
     }
   $$

   and

   $$
     \array{
       E_n \wedge S^0
         &\overset{id \wedge \iota_0 }{\longrightarrow}&
       E_n \wedge E_0
       \\
       &{}_{\mathllap{r^{Top^{\ast/}_{cg}}_{E_n}}}\searrow& \downarrow^{\mathrlap{\mu_{n,0}}}
       \\
       && E_n
     }
     \,,
   $$

   where the diagonal morphisms $\ell$ and $r$ are the left and right [[unitors]] in $(Top^{\ast/}_{cg}, \wedge, S^0)$, respectively.

1. (commutativity) for all $n_1, n_2 \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       E_{n_1} \wedge E_{n_2}
         &\overset{\tau^{Top^{\ast/}_{cg}}_{E_{n_1}, E_{n_2}}}{\longrightarrow}&
       E_{n_2} \wedge E_{n_1}
       \\
       {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{n_2,n_1}}}
       \\
       E_{n_1 + n_2}
         &\underset{\chi_{n_1,n_2}}{\longrightarrow}&
       E_{n_2 + n_1}
     }
     \,,
   $$

   where the top morphism $\tau$ is the [[braiding]] in $(Top^{\ast/}_{cg}, \wedge, S^0)$ (def. \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}) and where  $\chi_{n_1,n_2} \in \Sigma(n_1 + n_2)$ denotes the [[permutation]] action which [[shuffle|shuffles]] the first $n_1$ elements past the last $n_2$ elements.

A [[homomorphism]] of symmetric commutative ring spectra $f \colon E \longrightarrow E'$ is a sequence $f_n \;\colon\; E_n \longrightarrow E'_n$ of $\Sigma(n)$-equivariant pointed continuous functions such that the following [[commuting diagram|diagrams commute]] for all $n_1, n_2 \in \mathbb{N}$

$$
  \array{
    E_{n_1} \wedge E_{n_2}
     &\overset{f_{n_1} \wedge f_{n_2}}{\longrightarrow}&
    E'_{n_1} \wedge E'_{n_2}
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow
      &&
    \downarrow^{\mu_{n_2,n_1}}
    \\
    E_{n_1 + n_2}
     &\underset{\chi_{n_1, n_2}}{\longrightarrow}&
    E_{n_2 + n_1}
  }
$$

and $f_0 \circ \iota_0 = \iota_0$ and $f_1\circ \iota_1 = \iota_1$.

Write

$$
  CRing(SymSpec(Top_{cg}))
$$

for the resulting [[category]] of symmetric [[commutative ring spectra]].

We regard a  symmetric ring spectrum in particular as a [[symmetric spectrum]] (def. \ref{SymmetricSpectrum}) by taking the structure maps to be

$$
  \sigma_n
    \;\colon\;
  S^1 \wedge E_n
    \overset{\iota_1 \wedge id}{\longrightarrow}
  E_1 \wedge E_n
    \overset{\mu_{1,n}}{\longrightarrow}
  E_{n+1}
  \,.
$$

This defines a [[forgetful functor]]

$$
  CRing(SymSpec(Top_{cg}))
   \longrightarrow
  SymSpec(Top_{cg})
$$

There is an analogous definition of **[[orthogonal ring spectrum]]** and we write

$$
  CRing(OrthSpec(Top_{cg}))
$$

for the category that these form.

=--

(e.g. [Schwede 12, def. 1.3](#Schwede12))

We discuss **examples** below in a dedicated section _[Examples](#Examples)_.


+-- {: .num_prop #RingSpectraAreDayMonoids}
###### Proposition

The symmetric (orthogonal) [[commutative ring spectra]] in def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra} are equivalently the [[commutative monoid in a symmetric monoidal category|commutative monoids in]] (def. \ref{MonoidsInMonoidalCategory}) the [[symmetric monoidal category]] $\mathbb{S}_{sym}Mod$ ($\mathbb{S}_{orth}Mod$) of def. \ref{SsymModuleSymmetricSpectra} with respect to the [[symmetric monoidal smash product of spectra]] $\wedge = \otimes_{\mathbb{S}_{sym}}$ ($\wedge = \otimes_{\mathbb{S}_{orth}}$). Hence there are [[equivalences of categories]]

$$
  CRing(SymSpec(Top_{cg}))
   \;\simeq\;
  CMon( \mathbb{S}_{sym}Mod, \otimes_{\mathbb{S}_{sym}}, \mathbb{S}_{sym} )
$$

and

$$
  CRing(OrthSpec(Top_{cg}))
   \;\simeq\;
  CMon( \mathbb{S}_{orth}Mod, \otimes_{\mathbb{S}_{orth}}, \mathbb{S}_{orth} )
  \,.
$$

Moreover, under these identifications the canonical forgetful functor

$$
  CMon( \mathbb{S}_{sym}Mod, \otimes_{\mathbb{S}_{sym}}, \mathbb{S}_{sym} )
    \longrightarrow
  SymSpec(Top_{cg})
$$

and

$$
  CMon( \mathbb{S}_{orth}Mod, \otimes_{\mathbb{S}_{orth}}, \mathbb{S}_{orth} )
    \longrightarrow
  OrthSpec(Top_{cg})
$$

coincides with the forgetful functor defined in def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}.


=--

+-- {: .proof}
###### Proof

We discuss this for symmetric spectra. The proof for orthogonal spectra is directly analogous.

By prop. \ref{AlgebrasOverAAreMonoidsUnderA} and def. \ref{SsymModuleSymmetricSpectra}, the commutative monoids in $\mathbb{S}_{sym}Mod$ are equivalently commtutative monoids $E$ in $([Sym,Top^{\ast/}_{cg}], \otimes_{Day}, y(0))$ equipped with a homomorphism of monoids $\mathbb{S}_{sym} \longrightarrow E$. In turn, by prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} this are equivalently braided lax monoidal functors (which we denote by the same symbols, for convenience) of the form

$$
  E \;\colon\; (Sym, +, 0) \longrightarrow (Top^{\ast/}_{cg}, \wedge, S^0)
$$

equipped with a [[monoidal natural transformation]] (def. \ref{LaxMonoidalFunctor})

$$
  \iota \;\colon\; \mathbb{S}_{sym} \longrightarrow E
  \,.
$$

The structure morphism of such a lax monoidal functor $E$ has as components precisely the morphisms $\mu_{n_1, n_2}\colon E_{n_1} \wedge E_{n_2} \to E_{n_1 + n_2}$.
In terms of these, the associativity and braiding condition on the lax monoidal functor are manifestly the above associativity and commutativity conditions.

Moreover, by the proof of prop. \ref{AlgebrasOverAAreMonoidsUnderA} the $\mathbb{S}_{sym}$-module structure on an an $\mathbb{S}_{sym}$-algebra $E$ has action given by

$$
  \mathbb{S}_{sym} \wedge E
    \overset{e \wedge id}{\longrightarrow}
  E \wedge E
   \overset{\mu}{\longrightarrow}
  E
  \,,
$$

which shows, via the identification in prop \ref{DiagramSpectraGiveSymmetricAndOrthogonalSpectra}, that the forgetful functors to underlying symmetric spectra coincide as claimed.


Hence it only remains to match the nature of the units. The above unit morphism $\iota$ has components

$$
  \iota_n \;\colon\; S^n \longrightarrow E_n
$$

for all $n \in \mathbb{N}$, and the unitality condition for $\iota_0$ and $\iota_1$ is manifestly as in the statement above.

We claim that the other components are uniquely fixed by these:

By lemma \ref{FSPStructuredSphereSpectra}, the product structure in $\mathbb{S}_{sym}$ is by isomorphisms $S^{n_1} \wedge S^{n_2} \simeq S^{n_1 + n_2}$, so that the commuting square for the coherence condition of this [[monoidal natural transformation]]

$$
  \array{
    S^{n_1} \wedge S^{n_2}
      &\overset{\iota_{n_1} \wedge \iota_{n_2}}{\longrightarrow}&
    E_{n_1} \wedge E_{n_2}
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_{n_1, n_2}}}
    \\
    S^{n_1 + n_2}
      &\underset{\iota_{n_1 + n_2}}{\longrightarrow}&
    E_{n_1 + n_2}
  }
$$

says that $\iota_{n_1 + n_2} = \mu_{n_1,n_2} \circ (\iota_{n_1} \wedge \iota_{n_2})$. This means that $\iota_{n \geq 2}$ is uniquely fixed once $\iota_0$ and $\iota_1$ are given.

Finally it is clear that homomorphisms on both sides of the equivalence precisely respect all this structure under both sides of the equivalence.

=--

Similarly:

+-- {: .num_defn #SymmetricModuleSpectrum}
###### Definition

Given a symmetric (orthogonal) [[commutative ring spectrum]] $E$ (def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}), then a left symmetric (orthogonal) **[[module spectrum]]** $N$ over $E$ is

1. a sequence of component spaces $N_n \in Top^{\ast/}_{cg}$ for $n \in \mathbb{N}$;

1. a basepoint preserving continuous left [[action]] of the [[symmetric group]] $\Sigma(n)$ on $N_n$;

1. for all $n_1,n_2\in \mathbb{N}$ an _action map_

   $$
     \rho_{n_1,n_2}
       \;\colon\;
      E_{n_1} \wedge N_{n_2} \longrightarrow N_{n_1 + n_2}
   $$

   (a morphism in $Top^{\ast/}_{cg}$)

such that

1. (equivariance) $\rho_{n_1,n_2}$ intertwines the $\Sigma(n_1) \times \Sigma(n_2)$-action;

1. (action property) for all $n_1, n_2, n_3 \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]] (where we are notationally suppressing the [[associators]] of $(Top^{\ast/}_{cg}, \wedge, S^0)$)

   $$
     \array{
       E_{n_1} \wedge E_{n_2} \wedge N_{n_3}
         &\overset{id \wedge \rho_{n_2,n_3}}{\longrightarrow}&
       E_{n_1} \wedge N_{n_2 + n_3}
       \\
       {}^{\mathllap{\mu_{n_1,n_2}\wedge id }}\downarrow
         &&
       \downarrow^{\mathrlap{\rho_{n_1, n_2 + n_3}}}
       \\
       E_{n_1 + n_2} \wedge N_{n_3}
         &\underset{\rho_{n_1 + n_2, n_3}}{\longrightarrow}&
       N_{n_1 + n_2 + n_3}
     }
     \,;
   $$

1. (unitality) for all $n \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       S^0 \wedge N_n
         &\overset{\iota_0 \wedge id}{\longrightarrow}&
       E_0 \wedge N_n
       \\
       &{}_{\mathllap{\ell^{Top^{\ast/}_{cg}}_{N_n}}}\searrow& \downarrow^{\mathrlap{\mu_{0,n}}}
       \\
       && N_n
     }
     \,.
   $$

A [[homomorphism]] of left $E$-module spectra $f\;\colon\; N \longrightarrow N'$ is a sequence of pointed continuous functions $f_n \;\colon\; N_n \longrightarrow N'_n$ such that for all $n_1,n_2 \in \mathbb{N}$ the following [[commuting diagram|diagrams commute]]:

$$
  \array{
    E_{n_1} \wedge N_{n_2}
     &\overset{id \wedge f_{n_2}}{\longrightarrow}&
    E_{n_1} \wedge N'_{n_2}
    \\
    {}^{\mathllap{\rho_{n_1,n_2}}}\downarrow
      &&
    \downarrow^{\rho_{n_1, n_2}}
    \\
    N_{n_1 + n_2}
      &\underset{f_{n_1 + n_2}}{\longrightarrow}&
    N'_{n_1 + n_2}
  }
  \,.
$$

We write

$$
  E Mod(SymSpec(Top_{cg}))
  \;\;\,,
  \;\;
  E Mod(OrthSpec(Top_{cg}))
$$

for the resulting category of symmetric (orthogonal) $E$-module spectra.

=--

(e.g. [Schwede 12, I, def. 1.5](#Schwede12))

+-- {: .num_prop #ModuleSpectraAreModuleFunctors}
###### Proposition

Under the identification, from prop. \ref{RingSpectraAreDayMonoids}, of [[commutative ring spectra]] with [[commutative monoids in a symmetric monoidal category|commutative monoids with respect to]] the [[symmetric monoidal smash product of spectra]], the $E$-[[module spectra]] of def. \ref{SymmetricModuleSpectrum} are equivalently the left [[module objects]] (def. \ref{ModulesInMonoidalCategory}) over the respective monoids, i.e. there are [[equivalences of categories]]

$$
  E Mod(SymSpec(Top_{cg}))
    \;\simeq\;
  E Mod( [Sym,Top^{\ast/}_{cg}], \otimes_{Day}, y(0) )
$$

and

$$
  E Mod(OrthSpec(Top_{cg}))
    \;\simeq\;
  E Mod( [Orth, Top^{\ast/}_{cg}], \otimes_{Day}, y(0) )
  \,,
$$

where on the right we have the [[categories of modules]] from def. \ref{ModulesInMonoidalCategory}.

=--

+-- {: .proof}
###### Proof

The proof is directly analogous to that of prop. \ref{RingSpectraAreDayMonoids}.  Now prop. \ref{AlgebrasOverAAreMonoidsUnderA} and prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} give that the module objects in question are equivalently [[modules over a monoidal functor]] (def. \ref{ModuleOverAMonoidalFunctor}) and writing these out in components yields precisely the above structures and properties.

=--



### As diagram spectra

In _[[Introduction to Stable homotopy theory -- 1-1]]_ we obtained the strict/level [[model structure on topological sequential spectra]] by identifying the category $SeqSpec(Top_{cg})$ of [[sequential spectra]] with a category of [[topologically enriched functors]] with values in $Top^{\ast/}_{cg}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#SequentialSpectraAsDiagramSpectra)) and then invoking the general existence of the [[projective model structure on functors]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ProjectiveModelStructureOnTopologicalFunctors)).

Here we discuss the analogous construction for the more general structured spectra from [above](#SModules).


+-- {: .num_prop #ModulesForDayConvolutionAsEnrichedFunctors}
###### Proposition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ be a [[topologically enriched category|topologically enriched]] [[monoidal category]] (def. \ref{MonoidalCategory}), and let $A \in Mon([\mathcal{C},Top^{\ast/}_{cg}],\otimes_{Day}, y(1_{\mathcal{C}}))$ be a [[monoid in a monoidal category|monoid in]] (def. \ref{MonoidsInMonoidalCategory}) the pointed topological [[Day convolution]] monoidal category over $\mathcal{C}$ from prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure}.

Then the [[category of modules|category of left A-modules]] (def. \ref{ModulesInMonoidalCategory}) is a pointed topologically [[enriched functor category]] category ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctorsToTopk))

$$
  A Mod
  \;\simeq\;
  [ A Free_{\mathcal{C}}Mod^{op}, \; Top_{cg}^{\ast/} ]
  \,,
$$

over the category of [[free modules]] over $A$ (prop. \ref{MonoidModuleOverItself}) on objects in $\mathcal{C}$ (under the [[Yoneda embedding]] $y \colon \mathcal{C}^{op} \to [\mathcal{C}, Top^{\ast/}_{cg}]$). Hence the objects of $A Free_{\mathcal{C}}Mod$ are identified with those of $\mathcal{C}$, and its [[hom-spaces]] are

$$
  A Free_{\mathcal{C}}Mod( c_1, c_2)
  \;=\;
  A Mod( A \otimes_{Day} y(c_1),\; A \otimes_{Day} y(c_2) )
  \,.
$$

=--

([MMSS 00, theorem 2.2](#MMSS00))


+-- {: .proof}
###### Proof


Use the identification from prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} of $A$ with a [[lax monoidal functor]] and of any $A$-[[module object]] $N$ as a functor with the structure of a [[module over a monoidal functor]], given by [[natural transformations]]

$$
  A(c_1)\otimes N(c_2) \overset{\rho_{c_1,c_2}}{\longrightarrow} N(c_1 \otimes c_2)
  \,.
$$

Notice that these transformations have just the same structure as those of the [[enriched functor|enriched functoriality]] of $N$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedFunctor)) of the form

$$
  \mathcal{C}(c_1,c_2) \otimes N(c_1) \overset{}{\longrightarrow} N(c_2)
  \,.
$$

Hence we may unify these two kinds of transformations into a single kind of the form

$$
   \mathcal{C}(c_3 \otimes c_1 , c_2)
        \otimes
      A(c_3)
      \otimes
    N(c_1)
      \overset{id \otimes \rho_{c_3,c_1}}{\longrightarrow}
    \mathcal{C}(c_3 \otimes c_1, c_2)
      \otimes
    N(c_3 \otimes c_2)
      \longrightarrow
    N(c_2)
$$

and subject to certain identifications.

Now observe that the hom-objects of $A Free_{\mathcal{C}}Mod$  have just this structure:

$$
  \begin{aligned}
    A Free_{\mathcal{C}}Mod(c_2,c_1)
      & =
    A Mod( A \otimes_{Day} y(c_2) , A \otimes_{Day} y(c_1) )
    \\
      & \simeq
    [\mathcal{C},Top^{\ast/}_{cg}](y(c_2), A \otimes_{Day} y(c_1) )
    \\
      & \simeq
    (A \otimes_{Day} y(c_1) )(c_2)
    \\
      & \simeq
     \overset{c_3,c_4}{\int}
       \mathcal{C}(c_3 \otimes c_4,c_2)
         \wedge
       A(c_3) \wedge \mathcal{C}(c_1, c_4)
     \\
     & \simeq
     \overset{c_3}{\int}
       \mathcal{C}(c_3 \otimes c_1, c_2)
       \wedge  A (c_3)
  \end{aligned}
  \,.
$$

Here we used first the [[free-forgetful adjunction]] of prop. \ref{MonoidModuleOverItself}, then the [[enriched Yoneda lemma]] (prop. \ref{YonedaReductionTopological}), then the [[coend]]-expression for [[Day convolution]] (def. \ref{TopologicalDayConvolutionProduct}) and finally the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}).

Then define a [[topologically enriched category]] $\mathcal{D}$ to have [[objects]] and [[hom-spaces]] those of $A Free_{\mathcal{C}}Mod^{op}$ as above, and whose [[composition]] operation is defined as follows:


$$
  \begin{aligned}
    \mathcal{D}(c_2,c3) \wedge \mathcal{D}(c_1,c_2)
    & \simeq
    \left(
    \overset{c_5}{\int}
      \mathcal{C}(c_5 \otimes_{\mathcal{C}} c_2 , c_3 )
      \wedge A(c_5)
    \right)
      \wedge
    \left(
    \overset{c_4}{\int}
       \mathcal{C}(c_4 \otimes_{\mathcal{C}} c_1, c_2)
       \wedge
       A(c_4)
    \right)
    \\
    & \simeq
    \overset{c_4, c_5}{\int}
      \mathcal{C}(c_5 \otimes_{\mathcal{C}} c_2 , c_3)
        \wedge
      \mathcal{C}(c_4 \otimes_{\mathcal{C}} c_1, c_2 )
        \wedge
      A(c_5) \wedge A(c_4)
    \\
    & \longrightarrow
      \overset{c_4,c_5}{\int}
      \mathcal{C}(c_5 \otimes_{\mathcal{C}} c_2 , c_3)
        \wedge
      \mathcal{C}(c_5 \otimes_{\mathcal{C}} c_4 \otimes_{\mathcal{C}} c_1, c_5 \otimes_{\mathcal{C}} c_2 )
        \wedge
       A(c_5  \otimes_{\mathcal{C}}  c_4   )
     \\
     & \longrightarrow
      \overset{c_4, c_5}{\int}
      \mathcal{C}(c_5 \otimes_{\mathcal{C}} c_4 \otimes_{\mathcal{C}} c_1, c_5 \otimes_{\mathcal{C}} c_2 )
        \wedge
       A(c_5  \otimes_{\mathcal{C}} c_4 )
     \\
     & \longrightarrow
      \overset{c_4}{\int}
      \mathcal{C}(c_4 \otimes_{\mathcal{C}} c_1  , c_3)
        \otimes_V
      A(c_4 )
  \end{aligned}
  \,,
$$

where

1. the equivalence is [[braiding]] in the integrand (and the [[Fubini theorem]], prop. \ref{CoendsCommuteWithEachOther});

1. the first morphism is, in the integrand, the smash product of

   1. forming the tensor product of hom-objects of $\mathcal{C}$ with the identity morphism on $c_5$;

   1. the monoidal functor incarnation $A(c_5) \wedge A(c_4)\longrightarrow A(c_5 \otimes_{\mathcal{C}} c_4 )$ of the monoid structure on $A$;

1. the second morphism is, in the integrand, given by composition in $\mathcal{C}$;

1. the last morphism is the morphism induced on [[coends]] by regarding [[extranatural transformation|extranaturality]] in $c_4$ and $c_5$ separately as a special case of extranaturality in $c_6 \coloneqq c_4 \otimes c_5$ (and then renaming).

With this it is fairly straightforward to see that

$$
  A Mod \simeq [\mathcal{D}, Top^{\ast/}_{cg}]
  \,,
$$

because, by the above definition of composition, functoriality over $\mathcal{D}$ manifestly encodes the $A$-[[action]] property together with the functoriality over $\mathcal{C}$.

This way we are reduced to showing that actually $\mathcal{D} \simeq A Free_{\mathcal{C}}Mod^{op}$.

But by construction, the image of the objects of $\mathcal{D}$ under the [[Yoneda embedding]] are precisely the free $A$-modules over objects of $\mathcal{C}$:


$$
  \mathcal{D}(c,-)
  \simeq
  A Free_{\mathcal{C}}Mod(-,c)
  \simeq
  (A \otimes_{Day} y(c))(-)
  \,.
$$

Since the [[Yoneda embedding]] is [[fully faithful functor|fully faithful]], this shows that indeed

$$
  \mathcal{D}^{op} \simeq A Free_{\mathcal{C}}Mod \hookrightarrow A Mod
  \,.
$$

=--





+-- {: .num_example #SequentialSpectraAsFunctorsOnFreeSSequModules}
###### Example

For the sequential case $Dia = Seq$ in def. \ref{TopologicalDiagramCategoriesForSpectra}, then the opposite category of [[free modules]] on objects in $Seq$ over $\mathbb{S}_{seq} $ ([def.](Introduction+to+stable+homotopy+theory+--+1-1#StandardRepresentativeOfTheSphereSpectrum)) is identified as the category $StdSpheres$ ([def.](Introduction+to+stable+homotopy+theory+--+1-1#CategoriesOfStandardSpheres)):


$$
  \mathbb{S}_{seq} Free_{seq}Mod^{op}
   \;\simeq\;
  StdSpheres
$$

Accordingly, in this case prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors} reduces to the identification ([prop.](Introduction+to+stable+homotopy+theory+--+1-1#SequentialSpectraAsDiagramSpectra)) of [[sequential spectra]] as topological diagrams over $StdSpheres$:

$$
  [ \mathbb{S}_{seq} Free_{seq}Mod^{op}, Top^{\ast/}_{cg} ]
    \simeq
  [StdSpheres, Top^{\ast/}_{cg}]
    \simeq
  SeqSpec(Top_{cg})
  \,.
$$


=--


+-- {: .proof}
###### Proof

There is one object $y(n)$ for each $n \in \mathbb{N}$. Moreover, from the expression in the proof of prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors} we compute the [[hom-spaces]] between these to be

$$
  \begin{aligned}
    \mathbb{S}_{seq} Free_{seq}Mod(
       \mathbb{S}_{seq} \otimes_{Day} y_{k_2}
       ,
       \mathbb{S}_{seq} \otimes_{Day} y_{k_1}
    )
    &
    \simeq
    \overset{n}{\int} Seq(n + k_1 , k_2) \wedge \mathbb{S}_{seq}(n)
    \\
    &
    \simeq
    \left\{
      \array{
        S^{k_2-k_1} & if \; k_2 \geq k_1
        \\
        \ast & otherwise
      }
    \right.
  \end{aligned}
  \,.
$$

These are the objects and hom-spaces of the category $StdSpheres$. It is straightforward to check that the definition of composition agrees, too.

=--






### Stable weak homotopy equivalences

We consider the evident version of [[stable weak homotopy equivalences]] for [[structured spectra]] and prove a few technical lemmas about them that are needed in the proof of the stable model structure [below](#MonoidalStableModelStructure.)

+-- {: .num_defn #StableOrthStructureClassesOfMorphisms}
###### Definition

For $Dia \in \{Top^{\ast/}_{cg,fin}, Orth, Sym, Seq\}$ one of the shapes of structured spectra from def. \ref{TopologicalDiagramCategoriesForSpectra}, let $\mathbb{S}_{dia}Mod$ be the corresponding category of structured spectra (def. \ref{FinitePointedCWComplexes}, prop. \ref{SseqModulesAreSequentialSpectra}, def. \ref{SsymModuleSymmetricSpectra}).

1. The [[stable homotopy groups]] of an object $X \in \mathbb{S}_{dia}Mod$ are those of the underlying sequential spectrum ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroups)):

   $$
     \pi_\bullet(X) \coloneqq \pi_\bullet(seq^\ast X)
     \,.
   $$

1. An object $X \in \mathbb{S}_{dia}Mod$ is a **structured [[Omega-spectrum]]** if the underlying [[sequential spectrum]] $seq^\ast X$ (def. \ref{TopologicalDiagramCategoriesForSpectra}) is a sequential [[Omega spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#OmegaSpectrum))

1. A morphism $f$ in $\mathbb{S}_{dia}Mod$ is a **[[stable weak homotopy equivalence]]** (or: **$\pi_\bullet$-isomorphism**) if the underlying morphism of [[sequential spectra]] $seq^\ast(f)$ is a [[stable weak homotopy equivalence]] of sequential spectra ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableWeakHomotopyEquivalenceOfSequentialTopologicalSpectra));

1. a morphism $f$ is a **stable cofibration** if it is a cofibration in the strict model structure $OrthSpec(Top_{cg})_{strict}$ from prop. \ref{StrictModelStructureOnDiagramSpectra}.

=--

([MMSS 00, def. 8.3 with the notation from p. 21](#MMSS00), [Mandell-May 02, III, def. 3.1, def. 3.2](#May02))


+-- {: .num_lemma #DegreewiseLESofHomotopyGroupsInducedStableLES}
###### Lemma

Given a morphism $f\;\colon\; X \longrightarrow Y$ in $\mathbb{S}_{dia}Mod$, then there are [[long exact sequences]] of [[stable homotopy groups]] (def. \ref{StableOrthStructureClassesOfMorphisms}) of the form

$$
  \cdots
   \longrightarrow
  \pi_{\bullet + 1}(Y)
    \overset{}{\longrightarrow}
  \pi_\bullet(Path_\ast(f))
    \overset{}{\longrightarrow}
  \pi_\bullet(X)
    \overset{f_\ast}{\longrightarrow}
  \pi_\bullet(Y)
    \longrightarrow
  \pi_{\bullet-1}(Path_\ast(f))
    \longrightarrow
  \cdots
$$

and

$$
  \cdots
   \longrightarrow
  \pi_{\bullet+1}(Y)
    \overset{}{\longrightarrow}
  \pi_{\bullet+1}(Cone(f))
    \overset{}{\longrightarrow}
  \pi_\bullet(X)
    \overset{f_\ast}{\longrightarrow}
  \pi_\bullet(Y)
    \longrightarrow
  \pi_{\bullet}(Cone(f))
    \longrightarrow
  \cdots
  \,,
$$

where $Cone(f)$ denotes the [[mapping cone]] and $Path_\ast(f)$ the [[mapping cocone]] of $f$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#MappingConeAndMappingCocone)) formed with respect to the standard [[cylinder spectrum]] $X \wedge (I_+)$ hence formed degreewise with respect to the standard [[reduced cylinder]] of pointed topological spaces.



=--

([MMSS 00, theorem 7.4 (vi) ](#MMSS00))

+-- {: .proof}
###### Proof

Since limits and colimits in the diagram category $\mathbb{S}_{dia}Mod$ are computed objectwise, the functor $seq^\ast$ that restricts $\mathbb{S}_{dia}$-modules to their underlying [[sequential spectra]] preserves both limits and colimits, hence it is sufficient to consider the statement for sequential spectra.

For the first case, there is degreewise the [[long exact sequence of homotopy groups]] to the left of pointed topological spaces ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#LongExactSequeceOfHomotopyGroups))

$$
  \cdots
   \to
  \pi_2(Y)
    \longrightarrow
  \pi_1(Path_\ast(f))
    \longrightarrow
  \pi_1(X)
   \overset{f_\ast}{\longrightarrow}
  \pi_1(Y)
   \longrightarrow
  \pi_0(Path_\ast(f))
    \longrightarrow
  \pi_0(X_n)
    \overset{f_\ast}{\longrightarrow}
  \pi_0(Y_n)
  \,.
$$

Observe that the [[sequential colimit]] that defines the [[stable homotopy groups]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroups)) preserves [[exact sequences]] of [[abelian groups]], because generally [[filtered colimits]] in [[Ab]] are [[exact functors]] ([prop.](Mod#FilteredColimitsInRModAreExact)). This implies that by taking the colimit over $n$ in the above sequences, we obtain a long exact sequence of stable homotopy groups as shown.

Now use that in sequential spectra the canonical morphism morphism $Path_\ast(f) \longrightarrow \Omega Cone(f)$ is a stable weak homotopy equivalence and is compatible with the map $f$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra)) so that there is a commuting diagram of the form

$$
  \array{
    \cdots
      &\longrightarrow&
    \pi_{\bullet + 1}(Y)
      &\overset{}{\longrightarrow}&
    \pi_\bullet(Path_\ast(f))
      &\overset{}{\longrightarrow}&
    \pi_\bullet(X)
      &\overset{f_\ast}{\longrightarrow}&
    \pi_\bullet(Y)
      &\longrightarrow&
    \pi_{\bullet-1}(Path_\ast(f))
      &\longrightarrow&
    \cdots
    \\
      &&
    \downarrow^{\mathrlap{=}}
      &&
    \downarrow^{\mathrlap{\simeq}}
      &&
    \downarrow^{\mathrlap{=}}
      &&
    \downarrow^{\mathrlap{=}}
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \cdots
      &\longrightarrow&
    \pi_{\bullet + 1}(Y)
      &\overset{}{\longrightarrow}&
    \pi_{\bullet+1}(Cone(f))
      &\overset{}{\longrightarrow}&
    \pi_\bullet(X)
      &\overset{f_\ast}{\longrightarrow}&
    \pi_\bullet(Y)
      &\longrightarrow&
    \pi_{\bullet}(Cone(f))
      &\longrightarrow&
    \cdots
  }
  \,.
$$

Since the top sequence is exact, and since all vertical morphisms are isomorphisms, it follows that also the bottom sequence is exact.


=--

+-- {: .num_lemma #SmashTensoringWithFiniteCellComplexPreservesSWHE}
###### Lemma

For $K \in Top^{\ast/}_{cg,fin}$ a [[CW-complex]]  then the operation of smash tensoring $(-) \wedge K$ preserves [[stable weak homotopy equivalences]] in $\mathbb{S}_{dia}Mod$.

=--

+-- {: .proof}
###### Proof

Since limits and colimits in the diagram category $\mathbb{S}_{dia}Mod$ are computed objectwise, the functor $seq^\ast$ that restricts $\mathbb{S}_{dia}$-modules to their underlying [[sequential spectra]] preserves both limits and colimits, and it also preserves smash tensoring. Hence it is sufficient to consider the statement for sequential spectra.

Fist consider the case of a finite cell complex $K$.


Write

$$
  \ast = K_0 \hookrightarrow \cdots \hookrightarrow K_i \hookrightarrow K_{i+1} \hookrightarrow \cdots \hookrightarrow K
$$

for the stages of the [[cell complex]] $K$, so that for each $i$ there is a [[pushout]] diagram in $Top^{}_{cg}$ of the form

$$
  \array{
    S^{n_i-1} &\longrightarrow& K_i &\longrightarrow& \ast
    \\
    {}^{\mathllap{}}\downarrow &(po)& \downarrow &(po)& \downarrow
    \\
    D^{n_i-1} &\longrightarrow& K_{i+1} &\longrightarrow& S^{n_i}
  }
  \,.
$$

Equivalently these are pushoutdiagrams in $Top^{\ast/}_{cg}$ of the form

$$
  \array{
    S^{n_i-1}_+ &\longrightarrow& K_i &\longrightarrow& \ast
    \\
    {}^{\mathllap{}}\downarrow &(po)& \downarrow &(po)& \downarrow
    \\
    D^{n_i-1}_+ &\longrightarrow& K_{i+1} &\longrightarrow& S^{n_i}
  }
  \,.
$$

Notice that it is indeed $S^{n_i}$ that appears in the top right, not $S^{n_i}_+$.

Now forming the smash [[tensoring]] of any morphism $f\colon X \longrightarrow Y$ in $\mathbb{S}_{dia}Mod(Top_{cg})$ by the morphisms in the pushout on the right yields a commuting diagram in $\mathbb{S}_{dia}Mod$ of the form

$$
  \array{
    X \wedge K_i
      &\longrightarrow&
    X \wedge K_{i+1}
     &\longrightarrow&
    X \wedge S^{n_i}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Y \wedge K_i
      &\longrightarrow&
    Y \wedge K_{i+1}
     &\longrightarrow&
    Y \wedge S^{n_i}
  }
  \,.
$$

Here the horizontal morphisms on the left are degreewise cofibrations in $Top^{\ast/}_{cg}$, hence the morphism on the right is degreewise their homotopy cofiber. This way lemma \ref{DegreewiseLESofHomotopyGroupsInducedStableLES} implies that there are commuting diagrams

$$
  \array{
    \pi_{\bullet+1}(X \wedge S^{n_i})
      &\longrightarrow&
    \pi_\bullet(X \wedge K_i)
      &\longrightarrow&
    \pi_\bullet(X \wedge K_{i+1})
      &\longrightarrow&
    \pi_\bullet(X \wedge S^{n_i})
      &\longrightarrow&
    \pi_{\bullet-1}(X \wedge K_i)
    \\
    \downarrow &&
    \downarrow && \downarrow^{\mathrlap{f \wedge K_{i+1}}} && \downarrow
    && \downarrow
    \\
    \pi_{\bullet+1}(Y \wedge S^{n_i})
      &\longrightarrow&
    \pi_\bullet(Y \wedge K_i)
      &\longrightarrow&
    \pi_\bullet(Y \wedge K_{i+1})
     &\longrightarrow&
    \pi_\bullet(Y \wedge S^{n_i})
      &\longrightarrow&
    \pi_{\bullet-1}(X \wedge K_i)
  }
  \,,
$$

where the top and bottom are [[long exact sequences]] of [[stable homotopy groups]].

Now proceed by [[induction]]. For $i = 0$ then clearly smash tensoring with $K_0 = \ast$ preserves stable weak homotopy equivalences. So assume that smash tensoring with $K_i$ does, too. Observe that $(-)\wedge S^n$ preserves stable weak homotopy equivalences, since $\Sigma X[1]\to X$ is a stable weak homotopy equivalence ([lemma](Introduction+to+Stable+homotopy+theory+
--+1-1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra)). Hence in the above the two vertical morphisms on the left and the two on the right are isomorphism. Now the [[five lemma]] implies that also $f \wedge K_{i+1}$ is an isomorphism.

Finally, the statement for a non-finite cell complex follows with these arguments and then using that spheres are [[compact topological spaces|compact]] and hence maps out of them into a [[transfinite composition]] factor through some finite stage ([prop.](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)).

=--

+-- {: .num_lemma #PushoutOfSWHEAlongDegreewiseCofibration}
###### Lemma

The pushout in $\mathbb{S}_{dia}Mod$ of a [[stable weak homotopy equivalence]] along a morphism that is degreewise a cofibration in $(Top^{\ast/}_{cg})_{Quillen}$ is again a stable weak homotopy equivalence.

=--

+-- {: .proof}
###### Proof

Given a pushout square

$$
  \array{
     X &\overset{g}{\longrightarrow}& Z
     \\
     {}^{\mathllap{f}}\downarrow &(po)& \downarrow
     \\
     Y &\underset{}{\longrightarrow}& Y \underset{X}{\sqcup}Z
  }
$$

observe that the [[pasting law]] implies an isomorphism between the horizontal [[cofibers]]

$$
  \array{
     X &\overset{g}{\longrightarrow}& Z &\longrightarrow& cofib(g)
     \\
     {}^{\mathllap{f}}\downarrow &(po)& \downarrow && \downarrow^{\mathrlap{\simeq}}
     \\
     Y &\underset{}{\longrightarrow}& Y \underset{X}{\sqcup}Z &\longrightarrow& cofib(g)
  }
  \,.
$$

Moreover, since cofibrations in $(Top^{\ast/}_{cg})_{Quillen}$ are preserves by pushout, and since pushout of spectra are computed degreewise, both the top and the bottom horizontal sequences here are degreewise homotopy cofiber sequence in $(Top^{\ast/}_{cg})_{Quillen}$.  Hence lemma \ref{DegreewiseLESofHomotopyGroupsInducedStableLES} applies and gives a commuting diagram

$$
  \array{
     \pi_{\bullet+1}(cofib(g))
      &\longrightarrow&
     \pi_\bullet(X)
       &\overset{}{\longrightarrow}&
     \pi_\bullet(Z)
       &\longrightarrow&
     \pi_\bullet(cofib(g))
       &\longrightarrow&
     \pi_{\bullet-1}(X)
     \\
     \downarrow^{\mathrlap{\simeq}}
       &&
     {}^{\mathllap{\pi_\bullet(f)}}_{\mathllap{\simeq}}\downarrow
       &&
     \downarrow
       &&
     \downarrow^{\mathrlap{\simeq}}
       &&
     \downarrow^{\mathrlap{\simeq}}
     \\
     \pi_{\bullet+1}(cofib(g))
      &\longrightarrow&
     \pi_\bullet(Y)
       &\underset{}{\longrightarrow}&
     \pi_\bullet(Y \underset{X}{\sqcup}Z)
       &\longrightarrow&
     \pi_\bullet(cofib(g))
       &\longrightarrow&
     \pi_{\bullet-1}(Y)
  }
  \,,
$$

where the top and the bottom row are both [[long exact sequences]] of [[stable homotopy groups]]. Hence the claim now follows by the [[five lemma]].

=--





### Free spectra and Suspension spectra
 {#FreeSpectra}

The concept of _[[free spectrum]]_ is a generalization of that of _[[suspension spectrum]]_. In fact the [[stable homotopy types]] of free spectra are precisely those of iterated [[loop space objects]] of [[suspension spectra]]. But for the development of the theory what matters is free spectra before passing to stable homotopy types, for as such they play the role of the basic cells for the stable [[model structures on spectra]] analogous to the role of the [[n-spheres]] in the [[classical model structure on topological spaces]] (def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} below).

Moreover, while free [[sequential spectra]] are just re-indexed [[suspension spectra]], free [[symmetric spectra]] and free [[orthogonal spectra]] in addition come with suitably freely generated [[actions]] of the [[symmetric group]] and the [[orthogonal group]]. It turns out that this is not entirely trivial; it leads to a subtle issue (lemma \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences} below) where the [[adjuncts]] of certain canonical inclusions of free spectra are [[stable weak homotopy equivalences]] for sequential and orthogonal spectra, but _not_ for symmetric spectra.

+-- {: .num_defn #FreeStructuredSpectrum}
###### Definition

For $Dia \in \{Top^{\ast/}_{fin}, Orth, Sym, Seq\}$ any one of the four diagram shapes of def. \ref{TopologicalDiagramCategoriesForSpectra}, and for each $n \in \mathbb{N}$, the functor

$$
  (-)_n
  \;\colon\;
  \mathbb{S}_{dia}Mod
    \overset{seq^\ast}{\longrightarrow} \mathbb{S}_{seq}Mod
  \simeq
    SeqSpec(Top_{cg}) \stackrel{(-)_n}{\longrightarrow} Top^{\ast/}_{cg}
$$

that sends a [[structured spectrum]] to the $n$th component space of its underlying [[sequential spectrum]] has, by prop. \ref{TopologicalLeftKanExtensionBCoend}, a [[left adjoint]]

$$
  F^{dia}_n \;\colon\; Top^{\ast/} \longrightarrow \mathbb{S}_{dia}Mod
  \,.
$$

This is called the **[[free structured spectrum]]**-functor.

For the special case $n = 0$ it is also called the **structured [[suspension spectrum]]** functor and denoted

$$
  \Sigma^\infty_{dia} K
    \;\coloneqq\;
  F^{dia}_0 K
$$

=--

([Hovey-Shipley-Smith 00, def. 2.2.5](#HoveyShipleySmith00), [MMSS 00, section 8](#MMSS00))

+-- {: .num_lemma #ExplicitExpressionForFreeSpectra}
###### Lemma

Let $Dia \in \{Top^{\ast/}_{fin}, Orth, Sym, Seq\}$ be any one of the four diagram shapes of def. \ref{TopologicalDiagramCategoriesForSpectra}. Then

1. the [[free spectrum]] on $K \in Top^{\ast/}_{cg}$ (def. \ref{FreeStructuredSpectrum}) is equivalently the smash [[tensoring]] with $K$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#TensoringAndPoweringOfTopologicallyEnrichedCopresheaves)) of the [[free module]] (def. \ref{MonoidModuleOverItself}) over $\mathbb{S}_{dia}$ (remark \ref{RestrictionsOfExcisiveSphere}) on the [[representable functor|representable]] $y(n) \in [Dia, Top^{\ast/}_{cg}]$

   $$
     \begin{aligned}
       F^{dia}_n K
         & \simeq
       (\mathbb{S}_{dia} \otimes_{Day} y(n)) \wedge K
       \\
       & \simeq \mathbb{S}_{dia} \otimes_{Day} (y(n) \wedge K)
     \end{aligned}
     \,;
   $$

1. on $n' \in Dia^{op} \stackrel{y}{\hookrightarrow} [Dia, Top^{\ast/}_{cg}]$ its value is given by the following [[coend]] expression (def. \ref{EndAndCoendInTopcgSmash})

  $$
    (F^{dia}_n K)(n')
      \;\simeq\;
    \overset{n_1 \in Dia}{\int}
      Dia(n_1 \otimes n, n') \wedge S^{n_1} \wedge K
    \,.
  $$

In particular the structured [[sphere spectrum]] is the free spectrum in degree 0 on the [[0-sphere]]:

$$
  \mathbb{S}_{dia}
  \simeq
  F_0^{dia} S^0
$$

and generally for $K \in Top^{\ast/}_{cg}$ then

$$
  F_0^{dia} K \simeq \mathbb{S}_{dia} \wedge K
$$

is the smash tensoring of the strutured sphere spectrum with $K$.

=--

([Hovey-Shipley-Smith 00, below def. 2.2.5](#HoveyShipleySmith00), [MMSS00, p. 7 with theorem 2.2](#MMSS00))


+-- {: .proof}
###### Proof

Under the [[equivalence of categories]]

$$
  \mathbb{S}_{dia} Mod \simeq [\mathbb{S}_{dia}Free_{dia}Mod^{op}, Top^{\ast/}_{cg}]
$$

from prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors}, the expression for $F^{dia}_n K$ is equivalently the smash tensoring with $K$ of the functor that $n$ represents over $\mathbb{S}_{dia}Free_{dia}Mod$:

$$
  \begin{aligned}
    F^{dia}_n K
      & \simeq
      y_{\mathbb{S}_{dia} Free_{Dia}Mod}(n) \wedge K
      \\
      & \simeq
      \mathbb{S}_{dia}Free_{dia}Mod( - , \mathbb{S}_{dia} \wedge y_{Dia}(n) ) \wedge K
  \end{aligned}
$$

(by [[full subcategory|fully faithfulness]] of the [[Yoneda embedding]]).

This way the first statement is a special case of the following general fact: For $\mathcal{C}$ a pointed [[topologically enriched category]], and for $c \in \mathcal{C}$ any [[object]], then there is an [[adjunction]]

$$
  [\mathcal{C}, Top^{\ast/}_{cg}]
    \underoverset
      {\underset{(-)_c}{\longrightarrow}}
      {\overset{y(c)\wedge(-)}{\longleftarrow}}
      {\bot}
  Top^{\ast/}_{cg}
$$

(saying that evaluation at $c$ is [[right adjoint]] to smash tensoring the functor represented by $c$) witnessed by the following composite [[natural isomorphism]]:

$$
  [\mathcal{C}, Top^{\ast/}_{cg}](y(c)\wedge K, F)
    \;\simeq\;
  Maps(K, [\mathcal{C}, Top^{\ast/}_{cg}](y(c),  F)  )_\ast
    \;\simeq\;
  Maps(K,F(c))_\ast
   \;=\;
  Top^{\ast/}_{cg}(K,F(c))
  \,.
$$

The first is the characteristic isomorphism of [[tensoring]] from prop. \ref{UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg}, while the second is the [[enriched Yoneda lemma]] of prop. \ref{YonedaReductionTopological}.

From this, the second statement follows by the proof of prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors}.

For the last statement it is sufficient to observe that $y(0)$ is the [[tensor unit]] under [[Day convolution]] by prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} (since $0$ is the tensor unit in $Dia$), so that

$$
  \begin{aligned}
    F_0^{dia} S^0
    & =
    \mathbb{S}_{dia} \otimes_{Day} (y(0) \wedge S^0)
    \\
    & \simeq
    \mathbb{S}_{dia} \otimes y(S^0)
    \\
    & \simeq
    \mathbb{S}_{dia}
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop #ExplicitFormOfFreeSpectra}
###### Proposition

Explicitly, the [[free spectra]] according to def. \ref{FreeStructuredSpectrum}, look as follows:

For [[sequential spectra]]:

$$
  (F^{Seq}_n K)_q
    \simeq
   \left\{
     \array{
       S^{q-n} \wedge K & if \; q \geq n
       \\
       \ast & \otherwise
     }
   \right\}
$$

for [[symmetric spectra]]:

$$
  (F^{Sym}_n K)_q
    \simeq
  \left\{
    \array{
      \Sigma(q)_+ \wedge_{\Sigma(q-n)} S^{q-n} \wedge K & if\; q \geq n
      \\
      \ast & otherwise
    }
  \right.
$$

for [[orthogonal spectra]]:

$$
  (F^{Orth}_n K)_q
    \simeq
  \left\{
    \array{
       O(q)_+ \wedge_{O(q-n)} \wedge S^{q-n} \wedge K & if \; q \geq n
       \\
       \ast & otherwise
    }
  \right.
  \,,
$$

where "$\wedge_G$" is as in example \ref{CoendGivesQuotientByDiagonalGroupAction}.


=--

(e.g. [Schwede 12, example 3.20](#Schwede12))

+-- {: .proof}
###### Proof

With the formula in item 2 of lemma \ref{ExplicitExpressionForFreeSpectra} we have for the case of [[orthogonal spectra]]

$$
  \begin{aligned}
    (F_n^{Orth} K)(\mathbb{R}^q)
    & \simeq
    \overset{n_1 \in Orth}{\int}
     \underset{= \left\{ \array{ O(q)_+ & if \, n_1+n = q \\ \ast & otherwise} \right.}{\underbrace{Orth(n_1 + n,q)}}
       \wedge
     S^{n_1}
       \wedge
     K
    \\
    & \simeq
    \left\{
      \array{
        \overset{n_1 = \ast \in \mathbf{B}(O(q-n))}{\int}
          O(q)_+ \underset{O(q-n)}{\wedge} S^{q-n} \wedge K
        & if \; q \geq n
        \\
        \ast & otherwise
      }
    \right.
  \end{aligned}
  \,,
$$

where in the second line we used that the [[coend]] collapses to $n_1 = q-n$ ranging in the full subcategory

$$
  \mathbf{B}(O(q-n)_+) \hookrightarrow Orth
$$

on the object $\mathbb{R}^{q-n}$ and then we applied example \ref{CoendGivesQuotientByDiagonalGroupAction}. The case of symmetric spectra is verbatim the same, with the symmetric group replacing the orthogonal group, and the case of sequential spectra is again verbatim the same, with the orthogonal group replaced by the trivial group.

=--

+-- {: .num_lemma #S0FreeSpectraCellDegreewise}
###### Lemma

For $Dia \in \{ Orth, Sym, Seq\}$ the diagram shape for [[orthogonal spectra]], [[symmetric spectra]] or [[sequential spectra]], then the [[free structured spectra]]

$$
  F^{dia}_n S^0
  \in
  \mathbb{S}_{dia}Mod
$$

from def. \ref{FreeStructuredSpectrum} have component spaces that admit the structure of [[CW-complexes]].

=--

+-- {: .proof}
###### Proof

We consider the case of [[orthogonal spectra]]. The case of [[symmetric spectra]] works verbatim the same, and the case of [[sequential spectra]] is tivial.

By prop. \ref{ExplicitFormOfFreeSpectra} we have to show that for all $q \geq n \in \mathbb{N}$ the topological spaces of the form

$$
  O(q)_+ \wedge_{O(q-n)} S^{q-n}
  \;\;
  \in Top^{\ast/}_{cg}
$$

admit the structure of CW-complexes.

To that end, use the [[homeomorphism]]

$$
  S^{q-n} \simeq D^{q-n}/\partial D^{q-n}
$$

which is a [[diffeomorphism]] away from the basepoint and hence such that the action of the [[orthogonal group]] $O(q-n)$ induces a smooth action on $D^{q-n}$ (which happens to be constant on $\partial D^{q-n}$).

Also observe that we may think of the above quotient by the group action

$$
  (x, g y) \simeq (x g , y)
$$

as being the quotient by the diagonal action

$$
  O(q-n) \times ( O(q)_+ \wedge S^{q-n} )
    \longrightarrow
  (O(q)_+ \wedge S^{q-n})
$$

given by

$$
  (g, (x,y)) \mapsto (x g^{-1}, g y)
  \,.
$$

Using this we may rewrite the space in question as

$$
  \begin{aligned}
    (O(q)_+ \wedge_{O(q-n)} S^{q-n} )
    &
    \simeq
    ( O(q)_+ \wedge S^{q-n} )/ O(q-n)
    \\
    &\simeq
    \frac{ O(q) \times D^{q-n} }{ O(q) \times \partial D^{q-n} } / O(q-n)
    \\
    & \simeq
    \frac{ O(q) \times D^{q-n} }{ \partial( O(q) \times D^{q-n} ) } / O(q-n)
    \\
    & \simeq
    \frac{
      (O(q) \times D^{q-n})/ O(q-n)
    }{
      (\partial(O(q)\times D^{q-n}))/O(q-n)
    }
  \end{aligned}
  \,.
$$

Here $O(q)\times D^{q-n}$ has the structure of a [[smooth manifold]] [[manifold with boundary|with boundary]] and equipped with a smooth [[action]] of the [[compact Lie group]] $O(q-n)$. Under these conditions ([Illman 83, corollary 7.2](G-CW+complex#Illman83)) states that $O(q) \times D^{q-n}$ admits the structure of a [[G-CW complex]] for $G = O(q-n)$, and moreover ([Illman 83, line above theorem 7.1](G-CW+complex#Illman83)) states that this may be chosen such that the boundary is a $G$-CW subcomplex.

Now the quotient of a $G$-CW complex by $G$ is a [[CW complex]], and so the last expression above exhibits the quotient of a CW-complex by a subcomplex, hence exhibits CW-complex structure.


=--

+-- {: .num_prop #SmashProductOfFreeSpectra}
###### Proposition
**([[structured spectrum|structured]] [[suspension spectrum]]-construction is [[strong monoidal functor]])**

Let $Dia \in \{Top^{\ast/}_{cg,fin}, Orth, Sym\}$ be the diagram shape of either [[pre-excisive functors]], [[orthogonal spectra]] or [[symmetric spectra]]. Then under the [[symmetric monoidal smash product of spectra]] (def. \ref{FinitePointedCWComplexes}, def. \ref{FinitePointedCWComplexes}, def.\ref{SsymModuleSymmetricSpectra}) the [[free structured spectra]] of def. \ref{FreeStructuredSpectrum} behave as follows

$$
  F^{dia}_{n_1}(K_1)
    \otimes_{\mathbb{S}_{dia}}
  F^{dia}_{n_2}(K_2)
   \;\simeq\;
  F_{n_1 + n_2}(K_1 \wedge K_2)
  \,.
$$

In particular for structured [[suspension spectra]] $\Sigma^\infty_{dia}\coloneqq F_0^{dia}$ (def. \ref{FreeStructuredSpectrum}) this gives isomorphisms

$$
  \Sigma^\infty_{dia}(K_1)
    \otimes_{\mathbb{S}_{dia}}
  \Sigma^\infty_{dia}(K_2)
    \;\simeq\;
  \Sigma^\infty_{dia}(K_1 \wedge K_2)
  \,.
$$

Hence the structured [[suspension spectrum]] functor $\Sigma^\infty_{dia}$ is a [[strong monoidal functor]] (def. \ref{LaxMonoidalFunctor}) and in fact a [[braided monoidal functor]] (def. \ref{LaxMonoidalFunctor}) from [[pointed topological spaces]] equipped with the [[smash product]] of pointed objects, to [[structured spectra]] equipped with the [[symmetric monoidal smash product of spectra]]

$$
  \Sigma_{dia}^\infty
   \;\colon\;
  (Top^{\ast/}_{cg},\wedge, S^0)
    \longrightarrow
  ( \mathbb{S}_{dia}Mod, \otimes_{\mathbb{S}_{dia}}, \mathbb{S}_{dia} )
  \,.
$$

More generally, for $X \in \mathbb{S}_{dia}Mod$ then

$$
  X \otimes_{\mathbb{S}_{dia}} ( \Sigma^\infty_{dia} K )
  \simeq
  X \wedge K
  \,,
$$

where on the right we have the smash tensoring of $X$ with $K \in Top^{\ast/}_{cg}$.

=--

([MMSS 00, lemma 1.8 with theorem 2.2](#MMSS00), [Mandell-May 02, prop. 2.2.6](#May02))

+-- {: .proof}
###### Proof

By lemma \ref{ExplicitExpressionForFreeSpectra} the free spectra are [[free modules]] over the structured [[sphere spectrum]] $\mathbb{S}_{dia}$ of the form
$F^{dia}_n(K) \simeq \mathbb{S}_{dia} \otimes_{Day} ( y(n) \wedge K )$. By example \ref{FreeModulesTensorProduct} the tensor product of such free modules is given by

$$
  \left(
    \mathbb{S}_{dia} \otimes_{Day} (y(n_1) \wedge K_1)
  \right)
   \otimes_{Day}
  \left(
    \mathbb{S}_{dia} \otimes_{Day} ( y(n_2) \wedge K_2 )
  \right)
    \;\simeq\;
  \mathbb{S}_{dia}
   \otimes_{Day}
  ( y(n_1) \wedge K ) \otimes_{Day} ( y(n_2) \wedge K )
  \,.
$$

Using the [[co-Yoneda lemma]] (prop. \ref{TopologicalCoYonedaLemma}) the expression on the right is

$$
  \begin{aligned}
    \left(
      (y(n_1) \wedge K_1)
        \otimes_{Day}
      (y(n_2) \wedge K_2)
    \right)(c)
    & =
    \overset{c_1,_2}{\int}
      Dia(c_1 + c_2, c)
        \wedge
      y(n_1)(c_1) \wedge K_1
       \wedge
      y(n_2)(c_2) \wedge K_2
    \\
    & \simeq
    \overset{c_1,c_2}{\int}
     Dia(c_1 + c_2, c)
     \wedge
     Dia(n_1,c_1)
     \wedge
     Dia(n_2,c_2)
     \wedge K_1 \wedge K_2
     \\
       & \simeq
     Dia(n_1 + n_2,c) \wedge K_1 \wedge K_2
     \\
       & \simeq
     \left(y(n_1 + n_2) \wedge (K_1 \wedge K_2)\right)(c)
  \end{aligned}
  \,.
$$

For the last statement we may use that $\Sigma^\infty_{dia} K \simeq \mathbb{S}_{dia} \wedge K$, by lemma \ref{ExplicitExpressionForFreeSpectra}), and that $\mathbb{S}_{dia}$ is the [[tensor unit]] for $\otimes_{\mathbb{S}_{dia}}$ by prop. \ref{MonoidalCategoryOfModules}.

To see that $\Sigma^\infty_{dia}$ is braided, write $\Sigma^\infty_{dia}K\simeq \mathbb{S} \wedge K$. We need to see that

$$
  \array{
    (\mathbb{S} \wedge K_1)
      \otimes_{\mathbb{S}}
    (\mathbb{S} \wedge K_2)
    &\overset{}{\longrightarrow}&
    (\mathbb{S} \wedge K_2)
      \otimes_{\mathbb{S}}
    (\mathbb{S} \wedge K_1)
    \\
    \downarrow
      &&
    \downarrow
    \\
    \mathbb{S} \wedge (K_1 \wedge K_2)
      &\underset{}{\longrightarrow}&
    \mathbb{S} \wedge (K_2 \wedge K_1)
  }
$$

commutes. Chasing the smash factors through this diagram and using symmetry (def. \ref{SymmetricMonoidalCategory}) and the hexagon identities (def. \ref{BraidedMonoidalCategory}) shows that indeed it does.

=--

One use of free spectra is that they serve to co-represent adjuncts of structure morphisms of spectra. To this end, first consider the following general existence statement.

+-- {: .num_lemma #CorepresentingOfAdjunctsOfStructureMapsExists}
###### Lemma

For each $n \in \mathbb{N}$ there exists a morphism

$$
  \lambda_n
    \;\colon\;
  F_{n+1}^{dia}S^1
    \longrightarrow
  F_n^{dia} S^0
$$

between [[free spectra]] (def. \ref{FreeStructuredSpectrum}) such that for every structured spectrum $X\in \mathbb{S}_{dia} Mod$ precomposition $\lambda_n^\ast$ forms a [[commuting diagram]] of the form

$$
  \array{
    \mathbb{S}_{dia}Mod(F^{dia}_n S^0, X) &\simeq& Top^{\ast/}(S^0,X_n) &\simeq& X_n
    \\
    \downarrow^{\mathrlap{\lambda_n^\ast}}
    && &&
    \downarrow^{\mathrlap{\tilde \sigma^X_n}}
    \\
    \mathbb{S}_{dia}Mod(F^{dia}_{n+1} S^1, X)
    &\simeq&
    Top^{\ast/}(S^1, X_{n+1})
    &\simeq&
    \Omega X_{n+1}
  }
  \,,
$$

where the horizontal equivalences are the [[adjunction]] isomorphisms and the canonical identification, and where the right morphism is the $(\Sigma \dashv \Omega)$-[[adjunct]] of the structure map $\sigma_n$ of the [[sequential spectrum]] $seq^\ast X$ underlying $X$ (def. \ref{TopologicalDiagramCategoriesForSpectra}).

=--

+-- {: .proof}
###### Proof

Since all prescribed morphisms in the diagram are [[natural transformations]], this is in fact a diagram of [[copresheaves]] on $\mathbb{S}_{dia} Mod$

$$
  \array{
    \mathbb{S}_{dia}Mod(F^{dia}_n S^0, -) &\simeq& Top^{\ast/}(S^0,(-)_n) &\simeq& (-)_n
    \\
    \downarrow^{\mathrlap{}}
    && &&
    \downarrow^{\mathrlap{\tilde \sigma^{(-)}_n}}
    \\
    \mathbb{S}_{dia}Mod(F^{dia}_{n+1} S^1, -)
    &\simeq&
    Top^{\ast/}(S^1, (-)_{n+1})
    &\simeq&
    \Omega (-)_{n+1}
  }
  \,.
$$

With this the statement follows by the [[Yoneda lemma]].

=--

Now we say explicitly what these maps are:

+-- {: .num_defn #CorepresentationOfAdjunctsOfStructureMaps}
###### Definition

For $n \in \mathbb{N}$, write

$$
  \lambda_n \;\colon\; F_{n+1} S^1 \longrightarrow F_n S^0
$$

for the [[adjunct]] under the ([[free structured spectrum]] $\dashv$ $n$-component)-[[adjunction]] in def. \ref{FreeStructuredSpectrum} of the composite morphism

$$
  S^1
    \stackrel{=}{\to}
  (F_n^{Seq}(S^0))_{n+1}
    \stackrel{(f_n^{Seq})_{n+1}}{\hookrightarrow}
  (F^{dia}_n S^0)_{n+1}
  \,,
$$

where the first morphism is via prop. \ref{ExplicitFormOfFreeSpectra} and the second comes from the adjunction units according to def. \ref{FreeStructuredSpectrum}.

=--

([MMSS 00, def. 8.4](#MMSS00), [Schwede 12, example 4.26](#Schwede12))

+-- {: .num_lemma #IndeedCorepresentationOfAdjunctsOfStructureMaps}
###### Lemma

The morphisms of def. \ref{CorepresentationOfAdjunctsOfStructureMaps} are those whose existence is asserted by prop. \ref{CorepresentingOfAdjunctsOfStructureMapsExists}.

=--

([MMSS 00, lemma 8.5](#MMSS00), following [Hovey-Shipley-Smith 00, remark 2.2.12](#HoveyShipleySmith00))


+-- {: .proof}
###### Proof

Consider the case $Dia = Seq$ and $n = 0$. All other cases work analogously.

By lemma \ref{ExplicitFormOfFreeSpectra}, in this case the morphism $\lambda_0$ has components like so:

$$
  \array{
    \vdots && \vdots
    \\
    S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    F_1 S^1 &\stackrel{\lambda_0}{\longrightarrow}& F_0 S^0
  }
  \,.
$$

Now for $X$ any sequential spectrum, then a morphism $f \colon F_0 S^0 \to X$ is uniquely determined by its 0th components $f_0 \colon S^0 \to X_0$ (that's of course the very free property of $F_0 S^0$); as the compatibility with the structure maps forces the first component, in particular, to be $\sigma_0^X\circ \Sigma f$:

$$
  \array{
    \Sigma S^0 &\stackrel{\Sigma f}{\longrightarrow}& \Sigma X_0
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\sigma_0^X}}
    \\
    S^1 &\stackrel{\sigma_0^X \circ \Sigma f}{\longrightarrow}& X_1
  }
$$

But that first component is just the component that similarly determines the precompositon of $f$ with $\lambda_0$, hence $\lambda_0^\ast f$ is fully fixed as being the map $\sigma_0^X \circ \Sigma f$. Therefore $\lambda_0^\ast$ is the function

$$
  \lambda_0^\ast
  \;\colon\;
  X_0
  =
  Maps(S^0, X_0)
  \stackrel{f \mapsto \sigma_0^X \circ \Sigma f}{\longrightarrow}
  \Maps(S^1, X_1)
  =
  \Omega X_1
  \,.
$$

It remains to see that this is the $(\Sigma \dashv \Omega)$-[[adjunct]] of $\sigma_0^X$. By the general formula for adjuncts, this is

$$
  \tilde \sigma_0^X
    \;\colon\;
  X_0
     \stackrel{\eta}{\longrightarrow}
  \Omega \Sigma X_0
     \stackrel{\Omega \sigma_0^X}{\longrightarrow}
  \Omega X_1
  \,.
$$

To compare to the above, we check what this does on points: $S^0 \stackrel{f_0}{\longrightarrow} X_0$ is sent to the composite

$$
   S^0
     \stackrel{f_0}{\longrightarrow}
   X_0
     \stackrel{\eta}{\longrightarrow}
   \Omega \Sigma X_0
     \stackrel{\Omega \sigma_0^X}{\longrightarrow}
   \Omega X_1
   \,.
$$

To identify this as a map $S^1 \to X_1$ we use the adjunction isomorphism once more to throw all the $\Omega$-s on the right back to $\Sigma$-s the left, to finally find that this is indeed

$$
  \sigma_0^X \circ \Sigma f
    \;\colon\;
  S^1 = \Sigma S^0 \stackrel{\Sigma f}{\longrightarrow} \Sigma X_0 \stackrel{\sigma_0^X}{\longrightarrow} X_1
  \,.
$$

=--


+-- {: .num_lemma #AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences}
###### Lemma

The maps $\lambda_n \;\colon\; F_{n+1} S^1 \longrightarrow F_n S^0$  in def. \ref{CorepresentationOfAdjunctsOfStructureMaps} are

1. [[stable weak homotopy equivalences]] for [[sequential spectra]], [[orthogonal spectra]] and [[pre-excisive functors]], i.e. for ${Dia} \in \{Top^{\ast/}, Orth, Seq\}$;

1. **not** stable weak homotopy equivalences for the case of symmetric spectra ${Dia} = {Sym}$.

=--

([Hovey-Shipley-Smith 00, example 3.1.10](#HoveyShipleySmith00), [MMSS 00, lemma 8.6](#MMSS00), [Schwede 12, example 4.26](#Schwede12))

+-- {: .proof}
###### Proof


This follows by inspection of the explicit form of the maps, via prop. \ref{ExplicitFormOfFreeSpectra}. We discuss each case separately:

**sequential case**

Here the components of the morphism eventually stabilize to isomorphisms

$$
  \array{
    & \vdots && \vdots
    \\
    (\lambda_n)_{n+3} & S^3 &\stackrel{id}{\longrightarrow}& S^3
    \\
    (\lambda_n)_{n+2} & S^2 &\stackrel{id}{\longrightarrow}& S^2
    \\
    (\lambda_n)_{n+1} & S^1 &\stackrel{id}{\longrightarrow}& S^1
    \\
    (\lambda_n)_n \colon & \ast &\stackrel{0}{\longrightarrow}& S^0
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \vdots && \vdots
    \\
    & \ast &\longrightarrow& \ast
    \\
    & \underbrace{\,\,\,} && \underbrace{\,\,\,}
    \\
    \lambda_n \colon & F_{n+1} S^1 &\stackrel{}{\longrightarrow}& F_n S^0
  }
$$

and this immediately gives that $\lambda_n$ is an isomorphism on [[stable homotopy groups]].

**orthogonal case**

Here for $q \geq n+1$ the $q$-component of $\lambda_n$ is the [[quotient]] map

$$
  (\lambda_n)_q
    \;\colon\;
  O(q)_+ \wedge_{O(q-n-1)} S^{q-n}
   \simeq
  O(q)_+ \wedge_{O(q-n-1)} S^1 \wedge S^{q-n-1}
  \longrightarrow
  O(q)_+ \wedge_{O(q-n)}S^{q-n}
  \,.
$$

By the [suspension isomorphism](homotopy+group+of+a+spectrum#SuspensionIsomorphismOfStableHomotopyGroups) for [[stable homotopy groups]], $\lambda_n$ is a stable weak homotopy equivalence precisely if any of its [[reduced suspension|suspensions]] is. Hence consider instead $\Sigma^n \lambda_n \coloneqq S^n \wedge \lambda_n$, whose $q$-component is

$$
  (\Sigma^n\lambda_n)_q
    \;\colon\;
  O(q)_+ \wedge_{O(q-n-1)} S^{q}
    \longrightarrow
  O(q)_+ \wedge_{O(q-n)}S^{q}
  \,.
$$

Now due to the fact that $O(q-k)$-action on $S^q$ lifts to an $O(q)$-action, the quotients of the diagonal action of $O(q-k)$ equivalently become quotients of just the left action. Formally this is due to the existence of the [[commuting diagram]]

$$
  \array{
    O(q)_+ \wedge S^q
     &\stackrel{id}{\longrightarrow}&
    O(q)_+ \wedge S^q
     &\stackrel{id}{\longrightarrow}&
    O(q)_+ \wedge S^q
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{p_2}}
    \\
    Q(q)_+ \wedge_{Q(q-k)} S^q
     &\longrightarrow&
    Q(q)_+ \wedge_{Q(q)} S^q
    & \stackrel{\simeq}{\longrightarrow} & S^q
  }
$$

which says that the image of any $(g,s) \in O(q)_+  \wedge S^q$ in the quotient $Q(q)_+ \wedge_{Q(q-k)} S^q$ is labeled by $([g],s)$.

It follows that $(\Sigma^n\lambda_n)_q$ is the smash product of a projection map of [[coset spaces]] with the identity on the sphere:

$$
  (\Sigma^n\lambda_n)_q
    \simeq
  proj_+ \wedge id_{S^q}
    \;\colon\;
  O(q)/O(q-n-1)_+ \wedge S^q
    \longrightarrow
  O(q)/O(q-n)_+ \wedge S^{q}
  \,.
$$

Now finally observe that this projection function

$$
  proj
  \;\colon\;
  O(q)/O(q-n-1)
    \longrightarrow
  O(q)/O(q-n)
$$

is $(q - n -1 )$-connected (see [here](coset+space#CofiberSequencesOfCosetsOfOrthogonalGroups)). Hence its smash product with $S^q$ is $(2q - n -1 )$-connected.

The key here is the fast growth of the connectivity with $q$. This implies that for each $s$ there exists $q$ such that $\pi_{s+q}((\Sigma^n \lambda_n)_q)$ becomes an isomorphism. Hence $\Sigma^n \lambda_n$ is a stable weak homotopy equivalence and therefore so is $\lambda_n$.

**symmetric case**

Here the morphism $\lambda_n$ has the same form as in the orthogonal case above, except that all occurences of [[orthogonal groups]] are replaced by just their sub-[[symmetric groups]].

Accordingly, the analysis then proceeds entirely analogously, with the key difference that the projection

$$
  \Sigma(q)/\Sigma(q-n-1)
    \longrightarrow
  \Sigma(q)/\Sigma(q-n)
$$

does _not_ become highly connected as $q$ increases, due to the [[discrete topological space]] underlying the symmetric group. Accordingly the conclusion now is the opposite: $\lambda_n$ is not a stable weak homotopy equivalence in this case.

=--

Another use of free spectra is that their [[pushout products]] may be explicitly analyzed, and checking the [[pushout-product axiom]] for general cofibrations may be reduced to checking it on morphisms between free spectra.


+-- {: .num_lemma #PushoutSmashProductOfFreeSpectraOnGeneratingCofibrationsOfTop}
###### Lemma

The [[symmetric monoidal smash product of spectra]] of the [[free spectrum]] constructions (def. \ref{FreeStructuredSpectrum}) on the generating cofibrations $\{S^{n-1}\overset{i_n}{\hookrightarrow} D^n\}_{n \in \mathbb{B}}$ of the [[classical model structure on topological spaces]] is given by addition of indices

$$
  (F_k i_{n_1}) \Box_{\mathbb{S}_{dia}} (F_\ell i_{n_2})
  \simeq
  F_{k+\ell}( i_{n_1 + n_2})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{SmashProductOfFreeSpectra} the [[commuting diagram]] defining the [[pushout product]] of [[free spectra]]

$$
  \array{
    && F_k S^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} S^{n_2-1}_+
    \\
    & \swarrow && \searrow
    \\
    F_k D^{n_1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} S^{n_2-1}_+
    &&
    &&
    F_k S^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_{\ell} D^{n_2-1}_+
    \\
    & \searrow && \swarrow
    \\
    && F_k D^{n_1-1}_+ \wedge_{\mathbb{S}_{dia}} F_k D^{n_2-1}_+
  }
$$

is equivalent to this diagram:

$$
  \array{
    && F_{k+\ell}((S^{n_1-1}\times S^{n_2-1})_+)
    \\
    & \swarrow && \searrow
    \\
    F_{k+\ell}((D^{n_1} \times S^{n_2-1})_+)
    &&
    &&
    F_{k+\ell}((S^{n_1-1} \times D^{n_2})_+)
    \\
    & \searrow && \swarrow
    \\
    && F_{k+ \ell}( (D^{n_1}\times D^{n_2})_+ )
  }
  \,.
$$

Since the [[free spectrum]] construction is a left adjoint, it preserves pushouts, and so

$$
  (F_{k}i_{n_1})
    \Box_{\mathbb{S}_{dia}}
  (F_{\ell}i_{n_2})
   \simeq
  F_{k + \ell}( i_{n_1} \Box i_{n_2})
   \simeq
  F_{k + \ell}( i_{n_1 + n_2})
 \,,
$$

where in the second step we used [this lemma](pushout-product#PushoutProductOfSpheresInclusionsIntoDisks).

=--






## The strict model structure on structured spectra


+-- {: .num_theorem #StrictModelStructureOnDiagramSpectra}
###### Theorem

The four categories of

1. [[pre-excisive functors]] $Exc(Top_{cg})$;

1. [[orthogonal spectra]] $OrthSpec(Top_{cg}) = \mathbb{S}_{orth} Mod$;

1. [[symmetric spectra]] $SymSpec(Top_{cg}) = \mathbb{S}_{sym}Mod$;

1. [[sequential spectra]] $SeqSpec(Top_{cg}) = \mathbb{S}_{seq}Mod$

(from def. \ref{FinitePointedCWComplexes}, prop. \ref{SseqModulesAreSequentialSpectra}, def. \ref{SsymModuleSymmetricSpectra}) each admit a [[model category]] structure ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) whose weak equivalences and fibrations are those morphisms which induce on all component spaces weak equivalences or fibrations, respectively, in the [[classical model structure on pointed topological spaces]] $(Top^{\ast/}_{cg})_{Quillen}$. ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)).
These are called the **strict model structures** (or **level model structures**) on [[structured spectra]].

Moreover, under the [[equivalences of categories]] of prop. \ref{SseqModulesAreSequentialSpectra} and prop. \ref{DiagramSpectraGiveSymmetricAndOrthogonalSpectra}, the restriction functors in def. \ref{TopologicalDiagramCategoriesForSpectra} constitute [[right adjoints]] of [[Quillen adjunctions]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunction)) between these model structures:



$$
 \array{
   Exc(Top_{cg})_{strict} && OrthSpec(Top_{cg})_{strict} && SymSpec(Top_{cg})_{strict} && SeqSpec(Top_{cg})_{strict}
   \\
   \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   && \downarrow^{\mathrlap{\simeq}}
   \\
   \mathbb{S} Mod_{strict}
   &
     \underoverset
       {\underset{orth^\ast}{\longrightarrow}}
       {\overset{orth_!}{\longleftarrow}}
       {\bot}
   &
   \mathbb{S}_{Orth} Mod_{strict}
   &
     \underoverset
       {\underset{sym^\ast}{\longrightarrow}}
       {\overset{sym_!}{\longleftarrow}}
       {\bot}
   &
   \mathbb{S}_{Sym} Mod_{strict}
   &
     \underoverset
       {\underset{seq^\ast}{\longrightarrow}}
       {\overset{seq_!}{\longleftarrow}}
       {\bot}
   &
   \mathbb{S}_{Seq} Mod_{strict}
  }
  \,.
$$

=--

([MMSS 00, theorem 6.5](#MMSS00))

+-- {: .proof}
###### Proof

By prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors} all four categories are equivalently categories of pointed [[topologically enriched functors]]

$$
  \mathbb{S}_{dia}Mod
   \simeq
  [ \mathbb{S}_{dia} Free_{dia}Mod, Top^{\ast/}_{cg} ]
$$

and hence the existence of the model structures with componentwise weak equivalences and fibrations is a special case of the general existence of the [[projective model structure on enriched functors]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ProjectiveModelStructureOnTopologicalFunctors)).

The three restriction functors $dia^\ast$ each have a [[left adjoint]] $dia_!$ by topological [[left Kan extension]] (prop. \ref{TopologicalLeftKanExtensionBCoend}).

Moreover, the three right adjoint restriction functors are along inclusions of objects, hence evidently preserve componentwise weak equivalences and fibrations.  Hence these are [[Quillen adjunctions]].

=--

+-- {: .num_defn #GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}
###### Definition

Recall the sets

$$
  I_{Top^{\ast/}} \coloneqq \{S^{n-1}_+ \overset{(i_n)_+}{\hookrightarrow} D^n_+\}_{n \in \mathbb{N}}
$$

$$
  J_{Top^{\ast/}} \coloneqq \{D^n_+ \overset{(j_n)_+}{\hookrightarrow} (D^n \times I)_+\}_{n \in \mathbb{N}}
$$

of generating cofibrations and generating acyclic cofibrations, respectively, of the [[classical model structure on pointed topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#GeneratingCofibrationsForPointedTopologicalSpaces))

Write


$$
  I^{strict}_{dia}
    \;\coloneqq\;
  \left\{
    F_c^{dia}((i_n)_+)
  \right\}_{c \in Dia, n \in \mathbb{N}}
$$

for the set of images under forming [[free spectra]], def. \ref{FreeStructuredSpectrum}, on the morphisms in $I_{Top^{\ast/}}$ from above. Similarly, write

$$
  J^{strict}_{dia}
    \;\coloneqq\;
  \left\{
   F_c^{dia}((j_n)_+)
  \right\}
  \,,
$$

for the set of images under forming free spectra of the morphisms in $J_{Top^{\ast/}_{cg}}$.

=--


+-- {: .num_prop #CofibrantGenerationOfStrictModelStructure}
###### Proposition

The sets $I^{strict}_{dia}$
and $J^{strict}_{dia}$ from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} are, respectively sets of [[generating cofibrations]] and generating acyclic cofibrations that exhibit the strict model structure $\mathbb{S}_{Dia}Mod_{strict}$ from theorem \ref{StrictModelStructureOnDiagramSpectra} as a [[cofibrantly generated model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CofibrantlyGeneratedModelCategory)).

=--

([MMSS 00, theorem 6.5](#MMSS00))


+-- {: .proof}
###### Proof

By theorem \ref{StrictModelStructureOnDiagramSpectra} the strict model structure is equivalently the projective pointed  [[model structure on enriched functors|model structure on topologically enriched functors]]

$$
  \mathbb{S}_{Dia}Mod_{strict}
    \simeq
  [\mathbb{S}_{Dia}Free_{Dia}Mod^{op}, Top^{\ast/}]_{proj}
$$

of the opposite of the category of free spectra on objects in $\mathcal{C} \hookrightarrow [\mathcal{C}, Top^{\ast/}_{cg}]$.

By the general discussion in _[[Introduction to Stable homotopy theory -- P|Part P -- Classical homotopy theory]]_ ([this](classical+model+structure+on+topological+spaces#ProjectiveModelStructureOnTopEnrichedFunctors) theorem) the [[projective model structure on functors]] is cofibrantly generated by the smash tensoring of the [[representable functors]] with the elements in $I_{Top^{\ast/}_{cg}}$ and $J_{Top^{\ast/}_{cg}}$. By the proof of lemma \ref{ExplicitExpressionForFreeSpectra}, these are precisely the morphisms of free spectra in $I^{strict}_{dia}$ and $J^{strict}_{dia}$, respectively.

=--





### Topological enrichment


By the general properties of the [[projective model structure on functors|projective model structure]] on [[topologically enriched functors]], theorem \ref{StrictModelStructureOnDiagramSpectra} implies that the strict model category of structured spectra inherits the structure of an [[enriched model category]], enriched over the [[classical model structure on pointed topological spaces]]. This proceeds verbatim as for sequential spectra (in _[part 1.1 -- Topological enrichement](Introduction+to+Stable+homotopy+theory+--+1-1#TopologicalEnrichment)_), but for ease of reference we here make it explicit again.


+-- {: .num_defn #PushoutProductWithRespectToSmashTensoring}
###### Definition

Let $Dia \in \{Top^{\ast/}_{cg,fin}, Orth, Sym, Seq\}$ one of the shapes for structured spectra from def. \ref{TopologicalDiagramCategoriesForSpectra}.

Let $f \;\colon \; X \to Y$ be a morphism in $\mathbb{S}_{dia}Mod$ (as in prop. \ref{StrictModelStructureOnDiagramSpectra}) and let $i \;\colon\; A \to B$ a morphism in $Top_{cg}^{\ast/}$.

Their **[[pushout product]] with respect to smash tensoring** is the universal morphism

$$
  f \Box i
    \coloneqq
  \left((id,i), (f,id)\right)
$$

in

$$
  \array{
    && X \wedge A
    \\
    & {}^{\mathllap{(f,id)}}\swarrow && \searrow^{\mathrlap{(id,i)}}
    \\
    Y \wedge A && (po) && X \wedge B
    \\
    & {}_{\mathllap{}}\searrow && \swarrow
    \\
    && (Y \wedge A) \underset{X \wedge A}{\sqcup} (X \wedge B)
    \\
    && \downarrow^{\mathrlap{((id, i), (f,id))}}
    \\
    && Y \wedge B
  }
  \,,
$$

where

$$
  (-)\wedge(-)
    \;\colon\;
  \mathbb{S}_{dia}Mod
   \times
  Top^{\ast/}_{cg}
   \simeq
  [ \mathbb{S}_{dia}Fre_{dia}Mod^{op},\; Top^{\ast/}_{cg}]
  \times
  Top^{\ast/}_{cg}
    \longrightarrow
  [ \mathbb{S}_{dia}Fre_{dia}Mod^{op},\; Top^{\ast/}_{cg}]
  \simeq
  \mathbb{S}_{dia}Mod
$$

denotes the smash tensoring of pointed topologically enriched functors with pointed topological spaces ([def.](Introduction+to+Stable+homotopy+theory+--+P#TensoringAndPoweringOfTopologicallyEnrichedCopresheaves))

Dually, their **pullback powering** is the universal morphism

$$
  f^{\Box i}
    \coloneqq
  (Maps(B,f)_\ast, Maps(i,X)_\ast)
$$

in

$$
  \array{
    && Maps(B,X)_\ast
    \\
    && \downarrow^{\mathrlap{(Maps(B,f)_\ast, Maps(i,X)_\ast)}}
    \\
    && Maps(B,Y)_\ast \underset{Maps(A,Y)_\ast}{\times} Maps(A,X)_\ast
    \\
    & \swarrow && \searrow
    \\
    Maps(B,Y)_\ast && (pb) && Maps(A,X)_\ast
    \\
    & {}_{\mathllap{Maps(i,Y)_\ast}}\searrow
      &&
    \swarrow_{\mathrlap{Maps(A,p)_\ast}}
    \\
    && Maps(A,Y)_\ast
  }
  \,,
$$

where

$$
  Maps(-,-)_\ast
   \;\colon\;
  (Top^{\ast}_{cg})^{op}
   \times
  \mathbb{S}_{dia}Mod
   \simeq
  (Top^{\ast/}_{cg})^{op}
   \times
  [\mathbb{S}_{dia}Free_{Dia}Mod^{op},Top^{\ast/}_{cg}]
    \longrightarrow
  [\mathbb{S}_{dia}Free_{Dia}Mod^{op},Top^{\ast/}_{cg}]
   \simeq
  \mathbb{S}_{dia}Mod
$$

denotes the smash powering ([def.](Introduction+to+Stable+homotopy+theory+--+P#TensoringAndPoweringOfTopologicallyEnrichedCopresheaves)).

Finally, for $f \colon X \to Y$ and $i \colon A \to B$ both morphisms in $\mathbb{S}_{dia}Mod$, then their pullback powering is the universal morphism

$$
  f^{\Box i} \coloneqq (\mathbb{S}_{dia}Mod(B,f), \mathbb{S}_{dia}Mod(i,X))
$$

in

$$
  \array{
    && \mathbb{S}_{dia}Mod(B,X)
    \\
    && \downarrow^{\mathrlap{(\mathbb{S}_{dia}Mod(B,f), \mathbb{S}_{dia}Mod(i,X))}}
    \\
    && \mathbb{S}_{dia}Mod(B,Y) \underset{\mathbb{S}_{dia}Mod(A,Y)}{\times} \mathbb{S}_{dia}Mod(A,X)
    \\
    & \swarrow && \searrow
    \\
    \mathbb{S}_{dia}Mod(B,Y) && (pb) && \mathbb{S}_{dia}Mod(A,X)
    \\
    & {}_{\mathllap{\mathbb{S}_{dia}Mod(i,Y)}}\searrow
      &&
    \swarrow_{\mathrlap{\mathbb{S}_{dia}Mod(A,p)}}
    \\
    && \mathbb{S}_{dia}Mod(A,Y)
  }
  \,,
$$

where now $\mathbb{S}_{dia}Mod(-,-)$ is the [[hom-space]] functor of $\mathbb{S}_{dia}Mod \simeq [\mathbb{S}_{dia}Free_{Dia}Mod^{op}, Top^{\ast/}_{cg}]$ from def. \ref{PointedTopologicalFunctorCategory}.

=--

+-- {: .num_prop #PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms}
###### Proposition

The operations of forming pushout products and pullback powering with respect to smash tensoring in def. \ref{PushoutProductWithRespectToSmashTensoring} is compatible with the strict model structure $\mathbb{S}_{dia}Mod_{strict}$ on structured spectra from theorem \ref{StrictModelStructureOnDiagramSpectra} and with the [[classical model structure on pointed topological spaces]] $(Top^{\ast/}_{cg})_{Quillen}$  ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)) in that pushout product takes two cofibrations to a cofibration, and to an acyclic cofibration if at least one of the inputs is acyclic, and pullback powering takes a fibration and a cofibration to a fibration, and to an acylic one if at least one of the inputs is acyclic:

$$
  \begin{aligned}
    Cof_{strict} \Box Cof_{cl}
    & \subset\;
    Cof_{strict}
    \\
    Cof_{strict} \Box (Cof_{cl} \Box W_{cl})
    & \subset\;
    Cof_{strict} \cap W_{strict}
    \\
    (Cof_{strict} \cap W_{strict})
    \Box
    Cof_{cl}
    & \subset\;
    Cof_{strict} \cap W_{strict}
  \end{aligned}
  \,.
$$

Dually, the pullback powering (def. \ref{PushoutProductWithRespectToSmashTensoring}) satisfies

$$
  \begin{aligned}
    Fib_{strict}^{\Box Cof_{cl}}
    & \subset\;
    Fib_{strict}
    \\
    Fib_{strict}^{\Box ( Cof_{cl} \cap W_{cl})}
    & \subset\;
    Fib_{strict}\cap W_{strict}
    \\
    (Fib_{strict} \cap W_{strict})^{\Box Cof_{cl}}
    & \subset\;
    Fib_{strict} \cap W_{strict}
  \end{aligned}
  \,.
$$


=--


+-- {: .proof}
###### Proof

The statement concering the pullback powering follows directly from the analogous statement for topological spaces ([prop.](Introduction+to+Stable+homotopy+theory+--+P#PullbackPowering)) by the fact that, via theorem \ref{StrictModelStructureOnDiagramSpectra}, the fibrations and weak equivalences in $\mathbb{S}_{dia}Mod_{strict}$ are degree-wise those in $(Top_{cg}^{\ast/})_{Quillen}$, and since smash tensoring and powering is defined degreewise. From this the statement about the pushout product follows dually by [[Joyal-Tierney calculus]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#JoyalTierneyCalculus)).

=--

+-- {: .num_remark #StructuredSpectraIsTopologicallyEnrichedModelCategory}
###### Remark

In the language of [[model category]]-theory, prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} says that $\mathbb{S}_{dia}Mod_{strict}$ is an _[[enriched model category]]_, the enrichment being over $(Top_{cg}^{\ast/})_{Quillen}$. This is often referred to simply as a "topological model category".

=--

We record some immediate consequences of prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} that will be useful.

+-- {: .num_prop #SmashTensoringWithCellComplexIsLeftQuillen}
###### Proposition

Let $K \in Top^{\ast}_{cg}$ be a [[retract]] of a [[cell complex]] ([def. ](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCellComplex)), then the smash-tensoring/powering adjunction from prop. \ref{UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg} is a [[Quillen adjunction]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunction)) for the strict model structure from theorem \ref{StrictModelStructureOnDiagramSpectra}

$$
  \mathbb{S}_{dia}Mod(Top_{cg})_{strict}
    \underoverset
      {\underset{Maps(K,-)_\ast}{\longrightarrow}}
      {\overset{(-)\wedge K}{\longleftarrow}}
      {\bot}
  \mathbb{S}_{dia}Mod(Top_{cg})_{strict}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By assumption, $K$ is a cofibrant object in the [[classical model structure on pointed topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#TopQuillenModelStructure), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)), hence $\ast \to K$ is a cofibration in $(Top^{\ast/}_{cg})_{Quillen}$. Observe then that the the [[pushout product]] of any morphism $f$ with $\ast \to K$ is equivalently the smash tensoring of $f$ with $K$:

$$
  f \Box (\ast \to K)
  \simeq
  f \wedge K
  \,.
$$

This way prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} implies that $(-)\wedge K$ preserves cofibrations and acyclic cofibrations, hence is a left Quillen functor.

=--


+-- {: .num_lemma #StandardReducedCylinderOnStructuredSpectrumIsGood}
###### Lemma

Let $X \in \mathbb{S}_{dia}Mod_{strict}$ be a structured spectrum, regarded in the strict model structure of theorem \ref{StrictModelStructureOnDiagramSpectra}.

1. The smash powering of $X$ with the standard topological interval $I_+$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#StandardReducedCyclinderInTop)) is a good [[path space object]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#PathAndCylinderObjectsInAModelCategory))

   $$
     \Delta_X
      \;\colon\;
     X
       \overset{\in W_{strict}}{\longrightarrow}
     X^{I_+}
       \overset{\in Fib_{strict}}{\longrightarrow}
     X \times X
     \,.
   $$

1. If $X$ is cofibrant, then its smash tensoring with the standard topological interval $I_+$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#StandardReducedCyclinderInTop)) is a good [[cylinder object]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#PathAndCylinderObjectsInAModelCategory))

   $$
     \nabla_X
       \;\colon\;
     X \vee X
       \overset{\in Cof_{strict}}{\longrightarrow}
     X\wedge (I_+)
       \overset{\in W_{strict}}{\longrightarrow}
     X
     \,.
   $$

=--

+-- {: .proof}
###### Proof

It is clear that we have weak equivalences as shown ($I \to \ast$ is even a [[homotopy equivalence]]), what requires proof is that the path object is indeed good in that $X^{(I_+)} \to X \times X$ is a fibration, and the cylinder object is indeed good in that $X \vee X \to X\wedge (I_+)$ is indeed a cofibration.

For the first statement, notice that the pullback powering (def. \ref{PushoutProductWithRespectToSmashTensoring}) of $\ast \sqcup \ast \overset{(i_0,i_1)}{\longrightarrow} I$ into the terminal morphism $X \to \ast$ is the same as the powering $X^{(i_0,i_1)}$:

$$
  ((X\to\ast)^{\Box(i_0,i_1)})
    \;\simeq\;
  X^{(i_0,i_1)}
  \,,.
$$

But since every object in $\mathbb{S}_{dia}Mod_{strict}$ is fibrant, so that $X \to \ast$ is a fibration, and since $(i_0,i_1)$ is a [[relative cell complex]] inclusion and hence a cofibration in $(Top^{\ast/}_{cg})_{Quilln}$, prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} says that $X^{(i_0,i_1)} \colon X^{I_+}\to X \times X$ is a fibration.

Dually, observe that

$$
   (\ast \to X) \Box (i_0, i_1)
     \;\simeq\;
   X \wedge (i_0,i_1)
   \,.
$$

Hence if $X$ is assumed to be cofibrant, so that $\ast \to X$ is a cofibration, then prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} implies that $X \wedge (i_0,i_1) \colon X \wedge X \to X \wedge (I_+)$ is a cofibration.

=--



+-- {: .num_prop #PushoutProductOfspectrumWithSpaceInteractingWithHomSpaces}
###### Proposition

For $X \in \mathbb{S}_{dia}Mod$ a [[structured spectrum]], $f \in Mor(\mathbb{S}_{dia}Mod)$ any morphism of structured spectra, and for $g  \in Mor(Top_{cpt}^{\ast/})$ a morphism of [[pointed topological spaces]], then the [[hom-spaces]] of def. \ref{PointedTopologicalFunctorCategory} (via prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors}) interact with the pushout-product and pullback-powering from def. \ref{PushoutProductWithRespectToSmashTensoring} in that there is a [[natural isomorphism]]

$$
  \mathbb{S}_{dia}Mod(f \Box g, X)
    \simeq
  (\mathbb{S}_{dia}Mod(f,X))^{\Box g}
  \,.
$$

=--


+-- {: .proof}
###### Proof

Since the pointed compactly generated [[mapping space]] functor ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PointedMappingSpace))

$$
  Maps(-,-)_\ast
  \;\colon\;
  \left(Top^{\ast/}_{cg}\right)^{op}
  \times
  Top^{\ast/}_{cg}
  \longrightarrow
  Top^{\ast/}_{cg}
$$

takes [[colimits]] in the first argument to [[limits]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#MappingSpacesSendsColimitsInFirstArgumentToLimits)) and [[ends]] in the second argument to ends (remark \ref{MappingSpacePreservesEnds}), and since limits and colimits in $\mathbb{S}_{dia}Mod$ are computed objectswise ([this prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedCopresheavesHaveAllLimitsAndColimits) via prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors}) this follows with the [[end]]-formula for the mapping space (def. \ref{PointedTopologicalFunctorCategory}):

$$
  \begin{aligned}
    \mathbb{S}_{dia}Mod(f \Box g, X)
    & =
    \underset{c}{\int} Maps( (f \Box g)(c), X(c) )_\ast
    \\
    & \simeq
    \underset{c}{\int} Maps( f(c) \Box g, X(c) )_\ast
    \\
    & \simeq
    \underset{c}{\int} Maps( f(c), X(c))_\ast^{\Box g}
    \\
    & \simeq
    \left(
       \underset{c}{\int} Maps(f(c), X(c))_\ast
    \right)^{\Box g}
    \\
    & \simeq
    (\mathbb{S}_{dia}Mod(f,X))^{\Box g}
  \end{aligned}
  \,.
$$


=--




+-- {: .num_prop #ConnectedComponentOfHomSpaceOfSModsIsLeftHomotopyClasses}
###### Proposition

For $X,Y \in \mathbb{S}_{dia}Mod(Top_{cg})$ two structured spectra with $X$ cofibrant in the strict model structure of def. \ref{StrictModelStructureOnDiagramSpectra}, then there is a [[natural bijection]]

$$
  \pi_0 \mathbb{S}_{dia}Mod(X,Y)
  \simeq
   [X,Y]_{strict}
$$

between the [[connected components]] of the [[hom-space]] (def. \ref{PointedTopologicalFunctorCategory} via prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors}) and the [[hom-set]] in the [[homotopy category of a model category|homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) of the strict model structure from theorem \ref{StrictModelStructureOnDiagramSpectra}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg} the path components of the [[hom-space]] are the [[left homotopy]] classes of morphisms of structured spectra with respect to the standard [[cylinder spectrum]] $X \wedge (I_+)$:

$$
  \frac{
    I_+ \longrightarrow SeqSpec(X,Y)
  }{
    X \wedge (I_+) \longrightarrow Y
  }
  \,.
$$

Moreover, by lemma \ref{StandardReducedCylinderOnStructuredSpectrumIsGood} the degreewise standard [[reduced cylinder]] $X \wedge (I_+)$ of structured spectra is a good [[cylinder object]] on $X$ in $\mathbb{S}_{dia}Mod_{strict}$. Hence hom-sets in the strict [[homotopy category of a model category|homotopy category]] out of a cofibrant into a fibrant object are given by standard [[left homotopy]] classes of morphisms

$$
  [X,Y]_{strict} \simeq Hom_{\mathbb{S}_{dia}Mod}(X,Y)_{/\sim}
$$

([this lemma](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)). Since $X$ is cofibrant by assumption and since every object is fibrant in $\mathbb{S}_{dia}Mod_{strict}$, this is the case. Hence the notion of left homotopy here is that seen by the standard interval, and so the claim follows.

=--







### Monoidal model structure

We now combine the concepts of [[model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) and [[monoidal category]] (def. \ref{MonoidalCategory}).

Given a category $\mathcal{C}$ that is equipped both with the structure of a [[monoidal category]] and of a [[model category]], then one may ask whether these two structures are compatible, in that the [[left derived functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#LeftAndRightDerivedFunctorsOnModelCategories)) of the [[tensor product]] exists to equip also the [[homotopy category of a model category|homotopy category]] with the structure of a monoidal category. If so, then one may furthermore ask if the [[localization]] functor $\gamma \;\colon\; \mathcal{C} \longrightarrow Ho(\mathcal{C})$ is a [[monoidal functor]] (def. \ref{LaxMonoidalFunctor}).

The axioms on a _[[monoidal model category]]_ (def. \ref{MonoidalModelCategory} below) are such as to ensure that this is the case.

A key consequence is that, via prop. \ref{MonoidsPreservedByLaxMonoidalFunctor}, for a monoidal model category the localization functor $\gamma$ carries monoids to monoids. Applied to the [[stable model category]] of spectra established below, this gives that [[structured ring spectra]] indeed represent [[ring spectra]] in the homotopy category.  (In fact much more is true, but requires further proof: there is also a model structure on monoids in the model structure of spectra, and with respect to that the structured ring spectra represent [[A-infinity rings]]/[[E-infinity rings]].)




+-- {: .num_defn #MonoidalModelCategory}
###### Definition

A (symmetric) **[[monoidal model category]]** is a [[model category]] $\mathcal{C}$
([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) equipped with the structure of a  [[closed monoidal category|closed]] (def. \ref{ClosedMonoidalCategory}) [[symmetric monoidal category|symmetric]] (def. \ref{SymmetricMonoidalCategory}) [[monoidal category]] $(\mathcal{C}, \otimes, I)$ (def. \ref{MonoidalCategory}) such that the following two compatibility conditions are satisfied

1. **([[pushout-product axiom]])** For every pair of cofibrations $f \colon X \to Y$ and $f' \colon X' \to Y'$, their [[pushout-product]], hence the induced morphism out of the cofibered [[coproduct]] over ways of forming the tensor product of these objects

   $$
     f \Box_{\otimes} g
       \;\coloneqq\;
     (X \otimes Y') \underset{{X \otimes X'}}{\sqcup} (Y \otimes X')
     \longrightarrow
     Y \otimes Y'
     \,,
   $$

   is itself a cofibration, which, furthermore, is acyclic if at least one of $f$ or $f'$ is.

   (Equivalently this says that the [[tensor product]] $\otimes \colon \mathcal{C} \times \mathcal{C} \to \mathcal{C}$ is a _left [[Quillen bifunctor]]_.)

1. **(unit axiom)** For every cofibrant object $X$ and every cofibrant resolution $\emptyset \overset{\in Cof}{\longrightarrow} Q 1 \underoverset{p_1}{\in W}{\longrightarrow} 1$ of the [[tensor unit]] $1$, the resulting morphism

   $$
     Q 1 \otimes X
       \overset{p_1 \otimes X}{\longrightarrow}
     1 \otimes X
       \underoverset{\ell}{\in Iso \subset W}{\longrightarrow}
     X
   $$

  is a weak equivalence.


=--

([Hovey 99, def. 4.2.6](#Hovey99) [Schwede-Shipley 00, def. 3.1, remark 3.2](#SchwedeShipley00))

Observe some immediate consequences of these axioms:

+-- {: .num_remark }
###### Remark

Since a [[monoidal model category]] (def. \ref{MonoidalModelCategory}) is assumed to be [[closed monoidal category|closed monoidal]] (def. \ref{ClosedMonoidalCategory}), for every object $X$ the tensor product $X \otimes (-) \simeq (-) \otimes X$ is a [[left adjoint]] and hence preserves all [[colimits]]. In particular it preserves the [[initial object]] $\emptyset$ (which is the colimit over the empty diagram).

If follows that the tensor-[[pushout-product axiom]] in def. \ref{MonoidalModelCategory} implies that for $X$ a cofibrant object, then the functor $X \otimes (-)$ preserves cofibrations and acyclic cofibrations, since

$$
  f \Box_\otimes (\emptyset \to X)
  \simeq
  f \otimes X
  \,.
$$

This implies that if the [[tensor unit]] $1$ happens to be cofibrant, then the unit axiom in def. \ref{MonoidalModelCategory} is already implied by the pushout-product axiom.  This is because then we have a lift in

$$
  \array{
    \emptyset &\longrightarrow& Q 1
    \\
    {}^{\mathllap{\in Cof}}\downarrow
      &\nearrow&
    \downarrow^{\mathrlap{p_1}}_{\mathrlap{\in W}}
    \\
    1 &=& 1
  }
  \,.
$$

This lift is a weak equivalence by [[two-out-of-three]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryWithWeakEquivalences)). Since it is hence a weak equivalence between cofibrant objects, it is preserved by the left Quillen functor $(-) \otimes X$ (for any cofibrant $X$) by [[Ken Brown's lemma]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#KenBrownLemma)). Hence now $p_1 \otimes X$ is a weak equivalence by [[two-out-of-three]].

Since for all the categories of spectra that we are interested in here the tensor unit is always cofibrant (it is always a version of the [[sphere spectrum]], being the image under the left Quillen functor $\Sigma^\infty_{dia}$ of the cofibrant pointed space $S^0$, prop. \ref{SuspensionSpectrumStructuredStrictQuillenAdjunction}), we may ignore the unit axiom.

=--



+-- {: .num_prop #MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}
###### Proposition

Let $(\mathcal{C}, \otimes, I)$ be a [[monoidal model category]] (def. \ref{MonoidalModelCategory}) with cofibrant [[tensor unit]] $1$.

Then the [[left derived functor]] $\otimes^L$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#LeftAndRightDerivedFunctors)) of the tensor product $\otimes$ exsists and makes the [[homotopy category of a model category|homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) into a [[monoidal category]] $(Ho(\mathcal{C}), \otimes^L, \gamma(1))$ (def. \ref{MonoidalCategory}) such that the [[localization]] functor $\gamma\colon \mathcal{C}_c\to Ho(\mathcal{C})$ ([thm.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)) on the [[category of cofibrant objects]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#FullSubcategoriesOfFibrantCofibrantObjects)) carries the structure of a [[strong monoidal functor]] (def. \ref{LaxMonoidalFunctor})

$$
  \gamma
    \;\colon\;
  (\mathcal{C}, \otimes, 1)
    \longrightarrow
  (Ho(\mathcal{C}), \otimes^L , \gamma(1))
  \,.
$$

=--

The first statement is also for instance in ([Hovey 99, theorem 4.3.2](#Hovey99)).

+-- {: .proof}
###### Proof

For the [[left derived functor]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#LeftAndRightDerivedFunctorsOnModelCategories)) of the tensor product

$$
  \otimes
  \;
  \mathcal{C}\times \mathcal{C}
    \longrightarrow
  \mathcal{C}
$$

to exist, it is sufficient that its restriction to the subcategory

$$
  (\mathcal{C} \times \mathcal{C})_c
  \simeq
  \mathcal{C}_c \times \mathcal{C}_c
$$

of cofibrant objects preserves acyclic cofibrations (by [[Ken Brown's lemma]], [here](Introduction+to+Stable+homotopy+theory+--+P#KenBrownLemma)).

Every morphism $(f,g)$ in the [[product category]] $\mathcal{C}_{c}\times \mathcal{C}_{c}$ (def. \ref{OppositeAndProductOfPointedTopologicallyEnrichedCategory}) may be written as a composite of a pairing with an identity morphisms

$$
  (f,g)
    \;\colon\;
  (c_1, d_1)
    \overset{(id_{c_1},g)}{\longrightarrow}
  (c_1,d_2)
    \overset{(f,id_{c_2})}{\longrightarrow}
  (c_2,d_2)
  \,.
$$

Now since the [[pushout product]] (with respect to tensor product) with the initial morphism $(\ast \to c_1)$ is equivalently the tensor product

$$
  (\ast \to c_1) \Box_{\otimes} g
    \;\simeq\;
  id_{c_1} \otimes g
$$

and

$$
  f \Box_{\otimes} (\ast \to c_2)
    \;\simeq\;
  f \otimes id_{c_2}
$$

the [[pushout-product axiom]] (def. \ref{MonoidalModelCategory}) implies that on the subcategory of cofibrant objects the functor $\otimes$ preserves acyclic cofibrations. (This is why one speaks of a _[[Quillen bifunctor]]_, see also [Hovey 99, prop. 4.3.1](#Hovey99)).

Hence $\otimes^L$ exists.

By the same decomposition and using the [[universal property]] of the [[localization]] of a category ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) one finds that for $\mathcal{C}$ and $\mathcal{D}$ any two [[categories with weak equivalences]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryWithWeakEquivalences)) then the [[localization]] of their [[product category]] is the product category of their localizations:

$$
  (\mathcal{C} \times \mathcal{D})[(W_{\mathcal{C}} \times W_{\mathcal{D}})^{-1}]
  \simeq
  (\mathcal{C}[W^{-1}_{\mathcal{C}}])
  \times
  (\mathcal{D}[W^{-1}_{\mathcal{D}}])
  \,.
$$

With this, the [[universal property]] as a [[localization]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) of the [[homotopy category of a model category]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)) induces [[associators]] $\alpha^L$ and [[unitors]] $\ell^L$, $r^L$ on $(Ho(\mathcal{C}, \otimes^L ))$:


First write

$$
  \mu
    \;\colon\;
  \gamma(-) \otimes^L \gamma(-)
     \overset{\simeq}{\longrightarrow}
  \gamma( (-) \otimes (-) )
$$

for (the inverse of) the corresponding [[natural isomorphism]] in the localization diagram

$$
  \array{
    \mathcal{C} \times \mathcal{C}
      &\overset{\otimes}{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{\gamma \times \gamma}}\downarrow
      &\swArrow^{\mu^{-1}}&
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C})
      \times
    Ho(\mathcal{C})
      &\underset{\otimes^L}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \,.
$$

Then consider the associators:

The essential uniqueness of derived functors shows that the left derived functor of $(-)\otimes ( (-) \otimes (-) )$ and of $( (-) \otimes (-) )\otimes (-) $ is the composite of two applications of $\otimes^L$, due to the factorization

$$
  \array{
    \mathcal{C}_c
      \times
    \mathcal{C}_c
      \times
    \mathcal{C}_c
     &\overset{(-) \otimes ( (-) \otimes (-) )}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{\gamma \times \gamma \times \gamma}}\downarrow
      &\swArrow&
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
     &\underset{\mathbb{L}((-) \otimes ( (-) \otimes (-) ))}{\longrightarrow}&
    Ho(\mathcal{C})
  }
$$

$$
  \;\;\;\;\;\;\;
    \simeq
  \;\;\;\;\;\;\;
$$

$$
  \array{
    \mathcal{C}_c
      \times
    \mathcal{C}_c
      \times
    \mathcal{C}_c
     &\overset{id \times \otimes}{\longrightarrow}&
    \mathcal{C}_c \times \mathcal{C}_c
      &\overset{\otimes}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{\gamma \times \gamma \times \gamma}}\downarrow
       &\swArrow_{id \times \mu^{-1}}&
    {}^{\mathllap{\gamma \times \gamma}}\downarrow
      &\swArrow_{\mu^{-1}}&
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
     &\underset{id \times \otimes^L}{\longrightarrow}&
    Ho(\mathcal{C}) \times Ho(\mathcal{C})
     &\underset{\otimes^L}{\longrightarrow}&
    Ho(\mathcal{C})
  }
$$

and similarly for the case with the parenthesis to the left.

So let

$$
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{((-)\otimes(-))\otimes (-)}{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{
      \mathllap{
         \gamma \times \gamma \times \gamma
     }
    }\downarrow
      &\swArrow_{\mu^{-1}\cdot (\mu^{-1} \times id)}&
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{((-)\otimes^L(-))\otimes^L (-)}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \;\;\;\,,\;\;\;\;\;
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{ (-) \otimes ( (-) \otimes (-) ) }{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{
      \gamma \times \gamma \times \gamma
    }
    }\downarrow
      &\swArrow_{\mu^{-1}\cdot (id \times \mu^{-1})}&
    \downarrow^{\mathrlap{\gamma  }}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{ (-) \otimes^L ( (-) \otimes^L (-) )  }{\longrightarrow}&
    Ho(\mathcal{C})
  }
$$

be the [[natural isomorphism]] exhibiting the [[derived functors]] of the two possible tensor products of three objects, as shown at the top. By pasting the second with the [[associator]] natural isomorphism of $\mathcal{C}$ we obtain another such factorization for the first, as shown on the left below,

$$
  (\star)
  \;\;\;\;\;\;
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{((-)\otimes(-))\otimes (-)}{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{=}}\downarrow
      &\swArrow_{\alpha}&
    \downarrow^{\mathrlap{=}}
    \\
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{ (-) \otimes ( (-) \otimes (-) ) }{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{
      \gamma \times \gamma \times \gamma
    }}\downarrow
      &\swArrow_{\mu^{-1} \cdot ( id \times \mu^{-1} )}&
    \downarrow^{\mathrlap{ \gamma }}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{ (-) \otimes^L ( (-) \otimes^L (-) )  }{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \;\;\;\;\;\;
  =
  \;\;\;\;\;\;
  \array{
    \mathcal{C}_c \times \mathcal{C}_c \times \mathcal{C}_c
      &\overset{((-)\otimes(-))\otimes (-)}{\longrightarrow}&
    \mathcal{C}
    \\
    {}^{\mathllap{
       \gamma \times \gamma \times \gamma
     }}\downarrow
      &\swArrow_{\mu^{-1}\cdot (id \times \mu)}&
    \downarrow^{\mathrlap{\gamma }}
    \\
    Ho(\mathcal{C}) \times Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\overset{((-)\otimes^L(-))\otimes^L (-)}{\longrightarrow}&
    Ho(\mathcal{C})
    \\
    {}^{\mathllap{=}}\downarrow
      &\swArrow_{\alpha^L}&
    \downarrow^{\mathrlap{=}}
    \\
    Ho(\mathcal{C})\times Ho(\mathcal{C})\times Ho(\mathcal{C})
      &\underset{(-)\otimes^L((-)\otimes^L (-))}{\longrightarrow}&
    Ho(\mathcal{C})
  }
$$

and hence by the universal property of the factorization through the derived functor, there exists a unique natural isomorphism $\alpha^L$ such as to make this composite of natural isomorphisms equal to the one shown on the right. Hence the [[pentagon identity]] satisfied by $\alpha$ implies a pentagon identity for $\alpha^L$, and so $\alpha^L$ is an [[associator]] for $\otimes^L$.

Moreover, this equation of natural isomorphisms says that on components the following [[commuting diagram|diagram commutes]]

$$
  \array{
    (\gamma(X) \otimes^L \gamma(Y)) \otimes^L \gamma(Z)
     &\overset{\alpha^L_{\gamma(X), \gamma(Y), \gamma(Z)}}{\longrightarrow}&
    \gamma(X) \otimes^L (\gamma(Y) \otimes^L \gamma(Z))
    \\
    {}^{\mathllap{\mu^{-1}\cdot (\mu^{-1} \times id)}}\uparrow
      &&
    \uparrow^{\mu^{-1} \cdot (id\times \mu^{-1})}
    \\
    \gamma( (X \otimes Y) \otimes Z )
     &\underset{\gamma(\alpha)}{\longrightarrow}&
   \gamma(X \otimes (Y \otimes Z))
  }
  \,.
$$

This is just the [[coherence law]] for the the compatibility of the [[monoidal functor]] $\mu$ with the associators.

Similarly consider now the [[unitors]].

The essential uniqueness of the derived functors gives that the left derived functor of $1\otimes (-)$ is $\gamma(1)\otimes^L (-)$

$$
  \array{
    \mathcal{C}_c
      &\overset{1 \otimes (-)}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{\gamma}}\downarrow
      &&
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C})
      &\underset{\mathbb{L}(1 \otimes (-))}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \;\;\;\;\;\simeq
  \;\;\;\;\;
  \array{
    \mathcal{C}_c
      &\overset{(1,id)}{\longrightarrow}&
    \mathcal{C}_c \times \mathcal{C}_c
     &\overset{\otimes}{\longrightarrow}&
   \mathcal{C}
   \\
   {}^{\mathllap{\gamma}}\downarrow
     &&
   {}^{\mathllap{\gamma \times \gamma}}\downarrow
     &\swArrow_{\mu^{-1}}&
   \downarrow^{\mathrlap{\gamma}}
   \\
   Ho(\mathcal{C})
     &\underset{(\gamma(1),id)}{\longrightarrow}&
   Ho(\mathcal{C}) \times Ho(\mathcal{C})
     &\underset{\otimes^L}{\longrightarrow}&
   Ho(\mathcal{C})
  }
  \,.
$$

Hence the left unitor $\ell$ of $\mathcal{C}$ induces a derived unitor $\ell^L$ by the following factorization

$$
  \array{
    \mathcal{C}_c
       &\overset{1 \otimes (-)}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{\gamma}}\downarrow
      &\swArrow_{\ell}&
    \downarrow^{\mathrlap{\gamma}}
    \\
    \mathcal{C}_c
      &\overset{id}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{\gamma}}\downarrow
      &&
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C})
      &\underset{id}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \;\;\;\;\;\;\;
  =
  \;\;\;\;\;\;\;
  \array{
    \mathcal{C}_c
      &\overset{1 \otimes (-)}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{\gamma}}\downarrow
      &\swArrow_{\mu^{-1}_{1,(-)}}&
    \downarrow^{\mathrlap{\gamma}}
    \\
    Ho(\mathcal{C})
      &\overset{\gamma(1) \otimes^L (-)}{\longrightarrow}&
    Ho(\mathcal{C})
    \\
    {}^{\mathllap{=}}\downarrow
      &\swArrow_{\ell^L}&
    \downarrow^{\mathrlap{=}}
    \\
    Ho(\mathcal{C})
     &\underset{id}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \,.
$$

Moreover, in components this equation of natural isomorphism expresses the coherence law stating the compatibility of the monoidal functor $\mu$ with the unitors.

Similarly for the right unitors.


=--

The restriction to cofibrant objects in prop. \ref{MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory} serves the purpose of giving explicit expressions for the associators and unitors of the derived tensor product $\otimes^L$ and hence to establish the monoidal category structure $(Ho(\mathcal{C}), \otimes^L, \gamma(1))$ on the [[homotopy category of a model category|homotopy category]] of a [[monoidal model category]]. With that in hand, it is natural to ask how the localization functor on all of $\mathcal{C}$ interacts with the monoidal structure:

+-- {: .num_prop #LaxMonoidalLocalizationOfMonoidalModelCategory}
###### Proposition

For $(\mathcal{C}, \otimes, 1)$ a [[monoidal model category]] (def. \ref{MonoidalModelCategory}) then the [[localization]] functor to its monoidal [[homotopy category of a model category|homotopy category]] (prop. \ref{MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}) is a [[lax monoidal functor]]

$$
  \gamma
   \;\colon\;
  (\mathcal{C}, \otimes, 1)
    \longrightarrow
  (Ho(\mathcal{C}), \otimes^L, \gamma(1))
  \,.
$$

=--

The explicit **proof** of prop. \ref{LaxMonoidalLocalizationOfMonoidalModelCategory} is tedious. An abstract proof using tools from homotopical [[2-category theory]] is [here](monoidal+model+category#LocalizationFunctorIsLaxMonoidal).

+-- {: .num_defn #MonoidalQuillenAdjunction}
###### Definition

Given [[monoidal model categories]] $(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D}, \otimes_{\mathcal{D}}, 1_{\mathcal{D}})$ (def. \ref{MonoidalModelCategory}) with cofibrant [[tensor units]] $1_{\mathcal{C}}$ and $1_{\mathcal{D}}$, then a **[[strong monoidal Quillen adjunction]]** between them is a [[Quillen adjunction]]

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

such that $L$ (hence equivalently $R$) has the structure of a [[strong monoidal functor]].

=--

+-- {: .num_prop #StrongMonoidalDerivedFunctorFromStrongMonoidalQuillenAdjunction}
###### Proposition

Given a [[strong monoidal Quillen adjunction]] (def. \ref{MonoidalQuillenAdjunction})

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$


between [[monoidal model categories]] $(\mathcal{C}, \otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D}, \otimes_{\mathcal{D}}, 1_{\mathcal{D}})$ with cofibrant [[tensor units]] $1_{\mathcal{C}}$ and $1_{\mathcal{D}}$, then the  [[left derived functor]] of $L$ canonically becomes a [[strong monoidal functor]] between [[homotopy category of a model category|homotopy categories]]

$$
  \mathbb{L}L
  \;\colon\;
  (Ho(\mathcal{C}), \otimes_{\mathcal{C}}, \gamma(1)_{\mathcal{C}})
   \longrightarrow
  (Ho(\mathcal{D}), \otimes_{\mathcal{D}}, \gamma(1)_{\mathcal{D}})
  \,.
$$

=--

+-- {: .proof}
###### Proof

As in the proof of prop. \ref{MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}, consider the following pasting composite of commuting diagams:


$$
  \array{
    \mathcal{D}_c \times \mathcal{D}_c
      &\overset{\otimes_{\mathcal{D}}}{\longrightarrow}&
    \mathcal{D}_c
      &\overset{L}{\longrightarrow}&
    \mathcal{C}_c
    \\
    {}^{\mathllap{=}}\downarrow
      &&
        \swArrow_{\simeq}
      &&
    \downarrow^{\mathrlap{=}}
    \\
    \mathcal{D}_c \times \mathcal{D}_c
      &\overset{L \times L}{\longrightarrow}&
    \mathcal{C}_c \times \mathcal{C}_c
      &\overset{\otimes_{\mathcal{C}}}{\longrightarrow}&
    \mathcal{C}_c
    \\
    ^{\mathllap{\gamma_{\mathcal{D}} \times \gamma_{\mathcal{D}}}}\downarrow
      &&
    \downarrow^{\mathrlap{\gamma_{\mathcal{C}} \times \gamma_{\mathcal{C}} }}
      &&
    \downarrow^{\gamma_{\mathcal{C}}}
    \\
    Ho(\mathcal{D}) \times Ho(\mathcal{D})
      &\underset{\mathbb{L}L \times \mathbb{L}L}{\longrightarrow}&
    Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\underset{\otimes^L_{\mathcal{C}}}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \;\;\;\;\;
   \simeq
  \;\;\;\;\;
  \array{
     \mathcal{D}_c \times \mathcal{D}_c
       &\overset{\otimes_{\mathcal{D}}}{\longrightarrow}&
     \mathcal{D}_c
       &\overset{L}{\longrightarrow}&
     \mathcal{C}_c
     \\
    \\
    ^{\mathllap{\gamma_{\mathcal{D}} \times \gamma_{\mathcal{D}}}}\downarrow
      &&
    \downarrow^{\mathrlap{\gamma_{\mathcal{D}}  }}
      &&
    \downarrow^{\gamma_{\mathcal{C}}}
    \\
    Ho(\mathcal{D}) \times Ho(\mathcal{D})
      &\overset{\otimes^L_{\mathcal{D}}}{\longrightarrow}&
    Ho(\mathcal{D})
      &\overset{\mathbb{L}L}{\longrightarrow}&
    Ho(\mathcal{C})
    \\
    {}^{\mathllap{=}}\downarrow
      && \swArrow_{\simeq}&&
    \downarrow^{\mathrlap{=}}
    \\
    Ho(\mathcal{D}) \times Ho(\mathcal{D})
      &\underset{\mathbb{L}L \times \mathbb{L}L}{\longrightarrow}&
    Ho(\mathcal{C}) \times Ho(\mathcal{C})
      &\underset{\otimes^L_{\mathcal{C}}}{\longrightarrow}&
    Ho(\mathcal{C})
  }
  \,.
$$

On the top left we have the natural transformation that exhibits $L$ as a [[strong monoidal functor]]. By universality of [[localization]] and [[derived functors]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) this induces the unique factorization through the natural transformation on the bottom right. This exhibits strong monoidal structure on the [[left derived functor]] $\mathbb{L}L$.


=--


With some general monoidal homotopy theory established, we now discuss that structured spectra indeed constitute an example. The version of the following theorem for the stable model structure of actual interest is theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom} further below.

+-- {: .num_theorem #MonoidalStrictModelStructure}
###### Theorem

1. The [[classical model structure on pointed topological spaces]] equipped with the [[smash product]] is a [[monoidal model category]]

   $$
     ((Top^{\ast/}_{cg})_{Quillen}, \wedge, S^0)
     \,.
   $$

1. Let $Dia\in \{Top^{\ast/}_{cg,fin}, Orth, Sym\}$. The strict model structures on [[structured spectra]] modeled on $Dia$ from theorem \ref{StrictModelStructureOnDiagramSpectra} equipped with the [[symmetric monoidal smash product of spectra]]  (def. \ref{FinitePointedCWComplexes}, def. \ref{SsymModuleSymmetricSpectra}) is a [[monoidal model category]] (def. \ref{MonoidalModelCategory})

   $$
     \left(
       \mathbb{S}_{dia}Mod_{strict},\;
       \wedge = \otimes_{\mathbb{S}_{dia}}
       ,\;
       \mathbb{S}_{dia}
     \right)
     \,.
   $$


=--

([MMSS 00, theorem 12.1 (iii) with prop. 12.3](#MMSS00))


+-- {: .proof}
###### Proof

By cofibrant generation of both model structures ([this theorem](Introduction+to+Stable+homotopy+theory+--+P#CofibrantGenerationOfPointedTopologicalSpaces) and prop. \ref{CofibrantGenerationOfStrictModelStructure}) it is sufficient to check the [[pushout-product axiom]] on generating (acylic) cofibrations (this is as in the proof of [this proposition](Introduction+to+Stable+homotopy+theory+--+P#PushoutProductInTopCGSendsCofCofToCof)).

Those of $Top^{\ast/}_{cg}$ are as recalled in def. \ref{StableGeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}. These satisfy ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#PushoutProductOfITopwithITopAndJTop)) the relations

$$
  i_{k_1} \Box i_{k_2} = i_{k_1 + k_2}
$$

and

$$
  i_{k_1} \Box j_{k_2} = j_{k_1 + k_2}
  \,.
$$

This shows that

$$
  I_{Top^{\ast/}}
    \Box_{\otimes_{\mathbb{S}_{dia}}}
  I_{Top^{\ast/}}
    \subset
  I_{Top^{\ast/}}
$$

and

$$
  I_{Top^{\ast/}}
    \Box_{\otimes_{\mathbb{S}_{dia}}}
  J_{Top^{\ast/}}
    \subset
  J_{Top^{\ast/}}
$$

which implies the [[pushout-product axiom]] for $Top^{\ast/}_{cg}$. (However the [[monoid axiom]] (def.\ref{MonoidAxiom}) is problematic.)


Now by def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} the generating (acyclic) cofibrations of $\mathbb{S}_{dia}Mod_{strict}$ are of the form $F^{dia}_n (i_k)_+$ and $F^{dia}_n (j_k)_+$, respectively. By prop. \ref{SmashProductOfFreeSpectra} these satisfy

$$
  F_{n_1} (i_{k_1})_+ \; \Box_{\wedge} \; F_{n_2} (i_{k_2})_+
  \;\simeq\;
  F_{n_1 + n_2} ( i_{k_1} \Box_{\wedge} i_{k_2} )_+
$$

and

$$
  F_{n_1} (i_{k_1})_+ \; \Box \; F_{n_2} (j_{k_2})_+
  \;\simeq\;
  F_{n_1 + n_2} ( i_{k_1} \Box j_{k_2} )_+
  \,.
$$

Hence with the previous set of relations this shows that

$$
  I^{strict}_{dia}
    \Box_{\otimes_{\mathbb{S}_{dia}}}
  I^{strict}_{dia}
    \subset
  I^{strict}_{dia}
$$

and

$$
  I^{strict}_{dia}
    \Box_{\otimes_{\mathbb{S}_{dia}}}
  J^{strict}_{dia}
    \subset
  J^{strict}_{dia}
$$

and so the [[pushout-product axiom]] follows also for
$\mathbb{S}_{dia}Mod_{strict}$.

It is clear that in both cases the [[tensor unit]] is cofibrant: for $Top^{\ast/}_{cg}$ the tensor unit is the [[0-sphere]], which clearly is a [[CW-complex]] and hence cofibrant. For $\mathbb{S}_{dia}Mod$ the tensor unit is the standard [[sphere spectrum]], which, by prop. \ref{ExplicitExpressionForFreeSpectra} is the [[free structured spectrum]] (def. \ref{FreeStructuredSpectrum}) on the 0-sphere

$$
  \mathbb{S}_{dia} \simeq F^{dia}_0(S^0)
  \,.
$$

Now the free structured spectrum functor is a left Quillen functor (prop. \ref{SuspensionSpectrumStructuredStrictQuillenAdjunction}) and hence $\mathbb{S}_{dia}$ is cofibrant.


=--








### Suspension and looping

For the strict [[model structure on topological sequential spectra]], forming [[suspension spectra]] consitutes a [[Quillen adjunction]] $(\Sigma^\infty \dashv \Omega^\infty)$ with the [[classical model structure on pointed topological spaces]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#SigmaInfinityIsQuillenOnStrictModelStructureOnSequential)) which is the precursor of the [[stabilization]] adjunction involving the [[stable model category|stable model structure]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory)). Here we briefly discuss the lift of this strict adjunction to [[structured spectra]].



+-- {: .num_prop #SuspensionSpectrumStructuredStrictQuillenAdjunction}
###### Proposition

Let $Dia \in \{Top^{\ast/}_{cg,fin}, Orth, Sym, Seq\}$ be one of the shapes of structured spectra from def. \ref{TopologicalDiagramCategoriesForSpectra}.

For every $n \in \mathbb{N}$, the functors $Ev^{dia}_n$ of extracting the $n$th component space of a structured spectrum, and the functors $F_n^{dia}$ of forming the [[free structured spectrum]] in degree $n$ (def. \ref{FreeStructuredSpectrum}) constitute a [[Quillen adjunction]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenAdjunction)) between the strict model structure on structured spectra from theorem \ref{StrictModelStructureOnDiagramSpectra} and the [[classical model structure on pointed topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnCompactlyGeneratedTopologicalSpaces), [prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)):

$$
  \mathbb{S}_{dia}Mod_{strict}
    \underoverset
      {\underset{Ev^{dia}_n}{\longrightarrow}}
      {\overset{F^{dia}_n}{\longleftarrow}}
      {\bot}
  (Top^{\ast/}_{cg})_{Quillen}
  \,.
$$

For $n = 0$ and writing $\Sigma_{dia}^\infty \coloneqq F^{dia}_0$ and $\Omega_{dia}^\infty \coloneqq Ev^{dia}_0$, $\Sigma^\infty_{dia}$ this yields a [[strong monoidal Quillen adjunction]] (def. \ref{MonoidalQuillenAdjunction})

$$
  \mathbb{S}_{dia}Mod_{strict}
    \underoverset
      {\underset{\Omega_{dia}^\infty}{\longrightarrow}}
      {\overset{\Sigma_{dia}^\infty}{\longleftarrow}}
      {\bot}
  (Top^{\ast/}_{cg})_{Quillen}
  \,.
$$

Moreover, these Quillen adjunctions factor as

$$
  (\Sigma^\infty_{dia}
    \dashv
  \Omega^\infty_{dia})
   \;\colon\;
  \mathbb{S}_{dia}Mod(Top_{cg})_{strict}
   \underoverset
     {\underset{seq^\ast}{\longrightarrow}}
     {\overset{seq_!}{\longleftarrow}}
     {\bot}
   SeqSpec(Top_{cg})_{strict}
    \underoverset
      {\underset{\Omega^\infty}{\longrightarrow}}
      {\overset{\Sigma^\infty}{\longleftarrow}}
      {\bot}
   (Top^{\ast/}_{cg})
$$

where the Quillen adjunction $(seq_! \dashv seq^\ast)$ is that from theorem \ref{StrictModelStructureOnDiagramSpectra} and where $(\Sigma^\infty \dashv \Omega^\infty)$ is the suspension spectrum adjunction for sequential spectra ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#SigmaInfinityIsQuillenOnStrictModelStructureOnSequential)).

=--

+-- {: .proof}
###### Proof

By the very definition of the [[projective model structure on functors]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#ProjectiveModelStructureOnTopologicalFunctors)) it is immediate that $Ev_n^{dia}$ preserves fibrations and weak equivalences, hence it is a right Quillen functor. $F^{dia}_n$ is its left adjoint by definition.

That $\Sigma^\infty_{dia}$ is a [[strong monoidal functor]] is part of the statement of prop. \ref{SmashProductOfFreeSpectra}.

Moreover, it is clear from the definitions that

$$
  \Omega^\infty_{dia} \simeq \Omega^\infty \circ seq^\ast
  \,,
$$

hence the last statement follows by uniqueness of adjoints.

=--

+-- {: .num_remark #SummarySituationForStrictModelStructure}
###### Remark

In summary,  we have established the following situation. There is a [[commuting diagram]] of [[Quillen adjunctions]] of the form

$$
  \array{
    (Top^{\ast/}_{cg})_{Quillen}
      &
      \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
      &
    (Top^{\ast/}_{cg})_{Quillen}
    \\
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
      &&
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
    \\
    SeqSpec(Top_{cg})_{strict}
     &
      \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
     &
    SeqSpec(Top_{cg})_{strict}
    \\
    {}^{\mathllap{dia_!}}\downarrow \dashv \uparrow^{\mathrlap{dia^\ast}}
      &&
    {}^{\mathllap{dia_!}}\downarrow \dashv \uparrow^{\mathrlap{dia^\ast}}
    \\
    \mathbb{S}_{dia}Mod_{strict}
      &&
    \mathbb{S}_{dia}Mod_{strict}
  }
  \,.
$$

The top square stabilizes to the actual [[stable homotopy theory]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory)). On the other hand, the top square does not reflect the [[symmetric monoidal smash product of spectra]] (by remark \ref{RestrictionsOfExcisiveSphere}). But the total vertical composite $\Sigma^\infty_{dia} = dia_! \Sigma^\infty$ does, in that it is a [[strong monoidal Quillen adjunction]] (def. \ref{MonoidalQuillenAdjunction}) by prop. \ref{SuspensionSpectrumStructuredStrictQuillenAdjunction}.

Hence to obtain a [[stable model category]] which is also a [[monoidal model category]] with respect to the [[symmetric monoidal smash product of spectra]], it is now sufficient to find such a monoidal model structure on $\mathbb{S}_{dia}Mod$ such that $(seq_! \dashv seq^\ast)$ becomes a [[Quillen equivalence]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenEquivalence))


=--


This we now turn to in the section _[The stable model structure on structured spectra](#MonoidalStableModelStructure)_.






## The stable model structure on structured spectra
 {#MonoidalStableModelStructure}



+-- {: .num_theorem #OrthogonalSpectraStableModelStructure}
###### Theorem

The category $OrthSpec(Top_{cg})$ of [[orthogonal spectra]] carries a [[model category]] structure ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) where

* the weak equivalences $W_{stable}$ are the [[stable weak homotopy equivalences]] (def. \ref{StableOrthStructureClassesOfMorphisms});

* the cofibrations $Cof_{stable}$ are the cofibrations of the strict model stucture of prop. \ref{StrictModelStructureOnDiagramSpectra};

* the fibrant objects are precisely the [[Omega-spectra]] (def. \ref{StableOrthStructureClassesOfMorphisms}).

Moreover, this is a [[cofibrantly generated model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CofibrantlyGeneratedModelCategory)) with generating (acyclic) cofibrations the sets $I^{stable}$ ($J^{stable}$) from def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}.

=--

([Mandell-May 02, theorem 4.2](#May02))

We give the **proof** [below](#StableModelStructureOnDiagramSpectraProof), after





### Proof of the model structure

The generating cofibrations and acylic cofibrations are going to be the those induced via [[tensoring]] of representables from the [[classical model structure on topological spaces]] (giving the strict model structure), together with an additional set of morphisms to the generating acylic cofibrations that will force fibrant objects to be Omega-spectra. To that end we need the following little preliminary.



+-- {: .num_defn #ResolutionOfCorepresentationOfAdjunctsOfStructureMaps}
###### Definition

For $n \in \mathbb{N}$ let

$$
  \lambda_n
    \colon
   F_{n+1}S^1
     \overset{k_n }{\longrightarrow}
   Cyl(\lambda_n)
    \stackrel{}{\longrightarrow}
   F_n S^0
$$

be the factorization as in the [[factorization lemma]] of the morphism $\lambda_n$ of lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists} through its [[mapping cylinder]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ConeAndMappingCylinder)) formed with respect to the standard [[cylinder spectrum]] $(F_{n+1}S^1) \wedge (I_+)$:


=--

Notice that:

+-- {: .num_lemma}
###### Lemma

The factorization in def. \ref{ResolutionOfCorepresentationOfAdjunctsOfStructureMaps} is through a cofibration followed followed by a left [[homotopy equivalence]] in $\mathbb{S}_{dia}Mod(Top_{cg})_{strict}$

=--

+-- {: .proof}
###### Proof


Since the cell $S^1$ is cofibrant in $(Top^{\ast/}_{cg})_{Quillen}$, and since $F_{n+1}(-)$ is a left Quillen functor by prop. \ref{SuspensionSpectrumStructuredStrictQuillenAdjunction},
the free spectrum $F_{n+1}S^1$ is cofibrant in $\mathbb{S}_{dia}Mod(Top_{cg})_{strict}$. Therefore lemma \ref{StandardReducedCylinderOnStructuredSpectrumIsGood} says that its standard [[cylinder spectrum]] is a good [[cylinder object]] and then the [[factorization lemma]] ([lemma](Introduction+to+Stable+homotopy+theory+--+P#FactorizationLemma)) says that $k_n$ is a cofibration. Moreover, the morphism out of the standard mapping cylinder is a homotopy equivalence, with homotopies induced under tensoring from the standard homotopy contracting the standard cylinder.


=--


With this we may state the classes of morphisms that are going to be shown to be the classes of generating (acyclic) cofibrations for the stable model structures:

+-- {: .num_defn #StableGeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}
###### Definition

Recall the sets of generating (acyclic) cofibrations of the strict model structre def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}. Set

$$
  I^{stable}_{\mathbb{S}_{dia}Mod(Top_{cg})}
    \;\coloneqq\;
  I^{strict}_{\mathbb{S}_{dia}Mod(Top_{cg})}
$$

and

$$
  J^{stable}_{\mathbb{S}_{dia}Mod(Top_{cg})}
    \;\coloneqq\;
  J^{strict}_{\mathbb{S}_{dia}Mod(Top_{cg})}
  \;\sqcup\;
  \{
    k_n \Box i_+
  \}_{{n \in \mathbb{N}} \atop {i \in I}}
$$

for the [[disjoint union]] of the strict acyclic generating cofibration with the [[pushout products]] under smash tensoring of the resolved maps $k_n$ from def. \ref{ResolutionOfCorepresentationOfAdjunctsOfStructureMaps} with the elements in $I$.

=--

([MMSS 00, def.6.2, def. 9.3](#MMSS00))


+-- {: .num_lemma #ElementsOfKAreStableEquivalencesAndStrictCofibrations}
###### Lemma

Let $Dia \in \{Top^{\ast/}_{cg,fin}, Orth, Seq\}$ (but not $Sym$). Then every element in $J^{stable}_{\mathbb{S}_{dia}Mod(Top_{cg})}
$ (def. \ref{StableGeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) is both:

1. a cofibration with respect to the strict model structure (prop. \ref{StrictModelStructureOnDiagramSpectra});

1. a [[stable weak homotopy equivalence]] (def. \ref{StableOrthStructureClassesOfMorphisms}).

=--

+-- {: .proof}
###### Proof

First regarding strict cofibrations:

By the [[Yoneda lemma]], the elements in $J$ have [[right lifting property]] against the strict fibrations, hence in particular they are strict cofibrations. Moreover, by [[Joyal-Tierney calculus]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#JoyalTierneyCalculus)), $k_n \Box i_+$ has left lifting against any acyclic strict fibration $f$ precisely if $k_n$ has left lifting against $f^{\Box i}$. By prop. \ref{PushoutProductWithRespectToSmashTensoringSatisfiesEnrichedModelCategoryAxioms} the latter is still a strict acyclic fibration. Since $k_n$ by construction is a strict cofibration, the lifting follows and hence also $k_n \Box i_+$ is a strict cofibration.

Now regarding stable weak homotopy equivalences:

The morphisms in $J^{strict}$ by design are strict weak equivalences, hence they are in particular stable weak homotopy equivalences. The morphisms $k_n$ are stable weak homotopy equivalences by lemma \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences} and by [[two-out-of-three]].

To see that also the pushout products $k_n \Box (i_n)_+$ are stable weak homotopy equivalences. (e.g. [Mandell-May 02, p.46](#May02)):

First $k_n \wedge (S^{n-1})_+$ is still a stable weak homotopy equivalence, by lemma. \ref{SmashTensoringWithFiniteCellComplexPreservesSWHE}.

Moreover, observe that $dom(k_n)\wedge i_+$ is degreewise a [[relative cell complex]] inclusion, hence degreewise a cofibration in the [[classical model structure on pointed topological spaces]]. This follows from lemma \ref{S0FreeSpectraCellDegreewise}, which says that $dom(k_n) \wedge i_+$ is degreewise the [[smash product]] of a [[CW complex]] with $i_+$, and from the fact that smashing with CW-complexes is a left Quillen functor $(Top^{\ast/}_{cg})_{Quillen} \longrightarrow (Top^{\ast/}_{cg})_{Quillen}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#HomProductAdjunctionForCofibrantObjectInPointedTopCGIsQuillen)) and hence preserves cofibrations.

Altogether this implies by lemma \ref{PushoutOfSWHEAlongDegreewiseCofibration} that the  pushout of the stable weak homotopy equivalence $k_n \wedge (S^{n-1})_+$ along the degreewise cofibration $dom(k_n)\wedge i_+$ is still a stable weak homtopy equivalence, and so the pushout product $k_n \Box i_+$ is, too, by [[two-out-of-three]].


=--


The point of the class $K$ in def. \ref{GeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra} is to make the following true:

+-- {: .num_lemma #KInjectivesAreAcyclicCofibrations}
###### Lemma

A morphism $f \colon X \to Y$ in $\mathbb{S}_{dia} Mod$ is a $J^{stable}$-[[injective morphism]] (for $K$ from def. \ref{StableGeneratingAndGeneratingAcyclicCofibrationsForDiagramSpectra}) precisely if

1. it is a fibration in the strict model structure (hence degreewise a fibration);

1. for all $n \in \mathbb{N}$ the [[commuting squares]] of structure map compatibility on the underlying [[sequential spectra]]

   $$
     \array{
       X_n  &\overset{\tilde\sigma}{\longrightarrow}& \Omega X_{n+1}
       \\
       \downarrow && \downarrow
       \\
       Y_n &\underset{\tilde \sigma}{\longrightarrow}& \Omega Y_{n+1}
     }
   $$

   are [[homotopy pullbacks]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyPullback)).

=--

([MMSS 00, prop. 9.5](#MMSS00))

+-- {: .proof}
###### Proof

By prop \ref{CofibrantGenerationOfStrictModelStructure}, lifting against $J^{strict}$ alone characterizes strict fibrations, hence degreewise fibrations. Lifting against the remaining [[pushout product]] morphism $k_n \Box i_+$ is, by [[Joyal-Tierney calculus]], equivalent to left lifting $i_+$ against the dual pullback product of $f^{\Box k_n}$, which means that $f^{\Box k_n}$ is a weak homotopy equivalence. But by construction of $k_n$ and by lemma \ref{CorepresentingOfAdjunctsOfStructureMapsExists}, $f^{\Box k_n}$ is the comparison morphism into the homotopy pullback under consideration.

=--

+-- {: .num_cor #KInjectivesObjectsAreOmegaSpectra}
###### Corollary

The $J^{stable}$-[[injective objects]] are precisely the [[Omega-spectra]] (def. \ref{StableOrthStructureClassesOfMorphisms}).

=--


+-- {: .num_lemma #KInjectiveStableEquivalencesAreStrictEquivalences}
###### Lemma

A morphism in $\mathbb{S}_{dia}Mod$ which is both

1. a stable weak homotopy equivalence (def. \ref{StableOrthStructureClassesOfMorphisms});

1. a $J^{stable}$-[[injective morphisms]]

is an acyclic fibration in the strict model structure of prop. \ref{StrictModelStructureOnDiagramSpectra}, hence is degreewise a [[weak homotopy equivalence]] and [[Serre fibration]] of topological spaces;

=--

([MMSS 00, corollary 9.8](#MMSS00))

+-- {: .proof}
###### Proof

Let $f\colon X \to B$ be both a stable weak homotopy equivalence as well as a $J^{stable}$-injective morphism. Since $J^{stable}$ contains, by prop. \ref{CofibrantGenerationOfStrictModelStructure}, the generating acyclic cofibrations for the strict model structure of prop. \ref{StrictModelStructureOnDiagramSpectra}, $f$ is in particular a strict fibration, hence a degreewise fibration. Therefore the fiber $F$ of $f$ is its [[homotopy fiber]] in the strict model structure.


Hence by lemma \ref{DegreewiseLESofHomotopyGroupsInducedStableLES} there is an [[exact sequence]] of [[stable homotopy groups]] of the form

$$
  \pi_{\bullet+1}(X)
    \overset{\pi_{\bullet+1}(f)}{\longrightarrow}
  \pi_{\bullet+1}(Y)
    \overset{}{\longrightarrow}
  \pi_\bullet(F)
    \longrightarrow
  \pi_\bullet(X)
    \overset{\pi_\bullet(f)}{\longrightarrow}
  \pi_\bullet(Y)
  \,.
$$

By exactness and by the assumption that $\pi_\bullet(f)$ is an isomorphism, this implies that $\pi_\bullet(F) \simeq 0$, hence that $F\to \ast$ is a stable weak homotopy equivalence.



Observe also that $F$, being the pullback of a $J^{stable}$-injective morphisms (by the standard [closure properties](injective+or+projective+morphism#ClosureProperties)) is a $J^{stable}$-[[injective object]], so that by corollary \ref{KInjectivesObjectsAreOmegaSpectra} $F$ is an Omega-spectrum. Since stable weak homotopy equivalences between Omega-spectra are already degreewise weak homotopy equivalences, together this says that $F \to \ast$ is a weak equivalence in the strict model structure, hence degreewise a [[weak homotopy equivalence]]. From this the [[long exact sequence of homotopy groups]] implies that $\pi_{\bullet \geq 1}(f_n)$ is a [[weak homotopy equivalence]] for all $n$ and for each homotopy group in positive degree.


To deduce the remaining case that also $\pi_0(f_0)$ is an isomorphism, observe that, by assumption of $J^{stable}$-injectivity, lemma \ref{KInjectivesAreAcyclicCofibrations} gives that $f_n$ is a homotopy pullback (in topological spaces) of $\Omega (f_{n+1})$. But, by the above, $\Omega (f_{n+1})$ is a weak homotopy equivalence, since $\pi_\bullet(\Omega(-)) = \pi_{\bullet+1}(-)$. Therefore $f_n$ is the homotopy pullback of a weak homotopy equivalence and hence itself a weak homotopy equivalence.

=--

+-- {: .num_lemma #RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations}
###### Lemma

The [[retracts]] of $J^{stable}$-[[relative cell complexes]] are precisely the morphisms which are

1. stable weak homotopy equivalences (def. \ref{StableOrthStructureClassesOfMorphisms}),

1. as well as cofibrations with respect to the strict model structure  of prop. \ref{StrictModelStructureOnDiagramSpectra}.

=--

([MMSS 00, prop. 9.9 (i)](#MMSS00))


+-- {: .proof}
###### Proof

Since all elements of $J^{stable}$ are stable weak homotopy equivalences as well as strict cofibrations by lemma \ref{ElementsOfKAreStableEquivalencesAndStrictCofibrations}, it follows that every retract of a relative $K$-cell complex has the same property.

In the other direction, if $f$ is a stable weak homotopy equivalence and a strict cofibration, by the [[small object argument]] it factors $f \colon \stackrel{i}{\to}\stackrel{p}{\to}$ as a relative $J^{stable}$-cell complex $i$ followed by a $J^{stable}$-[[injective morphism]] $p$. By the previous statement $i$ is a stable weak homotopy equivalence, and so by assumption and by [[two-out-of-three]] so is $p$. Therefore lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} implies that $p$ is a strict acyclic fibration. But then the assumption that $f$ is a strict cofibration means that it has the [[left lifting property]] against $p$, and so the [[retract argument]] implies that $f$ is a retract of the relative $K$-cell complex $i$.


=--

+-- {: .num_cor #KInjectivesAreIndeedTheStableFibrations}
###### Corollary

The $J^{stable}$-[[injective morphisms]] are precisely those which are
[[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable weak homotopy equivalences.

=--

([MMSS 00, prop. 9.9 (ii)](#MMSS00))


+-- {: .num_lemma #StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations}
###### Lemma

A morphism in $\mathbb{S}_{dia}Mod$ (for $Diq \neq Sym$) is both

1. a stable weak homotopy equivalence (def. \ref{StableEquivalencesForDiagramSpectra})

1. [[injective morphism|injective]] with respect to the cofibrations of the strict model structure that are also stable weak homotopy equivalences;

precisely if it is an acylic fibration in the strict model structure of theorem \ref{StrictModelStructureOnDiagramSpectra}.

=--

([MMSS 00, prop. 9.9 (iii)](#MMSS00))

+-- {: .proof}
###### Proof

Every acyclic fibration in the strict model structure is injective with respect to strict cofibrations by the strict model structure; and it is a clearly a stable weak homotopy equivalence.

Conversely, a morphism injective with respect to strict cofibrations that are stable weak homotopy equivalences is a $J^{stable}$-[[injective morphism]] by corollary \ref{KInjectivesAreIndeedTheStableFibrations}, and hence if it is also a stable equivalence then by lemma \ref{KInjectiveStableEquivalencesAreStrictEquivalences} it is a strict acylic fibration.

=--

+-- {: .proof #StableModelStructureOnDiagramSpectraProof}
###### Proof
(of theorem \ref{OrthogonalSpectraStableModelStructure})

The non-trivial points to check are the two [[weak factorization systems]].

That $(cof_{stable}\cap weq_{stable} \;,\; fib_{stable})$ is a weak factorization system follows from lemma \ref{RetractsOfRelativeKCellComplexesAreTheStableEquivalencesAndStrictCofibrations} and the [[small object argument]].

By lemma \ref{StableAcyclicFibrationsAreEquivalentlyStrictAcyclicFibrations} the stable acyclic fibrations are equivalently the strict acyclic fibrations and hence the weak factorization system $(cof_{stable} \;,\; fib_{stable} \cap we_{stable})$ is identified with that of the strict model structure $(cof_{strict} \;,\; fib_{strict} \cap we_{strict})$.

=--





### Stability of the homotopy theory

We show now that the [[model structure on orthogonal spectra]] $OrthSpec(Top_{cg})_{stable}$ from theorem \ref{OrthogonalSpectraStableModelStructure} is [[Quillen equivalence|Quillen equivalent]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenEquivalence)) to the stable [[model structure on topological sequential spectra]] $SeqSpec(Top_{cg})_{stable}$ ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentialSpectraIsModelCategory)), hence that they model the same [[stable homotopy theory]].

+-- {: .num_theorem #SequentialSpectraQuillenEquivalence}
###### Theorem

The [[free-forgetful adjunction]] $(seq_! \dashv seq^\ast)$ of def. \ref{TopologicalDiagramCategoriesForSpectra} and theorem \ref{StrictModelStructureOnDiagramSpectra} is a [[Quillen equivalence]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenEquivalence)) between the stable [[model structure on topological sequential spectra]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentialSpectraIsModelCategory)) and the stable model structure on orthogonal spectra from theorem \ref{OrthogonalSpectraStableModelStructure}.

$$
  OrthSpec(Top_{cg})_{stable}
    \underoverset
      {\underset{seq^\ast}{\longrightarrow}}
      {\overset{seq_!}{\longleftarrow}}
      {\simeq_{Quillen}}
  SeqSpec(Top_{cg})_{stable}
$$

=--

([MMSS 00, theorem 10.4](#MMSS00))

+-- {: .proof}
###### Proof

Since the [[forgetful functor]] $seq^\ast$ "creates weak equivalences",
in that a morphism of orthogonal spectra is a weak equivalence precisely if the underlying morphism of sequential spectra is (by def. \ref{StableOrthStructureClassesOfMorphisms}) it is sufficient to show (by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#InCaseTheRightAdjointCreatesWeakEquivalences)) that for every cofibrant sequential spectrum $X$, the [[adjunction unit]]

$$
  X
    \longrightarrow
  seq^\ast seq_! X
$$

is a [[stable weak homotopy equivalence]].

By [[cofibrantly generated model category|cofibrant generation]] of the stable [[model structure on topological sequential spectra]] $SeqSpec(Top_{cg})_{stable}$ ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#AlternativeStableModelStructureOnSequentialSpectraIsModelCategory)) every cofibrant sequential spectrum is a [[retract]] of an $I_{seq}^{stable}$-[[relative cell complex]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GeneratingAndGeneratingAcyclicCofibrationsForSeqSpecStable), [def.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalCellComplex)), where

$$
  I^{stable}_{seq}
  \;=\;
  \left\{
    F_{n_1} S^{n_2-1}_+
      \overset{F_{n_1} (i_{n_2})_+ }{\longrightarrow}
    F_{n_1} D^{n_2}_+
  \right\}
  \,.
$$

Since $seq_!$ and $seq^\ast$ both preserve [[colimits]] ($seq^\ast$ because it evaluates at objects and colimits in the diagram category $OrthSpec$ are computed objectwise, and $seq_!$ because it is a [[left adjoint]]) we have for $X \simeq \underset{\longrightarrow}{\lim}_i X_i$ a relative $I^{stable}_{seq}$-decompositon of $X$, that $\eta_X \colon X \to seq^\ast seq_! X$ is equivalently

$$
  \underset{\longrightarrow}{\lim}_i \eta_{X_i}
   \;\colon\;
  \underset{\longrightarrow}{\lim}_i X_i
    \longrightarrow
  \underset{\longrightarrow}{\lim}_i seq_! seq^\ast X_i
  \,.
$$

Now observe that the colimits involved in a relative $I^{stable}_{seq}$-complex (the [[coproducts]], [[pushouts]], [[transfinite compositions]]) are all [[homotopy colimits]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#LeftDerivedFunctorOfColimitFunctor)): First, all objects involved are cofibrant. Now for the transfinite composition all the morphisms involved are cofibrations, so that their colimit is a homotopy colimit by [this example](Introduction+to+Stable+homotopy+theory+--+P#ProjectiveModelStructureOnNSequencesOfTopologicalSpaces), while for the pushout one of the morphisms out of the "top" objects is a cofibration, so that this is a [[homotopy pushout]] by ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyPullback)).

It follows that if all $\eta_{X_i}$ are weak equivalences, then so is $\eta = \underset{\longrightarrow}{\lim}_i \eta_{X_i}$.

Unwinding this, one finds that it is sufficient to show that

$$
  \eta_{F_{n_1} S^{n_2}}
  \;\colon\;
  F_{n_1} S^{n_2}_+
    \longrightarrow
  seq^\ast seq_! F_{n_1} S^{n_2}
$$

is a stable weak homotopy equivalence for all $n_1, n_2 \in \mathbb{N}$.

Consider this for $n_2 \geq n_2$. Then there are canonical morphisms

$$
  F_{n_1} S^{n_2} \longrightarrow F_{0} S^{n_2-n_1}
$$

whose components in degree $q \geq n_1$ are the identity. These are the composites of the maps $\lambda_k \wedge S^{k+n_2-n_1}$ for $k \lt n_1$ with $\lambda_n$ from def. \reg{CorepresentationOfAdjunctsOfStructureMaps}. By prop. \ref{AdjunctsOfFreeSpectrumInclusionsAreOrAreNotStableWeakHomotopyEquivalences} also $seq^\ast seq_! \lambda_n$ are weak homotopy equivalences. Hence we have [[commuting diagrams]] of the form

$$
  \array{
    F^{seq}_{n_1} S^{n_2} &\longrightarrow& F_0 S^{n_2-n_1}
    \\
    {}^{\mathllap{\eta}}\downarrow
    &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    seq^\ast F^{orth}_{n_1}S^{n_2-n_1}
      &\longrightarrow&
    seq^\ast F_0^{orth} S^{n_2-n_1}
  }
  \,,
$$

where the horizontal maps are stable weak homotopy equivalences by the previous argument and the right vertical morphism is an isomorphism by the formula in prop. \ref{ExplicitFormOfFreeSpectra}.Hence the left vertical morphism is a stable weak homotopy equivalence by [[two-out-of-three]].

If $n_2 \lt n_1$ then one reduces this to the above case by smashing with $S^{n_1-n_2}$.

=--

+-- {: .num_remark #StableHomotopyCategoryStructuredSpectra}
###### Remark

Theorem \ref{SequentialSpectraQuillenEquivalence} means that the [[homotopy category of a model category|homotopy categories]] of $SeqSpec(Top_{cg})_{stable}$ and $OrthSpec(Top_{cg})_{stable}$ are [[equivalence of categories|equivalent]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ConditionsForQuillenAdjunctionAreIndeedEquivalent)) via

$$
  Ho( OrthSpec(Top_{cg})_{stable} )
   \underoverset
     {\underset{\mathbb{R}seq^\ast}{\longrightarrow}}
     {\overset{\mathbb{L}seq_!}{\longleftarrow}}
     {\simeq}
  Ho( SeqSpec(Top_{cg})_{stable} )
  \,.
$$

Since $SeqSpec(Top_{cg})_{stable}$ is a [[stable model category]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentiaSpectraIsStableModelCategory)) in that the derived suspension looping adjunction is an equivalence of categories, and and since this is a condition only on the [[homotopy category of a model category|homotopy categories]], and since $\mathbb{R}seq^ast$ manifestly preserves the construction of [[loop space objects]], this implies that we have a [[commuting square]] of [[adjoint equivalences]] of homotopy categories

$$
  \array{
    Ho(SeqSpec(Top_{cg})_{stable})
     &
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\simeq}
     &
    Ho(SeqSpec(Top_{cg})_{stable})
    \\
    {}^{\mathllap{\mathbb{L} seq_!}}\downarrow \simeq \uparrow^{\mathrlap{\mathbb{R}seq^\ast}}
      &&
    {}^{\mathllap{\mathbb{L} seq_!}}\downarrow \simeq \uparrow^{\mathrlap{\mathbb{R}seq^\ast}}
    \\
    Ho( OrthSpec(Top_{cg})_{stable} )
      &
      \underoverset
        {\underset{\Omega}{\longrightarrow}}
        {\overset{\Sigma}{\longleftarrow}}
        {\simeq}
      &
    Ho( OrthSpec(Top_{cg})_{stable} )
  }
$$

and so in particular also $OrthSpec(Top_{cg})_{stable}$ is a [[stable model category]].

Due to the vertical equivalences here we will usually not distinguish between these homotopy categories and just speak of the _[[stable homotopy category]]_ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategory))

$$
  Ho(Spectra)
   \coloneqq
  Ho( SeqSpec(Top_{cg})_{stable} )
   \simeq
  Ho( OrthSpec(Top_{cg})_{stable} )
  \,.
$$

=--






### Monoidal model structure

We now discuss that the [[monoidal model category]] structure of the strict [[model structure on orthogonal spectra]] $OrthSpec(Top_{cg})_{strict}$ (theorem \ref{MonoidalStrictModelStructure}) remains intact as we pass to the stable model structure $OrthSpec(Top_{cg})_{stable}$ of theorem \ref{OrthogonalSpectraStableModelStructure}.

+-- {: .num_theorem #StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom}
###### Theorem

The stable model structure $OrthSpec(Top_{cg})_{stable}$ of theorem \ref{OrthogonalSpectraStableModelStructure} equipped with the [[symmetric monoidal smash product of spectra]] (def. \ref{SsymModuleSymmetricSpectra}) is a [[monoidal model category]] (def. \ref{MonoidalModelCategory}) with cofibrant [[tensor unit]]

$$
  (OrthSpec(Top_{cg}),\; \wedge = \otimes_{\mathbb{S}_{orth}},\; \mathbb{S}_{orth}  )
  \,.
$$


=--

([MMSS 00, prop. 12.6](#MMSS00))

+-- {: .proof}
###### Proof

Since $Cof_{stable} = Cof_{strict}$, the fact that the pushout product of two stable cofibrations is again a stable cofibration is part of theorem \ref{MonoidalStrictModelStructure}.

It remains to show that if at least one of them is a [[stable weak homotopy equivalence]] (def. \ref{StableOrthStructureClassesOfMorphisms}), then so is the pushout-product.

Since $OrthSpec(Top_{cg})$ is a [[cofibrantly generated model category]] by theorem \ref{OrthogonalSpectraStableModelStructure} and since it has [[internal homs]] ([[mapping spectra]]) with respect to $\otimes_{\mathbb{S}_{dia}}$ (prop. \ref{DayMonoidalStructureIsClosed}), it suffices (as in the proof of [this prop.](Introduction+to+Stable+homotopy+theory+--+P#PushoutProductInTopCGSendsCofCofToCof)) to check this on generating (acylic) cofibrations, i.e. to check that

$$
  I^{stable}
    \Box_{\otimes}
  J^{stable}
    \subset
  W_{stable} \cap Cof_{stable}
  \,.
$$

Now $I^{\stable} = I^{strict}$ and  $J^{stable} = J^{strict} \sqcup \{ k_n \Box i_+\}$ so that the special case

$$
  \begin{aligned}
    I^{stable} \Box_{\otimes} J^{strict}
    &=
    I^{strict} \Box_{\otimes} J^{strict}
    \\
      &\subset
     W_{strict}\cap Cof_{strict}
     \\
      & \subset
     W_{stable} \cap Cof_{stable}
  \end{aligned}
$$

follows again from the monoidal stucture on the strict model category of theorem \ref{MonoidalStrictModelStructure}.

It hence remains to see that

$$
  I^{strict} \Box_{\otimes} ( k_{n_1} \Box  (i_{n_2})_+ )
  \subset
  W_{stable} \cap Cof_{stable}
$$

for all $n_1, n_2 \in \mathbb{N}$.

By lemma \ref{ElementsOfKAreStableEquivalencesAndStrictCofibrations} $k_n \Box i_+$ is in $Cof_{strict}$ and hence

$$
  I^{strict} \Box_{\otimes} ( k_{n_1} \Box  (i_{n_2})_+ ) \subset Cof_{strict}
$$

follows, once more, from the monoidalness of the strict model structure.

Hence it only remains to show that

$$
  I^{strict} \Box_{\otimes} ( k_{n_1} \Box  (i_{n_2})_+ )
    \subset
  W_{stable}
  \,.
$$

This we now prove by inspection:

By [[two-out-of-three]] applied to the definition of the [[pushout product]], it is sufficient to show that for every $F_{n_3} (i_{n_4})_+$ in $I^{strict}$, the right vertical morphism in the pushout diagram

$$
  \array{
    &\overset{F_{n_3}(i_{n_4})_+ \otimes dom(k_{n_1} \Box (i_{n_2})_+) }{\longrightarrow}&
    \\
    {}^{\mathllap{dom(F_{n_3}(i_{n_4})} \otimes (k_{n_1} \Box (i_{n_2})_+ )}
    \downarrow
      &(po)&
    \downarrow
    \\
    &\longrightarrow&
  }
$$

is a stable weak homotopy equivalence. Since $seq^\ast$ preserves pushouts, we may equivalently check this on the underlying sequential spectra.

Consider first the top horizontal morphism in this square.

We may rewrite it as

$$
  \begin{aligned}
    F_{n_3}(i_{n_4})_+ \otimes (dom(k_{n_1}) \Box (i_{n_2})_+  )
      & \simeq
    F_{n_3}(i_{n_4})_+
      \otimes
    \left(
      F_{n_1}S^0 \wedge S^{n_2-1}_+
        \underset{F_{n_1+1} S^1 \wedge S^{n_2-1}_+}{\sqcup}
      F_{n_1+1}S^1 \wedge D^{n_2}_+
    \right)
    \\
    & \simeq
      F_{n_3}(i_{n_4})_+ \otimes F_{n_1}S^0 \wedge S^{n_2-1}_+
        \underset{F_{n_3}(i_{n_4})_+\otimes F_{n_1+1} S^1 \wedge S^{n_2-1}_+}{\sqcup}
      F_{n_3}(i_{n_4})_+\otimes F_{n_1+1}S^1 \wedge D^{n_2}_+
    \\
    & \simeq
    F_{n_1+n_3} (i_{n_4})_+ \wedge S^{n_2-1}_+
      \underset{F_{n_1+n_3+1} (i_{n_4})_+ \wedge S^{n_2-1}_+ }{\sqcup}
    F_{n_1+n_3+1} (i_{n_4})_+ \wedge S^1 \wedge D^{n_2}_+
  \end{aligned}
  \,,
$$

where we used that $X \otimes (-)$ is a left adjoint and hence preserves colimits, and we used prop. \ref{SmashProductOfFreeSpectra} to evaluate the smash product of free spectra.

Now by lemma \ref{S0FreeSpectraCellDegreewise} the morphism

$$
  F_{n_1 + n_3 + 1} S^{n_4-1}_+ \wedge S^1 \wedge S^{n_2-1}_+
   \longrightarrow
  F_{n_1 + n_3 + 1} S^{n_4-1}_+ \wedge S^1 \wedge D^{n_2}_+
$$

is degreewise the smash product of a CW-complex with a [[relative cell complex]] inclusion, hence is itself degreewise a relative cell complex inclusion, and therefore its pushout

$$
  F_{n+1 + n_3} S^{n_4-1}_+  \otimes  F_{n_1}S^0 \wedge S^{n_2-1}_+
    \longrightarrow
  F_{n_3} (S^{n_4-1})_+ \otimes dom(k_{n_1} \Box (i_{n_2})_+)
$$

is degreewise a retract of a relative cell complex inclusion. But since it is the identity on the smash factor $S^{n_4-1}_+$ in the argument of the free spectra as above, the morphism is degreewise the smash tensoring with $S^{n_4-1}$ of a retract of a relative cell complex inclusion. Since the domain is degreewise a CW-complex by lemma \ref{S0FreeSpectraCellDegreewise}, $F_{n_3} (S^{n_4-1})_+ \otimes dom(k_{n_1} \Box (i_{n_2})_+)$ is degreewise the smash tensoring with $S^{n_4-1}_+$ of a retract of a cell complex.

The same argument applies to the domain of $F_{n_3}(i_4)_+ \otimes (dom(k_n) \Box (i_2)_+)$, and so in conclusion this morphism is degreewise the smash product of a cofibration with a cofibrant object in $(Top^{\ast/}_{cg})_{Quillen}$, and hence is itself degreewise a cofibration.

Now consider the vertical morphism in the above square

The same argument that we just used shows that this is the smash tensoring of the stable weak homotopy equivalence $k_{n_1} \Box (i_{n_2})_+$ with a CW-complex. Hence by lemma \ref{SmashTensoringWithFiniteCellComplexPreservesSWHE} the left vertical morphism is a stable weak homotopy equivalence.

In conclusion, the right vertical morphism is the pushout of a stable weak homotopy equivalence along a degreewise cofibration of pointed topological spaces. Hence lemma \ref{PushoutOfSWHEAlongDegreewiseCofibration} implies that it is itself a stable weak homotopy equivalence.

=--

+-- {: .num_cor #StableMonoidalQuillenSuspensionSpectrumFunctor}
###### Corollary

The [[strong monoidal Quillen adjunction]] (def. \ref{MonoidalQuillenAdjunction}) $(\Sigma^\infty_{orth} \dashv \Omega^\infty_{orth})$ on the strict model structure (prop. \ref{SuspensionSpectrumStructuredStrictQuillenAdjunction}) descends to a [[strong monoidal Quillen adjunction]] on the stable [[monoidal model category]] from theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom}:

$$
  OrthSpec(Top_{cg})_{stable}
   \underoverset
     {\underset{\Omega^\infty_{orth}}{\longrightarrow}}
     {\overset{\Sigma^\infty_{orth}}{\longleftarrow}}
     {\bot}
  (Top^{\ast/}_{cg}, \wedge, S^0)_{Quillen}
  \,.
$$


=--

+-- {: .proof}
###### Proof

The stable model structure $OrthSpec(Top_{cg})_{stable}$ is a [[Bousfield localization of model categories|left Bousfield localization]] of the strict model structure ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#BousfieldLocalizationOfModelCategories)) in that it has the same cofibrations and a larger class of acyclic cofibrations. Hence $\Sigma^\infty_{orth}$ is still a left Quillen functor also to the stable model structure.

=--




##  The monoidal stable homotopy category
 {#TheMonoidalStableHomotopyCategory}

We discuss now the consequences for the [[stable homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategory)) of the fact that by theorem \ref{SequentialSpectraQuillenEquivalence} and theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom} it is equivalently the [[homotopy category of a model category|homotopy category]] of a stable [[monoidal model category]]. This makes the stable homotopy category become a _[[tensor triangulated category]]_ (def. \ref{TensorTriangulatedCG}) below. The abstract structure encoded by this governs much of [[stable homotopy theory]] ([Hovey-Palmieri-Strickland 97](#HoveyPalmieriStrickland97)). In particular it is this structure that gives rise to the $E$-[[Adams spectral sequences]] which we discuss in [[Introduction to Stable homotopy theory -- 2|Part 2]].


+-- {: .num_cor #MonoidalStableHomotopyCategory}
###### Corollary

The [[stable homotopy category]] $Ho(Spectra)$ (remark \ref{StableHomotopyCategoryStructuredSpectra}) inherits the structure of a [[symmetric monoidal category]]

$$
  (Ho(Spectra), \wedge^L, \mathbb{S} \coloneqq \gamma(\mathbb{S}_{orth}))
$$

with [[tensor product]] the [[left derived functor]] $\wedge^L$ of the [[symmetric monoidal smash product of spectra]] (def. \ref{SsymModuleSymmetricSpectra}, def. \ref{SmashProductOfSymmetricSpectra}, prop. \ref{AbstractFormulaGivesSmashProductOfSymmetricSpectra}) and with [[tensor unit]] the [[sphere spectrum]] $\mathbb{S}$ (the image in $Ho(Spectra)$ of any of the structured sphere spectra from def. \ref{TopologicalDiagramCategoriesForSpectra}).

Moreover, the [[localization]] functor ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) is a [[lax monoidal functor]]

$$
  \gamma
   \;\colon\;
  ( OrthSpec(Top_{cg}), \wedge, \mathbb{S}_{orth} )
     \longrightarrow
  ( Ho(Spectra), \wedge^L, \gamma(\mathbb{S}) )
  \,.
$$


=--

+-- {: .proof}
###### Proof

In view of theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom} this is a special case of prop. \ref{MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}.

=--

+-- {: .num_remark #EMHomology}
###### Remark

Let $A,X \in Ho(Spectra)$ be two spectra in the [[stable homotopy category]], then the [[stable homotopy groups]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroups)) of their derived [[symmetric monoidal smash product of spectra]] (corollary \ref{MonoidalStableHomotopyCategory}) is also called the _[[generalized homology]]_ of $X$ with [[coefficients]] in $A$ and denoted

$$
  A_\bullet(X)
    \coloneqq
  \pi_\bullet(A \wedge X)
  \,.
$$

This is conceptually dual to the concept of [[generalized (Eilenberg-Steenrod) cohomology]] ([example](Introduction+to+Stable+homotopy+theory+--+1-1#ForASpectrumXGeneralizedECohomology))

$$
  A^\bullet(X)
   \coloneqq
  [X,A]_\bullet
  \,.
$$

Notice that ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory), [lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum))

$$
  \begin{aligned}
    A_\bullet(X)
    =
    & \pi_\bullet(A \wedge X)
    \\
    & \simeq
    [\mathbb{S}, A \wedge X]_\bullet
  \end{aligned}
  \,.
$$

In the special case that $X = \Sigma^\infty K$ is a [[suspension spectrum]], then

$$
  A_\bullet(X)
  \simeq
  \pi_\bullet( A \wedge K )
$$

(by prop. \ref{SmashProductOfFreeSpectra} ) and this is called the _generalized $A$-homology_ of the topological space $K \in Top^{\ast/}_{cg}$.

Since the [[sphere spectrum]] $\mathbb{S}$ is the [[tensor unit]] for the derived [[smash product of spectra]] (corollary \ref{MonoidalStableHomotopyCategory}) we have

$$
  E_\bullet(\mathbb{S})
  \simeq
  \pi_\bullet(E)
  \,.
$$

For that reason often one also writes for short

$$
  E_\bullet \coloneqq \pi_\bullet(E)
  \,.
$$

Notice that similarly the $E$-[[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-1#ForASpectrumXGeneralizedECohomology)) of the sphere spectrum  is

$$
  \begin{aligned}
    E^\bullet
      & \coloneqq
    E^\bullet(\mathbb{S})
    \\
      & =
    [\mathbb{S},E]_{-\bullet}
    \\
      & \simeq
    \pi_{-\bullet}(E)
    \\
    & \simeq E_{-\bullet}
  \end{aligned}
  \,.
$$

(Beware that, as usual, here we are not displaying a tilde-symbol to indicate reduced cohomology).


=--







### Tensor triangulated structure

We discuss that the derived smash product of spectra from corollary \ref{MonoidalStableHomotopyCategory} on the [[stable homotopy category]] interacts well with its structure of a [[triangulated category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)).

+-- {: .num_defn #TensorTriangulatedCG}
###### Definition

A **[[tensor triangulated category]]** is a [[category]] $Ho$ equipped with

1. the structure of a [[symmetric monoidal category]] $(Ho, \otimes, 1, \tau)$ (def. \ref{SymmetricMonoidalCategory});

1. the structure of a [[triangulated category]] $(Ho, \Sigma, CofSeq)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated));

1. for all objects $X,Y\in Ho$ [[natural isomorphisms]]

   $$
     e_{X,Y}
       \;\colon\;
     (\Sigma X) \otimes Y
       \overset{\simeq}{\longrightarrow}
     \Sigma(X \otimes Y)
   $$

such that

1. (tensor product is additive) for all $V \in Ho$ the functors $V \otimes (-) \simeq (-) \otimes V$ preserve finite [[direct sums]] (are [[additive functors]]);

1. (tensor product is exact) for each object $V \in Ho$ the functors $V \otimes (-) \simeq (-)\otimes V$ preserves distinguished triangles in that for

   $$
     X
       \overset{f}{\longrightarrow}
     X
       \overset{g}{\longrightarrow}
     Y
       \overset{h}{\longrightarrow}
     \Sigma X
   $$

   in $CofSeq$, then also

   $$
     V \otimes X
       \overset{id_V \otimes f}{\longrightarrow}
     V\otimes X
       \overset{id_V \otimes g}{\longrightarrow}
     V \otimes Y
       \overset{id_V \otimes h}{\longrightarrow}
     V \otimes (\Sigma X)
     \simeq
     \Sigma(V \otimes X)
   $$

   is in $CofSeq$, where the equivalence at the end is $e_{X,V}\circ \tau_{V, \Sigma Y}$.

Jointly this says that for all objects $V$ the equivalences $e$ give $V \otimes (-)$ the structure of a _[[triangulated functor]]_.

([Balmer 05, def. 1.1](tensor+triangulated+category#Balmer05))

In addition we ask that

1. (coherence) for all $X, Y, Z \in Ho$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       ( \Sigma(X) \otimes Y) \otimes Z
         &\overset{e_{X,Y} \otimes id}{\longrightarrow}&
       (\Sigma (X \otimes Y)) \otimes Z
         &\overset{e_{X \otimes Y, Z}}{\longrightarrow}&
       \Sigma( (X \otimes Y) \otimes Z )
       \\
       {}^{\mathllap{\alpha_{\Sigma X, Y, Z}}}\downarrow
         &&
         &&
       \downarrow^{\mathrlap{\Sigma \alpha_{X,Y,Z}}}
       \\
       \Sigma (X) \otimes (Y \otimes Z)
         &&
         \underset{e_{X, Y \otimes Z }}{\longrightarrow}
         &&
      \Sigma( X \otimes (Y \otimes Z) )
     }
     \,,
   $$

   where $\alpha$ is the [[associator]] of $(Ho, \otimes, 1)$.

1. (graded commutativity) for all $n_1, n_2 \in \mathbb{Z}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       (\Sigma^{n_1} 1) \otimes (\Sigma^{n_2} 1)
       &\overset{\simeq}{\longrightarrow}&
       \Sigma^{n_1 + n_2} 1
       \\
       {}^{\mathllap{\tau_{\Sigma^{n_1}1, \Sigma^{n_2}1}}}\downarrow
         &&
       \downarrow^{\mathrlap{(-1)^{n_1 \cdot n_2}}}
       \\
       (\Sigma^{n_2} 1) \otimes (\Sigma^{n_1} 1)
       &\underset{\simeq}{\longrightarrow}&
       \Sigma^{n_1 + n_2} 1
     }
     \,,
   $$

   where the horizontal isomorphisms are composites of the $e_{\cdot,\cdot}$ and the braidings.


=--

([Hovey-Palmieri-Strickland 97, def. A.2.1](#HoveyPalmieriStrickland97))

+-- {: .num_prop #TensorTriangulatedStructureOnStableHomotopyCategory}
###### Proposition

The [[stable homotopy category]] $Ho(Spectra)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategory)) equipped with

1. its [[triangulated category]] structure $(Ho(Spectra), \Sigma, CofSeq)$ for distinguished triangles the [[homotopy cofiber sequences]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated);

1. the derived [[symmetric monoidal smash product of spectra]] $(Ho(Spectra), \wedge^L , \mathbb{S})$ (corollary \ref{MonoidalStableHomotopyCategory})

is a [[tensor triangulated category]] in the sense of def. \ref{TensorTriangulatedCG}.

=--

(e.g. [Hovey-Palmieri-Strickland 97, 9.4](HoveyPalmieriStrickland97))

We break up the **proof** into lemma \ref{DerivedSmashProductOfSpectraPreservesDirectSums}, lemma \ref{SmashTensoringWithSpectrumDerivedPreserveshomotopycofibers}, lemma \ref{SmashProductOfSpectraCompatibleWithSuspension} and lemma \ref{GradedCommutativityOfSuspendedSphereSpectra}.

+-- {: .num_lemma #DerivedSmashProductOfSpectraPreservesDirectSums}
###### Lemma

For $V \in Ho(Spectra)$ any spectrum in the [[stable homotopy category]] (remark \ref{StableHomotopyCategoryStructuredSpectra}), then the derived [[symmetric monoidal smash product of spectra]] (corollary \ref{MonoidalStableHomotopyCategory})

$$
  V \wedge^L (-)
  \;\colon\;
  Ho(Spectra)
    \longrightarrow
  Ho(Spectra)
$$

preserves [[direct sums]], in that for all $X, Y \in Ho(Spectra)$ then

$$
  V \wedge^L ( X \oplus Y )
  \simeq
  (V \wedge^L X)
   \oplus
  (V \wedge^L Y)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The direct sum in $Ho(Spectra)$ is represented by the [[wedge sum]] in $SeqSpec(Top_{cg})$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryHasCoproducts
), [prop.](Introduction+to+Stable+homotopy+theory+--+1-1#ProductsAreBiproducts)). Since wedge sum of sequential spectra is the [[coproduct]] in $SeqSpec(Top_{cg})$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-1#WedgeSumOfSpectra)) and since the [[forgetful functor]] $seq^\ast \colon OrthSpec(Top_{cg}) \longrightarrow SeqSpec(Top_{cg})$ preserves colimits (since by prop. \ref{ModulesForDayConvolutionAsEnrichedFunctors} it acts by precomposition on functor categories, and since for these colimits are computed objectwise), it follows that also wedge sum of orthogonal spectra represents the direct sum operation in the stable homotopy category.

Now assume without restriction that $V$, $X$ and $Y$ are cofibrant orthogonal spectra representing the objects of the same name in the stable homotopy catgeory. Since wedge sum is coproduct, it follows that also the wedge sum $X \vee Y$ is cofibrant.

Since $V \wedge^L (-)$ is a [[left Quillen functor]] by theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom}, it follows that the derived tensor product $V \wedge^L (X \oplus Y)$ is represented by the plain [[symmetric monoidal smash product of spectra]] $V \wedge (X \vee Y)$. By def.
\ref{SsymModuleSymmetricSpectra} (or more explicitly by prop. \ref{AbstractFormulaGivesSmashProductOfSymmetricSpectra}) this is the [[coequalizer]]

$$
  V \otimes_{Day} \mathbb{S}_{orth} \otimes_{Day} (X \vee Y)
    \underoverset
      {\longrightarrow}
      {\longrightarrow}
      {\phantom{AAAAAA}}
  V \otimes_{Day} (X \vee Y)
    \overset{coeq}{\longrightarrow}
  V \otimes_{\mathbb{S}_{orth}} (X \vee Y)
  \,.
$$

Inserting the definition of [[Day convolution]] (def. \ref{TopologicalDayConvolutionProduct}), the middle term here is

$$
  \begin{aligned}
    \overset{c_1,c_2}{\int}
    Orth(c_1 \otimes_{Orth} c_2, -)
    \wedge
    V(c_1)
    \wedge
    (X \vee Y)(c_2)
    &\simeq
    \overset{c_1,c_2}{\int}
    Orth(c_1 \otimes_{Orth} c_2, -)
    \wedge
    V(c_1)
    \wedge
    (X(c_2) \vee Y(c_2))
    \\
    &
    \overset{c_1,c_2}{\int}
    Orth(c_1 \otimes_{Orth} c_2, -)
    \wedge
    V(c_1)
    \wedge
    X(c_2)
    \;\vee\;
    \overset{c_1,c_2}{\int}
    Orth(c_1 \otimes_{Orth} c_2, -)
    \wedge
    V(c_1)
    \wedge
    Y(c_2)
    \\
    & \simeq
    V \otimes_{Day} X
    \;\vee\;
    V \otimes_{Day} Y
  \end{aligned}
  \,,
$$

where in the second but last step we used that the [[smash product]] in $Top^{\ast/}_{cg}$ distributes over [[wedge sum]] and that [[coends]] commute with wedge sums (both being [[colimits]]).

The analogous analysis applies to the left term in the coequalizer diagram. Hence the whole diagram splits as the wedge sum of the respective diagrams for $V \wedge X$ and $V \wedge Y$.

=--

+-- {: .num_lemma #SmashTensoringWithSpectrumDerivedPreserveshomotopycofibers}
###### Lemma

For $X \in Ho(Spectra)$ any spectrum in the [[stable homotopy category]] (remark \ref{StableHomotopyCategoryStructuredSpectra}), then the derived [[symmetric monoidal smash product of spectra]] (corollary \ref{MonoidalStableHomotopyCategory})

$$
  X \wedge^L (-)
  \;\colon\;
  Ho(Spectra)
    \longrightarrow
  Ho(Spectra)
$$

preserves [[homotopy cofiber sequences]].

=--

+-- {: .proof}
###### Proof

We may choose a cofibrant representative of $X$ in $OrthSpec(Top_{cg})_{stable}$, which we denote by the same symbol. Then the functor

$$
  X \wedge (-) \;\colon\; OrthSpec(Top_{cg})_{stable} \longrightarrow OrthSpec(Top_{cg})_{stable}_{stable}
$$

is a left Quillen functor in that it preserves cofibrations and acyclic cofibrations by theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom} and it is a [[left adjoint]] by prop. \ref{MonoidalCategoryOfModules}. Hence its [[left derived functor]] is equivalently its restriction to cofibrant objects followed by the localization functor.

But now every [[homotopy cofiber]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)) is represented by the ordinary [[cofiber]] of a cofibration. The left Quillen functor preserves both the cofibration as well as its cofiber.

=--

+-- {: .num_lemma #SmashProductOfSpectraCompatibleWithSuspension}
###### Lemma

The canonical [[suspension]] functor on the [[stable homotopy category]]

$$
  \Sigma \;\colon\; Ho(Spectra) \longrightarrow Ho(Spectra)
$$

commutes with forming the derived [[symmetric monoidal smash product of spectra]] $\wedge^L$ from corollary \ref{MonoidalStableHomotopyCategory} in that for $X,Y\in Ho(Spectra)$ any two spectra, then there are [[isomorphisms]]

$$
  \Sigma ( X \wedge^L Y)
  \simeq
  (\Sigma X) \wedge^L Y
  \simeq
  X \wedge^L (\Sigma Y)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom} the [[symmetric monoidal smash product of spectra]] is a [[left Quillen functor]], and by prop. \ref{SmashTensoringWithCellComplexIsLeftQuillen} and lemma \ref{StandardReducedCylinderOnStructuredSpectrumIsGood} the canonical suspension operation is the [[left derived functor]] of the [[left Quillen functor]] $(-)\wedge S^1$ of smash tensoring with $S^1$. Therefore all three expressions are represented by application of the underived functors on cofibrant representatives in $OrthSpec(Top_{cg})$ (the fibrant replacement that is part of the derived functor construction is preserved by left Quillen functors).

So for $X$ and $Y$ cofibrant orthogonal spectra (which we denote by the same symbol as the objects in the homotopy category which they represent), by def.
\ref{SsymModuleSymmetricSpectra} (or more explicitly by prop. \ref{AbstractFormulaGivesSmashProductOfSymmetricSpectra}), the object $\Sigma(X \wedge^L Y) \in Ho(Spectra)$ is represented by the [[coequalizer]]

$$
  (X \otimes_{Day} \mathbb{S}_{orth} \otimes Y) \wedge S^1
    \underoverset
      {\longrightarrow}
      {\longrightarrow}
      {\phantom{AAAAAA}}
  (X \otimes_{Day} Y) \wedge S^1
  \overset{coeq}{\longrightarrow}
  (X \otimes_{\mathbb{S}_{orth}}Y) \wedge S^1
  \,,
$$

where the two morphisms bing coequalized are the images of those of def. \ref{SsymModuleSymmetricSpectra} under smash tensoring with $S^1$. Now it is sufficient to observe that for any $K \in Top^{\ast/}_{cg}$ we have canonical isomorphisms

$$
  (X \otimes_{Day} Y) \wedge K
  \simeq
  (X \otimes_{Day} (Y \wedge K))
  \simeq
  ( (X \wedge K) \otimes_{Day} Y )
$$

and similarly for the triple Day tensor product.

This follows directly from the definition of the [[Day convolution]] product (def. \ref{TopologicalDayConvolutionProduct})

$$
  \begin{aligned}
     ((X \otimes_{Day} Y) \wedge K)(V)
     & =
     \overset{V_1,V_2}{\int}
      Orth(V_1 \oplus V_2,V)
        \wedge
      X(V_1)
        \wedge
      Y(V_2)
        \wedge
      K
  \end{aligned}
$$

and the symmetry of the smash product on $Top^{\ast/}_{cg}$ (example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}).

=--


+-- {: .num_example #SuspendedSphereSpectrumHomology}
###### Example

For $A \in Ho(Spectra)$ a [[spectrum]], then the $A$-[[generalized homology]] (according to remark \ref{EMHomology}) of a suspension of the [[spectrum]] is the [[stable homotopy groups]] of $A$ in shifted degree:

$$
  A_{\bullet}(\Sigma^n \mathbb{S})
  \simeq
  \pi_{\bullet - n}(A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We compute

$$
  \begin{aligned}
    A_\bullet(\Sigma^n \mathbb{S})
     & \coloneqq
    \pi_\bullet(A \wedge \Sigma^n \mathbb{S})
    \\
      & \simeq
    \pi_\bullet( \Sigma^n( A \wedge \mathbb{S} ) )
     \\
    & \simeq
    \pi_\bullet( \Sigma^n A )
    \\
    & \simeq
    [\mathbb{S}, \Sigma^n A]
    \\
    & =
    [\mathbb{S}, A]_{-n}
    \\
    & \simeq \pi_{\bullet-n}(A)
  \end{aligned}
  \,.
$$

Here we use

* first the definition (remark \ref{EMHomology});

* then the fact that suspension commutes with smash product (lemma \ref{SmashProductOfSpectraCompatibleWithSuspension}, part of the [[tensor triangulated category|tensor triangulated]] structure of prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory});

* then the fact that the [[sphere spectrum]] is the [[tensor unit]] of the smash product of spectra (cor. \ref{MonoidalStableHomotopyCategory});

* then the isomorphism of stable homotopy groups with graded homs out of the spjere spectrum ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum)).

=--

+-- {: .num_lemma #GradedCommutativityOfSuspendedSphereSpectra}
###### Lemma

For $n_1, n_2 \in \mathbb{Z}$ then the following [[commuting diagram|diagram commutes]] in $Ho(Spectra)$:

$$
  \array{
    (\Sigma^{n_1}\mathbb{S}) \wedge^L (\Sigma^{n_2}\mathbb{S})
      &\overset{\simeq}{\longrightarrow}&
    \Sigma^{n_1 + n_2} \mathbb{S}
    \\
    {}^{\mathllap{\tau_{\Sigma^{n_1}\mathbb{S}, \Sigma^{n_2}\mathbb{S}}}}\downarrow
      &&
    \downarrow^{\mathrlap{(-1)}}
    \\
    (\Sigma^{n_2} \mathbb{S}) \wedge^L (\Sigma^{n_1} \mathbb{S})
      &\underset{\simeq}{\longrightarrow}&
    \Sigma^{n_1 + n_2} \mathbb{S}
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

It is sufficient to prove this for $n_1, n_2 \in \mathbb{N} \hookrightarrow \mathbb{Z}$. From this the general statement follows by looping and using lemma \ref{SmashProductOfSpectraCompatibleWithSuspension}.

So assume $n_1, n_2 \geq 0$.

Observe that the sphere spectrum $\mathbb{S} = \gamma(\mathbb{S}_{orth}) \in Ho(Spectra)$ is represented by the orthogonal sphere spectrum $\mathbb{S}_{orth} = \Sigma^\infty_{orth} S^0$ (def. \ref{FreeStructuredSpectrum}) and since $\Sigma^\infty_{orth}$ is a left Quillen functor (prop. \ref{SuspensionSpectrumStructuredStrictQuillenAdjunction}) and $S^0 \in (Top^{\ast/}_{cg})_{Quillen}$ is cofibrant, this is a cofibrant orthogonal spectrum. Hence, as in the proof of lemma \ref{SmashProductOfSpectraCompatibleWithSuspension}, $\Sigma^{n_1} \mathbb{S}$ is represented by

$$
  \mathbb{S}\wedge S^{n_1}
  \simeq
  \Sigma^\infty_{orth}S^{n_1}
  \,.
$$

Since $\Sigma^\infty_{orth}$ is a [[symmetric monoidal functor]] by prop. \ref{SmashProductOfFreeSpectra}, it makes the following [[commuting diagram|diagram commute]]

$$
  \array{
     (\mathbb{S}\wedge S^{n_1})
       \otimes_{\mathbb{S}_{orth}}
     (\mathbb{S} \wedge S^{n_2})
    &\overset{\tau^{OrthSpec(Top_{cg}))}_{\mathbb{S}\wedge S^{n_1}, \mathbb{S}\wedge S^{n_2}}}{\longrightarrow}&
     (\mathbb{S} \wedge S^{n_2})
       \otimes_{\mathbb{S}_{orth}}
     (\mathbb{S}\wedge S^{n_1})
     \\
     \downarrow
       &&
     \downarrow
     \\
     \mathbb{S} \wedge (S^{n_1} \wedge S^{n_2})
       &\underset{\mathbb{S}(\tau^{Top^{\ast/}_{cg}}_{S^{n_1}, S^{n_2}})}
   {\longrightarrow}&
     \mathbb{S}\wedge (S^{n_2} \wedge S^{n_1})
  }
  \,.
$$

Now the homotopy class of $\tau^{Top^{\ast/}_{cg}}_{S^{n_1},S^{n_2}}$ in

$$
  [S^{n_1+n_2}, S^{n_2 +n_1}]_\ast
    \simeq
  \pi_{n_1+n_2}(S^{n_1 + n_2})
    \simeq
  \mathbb{Z}
$$

is

$$
  [\tau^{Top^{\ast/}_{cg}}_{S^{n_1},S^{n_2}}]
  =
  \left\{
    \array{
      1 & if \; n_1 \cdot n_2 \; even
      \\
      -1 & if n_1 \cdot n_2 \; odd
    }
  \right.
  \,.
$$

This translates to $\mathbb{S}\wedge \tau^{Top^{\ast/}_{cg}}_{S^{n_1},S^{n_2}}$ under the identification ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum))

$$
  [\mathbb{S}, X]_\bullet \simeq \pi_\bullet(X)
$$

and using the adjunction $(-)\wedge (S^{n_1 + n_2}) \dashv Maps(S^{n_1 + n_2},-)_\ast$ from prop. \ref{UniversalPropertyOfTensoringAndPoweringOfFunctorsToTopcg}:

$$
  \begin{aligned}
    [\mathbb{S}\wedge (S^{n_1+n_2}),
    \mathbb{S} \wedge ( S^{n_1 + n_2} )]
    \simeq
    [ \mathbb{S}, \mathbb{S} \wedge Maps(S^{n_1+n_2} , S^{n_1+n_2}) ]
  \end{aligned}
  \,.
$$


=--





### Homotopy ring spectra
 {#HomotopyRingSpectra}

We discuss [[commutative monoids]] in the [[tensor triangulated category|tensor triangulated]] [[stable homotopy category]] (prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory}): _[[homotopy commutative ring spectra]]_.

In this section the only [[tensor product]] that plays a role is the [[derived functor|derived]] [[smash product of spectra]] $\wedge^L$ from corollary \ref{MonoidalStableHomotopyCategory}. Therefore to ease notation, in this section (and in all of [[Introduction to Stable homotopy theory -- 2|Part 2]]) we write for short:

$$
  \wedge \coloneqq \wedge^L
  \,.
$$

+-- {: .num_defn #HomotopyCommutativeRingSpectrum}
###### Definition

A [[commutative monoid in a symmetric monoidal category|commutative monoid]] $(E,\mu,e)$ (def. \ref{MonoidsInMonoidalCategory}) in the monoidal [[stable homotopy category]] $(Ho(Spectra),\wedge, \mathbb{S})$ of corollary \ref{MonoidalStableHomotopyCategory} is called a **[[homotopy commutative ring spectrum]]**.

A [[module object]] (def. \ref{ModulesInMonoidalCategory}) over $E$ is accordingly called a **[[homotopy module spectrum]]**.

=--

+-- {: .num_prop #HomotopyGroupsOfHomotopyCommutativeRingSpectrum}
###### Proposition

For $(E, \mu, e)$ a [[homotopy commutative ring spectrum]] (def. \ref{HomotopyCommutativeRingSpectrum}), its [[stable homotopy groups]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroups))

$$
  \pi_\bullet(E)
$$

canonically inherit the structure of a $\mathbb{Z}$-[[graded-commutative ring]].

Moreover, for $X \in Ho(Spectra)$ any spectrum, then the [[generalized homology]] (remark \ref{EMHomology})

$$
  E_\bullet(X)
    \coloneqq
  \pi_\bullet(E \wedge X)
$$

(i.e. the [[stable homotopy groups]] of the [[free module]] over $E$ on $X$ (prop. \ref{MonoidModuleOverItself}))  canonically inherits the structure of a left graded $\pi_\bullet(E)$-[[module object|module]], and similarly

$$
  X_\bullet(E)
   \coloneqq
  \pi_\bullet(X \wedge E)
$$

canonically inherits the structure of a right graded $\pi_\bullet(E)$-[[module]].

=--

+-- {: .proof}
###### Proof

Under the identification ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum))

$$
  \begin{aligned}
    \pi_\bullet(E)
      & \simeq
    [\mathbb{S}, E]_\bullet
    \\
      & \simeq
    [\mathbb{S}, \Sigma^{-\bullet} E]
    \\
      & \simeq
    [ \Sigma^{\bullet} \mathbb{S},E]
  \end{aligned}
$$

let

$$
  \alpha_i
     \;\colon\;
  \Sigma^{n_i}\mathbb{S}
    \longrightarrow
  E
$$

for $i \in \{1,2\}$ be two elements of $\pi_\bullet(E)$.

Observe that there is a canonical identification

$$
   \Sigma^{n_1 + n_2} \mathbb{S} \simeq \Sigma^{n_1} \mathbb{S} \wedge \Sigma^{n_2} \mathbb{S}
$$

since $\mathbb{S}\simeq \mathbb{S}\wedge \mathbb{S}$ is the [[tensor unit]] (cor. \ref{MonoidalStableHomotopyCategory}, lemma \ref{kel1}) using lemma \ref{SmashProductOfSpectraCompatibleWithSuspension} (part of the [[tensor triangulated category|tensor triangulated]] structure from prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory}). With this we may form the composite

$$
  \alpha_1 \cdot \alpha_2
  \; \colon \;
  \Sigma^{n_1 + n_2}\mathbb{S}
    \overset{\simeq}{\longrightarrow}
  \Sigma^{n_1}\mathbb{S}
   \wedge
  \Sigma^{n_2}\mathbb{S}
    \overset{\alpha_1 \wedge \alpha_2}{\longrightarrow}
  E \wedge E
   \overset{\mu}{\longrightarrow}
  E
  \,.
$$

That this pairing is associative and unital follows directly from the associativity and unitality of $\mu$ and the [[coherence]] of the isomorphism on the left (prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory}). Evidently the pairing is graded. That it is bilinear follows since addition of morphisms in the stable homotopy category is given by forming their [[direct sum]] ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#SemiaddtiveStructureUnderlyingAdditiveInducesOriginalEnrichment)) and since $\wedge$ distributes over direct sum (lemma \ref{DerivedSmashProductOfSpectraPreservesDirectSums},  part of the [[tensor triangulated category|tensor triangulated]] structure of prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory})).

It only remains to show graded-commutivity of the pairing. This is exhibited by the following [[commuting diagram]]:

$$
  \array{
     \Sigma^{n_1 + n_2} \mathbb{S}
       &&\overset{(-1)^{n_1 \cdot n_2}}{\longrightarrow}&&
     \Sigma^{n_1 + n_2} \mathbb{S}
     \\
     {}^{\mathllap{\simeq}}\downarrow
       && &&
     \downarrow^{\mathrlap{\simeq}}
     \\
     \Sigma^{n_1}\mathbb{S} \wedge \Sigma^{n_2}\mathbb{S}
       &&\overset{\tau_{\Sigma^{n_1}\mathbb{S}, \Sigma^{n_2}\mathbb{S}}}{\longrightarrow}&&
     \Sigma^{n_2}\mathbb{S} \wedge \Sigma^{n_1}\mathbb{S}
     \\
     {}^{\mathllap{\alpha_1 \wedge \alpha_2}}\downarrow
      && &&
     \downarrow^{\mathrlap{\alpha_2 \wedge \alpha_1}}
     \\
     E \wedge E
       &&\overset{\tau_{E,E}}{\longrightarrow}&&
     E \wedge E
     \\
     & {}_{\mathllap{\mu}}\searrow
     &&
       \swarrow_{\mathrlap{\mu}}
     \\
     && E
  }
  \,.
$$

Here the top square is that of lemma \ref{GradedCommutativityOfSuspendedSphereSpectra} (part of the [[tensor triangulated category|tensor triangulated]] structure of prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory})), the middle square is the naturality square of the [[braiding]] (def. \ref{BraidedMonoidalCategory}, cor. \ref{MonoidalStableHomotopyCategory}), and the bottom triangle commutes by definition of $(E,\mu,e)$ being a commutative monoid (def. \ref{MonoidsInMonoidalCategory}).

Similarly given

$$
  \alpha
     \;\colon\;
  \Sigma^{n_1}\mathbb{S}
    \longrightarrow
  E
$$

as before and

$$
  \nu
    \;\colon\;
  \Sigma^{n_2}\mathbb{S}
    \longrightarrow
  E \wedge X
  \,,
$$

then an action is defined by the composite

$$
  \alpha \cdot \nu
    \;\colon\;
  \Sigma^{n_1 + n_2}\mathbb{S}
   \overset{\simeq}{\longrightarrow}
  \Sigma^{n_1} \mathbb{S} \wedge \Sigma^{n_2}\mathbb{S}
    \overset{\alpha \wedge \nu}{\longrightarrow}
  E \wedge E \wedge X
    \overset{\mu\wedge id}{\longrightarrow}
  E \wedge X
  \,.
$$

This is clearly a graded pairing, and the action property and unitality follow directly from the associativity and unitality, respectively, of $(E,\mu,e)$.

Analogously for the right action on $X_\bullet(E)$.

=--



+-- {: .num_example #StableStemsRingStructure}
###### Example
**(ring structure on the stable homotopy groups of spheres)**

The [[sphere spectrum]] $\mathbb{S} = \gamma(\mathbb{S}_{orth})$ is a [[homotopy commutative ring spectrum]] (def. \ref{HomotopyCommutativeRingSpectrum}).

On the one hand this is because it is the [[tensor unit]] for the derived [[smash product of spectra]] (by cor. \ref{MonoidalStableHomotopyCategory}), and by example \ref{MonoidGivenByTensorUnit} every such is canonically a (commutative) monoid. On the other hand we have the explicit representation by the [[orthogonal ring spectrum]] (def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}) $\mathbb{S}_{orth}$, according to lemma \ref{FSPStructuredSphereSpectra}, and the [[localization]] functor $\gamma$ is a [[symmetric monoidal functor|symmetric]] [[lax monoidal functor]] (prop. \ref{LaxMonoidalLocalizationOfMonoidalModelCategory}, and in fact a [[strong monoidal functor]] on cofibrant objects such as $\mathbb{S}_{orth}$ according to prop. \ref{MonoidalStructureOnHomotopyCategoryOfMonoidalModelCategory}) and hence preserves commutative monoids (prop. \ref{MonoidsPreservedByLaxMonoidalFunctor}).

The [[stable homotopy groups]] of the [[sphere spectrum]] are of course the [[stable homotopy groups of spheres]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroupsOfSpheres))

$$
  \pi^s_\bullet
    \coloneqq
  \pi_\bullet(\mathbb{S})
    \simeq
  \underset{\longrightarrow}{\lim}_k \pi_{\bullet+k}(S^k)
  \,.
$$

Now prop. \ref{HomotopyGroupsOfHomotopyCommutativeRingSpectrum} gives the stable homotopy groups of spheres the structure of a [[graded commutative ring]]. By the proof of prop. \ref{HomotopyGroupsOfHomotopyCommutativeRingSpectrum}, the product operation in that ring sends elements $\alpha_i \colon \Sigma^{n_i}\mathbb{S} \longrightarrow \mathbb{S}$ to

$$
  \Sigma^{n_1 + n_2} \mathbb{S}
    \overset{\simeq}{\longrightarrow}
  \Sigma^{n_1} \mathbb{S}
    \wedge
  \Sigma^{n_2} \mathbb{S}
    \overset{\alpha_1 \wedge \alpha_2}{\longrightarrow}
  \mathbb{S} \wedge \mathbb{S}
    \underoverset{\simeq}{\mu^{\mathbb{S}}}{\longrightarrow}
  \mathbb{S}
  \,,
$$

where now not only the first morphism, but also the last morphism is an [[isomorphism]] (the isomorphism from lemma \ref{kel1}). Hence up to isomorphism, the ring structure on the stable homotopy groups of spheres _is_ the derived smash product of spectra.

This implies that for $X, Y \in Ho(Spectra)$ any two spectra, then the [[graded abelian group]] $[X,Y]_\bullet$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)) of morphisms from $X$ to $Y$ in the [[stable homotopy category]] canonically becomes a [[module]] over the ring $\pi^s_\bullet$

$$
  \pi_\bullet^s \otimes [X,Y]_\bullet
    \longrightarrow
  [X,Y]_\bullet
$$

by

$$
  (\Sigma^{n_1} \mathbb{S} \overset{\alpha}{\to} \mathbb{S}),
  (\Sigma^{n_2} X \overset{f}{\to} Y)
    \;\mapsto\;
  \left(
    \Sigma^{n_1 + n_2} X
     \overset{\simeq}{\to}
    \Sigma^{n_1}\mathbb{S}\wedge \Sigma^{n_2} X
      \overset{\alpha \wedge f}{\longrightarrow}
    \mathbb{S} \wedge Y
     \overset{\simeq}{\to}
    Y
  \right)
  \,.
$$

In particular for every spectrum $X \in Ho(Spectra)$, its [[stable homotopy groups]] $\pi_\bullet(X)\simeq [\mathbb{S}, X]_\bullet$ ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum)) canonically form a module over $\pi_\bullet^s$. If $X = E$ happens to carry the structure of a [[homotopy commutative ring spectrum]], then this module structure coincides the one induced from the unit

$$
  \pi_\bullet(e)
  \;\colon\;
  \pi_\bullet^s = \pi_\bullet(\mathbb{S})
   \longrightarrow
  \pi_\bullet(E)
$$

under prop. \ref{HomotopyGroupsOfHomotopyCommutativeRingSpectrum}.

(It is straightforward to unwind all this categorical algebra to concrete component expressions by proceeding as in the proof of [this lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGrouspAsHomsOutOfSphereSpectrum)).)


=--

This finally allows to uniquely characterize the [[stable homotopy theory]] that we have been discussing:


+-- {: .num_theorem #CharacterizationOfStableHomotopyTheory}
###### Theorem
**(Schwede-Shipley uniqueness theorem)**

The [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C})$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfAModelCategory)) of every [[stable homotopy category]] $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelCategory)) canonically has graded hom-groups with the structure of modules over $\pi_\bullet^s = \pi_\bullet(\mathbb{S})$ (example \ref{StableStemsRingStructure}). In terms of this, the following are equivalent:

1. There is a [[zig-zag]] of [[Quillen equivalences]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#QuillenEquivalence)) between $\mathcal{C}$ and the stable [[model structure on topological sequential spectra]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentialSpectraIsModelCategory)) (equivalently (thm. \ref{SequentialSpectraQuillenEquivalence}) the stable [[model structure on orthogonal spectra]])

   $$
      \mathcal{C}
        \underoverset
          {\longrightarrow}
          {\longleftarrow}
          {{}_{\phantom{Qu}}\simeq_{Qu}}
        \underoverset
          {\longleftarrow}
          {\longrightarrow}
          {{}_{\phantom{Qu}}\simeq_{Qu}}
         \;\;\cdots \;\;
        \underoverset
          {\longleftarrow}
          {\longrightarrow}
          {{}_{\phantom{Qu}}\simeq_{Qu}}
       OrthSpec(Top_{cg})_{stable}
        \underoverset
          {\longrightarrow}
          {\longleftarrow}
          {{}_{\phantom{Qu}}\simeq_{Qu}}
       SeqSpec(Top_{cg})_{stable}
   $$

1. there is an [[equivalence of categories]] between the [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C})$ and the [[stable homotopy category]] $Ho(Spectra)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategory))

   $$
      Ho(\mathcal{C}) \simeq Ho(Spectra)
   $$

   which is $\pi^s_\bullet$-linear on all hom-groups.

=--

([Schwede-Shipley 02, Uniqueness theorem](#SchwedeShipley02))






## Examples
 {#Examples}

For reference, we consider some basic examples of [[orthogonal ring spectra]] (def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}) $E$. By prop. \ref{RingSpectraAreDayMonoids} and corollary \ref{MonoidalStableHomotopyCategory} each of these examples in particular represents a [[homotopy commutative ring spectrum]] (def. \ref{HomotopyCommutativeRingSpectrum}) in the [[tensor triangulated category|tensor triangulated]] [[stable homotopy category]] (prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory}).

We make use of these examples of homotopy commutative ring spectra $E$ in [[Introduction to Stable homotopy theory -- 2|Part 2]] in the computation of $E$-[[Adams spectral sequences]].

For constructing representations as [[orthogonal ring spectra]] of spectra that are already known as [[sequential spectra]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#SequentialSpectra)) two principles are usefully kept in mind:

1. by prop. \ref{RingSpectraAreDayMonoids} it is sufficient to give an equivariant  multiplicative pairing $E_{n_1} \wedge E_{n_2} \to E_{n_1 + n_2}$ and equivariant unit maps $S^0 \to E_0$, $S^1 \to E_1$, from these the structure maps $S^{n_1} \wedge E_{n_2}\to E_{n_1+n_2}$ are already uniquely induced;

1. the choice of $O(n)$-action on $E_n$ is governed mainly by the demand that the unit map $S^n \to E_n$ has to be equivariant, with respect to the $O(n)$-action on $S^n$ induced by regarding $S^n$ as the [[one-point compactification]] of the defining $O(n)$-representation on $\mathbb{R}^n$ ("[[representation sphere]]").





### Sphere spectrum

We already described the orthogonal [[sphere spectrum]] $\mathbb{S}$ as an [[orthogonal ring spectrum]] in lemma \ref{FSPStructuredSphereSpectra}. The component spaces are the spheres $S^n$ with their $O(n)$-action as [[representation spheres]], and the multiplication maps are the canonical identifications

$$
  S^{n_1} \wedge S^{n_2}
    \longrightarrow
  S^{n_1 + n_2}
  \,.
$$

More generally, by prop. \ref{SmashProductOfFreeSpectra} the orthogonal [[suspension spectrum]] functor is a [[strong monoidal functor]], and so by prop. \ref{RingSpectraAreDayMonoids} the [[suspension spectrum]] of a monoid in $Top^{\ast/}_{cg}$ (for instance $G_+$ for $G$ a [[topological group]]) canonically carries the structure of an orthogonal ring spectrum.

The orthogonal sphere spectrum is the special case of this with $\mathbb{S}_{orth} \simeq \Sigma^\infty_{orth} S^0$ for $S^0$ the tensor unit in $Top^{\ast/}_{cg}$ (example \ref{PointedTopologicalSpacesWithSmashIsSymmetricMonoidalCategory}) and hence a monoid by example \ref{MonoidGivenByTensorUnit}.





### Eilenberg-MacLane spectra

We discuss the model of [[Eilenberg-MacLane spectra]] as [[symmetric spectra]] and [[orthogonal spectra]]. To that end, notice the following model for [[Eilenberg-MacLane spaces]].

+-- {: .num_defn #ReducedALinearizationOfnSphere}
###### Definition

For $A$ an [[abelian group]] and $n \in \mathbb{N}$, the **reduced $A$-linearization** $A[S^n]_\ast$ of the [[n-sphere]] $S^n$ is the [[topological space]], whose underlying set is the [[quotient]]
of the [[tensor product]]  with $A$ of the [[free abelian group]] on the underlying set of $S^n$,

$$
  A \otimes_{\mathbb{Z}}[S^n]
  =
  A[S^n]
   \longrightarrow
  A[S^n]_\ast
$$

by the relation that identifies every [[formal linear combination]] of the basepoint of $S^n$ with 0. The [[topological space|topology]] is the induced [[quotient topology]]

$$
  \underset{k \in \mathbb{N}}{\sqcup}
   A^k \times (S^n)^k
  \longrightarrow
  A[S^n]_\ast
$$

(of the [[disjoint union]] of [[product topological spaces]], where $A$ is equipped with the [[discrete topology]]).

=--

([Aguilar-Gitler-Prieto 02, def. 6.4.20](Eilenberg-MacLane+space#AguilarGitlerPrieto02))


+-- {: .num_prop #ReducedALinearizationOfnSphereIsEMSpace}
###### Proposition

For $A$ a [[countable set|countable]] [[abelian group]], then the reduced $A$-linearization $A[S^n]_\ast$ (def. \ref{ReducedALinearizationOfnSphere}) is an [[Eilenberg-MacLane space]], in that its [[homotopy groups]] are

$$
  \pi_q(A[S^n]_\ast)
   \simeq
   \left\{
     \array{
       A & if \; q = n
       \\
       \ast & otherwise
     }
   \right.
$$

(in particular for $n \geq 1$ then there is a unique connected component and hence we need not specify a basepoint for the homotopy group).


=--

([Aguilar-Gitler-Prieto 02, corollary 6.4.23](Eilenberg-MacLane+space#AguilarGitlerPrieto02))

+-- {: .num_defn #OrthogonalEilenbergMacLaneRingSpectrum}
###### Definition

For $A$ a [[countable set|countable]] [[abelian group]], then the **orthogonal [[Eilenberg-MacLane spectrum]]** $H A$ is the [[orthogonal spectrum]] (def. \ref{OrthogonalSpectrum}) with

* component spaces

  $$
    (H A)_n \coloneqq A[S^n]_\ast
  $$

  being the reduced $A$-linearization (def. \ref{ReducedALinearizationOfnSphere}) of the [[representation sphere]] $S^n$;

* $O(n)$-[[action]] on $A[S^n]_\ast$ induced from the canonical $O(n)$-action on $S^n$ ([[representation sphere]]);

* structure maps

  $$
    \sigma_n
      \;\colon\;
    S^1 (H A)_n
      \longrightarrow
    (H A)_{n+1}
  $$

  hence

  $$
    S^1 \wedge A[S^n]
      \longrightarrow
    A[S^{n+1}]
  $$

  given by

  $$
    \left(
     x,
    \left(
       \underset{i}{\sum} a_i y_i
    \right),
    \right)
      \mapsto
    \underset{i}{\sum} a_i (x,y_i)
    \,.
  $$

The incarnation of $H A$ as a [[symmetric spectrum]] is the same, with the group action of $O(n)$ replaced by the [[subgroup]] action of the [[symmetric group]] $\Sigma(n) \hookrightarrow O(n)$.

If $R$ is a [[commutative ring]], then the Eilenberg-MacLane spectrum $H R$ becomes a commutative [[orthogonal ring spectrum]] or [[symmetric ring spectrum]] (def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}) by

1. taking the multiplication

   $$
     (H R)_{n_1} \wedge (H R)_{n_2}
       =
     R[S^{n_1}]_\ast \wedge R[S^{n_2}]_\ast
       \longrightarrow
     R[S^{n_1 + n_2}]
      =
     (H R)_{n_1 + n_2}
   $$

   to be given by

   $$
     \left(
     \left(
        \underset{i}{\sum} a_i x_i
     \right)
     ,
     \left(
       \underset{j}{\sum} b_j y_j
     \right)
     \right)
      \;\mapsto\;
     \underset{i,j}{\sum}
      (a_i \cdot b_j)(x_i, y_j)
   $$

1. taking the unit maps

   $$
     S^n
       \longrightarrow
     A[S^n]_\ast = (H R)_n
   $$

   to be given by the canonical inclusion of generators

   $$
     x \mapsto 1 x
     \,.
   $$

=--

([Schwede 12, example I.1.14](#Schwede12))

+-- {: .num_prop #StableHomotopyGroupsOfEMSpectrum}
###### Proposition

The [[stable homotopy groups]] (def. \ref{StableOrthStructureClassesOfMorphisms}) of an [[Eilenberg-MacLane spectrum]] [[HA]] (def. \ref{OrthogonalEilenbergMacLaneRingSpectrum}) are

$$
  \pi_q(H A)
    \simeq
  \left\{
    \array{
      A & if \; q = 0
      \\
      0 & otherwise
    }
  \right.
$$


=--







### Thom spectra
 {#ThomSpectra}

We discuss the realization of _[[Thom spectra]]_ as [[orthogonal ring spectra]]. For background on Thom spectra realized as [[sequential spectra]] see [[Introduction to Stable homotopy theory -- S|Part S]] the section _[Thom spectra](Introduction+to+Stable+homotopy+theory+--+S#ThomSpectra)_.

+-- {: .num_defn}
###### Definition

As an [[orthogonal ring spectrum]] (def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}), the **universal [[Thom spectrum]]** $M O$ has

* component spaces

  $$
    (M O)_n \coloneqq E O(n)_+ \underset{O(n)}{\wedge} S^n
  $$

  the [[Thom spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#ThomSpace)) of the [[universal vector bundle]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#EOn)) of [[rank]] $n$;

* left $O(n)$-action induced by the remaining canonical left action of $E O(n)$;

* canonical multiplication maps ([def.](Introduction+to+Stable+homotopy+theory+--+S#UniversalThomSpectrumForBfStructure))

  $$
    (E O(n_1)_+ \underset{O(n_1)}{\wedge} S^{n_1})
      \wedge
    (E O(n_2)_+ \underset{O(n_2)}{\wedge} S^{n_2}
      \longrightarrow
    E O(n_1 + n_2)_+
      \underset{O(n_1 + n_2)}{\wedge}
    S^{n_1 + n_2}
  $$

* unit maps

  $$
    S^n \simeq O(n)_+ \wedge_{O(n)} S^n
      \longrightarrow
    E O(n)_+ \wedge_{O(n)} S^n
  $$

  induced by the fiber inclusion $O(V) \hookrightarrow E O(V)$.

=--

([Schwede 12, I, example 1.16](#Schwede12))


For the universal complex Thom spectrum [[MU]] the construction is a priori directly analogous, but with the real [[Cartesian space]] $\mathbb{R}^n$ replace by the [[complex vector space]] $\mathbb{C}^n$ thoughout. This makes the [[n-sphere]] $S^n = S^{(\mathbb{R}^n)}$ be replaced by the $2n$-sphere $S^{2n} \simeq S^{\mathbb{C}^n}$ throughout. Hence the construction requires a second step in which the resulting $S^2$-spectrum ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#SequentialTSpectra)) is turned into an actual [[orthogonal spectrum]]. This proceeds differently than for [[sequential spectra]] ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#AdjunctionBetweenSequentialSpectraAndSequentialTSpectra)) due to the need to have compatible [[orthogonal group]]-[[action]] on all spaces.

+-- {: .num_defn #OrthogonalComplexThomSpectrum}
###### Definition

The **universal complex [[Thom spectrum]]** [[MU]] is represented as an [[orthogonal ring spectrum]] (def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}) as follows

First consider the component spaces

$$
  \overline{M U}_n
  \coloneqq
  E U(n)_+ \wedge_{U(n)} S^{(\mathbb{C}^n)}
$$

given by the [[Thom spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#ThomSpace)) of the [[complex vector bundle|complex]] [[universal vector bundle]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#EOn)) of [[rank]] $n$, and
equipped with the $O(n)$-action which is induced via the canonical inclusions

$$
  O(n) \hookrightarrow U(n) \hookrightarrow E U(n)
  \,.
$$

Regard these as equipped with the canonical pairing maps ([def.](Introduction+to+Stable+homotopy+theory+--+S#UniversalThomSpectrumForBfStructure))

$$
  \overline{\mu}_{n_1,n_2}
    \;\colon\;
  \overline{M U}_{n_1}
    \wedge
  \overline{M U}_{n_2}
    \longrightarrow
  \overline{M U}_{n_1 + n_2}
  \,.
$$

These are $U(n)$-equivariant, hence in particular $O(n)$-equivariant.

Then take the actual components spaces to be [[loop spaces]] of these:

$$
  M U_n
  \coloneqq
  Maps(S^n, \overline{M U}_n)
$$

and regard these as equipped with the [[conjugation action]] by $O(n)$ induced by the above action on $\overline{M U}_n$ and the canonical action on $S^n \simeq S^{(\mathbb{R}^n)}$.

Define the actual pairing maps

$$
  \mu_{n_1, n_2}
    \;\colon\;
  M U_{n_1} \wedge M U_{n_2}
   \longrightarrow
  M U_{n_1 + n_2}
$$

via

$$
  \begin{aligned}
    Maps(S^{n_1}, \overline{M U}_{n_1})
      \wedge
    Maps(S^{n_2}, \overline{M U}_{n_2})
     & \longrightarrow
    Maps(S^{n_1 + n_2}, \overline{M U}_{n_1 + n_2})
    \\
    (\alpha_1, \alpha_2)
      & \mapsto
    \overline{\mu}_{n_1, n_2} \circ (\alpha_1 \wedge \alpha_2)
  \end{aligned}
  \,.
$$

Finally in order to define the unit maps, consider the isomorphism

$$
  S^{2 n}
  \simeq
  S^{\mathbb{C}^n}
  \simeq
  S^{\mathbb{R}^n \oplus i \mathbb{R}^n}
  \simeq
  S^{n} \wedge S^n
$$

and then take the unit maps

$$
  S^n \longrightarrow (M U)_n = Maps(S^n , \overline{M U}_n)
$$

to be the [[adjuncts]] of the canonical embeddings

$$
  S^n \wedge S^n
  \simeq
  S^{\mathbb{C}^n}
  \simeq
  U(n)_+ \wedge_{U(n)} S^{\mathbb{C}^n}
    \longrightarrow
  E U(n)_+ \wedge_{U(n)} S^{\mathbb{C}^n}
  \,.
$$

=--

([Schwede 12, I, example 1.18](#Schwede12))





## Conclusion
 {#Conclusion}

We summarize the results about [[stable homotopy theory]] obtained above.

First of all we have established a [[commuting diagram]] of [[Quillen adjunctions]] and [[Quillen equivalences]] of the form

$$
  \array{
    (Top^{\ast/}_{cg})_{Quillen}
      &
      \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
      &
    (Top^{\ast/}_{cg})_{Quillen}
    \\
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
      &&
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
    \\
    SeqSpec(Top_{cg})_{strict}
     &
      \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
     &
    SeqSpec(Top_{cg})_{strict}
    \\
    {}^{\mathllap{id}}\downarrow \dashv \uparrow^{\mathrlap{id}}
      &&
    {}^{\mathllap{id}}\downarrow \dashv \uparrow^{\mathrlap{id}}
    \\
    SeqSpec(Top_{cg})_{stable}
     &
      \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\simeq_Q}
     &
    SeqSpec(Top_{cg})_{stable}
    \\
    {}^{\mathllap{seq_!}}\downarrow \simeq_Q \uparrow^{\mathrlap{seq^\ast}}
      &&
    {}^{\mathllap{seq_!}}\downarrow \simeq_Q \uparrow^{\mathrlap{seq^\ast}}
    \\
    OrthSpec(Top_{cg})_{stable}
      &&
    OrthSpec(Top_{cg})_{stable}
  }
$$

where

* $(Top^{\ast/}_{cg})_{Quillen}$ is the [[classical model structure on pointed topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#TopQuillenModelStructure), [thm.](Introduction+to+Stable+homotopy+theory+--+P#CofibrantGenerationOfPointedTopologicalSpaces));

* $SeqSpec(Top_{cg})_{stable}$ is the stable [[model structure on topological sequential spectra]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentialSpectraIsModelCategory));

* $OrthSpec(Top_{cg})_{stable}$ is the stable [[model structure on orthogonal spectra]] from theorem \ref{OrthogonalSpectraStableModelStructure}.

Here the top part of the diagram is from remark \ref{SummarySituationForStrictModelStructure}, while the vertical [[Quillen equivalence]] $(seq_! \dashv seq^\ast)$ is from theorem \ref{OrthogonalSpectraStableModelStructure}.

Moreover, the top and bottom [[model categories]] are [[monoidal model categories]] (def. \ref{MonoidalModelCategory}): $Top^{\ast/}_{cg}$ with respect to the [[smash product]] of [[pointed topological spaces]] (theorem \ref{MonoidalStrictModelStructure}) and $OrthSpec(Top_{cg})_{strict}$ as well as $OrthSpec(Top_{cg})_{stable}$ with respect to the [[symmetric monoidal smash product of spectra]] (theorem \ref{MonoidalStrictModelStructure} and theorem \ref{StableModelStructureWithSymmetricMonoidalSmashProductSatisfiesPushoutProductAxiom}); and the compsite vertical adjunction

$$
  \array{
    (Top^{\ast/}_{cg}, \wedge , S^0)
    \\
    {}^{\mathllap{\Sigma^\infty_{orth}}}\downarrow
     \dashv
    \uparrow^{\mathrlap{\Omega^\infty_{orth}}}
    \\
    ( OrthSpec(Top_{cg}), \wedge, \mathbb{S}_{orth} )
  }
$$

is a [[strong monoidal Quillen adjunction]] (def. \ref{MonoidalQuillenAdjunction}, corollary \ref{StableMonoidalQuillenSuspensionSpectrumFunctor}), and so also the induced adjunction of [[derived functors]]

$$
  \array{
     (Ho(Top^{\ast/}), \wedge^L, S^0)
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     (Ho(Spectra), \wedge^L, \mathbb{S})
  }
$$

is a [[strong monoidal adjunction]] (by prop. \ref{StrongMonoidalDerivedFunctorFromStrongMonoidalQuillenAdjunction}) from the the derived [[smash product]] of [[pointed topological spaces]] to the derived [[symmetric smash product of spectra]].



Under passage to [[homotopy category of a model category|homotopy categories]] this yields a [[commuting diagram]] of [[derived functor|derived]] [[adjoint functors]]

$$
  \array{
    Ho(Top^{\ast/})
    &
      \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\bot}
    &
    Ho(Top^{\ast/})
    \\
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
      &&
    {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
   \\
   Ho(Spectra)
     &
     \underoverset
       {\underset{\Omega}{\longrightarrow}}
       {\overset{\Sigma}{\longleftarrow}}
       {\simeq}
    &
  Ho(Spectra)
  }
$$

between the (Serre-Quillen-)[[classical homotopy category]] $Ho(Top^{\ast/})$ and the [[stable homotopy category]] $Ho(Spectra)$ (remark \ref{StableHomotopyCategoryStructuredSpectra}). The latter is an [[additive category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#AdditiveCategory)) with [[direct sum]] the [[wedge sum]] of spectra $\oplus = \vee$ ([lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryHasCoproducts), [lemma](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsAbEnriched)) and in fact a [[triangulated category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CategoryWithCofiberSequences)) with distinguished triangles the [[homotopy cofiber sequences]] of spectra ([prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)).

While this is the situation already for [[sequential spectra]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsIndeedStabilizationOfClassicalHomotopyCategory)), in addition we have now that both the [[classical homotopy category]] as well as the [[stable homotopy category]] are [[symmetric monoidal categories]] with respect to derived [[smash product]] of [[pointed topological spaces]] and the derived [[symmetric monoidal smash product of spectra]], respectively (corollary \ref{MonoidalStableHomotopyCategory}).

Moreover, the derived smash product of spectra is compatible with the [[additive category]] structure ([[direct sums]]) and the [[triangulated category]] structure ([[homotopy cofiber sequences]]), this being a _[[tensor triangulated category]]_ (prop. \ref{TensorTriangulatedStructureOnStableHomotopyCategory}).

| [[abelian groups]] | [[spectra]] |
|--------------------|-------------|
| [[integers]] $\mathbb{Z}$ | [[sphere spectrum]] $\mathbb{S}$ |
| $Ab \simeq \mathbb{Z} Mod$   | $Spectra \simeq \mathbb{S} Mod$ |
| [[direct sum]] $\oplus$ | [[wedge sum]] $\vee$ |
| [[tensor product of modules|tensor product]] $\otimes_{\mathbb{Z}}$ | [[smash product of spectra]] $\wedge_{\mathbb{S}}$ |
| [[kernels]]/[[cokernels]] | [[homotopy fibers]]/[[homotopy cofibers]] |


The [[commutative monoids in a symmetric monoidal category|commutative monoids]] with respect to this [[smash product of spectra]] are precisely the commutative [[orthogonal ring spectra]] (def. \ref{RingSpectrumInSymmetricAndOrthogonalSpectra}, prop. \ref{RingSpectraAreDayMonoids}) and the [[module objects]] over these are precisely the orthogonal [[module spectra]] (def. \ref{SymmetricModuleSpectrum}, prop. \ref{ModuleSpectraAreModuleFunctors}).


[[!include homological and higher algebra -- table]]


The [[localization]] functors $\gamma$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) from the [[monoidal model categories]] to their [[homotopy category of a model category|homotopy categories]] are [[lax monoidal functors]]  (cor. \ref{MonoidalStableHomotopyCategory})

$$
  \array{
    (Top^{\ast/}_{cg}, \wedge, S^0)
      &\longrightarrow&
    (Ho(Top^{\ast/}), \wedge^L, \gamma(S^0))
    \\
    ( OrthSpec(Top_{cg}), \wedge, \mathbb{S}_{orth} )
      &\longrightarrow&
    ( Ho(Spectra), \wedge^L, \gamma(\mathbb{S}) )
  }
  \,.
$$

This implies that for $E \in OrthSpec(Top_{cg})$ a commutative[[orthogonal ring spectrum]], then its image $\gamma(E)$ in the [[stable homotopy category]] is a [[homotopy commutative ring spectrum]] (def. \ref{HomotopyCommutativeRingSpectrum}) and similarly for module spectra (prop. \ref{MonoidsPreservedByLaxMonoidalFunctor}).


| [[monoidal model category|monoidal]] [[stable model category]] | -[[localization]]$\to$ | [[tensor triangulated category]] |
|------|----------|-----------|
| stable [[model structure on orthogonal spectra]] $OrthSpec(Top_{cg})_{stable}$ | | [[stable homotopy category]] $Ho(Spectra)$ |
| [[symmetric monoidal smash product of spectra]] | | derived [[smash product of spectra]] |
| commutative [[orthogonal ring spectrum]] ([[E-infinity ring]]) |   | [[homotopy commutative ring spectrum]] |

Finally, the graded hom-groups $[X,Y]_\bullet$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory)) in the [[tensor triangulated category|tensor triangulated]] [[stable homotopy category]] are canonically graded modules over the [[graded commutative ring]] of [[stable homotopy groups of spheres]] (exmpl. \ref{StableStemsRingStructure})

$$
  [X,Y]_\bullet
    \in
  \pi_\bullet(\mathbb{S}) Mod
  \,.
$$

Hence the next question is how to actually compute any of these. This is the topic of _[[Introduction to Stable homotopy theory -- 2|Part 2 -- The Adams spectral sequence]]_.




## References
 {#References}


The [[model structure on orthogonal spectra]] is due to

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]],  _[[Model categories of diagram spectra]]_,   Proceedings of the London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

* {#May02} [[Michael Mandell]], [[Peter May]], _Equivariant orthogonal spectra and S-modules_, Memoirs of the AMS 2002  ([pdf](http://www.math.uiuc.edu/K-theory/0408/MMM.pdf))


following the [[model structure on symmetric spectra]] in

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))

The basics of [[monoidal model categories]] are the topic of

* {#Hovey99} [[Mark Hovey]], chapter 4 of _Model Categories_ Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/hovey-model-cats.pdf))

and the theory of monoids in [[monoidal model categories]] is further developed in

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], _Rings, modules and algebras in stable homotopy theory_, AMS 1997, 2014

* {#SchwedeShipley00} [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf))

For the induced [[tensor triangulated category]] structure on the stable homtopy category we follow

* {#HoveyPalmieriStrickland97} [[Mark Hovey]], [[John Palmieri]], [[Neil Strickland]], _Axiomatic stable homotopy theory_, Memoirs of the AMS 610 (1997) ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/axiomatic.pdf))

which all goes back to

* {#Adams74} [[Frank Adams]], _[[Stable homotopy and generalised homology]]_, 1974


A compendium on [[symmetric spectra]] is

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

