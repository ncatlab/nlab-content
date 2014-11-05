
# Confluent categories
* table of contents
{: toc}

## Definition

A [[category]] is **confluent** if for any [[span]] $B \leftarrow A \to C$, there exists a [[cospan]] $B \to D \leftarrow C$.  Note that we do not require the resulting square to [[commutative diagram|commute]].


## Remarks

If the morphisms in a category represent (sequences of) "rewriting" operations, then confluence means that any two ways to rewrite the same thing can eventually be brought back together.  This is a good property of rewriting in systems such as the [[lambda calculus]] (the [[Church-Rosser theorem]]), and as such it is a property one might expect for the hom-categories in a [[2-category|2-categorical]] model of lambda calculus.

Another good property one might want to assume is termination, i.e. the lack of infinite chains of nonidentity arrows.

As stated in the definition, the notion of confluence is perfectly sensible if we replace "category" by "[[directed graph]] (quiver)". However, it is also occasionally useful to strengthen the notion the notion of confluence so that commutativity of the resulting square holds in the category. An example is Mac Lane's proof of the coherence theorem for monoidal categories (as given in [[Cats Work]]), where the "rewrite" arrows are expanded (whiskered) instances of associativity morphisms $\alpha_{A B C}: (A \otimes B) \otimes C \to A \otimes (B \otimes C)$ (as opposed to their inverses). 


## Related pages

* [[lambda-calculus]]

* [[diamond]]


## References

* John Baez, [2-categories of computation](http://math.ucr.edu/home/baez/qg-winter2007/w07week04b.pdf).

* Barnaby P. Hilken, [Towards a proof theory of rewriting: the simply-typed 2&#955;-calculus](http://math.ucr.edu/home/baez/qg-winter2007/hilken_2lambda_calculus.ps),
*Theor. Comp. Sci.* **170** (1996), 407-444. 


[[!redirects confluent category]]
[[!redirects confluent categories]]

[[!redirects confluence]]
[[!redirects confluences]]
