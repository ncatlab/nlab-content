[[!redirects twistor]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Twistor space_ in the original sense of ([Penrose 67](#Penrose67)) is a [[complex manifold]] whose [[complex geometry]] is usefully related to the [[conformal geometry]] of ([[conformal compactification|conformally compactified]] [[complexification|complexified]]) 4-dimensional [[Minkowski spacetime]]. The _Penrose transform_ from twistor space to this [[spacetime]] yields powerful computational tools for studying certain [[quantum field theories]], in particular 4d [[Yang-Mills theory]]. Notably it sends [[ordinary cohomology]] classes on twistor space to [[self-dual Yang-Mills theory|self-dual Yang-Mills fields]] on spacetime ([Ward 77](#Ward77), [Ward-Wells 90](#WardWells90)). Morever, when twistor space is taken as a [[target space]] for [[twistor string theory]], then it serves to compute the [[MHV amplitudes]] in [[super Yang-Mills theory]] ([Witten 03](#Witten03)).

This _Penrose transform_ is exhibited by a [[correspondence]] of [[coset spaces]]/[[flag varieties]]/[[Grassmannians]] which is a special case of general such [[correspondences]] as they are studied in [[Schubert calculus]], [[geometric representation theory]], [[parabolic geometry]]. Therefore one can consider "generalized twistors" to be elements of certain [[flag varieties]] and "generalized Penrose transforms" to be those induced by the relevant [[correspondences]]. ([Baston-Eastwood 89](#BastonEastwood89), [Cap 01](#Cap01)). 

In this generality given a [[semisimple Lie group]] $G$ and two [[parabolic subgroups]] $P_1$ and $P_2$ with [[intersection]] $P_1 \cap P_2$, then the _twistor correspondence_ is the [[correspondence]] (see also at _[Schubert calculus -- Correspondences](http://ncatlab.org/nlab/show/Schubert+calculus#Correspondences)_ and at _[[horocycle correspondence]]_) of the form

$$
  \array{
      && G/(P_1 \cap P_2)
      \\
      & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
     G/P_1 && && G/P_2
  }
$$

given by the [[projections]] onto the two [[coset spaces]]/[[flag varieties]] and a _Penrose transform_ is an [[integral transform]]/pull-[[fiber integration|push]] $(p_2)_! \circ (p_1)^\ast$ through this correspondence.

In particular there are higher twistor spaces corresponding to higher dimensional [[Minkowski spacetimes]] which are useful for describing higher dimensional [[quantum field theory]], notably there are twistor spaces for 6-dimensional spacetime useful for the study of the [[6d (2,0)-superconformal QFT]] on the [[worldvolume]] of the [[M5-brane]] ([MREIC 11](#MREIC11)) with its [[self-dual higher gauge field]], the [[B-field]] .

The original _twistor correspondence_ ([Penrose 67](#Penrose67)) is the [[correspondence]]


$$
  \left(
  \array{
    && Gr_{1,2}(\mathbb{C}^4)
    \\
    & \swarrow && \searrow
    \\
    \mathbb{C}P^3 && && Gr_2(\mathbb{C}^4)
  }
  \right)
  \;\;\;\;\; 
    \simeq
  \;\;\;\;\; 
  \left(
  \array{
    && SL_\mathbb{C}(4)/SL_{\mathbb{C}}(2)
    \\
    & \swarrow && \searrow
    \\
    SL_{\mathbb{C}}(4)/SL_{\mathbb{C}}(3) 
     && && 
    SL_{\mathbb{C}}(4)/(SL_{\mathbb{C}}(2)\times SL_{\mathbb{C}}(2))
  }  
  \right)
  \,,
$$

where 

* the [[Grassmannian]] $G_2(\mathbb{C}^4)$ of [[planes]] in complexified 4d [[Minkowski spacetime]];

* the **twistor space** is the [[complex projective 3-space]] $\mathbb{C}P^3 = Gr_1(\mathbb{C}^4)$;

* the correspondence space $Gr_{1, 2}(\mathbb{C}^4)$ is the space of lines in planes in $\mathbb{C}^4$.

(e.g. [Ward-Wells 90](#WardWells90))

## Details

### Twistors for 4d Minkowski space
 {#TwistorsFor4dMinkowskiSpacetime}

We discuss the original twistors for the description of [[physics]] in 4d 
[[Minkowski spacetime]]. In summary, twistor space of 4d Minkowski space is the space of pairs consisting of a [[momentum]] vector and an [[angular momentum]] [[tensor]] subject to the constraint that the momentum is [[lightlike]] and of definite [[helicity]].

The formulation is all motivated from the form that basic quantities of [[special relativity|special relativistic physics]] take when [[vectors]] are expressed in [[spinor]] coordinates via the [exceptional spin isomorphism](spin+group#ExceptionalIsomorphisms) 

$$
  Spin(3,1) \simeq SL(2,\mathbb{C})
  \,.
$$

Under this identification a chiral [[spinor]] $\kappa$ is represented just by a pair of [[complex numbers]] $\xi, \eta \in \mathbb{C}$ and one may write the spinor as 

$$
  \left(
    \kappa^\alpha
  \right)
  = 
  \left(
    \array{
     \xi
     \\
     \eta
    }
  \right)
  \in
  \;\; \mathbb{C}^2
  \,.
$$

Moreover, via the non-degenerate bilinear pairing

$$
  \Gamma \;\colon\; S \otimes S \longrightarrow V
$$

given by the [[Clifford algebra]] (see at [[spin representation]] for details) one can express vectors

$$
  (x^i) = (x^0, x^1, x^2, x^3)
$$ 

in [[Minkowski spacetime]] as "bi-spinors" given by 2x2 [[Hermitean matrices]]

$$
  \begin{aligned}
    \left(x^{\alpha \beta}\right)
    & \coloneqq
    (x^i \gamma_i^{\alpha \beta})
    \\
    & 
    =
    \tfrac{1}{\sqrt{2}}
    \left(
      \array{
         x^0 + x^3 & x^1 + i x^2
         \\
         x^1 - i x^2 & x^0 - x^3
      }
    \right)
  \;\;
  \in Mat_{2}(\mathbb{C})
  \end{aligned}
  \,,
$$

where $\gamma_i$ denote the generators of the [[Clifford algebra]] given by the [[Pauli matrices]]. 

This is such that the [[Lorentz metric]] [[norm]] is just the [[determinant]] of this [[matrix]]

$$
  \Vert \left(x^i\right) \Vert 
   = 
   2 det\left(\left(x^{\alpha \beta} \right)\right)
  \,.
$$

This spinorial re-expression of vectors turns out to yield very efficient expressions particularly for those kinds of terms that appear in the observed physics of massless chiral particles, such as they appear in the [[standard model of particle physics]]. 


For instance a skew rank-2 [[tensor]] (2-from) $(F_{i j})$ with $F_{i j} = - F_{j i}$ (for instance the [[field strength]] of an [[electromagnetic field]]) has spinorial expression of the simple form

$$
  \begin{aligned}
    F_{\alpha_1 \beta_1 \alpha_2 \beta_2}
    & \coloneqq
    F_{i_1 i_2} \gamma^{i_1}_{\alpha_1 \beta_1} \gamma^{i_2}_{\alpha_2 \beta_2}
    \\
    & = 
    \phi_{\alpha_1 \alpha_2} \epsilon_{\beta_1 \beta_2}
    + 
    \psi_{\beta_1 \beta_2} \epsilon_{\alpha_1 \alpha_2}
  \end{aligned}
$$

for complex numbers $(\phi_{\alpha_1 \alpha_2})$ and $(\psi_{\beta_1 \beta_2})$. Here if $F$ itself is real-number valued, then $\psi$ is the [[complex conjugate]] of $\phi$ and hence any real 2-form is encoded equivalently by a bispinor $\phi$ via

$$
  F_{\alpha_1 \beta_1 \alpha_2 \beta_2}
  \coloneqq
  \phi_{\alpha_1 \alpha_2} \epsilon_{\beta_1 \beta_2}
  + 
  \overline{\phi}_{\beta_1 \beta_2} \epsilon_{\alpha_1 \alpha_2}
$$

Crucially the [[Hodge star|Hodge dual]] of a 2-form has then the simple expression

$$
  (\star F)_{\alpha_1 \beta_1 \alpha_2 \beta_2}
  = 
  - i \phi_{\alpha_1 \alpha_2} \epsilon_{\beta_1 \beta_2}
  + 
  i \psi_{\beta_1 \beta_2} \epsilon_{\alpha_1 \alpha_2}  
  \,,
$$

which is the first sign that [[self-dual Yang-Mills theory]] has a simpler expression in terms of such spinorial coordinates.

Now characterizing an [[elementary particle]] is (by the discussion at _[[unitary representation of the Poincaré group]]_) the [[momentum]] 4-vector $(p^i)$ and its [[angular momentum]] [[tensor]] $(M^{i j})$. A **twistor** is effectively a pair of spinorial coordinates expression this data for _massless_ and _chiral_ particles.

Here chiral means this: from combining the [[momentum]] and [[angular momentum]] one obtains the  [[Pauli-Lubanski vector]]

$$
  S_i \coloneqq \tfrac{1}{2} (\star M)_{i j} p^j
$$

and chiral particles satisfy 

$$
  S_i  = s p_i
$$

for some constant $s$. 

A _twistor_ is a set of spinorial coordinates for encoding tensors $\left(\left(p^i\right), \left(M^{i j}\right)\right)$ which satisfy

1. masslessness: $p^i p_i = 0$

1. chirality $S_i = s p_i$.

By the discussion at _[[celestial sphere]]_ we have that the first condition means equivalently that there is a single [[spinor]] $(\pi_\alpha)$ such that the spinorial expression for the momentum is

$$
  p_{\alpha \beta} = \pi_\alpha \overline{\pi}_\beta
  \,.
$$

By the above discussion of 2-forms we know moreover that $M^{i j}$ is encoded by a bispinor $\mu_{\alpha \beta}$ and imposing the chirality constraint one finds, using the above formula for the Hodge dual, that its solutions are parameterized precisely by another spinor $(\omega_\alpha)$ via

$$
  \overline{\mu}_{\alpha \beta} = i \omega_{(\alpha} \overline{\pi}_{\beta)}
$$

(where the parenthesis denote symmetrization of indices).

In summary, the possible momentum and angular momentum $(p^i, M^{i j})$ of massless chiral particles in 4d Minkowski spacetime is parameterized precisely by pair of spinors

$$
  Z = 
  \left(
    (\omega^\alpha), (\pi_\beta)
  \right)
  \;\;
  \in 
  \mathbb{C}^4
  \,.
$$

The image of this under modding out by a global complex factor is a Penrose _twistor_

$$
  Z \in \mathbb{C}P^3
  \,,
$$

an element of the [[complex projective 3-space]], called _twistor space_.


### Twistor space
 {#TwistorSpace}

To discuss twistor space for Minkowski spacetime, it is useful to work more generally with $d$-dimensional Minkowski spacetime for $d \in \{3,4,6,10\}$. If we also use the corresponding irreducible real [[spin representation]] then by the discussion [there](spin+representation#InTermsOfNormedDivisionAlgebraInDimension3To10), these are equivalently 2-component vectors over the real [[normed division algebras]] $\mathbb{K} \in \{\mathbb{R}, \mathbb{C}, \mathbb{H}, \mathbb{O}\}$, respectively. (See also at _[[supersymmetry and division algebra]]_, we follow [Bengtsson-Cederwall 88](#BengtssonCederwall88)).

With this, the vector space underlying $d$-dimensional [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ is identified with the space of $2 \times 2$ [[hermitian matrices]] with entries in $\mathbb{K}$

$$
  \mathbb{R}^{d-1,1} \simeq_{linear} Mat_{2 \times 2}^{hermitian}(\mathbb{K})
$$

and the [[Minkowski metric]] [[norm]]-square is then identified with the [[determinant]] of matrices:

$$
  \eta(v,v) = det(v)  \;\;\; v\in \mathbb{R}^{d-1,1} \simeq_{linear} Mat_{2 \times 2}^{hermitian}(\mathbb{K})
  \,.
$$

A choice of [[linear basis]] for this space is provided by the [[Pauli matrices]] with coefficients in $\mathbb{K}$, namely the matrices

$$
  (\Gamma_0^{\dot \alpha \alpha})
    \coloneqq
   \left[
      \array{
        1 & 0
        \\
        0 & -1
      }
   \right]
   \;\;\,,
   \;\;\;\;
  (\Gamma_1^{\dot \alpha \alpha})
    \coloneqq
   \left[
      \array{
        1 & 0
        \\
        0 & 1
      }
   \right]
   \;\;\,,
   \;\;\;\;
  (\Gamma_{n+1}^{\dot \alpha \alpha})
    \coloneqq
   \left[
      \array{
        0 & e_n
        \\
        \overline{e}_n & 0
      }
   \right]
$$

where $\{e_n\}_{n = 2}^{d}$ denotes an [[orthonormal basis]] for the elements of $\mathbb{K}$. Here we write 

$$
  \overline{(-)}
  \;\colon\;
  \mathbb{K}
    \longrightarrow
  \mathbb{K}
$$

for the operation of complex conjugation in $\mathbb{K}$, i.e. the $\mathbb{R}$-linear operation which sends the unit $1$ to itself, and sends imaginary elements to their negative.

In terms of this basis then a $d$-component vector $(X^\mu) \in \mathbb{R}^{d-1,1}$ is identified with the hermitian $2 \times 2$ matrix

$$
  (X^{\dot \alpha \alpha})
  \;\coloneqq\;
  (X^\mu \Gamma_\mu^{\dot \alpha \alpha})
   \;=\;
  \left[
    \array{
      x^0 + x^1 & x^{n} e_n
      \\
      x^n \overline{e}_n & x^0 - x^1
    }
  \right]
  \,.
$$

This presentation of [[Minkowski spacetime]] by $2 \times 2$ hermitian matrices with coefficients in $\mathbb{K}$ makes it very natural to consider also its "$\mathbb{K}$-ification" (hence [[complexification]] in the case that $d = 4$ and $\mathbb{K} = \mathbb{C}$), namely the space of _all_ $2 \times 2$ [[matrices]] with entries in $\mathbb{K}$:

$$
  \mathbb{K}\mathbb{R}^{d-1,1}
    \coloneqq
   Mat_{2\times 2}(\mathbb{K})
  \,.
$$

This space carries the operation of [[Hermitian conjugation]]

$$
  X \mapsto X^\dagger
$$

as an [[involution]], and ordinary $d$-dimensional Minkowski spacetime is hence the [[fixed point]] set of this involution.


By the discussion [there](spin+representation#InTermsOfNormedDivisionAlgebraInDimension3To10), the Spin-invariant pairing of two real spinors $\psi, \phi \in \mathbb{K}^2$ to a vector $\overline{\psi} \Gamma \phi \in Mat_{2\times 2}^{hermitian}(\mathbb{K})$ is given by ([prop.](spin+representation#RealSpinorPairingsViaDivisionAlg))

$$
  (\overline{\psi}\Gamma \phi)
   \coloneqq
   \psi \phi^\dagger + \phi \psi^\dagger
  \,.
$$

In particular the pairing of a spinor $\psi = (\psi_{\dot \alpha})$ with itself is

$$
  (\psi \psi^\dagger)_{\alpha \dot\alpha}
  =
  2
  \overline{\psi}_\alpha \psi_{\dot \alpha}
  \,.
$$

Since, as hermitian matrices, the $2 \times 2$ matrices arising this way are manifestly precisely the hermitian projection operators on 1-dimensional linear subspaces of $\mathbb{K}^2$, these are precisely the $2 \times 2$ hermitian matrices with vanishing determinant. Hence the future-oriented [[lightlike]] vectors in Minkowski spacetime in $d = \{3,4,6,10\}$ are precisely those that arise as the pairing of a chiral spinor with itself.

The above formula shows that as we rescale $\psi \mapsto k \psi$ with $k \in \mathbb{K}$, then the corresponding lightlike vector is sent to itself, rescaled by the real number $k \overline{k} \in \mathbb{R}$. Hence the direction of lightlike vectors is parameterized by the [[projective space]] $\mathbb{K}P^1$. At least for $\mathbb{K} = \mathbb{C}$ (the [[complex numbers]]) this is called the [[celestial sphere]] (in this case: the [[Riemann sphere]] $\mathbb{C}P^1$).

Lightlike vectors in $\mathbb{R}^{d-1,1}$ up to scale are equivalently loci of lightlike [[geodesics]] through the origin. A general lightlike geodesic in $\mathbb{R}^{d-1,1}$ is instead parameterized by

$$
  \tau \mapsto (X^{\dot \alpha \alpha} + \tau {\psi}^\alpha \overline{\psi}^{\dot \alpha})
$$

for some offset $(X^{\dot \alpha \alpha})$. To encode this offset into spinors, consider the image of $\psi$ under the Clifford action with $X$:

$$
  \omega^\alpha \coloneqq \psi_{\dot \alpha} X^{\dot \alpha \alpha}
  \,.
$$

This relation bewteen $\omega$ and $\psi$ is called the _incidence relation_ in this context.

The locus of the lightlike geodesic does not change as we rescale $\psi$ by elements $k \in \mathbb{K}$, and then $\omega$ gets rescaled accordingly. Hence the pair $(\omega^\alpha, \psi_{\dot \alpha})$ regarded as encoding lightlike geodesics in Minkowski spacetime should be thought of as an element of the [[projective space]] 

$$
  \mathbb{K}P^3
   \coloneqq \{ (Z^{a}) = (\omega^\alpha,\psi_{\dot \alpha}) \in \mathbb{K}^4 \}_{( (Z^a) \sim (k Z^a) \vert k \in \mathbb{K} )}.
$$

This is the _twistor space_ corresponding to the given Minkowski spacetime.

However, by the above definition of $\omega^\alpha$, not every element of this space corresponds to a lightlike geodesic. Rather (for $d \in \{3,4,6\}$) it is only those satisfying

$$
  \omega^\alpha \overline{\psi}_\alpha
    = 
  \psi_{\dot \alpha} \overline{\omega}^{\dot \alpha}
$$

reflecting the fact that $(X^{\dot \alpha \alpha})$ is a hermitian matrix, instead of a general $2\times 2$ matrix. (For $d = 10$ there is no elegant statement like this, due to the non-associativity of the [[octonions]] $\mathbb{K} = \mathbb{O}$. But there is nevertheless an analogue of the twistor transform in 10d [Witten 86](#Witten86)).

Hence the subspace inclusion

$$
  \mathbb{R}^{d-1,1} \hookrightarrow \mathbb{K}\mathbb{R}^{d-1,1}
$$

of Minkowski-spacetime into its $\mathbb{K}$-ification, corresponds to a subspace

$$
  \mathcal{N} \hookrightarrow \mathbb{K}P^3
$$

of twistor space. This is called the space of _null twistors_, or the _spin shell_.

If we consider the metric on $\mathbb{K}^4$ given in component by

$$
  \left[
    \array{
       0 & \delta^\beta_\alpha
       \\
       - \delta^{\dot \alpha}_{\dot \beta} & 0
    }
  \right]
$$

then this subspace is the [[quadric]] given by the equation

$$
  Z^a \overline{Z}_a = 0
  \,.
$$

Now conversely, given $Z^a = (\omega^\alpha, \psi_{\dot\alpha})$ not equal to zero and satisfying this condition in that there is a hermitian $X^{\dot \alpha \alpha}$ with $\omega^{\alpha} = \psi_{\dot \alpha} X^{\dot \alpha \alpha}$, then also every hermitian matrix of the form

$$
  X^{\dot \alpha \alpha} + \tau \psi^{\dot \alpha}\psi^\alpha
$$

(for $\tau \in \mathbb{R}$, hence every point on the lightlike geodesic through $X$ in the direction of $\psi \psi^\dagger$) satisfies the relation (since the spinor index is raised with $(\epsilon^{\dot \alpha \dot \beta})$, which is skew symmetric).  This way non-zero points in $\mathcal{N} \hookrightarrow \mathbb{K}P^3$ correspond to lightlike geodesics in Minkowski spacetime. 

<img src="http://ncatlab.org/nlab/files/TwistorSpaceCorrespondence.jpg" width="700">

(graphics from [Adamo 13](#Adamo13))

This correspondence extends also to the 0-point in $\mathcal{N}$ if one passes to "compactified Minkowski spacetime", given by the [[Grassmannian]] $Gr_2(\mathbb{C}^4)$ of complex planes in $\mathbb{C}^4$ (review includes [Fioresi-Lledo-Varadarajan 07, section 2](#FioresiLledoVaradarajan07)).




## Related concepts

* [[twistor fibration]]

* A real analog of this is the _[[Radon transform]]_.

* [[spinor]]

* [[twistor string theory]]

* [[MHV amplitude]]

* [[Radon transform]]

* [[Schubert calculus]]

* [[celestial sphere]], [[quadric]], [[Klein quadric]]

## References

### General

The notion originates in 

* {#Penrose67} [[Roger Penrose]], _Twistor algebra_,  Journal of Mathematical Physics 8 (2): 345&#8211;366, (1967) 

* [[Roger Penrose]], _The twistor programme, Reports on Mathematical Physics 12 (1): 65&#8211;76 (1977)

Key developments concerning [[scattering amplitudes]] are due to 

* [[Andrew Hodges]], _Twistor diagrams_ ([web](http://www.twistordiagrams.org.uk/papers/index.html))

The relation to [[self-dual Yang-Mills theory]] is due to 

* {#Ward77} R. S. Ward, _On Selfdual gauge fields_, Phys. Lett. A61 (1977) 81-82.
 

Introductions and surveys include

* [[Yuri Manin]], chapters 1 and 2 of _[[Gauge Field Theory and Complex Geometry]], Grundlehren der Mathematischen Wissenschaften 289, Springer 1988

* Fedja Hadrovich, _Twistor primer_ ([html](http://users.ox.ac.uk/~tweb/00004), [pdf](http://henry.pha.jhu.edu/twistors.pdf))

* Paul Bair, _Introduction to twistors_ ([pdf](http://www.math.jussieu.fr/~helein/encyclopaedia/baird-twistors.pdf))

* S. A. Huggett, K. P. Todd, _An introduction to twistor theory_, Cambridge University Press (1985)

* Liana David, _The Penrose transform and its applications_, 2001 ([pdf](http://www.maths.ed.ac.uk/pg/thesis/david.pdf))

* {#Dunajski09} Maciej Dunajski, _Twistor theory and differential equations_, J.Phys. __A42__:404004 (2009) [arXiv:0902.0274](http://arxiv.org/abs/0902.0274) [doi](https://doi.org/10.1088/1751-8113/42/40/404004)

* [[Roger Penrose]], _Twistor theory_, talk at _[[New Spaces for Mathematics and Physics]]_, IHP Paris, 2015 ([video recording](https://www.youtube.com/watch?v=kmYfYOW0vSg))

* {#FioresiLledoVaradarajan07} R. Fioresi, M. A. Lledo, [[Veeravalli Varadarajan]], _The Minkowski and conformal superspaces_, J.Math.Phys.48:113505,2007 ([arXiv:0609813](https://arxiv.org/abs/math/0609813))

* [[Michael Atiyah]], Maciej Dunajski, Lionel Mason, _Twistor theory at fifty: from contour integrals to twistor strings_ ([arXiv:1704.07464](https://arxiv.org/abs/1704.07464))

* {#Adamo17} Tim Adamo, _Lectures on twistor theory_ ([arXiv:1712.02196](https://arxiv.org/abs/1712.02196))

* L. J. Mason, N. M. J. Woodhouse, _Integrability, self-duality and twistor theory_, OUP 1996
* R. S. Ward, R. O. Wells, Jr. _Twistor geometry and field theory_, Cambridge Univ. Press 1990

Review of the application in [[super Yang-Mills theory]] includes

* {#Adamo13} [[Tim Adamo]], _Twistor actions for gauge theory and gravity_ ([arXiv:1308.2820](https://arxiv.org/abs/1308.2820)) 

See also 

* Wikipedia, _[Twistor theory](http://en.wikipedia.org/wiki/Twistor_theory)_


### Relation to geometric representation theory and parabolic geometry

A discussion in the general context of [[geometric representation theory]] is in

* R. J. Baston, M. G. Eastwood, _The Penrose transform its interaction with representation theory_ Oxford Science Publications, Clarendon Press, 1989 
 {#BastonEastwood89}

and the further generalization to [[Cartan geometry]]/[[parabolic geometry]] is discussed in

* {#Cap01} [[Andreas Čap]], _Correspondence spaces and twistor spaces for parabolic geometries_, J. Reine Angew. Math. 582 (2005) 143-172 ([arXiv:math/0102097](http://arxiv.org/abs/math/0102097))
  
### Palatial twistor theory

* Roger Penrose, _Palatial twistor theory and the twistor googly problem_, Phil. Trans. Royal Soc. A373: 20140237 (2015) [doi](http://dx.doi.org/10.1098/rsta.2014.0237)
* R. Penrose, _Twistor theory as an approach to fundamental physics_, in: Foundations of mathematics and physics one century after Hilbert, 253-285 (2018), ed. Joseph Kouneiher [doi](https://doi.org/10.1007/978-3-319-64813-2_10)

### Application to quantum field theory

More on traditional applications to [[quantum field theory]] is in 

* {#WardWells90} R.S. Ward, R.O. Wells, _Twistor geometry and field theory_, Cambridge Univ. Press 1990.
  

The relation of twistor geometry to [[MHV amplitudes]] in 4d [[Yang-Mills theory]] and [[twistor string theory]] is due to 

* {#Witten03} [[Edward Witten]], _Perturbative Gauge Theory As A String Theory In Twistor Space_, Commun. Math. Phys. 252:189-258, 2004 ([arXiv:hep-th/0312171](http://arxiv.org/abs/hep-th/0312171))
  


Surveys of the resulting modern application of twistors in field theory include

* David Skinner, _The geometry of scattering amplitudes_, talk notes, November 2009 ([pdf](http://research.physics.unc.edu/string/transparencies/trans_20091112.pdf))


### Twistors in higher dimensions

Discussion of twistors in dimensions 3,4,6 and 10 using the [[normed division algebras]] (as in [[supersymmetry and division algebras]]) is in

* {#BengtssonCederwall88} [[Ingemar Bengtsson]], [[Martin Cederwall]], _Particles, Twistors and the Division Algebras_, Nucl.Phys. B302 (1988) 81-103 ([spire:247269](http://inspirehep.net/record/247269), <a href="https://doi.org/10.1016/0550-3213(88)90667-0">doi:10.1016/0550-3213(88)90667-0</a>)

* {#Cederwall93} [[Martin Cederwall]], _Introduction to Division Algebras, Sphere Algebras and Twistors_ ([arXiv:hep-th/9310115](https://arxiv.org/abs/hep-th/9310115))


and specifically for dimension 10 

* {#Witten86} [[Edward Witten]], _Twistor-like transform in ten dimensions_, Nuclear Physics __B266__:2, 245-264. (1986) (<a href="http://dx.doi.org/10.1016/0550-3213(86)90090-8">10.1016/0550-3213(86)90090-8</a>)

and its [[anti de Sitter spacetime|AdS]] version:

* [[Alex Arvanitakis]], Alec E. Barns-Graham, [[Paul Townsend]], _Twistor description of spinning particles in AdS_, JHEP 01 (2018) 059 ([arXiv:1710.09557](https://arxiv.org/abs/1710.09557))


#### Application to the 6d self-dual 2-form field
 {#ReferencesApplicationToSelfDual2FormField}

A general discussion of Penrose-Ward-type transforms sending [[circle 2-bundles]] ([[holomorphic line 2-bundles]]) on some twistor space to [[circle 2-bundles with connection]] and self-dual [[curvature]] 3-form on spacestime (expected to play a role in the description of the [[6d (2,0)-superconformal QFT]]) is in 

* [[David Chatterjee]], sections 4 and 8 of _On gerbs_, 1998 ([pdf](http://people.maths.ox.ac.uk/hitchin/hitchinstudents/chatterjee.pdf))

* L. J. Mason, R. A. Reid-Edwards, A. Taghavi-Chabert, appendix of _Conformal field theories in six-dimensional twistor space_, J. Geom. Phys. 62 (2012), no. 12, 2353-2375 ([arXiv:1111.2585](http://arxiv.org/abs/1111.2585))
 {#MREIC11}

* [[Christian Saemann]], [[Martin Wolf]], _On twistors and conformal field theories from six dimensions_, J. Math. Phys. 54:013507, 2013  ([arXiv.1111.2539](http://arxiv.org/abs/1111.2539))

More generally, there are arguments that the [[worldvolume]] theory of several coincident [[M5-branes]] carries not just an abelian but a nonabelian [[higher gauge field]] given by a [[principal 2-bundle]] [[principal 2-connection]].

The idea of generalizing the Penrose-Ward transform to one that takes nonabelian [[principal 2-bundles]] to [[self-dual higher gauge field|self-dual]] [[principal 2-connections]] is explored in 

* [[Christian Saemann]], [[Martin Wolf]], _Six-dimensional superconformal field theories from principal 3-bundles over twistor space_ ([arXiv:1305.4870](http://arxiv.org/abs/1305.4870))


[[!redirects twistor spaces]]

[[!redirects twistor]]
[[!redirects twistors]]


[[!redirects twistor theory]]

[[!redirects twistor space]]
[[!redirects twistor spaces]]

[[!redirects twistor correspondence]]
[[!redirects twistor correspondences]]

[[!redirects Penrose transform]]
[[!redirects Penrose transforms]]

[[!redirects twistor transform]]
[[!redirects twistor transforms]]


[[!redirects Penrose transformation]]
[[!redirects Penrose transformations]]

[[!redirects Penrose twistor transform]]
[[!redirects Penrose twistor transforms]]

[[!redirects Penrose twistor transformation]]
[[!redirects Penrose twistor transformations]]

[[!redirects Penrose-Ward transform]]
[[!redirects Penrose-Ward transforms]]

[[!redirects Penrose-Ward transformation]]
[[!redirects Penrose-ward transformations]]

[[!redirects Penrose-Ward twistor transform]]
[[!redirects Penrose-Ward twistor transforms]]

[[!redirects Penrose-Ward twistor transformation]]
[[!redirects Penrose-Ward twistor transformations]]