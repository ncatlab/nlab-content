A __dg-algebra__, or __differential graded algebra__, is a [[monoid]] in the [[symmetric monoidal category]] of (possibly unbounded) (co)[[chain complex]]es where the tensor product is given by
$$
(A\otimes B)_n = \sum_{i+j=n} A_i\otimes B_j,
$$
with the differential $d_{A\otimes B} = d_A\otimes B + A\otimes d_B$.

+--{.query}
Zoran, why would you not say that this is 'following the product rule from ordinary calculus', as I wrote?  Not that this can be proved like the product rule can, but it\'s an easy mnemonic (and a similar one works for direct sums too).  ---Toby

I find it very confusing for me at least. The Leibniz rule is about the coproduct in a single algebra; here one has several algebras with different differentials, not a single derivative operators, and not acting on a tensor square of a single algebra, so it is a bit far. If $A=B$ then I would be happy, but otherwise it is too general. ---Zoran

You mean that if $A = B$, then the Leibniz rule is a special case of this?  Then surely it is also a special case of the more general case without $A = B$?  Anyway, I think that it\'s more an example of [[vertical categorification|categorification]] than generalisation.  ---Toby
=--

A __cochain algebra__ is simply a dg-algebra following the cochain convention (where the differential $d$ raises the degree); a __chain algebra__ is simply a dg-algebra following the chain convention (where $d$ lowers the degree).