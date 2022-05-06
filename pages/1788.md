
$$
  \left(
    \array{
      \mathbb{H}
      \\
      \mathbb{H}
    }
  \right) 
$$


$$
  \left(
    \array{
      0 & j
      \\
      -j & 0
    }
  \right)
$$


$$
  j 
  \cdot
  (a + j \cdot b)
  \;=\;
  (- b + j \cdot a)
  \;=\;
  \left( 
    \array{
      0 & 1
      \\
      -1 & 0
    }
  \right)
$$

$$
  k
  \cdot
  (a + j \cdot b)
  \;=\;
  (- i \cdot b - j \cdot i a)
  \;=\;
  \left( 
    \array{
      0 & -i
      \\
      -i & 0
    }
  \right)
$$

$$
  \left( 
    \array{
      0 & 1
      \\
      -1 & 0
    }
  \right)
  \cdot
  \left( 
    \array{
      (x_0 + x_1) & q
      \\
      \overline{q} & (x_0  - x_1)
    }
  \right)
  =
  \left( 
    \array{
      \overline{q} & (x_0 - x_1)
      \\
      -(x_0 + x_1) & - q
    }
  \right)
$$


$$
  \left( 
    \array{
      (x_0 + x_1) & q
      \\
      \overline{q} & (x_0  - x_1)
    }
  \right)
  \cdot
  \left( 
    \array{
      0 & 1
      \\
      -1 & 0
    }
  \right)
  =
  \left( 
    \array{
      -q & (x_0 + x_1)
      \\
      -(x_0 - x_1) & \overline{q}
    }
  \right)
$$

\linebreak

The 6d spinors in $\mathbb{H}^2$ decompose as pairs of 4d spinors under

$$
  \mathbb{H}
  \;\simeq_{\mathbb{R}}\;
  \mathbb{C} \oplus \mathbb{C} j
  \,.
$$

What's the residual action of $SU(2)_R$ on these? The one generated from $\mathbf{\Gamma}_6 \mathbf{\Gamma}_7$?

The corresponding octonionic matrix is

$$
  \mathbf{\Gamma}_6 \mathbf{\Gamma}_7
  \;=\;
  \left( 
    \array{
      0 & L_{e_4}
      \\
      - L_{e_4} & 0
    }
  \right)
  \left( 
    \array{
      0 & L_{e_5}
      \\
      - L_{e_5} & 0
    }
  \right)
  \;=\;
  - L_{e_4} L_{e_5}  
$$

Now we compute from the octonionic multiplication table


$$
  L_{e_4} L_{e_6} 1
  \;=\;
  j
$$

$$
  L_{e_4} L_{e_6} i
  \;=\;
  k = i j
$$

$$
  L_{e_4} L_{e_6} j
  \;=\;
  - 1
$$

$$
  L_{e_4} L_{e_6} k
  \;=\;
  - i
$$





\linebreak

\linebreak


If I understand well what you're after, you want to show that a ultracategory is just a $T$-algebra for a suitable monad.

My claim is that the monad acts as follows on objects:

$$ T : \mathcal{A} \mapsto \int^X \beta(X)\times \mathcal{A}^X $$ 

I am basing this conjecture on the fact that an ultracategory consists of maps

$$ i_X : \beta(X)\times \mathcal{A}^X \to \mathcal{A} $$ 

that if this conjecture is correct amount exactly to a functor $T\mathcal{A} \to \mathcal{A}$ (by the universal property of the coend, the $i_X$ forming a cowedge in $X$).

Of course, strictly speaking $T$ does not exist, because as $X$ ranges over all sets the coend I'm taking is on too large a diagram. I kindly ask you to set aside size issues and follow a bit of coend-nonsense: so, just for today $T$ exists and defines a functor.

1. First, the initial cowedge $i_X : \beta(X) \times \mathcal{A}^X \to TA$ has a component at $X=1$, the terminal category; this gives $T$ the structure of a pointed functor (of course, $i$ depends naturally on $\mathcal{A}$).

2. A candidate multiplication map $TT\mathcal{A} \to T\mathcal{A}$ can be obtained as follows:

$$\begin{array}{rl} 
TT\mathcal{A} &= \displaystyle \int^Y \beta(Y) \times T\mathcal{A}^Y \\
&\displaystyle  = \int^Y \beta(Y) \times \left( \int^X \beta(X)\times \mathcal{A}^X \right)^Y \\
&\displaystyle \to \int^Y\int^X \beta(Y) \times  \beta(X)^Y \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta(Y) \times  \beta\beta(X)^{\beta Y} \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta\beta(X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta (X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \text{colim}_Y\int^X \beta (X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \cong \int^X \beta (X) \times \mathcal{A}^{X}
\end{array}$$