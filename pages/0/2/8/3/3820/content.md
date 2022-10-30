
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _covariant phase space_ of a system in [[physics]] is the [[space]] of all of its solutions to its [[classical mechanics|classical equations of motion]], the space of _classical trajectories_ of the system.  Often one considers a parameterization of this by boundary data on choice a [[Cauchy surface]]. This parameterization is what traditionally is just called a "phase space". The "covariant" in "covariant phase space" is to indicated that it goes without any unnatural choices.

For a system described by [[Lagrangian]] mechanics this comes canonically equipped with a [[presymplectic structure]]. A proper _phase space_ or _reduced phase space_ is a subspace or [[quotient space]] of the covariant phase space on which the presymplectic structure refines to a [[symplectic manifold|symplectic structure]] or [[Poisson manifold|Poisson strucure]]. 

Typically these phase spaces are (locally) naturally parameterized by the suitable boundary conditions which uniquely determine the corresponding history of the physical system. Much of the literature on phase spaces deals with parameterizing these boundary conditions. 

For instance for a [[relativistic particle|particle]] propagating on a [[Riemannian manifold]] $X$ with the usual [[action functional]], a trajectory is uniquely fixed by the position $x \in X$ and the momentum $p \in T^*_x X$ of the particle at a given time. Correspondingly the space of all solutions and hence the (covariant) phase space of the system may be identified with the [[cotangent bundle]] $T^* X$ of $X$.  
 
However, even reduced phase spaces are not all cotangent bundles, typically not, for instance, if they are obtained by [[symplectic reduction]]. This way a finite-dimensional phase space can sometimes describe continuous systems (e.g. in hydrodynamics) whch have infinitely many degrees of freedom; that phase space is however not a cotangent bundle of something in general. 


## Covariant phase space

There are two main routes to the construction of the covariant phase space, 

* (S) via [[presymplectic structure]];

* (P) via [[Poisson algebra]] structure.

### (S) Via pre-symplectic structures
 {#ViaSymplecticStructure}

We describe the canonical [[presymplectic structure]] on the covariant phase space of a [[local action functional]]. The _covariant phase space_ is defined as the space of critical points of an action functional or, equivalently, the space of solutions of its [[Euler-Lagrange equation]]s, also known as the _shell_. The shell is naturally embedded as a subset of the space of all field configurations. Terminology is as in the discussion at [[variational bicomplex]].

Let $E \to X$ be a smooth [[fiber bundle]] over [[spacetime]] $X$ and $J(E)$ the corresponding [[jet bundle]]. The [[local action functional]]

$$
  S : \Gamma(E) \to \mathbb{R}
$$

is by definition given by a [[Lagrangian]]

$$
  L : \Gamma(J(E)) \to \Omega^{dim X}(X)
$$

as

$$
  S : \phi \mapsto \int_X L(j_\infty(\phi))
  \,.
$$

The [[variational calculus|variation]] of $S$ is

$$
  \begin{aligned}
    \delta S (\phi) 
     &= 
    \int_X \delta L(j_\infty(\phi))
    \\
     &= 
    \int_X EL(\phi) \delta \phi 
      + 
     \int_X d_{dR} \theta(\phi)
    \,,
  \end{aligned}
$$

where $EL(\phi) = 0$ is the [[Euler-Lagrange equation]] on $\phi$, and where $EL(\phi)\delta\phi$ is a degree-$(1,dim X)$ and $\theta$ is a deggre-$(1, dim X - 1)$ element in the [[variational bicomplex]] (one variational form degree and, respectively, $dim X$ or $(dim X - 1)$-spacetime form degrees). On a local [[coordinate]] patch $\{x^i\}$ for $X$ this is 

$$
  \theta(\phi) 
    = 
  (\iota_{\partial_i} \frac{\partial L}{\partial_i \phi^a} )
   \delta \phi^a
  \,.
$$

The above definition of $EL$ and $\theta$ in terms of $\delta S$ yields the following identity upon taking another exterior variational derivative of both sides

$$
  \delta(\delta S(\phi)) = 0
  = \int_X \left[
    \delta(EL(\phi)) \wedge \delta\phi
    + d_{dR} \delta \theta(\phi) \right]
  \, ,
$$

where the first term on the right clearly vanishes when pulled back to the shell, $EL(\phi)=0$ on $X$. The above wedge product is between variational forms. This implies that the presymplectic current density, $\omega(\phi) = \delta(\theta(\phi))$, is de Rham-closed on shell:

$$
\begin{aligned}
  d_{dR} \iota^* \omega(\phi)
  &= d_{dR} \iota^* (\delta \theta(\phi)) \\
  &= \iota^* d_{dR} (\delta \theta(\phi)) \\
  &= -\iota^* \delta(EL(\phi)) \wedge \delta\phi \\
  &= 0
  \, ,
\end{aligned}
$$

where $\iota$ is the embedding of the solutions of the [[Euler-Lagrange equation]]s  (the shell) into the space of all field configurations. The reason is that $\iota^* \delta(EL(\phi)) = 0$ for each $x\in X$, since the functions $EL(\phi)$ are all constant (in fact $0$) on solutions.

The variational 1-form on the space of field configurations

$$
  \Theta = \int_{X|_{in}} \theta(\phi)
$$

given by an [[integration]] over a [[Cauchy surface]] $X|_{in}$ is the potential for the presymplectic form 

$$
  \Omega = \delta \Theta = \int_{X|_{in}} \delta(\theta(\phi))
  = \int_{X|_{in}} \omega(\phi)
$$

on the space of field configurations. Since $\omega(\phi)$ is de Rham-closed on shell, the the pullback of the presymplectic form $\iota^* \Omega$ is independent of the choice of the surface $X|_{in}$ (provided the choice is restricted to a single homology class of surfaces).

+-- {: .un_claim}
###### Claim

The presymplectic form $\iota^* \Omega$ on the covariant phase space is symplectic iff the linearized [[Euler-Lagrange equation]]s, $EL(\phi)=0$, have a locally well-posed initial value problem on $X|_{in}$. In particular, in the presence of gauge symmetries, due to the failure of uniqueness of solutions for given initial data on $X|_{in}$, the form $\iota^*\Omega$ is only presymplectic.

=--

However, the infinitesimal actions of gauge symmetries exhaust the kernel of the $\iota^* \Omega$ and upon performing [[symplectic reduction]], we obtain the space of orbits of solutions under the action of gauge symmetries, which is the _physical_ or _reduced phase space_.

Notice that the form $\Omega$, on the field configuration space, does depend on the choice of Cauchy surface. Performing [[symplectic reduction]] gives the symplectic space of equivalence classes of solutions of equations of motion modulo [[gauge transformation]]s, and hence also the _reduced phase space_. Thus, the end point of the reduction no longer depends on the choice of the Cauchy surface.

#### Application to the inverse problem of the calculus of variations
 {#InverseProblem}

We use same notation as the preceding section. Namely dependence on $\phi$ in local forms really means dependence on finitely many components of the infinite jet $j^\infty(\phi)$. Also, $\iota$ denotes the embedding of the space of solutions in the space of field configurations. Moreover, we presume to work on a sufficiently small neighborhoods in the space of solutions and field configurations that the Poincar\'e lemma applies.

Consider a system of partial differential equations $P(\phi)=0$, together with a local presymplectic form $\Omega = \int_X \omega(\phi)$, where $\omega(\phi)$ is a degree-$(2,dim X-1)$ element of the [[variational bicomplex]], that is $\delta \omega = 0$. Suppose further that presymplectic current density $\omega(\phi)$ is de Rham conserved on solutions:

$$
  d_{dR}  \iota^* \omega(\phi) = \iota^* d_{dR} \omega(\phi) = 0
  \quad \implies \quad
  d_{dR} \omega(\phi) = P(\phi) \lambda(\phi) + \delta(P(\phi)) \wedge \mu(\phi)
    = P(\phi) (\lambda(\phi) - \delta\mu(\phi)) + \delta (P(\phi)\mu(\phi))
  \, ,
$$
where $\lambda$ and $\mu$ are systems (suitably contracted with the $P(\phi)$ system) of degree-$(2,dim X)$ and degree-$(1,dim X)$ elements of the [[variational bicomplex]]. Using the variational closure of $\omega(\phi)$, we can conclude that
$\delta(P(\phi)(\lambda(\phi)-\delta\mu(\phi))) = 0$ and thus $P(\phi)(\lambda(\phi)-\delta(\phi)) = \delta(P(\phi)\lambda'(\phi))$. [Justify why the representative on the last RHS can be chosen proportional to $P(\phi)$.]

On the other hand, the variational closure of $\omega(\phi)$ also implies the existence of a degree-$(1,dim X-1)$ form $\theta(\phi)$, such that $\delta(\theta(\phi)) = \omega(\phi)$. The following identity then allows us to (locally) reconstruct a Lagrangian whose [[Euler-Lagrange equation]]s are satisfied by solutions to $P(\phi)=0$.

$$
\begin{aligned}
  \delta(d_{dR} \theta(\phi))
    &= - d_{dR}(\delta\theta(\phi)) \\
    &= - d_{dR} \omega(\phi) \\
    &= - \delta[P(\phi)(\lambda'(\phi)+\mu(\phi))] \\
  \implies d_{dR}\theta(\phi) - \delta L(\phi)
    &= -P(\phi)\lambda''(\phi)
  \, ,
\end{aligned}
$$

where $\lambda''(\phi)$ is a degree-$(1,dim X)$ form and $L(\phi)$ is a Lagrangian degree-$(0,dim X)$ form. Rearranging the last equality as

$$
  \delta L(\phi) = P(\phi)\lambda''(\phi) + d_{dR}\theta(\phi) \, ,
$$
we conclude that the [[Euler-Lagrange equation]]s of $L(\phi)$ are satisfied on solutions of $P(\phi)=0$, since $EL(\phi)\delta\phi = P(\phi)\lambda''(\phi)$.

### (P) Via Poisson structures
 {#ViiaPoissonStructure}
 
The covariant phase space can be embedded into the 
[[space of field configurations]] as a subspace of the set of solutions that transversely intersects [[gauge orbit]]s. This embedding is characterized as the [[zero locus]] of the [[equations of motion]] and some [[gauge fixing]] conditions. The non-degenerate [[Poisson structure]] on the algebra of functions on the covariant phase space is given by the [[Peierls bracket]]. 

The Peierls bracket of two functions $A$ and $B$ is the antisymmetrized influence on $B$ of an infinitesimal perturbation of a gauge-fixed action by function that restricts to $A$ on the embedding. The algebra of functions on the space of field configurations becomes a [[Poisson algebra]] in the following way. Pick a set of functions on the space of field configurations that restrict to a non-degenerate coordinate system on the embedded covariant phase space. These functions, together with the equations of motion and gauge fixing conditions define a Poisson bivector by being declared canonical, such that the kernel of the bivector coincides with the ideal generated by the equations of motion
and the gauge fixing conditions. Obviously the Poisson structure thus
constructed on the algebra of functions on field configurations is not unique and depends on the above choice of coordinates; the same
non-uniqueness may be parametrized instead by a choice of a [[connection on a bundle|connection]] on the space of field configurations. The embedded covariant phase space becomes a leaf of the symplectic [[foliation]] of the space of field configurations.

### Via the BV-complex
 {#ReducedCovariantPhaseSpaceViaBV}

The [[BV-BRST complex]] of a [[local action functional]] is (the [[Isbell duality|formal dual]] to) a [[resolution]] of the _reduced_ covariant phase space (the quotient of the covariant phase space by symmetries). As discussed in more detail at _[[BV-BRST complex]]_ the ghost sector of that complex is a model for the quotient by the symmetries, whereas the antifield/antighost sector is a model for the [[critical locus]] of the action functional.

Moreover, by the nature of its construction, the BV-complex is canonically equipped with a _graded_ symplectic form $\Omega$, whose [[Gerstenhaber algebra|(-1)-graded Poisson bracket]] is called the _antibracket_ (essentially the canonical [[Schouten bracket]] on graded derivations). This is not the canonical symplectic form  $\int_\Sigma \omega$ on the reduced phase space, as discussed above, but it is  something like a potential for it.

We want to make the following

+-- {: .un_claim}
###### Claim

Given a [[local action functional]] on a space of fields over a spacetime $X$. Let $d_{BV}$ denote the [[differential]] of the [[BV-BRST complex]] and let $d_{dR}$ denote the horizontal de Rham differential on $X$. Then

$$
  d_{BV} \int_\Sigma \Omega = \int_X d_{dR} \omega
  \,.
$$

If $X$ is a [[globally hyperbolic spacetime]] of the form $\Sigma \times [0,1]$ then this is

$$
  d_{BV} \int_\Sigma \Omega 
    = 
  \int_{\Sigma_{out}} \omega
   -
  \int_{\Sigma_{in}} \omega
  \,.
$$

=--

We discuss this now in more detail. 

> Warning. The following is a bit preliminary.

Write 

* $X$ for the [[spacetime]] on which the fields are defined;

* $Conf = Maps(X,V) = \Gamma_X(X \times V)$ for the [[configuration space]] of fields on $X$, where $V$ is 
some [[vector space]] (for simplicity);

* $Conf_{BV} $ for the BV-extension; $V_{BV}$ for the corresponding [[graded vector space]];

* $\{v_a\}$ for a chosen [[basis]] of $V_{BV}$;

* $\Phi^a(x) \in \Omega_{loc,BV}^{0,0}(X \times Conf_{BV})$ for the functional whose value on $\phi^a v_a \in Conf$ is $\phi^a(x)$ (for $x \in X$);

* $\Omega_{loc,BV}^{\bullet,\bullet}(X \times Conf_{BV})$ for the corresponding [[variational bicomplex]].

* $\bar \Phi_a(x) \in \Omega^{dim X,0}_{loc}(X \times Conf_{BV})$ for the antifield corresponding to $\Phi^a(x)$ (which is an _antighost_ if $\Phi^a(x)$ is a ghost).

Then the symplectic form density $\Omega$ for the antibracket 

$$
  \Omega \in \Omega^{(n,2)}_{loc, BV}(X \times Conf_{BV})
$$

is

$$
  \Omega = \int_X d_{var} \bar \Phi_a(x) \wedge d_{var} \Phi^a(x)
  \,.
$$

Then, 

$$
  \begin{aligned}
    d_{BV} \int_\Sigma \Omega 
    & =
    d_{BV} \left(
      \int_\Sigma
      d_{var} \bar \Phi_a(x) \wedge d_{var} \Phi^a(x)
    \right)
    \\
    & = 
    - d_{var} (d_{BV} \int_\Sigma \var \Phi_a(x)) \wedge d_{var} \Phi^a(x)
  \end{aligned}
$$

We observe that the term in parenthesis is -- in the notation at _[[schreiber:derived critical locus]]_ (so we are assuming now the assumptions made there) --

$$
  [\hat S + d_{BRST}, d_{W(BRST)}]
  =
  [\hat S, d_{W(BRST)}]
  \,.
$$

Hence 

$$
\begin{aligned}
    \cdots & =
    - d_{var} EL_a(x) \wedge d_{var} \Phi^a(x)
    \\
    & = - \int_X d_{var}  EL
  \end{aligned}
  \,,
$$

where $EL \in \Omega^{dim X, 1}_{loc, BV}(X \times \mathrm{Conf}_{BV})$ is the [[Euler-Lagrange equation|Euler-Lagrange density]] as in [Zuckerman, p. 267](#Zuckerman). By equation g) there, this is

$$
  \cdots = - \int_X d_{dR} \omega
  \,.
$$




## Examples

### Relativistic particle

The covarint phase space of the [[relativistic particle]] on a [[pseudo-Riemannian manifold]] $X$ is the space of [[geodesic]]s of $X$ (in the absence of a [[background gauge field]]).

### Chern-Simons theory

For [[Chern-Simons theory]] corresponding to a non-degenerate bilienear [[invariant polynomial]]
$\langle -,-\rangle$ on a [[Lie algebra]] $\mathfrak{g}$ the 

* configuration space is the space $\Omega^1(\Sigma, \mathfrak{g})$ of [[Lie algebra valued forms]];

* covariant phase space is the space of field configurations $A$ whose [[curvature]] 2-form vanishes

  $$
    F_A = 0
  $$

* the [[presymplectic structure]] is

  $$
    \Omega(\delta A_1, \delta A_2) = 
   \int_{\Sigma_0} \langle \delta A_1 \wedge \delta A_2\rangle
    \,.
  $$

See [[Chern-Simons theory]] and [[schreiber:∞-Chern-Simons theory]] for more details.



### In dg-geometry

(...)

Let the ambient context be that of [[dg-geometry]]. Let $C$ be an ordinary [[smooth manifold]], assumed finite dimensional for the moment, and $\exp(i S) : C \to \mathbb{R}/\mathbb{Z}$ an ordinary [[smooth function]] such that its 0-locus is an sub-manifold.

Then a presentation for the homotopy fiber of $\exp(i S)$ is given by the formal dual of the [[dg-algebra]]

$$
 (\wedge^{-\bullet}_{C^\infty(X)}\Gamma(T X), \iota_{(-)} d \exp(i S))
  =
 \left[
  \cdots \to \wedge_{C^\infty(X)}^2\Gamma(T X) \stackrel{{\iota_{(-)}d \exp(i S)}}{\to} \Gamma(T X) \stackrel{\iota_{(-)}d \exp(i S)}{\to} C^\infty(X) 
  \right]
$$

concentrated in non-positive degree, which in degree $k$ has the $k$th exterior powers of the [[tangent vector]]s of $X$ and whose differential is given by contracting a tangent vector with the 1-form $d \exp(i S)$.  

This is a [[Koszul resolution]]-type resolution of the 0-locus of $\exp(i S)$. More generally, the homotopy fiber is given by a [[Koszul-Tate resolution]]-type complex. This is known as the _antifield complex_ in the [[BV-BRST formalism|BV-BRST formulation]] of derived phase spaces.

(...)


## References


### Covariant phase space

A standard textbook reference is chapter 17.1 of 

* [[Marc Henneaux]], [[Claudio Teitelboim]], _[[Quantization of Gauge Systems]]_ , Princeton University Press 1992. xxviii+520 pp.

Reviews of covariant phase space theory include:

* L. Vitagliano, _Secondary calculus and the covariant phase space_, [pdf](http://diffiety.ac.ru/preprint/2008/02-08.pdf)
 {#Vitagliano}

* M. J. Gotay, J. Isenberg, R. Montgomery, J. E. Marsden, _Momentum Maps and Classical Fields, Part I: Covariant Field Theory_ [pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.6.6137&rep=rep1&type=pdf)

A discussion in the context of the [[variational bicomplex]] with further pointers to the use in [[physics]] is in 

* E. Reyes, _On Covariant Phase Space and the Variational Bicomplex_ , Int. J. Theor. Phys. 43, no 5 (2004) 1267&#8364;1286

A discussion in the language of [[D-module]]s, following the book [[Chiral Algebras]] and leading up to the derived covariant phase space by [[BRST-BV formalism]] is in section 8.3 of

* [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics-impa-v01-2011.pdf))
{#Paugam}

The relation between covariant phase space methods and [[multisymplectic geometry]] is discussed in

* [[Frédéric Hélein]], _Multisymplectic formalism and the covariant phase_ ([arXiv:1106.2086](http://arxiv.org/abs/1106.2086))
  {#Helein}


### Original articles on covariant phase space technology

In the following we give a commented list of references following the hostorical development.

It seems that there have been two independent lines of development,
somewhat independent of each other, but also with some
crosspollination along the way. One stream [(P)](#ViaPoissonStructure) was concerned with the
construction of a [[Poisson structure]] on functions of solutions, while the other [(S)](#ViaSymplecticStructure) was concerned with the construction of a  [[symplectic form]]
on the space of solutions. Obviously, the differences between the two
kinds of constructions show up precisely in [[gauge theory]] systems.

The earliest papers are those of Peierls and
Bergmann-Schiller in the early 50's. They seem to have been
self-motivated. Below, we try to list papers that have established key results or have served as important popularizers together with their
main influences from previous works. The constructions of the (S)
stream seem to have appeared nearly independently several times over
several decades, until Lee-Wald and followups of Ashtekar's papers
became standard references. The (P) stream flowed slowly, but
consistently from original idea of Peierls. The papers of
Fredenhagen-D&#252;tsch-et-al are a most readable modern formulation.

* R. Peierls, _The commutation laws of relativistic field theory_ (1952) ([jstor](http://www.jstor.org/pss/99080))

  (P)

  Influence: Appears to be self-motivated. The result may have been
guessed from the known unequal-time, covariant Poisson brackets
between free fields, which involve the causal Green function in an
explicit way.

  Result: The Peierls bracket on the covariant phase pace of a non-gauge system is defined and equivalence with the Hamiltonian phase space symplectic structure is proved. Gauge systems are treated by example of electrodynamics. The solution to degenerate equations of motion is either adding gauge fixing terms to the action or consider non-degenerate equations of motion satisfied by gauge invariant fields. Fermions are handled by multiplying fermi fields by formal odd parameters.


* Bergmann-Schiller, _Classical and quantum field theories in the Lagrangian Formalism_ Phys. Rev. 89 4-16 (1953)  ([prola](http://prola.aps.org/abstract/PR/v89/i1/p4_1))

  (S)

  Influence: Appears to be motivated by Bergmann's long term and "brute force" analysis of the gauge invariance structure of relativity and structurally similar theories. Another motivation is the possibility of writing divergence-less stress energy tensors as "curls" of "superpotentials".

  Result: The pre-symplectic potential form-current makes an appearance. The definitions of the covariant phase space and the resulting symplectic form on it are obscure (at least to me), but later papers make reference to them.

* Bergmann-Goldberg-Janis-Newman, _Canonical Transformations and Commutators in the Lagrangian Formalism_ Phys. Rev. 103, 807&#8211;813 (1956) ([prola](http://prola.aps.org/abstract/PR/v103/i3/p807_1))

  (P&S) 

  Influence: Peierls, Bergmann-Schiller

  Result: Proof of the equivalence between the Peierls bracket and the bracket obtained by Bergmann-Schiller for non-gauge systems. The
treatment of gauge systems and many of the calculations are maybe a  bit obscure.

* Komar, _Commutators on Characteristic Surfaces_ 
  Phys. Rev. 134, B1430&#8211;B1440 (1964) 
  (proceedings w/ Bergmann 1962)

  (S) 

  Influence: Bergmann-Schiller

  Result: Uses the methods of Bergmann-Schiller to define Poisson
brackets on initial data for linearized gravitational waves on null
hypersurfaces, including at null infinity.

* DeWitt B.S., DeWitt C. (eds.) _Relativity, Groups, and Topology_ 
  (Les Houches 1963, Gordon and Breach, 1964), pp.585-820
  (1964; lecture notes 1963)

  (P) 

  Influence: Peierls

  Result: A more detailed exposition of Peierls' idea, with a bit more generality in the treatment of gauge systems. Becomes a standard reference along with Peierls' original paper.

* Friedman, _Generic instability of rotating relativistic stars_ 
  Commun. math. Phys. 62, 247--278 (1978) ([springer] (http://dx.doi.org/10.1007/BF01202527))

  (S) 

  Influence: Bergmann-Schiller, Komar, ... (?)

* Ashtekar-Magnon, _On the symplectic structure of general relativity_ Communications in Mathematical Physics
Volume 86, Number 1, 55-68, DOI: 10.1007/BF01205661 (1982) ([springer](http://dx.doi.org/10.1007/BF01205661))

  (S)

  Influence: Komar, also some more obscure papers by Fridmann and Palmer

  Result: Write down the explicit pre-symplectic current and the
corresponding pre-symplectic form on the space of solutions of
linearized gravitational wave equations. This symplectic form on the
reduced space of solutions is shown to coincide with the ADM
symplectic structure and with the Komar symplectic structure at null
infinity. The motivation explicit pre-symplectic current formula
appears from the desire to interpolate between the above two
formalisms.

* [[Edward Witten]] _Interacting field theory of open superstrings_ Nuclear Physics B Volume 276, Issue 2, 13 October 1986, Pages 291-324  (1986) ([web](http://dx.doi.org/10.1016/0550-3213%2886%2990298-1))

  (S)

  Influence: Appears to be self-motivated. Witten needed a covariant way to define Poisson brackets from the action of open string field theory. Acknowledges parallel, independent work of [Zuckerman](#Zuckerman).

  Result: Witten writes down the pre-symplectic form-current "by
inspection" for a scalar field and for a Chern-Simons theory, then he
explicitly shows that the current is conserved on the space of
solutions, and that its integral over a Cauchy surface is
variationally closed.


* Ashtekar, Bombelli, Koul, YS Kim, WW Zachary (eds.), The Physics of Phase Space: Nonlinear Dynamics and Chaos, Geometric Quantization, and Wigner Function
(p.356) ISBN 0-387-17894-5
(1987; preprint 1986)

  (S) 

  Influence: Ashtekar-Magnon

  Result: Explicit formula for the symplectic form of full, nonlinear
[[general relativity]] as an integral of a conserved form-current over an arbitrary Cauchy surface. Discussion of conversion of symmetries into conserved quantities using this form. Some of the aspects related to the construction of such conserved have apparently been treated in earlier works by Friedman, Sachs and possibly some others.

* [[Gregg Zuckerman|G. J. Zuckerman]], _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259-284. ([[ZuckermanVariation.pdf:file]])
  {#Zuckerman}

  (S)

  Influence: Appears to be self-motivated. Possible motivation is a more general construction of conserved currents in variational problems, a la Noether. Acknowledges that he reproduces parallel, but applied to specific theories, work of Crnkovic-Witten and Ashtekar-Bombelli-Koul.

  Result: The construction of the pre-symplectic potential form-current and pre-symplectic form-current are given in essentially modern terms. Not all proofs are given. Little discussion of symplectic reduction.


* C. Crnkovi&#263;, [[Edward Witten]], _Covariant Description of Canonical Formalism in Geometrical Theories_, in Three Hundred Years of Gravitation, S. W. Hawking and W. Israel (Eds.), Cambridge
University Press, Cambridge, 1987, pp. 676&#8364;684. ([pdf](http://www.phys.lsu.edu/classes/spring2006/phys7777/crnkovicwitten.pdf))

  (S)

  Influence: Witten

  Result: Applies the "by inspection" methods of Witten's earlier paper to write down conserved, variationally-closed pre-symplectic currents for Yang-Mills and general relativity.

* C. Crnkovi&#263;, _Symplectic Geometry of the Covariant Phase Space_ , Class. Quant. Grav. 5 (1988) 1557&#128;1575.


* J. Lee, [[Robert Wald]], _Local symmetries and constraints_ (1989) J. Math. Phys. 31, 725 (1990); doi:10.1063/1.528801  ([jMP](http://jmp.aip.org/resource/1/jmapaq/v31/i3/p725_s1?isAuthorized=no))

  (S)

  Influence: Crnkovi&#263;-Witten, Friedman

  Result: Essentially gives the modern formulation as described above. The exposition is quite similar to Zuckerman (though no connection with that work is made), but with complete proofs.

* Ashtekar-Bombelli-Reula, _The Covariant Phase Space of Asymptotically Flat Gravitational Fields_ in Mechanics, Analysis and Geometry: 200 Years after Lagrange edited by M. Francaviglia and D.~Holm, North-Holland, Amsterdam, 1990. ([web](http://www.famaf.unc.edu.ar/~reula/Papers/200_Lagrange.pdf))

  (S)

  Influence: Ashtekar-...

  Result: Becomes standard reference. (?)


* Marolf, 

  _Poisson Brackets on the Space of Histories_ Annals of Physics Volume 236, Issue 2, December 1994, Pages 374-391  
  ([arXiv:hep-th/9308141](http://arxiv.org/abs/hep-th/9308141))

  _The generalized Peierls bracket_ ([arXiv:hep-th/9308150](http://arxiv.org/abs/hep-th/9308150))

  (1994; preprints 1993, thesis 1992)

  (P)

  Influence: Peierls, DeWitt; mentions but does not use the material
from Lee-Wald, Crnkovic-Witten, Ashtekar

  Result: Gives the construction outlined above.


* [[Stefan Hollands]], [[Donald Marolf]], _Asymptotic generators of fermionic charges and boundary conditions preserving supersymmetry_ ([arXiv](http://arxiv.org/abs/gr-qc/0611044)) (2007, preprint 2006)

  (S)
  
  Influence: Lee-Wald

  Result: Extends analysis to classical fermi fields.


* D&#252;tsch [[Klaus Fredenhagen]], _The Master Ward Identity and Generalized Schwinger-Dyson Equation in Classical Field Theory_ ([arXiv:hep-th/0211242](http://arxiv.org/abs/hep-th/0211242)) (2003), 

  Brennecke-Duetsch, _Removal of violations of the Master Ward Identity in perturbative QFT_ (2008) ([arXiv:0705.3160](http://arxiv.org/abs/0705.3160)), 

  Rejzner, _Fermionic fields in the functional approach to classical field theory_  (2011) ([arXiv:1101.5126](http://arxiv.org/abs/1101.5126))

  (P)

  Influence: Peierls, DeWitt, Marolf; also some ideas related to retarded products that go back to Glaser-Lehmann-Zimmermann in the
1950s

  Result: Modern, elementary treatment of the Peierls bracket, including for classical fermi fields. The discussion is simplified by sticking to non-degenerate (or gauge fixed) actions. The choice of coordinates on the space of field configurations is simplified by considering only vector bundle valued fields.




### Reduced phase space

Standard textbooks on [[classical mechanics]] include

* [[Vladimir Arnold]], _Mathematical methods of classical mechanics_

* H. Goldstein, _Classical mechanics_

* L. D. Landau, E. M. Lifshitz, _Mechanics_, (vol. I of [[Landau-Lifschitz]] Course on theoretical physics)

* R. Abraham, J. E. Marsden, _Foundations of mechanics_

* J. E. Marsden, T. Ratiu, _Introduction to mechanics and symmetry_

* wikipedia: [phase space](http://en.wikipedia.org/wiki/Phase_space)

[[!redirects covariant phase space]]

[[!redirects phase spaces]]
[[!redirects covariant phase spaces]]

[[!redirects reduced phase space]]