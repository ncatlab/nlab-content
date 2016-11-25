
> this entry is one section of "[[geometry of physics -- supergeometry and superphysics]]"
> which is one chapter of "[[geometry of physics]]"

> previous section: _[[geometry of physics -- supergeometry]]_

> next section _[[geometry of physics -- fundamental super p-branes]]_

> under construction





#Supersymmetry#
* table of contents
{:toc}

### Spacetime supersymmetry


We consider now very specific [[super Lie algebras]], def. \ref{SuperLieAlgebraViaCE}, those of _[[spacetime]] [[supersymmetry]]_.

Just as traditional [[Cartan geometry]] involves a pair of [[Lie algebras]] $\mathfrak{h} \hookrightarrow \mathfrak{g}$, so super-Cartan geometry involves a similar pair of [[super Lie algebras]].
For describing [[supergravity]], we now
want to establish an [[superalgebra]]-[[analogy|analog]] of the inclusion of the [[Lorentz Lie algebra]] $\mathfrak{h} = \mathfrak{so}(\mathbb{R}^{d-1,1})$ into the [[Poincaré Lie algebra]] $\mathfrak{g} = \mathfrak{Iso}(\mathbb{R}^{d-1,1})$.

| ([[higher Cartan geometry|higher]]-)[[Cartan geometry]] | $\mathfrak{g}$ | $\mathfrak{h}$ | $\mathfrak{g}/\mathfrak{h}$ |
|---------------------|----------------|----------------|-----------------------------|
| [[Einstein gravity]]  | $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ | $\mathfrak{so}(\mathbb{R}^{d-1,1})$ | $\mathbb{R}^{d-1,1}$ |
| [[supergravity]] | $\mathfrak{Iso}(\mathbb{R}^{d-1,1\vert N})$ | $\mathfrak{so}(\mathbb{R}^{d-1,1})$ | $\mathbb{R}^{d-1,1\vert N}$ |
| [[11-dimensional supergravity]] | $\mathfrak{Iso}(\widehat{\mathbb{R}}^{10,1\vert \mathbf{32}})$ | $\mathfrak{so}(\mathbb{R}^{d-1,1})$ | $\widehat{\mathbb{R}}^{10,1\vert \mathbf{32}}$ |

(Here the hat in the lowest row indicates an [[extended super Minkowski spacetime]], which involves [[higher Cartan geometry]].)

To that end, consider the structure of any [[super Lie algebra]]

$$
  \left(
    \mathfrak{Iso}(\mathbb{R}^{d-1,1})\oplus N
    ,
    [-,-]
  \right)
$$

that extends the [[Poincaré Lie algebra]] $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ by some odd-[[graded vector space]] $N$. Any such extension involves involves:

1. the even-odd superbracket $[\mathfrak{so},N]$, which hence is an [[action]] of the [[Lorentz Lie algebra]] on  $N$;

1. the even-even-odd [[Jacobi identity]], which is the action property of that action;

1. the odd-odd superbracket $[N,N]$ which is a _symmetric_ [[bilinear form]] $N \otimes N \to \mathbb{R}^{d-1,1}$

1. the even-odd-odd [[Jacobi identity]], which says that this bilinear form is $\mathfrak{o}(d-1,1)$-[[equivariance|equivariant]].


Such structure exists on [[real structure|real]] [[spin representation]] ([[Majorana representations]]):







#### Real spin representations -- Majorana spinors

+-- {: .num_defn #MajoranaSpinorGeneral}
###### Definition

Let $\rho \colon Spin(s,t) \longrightarrow GL_{\mathbb{C}}(V)$ be a [[unitary representation]] of a [[spin group]]. Then $\rho$ is called _Majorana_ if it admits a real structure $J$ (def. \ref{RealStructureOnLinearRepresentation}) and _symplectic Majorana_ if it admits a [[quaternionic structure]] $J$ (def. \ref{RealStructureOnLinearRepresentation}). An element $\psi \in V$ is called a _Majorana spinor_ if $J(\psi) = \psi$.

=--


Below we work out the following:

+-- {: .num_prop #RealSpinRepresentations}
###### Proposition

Let $V = \mathbb{R}^{d-1,1}$ be [[Minkowski spacetime]] of some [[dimension]] $d$.

The following table lists the [[irreducible representation|irreducible]] [[real structure|real]] [[spin representations]] of $Spin(V)$.

| $d$ | $Spin(d-1,1)$ | minimal real spin representation $N$ | $dim_{\mathbb{R}} S\;\;$ |  $V$ in terms of $S^\ast$ |  [[supergravity]] |
|--|--|--|--|--|--|
| 1 | $\mathbb{Z}_2$ | $N$ real | 1 | $V \simeq (N^\ast)^{\otimes}^2$ |  |
| 2 | $\mathbb{R}^{\gt 0} \times \mathbb{Z}_2$ | $N^+, N^-$ real | 1 | $V \simeq ({N^+}^\ast)^{\otimes^2} \oplus ({N^-}^\ast)^{\otimes 2}$ |  |
| 3 | $SL(2,\mathbb{R})$ | $N$ real | 2 |  $V \simeq Sym^2 N^\ast$ |  |
| 4 | $SL(2,\mathbb{C})$ | $N_{\mathbb{C}} \simeq N' \oplus N''$ | 4 | $V_{\mathbb{C}} \simeq {N'}^\ast \oplus {N''}^\ast$ |  |
| 5 | $Sp(1,1)$ | $N_{\mathbb{C}} \simeq N_0 \otimes_{\mathbb{C}} W$ | 8 |  $\wedge^2 S_0^\ast \simeq \mathbb{C} \oplus V_{\mathbb{C}}$ |  |
| 6 | $SL(2,\mathbb{H})$ | $N^\pm_{\mathbb{C}} \simeq N_0^\pm  \otimes_{\mathbb{C}} W$ | 8 | $V_{\mathbb{C}} \simeq \wedge^2 {N_0^+}^\ast \simeq (\wedge^2 {N_0^-}^\ast)^\ast$ |  |
| 7 |  |  $N_{\mathbb{C}} \simeq N_0 \otimes_{\mathbb{C}} W$ | 16 |  $\wedge^2 S_0^\ast \simeq V_{\mathbb{C}} \oplus \wedge^2 V_{\mathbb{C}}$ |  |
| 8 |  | $N_{\mathbb{C}} \simeq N^\prime \oplus N^{\prime\prime}$ | 16 | ${N'}^\ast {N''}^\ast \simeq V_{\mathbb{C}} \oplus \wedge^3 V_{\mathbb{C}}$ |  |
| 9 |  | $N$ real | 16 |  $Sym^2 N^\ast \simeq \mathbb{R} \oplus V \wedge^4 V$ |  |
| 10 |   | $N^+ , N^-$ real | 16 | $Sym^2(N^\pm)^\ast \simeq V  \oplus \wedge_\pm^5 V$ | [[type II supergravity]] |
| 11 |   | $N$ real | 32 | $Sym^2 N^\ast \simeq V \oplus \wedge^2 V \oplus \wedge^5 V$ | [[11-dimensional supergravity]] |

Here $W$ is the 2-dimensional [[complex vector space]] on which the [[quaternions]] naturally act.

=--

(e.g. [Freed 99, page 48](#spin+representation#Freed99))

+-- {: .num_remark #BilinearPairingOnSpinors}
###### Remark

The last column in prop. \ref{RealSpinRepresentations} implies that in each dimension there exists a [[linear map]]

$$
  \overline{(-)}\Gamma(-) \;\colon\; S^\ast \otimes S^\ast \longrightarrow \mathbb{R}^{d-1,1}
$$

which is

1. symmetric;

1. $Spin(V)$-equivariant.

This is what in the [[physics]] literature is expressed in components by the Gamma matrices with "indices lowered" using the _[[charge conjugation matrix]]_.

=--

Before looking into this, recall the basics of [[unitary representations]] with [[real structure]]:

For reference, we here collect some basics regarding [[unitary representations]] equipped with [[real structure]].

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

1. (conjugate symmetry) $\langle v_1, v_2\rangle^\ast = \langle v_2, v_1\rangle $.

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

The following proposition uses assumptions stronger than what we have in the application to Majorana spinors (compact Lie group, positive definite hermitian form) but it nevertheless helps to see the pattern.

+-- {: .num_prop }
###### Proposition

Let $V$ be a [[complex vector space|complex]] [[finite dimensional vector space]], $\langle -,-\rangle$ some [[positive definite bilinear form|positive definite]] [[hermitian form]] on $V$, def. \ref{HermitianForms}, let $G$ be a [[compact Lie group]], and $\rho \colon G \to U(V)$ a [[unitary representation]] of $G$ on $V$. Then $\rho$ carries a real structure or quaternionc structure $\phi$ on $\rho$ (def. \ref{RealStructureOnLinearRepresentation}) precisely if it carries a symmetric or anti-symmetric, respectively, non-degenerate complex-[[bilinear map]]

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

(e.g. [Meinrenken 13, p. 81](Majorana+spinor#Meinrenken13))

We now work out in detail what def. \ref{MajoranaSpinorGeneral} comes down to in components (i.e. in terms of choices of [[linear bases]]), using standard notation and conventions from the physics literature (e.g. [Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre)).








#### Conventions and Notation

In the following we use standard notation for operations on [[matrices]] with entries in the [[complex numbers]] (and of course these matrices may in particular be complex row/column vectors, which may in particular be single complex numbers):

* $(-)^\ast$ -- componentwise [[complex conjugation]];

* $(-)^T$ -- [[transpose matrix]]

* $(-)^\dagger \coloneqq ((-)^\ast)^T = ((-)^T)^\ast$

* $A B$ for the [[matrix product]] of two matrices $A$ and $B$.

We will be discussing three different pairing operations on complex column vectors $\psi_1, \psi_2 \in \mathbb{C}^\nu$:

* $\psi_1^\dagger \psi_2$ -- the standard [[hermitian form]] on $\mathbb{C}^\nu$, this will play a purely auxiliary role.

* $\langle \psi_1,\psi_2\rangle \coloneqq \overline{\psi}_1 \psi_2 \coloneqq \psi_1^\dagger \Gamma_0 \psi_2$ -- the _Dirac pairing_, this will be the alternative [[hermitian form]] with respect to which the [[spin representation]] below is a [[unitary representation]];

* $(\psi_1,\psi_2) \coloneqq \psi_1^T C \psi_2$ -- the _Majorana pairing_ (for $C$ the [[charge conjugation matrix]]), this turns out to coincide with the Dirac pairing above _if_ $\psi_1$ is a Majorana spinor.

Then we use the following conventions on spacetime signature and the correspondig [[Clifford algebra]]:

+-- {: .num_defn #MinkowskiSpacetime}
###### Definition

We write $\mathbb{R}^{s,t}$ for the real [[vector space]] $\mathbb{R}^{s+t}$ of [[dimension]] $d = s + t$ equipped with the standard [[quadratic form]] $q$ of [[signature of a quadratic form|signature]] $(t,s)$ ("time", "space"), i.e.

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

Hence the corresponding [[metric]] is

$$
  \eta = (\eta_{a b}) \coloneqq diag(\underset{t}{\underbrace{+1 , \cdots, +1}}, \underset{s}{\underbrace{-1, \cdots, -1}})
  \,.
$$

The real [[Clifford algebra]] $Cl(s,t)$ associated with this [[inner product space]] is the $\mathbb{R}$-[[associative algebra|algebra]] [[generators and relations|generated]] from elements $\{\Gamma_a\}_{0 = 1}^{s+t-1}$ subject to the [[generators and relations|relation]]

$$
  \Gamma_a \Gamma_b + \Gamma_b \Gamma_a = 2 \eta_{a b}
  \;\;\;\;
  \forall a,b \in \{0,1,\cdots, t+s-1\}
  \,.
$$

For $n$-[[tuples]] $(a_i)_{i = 1}^n$ of indices we write

$$
  \Gamma_{a_1 \cdots a_n}
  \coloneqq
  \Gamma_{[a_1}
    \cdots
  \Gamma_{a_2]}
   \coloneqq
  \frac{1}{n!} \underset{\sigma}{\sum}
   (-1)^{\vert \sigma\vert}
  \Gamma_{a_{\sigma_1}}
   \cdots
  \Gamma_{a_{\sigma_n}}
$$

for the skew-symmetrized product of Clifford generators with these indices. In partcular if all the $a_i$ are pairwise distinct, then this is simply the plain product of generators

$$
  \Gamma_{a_1 \cdots a_n}
  =
  \Gamma_{a_1} \cdots \Gamma_{a_n}
  \;\;\;
  \text{if}
  \;
  \underset{i,j}{\forall} (a_i \neq a_j)
  \,.
$$

=--

Indices are raised with $\eta^{-1} = (\eta^{a b})$ (which of course as a [[matrix]] coincides with $(\eta_{a b})$)

$$
  \Gamma^a \coloneqq \eta^{a b} \Gamma_b
$$

+-- {: .num_defn #LorentzianSignature}
###### Definition

The case $t = 1$ is that of **Lorentzian signature**.

In this case the single [[timelike]] Clifford genrator is $\Gamma_0$ and the remaining spatial Clifford generators are $\Gamma_1, \Gamma_2, \cdots, \Gamma_{d-1}$. So then

* $\Gamma^0 = \Gamma_0$ and $\Gamma_0^2 = + 1$;

* $\Gamma^a = - \Gamma_a$ and $\Gamma_a^2 = -1$ for $a \in \{1,\cdots, d-1\}$.

=--










#### Dirac and Weyl representations
 {#DiracAndWeylRepresentations}

The following is a standard convention for the complex representation of the Clifford algebra for $\mathbb{R}^{s,1}$ ([Castellani-D'Auria-Fr&#233;, (II.7.1)](#CastellaniDAuriaFre)):

+-- {: .num_prop #CliffordAlgebraRepresentation}
###### Proposition
(**Dirac representation**)

Let $t = 1$ (Lorentzian signature, def. \ref{LorentzianSignature}) and let

$$
  d = s + 1 \in \{ 2\nu, 2 \nu + 1 \}
  \;\;\;\;
  \text{for}\, \nu \in \mathbb{N}\,,\; d\geq 4
  \,.
$$

Then there is a choice of complex linear representation of the [[Clifford algebra]] $Cl(s,1)$ (def. \ref{MinkowskiSpacetime}) on the [[complex vector space]]

$$
  V \coloneqq \mathbb{C}^{\nu}
$$

such that

1. $\Gamma_{0}$ is [[hermitian]]

1. $\Gamma_{spatial}$ is [[anti-hermitian]].

Moreover, the pairing

$$
  \langle -,-\rangle \coloneqq (-)^\dagger \Gamma_0 (-)
    \;\colon\;
  V \times V
    \longrightarrow
  \mathbb{C}
$$

is a [[hermitian form]] (def. \ref{HermitianForms}) with respect to which the resulting representation of the [[spin group]] $\exp(\omega^{a b} \Gamma_{a b})$ is [[unitary representation|unitary]]:

$$
  \Gamma_0^{-1} \exp(\omega^{a b} \Gamma_{a b})^{\dagger} \Gamma_0
  =
  \exp(\omega^{a b} \Gamma_{a b})^{-1}
  \,.
$$

These representations are called the **[[Dirac representations]]**, their elements are called **Dirac spinors**.

=--

+-- {: .proof}
###### Proof

In the case $d = 4$ consider the [[Pauli matrices]] $\{\sigma_{a}\}_{a = 0}^3$, defined by

$$
  \sigma_a x^a
  \coloneqq
  \left(
    \array{
       x^0 + x^1 & x^2 + i x^3
       \\
       x^2 - i x^3 & x^0 - x^1
    }
  \right)
  \,.
$$

Then a Clifford representation as claimed is given by setting

$$
  \Gamma_0
     \coloneqq
  \left(
    \array{
      0 & id
      \\
      id & 0
    }
  \right)
$$

$$
  \Gamma_a
    \coloneqq
  \left(
    \array{
      0 & \sigma_a
      \\
      -\sigma_a & 0
    }
  \right)
  \,.
$$

From $d = 4$ we proceed to higher dimension by [[induction]], applying the following two steps:

**odd dimensions**

Suppose a Clifford representation $\{\gamma_a\}$ as claimed has been constructed in even dimension $d = 2 \nu$.

Then a Clifford representation in dimension $d = 2 \nu + 1$ is given by taking

$$
  \Gamma_a
   \coloneqq
  \left\{
    \array{
      \gamma_a & \vert \; a \leq d - 2
      \\
      \epsilon \gamma_0 \gamma_1 \cdots \gamma_{d-2}
       & \vert\; a = d-1
    }
  \right.
$$

where

$$
  \epsilon
     =
   \left\{
     \array{
       1 & \vert \; \nu \, \text{odd}
       \\
       i & \vert \; \nu \, \text{even}
     }
   \right.
   \,.
$$

**even dimensions**

Suppose a Clifford representation $\{\gamma_a\}$ as claimed has been constructed in even dimension $d = 2 \nu$.

Then a corresponding representation in dimension $d+2$ is given by setting


$$
  \Gamma_{a \lt d}
    \coloneqq
  \left(
    \array{
      0 & \gamma_a
      \\
      \gamma_a & 0
    }
  \right)
  \;\;\,,
  \;\;\;
  \Gamma_{d}
    =
  \left(
    \array{
      0 & id
      \\
      -id & 0
    }
  \right)
  \;\;\,,
  \;\;\;
  \Gamma_{d+1}
    =
  \left(
    \array{
       i \mathrm{id} & 0
       \\
       0 & -i \mathrm{id}
    }
  \right)
  \,.
$$

Finally regarding the statement that this gives a [[unitary representation]]:

That $\langle -,-\rangle \coloneqq (-)^\dagger \Gamma_0 (-)$ is a [[hermitian form]] follows since $\Gamma_0$ obtained by the above construction is a [[hermitian matrix]].

Let $a,b \in \{1, \cdots, d-1\}$ be spacelike and distinct indices. Then by the above we have

$$
  \begin{aligned}
    \Gamma_0^{-1} (\Gamma_a \Gamma_b)^\dagger \Gamma_0
    & =
    \Gamma_0^{-1} \Gamma_0 (\Gamma_b^\dagger \Gamma_a^\dagger)
    \\
    & = (-\Gamma_b) (-\Gamma_a)
    \\
    & = \Gamma_b \Gamma_a
    \\
    & = - \Gamma_a \Gamma_b
  \end{aligned}
$$

and

$$
  \begin{aligned}
    \Gamma_0^{-1} (\Gamma_0 \Gamma_a)^\dagger
    & =
    - \Gamma_0^{-1} \Gamma_0 \Gamma_a^\dagger \Gamma_0^\dagger
    \\
    & =
      - (- \Gamma_a) (\Gamma_0)
    \\
    & = \Gamma_a \Gamma_0
    \\
    & = - \Gamma_0 \Gamma_a
  \end{aligned}
  \,.
$$

This means that the exponent of $\exp(\omega^{a b} \Gamma_a \Gamma_b)$ is an [[anti-hermitian matrix]], hence that exponential is a [[unitary operator]].

=--

+-- {: .num_defn #WeylRepresentation}
###### Definition
(**Weyl representation**)

Since by prop. \ref{CliffordAlgebraRepresentation} the Dirac representations in dimensions $d = 2\nu$ and $d+1 = 2\nu+1$ have the same underlying complex vector space, the element

$$
  \Gamma_{d}
    \propto
  \Gamma_0 \Gamma_1 \cdots \Gamma_{d-1}
$$

acts $Spin(d-1,1)$-invariantly on the representation space of the Dirac $Spin(d-1,1)$-representation. Therefore this representation decomposes as a [[direct sum]]

$$
  V = V_+ \oplus V_-
$$

of the [[eigenspaces]] $V_{\pm}$ of $\Gamma_d$ of [[eigenvalue]] $\pm i$, respectively. These $V_{\pm}$ are called the two **[[Weyl representations]]** of $Spin(d-1,1)$. An element of these is called a **chiral spinor** ("left handed", "right handed", respectively). The operator $\Gamma_d$ then is called the **chirality operator**.

Analogously, since in odd dimensions there is no further decomposition, the Dirac representation for odd $d$ is also called a Weyl representation.

=--

+-- {: .num_remark}
###### Remark

Beware that in the context of def. \ref{WeylRepresentation}, the chirality operator $\Gamma_{d}$ is traditionally denoted $\Gamma_{d+1}$, i.e.

* $\{\Gamma_0,\cdots,\Gamma_{d-1}\}$ -- Clifford algebra for $Spin(d-1,1)$;

* $\Gamma_{d+1}$ -- Chirality operator.

This is partiularly common for $d= 4$, in which case the physics literaure usually refers to the chirality operator as "the $\Gamma_5$-matrix".

Clearly this notational convention has its pitfalls once one considers spinors in various dimensions. Nevertheless, even then the convention is often still followed (e.g. [Castellani-D'Auria-Fr&#233;, section (II.7.11) and top of p. 523](#CastellaniDAuriaFre)).

=--

+-- {: .num_defn #DiracConjugate}
###### Definition

For a Clifford algebra representation on $\mathbb{C}^\nu$ as in prop. \ref{CliffordAlgebraRepresentation}, we write

$$
  \overline{(-)}
  \coloneqq
  (-)^\dagger \Gamma_0
  \;\colon\;
  Mat_{\nu \times 1}(\mathbb{C})
    \longrightarrow
  Mat(1 \times \nu)(\mathbb{C})
$$

for the map from complex column vectors to complex row vectors which is hermitian congugation $(-)^\dagger = ((-)^\ast)^T$ followed by matrix multiplication with $\Gamma_0$ from the right.

This operation is called **Dirac conjugation**.

In terms of this the [[hermitian form]] from prop. \ref{CliffordAlgebraRepresentation} (Dirac pairing) reads

$$
  \langle -,-\rangle = \overline{(-)}(-)
  \,.
$$

=--

+-- {: .num_prop #CliffordRepresentationIsDiracSelfConjugate}
###### Proposition

The operator adjoint $\overline{A}$ of a $\nu \times \nu$-matrix $A$ with respect to the Dirac pairing of def. \ref{DiracConjugate}, characterized by

$$
  \langle A (-), (-)\rangle
  =
  \langle   - , \overline{A} -\rangle
  \;\;\;\text{and} \;\;\;
  \langle  -, A -\rangle
  =
  \langle \overline{A} - ,  -\rangle
$$

is given by

$$
  \overline{A} = \Gamma_0^{-1} A^\dagger \Gamma_0
  \,.
$$

All the Clifford generators from prop. \ref{CliffordAlgebraRepresentation} are Dirac self-conjugate in that

$$
  \overline{\Gamma}_a = \Gamma_a
  \,.
$$

=--

+-- {: .proof}
###### Proof

For the first claim consider

$$
  \begin{aligned}
    \langle A \psi_1,  \psi_2\rangle
    & =
    \psi_1^\dagger A^\dagger \Gamma_0  \psi_2
    \\
    & =
    \psi_1^\dagger \Gamma_0 (\Gamma_0^{-1} A^\dagger \Gamma_0) \psi_2
    \\
    & =
    \langle \psi_1, (\Gamma_0^{-1} A \Gamma_0)\psi_2\rangle
  \end{aligned}
  \,.
$$

and

$$
  \begin{aligned}
    \langle \psi_1, A \psi_2\rangle
    & =
    \psi_1^\dagger \Gamma_0 A \psi_2
    \\
    & =
    \psi_1^\dagger \Gamma_0 A \Gamma_0^{-1} \Gamma_0 \psi_2
    \\
    & =
    ( (\Gamma_0^{-1})^\dagger A^\dagger (\Gamma_0)^\dagger \psi_1 )^\dagger \Gamma_0 \psi_2
    \\
    & =
    ( \Gamma_0^{-1} A^\dagger \Gamma_0 \psi_1 )^\dagger \Gamma_0 \psi_2
    \\
    &=
    \langle \overline{A} \psi_1, \psi_2\rangle
  \end{aligned}
  \,,
$$

where we used that $\Gamma_0^{-1} = \Gamma_0$ (by def. \ref{LorentzianSignature}) and $\Gamma_0^\dagger = \Gamma_0$ (by prop. \ref{CliffordAlgebraRepresentation}).

Now for the second claim, use def. \ref{LorentzianSignature} and prop. \ref{CliffordAlgebraRepresentation} to find

$$
  \begin{aligned}
     \overline{\Gamma}_0
     & =
     \Gamma_0^{-1}\Gamma_0^\dagger \Gamma_0
     \\
     & = \Gamma_0^{-1} \Gamma_0 \Gamma_0
     \\
     & =
     \Gamma_0
   \end{aligned}
$$

and

$$
  \begin{aligned}
    \overline{\Gamma}_{spatial}
    & =
    \Gamma_0^{-1} \Gamma_{spatial}^\dagger\Gamma_0
    \\
    &=
    - \Gamma_0^{-1} \Gamma_{spatial} \Gamma_0
    \\
    & = + \Gamma_0^{-1} \Gamma_0 \Gamma_{spatial}
    \\
    &= \Gamma_{spatial}
  \end{aligned}
  \,.
$$

=--











#### Charge conjugation matrix
 {#ChargeConjugationMatrix}

+-- {: .num_prop #ChargeConjugationMatrix}
###### Proposition

Given the Clifford algebra representation of the form of prop. \ref{CliffordAlgebraRepresentation}, consider the equation

$$
  C_{(\pm)} \Gamma_a  = \pm \Gamma_a^T C_{(\pm)}
$$

for $C_{(\pm)} \in Mat_{\nu \times n}(\mathbb{C})$.

In even dimensions $d = 2 \nu$ then both these equations have a solution, wheras in odd dimensions $d = 2 \nu + 1$ only one of them does (alternatingly, starting with $C_{(+)}$ in dimension 5). Either $C_{(\pm)}$ is called the _[[charge conjugation matrix]]_.

Moreover, all $C_{(\pm)}$ may be chosen to be real matrices

$$
  (C_{(\pm)})^\ast = C_{(\pm)}
$$

and in addition they satisfy the following relations:

| $d$ |   |    |
|-----|---|----|
| 4 | $C_{(+)}^T = -C_{(+)}$; $C_{(+)}^2 = -1$ | $C_{(-)}^T = -C_{(+)}$; $C_{(-)}^2 = -1$ |
| 5 | $C_{(+)}^T = -C_{(+)}$; $C_{(+)}^2 = -1$  |  |
| 6 | $C_{(+)}^T = -C_{(+)}$; $C_{(+)}^2 = -1$  | $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = 1$ |
| 7 |   |  $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = 1$ |
| 8 | $C_{(+)}^T = C_{(+)}$; $C_{(+)}^2 = 1$ | $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = 1$ |
| 9 | $C_{(+)}^T = C_{(+)}$; $C_{(+)}^2 = 1$ |  |
| 10 | $C_{(+)}^T = C_{(+)}$; $C_{(+)}^2 = 1$ |  $C_{(-)}^T = -C_{(-)}$; $C_{(-)}^2 = -1$ |
| 11 |   |  $C_{(-)}^T = -C_{(-)}$; $C_{(-)}^2 = -1$ |

=--

{#beware} (This is for instance in [Castellani-D'Auria-Fr&#233;, section (II.7.2), table (II.7.1)](#CastellaniDAuriaFre), but beware that there $C_{(-)}$ in $d = 10, 11$ is claimed to be symmetric, while instead it is anti-symmetric as shown above, see [van Proeyen 99, table 1](#VanProeyen99), [Laenen, table E.3](#GammaMatrices)).

+-- {: .num_remark #TransposeChargeConjugation}
###### Remark


Prop. \ref{ChargeConjugationMatrix} implies that for all $C_{(\pm)}$ listed there then

$$
  C^{-1} = C^T
  \,.
$$

This implies in all cases that

$$
  \Gamma_a C_{(\pm)}^T = \pm C_{(\pm)}^T \Gamma_a^T
  \,.
$$

=--













#### Majorana representations and Real structure


+-- {: .num_prop #MajoranaConjugationIsRealStructure}
###### Proposition

For $d \in \{4,8,9,10,11\}$, let $V = \mathbb{C}^\nu$ as above. Write $\{\Gamma_a\}$ for a Dirac representation according to prop. \ref{CliffordAlgebraRepresentation}, and write

$$
  C
  \coloneqq
  \left\{
    \array{
      C_{(-)} & \text{for}\; d = 4
      \\
      C_{(+)} & \text{for}\; d = 8
      \\
      C_{(+)} & \text{for}\; d = 9
      \\
      C_{(+)} or C_{(-)} & \text{for}\; d = 10
      \\
      C_{(-)} & \text{for}\; d = 11
    }
  \right.
$$

for the choice of [[charge conjugation matrix]] from prop. \ref{ChargeConjugationMatrix} as shown. Then the function

$$
  J \colon V \longrightarrow V
$$

given by

$$
  \psi \mapsto C \Gamma_0^T \psi^\ast
$$

is a [[real structure]] (def. \ref{RealStructureOnLinearRepresentation}) for the corresponding complex [[spin representation]] on $\mathbb{C}^\nu$.

=--

+-- {: .proof}
###### Proof

The conjugate linearity of $J$ is clear, since $(-)^\ast$ is conjugate linear and [[matrix multiplication]] is complex linear.

To see that $J$ squares to +1 in the given dimensions: Applying it twice yields,

$$
  \begin{aligned}
    J^2 \psi &=
     C \Gamma_0^T (C \Gamma_0^T\psi^\ast)^\ast
     \\
     & =
     C \Gamma_0^T C \Gamma_0^\dagger \psi
     \\
     &=
     C \underset{= \pm C \Gamma_0}{\underbrace{\Gamma_0^T C}} \Gamma_0 \psi
     \\
     & = \pm C_{(\pm)}^2 \Gamma_0^2 \psi
     \\
     & = \pm C_{(\pm)}^2 \psi
  \end{aligned}
  \,,
$$

where we used $\Gamma_0^\dagger = \Gamma_0$ from prop. \ref{CliffordAlgebraRepresentation}, $C^\ast = \ast$ from prop. \ref{ChargeConjugationMatrix} and then the defining equation of the [[charge conjugation matrix]] $\Gamma_a^T C_{(\pm)} = \pm C_{(\pm)} \Gamma_a$ (def. \ref{ChargeConjugationMatrix}), finally the defining relation $\Gamma_0^2 = +1$.

Hence this holds whenever there exists a choice $C_{(\pm)}$ for the charge conjugation matrix with $C_{(\pm)}^2 = \pm 1$. Comparison with the table from prop. \ref{ChargeConjugationMatrix} shows that this is the case in $d = 4,8,9,10,11$.

Finally to see that $J$ is spin-invariant (in [Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre) this is essentially (II.2.29)), it is sufficient to show for distinct indices $a,b$, that

$$
  J(\Gamma_a \Gamma_b \psi)
  =
  \Gamma_a \Gamma_b J(\psi)
  \,.
$$

First let $a,b$ both be spatial. Then

$$
  \begin{aligned}
    J(\Gamma_a \Gamma_b \psi)
    & =
    C \Gamma_0^T \Gamma_a^\ast \Gamma_b^\ast \psi^\ast
    \\
    & =
    C \Gamma_0^T (-\Gamma_a^T)(-\Gamma_b^T) \psi^\ast
    \\
    & =
    C \Gamma_0^T \Gamma_a^T \Gamma_b^T \psi^\ast
    \\
    & =
    C  \Gamma_a^T \Gamma_b^T \Gamma_0^T \psi^\ast
    \\
    & =
    \Gamma_a \Gamma_b C \Gamma_0^T \psi^\ast
    \\
    & =
    \Gamma_a \Gamma_b J(\psi)
  \end{aligned}
  \,.
$$

Here we first used that $\Gamma_{spatial}^\dagger = -\Gamma_{spatial}$ (prop. \ref{CliffordAlgebraRepresentation}), hence that $\Gamma_{spatial}^\ast = - \Gamma_{spatial}^T$ and then that $\Gamma_0$ anti-commutes with the spatial Clifford matrices, hence that $\Gamma_0^T$ anti-commutes the the transposeso fthe spatial Clifford matrices. Then we used the defining equation for the [[charge conjugation matrix]], which says that passing it through a Gamma-matrix yields a transpose, up to a global sign. That global sign cancels since we pass through two Gamma matrices.

Finally, that the same conclusion holds for $\Gamma_{spatial} \Gamma_{spatial}$ replaced by $\Gamma_0 \Gamma_{spatial}$: The above reasoning applies with two extra signs picked up: one from the fact that $\Gamma_0$ commutes with itself, one from the fact that it is hermitian, by prop. \ref{CliffordAlgebraRepresentation}. These two signs cancel:

$$
  \begin{aligned}
    J(\Gamma_0 \Gamma_a \psi)
    & =
    C \Gamma_0^T \Gamma_0^\ast \Gamma_a^\ast \psi^\ast
    \\
    & =
    C \Gamma_0^T (+\Gamma_0^T)(-\Gamma_a^T) \psi^\ast
    \\
    & =
    - C \Gamma_0^T \Gamma_0^T \Gamma_a^T \psi^\ast
    \\
    & =
    + C \Gamma_0^T \Gamma_a^T \Gamma_0^T \psi^\ast
    \\
    & = \Gamma_0 \Gamma_a \Gamma_0^T \psi^\ast
    \\
    &= \Gamma_0 \Gamma_a J(\psi)
  \end{aligned}
  \,.
$$


=--

+-- {: .num_defn #MajoranaRepresentation}
###### Definition

Prop. \ref{MajoranaConjugationIsRealStructure} implies that given a [[Dirac representation]] (prop. \ref{CliffordAlgebraRepresentation}) $V$, then the real subspace $S \hookrightarrow V$ of real elements, i.e. elements $\psi$ with $J \psi = \psi$ according to prop. \ref{MajoranaConjugationIsRealStructure} is a [[sub-representation]]. This is called the **Majorana representation** inside the Dirac representation (if it exists).

=--

+-- {: .num_prop #RealStructureAntiCommutesWithSingleCliffordGenerator}
###### Proposition

If $C = C_{(\pm)}$ is the [[charge conjugation matrix]] according to prop. \ref{ChargeConjugationMatrix}, then the real structure $J$ from prop. \ref{MajoranaConjugationIsRealStructure} commutes or anti-commutes with the action of _single_ Clifford generators, according to the subscript of $C = C_{(\pm)}$:

$$
  J(\Gamma_a(-)) = \pm \Gamma_a J(-)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is same kind of computation as in the proof prop. \ref{MajoranaConjugationIsRealStructure}. First let $a$ be a spatial index, then we get

$$
  \begin{aligned}
    J(\Gamma_a \psi)
    & =
    C \Gamma_0^T \Gamma_a^\ast  \psi^\ast
    \\
    & =
    C \Gamma_0^T (-\Gamma_a^T) \psi^\ast
    \\
    & =
    + C \Gamma_a^T \Gamma_0^T \psi^\ast
    \\
    & =
    \epsilon C^T \Gamma_a^T \Gamma_0^T
    \\
    & =
    \pm \epsilon \Gamma_a C^T \Gamma_0^T \psi^\ast
    \\
    & = \pm \epsilon^2 \Gamma_a C \Gamma_0^T \psi^\ast
    \\
    & = \pm \Gamma_a J(\psi)
  \end{aligned}
  \,,
$$

where, by comparison with the table in prop. \ref{ChargeConjugationMatrix}, $\epsilon$ is the sign in $C^T = \epsilon C$, which cancels out, and the remaining $\pm$ is the sign in $C = C_{(\pm)}$, due to remark \ref{TransposeChargeConjugation}.

For the timelike index we similarly get:

$$
  \begin{aligned}
    J(\Gamma_0 \psi)
    & =
    C \Gamma_0^T \Gamma_0^\ast  \psi^\ast
    \\
    & =
    + C \Gamma_0^T \Gamma_0^T \psi^\ast
    \\
    & =
    \epsilon C^T \Gamma_0^T \Gamma_0^T
    \\
    & =
    \pm \epsilon \Gamma_0 C^T \Gamma_0^T \psi^\ast
    \\
    & = \pm \Gamma_0 C \Gamma_0^T \psi^\ast
    \\
    & = \pm \Gamma_0 J(\psi)
  \end{aligned}
  \,.
$$


=--


We record some immediate consequences:

+-- {: .num_prop #ComplexBilinearFormInducedFromMajoranaStructure}
###### Proposition

The complex [[bilinear form]]

$$
  (-,-)
   \coloneqq
  \langle J(-),(-)\rangle
$$

induced from the [[real structure]] $J$ of prop. \ref{MajoranaConjugationIsRealStructure} from the [[hermitian form]] $\langle -,-\rangle$ of prop. \ref{CliffordAlgebraRepresentation} is that represented by the [[charge conjugation matrix]] of prop. \ref{ChargeConjugationMatrix}

$$
  (-,-)
   =
  (-)^T C (-)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By direct unwinding of the various definitions and results from above:

$$
  \begin{aligned}
    \langle J(\psi_1),\psi_2 \rangle
     &=
     \langle C \Gamma_0^T\psi_1^\ast, \psi_2\rangle
     \\
     & =
     (C \Gamma_0^T \psi_1^\ast)^\dagger \Gamma_0 \psi_2
     \\
     & = \psi_1^T C^\dagger \Gamma_0^\ast \Gamma_0 \psi_2
     \\
     & = \psi_1^T C \psi_2
  \end{aligned}
  \,.
$$

=--

+-- {: .num_defn #MajoranaConjugation}
###### Definition

For a Clifford algebra representation on $\mathbb{C}^\nu$ as in prop. \ref{CliffordAlgebraRepresentation}, then the map

$$
  (-)^T C
  \;\colon\;
  Mat_{\nu \times 1}(\mathbb{C})
    \longrightarrow
  Mat(1 \times \nu)(\mathbb{C})
$$

(from complex column vectors to complex row vectors) which is given by transposition followed by [[matrix multiplication]] from the right by the [[charge conjugation matrix]] according to prop. \ref{MajoranaConjugationIsRealStructure} is called the
**Majorana conjugation**.


=--



+-- {: .num_prop #TheMajoranaConditionInComponents}
###### Proposition

In dimensions $d = 4,8,9,10,11$ a spinor $\psi \in \mathbb{C}^{\nu}$ is Majorana according to def. \ref{MajoranaSpinorGeneral} with respect to the [[real structure]] from prop. \ref{MajoranaConjugationIsRealStructure}, precisely if

$$
  \psi = C \Gamma_0^T \psi^\ast
$$

(as e.g. in [Castellani-D'Auria-Fr&#233;, (II.7.22)](#CastellaniDAuriaFre)),

This is equivalent to the condition that the Majorana conjugate (def. \ref{MajoranaConjugation}) coincides with  the Dirac conjugate (def. \ref{DiracConjugate}) on $\psi$:

$$
  \psi^T C = \psi^\dagger \Gamma_0
  \,,
$$

which in turn is equivalent to the condition that

$$
  (\psi,-) = \langle \psi,-\rangle
  \,,
$$

where on the left we have the complex bilinear form of prop. \ref{ComplexBilinearFormInducedFromMajoranaStructure} and on the right the [[hermitian form]] from prop. \ref{CliffordAlgebraRepresentation}.

=--

+-- {: .proof}
###### Proof

The first statement is immediate. The second follows by applying transpose to the first equation, and using that $C^{-1} = C^T$ (from prop. \ref{ChargeConjugationMatrix}). Finally the last statement follows from this by prop. \ref{ComplexBilinearFormInducedFromMajoranaStructure}.

=--













#### Majorana-Weyl spinors


+-- {: .num_defn #WeylMajorana}
###### Definition

In the even dimensions among those dimensions $d$ for which the Majorana projection operator (real structure) $J$ exists (prop. \ref{MajoranaConjugationIsRealStructure}) also the chirality projection operator $\Gamma_{d}$ exists (def. \ref{WeylRepresentation}). Then we may ask that a Dirac spinor $\psi$ is both Majorana, $J(\psi) = \psi$, as well as Weyl, $\Gamma_d \psi = \pm i \psi$. If this is the case, it is called a **Majorana-Weyl spinor**, and the [[sub-representation]] these form is a called a _Majorana-Weyl representation_.

=--

+-- {: .num_prop #WeylMajoranaInLorentzian10d}
###### Proposition

In Lorentzian signature (def. \ref{LorentzianSignature}) for $4 \leq d \leq 11$, then Majorana-Weyl spinors (def. \ref{WeylMajorana}) exist precisely only in $d = 10$.

=--

+-- {: .proof}
###### Proof

According to prop. \ref{MajoranaConjugationIsRealStructure} Majorana spinors in the given range exist for $d \in \{4,8,9,10,11\}$. Hence the even dimensions among these are $d \in \{4,8,10\}$.

Majorana-Weyl spinors clearly exist precisely if the two relevant projection operators in these dimensions commute with each other, i.e. if

$$
  [J, \epsilon \Gamma_0 \cdots \Gamma_{d-1}] = 0
$$

where

$$
  \epsilon
     =
   \left\{
     \array{
       1 & \vert \; \nu \, \text{odd}
       \\
       i & \vert \; \nu \, \text{even}
     }
   \right.
   \,.
$$

with $d = 2\nu$ (from the proof of prop. \ref{CliffordAlgebraRepresentation}).

By prop. \ref{RealStructureAntiCommutesWithSingleCliffordGenerator} all the $\Gamma_a$ commute or all anti-commute with $J$. Since the product $\Gamma_0 \cdots \Gamma_{d-1}$ contains an even number of these, it commutes with $J$. It follows that $J$ commutes with $\Gamma_d$ precisely if it commutes with $\epsilon$. Now since $J$ is conjugate-linear, this is the case precisely if $\epsilon = 1$, hence precisely if $d = 2\nu$ with $\nu$ odd.

This is the case for $d = 10 = 2 \cdot 5$, but not for $d = 8 = 2 \cdot 4$ neither for $d = 4 = 2 \cdot 2$.

=--












####  The spinor bilinear pairing to antisymmetric $p$-tensors
 {#TheSpinorPairingToVectors}

We now discuss, in the component expressions established [above](#InComponents), the complex bilinear pairing operations that take a pair of Majorana spinors to a [[vector]], and more generally to an antisymmetric rank $p$-[[tensor]]. These operations are all of the form

$$
  \psi
    \mapsto
  \epsilon \, \overline{\psi} \Gamma^{a_1 \cdots a_p} \psi
  \,,
$$

where $\epsilon \in \mathbb{C}$ is some prefactor, constrained such as to make the whole expression be real, hence such as to make this the components of an element in $\wedge^p \mathbb{R}^{d-1,1}$.


For a $Spin(d-1,1)$ representation $V$ as in prop. \ref{CliffordAlgebraRepresentation}, with real/Majorana structure as in prop. \ref{MajoranaConjugationIsRealStructure}, write

$$
  S \hookrightarrow V
$$

for the subspace of Majorana spinors, regarded as a real vector space.

Recall, by prop. \ref{TheMajoranaConditionInComponents}, that on Majorana spinors the Majorana conjugate $(-)^T C$ coincides with the Dirac conjugate $\overline{(-)} \coloneqq (-)^\dagger \Gamma_0 $. Therefore we write $\overline{(-)}$ in the following for the conjugation of Majorana spinors, unambiguously defined.


+-- {: .num_defn #SpinorToVectorBilinearPairing}
###### Definition

For a $Spin(d-1,1)$ representation $V$ as in prop. \ref{CliffordAlgebraRepresentation}, with real/Majorana structure as in prop. \ref{MajoranaConjugationIsRealStructure}, let

$$
  \overline{(-)}\Gamma (-)
    \;\colon\;
  S \times S
   \longrightarrow
  \mathbb{R}^{d-1,1}
$$

be the function that takes Majorana spinors $\psi_1$, $\psi_2$ to the vector with components

$$
  \overline{\psi}_1\Gamma^a \psi_2
    \coloneqq
  \psi_1^T C \Gamma^a \psi_2
  \,.
$$

=--


+-- {: .num_prop #SpinorToVectorPairing}
###### Proposition

The pairing in def. \ref{SpinorToVectorBilinearPairing} is

1. symmetric:

   $$
     \overline{\psi}_1 \Gamma \psi_2
       =
     \overline{\psi}_2 \Gamma \psi_1
   $$

1. component-wise real-valued (i.e. it indeed takes values in $\mathbb{R}^d \subset \mathbb{C}^d$);

1. $Spin(d-1,1)$-equivariant: for $g \in Spin(d-1,1)$ then

   $$
     \overline{g(-)}\Gamma(g(-))
       =
     g(\overline{(-)}\Gamma(-))
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Regarding the first point, we need to show that for all $a$ then $C \Gamma_a$ is a symmetric matrix. Indeed:

$$
  \begin{aligned}
     (C \Gamma_a)^T
       & =
     \Gamma_a^T C^T
      \\
      & = \pm \Gamma_a^T C
      \\
      & = \pm \pm C \Gamma_a
      \\
      & = C \Gamma_a
  \end{aligned}
  \,,
$$

where the first sign picked up is from $C^T = \pm C$, while the second is from $\Gamma_a^T C = \pm C \Gamma_a$ (according to prop. \ref{ChargeConjugationMatrix}). Imposing the condition in prop. \ref{MajoranaConjugationIsRealStructure} one finds that these signs agree, and hence cancel out.

(In [van Proeyen99](#VanProeyen99) this is part of table 1, in ([Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre)) this is implicit in equation (II.2.32a).)

With this the second point follows together with the relation $\psi^T C = \psi^\dagger \Gamma_0$ for Majorana spinors $\psi$ (prop. \ref{TheMajoranaConditionInComponents}) and using the conjugate-symmetry of the [[hermitian form]] $\langle -,-\rangle = (-)^\dagger \Gamma_0 (-)$ as well as the hermiticity of $\Gamma_0 \Gamma_a$ (both from prop. \ref{CliffordAlgebraRepresentation}):

$$
  \begin{aligned}
    (\overline{\psi}_1 \Gamma_a \psi_2)^\ast
    &=
    (\psi_1^T C \Gamma_a \psi_2)^\ast
    \\
    & =
    (\psi_1^\dagger \Gamma_0 \Gamma^a \psi_2)^\ast
    \\
    & =
    \psi_2^\dagger (\Gamma_0 \Gamma^a)^\dagger \psi_1
    \\
    & =
    \psi_2^\dagger \Gamma_0 \Gamma^a \psi_1
    \\
    & =
    \overline{\psi}_2 \Gamma_a \psi_1
  \end{aligned}
  \,.
$$

Regarding the third point: By prop. \ref{MajoranaConjugationIsRealStructure} and prop. \ref{ComplexBilinearFormInducedFromMajoranaStructure} we get

$$
  \begin{aligned}
    (g(\psi_1), \Gamma_a g(\psi_2))
    & =
    \langle g(\psi_1),\Gamma_a g(\psi_2)\rangle
    \\
    & =
     \langle \psi_1, (\Gamma_0^{-1}g^\dagger\Gamma_0) \Gamma_a g \psi_2 \rangle
    \\
    & = \langle \psi_1 (g^{-1} \Gamma_a g) \psi_2 \rangle
  \end{aligned}
  \,,
$$

where we used that $\Gamma_0^{-1}(-)^\dagger \Gamma_0$ is the adjoint with respect to the hermitian form $\langle -,-\rangle = (-)^\dagger \Gamma_0 (-)$ (prop. \ref{CliffordRepresentationIsDiracSelfConjugate}) and that $g$ is unitary with respect to this hermitian form by prop. \ref{CliffordAlgebraRepresentation}.

(In ([Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre)) this third statement implicit in equations (II.2.35)-(II.2.39).)

=--

+-- {: .num_remark #SuperPoincareOutlook}
###### Remark

Proposition \ref{SpinorToVectorPairing} implies that adding a copy of $S$ to the [[Poincaré Lie algebra]] in odd degree, then the pairing of def. \ref{SpinorToVectorBilinearPairing} is a consistent extension of the [[Lie bracket]] of the latter to a [[super Lie algebra]]. This is the _[[super Poincaré Lie algebra]]_.

=--

+-- {: .num_defn #SpinorToRank2TensorBilinearPairing}
###### Definition

For a $Spin(d-1,1)$ representation $V$ as in prop. \ref{CliffordAlgebraRepresentation}, with real/Majorana structure as in prop. \ref{MajoranaConjugationIsRealStructure}, let

$$
  \overline{(-)}\Gamma\Gamma (-)
    \;\colon\;
  S \times S
   \longrightarrow
  \wedge^2 \mathbb{C}^d
$$

be the function that takes Majorana spinors $\psi_1$, $\psi_2$ to the skew-symmetric rank 2-tensor with components

$$
  \overline{\psi}_1\Gamma^{a b} \psi_2
    \coloneqq
  i \psi_1^T C \tfrac{1}{2}(\Gamma^a \Gamma^b - \Gamma^b \Gamma^a) \psi_2
  \,,
$$


=--


+-- {: .num_prop #RealityOfTheSpinorPairingtoBivectors}
###### Proposition

For $\psi_1 = \psi_2 = \psi$ then the pairing in prop. \ref{SpinorToRank2TensorBilinearPairing} is real

$$
  \underset{a,b}{\forall}
  \;\;\;\;
  i \overline{\psi} \Gamma^{a b} \psi \in \mathbb{R} \subset \mathbb{C}
$$

and $Spin(d-1,1)$-equivariant.

=--

+-- {: .proof}
###### Proof

The equivariance follows exactly as in the proof of prop. \ref{SpinorToVectorPairing}.

The reality is checked by direct computation as follows:

$$
  \begin{aligned}
    (\overline{\psi}_1 \Gamma_a \Gamma_b \psi_2)^\ast
    & =
    (\psi_1^\dagger \Gamma_a \Gamma_b \psi_2)^\ast
    \\
    & =
    \psi_2^\dagger (\Gamma_0 \Gamma_a \Gamma_b)^\dagger \psi_1
    \\
    & =
    -\langle \psi_2^\dagger \Gamma_0 \Gamma_a \Gamma_b \psi_1 \rangle
    \\
    & =
    -\overline{\psi}_2 \Gamma_a \Gamma_b \psi_1
  \end{aligned}
  \,,
$$

where for the identification $(\Gamma_0 \Gamma_a \Gamma_b)^\dagger = - \Gamma_0 \Gamma_a \Gamma_b$ we used the properties in prop. \ref{CliffordAlgebraRepresentation}.

Hence for $\psi_1 = \psi_2$ then

$$
  (\overline{\psi} \Gamma_a \Gamma_b \psi)^\ast
  =
  -
  \overline{\psi} \Gamma_a \Gamma_b \psi
$$

and so this sign cancels against the sign in $i^\ast = -i$.

=--

Generally:

+-- {: .num_prop }
###### Proposition

The following pairings are real and $Spin(d-1,1)$-equivariant:

$$
  \begin{aligned}
    & \overline{\psi} \Gamma_a \psi
    \\
    i & \overline{\psi}\Gamma_{a_1 a_2} \psi
    \\
    i & \overline{\psi} \Gamma_{a_1 a_2 a_3} \psi
    \\
     & \overline{\psi} \Gamma_{a_1 \cdots a_4} \psi
    \\
     & \overline{\psi} \Gamma_{a_1 \cdots a_5} \psi
    \\
    i  & \overline{\psi} \Gamma_{a_1 \cdots a_6} \psi
    \\
    i  & \overline{\psi} \Gamma_{a_1 \cdots a_7} \psi
    \\
    & \vdots
  \end{aligned}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The equivariance follows as in the proof of prop. \ref{SpinorToVectorPairing}.

Regarding reality:

Using that all the $\Gamma_a$ are hermitian with respect $\overline{(-)}(-)$ (prop. \ref{CliffordRepresentationIsDiracSelfConjugate}) we have

$$
  \begin{aligned}
    \left(
      \overline{\psi}
       \Gamma_{a_1 \cdots a_p}
      \psi
    \right)^\ast
    & =
    \overline{\psi}
      \Gamma_{a_p \cdots a_1}
    \psi
    \\
    &=
    (-1)^{p(p-1)/2}
    \overline{\psi}
      \Gamma_{a_1 \cdots a_p}
    \psi
  \end{aligned}
  \,.
$$


=--











#### Spacetime supersymmetry: Super-Poincar&#233; and super-Minkowski
 {#Supersymmetry}

Every real spin representation of $Spin(d-1,1)$ induces a [[super Lie algebra]] [[Lie algebra extension|extension]] of the [[Poincaré Lie algebra]] $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ in that dimension, i.e. of the Lie algebra of the [[isometry group]] of the [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}) in that dimension.

Since we may recover a [[Minkowski spacetime]] from its [[Poincaré Lie algebra]] as the (vector space underlying the) [[coset]] of the [[Poincaré Lie algebra]] by the Lie algebra $\mathfrak{so}(d-1,1)$ of the [[spin group]] (the [[orthogonal Lie algebra]] in Lorentian signature)

$$
  \mathbb{R}^{d-1,1}
   \simeq
  \mathfrak{Iso}(\mathbb{R}^{d-1,1})/\mathfrak{so}(d-1,1)
$$

(namely as the Lie algebra of translations along itself), every [[super Lie algebra]] [[extension of Lie algebras|extension]] of the [[Poincaré Lie algebra]] defines a [[super Lie algebra]] [[extension of Lie algebras|extension]] of Minkowski spacetime. These extensions are the [[super Minkowski spacetimes]] $\mathbb{R}^{d-1,1\vert N}$ of the following definition, and this justifies the following notation:

+-- {: .num_defn #SuperMinkowskiSpacetime}
###### Definition

Let $d \in \mathbb{N}$ and let $N \in Rep(Spin(d-1,1))$ be a real spin representation, hence a [[direct sum]] of Majorana representations (def. \ref{MajoranaRepresentation}) and/or Majorana-Weyl representations (def. \ref{WeylMajorana}) (or tensor product of two symplectic Majorana representations...).

We define the corresponding **[[super Poincaré Lie algebra]]**

$$
  \mathfrak{Iso}(\mathbb{R}^{d-1,1|N})
$$

equivalently in terms of its [[Chevalley-Eilenberg algebra]]: $CE(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$ (a $\mathbb{N} \times \mathbb{Z/2}$-bigraded [[dg-algebra]], see at _[[signs in supergeometry]]_).

This is generated on

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

where $a \in \{0,1, \cdots, d-1\}$ is a spacetime index, and where $\alpha$ is an index ranging over a basis of the chosen Majorana spinor representation $N$.

The CE-differential is defined as follows

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

and

$$
  d_{CE} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

(which so far is the differential for the [[semidirect product]] of the [[Poincaré Lie algebra]] [[action|acting]] on the given [[Majorana spinor]] representation)

and

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \overline{\psi} \Gamma^a \psi
$$

where on the right we have the spinor-to-vector pairing in $N$ (def. \ref{SpinorToVectorBilinearPairing}).

That this is indeed a [[super Lie algebra]] follows from the fact that the [[Poincaré Lie algebra]] is a [[Lie algebra]] and the fact that the spinor-to-vector pairing is symmetric (which makes it qualify as the odd-odd component of a super-Lie algebra) and $Spin(d-1,1)$-equivariant (which is seen to be the super-[[Jacobi identity]] for it), all according to prop. \ref{SpinorToVectorPairing}.

This defines the [[super Poincaré super Lie algebra]]. After discarding the terms involving $\omega$ this becomes the CE algebra of the [[super translation algebra]] underlying [[super Minkowski spacetime]]

$$
  \mathbb{R}^{d-1,1\vert N}
  \,.
$$

=--














#### Example: Majorana spinors in dimensions 11, 10, and 9
 {#InDimensions11And10And9}

We spell out some of the above constructions and properties for Majorana spinors in Lorentzian spacetimes (def. \ref{LorentzianSignature}) of dimensions 11, 10 and 9, and discuss some relations between these. These spinor structures are relevant for spinors in [[11-dimensional supergravity]] and [[type II supergravity]] in 10d and 9d, as well as to the relation between these via [[Kaluza-Klein compactification]] and [[T-duality]].

+-- {: .num_prop #DiracRepInD11FromD9}
###### Proposition

Let $\{\gamma_a\}$ be any [[Dirac representation]] of $Spin(8,1)$ according to prop. \ref{CliffordAlgebraRepresentation}. By the same logic as in the proof of prop. \ref{CliffordAlgebraRepresentation} we get from this the Dirac representations in dimensions 9+1 and 10+1 by setting

$$
  \Gamma_{a \leq 8}
    \coloneqq
  \left(
    \array{
      0 & \gamma_a
      \\
      \gamma_a & 0
    }
  \right)
  \;\,,\;\;
  \Gamma_{9}
   \coloneqq
  \left(
    \array{
       0 & id
       \\
       -id & 0
    }
  \right)
  \;\,,\;\;
  \Gamma_{10}
   \coloneqq
  \left(
    \array{
      i id & 0
      \\
      0 & -i id
    }
  \right)
  \,.
$$

=--

+-- {: .num_remark #SpinRepsFrom11dToTDuality}
###### Remark


By prop. \ref{CliffordAlgebraRepresentation} the Dirac representation in $d = 11$ has complex dimension $2^{10/2} = 2^{5} = 32$. By prop. \ref{MajoranaConjugationIsRealStructure} and prop. \ref{TheMajoranaConditionInComponents} this representation carries a real structure and hence gives a real/Majorana [[spin representation]] $S \hookrightarrow \mathbb{C}^{32}$ of $Spin(10,1)$ of real dimension 32. This representation often just called "$\mathbf{32}$". This way the corresponding [[super-Minkowski spacetime]] (remark \ref{SuperPoincareOutlook}) is neatly written as

$$
  \mathbb{R}^{10,1\vert \mathbf{32}}
$$

which thus serves to express both, the real dimension of the space of odd-graded coordinate functions at every point on it, as well as the way that the $Spin(10,1)$-cover of the [[Lorentz group]] $SO(10,1)$ acts on these. This is the local model space for [[super spacetimes]] in [[11-dimensional supergravity]].

As we regard $\mathbb{C}^{32}$ instead as the Dirac representation of $Spin(9,1)$ via def. \ref{WeylRepresentation}, then it decomposes into to chiral halfs, each of complex dimension 16. This is the direct sum decomposition in terms of which the block decomposition of the above Clifford matrices is given.

Since in 10d the Weyl condition is compatible with the Majorana condition (by prop. \ref{WeylMajoranaInLorentzian10d}), the real Majorana representation $\mathbf{32}$ correspondingly decomposes as a direct sum two real representations of dimension 116 which often are denoted $\mathbf{16}$ and $\overline{\mathbf{16}}$. Hence as real/Majorana $Spin(9,1)$-representations there is a [[direct sum]] decomposition

$$
  \mathbf{32} \simeq \mathbf{16} \oplus \overline{\mathbf{16}}
  \,.
$$

The corresponding [[super Minkowski spacetime]] (remark \ref{SuperPoincareOutlook})

$$
  \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}
$$

is said to be of "type IIA", since this is the local model space for [[superspacetimes]]  in [[type IIA supergravity]]. This is as opposed to $\mathbb{R}^{9,1\vert \mathbf{16}\oplus \mathbf{16}}$, which is "type IIB" and in contrast to $\mathbb{R}^{9,1\vert \mathbf{16}}$ which is "heterotic" (the local model space for [[heterotic supergravity]]).

Now the Dirac-Weyl representation for $Spin(8,1)$ is of complex dimension $d = 2^{8/2} = 2^4 = 16$. By prop. \ref{MajoranaConjugationIsRealStructure} and prop. \ref{TheMajoranaConditionInComponents} this also admits real structure, and hence gives a Majorana representation fro $Spin(8,1)$, accordingly denoted $\mathbf{16}$. Notice that this is Majorana-Weyl.

We want to argue that both the $\mathbf{16}$ and the $\overline{\mathbf{16}}$ of $Spin(9,1)$ become isomorphic to the single $\mathbf{16}$ of $Spin(8,1)$ under forming the [[restricted representation]] along the inclusion $Spin(8,1)\hookrightarrow Spin(9,1)$ (the one fixed by the above choice of components).

For this it is sufficient to see that $\Gamma_9$, which as a complex linear map goes $\Gamma_9 \colon \mathbf{16} \longrightarrow \overline{\mathbf{16}}$ constitutes an [[isomorphism]] when regarded as a morphism in the [[category of representations]] of $Spin(8,1)$.

Clearly it is a linear isomorphism, so it is sufficient that it is a [[homomorphism]] of $Spin(8,1)$-representations at all. But that's clear since by the Clifford algebra relations $\Gamma_9$ commutes with all $\Gamma_a \Gamma_b$ for $a,b \on \{0,\cdots, 8\}$.

Hence the [[branching rule]] for [[restricted representation|restricting]] the Weyl representation in 11d along the sequence of inclusions

$$
  Spin(8,1) \hookrightarrow Spin(9,1) \hookrightarrow Spin(10,1)
$$

is

$$
  \underset{\in Rep(Spin(10,1))}\underbrace{\mathbf{32}}
    \mapsto
  \underset{\in Rep(Spin(9,1))}\underbrace{\mathbf{16} \oplus \overline{\mathbf{16}}}
    \mapsto
  \underset{\in Rep(Spin(8,1))}\underbrace{\mathbf{16} \oplus \mathbf{16}}
  \,.
$$


If we write a Majorana spinor in $\mathbf{32}$ as $\vartheta \in \mathbb{C}^{32}$, decomposed as a $(1 \times 32)$-matrix as

$$
  \vartheta
    =
  \left(
    \array{
      \psi_1
      \\
      \psi_2
    }
  \right)
  \,.
$$

and if we write for short

$$
  \psi_1
   =
  \left(
    \array{
      \psi_1 \\ 0
    }
  \right)
  \,,\;\;\;
  \psi_2
   =
  \left(
    \array{
      0 \\  \psi_2
    }
  \right)
$$

then this says that after restriction to $Spin(9,1)$-action then $\psi_1$ becomes a Majorana spinor in the $\mathbf{16}$, and $\psi_2$ a Majorana spinor in the $\overline{\mathbf{16}}$, and after further restriction to $Spin(8,1)$-action then either comes a Majorana spinor in one copy of $\mathbf{16}$.

=--



The type IIA spinor-to-vector pairing is just that of 11d under this re-interpretation. We find:

+-- {: .num_prop #typeIIASpinorToVectorPairing}
###### Proposition

The type IIA spinor-to-vector pairing is given by

$$
  \begin{aligned}
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
     \Gamma_a^{IIA}
    \left(
      \array{\psi_1 \\ \psi_2}
    \right)
    & =
    \left\{
      \array{
        \overline{\psi}_1 \gamma_a \psi_1
        + \overline{\psi}_2 \gamma_a \psi_2
        &
        \vert \; a \leq 8
        \\
        \overline{\psi}_1 \psi_1
        -
        \overline{\psi}_2 \psi_2
        &
        \vert \; a = 9
      }
    \right.
  \end{aligned}
  \,.
$$


=--

+-- {: .proof}
###### Proof

Using that on Majorana spinors the Majorana conjugate coincides with the Dirac conjugate (prop. \ref{TheMajoranaConditionInComponents}) and applying prop. \ref{DiracRepInD11FromD9} we compute:

$$
  \begin{aligned}
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
     \Gamma_a^{IIA}
    \left(
      \array{\psi_1 \\ \psi_2}
    \right)
      &\coloneqq
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
     \Gamma_a
    \left(
      \array{\psi_1 \\ \psi_2}
    \right)
    \\ & =
    \left(\array{\psi_1 \\ \psi_2}\right)^\dagger
     \Gamma_0 \Gamma_a
    \left(
      \array{\psi_1 \\ \psi_2}
    \right)
    \\
    & =
    \left\{
      \array{
    \left(\array{\psi_1 \\ \psi_2}\right)^\dagger
     \left(
       \array{
         \gamma_0 \gamma_a & 0
         \\
         0 & \gamma_0 \gamma_a
       }
     \right)
    \left(
      \array{\psi_1 \\ \psi_2}
    \right)
     & \vert \; a\leq 8
     \\
    \left(\array{\psi_1 \\ \psi_2}\right)^\dagger
     \left(
       \array{
         \gamma_0  & 0
         \\
         0 & -\gamma_0
       }
     \right)
    \left(
      \array{\psi_1 \\ \psi_2}
    \right)
     & \vert \; a = 9
     }
    \right.
    \\
    & =
    \left\{
      \array{
        \overline{\psi}_1 \gamma_a \psi_1
        + \overline{\psi}_2 \gamma_a \psi_2
        &
        \vert \; a \leq 8
        \\
        \overline{\psi}_1 \psi_1
        -
        \overline{\psi}_2 \psi_2
        &
        \vert \; a = 9
      }
    \right.
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop #typeIIBSpinorToVectorPairing}
###### Proposition

The type IIB spinor-to-vector pairing is

$$
  \begin{aligned}
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
    \Gamma_a^{IIB}
    \left(\array{\psi_1 \\ \psi_2}\right)
    & =
    \left\{
      \array{
        \overline{\psi}_1 \gamma_a \psi_1
        + \overline{\psi}_2 \gamma_a \psi_2
        &
        \vert \; a \leq 8
        \\
        \overline{\psi}_1 \psi_1
        +
        \overline{\psi}_2 \psi_2
        &
        \vert \; a = 9
      }
    \right.
  \end{aligned}
$$


=--

+-- {: .proof}
###### Proof

The type II pairing spinor-to-vector pairing is obtained from the type IIA pairing of prop. \ref{typeIIASpinorToVectorPairing} by replacing all bottom right matrix entries (those going $\overline{\mathbf{16}}\to \overline{\mathbf{16}}$ by the corresponding top left entries (those going $\mathbf{16} \to \mathbf{16}$ )). Notice that in fact all these block entries are the same, except for the one at $a = 9$, where they simply differ by a sign. This yields the claim.

=--

Notice also the following relation between the different pairing in dimensions 11, 10 and 9:

+-- {: .num_prop #9ComponentOfIIBPairing}
###### Proposition

The $(9,10)$-component of the spinor-to-bivector pairing (def. \ref{SpinorToRank2TensorBilinearPairing}) in 11d equals the 9-component of the type IIB spinor-to-vector pairing

$$
  \begin{aligned}
    i
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
     \Gamma_9 \Gamma_{10}
    \left(\array{\psi_1 \\ \psi_2}\right)
    & =
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
    \Gamma_9^{IIB}
    \left(\array{\psi_1 \\ \psi_2}\right)
  \end{aligned}
$$


=--

+-- {: .proof}
###### Proof

Using prop. \ref{DiracRepInD11FromD9} and prop. \ref{typeIIBSpinorToVectorPairing} we compute:

$$
  \begin{aligned}
    i\,
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
     \Gamma_9 \Gamma_{10}
    \left(\array{\psi_1 \\ \psi_2}\right)
    & =
    i
    \left(\array{\psi_1 \\ \psi_2}\right)^\dagger
     \Gamma_0\Gamma_9 \Gamma_{10}
    \left(\array{\psi_1 \\ \psi_2}\right)
    \\
    & =
    i \,
    \left(\array{\psi_1 \\ \psi_2}\right)^\dagger
      \left(
        \array{
          -i \gamma_0 & 0
          \\
          0 & -i \gamma_0
        }
      \right)
    \left(\array{\psi_1 \\ \psi_2}\right)
    \\
    & =
      \overline{\psi}_1 \psi_1
      +
      \overline{\psi}_2 \psi_2
    \\
    & =
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
    \Gamma_9^{IIB}
    \left(\array{\psi_1 \\ \psi_2}\right)
  \end{aligned}
$$

=--

The following is an evident variant of the extensions considered in ([CAIB 99](#CAIB99), [FSS 13](#FiorenzaSatiSchreiber13)).

+-- {: .num_prop #TypeIIExtension}
###### Proposition

We have

1. The 11d $N = 1$ [[super-Minkowski spacetime]] $\mathbb{R}^{10,1\vert \mathbf{32}}$ (def. \ref{SuperMinkowskiSpacetime}) is the  [[central extension|central]] [[super Lie algebra|super]] [[Lie algebra extension]] of the 10d type IIA [[super-Minkowski spacetime]] $\mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}$ by the 2-cocycle

   $$
     c_2 \coloneqq \overline{\psi} \wedge \Gamma_{10} \psi
     \;\;\;
     \in
     CE(\mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}})
   $$

   (from def. \ref{SpinorToVectorBilinearPairing}).

1. The 10d type IIA [[super-Minkowski spacetime]] $\mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}$  is [[central extension|central]] [[super Lie algebra|super]] [[Lie algebra extension]] of th 9d $N = 2$ [[super-Minkowski spacetime]] by the 2-cocycle given by the type IIA spinor-to-vector pairing

   $$
     c_2^{IIA}
      \;\coloneqq\;
     \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
      \wedge \Gamma_9^{IIA}
      \left(
       \array{\psi_1 \\ \psi_2}
      \right)
        \;\;\;\in
      CE(\mathbb{R}^{8,1\vert \mathbf{16}+ \mathbf{16}})
   $$

   (from prop. \ref{typeIIASpinorToVectorPairing}).

1. The 10d type IIB [[super-Minkowski spacetime]] $\mathbb{R}^{9,1\vert \mathbf{16}+ \mathbf{16}}$  is [[central extension|central]] [[super Lie algebra|super]] [[Lie algebra extension]] of th 9d $N = 2$ [[super-Minkowski spacetime]] by the 2-cocycle given by the type IIB spinor-to-vector pairing

   $$
     c_2^{IIB}
       \;\coloneqq\;
     \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
      \wedge
      \Gamma_9^{IIB}
      \left(
       \array{\psi_1 \\ \psi_2}
      \right)
      \;\;\;
      \in CE(\mathbb{R}^{8,1\vert \mathbf{16} + \mathbf{16}})
   $$

   (from prop. \ref{typeIIBSpinorToVectorPairing}).

In summary, we have the following [[diagram]] in the [[category]] of [[super L-infinity algebras]]

$$
  \array{
    && && \mathbb{R}^{10,1\vert \mathbf{32}}
    \\
    && && \downarrow
    \\
    \mathbb{R}^{9,1\vert \mathbf{16} + \mathbf{16}}
      && &&
    \mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}
     &\overset{c_2}{\longrightarrow}&
    B \mathbb{R}
    \\
    & \searrow && \swarrow
    \\
    && \mathbb{R}^{8,1\vert \mathbf{16} + \mathbf{16}}
    \\
    & {}^{\mathllap{c_2^{IIB}}}\swarrow && \searrow^{\mathrlap{c_2^{IIA}}}
    \\
    B \mathbb{R} && && B \mathbb{R}
  }
  \,,
$$


where $B\mathbb{R}$ denotes the [[line Lie 2-algebra]], and where each "hook"

$$
  \array{
    \widehat{\mathfrak{g}}
    \\
    \downarrow
    \\
    \mathfrak{g}
      &\overset{\omega_2}{\longrightarrow}&
    B\mathbb{R}
  }
$$

is a [[homotopy fiber sequence]] (because homotopy fibers of super $L_\infty$-algebra cocycles are the corresponding extension that they classify, see at _[[L-infinity algebra cohomology]]_).

=--

+-- {: .proof}
###### Proof

To see that the given 2-forms are indeed cocycles: they are trivially closed (by def. \ref{SuperMinkowskiSpacetime}), and so all that matters is that we have a well defined super-2-form in the first place. Since the $\psi^\alpha$ are in bidegree $(1,odd)$, they all commutes with each other (see at _[[signs in supergeometry]]_) and hece the condition is that the pairing is symmetric. This is the case by prop. \ref{SpinorToVectorPairing}.

Now to see the extensions. Notice that for $\mathfrak{g}$ any ([[super Lie algebra|super]]) [[Lie algebra]] (of finite dimension, for convenience), and for $\omega \in \wedge^2\mathfrak{g}^\ast$ a [[Lie algebra cohomology|Lie algebra 2-cocycle]] on it, then the [[Lie algebra extension]] $\widehat{\mathfrak{g}}$ that this classifies is neatly characterized in terms of its dual [[Chevalley-Eilenberg algebra]]: that is simply the original CE algebra with one new generator $e$ (in degree $(1,even)$) adjoined, and with the differential of $e$ taking to be $\omega$:

$$
  CE(\widehat{\mathfrak{g}})
   =
  (CE(\mathfrak{g}) \otimes \langle e\rangle), d e = \omega)
  \,.
$$

Hence in the case of $\omega = c_2^{IIA}$ we identify the new generator with $e^9$ and see that the equation $d e^9 = c_2^{IIA}$ is precisely what distinguishes the CE-algebra of $\mathbb{R}^{8,1\vert \mathbf{16}+ \mathbf{16}}$ from that of $\mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}}$, by prop. \ref{DiracRepInD11FromD9} and the fact that both spin representation have the same underlying space, by remark \ref{SpinRepsFrom11dToTDuality}.

The other two cases are directly analogous.

=---

Recall the following (e.g. from [FSS 16](#FiorenzaSatiSchreiber16) and references given there):

+-- {: .num_defn #M2CoycleAndIIAStringCocycle}
###### Definition

The cocycle for the [[higher WZW term]] of the [[Green-Schwarz sigma-model]] for the [[M2-brane]] is

$$
  \mu_{M2}
    \coloneqq
  i\,\overline{\vartheta} \wedge \Gamma_a \Gamma_b \vartheta \wedge e^a \wedge e^b
  \;\;\;
  \in
  CE(\mathbb{R}^{10,1\vert \mathbf{32}})
$$

obtained from the spinor-to-bivector pairing of def. \ref{SpinorToRank2TensorBilinearPairing}.
(Here and in the following we are using the nation from remark \ref{SpinRepsFrom11dToTDuality}.)

The cocycle for the [[WZW term]] of the [[Green-Schwarz sigma-model]] for the [[type IIA string theory|type IIA]] [[superstring]] is

$$
  \mu_{IIA}
   \coloneqq
  i\,\overline{\vartheta} \wedge \Gamma_a \Gamma_{10} \vartheta \wedge e^a
  =
  i\,
  \overline{\left(
    \array{\psi_1 \\ \psi_2}
  \right)}
    \Gamma_a \Gamma_{10}
  \left(
    \array{\psi_1 \\ \psi_2}
  \right)
  \;\;\;
  \in
  CE(\mathbb{R}^{9,1\vert \mathbf{16} + \overline{\mathbf{16}}})
  \,,
$$

i.e. this is the the $e^{10}$-component of $\mu_{M2}$ ("[[double dimensional reduction]]" [FSS 16](#FiorenzaSatiSchreiber16)):

$$
  \mu_{IIA} = (\pi_{10})_\ast \mu_{M2}
  \,.
$$

=--

+-- {: .num_prop #DDReductionOfIIAStringCocycle}
###### Proposition

The $e^9$-component of the cocycle for the IIA-superstring (def. \ref{M2CoycleAndIIAStringCocycle}), regarded as an element in $CE(\mathbb{R}^{8,1}\vert \mathbf{16} + \mathbf{16})$, equals the 2-cocycle that defines the type IIB extension, according to prop. \ref{TypeIIExtension}:

$$
  (\pi_9)_\ast \mu_{IIA} = c_2^{IIB}
  \,.
$$

=--

+-- {: .proof}
###### Proof

We have

$$
  \begin{aligned}
    (\pi_9)_\ast \mu_{IIA}
      & =
    i\,
    \overline{\left(
      \array{\psi_1 \\ \psi_2}
    \right)}
      \Gamma_9 \Gamma_{10}
    \left(
      \array{\psi_1 \\ \psi_2}
    \right)
    \\
    & =
    \overline{\left(\array{\psi_1 \\ \psi_2}\right)}
    \Gamma_9^{IIB}
    \left(\array{\psi_1 \\ \psi_2}\right)
    \\
    & =
    c_2^{IIB}
  \end{aligned}
$$

where the first equality is by def. \ref{M2CoycleAndIIAStringCocycle}, the second is the statement of prop. \ref{9ComponentOfIIBPairing}, while the third is from prop. \ref{TypeIIExtension}.

=--














#### Poincar&#233; connections: Graviton and gravitino field
 {#GravitonAndGravitino}

We may now apply the general discussion of super Lie algebra valued super differential forms, def. \ref{SuperLieAlgValuedDiffForms}, to the case of the [[super Poincare Lie algebra]], def. \ref{SuperPoincareAndSuperMinkowski}.

its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$ is generated on

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

with the differential defined by

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi
$$

$$
  d_{CE} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

Accordingly its [[Weil algebra]]
$W(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$
has these generators together with a further degree-shifted copy of each $\{t^a\}$, $\{r^{a b}\}$ and $\{\rho^{\alpha}\}$ with differential given by

$$
  d_{W} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c} + r^{a b}
$$

$$
  d_{W} \, e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi + t^a
$$

$$
  d_{W} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi + \rho
  \,.
$$


Differential form data with values in this is a morphism of [[dg-algebras]] from the [[Weil algebra]] $W(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))$ to the [[deRham dg-algebra]] $\Omega^\bullet(\mathbb{R}^{p|q})$, def. \ref{SuperDeRhamComplex}

$$
  \Omega^\bullet(X)
   \leftarrow
   W(\mathfrak{Iso}(\mathbb{R}^{d-1,1|N}))
   :
   (A,F_A)
   \,.
$$

This is [[∞-Lie algebroid valued differential form]] data with [[curvature|∞-Lie algebroid valued curvature]] that is explicitly given by:




* connection forms / field configuration

  * $E \in \Omega^1(X,\mathbb{R}^{d-1,1|N})$ -- the **[[vielbein]]** (part of the _[[graviton]] [[field (physics)|field]]_)

  * $\Omega \in \Omega^1(X, \mathfrak{so}(\mathbb{R}^{d-1,1}))$ -- the **[[spin connection]]** (part of the _[[graviton]] [[field (physics)|field]]_)

  * $\Psi \in \Omega^ 1(X,S)$ -- the **[[spinor]]** (the [[gravitino]] [[field (physics)|field]])


* [[curvature]] forms / [[field strength]]s

  * $T = d E + \Omega \cdot E + \Gamma(\bar \Psi \wedge \Psi) \in \Omega^2(X,\mathbb{R}^{d-1,1})$ - the **[[torsion of a metric connection|torsion]]**

  * $R = d \Omega + [\Omega \wedge \Omega] \in \Omega^2(X, \mathfrak{so}(10,1))$ - the **[[Riemann curvature]]**

  * $\rho = d \Psi + (\Omega \wedge \Psi) \in \Omega^2(X, S)$ -- the **[[covariant derivative]] of the [[gravitino]]**


+-- {: .num_defn #CEAlgebraOfSuperPoincare}
###### Definition

The [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{iso}(\mathbb{R}^{d-1,1|N}))$ is generated by

* elements $\{e^a\}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$

* and elements $\{\psi^\alpha\}$ of degree $(1,odd)$

with the differential defined by

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \bar \psi \Gamma^a \psi
$$

$$
  d_{CE} \, \psi = \frac{1}{4} \omega^{ a b} \Gamma_{a b} \psi
  \,.
$$

Discarding the terms involving $\omega$ here this is the CE algebra of the [[super translation algebra]] underlying [[super Minkowski spacetime]].

=--

In this way the super-Poincar&#233; Lie algebra and its extensions is usefully discussed for instance in ([D'Auria-Fr&#233; 82](#DAuriaFre82)) and in ([Azc&#225;rraga-Townsend 89](super+Minkowski+spacetime#AzcarragaTownsend89), [CAIB 99](super+Minkowski+spacetime##CAIB99)). In much of the literature instead the following equivalent notation is popular, which more explicitly involves the [[coordinates]] on [[super Minkowski space]].

+-- {: .num_remark }
###### Remark

The abstract generators in def. \ref{CEAlgebraOfSuperPoincare} are identified with [[left invariant 1-forms]] on the [[super-translation group]] (= [[super Minkowski space]]) as follows.

Let $(x^a, \theta^\alpha)$ be the canonical [[coordinates]] on the [[supermanifold]] $\mathbb{R}^{d|N}$ underlying the super translation group. Then the identification is

* $\psi^\alpha = d \theta^\alpha$.

* $e^a = d x^a +  \overline{\theta} \Gamma^a d \theta$.

Notice that this then gives the above formula for the differential of the [[super-vielbein]] in def. \ref{CEAlgebraOfSuperPoincare} as

$$
  \begin{aligned}
    d e^a & = d (d x^a +  \overline{\theta} \Gamma^a d \theta)
    \\
    & =  d \overline{\theta}\Gamma^a d \theta
    \\
    & =  \overline{\psi}\Gamma^a \psi
  \end{aligned}
  \,.
$$


=--


+-- {: .num_remark #Supertorsion}
###### Remark

The term $\bar \psi \Gamma^a \psi$ is sometimes called the *[[supertorsion]]* of the [[super-vielbein]] $e$, because the defining equation

$$
  d_{CE} e^{a } -\omega^a{}_b \wedge e^b = \bar \psi \Gamma^a \psi
$$

may be read as saying that $e$ is [[torsion]]-free except for that term. Notice that this term is the only one that appears when the differential is applied to "Lorentz scalars", hence to object in $CE(\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N}))$ which have "all indices contracted". See also at _[[torsion constraints in supergravity]]_.

Notably we have

$$
  d \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \right)
  \propto
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
  \,.
$$

This remaining operation "$e \mapsto \Psi^2$" of the differential acting on Loretz scalars is sometimes denoted "$t_0$", e.g. in ([Bossard-Howe-Stelle 09, equation (8)](super+Minkowski+spacetime#BossardHoweStelle09)).

This relation is what govers all of the exceptional super Lie algebra cocycles that appear [below](#TheOldBraneScan): for some combinations of $(d,p,N)$ a [[Fierz identity]] implies that the term

$$
  \left(
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}
  \right)
  \wedge
  \left(
    \overline{\Psi} \wedge \Gamma_{a_p} \Psi
  \right)
$$

vanishes identically, and hence in these dimensions the term

$$
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
$$

is a [[cocycle]] in super [[Lie algebra cohomology]].

=--











