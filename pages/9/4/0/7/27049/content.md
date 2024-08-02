## Idea

$$ f (n, i, j) f (n-2, i, j) = f (n-1, i-1, j) f (n-1, i + 1, j)
+ \lambda f (n-1, i, j-1) f (n-1, i, j + 1) $$


This is a recurrence obtained in [Robbins, Rumsey 1986](#RobbinsRumsey86) by extension of Desnanot-Jacobi (Lewis-Caroll) identity underlying the recursive computation of determinants called [[Dodgson condensation]] method which is obtained by setting $\lambda = 1$, $f(-1,i,j)=1$  and allowing only $n+i+j = 0\,\,\,(mod\,\,2)$.

## Properties

Solutions are [[Laurent polynomial]]s in $f(0,i,j)$ and $\lambda$. This is an example in [[cluster algebra]] theory.

According to [Robbins, Rumsey 1986](#RobbinsRumsey86), exponents of the $f(0,i,j)$ in any monomial
occurring in a $f(n_0,i_0,j_0)$ form pairs of compatible [[alternating sign matrices]].

Birational [[Robinson--Schensted--Knuth correspondence]] satisfies the octahedron recurrence.

## Literature


Appearance in the study of [[alternating-sign matrices]]

* {#RobbinsRumsey86} [[D. P. Robbins]], H. Rumsey, _Determinants and alternating-sign matrices_, Advances in Math. __62__ (1986) 169--184 <a href="https://doi.org/10.1016/0001-8708(86)90099-X">doi</a>
* J. Propp, _The many faces of alternating-sign matrices, in Discrete Models: Combinatorics, Computation,
and Geometry_, Discrete Math. Theor. Comput. Sci. Proc., AA, Maison Inform. Math. Discrét. (Paris,
2001) 43--58

Providing a major example in [[cluster algebra]]s

* [[Sergey Fomin]], [[Andrei Zelevinsky]], _The Laurent phenomenon_, Adv. in Appl. Math. 28 (2002), no. 2, 119--144
* [[David E. Speyer]], _Perfect matchings and the octahedron recurrence_, J. Algebr. Comb. (2007) 25:309--348 [doi](https://doi.org/10.1007/s10801-006-0039-y) arXiv:[math.CO/0402452](https://arxiv.org/abs/math/0402452)
* V. Danilov, [[Gleb Koshevoy]], _Arrays and the octahedron recurrence_, arXiv:[math.CO/0504299](https://arxiv.org/abs/math/0504200)
* [[André Henriques]], _A periodicity theorem for the octahedron recurrence_, J. Algebraic Comb. 26(1), 1--26 (2007) arXiv:[math.CO/0604289](https://arxiv.org/abs/math/0604289)

Relation to [[crystal bases]]

* [[André Henriques]], [[Joel Kamnitzer]], _The octahedron recurrence and $gl_n$ crystals_, Adv. Math. __206__:1 (2006) 211--249 [doi](https://doi.org/10.1016/j.aim.2005.08.007)

Application to [[Littlewood-Richardson rule]]

* [[Allen Knutson]], [[Terence Tao]], Christopher T. Woodward. _A positive proof of the Littlewood-Richardson rule using the octahedron recurrence_, arXiv:[math.CO/0306274](https://arxiv.org/abs/math/0306274)

[[Robinson--Schensted--Knuth correspondence]] satisfies octahedron recurrence

* V.I. Danilov, G. A. Koshevoy, _The octahedron recurrence and RSK-correspondence_, Sém. Lothar. Combin., 54A (2005/07) Art. B54An, 16 pp. (electronic) [published pdf](https://emis.univie.ac.at/journals/SLC/wpapers/s54Adanikosh.pdf) arXiv:[math.CO/0703414](https://arxiv.org/abs/math/0703414)

On a bijective proof of that fact

* Miriam Farber, Sam Hopkins, Wuttisak Trongsiriwat, _Interlacing networks: Birational RSK, the octahedron recurrence, and Schur function identities_, Journal of Combinatorial Theory __A 133__ (2015) 339--371 [doi](https://doi.org/10.1016/j.jcta.2015.03.001)

category: combinatorics