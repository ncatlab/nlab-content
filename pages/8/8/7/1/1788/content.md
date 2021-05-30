$$
a_N(n) ~ \frac{N^n}{\pi^{N/2}} \cdot \biggl( \frac{N}{n}   \biggr)^{\frac{N(N-1)}{4}} \cdot \prod_{j = 1}^N \Gamma \biggl( \frac{j}{2} \biggr) .
$$


$$
  \begin{aligned}
  \left\vert
    sYT_n(N)
  \right\vert  
  &
  \;
  \overset{
    n \to \infty
  }{\sim}
  \;
  \underset{
    \gamma_N
  }{
  \underbrace{
    (2 \pi)^{ -(N-1)/2 }
    \cdot
    N^{ N^2 / 2 }
  }
  }
  \cdot
  n^{ - (N - 1)(N + 2)/4 }
  \cdot
  N^{ n }
  \cdot
  n^{ (N - 1)/2 }
  \cdot
  \underset{
    \mathclap{
      x_1 \geq \cdots \geq x_N
    }
  }{\int}
    \;\;\;\;\;
    \underset{
      D(x_1, \cdots, x_N)
    }{
    \underbrace{
    \underset{i \lt j}{\prod}
    \big(
      x_i - x_j 
    \big)
    }
    }
    e^{ - N \left\vert x\right\vert^2 /2 }
   d x_1 \cdots d x_{N}
   \\
   & \;=\;
   (2 \pi)^{ -\tfrac{1}{2}( N - 1 ) }
   \cdot
   N^{ \tfrac{1}{2} N^2 + n}
   \cdot
   n^{  - \tfrac{1}{4}( N^2 + N ) }
   \cdot
   \underset{
     \mathclap{
       x_1 \geq \cdots \geq x_N
     }
   }{\int}
    \;\;\;\;\;
   \underset{i \lt j}{\prod}
   \big(
     x_i - x_j 
   \big)
   e^{ - N \left\vert x\right\vert^2 /2 }
   d x_1 \cdots d x_{N}
   \\
   & \;=\;
   (2 \pi)^{ -\tfrac{1}{2}( N - 1 ) }
   \cdot
   N^{ \tfrac{1}{2} N^2 + n}
   \cdot
   n^{  - \tfrac{1}{4}( N^2 + N ) }
   \cdot
   \underset{
     \mathclap{
       { x_1 \geq \cdots \geq x_N }
       \atop
       { \vert x \vert^2 = 1 }
     }
   }{\int}
    \;\;\;\;\;
   \underset{i \lt j}{\prod}
   \big(
     x_i - x_j 
   \big)
   dvol_{S^{N}}
   \,
   \int_0^{\infty}
   R^{ N(N-1) / 2 }
   e^{ - N R^2 /2 }
   d R
   \\
   & \;\propto\;
   (2 \pi)^{ -\tfrac{1}{2}( N - 1 ) }
   \cdot
   N^{ \tfrac{1}{2} N^2 + n}
   \cdot
   n^{  - \tfrac{1}{4}( N^2 + N ) }
   \,
   N^{ - \tfrac{1}{4} (N^2 - N) }
   \\
   & \;=\;
   (2 \pi)^{ -\tfrac{1}{2}( N - 1 ) }
   \cdot
   N^{ \tfrac{1}{4} (N^2 + N) + \tfrac{1}{2} n}
   \cdot
   n^{  - \tfrac{1}{4}( N^2 + N ) }
  \end{aligned}
$$