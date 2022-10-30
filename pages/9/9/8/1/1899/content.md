# Idea #

Given an [[algebraic theory]] $V$, a $V$-algebra is a model of $V$ in the category $Set$.  A _Tall--Wraith $V$-monoid_ is _the kind of thing that acts on $V$-algebras_.  


# Definition #

Let $V$ be an [[algebraic theory]] and let $V Alg$ be the category of models of this theory in $Set$.  Then a **Tall--Wraith $V$-monoid** is a [[monoid|monoid object]] in the category of co-$\mathcal{V}$-objects in $V Alg$.   


# Examples #

* If $V$ is the theory of [[commutative ring|commutative unital rings]], a $V$-algebra is a commutative unital ring, and the corresponding sort of Tall--Wraith $\mathcal{V}$-monoid is called a [[biring]].  

* If $V$ is the theory of [[commutative algebra|commutative associative algebras]] over a [[field]] $k$, then a $V$-algebra is a commutative associative algebra over $k$, and the corresponding sort of Tall--Wraith $V$-monoid is called a [[plethory]].

+-- {: .query}

* If $V$ is the theory of [[abelian group|abelian groups]], than a $V$-algebra is an abelian group, and the corresponding sort of Tall--Wraith $V$-monoid must be something very simple, but don't ask me what!  

It should be very easy to see _why_ these Tall-Wraith monoids act on $V$-algebras: with our categorical sophistication, I bet there's a one-sentence explanation.  But don't ask me what that is, either.  

Can someone help out?  [[John Baez]]

=--

# References #

* _Representable functors and operations on rings_, D. Tall and [[Gavin Wraith|G. Wraith]], Proc. London Math. Soc. (3), 1970

* _Plethystic algebra_, J. Borger and B. Wieland, Adv. Math, 2005

* _The Hunting of the Hopf Ring_, [[Andrew Stacey|A. Stacey]] and S. Whitehouse, [arXiv:0711:3722](http://arxiv.org/abs/0711.3722)


+-- {: .standout}
[[John Baez]]: The above material is tentative, based on things I heard [on the $n$-Cafe](http://golem.ph.utexas.edu/category/2009/07/the_monads_hurt_my_head_but_no.html#c025550), but may not have understood. 

[[Andrew Stacey]]: looks okay to me.  I put in lots of "commutative"s in the examples because the original papers in both cases dealt with commutative cases and I thought it best that the examples were as close as possible to the originals.  I also changed the $V$ to $\mathcal{V}$ in line with the notation from _The Hunting of the Hopf Ring_.  Should there be a lab standard on fonts for categories, objects, functors, and the like?

_Toby_:  Based on [this discussion](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=37), '$\mathcal{V}$' is more likely to cause problems for people that haven\'t installed appropriate fonts.  (Not that I\'m changing it back, mind you ....)

[[John Baez]]: I hate 'fancy fonts for fancy gizmos', because they mainly serve to make gizmos seem fancy and intimidating.  That's why I had changed $\mathcal{V}$ to $V$.  I think I'll change it back again, just to annoy Andrew.  It's just a category with products, for god's sake!  Surely we can't insist on calligraphic font whenever we see one of those: must we say $\mathcal{Set}$?  (Yes, I'm being ornery.)

=--


[[!redirects Tall--Wraith monoid]]
[[!redirects Tall–Wraith monoid]]