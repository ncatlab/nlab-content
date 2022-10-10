
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

#Contents#
* table of contents
{:toc}

## Idea

In [[homotopy type theory]], the type of [[h-propositions]] of a [[Tarski universe]] (or [[Russell universe]]) $U$ is not in general $U$-small. Propositional resizing is then the statement that the type of h-propositions is $U$-small. 

There is a separate axiom of propositional resizing for a hierarchy of universes, where the type of h-propositions of each universe, where one universe embeds into the other universe, are equivalent to each other. 

Propositional resizing is a form of [[impredicativity]] for h-propositions, and by avoiding its use, the universe or hierarchy is said to remain predicative.

However, when using Tarski universes, while universes and universe hierarchies may be impredicative, the overarching type theory is still predicative if it has a judgment '$A \; \mathrm{type}$', since it is impossible to talk about all types. 

## Definition

### For individual universes

Let $(U, T)$ be a [[weakly Tarski universe]] and let
$$\sum_{A:U} \mathrm{isProp}(T(A))$$ 
be the type of all propositions in $U$. The weakly Tarski universe $(U, T)$ is **impredicative** or satisfies **propositional resizing** if it has a term $\Omega_U:U$ and an equivalence 
$$\mathrm{propresize}:T(\Omega_U) \simeq \sum_{A:U} \mathrm{isProp}(T(A))$$

A weakly Tarski universe is **strictly impredicative** or satisfies **strict propositional resizing** if the above equivalence becomes a [[definitional equality]]:

$$T(\Omega_U) \equiv \sum_{A:U} \mathrm{isProp}(T(A))$$

In particular, every impredicative [[strictly Tarski universe]] is strictly impredicative. 

### For a universe hierarchy

Let $(P, U, T. t)$ be a hierarchy of weakly Tarski universes. By definition, $P$ is a [[preorder]] and there is a function
$$t:\prod_{a:P} \prod_{b:P} (a \leq b) \to (U(a) \hookrightarrow U(b))$$
which states that for all terms $a:P$ and $b:P$ $a \leq b$ implies the type of embeddings $U(a) \hookrightarrow U(b)$ is pointed. We thus have a natural map
$$t_\Omega:\prod_{a:P} \prod_{b:P} (a \leq b) \to \left(\sum_{A:U(a)} \mathrm{isProp}(T(a)(A)) \hookrightarrow \sum_{A:U(b)} \mathrm{isProp}(T(b)(A))\right)$$
which is the restriction of the above function to small propositions of the universe. 

The axiom of **proposition resizing** states that for all terms $a:P$, $b:P$, and $q:a \leq b$ the embedding $t_\Omega(a, b)(q)$ is an [[equivalence of types]] 
$$\mathrm{propresize}:\prod_{a:P} \prod_{b:P} \prod_{q:a \leq b} \mathrm{isEquiv}(t_\Omega(a, b)(q))$$
The type of all h-propositions in the larger universe $U(a)$ may be *resized* to be equivalent to the type of all h-proposition in the smaller universe $U(b)$. The universe hierarchy is then said to be **impredicative**. 

Usually, the hierarchy of Tarski universes is a sequential hierarchy indexed by the [[natural numbers]] $\mathrm{N}$. 

## See also

* [[essentially small type]]

## References

* Section 3.5 of [[The HoTT Book]]

[[!redirects propositional resizing]]
[[!redirects weak propositional resizing]]
[[!redirects strict propositional resizing]]

[[!redirects impredicative universe]]
[[!redirects impredicative universes]]
[[!redirects impredicative Tarski universe]]
[[!redirects impredicative Tarski universes]]

[[!redirects weakly impredicative universe]]
[[!redirects weakly impredicative universes]]
[[!redirects weakly impredicative Tarski universe]]
[[!redirects weakly impredicative Tarski universes]]

[[!redirects strictly impredicative universe]]
[[!redirects strictly impredicative universes]]
[[!redirects strictly impredicative Tarski universe]]
[[!redirects strictly impredicative Tarski universes]]

[[!redirects axiom of propositional resizing]]