

Suppose that

$$
  supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
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
