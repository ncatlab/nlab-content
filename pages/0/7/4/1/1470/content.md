#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

An **algebraic stack** denotes either a [[Deligne-Mumford stack]] or a more general [[Artin stack]] in the traditional setup of [[algebraic space]]s: they are (Grothendieck) $1$-[[stack|stacks]] of groupoids on the [[etale topology|étale site]] satisfying additional representability conditions.  

#Definition#

An algebraic stack $X$ is required to have an atlas $A\to X$ from an algebraic space (or in a stronger version a [[scheme]]) $A$; the morphisms of the cover are required to be

* surjective representable and &#233;tale (for a [[Deligne-Mumford stack]]);

* surjective representable and smooth (for an [[Artin stack]]).

Here we used the following definition.  A map $f:X\to Y$ of 1-stacks on the &#233;tale site is a *[[representable morphism of stacks]]* if for any scheme $S$ the [[fiber product]] $S\times_Y X$ is a stack associated to a scheme. 

Let $P$ be a property stable under composition and pullback. A representable map $f:X\to Y$ of stacks is said to have a property $P$ if for any scheme $S$ and a morphism of 1-stacks $S\to Y$ the pullback $S\times_Y X\to X$ has property $P$.  


+-- {: .query}

[[Urs Schreiber]]: don't we also need to demand that the diagonal morphism $\Delta : X \to X \times_S X$ is a) [[representable morphism of stacks]], b) separated, c) quasi compact ? 

See for instance def (4.1) in Laumon, Moret/Bailly
Champs alg&#233;briques.
=--


+-- {: .query}

[[Urs Schreiber]]: how precisely am I to think of the relation between [[geometric stack]]s and [[algebraic stack]]s. I am hoping that there is a very general definition of geometric ($\infty$-)stack of which algebraic stacks are a special case, but I am not sure about some technical details.

=--


#Generalizations#

## differentiable and topological stacks ##

Nowdays people talk about [[differentiable stacks]] and [[topological stack]]s, meaning analogues of Deligne--Mumford (DM) or Artin stacks defined in the setup of [[Diff|the category of manifolds]] or some [[convenient category of topological spaces]]. [[orbifold|Orbifolds]] are an example of an Artin stack. For orbifolds stabilizer groups are finite, while for Artin stacks in general they are [[algebraic group]]s. 


## noncommutative spaces ##

A noncommutative generalization for [[Q-category|Q-categories]] instead of [[Grothendieck topology|Grothendieck topologies]], hence applicable in noncommutative geometry of Deligne--Mumford and Artin stacks can be found in

* M. Kontsevich, A. Rosenberg, Noncommutative stacks, preprint MPIM2004-37 [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305) [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333)

#References#

For the topological variant, see [[topological stack]]s and references therein; and for differentiable stacks 

* Kai Behrend, Ping Xu, [Differentiable Stacks and Gerbes](http://front.math.ucdavis.edu/0605.5694)