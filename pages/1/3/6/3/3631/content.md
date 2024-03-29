
#Contents#
* table of contents
{:toc}


##Reprise of the Idea##
The basic idea behind Borsuk's shape theory is explained in the entry on [[shape theory]], so will not be repeated here, except to say that it considers compact metric spaces embedded in the [[Hilbert cube]], then uses the open neighbourhoods of the space as a 'net' of approximations of the space.  The space is, of course, the intersection of all these open neighbourhoods.

Any compact metric space can be embedded in the [[Hilbert cube]], so it is sufficient to consider just compact subspaces of that space.

##Some details##
Let $s= \prod_{n=1}^\infty (-\frac{1}{n},\frac{1}{n})$ be the _pseudo-interior_ of the [[Hilbert cube]], $Q= \prod_{n=1}^\infty [-\frac{1}{n},\frac{1}{n}]$. 

We will define (a category equivalent to) the *Borsuk Shape category*, $Shape_B$, to have compact subsets of $s$ as objects and some morphisms that need a bit of explaining.



If $X$ and $Y$ are compact subsets of $s$, then a _fundamental sequence_, $\underline{f} : X\to Y$, is defined to be a sequence of maps $f_n : Q\to Q$ such that for every neighbourhood $V$ of $Y$ in $Q$, there exists a neighbourhood $U$ of $X$ in $Q$ and an integer $n_0$ such that if $n, n^\prime \geq n_0$, the restrictions $f_n|_U$ and $f_{n^\prime}|_U$ are homotopic within $V$.

Note that the $f_n(X)$ do not have to be contained in $Y$, they only have to be 'near' $Y$.

Two fundamental sequences,  $\underline{f},\underline{f}^\prime : X\to Y$, are said to be _homotopic_, $\underline{f}\sim \underline{f}^\prime$ provided that for every neighbourhood $V$ of $Y$ in $Q$, there is a neighbourhood $U$ of $X$ in $Q$ and an integer $n_0$ such that if $n \geq n_0$, then $f_n|_U$ and $f^\prime_{n}|_U$ are homotopic within $V$.

The morphisms of $Shape_B$  and taken to be the homotopy classes of fundamental sequences between the corresponding spaces.

Two compacta contained in $s$ are said to have the _same shape_ if they are isomorphic in $Shape_B$.  As an example, the [[Warsaw circle]] has the same shape as the circle.

##Chapman complement theorem##
+--{.un_theorem}
######Theorem (Chapman, 1972)
If $X$ and $Y$ are compacta in $s$, then $X$ and $Y$ have the same shape if and only if their complements $Q\setminus X$ and $Q\setminus Y$ are homeomorphic.
=--

Chapman extended the association $X$ 'goes to' $Q\setminus X$ to a functor from the Borsuk shape category to the weak [[proper homotopy theory|proper homotopy]] category of complements in $Q$ of compacta.  This was the basis for Edwards-Hastings formulation of [[strong shape theory]], on replacing the weak form of proper homotopy by a strong form. 

## Related concepts

* [[shape theory]]

  * [[strong shape theory]]


##References##

* K. Borsuk, _Concerning homotopy properties of compacta_, Fund Math. 62 (1968) 223-254
* K. Borsuk, _Theory of Shape_, Monografie Matematyczne Tom 59,Warszawa 1975.
* T. A.Chapman, _On Some Applications of Infinite Dimensional Manifolds to the Theory of Shape_, Fund. Math. 6 (1972), 181 - 193.
* D. A. Edwards and [[H. M. Hastings]], (1976), &#268;ech and Steenrod homotopy theories with applications to geometric topology, Lecture Notes in Maths. 542, Springer-Verlag. 
[[!redirects Borsuk shape theory]]