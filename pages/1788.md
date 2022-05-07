
$\ldots$

\begin{tikzcd}
    &&
    &[-15pt]
    \frac{W \mathcal{G}}{\mathcal{G}}
    \times W\mathcal{G}
    \ar[
      dr,
      "\mathrm{pr}_1 \in \mathrm{W}"{description}
    ]
    &[-15pt]
    \\
    \frac{
      \mathclap{\phantom{\vert_a}}
      W \mathcal{G} \times \mathcal{G}_{\scalebox{.4}{ad}}
    }{
      \mathcal{G}
    }
    \ar[dd]
    \ar[rr]
    \ar[
      ddrr,
      phantom,
      "\mbox{\tiny\rm (pb)}"{pos=.14}
    ]
    &&
    \frac{
      \mathclap{\phantom{\vert_a}}
      W \mathcal{G} \times W\mathcal{G} \times \mathcal{G}_{\scalebox{.4}{ad}}
    }
    {
      \mathcal{G} \times \mathcal{G}
    }
    \ar[
      ur,
      "\sim"{sloped, below},
      "{
        \scalebox{.7}{$
        \!\!\!\!
        [\vec g, (\vec g',h)] \mapsto ([\vec g], h^{-1}\cdot \vec g')
        $}
      }"{sloped, above}
    ]
    \ar[
      dd,
      "\in \mathrm{Fib}"{right},
      "
       \frac{
         W(\mathcal{G} \times \mathcal{G})
         \times
         \left(
           \!\!\!\!\!\!
           \begin{array}{c}
             \mathcal{G}_{\scalebox{.4}{ad}}
             \\
             \downarrow
             \\
             \ast
           \end{array}
           \!\!\!\!\!\!
         \right)
       }{
         \mathclap{\phantom{\vert^{a}}}
         \mathcal{G} \times \mathcal{G}
       }
      "{left}
    ]
    &
    &
    \frac{
      W\mathcal{G}
    }
    {
     \mathcal{G}
    }
    \ar[
      ddll,
      "\mathrm{diag}"{right, xshift=4pt}
    ]
    \ar[
      ll,
      "\in \mathrm{W}"{below},
      "{
        [ \vec g, (\vec g, e) ]
        \raisebox{5pt}{\rotatebox{180}{$\mapsto$}}
        [\vec g]
      }"{above}
    ]
    \\
    \\
    \frac{
      W\mathcal{G}
    }{
      \mathcal{G}
    }
    \ar[
      rr,
      "\mathrm{diag}"{below}
    ]
    &&
    \frac{
      W \mathcal{G} \times W\mathcal{G}
    }{
      \mathcal{G} \times \mathcal{G}
    }
\end{tikzcd}
