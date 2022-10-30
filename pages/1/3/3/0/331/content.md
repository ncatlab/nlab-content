
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

Traditionally, as a discipline, __logic__ is the study of correct methods of reasoning.  Logicians have principally studied [[deduction]], the process of passing from premises to conclusion in such a way that the truth of the former necessitates the truth of the latter. In other words, deductive logic studies what it is for an argument to be _valid_. A second branch of logic studies [[inductive reasoning|induction]], reasoning about how to assess the plausibility of general propositions from observations of their instances. This has often been done in terms of [[probability theory]], particularly Bayesian.

Some philosophers, notably [[Charles Peirce]], considered there to be third variety of reasoning for logic to study, namely, [[abduction]]. This is a process whereby one reasons to the truth of an explanation from its ability to account for what is observed. It is therefore sometimes also known as _inference to the best explanation_. At least some aspects of this can also be studied using Bayesian probability.

Deductive logic is the best developed of the branches. For centuries, treatments of the [[syllogism]] were at the forefront of the discipline. In the nineteenth century, however, spurred largely by the needs of mathematics, in particular the need to handle [[quantifiers]], a new logic emerged, known today as [[predicate logic]]. 

As we said above, logic is traditionally concerned with *correct* methods of reasoning, and philosophers (and others) have had much to say *prescriptively* about logic.  However, one can also study logic *descriptively*, taking it to be the study of methods of reasoning, without attempting to determine whether these methods are correct.

A __logic__ is a specific method of reasoning.  There are several ways to formalise this as a [[mathematics|mathematical]] object; see [[mathematical logic]].


## Category-theoretic logic

It turns out that logic is naturally expressed in the language of [[category theory]]: given any [[category]] $C$, its [[object]]s $T$ may be understood as [[type]]s of terms, and morphisms $\psi \stackrel{\Psi}{\to} T$ as [[term]]s ([[generalized element]]s of $T$). A [[proposition]] is then a [[subobject]], $\phi \hookrightarrow T$ -- the subobject of all those variables for which the proposition is true.

In summary:

* [[type theory]] deals with understanding categories in terms of their [[slice categories]], collected in their [[codomain fibration]];

* logic deals with understanding [[subobject]]s, hence [[subterminal object]]s of these slice categories.

For instance, 

* [[limit]]s and [[colimit]]s, [[exponential]]s, and [[object classifier]]s belong to the [[type theory]], 

* while [[image]]s, dual images, [[intersection]]s, [[union]]s, and [[subobject classifiers]] belong to the logic.

See also:

* [[internal language]],
* [[syntactic category]].


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
* [[evil]]
* [[excluded middle]]
* [[geometric logic]]
* [[Heyting algebra]]
* [[higher-order logic]]
* [[internal logic]]
* [[intuitionistic logic]]
* [[linear logic]]
* [[minimal logic]]
* [[modal logic]]

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

* [[type theory]], **logic**

* [[2-type theory]], [[2-logic]]

* [[(∞,1)-type theory]], [[(∞,1)-logic]]


## References

* [[Lambek]], J.; [[Philip Scott|Scott]], P.J. (1986), _Introduction to Higher Order Categorical Logic_, Cambridge University Press.
* [[Bart Jacobs]] (1999), _Categorical Logic and Type Theory_, Elsevier.
  

Historically, in some philsoophical circles 'logic' was understood in a broader sense:

* [[Hegel]], _Wissenschaft der Logik_ ( _[[Science of Logic]]_ )


[[!redirects logic]]
[[!redirects logics]]

[[!redirects categorical logic]]
[[!redirects categorial logic]]
[[!redirects category-theoretic logic]]

[[!redirects symbolic logic]]
