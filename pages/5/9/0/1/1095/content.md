<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>


This entry is about the general properties and characterization of [[(∞,1)-categories]] of [[(∞,1)-sheaves]] -- also known as [[∞-stack]] [[(∞,1)-topos]]es.

The 1-categorical analog of the discussion is this entry is at [[category of sheaves]].

#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

For any [[(∞,1)-category]] $C$ every [[(∞,1)-functor]] $\bar {(-)} : C \to D$ which admits a [[(infinity,1)-fully faithful functor|fully faithful]] [[adjoint (infinity,1)-functor|right adjoint]] -- equivalently every [[(∞,1)-functor]] $L : C \to C$ which is 
[[adjoint (infinity,1)-functor|left adjoint]] to the inclusion $L C \hookrightarrow C$ of its [[essential image|essential image]] $L C$ into $C$ -- is a [[localization of an (∞,1)-category]] onto a [[reflective (∞,1)-subcategory]] characterized by the collection $W$ of [[morphisms]] which it sends to [[(infinity,1)-equivalence|equivalences]]. One can think of it 

* as _inverting_ these morphisms;

* as projecting onto those objects of $C$ which are [[local object|local]] with respect to these morphsims: those objects which sees $W$ as a collection of equivalences.

Using the familiar characterization of the [[category of sheaves]] in the 1-categorical context, this straightforwardly suggests to characterize 
_$(\infinity,1)$-categories $Sh(S)$ of $(\infty,1)$-sheaves_ -- also called (Grothendieck-Rezk-Lurie) [[(∞,1)-topoi]] as essential images of [[exact (infinity,1)-functor|left exact]] $(\infty,1)$-functors from [[(infinity,1)-category of (infinity,1)-functors|(∞,1)-categories of (∞,1)-presheaves]]

$$
 \bar{(-)} : PSh(S) \to Sh(S)
$$ 

(called [[∞-stackification]], analogous to [[sheafification]])

that have a 
[[(infinity,1)-fully faithful functor|fully faithful]] [[adjoint (infinity,1)-functor|right adjoint]] [[stuff, structure, property|forgetful]] functor

$$
  Sh(S) \hookrightarrow PSh(S)
  \,.
$$


# Models #


The [[hypercompletion|hypercomplete]] $(\infty,1)$-sheaf toposes are [[presentable (infinity,1)-category|presented]] by the [[model structure on simplicial presheaves]].

Detailed discussion of this [[model category]] presentation is at 

* [[models for infinity-stack (infinity,1)-toposes|models for (infinity,1)-category of (infinity,1)-sheaves]] .

#References#

The study of simplicial presheaves apparently goes back to 

* K. Brown, [Abstract Homotopy Theory and Generalized Sheaf Cohomology](http://ncatlab.org/nlab/show/BrownAHT)

which considers locally [[Kan complex|Kan]] [[simplicial presheaf|simplicial presheaves]] as a [[category of fibrant objects]].

This was later conceived in terms of a [[model structure on simplicial presheaves]] and on simplicial sheaves by Jocal and Jardine. To&#235; summarizes the situation and emphasizes the interpretation in terms of [[∞-stacks]] living in $(\infty,1)$-categories for instance in

B. To&euml;n, _Higher and derived stacks: a global overview_   ([arXiv](http://arxiv.org/abs/math/0604504)) .

The full picture in terms of Grothendieck-$(\infty,1)$-topoi of $(\infty,1)$-sheaves is the topic of

J. Lurie, [[Higher Topos Theory]].

* localization $(\infty,1)$-functors ($(\infty,1)$-sheafification for the present purpose) are discussed in section 5.2.7;

* local objects ($(\infty,1)$-sheaves for the present purpose) and [[local isomorphism]]s are discussed in section 5.5.4;

* the definition of $(\infty,1)$-topoi of $(\infty,1)$-sheaves is then definition 6.1.0.4 in section 6.1;

* the characterization of $(\infty,1)$-sheaves in terms of [[descent|descent and codescent]] is in section 6.1.3 

* the relation between the [[model structure on simplicial presheaves|Brown--Joyal--Jardine model]] and the general story is discussed at length in section 6.5.4

[[!redirects (∞,1)-category of (∞,1)-sheaves]]
