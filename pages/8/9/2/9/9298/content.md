In the theory of [[nLab:cartesian fibration]]s of simplicial sets cartesian fibrations $X\to \Delta^n$ over a simplex play an important role since an arbitrary  morphism $X\to S$ is a cartesian fibration iff for all $n$, $X\times_S \Delta^n\to \Delta^n$ is a cartesian fibration.

A cartesian fibration $X\to \Delta^n$ is by the $(\infty,1)$-Grothendieck construction equivalently a functor $\Delta^n\to (\infty,1)Cat$; i.e. a composable sequence of $(\infty,1)$-categories and functors $\phi:A^0\leftarrow\dots\leftarrow A^n$.

+-- {: .un_defn}
###### Definition
The *mapping simplex* $M(\phi)$ of $\phi$ is defined by:

* For a nonempty finite linear order $L$ with greatest element $j$, a map $\Delta^L\to M(\phi)$ consists of an order preserving map $f:L\to [n]$ and a morphism $\sigma:\Delta^L\to A^{f(j)}$.

* Given two such linear orders $L$ and $L^\prime$ with greatest elements $j$ resp. $j^\prime$ there is a natural map $M(\phi)(\Delta^{L^\prime})\to M(\phi)(\Delta^{L})$ sending $(f,\sigma)$  to $(f\circ p, e\circ \sigma)$, where $e:A^{f(j^\prime)}\to A^{f(p(j))}$ is obtained by $\phi$.

There is a natural map $h:M(\phi)\to \Delta^n$ (take $J=m$, then the Yoneda lemma gives a map $\Delta^m\to \Delta^n$).

An edge $e$ of $M(\phi)$ is defined by a pair of integers $0\le i\le j\le n$ and an edge $e^\prime\in A^j$. $M(\phi)$ becomes a [[nLab:marked simplicial set]] $(M(\phi), E)$ by marking those edges for which $e^\prime$ is degenerated.
=--

+-- {: .un_defn}
###### Definition
Let $p:X\to \Delta^n$ be a cartesian fibration, let $\phi:A^0\leftarrow\dots\leftarrow A^n$ be  a composable sequence of $(\infty,1)$-categories and functors. Then A map $q:M(\phi)\to X$ is called a *quasi-equivalence* if it satisfies:

(1) The map $h$ commutes with $p$ and $q$.

(2) $q$ sends marked edges of $M(\phi)$ to $p$-cartesian ones.

(3) For every $0\le i\le n$, the induced map $A^i\to p^{-1}\{ i \}$ is a [[nLab:categorical equivalence]].
=--

+-- {: .un_prop}
######  Proposition
Let $p:X\to \Delta^n$ be a cartesian fibration.

(1) There exists  a composable sequence of $(\infty,1)$-categories and functors $\phi:A^0\leftarrow\dots\leftarrow A^n$ and a quasi-equivalence $q:M(\phi)\to X$.

(2) If $\phi:A^0\leftarrow\dots\leftarrow A^n$ is a composable sequence and $q:M(\phi)\to X$ a quasi-equivalence. Then for any map $T\to \Delta^n$, the induced map

$$M(\phi)\times_{\Delta^n}T\to X\times_{\Delta^n}T$$

is a [[nLab:categorical equivalence]].
=--

## Related topics

* [[nLab:relative nerve]]

* [[nLab:(infinity,1)-Grothendieck construction]]

## Reference

* [[nLab:Higher Topos Theory]] section 3.2.2.