
## Idea

Dodgson condensation is a method of calculating the [[determinant]] of $n\times n$-matrix by means of a determinant of $(n-1)\times(n-1)$-matrix whose entries are $2\times 2$-minors of the original entry and divided by certain correction. This gives an algorithm for computing determinants of order $n$ in cubic time in $n$.

It is related to [[cluster algebras]] and so called [[T-system]]. Its underlying "Lewis Caroll" identity (also called Desnanot-Jacobi relation) is, as shown by Gelfand et al., a special case of [[Sylvester identity]]. Desnanot-Jacobi relation is sometimes extended to [[octahedron recurrence]].

## Literature

* [wikipedia](https://en.wikipedia.org/wiki/Dodgson_condensation)

The method is from

* C. Dodgson, _Condensation of determinants_, Proc. R. Soc. Lond. __15__ (1866) 150--155

Extra terms cancel thanks to appearance of some [[alternating sign matrix]] alluded to in

* Andrew N. W. Hone, _Dodgson condensation, alternating signs and square ice_, Phil. Trans. R. Soc. A (2006) __364__, 3183--3198 [doi](https://doi.org/10.1098/rsta.2006.1887)

On relation to [[octahedron recurrence]]

* David E. Speyer, _Perfect matchings and the octahedron recurrence_, J. Algebr. Comb. (2007) 25:309--348 [doi](https://doi.org/10.1007/s10801-006-0039-y)

* [[Israel Gelfand]], Sergei Gelfand, [[Vladimir Retakh]], Robert Lee Wilson, _Quasideterminants_, Advances in Mathematics 193 (2005) 56--141 [doi](https://doi.org/10.1016/j.aim.2004.03.018)

* [[Doron Zeilberger]], _Dodgson's determinant-evaluation rule proved by two-timing men and women_, Electron. J. Comb. 4 (2), art. R22 [doi][https://doi.org/10.37236/1337)

* MathOverflow: [geometric-interpretation-of-the-desnanot-jacobi-identity](https://mathoverflow.net/questions/203102/geometric-interpretation-of-the-desnanot-jacobi-identity)

[[Robinson--Schensted--Knuth correspondence]] satisfies the [[octahedron recurrence]]. In the following article this is established with a point of view that RSK correspondence is a [[tropicalization]] of Dodgson condensation rule,

* V.I. Danilov, [[G. A. Koshevoy]], _The octahedron recurrence and RSK-correspondence_, Sém. Lothar. Combin. 54A (2005/07) Art. B54An, 16 pp. (electronic) [published pdf](https://emis.univie.ac.at/journals/SLC/wpapers/s54Adanikosh.pdf) arXiv:[math.CO/0703414](https://arxiv.org/abs/math/0703414)

category: algebra