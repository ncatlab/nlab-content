#Idea#

The _category of elements_ is a $0$-category-theoretic version of the [[Grothendieck construction]], due to Mac Lane.

The notion of category of elements and of Grothendieck construction and its higher analogs are all examples of pullbacks of [[generalized universal bundle]]s:

for $F : C^{op} \to Set$ a [[presheaf]], we may think of $Set$ as the [[classifying space]] of "[[Set]]-bundles". The category of elements of $F$ is, in this sense, the [[Set]]-bundle classified by $F$.

#Definition#

Given a functor $P:C^{\mathrm{op}}\to\mathbf{Set}$ (a [[presheaf]] of sets on $C$), the **category of elements**$ \int_C P$ of $P$ is equivalently

* the [[category]] whose objects are pairs $(c,x)$ where $c$ is an object in $C$ and $x$ is an element in $P(c)$ and morphisms $(c,x)\to(c',x')$ are morphisms $u:c\to c'$ such that $P(u)(x') = x$;

* the [[comma category]] $(Y,const_P)$, where $Y$ is the [[Yoneda embedding]];

* the [[pullback]] along $F$ of the [[generalized universal bundle|universal Set-bundle]] $U : Set_* \to Set$ $\array{ (\int_C P)^{op} &\to& Set_* \\ \downarrow^{\pi_P^{op}} && \downarrow^U \\ C^{op} &\to& Set}\,,$ where $U$ is the [[stuff, structure, property|forgetful functor]] from pointed sets to sets.

* the "lax pullback" (really: [[comma object]]) of the [[point]] along $F$: $\array{ (\int_C P)^{op} &\to& * \\ \downarrow^{\pi_P^{op}} &\Downarrow& \downarrow^{pt} \\ C^{op} &\to& Set}$. 

#Properties#

* The category of elements is naturally equipped with a _projection functor_ $\pi_P:\int_C P \to C$ given by $(c,x)\mapsto c$ and $u\mapsto u$; this projection should be viewed also as a $C$-indexed family.