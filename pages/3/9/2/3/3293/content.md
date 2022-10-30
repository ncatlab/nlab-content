

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In analogy to how a [[smooth manifold]] is a [[manifold]] modeled on a [[Cartesian space]] $\mathbb{R}^n$ in [[CartSp]], a _Fr&#233;chet manifold_ is a [[manifold]] modeled on a [[Fréchet space]].

## Definition
It is possible to define, analog to the finite dimensional case, the notion of smooth functions of [[Fréchet spaces]], see there. Therefore, the usual definition of a manifold carries over word by word:

+-- {: .un_defn}
###### Definition
A **Fr&#233;chet manifold** is a Hausdorff topological space with an atlas of coordinate charts taking their value in Fr&#233;chet spaces, such that the coordinate transition functions are all smooth functions between Fr&#233;chet spaces.
=--

It is possible to generalize some concepts of differential geometry from the finite case to the Fr&#233;chet case, one has to be careful, however:

1. The dual of a Fr&#233;chet space that is not a [[Banach space]] is never a Fr&#233;chet space, therefore one cannot e.g. define both the tangent and the cotangent bundle as Fr&#233;chet manifolds. More serious is however

2. The existence and uniqueness theorems for ordinary differential equations fail in infinite dimensions, so that theorems depending on that from finite dimensional differential geometry cannot be transscribed to the infinite situation in general. It is possible to do this on a case by case basis however.

## Details

### Tangent Vectors and Differential Forms
There are several definitions of tangent vectors that are equivalent in the finite dimensional setting, but may be different in infinite dimensions. Tangent vectors can be defined to be derivations on germs of functions (algebraic definition), or as equivalence classes of smooth curves (kinematic definition). For the time being we settle with the kinematic definition:

+-- {: .un_defn}
###### Definition
**kinematic tangent vector**

The kinematic tangent vector space of a Fr&#233;chet manifold $M$ at a point $p$ consists of all pairs $(p, c'(0))$ where $c$ is a smooth curve
$$
c: \mathbb{R} \to M \; \text{with} \; c(0) = p
$$
As usual, the set of pairs $(p, c'(0)), p \in M$ forms a Fr&#233;chet manifold, the tangent bundle $TM$.
=--

The last sentence makes use of the notion of vector bundle, which can be defined exactly as in the finite dimensional setting:


+-- {: .un_defn}
###### Definition
**vector bundle**

A Fr&#233;chet manifold $V$ is a Fr&#233;chet vector bundle over $M$ with projection $\pi$, if for every point $p \in M$ there are charts of $M$ and $V$ such that $V$ is mapped locally to $U \subset F \times G$ for Fr&#233;chet spaces $F, G$, the projection $\pi$ corresponds to the projection of $U \times G$ to $U$, and the vector space structure on each fibre is that induces by the vector space structure on $G$.
=--

Since, as mentioned before, the dual space of a Fr&#233;chet space that is not a Banach space is itself not a Fr&#233;chet space, we cannot define the cotangent space canonically as the dual space of the tangent space. Instead we define it directly:


+-- {: .un_defn}
###### Definition
**differential form**

A differential form (a one form) $\alpha$ is a smooth map
$$
\alpha: TM \to \mathbb{R}
$$
where $TM$ is the tangent bundle.
=--

## Examples

Standard examples of Fr&#233;chet manifolds are smooth mapping spaces such as the

* [[smooth loop space]].


## References

For instance

* Kriegl and Michor, _A Convenient Setting of Global Analysis_ 

* V.I. Arnold, ; B.A. Khesin: _Topological methods in hydrodynamics._ (Springer 1998, [ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0902.76001&format=complete))

* Boris Khesin, Robert Wendt: _The geometry of infinite-dimensional groups._ (Springer 2009, [ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1153.22001&format=complete))

[[!redirects Frechet manifold]]