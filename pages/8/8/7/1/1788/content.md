$$
  \begin{aligned}
    & T(V_1, \cdots, V_v, V_{v+1})
    \\
    & =
    T( T(V_1, \cdots ,V_v),  V_{v+1} )
    \\
    &=
    prod
      \circ
    \exp\left(
      \left\langle
        \hbar \Delta_F, 
        \frac{\delta}{\delta \mathbf{\Phi}} 
          \otimes 
        \frac{\delta}{\delta \mathbf{\Phi}}
      \right\rangle
    \right)
    \left(
    \left(
      prod
        \circ
      \!\!\!\!
      \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v}}}{\sum}
      \underset{ { r \lt s } \atop { \in \{1, \cdots, v\} }  }{\prod}
      \frac{1}{e_{r,s}!}
      \left\langle
          (\hbar \Delta_F)^{e_{r,s}}
          \,,\,
          \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
          \frac{\delta^{e_{r,s}}}{ \delta \mathbf{\Phi}_s^{e_{r,s}} }
      \right\rangle
      (V_1 \otimes \cdots \otimes V_v)
    \right)
      \,\otimes\,
    V_{v+1}
    \right)
    \\
    & =
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v+1}}}{\sum}
    \\
    & \phantom{=}
      \underset{ {  r \lt s } \atop {  \in \{1,\cdots, v\}}  }{\prod}
      \frac{1}{e_{r,s}!}
    \left\langle
        (\hbar \Delta_F)^{e_{r,s}}
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{ \delta \mathbf{\Phi}_s^{e_{r,s}} }
    \right\rangle
    \\
    & \phantom{=}
    \underset{  
       { e_{v+1} =} 
       \atop
       { e_{1,{v+1}} + \cdots + e_{v,v+1} } 
    }{\sum}
      \underset{
        = (e_{1,v+1}) \cdots (e_{v,v+1}))
      }{
      \underbrace{
      \frac{ 
        \left(
          { e_{v+1} }
          \atop
          { (e_{1,v+1}), \cdots, (e_{v,v+1}) }
        \right) 
      }{
        ( e_{v+1} ) !
      }
      }
      }
    \left\langle
      (\hbar \Delta_F)^{e_{v+1}}
    \left(
      \frac{\delta^{e_{1,v+1}} V_1 }{\delta \mathbf{\Phi}^{e_{1,v+1}}}
        \otimes
        \cdots
        \otimes
      \frac{ 
        \delta^{e_{v,v+1}} V_v
      }{ 
        \delta \mathbf{\Phi}^{e_{v,v+1}} 
      }
    \;\otimes\;
    \frac{
      \delta^{ e_{v+1} } V_{v+1}
    }{
      \delta \mathbf{\Phi}^{e_{1,v+1} + \cdots + e_{v,v+1}}
    }
    \right\rangle
    \right)
    \\
    &=
    prod
      \circ
    \underset{\Gamma \in \mathcal{G}_{(V_j)_{j = 1}^{v+1}}}{\sum}
    \underset{ { r \lt s } \atop { \in \{1, \cdots, v+1\} } }{\prod}
    \tfrac{1}{e_{r,s}!}
    \left\langle
        (\hbar \Delta_F)^{e_{r,s}}
        \,,\,
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_r^{e_{r,s}}}
        \frac{\delta^{e_{r,s}}}{\delta \mathbf{\Phi}_s^{e_{r,s}}}
    \right\rangle
    (V_1 \otimes \cdots \otimes V_{v+1})
  \end{aligned}
$$
