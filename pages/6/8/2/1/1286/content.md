
#Contents#
* automatic table of contents
{:toc}

## Idea 

A _derived stack_ $X$ is an [[∞-stack]] -- an [[(∞,1)-sheaf]] -- whose domain is not a [[1-category]] but more generally an [[(∞,1)-category]] $C$.

$$
  X \in Sh_{(\infty,1)}(C)
  \,.
$$

One says _derived stack_ in order to distinguish from the more restrictive notion of an [[∞-stack]] on a 1-categorical [[site]], such as for instance described at [[topological ∞-groupoid]].

For recall that a [[sheaf]] is a [[functor]] $F : C^{op} \to Set$ satisfying some [[descent]]-condition.
So there are two steps in which the notion of [[sheaf]] may be [[vertical categorification|categorified]]:

1. the codomain is categorified and the domain remains a 1-category
1. the codomain and the domain are categorified.

The categorification of the codomain leads to the notion of [[stack]]s when [[Set]] replaced by [[Grpd]], and further to [[∞-stack]]s, when sets are replaced by [[∞-groupoid]]s. 

But there is no natural reason why the domain should in general remain a 1-category if one passes to an [[infinity-category|∞-categorical]]-context. A _derived stack_ is a generalization of the notion of sheaf where both domain and codomain are taken to be $\infty$-categorical.

Following the general logic of [[models for ∞-stack (∞,1)-toposes]], derived stacks are typically [[model category|modeled]] by the [[model structure on SSet-enriched presheaves]] on an [[SSet-site]] or [[model site]] $C$. In such a model a derived stack is represented by an  [[SSet]]-[[enriched functor]]
$F : C^{op} \to SSet$ from an [[SSet]]-[[enriched category]] $C$ to [[SSet]] that satisfies a [[descent]] condition.

## Central motivation: derived stacks have good limits

One general idea for the use of higher and derived stacks is that

* passing to a higher categorical codomain  -- i.e. from Set-values [[sheaf|sheaves]] to higher [[groupoid]] valued sheaves -- is a means to obtain _good colimits_, [[colimit]]s that do not lose information. For instance 

  * in the category [[Diff]] of manifolds the quotient by a non-free action of a group may not exist

  * in [[sheaf|sheaves]] in $[Diff^{op},Set]$ it will exist, but will have the wrong properties in general with respect to some operations such as taking cohommology,

  * while finally in [[stack]]s $[Diff^{op}, Grpd]$ it exists as the corresponding smooth [[action groupoid]] or [[orbifold]] and in this form rembers in terms of the isomorphisms how the quotient was obtained. The cohomology of the stack is then indeed the equivariant cohomology of the original manifold.

* similarly passing to higher categorical domain -- i.e. from presheaves on categories to presheaves on higher categories, is analogously a means to ensure that good [[limit]]s exist.

A detailed illustration and motivation of the need of these "good limits" that don't forget the way they were formed is 

* in the introductory section of 

  * [[Jacob Lurie]], _[[Structured Spaces]]_

* in the introductory section of 

  * David Spivak, _[Quasi-smooth derived manifolds](http://math.berkeley.edu/~dspivak/thesis2.pdf)_


## Examples


* A derived refinement of the ordinary [[site]] [[CRing]]${}^{op}$ of formal duals to commutative tings is the [[SSet-site]] $SCRing^{op}$ of [[simplicial ring]]s. Derived stacks on this site are studied in [[derived algebraic geometry]].

  An introduction to this is for instance in 
  [chapter 5](http://www.crm.cat/HigherCategories/hc1.pdf#page=135) of the lecture notes

  * [[Bertrand Toen]], _Simplicial presheaves and derived algebraic geometry_ course on [Simplicial Methods in Higher Categories](http://www.crm.cat/HigherCategories/) ([pdf](http://www.crm.cat/HigherCategories/hc1.pdf#page=99))

  There are various slight variations of this. For instance using the [[monoidal Dold-Kan correspondence]], simplicial rings may be replaced with non-positively graded cochain [[dg-algebra]]s.

  One application of derived stacks on $(dgAlg^-)^{op}$ is the [[BV-BRST formalism]] in [[physics]].

* A derived refinement of the ordinary [[site]] $\mathbb{L}$ of [[smooth loci]] is the [[SSet-site]] $cs \mathbb{L}$ of [[cosimplicial object|cosimplicial]] [[smooth loci]]. Derived stacks on this are the objects in a theory that could be called [[derived synthetic differential geometry]].

## Remarks

### Derived Yoneda embedding

One obvious but notable phenomenon that occurs in derived stacks in general, but not in [[∞-stack]]s over a 1-categorical site, is that under the [[Yoneda lemma for (∞,1)-categories|Yoneda embedding for (∞,1)-categories]] a categorically discrete object, i,e. a [[n-truncated object in an (∞,1)-category|0-truncated object]] may be mapped to a higher categorical object.

Consider specifically an ordinary [[site]] $C$ and let $csC = [\Delta,C]$ be the corresponding [[SSet-site]] of [[cosimplicial object]]s. Write

$$
  \mathbf{Y} : C \hookrightarrow [\Delta,C] \stackrel{\mathbb{R}Y}{\to}
  [[Delta,C],SSet]
$$ 

for the composite that first regards objects of $C$ as constant cosimplicial objects and then applies the [[derived functor]] of the [[enriched category theory|enriched]] [[Yoneda embedding]], i.e. the functor 

$$
  \mathbb{R}Y = Y(Q(-), P(-))
$$

for $Q$ a fibrant and $P$ a cofibrant replacement functor. Then of course the simplicial presheaf $\mathbf{Y}(U)$ for $U \in C$ may in general take values in [[simplicial set]]s with nontrivial higher [[simplicial homotopy group]]s, to the extent that the [[SSet]]-[[hom-object]]s $\mathbf{Y}(U) : V \mapsto [\Delta,C](V,U)$ in $[\Delta,C]$ are nontrivial. 

This cannot happen for [[∞-stack]]s over 1-categorical site. For instance a [[topological space]] regarded as a [[topological ∞-groupoid]] is always an [[n-truncated object of an (∞,1)-category|0-truncated object]] as an [[∞-stack]].

A notable example of this is the case where $C = $ [[CRing]] and $U = Spec R$. While ordinarily this is 0-categorical, when regarded as a derived stack on formal duals of [[simplicial ring]]s this has in general a nontrivial [[free loop space object]], i.e. a nontrivial [[homotopy pullback]] of the form

$$
  \array{
    \Spec \Omega^\bullet_K(R) &\to& Spec R
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    Spec R &\stackrel{(Id,Id)}{\to}& Spec R \times Spec R
  }
  \,,
$$

where, as indicated, the free loop space object is something like the [[de Rham space]] of $Spec R$. This means that regarded as a derived stack, the space $Spec R$ becomes an [[∞-groupoid]] whose morphisms are given by [[infinitesimal object|infinitesimal paths]] in the orighinal space.

By the $\infty$-erspective on [[Hochschild cohomology]] (as discussed there) this implies a bunch of nice relations. Details are in

* [[Bertrand Toen]] [[Gabriele Vezzosi]], _$S^1$-Equivariant simplicial algebras and de Rham theory_ ([arXiv:0904.3256](http://arxiv.org/abs/0904.3256))
 
The fact is also mentioned and used in passing every now and then (e.g. p. 9) in 

* [[David Ben-Zvi]], [[David Nadler]], [[John Francis]], _[[geometric infinity-function theory|Integral transforms etc.]]_

But there must be a better reference, somewhere.

## References

An overview is provided in 

* [[Bertrand Toën]], _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504))

A set of lecture notes on the [[model structure on simplicial presheaves]] with an eye towrads algebraic sites and derived algebraic geometry is

* [[Bertrand Toën]], _Simplicial presheaves and derived algebraic geometry_ , lecture at [Simplicial methofs in higher categories](http://www.crm.es/HigherCategories/)  ([pdf](http://www.crm.cat/HigherCategories/hc1.pdf))


Details modeled on [[simplicially enriched category|simplicial categories]] have been developed in the series of articles by To&#235;n and Vezossi.

This article generalizes the notion of [[site]] and [[model structure on simplicial presheaves]] from 1-categorical sites to [[simplicially enriched category|simplicial sites]] and hence to a [[model structure on SSet-enriched presheaves]]:

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv](http://arxiv.org/abs/math.AG/0207028))

Of central interest in derived algebraic geometry is the simplicial site of _simplicial algebras_, which generalizes the familiar site of algebra used in algebraic geometry. This is introduced and studied in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications_ ([arXiv](http://arxiv.org/abs/math.AG/0404373))

Further developments in this direction are in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _From HAG to DAG: derived moduli stacks_ in Axiomatic, enriched
and motivic homotopy theory, 173&#8211;216, NATO Sci. Ser. II Math. Phys. Chem., 131, Kluwer
Acad. Publ., Dordrecht, 2004. ([arXiv](http://arxiv.org/abs/math.AG/0210407))


The unifying picture, in particular independent of the choice of model for the [[(infinity,1)-category|(infinity,1)-categories]] is presented in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Derived ($\infty$-)stacks are currently mostly, maybe exclusively, studied on algebraic sites $S$, where the category $S^{op} := $ [[Alg]] is replaced with a category of "$\infty$-algebras" of sorts. The theory of these $\infty$-algebras is described in great detail in


* [[Jacob Lurie]], _[[higher algebra|Noncommutative and Commutative algebra]]_

Concretely the need for the site of simplicial ring objects is discussed in the introduction of 

* [[Jacob Lurie]], _[[Structured Spaces]]_

and in the introduction of

* [[David Spivak]], _[Quasi-smooth derived manifolds](http://math.berkeley.edu/~dspivak/thesis2.pdf)_ .


The proof that [[simplicial object|simplicial]] [[algebra]]s are Quillen equivalent of [[differential graded algebra]]s -- so that derived stacks on simplicial algebras are the same as derived stacks on DGAs -- is in

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342)) .


[[!redirects derived stacks]]
[[!redirects derived infinity-stack]]
[[!redirects derived infinity-stacks]]
[[!redirects derived ∞-stack]]
[[!redirects derived ∞-stacks]]
