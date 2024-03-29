[[!redirects propagating flows]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

[[smooth mapping space|Smooth mapping spaces]] are very nice examples of [[infinite dimensional smooth manifolds]].
One reason for their nice behaviour is that it is often possible to use the structure of the [[target space]] (a finite [[dimension]]al [[manifold]]) to study the mapping space.
This provides a route from finite dimensional [[differential topology]] to that of infinite dimensions.
It is usually the case that one needs stronger structure on the target space to do this than would be needed just for the finite dimensional result, but as the target space is a finite dimensional manifold that stronger structure is usually there anyway.

An example of this is the concept of a [[tubular neighbourhood]] of an [[embedding]].  As shown at [[A Not-So-Nice Submanifold]], not all embeddings of infinite dimensional manifolds - even of mapping spaces - admit tubular neighbourhoods.  However, if the embedding is of a coincidental nature then it is possible to use structure on the target manifold to find tubular neighbourhoods in infinite dimensions.

By "coincidental nature", we mean that the submanifold is defined by taking those smooth maps with some condition imposed that says that certain "coincidences" happen.  That is, that the values of the map at certain points coincide, or are constrained to lie in some submanifold of the target space.

Let us consider, for an example, the simplest case: the inclusion of based loops in [[smooth loop space|smooth loops]].  So let $M$ be a smooth finite dimensional manifold, $L M$ its smooth [[free loop space]] and $\Omega M$ its smooth [[based loop space]].  Let $x_0$ be the basepoint of $M$, and $1$ the basepoint of the [[circle]], $S^1$.  To get a tubular neighbourhood of this, we need to start by finding a suitable neighbourhood.  To do this, we choose a [[chart]] $\phi \colon \mathbb{R}^n \to U \subseteq M$ at $x_0$ (so that $\phi(0) = x_0$).  We define the neighbourhood of $\Omega M$ to be those loops $\alpha \in L M$ such that $\alpha(1) \in U$.  To make this a _tubular_ neighbourhood, we need to find a way to project these loops on to $\Omega M$.  That is, given a loop $\alpha \colon S^1 \to M$ with $\alpha(1) \in U$ we need to produce a loop $\pi(\alpha) \colon S^1 \to M$ with $\pi(\alpha)(1) = x_0$.  It is obvious how to move the basepoint: simply scale it to $x_0$ using the scalar multiplication coming from the chart.  However, that just moves $\alpha(1)$.  We need to move the whole of $\alpha$ with it - or at least, drag that part of it near $1$.  We cannot assume that all of $\alpha$ lies in $U$.  The solution is to define a diffeomorphism $\Psi$ of $M$ with the property that $\Psi(\alpha(1)) = x_0$.  Then we can define $\pi(\alpha) = \Psi \circ \alpha$.  As we vary $\alpha$, so we also vary $\alpha(1)$, and thus must vary the diffeomorphism $\Psi$.  The trick is to choose $\Psi$ so that it varies smoothly with $\alpha(1)$.

In the above example, this is straightforward because everything happens in the chart, and thus effectively on $\mathbb{R}^n$.  There are more complicated examples.  One such is the basic construction in [[string topology]].  Within $L M \times L M$ we consider those pairs of loops $(\alpha,\beta)$ such that $\alpha(1) = \beta(1)$.  Then for $(\alpha,\beta)$ with $\alpha(1)$ _near_ to $\beta(1)$ we want to project the pair $(\alpha,\beta)$ to a pair where these values coincide.  Now although the points $\alpha(1)$ and $\beta(1)$ are near (in some vague not-yet-defined sense), they may, as a pair, roam all over the manifold.  Thus local solutions are not applicable here.  Nonetheless, the question still comes down to the ability to choose diffeomorphisms consistently according to some conditions.

## Definition ##

One way to choose these diffeomorphisms is to use the notion of a **propagating flow**.  The term was coined by [[Veronique Godin]] in ([Godin, 07](#Godin)) and is based on an idea due to [[Andrew Stacey]] in ([Stacey, 05](#Stacey)), though there are probably antecedents.
The basic idea is contained in the following definition.

+-- {: .num_definition #propflow}
###### Definition
Let $\pi \colon E \to M$ be a [[vector bundle]] over a [[smooth manifold]].  Everything here is assumed to be finite dimensional.  We consider the space $Diff_{fc}(E)$ of [[diffeomorphisms]] of $E$ which preserve the [[fibres]] of $E$ and have [[compact support]].  A **propagating flow** is a [[smooth map]] 

$$
  \phi \colon E \to Diff_{fc}(E)
$$ 

with the property that 

$$
  \phi(v) : v \mapsto \pi(v)
$$

where we identify $\pi(v)$ with the zero vector in the corresponding fibre of $E$.

=--

## Construction ##

The original definition of a propagating flow in [Stacey, 05](#Stacey) and [Godin, 07](#Godin) used the exponentiation map from vector fields to diffeomorphisms to get the actual diffeomorphism.  The idea of that was that it is much easier to build a vector field with the required properties than a diffeomorphism because vector fields are more easily manipulated.  But the diffeomorphisms used here are simple enough that they can be constructed directly.  This makes it easier to generalise to situations where the exponentiation map cannot be assumed to exist.

Let us consider the linear situation first.  We start with a vector space, $V$, and a vector $v \in V$.  We want to define a diffeomorphism $\phi_v \colon V \to V$ with the property that $\phi_v(v) = 0$.  This is simple enough:
$$
\phi_1(w) = w - v.
$$
The problem with this is that we do not want just any diffeomorphism.  We want one that is the identity "near infinity".  Let us start by fixing the diffeomorphism in the $v$-direction.

Choose a smooth function $\sigma \colon \mathbb{R} \to [-1,0]$ with the following properties:

1. $\sigma(t) = \begin{cases} 0 & t \le -2 \\ - 1 & 0 \le t \le 1 \\ 0 & 2 \le t \end{cases}$
2. $\sigma'(t) \gt -1$ (note that this is possible as we have given ourselves an interval of length $2$ to get from $0$ at $t = -2$ to $-1$ at $t = 0$.

We are actually interested in the function $t \mapsto t + h \sigma(t)$ for $|h| \le 1$.  The first property of $\sigma$ tells us that this agrees with the identity outside $[-2,2]$ and that it is $t \mapsto t - h$ on $[0,1]$.  The second property tells us that its derivative is strictly bigger than $1 - h$ and so, for $h \le 1$, is a diffeomorphism.

On $V$, we choose a "dual functional" to $v$.  That is, we choose some continuous linear functional $f \colon V \to \mathbb{R}$ with $f(v) = 1$ (we need to assume that $v \ne 0$ for this part, we shall correct for that later).  Then we define a diffeomorphism on $V$ by:
$$
\phi_2(w) = w + \sigma(f(w))v =  (w - f(w)v) + (f(w) + \sigma(f(w)))v.
$$
The second expression shows that what we have done is used $f$ to identify $V$ with $\ker f \oplus \mathbb{R}$ and then applied $t \mapsto t + \sigma(t)$ on the $\mathbb{R}$-factor.

This fixes our diffeomorphism in the $v$-direction.  To fix it in the other direction, we choose a smooth function $\widehat{\tau} \colon \ker f \to [0,1]$ which is $0$ "near infinity" and $1$ at $0$.  Then we mix this in to the above as follows:
$$
\phi_3(w) = w + \widehat{\tau}(w - f(w)v) \sigma(f(w))v = (w - f(w)v) + (f(w) + \widehat{\tau}(w - f(w)v) \sigma(f(w)) v.
$$
As before, the second expression makes it clear that this is a diffeomorphism.  When $\widehat{\tau}(w - f(w)v) = 0$ then it is the identity.

This will do, but there are a few too many choices in the above.  To simplify these, we assume that $V$ admits a smooth inner product, $g$.  Let us write $q$ for the square of the associated norm.  Then we can choose $f$ to be evaluation of the inner product at $v$ and $\tau$ to be composition of the inner product with a suitable bump function on $\mathbb{R}$.  We shall write $\tau$ for that bump function.  To make the final formula cleaner, we assume that $\tau(t) = 1$ for $|t| \le 2$.  This leads us to:
$$
\begin{aligned}
\phi_v(w) &= w + \tau\left(\frac{q(w)}{1 + q(v)}\right) \sigma\left(\frac{g(w,v)}{q(v)}\right) v
&= w - \frac{g(w,v)}{q(v)}v + \left(\frac{g(w,v)}{q(v)} + \tau\left(\frac{q(w)}{q(v)}\right) \sigma\left(\frac{g(w,v)}{q(v)}\right) \right)v.
\end{aligned}
$$
As written, this makes sense only for $v \ne 0$.  But it extends to the identity at $v = 0$.  To see that this extension is smooth, we need merely point out that as $v \to 0$, so $q(v) \to 0$ and thus $\sigma\left(\frac{g(w,v)}{q(v)}\right) \to 0$.  The second expression again shows that, for $v \ne 0$, this is a diffeomorphism.

This, then, is our required linear diffeomorphism.  For $w$ with $q(w) \ge 2(1 + q(v))$ it is the identity, and thus will extend "at infinity", whilst $\phi_v(v) = 0$.

The next step is to extend this to a bundle over a manifold.  So let $\pi \colon E \to M$ be a smooth vector bundle over a smooth manifold.  We wish to extend the above formula so that it is valid for $E$.  That is, $v$ is an arbitrary point in $E$ and we wish to define $\phi_v \colon E \to E$ such that $\phi_v(v) = 0_{\pi(v)}$.  So also we must take $w$ to be an arbitrary point in $E$.  And thereby lies the problem: in the formula $v$ and $w$ interact but they may be in different fibres.  The solution is to extend one of them to a vector field.  Since $v$ is static in the formula for $\phi_v$, that is the obvious choice.

We should also note that the explicit formula requires the existence of a smooth [[orthogonal structure]] on $E$.

Thus we want to define a smooth function $X \colon E \to \Gamma(E)$ with the property that $X_v(\pi(v)) = v$.  This is easy if $E$ is trivial, and the condition is convex, so a standard [[partition of unity]] argument will suffice.  Specifically, let $\{\rho_\lambda : \lambda \in \Lambda\}$ be a partition of unity on $M$ with the property that for each $\lambda \in \lambda$ there is an open set $U_\lambda$ containing the support of $\rho_\lambda$ over which $E$ is trivial.  Let $E_\lambda$ denote the restriction of $E$ to $U_\lambda$ and let $\psi_\lambda \colon E_\lambda \to U_\lambda \times V$ be a trivialisation.  Let $p_\lambda \colon E_\lambda \to V$ be the composition of this trivialisation with the projection on to the $V$-factor.  We define $X_\lambda \colon E_\lambda \to \Gamma(E_\lambda)$ by
$$
X_{\lambda,v}(p) = \psi_\lambda^{-1}(p,p_\lambda(v)).
$$

Now we define $X \colon E \to \Gamma(E)$ by
$$
X_v(p) = \sum_\lambda \rho_\lambda(p) X_{\lambda,v}(p).
$$
Notice that $X_v(p) = 0$ if $p$ is "sufficiently far" from $\pi(v)$.

Thus our diffeomorphism $\phi_v$ at $w$, with $p = \pi(w)$, is:
$$
\phi_v(w) = \begin{cases} w + \tau\left(\frac{q(w)}{1 + q(X_v(p))}\right) \sigma \left(\frac{g(w,X_v(p))}{q(X_v(p))}\right) X_v(p) & X_v(p) \ne 0 \\
w & X_v(p) = 0 \end{cases}.
$$

## References

The idea goes back to 

* [[Andrew Stacey]], _The differential topology of smooth loops_ ([arXiv:math/0510097](http://arxiv.org/abs/math/0510097))
 {#Stacey}


The term _propagating flow_ was coined in 

* [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 {#Godin}

and used for the construction of [[umkehr maps]] to construct [[string topology]] operations.

