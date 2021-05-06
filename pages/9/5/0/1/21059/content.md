
### M2-M5 brane bound states in the BMN matrix model
 {#M2M5BraneBoundStatesInTheBMNMatrixModel}

There is the suggestion  ([MSJVR 02](BMN+matrix+model#MSJVR02), checked in [AIST 17a](BMN+matrix+models#AIST17a), [AIST 17b](BMN+matrix+models#AIST17b)) that, in the [[BMN matrix model]], [[supersymmetry|supersymmetric]] [[M2-M5-brane bound states]] are identified with [[isomorphism classes]] of certain "limit sequences" of longitudinal-[[light cone]]-[[constant function|constant]] $N \times N$-[[matrix]]-[[field (physics)|fields]] constituting [[finite-dimensional vector space|finite-dimensional]] [[complex numbers|complex]] [[Lie algebra representations]] of [[su(2)]].


#### Traditional discussion
 {#TraditionalDiscussion}

Concretely, if

$$
  \underset{ i }{\oplus}  
  \big(
    N^{(M2)}_i \cdot \mathbf{N}^{(M5)}_i
  \big)
  \;\;\in\;\;
  \mathfrak{su}(2)_{\mathbb{C}}Rep^{fin}
$$

denotes [[generalized the|the]] [[Lie algebra representation|representation]] containing 

* $N^{(M2)}_i$ [[direct sum|direct summands]]

of [[generalized the|the]]

* $N^{(M5)}_i$-[[dimension|dimensional]] [[irrep]] $\mathbf{N}^{(M5)}_i \in \mathfrak{su}(2)_{\mathbb{C}}Rep$

(for $\{N^{(M2)}_i, N^{(M5)}_i\}_{i} \in (\mathbb{N} \times \mathbb{N})^I$ some [[finite set|finitely]] [[indexed set]] of [[pairs]] of [[natural numbers]])

with total [[dimension]]

$$
  N 
    \;\coloneqq\; 
  dim
  \big( 
    \underset{ i }{\oplus}  
    \big(
      N^{(M2)}_i \cdot \mathbf{N}^{(M5)}_i
    \big)    
  \big)
$$

then:

1. a configuration of a [[finite number]] of [[coincident brane|stacks of coincident]] [[M5-branes]] corresponds to a [[sequence]] of such representations for which 
 
   1. $N^{(M2)}_i \to \infty$ (this being the relevant [[large N limit]])

   1. for fixed $N^{(M5)}_i$ (being the number of M5-branes in the $i$th stack)

   1. and fixed [[ratios]] $N^{(M2)}_i/N$ (being the [[charge]]/[[light-cone momentum]] carried by the $i$th stack);

1. an [[M2-brane]] configuration corresponds to a [[sequence]] of such representations for which 
 
   1. $N^{(M5)}_i \to \infty$ (this being the relevant [[large N limit]])

   1. for fixed $N^{(M2)}_i$ (being the number of M2-brane in the $i$th stack)

   1. and fixed [[ratios]] $N^{(M5)}_i/N$ (being the [[charge]]/[[light-cone momentum]] carried by the $i$th stack)

for all $i \in I$.

Hence, by extension, any other sequence of finite-dimensional $\mathfrak{su}(2)$-representations is a kind of mixture of these two cases, interpreted as an [[M2-M5 brane bound state]] of sorts.


#### Formalization via weight systems on chord diagrams
 {#FormalizationViaWeightSystems}

To make this precise, let 

$$
  \mathfrak{su}(2)_{\mathbb{C}} MetMod_{/\sim}
  \;\in\;
  Set
$$

be the [[set]] of [[isomorphism classes]] of [[complex numbers|complex]] [[metric Lie representations]] (hence [[finite-dimensional vector space|finite-dimensional representations]]) of [[su(2)]] ([hence](su2#Complexification) of the [[special linear Lie algebra]] $\mathfrak{sl}(2,C)$) and write 

$$
  Span
  \big(
    \mathfrak{su}(2)_{\mathbb{C}} MetMod_{/\sim}
  \big)
  \;\in\;
  Vect_{\mathbb{C}}
$$

for its [[linear span]] (the [[complex vector space]] of [[formal linear combinations]] of [[isomorphism classes]] of [[metric Lie representations]]).

Finally, write 
 
$$
  \array{
    Span
    \big(
      \mathfrak{su}(2)_{\mathbb{C}}MetMod_{/\sim}
    \big)
    &
      \longrightarrow
    &
    \big(
      \mathcal{W}^{{}^{s}}
    \big)^{deg}
    \\
    c_1 \cdot V_1
    +
    c_2 \cdot V_2
    &\mapsto&
    c_1 \cdot w_{V_1}
    +
    c_2 \cdot w_{V_2}
  }
$$

for the [[linear map]] which sends a [[formal linear combination]] or representations to the [[weight system]] on [[Sullivan chord diagrams]] with $deg \in \mathbb{N}$ chords which is given by [[trace|tracing]] in the given representation.

Then a [[M2-M5-brane bound state]] as in the traditional discussion [above](#TraditionalDiscussion), but now formalized as an [[Lie algebra weight system|su(2)-weight system]] 

$$
  \Psi_{
    \left\{
      N^{(M2)}_i, N^{(M5)}_i
    \right\}_{i}
  }
  \;\in\;
  \underset{
    deg \in \mathbb{N}
  }{\prod}
  \big(
    \mathcal{W}^{{}^{\mathrm{s}}} 
  \big)^{deg}
$$

hence a [[weight system]] [[horizontal chord diagrams]] closed to [[Sullivan chord diagrams]], these now being the [[multi-trace observables]] on these) is

\[
  \label{M2M5BraneBoundStateInWeightSystems}
  \Psi_{
    \left\{
      N^{(M2)}_i, N^{(M5)}_i
    \right\}_{i}
  }
  \;\coloneqq\;
  \tfrac{
    4 \pi \, 2^{2\,deg}
  }{
    \sum_i N^{(M2)}_i 
  }
  \underset{i}{\sum}
  \left(
    N^{(M2)}_i
    \cdot
    \tfrac{1}{
      \left(
        \sqrt{
          \left(
            N^{(M5)}_i
          \right)^2 - 1
        }
      \right)^{1 + 2 deg}
    }  
    \mathbf{N}^{(M5)}_i
  \right)
\]

<center>
<img src="https://ncatlab.org/nlab/files/M2M5BraneBoundStatesAsWeightSystemsII.jpg" width="800">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


{#M2M5BraneBoundStatesAsWeightSystemsGraphics} **Normalization and large $N$ limit.** The first power of the square root in (eq:M2M5BraneBoundStateInWeightSystems) reflects the [[volume]] measure on the [[fuzzy 2-sphere]] (by the formula [here](fuzzy+sphere#eq:FuzzyS2Integration)), while the power of $2\,deg$ (which is the number of operators in the [[multi-trace observable]] evaluating the [[weight system]]) gives the normalization ([here](fuzzy+sphere#eq:BasisFunctionsOnFuzzy2Sphere)) of the functions on the fuzzy 2-sphere.

Hence this normalization is such that the [[single-trace observables]] among the [[multi-trace observables]], hence those which come from [[round chord diagrams]], coincide on those [[M2-M5 brane bound states]] 
$
  \Psi_{
    \left\{
      N^{(M2)}_i, N^{(M5)}_i
    \right\}_{i}
  }
$
for which $N^{(M2)}_i = \delta_i^{i_0} N^{(M2)}$,
hence those which have a single constitutent [[fuzzy 2-sphere]],  with the shape observables on single fuzzy 2-spheres discussed  [here](fuzzy+sphere#ShapeObservablesAsVassilievInvariants):

<center>
<img src="https://ncatlab.org/nlab/files/SingleTraceObservableOnBMNModel.jpg" width="740">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


Therefore, with this normalization, the [[limit of a sequence|limits]] $N^{(M2)} \to \infty$ and $N^{(M5)} \to \infty$ of (eq:M2M5BraneBoundStateInWeightSystems) should exist in [[weight systems]]. The former trivially so, the latter by the usual convergence ofthe [[fuzzy 2-sphere]] to the [[round sphere|round]] [[2-sphere]] in the [[large N limit]].

Notice that the [[multi trace observables]] on these states only see the relative [[radii]] of the constitutent [[fuzzy 2-spheres]]: If $N^{(M2)}_i = \delta_i^{i_0} N^{(M2)}$ then the $N^{(M2)}$-dependence of (eq:M2M5BraneBoundStateInWeightSystems) cancels out, reflecting the fact that then there is only a single constituent 2-sphere of which the observable sees only the radius fluctuations, not the absolute radius (proportional to $N^{(M2)}$).



