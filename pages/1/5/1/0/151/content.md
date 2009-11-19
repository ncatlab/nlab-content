From a fundamental category theoretic perspective, there are two fundamental kinds of dualities:

* _abstract duality_: formally nothing but the reversal of arrows in a category $C$, i.e. the passage from $C$ to the [[opposite category]] $C^{op}$;

* _concrete duality_: the oppositely-oriented image of some diagram under a contravariant [[internal hom]] functor $hom(-,V)$.

(See Chapter 7 of Lawvere and Rosebrugh's [Sets for Mathematics](http://www.mta.ca/~rrosebru/setsformath/).)

> Not every statement will be taken into its formal dual by the process of dualizing with respect to $V$, and indeed a large part of the study of mathematics

>>space vs. quantity

> and of logic

>>theory vs. example

>may be considered as the detailed study of the extent to which formal duality and concrete duality into a favorite $V$ correspond or fail to correspond. (p. 122)

#Examples#

* the duality between [[space and quantity]]
* [[Pontryagin duality]]
* [[Stone duality]]
* [[Eckmann-Hilton duality]]

#Definition#

A _duality_ or _[[dual equivalence]]_ is an [[equivalence of categories|equivalence]] between a category $C$ and the abstract dual (i.e. [[opposite category|opposite]]) of a category $D$.

#Remarks#

* Often two categories are not related by a dual equivalence, but just by a [[dual adjunction]]: an [[adjoint functor|adjunction]] between $C^{op}$ and $C$. But every dual adjunction induces a _maximal dual equivalence_ between subcategories of $C$ and $D$, as described below.


#Maximal dualities inside dual adjunctions#

...


#Dualizing objects#

Of particular interest are concrete dualities between concrete categories $C, D$, i.e. categories equipped with a faithful functor 
$f : C \to Set$, $\hat f : D \to Set$
to [[Set]], which are represented by objects $a \in C$, $\hat a \in D$ with the same underlying set $f(a) = \hat f(\hat a)$. Such objects are known as [[dualizing object]]s. 

#References#

* H.-E. Porst, W. Tholen, _Concrete Dualities_ in _Category Theory at Work_, Herrlich, Porst (eds.) ([pdf](http://www.heldermann.de/R&E/RAE18/ctw07.pdf))



#Blog discussion#

* David Corfield: [More on duality](http://golem.ph.utexas.edu/category/2007/01/more_on_duality.html)