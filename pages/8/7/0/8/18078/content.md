
$$
  \gamma_\Omega
  \;=\;
  \left(
    \array{
      0_{16} & 1_{16}
      \\
      -1_{16} & 0_{16}
    }
  \right)
$$

$$
  (\gamma_\Omega)^{-1}
  \;=\;
  \gamma_\Omega
$$

$$
  \gamma_{1}
  \;=\;
  
  diag
  \big(
    \array{
      1_8, & i_{8}, & -1_{8}, & -i_{8}
    }
  \big)
$$

$$
  (\gamma_{\Omega})^{-1}
  \gamma_1
  (\gamma_{\Omega})
  \;=\;
  \gamma_1
$$

$$
  (\gamma_{\Omega})^{-1}
  (A)^{T}
  (\gamma_{\Omega})
  \;=\;
  -A
$$

$$
  \begin{aligned}
    (\gamma_\Omega A)^T
    & =
    (A)^T (\gamma_\Omega)^T
    \\
    & =
    -
    (A)^T (\gamma_\Omega)
    \\
    & =
    (\gamma_\Omega) (A)
  \end{aligned}
$$

\linebreak

$$
  e_{b_1 b_2}
  \;=\;
  F_{a [b_1} \delta_{b_2]}^5 \, d x^a
  +
  \tfrac{1}{3!}
  \epsilon_{b_1 b_2 b_3 a_1 a_2} F^{a_1 a_2} d x^{b_3}
$$

$$
  \,
$$

$$
  \begin{aligned}
    & 
    \Big(
    \underset{
      \mathclap{
        0 \leq a_i \leq 5 
      }
    }{\sum}
    e_{a_1}{}^{a_2} \wedge e_{a_2}{}^{a_3} \wedge e_{a_3}{}^{a_1}
    \Big)
    \wedge 
    \Big(
    F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}
    \Big)
    \\
    & =
    \Big(
    3
    \underset{
      \mathclap{
        0 \leq a_i \leq 4 
      }
    }{\sum}
    e_{a_1 5} \wedge e_{a_3 5} \wedge e^{a_1 a_3}
    +
    \underset{
      \mathclap{
        0 \leq a_i \leq 4 
      }
    }{\sum}
    e_{a_1 a_2} 
     \wedge 
    e^{a_2 a_3} 
     \wedge e_{a_3}{}^{a_1}    
    \Big)
    \wedge 
    \Big(
    F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}
    \Big)
    \\   
    & =
    \phantom{+}\;
    \tfrac{1}{2}
    F_{a_1 b_1} d x^{a_1}
     \wedge 
    F_{a_2 b_2} d x^{a_2}
      \wedge 
    g_{a_3 b_3}  d x^{a_3}
    \epsilon^{b_1 b_2 b_3 c_1 c_2} F_{c_1 c_2} 
      \wedge 
    F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}
    \\
    & \phantom{=}\; + 
    \epsilon^{b_1}{}_{b_2 c_1 c_2 c_3 }
    \delta^{b_1}_{[b_2}
    \delta^{a_1}_{a'_1}
    \delta^{a_2}_{a'_2}
    \delta^{a_3}_{a'_3]}
    F^{a'_1 a'_2} d x^{a'_3}
    F^{c_1 c_2} d x^{c_3}
    F_{a_1 a_2} g_{a_4 a_3} d x^{a_4}
      \wedge 
    F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}    
    \\
    & =
    \phantom{+}\;
    \tfrac{1}{2}
    F_{a_1 b_1} d x^{a_1}
     \wedge 
    F_{a_2 c_2} d x^{a_2}
      \wedge 
    g_{a_3 b_3}  d x^{a_3}
    \epsilon^{b_1 b_2 b_3 c_1 c_2} F_{c_1 b_2} 
      \wedge 
    F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}
    \;+\;
    \cdots
  \end{aligned}
$$


\linebreak


$$
  \begin{aligned}
    & 
    \Big(
      \underset{
        \mathclap{
          0 \leq a_i \leq 5 
        }
      }{\sum}
      e_{a_1}{}^{a_2} \wedge e_{a_2}{}^{a_3} \wedge e_{a_3}{}^{a_1}
    \Big)
    \wedge 
    \Big(
      F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}
    \Big)
    \\
    & =
    \Big(
    3
    \underset{
      \mathclap{
        0 \leq a_i \leq 4 
      }
    }{\sum}
    e_{a_1 5} \wedge e_{a_3 5} \wedge e^{a_1 a_3}
    +
    \underset{
      \mathclap{
        0 \leq a_i \leq 4 
      }
    }{\sum}
    e_{a_1 a_2} 
     \wedge 
    e^{a_2 a_3} 
     \wedge e_{a_3}{}^{a_1}    
    \Big)
    \wedge 
    \Big(
      F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}
    \Big)
    \\   
    & =
    \tfrac{1}{2}
    F_{a_1 b_1} d x^{a_1}
     \wedge 
    F_{a_2 b_2} d x^{a_2}
      \wedge 
    g_{a_3 b_3}  d x^{a_3}
    \epsilon^{b_1 b_2 b_3 c_1 c_2} F_{c_1 c_2} 
      \wedge 
    F_{a_4 b_4} d x^{a_4} \wedge d x^{b_4}
    \\  
    & =
    \tfrac{1}{2}
    \epsilon^{b_1 b_2 b_3 c_1 c_2} 
    F_{a_1 b_1} 
    F_{a_2 b_2} 
    g_{a_3 b_3} 
    F_{c_1 c_2} 
    F_{d_1 d_2} 
    \epsilon^{a_1 a_2 a_3 d_1 d_2}
    \cdot
    \mathrm{dvol}
    \;+\;
    \cdots
  \end{aligned}
$$

\linebreak

$$
  \begin{aligned}
    & \phantom{= +}\,
    \epsilon^{a_1 a_2 a_3 d_1 d_2} 
    \big(
      F_{a_1 b_1} 
      F_{a_2 b_2}
      g_{a_3 b_3}
      F_{c_1 c_2}
      F_{d_1 d_2}
    \big)
    \epsilon^{b_1 b_2 b_3 c_1 c_2}
    \\
    & =
    -
    \epsilon^{a_1 a_2 a_3 d_1 d_2} 
    \big(
      F_{a_1 b_1} 
      F_{a_2 c_2}
      g_{a_3 b_3}
      F_{c_1 b_2}
      F_{d_1 d_2}
    \big)
    \epsilon^{b_1 b_2 b_3 c_1 c_2}
    \\
    & =
    +
    \epsilon^{a_1 a_2 a_3 d_1 d_2} 
    \big(
      F_{a_1 b_1} 
      F_{d_1 c_2}
      g_{a_3 b_3}
      F_{c_1 b_2}
      F_{a_2 d_2}
    \big)
    \epsilon^{b_1 b_2 b_3 c_1 c_2}
  \end{aligned}
$$
