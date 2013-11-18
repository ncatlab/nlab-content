
#Contents#
* table of contents
{:toc}

## Motivation

In Lie theory, Bernoulli numbers appear as coefficients 
in the linear part of the [[Hausdorff series]] (and recursive
relation for the Dynkin Lie polynomials appearing in Hausdorff series); this has consequences in [[deformation theory]]. 
(Determinant of the square root of) inverse of its generating function appears (for variable in adjoint representation) in an expression for the [[Duflo isomorphism]] in Lie theory and in its generalizations in knot theory etc. 

In algebraic topology Bernoulli numbers (or equivalently, 
their generating function) appear 
in the expression for the [[Todd class]] 
and as the order of some groups 
in the [[image of the J-homomorphism]] 
(cf. [Adams 65, section 2](#Adams65)).

It also has applications in analysis ([[Euler-MacLaurin formula]], with applications in numerical analysis).

Bernoulli numbers appear also in [[umbral calculus]]. There are generalizations, for example, Bernoulli polynomials. 

## Definition

Bernoulli numbers $B_k$ are rational numbers given by their [[generating function]], i.e. by the [[equation]] of [[functions]]/[[power series]] $x \mapsto f(x)$

$$
  \frac{x}{
    e^x -1
  }
  =
  \sum_{k = 0}^{\infty} \frac{\beta_k}{k !}x^k
  \,.
$$

The $k$th Bernoulli number $B_k \in \mathbb{Q}$ is, depending on convention, either equal to $\beta_k$ (or sporadically, in older literature, to $(-1)^{k-1} \beta_{2k}$). 
If we take generating function
$x+\frac{x}{e^x-1}=\frac{x e^x}{e^x -1}=\frac{-x}{e^{-x}-1}$ this only changes the sign of $B_1$ as all other odd Bernoulli numbers (in standard convention) vanish. 

## Reference

### General

* wikipedia: [Bernoulli number](http://en.wikipedia.org/wiki/Bernoulli_number)
* Wolfram MathWorld:  [Bernoulli number](http://mathworld.wolfram.com/BernoulliNumber.html)
* [[John C. Baez]], _The Bernoulli numbers_, 2003 expository notes, [pdf](http://math.ucr.edu/home/baez/qg-winter2004/bernoulli.pdf)
* Bernoulli numbers page [bernoulli.org](http://bernoulli.org)
* chapter 3 in [[Pierre Cartier]], _Mathematigics_, [pdf](http://www.mat.univie.ac.at/~slc/wpapers/s44cartier1.pdf)

### Lie theory, deformation theory, knot theory, geometry

* MathOverflow [Todd class and Baker-Campbell-Hausdorff, or the curious number 12](http://mathoverflow.net/questions/31972/todd-class-and-baker-campbell-hausdorff-or-the-curious-number-12)
* [[Nikolai Durov|N. Durov]], S. Meljanac, A. Samsarov, [[Z. Škoda]], _A universal formula for representing Lie algebra generators as formal power series with coefficients in the Weyl algebra_, Journal of Algebra __309__:1, pp.318-359 (2007) [math.RT/0604096](http://arxiv.org/abs/math.RT/0604096), MPIM2006-62
* Vinay Kathotia, _Kontsevich's universal formula for deformation quantization and the Campbell-Baker-Hausdorff formula, I_, [math.QA/9811174](http://arxiv.org/abs/math/9811174)
* Emanuela Petracci, _Functional equations and Lie algebras_, PhD thesis, [pdf](http://www1.mat.uniroma1.it/didattica/dottorato/TESI/ARCHIVIO/petracciemanuela.pdf)
* E. Meinrenken, _Clifford algebras and Lie theory_, Springer
* [[Anton Alekseev]], _Bernoulli numbers, Drinfeld associators, and the Kashiwara&#8211;Vergne problem_, slides, [pdf](http://www.6ecm.pl/docs/Alekseev.pdf)
* Dror Bar-Natan, Stavros Garoufalidis, Lev Rozansky, Dylan P. Thurston, _Wheels, wheeling, and the Kontsevich integral of 
the unknot_, [q-alg/9703025](http://arxiv.org/abs/q-alg/9703025)

### In classical algebraic topology

* [[John Adams]], _On the groups $J(X)$ II_, Topology 3 (2) (1965) ([pdf](http://math1.unice.fr/~cazanave/Gdt/ImJ/J-II.pdf))
 {#Adams65}

### Analysis

* T. Tao's blog: [The Euler-Maclaurin formula, Bernoulli numbers, the zeta function, and real-variable analytic continuation](http://terrytao.wordpress.com/2010/04/10/the-euler-maclaurin-formula-bernoulli-numbers-the-zeta-function-and-real-variable-analytic-continuation)

[[!redirects Bernoulli numbers]]