## Idea

The classical Capelli identity is an equality of differential operators written in a form roughly
resembling the classical identity $det(A B) = det(A) det(B)$ where however at the right hand side are true determinants of commutative entries and at the left side is a column determinant whose entries are (corrections of) non-commuting vector fields, so called polarization operators. 

There are numerous generalizations.

## Statement

Define the polarization operators $E_{i j} = \sum_{a=1}^n x_{i a}\frac{\partial}{\partial x_{j a}}$ for $i,j\in\{1,\ldots n\}$. These operators satisfy the commutation relations of the Lie algebra $gl(n)$.

Define the column determinant of a matrix $A = (a_{i j})_{i,,j=1,\ldots,n}$ with not necessarily commuting entries 
$$
det_c(A) = \sum_{\sigma\in\Sigma(n)}sign(\sigma) 
a_{\sigma(1)1}a_{\sigma(2)2}\cdots a_{\sigma(n)n}
$$
This is in generally an ill-behaved object of comparing to the case of the [[determinant]] of a matrix with commuting entries; in particular the other formulas for a determinant give different results in noncommutative case.
Then
$$
det_c((E_{i j} - (n-i)\delta_{i j})_{i j}) = det((x_{i j})_{i j}) det((\frac{\partial}{\partial x_{i j}})_{i j})
$$

## Literature 

* wikipedia [Capelli's identity](https://en.wikipedia.org/wiki/Capelli%27s_identity)

A treatment in terms of [[quasideterminant]]s is in 3.7 of

* [[Israel Gelfand]], Sergei Gelfand, [[Vladimir Retakh]], Robert Lee Wilson, _Quasideterminants_, Advances in Mathematics 193 (2005) 56--141 [doi](https://doi.org/10.1016/j.aim.2004.03.018)

* [[Bertram Kostant]], Siddharta Sahi, _Jordan algebras and Capelli identities_, Invent. math. __112__ (1993) 657--664

> The purpose of this paper is to establish a connection between semisimple Jordan algebras and certain invariant differential operators on symmetric spaces; and to prove
an identity for such operators which generalizes the classical Capelli identity.

* [[Roger Howe]], T. Umeda, _The Capelli identity, the double commutant theorem, and multiplicity-free actions_, Math. Ann. __290__ (1991) 565--619
* E. Mukhin, V. Tarasov, [[A. Varchenko]], _A generalization of the Capelli identity_, [pdf](https://math.nyu.edu/~tschinke/.manin/final/mukhin/mukhin.pdf)
* Maxim Nazarov, _Yangians and Capelli identities_, in: Kirillov’s seminar on representation theory, Amer. Math. Soc. Translations: 181 (Series 2) 1998 [doi](https://doi.org/10.1090/trans2/181/05) 
* Dimitri Gurevich, Varvara Petrova, Pavel Saponov, _Matrix Capelli identities related to reflection equation algebra_, J. Geom. Phys. __179__ (2022) 104606 [doi](https://doi.org/10.1016/j.geomphys.2022.104606) 

category: algebra

[[!redirects Cappeli's identity]]