**Under Construction**

Given a [[concrete category]] $C$, we can **explode** $C$ into a new category $Explode(C)$. The objects of $Explode(C)$ consist of all the elements of all the objects of $C$.

The morphisms of $Explode(C)$ are the obvious ones inherited from the morphisms of $C$, i.e. given a morphism


$$X\stackrel{f}{\to} Y$$


in $C$, we have the obvious morphism


$$(x\in X)\stackrel{f_x}{\to} (y\in Y)$$


in $Explode(C)$.

##Example: Action Groupoid##

Given a vector space $V$, a group $G$, and a [[representation]] 

$$\rho:\mathbf{BG}\to Vect,$$

denote the image of $\rho$ by

$$V\nearrow G.$$

This has a nice pictorial depiction via

$$V\bullet\righttoleftarrow G.$$

The [[action groupoid]] $V//G$ is then given by

$$V//G=Explode(V\nearrow G).$$

##Example: Path Category##

+--{.query}

>[[Urs Schreiber|Urs]]: I am not sure what is meant with the following example!

=--

Consider a category $X\nearrow\Gamma$ with one object, a set $X$, and one morphism

$\Gamma:X\to X$

for each "evolution map" in $X$. This category may be depicted as

$$X\bullet\righttoleftarrow\Gamma.$$

The [[path category]] $P_1(X)$ is given by

$$P_1(X)=Explode(X\nearrow\Gamma).$$

##References##

* [Exploding a Category](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017574)

##Discussion##

>[[Urs Schreiber|Urs]]: the following really describes this concept: given a category $C$ with a [[generator]] ${*}$ or some other singled out object such as a tensor unit if $C$ is monoidal, there is the category of [[generalized element]]s of $C$ with respect to ${*}$, which is the [[over category]] $(*/C)$. The term "exploding a category" is very non-standard and I don't really like it, to be frank. Could we move this here maybe to something like "category of elements", or the like? 

>[[Eric Forgy|Eric]]: It does no harm to keep this here. I'm not sure why you don't like it so much. I spent a lot of time trying to understand this and I think others (maybe non-mathematicians) would be served to see this concept explained on a low brow level. The picture **is** that of a category being "exploded" into pieces, so I think the term is accurately descriptive. Once again, it does no harm to keep this here. A pointer to [[category of generalized elements]] for the high brow version should suffice I think.