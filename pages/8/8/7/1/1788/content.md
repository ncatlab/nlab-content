

* [[Nicholas Wheeler]], *Generalized Quantum Measurement* (2012) &lbrack;[pdf](https://www.reed.edu/physics/faculty/wheeler/documents/Quantum%20Mechanics/Miscellaneous%20Essays/Generalized%20Quantum%20Measurement/Generalized%20Quantum%20Measurements.pdf), [[Wheeler-GeneralizedQuantumMeasurement.pdf:file]]&rbrack;



***

Bath coupling is quantum state transformation

Unitary evolution is quantum state and costate transformation


Partial trace is quantum costate transformation



$$
  \array{
    D 
    &=& 
    D
    \\
    \Big\downarrow\mathrlap{
      {}^{ ret^{\mathcal{E}}_{\mathcal{E}(D)} }
    }
    &&
    \Big\downarrow\mathrlap{
      {}^{ ret^{\mathcal{E}}_{\mathcal{E}'(D)} }
    }
    \\
    \mathcal{E}
    \mathcal{E}(D)
    &
    \overset{
      \mathcal{E}(tr_D)
    }{\longrightarrow}
    &
    \mathcal{E}
    \mathcal{E}'(D)
    &
    \overset{
      tr_{\mathcal{E}'(D)}
    }{\longrightarrow}
    &
    \mathcal{E}' 
    \mathcal{E}'(D)
    \\
    \Big\downarrow\mathrlap{ {}^{ join^{\mathcal{E}}_D } } 
    &&
    \Big\downarrow\mathrlap{ {}^{  
      tr^\ast 
      join^{\mathcal{E}'}_D
    } } 
    &&
    \Big\downarrow\mathrlap{ {}^{ join^{\mathcal{E}'}_D } }
    \\
    \mathcal{E}'(D)
    &
    \underset{
      \;\; tr_D \;\;
    }{\longrightarrow}
    &
    \mathcal{E}'(D)
    &=&
    \mathcal{E}'(D)
  }
$$

$$
  \array{
    \mathcal{E}' 
    &
    \xleftarrow{\;\;\;\;\;  tr \;\;\;\;\;}
    &
    \mathcal{E}
    \\
    \mathbf{C}^{\mathcal{E}}
    &
    \xrightarrow{\;\;\;\; tr^\ast \;\;\;\;}
    &
    \mathbf{C}^{ \mathcal{E}^' }
    \\
    \left(
      \array{
        \mathcal{E}'(D)
        \\
        \big\downarrow\mathrlap{ {}^{\rho'} }
        \\
        D
      }
    \right)
    &\mapsto&
    \left(
      \array{
        \mathcal{E}(D)
        &\overset{tr_D}{\to}&
        \mathcal{E}'(D)
        \\
        \big\downarrow
        \mathrlap{ {}^{
          tr^\ast\rho'
        } }
        &&
        \big\downarrow\mathrlap{ {}^{\rho'} }
        \\
        D
        &=&
        D
      }
    \right)
  }
$$
