
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

<a id="DocStart"></a>

#Contents#
* table of contents
{: toc}

+-- {: .num_section #sectiona }
=--

## Introduction ## {: .num_section}

A _kinematic tangent space_ of a [[generalized smooth space]] at some point is an equivalence class of smooth [[curves]] through that point, regraded as equivalent if their first [[derivatives]] coincide. This generalizes the notion of [[tangent space]] of a [[differentiable manifold]]. The alternative notion is that of _[[operational tangent space]]_ which for differentiable manifolds coincides, but more generally need not.

[[generalized smooth space|Generalised smooth spaces]] are, as the name suggests, generalisations of [[smooth manifolds]]. They share many common properties and constructions with manifolds. One of the most basic constructions applied to manifolds is that of the [[tangent space]]. There are, indeed, several different constructions of tangent spaces, but as can be shown they are all equivalent for smooth manifolds (see [Spivak 79](#Spivak79), for example). This is no longer true for more general smooth spaces, indeed even for [[Fréchet manifolds]] the various notions are no longer equivalent.

One of the more intuitive definitions of the tangent space of a manifold is as the space of derivatives of smooth curves. Roughly speaking, in this view the tangent space of a manifold at a point is the home of all derivatives of smooth curves through that point. To differentiate this notion from the other definitions, it is sometimes called the **kinematic tangent space**.

Once we go beyond ordinary smooth manifolds, the kinematic tangent space of a smooth space $X$ may not have some or all of its "usual" properties. In particular, it may not even be a [[vector space]]. (If it is then $X$ is also called a _[[microlinear space]]_, at least in the context of [[synthetic differential geometry]] and possibly under some more conditions. ) However, it will always be a kind of *partial* vector space.

It is also possible to define "higher" kinematic tangent spaces. This is not done by iterating the construction, but rather by considering a slightly different construction: instead of [[derivatives]] of [[curves]], we can take the second derivative of curves whose first derivative vanishes. For an ordinary manifold, this yields nothing extra as it is merely observing that the tangent space of the zero vector is again the tangent space. However, for more general spaces it can provide more tangent vectors. For example, the kinematic tangent space at $0$ of the space $[0,1)$ is just $\{ 0\} $ because any curve $\alpha $ with $\alpha (0) = 0$ must also have $\alpha '(0) = 0$. But there are curves $\alpha $ with $\alpha (0) = 0$ and $\alpha '(0) = 0$ but $\alpha''(0) \ne 0$. These curves define a tangent vector that "sees" the inward direction from $0$.

+-- {: .num_section #sectionb }
=--
## Definition ## {: .num_section}

Unless otherwise specified, we shall assume that we have fixed an arbitrary category of [[generalised smooth space]]. The general construction does not rely on a particular choice, though of course one should be consistent.

+-- {: .num_defn #defna }
###### Definition ######
Let $X$ be a smooth space. Let $x \in X$ be a point. The *kinematic tangent space* at $x$, written $T_{x} X$, is defined as the set of equivalence classes of smooth curves $\alpha \colon \mathbb{R} \to X$ with the property that $\alpha (0) = x$ under the relation $\alpha \simeq \beta $ if $(f \circ \alpha )'(0) = (f \circ \beta )'(0)$ for all smooth functions $f \colon X \to \mathbb{R} $.
=--

As mentioned in the introduction, this need not be a [[vector space]]. However, it will always have some of the structure of a vector space. There is a special vector, which we write as $0$ (or $0_{x}$) represented by the constant curve at $x$. And for $v \in T_{x} X$ and $\lambda \in \mathbb{R} $ we can define $\lambda v$ by taking a representative for $v$, say $\alpha $, and letting $\lambda v$ be the equivalence class of $t \mapsto \alpha (\lambda t)$. What fails is the existence of a globally defined addition. It may be defined for a given pair of vectors: for $u, v \in T_{x} X$ we say that the sum $u + v$ exists if, for representatives $\alpha $ and $\beta $ of $u$ and $v$ respectively, there is a smooth curve $\gamma $ with $\gamma (0) = x$ and
$$
(f \circ \gamma )'(0) = (f \circ \alpha )'(0) + (f \circ \beta )'(0)
$$
for all smooth $f \colon X \to \mathbb{R} $. It follows from the definition that if $u + v$ exists, it is unique. Also, all the identities one would expect from addition hold providing all the terms are defined.

One nice property of the kinematic tangent spaces is that the construction of the analogous tangent *bundle* is straightforward. This is because all of our categories are cocomplete and cartesian closed.

+-- {: .num_defn #defnb }
###### Definition ######
Let $X$ be a smooth space. The *tangent bundle* of $X$ is defined to be the quotient of the smooth space $C^{\infty } (\mathbb{R},X)$ by the relation $\alpha \simeq \beta $ if $\alpha (0) = \beta (0)$ and for all smooth $f \colon X \to \mathbb{R} $, $(f \circ \alpha )'(0) = (f \circ \beta )'(0)$.
=--

If $X$ is *functionally Hausdorff* - that is, smooth functions separate points - then the equivalence class can be written more elegantly as: $\alpha \simeq \beta $ if for all $f \colon X \to \mathbb{R} $ and $i \in \{ 0,1\} $, $(f \circ \alpha )^{(i)}(0) = (f \circ \beta )^{(i)}(0)$.

It should be pointed out at this early stage that when considering the space of tangent vectors at a particular point, say $x \in X$, then there are potentially two smooth structures on this set coming from the above definitions. We have the space $T_{x} X$ defined as the quotient of curves based at $x$ and the space $(T X)_{x}$ defined as the fibre of the full tangent bundle. The inclusion of based curves in all curves descends to a smooth map $T_{x} X \to (T X)_{x}$ which is a bijection on the underlying sets, but this need not be a diffeomorphism.

The definition of the kinematic tangent spaces and bundle are closely related to the alternative definition of the tangent space in terms of derivations (sometimes called the [[operational tangent space]]). One could say that the kinematic tangent space is the space of curves seen through the lens of derivations.

Now if the first derivative of a curve vanishes, then its second derivative acts as a derivation since:
$$
\begin{aligned}
((f g) \circ \alpha )''(0) &= (f \circ \alpha )''(0) (g \circ \alpha )(0) + 2 (f \circ \alpha )'(0) (g \circ \alpha )'(0) + (f \circ \alpha )(0) (g \circ \alpha )''(0) \\    &= (f \circ \alpha )''(0) (g \circ \alpha )(0) + (f \circ \alpha )(0) (g \circ \alpha )''(0).
\end{aligned}
$$
With this in mind, we can define higher level kinematic tangent spaces.

+-- {: .num_defn #defnc }
###### Definition ######
Let $X$ be a smooth space. Let $x \in X$ be a point. Let $k \in \mathbb{N} $. The *$k$th kinematic tangent space* at $x$, written $T_{x,k} X$, is defined as the set of equivalence classes of smooth curves $\alpha \colon \mathbb{R} to X$ with the property that $\alpha (0) = x$ and $(f \circ \alpha )^{(j)}(0) = 0$ for $1 \le j \le k - 1$ and smooth $f \colon X \to \mathbb{R} $. The relation is $\alpha \simeq \beta $ if $(f \circ \alpha )^{(k)}(0) = (f \circ \beta )^{(k)}(0)$ for all smooth functions $f \colon X \to \mathbb{R} $.

The *$k$th kinematic tangent bundle* is defined similarly.
=--

There is an obvious map $T_{x,k} X \to T_{x,m k} X$ for $m \in \mathbb{N} $ given by precomposition with $t^{m}$. This defines a diagram indexed by the [[poset]] $\mathbb{N}$ with divisibility as the order. We can define the *full* kinematic tangent space at $x$ as the colimit of this diagram.

The structure of the higher kinematic tangent spaces is somewhat complicated. For example, in the second kinematic tangent space then $(-1) \cdot v = v$.

In the following we shall concentrate on the first kinematic tangent space.

+-- {: .num_section #sectionc }
=--
## Properties ## {: .num_section}


In this section, we shall gather various results on kinematic tangent spaces that will be of use elsewhere.

Because the kinematic tangent space is defined using curves, it has nice properties with respect to limits and mapping spaces. However, as it also uses quotients, these properties are not necessarily as nice as they could be.

+-- {: .num_prop #propositiona }
###### Proposition ######
Let $X,Y$ be smooth spaces. There is a natural isomorphism $T(X \times Y) \to T X \times T Y$.
=--

+--   {: .proof }
The   map in the given direction is obvious: the projection $X \times Y \to X$ is smooth and so induces a map $T(X \times Y) \to T X$. Together with the other projection, we get a map:
$$
T(X   \times Y) \to T X \times T Y.
$$
For   the other direction, we need to consider curves. The result will hinge on the fact that when testing the equivalence relation for curves in $X \times Y$, it is enough to consider functions $X \times Y \to \mathbb{R} $ that factor through one of the projections.

To see this, consider curves $\alpha \colon \mathbb{R} \to X$ and $\beta \colon \mathbb{R} \to Y$ and let $\gamma \colon \mathbb{R} \to X \times Y$ be their product. Let $f \colon X \times Y \to \mathbb{R} $ be a smooth function. The composition $f \circ \gamma $ factors as:
$$
\mathbb{R} \xrightarrow{\Delta } \mathbb{R} \times \mathbb{R} \xrightarrow{\alpha \times \beta } X \times Y \xrightarrow{f} \mathbb{R}.
$$
Thus the derivative of $f \circ \gamma $, at $0$, factors through the derivative of $(s,t) \mapsto f(\alpha (s),\beta (t))$ at $(0,0)$. As this map is smooth, its derivative agrees with the vector of partial derivatives. As every beginner in calculus knows, to compute the, say, $s$-derivative we "hold $t$ fixed and vary $s$". That is to say, we compute the derivative of:
$$
s \mapsto f(\alpha (s),\beta (0)).
$$
Let $y_{0} = \beta (0)$ and define $g \colon X \to \mathbb{R} $ as $g(x) = f(x,y_{0})$. Then the above function agrees with $g \circ \alpha $. For the other side, let $x_{0} = \alpha (0)$ and define $h \colon Y \to \mathbb{R} $ as $h(y) = f(x_{0},y)$.

Hence
$$
(f \circ \gamma )'(0) = \begin{bmatrix} (g \circ \alpha )'(0) & (h \circ \beta )'(0) \end{bmatrix} D \Delta _{0}.
$$
From this we see that the map $T (X \times Y) \to T X \times T Y$ is injective. It is clearly surjective, and thus it remains to show that it is a diffeomorphism.

This follows from the fact that they can both be written as quotients of the same space. For this, we use the natural isomorphism $C^{\infty } (\mathbb{R}, X) \times C^{\infty } (\mathbb{R},Y) \cong C^{\infty } (\mathbb{R}, X \times Y$.
=--

For mapping spaces, we have an obvious map in one direction. A tangent vector at a map is an infinitesimal deformation of that map. Evaluation yields deformations at each point which fit together to give a family of deformations. A simple diagram chase shows that everything involved is smooth.

+-- {: .num_prop #propositionb }
###### Proposition ######
Let $S, X$ be smooth spaces. There is a natural transformation $TC^{\infty } (S, X) \to C^{\infty } (S,T X)$.
=--

+-- {: .proof }
The natural transformation is build up as follows. We start with the evaluation map, $S \times C^{\infty } (S,X) \to X$. Applying the tangent bundle functors, we obtain:
$$
T (S \times C^{\infty } (S,X)) \to T X.
$$
We can compose that with the natural isomorphism from Proposition&nbsp;[1](#propositiona) to obtain:
$$
T S \times T C^{\infty } (S,X) \to T X.
$$
Composing this with the zero section on $T S$ yields:
$$
S \times T C^{\infty } (S,X) \to T X.
$$
Whereupon the adjunction comes in to play to produce:
$$
T C^{\infty } (S,X) \to C^{\infty } (S, T X)
$$
as required.
=--


## Related concepts

* [[operational tangent bundle]]

* [[synthetic tangent bundle]]


## References ##

* {: #citeMR53283} **Spi79** [[Michael Spivak]], _A comprehensive introduction to differential geometry_ Vol. I. Wilmington, Del., 1979.
 {#Spivak79}

[[!redirects kinematic tangent spaces]]
[[!redirects kinematic tangent bundle]]
[[!redirects kinematic tangent bundles]]
