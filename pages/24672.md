[[!redirects sets in homotopy type theory]]
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

* An [[h-set]] (as common in [[cubical type theory]] and [[Martin-Löf type theory]])
* A preset/type with an [[equivalence relation]]/[[symmetric relation|symmetric]] [[preorder]] (as common in preset theories)
* An h-set with an [[equivalence relation]]/[[symmetric relation|symmetric]] [[preorder]] 
* A [[Bishop set]] (as common in [[Errett Bishop]]'s [[Bishop's constructive mathematics|branch of constructive mathematics]])
* A [[setoid]] (as common in [[MLTT]] without the [[quotient set]] [[higher inductive type]])

In [[homotopy type theory]] (and more generally in any [[intensional type theory]]), all these definitions are valid, but they lead to different structures which behave differently from each other. This article is dedicated to distinguishing between the different set-like structures which have popped up throughout history, in the context of homotopy type theory. 

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

The graph $(A_0, A_1)$ is similarly called 

* **transitive** if its edge type family is transitive

* **symmetric** if its edge type family is symmetric

* **reflexive** if its edge type family is reflexive

In analogy with similar concepts in category theory ([[wild category]], [[precategory]], [[strict category]], and [[univalent category]]), we define the following:

A **wild set** $(A_0, A_1,\mathrm{trans}, \mathrm{sym}, \mathrm{refl})$ is a reflexive, symmetric, transitive graph. 

A **preset** is a wild set whose hom-types are [[h-propositions]]. This is the same as a type with an [[equivalence relation]]. Note that "preset" used here is different from the notion of [[preset]] in preset theories like [[SEAR]] without equality, which correspond more to bare types in homotopy type theory. 

A **strict set** or **strict preset** is a preset whose object type is also an h-set. 

A **univalent set** is a preset which satisfies the Rezk completion condition

$$\mathrm{idToArr}:a =_{A_0} b \simeq A_1(a, b)$$

Univalent sets are the same as [[h-sets]], and so they are typically just called **[[sets]]**. 

We do the same for the notion of [[setoids]]/[[Bishop set]]:

A **wild setoid** $(A_0, A_1,\mathrm{trans}, \mathrm{sym}, \mathrm{refl})$ is the same as a wild set, a reflexive, symmetric, transitive graph. These are the [[setoids]]/[[Bishop sets]] talked about in general [[intensional type theory]]. 

A **[[presetoid]]** is a wild setoid whose hom-types are [[h-sets]]. This is the same as a type with a [[pseudo-equivalence relation]]. 

A **[[strict category|strict]] setoid** is a presetoid whose object type is also an h-set. These are the [[setoids]]/[[Bishop sets]] talked about in [[set-level foundations]]. 

A **[[univalent setoid]]** is a [[presetoid]] which satisfies the Rezk completion condition

$$\mathrm{idToIso}:a =_{A_0} b \simeq a \cong b$$

where $a \cong b$ are the hom-sets of the [[core]] [[pregroupoid]] of the [[presetoid]]. 

## Bijections, isomorphisms, and equivalences 

We begin with wild sets 
$$A \coloneqq (A_0, A_1, \mathrm{trans}_A, \mathrm{refl}_A, \mathrm{sym}_A)$$ 
$$B \coloneqq (B_0, B_1, \mathrm{trans}_B, \mathrm{refl}_B, \mathrm{sym}_B)$$ 
$$C \coloneqq (C_0, C_1, \mathrm{trans}_C, \mathrm{refl}_C, \mathrm{sym}_C)$$ 
An extensional function between two wild sets $f:A \to B$ consists of a function $f_0:A_0 \to B_0$ and for each object $a:A_0$ and $b:B_0$ a function $f_1(a, b):A_1(a, b) \to B_1(a, b)$. 

The identity function $id_A:A \to A$ is an extensional function which consists of the identity function $id_{A_0}:A_0 \to A_0$ for all elements $a:A_0$ and $b:A_0$, the identity function $id_\equiv(a, b):(a \equiv_A b) \to (a \equiv_A b))$. 

The composition $g \circ f:A \to C$ of extensional functions $f:A \to B$ and $g:B \to C$ is defined as 
$$(g \circ f)_0 \coloneqq g_0 \circ f_0$$ 
and for all objects $a:A_0$ and $b:A_0$, 
$$(g \circ f)_\equiv(a, b) \coloneqq g_equiv(f_0(a), f_0(b)) \circ f_equiv(a, b)$$

We naively copy the set-theoretic definitions of [[injection]], [[surjection]], and [[bijection]] over to type theory

An extensional function $f:A \to B$ is a **[[injection]]** if for all elements $b:B_0$ the type of elements $a:A_0$ with a witness $p(a, b):B_1(f_0(a), b)$ is a [[subsingleton]].

$$\mathrm{isInj}(f) \coloneqq \prod_{b:B_0} \mathrm{isProp}\left(\sum_{a:A} B_1(f_0(a), b)\right)$$

An extensional function $f:A \to B$ is a **[[surjection]]** if for all elements $b:B_0$ the type of elements $a:A_0$ with a witness $p(a, b):B_1(f_0(a), b)$ is inhabited.

$$\mathrm{isSurj}(f) \coloneqq \prod_{b:B_0} \left|\sum_{a:A} B_1(f_0(a), b)\right|$$

An extensional function $f:A \to B$ is a **[[bijection]]** if for all elements $b:B_0$ the type of elements $a:A_0$ with a witness $p(a, b):B_1(f_0(a), b)$ is a [[singleton]].

$$\mathrm{isBij}(f) \coloneqq \prod_{b:B_0} \mathrm{isContr}\left(\sum_{a:A} B_1(f_0(a), b)\right)$$

We also naively copy the categorical-theoretic definition of [[isomorphism]] over to type theory

An extensional function $f:A \to B$ is an **[[isomorphism]]** if there exist an extensional function $g:B \to A$ with witnesses 
$$\mathrm{ret}_0(f, g):(g \circ f)_0 = id_{A_0}$$ 
$$\mathrm{sec}_0(f, g):(f \circ g)_0 = id_{B_0}$$ 
$$\mathrm{ret}_1(f, g)(a, b):(g \circ f)_1(a, b) = id_{A_1}(a, b)$$ 
$$\mathrm{sec}_1(f, g)(a, b):(f \circ g)_1(a, b) = id_{B_1}(a, b)$$

An extensional function $f:A \to B$ is an **[[equivalence]]** if the function $f_0:A_0 \to B_0$ is an equivalence of types and for all elements $a:A_0$ and $b:A_0$ the function $f_1(a, b):A_1(a, b) \to B_1(f_0(a), f_0(b))$ is an equivalence of types. 

The only notion of wild sets for which the set-theoretic notions of [[bijection]], [[isomorphism]], and [[equivalence]] are all the same is an [[h-set]]: a transitive, reflexive, and symmetric graph whose hom-types are propositionally truncated, and which satisfy the [[Rezk completion]] condition

$$\mathrm{idToArr}:a =_{A_0} b \simeq A_1(a, b)$$

Isomorphism and equivalence of wild sets are the same only when both the object type and the hom-types are [[h-sets]]. Bijection and equivalence of wild sets are the same only in the presence of the Rezk completion condition on the structure. Combined with the requirement that the object type is an [[h-set]], this automatically means that the hom-types are [[h-propositions]], which makes the entire structure an [[h-set]]. 

This is why [[h-sets]] are simply called [[sets]] in [[homotopy type theory]] and more generally in [[intensional type theory]]. 

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