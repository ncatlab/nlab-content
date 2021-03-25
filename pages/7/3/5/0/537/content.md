
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The notion of _disjoint coproduct_ is a generalization to arbitrary [[categories]] of that of _[[disjoint union]]_ of sets.

One says that a [[coproduct]] $X + Y$ of two [[objects]] $X, Y$ in a [[category]] $\mathcal{C}$ is _disjoint_ if the [[intersection]] of $X$ with $Y$ in $X + Y$ is [[initial object|empty]]. In this case one often writes $X \coprod Y \coloneqq X + Y$ for the coproduct, particularly if the coproduct is [[extensive category|stable under pullbacks]], and speaks of the _[[disjoint union]]_ of $X$ with $Y$.

## Definition

### In a category

A [[coproduct]] $a+b$ in a [[category]] is **disjoint** if

1. the coprojections $a\to a+b$ and $b\to a+b$ are [[monomorphism|monic]], and 

2. their [[intersection]] is an [[initial object]].

Equivalently, this means we have [[pullback]] squares

$$
\array{ a & \to & a &&&
b & \to & b &&&
0 & \to & b\\
\downarrow && \downarrow &&&
\downarrow && \downarrow &&&
\downarrow && \downarrow \\
a & \to & a+b &&&
b & \to & a+b &&&
a & \to & a+b}
$$

An arbitrary coproduct $\sum_i a_i$ is disjoint if each coprojection $a_i\to \sum_i a_i$ is monic and the intersection of any two is initial.  Note that every 0-ary coproduct (that, is initial object) is disjoint.

## Examples

* In the category $Set$ of sets and functions, the coproduct is given by [[disjoint union]] and is, unsurprisingly, disjoint. In the category $Pfn$ of sets and [[partial function|partial functions]] the coproduct is equally  given by disjoint union and total injections and is disjoint as well.
 
* Since having all finitary disjoint coproducts is half of the condition for a category to be [[extensive category|extensive]], extensive categories provide [[extensive category#examples|examples for categories with disjoint finite coproducts]]. In the preceding discussion $Set$ instantiates this case whereas $Pfn$ does not: since the initial object $\emptyset$ in $Pfn$ is not [[strict initial object|strict]], the latter category is not extensive.

* In the category $Vect$ of (real) [[vector space|vector spaces]] coproducts are given by [[direct sum]] and are disjoint but not [[pullback-stable colimit|stable under pullback]]: pulling back the colimit diagram $\mathbb{R}\to\mathbb{R}\oplus\mathbb{R}\leftarrow\mathbb{R}$ along the diagonal morphism $\Delta:\mathbb{R}\to\mathbb{R}\oplus\mathbb{R}\; ,\; x\mapsto x\oplus x$ yields $0\to\mathbb{R}\leftarrow 0$ which is not a colimit diagram. Whence $Vect$ is not [[extensive category|extensive]].

* Non-example: the [[interval category]]  $\left\{
    0 \to 1
  \right\}$ has coproducts but they are not all disjoint: $1+1=1$. 
There are plenty more examples of [[posets]] that have non-disjoint coproducts besides this one. In a [[Boolean algebra]], two elements $a$ and $b$ are disjoint in the sense that $a\wedge b=0$ if and only if $a\vee b$ is their disjoint coproduct. 

## Properties

### Characterization of sheaf toposes
  

Having all small disjoint coproducts is one of the conditions in [[Giraud's theorem]] characterizing [[sheaf toposes]].

### In coherent categories

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a [[coherent category]]. If $X, Y \hookrightarrow Z$ are two [[subobjects]] of some [[object]] $Z \in \mathcal{C}$ and are disjoint, in that their [[intersection]] in $Z$ is [[initial object|empty]], $X \cap Y \simeq\emptyset$, then their [[union]] $X \cup Y$ is their (disjoint) [[coproduct]].

=--

This apears as ([Johnstone, cor. A1.4.4](#Johnstone)).

+-- {: .num_defn #PositiveCategory}
###### Definition

A coherent category in which all coproducts are disjoint is also called a **[[positive category|positive coherent category]]**.

=--

([Johnstone, p. 34](#Johnstone))

+-- {: .num_example}
###### Example

Every [[extensive category]] is in particular positive, by definition.

=--

In a positive coherent category, every morphism into a coproduct factors through the coproduct coprojections:

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a postive coherent category, def. \ref{PositiveCategory}, and let $f \colon A \to X \coprod Y$ be a [[morphism]]. Then the two [[subobjects]] $f^*(X) \hookrightarrow A$ and $f^*(Y) \hookrightarrow Y$ of $A$, being the [[pullbacks]] in 

$$
  \array{
    f^* (X) &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{i_X}}
    \\
    A &\stackrel{f}{\to}& X \coprod Y
  }
  \;\;\;\;
  \array{
    f^* (Y) &\to& Y
    \\
    \downarrow && \downarrow^{\mathrlap{i_Y}}
    \\
    A &\stackrel{f}{\to}& X \coprod Y
  }
$$

are disjoint in $A$ and $A$ is their disjoint coproduct

$$
  A \simeq f^*(X) \coprod f^*(Y)
  \,.
$$

=--

This appears in ([Johnstone, p. 34](#Johnstone)).

+-- {: .num_remark}
###### Remark

This means that if $A \in \mathcal{C}$ itself is indecomposable in that it is not a coproduct of two objects in a non-trivial way, for instance if $\mathcal{C}$ is an [[extensive category]] and $A \in \mathcal{C}$ is a [[connected object]], then every morphism $A \to X \coprod Y$ into a disjoint coproduct factors through one of the two canonical inclusions.

=--

## Related concepts

* [[disjoint subset]]

* [[disjunctive logic]]


## References

For instance page 34 in section A1.4.4 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_


[[!redirects disjoint coproduct]]
[[!redirects disjoint coproducts]]


