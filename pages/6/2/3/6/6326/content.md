## Idea

__Orlov's dimension spectrum__ (or simply Orlov spectrum) is an invariant of a triangulated category, introduced by [[Dmitri Orlov]]. When the triangulated category is of geometric origin (e.g. the bounded derived category of coherent sheaves on a projective variety, or the Fukaya category associated to a symplectic manifold) then the Orlov spectrum reflects some geometric information. The spectrum is 
defined in terms of counting the extensions needed to generate all the objects from a fixed object, with some other operations, like competing under direct coproducts and summands not counted. 

## Definitions

An object $E$ in a triangulated category $T$ defines the smallest triangulated subcategory $I_E\subset T$ which is closed under direct sum. Given two full triangulated subcategories $I_1$ and $I_2$ one defines the full triangulated category $I_1 \ast I_2$ consisting of all $M$ such that there exist $M_1$ in $I_1$ and $M_2$ in $I_2$ such that $M_1\to M \to M_2$ is a distinguished triangle, and by $\langle I_1 \ast I_2\rangle$ the smallest full subcategory of $T$ containing $I_1 \ast I_2$ and closed under finite coproducts, summands and shifts. Define by induction $\langle E\rangle_1 = I_E$ and $\langle E\rangle_{k+1} = \langle \langle E\rangle_k \ast I_E \rangle$, $k\gt 1$. 

The __dimension of a triangulated category__ $T$ is the minimal integer $d\gt 0$ such that there is $E\in Ob T$ such that $\langle E\rangle_d = T$ or infinity otherwise. The __generation time__ $d_E$ of an object $E$ in $T$ such that $\langle E\rangle_{d+1} = T$ and $\langle E\rangle_d \neq T$. $E$ is a strong generator if the generation time $d_E$ is finite. 

The __dimension spectrum__ of $T$ is the set $\sigma(T)$ of generation times of all strong generators of $T$. 

## Basic results

By a result of Rouquier, the dimension of the triangulated category $D^b(Coh X)$ for a separated scheme $X$ of finite type over a perfect field is finite and, if $X$ is in addition reduced, it is equal or bigger than the Krull dimension of $X$ but smaller or equal the double dimension $2 dim(X)$. By a conjecture of Orlov, for any smooth variety it should be in fact equal to $dim(X)$. 

## Literature

* [[Dmitri Orlov]], _Remarks on generators and dimensions of triangulated categories_, [arxiv/0804.1163](http://arxiv.org/abs/0804.1163)
* R. Rouquier, _Dimension of triangulated categories_, J. K-Theory 1 (2008), no.2, 193-256, [arXiv:math.CT/0310134](http://arxiv.org/abs/math/0310134)
* Matthew Ballard, David Favero, [[Ludmil Katzarkov]], _Orlov spectra: bounds and gaps_, [arxiv/1012.0864](http://arxiv.org/abs/1012.0864)
* [[A. Bondal]], M. van den Bergh, _Generators and representability of functors in commutative and non-commutative geometry_, Mosc. Math. J. __3__ (2003), no.1, 1-36, [math.AG/0204218](http://arxiv.org/abs/math/0204218)
* David Favero, _Dimensions of triangulated categories_, joint
work with M. Ballard and L. Katzarkov, slides, Jan 2010, [pdf](http://www-math.mit.edu/~auroux/frg/miami10-notes/D.%20Favero%20-%2021-01-10%20-%20The%20dimension%20spectrum%20of%20a%20triangulated%20category.pdf)
[[!redirects Orlov's spectrum]]
[[!redirects Orlov spectra]]
[[!redirects dimension spectrum]]