
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contenta
{:toc}

## Idea

Each [[filtered object|filtering]] on an [[object]] $X$ in a suitable [[stable (∞,1)-category]] $\mathcal{C}$ (a _[[stable homotopy type]]_ $X$ such as a [[spectrum object]], in particular possibly a [[chain complex]]) induces a [[spectral sequence]] whose first page consists of the [[homotopy groups]] of the [[homotopy cofibers]] of the filtering and which under suitable conditions converges to the [[homotopy groups]] of the total object $X$.

This is a generalization of the traditional [[spectral sequence of a filtered complex]] to which it reduces for $\mathcal{C} = Ch_\bullet(\mathcal{A})$ an [[(∞,1)-category of chain complexes]] [[presentable (infinity,1)-category|presented]] in the projective [[model structure on chain complexes]].

Moreover, by applying general [[(∞,1)-category theory|(∞,1)-categorical]] notion to naturally arising towers (such as the [[Whitehead tower]], the [[chromatic tower]]) it naturally produces more specialized spectral sequences (such as the [[Atiyah-Hirzebruch spectral sequence]], the [[chromatic spectral sequence]], etc.). Specifically, applied to a [[coskeleton]] tower of a dual [[Cech nerve]] of an [[E-∞ algebra]] $E$ it naturally produces the $E$-[[Adams spectral sequence]]. See the discussion of the _[Examples](#Examples)_ below.

Therefore in [[(∞,1)-category theory]] one finds a lucky coincidence of historical terminology: _[[spectral sequences]] are essentially [[sequential diagram|sequences]] of [[spectra]]_, when considered on homotopy groups.


The general construction can be summarized as follows:

+-- {: .standout}
Any [[homological functor]]

$$ \mathcal{C}\to\mathcal{A} $$

from a [[stable (∞,1)-category]] to an [[abelian category]] induces a functor

$$ Filt(\mathcal{C}) \to SpSeq(\mathcal{A}) $$


from the stable (∞,1)-category of [[filtered object in an (∞,1)-category|filtered objects]] in $\mathcal{C}$ to the abelian category of bigraded [[spectral sequence|spectral sequences]] in $\mathcal{A}$. 
=--

## Definition


Let throughout $\mathcal{C}$ be a [[stable (∞,1)-category]], $\mathcal{A}$ an [[abelian category]], and $\pi \;\colon\; \mathcal{C}\longrightarrow \mathcal{A}$ a [[homological functor]] on $\mathcal{C}$, i.e., a functor that transforms every [[cofiber sequence]]

$$ X\to Y\to Z\to \Sigma X $$

in $\mathcal{C}$ into a long exact sequence



$$ \dots \to \pi(X)\to \pi(Y)\to \pi(Z)\to \pi(\Sigma X) \to \dots $$

in $\mathcal{A}$. We write $\pi_n=\pi\circ \Sigma^{-n}$. 

+-- {: .num_example}
###### Example

* $\mathcal{C}$ is arbitrary, $\mathcal{A}$ is the category of [[abelian groups]] and $\pi$ is taking the 0th [[homotopy group]] $\pi_0 \mathcal{C}(S,-)$ of the [[mapping spectrum]] out of some [[object]] $S\in\mathcal{C}$

* $\mathcal{C}$ is equipped with a [[t-structure]], $\mathcal{A}$ is the [[heart of a stable (∞,1)-category|heart]] of the t-structure, and $\pi$ is the canonical functor.

* $\mathcal{C} = D(\mathcal{A})$ is the [[derived category]] of the abelian category $\mathcal{A}$ and $\pi=H_0$ is the degree-0  [[chain homology]] functor.

* Any of the above with $\mathcal{C}$ and $\mathcal{A}$ replaced by their [[opposite categories]].

=--

### (Co-)Filtered objects and their (co-)chain complexes
 {#FilteredObjectsAndTheirChainComplexes}

+-- {: .num_defn #GeneralizedFilteredObject}
###### Definition

A _[[filtered object in an (∞,1)-category]]_ in $\mathcal{C}$ is
an [[object]] $X \in \mathcal{C}$ together with 
a [[sequential diagram]] $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n-1} \to X_n \to X_{n+1} \to \cdots
$$

and an [[equivalence in an (infinity,1)-category|equivalence]]

$$
  X \coloneqq \underset{\rightarrow}{\lim}_n X_n
$$

between $X$ and the [[(∞,1)-colimit]] of this sequence.
(The sequence itself is _the filtering on $X$_.)

Dually, a _[[filtered object in an (∞,1)-category|co-filtered object in an (∞,1)-category]]_ in $\mathcal{C}$ is
an [[object]] $X \in \mathcal{C}$ together with 
a [[sequential diagram]] $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n-1} \to X_n \to X_{n+1} \to \cdots
$$

and an [[equivalence in an (infinity,1)-category|equivalence]]

$$
  X \coloneqq \underset{\leftarrow}{\lim}_n X_n
$$

between $X$ and the [[(∞,1)-limit]] of this sequence.
(The sequence itself is _the co-filtering on $X$_.)


=--

This appears as ([[Higher Algebra|Higher Algebra, def. 1.2.2.9]]).
The notions are equivalent under replacing $\mathcal{C}$ by its [[opposite category]] $\mathcal{C}^{op}$.


+-- {: .num_remark #FilteredObjectInModelCategory}
###### Remark

If $\mathcal{C}$ is [[presentable (infinity,1)-category|presented]] by a 
sufficiently nice [[model category]] $C$ (for instance a [[combinatorial  model category]]), then [[(∞,1)-colimits]] in $\mathcal{C}$ are computed by [[homotopy colimits]] in $C$. These in turn are computed as ordinary [[colimits]] in $C$ over a cofibrant [[diagram]] in the [[projective model structure on functors]]. 

Specifically, as discussed at _[homotopy limit -- Examples -- Over sequential diagrams](homotopy+limit#SequentialHocolims)_ a cofibrant resolution of a [[sequential diagram]] $(\mathbb{N}, \leq) \to C$ is a sequential diagram all whose whose objects are cofibrant and all whose morphisms are cofibrations in $C$

$$
  \emptyset \stackrel{cof}{\to} X_0 \stackrel{cof}{\to} \cdots \to X^C_{n-1} \stackrel{cof}{\to} X_{n}^C \stackrel{cof}{\to} X_{n+1}^C \to \cdots
  \,,
$$

where $X_n^C \in C$ denotes an object in the model category presenting the given object $X_n \in \mathcal{C}$. 

Moreover, in many [[model categories]] that appear in practice the cofibrations are in particular [[monomorphisms]], this is the case in particular in a projective [[model structure on chain complexes]]. In these cases then a filtering on an object $X \in \mathcal{C}$ in the abstract sense of [[(∞,1)-categories]] is presented by a [[filtered object]] $X^C \in C$ in the sense of plain [[category theory]].

The intrinsic definition \ref{GeneralizedFilteredObject} makes manifest however that the [[monomorphism]]-aspect here is just a means of a presentation of the filtering and not an intrinsic aspect of the [[homotopy theory]]. 

 
=--


+-- {: .num_defn #ChainComplexInStableInfinityCategory}
###### Definition

Let $I$ be a [[linearly ordered set]]. An _$I$-chain complex_ in a [[stable (∞,1)-category]] $\mathcal{C}$ is an [[(∞,1)-functor]]

$$
  F \;\colon\; I^{\Delta[1]} \longrightarrow \mathcal{C}
$$

from the subposet of $I \times I$ on pairs of elements $i \leq j$, such that 

1. for each $n \in I$, $F(n,n) \simeq 0$ is the [[zero object]];


1. for all $i \leq j \leq k$ the induced [[diagram]]

   $$
     \array{
        & F(i,j) &\longrightarrow& F(i,k)
        \\
        & \downarrow && \downarrow
        \\
        0 \simeq & F(j,j) &\longrightarrow& F(j,k)
     }
   $$

   is a [[homotopy pushout]] square (hence equivalently, by [[stable (infinity,1)-category|stability]], a [[homotopy pullback]]).

Write

$$
  Gap(I,\mathcal{C}) \hookrightarrow Func(I^{\Delta[1]}, \mathcal{C})
$$

for the [[full sub-(∞,1)-category]] of diagrams satisfying these conditions.

=--


This is [[Higher Algebra|Higher Algebra, def. 1.2.2.2]].

+-- {: .num_remark #MoreSquaresArePushouts}
###### Remark


The conditions in def. \ref{ChainComplexInStableInfinityCategory} imply
by the [[pasting law]] that also all squares

$$
  \array{
     F(i,k) &\longrightarrow& F(i,l)
     \\
     \downarrow && \downarrow
     \\
     F(j,k) &\longrightarrow& F(j,l)
  }
$$

for all $i \leq k$ and $k \leq l$  are [[homotopy pushout]] squares.

=--


+-- {: .num_defn #ChainComplexInducedFromZComplex}
###### Definition

Given a $\mathbb{Z}$-chain complex $F$ in $\mathcal{C}$ as in def. \ref{ChainComplexInStableInfinityCategory}, 
define a [[sequential diagram]] in the ([[triangulated category|triangulated]]) [[homotopy category of an (infinity,1)-category|homotopy category]] $Ho(\mathcal{C})$ of $\mathcal{C}$

$$
  C_\bullet

  \;\colon\;
  (\mathbb{Z}, \leq)^{op}
    \longrightarrow
  Ho(\mathcal{C})
$$

by setting

$$
  C_n \coloneqq \Sigma^{-n} F(n-1,n) \in Ho(\mathcal{C})
$$

and taking

$$
  d_n \coloneqq \Sigma^{-n} \delta_n \;\colon\; C_n \longrightarrow C_{n-1}
$$

to be the $n$-fold de-[[suspension]] of the [[connecting homomorphisms]] of the defining [[homotopy fiber sequences]]

$$
  F(n-1,n) \to F(n-1, n+1) \to F(n,n+1)
  \,,
$$

hence the $(n+1)$-fold de-[[suspension]] of the morphism $\delta_n$  in the following [[pasting]] of [[homotopy pushouts]]

$$
  \array{
    F(n-1,n) &\longrightarrow& F(n-1,n+1) &\to& 0
    \\
    \downarrow && \downarrow && \downarrow
    \\
    0 &\longrightarrow& F(n,n+1) &\stackrel{\delta_n}{\longrightarrow}& \Sigma F(n-1,n)
  }
$$

where the total outer [[homotopy pushout]] exhibits the [[suspension]] of $F(n-1,n)$, by the [[pasting law]].


=--

+-- {: .num_prop #ZComplexInCInducedChainComplexInHoC}
###### Proposition

The sequence $C_\bullet$ in def. \ref{ChainComplexInducedFromZComplex} is a [[chain complex]] in that the $d_\bullet$ are [[differentials]], hence in that for all $n \in \mathbb{Z}$ we have that the composite 

$$
  d_n \circ d_{n+1} = 0
$$


is the [[zero morphism]] in the [[triangulated category]] $Ho(\mathcal{C})$.

=--

([[Higher Algebra|Higher Algebra, remark 1.2.2.3]])

+-- {: .proof}
###### Proof

Consider the [[pasting]] [[diagram]]

$$
  \array{
    F(n-2,n) &\longrightarrow& F(n-2,n+1) &\longrightarrow& 0
    \\
    \downarrow &(c)& \downarrow && \downarrow
    \\
    F(n-1,n) &\longrightarrow& F(n-1,n+1) &\longrightarrow& 0
    \\
    \downarrow &(c)& \downarrow &(c)& \downarrow
    \\
    0 &\longrightarrow& F(n,n+1) &\underset{\delta_n}{\longrightarrow}& \Sigma F(n-1,n)
  }
$$

where the squares labeled "c" are (co-)cartesian ([[homotopy pushouts]]) ( by def. \ref{ChainComplexInducedFromZComplex} and by remark \ref{MoreSquaresArePushouts} and ). 
Notice that the [[homotopy pushout]] of the outermost [[span]] gives the [[suspension]]

$$
  \array{
     F(n-2,n) &\longrightarrow& 0
     \\
     \downarrow &(c)& \downarrow
     \\
     0 &\longrightarrow& \Sigma F(n-2,n)
  }
  \,.
$$

Therefore we have two paths of morphisms of span diagrams, the first is

$$
  \left(
    \array{
       F(n-2,n) &\to& F(n-2,n+1)
       \\
       \downarrow 
       \\
       0 
    }
  \right)
  \to
  \left(
    \array{
       F(n-2,n) &\to& 0
       \\
       \downarrow
       \\
       0 
    }
  \right)
  \to
  \left(
    \array{
       F(n-1,n) &\to& 0
       \\
       \downarrow
       \\
       0 
    }
  \right)
$$

which gives on [[homotopy pushouts]]

$$
  F(n,n+1) \longrightarrow \Sigma F(n-2,n) \longrightarrow \Sigma F(n-1,n)
$$

and the second is

$$
  \left(
    \array{
       F(n-2,n) &\to& F(n-2,n+1)
       \\
       \downarrow 
       \\
       0 
    }
  \right)
  \to
  \left(
    \array{
       F(n-1,n) &\to& F(n-1,n+1)
       \\
       \downarrow
       \\
       0 
    }
  \right)
  \to
  \left(
    \array{
       F(n-1,n) &\to& 0
       \\
       \downarrow
       \\
       0 
    }
  \right)
$$

which on homotopy pushouts is

$$
  F(n,n+1) \stackrel{\simeq}{\longrightarrow} F(n,n+1) \stackrel{\delta_n}{\longrightarrow} \Sigma F(n-1,n)
$$

(all by the [[pasting law]]). By the commutativity of the original pasting diagram these two paths are equivalent. Therefore on homotopy pushouts this exhibits a factorization of $\delta_n$ through $\Sigma F(n-2,n)$:

$$
  \array{
    F(n,n+1) &\longrightarrow& \Sigma F(n-2,n)
    \\
    & {}_{\mathllap{\delta_n}}\searrow & \downarrow
    \\
    && \Sigma F(n-1,n)
  }
  \,.
$$

Pasting this to the homotopy pushout that defines $\Sigma \delta_{n-1}$

$$
  \array{
    F(n,n+1) &\longrightarrow& \Sigma F(n-2,n)  &\longrightarrow& 0 
    \\
    & {}_{\mathllap{\delta_n}}\searrow & \downarrow &(c)& \downarrow
    \\
    && \Sigma F(n-1,n) &\underset{\Sigma \delta_{n-1}}{\longrightarrow}&
    \Sigma^2 F(n-2,n-1)
  }
$$

and then suspending the result $n$ times yields a diagram that exhibits a null-homotopy

$$
  d_{n-1}  \circ d_n \simeq 0
$$

in $\mathcal{C}$.

=--

The following proposition observes that the $\mathbb{Z}$-chain complexes of def. \ref{ChainComplexInStableInfinityCategory} are, despite the explict appearance of square diagrams, equivalently already determined by a [[sequential diagram]].

+-- {: .num_prop #ChainComplexesFromFilteredObjects}
###### Proposition

Consider the inclusion of [[posets]]

$$
  (\mathbb{Z}, \leq)
  \to 
  (\mathbb{Z}, \leq)^{\Delta[1]}  
$$

given by

$$
  n \mapsto (-\infty, n)
  \,.

$$

The induced [[(∞,1)-functor]]


$$
  Func((\mathbb{Z}\cup \{-\infty\}, \leq)^{\Delta[1]} , \mathcal{C})
  \longrightarrow
  Func((\mathbb{Z}, \leq), \mathcal{C})
$$

restricts to an [[equivalence of (∞,1)-categories|equivalence]] between the (∞,1)-category $Gap(\mathbb{Z},\mathcal{C})$ of $\mathbb{Z}\cup \{\infty\}$-chain complexes in $\mathcal{C}$ (def. \ref{ChainComplexInStableInfinityCategory}) and that of filtered objects in $\mathcal{C}$ (def. \ref{GeneralizedFilteredObject}). The equivalence is given by left and right [[(∞,1)-Kan extension]].



=--

This is [[Higher Algebra|Higher Algebra, lemma 1.2.2.4]]. 

+-- {: .num_remark #FromSequencesToZComplexes}
###### Remark

The inverse functor can be described informally as follows: 


given a filtered object $X_\bullet$, the associated chain complex $X(\bullet,\bullet)$ is given by taking each entry $X(n,n+r)$ to be given by the [[homotopy cofiber]] of $X_n \to X_{n+r}$

$$ X(n, n+r) = \operatorname{cofib}(X_n\to X_{n+r})$$

because that makes the squares

$$
  \array{
    & X(-\infty,n) &\longrightarrow& X(-\infty,n+r)
    \\
    & \downarrow && \downarrow
    \\
    0 \simeq & X(n, n) &\longrightarrow& X(n,n+r)
  }
$$

be [[homotopy pushout]] squares.


=--





### Spectral sequence of a filtered object
 {#SpectralSequenceOfAFilteredObject}

We discuss now how in the presence of [[sequential colimits]],
every [[filtered object in an (infinity,1)-category|filtered object]]
induces a [[spectral sequence]] which converges to its [[homotopy groups]], equipped with the induced filtering. The discussion for co-filtered objects is formally dual, but also spelled out [below](#SpectralSequenceOfACofilteredObject), for reference.

+-- {: .num_remark #LongExactSequencesOfHomotopyGroups}
###### Remark

Let $X_\bullet$ be a filtered object in the sense of def. \ref{GeneralizedFilteredObject}. Write $X(\bullet,\bullet)$ for the corresponding $\mathbb{Z}$-complex, according to prop. \ref{ChainComplexesFromFilteredObjects}.
Then for all $i \leq j \leq k$ there is a [[long exact sequence of homotopy groups]] in $\mathcal{A}$ of the form

$$
  \cdots \to 
  \pi_n X(i,j) 
  \to 
  \pi_n X(i,k)
  \to 
  \pi_n X(j,k)
  \to
  \pi_{n-1}X(i,j)
  \to \cdots
  \,.
$$

=--

+-- {: .num_defn #TheSpectralSequence}
###### Definition

Define for $p,q \in \mathbb{Z}$ and $r \geq 1$ an object $E_r^{p,q} \in \mathcal{A}$ by the canonical [epi-mono factorization](abelian+category#FactorizationOfMorphisms)

$$
    \pi_{p+q} X(p-r,p)
    \twoheadrightarrow
    E_r^{p,q}
    \hookrightarrow
    \pi_{p+q} X(p-1, p+r-1)
$$

in the [[abelian category]] $\mathcal{A}$, of the morphism $X((p-r,p) \leq (p-1,p+r-1))$, so that $E_r^{p,q}$ is the [[image]] of this morphism. Moreover, define [[morphisms]]

$$
  d_r \;\colon\; E_r^{p,q} \to E_r^{p-r, q+r-1}
$$

to be the restriction (the [[image]] on morphisms) of the [[connecting homomorphism]] 

$$
  \array{
     \pi_{p+q} X(p-r, p)
     &\longrightarrow&
     E_r^{p,q}
     &\longrightarrow&
     \pi_{p+q} X(p-1, p+r-1)
     \\
     {}^{\mathllap{\delta}}\downarrow && \downarrow^{\mathrlap{d_r}} && \downarrow^{\mathrlap{\delta}}
     \\
     \pi_{p+q-1} X(p-2r, p-r)
     &\longrightarrow&
     E_r^{p-r,q+r-1}
     &\longrightarrow&
     \pi_{p+q-1} X(p-r-1, p-1)
  }
$$

in the [[long exact sequence of homotopy groups]] of remark \ref{LongExactSequencesOfHomotopyGroups},

* on the left for the case $(i \leq j \leq k) = (p-2r \leq p - r \leq p)$

* on the right for the case $(i \leq j \leq k) = (p - r - 1 \leq p - 1 \leq p + r - 1)$.


=--

+-- {: .num_remark #FirstPageOfTheSpectralSequence}
###### Remark

For $r = 1$ def. \ref{TheSpectralSequence} reduces to

$$
  \begin{aligned}
    E_1^{p,q}  
      & \simeq 
    \pi_{p+q} X(p-1,p) 
      \\
      & \simeq
    \pi_{q} (\Sigma^{-p} X(p-1,p)) 
      \\
      & \simeq 
    \pi_{q} (C_{p}) 
  \end{aligned}
$$

where $C_p$ is the $p$th element in the [[chain complex]]
associated with $X(\bullet,\bullet)$ 
according to def. \ref{ChainComplexInducedFromZComplex}.

=--

([[Higher Algebra|Higher Algebra, construction 1.2.2.6]])




+-- {: .num_prop #ExistenceOfTheSpectralSequence}
###### Proposition

In def. \ref{TheSpectralSequence}
we have $d^r\circ d^r = 0$ for all $r \geq 1$ and all $p,q \in \mathbb{Z}$.

Moreover, there are [[natural isomorphisms]]
(natural in $X_\bullet$)

$$
  E_{r+1}^{p,q}
  \simeq
  \frac{
   ker(d_r \colon E_r^{p,q} \to E_r^{p-r, q+r-1})
  }{
   im(d_r \colon E_r^{p+r, q-r+1} \to E_r^{p,q})
  }
  \,.
$$

Thus, $\{E_r^{\bullet,\bullet}\}_{r\geq 1}$ is a homology [[spectral sequence]]  in the [[abelian category]] $\mathcal{A}$, functorial in the filtered object $X_\bullet$, with first page 

$$ 
  \begin{aligned}
    E_1^{p,q} 
     &= 
    \pi_{p+q} \operatorname{cofib}(X_{p-1}\to X_{p})
    \\
    & \simeq \pi_q (C_p)
  \end{aligned}
  \,.
$$

=--


([[Higher Algebra|Higher Algebra, prop. 1.2.2.7]])

+-- {: .proof}
###### Proof


Since $d_r$ is by definition the [[image]] morphism of a [[connecting homomorphism]], for showing $d_r \circ d_r = 0$ it suffices to show that the connecting homomorphisms compose to the [[zero morphism]], 
$\delta_r \circ \delta_r \simeq 0$. This is the same argument
as in the proof of prop. \ref{ZComplexInCInducedChainComplexInHoC}, generalized from vertical steps of length 1 to vertical steps of length $r$.

Explicitly, we have the pasting diagram 

$$
  \array{
    F(p-2r,p) &\longrightarrow& F(p-2r,p+1) &\longrightarrow& 0
    \\
    \downarrow &(c)& \downarrow && \downarrow
    \\
    F(p-r,n) &\longrightarrow& F(p-r,p+1) &\longrightarrow& 0
    \\
    \downarrow &(c)& \downarrow &(c)& \downarrow
    \\
    0 &\longrightarrow& F(p,p+r) &\underset{\delta_r}{\longrightarrow}& \Sigma F(p-r,p)
  }
$$

where the squares labeled "c" are (co-)cartesian ([[homotopy pushouts]]). 
By the [[universal property]] of the pushout, this induces a factorization

$$
  \array{
    F(p,p+1) &\longrightarrow& \Sigma F(p-2r,p)
    \\
    & {}_{\mathllap{\delta_r}}\searrow & \downarrow
    \\
    && \Sigma F(p-r,p)
  }
  \,.
$$

Pasting this in turn to the homotopy pushout that defines $\Sigma \delta_{p-r}$

$$
  \array{
    F(p,p+1) &\longrightarrow& \Sigma F(p-2r,p)  &\longrightarrow& 0 
    \\
    & {}_{\mathllap{\delta_r}}\searrow & \downarrow &(c)& \downarrow
    \\
    && \Sigma F(p-r,p) &\underset{\Sigma \delta_{r}}{\longrightarrow}&
    \Sigma^2 F(p-2r,p-1)
  }
$$

and then suspending the result $n$ times yields a diagram that exhibits a null-homotopy

$$
  \delta_{r}  \circ \delta_r \simeq 0
$$

in $\mathcal{C}$.

Next, to show the homology isomorphisms; consider for fixed $p,q,r$ the usual abbreviation

$$
  C \coloneqq E_r^{p,q}
$$

for the $r$-relative [[chains]],

$$
   Z \coloneqq ker(d_r \colon E_r^{p,q} \to E_r^{p-r, q+r-1})
$$

for the $r$-relative [[cycles]] and

$$
  B \coloneqq im(d_r \colon E_r^{p+r, q-r+1} \to E_r^{p,q})
$$

for the $r$-relative boundaries, all in bidegree $p,q$.

We claim that the canonical maps induce a sequence of morphisms in $\mathcal{A}$ of the form

$$
  \pi_{p+q} X(p-r-1, p)
   \stackrel{\phi}{\to}
  Z
   \stackrel{\phi'}{\to}
  Z/B
   \stackrel{\psi'}{\to}
  C/B
   \stackrel{\psi}{\to}
  \pi_{p+q} X(p-1, p+r)
$$

and that $\phi'\circ \phi$ is an [[epimorphism]] and $\psi \circ \phi'$ is a [[monomorphism]]. By the uniqueness of the [[image]] factorization in the [[abelian category]] $\mathcal{A}$, this will prove the proposition.

To see that $\pi_{p+q} X(p-r-1,p)$ is indeed in the [[kernel]] of $d_r$ consider the [[commuting diagram]]

$$
  \array{
    \pi_{p+q} X(p-r-1,p) &\longrightarrow& \pi_{p+q-1} X(p-2r, p- r-1)
    \\
    \downarrow && \downarrow & \searrow
    \\
    \pi_{p+q} X(p-r, p) &\longrightarrow& \pi_{p+q-1}X(p-2r, p-r)
    \\
    \downarrow && \downarrow 
    \\
    E_r^{p,q} &\stackrel{d_r}{\longrightarrow}& E_r^{p-r, q+r-1}
    && \pi_{p+q-1} X(p - 2r, p-r)
    \\
    && \downarrow & \swarrow
    \\
    && \pi_{p+q-1} X(p - r - 1, p - 1)
  }
  \,.
$$

Since the bottom right morphism is a [[monomorphism]] by construction, the claim is equivalently that the total composite from top-left to bottom right is zero. By commutativity of the diagram this factors through the composite from top-right to bottom-right. As indicated, this in turn factors through two consecutive morphisms of an $(i \leq j \leq k)$-square, which by definition of $\mathbb{Z}$-chain complex is null-homotopic.

By a dual argument one has that $\pi_{p+q}X(p-1, p+r)$ is in the [[coimage]] of $d_r$. This shows that we indeed have the above sequence of morphisms $\stackrel{\phi}{\to}\stackrel{\phi'}{\to}\stackrel{\psi'}{\to}\stackrel{\psi}{\to}$.

It now remains to show that $\phi$ is an [[epimorphism]] (dually $\psi$ will be a [[monomorphism]].) (...[[Higher Algebra|Higher Algebra, p. 41]]...)


=--

We can now consider the convergence of the spectral sequence of prop. \ref{ExistenceOfTheSpectralSequence}. To state that efficiently, first consider the following definition

+-- {: .num_defn #FilteringOnHomotopyGroups}
###### Definition

Given a [[filtered object in an (∞,1)-category|filtered object]], def. \ref{GeneralizedFilteredObject}, $X \simeq \underset{\longrightarrow}{\lim}_n X_n \in \mathcal{C}$, say that the induced [[filtered object|filtering]] on its [[homotopy groups]] $F^\bullet \pi_\bullet X$ is given by the [[images]] of the homotopy groups of the [[strata]] of $X$

$$
  F^p \pi_{p+q}X 
   \coloneqq
  im\left(
    \pi_{p+q} X_{p} \to \pi_{p+q} X
  \right)
  \,\,\,
  \in \mathcal{A}
  \,.
$$

=--

([[Higher Algebra|Higher Algebra, p. 43]])

+-- {: .num_prop #ConvergenceOfTheSpectralSequence}
###### Proposition

Assume that  $\mathcal{C}$ admits all [[sequential colimits]] and that $\pi$ preserves these. Let $X \simeq \underset{\longrightarrow}{\lim}_n X_n$ be a [[filtered object in an (∞,1)-category|filtered object]], def. \ref{GeneralizedFilteredObject}, for filtering with $X_{n \lt 0} \simeq 0$. Then the spectral sequence of prop. \ref{ExistenceOfTheSpectralSequence}, converges to the [[homotopy groups]] of $X$

$$ 

    E_1^{p,q} 
    = 
    \pi_{p+q} \operatorname{cofib}(X_{p-1}\to X_{p})
    \simeq \pi_q (C_p)
    \;\;\Rightarrow\;\;
    \pi_{p+q} X
  \,,
$$

where the first page is identified following remark \ref{FirstPageOfTheSpectralSequence}.

In detail, for all $p,q \in \mathbb{Z}$ the [[differentials]] $d_r \colon E_r^{p,q} \to E_r^{p-r, q+r-1}$ vanish for $r \gt p$, and the [[colimit]] (in $\mathcal{A}$)

$$
  E^{p,q}_\infty \coloneqq \underset{\longrightarrow}{\lim}_{r \gt p} E_r
$$

is [[isomorphism|isomorphic]] to the [[associated graded object]] of the filtered homotopy groups of def. \ref{FilteringOnHomotopyGroups}:

$$
  E^{p,q}_\infty \simeq F^p \pi_{p+q}(X) / F^{p-1} \pi_{p+q}(X)
  \,.
$$

=--

This is due to ([[Higher Algebra|Higher Algebra, prop. 1.2.2.14]]). A quick review is in ([Wilson 13, theorem 1.2.1](#Wilson13)).

+-- {: .proof}
###### Proof

The assumption $X_{n \lt 0} \simeq 0$  implies that for $i,j \lt 0$ we have, by remark \ref{FromSequencesToZComplexes},

$$
  X(i,j) \simeq cofib(X_i \to X_j) \simeq 0 \;\;\;\; for\, i,j \lt 0
$$

and therefore it follows that $E_r^{p-r,q+r-1}$, being a [[quotient]] of $\pi_{p+q} X(p-2r, p-r)$, vanishes for $r \gt p$.

The same assumption implies that 

$$
  X(p-r,p) \simeq X_p \;\;\;\; for\, p \gt r
$$

and so $E_\infty^{p,q}$ is 

$$
  E_\infty^{p,q} 
    \simeq 
  im\left(
    \pi_{p+q} X_p \to \pi_{p+q} Y
  \right)
$$

for 

$$
  Y \coloneqq \underset{\longrightarrow}{\lim}_r X(p-1,p+r)
  \,.
$$

We need to show that this image is the [[associated graded object]] of the filtered homotopy groups.

To that end, observe that the [[homotopy fiber sequences]] 

$$
  X_{p-1} \to X_{p+r} \to X(p-1,p+r)
$$ 

for all $r$ give a homotopy fiber sequence under the colimit over $r$ of the form

$$
  X_{p-1} \to X \to Y
  \,.
$$

The corresponding [[long exact sequence of homotopy groups]] 
truncates on the left to read

$$
  0 \to F^{p-1} \pi_{p+q}(X) \stackrel{ker(f')}{\hookrightarrow} \pi_{p+q} X \stackrel{f'}{\to} \pi_{p+q}Y
  \,.
$$

By construction the morphism $f'$ appearing here factors the morphism $f$ whose image we need to compute as


$$
  \array{
    && \pi_{p+q}X
    \\
    & {}^{\mathllap{g}}\nearrow && \searrow^{\mathrlap{f'}}
    \\
    \pi_{p+q} X(p)
    && 
      \stackrel{f}{\longrightarrow}
    &&
    \pi_{p+q} Y
  }
$$

Using these relation we can now express $E_\infty^{p,q} \simeq im(f)$ as:

$$
  \begin{aligned}
    E_\infty^{p,q}
      & \simeq
    im(f)
      \\
      & \simeq
    im(f'|_{im(g)})
      \\
      & \simeq
    im(f'|_{F^p \pi_{p+q} X})
      \\
       & \simeq
     F^p \pi_{p+q}X/ker(f')
      \\
      & \simeq 
     F^p \pi_{p+q} X/F^{p-1} \pi_{p+q}X
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

While historically the appearances of the root "spectr-" in "[[spectral sequence]]" and in "[[spectrum]]" ([[stable homotopy types]]) are unrelated, 
prop. \ref{ExistenceOfTheSpectralSequence} and prop. \ref{ConvergenceOfTheSpectralSequence} say that there is a lucky coincidence of terminology: 

_Every sequence of spectra manifests itself on homotopy groups in a spectral sequence_.

Moreover, the discussion below in _[Examples](#Examples)_ shows that also conversely, essentially every spectral sequence that appears in practice comes from a sequence of spectra this way.

(See also the title of ([Wilson 13](#Wilson13))).

=--

+-- {: .num_remark }
###### Remark

The spectral sequence above itself only actually depends to the [[triangulated category|triangulated]] [[homotopy category of an (infinity,1)-category|homotopy category]] $Ho(\mathcal{C})$. But its $\infty$-functorial dependence on the filtered object needs the full structure of the [[(∞,1)-category]] $\mathcal{C}$

=--



### Spectral sequence of a cofiltered object
 {#SpectralSequenceOfACofilteredObject}

We discuss here the dual notion to the spectral sequence
of a filtered object above, now for a cofiltered object.

> The following does not just dualize but also change the indexing convention on top of dualization. Needs further discussion/harmonization.


+-- {: .num_prop}
###### Proposition

Consider the inclusion of [[posets]]

$$
  (\mathbb{Z}, \leq)
  \to 
  (\mathbb{Z}\cup \{\infty\}, \leq)^{\Delta[1]}
$$

given by

$$
  n \mapsto (n,\infty)
  \,.

$$

The induced [[(∞,1)-functor]]

$$
  Func((\mathbb{Z}\cup \{\infty\}, \leq)^{\Delta[1]}, \mathcal{C})
  \longrightarrow
  Func((\mathbb{Z}, \leq), \mathcal{C})
$$

restricts to an [[equivalence of (∞,1)-categories|equivalence]] between the (∞,1)-category of $\mathbb{Z}\cup \{\infty\}$-chain complexes in $\mathcal{C}$ (def. \ref{ChainComplexInStableInfinityCategory}) and that of generalized filtered objects in $\mathcal{C}$ (def. \ref{GeneralizedFilteredObject}).

=--

Given a filtered object $X_\bullet$, the associated chain complex $X(\bullet,\bullet)$ is given by the [[homotopy fiber]]

$$ X(n, n+r) = \operatorname{fib}(X_n\to X_{n+r}). $$


+-- {: .num_defn #ExactCoupleForFilteredObject}
###### Definition

For a cofiltered object $X_\bullet$, def. \ref{GeneralizedFilteredObject}, write 

$$
  K_n \coloneqq fib(X_n \to X_{n+1})
$$

for the [[homotopy fiber]] of the $n$th structure map, for all $n \in \mathbb{Z}$, and define an [[exact couple]]

$$
  \array{
    && \pi_\bullet(K_\bullet)
    \\
    & \swarrow && \nwarrow
    \\
    \pi_\bullet(X_\bullet)
    && 
       \stackrel{}{\longrightarrow}
    && 
    \pi_\bullet(X_\bullet)
  }
$$

where the maps are given by the long exact sequences

$$
  \cdots
  \to
  \pi_\bullet(X_{n+1})
  \to 
  \pi_\bullet(K_n) \to  \pi_\bullet(X_n) \to \pi_\bullet(X_{n+1}) \to \pi_{\bullet+1}(K_n) \to \cdots
$$

=--

This exact couple gives rise in the usual way to a spectral sequence. 


Let $X_\bullet$ be a cofiltered object.

+-- {: .num_defn }
###### Definition

Define for $p,q \in \mathbb{Z}$ and $r \geq 1$ the object $E^r_{p,q}$ by the canonical [epi-mono factorization](abelian+category#FactorizationOfMorphisms)

$$
    \pi_{p} X(q-r+1,q+1)
    \twoheadrightarrow
    E^r_{p,q}
    \hookrightarrow
    \pi_{p} X(q, q+r)
$$

in the abelian category $\mathcal{A}$, and define the [[differential]]

$$
  d^r \;\colon\; E_{p,q}^r \to E_{p-1, q-r}^r
$$

to be the restriction of the [[connecting homomorphism]]

$$
 \pi_{p} X(q,q+r) \to \pi_{p-1} X(q-r, q)
$$

from the long exact sequence of remark \ref{LongExactSequencesOfHomotopyGroups},  
for the case  $i=q-r$, $j=q$, and $k=q+r$.

=--

+-- {: .num_prop}
###### Proposition

$d^r\circ d^r = 0$ and there are natural (in $X_\bullet$) isomorphisms

$$
E^{r+1}\cong \operatorname{ker}(d^r)/\operatorname{im}(d^r).
$$

Thus, $\{E^r_{*,*}\}_{r\geq 1}$ is a bigraded [[spectral sequence]]  in the [[abelian category]] $\mathcal{A}$, functorial in the filtered object $X_\bullet$, with

$$ E^1_{p,q} = \pi_p \operatorname{fib}(X_q\to X_{q+1}), \qquad d^r: E^r_{p,q}\to E^r_{p-1,q-r}. $$

=--

If [[sequential limits]] and [[sequential colimits]] exist in $\mathcal{A}$, we can form the limiting term $E^\infty_{*,*}$ of this spectral sequence.

On the other hand, the [[graded object]] $\pi_\bullet (X)$ admits a [[filtered object|filtration]] by

$$ F_q \pi_p (X) = \operatorname{ker}(\pi_p (X)\to \pi_p(X_q)) $$

and we would like to compare $E^\infty_{*,*}$ with the [[associated graded]] of this filtration. We say that 

+-- {: .num_defn #WeakAndStrongConvergence}
###### Definition

The spectral sequence **converges weakly** if there is a canonical isomorphism

$$ E^\infty_{p,q} \cong F_q\pi_p(X)/ F_{q-1}\pi_p(X) $$

for every $p,q\in\mathbb{Z}$. 

We say that the spectral sequence **converges strongly** if it converges weakly and if, in addition, the filtration $F_\bullet\pi_p(X)$ is complete on both sides, that is:

$$
\underset{\rightarrow}{\lim}_q F_q\pi_p (X)
\simeq
\pi_p(X)
\simeq
\underset{\leftarrow}{\lim}_q F^q\pi_p (X),
$$

where $F^\bullet$ is the cofiltration.

=--

+-- {: .num_remark}
###### Remark

The meaning of the word *canonical* in def. \ref{WeakAndStrongConvergence} is somewhat subtle since, in general, there is no map from one side to the other. However, there always exists a canonical *[[relation]]* between the two, and we ask that this relation be an isomorphism (see [Hilton-Stammbach, VIII.7](#HiltonStammbach)).

=--


+-- {: .num_prop #FiltrationSpectralSequence}
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]] and let $\pi:\mathcal{C}\to\mathcal{A}$ be a homological functor where $\mathcal{A}$ is an [[abelian category]] which admits [[sequential limits]]. Let $X_\bullet$ be a filtered object in $\mathcal{C}$ such that $\underset{\leftarrow}{\lim} X_\bullet$ exists. Suppose further that:


1. For every $n$, the diagram $r\mapsto \operatorname{fib}(X_{n-r}\to X_n)$ has a limit in $\mathcal{C}$ and that limit is preserved by $\pi$.
2. For every $n$, $\pi_n(X_r)=0$ for $r\gg 0$.

Then the [[spectral sequence]] $\{E^r_{*,*}\}_{r\geq 1}$ in $\mathcal{A}$ converges strongly (def. \ref{WeakAndStrongConvergence}). We write:

$$
  E_{p,q}^1
  =
  \pi_{p} \operatorname{fib}(X_q\to X_{q+1})
  \Rightarrow
  \pi_{p} (\underset{\leftarrow}{\lim} X_\bullet) 
$$

=--

There is also a dual statement in which limits are replaced by colimits, but it is in fact a special case of the proposition with $\pi$ replaced by $\pi^{op}$. A proof of this proposition (in dual form) is given in ([[Higher Algebra|Higher Algebra, prop. 1.2.2.14]]). Review is in ([Wilson 13, theorem 1.2.1](#Wilson13)).


## Examples
 {#Examples}


### General

[[!include Lurie spectral sequences -- table]]


+-- {: .num_example }
###### Example

For $\mathcal{A}$ a good [[abelian category]] and $\mathcal{C} = Ch_\bullet(\mathcal{A})$ the [[(∞,1)-category of chain complexes]] in $\mathcal{A}$, we recover, by \ref{FilteredObjectInModelCategory},
the traditional notion of a _[[spectral sequence of a filtered complex]]_.

=--

([[Higher Algebra|Higher Algebra, example 1.2.2.11]]).

+-- {: .num_example }
###### Example

Let $\mathcal{C} = Spec^{op}$ be the opposite (∞,1)-category of spectra, let $\mathcal{A}$ be the opposite category of abelian groups, and let $\pi$ be the functor $[K,-]$ where $K$ is spectrum. Then condition (1) in Proposition \ref{FiltrationSpectralSequence} holds for all filtered objects if and only if $K$ is a [[finite spectrum]]. When the filtered object is the [[Whitehead tower]] of a spectrum $E$, the associated spectral sequence is the [[Atiyah-Hirzebruch spectral sequence]] with target $E^*(K)$. It is thus strongly convergent if $K$ is a finite spectrum.

=--


+-- {: .num_example #SpectralSequenceOfASimplicialStableHomotopyType}
###### Example


For $\mathcal{C}$ a [[stable (∞,1)-category]] and $X_\bullet$ a [[simplicial object in an (∞,1)-category]] in $\mathcal{C}$, then the [[simplicial skeleta]] of $X$ give it the structure of a [[filtered object in an (∞,1)-category]]. The corresponding [[spectral sequence of a filtered stable homotopy type]] has as its first page the [[Moore complexes]] of the corresponding [[simplicial objects]] of [[homotopy groups]].

See at _[[spectral sequence of a simplicial stable homotopy type]]_.

=--

As a special case of example \ref{SpectralSequenceOfASimplicialStableHomotopyType} we have:

+-- {: .num_example }
###### Example

The $E$-based [[Adams spectral sequence]] that approximates homotopy classes of maps between two spectra $X$ and $Y$ using a [[ring spectrum]] $E$ is a special case of the above spectral sequence, with $\mathcal{C}=Spec$, $\pi=[X,-]$, and the filtered object associated with the cosimplicial spectrum $E^{\wedge\bullet+1}\wedge Y$. Bousfield's theorems on the convergence of the Adams spectral sequence can be rephrased as giving sufficient conditions on $X$, $Y$, and $E$ for condition (1) in Proposition \ref{FiltrationSpectralSequence} to hold (see [Bousfield, Theorems 6.6 and 6.10](#Bousfield)).

See _[[J-homomorphism and chromatic homotopy]]_ for an exposition.

=--


### Canonical cosimplicial resolution of $E_\infty$-algebras
 {#CanonicalCosimplicialResolutionOfEInfinityAlgebras}

We discuss now the special case of coskeletally filtered 
totalizations coming from the canonical cosimplicial objects
induced from [[E-∞ algebras]] (dual [[Cech nerves]]/[[Sweedler corings]]/[[Amitsur complexes]]).

In this form this appears as ([Lurie 10, theorem 2](#LurieLecture)). A review is in ([Wilson 13, 1.3](#Wilson13)). For the analog of this in the traditional formulation see ([Ravenel, ch. 3, prop. 3.1.2](#Ravenel)).


+-- {: .num_defn #FiltrationOfTotalizationByTotalizationOfCoskeleta}
###### Definition

Given an [[cosimplicial object in an (∞,1)-category]]  with [[(∞,1)-colimits]]

$$
  Y \;\colon\; \Delta  \longrightarrow \mathcal{C}
$$

its [[totalization]] $Tot Y \simeq \underset{\leftarrow}{\lim}_n Y_n$
is [[filtered object in an (infinity,1)-category|filtered]], def. \ref{GeneralizedFilteredObject}, by the 
totalizations of its [[coskeleta]]

$$
  Tot Y 
  \to 
  \cdots 
  \to 
  Tot (cosk_2 Y) 
  \to
  Tot (cosk_1 Y) 
  \to
  Tot (cosk_0 Y) 
  \to 0
  \,.
$$

=--

+-- {: .num_defn #SpectralSequenceOfSimplicialStableHomotopyType}
###### Definition

The [[spectral sequence of a filtered stable homotopy type|filtration spectral sequence]], prop. \ref{FiltrationSpectralSequence},
applied to the filtration of a [[totalization]] by [[coskeleton|coskeleta]] as in def. \ref{FiltrationOfTotalizationByTotalizationOfCoskeleta}, we call the _[[spectral sequence of a simplicial stable homotopy type]]_.

=--


([[Higher Algebra|Higher Algebra, prop. 1.2.4.5]])

+-- {: .num_prop #E2PageByMooreComplex}
###### Proposition

The [[spectral sequence of a simplicial stable homotopy type]] has as first page/$E_1$-term the [[cohomology groups]] of the [[Moore complex]] associated with the [[cosimplicial objects]] of [[homotopy groups]]

$$
  E_2^{p,q}
  = 
  H^p(\pi_q(Tot (cosk_\bullet(Y))))
  \Rightarrow
  \pi_{p-q} Tot(Y)
  \,.
$$

=--

By the discussion at _[[∞-Dold-Kan correspondence]]_ and _[[spectral sequence of a filtered stable homotopy type]]_. This appears as ([[Higher Algebra|Higher Algebra, remark 1.2.4.4]]). Review is around  ([Wilson 13, theorem 1.2.4](#Wilson13)).




+-- {: .num_defn}
###### Definition

Let $S$ be an [[E-∞ ring]] and let $E$ be an [[E-∞ algebra]] over $S$, hence an [[E-∞ ring]] equipped with a [[homomorphism]]

$$
  S \longrightarrow E
  \,.
$$

The _canonical [[cosimplicial object]]_ 
associated to this (the $\infty$-[[Cech nerve]]/[[Sweedler coring]]/[[Amitsur complex]]) is that given by the iterated [[smash product]]/[[tensor product]] over $S$:

$$
  E^{\wedge^{\bullet+1}_S} \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

More generally, for $X$ an $S$-[[∞-module]], the canonical [[cosimplicial object]] is

$$
  E^{\wedge^{\bullet+1}_S}\wedge_S X \;\colon\; \Delta \to \mathcal{C}
  \,.
$$

=--

+-- {: .num_prop #FlatnessCondition}
###### Proposition

If $E$ is such that the self-[[generalized homology]] 
$E_\bullet(E) \coloneqq \pi_\bullet(E \wedge_S E)$ (the dual $E$-[[Steenrod operations]]) is such that as a [[module]] over $E_\bullet \coloneqq \pi_\bullet(E)$ it is a [[flat module]], then there is a [[natural equivalence]]

$$
  \pi_\bullet
  \left(
    E^{\wedge^{n+1}_S}
    \wedge_S 
    X
  \right)
  \simeq
  E_\bullet(E^{\wedge^n_S})
  \otimes_{E_\bullet}
  E_\bullet(X)
  \,.
$$

=--

Reviewed for instance as ([Wilson 13, prop. 1.3.1](#Wilson13)).

+-- {: .num_remark}
###### Remark

This makes $(E_\bullet, E_\bullet(E))$ be 
the [[commutative Hopf algebroid]]
formed by the  $E$-[[Steenrod algebra]]. See there for more on this.

=--

+-- {: .num_example}
###### Example

The condition in prop. \ref{FlatnessCondition} is
satisfied for 

* $E = H \mathbb{F}_p$ an [[Eilenberg-MacLane spectrum]] with $mod\;p$ [[coefficients]];

* $E = B P$ the [[Brown-Peterson spectrum]];

* $E = MU$ the [[complex cobordism cohomology theory|complec cobordism spectrum]].

It is NOT satisfied for

* $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]] for [[integer|integers]] [[coefficients]];

* $E = M S U$.

=--

+-- {: .num_remark #ExtGroupsByMooreComplex}
###### Remark

Under good conditions (...), $\pi_\bullet$ of the canonical [[cosimplicial object]] provides a [[resolution]] of [[comodule]] [[tensor product]] and hence computes the [[Ext]]-groups over the [[commutative Hopf algebroid]]:

$$
  H^p(\pi_q(Tot(cosk_\bullet(E^{\wedge^{\bullet+1}_S } \wedge_S X))))
  \simeq
  Ext^p_{E_\bullet(E)}(\Sigma^q E_\bullet, E_\bullet(X))
  \,.
$$

(...)

=--


+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

There is a canonical map

$$
  L_E X \stackrel{}{\longrightarrow} \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the [[totalization]].


=--

([Lurie 10, lecture 30, prop. 1](LurieLecture))


We consider now conditions for this morphism to be an [[equivalence]].

+-- {: .num_defn #CoreOfARing}
###### Definition

For $R$ a [[ring]], its _core_ $c R$ is the [[equalizer]] in

$$
  c R 
    \longrightarrow 
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,.
$$

=--

+-- {: .num_prop #SufficientConditionsForTotalizationToBeELocalization}
###### Proposition

Let $E$ be a [[connective spectrum|connective]] [[E-∞ ring]] such that the core or $\pi_0(E)$, def. \ref{CoreOfARing} is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \matbb{Z}[J^{-1}]$;

* $\mathbb{Z}_n$ for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X \stackrel{\simeq}{\longrightarrow} 
  \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
  \,.
$$

=--


([Bousfield 79](Bousfield+localization+of+spectra#Bousfield79), [Lurie 10, lecture 30, prop. 3](LurieLecture), [Lurie 10, lecture 31, ](LurieLecture)).






## References

The general theory is set up in section 1.2.2 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_.

A quick exposition of that is for instance in section 1.2 of

* [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php) ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}


The case of the derived category of an arbitrary abelian category is discussed in details in Chapter VIII of

* P. Hilton, U. Stammbach, *A Course in Homological Algebra*, Graduate Texts in Mathematics 4
{#HiltonStammbach}


The traditional discussion of the [[Adams spectral sequence]] in this style originates in

* [[Aldridge Bousfield]], *The localization of spectra with respect to homology*, Topology vol 18 (1979) ([pdf](http://www.math.uwo.ca/~mfrankla/Bousfield_LocalnSpectraHomol.pdf))
{#Bousfield}

see also at _[[Bousfield localization of spectra]]_. The formulation of this in modern [[chromatic homotopy theory]] is discussed in

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, lecture notes (2010)
 {#LurieLecture}



[[!redirects spectral sequence of a filtered object in a stable (∞,1)-category]]
[[!redirects spectral sequence of a filtered object in a stable (infinity,1)-category]]

[[!redirects filtered stable homotopy type]]
[[!redirects filtered stable homotopy types]]

[[!redirects Lurie spectral sequence]]
[[!redirects Lurie spectral sequences]]