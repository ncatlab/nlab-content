
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _inverter_ is a particular kind of [[2-limit]] in a [[2-category]], which universally renders a [[2-morphism]] invertible.

## Definition

Let $f,g\colon A\rightrightarrows B$ be a pair of parallel 1-morphisms in a 2-category and $\alpha\colon f\to g$ a 2-morphism.  The **inverter** of $\alpha$ is a universal object $V$ equipped with a morphism $v\colon V\to A$ such that $\alpha v$ is invertible.

More precisely, universality means that for any object $X$, the induced functor
$$Hom(X,V) \to Hom(X,A)$$
is fully faithful, and its [[replete image]] consists precisely of those morphisms $u\colon X\to A$ such that $\alpha u$ is invertible.  If the above functor is additionally an *isomorphism* of categories onto the exact subcategory of such $u$, then we say that $V\xrightarrow{v} A$ is a **strict inverter**.

Inverters and strict inverters can be described as a certain sort of [[weighted limit|weighted]] 2-limit, where the diagram shape is the [[walking structure|walking]] 2-morphism

$T=$ [[!include 2-morphism - SVG]]

and the weight $T\to Cat$ is the diagram
$$\array{ & \to \\ 1 & \Downarrow & Inv\\ & \to } $$
where $1$ is the [[terminal category]] and $Inv$ is the walking [[isomorphism]].  Since $Inv$ is equivalent to $1$, this weight is equivalent to the terminal weight, and thus an inverter (but not a strict inverter) can also be defined simply as a [[conical limit|conical]] 2-limit over a diagram of shape $T$.

## Properties

* The above description makes it clear that any inverter is in particular a [[fully faithful morphism]].

* Any strict inverter is, in particular, an inverter.  (This is not true for all strict 2-limits.)

* Inverters can be constructed in a straightforward way from [[inserters]] and [[equifiers]]: first we insert a 2-morphism $\beta$ going in the opposite direction from $\alpha$, then we equify $\beta\alpha$ and $\alpha\beta$ with identities.  In particular, it follows that strict inverters are [[PIE-limits]].

## References

In 

* [[Peter Johnstone]], _[[Elephant]]_

inverters appear in B1.1.4. The inverter of a transformation between [[geometric morphism]]s of [[topos]]es is constructed in the proof of corollary 4.1.7 in section B4.1. Coinverters are discussed in section B4.5 there.

[[!redirects inverters]]
[[!redirects strict inverter]]
[[!redirects strict inverters]]
