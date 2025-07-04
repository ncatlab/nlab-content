

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

The __spin group__ $Spin(n)$ is the [[universal covering space]] of the [[special orthogonal group]] $SO(n)$. By the usual arguments it inherits a group structure for which the operations are smooth and so is a [[Lie group]] like $SO(n)$.

For special cases in low dimensions see at:  [[Spin(2)]], [[Spin(3)]], [[Spin(4)]], [[Spin(5)]], [[Spin(6)]], [[Spin(7)]], [[Spin(8)]]

## Definition

+-- {: .num_defn #QuadraticVectorSpace}
###### Definition


A _quadratic vector space_ $(V, \langle -,-\rangle)$ is a [[vector space]] $V$ of finite [[dimension]] over a [[field]] $k$ of [[characteristic]] 0, and equipped with a symmetric [[bilinear form]] $\langle -,-\rangle \colon V \otimes V \to k$.

=--

Conventions as in ([Varadarajan 04, section 5.3](#Varadarajan04)).

We write $q\colon v \mapsto \langle v ,v \rangle$ for the corresponding [[quadratic form]].

+-- {: .num_defn }
###### Definition

The _[[Clifford algebra]]_ $Cl(V,q)$ of a quadratic vector space, def. \ref{QuadraticVectorSpace}, is the [[associative algebra]] over $k$ which is the [[quotient]]

$$
  Cl(V,q)
    \coloneqq
  T(V)/I(V,q)
$$ 

of the [[tensor algebra]] of $V$ by the ideal generated by the elements $v \otimes v - q(v)$.

=--

Since the [[tensor algebra]] $T(V)$ is naturally $\mathbb{Z}$-graded, the Clifford algebra $Cl(V,q)$ is naturally $\mathbb{Z}/2\mathbb{Z}$-graded.

Let $(\mathbb{R}^n, q = {\vert -\vert})$ be the $n$-dimensional [[Cartesian space]] with its canonical [[scalar product]]. Write $Cl^\mathbb{C}(\mathbb{R}^n)$ for the [[complexification]] of its [[Clifford algebra]].


+-- {: .num_prop }
###### Proposition

There exists a unique [[complex number|complex]] [[representation]] 

$$
  Cl^{\mathbb{C}}(\mathbb{R}^n) \longrightarrow End(\Delta_n)
$$

of the algebra $Cl^\mathbb{C}(\mathbb{R}^n)$ of smallest [[dimension]]

$$
  dim_{\mathbb{C}}(\Delta_n) = 2^{[n/2]}
  \,.
$$


=--

+-- {: .num_defn #SpinGroup}
###### Definition

The [[Pin group]] $Pin(V;q)$ of a quadratic vector space, def. \ref{QuadraticVectorSpace}, is the [[subgroup]] of the [[group of units]] in the [[Clifford algebra]] $Cl(V,q)$ 

$$
  Pin(V,q) \hookrightarrow GL_1(Cl(V,q))
$$

on those elements which are multiples $v_1 \cdots v_{n}$ of elements $v_i \in V$ with $q(v_i) = 1$.

The [[Spin group]] $Spin(V,q)$ is the further [[subgroup]] of $Pin(V;q)$ on those elements which are even number multiples $v_1 \cdots v_{2k}$ of elements $v_i \in V$ with $q(v_i) = 1$.

Specifically, "the" Spin group is

$$
  Spin(n) \coloneqq Spin(\mathbb{R}^n)
  \,.
$$

=--

A _[[spin representation]]_ is a [[linear representation]] of the spin group, def. \ref{SpinGroup}.


## Properties

### General

By definition the spin group sits in a [[short exact sequence]] of groups

$$
  \mathbb{Z}_2 \to Spin \to SO
  \,.
$$

### Relation to Whitehead tower of orthogonal group

The spin group is one element in the [[Whitehead tower]] of $O(n)$, which starts out like

$$
  \cdots \to Fivebrane(n) \to String(n) \to Spin(n) \to SO(n) \to \mathrm{O}(n)
  \,.
$$

The [[homotopy group]]s of $O(n)$ are for $k \in \mathbb{N}$ and for sufficiently large $n$

$$
  \array{
     \pi_{8k+0}(O) & = \mathbb{Z}_2
     \\
     \pi_{8k+1}(O) & = \mathbb{Z}_2
     \\
     \pi_{8k+2}(O) & = 0
     \\
     \pi_{8k+3}(O) & = \mathbb{Z}
     \\
     \pi_{8k+4}(O) & = 0
     \\
     \pi_{8k+5}(O) & = 0
     \\
     \pi_{8k+6}(O) & = 0
     \\
     \pi_{8k+7}(O) & = \mathbb{Z}
  }
  \,.
$$

By [[Whitehead tower|co-killing]] these groups step by step one gets

$$
  \array{
     cokill\, this &&&& to\,get
     \\
     \\
     \pi_{0}(O) & = \mathbb{Z}_2 &&& SO
     \\
     \pi_{1}(O) & = \mathbb{Z}_2 &&& Spin
     \\
     \pi_{2}(O) & = 0
     \\
     \pi_{3}(O) & = \mathbb{Z} &&& String
     \\
     \pi_{4}(O) & = 0
     \\
     \pi_{5}(O) & = 0
     \\
     \pi_{6}(O) & = 0
     \\
     \pi_{7}(O) & = \mathbb{Z} &&& Fivebrane
  }
  \,.
$$

Via the [[J-homomorphism]] this is related to the [[stable homotopy groups of spheres]]:

[[!include image of J -- table]]


### Exceptional isomorphisms
 {#ExceptionalIsomorphisms}

In low [[dimensions]] the [[spin groups]] happens to be [[isomorphism|isomorphic]]  to various other [[classical Lie groups]]. One speaks of _[[exceptional isomorphisms]]_ or _[[sporadic isomorphisms]]_.

See for instance ([Garrett 13](#Garrett13)). See also _[[division algebra and supersymmetry]]_.

In the following $Sp(n)$ denotes the [[quaternionic unitary group]] in [[quaternion|quaternionic]] [[dimension]] $n$.

We have

* in [[Euclidean geometry|Euclidean]] signature

  * $Spin(1) \simeq O(1)$

  * [[Spin(2)]] $\simeq U(1) \simeq SO(2) \simeq S^1$ ([[SO(2)]], the [[circle group]], see also at _[[real Hopf fibration]]_)

    the projection $Spin(2)\to SO(2)$ corresponds to $S^1\stackrel{\cdot 2}{\longrightarrow} S^1$, see also at _[[Theta characteristic]]_

  * [[Spin(3)]] $\simeq Sp(1) \simeq SU(2) \simeq S^3$ (the [[special unitary group]] [[SU(2)]]

    the inclusion $Spin(2) \hookrightarrow Spin(3)$ corresponds to the canonical $S^1 \hookrightarrow S^3$ (see e.g. [Gorbounov-Ray 92](#GorbounovRay92))

  * [[Spin(4)]] $\simeq Sp(1)\times Sp(1) \simeq S^3 \times S^3$

    this is given by identifying $\mathbb{R}^4 \simeq \mathbb{H}$ with the [[quaternions]] and $SU(2) \simeq S^3$ with the group of unit quternions. Then left and right quaternion multiplication gives a [[homomorphism]]

    $$
      SU(2) \times SU(2) \longrightarrow SO(4)
    $$

    $$
      (g,h) \mapsto ( x \mapsto \; g^{-1}  x h )
    $$

    which is a [[double cover]] and hence exhibits the isomorphism.

    In particular therefore the inclusion $Spin(3) \hookrightarrow Spin(4)$ corresponds to the [[diagonal]] $S^3 \hookrightarrow S^3 \times S^3$.

    At the level of [[Lie algebras]] $\mathfrak{so}(4) \simeq \wedge^2 \mathbb{R}^4$ and the $\pm 1$-[[eigenspaces]] of the [[Hodge star operator]] $\star \colon \Wedge^2 \mathbb{R}^4 \to \mathbb{R}^4$ gives the [[direct sum]] decomposition $\mathfrak{so}(4) \simeq \mathfrak{su}(2) \oplus \mathfrak{su}(2) \simeq \mathfrak{so}(3) \oplus \mathfrak{so}(3)$
 
  * [[Spin(5)]] $\simeq Sp(2)$ (an indirect consequence of [[triality]], see e.g. [Čadek-Vanžura 97](#CadekVanzura97))

  * [[Spin(6)]] $\simeq SU(4)$ (the [[special unitary group]] [SU(4)](special+unitary+group#SU4))

* in [[Lorentz group|Lorentzian]] signature

  * $Spin(1,1) \simeq GL(1,\mathbb{R})$

  * $Spin(2,1) \simeq SL(2, \mathbb{R})$ -- 2d [[special linear group]] of [[real numbers]]

  * $Spin(3,1) \simeq SL(2,\mathbb{C})$ -- 2d [[special linear group]] of [[complex numbers]]

  * $Spin(4,1) \simeq Sp(1,1)$

  * $Spin(5,1) \simeq SL(2,\mathbb{H})$ -- 2d [[special linear group]] of [[quaternions]]

  * $Spin(9,1) \simeq_{in\;some\;sense} SL(2, \mathbb{O})$ -- 2d [[special linear group]] of [[octonions]] (see [[SL(2,O)]] for more on this would-be isomorphism)

* in [[anti de Sitter group|anti de Sitter]] signature

  * $Spin(2,2) \simeq SL(2,\mathbb{R}) \times SL(2,\mathbb{R})$

  * $Spin(3,2) \simeq Sp(4,\mathbb{R})$

  * $Spin(4,2) \simeq SU(2,2)$

* in mixed signature

  * $Spin(3,3) \simeq SL(4,\mathbb{R})$ ([Garrett 13 (2.12)](#Garrett13))

Beyond these dimensions there are still some interesting identifications, but the situation becomes much more involved.

[[!include exceptional spinors and division algebras -- table]]




## Examples
 {#ExampleSection}


[[!include low dimensional rotation groups -- table]]


* [[Spin(11,3)]]


## Applications

### Spin geometry

See [[spin geometry]]

### In physics

The name arises due to the requirement that the structure group of the [[tangent bundle]] of [[spacetime]] lifts to $Spin(n)$ so as to 'define particles with spin'... (Someone more awake and focused please put this into proper words!)

See [[spin structure]].

## Related concepts

* [[spinor]], [[spin representation]], [[spinor bundle]]

The [[Whitehead tower]] of the [[orthogonal group]] looks like

$\cdots \to$ [[fivebrane group]] $\to$ [[string group]] $\to$ **spin group** $\to$ [[special orthogonal group]] $\to$ [[orthogonal group]].

* [[spin^c group]], [[spin^h group]]

* [[metaplectic group]]

* [[semi-spin group]]

[[!include table of orthogonal groups and related]]


## References

Textbook accounts:

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], chapter I, section 2 of _[[Spin geometry]]_, Princeton University Press (1989)

* [[Eckhard Meinrenken]]: *Clifford algebras and Lie groups*, Ergebn. Mathem. & Grenzgeb., Springer (2013) &lbrack;[doi:10.1007/978-3-642-36216-3](https://doi.org/10.1007/978-3-642-36216-3)&rbrack;

* [[Howard Georgi]], §21 & 22 in: *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;
  > (with an eye towards application to [[spinors]] in (the [[standard model of particle physics|standard model]] of) [[particle physics]])




See also

* {#Varadarajan04} [[Veeravalli Varadarajan]], section 7 of _[[Supersymmetry for mathematicians]]: An introduction_, Courant lecture notes in mathematics, American Mathematical Society, Providence, R.I (2004)
  

* wikipedia _[Spin group](http://en.wikipedia.org/wiki/Spin_group)_ 


Examples of sporadic (exceptional) spin group isomorphisms incarnated as [[isogenies]] onto [[orthogonal groups]] are discussed in 

* {#Garrett13} [[Paul Garrett]], _Sporadic isogenies to orthogonal groups_ (July 2013) &lbrack;[pdf](http://www.math.umn.edu/~garrett/m/v/sporadic_isogenies.pdf), [[Garrett-SporadicIsogenies.pdf:file]] &rbrack;
 
* {#GorbounovRay92} [[Vassily Gorbounov]], [[Nigel Ray]], _Orientations of $Spin$ Bundles and Symplectic Cobordism_, Publ. RIMS, Kyoto Univ. 28 (1992), 39-55 ([[GorbunovRaySpinBundles.pdf:file]], [doi: 10.2977/prims/1195168855](https://www.ems-ph.org/journals/show_abstract.php?issn=0034-5318&vol=28&iss=1&rank=4))

The [[exceptional isomorphism]] [[Spin(5)]] $\simeq$ [[Sp(2)]] is discussed via [[triality]] in 

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))

Discussion of the [[cohomology]] of the [[classifying space]] $B Spin$ includes

* E. Thomas, _On the cohomology groups of the classifying space for the stable spinor groups_, Bol. Soc. Mat. Mexicana (2) 7 (1962) 57-69.

* {#Pittie91} [[Harsh Pittie]], _The integral homology and cohomology rings of SO(n) and Spin(n)_, Journal of Pure and Applied Algebra Volume 73, Issue 2, 19 August 1991, Pages 105&#8211;153 (<a href="https://doi.org/10.1016/0022-4049(91)90108-E">doi:10.1016/0022-4049(91)90108-E</a>)

[[!redirects spin groups]]

[[!redirects Spin group]]
[[!redirects Spin groups]]


[[!redirects Spin]]
[[!redirects Spin(n)]]

[[!redirects spin-group]]

[[!redirects spin groups]]
[[!redirects spin-groups]]