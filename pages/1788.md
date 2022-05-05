
$\bigotimes$

$$
  \array{
    && L X
    \\
    &{}^{\mathllap{id}}\nearrow& \big\uparrow{}^{ \mathrlap{ L \epsilon_X } }
    \\
    L X &\underoverset{\simeq}{ \eta_{L X} }{\longrightarrow}& L \iota L X
    \\
    {}^{\mathllap{ f }}
    \big\downarrow
      &&
    \big\downarrow{}^{\mathrlap{ L \iota f }}
    \\
    L Y &\underoverset{ \eta_{L Y} }{\simeq}{\longrightarrow}& L \iota L Y
    \\
    & {}_{\mathllap{id}}\searrow  & \big\downarrow{}^{\mathrlap{ L \epsilon_Y }}
    \\
    && L Y
  }
$$

$\,$

$\,$

$$
  \array{
     c && \mathbf{X}(d)
     \\
     {}^{\mathllap{ f }}\big\downarrow
       &&
     \big\uparrow{}^{\mathrlap{ \mathbf{X}(f) \, \text{"=}(-)\circ f\text{"}}}
     \\
     d && \mathbf{X}(c)
  }
$$


the localization at $\mathcal{F}'$-equivalences is [[smashing localization]], given by smashing with 

$$
  \tilde E \mathcal{F}
$$

Prop. 9.1, 9.2

for $X$ a space and $E$ a spectrum

$$
  \left(
     \tilde E \mathcal{F}[N]
     \wedge E 
     \wedge X
  \right)
  \;\simeq\;
  \left(
     \tilde E \mathcal{F}[N]
     \wedge E 
  \right)
     \wedge X^N
$$

prop. 9.12

we have

$$
  Hom_{G Spectra}\left( 
    \tilde E \mathcal{F} X, 
    \tilde E \mathcal{F} Y
  \right)
  \;\simeq\;
  Hom_{G Spectra}\left( 
    X, 
    \tilde E \mathcal{F} Y
  \right)
$$

(top of p. 109)

hence

$$
  loc_{X,Y}
  \coloneqq
  Hom_{G Spectra}(X, (S^0 \to \tilde E \mathcal{F}) \wedge Y)
  \;\colon\;
  Hom_{G Spectra}(X,Y)
    \longrightarrow
  Hom_{L_{\mathcal{F}'} G Spectra}(X,Y)
$$

is localization


the map 

$$
  \begin{aligned}
  E^{\epsilon^\ast \alpha}(\epsilon^\sharp X)
  & =
  Hom_{G Spectra}\left( 
    \epsilon^\sharp \Sigma^\infty_{G/N} X  
    \;,\;  
    \Sigma^\infty_G S^{\epsilon \alpha} \wedge E
  \right)
  \\
  & \simeq
  Hom_{G Spectra}\left( 
    \epsilon^\sharp \Sigma^\infty_{G/N} X  
    \;,\;  
    \Sigma^\infty_G S^{\epsilon \alpha} \wedge S^0 \wedge E
  \right)
  \\
  & \simeq
  \overset{ loc }{\longrightarrow}
  Hom_{G Spectra}\left( 
    \epsilon^\sharp \Sigma^\infty_{G/N} X  
    \;,\;  
    \Sigma^\infty_G S^{\epsilon \alpha} \wedge \tilde E \mathcal{F}[N]\wedge E
  \right)
  \\
  & \simeq
  Hom_{G/N Spectra}\left( 
     \Sigma^\infty_{G/N} X
    \;,\; 
    \left(    
       \Sigma^\infty_G S^{\epsilon^\ast \alpha} \wedge \tilde E \mathcal{F}[N]\wedge E
    \right)^N
  \right)
  \\  
  & \simeq
  Hom_{G/N Spectra}\left( 
     \Sigma^\infty_{G/N} X
    \;,\; 
    \left(    
       \Sigma^\infty_G S^{\epsilon^\ast \alpha} 
    \right)^N
    \wedge 
    \left(
       \tilde E \mathcal{F}[N]\wedge E
    \right)^N
  \right)  
  \\
  & \simeq
  Hom_{G/N Spectra}\left( 
     \Sigma^\infty_{G/N} X
    \;,\; 
    \left(    
       \Sigma^\infty_G S^{\epsilon^\ast \alpha} 
    \right)^N
    \wedge 
    \Phi^N E
  \right)  
  \end{aligned}
$$


