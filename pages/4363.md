
> this entry is about the concept in [[topology]], especially in [[point-free topology]]. For the concept in [[physics]]/[[chemistry]] see [[nucleus (physics)]], or see [[nucleus (disambiguation)]].

# Nuclei
* table of contents
{: toc}

## Idea

Recall that [[frames]] are [[duality|dual]] to [[locales]], and locales are kinds of [[spaces]].  So, if you adopt locales as models for spaces, then your models for [[subspaces]] are [[sublocales]] or, dually, [[quotient object|quotient]] frames.  However, much as a [[quotient set]] can be described by an [[equivalence relation]] on the original [[set]], so a quotient frame may be described by an appropriate [[structure]] on the original frame.  That structure is a _nucleus_.

Thus, nuclei correspond to [[sublocales]].


## Definitions

Let $L$ be a [[frame]], that is a [[suplattice]] satisfying the infinite distributivity law.

A __nucleus__ on $L$ is a [[function]] $j\colon L \to L$ that satisfies the following identities:

1.  $j(a \wedge b) = j(a) \wedge j(b)$,
2.  $a \leq j(a)$,
3.  $j(j(a)) \leq j(a)$.

In other words, a nucleus on $L$ is a [[meet]]-preserving [[monad]] on $L$.

Note that the following properties of a nucleus might be included in the definition, but they follow from the above:

1.  $j(\top) = \top$,
2.  $j(a) \leq j(b)$ if $a \leq b$,
3.  $j(j(a)) = j(a)$.


## The subset of closed elements

Let $L$ be a frame.

As a nucleus $j$ on $L$ (being a monad on a [[poset]]) is a kind of [[Moore closure]], we say that an element $a$ of $L$ is __$j$-closed__ if $j(a) = a$.  (But note that this has nothing to do with the [[closed subspaces]] of the locale $L$.)

We may equivalently define a nucleus on $L$ to be a [[subset]] $J$ of $L$ that satisfies certain conditions, namely these identities:

1.  $\bigwedge A \in J$ whenever $A \subseteq J$ (using that $L$ is a [[complete lattice]]),
2.  $a \Rightarrow b \in J$ whenever $b \in J$ (using that $L$ is a [[Heyting algebra]]).

Then we recover $j\colon L \to L$ by

$$ j(a) \coloneqq \bigwedge \{ b\colon L \;|\; b \in J,\; a \leq b \} $$

and we have

$$ J = \{ a \colon L \;|\; j(a) = a \} .$$

+-- {: .query}
Check all this, and expand on it if necessary.
=--

This approach to nuclei is not appropriate in a [[predicative mathematics|predicative]] approach to topology, where we want to use [[large category|large]] (but [[accessible category|accessible]]) frames, which may not be meet-complete.


## Quotient frames and sublocales

Let $L$ be a frame, and let $j$ be a nucleus on $L$.

Let $L/j$ be the [[subset]] of $L$ consisting of the $j$-closed elements of $L$ (those elements $a$ such that $j(a) = a$).  Note that, by property (3) above, we may interpret $j$ as a function $j^*\colon L \to L/j$, which is a [[surjection|surjective]] frame [[homomorphism]].  Since [[Frm]] is an [[algebraic category]], this means that $L/j$ is a [[regular quotient]] of $L$.

Conversely, suppose that $M$ is any regular quotient of $L$; that is, we have a surjective frame homomorphism $k\colon L \to M$.  Since $k$ is a frame homomorphism, it has (by the [[adjoint functor theorem]]) a [[right adjoint]] $k_*\colon M \to L$.  Let $j\colon L \to L$ be the [[composite]] of $k$ followed by $k_*$.  Then $j$ is a nucleus, and $k_*$ is an [[embedding]] (in [[Pos]], not $Frm$) whose [[image]] is $L/j$.

In short, given a nucleus $j$, we have an [[adjunction]] $j^*\colon L \rightleftarrows L/j: j_*$, where $j^*$ is a surjective homomorphism and $j_*$ is the [[inclusion function]]; while, given a surjective homomorphism $k$, we have an adjunction $k\colon L \rightleftarrows M: k_*$, where $k_* \circ k$ is a nucleus and $k_*$ is an embedding.

If we think of $L$ as a [[locale]], then we define a __[[sublocale]]__ of $L$ to be a quotient frame of $L$, which corresponds to a nucleus on $L$ as above.


## Categorification

If you [[categorify]] from locales to [[toposes]], then nuclei become [[Lawvere–Tierney topologies]], and the operation of the nucleus becomes [[sheafification]].


## References

* _[[Stone Spaces]]_, II.2


[[!redirects nucleus]]
[[!redirects nucleuses]]
[[!redirects nuclei]]
