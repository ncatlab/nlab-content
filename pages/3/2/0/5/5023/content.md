

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
 {#H3InComponents}

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
  \exp\big(
    (a_1 + b_1) \mathbf{q} + (b_1 + c_1) \mathbf{p}
  \big)
  \exp\big(
    c_1 + c_2 - \tfrac{1}{2}(a_1 b_2 - a_2 b_1) \mathbf{e}
  \big)
  \,.
$$

A discrete [[quotient group]] of this, [[Lie integration|integrating]] the same [[Lie algebra]], has as underlying manifold $\mathbb{R}^2 \times U(1)$ (the second factor being the [[circle group]]), with the projection

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
  \exp\big(
    (a_1 + b_1) \mathbf{q} + (b_1 + c_1) \mathbf{p}
  \big)
  \exp\Big(
    2 \pi \mathrm{i}\big(
     c_1 + c_2 - \tfrac{1}{2}(a_1 b_2 - a_2 b_1)
   \big)
  \Big)
  \,.
$$

While the Lie algebra is still the same real [[Heisenberg Lie algebra]] as before, it is now suggestive to write the Lie bracket as

$$
  [q,p] = \mathrm{i}
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
  \Big(
    v_1 + v_2, c_1 c_2 \exp\big(2 \pi i \omega(v,w)\big)
  \Big)
  \,.
$$


\linebreak

## Properties

### Relation to Poisson algebra
 {#RelationToPoissonBracket}

A [[symplectic vector space]] $(V, \omega)$ is in particular a [[symplectic manifold]]. Accordingly its algebra of [[smooth functions]] $C^\infty(V)$ is a [[Poisson algebra]]. The [[Lie algebra]] underlying the Poisson algebra contains the [[Heisenberg Lie algebra]] as the subspace with is the [[direct sum]] of the [[linear functions]] $V^* \hookrightarrow C^\infty(V)$ and the constant functions $\mathbb{R} \hookrightarrow C^\infty(V)$.

For more details in this at _[[Heisenberg Lie algebra]]_ the section _[Relation to Poisson algebra](Heisenberg+Lie+algebra#RelationToPoissonAlgebra)_.

### Relation to symplectomorphisms
 {#RelationToSymplectomorphisms}

By the [above](#RelationToPoissonBracket), the Heisenberg group is a [[subgroup]] of the group that integrates the [[Poisson bracket]]. The latter is a [[central extension]] of the group of [[Hamiltonian symplectomorphisms]].

(Of course, on a contractible [[symplectic manifold]] such as a [[symplectic vector space]], every [[symplectomorphism]] is automatically a [[Hamiltonian symplectomorphism]].)

### Cocycle and extension

The additive group on the [[Cartesian space]] $\mathbb{R}^2$ with group operation

$$
  (a,b) + (a',b') = (a + a' , b + b')
$$

carries a degree=2 [[group cocycle]] $\omega$ with values in $\mathbb{R}$ given by

$$
  \omega \colon 
    \big((a_1,b_1), (a_2,b_2)\big) 
    \mapsto 
    a_1 \cdot b_2
  \,.
$$

The cocycle condition for this is

$$
  a_1 \cdot (b_2 + b_3) + a_2 \cdot b_3 
  =
  a_1 \cdot b_2 + (a_1 + a_2) \cdot b_3
  \,,
$$

which evidently holds due to [[distributivity]].

The Heisenberg group $H_3$ is equivalently the [[central extension]] of $\mathbb{R}^2$ [classified by](group+extension#CentralExtensionClassificationByGroupCohomology) this cocycle.


### Unitary representations

See _[[Stone-von Neumann theorem]]_.

### Automorphism group

The [[automorphism group]] of the Heisenberg group is the [[symplectic group]].

## Related concepts

* [[Heisenberg Lie algebra]]

* [[quantomorphism group]]

* [[integer Heisenberg group]]

* [[spherical CR manifold]]

* [[Heisenberg n-group]]

## References

### General

An original account:

* [[Bertram Kostant]], _Quantization and unitary representations_, in _Lectures in modern analysis and applications III_. Lecture Notes in Math. 170 (1970), Springer Verlag, 87&#8212;208

Monographs:  

* [[Jean-Luc Brylinski]], section II.3 of: _Loop spaces, characteristic classes and geometric quantization_, Birkh&#228;user (1993) &lbrack;([doi:10.1007/978-0-8176-4731-5](https://www.springer.com/gp/book/9780817647308)&rbrack;

* [[Ernst Binz]], Sonja Pods, *The geometry of Heisenberg groups --- With Applications in Signal Theory, Optics, Quantization, and Field Quantization*, Mathematical Surveys and Monographs **151**, American Mathematical Society (2008) &lbrack;[ams:surv-151](https://bookstore.ams.org/surv-151)&rbrack; 


Discussion in the context of [[geometric quantization]]: 

* _Geometric quantization II, Prequantization and the Heisenberg group_ ([pdf](http://www.maths.ed.ac.uk/~jthomas7/GeomQuant/Lecture2.pdf))

Discussion of the [[representation theory]] of the infinite-dimensional Heisenberg group is in

* G&#252;nther H&#246;rmann, _Representations of the infinite dimensional Heisenberg group_, PhD thesis, Vienna 1993 ([pdf](http://www.mat.univie.ac.at/~michor/hoermann_diss.pdf))

On [[group algebras]] of ([[underlying]] [[discrete group|discrete]]) [[Heisenberg groups]] as [[strict deformation quantizations]] of [[presymplectic manifold|pre-]][[symplectic vector spaces|symplectic]] [[topological vector spaces]] by [[continuous field of C-star algebras|continuous fields of]] [[Weyl algebras]]:

* [[Ernst Binz]], [[Reinhard Honegger]], [[Alfred Rieckers]], *Infinite dimensional Heisenberg group algebra and field-theoretic strict deformation quantization*, International Journal of Pure and Applied Mathematics **38** 1 (2007) &lbrack;[ijpam:2007-38-1/6](https://ijpam.eu/contents/2007-38-1/6/index.html), [pdf](https://www.ijpam.eu/contents/2007-38-1/6/6.pdf)&rbrack;

* [[Reinhard Honegger]], [[Alfred Rieckers]], *Heisenberg Group Algebra and Strict Weyl Quantization*, Chapter 23 in: *Photons in Fock Space and Beyond, Volume I: From Classical to Quantized Radiation Systems*, World Scientific (2015) &lbrack;chapter:[doi;10.1142/9789814696586_0023](https://doi.org/10.1142/9789814696586_0023), book:[doi:10.1142/9251-vol1](https://doi.org/10.1142/9251-vol1)&rbrack;


### For abelian Chern-Simons theory

The [[integer Heisenberg group]] describing the [[phase space]] of [[abelian Chern-Simons theory]] on [[closed manifold|closed]] [[Riemann surfaces]] (and its relation to [[skein relations]] and [[theta functions]]):

* {#GelcaUribe10} [[Răzvan Gelca]], [[Alejandro Uribe]]: *From classical theta functions to topological quantum field theory*, in: *The Influence of Solomon Lefschetz in Geometry and Topology: 50 Years of Mathematics at CINVESTAV*, Contemporary Mathematics **621**, AMS (2014) 35-68 &lbrack;[arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [doi;10.1090/conm/621](https://doi.org/10.1090/conm/621), [ams:conm-621](https://bookstore.ams.org/conm-621), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf), [[GelcaUribe-ThetaFunctionsTQFT.pdf:file]]&rbrack;

* {#GelcaHamilton12} [[Răzvan Gelca]], [[Alastair Hamilton]]: *Classical theta functions from a quantum group perspective*, New York J. Math. **21** (2015) 93–127 &lbrack;[arXiv:1209.1135](http://arxiv.org/abs/1209.1135), [nyjm:j/2015/21-4](https://nyjm.albany.edu/j/2015/21-4.html)&rbrack;

* {#GelcaHamilton15} [[Răzvan Gelca]], [[Alastair Hamilton]]: *The topological quantum field theory of Riemann’s theta functions*, Journal of Geometry and Physics **98** (2015) 242-261 &lbrack;[doi:10.1016/j.geomphys.2015.08.008](https://doi.org/10.1016/j.geomphys.2015.08.008), [arXiv:1406.4269](https://arxiv.org/abs/1406.4269)&rbrack;


[[!redirects Heisenberg groups]]

[[!redirects Heisenberg Lie group]]
[[!redirects Heisenberg Lie groups]]

[[!redirects Weyl-Heisenberg group]]
[[!redirects Weyl-Heisenberg groups]]



