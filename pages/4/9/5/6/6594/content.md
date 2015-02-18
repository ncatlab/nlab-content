
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Higher Cartan geometry_ is supposed to be the generalization of [[Cartan geometry]] to [[higher geometry]]; the globalized version of [[higher Klein geometry]]. 

This means that given a morphism $H \to G$ of suitably geometric [[∞-groups]] then a _higher Cartan geometry_ modeled on the [[homotopy quotient]] $G/H$ is a higher geometric space $X$ such as an [[orbifold]], [[geometric ∞-stack]], [[derived scheme]] etc. which, in some suitable sense, has its [[tangent spaces]] identified with an [[infinitesimal neighbourhood]] in $G/H$.

Just like traditional [[Cartan geometry]] (in particular in the guise of [[G-structures]]) captures a plethora of relevant kinds of geometries ([[Riemannian geometry]], [[conformal geometry]], ... [[complex geometry]], [[symplectic geometry]], ..., [[parabolic geometry]]) so higher Cartan geometry is supposed to similarly govern types of [[higher differential geometry]].

A class of examples where aspects of higher Cartan geometry may be seen to secretly underly traditional discussion is the theory of [[super p-brane sigma-models]] on [[supergravity]] [[target space|target]]-[[super-spacetimes]]. This we consider in the examples [below](#SuperBraneGeometry).

## Motivation
 {#Motivation}

1. [Pre-quantization of symplectic geometry](#MotivationPrequantizationOfSymplectic)

1. [Higher pre-quantization and Parameterized WZW terms](#MotivationDefiniteParameterizationOfWZWTerms)

1. [Interlude: Super Cartan geometry](#MotivationSuperCartanGeometry)

1. [Higher pre-quantization and Globalized WZW terms](#MotivationDefiniteGlobalizationOfWZWTerms)

1. [Geometries locally modeled on homotopy quotients](#MotivationGeometriesModerledOnHomotopyQuotients)

### Pre-quantization of symplectic geometry
 {#MotivationPrequantizationOfSymplectic}

While a [[symplectic manifold]] structure $(X,\omega)$ is an example of an ([[integrable G-structure|integrable]]) [[G-structure]], hence of a [[Cartan geometry]], in many applications [[symplectic forms]] $\omega$ are to be refined to [[circle-bundles with connection]] $\nabla$ (with [[curvature]] $F_\nabla = \omega$), a refinement known as [[prequantization]]. Notice that while two [[differential forms]] on $X$ are either [[equal]] or not, two [[principal connections]] on $X$ may be different and still [[equivalence|equivalent]]: while there is just a [[set]] and hence a [[homotopy 0-type]] of [[symplectic forms]] on $X$, there is a [[groupoid]] and hence a [[homotopy 1-type]] of [[principal connections]] on $X$. It is in this sense that the pair $(X,\nabla)$ involves [[higher geometry]], namley [[homotopy n-types]] for $n \gt 0$.

In this way the pair $(X,\nabla)$ is still clearly a geometry of sorts, but not a Cartan geometry. On the other hand, it is still similar enough to be usefully regarded form this perspective:

Just like, by the [[Darboux theorem]], every symplectic manifold has an [[atlas]] by [[charts]] [[isomorphism|isomorphic]] to $(\mathbb{R}^{2n}, \mathbf{d}p_i \wedge \mathbf{d}q^i)$, so every [[prequantum line bundle]] $\nabla$ on $X$ refining $\omega$ is [[equivalence|equivalent]] over this atlas to the $U(1)$-[[principal connection]] given by the globally defined connection for $\theta \coloneqq p_i \wedge \mathbf{d}q^i$. 

Moreover, just like the [[affine symplectic group]] is the [[stabilizer group]] of the local model $\mathbf{d}p_i \wedge \mathbf{d}q^i$ under the canonical [[Euclidean group]]-[[action]] on $\mathbb{R}^{2n}$, so the [[homotopy stabilizer group]] of $\theta$ covering this is the [[extended affine symplectic group]] which is the [[semidirect product]] of the [[Heisenberg group]] and the [[metaplectic group]]. In this sense [[metaplectic quantization]] is a pre-quantized higher analog of symplectic structure. 

While one may well reason, evidently, about pre-quantization of symplectic manifolds without a general theory of higher Cartan geometry in hand, this class of examples serves as a first blueprint for what higher Cartan geometry should be like, and points the way to its higher-degree generalizations considerd [below](#MotivationDefiniteParameterizationOfWZWTerms).

### Higher pre-quantization and Parameterized WZW terms
 {#MotivationDefiniteParameterizationOfWZWTerms}

A particularly interesting example of a pre-quantization as above is the Kac-Moody [[central extension]] of [[loop groups]] of [[compact Lie group|compact]] [[semisimple Lie group]] $G$ (see [here](loop+group#ByGeometricQuantization)). These may be understood as the [[transgression]] to [[loop space]] of a  higher-degree analog of traditional [[pre-quantization]] down on $G$: the canonical [[left invariant form|left invariant]] [[differential 3-form]] $\omega_3 = \langle-,[-,-]\rangle$ lifts to a [[circle 2-bundle with connection]] $\nabla^G$. This is also called the _[[WZW gerbe]]_ or _WZW term_, as its [[volume holonomy]] serves as the [[gauge interaction]] [[action functional]] for the [[Wess-Zumino-Witten sigma model]] with [[target space]] $G$.

Since the 2-connections on $G$ form a [[2-groupoid]] hence a [[homotopy 2-type]], the pair $(G,\nabla^G)$ may be regarded as being an object in yet a bit higher differential geometry.

Now given a $G$-[[principal bundle]] $P\to X$, then a natural question is whether there is a _definite parameterization_ of $\nabla^G$ to a 2-form connection on $P$ which restricts fiberwise to $\nabla^G$ in a suitable sense up to [[gauge transformation]]. Such _[[parameterized WZW terms]]_ play a key role in [[heterotic string theory]] and [[equivariant elliptic cohomology]].

One finds that such definite parameterizations are equivalent to [[lift of structure group|lifts of structure group]] of the bundle from $G$ to the [[homotopy stabilizer group]] of $\nabla^G$ under the right $G$-action on itself, and this turns out to be the [[string 2-group]] $String(G)$. 

While this class of examples is not yet Cartan geometry proper (higher or not) since the bundle here is not a [[tangent bundle]], it contains in it the key aspect of definitie parameterizations of higher pre-quantized forms related to higher [[G-structures]]. Such definite parameterizations turn out to be part of genuine examples of higher Cartan geometry, to which we turn [below](#MotivationDefiniteGlobalizationOfWZWTerms) and key ingredients of higher Cartan geometry apply to both cases.

More generally, one considers this situation for WZW terms on [[coset spaces]] $G/H$ (the _[[gauged WZW model]]_), and their definite parameterization over $G/H$-[[fiber bundles]]. 

### Interlude: Super-Cartan geometry
 {#MotivationSuperCartanGeometry}

Before further motiviating ever higher Cartan geometry, it serves to pause and realize that while passing from manifolds to [[stacks]], we are in particular first of all generalizing to [[sheaves]]. So even before going higher in homotopy degree, one may ask how much of Cartan geometry may be formulated in [[sheaf toposes]] over [[sites]] other than that of [[smooth manifolds]]. 

One key example for this is [[supergeometry]]. Where a major application of traditonal Cartan geometry is its restriction to [[orthogonal structures]] encoding ([[pseudo-Riemannian geometry|pseudo]]-)[[Riemannian geometry]] of particular relevance in the theory of [[gravity]], the analogous orthogonal structures in [[supergeometry]] serve to set up the theory of [[supergravity]]. Indeed, all the traditional literature on supergravity is phrased in terms of [[Cartan connections]] for the inclusion of the [[Lorentz group]] into the [[super Poincaré group]], this being the formalization of what physicists mean when saying that they pass to "local supersymmetry".

It so happens that from within such super-Cartan geoemtry there appear some of the most interesting examples of what should be higher Cartan geometry, hence _higher super-Cartan geometry_. This we turn to [below](#MotivationDefiniteGlobalizationOfWZWTerms).

### Higher pre-quantization and Globalized WZW terms
 {#MotivationDefiniteGlobalizationOfWZWTerms}

Given a [[vector space]] $V$ equipped with a (constant, i.e. translationally [[left invariant form|left invariant]]) [[differential n-form|differential (p+2)-form]]

$$
  \phi \in \Omega^{p+2}(V)
$$

a natural question to ask is for a $V$-manifold $X$ (i.e. an $n$-dimensional manifold if $V \simeq \mathbb{R}^n$) to carry a differential form

$$
  \omega \in \Omega^2(X)
$$

which is a [[definite form]], definite on $\phi$, in that its restriction to each [[tangent space]] is equal, up to a $GL(V)$-transformation, to $\phi$.

Standard theory of [[G-structures]] easily shows that such definite forms correspond to $Stab_{GL(V)}(\phi)$-structures on $X$, for $Stab_{GL(V)}(\phi)$ the [[stabilizer group]] of $\phi$ under the canonical $GL(V)$-[[action]] (by [[pullback of differential forms]]).

For instance if $V = \mathbb{R}^7$ and $\phi \in \Omega^3(V)$ is the [[associative 3-form]], then $Stab_{GL(V)}(\phi) = G_2$ is the [[exceptional Lie group]] [[G2]] and this yields [[G2-structures]]. 


But in view of the [above](#MotivationDefiniteParameterizationOfWZWTerms) discussion one is led to re-state this question for the case that $\phi$ is refined to a [[prequantum n-bundle|prequantum (p+1)-bundle]] $\nabla$. A _definite globalization_ of this over a $V$-manifold $X$ should be a [[circle n-bundle with connection|circle (p+1)-connection]] on $X$ which suitably, up to the relavant [[higher gauge transformations]], restrics locally to $\nabla$.

This problem indeed appears in the formulation of [[super p-brane sigma models]] on [[target space|target]] [[super-spacetimes]]. Here $V$ is a [[super Minkowski spacetime]], $\phi$ is an exceptional [[super Lie algebra]] [[Lie algebra cohomology|cocycle]] of degree $(p+2)$ and the formulation of the [[Green-Schwarz sigma model]] requires that it is refined (higher pre-qauntized) to a higher WZW term, a $p$-form connection. The [[supergravity]] [[equations of motion]] imply a [[definite globalization]] $\omega$ of $\phi$ of a [[super-spacetime]], but to globally define the GS-WZW model one hence needs to lift this globalization to a $(p+1)$-connection, too (thereby "canceling the [[classical anomaly]]" of the model).

These definite globalizations are in particular definite parameterizations, as above, of the restriction of the higher WZW term to the [[infinitesimal disk]]-bundle of spacetime, and hence they imply higher $G$-structure along the above lines. 

It is here that developing a theory of higher Cartan geometry has real potential, since, while the globalizations of the forms $\phi$ have been extensively studied in the literature, the globalization of their pre-quantized refinement to higher WZW-terms has traditionally received almost no attention yet. A brief mentioning of the necessity of considering appears for instance in ([Witten 86, p. 17](#Witten86)), but traditional tools do get one very far in this question.
 
More precisely, this is the situation for all those [[branes]] in the old [[brane scan]] which have no tensor-multiplets on the [[worldvolume]], equivalently those on which no other branes may end (such as the [[string]] or the [[M2-brane]], but not the [[D-branes]] and not the [[M5-brane]]). For more general branes, it turns out that the target space itself is a higher geoemtric space. This leads us to higher Cartan geometry proper:

### Geometries locally modeled on homotopy quotients
 {#MotivationGeometriesModerledOnHomotopyQuotients}

More generally, the local model WZW term in question is itself already defined on a [[2-group]] $G$ or a [[homotopy quotient]] $G/H$. This happens for the [[D-brane]] and the [[M5-brane]] sigma models. 

Now to speak of definite globalizations first of all means that the space $X$ itself is a stacky higher space, locally equivalent to $G/H$.

This is the case of relevance in what is thought to be the case of super $p$-brane sigma models on supgergravity targets form which all the other are thought to descent: the [[M5-brane]] on an [[11-dimensional supergravity]] target locally modeled on an [[extended super Minkowski spacetime]], a [[homotopy quotient]] of the [[supergravity Lie 3-algebra]]. One sees that this is the situation which the physics textbook ([Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre91)) is secretly grappling with in terms of local differential form data (see at [[D'Auria-Fré formulation of supergravity]]).

In these classes of example all possible ingredients of higher Cartan geometry appear. (...)

## Examples

### Super-Poincar&#233;-geometry, Super $p$-brane geometry
 {#SuperBraneGeometry}

Notice that ordinary [[gravity]] can be understood as the theory of $(O(d,1) \hookrightarrow Iso(d,1))$-[[Cartan geometry]], where $Iso(d,1)$ is the [[Poincare group]] and $O(d,1)$ the [[orthogonal group]] of [[Minkowski space]]. This is called the [[first order formulation of gravity]].

One can read the [[D'Auria-Fre formulation of supergravity]] as saying that higher dimensional [[supergravity]] is analogously given by higher Cartan supergeometry. See there and see the examples at [[higher Klein geometry]] for more on this.

## Related concepts

[[!include local and global geometry - table]]

## References

There is secretly a good bit of higher super-Cartan geometry in 

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

Mentioning of the need for higher geometric globalizations is (ever so briefly) in 

* {#Witten86} [[Edward Witten]], p. 17 of _Twistor - Like Transform in Ten-Dimensions_, Nucl. Phys. B266 (1986) 245 ([spire](http://inspirehep.net/record/214192/?ln=en))

A formalization via [[differential cohesion]] is in

* {#dcct} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Urs Schreiber]], _[[schreiber:Higher Cartan Geometry]]_, Differential geometry seminar, Charles University Prague, 2015

[[!redirects Cartan 2-geometry]]

[[!redirects ∞-Cartan connection]]
[[!redirects ∞-Cartan connections]]

[[!redirects higher Cartan connection]]
[[!redirects higher Cartan connections]]

