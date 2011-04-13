{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: goal}
###### Goal
The purpose of this page is to investigate the question:

> How much of a [[smooth manifold]]'s structure can be determined by knowing its [[submanifolds]]?
=--

This can be interpreted in several ways mathematically.  We start with two smooth manifolds, $M$ and $N$, and a bijection $\Phi \colon M \to N$.  We want to learn something about what $\Phi$ must or can be by testing it on submanifolds.  Ideally, we would like a condition equivalent to $\Phi$ being a diffeomorphism.  Some conditions to consider are the following.

1. $S \subseteq M$ is a submanifold if and only if $\Phi(S) \subseteq N$ is a submanifold.
1. $S \subseteq M$ is a submanifold of dimension $m$ if and only if $\Phi(S) \subseteq N$ is a submanifold of dimension $m$.
1. For some fixed $m$ and for all $k \le m$, $S \subseteq M$ is a submanifold of dimension $k$ if and only if $\Phi(S) \subseteq N$ is a submanifold of dimension $k$.
1. For some fixed $m$, $S \subseteq M$ is a submanifold of dimension $m$ if and only if $\Phi(S) \subseteq N$ is a submanifold of dimension $m$.

## Ideology ##

One reason that [[Andrew Stacey|I]] am interested in this is that it is a variation of the idea of [[generalised smooth spaces]].  In a generalised smooth space, one defines "smoothness" to be "that which is detectable when tested on known spaces".  The point is that the _known spaces_ are fixed and independent of the object being tested.  Here, the known spaces can (and, indeed, do) vary with the object being tested.  So each object has its own family of test objects.  Closely related to this is the question of automorphisms of a category.  If we have a category with test objects inside it then applying an automorphism will change the test objects so to study this situation we have to find some other way of characterising the test objects.  In [[comparative smootheology]], I showed that there were no (essentially) non-trivial automorphisms of the category of [[Frölicher spaces]] by showing that one could identify the real line by its endomorphism monoid.

## Preliminary Thoughts ##

For $\mathbb{R}$, it is the case that preserving submanifolds is equivalent to being a homeomorphism so long as we are considering submanifolds of dimension $1$.  By cardinality, we can separate submanifolds of dimension $1$ and $0$ and so from any of the statements we see that $\Phi$ takes submanifolds of dimension $1$ to submanifolds of dimension $1$.  But submanifolds of $\mathbb{R}$ of dimension $1$ are precisely the open sets, whence $\Phi$ is a homeomorphism.

This extends more generally.  If $\Phi \colon \mathbb{R}^n \to \mathbb{R}^m$ is a bijection with the property that $\Phi(S)$ is a submanifold of $\mathbb{R}^m$ if and only if $S$ is a submanifold of $\mathbb{R}^n$ then $\Phi$ is a homeomorphism.  The proof is slightly different depending on whether we allow the dimension of a submanifold to be [[locally constant]] or insist that it be [[constant]].

We start with an open set $U \subseteq \mathbb{R}^n$.  As this is a submanifold, $\Phi(U)$ is a submanifold of $\mathbb{R}^m$.  For cardinality reasons, $\Phi(U)$ cannot be zero dimensional everywhere.  Indeed, it can be zero dimensional at at most a countable number of points.  Choose a point $p \in U$ such that $\dim_{\Phi(p)} \Phi(U) \ne 0$.

We choose an open set $V$ with $p \in V \subseteq \overline{V} \subseteq U$.  By assumption, $\Phi(V)$ is a submanifold of $\mathbb{R}^m$ and $\Phi(p) \in \Phi(V)$.  Suppose that $\dim_{\Phi(p)} \Phi(U) \ne m$.  Then there is a connected submanifold $T$ of $\mathbb{R}^m$ of dimension at least $1$ which meets $\Phi(U)$ transversally at $\Phi(p)$.  In particular $T \cap \Phi(U) = \{\Phi(p)\}$.  Applying $\Phi^{-1}$, we find that $\Phi^{-1}(T)$ is a submanifold of $\mathbb{R}^n$ which meets $U$ only at $p$.  Thus $p$ must be an isolated point of $\Phi^{-1}(T)$.  Since the closure of $V$ is contained within $U$, the union $V \cup \Phi^{-1}(T)$ is therefore a submanifold of $\mathbb{R}^n$.  Applying $\Phi$, we see that $\Phi(V) \cup T$ is a submanifold of $\mathbb{R}^m$.  But $\Phi(V)$ and $T$ both have non-zero dimension at $p$ and meet transversally there, so their union cannot be a submanifold of $\mathbb{R}^m$.

Thus at those points where $\dim \Phi(U) \ne 0$, it must be of dimension $m$.  To conclude the proof, we just need to show that there are no points where $\dim \Phi(U) = 0$.  Suppose that there is such a point, say $p$.  Then $\Phi(p)$ is an isolated point from $\Phi(U)$.  Choose an open set $W \subseteq \mathbb{R}^m$ such that $\Phi(p) \in \partial W$ and $W \cap \Phi(U) = \emptyset$.  Then $W \cup \{\Phi(p)\}$ is not a submanifold of $\mathbb{R}^m$, but $\Phi(W) \cap U = \emptyset$ so $\Phi(W) \cap \{p\}$ is a submanifold of $\mathbb{R}^n$.  Hence there cannot be any such points.

In conclusion, $\Phi(U)$ is a submanifold of $\mathbb{R}^m$ of dimension $m$, whence an open subset.  As the same holds for $\Phi^{-1}$, we conclude that $\Phi$ is a homeomorphism.

## Initial Motivation ##

The initial motivation for this page came from [this question](http://math.stackexchange.com/q/26954/2907) on &lt;http://maths.stackexchange.com>.