# Twisting cochains
* table of contents
{: toc}

## Definition

Let $(C,d_C)$ be a dg-[[coalgebra]] with comultiplication $\Delta$ and $(A,d_A)$ a [[dg-algebra]] with multiplication $\mu$. A __twisting cochain__ is a morphism $\tau:C\to A[1]$ such that the following [[Maurer-Cartan equation]] holds:
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

Apart from original usage for the algebraic models for fibrations, twisting cochains and variants are used in [[homological perturbation theory]] (sometimes abbreviated HPT), rational homotopy theory, deformation theory, study of $A_\infy$-categories, Grothendieck duality on complex manifolds (Toledo-Tong) and so on.  

+--{+ .query}
It is equally true that it is related to 20 more areas like
that one (which is not the central). Brown's paper on twisting cochains, is much earlier than homological perturbation theory. basic idea was to give algebraic models for fibrations. Nowedays you have these things in deformation theory, A-infty, gluing of complexes on varieties, Grothendieck duality on complex manifolds (Toledo-Tong), rational homotopy theory etc. One should either give a fairly balanced view to all applications or not list anything, otherwise it is not fair. This should be done together with massive expansion of [[Maurer-Cartan equation]] what is almost the same topic. The same with literature: Smirnov's book on simplicial and operadic methods in algebraic topology is the most wide reference for twisting cochains and related issues in algebraic topology setup; Keller wrote much and well about this and Lef&#232;vre-Hasegawa thesis (<a href="http://people.math.jussieu.fr/~keller/lefevre/TheseFinale/tel-00007761.pdf">pdf</a>) is very good, and the first reference is E. Brown's paper from 1959. For applications in deformation theory there are many references, pretty good one from dg point of view and using 2-categorical picture of def functors is a trilogy of Efimov, Lunts and orlov on the arXiv. Few days ago Sharygin wrote a long article on twisting cochains on the arXiv, with more specific purposes in index theory. Interesting is the application of Baranovsky on constructing universal enveloping of L infty algebra. -- Zoran

[[Urs Schreiber|Urs]]: concerning the "either give a fairly balanced view to all applications or not list anything", I can see where you are coming from, Zoran, but I would still prefer here to have a little bit of material than to have none. The $n$Lb is imperfect almost everywhere, we'll have to improve it incrementally as we find time, leisure and energy. But it's good that you point out further aspects in a query box, so that we remember to fill them in later.

[[Zoran Skoda]] My experience is that correcting a rambling and unbalanced entries takes more time than writing a new one at a stage when you really work on it. Plus all the communication explaining to others who made original entry which is hastily written. When it becomes very random and biased I stopped enjoying it at all to work on it.

[[Ronnie Brown]] It may not possible for one person to give a "balanced entry" and is certainly not possible for me in this area. On the other hand, this may be endemic to the description of an area of maths for students and research workers. 

An advantage of the Homological Perturbation Lemma (HPL) is that it is an explicit formula, and this has been exploited by various writers, especially Gugenheim, Larry Lambe and collaborators, Huebschmann, and others,  for symbolic computations in homological algebra. It is good of course to have the wide breadth of applications of twisting cochains explained.

For me, an insight of the HPL was the explicit use of the _homotopies_ in  a deformation retract situation to lead to new results. This has been developed to calculate resolutions of groups, where one is constructing inductively a universal cover of a $K(G,1)$ with its contracting homotopy. 

So let us continue to have various individually "unbalanced" points of view explained in this  wiki, to let the readers be informed, and decide.

_Toby_:  Knowing basically nothing about this, I prefer to see various people explain their own perspectives.  Even if they don\'t try to take the work to integrate them.
=--


## References

* Edgar H. Brown Jr. Twisted tensor products. I.  Ann. of Math. (2)  69  (1959) 223--246.

* Kenji Lef&#232;vre-Hasegawa, Sur les A-infini cat&#233;gories, ([pdf](http://people.math.jussieu.fr/~keller/lefevre/TheseFinale/tel-00007761.pdf))

* V. A. Smirnov, Simplicial and operad methods in algebraic topology, Transl. Math. Monogr. 198, AMS 2001 (transl. by G. L. Rybnikov) 

* D. Barnes and L. A. Lambe, A Fixed Point Approach to Homological Perturbation Theory, with Don Barnes, Proc. AMS, 112 (1991), 881--892. 

* K. Hess, The cobar construction: a modern perspective ([pdf](http://sma.epfl.ch/~hessbell/Minicourse_Louvain_Notes.pdf)) (lecture notes from a minicourse at Louvain)

* Alexander I. Efimov, Valery A. Lunts, Dmitri O. Orlov, Deformation theory of objects in homotopy and derived categories, [part 1](http://arxiv.org/abs/math/0702838), [part 2](http://arxiv.org/abs/math/0702839), [part 3](http://arxiv.org/abs/math/0702840))

* N. R. O'Brian, Geometry of twisting cochains.  Compositio Math.  63  (1987),  no. 1, 41--62.

* D. Toledo, Yue Lin L.  Tong, Duality and intersection theory in complex manifolds. I.  Math. Ann.  237  (1978), no. 1, 41--77; II. The holomorphic Lefschetz formula.  Ann. of Math. (2)  108  (1978), no. 3, 519--538.

* Henri Gillet, The $K$-theory of twisted complexes, in "Applications of algebraic $K$-theory to algebraic geometry and number theory", Part I, II (Boulder, Colo., 1983), 159--191, Contemp. Math., 55, AMS 1986. 

* Richard M. Hain, Twisted cochains and duality between minimal algebras and minimal Lie algebras, Trans. AMS 277, 1 (1983) 397--411.


[[!redirects twisting cochain]]
[[!redirects twisting cochains]]
