

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[Stokes theorem]] immediately implies that the [[integration of differential forms|integration]] of an [[exact differential form]] with [[compact support]]  vanishes. But in fact also the opposite is true: If the [[integration of differential forms|integration]] of a differential form with [[compact support]] of top degree vanishes, then it is exact (prop. \ref{KernelOfIntegrationOverSmoothManifold} below) .

## Statement

+-- {: .num_prop #KernelOfIntegrationOverSmoothManifold}
###### Proposition

Let $X$ be a [[smooth manifold]] of [[dimension]] $n \geq 1$. Write $\Omega^n_{cp}(X)$ for the [[vector space]] of [[differential n-forms]] with [[compact support]] and

$$
  \int_X \;\colon\; \Omega^n_{cp}(X) \longrightarrow \mathbb{R}
$$

for the [[linear map]] to the [[real numbers]] given by [[integration of differential forms]]. 

Then the [[kernel]] of this map is precisely the [[exact differential forms]]

$$
  ker\left(\int_X\right) = im(d)
  \,,
$$

hence the [[image]] of the [[de Rham differential]] $d \colon \Omega^{n-1}_{cp} \to \Omega^n_{cp}(X)$.

=--

(e.g. [Lafointaine 15, section 7.3, theorem 7.5](#Lafointaine15))


+-- {: .num_prop #Smooth0TypeIsSheavesOnSmoothMfd}
###### Proposition

At least when $X = \mathbb{R}^n$ is a [[Cartesian space]], then the statement of prop. \ref{KernelOfIntegrationOverSmoothManifold} also holds in smoothly [[indexed sets]] of smooth differential forms.

=--

(e.g. [Lafointaine 15, section 7.3, lemma 7.3](#Lafointaine15))

## Related concepts

* [[de Rham theorem]]

* [[Lie integration]] (proof of [this prop.](Lie+integration#LieIntegrationOfLinenLieAlgebra))


## References

* {#Lafointaine15} Jacques Lafontaine, section 7.3 of _An introduction to differential manifolds_, Springer 2015