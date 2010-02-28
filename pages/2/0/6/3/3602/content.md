
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _quantaloid_ is the [[horizontal categorification]] of that of [[quantale]]: a quantaloid is a quantale with many objects.

## Definition

A **quantaloid** is a category [[enriched category|enriched in]] the [[closed monoidal category|closed]] [[symmetric monoidal category]] of [[suplattice]]s. Equivalently, it may be defined as a locally [[poset]]al [[bicategory]] in which each hom-poset is cocomplete, and which admits right adjoints to composing with an arrow on either side (making it a (bi)closed bicategory). 

Taking the view that a quantaloid $Q$ is a closed bicategory, one can study categories enriched in $Q$. This can become particularly interesting if $Q$ is a **$*$-quantaloid**, i.e., comes equipped with an involution $*: Q \to Q$ which is the identity on 0-cells, reverses the direction of 1-cells, and preserves the direction of 2-cells. In that case one can study $*$-enriched categories over $Q$, i.e., $Q$-categories 

$$(X, p: X \to Q_0, d: X \times X \to Q_1)$$ 

for which $d(y, x) = d(x, y)^*$. A famous example, due to R.F.C. Walters, is given below. 

## Examples of quantaloids ##

Despite the exotic-sounding name (a portmanteau of [[quantale]] and [[groupoid]], i.e., a many-object quantale), quantaloids are quite commonplace. 

* Let $E$ be a Grothendieck topos. Then the bicategory of relations in $E$, $Rel(E)$, is a quantaloid. 

A toy form of this example: take any [[frame]] $H$, and considering the bicategory of spans in $H$: this is evidently a quantaloid, $Span(H)$. 

Here is a particularly rich source of examples. Let $Q$ be a quantale. Then there is a quantaloid $Q$-$Mat$ of $Q$-valued matrices: 

* Objects are sets $X$; 

* Morphisms $X \to Y$ are functions $M: X \times Y \to Q$. 

Matrix composition is performed according to the usual rule 

$$(M N)(x, z) = \sum_{y: Y} M(x, y) \cdot N(y, z)$$ 

where $\cdot$ is the multiplication of $Q$ and the sum is the sup in $Q$. This class of examples easily internalizes in a topos, and in that sense it subsumes the first example, $Rel(E)$, by taking $Q = \Omega$ (as an internal frame, hence a quantale). 

Slightly more generally, if $Q$ is a quantal_oid_, there is a quantaloid $Q$-$Mat$ of $Q$-matrices, as follows: 

* Objects are sets $X$ together with functions $p: X \to Q_0$; 

* Morphisms $(X, p) \to (Y, q)$ are matrices $M: X \times Y \to Q_1$ that satisfy the typing constraint $M(x, y): p(x) \to q(y)$. 

Composition works exactly as before. 

## Examples of *-quantaloids ## 

The examples in the preceding section carry over straightforwardly: 

* For $E$ a Grothendieck topos, $Rel(E)$ is a $*$-quantaloid where the $*$-operator takes a relation from $X$ to $Y$, i.e., a subobject $i: R \hookrightarrow X \times Y$, to its opposite obtained by composing $i$ with the symmetry isomorphism $X \times Y \cong Y \times X$. 

Next, let $Q$ be a [[quantale|*-quantale]]. The quantaloid $Q$-$Mat$ is as before; this becomes a $*$-quantaloid by defining the transpose of a matrix as 

* $M^*(x, y) = (M(y, x))^*$ 

This easily carries over to the case where we start with a $*$-quantaloid $Q$: we similarly obtain a $*$-quantaloid $Q$-$Mat$, by defining transpose as above. 

## Connection with Q-valued sets ## 

Let $Q$ again be a $*$-quantale; for example, $Q$ could be a frame or it could be a commutative quantale, taking the involution to be the identity. 

A **$Q$-valued set** consists of a set $X$ and a morphism $M: X \to X$ in $Q$-$Mat$ which is 

* Symmetric: $M^* = M$, 

* Idempotent: $M \circ M = M$ 

In the case where $Q = \Omega$, the subobject classifier in a topos with its locale structure, symmetry and idempotence of a relation is equivalent to the _a priori_ weaker condition of symmetry and transitivity. The reason is that $Q$-$Mat = Rel(E)$ is an [[allegory]], where the modular law holds, one of whose consequences is the inequality $M \leq M M^* M$. As a result, we have 

$$M \leq M M^* M \stackrel{sym}{=} M M M \stackrel{trans}{\leq} M M$$ 

which together with transitivity guarantees idempotence. 

Thus, symmetric idempotents in $Rel(E)$ are what are known as [[partial equivalence relation]]s (which differ from equivalence relations by dropping reflexivity), or PERs for short. 

To be continued... 
 