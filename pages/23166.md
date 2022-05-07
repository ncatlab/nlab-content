## Idea

A __measurable field of Hilbert spaces__ is the exact analogue of a vector bundle over a topological spaces in the setting of bundles of infinite-dimensional Hilbert spaces over [[measurable spaces]].

## Definition

The original definition is due to [[John von Neumann]] (Definition 1 in \cite{Neumann}).

We present here a slightly modernized version, which can be found in many modern sources, e.g., Takesaki \cite{Takesaki}.

\begin{definition}
Suppose $(X,\Sigma)$ is a [[measurable space]]
equipped with a [[σ-finite measure]] $\mu$,
or, less specifically, with a [[σ-ideal]] $N$ of negligible subsets
so that $(X,\Sigma,N)$ is an [[enhanced measurable space]].
A __measurable field of Hilbert spaces__ over $(X,\Sigma,N)$
is a family $H_x$ of [[Hilbert spaces]] indexed by points $x\in X$
together with a [[vector subspace]] $M$
of the [[product]] $P$ of [[vector spaces]] $\prod_{x\in X} H_x$.
The elements of $M$ are known as __measurable sections__.
The pair $(\{H_x\}_{x\in X},M)$ must satisfy the following conditions.
* For any $m\in M$ the function $X\to\mathbf{R}$ ($x\mapsto \|m(x)\|$)
is a measurable function on $(X,\Sigma)$.
* If for some $p\in P$, the function $X\to\mathbf{C}$ ($x\mapsto\langle p(x),m(x)\rangle$) is a measurable function on $(X,\Sigma)$ for any $m\in M$,
then $p\in M$.
* There is a countable subset $M'\subset M$ such that for any $x\in X$, the closure of the span of vectors $m(x)$ ($m\in M'$) coincides with $H_x$.
\end{definition}

The last condition restrict us to bundles of separable Hilbert spaces.
One can also define bundles of nonseparable Hilbert spaces,
but this cannot be done simply by dropping the last condition.

## Serre–Swan-type duality

The category of measurable fields of Hilbert spaces on $(X,\Sigma,N)$ is equivalent
to the category of [[W*-modules]] over the [[commutative von Neumann algebra]]
$\mathrm{L}^\infty(X,\Sigma,N)$.

(If we work with bundles of separable Hilbert spaces,
then [[W*-modules]] must be countably generated.)

## Related entries

* [[duality between algebra and geometry]]

* [[Serre-Swan theorem]]

* [[W*-module]]

* [[commutative von Neumann algebra]]

## References

* {#Neumann} [[John von Neumann]], _On Rings of Operators. Reduction Theory_, The Annals of Mathematics 50:2 (1949), 401.  [doi](http://dx.doi.org/10.2307/1969463).

* {#Takesaki} [[Masamichi Takesaki]], _Theory of Operator Algebras.  I_, Springer, 1979.

[[!redirects measurable field]]
[[!redirects measurable fields]]
[[!redirects measurable fields of Hilbert spaces]]
