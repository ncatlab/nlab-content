## Idea

A compact space is a [[topological space]] in which every [[net]] has a convergent subnet. It is a kind of ultimate topological expression of the general idea of a space being "bounded" in extent: every net must accumulate somewhere in the space (must frequently get close to some point $x$). 

## Definitions 

There are many ways to characterize compactness. The first is perhaps the most common: 

* $X$ is **compact** if for every collection of open sets whose union is $X$ (which _covers_ $X$), there is a finite subcollection which also covers $X$. 

This is easily equivalent to: 

* $X$ is compact if, for any collection of closed sets of $X$ whose intersection is empty, some finite subcollection also has empty intersection. 

If the [[axiom of choice]] is assumed, compactness can be characterized in terms of [[ultrafilter|filter]] convergence: 

* $X$ is compact if every [[ultrafilter]] $\cal{U}$ on $X$ converges to some point $x \in X$, meaning that $\cal{U}$ contains the neighborhood filter of $x$. 

Similarly (but without assuming [[axiom of choice|AC]]), 

* $X$ is compact if every filter on $X$ has a convergent refinement. 

This is similar in tone to the characterization given above: 

* $X$ is compact if every net in $X$ has a convergent subnet. 

Assuming the axiom of choice, compactness can also be characterized in terms of universal closure: 

* $X$ is compact iff for any space $Y$, the projection map $X \times Y \to Y$ is closed. 

+--{.query}
I'm not entirely sure that the axiom of choice is needed to prove the last equivalence. It's easy (and classical) that the projection map is closed if $X$ is compact. For the other direction, I know a proof which involves taking $Y$ to be the space of ultrafilters on the underlying set of $Y$, but there may be some other choice(s) for $Y$ which allows one to get around AC. 
=-- 

## Standard Results

* A topological space $X$ is compact if it is a [[compact object]] in its [[category of open subsets]] $Op(X)$.

* Assuming the axiom of choice, the category of compact spaces admits all small limits. See also [[Tychonoff theorem]]. 

* The direct image of a compact subspace under a continuous map is compact. Thus any topological space becomes a [[bornological space]] by taking the bounded sets to be compact subspaces. 

* In the presence of compactness, the following three [[separation axioms]] are equivalent: $T_2$, $T_3$, $T_4$. 

In his book _Stone Spaces_, Johnstone observes that in the localic setting, it is easier to formulate and handle the notion of compact regular [[locale]], rather than say compact Hausdorff locale. 

## Terminology

Some authors choose "compact" to mean "compact Hausdorff" (a much nicer sort of space, and forming a much nicer category of spaces), and use the word "[[quasicompact]]" to refer to just "compact" as we are using it here. This custom seems to be prevalent among algebraic geometers, for example, and particularly so within Francophone schools of algebraic geometry. 

But it is far from clear to me ([[Todd Trimble]]) that "quasicompact" is very well-established outside such circles (despite some arguments in favor of it), and using simply "compact" for the nicer concept therefore carries some risk of creating misunderstanding among mathematicians at large. My own habit at any rate is to say "compact Hausdorff" for the nicer concept, and I will continue using this on the nLab until consensus is reached (if that happens). 
