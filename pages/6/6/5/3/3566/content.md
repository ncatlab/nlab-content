
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The generalization of the notion of [[monomorphism]] from [[category theory]] to [[(∞,1)-category]] theory.

The dual concept is that of an [[epimorphism in an (∞,1)-category]].

There is also the concept [[regular monomorphism in an (∞,1)-category]], but beware that this need not be a special case of the definition given here.

## Definition

For $C$ an [[(∞,1)-category]], a [[morphism]] $f : Y \to Z$ is a **monomorphism** if regarded as an object in the [[over quasi-category|(∞,1)-overcategory]] $X_{/Z}$ it is a [[n-truncated object in an (∞,1)-category|(-1)-truncated object]].

Equivalently this means that the projection

$$
  C_{/f} \to C_{/D}
$$

is a [[full and faithful (∞,1)-functor]].

Equivalently this means that for every object $X \in C$ the induced morphism

$$
  C(X,f) : C(X,Y) \to C(X,Z)
$$

of [[∞-groupoid]]s is such that its image in the [[homotopy category of an (∞,1)-category|homotopy category]] exhibits $C(X,Y)$ as a direct summand in a  [[coproduct]] decomposition of $C(X,Z)$.

So if $C(X,Y) = \coprod_i C(X,Y)_{i \in \pi_0(C(X,Y))}$ and $C(X,Z) = \coprod_{j \in \pi_0((C(X,Z))} C(X,Z)_j$ is the decomposition into connected components, then there is an injective function

$$
  j : \pi_0(C(X,Y)) \to \pi_0(C(X,Z))
$$

such that $C(X,f)$ is given by component maps $C(X,Y)_i \to C(X,Z)_{j(i)}$ which are each an equivalence.

## Properties

Write $Sub(Z)$ for the collection of equivalence classes of monomorphisms to $Z$. 

$$
  Sub(Z) \simeq \tau_{\leq -1} C_{/Z}
  \,.
$$

This is [[poset|partially ordered]] under inclusion.

**Proposition** If $C$ is a [[presentable (∞,1)-category]], then $Sub(Z)$ is a small [[set]]. ([[Higher Topos Theory|HTT, prop 6.2.1.4]])

## Related pages

The notion of monomorphism in an $(\infty,1)$-category can also be characterized in its underlying homotopy [[derivator]]; see [[monomorphism in a derivator]].

## References

The definition appears after example 5.5.6.13 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

with further discussion in section 6.2.


[[!redirects monomorphism in an (∞,1)-category]]
[[!redirects monomorphisms in an (∞,1)-category]]
[[!redirects monomorphisms in an (infinity,1)-category]]
