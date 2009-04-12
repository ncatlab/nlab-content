#Definition#
Let $(C,d_C)$ be a dg-[[coalgebra]] with comultiplication $\Delta$ and $(A,d_A)$ a [[dg-algebra]] with multiplication $\mu$. A __twisting cochain__ is a morphism $\tau:C\to A[1]$ such that the following [[Maurer-Cartan equation]] holds:
$$d_A\circ\tau+\tau\circ d_C+\mu\circ(\tau\otimes\tau)\circ\Delta = 0.$$
Notice that the last, perturbation term describes the square $\tau\star\tau$ in the [[convolution]] algebra of homogeneous maps in $\mathrm{Hom}(C,A)$.

#Relation to the adjunction bar-cobar#
Let $\mathrm{Cogc}$ be the category of cocomplete dg-co(al)gebras and $\mathrm{Alg}$ the category of dg-algebras. There is a [[bar and cobar construction|bar-construction]] functor $B :\mathrm{Alg}\to\mathrm{Cogc}$ which is a [[adjoint functor|right adjoint]] to the [[bar and cobar construction|cobar-construction]] functor $\Omega:\mathrm{Cogc}\to\mathrm{Alg}$. Starting from a map $f\in\mathrm{Cogc}(C,B A)$, one constructs a twisting cochain $\tau_f$ by postcomposing $f: C\to B A$ by the natural projection $B A\to A[1]$; the Maurer--Cartan equation for $\tau_f$ translates to saying that $f$ is a chain map, $d_{B A}\circ f = f\circ d_C$. One then replaces $\tau_f$ by the composition of the evident canonical map $\tau_0:\Omega C\to C[-1]$ (called the _canonical twisting cochain_) and $\tau_f[-1]:C[-1]\to A$ to obtain a morphism $f':\Omega C\to A$. The Maurer--Cartan equation for $\tau$ is equivalent also to saying that $f'$ is a chain map, i.e. $d_A\circ f'=f'\circ d_{\Omega C}$.

#Some usages of twisting cochains#

A twisting cochain is a datum used to define the [[twisted tensor product]] $L\otimes_\tau M$ for any right $C$-co[[module]] $L$ and any left $A$-comodule $M$,
as well as the [[twisted module of homomorphisms]] $\mathrm{Hom}_\tau(N,P)$ where $N$ is a left $C$-dg-comodule and $P$ a left $A$-dg-module.

B. Keller and his student Lefevre-Hasegawa have shown that [[Koszul duality]] is closely related to twisting cochains. Given a twisting cochain $\tau$, one always has a pair of [[adjoint functor]]s $\otimes_\tau A$ and $\otimes_\tau C$ between the [[derived category]] of modules over $A$ and the coderived category of comodules over $C$ (where $C$ is in $\mathrm{Cogc}$ and the coderived category is just the localization of the category of complexes of comodules at the class of [[weak equivalence]]s, which are by definition those morphisms which became [[quasi-isomorphism]]s after applying $\otimes_{\tau_0}\Omega C$ where $\tau_0:\Omega C\to C[-1]$ is the canonical twisting cochain). This pair of adjoint functors is an [[adjoint equivalence]] iff the composition $\Omega C\to C[-1]$ by $\tau[-1]:C[-1]\to A$ (compare reasoning above) is a quasi-isomorphism. This can also be expressed by saying that the canonical map
$$
A\otimes_\tau C\otimes_\tau A\to A
$$
is a quasiisomorphism. In that case, Keller calls the triple $(C,A,\tau)$ the _Koszul--Moore triple_. Lefevre-Hasegawa's thesis asserts that in that case $A$ determines $C$ up to a weak equivalence (defined above) and $C$ determines $A$ up to a quasi-isomorphism. Moreover,
$$H_* C = \mathrm{Tor}^A_*(k,k)\quad \text{and}\quad H^* A = \mathrm{Ext}_C(k,k)$$
where $k$ is the ground field. Notice that such a formulation of Koszul duality using coalgebras and coderived categories avoids various finiteness conditions present when Koszul duality is phrased as relating algebras to algebras.

#Remarks#

Moore was one of the people who studied the subject of 'differential coalgebra', including twisting cochains, in the 1960s and 1970s and gave a survey of the area during his ICM address.

There are variants of the notion of twisting cochain in a variety of other contexts.

A [[twisting function]] is an analogue of a twisting cochain in the context of [[simplicial set]]s.

This area is related to [[homological perturbation theory]], often abbreviated to HPT. 

+--{+ .query}
It is equally true that it is related to 20 more areas like
that one (which is not the central). Brown's paper on twisting cochains, is much earlier than homological perturbation theory. basic idea was to give algebraic models for fibrations. Nowedays you have these things in deformation theory, A-infty, gluing of complexes on varieties, Grothendieck duality on complex manifolds (Toledo-Tong), rational homotopy theory etc. One should either give a fairly balanced view to all applications or not list anything, otherwise it is not fair. This should be done together with massive expansion of [[Maurer-Cartan equation]] what is almost the same topic. The same with literature: Smirnov's book on simplicial and operadic methods in algebraic topology is the most wide reference for twisting cochains and related issues in algebraic topology setup; Keller wrote much and well about this and Lefevre-Hasegawa thesis is very good, and the first reference is E. Brown's paper from 1959. For applications in deformation theory there are many references, pretty good one from dg point of view and using 2-categorical picture of def functors is a trilogy of Efimov, Lunts and orlov on the arXiv. Few days ago Sharygin wrote a long article on twisting cochains on the arXiv, with more specific purposes in index theory. Interesting is the application of Baranovsky on constructing universal enveloping of L infty algebra. -- Zoran
=--

#Reference# 

D. Barnes and L. A. Lambe, A Fixed Point Approach to Homological Perturbation Theory, with Don Barnes, Proc. AMS, 112 (1991), 881-892. 
