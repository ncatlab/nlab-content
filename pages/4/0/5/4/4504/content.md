Given a $k$-algebra $A$ and an $A$-[[coring]] $C$ one can introduce  right $C$-comodules $(M,\rho)$ as right $A$-modules $M$ equipped with a  coaction which is a right $A$-module map $\rho: M\to M\otimes_A C$ satisfying the standard axioms (comodules for coalgebras were introduced by Cartier in 1950-s). There is a rather more recent dualization of the concept. A __$C$-contramodule__ is a right $A$-module $M$ equipped with a right $A$-module map $\alpha: Hom_A(C,M)\to M$ such that the diagrams

$$\array{
Hom_A(C,Hom_A(C,M)) &&\stackrel{Hom_A(C,\alpha)}\to && Hom_A(C,M)\\
\downarrow \cong &&&&\downarrow \alpha\\
Hom_A(C\otimes_A C,M)&\stackrel{Hom_A(\Delta,M)}\to&Hom_A(C,M)&\stackrel{\alpha}\to& M\\}$$

$$\array{
Hom_A(A,M) &&\stackrel{Hom_A(\epsilon,M)}\to && Hom_A(C,M)\\
&\searrow \cong &&\swarrow \alpha &\\
&&M&& \\}$$

commute.

Historically contramodules seem to first being mentioned few times in Eilenberg-Moore treatments in [[homological algebra]] in 1960s and by category theorists (Vazquez, Garcia, Barr). Positselski has used them in his approach to [[semiinfinite cohomology]].

* Leonid Positselski, _Homological algebra of semimodules and semicontramodules. Semi-infinite homological algebra of associative algebraic structures_, [arxiv/0708.3398](http://arxiv.org/abs/0708.3398)

* [[T. Brzeziński]], [Contramodules (pdf)](http://www.irb.hr/korisnici/zskoda/BrzezinskiSplitSlides.pdf), slides at International Conference on "Categories in Geometry", Split, September 24-28, 2007.

* [[T. Brzeziński]], _Hopf-cyclic homology with contramodule coefficients_, To appear in Quantum Groups and Noncommutative Spaces, M Marcolli and D Parashar (eds) Vieweg Verlag (Max-Planck Series), Preprint 2008, [arxiv:0806.0389](http://arxiv.org/abs/0806.0389)

[[!redirects contramodules]]