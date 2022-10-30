#Contents#
* table of contents
{:toc}

##Overview##

**Symplectic duality** is the name of a hypothetical duality operation $\mathfrak{M}_0\mapsto \mathfrak{M}^!_0$ on conical [[symplectic singularities.]]  At moment, no rigorous definition exists, though there are a number of conjectured examples and a great number of connections that should tie together dual singularities.

##Correspondence between geometric data##
For $\mathfrak{M}_0$ a conical symplectic singularity, there is an associated [[Harrison homology]] $HP^2( \mathfrak{M}_0)$ which is the base of a universal Poisson deformation of $\mathfrak{M}_0$; this group actually coincides with the quotient by a Coxeter group $W$ (called the **Weyl group** of $\mathfrak{M}_0$) of the $\mathbb{C}$-[[Picard group]] $H$ of a [[Q-factorial|$\mathfrak{Q}$-factorial]] [[terminal singularity|terminalization]] of $\mathfrak{M}_0$ (a [[symplectic resolution]] is an example of such a terminalization, but not all symplectic singularities have resolutions).  Let $H_{\mathbb{Z}}$ denote the Picard group of this variety.

The variety $\mathfrak{M}_0$ also has a finite-dimensional group of [[Hamiltonian vector field|Hamiltonian]] automorphisms commuting with the conical structure.  Let $G$ be a Levi complement of this group, $T$ a maximal torus of $G$ and $\mathbb{W}=N_G(T)/T$ its [[Weyl group]].  For all these pieces of data, let the corresponding object for the (hypothetical) dual be denoted by $(-)^!$

Among the basic properties we expect of $\mathfrak{M}_0$ is 
+-- {: .num_conj}
###### Conjecture 

There are canonical isomorphisms of Coxeter groups $\mathbb{W}\cong W^!$ and $\mathbb{W}^!\cong W$ and 
canonical equivariant  isomorphisms
$\mathfrak{t}\cong H^!$ and $\mathfrak{t}^!\cong H$, inducing isomorphisms $HP^2( \mathfrak{M}_0)\cong\mathfrak{t}^!/\mathbb{W}^!\cong \mathfrak{g}^!/G^!$.

=--

##Quantizations##

Every conical symplectic singularity has a canonical [[deformation quantization]]: a family $A$ of filtered non-commutative algebras over $HP^2( \mathfrak{M}_0)$, each of whose [[associated graded]] is isomorphic to the [[coordinate ring]] $\mathbb{C}[\mathfrak{M}_0]$.  One of the most interesting manifestations of the (hypothetical) duality is the effect it seems to have on the representation theory of these algebras.

Using the isomorphisms above, the choice of a quantization parameter $\lambda$ for $\mathfrak{M}_0$ thus corresponds to a $G^!$-conjugacy class of an element of $\mathfrak{g}^!$, which we can think of as a Hamiltonian vector field on $\mathfrak{M}_0^!$.  There is an element $\xi\in A_\lambda$ which corresponds to the [[Hamiltonian]] of this vector field under associated graded, and thus whose inner action on $A_\la$ is a lift of that of the vector field on functions on $\mathfrak{M}_0$.  

+-- {: .num_defn}
###### Definition 

Category $\mathcal{O}_{\la;\xi}$ for $\xi$ is the category of finitely generated $A_\lambda$-modules where $\xi$ acts locally finitely with generalized eigenvalues whose real parts bounded above.  

=--

Note that the definition of category $\mathcal{O}$ involved the choice of parameters $\lambda$ and $\xi$, and that under duality, the spaces where these parameters live switch places.

+-- {: .num_conj}
###### Conjecture 

There is a choice of "[[Kalb-Ramond field|b-fields]]" $b\in H, b^!\in H^!$ such that for $\lambda\in H_{\mathbb{Z}}, \lambda^!\in H_{\mathbb{Z}}^!$ generic, with $\xi,\xi^!$ the elements of $A^!$ and $A$ associated to these elements as described above,
the categories $\mathcal{O}_{\lambda+b;\xi^!}$ and $\mathcal{O}_{\lambda^!+b^!,\xi}^!$
generate equivalent triangulated subcategories of the [[triangulated category|triangulated categories]] of $A_{\lambda+b}$-modules and $A_{\lambda^!+b^!}$-modules.
=--

[This mathoverflow question](http://mathoverflow.net/questions/51289/) was an attempt to get a rigorous definition of what these b-fields are.

##The smooth case##

+-- {: .num_conj}
###### Conjecture 

The variety $\mathfrak{M}_0$ possesses a symplectic resolution of singularities $\mathfrak{M}$ if and only if $T^!$ acts on $\mathfrak{M}_0^!$ with a unique fixed point.

=--

Thus, if both $\mathfrak{M}_0$ and $\mathfrak{M}_0^!$ possess symplectic resolutions, they also both carry Hamiltonian torus actions with isolated fixed points.  In this case, the simple modules in category $\mathcal{O}_{\la;\xi}$ (for both $\la$ and $\xi$ generic)  are in bijection with $T$-fixed points on $\mathfrak{M}$.

+-- {: .num_conj}
###### Conjecture 

The categories $\mathcal{O}_{\lambda+b;\xi^!}$ and $\mathcal{O}_{\lambda^!+b^!,\xi}^!$ are both [[Koszul]] and Koszul dual to each other.

=--

##Twisting and shuffling##

The categories $\mathcal{O}_{\lambda;\xi}$ (for $\lambda$ generic) carry actions of topologically defined groups.  Let $V\subset \mathfrak{t}_{\mathbb{R}}$ be the subset of the Lie algebra of the compact real form of $T$ consisting of vector fields with isolated fixed points, and let $U\subset H_{\mathbb{R}}$ be the complement of the walls of all the Mori chambers of the $\mathbb{R}$-Picard group.  Then we have an action of $\pi_1(U/W,\la)$ by functors we call **twisting functors** and on $\pi_1(V/\mathbb{W},\xi)$ by  functors we call **shuffling functors**.

+-- {: .num_conj}
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

More generally, given partitions $\la$ and $\mu$, there is a symplectic variety called an **S3-variety** $\mathfrak{X}^\nu_\mu$ which is the preimage in the cotangent bundle of the space of flags of type $\nu$ of the Slodowy slice to the nilpotent orbit with Jordan type $\mu$.  The algebra quantizing this variety is a primitive quotient of the W-algebra for the orbit of Jordan type $\mu$.  In 

* [[Ben Webster]], _Singular blocks of parabolic category $\mathcal{O}$ and
  finite W-algebras_, Journal of Pure and Applied Algebra
Volume 215, Issue 12, December 2011, Pages 2797&#8211;2804 [arXiv:0909.1860](http://front.math.ucdavis.edu/0909.1860) 

it's shown that the category $\mathcal{O}$'s attached to generic integral quantization parameters are in fact singular blocks of parabolic category $\mathcal{O}$'s (in the BGG sense) attached to the same Lie algebra.  

The dual is again an S3 variety $\mathfrak{X}^{\mu}_{\nu}$ where $\mu$ and $\nu$ have switched roles.  The Koszul duality is that proven by BGS (referenced above), after using the equivalence to singular blocks of parabolic category $\mathcal{O}$ mentioned before.  One particularly interesting special case of this is when $\mu=0$, in which case we obtain the duality between cotangent bundle of the space of flags of type $\nu$ and the Slodowy slice to $O_{\mu}$ in the full nilcone.  

###Quiver varieties and affine Grassmannian slices###


##Connections to physics## 


  In this final section, we deal
with a topic which is particularly speculative: the relationship of
these constructions to physics.  While we are not experts on the
constructions occuring in the physics literature which seem to overlap
with some of those given in this paper, enough tantalizing hints of
connections have appeared that we could not in good conscience exclude
them from this paper.

The physical theories which concern us are certain gauge theories in 3
dimensions which carry N=4 supersymmetry; the most important examples
of these are associated to a simple compact Lie group $G$ and a
complex representation $V$ of $G$ and are obtained by dimensional
reduction from 6 dimensional super Yang-Mills, considered for example
in  

* [[N. Seiberg]] and [[E. Witten]], _Gauge dynamics and compactification to three
  dimensions_, The mathematical beauty of physics (Saclay, 1996), Adv. Ser.
  Math. Phys., vol. 24, World Sci. Publ., River Edge, NJ, 1997, pp. 333--366.
  
The fields of this theory include scalar fermions
valued in the adjoint representation $\mg$ and hypermultiplets
corresponding to the representation $V$ (called "the matter content").  

In 

* K. Intriligator and N. Seiberg, _Mirror symmetry in three-dimensional
  gauge theories_, Phys. Lett. B **387** (1996), no. 3, 513--519.

Seiberg and
Intrilligator propose a notion of a "mirror duality" between such
gauge theories.  The most important feature of such a duality is that it interchanges
two spaces attached to them, the Higgs branch and
Coulomb branch of the moduli space of vacua.  These are a pair of
hyperk\"ahler cones defined in the moduli space of vacua by the
vanishing of some of the fields (the adjoint scalars for Higgs, the
hypermultiplets for Coulomb).  After arriving at a
preliminary version of the conjectures discussed above, it
was pointed out (initially by Sergei Gukov) that there is a very
large overlap between the list of examples above and
the known list of Higgs/Coulomb pairs in physics.  For example,  Intriligator and Seiberg have it is shown that an ALE space forms a
  Higgs/Coulomb pair with the
  moduli space of an instanton of the corresponding simply-laced
  Lie group on $\mathbb{R}^2$.

In 

* Jan de~Boer, Kentaro Hori, Hirosi Ooguri, and Yaron Oz, _Mirror symmetry
  in three-dimensional gauge theories, quivers and {D}-branes_, Nuclear Phys. B **493** (1997), no. 1-2, 101--147.

it is shown that 

* Gale
  dual hypertoric varieties are a Higgs/Coulomb pair.
* if an S3-variety is
  presented as a type A quiver variety, its dual is the dual S3-variety,
  also presented as a type $A$ quiver variety.
* all affine
  type quiver varieties are in a Higgs/Coulomb pair with another
  affine quiver variety, with the weight data transforming as in the
  rank/level duality.

These examples strongly suggest that

+-- {: .num_conj}
###### Conjecture 
  If $\mathfrak{M}$ is the Higgs branch of a 3-dimensional $N=4$ supersymmetric
  gauge theory, then the dual $\mathfrak{M}^!$ exists and is the Coulomb branch
  of the same theory (equivalently, the Higgs branch of its mirror).

=--

Unfortunately, this conjecture is not as useful as one might imagine,
as the construction of the Coulomb branch is rather subtle, and we
have found no description of it at the level of precision which would
satisfy a mathematician.  The issue is that while the "classical"
and "quantum" Higgs branches are the same, the Coulomb branch
acquires "quantum corrections."  The classical Coulomb branch is
easy to describe; it is $T^*H/W$ where $H$ is the abstract Cartan
subalgebra of $G$. However, to arrive at the correct conjecture for
$\mathfrak{M}^!$ one must change the hyperk&#228;hler metric on this space, and
thus also its topology, to account for the quantized nature of the
situation.  At the moment, we do not understand how to make these
changes of metric and topology precise, but we are optimistic about
the future.
