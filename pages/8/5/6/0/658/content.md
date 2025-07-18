+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Contents#
* table of content
{:toc}

## Idea

The concept of _profunctor_ is a generalization of the concept of [[functor]] in much the same way that the concept of [[bimodule]] generalizes that of [[associative algebra|algebra]] [[homomorphism]] (in fact, this may be understood as a special case of enriched profunctors).

## Definition ##

If $C$ and $D$ are [[categories]], then a **profunctor** from $C$ to $D$ is a [[functor]] of the form

$$
  H_F \colon D^{op}\times C \to Set
  \,.
$$

Such a  profunctor is usually written as $F\colon  C $&#8696;$ D$. For $d \in D$ and $c \in C$ the set $H_F(d,c)$ is also called the set of [[heteromorphisms]] from $d$ to $c$.

Every [[functor]] $f\colon C\to D$ induces two profunctors $D(1,f)\colon C $&#8696;$ D$ and $D(f,1)\colon D $&#8696;$ C$, defined by $D(1,f)(d,c) = D(d,f(c))$ and $D(f,1)(c,d) = D(f(c),d)$. (Here $D(-,-)$ denotes the [[hom functor]] of $D$ and $1$ denotes the identity functor on the respective category.) Since this construction may be thought of as the [[adjunct]] of the composition of $f$ with the [[Yoneda embedding]] $C \stackrel{f}{\longrightarrow} D \stackrel{Yoneda}{\longrightarrow} [D^{op},Set]$, these profunctors are called *representable* (or sometimes one of them is called *corepresentable*) and this way profunctors subsume and generalize ordinary functors.

In particular the identity profunctor $Id \colon  C $&#8696;$ C$ is represented by the identity functor and hence is given by the [[hom-functor]] $C(-,-) : C^{op} \times C \to Set$ itself.

The notion generalizes to many other kinds of categories.  For instance, if $C$ and $D$ are [[enriched category|enriched]] over some symmetric [[closed monoidal category]] $V$, then a profunctor from $C$ to $D$ is a $V$-functor $D^{op} \otimes C\to V$.  If they are [[internal categories]], then a profunctor $C $&#8696;$ D$ is an [[internal diagram]] on $D^{op}\times C$, and so on.  There are also other equivalent definitions in each case; see below.

A profunctor is also sometimes called a **[[bimodule|(bi)module]]** or a **distributor** or a **relator** or a **correspondence**, though the latter word is also used for a [[span]].  The term "module" tends to be common in Australia, especially in the enriched case; here the intuition is that for one-object $V$-categories, i.e. monoids in $V$, profunctors really are the same as [[bimodules]] between such monoids in the usual sense.  "Profunctor" is perhaps more common in the Set-based and internal cases (but is also used in the enriched case); here the intuition is that a profunctor is a generalization of a functor, via the construction of "representable" profunctors.  Jean B&#233;nabou, who invented the term and originally used "profunctor," later preferred "distributor". One reason for this is that lax functors from a given category to the bicategory of distributors give a notion of "distribution on a category", formally resembling [[distributions]] qua generalized [[functions]] - see [Bénabou 95](#Benabou95).

Note that the convention that a profunctor is a functor $D^{op}\times C \to Set$ is not universal; some authors reverse $C$ and $D$ and/or put the "op" on the other one.  See the discussion below.


## The bicategory of profunctors

Profunctors are composed by using a [[coend]] to "trace out" the middle variable.  Specifically, for profunctors $F : C $&#8696;$ D$ and $G : D $&#8696;$ E$, their composite $G \circ F: C $&#8696;$ E$ is defined to be

$$
  (G \circ F)(e,c) := \int^{d \in D} F(d,c)\otimes G(e,d)
  \,.
$$

This yields a [[bicategory]] in which

* [[objects]] are [[small categories]],

* [[morphism]]s are profunctors with the above composition, and

* [[2-morphisms]] are [[natural transformation]]s.

This bicategory is variously denoted [[Prof]], $Mod$, or $Dist$, according to one's chosen name for profunctors.  In the $V$-enriched case, it is written $V Prof$ or $V Mod$ or $V Dist$.

The construction of the "representable" profunctors $D(1,f)$ and $D(f,1)$ from a functor $f\colon C\to D$ yield two identity-on-objects functors $Cat \to Prof$ and $Cat^{op}\to Prof$.  Moreover, it is easy to check that $D(1,f) \vdash D(f,1)$ in the bicategory $Prof$; thus $Cat\to Prof$ is a [[proarrow equipment]] in the sense of Wood (in fact, the prototypical one).  This same fact can also be expressed by defining a (pseudo) [[double category]] in which functors and profunctors are the two kinds of arrows; the construction of representable profunctors is then given by [[companion]]s and [[conjoint]]s in this double category, which make it a [[framed bicategory]], hence an equivalent representation of a proarrow equipment.

The [[full sub-2-category]] $Prof_{rep}$ on representable profunctors is equivalent to $Cat_{ana}$, the 2-category of [[anafunctor]]s. See there for more details.

## Alternative definitions ##


### In terms of colimit-preserving functors on presheaf categories {#FuncsOnPresheaves}

A basic fact (e.g. Kashiwara, Schapira, [[Categories and Sheaves]], corollary 2.7.4, page 63) is that for $A$ a [[cocomplete category]], [[cocontinuous functor|colimit-preserving functors]] from [[presheaf|presheaves]] on some small category $C$ to $A$ are canonically equivalent to functors from $C$ to $A$: we have an equivalence of [[functor category|functor categories]]

$$
 Cocont(PSh(C),A)
 \simeq
  Func(C,A)
  \,.
$$

This may be thought of as a consequence of the [[co-Yoneda lemma]] (and hence, of course, of the [[Yoneda lemma]]) which says that every presheaf is a colimit over [[representable functor|representables]], i.e. over objects in the image of the [[Yoneda embedding]] $Y : C \to PSh(C)$. This immediately implies that a colimit-preserving functor on $PSh(C)$ is already determined by its restriction along $Y$ to $C$.

Now, profunctors $D^{op} \otimes C \to V$ are [[adjunct]] to functors $C \to [D^{op}, V] \simeq PSh(D)$. Hence by the above, profunctors are equivalent to colimit-preserving functors

$$
  PSh(C) \to PSh(D)
  \,.
$$

Indeed, there is an equivalence of bicategories between $V Prof$ and the 2-category of categories and colimit-preserving functors and natural transformations between their presheaf categories.  Note that the latter is a [[strict 2-category]] which can thus serve as a "natural" strictification of $V Prof$ (e.g. [Cattani 1999, Prop. 4.2.4](#Cattani99)).


From this perspective, the representable profunctor induced by an ordinary $V$-functor $f : C \to D$ is 
the [[adjunct]] of the postcomposition 
$$
  C \stackrel{f}{\to} D \stackrel{Y}{\to} [D^{op},V]
$$
with the [[Yoneda embedding]] under the Hom-adjunction.

The formulation of profunctors as colimit-preserving functors on presheaf categories plays a big role also in the context of [[(∞,1)-categories]]. A [[presentable (∞,1)-category]] is one equivalent to a [[localization]] of some [[(∞,1)-category of (∞,1)-presheaves]] (i.e. some [[reflective (∞,1)-subcategory]] of the latter). The collection of all [[presentable (∞,1)-categories]] and colimit-preserving [[(∞,1)-functors]] betweem them forms the [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]], whose [[tensor product]] is the "bilinear" tensor product coming from interpreting colimit-preserving functors as "linear" (reading: colimit $\sim$ sum).

This $(\infty,1)$-category $Pr^L$ therefore is an $(\infty,1)$-analog of $Set\text{-}Mod$. In [[geometric ∞-function theory]] one finds (see section 4 there) that morphisms in $Pr^L$ encode the "correspondence operations" such as Fourier-Mukai and its generalizations. See in that context also the examples below.


### In terms of two-sided discrete fibrations

Recall that a functor $D^{op}\to Set$ can equivalently be described as a [[discrete fibration|discrete]] [[(Grothendieck) fibration]], and similarly a functor $C\to Set$ can be described as a discrete opfibration.  Thus, a profunctor $D^{op}\times C\to Set$ could be described by a discrete opfibration over $D^{op}\times C$, or a discrete fibration over $D\times C^{op}$, but there is also a more directly "two-sided" fibrational description.  A *[[two-sided fibration]]* from $C$ to $D$ is a functor $E\to C\times D$ which is a fibration over $D$ and an opfibration over $C$ in a compatible way.  Such a fibration represents a pseudofunctor $D^{op}\times C\to Cat$, and hence if it is discrete it represents a profunctor $D^{op}\times C\to Set$.

This definition/characterization of profunctors works for internal categories as well, but *not* for enriched ones.  It is sometimes called the [[graph of a profunctor]] (although this is sometimes also used for the other fibrational representations mentioned above).


### In terms of two-sided codiscrete cofibrations

Yet another way of representing profunctors is via their [[collages]], also called [[cograph of a profunctor|cographs]].  The collage of a profunctor $H\colon C$&#8696;$ D$ is, in particular, a category $\bar{H}$ equipped with functors $C\to \bar{H}$ and $D\to\bar{H}$ which are [[fully faithful functor|fully faithful]] and jointly bijective on objects.

In fact, the objects of the [[undercategory]] $(C\sqcup D)/Cat$ which are collages of profunctors $C$&#8696;$D$ can be characterized, up to equivalence, as the two-sided [[codiscrete cofibrations]], i.e. the two-sided discrete fibrations in $Cat^{op}$.  In simpler and more explicit language, these are the categories $M$ which contain $C$ and $D$ as disjoint full subcategories which are jointly-[[wide subcategory|wide]] (i.e. together contain all the objects), and such that there are no morphisms from an object of $C$ to an object of $D$.  Equivalently, they are the categories which admit a functor to the [[interval category]] $I$ such that $D$ is the fiber over $0$ and $C$ is the fiber over $1$.

When viewing a profunctor $H\colon C$&#8696;$D$ in this way, one may sometimes speak of elements of $H(d,c)$ as *heteromorphisms* from $d$ to $c$, since they are morphisms in the category $\bar{H}$ and can be "composed" with morphisms of $C$ and $D$ (this corresponds to the "action" of $C$ and $D$ on $H$ in the other formulations), but they go between objects of two different categories (namely $C$ and $D$).

This characterization works just as well in both the internal and enriched case.  Perhaps surprisingly, it also tends to give the "right" notion of profunctor starting with many other, even more exotic, 2-categories.  However, it is trickier to figure out how to define the composite of profunctors viewed as codiscrete cofibrations; see [[codiscrete cofibration]].

### Comparing fibrations and cofibrations

If $C \overset{g}{\to} \bar{H} \overset{f}{\leftarrow} D$ is a codiscrete cofibration representing a profunctor $H$ from $C$ to $D$, then the two-sided discrete fibration representing the same profunctor can be obtained as the [[comma category]] $(f\downarrow g)$ with its two projections to $C$ and $D$.

Dually, if $C \overset{p}{\leftarrow} E \overset{q}{\to} D$ is a two-sided discrete fibration representing a profunctor from $C$ to $D$, then the codiscrete cofibration representing the same profunctor can be obtained as the [[cocomma object]] $(q\uparrow p)$ with the two inclusions of $C$ and $D$.

In fact, in any 2-category with comma and cocomma objects, we have an [[adjunction]]
$$ cocomma: Span(C,D) \;\rightleftarrows\; Cospan(C,D) : comma. $$
One can show that comma objects are always discrete fibrations, and dually cocomma objects are always codiscrete cofibrations.  In $Cat$ and other similar 2-categories, this adjunction is [[idempotent adjunction|idempotent]] and restricts to an equivalence between the categories of discrete fibrations and codiscrete cofibrations (both of which are of course equivalent to the category of profunctors from $C$ to $D$).  This is a two-sided version of the [[Grothendieck construction]].

### In terms of spans

A profunctor $F$ between $C$ and $D$ can also be viewed as a span $C_0 \leftarrow F_1 \rightarrow D_0$ that is compatible with composition in $C$ and $D$ in an appropriate way. This formulation falls out from the definition of a category as a [[monad]] in the [[bicategory]] (more generally [[double category]]) [[Span]] and defining a profunctor to be a [[module over a monad|bimodule]]. The formulation in terms of double categories can be used to produce the appropriate notion of both enriched and internal profunctors.

## Examples ##

* Recall that a one-object [[Vect]]-[[enriched category]] is just an [[algebra]], while a general [[Vect]]-[[enriched category]] is an [[algebroid]]. The full sub-bicategory of $Vect\Mod$ on one-object $Vect$-enriched categories is the familiar category of [[algebras]], [[bimodules]] and bimodule homomorphisms.  In this case, the "representable" profunctors correspond to the way in which every morphism $A \to B$ of [[algebras]] induces the $A$-$B$ bimodule which as a vector space is $B$ with obvious right $B$ action and left $A$-action induced by first mapping $A$ to $B$ via $f$ and then using multiplication in $B$.

* The full sub-bicategory of $Set Prof$ on [[discrete category|discrete categories]] is the bicategory of sets, [[spans]] of sets and morphisms of spans:
  $$
    Set\Mod_{disc} \simeq Span(Set) 
    \,.
  $$

  In particular a [[relation]] between sets is a special case of this. From this point of view the 2-category [[Prof]] of profunctors is a [[categorification]] of the category [[Rel]] of sets and relations.

  Moreover, the representable profunctor between discrete category induced by a [[function]] $f : C \to D$ of sets is the span
  $$
  \array{
    && C
    \\
    & {}^{Id}\swarrow && \searrow^{f}
    \\
    C &&&& D
  }
  \,.
  $$

* Similarly, the full sub-bicategory of internal profunctors in $S = (Set^{op}, \times)$ on "discrete categories" is the bicategory of [[cospans]]
  $$
  Set^{op}\Mod_{disc} \simeq Span(Set^{op}) = Cospan(Set) 
  \,.
  $$

* for [[enriched category|enrichment]] over a [[category of chain complexes]] an [[enriched category]] is a [[dg-category]] and a profunctor is now a dg-[[bimodule]] of dg-categories. This appears notably in the definition of [[noncommutative motives]].

## Properties
 {#Properties}

* If a [[functor]] represents a given profunctor, then the action of the functor on morphisms is determined by the action of the profunctor and the representation isomorphism. For details see at _[[representability determines functoriality]]_

* If $\mathcal{D}$ is [[Cauchy complete category|Cauchy complete]], then the profunctors that correspond to functors (via Yoneda, which here looks like $F\mapsto F_*$, with $F_*(d,c)=\mathcal{D}(d,F c)$) are exactly those that admit right adjoints.  In general, right adjoint profunctors correspond to functors into the [[Cauchy complete category#InOrdinaryCatTheoryByProfunctors|Cauchy completion]] of their codomain.

## Related entries ##

* [[module]]

* [[2-vector space]]

* [[double profunctor]]

* [[nucleus of a profunctor]]

* [[Mealy morphism]]

## References ##


Original articles:

* [[Maren Justesen]], *Bikategorien af Profunktorer*, Aarhus 1968 ([pdf](https://ncatlab.org/nlab/files/Justesen_Profunktoren.pdf))

* [[Marta Bunge]], Chapter 3 of: _Categories of Set-Valued Functors_, University of Pennsylvania, 1966

  > based on suggestions by [[Bill Lawvere]]

* [[Michel André]], _Categories of Functors and Adjoint Functors_, Batelle Institute at Geneva, 1964, see also _Categories of Functors and Adjoint Functors_,American Journal of Mathematics, Vol. 88, No. 3 (Jul., 1966), pp. 529-543 

* {#Benabou73} [[Jean Bénabou]], *Les distributeurs*, Université Catholique de Louvain, Institut de Mathématique Pure et Appliquée,  rapport **33** (1973) &lbrack;[pdf](http://www.entretemps.asso.fr/maths/DistributeursLouvain.pdf), [[Benabou-LesDistributeurs.pdf:file]]&rbrack;

  > (including discussion of [[enriched category|enriched]] and [[internal category|internal]] profunctors)


Some of these ideas were exposed at Oberwolfach in 1966. There are extant notes taken by [[Anders Kock]] of a talk by [[Bill Lawvere]], but there is only a passing mention of 'generalised functors' (what are now called profunctors) and their 'generalised matrix multiplication'.

Texbook account:

* [[Francis Borceux]], Sec. 7.7 _[[Handbook of Categorical Algebra]] I_, Cambridge UP 1994. 

Lecture notes:

* {#Bénabou00} [[Jean Bénabou]] (notes by [[Thomas Streicher]]), *Distributors at Work*, lectures given at TU Darmstadt (2000) &lbrack;[pdf](http://www.mathematik.tu-darmstadt.de/~streicher/FIBR/DiWo.pdf), [[Benabou-DistributorsAtWork.pdf:file]]&rbrack;

Exposition:

* [[John Baez]], _Re: Klein 2-Geometry VII_ ([blog](http://golem.ph.utexas.edu/category/2006/11/klein_2geometry_vii.html#c005985))


A nice example of profunctors between Lawvere [[metric spaces]] can be found in [this comment](http://golem.ph.utexas.edu/category/2009/11/equipments.html#c029633).


The following classic paper is a good appetizer

* [[William Lawvere]], _Metric Spaces, Generalized Logic, and Closed Categories_ , Rendiconti di Seminario mat&#233;matico e fisico di Milano XLIII (1973) pp.135-166. Reprinted in TAC Reprints no.1 (2002) pp.1-37. ([tac](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html))

See the [[joyalscatlab:HomePage|Joyal's CatLab]] for the theory of [[Set]]-valued distributors:

* [[André Joyal]], _[[joyalscatlab:Distributors and barrels]]_ .

Internal profunctors are considered in 

* [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint Minneola 2014; sect. 2.4)

* [[Peter Johnstone]], _Sketches of an [[Elephant]] I_, Oxford UP 2002. (pp.359-367)

The relation to [[locally presentable categories]] is almost explicit in:

* {#Cattani99} [[Gian Luca Cattani]], *Presheaf Models for Concurrency*, PhD thesis from [[BRICS]], University of Aarhus (1999) &lbrack;[pdf](http://www.brics.dk/DS/99/1/BRICS-DS-99-1.pdf), [[Cattani_PresheafModels.pdf:file]]&rbrack;


Profunctors play an important in categorical [[shape theory]]. The original source is 

* [[Dominique Bourn]], [[Jean-Marc Cordier]], _Distributeurs et th&#233;orie de la forme_, Cah. Top. G&#233;om. Diff. Cat. **21** no.2 (1980) pp.161-189. ([numdam:CTGDC_1980__21_2_161_0](http://www.numdam.org/item/CTGDC_1980__21_2_161_0), [pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1980__21_2/CTGDC_1980__21_2_161_0/CTGDC_1980__21_2_161_0.pdf))

The material together with a general discussion of profunctors is also available in English in the reprinted monograph

* J.-M. Cordier , [[Tim Porter]], _Shape Theory: Categorical Methods of Approximation_ , (1989), Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).

Discussion of simplicial enriched profunctors in the context of strong shape theory in

* [[Michael Batanin]], _Categorical Strong Shape Theory_, Cah. Top. G&#233;om. Diff. Cat. **38** no.1 (1997) pp.3-66. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1997__38_1/CTGDC_1997__38_1_3_0/CTGDC_1997__38_1_3_0.pdf))

Overview and application in [[computer science]]:

* [[Gian Luca Cattani]], G. Winskel, _Profunctors, Open Maps, and Bisimulation_ , [[BRICS]] Report **04-22** (2004) &lbrack;[pdf](http://www.brics.dk/RS/04/22/BRICS-RS-04-22.pdf)&rbrack;


The common generalization of [[bimodules]] and [[spans]] in terms of profunctors has been discussed on the blog at

* [[John Baez]], _Bimodules versus spans_ ([blog](http://golem.ph.utexas.edu/category/2008/08/bimodules_versus_spans.html))

Distributions on a category as lax functors into the category of distributors are sketched in the abstract:

* {#Benabou95} [[Jean Bénabou]], _Distributions and 2-descent_, (1995), [pdf](https://oda.mfo.de/themes/MFO/vendor/pdfjs-dist-viewer-min/build/minified/web/viewer.html?file=https://oda.mfo.de/bitstream/handle/mfo/102/full-text.pdf#page=275)

## Notation ## {#notation}

Profunctors are often notated with a slashed or barred arrow, as in $C$&#8696;$D$, which is U+21F8 in Unicode.  It is not always obvious how to draw this character, so here are some hints.

* On the nLab (or anywhere that accepts SGML character entities, including raw HTML on the web), it can be found using a Unicode entity:

      &#8696;

* In LaTeX, one can use `\nrightarrow` (producing '$\nrightarrow$') in a pinch, but a nice-looking extensible barred arrow command `\xslashedrightarrow` can also be produced with the following preamble code (modified from amsmath's `\xrightarrow`).  It requires the packages `amsmath` and `mathtools` to be loaded.

      <nowiki>\makeatletter
      \def\slashedarrowfill@#1#2#3#4#5{%
        $\m@th\thickmuskip0mu\medmuskip\thickmuskip\thinmuskip\thickmuskip
        \relax#5#1\mkern-7mu%
        \cleaders\hbox{$#5\mkern-2mu#2\mkern-2mu$}\hfill
        \mathclap{#3}\mathclap{#2}%
        \cleaders\hbox{$#5\mkern-2mu#2\mkern-2mu$}\hfill
        \mkern-7mu#4$%
      }
      \def\rightslashedarrowfill@{%
        \slashedarrowfill@\relbar\relbar\mapstochar\rightarrow}
      \newcommand\xslashedrightarrow[2][]{%
        \ext@arrow 0055{\rightslashedarrowfill@}{#1}{#2}}
      \makeatother
      </nowiki>

  The command `\xslashedrightarrow` can then be used with one required argument and one optional argument, just like `\xrightarrow`.  A version taking no arguments can of course be defined with

      \def\slashedrightarrow{\xslashedrightarrow{}}

  A simpler barred arrow taking no arguments can be created with

      \def\slashedrightarrow{\relbar\joinrel\mapstochar\joinrel\rightarrow}

* In Xypic, a barred arrow (to the right, in this example) can be produced with

      \ar[r]|-@{|}




[[!redirects profunctors]]
[[!redirects distributor]]
[[!redirects distributors]]
[[!redirects relator]]
[[!redirects relators]]
[[!redirects representable profunctor]]
[[!redirects representable profunctors]]

[[!redirects internal profunctor]]
[[!redirects internal profunctors]]

[[!redirects enriched profunctor]]
[[!redirects enriched profunctors]]



