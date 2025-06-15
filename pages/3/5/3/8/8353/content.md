
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

> *There are good reasons why the theorems should all be easy and the definitions hard.* &lbrack;[[Michael Spivak]], preface to "[[Calculus on Manifolds]]"&rbrack;


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[type theory]] a _definition_ is the construction of a [[type]] or a [[term]] of a certain [[type]]. By "construction", we mean that the [[type]] has a [[formation rule]] and the [[term]] has an [[introduction rule]]. Then, there are in general two ways to complete the construction: 

* by adding to the [[type theory]] the [[elimination rules]], [[computation rules]], and [[uniqueness rules]] for [[types]] and their associated [[terms]] which characterize the [[universal property]] of the type (see *[[natural deduction]]*),

* by adding to the type theory a rule stating that the type or term [[equality|is equal to]] an existing term or type.

Many types in type theory, such as [[function types]], [[product types]], [[coproduct types]], [[booleans type]], [[natural numbers type]], [[integers]], et cetera, are defined in both ways, by [[universal properties]] and by [[equality in type theory|equality]] with another type. 

## Rules for definitions and single assignment operators

One way that definitions of types and of terms could be formalized inside the type theory is by the use of [[equality in type theory|equality]] with another term or type. More specifically, every definition of a symbol $A$ comes with a **formation rule** for the symbol which states that it is a type or an **introduction rule** for the symbol which states that it is a term of a type, and a **definition rule** that the term or type $A$ is equal to some existing term or type $B$. The equality used in the definition rule is called **[[definitional equality]]**. 

As documented in the article on [[equality in type theory]], there are three notions of equality used in type theory: judgmental equality, propositional equality, and typal equality. All three notions of equality could be used in the definition rule. In [[Martin-Löf type theory]] and [[cubical type theory]], symbols and abbreviations are defined using judgmental equality. In [[ZFC]] and [[ETCS]], they are defined using propositional equality, and in [[objective type theories]], they are defined using typal equality. 

For example, suppose that the type $B$ is already derived in some context $\Gamma$. Then, in order to define the symbol $A$ to be the type $B$ there are the following formation and definition rules for $A$:

* Formation and judgmental definition rules for $A$:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A = B \; \mathrm{type}}$$

* Formation and propositional definition rules for $A$:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A = B\; \mathrm{true}}$$

* Formation and typal definition rules for $A$:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \: \mathrm{ctx}}{\Gamma \vdash \delta_A:A \simeq B}$$

Similarly, suppose that the term $b:A$ is already derived in some context $\Gamma$. Then, in order to define the symbol $a$ to be the term $b:A$ there are the following introduction and definition rules for $a$:

* Introduction and judgmental definition rules for $a$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a:A} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a = b:A}$$

* Introduction and propositional definition rules for $a$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a:A} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a =_A b \; \mathrm{true}}$$

* Introduction and typal definition rules for $a$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a:A} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \delta_a:a =_A b}$$

However, including separate rules for each new term or type is very cumbersome and would lead to an explosion of rules in the type theory. To handle that, one usually introduces the **single assignment operator**, **initialization operator**, **initialisation operator**, or **definition operator** $\coloneqq$ to the type theory, which is formally defined as a pair of judgments 

* $B \coloneqq A \; \mathrm{type}$, where we judge $B$ to be defined as the type $A$, or assigned the type $A$ 
* $b \coloneqq a:A$, where we judge $b$ to be defined as the term $a:A$, or assigned the term $a:A$ 

in addition to the [[judgments]] for [[types]], [[terms]], and [[judgmental equality]]. $B \coloneqq A \; \mathrm{type}$ is called **type definition**, **type initialization**, **type initialisation** or **type single assignment**, while $b \coloneqq a:A$ is called **term definition**, **term initialization**, **term initialisation**, or **term single assignment**. Judgmental single assignment is different from judgmental equality as judgmental equality is an [[equivalence relation]], while judgmental single assignment is not an equivalence relation, but instead has a reflection rule into [[equality in type theory|equality]]. 

Depending upon what notion of [[equality in type theory|equality]] is used for [[definitional equality]], the single assignment operator has the following formation and equality reflection rules for type definitions

* Formation and judgmental equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A\; \mathrm{type}}$$

* Formation and propositional equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A\; \mathrm{true}}$$

* Formation and typal equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash P:B \simeq A}$$

There are also the following introduction and equality reflection rules for term definitions:

* Introduction and judgmental equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv a:A}$$

* Introduction and propositional equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv_A a \; \mathrm{true}}$$

* Introduction and typal equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash p:b =_A a}$$

## Copy definitions

Another way of typally defining a type $A$ to be a type $B$ is via *[[copying]]*. Copying becomes important for typally defining the [[type of equivalences]], as the usual way of typally defining types involves the [[type of equivalences]] and thus isn't available. One add rules saying that from the [[assignment]] [[judgment]] $B \coloneqq A \; \mathrm{type}$ one can derive that $B$ satisfies the universal property of a [[copy]] of $A$. 

## Related concepts

* [[natural deduction]]

* [[copy]]


[[!include mathematical statements --- contents]]


## References

The single assignment operator is defined (not by name) in Remark 2.2.1 in:

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

See also:

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Assignment_(computer_science)#Single_assignment">Assignment (computer science)#Single assignment</a>_ 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Assignment_(computer_science)#Assignment_versus_equality">Assignment (computer science)#Assignment versus equality</a>_ 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Relational_operator#Confusion_with_assignment_operators">Relational operator#Confusion with assignment operators</a>_

[[!redirects definition]]
[[!redirects definitions]]

[[!redirects definition rule]]
[[!redirects definition rules]]

[[!redirects copy definition]]
[[!redirects copy definitions]]
[[!redirects copy-definition]]
[[!redirects copy-definitions]]

[[!redirects type definition]]
[[!redirects type definitions]]
[[!redirects term definition]]
[[!redirects term definitions]]

[[!redirects definition judgment]]
[[!redirects definition judgments]]
[[!redirects type definition judgment]]
[[!redirects type definition judgments]]
[[!redirects term definition judgment]]
[[!redirects term definition judgments]]

[[!redirects single assignment]]
[[!redirects single assignment operator]]
[[!redirects single assignment operators]]

[[!redirects single assignment judgment]]
[[!redirects single assignment judgments]]
[[!redirects type single assignment judgment]]
[[!redirects type single assignment judgments]]
[[!redirects term single assignment judgment]]
[[!redirects term single assignment judgments]]

[[!redirects initialization]]
[[!redirects initialization operator]]
[[!redirects initialization operators]]
[[!redirects initialisation]]
[[!redirects initialisation operator]]
[[!redirects initialisation operators]]

[[!redirects initialization judgment]]
[[!redirects initialization judgments]]
[[!redirects type initialization judgment]]
[[!redirects type initialization judgments]]
[[!redirects term initialization judgment]]
[[!redirects term initialization judgments]]

[[!redirects initialisation judgment]]
[[!redirects initialisation judgments]]
[[!redirects type initialisation judgment]]
[[!redirects type initialisation judgments]]
[[!redirects term initialisation judgment]]
[[!redirects term initialisation judgments]]