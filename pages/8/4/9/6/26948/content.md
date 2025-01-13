
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

A [[setoid]] or [[Bishop set]] whose [[quotient set]] is a [[monoid]]. Equivalently, a [[thin category|thin]] [[monoidal category|monoidal]] [[groupoid]], or in foundations where groupoids are [[univalent groupoid|univalent]] by default, a [[thin category|thin]] monoidal [[pregroupoid]]. 

“Monoidal setoid”, "monoidal Bishop set", and "Bishop monoid" are placeholder names for a concept which may or may not have another name in the mathematics literature. 

## Definition

Here we assume that setoids or Bishop sets are equipped with an [[equivalence relation]] (rather than a [[pseudo-equivalence relation]]). A **monoidal setoid** or **monoidal Bishop set** or **Bishop monoid** is a [[setoid]] $(A, \sim)$ with an element $e \in A$ and a function $m:A \times A \to A$ such that 

* $m$ preserves the [[equivalence relation]]: for all elements $a \in A$, $b \in A$, $c \in A$, and $d \in A$, if $a \sim c$ and $b \sim d$, then $m(a, b) \sim m(c, d)$. 

* $m$ is associative up to the equivalence relation: for all elements $a \in A$, $b \in A$, $c \in A$, $m(a, m(b, c)) \sim m(m(a, b), c)$

* $m$ is left and right unital up to the equivalence relation: for all elements $a \in A$, $m(a, e) \sim a$ and $m(e, a) \sim e$. 

$A$ is **[[commutative monoid|commutative monoidal]]** or **[[symmetric monoidal category|symmetric monoidal]]** or **[[braided monoidal category|braided monoidal]]** if additionally for all elements $a \in A$ and $b \in A$, $m(a, b) \sim m(b, a)$. 

## Examples

* The set $\mathbb{N}^\mathbb{2}$ of functions from the [[boolean domain]] $\mathbb{2}$ to the [[natural numbers]] $\mathbb{N}$, equipped with the equivalence relation $f \sim g \coloneqq f(0) + g(1) = f(1) + g(0)$, is a monoidal setoid.  

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is a [[monoidal setoid]]. 

* Given any [[Archimedean ordered field]] $F$, the set of all [[locators]] of all elements of $F$ is a [[monoidal setoid]].

* The [[quotient set]] of any [[monoidal setoid]] by its [[equivalence relation]] is a monoidal setoid where the equivalence relation is given by equality

* More generally, any [[monoid]] is a monoidal setoid in which the equivalence relation is given by equality. 

## Monoidal setoid homomorphisms

A **monoidal setoid [[homomorphism]]** between two monoidal setoids $A$ and $B$ is a function $h:A \to B$ such that 

* $f$ preserves the equivalence relation: for all $a \in A$ and $b \in A$, $a \sim_A b$ implies $f(a) \sim_B f(b)$

* $f$ preserves the monoidal unit up to equivalence relation: $f(e_A) \sim_B e_B$

* $f$ preserves the monoidal product up to equivalence relation: for all $a \in A$ and $b \in A$, 
$$f(m_A(a, b)) \sim_B m_B(f(a), f(b))$$

\begin{theorem}
Let $A$ be a monoidal setoid, and let $A / \sim$ be its [[quotient set]]. Then the function $[-]:A \to (A / \sim)$ which takes an element of $A$ to its [[equivalence class]] is a monoidal setoid homomorphism. 
\end{theorem}

## Related concepts

* [[setoid]]

* [[monoid]]

* [[groupal setoid]]

* [[ring setoid]]

* [[monoidal category]]

* [[A-monoid]]

[[!redirects monoidal setoid]]
[[!redirects monoidal setoids]]

[[!redirects monoidal Bishop set]]
[[!redirects monoidal Bishop sets]]

[[!redirects Bishop monoid]]
[[!redirects Bishop monoids]]

[[!redirects thin monoidal groupoid]]
[[!redirects thin monoidal groupoids]]

[[!redirects thin monoidal pregroupoid]]
[[!redirects thin monoidal pregroupoids]]

[[!redirects commutative monoidal setoid]]
[[!redirects commutative monoidal setoids]]

[[!redirects commutative monoidal Bishop set]]
[[!redirects commutative monoidal Bishop sets]]

[[!redirects commutative Bishop monoid]]
[[!redirects commutative Bishop monoids]]

[[!redirects braided monoidal setoid]]
[[!redirects braided monoidal setoids]]

[[!redirects braided monoidal Bishop set]]
[[!redirects braided monoidal Bishop sets]]

[[!redirects thin braided monoidal groupoid]]
[[!redirects thin braided monoidal groupoids]]

[[!redirects thin braided monoidal pregroupoid]]
[[!redirects thin braided monoidal pregroupoids]]

[[!redirects symmetric monoidal setoid]]
[[!redirects symmetric monoidal setoids]]

[[!redirects symmetric monoidal Bishop set]]
[[!redirects symmetric monoidal Bishop sets]]

[[!redirects thin symmetric monoidal groupoid]]
[[!redirects thin symmetric monoidal groupoids]]

[[!redirects thin symmetric monoidal pregroupoid]]
[[!redirects thin symmetric monoidal pregroupoids]]

[[!redirects monoidal setoid homomorphism]]
[[!redirects monoidal setoid homomorphisms]]

[[!redirects monoidal Bishop set homomorphism]]
[[!redirects monoidal Bishop set homomorphisms]]