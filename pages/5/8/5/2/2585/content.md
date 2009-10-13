#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

In the [[(∞,1)-topos]] [[Top]] to every object -- every [[topological space]] -- $X$ is associated 
the set $\pi_0(X)$ of connected components and the [[homotopy group]]s $\pi_n(X,x)$ for $n \in \mathbb{N}$, $n\gt 0$.

This consruction of homotopy groups 
has an analogue for objects in an arbitrary [[∞-stack]]
[[(∞,1)-topos]].

#Definition#

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





#References#

section 6.5.1 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects homotopy group (of an infinity-stack)]]