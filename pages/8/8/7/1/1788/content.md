By assumption we have [[sections]] 
$$
  \array{
    \overline{f} \,\colon &  X 
      &\overset{\phantom{--}}{\hookrightarrow}& 
    X'
    &
    \text{with} 
    &
    f \circ \overline{f} \,=\, id
    \\
    \overline{g} \,\colon &  Y 
      &\overset{\phantom{--}}{\hookrightarrow}& 
   Y'
    &
    \text{with} 
    &
    g \circ \overline{g} \,=\, id
  }
$$
from which we obtain a candidate dashed morphism by setting
$$
  \phi \,\coloneqq\, r \circ (\overline{f} \times id) 
  \,,
$$
which clearly makes the top-right triangle commute
$$
  \begin{array}{l}
    \phi \circ (f \times id) 
    \\
    \;=\;
    r \circ (\overline{f} \times id)  \circ (f \times id) 
    \\
    \;=\;
    r
  \end{array}
$$
but also makes the other triangle commute
$$
  \begin{array}{l}
    \phi \circ (id \times g) 
    \\
    \;=\;
    \phi
      \circ 
    (id \times g) 
      \circ
    (f  \times id)
      \circ
    (\overline{f} \times id)
    \\
    \;=\;
    \phi
      \circ 
    (f \times id) 
      \circ
    (id  \times g)
      \circ
    (\overline{f}  \times id)
    \\
    \;=\;
    r
      \circ
    (id  \times g)
      \circ
    (\overline{f}  \times id)
    \\
    \;=\;
    s
      \circ
    (f  \times id)
      \circ
    (\overline{f}  \times id)
    \\
    \;=\;
    s
    \mathrlap{\,,}
  \end{array}
$$
and given any $\phi$ which makes the diagram commute, it must be of this form:
$$
  \begin{array}{l}
    \phi
    \\
    \;=\;
    \phi 
      \circ 
    (f \times id) 
      \circ 
    (\overline{f} \times id) 
    \\
    \;=\;
    r \circ (\overline{f} \times id) 
    \mathrlap{\,.}
  \end{array}
$$
