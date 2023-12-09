
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Just as a [[groupoid]] is the [[oidification]] of a [[group]] and a [[ringoid]] is the oidification of a [[ring]], a [[magmoid]] should be the oidification of a [[magma]]. 

## Definition

### With a set of morphisms

Let $Q$ be a [[quiver]] with a collection of objects $Ob(Q)$, a set of morphisms $Mor(Q)$, a function $s: Mor(Q) \to Ob(Q)$ called the __source__ or __domain__ and a function $t: Mor(Q) \to Ob(Q)$ called the __target__ or __codomain__. A __magmoid__ is a quiver $Q$ with a [[partial map|partial binary operation]] 

$$\left(-\right)\circ\left(-\right): Mor(Q) \times Mor(Q) \to Mor(Q) + 1$$ 

with coproduct injections $inj:Mor(Q) \to Mor(Q) + 1$ and $pt: 1 \to Mor(Q) + 1$, such that for $f, g \in Mor(Q)$, there is a function $h$ in the inverse image of $inj(h) = f \circ g$ if $s(f) = t(g)$, and $f \circ g = pt(\bullet)$ otherwise. 

### With a family of sets of morphisms

Let $Q$ be a [[quiver]] with a collection of objects $Ob(Q)$ and a [[Set]]-valued functor $Mor: Ob(Q) \times Ob(Q) \to Set$ for all objects $a, b \in Ob(Q)$. A __magmoid__ is a quiver $Q$ with a binary operation 

$$\left(-\right)\circ\left(-\right): Mor(b,c) \times Mor(a,b) \to Mor(a,c)$$ 

for all $a,b,c \in Ob(Q)$. 

### Weak and strict magmoids

A __weak magmoid__ is a magmoid $Q$ whose collection of objects $Ob(Q)$ form a [[groupoid]], while a __strict magmoid__ is a magmoid $Q$ whose collection of objects $Ob(Q)$ form a [[set]]. 

### Enriched magmoids

Let $V$ be a [[monoidal category]] (or a [[monoidal (infinity,1)-category]]) and let $Q$ be a $V$-enriched [[quiver]], with a collection of objects $Ob(Q)$ and a $V$-valued functor $Mor: Ob(Q) \times Ob(Q) \to V$ for all objects $a, b \in Ob(Q)$. A __$V$-enriched magmoid__ is a $V$-enriched quiver $Q$ with a binary operation 

$$\left(-\right)\circ\left(-\right): Mor(b,c) \times Mor(a,b) \to Mor(a,c)$$ 

for all $a,b,c \in Ob(Q)$. 

## Examples

A [[transitive relation]] is a magmoid [[enriched category|enriched]] in [[truth values]], or a magmoid $M$ where there is at most one morphism from every object $a$ to another object $b$ in $M$.

[[!include oidification - table]]

## Related concepts

* [[magmoidal category]]
* [[H-magmoid]]

## References

The terminology seems to have been introduced in:

* A. Arnold, M. Dauchet, *Théorie des magmoïdes (I)*, RAIRO -- Informatique Théorique **12** 3 (1978) 235-257 &lbrack;[numdam:ITA_1978__12_3_235_0](http://www.numdam.org/item/?id=ITA_1978__12_3_235_0), [eudml:92079](https://eudml.org/doc/92079)&rbrack;

* A. Arnold, M. Dauchet, *Théorie des magmoïdes (II)*, RAIRO -- Informatique Théorique **13** 2 (1979) 135-154 &lbrack;[numdam:ITA_1979__13_2_135_0](http://www.numdam.org/item/ITA_1979__13_2_135_0)&rbrack;

Further discussion:

* Miklos Bartha, p. 101 in: *An algebraic model of synchronous systems*, Information and Computation
**97** 1 (1992) 97-131

* Dan Jonsson, Def. 2.2 in: *On Group-Like Magmoids* &lbrack;[arXiv:1902.06109](https://arxiv.org/abs/1902.06109)&rbrack;


* {#Torzewska22} [[Fiona Torzewska]], §2.1 of: *Topological quantum field theories and homotopy cobordisms* &lbrack;[arXiv:2208.14504](https://arxiv.org/abs/2208.14504)&rbrack;

[[!redirects magmoids]]

[[!redirects enriched magmoid]]
[[!redirects enriched magmoids]]