[[!redirects cube category]]
# Contents
* table of contents
{: toc}

## Idea

A **category of cubes** is a category of [[geometric shapes for higher structures]] in which the basic shapes are cubes of all dimensions.  There are actually many different categories of cubes, depending on what sorts of operations are permitted between cubes; potential operations include:

* faces and degeneracies
* connections
* symmetries
* reversals
* diagonals

## Definitions

### The ordered cube category

The ordered cube category has faces and degeneracies, but no other operations.

+-- {: .num_defn #NotationOneTruncatedCategoryOfCubes}
###### Notation

We denote by $\square_{\leq 1}$ the category defined uniquely (up to isomorphism) by the following.

1) There are exactly two objects, which we shall denote by $I^{0}$ and $I^{1}$.

2) There are exactly two arrows $i_{0}, i_{1} : I^{0} \rightarrow I^{1}$.

3) There is exactly one arrow $p : I^{1} \rightarrow I^{0}$.

4) There are no non-identity arrows $I^{0} \rightarrow I^{0}$. 

5) There are exactly two non-identity arrows $I^{1} \rightarrow I^{1}$, which are $i_{0} \circ p$ and $i_{1} \circ p$.

=--

+-- {: .num_defn #RemarkCommutativeDiagrams}
###### Remark

In particular, because of 4) in Notation \ref{NotationOneTruncatedCategoryOfCubes}, the diagram 

$$
   \array{
      I^{0}  & \overset{i_{0}}{\to}    & I^{1} \\
             & \underset{id}{\searrow} & \downarrow p \\
             &                         & I^{0}
   }
$$

commutes in $\square_{\leq 1}$, and the diagram 

$$
   \array{
      I^{0}  & \overset{i_{1}}{\to}    & I^{1} \\
             & \underset{id}{\searrow} & \downarrow p \\
             &                         & I^{0}
   }
$$

commutes in $\square_{\leq 1}$.

=--

+-- {: .num_defn}
###### Remark

The category $\square_{\leq 1}$ is isomorphic to the category $\Delta_{\leq 1}$, i.e. it may also be described as

 * The full subcategory of the [[simplex category]] $\Delta$ on the objects $[0]$ and $[1]$.

 * (A skeleton of) the category of linearly ordered sets of cardinality 1 or 2.

 * The indexing category for [[reflexive coequalizer|reflexive equalizers]].

=--

+-- {: .num_defn}
###### Remark

The category $\square_{\leq 1}$ can also be constructed by beginning with the free category on the directed graph defined uniquely by the fact that 1), 2), and 3) in Notation \ref{NotationOneTruncatedCategoryOfCubes} hold, and by the fact that there are no other non-identity arrows. One then takes a quotient of this free category which forces the diagrams in Remark \ref{RemarkCommutativeDiagrams} to commute. 

This quotient can be expressed as a colimit in the category of small categories, or, which ultimately amounts to the same, by means of the equivalence relation $\sim$ on the arrows of the free category generated by requiring that $p \circ i_{0} \sim id$ and $p \circ i_{1} \sim id$, and by requiring that $g_{1} \circ g_{0} \sim f_{1} \circ f_{0}$ if $g_{1} \sim f_{1}$ and $g_{0} \sim f_{0}$. 

=--

+-- {: .num_defn}
###### Definition

The _category of cubes_ is the [[free strict monoidal category]] on $\square_{\leq 1}$ whose unit object is $I^{0}$.

=--

+-- {: .num_defn}
###### Notation

We denote the category of cubes by $\square$.

=--

+-- {: .num_defn}
###### Terminology

We refer to $\square$ as the _category of cubes_.

=--

+-- {: .num_defn}
###### Remark

It is _not_ the case that $\square$ is the free strict monoidal category on $\square_{\leq 1}$. Rather, $\square$ is the free strict monoidal category _with specified unit_ on $\square_{\leq 1}$, where the unit is specified to be $I^{0}$.

=--

+-- {: .num_defn}
###### Notation

Let $n \geq 0$ be an integer. We often denote the object $\underbrace{I^{1} \otimes \cdots \otimes I^{1}}_{n}$ of $\square$ by $I^{n}$. 

=--

### The symmetric cube category

The symmetric, or substructural, or semicartesian, or "BCH", cube category has faces, degeneracies, and symmetries only.

### The cartesian cube category

The cartesian, or "ABCFHL", cube category has faces, degeneracies, symmetries, and diagonals.

### The De Morgan cube category

The De Morgan, or "CCHM", cube category has faces, degeneracies, symmetries, diagonals, connections, and reversals. 

## Expository material

For expository and other material, see [[category of cubes - exposition]].

## References

For the semicartesian cube category:

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 3* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-12.pdf), [video](https://www.youtube.com/watch?v=9pDddxB7LbE))

[[!redirects symmetric cube category]]
[[!redirects semicartesian cube category]]
[[!redirects cartesian cube category]]
[[!redirects de Morgan cube category]]