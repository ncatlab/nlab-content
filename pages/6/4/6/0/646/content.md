
#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

The most important invariants of a [[topological space]] $X$ or, more generally, of an object $X$ in an [[∞-stack]] [[(∞,1)-topos]] are its [[homotopy group]]s $\pi_k(X)$.

A **homotopy $n$-type** is an object $X$ for which all $\pi_k(X)$ with $k \gt n$ are trivial. More precisely, these are the [[n-truncated object of an (infinity,1)-topos|n-truncated objects]] and one says that two object $X$, $Y$ are _of the same homotopy $n$-type_ if there is a zig-zag of morphisms connecting them that induces [[isomorphism]]s on [[homotopy group]]s $\pi_k(X) \stackrel{\simeq}{\to} \pi_k(Y)$ for $0 \leq k \leq n$.

So homotopy $n$-types are the equivalence classes of an [[equivalence relation]] imposed on objects in [[Top]] (or objects in another [[(∞,1)-topos]]). Thus, we say that two spaces 'have the same homotopy $n$-type' if their [[homotopy group]]s agree up to $\pi_n$, and 'a homotopy $n$-type' can equally well be represented by any space having that $n$-type.  This is analogous to the definition of 'a [[real number]]' as an equivalence class of Cauchy sequences.

However, as usual in [[homotopy theory]], merely having isomorphic homotopy groups is not enough; rather there needs to be a map _inducing_ such an isomorphism.  Thus, the relevant equivalence relation relates two spaces when there is a zigzag of maps between them, all inducing isomorphisms on homotopy groups $\pi_k$ for $k\le n$.  One can then show that any space is equivalent, in this sense, to one having trivial homotopy groups above level $n$, so that the other definition is also correct.

The use of [[topological space]]s is not, of course, essential; we could just as well use any other structure that models the same [[homotopy theory]], such as [[simplicial set]]s, [[simplicial groupoid]]s, or (for [[connected space]]s) [[simplicial group]]s.  Moreover, the fact that homotopy $n$-types can be modeled by spaces that are trivial above level $n$ raises the possibility of finding reasonably complete _algebraic_ models for such $n$-types.


+-- {: .query}
[[Tim Porter|Tim]]:  When teaching homotopy theory I found blank looks from students if I used this idea as motivation as they felt it was too vague. I also do not like the idea of an $n$-type being a space as it does not allow one to say that two spaces 'have the same $n$-type.'

_Toby_:  If you can explain the motivation that works here, then please do!  But this doesn\'t say that a type is a kind of space, it says that it\'s a space 'up to ...', so two spaces have the same type if they\'re the same 'up to ...'.  (In other words, we have a surjection Spaces &#8594; Types rather than an injection Types &#8594; Spaces, at least for purposes of motivation since of course both do exist).

[[Tim Porter|Tim]]:As you sort of suggest, the problem is in the exact choice of words! At present you actually do say it is a space, at least as I read it, and that is my problem with the wording. Liberal use of inverted commas is not a good way around the difficulty.  I will bounce a form of words past you to see how you like it first.

'In talking of a homotopy n-type, we are thinking of a space, or spaces, where the properties being considered are given by the homotopy groups $\pi_1$ up to $\pi_n$, so information recorded by the even higher homotopy groups is ignored.'

How about something along those lines?

Another question is how long should this entry on homotopy n-type be? I put in something on simplicial groups as an illustration, which I think you removed, but that section now reads strangely as after the first line (which mentions them) there does not seem to be any mention after that! As you and I seem, de facto, to be the main contributors on this entry (not exclusively) perhaps some discussion of the overall structure might be an idea.

[[Mike Shulman|Mike]]: The really precise way to say it is, of course, that a homotopy $n$-type is an object of the homotopy category (or $\infty$-category) of spaces where we invert the $n$-equivalences.  This is analogous to defining a real number to be an equivalence class of Cauchy sequences of rationals; two spaces 'have the same $n$-type' in the same sense that two Cauchy sequences of rationals 'define (or converge to) the same real number'.  Perhaps it would be useful to say this?

_Toby_:  My only use of quotation marks was to provide direct quotations; of course we don\'t need scare quotes in the text.  You are all saying fine things, so I will [be bold](https://secure.wikimedia.org/wikipedia/en/wiki/Wikipedia:Be_bold) and incorporate them now.  (In the end, I tightened up the prose a bit, but change it if you don\'t like it.)

I didn\'t mean to *remove* anything about simplicial groups, just to generalise.  But I specified how to interpret it for simplicial groups in the algebraic models below.  But maybe none of that really depends on using simplicial groups?  What you had before didn\'t read to me as an example so much as a prerequisite for the remainder to be correct.

[[Mike Shulman|Mike]]: I moved the discussion on nice spaces to [[nice topological space]], and merged the two sections "Idea" and "Motivation" since I was confused about the distinction between them.
=--

# Definition #

A continuous map $X \to Y$ is a **homotopy $n$-equivalence** if it induces isomorphisms on $\pi_i$ for $0 \leq i \leq n$ at each basepoint.  Two spaces share the same **homotopy $n$-type** if they are linked by a zig-zag chain of homotopy $n$-equivalences.

More formally, inverting the $n$-equivalences in [[Top]] gives a [[homotopy category]] $\Ho_n(\Top)$, and two spaces have the same **homotopy $n$-type** if they become isomorphic in $\Ho_n(\Top)$.

For any space $X$, you can kill its homotopy groups in higher dimensions by attaching cells, thus constructing a new space $Y$ so that the inclusion of $X$ into $Y$ is a homotopy $n$-equivalence; up to (weak) [[homotopy equivalence]], the result is the same for any space with the same homotopy $n$-type as $X$.  Accordingly, a **homotopy $n$-type** may alternatively be defined as a space with trivial $\pi_i$ for $i \gt n$, or as the unique (weak) [[homotopy type]] of such a space, or as its fundamental $\infty$-[[fundamental infinity-groupoid|groupoid]] (which should be an $n$-[[n-groupoid|groupoid]], by one direction of the [[homotopy hypothesis]]).

One can also construct [[model category|model structures]] on $\Top$ whose homotopy categories are the categories $\Ho_n(\Top)$.  This is one of the original examples of [[Bousfield localization]].  From this perspective, the above replacement of a space by one having trivial $\pi_k$ for $k\gt n$ is an example of _fibrant replacement_.


# Algebraic models #

We will use simplicial groups and simplicial groupoids rather than spaces below as they are already partially algebraicised.  So in the definition above, 'space' means a simplicial group(oid) and 'continuous map' means a homomorphism of simplicial group(oid)s.

Considerable effort has gone into finding 'good' algebraic models for (connected) homotopy $n$-types. In low dimensions the results are 'old' or 'classical'.  We will consider connected cases (simplicial groups) only.  The extension to the non-connected case (simplicial groupoids) is 'routine'.

* The 1-type of a connected space is completely determined by its [[fundamental group]], so groups form an algebraic model for [[homotopy 1-type]]s. For the non pointed case, we can say [[groupoid]]s form an algebraic model. 

* [[crossed module|Crossed modules]] form an algebraic model for [[homotopy 2-type]]s by a result of Mac Lane and Whitehead
     
*  S. Mac Lane and J. H. C. Whitehead, _On the 3-type of a complex_, Proc. Nat. Acad. Sci. U.S.A., 36, (1950), 41 &#8211; 48.

The use of crossed modules of groupoids and their [[classifying space]] for the non pointed case is explained under [[homotopy 2-type]]. 


*  Finding the algebraic model for the $n$-types is just a start.  Ideally one searches for algebraic models of all the higher homotopy structure as well.

* The method initiated by J.H.C. Whitehead was to approximate homotopy theory by models which analysed particular types of behaviour. One of his most widely followed models is that of [[stable homotopy theory]]. The opposite method was to find algebraic models of restricted classes of spaces, such as 2-types, or with cells in a small range of dimensions.  H.-J. Baues has followed up many of the latter ideas. 

It is sensible to regard [[crossed complex|crossed complexes]] as giving a _linear_ model of homotopy types. These crossed complexes are equivalent to [[strict omega-groupoid|strict globular]] $\infty$-groupoids. Although these are restricted model of homotopy types, they are convenient in many aspects, because of the many analogies with the familiar [[chain complex]]es. 

Crossed complexes capture operations of the fundamental groupoid, but not quadratic information such as Whitehead products (for dimensions $\gt 1$). However one can define $n$-fold crossed complexes inductively as crossed complexes internal to $(n-1)$-fold crossed complexes. So one can give the 

*(Conjecture) double crossed complexes capture the quadratic information on homotopy types, triple crossed complexes capture the cubic information, etc., etc. 

This has the possibility of leading to computations, by applying [[van Kampen theorem]]s to specific levels.


[[!redirects n-type]]