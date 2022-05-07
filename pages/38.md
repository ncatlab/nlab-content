
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Classical Lie theory and beyond

__Lie theory__ (wikipedia: [Lie theory](http://en.wikipedia.org/wiki/Lie_theory)) is the study of [[Lie groups]], [[Lie algebras]], their actions as groups of transformations, their representations, their 
cousins ([[Chevalley group]]s, [[quantum group]]s, Banach Lie groups, [[Lie bialgebra]]s, [[universal enveloping algebra]]s)
and categorifications (higher Lie groups, $L_\infty$-[[L-infinity-algebra|algebras]] etc.), including horizontal: [[Lie groupoid]], [[Lie algebroid]], $L_\infty$-[[L-infinity-algebroid|algebroid]]. 

[[Lie group]] is a [[group|groups]] [[internalization|internal to]] [[Diff]]. The [[Lie algebras]] over real or complex numbers appear as the linearization of real or complex Lie groups; the infinitesimal version of Lie groups are [[local Lie group]]s. The relation between real Lie algebras and real Lie groups was established by [[Lie's three theorems]] and the study of this correspondence is the classical Lie theory in narrow sense. 

In a categorical context there are the usual two generalization of Lie groups: the [[horizontal categorification]] -- or oidification -- which adds _more objects_ and leads to _Lie groupoids_; and the [[vertical categorification]] which adds _higher morphisms_ and leads to $\infty$-Lie groups and $\infty$-Lie groupoids. This is described below.

In the course of these categorifications one usually finds that working [[internalization|internal to]] $Diff$ is too restrictive for many purposes. Therefore higher Lie theory is often considered internal to [[generalized smooth space|generalized smooth spaces]].


## Lie groupoids versus Lie algebroids

[[horizontal categorification|Oidification]] leads from Lie groups to [[Lie groupoid|Lie groupoids]]
and from [[Lie algebra|Lie algebras]] to 
[[Lie algebroid|Lie algebroids]].

When it was found that Lie algebroids integrate to Lie groupoids by mapping paths into them, not only a "well known" but apparently also well forgotten way to integrate Lie algebras by means of paths was rediscovered, but also the idea to integrate higher Lie algebroids by mapping higher dimenmsional paths into them was clearly suggested.



## Higher Lie theory: $\infty$-Lie groupoids and $L_\infty$-algebroids

bla bla bla 
[[infinity-groupoid]] bla bla bla
[[Lie infinity-groupoid]] bla bla bla
[[Lie infinity-algebroid]] bla bla bla

## Related entries

Smooth spaces and smooth groups: [[homogeneous space]], [[Lie group]], [[Lie groupoid]], [[Morita equivalence]] of Lie groupoids, [[NQ-supermanifold]], [[orbifold]], [[differentiable stack]], [[generalized smooth algebra]], [[generalized smooth space]], [[Lie infinity-groupoid]], [[local Lie group]], [[Poisson-Lie group]], [[symmetric space]]

Algebraic cousins and tools: [[algebraic group]]
[[Chevalley-Eilenberg algebra]], [[CoDGCA]], [[coalgebra]], [[L-infinity-algebra]], [[Lie algebra]], [[Lie algebroid]], [[Lie infinity-algebroid]],
[[universal enveloping algebra]], [[PBW theorem]], [[Ado's theorem]], [[Hausdorff series]], [[Duflo isomorphism]], [[coexponential map]], [[free graded co-commutative coalgebra]], [[quantum group]], [[Chevalley group]], [[Lie bialgebra]], [[Leibniz algebra]]

Geometry on Lie groups and related spaces: [[integration over supermanifolds]], [[space and quantity]], [[superdifferential form]], [[volume of a Lie groupoid]], [[Maurer-Cartan form]], [[invariant vector field]] 

Lie theory in narrow sense (Lie group(oid)s vs. algebr(oid)s): [[tangent Lie algebra]], [[tangent Lie algebroid]], [[Lie integration]], [[Lie theory for stacky Lie groupoids]], [[Lie's three theorems]], [[exponential map]]

Applications where Lie objects appear: [[matrix theory]], [[connection on a bundle]], [[BRST complex]], [[BV theory]],  [[examples for Lagrangian BV]], [[fundamental groupoid]], [[geometric quantization]], [[invariant theory]], [[representation theory]], [[conformal field theory]]

There are also many special kinds of [[Lie groups]] ([[semisimple Lie group|semisimple]], solvable, nilpotent, [[general linear group|general linear]], [[special linear group|special linear]], [[metaplectic group]], [[unitary group]] etc.), kinds of [[Lie algebras]] ([[Kac-Moody algebra|Kac-Moody]], [[semisimple Lie algebra|semisimple]], [[affine Lie algebra|affine]] Lie algebras, [[Virasoro Lie algebra]]...), structure notions on Lie groups and algebras (maximal torus, [[Killing form]], Dynkin diagram, root system, Cartan subalgebra, Gauss decomposition, Bruhat decomposition...),  and versions and tools of [[representation theory]] ([[Young diagram]], [[symmetric function]], [[Schur function]], [[combinatorial representation theory]], [[geometric representation theory]], weight lattice, [[induced representation]], [[Verma module]], [[Langlands program]]), see those entries.



## References

### General
 

* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993


* {#HilgertNeeb12} Joachim Hilgert, [[Karl-Hermann Neeb]], _Structure and Geometry of Lie Groups_, Springer Monographs in Mathematics, Springer-Verlag New York, 2012 ([doi:10.1007/978-0-387-84794-8](https://link.springer.com/book/10.1007/978-0-387-84794-8))


* {#Okounkov18} [[Andrei Okounkov]], _New worlds for Lie theory_, talk at [ICM 2018](http://www.icm2018.org/portal/en/home) ([pdf](http://www.math.columbia.edu/~okounkov/icm.pdf))

### Lie 1-groupoids vs. Lie algebroids

The study of Lie theory of Lie groupoids and Lie algebroids was notably motivated by Alan Weinstein's studies of [[geometric quantization]] of [[Poisson manifold|Poisson manifolds]], as well as by [[Kirill Mackenzie|Kirill Mackenzie's]] work. 

The canonical review for the integration theory of Lie algebroids (and hence for Lie algebras by the **path integration method**) is:

* Marius Crainic, Rui Loja Fernandes, _Lectures on Integrability of Lie Brackets_, ([arXiv](http://aps.arxiv.org/abs/math.DG/0611259),[blog](http://golem.ph.utexas.edu/category/2008/05/integrability_of_lie_brackets.html)).

This focuses on integration to [[Lie groupoid|Lie groupoids]] proper, i.e. to integration internal to manifolds. In contrast to Lie algebras, not every Lie algebroid integrates to such a proper [[Lie groupoid]], though: the space of morphisms of the Lie groupoid is a quotient of paths in the Lie algebroid by Lie algebroid homotopies, and this quotient may not exist as a manifold. (Crainic and Fernandes [discuss](http://aps.arxiv.org/abs/math.DG/0611259) the obstruction in detail.) But the quotient of course always exists as a [[weak quotient]] or [[homotopy quotient]] or [[stacky quotient]] itself. The result of realizing the space of morphisms of the integrated Lie algebroid as such a stacky quotient has been studied by [Chenchang Zhu](http://chenchangzhu.blogspot.com/):
[[Lie theory for stacky Lie groupoids]]

### Higher categorical

See at _[[Lie integration]]_.



[[!redirects Lie Theory]]

category: Lie theory
