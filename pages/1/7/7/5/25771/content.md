This article is about the twisted tensor product of associative algebras yielding a new algebra containing the original algebras as subalgebras. For another notion of [[twisted tensor product]] of a dg-algebra with a dg-coalgebra yielding a chain complex see there. While twisting tensor products of dg-algebra with a dg-coalgebra involves a twisting cochain, the twist for algebras here is rather of different nature (sort of distributive law). 

## Definition 

This is the definition for the relative case over a possibly noncommutative ring $R$.

$R$-ring $D$ is a twisted tensor product of an $R$-ring $A$ and $R$-ring $B$ if there are $R$-ring morphisms
$i_A:A\to D$ and $i_B:B\to D$ such that the canonical map
$A\otimes_R B\to D$ given by $a\otimes b\mapsto i(a)i(b)$ is an isomorphism of $R$-bimodules. 

## Constructions

(Suppose $R$ is in the center and bimodules are central.) If $\tau:B\otimes A\to A\otimes B$ is an $R$-linear map such that $\tau(b\otimes 1) = 1\otimes b$ and $\tau(1\otimes a) = a\otimes 1$. This implies that the mixed triangle $\tau\circ(B\otimes\eta_A) = A\otimes\eta_B$ holds; clearly also the distributive laws triangles
$\mu_B\circ(B\otimes\eta_A) = B$ and $\mu_A\circ (\eta_B\otimes A)=A$. A hexagon formula 
$$
\mu_{A\otimes B} = (\mu_A\otimes \mu_B)\circ(A\otimes_R\tau\otimes_R B) : (A\otimes_R B)\otimes (A\otimes_R B)\to
(A\otimes_R B)
$$
defines an associative multiplication iff
$$
\tau\circ(\mu_B\otimes_R\mu_A)= (\mu_A\otimes_R\mu_B)
\circ(A\otimes\tau\otimes B)\circ(\tau\otimes\tau)\circ(B\otimes\tau\otimes A)
$$

The following distributive law pentagons are needed
and are equivalent to the above condition (we skip adorning the relative tensor products):
$$
(A\otimes\mu_B)\circ (\tau\otimes B)\circ(B\otimes \tau)=  \tau\circ(\mu_B\otimes A): B\otimes B\otimes A\to A\otimes B
$$ 
$$
(\mu_A\otimes B)\circ (A\otimes\tau)\circ(\tau\otimes A)= \tau\circ(B\otimes\mu_A): B\otimes A\otimes A\to A\otimes B
$$

## Literature

The present notion is related to factorizations of algebras, hence also to distributive laws in categorical setup. 

Original reference with one hexagon identity instead of two pentagons for associative algebras

* A. Čap, H. Schichl, J. Vanžura, _On twisted tensor products of algebras_, Commun. Alg. __23__ (1995) 4701 [doi](https://doi.org/10.1080/00927879508825496)

The construction for (concrete) twisted algebras with the explicit two pentagon identities for twist appear e.g. (see Eqs. (4.4), (4.5)) in

* [[Piotr Podleś]], [[S. L. Woronowicz]], _Quantum deformation of Lorentz group_, Comm. Math. Phys. __130__(2) (1990) 381--431 [doi](https://doi.org/10.1007/bf02473358)

and the dual version (C) for coalgebras at page 1004 of 

* [[Georges Skandalis]], _Operator algebras and duality_, in: Proceedings of the ICM Kyoto (1990) 997--1009 [pdf](https://www.imj-prg.fr/wp-content/uploads/2020/prix/skandalis1990.pdf)

More elaborate versions for matched products and bicrossproducts in Hopf algebra theory were earlier in

* W. M. Singer, _Extension theory for connected Hopf algebras_, J. Algebra 21 (1972) 1-16
* [[Shahn Majid|S. H. Majid]], _Physics for algebraists: non-commutative and non-cocommutative Hopf algebras by a bicrossproduct construction_, J. Algebra __130__:1 (1990) 17-64 <a href="https://doi.org/10.1016/0021-8693(90)90099-A">doi</a>

In some abstract setups (factorization algebras, factorization monads etc.) more general construction was known beforehands, using distributive laws and further generalizations appear later. 

For dg-algebras including a relative version, $R$-dg-rings, 

* [[Dmitri Orlov]], _Twisted tensor products of DG algebras_, Russ. Math. Surv. 76 (2021) 1146; _Smooth DG algebras and twisted tensor product_, [arXiv:2305.19799](https://arxiv.org/abs/2305.19799)

category: algebra
 