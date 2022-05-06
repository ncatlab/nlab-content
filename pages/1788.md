




$$
  \underline{\mathbf{1}}
  \;\;
  \colon
  \;\;
  \array{
    \mathbb{Z}_2/1  
    &\mapsto&
    \mathbf{1}
    \\
    \big\downarrow 
    &&
    \big\downarrow{}^{\mathrlap{id}}
    \\
    \mathbb{Z}_2/\mathbb{Z}_2
    &\mapsto&
    \mathbf{1}
  }
$$

The injective envelope is 


Let the equivariance group be the [[cyclic group of order 2]]:

$$
  G \;\coloneqq\;  \mathbb{Z}_2
$$

The [[orbit category]] looks like this:

\[
  \label{OrbitCategoryOfZMod2}
  \mathbb{Z}_2
  Orbits
  \;=\;
  \left\{
  \array{
    \mathbb{Z}_2/1
    &
      \overset{
        \phantom{AAAAA}
      }{ 
        \longrightarrow
      }
    &
    \mathbb{Z}_2/\mathbb{Z}_2
    \\
    Aut = \mathbb{Z}_2
    &&
    Aut = 1
  }
  \right\}
\]

i.e.:

$$
  \begin{aligned}
    G Orbits
    \big(
      \mathbb{Z}_2/\mathbb{Z}_2
      \,,\,
      \mathbb{Z}_2/\mathbb{Z}_2
    \big)
    \;\simeq\;
    1
    \\
    G Orbits
    \big(
      \mathbb{Z}_2/1
      \,,\,
      \mathbb{Z}_2/\mathbb{Z}_2
    \big)
    \;\simeq\;
    \ast
    \\
    G Orbits
    \big(
      \mathbb{Z}_2/\mathbb{Z}_2
      \,,\,
      \mathbb{Z}_2/1
    \big)
    \;\simeq\;
    \emptyset
    \\
    G Orbits
    \big(
      \mathbb{Z}_2/1
      \,,\,
      \mathbb{Z}_2/1
    \big)
    \;\simeq\;
    \mathbb{Z}_2
  \end{aligned}
$$

Consider the [[topological G-space]]

$$
  \prec (X \sslash G)   
    \;\coloneqq\; 
  \prec (S^4 \sslash \mathbb{Z}_2)
$$

with $\mathbb{Z}_2$ [[action|acting]] on the [[4-sphere]] $S^4 = S(\mathbb{R}^5)$ by the [[involution]] $(x^1, x^2, x^3, x^4, x^5) \mapsto (x^1, x^2, x^3, - x^4, - x^5)$.

Minimal equivariant Sullivan model

**Stage 0**

$$
  CE(\mathfrak{l} \prec (X \sslash G) )_0
  \;\coloneqq\;
  \underline{\mathbb{Q}}
$$

**Stage 1**

$$
  CE(\mathfrak{l} \prec (X \sslash G) )_1
  \;\coloneqq\;
  \underline{\mathbb{Q}}
$$

**Stage 2**

$$
  CE(\mathfrak{l} \prec (X \sslash G) )_2
  \;\coloneqq\;
  \mathbb{Q}
  \big[
    I_1(\mathbf{1})
  \big]
  \big/
  \big(
    d\, I_1(\mathbf{1}) = 0
  \big)
$$


Consider the [[vector G-space]] given by


$$
  I_1(\mathbf{1})
  \;\;
  \colon
  \;\;
  \array{
    \mathbb{Z}_2/1  
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, \mathbf{1} \oplus \mathbf{1}_{sgn}
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/1, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    &
    \simeq 
    &
    \mathbf{1}
    \\
    \big\downarrow 
    &&
    \\
    \mathbb{Z}_2/\mathbb{Z}_2
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, 0
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/\mathbb{Z}_2, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    & \simeq
    &
    0
  }
$$


$$
  I_1(\mathbf{1}_{sgn})
  \;\;
  \colon
  \;\;
  \array{
    \mathbb{Z}_2/1  
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, \mathbf{1} \oplus \mathbf{1}_{sgn}
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/1, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}_{sgn}
    \Big)
    &
    \simeq 
    &
    \mathbf{1}_{sgn}
    \\
    \big\downarrow 
    &&
    \\
    \mathbb{Z}_2/\mathbb{Z}_2
    &\mapsto&
    \mathbb{Z}_2 Reps
    \Big(
      \underset{
        \simeq \, 0
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/\mathbb{Z}_2, \mathbb{Z}_2/1 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}_{sgn}
    \Big)
    & \simeq
    &
    0
  }
$$



$$
  I_{\mathbb{Z}_2}(\mathbf{1})
  \;\;
  \colon
  \;\;
  \array{
    \mathbb{Z}_2/1  
    &\mapsto&
    1 Reps
    \Big(
      \underset{
        \simeq \, 0
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/1, \mathbb{Z}_2/\mathbb{Z}_2 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    &
    \simeq 
    &
    0
    \\
    \big\downarrow 
    &&
    \\
    \mathbb{Z}_2/\mathbb{Z}_2
    &\mapsto&
    1 Reps
    \Big(
      \underset{
        \simeq \, \mathbb{Q}
      }{
      \underbrace{
        \mathbb{Q}
        \big[
          \mathbb{Z}_2 Orbits( \mathbb{Z}_2/\mathbb{Z}_2, \mathbb{Z}_2/\mathbb{Z}_2 )
        \big]   
      }
      }
      \,,\,
      \mathbf{1}
    \Big)
    & \simeq
    &
    \mathbf{1}
  }
$$


