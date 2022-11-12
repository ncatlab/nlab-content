
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

**Mostowski set theory** is a [[well-founded relation|well-founded]] [[material set theory]] which is [[material-structural adjunction|equivalent in strength]] to the [[structural set theories]] of [[ETCS]] and bounded [[SEAR]] with [[axiom of choice|choice]]. 

## Definition

Mostowski set theory has the following [[axioms]]:

1. Full classical logic: For any formula $\phi$, $\phi \vee \neg \phi$

2. [[axiom of extensionality|Extensionality]]: for any set $x$ and $y$, $x = y$ if and only if for all $z$, $z \in x$ if and only if $z \in y$. 

3. [[empty set|Empty set]]: there is a set $\varnothing = \{\}$. 

4. Pairing: for all sets $x$ and $y$, there is a set $\{x, y\}$

5. Union: for all sets $x$, there is a set $\{z \vert \exists y \in x.z \in y\}$

6. Schema of $\Delta_0$-separation: for any $\Delta_0$-formula $\phi(x)$ and for any set $a$, there is a set $\{x \in a \vert \phi(x)\}$

7. Schema of limited $\Delta_0$-replacement: for any $\Delta_0$-formula $\phi(x, y)$, for all sets $a$ and $b$, if for any set $x \in a$ there is a unique set $y$ such that $\phi(x, y)$, and for all $z \in y$, $z \subseteq b$, then there is a set $\{y \vert \exists x \in a.\phi(x, y)\}$

8. [[power set|Power sets]]: for any set $x$, there is a set $\mathcal{P}(x) = \{y \vert y \subseteq x\}$

9. [[axiom of infinity|Infinity]]: there is a set $\omega$ such that for all sets $x$, $x \in \omega$ if and only if $x = \emptyset$ or there exists a set $y \in \omega$ such that $y \cup \{y\} = x$. 

10. [[axiom of choice|Choice]]: for any set $a$, if for all $x \in a$ there is a set $y \in x$, then there is a function $f$ from $a$ to $\bigcup a$ such that $f(x) \in x$ for all $x \in a$. 

11. [[axiom of foundation|Regularity]]: if there is a set $y \in x$, then there is a set $y \in x$ such that $x \cap y = \emptyset$

12. [[transitive closure|Transitive closure]]: every set is a subset of a smallest transitive set

13. [[Mostowski's principle]]: every well-founded extensional relation is isomorphic to a transitive set equipped with the relation $\in$

## Variations of Mostowski set theory

By removing axioms 1 and 10 from Mostowski set theory, one gets **[[constructive mathematics|intuitionistic]] Mostowski set theory**, which is equivalent in strength to a [[well-pointed topos]] with [[natural numbers object]] and the [[axiom of well-founded materialization]] (intuitionistic ETCS), or to intuitionistic bounded SEAR with the [[axiom of well-founded materialization]].

By removing axiom 8 from Mostowski set theory, one gets **[[predicative mathematics|strongly predicative]] Mostowski set theory**, which is equivalent in strength to a [[well-pointed pretopos|well-pointed]] [[Heyting pretopos]] with [[natural numbers object]] and the [[axiom of choice]]. 

By removing axiom 8 from intuitionistic Mostowski set theory and adding the **axiom of $\omega$-induction** (for any formula $\phi$, if $\phi(\emptyset)$ and for all sets $x \in \omega$, $\phi(x)$ implies that $\phi(x \cup \{x\})$, then for all sets $x \in \omega$, $\phi(x)$), one gets **[[constructive mathematics|constructive]] strongly predicative Mostowski set theory**, which is equivalent in strength to a [[well-pointed pretopos|well-pointed]] [[Heyting pretopos]] with a [[natural numbers object]] and the [[axiom of well-founded materialization]]. 

By replacing axiom 8 by the axiom of exponentiation (for all sets $a$ and $b$, the set $b^a$ of functions from $a$ to $b$ exists) in intuitionistic Mostowski set theory, one gets **[[constructive mathematics|constructive]] [[predicative mathematics|weakly predicative]] Mostowski set theory**, which is equivalent in strength to a [[well-pointed pretopos|well-pointed]] [[Heyting pretopos|Heyting]] [[ΠW-pretopos]] with the [[axiom of well-founded materialization]]. 

By removing axiom 9 from Mostowski set theory, one gets **[[finite mathematics|weakly finitist]] Mostowski set theory**, which is equivalent in strength to a [[well-pointed topos]] with the [[axiom of choice]]. 

If one replaces axiom 9 with the **[[axiom of finiteness|axiom of finiteness]]** (for any formula $\phi$, if $\phi(\emptyset)$ and for all sets $x$, $\phi(x)$ implies that $\phi(x \cup \{x\})$, then for all sets $x$, $\phi(x)$), one gets **strongly finitist Mostowski set theory**, which is equivalent in strength to the category [[FinSet]]. Axioms 8 and 10 are redundant in this formulation, since both are implied by the axiom of finiteness. 

Thus, the most general variation of Mostowski set theory is **weakly finitist, constructive strongly predicative Mostowski set theory**, which consists of axioms 2-7 and 11-13, and is equivalent in strength to a general [[well-pointed pretopos|well-pointed]] [[Heyting pretopos]] with the [[axiom of well-founded materialization]]. 

## See also

* [[material set theory]]
* [[ETCS]]

## References

* [[Michael Shulman]] (2018). Comparing material and structural set theories. [arXiv:1808.05204](https://arxiv.org/abs/1808.05204).