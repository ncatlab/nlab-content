
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


##Idea

The notion of _abelian category_ is an abstraction of basic properties of the category [[Ab]] of [[abelian groups]], more generally of the category $R$[[Mod]] of [[modules]] over some [[ring]], and still more generally of categories of [[sheaves]] of abelian groups and of modules. It is such that much of the [[homological algebra]] of [[chain complexes]] can be developed inside every abelian category.

The concept of abelian categories is one in a sequence of notions of [[additive and abelian categories]].  

While additive categories differ significantly from [[toposes]], there is an intimate relation between abelian categories and toposes. See _[[AT category]]_ for more on that.

##Definition

Recall the following fact about [[pre-abelian categories]] from [this proposition](pre-abelian+category#DecompositionOfMorphisms), discussed there:

+-- {: .num_prop #DecompositionOfMorphisms}
###### Proposition

Every [[morphism]] $f \colon A\to B$ in a [[pre-abelian category]] has a canonical de-[[composition]]

\[
  \label{PreImageFactorization}
  A
  \overset{\; p \;}{\twoheadrightarrow}
  \coker\big(\ker f\big)
  \xrightarrow{\; \overline{f} \;}
  \ker\big(\coker f\big)
  \xhookrightarrow{\; i \;}  
  B
\]

where: 

* $p$ is a [[cokernel]], hence  an [[epimorphism]], 

* $i$ is a [[kernel]], hence a [[monomorphism]].

=--


+-- {: .num_defn #AbelianCategory}
###### Definition

An **abelian category** is a [[pre-abelian category]] satisfying the following equivalent conditions.

1. For every [[morphism]] $f$, the canonical morphism $\bar{f} \colon coker(ker(f)) \to ker(coker(f))$ (eq:PreImageFactorization) from prop. \ref{DecompositionOfMorphisms} is an [[isomorphism]] (hence providing an [[image]] factorization $A \twoheadrightarrow im(f) \hookrightarrow B$).

1. Every [[monomorphism]] is a [[kernel]] and every [[epimorphism]] is a [[cokernel]].

=--

+-- {: .num_prop}
###### Proposition

These two conditions are indeed equivalent.

=--

+-- {: .proof}
###### Proof

The first condition implies that if $f$ is a [[monomorphism]] then $f \cong \ker(\coker(f))$ (in the category of objects over $B$) so $f$ is a kernel. Dually if $f$ is an [[epimorphism]] it follows that $f \cong coker(ker(f))$. So (1) implies (2).

The converse can be found in, among other places, Chapter VIII of ([MacLane](#MacLane)).

=--


## Properties

### General
 {#PropertiesGeneral}

+-- {: .num_remark}
###### Remark

The notion of abelian category is self-dual: [[opposite category|opposite]] of any abelian category is abelian. 

=--

+-- {: .num_remark #RegularEpisAndMonos}
###### Remark

By the second formulation of the definition \ref{AbelianCategory},  in an abelian category

* every [[monomorphism]] is a [[regular monomorphism]];

* every [[epimorphism]] is a [[regular epimorphism]].

It follows that every abelian category is a _[[balanced category]]_.

=--

\begin{prop}\label{PullbackPreservesEpimorphisms}
  In an [[abelian category]], [[pullback]] preserves [[epimorphisms]] and [[pushout]] preserves [[monomorphisms]].
\end{prop}
Because every abelian category is a [[regular category]]. For an explicit proof see, e.g., [Selick, Prop. 1.3.13](#Selick).




### Factorization of morphisms
 {#FactorizationOfMorphisms}

+-- {: .num_prop}
###### Proposition

In an abelian category every morphism decomposes [[generalized the|uniquely up to a unique isomorphism]] into the composition of an [[epimorphism]] and a [[monomorphism]], via prop \ref{DecompositionOfMorphisms} combined with def. \ref{AbelianCategory}.  

Since by remark \ref{RegularEpisAndMonos} every monic is [[regular monomorphism|regular]], hence [[strong monomorphism|strong]], it follows that $(epi, mono)$ is an [[orthogonal factorization system]] in an abelian category; see at _[[(epi, mono) factorization system]]_.

=--

+-- {: .num_remark}
###### Remark

Some references claim that this property characterizes abelian categories among pre-abelian ones, but it is not clear to the authors of this page why this should be so, although we do not currently have a counterexample; see [this discussion](http://nforum.mathforge.org/discussion/4094/?Focus=33415#Comment_33415).

=--

### Canonical $Ab$-enrichment
 {#CanonicalAbEnrichment}

The $Ab$-enrichment of an abelian category need not be specified a priori.  If an arbitrary (not necessarily pre-additive) [[locally small category|locally small]] category $C$ has a [[zero object]], binary products and coproducts, kernels, cokernels and the property that every monic is a kernel arrow and every epi is a cokernel arrow (so that all monos and epis are [[normal monomorphism|normal]]), then it can be equipped with a unique addition on the morphism sets such that composition is bilinear and $C$ is abelian with respect to this structure.  However, in most examples, the $Ab$-enrichment is evident from the start and does not need to be constructed in this way.  (A similar statement is true for [[additive categories]], although the most natural result in that case gives only enrichment over abelian [[monoids]]; see [[semiadditive category]].)

The last point is of relevance in particular for [[infinity-category|higher categorical]] generalizations of additive categories. See for instance [remark 2.14, p. 5](http://www.math.harvard.edu/~lurie/papers/DAG-I.pdf#page=5) of [[Jacob Lurie]]'s [[Stable Infinity-Categories]].

### Relation to exactness properties of toposes
 {#RelationToToposes}

The [[exactness properties]] of abelian categories have many features in common with exactness properties of [[toposes]] or of [[pretoposes]]. 

[Freyd (1999)](AT+category#Freyd99) gave a sharp description of the properties shared by these categories, introducing a new concept called _[[AT categories]]_ (for "abelian-topos"), and showing convincingly that the difference between the A and the T can be concentrated precisely in the difference of the behavior of the initial object. 

### Embedding theorems
 {#EmbeddingTheorems}

Not every [[abelian category]] is a [[concrete category]] such as [[Ab]] or $R$[[Mod]]. But for many proofs in [[homological algebra]] it is very convenient to have a concrete abelian category, for that allows one to check the behaviour of morphisms on actual _elements_ of the sets underlying the [[objects]].

The following _embedding theorems_, however, show that under good conditions an abelian category can be _embedded_ into [[Ab]] as a [[full subcategory]] by an [[exact functor]], and generally can be embedded this way into $R Mod$, for some ring $R$. This is the celebrated _[[Freyd-Mitchell embedding theorem]]_  discussed [below](#FreydMitchellEmbedding).

This implies for instance that proofs about [[exact sequence|exactness of sequences]] in an abelian category can always be obtained by a naive argument on elements -- called a "[[diagram chasing|diagram chase]]" -- because that does hold true after such an embedding, and the exactness of the embedding means that the notion of exact sequences is preserved by it.

Alternatively, one can reason with [[generalized elements]] in an abelian category, without explicitly embedding it into a larger concrete category, see at _[[element in an abelian category]]_. But under suitable conditions this comes down to working subject to an embedding into $Ab$, see the discussion at _[Embedding into Ab](#EmbeddingIntoAb)_ below.

#### Counterexamples

First of all, it's easy to see that not every abelian category is equivalent to $R$[[Mod]] for some ring $R$.  The reason is that $R Mod$ has all [[small category]] [[limits]] and [[colimits]].  For a [[Noetherian ring]] $R$ the category of [[finitely generated module|finitely generated]] $R$-modules is an abelian category that lacks these properties.


#### Embedding into $Ab$
 {#EmbeddingIntoAb}

(...)

([Bergman 1974](#Bergman))

(...)

#### Freyd-Mitchell embedding into $R Mod$
 {#FreydMitchellEmbedding}

+-- {: .num_thm}
###### Mitchell's Embedding Theorem

Every small abelian category admits a [[full functor|full]], [[faithful functor|faithful]] and [[exact functor|exact]] functor to the category $R Mod$ for some ring $R$.

=--

+-- {: .proof}
###### Proof
This result can be found as Theorem 7.34 on page 150 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=176).  His terminology is a bit outdated, in that he calls an abelian category "fully abelian" if admits a full and faithful exact functor to a category of $R$-modules.  See also the [Wikipedia article](http://en.wikipedia.org/wiki/Mitchell%27s_embedding_theorem) for the idea of the proof.
=--

For more see at _[[Freyd-Mitchell embedding theorem]]_.

We can also characterize which abelian categories _are_ equivalent to a category of $R$-modules:

+-- {: .num_theorem}
###### Theorem
Let $C$ be an abelian category.  If $C$ has all [[small category|small]] [[coproducts]] and has a [[compact object|compact]] [[projective object|projective]] [[generator]], then $C \simeq R Mod$ for some ring $R$.  In fact, in this situation we can take $R = C(x,x)^{op}$ where $x$ is any compact projective generator.   Conversely, if $C \simeq R Mod$, then $C$ has all small coproducts and $x = R$ is a compact projective generator.
=--

+-- {: .proof}
###### Proof
This theorem, minus the explicit description of $R$, can be found as Exercise F on page 103 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=132).
The first part of this theorem can also be found as Prop. 2.1.7. of Victor Ginzburg's [Lectures on noncommutative geometry](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=4).  Conversely, it is easy to see that $R$ is a compact projective generator of $R Mod$. 
=--

One can characterize functors between categories of $R$-modules that are either (isomorphic) to functors of the form $B \otimes_R -$ where $B$ is a bimodule or those which look as Hom-modules. For the characterization of the tensoring functors see [[Eilenberg-Watts theorem]]. 

Going still further one should be able to obtain a nice theorem describing the image of the embedding of the weak 2-category of

* rings
* bimodules
* bimodule homomorphisms

into the strict 2-category of 

* abelian categories
* right exact functors
* natural transformations.

For more discussion see the [$n$-Cafe](http://golem.ph.utexas.edu/category/2007/08/questions_about_modules.html).

## Examples

* Of course, [[Ab]] is abelian, 

* the [[category of modules|category $R$Mod of (left) modules]] over any [[ring]] $R$ is abelian

* Therefore in particular the category [[Vect]] of vector spaces over any field is an abelian category

* The full subcategory of $R$Mod whose objects are the Noetherian left $R$-modules is abelian, since it contains any submodule or quotient module of any of its objects (see Theorem 2.3.8 p.103 of Berrick and Keating in the textbook references below).

* Similarly, the full subcategory of $R$Mod whose objects are the Artinian left $R$-modules is abelian, since it contains any submodule or quotient module of any of its objects (loc. cit.).

* Also similarly, the full subcategory of $R$Mod whose objects are the Artinian semisimple modules is abelian, since it contains any submodule or quotient module of any of its objects (loc. cit.) . 

* as is the [[category of representations]] of a [[group]] (e.g. [here](https://unapologetic.wordpress.com/2008/12/15/the-category-of-representations-is-abelian/))

* The [[category of sheaves|category of]] [[sheaves of abelian groups]] on any [[site]] is abelian.


Counter-examples:

* The category of [[torsion subgroup|torsion-free]] abelian groups is pre-abelian, but not abelian: the monomorphism $2:\mathbb{Z}\to\mathbb{Z}$ is not a kernel.


## Related concepts

* [[additive and abelian categories]]

* [[abelian subcategory]]

* [[Deligne tensor product of abelian categories]]

* [[pseudo-abelian category]]

* [[quasi-abelian category]]

* [[semi-abelian category]]

* [[length of an object]]

## References

Maybe the first reference on abelian categories, then still called _exact categories_ is 

* D. A. Buchsbaum, _Exact categories and duality_, Transactions of the American Mathematical Society Vol. 80, No. 1 (1955), pp. 1-34 ([JSTOR](http://www.jstor.org/stable/1993003))

Further foundations of the theory were then laid in 

* [[Alexander Grothendieck]], _[[Tohoku|Sur quelques points d'algèbre homologique]], T&#244;hoku Math. J. vol 9, n.2, 3, 1957.

Other classic references:

* [[Pierre Gabriel]], *[[Des Catégories Abéliennes]]*, Bulletin de la Société Mathématique de France **90** (1962) 323-448 &lbrack;[numdam:BSMF_1962__90__323_0](http://www.numdam.org/item?id=BSMF_1962__90__323_0)&rbrack;


* {#Freyd64} [[Peter Freyd]], _Abelian Categories -- An Introduction to the theory of functors_, originally published by Harper and Row, New York(1964), Reprints in Theory and Applications of Categories **3** (2003)  &lbrack;[tac:tr3](http://www.emis.de/journals/TAC/reprints/articles/3/tr3abs.html), [pdf](https://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf)&rbrack;
  

Textbook accounts:

* [[Nicolae Popescu]], _[[Abelian categories with applications to rings and modules]]_, London Math. Soc. Monographs __3__, Academic Press (1973) &lbrack;[MR0340375](http://www.ams.org/mathscinet-getitem?mr=0340375)&rbrack;

* [[Saunders MacLane]], Chapter VIII of: _[[Categories for the Working Mathematician]]_ (1978)

* A. J. Berrick and M. E. Keating, *Categories and Modules, with K-theory in View*, Cambridge Studies in Advanced Mathematics **67**, Cambridge University Press (2000)

* [[Masaki Kashiwara]], [[Pierre Schapira]], Section 8 of: *[[Categories and Sheaves]]*, Grundlehren der Mathematischen Wissenschaften **332**, Springer (2006) &lbrack;[doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)&rbrack;

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], Chapter 1 of: *Tensor Categories*, AMS Mathematical Surveys and Monographs **205** (2015) &lbrack;[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)&rbrack;

Further review:

* Rankey Datta, _An introduction to abelian categories_  (2010) ([pdf](http://www-bcf.usc.edu/~lauda/teaching/rankeya.pdf))

* {#Selick} Paul Selick, *Homological Algebra Notes* ([pdf](www.math.toronto.edu/selick/mat1352/1350notes.pdf),[[Selick_HomologicalAlgebra.pdf:file]])


On [[diagram chasing]] and [[elements in an abelian category]]:

* {#Bergman} [[George Bergman]], _A note on abelian categories -- translating element-chasing proofs, and exact embedding in abelian groups_ (1974) &lbrack;[pdf](http://math.berkeley.edu/~gbergman/papers/unpub/elem-chase.pdf), [[Bergman-ElementChasing.pdf:file]]&rbrack;
 

For more discussion of the _[[Freyd-Mitchell embedding theorem]]_ see there.

The proof that $R Mod$ is an abelian category is spelled out for instance in 

* Rankeya Datta, _The category of modules over a commutative ring and abelian categories_ ([pdf](http://www.math.columbia.edu/~ums/pdf/Rankeya_R-mod_and_Abelian_Categories.pdf))

A discussion about to which extent abelian categories are a general context for [[homological algebra]] is archived at nForum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2052&Focus=17680#Comment_17680).

See also the [catlist 1999 discussion](http://www.mta.ca/~cat-dist/catlist/1999/atcat) on comparison between abelian categories and topoi ([[AT categories]]).

Formalization of abelian categories as [[univalent categories]] in [[univalent foundations of mathematics]] ([[homotopy type theory]]):

* [[unimath]], *Abelian Categories* &lbrack;[UniMath.CategoryTheory.Abelian](https://unimath.github.io/doc/UniMath/4dd5c17/UniMath.CategoryTheory.Abelian.html)&rbrack;

Generalization of abelian categories to [[(n,1)-categories]] is in:

* Nao Mochizuki, _Higher-dimensional generalization of abelian categories via DG Categories_ &lbrack;[arXiv:2501.06955](https://arxiv.org/abs/2501.06955)&rbrack;

[[!redirects abelian categories]]
[[!redirects Abelian category]]
