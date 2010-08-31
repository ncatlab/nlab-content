## Warning

The term 'topological category' is traditional, and comes from the frequent examples in [[topology]].  It does *not* mean an [[internal category]] or [[enriched category]] in [[Top]]!  (Fortunately the term [[topological groupoid]] is not taken by this tradition; indeed, the only groupoid that is a topological category over $Set$ is [[terminal category|trivial]].  On the other hand, they do seem to use the term 'topological functor', which here we avoid.)




## Idea

A _topological category_ is a [[concrete category]] with nice features matching the ability to form 'weak' and 'strong' topologies in [[Top]].


## Definition

Most generally, the definition relates to a [[functor]] $U: C \to D$ (such as the [[forgetful functor]] from $Top$ to [[Set]]), but one can think of this as giving $C$ as a [[bundle]] over $D$.  Usually $C$ and $D$ will be [[large categories]].  Let a _space_ be an object of $C$, an _algebra_ be an object of $D$, a _map_ be a morphism in $C$, and a _homomorphism_ be a morphism in $D$.  (The reason is that, typically, $C$ will be a category of spaces with some kind of topological structure while $D$ will be, if not $Set$, then some kind of algebraic category.)

Then $C$ is a __topological category__ over $D$ if, given any algebra $X$ and any (possibly large) family of spaces $S_i$ and homomorphisms $f_i: X \to U(S_i)$ (that is a [[sink|source]] from $X$), there exist
*  a space $T$, an [[isomorphism]] $g: U(T) \to X$, and maps $m_i: T \to S_i$ such that each [[composite]] $g ; f_i$ equals $U(m_i)$ and,
*  given any space $T'$, homomorphism $g': U(T') \to X$, and maps $m'_i: T' \to S_i$, if each composite $g' ; f_i$ equals $U(m'_i)$, then there exists
   *  a map $n: T' \to T$ such that $U(n) ; g = g'$ and
   *  given any map $n': T' \to T$, if $U(n') ; g = g'$, then $n = n'$.

Here are some illustrative commutative diagrams (if you can read them):
$$ \array {
T' \\
n \downarrow \downarrow n' & \searrow^{m'_i} \\
T                          & \underset{m_i}\rightarrow & S_i
} \;\;\; \stackrel{U}\mapsto \;\;\; \array {
U(T') \\
U(n) \downarrow \downarrow U(n') & \searrow^{g'}                         &                                  & \searrow^{U(m'_i)} \\
U(T)                             & \overset{\sim}\underset{g}\rightarrow & X                                & \underset{f_i}\rightarrow & U(S_i) \\
                                 &                                       & \underset{U(m_i)}\longrightarrow
} $$


It follows by a clever argument that $U: C \to D$ must be [[faithful functor|faithful]]; see Theorem 21.3 of [ACC][acc].  That is also often included in the definition, in which case the uniqueness of $n$ can be left out.  Thus we may think of objects of $C$ as objects of $D$ equipped with [[extra structure]].  The idea is then that $T$ is $X$ equipped with the __intitial structure__ or __[[weak structure]]__ determined by the requirement that the homomorphisms $f_i$ be structure-preserving maps.

The dual concept could be called a _cotopological category_.  However, this is not actually anything new; $U: C \to D$ is topological if and only if $U^op: C^op \to D^op$ is.  This is a [[categorification]] of the theorem that any complete [[semilattice]] is a [[complete lattice]].  Thus, every topological category also has __final__ (not usually called _terminal_) or __[[strong structure|strong]]__ structures, each determined by a family of homomorphisms $f_i: U(S_i) \to X$ (a [[sink]] to $X$).

Both of these results (faithfulness and self-duality) depend on the fact that we have allowed the family $\{S_i\}$ to be potentially *large*.  Counterexamples are easy to find.  For instance, if $C$ is a large category with all (small) products, then the functor $C\to 1$ to the [[terminal category]] satisfies the above lifting property for small families $\{S_i\}$.  However, it need not satisfy the dual property (unless $C$ also has all small coproducts) nor need it be faithful.

It also follows that $U$ is a [[Grothendieck fibration|fibration]] and opfibration, in the weakened bicategorical sense of Street.  One also often assumes in the definition $U(T) = X$ and that $g$ is the [[identity morphism]], which in particular makes $U$ into a fibration in the original sense of Grothendieck.  This is a bit [[evil]], but it is convenient and satisfied in almost all examples, and any example not satisfying it is equivalent to one which does (via fibrant replacement by an [[isofibration]]).


## Examples

*  The name 'topological category' comes from these examples from point-set [[topology]]; these are all topological over [[Set]]:
   *  the category [[Top]] of [[topological space]]s,
   *  the category of [[convergence space]]s (or of [[pseudotopological space|pseudotopological]] or of [[pretopological space|pretopological]] spaces),
   *  the category of [[uniform space]]s or of [[Cauchy space]]s,
   *  lots more in this vein.
*  In contrast, the category of [[locale]]s is *not* topological over $Set$, apparently not even the category of *spatial* locales (equivalent to the category of [[sober space]]s), essentially because soberification of a topological space may not preserve the underlying set.
*  Also, the category [[Diff]] of smooth [[manifold]]s is not topological but most categories of [[generalized smooth space]]s are.
   +-- {: .query}
   [[Andrew Stacey]]:
   All of the categories listed on [[generalized smooth space]] are concrete and are topological over Set: all admit discrete and indiscrete structures (only constant maps and all maps respectively).

   There are non-set based generalisations but the current flavour of [[generalized smooth space]] is set-based.

   _Toby_:  Sorry, I should have checked there.  Of course, these about *concrete* sheaves; I knew that once!
   =--
*  Outside of topology, the category of [[measurable space]]s is topological over $Set$.
*  The category of [[topological group]]s is topological over [[Grp]], the category of [[topological vector space]]s is topological over $\mathbb{R}$-[[Vect]], etc.


## Further properties

*  If $C$ is topological over $D$, then so is any full [[retract]] of $C$, as long as the functors involved live in $Cat$/$D$.
*  In particular, a [[reflective subcategory|reflective]] or [[coreflective subcategory|coreflective]] subcategory of $C$ is topological, as long as the reflectors or coreflectors become [[identity morphism]]s in $D$.
*  The forgetful functor $U: C \to D$ is not only faithful but also (for different reasons) [[essentially surjective functor|essentially surjective]].  Thus it is never [[full functor|full]] (except in the trivial case where $U$ is an [[equivalence of categories|equivalence]], of course).
*  If $D$ is [[complete category|complete]] or [[cocomplete category|cocomplete]], then so is $C$.
*  If $D$ is [[well-powered category|well-powered]] or co-well-powered, then so is $C$.
*  If $D$ is [[concrete category|concrete]], then so is $C$.  More generally, if $D$ has a [[generator]], then $C$ is concrete over $D$.
*  In particular, if $D$ is [[Set]], then $C$ is a concrete category that is complete, cocomplete, well powered, and well copowered.


## Special cases

*  If $X$ is any algebra, then there is a _[[discrete space]]_ over $X$ induced by the empty family of maps.  Similarly, we have an _indiscrete space_ with the final structure induced by no maps.  This defines functors $disc, indisc: D \to C$ that are respectively left and right [[adjunct]]s of $U$.
*  Suppose that $D$ has an [[initial object]] $0_D$.  Then the discrete space $0_C$ over $0_D$ is initial in $C$.  Similarly, the indiscrete space over a [[terminal object]] in $D$ is terminal in $C$.
*  More generally, suppose that $D$ has [[product]]s or [[coproduct]]s (indexed by whichever [[cardinal number|cardinalities]] you may wish to consider).  Then $C$ also has (co)products, lying over the (co)products in $D$, with structures induced by the product projections or coproduct inclusions.
*  More general [[limit]]s and [[colimit]]s are constructed in a similar way.  We say that $U$ _creates_ (co)limits in $C$.
*  If a single algebra $X$ has been given the structure of several spaces, then there are a _supremum_ structure and an _infimum_ structure on $X$ induced (as the initial and final structures) by the various incarnations of its [[identity morphism|identity]] homomorphism.  Exploiting this shows how to construct final structures out of initial ones and conversely.
*  If $X$ is a [[regular monomorphism|regular]] [[subobject|subalgebra]] of some $U(S)$, then the inclusion homomorphism makes $X$ into a _subspace_ of $S$, which is also a subobject in $C$.  Every regular subobject of $S$ is of this form; note however that there may be nonregular subobjects in $C$ even if all subobjects in $D$ are regular.

## Discussion


Here is some old discussion about terminology

+-- {: .query}
[[David Roberts]]: How about saying _a category is topological_ instead of/as well as topological category? From the other side, people (used to) refer to _continuous categories_ when talking about categories in Top. This brings clashes of its own, when extending this to continuous functors!

_Toby_:  Yeah, we need a better name.  But 'topological category' seems firmly entrenched; even my phrasing '$C$ is topological over $D$' is something that I\'ve never seen in the wild.  Perhaps something that focuses on the forgetful functor $U: C \to D$?  (But 'topological functor' and 'topological bundle' have their own meanings that we don\'t want to mess with.)

I\'m hoping that somebody will come up with a good suggestion, actually.

[[Tim Porter|Tim]]: On the terminology, a category as such is NOT 'topological'.  Pedantically a concrete category can be topological, but this requires that the $U : C\to sets$ is specified. Adamek, Herrlich
and Strecker, in their book ACC (see references) use _topological concrete category_ in the index, although slip back to _topological category_ in the main discussion. Perhaps that is the solution.
_Thinks: stuff, structure, properties!!!!!_

_Toby_:  Your pedantic point is acknowledged below; more importantly, I like your suggested terminology.  It\'s not perfect, as $C$ can be topological over $D$ without either being concrete (although perhaps we should say that $C$ is concrete over $D$? what would that mean exactly?), but it solves the problem of what to call the page, I think.  (Since page moves are easily reversible, I\'ll move it to [[topological concrete category]] now, but other good suggestions are still welcome!)

Update:  Looks like ACC uses 'topological functor' too; let\'s just avoid that, shall we?
=--

## References

I should find some ... I used [[HAF]] (Section 9.15) and the English Wikipedia (on [topological vector spaces](https://secure.wikimedia.org/wikipedia/en/wiki/Topological_vector_space)) as reminders, but there not good for much more than that.

The Wikipedia entry on [Category of topological spaces](http://en.wikipedia.org/wiki/Category_of_topological_spaces) contains some references, including

* Ji&#345;&#237; Ad&#225;mek, Horst Herrlich, & George E. Strecker; 1990; Abstract and Concrete Categories; originally published John Wiley & Sons ISBN 0-471-60922-6; [free on-line edition](http://katmat.math.uni-bremen.de/acc) (4.2MB PDF).

[acc]: http://katmat.math.uni-bremen.de/acc "Abstract and Concrete Categories"

[[!redirects topological concrete categories]]
[[!redirects topological category]]
[[!redirects topological categories]]
[[!redirects topological functor]]
