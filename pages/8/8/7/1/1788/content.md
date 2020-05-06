


Consider the 5d metric

$$
  g
  \;=\;
  H^{+1} \, \eta_{\mu \nu} d x^\mu \otimes d x^\nu 
    + 
  H^{-1} d z \otimes d z
$$

for $H$ a [[smooth function]] of $z$.

Notice

$$
  \sqrt{
    \left\vert
      det (g_{\kappa_1 \kappa_2})
    \right\vert
  }
  \;=\;
  H^{3/2}
$$

Consider 

$$
  A
  \in 
  \Omega^1(\mathbb{R}^{3,1})
  \overset{i^\ast}{\longrightarrow}
  \Omega^1(\mathbb{R}^{4,1})
$$

a 1-form pulled back from 4d, and in Lorenz gauge ($d \star A = 0$). Then the [[Laplace-Beltrami-operator]] on $A$ is given by

$$
  \begin{aligned}
    \big( 
      \star d \star \pm d \star d \star 
    \big) 
    d A
    \;=\;
    H^{-2} \eta^{\mu \nu}\partial_\mu \partial_\nu A
    +
    H^{-3/2}
    \partial_z
    \left(
      H^{3/2} \partial_z A
    \right)
  \end{aligned}
  \,.
$$

Proof:

First notice the general formula, akin to that of the Laplace-Beltrami operator on functions:

$$
  \begin{aligned}
    \star d \star d A
    & =
    \star d \star (\partial_{j_1} f) A_{j_2} d x^{j_1} \wedge d x^{j_2}
    \\
    & = 
    \star d
    \left( 
      \tfrac{1}{ 2 \color{green}  (D-2)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
      \,
      \epsilon_{
        i_1 i_2
        {\color{green} k_3 \cdots k_{D} }
      }
      d x^{
        \color{green} k_3
      } 
      \wedge \cdots \wedge 
      d x^{
        \color{green} k_{D}
      }
    \right)
    \\
    & =
    \star
    \partial_{ \color{magenta} k_2}
    \left( 
      \tfrac{1}{ 2 \color{green} (D-2)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{ i_1 j_1 } 
      g^{ i_2 j_2 } 
      (\partial_{j_1} A_{j_2} )
      \,
      \epsilon_{
        i_1 i_2
        {\color{green} k_3 \cdots k_{D} }
      }
      d x^{ \color{magenta} k_2 }
      \wedge 
      d x^{
        \color{green} k_3
      } \wedge \cdots \wedge 
      d x^{
        \color{green} k_{D}
      }
    \right)
    \\
    & =
    \sqrt{
      \left\vert
        det\big( (g_{i j}) \big)
      \right\vert
    }
    \underset{
      = 
      \det\big( (g_{i j})^{-1}  \big)
      \tfrac{1}{2}
      \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    }{
    \underbrace{
    \tfrac{
      (-1)^{D-1}
    }{ 
       { \color{orange} (D-1)! }
       2 { \color{green} (D-2)! }
    }
    \epsilon_{ 
      l_1
      { \color{orange} l_2 \cdots l_{D} }
    }
    g^{ 
      { \color{orange} l_1 }
      { \color{magenta} k_1  } 
    }
    g^{ 
      { \color{orange} l_2 }
      { \color{magenta} k_2  } 
    }
    g^{ 
      { \color{orange} l_3 }
      { \color{green} k_3  } 
    }
    \cdots
    g^{ 
      { \color{orange} l_D} 
      { \color{green} k_D } 
    }
    \epsilon_{
      i_1 i_2
      {\color{green} k_3 \cdots k_{D} }
    }
    }
    }
    \,
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \, 
    g_{ {\color{magenta} k_1} r }
    d x^{ \color{magenta} r  }
    \\
    & =
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} k_1 } r }
    d x^{  r }
  \end{aligned}
$$

Now specialize to the the case at hand, where 

1. $A = A_\mu d x^{\mu} A_z d^z $ 

1. $A_z = 0$

1. $\partial_\mu \eta^{\mu \nu} A_\nu = 0$ 

1. $g_{\mu nu} = H \eta_{\mu \nu}$

1. $\partial_\mu H = 0$

$$
  \begin{aligned}
    & 
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} k_1 } r }
    d x^{  r }
    \\
    & =
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} \mu_1 \mu_2 }_{i_1 i_2}
    \partial_{ \color{magenta} \mu_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} \mu_1 } r }
    d x^{  r }
    \\
    & \phantom{=}\;
    +
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} \mu_1 z }_{i_1 i_2}
    \partial_{ \color{magenta} z }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} \mu_1 } r }
    d x^{  r }
    \\
    & \phantom{=}\;
    +
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} z \mu_2 }_{i_1 i_2}
    \partial_{ \color{magenta} \mu_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} z } r }
    d x^{  r }
  \end{aligned}
$$

$$
  \begin{aligned}
    \star d \star d A
    & =\;
    H^{-3/2} 
    \partial_\mu 
    \left(
      H^{3/2} H^{-1-1} \eta^{\mu \nu} \partial_\nu A
    \right)
    +
    H^{-3/2}
    \partial_z
    \left(
      H^{3/2} H^{1-1} \partial_z A
    \right)
    \\
    & =
    H^{-2} \eta^{\mu \nu}\partial_\mu \partial_\nu f
    +
    H^{-3/2}
    \partial_z
    \left(
      H^{3/2} \partial_z A
    \right)
  \end{aligned}
$$

and hence

$$
  \begin{aligned}
    & 
    \; \star d \star d A \;=\; 0
    \\
    \Leftrightarrow
    &
    \;
    \eta^{\mu \nu}\partial_\mu \partial_\nu A
    +
    H^{+1/2}
    \partial_z
    \left(
      H^{3/2} \partial_z A
    \right)
  \end{aligned}
$$

\linebreak

$$
    \eta^{\mu \nu}\partial_\mu \partial_\nu \partial_z f
    +
    \tfrac{5}{2}
    \tfrac{1}{2}(H^2)''
    \partial_z f
    +
    (H^2 + \tfrac{1}{2}(H^2)') \partial^2_z f
$$


\linebreak

$$
  d B + Tr(d \pi \wedge d \pi \wedge d \pi)
  \;=\;
  \star_{5} F
$$

$$
  \star_5
  d \star_5 F 
  =
  \star_5
  Tr(d \pi \wedge d \pi \wedge d \pi) h' d x^4
$$

$$
  d \star_5 
  \big( 
    F + \omega \wedge d x^4
  \big)  
$$

$$
  d \star_4 F \wedge d x^4
  \;=\;
  d \big( \pi \wedge d \pi \wedge d \pi _\big) \wedge d x^4
$$

$$
  d A \wedge d x^5
  +
  d \omega \wedge d x^5
  + 
  d \rho^0 \wedge d x^5
  +
  B \wedge d x^4
  + 
  \pi \wedge d \pi \wedge d \pi \wedge d x^4
$$

$$
  \star_4
  (d A + d \omega + d \rho^0)
  = 
   B + \pi \wedge d \pi \wedge d \pi
$$

$$
  \star_4 d \star_4 F 
  = 
  - \star_4 d \star_4 d (\omega + \rho^0)
  +
  d B + d \pi \wedge d \pi \wedge d \pi
$$



\linebreak


\linebreak

\linebreak
  
\linebreak

***


\linebreak

\linebreak


If I understand well what you're after, you want to show that a ultracategory is just a $T$-algebra for a suitable monad.

My claim is that the monad acts as follows on objects:

$$ T : \mathcal{A} \mapsto \int^X \beta(X)\times \mathcal{A}^X $$ 

I am basing this conjecture on the fact that an ultracategory consists of maps

$$ i_X : \beta(X)\times \mathcal{A}^X \to \mathcal{A} $$ 

that if this conjecture is correct amount exactly to a functor $T\mathcal{A} \to \mathcal{A}$ (by the universal property of the coend, the $i_X$ forming a cowedge in $X$).

Of course, strictly speaking $T$ does not exist, because as $X$ ranges over all sets the coend I'm taking is on too large a diagram. I kindly ask you to set aside size issues and follow a bit of coend-nonsense: so, just for today $T$ exists and defines a functor.

1. First, the initial cowedge $i_X : \beta(X) \times \mathcal{A}^X \to TA$ has a component at $X=1$, the terminal category; this gives $T$ the structure of a pointed functor (of course, $i$ depends naturally on $\mathcal{A}$).

2. A candidate multiplication map $TT\mathcal{A} \to T\mathcal{A}$ can be obtained as follows:

$$\begin{array}{rl} 
TT\mathcal{A} &= \displaystyle \int^Y \beta(Y) \times T\mathcal{A}^Y \\
&\displaystyle  = \int^Y \beta(Y) \times \left( \int^X \beta(X)\times \mathcal{A}^X \right)^Y \\
&\displaystyle \to \int^Y\int^X \beta(Y) \times  \beta(X)^Y \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta(Y) \times  \beta\beta(X)^{\beta Y} \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta\beta(X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta (X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \text{colim}_Y\int^X \beta (X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \cong \int^X \beta (X) \times \mathcal{A}^{X}
\end{array}$$