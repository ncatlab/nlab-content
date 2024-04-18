
...


$$
  \array{
    &&&& 
   \big[ 
     (\Gamma, x \colon A, y \colon B(x))
   \big]
    \\
    &&&&
    \Big\downarrow
    \mathrlap{
      {}^{
        \big[
          \Gamma, 
          x \colon A \,\vdash\, B(x) \colon Type
        \big]
      }
    }
    \\
    [\Gamma] 
    &&
    \overset{
       [\Gamma \vdash a \colon A]
     }
     {\longrightarrow}
   &&
     \big[
       (\Gamma, x \colon A)
    \big]
    \\
    & {}_{id}\searrow 
      && 
    \swarrow_{\mathrlap{[\Gamma \vdash A \colon Type]}}
    \\
    && 
    [\Gamma]
  }
$$
