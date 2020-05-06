
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

(..)

## Definition

+-- {: .num_defn }  
###### Definition
**([[Laplace-Beltrami operator]])**

Given a [[Riemannian manifold]] $(X,g)$, the _[[Laplace-Beltrami operator]]_ $\Delta$ is the [[differential operator]]  on the space of [[smooth functions]]  $f \in C^\infty(X) = \Omega^0(X)$ given by the formula

\[
  \label{LaplaceOperatorViaHodgeDeRhamCalculus}
  \Delta f
  \;\coloneqq\;
  \star d \star d f
  \,,
\]

where

* $d \;\colon\; \Omega^\bullet(X) \to \Omega^{\bullet + 1}(X)$ is the [[de Rham differential]] (depending only on the [[smooth manifold]] $X$, not on the [[metric tensor]]);

* $\star \;\colon\; \Omega^\bullet(X) \to \Omega^{dim(X)-\bullet}(X)$ is the [[Hodge star operator]] of $(X,g)$ (this is where the dependence on the [[metric tensor]] enters).

The same formula makes sense more generally for [[pseudo-Riemannian manifolds]]. Even so, in the pseudo-Riemannian case one tends to speak of the _[[wave operator]]_ instead of the Laplace operator, and to use the symbol $\Box$ instead of $\Delta$ (at least for flat [[pseudo-Riemannian manifolds]]: [[Minkowski spacetime]]).

=--

+-- {: .num_prop #LaplaceOperatorInComponents}  
###### Proposition
**([[coordinate]]-expression of [[Laplace operator]])**

If $U \subset X$ is a [[chart]] of $X$ with [[coordinate functions]] $\{x^i \colon U \to \mathbb{R}\}$, then the Laplace operator (eq:LaplaceOperatorViaHodgeDeRhamCalculus) is equivalently given by the following component-expression:

$$
  \Delta f_{\vert U}
  \;=\;
  \frac{ 
     sgn(g)
  }{
    \sqrt{
      \left\vert
        det\big( (g_{i j})  \big)
      \right\vert
    }
  }
  \partial_i
  \left( 
    \sqrt{
      \left\vert
        det\big( (g_{i j})  \big)
      \right\vert
    }
    g^{i j}    
    \partial_j 
    f
  \right)
  \,,
$$

=--

Here:

* $sgn(g)$ is the [[signature of a quadratic form|signature]] of the [[metric tensor]], hence 

  * $sgn(g) = +1$ for [[Riemannian manifolds]],

  * $sgn(g) = -1$ for [[pseudo-Riemannian manifolds]];

* $\partial_i \coloneqq \frac{\partial}{\partial x^i}$ denotes the [[partial derivative]] by the coordinate $x^i$;

* $(g_{i j})$ is the [[square matrix]] of components of the [[metric tensor]] $g$ in the given [[coordinate chart]], hence such that

  $$
    g 
    \;=\;
    g_{i j}
    d x^i \otimes d x^j
  $$

* $det\big( (g_{i j}) \big)$ is the [[determinant]] of this [[matrix]], 

  $\left\vert det\big( (g_{i j}) \big)\right\vert$ its [[absolute value]] (taking this is irrelevant for [[Riemannian manifolds]] but necessary for [[pseudo-Riemannian manifolds]], where the determinan of the metric is negative),

  $\sqrt{\left\vert det\big( (g_{i j}) \big)\right\vert}$ is the [[positive number|positive]] [[square root]] of that;

* $(g^{i j})$ is the corresponding [[inverse matrix]];

* the [[Einstein summation convention]] is used throughout, meaing that a [[sum]] over repeated indices is understood.

+-- {: .proof}
###### Proof

Using 

1. the component formula for the [[de Rham differential]] $d = d x^i \partial_i$, 

1. the component formula for the [[Hodge star operator]] (see [there](Hodge+star+operator#eq:ComponentFormulaForHodgeStar))

we compute as follows:

$$
  \begin{aligned}
    \star d \star d f
    & =
    \star d \star (\partial_j f) d x^j
    \\
    & = 
    \star d
    \left( 
      \tfrac{1}{ \color{green} (D-1)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{ i  j} (\partial_j f)
      \,
      \epsilon_{
        i
        {\color{green} k_2 \cdots k_{D} }
      }
      d x^{
        \color{green} k_2
      } 
      \wedge \cdots \wedge 
      d x^{
        \color{green} k_{D}
      }
    \right)
    \\
    & =
    \star
    \partial_{ \color{magenta} k_1}
    \left( 
      \tfrac{1}{ \color{green} (D-1)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{i j} (\partial_j f)
      \,
      \epsilon_{
        i 
        {\color{green} k_2 \cdots k_{D} }
      }
      d x^{ \color{magenta} k_1 }
      \wedge 
      d x^{
        \color{green} k_2
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
      \delta^{ \color{magenta} k_1 }_i
    }{
    \underbrace{
    \tfrac{1}{ 
       { \color{orange} D! }
       { \color{green} (D-1)! }
    }
    \epsilon_{ 
      \color{orange} l_1 l_2 \cdots l_D 
    }
    g^{ 
      { \color{orange} l_1 }
      { \color{magenta} k_1  } 
    }
    g^{ 
      { \color{orange} l_2 }
      { \color{green} k_2  } 
    }
    \cdots
    g^{ 
      { \color{orange} l_D} 
      { \color{green} k_D } 
    }
    \epsilon_{
      i
      {\color{green} k_2 \cdots k_{D} }
    }
    }
    }
    \,
    \partial_{ \color{magenta} k_1 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{i j} (\partial_j f)
    \right)    
    \\
    & =
    \frac{1}{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \delta^{ \color{magenta} k_1 }_i
    \partial_{ \color{magenta} k_1 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{i j} (\partial_j f)
    \right)    
    \\
    & =
    \frac{  
      sgn(g)
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \partial_{i}
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{i j} (\partial_j f)
    \right)    
  \end{aligned}
$$


=--

## Properties

### Functional determinant and Analytic torsion

The [[functional determinant]] of Laplace operator on a given space of [[differential p-forms]] appears as factor of the _[[analytic torsion]]_ of the given [[Riemannian manifold]].

## Related entries

* [[heat kernel]]

* [[harmonic form]], [[Hodge theory]]

* [[hearing the shape of a drum]]

* [[BV-Laplacian]]

## References


Textbook accounts:

* [[Nicole Berline]], [[Ezra Getzler]], [[Michele Vergne]], _Heat kernels and Dirac operators_, Grundlehren __298__, Springer 1992, "Text Edition" 2003. 


See also:

* Wikipedia, _[Laplace operator](https://en.wikipedia.org/wiki/Laplace_operator)_, _[Laplace-Beltrami operator](https://en.wikipedia.org/wiki/Laplace%E2%80%93Beltrami_operator)_

* MathOverflow: [why-is-the-laplacian-ubiquitous](http://mathoverflow.net/questions/54986/why-is-the-laplacian-ubiquitous)

[[!redirects Laplacian]]
[[!redirects Laplace operators]]

[[!redirects Laplace-Beltrami operator]]
[[!redirects Laplace-Beltrami operators]]

[[!redirects generalized Laplace operator]]
[[!redirects generalized Laplace operators]]

