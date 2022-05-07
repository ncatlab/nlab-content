
\begin{tikzcd}
    \mathcal{S}_1
    \ar[
      rr,
      shift left=7pt,
      "{ \ell }"{above}
    ]
    &&
    \mathcal{S}_2
    \ar[
      ll,
      shift left=7pt,
      "{ r }"{below}
    ]
    \ar[
      ll,
      phantom,
      "{ \scalebox{.6}{$\bot$} }"
    ]
\end{tikzcd}

\begin{tikzcd}[column sep=large]
      \mathrm{PSh}(\mathcal{S}_1)
      \;\;
      \ar[
        rr,
        shift left=-7pt,
        "{ \ell_\ast \,\simeq\, r^\ast    }"{description}
      ]
      \ar[
        rr,
        shift left=32pt-7pt,
        "{ \ell_! }"{description, pos=.4}
      ]
      &&
      \;\;
      \mathrm{PSh}(\mathcal{S}_2)
      \ar[
        ll,
        shift right=16pt-7pt,
        "{ \ell^\ast \,\simeq\, r_! }"{description}
      ]
      \ar[
        ll,
        shift right=-16pt-7pt,
        "{ r_\ast }"{description, pos=.4}
      ]
      \ar[
        ll,
        phantom,
        shift right=8pt-7pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=24pt-7pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=-8pt-7pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
\end{tikzcd}


$$
  \begin{aligned}
      &
      \mathrm{PSh}(\mathcal{S}_1)
      \big(
        X_1
        ,\,
        r^\ast(X_2)
      \big)
      \\
      &
      \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_1)
      \Big(
         \underset{
           \underset{
             s_1 \to X_1
           }{\longrightarrow}
         }{\lim}
         \,
        y(s_1)
        \,
        ,\,
        r^\ast
        \big(
         \underset{
           \underset{
             s_2 \to X_2
           }{\longrightarrow}
         }{\lim}
         \,
        y(s_2)
        \big)
      \Big)
      \\
      &
      \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \mathrm{PSh}(\mathcal{S}_1)
      \Big(
        y(s_1)
        ,\,
         \underset{
           \underset{
             s_2 \to X_2
           }{\longrightarrow}
         }{\lim}
         \,
        r^\ast
        \big(
          y(s_2)
        \big)
      \Big)
      \\
      &
      \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \,
         \underset{
           \underset{
             s_2 \to X_2
           }{\longrightarrow}
         }{\lim}
      \mathrm{PSh}(\mathcal{S}_1)
      \Big(
        y(s_1)
        ,\,
        r^\ast
        \big(
          y(s_2)
        \big)
      \Big)
      \\
      & \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \;
      \underset{
        \underset{
          s_2 \to X_2
        }{\longrightarrow}
      }{\lim}
      \mathcal{S}_2
      \big(
        r(s_1)
        ,\,
        s_2
      \big)
      \\
      & \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \;
      \underset{
        \underset{
          s_2 \to X_2
        }{\longrightarrow}
      }{\lim}
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        y\big(r(s_1)\big)
        ,\,
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \underset{
        \underset{
          s_1 \to X_1
        }{\longleftarrow}
      }{\lim}
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        y\big(r(s_1)\big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        y\big(r(s_1)\big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        \mathcal{S}_2
        \big(
          (-)
          ,\,
          r(s_1)
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
      \mathrm{PSh}(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        \mathcal{S}_2
        \big(
          \ell(-)
          ,\,
          s_1
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
    PSh(\mathcal{S}_2)
      \Big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        \ell^\ast
        \big(
          y(s_1)
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
    PSh(\mathcal{S}_2)
      \Big(
        \ell^\ast
        \big(
        \underset{
          \underset{
            s_1 \to X_1
          }{\longrightarrow}
        }{\lim}
        y(s_1)
        \big)
        ,\,
        \underset{
          \underset{
            s_2 \to X_2
          }{\longrightarrow}
        }{\lim}
        y(s_2)
      \Big)
      \\
      & \;\simeq\;
    PSh(\mathcal{S}_2)
      \Big(
        \ell^\ast
        (
          X_1
        )
        ,\,
        X_2
      \Big)
  \end{aligned}
$$
