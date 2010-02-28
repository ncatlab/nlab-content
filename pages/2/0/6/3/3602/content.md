
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

## Example: sheaves on a locale

To be written... 
