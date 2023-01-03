
**[[type formation rule]]**

$$
  \frac{
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    \ast \,\colon\, Type
  }
$$

\linebreak


**[[term introduction rule]]**

$$
  \frac{
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    pt \,\colon\, \ast
  }
$$

\linebreak

**[[term elimination rule]]**

$$
  \frac{
    x \,\colon\, \ast
    \;\vdash\;\;
    D(x) \,:\, Type
    \;;
    \;\;\;
    pt_D \,\colon\, D(pt)
    \mathclap{\phantom{\vert_{\vert}}}
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{(D,\,pt_D)}
    \,\colon\,
    \underset{x \colon \ast}{\prod}
    D(x)
  }
$$

\linebreak

**[[computation rule]]**

$$
  ind_{(D,\,pt_D)}(pt)
  \;=\;
  pt_D
$$



