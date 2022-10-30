
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An [[operad]] whose [[algebras over an operad]] are triples consistsing of two [[associative algebras]] $A$, $B$ and an $A$-$B$-[[bimodule]] .

## Definition

+-- {: .num_defn}
###### Definition

Write $BMod$ for the [[colored operad|colored]] [[symmetric operad]] whose

* [[objects]] are three elements, to be denoted $\mathfrak{a}_-, \mathfrak{a}_+$ and $\mathfrak{n}$;

* [[multimorphisms]] $(X_i)_{i = 1}^n \to Y$ form

  * if $Y = \mathfrak{a}_-$ and all $X_i = \mathfrak{a}_-$ then: the set of [[linear orders]] of $n$ elements;

  * if $Y = \mathfrak{a}_*$ and all $X_i = \mathfrak{a}_*$ then again: the set of [[linear orders]] of $n$ elements;

  * if $Y = \mathfrak{n}$: the set of linear orders $\{i_1 \lt \cdots \lt i_n\}$ such that there is exactly one index $i_k$ with $X_{i_k} = \mathfrak{n}$ and $X_{i_j} = \mathfrak{a}_-$ for all $j \lt k$ and $X_{i_j} = \mathfrak{a}_+$ for all $k \gt k$.

* [[composition]] is given by the composition of linear orders as for the [[associative operad]].

=--

## Properties

### Relation to the associative operad
 {#RelationToTheAssociativeOperad}

There are two canonical inclusions $Assoc \to BMod$ of the [[associative operad]] given by labelling its unique color/object with either $\mathfrak{a}_-$ or $\mathfrak{a}_+$, respectively. For 

$$
  (A_1,A_2,N) \colon BMod^\otimes \to \mathcal{C}^\otimes
$$

a morphism to a [[symmetric monoidal category]], there compositions pick the left and the right algebra

$$
  A_i \colon Assoc^\otimes \to BMod^\otimes \stackrel{(A_1, A_2, N)}{\to}
  \mathcal{C}^\otimes
  \,.
$$

There is also a morphism $BMod \to Assoc$ given by forgetting the labels and just remembering the linear orders. 

+-- {: .num_defn}
###### Proposition

This is a [[fibration of (∞,1)-operads]].

=--

In ([Lurie](#Lurie)) this appears as remark 4.3.1.8.

This is such that for

$$
  A \colon Assoc^\otimes \to \mathcal{C}^\otimes
$$

an algebra, the composite

$$
  (A, A, A) \colon BMod^\otimes \to Assoc^\otimes \stackrel{A}{\to} \mathcal{C}^\otimes
$$

exhibits $A$ canonically as a bimodule over itself.

### Relation to the operad for modules over an algebra

Similarly, there is an inclusion of the [[operad for modules over an algebra]]

$$
  LMod \to BMod
$$

etc. 

### Relation to bitensoring
 {#RelationToBitensoring}

+-- {: .num_defn}
###### Definition

A [[coCartesian fibration of (∞,1)-operads]] $\mathcal{C}^\otimes \to BMod^\otimes$, hence the structure of a  $BMod$-[[monoidal (∞,1)-category]] is a **bi[[tensoring]]** of 

$$
  \mathcal{C} \coloneqq \mathcal{C}^\otimes \underset{BMod}{\times} \{\mathfrak{n}\}
$$

over the (ordinary) [[monoidal (∞,1)-categories]]

$$
  \mathcal{C}^\otimes_{\pm}
  \coloneqq
  \mathcal{C}^\otimes \underset{BMod}{\times} Assoc^\otimes_{\pm}
  \,.
$$

=--

([Lurie, def. 4.3.1.17](#Lurie))

+-- {: .num_remark}
###### Remark

By the [[microcosm principle]], bitensored $(\infty,1)$-categories are the right context into which to internalize [[bimodules]]. See _[Relation to the category of bimodules](#RelationToCategoriesOfBimodules)_ below.

=--



### Relation to categories of bimodules
 {#RelationToCategoriesOfBimodules}

For $\mathcal{C}^\otimes \to BMod^\otimes$ a [[fibration of (∞,1)-operads]] the corresponding [[(∞,1)-category]] of [[(∞,1)-algebras over an (∞,1)-operad]]

$$
  BMod(\mathcal{C})
  \coloneqq
  Alg_{/BMod}(\mathcal{C})
$$

is the [[(∞,1)-category of (∞,1)-bimodules]] in $\mathcal{C}$.

## Related concepts

* [[operad for modules over an algebra]]

## References

Section 4.3.1 in 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects operad for bimodules over algebras]]