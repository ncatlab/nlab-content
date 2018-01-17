
+-- {: .num_example}
###### Example
**([[Feynman diagrams]] in [[causal perturbation theory]])**

In [[perturbative quantum field theory]], **[[Feynman diagrams]]** are labeled [[graphs]] that encode [[product of distributions|products of]] [[Feynman propagators]], called [[Feynman amplitudes]] ([this prop.](S-matrix#FeynmanPerturbationSeriesAwayFromCoincidingPoints)).  These are the summands in the _[[Feynman perturbation series]]_ expansion of the _[[scattering matrix]]_ 

$$
  \mathcal{S}
  \left(
    S_{int}
  \right)
  = 
  \underset{k \in \mathbb{N}}{\sum} 
  \frac{1}{k!}
  \frac{1}{(i \hbar)^k}
  T( \underset{k \, \text{factors}}{\underbrace{S_{int}, \cdots , S_{int}}} )
$$

of a given [[interaction]] [[Lagrangian density]] $L_{int}$.
They arise from expanding out the _[[time-ordered products]]_ $T(\cdots)$ of the [[interaction]] with itself, which, away from coincident vertices, is given by the [[star product]] of the [[Feynman propagator]] $\Delta_F$, via the [[exponential]] contraction

$$
  T(S_{int}, S_{int}) 
  \;=\; 
  prod \circ \exp
  \left( 
     \hbar 
      \int \Delta_{F}^{a b}(x,y) 
        \frac{\delta}{\delta \mathbf{\Phi}^a(x)} 
          \otimes 
        \frac{\delta}{\delta \mathbf{\Phi}(y)}  
    \right) 
    ( S_{int} \otimes S_{int} )
   \,.
$$

Each [[edge]] in the [[Feynman diagram]]/[[graph]] corresponds to a factor of a [[Feynman propagator]]  in $T( \underset{k \, \text{factors}}{\underbrace{S_{int} \cdots S_{int}}} )$, being a [[distribution of two variables]]; and each [[vertex]] corresponds to a factor of the [[interaction]] [[Lagrangian density]] at $x_i$. 

For example [[quantum electrodynamics]] in [[Lorenz gauge]] has

1. the [[Dirac field]] modelling the [[electron]], with [[Feynman propagator]] here to be denoted $\Delta$ ([this def.](Feynman+propagator#FeynmanPropagatorForDiracOperatorOnMinkowskiSpacetime));

1. the [[electromagnetic field]] modelling the [[photon]], with [[Feynman propagator]] called the _[[photon propagator]]_, here to be denoted $G$ ([this prop.](A+first+idea+of+quantum+field+theory#PhotonPropagatorInGaussianAveragedLorenzGauge));
 
1. the [[electron-photon interaction]]

   $$
     L_{int} 
     \;=\; 
     g i 
     (\gamma^\mu)^\alpha{}_\beta
     \,
     \underset{
       { \text{incoming} \atop \text{electron}  }
       \atop
       \text{field}
     }{\underbrace{\overline{\psi_\alpha}}} 
     \;
     \underset{
       { 
         \, 
         \atop
         \text{photon}
       }
       \atop
       \text{field}
     }{\underbrace{a_\mu}} 
     \;
     \underset{
       {\text{outgoing} \atop \text{electron} }
       \atop
       \text{field}
     }{\underbrace{\psi^\beta}}
   $$ 

The [[Feynman diagram]] for the [[electron-photon interaction]] alone is

<center>
<img src="https://ncatlab.org/nlab/files/InteractionVertexOfQED.jpg" width="150">
</center>

where the solid lines correspond to the [[electron]], and the wiggly line to the [[photon]]. The corresponding [[product of distributions]] is (written in [[generalized function]]-notation)

$$
  i g (\gamma^\mu)^\alpha{}_\beta 
  \,.
  \,
  \underset{
    {\text{incoming} \atop \text{electron}}
    \atop
    \text{propagator}  
  }{
  \underbrace{
    \overline{\Delta(-,x)}_{-, \alpha} 
  }
  }
  \underset{
    {
      \, 
      \atop
      \text{photon}
    }
    \atop
    \text{propagator}
  }{
  \underbrace{
     G(x,-)_{\mu,-}
  }
  }
  \underset{
    { \text{outgoing} \atop \text{electron} }
    \atop
    \text{propagator}
  }{
  \underbrace{
    \Delta(x,-)^{\beta, -} 
  }
  }
$$

Hence a typical Feynman diagram in the [[QED]] [[Feynman perturbation series]] induced by this [[electron-photon interaction]] looks as follows:

<center>
<img src="https://ncatlab.org/nlab/files/FeynmanDiagramGlobal.jpg" width="560"/>
</center>

where on the bottom the corresponding [[product of distributions]] is shown.
(Now the contraction of the internal indices and all prefactors are notationally suppressed.)

For instance the two solid [[edges]] between the [[vertices]] $x_2$ and $x_3$ corresponds to the two factors of $\Delta(x_2,x_2)$:

<center>
<img src="https://ncatlab.org/nlab/files/FeynmanDiagramComponent1.jpg" width="560"/>
</center>

This way each sub-graph encodes its corresponding subset of factors in the [[Feynman amplitude]]:

<center>
<img src="https://ncatlab.org/nlab/files/FeynmanDiagramComponentTwo.jpg" width="560"/>
</center>

<center>
<img src="https://ncatlab.org/nlab/files/FeynmanDiagramComponentThree.jpg" width="560"/>
</center>

> graphics grabbed from  [Brouder 10](Feynman+diagram#Brouder10)

A priori this [[product of distributions]] is defined away from coincident vertices: $x_i \neq x_j$. The definition at coincident vertices $x_i = x_j$ requires a choice of _[[extension of distributions]]_ to the [[diagonal]] locus. This choice is the [[renormalization|("re-")normalization]] of the [[Feynman amplitude]].

=--