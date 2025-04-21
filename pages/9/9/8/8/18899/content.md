

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

In [[relativistic field theory|relativistic]] [[perturbative quantum field theory]], the _time-ordered product_ is a product on suitably well-behave [[observables]]  which re-orders its arguments according to the [[causal ordering]] of their spacetime supports befor multiplying with the [[Wick algebra]] product. 

(Analogously reverse [[causal ordering]] this is called the _reverse-time ordered_ or _anti-time ordered_ prouct.)

For example for point-evaluation [[field observables]] and distinct [[events]] $x,y \in \Sigma$ the time-ordered product is defined by

$$
  T(\mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y))
  \;\coloneqq\;
  \left\{
    \array{
      \mathbf{\Phi}^a(x) \mathbf{\Phi}^a(y) 
        &\vert& 
      x \, \text{not in the past of}\, y
      \\
      \mathbf{\Phi}^a(y) 
      \mathbf{\Phi}^a(x) 
      &\vert& 
      \text{otherwise} 
    }
  \right.
$$



This may be understood as arising from the [[causal additivity]]-[[axiom]] of the [[perturbative S-matrix]]. It generalizes the 1-dimensional time-ordering (path ordering) of the [[Dyson series]] in [[quantum mechanics]].

More precisely, the time-ordered product is a  [[commutative algebra]]-[[structure]] on the [[microcausal polynomial observables]] of a [[free field theory|free]] [[Lagrangian field theory]] equipped with a [[vacuum state]] ([[Hadamard state]]) which on [[regular polynomial observables]] given on the [[regular polynomial observables]] by the [[star product]] which is induced (via [this def.](star+product#PropagatorStarProduct)) by the [[Feynman propagator]] and which is extended from there, in the sense of [[extensions of distributions]], to all [[microcausal polynomial observables]]. (This extension is the "[[renormalization]]" of the time-ordered product).

## Definition
 {#Definition}

### On regular polynomial observables
 {#OnRegularPolynomialObservables}


+-- {: .num_defn #OnRegularPolynomialObservablesTimeOrderedProduct}
###### Definition
**([[time-ordered product]] on [[regular polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]]
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the _[[time-ordered product]]_ on the space of [[off-shell]] [[regular polynomial observable]] $PolyObs(E)_{reg}$ is the [[star product]] induced by the [[Feynman propagator]] (via [this prop.](star+product#PropagatorStarProduct)):

$$
  \array{
    PolyObs(E)_{reg}[ [\hbar] ]
    \otimes
    PolyObs(E)_{reg}[ [\hbar] ]
      &\overset{}{\longrightarrow}&
    PolyObs(E)_{reg}[ [\hbar] ]
    \\
    (A_1, A_2)
    &\mapsto&
    \phantom{\coloneqq} A_1 \star_F A_2
  }
$$

hence

$$
  A_1 \star_F A_2
  \;
  \coloneqq
  \;
  ((-)\cdot(-))
  \circ
  \exp\left(
    \underset{\Sigma \times \Sigma}{\int}
    \Delta_F^{a b}(x,y)
    \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
    \otimes
    \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
    \,
    dvol_\Sigma(x)
    \,
    dvol_\Sigma(y)
  \right)
$$

(Notice that this does not descend to the [[on-shell]] observables, since the [[Feynman propagator]] is not a solution to the _homogeneous_ [[equations of motion]].)

=--

+-- {: .num_prop #CausalOrderingTimeOrderedProductOnRegular}
###### Proposition
**([[time-ordered product]] is indeed causally ordered [[Wick algebra]] product)**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] 
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the [[time-ordered product]] on [[regular polynomial observables]] (def. \ref{OnRegularPolynomialObservablesTimeOrderedProduct}) is indeed a time-ordering of the [[Wick algebra]] product $\star_H$ in that for all [[pairs]] of [[regular polynomial observables]]

$$
  A_1, A_2 \in PolyObs(E)_{reg}[ [\hbar] ]
$$

with [[disjoint subset|disjoint]] [[spacetime]] [[support]] we have

$$  
  T(A_1 A_2)
  \;=\;
  \left\{
    \array{
      A_1 \star_H A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
      \\
      A_2 \star_H A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)
    }
  \right.
  \,.
$$

Here $S_1 {\vee\!\!\!\wedge} S_2$ is the [[causal order]] relation ("$S_1$ does not intersect the [[past cone]] of $S_2$"). Beware that for general [[pairs]] $(S_1, S-2)$ of subsets neither $S_1 {\vee\!\!\!\wedge} S_2$ nor $S_2 {\vee\!\!\!\wedge} S_1$.

=--


+-- {: .proof}
###### Proof

Recall the following facts:

1. the [[advanced and retarded propagators]] $\Delta_{\pm}$ by definition are [[support|supported]] in the [[future cone]]/[[past cone]], respectively

   $$
     supp(\Delta_{\pm}) \subset \overline{V}^{\pm}
   $$

1. they turn into each other under exchange of their arguments ([this cor.](causal+propagator#CausalPropagatorIsSkewSymmetric)):

   $$
     \Delta_\pm(y,x) = \Delta_{\mp}(x,y)
     \,.
   $$

1. the real part $H$ of the [[Feynman propagator]], which by definition is the real part of the [[Wightman propagator]] is symmetric (by definition or else by [this prop.](Hadamard+distribution#SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime)):

   $$
     H(x,y) = H(y,x)
   $$

Using this we compute as follows:

$$
  \begin{aligned}
    A_1 \underset{\Delta_{F}}{\star} A_2
    \;
    & =
    A_1 \underset{\tfrac{i}{2}(\Delta_+ + \Delta_-) + H}{\star} A_2
    \\
    & =
    \left\{
      \array{
        A_1 \underset{\tfrac{i}{2}\Delta_+ + H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_1 \underset{\tfrac{i}{2}\Delta_- + H}{\star} A_2 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
    \\
    & = 
    \left\{
      \array{
        A_1 \underset{\tfrac{i}{2}\Delta_+ + H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_2 \underset{\tfrac{i}{2}\Delta_+ + H}{\star} A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
    \\
    & =
    \left\{
      \array{
        A_1 \underset{\tfrac{i}{2}(\Delta_+ - \Delta_-) + H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_2 \underset{\tfrac{i}{2}(\Delta_+ - \Delta_-) + H}{\star} A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
    \\
    & =
    \left\{
      \array{
        A_1 \underset{\Delta_H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_2 \underset{\Delta_H}{\star} A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
  \end{aligned}
$$


=--

+-- {: .num_prop #IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise}
###### Proposition
**([[time-ordered product]] on [[regular polynomial observables]] [[isomorphism|isomorphic]] to pointwise product)

The [[time-ordered product]] on [[regular polynomial observables]] (def. \ref{CausalOrderingTimeOrderedProductOnRegular}) is [[isomorphism|isomorphism]] to the pointwise product of [[observables]] ([this def.](A+first+idea+of+quantum+field+theory#Observable)) via the [[linear isomorphism]]

$$
  \mathcal{T}
  \;\colon\;
  PolyObs(E)_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E)_{reg}[ [\hbar] ]
$$

given by

$$
  \mathcal{T}A
  \;\coloneqq\;
  \exp\left(
    \tfrac{1}{2}
    \hbar 
    \underset{\Sigma}{\int} 
     \Delta_F(x,y)^{a b} 
     \frac{\delta^2}{\delta \mathbf{\Phi}^a(x) \delta \mathbf{\Phi}^b(y)}
  \right)
  A
$$

in that 

$$
  \begin{aligned}
    T(A_1 A_2)
    & \coloneqq
    A_1 \star_{F} A_2
    \\
    & =
    \mathcal{T}( \mathcal{T}^{-1}(A_1) \cdot \mathcal{T}^{-1}(A_2) )
  \end{aligned}
$$

hence

$$
  \array{
    PolyObs(E)_{reg}[ [\hbar] ]
      \otimes
    PolyObs(E)_{reg}[ [\hbar] ]
      &\overset{(-)\cdot (-)}{\longrightarrow}&   
    PolyObs(E)_{reg}[ [\hbar] ]
    \\
    {}^{\mathllap{\mathcal{T} \otimes \mathcal{T}}}_\simeq\Big\downarrow 
      && 
    \downarrow^{\mathrlap{\mathcal{T}}}_\simeq
    \\
    PolyObs(E)_{reg}[ [\hbar] ]
      \otimes
    PolyObs(E)_{reg}[ [\hbar] ]
      &\overset{(-) \star_F (-)}{\longrightarrow}&   
    PolyObs(E)_{reg}[ [\hbar] ]
  }
$$

=--

([Brunetti-Dütsch-Fredenhagen 09, (12)-(13)](#BrunettiDuetschFredenhagen09), [Fredenhagen-Rejzner 11b, (14)](#FredenhagenRejzner11b))

+-- {: .proof}
###### Proof

Since the [[Feynman propagator]] is symmetric ([this prop.](A+first+idea+of+quantum+field+theory#SymmetricFeynmanPropagator)), the statement is a special case of [this prop.](star+product#SymmetricContribution)).

=--


+-- {: .num_example #RegularObservablesExponentialTimeOrdered}
###### Example
**([[time-ordered product|time-ordered]] [[exponential]] of [[regular polynomial observables]])**

Let 

$$
  V \in PolyObs_{reg, deg = 0}[ [ \hbar ] ]
$$

be a [[regular polynomial observables]] of degree zero, and write 

$$
  \exp(V)
  =
  1 + V + \tfrac{1}{2!} V \cdot V + \tfrac{1}{3!} V \cdot V \cdot V + \cdots
$$

for the [[exponential]] of $V$ with respect to the pointwise product.

Then the [[exponential]] $\exp_{\mathcal{T}}(V)$ of $V$ with respect to the [[time-ordered product]] $\star_F$ (def. \ref{OnRegularPolynomialObservablesTimeOrderedProduct}) is equal to the [[conjugation]] of the exponential with respect to the
pointwise product by the time-ordering isomorphism $\mathcal{T}$ from prop. \ref{IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise}:

$$
  \begin{aligned}
    \exp_{\mathcal{T}}(V)
    &
    \coloneqq
    1 + V + \tfrac{1}{2} V \star_F V + \tfrac{1}{3!} V \star_F V \star_F V + \cdots
    \\
    & = 
    \mathcal{T} \circ \exp(-) \circ \mathcal{T}^{-1}(V)
  \end{aligned}
$$

=--


### On local observables
 {#OnLocalObservables}

The time-ordered product on regular polynomial observables from prop. \ref{OnRegularPolynomialObservablesTimeOrderedProduct} extends to a product on [[polynomial observable|polynomial]] [[local observables]], then taking values in [[microcausal observables]]:

$$
  T
  \;\colon\;
  PolyLocObs(E)^{\otimes_n}[ [\hbar] ]
    \longrightarrow
  PolyObs(E)_{mc}[ [\hbar] ]
  \,.
$$

This extension is not unique. A choice of such an extension, satisfying some evident compatibility conditions, is a choice of _[[renormalization scheme]]_ for the given [[perturbative quantum field theory]]. Every such choice corresponds to a choice of [[perturbative S-matrix]] for the theory. This construction is called _[[causal perturbation theory]]_.

## Properties

### Relation to path integral

\begin{remark}\label{OperatorOrderAndTimeOrder}
**(operator product order and time-order)**
\linebreak
  Under the [[path integral]], the order of the product of [[linear operators]] (such as $x \cdot \frac{d}{d x}$ as opposed to $\frac{d}{d x} x \xdot$) corresponds to *temporal ordering* of their [[observable]] values ([Feynman 1948, p. 381](path+integral#Feynman48),  reviewed in [Nagaosa 1999, pp. 33](path+integral#Nagaosa99); [Ong](path+integral#Ong)).

Conversely the product of [[observable]] values in the path integral corresponds to the time-ordered product of the corresponding [[linear operators]] (eg. [Polchinski 1998 (A.1.17)](path+integral#Polchinski98); [Rischke 2021 (5.63)](path+integral#Rischke21)).
\end{remark}


## Related concepts

[[!include products in pQFT -- table]]

$\,$

[[!include Wick algebra -- table]]


## References

See also the references at _[[S-matrix]]_

The equivalence of the time-ordered product on regular observables to the point-wise product was maybe first highlighted in

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], p. 6 of _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))

and then further amplified in 

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], p. 6 of _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))


[[!redirects time-ordered products]]

[[!redirects time ordered product]]
[[!redirects time ordered products]]

[[!redirects reverse-time ordered product]]
[[!redirects reverse-time ordered products]]

[[!redirects anti-time ordered product]]
[[!redirects anti-time ordered products]]

