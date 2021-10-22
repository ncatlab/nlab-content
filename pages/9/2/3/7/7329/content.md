
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Overview##

**Symplectic duality** is the name of a hypothetical duality operation $\mathfrak{M}_0\mapsto \mathfrak{M}^!_0$ on conical [[symplectic singularities]].  At the moment, no rigorous definition exists, though there are a number of conjectured examples and a great number of connections that should tie together dual singularities.

The reader should be warned that this page and this circle of ideas are works in progress.  At the moment, two papers by [[Tom Braden|Braden]], [[Anthony Licata|Licata]], [[Nicholas Proudfoot|Proudfoot]] and [[Ben Webster|Webster]] that will lay out lots of the ideas and details behind the claims made below are still in preparation;  links will be added when they are ready to be publicly shared.

##Correspondence between geometric data##

For $\mathfrak{M}_0$ a conical symplectic singularity, there is an associated [[Harrison homology]] $HP^2( \mathfrak{M}_0)$ which is the base of a universal [[Poisson deformation]] of $\mathfrak{M}_0$; this group actually coincides with the quotient by a [[Coxeter group]] $W$ (called the **[[Weyl group]]** of $\mathfrak{M}_0$) of the $\mathbb{C}$-[[Picard group]] $H$ of a $\mathfrak{Q}$-[[Q-factorial|factorial]] [[terminal singularity|terminalization]] of $\mathfrak{M}_0$ (a [[symplectic resolution]] is an example of such a terminalization, but not all symplectic singularities have resolutions).  Let $H_{\mathbb{Z}}$ denote the Picard group of this variety.

The variety $\mathfrak{M}_0$ also has a finite-dimensional group of [[Hamiltonian vector field|Hamiltonian]] [[automorphisms]] commuting with the conical structure.  Let $G$ be a [[Levi complement]] of this group, $T$ a [[maximal torus]] of $G$ and $\mathbb{W}=N_G(T)/T$ its [[Weyl group]].  For all these pieces of data, let the corresponding object for the (hypothetical) dual be denoted by $(-)^!$

Among the basic properties we expect of $\mathfrak{M}_0$ is 
+-- {: .num_conjecture}
###### Conjecture 


There are canonical isomorphisms of Coxeter groups $\mathbb{W}\cong W^!$ and $\mathbb{W}^!\cong W$ and 
canonical equivariant  isomorphisms
$\mathfrak{t}\cong H^!$ and $\mathfrak{t}^!\cong H$, inducing isomorphisms $HP^2( \mathfrak{M}_0)\cong\mathfrak{t}^!/\mathbb{W}^!\cong \mathfrak{g}^!/G^!$.

=--

##Quantizations##

Every conical symplectic singularity has a canonical [[deformation quantization]]: a family $A$ of filtered non-commutative algebras over $HP^2( \mathfrak{M}_0)$, each of whose [[associated graded]] is isomorphic to the [[coordinate ring]] $\mathbb{C}[\mathfrak{M}_0]$.  One of the most interesting manifestations of the (hypothetical) duality is the effect it seems to have on the representation theory of these algebras.

Using the isomorphisms above, the choice of a quantization parameter $\lambda$ for $\mathfrak{M}_0$ thus corresponds to a $G^!$-conjugacy class of an element of $\mathfrak{g}^!$, which we can think of as a Hamiltonian vector field on $\mathfrak{M}_0^!$.  There is an element $\xi\in A_\lambda$ which corresponds to the [[Hamiltonian]] of this vector field under associated graded, and thus whose inner action on $A_\lambda$ is a lift of that of the vector field on functions on $\mathfrak{M}_0$.  

+-- {: .num_defn}
###### Definition 

Category $\mathcal{O}_{\lambda;\xi}$ for $\xi$ is the category of finitely generated $A_\lambda$-modules where $\xi$ acts locally finitely with generalized eigenvalues whose real parts bounded above.  

=--

Note that the definition of category $\mathcal{O}$ involved the choice of parameters $\lambda$ and $\xi$, and that under duality, the spaces where these parameters live switch places.

+-- {: .num_conjecture}
###### Conjecture 

There is a choice of "[[Kalb-Ramond field|b-fields]]" $b\in H, b^!\in H^!$ such that for $\lambda\in H_{\mathbb{Z}}, \lambda^!\in H_{\mathbb{Z}}^!$ generic, with $\xi,\xi^!$ the elements of $A^!$ and $A$ associated to these elements as described above,
the categories $\mathcal{O}_{\lambda+b;\xi^!}$ and $\mathcal{O}_{\lambda^!+b^!,\xi}^!$
generate equivalent triangulated subcategories of the [[triangulated category|triangulated categories]] of $A_{\lambda+b}$-modules and $A_{\lambda^!+b^!}$-modules.
=--

[This mathoverflow question](http://mathoverflow.net/questions/51289/) was an attempt to get a rigorous definition of what these b-fields are.

##The smooth case##

+-- {: .num_conjecture}
###### Conjecture 

The variety $\mathfrak{M}_0$ possesses a symplectic resolution of singularities $\mathfrak{M}$ if and only if $T^!$ acts on $\mathfrak{M}_0^!$ with a unique fixed point.

=--

Thus, if both $\mathfrak{M}_0$ and $\mathfrak{M}_0^!$ possess symplectic resolutions, they also both carry Hamiltonian torus actions with isolated fixed points.  In this case, the simple modules in category $\mathcal{O}_{\lambda;\xi}$ (for both $\lambda$ and $\xi$ generic)  are in bijection with $T$-fixed points on $\mathfrak{M}$.

+-- {: .num_conjecture}
###### Conjecture 

The categories $\mathcal{O}_{\lambda+b;\xi^!}$ and $\mathcal{O}_{\lambda^!+b^!,\xi}^!$ are both 
[[Koszul algebra|Koszul]] and [[Koszul dual]] to each other.

=--

Underlying this Koszul duality should be a bijection between fixed points.  This bijection should also appear on the level of equivariant cohomology.

The map of equivariant homology $\scqup{x\in \mathfrak{M}^T} H_2^T(\{x\})\to H_2^T(\mathfrak{M})$ produces an arrangement of subspaces in $ H_2^T(\mathfrak{M})$.

+-- {: .num_conjecture}
###### Conjecture 
The vector spaces $H_2^T(\mathfrak{M})$ and $H_2^{T^!}(\mathfrak{M}^!)$ are canonically dual, with the spaces $H_2^T(\{x\})$ and $H_2^{T^!}(\{x^!\})$ mutual annihilators.
=--

In the paper 

*  [[Tom Braden]], [[Anthony Licata]], [[Nicholas Proudfoot]] and [[Ben Webster]], _Localization algebras and deformations of Koszul algebras_, Selecta Mathematica  **17**, Issue 3 (2011), Page 533-572. [arXiv:arXiv:0905.1335](http://front.math.ucdavis.edu/arXiv:0905.1335)

it's shown that Koszul algebras have a similar duality property when equivariant cohomology rings are replaced with the centers of certain deformations.

##Twisting and shuffling##

The categories $\mathcal{O}_{\lambda;\xi}$ (for $\lambda$ generic) carry actions of topologically defined groups.  Let $V\subset \mathfrak{t}_{\mathbb{R}}$ be the subset of the Lie algebra of the compact real form of $T$ consisting of vector fields with isolated fixed points, and let $U\subset H_{\mathbb{R}}$ be the complement of the walls of all the Mori chambers of the $\mathbb{R}$-Picard group.  Then we have an action of $\pi_1(U/W,\lambda)$ by functors we call **twisting functors** and on $\pi_1(V/\mathbb{W},\xi)$ by  functors we call **shuffling functors**.

+-- {: .num_conjecture}
###### Conjecture 

The Koszul duality between $\mathcal{O}_{\lambda+b;\xi^!}$ and $\mathcal{O}_{\lambda^!+b^!,\xi}^!$ interchanges twisting and shuffling functors.

=--

##Examples##


All conjectured properties are proven for the following examples:

###Hypertoric varieties###
For a [[hypertoric variety]], the quantization is the torus invariant differential operators on a vector space (called the _hypertoric enveloping algebra_) which is constructed from a linear
    algebraic object called a polarized arrangement.   The symplectic dual is the
    hypertoric variety associated to the Gale dual arrangement.  [[Tom Braden|Braden]], [[Anthony Licata|Licata]], [[Nicholas Proudfoot|Proudfoot]] and [[Ben Webster|Webster]] constructed Koszul dual categories conjectured to arise this way in 

*  [[Tom Braden]], [[Anthony Licata]], [[Nicholas Proudfoot]] and [[Ben Webster]], _Gale duality and Koszul duality_, Adv. Math. **225**
  (2010), no. 4, 2002--2049. [arXiv:0806.3256](http://front.math.ucdavis.edu/0806.3256)

and then proved that these categories arise in geometry, compatibly with all conjectures discussed in 

*   [[Tom Braden]], [[Anthony Licata]], [[Nicholas Proudfoot]] and [[Ben Webster]], _Hypertoric category $\mathcal{O}$_, [arXiv:1010.2001](http://front.math.ucdavis.edu/1010.2001)

###Cotangent bundles and S3-varieties### 
For the cotangent bundle $T^*(G/B)$, where $G$ is a
    reductive algebraic group and $B\subset G$ a Borel, the associated quantization is the universal enveloping algebra of $\mathfrak{g}$.  However, our definition of category $\mathcal{O}$ is not actually the same as the BGG category $\mathcal{O}$.  We require semi-simple action of the center, and allow non-semi-simple action  of the Cartan; in usual category $\mathcal{O}$ it is vice versa.  However, one can use a functor constructed by Soergel to construct an equivalence between these categories.   

The symplectic dual to $T^*(G^\vee/B^\vee)$, $G^\vee$ is the Langlands dual of $G$.

Modulo the issues discussed above, the Koszul duality portion of duality is shown in

* [[Alexander Beilinson]], [[Victor Ginzburg]], and [[Wolfgang Soergel]], _Koszul
  duality patterns in representation theory_, J. Amer. Math. Soc. **9**
  (1996), no. 2, 473-527.

and the duality between twisting and shuffling in 

* [[Volodymyr Mazorchuk]], [[Serge Ovsienko]], and [[Catharina Stroppel]], _Quadratic
  duals, Koszul dual functors, and applications_, Trans. Amer. Math. Soc.
  **361** (2009), no. 3, 1129-1172.

More generally, given partitions $\nu$ and $\mu$, there is a symplectic variety called an **S3-variety** $\mathfrak{X}^\nu_\mu$ which is the preimage in the cotangent bundle of the space of flags of type $\nu$ of the Slodowy slice to the nilpotent orbit with Jordan type $\mu$.  The algebra quantizing this variety is a primitive quotient of the W-algebra for the orbit of Jordan type $\mu$.  In 

* [[Ben Webster]], _Singular blocks of parabolic category $\mathcal{O}$ and
  finite W-algebras_, Journal of Pure and Applied Algebra
Volume 215, Issue 12, December 2011, Pages 2797&#8211;2804 [arXiv:0909.1860](http://front.math.ucdavis.edu/0909.1860) 

it's shown that the category $\mathcal{O}$'s attached to generic integral quantization parameters are in fact singular blocks of parabolic category $\mathcal{O}$'s (in the BGG sense) attached to the same Lie algebra.  

The dual is again an S3 variety $\mathfrak{X}^{\mu}_{\nu}$ where $\mu$ and $\nu$ have switched roles.  The Koszul duality is that proven by BGS (referenced above), after using the equivalence to singular blocks of parabolic category $\mathcal{O}$ mentioned before.  One particularly interesting special case of this is when $\mu=0$, in which case we obtain the duality between cotangent bundle of the space of flags of type $\nu$ and the Slodowy slice to $O_{\mu}$ in the full nilcone.  

###Quiver varieties and affine Grassmannian slices###

Perhaps the richest examples of symplectic singularities come from [[quiver varieties]]; these are varieties associated to a pair of weights in the [[weight lattice]] of a [[Kac-Moody algebra]].  The category $\cO$'s of these varieties are derived equivalent to algebras studied in 

* [[Ben Webster]], _Knot invariants and higher representation theory I: diagrammatic and geometric categorification of tensor products_, [arXiv:1001.2020](http://arxiv.org/abs/1001.2020).
* [[Ben Webster]], _Knot invariants and higher representation theory II: the categorification of quantum knot invariants_, [arXiv:1005.4559](http://arxiv.org/abs/1005.4559).

with the shuffling functors coinciding with the R-matrix action from the second paper above, and the twisting functors coinciding with the Chuang-Rouquier braid group action on the category (these statements will be proved in a forthcoming paper of [[Ben Webster]]).

Heuristic considerations suggest that the dual variety to a quiver variety in finite type should be a slice between Schubert cells in the affine Grassmannian of the Langlands dual group.  Ongoing work of [[Joel Kamnitzer]], [[Ben Webster]] and [[Oded Yacobi]] is aimed at understanding the behavior of the quantization referred to above for an affine Grassmannian slice.

##Connections to physics## 


This topicis particularly speculative: the relationship of
these constructions to [[physics]].  

The physical theories which concern us are certain 
[[gauge theories]] in 3
dimensions which carry $N=4$ [[supersymmetry]] (see _[[N=4 D=3 super Yang-Mills theory]]_); the most important examples
of these are associated to a [[compact topological space|compact]] [[simple Lie group]] $G$ and a
complex [[representation]] $V$ of $G$ and are obtained by [[Kaluza-Klein mechanism|dimensional reduction]] from 6 dimensional [[super Yang-Mills theory|super Yang-Mills]], considered for example in  

* [[Nathan Seiberg]] and [[Edward Witten]], _Gauge dynamics and compactification to three dimensions_, The mathematical beauty of physics (Saclay, 1996), Adv. Ser.
  Math. Phys., vol. 24, World Sci. Publ., River Edge, NJ, 1997, pp. 333--366. ([arXiv:hep-th/9607163](http://arxiv.org/abs/hep-th/9607163))
  
The fields of this theory include scalar fermions
valued in the [[adjoint representation]] $\mg$ and hypermultiplets
corresponding to the representation $V$ (called "the matter content").  

In 

* [[Ken Intriligator]], [[Nathan Seiberg]], _Mirror symmetry in three-dimensional gauge theories_, Phys. Lett. B **387** (1996), no. 3, 513--519 ([arXiv:hep-th/9607207](http://arxiv.org/abs/hep-th/9607207))

Seiberg and Intrilligator propose a notion of a "[[mirror symmetry|mirror duality]]" between such [[gauge theories]] ([[3d mirror symmetry]]).  The most important feature of such a duality is that it interchanges two spaces attached to them, the [[Higgs branch]] and [[Coulomb branch]] of the [[moduli space]] of [[vacua]].  These are a pair of hyperk&#228;hler cones defined in the [[moduli space]] of [[vacua]] by the vanishing of some of the fields (the adjoint scalars for Higgs, the hypermultiplets for Coulomb).  After arriving at a preliminary version of the conjectures discussed above, it was pointed out (initially by [[Sergei Gukov]]) that there is a very large overlap between the list of examples above and the known list of Higgs/Coulomb pairs in physics.  For example,  Intriligator and Seiberg have shown that an [[ALE space]] forms a Higgs/Coulomb pair with the moduli space of an [[instanton]] of the corresponding simply-laced Lie group on $\mathbb{R}^2$.

In 

* [[Jan de Boer]], [[Kentaro Hori]], [[Hirosi Ooguri]], and [[Yaron Oz]], _Mirror symmetry in three-dimensional gauge theories, quivers and D-branes_, Nuclear Phys. B **493** (1997), no. 1-2, 101--147.

it is shown that 

* Gale dual hypertoric varieties are a Higgs/Coulomb pair.

* if an S3-variety is presented as a type A quiver variety, its dual is the dual S3-variety, also presented as a type $A$ quiver variety.

* all affine type quiver varieties are in a Higgs/Coulomb pair with another affine quiver variety, with the weight data transforming as in the rank/level duality.

These examples strongly suggest that

+-- {: .num_conjecture}
###### Conjecture 
  If $\mathfrak{M}$ is the [[Higgs branch]] of a [[N=4 D=3 super Yang-Mills theory]], then the dual $\mathfrak{M}^!$ exists and is the [[Coulomb branch]] of the same theory (equivalently, the Higgs branch of its [[mirror symmetry|mirror]]).

=--

Unfortunately, this conjecture is not as useful as one might imagine, as the construction of the Coulomb branch is rather subtle, and we have found no description of it at the level of precision which would satisfy a mathematician.  The issue is that while the "classical"
and "quantum" Higgs branches are the same, the Coulomb branch acquires "quantum corrections."  The classical Coulomb branch is easy to describe; it is $T^*H/W$ where $H$ is the abstract Cartan
subalgebra of $G$. However, to arrive at the correct conjecture for
$\mathfrak{M}^!$ one must change the hyperk&#228;hler metric on this space, and
thus also its topology, to account for the quantized nature of the
situation.  At the moment, we do not understand how to make these
changes of metric and topology precise, but we are optimistic about
the future.

## References

A recent seminar with a list of resources is 

* [GRT learning seminar winter 2020: Symplectic Duality](http://www.math.toronto.edu/dbutson/ls20.html)

A survey is in

* [[Nick Proudfoot]], _[research statement](http://pages.uoregon.edu/njp/research.pdf)_

A workshop dealing with related topics is

* [Young Researchers Workshop on Higher Algebraic and Geometric Structures: Modern Methods in Representation Theory](http://www.fields.utoronto.ca/programs/scientific/11-12/reptheory2012/), May 7-9, 2012
Hosted by the Fields Institute, at the Univerity of Toronto 

