
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Prefix Orders
* table of contents
{: toc}

## Idea ##

By a  _prefix order_ we mean a [[partial order]] which is also downwards [[total order|totally ordered]].

The concept was introduced in ([Cuijpers 13a](#Cuijpers13a), [Cuijpers 13b](#Cuipers13b)) in the context of [[semantics]] for [[programming languages]], and in particular hybrid and cyber-physical systems, as need arose to generalize the notion of (execution) tree to something that would include a mix of continuous and discrete progress of time. After a lot of experimentation, [Cuijpers 13a](#Cuijpers13a) discovered that the generalization needed was something that expresses two things: time branches when it goes forward (due to different possible courses of action a system may take), but seems linear when looking backward. 

A different way of looking at it, is that executions of systems have a natural prefix order on them. Trying to come up with a generic definition of what a 'prefix' is, Cuijpers could not find anything in literature and came up with the definition below. As it turns out, in roughly the same period, [Ferlez-Cleaveland-Marcus 14](#FerlezCleavelandMarcus14) discovered the definition of "pointed prefix orders" and named them "generalized execution trees".


## Definition ##

### As a set with extra structure

A prefix order may be understood as a [[set]] with [[extra structure]].

Given a [[set]] $S$, a __prefix order__ on $S$ is a (binary) [[relation]] $\leq$ with the following properties:

* [[reflexive relation|reflexivity]]: $x \leq x$ always;

* [[transitive relation|transitivity]]: if $x \leq y \leq z$, then $x \leq z$;

* [[antisymmetric relation|antisymmetry]]: if $x \leq y \leq x$, then $x = y$.

* [[downward totality]]: if $x \leq z$ and $y \leq z$, then $x \leq y$ or $y \leq x$.

A __prefix ordered set__ is a set equipped with a prefix order.


### As a partial order with downward totality

A prefix ordered set is precisely a [[poset]] satisfying the extra condition that 
$x \leq z$ and $y \leq z$ implies that $x \leq y$ or $y \leq x$. 


### History preserving functions

The morphisms of prefix ordered sets are [[history preserving function]]s.
Given $x \in S$, the __history__ of $x$ is the set $x^- = \{ y \mid y \leq x \}$.
A __history preserving function__ $f$ from a prefix ordered set $S$ to a prefix ordered set $T$ is a [[function]] from $S$ to $T$ (seen as [[structured sets]]) such that $f(x^-) = f(x)^-$. 

Equivalently, it is a [[monotone function]] between $S$ and $T$ (interpreted as [[posets]]) satisfying the additional property that for every $x \in S$ and $y \in T$ such that $y \leq f(x)$ there exists a $x' \in S$ with $x' \leq x$ and $f(x') = y$.

In this way, prefix ordered sets form a [[category]] [[Pfx]]. Furthermore, they are sometimes also viewed as a [[concrete category]] over [[Pos]] (rather than [[Set]]), with history preserving maps preserving the way in which executions of a system unfold, while order preserving maps preserve only the way in which the executions are observed by external observers. (For an example of why this distinction is useful, see also the article on [[embedding open maps]] as a generalization of [[bisimulation]])


## Properties ##

* Every prefix order is isomorphic to its set of histories under subsets, leading to the intuition that the elements of a prefix order 'are' their histories. Formally: given a prefix ordered set $S$, the set $H = \{ x^- \mid x \in S \}$ is prefix ordered and isomorphic to $S$ (with 'taking the history of an element' and 'taking the maximum of a history' being the witnessing isomorphisms).

* Products of prefix orders are not the usual Cartesian products, but rather are formed by all possible 'mergings' of the histories of elements of the combined prefix orders.

* In the work of Cleaveland, a different type of products was defined, but at this point I do not know of a notion of morphism on prefix ordered sets that would result in that product.


## Examples ##

* Be careful. Products of prefix orders are not the usual Cartesian products, rather the histories of a prefix order are 'merged'. When taking the product of a countable and an uncountable history, unexpected phenomena may happen that leave one with an empty set. A 'cure' for this seems to be to restrict to prefix orders in which each history has a minimum.


## Related concepts

* [[partial order]]
* In some books on order theory, a partially ordered set that is downward well-ordered is used as a characterization of a [[tree]]. Prefix orders relax this definition to downward total orders.
* Any partial order can be viewed as an [[Alexandroff topology]]. When viewing prefix orders as an Alexandroff topology, the history preserving maps translate to continuous open maps.

## References 
 {#References}

* {#Cuijpers13a} [[Pieter Cuijpers]], _Prefix Orders as a General Model of Dynamics_, Proceedings of the [9th International Workshop on Developments in Computational Models (DCM)](http://www.dcm-workshop.org.uk/2013/) p. 25–29 ([pdf](http://www.dcm-workshop.org.uk/2013/dcm-2013-pre-proc.pdf#page=30))

* {#Cuijpers13b} [[Pieter Cuijpers]], _The Categorical Limit of a Sequence of Dynamical Systems_, [EPTCS 120 : Proceedings EXPRESS/SOS 2013](https://www.win.tue.nl/expresssos2013/), p. 78-92, 2013 ([arXiv:1307.7445](https://arxiv.org/abs/1307.7445), [doi:10.4204/EPTCS.120.7]())

* {#FerlezCleavelandMarcus14} James Ferlez, Rance Cleaveland, Steve Marcus, _Generalized Synchronization Trees_, LLNCS 8412: Proceedings of FOSSACS'14, 2014, p. 304–319 (<a href="https://doi.org/10.1007/978-3-642-54830-7_20">10.1007/978-3-642-54830-7_20</a>)


[[!redirects prefix ordered]]
[[!redirects downward totality]]
[[!redirects downward total relation]]
[[!redirects history preserving function]]
[[!redirects Pfx]]
