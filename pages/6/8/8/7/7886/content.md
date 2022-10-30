## Idea

The condition that an $(\infty,1)$-category is an [[n-category]] is (in general) not invariant under [[Joyal model structure|categorical equivalence]]. Hence there is no intrinsic characterization of the class of $(n,1)$-categories.

However there is such a description of the class of $(\infty,1)$-categories which are *equivalent* to $(n,1)$-categories. To make this more concrete the notion of a *minimal fibration* which is a [[inner fibration]] of simplicial sets satisfying a relative homotopy condition and that of a *minimal $(\infty,1)$-category* are introduced.

Every $(\infty,1)$-category is equivalent to a minimal $(\infty,1)$-category.

## Definition

+-- {: .num_defn #homotopic relative}
###### Definition
Let
$$\array{
A&\stackrel{u}{\to}&X
\\
\downarrow^i&&\downarrow^p
\\
B&\stackrel{v}{\to}&S}$$

denote a lifting problem. Then putative solutions $f,g$ of this lifting problem are called *homotopic relative $A$ over $S$* if they are equivalent as objects in the fiber of the map

$$X^B\to X^A\times_{S^A}S^B$$

Equivalently $f,g$ are homotopic relative $A$ over $B$ if there is a map

$$F:B\times \Delta[1]\to X$$

such that

$F|B\times\{0\}=f$

$F|B\times\{1\}=g$

$p\circ F=v\circ \pi_B$

$F\circ(i\times id_{\Delta[1]})=u\circ\pi_A$

$F|\{b\}\times \Delta[1]$

and $F|\{b\}\times\Delta[1]$ is an equivalence in the $(\infty,1)$-category $X_{v(b)}$ for every vertex $b$ of $B$.

=--
+-- {: .un_defn}
###### Definition 2.3.3.1

Let $p : X \to S$ be an inner fibration of simplicial sets. $p$ is called *minimal inner fibration*  if $f = f^\prime$ for every pair of maps $f , f ^\prime : \Delta[n] \to X$ which are homotopic relative to $\partial \Delta[n]$ over $S$ . 

An $(\infty,1)$-category $C$ is called *minimal $(\infty,1)$-category* if $C\to *$ is minimal.
=--

+-- {: .un_prop #prop2.3.4.18}
###### Proposition 2.3.4.18
Let $C$ be an $(\infty,1)$-category and let $n\ge -1$. The the following statements are equivalent:

1. There exists a minimal model $C^\prime\subseteq C$ such that $C^\prime$ is an $(n,1)$-category.

1. There exists a categorical equivalence $D\to C$, where $D$ is an $(n,1)$-category.

1. For every pair of objects $X,Y\in C$, the mapping space $Map_C(X,Y)\in H$ is $(n-1)$-truncated.
=--

+-- {: .un_cor #cor2.3.4.19}
###### Corollary 2.3.4.19
Let $X$ be a [[nLab:Kan complex]]. Then is is equivalent to an $(n,1)$-category iff it is $n$[[truncation|-truncated]].
=--


## Related concepts

[[minimal Kan fibration]]

## References

Jacob Lurie, [[higher topos theory]], section 2.3.3 and section 2.3.4
