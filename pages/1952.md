Given an [[associative algebra]] $A$ let $\Omega A$ be its [[universal differential envelope]]. 


##Definition (Cuntz--Quillen 1995)## 

An associative unital $k$-algebra $A$ is __quasi-free__ (or __formally smooth__) if one of the following equivalent conditions is satisfied

* Given an extension $0\to N\to E\stackrel{q}\to B\to 0$ of algebras where the ideal $N$ is
nilpotent and $a:A\to B$ an algebra map.
Then there exists a homomorphism $a' : A \to E$ such that $q \circ a' = a$.

* $A$ has cohomological dimension $\leq 1$ with respect to [[Hochschild cohomology]];

* $\Omega^1 A$ is a projective $A$-bimodule;

* the universal Hochschild 2-cocycle $c : A\otimes A\to\Omega^2 A$, $c : a\otimes b\mapsto d a d b$ is a coboundary, i.e. $c = b\phi$ for some $\phi:A\to\Omega^2 A$ satisfying the cocycle condition $\phi(a b)=a\phi(b)+\phi(a)b-d a d b$;

* there exists a "right connection" $\nabla:\Omega^1 A\to \Omega^2 A$ i.e. a $k$-linear map satisfying $\nabla(a w)=a\nabla(w)$ and $\nabla (w a) = \nabla(w)a+w d a$ where $w\in\Omega^1 A$ and $a\in A$. 

Path algebras of [[quivers]] and free algebras are some of the (few classes of) examples. Notice that the characterization via nilpotent extensions is similar to the definition of commutative formally smooth algebras as in EGAIV4 17.1.1. However most commutative formally smooth algebras are _not_ formally smooth in the associative noncommutative sense.


##Literature##

* J. Cuntz and D. Quillen, Algebra extensions and nonsingularity, J.Amer. Math.
Soc. 8 (1995), 251-289.

* J. Cuntz and D. Quillen: Cyclic homology and nonsingularity, J. Amer. Math.
Soc. 8 (1995), 373-442.

* M. Kontsevich, A. Rosenberg, Noncommutative smooth spaces, ([arXiv:math/9812158](http://arxiv.org/abs/math/9812158))