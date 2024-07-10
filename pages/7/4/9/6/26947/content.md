
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[setoid]] whose [[quotient set]] is a [[ring]]. Equivalently, a [[thin category|thin]] [[ring category|ring]] [[groupoid]], or in foundations where groupoids are [[univalent groupoid|univalent]] by default, a [[thin category|thin]] ring [[pregroupoid]]. 

“Ring setoid” is a placeholder name for a concept which may or may not have another name in the mathematics literature. 

## Definition

A **ring setoid** is a [[setoid]] $(A, \sim)$ with elements $0 \in A$ and $1 \in A$ and functions $\alpha:A \times A \to A$, $\nu:A \to A$, and $\mu:A \times A \to A$, such that 

* $(A, \sim, 0, \alpha, \nu)$ is a [[braided groupal setoid]]

* $(A, \sim, 1, \mu)$ is a [[monoidal setoid]]

* $\mu$ distributes over $\alpha$ up to the [[equivalence relation]]: for all elements $a \in A$, $b \in A$, and $c \in A$, 
$$\mu(a, \alpha(b, c)) \sim \alpha(\mu(a, b), \mu(a, c)) \quad \mathrm{and} \quad \mu(\alpha(a, b), c) \sim \alpha(\mu(a, c), \mu(b, c))$$

$A$ is **[[commutative ring|commutative]]** or **[[symmetric monoidal category|symmetric]]** or **[[braided monoidal category|braided]]** if additionally for all elements $a \in A$ and $b \in A$, $\mu(a, b) \sim \mu(b, a)$. 

## Examples

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is a [[ring setoid]]. 

## Related concepts

* [[setoid]]

* [[ring]], [[commutative ring]]

* [[monoidal setoid]], [[groupal setoid]]

* [[ring category]]

[[!redirects ring setoid]]
[[!redirects ring setoids]]

[[!redirects thin ring groupoid]]
[[!redirects thin ring groupoids]]

[[!redirects thin ring pregroupoid]]
[[!redirects thin ring pregroupoids]]

[[!redirects commutative ring setoid]]
[[!redirects commutative ring setoids]]

[[!redirects symmetric ring setoid]]
[[!redirects symmetric ring setoids]]

[[!redirects thin symmetric ring groupoid]]
[[!redirects thin symmetric ring groupoids]]

[[!redirects thin symmetric ring pregroupoid]]
[[!redirects thin symmetric ring pregroupoids]]

[[!redirects braided ring setoid]]
[[!redirects braided ring setoids]]

[[!redirects thin braided ring groupoid]]
[[!redirects thin braided ring groupoids]]

[[!redirects thin braided ring pregroupoid]]
[[!redirects thin braided ring pregroupoids]]