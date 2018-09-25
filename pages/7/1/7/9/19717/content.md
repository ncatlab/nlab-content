
#Contents#
* table of contents
{:toc}

In [[computer science]], originally in database theory, **lenses** are used in situations where some structure is converted to a different form -- a *view* -- in such a way that changes made to the view can be reflected as updates to the original structure. The some construction has been devised on numerous occasions ([Hedges](#Hedges)).

## Definition

Let $C$ be a [[category]] with [[finite products]]. A **lens** in C denoted $L =(S,V,g,p)$ has states $S$ and view states $V$ which are objects of $C$, and two arrows of C, a *Get* arrow $g:S \to V$ and a *Put* arrow $p:V \times S \to S$, often taken to satisfy the following equations, or _lens laws_:

1. (PutGet) the Get of a Put is the projection: $g p= \pi_0$.
1. (GetPut) the Put for a trivially updated state is trivial: $p \langle g, 1_S \rangle = 1_S$.
1. (PutPut) composing Puts does not depend on the first view update: $p(1_V \times p) = p \pi_{0,2}$.

[Sometimes a lens satisfying all three laws is said to be _lawful_. Sometimes it is said that a _well-behaved_ lens satisfies (1) and (2) and a _very well-behaved_ lens satisfies also (3).]

In other words, a (lawful) lens for a fixed $V$ is an [[algebra over a monad|algebra]] from the monad $V^{\ast} \cdot \Sigma$ (the [possibility](necessity+and+possibility#globally) operator):

$$
  C/V
  \underoverset
    {\underset{V^{\ast}}{\longleftarrow}}
    {\overset{\Sigma}{\longrightarrow}}
    {\bot}
  C.
$$

They are also [[coalgebra over a comonad|coalgebras]] for the [[store comonad]].

## Generalizations

Many kinds of generalization have been proposed - asymmetric lenses, bimorphic lens, etc.

One generalization considers the lenses from the previous section as _monomorphic_ by contrast to _polymorphic_ lens which go between pairs of types, $\lambda: (S, T) \to (A, B)$, consisting of a view function, $v_{\lambda}: S \to A$, and an update function $u_{\lambda}: S \times B \to T$. Without further conditions, these are known as _bimorphic lenses_. To impose conditions comparable to the lens laws above requires that the types be related.

##References

* Bohannon, A., Vaughan, J. and Pierce, B. (2006)  Relational Lenses: A language for updatable views. Proceedings of Principles of Database Systems (PODS) 2006


* Foster, J., Greenwald, M., Moore, J., Pierce, B. and Schmitt, A. (2007)  Combinators for bidirectional  tree  transformations:  A  linguistic  approach  to  the  view  update  problem. ACM Transactions on Programming Languages and Systems 29

* Michael Johnson, Robert Rosebrugh, and R. J. Wood.  Lenses, fibrations and universal translations. Math. Structures Comput. Sci., 22(1):25–42, 2012

* [[Bartosz Milewski]], [Lenses, Stores, and Yoneda](https://bartoszmilewski.com/2013/10/08/lenses-stores-and-yoneda/)

* Jeremy Gibbons, [Lenses are the coalgebras for the costate comonad](https://patternsinfp.wordpress.com/2011/01/31/lenses-are-the-coalgebras-for-the-costate-comonad/)

* {#Hedges} [[Jules Hedges]], _Lenses for philosophers_, [blog post](https://julesh.com/2018/08/16/lenses-for-philosophers/)

* [[Mitchell Riley]], _Categories of optics_, ([arXiv:1809.00738](https://arxiv.org/abs/1809.00738))