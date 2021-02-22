There are two different notions of a discrete valuation.

A __discrete valuation__ on a field $K$ is a function $v:K\to \mathbf{Z}\cup \{\infty\}$ such that 

* $v$ defines the homomorphism of groups $v|_{K^*} : K^*\to \mathbf{Z}$ where $K^*$ is the multiplicative group of $K$

* $v(0) = \infty$

* $v(x+y) \geq inf\{ v(x),v(y)\}$

with usual conventions for $\infty$. 

The set $R_v = \{x\in K\,|\, v(x)\geq 0\}$ is called the [[valuation ring]] of the valuation $v$, and it is an integral domain with quotient field $K$; its part $\mathfrak{p}_v = \{x\in K\,|\, v(x)\gt 0\}$ is a maximal ideal of $R_v$ and is called the __valuation ideal__ of $v$. This can be generalized to other [[valuation]]s.

Let $0\lt \rho\lt 1$ and define $|x|_v = \rho^{v(x)}$. Then $||$ will be a nonarchimedean multiplicative discrete valuation in the sense of the following definition. If we change a $\rho$ then we get an *equivalent* multiplicative valuation. 

A valuation on a field $K$ is a function $| |:K\to \mathbf{R}_{\geq 0}$ such that

* $|x| = 0$ iff $x=0$

* $|x y| = |x| |y|$

* there is a constant $C$ such that $|1+x|\leq C$ if $|x|\leq 1$

Two valuations on the same field are equivalent if one is the positive power of another i.e. $\exists c\gt 0$ such that $|x|_1 = |x|_2^c$ for all $x\in K$.  

A valuation is __non-archimedean__ if $C$ above can be taken $1$ and archimedean otherwise. A (multiplicative) valuation is __discrete__ if there is a neighborhood $U\ni 1\in \mathbf{R}_+$ such that the only $x\in K$ such that $|x|\in U$ is $1_K\in K$.  

By a theorem of Gel'fand and Tornheim the only archimedean valuation fields are the subfields of $\mathbf{C}$ with a valuation which is equivalent to the valuation obtained by resriction from the standard absolute value on $\mathbf{C}$.

* A. Fr&#246;hlich, J. W. S. Cassels (editors), _Algebraic number theory_, Acad. Press 1967, with many reprints; Fr&#246;hlich, Cassels, Birch, Atiyah, Wall, Gruenberg, Serre, Tate, Heilbronn, Rouqette, Kneser, Hasse, Swinerton-Dyer, Hoechsmann, systematic lecture notes from the instructional conference at Univ. of Sussex, Brighton, Sep. 1-17, 1965.  
* Serge Lang, _Algebraic number theory_. GTM 110, Springer 1970, 2000

[[!redirects discrete valuations]]