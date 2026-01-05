
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents


## Idea

Let $\mathcal{C}$ be a [[category of modules]] or [[bimodules]] over a fixed ring. 

\begin{definition}
\label{EssentialSubmodule}
A [[subobject]] $M\subset N$ is an *essential submodule* of $N$ 
if $M$ has non-[[zero object|zero]] intersection ([[pullback]]) with any non-[[zero object|zero]] subobject of $N$, or equivalently, if $M$ has zero intersection with only the [[zero object|zero subobject]] of $N$.

\end{definition} 

\begin{remark}
**(terminology)**
Some authors call an essential submodule $M \subset N$ a _large submodule_, or say that $N$ is an _essential extension_ of $M$, while others argue that this should be called an _inessential extension_. 

A [[monomorphism]] of modules $i \colon M\to N$ is called an *essential monomorphism* or an *essential embedding* if $N$ is an essential extension of $i(M)$. This alternative terminology is useful for motivating the notion of *essential embeddability* in $N$ as a property of $M$.

In particular, this terminology is also applied to [[ideals]], i.e., submodules (or sub-bimodules, in the $2$-sided case) of the ring. Hence, one speaks of _essential ideals_, etc. For essential extensions, one considers [[extensions]] of algebras, where 'essential' still refers to non-zero intersection with submodules rather than with subalgebras.

For [[C-star algebras|$C^\ast$-algebras]], essential ideals are required to be [[closed subset|closed]] and 2-sided.

\end{remark}

In [AHRT02](#AHRT02), the following generalized notion is considered.

\begin{definition}
A [[morphism]] $h$ in a [[class]] $H$ of morphisms in a category $\mathcal{C}$ is *$H$-essential* if, for every morphism $g$ in $\mathcal{C}$, $g$ is in $H$ whenever $g\circ h$ is in $H$.

\end{definition}

For $H$ the class of monomorphisms in a category of modules, this reduces to the above notion of essential extensions.

[[coessential epimorphism|Coessential epimorphisms]] are the dual notion; they define [[superfluous submodule]]s.

The [[singular submodule|singular submodule]] of a left $R$-module $M$ is the subset $\mathcal{Z}(M)$ of all elements in $M$ whose annihilator is an essential left ideal of $R$.

## Properties

\begin{proposition}
If $R$ is a ring, a (left, say) $R$-module $M\neq 0$ is [[uniform module|uniform]] if every nonzero submodule of $M$ is essential. In other words, the intersection of any two nonzero submodules of $M$ is nonzero.

\end{proposition}

\begin{proposition}
Every essential embedding $I\hookrightarrow M$ where $I$ is [[injective morphism|injective]] is an [[isomorphism]].

\end{proposition}

See [[injective hull]] for related statements. 

\begin{proposition}
A monomorphism $h\colon M\to N$ is essential iff, for all morphisms $g$, we have that $g$ is monic if $g\circ h$ is monic.

\end{proposition}

\begin{proof}
Indeed, if $h$ is essential and $g$ is not monic, then $Ker g\cap M\neq 0$, and hence $Ker (g|_M)\neq 0$ and $g\circ h$ is not monic. Conversely, suppose that $g$ is monic whenever $g\circ h$ is monic. If $h$ were not essential, then there would be $0\neq K\subset N$ such that $K\cap M = 0$; thus the cokernel map $g: N\to N/K$ is not monic, while $g\circ h$ is monic because  $Ker(g)\cap Im(h) = K\cap M = 0$ and $h$ is monic. Since this is a contradiction, the claim follows.

\end{proof}

\begin{proposition}
The [[socle]] of a module (the [[internal sum]] of all [[simple module|simple]] submodules) equals the intersection of all its essential submodules.

\end{proposition}

## Literature

* Wikipedia, [Essential extension](https://en.wikipedia.org/wiki/Essential_extension)

* [[K. R. Goodearl]], R. B. Warfield, _An introduction to noncommutative Noetherian rings_, London Math. Society Student Texts __16__ (1st ed,), 1989, xviii+303 pp.; or __61__ (2nd ed.), 2004, xxiv+344 pp. 

* Louis H. Rowen, starting from Def. 2.10.16 in: *Ring theory -- Student edition*, Academic Press (1991, 2012)
 
* {#AHRT02} [[Jiří Adámek]], [[Horst Herrlich]], [[Jiří Rosický]], [[Walter Tholen]], _Injective hulls are not natural_, Algebra univers. **48** (2002) 379-388 &lbrack;[doi:10.1007/s000120200006](https://doi.org/10.1007/s000120200006)&rbrack;



category: algebra, operator algebras

[[!redirects essential submodule]]
[[!redirects essential submodules]]
[[!redirects essential ideal]]
[[!redirects essential ideals]]
[[!redirects essential extension]]
[[!redirects essential extensions]]
[[!redirects essential embedding]]
[[!redirects essential embeddings]]
[[!redirects essential monomorphism]]
[[!redirects essential monomorphisms]]
