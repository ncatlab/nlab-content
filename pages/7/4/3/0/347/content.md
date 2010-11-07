
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



> under construction

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Generally, for  $X$ an object we think of as a [[space and quantity|space]], a _cover_ of $X$ is some other object $Y$ together with a morphism $\pi : Y \to X$, usually an [[epimorphism]] demanded to be well behaved in certain way.

The idea is that $Y$ provides a "locally resolved" picture of $X$ in that $X$ and $Y$ are "locally the same" but that $Y$ is "more flexible" than $X$.

The archetypical example are ordinary covers of topological spaces $X$ by open subsets $\{U_i\}$: here $Y$ is their [[disjoint union]] $Y := \coprod_i U_i$.

More generally, you might need a cover to be *family* of maps $(\pi_i: Y_i \to X)_i$; if the category has [[coproduct]]s that get along well with the covers, then you can replace these families with single maps as above---see [[superextensive site]].


## Definitions

In the context of [[sheaf and topos theory]] a cover 
on an [[object]] $U$ in a [[category]] $C$ is a collection of [[morphism]]s $\{U_i \to U\}_{i \in I}$.

A specification of a collection of covers for each object of the category, subject to some compatibility condition, makes a [[coverage]] on $C$. If the collection of covers in a coverage is being closed under some operations, the result us called a [[Grothendieck topology]]. Equipped with a coverage/Grothendieck toplogy, the category is called a [[site]]. See there for more details.

Covering families $\{U_i \to U\}$ in $C$ have incarnations as single morphisms in the [[category of presheaves]] $PSh(C)$ over $C$, and these are also sometimes called _covers_ : 

the [[Cech nerve]] of the morphism $\coprod_i U_i \to U$ in $PSh(C)$ is a [[simplicial object]] in $PSh(C)$


$$
  C(\{U_i\})
  = 
  \left(
     \cdots 
   \stackrel{\to}{\stackrel{\to}{\to}} 
   \coprod_{i j} U_i \times_U U_j \stackrel{\to}{\to} \coprod_i U_i
  \right)
  \to 
  U
  \,.
$$

Its [[colimit]] is the [[local epimorphism]] on $U$ that is the incarnation of the covering family in $C$, now in $PSh(C)$.

In [[higher category theory]], when we do not restrict to presheaves, for instance when we use [[simplicial presheaves]], the full Cech nerve itself $C(\{U_i\}) \to U$ is the "local epimorphism", the covering map.

More generally, given a [[coverage]] one can form [[hypercover]]s in the category of simplicial presheaves, by starting with a Cech nerve and then iteratively refining it in each degree further and further by more covers.


...


## Examples

In the category $C$ =[[Top]] of [[topological space]]s or $C$ = [[Diff]] of [[smooth manifold]]s or similar, one has the notions

* [[open cover]] -- for $X \in C$ a space, an _open cover_ is a collection $\{U_i \subset X\}$ of [[open subset]]s, that cover $X$ in the obvious naive sense of the word, i.e. which are such that their union equals $X$;

* [[good cover]] -- a cover $\{U_i \to X\}$ is called a _good cover_ (or _[[good open cover]]_ if in addition it is an open cover) if all of the $U_i$ and all their finite intersections $U_{i_1} \times_X U_{i_2} \times_X \cdots \times_X U_{i_n}$ are [[contractible]] as topological spaces.

  A parameterized version of this is a [[stacked cover]].


There is also the notion of

* [[covering space]]

of a topological space or manifold. This is a priori an independent notion of cover, but for the standard [[Grothendieck topologies]] on [[Top]], [[Diff]], etc. the projection $\{\hat X \to X\}$ from a covering space is a covering family.



[[!redirects covers]]
[[!redirects covering family]]
[[!redirects covering families]]
