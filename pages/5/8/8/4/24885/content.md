+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

A membership relation is a [[binary relation]] $\in$ found in [[simple type theory|simply sorted]] [[set theory]] between terms which can be elements and terms which can be sets. Membership relations are found both [[material set theory]] and [[structural set theory]]. 

This is in contrast to [[dependent type theory|dependently sorted]] set theories, where membership $\in$ is a typing [[judgment]] rather than a binary relation. 

## Properties

Membership relations have different properties in different set theories which can be distinguished. 

### Homogeneous and heterogeneous membership relations

Recall that a [[binary relation]] $R$ takes values in sorts $A$ and $B$. A binary relation $R$ is **homogeneous** or an **endorelation** if it takes values in the same sort $A$, and a binary relation is **heterogeneous** if it takes values in two distinct sorts $A$ and $B$. 

The membership relation $\in$ is homogeneous if both sets and elements are terms of the same sort, while $\in$ is heterogeneous if sets and elements are terms of different sorts. For example, in [[ZFC]], [[ZFA]], and [[fully formal ETCS]], the membership relations $\in$ are homogeneous, while in the traditional presentation of [[ETCS]] as a two-sorted theory, the membership relation $\in$ is heterogeneous. 

### Material and structural membership relations

Another important difference is the distinction between the membership relations in material and structural set theories, in what we could call **material membership relation** and **structural membership relation**. This has been proposed to distinguish between [[material set theory]] and [[structural set theory]] in set theories with [[homogeneous membership relations]]:

A set theory with a homogeneous membership relation is a **[[material set theory]]** if it has a material membership relations, and it is a **[[structural set theory]]** if it has a structural membership relation. If the set theory has multiple homogeneous membership relations, the set theory is a **structural set theory** if there exists a structural membership relation, and the set theory is a **material set theory** if every homogeneous membership relation $\in$ is a [[material membership relation]]. 

A few definitions have been proposed to distinguish between homogeneous membership relations in material and structural set theories:

#### Structural membership relations without Quine atoms

Both material set theories like [[ZFC]] and [[ZFA]] and structural set theories like [[fully formal ETCS]] have a homogeneous membership relation on the theory (and fully formal ETCS has multiple homogeneous membership relations). This means that merely having a homogeneous membership relation is not sufficient for the membership relation to be a material membership relation. 

One proposed difference between material set theory and structural set theory is that in material set theory, elements have internal structure and/or sets are the internal structure of some other objects, while in structural set theory, elements do not have internal structure and sets are not the internal structure of other objects.  

Thus, an element $e$ **has internal structure** if there exists an object $a$ such that $a \in e$, and an set $S$ **is an internal structure** if there exists an object $a$ such that $S \in a$. 

$$\mathrm{hasInternalStructure}(e) \coloneqq \mathrm{isElement}(e) \wedge \exists a.a \in e$$
$$\mathrm{isInternalStructure}(S) \coloneqq \mathrm{isSet}(S) \wedge \exists a.S \in a$$

If an set theory only has one homogeneous membership relation, then the membership relation is a **material membership relation** if there exists an element $e$ which has internal structure or a set $S$ which is an internal structure, and the membership relation is a **structural membership relation** if for all elements $e$, $e$ does not have internal structure, and for all sets $S$, $S$ is not an internal structure. 

$$\mathrm{isMaterial} \coloneqq \exists a.(\mathrm{hasInternalStructure}(a) \vee \mathrm{isInternalStructure}(a))$$

$$\mathrm{isStructural} \coloneqq \forall a.(\neg\mathrm{hasInternalStructure}(a) \wedge \neg\mathrm{isInternalStructure}(a))$$

Thus, the membership relation in a theory like [[ZFC]] is a material membership relation because sets and elements are the same, and thus all elements have internal structure and all sets are internal structure. The same is true of any theory of [[pure sets]], such as [[New Foundations]]. In a theory with non-set [[urelements]] such as [[ZFA]], the membership relation is still a material membership relation, because every object in the theory is an element, and while urelements do not have internal structure, there exist other elements which do have internal structure, namely those elements which are sets. 

In contrast, the homogeneous membership relation in [[fully formal ETCS]], defined by 
$$a \in b \coloneqq s(a) = 1 \wedge s(b) = 0 \wedge t(a) = t(b)$$
where the constant primitive $1$ is the identity morphism of the terminal object and the constant primitive $0$ is the identity morphism of the initial object, and where sets and elements are defined as
$$\mathrm{isSet}(a) \coloneqq s(b) = 0$$
$$\mathrm{isElement}(a) \coloneqq s(b) = 1$$
is a structural membership relation, because it can be proven that every element does not have internal structure and every set is not internal structure. 

#### Structural membership relations with Quine atoms

The above definition states that in a structural set theory with a homogeneous membership relation, [[Quine atoms]] cannot exist. However, this means that in [[fully formal ETCS]] when sets are defined as identity functions or as functions with singleton codomain, the defined  membership relation $\in$ is a material membership relation, as in both cases the singleton is a [[Quine atom]] with respect to $\in$. From one point of view, one could argue that those given definitions of set are incorrect, and one should instead use a definition of set which results in a structural homogeneous membership relation. 

However, since the subset of [[identity functions]], functions with [[singleton]] [[codomain]], and functions with [[empty set]] [[domain]] are all in [[bijection]] with each other, it should not matter which subset of function to designate as the sets. This motivates an alternate definition of structural and material membership relations, which allow for Quine atoms to exist with respect to a structural membership relation. 

A membership relation is a **structural membership relation** if each connected component of the respective membership graph is either an edgeless vertex, a rooted [[tree]] whose children are all leaves, or possibly a vertex with a single loop:

* the edgeless vertex represents the [[empty set]], as well as any non-set non-element objects in the set theory 

* the root of the rooted tree represents a set with more than one element, as well as the [[singleton]] in presentations of unsorted structural set theories where the singleton is different from the element in the singleton. The children leaves of the root represent the elements of the set. 

* the vertex with a single loop represents a [[Quine atom]] with respect to the membership relation $\in$, which occur in some definitions of sets in structural set theories, such as defining sets as [[identity functions]] or as functions with [[singleton]] [[codomain]], where the [[singleton]] is always a [[Quine atom]]. 

A **material membership relation** is then a membership relation whose membership graphs have more complex structure than those of structural membership relations. 

## See also

* [[relation]]
* [[set theory]]

[[!redirects membership relation]]
[[!redirects membership relations]]

[[!redirects homogeneous membership relation]]
[[!redirects homogeneous membership relations]]

[[!redirects heterogeneous membership relation]]
[[!redirects heterogeneous membership relations]]

[[!redirects material membership relation]]
[[!redirects material membership relations]]

[[!redirects structural membership relation]]
[[!redirects structural membership relations]]