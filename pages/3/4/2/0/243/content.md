<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


#Idea#

An _end_ is a special kind of [[limit]] over a [[functor]] of the form $F : C^{op} \times C \to D$ (sometimes called a _bifunctor_).

If we think of such a functor in the sense of [[distributors]] as encoding a left and right [[action]] on the object

$$
  \prod_{c \in C} F(c,c)
$$

then the _end_ of the functor picks out the universal [[subobject]] on which the left and right action coincides.

A classical example of an _end_ is the $V$-object of [[natural transformations]] between $V$-[[enriched functors]] in [[enriched category theory]]. 

#In ordinary category theory#

In ordinary [[category theory]], given a [[functor]] $F: C^{op} \times C \to X$, an __end__ of $F$ in $X$ is an object $e$ of $X$ equipped with a [[universal construction|universal]] [[dinatural transformation]] from $e$ to $F$. This means that given any dinatural transformation from an object $x$ of $X$ to $F$, there exists a unique map $x \to e$ which respects the dinatural transformations. 

In more detail: the end of $F$ is traditionally denoted $\int_{c: C} F(c, c)$, and the components of the universal dinatural transformation, 
$$\pi_c: \int_{c: C} F(c, c) \to F(c, c)$$ 
are called the _projection maps_ of the end. Then, given any dinatural transformation with components 
$$\theta_c: x \to F(c, c),$$ 
there exists a unique map $f: x \to e$ such that 
$$\theta_c = \pi_c f$$ 
for every object $c$ of $C$.

The notion of __coend__ is dual to the notion of end, written $\int^{c: C} F(c, c)$. 

## Examples: Module homs and module tensor products

Perhaps the most common way in which ends and coends arise is through homs and tensor products of (generalized) modules, and their close cousins, weighted limits and weighted colimits. These concepts are fundamental in enriched category theory. 



# In enriched category theory #

There is a definition of _end_ in [[enriched category theory]], as follows. 

## End of $V$-valued functors ##

Let $V$ be a [[symmetric monoidal category]], let $C$ be a $V$-[[enriched category]], and let $F: C^{op} \otimes C \to V$ be a $V$-[[enriched functor]]. 

Then in particular there is a covariant [[action]] of $C$ on $F$, with components
$$\lambda_{c, d, e}: F(c, d) \otimes C(d, e) \to F(c, e),$$
[where $C(d, e)$ is customary notation for the enriched hom $\hom_C(d, e)$ of $C$ in $V$], and a contravariant action of $C$ on $F$, with components
$$\rho_{c, d, e}: F(d, e) \otimes C(c, d) \to F(c, e).$$ 

In detail, the covariant action is the [[adjunct]] of the morphism 

$$(F(c,-) : C(d,e) \to [F(c,d), F(c,e)]) \in Hom_V(C(d,e),[F(c,d), F(c,e)])
$$ 

under the [[closed monoidal category|Hom-adjunction]] 

$$
Hom_V(C(d,e),[F(c,d), F(c,e)]) \stackrel{\simeq}{\to} Hom_V(C(d,e)\otimes F(c,d),F(c,e))
$$ 

in $V$. Similarly for the contravariant action.



A $V$- **dinatural transformation**
$$\theta: v \stackrel{\bullet}{\to} F$$ 
from $v$ to $F$ consists of a family of arrows in $V$, 
$$\theta_c: v \to F(c, c),$$ 
indexed over objects $c$ of $C$, such that for every pair of objects $(c, d)$ in $V$, the composites of (1) and (2) agree: 
$$v \otimes C(c, d) \stackrel{\theta_c \otimes 1}{\to} F(c, c) \otimes C(c, d) \stackrel{\lambda_{c, c, d}}{\to} F(c, d) \qquad (1)$$ 
$$v \otimes C(c, d) \stackrel{\theta_d \otimes 1}{\to} F(d, d) \otimes C(c, d) \stackrel{\rho_{c, d, d}}{\to} F(c, d) \qquad (2)$$

A $V$-enriched **end** of $F$ is an object $\int_{c: C} F(c, c)$ of $V$ equipped with a $V$-dinatural transformation 
$$\pi: \int_{c: C} F(c, c) \stackrel{\bullet}{\to} F$$ 
such any $V$-dinatural transformation $\theta$ from $v$ to $F$ is obtained by pulling back the components of $\pi$ along $f: v \to \int_{c: C} F(c, c)$, for some unique map $f$. That is,
$$\theta_c = \pi_c f$$ 
for all objects $c$ of $C$. 


## End of $C$-valued functors for $C \in V\Cat$ ##

If $X$ is any $V$-enriched category and $F: C^{op} \otimes C \to X$ is a $V$-enriched functor, then the **end** of $F$ in $X$ is an object $\int_{c: C} F(c, c)$ of $X$ equipped with an $Ob(C)$-indexed family of arrows 
$$\pi_c: I \to X(\int_{c: C} F(c, c), F(c, c))$$ 
in $V$, such that for every object $x$ of $X$, the family 
of maps 
$$X(x, \pi_c): X(x, \int_{c: C} F(c, c)) \to X(x, F(c, c))$$ 
are the projection maps realizing $X(x, \int_{c: C} F(c, c))$ as the corresponding end in $V$. This is an example of the general notion of [[weighted limit]] in enriched category theory. 


## End as an equalizer ##

### ordinary ends as equalizers ###

Now we motivate and define the _end_ in [[enriched category theory]] in terms of [[equalizers]].

Recall from the discussion at the end of [[limit]] that the [[limit]] over an (ordinary, i.e. not enriched) [[functor]]

$$
  F : C^{op} \to Set
$$

is given by the [[equalizer]] of 

$$
  \prod_{c \in Obj(C)}
  F(c)
  \stackrel{\prod_{f \in Mor(c)} (F(f) \circ p_{t(f)}) }{\to}  
  \prod_{f \in Mor(C)}
  F(s(f))
$$

and

$$
  \prod_{c \in Obj(C)}
  F(c)
  \stackrel{\prod_{f \in Mor(c)} (p_{s(f)}) }{\to}  
  \prod_{f \in Mor(C)}
  F(s(f))  
  \,.
$$

If we want to generalize an expression like this to [[enriched category theory]] the explicit indexing over the set of morphisms has to be replaced by something that makes sense in an [[enriched category]]. 

To that end, observe that we have a canonical isomorphism (of sets, still)

$$
  \prod_{{(c_1 \stackrel{f}{\to} c_2)} \in Mor(C)} F(c_1)
  \simeq
  \prod_{c_1,c_2 \in Obj(C)} F(c_1)^{C(c_1,c_2)}
  \,.
$$

If we write for the [[hom-set]] instead

$$
 [C(c_1,c_2), F(c_1)] := F(c_1)^{C(c_1,c_2)}
$$ 

with $[-,-]$ the [[internal hom]] in [[Set]], then the expression starts to make sense in any $V$-[[enriched category]].

Still equivalently but suggestively rewriting the above, we now obtain the limit over $F$ as the [[equalizer]] of

$$
  \prod_{c \in Obj(C)}
  F(c)
  \stackrel{\stackrel{\rho}{\to}}{\stackrel{\lambda}{\to}}  
  \prod_{c_1,c_2 \in Obj(C)}
  [C(c_1,c_2),F(c_1)]
  \,,
$$

where in components

$$
  \rho_{c_1, c_2} : F(c_1) \to [C(c_1,c_2), F(c_1)]
$$

is the [[adjunct]] of

$$
  C(c_1, c_2) \to * \to [F(c_1), F(c_1)]
$$

(with the last map the [[adjunct]] of $Id_{F(c_1)}$) and where 

$$
  \lambda_{c_1, c_2} : F(c_2) \to [C(c_1,c_2), F(c_1)]
$$

is the [[adjunct]] of

$$
  F_{c_1, c_2} : C(c_1, c_2) \to [F(c_2), F(c_1)]
  \,.
$$

So for definiteness, the equalizer we are looking at is that of 

$$
  \rho := \prod_{c_1, c_2 \in C} \rho_{c_1,c_2}\circ pr_{F(c_1)}
$$

and

$$
  \lambda := \prod_{c_1, c_2 \in C} \lambda_{c_1,c_2}\circ pr_{F(c_2)}
$$

This way of writing the [[limit]] clearly suggests that it is more natural to have $\lambda$ and $\rho$ on equal footing. That leads to the following definition.


### enriched ends over $V$-valued functors as equalizers ###

For $V$ a [[symmetric monoidal category]], $C$ a $V$-[[enriched category]] and 
$F : C^{op} \times C \to V$ a 
$V$-[[enriched functor]],
the **end** of $F$ is the [[equalizer]]

$$
  \int_{c \in C}
  F(c,c)
  \to 
  \prod_{c \in Obj(C)}
  F(c)
  \stackrel{\stackrel{\rho}{\to}}{\stackrel{\lambda}{\to}}  
  \prod_{c_1,c_2 \in Obj(C)}
  [C(c_1,c_2),F(c_1,c_2)]
$$

with $\rho$ in components given by

$$
  \rho_{c_1, c_2} : F(c_1,c_1) \to [C(c_1,c_2), F(c_1,c_2)]
$$

being the [[adjunct]] of

$$
  F(c_1,-) : C(c_1, c_2) \to [F(c_1,c_1), F(c_1,c_2)]
$$

and

$$
  \lambda_{c_1, c_2} : F(c_2,c_2) \to [C(c_1,c_2), F(c_1,c_2)]
$$

being the [[adjunct]] of

$$
  F(-,c_2) : C(c_1, c_2) \to [F(c_2,c_2), F(c_1,c_2)]
  \,.
$$


This definition manifestly exhibits the **end as the equalizer of the left and right action** encoded by the [[distributor]] $F$.

## End as a weighted limit ##

The end for $V$-functors with values in $V$ serves, among other things, to define [[weighted limits]], and weighted limits in turn define ends of bifunctors with values in more general $V$-categories.

For $C$ and $D$ both $V$-categories and $F : C^\op \times C \to D$ an $V$-[[enriched functor]], the **end** of $F$ is the [[weighted limit]]

$$
  \int_{c \in C} F(c,c)
  :=
  lim^{Hom_C} F
  \,,
$$

where the right hand denotes the [[weighted limit]] over $F$ with weight $Hom_C : C^{op} \times C \to V$.

#Examples#

## enriched functor categories ##

For $C$ and $D$ both $V$-[[enriched category|enriched categories]], the $V$-[[enriched functor category]] $[C,D]$ is the $V$-[[enriched category]] whose

* objects are $V$-[[enriched functors]] $F : C \to D$;

* [[hom-objects]] in $V$ are given by the end-formula $[C,D](F,G) := \int_{c \in C} D(F(c), G(c))$.

For $V = Set$ this reproduces of course the ordinary [[functor category]].



#References#

in 

* M. Kelly, _Basic concepts in enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

  * ends of $V$-valued bifunctors are discussed in section 2.1

  * the enriched functor category that they give rise to is discussed in section 2.2;

  * enriched [[weighted limits]] in terms of enriched functor categories are in section 3.1

  * the end of general $V$-enriched functors in terms of weighted limits is in section 3.10 .

[[!redirects ends]]
[[!redirects coend]]
[[!redirects coends]]