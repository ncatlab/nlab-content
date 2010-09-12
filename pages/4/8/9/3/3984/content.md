{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

# Tangential Topics of Fr&#246;licher Spaces
{#tangent}

+-- {: .query}
This section is essentially lifted from [Comparative Smootheology](http://arxiv.org/abs/0802.2225) as I intend to remove it from that article and this seems a good place to put it.
=--

Nearly every construction in differential topology starts with tangent or cotangent bundles.
As a conclusion of this note, we shall look at how one could define these in the more general setting.
An advantage of the dual nature of the definition of a smooth structure due to Fr&#246;licher is that just about every definition of a tangent or cotangent vector is possible.
Essentially, as we have access to both curves and functionals we can consider push-forwards and pull-backs.

The ideas in this section can be traced at least as far back as Fr&#246;licher's work in [MR842916](http://www.ams.org/mathscinet-getitem?mr=842916).
That there are different orders of tangent and cotangent vectors appears in Kriegl and Michor's book [MR1471480](http://www.ams.org/mathscinet-getitem?mr=1471480), though it doubtless has antecedents.
However in [MR1471480](http://www.ams.org/mathscinet-getitem?mr=1471480), only operational tangent vectors have higher orders.
This is because the context is that of manifolds and so non-trivial higher order kinematic tangent vectors do not appear.

Let us start with _kinematic tangent vectors_.
We start with a notion of what it means for a curve to be flat.


+-- {: mynumdef #Flatness}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space.
 A curve $c \in \mathcal{C}$ is said to be _$k$-flat_ at $t \in \mathbb{R}$ if for each $f \in \mathcal{F}$, $(f c)^{(j)}(t) = 0$ for $1 \le j \le k$.
 It is _flat_ at $t \in \mathbb{R}$ if it is $k$-flat for all $k \in \mathbb{N}$.

 We write $\mathcal{C}_{x,k}$ for the subset of $\mathcal{C}$ consisting of those curves that map $0$ to $x$ and are $(k-1)$-flat at $0$.
=--

For convenience, in the next definition we will say that any curve is $0$-flat.

+-- {: mynumdef #FroTanSet}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space.
 Let $x \in X$ and let $k \in \mathbb{N}$.
 The _$k$th kinematic tangent set_ at $x$, $T_{x,k} X$, is the quotient of $\mathcal{C}_{x,k-1}$ by the equivalence relation $c_1 \simeq c_2$ if
  $(f c_1)^{(k)}(t) = (f c_2)^{(k)}(t)$
 for all $f \in \mathcal{F}$.
=--

We write this as $T_{x,k} X$ rather than $T_x^k X$ to avoid conflict of notation with iterated tangent spaces.
Since any curve can be composed with a suitable smooth map $\mathbb{R} \to \mathbb{R}$ to produce a curve of higher flatness, there are natural inclusions
 $T_{x,k} X \to T_{x,k+1} X$.
For Euclidean spaces with their usual structure, all of these tangent sets coincide.

+-- {: mynumdef #FroKinTan}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space.
 The _full kinematic tangent set_ of $X$ at $x$ is
  $T_{x,\infty} X = \bigcup_k T_{x,k} X$.
=--

It is obvious that each of these kinematic tangent sets is functorial in Fr&#246;licher spaces.

One would anticipate that in a given application the only two candidates for a kinematic tangent set will be either the full kinematic tangent set or the first kinematic tangent set.
Note that for a manifold with boundary, the first kinematic tangent set at a point in the boundary is the tangent space of the boundary whereas the full kinematic tangent set is the tangent space of the ambient manifold (including the outward pointing normal).

We have been careful in writing "tangent _set_" rather than "tangent _space_" so as not to imply any particular structure.
Reparametrisation of paths easily defines the structure of an $\mathbb{R}$-set on each tangent set but in general one will not be able to add tangent vectors.
Nonetheless, some addition may be possible and addition has nice properties when it is defined.

+-- {: mynumdef #TanSum}
###### Definition
Let $X$ be a Fr&#246;licher space, $x \in X$.
For $u,v, w \in T_{x,k} X$ we say that $w$ is a _sum_ of $u$ and $v$ if there are representatives $\alpha$, $\beta$, $\gamma$ such that $(f \alpha)^{(k)} = (f \beta)^{(k)} + (f \gamma)^{(k)}$ for all $f \in F_X$.

More generally, $u_1, \dots, u_k \in T_{x,k} X$ have a sum if there is some $w \in T_{x,k} X$ with $(f \beta)^{(k)} = \sum (f \alpha_i)^{(k)}$. 
=--

+-- {: .num_lemma #LemTanSum}
###### Lemma
Sums are unique if they exist.
=--

+-- {: myproof}
###### Proof
If $\beta$ and $\gamma$ both represent sums of $u_1, \dotsc, u_k$ then
\[
(f \beta)^{(k)} = \sum (f \alpha_i)^{(k)} = (f \gamma)^{(k)}
\]
so $\beta$ and $\gamma$ represent the same vector in $T_{x,k} X$.
=--

The construction of kinematic tangent vectors suggests a similar construction for cotangent vectors.
As with tangent vectors, we need an auxiliary definition.

+-- {: mynumdef #FlatFun}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space, $x \in X$.
 A functional $f \in \mathcal{F}$ is said to be _$k$-flat_ at $x \in X$ if for each $c \in \mathcal{C}$ with $c(0) = x$, $(f c)^{(j)}(0) = 0$ for $1 \le j \le k$.
 It is _flat_ at $x \in X$ if it is $k$-flat for all $k \in \mathbb{N}$.

 We write $\mathcal{F}_{x,k}$ for the subset of $\mathcal{F}$ of functionals that are $k$-flat at $x$.
=--

Again, for convenience we will say that all functionals are $0$-flat.

+-- {: mynumdef #KinCoTan}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space, $x \in X$.
 The _$k$th kinematic cotangent space_ at $x$, $T^*_{x,k} X$, is the quotient of $\mathcal{F}_{x,k-1}$ by the relation $f_1 \simeq f_2$ if
  $(f_1 c)^{(k)}(0) = (f_2 c)^{(k)}(0)$
 for all $c \in \mathcal{C}$ with $c(0) = x$.
=--

The same discussion for kinematic tangent vectors applies to kinematic cotangent vectors except for the fact that cotangent vectors automatically form vector spaces.

+-- {: mynumdef #KinFullCoTan}
###### Definition
 The _full kinematic cotangent space_ of $X$ at $x$ is
  $T^*_{x,\infty} X = \bigcup T^*_{x,k} X$.
=--

There are obvious pairings between kinematic tangent and cotangent vectors based on evaluation.
One defines a map
 $(f,c) \mapsto (f c)^{(k)}(0)$
and this descends to providing one knows that $(f c)^{(j)}(0)$ vanishes for $j \lt k$.
The simplest case of this is where one of the tangent or cotangent vectors has order $k$.
Thus the highest level pairing,
 $(f, c) \mapsto (f c)'(0)$,
defines a pairing for all tangent and cotangent vectors but one which vanishes unless both are of first order.



We can also define _operational tangent vectors_.
Recall that $\mathcal{F}$ is an algebra of functions.

+-- {: mynumdef #OpTanSet}
###### Definition
 Let $(X, \mathcal{C}, \mathcal{F})$ be a Fr&#246;licher space, $x \in X$.
 An _operational tangent vector_ at $x$ is a derivation at $x$ of $\mathcal{F}$.
 That is, a linear map
  $\partial : \mathcal{F} \to \mathbb{R}$
 such that
  $\partial(f g) = f(x) \partial g + g(x) \partial f$.

 We write $D_x X$ for the vector space of operational tangent vectors at $x$ and $D_{x,k} X$ for the space of operational tangent vectors at $x$ that vanish on $\mathcal{F}_{x,k}$.
=--

The order of an operational tangent vector is defined to be the least $k$ for which it lies in $D_{x,k} X$, otherwise it is said to have infinite order.
Again, in a given application it may be preferable to restrict to operational tangent vectors of finite order, or of order $1$.

+-- {: .num_lemma #KinToOp}
###### Lemma
 There are natural maps
  $T_{x, k} X \to D_{x,k} X$
 compatible with the connecting maps on each side.
=--

+-- {: myproof}
###### Proof
 For $c \in \mathcal{C}_{x,k-1}$ and $f \in \mathcal{F}$ we define an operational tangent vector by
  $f \mapsto (f c)^{(k-1)}(0)$.
 This has the required properties.
=--

This map, however, need not be injective and neither need it map to a spanning set.



One can define two more versions of "cotangent vectors" by taking linear duals of the two versions of tangent vectors (this has to be done with care for the kinematic tangent vectors); however, these definitions may be thought of as one-step removed from the smooth structure itself.


[[!redirects tangential notions of Frölicher spaces]]
[[!redirects tangential notions of Frolicher spaces]]
[[!redirects tangential notions of Froelicher spaces]]
