
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Mapping space
+-- {: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The notion of the _smooth loop space_ of a (smooth) [[smooth manifold|manifold]] is a way to make the set of smooth maps from the [[circle]] to the target manifold into an object amenable to the tools of [[differential topology]].

Let $M$ be a [[smooth manifold|smooth finite dimensional manifold]].  Then the set of smooth maps $S^1 \to M$ is not usefully the underlying set of a finite dimensional manifold.  Therefore to make it into an object that can be studied in differential topology, one has to allow for smooth spaces other than finite dimensional smooth manifolds.  That is to say, one has to work in a larger category than just that of finite dimensional smooth manifolds.

If the category is [[cartesian closed]] then the smooth loop space of a smooth space, say $X$, is simply the result of applying the [[internal hom]] functor with that space as target and the circle as source:
$$
  L X \coloneqq [S^1, X]
$$
(This is the smooth [[free loop space]]; for the smooth [[based loop space]] one applies the standard restriction.)

There are a variety of suitable categories listed at [[generalized smooth spaces]].

The categories of smooth spaces discussed at [[generalized smooth spaces]] are all cartesian closed and thus all admit smooth loop spaces of all objects.
However, by restricting to a subcategory that might not be cartesian closed (for example, finite dimensional smooth manifolds) one can ask for another subcategory that is large enough to contain all the resulting smooth loop spaces.  For finite dimensional smooth manifolds it turns out that one can give their smooth loop spaces the structure of an infinite dimensional [[Fréchet manifold]].

Depending on taste and application, certain smooth [[quotient objects]] of this free loop space may be and are often considered. 

## Properties


### Fr&#233;chet manifold structure on $[S^1,X]$ for $X$ a manifold
 {#FrechetManifoldStructure}

In this section, we will describe the structure of a 
smooth loop space of a smooth manifold
as a Fr&#233;chet manifold in detail.  The construction is quite standard, and a partial list of references and further reading can be found at the end of this page.

We start with a [[smooth manifold]], $M$, of dimension $n$.  Note that here manifolds definitely do not have a boundary.  For simplicity, we assume that it is orientable.  The point of this assumption is that it allows us to identify the model space of $L M$ with the Fr&#233;chet space $L \mathbb{R}^n = C^\infty (S^1, \mathbb{R}^n)$.  In the unorientable case, some components would have this as model space whereas others would have a _twisted_ version of this space.

The key piece of structure needed on $M$ is that of a [[local addition]], $\eta \colon T M \to M$.

Let $\eta \colon T M \to M$ be a local addition on $M$.  Let $V \subseteq M \times M$ be the image of the map $\pi \times \eta \colon T M \to M \times M$.  Although (as yet) we know nothing about the topologies of $L T M$ or of $L V$, we can at least say that the looped map, $(\pi \times \eta)^L \colon L T M \to L V$, is a bijection.

+-- {: .num_lemma #lemcharts}
###### Lemma
Let $\alpha \in L M$.  Define the set $U_\alpha \subseteq L M$ by:

$$
U_\alpha \coloneqq \{ \beta \in L M : (\alpha, \beta) \in L V\}.
$$

Then the preimage of $\{\alpha\} \times U_\alpha$ under $(\pi \times \eta)^L$ is naturally identified with $\Gamma_{S^1}(\alpha^* T M)$.  In particular, the zero section of $\alpha^* T M$ maps to $(\alpha, \alpha) \in \{\alpha\} \times U_\alpha$.
=--

+-- {: .proof}
###### Proof
We claim that there is a diagram:

$$
\begin{matrix}
L T M &\overset{(\pi \times \eta)^L}{\to} & L V \\
\uparrow & & \uparrow\mathrlap{\beta \mapsto (\alpha,\beta)} \\
\Gamma_{S^1}(\alpha^* T M) & & U_\alpha
\end{matrix}
$$

such that the bijection at the top takes the image of the left-hand vertical map to the image of the right-hand one.  Both of the vertical maps are injective - the right-hand one obviously so, we shall investigate the left-hand one in a moment - and thus the bijection $(\pi \times \eta)^L$ induces a bijection from the lower-left to the lower-right.

The left-hand vertical map, $\Gamma_{S^1}(\alpha^* T M) \to L T M$, is defined as follows: the total space of $\alpha^* T M$ is:

$$
\big\{(t, v) \in S^1 \times T M : \alpha(t) = \pi(v) \big\}.
$$

It is an embedded submanifold of $S^1 \times T M$.  Therefore, a map into $\alpha^* T M$ is smooth if and only if the compositions with the projections to $S^1$ and to $T M$ are smooth.  Now a map $S^1 \to \alpha^* T M$ is a section if and only if it projects to the identity on $S^1$.  Therefore, there is a bijection (of sets):

$$
\begin{aligned}
\Gamma_{S^1}(\alpha^* T M) &\cong \big\{ \beta \in L T M : (t, \beta(t)) \in \alpha^* T M\; \text{for all}\; t \in S^1\big\} \\
 &\cong \big\{ \beta \in L T M : \alpha(t) = \pi \beta(t) \text{for all}\; t \in S^1\big\} \\
 &\cong \big\{ \beta \in L T M : \pi^L \beta = \alpha \big\} &\eqcolon L_\alpha T M
\end{aligned}
$$

In particular, the map $\Gamma_{S^1}(\alpha^* T M) \to L T M$ is injective.

We apply $(\pi \times \eta)^L$ to the defining condition for $L_\alpha T M$ and see that $L_\alpha T M$ is the preimage under this map of everything of the form $(\alpha, \gamma)$ in $L V$.  By construction, $\gamma \in L M$ is such that $(\alpha, \gamma) \in L V$ if and only if $\gamma \in U_\alpha$.  Hence $(\pi \times \eta)^L$ identifies $L_\alpha T M$ with $\{\alpha\} \times U_\alpha$.

Finally, note that the zero section of $\alpha^* T M$ maps to the image of $\alpha$ under the zero section of $T M$.  Since $\eta$ composed with the zero section of $T M$ is the identity on $M$, the image under the zero section of $\alpha^* T M$ in $V$ is $(\alpha, \alpha)$ as required.
=--

The resulting map, let us write it $\Psi_\alpha \colon \Gamma_{S^1}(\alpha^* T M) \to U_\alpha$, has the following concrete description.  Let $\beta \colon S^1 \to \alpha^* T M$ be a section and let $\tilde{\beta} \colon S^1 \to T M$ be the corresponding loop in $T M$ (so that $\beta(t) = (t, \tilde{\beta}(t))$ when viewing $\alpha^* T M$ as a submanifold of $S^1 \times T M$).  Then $(\pi \times \eta)^L (\tilde{\beta}) = (\alpha, \eta^L (\tilde{\beta}))$ so $\Psi_\alpha(\beta) = \eta^L (\tilde{\beta})$.

As we have assumed $M$ to be orientable, $\alpha^* T M$ can be trivialised.  A smooth such trivialisation defines a linear homeomorphism $\Gamma_{S^1}(\alpha^* T M) \cong L \mathbb{R}^n$.  We use this to impose a smooth structure on $\Gamma_{S^1}(\alpha^* T M)$, noting that any two such trivialisations induce the same structure.

To investigate the transition functions, we need two loops.  In fact, let's have two of everything.

+-- {: .num_proposition #transition}
###### Proposition
Let $\eta_1, \eta_2 \colon T M \to M$ be local additions with corresponding neighbourhoods $V_1$, $V_2$ of the diagonal in $M \times M$.  Let $\alpha_1$, $\alpha_2$ be smooth loops in $M$.  Let $\Psi_1 \colon \Gamma_{S^1}(\alpha_1^* T M) \to U_1$ and  $\Psi_2 \colon \Gamma_{S^1}(\alpha_2^* T M) \to U_2$ be the corresponding maps defined as above.

The transition function:

$$
\Psi_{1 2} \coloneqq \Psi_1^{-1} \Psi_2 \colon \Psi_1^{-1}(U_1 \cap U_2) \to \Psi_2^{-1}(U_1 \cap U_2)
$$

is a diffeomorphism.
=--

+-- {: .proof}
###### Proof
We start by characterising the space $\Psi_1^{-1}(U_1 \cap U_2)$ within $\Gamma_{S^1}(\alpha_1^* T M)$.
Let $W_{1 2} \subseteq \alpha_1^* T M$ be the set:
$$
\big\{ (t,v) \in \alpha_1^* T M : (\alpha_2(t), \eta_1(v)) \in V_2\big\}.
$$

Note that this is open in $\alpha_1^* T M$ as it is the preimage of the open set $V_2$ by the continuous map $\alpha_2 \times \eta_1$.

Let $\gamma \in \Gamma_{S^1}(\alpha_1^* T M)$ and let $\tilde{\gamma} \in L T M$ be the image of $\gamma$ (so that $\gamma(t) = (t, \tilde{\gamma}(t))$.  Then $\gamma(t) \in W_{1 2}$ for all $t$ if and only if $(\alpha_2(t), \eta_1(\tilde{\gamma}(t))) \in V_2$ for all $t$.  That is to say, if and only if $(\alpha_2, \eta_1^L(\tilde{\gamma})) \in L V_2$.  This is precisely the condition that $\eta_1^L(\tilde{\gamma}) \in U_2$.  Since $\eta_1^L(\tilde{\gamma}) = \Psi_1(\gamma)$, we see that $\gamma$ takes values in $W_{1 2}$ if and only if $\Psi_1(\gamma) \in U_2$.  Since $\operatorname{Im} \Psi_1 = U_1$, we conclude that $\Gamma_{S^1}(W_{1 2}) = \Psi_1^{-1}(U_1 \cap U_2)$.

Let us define $W_{2 1} \subseteq \alpha_2^* T M$ similarly.  The idea of the proof that $\Phi_{1 2}$ is a diffeomorphism is to show that it is induced by a diffeomorphism $W_{1 2} \cong W_{2 1}$.

Let $\theta_1 \colon W_{1 2} \to T M$ be the map:
$$
\theta_1(t,v) = (\pi \times \eta_2)^{-1}(\alpha_2(t), \eta_1(v)).
$$
The definition of $W_{1 2}$ ensures that $(\alpha_2(t) ,\eta_1(v)) \in V_2$ for $(t,v) \in W_{1 2}$ and this is the image of $\pi \times \eta_2$.  Hence $\theta_1$ is well-defined.  Define $\theta_2 \colon W_{2 1} \to T M$ similarly.  These are both smooth maps.

Notice that $\pi(\pi \times \eta_i)^{-1} \colon V_i \subseteq M \times M \to M$ is the projection on to the first factor and $\eta_i(\pi \times \eta_i)^{-1} \colon V_i \to M$ is the projection on to the second.  Thus $\pi \theta_1(t,v) = \alpha_2(t)$.  Hence $\theta_1 \colon W_{1 2} \to T M$ is such that $(t, \theta_1(t,v)) \in \alpha_2^* T M$ for all $(t,v) \in W_{1 2}$.  Then:

$$
(\alpha_1(t), \eta_2(\theta_1(t,v))) = (\alpha_1(t), \eta_1(v)) \in V_1
$$

so $(t, \theta_1(t,v)) \in W_{2 1}$.  Hence we have a map $\phi_{1 2} \colon W_{1 2} \to W_{2 1}$ given by:

$$
\phi_{1 2}(t, v) = (t, \theta_1(t,v)).
$$

Similarly we have a map $\phi_{2 1} \colon W_{2 1} \to W_{1 2}$.  These are both smooth since the composition with the inclusion into $S^1 \times T M$ is smooth.

Consider the composition $\phi_{2 1}\phi_{1 2}(t,v)$.  Expanding this out yields:

$$
\begin{aligned}
\phi_{2 1} \phi_{1 2}(t,v) &= \phi_{2 1}(t, \theta_1(t,v))\\
&=(t, \theta_2(t,\theta_1(t,v))) \\
&=(t, (\pi \times \eta_1)^{-1}(\alpha_1(t), \eta_2(\theta_1(t,v)))) \\
&= (t, (\pi \times \eta_1)^{-1}(\alpha_1(t), \eta_1(v))) \\
&= (t, (\pi \times \eta_1)^{-1}(\pi(v), \eta_1(v))) \\
&= (t,v)
\end{aligned}
$$

The penultimate line is because $(t,v) \in \alpha_1^* T M$ so $\pi(v) = \alpha_1(t)$.  Hence $\phi_{2 1}$ is the inverse of $\phi_{1 2}$ and so $\phi_{1 2}$ is a diffeomorphism.  Thus the map $\phi_{1 2}^L$ is a diffeomorphism from $\Psi_1^{-1}(U_1 \cap U_2)$ to $\Psi_2^{-1}(U_1 \cap U_2)$.  We just need to show that this is the transition function.  To do this, we show that $\Psi_2 \psi_{1 2}^L = \Psi_2 \Phi_{1 2}$.  The right-hand side is, by definition, $\Psi_1$ which satisfies:

$$
\Psi_1(\gamma)(t) = \eta_1(\tilde{\gamma})(t).
$$

On the other side,

$$
\begin{aligned}
\phi_{1 2}^L (\gamma)(t) &= \phi_{1 2}(\gamma(t)) \\
= (t, \theta_1(t, \tilde{\gamma}(t))) \\
= (t, (\pi \times \eta_2)^{-1}(\alpha_2(t), \eta_1(\tilde{\gamma}(t)))).
\end{aligned}
$$

Hence

$$
\Psi_2 \phi_{1 2}^L(\gamma)(t) = \eta_2(\pi \times \eta_2)^{-1}(\alpha_2(t), \eta_1(\tilde{\gamma}(t))) = \eta_1(\tilde{\gamma})(t).
$$

Thus $\phi_{1 2}^L = \Phi_{1 2}$ and so the transition functions are diffeomorphisms.
=--

+-- {: .num_remark #extension}
###### Remark
This construction easily generalises quite widely.  Very little of the  structure of $S^1$ was used at all: that mainly came in in the smooth structure of $L \mathbb{R}^n$.  The key structure of $M$ was the local addition and thus one could regard this as a construction of [[locally additive space|locally additive spaces]].  For more on the possible extensions, see the references.
=--

### Relation between Fr&#233;chet-manifold structure and diffeological structure
 {#SmoothStruc}

For $X$ a [[smooth manifold]], the [[Fréchet manifold]] structure on $L X$, discussed [above](#FrechetManifoldStructure) 
agrees with the standard [[mapping space]] [[diffeological space|diffeology]] on $L X$ in the following sense.

There is a [[functor]]

$$
  F: Frech \to Diff
$$

from [[Frechet manifold|Fréchet manifold]]s to [[diffeological spaces]] defined in the same way as the well-known functor from [[smooth manifold]]s to [[diffeological space]]s: a plot is precisely a smooth map $c : U \to L X$, where $U$ is an object in the domain category, e.g. an open subset of some $\mathbb{R}^n$.

(Notice that a theorem of M. Losik says that the functor F is [[full and faithful functor|full and faithful]], just like that including manifolds into diffeological spaces!)

Now there are two diffeologies on $L X$: this is the structure of a [[sheaf]] on the category [[CartSp]] obtained as regarding $L X$ as the [[internal hom]] with respect to the [[closed monoidal structure on sheaves]]

$$
  L X = [S^1,X] : U \mapsto Hom_{Sh(CartSp)}(S^1 \times Y(U), X)
$$

(where $Y$ denotes the [[Yoneda embedding]]).

This means that a map $c : U \to L X$ is a plot if and only if the associated map $U \times S^1 \to X$ is smooth. The second diffeology is the one obtained from the functor $F$.

These two diffeologies _coincide_  -- in the sense that every plot of one is a plot of the other. In particular, they have the same sets of smooth functions.

A detailed proof of this is in ([Waldorf, lemma A.1.7](#Waldorf)) 


### $G$-Structures on smooth loop spaces
 {#GStructures}

The usual notions of _[[G-structures]]_ for [[manifolds]], such as [[orientation]], [[spin structure]], [[string structure]], etc. do not carry over directly to their smooth loop spaces, but they are closely related by [[transgression]]: a [[spin structure]] on $X$ is supposed to induce a kind of orientation structure on $\Omega X$, a string structure on $X$ is supposed to induce a kind of spin structure on $\Omega X$.

Formalizations of such "smooth loop space $G$-structures" have been proposed in  ([Stolz-Teichner 2005](#Stolz)), ([Waldorf 2010](#Waldorf10))  and ([Waldorf 2012](#Waldorf12)). In particular an equivalence between spin structures on smooth loop space and [[string structure]] on the underlying space is discussed in ([Waldorf 14](#Waldorf14)).



### As the loop space object of the smooth path groupoid 
 {#AsLoopObj}

Given the notion of the smooth [[path groupoid]] $\mathcal{P}_1(X)$ of the smooth space $X$, we may think of the smooth loop _space_ as the corresponding [[loop space object]].

We say this in detail now.

#### Recollection of the situation in $Top$

First briefly recall the situation for [[topological space]]s and their [[loop space object]]s, which are the topological [[loop space]]s:

The ordinary procedure is that we regard a [[topological space]] as an [[object]] in the [[(∞,1)-category]] [[Top]] and produce its [[loop space]] at a chosen [[pointed object|base point]] $x : {*} \to X$ as the [[limit in a quasi-category|(∞,1)-pullback]] of the base point along itself:

$$
  \array{
    \Omega_x X &\to& {*}
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{x}}
    \\
    {*} &\stackrel{x}{\to}& X
  }
  \,.
$$

**In words** this is the simple statement that $\Omega_x X$ is the space of all [[homotopy|homotopies]] in the [[(∞,1)-category]] [[Top]] from the map $x : {*} \to X$ to itself. Any one such homotopy is itself a continuous map $\gamma : I \to X$ from the [[interval object|standard interval]] $I = [0,1]$ to $X$, such that restricted to its endpoints it produces the map $x$. Clearly, these are precisely the loops in $X$, based at $x$.

#### Generalization to $\infty$-Lie groupoids

You might think: well, now let $X \in Sh_{(\infty,1)}(Diff)$ be a [[smooth manifold]] regarded as a [[representable functor|representable]] object in the [[(∞,1)-category of (∞,1)-sheaves]] of [[∞-stack]]s on [[Diff]] or maybe better in $Sh_{(\infty,1)}(CartSp)$ on [[CartSp]] -- i.e. of [[Lie ∞-groupoid]]s -- , we play the same trick and compute the [[homotopy pullback]] $Q$

$$
  \array{
    Q &\to& {*}
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{x}}
    \\
    {*} &\stackrel{x}{\to}& X
  }
  \;\;\;\;\;\;\;\;\;\;\;\;
  \in Sh_{(\infty,1)}(CartSp)
$$

to obtain the smooth loop space. But it doesn't: the $Q$ here is $Q = {*}$! That's because $X$ regarded as a representable object in $Sh_{(\infty,1)}(Diff)$ is really a [[discrete category|categorically discrete]] [[Lie groupoid]]: it has a smooth space $X$ of objects, but no nontrivial morphisms. And the "homotopies" in the [[homotopy pullback]] are homotopies as seen by the _[[morphisms]]_ in $X$. There is just the identity morphism in $X$ going from ${*} \to X$ to itself, so the homotopy pullback is the point.

Why then did it work in [[Top]]? Because, if you look closely, there really we did something different! Regarded as an [[(∞,1)-category]], [[Top]] is really the collection of [[∞-stack]]s _on the point_ :

$$
  Sing : Top \stackrel{\simeq}{\to} Sh_{(\infty,1)}({*})
  \,.
$$

Under this identification, a topological space is _not_ identified with a [[representable functor|representable]] object! The only representable object in $Sh_{(\infty,1)}({*})$ is of course the [[point]] itself, the [[terminal object]]. Instead, as the notation above already suggests, under this identification a topological space is really identified with its _singular simplicial complex_ $Sing(X)$. But that's really to be thought of as the topological [[fundamental ∞-groupoid]] of $X$. We should write

$$
  \Pi(X) = Sing(X) = Hom_{Top}(\Delta^\bullet_{Top},X) \in SSet
$$

instead of $X$ when we regard the topological space $X$ as an object of the [[(∞,1)-category]] of topological spaces! For more on this, see the discussion at [[homotopy hypothesis]].

If instead we had interpreted the topological space $X$ as a representable object, hence as a [[discrete category|categorically discrete]] object in the $(\infty,1)$-category of [[topological ∞-groupoid]]s, we would have seen the same phenomenon as for the smooth $X$ above: its [[loop space object]] would have been the point.
From this perspective now it is clear how the abstract notion of [[loop space object]] corresponds to the geometrically expected one: for a geometric [[space]] $X$, its loop space is the [[loop space object]] of its [[fundamental ∞-groupoid]].

This statement can be given sense in all contexts where the underlying [[topos]] of our ambient [[(∞,1)-topos]] of [[space]]s is a [[lined topos]]: we need to know which object $R$ is the standard _line_ or [[interval object]]. This determines the _geometric paths_ in a space. Taking these geometric paths to be the [[morphism]]s of a [[fundamental ∞-groupoid]] then makes the geometric paths into "categorical paths", i.e. into morphisms. These then are what the abstract definition of [[loop space object]] can see.

And indeed, whenever the underlying [[topos]] of [[space]]s that we are looking at is a [[lined topos]] the corresponding [[(∞,1)-topos]] comes equipped with a generalization of the topological [[fundamental ∞-groupoid]] construction: we can associate to every [[space]] $X$ its
[[schreiber:path ∞-groupoid]] $\Pi(X)$: the morphisms of $\Pi(X)$ are given by paths in $X$ as seen by the given [[interval object]] $I$. All entirely analogous to the familiar situation for [[Top]], only that now we are testing our generalized [[space]]s over test objects in an arbitrary [[site]] and are using a correspondingly different notion of [[interval object]].

#### The concrete definition

So for $X$ a [[smooth manifold]], regarded as a representable object in the [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$ of [[Lie ∞-groupoid]]s we have now that the homotopy pullback of any point ${*} \to X \hookrightarrow \Pi(X)$ along itself in the [[schreiber:path ∞-groupoid]] $\Pi(X)$ does indeed produce the expected [[Lie ∞-groupoid]] $\Omega_x X$  in 

$$
  \array{
    \Omega_x X &\to& {*}
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{x}}
    \\
    {*} &\stackrel{x}{\to}& \Pi(X)
  }
  \;\;\;\;\;\;\;\;\;\;\;\;
  \in Sh_{(\infty,1)}(CartSp)
$$

whose

* smooth space of objects is the smooth space of smooth loops in $X$ based at $x$;

* smooth space of morphisms is the smooth space of smooth $I$-homotopies between smooth loops in $X$

* etc;

Here we want not the full loop [[∞-groupoid]], but just some sort of truncation to a [[0-category|0-groupoid]] just of loops. There are several choices for how exactly to do this, depending on which higher morphisms we just discard, and which we use to identify 1-morphisms. Whatever we do, we end up with some notion of smooth [[path groupoid]] $\mathcal{P}_1(X)$ of $X$, whose 1-morphisms are certain smooth quotient space of the smooth space of 1-morphisms in $\Pi(X)$.

Then, accordingly, forming the [[loop space object]] of this [[path groupoid]] $\mathcal{P}_1(X)$ yields the smooth space $LoopSpace(X)$

$$
  \array{
    LoopSpace_x(X) &\to& {*}
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{x}}
    \\
    {*} &\stackrel{x}{\to}& \mathcal{P}_1(X)
  }
$$

which is the smooth subspace of the smooth space of morphisms in $\mathcal{P}_1(X)$ of those morphisms that start and end at $x$.

When unwrapping what all this means, one sees that the object $LoopSpace_x(X) \in Sh_{(\infty,1)}(CartSp)$ that we obtain this way is nothing but the image under the embedding $Sh(CartSp) \hookrightarrow Sh_{(\infty,1)}(CartSp)$ of ordinary [[sheaf|sheaves]] into $\infty$-stacks of some [[quotient object|quotient]] of the [[internal hom]] $[I,X]$ in the [[closed monoidal structure on sheaves]]. Being an internal hom of representables, this is a [[concrete sheaf]] and as such it is precisely the smooth loop space regarded as a [[diffeological space]].

## Related concepts

* [[Dirac operator on smooth loop space]]

* [[Dirac-Ramond operator]], [[Witten genus]]

* [[free loop orbifold]], [[inertia orbifold]]

* [[loop space]], [[free loop space]]

## References

A general standard reference on generalized smooth spaces is

* {#km} Kriegl and Michor, _A Convenient Setting of Global Analysis_
 

The structure of loop spaces as Fr&#233;chet manifolds is covered in chapter 42 of [KM](#km) and in various other articles, many of which cover extensions of the basic construction to other mapping spaces.  In particular,

* Michor, _Manifolds of differentiable mappings_ [MR583436 (83g:58009)](http://www.ams.org/mathscinet-getitem?mr=583436)

* Michor, _A convenient setting for differential geometry and global analysis (I and II)_ [MR764972 (86g:58014a)](http://www.ams.org/mathscinet-getitem?mr=764972)

* [[Andrew Stacey]], _The Differential Topology of Loop Spaces_ [main page](http://www.math.ntnu.no/~stacey/Seminars/diffloop.html) (Note: this was designed as an "easy reader" version of [KM](#km))

* [[Andrew Stacey]], _Constructing Smooth Manifolds of Loop Spaces_ [main page](http://www.math.ntnu.no/~stacey/Research/Papers/smooth.html)

The relation of this [[Fréchet manifold]]  structure to the canonical [[diffeological space]] structure is discussed in 

* {#Waldorf} [[Konrad Waldorf]], _Transgression to Loop Spaces and its Inverse I_ ([arXiv:0911.3212](http://arxiv.org/abs/0911.3212)) 
 
Discussion of [[G-structures]] on smooth loop spaces is in the following articles. 

For [[orientation]] structure on loop space and its [[transgression]] from [[spin structure]] on target space:

* {#Waldorf10} [[Konrad Waldorf]], _A Loop Space Formulation for Geometric Lifting Problems_ ([arXiv:1007.5373](http://arxiv.org/abs/1007.5373))
 

For [[spin structure]] on loop spaces and its [[transgression]] from [[string structure]] on target space:

* {#Stolz} [[Stephan Stolz]], [[Peter Teichner]], _The spinor bundle on loop space_ (2005) ([pdf])
 

* {#Waldorf12} [[Konrad Waldorf]], _Spin structures on loop spaces that characterize string manifolds_ ([arXiv:1209.1731](http://arxiv.org/abs/1209.1731))

* {#Waldorf14} [[Konrad Waldorf]], _String geometry vs. spin geometry on loop spaces_ ([arXiv:1403.5656](http://arxiv.org/abs/1403.5656))

There are also sketchy notes in

* {#Melrose} [[Richard Melrose]], _Analysis on loop spaces_, Lecture notes, 2013 ([pdf](http://math.mit.edu/~rbm/18.158-S13/18-158-S13.pdf))
 

For the motivation of much of this via the [[Dirac-Ramond operator]] and the [[Witten genus]] see the references there.

This entry was created in parallel with [this MO thread](http://mathoverflow.net/questions/12652/loop-spaces-as-generalized-smooth-spaces-or-as-infinite-dimensional-manifolds) from which parts of it is taken.


[[!redirects smooth loop space]]
[[!redirects smooth loop spaces]]

