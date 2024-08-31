
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

A **classical set** is 

* a set $S$ with a [[decidable relation|decidable]] [[tight apartness relation]]

* a set $S$ with [[decidable equality]] whose [[denial inequality]] is an [[apartness relation]]. 

The two conditions are equivalent: 

* Decidable equality implies [[stable equality]], which implies that if [[denial inequality]] is an [[apartness relation]], it is a tight apartness relation, meaning that the tight apartness relation is decidable. 

* Conversely, every decidable tight apartness relation implies that the tight apartness relation is a [[stable relation]] and thus equivalent to [[denial inequality]]; hence denial inequality is decidable and an apartness relation and equality is also decidable. 

Note that classical sets are not the same as sets with [[decidable equality]], there are possibly sets with decidable equality and with a [[tight apartness relation]] which cannot be proved decidable, such as the [[real numbers]] with [[analytic WLPO]] but no [[analytic LPO]]. 

## The category of classical sets

The category of classical sets is the category whose objects are classical sets and whose morphisms are functions. Since tight apartness coincides with denial inequality in classical sets, every function between classical sets is a [[strongly extensional function]].  

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

* That the category of classical sets is [[cartesian closed category|cartesian closed]] or equivalently [[locally cartesian closed category|locally cartesian closed]], which implies the [[limited principle of omniscience]]. This is provable in the cohesive mode in [[cohesive homotopy type theory]] from crisp [[excluded middle]] and [[punctual cohesion]]. 

* That every [[inequality space]] is a [[classical set]], which implies [[analytic LPO]]. In the presence of [[quotient sets]], this is equivalent in strength to the statement that every [[apartness relation]] on a [[set]] is [[decidable relation|decidable]]:

$$((\forall x.\neg R(x, x)) \wedge (\forall x, y.R(x, y) \Rightarrow R(y, x)) \wedge (\forall x, y, z.R(x, y) \wedge R(y, z) \Rightarrow R(x, z))) \Rightarrow (\forall x, y.R(x, y) \vee \neg R(x, y))$$

* That the [[set of truth values]] is a classical set is equivalent to [[excluded middle]]; thus this is usually not assumed to be a classical set in constructive mathematics. In fact, either [[decidable equality]] or a [[tight apartness relation]] on the set of truth values is sufficient to prove [[excluded middle]]. 

The category of classical sets being cartesian closed implies that the [[boolean domain]] is the [[initial object|initial]] [[Boolean algebra]] with all [[joins]] and [[meets]] indexed by classical sets. If every set is a classical set, this implies that the [[boolean domain]] is a [[complete Boolean algebra]]. 

If classical sets are [[cartesian closed]], there is a cartesian closed [[subcategory]] of the category of classical sets, which is the [[initial object|initial]] cartesian closed category with pullbacks and closed under [[finite sets]] and the [[natural numbers]]. This cartesian closed subcategory is a [[Boolean topos]] since if classical sets are [[cartesian closed]], the only subsingletons that can be generated by finite sets and natural numbers in a cartesian closed category with pullbacks are the [[decidable subset|decidable subsingletons]]. This means that cartesian closure of classical sets is sufficient to replicate the entirety of (neutral, impredicative) [[classical mathematics]] in constructive mathematics, so long as one only works inside the Boolean subtopos. 

## Applications
 {#Applications}

Working with decidable subsets of sets with a decidable tight apartness makes [[constructive mathematics]] very much like [[classical mathematics]]. This is why constructivism has few consequences for basic [[combinatorics]] and [[algebra]] (although it does have important consequences for more advanced topics in those fields). In [[analysis]], in contrast, [[constructivism]] matters right away, because constructively the set of [[real numbers]] may not have decidable tight apartness. 

## Related concepts

* [[set]]

* [[inequality space]]

* [[discrete field]]

[[!redirects classical set]]
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