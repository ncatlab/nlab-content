
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The generalization of the notion of [[monomorphism]] from [[category theory]] to [[(∞,1)-category]] theory.

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

of [[∞-groupoid]]s is such that its image in the [[homotopy category of an (∞,1)-category|homtopy category]] exhibits $C(X,Y)$ as a [[direct sum]]mand of $C(X,Z)$

## Properties

Write $Sub(Z)$ for the collection of equivalence classes of monomorphisms to $Z$. 

$$
  Sub(Z) \simeq \tau_{\leq -1} C_{/Z}
  \,.
$$

This is [[poset|partially ordered]] under inclusion.

**Proposition** If $C$ is a [[presentable (∞,1)-category]], then $Sub(Z)$ is a small [[set]]. ([[Higher Topos Theory|HTT, prop 6.2.1.4]])


## References

The definition appears after example 5.5.6.13 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

with further discussion in section 6.2.


[[!redirects monomorphism in an (∞,1)-category]]
