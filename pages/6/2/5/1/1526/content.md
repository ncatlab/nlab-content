>[[Urs Schreiber|Urs]]: the following really describes this concept: given a category $C$ with a [[generator]] ${*}$ or some other singled out object such as a tensor unit if $C$ is monoidal, there is the category of [[generalized element]]s of $C$ with respect to ${*}$, which is the [[over category]] $(*/C)$. The term "exploding a category" is very non-standard and I don't really like it, to be frank. Could we move this here maybe to something like "category of elements", or the like? 


Given a [[category]] $C$, it is often the case that each object $X$ itself contains many elements $x\in X$.

**Exploding a category** $C$ results in a new category $Explode(C)$. The objects of $Explode(C)$ consist of all the elements of all the objects of $C$.

The morphisms of $Explode(C)$ are the obvious ones inherited from the morphisms of $C$, i.e. given a morphism


$$X\stackrel{f}{\to} Y$$


in $C$, we have the obvious morphism


$$(x\in X)\stackrel{f}{\to} (y\in Y)$$


in $Explode(C)$.

##Example: Action Groupoid##

Given a vector space $V$, a group $G$, and a representation $\rho$, define a category

$$V\nearrow G.$$

There is one object $V$ in $V\nearrow G$ and one morphism 

$$g:V\to V$$ 

for each element in $G$. This has a nice pictorial depiction via

$$V\bullet\righttoleftarrow G.$$

The [[action groupoid]] $V//G$ is then given by

$$V//G=Explode(V\nearrow G).$$

##Example: Path Category##

Consider a category $X\nearrow\Gamma$ with one object, a set $X$, and one morphism

$\Gamma:X\to X$

for each "evolution map" in $X$. This category may be depicted as

$$X\bullet\righttoleftarrow\Gamma.$$

The [[path category]] $P_1(X)$ is given by

$$P_1(X)=Explode(X\nearrow\Gamma).$$

##References##

* [Exploding a Category](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017574)