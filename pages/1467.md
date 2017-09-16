## Idea

A [[topological space]] (or more generally [[convergence space]]) is _compact_ if everything converges as much as possible. It is a kind of ultimate topological expression of the general idea of a space being "closed and bounded": every [[net]] must accumulate somewhere in the space; by boundedness it cannot escape, and by closure the point is in the space. There is also a notion of compactness for [[locale]]s.

## Definitions 

There are many ways to characterize compactness. The first is perhaps the most common: 

* $X$ is **compact** if for every collection of open sets whose union is $X$ (which _[[cover]]s_ $X$), there is a (Kuratowski)-[[finite set|finite]] subcollection which also covers $X$. 

If [[excluded middle]] is assumed, this is easily equivalent to: 

* For any collection of closed sets of $X$ whose intersection is [[empty set|empty]], some finite subcollection also has empty intersection. 

If the [[ultrafilter theorem]] (a weak form of the [[axiom of choice]]) is assumed, compactness can be characterized in terms of [[ultrafilter]] (or ultranet) convergence: 

* Every ultrafilter $\mathcal{U}$ (or ultranet $\nu$) on $X$ converges to some point $x \in X$, meaning that $\mathcal{U}$ contains the filter of neighborhoods of $x$ (or that $\nu$ is eventually in any neighbourhood of $x$). 

In any case, compactness can be characterized in terms of [[filter]] (or [[net]]) convergence:

* Every filter (or net) on $X$ has a convergent refinement (or subnet). 

This is equivalent to the characterization given in **Idea** above: 

* Every filter $\mathcal{U}$ (or net $\nu$) on $X$ has a cluster point $x$, meaning that every element of $\mathcal{U}$ meets every neighbourhood of $x$ (or $\nu$ is frequently in every neighbourhood of $x$).

The convergence characterisations make sense in any [[convergence space]]; here is a definition for [[locale]]s:

* ... (Get this from Johnstone).

Assuming the axiom of choice, compactness can also be characterized in terms of universal closure: 

* $X$ is compact iff for any space $Y$, the projection map $X \times Y \to Y$ is closed. 

+--{.query}
I'm not entirely sure that the axiom of choice is needed to prove the last equivalence. It's easy (and classical) that the projection map is closed if $X$ is compact. For the other direction, I know a proof which involves taking $Y$ to be the space of ultrafilters on the underlying set of $Y$, but there may be some other choice(s) for $Y$ which allows one to get around AC. 
=-- 

## Standard Results

* A topological space $X$ is compact if it is a [[compact object]] in its [[category of open subsets]] $Op(X)$.

* Assuming the axiom of choice, the category of compact spaces admits all small [[limit]]s. See also [[Tychonoff theorem]]. In any case, the category of compact locales admits all small limits.

* The direct [[image]] of a compact subspace under a continuous map is compact. Thus any topological space becomes a [[bornological space]] by taking the bounded sets to be compact subspaces. 

* In the presence of compactness, the following three [[separation axioms]] are equivalent: $T_2, T_3, T_4$. That is, a compact Hausdorff space must be normal.

One often wishes to study compact [[Hausdorff space]]s.  For locales, one usually speaks of compact *regular* locales; these are equivalent (since every locale is $T_0$ and hence $T_3$ if regular) since regularity is easier to formulate and handle than Hausdorffness.

## Terminology

Some authors use "compact" to mean "compact Hausdorff" (a much [[nice topological space|nicer sort of space]], and forming a much [[nice category of spaces|nicer category of spaces]]), and use the word "[[quasicompact]]" to refer to just "compact" as we are using it here. This custom seems to be prevalent among [[algebraic goemetry|algebraic geometers]], for example, and particularly so within Francophone schools.

But it is far from clear to me ([[Todd Trimble]]) that "quasicompact" is very well-established outside such circles (despite some arguments in favor of it), and using simply "compact" for the nicer concept therefore carries some risk of creating misunderstanding among mathematicians at large. My own habit at any rate is to say "compact Hausdorff" for the nicer concept, and I will continue using this on the nLab until consensus is reached (if that happens). 

Another term in usage is 'compactum' to mean a compact Hausdorff space (even when 'compact' is not used to imply Hausdorffness).