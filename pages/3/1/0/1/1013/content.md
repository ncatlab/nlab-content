#Idea#

[[category theory|Category theory]] frequently allows to give precise and useful formalized meanings to "everyday" terms, at least terms used everyday by practicing mathematicians. 

It was indeed introduced originally in order to formalize the use of the notion "natural" in mathematics. Another frequently recurring triple of terms in math is "extra structure", and "extra properties" and "extra stuff". In discussion among Jim Dolan, John Baez and Toby Bartels, the following useful formalization of these concepts in category theoretic terms was established.

#Definition (for groupoids)#

Let $C$ and $D$ be [[groupoid]]s, and let $F: C \to D$ be a [[functor]].  By fiat, declare $F$ to be a [[forgetful functor]].  Then 

* $F$ **forgets nothing** if it is an [[equivalence of categories]]; 

* $F$ **forgets only property** if $F$ is [[full and faithful functor|fully faithful]]; 

* $F$ **forgets at most structure** if $F$ is [[faithful functor|faithful]]; 

* $F$ **forgets at most stuff** regardless.  

## Interpretation in terms of k-surjectivity##

The pattern here is best understood in terms of the notion of [[k-surjective functor|essentially k-surjective functor]]. 

Recall that for a functor between ordinary categories (1-categories)

* essentially surjective $\simeq$ essentially 0-surjective

* full $\simeq$ essentially 1-surjective

* faithful $\simeq$ essentially 2-surjective

and that every 1-functor is essentially $k$-surjective for all $k \geq 3$.

So the above says for a functor $F : C \to D$:

$$
  \array{
     essentially (k \geq 0)-surjective & forgets & nothing
     \\
     essentially (k \geq 1)-surjective & forgets at most & property
     \\
     essentially (k \geq 2)-surjective & forgets at most & structure
     \\
     essentially (k \geq 3)-surjective & forgets & stuff
  }
$$



## Generalization to higher groupoids##

The formulation in terms of $k$-surjectivity induces an immediate generalization of the notions of stuff, structure and property to the context of [[infinity-category|infinity-groupoids]].

(I believe Baez's students speak of "2-stuff", etc.)


##Generalization to categories and higher categories##

The theory is easiest when restricted to groupoids as above; for [[category|categories]], there are two ways to go.  One is to keep the definition as phrased above; the other is to look at the functor between the underlying groupoids of the categories.  To tell the difference, ask yourself whether the difference between a [[monoid]] and a [[semigroup]] is the *structure* of being equipped with an [[identity]] element or only the *property* that an identity element exists.  (Note that an identity element, if it exists, must be unique and must be preserved by semigroup isomorphisms and by monoid homomorphisms but not by semigroup homomorphisms.)

#References#

* [original UseNet discussion](http://math.ucr.edu/home/baez/qg-spring2004/discussion.html) on `sci.physics.research` in 1998;
* a pedagogical comparison to quadratic, linear, and constant polynomials ([PDF](http://math.ucr.edu/home/baez/qg-spring2004/polynomials.pdf)) by Toby Bartels in 2004;
* [section 2.4, p. 15](http://arxiv.org/PS_cache/math/pdf/0608/0608420v2.pdf#page=15) of J. Baez and M. Shulman, _Lectures on $n$-categories and cohomology_ ([arXiv](http://arxiv.org/abs/math/0608420)).