
## Idea

Let $C$ be some [[category]] of [[modules]] or [[bimodules]] (say over a [[ring]], algebra, or operator algebra). Then an [[subobject]] $M\subset N$ is an __essential submodule__ of $N$ (or, we say that $N$ is an __essential extension__ of $M$) if $M$ has nonzero intersection ([[pullback]] in more abstract situations) with any nonzero subobject of $N$ (or equivalently, $M$ has zero intersection with only the [[zero object|zero subobject]] of $N$). In $C^\ast$-algebraic setup the ideals in the definition are required to be closed and 2-sided. 

In particular, one applies this terminology to [[ideals]], i.e. submodules (or subbimodules in the $2$-sided case) of a ring, algebra, or operator algebra itself. Hence we talk about __essential ideals__. For essential extensions, one considers [[extensions]] of algebras, where 'essential' still refers to non-intersection with submodules rather than with [[subalgebras]].

A monomorphism of modules $i:M\to N$ is an essential embedding if $N$ is an essential extension of $i(M)$. This alternative terminology is useful to motivate the notion of essential embeddability in $N$ as a property of $M$.

If $R$ is a ring a (say, left) $R$-module $M\neq 0$ is [[uniform module|uniform]] if every nonzero submodule of $M$ is essential. In other words, the intersection of any two nonzero submodules of $M$ is nonzero. 

## Literature

* wikipedia [essential extension](https://en.wikipedia.org/wiki/Essential_extension)
* [[K. R. Goodearl]], R. B. Warfield, _An introduction to noncommutative Noetherian rings_, London Math. Society Student Texts __16__ (1st ed,), 1989, xviii+303 pp.; or __61__ (2nd ed.), 2004, xxiv+344 pp. 

In
 
* [[Jiří Adámek]], [[Horst Herrlich]], [[Jiří Rosický]], [[Walter Tholen]], _Injective hulls are not natural_, Algebra univers. 48 (2002) 379--388 [doi](https://doi.org/10.1007/s000120200006)

the following generalization is considered. A morphism h in a class $H$ of morphisms in a category $C$ is $H$-essential if for every morphism $g$, the composite
$g\circ h$ lies in $H$ only if $g$ does. If $H$ is the class of monomorphisms we get the standard notion of an essential extension.


category: algebra, operator algebras

[[!redirects essential submodule]]
[[!redirects essential submodules]]
[[!redirects essential ideal]]
[[!redirects essential ideals]]
[[!redirects essential extension]]
[[!redirects essential extensions]]
[[!redirects essential embedding]]
[[!redirects essential embeddings]]
