# Covert space

* table of contents
{: toc}

## Idea

A **covert space** is a [[space]] $X$ such that the unique map $X\to 1$ to the [[terminal object|terminal]] space is a [[closed map]].  This should be compared with [[overt spaces]], where $X\to 1$ is an [[open map]], and [[compact spaces]], where $X\to 1$ is a [[proper map]].  Since proper maps are closed, all compact spaces are covert.

In [[classical mathematics]], every space is covert, just as every space is overt.  However, in [[constructive mathematics]], and in particular in [[synthetic topology]], covertness can be a strong condition that already carries much of the power of compactness.

## Definition

A [[locale]] $X$ is **covert** if the unique map $X\to 1$ is a [[closed map]] of locales, i.e.\ the [[adjunction]] $f^* : O(1) \rightleftarrows O(X) : f_*$ satisfies the [[Frobenius reciprocity]] condition $f_*(U\cup f^*(V)) = f_*(U)\cup V$.

If [[excluded middle]] holds, then every locale is covert.

## Covert sets

Constructively, covertness is already interesting when $X$ is a set with the [[discrete topology]].  In this case, since $O(1) = P(1)$ is the poset of [[truth values]] (the [[subobject classifier]]) and $O(X)=P(X)$ is the [[powerset]] of $X$, covertness of $X$ can be expressed more logically as

> if $P$ is a [[proposition]] and $Q$ a [[predicate]] on $X$ such that $\forall x\in X, (P \vee Q(x))$, then $P\vee (\forall x\in X, Q(x))$.

This is always true if $X$ is [[finite set|(Kuratowski) finite]] (in which case the discrete topology on $X$ is not just covert but compact), but in general it can be quite a strong condition.

In [[synthetic topology]], covertness of sets carries much of the strength of compactness.  (Note that here we are talking about covertness of sets --- i.e. "spaces" in the sense of synthetic topology, i.e. basic objects of our foundational system --- equipped with the "discrete [[topology]]" internal to our synthetic-topological formal system; these are quite different from sets whose intrinsic *synthetic* topology is discrete.)  For instance, in various [[gros toposes]] of topological, smooth, or algebraic spaces, the covert spaces are precisely the compact ones; see [Dubuc-Penon](#DubucPenon) (who call covert sets "compact").

Covert sets also satisfy the following property.

+-- {: .un_theorem}
###### Theorem
If $X$ is covert, then for any two predicates $P,Q$ on $X$ such that $\forall x\in X, (P(x) \vee Q(x))$, we have either $\exists x\in X, P(x)$ or $\forall x\in X, Q(x)$.
=--
+-- {: .proof}
###### Proof
Let $P'$ be the proposition $\exists x\in X, P(x)$ in the defining property of covertness for $X$.
=--

Note that if $P$ and $Q$ are incompatible (i.e. $\neg (P(x)\wedge Q(x))$), then this becomes the [[limited principle of omniscience]] for $A$.  Thus, every covert set is [[omniscient set|omniscient]].


## References

* [[Eduardo Dubuc]] and [[Jacques Penon]], *Objets compacts dans les topos*
 {#DubucPenon}

[[!redirects covert spaces]]
[[!redirects covert sets]]
[[!redirects covert set]]
