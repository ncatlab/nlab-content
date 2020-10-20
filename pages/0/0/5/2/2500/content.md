
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

A [[quantum field theory]] of **supergravity** is similar to the theory of [[gravity]], but where (in [[first-order formulation of gravity|first order formulation]]) the latter is given by an [[action functional]] (the [[Einstein-Hilbert action]] functional) on the space of [[connection on a bundle|connection]]s (over [[spacetime]]) with values in the [[Poincare Lie algebra]] $\mathfrak{iso}(n,1)$, supergravity is defined by an extension of this to an action functional on the space of connections with values in the [[super Poincare Lie algebra]] $\mathfrak{siso}(n,1)$. One says that supergravity is the theory of _local_ (Poincar&#233;) [[supersymmetry]] in the same sense that ordinary [[gravity]] is the theory of "local Poincar&#233;-symmetry". These are [[gauge theories]] for the [[Poincare Lie algebra]] and the [[super Poincare Lie algebra]], respectively, in that the [[field (physics)]] is a [[Cartan connection]] for the inclusion $o(n,1) \hookrightarrow \mathfrak{siso}(n,1)$:

if we write $\mathfrak{siso}(n,1)$ as a [[semidirect product]] of the translation Lie algebra $\mathbb{R}^{(n,1)}$, the [[special orthogonal Lie algebra]] $\mathfrak{so}(n,1)$ and a [[spin group]] [[representation]] $\Gamma$, then locally a connection is a [[Lie algebra valued 1-form]] 

$$
  A : T X \to \mathfrak{siso}(n,1)
$$

that decomposes into three components, $A = (E, \Omega, \Psi)$:

* a $\mathbb{R}^{n,1}$-valued 1-form $E$ -- the [[vielbein]] 

  (this encodes the [[pseudo-Riemannian metric]] and hence the field of [[gravity]]);

* a $\mathfrak{so}(n,1)$-valued 1-form $\Omega$ -- called the [[spin connection]];

* a $\Gamma$-valued 1-form $\Psi$ -- called the [[gravitino]] field.

Typically in fact the field content of supergravity is larger, in that a field $A$ is really an [[∞-Lie algebra-valued differential form]] with values in an [[∞-Lie algebra]] such as the [[supergravity Lie 3-algebra]] ([DAuriaFreCastellani](#DAuriaFreCastellani)) $\mathfrak{sugra}(10,1)$. Specifically such a field

$$
  A : T X \to \mathfrak{sugra}(10,1)
$$

has one more component

* a 3-form $C$ -- the [[supergravity C-field]].

The [[gauge transformation]]s on the space of such connections that are parameterized by the elements of $\Gamma$ are called [[supersymmetries]].

[[!include local and global geometry - table]]

The condition of [[gauge invariance]] of an action functional on $\mathfrak{siso}$-connections is considerably more restrictive than for one on $\mathfrak{iso}$-connections. For instance there is, under mild assumptions, a _unique_ maximally supersymmetric supergravity extension of the ordinary [[Einstein-Hilbert action]] on a 4-dimensional manifold. This in turn is obtained from the _unique_ (under mild assumptions) maximally supersymmetric supergravity action functional on a (10,1)-dimensional [[spacetime]] by thinking of the 4-dimensional action function as being a [[dimensional reduction]] of the 11-dimensional one.


This uniqueness (under mild conditions) is one reason for interest in supergravity theories. Another important reason is that supergravity theories tend to remove some of the problems that are encountered when trying to realize [[gravity]] as a [[quantum field theory]]. Originally there had been high hopes that the maximally supersymmetric supergravity theory in 4-dimensions is fully [[renormalizable]]. This couldn't be shown computationally -- until recently: triggered by new insights recently there there has been lots of renewed activity on the renormalizability of maximal supergravity. 


### As a gauge theory -- Super Cartan geometry
 {#SuperCartanGeometry}

Ordinary [[Einstein gravity]] has a natural formulation in terms of [[Cartan geometry]] for the inclusion of the [[Lorentz Lie algebra]] into the [[Poincaré Lie algebra]] $\mathfrak{o}(d-1,1) \hookrightarrow \mathfrak{Iso}(\mathbb{R}^{d-1,1})$. In this [[first order formulation of gravity]] a [[field (physics)|field]] configuration is a [[Cartan connection]] with such [[coefficients]].

This perspective directly generalizes to [[supergeometry]] and yields the _superspace formulation_ of theories of supegravity -- _[[super Cartan geometry]]_.

After picking a [[dimension]] $d\in \mathbb{N}$ and writing $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ for the [[Poincaré Lie algebra]], then a choice of "number of supersymmetries" is a choice of [real spin representation](spin+representation#RealIrreducibleSpinRepresentationInLorentzSignature) $N$. Then the [[direct sum]] 

$$
  \mathfrak{Iso}(\mathbb{R}^{d-1,1|N})
  \coloneqq
  \underbrace{\mathfrak{Iso}(\mathbb{R}^{d-1,1})}_{even} \oplus \underbrace{N}_{odd}
$$

regarded as a [[super vector space]] with $N$ in odd degree becomes a [[super Lie algebra]] by letting the $[even,odd]$ bracket be given by the defining [[action]] and by letting the $[odd,odd]$ bracket be given by a canonically induced bilinear and $\mathfrak{o}$-equivariant pairing -- the [[super Poincaré Lie algebra]]. This still canonical contains the [[Lorentz Lie algebra]] $\mathfrak{o}(\mathbb{R}^{d-1,1})$ and the [[quotient]]

$$
  \mathbb{R}^{d-1,1|N} 
  \coloneqq
  \mathfrak{Iso}(\mathbb{R}^{d-1,1|N})/\mathfrak{o}(\mathbb{R}^{d-1,1})
$$

is called [[super Minkowski spacetime]] (equipped with its [[super translation Lie algebra]] structure).

From this, a [[super-Cartan geometry]] is defined in direct analogy to the Cartan formulation of Riemannian geometry


| ([[higher Cartan geometry|higher]]-)[[Cartan geometry]] | $\mathfrak{g}$ | $\mathfrak{h}$ | $\mathfrak{g}/\mathfrak{h}$ |
|---------------------|----------------|----------------|-----------------------------|
| [[Einstein gravity]]  | $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ | $\mathfrak{o}(d-1,1)$ | $\mathbb{R}^{d-1,1}$ |
| [[supergravity]] | $\mathfrak{Iso}(\mathbb{R}^{d-1,1\vert N})$ | $\mathfrak{o}(d-1,1)$ | $\mathbb{R}^{d-1,1\vert N}$ |
| [[11-dimensional supergravity]] | $\mathfrak{Iso}(\widehat{\mathbb{R}}^{10,1\vert N=1})$ | $\mathfrak{o}(d-1,1)$ | $\widehat{\mathbb{R}}^{10,1\vert N=1}$ |

Indeed, all the traditional literature on supergravity (e.g. ([Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre91))) is phrased, more or less explicitly, in terms of [[Cartan connections]] for the inclusion of the [[Lorentz group]] into the [[super Poincaré group]] this way, this being the formalization of what physicists mean when saying that they pass to "local supersymmetry".

One subtlety to take care of is that this makes [[spacetime]] a [[super-spacetime]] locally modeled on [[super Minkowski spacetime]]. But the resulting theory is supposed to be a field theory on an ordinary [[spacetime]] locally modeled on ordinary [[Minkowski spacetime]]. This is enforced by a further constraint on the super-Cartan connection which forces it to be determined by the bosonic manifold underlying the given supermanifold. This constraint is variously known as the _superspace constraints_ or as _[rheonomy](D%27Auria-Fre+formulation+of+supergravity#Rheonomy)_ .

The other subtlety to take care of is that a key aspect of higher dimensional [[supergravity]] theories is that their [[field (physics)|field]] content necessarily includes, in addition to the [[graviton]] and the [[gravitino]], higher [[differential n-form]] fields, notably the 2-form [[B-field]] of 10-dimensional [[type II supergravity]] and [[heterotic supergravity]] as well as the 3-form [[C-field]] of [[11-dimensional supergravity]].

This means that these higher dimensional supergravity theories are not in fact entirely described  by super-[[Cartan geometry]] -- but by super-[[higher Cartan geometry]]. 

This follows a key insight due to ([D'Auria-Fr&#233;-Regge 80](#DAuriaFreRegge80), [D'Auria-Fr&#233; 82](#DAuriaFre82)) -- the _[[D'Auria-Fre formulation of supergravity]]_ -- that the "tensor multiplet" fields of higher dimensional supergravity theories as above are naturally brought into the previous perspective if only one allows more general [[Chevalley-Eilenberg algebras]]. 

Namely, we may add to the above CE-algebra

* a single generator $c_3$ of degree $(3,even)$ 

and extend the differential to that by the formula

$$
  d_{CE} \, c_3 = \frac{1}{2}\bar \psi \Gamma^{a b} \wedge \psi \wedge e_a \wedge e_b
  \,.
$$

This still squares to zero due to the remarkable property of 11d [[super Minkowski spacetime]] by which $\frac{1}{2}\bar \psi \Gamma^{a b} \wedge \psi \wedge e_a \wedge e_b \in CE^4(\mathfrak{Iso}(10,1|N=1))$ is a representative of an exception [[super Lie algebra|super]]-[[Lie algebra cohomology]] class. (The collection of all these exceptional classes constitutes what is known as the _[[brane scan]]_).

In the textbook ([Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre91)) a beautiful algorithm for constructing and handling higher supergravity theories based on such generalized CE-algebras is presented, but it seems fair to say that the authors struggle a bit with the right mathematical perspective to describe what is really happening here.

But from a modern perspective this becomes crystal clear: these generalized CE algebras are CE-algebras not of [[Lie algebras]] but of [[strong homotopy Lie algebras]], hence of [[L-infinity algebras]], in fact of [[Lie n-algebras|Lie (p+1)-algebras]] for $(p+1)$ the degree of the relevant differential form field. 

Specifically, me may write the above generalized CE-algebra with the extra degree-3 generator $c_3$ as the CE-algebra $CE(\mathfrak{m}2\mathfrak{brane}) $

of the _[[supergravity Lie 3-algebra]]_ $\mathfrak{m}2\mathfrak{brane}$.

Now a morphism

$$
  \Omega^\bullet(U) \stackrel{}{\longleftarrow} CE(\mathfrak{m}2\mathfrak{brane}) \;\colon\; A
$$

encodes [[graviton]] and [[gravitino]] fields as above, but in addition it encodes a 3-form

$$
  C_3 \coloneqq A(c_3) \in \Omega^{(3,even)}(U)
$$

whose [[curvature]] 

$$
  G_4 = \mathbf{d}C_3 + \frac{1}{2}\bar \Psi \Gamma^{a b} \wedge \Psi \wedge E_a \wedge E_b
$$

satisfies a modified [[Bianchi identity]], crucial for the theory of [[11-dimensional supergravity]] ([D'Auria-Fr&#233; 82](#DAuriaFre82)).

So this collection of differential form data is no longer a [[Lie algebra valued differential form]], it is an [[L-infinity algebra valued differential form]], with values in the [[supergravity Lie 3-algebra]]. 

The quotient

$$
  \widehat{\mathbb{R}}^{10,1|N=1}
  \coloneqq
  \mathfrak{g}/\mathfrak{h}
  =
  \mathfrak{m}2\mathfrak{brane} / \mathfrak{o}(\mathbb{R}^{10,1|N=1})
$$

is known as _[[extended super Minkowski spacetime]]_.

The [[Lie integration]] of this is a [[smooth infinity-group|smooth 3-group]] $G$ which receives a map from the [[Lorentz group]].

This means that a global description of the geometry which ([Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre91)) discuss locally on [[charts]] has to be a higher kind of Cartan geometry which is locally modeled not just on [[cosets]], but on the [[homotopy quotients]] of ([[smooth infinity-group|smooth]], [[smooth super infinity-groupoid|supergeometric]], ...) [[infinity-groups]] -- [[higher Cartan geometry]].

### Solutions with global supersymmetry
 {#SolutionsWithGlobalSupersymmetry}

A solution to the bosonic [[Einstein equations]] of ordinary [[gravity]] -- some [[Riemannian manifold]] -- has a _global symmetry_ if it has a [[Killing vector]].

Accordingly, a configuration that solves the supergravity [[Euler-Lagrange equations]] is a _[[global supersymmetry]]_ if it has a [[Killing spinor]]: a [[covariantly constant spinor]].

Here the notion of [[covariant derivative]] includes the usual [[Levi-Civita connection]], but also in general [[torsion]] components and contributions from other [[background gauge fields]] such as a [[Kalb-Ramond field]] and the [[RR-field]]s in [[type II supergravity]] or [[heterotic string theory|heterotic supergravity]].

Of particular interest to phenomenologists around the turn of the millennium (but maybe less so today with new experimental evidence) has been in solutions of spacetime manifolds of the form $M^4 \times Y^6$ for $M^4$ the locally observed [[Minkowski spacetime]] (that plays a role as the background for all available particle accelerator experiments) and a small closed 6-dimensional [[Riemannian manifold]] $Y^6$. 

In the absence of further fields besides gravity, the condition that such a configuration has precisely one [[Killing spinor]] and hence precisely one [[global supersymmetry]] turns out to be precisely that $Y^6$ is a [[Calabi-Yau manifold]]. This is where all the interest into these manifolds in [[string theory]] comes from. (Notice though that nothing in the theory itself demands such a compactification. It is only the phenomenological assumption of the factorized spacetime compactification together with $N = 1$ supersymmetry that does so.)

More generally, in the presence of other [[background gauge field]]s, the Calabi-Yau condition here is deformed. One also speaks of [[generalized Calabi-Yau space]]s. (For instance ([GMPT05](#GMPT))).

For more see 

* [[supersymmetry and Calabi-Yau manifolds]]


## Properties

### As a background for Green-Schwarz $\sigma$-models

The [[equations of motion]] of those theories of supergravity which qualify as [[target spaces]] for [[Green-Schwarz action functional]] [[sigma models]] (e.g. 10d [[heterotic supergravity]] for the [[heterotic string]] and 10d [[type II supergravity]] for the [[type II string]]) are supposed to be equivalent to those $\sigma$-models being well defined (the [[WZW-model]] term being well defined, hence $\kappa$-symmetry being in effect). See at _[Green-Schwarz action -- References -- Supergravity equations of motion](Green-Schwarz+action+functional#ReferencesSupergravityBackgroundEquationsOfMotion)_ for pointers.

### Scalar moduli spaces and $U$-duality
 {#UDuality}

The [[compact space|compact]] [[exceptional Lie groups]] form a series

$$
  E_8, E_7, E_6
$$

which is usefully thought of to continue as

$$
  E_5 := Spin(10), E_4 := SU(5), E_3 := SU(3) \times SU(2)
  \,.
$$

Supergravity theories are controled by the corresponding
[[split real forms]]

$$
  E_{8(8)}, E_{7(7)}, E_{6(6)}
$$

$$
  E_{5(5)} := Spin(5,5), E_{4(4)} := SL(5, \mathbb{R}), 
  E_{3(3)} := SL(3, \mathbb{R}) \times SL(2, \mathbb{R})
  \,.
$$

For instance the [[scalar fields]] in the field [[supermultiplet]] of $3 \leq d \leq 11$-dimensional supergravity have [[moduli spaces]] parameterized by the [[homogeneous spaces]] 

$$
  E_{n(n)}/ K_n
$$

for 

$$
  n = 11 - d
  \,,
$$

where $K_n$ is the [[maximal compact subgroup]] of $E_{n(n)}$:

$$
  K_8 \simeq Spin(16), K_7 \simeq SU(8), K_6 \simeq Sp(4)
$$

$$
  K_5 \simeq Spin(5) \times Spin(5), 
  K_4 \simeq Spin(5),
  K_3 \simeq SU(2) \times SO(2)
  \,.
$$

Therefore $E_{n(n)}$ acts as a [[global symmetry]] on the supergravity fields. 

This is no longer quite true for their [[UV-completion]] by the corresponding [[Kaluza-Klein mechanism|compactifications]] of [[string theory]] (e.g. [[type II string theory]] for [[type II supergravity]], etc.). Instead, on these a [[discrete group|discrete subgroup]]

$$
  E_{n(n)}(\mathbb{Z}) \hookrightarrow E_{n(n)}
$$

acts as global symmetry. This is called the **[[U-duality]]** group of the supergravity theory (see there for more).

It has been argued that this pattern should continue in some way further to the remaining values $0 \leq d \lt 3$,
with "[[Kac-Moody groups]]" corresponding to the [[Kac-Moody algebras]]

$$
  \mathfrak{e}_9, \mathfrak{e}_10, \mathfrak{e}_{11}
  \,.
$$

Continuing in the other direction to $d = 10$ ($n = 1$) connects to the [[T-duality]] group $O(d,d,\mathbb{Z})$ of [[type II string theory]].

See the references ([below](#UDualityReferences)).

[[!include U-duality -- table]]


### Exceptional geometry

For the moment see the remarks/references on supergravity at _[[exceptional geometry]]_ and _[[exceptional generalized  geometry]]_.

## Examples

The usual [[folklore]] is that for supergravity Lagrangians "of ordinary type" it turns out that  

* $N = 1$ [[11-dimensional supergravity]] 

is the highest dimension possible, but see also at 

* [[12-dimensional supergravity]]

for some qualification.

All lower dimensional theories in this class appear as [[KK-compactifications]] of this theory or are [[deformations]] of such:

* [[10-dimensional supergravity]] 

  * [[type II supergravity]]

    * [[type IIA supergravity]]
  
      * [[massive type IIA supergravity]]

    * [[type IIB supergravity]]

  * [[heterotic supergravity]]

* [[9-dimensional supergravity]]

* [[8-dimensional supergravity]]

* [[7-dimensional supergravity]]

* [[6-dimensional supergravity]]

* [[5-dimensional supergravity]]

* [[4-dimensional supergravity]]

* [[3-dimensional supergravity]]

* [[2-dimensional supergravity]]

In dimension $(1+0)$ supergravity coupled to [[sigma-model]] fields is the [[spinning particle]].

In dimension $(1+1)$ supergravity coupled to [[sigma-model]] fields is the [[spinning string]]/[[NSR superstring]].

In non-Lorenzian signature it is also possible to consider

* [[12-dimensional supergravity]] 

## Phenomenology

Discussion of evidence for supergravity from [[experiment]]/[[phenomenology]] includes the following:

in  ([Dalianis-Farakos 15](#DalianisFarakos15)) it is argued that the [[Starobinsky model of cosmic inflation]], which is strongly preferred by experiment, further improves after embedding into supergravity.


## Related concepts

* [[gravitino condensation]]

* [[gauged supergravity]]

* [[magic supergravity]]

* [[topologically twisted supergravity]]

* [[Rarita-Schwinger field]]

* [[duality in physics]], [[duality in string theory]]

* [[special geometry]]

* [[torsion constraints of supergravity]]

* [[D'Auria-Fre formulation of supergravity]]

* [string theory FAQ -- Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)

* [[cosmic inflation]] and [[supersymmetry breaking]] via [[higher curvature corrections]] of supergravity are discussed in the context of the [[Starobinsky model of cosmic inflation]]

[[!include table of branes]]


## References

### General

An early survey is 

* {#Nieuwenhuizen81} [[Peter van Nieuwenhuizen]], _Supergravity_, Physics Reports, Vol. 68, p. 189 - 398, 1981

Textbook accounts include

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* [[Antoine Van Proeyen]], [[Daniel Freedman]], _Supergravity_, Cambridge University Press, 2012

Lecture notes include

* P. Binetruy, G. Girardi, R. Grimm, _Supergravity couplings: a geometric formulation_, Phys.Rept.343:255-462,2001 ([arXiv:hep-th/0005225](http://arxiv.org/abs/hep-th/0005225))

* [[Friedemann Brandt]], _Lectures on supergravity_ ([arXiv:hep-th/0204035](http://arxiv.org/abs/hep-th/0204035))

* [[Bernard de Wit]], _Supergravity_ ([arXiv:hep-th/0212245](http://arxiv.org/abs/hep-th/0212245))

* [[Antoine Van Proeyen]], _Structure of supergravity theories_ ([arXiv:hep-th/0301005](http://arxiv.org/abs/hep-th/0301005))

* [[Joachim Gomis]], _Three lectures on Supergravity_ ([pdf slides](http://www.fis.puc.cl/~jalfaro/supergravity/Three%20Lectures%20on%20Supergravity.pdf))

On [[Kaluza-Klein compactification]] in supergravity:

* {#DuffNilssonPope86} [[Mike Duff]], [[Bengt Nilsson]], [[Christopher Pope]], _Kaluza-Klein supergravity_, Physics Reports Volume 130, Issues 1–2, January 1986, Pages 1-142 ([spire:229417](https://inspirehep.net/record/229417), <a href="https://doi.org/10.1016/0370-1573(86)90163-8">doi:10.1016/0370-1573(86)90163-8</a>)


Further surveys include

* {#Duff04} [[Michael Duff]], _Erice lectures on "The status of local supersymmetry"_ ([arXiv:hep-th/0403160](http://arxiv.org/abs/hep-th/0403160))


A fair bit of detail on [[supersymmetry]] and on supergravity is in 

* [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

The original article that introduced the [[D'Auria-Fre formulation of supergravity]] is

* [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140

The underlying [[super Cartan geometry]] is made fully explicit in:

* [[Konstantin Eder]], _Super Cartan geometry and the super Ashtekar connection_ ([arXiv:2010.09630](https://arxiv.org/abs/2010.09630))
 
A compendium, of relevant [[action functionals]] and [[equations of motion]] is in 

* M. J. D. Hamilton, _The field and Killing spinor equations of M-theory and type IIA/IIB supergravity in coordinate-free notation_ ([arXiv:1607.00327](http://arxiv.org/abs/1607.00327))

On [[black hole]]-solutions:

* [[Riccardo D'Auria]], [[Pietro Fre]], _BPS black holes in supergravity_, ([hep-th/9812160](http://arxiv.org/abs/hep-th/9812160))


* Antonio Gallerati, _Constructing black hole solutions in supergravity theories_ ([arXiv:1905.04104](https://arxiv.org/abs/1905.04104))


### Renormalization

* S. Deser, J.H. Kay, K.S. Stelle, _Renormalizability Properties of Supergravity_, Phys Rev Lett 38, 527 (1977) (reproduced as [arXiv:1506.03757](http://arxiv.org/abs/1506.03757))


### U-duality
 {#UDualityReferences}

Some basic facts are recalled in

* [[Jacques Distler]], _Split real forms_ ([blog post](http://golem.ph.utexas.edu/~distler/blog/archives/001213.html)).

The $E_{7(7)}$-symmetry was first discussed in 

* [[Bernard de Wit]], [[Hermann Nicolai]], _$D = 11$ Supergravity With Local $SU(8)$ Invariance_, Nucl. Phys.
B 274, 363 (1986)

and $E_{8(8)}$ in 

* [[Hermann Nicolai]], _$D = 11$ Supergravity with Local $SO(16)$ Invariance_ , Phys. Lett. B 187, 316 (1987).

* K. Koepsell, [[Hermann Nicolai]], [[Henning Samtleben]], _An exceptional geometry for $d = 11$
supergravity?_, Class. Quant. Grav. 17, 3689 (2000) ([arXiv:hep-th/0006034](http://arxiv.org/abs/hep-th/0006034)).

The discrete quantum subgroups were discussed in 

* [[Chris Hull]], [[Paul Townsend]], _Unity of Superstring Dualities_ Nucl.Phys.B438:109-137 (1995) ([arXiv:hep-th/9410167](http://arxiv.org/abs/hep-th/9410167))

which also introduced the term "U-duality".

Review and further discusssion is in 

* Shun'ya Mizoguchi, Germar Schroeder, _On Discrete U-duality in M-theory_, Class.Quant.Grav. 17 (2000) 835-870 ([arXiv:hep-th/9909150](http://arxiv.org/abs/hep-th/9909150))

A careful discussion of the topology of the U-duality groups is in 

* [[Arjan Keurentjes]], _The topology of U-duality (sub-)groups_ ([arXiv:hep-th/0309106](http://arxiv.org/abs/hep-th/0309106))

* [[Arjan Keurentjes]], _U-duality (sub-)groups and their topology_ ([arXiv:hep-th/0312134](http://arxiv.org/abs/hep-th/0312134))

A discussion in the context of [[generalized complex geometry]] / [[exceptional generalized complex geometry]] is in 

* Paulo Pires Pacheco, [[Daniel Waldram]], _M-theory, exceptional generalised geometry and superpotentials_ ([arXiv:0804.1362](http://arxiv.org/abs/0804.1362))

* Nicholas Houston, _Supergravity and Generalized Geometry_ Thesis (2010) ([pdf](https://workspace.imperial.ac.uk/theoreticalphysics/Public/MSc/Dissertations/2010/Nicholas%20Houston%20Dissertation.pdf))

The case of "$E_{10}$" is discussed in 

* [[Thibault Damour]], [[Marc Henneaux]], [[Hermann Nicolai]], _$E(10)$ and a 'small tension expansion' of M
theory_, Phys. Rev. Lett. 89, 221601 (2002) ([arXiv:hep-th/0207267](http://arxiv.org/abs/hep-th/0207267));

* [[Axel Kleinschmidt]], [[Hermann Nicolai]], _$E(10)$ and $SO(9,9)$ invariant supergravity_, JHEP 0407,
041 (2004) ([arXiv:hep-th/0407101](http://arxiv.org/abs/hep-th/0407101))

and that of "$E_{11}$" in 

* [[Peter West]], _$E_{11}$ and M-theory_, Class. Quant. Grav. 18, 4443 (2001) ([arXiv:hep-th/0104081](http://arxiv.org/abs/hep-th/0104081)).

General discussion of the [[Kac-Moody groups]] arising in this context is for instance in 

* Philipp Fleig, [[Axel Kleinschmidt]], _Eisenstein series for infinite-dimensional U-duality groups_ ([arXiv:1204.3043](http://arxiv.org/abs/1204.3043))

### Gauged supergravity

* Natxo Alonso-Alberca; and Tom&#225;as Ort&#237;n, _Gauged/Massive supergravities in diverse dimensions_ ([pdf](http://digital.csic.es/bitstream/10261/38952/1/ARTICULOS302400%5B1%5D.pdf))

### Chern-Simons supergravity

A survey of the [[Chern-Simons gravity]]-style action functionals for supergravity is in

* [[Jorge Zanelli]], _Lecture notes on Chern-Simons (super-)gravities_ ([arXiv:0502193](http://arxiv.org/abs/hep-th/0502193))
{#Zanelli}


### History
 {#History}

The idea of supergravity was proposed by

* [[Dmitry Volkov]], V.P. Akulov, _Possible universal neutrino interaction_, ZhETF Pis. Red. (JETP Letters, AIP translation), 16, n.11 (1972) 621 ([pdf](http://www.jetpletters.ac.ru/ps/1766/article_26864.shtml))

followed up by the first model of supergravity (in nonlinear realization) constructed in 

* [[Dmitry Volkov]] and [[Vyacheslav Soroka]], _Higgs effect for Goldstone particles with spin 1/2_, ZhETF Pis. Red. (JETP Letters, AIP translation), 18, n.8 (1973) 529 ([pdf](https://www.jetpletters.ac.ru/ps/1568/article_24038.shtml))  

However, the term "supergravity" was coined later by
[Freedman, Nieuwenhuizen, Ferrara 76](#FreedmanNieuwenhuizenFerrara76), whose work on supergravity is regarded as foundational for the subject.

This early history is discussed in

* [[Steven Duplij]], _Supergravity was discovered by D.V. Volkov and V.A. Soroka in 1973, wasn't it?_, East Eur. J. Phys., v3, p. 81-82 (2019) ([arXiv:1910.03259](https://arxiv.org/abs/1910.03259))
 

Supergravity, in the guise of [[4d supergravity]], was first found (constructed) in

* {#FreedmanNieuwenhuizenFerrara76} [[Daniel Freedman]], [[Peter van Nieuwenhuizen]], [[Sergio Ferrara]], _Progress toward a theory of supergravity_, Phys. Rev. D13 (1976) 3214 ([doi.org/10.1103/PhysRevD.13.3214](https://doi.org/10.1103/PhysRevD.13.3214))


Accounts of the early history include the following:

* [[Sergio Ferrara]], _Supergravity and the quest for a unified theory_ ([arxiv:hep-th/9405065](https://arxiv.org/abs/hep-th/9405065))


* [[Dmitry Volkov]], _Supergravity before 1976_,
International Conference on the History of Original Ideas and Basic Discoveries in Particle Physics, Erice, 1994 ([Springer, Chapter](http://link.springer.com/chapter/10.1007/978-1-4613-1147-8_34) or [arXiv:hep-th/9410024](http://arxiv.org/abs/hep-th/9410024))

* R. Arnowitt, [[Ali Chamseddine]], Pran Nath, _The Development of Supergravity Grand Unification: Circa 1982-85_ ([arXiv:1206.3175](http://arxiv.org/abs/1206.3175))

* [[Dmitry Volkov]], _Supergravity before and after 1976. The story of goldstonions_, in  [Concise Encyclopedia of Supersymmetry,
S. Duplij, J. Bagger, W. Siegel (Eds.), Springer, 2004](http://www.springer.com/gp/book/9781402013386) or [arXiv:hep-th/9404153](http://arxiv.org/abs/hep-th/9404153)

* David Appell, _When supergravity was born_, 2012 ([pdf](http://www.davidappell.com/articles/PWSep12appell-supergravity.pdf))

* [[Peter van Nieuwenhuizen]], _Aspects of supergravity_, 2014 ([pdf](http://media.scgp.stonybrook.edu/presentations/20140109_vanNieuwenhuizen.pdf))

* [[Vyacheslav Soroka]], _The Sources of Supergravity_ in [The Supersymmetric World. The Beginnings of the Theory, G. Kane and M. Shifman (Eds.), World Scientific, 2000](http://www.worldscientific.com/doi/10.1142/9789812385505_0011) or [arXiv:hep-th/0203171](https://arxiv.org/abs/hep-th/0203171)

* [[Sergio Ferrara]], A. Sagnotti, _Supergravity at 40: Reflections and Perspectives_, Based in part on the talk delivered by S. F. at the "Infeld Colloquium and Discrete", in Warsaw, on December 1 2016, and on a joint CERN Courier article. Dedicated to [[John Schwarz]] on the occasion of his 75-th birthday ([arXiv:1702.00743](https://arxiv.org/abs/1702.00743))

* [[Stanley Deser]], _A brief history of Supergravity: the first three weeks_ ([arXiv:1704.05886](https://arxiv.org/abs/1704.05886))

See also _[supersymmetry -- History](supersymmetry#ReferencesHistory)_.


### Related

Further physics monographs on supergravity include

* I. L. Buchbinder, S. M. Kuzenko, _Ideas and methods of supersymmetry and supergravity; or A walk through superspace_, [googB](http://books.google.com/books?isbn=0750305061)

* [[Julius Wess]], Jonathan Bagger, _Supersymmetry and supergravity_, 1992

* [[Steven Weinberg]], _Quantum theory of fields_, volume III: supersymmetry

* [Concise Encyclopedia of Supersymmetry, S. Duplij, J. Bagger, W. Siegel (Eds.), Springer, 2004](http://www.springer.com/gp/book/9781402013386), [SUSY story](http://ivv5hpp.uni-muenster.de/u/douplii/susy/SUSYEnc_Story.pdf) narrated by its founders


The [[Cauchy problem]] for classical solutions of simple supergravity has been discussed in

* [[Yvonne Choquet-Bruhat]], _[[The Cauchy Problem in Classical Supergravity]]_, Letters in Mathematical Physics 7 (1983) 459-467. 0377

A canonical textbook reference for the role of Calabi-Yau manifolds in compactifications of 10-dimensional [[supergravity]] is volume II, starting on page 1091 in

* [[P. Deligne]], [[P. Etingof]], [[D. Freed]], L. Jeffrey, [[D. Kazhdan]], J. Morgan, D. R. Morrison and [[E. Witten]], eds. _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

Discussion of solutions with $N = 1$ global supersymmetry left and their relation to Calabi-Yau compactifications are for instance in 

* {#GMPT} [[Mariana Graña]], [[Ruben Minasian]], Michela Petrini, [[Alessandro Tomasiello]], _Generalized structures of $N=1$ vacua_, [arXiv:hep-th/0505212](http://arxiv.org/abs/hep-th/0505212)
  
### Phenomenology

Discussion of implications of supergravity for [[phenomenology]]/[[cosmology]] includes

* {#DalianisFarakos15} Ioannis Dalianis, [[Fotis Farakos]], _On the initial conditions for inflation with plateau potentials: the $R + R^2$ (super)gravity case_ ([arXiv:1502.01246](http://arxiv.org/abs/1502.01246))


[[!redirects supergravity]]
[[!redirects supergravities]]
[[!redirects Supergravity]]



[[!redirects super-gravity]]
[[!redirects super-gravities]]