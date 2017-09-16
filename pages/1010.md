#Idea#

Problems of set theory arise by unjustified recursion of the naive notion of collection. If "Col"s are one notion of collections, then the notion "Col of all Cols" is in general problematic, since it is subject to the construction of Russel-style paradoxes. 

One way out is to consider a hierarchy of notions of collections: postulate that the collection of all "Col"s is not a "Col" itself, but is another notion of collection, a "Col+": the "Col+ of all Cols". Similarly, the collection of all "Col+"-type collections may be taken to be a "Col++", and so on.

One formalization of this idea is that of a _Grothendieck universe_: this is defined to be a set $U$ which behaves like a "set+ of all sets" in that all the standard operations of set theory (union, power set, etc.) can be performed on its elements. 




#Membership-based version#

Although developed for application to [[category theory]], the definition is usually given in a form that only makes sense in a membership-based [[set theory]], so we begin with that.

##Definition##

A **Grothendieck universe** $U$ is a [[pure set]] $U$ such that:
1. for all $u \in U$ and $t \in u$, $t \in U$ (so $U$ is _transitive_);
1. for all $u \in U$, the [[power set]] $P(u) \in U$;
1. the [[empty set]] $\empty \in U$;
1. for all $I \in U$ and functions $u: I \to U$, the [[union]] $\cup_{i: I} u_i \in U$.

Some authors leave out (3), which allows $\empty$ itself to be a Grothendieck universe.  Other authors use the set $\mathbb{N}$ of [[natural number]]s in place of $\empty$ in (3), which prevents $\mathbb{N}$ itself from being a Grothendieck universe.

##Consequences##

From the definition above, one can prove additional closure properties of a universe $U$, including the usual codings in pure set theory of [[function set]]s and [[cartesian product]]s and [[disjoint union]]s of sets, using these lemmata:

+--{.lemma}
If $t$ is a [[subset]] of $u$ and $u \in U$, then $t \in U$.
=--
+--{.proof}
By (2), $P(u) \in U$; $t \in P(u)$, so $t \in U$ by (1).
=--

+--{.lemma}
If $u, v \in U$, then $u \cup v \in U$.
=--
+--{.proof}
Since $\empty \in U$ by (3), so are $\star = P(\empty)$ and $TV = P(\star)$ by (2).  Even in [[constructive mathematics]], $2 = \{\bot, \top\}$ is a subset of $TV$, so $2 \in U$ in by Lemma 1.  Then $(\bot \mapsto u, \top \mapsto v)$ is a function $2 \to U$, so the union $u \cup v$ in $U$ by (4).
=--

Then using their usual encodings in set theory:
* the nullary cartesian product $\star$ is $P(\empty)$ as in the previous proof;
* the binary cartesian product $u \times v$ is a subset of $P(P(u \cup v))$;
* the general cartesian product $\prod_{i: I} u_i$ is a subset of $P(I \times \bigcup_{i: I} u_i)$;
* the the nullary disjoint union is $\empty$;
* the binary disjoint union $u \uplus v$ is a subset of $2 \times (u \cup v)$;
* the general disjoint union $\biguplus_{i: I} u_i$ is a subset of $I \times \bigcup_{i: I} u_i$;
* the set of functions $u \to v$ is a subset of $P(u \times v)$.


## Terminology: small/large ##


Given a universe $U$, an element of $U$ is called a **$U$-small set**, while a subset of $U$ is called **$U$-large**.  Technically, every $U$-small set is $U$-large (by requirement 1), but often one uses 'large' to mean 'large but not small'.  However, note that there are many sets (such as the power set of $U$) that are still *too* large to be 'large'.

As such, these concepts are [[evil]], since two sets may be [[isomorphism|isomorphic]] yet have different properties with respect to $U$.  However, a set which is isomorphic to a $U$-small or $U$-large set is called **essentially** $U$-small or $U$-large; these concepts are non-evil.

## Axiom of universes ##

When working with Grothendieck universes one usually adds the following **axiom of universes** to the usual axioms of set theory:

* For every set $s$ there exists a universe which contains $s$, i.e. such that $s \in U$.

This way whenever any operation leads one outside of a given Grothendieck universe (see applications below), there is guaraneteed to be a bigger Grothendieck universe in which one lands.  In other words, every set is small if your universe is large enough!

#Structural version#

An equivalent concept (at least for the purposes of category theory) can also be defined in structural set theories (like [[ETCS]]).

The important point is the [[cardinal number|cardinality]] $|U|$ of the Grothendieck universe $U$; it must be a _strongly inaccessible cardinal_.  In the arithmetic of cardinal numbers, this means that $0 \lt |U|$ and $\sum_{i: I} \kappa_i \lt |U|$ whenever $|I| \lt |U|$ and $\kappa_i \lt |U|$ for each $i: I$ (to be inaccessible) and $2^\kappa \lt |U|$ whenever $\kappa \lt |U|$ (to be strongly so).  Traditionally one also requires an inaccessible cardinal to be uncountable, but this is just to rule out $\mathbb{N}$ again.

We still need to formalise the idea that a set might 'belong' to $U$.  We can do this by equipping $U$ with a family $(S_u)_{u: U}$ of sets indexed by $U$; if you like, you can formalise this as a [[bundle]] over $U$.

##Definition##

A **Grothendieck universe** is a family $(S_u)_{u: U}$ of sets such that:
1. for all $u$ in $U$, if $X$ is a [[subset]] of $S_u$ (in the sense that there exists an [[injection]] $X \embedsin S_u$), then there is a $v$ in $U$ such that $X \cong S_v$;
1. for all $u$, there is a $v$ such that the [[power set]] $P(S_u) \cong S_v$;
1. there is a $v$ such that $S_v$ is [[empty set|empty]];
1. for all $u$ and functions $f: S_u \to U$, there is a $v$ such that the [[disjoint union]] $\biguplus_{i: S_u} S_{f(i)} \cong S_v$.

If you want to allow $\empty$, then remove axiom (3) again; if you want to rule out $\mathbb{N}$, then replace it with the requirement that some set in the family is isomorphic to $\mathbb{N}$.


## Terminology: small/large ##


Given a universe $U$, an set $X$ is called **$U$-small** if $X \cong S_u$ for some $u$ in $U$; $X$ is called **$U$-large** if $X$ is a subset of $U$.  As before, every $U$-small set is technically $U$-large, but often one uses 'large' to mean 'large but not small'.  However, note that there are many sets (such as the power set of $U$) that are still *too* large to be 'large'.  These concepts are already non-[[evil]], so there is no need for versions with 'essentially'.


## Axiom of universes ##

When working with Grothendieck universes one usually adds the following **axiom of universes** to the usual axioms of set theory:

* For every set $X$ there exists a universe which contains $X$, i.e. such that $X \cong S_u$ for some $u$ in $U$.

This way whenever any operation leads one outside of a given Grothendieck universe (see applications below), there is guaranteed to be a bigger Grothendieck universe in which one lands.  In other words, every set is small if your universe is large enough!

+-- {: .query}
[[Urs Schreiber|Urs]]: unless I am missing something, the Grothendieck universe approach goes right against Lawvere's attitude to set theory as reviewed and emphasized at [[Trimble on ETCS I]]: that it is unnatural to consider membership of sets as a global relation, i.e. to handle sets and their elements on the same footing. On the contrary, for the above definition to even make sense, we have to assume that "everything is a set" (becuase the above definition tacitly assume that every element of a Grothendieck universe is itself a set). 

So what is the analog of Grothendieck universes, or of what they accomplish in practice, in [[ETCS]]? How are the applications mentioned below handled in [[ETCS]] without use of Grothendieck universes?

[[Todd Trimble|Todd]]: Urs asked me to comment here, although I don't consider myself all that qualified. I know Mike Shulman has thought at length about all these issues. 

But a nice way of thinking of Grothendieck universes is as an internal topos object. That is, it is possible to express the notion of 'topos object' in any category with finite limits, and then one can define a Grothendieck universe within say a topos or pretopos of sets $E$ as such an internal topos object $U$ inside $E$. Mike?

_Toby_:  The important point is the bit about cardinal numbers as I have written above.  The rest of the structural formulation *seems* right to me, but I wouldn\'t be surprised if I messed it up.  There is probably an elegant way to say this using [[indexed category|indexed categories]] anyway.  But the infinite strongly inacessible cardinal is the bottom line.
=--


# Examples #

The set $\mathbb{N}$ of [[natural number]]s is a Grothendieck universe, unless you phrase axiom (3) in the definition to specifically rule it out.  In this way, the axiom of infinity can be seen as a simply universe axiom (stating that at least one universe exists).

If you refrain from using the axiom of universes (except perhaps once, to get $\mathbb{N}$ as above), then the set of all sets (or cardinal numbers) that you can actually construct is a Grothendieck universe.  Of course, you cannot possibly have proved that this universe exists, but the intuition that you ought be able to form the collection of 'everything that we\'ve used so far' is the justification for the axiom of universes.

Similarly, if you use the axiom of universes at most $n$ times, then the set of all sets that you can construct with this restriction is a Grothendieck universe.  So is, in principle, the set of all sets that you can construct using any number of applications of the axiom of universes, but the existence of *this* set cannot be proved, even using this axiom!  (So the axiom of universes is not the final word on large cardinal axioms.)

#Applications#

Let $U Set$ be the [[category]] of $U$-small sets, a [[full subcategory]] of [[Set]].

A category whose set of morphisms is $U$-small may be called a $U$-[[small category]]; it can also be thought of as an [[internal category]] in $U Set$.

A category whose [[hom-set]]s are all $U$-small may be called [[locally small category|locally]] $U$-small; it can also be thought of as an [[enriched category]] over $U Set$.  Every $U$-small category is locally $U$-small.

A category whose set of morphisms is $U$-large may be called a $U$-[[large category]]; normally, this term is used only when the category is not also $U$-small.  Typically, $U$-large categories are locally $U$-small and vice versa, but exceptions are possible.

Note that $U Set$ itself is $U$-large and locally $U$-small.

##Presheaf categories##

Let $C$ be a $U$-small category.  Then the category of $U$-[[presheaf|presheaves]] on $C$ (the [[functor category]] $[C^{op}, U Set]$) is also $U$-large and locally $U$-small but not $U$-small unless $C$ is empty.  ($U Set$ itself is the special case of this where $C$ is the [[point]].)

Now let $C$ be a $U$-large category (and not small).  Then the category of $U$-presheaves on $C$ is not even locally $U$-small, nor is it even $U$-large (it is 'too large to be large').  However, it is locally $U$-large.  Also, it is quite possible, if $C$ is a $U$-[[large site]], that the category of $U$-[[sheaf|sheaves]] on $C$ is $U$-large and locally $U$-small.

These arguments go as follows:

### $U PSh(C)$ is $U$-large ###


An upper bound for the size of $[C^{op}, U Set]$, hence of the set $Obj([C^{op},U Set])$ is the size of $\{ F : Obj(C)\times Mor(C) \to U Set\}$ where both $Obj(C)$ and $Mor(C)$ are in $U Set$. 
So we are looking at the cardinal number $|U|^{|u| \times |v|}$ where $u = Obj(C)$ and $v = Mor(C)$.  Use the fact that any Grothendieck universe must be infinite (since it has $\emptyset$, $P(\emptyset)$, etc) and the result follows from cardinal arithmetic that $\kappa^\lambda = \kappa$ when $\lambda \lt \kappa$ and $\kappa$ is infinite.

### $U PSh(C)$ is locally $U$-small ###

An upper bound for the size of the set of morphisms between two functors $F,G : C^{op} \to U Set$ is the disjoint union indexed by the objects $c$ of $C$ over the $U$-sets $G(c)^{F(c)}$. Now $G(c)^{F(c)} \in U$ since it is a function set and $\cup_{c \in Obj(C)} G(c)^{F(c)}$ by the assumption that unions stay in $U$. 




+-- {: .query}

[[Zoran Skoda]] But starting with a $U$-small category one can look at the category of $U$-small presheaves instead of all presheaves.
This has been useful in hmotopy theory, there is for example
a paper by Chorny and Dwyer using it. Look also at the paper by Day and Lack on limits of small functors.
[www.maths.usyd.edu.au/u/stevel/papers/small.pdf](www.maths.usyd.edu.au/u/stevel/papers/small.pdf) 
 I once listened a talk by Chorny in Barcelona where he was convincing that in practice we should use small Yoneda lemma rather than the usual Yoneda, he had arguments that a number of things are more natural, but I have not being taking notes and he never wrote those things in a paper as far as I know (I do not see them in his other papers in which he uses small presheaves but without some of that discussion).
See anyway
[http://wwwmaths.anu.edu.au/~chorny/personal/research/](http://wwwmaths.anu.edu.au/~chorny/personal/research/)
and also earlier minipreprint version
[http://www.math.uwo.ca/~bchorny2/research/smalldiag.ps](http://www.math.uwo.ca/~bchorny2/research/smalldiag.ps)
the results of Chorny-Dwyer is cited  (I did not look yet how much used yet) by Rosicky in Accessible categories and homotopy theory
[www.math.yorku.ca/~tholen/HB07Rosicky.pdf](www.math.yorku.ca/~tholen/HB07Rosicky.pdf)

[[Urs Schreiber|Urs]]: above we are talking about "$U$-presheaves", i.e. the functor categories $[C^{op}, U Set]$. Isn't that the same as "$U$-small presheaves"?

=--