[[!redirects category of partial functions]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The essentially algebraic structure of partial endofunctions on a set $S$, and specific cases for when $S$ is an [[abelian group]], [[commutative ring]], and [[field]] respectively. 

## Definition ##

### In a set ###

Given a set $S$, the **category of [[partial function|partial]] [[endofunctions]]** in $S$, or just **category of partial functions**, is the [[concrete category]] $Part(S)$ with objects called [[subset]]s $A \in Ob(Part(S))$ with the set of elements for each subset $El(A)$, and the set of morphisms consist of functions $Hom(A, \Im(S)) \coloneqq (A \to S)$ for each subset $A \in Ob(Part(S))$, where $\Im(S)$ is the improper subset, as well as the set of monomorphisms $Hom(A, B)$ consisting of the subset inclusions for subsets $A \in Ob(Part(S))$ and $B:Ob(Part(S))$. 

There exist a global operator representing **composition of partial functions**

$$(-)\circ_{Part(S)}(-): \sum_{A:Ob(Part(S))} \sum_{B:Ob(Part(S))} Hom(A, \Im(S)) \times Hom(B, \Im(S)) \to Hom(A \cap B, \Im(S))$$

where

* for partial functions $f \in Hom(A, \Im(S))$, $g \in Hom(B, \Im(S))$, and $h \in Hom(C, \Im(S))$, given the canonical isomorphism $i_a \in Hom(A \cap (B \cap C), (A \cap B) \cap C)$, $i_a \circ (f \circ_{Part(S)} (g \circ_{Part(S)} h)) = ((f \circ_{Part(S)} g) \circ_{Part(S)} h)$

* for partial function $f \in Hom(A, \Im(S))$ and subset $B \subseteq A$, there is a function $g \in Hom(B, \Im(S))$ such that $g = f \circ_{Part(S)} i_{B,A}$ for canonical injection $i_{B,A} \in Hom(B,A)$,

* for partial function $f \in Hom(A, \Im(S))$ and superset $B \supseteq A$, there is a function $h \in Hom(B, \Im(S))$ such that $h \circ_{Part(S)} i_{A,B} = f $ for canonical injection $i_{A,B} \in Hom(A,B)$,

* for partial function $f \in Hom(A, \Im(S))$, $f = f \circ_{Part(S)} id_S$ and $f = id_S \circ_{Part(S)} f$ for the identity function $id_S:Hom(\Im(S), \Im(S))$

### In an abelian group ###

If $S$ is a [[abelian group]], then for every subset $A \in Ob(Part(S))$, $Hom(A, \Im(S))$ is a [[abelian group]], and in addition to the global operators corresponding to composition of partial functions, there exist global operators representing **addition of partial functions** and **negation of partial functions**, 

$$(-)+(-): \{A \in Ob(Part(S)) \vert Hom(A, \Im(S))\} \times \{B \in Ob(Part(S)) \vert Hom(B, \Im(S))\} \to \{(A,B) \in Ob(Part(S)) \times Ob(Part(S)) \vert Hom(A \cap B, \Im(S))\}$$

$$-(-): \{A \in Ob(Part(S)) \vert Hom(A, \Im(S))\} \to Hom(A, \Im(S)))$$

where 

* for partial functions $f \in Hom(A, \Im(S))$ and $g \in Hom(B, \Im(S))$ there is a partial function $f + g \in Hom(A \cap B, \Im(S))$ and a partial function $g + f \in Hom(B \cap A, \Im(S))$ such that given the canonical isomorphism $i_c \in Hom(A \cap B, B \cap A)$,  $i_c \circ (f + g) = (g + f)$

* for partial functions $f \in Hom(A, \Im(S))$, $g \in Hom(B, \Im(S))$, and $h \in Hom(C, \Im(S))$, given the canonical isomorphism $i_a \in Hom(A \cap (B \cap C), (A \cap B) \cap C)$, $i_a \circ (f + (g + h)) = ((f + g) + h)$

* for partial function $f \in Hom(A, \Im(S))$, and supersets $B \supseteq A$ for $B \in Ob(Part(S))$, given the local additive unit $0_{B,\Im{S}} \in Hom(B, \Im(S)$, $f + 0_{B,\Im{S}} = f$ and $0_{B,\Im{S}} + f = f$

* for partial function $f \in Hom(A, \Im(S))$, there is a partial function $-f \in Hom(A, \Im(S))$ representing negation where the negation of $F$ is the local additive inverse of $f$: $-f = -_{A,S}f$

### In a commutative ring ###

If $S$ is a [[commutative ring]], then for every subset $A \in Ob(Part(S))$, $Hom(A, \Im(Part(S)))$ is a $S$-[[commutative algebra]], and in addition to the global operators corresponding to composition, addition, and negation of partial functions, there exist a global operator representing **multiplication of partial functions**

$$(-)\cdot(-): \{A \in Ob(Part(S)) \vert Hom(A, \Im(S))\} \times \{B \in Ob(Part(S)) \vert Hom(B, \Im(S))\} \to \{(A,B) \in Ob(Part(S)) \times Ob(Part(S)) \vert Hom(A \cap B, \Im(S))\}$$

where

* for partial functions $f \in Hom(A, \Im(S))$ and $g \in Hom(B, \Im(S))$ there is a partial function $f \cdot g \in Hom(A \cap B, \Im(S))$ and a partial function $g \cdot f \in Hom(B \cap A, \Im(S))$ such that given the canonical isomorphism $i_c \in Hom(A \cap B, B \cap A)$,  $i_c \circ (f \cdot g) = (g \cdot f)$

* for partial functions $f \in Hom(A, \Im(S))$, $g \in Hom(B, \Im(S))$, and $h:Hom(C, \Im(S))$, given the canonical isomorphism $i_a \in Hom(A \cap (B \cap C), (A \cap B) \cap C)$, $i_a \circ (f \cdot (g \cdot h)) = ((f \cdot g) \cdot h)$

* for partial function $f \in Hom(A, \Im(S))$, and supersets $B \supseteq A$ for $B:Ob(Part(S))$, given the local multiplicative unit $1_{B,\Im{S}} \in Hom(B, \Im(S)$, $f \cdot 1_{B,\Im{S}} = f$ and $1_{B,\Im{S}} \cdot f = f$

* for partial function $f \in Hom(A, \Im(S))$, and supersets $B \supseteq A$ for $B:Ob(Part(S))$, given the local additive unit $0_{B,\Im{S}} \in Hom(B, \Im(S)$, $f \cdot 0_{B,\Im{S}} = 0_{A,\Im{S}}$ and $0_{B,\Im{S}} \cdot f = 0_{A,\Im{S}}$

* for partial functions $f \in Hom(A, \Im(S))$, $g \in Hom(B, \Im(S))$, and $h:Hom(C, \Im(S))$, given the canonical isomorphism $i_l \in Hom(A \cap (B \cap C), (A \cap B) \cap (A \cap C)$, $i_a \circ (f \cdot (g + h)) = (f \cdot g) + (f \cdot h)$

* for partial functions $f \in Hom(A, \Im(S))$, $g \in Hom(B, \Im(S))$, and $h:Hom(C, \Im(S))$, given the canonical isomorphism $i_r \in Hom((A \cap B) \cap C, (A \cap C) \cap (B \cap C)$, $i_a \circ ((f + g) \cdot h)) = (f \cdot h) + (g \cdot h)$

### In a field ###

If $S$ is a [[Heyting field]], then for every subset $A \in Ob(Part(S))$, $Hom(A, \Im(S))$ is a $S$-[[commutative algebra]], with global operators corresponding to composition, addition, negation, and multiplication of partial functions. Let 

$$Hom_{\#0}(A, \im(S)) \coloneqq \{f \in Hom(A, \Im(S)). \vert \forall x \in El(A).f(x) # 0\}$$

be the type of all functions whose evaluations at each element are apart from zero on the entire domain. There exists a global operator representing the **reciprocal of partial functions**:

$$\frac{1}{(-)}: \{A \in Ob(Part(S)) \vert Hom(A, \Im(S))\} \to Hom_{\#0}(A, \Im(S)$$

where

* for partial function $f \in Hom(A, \Im(S))$, 
$$f \cdot \frac{1}{f} = id_{\im(f)_{\#0}}$$
and 
$$\frac{1}{f} \cdot f = id_{\im(f)_{\#0}}$$

and the set $\im(f)_{\#0}$ is defined as 

$$\im(f)_{\#0} \coloneqq \{x \in El(A)\vert f(x) # 0\}$$

## See also ##

* [[partial function]]

* [[rational function]]

## References ##

* Fred Richman, [Algebraic functions, calculus style](https://web.archive.org/web/20130605213603/http://math.fau.edu/richman/Docs/Oily.pdf)

[[!redirects reciprocal of partial functions]]