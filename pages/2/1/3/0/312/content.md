# Definition #

In category theory, a **subobject** of an object $c$ of a category $C$ is an isomorphism class of [[monomorphism|monos]] $i: a \to c$ into $c$. (Two morphisms $i: a \to c$, $j: b \to c$ are _isomorphic_ if there exists an isomorphism $k: a \to b$ such that $i = j k$.)

Monos into an object $c$ are [[preorder|preordered]] by a relation
$$(i: a \to c) \leq (j: b \to c)$$
defined by the condition that there exists $k: a \to b$ such that $i = j k$. (There is at most one such $k$ since $j$ is monic, and such $k$ is monic since $i$ is monic.) A subobject of $c$ may equivalently be defined as an element of the posetal reflection of this preorder.  

# Restated in terms of over categories #

Let $C_c$ be the [[full subcategory]] of the [[over category]] $C/c$ on monomorphisms. Then $C_c$ is the [[partial order|poset]] of subobjects of $c$ and the set of isomorphism classes of $C_c$ is the set of subobjects of $c$.

# Generalizations #

* More generally, in some contexts we may take "subobject" to mean an isomorphism class of morphisms $i: a\to c$ satisfying some suitable condition other than being a monomorphism (usually a stronger one).  Common choices are [[strong monomorphism]]s, [[regular monomorphism]]s, or the right class of some [[orthogonal factorization system]].  (The latter choice has the advantage that then [[image]]s will automatically exist.)

  * For example, in [[Top]] a monomorphism is just an injective function, whereas the strong and regular monomorphisms coincide and are the subspace embeddings.  In some contexts at least, one can argue that subspace embeddings are a more appropriate notion of "subobject" in $Top$ (for example, if one wants to exhibit it as a [[locally bounded category]]).  A similar thing happens in a [[quasitopos]].

* The [[partial order]] on the collection of subobjects internalizes into contexts more general than [[Set]]. For instance in every [[topos]] the [[subobject classifier]] $\Omega$ has the structure of an internal poset (see there).


# Comparison with the notion of "subset" #

The notion of subobject figures prominently in [[topos]] theory and in other approaches to [[set theory]] based on categories. It is not an exact translation of the usual notion of "subset" in traditional set theory; in ordinary set theory, the notion of subset is defined in terms of a global elementhood relation between sets, which one doesn't have in categorical set theory (and which one wouldn't necessarily want: it's "[[evil|evil]]" in the sense of not being invariant with respect to isomorphism).

Category-theoretically, the traditional notion of subset gives a way of picking out a canonical representative or "normal form" among all the monos in an isomorphism class. As we intimated, there is no intrinsic way of defining such representatives in the theory of toposes: such would have to be considered an extra structure on a topos. Mathematically, there is no particular gain in having such structure around; at best it enables a traditional mode of discourse in which subsets are concrete maps, and to this end it can function as a linguistic or psychological convenience.

On the other hand, there is no particular harm either in having such structure around, as long as one remembers that it is not an isomorphism invariant.  People will instinctively turn to canonical representatives whenever they can -- think of what we would tell a student who asks for help understanding how to multiply elements in $\mathbb{Z}_13$ -- and even category theorists do so when they are available.

+--{.query}
_Todd_: I agree with everything in this last comment, but the tone could be misconstrued as ever-so-slightly pejorative or condescending. One could just as well say that there is no particular harm either in having such structure around, as long as one remembers that it is not an isomorphism invariant. 

My own guess is that people will instinctively turn to canonical representatives whenever they can -- think of what we would tell a student who asks for help understanding how to multiply elements in $\mathbb{Z}_13$. And for students of topos theory, too, it probably helps to keep it concrete whenever possible. So while we tell them that in abstract topos theory, we define subobjects this way, we should encourage them to think of e.g. [[sieve]]s in a Grothendieck topos in whatever terms are comfortable to them, e.g. as a subfunctor whose components are 'literal' subset inclusions. And not to give off whiffs of "well, if you really feel you need this psychological crutch, go right ahead, but it's not 'categorially correct' to do so" -- because I think if we are honest, we admit to doing the same things ourselves in visualizing mathematics. 

_Toby_:  How\'s this?
=--
