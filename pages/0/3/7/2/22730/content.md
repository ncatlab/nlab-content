+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### With multiplication, division, and identity

A __commutative [[loop (algebra)|loop]]__ is a [[commutative magma|commutative]] [[unital magma]] $(G,(-)\cdot(-):G \times G \to G,1:G)$ equipped with a binary operation $(-)/(-):G \times G \to G$ called __division__ such that $(x/y) \cdot y = x$ and $(x \cdot y)/y = x$. 

### With division and identity

A __commutative loop__ is a [[pointed]] [[magma]] $(G,/,1)$ such that:

  * For all $a$ in $G$, $a/a=1$
  * For all $a$ in $G$, $1/(1/a)=a$
  * For all $a$ and $b$ in $G$, $a/(1/b) = b/(1/a)$

with __multiplication__ defined as $a \cdot b= a/(1/b)$. 

### With multiplication, inverses, and identity

A __commutative loop__ is a [[commutative magma|commutative]] [[unital magma]] $(G, (-)\cdot(-):G\times G\to G,1:G)$ equipped with a __inverse__ $(-)^{-1}:G \to G$ such that $(x \cdot y^{-1}) \cdot y = x$ and $(x \cdot y) \cdot y^{-1} = x$. 

## Examples

* Every [[abelian group]] is a commutative loop.  

## Related concepts

* [[commutative quasigroup]]