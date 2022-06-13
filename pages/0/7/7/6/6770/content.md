
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The __Selberg integral__ is a higher-dimensional generalization of the integral representation of Euler's beta function due Alte Selberg. Many further "Selberg-type" generalizations appear in the study of multidimensional generalizations of hypergeometric functions, arrangements of hyperplanes, [[Knizhnik-Zamolodchikov equation]], representation theory of quantum and affine Lie algebras and of vertex operator algebras, random matrix theory etc. There is also an elliptic generalization, see [[elliptic Selberg integral]].

$$
\int_0^1 \cdots \int_0^1 (u_1\cdots u_p)^{x-1} [(1-u_1)\cdots (1-u_p)]^{y-1} \left( \prod_{i\lt j} (u_j-u_i)\right)^{2 z} d u_1 \ldots d u_p =
\prod_{s = 1}^p \frac{\Gamma(1+s z) \Gamma(x+(s-1)z)\Gamma(y+(s-1)z)}{ \Gamma(1+z)\Gamma(x+y+(p+s-2)z)}
$$
where $p\gt 0$ is a positive integer, $Re x\gt 0$, $Re y\gt 0$ , $Re z \gt max\{-p^{-1},- Re x/(p-1), - Re y/(p-1)\}$. Notice that the discriminant $\prod_{i\lt j} (u_j-u_i)$ is the value of the standard [[Vandermonde determinant]].

## References

* wikipedia [Selberg integral](http://en.wikipedia.org/wiki/Selberg_integral)
* Alte Selberg, _Remarks on a multiple integral_, Norsk Matematisk Tidsskrift __26__: 71&#8211;78, [MR0018287](http://www.ams.org/mathscinet-getitem?mr=0018287)
* Atle Selberg &#8211; utdypning, [biography](http://snl.no/.nbl_biografi/Atle_Selberg/utdypning) in Norweigian
* Nils A. Baas, _Atle Selberg (1917-2007)_ [pdf](http://www.math.ntnu.no/~baas/Atle_Selberg_en.pdf)
* Peter J. Forrester, S. Ole Warnaar, _The importance of the Selberg integral_, Bull. Amer. Math. Soc. (N.S.) __45__ (2008), 489-534, [pdf](http://www.ams.org/journals/bull/2008-45-04/S0273-0979-08-01221-4/S0273-0979-08-01221-4.pdf), [arxiv/0710.3981](http://arxiv.org/abs/0710.3981) 
* G. E. Andrews, R. Askey, R. Roy, _Special functions_, Enc. of Math. and its Appl. (1999)
* [[I. M. Gelfand]], M. M. [[Kapranov]], [[A. Zelevinsky]], _Discriminants, resultants and multidimensional determinants_, Birkh&#228;user 1994, 523 pp.
* J.-G. Luque, J.-Y. Thibon, _Hankel hyperdeterminants and Selberg integrals_, J. Phys. __A36__ (2003), 5267&#8211;5292,  MR1985318 (2004d:15011)
* K. Aomoto, _Jacobi polynomials associated with Selberg integrals_, SIAM
J. Math. Anal. 18 (1987) 545&#8211;549; _On the complex Selberg integral_, Q. J. Math. Oxford __38__ (1987) 385&#8211;399.
* R. S. Askey, _Some basic hypergeometric extensions of integrals of Selberg and Andrews_, SIAM J. Math. __11__ (1980) 938&#8211;951.