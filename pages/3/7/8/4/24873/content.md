
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

### In classical logic

We assume that we are working in full [[classical logic]]. Mostowski set theory has the following [[axioms]]:

1. [[axiom of extensionality|Extensionality]]: for any set $x$ and $y$, $x = y$ if and only if for all $z$, $z \in x$ if and only if $z \in y$. 

2. [[empty set|Empty set]]: there is a set $\varnothing = \{\}$. 

3. Pairing: for all sets $x$ and $y$, there is a set $\{x, y\}$

4. Union: for all sets $x$, there is a set $\{z \vert \exists y \in x.z \in y\}$

5. Schema of $\Delta_0$-separation: for any $\Delta_0$-formula $\phi(x)$ and for any set $a$, there is a set $\{x \in a \vert \phi(x)\}$

6. Schema of limited $\Delta_0$-replacement: for any $\Delta_0$-formula $\phi(x, y)$, for all sets $a$ and $b$, if for any set $x \in a$ there is a unique set $y$ such that $\phi(x, y)$, and for all $z \in y$, $z \subseteq b$, then there is a set $\{y \vert \exists x \in a.\phi(x, y)\}$

7. [[power set|Power sets]]: for any set $x$, there is a set $\mathcal{P}(x) = \{y \vert y \subseteq x\}$

8. [[axiom of infinity|Infinity]]: there is a set $\omega$ such that for all sets $x$, $x \in \omega$ if and only if $x = \emptyset$ or there exists a set $y \in \omega$ such that $y \cup \{y\} = x$. 

9. [[axiom of choice|Choice]]: for any set $a$, if for all $x \in a$ there is a set $y \in x$, then there is a function $f$ from $a$ to $\bigcup a$ such that $f(x) \in x$ for all $x \in a$. 

10. [[axiom of foundation|Regularity]]: if there is a set $y \in x$, then there is a set $y \in x$ such that $x \cap y = \emptyset$

11. [[transitive closure|Transitive closure]]: every set is a subset of a smallest transitive set

12. [[Mostowski's principle]]: every well-founded extensional relation is isomorphic to a transitive set equipped with the relation $\in$. 

This implies that Mostowski set theory is equivalent in strength to [[ETCS]], a [[well-pointed]] [[Boolean topos]] with [[natural numbers object]] and the [[axiom of choice]]. 

#### Variations of Mostowski set theory in classical logic

By removing axiom 9 from Mostowski set theory, one gets **Mostowski set theory without choice**, which is equivalent in strength to a [[well-pointed]] [[Boolean topos]] with [[natural numbers object]] and the [[axiom of well-founded materialization]].

By removing axiom 7 from Mostowski set theory, one gets **[[predicative mathematics|predicative]] Mostowski set theory**, which is equivalent in strength to a [[well-pointed]] [[Boolean pretopos]] with [[natural numbers object]] and the [[axiom of choice]]. 

By removing axiom 8 from Mostowski set theory, one gets **[[finite mathematics|weakly finitist]] Mostowski set theory**, which is equivalent in strength to a [[well-pointed]] [[Boolean topos]] with the [[axiom of choice]]. 

If one replaces axiom 8 with the **[[axiom of finiteness]]** (for any formula $\phi$, if $\phi(\emptyset)$ and for all sets $x$, $\phi(x)$ implies that $\phi(x \cup \{x\})$, then for all sets $x$, $\phi(x)$), one gets **strongly finitist Mostowski set theory**, which is equivalent in strength to the category [[FinSet]]. Axioms 7 and 9 are redundant in this formulation, since both are implied by the axiom of finiteness. 

Thus, the most general variation of Mostowski set theory in classical logic is **weakly finitist predicative Mostowski set theory without choice**, which consists of axioms 1-6 and 10-12, and is equivalent in strength to a general [[well-pointed]] [[Boolean pretopos]] with the [[axiom of well-founded materialization]]. 

### In intuitionisitc logic

Now, we assume that we are working in [[intuitionistic logic]]. Then **classical Mostowski set theory** has the following [[axioms]]:

1. [[axiom of extensionality|Extensionality]]: for any set $x$ and $y$, $x = y$ if and only if for all $z$, $z \in x$ if and only if $z \in y$. 

2. [[empty set|Empty set]]: there is a set $\varnothing = \{\}$. 

3. Pairing: for all sets $x$ and $y$, there is a set $\{x, y\}$

4. Union: for all sets $x$, there is a set $\{z \vert \exists y \in x.z \in y\}$

5. Schema of $\Delta_0$-separation: for any $\Delta_0$-formula $\phi(x)$ and for any set $a$, there is a set $\{x \in a \vert \phi(x)\}$

6. Schema of limited $\Delta_0$-replacement: for any $\Delta_0$-formula $\phi(x, y)$, for all sets $a$ and $b$, if for any set $x \in a$ there is a unique set $y$ such that $\phi(x, y)$, and for all $z \in y$, $z \subseteq b$, then there is a set $\{y \vert \exists x \in a.\phi(x, y)\}$

7. [[power set|Power sets]]: for any set $x$, there is a set $\mathcal{P}(x) = \{y \vert y \subseteq x\}$

8. [[axiom of infinity|Infinity]]: there is a set $\omega$ such that for all sets $x$, $x \in \omega$ if and only if $x = \emptyset$ or there exists a set $y \in \omega$ such that $y \cup \{y\} = x$. 

9. [[axiom of choice|Choice]]: for any set $a$, if for all $x \in a$ there is a set $y \in x$, then there is a function $f$ from $a$ to $\bigcup a$ such that $f(x) \in x$ for all $x \in a$. 

10. [[axiom of foundation|Regularity]]: if there is a set $y \in x$, then there is a set $y \in x$ such that $x \cap y = \emptyset$

11. [[transitive closure|Transitive closure]]: every set is a subset of a smallest transitive set

12. [[Mostowski's principle]]: every well-founded extensional relation is isomorphic to a transitive set equipped with the relation $\in$. 

This implies that Mostowski set theory is equivalent in strength to [[ETCS]], a [[constructively well-pointed topos]] with [[natural numbers object]] and the [[axiom of choice]]. 

#### Variations of Mostowski set theory in intuitionistic logic

By removing axiom 9 from classical Mostowski set theory, one gets **[[intuitionistic logic|intuitionistic]] Mostowski set theory** or **[[constructive mathematics|constructive]] Mostowski set theory**, which is equivalent in strength to a [[constructively well-pointed topos]] with [[natural numbers object]] and the [[axiom of well-founded materialization]].

By removing axiom 7 from classical Mostowski set theory, one gets **[[predicative mathematics|predicative]] classical Mostowski set theory**, which is equivalent in strength to a [[constructively well-pointed]] [[Heyting pretopos]] with [[natural numbers object]] and the [[axiom of choice]]. 

By removing axiom 7 from intuitionistic Mostowski set theory, one gets **[[predicative mathematics|strongly predicative]] constructive Mostowski set theory**, which is equivalent in strength to a [[constructively well-pointed]] [[Heyting pretopos]] with a [[natural numbers object]] and the [[axiom of well-founded materialization]]. 

By replacing axiom 7 by the axiom of exponentiation (for all sets $a$ and $b$, the set $b^a$ of functions from $a$ to $b$ exists) in intuitionistic Mostowski set theory, one gets **[[predicative mathematics|weakly predicative]] constructive Mostowski set theory**, which is equivalent in strength to a [[constructively well-pointed]] [[ΠW-pretopos]] with the [[axiom of well-founded materialization]]. 

By removing axiom 8 from any $X$ Mostowski set theory, with $X$ being one of (classical, intuitionistic, predicative classical, weakly predicative constructive, strongly predicative constructive), one gets **[[finite mathematics|weakly finitist]] $X$ Mostowski set theory**, which is equivalent in strength to a [[constructively well-pointed]] $C$, where $C$ is one of ([[Boolean topos]] with the [[axiom of choice]], [[elementary topos]] with the [[axiom of well-founded materialization]], [[Boolean pretopos]] with the [[axiom of choice]], [[Π-pretopos]] with the [[axiom of well-founded materialization]], [[Heyting pretopos]] with the [[axiom of well-founded materialization]]). 

If one replaces axiom 8 in any of the above with the **[[axiom of finiteness]]** (for any formula $\phi$, if $\phi(\emptyset)$ and for all sets $x$, $\phi(x)$ implies that $\phi(x \cup \{x\})$, then for all sets $x$, $\phi(x)$), one gets **strongly finitist Mostowski set theory**, which is equivalent in strength to the category [[FinSet]]. Axioms 7 and 9 are redundant in this formulation, since both are implied by the axiom of finiteness. 

Thus, the most general variation of Mostowski set theory in intuitionistic logic is **weakly finitist, strongly predicative, constructive Mostowski set theory**, which consists of axioms 1-6 and 10-12, and is equivalent in strength to a general [[constructively well-pointed]] [[Heyting pretopos]] with the [[axiom of well-founded materialization]]. 

## See also

* [[material set theory]]
* [[ETCS]]

## References

* [[Michael Shulman]] (2018). Comparing material and structural set theories. [arXiv:1808.05204](https://arxiv.org/abs/1808.05204).