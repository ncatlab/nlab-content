
The inductive [[inference rules]] for the [[empty type]]:


**[[type formation rule]]:**

$$
  \frac{
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    \varnothing \,\colon\, Type
  }
$$

\linebreak


**[[term introduction rule]]:**

$$
\text{--- none ---}
$$

\linebreak

**[[term elimination rule]]:**

$$
  \frac{
    x \,\colon\, \varnothing
    \;\vdash\;\;
    D(x) \,:\, Type
  }{
    \mathclap{\phantom{\vert^{\vert}}}
    ind_{(D)}
    \,\colon\,
    \underset{x \colon \varnothing}{\prod}
    D(x)
  }
$$

\linebreak

**[[computation rule]]:**

$$
\text{--- none ---}
$$


