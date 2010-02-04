[[!include contents]]


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


## Examples

The following is a (incomplete) list of examples of topics for which the $n$POV has proven to be a useful perspective. 


### In geometry

The field of [[differential geometry]] has long managed to avoid the change to an $n$-point of view that had been found to be unavoidable, natural and fruitful in algebraic geometry long ago. But more recently -- not the least due to the recognition of differential [[higher geometry|higher geometric]] structures in the physics of [[gauge theory]] and [[supergravity]] (such as that of [[orbifold]]s and [[orientifold]]s, of smooth [[gerbe]]s and smooth [[principal ∞-bundle]]s) -- [[sheaf and topos theory|sheaf and topos theoretic]] concepts, such as [[synthetic differential geometry]], [[diffeological space]]s and [[differentiable stack]]s are gaining wider recognition and appreciation. 

For instance the ordinary category [[Diff]] of smooth [[manifold]]s fails to have all [[pullback]]s, it only has pullbacks along [[transversal map]]s.
This observation is usually the starting point for realizing that differential geometry is in need of a bit of [[category theory]] in the form of [[higher geometry]]. 

In all notions of [[generalized smooth space]]s all pullbacks do exist. But they may still not be the "right" pullbacks. For instance cohomology of pullback objects may not have the expected properties. This is solved by passing to smooth [[derived stack]]s, such as [[derived smooth manifold]]s.


Recent developments in [[higher category theory]], such as the concept of higher [[Structured Spaces]] based on [[Higher Topos Theory]], put all these notions of generalized geometries into a unified picture of [[higher geometry]] that realizes old ideas about how category theory provides a language for [[space and quantity]] in great detail and powerful generality and sheds new light on old [[classical mathematics|classical]] problems such the description of the [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves|derived moduli stack of derived elliptic curves]] and the construction of the [[tmf]] [[spectrum]] from it.
This construction is probably literally _unthinkable_ without adopting the $n$-point of view when approaching it. Using this point of view, the general strategy for approaching it however becomes naturally evident.

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


### In deformation theory {#DeformationTheory}

In deformation theory it was early on recognized that for a good theory the notion of [[Kähler differential]]s has to be generalized to the notion of [[cotangent complex]]. With the advent of the study of derived [[moduli space]]s, such as the [[A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves|derived moduli space of derived elliptic curves]], this needed to be further generalized to notions of cotangent complexes not just of [[ring]]s, but of [[E-∞-ring]]s. 

It turns out that all these concepts are special cases of a construction obtained from a simple higher categorical notion, that of [[left adjoint]] [[section]]s of a [[tangent (∞,1)-category]]. 

### In logic {#Logic}

* In Martin-L&#246;f [[type theory]], from a [[type]] $A$ and elements $a, b \in A$, we construct a new type $Id(a, b)$ whose elements are to be thought of as proofs that $a$ and $b$ are propositionally equal. The type-theoretic [[functions]] $1 \to Id(a, a)$, $Id(b, c) \times Id(a, b) \to Id(a, c)$ and $Id(a, b) \to Id(b, a)$ express the [[equivalence relation|reflexivity, transitivity and symmetry]] of propositional [[equality]]. The type $A$ may be thought of as a [[groupoid]], but only by quotienting out by equations expressing associativity. As with the homotopy theoretic case, it makes sense not to do so. Then the type $A$ may be thought of as an [[∞-groupoid]].  See _[Homotopy theoretic models of identity types](http://arxiv.org/abs/0709.0248)_ by [[Michael Warren]] and [[Steve Awodey]].

...

### In your favorite topic

...


category: meta

[[!redirects n-point of view]]
[[!redirects n-category point of view]]
[[!redirects n-categorial point of view]]
[[!redirects n-categorical point of view]]
[[!redirects n-category-theoretic point of view]]
