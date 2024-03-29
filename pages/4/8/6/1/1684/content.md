Let $A,B$ be [[abelian category|abelian categories]], $R\subset \mathrm{Ob}A$ a class of objects in $A$ and $F:A\to B$ an [[additive functor]].

If $F$ is left [[exact functor]] we say that $R$ is a **class of objects adapted to** $F$ if $F$ sends acyclic and bounded below [[cochain complex|cochain complexes]] of objects in $R$ to acyclic complexes (= having trivial cohomology), and every object in $A$ is a [[subobject]] of an object from $R$. 

If $F$ is right [[exact functor]] we say that $R$ is a **class of objects adapted to** $F$ if $F$ sends acyclic and bounded above [[chain complex|chain complexes]] of objects in $R$ to acyclic complexes (= having trivial homology), and every object in $A$ is a [[quotient object]] of an object from $R$.

For example, if $R = I$ (resp. $R = P$) is the class of all [[injective object|injective]] (resp. [[projective object|projective]]) objects in an abelian category $A$ with sufficiently many injectives (resp. projectives), then $R$ is adapted to any left (resp. right) exact functor whose domain is $A$. If $F$ is left (resp. right) exact and a family $R$ of objects adapted to $F$ exists then the right [[derived functor]] $D^+(F):D^+(A)\to D^+(B)$ (resp. left derived functor $D^-(F):D^-(A)\to D^-(B)$) of $F$ exists by a standard construction using resolutions by objects in $R$. Flexibility in choosing an adapted class is often useful. 

References: 

* A. Grothendieck: [[Tohoku]]

* S. I. Gel'fand, Yu. I. Manin, Methods of homological algebra, Moskva 1988 (Russian); Springer 1996 (English): chapter 3

* (for generalizations in nonabelian setup) A. Rosenberg, Homological algebra of noncommutative 'spaces' I, [preprint MPIM2008-91](http://www.mpim-bonn.mpg.de/preprints/send?bid=3623)