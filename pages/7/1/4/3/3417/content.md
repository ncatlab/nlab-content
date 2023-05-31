
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Depending on the chosen [[model category]] structure, the [[category]] [[sSet]] of [[simplicial set]]s may model [[∞-groupoids]] (for the standard [[model structure on simplicial sets]]) or [[(∞,1)-categories]] in the form of [[quasi-categories]] (for the [[Joyal model structure]]) on [[SSet]].

Accordingly, there are [[model category]] structures on [[sSet-categories]] that similarly model [[(n,r)-categories]] with $r$ shifted up by 1:

* there is a model structure on $SSet$-enriched categories whose fibrant objects are [[∞-groupoid]]/[[Kan complex]]-enriched categories and which models [[(∞,1)-categories]];

This we discuss [below](ModelForInfinityCategories).

* there is another model structure on [[sSet-categories]] whose fibrant objects are [[(∞,1)-category]]/[[quasi-category]]-enriched categories, and which model [[(∞,2)-categories]]. 

  For more on this see [elsewhere](%28infinity%2C2%29-category#TotMod)

Both are special cases of a [[model structure on enriched categories]].


## Model for $(\infty,1)$-categories
 {#ModelForInfinityCategories}

Here we describe the model category structure on [[SSet Cat]] that  makes it a model for the [[(∞,1)-category of (∞,1)-categories]].

\begin{definition}\label{DwyerKanEquivalences}
**(Dwyer-Kan equivalences)**
\linebreak
An [[sSet]]-[[enriched functor]] $F : C \to D$ between [[sSet-categories]] is called a **weak equivalence** precisely if

* it is *essentially surjective* in that the induced functor of [[homotopy categories]] is an ordinary [[essentially surjective functor]];

* it is an $\infty$-[[full and faithful functor]] in that for all objects $x,y \in C$ the morphism

  $$
    F_{x,y} : C(x,y) \to D(F(x), F(y))
  $$

  is a weak equivalence in the standard [[model structure on simplicial sets]].

\end{definition}

This notion is due to [Dwyer & Kan (1980 FuncComp), §2.4](#DwyerKan80FunctionComplexes) and now known as *[[Dwyer-Kan equivalences]]*.



+-- {: .num_prop}
###### Proposition

A [[Quillen equivalence]] $D \leftrightarrows C$ between [[model categories]] induces a Dwyer-Kan-equivalence $L C \leftrightarrow L D$ between their [[simplicial localizations]].

=--

This is made explicit in [Mazel-Gee 15, p. 17](#MazelGee15) to follow from [Dwyer & Kan 80, Prop. 4.4 with 5.4](#DwyerKan80FunctionComplexes).

The analogous statement under further passage to [[model structure on quasi-categories|Joyal equivalences]] of [[quasi-categories]] is [Lurie (2009), Cor. A.3.1.12](#Lurie09), under the additional assumptions that the model categories are [[simplicial model category|simplicial]], that every object of $C$ is [[cofibrant object|cofibrant]] and that the right adjoint is an sSet [[enriched functor]].


 
+-- {: .num_prop #BergnerModelStructure}
###### Proposition

The category [[SSet Cat]] of [[small category|small]] [[sSet-enriched categories]] carries the structure of a [[model category]] with

* [[weak equivalences]] the [[Dwyer-Kan equivalences]] (Def. \ref{DwyerKanEquivalences});

* [[fibrations]] those [[sSet]]-[[enriched functors]] $F \colon C \to D$ such that

  1. for all $x, y \in C$ the morphism $F_{x,y} \colon C(x,y) \to D\big(F(x), F(y)\big)$ is a fibration in the [[classical model structure on simplicial sets]];

  1. the induced functor $\pi_0(F) \colon Ho(C) \to Ho(D)$ on [[homotopy categories]] is an [[isofibration]].

=--

&lbrack;[Bergner (2004)](#Bergner04), [Lurie (2009), thm. A.3.2.4](#Lurie09)&rbrack;

+-- {: .num_remark}
###### Remark

In particular, the [[fibrant objects]] in this model structure are the [[Kan complex]]-[[enriched categories]], i.e. the strictly [[∞-groupoid]]-enriched ones (see *[[(n,r)-category]]*).

=--

\begin{proposition}
\label{DKBCofibrationsAreInParticularHomSpaceWiseMonos}
The [[cofibrations]] in the Dwyer-Kan-Bergner model structure (Prop. \ref{BergnerModelStructure}) are in particular [[hom-object]]-wise cofibrations in the [[classical model structure on simplicial sets]], hence [[hom-object]] wise [[monomorphism]] of [[simplicial sets]]:
$$
  \left.
  \begin{array}{l}
    \mathbf{D}, \, \mathbf{C} \,\in\, sSet\text{-}Cat,
    \\
    F \colon \mathbf{D} 
     \underset{\in Cof_{DKB}}{\longrightarrow} \mathbf{C},
    \\
    X,Y \,\in\, \mathbf{D}
  \end{array}
  \;\;\;
  \right\}
  \;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;
  F_{X,Y} 
    \colon 
  \mathbf{D}(X,Y) 
    \underset{\in Cof_{KQ}}{\hookrightarrow}  
  \mathbf{C}\big(F(X), F(Y)\big)
  \,.
$$
\end{proposition}
&lbrack;[Lurie (2009), Rem. A.3.2.5](#Lurie09)&rbrack;



## Properties

### Further model category properties

+-- {: .num_prop #RightProperness}
###### Proposition

The Bergner model structure of prop. \ref{BergnerModelStructure} is a [[proper model category]].

=--

A reference for right properness is ([Bergner 04, prop. 3.5](#Bergner04)). A reference for left properness is ([Lurie, A.3.2.4](#Lurie09)) and ([Lurie, A.3.2.25](#Lurie09)).

\begin{remark}\label{FailureOfCartesianClosedModelStructure}
**(failure of cartesian closed model structure)**
\linebreak
  While the [[underlying]] category [[VCat|$sSet Cat$]] of [[sSet-enriched categories]] is [[cartesian closed category|cartesian closed]] (on general grounds, see [here](category+of+V-enriched+categories#MonoidalStructure), also cf. [Joyal (2008), §51.2](#Joyal2008)), the construction of [[enriched product category|$sSet$-enriched product categories]] and [[enriched functor categories|$sSet$-enriched functor categories]] does *not* make the Bergner model structure of prop. \ref{BergnerModelStructure} into a [[monoidal model category]] hence *not* into a [[cartesian closed model category]].

This is in contrast to the [[model structure on quasi-categories]] (see [there](model+structure+for+quasi-categories#CartesianMonoidalModelStructure)) to which the Bergner structure is [[Quillen equivalence|Quillen equivalent]] (see [below](#RelationToQuasiCategories)).
\end{remark}


### Relation to simplicial groupoids
 {#RelationToSimplicialGroupoids}


\begin{proposition}
The canonical inclusion functor
$$
  \iota 
    \,\colon\, 
  sSet\text{-}Grpd
   \xhookrightarrow{\phantom{--}}
  sSet\text{-}Cat
$$   
of the category of [[sSet]]-[[enriched groupoids]] (aka *Dwyer-Kan [[simplicial groupoids]]*) into that of [[sSet-enriched categories]] 

1. has a [[left adjoint]], given degreewise by the [[free groupoid]]-construction ([[localization of a category|localization]] at the class of all morphisms)

1. evidently preserves fibrations and weak equivalences between the above Bergner-model structure (Prop. \ref{BergnerModelStructure})
and the Dwyer-Kan [[model structure on simplicial groupoids]]
 
hence we have a [[Quillen adjunction]]:
$$
  sSet\text{-}Grpd_{DK}
  \underoverset
     {\underset{\iota}{\hookrightarrow}}
     {\overset{F}{\longleftarrow}}
     {\;\;\; \bot_{\mathrm{Qu}} \;\;\;}
  sSet\text{-}Cat_{Berg}
  \,.
$$
\end{proposition}

(see also [Minichiello, Rivera & Zeinalian (2023), Prop. 2.8](model+structure+on+simplicial+groupoids#MinichielloRiveraZeinalian23))


### Relation to quasi-categories
 {#RelationToQuasiCategories}

The operations of forming [[homotopy coherent nerves]], $N$, and of [[rigidification of quasi-categories]], $\mathfrak{C}$, constitute a [[Quillen equivalence]] between the Bergner model structure on $sSet Cat$ (Prop. \ref{BergnerModelStructure}) and the [[model structure for quasi-categories]]. 

For more see at *[[relation between sSet-enriched categories and quasi-categories]]*.


## Related concepts

* [[model structure on simplicial groupoids]]

* [[model structure for quasi-categories]]

* [[relation between quasi-categories and simplicial categories]]

* [[simplicial localization]]

[[!include table - models for (infinity,1)-operads]]


## References


A model category structure on the category of $sSet$-categories with a fixed collection of objects was first given in:

* {#DwyerKan1980Localizations} [[William Dwyer]], [[Daniel Kan]],  §7.1 in: *Simplicial localizations of categories*, J. Pure Appl. Algebra **17** 3 (1980), 267-284 &lbrack;<a href="https://doi.org/10.1016/0022-4049(80)90049-3">doi:10.1016/0022-4049(80)90049-3</a>&rbrack;

The notion of what is now called *[[Dwyer-Kan equivalences]]* appears in

* {#DwyerKan80FunctionComplexes} [[William Dwyer]], [[Daniel Kan]], §2.4 in: _Function complexes in homotopical algebra_, Topology 19 (1980), 427-440 &lbrack;<a href="https://doi.org/10.1016/0040-9383(80)90025-7">doi:10.1016/0040-9383(80)90025-7</a>, [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/dwyer-kan-3.pdf)&rbrack;

Dywer, Spalinski and later [[Charles Rezk|Rezk]] then pointed out that there ought to exist a model category structure on the collection of all $sSet$-categories that models the [[(∞,1)-category of (∞,1)-categories]]. This was then constructed in:

* {#Bergner04} [[Julie Bergner]], *A model category structure on the category of simplicial categories*,  Trans. Amer. Math. Soc. **359** (2007) 2043-2058 &lbrack;[arXiv:0406507](http://arxiv.org/abs/math/0406507), [doi:10.1090/S0002-9947-06-03987-0](https://doi.org/10.1090/S0002-9947-06-03987-0)&rbrack;

Also:

* {#Lurie09} [[Jacob Lurie]], Section A.3.2 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf)&rbrack;

* [[Jacob Lurie]], _$(\infty,2)$-categories and the Goodwillie calculus_, [GoodwillieI.pdf](http://www.math.harvard.edu/~lurie/papers/GoodwillieI.pdf)

Survey and review:

* [[Julie Bergner]], Section 3 of: _A survey of $(\infty,1)$-categories_ ([arXiv:math/0610239](http://arxiv.org/abs/math/0610239))

* [[Emily Riehl]], Section 16 of: _[[Categorical Homotopy Theory]]_, Cambridge University Press, 2014 ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457))

See also

* {#Joyal2008} [[André Joyal]], *Notes on quasi-categories* (2008) &lbrack;[pdf](http://www.math.uchicago.edu/~may/IMA/Joyal.pdf), [[JoyalNotesOnQuasiCategories.pdf:file]]&rbrack;



* {#MazelGee15} [[Aaron Mazel-Gee]], _Quillen adjunctions induce adjunctions of quasicategories_, New York Journal of Mathematics Volume 22 (2016) 57-93 ([arXiv:1501.03146](https://arxiv.org/abs/1501.03146), [publisher](http://nyjm.albany.edu/j/2016/22-4.html))



Recall the slight but crucial difference between the two notions of "[[simplicial categories]]", the other being an [[internal category]] in [[sSet]]. But also for this latter concept there is a [[model category]] structure which presents [[(infinity,1)-categories]], see

* {#Horel14} [[Geoffroy Horel]], _A model structure on internal categories_, Theory and Applications of Categories, Vol. 30, 2015, No. 20, pp 704-750 ([arXiv:1403.6873](http://arxiv.org/abs/1403.6873)).


[[!redirects model structure on SSet-categories]]

[[!redirects model structure on sSet-enriched categories]]
[[!redirects model structure on SSet-enriched categories]]

[[!redirects model structure on simplicial categories]]
[[!redirects model structure on simplicially enriched categories]]
[[!redirects Bergner model structure]]
[[!redirects Bergner model structure on simplicially enriched categories]]
[[!redirects Dwyer–Kan–Bergner model structure]]
[[!redirects Dwyer–Kan–Bergner model structure on simplicially enriched categories]]

[[!redirects Dwyer–Kan–Bergner model structure on sSet-enriched categories]]
[[!redirects Dwyer-Kan-Bergner model structure on sSet-enriched categories]]

[[!redirects Dwyer--Kan--Bergner model structure]]
[[!redirects Dwyer--Kan--Bergner model structure on simplicially enriched categories]]

[[!redirects Dwyer-Kan equivalence]]
[[!redirects Dwyer-Kan weak equivalence]]
[[!redirects Dwyer-Kan equivalence of simplicial categories]]
[[!redirects Dwyer-Kan equivalences]]
[[!redirects Dwyer-Kan weak equivalences]]
[[!redirects Dwyer-Kan equivalences of simplicial categories]]

[[!redirects Dwyer–Kan equivalence]]
[[!redirects Dwyer–Kan weak equivalence]]
[[!redirects Dwyer–Kan equivalence of simplicial categories]]
[[!redirects Dwyer–Kan equivalences]]
[[!redirects Dwyer–Kan weak equivalences]]
[[!redirects Dwyer–Kan equivalences of simplicial categories]]
