
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Compact spaces
* table of contents
{: toc}

## Idea
 {#Idea}

A [[topological space]] (or more generally: a [[convergence space]]) is _compact_ if everything converges as much as possible. It is a kind of ultimate topological expression of the general idea of a space being "[[closed space|closed]] and [[bounded set|bounded]]": every [[net]] must accumulate somewhere in the space; by boundedness it cannot escape, and by closure the point is in the space. There is also a notion of compactness for [[locales]].

It is also common to work with _compact [[subsets]]_ of a space.  These are those subsets which are compact spaces with the [[subspace topology]].

One often wishes to study [[compact Hausdorff spaces]].  For locales, one usually speaks of compact [[regular space|regular]] locales; these are equivalent (since every locale is $T_0$ and hence $T_3$ if regular, while every Hausdorff space is $T_3$ if compact) since regularity is easier to formulate and handle than Hausdorffness in locale theory.



## Definitions 

There are many ways to say that a space $X$ is compact. The first is perhaps the most common: 

+-- {: .num_defn #hb}
###### Definition

$X$ is compact iff for every collection of [[open subsets]] whose [[union]] is $X$ (i.e. which _[[covers]]_ $X$), there is a (Kuratowski)-[[finite set|finite]] subcollection which also covers $X$ (i.e. a [[finite cover|finite sub-cover]]).

=--

If [[excluded middle]] is assumed, this is easily seen to be equivalent to: 

+-- {: .num_defn #fip}
###### Definition

$X$ is compact iff for any collection of [[closed subsets]] of $X$ whose [[intersection]] is [[empty set|empty]], some finite subcollection also has empty intersection.

=--

If the [[ultrafilter theorem]] (a weak form of the [[axiom of choice]]) is assumed, compactness can be characterized in terms of [[ultrafilter]] (or ultranet) convergence: 

+-- {: .num_defn #ultrafilter}
###### Definition

$X$ is compact iff every [[ultrafilter]] $\mathcal{U}$ (or ultranet $\nu$) on $X$ [[converges|converges]] to some point $x \in X$, meaning that $\mathcal{U}$ contains the filter of [[neighborhoods]] of $x$ (or that $\nu$ is eventually in any neighbourhood of $x$).

=--

In any case, compactness can be characterized in terms of [[proper filter]] or equivalently (see at _[[eventuality filter]]_) of [[net]] [[convergence]] . 

+-- {: .num_defn #refinement}
###### Definition

$X$ is compact iff every [[proper filter]]/[[net]] on $X$ has a [[convergence|convergent]] proper [[refinement]]/[[subnet]].

=--

This is equivalent to the characterization given in the [Idea-section](#Idea) above:
 
+-- {: .num_defn #clustering}
###### Definition

$X$ is compact iff every proper filter $\mathcal{U}$ (or net $\nu$) on $X$ has a cluster point $x$, meaning that every element of $\mathcal{U}$ meets (has [[inhabited set|inhabited]] intersection with) every neighbourhood of $x$ (or $\nu$ is frequently in every neighbourhood of $x$).

=--

While the usual definitions (\ref{hb}&\ref{fip}) are for [[topological spaces]], the convergence definitions (\ref{ultrafilter}--\ref{clustering}) make sense in any [[convergence space]].

The definition (\ref{hb}) also works for [[locales]], since it refers only to the [[frame]] of open sets.  An equivalent way to phrase it is

+-- {: .num_defn #directed}
###### Definition

$X$ is compact iff given any [[direction|directed]] collection of opens whose union is $X$ (a directed open cover), $X$ belongs to the collection.

=--

As the union is the [[coproduct]] in the [[category of open subsets]] $Op(X)$, we can also say

+-- {: .num_defn #object}
###### Definition

$X$ is compact iff it is a [[compact object]] in $Op(X)$.

=--

Compactness is equivalent to the condition of being "stably closed" (and it is this condition which suggests the correct notion of [[proper map]] in [[algebraic geometry]] and elsewhere):

+-- {: .num_defn #projection}
###### Definition

$X$ is compact iff for any space $Y$, the [[projection map]] $X \times Y \to Y$ out of their [[Cartesian product]] is [[closed map|closed]] (see e.g. [Milne, section 17](#Milne)).

=--

Contrary to possible appearance, the equivalence of this with definition \ref{hb} does not require the axiom of choice; see [this MO question](http://mathoverflow.net/questions/42186/does-compact-iff-projections-are-closed-require-some-form-of-choice/42196) and answers, as well as [this page](/toddtrimble/published/Characterizations+of+compactness). See also the page [[compactness and stable closure]] (under construction).  This equivalence is also true for [[locales]], by way of proper maps; see below.

Closely related to the previous definition, a [[logic]]al characterisation of compactness is used in [[Abstract Stone Duality]]:

+-- {: .num_defn #quantification}
###### Definition

$X$ is compact iff for any space $Y$ and any open subset $U$ of $X \times Y$, the subset
$$ \forall_X U = \{ b : Y \;|\; \forall\; a: X,\; (a, b) \in U \} $$
is open in $Y$.

=--

To remove it from dependence on points, we can also write the definition like this:

+-- {: .num_defn #pointless}
###### Definition
$X$ is compact iff given any space $Y$ and any open $U$ in $X \times Y$, there exists an open $\forall_X U$ in $Y$ that satisfies the [[universal property]] of universal [[quantification]]:
$$ V \subseteq \forall_X U \;\Leftrightarrow\; X \times V \subseteq U $$
for every open $V$ in $Y$.
=--

A [[de Morgan duality|dual]] condition is satisfied by an [[overt space]].


+-- {: .num_remark}
###### Remark
**(differing terminology)**

Some authors use "compact" to mean "compact and [[Hausdorff topological space|Hausdorff]]" (a much [[nice topological space|nicer sort of space]], and forming a much [[nice category of spaces|nicer category of spaces]], see atz _[[compact Hausdorff space]]_), and use the word "[[quasicompact]]" to refer to just "compact" as we are using it here. This custom seems to be prevalent among [[algebraic geometry|algebraic geometers]], for example, and particularly so within Francophone schools.

> But it is far from clear to me ([[Todd Trimble]]) that "quasicompact" is very well-established outside such circles (despite some arguments in favor of it), and using simply "compact" for the nicer concept therefore carries some risk of creating misunderstanding among mathematicians at large. My own habit at any rate is to say "compact Hausdorff" for the nicer concept, and I will continue using this on the $n$Lab until consensus is reached (if that happens).

Another term in usage is 'compactum' to mean a [[compact Hausdorff space]] (even when 'compact' is not used to imply Hausdorffness).

=--

## Properties

+-- {: .num_prop }
###### Proposition

Assuming the [[axiom of choice]], the category of compact spaces admits all small [[limits]]. In any case, the category of compact locales admits all small limits. 

By the [[Tychonoff theorem]], every [[product topological space]] of compact spaces is itself again compact.

=--


+-- {: .num_prop }
###### Proposition

The direct [[image]] of a compact subspace under a [[continuous map]] is compact. A topological space becomes a [[bornological set]] by taking the bounded sets to be subsets contained in some compact subspace, and under this bornology, every continuous function is a bounded map.

If the spaces in question are $T_1$, then the sets with compact closure also constitute a bornology and continuous maps become bounded. In a non-Hausdorff situation these bornologies might differ because the closure of a compact set need not be compact.

=--


+-- {: .num_prop }
###### Proposition

A compact [[Hausdorff space]] must be [[normal space|normal]].  That is, the [[separation axioms]] $T_2$ through $T_4$ (when interpreted as an increasing sequence) are equivalent in the presence of compactness.

=--


+-- {: .num_prop }
###### Proposition

The [[Heine-Borel theorem]] asserts that a subspace $S \subset \mathbb{R}^n$ of a [[Cartesian space]] is compact precisely if it is [[closed subset|closed]] and [[bounded subset|bounded]].

=--

+-- {: .num_prop }
###### Proposition

We have:

1. [[compact subspaces of Hausdorff spaces are closed]].

1. [[closed subsets of compact spaces are compact]]

Hence:

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

=--

+-- {: .num_prop}
###### Proposition

[[sequentially compact metric spaces are equivalently compact metric spaces]]

[[countably compact metric spaces are equivalently compact metric spaces]]


=--

+-- {: .num_prop}
###### Proposition

[[continuous images of compact spaces are compact]]

=--

+-- {: .num_prop}
###### Proposition

[[maps from compact spaces to Hausdorff spaces are closed and proper]]

=--

+-- {: .num_prop }
###### Proposition

A [[discrete space]] is compact iff its underlying set is [[finite set|finite]].  In [[constructive mathematics]], a discrete space is compact iff its underlying set is [[Kuratowski-finite]].

=--


## Examples

### General

Every bounded [[closed interval]] $[a,b] \subset \mathbb{R}$ is compact.

By the [[Tychonoff theorem]], every [[product topological spaces]] of compact spaces is again compact. 

This implies the [[Heine-Borel theorem]], saying that every [[bounded subset|bounded]] and [[closed subset]] of a [[Euclidean space]] is compact.

### Compact spaces which are not sequentially compact
 {#CompactSpacesWhichAreNotSequentiallyCompact}

A famous example of a space that is compact, but not [[sequentially compact space|sequentially compact]] is the product space
$$
    \{0,1\}^{I} \coloneqq \{0, 1\}^{[0, 1]}
  \coloneqq \underset{[0,1]}{\prod} \{0,1\}
$$
with the [[product topology]]. 

This space is compact by the [[Tychonoff theorem]].

But it is not [[sequentially compact topological space|sequentially compact]]. We now discuss why. (We essentially follow [Steen-Seebach 70, item 105](#SteenSeebach70)).
 
Points of $\{0,1\}^{I}$ are functions $I \to \{0,1\}$, and the product topology is the topology of pointwise convergence.

Define a sequence $(a_n)$ in $I^{I}$ with $a_n(x)$ being the nth digit in the binary expansion of $x$ (we make the convention that binary expansions do not end in sequences of $1$s).  Let $a \coloneqq (a_{n_k})$ be a subsequence and define $p_a \in I$ by the binary expansion that has a $0$ in the $n_k$th position if $k$ is even and a $1$ if $k$ is odd (and, for definiteness and to ensure that this fits with our convention, define it to be $0$ elsewhere).  Then the projection of $(a_{n_k})$ at the $p_a$th coordinate is $1, 0, 1,0,...$ which is not convergent.  Hence $(a_{n_k})$ is not convergent.

(Basically that's the diagonal trick of [[Cantor's theorem]]).

However, as $\{0,1\}^I$ is compact, $a$ has a [[convergence|convergent]] [[subnet]].  An explicit construction of a convergent subset, given a [[cluster point]] $a$, is as follows.  A function $a \colon I \to \{0,1\}$ is a [[cluster point]] of $(a_n)$ if, for any $p_1, \dots, p_n \in I$ the set

$$
A(p_1,\dots,p_n) \coloneqq \{k \in \mathbb{R} : a_k(p_i) = a(p_i) \forall i\}
$$

is infinite.  We index our subnet by the family of finite subsets of $I$ and define the subnet function $\mathcal{F}(I) \to \mathbb{N}$ to be

$$
\{p_1,\dots,p_n\} \mapsto \min A(p_1,\dots,p_n)
$$

This is a convergent sub-[[net]].




## In synthetic topology

In [[synthetic topology]], where 'space' means simply 'set' (or [[type]], i.e. the basic objects of our foundational system), one natural notion of "compact space" is a [[covert set]], i.e. a set whose discrete topology is covert.  This includes the expected examples in various [[gros toposes]].


## Compact spaces and proper maps

A space $X$ is compact if and only if the unique map $X\to 1$ is [[proper map|proper]].  Thus, properness is a "relativized" version of compactness.

For topological spaces, this is either a definition of "proper map" (closed with compact fibers) or follows from the above characterization of compactness in terms of projections being closed maps (if proper maps are defined to be those that are universally closed).  For locales, it follows from the definition of proper map (a closed map such that $f_*$ preserves directed joins) and the fact that compact locales are automatically [[covert space|covert]] (see [[covert space]] for a proof).


## Related concepts

* [[Lebesgue number lemma]]

* [[sequentially compact topological space]]

* [[countably compact topological space]]

* [[paracompact topological space]], [[strongly compact topological space]]

* [[compactification]]

  * [[one-point compactification]]

  * [[Stone-Cech compactification]]

* [[compact-open topology]]

* [[closed manifold]]

* [[compact topos]]

* [[compactly supported cohomology]]

* [[complete algebraic variety]]


## References

Examples of compact spaces that are not sequentially compact are in

* {#SteenSeebach70} Lynn Steen, J. Arthur Seebach, _Counterexamples in Topology_, Springer-Verlag, New York (1970) 2nd edition,  (1978), Reprinted by Dover Publications, New York, 1995

On compact [[metric spaces]]:

* Roland Speicher, _Compact metric spaces_ ([pdf](http://www.mast.queensu.ca/~speicher/Chapter10.pdf))

* Alan Sokal, _Compactness of metric spaces_ ([pdf](http://www.ucl.ac.uk/~ucahad0/3103_handout_2.pdf))

For [[proper base change theorem]] e.g.

* {#Milne} [[James Milne]], section 17 of _[[Lectures on Étale Cohomology]]_
 


[[!redirects compact space]]
[[!redirects compact spaces]]
[[!redirects compact topological space]]
[[!redirects compact topological spaces]]
[[!redirects compact convergence space]]
[[!redirects compact convergence spaces]]
[[!redirects compact locale]]
[[!redirects compact locales]]

[[!redirects compact manifold]]
[[!redirects compact manifolds]]

[[!redirects compact subspace]]
[[!redirects compact subspaces]]
[[!redirects compact subset]]
[[!redirects compact subsets]]
[[!redirects compact set]]
[[!redirects compact sets]]

[[!redirects compact]]

[[!redirects compactness]]
