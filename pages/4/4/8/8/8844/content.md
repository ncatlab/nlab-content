
#Contents#
* table of contents
{:toc}

## Idea

In [[formal logic]] and [[model theory]], _interpretation_ refers to equipping the [[syntax]] of some [[theory]] with a [[semantics]]. Naiively this means finding a model (in the category of sets) for the theory. This is subsumed by treating interpretations as functors out of [[syntactic categories]].

## Definition

In the language of [[categorical logic]], interpretations are representations of theories inside some category $\mathbf{C}$. Depending on the kind of theory ([[cartesian logic|cartesian]], [[regular logic|regular]], [[coherent logic|coherent]], [[first-order logic|first-order]], [[geometric logic|geometric]]), an interpretation of $T$ in $\mathbf{C}$ is just a ([[cartesian logic|cartesian]], [[regular logic|regular]], [[coherent logic|coherent]], [[first-order logic|first-order]], [[geometric logic|geometric]]) functor to $\mathbf{C}$.

When $\mathbf{C}$ is [[Set]], $T$ is first-order, and the functor (say $M$) is _logical_ (in the sense of Makkai-Reyes, equivalently coherent if we take the [[Morleyization]] of $T$), we get _models_ in the sense usually studied in [[model theory]].

## Interpretations of theories in each other
Let $T_1$ and $T_2$ be ([[cartesian logic|cartesian]], [[regular logic|regular]], [[coherent logic|coherent]], [[first-order logic|first-order]], [[geometric logic|geometric]]) theories. A ([[cartesian logic|cartesian]], [[regular logic|regular]], [[coherent logic|coherent]], [[first-order logic|first-order]], [[geometric logic|geometric]]) _interpretation_ $T_1 \to T_2$ is just a functor between the [[syntactic categories]] $\mathbf{Def}(T_1) \to \mathbf{Def}(T_2)$.

Elsewhere, interpretations have been defined as assignments of symbols in the language $\mathcal{L}_1$ of $T_1$ to definable sets of $T_2$ satisfying various coherence conditions (usually at least product-preserving) which amount to functoriality.

Note that via the duality between taking [[syntactic category|syntactic categories]] and [[internal logic|internal logics]], a model of $T$ in $\mathbf{Set}$ is just an interpretation of $T$ in the theory $\mathsf{Lang}(\mathbf{Set})$.

### Bi-interpretations of theories
We say that $T_1$ and $T_2$ are _bi-interpretable_ if there are functors (of appropriate logical strength) $\mathbf{Def}(T_1) \leftrightarrows \mathbf{Def}(T_2)$ forming an [[equivalence of categories]]. One direction of [[conceptual completeness]] is that bi-interpretable theories have equivalent categories of models. This follows from the fact that ([[cartesian logic|cartesian]], [[regular logic|regular]], [[coherent logic|coherent]], [[first-order logic|first-order]], [[geometric logic|geometric]]) functors are closed under composition, and that equivalent categories induce equivalences of functor categories.


Many notions from [[geometric stability theory]] and [[classification theory]] are invariant under bi-interpretability, e.g. [[stable theory|stability]], [[quantifier elimination]], [[elimination of imaginaries]], etc.

Since bi-interpretations induce equivalences of categories of models, monsters of bi-interpretable first-order theories $T_1, T_2$ will have isomorphic automorphism groups, with the isomorphism induced by restrictions along reducts. This indicates the bi-interpretation extends to the [[imaginaries]] of $T_1$ and $T_2$ also, so that $T_1^{\operatorname{eq}} \simeq T_2^{\operatorname{eq}}$, in fact uniquely---which is the universal property of the [[pretopos completion]].

## Interpretations of models in each other.
This notion has appeared in the model-theoretic literature, and is what some model theorists mean when they say "interpretation." Specialize to first-order logic and models in [[Set]], and fix models $M_1 \models T_1, M_2 \models T_2$. An _interpretation_ of $M_1$ in $M_2$ is a surjection $U \overset{f}{\twoheadrightarrow} M_1$ for $U$ some subset of $M_2^k$, some $k \in \mathbb{N}$, such that the pullback of $f^*X$ of any definable (with parameters) set $X$ of $M_1$ along $f$ is again definable in $Y$. This is enough to induce a logical functor $\mathbf{Def}(T_1) \to \mathbf{Def}(T_2)$ (surjectivity implies witnessed existentials continue to be witnessed, and the functor being induced by pullback implies logicalness), in fact a logical functor $\mathbf{Def}(T_1(M_1)) \to \mathbf{Def}(T_2(M_2))$ of $T_1$ and $T_2$ enriched with the elementary diagrams of $M_1$ and $M_2$.

Facts:

* Every interpretation between theories can be realized as being induced by a concrete interpretation between sufficiently saturated models of those theories.

* Given an $f : U \twoheadrightarrow M_1$, any other $g : U \twoheadrightarrow M_1$ which is also an interpretation $M_1 \to M_2$ is of the form $\sigma \circ f$ for some $\sigma \in \operatorname{Aut}(M_1)$.

## Related entries

* [[formula]]

* [[model theory]], [[structure (model theory)]], 

## References

* wikipedia [interpretation (model theory)](http://en.wikipedia.org/wiki/Interpretation_%28model_theory%29)

* Wilfrid Hodges, _A shorter model theory_, Cambridge Univ. Press 1997 

* Olivia Caramello, _Topos-theoretic preliminaries_.