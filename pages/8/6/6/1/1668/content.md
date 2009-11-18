Two operations, $\alpha$ and $\beta$, of an [[algebraic theory]] are said to __commute__ if for any matrix $M$ of elements, with the number of rows given by the arity of $\alpha$ and the number of columns by the arity of $\beta$, one gets the same result whether one

1. applies $\alpha$ to each column of $M$ and then $\beta$ to the resulting row, or
1. applies $\beta$ to each row of $M$ and then $\alpha$ to the resulting column.

(It is left as an exercise to the reader to formulate this notion in an element-free way.) Note that an operation of arity $0$ or $1$ always commutes with itself; this is not necessarily the case for higher arities. Commuting nullary operations are necessarily equal.

The operations that commute with a given set of operations in an algebraic theory form a subtheory. The __centre__ of an algebraic theory is given by the operations that commute with all the operations of the theory. An algebraic theory is __commutative__ if every pair of its operations commute. Another way of describing the centre is to say that it consists of those operations which are also homomorphisms; an algebraic theory is commutative if all of its operations are homomorphisms.

If $f_1,\ldots , f_n$ are homomorphisms $A \to B$ of models (algebras) of a commutative algebraic theory, and $\omega$ is an n-ary operation of it, then the function $A \to B$ given by sending $a \in A$ to $\omega(f_1(a),\ldots ,f_n(a)) \in B$ is again a homomorphism, which is naturally called $\omega(f_1,\ldots ,f_n)$. In this way $Hom(A,B)$ is enriched as a model of the algebraic theory, and we have a [[closed category]] of models and homorphisms. Furthermore, this internal $Hom$ has a left adjoint $\otimes$ for which the free model on one generator is a unit, so we have a [[closed monoidal category]].

The notion of commutative algebraic theory was formulated in terms of [[monad]]s by Anders Kock.


### References ###

+-- {: .query}
Can we have some please!  This is something I want to use soon so it'd be nice to know where the details were originally worked out. ---Andrew 

=--

* Anders Kock, Monads on symmetric monoidal closed categories, Arch. Math. 21 (1970), 1-10. 

* Anders Kock, Strong functors and monoidal monads, Arhus Universitet, Various Publications Series No. 11 (1970). 

See also [here](http://home.imf.au.dk/kock/SFMM.pdf). 
