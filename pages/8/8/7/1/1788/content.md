
+-- {: .num_example #FeynmanPerturbationSeries}
###### Example
**([[Feynman perturbation series]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, and let

$$
  g S_{int} + j A 
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, h ] ]
$$

be a [[local observable]].

By prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} every choice of perturbative [[S-matrix]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) 

$$
  \mathcal{S}(g S_{int} + j A)
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{mc}((\hbar))[ [ g, j ] ] + 
$$

has an expansion as a [[formal power series]] of the form

$$
  \mathcal{S}(g S_{int} + j A)
  \;=\;
  \underset{\Gamma \in \mathcal{G}}{\sum}
  \Gamma_{norm}(g S_{int} + j A)
  \,,
$$

where the series is over all [[Feynman diagrams]] $\Gamma$ all whose vertices are labeled by $g S_{int} + jA $ (def. \ref{FeynmanDiagram}), and the summands are the corresponding [[renormalization|("re"-)normalized]] (def. \ref{ExtensionOfTimeOrderedProoductsRenormalization}) [[Feynman amplitudes]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}).

Expressed in this form the S-matrix is known as the _[[Feynman perturbation series]]_.

=--

+-- {: .num_defn #InPerturbationTheoryActionEffective}
###### Definition
**([[effective action]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be an [[S-matrix]] scheme for [[perturbative QFT]] around this vacuum (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) and let

$$
  g S_{int} + j A 
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, h ] ]
$$

be a [[local observable]]. 

Recall that for each [[Feynman diagram]] $\Gamma$ with all vertices labeled by $g S_{int} + j A$ (def. \ref{FeynmanDiagram}) the [[Feynman perturbation series]] for $\mathcal{S}(g S_{int} + j A)$ (example \ref{FeynmanPerturbationSeries}) 

$$
  \mathcal{S}(g S_{int} + j A)
  \;=\;
  \underset{\Gamma \in \mathcal{G}}{\sum}
    \Gamma(g S_{int} + j A)
$$

contributes with a [[renormalization|("re"-)nromalized]] [[Feynman amplitude]] $\Gamma(g S_{int} + j A) \in PolyObs(E_{\text{BV-BRST}})((\hbar))[ [ g, j ] ]$.

We say that the corresponding _[[effective action]]_ is $i \hbar$ times the [[vacuum expectation value]] of the sub-series

$$
  S_{eff}
  \;\coloneqq\;
  i \hbar
  \underset{\Gamma \in \mathcal{G}_{conn}}{\sum}
  \Gamma(g S_{int} + j A)
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})((\hbar))[ [ g, j ] ]
$$

of [[Feynman amplitudes]] that are labeled only by the _[[connected graph|connected]]_ [[Feynman diagrams]] $\Gamma \in \mathcal{G}_{conn} \subset \mathcal{G}$.

=--

The terminology "effective action" is due to the following fact:

+-- {: .num_prop}
###### Proposition
**([[effective action]] is [[logarithm]] of [[S-matrix]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be an [[S-matrix]] scheme for [[perturbative QFT]] around this vacuum (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) and let

$$
  g S_{int} + j A 
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, h ] ]
$$

be a [[local observable]] and let

$$
  S_{eff} \;\in\; PolyObs(E_{\text{BV-BRST}})((\hbar))[ [ g, j] ]
$$

be the corresponding [[effective action]] (def. \ref{InPerturbationTheoryActionEffective}).

Then then [[S-matrix]] for $g S_{int} + j A$ is the [[exponential]] of the [[effective action]] with respect to the pointwise product $(-)\cdot (-)$ of observables ([this def.](A+first+idea+of+quantum+field+theory#Observable)): 

$$
  \begin{aligned}
    \mathcal{S}(g S_{int} + j A)
    & =
    \exp_\cdot\left( \tfrac{1}{i \hbar} S_{eff}  \right)
    \\
    & \coloneqq
    1 
      + 
    \frac{1}{i \hbar} S_{eff} 
      + 
    \frac{1}{(i \hbar)^2} S_{eff} \cdot S_{eff}
      +
    \frac{1}{(i \hbar)^3} S_{eff} \cdot S_{eff} \cdot S_{eff}
      +
    \cdots
  \end{aligned}
$$

Moreover, this relation passes to the [[vacuum expectation values]]:

$$
  \left\langle 
    \mathcal{S}(g S_{int} + j A)
  \right\rangle
  \;=\;
  e^{\tfrac{1}{i \hbar} \langle S_{eff}\rangle}
  \,.
$$

Conversely the [[vacuum expectation value]] of the [[effective action]] is to the [[logarithm]] of that of the S-matrix:

$$
  \left\langle 
    S_{eff}
  \right\rangle
  \;=\;
  i \hbar 
  \, 
  \ln 
  \left\langle  
    \mathcal{S}(g S_{int} + j A) 
  \right\rangle
  \,.
$$

=--


+-- {: .proof}
###### Proof

By prop. \ref{TimeOrderedProductAwayFromDiagonal} the contributions to the S-matrix away from coinciding interaction points are given by the [[star product]] iinduced by the [[Feynman propagator]], and specifically, by prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}, the [[Feynman amplitudes]] are given this way. Now by definition of the star product ([this def.](star+product#PropagatorStarProduct)) it is given by first contracting with powers of the [[Feynman propagator]] and then multiplying all resulting terms with the pointwise product of observables. From this and the nature of the combinatorial factor in the definition of the [[Feynman amplitudes]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) it is clear that for 

$$
  \Gamma = \Gamma_1 \sqcup \Gamma_2 \sqcup \cdots \sqcup \Gamma_n
  \;\in\; \mathcal{G}
$$

a [[disjoint union]] of Feynman diagrams, then then corresponding [[Feynman amplitudes]] multiply by the pointwise product

$$
  \Gamma(g S_{int} + j A)
  \;=\;
  \Gamma_1(g S_{int} + j A)
   \cdot
  \Gamma_2(g S_{int} + j A)
    \cdot
    \cdots
    \cdot
  \Gamma_n(g S_{int} + j A)
  \,.
$$

This implies that the summands in the $n$th powers of $\frac{1}{i \hbar}$ times the effective action are precisely the Feynman amplitudes of Feynman diagrams with $n$ [[connected components]], where each such appears with multiplicity given by the [[factorial]] of $n$:

$$
  \frac{1}{n!}
  \left(
    \frac{1}{i \hbar}
    S_{eff}
  \right)^n
  \;=\;
  \Gamma(g S_{int} + j A)
  \underset{
     { \Gamma = \underoverset{j = 1}{n}{\sqcup} \Gamma_j }
     \atop
     { \Gamma_j \in \mathcal{G}_{conn} }
  }{\sum}
  \,.
$$

It follows that

$$
  \begin{aligned}
    \exp_\cdot\left( 
      \frac{1}{i \hbar} S_{int}
    \right)
    & =
    \underset{n \in \mathbb{N}}{\sum}
    \underset{
       { \Gamma = \underoverset{j = 1}{n}{\sqcup} \Gamma_j }
       \atop
       { \Gamma_j \in \mathcal{G}_{conn} }
    }{\sum}
    \Gamma(g S_{int} + j A)
    \\
    & =
    \underset{\Gamma \in \mathcal{G}}{\sum}
    \Gamma(g S_{int} + j A)
  \end{aligned}
$$

yields the [[Feynman perturbation series]] by expressing it as a series organized by number of [[connected components]].

To conclude the proof it is now sufficient to observe that taking [[vacuum expectation values]] of [[polynomial observables]] respects the pointwise product of observables 

$$
  \left\langle A_1 \cdot _2\right\rangle
  \;=\;
  \left\langle 
    A_1
  \right\rangle
  \,
  \left\langle
    A_2
  \right\rangle
$$

(since the [[Hadamard vacuum state]] $\langle -\rangle \colon PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]  \to \mathbb{C}[ [\hbar, g, j ] ]$ simply picks the zero-order monomial term, by [this prop.](Wick+algebra#WickAlgebraCanonicalState)).


=--



+-- {: .num_prop #FeynmanDiagramLoopOrder}
###### Proposition
**([[loop order]] of [[Feynman diagrams]])**

Let $\Gamma$ be a [[Feynman diagram]] (def. \ref{FeynmanDiagram}) whose underlying [[graph]] is [[planar]]. Then the order of $\hbar$ at which its [[Feynman amplitude]] (def. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) contributes in the [[S-matrix]] (def. \ref{LagrangianFieldTheoryPerturbativeScattering}) is

$$
  \hbar^{L(\Gamma) - 1}
  \,,
$$

where $L(\Gamma) \in \mathbb{N}$ is the number of _[[faces]]_ of the [[planar graph]] $\Gamma$, here called the _loop number_ of the diagram.

Accordingly, the order in $\hbar$ at which the [[Feynman amplitude]] of a ([[planar graph|planar]]) [[Feynman diagram]] contributes is often referred to as the _loop order_.

The contributions at loop order $L(\Gamma) = 0$ are often called the _[[tree level]]_ contributions.

=--

+-- {: .proof}
###### Proof


By def. \ref{LagrangianFieldTheoryPerturbativeScattering} the explicit $\hbar$-dependence of the [[S-matrix]] is

$$
  \mathcal{S}
  \left(
    S_{int}
  \right)
  \;=\; 
  \underset{k \in \mathbb{N}}{\sum} 
    \frac{1}{k!}
    \frac{1}{(i \hbar)^k}
    T( \underset{k \, \text{factors}}{\underbrace{S_{int}, \cdots,  S_{int}}} )
$$

and by prop. \ref{TimeOrderedProductAwayFromDiagonal} the further $\hbar$-dependence of the [[time-ordered product]] $T(\cdots)$ is

$$
  T(S_{int}, S_{int}) 
  \;=\; 
  prod \circ 
  \exp\left(
    \hbar
    \left\langle 
      \Delta_F, 
      \frac{\delta}{\delta \mathbf{\Phi}} 
        \otimes
      \frac{\delta}{\delta \mathbf{\Phi}}
    \right\rangle
  \right)
 ( S_{int} \otimes S_{int} )
  \,,
$$

By the [[Feynman rules]] (prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints}) this means that 

1. each [[vertex]] of the Feynman diagram contributes a power $\hbar^{-1}$;

1. each [[edge]] of the Feynman diagram contributes a power $\hbar^1$.

If we write

$$
  E(\Gamma), V(\Gamma) \;\in\; \mathcal{N}
$$

for the total number of [[vertices]] and [[edges]], respectively, in $\Gamma$, this means that $\Gamma$ contributes at the power

$$
  \hbar^{E(\Gamma) - V(\Gamma)}
  \,.
$$

So far this holds for arbitrary $\Gamma$. Now using the assumption that 

=--

+-- {: .num_defn #FeynmanAmplitudes}
###### Definition
**([[Feynman amplitude]])**

Let 

$$
  \mathbf{L}_{int} ,
  \;\in\;  
  \in \Omega^{p+1,0}_\Sigma(E_{\text{BV-BRST}})[ [ \hbar ] ]
$$

be a [[local Lagrangian density]].

For

$$
  g_{sw} \in C^\infty_{cp}(\Sigma)\langle g \rangle
$$ 

an [[adiabatic switching|adiabatically switched]] [[coupling constant]], we write

$$
  \tau_\Sigma\left( g_{sw} \mathbf{L}_{int}\right)
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]
$$

for the corresponding [[local observable]], given by [[transgression of variational differential forms|transgression]]. Similarly for 

$$
  j_{a} \in C^\infty_{cp}(\Sigma)\langle j \rangle
$$ 

[[adiabatic switching|adiabatically switched]] [[source field]] strngths, write

$$
  \tau_{\Sigma} 
  \left(
    j_{a} \phi^a
  \right)
  \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, j ] ]
$$

for the corresponding local observable.


Then the [[vacuum expectation values]] of the summands $\Gamma$ in prop. \ref{FeynmanPerturbationSeriesAwayFromCoincidingPoints} define [[distributions of several variables]]

$$
  \Gamma_{ \mathbf{L}_{int} }
  \;\in\;
  \mathcal{D}'\left(
    \Sigma^{{\vert \Gamma_{v_{int}, v_{ext}} \vert}}
    \setminus
    \left\{ (x_i)\,\vert\, x_i\neq x_j \, \text{for} \, j \neq j \right\}
  \right)[ [ \hbar, g, j] ]
$$

on the [[complement]] of the locus of coinciding vertex points, given by

$$  
  \Gamma_{\mathbf{L}_{int}  }
  \;\colon\;
  (g_{sw,1}, \cdots, g_{sw,v_{int}}, j_{sw,a_1}, \cdots, j_{a_{v_{ext}}})
  \;\mapsto\;
  \left\langle
    \Gamma\left(
      \tau_\Sigma(g_{sw,1}\mathbf{L}_{int}),
      \cdots,
      \tau_\Sigma(g_{sw,v_{int}}\mathbf{L}_{int}),
      \tau_\Sigma( j_{a_1} \phi^{a_1} ), 
      \cdots,
      \tau_{\Sigma}( j_{a_{v_{out}}} \phi^{a_{v_{out}}} ) 
    \right) 
  \right\rangle
  \;\in\;
  \mathbb{C}[ [ \hbar, g , j] ]
  \,
$$

where on the right $\langle -\rangle \;\colon\; PolyObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ] \to \mathbb{C}[ [ \hbar, g, j] ]$ is the given [[Hadamard vacuum state]] (def. \ref{VacuumFree}).

These are called the _[[Feynman amplitudes]] away from coinciding interaction ponts_ for the given [[Feynman diagram]] with [[interaction]] $\mathbf{L}_{int}$ and with _external vertices_..

An [[extension of distributions]] of this to the locus of coinciding points
is called a [[renormalization|("re"-)normalization]] of this [[Feynman amplitude]].

Hence given these, then the [[vacuum expectation value]] of the perturbative [[S-matrix]] is a [[formal power series]] of [[Feynman amplitudes]]:


$$
  \mathcal{S}(g S_{int} + \sum_i \tau_{\Sigma}(j_{a_i} \phi^a)  )
  \;=\;
  \underset{\Gamma \in \mathcal{G}}{\sum} 
  \Gamma(g S_{int}, \cdots, g S_{int}, \sum_i \tau_{\Sigma}(j_{a_i} \phi^a) )
$$


=--


$$
  \begin{aligned}
    & T(V_1, \cdots, V_v, V_{v+1})
    \\
    & =
    T( T(V_1, \cdots ,V_v),  V_{v+1} )
    \\
    &=
    prod
      \circ
    \exp\left(
      \left\langle
        \hbar \Delta_F, 
        \frac{\delta}{\delta \mathbf{\Phi}} 
          \otimes 
        \frac{\delta}{\delta \mathbf{\Phi}}
      \right\rangle
    \right)
    \left(
    \left(
      prod
        \circ
      \!\!\!\!
      \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
      \underset{ { r \lt s } \atop { \in \{1, \cdots, v\} }  }{\prod}
      \frac{1}{e_{r,s}!}
      \left\langle
          (\hbar \Delta_F)^{e_{r,s}}
          \,,\,
          \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
          \frac{\delta^{e_{r,s}}}{ \delta \mathbf{\Phi}_s^{e_{r,s}} }
      \right\rangle
      (V_1 \otimes \cdots \otimes V_v)
    \right)
      \,\otimes\,
    V_{v+1}
    \right)
    \\
    & =
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v+1}}}{\sum}
    \\
    & \phantom{=}
      \underset{ {  r \lt s } \atop {  \in \{1,\cdots, v\}}  }{\prod}
      \frac{1}{e_{r,s}!}
    \left\langle
        (\hbar \Delta_F)^{e_{r,s}}
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{ \delta \mathbf{\Phi}_s^{e_{r,s}} }
    \right\rangle
    \\
    & \phantom{=}
    \underset{  
       { e_{v+1} =} 
       \atop
       { e_{1,{v+1}} + \cdots + e_{v,v+1} } 
    }{\sum}
      \underset{
        = (e_{1,v+1}) \cdots (e_{v,v+1}))
      }{
      \underbrace{
      \frac{ 
        \left(
          { e_{v+1} }
          \atop
          { (e_{1,v+1}), \cdots, (e_{v,v+1}) }
        \right) 
      }{
        ( e_{v+1} ) !
      }
      }
      }
    \left\langle
      (\hbar \Delta_F)^{e_{v+1}}
    \left(
      \frac{\delta^{e_{1,v+1}} V_1 }{\delta \mathbf{\Phi}^{e_{1,v+1}}}
        \otimes
        \cdots
        \otimes
      \frac{ 
        \delta^{e_{v,v+1}} V_v
      }{ 
        \delta \mathbf{\Phi}^{e_{v,v+1}} 
      }
    \;\otimes\;
    \frac{
      \delta^{ e_{v+1} } V_{v+1}
    }{
      \delta \mathbf{\Phi}^{e_{1,v+1} + \cdots + e_{v,v+1}}
    }
    \right\rangle
    \right)
    \\
    &=
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v+1}}}{\sum}
    \underset{ { r \lt s } \atop { \in \{1, \cdots, v+1\} } }{\prod}
    \tfrac{1}{e_{r,s}!}
    \left\langle
        (\hbar \Delta_F)^{e_{r,s}}
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_s^{e_{r,s}}}
    \right\rangle
    (V_1 \otimes \cdots \otimes V_{v+1})
  \end{aligned}
$$
