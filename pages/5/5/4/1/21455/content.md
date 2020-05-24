
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In the context of [[gauge theory|gauging]] of [[U-duality]]-[[symmetry groups]] of  [[supergravity]]-theories to _[[gauged supergravity]]_, the _embedding tensor_ ([Nicolai-Samtleben 00](#NicolaiSamtleben00)) is the datum that specifies which [[subgroup]] of the [[global symmetry|global]] [[U-duality]] is promoted to a [[gauge group]]. The requirement of [[supersymmetry]] and of consistency then implies conditions on this choice, called the "linear constraint" and the "quadratic constraint". 

Formalized in terms of [[Lie theory]] ([Lavau 17](#Lavau17)) these conditions say that an embedding tensor is a [[homomorphism]] of [[Leibniz algebras]] from a [[Lie module]] to the underlying [[Lie algebra]] (the "quadratic constaint") where the [[Leibniz algebra|Leibniz]]-[[magma|product]] on the module is given by the Lie action induced by that homomorphism itself (the "linear constraint").

Any choice of embedding tensor for a [[gauged supergravity]] is supposed to induce a _[[tensor hierarchy]]_ ([de Wit-Samtleben 05](tensor+hierarchy#deWitSamtleben05), [08](tensor+hierarchy#deWitSamtleben08)) of higher degree [[differential form]]-[[field (physics)|fields]] which jointly serve as ever higher order corrections to the resulting gauge-covariance of the [[field strengths]]. This tensor hierarchy may be understood as a [[dg-Lie algebra]]/[[L-∞ algebra]]-[[mathematical structure|structure]] which lifts the [[Leibniz algebra]]-structure implied/induced by the embedding tensor ([Lavau 17](#Lavau17), [Lavau-Palmkvist 19](#LavauPalmkvist19), [Lavau-Stasheff 19](#LavauStasheff19)).


## Definition
 {#Definition}

+-- {: .num_defn}
###### Definition
**([[embedding tensor]])**

Given 

* $\mathfrak{g}$ a [[Lie algebra]],

* $\mathfrak{g} \otimes V \overset{\rho}{\longrightarrow} V $ a [[Lie algebra representation]] of $\mathfrak{g}$,

then an *embedding tensor* is a [[linear map]]

$$
  \Theta
  \;\colon\;
  V \longrightarrow \mathfrak{g}
$$

such that for all $v_i \in V$ the following condition ("quadratic constraint") is satisfied:

\[
  \label{QuadraticConstraint}
  [\Theta(v_1), \Theta(v_2)]
  \;=\;
  \Theta
  \big(
    \rho_{\Theta(v_1)}(v_2)
  \big)
  \,,
\]

where on the left we have the [[Lie bracket]] of $\mathfrak{g}$.

=--

The idea of this definition goes back to [Nicolai-Samtleben 00](#NicolaiSamtleben00), with many followups  in the literature on [[tensor hierarchies]] in [[gauged supergravity]]. The above mathematical formulation is due to [Lavau 17](#Lavau17).

+-- {: .num_remark #RelationToLeibnizAlgebraStructure}
###### Remark
**([[Leibniz algebra]]-[[mathematical structure|structure]])**

The "quadratic constraint" (eq:QuadraticConstraint) implies (see [this Prop.](Leibniz+algebra#LeibnizAlgebraFromLieModuleAndEmbeddingTensor)) that the [[magma|product]]

\[
  \label{InducedLeibnizAlgebraStructure}
  \array{
     V \otimes V
     &\overset{ }{\longrightarrow}&
     V
     \\
     (v_1, v_2) 
       &\mapsto& 
     v_1 \cdot v_2 
     \mathrlap{
       \;\coloneqq\;
       \rho_{\Theta(v_1)}(v_2)
     }
  }
\]

makes (the underlying [[vector space]] of) $V$ a [[Leibniz algebra]].
Conversely, if a [[Leibniz algebra]] structure "$\cdot$" on $V$ is already given, we may ask that it coincides with this one induced from the embedding tensor, a condition then called the _linear constraint_:

\[
  \label{LinearConstraint}
  v_1 \cdot v_2 \;=\; \rho_{\Theta(v_1)}(v_2)
  \,.
\]

With respect to this induced Leibniz algebra structure, hence equivalently with the "linear constraint" (eq:LinearConstraint) understood, the "quadratic constraint" (eq:QuadraticConstraint) equivalently says that the embedding tensor is a [[homomorphism]] of [[Leibniz algebras]] (using that [[Lie algebras]] are special cases of a Leibniz algebras):

$$
  [\Theta(v_1), \Theta(v_2)]
  \;=\;
  \Theta(v_1 \cdot v_2)
  \,.
$$

=--

## Relation with double and exceptional field theory
See [Hohm-Samtleben 19](#HohmSamtleben19) for a review.


## Related concepts

* [[gauged supergravity]]

* [[tensor hierarchy]]

* [[double field theory]], [[exceptional field theory]]


## References

The concept in [[gauged supergravity]] originates with

* {#NicolaiSamtleben00} [[Hermann Nicolai]], [[Henning Samtleben]], _Maximal gauged supergravity in three dimensions_, Phys. Rev. Lett. 86 (2001) 1686-1689 ([arXiv:hep-th/0010076](https://arxiv.org/abs/hep-th/0010076))

For further references see at _[[tensor hierarchy]]_.

The mathematical formulation above is due to 

* {#Lavau17} [[Sylvain Lavau]], _Tensor hierarchies and Leibniz algebras_, J. Geom. Phys. 144:147-189 (2019) ([arXiv:1708.07068](https://arxiv.org/abs/1708.07068))

See also

* {#LavauPalmkvist19} [[Sylvain Lavau]], [[Jakob Palmkvist]], _Infinity-enhancing of Leibniz algebras_ ([arXiv:1907.05752](https://arxiv.org/abs/1907.05752))

* {#LavauStasheff19} [[Sylvain Lavau]], [[Jim Stasheff]], _$L_\infty$-algebra extensions of Leibniz algebras_ ([arXiv:2003.07838](https://arxiv.org/abs/2003.07838))

For a review of the relation with [[double field theory]] and [[exceptional field theory]] see

* {#HohmSamtleben19} [[Henning Samtleben]], [[Olaf Hohm]], _Higher Gauge Structures in Double and Exceptional
Field Theory_ ([arXiv:1903.02821](https://arxiv.org/abs/1903.02821))


[[!redirects embedding tensors]]
