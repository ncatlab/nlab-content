#Idea#

* In the familiar **specific sense**, a coalgebra is a monoid [[internalization|in]] the [[category]] $Vect^{op}$, analogous to how an algebra is a monoid in $Vect$.

* In a more **general sense**, 

  * a **coalgebra for an endo[[functor]]** $F : C \to C$ on a [[category]] $C$ -- an _$F$-coalgebra_ --  is 

    * an [[object]] $A$ of $C$;

    * and a [[morphism]] $\alpha : A \to F(C)$;

  * a general **coassociative coalgebra** is a coalgebra over a comonad, dual to the concept of an [[algebra over a monad]].

##Examples##

* For $R$ a commutative ring, if the endofunction $F : C \to C$ is $F : R-Mod \to R-Mod$ given by $F : N \mapsto N \otimes N$, then $F$-coalgebras are precisely non-coassociative coalgebras in the specific sense of non-associtive monoids in $R-Mod^{op}$. (See Tom Leinster's comment [here](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html#c020741)).

* [[Lie infinity-algebroid]]s are [[CoDGCA|cocommutative comonoids]] in the category of chain complexes.


#Blog resources#

David Corfield, [_Coalgebraically Thinking_](http://golem.ph.utexas.edu/category/2008/11/coalgebraically_thinking.html)

David Corfield, [_The Status of Coalgebra_](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html)