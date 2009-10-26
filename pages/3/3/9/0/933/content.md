
#Contents#
* automatic table of contents
{:toc}

#Definition#

A __dg-algebra__, or __[[differential graded algebra]]__, is a [[monoid]] in the [[symmetric monoidal category]] of (possibly unbounded) [[chain complex]]es or [[]cochain complex]es with its standard structure of a [[monoidal category]]. 

For the case of chain complexes we also speak of **chain algebras**.

For the case of cochain complexes we also speak of **cochain algebras**.

Recall 

* that the standard tensor product on (co)chain complexes is given by
$$
(A\otimes B)_n = \sum_{i+j=n} A_i\otimes B_j,
$$
with the differential $d_{A\otimes B} = d_A\otimes B + A\otimes d_B$.

* that a [[monoid]] in a [[monoidal category]] $C$ is an object $A$ in $C$ together with a morphism

  $$
    \cdot : A \otimes A \to A
  $$

  that is unital and associative in the obvious sense.

This implies that a dg-algebra is, more concretely, a graded algebra $A$ equipped with a linear map $d : A \to A$ with the property that

* $d\circ d = 0$

* for $a \in A$ homogeneous of degree $k$, the element $d a$ is of degree $k+1$ (for monoids in cochain complexes) of of degree $k-1$ (for monoids in chain complexes)

* for all $a,b \in A$ with $a$ homogeneous of degree k the **graded Leibniz rule** holds

  $d (a \cdot b) = (d a) \cdot b + (-1)^k a \cdot (d b)$.   

A more detailed disucssion of this is at

* [[differential graded algebra]].

# relation to cosimplicial alghebras #


The [[monoidal Dold-Kan correspondence]] effectively identifies non-negatively graded chain algebras with simplicial algebras, and non-negatively graded cochain algebras with [[cosimplicial algebra]]s.

Since cosimplicial algebras have a fundamental interpretation dual to [[∞-space]], as described at [[∞-quantity]], this can be understood as explaining the great role differential graded algebras are playing in various context, suchh as notably in 

* [[rational homotopy theory]].


#Discussion#

A previous version of this entry gave rise to the following discussion

+--{.query}
Zoran, why would you not say that this is 'following the product rule from ordinary calculus', as I wrote?  Not that this can be proved like the product rule can, but it\'s an easy mnemonic (and a similar one works for direct sums too).  ---Toby

I find it very confusing for me at least. The Leibniz rule is about the coproduct in a single algebra; here one has several algebras with different differentials, not a single derivative operators, and not acting on a tensor square of a single algebra, so it is a bit far. If $A=B$ then I would be happy, but otherwise it is too general. ---Zoran

You mean that if $A = B$, then the Leibniz rule is a special case of this?  Then surely it is also a special case of the more general case without $A = B$?  Anyway, I think that it\'s more an example of [[vertical categorification|categorification]] than generalisation.  ---Toby

For some special algebras this is true. For example, the dual of symmetric algebra as a Hopf algebra can be identified with the infinite order formal differential operators with constant coefficients (the isomorphism is given by evaluation at zero). Thus the Leibniz rule for derivatives is indeed the dual coproduct to the product on the symmetric algebras. There are braided etc. generalizations to this, and a version for computing the coproduct on a dual of enveloping algebras. In physics the addition of momenta and angular momenta for multiparticle systems is exactly coming from this kind of coproduct. But in all these cases the operators whose product you are taking live in a representation of a single algebra. --- Zoran

=--




[[!redirects chain algebra]]
[[!redirects cochain algebra]]