
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _higher-order logic_ is any [[logic]] which features _higher-order predicates_, which are [[predicates]] of predicates or of operations.  If we think of a predicate as a [[function]] to [[truth values]], then a higher-order predicate is a function on a [[power set]] or a [[function set]].

[[type theory|Typed]] higher-order logic may be called higher-order type theory.  Typed higher-order [[intuitionistic logic]] is often identified with the [[internal logic]] of a [[topos]].

Higher-order logic in general could be thought of as a [[first order theory]] with [[dependent types]]. There is a [[type]] $V$ called the [[domain of discourse]], and for each type $T$ and each term $t:T$, a dependent type $\mathcal{P}(t)$ whose terms $P(t):\mathcal{P}(t)$ are higher-order predicates depending on $t$. The system $(\mathcal{U}, V:\mathcal{U}, \mathcal{P}:\mathcal{U}\rightarrow\mathcal{U})$ consisting of the [[type universe]] $\mathcal{U}$, the domain of discourse $V$, and the power type functor $\mathcal{P}$ is a [[natural numbers object]]. 

## Related concepts

* [[logic]]

  * [[propositional logic]] (0th order)

  * [[predicate logic]] (1st order)

  * [[second-order logic]]

  * **higher order logic**

    * [[HOL]], [[Isabelle]]

* [[higher-order set theory]]

* [[dependent type theory]]

* [[tripos]]


[[!redirects Higher-order logic]]
[[!redirects higher order logic]]

[[!redirects higher-order type theory]]
[[!redirects higher order type theory]]

[[!redirects higher-order proposition]]
[[!redirects higher-order propositions]]
[[!redirects higher order proposition]]
[[!redirects higher order propositions]]
[[!redirects higher-order predicate]]
[[!redirects higher-order predicate]]
[[!redirects higher order predicate]]
[[!redirects higher order predicate]]
