#Idea#

The notion of quasi-category is a [[geometric definition of higher category]] which relaxes the [[Kan complex|Kan condition]] on a simplicial set.


#Definition#


A quasi-category is a [[simplicial set]] in which all _inner_ [[horn]]s have fillers. This means that the lifting condition given at [[Kan complex]] is imposed only for horns $\Lambda^i[n]$ with $0 \lt i \lt n$.



#Remarks#

* Compare with the definition of a [[Kan complex]] in which _all_ horns are required to have fillers: a quasi-category is a structure slightly weaker than a Kan complex. Indeed, while we can think of a Kan complex as an $\infty$-[[infinity-groupoid]] (that is an $(\infty,0)$-category), in which _all_ morphisms are [[equivalence]]s, a quasi-category is a model for an $(\infty,1)$-[[(infinity,1)-category|category]], in which only all $n$-morphisms for $n \geq 2$ are required to be [[equivalence]]s.  

* As the quasi-category condition is a weakening of the Kan complex condition, they have also been called **weak Kan complexes** and the corresponding condition, the **weak Kan condition**.

* The [[nerve]] of a category is always a quasi-category, while the nerve of a category is a Kan complex iff the category is a groupoid.  In this sense quasi-categories are a "minimal common generalization" of Kan complexes and nerves of categories.

# Constructions in quasi-categories #

The point of quasi-categories is that they are supposed to provide a fully [[homotopy theory|homotopy-theoretic]] refinement of the ordinary notion of [[category]]. In particular, all the familiar constructions of category theory have natural analogs in the context of quasi-categories. See for instance

* [[limit in quasi-categories]]

* [[over-category in quasi-categories]]

* [[initial object in quasi-categories]]


#References#

Quasi-categories have originally been defined in

* J.M. Boardman and R.M. Vogt, _Homotopy invariant algebraic structures on topological
spaces_, Lecture Notes in Mathematics, Vol. 347. Springer-Verlag, 1973._

They occured as  weak Kan complexes in 

* R. Vogt, _Homotopy limits and colimits_, Math. Z., 134, (1973), 11&#8211;52.

Vogt's main theorem involved a category of homotopy coherent diagrams defined on a topologically enriched category and showed it was equivalent to a quotient category of the category of (commutative) diagrams on the same category. 


Cordier in

* J.-M. Cordier, _Sur la notion de diagramme homotopiquement coh&#233;rent_, Cahiers de Top. 
G&#233;om. Diff., 23, (1982), 93 &#8211;112,

defined a homotopy coherent nerve of any [[simplicially enriched category]], which generalised the [[nerve]] of an ordinary category. In 

* J.-M. Cordier and T. Porter, _Vogt's theorem on categories of homotopy coherent diagrams_, 
Math. Proc. Cambridge Philos. Soc., 100, (1986), 65&#8211;90, 

it was shown that this homotopy coherent nerve was a quasi-category if the simplicial enrichment was by Kan complexes.
 
Their importance as a basis for [[category theory]] has been emphasized in the work by Joyal

* A. Joyal, _Quasi-categories and Kan complexes_, J. Pure Appl. Algebra, 175 (2002), 207-222.

* A. Joyal, _Simplicial categories vs quasi-categories_, in preparation.

Jacob Lurie developed the theory of quasi-categories in

* Jacob Lurie, _Higher Topos Theory_ ([arXiv](http://arxiv.org/abs/math/0608040))

in order to discuss [[infinity-stack]]s.
