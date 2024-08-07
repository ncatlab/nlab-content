
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

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

_Higher Cartan geometry_ is supposed to be the generalization of [[Cartan geometry]] to [[higher geometry]]; hence the theory of [[geometric homotopy types]] ([[manifolds]], [[orbifolds]], [[Lie groupoids]], [[geometric stacks]], [[smooth groupoids]], [[smooth infinity-groupoids]], ...) which are locally modeled on [[homotopy quotients]] $G/H$ of geometric [[infinity-groups]] -- the globalized version of [[higher Klein geometry]] (see also the [survey table](#Survey) below). 

More in detail, this means that given a morphism $H \to G$ of suitably geometric [[∞-groups]] then a _higher Cartan geometry_ modeled on the [[homotopy quotient]] $G/H$ is a higher geometric space $X$ such as an [[orbifold]], [[geometric ∞-stack]], [[derived scheme]] etc. which, in some suitable sense, has its [[tangent spaces]] identified with an [[infinitesimal neighbourhood]] in $G/H$.

Just like traditional [[Cartan geometry]] (in particular in the guise of [[G-structures]]) captures a plethora of relevant kinds of geometries (([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian geometry]] ([Cartan 23](#Cartan23)), [[conformal geometry]], ... [[complex geometry]], [[symplectic geometry]], ..., [[parabolic geometry]]) so higher Cartan geometry is supposed to similarly govern types of [[higher differential geometry]].

A class of examples where aspects of higher Cartan geometry may be seen to secretly underlie traditional discussion is the theory of [[super p-brane sigma-models]] on [[supergravity]] [[target space|target]]-[[super-spacetimes]]. This we consider in the examples [below](#SuperBraneGeometry). See also at _[[super-Cartan geometry]]_.

It is therefore maybe curious to note that while [[Cartan geometry]] as originating in ([Cartan 23](#Cartan23)) drew its motivation from the mathematical formulation of the theory of [[Einstein gravity]], higher Cartan geometry is well motivated by higher dimensional [[supergravity]] such as 10d [[type II supergravity]] and [[heterotic supergravity]] as well as [[11-dimensional supergravity]].

## Motivation
 {#Motivation}

Here we informally survey motivation for higher Cartan geometry from phenomena and open problems visible in traditional geometry.

1. [Pre-quantization of symplectic geometry](#MotivationPrequantizationOfSymplectic)

1. [Higher pre-quantization and Parameterized WZW terms](#MotivationDefiniteParameterizationOfWZWTerms)

1. [Higher pre-quantization and Globalized WZW terms](#MotivationDefiniteGlobalizationOfWZWTerms)
    
   $\,$

1. [Interlude: Super Cartan geometry](#MotivationSuperCartanGeometry)

1. [Higher Cartan connections and stacky Cartan geometry](#HigherCartanConnectionsAndStackyCartanGeometries)

1. [Definite higher WZW terms on stacky Cartan geometries](#DefiniteWZWTermsOnStackyCartanGeometries)

$\,$

Alternatively, higher Cartan geometry may be motivated intrinsically simply as the result of [[synthetic geometry|synthetically]] formulating [[Cartan geometry]] in [[homotopy type theory]]. This is the way in which the _[definition below](#Definition)_ proceeds. In the _[Examples](#Examples)_ we discuss how this abstract theory indeed serves to inform the motivating phenomena listed here.

### Pre-quantization of symplectic geometry
 {#MotivationPrequantizationOfSymplectic}

While a [[symplectic manifold]] structure $(X,\omega)$ is an example of an ([[integrable G-structure|integrable]]) [[G-structure]], hence of a [[Cartan geometry]], in many applications [[symplectic forms]] $\omega$ are to be refined to [[complex line bundles]] with [[connection on a bundle|connection]], equivalently [[circle-bundles with connection]] $\mathbf{L}$ (with [[curvature]] $F_{\mathbf{L}} = \omega$), a refinement known as _[[geometric prequantization]]_. 

$$
  (X,\omega) \stackrel{pre-quantization}{\mapsto} (X,\mathbf{L})
$$

While two [[differential forms]] on $X$ are either [[equal]] or not, two [[principal connections]] on $X$ may be different and still [[equivalence|equivalent]]. The connection $\nabla$ may have non-trivial _[[automorphisms]]_, while a differential form $\omega$ does not. (Readers may be more familiar with this kind of phenomenon from the discussion of the _[[moduli stack of elliptic curves]]_.)


Hence while there is just a [[set]] and hence a [[homotopy 0-type]] of [[symplectic forms]] on $X$, there is a [[groupoid]] and hence a [[homotopy 1-type]] of [[principal connections]] on $X$. It is in this sense that the pair $(X,\nabla)$ involves [[higher geometry]], namely [[homotopy n-types]] for $n \gt 0$.

$$
  \array{
     \left\{ \omega \right\} && \left\{ \mathbf{L} \right\}
     \\
     0-type && 1-type
  }
$$

This implies notably that where $\omega$ has a [[stabilizer group]] under the [[diffeomorphism]] [[action]] on $X$ -- the [[symplectomorphism group]] --, $\mathbf{L}$ instead has a "[[homotopy stabilizer group]]", 

$$
  Stab^h_{Diff(X)}(\mathbf{L})
  =
  \left\{
    \left(
       \array{
         \phi \colon X \stackrel{\simeq}{\to} X\,,
         \\
         \eta \colon \phi^\ast \mathbf{L} \stackrel{\simeq}{\to} \mathbf{L}
       }
    \right)
  \right\}
$$

consisting of pairs of a [[diffeomorphism]] $\phi$ and an [[isomorphism]] $\phi^\ast \mathbf{L} \stackrel{\simeq}{\to} \mathbf{L}$. This is called the _[[quantomorphism group]]_.

$$
  \array{
    Stab^h_{Diff(X)}(\mathbf{L}) = QuantMorph(\mathbf{L})
    \\
    Stab_{Diff(X)}(\omega) = SymplMorph(\omega)    
  }  
$$

Hence the [[prequantum geometry]] $(X,\mathbf{L})$ is still clearly a geometry of sorts, but not a Cartan geometry. On the other hand, it is still similar enough to be usefully regarded form this perspective:

Just like, by the [[Darboux theorem]], every symplectic manifold $(X,\omega)$ has an [[atlas]] by [[charts]] [[isomorphism|isomorphic]] to a [[symplectic vector space]] 

$$
  (V \simeq \mathbb{R}^{2n}, \omega_V = \mathbf{d}p_i \wedge \mathbf{d}q^i)
  \,,
$$ 

so every [[prequantum line bundle]] $\mathbf{L}$ on $X$ refining $\omega$ is [[equivalence|equivalent]] over this atlas to the $U(1)$-[[principal connection]] given by the globally defined connection for 

$$
  \mathbf{L}_{V} \coloneqq p_i \wedge \mathbf{d}q^i
  \,.
$$ 

Moreover, just like the [[symplectic group]] $Sp(V,\omega_V)$ is the [[stabilizer group]] of $\omega_V$ under the canonical [[general linear group]]-[[action]] on $V$, so the [[homotopy stabilizer group]] of $\mathbf{L}_V$ (the part of the [[quantomorphism group]] $QuantMorph(\mathbf{L}_V)$ covering this) is the [[Mp^c]]-group, $Mp^c(V,\omega_V) = Mp(V,\omega_V)\underset{\mathbb{Z}/2\mathbb{Z}}{\times}U(1)$, the $U(1)$-version of the [[metaplectic group]] $Mp(V,\omega_V)$  , 

$$
  \array{
     && Stab^h_{GL(V)}(\mathbf{L}_V)
     \\
     && \simeq
     \\
     &&
     Mp^c(V,\omega_V) 
     &\hookrightarrow& 
     QuantMorph(V,\mathbf{L}_V)
     \\
     \downarrow && \downarrow && \downarrow
     \\
     &&
     Sp(V,\omega_V)
     &\hookrightarrow&
     SympMorph(V,\omega_V)
     \\
     && \simeq
     \\
     && Stab_{GL(V)}(\omega_V)
  }
$$

In this sense [[metaplectic quantization]] is a higher analog of symplectic geometry. 

While one may well reason, evidently, about pre-quantization of symplectic manifolds without a general theory of higher Cartan geometry in hand, this class of examples serves as a first blueprint for what higher Cartan geometry should be like, and points the way to its higher-degree generalizations considered [below](#MotivationDefiniteParameterizationOfWZWTerms).

In particular, recurring themes are 

1. [[circle n-bundles with connection]] $\mathbf{L}$ [[higher prequantization|higher prequantizing]] [[definite forms]] $\omega$;

1. their [[homotopy stabilizer groups]]/[[higher quantomorphism groups]] and the [[infinity-group extension]] they form and the higher [[G-structures]] associated with them.


### Higher pre-quantization and Parameterized WZW terms
 {#MotivationDefiniteParameterizationOfWZWTerms}

A particularly interesting example of a pre-quantization as above is the Kac-Moody [[central extension]] of [[loop groups]] of [[compact Lie group|compact]] [[semisimple Lie group]] $G$ (see [here](loop+group#ByGeometricQuantization)). 

Loop groups are naturally symplectic geometries, whose symplectic form is the [[transgression]] of the canonical [[left invariant form|left invariant]] [[differential 3-form]] $\omega_3 = \langle-,[-,-]\rangle$ on $G$:

$$
  (G, \omega_3)
  \stackrel{transgression}{\mapsto}
  (L G, \omega_2)
$$


Similarly their central extension is the [[transgression]] to [[loop space]] of a  higher-degree analog of traditional [[pre-quantization]] down on $G$: the canonical [[left invariant form|left invariant]] [[differential 3-form]] $\omega_3 = \langle-,[-,-]\rangle$ lifts to a [[circle 2-bundle with connection]] $\mathbf{L}_3$, whose [[curvature]] 3-form is $F_{\mathbf{L}_3} = \omega_3$:

$$
  (G, \mathbf{L}_3)
  \stackrel{transgression}{\mapsto}
  (L G, \mathbf{L}_2)
$$

This $\mathbf{L}_3$ is also called the _[[WZW gerbe]]_ or _WZW term_, as its [[volume holonomy]] serves as the [[gauge interaction]] [[action functional]] for the [[Wess-Zumino-Witten sigma model]] with [[target space]] $G$.


Now the 2-connections on $G$ form a [[2-groupoid]] hence a [[homotopy 2-type]], the pair $(G,\nabla^G)$ may be regarded as being an object in yet a bit higher differential geometry.

$$
  \array{
     \left\{ \omega_3 \right\} && \left\{ \mathbf{L}_3 \right\}
     \\
     0-type && 2-type
  }
$$


Now given a $G$-[[principal bundle]] 

$$
  \array{
    \mathbf{L}_3 && \mathbf{L}_3^P
    \\
    G &\stackrel{}{\longrightarrow}& P
    \\
    && \downarrow
    \\
    && X
  }
$$

then a natural question is whether there is a _[[parameterized WZW  term|definite parameterization]]_ $\mathbf{L}_3^P$ of $\mathbf{L}_3$ to a 2-form connection on $P$ which restricts fiberwise to $\nabla^G$ in a suitable sense up to [[gauge transformation]]. Such _[[parameterized WZW terms]]_ play a key role in [[heterotic string theory]] and [[equivariant elliptic cohomology]].

One finds that such [[parameterized WZW term|definite parameterizations]] are equivalent to [[lift of structure group|lifts of structure group]] of the bundle from $G$ to the [[homotopy stabilizer group]] of $\mathbf{L}_3$ under the right $G$-action on itself, and this turns out to be the [[string 2-group]] $String(G)$, which is itself the [[homotopy quotient]] of the group of based paths of $G$ by the Kac-Moody loop group of $G$. By the above we may also think of this as a [[Heisenberg 2-group]]:

$$
  Heis(\mathbf{L}_3)
  =
  Stab^h_{G}(\mathbf{L}_3)
  \simeq
  String(G)
  \simeq
  (P_\ast G) // \widehat{L G}
$$

Hence a definite parameterization of $\mathbf{L}_3$ over $P$ is a [[string structure]] on $P$. The [[obstruction]] to that is

* for $G = SU(N)$: the [[second Chern class]] $\c_2(P)$

* for $G = Spin$: the [[first fractional Pontryagin class]] $\tfrac{1}{2}p_1(P)$.

These are the obstructions famous from [[Green-Schwarz anomaly cancellation]] in [[heterotic supergravity]].


While this class of examples is not yet Cartan geometry proper (higher or not) since the bundle $P$ here is not a [[tangent bundle]], it contains in it the key aspect of [[parameterized WZW model|definite parameterizations]] of higher pre-quantized forms related to higher [[G-structures]]. Such definite parameterizations turn out to be part of genuine examples of higher Cartan geometry, to which we turn [below](#MotivationDefiniteGlobalizationOfWZWTerms) and key ingredients of higher Cartan geometry apply to both cases.

But more generally, one considers this situation for WZW terms on [[coset spaces]] $G/H$, relevant in  _[[gauged WZW model]]_. 



+-- {: goal}
#### Goal 1 of higher Cartan geometry

Provide [[obstruction]] classes for [[definite parameterizations of higher WZW terms]].

=--

This we consider [below](#ObstructionClassesForDefiniteParameterizations)



### Higher pre-quantization and Globalized WZW terms
 {#MotivationDefiniteGlobalizationOfWZWTerms}

Often one wants to consider definite parameterizations as above along the tangent bundle of a $V$-manifold $X$, such that the parameterization comes from a _global_ $\mathbf{L}$ on $X$, a [[definite globalization of a WZW term]].

Given a [[vector space]] $V$ equipped with a (constant, i.e. translationally [[left invariant form|left invariant]]) [[differential n-form|differential (p+2)-form]]

$$
  \omega_V \in \Omega^{p+2}(V)
$$

a natural question to ask is for a $V$-manifold $X$ (i.e. an $n$-dimensional manifold if $V \simeq \mathbb{R}^n$) to carry a differential form

$$
  \omega \in \Omega^2(X)
$$

which is a [[definite form]], definite on $\omega_V$, in that its restriction to each [[tangent space]] is equal, up to a $GL(V)$-transformation, to $\omega_V$.

Standard theory of [[G-structures]] easily shows that such definite forms correspond to $Stab_{GL(V)}(\omega_V)$-structures on $X$, for $Stab_{GL(V)}(\omega_V)$ the [[stabilizer group]] of $\omega_V$ under the canonical $GL(V)$-[[action]] (by [[pullback of differential forms]]).

For instance if $V = \mathbb{R}^7$ and $\omega_V \in \Omega^3(V)$ is the [[associative 3-form]], then $Stab_{GL(V)}(\omega_V) = G_2$ is the [[exceptional Lie group]] [[G₂]] and this yields [[G₂-structures]]. 


But in view of the [above](#MotivationDefiniteParameterizationOfWZWTerms) discussion one is led to re-state this question for the case that $(V,\omega_V)$ is refined to a [[prequantum n-bundle|prequantum (p+1)-bundle]] $(V,\mathbf{L}_{p+2})$. 

Just as a 1-connection is precisely the data needed to define [[holonomy|line holonomy]], so an $(p+1)$-connection is precisely the data needed to define $(p+1)$-[[volume holonomy]]

$$
  \array{
     \left\{ \omega_{p+2} \right\} && \left\{ \mathbf{L}_{p+2} \right\}
     \\
     0-type && (p+1)-type
  }
$$



A _[[definite globalization]]_ of such $\mathbf{L}_{p+2}$ over a $V$-manifold $X$ should be a [[circle n-bundle with connection|circle (p+1)-connection]] $\mathbf{L}_{p+1}^X$ on $X$ which suitably, up to the relevant [[higher gauge transformations]], restricts locally to $\mathbf{L}_V$.

For instance for first-order integrable such globalizations one would require that (in particular) for each [[infinitesimal disk]] $\mathbb{D}$ in a $V$-cover $U$ we have an [[equivalence]]

$$
  \array{
    & \mathbf{L}_{p+2}|_{|\mathbb{D}} & \simeq & \mathbf{L}_{p+2}^X|_{|\mathbb{D}}
    \\
    && \mathbb{D} 
    \\
    && \downarrow 
    \\
    && U && && 
    \\
    & \swarrow && \searrow
    \\
    V && && X
    \\
    \mathbf{L}_{p+2} && && \mathbf{L}_{p+2}^X
  }
$$

This problem indeed appears in the formulation of [[super p-brane sigma models]] on [[target space|target]] [[super-spacetimes]]. Here $V$ is a [[super Minkowski spacetime]], $\omega_V$ is an exceptional [[super Lie algebra]] [[Lie algebra cohomology|cocycle]] of degree $(p+2)$ and the formulation of the [[Green-Schwarz sigma model]] requires that it is refined (higher pre-quantized) to a higher WZW term, a $p$-form connection. The [[supergravity]] [[equations of motion]] imply a [[definite globalization]] $\omega$ of $\omega_V$ of a [[super-spacetime]], but to globally define the GS-WZW model one hence needs to lift this globalization to a $(p+1)$-connection, too (thereby "canceling the [[classical anomaly]]" of the model).

These [[definite globalizations]] are in particular [[parameterized WZW term|definite parameterizations]], as above, of the restriction of the higher WZW term to the [[infinitesimal disk]]-bundle of spacetime, 

$$
  \array{
     \mathbf{L}_{p+2}|_{|\mathbb{D}} && \mathbf{L}_{p+2}^X|_{T_{inf}X}
     \\
     \mathbb{D} & \longrightarrow& T_{inf}X
     \\
     && \downarrow
     \\
     && X
  }
$$

Notice that for the [[infinitesimal disk]] every [[diffeomorphism]] is a [[linear transformation]], hence

$$
  Aut(\mathbb{D}) \simeq GL(V)
$$

and therefore by the above a definite globalization determines a [[G-structure]] for $G = Stab^h_{GL(V)}(\mathbf{L}_{p+2})$. Conversely, the [[obstruction]] to such a structure is an obstruction to a definite globalization.

This construction extends to [[forgetful functor]] (an [[(infinity,1)-functor]])

$$
  \left\{
    \array{
       definite \; globalizations \; \mathbf{L}_{p+2}^X
       \\
       of\; \mathbf{L}_{p+2} \; over \; X
    }
  \right\}
  \longrightarrow
  \left\{
     \array{
        Stab^h_{GL(V)}(\mathbf{L}_{p+2}|_{\mathbb{D}})-structures
        \\
        on \; X
     }
  \right\}
  \,.
$$

(For instance in the case of applications to [[supergravity]] that we turn to [below](#MotivationSuperCartanGeometry), these structures are extensions of strutures given by solutions to the super-[[Einstein equations]].

It is here that developing a theory of higher Cartan geometry has much potential, since, while the globalizations of the forms $\omega_V$ have been extensively studied in the literature, the globalization of their pre-quantized refinement to higher WZW-terms $\mathbf{L}_{p+2}$ has traditionally received almost no attention yet. A brief mentioning of the necessity of considering appears for instance in ([Witten 86, p. 17](#Witten86)), but traditional tools do get one very far in this question.

More precisely, this is the situation for all those [[branes]] in the old [[brane scan]] which have no tensor-multiplets on the [[worldvolume]], equivalently those on which no other branes may end (such as the [[string]] or the [[M2-brane]], but not the [[D-branes]] and not the [[M5-brane]]). For more general branes, it turns out that the target space itself is a higher geometric space. This leads us to higher Cartan geometry proper. This we turn to [below](#MotivationSuperCartanGeometry).)


Accordingly, now the symmetries of $\mathbf{L}_{p+2}^X$ form an extension of the _[[isometries]]_ of the induced $Stab^h_{GL(V)}(\mathbf{L}_{p+2}|_{\mathbb{D}})$-structure.

$$
  (\mathbf{B}^p U(1))FlatConn(X)
  \longrightarrow
  Stab^h_{Diff(X)}(\mathbf{L}_{p+2}^X)
  \longrightarrow
  Isom(X)
$$

One finds that after [[Lie differentiation]] these extensions are of the kind konwn in the phyiscs literature as [[BPS charge]] extensions.

+-- {: goal}
### Goal 2 of higher Cartan geometry

Classify these refined and generalized [[BPS states]].

=--

This we turn to [below](#HigherExtended IsometryGroups).

So far these examples point to higher Cartan geometry modeled on homomorphisms

$$
  Stab^h_{GL(V)}(\mathbf{L}_{p+2})
  \longrightarrow
  V \rtimes Stab^h_{GL(V)}(\mathbf{L}_{p+2})
$$

where the [[homotopy stabilizer group]] $Stab^h_{GL(V)}(\mathbf{L}_{p+2})$ is a [[infinity-group]], but where $V$ is still an ordinary manifold. We now turn ([below](#HigherCartanConnectionsAndStackyCartanGeometries)) to examples that also turn the local model space $V$ into an higher [[geometric homotopy type]]. But first we need a little [interlude](#MotivationSuperCartanGeometry).



### Interlude: Super-Cartan geometry
 {#MotivationSuperCartanGeometry}

Before further motivating ever higher Cartan geometry, it serves to pause and realize that while passing from manifolds to [[stacks]], we are in particular first of all generalizing to [[sheaves]]. So even before going higher in homotopy degree, one may ask how much of Cartan geometry may be formulated in [[sheaf toposes]], first over the [[site]] of [[smooth manifolds]] itself, which leads to Cartan geometry in the generality of [[smooth spaces]], and next over [[sites]] other than that of [[smooth manifolds]] -- _[[super-Cartan geometry]]_.

One key example for this is [[supergeometry]]. Where a major application of traditional Cartan geometry is its restriction to [[orthogonal structures]] encoding ([[pseudo-Riemannian geometry|pseudo]]-)[[Riemannian geometry]] of particular relevance in the theory of [[gravity]], the analogous orthogonal structures in [[supergeometry]] serve to set up the theory of [[supergravity]].

More in detail, after picking a [[dimension]] $d\in \mathbb{N}$ and writing $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ for the [[Poincaré Lie algebra]], then a choice of "number of supersymmetries" is a choice of [real spin representation](spin+representation#RealIrreducibleSpinRepresentationInLorentzSignature) $N$. Then the [[direct sum]] 

$$
  \mathfrak{Iso}(\mathbb{R}^{d-1,1|N})
  \coloneqq
  \underbrace{\mathfrak{Iso}(\mathbb{R}^{d-1,1})}_{even} \oplus \underbrace{N}_{odd}
$$

regarded as a [[super vector space]] with $N$ in odd degree becomes a [[super Lie algebra]] by letting the $[even,odd]$ bracket to be given by the defining [[action]] and by letting the $[odd,odd]$ bracket be given by a canonically induced bilinear and $\mathfrak{o}$-equivariant pairing -- the [[super Poincaré Lie algebra]]. This still canonical contains the [[Lorentz Lie algebra]] $\mathfrak{o}(\mathbb{R}^{d-1,1})$ and the [[quotient]]

$$
  \mathbb{R}^{d-1,1|N} 
  \coloneqq
  \mathfrak{Iso}(\mathbb{R}^{d-1,1|N})/\mathfrak{o}(\mathbb{R}^{d-1,1})
$$

is called [[super Minkowski spacetime]] (equipped with its [[super translation Lie algebra]] structure).

From this, a [[super-Cartan geometry]] is defined in direct analogy to the Cartan formulation of Riemannian geometry


| [[Cartan geometry]] | $\mathfrak{g}$ | $\mathfrak{h}$ | $\mathfrak{g}/\mathfrak{h}$ |
|---------------------|----------------|----------------|-----------------------------|
| [[pseudo-Riemannian geometry]]/[[Einstein gravity]]  | $\mathfrak{Iso}(\mathbb{R}^{d-1,1})$ | $\mathfrak{o}(d-1,1)$ | $\mathbb{R}^{d-1,1}$ |
| [[supergravity]] | $\mathfrak{Iso}(\mathbb{R}^{d-1,1\vert N})$ | $\mathfrak{o}(d-1,1)$ | $\mathbb{R}^{d-1,1\vert N}$ |


Indeed, all the traditional literature on supergravity (e.g. ([Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre91))) is phrased, more or less explicitly, in terms of [[Cartan connections]] for the inclusion of the [[Lorentz group]] into the [[super Poincaré group]], this being the formalization of what physicists mean when saying that they pass to "local supersymmetry".

It so happens that from within such super-Cartan geometry there appear some of the most interesting examples of what should be higher Cartan geometry, hence _higher super-Cartan geometry_. This we turn to [below](#MotivationDefiniteGlobalizationOfWZWTerms).




### Higher Cartan connections and Stacky Cartan geometries
 {#HigherCartanConnectionsAndStackyCartanGeometries}

A traditional [[Cartan connection]], being a [[principal connection]] satisfying some extra conditions, is locally (on some [[chart]] $U \to X$) in particular a [[Lie algebra valued differential form]] $A \in \Omega^1(U,\mathfrak{g})$. Following Cartan, this is equivalently a [[homomorphism]] of [[dg-algebras]] of the form

$$
  \Omega^\bullet(U) \longleftarrow W(\mathfrak{g}) \colon A
$$

from the [[Weil algebra]] of the [[Lie algebra]] $\mathfrak{g}$ to the [[de Rham complex]] of $U$, equivalently a homomorphism of just [[graded algebras]]

$$
  \Omega^\bullet(U) \longleftarrow CE(\mathfrak{g}) \colon A
$$

from the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$. (Requiring this second morphism to also respect the dg-algebra structure, hence the differential, is equivalent to requiring the [[curvature]] form $F_A$ to vanish, hence to the connection being a [[flat connection]]).

In particular for the description of [[supergravity]] [[superspacetimes]] one considers this for $\mathfrak{g} = \mathfrak{Iso}(\mathbb{R}^{d-1,1|N})$ the [[super Poincaré Lie algebra]] of some [[super Minkowski spacetime]] $\mathbb{R}^{d-1|N}$. This serves to encode a [[Levi-Civita connection]] as for ordinary [[gravity]] modeled by ordinary [[orthogonal structure]] [[Cartan geometry]], together with the [[gravitino]] field.

In detail, the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{Iso}(\mathbb{R}^{10,1|N=1}))$ for 11-dimensional [[Minkowski spacetime]] turned super via the unique irreducible 32-dimensional [[spin representation]] (see [here](spin+representation#RealIrreducibleSpinRepresentationInLorentzSignature)) is freely generated as a [[graded commutative algebra|graded commutative]] [[superalgebra]] on 

* elements $\{e^a\}_{a = 1}^{11}$ and $\{\omega^{ a b}\}$ of degree $(1,even)$;

* and elements $\{\psi^\alpha\}_{\alpha = 1}^{32}$ of degree $(1,odd)$

and as a [[differential graded algebra]] its [[differential]] $d_{CE}$ is determined by the equations

$$
  d_{CE} \, \omega^{a b} = \omega^a{}_b \wedge \omega^{b c}
$$

$$
  d_{CE} \, e^{a } = \omega^a{}_b \wedge e^b + \frac{i}{2}\bar \psi \Gamma^a \psi
  \,.
$$

An algebra homomorphism as above sends these generators to differential forms of the corresponding degree, the [[vielbein]]

$$
  E^a \coloneqq A(e^a) \in \Omega^{(1,even)}(U)
  \,,
$$

whe [[spin connection]]

$$
  \Omega^{a}{}_{b} \coloneqq A(\omega^a{}_b) \in \Omega^{(1,even)}(U)
$$

and the [[gravitino]]

$$
  \Psi^\alpha \coloneqq A(\psi^\alpha) \in \Omega^{(1,odd)}(U)
  \,.
$$

But a key aspect of higher dimensional [[supergravity]] theories is that their [[field (physics)|field]] content necessarily includes, in addition to the [[graviton]] and the [[gravitino]], higher [[differential n-form]] fields, notably the 2-fom [[B-field]] of 10-dimensional [[type II supergravity]] and [[heterotic supergravity]] as well as the 3-form [[C-field]] of [[11-dimensional supergravity]].

This means that these higher dimensional supergravity theories are not in fact entirely described  by super-[[Cartan geometry]]. This is to be contrasted with the fact that the very motivation for Cartan geometry, in the original article ([Cartan 23](#Cartan23)), was the mathematical formulation of the [[theory (physics)|theory]] of [[gravity]] ([[general relativity]]).

Now a key insight due to ([D'Auria-Fr&#233;-Regge 80](#DAuriaFreRegge80), [D'Auria-Fr&#233; 82](#DAuriaFre82)) was that the "tensor multiplet" fields of higher dimensional supergravity theories as above are naturally brought into the previous perspective if only one allows more general [[Chevalley-Eilenberg algebras]]. 

Namely, we may add to the above CE-algabra

* a single generator $c_3$ of degree $(3,even)$ 

and extend the differential to that by the formula

$$
  d_{CE} \, c_3 = \frac{1}{2}\bar \psi \Gamma^{a b} \wedge \psi \wedge e_a \wedge e_b
  \,.
$$

This still squares to zero due to the remarkable property of 11d [[super Minkowski spacetime]] by which $\frac{1}{2}\bar \psi \Gamma^{a b} \wedge \psi \wedge e_a \wedge e_b \in CE^4(\mathfrak{Iso}(10,1|N=1))$ is a representative of an exception [[super Lie algebra|super]]-[[Lie algebra cohomology]] class. (The collection of all these exceptional classes constitutes what is known as the _[[brane scan]]_).

In the textbook ([Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre91)) a beautiful algorithm for constructing and handling higher supergravity theories based on such generalized CE-algebras is presented, but it seems fair to say that the authors struggle a bit with the right mathematical perspective to describe what is really happening here.

But from a modern perspective this becomes crystal clear: these generalized CE algebras are CE-algebras not of [[Lie algebras]] but of [[strong homotopy Lie algebra]], hence of [[L-infinity algebras]], in fact of [[Lie n-algebras|Lie (p+1)-algebras]] for $(p+1)$ the degree of the relevant differential form field. 

Specifically, we may write the above generalized CE-algebra with the extra degree-3 generator $c_3$ as the CE-algebra $CE(\mathfrak{m}2\mathfrak{brane}) $

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

This means that a global description of the geometry which ([Castellani-D'Auria-Fr&#233; 91](#CastellaniDAuriaFre91)) discuss locally on [[charts]] has to be a higher kind of Cartan geometry which is locally modeled not just on [[cosets]], but on the [[homotopy quotients]] of ([[smooth infinity-group|smooth]], [[smooth super infinity-groupoid|supergeometric]], ...) [[infinity-groups]].

### Definite higher WZW terms on stacky Cartan geometries
 {#DefiniteWZWTermsOnStackyCartanGeometries}

Once such a higher Cartan super-spacetime $X$ as [above](#HigherCartanConnectionsAndStackyCartanGeometries) has been obtained, then we are back to the [above](#MotivationDefiniteGlobalizationOfWZWTerms) question of constructing [[definite globalizations of WZW terms]] over it.

Indeed, the [[super p-brane sigma-models]] of the [[D-branes]] and the [[M5-brane]] have [[WZW terms]] defined not on plain [[super Minkowski spacetimes]], but on the above [[extended super Minkowski spacetimes]].  For instance the WZW term of the [[M5-brane]] sigma model is a [[higher prequantization]] of the following 7-form  ([D'Auria-Fr&#233; 82](#DAuriaFre82))

$$
  \omega_7 
  \;\coloneqq\;
  \frac{1}{2} \bar \psi \wedge \Gamma^{a_1 \cdots a_5} \psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_5}
   +
  \frac{13}{2} \bar \psi \Gamma^{a_1 a_2} \psi \wedge e_{a_1} \wedge e_{a_2} \wedge c_3
 \;\;\;
 \in 
  CE^7(\widehat{\mathbb{R}}^{10,1|N=1})
$$

on the above [[extended super Minkowski spacetime]], where $c_3$ is the extra degree-3 generator discussed above.

Under [[Lie integration]] this becomes ([FSS 13](#FSS13)) a degree-7 WZW term defined on a [[smooth super infinity-groupoid|supergeometric 3-group]] $G/H$ and defining the M5-brane sigma model on a curved supergravity target space means to construct [[definite globalizations]] of this over higher Cartan geometries $X$ modeled on this [[homotopy quotient]] $G/H$.

The result $(X,\mathbf{L}^X_7)$ is a pair which is still analogous to the [[symplectic geometry|symplectic geometries]] that we started with, but is now in higher geometric homotopy theory in every possible sense.

Computing for this case the higher extensions of isometries as [above](#MotivationDefiniteGlobalizationOfWZWTerms), one finds ([dcct, sections 1.2.11.3 and 1.2.15.3.3](#dcct)) the [[quantomorphism n-group]]
for the [[smooth super infinity-groupoid|supergeometric 7-group]] with is the [[Lie integration]] of the [[M-theory Lie algebra]] of $X$, witnessing the degree of $X$ being a "[[BPS state]]" of 11d supergravity. These BPS states are known to be an immensely rich mathematical topic (e.g. via their "[[wall crossing]] phenomena"), but one sees here that it is but the local and infinitesimal shadow of a much richer structure: higher isometries in higher super-Cartan geometry. 

In terms of the physics this refinement corresponds to [[classical anomaly]]-cancellation of [[super p-brane sigma models]], a problem that is by and large open.

+-- {: goal}
#### Goal 3 of higher Cartan geometry

Provide [[classical anomaly]] cancellation for [[super p-brane sigma-models]] such as the [[M5-brane]].

=--



## Definition
 {#Definition}

(...)

see at _[[differential cohesion]]_ the section _[structures](differential+cohesive+%28infinity%2C1%29-topos#structures)_.

(...)

## Properties

### Obstruction theorems
 {#ObstructionClassesForDefiniteParameterizations}

(...)

### Higher extended isometry groups (BPS)
 {#HigherExtended IsometryGroups}


(...)

## Examples
 {#Examples}

### Survey 
 {#Survey}

[[!include local and global geometry - table]]

### Super-Poincar&#233;-geometry, Super $p$-brane geometry
 {#SuperBraneGeometry}

Notice that ordinary [[gravity]] can be understood as the theory of $(O(d,1) \hookrightarrow Iso(d,1))$-[[Cartan geometry]], where $Iso(d,1)$ is the [[Poincare group]] and $O(d,1)$ the [[orthogonal group]] of [[Minkowski space]]. This is called the [[first order formulation of gravity]].

One can read the [[D'Auria-Fre formulation of supergravity]] as saying that higher dimensional [[supergravity]] is analogously given by higher Cartan supergeometry. See there and see the examples at [[higher Klein geometry]] for more on this.

## Related concepts

* [[higher differential geometry]]

* [[higher Klein geometry]]

## References

Traditional Cartan geometry goes back to

* {#Cartan23} [[Élie Cartan]] _Sur les vari&#233;t&#233;s &#224; connexion affine et la th&#233;orie de la relativit&#233; g&#233;n&#233;ralis&#233;e (premi&#232;re partie)_. Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 3, 40 (1923), p. 325-412  ([NUMDAM](http://www.numdam.org/item?id=ASENS_1923_3_40__325_0))

There is secretly a good bit of higher super-Cartan geometry in the [[supergravity]] textbook

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

based on results and observations due to

* {#DAuriaFreRegge80} [[Riccardo D'Auria]], [[Pietro Fré]] [[Tullio Regge]], _Graded Lie algebra, cohomology and supergravity_, Riv. Nuov. Cim. 3, fasc. 12 (1980) ([spire](http://inspirehep.net/record/156191))

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]] _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 


Mentioning of the need for [[definite globalizations of WZW terms]] is (ever so briefly) in 

* {#Witten86} [[Edward Witten]], p. 17 of _Twistor - Like Transform in Ten-Dimensions_, Nucl. Phys. B266 (1986) 245 ([spire](http://inspirehep.net/record/214192/?ln=en))

That there ought to be a systematic study of [[higher Klein geometry]] and higher Cartan geometry has been amplified by [[David Corfield]] since 2006.

Construction of the higher WZW terms on homotopy quotients $G/H$ of higher super-groups is due to

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, International Journal of Geometric Methods in Modern Physics, Volume 12, Issue 02 (2015) 1550018 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

with more details in ([dcct](#dcct)).

A formalization of higher Cartan geometry via [[differential cohesion]] is in

* {#dcct} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Urs Schreiber]], _[[schreiber:Higher Cartan Geometry]]_, Harmonic analysis seminar, Charles University Prague, 2015

Formalization in [[modal homotopy type theory|modal]] [[homotopy type theory]]:

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017

In the context of [[Poincaré duality]] on [[supermanifolds]] (cf. also at *[[super Cartan geometry]]*) :

* [[Konstantin Eder]], [[John Huerta]], [[Simone Noja]], _Poincaré Duality for Supermanifolds, Higher Cartan Structures and Geometric Supergravity_ &lbrack;[arXiv:2312.05224](https://arxiv.org/abs/2312.05224)&rbrack;

[[!redirects Cartan 2-geometry]]

[[!redirects ∞-Cartan connection]]
[[!redirects ∞-Cartan connections]]

[[!redirects higher Cartan connection]]
[[!redirects higher Cartan connections]]