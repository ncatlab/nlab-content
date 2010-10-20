

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


This entry discusses fundamental [[physics]] from the [[nPOV]].

#Contents#
* automatic table of contents goes here
{:toc}

## Survey

### Dynamics in space {#Fundamentals}

Physics is _dynamics_ in _spaces_ . 

[[higher topos theory|Higher topos theory]] provides the formalizations of this most fundamental aspect of physics.

* A general context of **[[space]]s** is an [[(∞,1)-topos]] $\mathbf{H}$. 

* A general context for **[[higher geometry|geometrical]] spaces** is a [[local (∞,1)-topos]].

* A general context for geometrical spaces and **processes** in these spaces is a [[cohesive (∞,1)-topos]].

An example of relevance for much of physics is the cohesive $(\infty,1)$-topos 
$\mathbf{H} = $ [[?LieGrpd]] of [[∞-Lie groupoid]]s. This contains

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

The [[quantum mechanics]] associated with such [[sigma-model]] is the collection of data given by

* on each closed piece $\Sigma_{d-n}$ of worldvolume of codimension $n$ the [[n-vector space]] of [[state]]s of the system;

* on each piece with boundary $\partial \Sigma_{in} \to \Sigma \leftarrow \partial \Sigma_{out}$ a [[morphism]] between these $n$-vector spaces encoding the propagation of states;

* on each open subset $U \subset \Sigma$ the _algebra of observables_ .

Two dual formalizations axiomatize this:

* [[AQFT]]/[[factorization algebra]]s: the assignment of algebras of observables is encoded in an [[(∞,1)-presheaf|(∞,n)-copresheaf]] on $\Sigma$ with suitable properties;

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



## Further details

We look at some aspects of the above story in more detail.

### Gauge theory {#GaugeTheory}

The mathematical model for a [[gauge field]] in physics is a [[cocycle]] in [[differential cohomology]]. The development of [[differential cohomology]] has to a fair extent been motivated by and influenced by its application to fundamental theoretical physics in general and [[gauge theory]] in particular.  

Around 1850 Maxwell realized that the  [[field strength]] of the [[electromagnetic field]] is modeled by a closed [[differential form|differential 2-form]] on [[spacetime]]. In the 1930s Dirac observed that more precisely this 2-form is the [[curvature]] 2-form of a [[circle group|U(1)]]-[[principal bundle]] with [[connection on a bundle|connection]], hence that the electromagnetic field is modeled as what today is called a degree 2-cocycle in _[[ordinary differential cohomology]]_ .

Meanwhile, in 1915, Einstein had identified also the [[field strength]] of the [[gravity|field of gravity]] as the $\mathfrak{so}(d,1)$-valued curvature 2-form of the canonical [[orthogonal group|O(d,1)]]-[[principal bundle]] [[connection on a bundle|with connection]] on a $d+1$-dimensional [[spacetime]] [[Lorentzian manifold]]. This is a cocycle in differential [[nonabelian cohomology]]: [[Chern-Weil theory]].

In the 1950s [[Yang-Mills theory]] identified the [[field strength]] of all the [[gauge field]]s in the [[standard model of particle physics]] as the $\mathfrak{u}(n)$-valued [[curvature]] 2-forms of [[unitary group|U(n)]]-[[principal bundle]]s [[connection on a bundle|with connection]]. This is again a cocycle in differential [[nonabelian cohomology]].


+-- {: .standout}

**Entities of ordinary [[gauge theory]]**

[[Lie algebra]] $\mathfrak{g}$ with [[gauge group|gauge]] [[Lie group]] $G$ --   [[connection on a bundle|connection]] with values in $\mathfrak{g}$ on $G$-[[principal bundle]] over [[smooth manifold]] $X$.

=--

It is noteworthy that already in this mathematical formulation of experimentally well-confirmed fundamental physics the seed of higher differential cohomology is hidden: Dirac had not only identified the [[electromagnetic field]] as a [[line bundle]] with connection, but he also correctly identified (rephrased in modern language) its underlying cohomological [[Chern class]] with the (physically hypothetical but formally inevitable) [[magnetic charge]] located in [[spacetime]]. But in order to make sense of this, he had to resort to removing the support of the magnetic charge density from the spacetime manifold, because Maxwell's equations imply that at the support of any magnetic charge, the 2-form representing the [[field strength]] of the [[electromagnetic field]] is in fact _not_ closed and hence in particular _not_ the curvature 2-form of a connection.

In ([Freed](#Freed)) Dirac's old argument was finally patched by refining the model for the electomagentic field one more step: 
[[Dan Freed]] notices that the charge current 3-form is itself to be regarded as a curvature, but for a connection on a [[circle n-bundle with connection|circle 2-bundle with connection]] -- also called a [[bundle gerbe]] -- , which is a cocycle in degree 3 [[ordinary differential cohomology]]. Accordingly, the [[electromagnetic field]] is fundamentally not quite a [[line bundle]], but a [[twisted bundle]] with connection, with the twist being the [[magnetic charge]] 3-cocycle. Freed shows that this perspective is inevitable for understanding the [[quantum anomaly]] of the [[action functional]] for [[electromagnetism]] is the presence of magnetic charge. 

In summary, the experimentally verified models, to date, of fundamental physics are based on the notion of (twisted) $U(n)$-principal bundles with connection for the [[Yang-Mills field]] and $O(d,1)$-principal bundles with connection for the description of [[gravity]], hence on nonabelian differential cohomology in degree 2 (possibly with a degree-3 twist). 

In attempts to better understand the structure of these two theories and their interrelation, theoretical physicists were led to consider variations and generalizations of them that are known as [[supergravity]] and [[string theory]]. In these theories the notion of [[gauge field]] turns out to generalize: instead of just [[Lie algebra]]s, [[Lie group]]s and connections with values in these, one finds structures called [[Lie 2-algebra]]s, [[Lie 2-group]]s and the gauge fields themselves behave like generalized connections with values in these. 

+-- {: .standout}

**Entities of 2-[[nLab:gauge theory]]**

[[Lie 2-algebra]] $\mathfrak{g}$ with gauge [[Lie 2-group]] $G$ --   [[connection on a 2-bundle]] with values in $\mathfrak{g}$ on $G$-[[principal 2-bundle]]/[[gerbe]] over an [[orbifold]] $X$.

=--

Notably the [[string theory|string]] is charged under a field called the [[Kalb-Ramond field]] which is modeled by a $\mathbf{B}U(1)$-[[principal 2-bundle]] with connection, where $\mathbf{B}U(1)$ is the [[nLab:Lie 2-group]] [[delooping]] of the [[circle group]]: the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle Lie 2-group</a>. Its [[Lie 2-algebra]] $b\mathfrak{u}(1)$ is given by the [[differential crossed module]] $[\mathfrak{u}(1) \to 0]$ which has $\mathfrak{u}(1)$ shifted up by one in homological degree.

So far all these differential cocycles were known and understood mostly as concrete constructs, without making their abstract home in [[differential cohomology]] explicit. It is the next gauge field that made [[Dan Freed|Freed]] and [[Mike Hopkins|Hopkins]] propose ([FreedHopkins](#FreedHopkins), [Freed](#Freed)) that the theory of differential cohomology is generally the formalism that models [[gauge field]]s in physics:

The superstring is also charged under what is called the [[RR-field]], a  [[gauge field]] modeled by cocycles in [[differential K-theory]]. In even degrees we may think of this as a differential cocycles whose [[curvature]] form has coefficients in the [[∞-Lie algebra]] $\oplus_{n=0}^\infty b^{2 n} \mathfrak{u}(1)$. Here $b^{2n} \mathfrak{u}(1)$ is the abelian [[L-∞-algebra|2n-Lie algebra]] whose underlying complex is concentrated in degree $2 n$ on $\mathbb{R}$.

So even more generally, one finds [[∞-Lie algebra]]s, [[∞-Lie group]]s and gauge fields behaving like connections with values in these.

+-- {: .standout}

**Entities of general [[gauge theory]]**

[[∞-Lie algebra]] $\mathfrak{g}$ with gauge [[∞-Lie group]] $G$ --  [[connection on an ∞-bundle]] with values in $\mathfrak{g}$ on $G$-[[principal ∞-bundle]] over an [[∞-Lie groupoid]] $X$.

=--

The [[curvature characteristic form]]s / [[Chern character]]s in the abelian formulation of differential cohomology take values in abelian [[∞-Lie algebra]]s and are therefore effectively nothing but differential forms with values in a complex of vector spaces, but more generally in [[∞-Chern-Weil theory]] on nonabelian [[principal ∞-bundle]]s, the [[curvature]]s forms themselves take values in general [[∞-Lie algebra]]s, such as the [[string Lie 2-algebra]] the [[supergravity Lie 3-algebra]] or the [[fivebrane Lie 6-algebra]].

Apart from generalizing the notion of gauge [[Lie group]]s to [[Lie 2-group]]s and further, structural considerations in fundamental physics also led theoretical physicists to consider models for [[spacetime]] that are more general than than the notion of a [[smooth manifold]]. In [[string theory]] [[spacetime]] is allowed to be more generally an [[orbifold]] or a generalization thereof, such as an [[orientifold]]. The natural mathematical model for these generalized spaces are [[Lie groupoid]]s or essentially equivalently: [[differentiable stack]]s. 

It is noteworthy that the notions of generalized gauge groups and the generalized spacetime models encountered this way have a natural common context: all of these are examples of a notion of smooth [[∞-groupoid]] modeled as differentiable [[∞-stack]]s: these we may call [[∞-Lie groupoid]]s.

There is a natural mathematical concept that serves to describe contexts of such [[nLab:space|generalized space]]s: a [[nLab:gros topos|gros]] [[(∞,1)-topos]]. The notion of [[schreiber:differential cohomology in an (∞,1)-topos]] provides a unifying perspective on the mathematical structure encoding the generalized [[gauge field]]s and generalized [[spacetime]] models encountered in modern theoretical physics in such a general context.

To consider some of these applications in more detail: 

* [[Chern-Simons theory]] may be understood as the [[sigma-model]] whose target space is the [[delooping]] [[Lie groupoid]] $\mathbf{B}G$ of the [[Lie group]] $G$ on which the [[gauge field]] is the [[Chern-Simons circle 3-bundle]] with connection.

* Similarly there is a 7-dimensional Chern-Simons theory with target space the [[Lie 2-groupoid]] $\mathbf{B}String$ and gauge field the [[Chern-Simons circle 7-bundle]].

* The familiar theory of smooth [[spin group|Spin(n)]]-[[principal bundle]]s [[connection on a bundle|with connnection]] has a motivation from the [[physics]] of quantum point particles such as electrons: for the [[quantum mechanics]] of a spinning point particle to be free of an obstruction called an [[quantum anomaly|anomalous]] [[action functional]], the target space it propagates in has to admit a [[spin structure]]. Then the dynamics of the particle is encoded in a smooth differential refinement of the corresponding
topological $Spin(n)$-[[principal bundle]] to a smooth [[connection on a bundle|bundle with connection]].

  It has been known since work by Killingback and [[Edward Witten|Witten]] that when this is generalized to the quantum mechanics of a spinning 1-dimensional object -- a [[string theory|quantum string]]  -- , the spin-structure of the space has to lift further to a [[string structure]], where the [[string group]] $String(n)$ is the universal 3-connected cover of $Spin(n)$. Contrary to the spin-group, the string-group cannot be refined to a (finite dimensional) [[Lie group]]. Therefore the question arises:  what is a smooth differential refinement of a string-principal bundle, that encodes the dynamics of these 1-dimensional objects?

  It turns out that this has a nice answer not in ordinary
[[differential geometry]], but in _[[nLab:higher geometry|higher]]_ or _[[derived geometry|derived]]_ differential
geometry: $String(n)$ naturally has the structure of a [[Lie 2-group]]. This allows to refine a topological String-principal bundle to a generalization of a differentiable nonabelian [[gerbe]]: a smooth [[principal 2-bundle]]. 

* [[BF-theory]] coupled to [[topological Yang-Mills theory]] is the gauge theory for a [[Lie 2-algebra]] valued conneciton 


* the models of [[AKSZ theory]] are precisely the gauge theories for [[n-symplectic manifold|symplectic Lie n-algebroids]]

  (see [[schreiber:∞-Chern-Simons theory]] for more)

(...)





### History of the development of FQFT

> the following a stub obtained from copy-and-pasting material that [[David Ben-Zvi]] mentioned [here](http://golem.ph.utexas.edu/category/2009/07/a_prehistory_of_ncategorical_p_1.html#c025075)

Kontsevich's 1994 ICM article, is one of the seminal papers of the 1990s. This paper invented the categorical side of mirror symmetry (homological mirror symmetry), discovered D-[[brane]]s (before physicists realized their role --- and directly inspiring many physicists) and the fact that they naturally form [[dg-category|dg-categories]] and $A_\infty$-[[A-infinity-category|category]], and thus led to a deluge of papers involving [[category theory]] and [[higher category theory]] in close relation with mathematical physics.

In particular the [[FQFT|Moore--Segal paper]] should be seen in the light of this development. On a similar note, roughly contemporary with Moore--Segal (which is [arXiv:math/0609042](http://www.arxiv.org/abs/math/0609042) though developed earlier) are the works of [[Kevin Costello]] on [[TCFT]] ([arXiv:math/0412149](http://www.arxiv.org/abs/math/0412149)) and Kontsevich--Soibelman ([arXiv:math/0606241](http://www.arxiv.org/abs/math/0606241) --- some of the results were lectured on in various places by Kontsevich in 2003 and in particular helped inspire Costello) proving a much stronger result, which is the [[TCFT]] (or equivalently differential graded or $A_\infty$-) version of the classification of open-closed 2d [[TQFT]]s. These papers were directly motivated by [[homological mirror symmetry]] and topological [[string theory]], and have greatly influenced work in areas such as [[string topology]] which you mention and the [[cobordism hypothesis]] ([[On the Classification of Topological Field Theories|Hopkins-Lurie]] started from Costello's paper and abstracted the argument, before the general argument in n-dimensions came around). 




## References

### Introductions to category theory in physics {#CatsinPhysics}

In 

* [[Bob Coecke]], _Introducing categories to the practicing physicist_ ([arXiv:0808.1032](http://arxiv.org/abs/0808.1032))

* [[Bob Coecke]], _Categories for the practising physicist_ ([arXiv:0905.3010](http://arxiv.org/abs/0905.3010))

the authors try to motivate and introduce some basic concepts of [[category theory]] for an audience familiar with standard physics and in particular with [[quantum mechanics]]. The article focuses towards the end on [[monoidal categories]], their description in terms of [[string diagram]]s and [[quantum mechanics in terms of dagger-compact categories]].

More details on the use of string diagrams in dagger-categories for the description of quantum mechanics is is

* [[Bob Coecke]], _Kindergarten quantum mechanics_ ([arXiv:quant-ph/0510032](http://arxiv.org/abs/quant-ph/0510032))

* [[Bob Coecke]], _Quantum Picturalism_ ([arXiv:0908.1787](http://arxiv.org/abs/0908.1787))

A similar introduction to the relation between quantum mechanics and [[monoidal categories]], but more from the perspective of [[FQFT]] is in

* [[John Baez]], _Quantum quandaries_ ([arXiv:quant-ph/0404040](http://arxiv.org/abs/quant-ph/0404040))


### Introductions to higher category theory and physics

A historical introduction to some aspects of [[n-categories]] (for low $n$) in physics can be found here:

* [[John Baez]] and [[Aaron Lauda]], _A prehistory of $n$-categorical physics_ ([pdf](http://math.ucr.edu/home/baez/history.pdf)), to appear in _Deep Beauty: Mathematical Innovation and the Search for an Underlying Intelligibility of the Quantum World_, ed. Hans Halvorson.

[[Jim Stasheff]] is also writing a historical introduction to applications of more [[homotopy theory|homotopy theoretic]] [[higher category theory]]:

* [[Jim Stasheff]], [[A Survey of Cohomological Physics]] 

The following book-to-be aims to give picture of the present state of the art of describing the category-theoretic structure of the universe, as far as fundamental physics is concerned

* [[Hisham Sati]], [[Urs Schreiber]], [[Branislav Jurco]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_


### On the quantization procedure {#LitOnQuantization}

First sketches of the idea that [[path integral]] [[quantization]] may have a formalization in terms of [[higher category theory]] appeared in

* [[Dan Freed]], _Higher Algebraic Structures and Quantization_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115))

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

* [[Dan Freed]], [[Mike Hopkins]], _On Raomnd-Ramond fields and K-theory_ ([pdf](http://web.me.com/teichner/Math/Smooth_Cohomology_files/Freed-Hopkins.pdf))
{#FreedHopkins}

Motivated by this the theory of differential cohomology itself was developed in

* [[Mike Hopkins]], I. Singer _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_
{#HopkinsSinger}

and shown to encode sublte [[quantum anomaly]]-cancellation phenomena in gauge theory. A systematic formal description of the nature of these quantum anomalies and further discussion of applications on differential cohomology in physics is in 

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_
{#Freed}

This article startes with an introduction on just basic [[electromagnetism]] and points out that already there, in the presence of [[magnetic charge]], a careful analysis of [[quantum anomalies]] shows that there are higher gauge theoretic effects even in this familiar theory.

### On topos-theoretic formulations of physics {#RefsOnToposTheoreticPhysics}

#### Classical

The observation that any formalization of physics ought to take place in a suitble [[topos]] has been promoted early on by [[Bill Lawvere]]. Lawvere started out as a student in [[continuum mechanics]] and his search for a formalization of physics made him end up being one of the most general abstract thinkers in [[category theory]]. 

Lawvere thought about [[classical physics]] governed, as it is since Newton, by the theory of [[differential equation]]s. He proposed that [[differential geometry]] is something that takes place inside a [[smooth topos]] -- a [[topos]] with a suitable notion of [[infinitesimal object]]s -- an approach now known as [[synthetic differential geometry]]. 

In 

* Lawvere, _Categorical dynamics_, lecture (1967)

which is recalled in

* Lawvere, _Toposes of laws of motion_ , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))

he sketched an outline both of synthetic differenial geometry in general and its application to the formulation of the [[differential equation]]s in classical dynamics.

In this spirit he to search for [[category theory|category theoretic]] formalizations of fundamental ( _metaphysical_  in the good sense of the word) ontological concepts. A collection of such formalizations is indicated in

* Lawvere, _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

On [page 14](http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf#page=14) there appears the hint of the general abstract definition of a [[locally connected topos]] as a general abstract [[gros topos]] context for geometric spaces. This idea was then refined to the concept of a [[cohesive topos]] in 

* Lawvere, _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

#### Quantum

Independent of these developments is another proposal for a role of topos theory in [[quantum mechanics]] initiated by [[Chris Isham]]. The motivation here is the observation that the [[Kochen-Specker theorem]] -- which may be used to formalize the way in which [[quantum mechanics]] fails to secretly a theory of classical mechanics -- has a natural interpretation in terms of the [[internal logic]] of the [[presheaf topos]] on the category of commutative sub-algebras of a given bounded [[operator algebra]].

This observation led Isham to propose a fundamental role of these presheaf toposes in [[quantum mechanics]].

* Andread Doering, C.J. Isham, _A Topos Foundation for Theories of Physics_ I-IV ([arXiv](http://arxiv.org/abs/quant-ph/0703060))

This idea was further refined in 

* [[Chris Heunen]], [[Nicolaas Landsman]], [[Bas Spitters]], _A topos for algebraic quantum theory_

  **Abstract**

  The aim of this paper is to relate [[AQFT|algebraic quantum mechanics]] to [[topos theory]], so as to construct new foundations for [[quantum logic]] and quantum spaces. Motivated by Bohr's idea that the empirical content of quantum physics is accessible only through classical physics, we show how a [[C-star-algebra]] of [[observable]]s $A$ induces a [[topos]] $T(A)$ in which the amalgamation of all of its commutative subalgebras comprises a single commutative $C^*$-algebra. According to the [[constructive mathematics|constructive]] [[Gelfand duality]] theorem of Banaschewski and Mulvey, the latter has an internal spectrum $S(A)$ in $T(A)$, which in our approach plays the role of a quantum [[phase space]] of the system. Thus we associate a [[locale]] (which is the topos-theoretical notion of a space and which intrinsically carries the intuitionistic logical structure of a [[Heyting algebra]]) to a $C^*$-algebra (which is the noncommutative notion of a space). In this setting, [[state]]s on $A$ become [[probability measure]]s (more precisely, valuations) on $S(A)$, and self-adjoint elements of $A$ define continuous functions (more precisely, locale maps) from $S(A)$ to Scott's interval domain. Noting that open subsets of $S(A)$ correspond to propositions about the system, the pairing map that assigns a (generalized) [[truth value]] to a state and a proposition assumes an extremely simple categorical form. Formulated in this way, the quantum theory defined by $A$ is essentially turned into a classical theory, internal to the topos $T(A)$. 


[[!redirects n-categorical physics]]
