
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


This page collects material related to the book

* [[Peter Johnstone]]

  **Sketches of an Elephant -- A Topos Theory Compendium**


  Oxford University Press 2002

  Volume 1 ([ISBN:9780198534259](https://global.oup.com/academic/product/sketches-of-an-elephant-9780198534259))
                  
  Volume 2 ([ISBN:9780198515982](https://global.oup.com/academic/product/sketches-of-an-elephant-9780198515982))

on [[topos theory]].


Like _Gravitation_, the title can be taken to refer not only to the subject matter but also to the immense size and scope of the book itself. Like _The Lord of the Rings_, it consists of 6 parts arranged evenly into 3 volumes (but without appendices). Actually, Volume&#160;3 has not yet been published (so who knows? it may have appendices after all!).

The _Elephant_ is a good reference for anything related to topos theory, and we may often cite it here. However, it introduced many terminological changes, some of which may not be widely accepted or even known. (Fortunately, it will tell you about these in the text.)


#Contents#
* automatic table of contents goes here
{:toc}

## A Toposes as Categories

### A1 Regular and cartesian closed categories

#### A1.1 Preliminary assumptions

* [[category theory]]

* [[reflective subcategory]]

* [[monadicity theorem]]

* [[adjoint lifting theorem]]

* [[Grothendieck construction]]

#### A1.2 Cartesian categories

* [[finitely complete category]] / [[cartesian category]]

* [[cartesian functor]]

#### A1.3 Regular categories

* [[strong epimorphism]]

* [[conservative functor]]

* [[regular category]]
 
  * [[regular epimorphism]]

* [[exact category]]
* [[regular and exact completion]]

#### A1.4 Coherent categories

* [[coherent category]]

* [[disjoint coproduct]]

* [[extensive category]]
* [[pretopos]]
* [[Heyting category]]
* [[Boolean category]]

#### A1.5 Cartesian closed categories

* [[cartesian closed category]]
* [[locally cartesian closed category]]

* [[cartesian closed functor]]
* [[Frobenius reciprocity]]

* [[dependent product]], [[dependent sum]]

#### A1.6 Subobject classifiers

* [[subobject classifier]]

### A2 Toposes - basic theory

#### A2.1 Definition and examples

* [[topos]]

* Examples

  * [[Set]], [[FinSet]]

  * [[category of sheaves]], [[presheaf]]


#### A2.2 The monadicity theorem

* [[monadicity theorem]]

#### A2.3 The Fundamental Theorem

#### A2.4 Effectiveness, positivity and partial maps

#### A2.5 Natural number objects

* [[natural number object]]

#### A2.6 Quasitoposes

* [[quasitopos]]

### A3 Allegories

#### A3.1 Relations in regular categories

* [[relation]]
* [[Rel]]

#### A3.2 Allegories and tabulations

* [[allegory]]
* [[bicategory of relations]]
* [[1-category equipped with relations]]

#### A3.3 Splitting symmetric idempotents

* [[idempotent]]

#### A3.4 Division allegories and power allegories

### A4 Geometric morphisms - basic theory

#### A4.1 Definition and examples

* [[geometric morphism]]

  * [[direct image]]

  * [[inverse image]]

  * [[geometric transformation]]

* [[essential geometric morphism]]

## B 2-Categorical Aspects of Topos Theory

### B1 Indexed categories and fibrations


#### B1.1 Review of 2-categories

* [[2-category]]
* [[2-limit]]

  * [[inverter]]

#### B1.2 Indexed categories

* [[indexed category]]

* [[indexed functor]]

* [[pseudofunctor]]

#### B1.3 Fibrations

* [[Grothendieck fibration]]

* [[bifibration]]

* [[Grothendieck construction]]

#### B1.4 Limits and colimits

* [[limit]]

* [[dependent product]], [[dependent sum]]

#### B1.5 Descent conditions and stacks

* [[descent]]

* [[stack]]

### B2 Internal and locally internal categories

#### B2.1 Review of enriched categories

* [[enriched category]]

* [[enriched category theory]]

#### B2.2 Locally internal categories

* [[locally internal category]]

#### B2.3 Internal categories and diagram categories

* [[internal category]], [[internal diagram]]

* [[internal (co-)limit]]

#### B2.4 The indexed adjoint functor theorem

* [[adjoint functor theorem]]

* [[indexed adjoint functor theorem]]

#### B2.5 Discrete opfibrations

* [[discrete fibration|discrete opfibration]]

#### B2.6 Filtered colimits

* [[filtered colimit]]

#### B2.7 Internal profunctors

* [[profunctor]]

* [[internal profunctor]]

### B3 Toposes over a base

#### B3.1 $\mathcal{S}$-Toposes as $\mathcal{S}$-indexed categories

* [[indexed topos]]

* [[bounded geometric morphism]]

* [[bounded topos]]

#### B3.2 Diaconescu's theorem

* [[torsor]], [[principal bundle]]

* [[Diaconescu's theorem]]

* [[Sierpinski topos]]

#### B3.3 Giraud's theorem

* [[Giraud's theorem]]

#### B3.4 Colimits in Top

* [[Topos]]

* The paragraph before B3.4.8 refers to A4.1.13, but should probably refer instead to A4.1.15.

## C Toposes as Spaces

### C1 Sheaves on a locale

#### C1.1 Frames and nuclei

* [[frame]]
* [[Heyting algebra]]

#### C1.2 Locales and spaces

* [[locale]]

#### C1.3 Sheaves, local homeomorphisms and frame-valued sets

* [[sheaf]]
* [[local homeomorphism]]

#### C1.4 Continuous maps

(...)

#### C1.5 Some topological properties of toposes

* [[locally connected topos]]

### C2 Sheaves on a site

#### C2.1 Sites and coverages

* [[coverage]]

  * [[regular coverage]]

* [[Grothendieck topology]]

  * [[Grothendieck pretopology]]

* [[site]]

  * [[standard site]]

* Lemma 2.1.7 is incorrect as stated: one should assume that $A$ is a sheaf for a (sifted) coverage. See [here](http://math.stackexchange.com/a/358709) for details.

#### C2.2 The topos of sheaves

* [[sheaf]]

* [[category of sheaves]], 

* [[Grothendieck topos]], [[sheaf topos]]

  * [[Giraud's theorem]]

  * [[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]]


* [[subcanonical topology]], [[canonical topology]]

* [[dense sub-site]]

* The statement that the induced coverage inherits closure properties requires assumptions on either the coverage or the subcategory. See the discussion [here](http://nforum.mathforge.org/discussion/3693/induced-coverage/).

#### C2.3 Morphisms of sites

* [morphism of sites](http://ncatlab.org/nlab/show/site#Morphisms)

#### C2.4 Internal sites and pullbacks

...

#### C2.5 Fibrations of sites

...

### C3 Classes of geometric morphisms

#### C3.1 Open maps

#### C3.2 Proper maps

* [[proper geometric morphism]]

* [[separated geometric morphism]]

* [[compact topos]], [[Hausdorff topos]]

#### C3.3 Locally connected morphisms

* [[locally connected topos]]

* [[locally connected geometric morphism]]

#### C3.4 Tidy morphisms

#### C3.5 Atomic morphisms

* [[atomic geometric morphism]]

#### C3.6 Local maps

* [[local geometric morphism]]

* [[local topos]]

* Example C3.6.15(e) says that $(E/l(M))_{ce}$ is equivalent to $Set$, but the referred-to paper "Local maps of toposes" seems to say that it should be equivalent to $E$ instead.

## D Toposes as theories

### D1 First-order categorical logic


#### D1.1 First-order languages

* [[signature]]

* [[term]]

* [[formula]]

* [[context]]

* [[sequent]]

* [[axiom]]

* [[theory]]

  * [[algebraic theory]]

  * [[propositional theory]]

  * [[Horn theory]]

  * [[regular theory]]

  * [[coherent theory]]

  * [[first-order theory]]

  * [[geometric theory]]

  * [[infinitary first-order theory]]

#### D1.2 Categorical semantics

* [[categorical semantics]]

* [[internal logic]]

* [[models in presheaf toposes]]

#### D1.3 First-order logic

#### D1.4 Syntactic categories

* [[syntactic category]]


#### D1.5 Classical completeness


### D2 Sketches

#### D2.1 The concept of sketch

* [[sketch]]

#### D2.2 Sketches and theories

* [[theory]]

* [[Lawvere theory]]

#### D2.3 Sketchable and accessible categories

* [[locally presentable category]]

* [[accessible category]]

#### D2.4 Properties of model categories

### D3 Classifying toposes


#### D3.1 Classifying toposes via syntactic sites

* [[syntactic site]]

  * [[regular coverage]]

  * [[coherent coverage]]

* [[classifying topos]]


#### D3.2 The object classifier

* [[theory of objects]]

* [[classifying topos for the theory of objects]]

#### D3.3 Coherent toposes

* [[coherent topos]]

#### D3.4 Boolean classifying toposes

#### D3.5 Conceptual completeness

* [[conceptual completeness]]

### D4 Higher-order logic

#### D4.1 Interpreting higher-order logic in a topos

#### D4.2 $\lambda$-Calculus and cartesian closed categories

* [[cartesian closed category]]

* [[lambda-calculus]]

#### D4.3 Toposes as type theories

#### D4.4 Predicative type theories

* [[predicative mathematics]]

#### D4.5 Axioms of choice and Booleanness

* [[axiom of choice]]
* [[internally projective object]] --- note that Lemma 4.5.3(iii) in the Elephant is not quite strong enough to imply (i) and (ii).
* [[excluded middle]]

#### D4.6 De Morgan's law and the Gleason cover

#### D4.7 Real numbers in a topos

* [[real numbers object]]

### D5 Aspects of finiteness

#### D5.1 Natural number objects revisited

#### D5.2 Finite cardinals

* [[finite set]]
* [[finite object]]

#### D5.3 Finitary algebraic theories

* [[algebraic theory]]

* [[Lawvere theory]]

#### D5.4 Kuratowski-finiteness

* [[finite set]]
* [[finite object]]

#### D5.5 Orbitals and numerals

## E Homotopy and Cohomology

### E1 Homotopy theory for toposes

* [[homotopy groups in an (∞,1)-topos]]


#### E1.1 Path-connectedness for locales

* [[locale]]

#### E1.2 The fundamental groupoid via paths

#### E1.3 The fundamental groupoid via coverings

#### E1.4 Natural homotopy


### E2 Algebraic homotopy theory

#### E2.1 Quillen model structures

* [[model category]]

#### E2.2 Model structure for simplicial sets

* [[model structure on simplicial sets]]

#### E2.3 Model structures for sheaves

* [[model structure on simplicial presheaves|model structure on simplicial sheaves]]

#### E2.4 Axiomatic theory of open maps

### E3 Cohomology theory

* [[cohomology]]

* [[abelian sheaf cohomology]]

#### E3.1 Abelian groups and modules in a topos

* [[abelian group]], [[abelian sheaf]]

* [[module]]


#### E3.2 Cech cohomology

* [[Cech cohomology]]

#### E3.3 Torsors and non-abelian cohomology

* [[nonabelian cohomology]]

* [[principal bundle]]

* [[principal ∞-bundle]]

#### E3.4 Classifying toposes and classifying spaces

* [[classifying topos]]

#### E3.5 Cohomological applications of descent theory

* [[descent]] 

## F Toposes as Mathematical Universes

### F1 Synthetic differential geometry

* [[synthetic differential geometry]]

#### F1.1 Properties of the generic ring

* [[classifying topos]]

#### F1.2 Rings of line type

* [[line object]]

#### F1.3 Well-adapted models

* [[Models for Smooth Infinitesimal Analysis]]

#### F1.4 Tiny objects

* [[tiny object]]

#### F1.5 Synthetic integration theory

* [[integration axiom]]

#### F1.6 Intrinsic infinitesimal

* [[infinitesimal object]]

* [[amazing right adjoint]]

### F2 Realizability toposes

#### F2.1 Sch&#246;nfinkel algebras and assemblies

#### F2.2 Realizability toposes

* [[realizability topos]]

#### F2.3 Modified Realizability

#### F2.4 Synthetic domain theory

* [[synthetic domain theory]]

### F3 The free topos

#### F3.1 The free topos as a mathematical universe

#### F3.2 Disjunction and existence properties

#### F3.3 Doing without the natural numbers

#### F3.4 Recursive functions in the free topos


### F4 Topos theory and set theory

#### F4.1 Internal sets in a topos


#### F4.2 Algebraic set theory

* [[algebraic set theory]]

#### F4.3 Independence proofs via classifying toposes

#### F4.4 Independence of the axiom of choice

* [[axiom of choice]]

category: reference


[[!redirects Sketches of an elephant]]

[[!redirects Sketches of an Elephant -- A Topos Theory Compendium]]

[[!redirects Elephant]]

