#Idea#

+--{.query}

**Under Construction**

_[[Eric Forgy|Eric]] says_: I am trying to adapt this from the [Exercise in Groupoidification](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html) that Urs walked me through.

=--

Given a set $S$ and group $G$, we define an **action groupoid** to be denoted $S//G$ as follows: its objects are the elements of $S$ and from each element $s$ there starts precisely one morphism per element in $g$:

$$S//G:=\{s\stackrel{g}{\to} g(s) | s\in S, g\in G\}.$$

Composition of morphisms is the obvious one coming from the product in the group.

***

Given a representation $\rho: BG\to Vect$, we define an **action groupoid** to be denoted $V//G$ as follows: its objects are the elements of $V$ (i.e. the vectors in $V$) and from each element $v$ there starts precisely one morphism per element in $g$ which goes to $\rho(g)(v)$:

$$V//G:=\{v\stackrel{g}{\to} \rho(g)(v)| v\in V,g\in G\}.$$

Composition of morphisms is the obvious one coming from the product in the group.

#References#

* John Armstrong's article, [Groupoids (and more group actions)](http://unapologetic.wordpress.com/2007/06/09/groupoids-and-more-group-actions/)