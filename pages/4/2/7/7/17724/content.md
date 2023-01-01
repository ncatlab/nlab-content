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

In type theory, **higher induction-reduction** is the principle that one could also have identity constructors and identity section constructors in addition to the element and section constructors. 

## Example 

A [[Tarski universe]] is an example of an inductive-recursive definition, where a type $U$ is defined inductively together with a [[type family]] $a:U \vdash T(a) \; \mathrm{type}$. The constructors for $U$ may depend negatively on $T$ applied to elements of $U$. This is the case if $U$, for example, is closed under [[dependent product types]], where it has constructors of 

* a [[dependent type]] $\Pi(a, b)$ for each $a:U$ and $b:T(a) \to U$, 
* a [[function]] $E_\Pi(a, b):\left(\prod_{x:T(a)} T(b)(x)\right) \to T(\Pi(a, b))$ for each $a:U$ and $b:T(a) \to U$. 

If the Tarski universe is strictly closed under dependent product types, then the last condition is replaced by 

* a [[judgmental equality]] $T(\Pi(a, b)) \equiv \prod_{x:T(a)} T(b)(x)$ for each $a:U$ and $b:T(a) \to U$. 

Here, the type family $T$ is defined recursively. Sometimes, however, one might
not want to give $T(u)$ completely as soon as $u:U$ is introduced, but instead
define $T$ inductively as well. This is the principle of [[induction-induction]].

##Related concepts

* [[inductive-inductive type]]

* [[algebraically compact category]]

## References 

* [[Peter Dybjer]], *A General Formulation of Simultaneous Inductive-Recursive Definitions in Type Theory*, The Journal of Symbolic Logic **65** 2 (2000) &lbrack;[pdf](http://www.cse.chalmers.se/~peterd/papers/Inductive_Recursive.pdf), [doi:10.2307/2586554](https://doi.org/10.2307/2586554)&rbrack;

* [[Peter Dybjer]] and [[Anton Setzer]], _A Finite Axiomatization of Inductive-Recursive Definitions_, [springer](https://link.springer.com/chapter/10.1007/3-540-48959-2_11)

* [papers by Peter Dybjer about induction and induction-recursion](http://www.cse.chalmers.se/~peterd/papers/inductive.html)

[[!redirects induction-recursion]]
