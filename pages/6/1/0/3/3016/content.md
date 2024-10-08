
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

[Wikipedia](http://en.wikipedia.org/wiki/Main_Page) enforces its entries to adopt an [NPOV](https://en.wikipedia.org/wiki/Wikipedia:Neutral_point_of_view) -- a _neutral point of view_.  This is appropriate for an encyclopedia.

However, [[About|the nLab is not Wikipedia]], nor is it an encyclopedia, although it does aspire to provide a useful reference in many areas (among its other purposes).  In particular, many parts of the $n$Lab *have* a particular point of view, which we may call the **$n$-point of view** ($n$POV) or the **[[higher structures]] point of view**, encompassing [[higher algebra|higher algebraic]], [[homotopy theory|homotopical]], or [[higher category theory|n-]] [[category theory|categorical]] point of views.

To some extent the $n$POV is just the observation that [[homotopy theory]]/[[algebraic topology]], ([[homotopy type theory|homotopy]]) [[type theory]], ([[higher category theory|higher]]) [[category theory]] and ([[higher algebra|higher]]) [[categorical algebra]] have a plethora of useful applications.


\tableofcontents

## Idea

Around the [[HomePage|nLab]] it is widely believed that [[homotopy theory]]/[[algebraic topology]], ([[homotopy type theory|homotopy]]) [[type theory]], ([[higher category theory|higher]]) [[category theory]] and ([[higher algebra|higher]]) [[categorical algebra]] provide a point of view on [[Mathematics]], [[Physics]] and [[Philosophy]] which is a valuable unifying point of view for the understanding of the concepts involved.

In particular, at the $n$Lab, there is no commitment to being neutral.  There are certainly other valid points of view on mathematics, but describing them and being neutral towards them is not the purpose of the $n$Lab.  Rather, the $n$Lab starts from the premise that homotopy theory/algebraic topology, (homotopy) type theory, (higher) category theory and (higher) categorical algebra are a useful point of view, and one of its aims is to expose this point of view generally and in a multitude of examples, and thereby accumulate evidence for it.

If you feel skeptical about the $n$-point of view, you should still find the $n$Lab useful, as the largest site for detailed category-theoretic and homotopy-theoretic information online. You are very much welcome to contribute relevant content even if you are such a skeptic.


### Category theory

As recalled in parts on the page on [[category theory]], category theorists have early on, beginning in the 1960s, proclaimed the advantages of category theory over other points of view. It has been observed that this claim, or at least the way it has been put forward, has contributed to a certain alienation of category theory in parts of the mathematical community. That may be true and is understandable. But since a claim is not false _just_ because it is put forward with possibly unpleasant boldness, all evidence for the claim deserves to be collected and exposed. We hope the $n$Lab to play a role in this effort.

In particular, there have been dramatic developments since the 1960s. Back then promoting category theory may have been as visionary as the invention of [[complex numbers]] was in the 16th century. But just as the early rejections of the complex numbers appear strangely out of place from today's perspective, where their ubiquity proves their reality to the point that it is hard to imagine how life must have been before their conception, so developments of category theory and its applications in the last years have in many areas brought it to the point that rejecting its prevalence amounts (we believe) to rejecting the obvious and ubiquitous. But also mathematics as a whole has drastically grown since then, and while category theory has become an entirely obvious ingredient in areas such as [[homotopy theory]], [[homological algebra]], [[algebraic geometry]] and even fields like [[topological quantum field theory]], its similar role to be played in many other areas has often not found wide recognition yet. But this is gradually changing. 

### Higher algebra/Homotopy theory/Type theory

From the perspective of [[higher algebra]], [[homotopy theory]], and [[type theory]], the fundamental objects of mathematics are [[homotopy types]] or [[infinity-groupoid|$\infty$-groupoids]], and the $n$-truncated versions of them, the [[n-groupoid|$n$-groupoids]], due to their differing treatment of [[equality]]/[[equivalence]] of such objects. This perspective is somewhat different from the perspective of category theory, as category theory takes $n$-categories to be more fundamental than $n$-groupoids, while these branches of mathematics view $n$-categories merely as $n$-groupoids with additional higher structure on top of the [[core]] $n$-groupoid. In particular, $n$-categories are merely specific kinds of [[directed (n,r)-graph|directed $(n,r)$-graphs]]. 

On the other hand, from this perspective, if one were to take the directed structure to be more fundamental as one does in category theory, then the fundamental structures would end up being $n$-[[n-poset|posets]] rather than $n$-[[n-category|categories]]; in particular, taking [[preorder]] to be more fundamental than [[equivalence relations]]/[[equality]]. 

## The role of the $n$POV {#RoleOfnPOV}

### Category theory

Practitioners of category theory have often attempted to express the striking power of category theory (or general conceptual methods), sometimes through aphorism, sometimes through metaphor. Early on, [[Peter Freyd]] wrote 

> Perhaps the purpose of categorical algebra is to show that which is trivial is trivially trivial.

This can be taken to mean that one thing category theory does is help make the softer bits seem utterly natural and obvious, so as to quickly get to the heart of the matter, isolating the hard nuggets, which one may then attack with abandon. This is an invaluable service category theory performs for mathematics; therefore, category theory is plain good pragmatics. 

However, it is also possible to take it a step beyond the pragmatic attitude, and see category theory (and now higher category theory) as exemplifying a style for doing even hard mathematics, as in the style for which Grothendieck is renowned. Paraphrasing from Colin McLarty's [excellent essay](http://webusers.imj-prg.fr/~leila.schneps/grothendieckcircle/Mathbiographies/mclarty1.pdf), let us regard the aforementioned pragmatic attitude as leading up to the _hammer-and-chisel principle_: if you think of a theorem to be proved as a nut to be opened, so as to reach "the nourishing flesh protected by the shell" (Grothendieck), then one thing to do is "put the cutting edge of the chisel against the shell and strike hard. If needed, begin again at many different points until the shell cracks -- and you are satisfied." Grothendieck points to Serre as a master of this technique. He then says: 

> I can illustrate the second approach with the same image of a nut to be opened. The first analogy which came to my mind is of immersing the nut in some softening liquid, and why not simply water? From time to time you rub so the liquid penetrates better, and otherwise you let time pass. The shell becomes more flexible through weeks and months -- when the time is ripe, hand pressure is enough, the shell opens like a perfectly ripened avocado! 

> A different image came to me a few weeks ago. The unknown thing to be known appeared to me as some stretch of earth or hard marl, resisting penetration... the sea advances insensibly in silence, nothing seems to happen, nothing moves, the water is so far off you hardly hear it... yet it finally surrounds the resistant substance. (Translated from the French by McLarty)

This arresting metaphor of "la mer qui monte" ("[[the rising sea]]"), which over time changes the very form of the resistant substance, is very much in the style of Grothendieck himself. McLarty quotes Deligne as saying that a typical Grothendieck proof consists of a long series of trivial steps where "nothing seems to happen, and yet at the end a highly non-trivial theorem is there." 


## Examples

For an (incomplete) list of examples of topics for which the $n$POV has proven to be a useful perspective, see

* [[applications of (higher) category theory]]


category: meta


[[!redirects higher structures point of view]]

[[!redirects n-category point of view]]
[[!redirects n-categorial point of view]]
[[!redirects n-categorical point of view]]
[[!redirects n-category-theoretic point of view]]
[[!redirects n-point of view]]