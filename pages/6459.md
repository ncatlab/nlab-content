<a id="DocStart"></a>

# Locally Kinematic Spaces # {: #title}

##### Andrew Stacey ##### {: #author}

* tic
{: toc}

+-- {: .num_section #sectiona }
=--
## Introduction ## {: .num_section}

The various categories of [[generalised smooth spaces]] were introduced to correct defects with the category of [[smooth manifolds]]. The category of manifolds, it is felt, is not big enough. There are things that behave like manifolds but which, for seemingly trivial reasons, are not considered as such: things like [[manifolds with corners]] or [[infinite dimensional manifolds]]. It is also relatively easy to break the structure of a manifold by doing things that most category theorists would regard as fairly trivial: taking subobjects, equalisers, and quotients being a few. So with the oft-heard cry of:   It is better to work in a nice category with some nasty objects than a nasty category with only nice objects;   people created various extensions of the category of smooth spaces to correct these limitations.

However, having built a suitable nice category, the "nice objects" (that is to say, the manifolds) are still inside it and it is a natural question as to how to identify these nice objects in amongst the nasty ones. The obvious answer is tautological: the manifolds are those objects that I first thought of. The real problem with this is that it is an external characterisation. A better characterisation would be one that could take an object from one of these categories and examine it purely within that category and conclude whether or not it was a manifold. This might lead to more things being called a manifold than were originally thought of, but should give a characterisation better knit to what a manifold actually is than just what happens to be our current best description thereof.

An example of this sort of result is [[Sta11](#citeStacey3), Proposition 8.3] where it was shown that in the category of [[Froelicher space|Frölicher spaces]], it is possible to *categorically* pick out $\mathbb{R}$.

The purpose of this page is to study a possible description of manifolds. The description is motivated by the construction of [[manifolds of smooth maps]]. A key component in constructing those spaces is that of a [[local addition]] on the target space. Therefore our first approximation is that of *locally additive* spaces, namely spaces that are equipped with a local addition.

The rough idea behind a local addition is simple. In any of the categories of [[generalised smooth spaces]], it is straightforward to define the notion of the tangent space at a point in a smooth space. Part of the data in a local addition says that near a point, the space is modelled on its tangent space. This would appear to instantly show that the space was locally Euclidean (or, at least, locally modelled on some vector space) except for the fact that tangent spaces are not automatically vector spaces.

The rest of the data in a local addition says that this modelling must vary smoothly over the space. This translates into the transition functions being smooth.

Thus a locally additive space is locally smoothly modelled in its tangent spaces. The key difference between this and the notion of a smooth manifold is that a locally additive space is somewhat tortoise-like in that it carries its model spaces around with it, rather than having them imposed from outside.

+-- {: .num_section #sectionb }
=--
## Definition ## {: .num_section}

We assume throughout that we have fixed upon one of the categories of [[generalised smooth space]].

The page [[local addition]] has the definition of a local addition for a smooth manifold. This is almost the same definition for us here, except that our underlying space is a generalised smooth space and we don't assume that the source is a vector bundle. We shall also work with the most precise version. Putting all of this together, we shall use the following definition.

+-- {: .num_defn #defna }
###### Definition ######
Let $X$ be a smooth space. A *local addition* on $X$ is a smooth map $\eta \colon T X \to X$ with the following properties: &nbsp;

1. <p></p>
   +-- {: .num_enuma #enumaZa }
   =--
   The composition of $\eta $ with the zero section is the identity on $X$,

1. <p></p>
   +-- {: .num_enuma #enumaZb }
   =--
   There is an open neighbourhood, say $V$, of the diagonal in $X \times X$ such that $\pi \times \eta \colon T X \to X \times X$ induces a diffeomorphism with image $V$, and

1. <p></p>
   +-- {: .num_enuma #enumaZc }
   =--
   For $x \in X$, the composition
   $$
   T_{x} X \xrightarrow[\cong ]{} T_{0} T_{x} X \xrightarrow[\cong ]{d\eta } T_{x} X
   $$
   is the identity.
=--

From this definition, that of a locally additive space is obvious.

+-- {: .num_defn #defnb }
###### Definition ######
A *locally additive space* is a pair $(X, \eta )$ where $X$ is a smooth space and $\eta $ is a local addition on $X$.
=--

Although the obvious definition, as it stands it is not quite precise. This is because the various notions of [[tangent space]] diverge once one goes outside the realm of smooth manifolds. In this article, we shall use the [[kinematic tangent space]]. To allow other notions based on other definitions of tangent space, we use the notion *locally kinematic space* for a locally additive space where the tangent space used is the kinematic version.

The other part of the definition that needs pinning down is the notion of an *open neighbourhood*. This requires that we supply our smooth spaces with a topology. Some definitions have a topology built in, and those that do not can be supplied with at least one suitable topology. We shall not prescribe the exact topology but rather assume that a method of supplying a smooth space with a topology has already been decided upon. The only properties that we require are the following:

1. <p></p>
   +-- {: .num_enumb #enumbZa }
   =--
   The assignment of a topology to a smooth space is functorial, and

1. <p></p>
   +-- {: .num_enumb #enumbZb }
   =--
   The topology on $\mathbb{R}$ is the standard one.     These both seem quite reasonable! In fact, these two conditions define a particular topology which we refer to as the [[curvaceous topology]]: it is the strongest topology for which these two statements are true.

The really important property of the local addition is that it allows us to lift tangent vectors to curves. Of course, we can always do this for a single tangent vector (as we are using the kinematic tangent space) but a local addition allows us to do it for a family. As a direct consequence of this lifting, we get the following simple result. Recall that for the [[kinematic tangent space]] at a point there are potentially two smooth structures: the quotient structure and the fibre structure. The lifting property of a locally additive space implies that these two are the same.

+-- {: .num_lemma #lemmaa }
###### Lemma ######
Let $(X,\eta )$ be a locally kinematic space. For $x \in X$, the two smooth structures on $T_{x} X$ agree. That is, $T_{x} X \to T X$ is an embedding.
=--

+-- {: .proof }
Let us write $T_{x} X$ for the tangent space at $x$ and $(T X)_{x}$ for the fibre of $T X$ at $x$.

We define a map $T X \to C^{\infty } (\mathbb{R},X)$ by sending $v \in T X$ to the curve $t \mapsto \eta (t v)$. This is smooth and splits the quotient $C^{\infty } (\mathbb{R},X) \to T X$. It is also fibre-preserving, and so maps $(T X)_{x}$ in to $C^{\infty } ((\mathbb{R},0), (X,x))$. Composing with the quotient, we obtain a map $(T X)_{x} \to T_{x} X$ inverse to the given map $T_{x} X \to (T X)_{x}$.
=--

+-- {: .num_section #sectionc }
=--
## Mapping Spaces ## {: .num_section}

The motivation for locally kinematic spaces comes from considering mapping spaces. All of the categories of [[generalised smooth space]] are cartesian closed. This means that for $S$ and $X$ smooth spaces, the set of smooth maps $C^{\infty } (S,X)$ is again a smooth space. This construction is functorial and satisfies lots of nice properties.

Let $X$ be a locally kinematic space, with local addition $\eta $, and let $V \subseteq X \times X$ be the corresponding neighbourhood of the diagonal, so that $\pi \times \eta $ is a diffeomorphism on to $V$. Then simply by functorality, we see that $C^{\infty } (S,\eta )$ is a diffeomorphism from $C^{\infty } (S, T X)$ to $C^{\infty } (S, V)$. Moreover, $C^{\infty } (S, V)$ is a subset of $C^{\infty } (S, X \times X)$ which is diffeomorphic to $C^{\infty } (S,X) \times C^{\infty } (S,X)$ and $C^{\infty } (S,V)$ contains the diagonal. That $C^{\infty } (S,\pi \times \eta ) = C^{\infty } (S,\pi ) \times C^{\infty } (S,\eta )$ takes the zero section of $C^{\infty } (S, T X)$ to the diagonal is obvious. Hence $C^{\infty } (S,\eta )$ is almost a local addition on $C^{\infty } (S,X)$. There are two pieces missing:

1. <p></p>
   +-- {: .num_enumc #enumcZa }
   =--
   A natural isomorphism $C^{\infty } (S,T X) \cong T C^{\infty } (S, X)$.

1. <p></p>
   +-- {: .num_enumc #enumcZb }
   =--
   That $C^{\infty } (S,V)$ is an open neighbourhood of the diagonal in $C^{\infty } (S, X \times X)$.

As we are using the [[kinematic tangent space]], there is always a natural *transformation* relating to the first piece. The locally additive structure allows us to construct the inverse.

+-- {: .num_lemma #lemmab }
###### Lemma ######
For $X$ a locally additive space, the natural transformation
$$
TC^{\infty } (S, X) \cong C^{\infty } (S, T X)
$$
is a natural isomorphism
=--

+-- {: .proof }
We need to define an inverse for this map. This starts by defining a lift from $C^{\infty } (S, T X)$ to $C^{\infty } (S, C^{\infty } (\mathbb{R},X))$. This map is defined as follows. Let $\alpha \in C^{\infty } (S, T X)$. Define $\mathbb{R} \times S \to X$ by:
$$
(t,s) \mapsto \eta (t \alpha (s))
$$
where $t \alpha (s)$ uses the $\mathbb{R}$-action on $T X$. Using the adjunction between mappings and products, this defines a curve in $C^{\infty } (S,X)$ and thus, by quotienting, a tangent vector in $C^{\infty } (S,X)$ based at $s \mapsto \eta (0 \alpha (s)) = \alpha (s)$.

To show that this is the required inverse, we need to evaluate the resulting tangent vector at some $s \in S$. This leads to the curve $t \mapsto \eta (t \alpha (s))$ in $X$. Under the natural isomorphism $T_{0} T_{x} X \cong T_{x} X$, the curve $t \mapsto t \alpha (s)$ has derivative (at $0$) $\alpha (s)$ again. Thus we have the image of this under $d \eta \colon T_{0} T_{x} X \to T_{x} X$ which is just $\alpha (s)$ again.

Thus we have the required inverse.
=--

This result is the mathematics behind the statement above that a local addition allows us to lift families of tangent vectors to curves.

The second missing piece is a little harder to pin down because without knowing precisely which category of smooth spaces we are working in, we will find it hard to know exactly how to define the topology on a smooth space, and thus to know how to work with it. Thus rather than a detailed study of when this occurs, we shall adopt the mathematician's defence.

+-- {: .num_defn #defnc }
###### Definition ######
A smooth space $S$ is said to be *smoothly compact* if whenever $U \subseteq X$ is open then $C^{\infty } (S,U)$ is open in $C^{\infty } (S,X)$.
=--

With that in place, we can now fill in the missing pieces.

+-- {: .num_theorem #theorema }
###### Theorem ######
Let $X$ be a locally kinematic space and $S$ a smoothly compact space. Then $C^{\infty } (S,X)$ is again a locally kinematic space.

The tangent space of $C^{\infty } (S,X)$ at $\alpha \colon S \to X$ consists of all maps $\beta \colon S \to T X$ such that $\pi \beta = \alpha $.
=--

+-- {: .num_section #sectiond }
=--
## Local Structure ## {: .num_section}

Having a local addition means that the smooth space is locally modelled on its tangent spaces. It turns out that this also puts some restrictions on what those tangent spaces look like.

+-- {: .num_theorem #theoremb }
###### Theorem ######
Let $X$ be a locally kinematic space. Then for $x \in X$, the tangent space $T_{x} X$ is a vector space.
=--

+-- {: .proof }
As shown at [[local addition]], the only thing missing on $T_{x} X$ of the vector space structure is the addition. We have the zero vector, scalar multiplication, and that the identities of a vector space are satisfied whenever everything is defined. So we need to define the sum, $u + v$, of two vectors $u, v \in T_{x} X$. To define this sum we define a map $W \to X$ where $W \subseteq \mathbb{R} ^{2}$ is a neighbourhood of the origin, such that $\partial _{t}$ maps to $v$ and $\partial _{s}$ to $u$. Then the image of $\partial _{s} + \partial _{t}$ will be the required sum.

Let $\eta \colon T X \to X$ be the local addition and let $V \subseteq X \times X$ be the corresponding neighbourhood of the diagonal. Consider the curve $t \mapsto (\eta (t v), \eta (u))$. At time $t = 0$, this is at $(x,\eta (u))$ which lies in $V$. There is, therefore, some interval $(-\epsilon ,\epsilon )$ for which $(\eta (t v), \eta (u)) \in V$. Since $(\pi \times \eta ) \colon T X \to V$ is a diffeomorphism, we can apply the inverse of this to that path, resulting in:
$$
(\pi \times \eta )^{-1} (\eta (t v), \eta (u)) \in T_{\eta (t v)} X.
$$
This is a tangent vector moving along the curve $\eta (t v)$ starting at $u$ above $x$. As this is, in totality, a curve of tangent vectors we can scale them. Thus we define a map:
$$
\mathbb{R} \times (-\epsilon ,\epsilon ) \to T X, \quad (s,t) \mapsto s \cdot (\pi \times \eta )^{-1} (\eta (t v), \eta (u)).
$$
The final step is to map this back down to $X$ via $\eta $:
$$
(s,t) \mapsto \eta (s \cdot (\pi \times \eta )^{-1} (\eta (t v), \eta (u))).
$$
Let us write this as $\tau \colon \mathbb{R} \times (-\epsilon ,\epsilon ) \to X$ for short. We note that it is smooth, as it is a composition of smooth maps.

It may aid the   comprehension of this map if we describe it in the case of $\mathbb{R} ^{2}$ with $u = \partial _{x}$ and $v = \partial _{y}$. In this case, $\tau $ is the map $(s,(1 - s)t)$. Thus
$$
D_{(0,0)} \tau   = \left . \begin{bmatrix}   (1 - s) & -t \\   0 & 1 \end{bmatrix} \right |_{(0,0)} = \begin{bmatrix}   1 & 0 \\   0 & 1 \end{bmatrix}.
$$
At $s = 0$, we   have the curve:
$$
t \mapsto \eta   (0 \cdot (\pi \times \eta )^{-1} (\eta (t v), \eta (u))).
$$
Under $\eta $,   the zero section maps to the "foot" of the tangent space, which is also $\pi $ of the vector. Thus the path is $t \mapsto \eta (t v)$. Hence the image of $\partial _{t}$ is $v$.

At $t = 0$, we have the curve:
$$
s \mapsto \eta (s \cdot (\pi \times \eta )^{-1}(x, \eta (u)))
$$
since $\eta (0 v) = x$. Unravelling this, we get $s \mapsto \eta (s u)$. Hence the image of $\partial _{s}$ is $u$.

Then the claim is that the image of $\partial _{s} + \partial _{t}$ will do for $u + v$. To see this, consider a smooth function $f \colon X \to \mathbb{R} $. The composition $f \circ \tau $ is smooth, and so we have that:
$$
f(u) + f(v) = (f \circ \tau )(\partial _{s}) + (f \circ \tau )(\partial _{t}) = (f \circ \tau )(\partial _{s} + \partial _{t}) = f(\tau _{*}(\partial _{s} + \partial _{t})).
$$
Hence $\tau _{*}(\partial _{s} + \partial _{t})$ is the sum $u + v$.
=--

Thus a locally additive space is modelled on vector spaces. This is not quite as strong as saying that it is a smooth manifold (even ignoring paracompactness and Hausdorff) since we do not know that the smooth structure on a tangent space is "the" smooth structure on a vector space.

+-- {: .num_section #sectione }
=--
## Related Concepts ## {: .num_section}

A similar concept to this was devised and studied by Kriegl and Michor in [Mic84a](#citeMR764972), [Mic84b](#citeMR767683). The key difference between these two approaches is that of the starting point. The goal of Kriegl and Michor's construction was to devise a cartesian closed category of manifolds, starting from almost nothing. Thus they had to build the notions of "smooth map" and of "tangent bundle" in to the foundations. Our goal is to identify manifold-like objects inside a category of smooth spaces. Thus we already know what is a "smooth map" and how to construct the "tangent bundle". Nonetheless, there are similarities in the approaches: both are particularly suited to mapping spaces, and both have "path lifting" at their core.

Another concept that should be kept in mind with regard to the above is that of the [[tangent microbundle]] of a topological manifold. This is an equivalence class of neighbourhoods of the diagonal. Thus one can say that a locally additive space is one for which the topological and smooth tangent bundles agree.
## References ##

* {: #citeMR764972} **Mic84a** Peter Michor. A convenient setting for differential geometry and global analysis. Cahiers Topologie G&eacute;om. Diff&eacute;rentielle, 25:63A109, 1984.

* {: #citeMR767683} **Mic84b** Peter Michor. A convenient setting for differential geometry and global analysis. II. Cahiers Topologie G&eacute;om. Diff&eacute;rentielle, 25:113A178, 1984.

* {: #citeStacey3} **Sta11** A.&nbsp;Stacey. Comparative smootheology. TAC, 25:64-117, 2011, http://www.tac.mta.ca/tac/volumes/25/4/25-04abs.html. arXiv:0802.2225v2.
