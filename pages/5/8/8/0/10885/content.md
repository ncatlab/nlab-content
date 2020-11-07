_Fredholm determinant_ is a generalization of a determinant of a finite-dimensional matrix to a class of operators on Banach spaces which differ from identity by a trace class operator or by an appropriate analogue in more abstract context (there are appropriate determinants on certain Banach ideals). It is often considered as an analytic function of a perturbation parameter $\lambda$. The calculations with Fredholm determinants have applications in operator theory, [[random matrix]] theory, integrable models etc.

In his original setup, Fredholm attached the determinant
$$
d(\lambda) = \sum_{n=0}^{\infty} 
\frac{\lambda^n}{n!}\int_a^b\int_a^b\ldots \int_a^b det((K(x_k, x_l))_{k,l=1}^n) d x_1 \cdots d x_n 
$$
to the Fredholm integral equation of the second kind
$$
u(x) + \lambda \int^b_a K(x,y) u(y) d y  = f(x), \,\,\,x\in (a,b),
$$
and $d$ is an [[entire function]] of $\lambda$ such that $d(\lambda) \neq 0$ iff the integral equation has a unique solution.

## References

#### General and mathematical

* wikipedia [Fredholm determinant](http://en.wikipedia.org/wiki/Fredholm_determinant)
* Albrecht Pietsch, _Operator ideals_,  North-Holland Mathematical Library 20; _Eigenvalues and s-Numbers_,  Cambridge Studies in Advanced Mathematics 13; _History of Banach spaces and linear operators_, sec 6.5.2
* [[Alexander Grothendieck]], _La th&#233;orie de Fredholm_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __84__ (1956), p. 319-384, [numdam](http://www.numdam.org/item?id=BSMF_1956__84__319_0)
* Fritz Gesztesy, Yuri Latushkin, Konstantin A. Makarov, _Evans functions, Jost functions and Fredholm determinants, Arch. Rational Mech. Anal. 186 (2007) 361&#8211;421,[doi](http://dx.doi.org/10.1007/s00205-007-0071-7) [pdf](http://www.math.missouri.edu/~yuri/preprints/EJF.pdf)
* Barry Simon, _Notes on infinite determinants of Hilbert space operators_, Advances in Math. __24__ (1977), no. 3, 244&#8211;273 [MR482328](http://www.ams.org/mathscinet-getitem?mr=482328) <a href="http://dx.doi.org/10.1016/0001-8708(77)90057-3">doi</doi>
* Folkmar Bornemann, _On the numerical evaluation of Fredholm determinants_, Math. Comp. 79 (2010), no. 270, 871&#8211;915 [MR2600548](http://www.ams.org/mathscinet-getitem?mr=2600548)
[pdf](http://www-m3.ma.tum.de/foswiki/pub/M3/Allgemeines/FolkmarBornemannPublications/Fredholm.pdf) [doi](http://dx.doi.org/10.1090/S0025-5718-09-02280-7) 

#### Physics applications

* F. J. Dyson, _Fredholm determinants and inverse scattering problems_, Comm. Math. Phys. 47, 171&#8211;183 (1976) [MR406201](http://www.ams.org/mathscinet-getitem?mr=406201) [euclid](http://projecteuclid.org/euclid.cmp/1103899727)
* C. A. Tracy, H. Widom, _Fredholm determinants, differential equations and matrix models_, Commun. Math. Phys. __163__, 33&#8211;72 (1994) [MR1277933](http://www.ams.org/mathscinet-getitem?mr=1277933) [euclid](http://projecteuclid.org/getRecord?id=euclid.cmp/1104270379) 
* J. Harnad, Alexander R. Its, _Integrable Fredholm operators and dual isomonodromic deformations_, 
Comm. Math. Phys. 226 (2002), no. 3, 497&#8211;530 [MR1896879](http://www.ams.org/mathscinet-getitem?mr=1896879) [doi](http://dx.doi.org/10.1007/s002200200614) 
* M. Adler, [[M. Cafasso]], P. van Moerbeke, _Nonlinear PDEs for Fredholm determinants arising from string equations_, [arxiv/1207.6341](http://arxiv.org/abs/1207.6341) 
* M. Bertola, [[M. Cafasso]], _Fredholm determinants and pole-free solutions to the noncommutative Painlev&#233; II equation_, Comm. Math. Phys. __309__ (2012), no. 3, 793&#8211;833 [MR2885610](http://www.ams.org/mathscinet-getitem?mr=2885610) [doi](http://dx.doi.org/10.1007/s00220-011-1383-x)
* Michio Jimbo, Tetsuji Miwa, Yasuko M&#244;ri, Mikio Sato, 
_Density matrix of an impenetrable Bose gas and the fifth Painlev&#233; transcendent_, Phys. D 1 (1980), no. 1, 80&#8211;158 [MR573370](http://www.ams.org/mathscinet-getitem?mr=573370) <a href="http://dx.doi.org/10.1016/0167-2789(8090006-8)">

category: functional analysis
[[!redirects Fredholm determinants]]