#Idea#

For $F : C^{op} \to Set$ a [[presheaf]], we may think of $Set$ as the [[classifying space]] of "[[Set]]-bundles;" see [[generalized universal bundle]].  The category of elements of $F$ is, in this sense, the [[Set]]-bundle classified by $F$.  It comes equipped with a projection to $C$ which is a [[Grothendieck fibration|discrete fibration]], and provides an equivalence between presheaves and discrete fibrations.

Forming a category of elements can be thought of as "unpacking" a [[concrete category]]. For example, consider a concrete category $C$ consisting of two objects $X,Y$ and two non-trivial morphisms $f,g$

[[explode.jpg|Exploding a Category:pic]]

The individual elements of $X,Y$ are "unpacked" and become objects of the new category. The "unpacked" morphisms are inherited in the obvious way from morphisms of $C$.

The analogue of the category of elements for functors landing in $Cat$, rather than $Set$, is called the [[Grothendieck construction]].


#Definition#

Given a functor $P:C^{\mathrm{op}}\to\mathbf{Set}$ (a [[presheaf]] of sets on $C$), the **category of elements** $El(P)$ may be understood in any of these equivalent ways:

* It is the [[category]] whose objects are pairs $(c,x)$ where $c$ is an object in $C$ and $x$ is an element in $P(c)$ and morphisms $(c,x)\to(c',x')$ are morphisms $u:c\to c'$ such that $P(u)(x') = x$.

* It is the [[comma category]] $(Y/P)$, where $Y$ is the [[Yoneda embedding]] $C\to [C^{op},Set]$ and $P$ is the functor $*\to [C^{op},Set]$ which picks out $P$ itself:
$$\array{ El(P) &\overset{\pi_P}{\to}& C \\ \downarrow &\Downarrow& \downarrow^{Y} \\ * & \underset{P}{\to}& [C^{op},Set].}$$

* Its [[opposite category|opposite]] is the [[pullback]] along $F$ of the [[generalized universal bundle|universal Set-bundle]] $U : Set_* \to Set$
$$\array{ El(P)^{op} &\to& Set_* \\ \downarrow^{\pi_P^{op}} && \downarrow^U \\ C^{op} &\to& Set}\,,$$
where $U$ is the [[forgetful functor]] from [[pointed set]]s to sets.

* Its opposite is the [[comma category]] $(*/P)$, where $*$ is the inclusion of the one-point set $*:*\to Set$ and $P:C^{op}\to Set$ is itself:
$$\array{ El(P)^{op} &\to& * \\ \downarrow^{\pi_P^{op}} &\Downarrow& \downarrow^{pt} \\ C^{op} &\to& Set.}$$


#Properties#

* The category of elements is naturally equipped with a _projection functor_ $\pi_P:El(P) \to C$ given by $(c,x)\mapsto c$ and $u\mapsto u$.  This projection is a [[Grothendieck fibration|discrete fibration]] and can be viewed also as a $C$-indexed family of sets.

##Example: Action Groupoid##

Given a vector space $V$, a group $G$, and a [[representation]] 

$$\rho:\mathbf{BG}\to Vect,$$

denote the image of $\rho$ by

$$V\nearrow G.$$

The [[action groupoid]] $V//G$ is then given by

$$V//G=El(V\nearrow G).$$

##References##

* [Wikipedia: Category of elements](http://en.wikipedia.org/wiki/Category_of_elements)

##Discussion##

[[Eric Forgy|Eric]]: This seems like the gadget I'm trying to describe at [[Exploding a Category]] (I may remove that material once I understand what's going on). I understand the concept (I think!), but why the notation $\int_C P$?

_Toby_:  That notation is a reference to the standard notation for a co[[end]].

[[Urs Schreiber|Urs]]: I'd say the integral sign here originates quite concretely in the idea that the category of elements of $F$ is the _union_ of all the elements of $P(c)$ for all $c$. 

[[Eric Forgy|Eric]]: I think this concept is important (for me anyway) and the intergal notation is cumbersome. What would be an acceptable alternative? For now, I think I will borrow from [[category of generalized elements]] and [Wikipedia](http://en.wikipedia.org/wiki/Category_of_elements) and denote it $El(P)$. I can change it back if there is an uproar. I would actually prefer something like $Unpack(C)$ to emphasize the relation to $C$.

PS: Don't worry. I will make the edits once a nice notation is decided.
