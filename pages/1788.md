


+-- {: .num_remark}
###### Remark

In Def. \ref{Orbifold} the condition of [[n-truncated object in an (infinity,1)-category|0-truncation]] is crucial in two respects:

1. First of all it means that $\mathcal{X} \to \mathbb{B}G$ is a [[faithful morphism]] which identifies it as an object in geometric $G$-[[equivariant homotopy theory]] via

   $$
     \left(
       \array{
         \mathcal{X}
         \\
         \downarrow
         \\
         \mathbb{B}G
       }
     \right)
     \;\in\;
     \left(
     \left(
       \mathbf{H}_{sing}
     \right)_{/\mathbb{B}G}
     \right)_{faith}
     \;\simeq\;
     Sh_\infty\left( G Orbits, \mathbf{H}\right)
   $$

1. but moreover, only with this condition is the [[shape modality|shape]] of an orbifold in the sense of Prop. \ref{Orbifold} the _expected_ object in plain $G$-[[equivariant homotopy theory]]


   $$
     &#643; \mathcal{X}
     \;\in\;
     \underset{
       \simeq Sh_\infty\left( G Orbits, \infty Groupoids \right)
     }{
     \underbrace{
       Sh_\infty\left( Singularities, \infty Groupoids \right)_{/\mathbb{B}G}
     }
     }
     \overset{Disc}{\hookrightarrow}
     \underset{
       \mathbf{H}_{sing}
     }{
     \underbrace{
       Sh_\infty\left( Singularities, \mathbf{H} \right)_{/\mathbb{B}G}
     }
     }
   $$

The second point comes about as follows: Given ab [[G-space]] $X$, its incarnation as an object in plain (non-geometric) [[globally equivariant homotopy theory]] is ([Rezk 14, 3.2](#Rezk14))

$$
  \delta_G
  \;\colon\;
  \mathbb{B}K 
  \;\mapsto\;
  \vert TopGroupoid\left( \ast\sslash K, X \sslash G\right) \vert
  \,,
$$

=--

...

$\acts$

$\textcircled{1}$