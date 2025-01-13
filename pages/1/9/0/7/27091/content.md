
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[constructive mathematics]], [[equality]] and [[denial inequality]] of [[sets]] do not have all the properties that they do in [[classical mathematics]]. Hence, a *classical set* is a set in which equality and denial inequality do behave as they do in classical mathematics. 

"Classical sets" is a placeholder name for a concept which may or may not have another name in the mathematics literature. The idea however is that classical sets in constructive mathematics are those whose equality and denial inequality behave as they do in classical mathematics. 

## Definition

A **classical set** is a set $S$ with an [[apartness relation]] $\neq$ such that for all elements $x$ and $y$ in $S$, $x = y$ [[disjunction|or]] $x \neq y$. 

The disjunction $x = y \vee x \neq y$ implies the weaker [[multiplicative disjunction]] in the [[antithesis interpretation]] of [[constructive mathematics]]

$$(\neg(x = y) \Rightarrow x \neq y) \wedge (\neg(x \neq y) \Rightarrow x = y)$$

which precisely says that $\neq$ is [[denial inequality]] and a [[tight relation]]. 

Note that classical sets are not the same as sets with [[decidable equality]], since the [[negation]] of [[equality]] is not provably an [[apartness relation]] in [[constructive mathematics]]. 

In addition, classical sets form a [[coherent theory]], since the theory of [[apartness relations]] is coherent, and the axiom $x:S, y:S \vdash x = y \vee x \neq y$ is also coherent. 

## The category of classical sets

The category of classical sets is the category whose objects are classical sets and whose morphisms are functions. Since the apartness coincides with denial inequality in classical sets, every function between classical sets is a [[strongly extensional function]].  

In constructive mathematics, the category of classical sets is a [[Heyting category]]. In particular, 

* [[finite sets]] are classical sets

* The [[natural numbers]] are a classical set

* the [[disjoint union]] of two classical sets is itself a classical set

* the indexed disjoint union of a family of classical sets indexed by a classical set is a classical set

* The [[preimage]] of a function $f:A \to B$ between two classical sets $A$ and $B$ at an element $b$ of $B$ is a classical set. 

* the product of two classical sets is itself a classical set

* any [[subsingleton]] is a classical set, and in particular

  * the [[support of a set|support of any set]] is a classical set

  * given two subsingletons $A$ and $B$, the [[function set]] from $A$ to $B$ is a classical set

  * the [[cartesian product]] of any family of subsingletons is a classical set

* more generally, any [[subset]] of a classical set is a classical set, and in particular

  * [[subfinite sets]] are classical sets

  * [[subcountable sets]] are classical sets

  * the [[disjoint union]] of any family of subsingletons is a classical set

  * Given a classical set $A$ with a equivalence relation $\sim$, one can construct the [[quotient set]] $A / \sim$. If one can construct a [[section]] of the unique [[surjection]] which takes elements of $A$ to its equivalence class in $A / \sim$, then $A / \sim$ is a classical set. 

Further axioms can be assumed of the category of classical sets which are not [[neutral constructive mathematics|neutrally constructive]]: 

* That [[Cantor space]] is a classical set is equivalent to the [[limited principle of omniscience]]. 

* That the [[Dedekind real numbers]] are a classical set is equivalent to the [[analytic LPO]]. 

* That the [[set of truth values]] is a classical set is equivalent to [[excluded middle]]; thus this is usually not assumed to be a classical set in constructive mathematics. In fact, either [[decidable equality]] or a [[tight apartness relation]] on the set of truth values is sufficient to prove [[excluded middle]]. 

### Cartesian closure

One can also postulate that the category of classical sets is [[cartesian closed category|cartesian closed]] or equivalently [[locally cartesian closed category|locally cartesian closed]]. 

\begin{theorem}
There are two definable functions from every subsingleton $A$ to the [[boolean domain]] $\{0, 1\}$, the [[constant functions]] $\lambda x:A.0$ and $\lambda x:A.1$. Suppose that either there exists $x:A$ such that $(\lambda x:A.0)(x) \neq (\lambda x:A.1)(x)$, or for all $x:A$, $(\lambda x:A.0)(x) = (\lambda x:A.1)(x)$. Then $A$ is a [[decidable subsingleton]]. 
\end{theorem}

\begin{proof}
We prove by case analysis. 

Suppose that there exists $x:A$ such that $(\lambda x:A.0)(x) \neq (\lambda x:A.1)(x)$. Then $A$ is a [[inhabited set|inhabited]] subsingleton and thus a decidable subsingleton. 

Then suppose that for all $x:A$, $(\lambda x:A.0)(x) = (\lambda x:A.1)(x)$. Then $A$ is [[empty set|empty]] and thus a decidable subsingleton, and the function set $\{0, 1\}^A$ is a [[singleton]] by the [[universal property]] of the empty set, with all functions equal to each other. 

This exhausts all options for decidable subsingletons, and exhausts all possible conditions in the hypothesis. 
\end{proof}

\begin{theorem}
Suppose that classical sets are [[cartesian closed]]; i.e. suppose that for sets $A$ and $B$ with [[decidable tight apartness relations]], the [[tight apartness relation]] on the function set $B^A$, defined by $f \# g \coloneqq \exists x:A.f(x) \neq g(x)$, is decidable. Then [[excluded middle]] holds. 
\end{theorem}

\begin{proof}
Every [[subsingleton]] $A$ has a [[decidable tight apartness relation]] where $x \# y$ is always [[false]]. The [[boolean domain]] $\{0, 1\}$ also has a decidable tight apartness relation where $x \# y$ is given by the [[denial inequality]] $x \neq y$. That the tight apartness relation on the function set $\{0, 1\}^A$ is decidable implies the previous theorem above, which implies that every subsingleton $A$ is a decidable subsingleton, which is precisely the condition of [[excluded middle]]. 
\end{proof}

\begin{theorem}
Suppose that classical sets are [[locally cartesian closed]]; i.e. suppose that for set $A$ with a [[decidable tight apartness relation]], and [[family of sets]] $B(x)$ indexed by elements $x \in A$ where each $B(x)$ comes with a [[decidable tight apartness relation]], the [[tight apartness relation]] on the indexed [[Cartesian product]] $\prod_{x \in A} B(x)$, defined by $f \# g \coloneqq \exists x:A.f(x) \neq g(x)$, is decidable. Then [[excluded middle]] holds. 
\end{theorem}

\begin{proof}
Let $A$ be a singleton and let $B(x) = \{0, 1\}$ be the [[constant function|constant]] [[family of sets]] that is always defined to be the [[boolean domain]]. Then the indexed [[Cartesian product]] $\prod_{x \in A} B(x)$ is in [[bijection]] with the function set $\{0, 1\}^A$, and by the previous theorem, [[excluded middle]] holds. 
\end{proof}

In essence, if we take [[classical mathematics]] to be mathematics where only the classical sets are relevant, then [[constructive mathematics]] are a form of [[predicative mathematics]] in the classical sense, where not all classical [[function sets]] exist, since general function sets are not classical sets. 

\begin{theorem}
Suppose that every [[inequality space]] is a [[classical set]]. Then [[excluded middle]] holds. 
\end{theorem}

\begin{theorem}
In the presence of [[quotient sets]], suppose that every [[apartness relation]] on a [[set]] is [[decidable relation|decidable]]:

$$((\forall x.\neg R(x, x)) \wedge (\forall x, y.R(x, y) \Rightarrow R(y, x)) \wedge (\forall x, y, z.R(x, y) \wedge R(y, z) \Rightarrow R(x, z))) \Rightarrow (\forall x, y.R(x, y) \vee \neg R(x, y))$$

Then [[excluded middle]] holds. 
\end{theorem}

## Applications
 {#Applications}

Working with decidable subsets of classical sets makes [[constructive mathematics]] very much like [[classical mathematics]]. This is why constructivism has few consequences for basic [[combinatorics]] and [[algebra]] (although it does have important consequences for more advanced topics in those fields). In [[analysis]], in contrast, [[constructivism]] matters right away, because constructively the set of [[real numbers]] may not be a classical set. 

## Related concepts

* [[set]]

* [[tight apartness relation]]

* [[discrete field]]

* [[coherent logic]], [[coherent mathematics]]

[[!redirects classical sets]]

[[!redirects decidable tight apartness]]

[[!redirects decidable tight apartness relation]]
[[!redirects decidable tight apartness relations]]

[[!redirects decidable connected apartness]]

[[!redirects decidable connected apartness relation]]
[[!redirects decidable connected apartness relations]]

[[!redirects decidable inequality]]
[[!redirects decidable inequalities]]
[[!redirects decidable inequality structure]]
[[!redirects decidable inequality structures]]
[[!redirects decidable inequality relation]]
[[!redirects decidable inequality relations]]
[[!redirects decidable inequality space]]
[[!redirects decidable inequality spaces]]

[[!redirects category of classical sets]]
[[!redirects categories of classical sets]]

[[!redirects category of decidable inequality spaces]]
[[!redirects categories of decidable inequality spaces]]