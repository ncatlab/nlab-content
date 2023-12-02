

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

What are called _Weyl relations_ is the incarnation of [[canonical commutation relations]] under passing to [[exponentials]], constituting the *[[Weyl algebra]]*. 

For example if $a, a^\ast$ are two elements of an [[associative algebra]] with [[commutator]]

$$
  [a,a^\ast] = \hbar
$$

then the corresponding Weyl relation is, by the [[Baker-Campbell-Hausdorff formula]],

$$
  e^{z a}
  e^{z^\ast a^\ast} 
  \;=\;  
  e^{z^\ast a^\ast} 
  e^{z a} 
  e^{\hbar z z^\ast} 
$$

for $z,z^\ast \in \mathbb{C}$.

## In the Wick algebra of free quantum fields

+-- {: .num_prop #MoyalStarProductOnMicrocausal}
###### Proposition
**([[Hadamard distribution|Hadamard]]-[[Moyal star product]] on [[microcausal observables]] -- [[abstract Wick algebra]])**

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] $P \Phi = 0$. Write $\Delta$ for the [[causal propagator]] and let 

$$
  \Delta_H
  \;=\;
  \tfrac{i}{2}\Delta + H
$$ 

be a corresponding [[Wightman propagator]] ([[Hadamard 2-point function]]).

Then the [[star product]] induced by $\Delta_H$

$$
  A \star_H A
  \;\coloneqq\;
  prod
   \circ
  \exp\left(
    \int_{X^2} \hbar \Delta_H^{a b}(x_1, x_2) \frac{\delta}{\delta \Phi^a(x_1)}
    \otimes \frac{\delta}{\delta \Phi^b(x_2)} dvol_g
  \right)
  (P_1 \otimes P_2)
$$

on [[off-shell]] [[microcausal observables]] $A_1, A_2 \in \mathcal{F}_{mc}$ is well defined in that the [[wave front sets]] involved in the [[products of distributions]] that appear in expanding out the [[exponential]] satisfy [[Hörmander's criterion]].

Hence by the general properties of [[star products]] ([this prop.](star+product#AssociativeAndUnitalStarProduct)) this yields a [[unital algebra|unital]] [[associative algebra]] [[structure]] on the space of [[formal power series]] in $\hbar$ of [[off-shell]] [[microcausal observables]]

$$
  \left(
    PolyObs(E)_{mc}[ [\hbar] ] \,,\, \star_H
  \right)
  \,.
$$ 

This is the _[[off-shell]] [[Wick algebra]]_ corresponding to the choice of [[Wightman propagator]] $H$.

Moreover the image of $P$ is an ideal with respect to this algebra structure, so that it descends to the [[on-shell]] [[microcausal observables]] to yield the _[[on-shell]] [[Wick algebra]]_

$$
  \left(
    PolyObs(E,\mathbf{L})_{mc}[ [ \hbar ] ] \,,\, \star_H
  \right)
  \,.
$$ 

Finally, under [[complex conjugation]] $(-)^\ast$ these are [[star algebras]] in that 

$$
  \left(
    A_1 \star_H A_2
  \right)^\ast
  =
  A_2^\ast \star_H A_1^\ast
  \,.
$$

=--

For **proof** see at _[[Wick algebra]]_ [this prop.](Wick+algebra#MoyalStarProductOnMicrocausal).

+-- {: .num_remark #WickAlgebraIsFormalDeformationQuantization}
###### Remark
**([[Wick algebra]] is [[formal deformation quantization]] of [[Poisson-Peierls bracket|Poisson-Peierls algebra of observables]])**


Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] $P \Phi = 0$ with [[causal propagator]] $\Delta$ and let $\Delta_H \;=\; \tfrac{i}{2}\Delta + H$  be a corresponding [[Wightman propagator]] ([[Hadamard 2-point function]]).


Then the [[Wick algebra]]  $\left( PolyObs(E,\mathbf{L})_{mc}[ [\hbar] ] \,,\, \star_H \right)$ from prop. \ref{MoyalStarProductOnMicrocausal} is a [[formal deformation quantization]] of the [[Poisson algebra]] on the [[covariant phase space]] given by the [[on-shell]] [[polynomial observables]] equipped with the [[Poisson-Peierls bracket]] $\{-,-\} \;\colon\; PolyObs(E,\mathbf{L})_{mc} \otimes PolyObs(E,\mathbf{L})_{mc}  \to PolyObs(E,\mathbf{L})_{mc}$ in that for all $A_1, A_2 \in PolyObs(E,\mathbf{L})_{mc}$ we have

$$
  A_1 \star_H A_2
  \;=\;
  A_1 \cdot A_2
  \;mod\;
  \hbar
$$

and

$$
  A_1 \star_H A_2
  -
  A_2 \star_H A_1
  \;=\;
  i \hbar \{A_1, A_2\}
  \;mod\;
  \hbar^2
  \,.
$$

=--

([Dito 90](#Dito90), [Dütsch-Fredenhagen 01](Wick+algebra#DutschFredenhagen01))

+-- {: .proof}
###### Proof

By prop. \ref{MoyalStarProductOnMicrocausal} this is immediate from the general properties of the [[star product]] ([this example](A+first+idea+of+quantum+field+theory+--+Quantization#MoyalStarProductIsFormalDeformationQuantization)). 

Explicitly, consider, without restriction of generality, $A_1 = \int (\alpha_1)_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)$ and $A_2 = \int (\alpha_2)_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)$ be two linear observables. Then

$$
  \begin{aligned}
    A_1 \star_H A_2
    & =
    A_1 A_2 
    +
    \hbar 
    \int 
    \left( 
      \tfrac{i}{2} \Delta^{a_1 a_2}(x_1, x_2) + H^{a_1 a_2}(x_1,x_2)  
     \right) 
      \frac{\partial A_1}{\partial \mathbf{\Phi}^{a_1}(x_1)}
      \frac{\partial A_2}{\partial \mathbf{\Phi}^{a_2}(x_2)}
    \;mod\;
    \hbar^2  
   \\
   & = 
   A_1 A_2 
   + 
   \hbar 
   \left(
    \int 
      (\alpha_1)_{a_1}(x_1)
      \left(
       \tfrac{i}{2}\Delta^{a_1 a_2}(x_1, x_2)
       + H^{a_1 a_2}(x_1, x_2)
      \right)
      (\alpha_2)_{a_2}(x_2)
   \right)
   \;mod\;
   \hbar^2
  \end{aligned}
$$

Now since $\Delta$ is skew-symmetric while $H$ is symmetric is follows that

$$
  \begin{aligned}
    A_1 \star_H A_2
    - 
    A_2 \star_H A_1
    & =
    i \hbar 
    \left(
     \int 
       (\alpha_1)_{a_1}(x_1)
       \Delta^{a_1 a_2}(x_1, x_2)
       (\alpha_2)_{a_2}(x_2)
    \right)
    \;mod\;
    \hbar^2
    \\
    & =
    i \hbar \, \left\{ A_1, A_2\right\}
  \end{aligned}
  \,.
$$

The right hand side is the [[integral kernel]]-expression for the [[Poisson-Peierls bracket]], as shown in the second line.


=--



+-- {: .num_example}
###### Example
**([[Hadamard vacuum state]] [[2-point function]])**

Let 

$$
  A_i \in LinObs(E,\mathbf{L})_{mc} \hookrightarrow PolyObs(E,\mathbf{L})_{mc}
$$

for $i \in \{1,2\}$ be two [[linear observable|linear]] [[microcausal observables]] represented by [[distributions]] which in [[generalized function]]-notation are given by

$$
  A_i
  \;=\;
  \int (\alpha_i)_{a_i}(x_i) \mathbf{\Phi}^{a_i}(x_i) \, dvol_\Sigma(x_i)
  \,.
$$

Then their Hadamard-Moyal [[star product]] (prop. \ref{MoyalStarProductOnMicrocausal}) is the [[sum]] of their pointwise product with $\tfrac{1}{2} i \hbar$ times the evaluation 

$$
  \begin{aligned}
    \langle A_1 A_2\rangle
    & \coloneqq
    \int \int
      (\alpha_1)_{a_1}(x_1) 
      \,
      \left\langle \mathbf{\Phi}^{a_1}(x_1) \mathbf{\Phi}^{a_2}(x_2)\right\rangle
     \,  
     (\alpha_2)_{a_2}(x_2)
     \, dvol_\Sigma(x_1)
     \, dvol_\Sigma(x_2)
    \\
    & \coloneqq
      \tfrac{1}{2} 
     i \hbar \int \int 
     (\alpha_1)_{a_1}(x_1) \Delta_H^{a_1 a_2}(x_1,x_2) (\alpha_2)_{a_2}(x_2)
      \,dvol_\Sigma(x_1)
      \,dvol_\Sigma(x_2)
  \end{aligned}
$$

of the [[Wightman propagator]] $\Delta_H$:

$$
  \label{StarProductOfTwoLinearObservables}
  A_1 \star_H A_2
  =
  A_1 \cdot A_2
  +
  \langle A_1 A_2\rangle
$$

Further [below](#HadamardVacuumStatesOnWickAlgebras) we see that this evaluation is the [[2-point function]] of a [[state on a star-algebra|state]] on the [[Wick algebra]].

=--


+-- {: .num_example #WeylRelations}
###### Example
**([[Weyl relations]])**

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] and with [[Wightman propagator]] $\Delta_H$.

Then for 

$$
  A_1, A_2 
  \;\in\;
  LinObs(E,\mathbf{L})_{mc}
  \hookrightarrow
  PolyObs(E,\mathbf{L})_{mc}
$$

two [[linear observables|linear]] [[microcausal observables]], the Hadamard-Moyal star product (def. \ref{MoyalStarProductOnMicrocausal}) of their [[exponentials]] exhibits the [[Weyl relations]]:

$$
  e^{A_1}
  \star_H
  e^{A_2}
  \;=\;
  e^{A_1 + A_2} \; e^{\langle A_1 A_2\rangle}
$$

where on the right we have the [[exponential]] [[Wightman 2-point function]] (eq:StarProductOfTwoLinearObservables).

=--

(e.g. [Dütsch 18, exercise 2.3](#Duetsch18))

## Related concepts

* [[Weyl algebra]]

* [[canonical commutation relations]]

* [[Heisenberg algebra]]

## References

> For more references see at *[[Weyl algebra]]*.

* {#Duetsch18} [[Michael Dütsch]], exercise 2.3 in: _[[From classical field theory to perturbative quantum field theory]]_, 2018



[[!redirects Weyl relations]]
