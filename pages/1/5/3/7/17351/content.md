# Smothering 2-functors

* table of contents
{:toc}

## Idea

A *smothering 2-functor* is the [[strict 2-category|2-categorical analogue]] of a [[smothering functor]].

## Definition

A 2-functor $F:C\to D$ is **smothering** if

1. It is [[surjective on objects]], and
1. It is *locally smothering*, i.e. each hom-functor $C(x,y) \to D(F x, F y)$ is a [[smothering functor]].  Thus, $F$ is full on 1-cells, full on 2-cells, and conservative on 2-cells.

## Properties

* Smothering 2-functors reflect equivalences: if $f:x\to y$ is in $C$ and $F(f)$ is an equivalence, then $f$ is an equivalence.  For by fullness on 1-cells, any inverse of $F(f)$ lifts to $C$, by fullness on 2-cells, the comparison 2-cells lift to $C$, and then by conservativity those lifts are again isomorphisms.

* Applying fullness on 1-cells again, if $x,y\in C$ and $F x \simeq F y$ in $D$, then $x\simeq y$ in $C$.

* Smothering 2-functors lift and reflect adjoints: any [[adjunction]] in $D$ is the image of some adjunction in $C$, and the lift can make use of any specified lifts of the objects, 1-cells, and either the unit or the counit 2-cell.  This is [RV, 4.5.2](#RV); the idea is to lift the missing 2-cell arbitrarily and then "fix" it by composing with the inverse of one [[triangle identity]] composite (which is an isomorphism by 2-cell conservativity).

## Examples

* For any [[∞-cosmos]] $K$, there is a smothering 2-functor $(K/A)_2 \to K_2/A$, where $K_2$ denotes the [[homotopy 2-category]] of an [[∞-cosmos]].  In the special case when $K=QCat$ consists of [[quasi-categories]], this is [RV, 3.4.7](#RV).

## Related pages

* [[smothering functor]]

## References

* [[Emily Riehl]], [[Dominic Verity]], _The 2-category theory of quasi-categories_, [arXiv](http://arxiv.org/abs/1306.5144)
 {#RV}
