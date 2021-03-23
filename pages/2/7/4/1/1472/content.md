

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


This entry lists aspects of [[fundamental physics]] from the [[nPOV]]: its description in terms of [[category theory]] and [[higher category theory]]. For a more coherent exposition, starting with introduction of the very basics, see also at _[[geometry of physics]]_.

#Contents#
* table of contents goes here
{:toc}

## The basic structures {#BasicStructures}

We discuss the setting in which fundamental physics takes place. 

### Dynamics in space {#Fundamentals}

Physics is _dynamics_ in _spaces_ . 

[[higher topos theory|Higher topos theory]] provides the formalizations of this most fundamental aspect of physics.

* A general context for **[[space]]s** is a [[big topos|big]] [[(∞,1)-topos]] $\mathbf{H}$. 

* A general context for **[[higher geometry|geometrical]] spaces** is a [[local (∞,1)-topos]].

* A general context for geometrical spaces and **processes** in these spaces is a [[cohesive (∞,1)-topos]].

An example of relevance for much of physics is the cohesive $(\infty,1)$-topos 
$\mathbf{H} = $ [[∞LieGrpd]] of [[∞-Lie groupoid]]s. This contains

* [[smooth manifold]]s;

* [[orbifold]]s;

* [[diffeological space]]s;

* smooth [[path space]]s;

In its [[Cahiers topos]]-version it contains also

* [[infinitesimal space]]s; 

* such as [[∞-Lie algebroid]]s.

* [[de Rham space]]s, smooth [[D-module]]s; 

In its full [[derived geometry]]-version it contains also

* [[derived ∞-Lie algebroid]]s such as the [[BV-BRST complex]]es of [[gauge theories]].


Every $(\infty,1)$-topos comes with its intrinsic notion of [[cohomology]]. This encodes **kinematics** in physics. Such as [[orientation]]; [[spin structure]]s; [[string structure]]s, [[fivebrane structure]]s.

Every cohesive $(\infty,1)$-topos is in particular a [[locally ∞-connected (∞,1)-topos]]. For these their intrinsic cohomology refines to [[schreiber:differential cohomology in an (∞,1)-topos]] classifying [[connections on ∞-bundles]]. This encodes **dynamics** in physics: a connection on a principal $\infty$-bundle is a **[[gauge field]]** which exerts **[[force]]**s. Such as:

* the [[electromagnetic field]], [[Yang-Mills field]], the field of [[gravity]], of [[supergravity]], the [[Kalb-Ramond field]], the [[supergravity C-field]], the [[RR-field]].

In every such connected $(\infty,1)$-topos every [[characteristic class]] gives rise to its [[∞-Chern-Weil homomorphism]] that sends gauge fields encoded as [[connections on ∞-bundles|∞-connections]] on [[principal ∞-bundles]] to [[circle n-bundles with connection]]. Such as: 

* the [[Chern-Simons circle 3-bundle]] known from the [[Green-Schwarz mechanism]] or the [[Chern-Simons circle 7-bundle]] known from [[dual heterotic string theory]]. 

Under the [[higher parallel transport]] of these circle $n$-bundles with connection, this assignment is the [[action functional]] for the [[schreiber:∞-Chern-Simons theory]] of the corresponding characteristic class. This includes as special cases various [[sigma-model]] [[quantum field theories]] such as: 

* [[Dijkgraaf-Witten theory]], ordinary [[Chern-Simons theory]], all versions of [[AKSZ theory]], (Chern-Simons-)[[supergravity]], [[BF-theory]] coupled to [[topological Yang-Mills theory]] with cosmological constant.

These are all [[topological quantum field theories]]. But by the [[holographic principle of higher category theory]] we have that on their boundaries live non-topological theories:

* on the boundary of [[Chern-Simons theory]] sits the [[Wess-Zumino-Witten model]].

* on the boundary of the [[A-model]] sits the [[quantum mechanics]] dynamics of any classical [[symplectic manifold|symplectic]] [[phase space]] and on the boundary of the [[Poisson sigma-model]] that of a [[Poisson manifold]] phase space.


### Quantum dynamics

The [[quantum mechanics]] associated with such [[sigma-model]]s is the collection of data given by

* on each closed piece $\Sigma_{d-n}$ of worldvolume [[cobordism]] of codimension $n$ the [[n-vector space]] of [[state]]s of the system;

* on each piece with boundary $\partial \Sigma_{in} \to \Sigma \leftarrow \partial \Sigma_{out}$ a [[morphism]] between these $n$-vector spaces encoding the propagation of states;

* on each open subset $U \subset \Sigma$ the _algebra of [[observable]]s_ .

Two dual formalizations axiomatize this:

* [[AQFT]]/[[factorization algebra]]s: the assignment of algebras of observables is encoded in an [[(∞,1)-presheaf|(∞,n)-copresheaf]] of [[∞-algebra]]s on $\Sigma$ with suitable properties;

* [[FQFT]]: the assignment of spaces of states and propagators is encoded in an [[(∞,n)-functor]] on the [[(∞,n)-category of cobordisms]] (see [[cobordism hypothesis]]).

Well-understood examples of such quantum field theories include

* [[AQFT]]:

  * 2-dimensional [[conformal field theory]] by [[conformal net]]s and [[vertex operator algebra]]

  * [[topological chiral homology]]

* [[FQFT]]:

  * 2-dimensional [[conformal field theory]] (see [[FFRS-formalism]])

  * [[TCFT]]s ([[(∞,1)-category]]-formulations of 2d [[TQFT]]): the [[A-model]], the [[B-model]], their duality under [[homological mirror symmetry]]


### Quantization  

By the above there is a fairly well-developed formalization of 

1. background [[gauge field]]s and their [[sigma-model]] [[action functional]];

1. [[quantum field theories]].

The idea is that the former induce examples of the latter by a process called [[quantization]]. This is imagined to be given by a [[path integral]] over the action functional.

This step in full generality is not yet well understood formally. For a list of literature addressing this problem see [Literature on quantization](#LitOnQuantization).

But special aspects of quantization are quite well understood. See for instance

* [[deformation quantization]]

* [[geometric quantization]], [[multisymplectic geometry]]

* [[Hopf-algebraic renormalization]]



## The detailed structures

We look at some aspects of the [above](#BasicStructures) general abstract story in more detail.

### Gauge theory 
  {#GaugeTheory}

#### Introduction
 {#GaugeTheoryIntroduction}

The discovery of [[gauge theory]]  is effectively the discovery of [[groupoid]]s in fundamental physics. The notion of [[gauge transformation]] is close to synonymous to the notion [[isomorphism]] and more generally to _[[equivalence in an (∞,1)-category]]_ .

From a modern point of view, the mathematical model for a [[gauge field]] in physics is a [[cocycle]] in (nonabelian) [[differential cohomology]]: a [[principal bundle]] with [[connection on a bundle|connection]] and its higher analogs. These naturally do not form just a set, but a [[groupoid]] and generally an [[∞-groupoid]], whose morphisms are gauge transformations, and higher morphisms are gauge-of-gauge transformations. The development of [[differential cohomology]] has to a fair extent been motivated by and influenced by its application to fundamental theoretical physics in general and [[gauge theory]] in particular.  

Around 1850 Maxwell realized that the [[field strength]] of the [[electromagnetic field]] is modeled by what today we call a closed [[differential form|differential 2-form]] on [[spacetime]]. In the 1930s Dirac observed that more precisely this 2-form is the [[curvature]] 2-form of a [[circle group|U(1)]]-[[principal bundle]] with [[connection on a bundle|connection]], hence that the electromagnetic field is modeled 
by what today is called a degree 2-cocycle in _[[ordinary differential cohomology]]_ .

Meanwhile, in 1915, Einstein had identified also the [[field strength]] of the [[gravity|field of gravity]] as the $\mathfrak{so}(d,1)$-valued curvature 2-form of the canonical [[orthogonal group|O(d,1)]]-[[principal bundle]] [[connection on a bundle|with connection]] on a $d+1$-dimensional [[spacetime]] [[Lorentzian manifold]]. This is a cocycle in differential [[nonabelian cohomology]]: in [[Chern-Weil theory]].

In the 1950s [[Yang-Mills theory]] identified the [[field strength]] of all the [[gauge field]]s in the [[standard model of particle physics]] as the $\mathfrak{u}(n)$-valued [[curvature]] 2-forms of [[unitary group|U(n)]]-[[principal bundle]]s [[connection on a bundle|with connection]]. This is again a cocycle in differential [[nonabelian cohomology]].


+-- {: .standout}

**Entities of ordinary [[gauge theory]]**

[[Lie algebra]] $\mathfrak{g}$ with [[gauge group|gauge]] [[Lie group]] $G$ --   [[connection on a bundle|connection]] with values in $\mathfrak{g}$ on $G$-[[principal bundle]] over a [[smooth manifold]] $X$.

=--

It is noteworthy that already in this mathematical formulation of experimentally well-confirmed fundamental physics the seed of higher differential cohomology is hidden: Dirac had not only identified the [[electromagnetic field]] as a [[line bundle]] with connection, but he also correctly identified (rephrased in modern language) its underlying cohomological [[Chern class]] with the (physically hypothetical but formally inevitable) [[magnetic charge]] located in [[spacetime]]. But in order to make sense of this, he had to resort to removing the support of the magnetic charge density from the spacetime manifold, because Maxwell's equations imply that at the support of any magnetic charge the 2-form representing the [[field strength]] of the [[electromagnetic field]] is in fact _not_ closed and hence in particular _not_ the curvature 2-form of an ordinary connection on 
an ordinary bundle.

In ([Freed](#Freed)) this old argument was improved by refining the model for the electromagnetic field one more step: 
[[Dan Freed]] notices that the charge current 3-form is itself to be regarded as a curvature, but for a connection on a [[circle n-bundle with connection|circle 2-bundle with connection]] -- also called a [[bundle gerbe]] -- , which is a cocycle in degree 3 [[ordinary differential cohomology]]. Accordingly, the [[electromagnetic field]] is fundamentally not quite a [[line bundle]], but a [[twisted bundle]] with connection, with the twist being the [[magnetic charge]] 3-cocycle. Freed shows that this perspective is inevitable for understanding the [[quantum anomaly]] of the [[action functional]] for [[electromagnetism]] is the presence of magnetic charge. 

In summary, the experimentally verified models, to date, of fundamental physics are based on the notion of (twisted) $U(n)$-principal bundles with connection for the [[Yang-Mills field]] and $O(d,1)$-principal bundles with connection for the description of [[gravity]], hence on nonabelian differential cohomology in degree 2 (possibly with a degree-3 twist). 

In attempts to better understand the structure of these two theories and their interrelation, theoretical physicists were led to consider variations and generalizations of them that are known as [[supergravity]] and [[string theory]]. In these theories the notion of [[gauge field]] turns out to generalize: instead of just [[Lie algebra]]s, [[Lie group]]s and connections with values in these, one finds structures called [[Lie 2-algebra]]s, [[Lie 2-group]]s and the gauge fields themselves behave like generalized connections with values in these. 

+-- {: .standout}

**Entities of 2-[[nLab:gauge theory]]**

[[Lie 2-algebra]] $\mathfrak{g}$ with gauge [[Lie 2-group]] $G$ --   [[connection on a 2-bundle]] with values in $\mathfrak{g}$ on $G$-[[principal 2-bundle]]/[[gerbe]] over an [[orbifold]] $X$.

=--

Notably the [[string theory|string]] is charged under a field called the _[[Kalb-Ramond field]]_ or _$B$-field_ which is modeled by a $\mathbf{B}U(1)$-[[principal 2-bundle]] with connection, where $\mathbf{B}U(1)$ is the [[nLab:Lie 2-group]] [[delooping]] of the [[circle group]]: the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle Lie 2-group</a>. Its [[Lie 2-algebra]] 
$\mathbf{B}\mathfrak{u}(1)$ is given by the [[differential crossed module]] $[\mathfrak{u}(1) \to 0]$ which has $\mathfrak{u}(1)$ shifted up by one in homological degree.

So far all these differential cocycles were known and understood mostly as concrete constructs, without making their abstract home in [[differential cohomology]] explicit. It is the next gauge field that made [[Dan Freed|Freed]] and [[Mike Hopkins|Hopkins]] propose ([FreedHopkins](#FreedHopkins), [Freed](#Freed)) that the theory of differential cohomology is generally the formalism that models [[gauge field]]s in physics:

The superstring is charged also under what is called the [[RR-field]], a  [[gauge field]] modeled by cocycles in [[differential K-theory]]. In even degrees we may think of this as a differential cocycle whose [[curvature]] form has coefficients in the [[∞-Lie algebra]] 
$\oplus_{n=0}^\infty \mathbf{B}^{2 n} \mathfrak{u}(1)$. Here $b^{2n} \mathfrak{u}(1)$ is the abelian [[L-∞-algebra|2n-Lie algebra]] whose underlying complex is concentrated in degree $2 n$ on $\mathbb{R}$.

So fully generally, one finds [[∞-Lie algebra]]s, [[∞-Lie group]]s and gauge fields behaving like connections with values in these.

+-- {: .standout}

**Entities of general [[gauge theory]]**

[[∞-Lie algebra]] $\mathfrak{g}$ with gauge [[∞-Lie group]] $G$ --  [[connection on an ∞-bundle]] with values in $\mathfrak{g}$ on $G$-[[principal ∞-bundle]] over an [[∞-Lie groupoid]] $X$.

=--

The [[curvature characteristic form]]s / [[Chern character]]s in the abelian formulation of differential cohomology take values in abelian [[∞-Lie algebra]]s and are therefore effectively nothing but differential forms with values in a complex of vector spaces, but more generally in [[∞-Chern-Weil theory]] on nonabelian [[principal ∞-bundle]]s, the [[curvature]]s forms themselves take values in general [[∞-Lie algebra]]s, such as the [[string Lie 2-algebra]], the [[supergravity Lie 3-algebra]] and the [[fivebrane Lie 6-algebra]].

Apart from generalizing the notion of gauge [[Lie group]]s to [[Lie 2-group]]s and further, structural considerations in fundamental physics also led theoretical physicists to consider models for [[spacetime]] that are more general than than the notion of a [[smooth manifold]]. In [[string theory]] [[spacetime]] is allowed to be more generally an [[orbifold]] or a generalization thereof, such as an [[orientifold]]. The natural mathematical model for these generalized spaces are [[Lie groupoid]]s or, essentially equivalently, _[[differentiable stack]]s_ . 

It is noteworthy that the notions of generalized gauge groups and the generalized spacetime models encountered this way have a natural common context: all of these are examples of [[smooth ∞-groupoid]]s.

There is a natural mathematical concept that serves to describe contexts of such [[nLab:space|generalized space]]s: a [[nLab:gros topos|gros]] [[(∞,1)-topos]]. The notion of [[schreiber:differential cohomology in an (∞,1)-topos]] provides a unifying perspective on the mathematical structure encoding the generalized [[gauge field]]s and generalized [[spacetime]] models encountered in modern theoretical physics in such a general context.

#### Classes of examples {#ClassesOfExamples}

We discuss classes of examples of gauge theories that have been considered. 
For all of these the configuration space is a space of 
[[connections on ∞-bundles]] $\{\nabla\}$ over [[spacetime]] $X$ of sorts, which one might take to be the 
defining property of a gauge theory. But there are different types of
[[action functional]]s on these configuration spaces.

##### Generalized Yang-Mills theory


In [[Yang-Mills theory]] the [[action functional]] is of the form

$$
  \nabla \mapsto \int_X \langle F_\nabla \wedge \star F_\nabla \rangle
  \,,
$$

where 

* $F_\nabla$ is the [[curvature]] [[differential form]], 

* "$\star$" the [[Hodge star]] operator with respect to a fixed
([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian metric]]-structure
on $X$ 

* and $\langle -\rangle$ some [[invariant polynomial]].

This is the original notion of _gauge theory_ 
and might be taken to be the strict sense of the term.

* For [[gauge group]] $G = U(1)$ the [[circle group]] this is [[electromagnetism]];

* For gauge group a general nonabelian [[Lie group]] $G$ this is [[Yang-Mills theory]] proper. 

* Specifically for $G$ a discrete quotient of $SU(3) \times SU(2) \times U(1)$ this is the gauge-field part of the [[standard model of particle physics]].

* For structure group $G = \mathbf{B}U(1)$ the <a href="http://nlab.mathforge.org/nlab/show/Lie%20infinity-groupoid#BnU1">circle 2-group</a> this yields the [[Kalb-Ramond field]]

* For structure group $G = \mathbf{B}^2U(1)$ the <a href="http://nlab.mathforge.org/nlab/show/Lie%20infinity-groupoid#BnU1">circle 3-group</a> this yields the [[supergravity C-field]].

* For structure group the [[K-theory spectrum]] we get [[differential K-theory]] describing the [[RR-field]].


A [[nonabelian cohomology]] version of higher Yang-Mills theory -- replacing a [[connection on a bundle]] by a [[connection on a 2-bundle]] is expected to control certain 6-dimensional theories that compactify to ordinary Yang-Mills on the torus and thereby explain _[[S-duality]]_ . See there for more details on this.

##### $\infty$-Chern-Simons theory

In [[schreiber:∞-Chern-Simons theory]] the [[action functional]] is of the form
  
$$
  \nabla \mapsto \int_X CS(\nabla)
  \,,
$$

* where $CS(-)$ is a [[Chern-Simons element]] for an [[invariant polynomial]]
$\langle - \rangle$ on an [[∞-Lie algebroid]] $\mathfrak{a}$.

This includes ordinary [[Chern-Simons theory]] in the case that 
$\mathfrak{a}$ is a [[semisimple Lie algebra]], but for general 
$\mathfrak{a}$ it subsumes a wide variety of types of
[[TQFT]]s that are often counted as of different type than Chern-Simons
theory, such as [[BF-theory]] and [[AKSZ theory]].

The action functional of [[∞-Chern-Simons theory]] stands out by the fact
that it arises by [[category theory|general abstract]] construction:
   
* the underlying Lagrangian $CS(\nabla)$ 
is nothing but the [[∞-Chern-Weil homomorphism]] 

  $$ 
    CS(-) : \mathbf{B}G_{diff} \to \mathbf{B}^n U(1)_{diff}
  $$ 

  induced by the given [[invariant polynomial]] $\langle - \rangle$. This sends gauge fields in the form of $G$-valued [[connections on ∞-bundles]] to the [[circle n-bundle with connection]] whose [[higher parallel transport]] is given by the Lagrangian;

* the integral over $CS(\nabla)$ is induced by postcomposition with the [[truncated|trunction]] morphism 

  $$
    \mathbf{H}(\Sigma, \mathbf{B}G_{conn}) 
      \stackrel{CS(-)}{\to} 
     \mathbf{H}(\Sigma,\mathbf{B}^n U(1)_{diff}) 
     \simeq 
     \infty Grpd(\Pi(\Sigma), B^n U(1)) 
    \stackrel{\int_\Sigma}{\to} 
      \tau_{n-dim \Sigma}
      \infty Grpd(\Pi(\Sigma), B^n U(1)) \simeq B^{n-dim \Sigma} U(1) 
    \,.
  $$


* For $\mathfrak{a}$ a [[semisimple Lie algebra]] equipped with its [[Killing form]] [[invariant polynomial]] we have that $CS(-)$ is the ordinary [[Chern-Simons element]] and $\int_X CS(\nabla)$ the ordinary [[Chern-Simons theory]] action functional. This may be understood as  the [[higher parallel transport]] of a [[Chern-Simons circle 3-bundle]] with connection.

* For $\mathfrak{a}$ a [[semisimple Lie algebra]] equipped with its degree 8 [[invariant polynomial]] this yields 7-dimensional, whose action functional may be understood as  the [[higher parallel transport]] of a [[Chern-Simons circle 7-bundle]] with connection.

* For $\mathfrak{a}$ a [[symplectic Lie n-algebroid]] equipped with its canonical [[invariant polynomial]] $\omega$ of degree $n+2$ $\int_X CS_\omega(-)$ is the actional functional of [[AKSZ theory]]:

  * for $n = 1$ this is the [[Poisson sigma-model]];

  * for $n = 2$ this is the [[Courant sigma-model]].

* For $\mathfrak{a}$ a [[Lie 2-algebra]] equipped with the [[Killing form]] invariant polynomial, $\int_X CS(-)$ is the action functional of [[BF-theory]] coupled to [[topological Yang-Mills theory]] with a [[cosmological constant]]. 

##### Gravity

The configuration spaces of [[gravity]] and [[supergravity]] may be identified with spaces of [[connections on ∞-bundles]] with gauge group a variant of the [[Poincare group]]. This parameterization of the configuration space of gravity is known as the [[first order formulation of gravity]], to be contrasted with a formulation explicitly over a space of [[pseudo-Riemannian manifold]]s. 

* The [[special orthogonal group]] $S O$-component of the connection in this case is called the [[spin connection]];

* the translation group-component of $\nabla$ is called the [[vielbein]].

For the ordinary Poincare group this yields the [[Palatini action]] expression for the standard [[Einstein-Hilbert action]] of [[general relativity]].

In contrast to the $\infty$-Chern-Simons theory discussed above, the general abstract nature, if any, of the action functional for gravity remains somewhat inconclusive and subject of a plethora of speculations. If one passes from connections to their associated [[Dirac operator]]s and interprets these as parts of a [[spectral triple]] there is the [[spectral action]] functional on the space of spectral triples. This we discuss in more detail [below](SpecStandModAndGravity).

There are various higher [[group extension]]s of the Poincare group and the orthonormal group that lead accordingly to higher order variations of gravity.


* lifting $S O$-connections through the <a href="http://nlab.mathforge.org/nlab/show/Lie%20infinity-groupoid#SmoothWhitehead">smooth Whitehead tower</a>

  $$
    \cdots \to Fivebrane \to String \to Spin \to S O \to O
  $$

  yields, in order of appearance,

  * [[spin structure]]s and [[spin group]]-[[principal bundle]]s with [[connection on a bundle|connection]]. 

    This lift is necessary to cancel the [[quantum anomaly]] of 
    spinning particles coupled to gravity;

  * [[string structure]]s and [[string 2-group]]-[[principal 2-bundle]]s
    with [[connection on a 2-bundle|2-connection]]

    This lift is necessary to cancel the quantum anomaly of heterotic super[[string theory|string]]s;

  * [[fivebrane structure]]s and [[fivebrane 6-group]]-[[principal ∞-bundle|principal 6-bundle]] with [[connection on an ∞-bundle|6-connection]]

  This lift is necessary to cancel the quantum anomaly of [[brane|super 5-brane]]s.

* lifting to [[super Lie group]] extensions of $SO$ yields 
  action functionals for [[supergravity]]

  The [[D'Auria-Fre formulation of supergravity]] explicitly describes higher dimensional supergravity theories as gauge theories with higher super Lie structure groups

  * 11-dimensional supergravity is a gauge theory for the [[supergravity Lie 6-algebra]].


### Phenomenological models: the standard model and gravity

Theoretical physics consists of two parts: theory and models, laws and initial conditions, axioms and phenomenology.

For instance the theory called [[general relativity]] describes the classical dynamics of [[gravity]], but does not predict the value of the [[cosmological constant]]. Rather, for each choice of the latter does the theory predict a certain dynamics the large-scale universe.

The theory that describes the fundamental forces and particles except gravity is [[Yang-Mills theory]]. This, too, does not predict the fundamental particle species seen in experiments, but for a correct choice and identification of these, the theory does predict the dynamics of these particles, as observed in accelerators.

The total collection of these choices of fundamental particles that are observed in experiments is called the [[standard model of particle physics]]. It consists basically of 

1. a choice of [[gauge group]] $G$, such that all observed [[gauge field]]s are components of a [[connection on a bundle|connection]] on a $G$-[[principal bundle]];

1. a choice of linear [[representation]] $\rho$ of $G$, such that all observed [[fermion]] fields are components of [[section]]s of a $\rho$-[[associated bundle]].

What precisely the "standard" model of particle physics is changes slightly over time, as new experimental insights are gained. Its particles were added item-by-item as they were discovered. More recently the mass of the particles called [[neutrino]]s, which was originally thought to be precisely 0, was measured to be very small, but non-vanishing.

The standard model as far as understood today exhibits a curious mixture of pattern and irregularity. This seems to suggest that it ought to have a more fundamental description in terms of a conceptually simpler structure out of which these patterns with their irregularities emerge. Since also the force of [[gravity]] is not presently included in the [[quantization]] of the standard model, it may seem plausible that this underlying structure is related to [[quantum gravity]].

We discuss in the following some of the proposals that have been suggested for how to formalize this situation.

#### Spectral standard model and gravity {#SpecStandModAndGravity}

A fundamental [[relativistic particle]] is technically a 1-dimensional [[sigma-model]] [[QFT]] on 1-[[dimension]]al [[cobordism]]s with target the [[spacetime]] $X$ that it propagates in. Since both [[gravity]] as well as [[Yang-Mills field]]s are encoded in [[connection on a bundle|connections]] it is plausible to assume that the only background field on $X$ that the particle couples to is a connection $\nabla_\rho$ on a $\rho$-[[associated bundle]] over a $G$-[[principal bundle]].

Here 

* roughly every [[semisimple Lie algebra]] [[direct sum|summand]] in $\mathfrak{g} = Lie(G)$ is one [[gauge field]] -- a bosonic field;

* every [[irreducible representation]] that $\rho$ decomposes into is one matter particle species -- a [[spinors in Yang-Mills theory|fermion field]].

This way a single $\sigma$-model may encode a rich multiple particle content and we shall speak of a single [[superparticle]] with different _excitations_ or _modes_ .

An early proposal for a single unified connection $\nabla$ that would subsume both gravity as well as Yang-Mills forces in a phenomenologically realistic way is the [[Kaluza-Klein mechanism]]. This assumes a single [[Levi-Civita connection]] but on a [[pseudo-Riemannian manifold]] $X$ which is locally of the [[product]] form $X_4 \times F_{d}$ with $X_4$ a 4-[[dimension]]al pseudo-Riemannian manifold and $F_d$ a $d$-dimensional [[Riemannian manifold]] of very small Riemannian volume. As described in more detail at [[Kaluza-Klein mechanism]], this makes the [[isometry]] groups of $F_d$ appear as extra [[gauge group]] factors as seen on $X_4$. As also described in more detail there, while this Ansatz does reproduce the correct general form of gravity coupled to Yang-Mills forces, in its original form it does also have some phenomenologically unviable aspects.

It was observed by [[Alain Connes]] and collaborators that the Kaluza-Klein mechanism works better when used not [[internalization|internal]] to the [[category]] [[Diff]] of [[smooth manifolds]] but in context for more general [[higher geometry|geometry]]: [[noncommutative geometry]]. This is the content of the _[[Connes-Lott-Chamseddine model]]_.

This more general geometry turns out to model exactly the most general $\sigma$-model backgrounds for a 1-dimensional [[FQFT]]: because such is algebraically specified by

1. the ([[Hilbert space|Hilbert]]) space $\mathcal{H}$ of [[state]]s that it assigns to the point;

1. An [[associative algebra]] $A \hookrightarrow \mathcal{H}$ whose [[monoid|multiplication operation]] $A\otimes A \to A$ is the [[operator product expansion|operator product]] assigned to the trivalent interaction vertex

   $$
     \array{
       \bullet
       \\
       & \searrow
       \\
       && \bullet & \to
       \\
       & \nearrow
       \\
       \bullet
     }
   $$

1. A [[Dirac operator]] $D$ whose [[Dyson formula]] exponential $\exp(t D^2 + \theta D)$ is assigned to a piece of 1-dimensional cobordism of superlength $(t, \theta)$.

This data is that of [[spectral triple]], which is well known to enocode Riemannian noncommutative geometry (rather: _spectral geometry_ ). It is therefore natural to search for a Kaluza-Klein ansatz in spectral geometry that would produce the standard model context.

A very detailed such construction was given by [[Alain Connes]] (see the [references below](#FunctorialSpectral)).

It turns out that the realistic model has $K$-theory dimension $D = 4+6$. 

By the result at [[(1,1)-dimensional Euclidean field theories and K-theory]] this $K$-theory dimension is precisely the intrinsic dimension of target space as seen by the [[superparticle]]. Moreover, $D = 4+6$ is precisely the dimension for whic the 2-dimensional super-[[CFT]] [[sigma-model]] is critical and hence allows to lift the 1-dimensional superparticle described here to [[string theory]].

This means that Connes' [[spectral triple]] whose particle spectrum reproduces the [[standard model of particle physics]] has a chance of being the point particle limit or [[decategorification]] of the kind of [[2-spectral triple]] -- a 2-dimensional [[CFT|superconformal field theory]] -- of the kind that is considered in [[string theory]]. If so the lift of Connes' model to the corresponding element in the [[moduli space]] of 2-spectral triples called the [[landscape of string theory vacua]] might provide, via the second quantization of the latter, a (perturbative) quantization of the [[spectral action]] of the former.

## Related introductions
  {#RelatedIntroductions}

* [[higher structures]]

* [[fiber bundles in physics]]

* [[motivation for sheaves, cohomology and higher stacks]]

* [[string theory FAQ]]

* [[motivation for higher differential geometry]]

* [[applications of (higher) category theory]]

* [[motivation for cohesion]]

* [[Hilbert's sixth problem]]

* [[motives in physics]]

* [[model theory and physics]]

* [[L-infinity algebras in physics]]

## References

We list various references related to higher category  theory and fundamental physics.

A discussion of an axiomatization of basic concepts of [[gauge theory|gauge]] [[quantum field theory]] in [[cohesive homotopy type theory]] is in

* [[Urs Schreiber]], [[Mike Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]_
 {#SchreiberShulman}

For general (formal) accounts of physics see also the references at [[books and reviews in mathematical physics]], such as 

* [[Frédéric Paugam]], _[Towards the mathematics of quantum field theory](http://people.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf)_


### Introductions to category theory in physics {#CatsinPhysics}

The translation between the axioms of [[functorial quantum field theory]] and [[path integral]] imagery is explained in

* [[Edward Witten]], Section 1 of: _Geometric Langlands From Six Dimensions_ ([arXiv:0905.2720](https://arxiv.org/abs/0905.2720))


In 

* [[Bob Coecke]], _Introducing categories to the practicing physicist_ ([arXiv:0808.1032](http://arxiv.org/abs/0808.1032))

* [[Bob Coecke]], _Categories for the practising physicist_ ([arXiv:0905.3010](http://arxiv.org/abs/0905.3010))

the authors try to motivate and introduce some basic concepts of [[category theory]] for an audience familiar with standard physics and in particular with [[quantum mechanics]]. The article focuses towards the end on [[monoidal categories]], their description in terms of [[string diagram]]s and [[quantum mechanics in terms of dagger-compact categories]].

More details on the use of string diagrams in [[dagger-categories]] for the description of quantum mechanics is is

* [[Bob Coecke]], _Kindergarten quantum mechanics_ ([arXiv:quant-ph/0510032](http://arxiv.org/abs/quant-ph/0510032))

* [[Bob Coecke]], _Quantum Picturalism_ ([arXiv:0908.1787](http://arxiv.org/abs/0908.1787))

A similar introduction to the relation between quantum mechanics and [[monoidal categories]], but more from the perspective of [[FQFT]] is in

* [[John Baez]], _Quantum quandaries_ ([arXiv:quant-ph/0404040](http://arxiv.org/abs/quant-ph/0404040))


### Introductions to higher category theory and physics

A historical introduction to some aspects of [[n-categories]] (for low $n$) in physics can be found here:

* [[John Baez]] and [[Aaron Lauda]], _A prehistory of $n$-categorical physics_ ([pdf](http://math.ucr.edu/home/baez/history.pdf)), to appear in _Deep Beauty: Mathematical Innovation and the Search for an Underlying Intelligibility of the Quantum World_, ed. Hans Halvorson.

A historical introduction to applications in physics of more [[homotopy theory|homotopy theoretic]] [[higher category theory]] (revolving around [[BV-BRST formalism]]) is in:

* [[Jim Stasheff]], _[[A Survey of Cohomological Physics]]_ 

The following book-to-be aims to give picture of the present state of the art of describing the category-theoretic structure of the universe, as far as fundamental physics is concerned

* [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_

Amplifying the ambition towards [[Hilbert's sixth problem]]:

* {#MartinsBiezuner20} [[Yuri Ximenes Martins]], [[Rodney Josué Biezuner]], _Towards An Approach to Hilbert's Sixth Problem: A Brief Review_, 2020 ([hal:02909681](https://hal.archives-ouvertes.fr/hal-02909681), [pdf](https://hal.archives-ouvertes.fr/hal-02909681/document))



### Monographs on cohomology and higher gauge theory

An unusually comprehensive collection of detailed discussion of bundles, higher bundles, cohomology, characteristic classes, etc. with an eye on applications in physics is

* [[Dale Husemöller]], [[Michael Joachim]], [[Branislav Jurco]], Martin Schottenloher,  _Basic bundle theory and K-cohomology invariants_ , Springer Lecture Notes in Physics 726, 2008 ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726.pdf))

### On formal quantum field theory

There are two axiomatizations of [[QFT]]: [[FQFT]] and [[AQFT]]. 

* [FQFT references](#FQFTReferences)

* [AQFT references](#AQFTReferences)

#### FQFT {#FQFTReferences}

Kontsevich's 1994 ICM article, is one of the seminal papers of the 1990s. This paper invented the categorical side of mirror symmetry (homological mirror symmetry), discovered D-[[brane]]s (before physicists realized their role --- and directly inspiring many physicists) and the fact that they naturally form [[dg-category|dg-categories]] and $A_\infty$-[[A-infinity-category|category]], and thus led to a deluge of papers involving [[category theory]] and [[higher category theory]] in close relation with mathematical physics.

In particular the [[FQFT|Moore--Segal paper]] should be seen in the light of this development. On a similar note, roughly contemporary with Moore--Segal (which is [arXiv:math/0609042](http://www.arxiv.org/abs/math/0609042) though developed earlier) are the works of [[Kevin Costello]] on [[TCFT]] ([arXiv:math/0412149](http://www.arxiv.org/abs/math/0412149)) and Kontsevich--Soibelman ([arXiv:math/0606241](http://www.arxiv.org/abs/math/0606241) --- some of the results were lectured on in various places by Kontsevich in 2003 and in particular helped inspire Costello) proving a much stronger result, which is the [[TCFT]] (or equivalently differential graded or $A_\infty$-) version of the classification of open-closed 2d [[TQFT]]s. These papers were directly motivated by [[homological mirror symmetry]] and topological [[string theory]], and have greatly influenced work in areas such as [[string topology]] which you mention and the [[cobordism hypothesis]] ([[On the Classification of Topological Field Theories|Hopkins-Lurie]] started from Costello's paper and abstracted the argument, before the general argument in n-dimensions came around). 

> (in parts taken from [here](http://golem.ph.utexas.edu/category/2009/07/a_prehistory_of_ncategorical_p_1.html#c025075))

For the moment see the references at [[FQFT]] for more.  

##### On functorial spectral geometry {#FunctorialSpectral}

Literature on the relation between [[spectral triple]]s and 1-dimensional super-QFT is to appear shortly. Spectral background for the standard model have been considered here:

The first proposal for such compactifications, which already came very close to the standard model, is decades old by now.


* [[Alain Connes]],  [[John Lott]], _Particle Models And Noncommutative Geometry_ Nucl.Phys.Proc.Suppl.18B:29-47,1991 ([spires](http://www.slac.stanford.edu/spires/find/hep/www?rawcmd=find+author+Connes+and+author+Lott&FORMAT=WWW&SEQUENCE=))

This is reviewed in  

* Daniel Kastler, Thomas Schucker, _The Standard Model a la Connes-Lott_ [arXiv:hep-th/9412185](http://arxiv.org/abs/hep-th/9412185) .

As far as I can tell, at that time the Yang-Mills terms were stilll included by hand. The main point of the spectral approach was to realize that it could nicely explain the Higgs boson and its Yukawa coupling terms to the fermions. It did (and does) so by realizing the Higgs boson as an internal part of an ordinary minimally coupled connection 1-form - an internal gauge boson.

A few years later Connes apparently realized that also the gravitational and gauge kinetic Yang-Mills terms had an inherent operator-theoretic formulation, namely the [[spectral action]] principle.

This is indicated in


* [[Alain Connes]], _Gravity coupled with matter and foundation of non-commutative geometry_ [arXiv:hep-th/9603053](http://arxiv.org/abs/hep-th/9603053)

and fully formulated in 


* [[Ali Chamseddine]], [[Alain Connes]], _The Spectral Action Principle_ [arXiv:hep-th/9606001](http://arxiv.org/abs/hep-th/9606001),

both of which start by presenting the general spectral idea and then working out how to realize the standard model in detail.

A useful discussion of the details of the realization of the standard model in this approach is

* C. P. Martin, Jose M. Gracia-Bondia, Joseph C. Varilly, _The Standard Model as a noncommutative geometry: the low energy regime_ ([arXiv:hep-th/9605001](http://arxiv.org/abs/hep-th/9605001)) .

This is in particular designed to take the ordinary physicst by the hand and introduce him or her gently to the operator-theoretic spectral description by motivating these by the structure of the standard model.

So already over ten years ago people had a pretty good idea that and how the standard model action has an elegant descritption as a spectral action. 

The only problem was: this description was wrong. But only in the sense in which  ideas in physics tend to be wrong - not entirely wrong but not quite right.

Namely, instead of containing the fermionic particle content of the standard model, these spectral models produced four copies of every fermion in the standard model. A slight overkill. 

By a remarkable synchronicity, it seems that there was no progress on this aspect for about ten years, and now two preprints appear almost simultaneously, presenting the solution:


* [[John Barrett]], _A Lorentzian version of the non-commutative geometry of the standard model of particle physics_ [arXiv:hep-th/0608221](http://arxiv.org/abs/hep-th/0608221).


* [[Alain Connes]], _Noncommutative Geometry and the standard model with neutrino mixing_ [arXiv:hep-th/0608226](http://arxiv.org/abs/hep-th/0608226)

And the modification needed to get this solution is rather tiny, just a small change in the real structure $J$ of the spectral triple from ten years ago.

A survey is also at

* [[Urs Schreiber]], _Connes on spectral geometry of the standard model IV_ ([blog entry](http://golem.ph.utexas.edu/category/2006/09/connes_on_spectral_geometry_of_3.html))

#### AQFT {#AQFTReferences}

For the moment see the references at [[AQFT]] for more.


### On the quantization procedure {#LitOnQuantization}

First sketches of the idea that [[path integral]] [[quantization]] may have a formalization in terms of [[higher category theory]] appeared in

* [[Dan Freed]], _[[Higher Algebraic Structures and Quantization]]_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115))

and its companion

* [[Dan Freed]], _Quantum groups and path integrals_ ([arXiv:q-alg/9501025](http://arxiv.org/abs/q-alg/9501025))

More formal aspects along these lines appear in

* [[Simon Willerton]] _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv:math/0503266](http://arxiv.org/abs/math.QA/0503266))

An indication of a full formalization of what that may mean for discrete QFTs such as [[Dijkgraaf-Witten theory]] is in

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]] _[[Topological Quantum Field Theories from Compact Lie Groups]]_

based on work in 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

### On gauge fields and differential cohomology

The observation that generally [[differential cohomology]] is the correct formalism for describing [[gauge field]]s in physics originates around

* [[Dan Freed]], [[Mike Hopkins]], _On Ramond-Ramond fields and K-theory_
Journal of High Energy Physics 0005 (2000) 044 ([pdf](http://web.me.com/teichner/Math/Smooth_Cohomology_files/Freed-Hopkins.pdf))
{#FreedHopkins}

Motivated by this, the theory of differential cohomology itself was developed in

* [[Mike Hopkins]], I. Singer _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_
{#HopkinsSinger}

and shown to encode subtle [[quantum anomaly]]-cancellation phenomena in gauge theory. A systematic formal description of the nature of these quantum anomalies and further discussion of applications on differential cohomology in physics is in 

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_
{#Freed}

This article starts with an introduction on basic [[electromagnetism]] and points out that already there, in the presence of [[magnetic charge]], a careful analysis of [[quantum anomalies]] shows that there are higher gauge theoretic effects even in this familiar theory.

### On topos-theoretic formulations of physics 
 {#RefsOnToposTheoreticPhysics}

#### Gros toposes

The observation that any formalization of physics ought to take place in a suitable [[topos]] has been promoted early on by [[Bill Lawvere]]. Lawvere started out as a student in [[continuum mechanics]] and his search for a formalization of physics made him end up being one of the most general abstract thinkers in [[category theory]]. 

Lawvere thought about [[classical physics]] governed, as it is since Newton, by the theory of [[differential equation]]s. He proposed that [[differential geometry]] is something that takes place inside a [[smooth topos]] -- a [[topos]] with a suitable notion of [[infinitesimal object]]s -- an approach now known as [[synthetic differential geometry]]. 

In 

* [[Bill Lawvere]], _Categorical dynamics_, lecture (1967)

which is recalled in

* [[Bill Lawvere]], _Toposes of laws of motion_ , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))

he sketched an outline both of synthetic differenial geometry in general and its application to the formulation of the [[differential equation]]s in classical dynamics.

In this spirit he to search for [[category theory|category theoretic]] formalizations of fundamental ( _metaphysical_  in the good sense of the word) ontological concepts. A collection of such formalizations is indicated in

* [[Bill Lawvere]], _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

On [page 14](http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf#page=14) there appears the hint of the general abstract definition of a [[locally connected topos]] as a general abstract [[gros topos]] context for geometric spaces. This idea was then refined to the concept of a [[cohesive topos]] in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

In this spirit a generalization of formalization of physics in [[(∞,1)-topos]] is discussed in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, Lectures at _[ESI program on K-theory and quantum fields](http://maths-old.anu.edu.au/esi/2012/)_ (2012)
 {#SchreiberLectures}

* [[Urs Schreiber]], [[Mike Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]_ (2012)

#### Petit toposes

Independent of these developments is another proposal for a role of topos theory in [[quantum mechanics]] initiated by [[Chris Isham]]. The motivation here is the observation that the [[Kochen-Specker theorem]] -- which may be used to formalize the way in which [[quantum mechanics]] fails to secretly a theory of classical mechanics -- has a natural interpretation in terms of the [[internal logic]] of the [[presheaf topos]] on the category of commutative sub-algebras of a given bounded [[operator algebra]].

This observation led Isham to propose a fundamental role of these presheaf toposes in [[quantum mechanics]].

* Andread Doering, C.J. Isham, _A Topos Foundation for Theories of Physics_ I-IV ([arXiv](http://arxiv.org/abs/quant-ph/0703060))

This idea was further refined in 

* [[Chris Heunen]], [[Nicolaas Landsman]], [[Bas Spitters]], _A topos for algebraic quantum theory_ ([arXiv:0709.4364](http://arxiv.org/abs/0709.4364))

  **Abstract**

  The aim of this paper is to relate [[AQFT|algebraic quantum mechanics]] to [[topos theory]], so as to construct new foundations for [[quantum logic]] and quantum spaces. Motivated by Bohr's idea that the empirical content of quantum physics is accessible only through classical physics, we show how a [[C-star-algebra]] of [[observable]]s $A$ induces a [[topos]] $T(A)$ in which the amalgamation of all of its commutative subalgebras comprises a single commutative $C^*$-algebra. According to the [[constructive mathematics|constructive]] [[Gelfand duality]] theorem of Banaschewski and Mulvey, the latter has an internal spectrum $S(A)$ in $T(A)$, which in our approach plays the role of a quantum [[phase space]] of the system. Thus we associate a [[locale]] (which is the topos-theoretical notion of a space and which intrinsically carries the intuitionistic logical structure of a [[Heyting algebra]]) to a $C^*$-algebra (which is the noncommutative notion of a space). In this setting, [[state]]s on $A$ become [[probability measure]]s (more precisely, valuations) on $S(A)$, and self-adjoint elements of $A$ define continuous functions (more precisely, locale maps) from $S(A)$ to Scott's interval domain. Noting that open subsets of $S(A)$ correspond to propositions about the system, the pairing map that assigns a (generalized) [[truth value]] to a state and a proposition assumes an extremely simple categorical form. Formulated in this way, the quantum theory defined by $A$ is essentially turned into a classical theory, internal to the topos $T(A)$. 

A refinement of this from [[quantum mechanics]] to [[AQFT]]-[[quantum field theory]] is in 

* [[Joost Nuiten]], _[[schreiber:bachelor thesis Nuiten|Boohrification of local nets of observables]]_ .

See _[[Bohr topos]]_ for more.

### In phenomenology and experimental physics
 {#InPhenomenology}

In the context of [[phenomenology]], [[higher category theory]] is currently applied mostly for [[2-categories]] in the context of 2-dimensional [[TQFT]] (modelling phenomena in [[solid state physics]]) and [[CFT]] (modelling critical surface phenomena in [[statistical physics]]).

Specifically 2d [[extended quantum field theory]] has been applied to the solid state physics modeled by the [[Levin-Wen model]], see

* [[Alexei Kitaev]], [[Liang Kong]], _Levin-Wen models and tensor categories ([pdf])_

For more discussion of 2d [[CFT]] in terms of higher category theory see the references there and at [[FRS formalism]].

In $d = 3$ the [[quantum hall effect]] and related effects are described to some extent by [[Chern-Simons theory]], and Chern-Simons theory comes with a rich higher categorical framework. Notably there is now a fully [[extended TQFT]] description of Chern-Simons theory down to the point, hence in terms of [[(infinity,n)-functors|(infinity,3)-functors]], see [here](Topological+Quantum+Field+Theories+from+Compact+Lie+Groups#3dCSFullyExtended).

Closely related to this, several approaches at realizing [[quantum computing]] rely on [[TQFT]] methods and are treated with methods from higher category theory. For instance the notion of a [[blob n-category]] orginates in investigations of quantum computing.

Indeed, if one counts computing as "experimental" or "phenomenology" -- at least as related to the tangible world -- then category theory is ubiquituous, see at _[[computational trinitarianism]]_ for the general idea and further pointers. For instance the _[[relation between type theory and category theory]]_ (see there) which underlies the formal understanding of modern [[computer science]], is an [[equivalence of 2-categories]] in  [[2-category theory]]. More recently, computing in the guise of _[[homotopy type theory]]_ is closely related to [[(infinity,1)-category theory]]. This carries in it the prospect of serving as the very [[foundations]] of [[mathematics]] and [[computer science]]. And hence, in effect, also of theoretical physics (see [Schreiber-Shulman 2012](#SchreiberShulman) above).

[[!redirects n-categorical physics]]

[[!redirects Physics]]

[[!redirects theoretical physics]]