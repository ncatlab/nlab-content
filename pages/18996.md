

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

### The supergravity C-field after splitting

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

Here for $\alpha_1$, $\alpha_2 \in CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})$ two elements of homogeneous bi-degree $(n_1, \sigma_1)$ and $(n_2, \sigma_2)$, respectively, the sign rule is

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

The [[differential]] on this CE-algebra, while of crucial for the role of the [[DF-algebra]] as such, is of no concern for the following discussion of H-chomology in this algebra.

In the following we use the [[Einstein summation convention]] with respect to the [[Minkowski metric]] on $\mathbb{R}^{10,1}$. For example

$$
  e^a \wedge B_a{}^b
  \;\coloneqq\;
  - e^0 B^{0 b} 
  +
  \underset{a \in \{1, \cdots, 10\}}{\sum}
  e^a \wedge B^{a b}
  \,.
$$

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

We want to compute the H-cohomology of this element.

**Strategy:** Compute the H-cohomology of each summand in (eq:CFieldAtSMinusSix) separately with the technique from ([Ševera 05, p. 1](#Severa05)), then use the [[spectral sequence of a double complex]], twice, to put the results together.


#### The first summand

We discuss the H-cohomology of the first summand in (eq:CFieldAtSMinusSix)

$$
  H_{(1)}
  \;\coloneqq\;
  B_{a b} \wedge e^a \wedge e^b  
$$

Write 

$$
  n_e, b_B \;\colon\;
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})
  \longrightarrow
  CE(T_{exc,-6}\mathbb{R}^{10,1\vert\mathbf{32}})
$$

for the [[linear maps]] which on [[monomials]] are given by multiplication with the number of generators $e^a$ or the number of generators $B^{a b}$, respectively.

It is clear that $H_{(1)}$ has non-trivial H-cohomology 

* at $n_e = 10, 11, b_B = 0$;

* $n_B = 55, n_1 = 0, 1$.

In order to see if we can trivialize the $H_{(1)}$-cohomology away from these values we consider as candidate [[homotopy operator]]
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

is non-zero on this subspace. As special cases we recover the two situations already seen above:

* $n_B = 0$ and $-2 n_e^2 + 42 n_e - 220 = 0$

  which is equivalent to 

  $n_B = 0$ and $ n_e = 10, 11$

* $n_e = =$ and $n_B =55$



## References

The terminology "$H$-cohomology" is used in

* {#Cavalcanti03} [[Gil Cavalcanti]], _New aspects of the $d d^c$-lemma_ ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))

The case of H-cohomology for $H = \omega$ a graded symplectic form (as on a [[Poisson Lie algebroid]] regarded as a  [[symplectic Lie n-algebroid]]) is considered in

* {#Severa05} [[Pavol Ševera]], p. 1 of _On the origin of the BV operator on odd symplectic supermanifolds_, Lett Math Phys (2006) 78: 55. ([arXiv:0506331](https://arxiv.org/abs/math/0506331))

[[!redirects H-cohomology group]]
[[!redirects H-cohomology groups]]
