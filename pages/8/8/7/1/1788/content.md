

**[[type formation rule]]**

$$
  \frac{
  }{
    Bit \,\colon\, Type
  }
$$

\linebreak

**[[term introduction rule]]**

$$
  \frac{ 
  }{
    0 \,\colon\, Bit
  }
  \;\;\;\;\;
  \frac{ 
  }{
    1 \,\colon\, Bit
  }
$$

\linebreak

**[[term elimination rule]]**

$$
  \frac{
    b \,\colon\, Bit \;\vdash\; P(b)
    ;\;
    \;\;
    0_P \,\colon\, P(0)
    ;\;
    \;\;
    1_P \,\colon\, P(1)
  }{
    ind_{(P,\,0_P,\,1_P)} 
      \,\colon\, 
    \underset{b \colon Bit}{\prod} P(b)
  }
$$

\linebreak

**[[computation rules]]**

$$
  \frac{
    b \,\colon\, Bit \;\vdash\; P(b)
    ;\;
    \;\;
    0_P \,\colon\, P(0)
    ;\;
    \;\;
    1_P \,\colon\, P(1)
  }{
    \begin{array}{l}
    ind_{(P,\,0_P,\,1_P)}(0) \;=\; 0_P
    ;\;
    \\
    ind_{(P,\,0_P,\,1_P)}(1) \;=\; 1_P
    \end{array}
  }
$$

\linebreak


\begin{tikzcd}[sep=40pt]
  &
  Y
  \ar[
    dr, 
    "{ \mathrm{cpr} }"{description, sloped}
  ]
  \ar[
    dd,
    Rightarrow,
    shorten=11pt,
    "{ \mathrm{homot} }"{description}
  ]
  \ar[
    rrrd,
    bend left=30,
    "{ \mathrm{cpr}_P }",
    "{\ }"{name=s, swap, pos=.55}
  ]
  \\[-20pt]
  X
  \ar[
    ur,
    "{ f }"
  ]
  \ar[
    dr,
    "{ f' }"{swap}
  ]
  && 
  Y \underset{X}{\sqcup} Y'
  \ar[ddr, equals, gray]
  \ar[
    rr, 
    dashed,
    "{ \mathrm{ind}_{(P,\, \cdots)} }"
  ]
  &&
  P
  \ar[ddl, gray, "{ \pi_P }"{description}]
  \\
  &
  Y'
  \ar[
    ur,
    shorten >=-6pt,
    "{ \mathrm{cpr}' }"{description, sloped}
  ]
  \ar[
    rrru,
    bend right=45,
    "{ \mathrm{cpr}_{P'} }"{swap, pos=.35},
    "{\ }"{name=t, pos=.4}
  ]
  \ar[
    from=s,
    to=t,
    shorten=8pt,
    Rightarrow,
    crossing over,
    "{\mathrm{homot_P}}"{description, pos=.7}
  ]
  \\[-100pt]
  && & 
  \color{gray}
  Y \underset{X}{\sqcup} Y'
\end{tikzcd}  



**[[type formation rule]]:**

$$
  \frac{
    \begin{array}{l}
    X,\, Y,\, Y^' \,\colon\, Type
    \;;
    \;\;
    f \,\colon\, X \to Y
    \;,
    \;\;
    f^' \,\colon\, X \to Y^'    
    \mathclap{\phantom{\vert_{\vert}}}
    \end{array}
  }
  {
    \mathclap{\phantom{\vert^{\vert}}}
    Y \underset{X}{\sqcup} Y^'
    \,\colon\,
    Type
  }
$$

\linebreak

**[[term introduction rules]]:**

$$
  \frac{
    y \,\colon\, Y^'
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    cpr(y)
    \,\colon\,
    Y \underset{X}{\sqcup} Y^'
  }
  \;\;\;\;\;\;\;\;\;
  \frac{
    y^' \,\colon\, Y^'
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    cpr^'(y^')
    \,\colon\,
    Y \underset{X}{\sqcup} Y^'
  }
  \;\;\;\;\;\;\;\;\;
  \frac{
    x \,\colon\, X
    \mathclap{\phantom{\vert}}
  }{
    \mathclap{\phantom{\vert^{\vert^{\vert}}}}
    homot(x)
    \,\colon\,
    Id_{\big(Y \underset{X}{\sqcup} Y^'\big)}
    \Big(
      cpr\big(f(x)\big)
      ,\,
      cpr^'\big(f^'(x)\big)      
    \Big)
  }
$$

\linebreak


**[[term elimination rule]]:**

$$
  \frac{
    \begin{array}{l}
    \hat{y}
      \,\colon\,
    Y \underset{X}{\sqcup} Y^'
    \;\vdash\;
    P(\hat{y})
    \,\colon\,
    Type
    \;;
    \\
    cpr_P
    \,\colon\,
    \underset{ y \colon Y }{\prod}
    P\big(
      cpr(\hat{y})
    \big)
    \;;
    \;\;
    cpr^'_P
    \,\colon\,
    \underset{ y^' \colon Y^' }{\prod}
    P\big(
      cpr^'(y^')
    \big)
    \;;
    \\
    homot_P
    \,\colon\,
    \underset{x \colon X}{\prod}
    Id_{P(x)}
    \bigg(
      homot(x)_\ast
      \Big(
        cpr_P\big(
          f(x)
        \big)
      \Big)
      ,\,
        cpr^'_P\big(
          f^'(x)
        \big)
    \bigg)
    \end{array}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{\big(P,\, cpr_P,\,cpr^'_P,\,homot_P\big)}
    \,\colon\,
    \underset{ 
      \hat{y} \,\colon\, Y \underset{X}{\sqcup} Y^' 
    }{\prod} 
    \,
    P(\hat{y})
  }
$$

\linebreak

**[[computation rules]]**

$$
  \frac{
    \begin{array}{l}
    \hat{y}
      \,\colon\,
    Y \underset{X}{\sqcup} Y^'
    \;\vdash\;
    P(\hat{y})
    \,\colon\,
    Type
    \;;
    \\
    cpr_P
    \,\colon\,
    \underset{ y \colon Y }{\prod}
    P\big(
      cpr^'(y)
    \big)
    \;;
    \;\;
    cpr^'_P
    \,\colon\,
    \underset{ y^' \colon Y^' }{\prod}
    P\big(
      cpr^'(y^')
    \big)
    \;;
    \\
    homot_P
    \,\colon\,
    \underset{x \colon X}{\prod}
    Id_{P(x)}
    \bigg(
      homot(x)_\ast
      \Big(
        cpr_P\big(
          f(x)
        \big)
      \Big)
      ,\,
        cpr^'_P\big(
          cpr^'(x)
        \big)
    \bigg)
    \end{array}
  }{
    \begin{array}{rlc}
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{\big(P,\, cpr_P,\,cpr^'_P,\,homot_P\big)}  
      \,\circ\,
    cpr
    &=&
    cpr_P
    \;;
    \\
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{\big(P,\, cpr_P,\,cpr^'_P,\,homot_P\big)} 
      \,\circ\, 
    cpr^'
    &=&
    cpr^'_P
    \;;
    \\
    happly_{\big(
      ind_{\big(P,\, cpr_P,\,cpr^'_P,\,homot_P\big)}
    \big)}
    \,\circ\,
    homot
    &=&
    homot_P
    \end{array}
  }
$$



