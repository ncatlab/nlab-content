
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
    f_P
    \,\colon\,
    \underset{ y \colon Y }{\prod}
    P\big(
      cpr(\hat{y})
    \big)
    \;;
    \;\;
    f^'_P
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
        f_P\big(
          f(x)
        \big)
      \Big)
      ,\,
        f^'_P\big(
          f^'(x)
        \big)
    \bigg)
    \end{array}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{\big(P,\, f_P,\,f^'_P\big)}
    \,\colon\,
    \underset{ 
      \hat{y} \,\colon\, Y \underset{X}{\sqcup} Y^' 
    }{\prod} 
    \,
    P(\hat{y})
  }
$$

\linebreak

**[[computation rule]]**

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
    f_P
    \,\colon\,
    \underset{ y \colon Y }{\prod}
    P\big(
      cpr^'(y)
    \big)
    \;;
    \;\;
    f^'_P
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
        f_P\big(
          f(x)
        \big)
      \Big)
      ,\,
        f^'_P\big(
          f^'(x)
        \big)
    \bigg)
    \end{array}
  }{
    \begin{array}{rlc}
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{\big(P,\, f_P,\,f^'_P\big)} \,\circ\,cpr
    &=&
    f_P
    \;;
    \\
    \mathclap{\phantom{\vert^{\vert}}}
    y^' \,\colon\, Y^'
    \;\vdash\;
    ind_{\big(P,\, f_P,\,f^'_P\big)} \,\circ\, cpr^'
    &=&
    f^'_P
    \;;
    \\
    happly_{\big(ind_{\big(P,\, f_P,\,f^'_P\big)}\big)}
    \,\circ\,
    homot
    &=&
    homot_P
    \end{array}
  }
$$

## References

* [[Egbert Rijke]], *Homotopy pushouts* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/pushout.pdf)&rbrack;, Lecture 13 in: *Introduction to Homotopy Type Theory*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;