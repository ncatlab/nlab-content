
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### In dg-Lie algebras

For $(\mathfrak{g}, [-,-],\partial)$ a [[dg-Lie algebra]] (the [[differential]] of degree -1), a **Maurer-Cartan element** in $\mathfrak{g}$ is

* an element $a \in \mathfrak{g}_1$ of degree -1

* such that the **Maurer-Cartan equation** holds

  $$
    \partial a + \frac{1}{2}[a,a] = 0 
     \,.
  $$

This is a special case of MC elements for [[L-∞ algebras]], which we discuss next.

### In $L_\infty$-algebras
 {#InLInfinityAlgebras}

For $\mathfrak{g}$ an [[L-∞ algebra]] with brackets $[-,\cdots,-]_k$, a Maurer-Cartan element is an element $a \in \mathfrak{g}$ such that

$$
  \sum_{k = 0}^\infty \frac{1}{k!} [a, \cdots, a]_k
  = 
  0
  \,.
$$ 


## Properties
 {#Properties}

### As $L_\infty$-homomorphisms
  {#AsHomomorphisms}

For $\mathfrak{g}$ an [[L-∞ algebra]] and $A$ a [[dg-algebra]], also the [[tensor product]] $A \otimes \mathfrak{g}$ naturally inherits the structure of an [[L-∞ algebra]]. 

Let $\mathfrak{g}$ be of [[finite type]] and write $CE(\mathfrak{g})$ for the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$. Then MC-elements in $A \otimes \mathfrak{g}$ correspond bijectively to dg-algebra homomorphisms $A \leftarrow CE(\mathfrak{g})$:

$$
  MC(A \otimes \mathfrak{g})
  \simeq
  Hom_{dgAlg}(CE(\mathfrak{g}), A)
  \,.
$$

A reference for this is for instance around def. 3.1 in ([Hain](#Hain)).

We unwind in steps how this comes about.

The space of [[graded algebra]] [[homomorphisms]] $A  \leftarrow CE(\mathfrak{g})$ is a subspace of the space of [[linear maps]] of [[graded vector spaces]], and since $\mathrm{CE}(\mathfrak{g})$ is freely
generated as a graded algebra and is of finite type by assumption, this is isomorphic to the
space of grading preserving homomorphisms 

$$
  \mathrm{Hom}_{\mathrm{Vect}[{\mathbb{Z}]}}(\mathfrak{g}^*,A)
$$ 

of linear grading-preserving maps from the graded vector space $\mathfrak{g}^*$ of dual generators to $A$. By the usual relation in $\mathrm{Vect}[\mathbb{Z}]$ for $\mathfrak{g}$ of finite type, this is isomorphic to the space of elements of total degree degree 1 in elements of $A$ tensored with $\mathfrak{g}$:

$$
  (A \otimes \mathfrak{g})_1  
  \simeq
  \mathrm{Hom}_{\mathrm{Vect}[{\mathbb{Z}]}}(\mathfrak{g}^*,A)
  \,.
$$ 

The dg-algebra homomorphism form the subspace of this space

$$
    \mathrm{Hom}_{dgAlg}(\mathrm{CE}(\mathfrak{g}),A)
    \hookrightarrow
    \mathrm{Hom}_{grAlg}(\mathrm{CE}(\mathfrak{g}),A)
    \simeq
    (A \otimes \mathfrak{g})_1
$$ 

on elements that respect the differential. Under the above equivalence this are elements $a$ in $(A \otimes \mathfrak{g})_1$ satisfying a certain condition. By inspection one finds that this condition is precisely the MC equation


$$
  d_A A + \partial a  + [a \cdot_A a]_2 + [a \cdot_A a \cdot_A a ]_3
      + \cdots = 0
      \,.
$$    

For instance if $A = \Omega^\bullet(X)$ is the [[de Rham algebra]] of a [[smooth manifold]] $X$, then $MC(A \otimes \mathfrak{g})$ is the space of flat [[infinity-Lie algebroid-valued differential form|L-∞ algebra valued differential forms]] on $X$. See there for more details.


## Examples


For $\mathfrak{g}$ a [[Lie algebra]], $X$ a [[smooth manifold]], there is a canonical dg-Lie algebra structure on $\Omega^\bullet(X) \otimes \mathfrak{g}$. 

A Maurer-Cartan element is then precisely a [[Lie algebra valued 1-form]] $A$ whose [[curvature]] 2-form vanishes

$$
  d_{dR} A + [A \wedge A] = 0
  \,.
$$

## Range of versions and applications

_Maurer--Cartan equation_ is a name for very many related equations in [[geometry]], [[algebra]], [[deformation theory]], [[category theory]] and [[quantization theory]]. Such equations express for example certain conditions in theory of isometric embedding of submanifolds into a euclidean space ('structure equations', with relations to the Lie groups $O(n)$), invariance of invariant differential forms ([[Maurer-Cartan form|Maurer-Cartan forms]]) on Lie groups, flatness of connections on principal or associated fibre bundles, the solutions in some contexts parametrize infinitesimal deformations, or define [[twisting cochain|twisting cochains]].
In the context of BV-quantization, a Maurer--Cartan equation has the role of classical master equation.

A Maurer--Cartan equation for $A_\infty$-[[A-infinity-algebra|algebra]]s is usually referred to as a _generalized Maurer--Cartan equation_ as it has more summands than the one for [[dg-algebra]]s. In some contexts like $A_\infty$-[[A-infinity-category|categories]], some authors prefer the geometric terminology 'homological vector field' as a datum on a formal geometric space which satisfies a Maurer--Cartan equation. Solutions to Maurer-Cartan equation for a dg- or $A_\infty$ algebra are called Maurer-Cartan elements. 

## Maurer-Cartan and Lie theory

[[Sophus Lie]] considered groups of transformations first and discovered [[Lie algebra]]s only later (letter to Mayer, 1874). He has shown that infinitesimally one can solve the Maurer--Cartan equations for a given set of structure constants of a finite-dimensional Lie algebra. This means that one can construct a neighborhood with either the invariant differential form, or dually the invariant vector fields whose commutator corresponds to the commutator of the Lie algebra. This amounts to integrating the Lie algebra to a [[local Lie group]]. Only much later, Elie Cartan succeeded in proving the global version of integration, that is the Cartan--Lie theorem. J-P. Serre in an influential textbook called the Cartan--Lie theorem the "[[Lie's three theorems|third Lie theorem]]", which became a rather popular term in recent years, though one should correctly call so just the theorem on local solvability of Maurer--Cartan equation.  


## References

The original article:

* [[Ludwig Maurer]], _&#220;ber allgemeinere Invarianten-Systeme_, M&#252;nch. Ber. __18__ (1888), 103-150.

Textbook accounts:

* {#Nakahara03} [[Mikio Nakahara]], Section 5.6.4 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)

* [[Martin Markl]], Def. 3.11 in: _Deformation theory of algebras and their diagrams_, 129 pp, CBMS __116__, AMS 2012 ([ISBN:978-0-8218-8979-4](http://www.ams.org/bookstore-getitem/item=CBMS-116), [toc pdf](https://www.gbv.de/dms/goettingen/721467989.pdf))


* [[Gerd Rudolph]], [[Matthias Schmidt]], Prop. 1.4.9 in: *Differential Geometry and Mathematical Physics Part II. Fibre Bundles, Topology and Gauge Fields*, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))



A MathOverflow entry about Maurer-Cartan forms for Lie groups: [maurer-cartan-form](http://mathoverflow.net/questions/34418/maurer-cartan-form)

On  [[Lie's third theorem]] from the point of view of Maurer--Cartan equations:

* Sigurdur Helgason, Differential geometry, Lie groups, and symmetric spaces

* N. Bourbaki, Lie algebras and lie groups, historical appendix 

* F. Engel, P. Heegaard, Sophus Lie Samlede Avhandliger (Collected works) 

In the generality of [[L-infinity algebras|$L_\infty$-algebras]]:

* [[Martin Doubek]], [[Martin Markl]], [[Petr Zima]], equation (31) in: *Deformation Theory (lecture notes)*, Archivum mathematicum 43(5), 2007, 333-371 ([arXiv:0705.3719](https://arxiv.org/abs/0705.3719))

* [[Andrey Lazarev]], Def. 5.1 in: *Maurer-Cartan moduli and models for function spaces*, Advances in Mathematics Volume 235, 1 March 2013, Pages 296-320 ([arxiv:1109.3715](http://arxiv.org/abs/1109.3715), [doi:10.1016/j.aim.2012.11.009](https://doi.org/10.1016/j.aim.2012.11.009))

* Joseph Chuang, [[Andrey Lazarev]], Def. 1.6 in: *Combinatorics and formal geometry of the master equation*,  Lett. Math. Phys. **103** (2013) 79–112  ([arXiv:1205.5970](https://arxiv.org/abs/1205.5970), [doi:10.1007/s11005-012-0586-1](https://doi.org/10.1007/s11005-012-0586-1)) 

Also around def. 3.1 in

* {#Hain} R. M. Hain, _Twisting cochains and duality between minimal algebras and minimal Lie algebras_, Trans. Amer. Math. Soc. **277** (1983), no. 1, 397--411.

In relation to [[equations of motion]] of [[Yang-Mills theory]] and [[gravity]] (by truncation of [[string field theory]]):

* [[Anton M. Zeitlin]], *Formal Maurer-Cartan Structures: from CFT to Classical Field Equations*, JHEP 0712:098, 2007 ([arXiv:0708.0955](https://arxiv.org/abs/0708.0955))
  
[[!redirects Maurer-Cartan equations]]

[[!redirects Maurer-Cartan equation]]

[[!redirects Maurer-Cartan element]]
[[!redirects Maurer-Cartan elements]]

