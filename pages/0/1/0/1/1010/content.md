#Idea#

Problems of set theory arise by unjustified recursion of the naive notion of collection. If "Col"s are one notion of collections, then the notion "Col of all Cols" is in general problematic, since it is subject to the construction of Russel-style paradoxes. 

One way out is to consider a hierarchy of notions of collections: postulate that the collection of all "Col"s is not a "Col" itself, but is another notion of collection, a "Col+": the "Col+ of all Cols". Similarly, the collection of all "Col+"-type collections may be taken to be a "Col++", and so on.

One formalization of this idea is that of a _Grothendieck universe_: this is defined to be a set $U$ which behaves like a "set+ of all sets" in that all the standard operations of set theory (union, intersection, etc.) can be performed on its elements. 




#Definitions#

##Membership-based##

Although developed for application to category theory, the definition is usually given in a form that only makes sense in a membership-based [[set theory]], so we begin with that.

A **Grothendieck universe** $U$ is a [[pure set]] $U$ such that:
1. $(t \in u \in U) \Rightarrow (t \in U)$;
1. $(u \in U) \Rightarrow (\{u\} \in U)$;
1. $(u \in U) \Rightarrow (P(u) \in U)$, where $P(u)$ is the [[power set]] of the set $u$;
1. for all $I \in U$ and functions $f: I \to U$, the union $\cup_{i: I} f_i \in U$.

From these, one can prove additional closure properties of $U$, including the usual codings in pure set theory of [[function set]]s and the [[cartesian product]] and [[disjoint union]] of sets.

+-- {: .query}

 [[Urs Schreiber|Urs]]: actually, could you indicate how 
the statement about function sets follows? (I understand that the power set $P(u)$ is the function set $2^u$.)

_Toby_:  The set of functions from $A$ to $B$ can be encoded as a subset of the power set of $A \times B$ (as can also be done in topos theory).  You can encode $A \times B$ (see [[cartesian product]] and look at the binary special case for the usual method) as a subset of $P(P(A \cup B))$.  As long as $\emptyset \in U$ (which I think should be required, but not $\mathbb{N}$), you get $2$ as $P(P(\emptyset))$ (or, constructively, as a subset of that), so you can form the $2$-indexed union $A \cup B$ and hence $P(P(A \cup B))$.  So all that is needed is to show that if $t \subseteq u \in U$, then $t \in U$; this follows from the first axiom since $t \in P(u)$.

=--



Some authors (for instance [[Categories and Sheaves|Kashiwara-Shapira]]) add
* $\emptyset \in U$ (it\'s enough to say that there exists some $u \in U$);
* $\mathbb{N} \in U$ (it\'s enough to say that some [[infinite set]] belongs to $U$).

Certainly the examples that we\'re interested in have these properties, but often it\'s nice to leave them out, so that $\emptyset$ and $\mathbb{N}$ themselves become examples of Grothendieck universes.  ($\emptyset$ is arguable, but seeing $\mathbb{N}$ as a universe shows how the axiom of infinity is but the first in a series of large-cardinal axioms.)


Given a universe $U$, an element of $U$ is called a **$U$-small set**, while a subset of $U$ is called **$U$-large**.  Technically, every $U$-small set is $U$-large (by requirement 1), but often one uses 'large' to mean 'large but not small'.  However, note that there are many sets (such as the power set of $U$) that are still *too* large to be 'large'.

When working with Grothendieck universes one usually adds the following **axiom of universes** to the usual axioms of set theory:

* For every set $s$ there exists a universe which contains $s$, i.e. such that $s \in U$.

This way whenever any operation leads one outside of a given Grothendieck universe (see applications below), there is guaraneteed to be a bigger Grothendieck universe in which one lands.  In other words, every set is small if your universe is large enough!

##Structural##

An equivalent (at least for our purposes) concept can also be defined in structural set theories (like [[ETCS]]).  The important point is the [[cardinal number|cardinality]] $|U|$ of the Grothendieck universe $U$; it must be a _strongly inaccessible cardinal_.  In the arithmetic of cardinal numbers, this means that $\sum_{i: I} \kappa_i \lt |U|$ whenever $|I| \lt |U|$ and $\kappa_i \lt |U|$ for each $i: I$.  (Traditionally one also requires an inaccessible cardinal to be uncountable, but this is just to rule out $\mathbb{N}$ again.)  Turned back into the language of sets, this says that a [[disjoint union]] of $U$-small sets indexed by a $U$-small set must be $U$-small.  From this perspective, the last axiom (which uses a set-theoretic [[union]] instead of a disjoint union, but that\'s not significant) is the important one; the rest is bookkeeping.

We still need to formalise the idea that a set might 'belong' to $U$.  We can do this by equipping $U$ with a family $(S_u)_{u: U}$ of sets indexed by $U$; if you like, you can formalise this as a [[bundle]] over $U$.  Then we can define a **Grothendieck universe** in terms of this family of sets as follows:
1. for all $u$ in $U$, if $X$ is a [[subset]] of $S_u$ (in the sense that there exists an [[injection]] $X \embedsin S_u$), then there is a $v$ in $U$ such that $X \cong S_v$;
1. for all $u$, there is a $v$ such that $S_v$ is a singleton;
1. for all $u$, there is a $v$ such that $P(S_u) \cong S_v$, where $P(S)$ is the [[power set]] of the set $S$;
1. for all $u$ and functions $f: S_u \to U$, there is a $v: U$ such that the disjoint union $\biguplus_{i: S_u} S_{f(i)} \cong S_v$.

The optional clauses in the definition become:
* For some $u$, $S_u$ is empty (it\'s enough to say that $U$ is [[inhabited set|inhabited]], or to rephrase (2) to remove the hypothesis that $u$ exists);
* For some $u$, $S_u \cong \mathbb{N}$ (it\'s enough to say that some $S_u$ is Dedekind-infinite).

A set $X$ is **$U$-small** is $X \cong S_u$ for some $u$; $X$ is **$U$-large** if $X$ is a subset of $U$.

Finally, the **axiom of universes** becomes:

* For every set $X$, there exists a universe $U$ such that $X$ is $U$-small.

+-- {: .query}
[[Urs Schreiber|Urs]]: unless I am missing something, the Grothendieck universe approach goes right against Lawvere's attitude to set theory as reviewed and emphasized at [[Trimble on ETCS I]]: that it is unnatural to consider membership of sets as a global relation, i.e. to handle sets and their elements on the same footing. On the contrary, for the above definition to even make sense, we have to assume that "everything is a set" (becuase the above definition tacitly assume that every element of a Grothendieck universe is itself a set). 

So what is the analog of Grothendieck universes, or of what they accomplish in practice, in [[ETCS]]? How are the applications mentioned below handled in [[ETCS]] without use of Grothendieck universes?

[[Todd Trimble|Todd]]: Urs asked me to comment here, although I don't consider myself all that qualified. I know Mike Shulman has thought at length about all these issues. 

But a nice way of thinking of Grothendieck universes is as an internal topos object. That is, it is possible to express the notion of 'topos object' in any category with finite limits, and then one can define a Grothendieck universe within say a topos or pretopos of sets $E$ as such an internal topos object $U$ inside $E$. Mike?

_Toby_:  The important point is the bit about cardinal numbers as I have written above.  The rest of the structural formulation *seems* right to me, but I wouldn\'t be surprised if I messed it up.  There is probably an elegant way to say this using [[indexed category|indexed categories]] anyway.  But the strongly inacessible cardinal is the bottom line.
=--


#Applications#

Let $U Set$ be the [[category]] of $U$-small sets, a [[full subcategory]] of [[Set]].

A category whose set of morphisms is $U$-small may be called a $U$-[[small category]]; it can also be thought of as an [[internal category]] in $U Set$.

A category whose [[hom-set]]s are all $U$-small may be called [[locally small category|locally]] $U$-small; it can also be thought of as an [[enriched category]] over $U Set$.  Every $U$-small category is locally $U$-small.

A category whose set of morphisms is $U$-large may be called a $U$-[[large category]]; normally, this term is used only when the category is not also $U$-small.  Typically, $U$-large categories are locally $U$-small and vice versa, but exceptions are possible.

Note that $U Set$ itself is $U$-large and locally $U$-small.

##Presheaf categories##

Let $C$ be a $U$-small category.  Then the category of $U$-[[presheaf|presheaves]] on $C$ (the [[functor category]] $[C^{op}, U Set]$) is also $U$-large... 


+-- {: .query}

[[Urs Schreiber|Urs]]: Let me see if I follow this in detail: an upper bound for the size of $Obj([C^{op},U Set])$ is the size of $\{ F : Obj(C)\times Mor(C) \to U Set\}$ where both $Obj(C)$ and $Mor(C)$ are in $U Set$. How do I see that this is $U$-large?

_Toby_:  We\'re looking at the cardinal number $|U|^{|u| \times |v|}$ where $u = Obj(C)$ and $v = Mor(C)$.  Use the fact that any Grothendieck universe must be infinite (since it has $\emptyset$, $P(\emptyset)$, etc) and you have the result from cardinal arithmetic that $\kappa^\lambda = \kappa$ when $\lambda \lt \kappa$ and $\kappa$ is infinite.

=--

...and locally $U$-small...

+-- {: .query}

[[Urs Schreiber|Urs]]: okay, I see this: an upper bound for the size of the set of morphisms between two functors $F,G : C^{op} \to U Set$ is the disjoint union indexed by the objects $c$ of $C$ over the $U$-sets $G(c)^{F(c)}$. Now $G(c)^{F(c)} \in U$ since it is a function set and $\cup_{c \in Obj(C)} G(c)^{F(c)}$ by the assumption that unions stay in $U$. 

=--



...but not $U$-small unless $C$ is empty.  ($U Set$ itself is the special case of this where $C$ is the [[point]].)

Now let $C$ be a $U$-large category (and not small).  Then the category of $U$-presheaves on $C$ is not even locally $U$-small, nor is it even $U$-large (it is 'too large to be large').  However, it is locally $U$-large.  Also, it is quite possible, if $C$ is a $U$-[[large site]], that the category of $U$-[[sheaf|sheaves]] on $C$ is $U$-large and locally $U$-small.

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