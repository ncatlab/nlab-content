+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Historically, there have been [[foundations]] which do not take the notion of [[set]] to be the fundamental notion. These include [[preset]] theories over [[first order logic]] such as [[SEAR#eqfree|certain presentations of SEAR]], as well as [[type theories]] like [[MLTT]] and [[cubical type theory]]. In such theories, there have been multiple proposed definitions of what a [[set]] should be. These include:

* An [[h-set]] (as common in [[cubical type theory]])
* A preset/type with an [[equivalence relation]]/[[symmetric relation|symmetric]] [[preorder]] (as common in preset theories)
* An h-set with an [[equivalence relation]]/[[symmetric relation|symmetric]] [[preorder]] 
* A [[Bishop set]] (as common in [[Errett Bishop]]'s [[Bishop's constructive mathematics|branch of constructive mathematics]])
* A [[setoid]] (as common in [[MLTT]] without the [[quotient set]] [[higher inductive type]])

In [[homotopy type theory]] (and more generally in any [[intensional type theory]]), all these definitions are valid definitions of "sets", but they lead to different structures which behave differently from each other. This article is dedicated to distinguishing between the different notions of sets which have popped up throughout history, in the context of homotopy type theory. 

## Definitions

A **[[proposition]]** is a type $A$ such that for all elements $a:A$ and $b:A$ there is an element $p(a, b):a =_A b$. An **[[h-set]]** is a type $A$ where every identity type $a =_A b$ is an proposition for all elements $a:A$ and $b:A$. 

We take the approach in [CapriottiKraus17](#CapriottiKraus17) in defining a **[[graph]]** $A \coloneqq (A_0, A_1)$ to be a type $A_0$ with a type family $A_1(a, b)$ indexed by elements $a:A_0$ and $b:A_0$. While not defined in CapriottiKraus17, we could continue to borrow from graph theory terminology and call  the type family $A_1$ the **[[edge]] type family** of a graph. 

The edge type family $A_1$ is 

* **transitive** if it comes with a family of functions
$$\mathrm{trans}(a, b, c):(A_1(a, b) \times A_1(b, c)) \to A_1(a, c)$$

* **symmetric** if it comes with a family of functions
$$\mathrm{sym}(a, b):A_1(a, b)\to A_1(b, a)$$

* **reflexive** if it comes with a family of elements
$$\mathrm{refl}(a):A_1(a, a)$$

* a **pseudo-relation** if every type $A_1(a, b)$ is an [[h-set]]. 

* a **[[relation]]** if every type $A_1(a, b)$ is an propositon. 

The graph $(A_0, A_1)$ is similarly called 

* **transitive** if its edge type family is transitive

* **symmetric** if its edge type family is symmetric

* **reflexive** if its edge type family is reflexive

A **[[Bishop set]]** $(A_0, A_1,\mathrm{trans}, \mathrm{sym}, \mathrm{refl})$ is a reflexive, symmetric, transitive graph. Historically in type theory $A_1$ was called an "equivalence relation", but the term "relation" in the context of [[homotopy type theory]] refers to edge type families for which all its edge types are [[propositions]]. 

A **[[pseudo-equivalence relation]]** is a reflexive, transitive, and symmetric pseudo-relation. A **[[setoid]]** is an h-set with a pseudo-equivalence relation. 

A **[[preorder]]** is a reflexive and transitive relation. An  **[[equivalence relation]]** is a [[symmetric relation|symmetric]] [[preorder]]. Thus, every type with an equivalence relation is a **symmetric preordered type**, and every h-set with an equivalence relation is a **symmetric [[proset]]**. 

Every symmetric preordered type is thus a Bishop set whose edge type family is a relation, or equivalently, if every edge type $A_1(a, b)$ is a propositon for elements $a:A_0$ and $b:A_0$. 

Every symmetric proset is a setoid whose pseudo-equivalence relation is an [[equivalence relation]], or equivalently, if every edge type $A_1(a, b)$ is a propositon for elements $a:A_0$ and $b:A_0$. 

Every h-set is equivalent to a type with an equivalence relation for which the canonical function
$$\mathrm{idtoequiv}(a, b):(a = b) \to A_1(a, b)$$
is an equivalence for all $a:A_0$ and $b:A_0$. 

## See also

* [[preset]]
* [[set]]
* [[setoid]]
* [[Bishop set]]
* [[h-set]]
* [[equivalence relation]]
* [[graph]]

For a similar phenomenon in defining preorders and posets, see

* [[relation between preorders and (0,1)-categories]]
* [[preorder]]
* [[poset]]
* [[thin category]]
* [[Prop]]-[[enriched category]]
* [[(0,1)-category]]

And for defining a [[category]] in [[homotopy type theory]], see

* [[category]]
* [[precategory]]
* [[univalent category]]
* [[strict category]]
* [[wild category]]

## References

* {#Bishop67} [[Errett Bishop]], _Foundations of Constructive Analysis_. New York: McGraw-Hill (1967)

* {#Palmgren05} [[Erik Palmgren]],  _Bishop's set theory_ (2005) ([pdf](http://www.cse.chalmers.se/research/group/logic/TypesSS05/Extra/palmgren.pdf))

* {#CapriottiKraus17} [[Paolo Capriotti]], [[Nicolai Kraus]], _Univalent Higher Categories via Complete Semi-Segal Types_ ([arXiv:1707.03693](https://arxiv.org/abs/1707.03693))