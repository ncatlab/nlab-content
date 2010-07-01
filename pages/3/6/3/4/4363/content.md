# Nuclei
* table of contents
{: toc}

## Idea

Recall that [[frames]] are [[duality|dual]] to [[locales]], and locales are kinds of [[spaces]].  So, if you adopt locales as models for spaces, then your models for [[subspaces]] are [[quotient object|quotient]] frames.  However, much as a [[quotient set]] can be described by an [[equivalence relation]] on the original [[set]], so a quotient frame may be described by an appropriate [[structure]] on the original frame.  That structure is a _nucleus_.

Thus, nuclei correspond to [[sublocale]]s.


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


## Relation to quotient frames

Let $L$ be a frame, and let $j$ be a nucleus on $L$.

Let $L/j$ be the [[subset]] of $L$ consisting of the $j$-closed elements of $L$ (those elements $a$ such that $j(a) = a$).  Note that, by property (3) above, we may interpret $j$ as a function $j\colon L \to L/j$.  In this way, check that $j$ becomes a [[surjection|surjective]] frame [[homomorphism]].  Since [[Frm]] is an [[algebraic category]], this means that $L/j$ is a [[regular quotient]] of $L$.

Conversely, suppose that $M$ is any regular quotient of $L$; that is, we have a surjective frame homomorphism $k\colon L \to M$.  Since $k$ is a frame homomorphism, it has (by the [[adjoint functor theorem]]) a [[left adjoint]] $k^*\colon M \to L$.  Let $j\colon L \to L$ be the [[composite]] of $k$ followed by $k^*$.  Then we may check that $j$ is a nucleus, and $k^*$ is a frame [[isomorphism]] from $M$ to $L/j$.

+-- {: .query}
Make sure that the claims directed to be checked above are straightforward calculations.
=--


## Relation to sublocales

Let $L$ be a [[locale]].  Then we simply *define* a __[[sublocale]]__ of $L$ to be a nucleus on the underlying frame of $L$.

There is nothing to be proved here, but there are ideas to motivate.  The elements of the frame $L$ correspond to opens in the locale $L$.  A subspace of a locale corresponds to a quotient frame, because we identify two opens if they 'agree on the sublocale'.  Given an open $a$, there will always be a largest open that is identified with $a$, so we can also describe a subspace of a locale as an operation that maps each open to its largest representative open.  This map is the nucleus $j$.


## Categorification

If you [[categorify]] from locales to [[toposes]], then nuclei become [[Lawvere–Tierney topologies]].


## References

* _[[Stone Spaces]]_, II.2


[[!redirects nucleus]]
[[!redirects nucleuses]]
[[!redirects nuclei]]
