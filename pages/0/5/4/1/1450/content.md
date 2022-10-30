
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--



# Contents

* table of contents
{:toc}


## Idea

> Der unendlich kleinste Theil des Raumes ist immer ein Raum, etwas, das Continuit&#228;t hat, nicht aber ein blosser Punct, oder die Grenze zwischen bestimmten Stellen im Raume; ([Fichte 1795, Grundriss, &#167;4.IV](Grundriss+des+Eigenth&#252;mlichen+der+Wissenschaftslehre#4IVUnendlichKleinsterTeilDesRaumes))


In _synthetic differential geometry_ one formulates [[differential geometry]] [[axiom|axiomatically]] in [[toposes]] -- called [[smooth toposes]] --  of [[generalized smooth spaces]] by assuming the explicit existence of [[infinitesimal neighbourhoods]] of points.

The main point of the axioms is to ensure that a well defined notion of [[infinitesimal spaces]] exists in the topos, whose existence concretely and usefully formalizes the wide-spread but often vague intuition about the role of infinitesimals in [[differential geometry]].

In particular, in such toposes $E$ there exists an [[infinitesimal space]] $D$ that behaves like the [[infinitesimal object|infinitesimal interval]] in such a way that for any space $X \in E$ the [[tangent bundle]] of $X$, is, again as an object of the topos, just the [[internal hom]] $T X \;\text{:=}\; X^D$ (using the notation of [[exponential object]]s in the [[cartesian closed category]] $E$). So a tangent vector in this context is literally an _infinitesimal path_ in $X$.

This way, in [[smooth topos]]es it is possible to give precise well-defined meaning to many of the familiar computations -- wide-spread in particular in the [[physics]] literature -- that compute with supposedly "infinitesimal" quantities.

+-- {: .num_remark #SophusLieQuote}
###### Remark

As quoted by [[Anders Kock]] in his first book ([p. 9 ](http://home.imf.au.dk/kock/sdg99.pdf#page=9)), [[Sophus Lie]] -- one of the founding fathers of [[differential geometry]] and, of course [[Lie theory]] -- once said that he found his main theorems in [[Lie theory]] using "synthetic reasoning", but had to write them up in non-synthetic style (see _[[analytic versus synthetic]]_) just due to lack of a formalized language:

> "The reason why I have postponed for so long these investigations, which are basic to my other work in this field, is essentially the following. I found these theories originally by synthetic considerations. But I soon realized that, as expedient ( _zweckm&#228;ssig_ ) the synthetic method is for discovery, as difficult it is to give a clear exposition on synthetic investigations, which deal with objects that till now have almost exclusively been considered analytically. After long vacillations, I have decided to use a half synthetic, half analytic form. I hope my work will serve to bring justification to the synthetic method besides the analytical one." ([[Sophus Lie]], _Allgemeine Theorie der partiellen Differentialgleichungen erster Ordnung_, Math. Ann. 9 (1876).)

=--

Synthetic differential geometry provides this formalized language.

+-- {: .num_remark #Peirce}
###### Remark

Another advocate of the use of infinitesimals in the late 19th century was the American philosopher [[Charles Sanders Peirce]] who also foresaw the role of non-classical logic in such a putative infinitesimal calculus:

> The illumination of the subject by a strict notation for the logic of relatives had shown me clearly and evidently that the idea of an infinitesimal involves no contradiction...As a mathematician, I prefer the method of infinitesimals to that of limits, as far easier and less infested with snares. Charles Sanders Peirce, _The Law of Mind_, The Monist **2** (1892) 

=--

## Axiomatics

The axioms of synthetic differential geometry demand that the [[topos]] $E$ of smooth spaces is 

* a [[smooth topos]] (see there for details)

in which in particular 

* [[infinitesimal space]]s exist and

* satisfy the [[Kock-Lawvere axiom]].

Depending on applications one imposes further axioms, such as the

* [[integration axiom]].

With that little bit of axiomatics alone, a large amount of [[differential geometry]] may be formulated. This has been carried through quite comprehensively by [[Anders Kock]], see the [reference](#References) below. 

In his work he particularly makes use of the fact that as sophisticated as a [[smooth topos]] may be when explicitly constructed (see the section on [models](#models)), being a [[topos]] means that one can reason inside it almost literally as in [[Set]]. Using this Kock's work gives descriptions of synthetic differential geometry which are entirely intuitive and have no esoteric topos-theoretic flavor. All he needs is the assumption that the [[Kock-Lawvere axiom]] is satisfied for "numbers". Here "numbers" is really to be interpreted in the topos, but if one just accepts that they satisfy the KL axiom, one may work with infinitesimals in this context in essentially precisely the naive way, with the topos theory in the background just ensuring that everything makes good sense.


## Models
{#models}

Being axiomatic, reasoning in synthetic differential geometry applies in every **model** for the axioms, i.e. in every concrete choice of [[smooth topos]] $T$.

Models of [[smooth toposes]] tend to be inspired, but more general than, constructions familiar from [[algebraic geometry]]. In particular the old insight promoted by [[Grothendieck]] in his work, that [[nilpotent ideals]] in [[rings]] are formal duals of spaces with infinitesimal extension is typically used to model [[infinitesimal spaces]] in synthetic differential geometry.

See at _[[synthetic differential geometry applied to algebraic geometry]]_ for more on this.

The main difference between models for [[smooth toposes]]  and  [[algebraic geometry]] from this perspective is that models for [[smooth topos]] tend to employ test spaces that are _richer_ than plain formal duals to commutative [[ring]]s or algebras, as in [[algebraic geometry]]: typical models for synthetic differential geometry use test spaces given by formal duals of [[generalized smooth algebras]] that remember "smooth structure" in the usual sense of [[differential geometry]] (and different from, though not entirely unrelated, to the notion of [[smooth scheme]] in algebraic geometry). This is in particular true for the [well adapted models](#wellAdaptedModels).

However, with a a sufficiently general perspective on [[higher geometry]] one finds that algebraic geometry and  synthetic differential geometry are both special cases of a more general notion of theories of generalized spaces. For more on this see [[generalized scheme]].


### Well adapted models
 {#wellAdaptedModels}

A [[topos]] $E$ modelling the axioms of synthetic differential geometry is called **(well) adapted** if the ordinary [[differential geometry]] of [[manifolds]] embeds into it, in particular if there is a [[full and faithful functor]] [[Diff]] $\to E$ from the category of ordinary [[smooth manifold]]s into $E$. 

A standard model for well adapted synthetic toposes is obtained in terms of sheaves on duals of "germ determined" $C^\infty$-rings. This is described in great detail in the textbook _[[Models for Smooth Infinitesimal Analysis]]_. 

The conception and discussion of these well adapted toposes goes back to [[Eduardo Dubuc]], who studied them in a long series of articles. He [asks](http://north.ecc.edu/alsani/ct99-00%288-12%29/msg00218.html) people to refer to this topos as the **[[Dubuc topos]]**. 

This theory of well-adapted models was later summarized and extended in the standard textbook

* [[Ieke Moerdijk]] [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ 



## Variations

### Higher categorical versions

* Synthetic differential geometry may be thought of as embedded in the general theory of [[derived smooth manifolds]] and, generally, that of [[generalized schemes]].

### Supergeometric versions

The notion of synthetic differential geometry extends to the context of [[supergeometry - contents|supergeometry]]. See

* [[synthetic differential supergeometry]].


## Constructions in synthetic differential geometry {#Constructions}

### Tangent bundle

The [[tangent bundle]] of an object $X$ in a [[smooth topos]] is just the [[exponential object]] $T X := X^D$. The unique inclusion ${*} \to D$ induces a canonical projection $T X \to X$. A [[section]] $X \to T X$ of that projection is a [[tangent vector]] on $X$. Its [[adjunct]] is a morphism $D \to X^X$ that sends the unique point of $D$ to the identity $Id_X \in X^X$.

### Differential equation

A [[differential equation]] is an extension problem in a [[smooth topos]] along a morphism that includes an [[infinitesimal object]] into another object.

For instance the ordinary first order homogeneous differential equation that asks the derivative of a function $f : X \to A$ along a [[vector field]] $v : D \to X^X$ to be given by a specified map $\alpha: X \to T A$ is given by a diagram of the form

$$
  \array{
    D &\stackrel{v}{\to}& X^X
    \\
    {}^{\mathllap{\alpha}}\downarrow & \swarrow_{\mathrlap{f}}
    \\
    A^X
  }
  \,,
$$

where we have freely identified morphisms with their [[adjunct]]s. See [[differential equation]] for details.


### Differential forms

A [[differential form|differential 1-form]] is a morphism $\omega : T X \to R$ that is "fiberwise linear". One elegant way to say this is obtained by considering all higher differential forms at once:

for a sufficiently well behaved object $X$ in a [[smooth topos]], there is the [[simplicial object]] which is the [[infinitesimal singular simplicial complex]] $X^{(\Delta^\bullet_{inf})}$ of $X$. Taking functions on this produces the [[cosimplicial algebra]] $Hom(X^{\Delta^\bullet_{inf}}, R)$. Its [[Moore complex|normalized Moore cochain complex]] is isomorphic to the [[de Rham complex|de Rham dg-algebra]] of differential forms on $X$:

$$
  N^\bullet(Hom(X^{(\Delta^{inf}_\bullet)}),R)
  =
  \Omega^\bullet_{dR}(X)
  \,.
$$

This is discussed at

* <a href="http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl">Spaces of infinitesimal k-simplices</a>

* [[differential forms in synthetic differential geometry]].



## Related concepts

* [[synthetic mathematics]]

* [[differential geometry]]

* [[synthetic geometry]]

* [[derived differential geometry]]

* [[D-geometry]]

* [[differential cohesion]]

  * [[synthetic differential infinity-groupoid]]

* [[topos of laws of motion]]

* [[nonstandard analysis]]

## References
{#References}

The idea of axiomatizing [[differential geometry]] using ideas inspired by [[topos]] theory originates in 

* [[Bill Lawvere]], _[[Categorical dynamics]]_, lecture  (Chicago 1967). ([abstract pdf](http://www.mat.uc.pt/~ct2011/abstracts/lawvere_w.pdf))

They were published as pp.1-28 in

* [[Anders Kock]] (ed.), _Topos Theoretic Methods in Geometry_ , Aarhus Univ. Var. Pub. Ser. 30 (1979). {#Kocked79} 
 
The first model for the axioms presented there served to demonstrate that the theory is non-empty, but was hard to work with. Much of the later work was concerned with refining the model-building. For instance

* [[Eduardo Dubuc]], _Sur les mod&egrave;les de la g&eacute;om&eacute;trie diff&eacute;rentielle synth&eacute;tique_, Cahier Top et G&eacute;om. Diff. **XX-3** (1979) pp.231-279. ([pdf](http://archive.numdam.org/article/CTGDC_1979__20_3_231_0.pdf))

These models are constructed in terms of [[sheaf]] [[topos]]es on the category of [[smooth loci]], formal duals to [[generalized smooth algebra|C∞-ring]]s. See there for a detailed list of references.

Transcripts or notes of further talks by Bill Lawvere on the subject are

* [[Bill Lawvere]], _[[Toposes of laws of motion]]_ , transcript of a talk in Montreal, Sept. 1997 ([[LawvereToposesOfLawsOfMotions.pdf:file]])

  (on the description of [[differential equation]]s in terms of synthetic differential geometry)

* [[Bill Lawvere]], _Outline of synthetic differential geometry_ , lectures in Buffalo (1998). ([[LawvereSDGOutline.pdf:file]])

Two articles that exhibit the link to [[continuum mechanics]]:


* [[Bill Lawvere|F. W. Lawvere]], _Toward the description in a smooth topos of the dynamically possible motions and deformations of a continuous body_ , Cah. Top. G&#233;om. Diff. Cat. **21** no.4 (1980) pp.377-392. ([pdf](http://archive.numdam.org/article/CTGDC_1980__21_4_377_0.pdf))

* [[Bill Lawvere|F. W. Lawvere]], _Categorical algebra for continuum microphysics_ , JPAA **175** (2002) pp.267-287.

See also

* [[Marta Bunge]], [[Eduardo Dubuc]], _Archimedian local $C^\infty$-rings and models of synthetic differential geometry_ Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, **XXVII-3** (1986) pp.3-22. ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_3_3_0)).


### Books

A nice elementary introduction which emphasizes calculations and the application as _engineering mathematics_ can be found in

* [[John Bell|John L. Bell]], _A Primer of Infinitesimal Analysis_ , Cambridge UP 1998.

The textbooks 

*  {#KockBookA} [[Anders Kock]], _Synthetic Differential Geometry_, ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

*  {#KockBookB} [[Anders Kock]], _Synthetic geometry of manifolds_, Cambridge Tracts in Mathematics 180 (2010). ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))


develop in great detail the theory of [[differential geometry]] using the axioms of synthetic differential geometry. The main goal in these books is to demonstrate how these axioms lead to a very elegant, very intuitive and very comprehensive conception of differential geometry. Accordingly, concrete models (whose explicit description is typically much more evolved than the nice axiomatics that holds once they have been constructed) play a minor role in these books.

Somewhat complementary to that, the book

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ , Springer Heidelberg 1991.

focuses on concrete constructions of well-adapted models using the technology of [[generalized smooth algebra]]s ($C^\infty$-rings). 

Another textbook is

* R. Lavendhomme, _Basic concepts of synthetic differential geometry_, Kluwer Dordrecht 1996.

### Expositions

For the early French connection see:

* [[André Weil]], _Th&#233;orie des points proches sur les vari&#233;t&#233;s diff&#233;rentiables_ , Colloq. Top. et G&#233;om. Diff., Strasbourg (1953) pp.111-117.

* Jean Penon, _De l'infinit&#233;simal au local (Th&#232;se de Doctorat d'&#201;tat)_ Diagrammes **S13** (1985), pp.1-191. ([pdf](http://archive.numdam.org/article/DIA_1985__S13__1_0.pdf))

Useful introductory expositions of basic ideas of synthetic differential geometry are

*  [[Mike Shulman]], _Chicago Pizza-Seminar: Synthetic Differential Geometry_ ([pdf](http://home.sandiego.edu/~shulman/papers/sdg-pizza-seminar.pdf))

*  [[John Bell]], _An invitation to smooth infinitesimal analysis_ ([pdf](http://publish.uwo.ca/~jbell/invitation%20to%20SIA.pdf))

* R. P. Kostecki, _Differential Geometry in Toposes_ , ms. University of Warsaw (2009). ([pdf](http://www.fuw.edu.pl/~kostecki/sdg.pdf))