

[[DualityGraphics.jpg:file]]

\begin{imagefromfile}
  "file_name": "DualityGraphics.jpg",
  "width": 200,
  "float": "right",
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  }
\end{imagefromfile}


+-- {: .num_defn #ReducedSimplicialSet}
###### Definition

ddd

=--

Def \ref{ReducedSimplicialSet}


[[Chen Ning Yang]] on the [[physics]] of [[Yang-Mills theory]] being about the [[mathematics]] of [[connection on a bundle|connections]] on [[fiber bundles]]:

> $[$This$]$ was not just joy. There was something more, something deeper: After all, what could be more mysterious, what could be more awe-inspiring, than to find that the structure of the [[observable universe|physical world]] is intimately tied to the deep [[mathematics|mathematical]] concepts, concepts which were developed out of considerations rooted only in [[logic]] and the beauty of form?

> In 1975, impressed with the fact that [[gauge fields]] are [[connection on a bundle|connections]] on [[fiber bundles]], I drove to the house of [[Shiing-shen Chern|S. S. Chern]] in El Cerrito, near Berkeley... I said I found it amazing that [[gauge theory]] are exactly [[connection on a bundle|connections]] on [[fiber bundles]], which the mathematicians developed without reference to the physical world. I added: "this is both thrilling and puzzling, since you mathematicians dreamed up these concepts out of nowhere." He immediately protested: "No, no. These concepts were not dreamed up. They were natural and real.




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


