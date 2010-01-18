#Idea#

A mathematical structure is _essentially algebraic_ if its definition involves [[functional relation|partially defined operations]] satisfying equational laws, where the domain of any given operation is a subset where various other operations happen to be equal.  And actual [[algebraic theory]] is one where all operations are total [[function]]s.

The most familiar example may be the (strict) notion of [[category]]: a [[small category]] consists of a set $C_0$ of objects, a set $C_1$ of morphisms, source and target maps $s,t : C_1 \to C_0$ and so on, but composition is only defined for pairs of morphisms where the source of one happens to equal the target of the other.

Essentially algebraic theories can be understood through [[category theory]] at least when they are finitary, so that all operations have only finitely many arguments.  This gives a generalisation of [[Lawvere theory|Lawvere theories]], which describe finitary [[algebraic theory|algebraic theories]].

As the domains of the operations are given by the solutions to equations, they may be understood using the notion of [[equalizer]].  So, just as a Lawvere theory is defined using a category with finite [[product]]s, an essentially algebraic theory is defined using a category with finite [[limit|limits]] &#8212; or in other words, finite products and also equalizers (from which all other finite limits, including [[pullback]]s, may be derived).

*Please add a formal definition and more information on how we actually use essentially algebraic theories to describe essentially algebraic mathematical structures!*


[[!redirects essentially algebraic theories]]