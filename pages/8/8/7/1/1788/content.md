
$$
  \begin{array}{l}
    \nabla^X_{\partial_i}
    \mathrm{d}\phi(
      \partial_j
    )
    -
    \mathrm{d}\phi\big(
      \nabla^\Sigma_{\partial_i} \partial_j
    \big)
    \\
    \;=\;
    \partial_i 
    \partial_j \phi^l
    +
    L_{m}{}^l{}_n 
    (\partial_i \phi^m) (\partial_j \phi^n)
    -
    \Gamma_{i}{}^k{}_j \partial_k \phi^l
  \end{array}
$$

$$
  {&#8545;} \text{II}
$$

Given an immersion $\phi \colon \Sigma \xrightarrow{\;} X$,

Let $(v_a)_{a = 1}^{dim X}$ be a local Darboux frame of $X$, so that $(v_a)_{a =1}^{dim \Sigma}$ is a local frame on $\Sigma$, to be called the *tangential* frame vectors (the others being the *transversal* ones).

It follows for any $\sigma \in \Sigma$ inside the given chart that pushforward of vector field in this linear basis is just the canonical injection

\[
  \label{PushforwardOfDarbouxFrame}
  \begin{array}{rcc}
    \mathrm{d}\phi_\sigma 
      \;\colon\; 
    T_\sigma \Sigma
    &\xrightarrow{\phantom{--}}&
    T_{\phi(\sigma)} X
    \\
    v_a(\sigma) &\mapsto& v_a(\sigma)
    \mathrlap{\,.}
  \end{array}
\]

For tangential $b_1, b_2$ we set
\begin{equation}
  \label{PullbackOfConnection}
  \phi^\ast \Omega_{b_1}{}^a{}_{b_2}
  \;\equiv\;
  \begin{array}{ll}
    \omega_{b_1}{}^a{}_{b_2} & \text{tangential}\; a
    \\   
    \text{II}^a_{b_1 b_2} & \text{transversal}\; a
  \end{array}
\end{equation}

This makes it immediate that

$$
  \begin{array}{l}
    \nabla^X_{b_1} \mathrm{d}\phi(v_{b_2})
    -
    \mathrm{d}\phi\big( \nabla^\Sigma_{b_1} v_{b_2} \big)
    \\
    \;=\;
    \nabla^X_{b_1} v_{b_2} 
    -
    \nabla^\Sigma_{b_1} v_{b_2}
    \\
    \;=\;
    \phi^\ast \Omega_{b_1}{}^{a}{}_{b_2} v_a
    -
    \omega_{b_1}{}^a{}_{b_2} v_a
    \\
    \;=\;
    \text{II}^a_{b_1 b_2} v_a
  \end{array}
$$

$$
  (\partial_{a_1} e^r_{a_2}) v_{r}
  +
  \Omega_{a_1}{}^{a'_2}{}_{a_2} V_{a'_2}
  -
  (\partial_{a_1} e^r_{a_2}) v_{r}
  -
  \Omega_{a_1}{}^{a'_2}{}_{a_2} v_{a'_2}
  \;\;
  =
  \;\;
  \text{II}^{a'_2}_{a_1 a_2} V_{a'_2}
$$



consider coordinate charts 

$$
  \big(x^r\big)_{r = 1}^{dim\Sigma}
  \,,
  \;\;\;\;
  \big(X^r\big)_{r = 1}^{dim X}
$$

$$
  \begin{array}{l}
    \phi^\ast 
    \big(
      \Omega_{b_1}{}^a{}_{b_2}
      E^{b_1} \otimes E^{b_2}
    \big)
    \\
    \;=\;
    \Big(
      \Omega_{b_1}{}^a{}_{b_2}
      \big(
        \mathrm{d}x^{r_1} 
        (\partial_{r_1} \phi^{r'_1})
        E^{b_1}_{r'_1}
      \big) 
        \otimes 
      \big(
        \mathrm{d}x^{r_2} 
        (\partial_{r_2} \phi^{r'_2})
        E^{b_2}_{r'_2}
      \big) 
    \Big)
  \end{array}
$$

$$
  \mathrm{d}\phi(v_a) = v_a
$$



$$
  \begin{array}{l}
    \mathrm{d} \phi^\ast E^a
    -
    \phi^\ast \Omega^a{}_{b_2} \phi^\ast E^{b_2}
    \\
    \;=\;
    \left\{
    \begin{array}{ll}
      \mathrm{d} e^a - \omega^a{}_{a'} e^{a'}
      &
      \text{tangential}\;a
      \\
      - \text{II}^a_{b_1 b_2} e^{b_1} \, e^{b_2}
      &
      \text{transversal}\;a
    \end{array}
    \right.
  \end{array}
$$

$$
  \Gamma_{r}{}^s{}_{t}
  \;=\;
  e_a^s \Omega_{r}{}^a{}_b e^b_t
  +
  e^s_a \partial_r e^a_t
$$

$$
  \big(
    e^{r'_1}_{b_1}
    \partial_{r'_1} \phi^{r_1}
  \big)
  \Omega_{r_1}{}^a{}_{b_2}
  \big(
    e^{b_2}_{r'_2} \partial_{r_2} \phi^{r'_2} 
  \big)
  \;=\;
  \big(
    e^{r'}_{b_1}
    \partial_{r'} \phi^r
  \big)
  \big(
    E^a_s \Gamma_r{}^s{}_t E^t_b
    +
    E^a_s \partial_r E^s_b  
  \big)
$$

$$
  \mathrm{d}e^a \;=\; \omega^a{}_{a'} e^{a'}
  \;\;\;
  \Leftrightarrow
  \;\;\;
  (\partial_s e^a_r) \mathrm{d}x^s \mathrm{d}x^r
  \;=\;
  (\omega_{s}{}^a{}_b e^b_r) \mathrm{d}x^s \mathrm{d}x^r
$$


$$
  E^a \;=\;
  E^a_r \mathrm{d}X^r
$$
$$
  \phi^\ast E^a
  \;=\;
  \mathrm{d}x^s  (\partial_s \phi^r) E^a_r
$$

$$
  \mathrm{d} \phi^\ast E^a
  \;=\;
  \mathrm{d}x^{s_1}
  \mathrm{d}x^{s_2}
  \Big(
    \big(
      \partial_{s^1} \partial_{s^2} \phi^r
    \big)
    E^a_r
    \,+\,
    (\partial_{s_2} \phi^{r'}) 
    (\partial_{s_1} E^a_{r'})
  \Big)
$$


$$
  \begin{array}{l}
    e^{r_1}_{b_1}\nabla_{r_1}
    \big(e^{r_2}_{b_2} \partial_{r_2} \phi^a\big)
    \\
    \;=\;
    e^{r_1}_{b_1}\partial_{r_1}
    \big(e^{r_2}_{b_2} \partial_{r_2} \phi^a\big)    
    -
    e^{r_1}_{b_1}
    \omega_{r_1}{}^{b'_2}{}_{b_2}
    \big(e^{r_2}_{b'_2} \partial_{r_2} \phi^a\big)    
    +
    e^{r_1}_{b_1}
    \Omega_{r_1}{}^{a}{}_{a'}
    \big(e^{r_2}_{b'_2} \partial_{r_2} \phi^{a'}\big)    
  \end{array}
$$


