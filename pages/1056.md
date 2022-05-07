
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

By regarding a [[simplicial set]] as an [[object]] in the standard [[model structure on simplicial sets]], one effectively identifies it (up to weak equivalence) with that [[∞-groupoid]] that it presents under [[Kan fibrant replacement]].

If the original simplicial set is the [[nerve]] of a [[category]], the corresponding Kan fibrant replacement is something like the _$\infty$-groupoidification_ of that category: see [[geometric realization of categories]].

This way each ordinary category models an [[∞-groupoid]]. The _Thomason_ [[model category]] structure on [[Cat]] exhibits this: in this [[model category]] a morphism between two categories is a weak equivalence, precisely if it induces a weak equivalence of the corresponding $\infty$-groupoids.  

It turns out the Thomason model structure on [[Cat]] is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on simplicial sets]].

This is remarkable, in that it says that every [[homotopy n-type|homotopy type]], i. e. every weak equivalence class of $\infty$-groupoids, is obtained by $\infty$-groupoidifying just categories.

In fact, every cofibrant object in this structure is a [[poset]]. Since every object in a model category is weakly equivalent to a cofibrant one, this means that even the [[nerve]]s of just posets are sufficient to model all homotopy types.


This is a rather curious aspect of the [[Robert Thomason|Thomason]] model on [[Cat]]: it does not really have anything intrinsically to do with [[category|categories]], but rather uses these as a way to present [[∞-groupoid]]s. In particular, the class of weak equivalences is much larger than just the [[equivalence of categories|equivalences of categories]]. 
There is a _different_ model structure on [[Cat]] in which the weak equivalences are precisely the "true" weak [[equivalence of categories|equivalences of categories]] (not of anything constructed from them). This is called the [[canonical model structure on Cat]].

## Definition

Recall the [[subdivision]] functor $Sd$ and its right adjoint $Ex$.
The Thomason model structure on $Cat$ is given by

* A functor is a Thomason cofibration iff it has the left lifting property
against the Thomason trivial fibrations
* A functor $f : C \to D$ is a Thomason weak equivalence iff $N(f)$ is a weak homotopy equivalence
* A functor $f : C \to D$ is a Thomason fibration iff $Ex^2 N(f)$ is a Kan fibration

## Properties

+-- {: .num_prop}
###### Proposition 
$Cat$ is a proper model category.
=--
This is corollary 5.5 of [Thomason](#Thomason).

### Equivalence with the classical model structure on simplicial sets

The Thomason model structure on Cat is [[Quillen equivalent]] to the [[classical model structure on simplicial sets]] by the adjunction

$$ h Sd^2 : sSet \rightleftarrows Cat : Ex^2 N $$

We can assert more: this is also an adjoint weak equivalence. These are relative functors between the [[relative categories]] $(sSet, Kan)$ and $(Cat, Thomason)$, and both the adjunction unit and counit are natural weak equivalences.

### Relation to ∞Gpd

The localization $L : Cat \to \infty Gpd$ sending a category to its homotopy type has a direct interpretation in terms of ∞-category theory:

+-- {: .num_prop}
###### Proposition 
$L$ is the ∞-groupoidification functor functor $C \mapsto C[C^{-1}]$.
=--

### Homotopy colimits

Let $f : C \to Cat$ be a functor. Its homotopy colimit in the Thomason model
structure can be computed using the [[Grothendieck construction]]:


### The nerve is a homotopy colimit of simplicial sets

By [Hirschhorn proposition 18.1.6](#Hir), the nerve of any category is the homotopy colimit of the constant point-valued diagram:

+-- {: .num_prop}
###### Proposition 
For any category $C$, $N(C) \simeq hocolim_{c \in C} \Delta^0$
=--

In fact, when Hirschhorn's definition of the homotopy colimit for functors valued in simplicial model categories:
$$
  hocolim(f) = N(- \downarrow C)^{op} \otimes_{C} f
$$
we get an isomorphism $N(C)^{op} \cong hocolim(1)$.




## Related concepts

* [[basic localizer]]

* [[Dwyer map]]

* [[homotopy hypothesis]]

* [[model structure on simplicial sets]], [[model structure on topological spaces]]

* [[Strøm model structure]]


## References

The original reference is

*  {#Thomason} [[Robert Thomason|R. W. Thomason]], _Cat as a closed model category_, Cahiers Topologie G&#233;om. Diff&#233;rentielle **21**, no. 3 (1980), pp. 305--324. MR0591388 (82b:18005) ([numdam:CTGDC_1980__21_3_305_0](http://www.numdam.org/item/?id=CTGDC_1980__21_3_305_0))

A correction to this article was made in

* [[Denis-Charles Cisinski]], _Les morphisme de Dwyer ne sont pas stables par r&eacute;tractes_, Cahiers Topologie et G&eacute;om. Diff&eacute;rentielle Cat&eacute;goriques, **40** no. 3 (1999), pp. 227--231. ([Numdam](http://www.numdam.org/item?id=CTGDC_1999__40_3_227_0))

There it was clarified that every cofibrant object in the Thomason model structure is a [[poset]] (although this is already explicitly mentioned in Thomason's paper -- see the beginning of section 5). 

A useful review of the Thomason model structure and a generalization of the model structure to [[n-fold category|n-fold categories]] is given in 

* Thomas M. Fiore, [[Simona Paoli]], _A Thomason model structure on the category of small n-fold categories_ ([arXiv](http://arxiv.org/abs/0808.4108))

The following article gives a large class of categories which are [[fibrant]] in the Thomason model structure.

* [[Lennart Meier]], [[Viktoriya Ozornova]], _Fibrancy of partial model categories_,  Homology, Homotopy and Applications, Volume 17 (2015) Number 2.  ([arXiv:1408.2743](https://arxiv.org/abs/1408.2743), [doi:10.4310/HHA.2015.v17.n2.a5](http://dx.doi.org/10.4310/HHA.2015.v17.n2.a5))

* [[Lennart Meier]], _Fibrancy of (Relative) Categories_, talk at _Young Topologists Meeting 2014_ ([slides pdf](http://www.staff.science.uu.nl/~meier007/Kopenhagen2014.pdf))

Some posets that are cofibrant in the Thomason model structure are studied in

* Roman Bruckner, Christoph Pegel, _Cofibrant objects in the Thomason Model Structure_, [arXiv](http://arxiv.org/abs/1603.05448)

The analog of the Thomason model structure for the _stable_ case -- an equivalence between connective [[stable homotopy theory]] and [[nerve]]s of [[symmetric monoidal categories]] -- is discussed in 

* [[Robert Thomason]], _Symmetric monoidal categories model all connective spectra_, Theory and Applications of Categories, Vol. 1, No. 5, (1995) pp. 78-118

Some other references

* {#Hir} Hirschhorn _Model categories and their localizations_.

[[!redirects Thomason weak equivalence]]
[[!redirects Thomason weak equivalences]]