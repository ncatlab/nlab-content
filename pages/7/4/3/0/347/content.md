#Idea#

Generally, for  $X$ an object we think of as a [[space and quantity|space]], a _cover_ of $X$ is some other object $Y$ together with a morphism $\pi : Y \to X$, usually an [[epimorphism]] demanded to be well behaved in certain way.

The idea is that $Y$ provides a "locally resolved" picture of $X$ in that $X$ and $Y$ are "locally the same" but that $Y$ is "more flexible" than $X$.

The archetypical example are ordinary covers of topological spaces $X$ by open subsets $\{U_i\}$: here $Y$ is their disjoint union $Y := \sqcup_i U_i$.

More generally, you might need a cover to be *family* of maps $(\pi_i: Y_i \to X)_i$; if the category has a [[coproduct]]s that get along well with the covers, then you can replace these families with single maps as above.

# Formalizations #

There are several different but related formalizations of the notion of cover.

* In the context of [[sheaf and topos theory]] a cover is a [[sieve]]. A collection of sieves for all objects in a category equips that category with a [[Grothendieck topology]] and hence makes it a [[site]].

* In the context of [[homotopy theory]] and in particular in the corresponding [[homotopical cohomology theory]] a cover is an [[model category|acyclic fibration]]. In the homotopy theory of simplicial objects this is usually called a [[hypercover]].

