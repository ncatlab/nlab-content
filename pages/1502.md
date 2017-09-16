A linear monoidal category (that is, a monoidal category enriched over [[Vect]]) is called _semisimple_ if it has direct sums and subobjects and if there exist objects $V_i$ labeled by an index set $I$ such that $Hom(V_i, V_j) \cong \delta_{ij} k$ where $k$ is the ground field (such objects are called _simple_) and such that for any two objects $V$ and $W$ in the category, the natural composition map
 \[
 \bigoplus_{i \in I} Hom(V, V_i) \otimes Hom(V_i, W) \rightarrow Hom(V, W)
\]
is an isomorphism.

For instance, the category of representations of a compact Lie group $G$ is semisimple, with the simple objects being precisely the irreducible representations (this is the content of Schur's lemma). If $G$ is noncompact, one needs to pass from the concept of 'direct sum' to 'direct integral'.

+-- {.query}
_Bruce_: This definition of semisimple (taken from the reference of Mueger below) does not use the concept of 'abelian category'. This is because the concepts that one thinks about with abelian categories such as kernels and cokernels do not play an important conceptual role in semisimple categories, being replaced by the more important concepts of 'direct sum' and 'subobject' . Hence it is best to give a streamlined definition from first principles without going through the language of abelian categories which would have muddied the waters.
=--

# References

* M. Mueger, [From Subfactors to Categories and Topology I. Frobenius algebras in and Morita equivalence classes of tensor categories](http://arxiv.org/math.CT/9812040). 




