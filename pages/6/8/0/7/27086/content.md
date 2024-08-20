
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

In [[dependent type theory]] defined via [[universes]] and universe levels, **global propositional resizing** is a weak version of the [[propositional resizing axiom]] which says that given two universe levels $i$ and $j$, the [[type of propositions]] $\mathrm{Prop}_i$ and $\mathrm{Prop}_j$ of universes $U_i$ and $U_j$ are [[equivalence of types|equivalent types]]. This implies that there is a [[type of all propositions]] $\Omega$ in some universe level which is [[equivalence of types|equivalent]] to all $\mathrm{Prop}_i$. The dependent type theory is then said to be **globally impredicative** or have **global impredicativity**. 

Unlike the usual propositional resizing axiom, the global propositional resizing axiom makes no assumption on whether all universes contain $\Omega$. If there is a base level $0$ where $0 \leq i$ for all universe levels $i$, then it is possible to assume global propositional resizing, that every $U_0$-small type has a [[tight apartness relation]], and [[Brouwer's continuity principle]] for the [[Dedekind real numbers]], contradicting the [[propositional resizing axiom]]. 

Thus, while the dependent type theory itself is impredicative since there is a type of *all* propositions $\Omega$ in the type theory, there might be universes $U_i$ which are predicative in the sense of *not* having the type of all propositions $\Omega$. However, it suffices for [[impredicative mathematics]] to find a universe $U_i$ which does contain the type of all propositions $\Omega$. 

The names *global propositional resizing* and *[[local propositional resizing]]*, along with *globally impredicative* and *[[locally impredicative]]* is in analogue with [[globally univalent bicategory|global univalence]] and [[locally univalent bicategory|local univalence]] for [[univalent bicategories]]: while all univalent bicategories are globally univalent, not all globally univalent bicategories are univalent bicategories. Similarly, while all impredicative dependent type theories are globally impredicative, not all globally impredicative dependent type theories are impredicative. 

## Definition

### Using Russell universes

We assume  an infinite hierarchy of [[Russell universes]] indexed by [[natural numbers]] in the metatheory or defined separately in some other [[sort]]. The Russell universes are non-cumulative in the sense that there is a lifting operation which takes types $A:U_i$ to $\mathrm{Lift}_i(A):U_{i + 1}$ for all universe levels $i$. The function $\lambda A:U_i.\mathrm{Lift}_i(A):U_i \to U_{i + 1}$ in $U_{i + 2}$ restricts to a function
$$\mathrm{LiftProp}_i:\left(\sum_{A:U_i} \mathrm{isProp}(A) \to \sum_{A:U_{i+1}} \mathrm{isProp}(\mathrm{Lift}_i(A))\right)$$
in $U_{i + 2}$ between the types of small propositions of the universes. 

The axiom of **global proposition resizing** states that for all universe levels $i$ the function $\mathrm{LiftProp}_i$ is an [[equivalence of types]] 
$$\frac{\Gamma \vdash i \; \mathrm{level}}{\Gamma \vdash \mathrm{globalpropresize}_i:\mathrm{isEquiv}(\mathrm{LiftProp}_i)}$$
The type of all propositions in the successor universe $U_{i+1}$ may be *resized* to be equivalent to the type of all propositions in the smaller universe $U_i$. By the properties of equivalences one can show that the types of propositions of any two universes $U_i$ and $U_j$ are equivalent for any universe levels $i$ and $j$, and that any such type of propositions is [[essentially small type|essentially $U_1$-small]]. 

The dependent type theory is then said to be **globally impredicative**. However, in the absence of [[local propositional resizing]], the base universe $U_0$ does not have an internal [[type of propositions]]. 

### Using Coquand universes

...

## For general universe hierarchies

More generally, one can speak of global propositional resizing for [[universe hierarchies]] as actual structure in a [[dependent type theory]]. 

Let $(P, U, T, t)$ be a [[hierarchy of weakly Tarski universes]]. By definition, $P$ is a [[preorder]] and there is a function
$$t:\prod_{a:P} \prod_{b:P} (a \leq b) \to (U(a) \hookrightarrow U(b))$$
which states that for all terms $a:P$ and $b:P$ $a \leq b$ implies the type of embeddings $U(a) \hookrightarrow U(b)$ is pointed. We thus have a natural map
$$t_\Omega:\prod_{a:P} \prod_{b:P} (a \leq b) \to \left(\sum_{A:U(a)} \mathrm{isProp}(T(a)(A)) \hookrightarrow \sum_{A:U(b)} \mathrm{isProp}(T(b)(A))\right)$$
which is the restriction of the above function to small propositions of the universe. 

The axiom of **global proposition resizing** for the universe hierarchy states that for all terms $a:P$, $b:P$, and $q:a \leq b$ the embedding $t_\Omega(a, b)(q)$ is an [[equivalence of types]] 
$$\mathrm{globalpropresize}:\prod_{a:P} \prod_{b:P} \prod_{q:a \leq b} \mathrm{isEquiv}(t_\Omega(a, b)(q))$$
The type of all h-propositions in the larger universe $U(a)$ may be *resized* to be equivalent to the type of all h-proposition in the smaller universe $U(b)$. 

The universe hierarchy is then said to be **globally impredicative**. However, it may still be the case that there are universes which do not have an internal [[type of propositions]], such as, in the absence of [[local propositional resizing]], any universe $U(a)$ indexed by a term $a:P$ such that there is no element $b:P$ where $b \leq a$ holds. 

Usually, the hierarchy of Tarski universes is a sequential hierarchy indexed by the [[natural numbers]] $\mathrm{N}$. 

## Related concepts

* [[propositional resizing]], [[local propositional resizing]]

* [[equivalence of types]]

[[!redirects global propositional resizing]]
[[!redirects weak global propositional resizing]]
[[!redirects strict global propositional resizing]]

[[!redirects globally impredicative]]
[[!redirects global impredicativity]]

[[!redirects globally impredicative universe hierarchy]]
[[!redirects globally impredicative universe hierarchies]]
[[!redirects globally impredicative hierarchy of universes]]
[[!redirects globally impredicative hierarchies of universes]]
[[!redirects globally impredicative hierarchy of Tarski universes]]
[[!redirects globally impredicative hierarchies of Tarski universes]]

[[!redirects weakly globally impredicative universe hierarchy]]
[[!redirects weakly globally impredicative universe hierarchies]]
[[!redirects weakly globally impredicative hierarchy of universes]]
[[!redirects weakly globally impredicative hierarchies of universes]]
[[!redirects weakly globally impredicative hierarchy of Tarski universes]]
[[!redirects weakly globally impredicative hierarchies of Tarski universes]]

[[!redirects strictly globally impredicative universe hierarchy]]
[[!redirects strictly globally impredicative universe hierarchies]]
[[!redirects strictly globally impredicative hierarchy of universes]]
[[!redirects strictly globally impredicative hierarchies of universes]]
[[!redirects strictly globally impredicative hierarchy of Tarski universes]]
[[!redirects strictly globally impredicative hierarchies of Tarski universes]]

[[!redirects axiom of global propositional resizing]]
[[!redirects axiom schema of global propositional resizing]]