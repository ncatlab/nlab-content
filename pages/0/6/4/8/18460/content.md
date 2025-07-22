# Pushout complements

* table of contents
{: toc}

## Idea

A *pushout complement* is a "completion of a pair of [[arrows]] to a [[pushout]]".  Intuitively, it is a way to "remove part of an [[object]] of a [[category]]" while retaining information about how that part is "connected" to other parts.  Pushout complements play an important role in some kinds of [[span rewriting]].

## Definition

Given [[morphisms]] $m:C\to A$ and $g:A\to D$ in a [[category]], a **pushout complement** is a pair of arrows $f:C\to B$ and $n:B\to D$ such that the square
\begin{tikzcd}
	C & A \\
	B & D
	\arrow["m", from=1-1, to=1-2]
	\arrow["f"', dashed, from=1-1, to=2-1]
	\arrow["g", from=1-2, to=2-2]
	\arrow["n"', dashed, from=2-1, to=2-2]
\end{tikzcd}
[[commutative square|commutes]] and is a [[pushout]].

In general, even in good categories, pushout complements may not exist.  However, if they do exist, then as long as the category is [[adhesive category|adhesive]] (such as a [[topos]]) and $m$ is a [[monomorphism]], they are unique up to unique isomorphism.  In the language of [[homotopy type theory]], the [[type]] of such pushout complements is an [[h-proposition]].

## Examples

* In the category [[Set]], if $m$ and $g$ are [[injections]] then a pushout complement always exists: take $B = D \setminus (A\setminus C)$.

* In a [[coherent category]], if $C=\emptyset$ and $g$ is a [[monomorphism]], then a pushout complement is the same as an ordinary [[complement]] for the [[subobject]] $A\to D$.

* In a category of [[graphs]], pushout complements play an important role in [[double pushout graph rewriting]].

* The dual of a pushout complement is a *pullback complement*.  Important pullback complements include [[final pullback complements]], which arise from [[exponential objects]] of [[monomorphisms]].

## References

* H. Ehrig, M. Pfender and H. J. Schneider. _Graph-grammars: An algebraic approach_, 14th Annual Symposium on Switching and Automata Theory, 1973, pp. 167-180. ([doi:10.1109/SWAT.1973.11](https://doi.org/10.1109/SWAT.1973.11))

* {#LS} [[Steve Lack]] and [[Pawel Sobocinski]], _Adhesive categories_, Foundations of Software Science and Computation Structures. FoSSaCS 2004. Lecture Notes in Computer Science, vol 2987. Springer, Berlin, Heidelberg. doi:[10.1007/978-3-540-24727-2_20](https://doi.org/10.1007/978-3-540-24727-2_20), [PDF](https://www.ioc.ee/~pawel/papers/adhesive.pdf)

[[!redirects pushout complements]]
[[!redirects pullback complement]]
[[!redirects pullback complements]]
