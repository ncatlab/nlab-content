

$$
  S_{eff,0,\Lambda}(O)
  -
  S_{eff}(O)
  =
  (O - Z_\Lambda(O))
$$


$$
  \begin{aligned}
  & 
  \frac{1}{(k+2)!}
  \frac{d}{d \Lambda} 
  (
    \underset{
      k+2 \, \text{factors}
    }{
    \underbrace{
      O 
        \star_{F,\Lambda} 
        \cdots 
        \star_{F,\Lambda}
      O
    }
    }
  )
  \\
  & =
  \frac{d}{d \Lambda}
  \left(
    prod
    \circ
    \exp\left(
      \hbar
      \underset{1 \leq i \lt j \leq k}{\sum}
      \left\langle
         \Delta_{F,\Lambda}
         ,
         \frac{\delta}{\delta \mathbf{\Phi}_i}
         \frac{\delta}{\delta \mathbf{\Phi}_j}
      \right\rangle
    \right)
    (
      \underset{
        k + 2 \, \text{factors}
      }{
      \underbrace{
        O \otimes \cdots \otimes O
      }
      }
    )
  \right)
  \\
  & =
  \underset{
    = \frac{1}{2} \frac{1}{k!}
  }{
  \underbrace{
    \frac{1}{(k+2)!}
    \left(
      k + 2
      \atop
      2
    \right)
  }}
  \left(
    \frac{d}{d \Lambda}
    O
     \star_{F,\Lambda}
    O
  \right)
    \star_{F,\Lambda}
  \underset{
    k \, \text{factors}
  }{
  \underbrace{
  O
    \star_{F,\Lambda}
    \cdots
    \star_{F,\Lambda}
  O
  }
  }
  \end{aligned}
$$

Here $\frac{\delta}{\delta \mathbf{\Phi}_i}$ denotes the functional derivative of the $i$th tensor factor of $O$, and the binomial coefficient counts the number of ways that an unordered pair of distinct labels of tensor factors may be chosen from a total of $k+2$ tensor factors, where we use that the [[star product]] $\star_{F,\Lambda}$ is commutative (by symmetry of $\Delta_{F,\Lambda}$) and associative (by [this prop.](star+product#AssociativeAndUnitalStarProduct)).

With this we compute as follows:

$$
  \begin{aligned}
    0
    & = 
    \frac{d}{d \Lambda} \mathcal{S}(g S_{int} + j A)
    \\
    & =
    \frac{d}{d \Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    \\
    & = 
    \left(
      \frac{1}{i \hbar} 
      \frac{d}{d \Lambda} S_{eff,\Lambda}
    \right)
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    +
    \left(
      \frac{d}{d \Lambda} 
      \mathcal{S}_{\Lambda}
   \right)
   \left( S_{eff, \Lambda} \right)
    \\
    & =
    \left(
      \frac{1}{i \hbar} 
      \frac{d}{d \Lambda} S_{eff,\Lambda}
    \right)
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda(S_{eff,\Lambda})
    \;+\;
    \frac{1}{2}
    \frac{d}{d \Lambda'} 
    \left(
      \frac{1}{i \hbar} S_{eff,\Lambda}
        \star_{F,\Lambda'}
      \frac{1}{i \hbar} S_{eff, \Lambda}
    \right)
    \vert_{\Lambda' = \Lambda}
      \star_{F,\Lambda}
    \mathcal{S}_\Lambda
    \left( 
      S_{eff, \Lambda} 
    \right)
  \end{aligned} 
$$

Acting on this equation with the multiplicative inverse $(-) \star_{F,\Lambda} \mathcal{S}_\Lambda( - S_{eff,\Lambda} )$ (using that $\star_{F,\Lambda}$ is a commutative product, so that exponentials behave as usual) this yields the claimed equation.


+-- {: .num_example #FieldSpeciesQED}
###### Example
**(field species in [[quantum electrodynamics]])**

abc

=--

see \ref{FieldSpeciesQED}


[[QEDVacuumDiagram.png:file]]

<img src="https://ncatlab.org/nlab/files/QEDVacuumDiagram.png" width="200">

$$
  E_{\text{BV-BRST}}
  \;\simeq\;
   \underset{
      \text{Dirac}
      \atop
      \text{field}
    }{
    \underbrace{
    (S_{odd} \times \Sigma)
    }}
     \times_\Sigma
   \underset{
     \text{gauge fixed}
     \atop
     \text{electromagnetic field}
   }{
   \underbrace{
   \underset{
     {\text{electromagnetic}}
     \atop
     {\text{field}}
    }{
    \underbrace{
    T^\ast\Sigma
    }}
      \times_\Sigma
    \underset{
      \text{ghost}
      \atop
      \text{field}
    }{
    \underbrace{
    (\mathbb{R}[1] \times \Sigma)
    }}
      \times_\Sigma
    \underset{
      \text{NL auxiliary}
      \atop
      \text{field}
    }{
    \underbrace{
    (\mathbb{R} \times \Sigma)
    }}
      \times_\Sigma
    \underset{
      \text{antighost}
      \atop
      \text{field}
    }{
    \underbrace{
    (\mathbb{R}[-1] \times \Sigma)
    }}
    }
    }
$$


$$
  \Bigtimes, \bigtimes,\big\times
$$


$$
  \begin{aligned}
   &
   \left\langle
     {\, \atop \,}
     (A_{out, 1})_{int}
     \cdots
     (A_{out,n_{out}})_{int}
     \,
     (A_{in, 1})_{int}
     \cdots
     (A_{in,n_{in}})_{int}
     {\, \atop \,}
   \right\rangle
   \\
   & =
   \left\langle 
     {\, \atop \,}
       A_{out,1}
       \cdots
       A_{out,n_{out}}
    \right|
       \;
       \mathcal{S}(g S_{int})
       \;
    \left|
       A_{in,1}
       \cdots
       A_{in, n_{in}}
     {\, \atop \,}
   \right\rangle
   \\
   & \coloneqq
   \frac{1}{ 
     \left\langle \mathcal{S}(g S_{int}) \right\rangle 
   }   
   \left\langle
     {\, \atop \,}
       A_{out,1}
       \cdots
       A_{out,n_{out}}
       \;
       \mathcal{S}(g S_{int})
       \;
       A_{in,1}
       \cdots
       A_{in, n_{in}}
     {\, \atop \,}
   \right\rangle
   \,.
  \end{aligned}
$$


+-- {: .num_defn}
###### Definition
**([[vacuum stability]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to def. \ref{VacuumFree}, let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to def. \ref{LagrangianFieldTheoryPerturbativeScattering}, and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]\langle g \rangle$ be a [[local observable]], regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

We say that the given [[Hadamard vacuum state]] is _[[vacuum stability|stable]]_ with respect to the [[interaction]] $S_{int}$, if for all elements of the [[Wick algebra]]

$$
  A \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g] ] 
$$

we have

$$
  \left\langle
    A \mathcal{S}(g S_{int})
  \right\rangle
  \;=\;
  \left\langle
     \mathcal{S}(g S_{int})
  \right\rangle
  \,
  \left\langle
    A
  \right\rangle
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \left\langle
    \mathcal{S}(g S_{int})^{-1}
    A
  \right\rangle
  \;=\;
  \frac{1}
  {
    \left\langle
      \mathcal{S}(g S_{int})
    \right\rangle
   }
   \left\langle 
     A  
   \right\rangle
$$

=--


$$
  S_1 {\gt\!\!\!\!\lt} S_2
  \phantom{AAA}
  \text{for}
  \phantom{AAA}
  \array{
    S_1 {\vee\!\!\!\wedge} S_2
    \\
    \text{and}
    \\
    S_2 {\vee\!\!\!\wedge} A_1 
  }
$$

Suppose that

$$
  supp(A_1) {\vee\!\!\!\!\wedge} supp(A_2)
$$

then (by [[causal additivity]]):

$$
  \begin{aligned}
    (A_1)_{int}
    (A_2)_{int}
    & =
    \left(
      \frac{\partial}{\partial j} \mathcal{Z}(j A_1 )
    \right)_{\vert j = 0}
    \left(
      \frac{\partial}{\partial j} \mathcal{Z}( j A_2 )
    \right)_{\vert j = 0}
    \\
    & =
    \frac{\partial^2}{\partial j_1 \partial j_2}
    \left(
      {\, \atop \,}
      \mathcal{Z}( j_1 A_1 )
      \mathcal{Z}( j_2 A_2 )
      {\, \atop \,}
    \right)_{ 
       \left\vert { {j_1 = 0}, \atop {j_2 = 0} } \right. 
    }
    \\
    & =
    \frac{\partial^2}{\partial j_1 \partial j_2}
    \left(
      {\, \atop \,}
      \mathcal{Z}( j_1 A_1 + j_2 A_2 )
      {\, \atop \,}
    \right)_{ 
       \left\vert { {j_1 = 0}, \atop {j_2 = 0} } \right. 
    }
  \end{aligned}
$$

Suppose moreover that

$$
  supp(A_{out})
   {\vee\!\!\!\wedge}
  supp(S_{int})
   {\vee\!\!\!\wedge}
  supp(A_{in})
$$

then (again by [[causal additivity]]):

$$
  \begin{aligned}
    (A_{out})_{int} (A_{in})_{int}
    & =
    \frac{d^2 }{\partial j_{out} \partial j_{in}}
    \left(
       \mathcal{Z}( j_{out} A_{out} )
       \mathcal{Z}( j_{in} A_{in} )
    \right)_{\left\vert { { j_{out} = 0 } \atop { j_{in} = 0 } }  \right.}
    \\
    & =
    \frac{\partial^2 }{\partial j_{out} \partial j_{in}}
    \left(
       \mathcal{S}(g S_{int})^{-1} 
       \underset{
         = 
         \mathcal{S}(j_{out} A_{out})
         \mathcal{S}(g S_{int})
       }{
       \underbrace{
         \mathcal{S}(g S_{int} + j_{out} A_{out})
       }
       }
       \mathcal{S}(g S_{int})^{-1} 
       \underset{
         = \mathcal{S}(g S_{int}) \mathcal{S}(j_{in} A_{in})
       }{
       \underbrace{
         \mathcal{S}(g S_{int} + j_{in}A_{in})
       }
       }
    \right)_{\left\vert { { j_{out} = 0 } \atop { j_{in} = 0 } }  \right.}    
    \\
    & =
    \frac{\partial^2 }{\partial j_{out} \partial j_{in}}
    \left(
       \mathcal{S}(g S_{int})^{-1} 
       \mathcal{S}(j_{out} A_{out}) 
       \underset{
         = \mathcal{S}(g S_{int})
       }{
       \underbrace{
         \mathcal{S}(g S_{int})
         \mathcal{S}(g S_{int})^{-1} 
         \mathcal{S}(g S_{int})
       }
       }
       \mathcal{S}(j_{in} A_{in})
    \right)_{\left\vert { { j_{out} = 0 } \atop { j_{in} = 0 } }  \right.}    
    \\
    \\
    & =
    \mathcal{S}(g S_{int})^{-1} 
    \,
    \underset{
      \text{"S-matrix element"}
    }{
    \underbrace{
    \left(
      {\, \atop \,}
      A_{out}
      \mathcal{S}(g S_{int})
      A_{in}
      {\, \atop \,}
    \right)
    }
    }
  \end{aligned}
$$

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$
