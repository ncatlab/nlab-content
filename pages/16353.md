
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

On a [[smooth manifold]] $X$ the smooth [[tangent vector fields]] $v \in \Gamma_X(T X)$ are geometrically defined as smoothly varying collections of smooth [[paths]] $\gamma_x \colon \mathbb{R}^1 \to X$ through every point $x \in X$ (i.e. $\gamma(0) = x$), with two such paths regarded as equivalent if their first [[derivative]] $v_x \in T_x X$ at $x$, seen in any [[chart]], coincides.

By pre-composing a [[smooth function]] $f \colon  X \longrightarrow \mathbb{R}^1$ which such a path, we obtain a function $f\circ \gamma_x \;\colon\; \mathbb{R}^1 \to \mathbb{R}^1$ from the [[real line]] to itself. Therefore its [[derivative]] 

$$
  (D_v f)(x) \coloneqq  d (f \circ \gamma)_0
$$

may be identified with a [[real number]] (measuring the rate of change of $f$ along $\gamma$ at $x$ to first order). Since $\gamma_x$, or rather its derivative $v_x \in T_x X$, is assumed to depend smoothly on $x$, this defines a new smooth function

$$
  D_v f \;\colon\; X \longrightarrow \mathbb{R}^1
  \,.
$$ 

Due to the [[product rule]] of differentiation, this assignment $f \mapsto D_v f$ is such that for $f,g \in C^\infty(X)$ two smooth functions, with pointwise product function $f \cdot g$ then 

$$
  D_v(f \cdot g)
  \;=\;
  D_v(f) \cdot g + f \cdot D_v(g)
  \,.
$$

This means that $D_v \;\colon\; C^\infty(X) \to C^\infty(X)$ is a _[[derivation]]_ on the algebra of smooth functions.

Remarkably, _all_ derivations on $C^\infty(X)$ arise this way, and for a unique vector field $v \in \Gamma_X(T X)$:

$$
  \left\{
    \array{
      \text{derivations on}
      \\
      \text{algebra of smooth functions}
      \\
      \text{on}\, X
    }
  \right\}
  \;\simeq\;
  \left\{
     \array{
        \text{smooth}
        \\
        \text{tangent vector fields}
        \\
        \text{on}\, X
     }
  \right\}
$$

This is prop. \ref{Statement} below. What makes this work is the _[[Hadamard lemma]]_, see the [proof](#Proof) below for details.

Notice that the concept of derivations is purely a concept of [[algebra]], with no input from the [[topology]] and [[differential geometry]] that goes into the definition and construction of smooth manifolds and their tangent bundles. 
Therefore the identification of smooth vector fields with derivations is an algebraic incarnation of an aspect of differential geometry, an identification  comparable two two other such phenomena:

* the [[embedding of smooth manifolds into formal duals of R-algebras]] -- which identifies smooth manifolds themselves with the [[formal dual]] of their real algebras of smooth functions;

* the [[smooth Serre-Swan theorem]] which identifies [[smooth vector bundles]] over a smooth manifold with the [[projective modules]] of the algebra of smooth functions.

These statements mean that [[differential geometry]] has more in common with [[algebraic geometry]] than is manifest from the traditional definitions. This serves as the bases for the definition of [[formal smooth manifolds]] and the theory of [[synthetic differential geometry]]. For more exposition of this relation see at _[[geometry of physics -- supergeometry]]_.

Beware however that related algebraic properties familiar from [[affine schemes]] may break in differential geometry: For the [[Kähler differential forms]] of $C^\infty(X)$ to come out as the expected smooth [[differential forms]] one needs to refine the plain $\mathbb{R}$-[[commutative algebra]] $C^\infty(X)$ to the structure of a _[[smooth algebra]]_. See at _[[Kähler differential forms]]_ for discussion of this issue.


## Statements

+-- {: .num_theorem #Statement}
###### Theorem

Let $X$ be a [[smooth manifold]]. 

Write 

1. $C^\infty(X)$ for its real [[algebra of functions|algebra]] of [[smooth functions]] $X \to \mathbb{R}^1$ (under pointwise multiplication);

1. $\Gamma_X(T X)$ for the [[real vector space]] of smooth [[tangent vector fields]] on $X$, hence the space of smooth [[sections]] of the [[tangent bundle]] $T X$ of $X$, regarded as a [[smooth vector bundle]].

1, $Der(C^\infty(X))$ for the [[real vector space]] of $\mathbb{R}$-linear [[derivations]] of the $\mathbb{R}$-algebra $C^\infty(X)$ 

Then:

1. The operation of [[differentiation]] with respect to a [[vector field]]  is a [[derivation]] of $C^\infty(X)$.

1. Every [[derivation]] on $C^\infty(X)$ arises this way, for a unique vector field.

Hence there is an [[isomorphism]]

$$
  D_{(-)}
    \;\colon\;
  \Gamma_X(T X) \stackrel{\simeq}{\longrightarrow} Der(C^\infty(X))
  \,.
$$

=--

+-- {: .proof #Proof}
###### Proof


First to discuss that vector fields induce derivations.
Let $v \in \Gamma_X(T X)$ be a smooth tangent vector field. 

This means first of all that for each $x \in X$ there is a [[smooth function]] $\gamma_x \;\colon\; \mathbb{R}^1 \longrightarrow X$ such that 

1. $\gamma_x(0) = x$

1. $d \gamma_x_0 = v_x \in T_x X$.

Then for $f \colon X \to \mathbb{R}^1$ a smooth function, define a new function 

$$
  D_v(f) \;\colon\; X \longrightarrow \mathbb{R}^1
$$

by

$$
  (D_v(f))(x) \coloneqq d (f \circ \gamma_x)_0 = \frac{d}{d t} (f(\gamma_x(t)))\vert_{t = 0}
  \,.
$$

By the linearity of differentation we have for $c \in \mathbb{R}$ that $D_v(c \cdot f) = c \cdot D_v(f)$. Moreover, by the [[product rule]] for differentiation we have for $f,g \in C^\infty(X)$ two smooth functions, that

$$
  \begin{aligned}
    D_v( f \cdot g)
    & =
    \frac{d}{d t}( (f \cdot g)(\gamma(t)) )\vert_{t = 0}
    \\
    & =
    \frac{d}{ d t}( f(\gamma_x(t)) \cdot g(\gamma_x(t)) )\vert_{t = 0}
    \\
    & =
    \left( \frac{d}{d t}  f(\gamma_x(t))\vert_{t = 0}  \right) \cdot g(\gamma_x(0))
    + 
    f(\gamma_x(0)) \cdot   
    \left(
      \frac{d}{d t} g(\gamma(t))\vert_{t = 0}
    \right)
    \\
    &
    =
    (D_v(f) \cdot g + f \cdot D_v(g))(x) 
  \end{aligned}
  \,.
$$

Therefore it only remains to check that the function $D_v(f)$ is a smooth function in the first place.

Let

$$
  \left\{ \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\to} U_i \subset X \right\}
$$

be an [[atlas]] that exhibits the [[smooth structure]] of $X$, hence an [[open cover]] by subsets equipped with a [[diffeomorphism]] $\phi_i$ from a [[Cartesian space]] $\mathbb{R}^n$ with its standard smooth structure. 

By definition of the [[tangent bundle]] $T X$, its restriction to any [[chart]] of this atlas is given by a diffeomorphism $\psi_i$ as in the following diagram

$$
  \array{
    \mathbb{R}^n \times \mathbb{R}^n
      && \underoverset{\simeq}{\psi_i}{\longrightarrow} && 
    T X\vert_{U_i}
    \\
    & {}_{\phi_i \circ \mathllap{pr_1}}\searrow && \swarrow_{p\vert_{U_i}}
    \\
    && U_i
  }
  \,.
$$

For $D_v(f) \colon X \to \mathbb{R}^1$ to be continuous and smooth, it is sufficient to see that its restrictions

$$
  D_v(f) \circ \psi_i
$$

are continuous and smooth, for all $i \in I$. (For continuity this follows by [this example](Top#ClosedSubspacesGluing) and for differentiability this is clear from the fact that derivatives at any point may be computed in an arbitrary open neighbourhood).

With respect to this chart the tangent vector field $v \in \Gamma_X(T X)$ is given by a smooth function

$$
  v_i
  \;\coloneqq\; 
  pr_2 \circ \psi_i^{-1}(v \vert_{U_i}) 
  \;\colon\;
  U_i
    \longrightarrow
  \mathbb{R}^n
$$

By the identification of tangent vectors on $\mathbb{R}^n$ with elements of $\mathbb{R}^n$, these tangent vectors are represented by straight smooth curves ([this remark](Introduction+to+Topology+--+1EuclideanSpaceTangentBundle)):

$$
  \gamma_{x, i}
  \;\colon\;
  t
  \mapsto
  \phi_i^{-1}(x) + t \cdot v_i(x)  
  \,.
$$

and for $f_i \coloneqq f \circ \phi_i \;\colon\; \mathbb{R}^n \to \mathbb{R}^1$
the restriction of the given smooth function, we have, by the [[chain rule]]

$$
  \frac{d}{d t} ( f_i(\gamma_{x,i}(t)) )\vert_{t = 0}
  =
  \sum_{k = 1}^n (v_i)^k(x) \cdot \frac{\partial f_i(y)}{\partial y^k}\vert_{y = x}
  \,.
$$

(Here and in the following we are writing $(-)^k$ for the $k$th component of an element of $\mathbb{R}^n$.)


This is the value of a function at $x$ with is the sum over the product of two smooth functions, namely the component functions $(v_i)^k$ of the smooth section
in the given chart, and the derivatives of $f_i$ (which are functions by the assumption that $f$ is smooth). 

This shows that $D_v(f)$ is a smooth function.

Now for the converse. Let $D \in Der(\C^\infty(X))$ be a derivation, we need to show that it arises on each chart $\phi_i$ from smooth vector field $v_i$ as above.

The [[Hadamard lemma]] gives that every [[smooth function]] $f_i \colon \mathbb{R}^n \to \mathbb{R}^1$ may be written for each point $x \in \mathbb{R}^n$ as

$$
  f(y) = f(y-x) + \sum_{k = 0}^n (y^k - x^k) \cdot g_{x,k}(y)
$$

for smooth functions

$$
  \{g_k \in C^\infty(\mathbb{R}^n)\}_{k \in \{1,\cdots, n\}}
$$

satisfying

$$
  g_{x,k}(x) = \frac{\partial f(y)}{\partial y^k}\vert_{y = x}
  \,.
$$

Now by the derivation property we have

$$
  \begin{aligned}
    D(f)(x)
    & =
    D
    \left(
       f(0) 
       +
       \sum_{k = 1}^n  ((-)^k - x^k) \cdot g_{x,k}(-)
    \right)
    \\
    & =
    \sum_{k = 1}^n 
      \big(
        {(D( (-)^k - x^k ))} \cdot g_{x,k}(-)
        +
         ((-)^k - x^k) \cdot D g_{x,k}(-)  
      \big)(x)
    \\
    & =
    \sum_{k = 1}^n (v_i)^k(x) \cdot \frac{\partial f(y)}{\partial y^k}\vert_{y = x}
  \end{aligned}
  \,.
$$

Here in the last step we _defined_

$$
  (v_i)^k(x) \coloneqq D( (-)^k )(x)
$$

to be the value at $x$ of the function which the derivation produces when applied to the $k$th coordinate function (which is a smooth function of $x$ by definition of $D$), and we used the above property of the $g_{x,k}$ as well as that $(-)^k - x^k$ vanishes at $x$.

This shows that the derivation $D$ comes, in the chart $\phi_i$, from the vector field $v_i$ as above.

=--






## Related theorems

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[smooth Serre-Swan theorem]]

* [[Borel's theorem]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]



## References

* [[W. F. Newns]], [[A. G. Walker]],  _Tangent Planes To a Differentiable Manifold_.  Journal of the London Mathematical Society s1-31:4 (1956), 400–407 ([doi:10.1112/jlms/s1-31.4.400](https://doi.org/10.1112/jlms/s1-31.4.400))

See also

* theorem 3.7 in [this pdf](http://www.math.toronto.edu/mgualt/MAT1300/week9.pdf)
 