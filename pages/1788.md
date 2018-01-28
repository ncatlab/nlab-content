

+-- {: .num_example #DiracFieldPolynomialObservables}
###### Example
**([[polynomial observables]] of the [[Dirac field]])**

Let $E = \Sigma \times S_{odd}$ be the [[field bundle]] of the [[Dirac field]] (example \ref{DiracFieldBundle}).

Then, by prop. \ref{DiracSpaceOfFieldHistories}, 
an $\mathbb{R}^{0\vert 1}$-parameterized plot of the space of [[off-shell]] [[polynomial observables]] (def. \ref{PolynomialObservables})

$$
  A_{(-)}
  \;\colon\;
  \mathbb{R}^{0 \vert 1}
  \longrightarrow 
  PolyObs(\Sigma \times S_{odd})
$$

is of the form

$$
  \begin{aligned}
    A_{(-)}
    & =
    a^{(0)}
    \\
    & \phantom{=}
    + 
    \theta
    \underset{\Sigma}{\int}
      a^{(1)}_{\alpha}(x)  
      \mathbf{\Psi}^\alpha(x)
    dvol_\Sigma(x)
    \\
    & = 
    \phantom{=}
    +
    \underset{\Sigma^2}{\int}
      a^{(2)}_{\alpha_1 \alpha_2}(x,y) 
      \mathbf{\Psi}^{\alpha_1}(x_1) 
        \cdot
      \mathbf{\Psi}^{\alpha_2}(x_2)
    \,
    dvol_\Sigma(x_1) \, dvol_\Sigma(x_2)
    \\
    & \phantom{=}
    +
    \theta
    \underset{\Sigma}{\int}
      a^{(3)}_{\alpha_1 \alpha_2 \alpha_3}(x_1, x_2, x_3) 
      \mathbf{\Psi}^{\alpha_1}(x_1)
       \cdot
      \mathbf{\Psi}^{\alpha_2}(x_2)
        \cdot
      \mathbf{\Psi}^{\alpha_3}(x_3)
    \, dvol_\Sigma(x_1) \, dvol_\Sigma(x_2) \, dvol_\Sigma(x_3)
    \\
    & \phantom{=}
    + \cdots
  \end{aligned}
$$

for any [[distributions of several variables]] $a^{(k)}_{\alpha_1, \cdots , \alpha_k}$. Here

$$
  \mathbf{\Psi}^\alpha(x)
  \;\colon\;
  \Gamma_\Sigma(\Sigma \times S_{even})
    \longrightarrow
  \mathbb{C}
$$

are the point-evaluation [[field observables]] (example \ref{PointEvaluationObservables}) on the [[spinor bundle]].
and 

$$
  \theta \in C^\infty(\mathbb{R}^{0\vert 1})_{odd}
$$ 

is the canonical odd-graded coordinate function
on the [[superpoint]] $\mathbb{R}^{0 \vert 1}$ (def. \ref{SuperCartesianSpace}). 

Hence all the _odd_ powers of the [[Dirac field|Dirac]]-[[field observables]] are proportional to $\theta$.

=--


+-- {: .proof}
###### Proof

By definition of supergeometric [[mapping spaces]] (def. \ref{MappingSpaceOutOfASuperCartesianSpace}),
there is a [[natural bijection]] between $\mathbb{R}^{0 \vert 1}$-plots $A_{(-)}$ of the space of observables
and smooth functionss out of the [[Cartesian product]] of $\mathbb{R}^{0 \vert 1}$ with the [[space of field histories]]
to the [[complex numbers]]:

$$
  \frac{
    \mathbb{R}^{0\vert 1}
      \overset{ A_{(-)} }{\longrightarrow}
    [ \Gamma_\Sigma(\Sigma \times S_{odd}), \mathbb{C} ]
  }
  {
    \mathbb{R}^{0 \vert 1} \times \Gamma_\Sigma(\Sigma \times S_{odd}) 
    \longrightarrow
    \mathbb{C}
  }
$$

Moreover, by prop. \ref{DiracSpaceOfFieldHistories} we have that the coordinate functions
on the space of field histories of the Dirac bundle are given by the field observables $\mathbf{\Psi}^\alpha(x)$
regarded in odd degree. Now a homomorphism as above has to pull back the even coordinate function $x$
on $\mathbb{C}$ to even coordinate functions on this Cartesian product, hence to joint even powers of 
$\theta$ and $\mathbf{\Psi}^\alpha(x)$.

=--


$$
  \begin{aligned}
    \mathcal{S}'(O)
    -
    \mathcal{S}(\mathcal{Z}(O))
    & =
    \underset{k}{\sum}
    \left(
      \frac{1}{k!}
      \frac{1}{(i \hbar)^k}
      T'_k( O^{\otimes_k} )
      -
      \underset{
        1 \lt n \leq k
      }{\sum}
      \underset{
        { \{1, \cdots, k\} = I_1 \sqcup \cdots \sqcup I_n }
        \atop
        { I_1, \cdots, I_n \neq \emptyset }
      }{\sum}
      \frac{1}{n!} \tfrac{1}{{\vert I_1\vert}! \cdots {\vert I_n\vert}!}
      \frac{1}{(i \hbar)^n}
      T_n\left(
        Z_{{\vert I_1\vert}}(O^{\otimes_{\vert I_1\vert}}),
        \cdots,
        Z_{{\vert I_n\vert}}(O^{\otimes_{\vert I_n\vert}}),  
      \right)
    \right)
    \\
    &
    \phantom{=} 
    +
    \frac{1}{i \hbar} 
    Z_k( O^{\otimes_k} )
  \end{aligned}
$$

([Dütsch 18, (3.333)](#Duetsch18))

$$
  \mathcal{Z}(O)
  \;=\;
  \underset{k \in \mathbb{N}}{\sum}
  \frac{1}{k!}
  Z_k( \underset{k \, \text{args}}{\underbrace{ O, \cdots, O }} )
$$


$$
  {\hat u}^\prime
  \,\,\,\,\,
  \hat{u'}
  \,\,\,\,\,
  {\hat u}'
$$


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
