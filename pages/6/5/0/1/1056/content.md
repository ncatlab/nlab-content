
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
* table of contents
{:toc}

## Idea

By regarding a [[simplicial set]] as an [[object]] in the [[classical model structure on simplicial sets]], one effectively identifies it (up to [[simplicial weak homotopy equivalence|weak equivalence]]) with the [[∞-groupoid]] that it presents under [[Kan fibrant replacement]].
If the original simplicial set is the [[nerve]] of a [[category]], then the corresponding Kan fibrant replacement is something like the _$\infty$-groupoidification_ of that category: see *[[geometric realization of categories]]*.

This way each ordinary category models an [[∞-groupoid]]. The _Thomason_ [[model category]] structure on [[Cat]] exhibits this: in this [[model category]] a morphism between two categories is a [[weak equivalence]] precisely if it induces a weak equivalence of the corresponding $\infty$-groupoids.  

It turns out the Thomason model structure on [[Cat]] is [[Quillen equivalence|Quillen equivalent]] to the [[classical model structure on simplicial sets]].

This is remarkable, in that it says that every [[homotopy type]], i. e. every [[equivalence in an (infinity,1)-category|equivalence]] class of [[infinity-groupoid|$\infty$-groupoids]], is obtained by $\infty$-groupoidifying just categories.

In fact, every [[cofibrant object]] in the Thomason model structure structure is a [[poset]]. Since every object in a model category is weakly equivalent to a cofibrant one, this means that even the [[nerves]] of just [[posets]] are sufficient to model all [[homotopy types]].


This is a rather curious aspect of the [[Robert Thomason|Thomason]] model on [[Cat]]: it does not really have anything intrinsically to do with [[category|categories]], but rather uses these as a way to present [[∞-groupoids]]. In particular, the class of [[weak equivalences]] is much larger than just the [[equivalence of categories|equivalences of categories]]. 
There is a _different_ model structure on [[Cat]] in which the weak equivalences are precisely the "true" weak [[equivalence of categories|equivalences of categories]] (not of anything constructed from them). This is called the *[[canonical model structure on Cat]]*.

## Definition
 {#Definition}

Recall the [[subdivision]] functor $Sd$ and its [[right adjoint]] [Ex-functor](Kan+fibrant+replacement#ExFunctor).

\begin{definition}
\label{ThomasonModelStructure}
Let $C$ and $D$ be [[small categories]]. A functor $f \colon C \to D$ is called :

* a *Thomason fibration* iff $Ex^2 N(f)$ is a Kan fibration,

* *Thomason weak equivalence* iff its [[nerve]] $N(f)$ is a [[weak homotopy equivalence]],

* *Thomason-cofibration* iff it has the [[left lifting property]] against the morphisms that are both Thomason-fibrations as well as Thomason-equivalences.

\end{definition}
\begin{proposition}
Equipped with these classes of morphisms, the [[1-category]] of [[small categories]] is a [[proper model category|proper]] [[model category]].
\end{proposition}
This is [Thomason (1980), corollary 5.5](#Thomason1980).

## Properties

### (Co)Fibrant objects

\begin{proposition}
\label{EveryThomasocCofibrantCategoryIsAPoset}
 Every [[cofibrant object]] in the Thomas model structure (Def. \ref{ThomasonModelStructure}) is a [[poset]] ([regarded](partial+order#AsACategoryWithExtraProperties) as a [[small category]]).
\end{proposition}
This is [Thomason (1980), proposition 5.7](#Thomason1980).

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

Let $f : C \to Cat$ be a functor. Its [[homotopy colimit]] in the Thomason model
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

The original reference:

*  {#Thomason1980} [[Robert W. Thomason]], *Cat as a closed model category*, Cahiers Topologie G&#233;om. Diff&#233;rentielle **21** 3 (1980) 305-324  &lbrack;[numdam:CTGDC_1980__21_3_305_0](http://www.numdam.org/item/?id=CTGDC_1980__21_3_305_0), MR0591388 (82b:18005)&rbrack;

A correction to this article was made in

* [[Denis-Charles Cisinski]], _La classe des morphismes de Dwyer n'est pas stable par r&eacute;tractes_, Cahiers Topologie et G&eacute;om. Diff&eacute;rentielle Cat&eacute;goriques, **40** no. 3 (1999), pp. 227--231. ([Numdam](http://www.numdam.org/item?id=CTGDC_1999__40_3_227_0))


Review and generalization to [[n-fold category|$n$-fold categories]]:

* [[Thomas M. Fiore]], [[Simona Paoli]], *A Thomason model structure on the category of small $n$-fold categories*, Algebr. Geom. Topol. **10** 4 (2010) 1933-2008 &lbrack;[arXiv:0808.4108](http://arxiv.org/abs/0808.4108), [doi:10.2140/agt.2010.10.1933](https://projecteuclid.org/journals/algebraic-and-geometric-topology/volume-10/issue-4/A-Thomason-model-structure-on-the-category-of-small-nfold/10.2140/agt.2010.10.1933.full)&rbrack;

Restriction of the Thomason model structure to the category of just [[posets]]:

* [[George Raptis]], *Homotopy theory of posets*, Homology Homotopy Appl. **12** 2 (2010) 211-230 &lbrack;[euclid:hha/1296223882](https://projecteuclid.org/journals/homology-homotopy-and-applications/volume-12/issue-2/Homotopy-theory-of-posets/hha/1296223882.full)&rbrack;
 
and to the category of just (small) acyclic categories:

* [[Roman Bruckner]], *A Model Structure On The Category Of Small Acyclic Categories* &lbrack;[arXiv:1508.00992](https://arxiv.org/abs/1508.00992)&rbrack;



Discussion of [[fibrant objects]] in the Thomason model structure:

* [[Lennart Meier]], [[Viktoriya Ozornova]], _Fibrancy of partial model categories_,  Homology, Homotopy and Applications, Volume 17 (2015) Number 2.  ([arXiv:1408.2743](https://arxiv.org/abs/1408.2743), [doi:10.4310/HHA.2015.v17.n2.a5](http://dx.doi.org/10.4310/HHA.2015.v17.n2.a5))

* [[Lennart Meier]], _Fibrancy of (Relative) Categories_, talk at _Young Topologists Meeting 2014_ ([slides pdf](http://www.staff.science.uu.nl/~meier007/Kopenhagen2014.pdf))

Discussion of [[cofibrant objects]] (Thomason-cofibrant posets):

* [[Roman Bruckner]], [[Christoph Pegel]], _Cofibrant objects in the Thomason Model Structure_, &lbrack;[arXiv:1603.05448](http://arxiv.org/abs/1603.05448)&rbrack;

* [[Roman Bruckner]], *Abstract Homotopy Theory and the Thomason Model Structure*, PhD thesis, Bremen 2016 &lbrack;[gbv:46-00105527-15](http://nbn-resolving.de/urn:nbn:de:gbv:46-00105527-15), [pdf](https://media.suub.uni-bremen.de/bitstream/elib/1120/1/00105527-1.pdf)&rbrack;

On the analog of the Thomason model structure for the _stable_ case -- an equivalence between connective [[stable homotopy theory]] and [[nerves]] of [[symmetric monoidal categories]]:

* [[Robert W. Thomason]], _Symmetric monoidal categories model all connective spectra_, Theory and Applications of Categories **1** 5 (1995) 78-118

Some other references

* {#Hir} [[Philip Hirschhorn]], _[[Model Categories and Their Localizations]]_, AMS Math. Survey and Monographs **99** (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/pshmain.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;


[[!redirects Thomason weak equivalence]]
[[!redirects Thomason weak equivalences]]