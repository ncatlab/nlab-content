
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

The term _topological conformal field theory_ (TCFT) is used for a  linearization or [[stabilization]] of something that is like a [[conformal field theory]] (CFT) up to [[homotopy]]. It is a notion somewhere half-way between a (2-dimensional) [[TQFT]] and a [[CFT]]. 

> (Actually, the remnant of conformal structure here should be just 
> an artefact of  the way to parameterize the moduli space of surfaces. 
> As the classification result by Lurie discussed below shows, 
> TCFTs are really $(\infty,2)$-TFTs.)

This formalizes the physics notion of "the [[topological string]]", a _topologically twisted_ superconformal field theory, such as, notably, the [[A-model]] and the [[B-model]]. TCFTs are therefore a tool for formalizing [[homological mirror symmetry]]. 

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

This means in particular that when two [[Riemann surface]]s $\Sigma_1$ and $\Sigma_2$ are homologous as chains in the [[moduli space]] of Riemann surfaces, then the TCFT will send them to two equivalent morphisms $f_{\Sigma_1}$ and $f_{\Sigma_2}$ of chain complexes between the in- and the output states. The equivalence between $f_{\Sigma_1}$ and $f_{\Sigma_2}$, however, is not unique neither up to equivalence. Rather, it funtorially depends on the 1-chain realizing the homology equivalence between $\Sigma_1$ and $\Sigma_2$ as 0-chains in the moduli space. In particular, two non-homologous 1-chains between $\Sigma_1$ and $\Sigma_2$ will in general lead 
to non-equivalent equivalences between $f_{\Sigma_1}$ and $f_{\Sigma_2}$.

## Definition

According to [[On the Classification of Topological Field Theories|ClassTFT]]
the original definition of the domain for TCFTs can be formulated as follows (without reference to any conformal or Riemann structure). 

**Definition**
The $(\infty,2)$-category $Bord^{nc}_2$ of non-compact 2-dimensional cobordism is defined as follows:

* The objects of $Bord^{nc}_2$ are oriented 0-manifolds.

* Given a pair of objects $X, Y \in Bord^{nc}_2$ , a 1-morphism from $X$ to $Y$ is an oriented bordism $B : X \to Y$.

* Given a pair of 1-morphsims $B,B' : X \to Y$ in $Bord^{nc}_2$, a 2-morphism from $B$ to $B'$ in $Bord^{nc}_2$ is
an oriented bordism $\Sigma: B \to B'$ (which is trivial along $X$ and $Y$) with the following property: every
connected component of $\Sigma$ has nonempty intersection with $B'$.

* Higher morphisms in $Bord^{nc}_2$ are given by (orientation preserving) diffeomorphisms, isotopies between
diffeomorphisms, and so forth.

Then, the [[cobordism hypothesis]]-theorem for $Bord^{nc}_2$ becomes

+-- {: .num_theorem}
###### Theorem

Let $C$ be a [[symmetric monoidal (∞,2)-category]]. Then 
symmetric monoidal [[(∞,2)-functor]]s

$$
  Z : Bord^{nc}_2 \to C
$$

are equivalent to [[Calabi-Yau objects]] $A$ in $C$:
the functor $Z$ sends the point to $A$.

=--

This is [[On the Classification of Topological Field Theories|ClassTFT, theorem 4.2.11]]. One can "unfold" $Bord^{nc}_2$ and the theorem above, obtaining a statement in terms of [[symmetric monoidal (∞,1)-category|symmetric monoidal (∞,1)-categories]]. Actually it was the unfolded version to be proven first, ([Costello 04](#Costello04)). 

in the particular case $C=Ch_\bullet$. We state it below in the general version given by [[Jacob Lurie]] in [[On the Classification of Topological Field Theories|ClassTFT]].

+-- {: .num_defn}
###### Definition

Let $\mathcal{OC}$ be the [[(infinity,1)-category]] of open-closed strings, described as follows:

1. objects are oriented 1-manifolds with boundary;

1. morphisms are oriented bordisms between 1-manifolds such that each
   connected component has non-vanishing intersection with the codomain
   1-manifold;

1. the higher morphisms are given by orientation preserving
   [[diffeomorphism]]s, isotopies between these, and so forth.

Write $\mathcal{O}$ for the full [[sub-(∞,1)-category]] on 
disjoint unions of intervals (open strings sector).

=--

This is [[On the Classification of Topological Field Theories|ClassTFT, above theorem 4.2.13]].


## Classification
 {#Classification}

### With coefficients in (algebras in) chain complexes

The original statement of the classification result for TCFTs 
concerned symmetric homotopy-monoidal functors $Bord_2^{conf,dg} \to Ch_\bullet$:

+-- {: .num_defn}
###### Definition
([[Kevin Costello|Costello]], following [[Maxim Kontsevich|Kontsevich]])

1. The category of open TCFTs with set $\Lambda$ of D-branes is equivalent to that of [[Calabi-Yau categories]] with set $\Lambda$ of objects.

1. The homology of the chain complex of closed states of the universal extension of an open TCFT to an open-closed TCFT is the [[Hochschild homology]] of the corresponding [[Calabi-Yau category]].

=--


In ([Costello 04](#Costello04)) this is proven using information about cell decompositions of the moduli space of punctured Riemann surfaces, thus effectively presenting $Bord_2^{conf,dg}$ by generators-and-relations, The then theorem amounts to noticing that representations of these generators and relations define the operations in an $A_\infty$-category with pairing operation.


### General version


+-- {: .num_theorem}
###### Theorem

Let $C$ be a [[symmetric monoidal (∞,1)-category]]. Then 
symmetric monoidal [[(∞,1)-functor]]s

$$
  Z : \mathcal{O} \to C
$$


are equivalent to [[Calabi-Yau algebra]] [[Calabi-Yau object|objects]] $A$ in $C$:
the functor $Z$ sends the interval $[0,1]$ to $A$.

=--

This is the result of spring [Cos04](http://arxiv.org/abs/math/0412149)
reformulated and generalized according to 
[[On the Classification of Topological Field Theories|ClassTFT, theorem 4.2.14]].

This is a special case of the general [[cobordism hypothesis]]-theorem.


The idea of the proof is that a topological open string theory, i.e., a symmetric monoidal [[(∞,1)-functor]] $Z : \mathcal{O} \to C$ has a [[Kan extension]] to an open-closed topological string theory, i.e., to a symmetric monoidal [[(∞,1)-functor]] $Z : \mathcal{OC} \to C$, which is the unfolded version of a symmetric monoidal [[(∞,2)-functor]] from $Bord^{nc}_2$ to a symmetric monoidal $(\infty,2)$-category $C'$.

## Worldsheet and effective background theories 
 {#ActionFunctionals}

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

So this constructs a 2d TCFT and shows that its [[effective field theory|effective]] background quantum field theory is a [[Chern-Simons theory]]. While the action functionl on the worldsheet itself, whose [[path integral]] should give the [[differential forms]] on [[moduli space]] considered above, is not explicitly considered here, this does formalizes at least some aspects of an observation that was earlier made in ([Witten 92](#Witten92)) where it was observed that Chern-Simons theory is the effective background string theory of 2d TFTs obtained from action functionals of the A-model and the B-model.

Similarly the effective background QFT of the [[B-model]] topological string can be identified. This is known as _[[Kodeira-Spencer gravity]]_ or as _[[BCOV theory]]_.

(See also at _[[world sheets for world sheets]]_ for a similar mechanism and see at _[[super 1-brane in 3d]]_ for related "physical" strings.)

So via the detour over the effective background field theory, this sort of shows that the physicist's A-model and B-model are indeed captured by the abstract [[FQFT]] definition of TCFT as given above.

## Related concepts

* [[A-model]], [[B-model]], [[Landau-Ginzburg model]], [[homological mirror symmetry]]

* [[HCFT]]

## References

The concept is essentially a formalization of what used to be called [[cohomological field theory]] in

* {#Witten91} [[Edward Witten]], _Introduction to cohomological field theory_, InternationalJournal of Modern Physics A, Vol. 6,No 6 (1991) 2775-2792 ([[WittenCQFT.pdf:file]])


The definition was given independently by 

* {#Getzler92} [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159(2), 265&#8211;285 (1994) ([arXiv:hep-th/9212043](http://arxiv.org/abs/hep-th/9212043))

and 

* [[Graeme Segal]], _Topological field theory_ , (1999), Notes of lectures at Stanford university. ([web](http://www.cgtp.duke.edu/ITP99/segal/)). See in particular [lecture 5](http://www.cgtp.duke.edu/ITP99/segal/stanford/lect5.pdf) ("topological field theory with cochain values").
 
The classification of TCFTs by [[Calabi-Yau categories]] was discussed in

* {#Costello04} [[Kevin Costello]], _Topological conformal field theories and Calabi-Yau categories_, Advances in Mathematics, Volume 210, Issue 1, (2007), ([arXiv:math/0412149](http://arxiv.org/abs/math/0412149))

* [[Kevin Costello]], _The Gromov-Witten potential associated to a TCFT_ ([arXiv:math/0509264](http://arxiv.org/abs/math/0509264))

following conjectures by [[Maxim Kontsevich]], e.g.

* [[Maxim Kontsevich]], _Homological algebra of mirror symmetry_ , in Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&#252;rich, 1994), pages 120&#8211;139, Basel, 1995, Birkh&#228;user.

This classification is a precursor of the full [[cobordism hypothesis]]-theorem. This, and the reformulation of the original TCFT constructions in full generality is in 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_



Here are notes from a seminar on these definitions and results:

* [[Peter Teichner]] and [[Kevin Costello]] _TCFT seminar_ ([pdf notes](http://math.berkeley.edu/~cpries/Hot-Topics-07.pdf))

Discussion of the construction of TCFTs from differential forms on moduli space and the way this induces by "[[second quantization]]" effective background Chern-Simons theories is in

* {#Costello06} [[Kevin Costello]], _Topological conformal field theories and gauge theories_ ([arXiv:math/0605647](http://arxiv.org/abs/math/0605647))
 

formalizing at least aspects of the observations in

* {#Witten92} [[Edward Witten]], _Chern-Simons Gauge Theory As A String Theory_ ([arXiv:hep-th/9207094](http://arxiv.org/abs/hep-th/9207094))
 

* P.A. Grassi, [[Giuseppe Policastro]], _Super-Chern-Simons Theory as Superstring Theory_ ([arXiv:hep-th/0412272](http://arxiv.org/abs/hep-th/0412272))

Discussion of how the [[second quantization]] of the [[B-model]] yields [[Kodeira-Spencer gravity]]/[[BCOV theory]] is in 

* {#BCOV93} M. Bershadsky, S. Cecotti, [[Hirosi Ooguri]], [[Cumrun Vafa]], _Kodaira-Spencer Theory of Gravity and Exact Results for Quantum String Amplitudes_, Commun.Math.Phys.165:311-428,1994 ([arXiv:hep-th/9309140](http://arxiv.org/abs/hep-th/9309140))
 

* [[Kevin Costello]], [[Si Li]], _Quantum BCOV theory on Calabi-Yau manifolds and the higher genus B-model_ ([arXiv:1201.4501](http://arxiv.org/abs/1201.4501))

* [[Si Li]], _BCOV theory on the elliptic curve and higher genus mirror symmetry_ ([arXiv:1112.4063](http://arxiv.org/abs/1112.4063))

* [[Si Li]], _Variation of Hodge structures, Frobenius manifolds and Gauge theory_ ([arXiv:1303.2782](http://arxiv.org/abs/1303.2782))

[[!redirects TCFTs]]


[[!redirects topological conformal field theory]]
[[!redirects topological conformal field theories]]

