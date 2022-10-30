
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# $\sigma$-Algebras
* table of contents
{: toc}

## Idea

$\sigma$-algebras and their variants are collections of [[subsets]] important in standard [[measure theory]] and [[probability theory]].

Although $\sigma$-algebras are often introduced as a mere technicality in the definition of [[measurable space]] (to specify the [[measurable subsets]]), even once one has a fixed measurable space $X$, it is often useful to consider additional (smaller) $\sigma$-algebras of measurable subsets of $X$.


## Definitions

We assume the law of [[excluded middle]] throughout; see [[Cheng measurable space]] for the constructive theory.


### Short version

Given a [[set]] $X$, a __$\sigma$-algebra__ is a collection of subsets of $X$ that is closed under [[complement|complementation]], [[countable set|countable]] [[unions]], and countable [[intersections]].

Notice that the [[power set]] $\mathcal{P} X$ of $X$ is a [[Boolean algebra]] under the operations of [[finite set|finitary]] union, intersection, and complementation.  Actually, it is a [[complete lattice|complete]] Boolean algebra, since we can also take arbitrary unions and intersections.  A $\sigma$-algebra is an intermediate notion, since (in addition to being closed under complementation) we only require that it be closed under *countable* unions and intersections.


### Long version

Given a [[set]] $X$ and a collection $\mathcal{M}$ of [[subsets]] $S \subseteq X$, there are really several kinds of collections that $\mathcal{M}$ could be:

*  A __ring__ on $X$ is a collection $\mathcal{M}$ which is closed under [[finite set|finitary]] [[union]] and under [[relative complement]]ation.  That is:

   1.  The [[empty set]] $\empty$ is in $\mathcal{M}$.
   2.  If $S$ and $T$ are in $\mathcal{M}$, then so is their union $S \cup T$.
   3.  If $S$ and $T$ are in $\mathcal{M}$, then so is their relative complement $T \setminus S$.

   It follows that $\mathcal{M}$ is closed under [[inhabited set|inhabited]] finitary intersection and under finitary [[symmetric difference]]:
   *  If $S$ and $T$ are in $\mathcal{M}$, then so is their intersection $S \cap T = T \setminus (T \setminus S)$.
   *  If $S$ and $T$ are in $\mathcal{M}$, then so is their symmetric difference $S \uplus T = (T \setminus S) \cup (S \setminus T)$.

   We can actually use the latter as an alternative to (2), since $S \cup T = (S \uplus T) \uplus (S \cap T)$.  Or we can use the pair as an alternative to (2,3), since $T \setminus S = (S \cap T) \uplus T$.  For that matter, we can weaken (1) to simply say that *some* set $S$ is in $\mathcal{M}$; then $\empty = S \setminus S$.

   While the nullary union and nullary symmetric difference (both the empty set) belong to $\mathcal{M}$, the nullary intersection (which is $S$ itself) might not.  The term 'ring' dates from the days when a [[ring]] in algebra was not assumed to be unital; so a ring on $X$ is simply a subring (in this sense) of the [[Boolean ring]] $\mathcal{P} X$.


*  A __$\delta$-ring__ on $X$ is a ring $\mathcal{M}$ which is closed under countably infinitary intersection.  That is:
   1.  The [[empty set]] $\empty$ is in $\mathcal{M}$.
   2.  If $S$ and $T$ are in $\mathcal{M}$, then so is their union $S \cup T$.
   3.  If $S$ and $T$ are in $\mathcal{M}$, then so is their relative complement $T \setminus S$.
   4.  If $S_1, S_2, S_3, \ldots$ are in $\mathcal{M}$, then so is their intersection $\bigcap_i S_i$.

   Of course, every $\delta$-ring is a ring, but not conversely.  Actually, if you want to define the concept of $\delta$-ring directly, it\'s quicker if you use the symmetric difference; then (2,3) follow by the reasoning above and the [[idempotent|idempotence]] of intersection (so that $S \cap T = S \cap T \cap T \cap T \cap \cdots$).

   The symbol '$\delta$' here is from German 'Durchschnitt', meaning intersection; it may be used in many contexts to refer to countable intersections.


*  A __$\sigma$-ring__ on $X$ is a ring $\mathcal{M}$ which is closed under countable infintary union.  That is:
   1.  The [[empty set]] $\empty$ is in $\mathcal{M}$.
   2.  If $S$ and $T$ are in $\mathcal{M}$, then so is their union $S \cup T$.
   3.  If $S$ and $T$ are in $\mathcal{M}$, then so is their relative complement $T \setminus S$.
   4.  If $S_1, S_2, S_3, \ldots$ are in $\mathcal{M}$, then so is their union $\bigcup_i S_i$.

   Now (2) is simply redundant; $S \cup T = S \cup T \cup T \cup T \cup \cdots$.  A $\sigma$-ring is obviously a ring, but in fact it is also a $\delta$-ring; $\bigcap_i S_i = (\bigcup_i S_i) \setminus \bigcup_j (\bigcup_i S_i \setminus S_j)$.

   The symbol '$\sigma$' here is from German 'Summe', meaning union; it may be used in many contexts to refer to countable unions.


*  An __algebra__ or __field__ on $X$ is a ring $\mathcal{M}$ to which $X$ itself belongs.  That is:
   1.  The [[empty set]] $\empty$ is in $\mathcal{M}$.
   2.  If $S$ and $T$ are in $\mathcal{M}$, then so is their union $S \cup T$.
   3.  If $S$ and $T$ are in $\mathcal{M}$, then so is their relative complement $T \setminus S$.
   4.  $X$ is in $\mathcal{M}$.

   Actually, (2) is now redundant again; $S \cup T = X \setminus ((X \setminus T) \setminus S)$.  But perhaps more importantly, $\mathcal{M}$ is closed under *absolute* complementation (that is, complementation relative to the entire ambient set $X$); that is:

   *  If $S$ is in $\mathcal{M}$, then so is its complement $\neg{S}$.

   In light of this, the most common definition of algebra is probably to use this fact together with (1,2); then (3) follows because $T \setminus S = \neg(S \cup \neg{T})$ and (4) follows because $X = \neg\empty$.  On the other hand, one could equally well use intersection instead of union; absolute complements allow the full use of [[de Morgan duality]].

   The term 'field' here is even more archaic than the term 'ring' above; indeed the only field in this sense which is a [[field]] (in the usual sense) under symmetric difference and intersection is the field $\{\empty, X\}$ (for an [[inhabited set]] $X$).


*  Finally, a __$\sigma$-algebra__ or __$\sigma$-field__ on $X$ is a ring $\mathcal{M}$ that is both an algebra and a $\sigma$-ring.  That is:
   1.  The [[empty set]] $\empty$ is in $\mathcal{M}$.
   2.  If $S$ and $T$ are in $\mathcal{M}$, then so is their union $S \cup T$.
   3.  If $S$ and $T$ are in $\mathcal{M}$, then so is their relative complement $T \setminus S$.
   4.  $X$ is in $\mathcal{M}$.
   5.  If $S_1, S_2, S_3, \ldots$ are in $\mathcal{M}$, then so is their union $\bigcup_i S_i$.

   As with $\sigma$-rings, (2) is redundant; as with algebras, it\'s probably most common to use the absolute complement in place of (3,4).  Thus the usual definition of a $\sigma$-algebra states:
   1.  The [[empty set]] $\empty$ is in $\mathcal{M}$.
   2.  If $S$ is in $\mathcal{M}$, then so is its complement $\neg{S}$.
   3.  If $S_1, S_2, S_3, \ldots$ are in $\mathcal{M}$, then so is their union $\bigcup_i S_i$.

   And again we could again just as easily use intersection as union, even in the infinite case.  That is, a $\delta$-algebra is automatically a $\sigma$-algebra, because $\bigcup_i S_i = \neg\bigcap_i \neg{S_i}$.


Any and all of the above notions have been used by various authors in the definition of measurable space; for example, Kolmogorov used algebras (at least at first), and Halmos used $\sigma$-rings.  Of course, the finitary notions (ring and algebra) aren\'t strong enough to describe the interesting features of Lebesgue measure; they are usually used to study very different examples (finitely additive measures).  On the other hand, $\delta$&#8209; or $\sigma$-rings may be more convenient than $\sigma$-algebras for some purposes; for example, vector-valued measures on $\delta$-rings make good sense even when the absolute measure of the whole space is infinite.

Note that the collection of measurable sets with finite measure (in a given [[measure space]]) is a $\delta$-ring, while the collection of measurable sets with $\sigma$-finite measure is a $\sigma$-ring.


### Measurable sets

A __[[measurable space]]__ is usually defined to be a [[set]] $X$ with a $\sigma$-algebra $\mathcal{M}$ on $X$; sometimes one of the more general variations above is used.

In any case, an __$\mathcal{M}$-measurable subset of $X$__, or just a __measurable set__, is any [[subset]] of $X$ that belongs to $\mathcal{M}$.  If $\mathcal{M}$ is one of the more general variations, then we also want some subsidiary notions: $S$ is __relatively measurable__ if $S \cap T$ belongs to $\mathcal{M}$ whenever $T$ does, and $S$ is __$\sigma$-measurable__ if it is a countable union of elements of $\mathcal{M}$.  Notice that every relatively measurable set is measurable iff $S$ is at least an algebra; in any case, the relatively measurable sets form a ($\sigma$)-algebra if $\mathcal{M}$ is at least a ($\delta$)-ring.  Similary, every $\sigma$-measurable set is measurable iff $S$ is at least a $\sigma$-ring; in any case, the $\sigma$-measurable sets form a $\sigma$-ring if $\mathcal{M}$ is at least a $\delta$-ring.

> The terms 'relatively measurable' and '$\sigma$-measurable' are [[Toby Bartels|my own]]; I cannot find them in Halmos.  Since Halmos uses $\sigma$-rings, he has no need to speak of $\sigma$-measurable sets; but that\'s the case where the best terminology is obvious.  He does use relatively measurable sets, but he doesn\'t seem to give them a name.


### Generating $\sigma$-algebras

As a $\sigma$-algebra is a collection of subsets, we might hope to develop a theory of [[base|bases]] and [[subbase|subbases]] of $\sigma$-algebras, such as is done for [[topological space|topologies]] and [[uniform space|uniformities]].  However, things do not work out as nicely.  (It *is* quite easy to generate rings or algebras, but generating $\delta$-rings and $\sigma$-rings is just as tricky as generating $\sigma$-algebras.)

We do get something by [[general abstract nonsense]], of course.  It\'s easy to see that the [[intersection]] of any collection of $\sigma$-algebras is itself a $\sigma$-algebra; that is, we have a [[Moore closure]].  So given any collection $\mathcal{B}$ of sets whatsoever, the intersection of all $\sigma$-algebras containing $\mathcal{B}$ is a $\sigma$-algebra, the $\sigma$-algebra __generated__ by $\mathcal{B}$.  (We can similarly define the $\delta$-ring generated by $\mathcal{B}$ and similar concepts for all of the other notions defined above.)

What is missing is a simple description of the $\sigma$-algebra generated by $\mathcal{B}$.  (For a mere algebra, this is easy; any $\mathcal{B}$ can be taken as a _subbase_ of an algebra, the finitary symmetric unions of elements of $\mathcal{B}$ form a _base_ of the algebra, and the finitary intersections of elements of the base form an algebra.  For a ring, the only difference is to use only non-nullary intersections.  But for anything from a $\delta$-ring to a $\sigma$-algebra, nothing like this will work.)


In fact, the question of how to generate a $\sigma$-algebra is the beginning of an entire field of mathematics, [[descriptive set theory]].  For our purposes, we need this much:

*  Start with a collection $\Sigma_0$ (our collection $\mathcal{B}$ above), and let $\Pi_0$ be the collection of the complements of the members of $\Sigma_0$.
*  Let $\Sigma_1$ be the collection of countably infinitary unions of sets in $\Pi_0$, and let $\Pi_1$ be the collection of their complements (the countably infinitary intersections of sets in $\Sigma_0$); even $\Sigma_1 \cup \Pi_1$ is not in general a $\sigma$-algebra.
*  Continue, defining $\Sigma_n$ for all [[natural numbers]] $n$.
*  Let $\Sigma_\omega$ be the union of the various $\Sigma_n$; although this is closed under complement, it is still not in general a $\sigma$-algebra.
*  Continue, defining $\Sigma_\alpha$ for all countable [[ordinal numbers]] $\alpha$.
*  Let $\Sigma_{\omega_1}$ be the union of the various $\Sigma_\alpha$; this is finally a $\sigma$-algebra.

So we need an uncountable number of steps, not just two.


(This is only the beginning of descriptive set theory; our $\Sigma_\alpha$ are their $\Sigma^0_\alpha$ ---except that for some reason they start with $\Sigma^0_1$ instead of $\Sigma^0_0$---, and the subject continues to higher values of the superscript.)

Note that [[countable choice]] is essential here and elsewhere in measure theory, to show that a countable union of a countable union is a countable union.  But the full [[axiom of choice]] is not; in fact, much of descriptive set theory (although this is irrelevant to the small portion above) works better with the [[axiom of determinacy]] instead.


## Examples

*  Of course, the [[power set]] of $X$ is closed under all operations, so it is a $\sigma$-algebra.


*  If $X$ is a [[topological space]], the $\sigma$-algebra generated by the open sets (or equivalently, by the closed sets) in $X$ is the __Borel $\sigma$-algebra__; its elements are called the __[[Borel sets]]__ of $X$. In particular, the Borel sets of [[real numbers]] are the Borel sets in the [[real line]] with its usual topology.

*  In the application of [[statistical physics]] to [[thermodynamics]], we have both a microcanonical [[phase space]] $P$ (typically something like $\mathbb{R}^N$ for $N$ on the order of [[Avogadro's number]]) describing every last detail of a [[physical system]] and a macrocanonical phase space $p$ (typically $\mathbb{R}^2$ or at least $\mathbb{R}^n$ for $n \lt 10$) describing those features of the system that can be measured practically, with a projection $P \to p$.  Then the [[preimage]] under this projection of the Borel $\sigma$-algebra of $p$ is a $\sigma$-algebra on $P$, and the thermodynamic [[entropy]] of the system is (theoretically) its information-theoretic entropy with respect to this $\sigma$-algebra.


*  If a measurable space $(X,\mathcal{M})$ is equipped with a (positive) measure $\mu$, making it into a [[measure space]], then the sets of measure zero form a $\sigma$-[[sigma-ideal|ideal]] of $\mathcal{M}$ (that is an [[ideal]] that is also a sub-$\sigma$-ring).  Let a __[[null set]]__ be *any* set (measurable or not) contained in a set of measure zero; then the null sets form a $\sigma$-ideal in the [[power set]] of $X$.  Call a set __$\mu$-measurable__ if it is the union of a measurable set and a null set; then the $\mu$-measurable sets form a $\sigma$-algebra called the __completion__ of $\mathcal{M}$ under $\mu$.  (Even if $\mathcal{M}$ is only a $\delta$-ring, still the null sets will form a $\sigma$-ring; in any case, we get as completion the same kind of structure as we began with.)

*  In particular, the __Lebesgue-measurable__ sets in the real line are the elements of the completion of the Borel $\sigma$-algebra under [[Lebesgue measure]].


## Alternatives

We are now learning ways to understand measure theory and probability away from the traditional reliance on sets required with $\sigma$-algebras; see [[measurable space]] for other ways to define this concept.  We still need to know what happens to all of the *other* $\sigma$-algebras of measurable sets in a measurable space.  One solution may to use [[quotient space|quotient]] measurable spaces in place of sub-$\sigma$-algebras; see the example of macroscopic entropy above.


[[!redirects sigma-algebra]]
[[!redirects sigma-algebras]]
[[!redirects ∞-algebra]]
[[!redirects ∞-algebras]]
[[!redirects ∞-algebra]]
[[!redirects ∞-algebras]]

[[!redirects delta-algebra]]
[[!redirects delta-algebras]]
[[!redirects ∞-algebra]]
[[!redirects ∞-algebra]]
[[!redirects ∞-algebras]]
[[!redirects ∞-algebras]]

[[!redirects sigma-field]]
[[!redirects sigma-fields]]
[[!redirects ∞-field]]
[[!redirects ∞-fields]]
[[!redirects ∞-field]]
[[!redirects ∞-fields]]

[[!redirects delta-field]]
[[!redirects delta-fields]]
[[!redirects ∞-field]]
[[!redirects ∞-fields]]
[[!redirects ∞-field]]
[[!redirects ∞-fields]]

[[!redirects sigma-ring]]
[[!redirects sigma-rings]]
[[!redirects ∞-ring]]
[[!redirects ∞-rings]]
[[!redirects ∞-ring]]
[[!redirects ∞-rings]]

[[!redirects delta-ring]]
[[!redirects delta-rings]]
[[!redirects ∞-ring]]
[[!redirects ∞-rings]]
[[!redirects ∞-ring]]
[[!redirects ∞-rings]]

[[!redirects relatively measurable subset]]
[[!redirects relatively measurable subsets]]
[[!redirects relatively measurable set]]
[[!redirects relatively measurable sets]]

[[!redirects sigma-measurable subset]]
[[!redirects sigma-measurable subsets]]
[[!redirects ∞-measurable subset]]
[[!redirects ∞-measurable subsets]]
[[!redirects sigma-measurable set]]
[[!redirects sigma-measurable sets]]
[[!redirects ∞-measurable set]]
[[!redirects ∞-measurable sets]]

[[!redirects completion of a sigma-algebra]]
[[!redirects completions of a sigma-algebra]]
[[!redirects completions of sigma-algebras]]
[[!redirects completion of a ∞-algebra]]
[[!redirects completions of a ∞-algebra]]
[[!redirects completions of ∞-algebras]]
