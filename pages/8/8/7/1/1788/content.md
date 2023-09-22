


* [[John Preskill]], *Generalized measurements*, Section 3.1.2 &lbrack;[pdf](http://theory.caltech.edu/~preskill/ph219/chap3_15.pdf#page=8)&rbrack; in: *Quantum Computation*, lecture notes, since 2004 &lbrack;[web](http://theory.caltech.edu/~preskill/ph229/)&rbrack;


* [[Stephen Barnett]], Chapter 4 of: *Quantum Information*, Oxford University Press (2009) &lbrack;[ISBN:9780198527633](https://global.oup.com/ukhe/product/quantum-information-9780198527633)&rbrack;



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
