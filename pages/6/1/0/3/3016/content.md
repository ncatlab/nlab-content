
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[category theory]]

* [[2-category theory]]

* [[(∞,1)-category theory]]

* [[higher category theory]]


***



[Wikipedia](http://en.wikipedia.org/wiki/Main_Page) enforces its entries to adopt an [NPOV](http://en.wikipedia.org/wiki/NPOV) -- a _neutral point of view_ .  This is appropriate for an encyclopedia.

However, [[About|the nLab is not Wikipedia]], nor is it an encyclopedia, although it does aspire to provide a useful reference in many areas (among its other purposes).  In particular, the $n$Lab *has* a particular point of view, which we may call the **$n$POV** or the _[[higher category theory|n-]] [[category theory|categorical]] point of view_ .

#$n$POV#
* automatic table of contents goes here
{:toc}


## Idea

Around the [[HomePage|nLab]] it is believed that [[category theory]] and [[higher category theory]] provide a point of view on [[Mathematics]], [[Physics]] and [[Philosophy]] which is a valuable unifying point of view for the understanding of the concepts involved.

So at the $n$Lab, we don't care so much about being neutral.  Although we don't want to offend people unnecessarily, we are also not ashamed about writing from this particular point of view.  There are certainly other valid points of view on mathematics, but describing them and being neutral towards them is not the purpose of the $n$Lab.  Rather, the $n$Lab starts from the premise that category theory and higher category theory are a true and useful point of view, and one of its aims is to expose this point of view generally and in a multitude of examples, and thereby accumulate evidence for it.

If you feel skeptical about the $n$-point of view, you may want to ignore the $n$Lab. Or you may want to take its content as a contribution to a discussion on what is behind the claim that category theory is the right language to describe the world, or at least the world of mathematical ideas.

As recalled in parts on the page on [[category theory]], category theorists have early on, beginning in the 1960s, proclaimed the advantages of category theory over other points of view. It has been observed that this claim, or at least the way it has been put forward, has contributed to a certain alienation of category theory in parts of the mathematical community. That may be true and is understandable. But since a claim is not false _just_ because it is put forward with possibly unpleasant boldness, all evidence for the claim deserves to be collected and exposed. We hope the $n$Lab to play a role in this effort.

In particular, there have been dramatic developments since the 1960s. Back then promoting category theory may have been as visionary as the invention of [[complex numbers]] was in the 16th century. But just as the early rejections of the complex numbers appear strangely out of place from today's perspective, where their ubiquity proves their reality to the point that it is hard to imagine how life must have been before their conception, so developments of category theory and its applications in the last years have in many areas brought it to the point that rejecting its prevalence amounts (we believe) to rejecting the obvious and ubiquitous. But also mathematics as a whole has drastically grown since then, and while category theory has become an entirely obvious ingredient in areas such as [[homotopy theory]], [[homological algebra]], [[algebraic geometry]] and even fields like [[topological quantum field theory]], its similar role to be played in many other areas has often not found wide recognition yet. But this is gradually changing. 


+-- {: .standout}

Similar to the statement that

> [Nothing in biology makes sense except in the light of evolution](http://en.wikipedia.org/wiki/Nothing_in_Biology_Makes_Sense_Except_in_the_Light_of_Evolution)

the nPOV asserts that

> Nothing in mathematics makes sense except in the light of [[higher category theory|higher]] [[category theory]].

=--

## The role of the $n$POV {#RoleOfnPOV}

Practitioners of category theory have often attempted to express the striking power of category theory (or general conceptual methods), sometimes through aphorism, sometimes through metaphor. Early on, [[Peter Freyd]] wrote 

> Perhaps the purpose of categorical algebra is to show that which is trivial is trivially trivial.

This can be taken to mean that one thing category theory does is help make the softer bits seem utterly natural and obvious, so as to quickly get to the heart of the matter, isolating the hard nuggets, which one may then attack with abandon. This is an invaluable service category theory performs for mathematics; therefore, category theory is plain good pragmatics. 

However, it is also possible to take it a step beyond the pragmatic attitude, and see category theory (and now higher category theory) as exemplifying a style for doing even hard mathematics, as in the style for which Grothendieck is renowned. Paraphrasing from Colin McLarty's [excellent essay](http://www.math.jussieu.fr/~leila/grothendieckcircle/mclarty1.pdf), let us regard the aforementioned pragmatic attitude as leading up to the _hammer-and-chisel principle_: if you think of a theorem to be proved as a nut to be opened, so as to reach "the nourishing flesh protected by the shell" (Grothendieck), then one thing to do is "put the cutting edge of the chisel against the shell and strike hard. If needed, begin again at many different points until the shell cracks -- and you are satisfied." Grothendieck points to Serre as a master of this technique. He then says: 

> I can illustrate the second approach with the same image of a nut to be opened. The first analogy which came to my mind is of immersing the nut in some softening liquid, and why not simply water? From time to time you rub so the liquid penetrates better, and otherwise you let time pass. The shell becomes more flexible through weeks and months -- when the time is ripe, hand pressure is enough, the shell opens like a perfectly ripened avocado! 

> A different image came to me a few weeks ago. The unknown thing to be known appeared to me as some stretch of earth or hard marl, resisting penetration... the sea advances insensibly in silence, nothing seems to happen, nothing moves, the water is so far off you hardly hear it... yet it finally surrounds the resistant substance. (Translated from the French by McLarty)

This arresting metaphor of "la mer qui monte", which over time changes the very form of the resistant substance, is very much in the style of Grothendieck himself. McLarty quotes Deligne as saying that a typical Grothendieck proof consists of a long series of trivial steps where "nothing seems to happen, and yet at the end a highly non-trivial theorem is there." 

## Examples

The following is a (incomplete) list of examples of topics for which the $n$POV has proven to be a useful perspective. 


### In geometry

The field of [[differential geometry]] has long managed to avoid the change to an $n$-point of view that had been found to be unavoidable, natural and fruitful in algebraic geometry long ago. But more recently -- not the least due to the recognition of differential [[higher geometry|higher geometric]] structures in the physics of [[gauge theory]] and [[supergravity]] (such as that of [[orbifold]]s and [[orientifold]]s, of smooth [[gerbe]]s and smooth [[principal ∞-bundle]]s) -- [[sheaf and topos theory|sheaf and topos theoretic]] concepts, such as [[synthetic differential geometry]], [[diffeological space]]s and [[differentiable stack]]s are gaining wider recognition and appreciation. 

For instance the ordinary category [[Diff]] of [[smooth manifold]]s fails to have all [[pullback]]s, it only has pullbacks along [[transversal map]]s.
This observation is usually the starting point for realizing that differential geometry is in need of a bit of [[category theory]] in the form of [[higher geometry]]. 

In all notions of [[generalized smooth space]]s all pullbacks do exist. But they may still not be the "right" pullbacks. For instance cohomology of pullback objects may not have the expected properties. This is solved by passing to smooth [[derived stack]]s, such as [[derived smooth manifold]]s.


Recent developments in [[higher category theory]], such as the concept of higher [[Structured Spaces]] based on [[Higher Topos Theory]], put all these notions of generalized geometries into a unified picture of [[higher geometry]] that realizes old ideas about how category theory provides a language for [[space and quantity]] in great detail and powerful generality and sheds new light on old [[classical mathematics|classical]] problems such the description of the [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves|derived moduli stack of derived elliptic curves]] and the construction of the [[tmf]] [[spectrum]] from it.
This construction is probably literally _unthinkable_ without adopting the $n$-point of view when approaching it. Using this point of view, the general strategy for approaching it however becomes naturally evident.

#### In differential equations {#DiffEqu}

Much of [[topological vector space]] theory, e.g., the theory of [[distribution]]s, [[nuclear space]]s, etc. has its origins in [[partial differential equation]] theory and is intensely conceptual (categorical) in spirit. It is routine these days to accept distributional solutions, but it wasn't always so, and it was the efficacy of the abstract TVS theory which changed people's minds.

Way back Cartan studied differential equations in terms of [[exterior differential system]]s. From the $n$POV, these may be understood naturally as nothing but sub [[Lie ∞-algebroid]]s of a [[tangent Lie algebroid]]. 

[[Bill Lawvere]] noticed in the 1960s that the notion of differential equation makes sense in any [[smooth topos]] (as described [here](http://ncatlab.org/nlab/show/differential+equation#InSynthDiff)). In his highly influental article _Categorical dynamics_ he promoted the point of view that all things [[differential geometry|differential geometric]] can be formulated in abstract category theory internal to a suitable [[topos]]. This is the origin of [[synthetic differential geometry]]. It may be understood as providing the fundamental characterization of the notion of the [[infinitesimal space|infinitesimal]].

Closely related to both these perspectives, a modern point of view on differential equations that is proving to be very fruitful regards them as part of the theory of [[D-module]]s. 



### In cohomology

Thousands of definitions of notions of cohomology and its variants. From the $n$POV, just a single concept: an [[derived hom space|∞-categorical hom-space]] in an [[(∞,1)-topos]]. See [[cohomology]].

### In homotopy theory {#InHomotopyTheory}

The study of [[homotopy theory]] originated in the study of categories such as those of [[topological space]]s and other objects such as [[chain complex]]es whose [[morphism]]s were known to admit a notion of [[homotopy]]. Historically, in a sequence of steps formalisms were proposed that would organize the rich interesting structure found in such situations. As a first approximation the notion of [[homotopy category]] and [[derived category]] was introduced in order to deal with structures "up to homotopy". But it was clear that the [[homotopy category]] captured only a very small part of the interesting information. Quillen introduced the notion of [[model category]] as a formalization of the full structure, and this formalization turned out to yield a powerful theory that today provides a powerful toolset for dealing with homotopy theoretic situations.

But also the notion of model category was seen to not be the full answer. For instance a model category in a sense retains _too much_ non-intrinsic information. Equivalence classes of model categories under [[Quillen equivalence]] are a more intrinsic characterization of a given [[homotopy theory]]. But this means that one needs some [[higher category theory|higher categorical]] notion for the collection of all model categories. This problem came to be known as the search for the **homotopy theory of homotopy theories**.

Recently, this problem was fully solved and homotopy theory fully understood as the special case of [[higher category theory]] that deals with [[(∞,1)-category|(∞,1)-categories]]:

* the notion of [[model category]], in particular when refined to that of a [[simplicial model category]] serves as a [[presentable (infinity,1)-category|presentation]] of the notion of [[(∞,1)-category]];

* the "homotopy theory of homotopy theories" is accordingly the [[(∞,1)-category of (∞,1)-categories]] $(\infty,1)Cat$;

  better yet: there is an [[(∞,n)-category|(∞,2)-category]] of all $(\infty,1)$-categories;

* in $(\infty,1)Cat$ two $(\infty,1)$-categories presented by model categories are equivalent precisely if the presenting model categories may be connected by a zig-zag sequence of [[Quillen equivalence]]s;

* all "homotopy"-constructions in model category theory, such as [[homotopy limit]]s, [[mapping cone]]s etc. are _tools for constructing_ the corresponding higher categorical intrinsic notions, such as [[limit in a quasi-category|limit in an (∞,1)-category]].

* all variant notions find their intrinsic higher categorical interpretation this way: for instance [[stable homotopy theory]] is the study of [[stable (∞,1)-category|stable (∞,1)-categories]];

* the [[homotopy category]] of a [[model category]] is simply the [[decategorification]] of the corresponding $(\infty,1)$-category to just a [[1-category]];

* and for instance the notion of homotopy category of a stable $(\infty,1)$-category reproduces the notion of [[triangulated category]], thus incorporating also a large toolset from [[homological algebra]] into the picture.


#### In rational homotopy theory {#RationalHomotopyTheory}

... The study of [[rational homotopy theory]] and is naturally understood as the study of the [[localization of an (∞,1)-category|localizations]] of [[(∞,1)-topos]]es at morphism that induce equivalences in [[cohomology]] with certain line-object coefficients. See [[rational homotopy theory in an (∞,1)-topos]]. ...


### In K-theory

In full generality, ([[algebraic K-theory|algebraic]]) [[K-theory]] is a universal assignment of [[spectra]] to [[stable (∞,1)-categories]].

...

### In Tannaka duality

... see [[Tannaka duality]] ...


### In deformation theory {#DeformationTheory}

In deformation theory it was early on recognized that for a good theory the notion of [[Kähler differential]]s has to be generalized to the notion of [[cotangent complex]]. With the advent of the study of derived [[moduli space]]s, such as the [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves|derived moduli space of derived elliptic curves]], this needed to be further generalized to notions of cotangent complexes not just of [[ring]]s, but of [[E-∞-ring]]s. 

It turns out that all these concepts are special cases of a construction obtained from a simple higher categorical notion, that of [[left adjoint]] [[section]]s of a [[tangent (∞,1)-category]]. 

### In logic {#Logic}

While it is common to view logic as the study of absolute truth, in fact logic can have many different interpretations, or [[semantics]].  A particular semantics for logic can be useful both to inform the study of logic, and to prove facts logically about the semantics.  One very fruitful semantics of this sort is *categorical semantics* for logic and [[type theory]], according to which every category (and especially every [[topos]]) has an [internal language](/nlab/show/type+theory#CategoricalSemantics) and [[internal logic]].  Interpreting "ordinary" mathematical statements in the internal language of exotic categories can make it much easier to study those categories, while on the other hand it can provide new insight into otherwise mysterious logical notions.

In particular, the internal logic of a category (such as a topos) is, in general, [[constructive mathematics|constructive]], i.e. the principle of [[excluded middle]] (and also stronger statements, such as the [[axiom of choice]]) are generally false.  Thus, in order for a theorem to be interpretable internally in such categories, its proof must be constructive.  So while the original "constructivists" believed that classical mathematics was "wrong," nowadays there are good reasons to care about constructive mathematics even if one believes that excluded middle and the axiom of choice are "true," since regardless of their "global" truth they will *not* be true in the internal logic of many interesting categories.  Conversely, category-theoretic models have provided new insight into the independence of various axioms in constructive mathematics, such as differing forms of the axiom of choice.

As another example, the [[identity types]] in Martin-L&#246;f's original constructive dependent [[type theory]] construct, from any [[type]] $A$ and terms $a, b \in A$, a new type $Id_A(a, b)$.  According to the [[propositions as types]] interpretation, the elements of $Id_A(a,b)$ are proofs that $a$ and $b$ are propositionally equal; thus$Id_A(a,b)$ is a replacement for the [[truth value]] of the [[proposition]] $(a=b)$.   There are type-theoretic [[functions]] $1 \to Id(a, a)$, $Id(b, c) \times Id(a, b) \to Id(a, c)$ and $Id(a, b) \to Id(b, a)$ expressing the [[equivalence relation|reflexivity, transitivity and symmetry]] of this propositional [[equality]], but in general an identity type (even the "reflexive" identity type $Id(a,a)$) can have many distinct elements.  This has long been a source of discomfort to type theorists.  However, from a higher-categorical point of view, it is natural to view the terms of identity types as *isomorphisms* in a [[groupoid]]---or, more precisely, an [[∞-groupoid]], since identity types have their own identity types, and all the laws of associativity, exchange, etc. only hold up to terms of these higher identity types.  This suggests that the nonuniqueness of identity proofs should be embraced rather than denigrated, producing a theory at least related to the "internal logic" of [[(∞,1)-category]] theory and [[homotopy theory]]; see [[identity type]] for more details.


### In physics {#Physics}


> the entry [[higher category theory and physics]] should eventually contain some decent material, but at the moment it is just a sketch of a sketch

#### Classical mechanics and its geometric quantization {#ClassMech}

By the end of the 19th century a fairly complete, powerful and elegant mathematical formulation of [[classical mechanics]]: in terms of [[symplectic geometry]]. By the middle of the 20th century, the passage to the corresponding quantum theory was pretty well modeled by the [[geometric quantization]] of symplectic geometries.

But there were some lose ends. Notably the fully general theory involved [[Poisson manifold]]s, not just symplectic manifolds. And the mechnics of relativistic [[classical field theory]] was realized to be more naturally described by [[multisymplectic geometry]].

Both these generalizations have a natural common higher categorical formulation: that of [[Lie ∞-algebroid]]s: a Poisson geometry is naturally encoded in its corresponding [[Poisson Lie algebroid]]. Its higher categorical versions -- the [[n-symplectic manifold]]s -- encode the corresponding multisymplectic geometry.

Moreover, the quantization step of geometric quantization was understood to be effectively the [[Lie integration]] of these [[Lie ∞-algebroid]]s to the corresponding [[Lie ∞-groupoid]]s (currently this is well understood for low $n$). 



#### Quantum mechanics and quantum information {#QuantumMechanics}

The basic structure of [[quantum mechanics]] and [[quantum information theory]] is encoded in the theory of [[dagger-compact categories]].

...


#### Gauge theory {#GaugeTheory}

Maxwell realized that the [[electromagnetic field]] is controlled by a degree 2-cocycle in [[de Rham cohomology]]: the electromagnetic [[field strength]]. Later Dirac noticed that this is one part of a degree 2-cocycle in [[differential cohomology]] that characterize a [[connection on a bundle|connection]] on a [[line bundle]].

Later the [[Yang-Mills field]] was understood to similarly be a [[connection on a bundle]], this time on a $G$-[[principal bundle]] for $G$ some possibly nonabelian [[group]]. 

While thinking about the mathematical structures possibly underlying [[standard model of particle physics]] and [[gravity]], theoretical physicists considered more general hypothetical [[gauge field]]s, such as the [[Kalb-Ramond field]], the [[RR-field]] or the [[supergravity C-field]]. Today all these gauge fields are understood to be modeled, mathematically, by generalized [[differential cohomology]].


##### Supergravity {#Supergravity}

Theories of [[supergravity]] have been known to require higher [[gauge field]]s in the above sense -- hence the term [[supergravity C-field]]. A powerful formalism for handling these theories is the [[D'Auria-Fre formulation of supergravity]]. As described there, this is secretly (but evidently) nothing but a description of supergravity as a theory of connections on nonabelian $G$-[[principal ∞-bundle]]s for $G$ some super [[Lie ∞-groupoid|Lie ∞-group]]. For instance Cremmer-Scherk 11-dimensional supergravity theory is governed by the super Lie 3-group $G$ whose [[L-∞-algebra]] is the [[supergravity Lie 3-algebra]].


#### BV-BRST formalism {#BVBRST}

The [[BV-BRST formalism]] is secretly a way to talk about the fact that configuraton spaces of [[gauge theory|gauge theories]] are not naive spaces such as [[manifold]]s, but are general [[space]]s in the sense of [[higher geometry]]: 

the configuration space is really an object $Conf \in Sh_{(\infty,1)}((dgAlg^-)^{op})$ in the [[∞-stack]] [[(∞,1)-topos]] on the [[(∞,1)-site]] $(dgAlg^-)^{op}$ of certain [[algebra in an (∞,1)-category|∞-algebras]] modeled as [[dg-algebra]]s. The BV-BRST-complex of a physical system is the global [[derived geometry|derived]] function algebra 

$$
  \mathcal{O}(Conf) \in dgAlg
  \,.
$$

> (many more aspects go here, eventually)...


#### Quantum field theory {#QFT}

There are essentially two axiomatizations of what [[quantum field theory]] is, both of which are inherently $\infty$-categorical:

* in the [[FQFT]] picture -- the _Schr&#246;dinger picture_ -- a quantum field theory is described as an [[(∞,n)-functor]] on an [[(∞,n)-category of cobordisms]]. The [[cobordism hypothesis]] -- now a theorem that characteizes central properties of these [[(∞,n)-categories]], has been a major driving force in the development of [[higher category theory]].

* in the [[AQFT]]/[[factorization algebra]] picture -- the _Heisenberg picture_  -- a quantum field theory is described as an $\infty$-copresheaf of observables on its parameter space. 


##### 3d TFT and 2d CFT {#3dTFT2dCFT}

3-dimensional [[TFT]] such as [[Chern-Simons theory]] and [[Dijkgraaf-Witten theory]] and the global aspects of 2-dimensional [[conformal field theory]] are inherently governed by the theory of [[modular tensor categories]].

The local aspects of 2-dimensional conforma field theory are governed by [[vertex operator algebra]]s. A [[vertex operator algebra]] is really the [[algebra over an operad]], for the operad of holomorphic pointed spheres (as described there).

...

### In your favorite topic

...


category: meta

[[!redirects n-point of view]]
[[!redirects n-category point of view]]
[[!redirects n-categorial point of view]]
[[!redirects n-categorical point of view]]
[[!redirects n-category-theoretic point of view]]
