
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_Homotopy type theory_ is a flavor of _[[type theory]]_ -- specifically of [[intensional type theory|intensional]] ([[Martin-Löf type theory|Martin-Löf]]-)[[dependent type theory]] -- which takes seriously the natural interpretation of _[[identity types]]_ as formalizing [[path space objects]] in [[homotopy theory]].  

In the [[categorical semantics of homotopy type theory]], [[types]] are interpreted not as [[set]]-like [[objects]], but as [[homotopy type]]- or [[∞-groupoid]]/[[∞-stack]]-like objects.  Thus, whereas [[extensional type theory]] can serve as the [[internal language]] of [[1-categories]] (such as [[pretoposes]], [[locally cartesian closed categories]], or [[elementary toposes]]), homotopy type theory can serve as an internal language for various kinds of [[(∞,1)-category]] (such as [[locally cartesian closed (∞,1)-categories]] and [[(∞,1)-toposes]]).  At present, such models are usually constructed by way of 1-categorical [[presentable (infinity,1)-category|presentations]] of (∞,1)-categories using [[type-theoretic model categories]] and related structures such as [[weak factorization systems]].

In addition to a viewpoint on identity types and a general class of categorical models, homotopy type theory is characterized by new homotopically motivated axioms and type-theoretic structures.  Notable among these are:

* Voevodsky's [[univalence axiom]], which represents [[object classifiers]] in (∞,1)-categorical semantics.

* Strong [[function extensionality]], which is a consequence of univalence.

* [[higher inductive type|Higher inductive types]], which among other things enable the construction of finite [[(∞,1)-colimits]], [[cell complexes]], [[n-truncated|truncations]], [[localizations]], and other objects which in classical homotopy theory are constructed using the [[small object argument]].

With all of these axioms included, homotopy type theory behaves like the [[internal language of an (∞,1)-topos]], and conjecturally should admit actual models in any [[(∞,1)-topos]].  With fewer axioms and type constructors, it is known to admit models in more weakly structured [[(∞,1)-categories]] --- see below.

Many details are still being worked out, but the impression is that homotopy type theory thus should serve as a [[foundation]] for [[mathematics]] that is natively about [[homotopy theory]]/[[(∞,1)-category theory]] --- in other words, a foundation in which *[[homotopy types]]*, rather than [[sets]], are basic objects.

## Properties

### Advantages {#Advantages}

As a [[foundation]] for [[mathematics]], homotopy type theory (also called **[[univalent foundations for mathematics|univalent foundations]]**) has the following advantages.  Many of these advantages are shared with some other foundational systems, but no other known system shares all of these, and some are unique to HoTT.

* It treats [[homotopy theory]] and [[∞-groupoids]] natively.  This is an advantage for doing homotopical and [[higher category theory|higher-categorical]] mathematics, which is spreading slowly into other fields.

* It inherits the good computational properties of intensional [[Martin-Löf type theory]].  Some of its new axioms, such as [[univalence]] and [[function extensionality]], are not fully understood yet from a computational perspective, but progress is being made. [This paragraph should be updated in view of the computational interpretation of univalence by the cubical model.]

* It is [[constructive mathematics|constructive]] by default, but can easily be made [[classical logic|classical]] by adding axioms.  This makes it potentially more expressive at essentially no cost.  (In fact, it is not entirely clear how possible it is to do homotopy theory constructively in other foundations.)

* It can (conjecturally) be [[internalization|internalized]] in many categories and higher categories, providing an [[internal logic]] which enables a single [[proof]] to be reinterpreted in many places with many different meanings.

* It is naturally [[isomorphism]]- and [[equivalence]]-invariant (respecting the [[principle of equivalence]]).  This is a consequence of the [[univalence axiom]]: any property or structure (even one which speaks only about [[sets]] and makes no reference to homotopy theory) which is expressible in the theory must be invariant under isomorphism/equivalence.

* Notions such as [[propositions]] and sets are *defined* objects, which inherit good computational properties from the underlying type theory.

* It treats sets, [[groupoids]], and [[n-groupoid|higher groupoids]] on an equal footing.  One can easily remain entirely in the fragment of the theory which talks about sets, not worrying about groupoids or homotopy theory, but as soon as one starts to say something which naturally needs structures of higher [[homotopy level]] (such as talking about some collection of structured sets), the groupoidal and homotopical structure is already there.


### Models in $(\infty,1)$-categories and $(\infty,1)$-toposes

It is well known that [[extensional type theory|extensional]] [[dependent type theory]] is an [[internal logic]] for [[locally cartesian closed categories]]. See at _[[relation between type theory and category theory]]_. 

The step from extensional to [[intensional type theory]] and the [[identity types]] that this brings with it makes intensional dependent type theory have models in certain [[(∞,1)-categories]].  This connection is usually shown by means of a presentation of the $(\infty,1)$-category using a [[weak factorization system]], a [[category of fibrant objects]], a [[model category]], or other similar structure.

It is conjectured (due to [Awodey 09](#Awodey09), [Awodey, 2010](#Awodey), [Joyal, 2011](#Joyal11), see [[Awodey's conjecture]]) that

* intensional dependent type theory with dependent sums and products and [[function extensionality]] (a form of homotopy type theory) is an internal language for [[locally cartesian closed (∞,1)-categories]]; and

* with the [[univalence axiom]] added, it becomes an internal language for [[(∞,1)-toposes]].

Indeed:


+-- {: .num_prop }
###### Proposition

Every [[presentable (∞,1)-category|presentable]] and [[locally cartesian closed (∞,1)-category]] has a presentation by a [[type-theoretic model category]]. This provides the [[categorical semantics]] for [[homotopy type theory]] (without, possibly, the [[univalence]] [[axiom]]).


=--

For more on this see at _[[locally cartesian closed (∞,1)-category]]_ in the section on internal logic.

With the [[univalence]] axiom included (for a [[type of types]] "weakly a la Tarski") then homotopy type theory has categorical semantics in [[(∞,1)-toposes]], with the [[type of types]] interpreted as the [[object classifier]]. 

* [[homotopytypetheory:model of type theory in an (infinity,1)-topos]]

See also at _[[relation between type theory and category theory#HomotopyWithUnivalence|relation between type theory and category theory --- univalent homotopy type theory and elementary $(\infty,1)$-toposes]]_.

For a short introduction to a simplicial model of homotopy type theory see [[T. Streicher - a model of type theory in simplicial sets - a brief introduction to Voevodsky' s homotopy type theory]].



### New Axioms

As a foundation for mathematics whose basic objects are higher groupoids, homotopy type theory makes visible new foundational axioms.  Most of these axioms are true as statements about classical $\infty$-groupoids, but may be false in "nonclassical" models of homotopy type theory such as [[(∞,1)-toposes]].

* [[Whitehead's principle]].

* [[sets cover]], and more generally [[n-types cover]].

* Several variants of the [[axiom of choice]].

Additionally, since homotopy type theory as the internal language of $(\infty, 1)$-toposes is not classical, it is possible to add classically inconsistent axioms, just as, say, the [[Kock-Lawvere axiom]] may be added to ordinary topos theory.

* Axiom R ([Shulman 15](cohesive+homotopy+type+theory#Shulman15))

### Relation to representation theory

[[!include homotopy type representation theory -- table]]


## Machine implementation

An important aspect of HoTT is the fact that the [[intensional type theory|intensional]] [[Martin-Löf type theory]] on which it is built has a computational implementation in proof assistants like [[Coq]] and [[Agda]].

This forms the basis of  the _Univalent Foundations_ program ([Voevodsky](#Voevodsky)), which uses Coq to generate and verify proofs with [[homotopy theory|homotopical]] content.

See the [code page](http://homotopytypetheory.org/coq/) at the [HoTT site](#HoTTSite) for more.

## Dictionary HoTT-Coq / $(\infty,1)$-Category theory
 {#DictionaryToCoq}

The following list displays some keywords defined in the [[Coq]]-implementation of homotopy type theory together with their meaning in the [[homotopy theory]]/[[(∞,1)-category theory]] that they describe. (See also at _[[categorical semantics]]_ and _[[categorical semantics of homotopy type theory]]_.)

Let $C$ be a given ambient [[(∞,1)-category]] which

* is [[locally cartesian closed (∞,1)-category|locally cartesian closed]];

* in addition has [[(∞,1)-colimits]]. 

For instance $C$ could be an [[(∞,1)-topos]] (in which case the homotopy type theory would be the [[internal language of an (∞,1)-topos]]).
 
Note that while Coq-HoTT is supposed to be the internal language for such $C$, the _strict [[models]]_ for it are actually [[homotopical category|homotopical]] [[1-categories]] equipped with extra structure (such as [[model categories]] or [[categories of fibrant objects]]) that make them serve as [[presentable (infinity,1)-categories|presentations]] for $C$.

We then have the following dictionary.

The [[type of types]] [[Type]] 

    Type

denotes an [[object classifier]] in $C$ for a certain size of [[universe]].   Both [[Coq]] and [[Agda]] have systems to manage universe sizes and [[universe enlargement]] automatically; Agda's is more advanced (universe polymorphism), whereas Coq's is good enough for many purposes but tends to produce "universe inconsistencies" when working with [[univalence]].  As a stopgap measure until this is improved, some HoTT code must be compiled with a patch to Coq that turns off all universe consistency checks.

A [[term]] of [[type]] Type (in the empty [[context]])

    X : Type

denotes an [[object]] in the $(\infty,1)$-category $C$.  In a presentation of $C$ by a model category or [[weak factorization system]], it denotes a *fibrant* object.

The [[unit type]]

    unit : Type

is the [[terminal object in an (∞,1)-category|terminal object]].

For $X, Y \in C$ two objects, the [[function type]]

    X -> Y : Type

denotes the [[internal hom]] $[X,Y] \in C$ (a formal proof of that fact is [here](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/AdjunctionProdHom.v)).

A [[dependent type]] (that is, a type in [[context]])

    x : X  |-  P x : Type

denotes a [[morphism]] $P \to X$ (regarded as a [[fibration]] or [[bundle]]) in $C$. In a [[presentable (∞,1)-category|presentation]] of $C$ by a [[category of fibrant objects]], it literally denotes a [[fibration]] $P \to X$.  In this case,

    P : X -> Type

denotes the corresponding classifying map, via an internal [[(∞,1)-Grothendieck construction]].

The total space object $P$ of this bundle -- the _[[dependent sum type]]_ -- is the type equivalently coded as any of the following.

    { x : X  &  P x } : Type
    sigT (fun (x : X) => P x) : Type.
    sigT P : Type

The first one is [[sugaring|syntactic sugar]] for the second.  The third is related to the second by [[eta expansion]], which (assuming [[function extensionality]]) is an equivalence in Coq, but not the identity.  In the next version of Coq, all three types above will be identical.

One might expect to also call the dependent sum type

    exists x : X, P x

(see [[existential quantifier]]) but in the current [[Coq]] implementation that keyword is reserved for the corresponding operation on Coq's built-in universe `Prop`, which is not used by homotopy type theory.  In particular, it should not be confused with what HoTT calls [[proposition]]s, which are the [[(-1)-truncated]] types.  In fact, arguably in HoTT `exists` should refer not to the dependent sum itself, but to the (-1)-truncation thereof (its [[bracket type]]).

The type

    forall x : X, P x

denotes the object of [[homotopy]] [[section]]s of this bundle $P\to X$ --- that is, the _[[dependent product]]_ of the bundle.  (See the section _[relation to spaces of sections](http://ncatlab.org/nlab/show/dependent+product#RelationToSpacesOfSections)_ there).  It also denotes the [[universal quantifier]] when acting on (-1)-truncated objects [[propositions]].  A term of this type :

    f : forall x : X, P x

denotes therefore a particular [[section]] of this bundle

$$
  \array{
     && P
     \\  
     & {}^{\mathllap{f}}\nearrow& \downarrow
     \\ 
     X &= & X
  }
  \,.
$$

Given a type $X$, its [[identity type]], denoted

    paths X : X -> X -> Type
    Id X : X -> X -> Type

corresponds to the [[diagonal morphism]] $X\to X\times X$ in $C$, regarded as a bundle over $X\times X$.  In a [[presentable (infinity,1)-category|presentation]] of $C$ by a [[category of fibrant objects]], this means the [[path space object]] $X^I$, since dependent types must always be fibrations.

The fact that there is a [[weak equivalence]] $X \stackrel{\simeq}{\to} X^I$ given by the inclusion of [[identity]] [[morphisms]] is reflected in the [[inductive type]]-definition of <code>paths</code>, which says that any proposition about terms in the path type is already determined by its value on all identity paths.

Then for <code>x y : X</code> two [[terms]] regarded as morphisms $1\to X$, the application of the identity type $x$ and $y$ (also called the [[identity type]]) denoted variously

    paths X x y : Type
    x ~~> y : Type
    x == y : Type

(the latter two make use of Coq's ability to define new notations), denotes the [[homotopy pullback]] of the form

$$
  \array{
    x \times_X y &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{x}}
    \\
    {*} &\stackrel{y}{\to}&  X
  }
$$

which in a presentation by a [[category of fibrant objects]] is given (see [[factorization lemma]]) by the ordinary pullback

$$
  \array{
    P_{x,y} X &\to& &\to& {*}
    \\
    \downarrow && && \downarrow^{\mathrlap{x}}
    \\
    \downarrow && X^{\Delta[1]} &\to& X
    \\  
    \downarrow && \downarrow
    \\
    {*} &\stackrel{y}{\to}& X
  }
  \,.
$$

Beware that the [[identity type|path induction rule]] applies to <code>paths X</code> not to <code>paths X x y</code>.  Where for the former a proposition is fixed by what it does on identity paths, for the latter this is not the case anymore.

More generally, we can define arbitrary pullbacks. If `f : A -> C` and `g : B -> C`, the [[homotopy pullback]] of `f` and `g` is defined by

    {a : A & {b : B & f a ~~> g b}}

together with the obvious projections to `A` and `B` and the homotopy between the composites.
(a proof can be found [here](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/Pullbacks.v))

Using [[higher inductive types]], we can also define [[homotopy pushouts]]. If `g : C -> A` and `f : C -> B`, the [[homotopy pushout]] of `f` and `g` is defined by

    Inductive hopushout :=
      | inl : A -> hopushout
      | inr : B -> hopushout
      | glue : forall x : C, inl (g x) ~~> inr (f x).

together with the map `inl`, `inr` and the homotopy `glue`.
(see [here](https://github.com/guillaumebrunerie/HoTT/blob/master/Coq/Limits/Pushout.v) for the proof)

## Related entries

* [[univalent foundations for mathematics]]

* [[homotopy type theory FAQ]]

* [[higher structures]]

* [[intensional type theory]], [[observational type theory]], [[extensional type theory]]

* [[cubical type theory]]

* [[type-theoretic model category]], [[fibrant type]]

* [[synthetic homotopy theory]]

* [[HoTT methods for homotopy theorists]]

* [[internal category in homotopy type theory]]

* [[Homotopy Type System]]

* [[modal homotopy type theory]]

* [[geometric homotopy type theory]]

* [[cohesive homotopy type theory]]

* [[directed homotopy type theory]]

  [[opetopic type theory]]


\linebreak

[[!include homotopy n-types - table]]


\linebreak

[[!include proof assistants and formalization projects -- list]]



## References
 {#References}

A survey page maintained by [[Steve Awodey]] is _[Homotopy Type Theory and the Univalent Foundations of Mathematics](http://www.andrew.cmu.edu/user/awodey/htt.html)_

### Introductions
 {#Introductions}

The standard textbook is

* [[Univalent Foundations Project]], _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013)

An introduction for philosophers is

* {#Shulman16} [[Michael Shulman]], _Homotopy Type Theory: A synthetic approach to higher equalities_ ([arXiv:1601.05035](http://arxiv.org/abs/1601.05035))

and one with an emphasis on [[synthetic geometry]] is 

* {#Shulman17} [[Michael Shulman]], _Homotopy type theory: the logic of space_, in [[Gabriel Catren]], [[Mathieu Anel]] (eds.) _[[New Spaces for Mathematics and Physics]]_ ([arXiv:1703.03007](https://arxiv.org/abs/1703.03007))

Early sketches and introductions to the idea of homotopy type theory include

* {#Awodey09} [[Steve Awodey]], _Homotopy and Type Theory_, grant proposal project description ([pdf](https://ncatlab.org/homotopytypetheory/files/proposal2009.pdf))

* {#Awodey} [[Steve Awodey]], _Type theory and homotopy_, Epistemology versus Ontology. Springer Netherlands, 2012. 183-201. (2010) [arXiv:1010.1810](http://arxiv.org/abs/1010.1810)
 


* [[Michael Shulman]], _Homotopy type theory_ [I](http://golem.ph.utexas.edu/category/2011/03/homotopy_type_theory_i.html), [II](http://golem.ph.utexas.edu/category/2011/03/homotopy_type_theory_ii.html), [III](http://golem.ph.utexas.edu/category/2011/03/homotopy_type_theory_iii.html), [IV](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_iv.html), [V](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_v.html), [VI](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_vi.html)

* [[Thorsten Altenkirch]], [[Thierry Coquand]], _Towards higher dimensional type theory_, Nottingham (2011) ([pdf](http://www.cs.nott.ac.uk/~txa/talks/aimxiii.pdf))


* {#ShulmanCourse} [[Mike Shulman]], _Minicourse on homotopy type theory_, Swansea, April (2012) ([web](http://home.sandiego.edu/~shulman/hottminicourse2012/))

* {#Voevodsky} [[Vladimir Voevodsky]], _[Univalent foundations](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations.html)_
  

Motivation via practical problems in [[homotopy theory]] and [[higher category theory]] is given in 

* {#VoevodskyIASTalk2014} [[Vladimir Voevodsky]], _Univalent foundations_, talk IAS, March 2014 ([pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/2014_IAS.pdf), [video](https://video.ias.edu/voevodsky14))

 (specifically highlighting the technical delicacies involved in the [[Simpson conjecture]]).

A list of video-recorded talks by Voevodsky on this topic is [here](http://video.ias.edu/taxonomy/term/42).


Writeups on the topic include

* [[Nicolai Kraus]], _Homotopy type theory -- An overview_ ([pdf](http://www.cs.nott.ac.uk/~ngk/homotopy_type_theory.pdf))

* [[Egbert Rijke]], _Homotopy type theory_ (2012) ([pdf](http://hottheory.files.wordpress.com/2012/08/hott2.pdf))

* {#PelayoWarren} &#193;lvaro Pelayo, [[Michael Warren]], _Homotopy type theory and Voevodsky's univalent foundations_ ([arXiv:1210.5658](http://arxiv.org/abs/1210.5658))

* Daniel Grayson, _An introduction to univalent foundations for mathematicians_, 2017, [arXiv:1711.01477](https://arxiv.org/abs/1711.01477).

* {#Rijke19} [[Egbert Rijke]], _[[Introduction to Homotopy Type Theory]]_ (2019)  ([web](http://www.andrew.cmu.edu/user/erijke/hott/), [pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [GitHub](https://github.com/EgbertRijke/HoTT-Intro)) 

* {#Rijke19b} [[Egbert Rijke]], _Classifying Types_ ([arXiv:1906.09435](https://arxiv.org/abs/1906.09435))

An introduction to the notion of [[equivalence]] in HoTT is in

* [[Andrej Bauer]], _A seminar on HoTT equivalences_ ([blog post](http://homotopytypetheory.org/2011/12/07/a-seminar-on-hott-equivalences/))

A guided walk through the basics of HoTT and then the formal proof in [[Coq]] that the [[univalence axiom]] implies [[functional extensionality]] is at

* [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _[[Oberwolfach HoTT-Coq tutorial]]_

Gentle invitation to some basics:

* {#Bauer19} [[Andrej Bauer]], _What is an explicit bijection?_, talk at [FPSAC 2019](http://fpsac2019.fmf.uni-lj.si/) ([slides pdf](http://videolectures.net/site/normal_dl/tag=1244258/FPSAC2019_bauer_explicit_bijection_01.pdf), [video recording](http://videolectures.net/FPSAC2019_bauer_explicit_bijection/))

From the point of view of [[cubical type theory]]:

* [[Anders Mörtberg]], Loïc Pujet, _Cubical synthetic homotopy theory_,  CPP 2020: Proceedings of the 9th ACM SIGPLAN International Conference on Certified Programs and Proofs January 2020, pp. 158–171, [doi:10.1145/3372885.3373825](https://doi.org/10.1145/3372885.3373825), ([pdf](https://staff.math.su.se/anders.mortberg/papers/cubicalsynthetic.pdf))


### General

A blog serving as a base for the HoTT community is at

* {#HoTTSite} _Homotopy Type Theory_ [website](http://homotopytypetheory.org/)

A wiki is here

* _[HoTT wiki](https://ncatlab.org/homotopytypetheory/show/HomePage)_

Reports from the original Oberwolfach workshop on homotopy type theory are in 

* _Homotopy type theory_ , Oberwolfach Reports 11-2011, ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf)).

Material concerning the 

* _[Univalent foundations program 2012/2013](http://www.math.ias.edu/sp/univalent)_, Institute of Advanced Study, Princeton

is in the wiki

* _[UF-IAS-2012](http://uf-ias-2012.wikispaces.com/)_ .

A FAQ of sorts, with tips for those getting started in the field, is being maintained at

* _[What I wish I knew when learning HoTT](https://abooij.github.io/wiwikwlhott/)_.


### Models and categorical semantics

The first [[model]] for [[intensional type theory|intensional]] [[Martin-Löf type theory]] on [[groupoids]] (instead of [[sets]] = [[0-groupoids]]) was

* {#HofmannStreicher98} [[Martin Hofmann]], [[Thomas Streicher]]  _The groupoid interpretation of type theory_, in: Giovanni Sambin et al. (ed.) , _Twenty-five years of constructive type theory_, Proceedings of a congress, Venice, Italy, October 19&#8212;21, 1995. Oxford: Clarendon Press. Oxf. Logic Guides. 36, 83-111 (1998).  ([ps](http://www.mathematik.tu-darmstadt.de/~streicher/venedig.ps.gz))

Generalization of this to [[strict ∞-groupoids]] were discussed in

* [[Michael Warren]], _The strict $\omega$-groupoid interpretation of type theory_ ([pdf](http://www.math.ias.edu/~mwarren/Papers/makkaifest_preprint.pdf))

The fact that every [[simplicial model category]] in which the cofibrations are [[monomorphisms]] provides a sound [[model]] for [[intensional type theory|intensional]] [[Martin-Löf type theory]] is discussed in 

* {#AwodeyWarren07} [[Steve Awodey]], [[Michael Warren]], _Homotopy theoretic models of identity type_,  Mathematical Proceedings of the Cambridge Philosophical Society vol 146, no. 1 (2009) ([arXiv:0709.0248](http://arxiv.org/abs/0709.0248))

and with more details in 

* [[Michael Warren]], _Homotopy theoretic aspects of constructive type theory_, PhD thesis (2008) ([pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf))

* [[Richard Garner]],  [[Benno van den Berg]], _Topological and simplicial models of identity types_. , ACM Transactions on Computational Logic ([pdf](http://www.mathematik.tu-darmstadt.de/~berg/papers/main.pdf))


* section 2 of ([Shulman 12](#Shulman12))


with lecture notes in 

* [[Mike Shulman]], _Categorical models of homotopy type theory_, April 13, 2012 ([pdf](https://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf))

* [[André Joyal]], _Categorical homotopy type theory_, March 17, 2014 ([pdf](http://ncatlab.org/homotopytypetheory/files/Joyal.pdf))

The full model in the [[classical model structure on simplicial sets]] is due to

* {#KapulkinLumsdaine12} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], _The Simplicial Model of Univalent Foundations (after Voevodsky)_ ([arXiv:1211.2851](https://arxiv.org/abs/1211.2851))

The trickiest question in finding models of homotopy type theory is to validate the [[univalence axiom]].  The first model satisfying this axiom was constructed by Voevodsky using the standard [[model structure on simplicial sets]], hence for the archetypical [[(∞,1)-topos]] [[∞Grpd]] of [[discrete ∞-groupoids]].  Some expositions are:

* [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], [[Vladimir Voevodsky]], *Univalence in simplicial sets*, [arXiv](http://arxiv.org/abs/1203.2553)

* [[T. Streicher - a model of type theory in simplicial sets - a brief introduction to Voevodsky' s homotopy type theory]]

* [[Ieke Moerdijk]] (notes by [[Chris Kapulkin]]): *Fiber bundles and univalence*, [link](http://www.pitt.edu/~krk56/fiber_bundles_univalence.pdf)

A discussion of univalence for [[categories of presheaves]] over an [[inverse category]], with values in a category for which univalence is already established (such as simplicial sets) is discussed in 

* {#Shulman12} [[Michael Shulman]], _The univalence axiom for inverse diagrams_ ([arXiv:1203.3253](http://arxiv.org/abs/1203.3253)).

Proof that all [[∞-stack]] [[(∞,1)-topos]] have [[presentable (∞,1)-category|presentations]] by [[model categories]] which interpret (provide [[categorical semantics]]) for [[homotopy type theory]] with [[univalence|univalent]] [[type universes]]:

* {#Shulman19} [[Michael Shulman]], _All $(\infty,1)$-toposes have strict univalent universes_ ([arXiv:1904.07004](https://arxiv.org/abs/1904.07004)).

Discussion of univalence in various other [[model category]] presentations for [[∞Grpd]] ([[cubical sets]], [[cellular sets]]) is in

* {#Cisinski14} [[Denis-Charles Cisinski]], _Univalent universes for elegant models of homotopy types_ ([arXiv:1406.0058](http://arxiv.org/abs/1406.0058))

Models in terms of [[cubical sets]] inside [[constructive set theory]]/[[type theory]] are discussed in

* {#BezemCoquandHuber13} Marc Bezem, [[Thierry Coquand]], Simon Huber, _A model of type theory in cubical sets_, 2013  ([web](http://drops.dagstuhl.de/opus/volltexte/2014/4628/), [pdf](http://drops.dagstuhl.de/opus/volltexte/2014/4628/pdf/7.pdf))

* {#KaposiAltenkirch14} Ambrus Kaposi, [[Thorsten Altenkirch]], _A syntax for cubical type theory_ ([pdf](http://mazzo.li/dump/aim-kaposi-pres.pdf))

A weaker version of the [[Awodey conjecture]], that the models of HoTT with function extensionality are [[locally cartesian closed (∞,1)-categories]] is explicitly stated in

* {#Joyal11} [[André Joyal]], _Remarks on homotopical logic_ Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))

See also the references at _[[relation between type theory and category theory]]_.

### Syntax

* [[Nicola Gambino]], [[Richard Garner]], _The identity type weak factorisation system_ , Theoretical Computer Science 409 (2008), no. 3, pages 94&#8211;109. 

* [[Richard Garner]], [[Benno van den Berg]],  _Types are weak &#969;-groupoids_ , 

* [[Peter LeFanu Lumsdaine]], _Weak &#969;-Categories from Intensional Type Theory_ , TLCA 2009, Bras&#237;lia, Logical Methods in Computer Science, Vol. 6, issue 23, paper 24. 

* [[Peter LeFanu Lumsdaine]], _Higher Categories from Type Theories_ , PhD Thesis: Carnegie Mellon University, 2010. [PDF]
    
* Michael Hedberg, _A coherence theorem for Martin-L&#246;f's type theory_ , Journal of Functional Programming 8 (4): 413&#8211;436, July 1998.
 

### Code
 {#Code}

The basic [[Coq]]-code libraries that set up [[identity types]] and the resulting homotopy type theory are at

* [[Vladimir Voevodsky]], _Experimental library of univalent formalization of mathematics_ ([arXiv:1401.0053](http://arxiv.org/abs/1401.0053)) [github](https://github.com/UniMath/)

* _The HoTT Library: A formalization of homotopy type theory in Coq_, 
Andrej Bauer, Jason Gross, Peter LeFanu Lumsdaine, Mike Shulman, Matthieu Sozeau, Bas Spitters, 2016 [arxiv](https://arxiv.org/abs/1610.04591) and on [github](https://github.com/HoTT/HoTT/wiki)


A slightly more human readable version is collected as a single pdf in

* _HoTT-Coq code_ ([[HoTT-Coq-code.pdf:file]])

* Voevodsky, Vladimir and Ahrens, Benedikt and Grayson, Daniel and others, [[unimath|UniMath]], [GitHub](https://github.com/UniMath) link.

[[!redirects homotopy type theory]]
[[!redirects (∞,1)-type theory]]
[[!redirects (infinity,1)-type theory]]
[[!redirects Homotopy type theory]]
[[!redirects HoTT]]
[[!redirects internal language of an (∞,1)-topos]]

