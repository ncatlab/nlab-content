# Idea #

A homotopy $n$-type is a space where we consider its properties only up to the $n$th [[homotopy group]] $\pi_n$.
+-- {: .query}
[[Tim Porter|Tim]]:  When teaching homotopy theory I found blank looks from students if I used this idea as motivation as they felt it was too vague. I also do not like the idea of an $n$-type being a space as it does not allow one to say that two spaces 'have the same $n$-type.'

_Toby_:  If you can explain the motivation that works here, then please do!  But this doesn\'t say that a type is a kind of space, it says that it\'s a space 'up to ...', so two spaces have the same type if they\'re the same 'up to ...'.  (In other words, we have a surjection Spaces &#8594; Types rather than an injection Types &#8594; Spaces, at least for purposes of motivation since of course both do exist).

[[Tim Porter|Tim]]:As you sort of suggest, the problem is in the exact choice of words! At present you actually do say it is a space, at least as I read it, and that is my problem with the wording. Liberal use of inverted commas is not a good way around the difficulty.  I will bounce a form of words past you to see how you like it first.

'In talking of a homotopy n-type, we are thinking of a space, or spaces, where the properties being considered are given by the homotopy groups $\pi_1$ up to $\pi_n$, so information recorded by the even higher homotopy groups is ignored.'

How about something along those lines?

Another question is how long should this entry on homotopy n-type be? I put in something on simplicial groups as an illustration, which I think you removed, but that section now reads strangely as after the first line (which mentions them) there does not seem to be any mention after that! As you and I seem, de facto, to be the main contributors on this entry (not exclusively) perhaps some discussion of the overall structure might be an idea.
=--
# Motivation #

For [[nice topological space|'nice' spaces]], 
+-- {: .query}
[[Tim Porter|Tim]]: As I read the entry on nice topological spaces, it really refers to 'nice categories' rather than 'nice spaces'! I have always thought of spaces such as CW-complexes and polyhedra as being 'locally nice', but the corresponding categories are certainly not 'nice' in the sense of  [[nice topological space]]. Perhaps we need to adjust that other entry in some way.

_Toby_:  You\'re right, I think I\'ve been linking that page wrongly.  (I just now did it again on [[homotopy type]]!)  Perhaps we should write [[locally nice space]] or [[locally nice topological space]] (you pick), and I\'ll fix all of the links tomorrow.

[[Tim Porter|Tim]]:I suggest [[locally nice space]].  (For some time I worked in Shape Theory where local singularities were allowed so the spaces were not locally nice!) There would need to be an entry on locally nice. I suggets various meanings are discussed briefly, e.g. locally contractible, locally Euclidean,  ... and so on, but each with a minimum on it as the real stuff is in CW-complex etc and these are the 'ideas'.
=--
e.g., CW-complexes, a weak [[homotopy equivalence]] is the same as a homotopy equivalence.  Here a weak homotopy equivalence is a map which induces an isomorphism on all [[homotopy group]]s:
$$f:X\to Y \Leftrightarrow \pi_k(f) : \pi_k(X)\to \pi_k(Y)$$
for all $k \geq 0$ and all choices of base point.  (For [[simplicial group]]s or [[groupoid]]s, we have a similar notion.)

What if we only have that $\pi_k(f)$ is an isomorphism up to some dimension, $n$, what can we say about the 'homotopy types'? Any space is equivalent in this truncated form to a space with trivial homotopy groups above level $n$, so can we find reasonably complete _algebraic_ models for such $n$-types.

# Definition #

A continuous map $X \to Y$ is a **homotopy $n$-equivalence** if it induces isomorphisms on $\pi_i$ for $0 \leq i \leq n$ at each basepoint.  Two spaces share the same **homotopy $n$-type** if they are linked by a zig-zag chain of homotopy $n$-equivalences.

More formally, inverting the $n$-equivalences in a category $\Sp$ of nice spaces gives a category $\Ho_n(\Sp)$ and two spaces have the same **homotopy $n$-type** if they are isomorphic in $\Ho_n(\Sp)$.

For any nice space $X$, you can kill its homotopy groups in higher dimensions by attaching cells, thus constructing a new space $Y$ so that the inclusion of $X$ into $Y$ is a homotopy $n$-equivalence; up to (weak) [[homotopy equivalence]], the result is the same for any space with the same homotopy $n$-type as $X$.  Accordingly, a **homotopy $n$-type** may alternatively be defined as a space with trivial $\pi_i$ for $i \gt n$, or as the unique (weak) [[homotopy type]] of such a space, or as its fundamental $\infty$-[[fundamental infinity-groupoid|groupoid]] (which should be an $n$-[[n-groupoid|groupoid]], by one direction of the [[homotopy hypothesis]]).

# Algebraic models #

We will use simplicial groups and simplicial groupoids rather than spaces below as they are already partially algebraicised.

Considerable effort has gone into finding 'good' algebraic models for (connected) homotopy $n$-types. In low dimensions the results are 'old' or 'classical'.  (We will consider connected cases only.  The extension to the non-connected case is 'routine'.)

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