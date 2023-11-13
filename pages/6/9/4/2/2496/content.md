
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

Higher-order logic in general could be thought of as a [[first order theory]] with [[dependent types]]. There is a [[type]] $V$ called the [[domain of discourse]], and for each type $T$ and each term $t:T$, a [[power set|type of predicates on $T$]] $\mathcal{P}(T)$ whose terms $P(t):\mathcal{P}(T)(t)$ are propositions dependent on $t$. The system $(\mathcal{U}, V:\mathcal{U}, \mathcal{P}:\mathcal{U}\rightarrow\mathcal{U})$ consisting of the [[type universe]] $\mathcal{U}$, the domain of discourse $V$, and the power type functor $\mathcal{P}$ is a [[natural numbers object]]. 

## Related concepts

* [[logic]]

  * [[propositional logic]] (0th order)

  * [[predicate logic]] (1st order)

  * [[second-order logic]]

  * **higher order logic**

    * [[HOL]], [[Isabelle]]
    * Girard's System Fω (also called λω) and Coquand-Huet's [[calculus of constructions]] are the higher-order subsystems of [[pure type system#lambda_cube|Barendregt's lambda-cube]]

* [[higher-order abstract syntax]]

* [[dependent type theory]]

* [[tripos]]

## References

* [[Colin Rothgang]], [[Florian Rabe]], [[Christoph Benzmüller]], *Theorem Proving in Dependently-Typed Higher-Order Logic -- Extended Preprint*, The 29th International Conference on Automated Deduction (CADE-29), July 1-5, 2023. ([arXiv:2305.15382](https://arxiv.org/abs/2305.15382))

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
