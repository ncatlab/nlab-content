+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

Recall the following properties of a [[Borel measure]] $\mu$ on a [[Hausdorff topological space]]:

* $\mu$ is __outer regular__ if for every [[Borel subset]] $B$ we have
$$\mu(B)=\inf\{\mu(V)\mid V\supset B and V is open\}.$$

* $\mu$ is __locally finite__ if every point has a neighborhood with a finite $\mu$-measure.

* $\mu$ is __inner regular__ on some [[Borel subset]] $B$ if
$$\mu(B)=\sup\{\mu(K)\mid K\subset B and K is compact\}.$$

Also, if $m$ and $M$ are [[Borel measures]],
then $m$ is the __essential measure__ associated with $M$ if
$$m(A)=\sup\{m^*(C)\mid C\subset A, m^*(C) is finite\},$$
where
$$m^*(C)=\inf\{m(B)\mid B\supset C and B is Borel\}.$$
Equivalently, one can simply say that
$$m(B)=\sup\{M(B')\mid B'\subset B, M(B') is finite, B' is Borel\}.$$

We give three equivalent definitions of Radon measures.

\begin{definition}
If $X$ is a [[Hausdorff topological space]], then a __Radon measure__ on $X$
is a [[Borel measure]] $m$ on $X$ such that $m$ is locally finite and inner regular on all [[Borel subsets]].
\end{definition}

\begin{definition}
If $X$ is a [[Hausdorff topological space]], then a __Radon measure__ on $X$
is a [[Borel measure]] $M$ on $X$ such that $M$ is locally finite, outer regular, and inner regular on all open subsets.
\end{definition}

\begin{definition}
If $X$ is a [[Hausdorff topological space]], then a __Radon measure__ on $X$
is a pair of [[Borel measures]] $m$ and $M$ on $X$ such that $m$ is the
essential measure associated with $M$,
$M$ is outer regular (on all Borel subsets),
$M$ is locally finite,
$M$ is inner regular on all Borel subsets,
and $m(B)=M(B)$ whenever $B$ is open or $M(B)$ is finite.
\end{definition}

## Equivalence of definitions

In order to pass from $m$ to $M$, set
$$M(B)=\inf\{m(V)\mid V\supset B and V is open\}.$$

In order to pass from $M$ to $m$, set
$$m(B)=\sup\{M(B')\mid B'\subset B, M(B') is finite, B' is Borel\}.$$

If $m(X)$ or $M(X)$ is finite, then $m=M$.

A Radon measure is __σ-finite__ if $m$ is σ-finite.

A Radon measure is __moderated__ if $M$ is σ-finite.

## Properties

* If a Radon measure is $\sigma$-finite then it is regular (i.e. both inner and outer regular) on all Borel subsets. 

* A Radon measure on a [[Hausdorff space]] is [[τ-additive]]. The converse is true on a [[compact Hausdorff space]].

* Radon [[probability measures]] on [[compact Hausdorff spaces]] form a [[monad]]: the [[Radon monad]]. Just as well, Radon probability measures of finite first moment on [[complete metric spaces]] give the [[Kantorovich monad]]. 

(See also [[monads of probability, measures and valuations]].)

## Examples

Most measures of interest in [[geometry]] are Radon. For example

* The [[Dirac measures]].

* The [[Lebesgue measure]] on the real line.

* The measure associated to a [[volume form]] on a Riemannian manifold.

* The left (right) [[Haar measure]] on a [[locally compact topological group]] is a nonzero Radon measure which is invariant under left (right) multiplications by elements in the group. 


## See also

* [[Radon monad]], [[Kantorovich monad]], [[monads of probability, measures, and valuations]]

* [[Borel measure]], [[τ-additive measure]], [[continuous valuation]]


## References

The canonical references on Radon measures are

* [[Laurent Schwartz]], _Radon measures on arbitrary topological spaces and cylindrical measures_.

* [[Nicolas Bourbaki]], _Integration.  Chapter IX_.

More recent expositions include

* V. Bogachev, _Measure Theory_, vol. 2 (2007).

* Gerald B. Folland, A course in abstract harmonic analysis, Studies in Adv. Math. CRC Press 1995


[[!redirects Radon measure]]
[[!redirects Radon measures]]
