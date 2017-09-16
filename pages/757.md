#Idea#

To the extent that a [[model category]] is a [[presentable (infinity,1)-category|presentation]] of an [[(infinity,1)-category]], the [[localization]] of a model category is a presentation for the [[localization of an (infinity,1)-category]].

See also [[localization of a simplicial model category]].

#Definition in model categories#

Let $C$ be a category equipped with a [[model category]] structure and let $S$ be a class of morphisms in $C$. 

The **left Bousfield localization** of $C$ with respect to $S$ is, if it exists, a [[model category]] structure $L_S C$ on $C$ such that

* the class of weak equivalenced of $L_S C$ equals the class of $S$-[[local equivalence]]s of $C$;

* the class of cofibrations of $L_S C$ equals that of $C$;

* the fibrations of $L_S C$ are precisely the morphisms with the right lifting property with respect to the $S$-[[local cofibration]]s of $C$.

Analogously the **right Bousfield localization** is defined as above, with the role of fibrations and cofibrations exchanged throughout.

#Bousfield localization in triangulated categories#

In the setup of [[triangulated category|triangulated categories]], the Bousfield localization is defined as follows. A *triangulated subcategory* $A$ of a triangulated category $B$ is a nonempty subcategory closed under suspension of objects and such that for all objects $X,Y$ in $A$ if $X\to Y\to Z\to X[1]$ is a distinguished triangle in $B$, then $Z$ is in $A$.  In that case one can define the [[Verdier quotient]] category $B/A$ which is a triangulated category equipped with a canonical functor $Q^*:B\to B/A$ which is also triangulated (additive and preserving distinguished triangles) and universal among all triangulated functors $B\to D$ which send objects of $A$ to objects isomorphic to $0$. A triangulated subcategory $A$ is *thick* if with any object in $A$ it contains all its direct summands in $B$.

In that case, the Verdier quotient $B/A$  has the property that the only objects whose images in $B/A$ are isomorphic to zero are the objects from $A$. Given a thick subcategory $A\subset B$, we say that the **Bousfield localization** exists if the Verdier quotient functor $Q^*$ has a right adjoint functor $Q_*$ which is then (automatically) triangulated and fully faithful. 

#References#

Bousfield localization appears as definition 3.3.1 in

* Hirschhorn, _Model categories and their localization_ 