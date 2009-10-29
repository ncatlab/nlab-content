<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Defintion#

Write $dgRing$ for the [[category]] of [[monoid]]s in the category of [[cochain complex]]es of abelian groups.

A [[dg-algebra]] is a dg-ring that is degreewise a $k$-[[vector spac]e] over some field $k$.

+-- {: .un_defn}
###### Definition

The  **projective** [[model category]] structure on $dgRing$ is given by setting:

* weak equivalences are the [[quasi-isomorphism]]s

* fibrations are the degreewise surjections.

=--

+-- {: .un_prop }
###### Proposition

This indeed defines a [[model category]] and in fact a [[cofibrantly generated model category]].

=--

+-- {: .proof}
###### Proof

See the references below.

=--


#References#



The cofibrantly generated model structure on commutative cochain [[dg-algebra]]s induced from the forgetful functor to cochain complexes is discussed for instance on p. 6 of 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

For commutative dg-rings see also

* A. Bousfield, V. Gugenheim, _On PL deRham theory and rational homotopy type_ Memoirs of the AMS 179 (1976)


The model structure on general dg-algebras is discussed for instance in

section V.3 of

* [[Sergei Gelfand]], [[Yuri Manin]], _Methods of homological algebra_, Springer

Also

* J.F. Jardine, _[[JardineModelDG.pdf:file]]_ , Cyclic Cohomology and Noncommutative Geometry, Fields Institute Communications, Vol. 17, AMS (1997), 55-58. 

This is also the structure used in 

* J.L. Castiglioni G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0306289v2))

where aspects of its relation to the [[model structure on cosimplicial rings]] is discussed. (See [[monoidal Dold-Kan correspondence]] for
more on this).

[[!redirects model structure on dg-rings]]