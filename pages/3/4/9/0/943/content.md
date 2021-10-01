
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The term [[convenient category of topological spaces]] is used (e.g. [Steenrod 1967](#Steenrod67)) for a [[category]] of [[topological spaces]] [[nice topological space|nice]] enough to address many of the needs of [[topology|working topologists]], notably including the condition of being a [[cartesian closed category]]. As such, they are examples of [[nice category of spaces|nice categories of spaces]].

A primary example is the category of [[compactly generated spaces]].


## Definition

While the authors of this article don't know whether there exists in the literature a widely accepted definition of "convenient category of topological spaces", we propose the following definition as reasonable and convenient (see also the discussion [below](#NvC) on the distinction between "nice" and "convenient"): 

+-- {: .num_defn}
###### Definition

A **convenient category of topological spaces** is a [[full subcategory|full]] [[replete subcategory]] $C$ of the category of all topological spaces [[Top]] such that the following conditions 1-3 hold: 

1. Every [[CW complex]] is an object of $C$; 

2. $C$ is [[cartesian closed]]; 

3. $C$ is [[complete category|complete]] and [[cocomplete category|cocomplete]]. 
=--

Frequently it is also felt desirable to add closure under certain types of [[subspaces]]. For instance, in the well-known examples one has 

* $C$ is closed under [[closed subspaces]] in [[Top]], i.e., if $X$ belongs to $C$ and $A \subseteq X$ is a closed subspace (in $Top$), then $A$ also belongs to $C$. 

At times one might hope that $C$ is closed under [[open subspaces]] as well, but this does not hold for all objects in some of the well-known examples of convenient categories. 

It may be well to note that [[colimits]] and [[limits]] in $C$ need not agree with the corresponding colimits and limits in $Top$, except under certain conditions.  Some convenient categories are [[reflective subcategory|reflective]] or [[coreflective subcategory|coreflective]] in $Top$, in which case they are closed under limits or colimits respectively.  Moreover, because $C$ is a full subcategory of $Top$ which contains all CW complexes, the usual sorts of colimits used to present CW complexes are the same whether interpreted in $Top$ or in $C$.  Also, if $C$ is closed under closed subspaces, then an [[equalizer]] of a pair of maps between [[Hausdorff spaces]] in $C$ (being a closed subspace) is the same whether computed in $Top$ or in $C$.

On the other hand, [[products]] of $C$-objects in $Top$ need not land in $C$, so in that situation the product in $Top$ and the product in $C$ do not agree.  This is in particular the case for compactly generated spaces.  In fact, the "[[compactly generated product]]" is sometimes preferable to the $Top$-product for more explicit reasons: for instance, if $X$ and $Y$ are CW complexes, then $X \times Y$ need not be a CW complex in the usual product topology, but it is in the compactly generated topology.


## Examples
 {#Examples}


### Categories of colimits of generating spaces
 {#CategoriesOfColimitsOfGeneratingSpaces}

The original example of a convenient category of topological spaces is that of 

* [[compactly generated topological space]]

and another example is that of 

* [[Delta-generated spaces]] ([[Euclidean-generated spaces]]).

Both of these are special cases of the general class of convenient *$GenSp$-generated topological spaces*:

These are those topological spaces $X$ which agree with the [[colimit]] ([in TopSp](Top#UniversalConstructions)) of all continuous images inside them of *generating spaces* in a specified [[full subcategory]] $GenSp \,\subset\, $ [[TopSp]] ([Vogt 1971, Sec. 1](#Vogt71)):

\[
  \label{Gfication}
  G(X)
  \,\coloneqq\,
  \Big(
  \underset{
    \underset{
      { T \in GenSp }
      \atop
      {T \to X}
    }{\longrightarrow}
  }{\lim}
  \,
  T
  \Big)
  \xrightarrow{\;\;\; \simeq \;\;\;}
  X
\]

The [[full subcategories]] of such $GenSp$-generated spaces are [[coreflective subcategory|coreflective]] ([Vogt 1971, Cor. 1.4](#Vogt71))

$$
  TopSp
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\hookleftarrow}
      {\;\;\;\;\bot\;\;\;\;}
  G TopSp
  \,.
$$

If one demands of the category $GenSp \,\hookrightarrow TopSp\,$ of generating spaces, for any pair $G_1, G_2 \,\in\, GenSp$ that ([Vogt 1971, Axiom 2](#Vogt71)):

1. their [[product topological space]] is again in $GenSp$;

1. the [[compact-open topology]] on the set of maps $G_1 \to G_2$ has a [[continuous function|continuous]] [[evaluation map]]

then $G TopSp$ is a [[Cartesian closed category]] ([Vogt 1971, Thm. 3.6](#Vogt71)), with [[internal hom]] given by the image under $G$-fication (eq:Gfication) of the [[compact open topology]].

If one in addition demands that $GenSp$ contains all [[Cartesian spaces]] $\mathbb{R}^n$, then $G(X) \to X$ is a [[weak homotopy equivalence]] (...).  

As special cases of this general construction, the above examples of

* [[compactly generated topological spaces]]  is obtained by 

  taking $GenSp$ to be given by all [[compact Hausdorff spaces]]

* [[Delta-generated topological spaces]] is obtained by 

  taking $GenSp$ to be given by all [[Cartesian spaces]] (equivalently by all [[topological simplices]]).

See also [Gaucher 2007, Sec. 2](#Gaucher07).

Further developments along these lines are in[Escardo, Lawson &Simpson 2004](#EscardoLawsonSimpson04):

The topological spaces $X$ for which there is an [[exponential law for spaces|exponentiable space]] in [[Top]] (i.e such that $X \times (-)  \;\colon\; Top \to Top$ has a [[right adjoint]])
may be described more concretely as _core-compact_ spaces (spaces whose topology is a [[continuous lattice]]). Suppose given a collection $\mathcal{C}$ of core-compact spaces, with the property that the product of any two spaces in $\mathcal{C}$ is a [[colimit]] in [[Top]] of spaces in $\mathcal{C}$. Such a collection $\mathcal{C}$ is called **productive**. Spaces which are $Top$-colimits of spaces in $\mathcal{C}$ are called $\mathcal{C}$-**generated**. 

+-- {: .num_theorem}
######Theorem 
**(Escard&#243;, Lawson, Simpson)**
 
If $\mathcal{C}$ is a productive class, then the full subcategory of $Top$ whose objects are $\mathcal{C}$-generated is a [[coreflective subcategory]] of [[Top]] (hence [[complete category|complete]] and [[cocomplete category|cocomplete]]) that is [[cartesian closed category|cartesian closed]]. 
=-- 

The other convenience conditions listed in this article (inclusion of [[CW-complexes]], closure under [[closed subspaces]]) are in practice usually satisfied as well. For example, if closed subspaces of objects of $\mathcal{C}$ are $\mathcal{C}$-generated, then closed subspaces of $\mathcal{C}$-generated spaces are also $\mathcal{C}$-generated. If the unit interval $I$ is $\mathcal{C}$-generated, then so are all CW-complexes. 

### Subcategories of toposes
 {#ExamplesSubcategoriesOfToposes}

The [above](#CategoriesOfColimitsOfGeneratingSpaces) example of the category of [[Delta-generated topological spaces]] [above](#CategoriesOfColimitsOfGeneratingSpaces) has the remarkable property that it is 

1. a [[full subcategory]] of the [[quasi-topos]] of [[diffeological spaces]] (see [there](diffeological+space#RelationToTopologicalSpaces)), 

1. which is in turn a [[full subcategory]] of the [[cohesive topos]] of [[smooth sets]] (see [there](geometry+of+physics+--+smooth+sets#DiffeologicalSpacesAreTheConcreteSmoothSets));

1. which in turn is a [[full sub-(infinity,1)-category|full sub-$(\infty,1)$-category]] of the [[cohesive (infinity,1)-topos|cohesive $(\infty,1)$-topos]] of [[smooth infinity-groupoids|smooth $\infty$-groupoids]]

such that the canonical [[shape modality]] (the [[shape via cohesive path ∞-groupoid|smooth path ∞-groupoid construction]]) still sees the correct underlying [[homotopy type]] of topological spaces ([[schreiber:Proper Orbifold Cohomology|SS20, Ex. 3.18]], see also at [[model structure on Delta-generated topological spaces]]):

\begin{imagefromfile}
    "file_name": "TopologicalConvenienceBySmoothGroupoids210930.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [SS21](https://ncatlab.org/schreiber/show/Equivariant+principal+infinity-bundles)"
\end{imagefromfile}

## Counterexamples

A naive approach to the problem of constructing "convenient categories" usually runs into problems. For example, one could try to work with the full subcategory of $Top$ consisting of [[exponentiable spaces]]; the problem is that even if $X$ and $Y$ are exponentiable, the exponential $Y^X$ may not be:

* The category of exponentiable spaces is not cartesian closed. (It is however [[cartesian monoidal category|cartesian]]: the product of two exponentiable spaces under the usual product topology is exponentiable.)

To see this, we recall that a [[Hausdorff space]] is exponentiable if and only if it is [[locally compact space|locally compact]], and that an exponential $Y^X$ (provided it exists) is Hausdorff if $Y$ is. Thus, it is enough to exhibit two locally compact Hausdorff spaces $X$, $Y$ whose exponential is not locally compact.

Take $X = \mathbb{R}$ with its usual topology and $Y = \mathbb{N}$ (the set of [[natural numbers]]) with the [[discrete topology]]. Suppose that an exponential $\mathbb{R}^\mathbb{N}$ exists in the category of locally compact Hausdorff spaces. Then it must be a countable product of copies of $\mathbb{R}$ by the following calculation: 

$$LCH(X \times \mathbb{N}, \mathbb{R}) \cong LCH(\sum_{\mathbb{N}} X, \mathbb{R}) \cong \prod_{\mathbb{N}} LCH(X, \mathbb{R})$$ 

where the last functor in $X$, in order to be [[representable functor|representable]], would have to be represented by a product $\prod_{\mathbb{N}} \mathbb{R}$. Using the universal property of products, one may easily exhibit a scalar multiplication 

$$\mathbb{R} \times \mathbb{R}^{\mathbb{N}} \to \mathbb{R}^{\mathbb{N}}$$ 

rendering $\mathbb{R}^{\mathbb{N}}$ a [[topological vector space]] (a TVS) over the real numbers. But it is well-known that locally compact TVS are finite-dimensional, and we have reached an absurdity. 

Similarly, the topological product $\mathbb{N}^{\mathbb{N}}$ is homeomorphic to [[Baire space of irrational numbers|Baire space]], and this is not locally compact either. 

## "Nice" versus "convenient" categories of spaces
{#NvC}

A related entry is [[nice category of spaces]]. Here we explain the difference between "convenient" and "nice" categories of spaces. 

"A convenient category of topological spaces" is the title of [a well-known paper](#Steenrod) by [[Norman Steenrod]], who emphasized particularly [[function space]] constructions (i.e., cartesian closure) as a great convenience for working algebraic topologists, on top of (generally less problematic) completeness and cocompleteness assumptions. (See also the historical remarks that follow.) 

It is well-known that $Top$ is not [[cartesian closed category|cartesian closed]].  One can characterize the [[exponential law for spaces|exponentiable spaces]], which include all [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] spaces, but as we saw above, the naive idea of simply cutting down to some of these does not give a good cartesian closed category either, since firstly it need not be complete and cocomplete, and secondly even if $X$ and $Y$ are exponentiable, the exponential $Y^X$ need not be.

However, one can cut down to *some* full subcategory of spaces which does admit function spaces.  This typically involves the subtle and delicate interplay between compactness conditions and openness conditions.  It comes at a cost -- that limits and/or colimits in the subcategory might not be computed as they are in $Top$ -- but this is generally considered a very small price to pay in exchange for the great convenience of these assumptions. 

That a convenient category of topological spaces contains all the CW complexes was not explicitly declared by Steenrod, but we feel certain that [[algebraic topology|algebraic topologists]] want these as part of their convenient category. In practice this is a mild assumption, because the usual examples certainly contain all finite topological products of the [[unit interval]] $I$, and are closed under those $Top$-colimits used to present CW complexes, as built inductively from the basic spaces $I^n \cong D^n$. 

"Nice categories of spaces" should be thought of as a wider and vaguer term; it really means the category of spaces has "nice" categorical properties for some mathematical purpose at hand. Certainly any convenient category of spaces should be considered a nice category of spaces for the general purposes of algebraic topology. On the other hand, there are categories of spaces which are not "convenient" in the technical sense described above, but which may be very nice for certain purposes. 

For example, the category of [[compact Hausdorff spaces]] can be considered as being very nice for certain purposes. For instance, it is [[monadic category|monadic]] over $Set$ (!) and a [[pretopos]]. It is, however, not "convenient", as it very far from being cartesian closed. In a different direction, there is the (complete, cocomplete) cartesian closed category of [[equilogical spaces]], but this is not a full subcategory of $Top$, and the core concerns of mathematicians working with equilogical spaces are somewhat different from those of algebraic topologists.

It should also be noted that "[[space]]" itself has a wider meaning than the technical notion of "[[topological space]]", even if topological intuitions come into play. For example, in [[domain theory]], one often considers certain types of [[posets]] (for example, [[directed-complete partial order|dcpos]]) as certain types of "spaces". In this direction, we have that the category of dcpos and [[Scott-continuous map]]s between them forms a complete, cocomplete, cartesian closed category. However, these types of spaces are quite far removed from the traditional concerns of topology, hence are not "convenient" in the sense given above (despite the manifold relations between Scott continuity and the point-set topology which underlies the classical results on compactly generated spaces). In another direction, the category of [[locales]] is in some respects "nice", but these are not topological spaces either. 

Along with the entry on [[nice category of spaces]] and the examples above, see [[Johnstone's topological topos]] and Spanier's [[quasitopological space]]s ([ref](#Spanier)). None of these is convenient in the precise sense above. However there are advantages in having a category which is not only cartesian closed but also locally cartesian closed. In algebraic topology, this has led to Peter Booth's work on "fibred mapping spaces" ([ref](#Booth)), ([ref](#Crabb-Jamea)).  

There are possible advantages in homotopy theory of using a "topological topos", (Johnstone [ref](#Johnstone)), Harasani [ref](#Harasani)). 


## Historical remarks 
 {#HistoricalRemarks}

The phrase "convenient category of topological spaces" predates [Steenrod 1967](#Steenrod67) by a number of years;  [Brown 1963, Introduction](#Brown63) says:

> It may be that the category of Hausdorff $k$-spaces is adequate and convenient for all purposes of topology.

The requirements for convenience were spelled out in [Brown 1964](#Brown64).

In fact, Brown (not Steenrod, as has sometimes been assumed) was the first to prove that Hausdorff [[Kelley space|k-spaces]] (with the "kelleyfied" weakening of the [[compact-open topology|compact--open topology]] on function spaces) formed what is now called a [[cartesian closed category]] (see [Brown 1961](#Brown61)), influenced by [Cohen 1954](#Cohen54).  

Note Brown's work predates the formal introduction of cartesian closed categories in [[Bill Lawvere]]'s thesis by a couple of years; in fact there is clear anticipation in Brown's thesis of the notions of [[closed monoidal category|monoidal closed]] and cartesian closed categories, which was to attract much attention throughout the sixties. Further,  Brown's results  on the topological case are more precise than Steenrod's, since the 1964 paper deals with functions continuous on compact subsets, and for these obtains a homeomorphism without kellyfication. An account of this may be found in the book [Topology and Groupoids](#Brown06).  

Of course, as has often been emphasized by Lawvere, the need for and convenience of considering function spaces is a very old idea in [[geometry]] (going back to the roots of the [[calculus of variations]], for example). The constructions of exponentials of topological spaces via the compact--open topology had been known for a long time; see for example [[John Kelley]]'s _General Topology_ (1955). The relevance of what are today called [[Kelley space]]s (or k-spaces[^1]) had also been recognized; for example, Kelley's book indicates the [[complete space|completeness]] of function spaces (wrt the compact--open topology) when the base is a complete [[uniform space]] and the exponent is a k-space. However, the problem of obtaining a class of spaces _closed_ under function spaces wasn't solved prior to Brown's thesis. Brown also observed the relevance of k-spaces to studies of how products interact with [[quotient space]]s. The general appreciation of the connection between cartesian closure and preservation of quotients under products came with the appreciation of the conceptual simplicity of categorical [[adjunctions]], namely the point that the functor $- \times X$ preserves colimits if it has an exponential right adjoint $(-)^X$. The question also solved in Brown's 1964 paper was to give, in the Hausdorff case,  a left adjoint to  the functor $ (-)^Y $ when the function spaces have the compact-open topology, and so to give a monoidal closed structure on the category of Hausdorff spaces; the generalisation to the non-Hausdorff case is given in the paper of Booth and Tillotson listed below. 

Appreciation of the role of convenient categories was in full force by the early seventies (for a sample, see [[Peter May]]'s _Geometry of Iterated Loop Spaces_, where the category of Hausdorff k-spaces plays a foundational role). The notion of a "convenient category" is recognized elsewhere too (and not just within the categorical and algebraic topology communities); see for example the book by [Kriegl and Michor](#KM). 


[^1]: The '$k$' certainly  refers to 'kompakt' rather than Kelley's initial. 

## Related concepts

* [[compactly generated topological space]]

* [[Delta-generated topological space]], [[D-topological space]]

* [[quasi-topological space]]


## References

The terminology ("convenient category of topological spaces") became widely adopted with

* {#Steenrod67} [[Norman Steenrod]], _A convenient category of topological spaces_, Michigan Math. J. 14 (1967) 133--152 ([euclid:mmj/1028999711](http://projecteuclid.org/euclid.mmj/1028999711))

referring there to the category of *[[compactly generated topological space]]* (see the references [there](compactly+generated+topological+space#Refererences) for more), whose convenient [[cartesian closed category|cartesian closure]] had [previously](#HistoricalRemarks) been highlighted in:

* {#Brown61} [[Ronnie Brown]], _Some problems of algebraic topology: a study of function spaces, function complexes, and FD-complexes_, DPhil thesis, Oxford University, 1961 (Note: the Appendix of this thesis was withdrawn from the examination.)  [(pdf)](https://ora.ox.ac.uk/objects/uuid:3af55800-4be7-462f-b91d-9769a6dac2c4)
 
* {#Brown63} [[Ronnie Brown]], _Ten topologies for $X\times Y$_, Quart. J.Math. (2) 14 (1963), 303--319. ([doi:10.1093/qmath/14.1.303](https://doi.org/10.1093/qmath/14.1.303), [pdf](http://groupoids.org.uk/pdffiles/tentopologies.pdf))

* {#Brown64} [[Ronnie Brown]], _Function spaces and product topologies_,  Quart. J. Math. (2) 15 (1964), 238--250. ([doi:10.1093/qmath/15.1.238](https://doi.org/10.1093/qmath/15.1.238))

influenced, in turn, by:

* {#Cohen54} D. E. Cohen,  _Spaces with weak topology_, Quart. J. Math., (2) 5 (1954) 77&#8211;-80 ([doi:10.1093/qmath/5.1.77](https://doi.org/10.1093/qmath/5.1.77))

Discussion in the generality that subsumes [[compactly generated topological spaces]] and [[Delta-generated topological spaces]] and all cases of subcategory-generated spaces in between:

* {#Vogt71} [[Rainer M. Vogt]], *Convenient categories of topological spaces for homotopy theory*,  Arch. Math 22, 545–555 (1971) ([doi:10.1007/BF01222616](https://doi.org/10.1007/BF01222616))

* {#EscardoLawsonSimpson04} [[Martín Escardó]], [[Jimmie Lawson]], [[Alex Simpson]], Section 3 of: *Comparing Cartesian closed categories of (core) compactly generated spaces*, Topology and its Applications Volume 143, Issues 1–3, 28 August 2004, Pages 105-145 ([doi:10.1016/j.topol.2004.02.011](https://doi.org/10.1016/j.topol.2004.02.011))

* {#Gaucher07} [[Philippe Gaucher]], Section 2 of: *Homotopical interpretation of globular complex by multipointed d-space*, Theory and Applications of Categories, vol. 22, number 22, 588-621, 2009 ([arXiv:0710.3553](https://arxiv.org/abs/0710.3553))



   
See also:

* {#Spanier} [[Edwin Spanier]], _Quasi-topologies_, Duke Mathematical Journal 30 (1) (1963), 1--14.

  > (on [[quasi-topological spaces]])

* {#Booth} Peter I. Booth,  _The exponential law of maps. II._  Math. Z. 121 (1971), 311&#8211;319. 

* {#BT} P. Booth, ; Tillotson, J., _Monoidal closed, Cartesian closed and convenient categories of topological spaces_. Pacific J. Math. 88 (1980), no. 1, 35--53. [project euclid](http://projecteuclid.org/euclid.pjm/1102779712)

* Michael Crabb, [[Ioan James]] ,  _Fibrewise homotopy theory_.   Springer Monographs in Mathematics. Springer-Verlag London, Ltd., London, 1998. viii+341 pp. ISBN: 1-85233-014-7 {#CrabbJames}


* {#Preuss02} Gerhard Preu&#223;, _Foundations of topology: an approach to convenient topology_, Kluwer, Dordrecht/ Boston 2002 ([doi:10.1007/978-94-010-0489-3](https://www.springer.com/gp/book/9781402008917))

  survey in: _Convenient topology --  a new branch of topology_ ([web](http://at.yorku.ca/i/a/a/c/54.htm))


* {#Brown06} [[Ronnie Brown]] _Topology and Groupoids_, Booksurge (2006), available from amazon: Section 5.9: Spaces of functions and the compact-open topology. 

Discussion via [[topos theory]]:

* {#Johnstone} [[Peter Johnstone]], _On a topological topos_, Proc. London Math. Soc. (3) 38 (1979) 237--271.

* Harasani, Hamed A. _Topos theoretic methods in general topology_, PhD Thesis, University of Wales, Bangor, (1988) [(link to pdf files)](http://groupoids.org.uk/harasani.html). {#Harasani}

Analogous considerations for [[diffeological spaces]] (subsuming [[D-topological spaces]])

* {#KM} [[Andreas Kriegl]]; [[Peter Michor]] , _[[The Convenient Setting of Global Analysis]]_, Mathematical Surveys and Monographs, Volume 53. American Mathematical Society, Providence, RI (1997).



[[!redirects convenient category of topological spaces]]
[[!redirects convenient categories of topological spaces]]
[[!redirects conventient category of topological spaces]]

[[!redirects convenient category of spaces]]
[[!redirects convenient categories of spaces]]