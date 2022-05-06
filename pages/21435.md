\tableofcontents

## Idea: the Banach–Ulam problem

The __Banach–Ulam problem__ asks: are there any nontrivial
[[measures]] on a [[set]] $X$ equipped with the [[σ-algebra]] $2^X$ of all [[subsets]] of $X$?

All [[measures]] are by definition countably additive.

Here a measure on $(X,2^X)$ is __trivial__ if it can be obtained by the following construction.
Start with a set $X$, a map $f\colon X\to\mathbf{R}$, and a [[σ-ideal]] $I$ on $X$.
Set $\mu(A)=\sum_{x\in A}f(x)$ if $A\in I$ and $\mu(A)=\infty$ otherwise.
Then $\mu$ is a [[measure]] on $(X,2^X)$.

Once trivial measure on $(X,2^X)$ are excluded, we can further
reduce to the case of [[probability measures]] on $(X,2^X)$
that vanish on all singleton subsets of $X$.

Recall that the additivity of a [[poset]] $P$
is the smallest cardinal $\kappa$ such that
$P$ has a subset of cardinality $\kappa$ without an upper bound.

Recall that the additivity of a [[measure]] $\mu$
is the smallest cardinal $\kappa$ such that
there is a disjoint family of cardinality $\kappa$ of measurable subsets
such that the additivity property of $\mu$ fails for this family.

Recall that any [[measure]] $\mu$ on $(X,\Sigma)$ induces a [[σ-ideal]] $N_\mu$
such that $A\in N_\mu$ if $A\subset X$ and there is $B\in\Sigma$
such that $A\subset B$ and $\mu(B)=0$.

## Definitions

A [[cardinal]] $\kappa$ is __real-valued-measurable__
if there is a $\kappa$-additive [[probability measure]]
$\mu\colon 2^\kappa\to\mathbf{R}$ that vanishes on all singleton subsets of $\kappa$.

If the [[probability measure]] only takes values 0 and 1,
then $\kappa$ is known as a [[measurable cardinal]].

A cardinal $\kappa$ is __atomlessly-measurable__
if there is an atomless $\kappa$-additive [[probability measure]]
$\mu\colon 2^\kappa\to\mathbf{R}$.

Here an __atom__ of a [[measure]] $\mu$ on $(X,\Sigma)$
is $A\in\Sigma$ such that $\mu(A)\ne0$ and if $B\in\Sigma$
satisfies $B\subset A$, then either $\mu(B)=0$ or $\mu(A\setminus B)=0$.

## Ulam's theorem

\begin{theorem}
([[Ulam]].)
Suppse $(X,2^X,\mu)$ is a nontrivial [[probability space]].

* The additivity of $\mu$ equals the additivity of the [[σ-ideal]] $N_\mu$
and is a real-valued measurable cardinal.

* Any real-valued-measurable cardinal is either atomlessly measurable or measurable.

* Any atomlessly measurable cardinal is [[weakly inaccessible]] and not greater than $\mathfrak{c}$.

* Any [[measurable cardinal]] is [[strongly inaccessible]].

* The [[Lebesgue measure]] on $\mathbf{R}$ extends to $2^{\mathbf{R}}$ if and only if there is an atomlessly measurable cardinal.

\end{theorem}

## References

* [[David H. Fremlin]], _Real-valued-measurable cardinals_.
[PDF](https://www1.essex.ac.uk/maths/people/fremlin/rvmc.pdf).