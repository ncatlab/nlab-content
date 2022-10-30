

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


+-- {: .num_defn #HCohomology}
###### Definition
**(H-cohomology)**

Given a [[smooth manifold]] or [[formal smooth manifold]] $X$, and given a [[differential 3-form]] $H \in \Omega^3(X)$, then forming the [[wedge product]] with $H$ is a nilpotent operation, and hence defines the [[differential]] of a [[cochain complex]] whose entries are the [[vector spaces]] $\Omega^{even/odd}(X)$ of all odd-graded or all even-graded [[differential forms]] on $X$:

$$
  \cdots
    \to
  \Omega^{even}(X)
    \overset{H\wedge(-)}{\longrightarrow}
  \Omega^{odd}(X)
    \overset{H\wedge(-)}{\longrightarrow}
  \Omega^{even}(X)
    \overset{H\wedge(-)}{\longrightarrow}
  \Omega^{odd}(X)
    \to
   \cdots
  \,.
$$

The [[cochain cohomology]] of this [[cochain complex]] 

$$
  H^{even/odd}_{H\wedge}(X)
  \coloneqq; 
  \frac{
    ker
    \left(
      \Omega^{even/odd}(X)
       \overset{H\wedge(-)}{\longrightarrow}
      \Omega^{odd/even}(X)
     \right)
   }{
    im
    \left(
      \Omega^{odd/even}(X)
       \overset{H\wedge(-)}{\longrightarrow}
      \Omega^{even/odd}(X)
     \right)
   }
$$

is also called the _H-cohomology_ of $X$. 

=--

([Cavalcanti 03, p. 19](#Cavalcanti03))

+-- {: .num_remark}
###### Remark

Often it is assumed that the 3-form $H$ in def. \ref{HCohomology} is [[closed differential form|closed]], because in this case H-cohomology serves as an approximation to the corresponding $H$-[[twisted de Rham cohomology]] (prop. \ref{TwistedDeRhamCohomologyCoincidesWithHCohomologyOnInfinitesimllayThickenedPoint} below). But of course for def. \ref{HCohomology} to make sense in itself, $H$ need not be closed.

=--

It is immediate to consider this more generally:

+-- {: .num_defn #HCohomologyInGradedCommutativeAlgebra}
###### Definition
**(H-cohomology in [[graded-commutative algebra]])**

Let $\mathcal{A}$ be a [[graded commutative algebra]] in [[characteristic zero]] and let $H \in \mathcal{A}$ be an odd-graded element. This implies that consecutive multiplication with $H$

$$
  \cdots
    \to
  \mathcal{A}
    \overset{H \cdot(-)}{\longrightarrow}
  \mathcal{A}
    \overset{H \cdot (-)}{\longrightarrow}
  \mathcal{A}
    \overset{H \cdot (-)}{\longrightarrow}
  \mathcal{A}
    \to
   \cdots
$$

is a [[chain complex]].

The [[cochain cohomology]] of this [[cochain complex]] 

$$
  H^{even/odd}_{H\cdot}(\mathcal{A})
  \coloneqq; 
  \frac{
    ker
    \left(
      \mathcal{A}_{even/odd}
       \overset{H \cdot(-)}{\longrightarrow}
      \mathcal{A}_{odd/even}
     \right)
   }{
    im
    \left(
      \mathcal{A}_{odd/even}
       \overset{H\cdot(-)}{\longrightarrow}
      \mathcal{A}_{even/odd}
     \right)
   }
$$

is the _H-cohomology_ of $\mathcal{A}$. 

=--

## Properties

+-- {: .num_prop #TwistedDeRhamCohomologyCoincidesWithHCohomologyOnInfinitesimllayThickenedPoint}
###### Proposition

If the [[de Rham complex]] $(\Omega^\bullet(X),d_{dr})$ is [[formal dg-algebra|formal]], then for $H \in \Omega_{cl}^3(X)$ a [[closed differential form|closed]] [[differential 3-form]], the H-cohomology of $X$ (def. \ref{HCohomology}) coincides with its $H$-[[twisted de Rham cohomology]]:

$$
  H^\bullet_{H \wedge (-)}(X)
  \simeq
  H^\bullet_{d + H \wedge (-)}(X)
  \,.
$$ 

=--

([Cavalcanti 03, theorem 1.6](#Cavalcanti03)).


## Examples

### The decomposed supergravity C-field 
 {#SupergravityCFieldAfterSplitting}

We discuss the H-cohomology (def. \ref{HCohomologyInGradedCommutativeAlgebra}) of the canonical degree-3 element in the _[[DF-algebra]]_, which serves as a [[supergeometry|super]]-[[exceptional geometry]]-[[tangent space]]-wise model of the [[supergravity C-field]]

#### The DF-Algebra

Let 

$$
  \label{DFAlgberaAtsIsMinus6}
  \begin{aligned}
  &
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})
  \\
  & \coloneqq\;
  Sym\left(
     (
      \underset{
        deg = (1,even)
      }{
      \underbrace{
       e^{a}
      }}
     )_{a \in \{0,1,\cdots, 10\}}
     \,,
     (
      \underset{
        deg = (1,even)
      }{
      \underbrace{
       B^{a b}
       =
       - B^{b a}
      }}
     )_{a,b \in \{0,1,\cdots, 10\}}
     \,,
     (
      \underset{
        deg = (1,odd)
      }{
      \underbrace{
       \psi^\alpha
      }}
     )_{\alpha \in \{1,\cdots, 32\}}
     \,,
     (
      \underset{
        deg = (1,odd)
      }{
      \underbrace{
       \eta^\alpha
      }}
     )_{\alpha \in \{1,\cdots, 32\}}
  \right)
  \end{aligned}
$$

be the $\mathbb{Z} \times (\mathbb{Z}/2)$-bi-[[graded-commutative algebra]] which is freely [[generators and relations|generated]] over the [[field]] of [[real numbers]] as shown.

Here for $\alpha_1$, $\alpha_2 \in CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})$ two elements of homogeneous bi-degree $(n_1, \sigma_1), (n_2, \sigma_2) \in \mathbb{Z} \times (\mathbb{Z}/2)$, respectively, the sign rule is

$$
  \alpha_1 \wedge \alpha_2
  \;=\;
  (-1)^{n_1 n_2 + \sigma_1 \sigma_2}
  \,
  \alpha_2
  \wedge
  \alpha_1
  \,.
$$

(See at _[[signs in supergeometry]]_ the section _[the sign rule from internalization](signs+in+supergeometry#TheSignRuleFromInternalization)_.)

This is the graded-commutative algebra that underlies the _[[DF-algebra]]_ at parameter $s = -6$, which in turn is the [[Chevalley-Eilenberg algebra]] of a [[super Lie algebra]] that is a fermionic extension of the "[[M-theory super Lie algebra]]" ([Bandos-Azcarraga-Izquierdo-Picon-Varela 04, section 3](M-theory+supersymmetry+algebra#BandosAzcarragaIzquierdoPiconVarela04), based on [D'Auria-Fré 82, section 6](M-theory+supersymmetry+algebra#DAuriaFre82)).


There is an [[action]] of the [[Spin group]] $Spin(10,1)$ on the algebra $CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})$ (eq:DFAlgberaAtsIsMinus6) which 

1. on the [[linear span]] of the $(e^a)$ is the defining [[representation]] of the [[proper orthochronous Lorentz group]] (i.e. the _[[vector representation]]_), 

1. on the [[linear span]] of the $(B^{ab} = - B^{b a})$ the corresponding [[bivector]] representation;

1. on the [[linear span]] of the $(\psi^\alpha)$ as well as on that of the $(\eta^\alpha)$ is the [[real spin representation]] $\mathbf{32}$ (the [[Majorana-Weyl spinor]] representation of $Spin(10,1)$).

We write

$$
  \label{SpinInvariantPartOfDFAlgebra}
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})^{Spin(10,1)}
  \hookrightarrow
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})
$$

for the [[invariant]] part of the algebra under this [[spin group]]-[[action]].

In the following we use the [[Einstein summation convention]] with respect to the [[Minkowski metric]] on $\mathbb{R}^{10,1}$. For example

$$
  e^a \wedge B_a{}^b
  \;\coloneqq\;
  - e^0 B^{0 b} 
  +
  \underset{a \in \{1, \cdots, 10\}}{\sum}
  e^a \wedge B^{a b}
$$

for vector indices, and 

$$
  \begin{aligned}
    \overline{\psi} \Gamma_a \eta 
    & \coloneqq
    \overline{\psi}_\alpha (\Gamma_a)^\alpha{}_\beta \eta^\beta 
    \\
    & \coloneqq
    \underset{
      \alpha,\beta \in \{1, \cdots, 32\}
    }{\sum} 
    \overline{\psi}_\alpha (\Gamma_a)^\alpha{}_\beta \eta^\beta 
  \end{aligned} 
$$

for spinor indices, where $(\Gamma_a)$ is a [[representation]] of the [[Clifford algebra]]  and where $\overline{-}$ denotes the [Majorana conjugate](Majorana+spinor#MajoranaConjugation) or equivalently (by [this prop.](Majorana+spinor#TheMajoranaConditionInComponents)) the [Dirac conjugate](Majorana+spinor#DiracConjugate).

In terms of this notation, the $Spin(10,1)$-[[invariants]] are precisely those elements "all whose indices are contracted via the [[Einstein summation convention]]". For example

$$
  \overline{\psi}
    \Gamma_{a b}
  \eta
  \wedge
  B^{a b}
  \;\in\;
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})^{Spin(10,1)}
  \,.
$$


There is a [[differential]] on (eq:DFAlgberaAtsIsMinus6), making it a [[differential graded-commutative algebra]], that extends the [[Chevalley-Eilenberg algebra]] of the [[super Minkowski spacetime]] $\mathbb{R}^{10,1\vert\mathbf{32}}$ and such that the image of the 3-form $H$ below in (eq:CFieldAtSMinusSix) under this differential is the the [[M2-brane]] [[higher WZW term]] $\mu_{M2} \coloneqq \tfrac{i}{2}\overline{\psi} \Gamma_{a b} \psi \wedge e^a \wedge e^b$).
This is what makes the [[DF-algebra]] interesting in itself. But since this differential  plays no role for the discussion of just H-cohomology (def. \ref{HCohomologyInGradedCommutativeAlgebra}), it is of no concern here.



#### The decomposed C-field

In the [[DF-algebra]] (eq:DFAlgberaAtsIsMinus6), consider the following element of bi-degree $(3,even)$

$$
  \label{CFieldAtSMinusSix}
  \begin{aligned}
    H
    & \coloneqq\;
    \underset{
      H_{(1)}
    }{
    \underbrace{
     \tfrac{1}{4!}
     B_{a b} \wedge e^a \wedge e^b  
    }}
    \\
    & \phantom{\coloneqq}
    \underset{
      H_{(2)}
    }{
    \underbrace{
     - \tfrac{1}{3 \cdot 5!}
     B^a{}_b \wedge B^c{}_c \wedge B^c{}_a
    }}
    \\
    & \phantom{\coloneqq}
    +
    \underset{
      H_{(ferm)}
    }{
    \underbrace{
    \tfrac{i}{4 \cdot 5!}
    \overline{\eta}
    \left(
      10 \Gamma_a e^a
      +
      i \Gamma_{a b} B^{a b}
    \right)
    \psi
    }}
  \end{aligned}
  \,.
$$

([Bandos-Azcarraga-Izquierdo-Picon-Varela 04, (37)](M-theory+supersymmetry+algebra#BandosAzcarragaIzquierdoPiconVarela04))

We want to compute the H-cohomology (def. \ref{HCohomologyInGradedCommutativeAlgebra})of this element.

**Strategy:** Compute the H-cohomology of each summand in (eq:CFieldAtSMinusSix) separately with the technique from ([Ševera 05, p. 1](#Severa05)), then use the [[spectral sequence of a double complex]], twice, to put the results together.


#### Number operators

For an analyzing the $H$-cohomology of (eq:CFieldAtSMinusSix) it will be useful to consider various countings of numbers of generators.

First of all there is the plain number of generators:

Write 

$$
  n_e, n_b 
   \;\colon\;
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})
  \longrightarrow
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})
$$

for the [[linear maps]] which on [[monomials]] are given by multiplication with the number of generators $e^a$ or the number of generators $B^{a b}$, respectively.

These are equivalently given by

$$
  n_e 
  \;=\;
  e^a \wedge \partial_{e^a}
$$

and

$$
  \label{BNumber}
  n_B
  \;=\;
  \tfrac{1}{2} B^{a}{}_b \wedge \partial_{B^{a}{}_b}
$$

Then there are mixed number operator, which are more subtle. We write:

$$
  \label{BBNumber}
  n_{B,B}
  \;\coloneqq\;
  -
  \frac{1}{4}
  B^{a}{}_b \wedge B^b{}_a
  \wedge
  \partial_{B^a{}_b} \partial_{B^b{}_a}
  \,.
$$

In order to understand these, consider the further subalgebra

$$
  \label{BSimplePartOfDFAlgebra}
  CE\left(
    T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}}
  \right)^{Spin(10,1)}_{B simp}
    \hookrightarrow
  CE\left(
    T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}}
  \right)^{Spin(10,1)}
$$

of the $Spin(10,1)$-[[invariant]] part of the [[DF-algebra]] (eq:SpinInvariantPartOfDFAlgebra) of these elements which do not contain contractions $B^{a}{}_{b}\wedge B^b{}_c$ of $B$-s with themselves.

{#nBBVanishesOnBSimpleSubalgebra} **Claim**. The mixed number operator $n_{B,B}$ (eq:BBNumber) vanishes on the subalgebra (eq:BSimplePartOfDFAlgebra).

Proof: Observe that $n_{B,B}$ commutes with the $Spin(10,1)$-action (since its algebraic expression has all indices contracted correctly). But if $n_{B,B}$ hits an invariant term with more than one $B$-generator in it, but not contracted among themselves, then the result breaks the Einstein summation-pattern of the indices, and hence is not $Spin(10,1)$-invariant anymore, unless it vanishes. 



#### The first summand

We discuss the H-cohomology (def. \ref{HCohomologyInGradedCommutativeAlgebra}) of the first summand in (eq:CFieldAtSMinusSix)

$$
  H_{(1)}
  \;\coloneqq\;
  B_{a b} \wedge e^a \wedge e^b  
$$


It is clear that $H_{(1)}$ has non-trivial H-cohomology 

* at $n_e = 10, 11, b_B = 0$

  given by elements that are proportional to the wedge product of all 11 or least least 10 factors of the generators $e^a$ (this makes these monomials be in the kernel of $H_{(1)}\wedge (-)$), and contain no factor of $B^{a b}$ (this makes them be not in the image of $H_{(1)}\wedge(-)$);

* $n_B = 55, n_1 = 0, 1$

  given by elements proportional to the product of all 55 factors of the generators $B^{a b}$ (this makes these elements be in the kernel of $H_{(1)} \wedge (-)$) and containing at most one factor of $e^a$ (this makes them be not in the image of $H_{(1)} \wedge (-)$).

In order to see if we can trivialize the $H_{(1)}$-cohomology away from these values, we consider as candidate [[homotopy operator]]
the graded [[derivation]] on the [[DF-algebra]] $CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})$ (eq:DFAlgberaAtsIsMinus6) given by

$$
  L_{(1)}
  \coloneqq
  \partial_{B_{ab}}\partial_{e^a}\partial_{e^b}
$$

Its graded commutator with $H_{(1)}$ (eq:CFieldAtSMinusSix) is the following:

$$
  \begin{aligned}
    & 
    L_{(1)} H_{(1)}\wedge(-)
    +
    H_{(1)}\wedge L_{(1)} (-)
    \\
    & = 
    \partial_{B_{a' b'}}\partial_{e^{a'}}\partial_{e^{b'}}
    B_{a b} \wedge e^a \wedge e^b\wedge (-)
    +
    B_{a b} \wedge e^a \wedge e^b\wedge 
    \partial_{B_{a' b' }}\partial_{e^{a'}}\partial_{e^{b'}}
    (-)
    \\
    & 
    =
    2
    \partial_{B_{a' b}}\partial_{e^{a'}}
    B_{a b} \wedge e^a \wedge (-)
    -
    \partial_{B_{a' b'}}\partial_{e^{a'}}
    B_{a b} \wedge e^a \wedge e^b\wedge \partial_{e^{b'}} (-)
    +
    B_{a b} \wedge e^a \wedge e^b\wedge 
    \partial_{B_{a' b'}}\partial_{e^{a'}}\partial_{e^{b'}}(-)
    \\
    & =
    -
    2
    \partial_{B_{a b}}
    B_{a b} \wedge  (-)
    +
    \underset{
      = 
      4
      \partial_{B_{a' b}}
      B_{a b} \wedge e^a\wedge \partial_{e^{a'}} (-)
    }{
    \underbrace{
    2
    \partial_{B_{a' b}}
    B_{a b} \wedge e^a\wedge \partial_{e^{a'}} (-)
    +
    2
    \partial_{B_{a b'}}
    B_{a b} \wedge e^b\wedge \partial_{e^{b'}} (-)
    }}
    +
    \partial_{B_{a' b'}}
    B_{a b} \wedge e^a \wedge e^b\wedge \partial_{e^{a'}}\partial_{e^{b'}} (-)
    +
    B_{a b} \wedge e^a \wedge e^b\wedge 
    \partial_{B_{a' b'}}\partial_{e^{a'}}\partial_{e^{b'}}
    (-)
    \\   
    & =
    -
    220 \cdot
    (-)
    +
    2 B_{a b} \wedge \partial_{B_{a b}} (-)
    +
    40
    e^a \wedge \partial_{e^a}(-)
    +
    4 B_{a b} \wedge e^a \partial_{B_{a' b}} \partial_{e^{a'}}(-)
    +
    2 e^a \wedge e^b\wedge \partial_{e^a}\partial_{e^b} (-)
    \\
    & =
    ( - 220 + 4 n_B + 40 n_e - 4 n_{e,B} - 2 n_e(n_e - 1)) \cdot (-)
    \\
    & =
    ( - 220 + 4 n_B + 42 n_e - 4 n_{e,B} - 2 n_e^2) \cdot (-)
  \end{aligned}
$$

If follows that a sufficient condition for $H_{(1)}$-cohomology to vanish on a subspace of forms is that 

$$
  ( - 220 + 4 n_B + 41 n_e - 4 n_{e,B} - 2 n_e^2)
$$

is invertible on this subspace. 

As special cases we recover the cohomology classes already observed above:

* $n_B = 0$ and 
  
  $\underset{-2(n_e - 10)(n_e - 11)}{\underbrace{- 220 + 42 n_e -2 n_e} }= 0$

  which is equivalent to 

  $n_B = 0$ and $ n_e = 10, \, 11$

* $n_e = 0$ and $- 220 + 4 n_B = 0$ 

  which is equivalent to 

  $n_e = 0$ and $n_B = 55$


#### The second summand
  {#TheSecondSummand}

We discuss the H-cohomology (def. \ref{HCohomologyInGradedCommutativeAlgebra}) of the second summand in (eq:CFieldAtSMinusSix)

$$
  H_{(2)}
  \;\coloneqq\;
  B^a{}_b \wedge B^b{}_c \wedge B^c{}_a
  \,.
$$

As a candidate [[homotopy operator]], consider

$$
  L_{(2)}
  \;\coloneqq\;
  \partial_{B^{a}{}_b}
  \partial_{B^{b}{}_c}
  \partial_{B^{c}{}_a}
$$

We compute the anticommutator of this with $H_{(2)}$:

$$
  \begin{aligned}
    & 
    L_{(2)} H_{(2)} \wedge (-)
    +
    H_{(2)} \wedge L_{(2)} (-)
    \\ 
    & =    
    \partial_{B^{a'}{}_{b'}}
    \partial_{B^{b'}{}_{c'}}
    \partial_{B^{c'}{}_{a'}}
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge(-)
    +
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{a'}{}_{b'}}
    \partial_{B^{b'}{}_{c'}}
    \partial_{B^{c'}{}_{a'}}
    (-)
    \\
    & =
    6
    \partial_{B^{a}{}_{b'}}
    \partial_{B^{b'}{}_{c}}
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    (-)
    \\
    & \phantom{=}
    -
    \partial_{B^{a'}{}_{b'}}
    \partial_{B^{b'}{}_{c'}}
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{c'}{}_{a'}}
    (-)
    \\
    & \phantom{=}
    +
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{a'}{}_{b'}}
    \partial_{B^{b'}{}_{c'}}
    \partial_{B^{c'}{}_{a'}}
    (-)
    \\
    & =
    \underset{
      -54
      \partial_{B^{a}{}_{b}}
      B^a{}_{b}
      \wedge
      (-)
    }{
    \underbrace{
    -6
    \partial_{B^{a}{}_{b}}
    B^b{}_{a}
    \wedge
    -
    60
    \partial_{B^{a}{}_{b}}
    B^a{}_{b}
    \wedge
    (-)
    }
    }
    +
    6
    \partial_{B^{a}{}_{b'}}
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    \partial_{B^{b'}{}_{c}}
    (-)
    \\
    & \phantom{=}
    +
    6
    \partial_{B^{a'}{}_{b}}
    B^a{}_{b}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{c}{}_{a'}}
    (-)
    +
    \partial_{B^{a'}{}_{b'}}
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{b'}{}_{c'}}
    \partial_{B^{c'}{}_{a'}}
    (-)
    \\
    & \phantom{=}
    +
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{a'}{}_{b'}}
    \partial_{B^{b'}{}_{c'}}
    \partial_{B^{c'}{}_{a'}}
    (-)
    \\
    & =
    - 54 \cdot 110
    \cdot
    (-)
    +
    54 B^a{}_b \partial_{B^a{}_b} (-)
    + 
    \underset{
      54 B^b{}_c \wedge \partial_{B^b{}_c}(-)
    }{
    \underbrace{
    60 B^b{}_c \wedge \partial_{B^b{}_c}(-)
    +
    6
    B^a{}_{b} \wedge \partial_{B^{b}{}_a}(-)
    }
    }
    +
    6 B^{a}{}_b \wedge B^{b}{}_c \partial_{B^{a}{}_{b'}} \partial_{B^{b'}{}_c} (-)
    \\
    & \phantom{=} 
    +
    \underset{
      54
      B^c{}_{a}
      \wedge
      \partial_{B^{c}{}_{a}}
      (-)       
    }{
    \underbrace{
    60
    B^c{}_{a}
    \wedge
    \partial_{B^{c}{}_{a}}
    (-)
    +
    6
    B^a{}_{b} \wedge \partial_{B^b{}_{a}} (-)
    }
    }
    +
    6
    B^a{}_{b}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{a'}{}_{b}}
    \partial_{B^{c}{}_{a'}}
    (-)
    +
    6
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{b}{}_{c'}}
    \partial_{B^{c'}{}_{a}}
    (-)
    -
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{a'}{}_{b'}}
    \partial_{B^{b'}{}_{c'}}
    \partial_{B^{c'}{}_{a'}}
    (-)
    \\
    & \phantom{=}
    +
    B^a{}_{b}
    \wedge
    B^b{}_{c}
    \wedge
    B^c{}_{a}
    \wedge
    \partial_{B^{a'}{}_{b'}}
    \partial_{B^{b'}{}_{c'}}
    \partial_{B^{c'}{}_{a'}}
    (-)
    \\
    & =
    \left(
      - 54 \cdot 110
      +
      54 \cdot \tfrac{3}{2} \cdot n_B
      -
      6 \cdot 3 \cdot 4
      n_{B,B}
    \right)
    \cdot
    (-)
  \end{aligned}
$$

Where in the last line we identified the number operators $n_B$ (eq:BNumber) and $n_{B,B}$ (eq:BBNumber).

It follows by [this claim](#nBBVanishesOnBSimpleSubalgebra) that restricted to the subalgebra  $CE\left( T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}} \right)^{Spin(10,1)}_{B simp}$ (eq:BSimplePartOfDFAlgebra) the anticommutator is

$$
    \left(
      - 54 \cdot 110
      +
      54 \cdot \tfrac{3}{2} \cdot n_B
    \right)
    \cdot
    (-)
$$

But this is an [[isomorphism]] (since $n_B$ is an integer on any [[monomial]], so that the action on any monomial is by multiplication with a non-vanishing number). Hence the $H_{(2)}$-cohomology vanishes on $CE\left( T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}} \right)^{Spin(10,1)}_{B simp}$ (eq:BSimplePartOfDFAlgebra).

But this implies that the full $(H = H_{(1)} + H_{(2)} + H_{(3)})$-cohomology vanishes on this subalgebra:

because if we decompose the underlying $H$-chain complex as the [[double complex]] with $d_1 \coloneqq H_{(2)}$ and $d_2 \coloneqq H_{(1)} + H_{(3)}$, then the corresponding [[spectral sequence of a double complex]] has vanishing second page when restricted to $CE\left( T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}} \right)^{Spin(10,1)}_{B simp}$ (eq:BSimplePartOfDFAlgebra).

(?)




## References

The terminology "$H$-cohomology" is used in

* {#Cavalcanti03} [[Gil Cavalcanti]], _New aspects of the $d d^c$-lemma_ ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))

The case of H-cohomology for $H = \omega$ a graded symplectic form (as on a [[Poisson Lie algebroid]] regarded as a  [[symplectic Lie n-algebroid]]) is considered in

* {#Severa05} [[Pavol Ševera]], p. 1 of _On the origin of the BV operator on odd symplectic supermanifolds_, Lett Math Phys (2006) 78: 55. ([arXiv:0506331](https://arxiv.org/abs/math/0506331))

[[!redirects H-cohomology group]]
[[!redirects H-cohomology groups]]
