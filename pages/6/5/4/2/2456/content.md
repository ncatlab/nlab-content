
# Choice operators
* table of contents
{: toc}

## Definitions

A **(global) choice operator** is structure included in some [[foundations]] of [[mathematics]] which provides a uniform way to choose an element of every [[inhabited set|inhabited]] [[set]] or [[class]].

In [[David Hilbert|Hilbert]]'s original formulation, for any property $P(x)$ we can form a term $\varepsilon x.P(x)$ such that
$$\exists x.P(x) \;\Rightarrow\; P\big(\varepsilon x.P(x)\big).$$
In other words, if $P$ holds of anything at all, then it holds of the particular term $\varepsilon x.P(x)$.  A similar operator was used by [[Bourbaki]] and appears in [[FMathL]].

### In dependent type theory

In dependent type theory with [[propositional truncations]], the naive translation of the global choice operator results in the following rule:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:\vert A \vert \vdash \varepsilon_A(x):A}$$

The type-theoretic global choice operator implies global [[axiom K]] or global [[UIP]], and thus is inconsistent with the existence of a univalent Tarski universe with [[h-proposition|non-propositional]] [[h-sets]]. 

If one wants to express the set-theoretic global choice operator and still consistently have a univalent Tarski universe with [[h-proposition|non-propositional]] [[h-sets]], one needs to set-truncate the target, or restrict the global choice operator to inhabited [[h-sets]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:\vert A \vert \vdash \varepsilon_A(x):\vert A \vert_0} \quad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:\mathrm{isSet}(A)}{\Gamma, x:\vert A \vert \vdash \varepsilon_A(x):A}$$

There is also a version of the type-theoretic choice operator local to a [[Tarski universe]] $(U, T)$, given by:

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, X:U \vdash T \; \mathrm{type}}{\Gamma, A:U, x:\vert T(A) \vert \vdash \varepsilon_U(A, x):T(A)}$$

$U$ having a choice operator implies that $U$ satisfies [[axiom K]] or [[UIP]]. If $U$ is also univalent, then it is an [[h-groupoid]]. 

## Foundational status

It should be noted that Hilbert and Bourbaki take the $\varepsilon$-operator, called $\tau$ in "Theory of Sets" to be a primitive symbol in a mathematical theory.  This has the advantage of also allowing the existential and universal [[quantifiers]] to be constructed explicitly, since $\exists x$ translates to $P(\varepsilon_x(P(x)))$.  The intuitive meaning behind the operator is that it returns a distinguished object for which the proposition is true, or if no such object exists, it returns any object for which it is not true.  Of course, the intuitive meaning can be misleading since the properties of the epsilon operator are governed by the axiom schema of existence and $\varepsilon$-extensionality, without which, the symbol has no meaning.  The __axiom scheme of existence__ is a statement of Hilbert's axiom that avoids mention of the existential quantifier.

A wonderful usage of the global choice operator in Bourbaki is that we can easily show that paradoxical sets  do not exist, since the definition of a set is given in terms of whether or not the relation defining the set is collectivizing.  The example of [[Russell's paradox]] is computed in (Theory of Sets, Chapter II, &#167;1, no.4).  A consequence of this formulation is that the epsilon calculus is quantifier-free, since $\varepsilon$ subsumes their roles from the predicate calculus.  If we adjoin $\varepsilon$ to intuitionistic logic with the axiom scheme of existence, we obtain a non-conservative extension of intuitionistic logic in which the law of excluded middle still does not hold.  However, the assumption of the axiom scheme of $\varepsilon$-extensionality implies the axiom of global choice and therefore the law of excluded middle.  

One use of the choice operator is to eliminate undesirable details of implementation.  For example, if $P(x)$ is "$x$ is a Dedekind-complete totally ordered field," then we can define "the real numbers" to be $\varepsilon x.P(x)$.  Any of the numerous constructions of the [[real numbers]] can then be used to show that there exists an $x$ such that $P(x)$, after which point we can discard whichever explicit construction and work only with $\mathbb{R}=\varepsilon x.P(x)$.  This way we can no longer assert that real numbers (elements of $\mathbb{R}$) *are* Dedekind cuts, or equivalence classes of Cauchy sequences, or anything in particular, since the axioms provide no rules about how $\varepsilon x.P(x)$ must be chosen other than that it must satisfy $P$.  So $\mathbb{R}$ *might* consist of Cauchy sequences, or Dedekind cuts, or any other way to construct the reals, but we have no way of knowing, and thus we cannot make use of any such definition in a proof about $\mathbb{R}$; we are forced to use only its formal properties. (For a type-theoretic treatment of this situation, see [generalized the](generalized+the#formalization)).

In many cases, the assumption of a global choice operator implies the [[axiom of choice]], since for any family $(A_u)$ of inhabited sets, a choice function is given by $u\mapsto (\varepsilon x.x\in A_u)$.  In fact, in the form given above it often implies the stronger *global* axiom of choice, which applies to proper classes as well as sets.

> "Here, moreover, we come upon a very remarkable circumstance, namely, that all of these transfinite axioms are derivable from a single axiom, one that also contains the core of one of the most attacked axioms in the literature of mathematics, namely, the axiom of choice: $A(a) \rightarrow A(\varepsilon(A))$, where $\varepsilon$ is the transfinite logical choice function."

> ---Hilbert (1925), "On the Infinite", excerpted in Jean van Heijenoort, _From Frege to G&#246;del_, p. 382.

However, in some [[foundations]] it seems to be possible to avoid this conclusion (if it is unwanted) by not requiring the choice operator to be extensional, i.e. it may not be the case that $A = B$ implies $\varepsilon x.A = \varepsilon x.B$.

Like the [[axiom of choice]], the existence of a global choice operator is consistent with the other axioms of most foundations.  For example, in ZF, the [[constructible universe]] (which models $ZF + (V=L)$, the [[axiom of constructibility]]) admits a natural classical [[well-ordering]] of the entire universe, giving rise to a naturally defined global choice operator (namely, $\varepsilon x.P$ = the smallest $x$ such that $P$ in the global well-ordering).

On the other hand, a type-theoretic global choice operator is inconsistent with the [[univalence axiom]] of [[homotopy type theory]]. For univalence requires that all operations on the [[type of types]] must be natural with respect to equivalences, which no global choice operator can be.

## See also

* [[split support]]

## Readings

* [Hilbert's $\varepsilon$-Operator](https://planetmath.org/hilbertsvarepsilonoperator), _PlanetMath_.

* Stanford Encyclopedia of Philosophy article on [The Epsilon Calculus](http://plato.stanford.edu/entries/epsilon-calculus/).

* See also Hilbert (1927), "The Foundations of Mathematics", pp. 464&#8211;479 in JvH.


category: foundational axiom

[[!redirects choice operator]]
[[!redirects choice operators]]
[[!redirects global choice operator]]
[[!redirects global choice operators]]

[[!redirects type-theoretic choice operator]]
[[!redirects type-theoretic choice operators]]
[[!redirects type-theoretic global choice operator]]
[[!redirects type-theoretic global choice operators]]

[[!redirects set-theoretic choice operator]]
[[!redirects set-theoretic choice operators]]
[[!redirects set-theoretic global choice operator]]
[[!redirects set-theoretic global choice operators]]

[[!redirects axiom of existence]]
[[!redirects axiom scheme of existence]]
[[!redirects axiom schema of existence]]
[[!redirects axiom schemas of existence]]
[[!redirects axiom schemata of existence]]
