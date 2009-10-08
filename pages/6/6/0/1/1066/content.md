<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>

#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

The [[homotopy category]] of an [[(infinity,1)-category]] $C$ is, roughly, the best [[category|1-categorical]] approximation to $C$.  It has the same objects as $C$, and its morphisms are [[equivalence]] classes of 1-morphisms in $C$.


#Definition#

The details of the definition depend on the chosen model for $(\infty,1)$-categories, as either

* [[simplicially enriched category]]/ Top-category

* [[complete Segal space]]

* [[Segal category]]

* [[quasi-category]]

##For simplicially enriched categories##

The **homotopy category** $h C$ of a [[SimpSet|SSet]]-[[enriched category]] $C$ (equivalently of a [[Top]]-[[enriched category]]) is hom-wise the image under the functor
$$
  \Pi_0 : SSet \to Set
 \,,
$$
which sends each [[simplicial set]] to its [[set]]
of connected components, i.e. to the set of [[path component]]s:

$$
  Hom_{h C}(A,B) := \pi_0(Hom_C(A,B))
  \,.
$$

+-- {: .query}
 
  [[Urs Schreiber|Urs]]: something is missing here: the homotopy category of an $(\infty,1)$-category is supposed to be enriched in $Ho_{Top}$, I think

=--


## For complete Segal spaces and Segal categories ##

Similar, but more complicated, definitions work for [[complete Segal space]]s and [[Segal category|Segal categories]].


##For quasi-categories ##

For [[quasi-category|quasi-categories]], one can write down a definition similar to those of $SSet$-enriched categories, but there is also the following direct construction: 

the [[nerve|simplicial nerve]] functor $N :$ [[Cat]] $\to$ [[SimpSet|SSet]] has a [[adjoint functor|left adjoint]]
$$
 h : SSet \to Cat
 \,.
$$
and the homotopy category of a quasi-category $C$ (a [[simplicial set]] with extra [[stuff, structure, property|properties]]) is its image $h C$ under this functor.


#References#

[Section 1.2.3, p. 33](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=33) of

* [[Jacob Lurie]], [[Higher Topos Theory]]


[[!redirects homotopy category of an (∞,1)-category]]
