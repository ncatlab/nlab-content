


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

A _Majorana spin representation_ is essentially a _real_ [[spin representation]] (see at _[spin representation -- Real representations](spin+representation#RealIrreducibleSpinRepresentationInLorentzSignature)_) but regarded as a _complex_ [[spin representation]] equipped with [[real structure]] (recalled as def. \ref{RealStructureOnLinearRepresentation} below).

Accordingly a _Majorana spinor_ or _Majorana fermion_ is a [[spinor]]/[[fermion]] corresponding to such a representation under [[Wigner classification]]. None of the particles in the [[standard model of particle physics]] except possibly the [[neutrinos]] are Majorana fermions (for neutrinos this remains open). The relevance of Majorana representations is that these appear in [[supersymmetry]], constituting for instance the odd-graded components of [[super-Minkowski spacetimes]]. See remark \ref{SuperPoincareOutlook} below.

The terminology _Majorana spinor_ originates in and is standard in the [[physics]] literature, where it usually refers to the explicit expression of the reality condition in terms of chosen basis components. With standard conventions understood (see prop. \ref{CliffordAlgebraRepresentation} below), then a complex [[spinor]] $\psi$ for $Spin(d-1,1)$, regarded as an element of $\mathbb{C}^{\nu}$ (with $d = 2 \nu, 2\nu+1$) is a Majorana spinor if it satisfies the condition

$$
  \psi^t C = \psi^\dagger \Gamma_0
  \,,
$$

where $(-)^T$ denotes forming [[transpose matrices]], $(-)^\dagger = \overline{(-)}^T$ denotes forming [[hermitian adjoint]] and where $C$ is the [[charge conjugation matrix]]. This says that the _Majorana conjugate_ (def. \ref{MajoranaConjugation} below) of $\psi$ (the left hand side) coincides with the "Dirac conjugate" (def. \ref{DiracConjugate} below) of $\psi$ (the right hand side). Equivalently this means that (e.g. [Castellani-D'Auria-Fr&#233;, (II.7.22)](#CastellaniDAuriaFre))

$$
  \psi = J(\psi) \coloneqq C \Gamma_0^T \psi^\ast
  \,,
$$

where $J(-)$ is the given real structure (prop. \ref{MajoranaConjugationIsRealStructure} below). See prop. \ref{TheMajoranaConditionInComponents} below.

In some dimensions there are no complex spin representations with real structure, but there may be those with [[quaternionic structure]]. The corresponding physics jargon then is _symplectic Majorana spinor_.

## Definition

+-- {: .num_defn #MajoranaSpinorGeneral}
###### Definition

Let $\rho \colon Spin(s,t) \longrightarrow GL_{\mathbb{C}}(V)$ be a [[unitary representation]] of a [[spin group]]. Then $\rho$ is called _Majorana_ if it admits a real structure $J$ (def. \ref{RealStructureOnLinearRepresentation}) and _symplectic Majorana_ if it admits a [[quaternionic structure]] $J$ (def. \ref{RealStructureOnLinearRepresentation}). An element $\psi \in V$ is called a _Majorana spinor_ if $J(\psi) = \psi$.

=--

## In components
 {#InComponents}

We work out in detail what def. \ref{MajoranaSpinorGeneral} comes down to in components (i.e. in terms of choices of [[linear bases]]), using standard notation and conventions from the physics literature (e.g. [Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre)).

### Conventions and Notation

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

+-- {: .num_defn}
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

### Clifford representation

The following is a standard convention for the complex representation of the Clifford algebra for $\mathbb{R}^{s,1}$ ([Castellani-D'Auria-Fr&#233;, (II.7.1)](#CastellaniDAuriaFre)):

+-- {: .num_prop #CliffordAlgebraRepresentation}
###### Proposition

Let $t = 1$ (Lorentzian signature, def. \ref{LorentzianSignature}) and let 

$$
  d = s + 1 = 2\nu, 2 \nu + 1
$$

with $d \geq 4$.

Then there is a choice of complex linear representation of the [[Clifford algebra]] $Cl(s,1)$ on 

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

Now proceed by [[induction]]:

**odd dimensions**

Suppose a Clifford representation $\{\gamma_a\}$ as claimed has been constructed in even dimension $d = 2 \nu$. 

Then a Clifford representation in dimension $d = 2 \nu + 1$ is given by taking

$$
  \Gamma_a
   \coloneqq
  \left\{
    \array{
      \gamma_a & \text{for}\, a \leq d - 2
      \\
      \epsilon \gamma_0 \gamma_1 \cdots \gamma_{d-2}
       & \text{for} a = d-1
    }
  \right.
$$

where

$$
  \epsilon 
     =
   \left\{
     \array{
       1 & \text{for}\, \nu \, \text{odd}
       \\
       i & \text{for}\, \nu \, \text{even}
     }
   \right.
   \,.
$$

**even dimensions**

Suppose a Clifford representation $\{\gamma_a\}$ as claimed has been constructed in dimension $d = 2 \nu$. 

Then a coresponding representation in dimension $d+2$ is given by setting


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
  \langle A -, -\rangle
  = 
  \langle \overline  - , \overline{A} -\rangle
  \;\;\;\text{and} \;\;\;
  \langle  -, A -\rangle
  = 
  \langle \overline  \overline{A} - ,  -\rangle
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


### Charge conjugation matrix
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
    & = \pm \Gamma_a C \Gamma_0^T \psi^\ast
    \\
    & = \pm \Gamma_a J(\psi^\ast) 
  \end{aligned}
  \,,
$$

where, by comparison with the table in prop. \ref{ChargeConjugationMatrix}, $\epsilon$ is the sign in $C^T = \epsilon C$, which cancels out, and the remaining $\pm$ is the sign in $C = C_{(\pm)}$, due to remark \ref{TransposeChargeConjugation}.

For the timelike index we similarly get

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
    & = \pm \Gamma_0 J(\psi^\ast) 
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

In dimensions $d = 4,8,9,10,11$ a spinor $\psi \in \mathbb{C}^{\nu}$ is Majorana according to def. \ref{MajoranaSpinorGeneral} with respect to the real structure from prop. \ref{MajoranaConjugationIsRealStructure}, precisely if

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


## The spinor bilinear pairing to antisymmetric $p$-tensors
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
    \psi_2^\dagger \Gamma_0 \Gamma^a
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

(e.g. [Meinrenken 13, p. 81](#Meinrenken13))





## Related concepts

* [[charge conjugation matrix]]

## References

The traditional component discussion in terms of a [[charge conjugation matrix]] is discussed for instance in 

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section II.7.3 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* {#VanProeyen99} [[Antoine Van Proeyen]], section 3 of _Tools for supersymmetry_ ([arXiv:hep-th/9910030](http://arxiv.org/abs/hep-th/9910030))

* {#Laenen} [[Eric Laenen]] _Classical Field Theory_ ([web](http://www.nikhef.nl/~t45/ftip/)) chapter on _Gamma matrices_ ([pdf](http://www.nikhef.nl/~t45/ftip/AppendixE.pdf))

The relation to the concept of real structures on complex Spin-representations is highlighted in

* {#FigueroaOFarrill} [[José Figueroa-O'Farrill]], _Majorana spinors_ ([pdf](http://www.maths.ed.ac.uk/~jmf/Teaching/Lectures/Majorana.pdf))

See also 

* {#Meinrenken13} [[Eckhard Meinrenken]], _Clifford algebras and Lie theory_, Springer (2013)

* Theodor Br&#246;cker, [[Tammo tom Dieck]], _Representations of Compact Lie Groups_, Springer (1985)

* Wikipedia, _[Majorana fermion](https://en.wikipedia.org/wiki/Majorana_fermion)_


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
