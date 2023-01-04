

\begin{tikzcd}
  X
  \ar[
    d,
    "{ \eta }"
  ]
  \ar[
    rr,
    equals
  ]
  &[-130pt]
  &[-10pt]
  X
  \ar[
    d,
    "{ \eta_D }"
  ]
  &[-130pt]
  \\
  {
    [X]_n
  }
  \ar[ddd, equals]
  \ar[
    rr, 
    dashed,
    shift left=2pt,
    "{ 
       \mathrm{ind}_{
         (D,\, \eta_D,\, \mathrm{hub}_D,\, \mathrm{hmt}_D)
    } }"{description}
  ]
  &[-70pt]
  &[-10pt]
  D
  \ar[dddll]
  \\
  &[-70pt]
  &[-10pt]
  &[-70pt]
  \mathrm{Map}\big({S^{n+1}},\,{D}\big)
  \ar[
    ul,
    "{ \mathrm{hub}_D}"{sloped},
    "{\ }"{name=t2}
  ]
  &[+70pt]
  \\[+10pt]
  &&
  \mathrm{Map}\big({S^{n+1}},\,{D}\big) \times S^{n+1}
  \ar[
    ur,
    "{ \mathrm{pr}_1 }"{description}
  ]
  \ar[dddll]
  \ar[
    uu,
    bend left=50,
    gray,
    "{ \mathrm{ev} }"{pos=.6},
    "{\ }"{pos=.7, swap, name=s2}
  ]
  \\[-80pt]
  {
    [X]_n
  }
  \\
  & 
  \mathrm{Map}\big({S^{n+1}},\,{[X]_n}\big)
  \ar[
    ul,
    "{ \mathrm{hub}}"{sloped},
    "{\ }"{name=t}
  ]
  \ar[
    from=uuurr,
    shorten <=-6pt,
    crossing over
  ]
  \\[+10pt]
  \mathrm{Map}\big({S^{n+1}},\,{[X]_n}\big) \times S^{n+1}
  \ar[
    ur,
    "{ \mathrm{pr}_1 }"{description}
  ]
  \ar[
    uu,
    bend left=40,
    "{ \mathrm{ev} }"{pos=.6},
    "{\ }"{pos=.7, swap, name=s}
  ]
  \ar[
    from=s,
    to=t,
    Rightarrow,
    "{ \mathrm{hmt} }"{yshift=1pt,sloped},
  ]
  \ar[
    from=s2,
    to=t2,
    Rightarrow,
    gray,
    "{ \mathrm{hmt}_D }"{yshift=1pt,sloped},
  ]
\end{tikzcd}



**[[type formation rule]]:**

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


**[[term introduction rules]]:**

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

**[[term elimination rule]]:**

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

**[[computation rule]]:**

$$
  ind_{\big(D,\,\eta_D,\, hub_D,\, hmt_D \big)}
  \big(
    \eta(x)
  \big)
  \;=\;
  \eta_D(x)
$$



