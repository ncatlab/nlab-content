
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


# Bishop's constructive mathematics

* table of contents
{: toc}

## Overview

In 1967, [[Errett Bishop]] revived interest and practice of [[constructive mathematics]] with his book [[Foundations of Constructive Analysis]], in which he showed that contrary to previous perceptions, large swaths of mathematics could be developed constructively with only minor changes from the classical theory.

While [[Brouwer]] had insisted that mathematics was primary to [[logic]], the [[intuitionism|intuitionists]] who followed him went more into intuitionistic [[foundations]] and [[philosophy]] than into mathematics as such.  The [[Russian constructivism|Russian school]] of constructivism focussed on [[recursion theory]] and was far removed from modern [[Bourbaki]]-style mathematics.  There was a pervasive feeling that constructive mathematics, particularly constructive [[analysis]], was simply unworkable; Bishop attacked this idea, not by arguing against it, but by simply demonstrating how constructive analysis could be done.

Bishop\'s work was primarily in [[analysis]], because constructive mathematics is more difficult at an elementary level there than in some other fields such as [[combinatorics]].  Bishop\'s style was extended to constructive [[algebra]] by his disciple [[Fred Richman]].  On the other hand, other fields such as point-set [[topology]] are so much *more* difficult constructively that Bishop did not even consider them; later authors have attacked the problem with tools such as [[apartness spaces]] and [[locales]]/[[formal topologies]].  In fact, even Bishop's treatment of analysis has actual flaws regarding the notion of continuous function (see [below](#Continuity)) that seem to be best fixed by using locales.

Bishop's work is important not only for its historical role in reviving interest in constructive mathematics and belief in its feasibility, but because the framework for constructive mathematics that he laid out has played a central role in a great deal of later work.  Known as **Bishop's constructive mathematics** and abbreviated **BISH** or **BCM**, this framework is often viewed as a sort of "common core" of all kinds of constructive mathematics.  However, this is not really a true statement about the mathematics that Bishop himself did, which in particular is not compatible with the [[internal logic]] of [[elementary toposes]] (see [below](#WhatItIs)) --- but for added confusion, some mathematicians who say they are working in "Bishop's constructive mathematics" are in fact working in a theory about which this statement *is* true.  Thus, unless one really does want to work in the mathematics that Bishop himself did, it is better to work in "pure neutral" constructive mathematics and say so explicitly, while clearly mentioning any additional principles one may be assuming.

This page will discuss Bishop's constructive mathematics *as Bishop did it*; see [[constructive mathematics]] for "pure neutral" constructive mathematics that is valid in any topos.  Unfortunately, the confusion surrounding BISH means that any individual paper claiming to use BISH must be read carefully to find out exactly what framework it *is* using.


## What is it?
 {#WhatItIs}

Bishop's constructive mathematics is often described as "obtained from classical mathematics by removing the law of [[excluded middle]] and the [[axiom of choice]]".  It is also claimed that "every other variety of constructive mathematics, including classical mathematics, can be obtained from Bishop's constructive mathematics by adding further assumptions" (e.g. [BridgesRichman](#BridgesRichman)).  However, neither of these statements is really true.

First of all, Bishop accepted the principle of [[countable choice]].  Since countable choice fails in the [[internal logic]] of many [[toposes]], this means that if we want to do constructive mathematics because it is valid in toposes, we cannot use Bishop's framework.  (Regarding countable choice see also [Richman](#Richman00).)  Similarly, although it is true (as often claimed) that "every constructive proof in BISH is also a classical proof" if by "classical" one includes both excluded middle and choice, it is not true if "classical" includes foundational theories like [[ZF]] (without the axiom of choice).

However, focusing attention on countable choice is misleading, because it may lead one to think that we could simply "remove that assumption" from BISH, and that proofs in BISH that don't happen to invoke countable choice would be topos-valid.  In fact it is not really possible to "remove countable choice" from BISH, because it is not an axiom but a *theorem*, and BISH also proves other non-topos-valid principles like the [[presentation axiom]].

The central point is the following: although the carriers of mathematical structure in BISH are, like in other mathematical frameworks, called [[sets]], BISH is not an *axiomatic [[set theory]]* but a *definitional set theory*.  That is, the notion of "set" in BISH is not an undefined one given meaning by axioms and rules the way it is in [[ZFC]] or [[ETCS]] (and also some ways of using [[type theory]] as a foundation, such as [[homotopy type theory]]).  Instead, the notion of "set" is *defined* in terms of more basic notions such as "construction" and "method".  (See [[Bishop set]].)  This definition then allows us to *prove* that sets satisfy various properties, including countable choice.  But Bishop directly uses "constructions" and "methods" throughout in addition to the "sets" that are defined from them, so his mathematics cannot be simply interpreted into an axiomatic set theory with certain assumptions added such as countable choice.

Bishop did not formalize his foundations, and in particular did not specify rules for how "constructions" and "methods" should behave.  However, many people believe that a fairly faithful reading is obtained by viewing "methods" as the [[terms]] in a [[dependent type theory]], whose [[types]] are classifiers for families of "constructions".  (Indeed, making this work was one of [[Per Martin-Lof]]'s original motivations for defining dependent type theory.)  Bishop's *logic* is then the *untruncated* [[propositions as types]] logic of this type theory, with for instance "or" interpreted as the [[sum type]] and "there exists" interpreted as the [[dependent sum type]]. Bishop: "choice is implied by the very meaning of existence".  (Other possible formalizations of Bishop's mathematics use Feferman's [[explicit mathematics]] or [[NuPrl]]. "Nuprl can be seen as expressing the philosophical ideas of Brouwer and Bishop" (expressed [here](http://www.nuprl.org/book/Overview.html) ).  Alternatively, one can try to isolate the principles implied by Bishop's definitional set theory to formulate an axiomatic set theory in which Bishop's work can be formalized --- one common proposal is [[CZF]] with the [[presentation axiom]] --- but this is getting further from what Bishop actually did.)

Thus, for instance, when Bishop says that a set is defined by specifying how to construct an element of it and how to say when two such elements are equal, we take this as meaning that a set is specified by a type $A$ and an equality relation $E : A \to A \to Type$ satisfying the laws of an [[equivalence relation]] (a.k.a. a [[setoid]] in the type theory).  And whenever Bishop says "for all $x$ there exists a $y$", he means $\prod_{x:A} \sum_{y:B}$, which by the commutation of $\Pi$ and $\Sigma$ entails the existence of a function $A\to B$.  This "function" is in the sense of the underlying type theory, i.e. an element of a function type; inside BISH it would be called a "method" or "operation", with the word "function" reserved for operations that respect the specified setoid equalities.  Since not every operation is a function, the full axiom of choice does not hold in BISH; but it does hold whenever the equality on $A$ is "minimal" or "identity" or "Leibniz" (that is, the [[identity type]] of the type theory).  In particular, since this is true for $\mathbb{N}$, countable choice holds.

Now we can see the more basic problem with saying that BISH specializes to other theories such as topos-logic or ZF.  It's not just that BISH proves statements that "don't hold" in these other theories; rather, the latter *have* no "constructions/methods" layer underneath, so there isn't even any natural way to *try* to interpret BISH into them.  (One might even argue that the same is true for the other flavors of constructivism that are generally believed to be specializations of BISH, such as Brouwer's [[intuitionistic mathematics]] and [[Russian constructivism]], but I'm not familiar enough with the philosophy of those theories to make that claim.)  The only halfhearted possibility seems to be to interpret the objects of the topos (or sets of ZF) as being the *types* in the underlying type theory; but in this case BISH is not talking about the same things as the other theory, and theorems of BISH do not specialize to the corresponding theorems of the other theory.  (For classical mathematics *with* choice, though, it happens that this specialization is correct: every setoid is isomorphic to a set, namely the actual quotient of its equality equivalence relation.)


## Relation to triposes
 {#Triposes}

One of the most distinctive aspects of Bishop's framework for mathematics is the notion that a "set" is something *equipped with an equality relation*, so that for instance we can construct a "quotient" of a set by simply equipping the same underlying "collection" with a new equality relation.  There is a way to preserve this idea in a theory that is general enough to include topos logic, but the result looks rather different from Bishop's.

First we have to allow a more general "logic" than untruncated propositions-as-types, such as the topos logic of [[subobjects]].  Semantically, this can be described as working in a [[first-order hyperdoctrine]].  Second, such a more general logic will no longer satisfy the [[unique choice|function comprehension]] (unique choice) principle *with respect to setoids* (though it may with respect to the "natural" equality of objects of the topos).  In fact it is nearly impossible for it to do so: if it does, then the morphisms in the base category of the hyperdoctrine satisfy the full axiom of choice!  For if $R$ is a total relation from $A$ to $B$ in such a hyperdoctrine, define a setoid equality on $A\times B$ by setting $(x_1,y_1) = (x_2,y_2)$ iff $x_1=x_2$ (in the minimal Leibniz sense) and $R(x_1,y_1) \leftrightarrow R(x_2,y_2)$.  Then $R$ induces a total functional relation from $A$ to $A\times B$ by $R'(x,(x',y)) = (x=x') \wedge R(x,y)$, and if there is an operation $f:A\to A\times B$ such that $R'(x,f(x))$ then $\pi_1 f : A \to B$ satisfies $R(x,\pi_1 f(x))$ and so is a choice function.

Thus, to obtain function comprehension, which is a *sine qua non* for much mathematics, we have to essentially generalize the notion of "function" to be not just an operation (a term in the underlying type theory) that preserves equality, but a total functional relation.  The "sets" in a hyperdoctrine, with the "functions" of this sort between them, are most studied in the case of [[triposes]] and are called the *tripos-to-topos construction*.

Thus, working with "sets" in tripos logic (defined there as [[partial equivalence relations]], since a tripos may lack "comprehensions" to allow us to assert conditions on a construction to define an element of a set) can be viewed as a generalization of BISH to include topos logic and ZF.  But a proof in BISH is not always valid in tripos logic, even if it doesn't explicitly invoke principles like countable choice, since it can use facts such as that every function has an underlying "operation" and that every existence statement comes with an "method" selecting its witnesses.



## Bishop's notion of continuity
 {#Continuity}

Bishop rejected the usual notion of pointwise [[continuous function]] (and more generally [[topological spaces]]) as inadequate for analysis and instead defined a "continuous function" (from $\mathbb{R}$ to $\mathbb{R}$) to be "locally uniformly continuous".  However, there is some confusion about this definition diagnosed by [Waaldijk](#Waaldijk).  In particular, the two books _FCA_ and _CA_ use different definitions, which can be reconciled only using the [[fan theorem]] (which Bishop rejected).  There is a similar problem with the notion of [[locally compact space]].  In fact, Waaldijk showed more strongly that if there is *any* notion of "kontinuous" function between subsets of $\mathbb{R}$ which is (1) closed under composition, (2) specializes on closed intervals to uniformly continuous functions, and (3) includes $f(x)= \frac{1}{x}$, then the fan theorem holds.  This seems quite damaging to the prospect of a treatment of analysis as Bishop envisioned it.

A more modern perspective is to use [[locale]] theory (or the predicative variant [[formal topologies]]) instead.  [Palmgren](#Palmgren03) shows that the continuous endomaps of the [[locale of real numbers]] $\mathbb{R}$ coincide with Bishop's locally uniformly continuous functions, whereas for spaces other than $\mathbb{R}$ itself locale maps are better-behaved than Bishops': in particular, they are of course closed under composition, and they contain inversion (suitably interpreted).  Similarly, locally compact spaces and measure theory are arguably better done with locales than spaces.  In particular, see [[localic completion]] and the references below.

Alternatively, one can consider sheaves over the localic unit interval to model the [[fan theorem]]. This approach is pushed even further in [[continuous truth]]. This may be seen as a modern approach to Brouwer's intuitions, where instead of postulating [[choice sequences]] to justify the [[fan theorem]], one works directly with representations of topological spaces and continuous functions between them. These are not unlike Bishop's basic "operations".

## References

Books about or using Bishop's constructive mathematics include:

* [[Errett Bishop]], _[[Foundations of Constructive Analysis]]_ (1967), the work which made him famous in the foundations of mathematics circles;

* [[Errett Bishop]] and [[Henry Cheng]], _Constructive Measure Theory_ (1972), featuring a better [[measure theory]] than in _FCA_;

* [[Errett Bishop]] and [[Douglas Bridges]], _Constructive Analysis_ (1985), a revised version of _FCA_, incorporating the measure theory of _CMT_.

* [[Ray Mines]], [[Fred Richman]], and [[Wim Ruitenberg]], _A course in constructive algebra_ (1988)

* [[Douglas Bridges]] and [[Luminiţa Vîţă]], _Apartness and Uniformity: A Constructive Development_ (2011)

* {#BridgesRichman}[[Douglas Bridges]] and [[Fred Richman]], _Varieties of constructive mathematics_ (1987)

Other papers mentioned above:

* {#Waaldijk} [[Frank Waaldijk]], _On the foundations of constructive mathematics - especially in relation to the theory of continuous functions_  (2001).  [web site](http://www.fwaaldijk.nl/mathematics.html)

* [[Fred Richman]], *Constructive Mathematics without Choice*,
in: *Reuniting the Antipodes -- Constructive and Nonstandard Views of the Continuum*, Synthese Library **306**, Springer (2001) 199-206 &lbrack;[doi:10.1007/978-94-015-9757-9_17](https://doi.org/10.1007/978-94-015-9757-9_17)&rbrack;
 {#Richman00}

For more about the localic approach, see:

* [[Erik Palmgren]], _Continuity on the real line and in formal spaces_. (2003). Revised version of U.U.D.M. Report 2003:32. [link](http://www2.math.uu.se/~palmgren/crealform-rvd2.pdf)
 {#Palmgren03}

* [[Erik Palmgren]], _From intuitionistic to point-free topology_ (2005) U.U.D.M. Report 2005:47. [link](http://www2.math.uu.se/~palmgren/homotopy.pdf)
 {#Palmgren05}

* [[Erik Palmgren]], _A constructive and functorial embedding of locally compact metric spaces into locales_. Topology and its Applications, 154
(2007), 1854--1880.

* [[Erik Palmgren]], _Resolution of the uniform lower bound problem in constructive analysis_, [link](http://onlinelibrary.wiley.com/doi/10.1002/malq.200710034/full)

* [[Bas Spitters]], _Locatedness and overt sublocales_, doi:10.1016/j.apal.2010.07.002 APAL

* [[Thierry Coquand]], [[Erik Palmgren]], [[Bas Spitters]], _Metric complements of overt closed sets_, Mathematical Logic Quarterly, 57(4), 373-378, 2011.  [link](http://dx.doi.org/10.1002/malq.201010011)

* T Kawai, _A point-free characterisation of Bishop locally compact metric spaces_, [link](http://www.logicandanalysis.com/index.php/jla/article/viewFile/239/120)

* T Kawai, _Localic completion of uniform spaces_, [arxiv](https://arxiv.org/pdf/1703.02255)

[[!redirects BCM]]
[[!redirects BISH]]
