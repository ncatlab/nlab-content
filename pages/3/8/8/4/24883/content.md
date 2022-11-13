
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

There are two general approaches to [[structural set theory]]; those that attempt to axiomatise the [[category]] [[Set]] of [[sets]] and [[functions]], and those that attempt to axiomatise the [[allegory]] [[Rel]] of [[sets]] and [[relations]]. The former is called **categorical set theory**. 

## Types of categorical set theories

One distinguishes between simply sorted categorical set theories, where membership is a [[relation]], and dependently sorted categorical set theories, where membership is a typing [[judgment]]. 

### Simply sorted categorical set theories

Simply sorted categorical set theories have a sort of possible sets and a sort of possible elements, and a membership relation between the sort of possible sets and the sort of possible elements. By possible set we mean that some of the terms in the sort might be a set; and by possible element we mean that some of the terms in the sort might be an element. 

* In unsorted categorical set theory, there is only a sort or judgment of [[functions]], and the sort/judgment of functions plays the role of both the sort of possible sets and the sort of possible elements. 
* In two-sorted categorical set theory, there are sorts for [[functions]] and [[sets]], the sort of sets plays the role of the sort of possible sets, and the sort of functions plays the role of the sort of possible elements. 
* In three-sorted categorical set theory, there are sorts for [[functions]], [[sets]], and [[elements]], and the sort of sets plays the role of the sort of possible sets, and the sort of elements plays the role of the sort of possible sets. 

#### Unsorted categorical set theory

Unsorted categorical set theory only consists of [[functions]] as primitive [[judgments]] or [[sorts]]. The elements are defined as functions with singleton domain ($\mathrm{element}(a) \coloneqq (\mathrm{dom}(a) = 1)$) However, there are multiple ways of defining sets in unsorted categorical set theory, each which lead to a different categorical set theory; examples include but are not limited to

* [[identity functions]] ($\mathrm{set}(a) \coloneqq \mathrm{dom}(a) = a$ or $\mathrm{set}(a) \coloneqq \mathrm{codom}(a) = a$)
* [[functions]] with [[singleton]] [[codomain]] ($\mathrm{set}(a) \coloneqq \mathrm{codom}(a) = 1$) 
* [[functions]] with [[empty set]] [[domain]] ($\mathrm{set}(a) \coloneqq \mathrm{dom}(a) = 0$)

In any unsorted first-order categorical set theory, the [[membership relation]] is a defined global relation on the functions, rather than a primitive global relation as in [[material set theory]]. For each definition of set, there is a definition of membership relation:

* for sets as identity functions, given functions $a$ and $b$, the membership relation is defined as $a$ being an element, $b$ being a set, and the codomain of $a$ being equal to $b$:
$$a \in b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(b) \wedge \mathrm{codom}(a) = b$$

* for sets as functions into the singleton, given functions $a$ and $b$, the membership relation is defined as $a$ being an element, $b$ being a set, and the codomain of $a$ being equal to the domain of $b$:
$$a \in b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(b) \wedge \mathrm{codom}(a) = \mathrm{dom}(b)$$

* for sets as functions out of the empty set, given functions $a$ and $b$, the membership relation is defined as $a$ being an element, $b$ being a set, and the codomain of $a$ being equal to the codomain of $b$:
$$a \in b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(b) \wedge \mathrm{codom}(a) = \mathrm{codom}(b)$$

While that membership relation can be proven to satisfy the [[axiom of weak extensionality]], it cannot in general be proven to satisfy the [[axiom of strong extensionality]]. In addition, depending on the definition of the set, the membership relation has different properties: 

* for sets as identity functions, every set is a [[Quine atom]] with respect to $\in$
* for sets as functions with singleton codomain, only sets in bijection with the singleton is a [[Quine atom]] with respect to $\in$
* for sets as functions with empty set domain, no set is a [[Quine atom]] with respect to $\in$ 

The canonical example of an unsorted first-order categorical set theory is [[fully formal ETCS]]. An [[axiom schema of collection]] or [[axiom schema of replacement]] could be added to fully formal ETCS to get an unsorted categorical set theory which is equivalent in strength to [[ZFC]]. 

#### Two-sorted categorical set theory

Two-sorted categorical set theory consists of [[sets]] and [[functions]] as primitive [[judgments]] or [[sorts]]. The elements are defined as functions with singleton domain. 

The canonical example of this is the two-sorted first-order theory [[ETCS]] of sets, functions, identity functions, and composition of functions. An [[axiom schema of collection]] or [[axiom schema of replacement]] could be added to ETCS to get an two-sorted categorical set theory which is equivalent in strength to [[ZFC]]. 

#### Three-sorted categorical set theory

Three-sorted categorical set theory consists of [[sets]], [[functions]], and [[elements]] as primitive [[judgments]] or [[sorts]]. An example of a three-sorted categorical set theory is the simply-sorted presentation of [[structural ZFC]]. 

### Dependently sorted categorical set theory

Two-sorted categorical set theory can also be expressed as a dependently sorted categorical set theory, where there are [[sets]], and there are [[functions]] which depend on a pair of sets. 

An example of this is the dependently sorted version of [[ETCS]]. 

Three-sorted categorical set theory can also be expressed as a dependently sorted categorical set theory, where there are [[sets]], there are [[elements]] which depend on a set, and there are [[functions]] which depend on a pair of sets. 

An example of this is [[ETCS with elements]], which defines the theory of a [[concrete category|concrete]] [[well-pointed topos]] with [[natural numbers object]] and the [[axiom of choice]]. 

An [[axiom schema of collection]] or [[axiom schema of replacement]] could be added to ETCS with elements to get an two-sorted categorical set theory which is equivalent in strength to [[ZFC]]. 

## See also

* [[structural set theory]]

* [[categorical set theory]], [[allegorical set theory]]

[[!redirects categorical set theory]]
[[!redirects categorical set theories]]