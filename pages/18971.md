[[!redirects vertex redefinitions]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[perturbative quantum field theory]] an ([[adiabatic switching|adiabatically switch]]) [[interaction]] [[action functional]] is a [[local observable]] of the form

$$
  g S_{int} + j A
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
  \,.
$$

In the [[Feynman perturbation series]] this is interpreted as the label of [[vertices]] in [[multigraphs]] underlying [[Feynman diagrams]] which encode [[field (physics)|field]] [[interactions]] at that point.


In the process of [[renormalization|(re-)normalization]] of [[perturbative QFT]] one considers redefinitions of such "interaction vertices" by terms of higher order in the [[coupling constant]] $g$  ad [[source field]] $j$:


$$
  \mathcal{Z}
  \;\colon\;
  g S_{int} + j A
  \;\mapsto\;
  g S_{int} + j A
  +
  \underset{
    \mathcal{O}(g^2, j^2, g j)
  }{
  \underbrace{   
    S_{counter}
  }}
  \,.
$$

In the context of [[effective QFT]] via [[UV cutoffs]], the correction term $S_{counter}$ is called a _[[counterterm]]_.

Under mild assumptions, such _interaction vertex redefinitions_ form a [[group]], called the _[[Stückelberg-Petermann renormalization group]]_. See there for more.

## Definition


+-- {: .num_defn #InteractionVertexRedefinition}
###### Definition
**([[perturbative interaction vertex redefinition]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)).

A _[[perturbative interaction vertex redefinition]]_ (or just _[[vertex redefinition]]_, for short) is an [[endofunction]]

$$
  \mathcal{Z}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

on [[local observables]] with formal parameters adjoined ([this def.](S-matrix#FormalParameters)) such that there exists a sequence $\{Z_k\}_{k \in \mathbb{N}}$ of [[continuous linear functionals]], symmetric in their arguments, of the form

$$
  \left(
    {\, \atop \,}
    LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    {\, \atop \,}
  \right)^{\otimes^k_{\mathbb{C}[ [ \hbar, g, j] ]}}
  \longrightarrow
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

such that for all $g S_{int} + j A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle$ the following conditions hold:

1. (perturbation) 

   1. $Z_0(g S_{int + j A}) = 0$

   1. $Z_1(g S_{int} + j A) = g S_{int} + j A$

   1. and

      $$
        \begin{aligned}
          \mathcal{Z}(g S_{int} + j A)
          & =
          Z \exp_\otimes( g S_{int} + j A )
          \\
          &
          \coloneqq
          \underset{k \in \mathbb{N}}{\sum}
          \frac{1}{k!}
          Z_k(
            \underset{
              k \, \text{args}
            }{
              \underbrace{
                g S_{int} + j A , \cdots, g S_{int} + j A
              }
            }
          )
        \end{aligned}
      $$

1. (field independence) The [[local observable]] $\mathcal{Z}(g S_{int} + j A)$ depends on the [[field histories]] only through its argument $g S_{int} + j A $, hence by the [[chain rule]]:

   $$
     \label{FieldIndependenceVertexRedefinition}
     \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
     \mathcal{Z}(g S_{int} + j A)
     \;=\;
     \mathcal{Z}'_{g S_{int} + j A}
     \left(
         \frac{\delta}{\delta \mathbf{\Phi}^a(x)} (g S_{int} + j A) 
     \right)
   $$

=--

## Properties

The following proposition should be compared to the axiom of _[[causal additivity]]_ of the [[S-matrix]] scheme ([this equation](S-matrix#eq:CausalAdditivity)):

+-- {: .num_prop #InteractionVertexRedefinitionAdditivity}
###### Proposition
**(local additivity of [[vertex redefinitions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)) and let $\mathcal{Z}$ be a [[vertex redefinition]] (def. \ref{InteractionVertexRedefinition}).

Then for all [[local observables]] $O_0, O_1, O_2 \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j ] ]\langle g, j\rangle$ with spacetime support denoted $supp(O_i) \subset \Sigma$ ([this def.](A+first+idea+of+quantum+field+theory#SpacetimeSupport)) we have

1. (local additivity)

   $$
     \begin{aligned}
       &
       \left(
         supp(O_1)
         \cap
         supp(O_2)
         = 
         \emptyset
       \right)
       \\
       &
         \Rightarrow
       \phantom{AA}
       \mathcal{Z}( O_0 + O_1 + O_2)
       =
       \mathcal{Z}( O_0 + O_1 ) - \mathcal{Z}(O_0) + \mathcal{Z}(O_0 + O_2)
     \end{aligned}
     \,.
   $$

1. (preservation of spacetime support)

   $$
     supp
     \left(
       {\, \atop \,}
         \mathcal{Z}(O_0 + O_1)
         -
         \mathcal{Z}(O_0)
       {\, \atop \,}
     \right)
     \;\subset\;
     supp(O_1)
   $$

   hence in particular

   $$
     supp
     \left(
       {\, \atop \,}
       \mathcal{Z}(O_1)
       {\, \atop \,}
     \right) = supp(O_1)
   $$

=--

([Dütsch 18, exercise 3.98](#Duetsch18))

+-- {: .proof}
###### Proof

Under the inclusion

$$
  LocObs(E_{\text{BV-BRST}})
    \hookrightarrow
  PolyObs(E_{\text{BV-BRST}})
$$

of [[local observables]] into [[polynomial observables]] we may think of each $Z_k$ as a [[generalized function]], as for [[time-ordered products]] in [this remark](S-matrix#NotationForTimeOrderedProductsAsGeneralizedFunctions).

Hence if

$$
  O_j = \underset{\Sigma}{\int} j^\infty_\Sigma( \mathbf{L}_j )
$$

is the [[transgression of variational differential forms|transgression]] of a [[Lagrangian density]] $\mathbf{L}$ we get

$$
  Z_k(
    (O_1 + O_2 + O_3)
    ,
    \cdots
    ,
    (O_1 + O_2 + O_3)
  )
  =
  \underset{
    j_1, \cdots, j_k \in \{0,1,2\}
  }{\sum}
  \underset{\Sigma^{k}}{\int}
    Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
  \,.
$$

Now by definition $Z_k(\cdots)$ is in the subspace of [[local observables]], i.e. those [[polynomial observables]] whose [[coefficient]] [[distributions]] are [[support of a distribution|supported]] on the [[diagonal]], which means that 

$$
  \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
  \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
  Z_{k}(\cdots) 
  = 
  0
  \phantom{AA}
  \text{for}
  \phantom{AA}
  x \neq y
$$

Together with the axiom "field independence" (eq:FieldIndependenceVertexRedefinition) this means that the support of these generalized functions in the [[integrand]] here must be on the [[diagonal]], where $x_1 = \cdots = x_k$.

By the assumption that the spacetime supports of $O_1$ and $O_2$ are disjoint, this means that only the summands with $j_1, \cdots, j_k \in \{0,1\}$ and those with $j_1, \cdots, j_k \in \{0,2\}$ contribute to the above sum. Removing the overcounting of those summands where all $j_1, \cdots, j_k \in \{0\}$ we get


$$
  \begin{aligned}
    & Z_k\left(
      {\, \atop \,}
      (O_1 + O_2 + O_3)
      ,
      \cdots
      ,
      (O_1 + O_2 + O_3)
      {\, \atop \,}
    \right)
    \\
    & =
    \underset{
      j_1, \cdots, j_k \in \{0,1\}
    }{\sum}
    \underset{\Sigma^{k}}{\int}
      Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
    \\
    & \phantom{=}
    -
    \underset{
      j_1, \cdots, j_k \in \{0\}
    }{\sum}
    \underset{\Sigma^{k}}{\int}
      Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
    \\
    & \phantom{=}
    -
    \underset{
      j_1, \cdots, j_k \in \{0,2\}
    }{\sum}
    \underset{\Sigma^{k}}{\int}
      Z( \mathbf{L}_{j_1}(x_1) , \cdots , \mathbf{L}_{j_k}(x_k) )
    \\
    & =
    Z_k\left( {\, \atop \,} (O_0 + O_1), \cdots, (O_0 + O_1) {\, \atop \,}\right)
    -
    Z_k\left( {\, \atop \,} O_0, \cdots,  O_0 {\, \atop \,} \right)
    +
    Z_k\left( {\, \atop \,} (O_0 + O_2), \cdots, (O_0 + O_2) {\, \atop \,} \right)
  \end{aligned}
  \,.
$$

This directly implies the claim.

=--

## References

The original discussion is due to 

* {#StueckelbergPetermann53} [[Ernst Stückelberg]], [[André Petermann]], _La normalisation des constantes dans la theorie des quanta_, Helv. Phys. Acta 26 (1953), 499–520

in the context of the [[Stückelberg-Petermann renormalization group]]. 


For more see the references there and those at _[[main theorem of perturbative renormalization]]_.


[[!redirects perturbative interaction vertex redefinition]]
[[!redirects perturbative interaction vertex redefinitions]]

[[!redirects interaction vertex redefinition]]
[[!redirects interaction vertex redefinitions]]

[[!redirects vertex redefinition]]
[[!redirects vertex redefinitions]]

