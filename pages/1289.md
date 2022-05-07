
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A __coreflective subcategory__ is a [[full subcategory]] whose inclusion functor has a [[right adjoint]] $R$ (a [[cofree functor]]):

$$
  C \stackrel{\overset{i}{\hookrightarrow}}{\underset{R}{\leftarrow}} D
  \,.
$$


The dual concept is that of a [[reflective subcategory]]. See there for more details.

## Characterizations


+-- {: .num_prop #CharacterizationByLocalization}
###### Proposition
**(equivalent characterizations)**

Given any pair of [[adjoint functors]]

$$
  (L \dashv R)
  \;:\; 
  B
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}} 
      {\bot}
  A
$$ 

the following are equivalent:

1. The [[left adjoint]] $L$ is [[full and faithful functor|fully faithful]]. (In this case $A$ is equivalent to its [[essential image]] in $B$ under $L$, a full [[coreflective subcategory]] of $B$.) 

2. The [[unit of an adjunction|unit]] $\eta : 1_A \to R L$ of the [[adjunction]] is a [[natural isomorphism]] of functors.

3. The [[comonad]] $(L R, L\eta R,\epsilon)$ associated with the adjunction is [[idempotent comonad|idempotent]], the left adjoint $L$ is [[conservative functor|conservative]], and the right adjoint $R$ is [[essentially surjective functor|essentially surjective on objects]].

4. If $S$ is the set of morphisms $s$ in $B$ such that $R(s)$ is an [[isomorphism]] in $A$, then $R \colon B \to A$ realizes $B$ as the (nonstrict) [[colocalization]] of $B$ with respect to the class $S$. 

5. The [[right adjoint]] $R$ is [[codense functor|codense]].

=--

For proofs, see the corresponding characterisations for [[reflective subcategories]].

## Properties

+-- {: .un_theorem}
###### Theorem

[[Vopěnka's principle]] is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[colimit]]s is a [[coreflective subcategory]].

=--

This is ([AdamekRosicky, theorem 6.28](#AdamekRosicky)).


## Examples

* the inclusion of [[Kelley space]]s into [[Top]], where the right adjoint "kelleyfies"

* the inclusion of [[torsion theory|torsion]] [[abelian groups]] into [[Ab]], where the right adjoint takes the [[torsion subgroup]].

* the inclusion of groups into monoids, where the right adjoint takes a monoid to its group of units.

* [[Lie integration]], which constructs a [[simply connected space|simply connected]] [[Lie group]] from a finite-dimensional real [[Lie algebra]]. The coreflector is Lie differentiation (taking a Lie group to its associated Lie algebra), and the [[counit]] is the natural map to a given Lie group $G$ from the universal [[covering space]] of the [[connected space|connected component]] at the identity of $G$. 

* In a [[recollement]] situation, we have several reflectors and coreflectors. We have a reflective and coreflective subcategory $i_*: A' \hookrightarrow A$ with reflector $i^*$ and coreflector $i^!$. The functor $j^*$ is both a reflector for the reflective subcategory $j_*: A'' \hookrightarrow A$, and a coreflector for the coreflective subcategory $j_!: A'' \hookrightarrow A$.

## Related concepts

* [[Quillen coreflection]]

## References

* {#AdamekRosicky} [[Jiri Adamek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, London Mathematical Society Lecture Note Series 189

* Robert El Bashir, Jiri Velebil, _Simultaneously Reflective And Coreflective Subcategories of Presheaves_ ([TAC](http://www.tac.mta.ca/tac/volumes/10/16/10-16abs.html))

[[!redirects coreflective subcategories]]

[[!redirects coreflective embedding]]
[[!redirects coreflective embeddings]]

[[!redirects co-reflective subcategory]]
[[!redirects co-reflective subcategories]]

[[!redirects coreflector]]
[[!redirects coreflectors]]
[[!redirects coreflection]]
[[!redirects coreflections]]
