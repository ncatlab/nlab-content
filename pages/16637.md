
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The [[sphere]] of [[dimension]] 7.

This is one of the [[parallelizable manifold|parallelizable]] spheres, as such corresponds to the [[octonions]] among the [[division algebras]], being the manifold of unit octonions, and is the only one of these which does not carry ([[Lie group|Lie]]) [[group]] structure but just [[Moufang loop]] structure.


## Properties



### Quaternionic Hopf fibration
 {#QuaternionicHopfFibration}

The 7-sphere participates in the [[quaternionic Hopf fibration]], the analog of the complex [[Hopf fibration]] with the field of [[complex numbers]] replaced by the division ring of [[quaternions]] or Hamiltonian numbers $\mathbb{H}$.

$$
  \array{
    S^3 &\hookrightarrow& S^7
    \\
    && \downarrow^\mathrlap{p}
    \\
    && S^4 &\stackrel{}{\longrightarrow}& \mathbf{B} SU(2)
  }
$$

Here the idea is that $S^7$ can be construed as $\{(x, y) \in \mathbb{H}^2: {|x|}^2 + {|y|}^2 = 1\}$, with $p$ mapping $(x, y)$ to $x/y$ as an element in the [[projective line]] $\mathbb{P}^1(\mathbb{H}) \cong S^4$, with each [[fiber]] a [[torsor]] parametrized by quaternionic [[scalars]] $\lambda$ of unit [[norm]] (so $\lambda \in S^3$).  This canonical $S^3$-bundle (or $SU(2)$-bundle) is classified by a map $S^4 \to \mathbf{B} SU(2)$. 

### Coset space realizations
 {#CosetSpaceRealization}

+-- {: .num_prop #QuotientOfSpin7ByG2IsS7}
###### Proposition
**([[coset space]] of [[Spin(7)]] by [[G2]] is [[7-sphere]])**

Consider the canonical [[action]] of [[Spin(7)]] on the [[unit sphere]] in $\mathbb{R}^8$ (the [[7-sphere]]),

1. This action is is [[transitive action|transitive]];

1. the [[stabilizer group]] of any point on $S^7$ is [[G2]];

1. all [[G2]]-subgroups of [[Spin(7)]] arise this way, and are all [[conjugate subgroup|conjugate]] to each other.

Hence the [[coset space]] of [[Spin(7)]] by [[G2]] is the [[7-sphere]]

$$
  S^7
  \;\simeq_{diff}\;
  Spin(7)/G_2
  \,.
$$

=--

(e.g [Varadarajan 01, Theorem 3](#Varadarajan01))


Other coset realizations of the usual [[differentiable manifold|differentiable]] 7-sphere ([Choquet-Bruhat, DeWitt-Morette 00, p. 288](#Choquet-Bruhat+DeWitt-Morette00)):

* $S^7 \simeq_{diff} $ [[Spin(6)]]$/SU(3) \simeq_{iso} SU(4)/SU(3)$ (by [this Prop.](sphere#OddDimSphereAsSpecialUnitaryCoset));

* $S^7 \simeq_{diff}  Spin(5)/SU(2)$ ([Awada-Duff-Pope 83](#AwadaDuffPope83), [Duff-Nilsson-Pope 83](#DuffNilssonPope83))

These three coset realizations of 'squashed' 7-spheres together with a fourth

* $S^7 \simeq_{diff}  Spin(8)/Spin(7)$,

the realization of the 'round' 7-sphere, may be seen jointly as resulting from the 8-dimensional representations of even [[Clifford algebras]] in 5, 6, 7, and 8 dimensions (see [Baez](#Baez)) and as such related to the four [[normed division algebras]]. See also [Choquet-Bruhat+DeWitt-Morette00, pp. 263-274](#Choquet-Bruhat+DeWitt-Morette00).

[[!include coset space structure on n-spheres -- table]]

The following gives an [[exotic 7-sphere]]:

* $S^7 \simeq_{homeo} Sp(1)\backslash Sp(2)/Sp(1)$ ([[Gromoll-Meyer sphere]])


\linebreak

### Exotic 7-spheres

A celebrated result of Milnor is that $S^7$ admits [[exotic smooth structures]] (see at _[[exotic 7-sphere]]_), i.e., there are [[smooth manifold]] structures on the [[topological manifold]] $S^7$ that are not [[diffeomorphism|diffeomorphic]] to the standard smooth structure on $S^7$. More structurally, considering smooth structures up to [[orientation|oriented]] diffeomorphism, the different smooth structures form a [[monoid]] under a (suitable) operation of [[connected sum]], and this monoid is isomorphic to the [[cyclic group]] $\mathbb{Z}/(28)$. With the notable possible exception of $n = 4$ (where the question of existence of exotic 4-spheres is wide open), exotic spheres first occur in dimension $7$. This phenomenon is connected to the [[h-cobordism theorem]] (the monoid of smooth structures is identified with the monoid of h-cobordism classes of oriented [[homotopy spheres]]). 

One explicit construction of the smooth structures is given as follows (see [Milnor 1968](#Mil2)). Let $W_k$ be the algebraic variety in $\mathbb{C}^5$ defined by the equation 

$$z_1^{6 k - 1} + z_2^3 + z_3^2 + z_4^2 + z_5^2 = 0$$ 

and $S_\epsilon \subset \mathbb{C}^5$ a sphere of small radius $\epsilon$ centered at the origin. Then each of the $28$ smooth structures on $S^7$ is represented by an intersection $W_k \cap S_\epsilon$, as $k$ ranges from $1$ to $28$. These manifolds sometimes go by the name _Brieskorn manifolds_ or _[[Brieskorn spheres]]_ or _[[Milnor spheres]]_.


### $G_2$-structure
 {#G2Structure}

Let $\phi_0 \in \Omega^3(\mathbb{R}^7)$ be the [[associative 3-form]] and let 

$$
  \Phi_0 \in \Omega^4(\mathbb{R} \oplus \mathbb{R}^7)
$$

be given by

$$
  \Phi_0 = d x_0 \wedge \phi_0 + \star \phi_0
$$

(where $x_0$ denotes the canonical coordinate on the first factor of $\mathbb{R}$ and $\phi_0$ is pulled back along the projection to $\mathbb{R}^7$)
.

By construction this is its own [[Hodge dual]]

$$
  \Phi = \star \Phi
  \,.
$$

This implies that as we restrict $\Phi_0$ to 

$$
  \mathbb{R}^8 - \{0\} \simeq \mathbb{R} \times S^7
$$

then there is a unique 3-form 

$$
  \phi \in \Omega^3(S^7)
$$

on the 7-sphere such that

$$
  \Phi_0 = r^3 \wedge \phi + r^4 \star_{S^7} \phi
  \;\;\;\; (on \; \mathbb{R}^8 - \{0\})
  \,.
$$

This 3-form $\phi$ defines a [[G2-structure]] on $S^7$. It is _nearly parallel_ in that

$$
  d \phi = 4 \star \phi
  \,.
$$

(e.g. [Lotay 12, def.2.4](#Lotay12))



## Related concepts

[[!include spheres -- contents]]

## References

* [[Martin Cederwall]], Christian R. Preitschopf, _The Seven-sphere and its Kac-Moody Algebra_, Commun. Math. Phys. 167 (1995) 373-394 ([arXiv:hep-th/9309030](http://arxiv.org/abs/hep-th/9309030))

* Takeshi &#212;no, _On the Hopf fibration $S^7 \to S^4$ over $Z$_, Nagoya Math. J.
Volume 59 (1975), 59-64. ([Euclid](http://projecteuclid.org/euclid.nmj/1118795554))

Relation to the [[Milnor fibration]]:

* [[Kenneth Intriligator]], [[Hans Jockers]], [[Peter Mayr]], [[David Morrison]], M. Ronen Plesser, _Conifold Transitions in M-theory on Calabi-Yau Fourfolds with Background Fluxes_, Adv.Theor.Math.Phys. 17 (2013) 601-699 ([arXiv:1203.6662](http://arxiv.org/abs/1203.6662))

An [[ADE classification]] of finite subgroups of $SO(8)$ [[free action|acting freely]] on $S^7$ (see at _[[group action on an n-sphere]]_) such that the quotient is [[spin structure|spin]] and has at least four [[Killing spinors]] (see also at [[ABJM model]]) is in

* [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], Sunil Gadhia, [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, 	JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_ ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761))

Discussion of [[subgroups]]:

* {#Varadarajan01} [[Veeravalli Varadarajan]], _Spin(7)-subgroups of SO(8) and Spin(8)_, Expositiones Mathematicae, 19 (2001): 163-177 ([pdf](https://core.ac.uk/download/pdf/81114499.pdf))


Discussion of [[exotic smooth structures]] on 7-spheres includes

* Wikipedia, _Exotic sphere_, [link](https://en.wikipedia.org/wiki/Exotic_sphere). 

The explicit construction of exotic 7-spheres by intersecting algebraic varieties with spheres is described in 

* {#Mil2} [[John Milnor]], "Singular points of complex hypersurfaces" , Princeton Univ. Press (1968). 

Discussion of (nearly) [[G2-structures]] on $S^7$ and [[calibrated submanifolds]] includes

* {#Lotay12} [[Jason Lotay]], _Associative Submanifolds of the 7-Sphere_, Proc. London Math. Soc. (2012) 105 (6): 1183-1214 ([arXiv:1006.0361](http://arxiv.org/abs/1006.0361), [talk slides](http://www.homepages.ucl.ac.uk/~ucahjdl/JDLotay_KIAS2011_slides.pdf))
 
On [[coset]]-realizations:

* {#Kramer98} Linus Kramer, _Octonion Hermitian quadrangles_, Bull. Belg. Math. Soc. Simon Stevin Volume 5, Number 2/3 (1998), 353-362 ([euclid:1103409015](https://projecteuclid.org/euclid.bbms/1103409015))

* {#Choquet-Bruhat+DeWitt-Morette00} Y. Choquet-Bruhat, C. DeWitt-Morette, _Analysis, Manifolds and Physics Part II_, North Holland 2000

* {#AwadaDuffPope83} M. A. Awada, [[Mike Duff]], [[Christopher Pope]], _$N=8$ Supergravity Breaks Down to $N=1$_, Phys. Rev. Lett. 50, 294 – Published 31 January 1983 ([doi:10.1103/PhysRevLett.50.294](https://doi.org/10.1103/PhysRevLett.50.294))

* {#DuffNilssonPope83} [[Mike Duff]], [[Bengt Nilsson]], [[Christopher Pope]], _Spontaneous Supersymmetry Breaking by the Squashed Seven-Sphere_, Phys. Rev. Lett. 50, 2043 – Published 27 June 1983; Erratum Phys. Rev. Lett. 51, 846  ([doi:10.1103/PhysRevLett.50.2043](https://doi.org/10.1103/PhysRevLett.50.2043))

* {#Baez} [[John Baez]], _Rotations in the 7th Dimension_, ([blog post](https://golem.ph.utexas.edu/category/2007/09/rotations_in_the_7th_dimension.html)), and _TWF 195_, ([webpage](http://math.ucr.edu/home/baez/week195.html))


[[!redirects 7-spheres]]

[[!redirects seven sphere]]
[[!redirects seven spheres]]



