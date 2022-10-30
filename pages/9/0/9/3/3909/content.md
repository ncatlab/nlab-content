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

_Twistor space_ in the original sense of ([Penrose 67](#Penrose67)) is a [[complex manifold]] whose [[complex geometry]] is usefully related to the [[conformal geometry]] of ([[one-point compactification|compactified]] [[complexification|complexified]]) 4-dimensional [[Minkowski spacetime]]. The _Penrose transform_ from twistor space to this [[spacetime]] yields powerful computational tools for studying certain [[quantum field theories]], in particular 4d [[Yang-Mills theory]]. Notably it sends [[ordinary cohomology]] classes on twistor space to [[self-dual Yang-Mills theory|self-dual Yang-Mills fields]] on spacetime ([Ward 77](#Ward77), [Ward-Wells 90](#WardWells90)). Morever, when twistor space is taken as a [[target space]] for [[twistor string theory]], then it serves to compute the [[MHV amplitudes]] in [[super Yang-Mills theory]] ([Witten 03](#Witten03)).

This _Penrose transform_ is exhibited by a [[correspondence]] of [[coset spaces]]/[[flag varieties]]/[[Grassmannians]] which is a special case of general such [[correspondences]] as they are studied in [[Schubert calculus]], [[geometric representation theory]], [[parabolic geometry]]. Therefore one can consider "generalized twistors" to be elements of certain [[flag varieties]] and "generalized Penrose transforms" to be those induced by the relevant [[correspondences]]. ([Baston-Eastwood 89](#BastonEastwood89), [Cap 01](#Cap01)). 

In this generality given a [[semisimple Lie group]] $G$ and two [[parabolic subgroups]] $P_1$ and $P_2$ with [[intersection]] $P_1 \cap P_2$, then the _twistor correspondence_ is the [[correspondence]] (see alsoat [Schubert calculus -- Correspondences](http://ncatlab.org/nlab/show/Schubert+calculus#Correspondences) and at _[[horocycle correspondence]]_) of the form

$$
  \array{
      && G/(P_1 \cap P_2)
      \\
      & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
     G/P_1 && && G/P_2
  }
$$

given by the [[projections]] onto the two [[coset spaces]]/[[flag varieties]] and a _Penrose transform_ is an [[integral transform]]/pull-[[fiber integration|push]] $(p_1)_! \circ (p_1)^\ast$ through this correspondence.

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

* the **twistor space** is the [[complex projective space]] $\mathbb{C}P^3 = Gr_1(\mathbb{C}^4)$;

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

for complex numbers $(\phi_{\alpha_1 \alpha_2})$ and $(\psi_{\beta_1 \beta_2})$. Here if $F$ itself is a real-number valued, then $\psi$ is the [[complex conjugate]] of $\phi$ and hence any real 2-form is encoded equivalently by a bispinor $\phi$ via

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

In summary then the possible momentum and angular momentum $(p^i, M^{i j})$ of massless chiral particles in 4d Minkowski spacetime is parameterized precisely by pair of spinors

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

an element of the 3-dimensional [[complex projective space]].


Given such a pair, conversely it defines a point in Minkowski spacetime.


### 4d Klein correspondence


A twistor $(\omega^\alpha, \pi_\beta)$ determines a complex [[plane]] in complexified [[Minkowski spacetime]] whose points $(x^i)$ are characterized by the [[equation]]

$$
  \omega^\alpha = x^{\alpha \beta} \pi_\beta
  \,.
$$

These planes are [[lightlike]].

This assignment is called the _Klein correspondence_.




## Related concepts

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

* [[Roger Penrose]], _Twistor algebra_,  Journal of Mathematical Physics 8 (2): 345&#8211;366, (1967) 
 {#Penrose67}

* [[Roger Penrose]], _The twistor programme, Reports on Mathematical Physics 12 (1): 65&#8211;76 (1977)

Key developments concerning [[scattering amplitudes]] are due to 

* [[Andrew Hodges]], _Twistor diagrams_ ([web](http://www.twistordiagrams.org.uk/papers/index.html))

The relation to [[self-dual Yang-Mills theory]] is due to 

* R. S. Ward, _On Selfdual gauge fields_, Phys. Lett. A61 (1977) 81-82.
 {#Ward77}

Introductions and surveys include

* Fedja Hadrovich, _Twistor primer_ ([html](http://users.ox.ac.uk/~tweb/00004/), [pdf](http://henry.pha.jhu.edu/twistors.pdf))

* Paul Bair, _Introduction to twistors_ ([pdf](http://www.math.jussieu.fr/~helein/encyclopaedia/baird-twistors.pdf))

* S. A. Huggett, K. P. Todd, _An introduction to twistor theory_, Cambridge University Press (1985)

* Liana David, _The Penrose transform and its applications_, 2001 ([pdf](http://www.maths.ed.ac.uk/pg/thesis/david.pdf))

See also 

* Wikipedia, _[Twistor theory](http://en.wikipedia.org/wiki/Twistor_theory)_


### Relation to geometric representation theory and parabolic geometry

A discussion in the general context of [[geometric representation theory]] is in

* R. J. Baston, M. G. Eastwood, _The Penrose Transform Its Interaction with Representation Theory_ Oxford Science Publications, Clarendon Press, 1989 
 {#BastonEastwood89}

and the further generalization to [[Cartan geometry]]/[[parabolic geometry]] is discussed in

* [[Andreas Cap]], _Correspondence spaces and twistor spaces for parabolic geometries_, J. Reine Angew. Math. 582 (2005) 143-172 ([arXiv:math/0102097](http://arxiv.org/abs/math/0102097))
  {#Cap01}

### Application to quantum field theory

More on traditional applications to [[quantum field theory]] is in 

* R.S. Ward, R.O. Wells, _Twistor geometry and field theory_, Cambridge Univ. Press 1990.
  {#WardWells90}

The relation of twistor geometry to [[MHV amplitudes]] in 4d [[Yang-Mills theory]] and [[twistor string theory]] is due to 

* [[Edward Witten]], _Perturbative Gauge Theory As A String Theory In Twistor Space_, Commun. Math. Phys. 252:189-258, 2004 ([arXiv:hep-th/0312171](http://arxiv.org/abs/hep-th/0312171))
  {#Witten03}

Surveys of the resulting modern application of twistors in field theory include

* David Skinner, _The geometry of scattering amplitudes_, talk notes, November 2009 ([pdf](http://research.physics.unc.edu/string/transparencies/trans_20091112.pdf))



### Application to the 6d self-dual 2-form field
 {#ReferencesApplicationToSelfDual2FormField}

A general discussion of Penrose-Ward-type transforms sending [[circle 2-bundles]] ([[holomorphic line 2-bundles]]) on some twistor space to [[circle 2-bundles with connection]] and self-dual [[curvature]] 3-form on spacestime (expected to play a role in the description of the [[6d (2,0)-superconformal QFT]]) is in 

* [[David Chatterjee]], sections 4 and 8 of _On Gerbs_, 1998 ([pdf](http://people.maths.ox.ac.uk/hitchin/hitchinstudents/chatterjee.pdf))

* L. J. Mason, R. A. Reid-Edwards, A. Taghavi-Chabert, appendix of _Conformal Field Theories in Six-Dimensional Twistor Space_, J. Geom. Phys. 62 (2012), no. 12, 2353-2375 ([arXiv:1111.2585](http://arxiv.org/abs/1111.2585))
 {#MREIC11}

* [[Christian Saemann]], Martin Wolf, _On Twistors and Conformal Field Theories from Six Dimensions_, J. Math. Phys. 54:013507, 2013  ([arXiv.1111.2539](http://arxiv.org/abs/1111.2539))

More generally, there are arguments that the [[worldvolume]] theory of several coincident [[M5-branes]] carries not just an abelian but a nonabelian [[higher gauge field]] given by a [[principal 2-bundle]] [[principal 2-connection]].

The idea of generalizing the Penrose-Ward transform to one that takes nonabelian [[principal 2-bundles]] to [[self-dual higher gauge field|self-dual]] [[principal 2-connections]] is explored in 

* [[Christian Saemann]], Martin Wolf, _Six-Dimensional Superconformal Field Theories from Principal 3-Bundles over Twistor Space_ ([arXiv:1305.4870](http://arxiv.org/abs/1305.4870))




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