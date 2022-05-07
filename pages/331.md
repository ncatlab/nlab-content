
> 'Contrariwise,' continued Tweedledee, 'if it was so, it might be; and if it were so, it would be; but as it isn't, it ain't. That's logic.' 

> (Lewis Carroll, _[Through the Looking Glass](http://sabian.org/looking_glass4.php)_)

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Logic
* table of contents
{: toc}

## Idea

Traditionally, as a discipline, __logic__ is the study of correct methods of reasoning.  Logicians have principally studied [[deduction]], the process of passing from premises to conclusion in such a way that the [[truth]] of the former necessitates the truth of the latter. In other words, deductive logic studies what it is for an argument to be _valid_. A second branch of logic studies [[inductive reasoning|induction]], reasoning about how to assess the plausibility of general propositions from observations of their instances. This has often been done in terms of [[probability theory]], particularly [[Bayesian reasoning|Bayesian]].

Some [[philosophy|philosophers]], notably [[Charles Peirce]], considered there to be third variety of reasoning for logic to study, namely, [[abduction]]. This is a process whereby one reasons to the truth of an explanation from its ability to account for what is observed. It is therefore sometimes also known as _inference to the best explanation_. At least some aspects of this can also be studied using Bayesian probability.

Deductive logic is the best developed of the branches. For centuries, treatments of the [[syllogism]] were at the forefront of the discipline. In the nineteenth century, however, spurred largely by the needs of [[mathematics]], in particular the need to handle [[relations]] and [[quantifiers]], a new logic emerged, known today as [[predicate logic]]. 

As we said above, logic is traditionally concerned with *correct* methods of reasoning, and philosophers (and others) have had much to say *prescriptively* about logic.  However, one can also study logic *descriptively*, taking it to be the study of methods of reasoning, without attempting to determine whether these methods are correct. One may study [[constructive logic]], or a [[substructural logic]], without saying that it should be adopted. Also psychologists study how people actually reason rapidly in situations without full information, such as by the [fast and frugal](http://fastandfrugal.com/) approach.

A __logic__ is a specific method of reasoning.  There are several ways to _formalise_ a logic as a [[mathematics|mathematical]] object; see at _[Mathematical Logic](#MathematicalLogic)_ below.


## Mathematical logic
 {#MathematicalLogic}

_Mathematical logic_ or _symbolic logic_ is the study of logic and [[foundations]] of mathematics as, or via, formal systems -- _[[theories]]_ --  such as [[first-order logic]] or [[type theory]].


### Classical subfields

The classical subfields of mathematical logic are

* [[set theory]]

* [[model theory]],

* [[recursion theory]]

* [[proof theory]]

### Categorical logic
 {#CategoricalLogic}

By a convergence and unification of concepts that has been named _[[computational trinitarianism]]_, mathematical logic is equivalently incarnated in 

1. [[type theory]]

1. [[category theory]]

1. [[programming theory]]

The logical theory that is specified by and specifies a given [[category]] $\mathcal{C}$ -- called its _[[internal logic]]_, see there for more details and also see [[internal language]], [[syntactic category]].
-- is the one 

* whose [[types]] are the [[objects]] $A$ of $\mathcal{C}$;

* whose [[contexts]] are the [[slice categories]] $\mathcal{C}_{/A}$;

* whose [[propositions]] in context are the [[(-1)-truncated objects]] $\phi$ of $\mathcal{C}_{/A}$;

* whose [[proofs]] $A \vdash PhiIsTrue : \phi $ are the [[generalized elements]] of $\phi$.

Hence pure mathematical logic in the sense of the study of [[propositions]] is identified with [[(0,1)-category theory]]: where one concentrates only on [[(-1)-truncated objects]]. Genuine [[category theory]], which is about [[0-truncated objects]], is the home for logic and [[set theory]], or rather [[type theory]], the 0-truncated objects being the [[sets]]/[[types]]/[[hSet|h-sets]]. 

For instance, 

* [[limits]] and [[colimits]], [[exponentials]], and [[object classifiers]] belong to the [[type theory]];

* while their (-1)-truncation, in this order: [[intersections]]/([[and]]), [[unions]]([[or]]), [[implications]], and [[subobject classifiers]], belong to the logic.

Generally, [[(∞,1)-category theory]], which is about untruncated objects, is the home for logic and types with a [[constructive mathematics|constructive]] notion of [[equality]], the [[identity types]] in [[homotopy type theory]].

See also at _[categorical model theory](model%20theory#CategoricalModelTheory)_.

## Entries on logic

* [[axiom of choice]]
* [[Boolean algebra]]
* [[algebraic models for modal logics|Boolean algebra with operators]]
* [[boolean domain]]
* [[boolean function]]
* [[boolean-valued function]]
* [[classical logic]]
* [[constructive mathematics]]
* [[context]]
* [[equality]]
* [[principle of equivalence]]
* [[excluded middle]]
* [[geometric logic]]
* [[Heyting algebra]]
* [[higher-order logic]]
* [[internal logic]]
* [[intuitionistic logic]]
* [[linear logic]]
* [[logicality and invariance]]
* [[minimal logic]]
* [[modal logic]]
* [[adjoint logic]]

   * [[algebraic models for modal logics]]
      * [[closure algebra]]
      * [[monadic algebra]]
      * [[temporal algebra]]
   * [[arrow logic]]
   * [[epistemic logic]]
      * [[the logic K(m)]]
      * [[the logic T(m)]]
      * [[the logic S4(m)]]
      * [[the logic S5(m)]]
   * [[frame (modal logic)]]
   * [[geometric models for modal logics]]
   * [[modal type theory]]
   * [[temporal logic]]     
* [[negation]]
* [[Peirce's law]]
* [[predicate]]
* [[predicate logic]]
* [[predicative mathematics]]
* [[propositional logic]]
* [[relation]]
* [[truth value]]
* [[type]]
* [[type theory]]


## Related concepts

* [[mathematical logic]]

* [[logic symbols]]

* [[type theory]], **logic**

* [[2-type theory]], [[2-logic]]

* [[(∞,1)-type theory]], [[(∞,1)-logic]]

* [[objective and subjective logic]]

[[!include logic symbols -- table]]

## References

### General
 {#General}

For centuries, logic was [[Aristotle's logic]] of [[deduction]] by [[syllogism]]. In the 19th century the idea of [[objective logic]] as [[metaphysics]] was influential

* [[Hegel]], _Wissenschaft der Logik_ ( _[[Science of Logic]]_ )

This "old logic" was famously criticized 

* [[Bertrand Russell]], _[[Logic as the Essence of Philosophy]]_, 1914

as opposed to the "new logic" of [[Peano]] and [[Frege]], contemporary [[predicate logic]].

The first textbook on mathematical logic is

* {#HilbertAckermann59} [[David Hilbert]], [[Wilhelm Ackermann]], _Grundz&#252;ge der Theoretischen Logik_ , 4th ed. Springer Heidelberg 1959 [1928]

Modern textbooks on mathematical logic include

* [[Open Logic Project]], _The open logic text_ ([pdf](http://people.ucalgary.ca/~rzach/static/open-logic/open-logic-complete.pdf))

### On categorical logic
 {#ReferencesCategoricalLogic}

* [[William Lawvere]], _[[Adjointness in Foundations]]_, Dialectica 23 (1969), 281-296

* [[William Lawvere]]  _Equality in hyperdoctrines and comprehension schema as an adjoint functor_.  In A. Heller, ed., _Proc. New York Symp. on Applications of Categorical Algebra_, pp. 1--14.  AMS, 1970. ([[LawvereComprehension.pdf:file]])

* [[Pierre Cartier]], _Logique, cat&#233;gories et faisceaux_, S&#233;minaire Bourbaki, 20 (1977-1978), Exp. No. 513, 24 p. ([numdam]( http://www.numdam.org/item?id=SB_1977-1978__20__123_0))

* [[Lambek]], J.; [[Philip Scott|Scott]], P.J. (1986), _Introduction to Higher Order Categorical Logic_, Cambridge University Press.

* [[Jim Lambek]], [[Phil Scott]], _Reflections on the categorical foundations of mathematics_ ([pdf](https://www.site.uottawa.ca/~phil/papers/LS11.final.pdf))

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

* [[Bart Jacobs]], _Categorical Logic and Type Theory_, (1999) Elsevier 

* [[John Bell]], _The development of categorical logic_ ([pdf](http://publish.uwo.ca/~jbell/catlogprime.pdf))

* [[Jean-Yves Girard]], _[[Lectures on Logic]]_, European Mathematical Society 2011

* [[Jean-Pierre Marquis]], [[Gonzalo Reyes]], (2009) _The History of Categorical Logic 1963-1977 ([pdf](https://www.webdepot.umontreal.ca/Usagers/marquisj/MonDepotPublic/HistofCatLog.pdf))

* [[Jacob Lurie]], *Categorical Logic*, Lecture notes 2018 ([web](https://www.math.ias.edu/~lurie/278x.html))

[[!include REF MakkaiReyes77]]


### Logic in natural languages

* Pieter A. M. Seuren, _The logic of language_, vol. II of Language from within; (vol. I: _Language in cognition_) Oxford University Press 2010

[[!redirects logic]]
[[!redirects logics]]

[[!redirects categorical logic]]
[[!redirects categorial logic]]
[[!redirects category-theoretic logic]]

[[!redirects symbolic logic]]