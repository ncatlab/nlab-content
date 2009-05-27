#Idea#

In the [most familiar sense](http://en.wikipedia.org/wiki/Coalgebra), a coalgebra is just like an associative algebra, but with all the maps 'turned around'.   More precisely, fix a ground field $k$.    An **algebra** $A$ is a vector space equipped with a multiplication

$$m : A \otimes A \to A$$

and a unit

$$i : k \to A $$

satisfying the associative law and left/right unit laws, which can be drawn as commutative diagrams.   Similarly, a **coalgebra** $C$ is a vector space equipped with a **comultiplication** 

$$\Delta : A \to A \otimes A $$

and a **counit**

$$ e: A \to k$$

satisfying the **coassociative** and left/right **counit** laws.  The commutative diagrams for these laws are obtained by taking the diagrams for the associative and left/right unit laws and turning all the arrows around.  To see these diagrams, try the [Wikipedia entry](http://en.wikipedia.org/wiki/Coalgebra#Formal_definition).  (Someone please put these diagrams here!)

We can express this idea much more efficiently using the concept of the [[opposite category|opposite]] of a [[category]], together with [[internalization]].  Namely: a **coalgebra** is a [[monoid]] [[internalization|in]] the $Vect^{op}$, just as an algebra is a monoid in $Vect$.

Coalgebras of this sort are an important ingredient in more sophisticated structures such as [[bialgebra|bialgebras]], [[Hopf algebra|Hopf algebras]] and [[Frobenius algebra|Frobenius algebras]].

More generally: 

* a **coalgebra for an endo[[functor]]** $F : C \to C$ on a [[category]] $C$ -- an _$F$-coalgebra_ --  is 

    * an [[object]] $A$ of $C$;

    * and a [[morphism]] $\alpha : A \to F(A)$;

* a general **coassociative coalgebra** is a coalgebra over a comonad, dual to the concept of an [[algebra over a monad]].

##Examples##

* For $R$ a commutative ring, if the endofunction $F : C \to C$ is $F : R-Mod \to R-Mod$ given by $F : N \mapsto N \otimes N$, then $F$-coalgebras are precisely non-coassociative coalgebras in the specific sense of non-associtive monoids in $R-Mod^{op}$. (See [[Tom Leinster]]'s comment [here](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html#c020741)).

* $L_\infty$-[[L-infinity-algebra|algebra]]s are [[CoDGCA|cocommutative comonoids]] in the category of chain complexes.


+--{.query}
_Todd_: I noticed under "algebra" that it wasn't so easy to find a page for algebras of an endofunctor. It might help to have something like "Algebra (disambiguation)" for this and other entries with multiple meanings. 

_Mike_: Seconded.

_Toby_:  The page [[algebra]] is already basically a disambiguation page; the problem is that some links to it should go to different pages, and [[algebra for an endofunctor]] really ought to be created (which I just did).
=--

##Differential graded coalgebras

These are explored briefly in the lexicon style entry [[differential graded coalgebra]].  (At present this is 'bare bones' with little or no motivation or discussion.)
