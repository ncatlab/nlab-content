# Twisting cochains
* table of contents
{: toc}

## Definition

Let $(C,d_C)$ be a dg-[[coalgebra]] with comultiplication $\Delta$ and $(A,d_A)$ a [[dg-algebra]] with multiplication $\mu$. A __twisting cochain__ is a morphism $\tau:C\to A[1]$ such that the following [[Maurer-Cartan equation]] in the [[convolution algebra]] holds:
$$d_A\circ\tau+\tau\circ d_C+\mu\circ(\tau\otimes\tau)\circ\Delta = 0.$$
Notice that the last, perturbation term describes the square $\tau\star\tau$ in the [[convolution]] algebra of homogeneous maps in $\mathrm{Hom}(C,A)$.


## Relation to the adjunction bar-cobar

Let $\mathrm{Cogc}$ be the category of cocomplete dg-co(al)gebras and $\mathrm{Alg}$ the category of dg-algebras. There is a [[bar and cobar construction|bar-construction]] functor $B :\mathrm{Alg}\to\mathrm{Cogc}$ which is a [[adjoint functor|right adjoint]] to the [[bar and cobar construction|cobar-construction]] functor $\Omega:\mathrm{Cogc}\to\mathrm{Alg}$. Starting from a map $f\in\mathrm{Cogc}(C,B A)$, one constructs a twisting cochain $\tau_f$ by postcomposing $f: C\to B A$ by the natural projection $B A\to A[1]$; the [[Maurer-Cartan equation]] for $\tau_f$ translates to saying that $f$ is a chain map, $d_{B A}\circ f = f\circ d_C$. One then replaces $\tau_f$ by the composition of the evident canonical map $\tau_0:\Omega C\to C[-1]$ (called the _canonical twisting cochain_) and $\tau_f[-1]:C[-1]\to A$ to obtain a morphism $f':\Omega C\to A$. The Maurer--Cartan equation for $\tau$ is equivalent also to saying that $f'$ is a chain map, i.e. $d_A\circ f'=f'\circ d_{\Omega C}$.


## Some usages of twisting cochains

A twisting cochain is a datum used to define the [[twisted tensor product]] $L\otimes_\tau M$ for any right $C$-co[[module]] $L$ and any left $A$-module $M$,
as well as the [[twisted module of homomorphisms]] $\mathrm{Hom}_\tau(N,P)$ where $N$ is a left $C$-dg-comodule and $P$ a left $A$-dg-module.

B. Keller and his student Kenji Lef&#232;vre-Hasegawa have shown that [[Koszul duality]] is closely related to twisting cochains. Given a twisting cochain $\tau$, one always has a pair of [[adjoint functor]]s $\otimes_\tau A$ and $\otimes_\tau C$ between the [[derived category]] of modules over $A$ and the coderived category of comodules over $C$ (where $C$ is in $\mathrm{Cogc}$ and the coderived category is just the localization of the category of complexes of comodules at the class of [[weak equivalence]]s, which are by definition those morphisms which became [[quasi-isomorphism]]s after applying $\otimes_{\tau_0}\Omega C$ where $\tau_0:\Omega C\to C[-1]$ is the canonical twisting cochain). This pair of adjoint functors is an [[adjoint equivalence]] iff the composition $\Omega C\to C[-1]$ by $\tau[-1]:C[-1]\to A$ (compare reasoning above) is a quasi-isomorphism. This can also be expressed by saying that the canonical map
$$
A\otimes_\tau C\otimes_\tau A\to A
$$
is a quasiisomorphism. In that case, Keller calls the triple $(C,A,\tau)$ the _Koszul--Moore triple_. Lefevre-Hasegawa's thesis (<a href="http://people.math.jussieu.fr/~keller/lefevre/TheseFinale/tel-00007761.pdf">pdf</a>) asserts that in that case $A$ determines $C$ up to a weak equivalence (defined above) and $C$ determines $A$ up to a quasi-isomorphism. Moreover,
$$H_* C = \mathrm{Tor}^A_*(k,k)\quad \text{and}\quad H^* A = \mathrm{Ext}_C(k,k)$$
where $k$ is the [[ground field]]. Notice that such a formulation of Koszul duality using coalgebras and coderived categories avoids various finiteness conditions present when Koszul duality is phrased as relating algebras to algebras.


## Remarks

Moore was one of the people who studied the subject of 'differential coalgebra', including twisting cochains, in the 1960s and 1970s and gave a survey of the area during his ICM address.

There are variants of the notion of twisting cochain in a variety of other contexts.

A [[twisting function]] is an analogue of a twisting cochain in the context of [[simplicial set]]s.

Apart from original usage for the algebraic models for fibrations, twisting cochains and variants are used in [[homological perturbation theory]] (sometimes abbreviated HPT), rational homotopy theory, deformation theory, study of $A_\infty$-categories, Grothendieck duality on complex manifolds (Toledo-Tong) and so on.  

An old query archived [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=3399&Focus=27888#Comment_27888).

## References

* Edgar H. Brown Jr. Twisted tensor products. I.  Ann. of Math. (2)  69  (1959) 223--246.

* Kenji Lef&#232;vre-Hasegawa, Sur les A-infini cat&#233;gories, ([pdf](http://people.math.jussieu.fr/~keller/lefevre/TheseFinale/tel-00007761.pdf))

* V. A. Smirnov, Simplicial and operad methods in algebraic topology, Transl. Math. Monogr. 198, AMS 2001 (transl. by G. L. Rybnikov) 

* D. Barnes and L. A. Lambe, A Fixed Point Approach to Homological Perturbation Theory, with Don Barnes, Proc. AMS, 112 (1991), 881--892. 

* K. Hess, The cobar construction: a modern perspective ([pdf](http://sma.epfl.ch/~hessbell/Minicourse_Louvain_Notes.pdf)) (lecture notes from a minicourse at Louvain)

* Alexander I. Efimov, Valery A. Lunts, Dmitri O. Orlov, Deformation theory of objects in homotopy and derived categories, [part 1](http://arxiv.org/abs/math/0702838), [part 2](http://arxiv.org/abs/math/0702839), [part 3](http://arxiv.org/abs/math/0702840))

* N. R. O'Brian, Geometry of twisting cochains.  Compositio Math.  63  (1987),  no. 1, 41--62.

* D. Toledo, Yue Lin L.  Tong, _Duality and intersection theory in complex manifolds. I._  Math. Ann.  __237__  (1978), no. 1, 41--77; II. The holomorphic Lefschetz formula.  Ann. of Math. (2) __108__ (1978), no. 3, 519--538.

* [[Henri Gillet]], The $K$-theory of twisted complexes, in "Applications of algebraic $K$-theory to algebraic geometry and number theory", Part I, II (Boulder, Colo., 1983), 159--191, Contemp. Math., 55, AMS 1986. 

* Richard M. Hain, _Twisted cochains and duality between minimal algebras and minimal Lie algebras_, Trans. AMS __277__, 1 (1983) 397--411.


[[!redirects twisting cochain]]
[[!redirects twisting cochains]]
