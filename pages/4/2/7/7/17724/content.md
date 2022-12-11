[[!redirects inductive-recursive types]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##


In [[type theory]], _induction-recursion_ is a principle for mutually defining [[types]] of the form 

$$A \; \mathrm{type} \qquad a:A \vdash B(a) \; \mathrm{type}$$

where $A$ is defined as an [[inductive type]] and $B$ is defined by [[recursion]] on $A$. Crucially, the definition of $A$ may use $B$. Without this last requirement, we could first define $A$ and then separately $B$.

In type theory, **higher induction-reduction** is the principle that one could also have identity and identity section constructors in addition to the element and section constructors. 

## Example 

A [[Tarski universe]] is an example of an inductive-recursive definition,
where a type $U$ is defined inductively together with a dependent type $a:U \vdash T(a) \; \mathrm{type}$. The constructors for $U$ may depend negatively on $T$ applied to
elements of $U$, as is the case if $U$, for example, is strictly closed under dependent function types:

$$\frac{\Gamma \vdash a:U \quad \Gamma \vdash b : T(a) \; \mathrm{type}}{\Gamma \vdash \Pi(a, b) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash a:U \quad \Gamma \vdash b : T(a) \; \mathrm{type}}{\Gamma \vdash T(\Pi(a, b)) \equiv \prod_{x:T(a)} T(b(x)) \; \mathrm{type}}$$

If the Tarski universe is weakly closed under dependent function types, then the Tarski universe becomes a higher inductive-recursive type, since the rules for defining an equivalence of types involve generating identities of the [[identity type]]. 

$$\frac{\Gamma \vdash a:U \quad \Gamma \vdash b : T(a) \; \mathrm{type}}{\Gamma \vdash \Pi(a, b) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash a:U \quad \Gamma \vdash b : T(a) \; \mathrm{type}}{\Gamma \vdash E_\Pi:T(\Pi(a, b)) \simeq \prod_{x:T(a)} T(b(x))}$$

Here, the type family $T$ is defined recursively. Sometimes, however, one might
not want to give $T(u)$ completely as soon as $u:U$ is introduced, but instead
define $T$ inductively as well. This is the principle of [[induction-induction]].

##Related concepts

* [[inductive-inductive type]]

* [[algebraically compact category]]

## References 

* [[Peter Dybjer]] (2000), _A General Formulation of Simultaneous Inductive-Recursive Definitions in Type Theory_ ([pdf](http://www.cse.chalmers.se/~peterd/papers/Inductive_Recursive.pdf))

* [[Peter Dybjer]] and [[Anton Setzer]], _A Finite Axiomatization of Inductive-Recursive Definitions_, [springer](https://link.springer.com/chapter/10.1007/3-540-48959-2_11)

* [papers by Peter Dybjer about induction and induction-recursion](http://www.cse.chalmers.se/~peterd/papers/inductive.html)

[[!redirects induction-recursion]]
