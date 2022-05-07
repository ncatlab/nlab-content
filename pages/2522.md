
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
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


Where generally a [[symmetry]] is an invariance under a [[group]] [[action]] (after all the mathematical term "[[group]]" is a contraction of _group of symmetries_), or, [[infinitesimal space|infinitesimally]], an invariance under a [[Lie algebra]] action,  in the general sense of the word, a **supersymmetry** is invariance under a [[supergroup]] action or a [[super Lie algebra]] action. 

By [[Deligne's theorem on tensor categories]] it is precisely the context of supersymmetry in which [[tensor categories]] over the [[complex numbers]] exhibit full [[Tannaka duality]].

In the stricter sense of the word as it originates in theoretical fundamental [[physics]], _supersymmetry_ refers specifically to supergeometric extensions of the [[isometry group]] (or its Lie algebra)  of the local model of [[spacetime]]. For [[Minkowski spacetime]] this is the [[Poincaré group]] with its [[Poincaré Lie algebra]] and their super-extensions are accordingly known as the [[super Poincaré group]]  and [[super Poincaré Lie algebra]]. In physics the latter are often referred to simply as  **the supersymmetry algebra**. An odd element in this [[super Lie algebra]] is called a **supersymmetry generator** and its [[Hamiltonian]] is called a _[[supercharge]]_. More generally, if spacetime geometry is taken to be [[conformal geometry]] or [[de Sitter spacetime]]/[[anti-de Sitter spacetime]], then one considers supergeometric extensions of the [[conformal group]], [[de Sitter group]] and [[anti de Sitter group]], respectively, and then these are the relevant "supersymmetries".

With the focus on spacetime symmetry groups implicitly understood, this implies that supersymmetry is the group theory relevant for [[super Cartan geometry]] locally modeled on [[super Minkowski spacetime]] or [[super anti de Sitter spacetime]], etc. In terms of physics and in view of the [[first order formulation of gravity]], this means that "locally gauged" supersymmetry is the super-geometric generalization from [[Einstein gravity]] to [[supergravity]] or, respectively, from [[conformal field theory]] to [[superconformal field theory]], etc.







### Global supersymmetry and superparticles

By [[Wigner-Weyl theory]] we have in ordinary [[quantum field theory]] that [[unitary representations of the Poincaré group]] correspond to the [[particle]]s in the theory. For a _globally_ supersymmetric quantum field theory the [[Poincaré group]] here is replaced by the [[super Poincaré group]] and accordingly particles are now [[irreducible representation]]s of this group: the irreducible [[unitary representations of the super Poincaré group]]. The new -- odd graded -- pieces of these representations -- called **[[supermultiplets]]** -- appearing this way  are called the **[[superpartners]]** of the original _bosonic_ particles.

### Local supersymmetry: supergravity

To be distinguished from this _global supersymmetry_ is _local supersymmetry_ (see at _[[gauge group]]_ and at _[[Cartan connection]]_):  given a [[gauge theory]] whose fields are [[connection on a bundle|connections]] with values in the [[Poincaré Lie algebra]] -- the theory of [[gravity]] in its [[first order formulation of gravity|first order formulation]] -- a supersymmetric extension is similarly a [[gauge theory]] with fields being connections in the [[super Poincaré Lie algebra]] -- a theory of [[supergravity]]. A [[gauge transformation]] in such a theory is called a **local supersymmetry transformation**.

### The relation between local and global supersymmetry

The distinction between local and global supersymmetry is important when considering [[supergravity]] in [[perturbation theory]] where all fields are expanded around a fixed [[spacetime]] [[geometry]] and fixed [[background gauge fields]] that form a solution of the [[Euler-Lagrange equations]].

While the theory of supergravity as such has, by definition, local supersymmetry, a solution to it may but need not have any _global supersymmetry_ left. In fact, generically it will not.

To see this, it is maybe helpful to compare with the analogous statement in non-supersymmetric [[QFT]]:

the theory of [[gravity]] is _locally_ Poincar&#233;-symmetric: in [[first order formulation of gravity|first order formulation]] it is a [[Poincaré group]] [[gauge theory]]. Nevertheless, any of its solutions -- which is a [[pseudo-Riemannian manifold]] -- may, but need not, have any Poincar&#233;-symmetry. It does have such a _global_ symmetry for every [[Killing vector]] on the [[spacetime]]. Such may or may not exist. Generically it does not exist.

The analog of these Killing vectors in [[supergravity]] are [[Killing spinor]]s: [[covariantly constant spinor]]s ([[section]]s of a 
[[spinor bundle]] annihilated by the [[spin connection]]'s [[covariant derivative]]).
For every such, the background has one global supersymmetry transformation. These may or may not exist. Generically they do not.

The most famous example of this is that of [[Calabi-Yau manifolds]]: a  standard assumption on [[phenomenology|phenomenological]] [[model building]] that used to be very popular around the turn of the millennium (but is maybe experimentally ruled out at the time of this writing) is that 

1. the [[spacetime]] we see around us locally looks like a product $M^4 \times Y^6$ of 4-dimensional [[Minkowski space]] times a tiny closed [[Riemannian manifold]] $Y^6$ (so tiny that it is not directly observable but manifests itself only by way of its lowest excitation modes that look like different [[particle]] species on the remaining $M^4$ -- see [[Kaluza-Klein mechanism]] );

1. such that on this product space a single covariant constant spinor exists, such that the resulting effective theory on $M^4$ has a single global supersymmetry ("$N=1$ supersymmetry").

One finds that this condition is solved precisely by $Y^6$ being a [[Calabi-Yau manifold]]. For more on this see the corresponding section at [[heterotic string theory]].

But notice that nothing in the theory of 10-dimensional [[supergravity]] _demands_ that its solutions have a global supersymmetry left (generically they will not) nor that they factor locally as $M^4 \times Y^6$. All this is an _ansatz_ a _phenomenological model_ . It only says that _if_ we make this ansatz, then $Y^6$ needs to be a Calabi-Yau space. In fact, it turns out to be nontrivial to check that with all the other fields taken into account, such a factor ansatz is indeed consistent. (This problem of "moduli stabilization" is discussed a little bit at [[landscape of string theory vacua]].)

Latest experimental results strongly suggest that this model of global $(N = 1)$-supersymmetry at observable energies is not a description of our phenomenological reality. Still, it could well be that the underlying theory of the world is nevertheless not plain [[general relativity]] but [[supergravity]].

### Observed supersymmetry: on the worldline

To appreciate this point it is worthwhile to notice that supersymmetric quantum field theory in fact _has_ been observed in nature, already since a century ago. To see this, one needs to notice how [[fundamental particle]]s are described by [[sigma model]] quantum field theories (see there) on their [[worldvolume]]:

the $\sigma$-model action functional for the standard Dirac [[spinor]] particle -- such as [[electron]]s and [[quarks]], the particles that all the matter in the world is made of -- just happens to have [[worldline supersymmetry]]. This is discussed at _[[spinning particle]]_ . Notice that this is true for electrons and quarks in the non-supersymmetric [[standard model of particle physics]]: the [[target space]] theory is completely void of (global) supersymmetry, and still the [[worldvolume]] theory of any [[fermion]] is automatically supersymmetric.


### Conjectured supersymmetry: on spacetime and on the worldsheet
 {#SupersymmetryOnSpacetimeAndWorldsheet}

A similar statement as for the [[spinning particle]] and its automatic local [[worldline supersymmetry]] indeed also holds for the _[[spinning string]]_ : while it is a conjecture of [[string theory]] which has not been experimentally verified that fundamentally the [[sigma-model]] theories that describe the physics around us is defined not on 1-dimensional but on 2-dimensional [[worldvolume]]s, it remains a noteworthy fact that the standard [[action functional]] for the [[string]] [[sigma model]] with [[fermion]]s _on the [[worldsheet]]_ just happens to be locally supersymmetric. It is hard to avoid this! And indeed, this was how the abstract notion of supersymmetry in [[quantum field theory]] was realized in the west first: people wrote down action functionals for _[[spinning string]]s_ and noticed that these happened to have an interesting graded symmetry (see there for references).

So while it is an open conjecture of [[string theory]] that the particle [[worldline]]s that are experimentally observed are secretly really [[worldsheet]]s, assuming that this conjecture holds for [[fermion]]s automatically implies local worldsheet supersymmetry and the [[superstring]].

Now, the effective [[spacetime]] [[target space]] theories arising from [[second quantization]] of the [[superstring]] are fairly well understood: these are higher dimensional [[supergravity]] theories coupled to the various [[background gauge field|higher gauge fields]] that are also in the spectrum of the string (the [[Kalb-Ramond field]] and the [[RR-field]]s, notably). They are called _[[type II supergravity]]_ , [[heterotic supergravity]], etc. All of these are obtained by compactifications of [[11-dimensional supergravity]].

This means that the assumption of [[spinning string]] [[sigma-models]] automatically implies that the [[spacetime]] [[QFT]] that we observe also has _local_ supersymmetry.

Over the decades it has often been suggested that therefore the assumption of [[spinning string]]s "suggests" or "favours" the observation of superpartner particles in accelerators. However, this is not so:

in these constructions the [[particle]] species seen in accelerators are [[Kaluza-Klein mechanism|KK-modes]] and/or brane-brane open string modes of the compactified locally supersymmetric theory. This means that they are determined by the compactification geometry. Only if that has a global [[Killing spinor]] is the effective 4-dimensional theory globally supersymmetric and exhibits superpartners. As was mentioned above, for spacetimes of the form $M^4 \times Y^6$ this is the case precisely if $Y^6$ is a [[Calabi-Yau manifold]].

But this is far from being the generic situation. This is clear qualitatively (a generic solution to the super-[[Einstein equations]] will not have a [[Killing spinor]]). A more sophisticated and quantitative argument to the same effect is given, for instance, in ([DLSW08](#DLSW)).





### In fundamental physics

Supersymmetric extensions of [[quantum field theories]] have been felt to be compelling in fundamental physics for _formal reasons_ : the simple step from [[Lie algebra]]s to [[super Lie algebra]]s

* make a pure theory of [[gravity]] seamlessly incorporate [[fermion]]s and [[gauge field]]s;

* leads to better [[renormalization]] properties (indeed the speculation that $N=8, D=4$ [[supergravity]] is fully renormalizable -- in stark contrast to ordinary [[gravity]] has more recently been checked up to high loop orders);

* produces a wealth of interesting mathematical structures. For instance 

  * [[Morse theory]] of a [[Riemannian manifold]] can naturally be understood in terms of [[supersymmetric quantum mechanics]] for [[superparticle]]s propagating on that manifold;

  * the interpretation of [[quantum field theories]] in terms of [[generalized cohomology]] theories only works for supersymmetric theories (see [[(1,1)-dimensional Euclidean field theories and K-theory
]] and [[(2,1)-dimensional Euclidean field theory]])

  * "topological twists" of supersymmetric field theories are a major source of examples of [[TQFT]]s, for instance the [[A-model]] and the [[B-model]] [[TCFT]] arise from such twists of 2-dimensional [[supergravity]] and there are deep connections between the [[geometric Langlands correspondence]] and topologically twisted [[super Yang-Mills theory]].

Moreover, since various observables in supersymmetric QFTs are easier to compute than in non-supersymmetric theories, supersymmetric quantum field theory is being used to _approximate_ certain aspects of other QFTs. For instance certain correlators in ordinary [[Yang-Mills theory]] coupled to [[spinors in Yang-Mills theory]] can be computed using an auxiliary [[super Yang-Mills theory]].

Therefore, if nothing else, supersymmetric quantum field theories constitute a part of the whole space of quantum field theories which is useful for understanding general properties of that space. What is however still missing is any experimental evidence that the world is fundamentally described by a supersymmetric quantum field theory.

## Definition
 {#Definition}


We start by saying what it means, in generality, to have a supersymmetric extension of an ordinary symmetry, then we specialize to spacetime supersymmetry.

Here we are concerned with [[symmetry groups]] that are [[Lie groups]], and we start by considering only the infinitesimal approximation, hence their [[Lie algebras]].

To discuss super-extensions of Lie algebras, recall from _[[geometry of physics -- supergeometry]]_ the concept of _[[super Lie algebras]]_:

+-- {: .num_defn #SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}
###### Definition

A _[[super Lie algebra]]_ is a [[Lie algebra]] [[internalization|internal]]
to the [[symmetric monoidal category]] $sVect = (Vect^{\mathbb{Z}/2}, \otimes_k, \tau^{super} )$ of [[super vector spaces]].
Hence this is

1. a [[super vector space]] $\mathfrak{g}$;

1. a homomorphism

   $$
     [-,-] \;\colon\; \mathfrak{g} \otimes_k \mathfrak{g} \longrightarrow \mathfrak{g}
   $$

   of super vector spaces (the _super Lie bracket_)

such that

1. the bracket is skew-symmetric in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g}
         &
           \overset{\tau^{super}_{\mathfrak{g},\mathfrak{g}}}{\longrightarrow}
         &
       \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       {}^{\mathllap{[-,-]}}\downarrow && \downarrow^{\mathrlap{[-,-]}}
       \\
       \mathfrak{g} &\underset{-1}{\longrightarrow}& \mathfrak{g}
     }
   $$

   (here $\tau^{super}$ is the [[braiding]] [[natural isomorphism]] in the category of [[super vector spaces]])

1. the [[Jacobi identity]] holds in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       &&
         \overset{\tau^{super}_{\mathfrak{g}, \mathfrak{g}} \otimes_k id }{\longrightarrow}
       &&
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       & {}_{\mathllap{[-,[-,-]]} - [[-,-],-] }\searrow && \swarrow_{\mathrlap{[-,[-,-]]}}
       \\
       && \mathfrak{g}
     }
     \,.
   $$

=--

Externally this means the following:

+-- {: .num_prop #SuperLieAlgebraTraditional}
###### Proposition

A [[super Lie algebra]] according to def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces} is equivalently

1. a $\mathbb{Z}/2$-[[graded vector space]] $\mathfrak{g}_{even} \oplus \mathfrak{g}_{odd}$;

1. equipped with a [[bilinear map]] (the _super Lie bracket_)

   $$
     [-,-] : \mathfrak{g}\otimes_k \mathfrak{g} \to \mathfrak{g}
   $$

   which is _graded_ skew-symmetric: for $x,y \in \mathfrak{g}$ two elements of homogeneous degree $\sigma_x$, $\sigma_y$, respectively, then

   $$
     [x,y] = -(-1)^{\sigma_x \sigma_y} [y,x]
     \,,
   $$

1. that satisfies the $\mathbb{Z}/2$-graded [[Jacobi identity]] in that
for any three elements $x,y,z \in \mathfrak{g}$ of homogeneous super-degree $\sigma_x,\sigma_y,\sigma_z\in \mathbb{Z}_2$ then

   $$
     [x, [y, z]] = [[x,y],z] + (-1)^{\sigma_x \cdot \sigma_y} [y, [x,z]]
     \,.
   $$

A [[homomorphism]] of super Lie algebras is a homomorphisms of the underlying [[super vector spaces]]
which preserves the Lie bracket. We write

$$
  sLieAlg
$$

for the resulting [[category]] of super Lie algebras.

=--

Some obvious but important classes of examples are the following:

+-- {: .num_example #SuperVectorSpaceAsAbelianSuperLieAlgebra}
###### Example

every $\mathbb{Z}/2$-[[graded vector space]] $V$ becomes a
[[super Lie algebra]]
(def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional})
by taking the super Lie bracket to be the [[zero morphism|zero map]]

$$
  [-,-] = 0
  \,.
$$

These may be called the "abelian" super Lie algebras.

=--


+-- {: .num_example #OrdinaryLieAlgebraAsSuperLieAlgebra}
###### Example

Every ordinary [[Lie algebra]] becomes a [[super Lie algebra]]
(def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional})
concentrated in even degrees. This constitutes a [[fully faithful functor]]

$$
  LieAlg \hookrightarrow sLieAlg
  \,.
$$

which is a  [[coreflective subcategory]] inclusion in that it has a [[left adjoint]]

$$
  LieAlg
    \underoverset
     {\underset{ \overset{ \rightsquigarrow}{(-)} }{\longleftarrow}}
     {\hookrightarrow}
     {\bot}
  sLieAlg
$$

given on the underlying super vector spaces by restriction to the even graded part

$$
  \overset{\rightsquigarrow}{\mathfrak{s}} = \mathfrak{s}_{even}
  \,.
$$

=--

Using this we may finally say what a super-extension is supposed to be:

+-- {: .num_defn #SuperExtensions}
###### Definition

Given an ordinary [[Lie algebra]] $\mathfrak{g}$, then a _super-extension_  of $\mathfrak{g}$
is a [[super Lie algebra]] $\mathfrak{s}$ (def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional}) equipped with a [[monomorphism]] of the form

$$
  i \;\colon\; \mathfrak{g} \hookrightarrow  \mathfrak{s}
$$

(where $\mathfrak{g}$ is regarded as a super Lie algebra according to example \ref{OrdinaryLieAlgebraAsSuperLieAlgebra})

such that this is an [[isomorphism]] on the even part (example \ref{OrdinaryLieAlgebraAsSuperLieAlgebra})

$$
  \overset{\rightsquigarrow}{i}
    \;\colon\;
  \mathfrak{g} \overset{\simeq}{\longrightarrow} \mathfrak{s}_{even}
  \,.
$$



=--


We now make explicit structure involved in super-extensions of Lie algebras:

+-- {: .num_prop #DataInSuperExtension}
###### Proposition

Given an ordinary [[Lie algebra]] $\mathfrak{g}$, then a choice of super-extension
$\mathfrak{g} \hookrightarrow \mathfrak{s}$ according to def. \ref{SuperExtensions}
is equivalently the following data:

1. a [[vector space]] $S$;

1. a Lie action of $\mathfrak{g}$ on $S$, hence a Lie algebra homomorphism

   $$
     \rho_{(-)} : \mathfrak{g} \longrightarrow \mathfrak{gl}(S)
   $$

   from $\mathfrak{g}$ to the [[endomorphism Lie algebra]] of $S$;

1. a symmetric [[bilinear map]]

   $$
     (-,-) \;\colon\; S \otimes_k S \longrightarrow \mathfrak{g}
   $$

such that

1. the pairing is $\mathfrak{g}$-equivariant in that for all $t \in \mathfrak{g}$ then

   $$
     \rho_{t}(-,-) = (\rho_t(-),(-)) + (-,\rho_t(-))
   $$

1. the pairing satisfies

   $$
     \rho_{(\phi,\phi)}(\phi) = 0
   $$
   
   for all $\phi \in S$.


=--

+-- {: .proof}
###### Proof

By definition of super-extension, the underlying super vector space of $\mathfrak{s}$ is necessarily of the form

$$
  \mathfrak{s}_{even} = \underset{\mathfrak{s}_{even}}{\underbrace{\mathfrak{g}}} \oplus \underset{\mathfrak{s}_{odd}}{\underbrace{S}}
$$

for some vector space $S$.

Moreover the super Lie bracket on $\mathfrak{s}$ restricts to that of $\mathfrak{g}$ when restricted to  $\mathfrak{g} \otimes_{k}\mathfrak{g}$
and otherwise constitutes

1. a bilinear map

   $$
     \rho_{(-)}(-) \coloneqq [-,-]\vert_{\mathfrak{s}_{even}\oplus \mathfrak{s}_{odd}} \;\colon\; \mathfrak{g} \otimes_k S \longrightarrow S
   $$

1. a symmetric bilinear map

   $$
     (-,-) \coloneqq [-,-]\vert_{\mathfrak{s}_{odd} \oplus \mathfrak{s}_{odd}} \;\colon\; S \otimes_k S \longrightarrow \mathfrak{g}
     \,.
   $$

This yields the claimed [[stuff, structure, property|structure]]. The claimed [[stuff, structure, property|properties]]
of these linear maps are now just a restatement of the super-Jacobi identity in terms of this data:

1. The restriction of the super Jacobi identity of $\mathfrak{s}$ to $\mathfrak{s}_{even} \otimes_k \mathfrak{s}_{even} \otimes_k \mathfrak{s}_{even}$ is equivalently the Jacobi identity in $\mathfrak{g}$ and hence is no new constraint;

1. The restriction of the super Jacobi identity of $\mathfrak{s}$ to $\mathfrak{s}_{even} \otimes_k \mathfrak{s}_{even} \otimes_k \mathfrak{s}_{odd}$ says that for $t_1,t_2 \in \mathfrak{g}$ and $\phi \in S$ then

   $$
     \rho_{t_1}( \rho_{t_2}(\phi) ) = \rho_{[t_1,t_2]}(\phi) + \rho_{t_1}( \rho_{t_2}(\phi) )
     \,.
   $$

   This is equivalent to

   $$
     \rho_{t_1} \circ \rho_{t_2} - \rho_{t_2} \circ \rho_{t_1} = \rho_{[t_1,t_2]}
   $$

   which means equivalently that $\rho_{(-)}$ is a Lie algebra homomorphism from $\mathfrak{g}$ to the
   [[endomorphism Lie algebra]] of $S$.

1. The restriction of the super Jacobi identity of $\mathfrak{s}$ to $\mathfrak{s}_{even} \otimes_k \mathfrak{s}_{odd}  \otimes_k \mathfrak{s}_{odd}$ says that for $t \in \mathfrak{g}$ and $\phi,\psi \in S$ then

   $$
     \rho_{t}(\phi,\psi) = (\rho_t(\phi), \psi) + (\phi, \rho_t(\psi))
     \,.
   $$

   This is exactly the claimed $\mathfrak{g}$-equivariance of the pairing.

1. The restriction of the super Jacobi identity of $\mathfrak{s}$ to $\mathfrak{s}_{odd} \otimes_k \mathfrak{s}_{odd}  \otimes_k \mathfrak{s}_{odd}$ implies that for all $\psi \in S$ that

   $$
     [\psi,(\psi,\psi)] = [ (\psi,\psi), \psi  ] - [\psi, (\psi, \psi)]
   $$

   and hence that

   $$
     [(\psi,\psi),\psi] =  \rho_{(\psi,\psi)}(\psi) = 0
     \,.
   $$

   Hence it only remains to show that this special case is in fact equivalent to the full odd-odd-odd super Jacobi identity. This follows by polarization: First insert $\psi = \phi_1 + \phi_2$ into the above cubic condition to obtain a quadratic condition, then polarize once more in $\phi_2$.

=--

+-- {: .num_example #TrivialSuperExtension}
###### Example

Given an ordinary [[Lie algebra]] $\mathfrak{g}$, then for every choice of [[vector space]] $V$
there is the _trivial_ super extension (def. \ref{SuperExtensions}) of $\mathfrak{g}$, with underlying
vector space

$$
  \mathfrak{s} \coloneqq \mathfrak{g} \oplus V
$$

and with both the action and the pairing (via prop. \ref{DataInSuperExtension}) trivial:

$$
  \rho = 0
$$

and

$$
  (-,-) = 0
  \,.
$$


=--

The key example of interest now is going to be this:

+-- {: .num_example #SuperExtensionOfPoincare}
###### Example

For $d \in \mathbb{N}$, a super extension (def. \ref{SuperExtensions}) of the [[Poincaré Lie algebra]]
$\mathfrak{iso}(\mathbb{R}^{d-1,1})$ (recalled as def. \ref{PoincareLieAlgebra} below)
which is non-trivial (def. \ref{TrivialSuperExtension}) is obtained from the following data:

1. a [[Lie algebra representation]] $\rho$ of $\mathfrak{so}(d-1,1)$ on some [[real vector space]] $S$;

1. an $\mathfrak{so}$-equivariant symmetric $\mathbb{R}$-[[bilinear map|bilinear pairing]] $(-,-) \colon S \otimes_k S \to \mathbb{R}^{d-1,1}$

It turns out that data as in example \ref{SuperExtensionOfPoincare} is given for $\rho$ the Lie algebra version of a [[real spin representation]] of the [[spin group]] $Spin(d-1,1)$ (see [this prop](geometry+of+physics+--+superymmetry#SpinorToVectorPairing)). These are introduced and discussed at _[[geometry of physics -- supersymmetry]]_ in the section _[Real spin representations](geometry+of+physics+--+superymmetry##RealSpinRepresentations)_.

The super-extensions of the [[Poincaré Lie algebra]] induced by
[[real spin representations]] are called _[[super Poincaré Lie algebras]]_ (def. \ref{SuperMinkowskiSpacetime}) below.
These are the standard _[[supersymmetry]] algebras_ in the physics literature.

=--

But beware that there are more super-extensions of the Poincar&#233; Lie algebra:

+-- {: .num_example #AnExotiSuperExtensionOfThePoincareLieAlgebra}
###### Example
**(an exotic super-extension of the Poincar&#233; Lie algebra)

Let $d \in \{3,4,6,10\}$ and let $S \in Rep_{\mathbb{R}}(Spin(d-1,1))$ be an [[irreducible representation|irreducible]]
[[real spin representation]] in that dimension. Let $(-,-) \colon S \otimes S \to \mathbb{R}^{d-1,1}$ be the
symmetric spinor pairing as in example \ref{SuperExtensionOfPoincare}, but let the action on $S$ via the even-odd
super-bracket not be the Spin-action of $\mathfrak{so}$, but the [[Clifford algebra]] action 

$$
  \Gamma(-) \;\colon \; \mathbb{R}^{d-1,1} \longrightarrow End(S)
  \,.
$$

of $\mathbb{R}^{d-1,1}$. Then the condition

$$
  \Gamma(\psi,\psi)(\psi) = 0
$$

from prop. \ref{DataInSuperExtension} does hold: this turns out to be equivalent to the 
[[Green-Schwarz superstring]] cocycle condition in these dimensions, here in its incarnation as the "3-$\psi$ rule" of [Schray 96](#Schray96), see [Baez-Huerta 09, theorem 10](#BaezHuerta09).

Now $\Gamma(-)$ thus defined is clearly not a [[Lie algebra action]] and hence fails one of the other conditions in
prop. \ref{DataInSuperExtension}, but this is readily fixed: take $S \coloneqq S_+ \oplus S_-$ to be 
the [[direct sum]] of two copies of the [[Majorana spinor]] representation and take  $\Gamma(-)$ to map as
before, but from $S_+$ to $S_-$, acting as zero on $S_-$. This forces the [[commutator]] of [[endomorphisms]]
in the image of $\Gamma$ to vanish, and hence makes $\Gamma(-)$ a [[Lie algebra action]] of the abelian Lie algebra
$\mathbb{R}^{d-1,1}$. Hence we get an "exotic" super-extension of the [[Poincaré Lie algebra]].



=--




+-- {: .num_remark}
###### Remark

By prop. \ref{DataInSuperExtension} the data in example \ref{SuperExtensionOfPoincare} is sufficient for
producing super-extensions (in the sense of def. \ref{SuperExtensions}) of [[Poincaré Lie algebras]], namely the
[[super Poincaré Lie algebras]].
It is however not necessary: example \ref{AnExotiSuperExtensionOfThePoincareLieAlgebra} is a super-extension in the sense of def. \ref{SuperExtensions} of the [[Poincaré Lie algebra]]
which is not a [[super Poincaré Lie algebra]] of the form of example \ref{SuperExtensionOfPoincare}.

One may add further natural conditions on the super-extension in order to narrow down to the [[super Poincaré super Lie algebras]]:

1. From the assumption alone that $S$ is a [[spin representation]] and using that the $Spin$-equivariant pairing has to take [[irreducible representations]] to an irreducible representation, one may in some dimensions already deduce that the pairing has to land in $\mathbb{R}^{d} \hookrightarrow \mathfrak{iso}(\mathbb{R}^{d-1,1})$. For $d = 4$ and $S$ the irreducible [[Majorana representation]] this is done in [Varadarajan 04, section 3.2](#Varadarajan04).

1. One may appeal to the _[[Haag–Łopuszański–Sohnius theorem]]_. This does rule out exotic super-extensions, by imposing the 
   additional condition that $P_a P^a$ remains a [[Casimir operator]]
   after super-extension, and more conditions. These conditions are well motivated from the expected symmetry-behaviour of
   [[S-matrices]] in [[field theory]]. 

At _[[geometry of physics -- supersymmetry]]_ in the section _[supersymmetry from the superpoint](geometry+of+physics+--+superymmetry##SupersymmetryFromTheSuperpoint)_ we discuss something at least
related. The [[super Poincaré Lie algebras]] at least in certain dimensions are singled out from a different perspective:
they are precisely the result of iterative maximal invariant [[central extensions]] of the superpoint.

=--

Now we write out the supersymmetry algebra thus obtained more explicitly.
In all of the following it is most convenient to regard [[super Lie algebras]] dually  via their [[Chevalley-Eilenberg algebras]]:

+-- {: .num_defn #CEAlgebraofSuperLieAlgebra}
###### Definition

For $\mathfrak{g}$ a [[super Lie algebra]] of [[finite number|finite]] [[dimension]], then its _[[Chevalley-Eilenberg algebra]]_ $CE(\mathfrak{g})$ is the super-[[Grassmann algebra]] on the [[dual vector space|dual]] super vector space

$$
  \wedge^\bullet  \mathfrak{g}^\ast
$$

equipped with a [[differential]] $d_{\mathfrak{g}}$ that on generators is the linear dual of the super Lie bracket

$$
  d_{\mathfrak{g}} \;\coloneqq\; [-,-]^\ast \;\colon\; \mathfrak{g}^\ast \to \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
$$

and which is extended to $\wedge^\bullet \mathfrak{g}^\ast$ by the graded Leibniz rule (i.e. as a graded [[derivation]]).

$\,$

Here all elements are $(\mathbb{Z} \times \mathbb{Z}/2)$-bigraded, the first being the _cohomological grading_ $n$ in $\wedge^\n \mathfrak{g}^\ast$, the second being the _super-grading_ $\sigma$ (even/odd).

For $\alpha_i \in CE(\mathfrak{g})$ two elements of homogeneous bi-degree $(n_i, \sigma_i)$, respectively,
the [[signs in supergeometry|sign rule]] is

$$
  \alpha_1 \wedge \alpha_2 = (-1)^{n_1 n_2} (-1)^{\sigma_1 \sigma_2}\; \alpha_2 \wedge \alpha_1
  \,.
$$

(See at _[[signs in supergeometry]]_ for discussion of this sign rule and of an alternative sign rule that is also in use. )

=--

We may think of $CE(\mathfrak{g})$ equivalently as the [[dg-algebra]] of [[invariant differential form|left-invariant]]
[[super differential forms]] on the [[Lie theory|corresponding]] simply connected [[super Lie group]] .


The concept of [[Chevalley-Eilenberg algebras]] is traditionally introduced as a means to define
[[Lie algebra cohomology]]:

+-- {: .num_defn #SuperLieAlgebraCohomology}
###### Definition

Given a [[super Lie algebra]] $\mathfrak{g}$, then

1. an _$n$-cocycle_ on $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is an element of degree $(n,even)$ in its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ (def. \ref{CEAlgebraofSuperLieAlgebra}) which is $d_{\mathbb{g}}$ closed.

1. the cocycle is non-trivial if it is not $d_{\mathfrak{g}}$-exact

1. hene the _super-[[Lie algebra cohomology]]_ of $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is the [[cochain cohomology]] of its [[Chevalley-Eilenberg algebra]]

   $$
     H^\bullet(\mathfrak{g}, \mathbb{R}) = H^\bullet(CE(\mathfrak{g}))
     \,.
   $$

=--



The following says that the [[Chevalley-Eilenberg algebra]] is an equivalent incarnation of the [[super Lie algebra]]:

+-- {: .num_prop}
###### Proposition

The functor

$$
  CE \;\colon\; sLieAlg^{fin}  \hookrightarrow dgAlg^{op}
$$

that sends a finite dimensional [[super Lie algebra]] $\mathfrak{g}$ to its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$
(def. \ref{CEAlgebraofSuperLieAlgebra}) is a [[fully faithful functor]] which hence exibits [[super Lie algebras]]
as a [[full subcategory]] of the [[opposite category]] of [[differential-graded algebras]].

=--







+-- {: .num_defn #SuperMinkowskiSpacetime}
###### Definition

Let 

$$
  d \in \mathbb{N}
$$ 

be a [[spacetime]] [[dimension]] and let 

$$
  N \in Rep_{\mathbb{R}}(Spin(d-1,1))
$$

be a [[real spin representation]] of the [[spin group]] cover $Spin(d-1,1)$ of the [[Lorentz group]] $O(d-1,1)$
in this dimension. Then the _$d$-dimensional $N$-supersymmetric [[super-Minkowski spacetime]]_ $\mathbb{R}^{d-1,1|N}$
is the [[super Lie algebra]] that is characterized by the fact that its [[Chevalley-Eilenberg algebra]]
$CE(\mathbb{R}^{d-1,1})$
is as follows:

The algebra has generators (as an [[associative algebra]] over $\mathbb{R}$)

$$
   \underset{deg = (1,even)}{\underbrace{e^a}}
   \;\;\;\;
   \text{and}
   \;\;\;\;
   \underset{deg = (1,odd)}{\underbrace{\psi^\alpha}}
$$

for $a \in \{0,1,2, \cdots, 9\}$ and $\alpha \in \{1, 2, \cdots dim_{\mathbb{R}}(N)\}$ subjects to the [[generators and relations|relations]]

$$
  \begin{aligned}
    e^a \wedge e^b = - e^b \wedge e^a
    \\
    \psi^\alpha \wedge \psi^\beta = + \psi^\beta \wedge \psi^\alpha
    \\
    e^a \wedge \psi^\alpha = - \psi^\alpha \wedge e^a
  \end{aligned}
$$

(see at _[[signs in supergeometry]]_), and the [[differential]] $d_{CE}$ acts on the generators as follows:

$$
  \begin{aligned}
    d_{\mathbb{R}^{d-1,1\vert N}} \; \psi^\alpha & 
      \coloneqq 
      0
    \\
    d_{\mathbb{R}^{d-1,1\vert N}} \; e^a 
      & \coloneqq \overline{\psi} \wedge \Gamma^a \psi
    \\
    & \coloneqq   \left(C_{\alpha \alpha'} {\Gamma^a}^{\alpha'}{}_\beta\right)  \psi^\alpha \wedge \psi^\beta
  \end{aligned}
    \,,
$$

where 

1. $\overline{\psi} \wedge \Gamma^a \psi$ denotes the $a$-component of the $Spin(d-1,1)$-invariant spinor bilinear pairing $N \otime N \to \mathbb{R}^d$ that comes with every [[real spin representation]] applied to $\psi \wedge \psi$ regarded as an $N \otimes N$-valued form;

1. hence in components (if $N$ is a [[Majorana spinor]] representation, by [this prop.](geometry+of+physics+--+supersymmetry#SpinorToVectorBilinearPairing)):

   1. $C = (C_{\alpha \alpha'})$ is the [[charge conjugation matrix]] (as discussed at _[[Majorana spinor]]_);

   1. $\Gamma^a = ((\Gamma^a)^{\alpha}{}_\beta)$ are the [[matrices]] representing the [[Clifford algebra]] action on $N$ in the [[linear basis]] $\{\psi^\alpha\}_{\alpha = 1}^{dim_{\mathbb{R}}(N)}$

1. [[Einstein summation convention|summation over paired indices]] is understood.

That this indeed yields a [[super Lie algebra]] follows by the symmetry and equivariance of the bilinear spinor pairing (via [this prop.](geometry+of+physics+--+supersymmetry#SpinorToVectorPairing)).

There is a canonical [[Lie algebra action]] of the [[special orthogonal Lie algebra]] 

$$
  Lie(Spin(d-1,1)) \simeq \mathfrak{so}(d-1,1)
$$

on $\mathbb{R}^{d-1,1\vert 1}$. The _$N$-supersymmetric [[super Poincaré Lie algebra]] $\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})$ in dimension $d$_ is the [[super Lie algebra]] which is the [[semidirect product Lie algebra]] of this [[Lie algebra action]]

$$
  \mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})
   =
  \mathbb{R}^{d-1,1\vert N} \rtimes \mathfrak{so}(d-1,1)
  \,.
$$

This is characterized by the fact that its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N}))$
is as follows: 

it is [[generators and relations|generated]] from elements 

$$
   \underset{deg = (1,even)}{\underbrace{e^a}}
   \;\;\;\;
   and
   \;\;\;\;
   \underset{deg = (1,odd)}{\underbrace{\psi^\alpha}}
   \;\;\;\;
   and
   \;\;\;\;
   \underset{deg = (1,even)}{\underbrace{\omega^{a b} = - \omega^{b a}}}
$$

with the [[super vielbein]] $(e^a, \psi^\alpha)$ as before, and with $\omega^{a b}$ the 
[[dual basis]] of the induced [[linear basis]] for vectro space of skew-symmetric matricces 
underlying the [[special orthogonal Lie algebra]]. The commutation relations are as before, 
together with the relation that the generators $\omega^{a b}$ anti-commute with every generator.
Finally the [[differential]] $d_{\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})}$ acts on 
these generators as follows:

$$
  \begin{aligned}
    d_{\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})} \; \psi^\alpha
      & \coloneqq
      \left(\tfrac{1}{4}\omega^{a b} \Gamma_{a b} \psi \right)^\alpha
      \\
      & \coloneqq
      \left(\tfrac{1}{4} (\Gamma_{a b})^\alpha{}_{\beta} \right) \omega^{a b} \wedge \psi^\beta
    \\
    d_{\mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})} \; e^a
      & \coloneqq \overline{\psi} \wedge \Gamma^a \psi - \omega^a{}_b \wedge e^b
    \\
    & \coloneqq
       \left(
           C_{\alpha \alpha'} {\Gamma^a}^{\alpha'}{}_\beta
       \right)
       \psi^\alpha \wedge \psi^\beta - \omega^a{}_b \wedge e^b
    \\
  \end{aligned}
    \,,
$$


where we are shifting spacetime indicices with the Lorentz metric

$$
  (\eta_{a b}) \coloneqq diag(-1,1,1,\cdots, 1)
  \,.
$$

The canonical maps between these [[super Lie algebras]], dually between their [[Chevalley-Eilenberg algebras]], that send each generator to itself, if present, or to zero if not, constitute the [[diagram]]

$$
  \array{
    \mathbb{R}^{d-1,1\vert N}
      &\hookrightarrow&
    \mathfrak{iso}(\mathbb{R}^{d-1,1\vert N})
    \\
    && \downarrow
    \\
    && \mathfrak{so}(d-1,1)
  }
  \,.
$$

=--




## Properties

### Classification
 {#Classification}

We discuss the classification of possible supersymmetry super Lie algebras.

1. _[Super-Poincar&#233; symmetry](#ClassificationSuperPoincareSymmetry)_

1. _[Superconformal and super AdS symmetry](#ClassificationSuperconformal)_

#### Super-Poincar&#233; symmetry
 {#ClassificationSuperPoincareSymmetry}

[[super Poincaré Lie algebras]] exist for every [real spinor representation](spin+representation#RealIrreducibleSpinRepresentationInLorentzSignature). See there for more. These come naturally equipped with a symmetric equivariant bilinear pairing of two spinors to a vector, and this constitutes the odd-odd bracket in the super Poincar&#233; Lie algebra.

The classification of minimal real spin representations in Lorentzian signature is as follows

[[!include real irreducible spin representations -- table]]


#### Superconformal and super anti de Sitter symmetry
 {#ClassificationSuperconformal}

We discuss [[super Lie algebra]] [[Lie algebra extension|extensions]] of the [[conformal group|conformal Lie algebra]] of $\mathbb{R}^{d-1,1}$ (equivalently the [[isometry]] Lie algebra of [[anti de Sitter space]] of dimension $d+1$, see also at _[[AdS-CFT]]_.)

##### In dimension 2
 {#ClassificationSuperconformalInDim2}

Discussion of classification of [[2d SCFT]] algebras includes ([Kac 03, section 2](#Kac03)).

(...)

##### In dimension $d \gt 2$
 {#ClassificationSuperconformalInDimgt2}

+-- {: .num_prop #SuperconformalLieAlgebras}
###### Proposition

There exist [[superconformal]] extensions of the [[super Poincaré Lie algebra]], (besides dimension $\leq 2$) in [[dimensions]] 3,4,5,6 as follows (with notation as at _[super Lie algebra -- classification](super%20Lie%20algebra#Classification)_):

[[!include superconformal symmetry -- table]]

There exists no [[superconformal]] extension of the [[super Poincaré Lie algebra]] in [[dimension]] $d \gt 6$.

=--

This is due to ([Shnider 88](#Shnider88)), see also ([Nahm 78](#Nahm78)). Review is in ([Minwalla 98, section 4.2](#Minwalla98)). See also the references at _[super p-brane -- As part of the AdS-CFT correspondence](Green-Schwarz+action+functional#AsPartOfTheAdSCFTCorrespodence)_.



+-- {: .proof #ProofOfClassificationOfSuperconformal}
###### Proof (sketch)

By realizing the conformal real Lie algebra $\mathfrak{so}(\mathbb{R}^{d,2})$ as a real section of the complexified $\mathfrak{so}(\mathbb{C}^{d+2})$ one is reduced to finding those (finite dimensional) simple super Lie algebras over the complex numbers whose even-graded part extends $\mathfrak{so}(\mathbb{C}^{d+2})$ and such that the implied [[representation]] of that on the odd-graded part contains the [[spin representation]].

The complex finite dimensional simple super Lie algebras have been classified, see at _[super Lie algebra -- Classification](super+Lie+algebra#Classification)_. By the tables shown there

| $\mathfrak{g}$ |  $\mathfrak{g}_{even}$  |  $\mathfrak{g}_{even}$ rep on $\mathfrak{g}_{odd}$ |
|----------------|-------------------------|------------------|
| $B(m,n)$  | $B_m \oplus C_n$  | vector $\otimes$ vector |
| $D(m,n)$  | $D_m \oplus C_n$  | vector $\otimes$ vector |
| $D(2,1,\alpha)$ |  $A_1 \oplus A_1 \oplus A_1$ | vector $\otimes$ vector $\otimes$ vector |
| $F(4)$ | $B_3\otimes A_1$ | spinor $\otimes$ vector |
| $G(3)$ | $G_2\oplus A_1$ | spinor $\otimes$ vector |
| $Q(n)$ | $A_n$ | adjoint |

| $\mathfrak{g}$ |  $\mathfrak{g}_{even}$  |  $\mathfrak{g}_{even}$ rep on $\mathfrak{g}_{{-1}}$ |
|----------------|-------------------------|------------------|
| $A(m,n)$ |  $A_m \oplus A_n \oplus C$ | vector $\otimes$ vector $\otimes$ $\mathbb{C}$ |
| $A(m,m)$ | $A_m \oplus A_n$ | vector $\otimes$ vector |
| $C(n)$ | $\mathbb{C}_{-1} \oplus \mathbb{C}$ | vector $\otimes$ $\mathbb{C}$ | 


the only manifest spinor representation of $\mathfrak{so}(2k+1) = B_k$ or of $\mathfrak{so}(2k) = D_k$ appears in the exceptional super Lie algebra $F(4)$, which contains $B_3 = \mathfrak{so}(7)$ in its even parts acting spinorially on its odd part. This hence gives a superconformal super Lie algebra in dimension $7-2 = 5$, as shown in the proposition.

But other spinor representations may still disguise as vector representations of other Lie algebras under one of the [exceptional isomorphisms](spin%20group#ExceptionalIsomorphisms). These exist only in low dimensions, and hence to conclude the proof it is sufficient to just list all candidates.

First there is the exceptional isomorphism

$$
  \mathfrak{so}(5) \simeq \mathfrak{sp}(2) = C_2
$$

with the spinor representation of $\mathfrak{so}(5)$ being the vector representation of $\mathfrak{sp}(2) = C_2$. This we find in the above tables as a summand in the even-graded subalgebra of $B(m,2)$ and of $D(m,2)$. Hence these are superconformal super Lie algebras in dimension $5-2 = 3$, as shown in the statement.

The other exceptional isomorphism of relevance is

$$
  \mathfrak{so}(6)\simeq \mathfrak{su}(4) = A_3
$$

with the spinor representation of $\mathfrak{so}(6)$ being the vector representation of $\mathfrak{su}(4) = A_3$. By the above tables this appears as a summand in the even-graded subalgebra of the super Lie algebra $A(3,k)$, and so this is the superconformal algebra in dimension $6-2 = 4$.

Finally by [[triality]] the vector representation of $\mathfrak{so}(8) = D_4$ is isomorphic to its spinor representation. By the above tables this means that $D(4,k)$ is a superconformal algebra in dimension $8-2 = 6$. For details on this see ([Shnider 88, last paragraphs](#Shnider88))


=--


+-- {: .num_remark }
###### Remark

Further constraints follow from requiring [[super-unitary representations]] ([Minwalla 98, section 4.3](#Minwalla98)). This restricts for instance the 6d superconformal algebra to $D(4,1) = \mathfrak{osp}(8|2)$ and $D(4,1) = \mathfrak{osp}(8,4)$, the latter being (over the reals as $\mathfrak{so}(8^\ast|4) = \mathfrak{osp}(6,2|4)$) the symmetry algebra of the [[6d (2,0)-superconformal QFT]] on the [[worldvolume]] of the [[M5-brane]].

=--


### Superymmetry multiplets and BPS states

* [[supermultiplet]]

* [[BPS state]]


### Extensions

In special dimensions supersymmetry super Lie algebras have [polyvector extensions](super%20Poincare%20Lie%20algebra#PolyvectorExtensions) by [[brane]] [[charges]], called for instance the _[[type II supersymmetry algebra]]_ for the case of [[type II supergravity]] or the _[[M-theory supersymmetry algebra]]_ for the case of [[11-dimensional supergravity]]. These in turn are the truncations of [[super L-infinity algebra]] extensions, related to the [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]] etc. See also at _[[extended supersymmetry]]_ and _[[extended super Minkowski spacetime]]_.


## Examples

* [[supergravity]]

* [[super Yang-Mills theory]]

  * [[N=4 D=4 super Yang-Mills theory]]

* [[spinning particle]] (which happens to have [[worldline supersymmetry]])

* [[superparticle]]

  * [[(1,1)-dimensional Euclidean field theories and K-theory]]

* [[SCFT]] 

  * [[2d SCFT]]

    * [[spinning string]] [[superstring]]

    * [[heterotic string]], [[2d (2,0)-superconformal QFT]]

    * [[type II superstring]]

    * [[(2,1)-dimensional Euclidean field theories and tmf]]

  * [[6d (2,0)-superconformal QFT]]


## Related concepts

* [[number of supersymmetries]]

* [[supermultiplet]], [[adinkra]]

* [[naturalness]]

* [[split supersymmetry]]

* [[gauge coupling unification]]

* [[supergeometry]], [[superalgebra]]
  
  * [[supermanifold]]

  * [[super Lie algebra]]

  * [[integration over supermanifolds]]

* [[supercharge]]

* [[supersymmetric cycle]]

* [[unitary representation of the super Poincaré group]]

* [[Haag–Lopuszanski–Sohnius theorem]]

* [[extended supersymmetry]]


* [[superconformal field theory]], [[2d SCFT]]

  * [[super vertex operator algebra]]

* [[hadron supersymmetry]]

* [[supergravity]], [[superstring theory]]

  * [[supersymmetry and Calabi-Yau manifolds]]

* [[MSSM]]


* [string theory FAQ -- Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)





## References

### History
 {#ReferencesHistory}

The notion of [[SU(n)]]-[[supergroup]] symmetry first appears in the proposal of [[hadron supersymmetry]] in

* [[Hironari Miyazawa]], _Baryon Number Changing Currents_, Prog. Theor. Phys. 36 (1966) 6, 1266-1276 ([spire:1235194](https://inspirehep.net/literature/1235194), [doi:10.1143/PTP.36.1266](https://doi.org/10.1143/PTP.36.1266))

* [[Hironari Miyazawa]], _Spinor Currents and Symmetries of Baryons and Mesons_, Phys. Rev. 170, 1586 (1968) ([doi:10.1103/PhysRev.170.1586](https://doi.org/10.1103/PhysRev.170.1586))
 
but was ignored (see [CGNY 19](hadron+supersymmetry#CGNY19) for historical comments).

The notion of [[super Poincaré Lie algebra|Poincaré supersymmetry]] was discovered in parallel by two groups in the early 1970s (separated and isolated at that time by "Cold War" nuisances):

On the one hand, [[André Neveu]], [[Pierre Ramond]] and [[John Schwarz]] wrote down in 1971 the [[model (in theoretical physics)|model]] originally called the _[[spinning string]]_ -- a 2-dimensional [[quantum field theory]] with [[fermions]] -- and noticed that it just so happens to have an extra graded extension of 2-dimensional Poincar&#233; symmetry. Ever since the previously baptized [[spinning string]] became known as the _[[superstring]]_ (specifically: the _[[NSR-superstring]]_):

* [[André Neveu]], [[John Schwarz]], _Factorizable dual model of pions_, Nucl. Phys. B31, 86 (1971) (<a href="https://doi.org/10.1016/0550-3213(71)90448-2">doi:10.1016/0550-3213(71)90448-2</a>)

* [[Pierre Ramond]], _Dual theory for Free Fermions_, Phys Rev. D3  2415 (1971) ([doi:10.1103/PhysRevD.3.2415](https://doi.org/10.1103/PhysRevD.3.2415))

See also at the [[string theory FAQ]]: _[Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)_


Independently, around the same time [[Yuri Golfand]] and [[Evgeny Likhtman]] in Russia wrote down the [[super Poincaré Lie algebra]] in four dimensions:

* {#GolfandLikhtman72} [[Yuri Golfand]], [[Evgeny Likhtman]], _On the Extensions of the Algebra of the Generators of the Poincaré Group by the Bispinor Generators_, in: [[Victor Ginzburg]] et al. (eds.) _I. E. Tamm Memorial Volume Problems of Theoretical Physics_, (Nauka, Moscow 1972), page 37, 

  translated and reprinted in: [[Mikhail Shifman]] (ed.) _[[The Many Faces of the Superworld]]_ pp. 44-53,  World Scientific (2000) ([doi:10.1142/9789812793850_0006](https://doi.org/10.1142/9789812793850_0006))

This then motivated [[Julius Wess]] and [[Bruno Zumino]] to study supersymmetric [[quantum field theories]] in four [[spacetime]] dimensions:

* {#WessZumino74} [[Julius Wess]], [[Bruno Zumino]], _Supergauge transformations in four dimensions_, Nucl. Phys. B70 (1974) 39; Phys. Letters 49B (1974) 52 ([doi:10.1142/9789814542340_0002](https://doi.org/10.1142/9789814542340_0002))

From this sprang the idea of [[super Yang-Mills theory]] in


* {#FerraraZumino74} [[Sergio Ferrara]], [[Bruno Zumino]], _Supergauge invariant Yang-Mills theories_, Nuclear Physics B Volume 79, Issue 3, 25 September 1974, Pages 413-421 (<a href="https://doi.org/10.1016/0550-3213(74)90559-8">doi:10.1016/0550-3213(74)90559-8</a>)

* {#SalamStrathdee74a} [[Abdus Salam]], [[John Strathdee]], _Super-symmetry and non-Abelian gauges_, Physics Letters B Volume 51, Issue 4, 19 August 1974, Pages 353-355 (<a href="https://doi.org/10.1016/0370-2693(74)90226-3">doi:10.1016/0370-2693(74)90226-3</a>)

and the early development of the concepts if [[superspace]] and [[superfields]] for [[supersymmetry|supersymmetric]] [[quantum field theory]]:

* {#SalamStrathdee74b} [[Abdus Salam]], [[John Strathdee]], _Supergauge Transformations_, Nucl.Phys. B76 (1974) 477-482 ([spire:89208](http://inspirehep.net/record/89208))

* {#SalamStrathdee75} [[Abdus Salam]], [[John Strathdee]], _Superfields and Fermi-Bose symmetry_, Physical Review D11, 1521-1535 (1975) ([doi:10.1142/9789812795915_0051](https://doi.org/10.1142/9789812795915_0051))


{#OriginOfTheTerm} On the origin of the "super"-terminology, from [Kane-Shifman 01, p. 4](#KaneShifman01):

> Often students ask where the name "super-symmetry" came  from?  It seems  that it was coined in the paper by  [Salam and Strathdee](#SalamStrathdee74a) where these  authors constructed [[supersymmetric Yang-Mills theory]].  This paper was received by the editorial office on June 6, 1974, exactly eight months after that of [Wess and Zumino](#WessZumino74).  Super-symmetry (with a hyphen) is in the title, while in the body of the paper Salam and Strathdee use both, the old version of [Wess and Zumino](#WessZumino74), "super-gauge symmetry", and the new one.  An earlier paper of [Ferrara and Zumino](#FerraraZumino74) (received by the editorial office on May 27, 1974) where the same problem of super-Yang-Mills was addressed, mentions only supergauge invariance and supergauge transformations. 

Accounts of the early history of the concept of supersymmetry:

* {#KaneShifman00} [[Gordon Kane]], [[Mikhail Shifman]], _The Supersymmetric World: The Beginnings of The Theory_, World Scientific 2000 ([doi:10.1142/4611](https://doi.org/10.1142/4611))

  * {#KaneShifman01} [[Gordon Kane]], [[Mikhail Shifman]], _Introduction to "The Supersymmetric world"_ ([arXiv:hep-ph/0102298](https://arxiv.org/abs/hep-ph/0102298)), chapter in: [Kane-Shifman 00](#KaneShifman00)

* {#Likhtman01} [[Evgeny Likhtman]], _Around SuSy 1970_, talk at "30 years of supersymmetry", Nucl.Phys.Proc.Suppl. 101 (2001) 5-14 ([arxiv:hep-ph/0101209](https://arxiv.org/abs/hep-ph/0101209))

* [[John Schwarz]], _String theory origins of supersymmetry_, Nucl. Phys. Proc. Suppl. 101 (2001) 54-61 ([arXiv:hep-th/0011078](http://arxiv.org/abs/hep-th/0011078))

* [[Pierre Ramond]], _SuSy: The Early Years (1966-1976)_, Eur. Phys. J. C (2014) 74: 2698 ([arxiv:1401.5977](https://arxiv.org/abs/1401.5977))

See also at _[supergravity -- History](supergravity#History)_.



### Textbooks and lectures
 {#ReferencesTextbooksAndLectures}

Historically the first textbook on supersymmetry was

* [[Jim Gates]], M.T. Grisaru, [[Martin Roček]], [[Warren Siegel]],  _Superspace, or One thousand and one lessons in supersymmetry_, Front.Phys. 58 (1983) 1-548 ([arXiv:hep-th/0108200](https://arxiv.org/abs/hep-th/0108200))

Further physics texts:

* Stephen P. Martin, _A Supersymmetry Primer_ ([arXiv:hep-ph/9709356](http://arxiv.org/abs/hep-ph/9709356))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 2 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

* Howard E. Haber, Laurel Stephenson Haskins, _Supersymmetric Theory and Models_ ([arXiv:1712.05926](https://arxiv.org/abs/1712.05926))

* [[Joseph Polchinski]], appendix B of _[[String theory]]_, volume II, 

* [[John Terning]], _Modern Supersymmetry_, Oxford Science Publications 

More mathematical accounts:

* {#Varadarajan04} [[Veeravalli Varadarajan]], section 3.1 of  _[[Supersymmetry for mathematicians]]: An introduction_, Courant lecture notes in mathematics, American Mathematical Society Providence, R.I 2004 ([doi:10.1090/cln/011](http://dx.doi.org/10.1090/cln/011))


* C. Carmeli, L. Caston, R. Fioresi, _Mathematical foundation of supersymmetry_, with an appendix by I. Dimitrov, EMS Series of Lectures in Mathematics (European Mathematical Society, Zurich, 2011) ([arXiv:0710.5742](https://arxiv.org/abs/0710.5742))

* {#Freed99} [[Daniel Freed]], _[[Five lectures on supersymmetry]]_, AMS (1999)

also ([Deligne-Freed 99](#DeligneFreed99)).



Discussion with an eye towards [[non-perturbative effects]] such as in [[AdS-CFT]] includes

* John Terning, _TASI-2002 Lectures: Non-perturbative Supersymmetry_ ([arXiv:hep-th/0306119](http://arxiv.org/abs/hep-th/0306119))

A fair bit of detail on supersymmetry and of [[supergravity]] with an eye towards their role in [[string theory]] is in the collection

* [[Pierre Deligne|P. Deligne]], [[Pavel Etingof|P. Etingof]], [[Dan Freed|D.S. Freed]], L. Jeffrey, [[David Kazhdan|D. Kazhdan]], J. Morgan, D.R. Morrison, [[Edward Witten|E. Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

especially in the contribution

* {#DeligneFreed99} [[Pierre Deligne]], [[Daniel Freed]], _Supersolutions_ ([arXiv:hep-th/9901094](http://arxiv.org/abs/hep-th/9901094)).

The appendix there,

* _Sign manifesto_ ([pdf](http://publications.ias.edu/sites/default/files/79_SignManifesto.pdf))

means to sort out various sign issues of relevance in [[supergeometry]] and supsersymmetric [[quantum field theory]] (see at _[[signs in supergeometry]]_.)

See also

* I. L. Buchbinder, S. M. Kuzenko, _Ideas and methods of supersymmetry and supergravity; or A walk through superspace_

* [[Antoine Van Proeyen]], _Tools for supersymmetry_ ([arXiv:hep-th/9910030](http://arxiv.org/abs/hep-th/9910030))

Discussion of the relation between [[supersymmetry and division algebras]] includes

* {#Schray96} J&#246;rg Schray, _The general classical solution of the superparticle_, Class. Quant. Grav. 13 (1996), 27&#8211;38. ([arXiv:hep-th/9407045](https://arxiv.org/abs/hep-th/9407045))

* {#BaezHuerta09} [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry I_, in R. Doran, G. Friedman and [[Jonathan Rosenberg]] (eds.), _Superstrings, Geometry, Topology, and $C*$-algebras_, Proc. Symp. Pure Math. 81, AMS, Providence, 2010, pp. 65-80 ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

and for superconformal symmetry:

* Jerzy Lukierski, Francesco Toppan, _Generalized Space-time Supersymmetries, Division Algebras and Octonionic M-theory_, Phys.Lett. B539 (2002) 266-276 ([arXiv:hep-th/0203149](https://arxiv.org/abs/hep-th/0203149))

### Classification

Results on the classification of supersymmetry [[super Lie algebras]] (including higher dimensions and conformal/de Sitter supersymmetry) includes

* {#Nahm78} [[Werner Nahm]], _[[Supersymmetries and their Representations]]_, Nucl.Phys. B135 (1978) 149 ([spire:120988](https://inspirehep.net/record/120988), <a href="https://doi.org/10.1016/0550-3213(78)90218-3">doi:10.1016/0550-3213(78)90218-3</a>)

  also in: [[Mike Duff]] (ed.), _[[The World in Eleven Dimensions]]_

* {#Shnider88} [[Steven Shnider]], _The superconformal algebra in higher dimensions_, Letters in Mathematical Physics November 1988, Volume 16, Issue 4, pp 377-383 ([doi:10.1007/BF00402046](https://doi.org/10.1007/BF00402046))

* [[Vladimir Dobrev]],  V.B. Petkova,  _All Positive Energy Unitary Irreducible Representations of Extended Conformal Supersymmetry_, Phys.Lett. B162 (1985) 127-132

* {#Minwalla98} [[Shiraz Minwalla]], _Restrictions imposed by superconformal invariance on quantum field theories_, Adv. Theor. Math. Phys. 2, 781 (1998) ([arXiv:hep-th/9712074](http://arxiv.org/abs/hep-th/9712074), [doi:10.4310/ATMP.1998.v2.n4.a4]( https://dx.doi.org/10.4310/ATMP.1998.v2.n4.a4))

* [[Riccardo D'Auria]], [[Sergio Ferrara]], M. A. Lled&#243;, [[Veeravalli Varadarajan]], _Spinor Algebras_, J.Geom.Phys. 40 (2001) 101-128 ([arXiv:hep-th/0010124](http://arxiv.org/abs/hep-th/0010124))

Review includes

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], volume 1, chapter II.2.2 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* {#Kac03} [[Victor Kac]], _Classification of supersymmetries_, Proceedings of the ICM, Beijing 2002, vol. 1, 319--344 ([arXiv:math-ph/0302016](http://arxiv.org/abs/math-ph/0302016))



* {#Duff08} [[Michael Duff]], section A of _Near-horizon brane scan revived_, Nucl. Phys. B810:193-209, 2009 ([arXiv:0804.3675](http://arxiv.org/abs/0804.3675))


For more on this see at _[[super Poincaré Lie algebra]]_.





### Supersymmetry in the standard model of particle physics

A nontechnical survey of the idea of supersymmetry in the 
[[standard model of particle physics]] including the [[hierarchy problem]] and the naturality question is in 

* [[Matthew Strassler]], _[5. Supersymmetry?](http://profmattstrassler.com/articles-and-posts/the-higgs-particle/taking-stock-of-the-higgs-jan-2013/5-supersymmetry/)_

### Supersymmetry in the standard model of cosmology

The observation that the lightest supersymmetric particle is a natural [[dark matter]] candidate goes back to 

* {#EHNOS84} [[John Ellis]],  J.S. Hagelin, Dimitri V. Nanopoulos, [[Keith Olive]], M. Srednicki  _Supersymmetric relics from the Big Bang_, Nuclear Physics B 238[2]: 453-76, 1984 ([SPIRE](http://inspirehep.net/record/191839?ln=en))

with review in 

* {#EllisOlive10} [[John Ellis]], [[Keith Olive]], _Supersymmetric Dark Matter Candidates_ ([arXiv:1001.3651](http://arxiv.org/abs/1001.3651))

Supersymmetry seems to be favored by the [[Starobinsky model of cosmic inflation]] (see there for more).


### Supersymmetry breaking

A review of [[supersymmetry breaking]] is in 

* Yael Shadmi, _Supersymmetry breaking_ ([arXiv:hep-th/0601076](http://arxiv.org/abs/hep-th/0601076)) 

A quantitative analysis showing that locally supersymmetric [[spacetime]] theories will generically not exhibit global spacetime supersymmetry is

* {#DLSW} [[Keith Dienes]], Michael Lennek, David S&#233;n&#233;chal, Vaibhav Wasnik, _Is SUSY Natural?_ NewJ.Phys.10:085003,2008 ([arXiv:0804.4718](http://arxiv.org/abs/0804.4718))
 

### Experimental searches

* [[Matt Reece]], _Supersymmetry: Where do we stand?_, talk in Barcelona, May 2013 ([pdf](https://indico.cern.ch/getFile.py/access?contribId=71&sessionId=1&resId=0&materialId=slides&confId=210555))

* {#Ellis13} [[John Ellis]], _Supersymmetric Fits after the Higgs Discovery and Implications for Model Building_ ([arXiv:1312.5426](http://arxiv.org/abs/1312.5426))

* Pran Nath, _Supersymmetry after the Higgs_ ([arXiv:1501.01679](http://arxiv.org/abs/1501.01679))

* Nathaniel Craig, _The State of Supersymmetry after Run I of the LHC_ ([arXiv:1309.0528](https://arxiv.org/abs/1309.0528))

Remembering that there is a considerable difference between global low energy supersymmetry and local higher energy supersymmetry aka [[supergravity]]:

* {#Duff04} [[Michael Duff]], _Erice lectures on "The status of local supersymmetry"_ ([arXiv:hep-th/0403160](http://arxiv.org/abs/hep-th/0403160))
 
[[!redirects supersymmetries]]
[[!redirects Supersymmetry]]]

[[!redirects supersymmetry algebra]]
[[!redirects supersymmetry algebras]]


[[!redirects local supersymmetry]]
[[!redirects global supersymmetry]]

[[!redirects local supersymmetries]]
[[!redirects global supersymmetries]]

[[!redirects supersymmetric]]

[[!redirects supersymmetric quantum field theory]]