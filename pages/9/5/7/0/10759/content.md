
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

## Definition


Let throughout $\mathcal{C}$ be a [[stable (∞,1)-category]], $\mathcal{A}$ an [[abelian category]], and $\pi:\mathcal{C}\to\mathcal{A}$ a homological functor on $\mathcal{C}$, i.e., a functor that transforms every [[cofiber sequence]]

$$ X\to Y\to Z\to \Sigma X $$

in $\mathcal{C}$ into a long exact sequence

$$ \dots \to \pi(X)\to \pi(Y)\to \pi(Z)\to \pi(\Sigma X) \to \dots $$

in $\mathcal{A}$. We write $\pi_n=\pi\circ \Sigma^{-n}$.

+-- {: .num_example}
###### Example


* $\mathcal{C}$ is arbitrary, $\mathcal{A}$ is the category of [[abelian groups]] and $\pi$ is $\pi_0 \mathcal{C}(S,-)$ for some object $S\in\mathcal{C}$

* $\mathcal{C}$ is equipped with a [[t-structure]], $\mathcal{A}$ is the [[heart of a stable (∞,1)-category|heart]] of the t-structure, and $\pi$ is the canonical functor.

* $\mathcal{C} = D(\mathcal{A})$ is the [[derived category]] of the abelian category $\mathcal{A}$ and $\pi=H_0$.

* Any of the above with $\mathcal{C}$ and $\mathcal{A}$ replaced by their opposite categories.

=--

+-- {: .num_defn #GeneralizedFilteredObject}
###### Definition

A _generalized [[filtered object]]_ in $\mathcal{C}$ is
simply a sequential diagram $X \colon (\mathbb{Z}, \lt) \to \mathcal{C}$

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


+-- {: .num_defn #ExactCoupleForFilteredObject}
###### Definition

For a generalized filtered object $X_\bullet$, def. \ref{GeneralizedFilteredObject}, write 

$$
  F_n \coloneqq fib(X_n \to X_{n+1})
$$

for the [[homotopy fiber]] of the $n$th structure map, for all $n \in \mathbb{Z}$, and define an [[exact couple]]

$$
  \array{
    && \pi_\bullet(F_\bullet)
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
  \pi_\bullet(F_n) \to  \pi_\bullet(X_n) \to \pi_\bullet(X_{n+1}) \to \pi_{\bullet+1}(F_n) \to \cdots
$$

=--

This exact couple gives rise to a bigraded [[spectral sequence]] $\{E_r^{*,*}\}_{r\geq 1}$ in the abelian category $\mathcal{A}$, functorial in the filtered object $X_\bullet$, with

$$ E_1^{p,q} = \pi_p(F_q), \qquad d_r: E_r^{p,q}\to E_r^{p-1,q-r}. $$

If sequential limits and colimits exist in $\mathcal{A}$, we can form the limiting term $E_\infty^{*,*}$ of this spectral sequence.

On the other hand, the graded object $\pi_\bullet (X)$ admits a filtration by

$$ F^q \pi_p (X) = \operatorname{ker}(\pi_p (X)\to \pi_p(X_q)) $$

and we would like to compare $E_\infty^{*,*}$ with the associated graded of this filtration. We say that the spectral sequence **converges weakly** if there is a canonical isomorphism

$$ E_\infty^{p,q} \cong F^q\pi_p(X)/ F^{q-1}\pi_p(X) $$

for every $p,q\in\mathbb{Z}$. The meaning of the word *canonical* is somewhat subtle since, in general, there is no map from one side to the other. However, there always exists a canonical *relation* between the two, and we ask that this relation be an isomorphism (see [Hilton-Stammbach, VIII.7](#HiltonStammbach)).

We say that the spectral sequence **converges strongly** if it converges weakly and if, in addition, the filtration $F^\bullet\pi_p(X)$ is complete on both sides.

+-- {: .num_prop #FiltrationSpectralSequence}
###### Proposition

Let $\mathcal{C}$ be a [[stable (∞,1)-category]] and let $\pi:\mathcal{C}\to\mathcal{A}$ be a homological functor where $\mathcal{A}$ is an [[abelian category]] which admits sequential limits. Let $X_\bullet$ be a filtered object in $\mathcal{C}$ such that $X=\underset{\leftarrow}{\lim}_n X_n$ exists. Suppose further that:

1. For every $n$, the diagram $r\mapsto \operatorname{fib}(X_{n-r}\to X_n)$ has a limit in $\mathcal{C}$ and that limit is preserved by $\pi$.
2. For every $n$, $\pi_n(X_r)=0$ for $r\gg 0$.

Then the [[spectral sequence]] $\{E_r^{*,*}\}_{r\geq 1}$ in $\mathcal{A}$ converges strongly to the [[homotopy groups]] of the [[homotopy limit]] $\underset{\leftarrow}{\lim}_n X_n$ of the generalized filted object:

$$
  E^{p,q}_1
  =
  \pi_{p} F_{q}
  \Rightarrow
  \pi_{p} (\underset{\leftarrow}{\lim} X_\bullet) 
$$

=--

There is also a dual statement in which limits are replaced by colimits, but it is in fact a special case of the proposition with $\pi$ replaced by $\pi^{op}$. A proof of this proposition (in dual form) is given in ([[Higher Algebra|Higher Algebra, prop. 1.2.2.14]]). Review is in [Wilson 13, theorem 1.2.1](#Wilson13).

For the traditional statement in the [[category of chain complexes]] see at _[[spectral sequence of a filtered complex]]_.

## Examples

* Let $\mathcal{C} = Spec^{op}$ be the opposite (∞,1)-category of spectra, let $\mathcal{A}$ be the opposite category of abelian groups, and let $\pi$ be the functor $[K,-]$ where $K$ is spectrum. Then condition (1) in Proposition [1](#FiltrationSpectralSequence) holds for all filtered objects if and only if $K$ is a [[finite spectrum]]. When the filtered object is the [[Whitehead tower]] of a spectrum $E$, the associated spectral sequence is the [[Atiyah-Hirzebruch spectral sequence]] with target $E^*(K)$. It is thus strongly convergent if $K$ is a finite spectrum.

* The $E$-based [[Adams spectral sequence]] that approximates homotopy classes of maps between two spectra $X$ and $Y$ using the generalized cohomology theory $E$ is a special case of the above spectral sequence, with $\mathcal{C}=Spec$, $\pi=[X,-]$, and the filtered object associated with the cosimplicial spectrum $E^{\wedge\bullet}\wedge Y$. Bousfield's theorems on the convergence of the Adams spectral sequence can be rephrased as giving sufficient conditions on $X$, $Y$, and $E$ for condition (1) in Proposition [1](#FiltrationSpectralSequence) to hold (see [Bousfield, Theorems 6.6 and 6.10](#Bousfield)).

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

* A.K. Bousfield, *The localization of spectra with respect to homology*, ([pdf](http://www.math.uwo.ca/~mfrankla/Bousfield_LocalnSpectraHomol.pdf))
{#Bousfield}

[[!redirects spectral sequence of a filtered object in a stable (∞,1)-category]]
[[!redirects spectral sequence of a filtered object in a stable (infinity,1)-category]]

[[!redirects filtered stable homotopy type]]
[[!redirects filtered stable homotopy types]]