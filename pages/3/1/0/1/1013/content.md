#Idea#

[[category theory]] frequently allows to give precise and useful formalized meanings to "everyday" terms, at least terms used everyday by practicing mathematicians. 

It was indeed introduced originally in order to formalize the use of the notion "natural" in mathematics. Another frequently recurring triple of terms in math is "extra structure", and "extra properties" and "extra stuff". In discussion among Jim Dolan, John Baez and Toby Bartels, the following useful formalization of these concepts in category theoretic terms was established.

#Definition#

Let $C$ and $D$ be [[groupoid]]s, and let $F: C \to D$ be a [[functor]].  By fiat, declare $F$ to be a [[forgetful functor]].  Then $F$ **forgets nothing** if it is an [[equivalence of categories]]; $F$ **forgets only property** if $F$ is [[full and faithful functor|fully faithfull]]; $F$ **forgets at most structure** if $F$ is [[faithful functor|faithful]]; $F$ **forgets at most stuff** regardless.  (One can generalise to [[2-groupoid]]s and so on, in which case not every functor forgets at most stuff.)

The theory is easiest when restricted to groupoids as above; for [[category|categories]], there are two ways to go.  One is to keep the definition as phrased above; the other is to look at the functor between the underlying groupoids of the categories.  To tell the difference, ask yourself whether the difference between a [[monoid]] and a [[semigroup]] is the *structure* of being equipped with an [[identity]] element or only the *property* that an identity element exists.  (Note that an identity element, if it exists, must be unique and must be preserved by semigroup isomorphisms and by monoid homomorphisms but not by semigroup homomorphisms.)

#References#

* [original UseNet discussion](http://math.ucr.edu/home/baez/qg-spring2004/discussion.html) on `sci.physics.research` in 1998;
* a pedagogical comparison to quadratic, linear, and constant polynomials ([PDF](http://math.ucr.edu/home/baez/qg-spring2004/polynomials.pdf)) by Toby Bartels in 2004;
* [section 2.4, p. 15](http://arxiv.org/PS_cache/math/pdf/0608/0608420v2.pdf#page=15) of J. Baez and M. Shulman, _Lectures on $n$-categories and cohomology_ ([arXiv](http://arxiv.org/abs/math/0608420)).