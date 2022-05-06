

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

[[!redirects Theory of flat functors]]
[[!redirects theory of continuous flat functors]]
[[!redirects theory of J-continuous flat functors]]


## Idea

The **theory of J-continuous flat functors** on a [[site]] $(\mathcal{C},J)$, or more concisely the theory of flat functors on $\mathcal{C}$, is the [[geometric theory]] $\mathbb{T}_J^{\mathcal{C}}$ whose models in a Grothendieck topos $\mathcal{E}$ correpond precisely to J-continuous flat functors $\mathcal{C}\to\mathcal{E}$ and, by well known representation theorems, to [[geometric morphisms]] $\mathcal{E}\to Sh(\mathcal{C},J)$ whence $\mathbb{T}_J^{\mathcal{C}}$ provides a uniform albeit (in general) uneconomical axiomatization of the [[geometric theory]] classified by $Sh(\mathcal{C},J)$.

## Definition

Let $(\mathcal{C},J)$ be a small site. The **theory of J-continuous flat functors** is given by the following geometric theory $\mathbb{T}_J^{\mathcal{C}}$ over the signature $\Sigma$ which has sorts (symbols) $\lceil A\rceil$ for every object $A$ of $\mathcal{C}$ and function symbols $\lceil f\rceil :\lceil A\rceil\to\lceil B\rceil$ for every function $f:A\to B$:

* axioms $\top\vdash_x \lceil f\rceil(x)=x$ for all identity morphisms $f$.

* axioms $\top_x\lceil f\rceil(x)=\lceil h(\lceil g\rceil (x))$ for all triples $f,g,h$ with $f=g\circ h$.

* an axiom $\top\vdash\Bigvee_{A\in\mathcal{C}} \exists x:A \top$.

* axioms $\top_{x:A,y:B}\Bigvee_{A\overset{f}{\leftarrow} C\overset{g}{\rightarrow B}}\exists z:C(\lceil f\rceil (z:C)=x:A\wedge \lceil g\rceil (z:C)=y:B)$ where the disjunction ranges over all cones on the discrete digram consisting of $a$ and $B$.

## Examples

* Let $(\emptyset,\emptyset)$ be the empty site. Then the signature $\Sigma$ is empty and only the third condition takes hold, yielding $\mathbb{T}_\emptyset^{\emptyset}=\{\top\vdash\bot$ i.e. the empty topos $Sh(\emptyset,\emptyset)=\mathbb{1}$ classifies the **inconsistent theory** whose models are precisely the [[initial objects]].


## Related entries

* [[flat functor]]

* [[geometric theory]]

* [[Diaconescu's theorem]]

* [[theory of objects]]

## References

* [[Olivia Caramello]], _Lattices of theories_ , arXiv:0905.0299 (2009). ([abstract](https://arxiv.org/abs/0905.0299), p.11)

* [[Olivia Caramello]], _Theories, Sites, Toposes_ , Oxford UP 2018. (p.58f)

* [[Peter Johnstone]], _Sketches of an Elephant vol.II_ , Oxford UP 2002. (p.897)

The code

      [[topos]] [[topos]]

gets rendered as:

[[topos]] [[topos]]

\linebreak

\linebreak


***


\linebreak

\linebreak

$$
  star_4 d \star_4 
  \left[
    \array{
      V^{(0)}
      \\
      V^{(1)}
      \\
      V^{(2)}
      \\
      V^{(3)}
      \\
      V^{(4)}
    }
  \right]
  \;\;=\;\;
  \left[
  \array{
    - 1/2 & 0 & 1/\sqrt{2} & 0 & 0 & 0 & 0
    \\
    0 & - 3/2 & 0 & \sqrt{3/2} & 0 & 0 & 0
    \\
    1/\sqrt{2} & 0 & - 5/2 & 0 & \sqrt{3} & 0 & 0
    \\
    0 & \sqrt{3} & 0 & - 7/2 & 0 & \sqrt{5} & 0
    \\
    0 & 0 & \sqrt{3} & 0 & -9/2 & 0 & \sqrt{15/2}
  }
  \right]
  \;\cdot\;
  \left[
    \array{
      V^{(0)}
      \\
      V^{(1)}
      \\
      V^{(2)}
      \\
      V^{(3)}
      \\
      V^{(4)}
    }
  \right]
$$

\linebreak

$$
  \begin{aligned}
  &
  d
  \star
  d (A_\mu)
  \;+\;
  d
  \star 
  \big(
    \overline{L}
    \!\cdot\!
    \gamma_\mu 
    \!\!\cdot\!
    d L
  \big)
  \\
  & 
  =
  \cdots
  +
  \partial_\nu
  \big(
    \overline{L}
    \!\cdot\!
    \gamma_\mu 
    \!\!\cdot\!
    \partial^\nu L  
  \big)
  \\
  & =
  \big(
    \overline{
      L
    }
    \!\cdot\!
    \gamma_\mu 
    \!\!\cdot\!
    \partial_\nu
    \partial^\nu L  
  \big)
  \end{aligned}
$$


$$
  \begin{aligned}
  d 
  \big( 
    \overline{L} \!\cdot\! \gamma_\mu \!\!\!\cdot\! L \, d x^\mu
  \big)
  & =\;
  \big(
    \overline{\partial_\nu L} 
    \!\cdot\! 
    \gamma_\mu \!\!\!\cdot\! L 
    +
    \overline{L} 
    \!\cdot\! 
    \gamma_\mu \!\!\!\cdot\! \partial_\nu L 
  \big)
  d x^\nu
  \wedge
  d x^\mu
  \\
  & 
  \big(
    \overline{\partial_\nu L} 
    \!\cdot\! 
    \gamma_\mu \!\!\!\cdot\! L 
    -
    \overline{\partial_\nu L} 
    \!\cdot\! 
    \gamma_\mu \!\!\!\cdot\! L 
  \big)
  d x^\nu
  \wedge
  d x^\mu
  \end{aligned}
$$


Consider the 5d metric

$$
  g
  \;=\;
  H^{+1} \, \eta_{\mu \nu} d x^\mu \otimes d x^\nu 
    + 
  H^{-1} d z \otimes d z
$$

for $H$ a [[smooth function]] of $z$.

Notice

$$
  \sqrt{
    \left\vert
      det (g_{\kappa_1 \kappa_2})
    \right\vert
  }
  \;=\;
  H^{3/2}
$$

Consider 

$$
  A
  \in 
  \Omega^1(\mathbb{R}^{3,1})
  \overset{i^\ast}{\longrightarrow}
  \Omega^1(\mathbb{R}^{4,1})
$$

a 1-form pulled back from 4d, and in Lorenz gauge ($d \star A = 0$). Then the [[Laplace-Beltrami-operator]] on $A$ is given by

$$
  \begin{aligned}
    \big( 
      \star d \star \pm d \star d \star 
    \big) 
    d A
    \;=\;
    H^{-2} \eta^{\mu \nu}\partial_\mu \partial_\nu A
    +
    H^{-3/2}
    \partial_z
    \left(
      H^{3/2} \partial_z A
    \right)
  \end{aligned}
  \,.
$$

Proof:

First notice the general formula, akin to that of the Laplace-Beltrami operator on functions:

$$
  \begin{aligned}
    \star d \star d A
    & =
    \star d \star (\partial_{j_1} f) A_{j_2} d x^{j_1} \wedge d x^{j_2}
    \\
    & = 
    \star d
    \left( 
      \tfrac{1}{ 2 \color{green}  (D-2)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
      \,
      \epsilon_{
        i_1 i_2
        {\color{green} k_3 \cdots k_{D} }
      }
      d x^{
        \color{green} k_3
      } 
      \wedge \cdots \wedge 
      d x^{
        \color{green} k_{D}
      }
    \right)
    \\
    & =
    \star
    \partial_{ \color{magenta} k_2}
    \left( 
      \tfrac{1}{ 2 \color{green} (D-2)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{ i_1 j_1 } 
      g^{ i_2 j_2 } 
      (\partial_{j_1} A_{j_2} )
      \,
      \epsilon_{
        i_1 i_2
        {\color{green} k_3 \cdots k_{D} }
      }
      d x^{ \color{magenta} k_2 }
      \wedge 
      d x^{
        \color{green} k_3
      } \wedge \cdots \wedge 
      d x^{
        \color{green} k_{D}
      }
    \right)
    \\
    & =
    \sqrt{
      \left\vert
        det\big( (g_{i j}) \big)
      \right\vert
    }
    \underset{
      = 
      \det\big( (g_{i j})^{-1}  \big)
      \tfrac{1}{2}
      \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    }{
    \underbrace{
    \tfrac{
      (-1)^{D-1}
    }{ 
       { \color{orange} (D-1)! }
       2 { \color{green} (D-2)! }
    }
    \epsilon_{ 
      l_1
      { \color{orange} l_2 \cdots l_{D} }
    }
    g^{ 
      { \color{orange} l_1 }
      { \color{magenta} k_1  } 
    }
    g^{ 
      { \color{orange} l_2 }
      { \color{magenta} k_2  } 
    }
    g^{ 
      { \color{orange} l_3 }
      { \color{green} k_3  } 
    }
    \cdots
    g^{ 
      { \color{orange} l_D} 
      { \color{green} k_D } 
    }
    \epsilon_{
      i_1 i_2
      {\color{green} k_3 \cdots k_{D} }
    }
    }
    }
    \,
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \, 
    g_{ {\color{magenta} k_1} r }
    d x^{ \color{magenta} r  }
    \\
    & =
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} k_1 } r }
    d x^{  r }
  \end{aligned}
$$

Now specialize to the the case at hand, where 

1. $A = A_\mu d x^{\mu} A_z d^z $ 

1. $A_z = 0$

1. $\partial_\mu \eta^{\mu \nu} A_\nu = 0$ 

1. $g_{\mu \nu} = H \eta_{\mu \nu}$

1. $\partial_\mu H = 0$

$$
  \begin{aligned}
    & 
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} k_1 } r }
    d x^{  r }
    \\
    & =
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} \mu_1 \mu_2 }_{i_1 i_2}
    \partial_{ \color{magenta} \mu_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} \mu_1 } r }
    d x^{  r }
    \\
    & \phantom{=}\;
    +
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} \mu_1 z }_{i_1 i_2}
    \partial_{ \color{magenta} z }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} \mu_1 } r }
    d x^{  r }
    \\
    & \phantom{=}\;
    +
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} z \mu_2 }_{i_1 i_2}
    \partial_{ \color{magenta} \mu_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} z } r }
    d x^{  r }
    \\
    & =
    \tfrac{
      (-1)^{D-1}
    }{2}
    H^{-2}
    \big(
      \underset{
        = 0
      }{
      \underbrace{
      \partial_{\mu_2}
      \partial_{\mu_1}
      A^{\mu_2}
      }
      }
    \big)
    H^1
    d x^{\mu_1}
    -
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-2}
    \big(
      \partial_{\mu_2}
      \partial^{\mu_2}
    A^{\mu_1}
    \big)
    H^1
    d x^{\mu_1}
    \\
    & \phantom{=}\;
    -
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-3/2}
    \partial_z
    \left( 
      H^{3/2}
      \partial_{z}
      A_{\mu_1}
    \right)
    H^1
    d x^{\mu_1}
    \\
    & \phantom{=}\;
    +
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-3/2}
    \underset{
      = 0
    }{
    \underbrace{
    \partial_{\mu_2}
    \left( 
      H^{3/2}
      \partial_z
      A^{\mu_2}
    \right)
    }
    }
    H^{-1} d z
  \end{aligned}
$$

$$
  \begin{aligned}
    \star d \star d A
    & =\;
    H^{-3/2} 
    \partial_\mu 
    \left(
      H^{3/2} H^{-1-1} \eta^{\mu \nu} \partial_\nu A
    \right)
    +
    H^{-3/2}
    \partial_z
    \left(
      H^{3/2} H^{1-1} \partial_z A
    \right)
    \\
    & =
    H^{-2} \eta^{\mu \nu}\partial_\mu \partial_\nu f
    +
    H^{-3/2}
    \partial_z
    \left(
      H^{3/2} \partial_z A
    \right)
  \end{aligned}
$$

and hence

$$
  \begin{aligned}
    & 
    \; \star d \star d A \;=\; 0
    \\
    \Leftrightarrow
    &
    \;
    \eta^{\mu \nu}\partial_\mu \partial_\nu A
    +
    H^{+1/2}
    \partial_z
    \left(
      H^{3/2} \partial_z A
    \right)
  \end{aligned}
$$

\linebreak

$$
    \eta^{\mu \nu}\partial_\mu \partial_\nu \partial_z f
    +
    \tfrac{5}{2}
    \tfrac{1}{2}(H^2)''
    \partial_z f
    +
    (H^2 + \tfrac{1}{2}(H^2)') \partial^2_z f
$$


\linebreak

$$
  d B + Tr(d \pi \wedge d \pi \wedge d \pi)
  \;=\;
  \star_{5} F
$$

$$
  \star_5
  d \star_5 F 
  =
  \star_5
  Tr(d \pi \wedge d \pi \wedge d \pi) h' d x^4
$$

$$
  d \star_5 
  \big( 
    F + \omega \wedge d x^4
  \big)  
$$

$$
  d \star_4 F \wedge d x^4
  \;=\;
  d \big( \pi \wedge d \pi \wedge d \pi _\big) \wedge d x^4
$$

$$
  d A \wedge d x^5
  +
  d \omega \wedge d x^5
  + 
  d \rho^0 \wedge d x^5
  +
  B \wedge d x^4
  + 
  \pi \wedge d \pi \wedge d \pi \wedge d x^4
$$

$$
  \star_4
  (d A + d \omega + d \rho^0)
  = 
   B + \pi \wedge d \pi \wedge d \pi
$$

$$
  \star_4 d \star_4 F 
  = 
  - \star_4 d \star_4 d (\omega + \rho^0)
  +
  d B + d \pi \wedge d \pi \wedge d \pi
$$



\linebreak


\linebreak

\linebreak
  
\linebreak

***


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

[[tphyahoo]]