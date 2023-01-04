
**[[type formation rule]]**

$$
  \frac{
     X \,\colon\, Type
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    [X]_n \,\colon\, Type
  }
$$

\linebreak


**[[term introduction rule]]**

$$
  \frac{
    x \,\colon\, X
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    \eta_X(x) \,\colon\, [X]_n
  }
  \;\;\;\;\;\;\;\;\;
  \frac{
    \phi \,\colon\, S^{n+1} \to [X]_n
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    hub_X^{\phi} \,\colon\, [X]_n
  }
  \;\;\;\;\;\;\;\;\;
  \frac{
    \phi \,\colon\, S^{n+1} \to [X]_n  
    \;;
    \;\;\;
    s \,\colon\, S^{n+1}
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    hmt_X^{\phi}(s) 
     \,\colon\, 
    Id_{[X]_n}\big(
      \phi(s)
      ,\,
      hub_X^{\phi}
    \big)
  }
$$

\linebreak

**[[term elimination rule]]**

$$
  \frac{
    \begin{array}{l}
      \overline{x} \,\colon\, [X]_n
      \;\vdash\;
      D(\overline{x}) \,\colon\, Type \;;
      \\
      x \,\colon\, X
      \;\vdash\;
      \eta_D(x) \,\colon\, D\big( \eta_X(x) \big)
      \;;
      \\
      \phi \,\colon\, S^{n+1} \to [X]_n
      \,,
      \;
      \phi_D 
        \,\colon\, 
      \underset{s \,\colon\,S^{n+1}}{\prod}
      \,
      D\big( \phi(s) \big)
      \;\;\vdash\;\;
      hub^{\phi_D}_D 
       \,\colon\,
      D\big( hub_X^\phi \big)
      \;;
      \\
      \phi \,\colon\, S^{n+1} \to [X]_n
      \,,
      \;
      \phi_D 
        \,\colon\, 
      \underset{s \,\colon\,S^{n+1}}{\prod}
      \,
      D\big( \phi(s) \big)
      \,,
      \;
      s \,\colon\, S^{n+1}
      \;\;\vdash\;\;
      hmt_D^{\phi_D}(s)
        \,\colon\, 
      Id_{D\big(hub_X^{\phi}\big)}\Big(
        \big(hmt^{\phi}_X(s)\big)_\ast
        \phi_D(s)
        ,\,
        hub_D^{\phi_D}
      \Big)
      \mathclap{\phantom{\vert^{\vert^{\vert}}}}
    \end{array}
  }{
    \mathclap{\phantom{\vert^{\vert_{\vert}}}}
    ind_{\big(D,\,\eta_D,\, hub_D,\, hmt_D \big)}
    \,\colon\,
    \underset{\overline{x}\colon [X]_n}{\prod}
    \,
    D(\overline{x})
  }
$$

\linebreak

**[[computation rule]]**

$$
  \cdots
$$



