
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

+-- {: .num_defn}
###### Definition

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

=--

For instance ([Lurie, def. 6.1.2.2](#Lurie)).

## Properties

### General
 {#General}

+-- {: .num_defn}
###### Definition

Let $\mathcal{C} \in QCat \hookrightarrow sSet$ be an [[(∞,1)-category]] incarnated as a [[quasi-category]], and let $X \colon \Delta^{op} \to \mathcal{C}$ be a simplicial object. Then for $K \in sSet$ any [[simplicial set]], write

$$
  X[K] \colon \Delta_{/K}^{op} \to \Delta^{op} \stackrel{X}{\to} \mathcal{C}
  \,,
$$

where the first homomorphism is the projection from the [[category of elements]] of $K$.

=--

+-- {: .num_prop #SlicingOverPoweringOfSimplicialObjects}
###### Proposition

Let $X \colon \Delta^{op} \to \mathcal{C}$ be a simplicial object.

If $K \to K'$ is a morphism in [[sSet]] which is a [[weak homotopy equivalence]] and a [[bijection]] on [[vertices]], then the induced morphism on [[slice-(∞,1)-categories]]

$$
  \mathcal{C}_{/X[K]}
  \to 
  \mathcal{C}_{/X[K']}
$$

is an [[equivalence of (∞,1)-categories]] (a [[weak equivalence]] in the [[model structure for quasi-categories]]).

=--

This is ([Lurie, prop. 6.1.2.6](#Lurie)).

### Cohesion

If $\mathcal{C} = \mathbf{H}$ is an [[(∞,1)-topos]] then $\mathcal{C}^{\Delta^{op}}$ is a [[cohesive (∞,1)-topos]] over $\mathbf{H}$. For more see at _[cohesive (∞,1)-topos - Examples - Simplicial objects](cohesive+%28infinity%2C1%29-topos#SimplicialObjctsInACohesiveTopos)_.

### Internal language

If $\mathcal{C}$ is a [[locally cartesian closed (∞,1)-category]] whose [[internal language]] is [[homotopy type theory]], then the internal language of $\mathcal{C}^{\Delta^{op}}$ is that homotopy type theory equipped with the axioms for a [[linear interval]] object. (...)

## Examples

### Internal category objects

* A [[pre-category object in an (∞,1)-category]] $\mathcal{C}$ is a simplicial object which satisfies the [[Segal conditions]];

* a [[category object in an (∞,1)-category]] is a pre-category object which also satisfies the [[univalence axiom]];

* a [[groupoid object in an (∞,1)-category]] is a category object all of whose [[morphisms]] are [[equivalences]] under composition.


## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

* [[semi-simplicial object]]

  * [[semisimplicial set]]

* [[simplicial homotopy theory]]

## Reference

Section 6.1.2 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}


[[!redirects simplicial objects in an (∞,1)-category]]
[[!redirects simplicial objects in an (infinity,1)-category]]

[[!redirects simplicial object in an (∞,1)-category]]
