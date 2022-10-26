
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

In [[type theory]] a _definition_ is the construction of a [[type]] or a [[term]] of a certain [[type]]. 

As such definitions are no different from [[proofs]] of [[theorems]] (due [[propositions-as-types]]). For instance the [[constructive mathematics|constructive]] proof that there _exists_ a [[natural number]] consists of exhibiting one, and hence the definition of, say $2 \in \mathbb{N}$ is the same as a specific proof that $\exists x \in \mathbb{N}$.

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

### Inductive and recursive definitions

Something similar happens with inductive and recursive definitions; however, there is one definition rule for every introduction rule of the type it is being defined on. For example, addition is usually defined by recursion on the natural numbers, and comes with an introduction rule and two definition rules, one for the base case $0$ and one for the inductive case $s$ the successor function: 

* Introduction and judgmental definition rules for addition $+$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash 0 + n = n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash s(m) + n = s(m + n):\mathbb{N}}$$

* Introduction and propositional definition rules for addition $+$:

$$\frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vert \Phi \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vert \Phi \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash 0 + n =_\mathbb{N} n \; \mathrm{true}} \qquad \frac{\Gamma \vert \Phi \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vert \Phi \vdash m:\mathbb{N} \quad \Gamma \vert \Phi \vdash n:\mathbb{N}}{\Gamma \vert \Phi \vdash s(m) + n =_\mathbb{N} s(m + n) \; \mathrm{true}}$$

* Introduction and typal definition rules for addition $+$:

$$\frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash m + n:\mathbb{N}} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \delta_{+}^0(n):0 + n =_\mathbb{N} n} \qquad \frac{\Gamma \vdash \mathbb{N} \; \mathrm{type}\quad \Gamma \vdash m:\mathbb{N} \quad \Gamma \vdash n:\mathbb{N}}{\Gamma \vdash \delta_{+}^s(m, n):s(m) + n =_\mathbb{N} s(m + n)}$$

## The initialization operator

Section to be written on the use of $\coloneqq$ in mathematics; for the time being, see [[initialization operator]]. 

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