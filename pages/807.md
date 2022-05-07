
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The **Euler characteristic** of an object is --  if it exists -- its [[category theory|categorical]] [[dimension]]. 


## Definitions

### Of a chain complex

There are two definitions of the Euler characteristic of a chain complex.  Let $R$ be a [[commutative ring]] and let $V$ be a [[chain complex]] of $R$-[[modules]].

+-- {: .num_defn #EulerCharOfChainComplexPointset}
###### Definition

If each $V_n$ is [[finitely generated object|finitely generated]] and [[projective object|projective]], then the **Euler characteristic** of $V$ is the alternating sum of their [[ranks]], if this is finite:
$$
  \chi(V) := \sum_{n \in \mathbb{Z}} (-1)^n rk_R V_n
  \,.
$$
=--

+-- {: .num_defn #EulerCharOfChainComplex}
###### Definition

If the [[homology group|homology]] of $V$ consists of finitely generated projective modules, then the **Euler characteristic** of $V$ is the alternating sum of its [[Betti number]]s (the [[ranks]] of its homology modules), if this is finite:
$$
  \chi(V) := \sum_{n \in \mathbb{Z}} (-1)^n rk_R H_n(V)
  \,.
$$
=--

When both of these are defined, they are equal.  This is a consequence of the functoriality of the categorical definition (Definition \ref{EulerCharInSymMonCat}).

+-- {: .num_remark #InvariantUnderQIso}
###### Remark
Definition \ref{EulerCharOfChainComplex} shows that the Euler characteristic of chain complexes is invariant under the natural notion of [[equivalence in an (infinity,1)-category|equivalence]] of chain complexes: (zig-zags of) [[quasi-isomorphism]]s.
=--

### Of a topological space (or $\infty$-groupoid)
 {#OfATopologicalSpace}

+-- {: .num_defn #EulerCharOfTopSpace}
###### Definition

For $X$ a [[topological space]] and $R$ some [[ring]], its Euler characteristic over $R$ is the Euler characteristic, according to Def. \ref{EulerCharOfChainComplex}, of its [[homology]] [[chain complex]] (for instance [[singular homology]]), if this is finite: the alternating sum of its [[Betti number]]s

$$
  \chi(X) = \sum_{n \in \mathbb{N}} (-1)^n rk_{\mathbb{Z}} H_n(X, R)
  \,.
$$

=--

By default one takes $R = \mathbb{Z}$ to be the [[integer]]s, but it is equivalent to take $R = \mathbb{Q}$ to be the rational numbers.  (Choosing a ring with torsion, however, might result in a different "Euler characteristic".)

This definition is usually known as the **Euler-Poincar&#233; formula**. Historically earlier was

+-- {: .num_defn #EulerCharOfCWComplex}
###### Definition/Proposition

Let $X$ be a finite [[CW-complex]]. Write $cell(X)_k$ for the set of its $k$-cells. Then the Euler characteristic of $X$ is

$$
  \chi(X) = \sum_{k \in \mathbb{N}} (-1)^k \vert cell(X)_k \vert
  \,.
$$

=--

This is equivalently the Euler characteristic of the [[cellular homology|cellular]] chain complex of $X$ according to Definition \ref{EulerCharOfChainComplexPointset}.  Thus, since the homology of $X$ can be computed with cellular homology, this Euler characteristic agrees with the previous one.

In the special case that $X$ is a [[surface]], Def. \ref{EulerCharOfCWComplex} reduces to the historical definition by [[Leonhard Euler]], which implicitly was known already to Descartes around 1620:

+-- {: .num_defn #EulerCharOfSurface}
###### Definition/Proposition

Let $X$ be a convex [[polyhedron]]. Then its Euler characteristic is

$$
  \chi(X)
  \;\coloneqq\; 
   \vert Vertices(X)\vert 
   - 
   \vert Edges(X)\vert
    + 
   \vert Faces(X)\vert
  \;\in\;
  \mathbb{Z}
  \,,
$$

hence the number of [[vertices]] minus the number of [[edges]] plus the number of [[faces]] in the polyhedron.

=--

In particular if $X$ may be embedded into the [[2-sphere]], this means that 

$$
  2 = \vert Vertices(X)\vert - \vert Edges(X)\vert + 
   \vert Faces(X)\vert
  \,.
$$

By removing one point from the 2-sphere not contained in $X$, the result may be thought of as a [[planar graph]]. This has one [[face]] less than $X$ had (the one containing the point which was removed). Hence 

+-- {: .num_cor #EulerFormulaForPlanarGraphs}
###### Corollary
**([[Euler formula for planar graphs]])**

For a planar [[graph]] $\Gamma$ we have

$$
  1 = \vert Vertices(\Gamma)\vert - \vert Edges(\Gamma)\vert + 
   \vert Faces(\Gamma)\vert
  \,.
$$

=--

### Of an object in a symmetric monoidal category

All the definitions considered so far can be subsumed by the following general abstract one.

+-- {: .num_defn #EulerCharInSymMonCat}
###### Definition

The Euler characteristic of a [[dualizable object]] in a [[symmetric monoidal category]] is its categorical [[dimension]]: the [[trace]] of its [[identity]] [[morphism]].
=--

Explicitly, this means the Euler characteristic of an object $X$ is the composite

$$ S \xrightarrow{\eta} X \otimes X^* \xrightarrow{\cong} X^* \otimes X \xrightarrow{\varepsilon} S $$

where $\eta$ and $\varepsilon$ are the [[unit of an adjunction|unit]] and counit of the dual pair $(X,X^*)$, and $S$ is the unit object of the symmetric monoidal category.  This subsumes the previous definitions as follows:

* In the category of chain complexes over a ring $R$, an object is dualizable if it is finitely generated overall, and projective in each degree.  Its dual is then given by $(X^*)_n = Hom_R(X_{-n},R)$.  The unit $\eta$ picks out $\sum x \otimes x^*$, where $\{x\}$ encompasses a basis for each $X_n$ and $\{x^*\}$ is the dual basis.

  The symmetry isomorphism $X \otimes Y \xrightarrow{\cong} Y \otimes X$ introduces a sign $x\otimes y \mapsto (-1)^{|y|} y\otimes x$, so that when we then evaluate, we get a contribution of $1$ for each $x$ of even degree and $-1$ for each $x$ of odd degree.  Thus we recover Def. \ref{EulerCharOfChainComplexPointset}.  Note that the unit object is $R$ itself in degree zero, so that we see $\chi(X)$ only as an element of $R$ (so, for instance, the Euler characteristic in this sense of a rank-$p$ free $(\mathbb{Z}/p)$-module is zero.

* In the [[derived category]] of chain complexes over $R$, an object is dualizable if it is quasi-isomorphic to one of the form above.  A similar argument shows that its Euler characteristic is then computed as in Def. \ref{EulerCharOfChainComplex}.

The Euler characteristic of a topological space or $\infty$-groupoid can also be defined *directly* with this approach, without a detour into homology.  Namely, if $X$ is any [[Euclidean Neighborhood Retract]], such as a finite [[CW complex]] or a [[smooth manifold]], then its [[suspension spectrum]] $\Sigma_+^\infty X$ is dualizable in the [[stable homotopy category]].  Its dual is the [[Thom spectrum]] of its stable [[normal bundle]], with the unit of the duality being the [[Thom collapse map]].  Its categorical Euler characteristic is then an endomorphism of the sphere spectrum, which can be identified with an integer (via $\pi_0^s(S) = \mathbb{Z}$). See around [DoldPuppe, corollary 4.6](#DoldPuppe)).

Since the categorical definition is purely in terms of the symmetric monoidal structure, Euler characteristics are preserved by any [[symmetric monoidal functor]] (as long as enough of its structure maps are isomorphisms).  Since chains and homology can be made into symmetric monoidal functors, it follows that all the ways of defining the Euler characteristic of a space agree.

See ([PontoShulman](#PontoShulman)) and the discussion at [[Thom spectrum]] for more on this.

### Homotopy cardinality ($\infty$-groupoid cardinality)
 {#HomotopyCardinality}

The [above](OfATopologicalSpace) Euler characteristic of a topological space is the alternating _sum_ over sizes of _homology_ groups. Similar in construction is the alternating _product_ of sizes of [[homotopy group]]s. This goes by the name _[[∞-groupoid cardinality]]_ or _[[homotopy cardinality]]_ . But [below](RelationBetweenDefinitions) we shall see that Euler characteristic of higher categories interpolates between this homotopical and the above homological notion. 

+-- {: .num_defn #EulerCharOfSpaceHomotopically}
###### Definition

For $X$ a [[topological space]] / [[homotopy type]] / [[∞-groupoid]], its **[[homotopy cardinality]]** or **[[∞-groupoid cardinality]]** is -- if it exists -- the [[rational number]] given by the alternating product of [[cardinality|cardinalities]] of [[homotopy group]]s

$$
  \chi_{homotop}(X) :=
  \sum_{[x] \in \pi_0(X)}
    \prod_{k =1}^\infty (|\pi_k(X,x)|)^{(-1)^k}
  \,.
$$

=--

### Of posets, groupoids and categories

The process of sending a [[category]] $C$ to its 
[[geometric realization of categories]] ${\vert C \vert} \in $ [[Top]] $\simeq$ [[Grpd]] is a way to _present_ [[topological space]]s, and hence [[∞-groupoid]]s, by a category: we can think of $\vert C \vert$ as the [[Kan fibrant replacement]] of $C$: the [[universal property|universal solution]] to [[weak inverse|weakly inverting]] all [[morphism]]s of $C$.

Up to the relevant notion of [[equivalence in an (infinity,1)-category]] (which is [[weak homotopy equivalence]]), _every_ [[∞-groupoid]] arises as the [[nerve]]/[[geometric realization of categories|geometric realization]] of a category. In fact one can assume the category to be a [[poset]]. (This follows from the existence of the [[Thomason model structure]], as discussed in more detail there.)

Since the combinatorial data in a [[category]] and all the more in a [[poset]] $C$ is much smaller than in that of its [[Kan fibrant replacement]] $\vert C \vert$, it is of interest to ask if one can read off the Euler characteristic $\chi(\vert C \vert)$ already from $C$ itself. This is indeed the case:

#### Of finite categories
 {#LECharOfCategory}

+-- {: .num_defn #EulerCharOfCat}
###### Definition

Let $C$ be a finite [[category]]. A **weighting** on $C$ is a [[function]]

$$
 k^{(-)} : ob C \to \mathbb{Q}
$$

satsifying 

$$
  \forall a \in ob C \;:\; \sum_{b \in ob C} \vert C(a,b) \vert k^b
  = 1
  \,,
$$

where $\vert C(a,b)\vert$ is the [[cardinality]] of the [[hom-set]] $C(a,b)$. A **coweighting** on $C$ is a weighting on the [[opposite category]] $C^{op}$.

If $C$ admits both a weighting $\{k^a\}$ and a coweighting $\{k_a\}$, then its **Euler characteristic** is

$$
  \chi(C) := \sum_{a \in ob C} k^a = \sum_{a \in ob C} k_a
  \;\;\;
  \in \mathbb{Q}
  \,.
$$

=--

The definition of Euler characteristic of [[poset]]s  appears for instance in ([Rota](#Rota)). For [[groupoid]]s it has been amplified in [BaezDolan](#BaezDolan). The joint generalization to categories is due to ([Leinster](#Leinster)), where the above appears as def. 2.2.

+-- {: .num_remark }
###### Remark

Notice that this $\chi(C)$ is in general not an [[integer]], but a [[rational number]]. However in sufficiently well-behaved cases, discussed [below](RelationBetweenDefinitions), $\chi(C)$ coincides with the topological Euler characteristic $\chi(\vert C \vert)$ of its [[geometric realization of categories|geometric realization]]. Since that is integral, in these cases also $\chi(C)$ is.

=--

#### Of enriched and higher categories
 {#LECharOfEnrichedCat}

Let $V$ be an good enrichment category (for instance a [[cosmos]]) which itself comes equipped with a good notion of cardinality, in the form of a monoidal functor

$$
  |-| : V \to \mathbb{R}
  \,.
$$

Then the above formula for the Euler characteristic of a category verbatim generalizes to $V$-[[enriched categories]]. The ordinary case is recovered for $V = $ [[FinSet]] and $|-| : FinSet \to \mathbb{R}$ the ordinary [[cardinality]] operation.

Since [[strict infinity-categories]] can be understood as arising from iterative enrichment

$$
  Str2Cat \simeq Cat-Cat
$$

$$
  Str3Cat \simeq Str2Cat-Cat
$$

etc, this gives a notion of Euler characteristic of strict $\infty$-categories, hence in particular of [[strict infinity-groupoid]]s.

One should be able to show that applied to strict $\infty$-groupoids this does reproduce [[homotopy cardinality]].



## Properties

### Compatibility with homotopy colimits
 {#UnderHomotopyColimits}

Euler characteristic behaves well with respect to the basic operations in [[homotopy theory]].

+-- {: .num_prop }
###### Proposition


In a [[symmetric monoidal category|symmetric monoidal]] [[triangulated category]] with [[dualizable object]]s $X, Y, Z$, if

$$
  \array{
    Z &\to& Y
    \\
    \downarrow && \downarrow
    \\
    X &\to& W
  }
$$

is a [[homotopy pushout]], then the [tractial Euler characteristic](EulerCharInSymMonCat) of $W$ exists and is

$$
  \chi(W) = \chi(X) + \chi(Y) - \chi(Z)
  \,.
$$

=--

This is due to ([May, 1991](#May)).


### Relations between the various definitions
 {#RelationBetweenDefinitions}

The following propositions assert that and how the various definitions of Euler characteristics all suitably agree when thez jointly apply.

+-- {: .num_prop }
###### Proposition

For $X$ a [[compact space|compact]] [[manifold]] let $P_T(X)$ be the [[poset]] of inclusions of [[simplices]] of a [[triangulation]] $T$ of $X$. Then the poset Euler characteristic of $P_T(X)$ coincides with the Euler characteristic of $X$ as a topological space

$$
  \chi(X) = \chi(P_T(X))
  \,.
$$

=--

This appears as ([Stanley, 3.8](#Stanley)).

The following proposition asserts that the definition \ref{EulerCharOfCat} of Euler characteristic of a category is indeed consistent, in that it does compute the Euler characteristic, def. \ref{EulerCharOfTopSpace} of the corresponding $\infty$-groupoid:

+-- {: .num_prop #PosteEulerCharGiveSpaceCharUnderRealization}
###### Proposition

Let $C$ be a finite [[poset]] or, slightly more generally, a finite [[skeleton|skeletal]] [[category]] with no nontrivial [[endomorphism]]s.

Write $\vert C \vert \in $ [[Top]] $\simeq$ [[∞Grpd]] for its [[geometric realization of categories|geometric realization]]. Then

$$
  \chi(C) = \chi(\vert C \vert)
  \,.
$$
 
=--

For posets this is due to Philipp Hall, appearing as ([Stanley, prop. 3.8.5]). For finite categories this is  ([Leinster, cor. 1.5, prop. 2.11](#Leinster)).

+-- {: .num_prop }
###### Proposition

For $X$ a [[manifold]], regard its [[suspension spectrum]]

$$
  \Sigma^\infty X \in Ho(Spec)
$$

as an object in the [[stable homotopy category]]. Then its Euler characteristic as an object of a [[symmetric monoidal category]], def. \ref{EulerCharInSymMonCat} coincides with its topological Euler characteristic, def. \ref{EulerCharOfTopSpace}.

=--

This is due to ... (?)

+--{: .query}
[[Mike Shulman|Mike]]: Can the Euler characteristic of a category be recovered as the trace for a dualizable object in some symmetric monoidal category?
=---

### Relation between Euler characteristic and $\infty$-groupoid cardinality

For topological space / $\infty$-groupoids, there is both the notion of [homological Euler characteristic](OfATopologicalSpace) as well as the notion of [homotopy cardinality](HomotopyCardinality). 

The latter looks a bit like the "exponential" of the former, so while similar to some extent they are very different notions, taken on face value. Still, the [Euler characteristic of a category](LECharOfCategory) or rather that [of a higher category](LECharOfEnrichedCat) does interpolate between the two notions:

+-- {: .num_prop #ReproducingGroupoidCardinality}
###### Proposition

For $C$ a finite [[groupoid]], its Euler characteristic as a category, def. \ref{EulerCharOfCat}, coincides with its homotopical Euler characteristic, def. \ref{EulerCharOfSpaceHomotopically} or [[groupoid cardinality]]

$$
  \chi(C) = \chi_{homotop}(C)
  \,.
$$

=--

This is noted in ([Leinster, example 2.7](#Leinster)).


+-- {: .num_example }
###### Example

For instance for $G$ a [[finite group]] let $B G \simeq K(G,1) \in $ [[Ho(Top)]] be its [[classifying space]]. This is the [[geometric realization of categories|geometric realization]] both of the one-object groupoids $*//G$ as well as of some finite [[poset]] $C$.

$$
  B G \simeq |*//G| \simeq |C|
  \,.
$$

By prop. \ref{PosteEulerCharGiveSpaceCharUnderRealization} we have that the categorical Euler characteristic of $C$ is the topological Euler characteristic of $B G$. But by prop. \ref{ReproducingGroupoidCardinality} we have that the categorical Euler characteristic of $*//G$ is the [[homotopy cardinality]] of $B G$.

=--

Typically for one and the same $\infty$-groupoid, Eucler characteristic and homotopy cardinality are never both well defined: if the series for one converges, that for the other does not.

However, by applying some standard apparent "tricks" on non-convergent series, often these can be made sense of after all, and then do agree with the other notion. For more on this see ([Baez05](#Baez05)).

### Connected sum formula

+-- {: .num_prop #EulerCharacteristicOfConnectedSums}
###### Proposition
**([[Euler characteristic]] of [[connected sums]])**

Let $X$ and $Y$ be [[closed manifolds]] ([[topological manifold|topological]] or [[differentiable manifold|differentiable]])  of [[even number|even]] [[dimension]]. Then the [[Euler characteristic]] of their [[connected sum]] is the [[sum]] of their separate [[Euler characteristics]], minus 2:

$$
  \chi
  \big(
    X \sharp Y 
  \big)
  \;=\;
  \chi
  \big(X\big)
  +
  \chi
  \big(Y\big)
  -2
$$ 

=--

(e.g. [here](http://math.ucr.edu/~res/miscpapers/csums+echars.pdf))

### Gauss-Bonnet theorem

For $X$ an even-[[dimension]]al [[smooth manifold]], its Euler characteristic may also be given by [[integration]] of [[infinitesimal object|infinitesimal]] data: this is the statement of the higher dimensional [[Gauss-Bonnet theorem]].

### Poincaré–Hopf theorem

* [[Poincaré–Hopf theorem]]

## Related concepts

* [[Euler class]]

* [[orbifold Euler characteristic]]

* [[arithmetic genus]]

* [[C-field tadpole cancellation]]

## References

Review includes

* Jonathan Libgober, _The Euler characteristic, Poincaré–Hopf theorem, and applications_ ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2010/REUPapers/Libgober.pdf))


Textbook account:

* [[Edwin Spanier]],  p. 156 onwards in: _Algebraic topology_, McGraw-Hill  (1966)  

Efremovich and Rudyak shown that the Euler characteristic is (up to the overall multiplicative factor) the only additive homotopy invariant of a finite CW complexes:

* V. A. Efremovich, Yu. B. Rudyak, _On the concept of the Euler characteristic_, Uspehi Mat. Nauk __31__:5(191) (1976), 239&#8211;240 [MR458412](http://www.ams.org/mathscinet-getitem?mr=458412), [Russian pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=3975&volume=31&year=1976&issue=5&fpage=239&what=fullt)

The description of Euler characteristics are categorical [[trace]]s in [[symmetric monoidal categories]] is discussed in section 4 of

* {#DoldPuppe} [[Albrecht Dold]], [[Dieter Puppe]], _Duality, trace and transfer_ , Proceedings of the Steklov Institute of Mathematics, (1984), issue 4
 

Behaviour of tracial Euler characteristic under [[homotopy colimit]]s is discussed in 

* {#May} [[Peter May]], _The additivity of traces in triangulated categories_ K-theory (1991) ([website](http://www.math.uiuc.edu/K-theory/0474/))
 

Textbooks on combinatorial aspects of Euler characteristic include

* {#Stanley} Richard P. Stanley, _Enumerative Combinatorics_ , Vol. I, Cambridge Studies in Advanced Mathematics 49, Cambridge University Press, corrected reprint (1997)
 

* {#Rota} [[Gian-Carlo Rota]], _On the foundations of combinatorial theory I: theory of M&#246;bius functions_ , Z. Wahrscheinlichkeitstheorie und Verw. Gebiete 2 (1964), 340&#8211;368.
 

The Euler characteristic of a smooth manifold as its [[dimension]] in the [[stable homotopy category]] is discussed in example 3.7 of

* {#PontoShulman} [[Kate Ponto]], [[Mike Shulman]], _Traces in symmetric monoidal categories_ ([pdf](http://www.sandiego.edu/~shulman/papers/traces_sym.pdf), [slides](http://www.sandiego.edu/~shulman/papers/ccrtraces.pdf)).
 

See [[Thom spectrum]] for more on this

The Euler characteristic of groupoids -- [[groupoid cardinality]] -- has been amplified in 

* {#BaezDolan} [[John Baez]], [[James Dolan]], _From Finite Sets to Feynman Diagrams_ ([arXiv](http://arxiv.org/abs/math.QA/0004133))
 

An exposition with an eye towards the relation between Euler characteristic and $\infty$-groupoid cardinality is in 

* [[John Baez]], _The mysteries of counting: Euler characteristic versus homotopy cardinality_ ([web](http://math.ucr.edu/home/baez/counting/)) Lecture notes (2005)
 {#Baez05}

The role of homotopy cardinality in [[quantization]] is touched on towards the end of

* [[Daniel Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]],  _[[Topological Quantum Field Theories from Compact Lie Groups]]_ 

The generalization of the definition of Euler characteristic from posets to categories is due to

* [[Tom Leinster]], _The Euler characteristic of a category_ ([arXiv:0610260](http://arxiv.org/abs/math/0610260))
  {#Leinster}

* [[Tom Leinster]], _The Euler characteristic of a category as a sum of a divergent series_ ([arXiv:0707.0835](http://arxiv.org/abs/0707.0835)) 


The compatibility of Euler characteristic of categories with [[homotopy colimits]] is discussed in 

* [[Thomas Fiore]], Wolfgang L&#252;ck, Roman Sauer, _Euler Characteristics of Categories and Homotopy Colimits_ ([arXiv:1007.3868](http://arxiv.org/abs/1007.3868))

More on Euler characteristics of categories is in

* Kazunori Noguchi, _The Euler characteristic of infinite acyclic categories with filtrations_, [arxiv/1004.2547](http://arxiv.org/abs/1004.2547)


On "Negative sets" and Euler characteristic:

* [[André Joyal]], _Regle des signes en algebre combinatoire_ , Comptes Rendus Mathematiques de l'Academie des Sciences, La Societe Royale du Canada VII (1985), 285-290.

* [[Steve Schanuel]], _Negative sets have Euler characteristic and dimension_ , Lecture Notes in Mathematics 1488, Springer Verlag, Berlin, 1991, pp. 379-385.

* Daniel Loeb, _Sets with a negative number of elements_ , Adv. Math. 91 (1992), 64-74. 

Resumming divergent Euler characteristics:

* William J. Floyd, Steven P. Plotnick, _Growth functions on Fuchsian groups and the Euler characteristic_ , Invent. Math. 88 (1987), 1-29.

* R. I. Grigorchuk, _Growth functions, rewriting systems and Euler characteristic_ , Mat. Zametki 58 (1995), 653-668, 798.

* James Propp, _Exponentiation and Euler measure_ , Algebra Universalis 49 (2003), 459-471. ([arXiv:math.CO/0204009](http://arxiv.org/abs/math/0204009)).

* James Propp, _Euler measure as generalized cardinality_ . ([arXiv](http://arxiv.org/abs/math/0203289)). 

Euler characteristics of tame spaces:

* Lou van den Dries, _Tame Topology and O-Minimal Structures_ Cambridge U. Press, Cambridge, 1998. Chapter 4.2: Euler Characteristic. 

Euler characteristics of groups:

* G. Harder, _A Gauss-Bonnet formula for discrete arithmetically defined groups_ , Ann. Sci. Ecole Norm. Sup. 4 (1971), 409-455.

* [[Jean-Pierre Serre]], _Cohomologie des groups discretes_ , Ann. Math. Studies 70 (1971), 77-169.

* [[Kenneth Brown]], _Euler characteristics, in Cohomology of Groups_ , Graduate Texts in Mathematics 182, Springer, 1982, pp. 230-272. 

* O. Y. Viro, _Some integral calculus based on Euler characteristic_, in Topology and Geometry -- Rohlin Seminar, Springer Lec. Notes in Math. __1346__, 127--138 (1988) [doi](http://dx.doi.org/10.1007/BFb0082775)

Complex cardinalities:

* Andreas Blass, _Seven trees in one_ , Jour. Pure Appl. Alg. 103 (1995), 1-21. ([web](http://www.math.lsa.umich.edu/~ablass/cat.html))

* Robbie Gates, _On the generic solution to $P(X) = X$ in distributive categories_ , Jour. Pure Appl. Alg. 125 (1998), 191-212.

* [[Marcelo Fiore]], [[Tom Leinster]], _An objective representation of the Gaussian integers_ , Jour. Symb. Comp. 37 (2004), 707-716. ([arXiv](http://arxiv.org/abs/math/0211454))

* [[Marcelo Fiore]], [[Tom Leinster]], _Objects of categories as complex numbers_ , Adv. Math. 190 (2005), 264-277 ([arXiv:0212377](http://arxiv.org/abs/math/0212377))

* [[Marcelo Fiore]], _Isomorphisms of generic recursive polynomial types_ , to appear in 31st Symposium on Principles of Programming Languages (POPL04). ([ps](http://www.cl.cam.ac.uk/~mpf23/papers/Types/recisos.ps.gz)) 

* [[C. T. C. Wall]], _Arithmetic invariants of subdivision of complexes_, Canad. J. Math. 18(1966), 92-96, [doi](http://dx.doi.org/10.4153/CJM-1966-012-9), [pdf](http://cms.math.ca/cjm/v18/cjm1966v18.0092-0096.pdf)

[[!redirects Euler characteristics]]
