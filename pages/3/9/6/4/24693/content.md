
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


* table of contents
{: toc}


## Idea
 {#Idea}


__$FinInj$__ (or __$FinSet_inj$__ or often just **$FI$**) refers to the [[wide subcategory]] of [[FinSet]] with its [[morphisms]] restricted to [[monomorphisms]] ([[injective functions]]).

It [may be characterised](https://github.com/punkdit/categories/blob/master/www.mta.ca/cat-dist/archive/2008/08-12#L1944-L1959) as:

* the free ([[symmetric monoidal category|symmetric]]) [[semicocartesian category]] on a single object

* the free [[symmetric monoidal category]] on a pointed object $I \to X$ (where $I$ is the [[monoidal category|monoidal unit]])

* the free [[monoidal category]] on an object $X$ equipped with an involution $s : X \otimes X \to X \otimes X$ satisfying the braid relations, and a morphism $i : I \to X$ satisfying $s \circ i \otimes X = s \circ X \otimes i$

A [[functor]] from $FinSet_{inj}$ to [[Vect]] (or more generally to some $R$[[Mod]]) is also known as an *[[FI-representation]]*, a kind of accumulated form of [[representation theory of the symmetric group|$Sym(n)$-representations]] as $n \in \mathbb{N}$ ranges (cf. also *[[representation stability]]*).

## Related concepts

* [[Inj]]

* [[FinSet]]

* [[FI-representation]]

[[!redirects FinSetInj]]
