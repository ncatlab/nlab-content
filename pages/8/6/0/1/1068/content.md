
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Category with translation#
* table of contents
{:toc}

## Idea

A _category with translations_ is a [[category]] equipped with a rudimentary notion of [[suspension objects]]. Categories with translation underlie [[triangulated categories]] where the "translation" becomes a genuine suspension as in [[homotopy fiber sequences]].

## Definition

+-- {: .num_defn }
###### Definition

A **category with translation** is a [[category]] $C$ equipped with an [[equivalence|auto-equivalence]] [[functor]]

$$
  T : C \to C
$$

called the **shift functor** or **translation functor** or **suspension functor**.

=--

+-- {: .num_remark }
###### Remark

Frequently $C$ is an [[additive category]] in which case $T$ is also required to be an _[[additive functor]].

=--

+-- {: .num_defn }
###### Definition


A **morphism of categories with translation** $F:(C,T)\to (C',T')$ is a [[functor]] $F:C\to C'$ equipped with an [[isomorphism]] $F\circ T\cong T'\circ F$:

$$
  \array{
    C &\stackrel{F}{\to}& C'
    \\
    \downarrow^T &\swArrow^{\simeq}& \downarrow^{T'}
    \\
    C &\stackrel{F}{\to}& C'
  }
  \,.
$$

 If $C$,$C'$ are [[additive category|additive]] and $F$ is additive $F$ is a "morphism of additive categories with translation". 

=--

+-- {: .num_defn }
###### Definition


In any additive category with translation a **triangle** is a sequence of morphisms of the form
$$
  a\stackrel{f}\to b\stackrel{g}\to c\stackrel{h}\to T a
 \,.
$$

=--

+-- {: .num_remark }
###### Remark


In some variants the translation endofunctor $T$ is not required to be an [[equivalence]]. This is the case for instance for the 
[[suspended category|presuspended categories]] of Keller and Vossieck. 

=--

## Examples

* The "translation" functor models the shift operation in a [[triangulated category]], where one chooses a distinguished collection of triangles satisfying some axioms. 

## Related concepts

* [[suspension object]]

* [[triangulated category]]

  * [[exact triangle]], [[distinguished triangle]]

[[!redirects categories with translation]]
[[!redirects category with translations]]
[[!redirects categories with translations]]

[[!redirects shift functor]]
[[!redirects shift functors]]
