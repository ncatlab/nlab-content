#Idea#


Pretriangulated dg-categories are models for [[stable (infinity,1)-category|stable (infinity,1)-categories]] in terms of [[differential graded category|dg-categories]], much like [[simplicially enriched category|simplicial categories]] are models for [[(infinity,1)-category|(infinity,1)-categories]].

The cohomology category of a pretriangulated dg-category is an ordinary [[triangulated category]], hence pretrignaulated dg-categories are called [[enhanced triangulated category|enhanced triangulated categories]].


#Definition#

For $E$ 
a [[differential graded category|dg-category]]
let $PreTr(E)$ be its dg-category of [[twisted complex]]es.

$E$ is **pretriangulated** if for every [[twisted complex]] $K \in PreTr(E)$ the corresponding dg-functor

$$
  PreTr(-,K) : E^{op} \to C(Ab)
$$

is [[representable functor|representable]].

(is that right??)

**Proposition**

For $E$ a pretriangulated dg-category, the homotopy category $H^0(E)$ is naturally a [[triangulated category]]. 

The morphism

$$
  H^0(PreTr(E)) \to H^0(E)
$$

is an [[equivalence of categories|equivalence]] of [[triangulated category|triangulated categories]].


#References#

* A. Bondal and M. Kapranov, _Enhanced triangulated categories_ 

See [[enhanced triangulated category]] for more links to references.