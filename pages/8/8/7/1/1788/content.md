$\leftrightarrows$


In particular

* the [[adjunction counit]] is 

  $$
    \epsilon^{
      \widehat{L} \dashv \widehat{R}
    }_{
      \mathscr{V}_{\mathbf{x}}
    }
    \;\colon\;
    \widehat{L}
    \widehat{R}
    \big(\mathscr{V}_{\mathbf{x}}\big)
    =
    \Big(
      \big(\epsilon^{L \dashv R}_{\mathbf{x}}\big)^\ast
      \mathscr{V}
    \Big)_{ L R(\mathbf{x}) }
    \overset{
      (id)_{\epsilon^{L \dashv R}_{\mathbf{x}}}
    }{\longrightarrow}
    \mathscr{V}_{\mathbf{x}}
  $$

$$
\array{
  \Bigg\{
    \mathscr{V}_{x}
      \xrightarrow{ \phi_{f} }
    \mathscr{V}'_{x'}
    \;\displaystyle{\Bigg\vert}\;
    \array{
      \mathscr{V} 
        &\xrightarrow{ \phi }& 
      L(f)^\ast \mathscr{V}' 
      & \in C_{L(x)}
      \\
      x 
        &\xrightarrow{ f }& 
      x'
      & \in \mathcal{D}
    }
  \Bigg\}
  \,\equiv
  &
  \!\!\!\!\!\!\!\!
  \Big(
    \underset
      {x \in \mathcal{D}}
      {\textstyle{\int}} 
    C_{L(x)}
  \Big)
  &
  \underoverset
    {\underset{\widehat R}{\longleftarrow}}
    {\overset{\widehat L}{\longrightarrow}}
    {\;\; \bot \;\;}
  &
  \Big(
    \underset
      {\mathbf{x} \in \mathbf{D}}
      {\textstyle{\int}} 
    C_{\mathbf{x}}
  \Big)
  &
  \!\!\!\!\!\!\!\!
  \equiv
  \,
  \Bigg\{
    \mathscr{V}_{\mathbf{x}}
      \xrightarrow{ \phi_{\mathbf{f}} }
    \mathscr{V}'_{\mathbf{x}'}
    \;\displaystyle{\Bigg\vert}\;
    \array{
      \mathscr{V} 
        &\xrightarrow{ \phi }& 
      \mathbf{f}^\ast \mathscr{V}' 
      & \in C_{\mathbf{x}}
      \\
      \mathbf{x} 
        &\xrightarrow{ \mathbf{f} }& 
      \mathbf{x}' 
      & \in \mathbf{D}
    }
  \Bigg\}
  \\
  &
  \Big\downarrow && \Big\downarrow
  \\
  &
  \mathcal{D}
  &
  \underoverset
    {\underset{R}{\longleftarrow}}
    {\overset{L}{\longrightarrow}}
    {\;\; \bot \;\;}
  &
  \mathbf{D}  
 }
$$
