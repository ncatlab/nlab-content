
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

**Theorem** (Costello, following Kontsevich)

1. The categroy of open TCFTs with set $\Lambda$ of D-branes is equivalent to that of [[Calabi-Yau categories]] with set $\Lambda$ of objects.

1. The homology of the chain complex of closed states of the universal extension of an open TCFT to an open-closed TCFT is the [[]Hochschild homology]] of the corresponding [[Calabi-Yau category]].

## References

The definition was given independently by 

* [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159(2), 265&#8211;285 (1994) ([arXiv:hep-th/9212043](http://arxiv.org/abs/hep-th/9212043))

and 

* G. Segal, _Topological field theory_ , (1999), Notes of lectures at Stanford university. ([web](http://www.cgtp.duke.edu/ITP99/segal/)).
 
The classification of TCFTs by [[Calabi-Yau categories]] was discussed in

* [[Kevin Costello]], 

  * _Topological conformal field theories and Calabi-Yau categories_ ([arXiv:math/0412149](http://arxiv.org/abs/math/0412149))

  * _The Gromov-Witten potential associated to a TCFT_ ([arXiv:math/0509264](http://arxiv.org/abs/math/0509264))

following conjectures by [[Maxim Kontsevich]], e.g.

* [[Maxim Kontsevich]], _Homological algebra of mirror symmetry_ , in Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&#168;urich, 1994), pages 120&#8211;139, Basel, 1995, Birkh&#228;user.

This classification is a precursor of the full [[cobordism hypothesis]]-theorem.

[[!redirects topological conformal field theory]]
[[!redirects topological conformal field theories]]