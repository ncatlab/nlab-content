
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _curvature characteristic form_ is a [[differential form]] naturally associated to a [[Lie algebra]]-valued 1-form that is a measure for the non-triviality of the [[curvature]] of the 1-form.

More generally, there is a notion of curvature characteristic forms of [[L-∞-algebra]]-valued differential forms and [[schreiber:∞-Lie algebroid valued differential forms]].

## Of connection 1-forms

For $\mathfrak{g}$ a [[Lie algebra]], $\langle -,-, \cdots, -\rangle$ an [[invariant polynomial]] of $n$ arguments on the Lie algebra and $A \in \Omega^1(P,\mathfrak{g})$ a Lie-algebra-valued 1-form with [[curvature]] 2-form $F_A = d_{dR} A + [A \wedge A]$, the **curvature characteristic form** of $A$ with respect to $\langle \cdots \rangle$ is the [[differential form]] 

$$
  \langle F_A \wedge \cdots \wedge F_A \rangle \in \Omega^{2 n}(P)
  \,.
$$

This form is always an [[exact form]].  The $(2 n -1)$-form trivializing it is called a [[Chern-Simons form]].

Notably if $G$ is a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$, $P$ is the total space of a $G$-[[principal bundle]] $\pi : P \to X$, and $A \in \Omega^1(P,\mathfrak{g})$ is an [[Ehresmann connection]] 1-form on $P$ then by the very definition of the $G$-equivariance of $A$ and the _invariance_ of $\langle \cdots \rangle$ it follows that the curvature form is invariant under the $G$-action on $P$ and is therefore the pullback along $\pi$ of a $2 n$-form $P_n \in \Omega^{2 n}(X)$ down on $X$. This form is in general no longer exaxt, but is always a [[closed form]] and hence represent a class in the [[de Rham cohomology]] of $X$. This establishes the [[Weil homomorphism]] from invariant polynomials to de Rham cohomology


## In terms of $\infty$-Lie algebroids

The above description of curvature characteristic forms may be formulated in terms of [[∞-Lie theory]] as follows.

For $P \to X$ a $G$-[[principal bundle]] write $T X$, $T P$ and $T_{vert} P$ for the [[tangent Lie algebroid]] of $X$, of $P$ and the [[vertical tangen Lie algebroid]] of $P$, respectively. Write $inn(\mathfrak{g})$ for the [[Lie 2-algebra]] given by the [[differential crossed module]] $\mathfrak{g}\stackrel{Id}{\to} \mathfrak{g}$ and finally $\prod_i b^{n_i} \mathbb{R}$ for the [[L-∞-algebra]] with one abelian generator for each generating [[invariant polynomial]] of $\mathfrak{g}$

From the discussion at [[invariant polynomial]] we have a canonical morphism $inn(\mathfrak{g}) \to \prod_i b^{n_i}\mathbb{R}$ that represents the generating invariant polynomials.

Recall that a morphism of [[∞-Lie algebroid]]s

$$
  T X \to b^n \mathbb{R}
$$

is equivalently a closed $n$-form on $X$. The data of an [[Ehresmann connection]] on $P$ then induces the following diagram of [[∞-Lie algebroid]]s

$$
  \array{
    T_{vert} P &\stackrel{A_{vert}}{\to}& \mathfrak{g}
    &&&
    flat vertical form
    \\
    \downarrow && \downarrow 
    &&&
    first Ehresmann condition
    \\
    T P &\stackrel{A}{\to}& inn(\mathfrak{g})
    &&&
    form on total space
    \\
    \downarrow && \downarrow
    &&&
    second Ehresmann condition
    \\
    T X &\stackrel{(P_n)}{\to}& \prod_i b^{n_i} \mathbb{R}
    &&&
    curvature characteristic forms
  }
  \,.
$$

## Examples

* The single curvature characteristic form of a complex [[line bundle]]/$U(1)$-[[principal bundle]] is the curvature 2-form itself.

* A sum of all curvature characteristic forms of a complex [[vector bundle]]/[[unitary group|U(n)]]-[[principal bundle]] gives the <a href="http://ncatlab.org/nlab/show/Chern+character#KTheory">Chern character of a vector bundle</a>.


## References

...

[[!redirects curvature characteristic forms]]

[[!redirects curvature characteristic class]]
[[!redirects curvature characteristic classes]]