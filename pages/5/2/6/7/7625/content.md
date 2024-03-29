
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the [[AQFT]] formalization of [[quantum field theory]] a [[local net of observables]] assigns to each region of [[spacetime]] the [[algebra]] of [[observables]] localized in that region. But in typical constructions of [[quantum field theories]] this algebra is obtained from an algebra of quantum fields that are _not_ all observable by quotienting out a [[gauge group]] [[action]]. A **field net** corresponding to a [[local net of observables]] is a [[net of C-star-systems]] which formalizes this idea, notably so that the quotient by the group action reproduces the given local net of observables.

## Reconstruction

Given a [[local net of observables]] $\mathcal{A}$ the corresponding field algebra, according to [Doplicher-Roberts](#DoplicherRoberts) the the following.

+-- {: .num_defn}
###### Definition

The _field algebra_ $\mathcal{F}_0$ corresponding to $\mathcal{A}$ is the collection of [[equivalence classes]] of triples $(A, \rho, \psi)$ consisting

* $A \in \mathcal{A}$ an [[observable]];

* $\rho : \mathcal{A} \to \mathcal{A}$ a [[superselection sector]], hence an object of the [[DHR category]] $\Delta_{DHR}$ of $\mathcal{A}$;

* $\psi \in E(\rho)$ a [[vector]] in the space [[Hilbert space]] assigned by the [[fiber functor]] of the [[Doplicher-Roberts reconstruction theorem]] to superselection sector $\rho$;

where the [[equivalence relation]] identifies for $T : \rho \to \rho'$ an intertwiner two such triples by the rule

$$
  (A T, \rho, \psi)
  \sim
  (A, \rho', E(T)\psi)
  \,.
$$

This becomes an [[associative algebra|algebra]] by defining the product on representatives as

$$
  (A_1, \rho_1, \psi_1) \cdot (A_2, \rho_2, \psi_2)
  =
  (A_1 \rho_1(A_2), \rho_1 \otimes \rho_2, \psi_1 \otimes \psi_2)
  \,.
$$

With a bit more work a [[star algebra]] structure is defined.

This becomes a net by assigning to an open $\mathcal{O}$ the subalgebra of such triples with $A \in \mathcal{A}(\mathcal{O})$ and $\rho$ localized in $\mathcal{O}$.

Finally, one can construct a representation of this in [[bounded operators]], and taking the [[norm]] closure there gives the field net $\mathcal{F}$.

=--


## References

The construction of a field net for every local net of observables in [[DHR superselection theory]] is due to 

* [[Sergio Doplicher]], [[John Roberts]], _Why there is a field algebra with a compact gauge group describing the superselection structure in particle physics_, Comm. Math. Phys. 131 (1) (1990)
 {#DoplicherRoberts}

A detailed review is in sections 9 and 10 of 

* [[Hans Halvorson]], _Algebraic quantum field theory_ ([pdf](http://www.princeton.edu/~hhalvors/aqft.pdf))

A purely [[category theory|category theoretic]] construction of the field-net analog of the [[DHR category]] is given in 

* [[Michael Müger]], _Galois Theory for Braided Tensor Categories
and the Modular Closure_, Adv. Math. 150, 151-201 (2000) ([arXiv:math.CT/9812040](http://arxiv.org/abs/math.CT/9812040))

[[!redirects field nets]]