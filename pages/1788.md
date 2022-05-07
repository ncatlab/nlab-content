

$$
  \mathbb{Z}
  \colon
  sSet
  \rightleftarrows
  sAb
  \colon
  frgt
$$

$$
  N
  \colon
  sAb
  \rightleftarrows
  Ch_+
  \colon
  DK
$$

\linebreak

$$
  \begin{aligned}
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
    &
    \;\simeq\;   
    sSet
    \big(
      S \times \Delta[\bullet],
      \,
      frgt \circ DK(V)
    \big)
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S \times \Delta[\bullet]),
      \,
      V
    \big)    
    \\
    & \;\xrightarrow{EZ_S}\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S) 
      \,\otimes\,
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      V
    \big)    
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      [
        N \circ \mathbb{Z}(S),
        \,
        V
      ]
    \big)    
    \\
    & \;\simeq\;
    \Big(
    frgt \circ DK
    \big(
      [
        N \circ \mathbb{Z}(S),
        \,
        V
      ]
    \big)
    \Big)_\bullet
  \end{aligned}
$$


$$
  \begin{aligned}
    \Big(
      frgt \circ DK
      \big(
        [
          N \circ \mathbb{Z}(S),
          \,
          V
        ]
      \big)
    \Big)_\bullet
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      [
        N \circ \mathbb{Z}(S),
        \,
        V
      ]
    \big)    
    \\
    & \;\simeq\;
    Ch_+
    \big(
      N \circ \mathbb{Z}(S) 
      \,\otimes\,
      N \circ \mathbb{Z}(\Delta[\bullet]),
      \,
      V
    \big)    
    \\
    & \xrightarrow{AW_S}
    Ch_+
    \big(
      N \circ \mathbb{Z}(S \times \Delta[\bullet]),
      \,
      V
    \big)    
    \\  
    & \;\simeq\;
    sSet
    \big(
      S \times \Delta[\bullet],
      \,
      frgt \circ DK(V)
    \big)
    \\
    & \;\simeq\;
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
  \end{aligned}
$$

$$
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
    \xrightarrow{\;EZ_S\;}
      \Big(
      frgt \circ DK
      \big(
        [
          N \circ \mathbb{Z}(S),
          \,
          V
        ]
      \big)
    \Big)_\bullet
    \xrightarrow{\;AW_S\;}
    \big[
      S, 
      \,
      frgt \circ DK(V)
    \big]_\bullet
$$



