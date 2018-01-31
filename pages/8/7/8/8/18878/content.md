

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

In [[perturbative quantum field theory]] the _Stückelberg-Petermann renormalization group_ ([Stückelberg-Petermann 53](#StiecelbergPetermann53)) is the (original) incarnation of the [[renormalization group]] in the perspective of [[causal perturbation theory]]: It is the group (def. \ref{StueckelbergPetermannRenormalizationGroup} below) of perturbative [[interaction vertex redefinitions]] (def. \ref{InteractionVertexRedefinition}) which is such that any two choices of [[S-matrix]] [[renormalization schemes]] $\mathcal{S}, \mathcal{S}'$ are related by a unique [[vertex redefinition]] $\mathcal{Z}$ via [[precomposition]]

$$
  \mathcal{S}'
  \;=\;
  \mathcal{S} \circ \mathcal{Z}
  \,.
$$

This statement (prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition} below) is also called the _[[main theorem of perturbative renormalization]]_.

If [[scaling transformations]] on [[spacetime]] happen to transform [[renormalization schemes]] into each other, then this [[main theorem of perturbative renormalization]] (prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}) directly implies that every [[scaling transformation]] uniquely corresponds to a [[interaction vertex redefinition]], or conversely that the [[vertex redefinitions]] are given as funcitons of scale. As such they are also referred to as _[[running coupling constants]]_ (def. \ref{GellMannLowTransformations} below). Beware that these do not in general form a [[group]] but a [[group cocycle]], the _[[Gell-Mann-Low renormalization cocycle]]_ (prop. \ref{CocyclePropertyOfRunningCouplingConstants} below.


## Definition

The elements of the Stückelberg-Petermann renormalization group are _perturbative [[interaction vertex redefinitions]]_ (def. \ref{InteractionVertexRedefinition} below). These [[action|act]] on [[S-matrix]] [[renormalization schemes|("re"-)normalization schemes]] by [[precomposition]] (def. \ref{CausalFactorizationSatisfiedByCompositionOfSMatrixWithVertexRedefinition}) and this action is [[free action|free]] and [[transitive action|transitive]] (prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition} below). In this way these [[vertex redefinitions]] translate between different choices of [[renormalization|("re"-)normalization]], and as such they form the _Stückelerg-Petermann renormalization group_ (def. \ref{StueckelbergPetermannRenormalizationGroup}) below.

$\,$

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
    Z_k\left( {\, \atop \,} (O_0 + O_1), \cdots, (O_0 + O_1) {\, \atop \,} \right)
  \end{aligned}
  \,.
$$

This directly implies the claim.

=--

As a corollary we obtain:

+-- {: .num_prop #CausalFactorizationSatisfiedByCompositionOfSMatrixWithVertexRedefinition}
###### Proposition
**([[composition]] of [[S-matrix]] scheme with [[vertex redefinition]] is again [[S-matrix]] scheme)**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)) and let $\mathcal{Z}$ be a [[vertex redefinition]] (def. \ref{InteractionVertexRedefinition}).

Then for

$$
  \mathcal{S}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g,j ] ]
$$

and [[S-matrix]] scheme ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering)), the [[composition|composite]]

$$
  \mathcal{S} \circ \mathcal{Z}
  \;\colon\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \overset{\mathcal{Z}}{\longrightarrow}
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
    \overset{\mathcal{S}}{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g,j ] ]
$$

is again an [[S-matrix]] scheme.

Moreover, if $\mathcal{S}$ satisfies the [[renormalization condition]] "field independence" ([this prop.](S-matrix#BasicConditionsRenormalization)), then so does $\mathcal{S} \circ \mathcal{Z}$.

=--

(e.g [Dütsch 18, theorem 3.99 (b)](#Duetsch18))

+-- {: .proof}
###### Proof

It is clear that [[causal order]] of the spacetime supports implies that they are in particular [[disjoint subset|disjoint]]

$$
  \left(
    {\, \atop \,}
    supp(O_1)
    {\vee\!\!\!\wedge}
    supp(O_2)
    {\, \atop \,}
  \right)
  \phantom{AA}
  \Rightarrow
  \phantom{AA}
  \left(
    {\, \atop \,}
    supp(O_1)
      \cap
    supp(O_)
    \;=\;
    \emptyset
    {\, \atop \,}
  \right)
$$

Therefore the local additivity of $\mathcal{Z}$ (prop. \ref{InteractionVertexRedefinitionAdditivity})
and the [[causal factorization]] of the [[S-matrix]] ([this remark](S-matrix#DysonCausalFactorization))
imply the causal factorization of the composite:

$$
  \begin{aligned}
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_1 + O_2)
      {\, \atop \,}
    \right)
    & =
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_1)
      +
      \mathcal{Z}(O_2)
      {\, \atop \,}
    \right)
    \\
    & =
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_1)
      {\, \atop \,}
    \right)
    \,
    \mathcal{S}
    \left(
      {\, \atop \,}
      \mathcal{Z}(O_2)
      {\, \atop \,}
    \right)
    \,.
  \end{aligned}
$$

But by [this prop.](S-matrix#CausalFactorizationAlreadyImpliesSMatrix) this implies in turn [[causal additivity]]
and hence that $\mathcal{S} \circ \mathcal{Z}$ is itself an S-matrix scheme.

Finally that $\mathcal{S} \circ \mathcal{Z}$ satisfies "field indepndence" if $\mathcal{S}$ does is immediate by the [[chain rule]], given that $\mathcal{Z}$ satisfies this condition by definition.

=--

+-- {: .num_prop #AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}
###### Proposition
**(any two [[S-matrix]] [[renormalization schemes]] differ by a unique [[vertex redefinition]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)).

Then for $\mathcal{S}, \mathcal{S}'$ any two [[S-matrix]] schemes ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering)) which both satisfy the [[renormalization condition]] "field independence", the  there exists a unique [[vertex redefinition]] $\mathcal{Z}$ (def. \ref{InteractionVertexRedefinition}) relating them by [[composition]], i. e. such  that

$$
  \mathcal{S}'
  \;=\;
  \mathcal{S} \circ \mathcal{Z}
  \,.
$$

=--

(See any of the reference at _[[main theorem of perturbative renormalization]]_.)

+-- {: .proof}
###### Proof

By applying both sides of the equation to linear combinations of local observables of the form $\kappa_1 O_1 + \cdots + \kappa_k O_k$ and then taking [[derivatives]] with respect to $\kappa$ at $\kappa_j = 0$ (as in [this example](S-matrix#TimeOrderedProductsFromSMatrixScheme)) we get that the equation in question implies

$$
  (i \hbar)^k
  \frac{
    \partial^k
  }{
    \partial \kappa_1 \cdots \partial \kappa_k
  }
  \mathcal{S}'( \kappa_1 O_1 + \cdots + \kappa_k O_k )
  \vert_{\kappa_1, \cdots, \kappa_k = 0}
  \;=\;
  (i \hbar)^k
  \frac{
    \partial^k
  }{
    \partial \kappa_1 \cdots \partial \kappa_k
  }
  \mathcal{S} \circ \mathcal{Z}( \kappa_1 O_1 + \cdots + \kappa_k O_k )
  \vert_{\kappa_1, \cdots, \kappa_k = 0}
$$

which in components means that

$$
  \begin{aligned}
    T'_k( O_1, \cdots, O_k )
    & =
    \underset{
      2 \leq n \leq k
    }{\sum}
      \frac{1}{n!}
      (i \hbar)^{k-n}
      \underset{
        { { I_1 \sqcup \cdots \sqcup I_n } \atop { =  \{1, \cdots, k\}, } }
        \atop
        { I_1, \cdots, I_n \neq \emptyset }
      }{\sum}
      \left(
        k \atop { {\vert I_1 \vert}, \cdots , {\vert I_1 \vert} }
      \right)
      T_n
      \left(
        Z_{{\vert I_1\vert}}( (O_{i_1})_{i_1 \in I_1} ),
        \cdots,
        Z_{{\vert I_n\vert}}( (O_{i_n})_{i_n \in I_n} ),
      \right)
  \\
  & \phantom{=}
    +
    Z_k( O_1,\cdots, O_k )
  \end{aligned}
$$

where $\{T'_k\}_{k \in \mathbb{N}}$ are the [[time-ordered product]] corresponding to $\mathcal{S}'$ (by [this example](S-matrix#TimeOrderedProductsFromSMatrixScheme)) and $\{T_k\}_{k \in \mathcal{N}}$ those correspondong to $\mathcal{S}$.

This shows that if $\mathcal{Z}$ exists, then it is unique, because its coefficients $Z_k$ are [[induction|inductively]] in $k$
given by the expressions

$$
  \begin{aligned}
    & Z_k( O_1,\cdots, O_k )
    \\
    & =
    T'_k( O_1, \cdots, O_k )
    \;-\;
    \underset{
      (T \circ \mathcal{Z}_{\lt k})_k
    }{
    \underbrace{
    \underset{
      2 \leq n \leq k
    }{\sum}
      \frac{1}{n!}
      (i \hbar)^{k-n}
      \underset{
        { { I_1 \sqcup \cdots \sqcup I_n } \atop { =  \{1, \cdots, k\}, } }
        \atop
        { I_1, \cdots, I_n \neq \emptyset }
      }{\sum}
      \left(
        k \atop { {\vert I_1 \vert}, \cdots , {\vert I_1 \vert} }
      \right)
      T_n
      \left(
        Z_{{\vert I_1\vert}}( (O_{i_1})_{i_1 \in I_1} ),
        \cdots,
        Z_{{\vert I_n\vert}}( (O_{i_n})_{i_n \in I_n} ),
      \right)
    }
    }
  \end{aligned}
$$

Hence it remains to see that the $Z_k$ defined this way satisfy the conditions in def. \ref{InteractionVertexRedefinition}.

The condition "perturbation" is immediate from the corresponding condition on $\mathcal{S}$ and $\mathcal{S}'$.

Similarly the condition "field independence" follows immediately from the assumoption that $\mathcal{S}$ and $\mathcal{S}'$ satisfy this condition.

It only remains to see that $Z_k$ indeed takes values in [[local observables]]. Give that the [[time-ordered products]] a priori take values in the larrger space of [[microcausal polynomial observables]] this means to show that the spacetime support of $Z_k$ is on the [[diagonal]].

But observe that, as indicated in the above formula, the term over the brace may be understood as the coefficient at order $k$ of the [[exponential series]]-expansion of the [[composition|composite]] $\mathcal{S} \circ \mathcal{Z}_{\lt k}$, where

$$
  \mathcal{Z}_{\lt k}
  \;\coloneqq\;
  \underset{
    n \in \{1, \cdots, k-1\}
  }{\sum}
  \frac{1}{n!} Z_n
$$

is the truncation of the [[vertex redefinition]] to degree $\lt k$. This truncation is clearly itself still
a vertex redefinition (according to def. \ref{InteractionVertexRedefinition}) so that the composite $\mathcal{S} \circ \mathcal{Z}_{\lt k}$
is still an [[S-matrix]] scheme (by prop. \ref{CausalFactorizationSatisfiedByCompositionOfSMatrixWithVertexRedefinition})
so that the $(T \circ \mathcal{Z}_{\lt k})_k$ are [[time-ordered products]] (by [this example](S-matrix#TimeOrderedProductsFromSMatrixScheme)).

So as we solve $\mathcal{S}' = \mathcal{S} \circ \mathcal{Z}$ inductively in degree $k$, then for the induction step in degree $k$ the expressions $T'_{\lt k}$ and $(T \circ \mathcal{Z})_{\lt k}$ agree and are both time-ordered products.
By [this prop.](S-matrix#RenormalizationIsInductivelyExtensionToDiagonal) this implies that  $T'_{k}$ and $(T \circ \mathcal{Z}_{\lt k})_{k}$ agree away from the diagonal. This means that their difference $Z_k$ is supported on the diagonal, and hence is indeed local.

=--

+-- {: .num_defn #StueckelbergPetermannRenormalizationGroup}
###### Definition
**([[Stückelberg-Petermann renormalization group]] of [[vertex redefinitions]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H)$ be a [[gauge fixing|gauge fixed]] [[free field theory|free field]] [[vacuum]] ([this def.](S-matrix#VacuumFree)).

Then prop. \ref{CausalFactorizationSatisfiedByCompositionOfSMatrixWithVertexRedefinition} and prop \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition} together says that ("[[main theorem of perturbative renormalization]]"):

1. the [[vertex redefinitions]] $\mathcal{Z}$ (def. \ref{InteractionVertexRedefinition}) form a [[group]] under [[composition]];

1. the set of [[S-matrix]] [[renormalization schemes|("re"-)normalization schemes]] ([this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering), [this remark](S-matrix#calSFunctionIsRenormalizationScheme)) satisfying at least the [[renormalization condition]] "field indepencen" is a [[torsor]] over this group, in that any two are related by a unique vertex redefinition.

This group is called the (large) _[[Stückelberg-Petermann renormalization group]]_.

Typically one imposes a set of [[renormalization conditions]] ([this def.](S-matrix#RenormalizationConditions))
and then the corresponding [[subgroup]] of [[vertex redefinitions]] preserving these.

=--

## Properties

### Scaling transformations and "running coupling constants"

A priori the Stückelberg-Petermann renormalization group is not about [[scaling transformations]]. But if [[scaling transformations]] happen to produce new S-matrices/renormalization schemes from given ones, then the [[main theorem of perturbative renormalization]] induces for each such scaling transformation a re-definition of interaction Lagrangian densities, this is the [[Gell-Mann-Low renormalization cocycle]] ([Gell-Mann & Low 54](#GellMannLow54), [Brunetti-Dütsch-Fredenhagen 09](#BrunettiDuetschFredenhagen09)) for review see ([Dütsch 18, section 3.5.3](#Duetsch18)).

+-- {: .num_defn #GellMannLowTransformations}
###### Definition
**([[running coupling constants]] under [[scale transformations]])**

Let

$$
  vac
    \;\coloneqq\;
  (E_{\text{BV-BRST}}, \mathbf{L}_{kin}, \Delta_H )
$$

be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] (according to [this def.](S-matrix#VacuumFree)) around which we consider [[interacting field theory|interacting]] [[perturbative QFT]].

Assume that in fact

1. the [[free field]] [[vacuum]] $vac = vac(m)$ depends on a [[mass]] parameter, and with it the choice $\mathcal{S}_{vac(m)}$ of [[renormalization scheme|normalization scheme]],

1. under [[scaling transformations]] on [[local observables]] $\sigma_\rho$ ([Dütsch 18, def. 3.19](#Duetsch18))  we have that with $\mathcal{S}_{vac(m)}$ a [[perturbative S-matrix]] scheme perturbing around $vac(m)$ also

   $$
     \sigma_\rho \circ \left(\mathcal{S}_{vac(m/\rho)}\right) \circ \sigma_\rho^{-1}
   $$

   is a perturbative S-matrix around $L_{kin}(m)$.

In this case the [[main theorem of perturbative renormalization]] (prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}) says that there exists for each scale $\rho$ a unique 
[[interaction vertex redefinition]] $\mathcal{Z}^m_\rho$ (def. \ref{InteractionVertexRedefinition}) such that

$$
  \begin{aligned}
    &
    \sigma_\rho
      \circ
    \mathcal{S}_{vac(m/\rho)}
      \circ
    \sigma_\rho^{-1}( g S_{int} + j A )
    \\
    & =
    \mathcal{S}_{vac(m)}(\mathcal{Z}^m_\rho(g S_{int} + j A))
  \end{aligned}
$$

for all [[interaction]] [[action functionals]] $g S_{int} + j A$.

These $\mathcal{Z}^m_\rho$ are the _[[Gell-Mann-Low renormalization cocycle]]_ elements. 

The [[interaction vertex redefinitions]] $\mathcal{Z}^m_\rho$ as a function of the [[rescaling]] 
is known as the _[[running coupling constants]]_.

=--

+-- {: .num_prop #CocyclePropertyOfRunningCouplingConstants}
###### Proposition
**(cocycle property of [[running coupling constants]])**

In the situation of def. \ref{GellMannLowTransformations}, the [[Gell-Mann-Low renormalization cocycles]] ([[running coupling constants]])
$\mathcal{Z}^m_\rho$ satisfy the relation

$$
  \mathcal{Z}^m_{\rho_1 \rho_2}
  \;=\;
  \mathcal{Z}^m_{\rho_1}
    \circ
  \left(
    \sigma_{\rho_1}
      \circ
    \mathcal{Z}^{m/\rho_1}_{\rho_2}
      \circ
    \sigma_{\rho_2}
  \right)
$$

Hence only for vaishing [[mass]] do these "renormalization cocycles" themselves form an actual [[renormalization group]].

=--

([Brunetti-Dütsch-Fredenhagen 09 (69)](#BrunettiDuetschFredenhagen09), [Dütsch 18 (3.325)](#Duetsch18))

+-- {: .proof}
###### Proof

From the definition we have

$$
  \begin{aligned}
    \mathcal{S}_{vac(m)}
      \circ
    \mathcal{Z}^m_{\rho_1 \rho_2}
    & =
    \sigma_{\rho_1}
      \circ
    \underset{
      \mathcal{S}_{vac(m/\rho_1)}
        \circ
      \mathcal{Z}^{m/\rho_1}_{\rho_2}
    }{
    \underbrace{
      \sigma_{\rho_2}
        \circ
      \mathcal{S}_{vac(m/\rho_1\rho_2)}
        \circ
      \sigma_{\rho_2}^{-1}
    }}
      \circ
    \sigma_{\rho_1}^{-1}
    \\
    & =
    \underset{
      =
      \mathcal{S}_{vac(m)}
        \circ
      \mathcal{Z}^m_{\rho_1}
        \circ
      \sigma_{\rho_1}
    }{
    \underbrace{
      \sigma_{\rho_1}
        \circ
      \mathcal{S}_{vac(m/\rho_1)}
        \circ
      \overset{ = id }{
        \overbrace{
          \sigma_{\rho_1}^{-1}
            \circ
          \sigma_{\rho_1}
        }
    }
    }}
      \circ
    \mathcal{Z}^{m/\rho_1}_{\rho_2}
      \circ
    \sigma_{\rho_1}^{-1}
    \\
    & =
    \mathcal{S}_{vac(m)}
      \circ
    \mathcal{Z}^m_{\rho_1}
      \circ
    \sigma_{\rho_1}
      \circ
    \mathcal{Z}^{m/\rho_1}_{\rho_2}
      \circ
    \sigma_{\rho_1}^{-1}
  \end{aligned}
$$

To conclude, it is now sufficient to see that the perturbative S-matrix $S_{vac(m)}$, as a function form [[interaction]] [[Lagrangian densities]] to [[Wick algebra]]-elements, is an [[injective function]]. (...)

=--



## References

(See also the references at _[[main theorem of perturbative renormalization]]_.)

The original article on the Stückelberg-Petermann renormalization group is

* {#StueckelbergPetermann53} [[Ernst Stückelberg]], [[André Petermann]], _La normalisation des constantes dans la theorie des quanta_, Helv. Phys. Acta 26 (1953), 499–520

The relation of the Stückelberg-Petermann renormalization group to [[scale transformations]] and the [[Gell-Mann-Low renormalization cocycle]] is due to

* {#GellMannLow54} [[Murray Gell-Mann]] and F. E. Low, _Quantum Electrodynamics at Small Distances_, Phys. Rev. 95 (5) (1954), 1300–1312 ([pdf](http://www.fafnir.phyast.pitt.edu/py3765/GellManLow.pdf))

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](https://arxiv.org/abs/0901.2038))

Review includes

* {#Duetsch18} [[Michael Dütsch]], section 3.5.1 of _[[From classical field theory to perturbative quantum field theory]]_, 2018



See also

* {#Duetschfredenhagen07} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Action Ward Identity and the Stückelberg-Petermann renormalization group_, Prog. Math. 251:113-124,2007

[[!redirects Stückelberg-Petermann renormalization groups]]

[[!redirects Stueckelberg-Petermann renormalization group]]
[[!redirects Stueckelberg-Petermann renormalization groups]]







