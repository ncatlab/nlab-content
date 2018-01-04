

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

In [[relativistic field theory|relativistic]] [[perturbative quantum field theory]], the _time-ordered product_ is a product on [[observables]] which is such that observables which evaluate [[field histories]] not in the [[past]] of some [[event]] are ordered to the left of those which do, before taking their [[Wick algebra]] product. For example for point-evaluation [[field observables]] and distinct [[events]] $x,y \in \Sigma$ the time-ordered product is defined by

$$
  T(\mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y))
  \;\coloneqq\;
  \left\{
    \array{
      \mathbf{\Phi}^a(x) \mathbf{\Phi}^a(y) 
        &\vert& 
      x\, \text{not in the past of}\ y
      \\
      \mathbf{\Phi}^a(y) \mathbf{\Phi}^a(x) &\vert& \text{otherwise} 
    }
  \right.
$$



This may be understood as arising from the [[causal additivity]]-[[axiom]] of the [[perturbative S-matrix]]. It generalizes the 1-dimensional time-ordering (path ordering) of the [[Dyson series]] in [[quantum mechanics]].

More precisely, the time-ordere product is a  [[commutative algebra]]-[[structure]] on the [[microcausal polynomial observables]] of a [[free field theory|free]] [[Lagrangian field theory]] equipped with a [[vacuum state]] ([[Hadamard state]]) which on [[regular polynomial observables]] given on the [[regular polynomial observables]] by the [[star product]] which is induced (via [this def.](star+product#PropagatorStarProduct)) by the [[Feynman propagator]] and which is extended from there, in the sense of [[extensions of distributions]], to all [[microcausal polynomial observables]]. (This extension is the "[[renormalization]]" of the time-ordered product).

## Definition

+-- {: .num_defn #OnRegularPolynomialObservablesTimeOrderedProduct}
###### Definition
**([[time-ordered product]] on [[regular polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] 
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the _[[time-ordered product]]_ on the space of [[on-shell]] [[regular polynomial observable]] $PolyObs(E,\mathbf{L})_{reg}$ is the [[star product]] induced by the [[Feynman propagator]] (via [this prop.](star+product#PropagatorStarProduct)):

$$
  \array{
    PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
    \otimes
    PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
      &\overset{T((-)(-))}{\longrightarrow}&
    PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
    \\
    (A_1, A_2)
    &\mapsto&
    \phantom{\coloneqq} A_1 \star_F A_2
  }
$$

hence

$$
  T(A_1 A_2)
  \coloneqq
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

=--

+-- {: .num_prop #CausalOrderingTimeOrderedProductOnRegular}
###### Proposition
**([[time-ordered product]] is indeed causally ordered [[Wick algebra]] product)**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] 
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the [[time-ordered product]] on [[regular polynomial observables]] (def. \ref{OnRegularPolynomialObservablesTimeOrderedProduct}) is indeed a time-ordering of the [[Wick algebra]] product $\star_H$ in that for all [[pairs]] of [[regular polynomial observables]]

$$
  A_1, A_2 \in PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
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

The [[advanced and retarded propagators]] $\Delta_{pm}$ by definition are [[support|supported]] in the [[future cone]]/[[past cone]], respectively

$$
  supp(\Delta_{\pm}) \subset \overline{V}^{\pm}
$$

and since they turn into each other under exchange of their arguments ([this cor.](causal+propagator#CausalPropagatorIsSkewSymmetric)):

$$
  \Delta_\pm(y,x) = \Delta_{\mp}(x,y)
  \,.
$$

Using this we compute as follows:

$$
  \begin{aligned}
    A_1 \underset{\Delta_{F}}{\star} A_2
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
        A_1 \underset{\tfrac{i}{2}\Delta_+ + H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!wedge} supp(A_2)
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

## Related concepts

[[!include products in pQFT -- table]]

$\,$

[[!include Wick algebra -- table]]


## References

See the references at _[[S-matrix]]_

[[!redirects time-ordered products]]

[[!redirects time ordered product]]
[[!redirects time ordered products]]
