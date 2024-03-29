
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
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

## Definition

The **Poincar&#233; group** $ISO(d,1)$ is the [[isometry group]] of [[Minkowski spacetime]] of [[dimension]] $d+1$. The classical case is $ISO(3, 1)$, the [[group]]  of affine transformations on $\mathbb{R}^4$ which preserve the [[pseudo-Riemannian metric|Minkowski "metric"]], i.e., the group of maps $f: \mathbb{R}^4 \to \mathbb{R}^4$ of the form $f(\vec{x}) = M \vec{x} + \vec{b}$ such that 

$$Q(f(\vec{x}) - f(\vec{y})) = Q(\vec{x} - \vec{y})$$ 

where the quadratic form $Q(t, x, y, z) = t^2 - x^2 - y^2 - z^2$ is often called the Minkowski "norm". The group elements are multiplied by composing maps. 

The Poincar&#233; group $G$ may also be described as a [[semidirect product]] 

$$(\mathbb{R} \oplus \mathbb{R}^3) \rtimes O(1, 3)$$ 

where $O(1, 3)$, the **Lorentz group**, consists of all _linear_ transformations $L: \mathbb{R}^4 \to \mathbb{R}^4$ that preserve the Minkowski inner product of signature $(1, 3)$. 

This is a linear [[algebraic group]] (e.g. [arXiv:0905.1217, p. 6-7](http://arxiv.org/abs/0905.1217)).

## Properties

### Basic structure of the Lorentz group 

The [[Lorentz group]] is a 6-dimensional [[Lie group]]. It has four connected components; the [[connected space|connected component]] of the identity is called the **special Lorentz group** and is denoted $SO^+(1, 3)$. 

* The superscript of $SO^+(1, 3)$ indicates that the group elements take the **forward light cone**, i.e., the set of vectors 
$$\{v = (t, x, y, z): Q(v) \gt 0, t \gt 0\},$$ 
to itself, and the $S$ indicates of course group elements which have determinant 1 as $4 \times 4$ matrices. It easily follows that elements of $SO^+(1, 3)$ preserve orientation of the spatial component $\mathbb{R}^3$. 

Passage between the four components of the full Lorentz group is effected by composing with a **time-reversal** operator 

$$(t, x, y, z) \mapsto (-t, x, y, z)$$ 

and with a spatial inversion (or **parity-reversal**) operator 

$$(t, x, y, z) \mapsto (t, -x, -y, -z)$$ 

The special Lorentz group (also called the **proper, orthochronous** Lorentz group: "orthochronous" here means the forward light cone is mapped to itself, and "proper" means orientation-preserving) may be analyzed further. The subgroup of $SO^+(1, 3)$ that fixes the unit time-like vector 

$$u_t := (1, 0, 0, 0)$$ 

may be identified with the group of rotations $SO(3)$, since the restriction of the Minkowski norm to the spatial component $\mathbb{R}^3$ is minus the usual Euclidean norm, $-x^2 - y^2 - z^2$. This subgroup is of course 3-dimensional. 

A general element $g \in SO^+(1, 3)$ may be decomposed uniquely in the form 

$$g = \beta_v \circ \rho$$ 

where $\rho$ is a rotation and $\beta_v$ is a **boost** in the direction $v$ ($v \in S^2$ a unit spatial vector), mapping 

$$u_t \mapsto \cosh(\beta)u_t + \sinh(\beta)v$$ 

$$v \mapsto \sinh(\beta)u_t + \cosh(\beta)v$$ 

for some parameter $\beta$ (called the **rapidity**), and acting as the identity on the spatial plane orthogonal to $v$. Thus a boost is described by a pair $(v, \beta)$, involving 3 parameters. (Warning: boosts do not compose to form a subgroup.) A boost can be thought of as a relativistic coordinate change from a "laboratory" frame of reference to the frame of reference of an observer moving inertially in the direction $v$ with speed $\tanh(\beta)$ (relative to the speed of light $c = 1$), as measured in the laboratory frame. 

### Universal spin covering 
 {#UniversalSpinCovering}

We discuss aspects of the [[Poincaré spinor group]].

The universal cover of $SO^+(1, 3)$ is a double cover (the **spin double cover**) 

$$SL_2(\mathbb{C}) \to SO^+(1, 3)$$ 

constructed as follows: to each $x = (x_0, x_1, x_2, x_3)$ one associates a [[Hermitian matrix]] 

$$X = \left(
\array{
x_0 + x_1 & x_2 + i x_3 \\
x_2 - i x_3 & x_0 - x_1
}
\right) 
= x_0 \left(
\array{
1 & 0 \\
0 & 1
}
\right) 
+ x_1 \left(
\array{
1 & 0 \\
0 & -1
}
\right)
+ x_2 \left(
\array{0 & 1 \\
1 & 0
}
\right)
+ x_3 \left(
\array{
0 & i \\
-i & 0
}
\right)
$$

whose determinant is the Minkowski norm of $x$. We thus identify $\mathbb{R}^4$ with the space $H$ of Hermitian matrices, and define an action of $SL_2(\mathbb{C})$ on $H$:  

$$A \cdot X = A X A^*, A \in SL_2(\mathbb{C}), X \in H$$ 

Observe that $A X A^*$ belongs to $H$. Also, $det(A \cdot X) = det(X)$ since $A$ has determinant 1, so the action preserves the Minkowski norm. Therefore the action 

$$SL_2(\mathbb{C}) \to GL(\mathbb{R}^4)$$ 

factors through the inclusion $O(1, 3) \hookrightarrow GL(\mathbb{R}^4)$. Furthermore, since $SL_2(\mathbb{C})$ is connected, the action $SL_2(\mathbb{C}) \to O(1, 3)$ factors through the connected component $SO^+(1, 3)$ of $O(1, 3)$. It is not hard to check that the kernel of the action is $\{I, -I\}$; therefore the map 

$$SL_2(\mathbb{C}) \to SO^+(1, 3)$$ 

is an open homomorphism between connected Lie groups of the same dimension, and is therefore surjective. In this way, we have produced an explicit identification 

$$SL_2(\mathbb{C})/\{\pm I\} \cong SO^+(1, 3)$$ 

which exhibits $SL_2(\mathbb{C})$ as a double cover of $SO^+(1, 3)$; another way to say it is that $SO^+(1, 3)$ is identified with the group $PSL_2(\mathbb{C})$ of complex [[Moebius transformation]]s. Finally, there is morphism of covering spaces 

$$\array{
SU(2) & \hookrightarrow & SL_2(\mathbb{C}) \\
\pi \downarrow & & \downarrow \pi \\
SO(3) & \hookrightarrow & SO^+(1, 3)
}$$ 

Here the inclusions are homotopy equivalences and the left projection is a universal covering map (as $SU(2) \cong S^3$ is simply connected), therefore $SL_2(\mathbb{C})$ is also simply connected and the projection on the right is a universal covering map. This is the _spin double cover_; it is crucial for getting a correct mathematical description of [[fermion]]s in particle theory. 

With regard to the inclusion maps above being homotopy equivalences, we remark in passing that the [[homogeneous space]] 

$$SO^+(1, 3)/SO(3)$$ 

is identified with the space of boost maps; concretely, each coset of $SO^+(1, 3)/SO(3)$ is of the form $\beta_v SO(3)$ for a unique boost map $\beta_v$. Topologically, the space of boost maps is $\mathbb{R}^3$ or a $3$-ball, hence contractible, and from the long exact homotopy sequence applied to the fibration 

$$SO(3) \to SO^+(1, 3) \to SO^+(1, 3)/SO(3)$$ 

we deduce that the inclusion $i: SO(3) \to SO^+(1, 3)$ is a homotopy equivalence. 

Similarly the lift to the double covers $SU(2) \to SL_2(\mathbb{C})$ is a homotopy equivalence. Since $SU(2) \cong S^3$ is identified with the space of unit quaternions, $SU(2)$ and $SL_2(\mathbb{C})$ are simply connected and hence the respective universal covering spaces of $SO(3)$ and $SO^+(1, 3)$. 

* **Remark:** Geometrically the space of boosts carries hyperbolic structure as well, in other words the space of boosts carries a structure of hyperbolic 3-space $H^3$. 

### Lie algebra presentations 

As for any Lie group, there are various mechanisms for describing the [[Lie algebra]]s of the Lorentz group and of the Poincar&#233; group: by left-invariant [[vector field]]s, or by studying "infinitesimal generators" of 1-parameter subgroups, etc. We begin with the Lorentz group. See also [[Poincaré Lie algebra]].



In the vector field picture, one often chooses a basis of the [[Lorentz algebra]] consisting of six elements: the first three 

$$M_{12} = x\partial_y - y\partial_x \qquad M_{23} = y\partial_z - z\partial_y \qquad M_{13} = z\partial_x - x\partial_z$$ 

describe rotational flows (around the $z$-, $x$-, and $y$-axes respectively), and the last three 

$$M_{01} = x\partial_t + t\partial_x \qquad M_{02} = y\partial_t + t\partial_y \qquad M_{03} = z\partial_t + t\partial_z$$ 

describe hyperbolic or boost flows, (where the boosts are in the directions of the $x$-, $y$-, and $z$-axes, respectively). One may easily compute the commutators by hand and reproduce the standard gobbledygook formula given in physics texts: 

$$[M_{\mu\nu}, M_{\rho\sigma}] = \eta_{\mu\rho} M_{\nu\sigma} - \eta_{\mu\sigma} M_{\nu\rho} - \eta_{\nu\rho} M_{\mu\sigma} + \eta_{\nu\sigma} M_{\mu\rho}$$ 

where lower-case Greek letters range over $0, 1, 2, 3$ and $\eta$ is the $4 \times 4$ matrix representing the Minkowski quadratic form. 

_(I could be off by a sign here. It depends on whether $\eta$ has one plus and three minuses, or one minus and three pluses.)_ 

By integrating the vector fields, we obtain in each of these cases flows or 1-parameter subgroups, e.g., 

$$s \mapsto \exp(s M_{12}) = \left(
\array{
1 & 0 & 0 & 0 \\
0 & \cos(s) & -\sin(s) & 0 \\
0 & \sin(s) & \cos(s) & 0 \\
0 & 0 & 0 & 1
}
\right)$$ 

$\,$

$$s \mapsto \exp(s M_{01}) = \left(
\array{ 
\cosh(s) & \sinh(s) & 0 & 0 \\
\sinh(s) & \cosh(s) & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
}
\right)$$

Differentiating these maps at $s = 0$ gives matrix representations for the Lie algebra elements $M_{\mu\nu}$. 

For the 10-dimensional Poincar&#233; algebra, we need to give, in addition to infinitesimal generators for rotations and boosts, four more elements which generate translations. In the vector field picture, these Lie algebra elements are represented by 

$$P_0 = \partial_t, P_1 = \partial_x, P_2 = \partial_y, P_3 = \partial_z$$ 

and these of course commute; the brackets with the $M_{\mu\nu}$ are 

$$[M_{\mu\nu}, P_\rho] = \eta_{\mu\rho} P_\nu - \eta_{\nu\rho} P_\mu$$ 

Integration of the vector fields $P_\rho$ leads to the expected translations, e.g.,  

$$\exp(s P_0)(t, x, y, z) = (t + s, x, y, z)$$ 

## The Poincare group in physics 

The Poincar&#233; group is basic to relativistic physics, since the fundamental principle of relativity is that physical laws are required to be invariant with respect to the action of the Poincar&#233; group on spacetime. (There is some fine print here: in some cases, e.g., where physical laws are not invariant under space or time inversions, one must restrict to the action of the group $\mathbb{R}^4 \rtimes SO^+(1, 3)$. If one is dealing with fermions, one considers invariance with respect to an action of the universal cover $\mathbb{R}^4 \rtimes SU_2(\mathbb{C})$.) 

Such physical laws may be classical or quantum, according to the description of physical states and observables in the theory. For example, in classical mechanics, pure states correspond to points in a symplectic phase space such as the cotangent bundle of Minkowski 4-space; in quantum mechanics, pure states are described by unit vectors in a suitable Hilbert space such as $L^2(\mathbb{R}^4)$. In either case, a relativistic theory will involve an action or representation of the Poincar&#233; group, together with a structure which governs the dynamics of the theory, e.g., a Hamiltonian. 

In the quantum case, a fundamental relativistic condition is that probability amplitudes $\langle \psi|\phi \rangle$, obtained by pairing an initial state $\phi$ with a final state $\psi$, are invariant under the action of the Poincar&#233; group. This condition says 

$$\langle \psi|\phi \rangle = \langle g \cdot \psi|g \cdot \phi \rangle$$ 

for every $g$ in the Poincar&#233; group. Thus the representation of the Poincar&#233; group on Hilbert space is required to be _unitary_. Due to the noncompactness of the Poincar&#233; group, unitary representations on finite-dimensional Hilbert spaces are scarce; one must really pass to unitary representations on infinite-dimensional Hilbert spaces to get anything interesting. 

In particular, an **elementary particle** in quantum physics is sometimes defined to be an [[unitary irreps of the Poincare group|irreducible unitary representation]] of the Poincar&#233; group on $L^2(\mathbb{R}^4)$. 

#### Unitary representations

* [[unitary irrep of the Poincare group]]


## Related entries

* [[Lorentzian geometry]]

* [[orthogonal group]], [[affine group]]

* [[Euclidean group]]

  * [[super Euclidean group]]

* [[super Poincaré group]]

* [[Poincaré Lie algebra]]

  * [[super Poincaré Lie algebra]]

[[!include table of orthogonal groups and related]]

[[!redirects Poincare group]]

[[!redirects Poincaré symmetry]]
[[!redirects Poincare symmetry]]

[[!redirects Poincaré symmetries]]
[[!redirects Poincare symmetries]]


[[!redirects Poincaré symmetry transformation]]
[[!redirects Poincare symmetry transformation]]

[[!redirects Poincaré symmetry transformations]]
[[!redirects Poincare symmetry transformations]]

