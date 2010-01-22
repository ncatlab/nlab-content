#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The smooth loop space of a smooth [[manifold]], say $M$, is the [[space]] of smooth maps from the circle, $S^1$, to $M$.  It naturally carries the structure of a [[diffeological space]] or [[Frolicher space]] and can be given compatibly the structure of an infinite dimensional [[Frechet manifold|Fréchet manifold]].

By extending the idea of a manifold to that of a [[generalized smooth space]], smooth loop spaces can be viewed as the result of applying the [[internal hom]]-functor $[-,-] : SmoothSpace^{op} \times SmoothSpace \to SmoothSpace$ with the circle as the source:

$$
  LoopSpace(X) = [S^1, X]
  \,.
$$

Depending on taste and application, certain smooth [[quotient object|quotient object]]s of this free loop space may be and are often considered. 

## Details on the smooth structures

The [[Frechet manifold|Fréchet manifold]] structure of $L X$ agrees with the [[diffeological space|diffeology]] on $L X$ in the following sense.

There is a [[functor]]

$$
  F: Frech \to Diff
$$

from [[Frechet manifold|Fréchet manifold]]s to [[diffeological space]]s defined in the same way as the well-known functor from smooth [[manifold]]s to [[diffeological space]]s: a plot is precisely a smooth map $c : U \to L X$, where $U$ is an object in the domain category, e.g. an open subset of some $\mathbb{R}^n$.

(Notice that a theorem of M. Losik says that the functor F is [[full and faithful functor|full and faithful]], just like that including manifolds into diffeological spaces!)

Now there are two diffeologies on $L X$: this is the structure of a [[sheaf]] on the category [[CartSp]] obtained as regarding $L X$ as the [[internal hom]] with respect to the [[closed monoidal structure on sheaves]]

$$
  L X = [S^1,X] : U \mapsto Hom_{Sh(CartSp)}(S^1 \times Y(U), X)
$$

(whery $Y$ denotes the [[Yoneda embedding]]).

This means that a map $c : U \to L X$ is a plot if and only if the associated map $U \times S^1 \to X$ is smooth. The second diffeology is the one obtained from the functor $F$.

These two diffeologies _coincide_  -- in the sense that every plot of one is a plot of the other. In particular, they have the same sets of smooth functions.

A pedestrian's proof of this is in [Lemma A.1.7](http://arxiv.org/PS_cache/arxiv/pdf/0911/0911.3212v1.pdf#page=27) in 

* [[Konrad Waldorf]] _Transgression to Loop Spaces and its Inverse I_ ([arXiv:0911.3212](http://arxiv.org/abs/0911.3212)) 


## As the loop space object of the smooth path groupoid {#AsLoopObj}

Given the notion of the smooth [[path groupoid]] $\mathcal{P}_1(X)$ of the smooth space $X$, we may think of the smooth loop _space_ as the corresponding [[loop space object]].

We say this in detail now.

### Recollection of the situation in $Top$

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

**In words** this is the simple statement that $\Omega_x X$ is the space of all [[homotopy|homotopies]] in the [[(∞,1)-category]] [[Top]] from the map $x : {*} \to X$ to itself. Any one such homotopy is itself a continuous map $\gamma : I \to X$ from the [[interval object|standard interval]] $I = [0,1]$ to $X$, such that restricted to its endpoints it produces the map $x$. Clearly, these are precisely the loops in $X$, based at $X$.

### Generalization to $\infty$-Lie groupoids

You might think: well, now let $X \in Sh_{(\infty,1)}(Diff)$ be a smooth [[manifold]] regarded as a [[representable functor|representable]] object in the [[(∞,1)-category of (∞,1)-sheaves]] of [[∞-stack]]s on [[Diff]] or maybe better in Sh_{(\infty,1)}(CartSp) on [[CartSp]] -- i.e. of [[Lie ∞-groupoid]]s -- , we play the same trick and compute the [[homotopy pullback]] $Q$

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

If instead we had interpreted the topological space $X$ as a representable object, hence as a [[discrete category|categorically discrete]] object in the $(∞,1)$-category of [[topological ∞-groupoid]]s, we would have seen the same phenomenon as for the smooth $X$ above: its [[loop space object]] would have been the point.

From this perspective now it is clear how the abstract notion of [[loop space object]] corresponds to the geometrically expected one: for a geometric [[space]] $X$, its loop space is the [[loop space object]] of its [[fundamental ∞-groupoid]].

This statement can be given sense in all context where the underlying [[topos]] of our ambient [[(∞,1)-topos]] of [[space]]s is a [[lined topos]]: we need to know which object $R$ is the standard _line_ or [[interval object]]. This determines the _geometric paths_ in a space. Taking these geometric paths to be the [[morphism]]s of a [[fundamental ∞-groupoid]] then makes the geometric paths into "categorical paths", i.e. into morphisms. These then are what the abstract definition of [[loop space object]] can see.

And indeed, whenever the underlying [[topos]] of [[space]]s that we are looking at is a [[lined topos]] the corresponding [[(∞,1)-topos]] comes equipped with a generalization of the topological [[fundamental ∞-groupoid]] construction: we can associate to every [[space]] $X$ its
[[schreiber:path ∞-groupoid]] $\Pi(X)$: the morphisms of $\Pi(X)$ are given by paths in $X$ as seen by the given [[interval object]] $I$. All entirely analogous to the familiar situation for [[Top]], only that now we are testing our generalized [[space]]s over test objects in an arbitrary [[site]]s and are using a correspondingly different notion of [[interval object]].

### The concrete definition

So for $X$ a smooth [[manifold]], regarded as a representable object in the [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$ of [[Lie ∞-groupoid]]s we have now that the homotopy pullback of any point ${*} \to X \hookrightarrow \Pi(X)$ aqlong itself in the [[schreiber:path ∞-groupoid]] $\Pi(X)$ does indeed produce the expected [[Lie ∞-groupoid]] $\Omega_x X$  in 

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

* smooth space of morphism is the smooth space of smooth $I$-homotopies between smooth loops in $X$

* etc;

Here we want not the full loop [[∞-groupoid]], but just some sort of truncation to a [[0-category|0-groupoid]] just of loops. There are several choices for how exatly to do this, depending on which higher morphisms we just discard, and which we use to identify 1-morphisms. Whatever we do, we end up with some notion of smooth [[path groupoid]] $\mathcal{P}_1(X)$ of $X$, whose 1-morphisms are certain smooth quotient space of the smooth space of 1-morphisms in $\Pi(X)$.

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

When unwarpping what all this means, one sees that the object $LoopSpace_x(x) \in Sh_{(\infty,1)}(Diff)$ that we obtain this way is nothing but the image under the embedding $Sh(Diff) \hookrightarrow Sh_{(\infty,1)}(X)$ of ordinary [[sheaf|sheaves]] into $\infty$-stacks of some [[quotient object|quotient]] of the [[internal hom]] $[I,X]$ in the [[closed monoidal structure on sheaves]]. Being an internal hom of representables, this is a [[concrete sheaf]] and as such it is precisely the smooth loop space regarded as a [[diffeological space]].

## References

A general standard reference on generalized smooth spaces is

* Kriegl and Michor, _A Convenient Setting of Global Analysis_ 

Concretely for the question discussed here some useful statements are collcted in

* [[Konrad Waldorf]] _Transgression to Loop Spaces and its Inverse I_ ([arXiv:0911.3212](http://arxiv.org/abs/0911.3212)) 


This entry was created in parallel with [this MO thread](http://mathoverflow.net/questions/12652/loop-spaces-as-generalized-smooth-spaces-or-as-infinite-dimensional-manifolds) from which parts of it is taken.