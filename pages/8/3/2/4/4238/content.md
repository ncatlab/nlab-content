
<div class="rightHandSide toc">
[[!include functorial quantum field theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The term _topological conformal field theory_ (TCFT) is used for a  linearization or [[stabilization]] of something that is like a [[conformal field theory]] (CFT) up to [[homotopy]]. It is a notion somewhere half-way between a (2-dimensional) [[TQFT]] and a [[CFT]]. This formalizes the physics notion of a _topologically twisted_ superconformal field theory, such as, notably, the [[A-model]] and the [[B-model]]. TCFTs are therefore a tool for formalizing [[homological mirror symmetry]]. 

Recall that an ordinary [[conformal field theory]] (CFT) is, in [[FQFT]]-language, a [[symmetric monoidal functor]] on a [[category]] $Bord_2^{conf}$ whose objects are disjoint unions of intervals and circles, and whose [[morphism]]s are [[Riemann surface]]s with these 1d manifolds as incoming and outgoing punctures.

Since Riemann surfaces form a well-understood [[moduli space]], one can turn this also into a [[Top]]-[[enriched category]], i.e. an [[(∞,1)-category]], 
$Bord_{2}^{conf,top}$ whose [[hom-space]]s are these [[moduli space]]s of [[Riemann surface]]s with given 1d manifolds as incoming and outgoing punctures.

A "truly topological conformal field theory" would be an [[(∞,1)-functor]] of the form

$$
  Bord_2^{conf,top} \to \infty Grpd
$$

or similar. But what is actually called a "topological conformal field theory" is the linearization or [[stabilization]] of this:

in a TCFT, this [[(∞,1)-category]] of conformal [[cobordism]]s is replaced by a [[stable (∞,1)-category]] whose [[hom-object]]s (when modeled by a [[dg-category]]) are just the [[homology]] [[chain complex]]s of the original [[hom-space]]s.


Write $Bord_2^{conf,dg}$ for the resulting [[symmetric monoidal category|symmetric monoidal]] [[dg-category]] of Riemann cobordisms. Then a TCFT is a an homotopy-symmetric monoidal [[chain complex]]-[[enriched functor]]

$$
  F : Bord_2^{conf,dg} \to Ch_\bullet
$$

to the symmetric monoidal [[dg-category]] of chain complexes.

This means in particular that when two [[Riemann surface]]s $\Sigma_1$ and $\Sigma_2$ are homologous as chains in the [[moduli space]] of Riemann surfaces, then the TCFT will send them to two equivalent morphisms $f_{\Sigma_1}$ and $f_{\Sigma_2}$ of chain complexes between the in- and the output states. The equivalence between $f_{\Sigma_1}$ and $f_{\Sigma_2}$, however, is not unique neither up to equivalence. Rather, it funtorially depends on the 1-chain realizing the homology equivalence between $\Sigma_1$ and $\Sigma_2$ as 0-chains in the moduli space. In particular, two non-homologous 1-chains between $\Sigma_1$ and $\Sigma_2$ will in general lead to non-equivalent equivalences between $f_{\Sigma_1}$ and $f_{\Sigma_2}$.

## Classification

+-- {: .un_defn}
###### Definition
([[Kevin Costello|Costello]], following [[Maxim Kontsevich|Kontsevich]])

1. The category of open TCFTs with set $\Lambda$ of D-branes is equivalent to that of [[Calabi-Yau categories]] with set $\Lambda$ of objects.

1. The homology of the chain complex of closed states of the universal extension of an open TCFT to an open-closed TCFT is the [[Hochschild homology]] of the corresponding [[Calabi-Yau category]].

=--

+-- {: .proof}
###### Proof

In [Cos04](http://arxiv.org/abs/math/0412149) this is proven using information about cell decompositions of the moduli space of punctured Riemann surfaces, thus effectively presenting $Bord_2^{conf,dg}$ by generators-and-relations, The then theorem amounts to noticing that representations of these generators and relations define the operations in an $A_\infty$-category with pairing operation.

=--


## Worldsheet and effective background theories {#ActionFunctionals}

One imagines generally that one obtains TCFTs, in their formal definition given above, from worldsheet [[action functional]]s as familiar from the physics literature (such as on the [[A-model]] and the [[B-model]]) by performing the [[path integral]] and finding from it a collection of [[differential form]]s on [[moduli space]] of bosonic field configurations.

It seems there is at this point no literature giving a direct construction along these lines, but there is the following:

In [Cos06](http://arxiv.org/abs/math/0605647) is constructed from the geometric input datum of a generalized [[Calabi-Yau space]] $(X,Q)$ and it is shown that

1. there is a collection of differential forms $K_{g,h}(\cdots)$on the [[moduli space]] $\mathcal{M}_{g}^{h,n}$ of [[Riemann surface]]s such that these define a 2d TCFT;

   (In the discussion leading up to Lemma 4.5.1 there. The proof that this yields a TCFT is theorem 4.5.4.)

1. the partition function of the string perturbation series for the 
   above TCFT is

   $$
     \sum_{{g,n \geq 0, h \gt 0} \atop {2g-2+h+\frac{n}{2}}}
     \lambda^{2g-2+h}N^h
     \frac{1}{n!}
     \int_{\mathcal{M}_g^{h,n}}
     K_{g,h}(a^\otimes n)
   $$
   
   which is shown to be the partition function of a background 
   [[Chern-Simons theory]] coming from the [[action functional]]

   $$
     a \mapsto S(a) = \int_X \frac{1}{2} a Q a + \frac{1}{3}a^3
     \,.
   $$

So this construxts a 2d TCFT and shows that its effective background [[string theory]] is a [[Chern-Simons theory]]. While the action functionl on the worldsheet itself, whose [[path integral]] should give the differential forms on moduli space considered above, is not explicitly considered here, this does formalizes at least some aspects of an observation that was earlier made in [Wit1995](http://arxiv.org/abs/hep-th/9207094) where it was observed that Chern-Simons theory is the effective background string theory of 2d TFTs obtained from action functionals of the A-model and the B-model.

So via the detour over the effective background field theory, this sort of shows that the physicist's A-model and B-model are indeed captured by the abstract [[FQFT]] definition of TCFT as given above.

## References

The definition was given independently by 

* [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159(2), 265&#8211;285 (1994) ([arXiv:hep-th/9212043](http://arxiv.org/abs/hep-th/9212043))

and 

* G. Segal, _Topological field theory_ , (1999), Notes of lectures at Stanford university. ([web](http://www.cgtp.duke.edu/ITP99/segal/)). See in particular [lecture 5](http://www.cgtp.duke.edu/ITP99/segal/stanford/lect5.pdf).
 
The classification of TCFTs by [[Calabi-Yau categories]] was discussed in

* [[Kevin Costello]], 

  * _Topological conformal field theories and Calabi-Yau categories_ ([arXiv:math/0412149](http://arxiv.org/abs/math/0412149))

  * _The Gromov-Witten potential associated to a TCFT_ ([arXiv:math/0509264](http://arxiv.org/abs/math/0509264))

following conjectures by [[Maxim Kontsevich]], e.g.

* [[Maxim Kontsevich]], _Homological algebra of mirror symmetry_ , in Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&uuml;rich, 1994), pages 120&#8211;139, Basel, 1995, Birkh&#228;user.

This classification is a precursor of the full [[cobordism hypothesis]]-theorem.

Here are notes from a seminar on these definitions and results:

* [[Peter Teichner]] and [[Kevin Costello]] _TCFT seminar_ ([pdf notes](http://math.berkeley.edu/~cpries/Hot-Topics-07.pdf))

Discussion of the construction of TCFTs from differential forms on moduli space and the way this induces effective background Chern-Simons theories is in

* [[Kevin Costello]], _Topological conformal field theories and gauge theories_ ([arXiv](http://arxiv.org/abs/math/0605647))

formalizing at least aspects of the observations in

* [[Edward Witten]], _Chern-Simons Gauge Theory As A String Theory_ ([arXiv](http://arxiv.org/abs/hep-th/9207094))


[[!redirects topological conformal field theory]]
[[!redirects topological conformal field theories]]