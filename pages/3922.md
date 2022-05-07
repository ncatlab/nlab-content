+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[number theory]], the concept of _algebraic integer_ is a generalization of that of [[integer]] to more general base-[[number fields]]. These algebraic integers form what is called the _[[ring of integers]]_ and so in order to distinguish that from the standard integers $\mathbb{Z}$ these are sometimes called _rational integers_, since they are the algebraic integers in the ring of [[rational numbers]].

## Definition


Colloquially, an **algebraic integer** is a solution to an equation 

$$x^n + a_1 x^{n-1} + \ldots + a_n = 0 \qquad (1)$$ 

where each $a_i$ is an [[integer]] (hence a [[root]] of the [[polynomial]] on the left). More precisely, an element $x$ belonging to an [[algebraic extension]] of the [[rational numbers]] $\mathbb{Q}$ is an (algebraic) integer, or more briefly is _integral_, if it satisfies an equation of the form (1). Equivalently, if $k$ is an algebraic extension of $\mathbb{Q}$ (e.g., if $k$ is a number field), an element $\alpha \in k$ is integral if the subring $\mathbb{Z}[\alpha] \subseteq k$ is finitely generated as a $\mathbb{Z}$-module. 

This notion may be relativized as follows: given an [[integral domain]] in its [[field of fractions]] $A \subseteq E$ and a finite [[field extension]] $E \subseteq F$, an element $\alpha \in F$ is **integral** over $A$ if $A[\alpha] \subseteq F$ is finitely generated as an $A$-module. 

If $\alpha, \beta$ are integral over $\mathbb{Z}$ (say), then $\alpha + \beta$ and $\alpha \cdot \beta$ are integral over $\mathbb{Z}$. For, if $\beta$ is integral over $\mathbb{Z}$, it is _a fortiori_ integral over $\mathbb{Z}[\alpha]$, hence 

$$(\mathbb{Z}[\alpha])[\beta] = \mathbb{Z}[\alpha, \beta]$$ 

is finitely generated over $\mathbb{Z}[\alpha]$ and therefore, since $\alpha$ is integral, also finitely generated over $\mathbb{Z}$. It follows that the submodules $\mathbb{Z}[\alpha + \beta]$ and $\mathbb{Z}[\alpha \cdot \beta]$ are therefore also finitely generated over $\mathbb{Z}$ (since $\mathbb{Z}$ is a [[Noetherian ring]]). Thus the integral elements form a [[ring]]. In particular, the integral elements in a [[number field]] $k$ form a ring often denoted by $\mathcal{O}_k$, usually called the **[[ring of integers]]** in $k$. This ring is a [[Dedekind domain]]. 

## Examples

* The algebraic integers in the [[rational numbers]] are the ordinary [[integers]].

* The algebraic integers in the [[Gaussian numbers]] are the [[Gaussian integers]].

* [[golden ratio]]

## Related concepts

* [[ring of integers]]

## References

Textbook account:

* {#Cassels86} [[J. W. S. Cassels]], Section 10.3 of: *Local Fields*, Cambridge University Press, 1986 (ISBN:9781139171885, [doi:10.1017/CBO9781139171885](https://doi.org/10.1017/CBO9781139171885)) 

Lecture notes:

* [[James Milne]], Chapter 2 of: *Algebraic number theory*, 2020 ([pdf](https://www.jmilne.org/math/CourseNotes/ANT.pdf))



[[!redirects algebraic integer]]
[[!redirects algebraic integers]]

[[!redirects rational integer]]
[[!redirects rational integers]]
