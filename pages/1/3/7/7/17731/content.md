
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Majorana spin representation_ is essentially a _real_ [[spin representation]] (see at _[spin representation -- Real representations](spin+representation#RealIrreducibleSpinRepresentationInLorentzSignature)_) but regarded as a _complex_ [[spin representation]] equipped with [[real structure]].

The terminology _Majorana spinor_ originates in and is standard in the [[physics]] literature, where it usually refers to the explicit expression of the reality condition in terms of chosen basis components. With standard conventions understood, then a complex [[spinor]] $\psi$ for $Spin(d-1,1)$, regarded as an element of $\mathbb{C}^{ceil((d-2)/2)}$ is a Majorana spinor if it satisfies the condition

$$
  \psi^t C = \psi^\dagger \Gamma_0
  \,,
$$

where $(-)^T$ denotes forming [[transpose matrices]], $(-)^\dagger = \overline{(-)}^T$ denotes forming [[hermitian adjoint]] and where $C$ is the [[charge conjugation matrix]]. This says that the _Majorana conjugate_ of $\psi$ (the left hand side) coincides with the _[[Dirac conjugate]]_ of $\psi$ (the right hand side). Equivalently this means that (e.g. [Castellani-D'Auria-Fr&#233;, (II.7.22)](#CastellaniDAuriaFre))

$$
  \psi = C \Gamma_0^T \psi^\ast
  \,.
$$

That this is indeed equivalent to $\psi$ being in the real part of a [[spin representation]] with [[real structure]] is made explicit for instance in ([Figueroa-O'Farrill](#FigueroaOFarrill)).

In some dimensions there are no complex spin representations with real structure, but there are those with [[quaternionic structure]]. The corresponding physics jargon then is _symplectic Majorana spinor_.

## Details

> under construction

### Review of unitary representations with real structure

All [[vector spaces]] in the following are taken to be [[finite dimensional vector spaces]].

+-- {: .num_defn #RealStructure}
###### Definition

Let $V$ be a [[complex vector space]]. A _[[real structure]]_ or _[[quaternionic structure]]_ on $V$ is a real-[[linear map]]

$$
  \phi \;\colon\; V \longrightarrow V
$$

such that 

1. $\phi$ is conjugate linear ($\phi(\lambda v) = \overline{\lambda} \phi(v)$ for all $\lambda \in \mathbb{C}$, $v \in V$);

1. $\phi^2 = \left\{ \array{ +id & \text{for real structure} \\ -id & \text{for quaternionic structure} }  \right.$

=--

+-- {: .num_remark}
###### Remark

A real structure $\phi$, def. \ref{RealStructure}, on a complex vector space $V$ corresponds to a choice of complex linear isomorphism

$$
  V \simeq \mathbb{C} \otimes_{\mathbb{R}} V_+
$$

of $V$ with the [[complexification]] of a real vector space $V_+$, namely the [[eigenspace]] of $\phi$ for [[eigenvalue]] +1, while $V_- \coloneqq i V_+$ is the eigenspace of eigenvalue -1.

A quaternionic structure, def. \ref{RealStructure}, o $V$ gives it the structure of a left [[module]] over the [[quaternions]] extending the underlying structure of a module over the complex numbers. Namely let

1. $I \coloneqq i(-) \colon V \to V$ be the operation of acting with $i \in \mathbb{C}$

1. $J \coloneqq \phi \colon V \to V$ be the given endomorphisms,

then the conjugate complex linearity of $\phi$ means that

$$
  J \circ I = - I \circ J
$$

and hence with $J^2 = -1$ and $I^2 = -1$ this means that $I$, $J$ and $K \coloneqq I \circ J$ act like the imaginary quaternions.

=--

+-- {: .num_defn #RealStructureOnLinearRepresentation}
###### Definition

Let $G$ be a [[Lie group]], let $V$ be a [[complex vector space]] and let 

$$
  \rho \;\colon\; G \longrightarrow GL_{\mathbb{C}}(V)
$$

be a complex [[linear representation]] of $G$ on $V$, hence a [[group homomorphism]] form $G$ to the [[general linear group]] of $V$ over $\mathbb{C}$.

Then a _real structure_ or _quaternionic structure_ on $(V,\rho)$ is a real or complex structure, respectively, $\phi$ on $V$ (def. \ref{RealStructure}) such that $\phi$ is $G$-invariant under $\rho$, i.e. such that for all $g \in G$ then 

$$
  \phi \circ \rho(g) = \rho(g) \circ \phi
  \,.
$$

=--

We will be interested in complex [[finite dimensional vector spaces]] equipped with [[hermitian forms]], i.e. finite-dimensional complex [[Hilbert spaces]]:

+-- {: .num_defn #HermitianForms}
###### Definition

A [[hermitian form]] (or symmetric complex [[sesquilinear form]]) $\langle -,-\rangle$ on a [[complex vector space]] $V$ is a real [[bilinear form]]

$$
  \langle
    -,-
  \rangle
  \;\colon\;
  V \times V
   \longrightarrow
  \mathbb{C}
$$

such that for all $v_1, v_2 \in V$ and $\lambda \in \mathbb{C}$ then

1. (sesquilinearity) $\langle v_1, \lambda v_2 \rangle = \lambda \langle v_1, v_2 \rangle $,

1. (symmetry) $\overline{\langle v_1, v_2\rangle} = \langle v_2, v_1\rangle $.

1. (non-degeneracy) if $\langle v_1,-\rangle = 0$ then $v_1 = 0$.



A complex [[linear function]]  $f \colon V \to V$ is _[[unitary operator|unitary]]_ with respect to this hermitian form if it preserves it, in that

$$
  \langle f(-), f(-)\rangle
  = 
  \langle -,-\rangle
  \,.
$$

Write

$$
  U(V) \hookrightarrow GL_{\mathbb{C}}(V)
$$

for the [[subgroup]] of [[unitary operators]] inside the [[general linear group]].

A complex [[linear representation]] $\rho \colon G \longrightarrow GL_{\mathbb{C}}(V)$ of a [[Lie group]] on $V$ is called a _[[unitary representation]]_ if it factors through this subgroup

$$
  \rho \;\colon\;  G \longrightarrow U(V) \hookrightarrow GL_{\mathbb{C}}(V)
  \,.
$$


=--


+-- {: .num_prop }
###### Proposition

Let $V$ be a [[complex vector space|complex]] [[finite dimensional vector space]], $\langle -,-\rangle$ some [[hermitian form]] on $V$, def. \ref{HermitianForms}, let $G$ be a [[Lie group]], and $\rho \colon G \to U(V)$ a [[unitary representation]] of $G$ on $V$. Then $\rho$ carries a real structure or quaternionc structure $\phi$ on $\rho$ (def. \ref{RealStructureOnLinearRepresentation}) precisely if it carries a symmetric or anti-symmetric, respectively, non-degenerate complex-[[bilinear map]]

$$
  (-,-) \;\colon\; V \otimes_{\mathbb{C}} V \longrightarrow \mathbb{C}
  \,.
$$

Explicitly:

Given a real/quaternionic structure $\phi$, then the corresponding symmetric/anti-symmetric complex bilinear form is 

$$
  (-,-) \coloneqq \langle \phi(-), -\rangle
  \,.
$$

Conversely, given $(-,-)$, first define $\tilde \phi$ by

$$
  (-,-) = \langle \tilde\phi(-),-\rangle
  \,,
$$ 

and then $\phi \coloneqq \frac{1}{\vert \phi\vert} \phi$ is the corresponding real/quaternionic structure. 

If $\tilde\phi = \phi$ then $(-,-)$ is called _compatible_ with $\langle-,- \rangle$.


=--

(e.g. [Meinrenken 13, p. 81](#Meinrenken13))

### Majorana spinors

+-- {: .num_defn}
###### Definition

Let $\rho \colon Spin(s,t) \longrightarrow GL_{\mathbb{C}}(V)$ be a [[unitary representation]] of a [[spin group]]. Then $\rho$ is called _Majorana_ if it admits a real structure $J$ (def. \ref{RealStructureOnLinearRepresentation}) and _symplectic Majorana_ if it admits a quaternionic structure $J$. An element $\psi \in V$ is called a _Majorana spinor_ if $J(\psi) = \psi$.

=--

### In components

+-- {: .num_defn}
###### Definition

We write $\mathbb{R}^{s,t}$ for the real [[vector space]] $\mathbb{R}^{s+t}$ equipped with the standard [[quadratic form]] $q$ of [[signature of a quadratic form|signature]] $(s,t)$, i.e.

$$
  q(\vec x)
    \coloneqq
  (x^1)^2
    + 
    \cdots
    +
  (x^s)^2
    -
  (x^{s+1})^2
    -
   \cdots
  -
  (x^{s+t})^2
  \,.
$$

Write 

$$
  \eta \coloneqq diag(\underset{s}{\underbrace{+1 , \cdots, +1}}, \underset{t}{\underbrace{-1, \cdots, -1}})
$$

for the corresponding [[metric]].

=--

The real [[Clifford algebra]] $Cl(s,t)$ is the $\mathbb{R}$-[[associative algebra|algebra]] [[generators and relations|generated]] from elements $\{\Gamma_a\}_{a = 1}^{s+t}$ subject to the [[generators and relations|relation]]

$$
  \Gamma_a \Gamma_b + \Gamma_b \Gamma_a = - 2 \eta_{a b} 
  \,.
$$

Case $t = 1$:

There is a choice for the complexified Clifford algebra generators such that

* $\Gamma_{time}$ is hermitian

* $\Gamma_{space}$ is anti-hermitian

This means that for $\mathbb{C}^{ceil(d-2)/2}$ a complex representation, then a hermitian form for which the Spin-group acts unitarily is given by

$$
  \langle 
    v_1, v_2
  \rangle
   \coloneqq
   v_1^\dagger \Gamma_0 v_2
$$

because the commutation through $\Gamma_0$ compensates the sign offset that elements of the form $\Gamma_{time} \Gamma_{space}$ pick up from the fact that $\Gamma_{time}$ fails to pick up the same sign from hermitian conjugation as the $\Gamma_{space}$ do.

Let then $C$ be the matrix that represents the bilinear form $(-,-)$, this is the [[charge conjugation matrix]]. From

$(-,-) = \langle J(-),(-)\rangle$

it jence follows for a Majorana spinor with $J(\psi) = \psi$ that 

$$
  \psi^t C \psi' = \psi^\dagger \Gamma_0 \psi'
$$

and hence by non-degeneracy of the pairing that 

$$
  \psi^t C = \psi^\dagger \Gamma_0
$$

which is the Majorana condition in the usual component expression


(...)




## Related concepts

* [[charge conjugation matrix]]

## References

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section II.7.3 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* {#FigueroaOFarrill} [[José Figueroa-O'Farrill]], _Majorana spinors_ ([pdf](http://www.maths.ed.ac.uk/~jmf/Teaching/Lectures/Majorana.pdf))

* {#Meinrenken13} [[Eckhard Meinrenken]], _Clifford algebras and Lie theory_, Springer (2013)

* Theodor Br&#246;cker, [[Tammo tom Dieck]], _Representations of Compact Lie Groups_, Springer (1985)

* Wikipedia, _[Majorana fermion](https://en.wikipedia.org/wiki/Majorana_fermion)_

[[!redirects Majorana spinor]]
[[!redirects Majorana spinors]]
[[!redirects Majorana representation]]
[[!redirects Majorana representations]]

[[!redirects symplectic Majorana spinor]]
[[!redirects symplectic Majorana spinors]]
[[!redirects symplectic Majorana representation]]
[[!redirects symplectic Majorana representations]]


[[!redirects Majorana-Weyl spinor]]
[[!redirects Majorana-Weyl spinors]]
[[!redirects Majorana-Weyl representation]]
[[!redirects Majorana-Weyl representations]]

[[!redirects Majorana fermion]]
[[!redirects Majorana fermions]]
