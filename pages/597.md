The notions of [[regular category]], [[exact category]], [[coherent category]], [[extensive category]], and [[pretopos]] can be nicely unified in a theory of "familial regularity and exactness."  This was apparently first noticed by Street.

# Sinks and relations #

Let $C$ be a [[finitely complete category]].  By a **sink** in $C$ we mean a family $\{f_i:A_i\to B\}_{i\in I}$ of [[morphism]]s with common [[target]].  A sink $\{f_i:A_i\to B\}$ is **strong epic** if it doesn't factor through any proper [[subobject]] of $B$.  The _pullback_ of a sink along a morphism $B'\to B$ is defined in the evident way.

By a (many-object) **[[relation]]** in $C$ we will mean a family of objects $\{A_i\}_{i\in I}$ together with, for every $i,j\in I$, a monic span $A_i \leftarrow R_{i j} \to A_j$  (that is, a [[subobject]] $R_{i j}$ of $A_i\times A_j$.  We say such a relation is:

* [[reflexive relation|reflexive]] if $R_{i i}$ contains the diagonal $A_i\to A_i\times A_i$, for all $i$,
* [[transitive relation|transitive]] if the pullback $R_{i j} \times_{A_j} R_{j k}$ factors through $R_{i k}$, for all $i,j,k$,
* [[symmetric relation|symmetric]] if $R_{i j}$ contains, hence is equal to, the transpose of $R_{j i}$ for all $i,j$, and
* a [[congruence]] if it is reflexive, transitive, and symmetric; this is an internal notion of [[equivalence relation]].

Abstractly, reflexive and transitive relations can be identified with categories [[enriched category|enriched]] in a suitable [[bicategory]]; see (Street 1984).

+--{.query}
Presumably, congruences can be identified with [[groupoid]]s enriched in this bicategory?

Mike: One could say that; it's certainly at least morally true.  But I don't know a definition of "enriched groupoid" that works in generality greater than, say, enrichment over a [[cartesian monoidal category]].  The bicategory in question is locally posetal and equipped with an "involution" which allows you to define "symmetric" enriched categories, and this level of generality can also be used to construct [[sheaf|sheaves]] and recover ordinary [[metric space|metric spaces]] from Lawvere's asymmetric ones.   But I'm iffy about using the word "groupoid" because I don't know an abstract formalism that includes this situation and also includes ordinary groupoids.
=--

A _quotient_ for a relation is a [[colimit]] for the diagram consisting of all the $A_i$ and all the spans $A_i \leftarrow R_{ij} \to A_j$.  And the _kernel_ of a sink $\{f_i:A_i\to B\}$ is the relation on $\{A_i\}$ with $R_{i j} = A_i\times_B A_j$.  It is evidently a congruence.

For example:

* If $|I|=1$, a congruence is the same as the ordinary internal notion of [[congruence]].  In this case [[quotient object|quotient]]s and [[kernel pair|kernels]] reduce to the usual notions.

* If $|I|=0$, a congruence or sink contains no data.  The empty congruence is, trivially, the kernel of the empty sink, and a quotient for the empty congruence is an [[initial object]].

* Given a family of objects $\{A_i\}$, define a congruence by $R_{i i}=A_i$ and $R_{i j}=0$ (an initial object) if $i\neq j$.  Call a congruence of this sort _trivial_ (empty congruences are always trivial).  Then a quotient for a trivial congruence is a [[coproduct]] of the objects $A_i$, and the kernel of a sink $\{f_i:A_i\to B\}$ is trivial iff the $f_i$ are disjoint monomorphisms.


# Familial regularity and exactness #

In what follows we will use **unary** to refer to sinks and relations with $|I|=1$, **finitary** to refer to sinks and relations with $|I|$ finite, and **infinitary** to refer to all small sinks and relations.  We say **$\kappa$-ary** to refer to an unspecified one of these three cases (of course, there are generalizations to other cardinals).

We say that a finitely complete category $C$ is **$\kappa$-ary regular** if the following hold.

* Every $\kappa$-ary sink factors as a strong epic sink followed by a monomorphism.
* The pullback of any strong epic $\kappa$-ary sink is strong epic.

We say that $C$ is **$\kappa$-ary exact** if it is $\kappa$-ary regular and in addition

* every $\kappa$-ary congruence is the kernel of some sink.

One can show (Street 1984) that in a $\kappa$-ary regular category, every strong epic $\kappa$-ary sink is the quotient of its kernel, and that any $\kappa$-ary congruence that is a kernel has a quotient.  Thus, in a $\kappa$-ary exact category, every $\kappa$-ary congruence has a quotient.  In fact, one can alternately define a $\kappa$-ary regular category to be one in which every $\kappa$-ary congruence which is a kernel has a pullback-stable quotient.

It is then not difficult to verify that

1. $C$ is [[regular category|regular]] iff it is unary regular.
1. $C$ is [[coherent category|coherent]] iff it is finitary regular.
1. $C$ is [[coherent category|infinitary-coherent]] iff it is [[well-powered category|well-powered]] and infinitary regular.
1. $C$ is [[exact category|exact]] iff it is unary exact.
1. $C$ is a [[pretopos]] iff it is finitary exact.
1. $C$ is an [[pretopos|infinitary pretopos]] iff it is [[well-powered category|well-powered]] and infinitary exact.
1. $C$ is [[extensive category|lextensive]] iff every finitary _trivial_ congruence has a pullback-stable quotient of which it is the kernel.
1. $C$ is [[extensive category|infinitary-lextensive]] iff every (small) trivial congruence has a pullback-stable quotient of which it is the kernel.

Actually, Street's paper referenced below gives a version of regularity and exactness that applies even to some _large_ sinks and congruences.


# References #

Street, "The family approach to total cocompleteness and toposes."  Transactions of the AMS 284 no. 1, 1984
