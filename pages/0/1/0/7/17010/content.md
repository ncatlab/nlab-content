
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

\begin{imagefromfile}
    "file_name": "Apostol_StereographicProjection.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Apostol 1973](#Apostol73)"
\end{imagefromfile}


## Idea


_Stereographic projection_ is the name for a specific [[homeomorphism]] (for any $n \in \mathbb{N}$) form the [[n-sphere]] $S^n$ with one point $p \in S^n$ removed to the [[Euclidean space]] $\mathbb{R}^n$ 

$$
  S^n \backslash \{p\} \overset{\simeq}{\longrightarrow} \mathbb{R}^n
  \,.
$$

One thinks of both the $n$-sphere as well as the Euclidean space $\mathbb{R}^n$ as [[topological subspaces]] of $\mathbb{R}^{n+1}$ in the standard way, such that they [[intersection|intersect]] in the [[equator]] of the $n$-sphere. 


\begin{imagefromfile}
    "file_name": "StereographicProjection.png",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

For $p \in S^n$ one of the corresponding poles, the _stereorgraphic projection_ is the  map which sends a point $x \in S^{n}\backslash \{p\}$ along the line connecting it with $p$ to the equatorial plane. 




If one applies stereographic projection to _both_ possible poles $p_+, p_- \in S^n$ of the sphere given a fixed equatorial plane, then one obtains two different [[homeomorphisms]]

$$
  \left\{
     \mathbb{R}^n 
       \underoverset{\simeq}{\phi_i}{\longrightarrow}
     S^n\backslash \{p_i\}
  \right\}_{i \in \{+,-\}}
  \,.
$$

The set of these two projections constitutes an [[atlas]] that exhibits the [[n-sphere]] as a [[topological manifold]], in fact a [[differentiable manifold]] and in fact as a [[smooth manifold]]. 

For $n = 2$ and with $\mathbb{R}^2 \simeq \mathbb{C}$ regarded as the [[complex plane]], then this atlas realizes the [[2-sphere]] as a [[complex manifold]]: the _[[Riemann sphere]]_.

## Definition

We consider the ambient canonical [[coordinates]] of $\mathbb{R}^{n+1}$, in terms of which the $n$-sphere is the [[topological subspace]] whose underlying [[subset]] is presented as follows:

$$
  S^n 
   \;\simeq\;
  \left\{
     x = (x_1, \cdots, x_{n+1})  \in \mathbb{R}^{n+1}
     \,\vert\,
     \underoverset{i = 1}{n+1}{\sum} (x_i)^2 = 1
  \right\}
  \;\subset\;
  \mathbb{R}^{n+1}
  \,.
$$

Without restriction, we may identify the given pole point in the coordinates with

$$
  p = (1,0,\ldots,0)
$$

hence the corresponding equatorial hyperplane with 

$$
  \mathbb{R}^n
    \;\simeq\;
  \left\{
    x = (x_1, x_2, \cdots, x_{n+1}) \in \mathbb{R}^{n+1}
    \,\vert\,
    x_1 = 0
  \right\}
   \;\subset\;
  \mathbb{R}^{n+1}
  \,.
$$

+-- {: .num_prop #StandardStereographicProjection}
###### Proposition
**(standard stereographic projection)**

The function which sends a point $x \in S^{n} \backslash p \subset \mathbb{R}^{n+1}$ to the  intersection of the line through $p$ and $x$ with the equatorial hyperplane is a [[homeomorphism]] which is given in terms of ambient coordinates by

$$
  \array{
    \mathbb{R}^{n+1} \supset \;\;\;
    &
    S^n \backslash (1,0, \cdots, 0)
      &\overset{\phantom{AA} \phantom{AA}}{\longrightarrow}&
    \mathbb{R}^{n}
    &
    \;\;\;
    \subset \mathbb{R}^{n+1}
    \\
    &
    (x_1, x_2, \cdots, x_{n+1})
    &\overset{\phantom{AAAA}}{\mapsto}&
    \frac{1}{1 - x_1}
    \left(
      0 , x_2, \cdots, x_{n+1}
    \right)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

First consider more generally the stereographic projection

$$
  \sigma
    \;\colon\;
  \mathbb{R}^{n+1} \backslash (1,0,\cdots, 0)
    \longrightarrow
  \mathbb{R}^n
   = 
  \{x \in \mathbb{R}^{n.1} \,\vert\, x_1 = 0 \}
$$

of the entire ambient space minus the point $p$ onto the equatorial plane, still given by mapping a point $x$ to the unique point $y$ on the equatorial hyperplane such that the points $p$, $x$ any $y$ sit on the same straight line. 

This condition means that there exists $d \in \mathbb{R}$ such that

$$
  p +  d(x-p) = y
  \,.
$$

Since the only condition on $y$ is that $y_1 = 0$ this implies that 

$$ 
  p_1 + d(x_1-p_1) = 0 
  \,.
$$

This equation has a unique solution for $d$ given by

$$ 
  d = \frac{1}{1 - x_1}
$$

and hence it follow that

$$
  \sigma(x_1, x_2, \cdots, x_{n+1}) 
    = 
  \frac{1}{1-x_1}(0,x_2, \cdots, x_n)
  \,
$$

Since [[rational functions are continuous]], this function $\sigma$ is continuous and since the topology on $S^n\backslash p$ is the [[subspace topology]] under the canonical embedding $S^n \backslash p \subset \mathbb{R}^{n+1} \backslash p$ it follows that the restriction

$$
  \sigma\vert_{S^n \backslash p}
    \;\colon\;
  S^n\backslash p 
    \longrightarrow
  \mathbb{R}^n
$$

is itself a [[continuous function]] (because its pre-images are the restrictions of the pre-images of $\sigma$ to $S^n\backslash p$).

To see that $\sigma \vert_{S^n \backslash p}$ is a [[bijection]] of the underlying sets we need to show that for every

$$
  (0, y_2, \cdots, y_{n+1})
$$

there is a unique $(x_1, \cdots , x_{n+1})$ satisfying

1. $(x_1, \cdots, x_{n+1}) \in S^{n} \backslash \{p\}$, hence

   1. $x_1 \lt 1$;

   1. $\underoverset{i = 1}{n+1}{\sum} (x_i)^2 = 1$;

1. $\underset{i \in \{2, \cdots, n+1\}}{\forall} \left(y_i = \frac{x_i}{1-x_1} \right)$.

The last condition uniquely fixes the $x_{i \geq 2}$ in terms of the given $y_{i \geq 2}$ and the remaining $x_1$, as 

$$
  x_{i \geq 2} = y_i \cdot (1-x_1)
  \,.
$$ 

With this, the second condition says that 


$$
  (x_1)^2 + (1-x_1)^2 \underset{r^2}{\underbrace{\underoverset{i = 2}{n+1}{\sum}(y_i)^2}} = 1
$$

hence equivalently that 

$$
  (r^2 + 1) (x_1)^2 - (2 r^2) x_1 + (r^2 - 1) = 0
  \,.
$$

By the [[quadratic formula]] the solutions of this equation are

$$
  \begin{aligned}
    x_1 
      & = 
    \frac
      { 2 r^2 \pm \sqrt{ 4 r^4 - 4 (r^4 - 1)  } }
      { 2 (r^2 + 1) }
    \\
    & = 
    \frac
      { 2 r^2 \pm 2  }
      { 2 r^2 + 2 }
  \end{aligned}
  \,.
$$

The solution $\frac{ 2 r^2 + 2  }{ 2 r^2 + 2 } = 1$ violates the first condition above, while the solution $\frac{ 2 r^2 - 2  }{ 2 r^2 + 2 } \lt 1$ satisfies it.

Therefore we have a unique solution, given by

$$
  \left(
    \sigma\vert_{S^n \backslash \{p\}}
  \right)^{-1}(0,y_2, \cdots, y_{n+1})
  \;=\;
  \left(
    \frac{2 r^2 - 2}{2 r^2 +2}
    , 
    \left( 1- \frac{2 r^2 - 2}{2 r^2 +2} \right) y_2
    ,
    \cdots
    ,
    \left( 1- \frac{2 r^2 - 2}{2 r^2 +2} \right) y_{n+1}
  \right)
$$

In particular therefore also an [[inverse function]] to the stereographic projection exists and is a [[rational function]], hence continuous. So we have exhibited a homeomorphism as required.

=--


## Generalizations

Of course the construction in prop. \ref{StandardStereographicProjection} does not really depend on the specific [[coordinates]] chosen there.

More generally, for any point $p\in S^n$, considered as a [[vector]] in $\mathbb{R}^{n+1}$, let $W\subset \mathbb{R}^{n+1}$ be the [[linear subspace]] that is the [[orthogonal complement]] to the [[linear span]] $span\{v\}$. Then there is a [[homeomorphism]]

$$
  \sigma \;\colon\; S^n\setminus \{v\} \stackrel{\simeq}{\longrightarrow} W
$$

given by sending a point $p\in S^n\setminus \{v\}$ to the point in $W$ that is the intersection of the line through $v$ and $p$ with $W$.


More generally, one may take for $W$ any _[[affine space|affine]]_ subspace of $\mathbb{R}^{n+1}$ normal to $span\{v\}$ and not containing $v$. For instance one option is to take $W$ to be the tangent space to $S^n$ at $-v$, embedded as a subspace of $\mathbb{R}^{n+1}$.

(see e.g. [Cook-Crabb 93, section 1](#CookCrabb93))

## Properties

### One-point compactification

The inverse map $\sigma^{-1}$ exhibits $S^n$ as the [[one-point compactification]] of $W$.


### Extra geometric structure

In most cases of interest one is doing [[geometry]] using stereographic projection, so the sphere and the subspace $W$ are equipped with extra structure. Taking the explicit case above ($v=(1,0,\ldots,0)$), as the formula is so simple, some structures are automatically preserved, for instance:

* [[conformal structure]]

* [[orthogonal group|orthogonal]] [[group action]] fixing $v,-v$ pointwise (note that these two points are sent to "$\infty$" and $0$, respectively, under $\sigma$)

## Over other fields 

Stereographic projection is a general [[algebraic geometry|geometric]] technique which can be applied to other [[commutative rings]] $k$ besides $k = \mathbb{R}$. We give a brief taste of this for the case of [[fields]]. For simplicity, we focus on [[conic sections]], i.e., solutions sets in the [[projective plane]] $\mathbb{P}^2(k)$ to [[polynomial|homogeneous polynomials]] of [[degree]] $2$. 

Via stereographic projection, all *pointed*[^1] nonsingular conic sections $C \subset \mathbb{P}^2(k)$ are isomorphic and can be identified explicitly with a projective line $\mathbb{P}^1(k)$ by means of a [[stereographic projection]]. 

Geometrically, if $p$ is the chosen basepoint of $C$ and $L \subset \mathbb{P}^2(k)$ is a line not incident to $p$, then for any other point $q$ of $C$ the unique line $L(p, q)$ incident to $p$ and $q$ intersects $L$ in exactly one point, denoted $\phi(q)$. (Here $\phi(p)$ is taken to be the intersection of the _tangent_ to $p$ at $C$ with $L$; this can be considered the basepoint of $L$.) In the opposite direction, to each point $x$ of $L$, the line $L(p, x)$ intersects $C$ in $p$ and (since a quadratic with one root will also have another root) another point $q$ (which might be the same as $p$; this happens precisely when $L(p, x)$ is the tangent to $C$ at $p$); this gives the inverse $\phi^{-1}(x) = q$. In this way we obtain an isomorphism $\phi: C \to L$ of subvarieties. 

+-- {: .num_example #PythagoreanTriples} 
###### Example 
For the case $k = \mathbb{Q}$ and the rational conic $C = \{(x, y) \in \mathbb{Q} \times \mathbb{Q}: x^2 + y^2 = 1\}$, stereographic projection from the point $(-1, 0)$ on $C$ to the rational line $x = 0$ defines an isomorphism of [[algebraic varieties]] $C \to \mathbb{P}^1(\mathbb{Q})$. As the calculations above show, its inverse takes $(0, t)$ (for $t \in \mathbb{Q}$) to $(\frac{1 - t^2}{1 + t^2}, \frac{2 t}{1 + t^2})$. 

A Pythagorean triple is a triple of integers $(a, b, c)$ such that $a^2 + b^2 = c^2$, so that $(\frac{a}{c}, \frac{b}{c})$ lies on $C$. The isomorphism indicates that for each such point on $C$ (written as a pair of fractions in reduced form), there is a rational number $t = \frac{p}{q}$ (again in reduced form) so that 

$$\frac{a}{c} = \frac{1 - t^2}{1 + t^2} = \frac{q^2 - p^2}{q^2 + p^2}, \qquad \frac{b}{c} = \frac{2 t}{1 + t^2} = \frac{2 p q}{q^2 + p^2}.$$ 

If we assume $a, b, c$ are coprime, and further (re)arrange the triple so that $a$ is odd and $b$ is even, one may quickly conclude from the first of this pair of equations that $p, q$ must have opposite parity. A little further argumentation then shows $q^2 - p^2, 2 p q, q^2 + p^2$ must be mutually coprime, so that in fact $a = q^2 - p^2, b = 2 p q$, and $c = q^2 + p^2$. Thus we arrive at the classical parametrization of Pythagorean triples, essentially on the basis of the geometry of stereographic projection! 
=-- 


## Related entries

* [[Riemann sphere]]

* [[representation sphere]]


## References

Textbook accounts:

* {#Apostol73} [[Tom Apostol]], Fig. 1.3 in: *Mathematical Analysis* 1973 ([pdf](http://www.ru.ac.bd/wp-content/uploads/sites/25/2019/03/205_04_Apostol-Mathematical-Analysis-1973.pdf))


See also:

* Wikipedia, _[Stereographic projection](https://en.wikipedia.org/wiki/Stereographic_projection)_

* {#CookCrabb93} A. L. Cook, M.C. Crabb, _Fiberwise Hopf structures on sphere bundles_, J. London Math. Soc. (2) 48 (1993) 365-384 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/crabbcook.pdf))


[[!redirects stereographic projections]]

