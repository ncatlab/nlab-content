


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

Accordingly a _Majorana spinor_ or _Majorana fermion_ is a [[spinor]]/[[fermion]] corresponding to such a representation under [[Wigner classification]]. None of the particles in the [[standard model of particle physics]] except possibly the [[neutrinos]] are Majorana fermions (for neutrinos this remains open). The relevance of Majorana representations is that these appear in [[supersymmetry]], constituting for instance the odd-graded components of [[super-Minkowski spacetimes]]. See remark \ref{SuperPoincareOutlook} below.

The terminology _Majorana spinor_ originates in and is standard in the [[physics]] literature, where it usually refers to the explicit expression of the reality condition in terms of chosen basis components. With standard conventions understood (see prop. \ref{CliffordAlgebraRepresentation} below), then a complex [[spinor]] $\psi$ for $Spin(d-1,1)$, regarded as an element of $\mathbb{C}^{\nu}$ (with $d = 2 \nu, 2\nu+1$) is a Majorana spinor if it satisfies the condition

$$
  \psi^t C = \psi^\dagger \Gamma_0
  \,,
$$

where $(-)^T$ denotes forming [[transpose matrices]], $(-)^\dagger = \overline{(-)}^T$ denotes forming [[hermitian adjoint]] and where $C$ is the [[charge conjugation matrix]]. This says that the _Majorana conjugate_ of $\psi$ (the left hand side) coincides with the "Dirac conjugate" of $\psi$ (the right hand side). Equivalently this means that (e.g. [Castellani-D'Auria-Fr&#233;, (II.7.22)](#CastellaniDAuriaFre))

$$
  \psi = C \Gamma_0^T \psi^\ast
  \,.
$$

See prop. \ref{TheMajoranaConditionInComponents} below.

In some dimensions there are no complex spin representations with real structure, but there may be those with [[quaternionic structure]]. The corresponding physics jargon then is _symplectic Majorana spinor_.

## Definition

+-- {: .num_defn #MajoranaSpinorGeneral}
###### Definition

Let $\rho \colon Spin(s,t) \longrightarrow GL_{\mathbb{C}}(V)$ be a [[unitary representation]] of a [[spin group]]. Then $\rho$ is called _Majorana_ if it admits a real structure $J$ (def. \ref{RealStructureOnLinearRepresentation}) and _symplectic Majorana_ if it admits a [[quaternionic structure]] $J$ (def. \ref{RealStructureOnLinearRepresentation}). An element $\psi \in V$ is called a _Majorana spinor_ if $J(\psi) = \psi$.

=--

## In components


+-- {: .num_defn}
###### Definition

We write $\mathbb{R}^{s,t}$ for the real [[vector space]] $\mathbb{R}^{s+t}$ equipped with the standard [[quadratic form]] $q$ of [[signature of a quadratic form|signature]] $(t,s)$, i.e.

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
  \eta \coloneqq diag(\underset{t}{\underbrace{+1 , \cdots, +1}}, \underset{s}{\underbrace{-1, \cdots, -1}})
$$

for the corresponding [[metric]].

=--

The real [[Clifford algebra]] $Cl(s,t)$ is the $\mathbb{R}$-[[associative algebra|algebra]] [[generators and relations|generated]] from elements $\{\Gamma_a\}_{a = 1}^{s+t}$ subject to the [[generators and relations|relation]]

$$
  \Gamma_a \Gamma_b + \Gamma_b \Gamma_a = 2 \eta_{a b} 
  \,.
$$

### Clifford representation

The following is a standard convention for the complex representation of the Clifford algebra for $\mathbb{R}^{s,1}$ ([Castellani-D'Auria-Fr&#233;, (II.7.1)](#CastellaniDAuriaFre)):

+-- {: .num_prop #CliffordAlgebraRepresentation}
###### Proposition

Let $t = 1$ and let 

$$
  d = s + 1 = 2\nu, 2 \nu + 1
$$

with $d \geq 4$.

We label the standard [[coordinates]] of $\mathbb{R}^{s,1}$ by

$$
  \{x^1, x^2, \cdots, x^{d-1}, x^0\}
  \,,
$$

where $x^0$ is the coordinate along the [[timelike]] direction.

Then there is a choice of complex linear representation of the [[Clifford algebra]] $Cl(s,1)$ on 

$$
  V \coloneqq \mathbb{C}^{\nu}
$$ 

such that

1. $\Gamma_{0}$ is [[hermitian]]

1. $\Gamma_{space}$ is [[anti-hermitian]].

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

Now proceed by [[induction]]. Suppose a Clifford representation $\{\gamma_a\}$ as claimed has been constructed in even dimension $d = 2 \nu$. Then a coresponding representation in dimension $d+2$ is given by setting


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

### Charge conjugation matrix

+-- {: .num_prop #ChargeConjugationMatrix}
###### Proposition

Given the Clifford algebra representation of the form of prop. \ref{CliffordAlgebraRepresentation}, consider the equations

* $C_{(-)} \Gamma_a  = - \Gamma_a^T C_{(-)}$;

* $C_{(+)} \Gamma_a = \Gamma_a^T C_{(+)}$

for $C_{(\pm)} \in Mat_{\nu \times n}(\mathbb{C})$.

In even dimensions $d = 2 \nu$ then both these equations have a solution, wheras in odd dimensions $d = 2 \nu + 1$ only one of them does (alternatingly, starting with $C_{(+)}$ in dimension 5). Either $C_{(\pm)}$ is called the _[[charge conjugation matrix]]_.

Moreover, all $C_{(\pm)}$ may be chosen to be real matrices, and in addition they satisfy the following relations:

| $d$ |   |    |
|-----|---|----|
| 4 | $C_{(+)}^T = -C_{(+)}$; $C_{(+)}^2 = -1$ | $C_{(-)}^T = -C_{(+)}$; $C_{(-)}^2 = -1$ |
| 5 | $C_{(+)}^T = -C_{(+)}$; $C_{(+)}^2 = -1$  |  |
| 6 | $C_{(+)}^T = -C_{(+)}$; $C_{(+)}^2 = -1$  | $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = 1$ |
| 7 |   |  $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = 1$ |
| 8 | $C_{(+)}^T = C_{(+)}$; $C_{(+)}^2 = 1$ | $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = 1$ |
| 9 | $C_{(+)}^T = C_{(+)}$; $C_{(+)}^2 = 1$ |  |
| 10 | $C_{(+)}^T = C_{(+)}$; $C_{(+)}^2 = 1$ |  $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = -1$ |
| 11 |   |  $C_{(-)}^T = C_{(-)}$; $C_{(-)}^2 = -1$ |

In particular this means that 

$$
  C^{-1} = C^T
  \,.
$$


=--

(e.g. [Castellani-D'Auria-Fr&#233;, (II.7.2)](#CastellaniDAuriaFre))




### Majorana conjugate and Real structure


+-- {: .num_prop #MajoranaConjugationIsRealStructure}
###### Proposition

For $d \in \{4,8,9,10,11\}$, let $V = \mathbb{C}^\nu$ as above. Write $\{\Gamma_a\}$ for a Clifford representation according to prop. \ref{CliffordAlgebraRepresentation}, and write 

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

for the [[charge conjugation matrix]] from prop. \ref{ChargeConjugationMatrix}. Then the function

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
    C \Gamma_a^\ast \Gamma_b^\ast \Gamma_0^T \psi^\ast
    \\
    & = 
    \Gamma_a^\dagger \Gamma_b^\dagger C \Gamma_0^T \psi^\ast
    \\
    & = (-\Gamma_a) (-\Gamma_b) C \Gamma_0^T \psi^\ast
    \\
    & = \Gamma_a \Gamma_b C \Gamma_0^T \psi^\ast
    \\
    & = \Gamma_a \Gamma_b J(\psi)
  \end{aligned}
  \,.
$$

Here we first used that $\Gamma_0^T \propto \Gamma_0$ by prop. \ref{CliffordAlgebraRepresentation} and that $\Gamma_0$ anti-commutes with the spatial Clifford matrices. Then we used the defining equation for the [[charge conjugation matrix]], which says that passing it through a Gamma-matrix yields a transpose, up to a global sign. That global sign cancels since we pass through two Gamma matrices. Finally we used that the spatial $\Gamma$-matrices may be chosen to be anti-hermitian, by prop. \ref{CliffordAlgebraRepresentation}.

Finally, that the same conclusion holds for $\Gamma_a \Gamma_b$ replaced by $\Gamma_0 \Gamma_a$: The above reasoning applies with two extra signs picked up: one from the fact that $\Gamma_0$ commutes with itself, one from the fact that it is hermitian, by prop. \ref{CliffordAlgebraRepresentation}. These two signs cancel.

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



+-- {: .num_prop #TheMajoranaConditionInComponents}
###### Proposition

In dimensions $d = 4,8,9,10,11$ a spinor $\psi \in \mathbb{C}^{\nu}$ is Majorana according to def. \ref{MajoranaSpinorGeneral} with respect to the real structure from prop. \ref{MajoranaConjugationIsRealStructure}, precisely if

$$
  \psi = C \Gamma_0^T \psi^\ast
$$

(as e.g. in [Castellani-D'Auria-Fr&#233;, (II.7.22)](#CastellaniDAuriaFre)),

This is equivalent to the condition that

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

### The spinor pairing to vectors
 {#TheSpinorPairingToVectors}

For a $Spin(d-1,1)$ representation $V$ as in prop. \ref{CliffordAlgebraRepresentation}, with real/Majorana structure as in prop. \ref{MajoranaConjugationIsRealStructure}, write

$$
  S \hookrightarrow V
$$

for the subspace of Majorana spinors, regarded as a real vector space.

+-- {: .num_defn #SpinorToVectorBilinearPairing}
###### Definition

For a $Spin(d-1,1)$ representation $V$ as in prop. \ref{CliffordAlgebraRepresentation}, with real/Majorana structure as in prop. \ref{MajoranaConjugationIsRealStructure}, let

$$
  \overline{(-)}\Gamma (-)
    \colon
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

where the first sign picked up is from $C^T = \pm C$, while the second is from $\Gamma_a^T C = \pm C \Gamma_a$. By the condition in prop. \ref{MajoranaConjugationIsRealStructure}, these signs agree, and hence cancel out. (In ([Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre)) this is implicit in (II.2.32a).)

Regarding the second point: By prop. \ref{MajoranaConjugationIsRealStructure} and prop. \ref{ComplexBilinearFormInducedFromMajoranaStructure} we get

$$
  (g(\psi_1), \Gamma_a g(\psi_2))
  = 
  \langle g(\psi_1),\Gamma_a g(\psi_2)\rangle
  = 
   \langle \psi_1, g^\dagger \Gamma_a g \psi_2 \rangle
  \,.
$$

(In ([Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre)) this is implicit in (II.2.35)-(II.2.39).)

=--

+-- {: .num_remark #SuperPoincareOutlook}
###### Remark

Proposition \ref{SpinorToVectorPairing} implies that adding a copy of $S$ to the [[Poincaré Lie algebra]] in odd degree, then the pairing of def. \ref{SpinorToVectorBilinearPairing} is a consistent extension of the [[Lie bracket]] of the latter to a [[super Lie algebra]]. This is the _[[super Poincaré Lie algebra]]_.

=--


## Appendix

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

(e.g. [Meinrenken 13, p. 81](#Meinrenken13))





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
