
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

_Dolbeault cohomology_ of a [[complex manifold]] $X$ is the [[chain cohomology]] of the [[Dolbeault complex]] of $X$ (see there for more).


## Properties

### Dolbeault theorem

By the _[[Dolbeault theorem]]_ (see there) Dolbeault cohomology is equivalently the [[abelian sheaf cohomology]] $H^q(X;\Omega_X^p)$, of the [[abelian sheaf]] $\Omega_X^p$ which is the [[Dolbeault complex]] of [[holomorphic p-forms]].

### Hodge isomorphism

For $X$ a [[Hermitian manifold]] write $\mathcal{H}^{p,q}(X)$ for the space of $(p,q)$-[[harmonic differential forms]] and write $H^{p,q}$ for its [[Dolbeault cohomology]] in the bidegree.

+-- {: .num_prop}
###### Proposition

There is a canonical [[homomorphism]]

$$
  \mathcal{H}^{p,q}(X) \longrightarrow H^{p,q}(X)
  \,.
$$

If $X$ is [[compact topological space|compact]], then this is an [[isomorphism]], the _[[Hodge isomorphism]]_

=--

Also

$$
  \mathcal{H}^k(X,\mathbb{C}) \longrightarrow H^k_{dR}(X,\mathbb{C}) 
$$ 

is an isomorphism

(e.g. [Maddock,  prop. 4.2.7](#Maddock))

### Serre duality

[[Serre duality]]: On a [[Hermitian manifold]] $X$ of complex dimension $dim_{\mathbb{C}}(X) = n$ the [[Hodge star operator]] induces [[isomorphisms]]

$$
  \mathcal{H}^{p,q}(X)\simeq \mathcal{H}^{n-p, n-q}(X)
  \,.
$$

(e.g. [Maddock,  prop. 4.2.8](#Maddock))


### Hodge decomposition

If $X$ is a [[compact topological space|compact]] [[Kähler manifold]] then 

$$
  \mathcal{H}^k(X) \simeq \underset{p+q = k}{\oplus} \mathcal{H}^{p,q}(X)
$$

(e.g. [Maddock,  prop. 4.2.9](#Maddock))

This is called the _[[Hodge decomposition]]_.

### Hodge symmetry

Over [[complex manifolds]] $X$, _[[Hodge symmetry]]_ is the property that the [[Dolbeault cohomology]] groups $H^{p,q}(X)$ are taken into each other under [[complex conjugation]] followed by switching the bidegree:

$$
  H^{p,q}(X) \simeq \overline{H^{q,p}(X)}
  \,.
$$

In particular this means that the [[dimension]] of the cohomology groups in degree $(p,q)$ coincides with that in bidegree $(q,p)$.



### Dolbeault resolution

Given any [[holomorphic vector bundle]] $E$, one can form the Dolbeault resolution $E \otimes \Omega^{0,q}$, where $\Omega^{0,q}$ is the sheaf of $C^\infty$ $(0,q)$-forms. This is an acyclic resolution of $E$ and hence computes its [[sheaf cohomology]].

(...)

### Double complex and Fr&#246;licher spectral sequence

The Dolbeault complexes naturall fit into a [[double complex]]

$$
  \array{
    \Omega^{p,0} &\stackrel{\bar \partial}{\to}& \Omega^{p-1,1} &\stackrel{\bar \partial}{\to}& \cdots
    \\
    \downarrow^{\mathrlap{\partial }}
    &&
    \downarrow^{\mathrlap{\partial }}
    \\
    \Omega^{p+1,0} &\stackrel{\bar \partial}{\to}& \Omega^{p,1} &\stackrel{\bar \partial}{\to}& \cdots
    \\
    \downarrow^{\mathrlap{\partial }}
    &&
    \downarrow^{\mathrlap{\partial }}
    \\
    \vdots && \vdots
  }
  \,.
$$

The corresponding [[spectral sequence of a double complex]] is called the _[[Frölicher spectral sequence]]_. On a [[Kähler manifold]] it exhibits the [[Hodge filtration]].

## Related concepts

* [[Hodge number]]

* [[Kodaira vanishing theorem]]

* [[de Rham cohomology]]

* [[Bott-Chern cohomology]]

## References

* {#Maddock} Zachary Maddock, _Dolbeault cohomology_ ([pdf](http://www.math.columbia.edu/~maddockz/notes/dolbeault.pdf))


[[!redirects Dolbeault resolution]]
