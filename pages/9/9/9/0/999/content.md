# Idea

An [[object]] of a [[category]] is often called *compact* if it is "finite" in some precise sense.

# Compactness in additive categories

When $C$ is an [[additive category]] (often a [[triangulated category]]), an object $x$ in $C$ is called __compact__ if for every set $S$ of objects of $C$ such that the coproduct $\coprod_{s\in S} s$ exists, the canonical map
$$
\coprod_{s\in S} C(x,s)\to C(x,\coprod_{s\in S}s)
$$
is an isomorphism of sets.

A triangulated category is __compactly generated__ if it is generated (see [[generator]]) by a _set_ of compact objects.

The notion can be modified for categories [[enriched category|enriched]] over a [[closed monoidal category]] (compare to the notions of finite and/or rigid objects in various contexts).

Compact objects in the derived categories of quasicoherent sheaves over a scheme are called perfect complexes. Any compact object in the category of modules over a perfect ring is finitely generated as a module.  Lurie uses $\kappa$-compact objects in the setup of $(\infty,1)$-categories.

# Compactness in non-additive categories

In non-additive contexts, the above definition is not right.  For instance, with this definition a [[topological space]] would be compact iff it is [[connected space|connected]]. In general one should expect to preserve _filtered colimits_ (see below for discussion). For $C$ any category and $X \in C$, the condition that $C(X,-) : C \to C$ preserves [[filtered category|filtered]] [[colimit]]s imposes  some kind of finiteness condition on $X$. For instance 

* in $C = $ [[Set]] this is the case if the set $X$ is [[finite set|finite]];
* in $C$ a [[topos]] this is the case if the object $X$ is $K$-[[finite object|finite]];
* in $C =$ [[Grp]] this is the case if the group $X$ is [[finitely presentable object|finitely presented]] as a group.

## Definition ##

An object $x$ is __compact__ if for every [[filtered category|filtered]] or [[direction|directed]] colimit $\colim_{d\in D} S_d$ in $C$, the canonical map
$$
\colim_{d\in D} C(x,S_d)\to C(x,\colim_{d\in D}S_d)
$$
is an isomorphism.  Sometimes, especially in categories like [[Top]], one may want to restrict to directed "unions," meaning directed colimits whose transition morphisms are (possibly [[strong monomorphism|strong]]) [[monomorphism]]s.


# Compact objects in Top

In the category [[Top]] of [[topological space]]s it is sometimes said that one has the following equivalent definitions of when a [[topological space]] $X$ is _compact_ in that every open cover of it has a finite subcover:

   X is compact precisely if the [[hom-functor]] $Top(X,-) : Top \to Top$ commutes with [[filtered category|filtered]] [[colimit]]s.

In fact, this characterization is not right, as was [pointed out](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_3.html#c023790) by Todd Trimble at the n-category cafe, via a (corrected) counterexample given on page 49 of Hovey's Model Categories due to Don Stanley. 

Namely, the two-element set with the indiscrete topology is a compact space $X$ for which 
 \[
 Hom(X, -): Top \rightarrow Top
\]
doesn't preserve filtered colimits, in fact not even colimits of sequences (functors out of the ordered set of natural numbers). 

For example, consider the sequence of spaces 
 \[
 X_n=[n,\infty) \times \{0,1\}
\]
where the open sets are of the form 
\[
 [n, \infty]\cup [m,\infty) \times \{1\}
\]
(where $m \geq n$), plus the empty set. Define $X_n \rightarrow X_{n+1}$ so that it sends a pair $(k, \epsilon)$ to itself if $k \gt n$, and $(n,\epsilon)$ to $(n+1,\epsilon)$. This defines a functor 
\[
F: \mathbb{N} \rightarrow Top 
\]
The colimit $X_\infty$ of this sequence is the two-element set $\{0,1\}$ with the indiscrete topology. However, the identity map on this space does not factor through any of the canonical maps $X_n \rightarrow X_\infty$. It follows that 
the comparison map 
\[
 colim_n Hom(X_\infty, X_n) \rightarrow Hom(X_\infty, X_\infty)
\]
is not surjective, and therefore not an isomorphism. 

+--{.query}
_Todd_ (posted from n-category cafe): I don't know if the story is any different for X compact _Hausdorff_, but it could be worth considering. 
=--


# Further categorical properties of compact topological spaces

+--{.query}
_Todd_ (posted from n-category cafe):  One of the "hall-of-fame" results I had in mind is given on page 50 of Hovey's book: if Y is compact, then 
$hom(Y,-)$ preserves colimits of functors mapping out of limit ordinals, provided that the arrows of the cocone diagram, 
 \[
 X_\alpha \rightarrow X_\beta,
\]
are closed inclusions of $T_1$ spaces. (This applies for example to the sequence of inclusions of n-skeleta in a CW-complex. Taking $Y=S_k$, this has obvious desirable consequences for the functor $\pi_k$.) Hovey wants this result in view of a small object argument on the way to proving that Top is a model category. I'll bet one can beef it up to a similar result but for more general filtered diagrams. 

I call it a hall-of-fame result because (a) it's quite useful; (b) it's not entirely trivial to prove. Further precise results along these lines would be most welcome. 
=--






