
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

Each [[filtered object|filtering]] on an [[object]] in a suitable [[stable (∞,1)-category]] (e.g. a [[stable homotopy type]]) induces a [[spectral sequence]] which under suitable conditions computes the [[homotopy groups]] of this object.

This is a generalization of the traditional [[spectral sequence of a filtered complex]].

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

### Filtered objects and their associated chain complexes

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


+-- {: .num_remark}
###### Remark

If $\mathcal{C}$ is [[presentable (infinity,1)-category|presented]] by a 
sufficiently nice [[model category]] $C$ (for instance a [[combinatorial  model category]]), then [[(∞,1)-colimits]] in $\mathcal{C}$ are computed by [[homotopy colimits]] in $C$. These in turn are computed as ordinary [[colimits]] in $C$ over a cofibrant [[diagram]] in the [[projective model structure on functors]]. 

Specifically, as discussed at _[homotopy limit -- Examples -- Over sequential diagrams](homotopy+limit#SequentialHocolims)_ a cofibrant resolution of a [[sequential diagram]] $(\mathbb{N}, \leq) \to C$ is a sequential diagram all whose whose objects are cofibrant and all whose morphisms are cofibrations in $C$

$$
  \cdots \to X^C_{n-1} \stackrel{cof}{\to} X_{n}^C \stackrel{cof}{\to} X_{n+1}^C \to \cdots
  \,,
$$

where $X_n^C \in C$ denotes an object in the model category presenting the given object $X_n \in \mathcal{C}$. 

Moreover, in many [[model categories]] that appear in practice the cofibrations are in particular [[monomorphisms]] (for instance, by definition, in all [[Cisinski model structures]]). In these cases then a filtering on an object $X \in \mathcal{C}$ in the abstract sense of [[(∞,1)-categories]] is presented by a [[filtered object]] $X^C \in C$ in the sense of plain [[category theory]].

The intrisnic definition \ref{GeneralizedFilteredObject} makes manifest however that the [[monomorphism]]-aspect here is just a means of a presentation of the filtering and not an intrinsic aspect of the [[homotopy theory]]. 
 
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

+-- {: .num_remark}
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


+-- {: .num_defn #ChanComplexInducedFromZComplex}
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

The sequence $C_\bullet$ in def. \ref{ChanComplexInducedFromZComplex} is a [[chain complex]] in that the $d_\bullet$ are [[differentials]], hence in that for all $n \in \mathbb{Z}$ we have that the composite 

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

where the squares labeled "c" are (co-)cartesian ([[homotopy pushouts]]). 
By the [[universal property]] of the pushout applied to the [[cocone]] given by the defining [[homotopy pushout]] of the [[suspension]]

$$
  \array{
     F(n-2,n) &\longrightarrow& 0
     \\
     \downarrow && \downarrow
     \\
     0 &\longrightarrow& \Sigma F(n-2,n)
  }
$$

we obtain maps $F(n-1, n+1) \to \Sigma F(n-2,n)$ and $F(n, n+1) \to \Sigma F(n-2,n)$ fitting into a diagram of the form

$$
  \array{
    F(n-1, n+1) && \longrightarrow && 0
    \\
    \downarrow  & \searrow && \swarrow & \downarrow
    \\
    && \Sigma F(n-2,n)
    \\
    \downarrow  & \nearrow && \searrow & \downarrow    
    \\
    F(n,n+1) && \underset{\delta_n}{\longrightarrow} && \Sigma F(n-1,n)
  }
  \,.
$$

In particular this is a factorization of $\delta_n$ through $\Sigma F(n-2,n)$:

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

Pasting this in turn to the homotopy pushout that defines $\Sigma \delta_{n-1}$

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

Dually:

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

This is [[Higher Algebra|Higher Algebra, lemma 1.2.2.4]]. 

+-- {: .num_remark}
###### Remark

The inverse functor can be described informally as follows: 

given a filtered object $X_\bullet$, the associated chain complex $X(\bullet,\bullet)$ is given by the [[homotopy cofiber]]

$$ X(n, n+r) = \operatorname{cofib}(X_n\to X_{n+r})$$

making the square

$$
  \array{
    & X(-\infty,n) &\longrightarrow& X(-\infty,n+r)
    \\
    & \downarrow && \downarrow
    \\
    0 \simeq & X(n, n) &\longrightarrow& X(n,n+r)
  }
$$

be a [[homotopy pushout]].

Dually:

given a filtered object $X_\bullet$, the associated chain complex $X(\bullet,\bullet)$ is given by the [[homotopy fiber]]

$$ X(n, n+r) = \operatorname{fib}(X_n\to X_{n+r}). $$

=--


### The exact couple


+-- {: .num_defn #ExactCoupleForFilteredObject}
###### Definition

For a generalized filtered object $X_\bullet$, def. \ref{GeneralizedFilteredObject}, write 

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

### The spectral sequence

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

Define for $p,q \in \mathbb{Z}$ and $r \geq 1$ the object $E_r^{p,q} \in \mathcal{A}$ by the canonical [epi-mono factorization](abelian+category#FactorizationOfMorphisms)

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

to be the restriction (the [[image]] on morphisms) of the [[connecting homomorphism]] in the [[long exact sequence of homotopy groups]]

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

from the [[long exact sequence of homotopy groups]] of remark \ref{LongExactSequencesOfHomotopyGroups}, for the case  
$i=p-2r$, $j=p-r$, and $k=p$ on the left and $i = p - r - 1$, $j = p-1$ and $k = p + r -1$ on the right.


=--

+-- {: .num_remark}
###### Remark

For $r = 1$ in def. \ref{TheSpectralSequence} we have

$$
  E_1^{p,q} = \pi_{p+q} X(p-1,p) = \pi_{q} C_{p} 
$$

where $C_p$ on the right is the $p$th element in the [[chain complex]]
associated with $X(\bullet,\bullet)$ 
according to def. \ref{ChanComplexInducedFromZComplex}.

=--

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


([[Higher Algebra|Higher Algebra, construction 1.2.2.6]])


+-- {: .num_prop}
###### Proposition

$d^r\circ d^r = 0$ and there are natural (in $X_\bullet$) isomorphisms

$$
E^{r+1}\cong \operatorname{ker}(d^r)/\operatorname{im}(d^r).
$$

Thus, $\{E^r_{*,*}\}_{r\geq 1}$ is a bigraded [[spectral sequence]]  in the [[abelian category]] $\mathcal{A}$, functorial in the filtered object $X_\bullet$, with

$$ E^1_{p,q} = \pi_p \operatorname{fib}(X_q\to X_{q+1}), \qquad d^r: E^r_{p,q}\to E^r_{p-1,q-r}. $$

=--

Dually:

+-- {: .num_prop}
###### Proposition

In def. \ref{TheSpectralSequence}
we have $d^r\circ d^r = 0$ for all $r \geq 1$ and all $p,q \in \mathbb{Z}$.

Moreover, there are [[natural isomorphisms]]
(natural in $X_\bullet$)

$$
  E_{r+1}^{p,q}
  \simeq
  \frac{
   ker(d_r \colon E_r^{p,1} \to E_r^{p-r, q+r-1})
  }{
   im(d_r \colon E_r^{p+r, q-r+1} \to E_r^{p,q})
  }
  \,.
$$

Thus, $\{E_r^{*,*}\}_{r\geq 1}$ is a bigraded [[spectral sequence]]  in the [[abelian category]] $\mathcal{A}$, functorial in the filtered object $X_\bullet$, with

$$ 
  E_1^{p,q} = \pi_{p+q} \operatorname{cofib}(X_p\to X_{p+1}), 
$$

=--


([[Higher Algebra|Higher Algebra, prop. 1.2.2.7]])

+-- {: .proof}
###### Proof


Since $d_r$ is by definition the [[image]] morphism of a [[connecting homomorphism]], for showing $d_r \circ d_r = 0$ it suffices to show that the connecting homomorphisms compose to the [[zero morphism]], 
$\delta_r \circ \delta_r \simeq 0$. This is the same kind of argument
as in the proof of prop. \ref{ZComplexInCInducedChainComplexInHoC}.

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
By the [[universal property]] of the pushout applied twice, this induces a factorization

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

Next, to show the homology isomorphisms (...)

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

For the traditional statement in the [[category of chain complexes]] see at _[[spectral sequence of a filtered complex]]_.

## Examples


+-- {: .num_example }
###### Example

Let $\mathcal{C} = Spec^{op}$ be the opposite (∞,1)-category of spectra, let $\mathcal{A}$ be the opposite category of abelian groups, and let $\pi$ be the functor $[K,-]$ where $K$ is spectrum. Then condition (1) in Proposition \ref{FiltrationSpectralSequence} holds for all filtered objects if and only if $K$ is a [[finite spectrum]]. When the filtered object is the [[Whitehead tower]] of a spectrum $E$, the associated spectral sequence is the [[Atiyah-Hirzebruch spectral sequence]] with target $E^*(K)$. It is thus strongly convergent if $K$ is a finite spectrum.

=--

+-- {: .num_example }
###### Example

The $E$-based [[Adams spectral sequence]] that approximates homotopy classes of maps between two spectra $X$ and $Y$ using a [[ring spectrum]] $E$ is a special case of the above spectral sequence, with $\mathcal{C}=Spec$, $\pi=[X,-]$, and the filtered object associated with the cosimplicial spectrum $E^{\wedge\bullet+1}\wedge Y$. Bousfield's theorems on the convergence of the Adams spectral sequence can be rephrased as giving sufficient conditions on $X$, $Y$, and $E$ for condition (1) in Proposition \ref{FiltrationSpectralSequence} to hold (see [Bousfield, Theorems 6.6 and 6.10](#Bousfield)).

=--

[[!include Lurie spectral sequences -- table]]

## References

The general theory is set up in section 1.2.2 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_.

The case of the derived category of an arbitrary abelian category is discussed in details in Chapter VIII of

* P. Hilton, U. Stammbach, *A Course in Homological Algebra*, Graduate Texts in Mathematics 4
{#HiltonStammbach}

A quick exposition is for instance in section 1.2 of

* [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php) ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}

For the case of the Adams spectral sequence, see

* [[Aldridge Bousfield]], *The localization of spectra with respect to homology*, ([pdf](http://www.math.uwo.ca/~mfrankla/Bousfield_LocalnSpectraHomol.pdf))
{#Bousfield}

[[!redirects spectral sequence of a filtered object in a stable (∞,1)-category]]
[[!redirects spectral sequence of a filtered object in a stable (infinity,1)-category]]

[[!redirects filtered stable homotopy type]]
[[!redirects filtered stable homotopy types]]

[[!redirects Lurie spectral sequence]]
[[!redirects Lurie spectral sequences]]