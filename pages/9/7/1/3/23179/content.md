

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--

#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In generalization of how a [[smooth ∞-groupoid]] is an [[∞-groupoid]] equipped with [[generalized smooth structure]] modeled on [[Cartesian spaces]] with [[smooth functions]] between them (hence: on [[smooth manifolds]]), a singular-smooth $\infty$-groupoid carries geometric structure which, in addition to being smooth almost everywhere, may have [[orbi-singularities]], in that it is locally modeled on [[Cartesian space]] regarded possibly as $G$-[[fixed loci]] for any [[finite group]] $G$. 

## Definition

Write 

* $CartesionSpaces \xhookrightarrow{\;} SmthMfd$ for the [[category]] of [[Cartesian spaces]] with [[smooth functions]] between them, regarded as a [[site]] via the [[coverage]] of [[differentiably good open covers]],

* $Singularities \xhookrightarrow{\;} Grpd_\infty$ for the [[(2,1)-category]] of [[groupoids]] which are [[deloopings]] of [[finite groups]], regarded as an [[(infinity,1)-site|$\infty$-site]] via the trivial topology.

Then singular-smooth $\infty$-groupoids are the [[objects]] in the [[hypercomplete (infinity,1)-topos|hypercomplete]] [[(infinity,1)-sheaf|$\infty$-sheaf]] [[(infinity,1)-topos|$\infty$-topos]] over the [[product category|product]] of these sites:

$$
  SingSmoothGrpd_\infty
  \;\coloneqq\;
  Sh_\infty
  \big(
    CartesianSpaces \times Singularities
  \big)
  \,.
$$

## Properties

In generalization of how [[smooth infinity-groupoids|smooth $\infty$-groupoids]] form a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]] over [[Infinity-Grpd|$Grpd_\infty$]],  so singular-smooth $\infty$-groupoids form a [[singular-cohesive (infinity,1)-topos|singular-cohesive $\infty$-topos]].

Where the [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]] [[smooth infinity-groupoid|$SmthGrpd_\infty$]] is the natural home of [[smooth manifolds]] and [[diffeological spaces]], reflecting their [[differential cohomology]], so $SingSmoothGrpd_\infty$ is the natural home of [[orbifolds]] reflecting their proper [[orbifold cohomology]] ([SaSc 2020](#SaSc20)).

## Related concepts

* [[orbifold]], [[orbifold cohomology]]

* [[singular-cohesive (infinity)-topos|singular-smooth $\infty$-topos]]

* [[cohesion of global- over G-equivariant homotopy theory]]


## References

* {#SaSc20} [[Hisham Sati]], [[Urs Schreiber]], Ex. 3.56 in: _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))


[[!redirects singular-smooth ∞-groupoids]]

[[!redirects singular-smooth infinity-groupoid]]
[[!redirects singular-smooth infinity-groupoids]]
