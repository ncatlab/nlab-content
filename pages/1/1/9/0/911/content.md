#Idea#

For a functor $F : C \to Set$, we may think of $Set$ as the [[classifying space]] of "[[Set]]-bundles;" see [[generalized universal bundle]].  The category of elements of $F$ is, in this sense, the [[Set]]-bundle classified by $F$.  It comes equipped with a projection to $C$ which is a [[Grothendieck fibration|discrete fibration]], and provides an equivalence between presheaves and discrete fibrations.

Forming a category of elements can be thought of as "unpacking" a [[concrete category]]. For example, consider a concrete category $C$ consisting of two objects $X,Y$ and two non-trivial morphisms $f,g$

<img src="http://ncatlab.org/nlab/files/explode.jpg" width = "275"/>

The individual elements of $X,Y$ are "unpacked" and become objects of the new category. The "unpacked" morphisms are inherited in the obvious way from morphisms of $C$.

Note that an "unpacked" category of elements can be "repackaged".

<img src="http://ncatlab.org/nlab/files/implode.jpg" width = "275"/>

The analogue of the category of elements for functors landing in $Cat$, rather than $Set$, is called the [[Grothendieck construction]].


#Definition#

Given a functor $P:C\to\mathbf{Set}$, the **category of elements** $el(P)$ or $El_P(C)$ (or obvious variations) may be understood in any of these equivalent ways:

* It is the [[category]] whose objects are pairs $(c,x)$ where $c$ is an object in $C$ and $x$ is an element in $P(c)$ and morphisms $(c,x)\to(c',x')$ are morphisms $u:c\to c'$ such that $P(u)(x) = x'$.

* It is the [[pullback]] along $P$ of the [[generalized universal bundle|universal Set-bundle]] $U : Set_* \to Set$
$$\array{ El_P(C) &\to& Set_* \\ \downarrow^{\pi_P} && \downarrow^U \\ C &\to& Set}\,,$$
where $U$ is the [[forgetful functor]] from [[pointed set|pointed sets]] to sets.

* It is the [[comma category]] $(*/P)$, where $*$ is the inclusion of the one-point set $*:*\to Set$ and $P:C\to Set$ is itself:
$$\array{ El_P(C) &\to& * \\ \downarrow^{\pi_P} &\Downarrow& \downarrow^{pt} \\ C &\to& Set.}$$

* Its [[opposite category|opposite]] is the [[comma category]] $(Y/P)$, where $Y$ is the [[Yoneda embedding]] $C^{op}\to [C,Set]$ and $P$ is the functor $*\to [C,Set]$ which picks out $P$ itself:
$$\array{ El_P(C)^{op} &\overset{\pi_P^{op}}{\to}& C^{op} \\ \downarrow &\Downarrow& \downarrow^{Y} \\ * & \underset{P}{\to}& [C,Set].}$$

$El_P(C)$ is also often written with [[end|coend]] notation as $\int^C P$, $\int^{c: C} P(c)$, or $\int^c P(c)$.  This suggests the fact the set of objects of the category of elements is the [[disjoint union]] (sum) of all of the sets $P(c)$.

When $C$ is a [[concrete category]] and the functor $F:C\to Set$ is simply the [[forgetful functor]], we can define a functor

$$Explode(-) := El_F(-).$$

This is intended to illustrate the concept that constructing a category of elements is like "unpacking" or "exploding" a category into its elements.

#Properties#

* The category of elements is naturally equipped with a _projection functor_ $\pi_P:El_P(C) \to C$ given by $(c,x)\mapsto c$ and $u\mapsto u$.  This projection is a [[Grothendieck fibration|discrete opfibration]] and can be viewed also as a $C$-indexed family of sets.

##Example: Action Groupoid##

Given a vector space $V$, a group $G$, and a [[representation]] 

$$\rho:\mathbf{BG}\to Vect,$$

denote the image of $\rho$ by

$$V\nearrow G.$$

The [[action groupoid]] $V//G$ is then given by

$$V//G=Explode(V\nearrow G).$$

##References##

* [Wikipedia: Category of elements](http://en.wikipedia.org/wiki/Category_of_elements)
* [An Exercise in Groupoidification: The Path Integral](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html)
  * [Exploding a Category](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017574)
  * [Library of Loops](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017584)

##Discussion##

[[Eric Forgy|Eric]]: This seems like the gadget I'm trying to describe at [[Exploding a Category]] (I may remove that material once I understand what's going on). I understand the concept (I think!), but why the notation $\int_C P$?

_Toby_:  That notation is a reference to the standard notation for an [[end]].

[[Urs Schreiber|Urs]]: I'd say the integral sign here originates quite concretely in the idea that the category of elements of $F$ is the _union_ of all the elements of $P(c)$ for all $c$. 

[[Eric Forgy|Eric]]: I think this concept is important (for me anyway) and the intergal notation is cumbersome. What would be an acceptable alternative? For now, I think I will borrow from [[category of generalized elements]] and [Wikipedia](http://en.wikipedia.org/wiki/Category_of_elements) and denote it $El(P)$. I can change it back if there is an uproar. I would actually prefer something like $Unpack(C)$ to emphasize the relation to $C$.

PS: Don't worry. I will make the edits once a nice notation is decided.

_Toby_:  I don\'t really like $Unpack$, although $El$ seems fine.  I do think that we should show the integral notation too, however, and give Urs\'s justification for it.  (I\'ll do that now.)

_Eric_: Excellent. Instead of $El$ (and forget about $Unpack$), could we call it $Element(P,C)$ or even $El_P(C)$ and let $P:C\to Set$? From what I can tell about [[Grothendieck construction]], this would be more consistent. Lurie uses the notation $Groth(P,C)$ for $P:C\to Cat$ so $El_P(C)$ with $P:C\to Set$ makes sense to me.

>_Toby_:  Strictly speaking, $C$ is redundant, which is why people leave it out.  I\'m fine with having it in there, but I moved the very common $el(P)$ higher up.  I also dislike long words in mathematical notation, but '$Elem$' is OK by me.

[[Mike Shulman|Mike]]: $el(P)$ is a fairly common notation.

[[Eric Forgy|Eric]]: Should the above statement be changed from disjoint union to direct product? - Eric

[[Mike Shulman|Mike]]: No.  Each object of $el(P)$ is an element of exactly one $P(c)$, so the set of objects is the disjoint union.  An element of the direct product would consist of an element of $P(c)$ for _every_ $c$.

>_Toby_:  Even as a coend, it\'s still like an integral: a sum.

[[Eric Forgy|Eric]]: Thanks. I hope my changes are acceptable. I'm pretty happy with the article now. I also added a note about $el(P)$.

[[!redirects Exploding a Category]]