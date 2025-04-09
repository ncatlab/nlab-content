
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _Hopf algebra_ is an abstraction of the properties of

* the [[group algebra]] of a [[group]];

* the [[algebra of functions]] on a finite group, and more generally, the algebra of regular functions on an affine algebraic $k$-group;

* the [[universal enveloping algebra]] of a [[Lie algebra]],

where not only the [[associative algebra]] structure is remembered, but also the natural [[coalgebra]] structure, making it a [[bialgebra]], as well as the algebraic structure induced by the [[inverse]]-operation in the group, called the _[[antipode]]_.

More intrinsically, a Hopf algebra structure on an [[associative algebra]] is precisely the structure such as to make its [[category of modules]] into a [[rigid monoidal category]] equipped with a [[fiber functor]] -- this is the statement of _[[Tannaka duality]]_ for Hopf algebras.

Hopf algebras and their generalization to [[Hopf algebroids]] arise notably as [[groupoid convolution algebras]]. Another important source of Hopf algebras is [[combinatorics]], see at _[[combinatorial Hopf algebras]]_.

There is a wide variety of variations of the notion of Hopf algebra, relaxing [[properties]] or adding [[structure]]. Examples are _[[weak Hopf algebras]]_, _[[quasi-Hopf algebras]]_, _([[quasi-triangular Hopf algebra|quasi]]-)[[triangular Hopf algebras]]_, _[[quantum groups]]_, _[[hopfish algebras]]_ etc. Most of these notions are systematized via [[Tannaka duality]] by the properties and structures on the coresponding [[categories of modules]], see at _[Tannaka duality](#TannakaDuality)_ below.


## Definition

+-- {: .num_defn #Antipode}
###### Definition
**([[antipode]])**

A $k$-[[bialgebra]] $(A,m,\eta,\Delta,\epsilon)$ with multiplication $m$, comultiplication $\Delta$, unit $\eta \colon k\to A$ and counit $\epsilon \colon A\to k$ is called a **Hopf algebra** if there exists a $k$-[[linear function]]

$$
  S \colon A \longrightarrow A
  \,,
$$

then called the **[[antipode]]** or **coinverse**, such that 

$$
  m\circ(\mathrm{id}\otimes S)\circ \Delta 
  \;=\; 
  m\circ(S\otimes\mathrm{id})\circ\Delta = \eta\circ\epsilon
$$ 

(as a map $A\to A$). 

=--

+-- {: .num_defn #InvolutiveHopfAlgebra}
###### Definition

If the antipode of a Hopf algebra (Def. \ref{Antipode}) is an [[anti-involution]], in that $S \circ S = id$, then one speaks of an *[[involutive Hopf algebra]]*.

=--

+-- {: .num_remark}
###### Remark

If an antipode exists then it is unique, just the way that if inverses exist in a [[monoid]] then they are unique. One sometimes prefers to have a __skew-antipode__ $\tilde{S}$ such that $h_{(2)}\tilde{S}(h_{(1)}) = \tilde{S}(h_{(2)}) h_{(1)} = 
(\eta\circ\epsilon) (h)$. If $S$ is an invertible antipode then $\tilde{S} - S^{-1}$ is a skew-antipode. $H$ is a bialgebra with a skew-antipode iff $H^{op}$ (the same vector space, opposite product, the same coproduct) is a Hopf algebra.

The unit of a Hopf algebra is a [[grouplike element]],  hence $S(1)1=1$, therefore $S(1)=1$. By linearity of $S$ this implies that $S\circ\eta\circ\epsilon = \eta\circ\epsilon$.

=--

+-- {: .num_prop #AntipodeIsAnAntihomomorphism}
###### Proposition

The antipode is an [[anti-homomorphism]] both of algebras and coalgebras (i.e. a homomorphism $S \colon A\to A^{cop}_{op}$). 

In particular, an [[involutive Hopf algebra]] (Def. \ref{InvolutiveHopfAlgebra}) is a [[star-algebra]].

=--

+-- {: .proof}
###### Proof (algebra part)
In [[Sweedler notation]], for any $g,h\in A$, 

$$S((h g)_{(1)}) (h g)_{(2)} = \epsilon(h g)$$ 

$$S((h g)_{(1)}) h_{(2)}g_{(2)} = \epsilon(h)\epsilon(g)$$

$$S((h g)_{(1)}) h_{(2)}g_{(2)} S g_{(3)} S h_{(3)} = \epsilon(h_{(1)})\epsilon(g_{(1)}) S g_{(2)} S h_{(2)}$$

$$S(h_{(1)}g_{(1)}) \epsilon(h_{(2)})\epsilon(g_{(2)}) = (S g) (S h)$$

$$S(h_{(1)}\epsilon(h_{(2)})g_{(1)}\epsilon(g_{(2)})) = (S g)(S h)$$

Therefore $S(h g) = (S g) (S h)$.

For the coalgebra part, notice first that $\epsilon(h)1\otimes 1 = \tau\circ\Delta(\epsilon(h)1)=\tau\circ\Delta(S h_{(1)}h_{(2)})$. Expand this as 

$$ (S h_{(1)}\otimes S h_{(2)})(h_{(4)}\otimes h_{(3)}) = ((S h_{(1)})_{(2)}\otimes (S h_{(1)})_{(1)})(h_{(4)}\otimes h_{(3)})$$

$$ (S h_{(1)}\otimes S h_{(2)})(h_{(4)}\otimes h_{(3)}) (S h_{(5)}\otimes S h_{(6)}) = ((S h_{(1)})_{(2)}\otimes (S h_{(1)})_{(1)})(h_{(3)}\otimes h_{(2)})(S h_{(4)}\otimes S h_{(5)})$$

$$ ((S h_{(1)}\otimes S h_{(2)})\epsilon(h_{(3)}) = ((S h_{(1)})_{(2)}\otimes (S h_{(1)})_{(1)})(1\otimes\epsilon(h_{(2)}))$$

$$ ((S h_{(1)}\otimes S h_{(2)})\epsilon(h_{(3)}) = (\tau\circ\Delta)(S h_{(1)})(1\otimes\epsilon(h_{(2)})1) = (\tau\circ\Delta)(S h_{(1)}\epsilon(h_{(2)}))$$

$$ (S h_{(1)}\otimes S h_{(2)})=(\tau\circ\Delta)(S h) = (S h)_{(2)}\otimes (S h)_{(1)}.$$
=--


The axiom that must be satisfied by the antipode looks like a $k$-linear version of the identity satisfied by the inverse map in a group bimonoid: taking a group element $g$, duplicating by the diagonal map $\Delta$ to obtain $(g,g)$, taking the inverse of either component of this ordered pair, and then multiplying the two components, we obtain the identity element of our group.

Just as an [[associative unital algebra|algebra]] is a [[monoid]] in [[Vect]] and a [[bialgebra]] is a [[bimonoid]] in $Vect$, a Hopf algebra is a [[Hopf monoid]] in $Vect$.


+-- {: .num_remark}
###### Remark
**Caution: convention in topology**

In [[algebraic topology]], it is common to define Hopf algebras without mentioning the antipode, since in many topological cases of interest it exists automatically.  For example, this is the case if it is [[graded object|graded]] and "connected" in the sense that its degree-0 part is just the [[ground field]] (a property possessed by the homology or cohomology of any connected space).  In algebraic topology also the strict coassociativity is not always taken for granted.

=--




## Properties

### Relation to Hopf groups

Note that the definition of Hopf algebra (or, really, of [[Hopf monoid]]) is [[duality|self-dual]]: a Hopf monoid in a [[symmetric monoidal category]] $V$ is the same as a Hopf monoid in the [[opposite category]] $V^{op}$ (i.e. a "Hopf comonoid").  Thus we can view a Hopf algebra as "like a group" in two different ways, depending on whether the group multiplication corresponds to the multiplication or the comultiplication of the Hopf algebra.  The formal connections between Hopf monoids and group objects are:

1. A Hopf monoid in a [[cartesian monoidal category]] $V$ is the same as a group object in $V$.  Such Hopf monoids are always _cocommutative_ (that is, their underlying comonoid is cocommutative).  This is because every object of a cartesian monoidal category is a cocommutative comonoid object in a unique way, and every morphism is a comonoid homomorphism. 

1. A _commutative_ Hopf monoid in a [[symmetric monoidal category]] $V$ is the same as a [[group object]] in the [[opposite category]] $CMon(V)^{op}$, where $CMon(V)$ is the category of commutative monoids in $V$, hence a [[cogroup]] object in $CMon(V)$ (a point highlighted by [[Haynes Miller]], see ([Ravenel 86, appendix A1](#Ravenel86))).  This works because the tensor product of commutative algebras is the categorical [[coproduct]], and hence the [[product]] in its [[opposite category]]. In particular, a [[commutative Hopf algebra]] is the same as a group object in the category $Alg^{op}$ of affine schemes.

Corresponding to these two, an ordinary group $G$ gives us two different Hopf algebras (here $k$ is the [[ground ring]]):

1. The [[group algebra]] $k[G]$ (the free vector space on the set $G$), with multiplication given by the group operation of $G$ and comultiplication given by the diagonal $g\mapsto g\otimes g$.  This Hopf algebra is always cocommutative, and is commutative iff $G$ is abelian.  It can be viewed as the result of applying the [[strong monoidal functor]] $k[-]:Set \to k Mod$ to the Hopf monoid $G$ in $Set$.

1. The function algebra $k(G)$ (the set of functions $G\to k$), with comultiplication given by precomposition with the group operation
$$k(G) \to k(G\times G) \cong k(G)\otimes k(G),$$
and multiplication given by pointwise multiplication in $k$.  In this case we need some finiteness or algebraicity of $G$ in order to guarantee $k(G\times G) \cong k(G)\otimes k(G)$.  This Hopf algebra is always commutative, and is cocommutative iff $G$ is abelian.

Note that if $G$ is finite, then $k[G]\cong k(G)$ as $k$-modules, but the Hopf algebra structure is quite different.

###  The theorem of Hopf modules 

Hopf algebras can be characterized among bialgebras by the [fundamental theorem of Hopf modules](https://ncatlab.org/nlab/show/Hopf+module#fundamental_theorem_on_hopf_modules): the category of Hopf modules over a bialgebra is canonically equivalent to the category of vector spaces over the ground ring iff the bialgebra is a Hopf algebra.  This categorical fact enables a definition of Hopf monoids in some setups that do not allow a sensible definition of antipode.

### Relation to Lie algebras

* [[Milnor-Moore theorem]]

### Tannaka duality
 {#TannakaDuality}

The [[category of modules]] (finite dimensional) over the underlying [[associative algebra]] of a Hopf algebra canonically inherits the structure of an [[rigid monoidal category|rigid]] [[monoidal category]] such that the forgetful [[fiber functor]] to [[vector spaces]] over the ground field is a [[strict monoidal functor]]. 

The statement of [[Tannaka duality]] for Hopf algebras is that this property characterizes Hopf algebras. (See for instance ([Bakke](#Bakke)))

For generalization of this characterization to [[quasi-Hopf algebras]] and [[hopfish algebras]] see ([Vercruysse](#Vercruysse)).

[[!include structure on algebras and their module categories - table]]

### As 3-vector spaces

A Hopf algebra structure on an [[associative algebra]] $A$ canonically defines on $A$ the structure of an algebra object [[internalization|internal]] to the [[2-category]] of algebras, [[bimodule]]s and bimodule homomorphisms.

By the discussion at [[n-vector space]] this allows to identify Hopf algebras with certain _3-vector spaces_ . 

(For instance ([FHLT, p. 27](http://ncatlab.org/nlab/show/Topological+Quantum+Field+Theories+from+Compact+Lie+Groups))).

More general 3-vector spaces are given by _[[hopfish algebras]]_ and generally by [[sesquiunital sesquialgebras]].


### Relation to Frobenius algebras

Both Hopf algebras and [[Frobenius algebras]] are at the same time an [[algebra]] and a [[coalgebra]], albeit with different additional structures and properties. Nevertheless, one may ask whether there is any relation between these two. This leads to the following result due to [Larson & Sweedler (1969)](#LS69).


+-- {: .num_prop #HopfAlgebraIsFrobeniusAlgebra}
###### Proposition

Any [[finite dimensional vector space|finite-dimensional]] Hopf algebra can be endowed with the structure of a Frobenius algebra.

=--

The finite-dimensional condition is expected since all Frobenius algebras are finite-dimensional. A nontrivial part of this result is that, while a finite-dimensional Hopf algebra $A$ already has a counit, this is not be the same counit that realizes $A$ as a Frobenius algebra. Rather, it is an *integral* (see [Larson & Sweedler (1969)](#LS69) for details on this), which for finite-dimensional Hopf algebras always exist and are unique up to scaling.

In fact, more is true. In [Fuchs, Schweigert & Stigner (2011)](#FSS11) a [symmetric special Frobenius algebra](https://ncatlab.org/nlab/show/Frobenius+algebra#special_frobenius_algebras) is constructed from a particular kind of Hopf algebra.

+-- {: .num_prop #DualHopfAlgebraIsSSFrobeniusAlgebra}
###### Proposition

Let $H$ be a finite-dimensional factorizable ribbon Hopf algebra, with multiplication $\mu$, counit $\epsilon$, comultiplication $\Delta$, and antipode $S$. Let $\Lambda$ be a left-integral element of $H$ and $\lambda$ a right-cointegral of $H$ (since $H$ is finite-dimensional, this is equivalent to an integral of the dual Hopf algebra $H^*$) such that $\lambda\circ\Lambda=1$. Then the dual vector space $H^*$ endowed with: a unit $\epsilon^*$, a multiplication $\Delta^*$, a counit $\Lambda^*$, and comultiplication 

$$\Delta_F=((\text{id}_H\otimes (\lambda\circ \mu))\circ (\text{id}_H\otimes S\otimes\text{id}_H)\circ (\Delta\otimes\text{id}_H))^*$$

is a symmetric Frobenius object in the category $\text{Bimod}(H,H)$ of bimodules of $H$, and it is furthermore special iff $H$ is is semisimple.

=--



## Examples

* [[group algebra]]

* [[Steenrod algebra]]

* the [[ordinary homology]] of a [[finite type]] [[H-space]] (for instance a [[based loop space]]) is a [[Hopf algebra]] via its [[Pontrjagin ring]]-[[mathematical structure|structure]] -- see at _[[homology of loop spaces]]_ for more

### The Kac-Paljutkin $H_8$ Hopf algebra 

The Kac-Paljutkin $H_8$ Hopf algebra was first described in [Kac & Paljutkin (1966)](#KP66) and it is the Hopf algebra with the smallest dimension that is [[semisimple object|semisimple]], [[commutative algebra|noncommutative]], and [[cocommutative coalgebra|noncocommutative]]. It is also [[self-dual object|self-dual]] (see e.g. [Burciu (2017)](#Burciu17)). One presentation  is in terms of generators $\{x,y,z\}$ satisfying the relations $x^2=y^2=z^2=1$, $xz=zx$, $zy=yz$, $xyz=yx$, along with comultiplication
 
$$\Delta(x)=xe_0\otimes x+xe_1\otimes y$$

 $$\Delta(y)=ye_1\otimes x+ye_0\otimes y$$ 

$$\Delta(z)=z\otimes z$$

 (where $e_0=\frac{1}{2}(1+z)$, $e_1=\frac{1}{2}(1-z)$) whose counit is $\epsilon(x)=\epsilon(y)=\epsilon(z)=1$. The antipode map is 

$$S(x)=xe_0+ye_1$$

 $$S(y)=xe_1+ye_0$$

 $$S(z)=z$$

. Its [[category of representations]] is the unique $\mathbb{Z}_2\times\mathbb{Z}_2$ [[Tambara-Yamagami category]] that admits a [[fiber functor]] and is not the representation category of some group.

## Related concepts

* [[quasi-Hopf algebra]]

* [[triangular Hopf algebra]]

* [[quasitriangular Hopf algebra]]/[[quantum group]]

* [[hopfish algebra]]

* [[Hopf algebroid]]

  * [[commutative Hopf algebroid]]

* [[Hopf C-star algebra]]

* [[Hopf monoid]]

* [[Hopf monoidal category]]

* [[Hopf monad]]

* [[change of rings theorem]]

* [[Hopf ring spectrum]]

* [[Pontrjagin product]]



[[!include structure on algebras and their module categories - table]]



## References

* [[Kenneth Brown]], _Hopf algebras_, lectures, [pdf](http://www.maths.gla.ac.uk/~kab/Hopf%20lects%201-8.pdf)

* Nicolas Andruskiewitsch, Walter Ferrer Santos, *The beginnings of the theory of Hopf algebras*, Acta Appl Math **108** (2009) 3-17 &lbrack;[arXiv:0901.2460](https://arxiv.org/abs/0901.2460)&rbrack;

* [[A. P. Balachandran]], S. G. Jo, [[Giuseppe Marmo]]: *Group Theory and Hopf Algebras -- Lectures for Physicists*, World Scientific (2010) &lbrack;[doi:10.1142/7872](https://doi.org/10.1142/7872)&rbrack;


The diagrammatic definition of a Hopf algebra, is also in the [Wikipedia entry](http://en.wikipedia.org/wiki/Hopf_algebra#Formal_definition).

* Eiichi Abe, _Hopf algebras_, Cambridge UP 1980.

* [[Pierre Cartier]], _A primer on Hopf algebras_, Frontiers in number theory, physics, and geometry II, 537--615, preprint IH&#201;S 2006-40, 81p ([doi:10.1007/978-3-540-30308-4_12](https://doi.org/10.1007/978-3-540-30308-4_12),  [pdf](http://preprints.ihes.fr/2006/M/M-06-40.pdf),  [pdf](http://www.math.osu.edu/~kerler.2/VIGRE/InvResPres-Sp07/Cartier-IHES.pdf), [[CartierHopfAlgebras.pdf:file]])

* V. G. [[Drinfel'd]], _Quantum groups_, Proceedings of the International Congress of Mathematicians 1986, Vol. 1, 2 798--820, AMS 1987, [djvu:1.3 M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.djvu), [pdf:2.5 M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.pdf)

* G. Hochschild, _Introduction to algebraic group schemes_, 1971

* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge University Press 1995, 2000.

* {#MilnorMoore65} [[John Milnor]], [[John Moore]], _On the structure of Hopf algebras_, Annals of Math. __81__ (1965), 211-264 ([doi:10.2307/1970615](https://doi.org/10.2307/1970615), [pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/milnor-moore-ann-math-1965.pdf))

* Susan Montgomery, _Hopf algebras and their actions on rings_, AMS 1994, 240p.

* B. Parshall, J.Wang, _Quantum linear groups_, Mem. Amer. Math. Soc. 89(1991), No. 439, vi+157 pp.

* [[Moss Sweedler]], _Hopf algebras_, Benjamin 1969.

* William C. Waterhouse, _Introduction to affine group schemes_, Graduate Texts in Mathematics __66__, Springer 1979. xi+164 pp.

[[Tannaka duality]] for Hopf algebras and their generalization is alluded to in 

* {#Vercruysse} Joost Vercruysse, _Hopf algebras---Variant notions and reconstruction theorems_ ([arXiv:1202.3613](http://arxiv.org/abs/1202.3613))
 

and discussed in detail in 

* {#Bakke} T&#248;rris Kol&#248;en Bakke, _Hopf algebras and monoidal categories_ (2007) ([pdf](https://munin.uit.no/bitstream/handle/10037/1084/finalthesis.pdf))
 

Discussion in [[algebraic topology]] with an eye towards [[stable homotopy theory]], [[Steenrod algebra]] and the [[Adams spectral sequence]]:

* [[Douglas Ravenel]], [[W. Stephen Wilson]], _The Hopf ring for complex cobordism_,  Bull. Amer. Math. Soc. 80 (6) 1185 - 1189, November 1974 (<a href="https://doi.org/10.1016/0022-4049(77)90070-6">doi:10.1016/0022-4049(77)90070-6</a>, [euclid](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-80/issue-6/The-Hopf-ring-for-complex-cobordism/bams/1183536024.full?tab=ArticleLink), [pdf](https://people.math.rochester.edu/faculty/doug/mypapers/hopfring.pdf))

  > (for [[MU]])

* {#Ravenel86} [[Douglas Ravenel]], appendix A1 of: _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))

* [[Neil Strickland]], _Bott periodicity and Hopf rings_, 1992 ([pdf](https://neil-strickland.staff.shef.ac.uk/research/thesis.pdf), [[StricklandHopfRings.pdf:file]])

  > (for [[topological K-theory]])

* [[W. Stephen Wilson]], _Hopf rings in algebraic topology_, Expositiones Mathematicae, 18:369–388, 2000 ([pdf](https://math.jhu.edu/~wsw/papers2/math/39-hopf-rings-expo-2000.pdf))


* [[Christoph Schweigert]], *Hopf algebras, quantum groups and topological field theory* (2022) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schweigert/skripten/hskript.pdf)&rbrack;

For Hopf algebras in generative linguistics, see:

* [[Matilde Marcolli]], [[Noam Chomsky]], Robert Berwick, *Mathematical Structure of Syntactic Merge* ([arXiv:2305.18278](https://arxiv.org/abs/2305.18278))

* [[Matilde Marcolli]], Robert Berwick, [[Noam Chomsky]], *Old and New Minimalism: a Hopf algebra comparison* ([arXiv:2306.10270](https://arxiv.org/abs/2306.10270))

The construction of a Frobenius algebra structure on finite-dimensional Hopf algebras due to

* {#LS69} Richard Larson, [[Moss Sweedler]]. *An Associative Orthogonal Bilinear Form for Hopf Algebras*. American Journal of Mathematics, Vol. 91, No. 1 (Jan., 1969), pp. 75-94 (20 pages). ([doi](https://doi.org/10.2307/2373270))

See also

* Alfons Van Daele. *Reflections on the Larson-Sweedler theorem for (weak) multiplier Hopf algebras* (2024). ([arXiv:2404.15046](https://arxiv.org/abs/2404.15046)).

Lecture notes on Hopf algebras (and [[quantum groups]]) in view of [[topological field theory]]:

* [[Christoph Schweigert]]: *Hopf algebras, quantum groups and topological field theory*, lecture notes (2022) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schweigert/skripten/hskript.pdf)&rbrack;

The proof that $H^*$ can be endowed with the structure of a symmetric special Frobenius object in $\text{Bimod}(H,H)$:

* {#FSS11} [[Jürgen Fuchs]], [[Christoph Schweigert]], Carl Stigner: *Modular invariant Frobenius algebras from ribbon Hopf algebra automorphisms*. Journal of Algebra **363**, 1 August 2012, Pages 29-72. ([doi](https://doi.org/10.1016/j.jalgebra.2012.04.008))


On the $H_8$ Hopf algebra

* {#KP66} [[G. I. Kac]], V. G. Paljutkin, *Finite ring groups_, Trans. Moscow Math. Soc. 15 (1966), 251–294.

* {#Burciu17} Sebastian Burciu. *Representations and conjugacy classes of semisimple quasitriangular Hopf algebras*. (2017) (([arXiv:1709.02176
](https://arxiv.org/abs/1709.02176)).

[[!redirects Hopf algebras]]

[[!redirects Hopf ring]]
[[!redirects Hopf rings]]


[[!redirects skew-antipode]]
[[!redirects skew-antipodes]]
[[!redirects skew antipode]]
[[!redirects skew antipodes]]




