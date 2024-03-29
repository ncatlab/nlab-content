
#Contents#
* table of contents
{:toc}

## Idea 

The idea of the following text is to begin with a category of objects presumed [[undirected object|undirected]] and construct from that a supercategory of directed objects, analogous to how [[Marco Grandis]] developed [[directed space|directed topological spaces]] out of the usual undirected ones.

(Rather different approaches to a notion of "directed object" will exist. See also at _[[directed homotopy theory]]_ and _[[directed homotopy type theory]]_.)

## Definition (tentative) 

Let $C$ be a [[Trimble n-category|Trimble omega-category]] with [[interval object]] $pt\stackrel{\sigma}{\to}I\stackrel{\tau}{\leftarrow}pt$, and suppose that every object $X$ of $C$ is $I$-[[undirected object|undirected]] (i.e. $[pt,X]\simeq [I,X]$).

Let $d_I \subset {}_{pt}hom(I,I)_{pt}$ be a subset of the set of [[co-span]]-endomorphisms of  $pt\stackrel{\sigma}{\to}I\stackrel{\tau}{\leftarrow}pt$. Let $dX\subset [I,X]$ be a subset of the [[hom-set]] $[I , X]$.

Then we call the pair $(X, dX)$ an *object with directed path space $dX$* (or *directed object*) if the following conditions (attributed to Marco Grandis) are satisfied:

1. (Constant paths) Every map $I \to \pt \to X$ is directed;

2. (Reparametrisation) If $\gamma\in d_I$, $\phi \in dX$, then $\gamma \circ \phi\in dX$. If e.g $d_I=[I,I]$, then this condition means that $d X$ is a sieve in $I/C$.

3. (Concatenation) Let $a,b:I\to X$ be *consecutive wrt. $I$* (i.e. $\pt \to^{\tau} I \to^{a} X$ equals $\pt \to^{\sigma} I \to^{b} X$), let $I^{v2}$ denote the pushout of $\sigma$ and $\tau$, then by the universal property of the pushout there is a map $\phi:I^{v2}\to X$. By definition of the [[interval object]] (described there in the section "Intervals for Trimble $\omega$-categories") there is a unique morphism $\psi:I\to I^{v2}$. Then the *composition of $a$ and $b$* is defined by $a\bullet b:=\phi\circ \psi$. Then $dX$ shall be closed under composition of consecutive paths.

We define a *morphism of objects with directed path space* to be a morphism of their underlying objects that preserves directed paths (i.e. if $p\in dX$, $\phi:X\to Y$, then $\phi\circ p\in d_Y$). Objects with directed path space and morphisms thereof define a category denoted by $d_I{C}$.

$C$ is a subcategory of $d_I{C}$.

## Examples 

* The category of [[directed space|directed topological spaces]] according to Grandis is of the above form $d_I{C}$ for $C = $ [[Top]], $I = [0,1]$ and $d_I = \{monotonic maps I \to I\}$.

## References

The definition and study of directed topological spaces was undertaken in

* [[Marco Grandis]], _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

Applications of categories regarded as models for directed spaces are discussed in

* [[Tim Porter]]: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88 - 100.

* [[Tim Porter]], _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))