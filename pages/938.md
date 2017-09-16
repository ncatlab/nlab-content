# Topological weak homotopy equivalences #

A **weak homotopy equivalence** between [[topological space]]s is a continuous map which induces [[isomorphism]]s on all [[homotopy group]]s.

More precisely, $f:X\to Y$ is a weak homotopy equivalence if

1. $f$ induces an isomorphism $f_*:\pi_0(X)\to \pi_0(Y)$ of path components, and
1. for any basepoint $x\in X$ and any $n\ge 1$, $f$ induces an isomorphism $f_*:\pi_n(X,x) \to \pi_n(Y,f(x))$.  If $X$ and $Y$ are [[connected space|path-connected]], then it suffices to require this for a single (arbitrary) $x$, but in general one must require it for all $x$.

Any [[homotopy equivalence]] is a weak homotopy equivalence.  It requires a little bit of thought to prove this, because $f$ and its homotopy inverse $g$ need not preserve any chosen basepoint.  But for any $x\in X$ and any $n\ge 1$, we have a diagram
$$\array{\pi_n(X,x) & & \to & & \pi_n(X,g(f(x)))\\
  & \searrow && \nearrow && \searrow\\
  && \pi_n(Y,f(x)) && \to && \pi_n(Y,f(g(f(x))))}$$
in which the two horizontal maps are isomorphisms because $g f$ and $f g$ are [[homotopy|homotopic]] to identities.  Hence, by the [[two-out-of-six property]] for isomorphisms, the diagonal maps are  also all isomorphisms.

Conversely, any weak homotopy equivalence between [[m-cofibrant space]]s (spaces that are homotopy equivalent to [[CW complex]]es) is a homotopy equivalence.

Weak homotopy equivalences are the [[weak equivalence]]s in the classical "Quillen" [[model structure on topological spaces]], and also in the "mixed" model structure.

The existence of a weak homotopy equivalence from $X$ to $Y$ is a reflexive and transitive relation, but it is not symmetric.  If $X$ and $Y$ are related under the [[equivalence relation]] it generates, we call them **weakly equivalent** and say that they have the same **weak homotopy type**.  Explicitly, this means there exists a [[zigzag]] of weak homotopy equivalences $X \leftarrow \to\leftarrow \dots \to Y$.  It is equivalent to saying that $X$ and $Y$ become [[isomorphism|isomorphic]] in the [[homotopy category]] of topological spaces with the weak homotopy equivalences inverted.


# Other types of weak homotopy equivalence #

A map of [[simplicial set]]s is called a weak homotopy equivalence if its [[geometric realization]] is a weak homotopy equivalence of topological spaces, as above.  (Since the geometric realization of any simpicial set is a CW complex, in this case its geometric realization is actually a homotopy equivalence.)  These are the weak equivalences in the classical [[model structure on simplicial sets]].

Likewise, a [[functor]] between [[small category|small]] categories is sometimes said to be a weak homotopy equivalence if its [[nerve]] is a weak homotopy equivalence of simplicial sets.  These are the weak equivalences in the Thomason [[model structure on categories]] (not the [[folk model structure]]).

Similarly, one can define weak homotopy equivalences between any sort of object that has a geometric realization, such as a [[cubical set]], a [[globular set]], an [[n-category]], an [[n-fold category]], and so on.
