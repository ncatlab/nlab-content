
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# Floors and ceilings
* table of contents
{: toc}

## Idea

By the *floor* and *ceiling* of a [[real number]] one means the [[integers]], obtained by rounding the real number down or up, respectively.

When viewed as [[functions]] from $\mathbb{R}$ to itself (or to $\mathbb{Z}$), these are standard examples of functions exhibiting partial notions of [[continuity]]: the floor function is both [[right-continuous map|right-continuous]] and [[upper semicontinuous map|upper semicontinuous]], while the ceiling function is both [[left-continuous map|left-continuous]] and [[lower semicontinuous map|lower semicontinuous]].  They are [[step functions]] used to approximate definite [[integrals]] of [[continuous maps]] and otherwise to relate integrals and [[series]].  They provide convenient notation to express various notions of [[rounding]].  From the perspective of [[order theory]], the maps may be seen as the [[right adjoint]] and [[left adjoint]] (respectively) of the [[inclusion map]] from $\mathbb{Z}$ to $\mathbb{R}$.


## Definitions

Given a [[real number]] $x$, the __floor__ of $x$, denoted $\lfloor{x}\rfloor$ or $[x]$, is the largest integer $n$ such that $n \leq x$, and the __ceiling__ of $x$, denoted $\lceil{x}\rceil$, is the smallest integer $n$ such that $n \geq x$.

Typically the notation $\lfloor{x}\rfloor$ is used when both floor and ceiling appear, but $[x]$ is often easier when only the floor is considered.  Since
$$ \lceil{x}\rceil = -\lfloor{-x}\rfloor ,$$
this is not actually a restriction.

The floor of $x$ is also called the __integer part__ of $x$, and then one refers as well to the __fractional part__ of $x$, denoted $\{x\}$, defined by
$$ \{x\} = x - [x] .$$

One must of course prove that the floor of $x$ exists; this fails in [[constructive mathematics]], although the floor of $x$ exists for [[full set|almost all]] $x$, and all of these functions can still be defined as continuous maps between appropriate [[locales]].


## Properties

### As adjoint functors
  {#AsAdjointFunctors}

We discuss how the floor and celing functions are left and right [[adjoint functors]] to the inclusion of the [[integers]] into the [[real numbers]], if both are regarded as [[posets]], and hence as [[categories]].

+-- {: .num_example #PartiallyOrderedSetsAsSmallCategories}
###### Example
**([[preordered sets]] as [[thin categories]])**

Let $(S, \leq)$ be a [[preordered set]]. Then this induces a [[small category]] whose [[set]] of [[objects]] is $S$, and which has precisely one morphism $x \to y$ whenever $x \leq y$, and no such morphism otherwise:

\[
  \label{RelationsAsMorphismInPartiallyOrderedSet}
  x \overset{\exists !}{\to} y
  \phantom{AAA}
  \text{precisely if}
  \phantom{AAA}
  x \leq y
\]

Conversely, every [[small category]] with at most one morphism from any object to any other, called a _[[thin category]]_, induces on its set of objects the [[structure]] of a  [[partially ordered set]] via (eq:RelationsAsMorphismInPartiallyOrderedSet).

Here the [[axioms]] for [[preordered sets]] and for [[categories]] match as follows:

| |  $\phantom{A}$[[reflexive relation|reflexivity]]$\phantom{A}$ | $\phantom{A}$[[transitive relation|transitivity]]$\phantom{A}$ |
|----|-----|------|
| $\phantom{A}$[[partially ordered sets]]$\phantom{A}$ | $\phantom{A}$ $x \leq x$ $\phantom{A}$ | $\phantom{A}$ $(x \leq y \leq z) \Rightarrow (x \leq z)$ $\phantom{A}$ |
| $\phantom{A}$[[thin categories]]$\phantom{A}$ | $\phantom{A}$[[identity morphisms]]$\phantom{A}$ | $\phantom{A}$[[composition]]$\phantom{A}$ |
{: style='margin:auto}

=--

+-- {: .num_prop #FloorAndCeilingAsAdjointFunctors}
###### Proposition
**([[floor]] and [[ceiling]] as [[adjoint functors]])**

Consider the canonical inclusion

$$
  \mathbb{Z}_{\leq} 
    \overset{\phantom{AA}\iota \phantom{AA}}{\hookrightarrow} 
  \mathbb{R}_{\leq}
$$

of the [[integers]] into the [[real numbers]], both regarded as [[preorders]] in the standard way ("lower or equal"). Regarded as [[full subcategory]]-inclusion of the corresponding [[thin categories]], via Example \ref{PartiallyOrderedSetsAsSmallCategories}, this inclusion functor has both a left and right [[adjoint functor]]:

* the [[left adjoint]] to $\iota$ is the [[ceiling function]]

* the [[right adjoint]] to $\iota$ is the [[floor function]]

\[
  \label{AdjointTriple}
  \lceil(-)\rceil \;\;\dashv\;\; \iota \;\;\dashv\;\; \lfloor (-) \rfloor
  \,.
\]

Hence this induces an [[adjoint modality]], as discussed there. 

The [[adjunction unit]] and [[adjunction counit]] express that each real number is in between its floor and ceiling

$$
  \iota \lfloor x \rfloor \;\leq\; x \;\leq\; \iota \lceil x \rceil
$$

Hence the [[modal objects]] in both cases are the [[integers]] among the [[real numbers]], while every real number is ceiling-submodal and floor-supmodal.

=--

+-- {: .proof}
###### Proof

First of all, observe that we indeed have [[functors]]

$$
  \lfloor(-)\rfloor \;,\;
  \lceil(-)\rceil
  \;\;\colon\;
  \mathbb{R}
    \longrightarrow
  \mathbb{Z}
$$

since floor and ceiling preserve the ordering relation.

Now in view of the identification of [[preorders]] with [[thin categories]] in Example \ref{PartiallyOrderedSetsAsSmallCategories}, the hom-isomorphism defining [[adjoint functors]] of the form $\iota \dashv \lfloor(-)\rfloor$ says for all $n \in \mathbb{Z}$ and $x \in \mathbb{R}$, that we have

$$
  \underset{ \in \mathbb{Z}}{\underbrace{n \leq \lfloor x \rfloor}}
  \;\Leftrightarrow\;
  \underset{ \in \mathbb{R}}{\underbrace{n \leq x }}
  \,.
$$

This is clearly already the defining condition on the [[floor]] function $\lfloor x \rfloor$. 

Similarly, the  hom-isomorphism defining [[adjoint functors]] of the form $\lceil(-)\rceil \dashv \iota$ says that for all $n \in \mathbb{Z}$ and $x \in \mathbb{R}$, we have

$$
  \underset{ \in \mathbb{Z}}{\underbrace{\lceil x \rceil \leq n}}
  \;\Leftrightarrow\;
  \underset{ \in \mathbb{R}}{\underbrace{x \leq n }}
  \,.
$$

This is evidently already the defining condition on the [[floor]] function $\lfloor x \rfloor$. 


Notice that in both cases the condition of a _[[natural isomorphism]]_ in both variables, as required for an [[adjunction]], is automatically satisfied: For let $x \leq x'$ and $n' \leq n$, then naturality means, again in view of the identifications in Example \ref{PartiallyOrderedSetsAsSmallCategories}, that

$$
  \array{ 
    (n \leq \lfloor x \rfloor) &\Leftrightarrow& (n \leq x)
    \\
    \Downarrow && \Downarrow
    \\
    (n' \leq \lfloor x' \rfloor) &\Leftrightarrow& (n' \leq x')
    \\
    \\
    \in \mathbb{Z} && \in \mathbb{R}
  }
$$ 

where the logical implications are equivalently functions between [[sets]] that are either [[empty set|empty]] or [[singletons]]. But Functions between such sets are unique, when they exist.

=--


## References

Wikipedia summarizes the basic properties:

* English Wikipedia. Floor and ceiling functions. [Web](https://en.wikipedia.org/wiki/Floor_and_ceiling_functions).

Chapter 6 of these notes uses the floor and ceiling functions throughout to relate [[integrals]] and [[series]] when teaching [[infinitesimal calculus]]:

* Toby Bartels. One-variable Calculus. [Web](http://tobybartels.name/MATH-1600/2017FA/calcbook/).


[[!redirects floor]]
[[!redirects floors]]
[[!redirects floor operation]]
[[!redirects floor operator]]
[[!redirects floor function]]
[[!redirects floor functor]]
[[!redirects floor map]]
[[!redirects floor mapping]]

[[!redirects ceiling]]
[[!redirects ceilings]]
[[!redirects ceiling operation]]
[[!redirects ceiling operator]]
[[!redirects ceiling function]]
[[!redirects ceiling functor]]
[[!redirects ceiling map]]
[[!redirects ceiling mapping]]
