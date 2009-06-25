For a given [[geometric theory]] $T$, a **classifying [[topos]]** for $T$ is a [[Grothendieck topos]] $S[T]$ equipped with a "universal model $U$ of $T$".  This means that for any Grothendieck topos $E$ together with a model $X$ of $T$ in $E$, there exists a unique (up to isomorphism) [[geometric morphism]] $f: E \to S[T]$ such that $f^*$ maps the $T$-model $U$ to the model $X$.  More precisely, for any Grothendieck topos $E$, the category of $T$-models in $E$ is equivalent to the category of geometric morphisms $E \to S[T]$.

Any [[Grothendieck topos]] can be thought of as a 'classifying topos'. A useful discussion of this idea starts
[here](http://golem.ph.utexas.edu/category/2007/10/geometric_representation_theor_2.html#c012724).

Classifying toposes can also be defined over any base topos $S$ instead of [[Set]].  In that case "Grothendieck topos" is replaced by "bounded $S$-topos."

## Discussion 

The notion of classifying topos is part of a trend, begun by Lawvere, of viewing a mathematical [[theory]] as a category with suitable exactness properties and which contains a "generic model", and a model of the theory as a functor which preserves those properties. The original example is that of finitary [[algebraic theory]], which was reformulated in terms of categories with finite products (see [[Lawvere theory]]). Roughly speaking, an algebraic theory is any theory which can be formulated in the language of categories with finite products. An example would be the theory of groups. As explained in the entry for [[Lawvere theory]], each algebraic theory has a Lawvere theory which is a "classifying category" for that theory, in that models for the theory correspond precisely to product-preserving functors coming out of the Lawvere theory.

Next up the line is the notion of (finitary) [[essentially algebraic theory]]. This is any theory which can be formulated in the language of [[finitely complete category|categories with finite limits]]. An example would be the theory of categories. Again, every essentially algebraic theory admits a classifying category: a [[finitely complete category]] with a "generic model", such that models of the theory correspond to left exact functors coming out of that category. 

Further up the line (and speaking roughly), a [[geometric theory]] is a theory which can be formulated in that fragment of first-order logic that deals in finite limits and arbitrary (small) colimits. Certain exactness properties which come into play here, but there are two basic ideas to keep in mind. One is that a geometric theory has a classifying category: a category having those exactness properties (viz., a Grothendieck topos) and possessing a "generic object" for that theory. The other is that a geometric morphism $ f_*: E \to S[T] $ is tantamount to a left exact left adjoint $ f^*: S[T] \to E $, which preserves such finite limits and small colimits ($ f_* $ is the right adjoint of $ f^* $). The left exact left adjoint would thus be a model of that theory, much as models of an essentially algebraic theory are left exact functors out of the classifying category for that theory. 

## Examples 

* The classifying topos for groups. 

As a warm-up, we first discuss the classifying category for the theory of groups $T$ _qua_ essentially algebraic theory, i.e., we give a finitely complete category $Lex[T]$ equipped with a "generic group". This works much the same way as the [[Lawvere theory]] for groups, which is the category opposite to the category of finitely generated free groups, except that we have to "close up" the Lawvere theory under all finite limits. 

Thus, we take $Lex[T]$ to be the category opposite to the category of _finitely presented groups_: those groups $G$ which arise as coequalizers of diagrams 

$$F(m) \rightrightarrows F(n)$$ 

between finitely generated free groups. It may be shown that $Lex[T]$ is finitely complete, and the "generic group" inside $Lex[T]$ is $F(1)$, the free group on one generator, just as it is for the [[Lawvere theory]] (see the discussion at that entry). 

* The classifying topos for intervals. 

* The classifying topos for [[local ring|local rings]]. 


[[!redirects Another page]]