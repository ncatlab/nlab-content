

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The *Taylor series* of a [[smooth function]] $f$ (at a given point $c$) is a [[formal power series]] (in $x - c$) whose [[partial sum|partial sums]] are the [[Taylor polynomials]] of $f$ (at $c$).  As the Taylor polynomials are approximations of $f$ by [[polynomials]] (up to a given degree), so the Taylor series is an approximation of $f$ by an [[analytic function]] (or at least an [[asymptotic expansion]] that attempts to be this).

See also [[Taylor's theorem]] for error estimates in the convergence of Taylor series.


## Definition

Let $f \in C^\infty(\mathbb{R})$ a [[smooth function]] with $n$th [[derivative]] $f^{(n)} \in C^\infty(\mathbb{R})$ and let $c$ be a [[real number]]. 

+-- {: .num_defn}
###### Definition

The **Taylor series** of $f$ at $c$ is the [[formal power series]]

$$
  \sum_{n = 0}^\infty \frac{1}{n!} f^{(n)}(c) (x-c)^n
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

For $f \in C^\infty(\mathbb{R})$ a [[smooth function]] with $n$th [[derivative]] $f^{(n)} \in C^\infty(\mathbb{R})$, its **Maclaurin series** is its Taylor series at [[zero]]:

$$
  \sum_{n = 0}^\infty \frac{1}{n!} f^{(n)}(0) x^n
  \,.
$$
=--

+-- {: .num_remark}
###### Remark

Similar definitions apply to functions on any [[Cartesian space]] or [[smooth manifold]].
=--


## Properties

Recall that a ([[partial function|partial]]) function $f$ is [[analytic function|analytic]] at $c$ (in the [[interior]] of $\dom f$) if there exists a [[power series]] $P$ at $c$ and a [[neighbourhood]] $U$ of $c$ such that, for all $x \in U \cap \dom f$, $P(x)$ converges to $f(x)$.

+-- {: .num_prop}
###### Proposition

If $f$ is analytic at $c$, then the only power series witnessing this is the Taylor series of $f$ at $c$ (so in particular, the Taylor series exists; analytic functions are [[smooth function|smooth]]).
=--

In contrast, a smooth function need not be analytic; the classic counterexample is a [[bump function]].  In fact, the Taylor series of $f$ at $c$ might not converge to $f$ anywhere except at $c$, either because the Taylor series has vanishing [[radius of convergence]] or because it converges to something else (an analytic function with the same [[jet]] as $f$ but a different [[germ]]).  However, we can say this:

+-- {: .num_prop}
###### Proposition
**(Taylor series is [[asymptotic series]])**

The Taylor series of a [[smooth function]] $f$ is always an [[asymptotic expansion]] of $f$.

=--

This follows from the [[Hadamard lemma]], see [this example](asymptotic series#TaylorSeriesOfSmoothFunctionIsAsymptoticSeries) for details.

+-- {: .num_theorem}
###### Theorem
**(Borel's theorem)**

The map

$$
  C^\infty(\mathbb{R}^{k+l})
  \to
  C^\infty(\mathbb{R}^k) [ [ X_1, \cdots X_l] ]
$$

obtained by forming Taylor series in $l$ variables is [[surjection|surjective]].
=--

In particular, every [[power series]] in one real variable is the Taylor series of some [[smooth function]] on the [[real line]] (even if it has vanishing radius of convergence and so is not the Taylor series of any analytic function).

+-- {: .proof}
###### Proof

The proof is reproduced for instance in [[Models for Smooth Infinitesimal Analysis|MSIA, I, 1.3]]
=--

See more at [[Borel's theorem]].

## Examples

* of the [[natural logarithm]]: see *[[Mercator series]]*


## Related concepts

* [[series]], [[asymptotic series]]

* [[analytic geometry]]

[[!include infinitesimal and local - table]]

* analogue in ([[stable homotopy theory|stable]]) [[homotopy theory]]/[[Goodwillie calculus]]: _[[Taylor tower]]_


[[!redirects Taylor series]]
[[!redirects Taylor series expansion]]
[[!redirects Mac Laurin series]]
[[!redirects MacLaurin series]]
[[!redirects Maclaurin series]]

[[!redirects Taylor expansion]]
[[!redirects Taylor expansions]]
