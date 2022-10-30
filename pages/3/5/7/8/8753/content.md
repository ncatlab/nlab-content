[[!redirects simplicial object in an (∞,1)-category]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\mathcal{C}$ an [[(∞,1)-category]], a [[simplicial object]] in $\mathcal{C}$ is an [[(∞,1)-functor]]

$$
  X \colon \Delta^{op} \to \mathcal{C}
$$

from the [[opposite category]] of the [[simplex category]] into $\mathcal{C}$.

The $(\infty,1)$-category of simplicial objects in $\mathcal{C}$ and morphisms between them is the [[(∞,1)-category of (∞,1)-functors]]

$$
  \mathcal{C}^{\Delta^{op}}
  = 
  Func_\infty(\Delta^{op}, \mathcal{C})
  \,.
$$

## Properties

### Cohesion

If $\mathcal{C} = \mathbf{H}$ is an [[(∞,1)-topos]] then $\mathcal{C}^{\Delta^{op}}$ is a [[cohesive (∞,1)-topos]] over $\mathbf{H}$. For more see at _[cohesive (∞,1)-topos - Examples - Simplicial objects](cohesive+%28infinity%2C1%29-topos#SimplicialObjctsInACohesiveTopos)_.

### Internal language

If $\mathcal{C}$ is a [[locally cartesian closed (∞,1)-category]] whose [[internal language]] is [[homotopy type theory]], then the internal language of $\mathcal{C}^{\Delta^{op}}$ is that homotopy type theory equipped with the axioms for a [[linear interval]] object. (...)

## Examples

### Internal category objects

* A [[pre-category object in an (∞,1)-category]] $\mathcal{C}$ is a simplicial object which satisfies the [[Segal conditions]];

* a [[category object in an (∞,1)-category]] is a pre-category object which also satisfies the [[univalence axiom]];

* a [[groupoid object in an (∞,1)-category]] is a category object all of whose [[morphisms]] are [[equivalences]] under composition.


[[!redirects simplicial objects in an (∞,1)-category]]
[[!redirects simplicial objects in an (infinity,1)-category]]
