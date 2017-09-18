

#Contents#
* table of contents
{:toc}

## Idea

A _standard Courant Lie algebroid_ of a [[manifold]] $X$ is a type of [[Courant algebroid]] constructed from the [[tangent bundle]] and [[cotangent bundle]] of $X$. This is the principal algebraic structure studied in [[generalized complex geometry]].

## Definition

Recall from the discussion at [[Courant algebroid]] that there are the following two equivalent definitions of Courant algebroids: 

* as a [[vector bundle]] equipped with a bracket and a bilinear form on its space of sections, satisfying various identities;

* as a [[L-infinity algebroid|Lie 2-algebroid]] equivalently encoded in its [[Chevalley–Eilenberg algebra]], equivalently the function algebra on a certain type of [[dg-manifolds]].

### As a vector bundle with extra structure 

In the first perspective a _standard Courant algebroid_ of a [[manifold]] $X$ is the vector bundle $E = T X\oplus T^* X$ -- the fiberwise [[direct sum]] of the [[tangent bundle]] and the cotangent bundle -- with 

* bilinear form 

  $$
    \langle X + \xi , Y +\eta \rangle = \eta(X) + \xi(Y)
  $$

  for $X,Y \in \Gamma(T X)$ and $\xi, \eta \in \Gamma(T^* X)$

* brackets

  $$
    [X + \xi, Y + \eta] = [X,Y] + \mathcal{L}_X \eta 
    - \mathcal{L}_Y \xi + \frac{1}{2} d (\eta(X) - \xi(Y))
  $$

  where $\mathcal{L}_X \eta = \{d,\iota_X\} \eta$ denotes the [[Lie derivative]] of the 1-form $\eta$ by the vector field $X$.

### As a dg-manifold

As an [[dg-manifold]] a standard Courant algeebroid is is $\Pi T^* \Pi T X$, the shifted cotangent bundle of the [[shifted tangent bundle]],

where the differential (homological vector field) is on each local coordinate patch $\mathbb{R}^n \simeq U \subset X$ with coordinates 

* $\{x^i\}$ in degree 0

* $\{d x^i\}$ and $\{\theta_i\}$ in degree 1 

* and $\{p_i\}$ in degree 2 

given by

  $$
    \begin{aligned}
      d_C &= d_{dR} + p_i \frac{\partial}{\partial \theta_i}
      \\
      &= d x^i \frac{\partial}{\partial x^i }
       + p_i \frac{\partial}{\partial \theta_i}
    \end{aligned}
    \,.
  $$


### As a Lie 2-algebroid

We may read the above [[dg-algebra]] as the [[Chevalley–Eilenberg algebra]] $CE(\mathfrak{c}(X))$ of the [[Lie ∞-algebroid|Lie 2-algebroid]] $\mathfrak{c}(X)$, the specification of which entirely specifies the Lie 2-algebroid itself. 

More on this in the discussion below.


## Properties

### As the Atiyah Lie 2-algebroid of a $U(1)$-gerbe

A standard Courant algebroid may be understood as being related to $\mathbf{B}U(1)$ [[principal 2-bundle]]s ($U(1)$-[[gerbe]]s) as an [[Atiyah Lie algebroid]] is related to a $U(1)$-[[principal bundle]].

(...explain...)


### Connections and generalized Riemannian metrics

Write $\mathfrak{c}(X)$ for the standard Courant algebroid of the manifold $X$. It comes canonically equipped with a projection down to the [[tangent Lie algebroid]] $T X $ of $X$:

$$
  \pi : \mathfrak{c}(X) \to X
  \,.
$$

A [[section]] 

$$
  \sigma : T X \to \mathfrak{c}(X)
$$

of this morphism of [[Lie ∞-algebroid]]s is often called a _connection_ on $\mathfrak{c}(X)$. One may regard it as being special flat [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebroid valued differential form]] data on $X$.

+-- {: .un_prop}
###### Proposition

On base manifolds of the form $X = \mathbb{R}^n$ sections of $\mathfrak{c}(X) \to T X$ in the 1-[[category]] of [[Lie ∞-algebroid]]s are in natural bijection with rank-2 tensor fields on $X$, i.e. with sections $q \in \Gamma(T X \oplus T X)$.

=--

The proof is straightforward and easy, but spelling it out in detail also serves to establish concepts and notation for the treatment of the Courant algebroid in terms of its [[Chevalley–Eilenberg algebra]].

+-- {: .proof}
###### Proof

The [[Chevalley–Eilenberg algebra]] of the Lie 2-algebroid $\mathfrak{c}(\mathbb{R}^n)$ is the [[semifree dga]] whose underlying algebra is the [[Grassmann algebra]]

$$
  CE(\mathfrak{c}(X))
  = 
  \left(
  \wedge_{C^\infty(X)}^\bullet
  ( \langle \xi^i \rangle_{i=1}^n 
    \oplus
    \langle \theta_i \rangle_{i=1}^n
    \oplus
    \langle p_i \rangle_{i=1}^n
  )
  \,,
  d_{\mathfrak{c}(X)}
  \right)
$$

where the generators $\xi_i$ and $\theta_i$ are in degree 1 and the $p_i$ in degree 2, equipped with the differential $d_{\mathfrak{c}(X)}$ that is defined on generators by

$$
  d_{\mathfrak{c}(X)} : x^i =  \xi^i
$$

$$
  d_{\mathfrak{c}(X)} : \xi^i = 0
$$

$$
  d_{\mathfrak{c}(X)} : \theta_i = p_i
$$

$$
  d_{\mathfrak{c}(X)} : p_i = 0
  \,
$$


where $\{x^i\}_{i=1}^n$ are the canonical coordinate functions on $\mathbb{R}^n$.

The [[Chevalley–Eilenberg algebra]] of the [[tangent Lie algebroid]] $T X$ is the [[deRham complex]] 

$$
  CE(T X ) = (\Omega^\bullet(X), d_{dR})
  \,.
$$

The morphism $\mathfrak{c}(X) \to T X$ is given by the [[dg-algebra]] morphism 

$$ 
  (\Omega^\bullet(X),d_{dR}) \hookrightarrow
  CE(\mathfrak{c}(X))
$$

that is the identity on $C^\infty(X)$ and identifies the $\xi^i$ with the deRham differentials of the standard coordinate functions

$$
  d x^i \mapsto \xi^i
  \,.
$$

A section $\sigma : \mathfrak{c}(X) \to T X$ is accordingly a dg-algebra morphism 

$$
  \sigma^* : CE(\mathfrak{c}(X)) \to (\Omega^\bullet(X), d_{dR})
  \,.
$$ 

Being a section, it has to be the identity on $C^\infty(X)$ and send $\xi^i \mapsto d_{dR} x^i$.

The image of the generators $\theta_i$, being of degree 1, must be a linear combination over $C^\infty(X)$ of the degree-1 elements in $\Omega^\bullet(X)$, i.e. must be 1-forms on $X$. This defines the rank-2 tensor $q$ in question by

$$
  \hat{t}_i \mapsto q_{i j} \d x^i
  \,.
$$

For this assignment to qualify as part of a morphism of dg-algebras, it has in addition to be compatible with the differential. The condition is that for all $i$ we have the equality in the bottom right corner of

$$
  \array{
     \theta_i &\stackrel{d_{\mathfrak{c}(X)}}{\mapsto}&& p_i
     \\
     \downarrow^{\mathrlap{\sigma^*}} 
     &&& \downarrow^{\mathrlap{\sigma^*}}
     \\
     q_{i j} d x^j &\stackrel{d_{dR}}{\mapsto}&
     (\partial_k q_{i j}) d x^k \wedge d x^j
     = &
     s^*(p_i)  
  }
  \,.
$$

This uniquely fixes the image under $\sigma^*$ of the generators $p_i$ and the differential is respected. So, indeed, the section $\sigma^*$ is specified by the tensor $q \in \Gamma(T X \otimes T X)$ and every such tensor gives rise to a section.


=--

The rank-2 tensor $q$ appearing in the above may be uniquely writtes as sum of a symmetric and a skew-symmetric rank-2 tensor $g \Gamma(Sym^2(T X))$ and $b \in \Gamma(\wedge^2 T X)$

$$
  q = g + b
  \,.
$$

If the symmetric part happens to be non-degenerate, it may be regarded as a (possibly [[pseudo-Riemannian metric|pseudo]]-)[[Riemannian metric]]. In this case the combination $q = g + b$ is called a **generalized Riemannian metric** in [[generalized complex geometry]].

### Canonical $\infty$-Lie algebroid 3-cocycle

The standard Courant albebroid $\mathfrak{c}(X)$ is canonically equipped with the [[Lie ∞-algebroid cohomology|Lie ∞-algebroid 3-cocycle]] $\mu \in CE(\mathfrak{c}(X))$ that is on a local patch $\mathbb{R}^n \simeq U \to X$ given by

$$
  \mu|_U = \xi^i \wedge p_i
  \,.
$$


### Morphisms between standard Courant algebroids

+-- {: .un_prop}
###### Proposition

In the 1-[[category]] of [[Lie ∞-algebroid]]s, [[automorphism]]s of the standard Courant algebroid of a cartesian space, $\mathfrak{c}(\mathbb{R}^n)$, that 

* respect the projection $\mathfrak{c}(X) \to T X$ 

  $$
     \array{
       \mathfrak{c}(X) &&\stackrel{f}{\to}&& \mathfrak{c}(X)
       \\
       & \searrow && \swarrow
       \\
       && T X
     }
  $$

* fix the canonical 3-cocycle $\mu = \xi^i p_i$

come from (...say this more precisely...) rank-2 tensors $q = g + b$ such that the skew symmetric part $b$ is a closed 2-form, $d_{dR} b = 0$.

=--

+-- {: .proof}
###### Proof

With the same kind of reasoning as above, we find that the action on the generators $\theta_i$ and $p_i$ is of the form

$$
  \array{
     \theta_i &\stackrel{d_{\mathfrak{c}(X)}}{\mapsto}&& p_i
     \\
     \downarrow^{\mathrlap{f^*}} 
     &&& \downarrow^{\mathrlap{f^*}}
     \\
     \theta_i + q_{i j} \theta^i  &
      \stackrel{d_{\mathfrak{c}(X)}}{\mapsto}&
     p_i
     +
     \partial_k q_{i j} \theta^k \wedge \theta^j     
     = &
     f^*(p_i)
  }
  \,.
$$

For the 3-cocycle to be preserved, $f^*(\xi^i p_i) = \xi^i p_i$ we need that

$$
  0 =
  \partial_k q_{i j} \theta^i \wedge \theta^k \wedge \theta^j
 = 
  \partial_k b_{i j} \theta^i \wedge \theta^k \wedge \theta^j
 = 
  \pi^*(d_{dR} b)
  \,.
$$


=--

## Related concepts

* [[higher Atiyah groupoid]]

  * [[Atiyah groupoid]]

  * [[Courant 2-groupoid]]

## References

The description of the standard Courant algebroid in its incarnation as an [[dg-manifold]] is given for instance in section 5 of

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_ ([arXiv:0203110](http://arxiv.org/abs/math/0203110))


[[!redirects standard Courant Lie 2-algebroid]]
