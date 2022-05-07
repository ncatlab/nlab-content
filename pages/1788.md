
### Orientations of Euclidean space

  An ordinary *orientation* of a
  differentiable manifold $Y$ is
  traditionally defined to be the choice of a volume form
  (a nowhere vanishing top degree differential form)
  up to pointwise positive rescaling.
  Assuming that $Y$ is closed, hence compact,
  we may equivalently remember just the class of this
  form in de Rham cohomology, up to positive rescaling:
  
\begin{xymatrix@C=3em}
      \mathrm{vol}_Y
      \;\in\;
      \underset{
        \raisebox{-3pt}{
          \tiny
          \color{blue}
          \bf
          \begin{tabular}{c}
            differential
            forms
          \end{tabular}
        }
      }{
        \Omega_{\mathrm{dR}}^{\mathrm{dim}(Y)}(Y)
      }
      \ar[rr]
        _-{
          \;[-]\;
        }
        ^-{
          \mathclap{
          \mbox{
            \tiny
            \color{olive}
            \bf
            \begin{tabular}{c}
              pass to total volume
            \end{tabular}
          }
          }
        }
      &&
      \underset{
        \mathclap{
        \raisebox{-3pt}{
          \tiny
          \color{blue}
          \bf
          de Rham cohomology
        }
        }
      }{
        H_{\mathrm{dR}}^{\mathrm{dim}(Y)}(Y)
      }
\end{xymatrix}

  If $Y$ were already oriented otherwise, we could ask that
  $[\mathrm{vol}_Y]$ be rescaled to
  a *[[unit]]* $\pm 1 \,\in\, \mathbb{Z} \subset \mathbb{R}$,
  {\it with respect to} the
  reference orientation. That number $\pm 1 \in \mathbb{Z}$ would
  be the choice of *relative orientation*.
  But since we want to
  define that reference orientation in the first place,
  the normalization demand on it is, conversely, that it be
  **(a)** integral and **(b)** minimally so, such that
  any other integral class is a unique integral multiple.
  This means to demand that


**(a)** the orienting volume class lifts to integral cohomology:
\begin{xymatrix@C=2em}
    \underset{
      \mathclap{
      \raisebox{-3pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          integral
          \\
          volume class
        \end{tabular}
      }
      }
    }{
      [\mathrm{vol}_Y]
    }
    \;\in\;
      \underset{
        \mathclap{
        \raisebox{-2pt}{
          \tiny
          \color{blue}
          \bf
          integral cohomology
        }
        }
      }{
        H^{\mathrm{dim}(Y)}
        \big(
          Y; \mathbb{Z}
        \big)
      }
      \ar[rr]^-{
        \mbox{
          \tiny
          \color{olive}
          \bf
          \begin{tabular}{c}
            extension
            \\
            of scalars
          \end{tabular}
        }
      }
      &&
      \underset{
        \mathclap{
        \raisebox{-2pt}{
          \tiny
          \color{blue}
          \bf
          real cohomology
        }
        }
      }{
        H^{\mathrm{dim}(Y)}
        \big(
          Y; \mathbb{R}
        \big)
      }
      \ar[rr]
        ^-{
          \mbox{
            \tiny
            \color{olive}
            \bf
            \begin{tabular}{c}
              de Rham
              \\
              theorem
            \end{tabular}
          }
        }
      _-{
        \simeq
      }
      &&
      \underset{
        \mathclap{
        \raisebox{-2pt}{
          \tiny
          \color{blue}
          \bf
          de Rham cohomology
        }
        }
      }{
        H_{\mathrm{dR}}^{\mathrm{dim}(Y)}
        \big(
          Y
        \big)
      }
\end{xymatrix}

**(b)** every other integral cohomology $n$-class of $Y$ is obtained
  by external cup product of $[\mathrm{vol}_Y]$ with
  an integral class on the point:

\begin{xymatrix}
    \underset{
      \mathclap{
      \raisebox{-3pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          top
          integral
          cohomology
        \end{tabular}
      }
      }
    }{
      H^{\mathrm{dim}(Y)}\big(Y;\, \mathbb{Z}\big)
    }
     \;\simeq\;
    \underset{
      \mathclap{
      \raisebox{-3pt}{
        \tiny
        \color{blue}
        \bf
        \begin{tabular}{c}
          generated
          \\
          under
          cupping
        \end{tabular}
      }
      }
    }{
      H^0\big(\ast;\, \mathbb{Z}\big)
    }
    \big\langle
      \underset{
        \mathrlap{
        \;
        \raisebox{-3pt}{
          \tiny
          \color{blue}
          \bf
          \begin{tabular}{c}
            from normalized
            \\
            volume class
          \end{tabular}
        }
        }
      }{
        [\mathrm{vol}_Y]
      }
    \big\rangle
    \;\;
    \in
    \;
    H^0\big(\ast;\, \mathbb{Z}\big)
    \,
    \mathrm{Modules}.
  \;
\end{xymatrix}

  If $Y$ is not compact, we apply this logic to
  those volume forms that *[[vanishing at infinity|vanish at infinity]]* on $Y$
  -- their classes are naturally
  identified with classes as above,
  defined on the one-point compactification space
  $X \coloneqq Y^{\mathrm{cpt}}$.


