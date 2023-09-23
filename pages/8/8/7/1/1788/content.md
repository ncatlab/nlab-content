
\begin{definition}
\label{MonadTransformer}
  Given monads $\mathcal{E}$, $\mathcal{E}'$ on the same [[category]] $\mathbf{C}$, a *monad transformer* between them is:

* a [[natural transformation]] of the [[underlying]] [[functors]]

  $trans \,\colon\, \mathcal{E} \to \mathcal{E}'$

which

1. preserves the return-operations, in that

   $$
     trans \circ ret^{\mathcal{E}}
     \;=\;
     ret^{\mathcal{E}'}
   $$

1. preserves the bind-operations, in that for
   $prog_{12}\,\colon\, D_1 \to \mathcal{E}(D_2)$
   and
   $prog_{23}\,\colon\, D_2 \to \mathcal{E}(D_3)$
   
   we have

   \[
     \label{RespectForBindOperation}
     trans_{D_3}
     \circ
     \Big(
       \big( bind^{\mathcal{E}} prog_{23} \big)
       \circ
       prog_{12}
     \Big)
     \;\;=\;\;
     bind^{\mathcal{E}'}
     \Big(
       \big(
         trans_{D_3} \circ prog_{23}
       \big)
     \Big)
     \circ
     \big(
       trans_{D_2} \circ prog_{12}
     \big)
   \] 

\end{definition}

\begin{proposition}
  A natural transformation $trans \,\colon\, \mathcal{E} \to \mathcal{E}'$ is a monad transformer in the sense of Def. \ref{MonadTransformer} iff it is a homomorphism of monads (in the original sense of [Maranda 1966](monad#Maranda66)) in that, besides respecting the [[unit of a monad|unit/return-operation]] also respects the join-operation ("monad multiplication") in that it makes the following [[commuting diagram|diagrams commute]]:

\begin{tikzcd}[sep=large]
  \mathcal{E}\big(\mathcal{E}(\mbox{-})\big)
  \ar[
     rr,
     "{
       \mathrm{trans}_{{}_{\mathcal{E}(\mbox{-})}}
     }"{description}
  ]
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}}_{(\mbox{-})}
    }"{description}
  ]
  &&
  \mathcal{E}\big(\mathcal{E}'(\text{-})\big)
  \ar[
    rr,
    "{
      \mathcal{E}'(\mathrm{trans}_{(\mbox{-})})
    }"{description}
  ]
  &&
  \mathcal{E}'\big(\mathcal{E}'(\text{-})\big)
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}'}_{(\mbox{-})}
    }"{description}
  ]
  \\
  \\
  \mathcal{E}(\mbox{-})
  \ar[
    rrrr,
    "{ 
       \mathrm{trans}_{(\mbox{-})} 
    }"{description}
  ]
  &&&&
  \mathcal{E}'(\mbox{-})
\end{tikzcd}

\end{proposition}
\begin{proof}
Recall that the relation between the bind- and join-operations is:

$$
  bind^{\mathcal{E}} \big( f \,\colon\, D_1 \to \mathcal{E}(D_2) \big)
  \;\equiv\;
  join^{\mathcal{E}}_{D_2} \circ \mathcal{E}(f)
$$

and 

$$
  join^{\mathcal{E}}_{D}
  \;\equiv\;
  bind^{\mathcal{E}}\big( id_{\mathcal{E}(D)} \big)
  \,.
$$


Now in one direction: If the above square commutes then consider its [[pasting diagram]] with the [[naturality square]] of $trans$ as follows


\begin{tikzcd}
  D_1
  \ar[
    rr,
    "{ 
      \mathrm{prog}_{12} 
    }"{description}
  ]
  &&
  \mathcal{E}(D_2)
  \ar[
     rr,
     "{
       \mathrm{trans}_{D_2}
     }"{description}
  ]
  \ar[
    dd,
    "{
      \mathcal{E}(\mathrm{prog}_{23})
    }"{description}
  ]
  &&
  \mathcal{E}'(D_2)
  \ar[
    dd,
    "{
      \mathcal{E}'(\mathrm{prog}_{23})
    }"{description}
  ]
  \\
  \\
  &&
  \mathcal{E}\big(\mathcal{E}(D_3)\big)
  \ar[
     rr,
     "{
       \mathrm{trans}_{{}_{\mathcal{E}(D_3)}}
     }"{description}
  ]
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}}_{D_3}
    }"{description}
  ]
  &&
  \mathcal{E}'\big(\mathcal{E}(D_3)\big)
  \ar[
    rr,
    "{
      \mathcal{E}'(\mathrm{trans}_{D_3})
    }"{description}
  ]
  &&
  \mathcal{E}'\big(\mathcal{E}'(D_3)\big)
  \ar[
    dd,
    "{
      \mathrm{join}^{\mathcal{E}'}_{D_3}
    }"{description}
  ]
  \\
  \\
  &&
  \mathcal{E}(D_3)
  \ar[
    rrrr,
    "{ 
       \mathrm{trans}_{D_3} 
    }"{description}
  ]
  &&&&
  \mathcal{E}'(D_3)
\end{tikzcd}

Going diagonally through this [[commuting diagram]]: The total left and bottom composite is the left hand side of (eq:RespectForBindOperation) and the total top and right composite is the right hand side of (eq:RespectForBindOperation), thus proving their equality.

In the other direction, if (eq:RespectForBindOperation) holds then its restriction to $prog_{12} \,=\, id \,=\, prog_{23}$ yields the above commtuting diagram.

\end{proof}


****

* [[John Preskill]], *Generalized measurements*, Section 3.1.2 &lbrack;[pdf](http://theory.caltech.edu/~preskill/ph219/chap3_15.pdf#page=8)&rbrack; in: *Quantum Computation*, lecture notes, since 2004 &lbrack;[web](http://theory.caltech.edu/~preskill/ph229/)&rbrack;


* [[Stephen Barnett]], Chapter 4 of: *Quantum Information*, Oxford University Press (2009) &lbrack;[ISBN:9780198527633](https://global.oup.com/ukhe/product/quantum-information-9780198527633)&rbrack;



* [[Nicholas Wheeler]], *Generalized Quantum Measurement* (2012) &lbrack;[pdf](https://www.reed.edu/physics/faculty/wheeler/documents/Quantum%20Mechanics/Miscellaneous%20Essays/Generalized%20Quantum%20Measurement/Generalized%20Quantum%20Measurements.pdf), [[Wheeler-GeneralizedQuantumMeasurement.pdf:file]]&rbrack;



***
Monad transformation property ensures that mixed composition of transformations with Kleisli morphisms is unambiguous.


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
