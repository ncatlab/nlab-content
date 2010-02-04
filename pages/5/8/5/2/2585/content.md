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



## Geometric homotopy groups {#Geometric}

### Idea

Let $C$ be some [[site]] and let $\mathbf{H} = Sh_{(\infty,1)}(C)$ be the [[(∞,1)-topos]] of [[∞-stack]]s over $C$. We think of objects $X \in \mathbf{H}$ as generalized [[space]]s modeled on $C$.

We have a squence of [[adjunction]]s

$$
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh_{(\infty,1)}(C)
  \stackrel{\overset{const}{\leftarrow}}{\to}
  PSh_{(\infty,1)}(*)
  =
  \infty Grpd 
  :
  LConst
$$

where on the left we have the defining adjunction of the [[(∞,1)-category of (∞,1)-sheaves]] -- $L$ is [[∞-stackification]] -- and on the right the [[geometric morphism]] that is induced from the canonical morphism of [[site]]s $C \to {*}$ (to the [[terminal object|terminal]] site).

The [[constant ∞-stack]] $\infty FinBund := LConf(Core(\infty FinGrpd)) \in \mathbf{H}$ is the classifying stack for [[locally constant ∞-stack]]s on objects $X \in \mathbf{H}$. We write

$$
  \infty FinBund(X) := \mathbf{H}(X,\infty FinBund)
$$ 

for the $\infty$-groupoid of [[locally constant ∞-stack]]s on $X$.

If the [[left adjoint]] $LConst$ is also a [[right adjoint]] 

$$
  (\Pi \dashv LConst)
  :
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Pi}{\to}}
  \infty Grpd   
$$

then we have from the [[adjunction]] that locally constant $\infty$-stacks on $X$ are equivalently given by [[(∞,1)-functor|∞-functors]] from the [[∞-groupoid]] $\Pi(X)$ to $\infty FinGrpd$:

$$
  \infty FinBund(X) \simeq Func(\Pi(X),\infty FinGrpd)
  \,.
$$

In $\mathbf{H} = $ [[Top]], this is the relation satisfied by the [[fundamental ∞-groupoid]] $\Pi(X)$ of a [[topological space]] $X$. Accordingly here in a general $(\infty,1)$-topos $\mathbf{H}$ we may think of the functor $\Pi : \mathbf{H} \to \infty Grpd$ as giving for each generalized [[space]] its geometric [[schreiber:path ∞-groupoid]] of geometric paths in it.

Accordingly, then, we may think of the ordinary [[homotopy group]]s of $\Pi(X)$ as the **geometric homotopy groups** of $X \in \mathbf{H}$.



### For 1-toposes

...

section 8.4 of

* [[Peter Johnstone]], _Topos theory_ 


### For the $(\infty,1)$-topos $Top$

...

* [[Pietro Polesello]] and [[Ingo Waschkies]], _Higher monodromy_ , Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150 ([pdf](http://www.intlpress.com/HHA/v7/n1/a7/pdf)) 

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))

[[!redirects homotopy groups (of an infinity-stack)]]
[[!redirects homotopy group (of an ∞-stack)]]
[[!redirects homotopy groups (of an ∞-stack)]]
