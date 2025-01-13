
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
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

A [[setoid]] or [[Bishop set]] whose [[quotient set]] is a [[ring]]. Equivalently, a [[thin category|thin]] [[ring category|ring]] [[groupoid]], or in foundations where groupoids are [[univalent groupoid|univalent]] by default, a [[thin category|thin]] ring [[pregroupoid]]. 

“Ring setoid” and "Bishop ring" are placeholder names for a concept which may or may not have another name in the mathematics literature. 

## Definition

A **ring setoid** or **Bishop ring** is a [[setoid]] $(A, \sim)$ with elements $0 \in A$ and $1 \in A$ and functions $\alpha:A \times A \to A$, $\nu:A \to A$, and $\mu:A \times A \to A$, such that 

* $(A, \sim, 0, \alpha, \nu)$ is a [[braided groupal setoid]]

* $(A, \sim, 1, \mu)$ is a [[monoidal setoid]]

* $\mu$ distributes over $\alpha$ up to the [[equivalence relation]]: for all elements $a \in A$, $b \in A$, and $c \in A$, 
$$\mu(a, \alpha(b, c)) \sim \alpha(\mu(a, b), \mu(a, c)) \quad \mathrm{and} \quad \mu(\alpha(a, b), c) \sim \alpha(\mu(a, c), \mu(b, c))$$

$A$ is **[[commutative ring|commutative]]** or **[[symmetric monoidal category|symmetric]]** or **[[braided monoidal category|braided]]** if additionally for all elements $a \in A$ and $b \in A$, $\mu(a, b) \sim \mu(b, a)$. 

## Examples

* The set $\mathbb{N}^\mathbb{2}$ of functions from the [[boolean domain]] $\mathbb{2}$ to the [[natural numbers]] $\mathbb{N}$, equipped with the equivalence relation $f \sim g \coloneqq f(0) + g(1) = f(1) + g(0)$, is a ring setoid.  

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is a [[ring setoid]]. 

* Given any [[Archimedean ordered field]] $F$, the set of all [[locators]] of all elements of $F$ is a [[ring setoid]].

* The [[quotient set]] of any [[ring setoid]] by its [[equivalence relation]] is a ring setoid where the equivalence relation is given by equality

* More generally, any [[ring]] is a ring setoid in which the equivalence relation is given by equality. 

## Ring setoid homomorphisms

A **ring setoid [[homomorphism]]** or **Bishop ring homomorphism** between two ring setoids $A$ and $B$ is a function $h:A \to B$ such that 

* $f$ preserves the equivalence relation: for all $a \in A$ and $b \in A$, $a \sim_A b$ implies $f(a) \sim_B f(b)$

* $f$ preserves the groupal unit up to equivalence relation: $f(0_A) \sim_B 0_B$

* $f$ preserves the groupal product up to equivalence relation: for all $a \in A$ and $b \in A$, 
$$f(\alpha_A(a, b)) \sim_B \alpha_B(f(a), f(b))$$

* $f$ preserves the groupal inverse up to equivalence relation: for all $a \in A$, 
$$f(\nu_A(a)) \sim_B \nu_B(f(a))$$

* $f$ preserves the monoidal unit up to equivalence relation: $f(1_A) \sim_B 1_B$

* $f$ preserves the monoidal product up to equivalence relation: for all $a \in A$ and $b \in A$, 
$$f(\mu_A(a, b)) \sim_B \mu_B(f(a), f(b))$$

\begin{theorem}
Let $A$ be a ring setoid, and let $A / \sim$ be its [[quotient set]]. Then the function $[-]:A \to (A / \sim)$ which takes an element of $A$ to its [[equivalence class]] is a ring setoid homomorphism. 
\end{theorem}

## Related concepts

* [[setoid]]

* [[ring]], [[commutative ring]]

* [[A-ring]]

* [[monoidal setoid]], [[groupal setoid]]

* [[ring category]]

* [[local ring setoid]]

* [[field setoid]]

[[!redirects ring setoid]]
[[!redirects ring setoids]]

[[!redirects Bishop ring]]
[[!redirects Bishop rings]]

[[!redirects thin ring groupoid]]
[[!redirects thin ring groupoids]]

[[!redirects thin ring pregroupoid]]
[[!redirects thin ring pregroupoids]]

[[!redirects commutative ring setoid]]
[[!redirects commutative ring setoids]]

[[!redirects commutative Bishop ring]]
[[!redirects commutative Bishop rings]]

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

[[!redirects ring setoid homomorphism]]
[[!redirects ring setoid homomorphisms]]

[[!redirects Bishop ring homomorphism]]
[[!redirects Bishop ring homomorphisms]]