# Ternary frames
* table of contents
{: toc}

## Warning

*The term 'frame' is used in a different sense here than in [[geometric logic]]; see [[frame]].  The usage here is analogous to [[Kripke frames]] in [[modal logic]].*

## Idea

A **ternary frame** is a way of presenting a model for a [[substructural logic]] (such as [[linear logic]] and [[relevant logic]]) in terms of a set of "worlds" or "states of information" and a ternary [[relation]].

The construction generalizes from [[posets]] to [[categories]] using the [[Day convolution]] of a [[promonoidal category]] ([see below](#dayconvolution)), or a "promagmal category" in the weakest version.

## Definition

A **ternary frame** is a set $A$ together with a ternary relation $R$ on $A$; we write $R x y z$ when $R$ holds of three elements $x,y,z\in A$.

We may additionally ask that $A$ have a [[partial ordering]]; in this case we demand the compatibility condition that if $R x y z$ and $x'\le x$, $y'\le y$, and $z\le z'$, then also $R x' y' z'$.

## Modeling substructural logic

We can model [[logic]] using a ternary frame with a "forcing" or "satisfaction" relation between points of $A$ and formulas.  We begin by assigning to each [[atomic formula]] a set of points of $A$ which satisfy it.  If $A$ has a partial order, as above, then we ask each of these sets to be up-closed.

The [[logical connectives]] can then be defined inductively by clauses such as the following:

* $x \Vdash P \& Q$ (the negative [[conjunction]]) if and only if $x\Vdash P$ and $x\Vdash Q$.
* $x \Vdash P \oplus Q$ (the positive [[disjunction]]) if and only if $x \Vdash P$ or $x\Vdash Q$.
* $x \Vdash \mathbf{0}$ (the positive [[falsity]]) never.
* $x \Vdash \top$ (the negative [[truth]]) always.
* $x \Vdash P \otimes Q$ (the positive conjunction) if and only if there exist $y,z$ such that $R y z x$ and $y\Vdash P$ and $z\Vdash Q$.
* $x \Vdash P \multimap Q$ (the one-sided linear implication) if and only if for all $y,z$, if $R x y z$ and $y\Vdash P$, then $z\Vdash Q$.
* $x \Vdash Q &#10204; P$ (the dual linear implication) if and only if for all $y,z$, if $R x y z$ and $z\Vdash P$, then $y\Vdash Q$.

The logic obtained thereby will generally be [[substructural logic|substructural]]: it need not satisfy the structural rules like [[weakening rule|weakening]], [[contraction rule|contraction]], [[exchange rule|exchange]] or even associativity and unit for the tensor product. On this page, we have used the notation for substructural connectives from [[linear logic]].

## Additional structure

We can impose properties or structure on the ternary frame to affect the logic.  For instance, if $R x y z$ implies $R y x z$, then the logic we obtain will satisfy the exchange rule.

We also need additional structure in order to model positive truth, negative falsity, negative disjunction, and negation.

### Truth sets

A **truth set** in an ordered ternary frame is a subset $T\subseteq A$ such that $x\le y$ if and only if there exists a $t\in T$ with $R t x y$, and if and only if there exists an $s\in T$ with $R x s y$.  (If $R$ is commutative, as above, then the two conditions are equivalent.)  Alternatively, given an unordered ternary frame $A$ and a subset $T$, we could *define* $x\le y$ in this way, and then require as a property of $T$ that the resulting relation is a [[partial order]].

If $T$ is a truth set, then it makes sense to define

* $x \Vdash \mathbf{1}$ (the positive truth) if and only if $x\in T$.

### Compatibility relations

One way to model negation (and thereby obtain negative falsity $\bot$ and negative disjunction $\parr$ by duality from positive truth $\mathbf{1}$ and positive conjunction $\otimes$) is with a **compatibility relation**, which is just a binary relation $C$.  If $A$ has a partial order, we demand additionally that if $x C y$ and $x'\le x$ and $y\le y'$, then $x' C y'$.

Given such a $C$, we define

* $x \Vdash \neg P$ if and only if for all $y$, if $x C y$ then not $y\Vdash P$.

### Falsity sets

Negation can alternatively be modeled using a *false set*.  Suppose given a subset $F\subseteq A$, to be the interpretation of the negative falsity $\bot$:

* $x\Vdash \bot$ if and only if $x\in F$.

We can then, if we wish, interpret negation and negative disjunction by defining $\neg P \coloneqq (P\multimap \bot)$ and $P\parr Q \coloneqq \neg (\neg P \otimes \neg Q)$.

The latter is most sensible if negation is involutive, which it need not be in general --- that is, if $x \Vdash \neg \neg P$ we need not have $x\Vdash P$.  One solution to this (if we want negation to be involutive) is to close up $\Vdash$ under double-negation.  This entails replacing the clauses defining the interpretation of the positive connectives $\otimes$, $\oplus$, $\mathbf{1}$, and $\mathbf{0}$ with their double-negation closure.  This is commonly done in the [[phase semantics]] for linear logic (see below).


## From ternary frames to quantales {#dayconvolution}

Since the models above associate to formulas *subsets* of $A$, it seems natural to describe them in a purely algebraic way using structure on the [[powerset]] of $A$.  In the case when $A$ is a poset, instead of the powerset of $A$ we must use the set of up-closed subsets of $A$.  Since this subsumes the unordered case (use the discrete ordering), we henceforth assume $A$ to be a poset, with $R$ having the assumed compatibility relation.

In fact, this axiom (which we repeat here for the reader's convenience):

* if $R x y z$ and $x'\le x$, $y'\le y$, and $z\le z'$, then also $R x' y' z'$.

says precisely that $R$ is a $\mathbf{2}$-[[enriched category|enriched]] [[profunctor]] $A^{op} \times A^{op} &#8696; A^{op}$.  (Here we are identifying posets with $\mathbf{2}$-enriched categories, where $\mathbf{2}$ is the [[interval category]].)

Therefore, by [[Day convolution]], $R$ induces a binary tensor product on the $\mathbf{2}$-enriched [[presheaf category]] $\mathbf{2}^A$, which is precisely the poset of up-closed sets in $A$.  This tensor product is precisely the above interpretation of $\otimes$.  By the usual Day convolution arguments, this tensor product functor has both left and right adjoints, which are precisely the interpretation of $\multimap$ and its dual.

Of course, the interpretations of $\&$ and $\oplus$ are just the categorical product and coproduct in $\mathbf{2}^A$.  Similarly, that of $\mathbf{0}$ and $\top$ are the initial and terminal objects.

A truth set $T$ corresponds to a profunctor $1 &#8696; A^{op}$ which is a unit for the pro-multiplication $R$.  Therefore, in this case the tensor product on $\mathbf{2}^A$ has a unit object, which is precisely $T$, the interpretation of the positive truth $\mathbf{1}$.

If we were to additionally add the assumption that $R$ is *associative*, in the sense that

* there exists a $z$ with $R x y z$ and $R z u v$ if and only if there exists a $w$ with $R x w v$ and $R y u w$

then $A^{op}$ would become a [[promonoidal category|promonoidal]] poset, and hence $\mathbf{2}^A$ would be a complete and cocomplete closed monoidal poset, i.e. a [[quantale]].

A false set $F$ is of course just an arbitrary object of this quantale.  Closing up under double-negation means restricting to the sub-poset of elements that are equal to their "double dual" $x = (x \multimap F) \multimap F$.  Since the self-adjunction $(-\multimap F)$ is [[idempotent adjunction|idempotent]], this sub-poset is itself a quantale, and indeed a [[star-autonomous category|*-autonomous]] one.

The quantale-theoretic content of a compatibility relation is somewhat trickier: as defined it is a profunctor from $A$ to itself, whereas the negation of a pro-$*$-autonomous poset would be a profunctor from $A^{op}$ to $A$.  (This would induce a functor $(\mathbf{2}^A)^{op} \to \mathbf{2}^{A}$ due to the special property that $\mathbf{2}\cong \mathbf{2}^{op}$.)  Moreover, the definition of $x \Vdash \neg P$ for a compatibility relation is also the (metatheoretic) *negation* of the map on $\mathbf{2}^A$ that would be induced profunctorially.  If we put these together, we can see that negation ought to be the the composite of the map $\mathbf{2}^A \to \mathbf{2}^A$ induced by the profunctor $C$ with the isomorphism $\mathbf{2}^A \cong (\mathbf{2}^{A^{op}})^{op}$ (using again that $\mathbf{2}\cong \mathbf{2}^{op}$).  At least if $A$ is discrete, so that $A\cong A^{op}$, then this has the correct domain and codomain, so we should be able to assert an axiom ensuring that it makes $\mathbf{2}^A$ $*$-autononmous.

+--{: .query}
To be completed...
=--

### Generalizations

The quantale-theoretic viewpoint suggests a generalization replacing $\mathbf{2}$ by any other quantale.  That is, for any quantale $Q$, we can define a notion of "$Q$-valued ternary frame" that generates a new quantale by Day convolution.  Everything goes through without significant change, except that compatibility relations seem to require $Q$ itself to be $*$-autonomous.

## Examples

### Phase spaces

If $A$ is a [[magma]] with multiplication $\cdot$, then we can make it a ternary frame by defining $R x y z$ to mean $x \cdot y = z$.  More generally, if $A$ is a poset equipped with a binary multiplication $\cdot$, we can make it an ordered ternary frame by defining $R x y z$ to mean $x \cdot y \le z$.

If $\cdot$ has a unit object $t$, then $T = \{t\}$ (in the unordered case) or $T = \{x | t \le x \}$ (in the ordered case) is a truth set.

Categorically, this corresponds to the usual way of regarding a [[monoidal category]] as a [[promonoidal category]].

In the special case when $A$ is a commutative [[monoid]] equipped with a "false set" $F$ as above (usually written $\bot$) in this context, this semantics for linear logic is called [[phase semantics]] (see there for more).  It is usually expressed in terms of the quantale $\mathbf{2}^A$ obtained by Day convolution, but after passing to fixed points of the double-negation monad (in order to obtain an involutive negation).  In this context, fixed points of $\neg\neg$ are referred to as *facts*.

It is also possible to interpret the exponential modalities $!$ and $?$ of linear logic using phase space semantics.  For instance, we can define

* $x \Vdash !P$ if and only if $x$ belongs to the $\neg\neg$-closure of the set of all idempotents $y$ such that $y\Vdash P \& \mathbf{1}$.

and obtain $?P$ by duality.

Phase space semantics is *complete* for [[linear logic]], in the sense that a formula is provable if and only if in any phase space semantics we have $1\vDash P$, where $1$ is the unit element of the monoid $A$.

### PCAs

If $A$ is a [[partial combinatory algebra]] (PCA), we can make it a ternary frame by defining $R x y z$ to mean that $x \cdot y$ is defined and equals $z$.  (Similarly, if $A$ is an ordered PCA we can make it an ordered ternary frame.)  The resulting interpretation of $\multimap$ almost coincides with the usual interpretation of implication in [[realizability]] over $A$, and the combinators $k,s$ have the property that $k \Vdash P \multimap (Q \multimap P)$ and $s \Vdash (P \multimap Q \multimap R) \multimap (P \multimap Q) \multimap P \multimap R$ for any $P,Q,R$, as would be expected from typed [[combinatory logic]].


## References

* R. Routley and R.K. Meyer, *The Semantics of Entailment I*, Truth, Syntax and Modality, ed. H. Leblanc, North-Holland Publishing Company (Amsterdam), pp. 199-243.  (1973)

* R. Routley and R.K. Meyer, *The Semantics of Entailment, II-III*. Journal of Philosophical Logic, 1, 53-73 and 192-208.  (1972)

* Natasha Kurtonina, *Frames and Labels - A modal analysis of categorial inference*.  Ph.D. Thesis, Institute of Logic, Language and Information (ILLC), Amsterdam, 1994

* J. M. Dunn and R. K. Meyer, *Combinators and Structurally Free Logic*.  Logic journal of the IGPL, 5(4):505-538, July 1997

* Greg Restall, *An introduction to substructural logic*.  Routledge, 2000.

[[!redirects ternary frames]]
