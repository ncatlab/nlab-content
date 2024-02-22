
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In the [[foundations]] of [[mathematics]], an [[axiom of infinity]] is any axiom that asserts that [[infinite set]]s exist. In [[set theory]] and [[set-level type theory]], infinite sets cannot be constructed from finite sets, so their existence must be posited as an extra axiom. Further axioms, in this vein which assert the existence of even larger sets that cannot be constructed from smaller ones are called [[large cardinal]] axioms.

## Statement

### Natural numbers

One common form of the axiom of infinity says that the particular set $N$ of [[natural number]]s exists.  In material [[set theory]] this often takes the form of asserting that the von Neumann [[ordinal number]] $\omega$ exists, where $\omega$ is characterized as the smallest set such that $\emptyset\in\omega$ and whenever $a\in \omega$ then $a\cup \{a\}\in \omega$.  In structural set theory the usual form of the axiom of infinity is the existence of a [[natural numbers object]]. 

In [[dependent type theory]], the axiom of infinity for a [[Tarski universe]] is given by the element
$$\mathrm{axinf}_U:\sum_{\mathbb{N}:U} \sum_{0:T(\mathbb{N})} \sum_{s:T(\mathbb{N}) \to T(\mathbb{N})} \prod_{C:T(\mathbb{N}) \to U} \prod_{c_0:T(C(0))} \prod_{c_s:\prod_{x:T(\mathbb{N})} T(C(x)) \to T(C(s(x)))} \sum_{c:\prod_{x:T(\mathbb{N})} T(C(x))} (c(0) =_{T(C(0))} c_0) \times \prod_{x:T(\mathbb{N})} (c(s(x)) =_{T(C(s(x)))} c_s(c(x)))$$
or
$$\mathrm{axinf}_U:\sum_{\mathbb{N}:U} \sum_{0:T(\mathbb{N})} \sum_{s:T(\mathbb{N}) \to T(\mathbb{N})} \prod_{C:U} \prod_{c_0:T(C)} \prod_{c_s:T(C) \to T(C)} \exists!c:T(\mathbb{N}) \to T(C).(f(0) =_{T(C)} c_0) \times \prod_{n:T(\mathbb{N})} c(s(n)) =_{T(C)} c_s(c(n))$$
which states that there is a [[natural numbers type]] in the universe. 

There is an alternate way to express the axiom of infinity in a Tarski universe, as the axiom of resizing the [[set truncation]] of the [[type of finite types]] in $U$, since $\mathrm{isFinite}$ and set truncations are definable from the [[type of propositions]] in $U$, $\sum_{A:U} \mathrm{isProp}(A)$, but they are all usually large, and so have to be resized to be small:

$$\mathrm{axinf}_U:\sum_{\mathbb{N}:U} T(\mathbb{N}) \simeq \left[\sum_{A:U} \mathrm{isFinite}(T(A))\right]_0$$

### Integers

#### Inductive definition

Instead of a defining the natural numbers via its induction principle, one can instead define the [[integers]] via its induction principle, and then use the fact that disjoint unions are disjoint and $\mathbb{Z} \cong \mathbb{Z} \uplus \mathbb{Z}$ to construct the natural numbers. 

#### Second-order definition

Alternatively, one can assume a (trichotomous) [[ordered integral domain]] $\mathbb{Z}$, such that every (trichotomous) ordered integral subdomain of $\mathbb{Z}$ is equivalent to the [[improper subset]] of $\mathbb{Z}$. This defines the [[integers]], since the integers are the [[initial object|initial]] (trichotomous) ordered integral domain and are [[strict initial object|strictly initial]]. Since the integers as defined automatically comes with a [[total order]] $\leq$ and a [[pseudo-order]] $\lt$, one can define the natural numbers as the set of non-negative integers. 

The benefit of such a definition of infinity is that it allows for a [[strongly predicative mathematics|strongly predicative]] definition of the [[natural numbers]], the [[rational numbers]], and the [[real numbers]] in [[dependent type theory]], since one doesn't need arbitrary [[function sets]] or [[dependent function types]] to define the natural numbers, which one needs to characterize the natural numbers by its usual recursion or induction principle. Instead, one only needs dependent function types of a family of propositions, weak function extensionality, and the power set of the ordered integral domain $\mathbb{Z}$. Unlike the case for arbitrary ordered integral domains, being an ordered integral subdomain is only a property of an element of a power set, and then one can construct the type of ordered integral subdomains of $\mathbb{Z}$, from which one can characterize $\mathbb{Z}$ as having a contractible type of ordered integral subdomains of $\mathbb{Z}$. 

### Rational numbers

If one has [[power sets]], one can assume an ([[trichotomous]]) [[ordered field]] $\mathbb{Q}$, such that every (trichotomous) ordered [[subfield]] of $\mathbb{Q}$ is equal to the [[improper subset]] of $\mathbb{Q}$. This defines the [[rational numbers]], since the rational numbers are the initial (trichotomous) [[ordered field]] and are [[strict initial object|strictly initial]]. The rational numbers are automatically infinite, and one can construct the [[integers]] $\mathbb{Z}$ as the [[intersection]] of all [[ordered integral domain|ordered integral subdomains]] of $\mathbb{Q}$, and since the integers as defined automatically comes with a [[total order]] $\leq$ and a [[pseudo-order]] $\lt$, one can define the natural numbers as the set of non-negative integers. 

## Generalizations 

In the form of an NNO, the axiom of infinity generalises to the existence of [[inductive type]]s or [[W-type]]s.  These can be constructed from a NNO if [[power set]]s exist, but in [[predicative mathematics|predicative]] theories they can be added as additional axioms.

One could also posit the existence of the set of [[extended natural numbers]] instead of the set of natural numbers, as the set of extended natural numbers have [[countable|countably infinite]] cardinality and is the categorical [[duality|dual]] of the natural numbers in Set, a [[terminal coalgebra]] for the endofunctor $F(X) = 1 + X$ in Set. This generalises to the existence of [[coinductive types]] or [[M-types]], which can be added as additional axioms. 

One could also posit the existence of [[FinSet]], the collection of [[finite sets]]. In dependent type theory this is a [[type of finite types]], a [[universe]] $\mathcal{U}$ that satisfies the axiom of finiteness (see below).

## Alternatives

Broadly speaking, [[finite mathematics]] is mathematics that does not use or need the axiom of infinity; a finitist is an extreme breed of [[constructive mathematics|constructivist]] that believes that mathematics is better without the axiom of infinity, or even that this axiom is false.

A more extreme case is to *deny* the axiom of infinity with an __axiom of finiteness__: every set is [[finite set|finite]].  There is one of these for every definition of 'finite' given on that page; here is the strongest stated directly in terms of [[set theory]] as an axiom of [[induction]]:

* Any property of sets that is invariant under [[isomorphism]] and holds for the [[empty set]] must hold for all sets if, whenever it holds for a set $X$, it holds for the [[disjoint union]] $X \uplus \{*\}$. 

In [[material set theory]], this is equivalent given the [[axiom of foundation]] (which guarantees that $X$ and $\{X\}$ are [[disjoint sets|disjoint]]):

* Any property of sets that holds for the empty set must hold for all sets if, whenever it holds for a set $X$, it holds for the [[union]] $X \cup \{X\}$.

In higher categorical terms, the above axiom of finiteness could be stated as follows: [[Set]] is an initial algebra of the 2-endofunctor $F(X) \cong X \coprod 1$ in the [[(2,1)-category]] [[Grpd]]. 

In [[dependent type theory]], given a [[Tarski universe]] $(U, T)$ that is closed under the [[empty type]], the [[unit type]], and [[sum types]], the axiom of finiteness for the universe states that 

* For all type families $A:U \vdash C(A)$ such that $T(A) \simeq T(B)$ implies that $C(A) \simeq C(B)$, elements $c_0:C(\mathbb{0})$ and dependent functions $c_s:\prod_{A:U} C(A) \to C(A + \mathbb{1})$, there exists a unique dependent function $c:\prod_{A:U} C(A)$ such that $c(\mathbb{0}) =_{C(\mathbb{0})} c_0$ and for all $A:U$, $c(A + 1) =_{C(A + 1)} c_s(c(A))$. 

In [[dependent type theory]] with [[dependent product types]], [[dependent sum types]], [[identity types]], [[function extensionality]], and a [[type of all propositions]], the *axiom of finiteness* for the entire type theory is an [[axiom schema]] which states that given a type $A$, one could derive a witness that the type is a [[finite type]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{finWitn}_A:\mathrm{isFinite}(A)}$$

where

$$
\mathrm{isFinite}(A) \equiv 
\begin{array}{c}
\prod_{S:(A \to \mathrm{Prop}) \to \mathrm{Prop}} (((\lambda x:A.\bot) \in S) \times \prod_{P:A \to \mathrm{Prop}} \prod_{Q:A \to \mathrm{Prop}} (P \in S) \\
\times (\exists!x:A.x \in Q) \times (P \cap Q =_{A \to \mathrm{Prop}} \lambda x:A.\bot) \to (P \cup Q \in S)) \to ((\lambda x:A.\top) \in S)
\end{array}
$$

The membership relation and the subtype operations used above are defined in the nLab article on [[subtypes]]. 

In particular, the axiom of finiteness for the entire type theory implies the [[principle of excluded middle]] for the [[type of all propositions]], since the only finite propositions are the [[decidable propositions]]. Furthermore, the axiom of finiteness implies that the type theory is a [[set-level type theory]] because every finite type is an [[h-set]]. 

## Related concepts

* [[finite set]], [[finite object]]

* [[Set]], [[FinSet]]

## References

In relation to [[classifying toposes]]:

* [[Andreas Blass]], *Classifying topoi and the axiom of infinity*, Algebra Universalis **26** (1989) 341-345 &lbrack;[doi:10.1007/BF01211840](https://doi.org/10.1007/BF01211840)&rbrack; 

For constructing the [[natural numbers]] from the [[integers]]:

* {#Sattler23} [[Christian Sattler]], *Natural numbers from integers* ([pdf](https://www.cse.chalmers.se/~sattler/docs/naturals.pdf))

category: foundational axiom

[[!redirects axiom of infinity]]
[[!redirects axioms of infinity]]

[[!redirects axiom of finiteness]]
[[!redirects axioms of finiteness]]
[[!redirects axiom of finity]]
[[!redirects axioms of finity]]
