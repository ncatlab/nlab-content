
# Contents
* table of contents
{: toc}

## Idea

A [[map]] $f$ between [[spaces]] (say, a [[continuous map]] between [[topological spaces]]) _vanishes at infinity_ if $f(x)$ gets arbitrarily close to $0$ as $x$ gets sufficiently close to infinity.

For a map $f\colon X \to Y$, we need a notion of being close to $0$ in $Y$, so take $Y$ to be a [[pointed space]]; then getting arbitrarily close to $0$ means entering any [[neighbourhood]] of the basepoint.  We also need a notion of being close to infinity in $X$, so take $X$ to be a [[locally compact Hausdorff space]]; then getting sufficiently close to infinity means entering the [[exterior]] of some [[compact subspace]].  (To interpret 'getting', of course, we may use [[nets]].)  It is likely, however, that further generalisations are possible.


## Definitions

Let $X$ and $Y$ be [[topological spaces]], and let $f$ be a [[continuous map]] (or potentially any [[function]]) from $X$ to $Y$.  Let $Y$ be [[pointed space|pointed]], and let $X$ be [[locally compact Hausdorff space|locally compact Hausdorff]].

+-- {: .num_defn}
###### Definition
The map $f\colon X \to Y$ __vanishes at infinity__ if:
* for every [[neighbourhood]] $N$ of the [[basepoint]] in $Y$,
* there is [[compact subspace]] $K$ of $X$ such that:
  * for every $x$ in the [[exterior]] of $K$ in $X$,
  * $f(x)$ belongs to $N$.
=--

In case $Y$ is a pointed [[metric space]] (such as a [[Banach space]], with basepoint $0$; or in particular the [[real line]], with basepoint $0$), then we may equivalently say:
* for every [[positive number]] $\epsilon$,
* there is [[compact subspace]] $K$ of $X$ such that:
  * for every $x$ in the [[exterior]] of $K$ in $X$,
  * ${\|f(x)\|} \lt \epsilon$.

(Here, ${\|{-}\|}$ is the [[norm]] in a Banach space, or more generally the distance from the basepoint in any pointed metric space.)


## Properties 

One way of considering this definition is that one can adjoin to $X$ a point "at infinity", denoted $\infty$, by declaring that the open neighborhoods of $\infty$ are sets of the form $\{\infty\} \cup Ext(K)$ for $K \subset X$ compact. This is called the [[one-point compactification]], denoted $X^+$. Then a map $f\colon X \to A$ vanishes at infinity iff there exists an extension of $f$ to a map $X^+ \to A$, continuous at $\infty$ (at least) that sends $\infty$ to $0$ (thus literally "vanishing at $\infty$").

More generally, for $X$ any [[Tychonoff space]], functions that vanish at infinity are precisely those that can be extended (continuously by $0$) to the [[Stone–Čech compactification]] of $X$.


## References

* Wikipedia, _[Locally compact space](http://en.wikipedia.org/wiki/Locally_compact_space)_


[[!redirects vanishing at infinity]]
[[!redirects vanish at infinity]]
