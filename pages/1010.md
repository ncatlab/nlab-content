#Idea#

Problems of set theory arise by unjustified recursion of the naive notion of collection. If "Col"s are one notion of collections, then the notion "Col of all Cols" is in general problematic, since it is subject to the construction of Russel-style paradoxes. 

One way out is to consider a hierarchy of notions of collections: postulate that the collection of all "Col"s is not a "Col" itself, but is another notion of collection, a "Col+": the "Col+ of all Cols". Similarly, the collection of all "Col+"-type collections may be taken to be a "Col++", and so on.

One formalization of this idea is that of a _Grothendieck universe_: this is defined to be a set $U$ which behaves like a "set+ of all sets" in that all the standard operations of set theory (union, intersection, etc.) can be performed on its elements. 




#Definitions#

##Membership-based

Although developed for application to category theory, the definition is usually given in a form that only makes sense in a membership-based [[set theory]], so we begin with that.

A **Grothendieck universe** $U$ is a [[pure set]] $U$ such that:
1. $(t \in u \in U) \Rightarrow (t \in U)$;
1. $(u, v  \in U) \Rightarrow (\{u, v\} \in U)$;
1. $(u \in U) \Rightarrow (P(u) \in U)$, where $P(u)$ is the [[power set]] of the set $u$;
1. for all $I \in U$ and functions $f : I \to U$, the union $\cup_{i \in I} f_i \in U$.

From these, one can prove additional closure properties of $U$, including the usual codings in pure set theory of [[function set]]s and the [[cartesian product]] and [[disjoint union]] of sets.

Some authors (for instance [[Categories and Sheaves|Kashiwara-Shapira]]) add

* $\emptyset \in U$;
* $\mathbb{N} \in U$.

Certainly the examples that we\'re interested in have these properties, but often it\'s nice to leave them out, so that $\emptyset$ and $\mathbb{N}$ themselves become examples of Grothendieck universes.  ($\emptyset$ is arguable, but seeing $\mathbb{N}$ as a universe shows how the axiom of infinity is but the first in a series of large-cardinal axioms.)

+-- {: .query}
[[Urs Schreiber|Urs]]: ??

_Toby_: Have I handled these question marks, Urs?

 
_Urs_: Yes, thanks a lot. Also for your other modifications. Very helpful. Maybe one more question: Kashiwara-Shapira demand just $(u \in U) \Rightarrow (\{u \} \in U)$. The above however is taken from Wikipedia, 
$(u, v  \in U) \Rightarrow (\{u, v\} \in U)$. What's the point of that, given 4?
=--

Given a universe $U$, an element of $U$ is called a **$U$-small set**, while a subset of $U$ is called **$U$-large**.  Technically, every $U$-small set is $U$-large (by requirement 1), but often one uses 'large' to mean 'large but not small'.  However, note that there are many sets (such as the power set of $U$) that are still *too* large to be 'large'.

When working with Grothendieck universes one usually adds the following **axiom of universes** to the usual axioms of set theory:

* For every set $s$ there exists a universe which contains $s$, i.e. such that $s \in U$.

This way whenever any operation leads one outside of a given Grothendieck universe (see applications below), there is guaraneteed to be a bigger Grothendieck universe in which one lands.  In other words, every set is small if your universe is large enough!

##Structural

An equivalent (at least for our purposes) concept can also be defined in structural set theories (like [[ETCS]]).

... I\'m writing this offline, in case more people want to edit the rest of the page meanwhile ---Toby ...


+-- {: .query}
[[Urs Schreiber|Urs]]: unless I am missing something, the Grothendieck universe approach goes right against Lawvere's attitude to set theory as reviewed and emphasized at [[Trimble on ETCS I]]: that it is unnatural to consider membership of sets as a global relation, i.e. to handle sets and their elements on the same footing. On the contrary, for the above definition to even make sense, we have to assume that "everything is a set" (becuase the above definition tacitly assume that every element of a Grothendieck universe is itself a set). 

So what is the analog of Grothendieck universes, or of what they accomplish in practice, in [[ETCS]]? How are the applications mentioned below handled in [[ETCS]] without use of Grothendieck universes?

[[Todd Trimble|Todd]]: Urs asked me to comment here, although I don't consider myself all that qualified. I know Mike Shulman has thought at length about all these issues. 

But a nice way of thinking of Grothendieck universes is as an internal topos object. That is, it is possible to express the notion of 'topos object' in any category with finite limits, and then one can define a Grothendieck universe within say a topos or pretopos of sets $E$ as such an internal topos object $U$ inside $E$. Mike?
=--


#Applications#

Let $U Set$ be the [[category]] of $U$-small sets, a [[full subcategory]] of [[Set]].

A category whose set of morphisms is $U$-small may be called a $U$-[[small category]]; it can also be thought of as an [[internal category]] in $U Set$.

A category whose [[hom-set]]s are all $U$-small may be called [[locally small category|locally]] $U$-small; it can also be thought of as an [[enriched category]] over $U Set$.  Every $U$-small category is locally $U$-small.

A category whose set of morphisms is $U$-large may be called a $U$-[[large category]]; normally, this term is used only when the category is not also $U$-small.  Typically, $U$-large categories are locally $U$-small and vice versa, but exceptions are possible.

Note that $U Set$ itself is $U$-large and locally $U$-small.

##Presheaf categories##

Let $C$ be a $U$-small category.  Then the category of $U$-[[presheaf|presheaves]] on $C$ (the [[functor category]] $[C^{op}, U Set]$) is also $U$-large and locally $U$-small, but not $U$-small unless $C$ is empty.  ($U Set$ itself is the special case of this where $C$ is the [[point]].)

Now let $C$ be a $U$-large category (and not small).  Then the category of $U$-presheaves on $C$ is not even locally $U$-small, nor is it even $U$-large (it is 'too large to be large').  However, it is locally $U$-large.  Also, it is quite possible, if $C$ is a $U$-[[large site]], that the category of $U$-[[sheaf|sheaves]] on $C$ is $U$-large and locally $U$-small.

+-- {: .query}

[[Zoran Skoda]] But starting with a $U$-small category one can look at the category of $U$-small presheaves instead of all presheaves.
This has been useful in hmotopy theory, there is for example
a paper by Chorny and Dwyer using it. Look also at the paper by Day and Lack on limits of small functors.
www.maths.usyd.edu.au/u/stevel/papers/small.pdf 
 I once listened a talk by Chorny in Barcelona where he was convincing that in practice we should use small Yoneda lemma rather than the usual Yoneda, he had arguments that a number of things are more natural, but I have not being taking notes and he never wrote those things in a paper as far as I know (I do not see them in his other papers in which he uses small presheaves but without some of that discussion).
See anyway
http://wwwmaths.anu.edu.au/~chorny/personal/research/
and also earlier minipreprint version
http://www.math.uwo.ca/~bchorny2/research/smalldiag.ps
the results of Chorny-Dwyer is cited  (I did not look yet how much used yet) by Rosicky in Accessible categories and homotopy theory
www.math.yorku.ca/~tholen/HB07Rosicky.pdf
=--