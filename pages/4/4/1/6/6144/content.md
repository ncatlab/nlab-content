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

From now, the symbols `$\subset$' and `$\supset$' are
used to denote nonstrict inclusions of sets,
which are sometimes also denoted by `$\subseteq$' and `$\supseteq$'.

Recall the following properties of a [[Borel measure]] $\mu$ on a [[Hausdorff topological space]]:

* $\mu$ is __outer regular__ if for every [[Borel subset]] $B$ we have
$$\mu(B)=\inf\{\mu(V)\mid V\supset B\; and\; V\; is\; open\}.$$

* $\mu$ is __locally finite__ if every point has a neighborhood with a finite $\mu$-measure.

* $\mu$ is __inner regular__ on some [[Borel subset]] $B$ if
$$\mu(B)=\sup\{\mu(K)\mid K\subset B\; and\; K\; is\; compact\}.$$

Also, if $m$ and $M$ are [[Borel measures]],
then $m$ is the __essential measure__ associated with $M$ if
$$m(A)=\sup\{m^*(C)\mid C\subset A,\; m^*(C)\; is\; finite\},$$
where
$$m^*(C)=\inf\{m(B)\mid B\supset C\; and\; B\; is\; Borel\}.$$
Equivalently, one can simply say that
$$
m(B)=\sup\{M(B')\mid B'\subset B,\; M(B')\; is\; finite,\; B'\; is\; Borel\}.
$$

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
$$M(B)=\inf\{m(V)\mid V\supset B\; and\; V\; is\; open\}.$$

In order to pass from $M$ to $m$, set
$$m(B)=\sup\{M(B')\mid B'\subset B,\; M(B')\; is\; finite,\; B'\; is\; Borel\}.$$

If $m(X)$ or $M(X)$ is finite, then $m=M$.

If $B$ is a [[Borel subset]] such that $M(B)$ is finite or $B$ is open,
then $m(B)=M(B)$.

A Radon measure is __σ-finite__ if $m$ is σ-finite.

A Radon measure is __moderated__ if $M$ is σ-finite.

## Real and complex Radon measures

\begin{definition}
A real (respectively complex) Radon measure on a [[Hausdorff topological space]] $X$
is a real (respectively complex) valued function $\mu$
defined on relatively compact [[Borel subsets]] of $X$
that is (1) countably additive,
(2) every relative compact [[Borel subset]] $B\subset X$
can be presented as the union of countably many compact subsets
and a subset $N\subset B$ such that $\mu(N')=0$ for any [[Borel subset]] $N'\subset N$,
and (3) any point has a neighborhood $V$ such that $\sup |\mu(B)|$
is finite, where $B\subset V$ is a relatively compact subset of $X$.
\end{definition}

If $\mu\ge0$, then $\mu$ can be extended to a Radon measure $(m,M)$
in the previous sense.

## On locally compact Hausdorff topological spaces

Radon measures on locally compact Hausdorff topological spaces
admit yet another, Daniell-style definition, which is explored
in detail in Bourbaki's book.

\begin{definition}
Suppose $X$ is a locally compact Hausdorff topological space.
A __Radon measure__ on $X$ is a positive linear functional
$$\mu\colon C_c(X,\mathbf{R})\to\mathbf{R},$$
where $C_c$ refers to the vector space of continuous compactly
supported functions.
\end{definition}

Such $\mu$ induces a pair $(m,M)$ in the sense of above definitions
as follows: $M=\mu^*$ and $m=\mu^{\bar*}$,
where $\mu^*$ is the outer measure associated to $\mu$, i.e.,
$$\mu^*(A)=\inf\{\mu(\chi_B)\mid B\supset A,\; B\; is\; Borel\}$$
and $\mu^{\bar*}$ is the essential measure associated to $\mu^*$:
$$\mu^{\bar*}(A)=\sup\{\mu^*(C)\mid C\subset A,\; \mu^*(C)\; is\; finite\}.$$

(For σ-finite spaces we have $\mu^*=\mu^{\bar*}$.)

Vice versa, given $M$, we can reconstruct $\mu$ as the integral
with respect to $M$.

## Pushforwards of Radon measures

\begin{definition}
Suppose $X$ and $Y$ are [[Hausdorff topological spaces]]
and $\mu=(m,M)$ is a Radon measure on $X$.
A map of sets $H\colon X\to Y$ is __Lusin $\mu$-measurable__
if for any compact $K\subset X$ and $\epsilon\gt0$
there is a compact $K'\subset K$ such that $\mu(K\setminus K')\lt\epsilon$
and the restriction of $H$ to $K'$ is continuous.
We say that $H$ is __$\mu$-proper__ if, in addition,
every point of $Y$ has a neighborhood whose inverse image
is $\mu$-integrable.
\end{definition}

For example, continuous maps are Lusin $\mu$-measurable for any $\mu$.

Lusin $\mu$-measurable maps form a [[sheaf]] with respect to $X$.

Any Lusin $\mu$-measurable map is Borel $\mu$-measurable
(meaning preimages of Borel sets are $\mu$-measurable sets).

If $Y$ is [[metrizable]] and [[separable]], then any Borel $\mu$-measurable
map is Lusin $\mu$-measurable.

Step functions and lower semicontinuous maps are always Lusin $\mu$-measurable.

\begin{definition}
Suppose $H\colon X\to Y$ is a $\mu$-proper map.
The pushforward measure $H_*\mu$ is a Radon measure on $Y$ defined as follows.
Given a [[Borel subset]] $B\subset Y$, we set
$$H_*\mu(B)=\mu^\bullet(H^*(B)).$$
This yields a Radon measure $m$ on $Y$.
\end{definition}

\begin{theorem}
If $H\colon X\to Y$ is a [[continuous map]] of [[Hausdorff topological spaces]],
then a Radon measure $\nu$ on $Y$ is the pushforward along $H$
of a Radon measure on $X$ if and only if $\nu$
is concentrated in a countable union of images under $H$
of compact subsets of $X$.
\end{theorem}

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

* V. Bogachev, _Measure Theory_, vol. 2 (2007). doi:[10.1007/978-3-540-34514-5](https://doi.org/10.1007/978-3-540-34514-5)

* Gerald B. Folland, A course in abstract harmonic analysis, Studies in Adv. Math. CRC Press 1995


[[!redirects Radon measure]]
[[!redirects Radon measures]]
