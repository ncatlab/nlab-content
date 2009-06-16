## Warning

The term 'topological category' is traditional, and comes from the frequent examples in [[topology]].  It does *not* mean an [[internal category]] in [[Top]]!


## Idea

A _topological category_ is a [[concrete category]] with nice features matching the ability to form 'weak' and 'strong' topologies in [[Top]].


## Definition

Most generally, the definition relates to a [[functor]] $U: C \to D$ (such as the [[forgetful functor]] from $Top$ to [[Set]]), but we think of this as giving $C$ as a [[bundle]] over $D$.  Let a _space_ be an object of $C$, an _algebra_ be an object of $D$, a _map_ be a morphism in $C$, and a _homomorphism_ be a morphism in $D$.  (The reason is that, typically, $C$ will be a category of spaces with some kind of topological structure while $D$ will be, if not $Set$, then some kind of algebraic category.)

Then $C$ is a __topological category__ over $D$ if, given any algebra $X$ and any (small) family of spaces $S_i$ and homomorphisms $f_i: X \to U(S_i)$, there exist
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


Here are some immediate consequences:
*  One may assume that $U(T) = X$ and that $g$ is the [[identity morphism]]; that\'s usually included in the definition, which is a bit [[evil]].
*  The forgetful functor $U: C \to D$ must be [[faithful functor|faithful]]; that\'s also often in the definition, in which case the uniqueness of $n$ can be left out.  Thus we may think of objects of $C$ as objects of $D$ equipped with [[extra structure]].

The idea is that $T$ is $X$ equipped with the __intitial structure__ or __weak structure__ determined by the requirement that the homomorphism $f_i$ be structure-preserving maps.


## Examples

*  The name 'topological category' comes from these examples from point-set [[topology]]; these are all topological over [[Set]]:
   *  the category [[Top]] of [[topological space]]s,
   *  the full subcategory of [[Hausdorff space]]s (similarly for other [[separation axioms]]),
   *  the category of [[convergence space]]s (or of [[pseudotopological space|pseudotopological]] or of [[pretopological space|pretopological]] spaces),
   *  the category of [[uniform space]]s or of [[Cauchy space]]s,
   *  lots more in this vein.
*  In contrast, the category of [[locale]]s is *not* topological over $Set$, although the category of *spatial* locales (equivalent to the category of [[sober space]]s) is.
*  Outside of topology, the category of [[measurable space]]s is topological over $Set$.
*  The category of [[topological group]]s is topological over [[Grp]], the category of [[topological vector space]]s is topological over $\mathbb{R}$-[[Vect]]$, etc.


## Further properties

*  If $C$ is topological over $D$, then so is any [[reflective subcategory]] of $C$.
*  The forgetful functor $U: C \to D$ is not only faithful but also (for different reasons) [[essentially surjective functor|essentially surjective]].  Thus it is never [[full functor|full]] (except in the trivial case where $U$ is an [[equivalence of categories|equivalence]], of course).
*  If $D$ is [[complete category|complete]], then so is $C$.
*  If $D$ is also [[cocomplete category|cocomplete]] (which may not even be necessary), then $C$ is cotopological; that is, $U^op: C^op \to D^op$ is topological.  In particular, then $C$ is also cocomplete.
*  If $D$ is [[concrete category|concrete]], then so is $C$.
*  In particular, if $D$ is [[Set]], then $C$ is a concrete category that is both complete and cocomplete.
*  Somewhere in there, we also get for free that initial structures also exist that are given by *large* families of homomorphisms.


## Special cases

*  If $X$ is any algebra, then there is a _[[discrete space]]_ over $X$ induced by the empty family of maps.  If $C$ is also cotopological, then we have an _indiscrete space_ as well.
*  Suppose that $D$ has a [[terminal object]] $1_D$.  Then the discrete space $1_C$ over $1_D$ and is terminal in $C$.
*  More generally, suppose that $D$ has [[product]]s (indexed by whichever [[cardinal number|cardinalities]] you may wish to consider).  Then $C$ also has products, lying over the products in $D$, with structure induced by the product projections.
*  More general [[limit]]s are constructed in the same way.  We say that $U$ _creates_ limits in $C$.
*  If a single algebra $X$ has been given the structure of several spaces, then there is a _supremum_ structure on $X$ induced by the various incarnations of its [[identity morphism|identity]] homomorphism.  This is (I guess) a [[categorification]] of the theorem that any complete [[semilattice]] is a [[complete lattice]]; exploiting it shows how to make $C$ cotopological as well as topological.
*  If $X$ is a [[subobject|subalgebra]] of some $U(S)$, then the inclusion homomorphism makes $X$ into a _subspace_ of $S$, which is also a subobject in $C$.  Not every subobject of $S$ is of this form; under at least some conditions, however, every [[regular subobject]] is.


## References

I should find some ... I used [[HAF]] (Section 9.15) and the English Wikipedia (on [topological vector spaces](https://secure.wikimedia.org/wikipedia/en/wiki/Topological_vector_space)) as reminders, but there not good for much more than that.