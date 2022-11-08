
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

> There are good reasons why the theorems should all be easy and the definitions hard. ([[Michael Spivak]], preface to "[[Calculus on Manifolds]]" )

#Contents#
* table of contents
{:toc}

## Idea

In [[type theory]] a _definition_ is the construction of a [[type]] or a [[term]] of a certain [[type]]. By construction, we mean that the type has a [[formation rule]] and the [[term]] has an [[introduction rule]]. Then, there are in general two ways to complete the construction, 

* by adding to the type theory the [[elimination rules]], [[computation rules]], and [[uniqueness rules]] for [[types]] and its associated [[terms]] which characterize the [[universal property]] of the type (see [[natural deduction]])

* by adding to the type theory a rule stating that the type or term [[equality|is equal to]] an existing term or type

Many types in type theory, such as [[function types]], [[product types]], [[coproduct types]], [[booleans type]], [[natural numbers type]], [[integers]], et cetera, are defined in both ways, by universal properties and by equality with another type. 

## Rules for definitions

One way that definitions of types and of terms could be formalized is by the use of [[equality]] with another term or type. More specifically, every definition of a symbol $A$ comes with a **formation rule** for the symbol which states that it is a type or an **introduction rule** for the symbol which states that it is a term of a type, and a **definition rule** that the term or type $A$ is equal to some existing term or type $B$. The equality used in the definition rule is called **definitional equality**. 

As documented in the article on [[equality]], there are three notions of equality used in type theory: judgmental equality, propositional equality, and typal equality. All three notions of equality could be used in the definition rule. In [[Martin-Löf type theory]] and [[cubical type theory]], symbols and abbreviations are defined using judgmental equality. In [[ZFC]] and [[ETCS]], they are defined using propositional equality, and in [[objective type theories]], they are defined using typal equality. 

For example, suppose that the type $B$ is already derived in some context $\Gamma$ or $\Gamma \vert \Phi$. Then, in order to define the symbol $A$ to be the type $B$ there are the following formation and definition rules for $A$:

* Formation and judgmental definition rules for $A$:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A = B \; \mathrm{type}}$$

* Formation and propositional definition rules for $A$:

$$\frac{\Gamma \vert \Phi \; \mathrm{ctx}}{\Gamma \vert \Phi \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \vert \Phi \; \mathrm{ctx}}{\Gamma \vert \Phi \vdash A = B\; \mathrm{true}}$$

* Formation and typal definition rules for $A$:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \: \mathrm{ctx}}{\Gamma \vdash \delta_A:A \simeq B}$$

Similarly, suppose that the term $b:A$ is already derived in some context $\Gamma$ or $\Gamma \vert \Phi$. Then, in order to define the symbol $a$ to be the term $b:A$ there are the following introduction and definition rules for $a$:

* Introduction and judgmental definition rules for $a$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a:A} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a = b:A}$$

* Introduction and propositional definition rules for $a$:

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type}}{\Gamma \vert \Phi \vdash a:A} \qquad \frac{\Gamma \vert \Phi \vdash A \; \mathrm{type}}{\Gamma \vert \Phi \vdash a =_A b \; \mathrm{true}}$$

* Introduction and typal definition rules for $a$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash a:A} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \delta_a:a =_A b}$$

For instance one usually defines the symbol $2$ to be the term $s(s(0))$ (meaning the successor of the successor of $0$) in the type of [[natural numbers]]. This is formally defined judgmentally, propositionally, and typally as follows:

* Introduction and judgmental definition rules for $2$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}}{\Gamma \vdash 2:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}}{\Gamma \vdash 2 = s(s(0)):\mathbb{N}}$$

* Introduction and propositional definition rules for $2$:

$$\frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type}}{\Gamma \vert \Phi \vdash 2:\mathbb{N}} \qquad \frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type}}{\Gamma \vert \Phi \vdash 2 =_{\mathbb{N}} s(s(0)) \; \mathrm{true}}$$

* Introduction and typal definition rules for $2$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}}{\Gamma \vdash 2:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}}{\Gamma \vdash \delta_2:2 =_{\mathbb{N}} s(s(0))}$$

Another example is the symbol $\mathrm{isProp}(A)$, which is usually defined as the type 
$$\prod_{x:A} \prod_{y:A} x =_A y$$ 
This is formally defined judgmentally, propositionally, and typally as follows:

* Formation and judgmental definition rules for $\mathrm{isProp}(A)$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isProp}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isProp}(A) = \prod_{x:A} \prod_{y:A} x =_A y \; \mathrm{type}}$$

* Formation and propositional definition rules for $\mathrm{isProp}(A)$:

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type}}{\Gamma \vert \Phi \vdash \mathrm{isProp}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vert \Phi \vdash A \; \mathrm{type}}{\Gamma \vert \Phi \vdash \mathrm{isProp}(A) = \prod_{x:A} \prod_{y:A} x =_A y\; \mathrm{true}}$$

* Formation and typal definition rules for $\mathrm{isProp}(A)$:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isProp}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash \mathrm{isProp}(A) \; \mathrm{type}}{\Gamma \vdash \delta_{\mathrm{isProp}(A)}:\mathrm{isProp}(A) \simeq \prod_{x:A} \prod_{y:A} x =_A y}$$

### Inductive and recursive definitions

Something similar happens with inductive and recursive definitions; however, there is one definition rule for every introduction rule of the type it is being defined on. For example, addition is usually defined by recursion on the natural numbers, and comes with an introduction rule and two definition rules, one for the base case $0$ and one for the inductive case $s$ the successor function: 

* Introduction and judgmental definition rules for addition $+$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash 0 + n = n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash s(m) + n = s(m + n):\mathbb{N}}$$

* Introduction and propositional definition rules for addition $+$:

$$\frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vert \Phi \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vert \Phi \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash 0 + n =_\mathbb{N} n \; \mathrm{true}} \qquad \frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vert \Phi \vdash m:\mathbb{N} \quad \Gamma \vert \Phi \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash s(m) + n =_\mathbb{N} s(m + n) \; \mathrm{true}}$$

* Introduction and typal definition rules for addition $+$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \delta_{+}^0(n):0 + n =_\mathbb{N} n} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \delta_{+}^s(m, n):s(m) + n =_\mathbb{N} s(m + n)}$$

Another example of an inductive definition is the definition of the [[transport]] function, which is given by the following introduction and definition rules:

* Introduction and judgmental definition rules for the transport function $\mathrm{tr}$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[a/x] \vdash \mathrm{tr}(x.B, a, a, \mathrm{refl}_A(a)) = \mathrm{id}_{B[a/x]}:B[a/x] \simeq B[a/x]}$$

* Introduction and propositional definition rules for the transport function $\mathrm{tr}$:

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A \quad \Gamma \vert \Phi \vdash b:A \quad \Gamma \vert \Phi \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vert \Phi \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vert \Phi[b/x] \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$

$$\frac{\Gamma \vert \Phi \vdash A \; \mathrm{type} \quad \Gamma \vert \Phi \vdash a:A \quad \Gamma, x:A, \Delta \vert \Phi \vdash B \; \mathrm{type}}{\Gamma, \Delta[a/x] \vert \Phi[a/x] \vdash \mathrm{tr}(x.B, a, a, \mathrm{refl}_A(a)) =_{B[a/x] \simeq B[a/x]} \mathrm{id}_{B[a/x]} \; \mathrm{true}}$$

* Introduction and typal definition rules for the transport function $\mathrm{tr}$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:a =_A b \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[b/x] \vdash \mathrm{tr}(x.B, a, b, p):B[a/x] \simeq B[b/x]}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma, x:A, \Delta \vdash B \; \mathrm{type}}{\Gamma, \Delta[a/x] \vdash \delta_\mathrm{tr}^{\mathrm{refl}_A}(x.B, a):\mathrm{tr}(x.B, a, a, \mathrm{refl}_A(a)) =_{B[a/x] \simeq B[a/x]} \mathrm{id}_{B[a/x]}}$$

### Copy definitions

Another way of typally defining a type $A$ to be a type $B$ is via **copying**. The rules for copying the type $A$ over to the symbol $B$ are given as follows:

Formation rules for the symbol $B$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash B \; \mathrm{type}}$$

Introduction rules for the symbol $B$:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):B}$$

Elimination rules for the symbol $B$:
$$\frac{\Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{B}^C(c, e):C[e/z]}$$

Computation rules for the symbol $B$:
$$\frac{\Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{B}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

Uniqueness rules for the symbol $B$:
$$\frac{\Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{B}:u[e/z] =_{C[e/z]} \mathrm{ind}_{B}^C(c, e)}$$

Copying becomes important for typally defining the [[type of equivalences]], as the usual way of typally defining types involves the [[type of equivalences]] and thus isn't available. 

## The single assignment operator

In type theory, the **single assignment operator**, **initialization operator**, **initialisation operator**, or **definition operator** $\coloneqq$ is formally defined as a pair of judgments 

* $B \coloneqq A \; \mathrm{type}$, where we judge $B$ to be defined as the type $A$, or assigned the type $A$ 
* $b \coloneqq a:A$, where we judge $b$ to be defined as the term $a:A$, or assigned the term $a:A$ 

in addition to the [[judgments]] for [[types]], [[terms]], and [[judgmental equality]]. $B \coloneqq A \; \mathrm{type}$ is called **type definition**, **type initialization**, **type initialisation** or **type single assignment**, while $b \coloneqq a:A$ is called **term definition**, **term initialization**, **term initialisation**, or **term single assignment**. Judgmental single assignment is different from judgmental equality as judgmental equality is an [[equivalence relation]], while judgmental single assignment is not an equivalence relation, but instead has a reflection rule into [[equality]]. 

Depending upon what notion of [[equality]] is used for [[definitional equality]], the single assignment operator has the following formation and equality reflection rules for type definitions

* Formation and judgmental equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A\; \mathrm{type}}$$

* Formation and propositional equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \equiv A\; \mathrm{true}}$$

* Formation and typal equality reflection rules for type definition:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash P:B \simeq A}$$

There is an alternative to the typal structural rules for type definitions, which use the [[natural deduction]] rules for copying types instead of a reflection rule into an [[equivalence of types]]:

* Formation and introduction rules for type definitions
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type}}{\Gamma \vdash B \; \mathrm{type}} \qquad \frac{\Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{copy}(a):B}$$

* Elimination rules for type definitions
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B}{\Gamma \vdash \mathrm{ind}_{B}^C(c, e):C[e/z]}$$

* Computation rules for type definitions rules:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_B:\mathrm{ind}_{B}^C(c, \mathrm{copy}(a)) =_{C[\mathrm{copy}(a)/z]} c[a/x]}$$

* Uniqueness rules for type definitions rules:
$$\frac{\Gamma \vdash B \coloneqq A \; \mathrm{type} \quad \Gamma, z:B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{copy}(x)/z] \quad \Gamma \vdash e:B \quad \Gamma, y:B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{copy}(u):u[\mathrm{copy}(a)/y] =_{C[\mathrm{copy}(a)/y]} c[a/x]}{\Gamma \vdash \eta_{B}:u[e/z] =_{C[e/z]} \mathrm{ind}_{B}^C(c, e)}$$

There are also the following introduction and equality reflection rules for term definitions:

* Introduction and judgmental equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv a:A}$$

* Introduction and propositional equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b \equiv_A a \; \mathrm{true}}$$

* Introduction and typal equality reflection rules for term definition:
$$\frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash b:A} \qquad \frac{\Gamma \vdash b \coloneqq a:A}{\Gamma \vdash p:b =_A a}$$

## History

According to [PML (1980), p. 31](#PML):

> Definitional equality is intensional equality, or equality of meaning (synonymy). [...] It is a relation between linguistic expressions [...] Definitional equality is the equivalence relation generated by abbreviatory definitions, changes of [[bound variables]] and the [[principle of substituting equals for equals]]. [...] Definitional equality can be used to rewrite expressions [...].

on p. 60:

> ... intensional (sameness of meaning) ...

The notion of definitional equality was introduced first in [[AUTOMATH]]. The following paper presents a suggestive explanation of this notion and how proof-checking was designed in this system (especially section 10):

[On the roles of types in mathematics](http://uf-ias-2012.wikispaces.com/file/view/deB1.pdf/401388596/deB1.pdf)

The notion of definitional equality was later introduced by [[Per Martin-Löf]], first in the context of normalization proofs for higher-order logic in the paper [Hauptsatz for Intuitionistic Simple Type Theory](http://www.sciencedirect.com/science/article/pii/S0049237X09703659) and generalized in Type Theory. He discusses this notion in the paper [About Models for Intuitionistic Type Theory and The notion of Definitional Equality](http://www.sciencedirect.com/science/article/pii/S0049237X08707274).

The extension from AUTOMATH is that one adds the notion of data type (natural number), of constructors (zero and successor) and primitive recursion as definitional equality. The motivation is that one can consider the schema of primitive recursion as a definition of a function.

This was also influenced by natural deduction, where constructors correspond to introduction rules and the work of Gödel on system T.

With this extension, one obtains a programming language with dependent types and where computations correspond to unfolding of definitions (that can be primitive recursive definitions). This programming language has the feature that all computations terminate. This has been also considered in functional programming, see e.g. the discussion in [this paper](http://uf-ias-2012.wikispaces.com/file/view/turner.pdf/401400700/turner.pdf).

A description of the evaluation algorithm using techniques from functional programming
can be found in [this work of Gregoire and Leroy](http://uf-ias-2012.wikispaces.com/file/view/strong-reduction.pdf/402005168/strong-reduction.pdf).  

## Related concepts

* [[natural deduction]]

* [[axiom]]

* [[definition]]

  * [[inductive definition]]

  * [[coinductive definition]]

* [[theory]]

* [[lemma]]

* [[proposition]]/[[type]] ([[propositions as types]]) 

* [[proof]]/[[program]] ([[proofs as programs]])

* [[theorem]]

* [[example]]

* [[counterexample]]

* [[conjecture]]

* [[folklore]]

* [[analogy]]

* [[paradox]]

* [[exercise]]

## References

There is 

* [[Kurt Gödel]], _Über eine bisher noch nicht benützte Erweiterung des finiten Standpunktes_. Dialectica (1958), pp. 280–287, 

which might be the first paper to mention intensional equality (and the fact that it should be decidable), and there is

* [[Nicolaas de Bruijn]], _[[Automath]]_, 

where de Bruijn makes a distinction between definitional equality and "book" equality.

Copying types could be found in 

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

and the single assignment operator is defined (not by name) in Remark 2.2.1 in:

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

See also:

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Assignment_(computer_science)#Single_assignment">Assignment (computer science)#Single assignment</a>_ 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Assignment_(computer_science)#Assignment_versus_equality">Assignment (computer science)#Assignment versus equality</a>_ 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Relational_operator#Confusion_with_assignment_operators">Relational operator#Confusion with assignment operators</a>_

[[!redirects definition]]
[[!redirects definitions]]

[[!redirects definition rule]]
[[!redirects definition rules]]

[[!redirects definitional equality rule]]
[[!redirects definitional equality rules]]

[[!redirects definitional identity]]
[[!redirects definitional identities]]
[[!redirects definitional equality]]
[[!redirects definitional equalities]]

[[!redirects intensional identity]]
[[!redirects intensional identities]]
[[!redirects intensional equality]]
[[!redirects intensional equalities]]
[[!redirects extensional equality]]
[[!redirects extensional equalities]]

[[!redirects copying]]
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