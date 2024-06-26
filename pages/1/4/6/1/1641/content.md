
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

* table of contents
{: toc}

## Warning

The term 'topological category' is traditional, and comes from the frequent examples in [[topology]].  It does *not* mean an [[internal category]] or [[enriched category]] in [[Top]] (a [[topologically enriched category]])!  (Fortunately the term [[topological groupoid]] is not taken by this tradition; indeed, the only groupoid that is a topological category over $Set$ is [[terminal category|trivial]].  On the other hand, there is use of the term 'topological functor', which  we tend to  avoid other than below.)


## Idea

A _topological category_ is a [[concrete category]] with nice features matching the ability to form [[weak topology|weak]] and [[strong topology|strong]] topologies in [[Top]].


## Definition

### Default version

Most generally, the definition relates to a [[functor]] $U\colon C \to D$ (such as the [[forgetful functor]] from $Top$ to [[Set]]), but one can think of this as giving $C$ as a [[bundle]] over $D$. Sometimes, when $D$ is in fact [[Set]], the category $C$ satisfying the properties described belows is called a _topological construct_ [(Preuss)](#Preuss). Usually $C$ and $D$ will be [[large categories]].

By a _space_ we will mean an object of $C$, and by an _algebra_ we will mean an object of $D$.  By a _map_ we will mean a morphism in $C$, and by a _homomorphism_ we will mean a morphism in $D$.  (The reason is that, typically, $C$ will be a category of spaces with some kind of topological structure while $D$ will be, if not $Set$, then some kind of algebraic category.)

Then $C$ is a __topological category__ over $D$ if, given any algebra $X$ and any (possibly large) family of spaces $S_i$ and homomorphisms $f_i\colon X \to U(S_i)$ (that is, a "$U$-structured" [[sink|source]] from $X$), there exists an [[initial lift]] (think: "smallest topology rendering the $f_i$ continuous"), which is to say

*  a space $T$ such that $U(T)=X$, and maps $m_i\colon T \to S_i$ such that $U(m_i) = f_i$, and

*  given any space $T'$, homomorphism $g'\colon U(T') \to X$, and maps $m'_i\colon T' \to S_i$, if each composite $g' ; f_i$ equals $U(m'_i)$, then there exists a unique map $n\colon T' \to T$ such that $U(n) = g'$ and $n ; m_i = m'_i$.

Here are some illustrative commutative diagrams (if you can read them):
$$ \array {
T' \\
n \downarrow \downarrow n' & \searrow^{m'_i} \\
T                          & \underset{m_i}\rightarrow & S_i
} \;\;\; \stackrel{U}\mapsto \;\;\; \array {
U(T') \\
U(n) \downarrow \downarrow U(n') & \searrow^{g'}                         &                                  & \searrow^{U(m'_i)} \\
U(T)                             & = & X                                & \underset{f_i}\rightarrow & U(S_i) \\
                                 &                                       & \underset{U(m_i)}\longrightarrow
} $$

It follows by a clever argument that $U\colon C \to D$ must be [[faithful functor|faithful]]; see Theorem 21.3 of [ACC][acc].  That is also often included in the definition, in which case the uniqueness of $n$ can be left out.  Thus we may think of objects of $C$ as objects of $D$ equipped with [[extra structure]].  The idea is then that $T$ is $X$ equipped with the __initial structure__ or __[[weak structure]]__ determined by the requirement that the homomorphisms $f_i$ be structure-preserving maps.

The dual concept could be called a _cotopological category_.  However, this is not actually anything new; $U\colon C \to D$ is topological if and only if $U^op\colon C^op \to D^op$ is.  This is a [[categorification]] of the theorem that any complete [[semilattice]] is a [[complete lattice]].  Thus, every topological category also has __final__ (not usually called _terminal_) or __[[strong structure|strong]]__ structures, each determined by a family of homomorphisms $f_i\colon U(S_i) \to X$ (a $U$-structured [[sink]] to $X$).

Both of these results (faithfulness and self-duality) depend on the fact that we have allowed the family $\{S_i\}$ to be potentially *large*.  Counterexamples are easy to find.  For instance, if $C$ is a large category with all (small) products, then the functor $C \to 1$ to the [[terminal category]] satisfies the above lifting property for small families $\{S_i\}$.  However, it need not satisfy the dual property (unless $C$ also has all small coproducts) nor need it be faithful.

It also follows that $U$ is a [[Grothendieck fibration]] and opfibration.

### Amnestic version

Since initial lifts have a universal property, they are unique up to unique isomorphism.  However, it is traditional in some literature to ask that they be literally unique (this is done for instance in [ACC][acc]). This is tantamount to deciding that $U$ should be an [[amnestic functor]].  A drawback (from an [[nPOV]]) is that this condition violates the [[principle of equivalence]], and arguably doesn't add anything mathematically important.

Thus, although it occurs in the literature, here we will consider it purely optional. (It is possible that some results recorded here about topological categories will depend on this assumption, but only results not respecting the [[principle of equivalence]] could be affected.)


### Weak version

On the other hand, the default definition above does already refer to equality of objects in the condition $U(T)=X$; thus as stated it *already* violates the [[principle of equivalence]], just as the notion of [[Grothendieck fibration]] does.  But (also as for Grothendieck fibrations) this other use of equality of objects is really more of a "typing judgment", which can be made precise by working with [[displayed categories]] instead.  (In the context of [[homotopy type theory]], the amnestic condition is equivalent to "fiberwise [[internal category in homotopy type theory|univalence]]".)

However, if we want to, we can also formulate a "fully isomorphism-invariant" version of the definition, corresponding to the weakened bicategorical notion of [[Street fibration]].  In this case, an initial lift consists of:

*  a space $T$, an [[isomorphism]] $g\colon U(T) \to X$, and maps $m_i\colon T \to S_i$ such that each [[composite]] $g ; f_i$ equals $U(m_i)$ and,

*  given any space $T'$, homomorphism $g'\colon U(T') \to X$, and maps $m'_i\colon T' \to S_i$, if each composite $g' ; f_i$ equals $U(m'_i)$, then there exists a unique map $n\colon T' \to T$ such that $U(n) ; g = g'$ and $n ; m_i = m'_i$.

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



## Examples

*  The name 'topological category' comes from these examples from point-set [[topology]]; these are all topological over [[Set]]:
   *  the category [[Top]] of [[topological spaces]],
   *  the category of [[convergence spaces]] (or of [[pseudotopological space|pseudotopological]] or of [[pretopological space|pretopological]] spaces),
   *  the category of [[uniform spaces]] or of [[Cauchy spaces]],
   *  lots more in this vein.

*  In contrast, the category of [[locales]] is *not* topological over $Set$, apparently not even the category of *spatial* locales (equivalent to the category of [[sober spaces]]), essentially because soberification of a topological space may not preserve the underlying set.

*  Also, the category [[Diff]] of [[smooth manifolds]] is not topological but most categories of [[generalized smooth space]]s are.

*  Outside of topology, the category of [[measurable spaces]] is topological over $Set$.

*  The category of [[topological groups]] is topological over [[Grp]], the category of [[topological vector spaces]] is topological over $\mathbb{R}$-[[Vect]], etc.


## Further properties

*  If $C$ is topological over $D$, then so is any full [[retract]] of $C$, as long as the functors involved live in $Cat/D$.

*  In particular, a [[reflective subcategory|reflective]] or [[coreflective subcategory|coreflective]] subcategory of $C$ is topological, as long as the reflectors or coreflectors become [[identity morphisms]] in $D$.

*  The forgetful functor $U\colon C \to D$ is not only faithful but also (because every algebra must have an initial/indiscrete topology determined by the empty source) [[essentially surjective functor|essentially surjective]] (in fact surjective on the nose for the non-weak definitions).  Thus it is never [[full functor|full]] (except in the trivial case where $U$ is an [[equivalence of categories|equivalence]], of course).

*  If $D$ is [[complete category|complete]] or [[cocomplete category|cocomplete]], then so is $C$.

* If $D$ is [[total category|total]] or cototal, then so is $C$; see [[solid functor]].

* If $D$ is [[mono-complete category|mono-complete]] or epi-cocomplete, then so is $C$.

*  If $D$ is [[well-powered category|well-powered]] or co-well-powered, then so is $C$.

* If $D$ has a [[factorization structure for sinks]] $(E,M)$, then $C$ has one $(E',M')$, where $M'$ is the collection of morphisms in $C$ lying over $M$-morphisms in $D$, and $E'$ the collection of *final* sinks in $C$ lying over $E$-sinks in $D$.  This generalizes the lifting of [[orthogonal factorization systems]] along [[Grothendieck fibrations]].

*  If $D$ is [[concrete category|concrete]], then so is $C$.  More generally, if $D$ has a [[generator]], then $C$ is concrete over $D$.

*  In particular, if $D$ is [[Set]], then $C$ is a concrete category that is complete, cocomplete, well powered, and well copowered.

## Functors

* A functor $F\colon C\to C'$ between topological concrete categories $C/D$, $C'/D$ with the same base category $D$ preserves initial lifts iff it is right adjoint. It preserves final lifts iff it is left adjoint.

* More generally: If a functor $F\colon C\to C'$ between topological concrete categories $C/D$, $C'/D'$ with different base categories lying over a functor $F_0: D\to D'$. If $F$ is right (left) adjoint, then $F_0$ is right (left) adjoint and $F$ preserves initial (final) lifts. A partial converse holds: If $F_0$ is right (left) adjoint to $G_0$ and $F$ preserves initial (final) lifts, then there is functor $G$ lying over $G_0$ so that $F$ is right (left) adjoint to $G_0$.


## Special cases

*  If $X$ is any algebra, then there is a _[[discrete space]]_ over $X$ induced by the empty family of maps.  Similarly, we have an _indiscrete space_ with the final structure induced by no maps.  This defines functors $disc, indisc\colon D \to C$ that are respectively left and right [[adjoint functor|adjoints]] of $U$.

*  Suppose that $D$ has an [[initial object]] $0_D$.  Then the discrete space $0_C$ over $0_D$ is initial in $C$.  Similarly, the indiscrete space over a [[terminal object]] in $D$ is terminal in $C$.

*  More generally, suppose that $D$ has [[products]] or [[coproducts]] (indexed by whichever [[cardinal number|cardinalities]] you may wish to consider).  Then $C$ also has (co)products, lying over the (co)products in $D$, with structures induced by the product projections or coproduct inclusions.

*  More general [[limits]] and [[colimits]] are constructed in a similar way.  However, it is _not_ typically the case that $U$ _[[created limit|creates]]_ (co)limits in $C$ because creation of a limit requires that every preimage of the limiting cone is limiting. This fails for $U: \mathrm{Top} \to \mathrm{Set}$ since we can coarsen the topology on the limit vertex to obtain a counterexample.

*  If a single algebra $X$ has been given the structure of several spaces, then there are a _[[supremum]]_ structure and an _[[infimum]]_ structure on $X$ induced (as the initial and final structures) by the various incarnations of its [[identity morphism|identity]] homomorphism.  Exploiting this shows how to construct final structures out of initial ones and conversely.

*  If $X$ is a [[regular monomorphism|regular]] [[subobject|subalgebra]] of some $U(S)$, then the inclusion homomorphism makes $X$ into a _[[subspace]]_ of $S$, which is also a subobject in $C$.  Every regular subobject of $S$ is of this form; note however that there may be nonregular subobjects in $C$ even if all subobjects in $D$ are regular.

## Familiarly fibrations

The theory of topological functors can be developed along the lines of Grothendieck's theory of fibrations, where  _cartesian morphisms_  are replaced by  _cartesian families_. In this way just as by definition  "A functor is a _fibration_ if it creates cartesian morphisms and cartesian morphism compose", there is the definition "A functor is _topological_  if it creates cartesian families and cartesian families compose". 

## References

* [[Jiří Adámek]], Horst Herrlich, & George E. Strecker; 1990; Abstract and Concrete Categories; originally published John Wiley & Sons ISBN 0-471-60922-6; [free on-line edition][acc] (4.2MB PDF).

[acc]: http://katmat.math.uni-bremen.de/acc "Abstract and Concrete Categories"


* Gerhard Preuss; 2002; _Foundations of Topology: An Approach to Convenient Topology_; Kluwer ISBN 1-4020-0891-0.
 {#Preuss}

* [[Richard Garner]], *Topological functors as total categories*, [TAC](http://www.tac.mta.ca/tac/volumes/29/15/29-15abs.html)

* [[Eduardo J. Dubuc]], Luis Espa&#241;ol, *Topological functors as familiarly fibrations* 
[arXiv](https://arxiv.org/abs/math/0611701) (2006)

* J. Martin Harvey, _Topological functors from factorization_, Categorical Topology: Proceedings of the International Conference, Berlin, August 27th to September 2nd, 1978. Springer Berlin Heidelberg, 1979.

[[!redirects topological concrete category]]
[[!redirects topological concrete categories]]

[[!redirects topological construct]]
[[!redirects topological constructs]]

[[!redirects topological category]]
[[!redirects topological categories]]

[[!redirects topological functor]]
[[!redirects topological functors]]