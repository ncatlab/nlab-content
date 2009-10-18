The [[Set|category of sets]] is, among other things, a [[well-pointed topos]] with a [[natural numbers object]] satisfying the [[axiom of choice]]---i.e. a model of [[ETCS]].  However, $Set$ cannot be characterized *uniquely* by this or any other elementary property, i.e. by a property that doesn't refer, explicitly or implicitly, to the notion of set.  This is a version of [[Gödel's incompleteness theorem]].

However, $Set$ can be characterized uniquely by the addition of non-elementary categorial properties, the most notable and obvious of which are [[complete category|completeness]] and [[cocomplete category|cocompleteness]].  On the other hand, it is also true that any [[topos]] is complete and cocomplete relative to itself, in the sense that its [[self-indexing]] is complete and cocomplete as an [[indexed category]].  Thus, in order to characterize $Set$ in this way we have to mean "external" completeness and cocompleteness (which is the intuitive notion of completeness, in the context of some notion of set).

+-- {: .un_theorem}
###### Theorem
Let $S$ be a [[locally small category|locally small]] model of ETCS; the following are equivalent.

1. $S$ is equivalent either to $Set$ or to the category of sets in some [[Grothendieck universe]].
1. $S$ admits all coproducts indexed by its own [[homsets]].
1. $S$ admits all products indexed by its own [[homsets]].
=--
+-- {: .proof}
###### Proof
The implications from 1 to 2 and 1 to 3 are easy exercises, following from the "second-order replacement axiom" of a Grothendieck universe.  And the implication from 3 to 2 follows because any [[topos]] which has some type of [[limit]] automatically also has the same sort of [[colimit]], because $S^{op}$ is [[monadic adjunction|monadic]] over $S$ (via the contravariant powerset functor).  Thus, it remains to prove that 2 implies 1.  So suppose that $S$ admits coproducts indexed by its homsets.  In particular, for any $X\in S$ we can form the coproduct $\coprod_{x\colon 1\to X} 1$, which of course comes with a canonical map to $X$.  This map is a bijection on [[global elements]], so since $S$ is well-pointed, it is an isomorphism.

Consider the "global sections" functor $\Gamma = S(1,-) \colon S\to Set$.  Well-pointedness implies that this functor is [[faithful functor|faithful]] and [[conservative functor|conservative]].  However, since by the above we have $X\cong \coprod_{\Gamma(X)} 1$, it follows that $\Gamma$ is [[full functor|full]] as well, so that $S$ is equivalent to a [[full subcategory]] of $Set$.  From now on we identify it with its [[essential image]].

Let $X\in S$ and suppose that $Y\subset X$ is a subset of $X$.  By assumption on $S$, it admits the coproduct $\coprod_{x\colon 1\to X} Z_x$ where $Z_x$ is $1$ if $x\in Y$ and $\emptyset$ otherwise.  But this coproduct maps to $Y$ via a bijection on global elements as before, so it is an isomorphism, and thus $Y\in S$ as well.  Hence $S$ is closed in $Set$ under subsets.  It follows that the full inclusion $S\hookrightarrow Set$ is a bijection on [[subobject]] lattices, and thus a [[logical functor]] (preserves [[power objects]]).  Finally, the hypothesis on coproducts implies that the union of an $S$-set of $S$-sets is again an $S$-set.

(We have proven the axioms of a universe in a "structural" form.  We can alternately directly construct an [[inaccessible cardinal]] such that $S$ is the category of sets in $V_\kappa$.  Let $\kappa$ denote the smallest cardinal number not in $S$, it follows that $S$ consists precisely of the sets of cardinality $\lt\kappa$.  Since $S$ is a topos with a NNO, $\kappa$ must be an uncountable strong limit.  Finally, if $X\in S$ and $Y_x \in S$ for each $x\in X$, then $\coprod_{x\colon 1\to x} Y_x\in S$, showing that $\kappa$ is regular, and hence inaccessible.)
=--

+-- {: .un_cor}
###### Corollary
$Set$ is, up to equivalence, the unique locally small and cocomplete model of ETCS, and the unique locally small and complete model of ETCS.
=--

A more direct proof of the corollary is possible.

+-- {: .proof}
###### Proof
We show as in the theorem that $\Gamma$ is a full inclusion.  Cocompleteness of $S$ then shows that it has a left adjoint given by $X\mapsto \coprod_X 1$, so it suffices to show that the unit $X\to S(1,\coprod_X 1)$ of this adjunction is a bijection.

For injectivity, we need to show that if $j_x=j_y$, then $x=y$.  If $x\neq y$, then since coproducts in a topos are [[disjoint coproduct|disjoint]], the pullback of $j_x$ and $j_y$ is the initial object $0$.  But since $j_x=j_y$, their pullback is also $1$.  By well-pointedness, $0$ is not isomorphic to $1$, so by contradiction, $x=y$.

For surjectivity, we need to show that any map $k\colon 1\to \coprod_X 1$ is equal to $j_x$ for some $x$.  Now for each $x$, the pullback of $k$ and $j_x$ is a [subobject of 1](http://ncatlab.org/nlab/show/subterminal+object), call it $U_x$.  Since a well-pointed topos in an ambient Boolean logic is Boolean and two-valued, each $U_x$ must be either $0$ or $1$.  Since coproducts in a topos are [[pullback stability|stable under pullback]], $1 = \coprod_X U_x$.  But then if $U_x=0$ for every $x$, we would have $1 = \coprod_X 0 = 0$, contradicting well-pointedness.  Thus there must be an $x$ with $U_x=1$, which implies that $k=j_x$.
=--


## Intuitionistic Failure

This theorem, and even the corollary, fail intuitionistically, as may be suspected from the use of [[excluded middle]] in their proofs.  A concrete counterexample is given by the following.

Let $\mathcal{U}$ be a truth value (identified with the subset $\{\star | \mathcal{U}\} \subseteq \{\star\} = 1$) such that $\not\not\mathcal{U}$ is valid and $\mathcal{U}$ is indecomposable and projective, and let $S$ be the topos $Set/\mathcal{U}$.  Then $S$ is a [[Grothendieck topos]], hence cocomplete and locally small, and the assumptions on $\mathcal{U}$ ensure that it is well-pointed, but in an intuitionistic theory they don't imply that $\mathcal{U}=\top$.
