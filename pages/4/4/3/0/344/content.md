#Definition#

An __extensive category__ is a category $E$ with finite coproducts such that one, hence all, of the following equivalent conditions holds:

 1. Finite coproducts are disjoint and stable under pullback.
 1. For any objects $a,b$ the coproduct functor $E/a \times E/b \to E/(a+b)$ is an equivalence of categories.
 1. a certain pair of squares is a pullback if and only if it is a coproduct (see the paper referenced below).

Extensive categories are also called __positive categories__, especially if they are also [[coherent category|coherent]].

If an extensive category also has finite limits, it is called __lextensive__ or __finitary disjunctive__.

#Arity#

The definition refers only to binary coproducts, but it obviously implies analogous statements for $n$-ary coproducts for all $n\ge 1$.  Less obviously, it also implies the analogous statement for 0-ary coproducts (that is, initial objects).  In this case, the statement is that the initial object 0 is _strict_, meaning that any map $a\to 0$ is an isomorphism.

In the other direction, if $E$ has all small coproducts and the analogous infinitary condition holds, $E$ is called __$\infty$-extensive__ or __$\infty$-positive__.  (Note that this use of $\infty$ is completely unrelated to $\infty$-[[infinity-category|categories]].)

+--{.query}
Can we say 'small-extensive'? Or even redefine 'extensive' to have this meaning, using 'finitely extensive' for the first version? &#8212;Toby
=--

#Examples#

1. A [[topos]] is an (l)extensive category.

1. The category of topological spaces is (l)extensive. 

1. The category of affine schemes (opposite to the category of commutative rings with identity) is (l)extensive. 

1. The category Cat is (l)extensive.

#Extensive sites#

If a (small) [[site]] is (small) $\infty$-extensive, then one can replace any [[cover]] with a single map. That is, replace the covering family $(j_i: U_i \to B)_i$ with the map $[j_i]_i: \coprod_i U_i \to B$. In other words, the singleton covers form a basis for the Grothendieck coverage on the site.

#References#

Carboni, Aurelio and Lack, Stephen and Walters, R. F. C., _Introduction to extensive and distributive categories_, JPAA 84 no. 2