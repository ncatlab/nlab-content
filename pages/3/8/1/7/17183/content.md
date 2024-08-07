
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents


## Idea


__Quantum linear semigroups__ are [[bialgebras]] which are [[deformations]] of bialgebras of [[coordinate functions]] on the [[groups]] of $n\times n$ [[invertible matrices]] for some $n \in \mathbb{N}$. They belong to the class of [[matrix bialgebras]]. 

The usual notation for the one-parametric version is $\mathcal{O}(M_q(n))$ or sometimes simply $\mathcal{M}_q(n)$.

Suppose we are given $n\times n$ matrices $P = (p_{ij})$ and 
$Q = (q_{ij})$ with invertible entries in the ground field $F$, 
for which there exist $q$ such that  
$$
  p_{ij} q_{ij} = q^2, q_{ij} = q^{-1}_{ji},\,\,\,\,\,i \lt j,\,\,and \,\,\,\,\,\,
q_{ii} = p_{ii},\,\,\,\,\,\,\, for\,\,\, all\,\,\,\, i.
$$ 

The multiparametric quantized matrix bialgebra (synonym:
multiparametric quantum linear semigroup) $\mathcal{O}(M_{P,Q}(F,n)):= F \langle T^i_j , i,j = 1,\ldots, n\rangle/I$,
where $I$ is the ideal spanned by the relations
\[\array{
T^k_i T^k_j = q_{ij} T^k_j T^k_i, & i \lt j \\
T^k_i T^l_i = p_{kl} T^l_i T^k_i, & k \lt l \\
q_{ij} T^k_j T^l_i = p_{kl} T^l_i  T^k_j, & i\lt j,\,\,\,\,k\lt l \\
T^k_i T^l_j - q_{ij} q^{-1}_{kl} T^l_j T^k_i
= (q_{ij}-p_{ij}^{-1}) T^k_j T^l_i,& i\lt j,\,\,\,\,k\lt l
}\]
$\mathcal{M} = \mathcal{O}(M_{P,Q}(F,n))$ is a bialgebra 
with respect to the "matrix" comultiplication
which is the unique algebra homomorphism $\Delta : \mathcal{M} 
\to\mathcal{M} \otimes\mathcal{M}$
extending the formulas which are written in the matrix form as
$\Delta T^i_j = \sum T^i_k \otimes T^k_j$ with 
counit $\epsilon T^i_j = \delta^i_j$ (Kronecker delta). This means that it is
a matrix bialgebra with basis $\{T^i_j\}_{i,j=1,\ldots,n}$, in fact a free matrix bialgebra over $F$. 

In these conventions, the 1-parametric version $\mathcal{O}(M_q(F))$ is obtained as
a special case when $P = Q$ and
$q_{ij} = q$ for $i \lt j$ and $q_{ij} = q^{-1}$ for $i \gt j$.

__Quantum linear groups__ are [[Hopf algebras]] which are quantum deformations of Hopf algebras of coordinate functions on the [[general linear group]] or [[special linear group]]. There exist one parametric and many parametric versions as well as super analogues. They belong to the class of [[matrix Hopf algebra]]s.

The usual notation for one-parametric versions is $\mathcal{O}(GL_q(n))$, $\mathcal{O}(SL_q(n))$ and variants thereof.



## Related entries

* [[quantum group]]

* [[quantum Gauss decomposition]]

* [[quantized function algebra]]

* [[general linear group]]

* [[quantum determinant]]


## Literature

* [[Yu. I. Manin]], _Quantum groups and non-commutative geometry_, CRM, Montreal 1988.
* [[Yu. I. Manin]], _Multiparametric quantum deformation of the general linear supergroup_, Comm. Math. Phys. __123__ (1989) 163--175.
* B. Parshall, J.Wang, _Quantum linear groups_, Mem. Amer. Math. Soc. 89(1991), No. 439, vi+157 pp. 
* E. E. Demidov, _Multiparameter quantum deformations
of the group $GL(n)$_, (Russian) Uspehi Mat. Nauk 46 (1991), no. 4 (280) 147--148; translation in Russian Math. Surveys 46 (1991) no. 4, 169--171.
* M. Hashimoto, T. Hayashi, _Quantum multilinear algebra_, Tohoku Math. J. __44__ (1992) 471--521 [doi](https://doi.org/10.2748/tmj/1178227246)
* [[Michael Artin]], W. Schelter, [[John Tate]], _Quantum deformations of $GL_n$_, Commun. Pure Appl. Math. XLIV, 879--895 (1991)
* [[Zoran Škoda]], _Localizations for construction of quantum coset spaces_, [math.QA/0301090](http://front.math.ucdavis.edu/math.QA/0301090), in "Noncommutative geometry and Quantum groups", W.Pusz, P.M. Hajac, eds. Banach Center Publications __61__, pp. 265--298, Warszawa 2003.
* Z. &#352;koda, _Every quantum minor generates an Ore set_,
International Math. Res. Notices 2008, rnn063-8; 
[math.QA/0604610](http://arxiv.org/abs/math/0604610)
* Karel Casteels, Si&#226;n Fryer, _From restricted permutations to Grassmann necklaces and back again_, Algebras and Representation Theory 20, 895--921 (2017). [doi](https://doi.org/10.1007/s10468-017-9668-1) [arxiv/1511.06664](https://arxiv.org/abs/1511.06664)
* Hechun Zhang, R.B.Zhang, _Dual canonical bases for the quantum special linear group and invariant subalgebras_, Letters in Mathematical Physics (2005) __73__:165--181 [doi](https://doi.org/10.1007/s11005-005-0015-9); _Dual canonical bases for the quantum general linear supergroup_, J. Algebra __304__ (2006) 1026--1058 [doi](https://doi.org/10.1016/j.jalgebra.2005.11.023)
* Hans Plesner Jakobsen, Hechun Zhang, _The center of the quantized matrix algebra_, J. Algebra __196__:2 (1997) 458-474 [doi](https://doi.org/10.1006/jabr.1997.7121)
* [[K. R. Goodearl]], E.S. Letzter, _Prime factor algebras of the coordinate ring of quantum matrices_, Proc. Amer. Math. Soc. __121__ (1994) 1017--1025 [doi](https://doi.org/10.1090/S0002-9939-1994-1211579-1)
* S. Launois, T. H. Lenagan, B. M. Nolan, _Total positivity is a quantum phenomenon: the Grassmannian case_, Memoirs of the Amer. Math. Soc. 1448 (2023) 123 p. 

[[!redirects quantum linear groups]]
