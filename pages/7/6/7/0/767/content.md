
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Often [[sites]] are required to be [[small category|small categories]] ([[small sites]]).  If not, if one has a _large site_,  there are complications.


Many of the good properties of [[sheaf|sheaves]] depend on such smallness.  To begin with, even the category of sheaves may have to be [[very large category|extra-large]], but there are other issues, such as:

* the existence of [[sheafification]],
* the existence of [[colimit|colimits]] in the category of sheaves,
* [[cartesian closed category|cartesian closedness]] of the category of sheaves, and
* the category of sheaves being a [[topos]].

However, for many purposes it is desirable to consider the notion of [[sheaves]] on large sites.  

## Small (dense) sub-sites

In some cases, sheaves on a large site can be identified with sheaves on some small full sub-site, for instance a [[dense sub-site]].  
A large site with a small dense sub-site is called an [[essentially small site]].

For example, if $C$ is a [[Grothendieck topos]] with its [[subcanonical coverage|canonical coverage]], then every sheaf on $C$ is representable, so $C\simeq Sh(C)$; thus $Sh(C)$ is equivalent to the category of sheaves on some small site (a defining site for $C$ itself).

## Sheaves on a large site

On the other hand, one sometimes wants to consider sheaves on [[large category|large categories]] such as [[Top]] or [[Diff]], which are certainly not Grothendieck toposes.  One way to deal with this is to consider [[full subcategory|full subcategories]] of these large categories on objects whose size is bounded by some large (in the non-technical sense) [[cardinal number]] $\kappa$.  In an extreme case, $\kappa$ could be an [[inaccessible cardinal]].  The idea is that for sheaves and in particular for any [[homotopy theory]] of sheaves the choice of these cardinality bounds is "inessential."

See for instance [p. 2](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=2) of Jardine, [Fields Lectures: Simplicial presheaves](https://www.math.uwo.ca/faculty/jardine/courses/fields/fields-01.pdf) where this issue arises in the study of [[simplicial presheaf|simplicial presheaves]] and the [[model structure on simplicial presheaves]].

[[!redirects large sheaf]]
[[!redirects sheaves on large sites]]

[[!redirects large site]]