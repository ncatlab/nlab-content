
## Idea

Let $C$ be some [[category]] of [[modules]] or [[bimodules]] (say over a [[ring]], algebra, or operator algebra). Then an [[subobject]] $M\subset N$ is an __essential submodule__ (some say large submodule) of $N$ (or, we say that $N$ is an __essential extension__ of $M$; some authors argue that this should be called inessential extension) if $M$ has nonzero intersection ([[pullback]] in more abstract situations) with any nonzero subobject of $N$ (or equivalently, $M$ has zero intersection with only the [[zero object|zero subobject]] of $N$). In $C^\ast$-algebraic setup the ideals in the definition are required to be closed and 2-sided. 

In particular, one applies this terminology to [[ideals]], i.e. submodules (or subbimodules in the $2$-sided case) of a ring, algebra, or operator algebra itself. Hence we talk about __essential ideals__. For essential extensions, one considers [[extensions]] of algebras, where 'essential' still refers to non-intersection with submodules rather than with [[subalgebras]].

A monomorphism of modules $i:M\to N$ is an essential embedding if $N$ is an essential extension of $i(M)$. This alternative terminology is useful to motivate the notion of essential embeddability in $N$ as a property of $M$.

If $R$ is a ring a (say, left) $R$-module $M\neq 0$ is [[uniform module|uniform]] if every nonzero submodule of $M$ is essential. In other words, the intersection of any two nonzero submodules of $M$ is nonzero. 

## Properties

Every essential embedding $I\hookrightarrow M$ where $I$ is injective is an isomorphism. See also [[injective hull]] for related statements. 

A monomorphism $h:M\to N$ is essential iff $g\circ h$ is monic only if $g$ is monic. Indeed, if $h$ is essential and $g$ is not monic, then $Ker g\cap M\neq 0$ hence $Ker (g|_M)\neq 0$ and $g\circ h$ is not monic. Conversely, suppose $g\circ h$ is monic implies $g$ is monic. If $h$ were not essential then there would be $0\neq K\subset N$ such that $K\cap M = 0$; thus the cokernel map $g: N\to N/K$ is not monic while $g\circ h$ is monic because  $Ker(g)\cap Im(h) = K\cap M = 0$ and $h$ is monic. This is a contradiction.

[[socle|Socle]] of a module ([[internal sum]] of all [[simple module|simple]] submodules equals the intersection of all essential submodules. 

## Literature

* wikipedia [essential extension](https://en.wikipedia.org/wiki/Essential_extension)
* [[K. R. Goodearl]], R. B. Warfield, _An introduction to noncommutative Noetherian rings_, London Math. Society Student Texts __16__ (1st ed,), 1989, xviii+303 pp.; or __61__ (2nd ed.), 2004, xxiv+344 pp. 
* Louis H. Rowen, _Ring theory. Student edition_, section starting from Def. 2.10.16

In 
 
* [[Jiří Adámek]], [[Horst Herrlich]], [[Jiří Rosický]], [[Walter Tholen]], _Injective hulls are not natural_, Algebra univers. 48 (2002) 379--388 [doi](https://doi.org/10.1007/s000120200006)

the following generalization is considered. A morphism $h$ in a class $H$ of morphisms in a category $C$ is $H$-essential if for every morphism $g$, the composite
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
