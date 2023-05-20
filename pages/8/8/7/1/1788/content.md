
\begin{example}
\label{PushoutProductOfSplitEpimorphisms}
  Assuming the [[axiom of choice]], the pushout-product in [[Set]] of two [[surjections]] 
$$
  \array{
    f \,\colon &  X 
      &\overset{\phantom{--}}{\twoheadrightarrow}& 
    X'
    \\
    g \,\colon &  Y 
      &\overset{\phantom{--}}{\twoheadrightarrow}& 
   Y'
  }
$$
is always an [[isomorphism]], in that the following [[commuting square]] is already a [[pushout]]
$$
  \array{
    X \times Y
      &\overset{id \times g}{\longrightarrow}&
    X \times Y'
    \\
    \mathllap{{}^{f \times id}}
    \Big\downarrow 
      && 
    \Big\downarrow
    \mathrlap{{}^{ f \times id}}
    \\
    X' \times Y
      &\underset{id \times g}{\longrightarrow}&
    X' \times Y'
  }
$$

Because, consider any other [[cocone]] under the given [[span]], such as shown in the outer part of the following diagram:
\begin{tikzcd}[sep=30pt]
  X \times Y
  \ar[dd, "{ f \times \mathrm{id} }"{description}]
  \ar[rr, "{ \mathrm{id} \times g }"{description}]
  &&
  X \times Y'
  \ar[dd, "{ f \times \mathrm{id} }"{description}]
  \ar[dddr, bend left=20, "{ r }"{description}]
  \\
  \\
  X' \times Y
  \ar[rr, "{ \mathrm{id} \times g }"{description}]
  \ar[drrr, bend right=20, "{ s }"{description}]
  &&
  X' \times Y'
  \ar[dr, dashed, "{ \phi }"{description}]
  \\
  && & 
  Z
\end{tikzcd}
then the dashed lift exists uniquely as follows:

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
from which we obtain a candidate dashed morphism 
$$
  \begin{array}{l}
    \mathllap{
      \phi \; \coloneqq \;
    }
    r
      \circ
    (\overline{f} \times id)
    \\
    \;=\;
    r
      \circ
    (\overline{f} \times id)
      \circ
    (id \times g)
      \circ
    (id \times \overline{g})
    \\
    \;=\;
    r
      \circ
    (id \times g)
      \circ
    (\overline{f} \times id)
      \circ
    (id \times \overline{g})
    \\
    \;=\;
    s
      \circ
    (f \times id)
      \circ
    (\overline{f} \times id)
      \circ
    (id \times \overline{g})
    \\
    \;=\;
    s
      \circ
    (id \times \overline{g})
  \end{array}
$$
which we see makes the bottom triangle commute
$$
  \begin{array}{l}
    \phi 
      \circ
    (id \times g)
    \\
    \;=\;
    r
      \circ
    (\overline{f} \times id)
      \circ
    (id \times g)
    \\
    \;=\;
    r
      \circ
    (id \times g)
      \circ
    (\overline{f} \times id)
    \\
    \;=\;
    s
      \circ
    (f \times id)
      \circ
    (\overline{f} \times id)
    \\
    \;=\;
    s
  \end{array}
$$
and analogously for the right triangle
$$
  \begin{array}{l}
    \phi 
      \circ
    (f \times id)
    \\
    \;=\;
    s
      \circ
    (id \times \overline{g})
      \circ
    (f \times id)
    \\
    \;=\;
    s
      \circ
    (f \times id)
      \circ
    (id \times \overline{g})
    \\
    \;=\;
    r
      \circ
    (id \times g)
      \circ
    (id \times \overline{g})
    \\
    \;=\;
    r
    \,.
  \end{array}
$$
Finally, this $\phi$ is unique, for given any $\phi$ making the diagram commute, we have
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
    r
      \circ
    (\overline{f} \times id)
    \,.
  \end{array}
$$
\end{example}
Of course, the same argument shows that any pushout-product of [[split epimorphisms]] is an isomorphism.


