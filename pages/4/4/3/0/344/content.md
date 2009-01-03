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

#References#

Carboni, Aurelio and Lack, Stephen and Walters, R. F. C., _Introduction to extensive and distributive categories_, JPAA 84 no. 2
