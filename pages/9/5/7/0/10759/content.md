
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
simply a [[sequential diagram]] $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

$$
  \cdots
  X_{n-1} \to X_n \to X_{n+1} \to \cdots
  \,.
$$

=--

This appears as ([[Higher Algebra|Higher Algebra, def. 1.2.2.9]]).

We will take the view that the object being filtered is the [[homotopy limit]]

$$
  X \coloneqq \underset{\leftarrow}{\lim}_n X_n.
$$

We could also consider the sequential diagram as a filtering of its [[homotopy colimit]], but this is really an equivalent point of view since we can replace $\mathcal{C}$ by $\mathcal{C}^{op}$.


+-- {: .num_defn #ChainComplexInStableInfinityCategory}
###### Definition

Let $I$ be a [[linearly ordered set]]. An $I$-chain complex in a [[stable (∞,1)-category]] $\mathcal{C}$ is an [[(∞,1)-functor]]

$$
  F \;\colon\; I \times I \longrightarrow \mathcal{C}
$$

such that 

1. for each $n \in I$, $F(n,n) \simeq 0$ is the [[zero object]];

1. for all $i \leq j \leq k$ the induced [[diagram]]

   $$
     \array{
        F(i,j) &\longrightarrow& F(i,k)
        \\
        \downarrow && \downarrow
        \\
        F(j,j) &\longrightarrow& F(j,k)
     }
   $$

   is a [[homotopy pullback]] square.

=--

This is [[Higher Algebra|Higher Algebra, def. 1.2.2.2]].


+-- {: .num_remark }
###### Remark

Given a $\mathbb{Z}$-chain complex $F$ in $\mathcal{C}$ as in def. \ref{ChainComplexInStableInfinityCategory}, 
setting

$$
  C_n \coloneqq \Sigma^{-n} F(n,n+1)
$$

and defining a [[differential]] induced from the [[connecting homomorphisms]] of the defining [[homotopy fiber sequences]]

$$
  F(n-1,n) \to F(n-1, n+1) \to F(n,n+1)
$$

yields an ordinary [[chain complex]] $C_\bullet$ in the [[homotopy category of an (∞,1)-category|homotopy category]].

=--

([[Higher Algebra|Higher Algebra, remark 1.2.2.3]])

+-- {: .num_prop #ChainComplexesFromFilteredObjects}
###### Proposition

Consider the inclusion of [[posets]]

$$
  (\mathbb{Z}, \leq)
  \to 
  (\mathbb{Z}\cup \{\infty\}, \leq) \times (\mathbb{Z}\cup \{\infty\}, \leq)
$$

given by

$$
  n \mapsto (n,\infty)
  \,.

$$

The induced [[(∞,1)-functor]]

$$
  Func((\mathbb{Z}\cup \{\infty\}, \leq) \times (\mathbb{Z}\cup \{\infty\}, \leq), \mathcal{C})
  \longrightarrow
  Func((\mathbb{Z}, \leq), \mathcal{C})
$$

restricts to an [[equivalence of (∞,1)-categories|equivalence]] between the (∞,1)-category of $\mathbb{Z}\cup \{\infty\}$-chain complexes in $\mathcal{C}$ (def. \ref{ChainComplexInStableInfinityCategory}) and that of generalized filtered objects in $\mathcal{C}$ (def. \ref{GeneralizedFilteredObject}).


=--

This is [[Higher Algebra|Higher Algebra, lemma 1.2.2.4]]. The inverse functor can be described informally as follows: given a filtered object $X_\bullet$, the associated chain complex $X(\bullet,\bullet)$ is given by

$$ X(n, n+r) = \operatorname{fib}(X_n\to X_{n+r}). $$


### The spectral sequence


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

This exact couple gives rise in the usual way to a spectral sequence. Explicitly:


+-- {: .num_defn }
###### Definition

Let $X_\bullet$ be a filtered object in the sense of def. \ref{GeneralizedFilteredObject}. Write $X(\bullet,\bullet)$ for the corresponding chain complex, according to prop. \ref{ChainComplexesFromFilteredObjects}.

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

Define then for $p,q \in \mathbb{Z}$ and $r \geq 1$ the object $E^r_{p,q}$ by the canonical [epic-monic factorization](http://ncatlab.org/nlab/show/abelian+category#FactorizationOfMorphisms)

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

from the above long exact sequence (with $i=q-r$, $j=q$, and $k=q+r$).


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

([[Higher Algebra|Higher Algebra, prop. 1.2.2.7]])

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
\underset{\rightarrow}{\lim}_q \operatorname{ker}(\pi_p (X)\to \pi_p(X_q))
\simeq
\pi_p(X)
\simeq
\underset{\leftarrow}{\lim}_q \operatorname{im}(\pi_p (X)\to \pi_p(X_q)).
$$


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