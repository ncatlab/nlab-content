
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A **Lie group** is a [[group]] with [[smooth structure]].


## Definition

+-- {: .un_def}
###### Definition

A **Lie group** is a smooth [[manifold]] whose underlying set of points is equipped with a structure of a [[group]] and the multiplication and inverse maps for the group are smooth maps.  

In other words, it is a [[group object]] [[internalization|internal to]] [[Diff]].

=--

Usually the manifold is assumed to be over the [[real numbers]] or the [[complex numbers]] and of finite [[dimension]] (f.d.), but extensions to some other ground fields and infinite-dimensional setting are also relevant. 

A real Lie group is _compact_ (or _connected_, _simply connected_, etc) if its underlying space is [[compact space|compact]] (or [[connected space|connected]], [[simply connected space|simply connected]], etc). 

Every connected f.d. real Lie group is homeomorphic to a [[product]] of a compact Lie group and an Euclidean space. Every abelian connected compact f.d. real Lie group is a [[torus]] (a product of circles $T^n = S^1\times S^1 \times \ldots \times S^1$).

There is an [[infinitesimal space|infinitesimal]] version of a Lie group, a so-called [[local Lie group]], where the multiplication and the inverse are only partially defined, namely if the arguments of these operations are in a sufficiently small neighborhood of identity. There is a natural equivalence of local Lie groups by means of agreeing (topologically and algebraically) on a smaller neighborhood of the identity. The category of local Lie groups is equivalent to the category of connected and simply connected Lie groups. 

The first order [[infinitesimal object|infinitesimal]] approximation to a Lie group is its [[Lie algebra]].


## Examples {#Examples}

The [[real line]] $\mathbb{R}$ with its standard [[smooth structure]] and the group operation being addition is a Lie group. So is every [[Cartesian space]] $\mathbb{R}^n$ with the componentwise addition of real numbers.

The [[quotient]] of $\mathbb{R}$ by the subgroup of [[integer]]s $\mathbb{Z} \hookrightarrow \mathbb{R}$ is the [[circle group]] $S^1 = \mathbb{R}/\mathbb{Z}$. The quotient $\mathbb{R}^n/\mathbb{Z}^n$ is the $n$-[[dimension|dimensional]] [[torus]].

The [[classical Lie group]]s include

* the [[general linear group]] $GL(n)$

* the [[orthogonal group]] $O(n)$ and [[special orthogonal group]] $SO(n)$;

* the [[unitary group]] $U(n)$ and [[special unitary group]] $SU(n)$;

* the [[symplectic group]] $Sp(2n)$.

The [[exceptional Lie group]]s incude

* ... [[E8]]





## Properties

### Lie's three theorems

[[Sophus Lie]] has proved several theorems -- [[Lie's three theorems]] -- on the relationship between [[Lie algebra]]s and Lie groups. What is called [[Lie's third theorem]] is about the [[equivalence of categories]] of f.d. real Lie algebras and local Lie groups. [[Élie Cartan]] has extended this to a global integrability theorem called the Cartan-Lie theorem, nowadays after Serre also called Lie's third theorem.


### Classification

+-- {: .un_prop}
###### Prposition

Every connected finite-dimensional real Lie group is [[homeomorphism|homeomorphic]] to a [[product]] of a compact Lie group and a [[Cartesian space|Euclidean space]]. Every abelian connected compact f.d. real Lie group is a [[torus]] (a product of circles $T^n = S^1\times S^1 \times \ldots \times S^1$).

=--

The [[simple Lie group]]s have a classification into infinite series of 

* [[classical Lie group]]s

and a finite snumber o

* [[exceptional Lie group]]s


### Different Lie group structures on a group

For $G$ a bare [[group]] (without smooth structure) there may be more than one way to equip it with the [[stuff, structure, property|structure]] of a Lie group.

+-- {: .un_example}
###### Example

As bare [[abelian group]]s, the  [[Cartesian space]]s $\mathbb{R}^n$ are, for all $n$, [[vector space]]s over the [[rational number]]s $\mathbb{Q}$ whose [[dimension]] is the [[cardinality]] of the [[continuum]], $2^{\aleph_0}$.

Therefore these are all [[isomorphic]] as bare group. But equipped with their canonical Lie group structure (as in the [Examples](#Examples)) they are of course not isomorphic.

=--

### Different topologies on a Lie group

* Linus Kramer, _The topology of a simple Lie group is essentially unique_, ([arXiv](http://arxiv.org/abs/1009.5457))

> Abstract: We study locally compact group topologies on simple Lie groups. We show that the Lie group topology on such a group $S$ is very rigid: every 'abstract' isomorphism between $S$ and a locally compact and $\sigma$-compact group $\Gamma$ is automatically a homeomorphism, provided that $S$ is absolutely simple. If $S$ is complex, then non-continuous field automorphisms of the complex numbers have to be considered, but that is all. 







## Applications

### In differential geometry

A central concept of [[differential geometry]] is that of a $G$-[[principal bundle]] $P \to X$ over a [[smooth manifold]] $X$ for $G$ a Lie group.

### In gauge theory

In the [[physics]] of [[gauge field]]s -- [[gauge theory]] -- Lie groups appear as local [[gauge group]]s parameterizing [[gauge transformation]]s: notably the [[Yang-Mills field]] is modeled by a $G$-[[principal bundle]] with [[connection on a bundle|connection]] for some Lie group $G$. For models that describe experimental observations the group $G$ in question is a quotient of a product of [[special unitary group]]s and the [[circle group]]. For details see [[standard model of particle physics]]


## In higher category theory

The notion of [[group]] generalizes in [[higher category theory]] to that of [[2-group]], ... [[∞-group]].

Accordingly, so does the notion of Lie group generalize to [[Lie 2-group]], ... [[∞-Lie group]]. For details see [[∞-Lie groupoid]].



[[!redirects Lie groups]]