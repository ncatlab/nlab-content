
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



# Subtraction
* table of contents
{: toc}

## Idea

The basic example of subtraction is, of course, the partial operation in the monoid of natural numbers or in the integers. It is often the first illustration of a non-associative operation met in abstract algebra. We think of subtraction as an operation $s:\mathbb{Z}\times \mathbb{Z}\to \mathbb{Z}$, where, of course, $s(m,n)=m-n$.

There are numerous related abstractions of this, relating to different aspects of the basic operation.



## Abstract






...


## Definition

1. (Universal Algebra) In the sense of Ursini  in the context of a varietal theory,  a _subtraction term_, $s$, is a binary term $s$ satisfying $s(x, x) = 0$ and $s(x, 0) = x$.
(see [[subtractive variety]]

1. In a [[co-Heyting algebra]], which are models of [[subtractive logic]], subtraction is the operation [[left adjoint]] to the [[join]] operator:
$$ (- \setminus y) \dashv (y \vee -)$$

1. A possibly-empty abelian group is a set $A$ with a binary operation $(-)-(-):A \to A$ satisfying the following axioms:
$$
  \forall a,b:A.a-a=b-b
$$
$$
  \forall a:A.(a-a)-((a-a)-a)=a
$$
$$
  \forall a,b,c:A.a-(b-c)=(a-((c-c)-c)-b
$$
$$
  \forall a,b:A.a-((b-b)-b)=b-((a-a)-a)
$$

## Properties

...


## Examples

* Subtraction in the [[commutative monoid]] of the [[natural numbers]] $\mathbb{N}$, is only partially defined. It is given by the [[monus]]/truncated subtraction operator:

$$\dot - \; : \mathbb{N} \times \mathbb{N} \rightarrow \mathbb{N}.$$

* Subtraction in the [[abelian group]] of the [[integers]] $\mathbb{Z}$, is well known to be an [[entire relation]] on the integers, 

$$- \; :\mathbb{Z} \times \mathbb{Z} \rightarrow \mathbb{Z}.$$

* Subtraction in a [[boolean ring]] is the [[symmetric difference]], and is the same as [[addition]] due to a boolean ring having a [[characteristic]] of 2. 

## References

...

## Related concepts

* [[difference]]


[[!redirects subtraction]]
