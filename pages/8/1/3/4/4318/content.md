
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
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

_Dolbeault cohomology_ of a [[complex manifold]] $X$ is the [[chain cohomology]] of the [[Dolbeault complex]] of $X$ (see there for more).

By the [[Dolbeault theorem]] this is equivalently the [[abelian sheaf cohomology]] $H^q(X;\Omega_X^p)$, of the [[abelian sheaf]] $\Omega_X^p$ is [[Dolbeault complex]] of [[holomorphic p-forms]].

## Properties

### Hodge isomorphism

For $X$ a [[hermitian manifold]] write $\mathcal{H}^{p,q}(X)$ for the space of $(p,q)$-[[harmonic differential forms]]. 

There is a canonical [[homomorphism]]

$$
  \mathcal{H}^{p,q}(X) \longrightarrow H^{p,q}(X)
  \,.
$$

If $X$ is [[compact topological space|compact]], then this is an [[isomorphism]].

Also

$$
  \mathcal{H}^k(X,\mathbb{C}) \longrightarrow H^k_{dR}(X,\mathbb{C}) 
$$ 

is an isomorphism

(e.g. [Maddock,  prop. 4.2.7](#Maddock))

### Serre duality

[[Serre duality]]: On a [[Hermitian manifold]] $X$ of complex dimension $dim_{\mathbb{C}}(X) = n$ the [[Hodge star operator]] induces [[isomorphisms]]

$$
  \mathcal{H}^{p,q}(X)\simeq \mathcal{H}^{n-p, n-q}
  \,.
$$

(e.g. [Maddock,  prop. 4.2.8](#Maddock))


### Properties of Hodge numbers

If $X$ is a [[compact topological space|compact]] [[Kähler manifold]] then 

$$
  \mathcal{H}^k(X) \simeq \underset{p+q = k}{\oplus} \mathcal{H}^{p,q}(X)
$$

(e.g. [Maddock,  prop. 4.2.9](#Maddock))


### Dolbeault resolution

Given any [[holomorphic vector bundle]] $E$, one can form the Dolbeault resolution $E \otimes \Omega^{0,q}$, where $\Omega^{0,q}$ is the sheaf of $C^\infty$ $(0,q)$-forms. This is an acyclic resolution of $E$ and hence computes its [[sheaf cohomology]].

## Related concepts

* [[Hodge number]]

* [[Kodaira vanishing theorem]]


## References

* {#Maddock} Zachary Maddock, _Dolbeault cohomology_ ([pdf](http://www.math.columbia.edu/~maddockz/notes/dolbeault.pdf))


[[!redirects Dolbeault resolution]]
