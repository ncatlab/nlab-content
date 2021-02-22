

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _Heisenberg group_ (or _Weyl-Heisenberg group_) is a [[Lie group]] [[Lie integration|integrating]] a _[[Heisenberg Lie algebra]]_. 

There are several such, and so the conventions in the literature vary slightly as to which one to pick by default. 

The Heisenberg group historically originates in and still has its strongest ties to [[quantum physics]]: there it is a group of [[unitary operators]] acting on the [[space of states]] induced from those [[observables]] on a linear [[phase space]] -- a [[symplectic vector space]] -- which are given by linear or by constant functions.
So any Heisenberg group is a subgroup of a group of observables in certain simple examples of quantum mechanical systems.


## Definition

A **Heisenberg group** is a [[Lie group]] whose [[Lie algebra]] is a [[Heisenberg Lie algebra]].

We spell out some special cases in detail.

### $H_3$ in components

The simplest non-trivial example of a Heisenberg group is the unique [[simply connected topological space|simply connected]] Lie integration of the [[Heisenberg Lie algebra]] $Heis(\mathbb{R}^2, \omega = d p \wedge dq)$ on the the canonical 2-dimensional [[symplectic vector space]] $\mathbb{R}^2$ with canonical [[coordinates]] $(p,q)$. 

This Heisenberg Lie algebra is [[generators and relations|generated]] from 3 elements, here to be denoted $\mathbf{p}, \mathbf{q},\mathbf{e}$, subject to the single non-trivial [[Lie bracket]]

$$
  [\mathbf{q}, \mathbf{p}] = \mathbf{e}
  \,.
$$

The corresponding Heisenberg group is usually denoted $H_3$:

$$
  H_3 \coloneqq \exp Heis(\mathbb{R}^2 , d p \wedge d q)
  \,.
$$

The underlying [[smooth manifold]] of this [[Lie group]] is the [[Cartesian space]] $\mathbb{R}^3$. A general element may be written as

$$
  g_{a,b,c}
   = 
  \exp(a \mathbf{q} + b \mathbf{p} )\exp(c \mathbf{e})
$$

with $a, b , c\in \mathbb{R}$. In terms of this notation the product in the group is given (by the [[Baker-Campbell-Hausdorff formula]]) by

$$
  \exp(a_1 \mathbf{q} + b_1 \mathbf{p})
  \exp(c_1 \mathbf{e})
  \cdot
  \exp(a_2 \mathbf{q} + b_2 \mathbf{p})
  \exp(c_2 \mathbf{e})
  = 
  \exp((a_1 + b_1) \mathbf{q} + (b_1 + c_1) \mathbf{p})
  \exp(c_1 + c_2 - \frac{1}{2}(a_1 b_2 - a_2 b_1) \mathbf{e})
  \,.
$$

A discrete [[quotient]] group of this, which still has the same [[Lie algebra]], has as underlying manifold $\mathbb{R}^2 \times U(1)$ (the second factor being the [[circle group]]), with the projection

$$
  \mathbb{R}^2 \times \mathbb{R}
  \to
  \mathbb{R}^2 \times U(1)
$$

being quotienting by $\mathbb{Z}$: $U(1) \simeq \mathbb{R} / \mathbb{Z}$.

If the circle group is instead thought of as the unit circle in the complex plane, then this quotient is thought of as the exponential map $\exp(2 \pi i (-)) : \mathbb{R} \to U(1)$. In terms of this the group elements in the quotient read

$$
  g_{a, b, c} 
   = 
  \exp(a \mathbf{q} + b \mathbf{p} )\exp(2 \pi i c )
$$

and their product is

$$
  \exp(a_1 \mathbf{q} + b_1 \mathbf{p})
  \exp(2 \pi i c_1 )
  \cdot
  \exp(a_2 \mathbf{q} + b_2 \mathbf{p})
  \exp(2 \pi i c_2 )
  = 
  \exp((a_1 + b_1) \mathbf{q} + (b_1 + c_1) \mathbf{p})
  \exp(2 \pi i(c_1 + c_2 - \frac{1}{2}(a_1 b_2 - a_2 b_1)))
  \,.
$$

While the Lie algebra is still the same real [[Heisenberg Lie algebra]] as before, it is now suggestive to write the Lie bracket as

$$
  [q,p] = i
  \,.
$$

This is the way the relation appears in texts on [[quantum physics]].
### For a symplectic vector space

Generally, there is a Heisenberg group $H(V, \omega)$ associated to 
any [[symplectic vector space]] $(V, \omega)$.

Regard $V$ with its [[abelian group]] structure underlying its [[vector space]] structure.

The Heisenberg group $H(V,\omega)$ is the space $V \times U(1)$ (for $U(1)$ the [[circle group]]) equipped with the group product

$$
  (v_1, c_1) \cdot (v_2, c_2)
  = 
  (v_1 + v_2, c_1 c_2 \exp(2 \pi i \omega(v,w)))
  \,.
$$

## Properties

### Relation to Poisson algebra
 {#RelationToPoissonBracket}

A [[symplectic vector space]] $(V, \omega)$ is in particular a [[symplectic manifold]]. Accordingly its algebra of [[smooth functions]] $C^\infty(V)$ is a [[Poisson algebra]]. The [[Lie algebra]] underlying the Poisson algebra contains the [[Heisenberg Lie algebra]] as the subspace with is the [[direct sum]] of the [[linear functions]] $V^* \hookrightarrow C^\infty(V)$ and the constant functions $\mathbb{R} \hookrightarrow C^\infty(V)$.

For more details in this at _[[Heisenberg Lie algebra]]_ the section _[Relation to Poisson algebra](#http://ncatlab.org/nlab/show/Heisenberg%20Lie%20algebra#RelationToPoissonAlgebra)_.

### Relation to symplectomorphisms
 {#RelationToSymplectomorphisms}

By the [above](#RelationToPoissonBracket), the Heisenberg group is a [[subgroup]] of the group that integrates the [[Poisson bracket]]. The latter is a [[central extension]] of the group of [[Hamiltonian symplectomorphisms]].

(Of course, on a contractible [[symplectic manifold]] such as a [[symplectic vector space]], every [[symplectomorphism]] is automatically a [[Hamiltonian symplectomorphism]].)

### Cocycle and extension

The additive group on the [[Cartesian space]] $\mathbb{R}^2$ with group operation

$$
  (a,b) + (a',b') = (a + a' , b + b')
$$

carries a degree-2 [[group cocycle]] $\omega$ with values in $\mathbb{R}$ given by

$$
  \omega : ((a_1,b_1), (a_2,b_2)) \mapsto a_1 \cdot b_2
  \,.
$$

The cocycle condition for this is the identity

$$
  a_1 \cdot (b_2 + b_3) + a_2 \cdot b_3 
  =
  a_1 \cdot b_2 + (a_1 + a_2) \cdot b_3
$$

The Heisenberg group $H_3$ is the [[group extension]] of $\mathbb{R}^2$ by this cocycle.

### Unitary representations

See _[[Stone-von Neumann theorem]]_.

### Automorphism group

The [[automorphism group]] of the Heisenberg group is the [[symplectic group]].

## Related concepts

* [[Heisenberg Lie algebra]]

* [[quantomorphism group]]

* [[spherical CR manifold]]

* [[Heisenberg n-group]]

## References

### General

An original account is in 

* [[Bertram Kostant]], _Quantization and unitary representations_, in _Lectures in modern analysis and applications III_. Lecture Notes in Math. 170 (1970), Springer Verlag, 87&#8212;208

A textbook account is in section II.3 of 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_, Birkh&#228;user (1993)


Discussion in the context of [[geometric quantization]] is in 

* _Geometric quantization II, Prequantization and the Heisenberg group_ ([pdf](http://www.maths.ed.ac.uk/~jthomas7/GeomQuant/Lecture2.pdf))

Discussion of the [[representation theory]] of the infinite-dimensional Heisenberg group is in

* G&#252;nther H&#246;rmann, _Representations of the infinite dimensional Heisenberg group_, PhD thesis, Vienna 1993 ([pdf](http://www.mat.univie.ac.at/~michor/hoermann_diss.pdf))

### For Chern-Simons theory

The Heisenberg group for the [[phase space]] $U(1)$-[[Chern-Simons theory]] on an arbitrary [[Riemann surface]] (and its relation to [[skein relations]] and [[theta functions]]) is discussed in

* {#GelcaUribe10a} [[Razvan Gelca]], [[Alejandro Uribe]], _From classical theta functions to topological quantum field theory_  ([arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf))

* {#GelcaHamilton12} [[Razvan Gelca]], [[Alastair Hamilton]], _Classical theta functions from a quantum group perspective_ ([arXiv:1209.1135](http://arxiv.org/abs/1209.1135))


[[!redirects Heisenberg groups]]

[[!redirects Heisenberg Lie group]]
[[!redirects Heisenberg Lie groups]]

[[!redirects Weyl-Heisenberg group]]
[[!redirects Weyl-Heisenberg groups]]

