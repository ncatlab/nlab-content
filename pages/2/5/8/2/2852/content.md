
\tableofcontents

## Idea

Generators of the quantized function algebra $G$ of FRT-type, for example the [[quantum linear groups]] $GL_q(n,k)$, $SL_q(n,k)$ form a matrix $T$ of generators with entries in $G$ and satisfying the matrix identity for the coproduct $\Delta T = T\otimes T$; in fact, $G$ is a [[matrix Hopf algebra]] with basis $T$. 

Using [[quasideterminants]], one can [[matrix decomposition|decompose the matrix]] $T$ as $w U A$, where 

1. $w$ is a [[permutation matrix]], 

1. $U$ [[upper triangular matrix|upper triangular]] unidiagonal 

1. $A$ [[lower triangular matrix|lower triangular]];.

for this one needs to enlarge $G$ to include the inverses which are needed to find the solution. This can be done for example in the quotient skewfield of $G$, but this is suboptimal. Nevertheless in some cases (and some super-analogues) the simple formulas for this decomposition in terms of quantum minors have been studied by Tolstoy, Kulish, Dobrev and others and many times rediscovered by many people and sometimes called quantum Gauss decomposition.

However, as in the classical case, more true meaning can be given to the decomposition $T = wUA$. The following should be true for most [[matrix Hopf algebras]] (except that the Ore localizations should be replaced by Cohn localizations for big examples) and is proved for quantum linear groups. Instead working in the quotient field one can define $n!$ Ore sets $S_w$ generated by certain "flag" quantum minors, so that the equation $T=wUA$ has a solution in the localized algebra $G_w :=S_w^{-1}G$. One defines the quotient Hopf algebra $B$ from $G$ by letting the Hopf ideal generated by the entries of $T$ above diagonal to zero; let the projection be $p:G\to B$. This projection induces a right $B$-coaction $(id\otimes p)\circ\Delta_G:G\to G\otimes B$ on $G$ ("quantum subgroup acts on a quantum group") which has a compatibility property that it uniquely extends to $G_w$ as an algebra map (this geometrically means that $Spec G_w$ is a $Spec B$-invariant subset). The coinvariants of this extended coaction are so-called [[localized coinvariant]]s and they provide a patch on the noncommutative coset space; namely the category of modules over the algebra of localized coinvariants is a localization of the category of quasicoherent sheaves on the quantum coset space; the algebra of localized coinvariants is the smallest invariant subalgebra of $G_w$ containing the entries of matrix $U$ from $g=wUA$, here the invariance is with respect to the natural action of $B$ provided in a natural way using the Gauss decomposition as sketched below. The quantum Gauss decomposition provides the local trivialization of the quantum fiber bundle which could be symbolically denoted $Spec(G)\to Spec(G)/Spec(B)$.  Namely, $G_w$ is isomorphic as a right $B$-comodule algebra to a [[smash product algebra]] $(G_w)^{co H}\sharp B$ with the canonical $B$-coaction, where the isomorphism is induced by the unique homomorphism of algebras (it is nontrivial that such exists!) $\gamma_w:B\hookrightarrow G_w$ such that $b^i_j$ which is the projection of the $(i,j)$-entry of $T$ in $B$ maps to the $(i,j)$-th entry $a^i_j$ of the matrix $A=A_w$ defined by the decomposition $T=wUA$; the left action of $B$ on $(G_w)^{co B}$ is given by $b\triangleright u = \sum\gamma(b_{(1)})u\gamma(S_B b_{(2)})$ where $S_B:B\to B^{cop}_{op}$ is the antipode of $B$. Thus the true meaning of quantum Gauss decomposition is the local trivialization (trivial bundle=smash product) of quantum principal bundle realized by a right $B$-comodule algebra $G$. Locality is in the sense of the cover by coaction-compatible local trivializations. This result is sketched in [Skoda 03](#Skoda03).

## Related concepts

* [[matrix decomposition]]

  * [[Gauss decomposition]]

## Literature

* E. V. Damaskinsky, P. P. Kulish, M. A. Sokolov, _Gauss decomposition for quantum groups and supergroups_, arXiv:[q-alg/9505001](https://arxiv.org/abs/q-alg/9505001)

The fact that global quantum Gauss decomposition gives a covering of a noncommutative principal bundle is stated as theorem 9 in 

* {#Skoda03} Zoran &#352;koda, _Localizations for construction of quantum coset spaces_, [math.QA/0301090](http://front.math.ucdavis.edu/math.QA/0301090), in "Noncommutative geometry and Quantum groups", W.Pusz,  P.M. Hajac, eds. Banach Center Publications vol.61, pp. 265--298, Warszawa 2003. 

The Ore condition for not only $S_w$, but any (multiplicative set) of quantum minors is proved in 

* Zoran &#352;koda, _Every quantum minor generates an Ore set_, International Math. Res. Notices 2008, rnn063-8; [math.QA/0604610](http://arxiv.org/abs/math.QA/0604610). 

In the case of $SL_q(2)$ the local trivialization has been applied to compute the resolution of unity formula for the $SU_q(2)$-coherent states in

* Zoran &#352;koda, _Coherent states for Hopf algebras_,  Letters in Mathematical Physics 81, N.1, pp. 1-17, July 2007. (earlier arXiv version: [math.QA/0303357](http://arxiv.org/abs/math.QA/0303357) ) 

The general picture of actions, coset spaces, compatibility with localizations, localized coinvariants and equivariance in noncommutative algebraic geometry is outlined in 

* Zoran &#352;koda, _Some equivariant constructions in noncommutative algebraic geometry_, Georgian Mathematical Journal 16 (2009), No. 1, 183--202, [arXiv:0811.4770](http://arxiv.org/abs/0811.4770)

The analogous results for the case of multiparametric $GL_{P,Q}(n)$ can be reduced to the one-parametric case using the twisting due Artin and Tate, and reinterpreted for a usage in quantum minor calculations in

* Zoran &#352;koda, _A simple algorithm for extending the identities for quantum minors to the multiparametric case_ [arXiv;0801.4965](http://arxiv.org/abs/0801.4965). 

Other works

* [[S. L. Woronowicz]], S. Zakrzewski, _Quantum Lorentz group having Gauss decomposition property_, Publ. Res. Inst. Math. Sci. __28__ (1992), no. 5, 809--824 [doi](https://doi.org/10.2977/prims/1195167937)

[[!redirects Gauss decompositions]]
