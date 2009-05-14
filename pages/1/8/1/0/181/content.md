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

## Terminal (final) coalgebras

This section gives some material on the notion of coalgebra of an endofunctor $F: C \to C$, as defined above. 

Given two coalgebras $(x, \eta: x \to F x)$, $(y, \theta: y \to F y)$, a coalgebra map is a morphism $f: x \to y$ which respects the coalgebra structures: 

$$\theta \circ f = F(f) \circ \eta$$

A **terminal coalgebra** (usually called a _final coalgebra_ in the literature) is of course a terminal object in the category of coalgebras. Many data structures can be expressed as terminal coalgebras of suitable endofunctors; a simple but useful theorem says that terminal coalgebras $x$ are "fixed points" of their endofunctors, in that $F x \cong x$. This is the dual form of a theorem discovered long ago by Lambek: 

**Theorem**: If $(x, \theta: x \to F x)$ is a terminal object in the category of $F$-coalgebras, then $\theta$ is an isomorphism. 

Proof: Define a coalgebra structure on $F x$ by $F\theta: F x \to F F x$. By terminality of $x$, there is a unique coalgebra map $f: F x \to x$. We claim this is inverse to $\theta$. Indeed, by how we defined the coalgebra structure on $F x$, it is tautological that $\theta$ is a coalgebra map. By terminality of $x$ again, this gives an equation of coalgebra maps:

$$f \circ \theta = 1_x.$$

On the other hand, 

$$\theta \circ f = F(f) \circ F(\theta) = F(f \circ \theta) = F(1_x) = 1_{F x}$$

where the first equation holds because $f$ is a coalgebra map. This completes the proof. $\Box$

To construct terminal coalgebras, the following result is useful and practical: 

**Theorem** (Adamek): If $C$ has a terminal object $1$ and the limit $L$ of the diagram 

$$\ldots F^3 1 \stackrel{F^2 !}{\to} F^2 1 \stackrel{F !}{\to} F 1 \stackrel{!}{\to} 1 \qquad (1)$$ 

exists in $C$ and $F$ preserves this limit, then the limit 
carries a structure of terminal coalgebra. 

Proof: Let $\pi_n: L \to F^n 1$ be the $n^{th}$ projection of the limiting cone. Then we have a cone from $F L$ to the diagram (1) whose components are 

$$F L \stackrel{F\pi_n}{\to} F^{n+1} 1 \stackrel{F^n !}{\to} F^n 1$$ 

and the induced map $F L \to L$ to the limit is invertible by hypothesis; let $\theta: L \to F L$ be the inverse. We claim the coalgebra $(L, \theta)$ is terminal. 

Indeed, suppose $(x, \eta: x \to F x)$ is any coalgebra. We recursively define maps $f_n: x \to F^n 1$: let $f_0: x \to 1$ be the unique map, and 

$$f_{n+1} = F(f_n) \circ \eta$$ 

It is easily checked by induction that these maps define a cone from $x$ to the diagram (1), and so we get a map $f: x \to L$. (More later)

+--{.query}
_Todd_: I noticed under "algebra" that it wasn't so easy to find a page for algebras of an endofunctor. It might help to have something like "Algebra (disambiguation)" for this and other entries with multiple meanings. 

_Mike_: Seconded.
=--

##Differential graded coalgebras

These are explored briefly in the lexicon style entry [[differential graded coalgebra]].  (At present this is 'bare bones' with little or no motivation or discussion.)

#Blog resources#

David Corfield, [_Coalgebraically Thinking_](http://golem.ph.utexas.edu/category/2008/11/coalgebraically_thinking.html)

David Corfield, [_The Status of Coalgebra_](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html)

#References#

Jiri Adamek, [Introduction to coalgebras](http://www.tac.mta.ca/tac/volumes/14/8/14-08abs.html),
_Theory and Applications of Categories_, Vol. 14 (2005), No. 8, 157-199.