
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A first-order hyperdoctrine is a [[hyperdoctrine]] with respect to  [[lattices]] that are [[Heyting algebras]].

## Definition

We denote by $HeytAlg_{AdjCyl}$ the category whose objects are [[Heyting algebras]], and whose
morphisms are Heyting algebra morphisms having both [[left adjoint|left]] and [[right adjoint]]s. (The adjoints are not required to be Heyting algebra morphisms, but can be arbitrary monotone maps.)

A **first-order hyperdoctrine** consists of a [[category]] with [[finite products]] $C_T$, along with a [[functor]] 

$$
  P \colon C_T^{op} \to HeytAlg_{AdjCyl}
$$ 
such that the following [[Beck-Chevalley condition]] is satisfied: for every [[object]] $A$, the [[left adjoint]]s to $P(\pi)$ for the [[projection]]s $\pi : A \times - \to -$ comprise a [[natural transformation]] from $P(A \times -)$ to $P(-)$, and so do the right adjoints. This expresses the Beck-Chevalley condition for pullback squares of the form 

$$\array{
A \times B & \stackrel{\pi_B}{\to} & B \\
 ^\mathllap{1_A \times f} \downarrow & & \downarrow^\mathrlap{f} \\
A \times C & \underset{\pi_C}{\to} & C
}$$ 

An element of $P(A)$ is often called a _predicate over $A$_ (with respect to the hyperdoctrine). 

For any first-order hyperdoctrine, an _equality predicate_ can be defined for each type $A \in Ob(C_T)$ as 

$$\exists(\delta_A)(\top_{P(A)}) \in P(A \times A)$$ 

where for any morphism $f$ in $C_T$, we use $\exists (f)$ to denote the left adjoint of $P(f)$, and $\top_H$ denotes the top element in a Heyting algebra $H$. 

However, to get good properties for equality, we need to assume a little more. A **first-order hyperdoctrine with [[equality]]** is a first-order hyperdoctrine such that the Beck-Chevalley condition is satisfied for pullback diagrams of the form  

$$\array{
A\times B & \stackrel{A\times f}{\to} & A \times C \\
 ^\mathllap{\delta_A\times B} \downarrow & & \downarrow^\mathrlap{\delta_A \times C} \\
A \times A \times B& \underset{A\times A\times f}{\to} & A \times A \times C
},$$ 

i.e. that $P(A\times A \times f) \circ \exists (\delta_A \times B) = \exists (\delta_A \times C) \circ P(A\times f)$. 


This assures that the equality predicate is well behaved
in the sense that it allows a sound interpretation of first order logic with equality in the hyperdoctrine. 

Additionally one may require the condition for pullbacks  of the form  

$$\array{
A & \stackrel{\delta_A}{\to} & A \times A \\
 ^\mathllap{\delta_A} \downarrow & & \downarrow^\mathrlap{1_A \times \delta_A} \\
A \times A & \underset{\delta_A \times 1_A}{\to} & A \times A \times A
},$$ 
which is a kind of [Frobenius law](http://ncatlab.org/nlab/show/Frobenius+reciprocity#frobenius_laws_and_frobenius_reciprocity_11). By taking right adjoints, a similar equation holds for $\forall (f)$ in place of $\exists (f)$, where $P(f) \dashv \forall (f)$. 

### As an Internal Heyting Algebra

Similar to the [[natural models]] formulation of a [[category with families]], a first-order hyperdoctrine can be defined concisely using the [[internal language]] of presheaf categories. That is, a first-order hyperdoctrine is equivalently defined as a category $C_T$ with finite products and $P$ an internal Heyting algebra in the category of presheaves on $C_T$ that additionally has

1. For every $A \in C_T$ internal $YA$-meets and joins where $YA$ is the [[representable]] presheaf of $A$.
2. For every $A \in C_T$, $P$ internally has an $YA$-equality predicate, i.e., a least reflexive binary relation on $YA$ valued in $P$. In more detail, this is an internal function $=_A \in P^{YA \times YA}$ such that for every $f \in P^{YA\times YA}$ we have $\forall x,y. x =_A y \leq f(x,y)$ if and only if $\forall x\in A. \top \leq f(x,x)$. 

Here the Beck-Chevalley conditions on the quantifiers and equality arises from the fact that the operations are internal and therefore natural in $C$. Unraveling the internal language, this definition is the same as the formulation given by Lawvere that requires only equality predicates and adjoints to substitution along projections.

### Interpretation

With this, we have enough structure to interpret multi-sorted [[first order logic|first-order]] [[intuitionistic logic]] with equality, taking the objects of $C_T$ to be sorts and its morphisms to be terms, $P$ to assign to each sort the [[Lindenbaum algebra]] of [[predicates]] upon that sort and to each term the operation of substitution of that term into predicates, and the left and right adjoints to $P$ upon projections to provide existential and universal [[quantification]], respectively, with the existence of the further adjoints providing the ability to interpret equality, and the [[Beck-Chevalley condition]] ensuring that quantification commutes appropriately with substitution (just as the propositional connectives do).

### Variants

There are, of course, many variants on this, corresponding straightforwardly to modifications of the kind of logic one wishes to represent. For instance, to represent specifically classical logic, one should use [[Boolean algebras]] instead of [[Heyting algebras]]. To represent first-order logic without equality, one should no longer require left and right adjoints to every morphism in the range of $P$, but rather only those given by the natural transformations yielding the quantifiers (i.e., only requiring adjoints to substitution along projections). Various higher-order constructs can be added by adding new ways of forming objects in $C_T$ (e.g., adding cartesian closedness). Etc.

One can even extend this into the realm not just of provability, but furthermore of proof theory, by taking the objects in the codomain of $P$ to be categories rather than mere [[preorder]]s (e.g., by using [[bicartesian closed category|bicartesian closed categories]] rather than [[Heyting algebra]]s); in this case, the objects in a category $P(\sigma)$ would still represent predicates on the sort $\sigma$, but the morphisms in $P(\sigma)$ would represent proofs (rather than mere provability) of entailments between these predicates, with the possibility that not all such proofs would be equal.

## Related concepts

* [[tripos]]

[[!include categories and logic - table]]

[[!redirects first-order hyperdoctrines]]

[[!redirects first-order hyperdoctrine with equality]]
[[!redirects first-order hyperdoctrines with equality]]
