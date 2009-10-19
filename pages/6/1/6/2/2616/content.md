The **Poincar&#233; group** is the group of affine transformations on $\mathbb{R}^4$ which preserve the Minkowski "metric", i.e., the group of maps $f: \mathbb{R}^4 \to \mathbb{R}^4$ of the form $f(\vec{x}) = M \vec{x} + \vec{b}$ such that 

$$Q(f(\vec{x}) - f(\vec{y})) = Q(\vec{x} - \vec{y})$$ 

where the quadratic form $Q(t, x, y, z) = t^2 - x^2 - y^2 - z^2$ is often called the Minkowski "norm". The group elements are multiplied by composing maps. 

The Poincar&#233; group $G$ may also be described as a [[semidirect product]] 

$$(\mathbb{R} \oplus \mathbb{R}^3) \rtimes O(1, 3)$$ 

where $O(1, 3)$, the **Lorentz group**, consists of all _linear_ transformations $L: \mathbb{R}^4 \to \mathbb{R}^4$ that preserve the Minkowski inner product of signature $(1, 3)$. 

## Basic structure of the Lorentz group 

The [[Lorentz group]] is a 6-dimensional [[Lie group]]. It has four connected components; the [[connected space|connected component]] of the identity is called the **special Lorentz group** and is denoted $SO^+(1, 3)$. The plus-superscript indicates that the group elements take the forward light cone (the set of vectors $\{v: Q(v) \geq 0\}$) to itself, and the $S$ indicates of course group elements which have determinant 1 as $4 \times 4$ matrices. (It easily follows that elements of $SO^+(1, 3)$ preserve orientation of the spatial component $\mathbb{R}^3$.) Passage between the four components of the full Lorentz group is effected by composing with a time-reversal operator 

$$(t, x, y, z) \mapsto (-t, x, y, z)$$ 

and with a spatial inversion (or parity-reversal) operator 

$$(t, x, y, z) \mapsto (t, -x, -y, -z)$$ 

The special Lorentz group may be analyzed further. The subgroup of $SO^+(1, 3)$ that fixes the unit time-like vector 

$$u_t := (1, 0, 0, 0)$$ 

may be identified with the group of rotations $SO(3)$, since the restriction of the Minkowski norm to the spatial component $\mathbb{R}^3$ is the usual Euclidean norm. This subgroup is of course 3-dimensional. 

A general element $g \in SO^+(1, 3)$ may be decomposed uniquely in the form 

$$g = \rho \circ \beta_v$$ 

where $\rho$ is a rotation and $\beta_v$ is a **boost** in the direction $v$ ($v \in S^2$ a unit spatial vector), mapping 

$$u_t \mapsto \cosh(\beta)u_t + \sinh(\beta)v$$ 

$$v \mapsto \sinh(\beta)u_t + \cosh(\beta)v$$ 

for some parameter $\beta$ (called the **rapidity**), and acting as the identity on the spatial plane orthogonal to $v$. Thus a boost is described by 3 parameters. (Warning: boosts do not compose to form a subgroup.) A boost can be thought of as a relativistic coordinate change from a "laboratory" frame of reference to the frame of reference of an observer moving inertially in the direction $v$ with speed $\tanh(\beta)$ (relative to the speed of light $c = 1$), as measured in the laboratory frame. 

## Universal spin covering 

The universal cover of $SO^+(1, 3)$ is a double cover (the **spin double cover**) 

$$SL_2(\mathbb{C}) \mapsto SO^+(1, 3)$$ 

constructed as follows: to each $x = (x_0, x_1, x_2, x_3)$ there is an associated Hermitian matrix 

$$X = \left(
\array{
x_0 + x_1 & x_2 + i x_3 \\
x_2 - i x_3 & x_0 - x_1
}
\right)
$$

whose determinant is the Minkowski norm of $x$. By identifying $\mathbb{R}^4$ with the space of Hermitian matrices $H$, we may define an action of $SL_2(\mathbb{C})$:  

$$A \cdot X = A X A^*, A \in SL_2(\mathbb{C})$$ 

Observe that $det(A \cdot X) = det(X)$ (so the action preserves the Minkowski norm). Since $SL_2(\mathbb{C})$ is connected, the action $SL_2(\mathbb{C}) \to hom(H, H)$ factors through the connected component $SO^+(1, 3)$ of the Lorentz group. It is not hard to check that the kernel of the action is $\{I, -I\}$; therefore the map 

$$SL_2(\mathbb{C}) \to SO^+(1, 3),$$ 

being an open homomorphism between connected Lie groups of the same dimension, is surjective. Finally, there is a commutative diagram 

$$\array{
SU(2) & \hookrightarrow & SL_2(\mathbb{C}) \\
\pi \downarrow & & \downarrow \pi \\
SO(3) & \hookrightarrow & SO^+(1, 3)
}$$ 

where the inclusions are homotopy equivalences and the left projection is a universal covering map, therefore the right projection is also a universal covering map. In this way, we have an explicit identification 

$$PSL_2(\mathbb{C}) \cong SO^+(1, 3)$$ 

## Lie algebra presentations 

As for any Lie group, there are various mechanisms for describing the [[Lie algebra]]s of the Lorentz group and of the Poincar&#233; group: by left-invariant vector fields, or by studying "infinitesimal generators" of 1-parameter subgroups, etc. We begin with the Lorentz group. 

In the vector field picture, one often chooses a basis of the Lorentz algebra consisting of six elements: the first three 

$$M_{12} = x\partial_y - y\partial_x \qquad M_{23} = y\partial_z - z\partial_y \qquad M_{13} = z\partial_x - x\partial_z$$ 

describe rotational flows (around the $z$-, $x$-, and $y$-axes respectively), and the last three 

$$M_{01} = x\partial_t + t\partial_x \qquad M_{02} = y\partial_t + t\partial_y \qquad M_{03} = z\partial_t + t\partial_z$$ 

describe hyperbolic or boost flows, (in the directions of the $x$-, $y$-, and $z$-axes, respectively). One may easily compute the commutators by hand and reproduce the standard formula given in physics texts: 

$$[M_{\mu\nu}, M_{\rho\sigma}] = \eta_{\mu\rho} M_{\nu\sigma} - \eta_{\mu\sigma} M_{\nu\rho} - \eta_{\nu\rho} M_{\mu\sigma} + \eta_{\nu\sigma} M_{\mu\rho}$$ 

where lower-case Greek letters range over $0, 1, 2, 3$ and $\eta$ is the $4 \times 4$ matrix representing the Minkowski quadratic form. 

_(I could be off by a sign here.)_ 

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

$$\exp(s P_0)|_{(t, x, y, z)} = (t + s, x, y, z)$$ 

## The Poincare group in physics 

The Poincar&#233; group is basic to relativistic physics, since the fundamental principle of relativity is that physical laws are required to be invariant with respect to the action of the Poincar&#233; group on spacetime. (There is some fine print here: in some cases, e.g., where physical laws are not invariant under space or time inversions, one must restrict to the action of the group $\mathbb{R}^4 \rtimes SO^+(1, 3)$, or pass to its universal cover.) 

Such physical laws may be classical or quantum, according to the description of physical states and observables in the theory. For example, in classical mechanics, pure states correspond to points in a symplectic phase space such as the cotangent bundle of Minkowski 4-space; in quantum mechanics, pure states are described by unit vectors in a suitable Hilbert space such as $L^2(\mathbb{R}^4)$. In either case there is an action or representation of the Poincare group. 

In the quantum case, a fundamental relativistic condition is that probability amplitudes $\langle \psi|\phi \rangle$, obtained by pairing an initial state $\phi$ with a final state $\psi$, are invariant under the action of the Poincar&#233; group. This condition says 

$$\langle \psi|\phi \rangle = \langle g \cdot \psi|g \cdot \phi \rangle$$ 

for every $g$ in the Poincare group. Thus the representation of the Poincar&#233; group on Hilbert space is required to be _unitary_. Due to the noncompactness of the Poincar&#233; group, unitary representations on finite-dimensional Hilbert spaces are scarce; one must really pass to unitary representations on infinite-dimensional Hilbert spaces to get anything interesting. 

In particular, an **elementary particle** in quantum physics is sometimes defined to be an [[unitary irreps of the Poincare group|irreducible unitary representation]] of the Poincar&#233; group. 
