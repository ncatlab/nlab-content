
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Definition

A __wide pullback__ in a [[category]] $\mathcal{C}$ is a [[product]] (of arbitrary [[cardinality]]) in a [[over category|slice category]] $\mathcal{C} \downarrow C$.  In terms of $\mathcal{C}$, this can be expressed as a [[limit]] over a category obtained from a [[discrete category]] by adjoining a [[terminal object]].

Yet more explicitly, the wide pullback of a family of coterminal morphisms $f_i\colon A_i \to C$ is an object $P$ equipped with projection $p_i\colon P\to A_i$ such that $f_i p_i$ is independent of $i$, and which is universal with this property.

Binary wide pullbacks are the same as ordinary [[pullbacks]], a.k.a. fiber products.

Of course, a **wide pushout** is a wide pullback in the opposite category.

## Properties

* A category has wide pullbacks (of all [[small category|small]] cardinalities) if and only if it has (binary) [[pullbacks]] and [[cofiltered limits]].

* The [[saturated class of limits|saturation]] of the class of wide pullbacks is the class of limits over categories $C$ whose [[fundamental groupoid]] $\Pi_1(C)$ is trivial.

On the other hand, together with a terminal object, wide pullbacks generate all limits:

+-- {: .num_prop #WidePbToComplete}
###### Proposition 
A [[category]] $C$ with all [[wide pullbacks]] and a [[terminal object]] $1$ is [[complete category|complete]]. If $C$ is complete and $F\colon C \to D$ preserves wide pullbacks and the terminal object, then it preserves all limits. 
=-- 

+-- {: .proof}
######Proof 
To build up arbitrary products $\prod_{i \in I} c_i$ in $C$, take the wide pullback of the family $c_i \to 1$. Then to build equalizers of diagrams $f, g\colon c \rightrightarrows d$, construct the pullback of the diagram 
$$\array{
 & & d \\
 & & \downarrow \delta \\
c & \underset{\langle f, g \rangle}{\to} & d \times d
}$$ 
From products and equalizers, we can get arbitrary limits. 

=--


## Related concepts

* [[connected limit]] 

[[!include notions of pullback -- contents]]


## References

* [[Robert Paré]], *Simply connected limits*.  Can. J. Math., Vol. XLH, No. 4, 1990, pp. 731-746, [CMS](http://math.ca/10.4153/CJM-1990-038-6)

[[!redirects wide pullback]]
[[!redirects wide pullbacks]]
[[!redirects wide pushout]]
[[!redirects wide pushouts]]
