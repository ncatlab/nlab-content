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
     & remembers & stuff, structure, property
     \\
     essentially (k \geq 1)-surjective & forgets at most & property 
     & remembers & stuff, structure
     \\
     essentially (k \geq 2)-surjective & forgets at most & structure
    & remembers & stuff
     \\
     essentially (k \geq 3)-surjective & forgets & stuff
    &
    remembers & nothing
  }
$$


It is noteworthy how this formalism captures the heuristic way in which "stuff", "structure" and "property" are expected to be related:

* stuff may be equipped with structure;

* structure may have (be equipped with) properties.

See also the examples below.

## Generalization to higher groupoids##

The formulation in terms of $k$-surjectivity induces an immediate generalization of the notions of stuff, structure and property to the context of [[infinity-category|infinity-groupoids]].

(I believe Baez's students speak of "2-stuff", etc.)


##Generalization to categories and higher categories##

The theory is easiest when restricted to groupoids as above; for [[category|categories]], there are two ways to go.  One is to keep the definition as phrased above; the other is to look at the functor between the underlying groupoids of the categories.  To tell the difference, ask yourself whether the difference between a [[monoid]] and a [[semigroup]] is the *structure* of being equipped with an [[identity]] element or only the *property* that an identity element exists.  (Note that an identity element, if it exists, must be unique and must be preserved by semigroup isomorphisms and by monoid homomorphisms but not by semigroup homomorphisms.)

#Examples#


## The classical categories of sets with extra structure ##

The classical examples are the forgetful functors to [[Set]]  that define the classical categories such as [[Top]], [[Grp]], [[Vect]], etc. All these categories are categories of <em>sets equipped with extra structure</em> (e.g. with a topology, with a group structure, etc). Accordingly the obvious functors to [[Set]] are 

* faithful

* not full.

Hence indeed, by the above yoga, they forget this extra structure but remember the stuff in question (the underlying set).

## More examples ##


The embedding of abelian groups into all groups, $F :$ [[Ab]] $\to$ [[Grp]] is faithful and full, but not essentially surjective. Hence it should remember stff and structure but forget property. Indeed, the property it forgets is the property "is abelian" which is a property of the group _structure_ sitting on the underlying set of a group. Hence the sequence of functors
$$
  Ab \to Grp \to Set \to Pt
$$
(with [[point|Pt]] the terminal category) successively forgets first a property (being abelian) then a structure (group structure on a set) then stuff (the underlying set).




#References#

* [original UseNet discussion](http://math.ucr.edu/home/baez/qg-spring2004/discussion.html) on `sci.physics.research` in 1998;
* a pedagogical comparison to quadratic, linear, and constant polynomials ([PDF](http://math.ucr.edu/home/baez/qg-spring2004/polynomials.pdf)) by Toby Bartels in 2004;
* [section 2.4, p. 15](http://arxiv.org/PS_cache/math/pdf/0608/0608420v2.pdf#page=15) of J. Baez and M. Shulman, _Lectures on $n$-categories and cohomology_ ([arXiv](http://arxiv.org/abs/math/0608420)).