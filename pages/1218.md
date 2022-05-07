
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Cohesive toposes
+-- {: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}



# Contents
* table of contents
{: toc}

## Idea

A **diffeological space** is a type of [[generalized smooth space]].  As with the other variants, it subsumes the notion of [[smooth manifold]] but also naturally captures other spaces that one would like to think of as smooth spaces but aren't manifolds; for example, the space of all smooth maps between two smooth manifolds can be made into a diffeological space. (These mapping spaces are rarely manifolds themselves, see [[manifolds of mapping spaces]].)

In a little more detail, a **diffeology**, $\mathcal{D}$ on a set $X$ is a [[presheaf]] on the [[category of open subsets]] of Euclidean spaces with smooth maps as morphisms.  To each open set $U \subseteq \mathbb{R}^n$, it assigns a subset of $\Set(U,X)$.  The functions in $\Set(U,X)$ are to be regarded as the "smooth functions" from $U$ to $X$.  A **diffeological space** is then a set together with a diffeology on it.

Diffeological spaces were originally introduced in ([Souriau 79](#Souriau79)). They have subsequently been developed in the textbook ([Iglesias-Zemmour 13](#PIZ))

## Definition

+-- {: mynumdef #DiffSp}
###### Definition
Let $\mathcal{Op}$ denote the [[site]] whose objects are the open subsets of the Euclidean spaces $\mathbb{R}^n$  and whose morphisms are [[smooth map]]s between these.

A **diffeological space** is a pair $(X,\mathcal{D})$ where 

* $X$ is a set 

* and $\mathcal{D} \in Sh(\mathcal{Op})$ is a **[[diffeology]]** on $X$:

  * a [[subobject|subsheaf]] of the sheaf $U \mapsto Hom_{Set}(U,X)$ with $\mathcal{D}(*) = X$

  * equivalently: a [[concrete sheaf]] on the [[site]] $\mathcal{Op}$ such that $\mathcal{D}(*) = X$ - a [[concrete object|concrete]] [[smooth space]] (see there for more details).

A [[morphism]] of diffeological spaces is a morphism of the corresponding [[sheaves]]: we take $DiffeologicalSp \hookrightarrow Sh(CartSp)$ to be the full [[subcategory]] on the diffeological spaces in the sheaf topos.

=--

For $(X,\mathcal{D})$ a diffeological space, and for any $U \in \mathcal{Op}$, the set $\mathcal{D}(U)$ is also called the set of **[[plots]]** in $X$ on $U$. This is to be thought of as the set of ways of mapping $U$ smoothly into the would-be space $X$. This assignment _defined_ what it means for a map $U \to X$ of sets to be smooth. 

For some comments on the reasoning behind this kind of definition of generalized [[space]]s see [[motivation for sheaves, cohomology and higher stacks]].

A sheaf on the site $\mathcal{Op}$ of open subsets of Euclidean spaces is completely specified by its restriction to [[CartSp]], the full subcategory of [[Cartesian space]]: The [[fully faithful functor]] $CartSp \hookrightarrow \mathcal{Op}$ is a [[dense subsite]]-inclusion.  Therefore in the sequel we shall often restrict our attention to [[CartSp]].

One may define a _[[smooth sets]]_ to be _any_ sheaf of [[CartSp]].
A diffeological space is equivalently a [[concrete sheaf]] on the [[concrete site]] [[CartSp]]. (For details see [this Prop.](geometry+of+physics+--+smooth+sets#DiffeologicalSpacesAreTheConcreteSmoothSets) at _[[geometry of physics -- smooth sets]]_.)


The [[full subcategory]]

$$
  DiffeologicalSpaces \hookrightarrow Sh(CartSp)
$$

on all concrete sheaves is not a [[topos]], but is a [[quasitopos]].

This is Prop. \ref{DiffeologicalSpacesAreTheConcreteSmoothSets} below.

The concreteness condition on the sheaf is a reiteration of the fact that a diffeological space is a subsheaf of the sheaf $U \mapsto X^{|U|}$.  In this way, one does not have to explicitly mention the underlying set $X$ as it is determined by the sheaf on the one-point open subset of $\mathbb{R}^0$.


## Examples

* Every [[smooth manifold]] $X$, i.e. every object of [[Diff]], becomes a diffeological space by defining the [[plots]] on $U \in CartSp$ to be the ordinary [[smooth function]]s from $U$ to $X$, i.e. the morphisms in [[Diff]]:

  $$  
    X : U \mapsto Hom_{Diff}(U,X)
    \,.
  $$

* For $X$ and $Y$ two diffeological spaces, their [[product]] as sets $X \times Y$ becomes a diffeological space whose [[plots]] are pairs consisting of a [[plot]] into $X$ and one into $Y$

  $$
    X \times Y : U \mapsto Hom_{DiffSp}(U,X) \times Hom_{DiffSp}(U,Y)
    \,.
  $$

* Given any two diffeological spaces $X$ and $Y$, the set of 
  morphisms $Hom_{DiffSp}(X,Y)$ becomes a smooth space by taking 
  the [[plots]] on some $U$ to be the smooth morphisms $X \times U \to Y$, 
  i.e. the smooth $U$-parameterized families of smooth maps from $X$ to $Y$:

  $$
    [X,Y] : U \mapsto Hom_{DiffSp}(X \times U, Y)
    \,.
  $$

  In this formula we regard $U \in CartSp \hookrightarrow Diff$ 
  as a diffeological space according to the above example. 
  In fact, we apply secretly here the [[Yoneda embedding]] 
  and use the general formula for the 
  cartesian [[closed monoidal structure on presheaves]].

## Properties

### Relation to topological and $\Delta$-generated spaces
 {#RelationToTopologicalSpaces}



[[!include adjunction between topological spaces and diffeological spaces]]


Further discussion of the [[D-topology]] is in [CSW 13](#CSW13).



### Topological homotopy type and diffeological shape
 {#OnTopologicalHomotopyTypeAndDiffeologicalShape}


[[!include diffeological singular simplicial set -- definition]]


[[!include topological homotopy type is cohesive shape of continuous diffeology -- proposition]]





### Embedding of smooth manifolds into diffeological spaces
 {#EmbeddingOfSmoothManifoldsIntoDiffeoloticalSpaces}

+-- {: .num_prop}
###### Proposition

The obvious functor from the [[category]] [[SmoothManifolds]] of [[smooth manifolds]] to the [[category]] [[DiffeologicalSpaces]] of diffeological spaces is a [[full and faithful functor]]

$$
  SmoothManifolds \hookrightarrow  DiffeologicalSpacess
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is a direct consequence of the fact that [[CartSp]]$_{smooth}$ is a [[dense sub-site]] of [[SmoothManifolds]] and the [[Yoneda lemma]]. 

It may nevertheless be useful to spell out the elementary proof directly:

To see that the functor is faithful, notice that if $f,g : X \to Y$ are two [[smooth function]]s that differ at some point, then they must differ in some [[open neighbourhood]] of that point. This [[open ball]] is a [[plot]], hence the corresponding diffeological spaces differ on that [[plot]].

To see that the functor is full, we need to show that a map of sets $f : X \to Y$ that sends [[plots]] to [[plots]] is necessarily a [[smooth function]], hence that all its [[derivative]]s exist. This can be tested already on all smooth curves $\gamma : (0,1) \to X$ in $X$. By [[Boman's theorem]], a function that takes all smooth curves to smooth curves is necessarily a smooth function. But curves are in particular [[plots]], so a function that takes all [[plots]] of $X$ to [[plots]] of $Y$ must be smooth.

=--

+-- {: .num_remark}
###### Remark

The proof shows that we could restrict attention to the full sub-site $CartSp_{dim \leq 1} \subset CartSp$ on the objects $\mathbb{R}^0$ and $\mathbb{R}^1$ and still have a full and faithful embedding

$$
  Diff \hookrightarrow Sh(CartSp_{dim \leq 1})
  \,.
$$

This fact plays a role in the definition of [[Frölicher space]]s, which are [[generalized smooth space]]s defined by [[plots]] by curves into and out of them.

While the site $CartSp_{dim \leq 1}$ is more convenient for some purposes, it is not so useful for other purposes, mostly when diffeological spaces are regarded from the point of view of the full sheaf topos: the sheaf topos $Sh(CartSp_{dim \leq 1})$ lacks some non-[[concrete sheaf|concrete]] sheaves of interest, such as the sheaves of differential forms of degree $\geq 2$.

=--

### Embedding of smooth manifolds with boundary into diffeological spaces

+-- {: .num_prop #SmoothManifoldsWithBoundaryEmbedIntoDiffeologicalSpaces}
###### Proposition
**([[manifolds with boundaries and corners]] form [[full subcategory]] of [[diffeological spaces]])**

The evident [[functor]]

$$
  SmthMfdWBdrCrn \overset{\phantom{AAAA}}{\hookrightarrow} DiffeologicalSpaces
$$

from the [[category]] of [[smooth manifold|smooth]] [[manifolds with boundaries and corners]] to that of [[diffeological spaces]] is [[fully faithful functor|fully faithful]], hence is a [[full subcategory]]-embedding.

=--

([Igresias-Zemmour 13, 4.16](#PIZ), [Gürer & Iglesias-Zemmour 19](#GurerIZ19))


### Embedding of Banach manifolds into diffeological spaces
 {#EmbeddingOfBanachManifoldsIntoDiffeologicalSpaces}


Also [[Banach manifolds]] embed [[full and faithful functor|fully faithfully]] into the category of diffeological spaces.  In ([Hain](#Hain)) this is discussed in terms of Chen smooth spaces.


### Embedding of Fr&#233;chet manifolds into diffeological spaces {#RelationBetweenDeffeologicalAndFrechetStructure}

We discuss a natural embedding of [[Fréchet manifolds]] into the category of  diffeological spaces.

+-- {: .num_defn }
###### Definition

Define a [[functor]]

$$
  \iota \colon FrechetManifolds \to DiffeologicalSpaces
$$

in the evident way by taking for $X$ a [[Fréchet manifold]] for any $U \in $ [[CartSp]] the set of $U$-[[plots]] of $\iota(X)$ to be the set of smooth functions $U \to X$.

=--

+-- {: .num_prop #FrechetEmbedding}
###### Proposition

The functor $\iota \colon FrechetManifolds \hookrightarrow DiffeologicalSpaces$ is a [[full and faithful functor]].

=--

This appears as ([Losik 94, theorem 3.1.1](#Losik94), following [Losik 92](#Losik92)), as variant of the analogous statement for [[Banach manifolds]] in ([Hain](#Hain)). The fact that maps between Fr&#233;chet spaces are smooth if and only if they send smooth curves to smooth curves was proved earlier in ([Fr&#246;licher 81, th&#233;or&#232;me 1](#Frolicher))

The statement is also implied by ([Kriegl-Michor 97, cor. 3.14](#KrieglMichor)) which states that functions between [[locally convex vector spaces]] are diffeologically smooth precisely if they send smooth [[curves]] to smooth curves. This is not true if one uses [[Michal-Bastiani smooth map|Michal-Bastiani smoothness]] ([Gl&#246;ckner 06](#Glockner06)), in which case one merely has a [[faithful functor]] $lctvs \to DiffeologicalSpaces$. Notice that the choice of topology in ([Kriegl-Michor 97](#KrieglMichor)) is such that this equivalence of notions reduces to the above just for Fr&#233;chet manifolds.


+-- {: .num_prop }
###### Proposition

Let $X, Y \in SmoothManifold$ with $X$ a [[compact manifold]]. 

Then under this embedding, the diffeological mapping space structure $C^\infty(X,Y)_{diff}$ on the mapping space coincides with the Fr&#233;chet manifold structure $C^\infty(X,Y)_{Fr}$:

$$
  \iota(C^\infty(X,Y)_{Fr})
  \simeq
  C^\infty(X,Y)_{diff}
  \,.
$$

=--

This appears as ([Waldorf 09, lemma A.1.7](#Waldorf09)).

$\,$

### Embedding of diffeological spaces into smooth sets
 {#EmbeddingOfDiffeologicalSpacesIntoTheSheafTopos}

We discuss how diffeological spaces are equivalently the [[concrete objects]] in the [[cohesive topos]] of [[smooth sets]] (see [there](smooth+set#Cohesion)).


+-- {: .num_prop #DiffeologicalSpacesAreTheConcreteSmoothSets}
###### Proposition
**(diffeological spaces are the concrete smooth sets)**

The [[full subcategory]] on the [[concrete objects]] in the [[topos]] $SmoothSet \coloneqq Sh(Cart)$ of [[smooth sets]] is [[equivalence of categories|equivalent]] to the category of diffeological spaces

=--

+-- {: .proof}
###### Proof


The [[concrete sheaves]] for the [[local topos]] $Sh(CartSp)$ are by definition those objects $X$ for which the 
$(\Gamma \dashv CoDisc)$-[[unit of an adjunction|unit]]

$$
  X \to CoDisc \Gamma X
$$

is a [[monomorphism]]. Monomorphisms of sheaves are tested objectwise, so that means equivalently that for every $U \in CartSp$ we have that 

$$
  X(U) \simeq Hom_{Sh}(U,X) \to Hom_{Sh}(U, Codisc \Gamma X)
  \simeq Hom_{Set}(\Gamma U, \Gamma X)
$$

is a monomorphism. This is precisely the condition on a sheaf to be a diffeological space.

=--

For a fully detailed proof see [this Prop.](geometry+of+physics+--+smooth+sets#DiffeologicalSpacesAreTheConcreteSmoothSets) at _[[geometry of physics -- smooth sets]]_.


+-- {: .num_cor}
###### Corollary

The category of diffeological spaces is a [[quasitopos]].

=--

+-- {: .proof}
###### Proof

This follows from the discussion at [Locality](#Locality).

=--



This has some immediate general abstract consequences

+-- {: .num_cor}
###### Corollary

The category of diffeological spaces is 

* a [[cartesian closed category]] 

* a [[closed monoidal category]].

=--

### Embedding of diffeological spaces into higher differential geometry
 {#EmbeddingOfDiffeologicalSpacesIntoHigherDifferentialGeometry}

In the last section we saw the embedding of diffeological spaces as precisely the [[concrete objects]] is the [[sheaf topos]] $Sh(CartSp) \simeq Sh(SmthMfd)$ of [[smooth sets]]. This is a general context for [[differential geometry]]. From there one can pass further to [[higher differential geometry]]: the topos of smooth sets in turn embeds

$$
  Sh(CartSp) \hookrightarrow
  Smooth \infty Grpd \coloneqq Sh_\infty(CartSp) 
$$

into the [[(∞,1)-topos]] [[Smooth∞Grpd]] of "higher [[smooth sets]]" --[[smooth ∞-groupoids]] -- as precisely the [[truncated object in an (∞,1)-category|0-truncated objects]].

### Distribution theory

Since a space of [[smooth functions]] on a [[smooth manifold]] is canonically a diffeological space, it is natural to consider the _smooth_ [[linear functionals]] on such [[mapping spaces]]. These turn out to be equivalent to the [[continuous linear functionals]], hence to [[distributional densities]]. See at _[[distributions are the smooth linear functionals]]_ for details.

## Related concepts

* [[model structure on diffeological spaces]]

* [[smooth set]]

* [[Diff]]

* [[diffeological groupoid]], [[diffeological ∞-groupoid]]

* [[connectology]]


## References 
 {#References}

### General
  {#ReferencesGeneral}

The basic idea of understanding [[generalized smooth spaces]] as [[concrete sheaves]] on a [[site]] of smooth test spaces originates in work of [[Kuo Tsai Chen]] (see also at _[[Chen space]]_):

* {#Chen73} [[Kuo Tsai Chen]], _Iterated integrals of differential forms and loop space homology_, Ann. Math. 97 (1973), 217&#8211;246 ([jstor:1970846](https://www.jstor.org/stable/1970846))

Chen considered (apart from [[iterated integrals]]) effectively [[presheaves]] on a site of [[convex subsets]] of [[Cartesian spaces]]. In

* {#Chen75} [[Kuo Tsai Chen]], _Iterated integrals, fundamental groups and covering spaces_, Trans. Amer. Math. Soc. 206 (1975), 83&#8211;98 ([jstor:1997148](https://www.jstor.org/stable/1997148))

roughly the [[sheaf]] condition was added (without using any of this sheaf-theoretic terminology). The definition of _[[Chen spaces]]_ stabilized in

* {#Chen77} [[Kuo Tsai Chen]], _Iterated path integrals_, Bull. Amer. Math. Soc. 83, (1977), 831&#8211;879 ([euclid:1183539443](https://projecteuclid.org/euclid.bams/1183539443))

and served as the basis of a celebrated theorem on the [[de Rham cohomology]] of [[loop spaces]].

A brief review is in 

* [[Kuo-Tsai Chen]], _On differentiable spaces_, in:  [[William Lawvere]], [[Stephen Schanuel]] (eds.), _[[Categories in Continuum Physics]]_, Lectures given at a Workshop held at SUNY, Buffalo 1982, Lecture Notes in Mathematics 1174, 1986 ([doi:10.1007/BFb0076928](https://link.springer.com/book/10.1007/BFb0076928))

(which, curiously, still does not make the connection to the theory of sheaves).

{#However} However, Chen does not require the domains of his plots to be [[open subsets]], which makes Chen spaces be closely related to but different from [[diffeological spaces]] (see [Stacey 11, p. 32](#Stacey11)) 

The proper concept of diffeological spaces was introduced, under the name _diff&eacute;ologie_ and apparently independently from Chen, in:

* {#Souriau79} [[Jean-Marie Souriau]], _Groupes diff&#233;rentiels_, in _Differential Geometrical Methods in Mathematical Physics_ (Proc. Conf., Aix-en-Provence/Salamanca, 1979), Lecture Notes in Math. 836, Springer, Berlin, (1980), pp. 91&#8211;128. ([doi:10.1007/BFb0089728](https://doi.org/10.1007/BFb0089728), [mr:607688](http://www.ams.org/mathscinet-getitem?mr=607688))

* {#Souriau84} [[Jean-Marie Souriau]], _Groupes différentiels et physique mathématique_,  In: Denardo G., Ghirardi G., Weber T. (eds.) Group Theoretical Methods in Physics. Lecture Notes in Physics, vol 201. Springer 1984 ([doi:10.1007/BFb0016198](https://doi.org/10.1007/BFb0016198))

motivated there by [[diffeological groups]] arising in [[geometric quantization]].

Following Souriau, a comprehensive textbook account of [[differential geometry]] formulated in terms of [[diffeological spaces]] (and coining that term) is 

* {#PIZ} [[Patrick Iglesias-Zemmour]], _Diffeology_, Mathematical Surveys and Monographs, AMS (2013) ([web](http://math.huji.ac.il/~piz/Site/The%20Book.html), [ ISBN:978-0-8218-9131-5](https://bookstore.ams.org/surv-185))
  
following the thesis

* {#IglesiasZemmour85} [[Patrick Iglesias-Zemmour]], _Fibrations diff&#233;ologiques et Homotopie_,  PhD thesis (1985) ([web](http://math.huji.ac.il/~piz/Site/The%20Articles/D9DD15EE-6993-4CA3-8B9B-4FC1DEF4A418.html), [pdf](http://math.huji.ac.il/~piz/documents/TheseEtatPI.pdf), [[IglesiasZemmourFibrationsDiffeologiques1985.pdf:file]])

which contains some useful material that may not yet have made it into the book. 


Further exposition and lecture notes are in 

* [[Patrick Iglesias-Zemmour]], _Diffeologies_, talk at _[[New Spaces for Mathematics and Physics]]_, IHP Paris 2015 ([video recording](https://www.youtube.com/watch?v=4sZDmiVOhaA))

* {#IglesiasZemmour18} [[Patrick Iglesias-Zemmour]], _An introduction to diffeology_, lecture at _[Modern Mathematics Methods in Physics: Diffeology, Categories and Toposes and Non-commutative Geometry Summer School](http://www.turkmath.org/beta/konferans.php?id_konferans=365)_, 2018, to appear in _[[New Spaces for Mathematics and Physics]]_ ([pdf](http://math.huji.ac.il/~piz/documents/AITD.pdf))

The article 

* [[John Baez]], [[Alexander Hoffnung]], _Convenient Categories of Smooth Spaces_, Transactions of the American Mathematical Society Vol. 363, No. 11  ([arXiv:0807.1704](http://arxiv.org/abs/0807.1704), [jstor:41307457](https://www.jstor.org/stable/41307457))

amplifies the point that diffeological spaces are [[concrete sheaves]] forming a [[quasi-topos]].


A discussion of the relations of variants of the definition is in

* {#Stacey11} [[Andrew Stacey]], _Comparative Smootheology_, Theory and Applications of Categories,  Vol. 25, 2011, No. 4, pp 64-117. ([tac:25-04](http://www.tac.mta.ca/tac/volumes/25/4/25-04abs.html))

More pointers and monthly seminars at:

* [diffeology.net](http://diffeology.net/)


Application to [[classifying spaces]] and [[universal connections]]:

* [[Mark Mostow]], _The differentiable space structures of Milnor classifying spaces, simplicial complexes, and geometric realizations_, J. Differential Geom. Volume 14, Number 2 (1979), 255-293 ([euclid:jdg/1214434974](https://projecteuclid.org/euclid.jdg/1214434974))


### Full subcategories

The [[full subcategory]]-inclusion of [[Banach manifolds]] into the category of diffeological spaces is due to 

* {#Hain} [[Richard Hain]], _A characterization of smooth functions defined on a Banach space_,  Proc. Amer. Math. Soc. 77 (1979), 63-67 ([web](http://www.ams.org/journals/proc/1979-077-01/S0002-9939-1979-0539632-8/home.html), [pdf](http://www.ams.org/journals/proc/1979-077-01/S0002-9939-1979-0539632-8/S0002-9939-1979-0539632-8.pdf))
 
The (non-full) embedding of [[locally convex vector spaces]] and [[Michal-Bastiani smooth maps]] into diffeological spaces is discussed around corollary 3.14 in 

* {#KrieglMichor} [[Andreas Kriegl]], [[Peter Michor]]: _[[The convenient setting of global analysis]]_, AMS (1997) 

That there are diffeologically-smooth maps between locally convex vector spaces that are not continuous, and a fortiori not smooth in the sense of Michal-Bastiani is given, for instance, in

* {#Glockner06} Helge Gl&#246;ckner, _Discontinuous non-linear mappings on locally convex direct limits_, Publ. Math. Debrecen 68 (2006) 1-13, [arXiv:math/0503387](http://arxiv.org/abs/math/0503387).

The [[full subcategory]]-inclusion of [[Fréchet manifolds]] into diffeological spaces is discussed in 

* {#Losik92} [[Mark Losik]], _Fr&#233;chet manifolds as diffeological spaces_, Soviet. Math. 5 (1992)  ([mathnet:ivm4812](http://mi.mathnet.ru/eng/ivm4812))

and reviewed in  

* {#Losik94} [[Mark Losik]], Section 3 of: _Categorical Differential Geometry_. Cah. Topol. G&#233;om. Diff&#233;r. Cat&#233;g., 35(4):274&#8211;290, 1994 ([numdam:CTGDC_1994__35_4_274_0](http://www.numdam.org/item/CTGDC_1994__35_4_274_0))
 

The proof can in fact be deduced from th&#233;or&#232;me 1 of

* {#Frolicher} [[Alfred Frölicher]], _Applications lisses entre espaces et vari&#233;t&#233;s de Fr&#233;chet_, C. R. Acad. Sci. Paris S&#233;r. I Math. **293** (1981), no. 2, 125&#8211;127. [BnF](http://gallica.bnf.fr/ark:/12148/bpt6k5533894s/f31.image)

The preservation of [[mapping spaces]] under this embedding is due to

* {#Waldorf09} [[Konrad Waldorf]], _Transgression to Loop Spaces and its Inverse I_, Cah. Topol. Geom. Differ. Categ., 2012, Vol. LIII, 162-210 ([arXiv:0911.3212](http://arxiv.org/abs/0911.3212)) 
 

The largest [[topological space|topology]] on the set which underlies a diffeological space with respect to which all [[plots]] are [[continuous functions]] (the "[[D-topology]]") is studied in 

* {#SYH10} [[Kazuhisa Shimakawa]], K. Yoshida, [[Tadayuki Haraguchi]], _Homology and cohomology via enriched bifunctors_, Kyushu Journal of Mathematics, 2018 Volume 72 Issue 2 Pages 239-252 ([arXiv:1010.3336](https://arxiv.org/abs/1010.3336), [doi:10.2206/kyushujm.72.239]( https://doi.org/10.2206/kyushujm.72.239))

* {#CSW13} [[J. Daniel Christensen]], Gord Sinnamon, [[Enxin Wu]], _The $D$-topology for diffeological spaces_, Pacific Journal of Mathematics 272 (1), 87-110, 2014 ([arXiv:1302.2935](http://arxiv.org/abs/1302.2935), [doi:10.2140/pjm.2014.272.87](https://msp.org/pjm/2014/272-1/p04.xhtml))

Some [[homotopy theory]] modeled on diffeological spaces (instead of on [[topological spaces]]) via their [[cohesion|cohesive]] [[shape modality|shape]] is discussed in 

* {#ChristensenWu13} [[J. Daniel Christensen|J. Daniel Christensen]],  [[Enxin Wu]], _The homotopy theory of diffeological spaces, I. Fibrant and cofibrant objects_, New York J. Math. 20 (2014), 1269-1303 ([arXiv:1311.6394](http://arxiv.org/abs/1311.6394))

The [[full subcategory]]-inclusion of [[manifolds with boundaries and corners]] is discussed in 

* {#GurerIZ19} [[Serap Gürer]],  [[Patrick Iglesias-Zemmour]], _Differential forms on manifolds with boundary and corners_, Indagationes Mathematicae, Volume 30, Issue 5, September 2019, Pages 920-929 ([doi:10.1016/j.indag.2019.07.004](https://doi.org/10.1016/j.indag.2019.07.004))





### For orbifolds
 {#ReferencesForOrbifolds}

On [[orbifolds]] regarded as naive [[quotient spaces]] (instead of [[homotopy quotients]]/[[Lie groupoids]]/[[differentiable stacks]]) but as such formed in [[diffeological spaces]]:

* {#IKZ10} [[Patrick Iglesias-Zemmour]], [[Yael Karshon]], Moshe Zadka, _Orbifolds as diffeologies_, Transactions of the American Mathematical Society 362 (2010), 2811-2831 ([arXiv:math/0501093](https://arxiv.org/abs/math/0501093))

* {#Watts15} [[Jordan Watts]], _The Differential Structure of an Orbifold_, Rocky Mountain Journal of Mathematics, Vol. 47, No. 1 (2017), pp. 289-327 ([arXiv:1503.01740](https://arxiv.org/abs/1503.01740))

On this approach seen in the broader context of [[higher differential geometry]]:

* [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

[[!redirects diffeological space]]
[[!redirects diffeological spaces]]

[[!redirects diffeological structure]]
[[!redirects diffeological structures]]

[[!redirects diffeology]]
[[!redirects diffeologies]]

[[!redirects DiffeologicalSpaces]]

[[!redirects Chen smooth space]]
[[!redirects Chen smooth spaces]]
