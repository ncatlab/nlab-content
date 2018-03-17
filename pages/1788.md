
$$
  \array{
  \text{fibration} & \array{\text{vector space underlying} \\ \text{minimal dg-model}} & \array{ \text{differential on} \\ \text{minimal dg-model} }
   \\
  \array{
    S^4
    \\
    \downarrow
    \\
    S^3
  }
  &
  Sym^\bullet \langle h_3\rangle 
  \otimes
  \left\langle 
     \underset{deg = 2p}{
     \underbrace{
       \omega_{2p}
     }},
     \underset{deg = 2p + 4}{ 
     \underbrace{
       f_{2p + 4}
     }} \,\vert\, p \in \mathbb{N} 
  \right\rangle
  &
  d \colon
  \left\{
    \begin{aligned}
      \omega_0 & \mapsto 0
      \\
      \omega_{2p+2} &\mapsto h_3 \wedge \omega_{2p}
      \\
      f_4 & \mapsto 0
      \\
      f_{2p+6} & \mapsto h_3 \wedge f_{2p + 4}
    \end{aligned}
    \right.
  \\
  \array{
    S^0
    \\
    \downarrow
    \\
    S^3
  }
  &
  Sym^\bullet \langle h_3\rangle 
  \otimes
  \left\langle 
     \underset{deg = 2p}{
     \underbrace{
       \omega_{2p}
     }},
     \underset{
       deg = 2p
     }{ 
     \underbrace{
       f_{2p}
     }} \,\vert\, p \in \mathbb{N} 
  \right\rangle
  &
  d \colon
  \left\{
    \begin{aligned}
      \omega_0 & \mapsto 0
      \\
      \omega_{2p+2} &\mapsto h_3 \wedge \omega_{2p}
      \\   
      f_0 & \mapsto 0
      \\
      f_{2p+2} &\mapsto h_3 \wedge f_{2p}
    \end{aligned}
    \right.
  \\
  \array{
    S^4//S^1
    \\
    \downarrow
    \\
    S^3
  }
  &
  Sym^\bullet  \langle h_3 , f_2 \rangle 
   \otimes
  \left\langle 
    \underset{deg = 2p}{
    \underbrace{
      \omega_{2p}
    }},
    \underset{
      deg =2p + 4
    }{ 
    \underbrace{
      f_{2p + 4}
    }} \,\vert\, p \in \mathbb{N}
  \right\rangle
  &
  d \colon
  \left\{
    \begin{aligned}
      \omega_0 & \mapsto 0
      \\
      \omega_{2p+2} &\mapsto h_3 \wedge \omega_{2p}
      \\
      f_2 & \mapsto 0
      \\
      f_{2p+4} & \mapsto h_3 \wedge f_{2p + 2}
    \end{aligned}
  \right.
  }
$$

$\,$


$\,$


$\,$


$$
  0
    \to
  \mathbb{Z}
    \overset{\phantom{AA} \iota \phantom{AA}}{\hookrightarrow}
  \mathbb{R}
    \overset{
      \exp\left(  \tfrac{1}{2\pi i}(-) \right) 
    }{ \longrightarrow }
   U(1)
     \to
   0 
$$

$$
  \array{
    && \mathbf{B}^n \mathbb{Z}
    \\
    & 
      {}^{\mathllap{mod\, 2}}\swarrow 
    && 
    \searrow^{\mathrlap{(-)/2}}
    \\
    \mathbf{B}^n \mathbb{Z}/2\mathbb{Z}
    && &&
    \mathbf{B}^n \flat \mathbb{R}
    \\
    & 
    {}_{\mathllap{
      \exp\left(
        \tfrac{1}{2 \cdot 2\pi i}(-)
      \right)
    }}\searrow 
    && \swarrow_{\mathrlap{ \exp\left( \tfrac{1}{2 \pi i}(-) \right) }}
    \\
    && \mathbf{B}^{n} \flat U(1)
    \\
    && 
    \downarrow^{ \mathrlap{ \cdot 2 } }
    \\
    && \mathbf{B}^{n} \flat U(1)
    
  }
$$

$\,$


$\,$


$\,$

$\,$


$\,$

$\,$

$$
  H_3 \coloneqq A \wedge d A
$$

$$
  \begin{aligned}
  \delta
  \left(
     \int_{X_{10}}
     H_3 \wedge 
     \star H_3
  \right)
  & =
  2 \int_{X_{10}} \delta A  \wedge F_2 \wedge \star H_3
  +
  \int_{X_{10}}
  A \wedge d \delta A
  \wedge \star H_3
  +
  \int_{X_{10}}
  H_3
  \wedge \star ( A \wedge d \delta A)
  \\
  & =
  2 \int_{X_{10}} \delta A  \wedge F_2 \wedge \star H_3
  +
  \int_{X_{10}}
  A \wedge d \delta A
  \wedge \star H_3
  +
  \int_{X_{10}}
  ( A \wedge d \delta A)
  \wedge \star 
  H_3
  \end{aligned}
$$

$$
  \begin{aligned}
    & 
    B^{a}{}_b \wedge B^b{}_c 
    \partial_{B^a{}_{b'}} \partial_{B^{b'}{}_c}
    (
      B^{d}{}_e \wedge B^{e}{}_f
    )
    \\
    & =
    B^{a}{}_b \wedge B^b{}_e 
    \partial_{B^a{}_{d}} 
    B^{e}{}_f
    -     
    B^{a}{}_b \wedge B^{b d} 
    \partial_{B^{a e}} 
    B^{e}{}_f
    \\
    & \phantom{=}
    -
    B^{a}{}_b \wedge B^b{}_f 
    \partial_{B^a{}_{b'}}
    B^{d}{}_{b'} 
    +
    B^{a}{}_b \wedge B^b{}_c 
    \partial_{B^{a f}} 
    B^{d c} 
    \\   
    & =
    B^{a}{}_b \wedge B^b{}_e 
    -     
    B^{a}{}_b \wedge B^{b d} 
    \partial_{B^{a e}} 
    B^{e}{}_f
    \\
    & \phantom{=}
    -
    B^{a}{}_b \wedge B^b{}_f 
    \partial_{B^a{}_{b'}}
    B^{d}{}_{b'} 
    +
    B^{a}{}_b \wedge B^b{}_c 
    \partial_{B^{a f}} 
    B^{d c} 
    \\
    & =
    10 B_{f b} \wedge B^{b d}
    -
    10 B^d{}_b \wedge B^b{}_f
    \\   
    & = 
    - 20 \cdot B^{d}{}_e \wedge B^{e}{}_f
  \end{aligned}
$$

$$
  \eta^\alpha_\mu = \phi \psi^\alpha_\mu +  \Gamma^{\mu}{\alpha \beta} \partial_\mu \phi
$$

Nice latex

## classic ##
`fixed width`
### `oh! sweet nuthin'` 
#### _she ain't got nuthin' at all_ ####