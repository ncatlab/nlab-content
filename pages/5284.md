
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Mapping space
+-- {: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _free loop space_ $\mathcal{L}X$ of a [[topological space]] $X$ (based or not) is the space of *all* [[loops]] in $X$. This is in contrast to the *based* [[loop space]] of a based space $X$ for which the loops are at the fixed [[base point]] $x_0\in X$.

(Regarded as a [[homotopy type]] the concept generalizes to other contexts of [[homotopy theory]], see at _[[free loop space object]]_ for more.)

The free loop space carries a canonical [[action]] ([[infinity-action]]) of the [[circle group]], and furthermore is a [[cyclotomic space]]. The [[homotopy quotient]] by that action $\mathcal{L}(X)/S^1$ (the "[[cyclic loop space]]") contains what is known as the _[[twisted loop space]]_ of $X$.


## Definition

### Explicit description

For $X$ a topological space, the free loop space $\mathcal{L}X$ is the topological space $Map(S^1,X)$ of [[continuous map]]s in [[compact-open topology]]. 

If we work in a category of [[pointed topological space|based spaces]], then still the topological space $Map(S^1,X)$ is in the non-based sense but has a distinguished point which is the constant map $t\mapsto x_0$ where $x_0$ is the base point of $X$.

### General abstract description

If $X$ is a [[topological space]], the **free loop space** $L X$ of $X$ is defined as the [[free loop space object]] of $X$ formed in the [[(∞,1)-category]] [[Top]].


### Cohomology of $\mathcal{L}X$ and Hochschild homology of $X$
  {#Cohomology}

Let $X$ be a [[simply connected topological space|simply connected]] [[topological space]]. 

The [[ordinary cohomology]] $H^\bullet$ of its free loop space is the [[Hochschild homology]] $HH_\bullet$ of its [[singular cohomology|singular chains]] $C^\bullet(X)$:

$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( C^\bullet(X) )
  \,.
$$

Moreover the $S^1$-equivariant cohomology of the loop space, hence the ordinary cohomology of the [[cyclic loop space]] $\mathcal{L}X/^h S^1$ is the [[cyclic homology]] $HC_\bullet$ of the singular chains:

$$
  H^\bullet(\mathcal{L}X/^h S^1)
    \simeq
  HC_\bullet( C^\bullet(X) )
$$

([Loday 11](#Loday11))

If the [[coefficients]] are [[rational numbers|rational]], and $X$ is of [[finite type]] then this may be computed by the _[[Sullivan model for free loop spaces]]_, see there the section on _[Relation to Hochschild homology](Sullivan+model+of+free+loop+space#RelationToHochschildHomology)_.


In the special case that the [[topological space]] $X$ carries the structure of a [[smooth manifold]], then the singular cochains on $X$ are equivalent to the [[dgc-algebra]] of [[differential forms]] (the [[de Rham algebra]]) and hence in this case the statement becomes that 


$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( \Omega^\bullet(X) )
  \,.
$$

$$
  H^\bullet(\mathcal{L}X/^h S^1)
    \simeq
  HC_\bullet( \Omega^\bullet(X) )
  \,.
$$

This is known as _[[Jones' theorem]]_ ([Jones 87](#Jones87))

An [[(infinity,1)-category theory|infinity-category theoretic]] proof of this fact is indicated at _[Hochschild cohomology -- Jones' theorem](Hochschild+cohomology#JonesTheorem)_.


### In rational homotopy theory

See at _[[Sullivan model of free loop space]]_.

## Related entries 

* [[loop space object]], [[free loop space object]],

  * [[delooping]]

  * [[loop space]], **free loop space**, [[derived loop space]]

  * [[Sullivan model of free loop space]]

* [[Hochschild homology]], [[cyclic homology]], [[dihedral homology]]

* [[smooth loop space]], [[free loop orbifold]], [[inertia orbifold]]

* [[caloron correspondence]]

* [[suspension object]]

  * [[suspension]]


## References

* [[Kathryn Hess]], _Free loop spaces in topology and physics_, [pdf](http://sma.epfl.ch/~hessbell/Pub_Edinburgh.pdf), slides from Meeting of Edinburgh Math. Soc. Glasgow, 14 Nov 2008

* {#Jones87} [[John D.S. Jones]], _Cyclic homology and equivariant homology_, Invent. Math. __87__, 403-423 (1987) ([pdf](https://math.berkeley.edu/~nadler/jones.pdf))

* {#Loday11} [[Jean-Louis Loday]], _Free loop space and homology_ ([arXiv:1110.0405](https://arxiv.org/abs/1110.0405))


* [[D. Ben-Zvi]], D. Nadler, _Loop spaces and connections_,
[arxiv/1002.3636](http://arxiv.org/abs/1002.3636)


[[!redirects free loop space]]
[[!redirects free loop spaces]]
