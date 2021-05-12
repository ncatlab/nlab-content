
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesion
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}
[[!redirects quality]]
[[!redirects Quality type]]
[[!redirects extensive quality]]
[[!redirects intensive quality]]
[[!redirects persistent localization]]
[[!redirects quintessential localization]]
[[!redirects quintessential localisation]]
[[!redirects persistent localisation]]

## Idea

A **quality type** is a key concept in [[W. Lawvere]]'s axiomatic approach to [[cohesion]] which permits to analyze a [[space]] understood as a domain of _quantitative_ variation via its _qualitative_ aspects. This can be viewed as an [[axiom|axiomatisation]] of the commonly encountered situation in [[geometry]] or [[dynamics]] that problems permit (only) a qualitative analysis.

A primary example for that kind of deferred analysis is the study of [[topological spaces]] via the [[homotopy category]] (hence via the [[homotopy types]] which they represent). So in a very broad sense, quality types are intended as ingredients to a _synthetic homotopy theory_[^SHT] where the (homotopy) contraction of a space (the collapsing of a [[cylinder object|cylinder]]/two [[idempotents]]) is extracted as essence of the concept of a spatial 'attribute'. 

Technically, a quality type amounts to a special sort of [[essential geometric morphism|essential localization]] and is therefore called a **quintessential localization**  in ([Johnstone 1996](#JS96)).

In typical (topos) cases these come in the form of [[adjoint modalities|adjoint cylinders]] $\Pi\dashv\Delta\dashv\Gamma$ (with $\Delta$ [[fully faithful functor|fully faithful]]) such that the [[connected components]] and the [[global section|global sections functor]] coincide (="collapse"): $\Pi\cong\Gamma$ (cf. [[points-to-pieces transform]]). This implies for spaces in the domain of the functors that every connected component contains exactly one point. Spaces with this property are called **infinitesimal spaces**[^Inf] in ([Lawvere 2008](#Law08)).

Hence from a more _geometrical point of view_, an object in a quality type is a particular simple kind of space with 'degenerate' components, or, if you prefer, a space with 'thick' or 'coarse' points which in turn can be viewed as a minimal vestige of cohesion: when a set is a space with no cohesion, an object in a quality type is a space with _almost_ no cohesion.[^GoC] (For an elaboration of this perspective in the context of [[cohesive toposes]] see at [[infinitesimal cohesion]].)

Quality types together with the **continuity axiom** are an essential ingredient to Lawvere's ([2007 axioms](#Law07)) for geometry:

>That Continuity axiom (preservation of infinite products by $\pi_0$) was introduced in order to obtain homotopy types that are "qualities" in an intuitive sense[^qual] (as they should be automatically in the continuous case). Lawvere ([message to catlist oct 26th 2011](https://github.com/punkdit/categories/blob/master/gmane/science/mathematics/categories/7016))

([Lawvere 1998](#Law98), [Lawvere 2008](#Law08), [Marmolejo-Menni 2016](#MarmoMenni16)) also point to the role of continuity in insuring that the Hurewicz homotopy category becomes a quality type. The definition of quality type yields important contrasts with _pure variation_ and _sufficient cohesion_ permitting to attend to the _fine structure_ of the [[gros topos|petit-gros]] landscape. So we can say with only slight exaggeration that the 2007 axioms revolve around the concept of a quality type and that cohesive spaces are those that admit qualitative (homotopical) analysis!

In the following we discuss the case for ordinary categories, for the higher order generalization see [[infinitesimal cohesive (infinity,1)-topos]].

## Definition

Let $\mathcal{S},\mathcal{F}$ be [[extensive categories]]. A [[fully faithful functor]] $q^*:\mathcal{S}\to\mathcal{F}$ is said to exhibit $\mathcal{F}$ as a **quality type** over $\mathcal{S}$ if $q^*$ has both a left and a right adjoint which moreover coincide: $q_!\dashv q^*\dashv q_*$ and $q_!\cong q_*$.

Let $\mathcal{E}$ be a (pre)cohesive category over $\mathcal{S}$ with adjoint string $p_!\dashv p^* \dashv p_* \dashv p^!:\mathcal{S}\to\mathcal{E}$ and $q^*:\mathcal{S}\to\mathcal{F}$ a quality type over $\mathcal{S}$. A functor $s:\mathcal{E}\to\mathcal{F}$ is called an **intensive quality** on $\mathcal{E}$ if $s$ preserves finite products and finite coproducts and $q_*\circ s =p_*$.

Dually, a finite coproduct preserving functor $h:\mathcal{E}\to\mathcal{F}$ with $q_!\circ h=p_!$ is called an **extensive quality** on $\mathcal{E}$.

####Remark

Intuitively, an intensive quality is compatible with the points of its domain spaces and an extensive quality with the connected components.

Note that a quality type yields itself a (pre)cohesive category with (degenerate) adjoint string $q_!\dashv q^*\dashv q_*\dashv q^*$. This situations obtains when the induced transformation $p_*\to p_!$ of the [[Nullstellensatz]] is not only an epimorphism but a natural isomorphism (cf. [Lawvere 2007](#Law07)).

## Examples

> If we divest smooth spaces of all global cohesion, keeping only the jets (on which the Thom-Mather singularities depend), we obtain a category in which every connected component of any object has exactly one point, so that the natural map between those functors is an isomorphism.  Lawvere (2004, p.108)

* Kan complexes over $Set$: The role of Kan complexes in this context is discussed in Marmolejo-Menni ([2016](#MarmoMenni16)).

* Galois theory - presheaves on the opposite of the category of finite-dimensional local k-algebras (Lawvere 2004).

####Remark

The properties of (pre)cohesive categories are fine-tuned to yield a canonical extensive quality via the Hurewicz construction $\pi (X^Y)$. In the blueprint for this, namely the combinatorial homotopy theory in Gabriel-Zisman ([1967](#GabrielZisman67), chap. III), the category of spaces has objects [[compactly generated space|Kelley spaces]]. In a sense, the concept of continuity can be viewed as a mean to bypass the construction of the [[category of fractions]] necessary in this case.

### The topos of $\mathbb{F}_1$-actions
 {#TheToposOfF1Actions}

Lawvere's work on the petit-gros topos distinction ([Lawvere 1976](#Law76)) started with the examination of two toposes of graphs ([Lawvere 1986](#Law86)). The first one of _"irreflexive" [[quiver|graphs]]_ is given by the presheaf topos of actions of the small diagram category $E\rightrightarrows V$ on $Set$ and is an [[étendue]] hence petit. 

Whereas the second one of _reflexive graphs_ is given by the actions of the [[graphic monoid]] $\Delta _1=\{1,\partial_0,\partial_1\}$ with $\partial_i\partial_j=\partial_i$ for $i,j=0,1$. $\Delta _1$ is [[Morita equivalence|Morita equivalent]] to the diagram category $E\stackrel{\leftrightarrows}{\leftarrow} V$ and consists entirely of [[idempotents]]. Its topos of actions is gros and when taken over $FinSet$ satisfies the axioms for a (sufficiently) [[cohesive topos]]. The 'abelianization' of $\Delta _1$ is $\mathbb{F}_1=\{1,e\}$, the multiplicative monoid with a generic (nontrivial) idempotent $e$ which incidentally is also the monoid underlying the [[blueprint]] for the [[field with one element]].

As observed in ([Lawvere 1989](#Law89), p.277) $\mathcal{S}^{\mathbb{F}_1^{op}}$ is a quality type over $\mathcal{S}$. It was probably the first one to arise and its status of being neither petit nor gros being commented on. Some of the details are spelled out in the following section.

The surjective homomorphism $q:\Delta_1\to\mathbb{F}_1$ induces an adjoint string $q_!\dashv q^*\dashv q_*:\mathcal{S}^{\Delta_1^{op}}\to\mathcal{S}^{\mathbb{F}_1^{op}}$ with $q_*$ discarding all non-loops in a reflexive graph.

For details how the [[zeta function]] arises via the Burnside ring of $\mathcal{S}^{\mathbb{F}_1^{op}}$ in this context see ([Lawvere 1989](#Law89), pp.291-292). $\mathbb{F}_1$-torsors are discussed in Johnstone ([2002](#J02a), p.380).

## Quality types as localizations

Properties of quality types were first studied by P. Johnstone ([1996](#JS96)) using the language of [[localization|localizations]].

+-- {: .num_defn #quintessentialloc}
###### Definition 
Let $\mathcal{C}$ be a finitely complete category. An [[level|essential localization]] $l\dashv r\dashv i:\mathcal{L}\to\mathcal{C}$ is called **quintessential** if $l$ is naturally isomorphic to $i$.
=--

A trivial example of a quintessential localization is provided by $id_\mathcal{C}$.

+-- {: .num_example}
###### Example

Another simple _example_ of a quintessential localization is given by the category $\mathcal{C}$ with objects pairs $(X, e)$ where $X$ is a set and $e=e^2$ an idempotent map $X\to X$. A morphism $f:(X_1, e_1)\to (X_2, e_2)$ is a function $f:X_1\to X_2$ with $f\cdot e_1=e_2\cdot f$. These equivariant morphisms are bound to preserve fixpoints: when $e_1(x)=x$ then $f(e_1(x))=f(x)=e_2(f(x))$. Then the fixpoint set functor $r:\mathcal{C}\to Set$ with $r(X, e)=\{x\in X | e(x)=x \}$ is left as well as right adjoint to $i(X)=(X, id_X)$ since an equivariant morphism $f:(X,e)\to (Y,id_Y)$ is uniquely determined by its restriction to the fixpoints of $e$ and its values are given by $f(e(x))$. The [[adjoint modalities]] $i\cdot r\dashv i\cdot r:\mathcal{C}\to\mathcal{C}$ corresponding to $i\dashv r\dashv i:Set\to\mathcal{C}$ map $(X,e)$ to $(r(X),id_{r(X)})$. Of course, $\mathcal{C}$ is up to equivalence just the category $\mathcal{S}^{\mathbb{F}_1^{op}}$ from above!

=--

+-- {: .num_example}
###### Example
Consider the monoid $(\overline{\mathbb{N}}, \cdot , 0)$ consisting of the natural numbers in their usual order with a point $\infty$ attached at infinity such that $\forall n\in \mathbb{N}: n$&lt;$\infty$ with multiplication $m\cdot n=max\{m,n\}$. $\overline{\mathbb{N}}$ is commutative and satisfies the [[graphic category|graphic identity]] $x\cdot y\cdot x = x\cdot y$. Then $i:Set\hookrightarrow Set^{\overline{\mathbb{N}}}$ with $i(X)=(X, \pi_2:\overline{\mathbb{N}}\times X\to X)$ exhibits $Set^{\overline{\mathbb{N}}}$ as a quality type over $Set$ (Cf. Freyd et al. ([1999](#FOPTST99)) and O'Hearn et al. ([1995](#OPTT95))).

This can be viewed as a more elaborate version of the preceding example where $\infty$ corresponds to $e$ upon identifying $\mathcal{C}$ as the category $\mathcal{S}^{\mathbb{F}_1^{op}}$.

(Caveat: this needs checking!)

=--

To say that $l\dashv r\dashv i:\mathcal{L}\to\mathcal{C}$ is a quintessential localization amounts to say that $i:\mathcal{L}\to\mathcal{C}$ exhibits $\mathcal{C}$ as a quality type over $\mathcal{L}$ with $r$ providing the right adjoint to $i\simeq l$ (provided $\mathcal{L}$, $\mathcal{C}$ are extensive).

Note that a quintessential subtopos is [[dense subtopos|dense]] since $i$ is up to natural isomorphism a left adjoint whence preserves all colimits and the initial object in particular!

Since the [[adjoint modality|adjoint modalities]] $l\cdot r\dashv i\cdot r$ corresponding to a quintessential subtopos as a [[level of a topos|level]] coincide up to natural isomorphism, one sees that quintessential levels are their own [[Aufhebung]].

+-- {: .num_defn #persistentloc}
###### Definition 
Let $\mathcal{C}$ be a finitely complete category. A [[localization]]  $r\dashv i:\mathcal{L}\to\mathcal{C}$ is called **persistent** if $\mathcal{L}$ is closed under subobjects in $\mathcal{C}$.
=--

Quintessential localizations of toposes are persistent ([Johnstone 1996](#JS96), p.94). Since [[separated object|separated objects]] for a [[Lawvere-Tierney topology]] $j$ are precisely the subobjects of $j-sheaves$ it follows that a persistent (and, in particular, a quintessential) subtopos coincides with its [[quasitopos]] of $j$-separated objects. Conversely, a subtopos with the property that it coincides with the corresponding quasitopos is persistent.

+-- {: .num_theorem #quintidempotent}
###### Theorem  

Let $\mathcal{E}$ be a [[Cauchy completion|Cauchy- complete category]]. The quintessential localizations of $\mathcal{E}$ correspond precisely to idempotent endomorphisms of the identity functor on $\mathcal{E}$. Moreover, quintessential subcategories of $\mathcal{E}$ form a semilattice under intersection.
=--

For the proof cf. ([Johnstone 1996](#JS96), p.93).

## Related entries

* [[cohesive topos]]

* [[infinitesimal cohesive (infinity,1)-topos]]

* [[compactly generated topological space]]

* [[ambidextrous adjunction]]

* [[Nullstellensatz]]

* [[Aufhebung]]

## Remarks on the literature

The definition of quality types occurs in ([Lawvere 2007](#Law07)) with important additional remarks in ([Lawvere 2008](#Law08)). The first occurrence of a quality type is in the work of the 1980s in the context of the gros topos of graphs: a discussion of this example is in ([Lawvere 1989](#Law89a),  p.277) where already the contrast to sufficient cohesion is observed. ([Lawvere 1991](#Law91a), pp.9-10) has a short but suggestive discussion in the context of [[synthetic differential geometry]]. The short abstract ([Lawvere 1998](#Law98)) anticipates the 2007 axioms as 'fine-tuning' to accomodate the homotopy category as a quality type. Quality types resurface without an explicit definition in the [2004 paper](#Law04) on data types.

Under the name of quintessential localization they are the focus of ([Johnstone 1996](#JS96)) where the characterization via central idempotents is given. Some additional results occur in the context of the [[Nullstellensatz]] in ([Johnstone 2011](#JS11)). ([Menni 2014](#Menni14b)) attends to the contrast between quality types and sufficient cohesion. A variant is studied as the concept of a _bireflective subcategory_ in Freyd et al. ([1999](#FOPTST99)).

## References

* {#FOPTST99}[[Peter Freyd|P. J. Freyd]], P. W. O'Hearn, [[John Power|A. J. Power]], M. Takeyama, [[Ross Street|R. Street]], R. D. Tennent, _Bireflectivity_ , Theor. Comp. Sci. **228** (1999) pp.49-76.

* [[Pierre Gabriel|P. Gabriel]], M. Zisman, _Calculus of Fractions and Homotopy Theory_ , Springer Heidelberg 1967.{#GabrielZisman67}

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#JS11} [[Peter Johnstone|P. Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#J02} [[Peter Johnstone|P. Johnstone]], _Sketches of an Elephant vol. 1_ , Cambridge UP 2002. (pp.202,380)

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law76}[[F. W. Lawvere]], _Variable quantities and variable structures in topoi_ , pp.101-131 in Heller, Tierney (eds.), Algebra, Topology and Category Theory, Academic Press New York 1976.

* {#Law86} [[F. W. Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](http://tac.mta.ca/tac/reprints/articles/9/tr9.pdf))

* {#Law89a} [[F. W. Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* {#Law91a} [[F. W. Lawvere]], _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law92} [[F. W. Lawvere]], _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al (eds.), _The Space of Mathematics_ , de Gruyter Berlin 1992.

* {#Law96} [[F. W. Lawvere]], _Unity and Identity of Opposites in Calculus and Physics_ , App. Cat. Struc **4** (1996) pp.167-174.

* {#Law98} [[F. W. Lawvere]], _Are Homotopy Types the same as Infinitesimal Skeleta ?_ , abstract (1998). ([link](http://cms.math.ca/Events/summer98/s98-abs/node17.e))

* {#Law99} [[F. W. Lawvere]], _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law04} [[F. W. Lawvere]], _Left and right adjoint operations on spaces and data types_ , Theor. Comp. Sci. **316** (2004) pp.105-111.

* {#Law07} [[F. W. Lawvere]], _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp.41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* {#Law08} [[F. W. Lawvere]], _Cohesive Toposes: Combinatorial and Infinitesimal Cases_, Como Ms. 2008. ([pdf](http://comocategoryarchive.com/Archive/temporary_new_material/FWLawvere-Cohesive-Toposes-Como-January-2008.pdf))

* {#MarmoMenni16}F. Marmolejo, [[Matías Menni|M. Menni]], _On the relation between continuous and combinatorial_ , arXiv:1602.02826 (2016). ([abstract](http://arxiv.org/abs/1602.02826))

* {#Menni14a} [[Matías Menni|M. Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah. Top. G&#233;om. Diff. Cat. **LV** (2014). ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))

* {#Menni14b} [[Matías Menni|M. Menni]], _Continuous Cohesion over Sets_ , TAC **29** no.20 (2014) pp.542-568. ([pdf](http://www.tac.mta.ca/tac/volumes/29/20/29-20.pdf))

* {#OPTT95} P. W. O'Hearn, A. J. Power, M. Takeyama, R. D. Tennent, _Syntactic Control of Interference Revisited_ , Electronic Notes in Theor. Comp. Sci. **1** (1995) pp.1-40.

* {#PRW89} [[Robert Paré|R. Paré]], [[Bob Rosebrugh|R. Rosebrugh]], R. J. Wood, _Idempotents in Bicategories_ , Bull. Austr. Math. Soc. **39** (1989) pp.421-434.

* C. Ruiz S., R. Ruiz, _Conditions for a Realization Functor to Commute with Finite Products_ , Revista Colombiana de Matem&#225;ticas **XV** (1981) pp.113-146. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002540479))

[^SHT]: The term _synthetic homotopy theory_ is slightly misleading here as Lawvere's ideas don't provide a fully fledged homotopy theory but are rather observations on the role of the cylinder configuration in the analysis of space and spatial dimension. Important facets of his views are documented in Lawvere [1992](#Law92), [1994](#Law94), [1999](#1999) and a more thorough discussion of the homotopical apects of the concept appears in Marmolejo-Menni ([2016](#MarmoMenni16)).
In a complementary direction, _[[homotopy type theory]]_ provides a synthetic formulation of [[homotopy theory]] proper, not just of the [[homotopy category]], and _[[cohesive homotopy type theory]]_ implements [[cohesion]] _in_ that natively homotopy-theoretic context. 

[^qual]: The claim that _quality types_ intend to model the philosophical concept of _quality_ reoccurs at several places in Lawvere's writings though the concrete connection still needs to be spelled out. Some motivation is provided in [Lawvere (1992)](#Law92) where it is linked to the negation of _quantity_ as a logical category of being that is indifferent to non-being (cf. Hegel's [[Science of Logic]]) e.g. whereas the temperature varies continuously or "indifferently" below and above zero degree, the same transition makes a crucial difference for the phase or "qualitative being" of water. Note that Lawvere sticks here to the traditional view that quantitative being comes before qualitative being whereas Hegel in his _Logic_ reversed the traditional hierarchy of the categories. 

[^Inf]: A motivation for this terminology from [[synthetic differential geometry|SDG]] can be found in a remark in ([Lawvere 1991](Law91a), pp.9-10).

[^GoC]: From another perspective, one could view an object in a quality type as a set with _germs of cohesion_.

[[!redirects bireflective subcategory]]