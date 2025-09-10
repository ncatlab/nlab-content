+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Statement

The _tangle hypothesis_ ([Baez and Dolan 95](#BaezDolan95)) is as follows:
+-- {: .un_prop}
###### Tangle Hypothesis

The $n$-category of framed $n$-[[tangles]] in $n+k$ dimensions is $(n+k)$-equivalent to the free [[k-tuply monoidal n-category]] with duals on one object.
=--

The tangle hypothesis may be seen as a refinement of the [[cobordism hypothesis]] in the sense that the latter arises from the former in the limit $k \to \infty$:
+-- {: .un_prop}
###### [[cobordism hypothesis|Cobordism Hypothesis]]

The $n$-category $n Cob$ of cobordisms is the free stable $n$-category with duals on one object (the point).
=--


## Generalized tangle hypothesis

### Tangles with structure

The tangle hypothesis has been generalized to allow certain structures on the tangles.

The $k$-tuply monoidal $n$-category of $G$-structured $n$-tangles in the $(n + k)$-cube is the [[fundamental category|fundamental]] $(n + k)$-category with duals of $(M G,Z)$.

* $M G$ is the [[Thom space]] of group $G$.
* $G$ can be any group equipped with a homomorphism to $O(k)$. ([comment](http://golem.ph.utexas.edu/category/2006/11/this_weeks_finds_in_mathematic_2.html#c006471))

### Tangles with singularities

The tangle hypothesis can further be generalized to allow for 'tangles with singularities' (also called [[stratified space|stratified]] tangles). The idea is analogous to that of [[cobordism hypothesis#ForCobordismsWithSingularities|cobordisms with singularities]]. The tangle hypothesis for tangles with singularities includes the case of $G$-structured tangles (which requires choosing generators for $M G$, that then yield a datum of singularity types, see ([Lurie 09, Sec. 4.3](#LurieCTFT))).

The generalized tangle hypothesis is closely related to the generalized [[Pontrjagin-Thom collapse map#ReferencesPontrjaginThomConstruction|Thom-Pontryagin construction]] which relates homotopy classes of maps from manifolds $M$ into CW complexes $X$ to cobordism classes of $X$-stratifications of $M$. (The relation was discussed on the $n$Café [here](https://golem.ph.utexas.edu/category/2006/11/this_weeks_finds_in_mathematic_2.html#c006196) and [here](https://golem.ph.utexas.edu/category/2023/03/an_invitation_to_geometric_hig.html).)

### Directed variants

[[manifold diagram|Manifold diagrams]] are stratified tangles 'without critical points'. The relation of stratified tangles to presented higher categories with duals is analogous to the relation of manifold diagrams to presented higher categories (without the need for duals). This yields a "directed" version of the generalized tangle hypothesis.


## The tangle hypothesis as a consequence of the cobordism hypothesis

While the tangle hypothesis and its generalizations may be seen as refinements of the cobordism hypothesis and its generalizations, Lurie shows ([Lurie 09, Sec. 4.4](#LurieCTFT)) that the former may be deduced from the latter when expressed in a sufficiently general form (namely, for cobordisms with singularities).


## Related concepts

* [[cobordism hypothesis]]

* [[open problems in category theory]]

## References

* {#BaezDolan95} [[John Baez]], [[James Dolan]], p. 28 of: *Higher dimensional algebra and Topological Quantum Field Theory*, J. Math. Phys. **36** (1995) 6073-6105 &lbrack;[doi:10.1063/1.531236](https://doi.org/10.1063/1.531236)[arXiv:q-alg/9503002](http://arxiv.org/abs/q-alg/9503002)&rbrack;

* {#LurieCTFT}[[Jacob Lurie]], [[On the Classification of Topological Field Theories]]  ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))

* {#LurieTQFT}[[Jacob Lurie]], _TQFT and the cobordism hypothesis_, videos of 4 lectures at the [Geometry Research Group](http://www.ma.utexas.edu/users/plowrey/dev/rtg/perspectives.html), Mathematics Department, University of Texas Austin. Lecture notes for Lurie's talks are available at the [Geometry Research Group website](http://www.ma.utexas.edu/users/plowrey/dev/rtg/perspectives.html).

For a discussion of the generalized tangle hypothesis see

* [n-Category Caf&eacute;] (http://golem.ph.utexas.edu/category/2006/11/this_weeks_finds_in_mathematic_2.html#c006381), This Week’s Finds in Mathematical Physics (Week 241)
* [n-Category Café](https://golem.ph.utexas.edu/category/2023/03/an_invitation_to_geometric_hig.html), Invitation to geometric higher categories

[[!redirects generalized tangle hypothesis]]

[[!redirects Tangle Hypothesis]]