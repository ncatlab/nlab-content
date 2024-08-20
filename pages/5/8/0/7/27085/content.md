
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]] defined via [[universes]] and universe levels, **local propositional resizing** is a weak version of the [[propositional resizing axiom]] which says that given a universe level $i$, the [[type of propositions]] $\mathrm{Prop}_i$ of each universe $U_i$ is $U_i$-small. The dependent type theory is then said to be **locally impredicative** or to have **local impredicativity**. 

Unlike the usual propositional resizing axiom, the local propositional resizing axiom makes no assumption on the equivalence of the types of propositions for different universe levels. It is possible to assume local propositional resizing, [[excluded middle]] for one universe $U_i$, and [[Brouwer's continuity principle]] for [[Dedekind real numbers]] for another universe $U_j$ where $j \gt i$, thus making $\mathrm{Prop}_i$ and $\mathrm{Prop}_j$ provably [[equivalence of types|inequivalent types]] and contradicting the [[propositional resizing axiom]]. 

Thus, while each universe $U_i$ itself is impredicative in the sense of having a type of all $U_i$-small propositions, the dependent type theory itself is still predicative since there is no type of *all* propositions in the type theory. However, local propositional resizing suffices for [[impredicative mathematics]] in most cases, since one is usually working inside of a universe $U_i$ and only the $U_i$-small propositions are relevant. 

The name *local propositional resizing* and *[[global propositional resizing]]*, along with *locally impredicative* and *[[globally impredicative]]* is in analogue with [[locally univalent bicategory|local univalence]] and [[globally univalent bicategory|global univalence]] for [[univalent bicategories]]: while all univalent bicategories are locally univalent, not all locally univalent bicategories are univalent bicategories. Similarly, while all impredicative dependent type theories are locally impredicative, not all locally impredicative dependent type theories are impredicative. 

## Definition

We assume an infinite hierarchy of [[Russell universes]] or [[Coquand universes]] indexed by [[natural numbers]] in the metatheory or defined separately in some other [[sort]]. 

The axiom of **weak local propositional resizing** says that the type of propositions $\sum_{A:U_i} \mathrm{isProp}(A)$ is [[essentially small type|essentially $U_i$-small]] 

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash \mathrm{propresize}_i:\sum_{\Omega_i:U_i} \Omega_i \simeq \sum_{A:U} \mathrm{isProp}(A)}$$

The dependent type theory is **weakly locally impredicative** or said to have **weak local impredicativity**. 

The axiom of **strict local propositional resizing** says that the type of propositions $\sum_{A:U_i} \mathrm{isProp}(A)$ is $U_i$-small:

$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash \Omega_i:U_i} \qquad \frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash \Omega_i \equiv \sum_{A:U_i} \mathrm{isProp}(A)}$$

The dependent type theory is **strictly locally impredicative** or said to have **strict local impredicativity**. 

In the case for [[Coquand universes]], local propositional resizing is equivalent to saying that for each universe level $i$ one can construct a [[type of all propositions]] for the type [[judgment]] $\mathrm{type}_i$: 

$$\frac{\Gamma \vdash i \mathrm{level}}{\Gamma \vdash \Omega_i \; \mathrm{type}_i}$$

$$\frac{\Gamma \vdash i \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i}{\Gamma \vdash \mathrm{toProp}_{i, A}:\mathrm{isProp}(A) \to \Omega_i}$$

$$\frac{\Gamma \vdash i \mathrm{level} \quad \Gamma \vdash A:\Omega_i}{\Gamma \vdash \mathrm{El}_i(A) \; \mathrm{type}_i} \qquad \frac{\Gamma \vdash i \mathrm{level} \quad \Gamma \vdash A:\Omega_i}{\Gamma \vdash \mathrm{proptrunc}_i(A):\mathrm{isProp}(\mathrm{El}_i(A))}$$

$$\frac{\Gamma \vdash i \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i \quad \Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \mathrm{El}_i(\mathrm{toProp}_{i, A}(p)) \equiv A \; \mathrm{type}_i}$$

$$\frac{\Gamma \vdash i \mathrm{level} \quad \Gamma \vdash A \; \mathrm{type}_i \quad \Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \mathrm{proptrunc}_i(\mathrm{toProp}_{i, A}(p)) \equiv p:\mathrm{isProp}(A)}$$

$$\frac{\Gamma \vdash i \mathrm{level} \quad \Gamma \vdash A:\Omega_i}{\Gamma \vdash A \equiv \mathrm{toProp}_{i, \mathrm{El}_i(A)}(\mathrm{proptrunc}_i(A)):\Omega_i}$$

## For general universe hierarchies

More generally, one can speak of local propositional resizing of [[universe hierarchies]] as actual structure in a [[dependent type theory]]. 

Let $(P, U, T, t)$ be a [[hierarchy of weakly Tarski universes]]. By definition, $P$ is a [[preorder]] and there is a function
$$t:\prod_{a:P} \prod_{b:P} (a \leq b) \to (U(a) \hookrightarrow U(b))$$
which states that for all terms $a:P$ and $b:P$ $a \leq b$ implies the type of embeddings $U(a) \hookrightarrow U(b)$ is pointed. We thus have a natural map
$$t_\Omega:\prod_{a:P} \prod_{b:P} (a \leq b) \to \left(\sum_{A:U(a)} \mathrm{isProp}(T(a)(A)) \hookrightarrow \sum_{A:U(b)} \mathrm{isProp}(T(b)(A))\right)$$
which is the restriction of the above function to small propositions of the universe. 

The axiom of **[[local propositional resizing]]** states that for all terms $a:P$ there is a $U(a)$-small type $\mathrm{Prop}_{U(a)}$ which is equivalent to the type of all $U(a)$-small propositions. 

$$\mathrm{localpropresize}:\prod_{a:P} \sum_{\Omega_U:U(a)} T(\Omega_U) \simeq \sum_{A:U(a)} \mathrm{isProp}(T(A))$$

The universe hierarchy is then said to be **locally impredicative**. However, it may still be the case that the type of propositions for two universe are not equivalent to each other, meaning that the universe hierarchy itself is not impredicative. 

Usually, the hierarchy of Tarski universes is a sequential hierarchy indexed by the [[natural numbers]] $\mathrm{N}$. 

## Related concepts

* [[propositional resizing]], [[global propositional resizing]]

* [[type of propositions]]

[[!redirects local propositional resizing]]
[[!redirects weak local propositional resizing]]
[[!redirects strict local propositional resizing]]

[[!redirects locally impredicative]]
[[!redirects local impredicativity]]

[[!redirects weak locally impredicative]]
[[!redirects weak local impredicativity]]

[[!redirects strict locally impredicative]]
[[!redirects strict local impredicativity]]

[[!redirects locally impredicative universe hierarchy]]
[[!redirects locally impredicative universe hierarchies]]
[[!redirects locally impredicative hierarchy of universes]]
[[!redirects locally impredicative hierarchies of universes]]
[[!redirects locally impredicative hierarchy of Tarski universes]]
[[!redirects locally impredicative hierarchies of Tarski universes]]

[[!redirects weakly locally impredicative universe hierarchy]]
[[!redirects weakly locally impredicative universe hierarchies]]
[[!redirects weakly locally impredicative hierarchy of universes]]
[[!redirects weakly locally impredicative hierarchies of universes]]
[[!redirects weakly locally impredicative hierarchy of Tarski universes]]
[[!redirects weakly locally impredicative hierarchies of Tarski universes]]

[[!redirects strictly locally impredicative universe hierarchy]]
[[!redirects strictly locally impredicative universe hierarchies]]
[[!redirects strictly locally impredicative hierarchy of universes]]
[[!redirects strictly locally impredicative hierarchies of universes]]
[[!redirects strictly locally impredicative hierarchy of Tarski universes]]
[[!redirects strictly locally impredicative hierarchies of Tarski universes]]

[[!redirects axiom of local propositional resizing]]
[[!redirects axiom schema of local propositional resizing]]

[[!redirects local propositional resizing axiom]]
[[!redirects local propositional resizing axiom schema]]

[[!redirects axiom of weak local propositional resizing]]
[[!redirects axiom schema of weak local propositional resizing]]

[[!redirects weak local propositional resizing axiom]]
[[!redirects weak local propositional resizing axiom schema]]

[[!redirects axiom of strict local propositional resizing]]
[[!redirects axiom schema of strict local propositional resizing]]

[[!redirects strict local propositional resizing axiom]]
[[!redirects strict local propositional resizing axiom schema]]