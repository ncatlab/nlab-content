[[!redirects RTT algebra]]

## Idea

Given a solution of the matrix quantum Yang-Baxter equation $R\in End(V\otimes V)$, which can be viewed as a certain endomorphism of $V\otimes V$ for a finite-dimensional vector space $V$, one defines the __RTT bialgebra__ $A(R)$ which is as an algebra
free associative algebra $F$ on $n^2$ generators $T^i_j$ (these generators could be viewed as elements of the dual $End^*(V)$) forming a matrix $T = (T^i_j)\in F\otimes End(V)$
modulo the relations packed in a matrix form as
$$
R (T\otimes Id) (Id\otimes T) = (Id\otimes T) (T\otimes Id) R,
$$
where the tensor entries correspond to $V$ factors only (tensor factor in $F$ is not shown).
The coalgebra structure on $A(R)$ is given on generators by $\Delta T^i_j = \sum_k T^i_k\otimes T^k_j$ and $\epsilon T^i_j = \delta^i_j$ (hence it is an example of a [[matrix bialgebra]]). These RTT relations come from [[quantum inverse scattering method]] where a version with spectral parameter appears; [[Yangian]]s and some other related structures satisfy versions of RTT equations. 

To get Hopf algebras one further quotients the RTT algebra by further relations listed for classical series by Faddeev, Reshetikhin and Takhtajan, so obtain quantum function algebras like $Fun(SO_q(n))$ and alike. This is called the __FRT construction__ or FRT approach to [[quantum groups]].

[[Shahn Majid]] complemented this with another algebra $B(R)$ which is paired with $A(R)$ but the pairing is degenerate. Then in an minimal way one finds biideals in $A(R)$ and $B(R)$ such that the quotients become Hopf algebras in a nondegenerate pairing, which may be viewed as the quantum groups of the function and of the universal enveloping algebra type. 

## Examples and variants

* [[quantum linear group]]s 
* a class of generalizations appear as [[face algebra]]s

## Literature

FRT construction is introduced in 

* [[Nikolai Reshetikhin|N. Yu. Reshetikhin]], [[Leon  Takhtajan|L. A. Takhtajan]], [[Ludwig Fadeev|L. D. Faddeev]], _Quantization of Lie groups and Lie algebras_, Algebra i analiz __1__, 178 (1989) (Russian), English transl. Leningrad Math. J. 1
* [[Ludwig Faddeev|L. D. Faddeev]], [[Nikolai Reshetikhin|N. Yu. Reshetikhin]], [[L. A. Takhtajan]], _Quantum Groups. Braid Group, Knot Theory and Statistical Mechanics_, in: Adv. Ser. Math. Phys. __9__, World Sci. 1989, pp. 97--110
* [[Shahn Majid]], _Quasitriangular Hopf algebras and Yang--Baxter equation_, Intern. J. Mod. Phys. __A 05__, No. 01, pp. 1--91 (1990) [doi](https://doi.org/10.1142/S0217751X90000027)

A slight generalization of the original procedure

* [[Jacob Towber]], Sara Westreich, _Hopf algebras constructed by the FRT-construction_, J. Pure & Applied Algebra __213__:5 (2009) 772--782 [doi](https://doi.org/10.1016/j.jpaa.2008.09.012)

A relation between [[reflection equation algebra]]s and  FRT algebras is discussed in 

* Joseph Donin, [[Andrey Mudrov]], _Reflection equation- and FRT-type algebras_,  Czech J Phys __52__, 1201--1206 (2002) [doi](https://doi.org/10.1023/A:1021324718185)

Other articles

* A. Abella, [[Nicolás Andruskiewitsch]], _Compact quantum groups arising from the FRT construction_,  Bol. Acad. Nacional de Ciencias (Córdoba) 63, 15--44 (1999) [pdf](https://www.famaf.unc.edu.ar/~andrus/aa-frt.pdf)


category: algebra

[[!redirects FRT algebra]]
[[!redirects FRT construction]]