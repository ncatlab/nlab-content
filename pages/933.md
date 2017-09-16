A __dg-algebra__, or __differential graded algebra__, is a [[monoid]] in the [[symmetric monoidal category]] of (possibly unbounded) (co)[[chain complex]]es where the tensor product is given by
$$
(A\otimes B)_n = \sum_{i+j=n} A_i\otimes B_j,
$$
with the differential $d_{A\otimes B} = d_A\otimes B + A\otimes d_B$.

+--{.query}
Zoran, why would you not say that this is 'following the product rule from ordinary calculus', as I wrote?  Not that this can be proved like the product rule can, but it\'s an easy mnemonic (and a similar one works for direct sums too).  ---Toby

I find it very confusing for me at least. The Leibniz rule is about the coproduct in a single algebra; here one has several algebras with different differentials, not a single derivative operators, and not acting on a tensor square of a single algebra, so it is a bit far. If $A=B$ then I would be happy, but otherwise it is too general. ---Zoran

You mean that if $A = B$, then the Leibniz rule is a special case of this?  Then surely it is also a special case of the more general case without $A = B$?  Anyway, I think that it\'s more an example of [[vertical categorification|categorification]] than generalisation.  ---Toby

For some special algebras this is true. For example, the dual of symmetric algebra as a Hopf algebra can be identified with the infinite order formal differential operators with constant coefficients (the isomorphism is given by evaluation at zero). Thus the Leibniz rule for derivatives is indeed the dual coproduct to the product on the symmetric algebras. There are braided etc. generalizations to this, and a version for computing the coproduct on a dual of enveloping algebras. In physics the addition of momenta and angular momenta for multiparticle systems is exactly coming from this kind of coproduct. But in all these cases the operators whose product you are taking live in a representation of a single algebra. --- Zoran
=--

A __cochain algebra__ is simply a dg-algebra following the cochain convention (where the differential $d$ raises the degree); a __chain algebra__ is simply a dg-algebra following the chain convention (where $d$ lowers the degree).

+--{.query}
[[Tim Porter|Tim]]:  From the point of view of exposition, there is a good case for someone (?) to do  entries on graded object, differential graded object, chain complexes, together with setting conventions for degree of a map, tensor product etc. Then 'graded algebra' and 'differential algebra' make sense and a dga is then the combination of the two. (I have some tex code that does introduce things in this way and I can make it available to you both to see if you think it works.  As it would require  the addition of quite a lot on new entries I don't feel like putting them on if they prove unnecessary.)
=--