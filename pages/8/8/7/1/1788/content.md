
* face maps are given by:

   \[
      \label{FaceMapsOfbarWG}
      \begin{aligned}
      &
      d_i
      \big(
        g_{n-1}, \cdots, g_0
      \big)
      \\
      &
      \;\coloneqq\;
      \left\{
      \array{
        \big(
          g_{n - 2}, 
          \,
          \cdots,
          \,
          g_0
        \big)
        & \text{if} &
        i = 0
        \\
        \big(
          d_{i-1}(g_{n-1}),
          \,
          \cdots
          ,\,
          d_0(g_{n-i}) \cdot g_{n-i-1},
          \,
          g_{n -  i - 2}, 
          \,
          \cdots,
          \,
          g_0
        \big)
        & \text{if} &
        0 \lt i \lt n
        \\
        \big(
          d_{n-1}(g_{n-1}),
          \,
          \cdots,
          \,
          d_1(g_1)
        \big)
        & \text{if} &
        i = n
      }
      \right.
      \end{aligned}
    \]

* degeneracy maps:

  \[
    \label{DegeneracyMapsOfbarWG}
    \begin{aligned}
    &
    s_i(g_{n-1}, \cdots, g_0)
    \\
    &
    \;\coloneqq\;
    \left\{
    \array{
    \big(
      e,
      \,
      g_{n-1},
      \,
      \cdots,
      \,
      g_0
    \big)
    & \text{if} &
    i = 0
    \\
    \big(
      s_{i - 1}(g_{n-1}),
      \,
      \cdots,
      \,
      s_0(g_{n-i}),
      \,
      e,
      \,
      g_{n-i-1},
      \,
      \cdots,
      \,
      g_0
    \big)
    & \text{if} &
    i \gt 0
    }
    \right.
    \end{aligned}
  \]

