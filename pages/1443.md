#Idea#

A _category of local models_ is a category whose objects play the role of particularly well-controled test spaces in the sense of [[space and quantity]]. The major notions of spaces, such as topological spaces, algebraic spaces, smooth manifolds, are spaces modeled on a _category of local models in the sense of [[structured generalized space]]s.

#Definition#

A **category of local models** is

* a small [[site]] $R$;

* a morphism of sites $U : R \to $ [[Top]];

* a set $L$ of [[diagram]]s $I_L \to R$ in $R$

* an object $A$ of $R$

* such that

  * $R$ is closed under [[limit]]s of shape in $L$;

  * $U$ is a _basis for its image_ in that...

  * $A$ generates $R$ under $L$-[[limit]]s and gluing (?).

The objects of $R$ are usually called **affine** spaces.
In particular the object $A$ is the **affine line**.

#Applications#

* For every category of local models there is the corresponding notion of [[locally modeled monoid]]s. See the examples below.


#Examples#

* $R = Rings^{op}$ is the category of local models for algebraic spaces; here $A = \mathbb{Z}[x]$;

* $R =$ [[CartSp]] is the category of local models for smooth manifolds and [[generalized smooth algebra]]s; here $A = \mathbb{R}$.


#References#

section 1.1 of

* David Spivak, _Quasi-smooth derived manifolds_ ([pdf](http://math.berkeley.edu/~dspivak/thesis2.pdf))