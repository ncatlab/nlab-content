#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In the [[(∞,1)-topos]] [[Top]] to every object -- every [[topological space]] -- $X$ is associated 
the set $\pi_0(X)$ of connected components and the [[homotopy group]]s $\pi_n(X,x)$ for $x \in X$ and $n \in \mathbb{N}$, $n\gt 0$.

By the general logic of [[space]], we may think of the objects in an arbitrary [[∞-stack]] [[(∞,1)-topos]] as generalized spaces of sorts. Accordingly, there there is a notion of homotopy group of an $\infty$-stack.

But care has to be taken. It turns out that there are actually _two_ different notions of homotopy groups in an arbitrary $(\infty,1)$-topos, two notions that accidentally coincide for [[Top]]:

* there is a notion of **categorical homotopy group**: 

  every $(\infty,1)$-topos $\mathbf{H}$ is [[power]]ed over [[∞Grpd]] [[model structure on simplicial sets|usually modeled]] as [[SSet]], hence for every object $X \in \mathbf{H}$ there is the **categorical $n$-sphere object** $X^{S^n_c}$, where $S^n_c = \Delta^n/\partial \Delta^n$. 

* there should be a notion of **geometric homotopy group**, ...

For instance let $\mathbf{H} = Sh_{(\infty,1)}(Diff)$ be the $(\infty,1)$-topos of [[Lie ∞-groupoid]]s. An ordinary smooth [[manifold]] $X$ is represented in $\mathbf{H}$ by a [[sheaf]] of [[set]]s on [[Diff]]. This has no higher nontrivial categorical homotopy groups -- $\pi_{n \gt 0}^{cat}(X) = 0$ -- reflecting the fact regarded as a smooth [[∞-groupoid]], $X$ is a categorically [[discrete groupoid]].

But of course the manifold $X$ may have nontrivial [[homotopy group]]s in terms of its underlying [[topological space]]. For instance if $X = S^1$ is the circle, then the _geometric_ first homotopy group is nontrivial, $\pi_1^{geom}(X) = \mathbb{Z}$.

We discuss below both cases. The case of categorical homotopy groups is fully understood, for the case of geometric homotopy groups at the moment only a few aspects are in the literature, more is in the making. We think [[Richard Williamson]] for pointing this out.

## Categorical homotopy groups

### Definition

Every [[∞-stack]] [[(∞,1)-topos]] $\mathbf{H}$ is naturally
[[power]]ed over [[∞Grpd]] ([[Higher Topos Theory|HTT, remark 5.5.2.6]]):

for every [[∞-groupoid]] $K$ and every object $A \in \mathbf{H}$ there is an object $A^K \in \mathbf{H}$ such that for every object $X \in \mathbf{H}$ there is
an equivalence

$$
  \mathbf{H}(X,A^K) \simeq \infty Grpd(K, \mathbf{H}(X,A))
  \,.
$$ 

Let $S^n := Ex^\infty \partial \Delta[n+1]$ be the [[Kan fibrant replacement]] of the [[boundary of a simplex|boundary of the (n+1)-simplex]], i.e. the model in [[∞Grpd]] of the [[pointed object|pointed]] $n$-[[sphere]].

For every $X \in \mathbf{H}$, evaluation at the base point induces a morphism

$$
  s : X^{S^n} \to X
  \,.
$$

This morphism may be regarded as an object of the [[over category]] [[(∞,1)-topos]] $\mathbf{H}/X$.

For $n \in \mathbb{N}$ define

$$
  \pi_n(X) := \tau_{\leq 0} s \in \mathbf{H}/X
$$

to be the discrete (i.e. [[n-truncated object of an (infinity,1)-topos|0-truncated]]) object obtained from $s$.

As in classical [[homotopy theory]], for $n \geq 1$ the object $\pi_n(X)$ is equipped with the structure of a [[group object]] in $\mathbf{H}/X$, which is an abelian group object for $n \geq 2$.

**Remark** The [[n-truncated object of an (infinity,1)-topos|0-truncated]] objects in $\mathbf{H}/X$ have the interpretation of [[sheaf|sheaves]] on $X$. So in the world of [[∞-stack]]s a homotopy [[group object]] is a [[sheaf]] of groups.



### References

section 6.5.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_



## Geometric homotopy groups

### Idea


For $X$ a connected [[topological space]], the following notions are equivalent:

* a finite covering space $P \to X$;

* a [[locally constant sheaf]] or [[local system]] on $X$ with finite fibers (the sheaf of sections of some $P$);

* a [[bundle]] of finite sets [[associated bundle|associated]] to the universal $\pi_1(X,x)$-[[principal bundle]] on $X$, for $\pi_1(X,x)$ the first [[homotopy group]] of $X$ at some chosen basepoint $x$;

* a [[functor]] $\mathbf{B} \pi_1(X,x) \to FinSet$, with $\mathbf{B} \pi_1(X,x)$ the [[delooping]] [[groupoid]],which exhibits the unique flat [[connection on a bundle|connection]] on the [[bundle]] $P$.


The last formulation makes it most manifest that the collection of all these things, in whichever incarnation, form the [[representation category]]

$$
  Rep(\pi_1(X,x))_{f} = Func(\mathbf{B}\pi_1(X,x), FinSet)
$$

of the [[group]] $\pi_1(X,x)$ on finite sets. But for representation categories [[Tannakian reconstruction theorems]] hold, which say that we may recover the group being represented essentially as the group of [[automorphism]]s of the forgetful functor

$$
  F : Rep(\pi_1(X,x))_{f} \to FinSet
  \,.
$$

So we may turn this around: we may start with the notion of [[local system]] on $X$, and then read off from the category of all of these the first fundamental group of $X$.

The choice of basepoint here of course plays no intrinsic role. A bit more elegantly we can instead use the [[fundamental groupoid]] $\Pi_1(X)$ of $X$ (which then no longer needs to be assumed to be connected) and locally constant sheaves with finite fibers as functors/representations in

$$
  Loc(X) = Rep(\Pi_1(X))_f = Func(\Pi_1(X), FinSet)
  \,.
$$

And conversely, given just the notion of $Loc(-)$, we may again _define_ $\Pi_1(-)$ as the groupoid that co-represents $Loc$. This is useful, because the notion of [[locally constant sheaf]] $Loc(-)$ is canonically given over every object $X$ in every [[topos]]. So this provides a way to define $\Pi_1(X)$ for every such object.

And this has an evident [[vertical categorification]]: 

in an [[(∞,1)-topos]] for every object $X$ there is an [[(∞,1)-category]] $Loc(X)$ of [[locally constant ∞-stack]]s on $X$. The [[fundamental ∞-groupoid]] of $X$ may then be defined as the [[∞-groupoid]] such that 

$$
  Loc(X) \simeq [\Pi(X), \infty Grpd]
  \,.
$$



### For 1-toposes

...

section 8.4 of

* [[Peter Johnstone]], _Topos theory_ 


### For the $(\infty,1)$-topos $Top$

...

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))

[[!redirects homotopy groups (of an infinity-stack)]]
[[!redirects homotopy group (of an ∞-stack)]]
[[!redirects homotopy groups (of an ∞-stack)]]
