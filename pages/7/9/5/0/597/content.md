
# $\kappa$-ary regular and exact categories
* table of contents
{: toc}

## Idea

The notions of [[regular category]], [[exact category]], [[coherent category]], [[extensive category]], [[pretopos]], and [[Grothendieck topos]] can be nicely unified in a theory of "familial regularity and exactness."  This was apparently first noticed by [[Ross Street]], and expanded by [[Mike Shulman]] with a generalized theory of [[exact completion]].


## Sinks and relations

Let $C$ be a [[finitely complete category]].  By a [[sink]] in $C$ we mean a family $\{f_i\colon A_i \to B\}_{i\in I}$ of [[morphism]]s with common [[target]].  A sink $\{f_i\colon A_i \to B\}$ is **[[extremal epimorphism|extremal epic]]** if it doesn't factor through any proper [[subobject]] of $B$.  The _[[pullback]]_ of a sink along a morphism $B' \to B$ is defined in the evident way.

By a (many-object) **[[relation]]** in $C$ we will mean a family of objects $\{A_i\}_{i\in I}$ together with, for every $i,j\in I$, a monic span $A_i \leftarrow R_{i j} \to A_j$ (that is, a [[subobject]] $R_{i j}$ of $A_i \times A_j$.  We say such a relation is:

* [[reflexive relation|reflexive]] if $R_{i i}$ contains the diagonal $A_i \to A_i \times A_i$, for all $i$,
* [[transitive relation|transitive]] if the pullback $R_{i j} \times_{A_j} R_{j k}$ factors through $R_{i k}$, for all $i,j,k$,
* [[symmetric relation|symmetric]] if $R_{i j}$ contains, hence is equal to, the transpose of $R_{j i}$ for all $i,j$, and
* a [[congruence]] if it is reflexive, transitive, and symmetric; this is an internal notion of (many-object) [[equivalence relation]].

Abstractly, reflexive and transitive relations can be identified with categories [[enriched category|enriched]] in a suitable [[bicategory]]; see (Street 1984).  Congruences can be identified with enriched $\dagger$-[[dagger-categories|categories]].

A __quotient__ for a relation is a [[colimit]] for the diagram consisting of all the $A_i$ and all the spans $A_i \leftarrow R_{i j} \to A_j$.  And the __kernel__ of a sink $\{f_i\colon A_i\to B\}$ is the relation on $\{A_i\}$ with $R_{i j} = A_i \times_B A_j$.  It is evidently a congruence.

Finally, a sink is called **[[effective epimorphism|effective-epic]]** if it is the quotient of its kernel.  It is called **universally effective-epic** if any pullback of it is effective-epic.


### Examples

* If ${|I|} = 1$, a congruence is the same as the ordinary internal notion of [[congruence]].  In this case [[quotient object|quotients]] and [[kernel pair|kernels]] reduce to the usual notions.

* If ${|I|} = 0$, a congruence contains no data and a sink is just an object in $C$.  The empty congruence is, trivially, the kernel of the empty sink with any target $B$, and a quotient for the empty congruence is an [[initial object]].

* Given a family of objects $\{A_i\}$, define a congruence by $R_{i i}=A_i$ and $R_{i j}=0$ (an initial object) if $i \neq j$.  Call a congruence of this sort _trivial_ (empty congruences are always trivial).  Then a quotient for a trivial congruence is a [[coproduct]] of the objects $A_i$, and the kernel of a sink $\{f_i\colon A_i\to B\}$ is trivial iff the $f_i$ are disjoint monomorphisms.


## $\kappa$-ary regularity and exactness

Let $\kappa$ be an [[arity class]].  We call a sink or relation **$\kappa$-ary** if the cardinality ${|I|}$ is $\kappa$-small.  As usual for arity classes, the cases of most interest have special names:

* When $\kappa = \{1\}$ we say **unary**.
* When $\kappa = \omega$ is the set of finite cardinals, we say **finitary**.
* When $\kappa$ is the class of all cardinal numbers, we say **infinitary**.

+-- {: .num_theorem #KRegular}
###### Theorem
For a category $C$, the following are equivalent:

1. $C$ has finite limits, every $\kappa$-ary sink in $C$ factors as an extremal epic sink followed by a monomorphism, and the pullback of any extremal epic $\kappa$-ary sink is extremal epic.

1. $C$ has finite limits, and the kernel of any $\kappa$-ary sink in $C$ is also the kernel of some universally effective-epic sink.

1. $C$ is a [[regular category]] and has pullback-stable [[joins]] of $\kappa$-small families of [[subobjects]].
=--

When these conditions hold, we say $C$ is **$\kappa$-ary regular**, or alternatively **$\kappa$-ary coherent**.  There are also some other more technical characterizations; see [Shulman](#Shulman).

+-- {: .num_theorem #KExact}
###### Theorem
For a category $C$, the following are equivalent:

1. $C$ has finite limits, and every $\kappa$-ary congruence is the kernel of some universally effective-epic sink.

1. $C$ is $\kappa$-ary regular, and every $\kappa$-ary congruence is the kernel of some sink.

1. $C$ is both [[exact category|exact]] and $\kappa$-ary [[extensive category|extensive]].
=--

When these conditions hold, we say that $C$ is **$\kappa$-ary exact**, or alternatively a **$\kappa$-ary pretopos**.

## Examples

1. $C$ is [[regular category|regular]] iff it is unary regular.
2. $C$ is [[coherent category|coherent]] iff it is finitary regular.
3. $C$ is [[coherent category|infinitary-coherent]] iff it is [[well-powered category|well-powered]] and infinitary regular.
4. $C$ is [[exact category|exact]] iff it is unary exact.
5. $C$ is a [[pretopos]] iff it is finitary exact.
6. $C$ is an [[pretopos|infinitary pretopos]] iff it is [[well-powered category|well-powered]] and infinitary exact.

Some other sorts of [[exactness properties]] (especially [[lex-colimits]]) can also be characterized in terms of congruences, kernels, and quotients.  For instance:

7. $C$ is $\kappa$-ary [[extensive category|lextensive]] iff every $\kappa$-ary _trivial_ congruence has a pullback-stable quotient of which it is the kernel.

In [Street](#Street), there is also a version of regularity and exactness that applies even to some _large_ sinks and congruences, and implies some small-generation properties of the category as well.


## Properties

In a $\kappa$-ary regular category,

* Every extremal-epic $\kappa$-ary sink is the quotient of its kernel.
* Any $\kappa$-ary congruence that is a kernel has a quotient.

Thus, in a $\kappa$-ary exact category,

* Every $\kappa$-ary congruence has a quotient.

In a $\kappa$-ary regular category, the class of all $\kappa$-small and effective-epic families generates a [[topology]], called its $\kappa$-canonical topology.  This topology makes it a [[∞-ary site]].


## The 2-category of $\kappa$-ary exact categories

A functor $F:C\to D$ between $\kappa$-ary exact categories is called **$\kappa$-ary exact** if it preserves finite limits and $\kappa$-small effective-epic (or equivalently extremal-epic) families.

The resulting 2-category $EX_\kappa$ is a full [[reflective subcategory|reflective]] sub-2-category of the 2-category $SITE_\kappa$ of [[∞-ary sites]].  The reflector is called [[exact completion]].


## References

*  [[Ross Street]], "The family approach to total cocompleteness and toposes."  Transactions of the AMS 284 no. 1, 1984
{#Street}

* [[Michael Shulman]], "Exact completions and small sheaves".  *Theory and Applications of Categories*, Vol. 27, 2012, No. 7, pp 97-173.  [Free online](http://www.tac.mta.ca/tac/volumes/27/7/27-07abs.html)
{#Shulman}

[[!redirects familial regularity and exactness]]
[[!redirects familial regularity]]
[[!redirects familial exactness]]
[[!redirects familially exact category]]
[[!redirects familially regular category]]
[[!redirects ∞-ary exact category]]
[[!redirects ∞-ary exact categories]]
[[!redirects k-ary exact category]]
[[!redirects k-ary exact categories]]
[[!redirects ∞-ary exactness]]
[[!redirects k-ary exactness]]
[[!redirects ∞-ary regular category]]
[[!redirects ∞-ary regular categories]]
[[!redirects k-ary regular category]]
[[!redirects k-ary regular categories]]
[[!redirects ∞-ary regularity]]
[[!redirects k-ary regularity]]
[[!redirects ∞-ary pretopos]]
[[!redirects ∞-ary pretoposes]]
[[!redirects ∞-ary pretopoi]]
[[!redirects k-ary pretopos]]
[[!redirects k-ary pretoposes]]
[[!redirects k-ary pretopoi]]
[[!redirects ∞-ary coherent category]]
[[!redirects ∞-ary coherent categories]]
[[!redirects k-ary coherent category]]
[[!redirects k-ary coherent categories]]
