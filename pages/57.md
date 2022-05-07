
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

_Lie integration_ is a process that assigns to a [[Lie algebra]] $\mathfrak{g}$ -- or more generally to an [[L-∞-algebra|∞-Lie algebra]] or [[∞-Lie algebroid]] -- a [[Lie group]] -- or more generally [[∞-Lie groupoid]] -- that is [[infinitesimal space|infinitesimally]] modeled by $\mathfrak{g}$. It is essentially the reverse operation to [[Lie differentiation]], except that there are in general several objects Lie integrating a given Lie algebraic datum, due to the fact that the infinitesimal data does not uniquely determine global topological properties.

Classically, Lie integration of [[Lie algebras]] is part of [[Lie's three theorems]], which in particular finds an unique (up to [[isomorphism]]) [[simply connected]] Lie group integrating a given finite-dimensional Lie algebra. 

One may observe that the [[simply connected]] [[Lie group]] integrating a (finite-dimensional) Lie algebra is equivalently realized as the collection of [[equivalence classes]] of [[Lie algebra valued 1-forms]] on the interval where two such are identified if they are interpolated by a _flat_ Lie-algebra valued 1-form on the [[disk]]. ([Duistermaat-Kolk 00, section 1.14](#DuistermaatKolk00), see also the example [below](#LieAlgebrasToLieGroups)). 

This _path method_ of Lie integration stands out as having natural generalizations to [[higher Lie theory]] ([&#352;evera 01](#Severa01)).  

In its evident generalization from [[Lie algebra valued differential forms]] to [[Lie algebroid valued differential forms]] this provides a means for Lie integration of [[Lie algebroids]] (e.g. [Crainic-Fernandes 01](#Crainic)).

In another direction, one may observe that [[L-∞ algebras]] are [[formal dual|formally dually]] incarnated by their [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]] [[dg-algebras]], and that under this identification the evident generalization of the path method to [[L-∞ algebra valued differential forms]] is essentially the [[Sullivan construction]], known from [[rational homotopy theory]], applied to these dg-algebras ([Hinich 97](#Hinich97), [Getzler 04](#Getzler04)). Or rather, the bare such construction gives the [[geometrically discrete ∞-groupoid|geometrically discrete]] [[∞-group]] underlying what should be the Lie integration to a [[smooth ∞-group]]. This is naturally obtained, as in the classical case, by suitably smoothly parameterizing the [[∞-Lie algebroid valued differential forms]] ([Henriques 08](#Henriques), [Roytenberg 09](#Roytenberg09), [FSS 12](#FSS12)).

Both these directions may be combined via the evident concept of [[∞-Lie algebroid valued differential forms]] to yield a Lie integration of [[∞-Lie algebroids]] to [[smooth ∞-groupoids]]. (Moreover, the same formula directly generalizes from $L_\infty$-algebroids to [[A-infinity categories]] to yield the _[[dg-nerve]]_ construction.)

While the construction exists and behaves as expected in examples, there is to date no good general theory providing higher analogs of, say, [[Lie's three theorems]]. But people are working on it.


## Definition

Throughout, let $\mathfrak{a}$ be an [[∞-Lie algebroid]] (for instance a [[Lie algebra]], or a [[Lie algebroid]] or an [[L-∞-algebra]]). Write 

$$
  CE(\mathfrak{a}) \in dgAlg
$$

for its [[Chevalley-Eilenberg algebra]], a [[dg-algebra]]. Notice that, by the discussion at _[[L-∞ algebra]]_ and at _[[∞-Lie algebroid]]_, the Chevalley-Eilenberg dg-algebras $CE(\mathfrak{a})$ is the [[formal dual]] of $\mathfrak{a}$, in that the [[functor]]

$$
  CE \colon \infty LieAlgd \hookrightarrow dgAlg^{op}
$$

is a [[fully faithful functor]]. Indeed, the following definition of Lie integration (being just a smooth refinement of the [[Sullivan construction]]) makes sense just as well for any dg-algebra, not necessarily in the [[essential image]] of this embedding. But only for dg-algebras in the essential image of this embedding do the examples come out as expected for [[higher Lie theory]].

An [[∞-Lie algebra]] is equivalently a [[pointed object|pointed]] [[∞-Lie algebroid]] whose base space is the point. We write $\mathfrak{b}\mathfrak{g} \in \infty Lie Algd$ for objects of this form ("[[delooping]]")

$$
  \array{
     \infty LieAlgd &\stackrel{CE}{\hookrightarrow}& dgAlg^{op}
     \\
     \uparrow^{\mathrlap{b}} & \nearrow_{\mathrlap{CE}}
     \\
     \infty LieAlg
     \,.
  }
$$

Notice that this induces some degree shifts that may be a little ambiguous in situations like the [[line Lie n-algebra]]: as an [[L-∞ algebra]] this is $b^{n-1}\mathbb{R}$, the corresponding [[∞-Lie algebroid]] is $b^n \mathbb{R}$.


### Higher dimensional paths in an $\infty$-Lie algebroid
 {#HigherPathsInAnInfinityLieAlgebroid}


+-- {: .num_example}
###### Example

For $X$ a [[smooth manifold]] (possibly [[nLab:manifold with boundary|with boundary]] and [[manifold with corners|with corners]]) then its [[tangent Lie algebroid]] $T X$ is the one whose [[Chevalley-Eilenberg algebra]] is the [[de Rham complex]] 

$$
  CE(T X) = (\Omega^\bullet(X), d_{dR})
  \,.
$$

=--

+-- {: .num_defn #kPath}
###### Definition

For $k \in \mathbb{N}$ write $\Delta^k$ for the standard $k$-[[simplex]] regarded as a [[smooth manifold]] ([[nLab:manifold with boundary|with boundary]] and [[manifold with corners|with corners]]).  

A **$k$-path** in the $\infty$-Lie algebroid $\mathfrak{a}$ is a morphism of $\infty$-Lie algebroids of the form

$$
  \Sigma \; \coloneqq \; T \Delta^k \longrightarrow \mathfrak{a}
$$ 

from the [[tangent Lie algebroid]] $T \Delta^k$ of the standard smooth $k$-simplex to $\mathfrak{a}$. Dually this is equivalently a [[homomorphism]] of [[dg-algebras]]

$$
  \Omega^\bullet(\Delta^k) \longleftarrow CE(\mathfrak{a}) \;\colon\; \Sigma^*
$$

from the [[Chevalley-Eilenberg algebra]] of $\mathfrak{a}$ to the [[de Rham complex]] of $\Delta^d$.

=--

See also at _[[differential forms on simplices]]_.

+-- {: .num_remark}
###### Remark

A $k$-path in $\mathfrak{a}$, def. \ref{kPath}, is equivalently 

1. a _flat_ $\mathfrak{a}$-[[infinity-Lie algebroid valued differential form|valued differential form]] on $\Delta^k$;

1. a [[Maurer-Cartan element]] in $\Omega^\bullet(\Delta^k)\otimes \mathfrak{a}$.

=--

The Lie integration of $\mathfrak{a}$ is essentially the [[simplicial object]] whose $k$-cells are the $d$-paths in $\mathfrak{a}$. However, in order for this to be well-behaved, it is possible and useful to restrict to $d$-paths that are sufficiently well-behaved towards the [[boundary]] of the simplex:

+-- {: .num_defn}
###### Definition

Regard the smooth simplex $\Delta^k$ as embedded into the [[Cartesian space]] $\mathbb{R}^{k+1}$ in the standard way, and equip $\Delta^k$ with the [[metric space]] structure induced this way.

A smooth [[differential form]] $\omega$ on $\Delta^k$ is said to have **sitting instants** along the boundary if, for every $(r \lt k)$-face $F$ of $\Delta^k$ there is an [[open neighbourhood]] $U_F$ of $F$ in $\Delta^k$ such that $\omega$ restricted to $U$ is constant in the directions perpendicular to the $r$-face on its value restricted to that face.

More generally, for any $U \in $ [[CartSp]] a smooth differential form $\omega$ on $U \times\Delta^k$ is said to have sitting instants if there is $0 \lt \epsilon \in \mathbb{R}$ such that for all points $u : * \to U$ the pullback along  $(u, \mathrm{Id}) : \Delta^k \to U \times \Delta^k$ is a form with sitting instants on $\epsilon$-[[open neighbourhood|neighbourhood]]s of faces.

Smooth forms with sitting instants clearly form a sub-dg-algebra of all smooth forms. We write $\Omega^\bullet_{si}(U \times \Delta^k)$ for this sub-dg-algebra.

We write $\Omega_{si,vert}^\bullet(U \times \Delta^k)$ for the further sub-dg-algebra of [[vertical differential form]]s with respect to the projection $p : U \times \Delta^k \to U$, hence the [[coequalizer]]

$$
  \Omega^\bullet(U)
  \stackrel{\stackrel{p^*}{\longrightarrow}}{\underset{0}{\longrightarrow}}
  \Omega^\bullet_{si}(U \times \Delta^k)
  \to
  \Omega^\bullet_{si, vert}(U \times \Delta^k)  
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The dimension of the normal direction to a face depends on the dimension of the face:  there is one perpendicular direction to a codimension-1 face, and $k$ perpendicular directions to a
vertex. 

=--

+-- {: .num_example}
###### Examples

* A smooth 0-form (a [[smooth function]]) has sitting instants on $\Delta^1$ if in a neighbourhood of the endpoints it is constant.

  A smooth function $f : U \times \Delta^1 \to \mathbb{R}$ is in $\Omega^0_{\mathrm{vert}}(U \times \Delta^1)$ if there is $0 \lt \epsilon \in \mathbb{R}$ such that for each $u \in U$ the function $f(u,-) : \Delta^1  \simeq [0,1] \to \mathbb{R}$ is constant on $[0,\epsilon) \coprod (1-\epsilon,1)$.

* A smooth 1-form has sitting instants on $\Delta^1$ if in a neighbourhood of the endpoints it vanishes.

* Let $X$ be a [[smooth manifold]], $\omega \in \Omega^\bullet(X)$ be a smooth differential form. Let 

  $$
    \phi \colon \Delta^k \to X
  $$

  be a [[smooth function]] that has [[sitting instants]] as a function: towards any $j$-face of $\Delta^k$ it eventually becomes perpendicularly constant.

  Then the [[pullback of differential forms|pullback]] form $\phi^* \omega \in \Omega^\bullet(\Delta^k)$ is a form with sitting instants.

=--

+-- {: .num_remark}
###### Remark

The condition of sitting instants serves to make smooth differential forms not be affected by the boundaries and corners of $\Delta^k$. Notably for $\omega_j \in \Omega^\bullet(\Delta^{k-1})$ a collection of forms with sitting instants on the $(k-1)$-cells of a [[horn]] $\Lambda^k_i$ that coincide on adjacent boundaries, and for

$$
  p \colon \Delta^k \to \Lambda^{k-1}_i
$$

a standard piecewise smooth [[retract]], the [[pullback of differential forms|pullbacks]]

$$
  p^* \omega_i 
$$

glue to a single smooth differential form (with sitting instants) on $\Delta^k$.

=--

+-- {: .num_remark}
###### Remark

That $\omega \in \Omega^\bullet(\Delta^k)$ having sitting instants does not imply that there is a neighbourhood of the boundary of $\Delta^k$ on which $\omega$ is entirely constant. It is important for the following constructions that in the vicinity of the boundary $\omega$ is allowed to vary parallel to the boundary, just not perpendicular to it.

=--

### Integration to a discrete $\infty$-groupoid 
 {#IntToBareGrpd}

Here we discuss the [[discrete ∞-groupoid]]s underlying the 
[[smooth ∞-groupoid]]s to which an [[∞-Lie algebroid]] integrates.

For $\mathfrak{a}$ an $\infty$-Lie algebroid, the $d$-paths in $\mathfrak{a}$ naturally form a [[simplicial set]] as $d$ varies:

$$
  \begin{aligned}
    \exp(\mathfrak{a})_{bare}
    & \coloneqq
    \left(
     \cdots    
     Hom_{\infty LieAlgd}(T \Delta^2, \mathfrak{a})
     \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
     Hom_{\infty LieAlgd}(T \Delta^1, \mathfrak{a})
     \stackrel{\longrightarrow}{\longrightarrow}
     Hom_{\infty LieAlgd}(T \Delta^0, \mathfrak{g})
    \right)
     \\
    & =
   (
   \cdots 
   Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(\Delta^2))
   \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
   Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(\Delta^1))
   \stackrel{\longrightarrow}{\longrightarrow}
   Hom_{dgAlg}(CE(\mathfrak{a}), \Omega^\bullet(\Delta^0))
   )
  \end{aligned}
  \,.
$$


(We are indicating only the face maps, not the degeneracy maps, just for notational simplicity).

If here instead of smooth differential forms one uses [[polynomial differential forms]] then this is precisely the [[Sullivan construction]] of [[rational homotopy theory]] applied to $CE(\mathfrak{a})$. We next realize [[smooth structure]]  on this and hence realize this as an object in [[higher Lie theory]].


+-- {: .num_remark #SpuriousHomotopyGroups}
###### Remark
**(spurious homotopy groups)**

For $\mathfrak{a}$ a [[infinity-Lie algebroid|Lie n-algebroid]] (an $n$-[[truncated]] $\infty$-Lie algebroid) this construction will not yield in general an $n$-[[truncated]] [[∞-groupoid]] $\exp(\mathfrak{a})$. 

To see this, consider the example (discussed in detail [below](#LieAlgebrasToLieGroups)) that $\mathfrak{a} = \mathfrak{g}$ is an ordinary [[Lie algebra]]. Then $\exp(\mathfrak{g})_n$ is canonically identified with the set of smooth based maps $\Delta^n \to G$ into the simply connected [[Lie group]] that integrates $\mathfrak{g}$ in ordinary [[Lie theory]]. This means that the simplicial [[homotopy group]]s of $\exp(\mathfrak{g})$ are the topological homotopy groups of $G$, which in general (say for $G$ the [[orthogonal group]] or [[unitary group]]) will be non-trivial in arbitrarily higher degree, even though $\mathfrak{g}$ is just a Lie 1-algebra. This phenomenon is well familiar from [[rational homotopy theory]], where a classical theorem asserts that the rational homotopy groups of $\exp(\mathfrak{g})$ are generated from the generators in a [[minimal Sullivan model]] resolution of $\mathfrak{g}$. 

=--

For the purposes of [[higher Lie theory]] therefore instead one wants to [[truncated|truncate]] $\exp(\mathfrak{g})$ to its $(n+1)$-[[coskeleton]]

$$
  \mathbf{cosk}_{n+1}\exp(\mathfrak{a})_{bare}  
  \,.
$$


This divides out [[n-morphisms]] by $(n+1)$-morphisms and forgets all higher higher nontrivial morphisms, hence all higher homotopy groups.

$\,$

### Integration to a smooth $\infty$-groupoid 
  {#SmoothIntegration}
 

We now discuss Lie integration of $\infty$-Lie algebroids to [[smooth ∞-groupoid]]s, [[presentable (∞,1)-category|presented]] by the [[model structure on simplicial presheaves]] $[CartSp_{smooth}^{op}, sSet]_{proj,loc}$ over the [[site]] [[CartSp]]${}_{smooth}$.



For the following definition recall the [[presentable (∞,1)-category|presentation]] of [[smooth ∞-groupoids]] by the [[model structure on simplicial presheaves]] over the [[site]] [[CartSp]]${}_{smooth}$. 

+-- {: .num_defn}
###### Definition

For $\mathfrak{a}$ an [[L-∞ algebra]] of [[finite type]] with [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ define the [[simplicial presheaf]] 

$$
  \exp(\mathfrak{a}) \;\colon\; CartSp_{smooth}^{op} \to sSet
$$

by

$$  
  \exp(\mathfrak{a})
  \;\colon\;
  (U,[k]) \mapsto 
  Hom_{dgAlg}(CE(\mathfrak{a}), 
  \Omega^\bullet(U \times \Delta^k)_{si,vert})
  \,,
$$


for all $U \in $ [[CartSp]] and $[k] \in \Delta$. 

=--

+-- {: .num_remark}
###### Remark

Compared to the integration to [[discrete ∞-groupoids]] [above](#IntToBareGrpd) this definition knows about $U$-parametrized _smooth families_ of $k$-paths in $\mathfrak{g}$.

The underlying [[discrete ∞-groupoid]] is recovered as that of the $\mathbb{R}^0 = *$-parameterized family:

$$
  \exp(\mathfrak{a}) \colon \mathbb{R}^0 \mapsto \exp(\mathfrak{a})_{disc}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The objects $\exp(\mathfrak{g})$ are indeed [[Kan complexes]] over each $U \in $ [[CartSp]].

=--

+-- {: .proof}
###### Proof

Observe that the standard [[continuous function|continuous]] [[horn]] [[retracts]] $f : \Delta^k \to \Lambda^k_i$ are [[smooth function|smooth]] away from the preimages of the $(r \lt k)$-faces of $\Lambda[k]^i$.

For $\omega \in \Omega^\bullet_{si,vert}(U \times \Lambda[k]^i)$ a differential form with sitting instants on $\epsilon$-neighbourhoods, let therefore $K \subset \partial \Delta^k$ be the set of points of distance $\leq \epsilon$ from any subface. Then we have a smooth function 

$$
  f : \Delta^k \setminus K \to \Lambda^k_i \setminus K
  \,.
$$

The [[pullback of differential forms|pullback]] $f^* \omega \in \Omega^\bullet(\Delta^k \setminus K)$ may be extended constantly back to a form with sitting instants on all of $\Delta^k$. 

The resulting assignment

$$
  (CE(\mathfrak{g}) \stackrel{A}{\longrightarrow} \Omega^\bullet_{si,vert}(U \times \Lambda^k_i))
  \mapsto
  (CE(\mathfrak{g}) \stackrel{A}{\to} \Omega^\bullet_{si,vert}(U \times \Lambda^k_i) \stackrel{f^*}{\to} \Omega^\bullet_{si,vert}(U \times \Delta^n))
$$

provides fillers for all [[horns]] over all $U \in $ [[CartSp]].

=--

+-- {: .num_defn}
###### Definition

Write $\mathbf{cosk}_{n+1} \exp(a)$ for the simplicial presheaf obtained by postcomposing $\exp(\mathfrak{a}) : CartSp^{op} \to sSet$ with the $(n+1)$-[[coskeleton]] [[functor]] $\mathbf{cosk}_{n+1} : sSet \stackrel{tr_n}{\longrightarrow} sSet_{\leq n+1} \stackrel{cosk_{n+1}}{\to} sSet$.

=--

## Properties

### Homotopy groups
 {#PropertiesHomotopyGroups}

...([Henriques, theorem 6.4](#Henriques))... remark \ref{SpuriousHomotopyGroups}...

### Quillen adjunction
 {#QuillenAdjunction}

The [above](#SmoothIntegration) construction of Lie integraton to [[smooth ∞-groupoids]] clearly applies to all [[differential graded-commutative algebras]], not necessarily just those which are [[Chevalley-Eilenberg algebras]] of [[L-∞ algebras]]. (but up to [[weak equivalence]], there is no difference). With this generalization, the higher Lie integration extends to a [[Quillen adjunction]] (Prop. \ref{LieIntegrationIsRightQuillenFunctor} below). In order to state this conveniently, we first make more explicit the [[functor]] assigning smooth families of [[smooth differential forms on simplices]] (Def. \ref{SmoothDifferentialFormsOnSimplicesWithSittingInstants} below).

$\,$

+-- {: .num_defn #SmoothDifferentialFormsOnSimplicesWithSittingInstants}
###### Definition
**(smooth families of [[smooth differential forms on simplices]] with [[sitting instants]])**

For $k \in \mathbb{N}$, write $\Delta^k_{mfd}$ for the [[k-simplex]] canonically regarded as a [[smooth manifold with boundaries and corners]].

For $n \in \mathbb{N}$, regard $\mathbb{R}^n \times \Delta^k_{mfd} \overset{p_1}{to} \mathbb{R}^n$ as the [[trivial bundle|trivial]] [[fiber bundle]] over the [[Cartesian space]] $\mathbb{R}^n$ with [[fiber]] that  smooth [[k-simplex]]. 

Write

$$
  \Omega^\bullet_{vert}(\mathbb{R}^n \times \Delta^k_{mfd})
  \hookrightarrow
  \Omega^\bullet(\mathbb{R}^n \times \Delta^k_{mfd})
$$

for the [[subobject|sub-]][[dgc-algebra]] of the [[de Rham algebra]] on the [[vertical differential forms]] with respect to this bundle structure.

Moreover, write

$$
  \Omega^\bullet_{vert, si}\left(\mathbb{R}^n \times \Delta^k_{mfd}\right)
  \hookrightarrow
  \Omega^\bullet_{vert}\left(\mathbb{R}^n \times \Delta^k_{mfd}\right)
$$

for the further [[subobject|sub-]][[dgc-algebra]] on those [[vertical differential forms]] which have [[sitting instants]] towards the [[boundary]] of the [[k-simplex]].

Via [[pullback of differential forms]] this construction provides a [[functor]]

$$
  \Omega^\bullet_{vert,si}
  \;\colon\;
  CartSp \times \Delta
    \longrightarrow
  dgcAlg_{\mathbb{R}, conn}^{op}
$$

from the [[product category]] of the [[category]] [[CartSp]] of [[Cartesian spaces]] and [[smooth functions]] between them, with the [[simplex category]], to the [[opposite category|opposite]] of the [[category]] of connective [[dgc-algebras]] over the [[real numbers]].

=--

([FSS 12, Def. 4.2.1](#FSS12), see [Braunack-Mayer 18, Def. 3.1.3](#BraunackMayer18))

+-- {: .num_prop #LieIntegrationIsRightQuillenFunctor}
###### Proposition
**(Lie integration is [[right Quillen functor]] to [[smooth ∞-groupoids]])**

There is a [[Quillen adjunction]]

$$
  dgcAlg^{op}_{\mathbb{R}, \geq 0, proj}
    \;
    \underoverset
      {\underset{ Spec }{\longrightarrow}}
      {\overset{ \mathcal{O} }{\longleftarrow}}
      {\phantom{A}\phantom{{}_{Qu}}\bot_{Qu}\phantom{A}}
    \;
  [CartSp^{op},sSet_{Qu}]_{proj,loc}
$$

between

1. the [[projective local model structure on simplicial presheaves]] over [[CartSp]], regarded as a [[site]] via the [[good open cover]] [[coverage]] (i.e. [[locally presentable (∞,1)-category|presenting]] [[smooth ∞-groupoids]]);

1. the [[opposite model category|opposite]] [[projective model structure on connective dgc-algebras]] over the [[real numbers]]

given by [[nerve and realization]] with respect to the [[functor]] of [[smooth differential forms on simplices]]
$  
  CartSp \times \Delta
    \overset{\Omega^\bullet_{vert,si}}{\longrightarrow}
  dgcAlg_{\mathbb{R}, conn}^{op}
$ from Def. \ref{SmoothDifferentialFormsOnSimplicesWithSittingInstants}:


1. the [[right adjoint]] $Spec$ sends a [[dgc-algebra]] $A \in dgcAlg_{\mathbb{R},\geq 0}$ to the [[simplicial presheaf]] which in degree $k$ is the set of [[dg-algebra]]-[[homomorphism]] form $A$ into the [[dgc-algebras]] of [[smooth differential forms on simplices]] $\Omega^\bullet_{si,vert}(-)$ (Def. \ref{SmoothDifferentialFormsOnSimplicesWithSittingInstants}):

   $$
     Spec(A)
     \;\colon\;
     \mathbb{R}^n \times \Delta[k]
     \;\mapsto\;
     Hom_{dgcAlg_{\mathbb{R}}}
     \left(
       A , \Omega^\bullet_{si, vert}(\mathbb{R}^n \times \Delta^k_{mfd})
     \right)
   $$

1. the [[left adjoint]] $\mathcal{O}$ is the [[Yoneda extension]] of the [[functor]] $\Omega^\bullet_{vert,si} \;\colon\; CartSp \times \Delta \to dgcAlg_{\mathbb{R},conn}^{op}$ assigning [[dgc-algebras]] of [[smooth differential forms on simplices]] from Def. \ref{SmoothDifferentialFormsOnSimplicesWithSittingInstants},

   hence which acts on a [[simplicial presheaf]] $\mathbf{X} \in [CartSp^{op}, sSet] \simeq [\CartSp^{op} \times \Delta^{op}, Set]$, expanded via the [[co-Yoneda lemma]] as a [[coend]] of [[representable presheaves|representables]], as

   $$
     \mathcal{O}
     \;\colon\;
     \mathbf{X}
     \simeq
     \int^{n,k}
     y(\mathbb{R}^n \times \Delta[k]) \times \mathbf{X}(\mathbb{R}^n)_k
     \;\mapsto\;
     \int_{n,k}
     \underset{\mathbf{X}(\mathbb{R}^n)_k}{\prod}
     \Omega^\bullet_{si,vert}\left(\mathbb{R}^n \times \Delta^k_{mfd}\right)
   $$

=--

([Braunack-Mayer 18, theorem 3.1.10](#BraunackMayer18))


## Examples

See also at _[[smooth ∞-groupoid -- structures]]_ the section _[Exponentiated ∞-Lie algebras](smooth+infinity-groupoid+--+structures#StrucLieAlg)_.


### Interating Lie algebras to Lie groups 
  {#LieAlgebrasToLieGroups}

Let $\mathfrak{g} \in L_\infty$ be an ordinary (finite dimensional) [[Lie algebra]]. Standard [[Lie theory]] (see [[Lie's three theorems]]) provides a [[simply connected]] [[Lie group]] $G$ integrating $\mathfrak{g}$.

With $G$ regarded as a [[smooth ∞-groupoid|smooth ∞-group]] write $\mathbf{B}G \in $ [[Smooth∞Grpd]] for its [[delooping]]. The standard presentation of this on $[CartSp_{smooth}^{op}, sSet]$ is by the [[simplicial presheaf]] 

$$
  \mathbf{B}G_c 
  \colon 
  U \mapsto N(C^\infty(U,G) \stackrel{\longrightarrow}{\longrightarrow} *)
  \,.
$$


See at _[smooth infinity-groupoid -- structures -- Lie groups](smooth+infinity-groupoid+--+structures#LieGroups)_ for more details.

+-- {: .num_prop #ResultOfIntegrationOfOrdinaryLieAlgebra}
###### Proposition

The operation of [[parallel transport]] $P \exp(\int -) : \Omega^1([0,1], \mathfrak{g}) \to G$ yields a weak equivalence (in $[CartSp^{op}, sSet]_{proj}$)

$$
  P \exp(\int (-) )
  \;\colon\;
  \mathbf{cosk}_3 \exp(\mathfrak{g}) 
  \;\simeq\; 
   \mathbf{cosk}_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G_c
  \,.
$$

=--


This follows from the [[Steenrod-Wockel approximation theorem]] and the following observation.

+-- {: .num_lemma}
###### Lemma

For $X$ a [[simply connected]] [[smooth manifold]] and $x_0 \in X$ a basepoint, there is a canonical [[bijection]]

$$
  \Omega^1_{flat}(X,\mathfrak{g}) \simeq C^\infty_*(X,G)
$$

between the set of [[Lie-algebra valued 1-form]]s on $X$ whose [[curvature]] 2-form vanishes, and the set of [[smooth function]]s $X\to G$ that take $x_0$ to the neutral element $e \in G$.

=--

+-- {: .proof}
###### Proof

The bijection is given as follows. For $A \in \Omega^1_{flat}(X,\mathfrak{g})$ a flat 1-form, the corresponding function $f_A : X \to G$ sends $x \in X$ to the [[parallel transport]] along any path $x_0 \to x$ from the base point to $x$

$$
  f_A : x \mapsto tra_A(x_0 \to x)
  \,.
$$

Because of the assumption that the [[curvature]] 2-form of $A$ vanishes and the assumption that $X$ is [[simply connected]], this assignment is independent of the choice of path.

Conversely, for every such function $f : X \to G$ we recover $A$ as the pullback of the [[Maurer-Cartan form]] on $G$

$$
  A = f^* \theta
  \,.
$$

=--

From this we obtain

+-- {: .proof}
###### Proof of prop. \ref{ResultOfIntegrationOfOrdinaryLieAlgebra}.

The $\infty$-groupoid $\mathbf{cosk}_2 \exp(\mathfrak{g})$ is equivalent to the [[groupoid]] with a single object (no non-trivial 1-form on the point) whose morphisms are equivalence classes of smooth based paths $\Delta^1 \to G$ (with sitting instants), where two of these are taken to be equivalent if there is a smooth [[homotopy]] $D^2 \to G$ (with sitting instant) between them.

Since $G$ is [[simply connected]], these equivalence classes are labeled by the endpoints of these paths, hence are canonically identified with $G$.

=--

+-- {: .num_remark}
###### Remark

We do not need to fall back to classical [[Lie theory]] to obtain $G$ in the above argument. A detailed discussion of how to find $G$ with its group structure and smooth structure from $d$-paths in $\mathfrak{g}$ is in ([Crainic](#Crainic)).

=--



### Integrating to line/circle Lie $n$-groups 
 {#IntegrationToLineNGroup}


+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}, n \geq 1$ write $b^{n-1} \mathbb{R}$ for the [[L-∞-algebra]] whose [[Chevalley-Eilenberg algebra]] is given by a single generator in degree $n$ and vanishing differential. We may call this the **[[line Lie n-algebra]]**.

Write $\mathbf{B}^{n} \mathbb{R}$ for the <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">smooth line (n+1)-group</a>.

=--


+-- {: .num_prop}
###### Observation

The [[discrete ∞-groupoid]] underlying $\exp(b^{n-1} \mathbb{R})$ is given by the [[Kan complex]] that in degree $k$ has the set of closed differential $n$-forms (with sitting instants) on the $k$-[[simplex]]

$$
  \exp(b^{n-1} \mathbb{R})_{disc}
  : 

  [k] \mapsto \Omega^n_{si,cl}(\Delta^k)
$$

=--

+-- {: .num_prop #LieIntegrationOfLinenLieAlgebra}
###### Proposition

The $\infty$-Lie integration of $b^{n-1} \mathbb{R}$ is the [[circle n-group]] $\mathbf{B}^{n} \mathbb{R}$. 

Moreover, with $\mathbf{B}^n \mathbb{R}_{chn} \in [CartSp_{smooth}^{op}, sSet]$ the standard presentation given under the [[Dold-Kan correspondence]] by the chain complex of sheaves concentrated in degree $n$ on $C^\infty(-, \mathbb{R})$ the equivalence is induced by the [[fiber integration]] of differential $n$-forms over the $n$-[[simplex]]:

$$
  \int_{\Delta^\bullet} 
   : 
  \exp(b^{n-1} \mathbb{R})
   \stackrel{\simeq}{\longrightarrow}
  \mathbf{B}^{n} \mathbb{R}_{chn}
  \,.
$$


=--



+-- {: .proof}
###### Proof


First we observe that the map

$$
  \int_{\Delta^\bullet}
  :
  (\omega \in \Omega^n_{si,vert,cl}(U \times \Delta^k))
  \mapsto
  \int_{\Delta^k} \omega \in C^\infty(U, \mathbb{R})
$$ 

is a morphism of 
[[simplicial presheaves]] $\exp(b^{n-1} \mathbb{R}) \to \mathbf{B}^{n}\mathbb{R}_{chn}$ on [[CartSp]]${}_{smooth}$. Since it goes between presheaves of abelian [[simplicial group]]s by the [[Dold-Kan correspondence]] it is sufficient to check that we have a morphism of [[chain complex]]es of presheaves on the corresponding [[Moore complex|normalized chain complex]]es.

The only nontrivial degree to check is degree $n$. Let $\lambda \in \Omega_{si,vert,cl}^n(\Delta^{n+1})$. The differential of the [[Moore complex|normalized chains complex]] sends this to the signed sum of its restrictions to the $n$-faces of the $(n+1)$-simplex. Followed by the integral over $\Delta^n$ this is the piecewise integral of $\lambda$ over the boundary of the $n$-simplex. Since $\lambda$ has sitting instants, there is $0 \lt \epsilon \in \mathbb{R}$ such that there are no contributions to this integral in an $\epsilon$-neighbourhood of the $(n-1)$-faces. Accordingly the integral is equivalently that over the smooth surface inscribed into the $(n+1)$-simplex, as indicated in the following diagram


<svg width="640" height="480" xmlns="http://www.w3.org/2000/svg">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <g>
  <title>Layer 1</title>
  <path id="svg_1" d="m40,149l281,-2l-138,192l-143,-190z" stroke="#000000" fill="#ffffff"/>
  <ellipse ry="117" rx="127" id="svg_2" cy="248" cx="495" stroke-width="2" stroke="#000000" fill="#5874c9"/>
  <path id="svg_5" d="m64,181l92,124c16.66701,23 38.33299,22 53,0l89,-125c18.33301,-26 16.66699,-33 -26,-33l-185,2c-30.66666,-0.33333 -39.33334,10.33333 -23,32z" stroke="#000000" fill="#558cc6"/>
  <path id="svg_6" d="m90,182c-16,-15.66667 -10,-22.33333 18,-20l152,-1c20,-1.33333 28,7.33333 18,20l-84,114c-6.33333,13 -14.66667,15 -22,0l-82,-113z" stroke="#000000" fill="#ffffff"/>
  <ellipse ry="52" rx="55" id="svg_7" cy="157" cx="61" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="55" rx="60" id="svg_8" cy="159" cx="289" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="46" rx="51" id="svg_9" cy="317" cx="180" stroke-dasharray="5,5" stroke="#000000" fill="none"/>
  <ellipse ry="87" rx="99" id="svg_10" cy="248.00001" cx="496" stroke-dasharray="5,5" stroke="#000000" fill="#ffffff"/>
  <line id="svg_13" y2="160" x2="103" y1="148" x1="103" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_14" y2="160" x2="240" y1="147" x1="241" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_15" y2="161" x2="144" y1="148" x1="144" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_16" y2="159" x2="185" y1="147" x1="185" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_17" y2="184" x2="425" y1="161" x1="407" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_18" y2="165" x2="458" y1="139" x1="446" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_19" y2="160" x2="507" y1="131" x1="507" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_20" y2="172" x2="543" y1="146" x1="556" stroke-width="4" stroke="#ff5656" fill="none"/>
  <line id="svg_22" y2="193" x2="76" y1="183" x1="90" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_23" y2="219" x2="93" y1="208" x1="108" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_24" y2="257" x2="121" y1="247" x1="135" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_25" y2="295" x2="150" y1="285" x1="164" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_26" y2="256" x2="396" y1="259" x1="368" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_27" y2="297" x2="413" y1="314" x1="391" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_28" y2="323" x2="444" y1="345" x1="427" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_29" y2="333" x2="479" y1="362" x1="473" stroke-width="4" stroke="#7fff00" fill="none"/>
  <line id="svg_30" y2="295" x2="215" y1="284" x1="201" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_31" y2="271" x2="231" y1="261" x1="218" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_32" y2="236" x2="255" y1="227" x1="243" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_33" y2="198" x2="283" y1="188" x1="271" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_34" y2="348" x2="555" y1="323" x1="542" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_35" y2="311" x2="602" y1="293" x1="580" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_36" y2="260" x2="620" y1="256" x1="594" stroke-width="4" stroke="#ffff00" fill="none"/>
  <line id="svg_37" y2="210" x2="615" y1="221" x1="590" stroke-width="4" stroke="#ffff00" fill="none"/>
  <path id="svg_39" d="m256,272c16.33334,40.33334 68.66666,63.66666 109,49" stroke-width="4" stroke="#000000" fill="none"/>
  <line id="svg_40" y2="320" x2="362" y1="311" x1="349" stroke-width="4" stroke="#000000" fill="none"/>
  <line id="svg_41" y2="321" x2="363" y1="332" x1="355" stroke-width="4" stroke="#000000" fill="none"/>
 </g>
</svg>

Since $\lambda$ is a closed form on the $n$-simplex, this surface integral vanishes, by the [[Stokes theorem]]. Hence $\int_{\Delta^\bullet}$ is indeed a chain map.

It remains to show that $\int_{\Delta^\bullet} : \exp(b^{n-1} \mathbb{R}) \to \mathbf{B}^{n}\mathbb{R}_{chn}$ is an [[isomorphism]] on all the [[simplicial homotopy]]s group over each $U \in CartSp$. This amounts to the statement that 

1. a smooth family of closed $n$-forms with sitting instants on the boundary of $\Delta^{n+1}$ may be extended to a smooth family of closed forms with sitting instants on $\Delta^{n+1}$ precisely if their smooth family of integrals over the boundary vanishes;

1. Any smooth family of closed $n \lt k$-forms with sitting instants on the boundary of $\Delta^{k+1}$ may be extended to a smooth family of closed $n$-forms with sitting instants on $\Delta^{k+1}$.

To demonstrate this, we want to work with forms on the $(k+1)$-[[ball]] instead of the $(k+1)$-[[simplex]]. To achieve this, choose again $0 \lt \epsilon \in \mathbb{R}$ and construct the [[diffeomorphism|diffeomorphic]] image of $S^k \times [1,1-\epsilon]$ inside the $(k+1)$-simplex as indicated in the above diagram: outside an $\epsilon$-neighbourhood of the corners the image is a rectangular $\epsilon$-thickening of the faces of the simplex. Inside the $\epsilon$-neighbourhoods of the corners it bends smoothly. By the [[Steenrod-Wockel approximation theorem]] the diffeomorphism from this $\epsilon$-thickening of the smoothed boundary of the simplex to $S^k \times [1-\epsilon,1]$ extends to a smooth function from the $(k+1)$-simplex to the $(k+1)$-ball. 

By choosing $\epsilon$ smaller than each of the sitting instants of the given $n$-form on $\partial \Delta^{k+1}$, we have that this $n$-form vanishes on the $\epsilon$-neighbourhoods of the corners and is hence entirely determined by its restriction to the smoothed simplex, identified with the $(k+1)$-ball.

It is now sufficient to show: a smooth family of smooth $n$-forms $\omega \in \Omega^n_{vert,cl}(U \times S^k)$ extends to a smooth family of closed $n$-forms $\hat \omega \in \Omega^n_{vert,cl}(U \times B^{k+1})$ that is radially constant in a neighbourhood of the boundary for all $n \lt k$ and for $k = n$ precisely if its smooth family of integrals vanishes, $\int_{S^k} \omega = 0 \in C^\infty(U, \mathbb{R})$.

Notice that over the point this is a direct consequence of the [[de Rham theorem]] ([[kernel of integration is the exact differential forms]]): an $n$-form $\omega$ on $S^k$ is exact precisely if $n \lt k$  or if $n = k$ and its integral vanishes. In that case there is an $(n-1)$-form $A$ with $\omega = d A$. Choosing any smoothing function $f : [0,1] \to [0,1]$ (smooth, surjective, non-decreasing and constant in a neighbourhood of the boundary) we obtain an $n$-form $f \wedge A$ on $(0,1] \times S^k$, vertically constant in a neighbourhood of the ends of the interval, equal to $A$ at the top and vanishing at the bottom. Pushed forward along the canonical $(0,1] \times S^k \to D^{k+1}$ this defines a form on the $(k+1)$-ball, that we denote by the same symbol $f \wedge A$. Then the form $\hat \omega := d (f \wedge A)$ solves the problem.

To complete the proof we have to show that this simple argument does extend to smooth families of forms, i.e., that we can choose the $(n-1)$-form $A$ in a way depending smoothly on the the $n$-form $\omega$. 

One way of achieving this is using [[Hodge theory]]. Fix a [[Riemannian metric]] on $S^n$, and let $\Delta$ be the corresponding [[Laplace operator]], and $\pi$ the projection on the space of [[harmonic forms]]. Then the 
<a href="http://ncatlab.org/nlab/show/Hodge+theory#ResultsOverRiemannianManifold">central result of Hodge theory</a> for [[compact topological space|compact]] [[Riemannian manifold]]s states that the operator $\pi$, seen as an operator from the 
[[de Rham complex]] to itself, is a cochain map [[homotopy|homotopic]] to the identity, via an explicit homotopy $P := d^* G$ expressed in terms of the adjoint $d^*$ of the de Rham differential and of the [[Green operator]] $G$ of $\Delta$. Since the $k$-form $\omega$ is exact its projection on [[harmonic form]]s vanishes. Therefore

$$
  \begin{aligned}
    \omega & = (Id-\pi)\omega 
    \\
     & = d (P\omega)+P (d\omega)
    \\
    & = d (P\omega).
  \end{aligned}
$$

Hence $A := P\omega$ is a solution of the differential equation $d A=\omega$ depending smoothly on $\omega$.
 
=--



### Integrating the string Lie 2-algebra to the string Lie 2-group

Let $\mathfrak{string} = \mathfrak{g}_\mu$ be the [[string Lie 2-algebra]].

Then $\mathbf{cosk}_3 \exp(\mathfrak{g}_\mu)$ is equivalent to the [[2-groupoid]] $\mathbf{B}String$ 

* with a single object;

* whose morphisms are based paths in $G$;

* whose 2-morphisms are equivalence class of pairs $(\Sigma,c)$, where 

  * $\Sigma : D^2_*  \to G$ is a smooth based map (where we use a [[homeomorphism]] $D^2 \simeq \Delta^2$ which away from the corners is smooth, so that forms with sitting instants there do not see any non-smoothness, and the basepoint of $D^2_*$ is the 0-vertex of $\Delta^2$) 

  * and $c \in U(1)$, and where two such are equivalent if the maps coincides at their boundary and if for any 3-ball $\phi : D^3 \to G$ filling them the labels $c_1, c_2 \in U(1)$ differ by the integral $\int_{D^3} \phi^* \mu(\theta) \;\; mod \;\; \mathbb{Z}$,,

where $\theta$ is the [[Maurer-Cartan form]], $\mu(\theta) = \langle \theta\wedge [\theta \wedge \theta]\rangle $ the 3-form obtained by plugging it into the cocycle.

This is the [[string Lie 2-group]]. It's construction in terms of integration by paths is due to ([Henriques](#Henriques))



### Integrating Lie algebroids to (stacky) Lie groupoids

Unlike finite dimensional Lie algebras, not every Lie algebroid may be integrated to a Lie groupoid. There exists topological obstruction coming from $\pi_2(L)$ of the leaf $L\subset M$ of a Lie algebroid $A\to M$. The integrability criteria is completely classified through the behaviour of certain monodromy groups and that is the achievement of  [Crainic-Fernandes 01](#Crainic). These monodromy groups, providing obstructions of integration, may be seen as the image of a transgression map of the long exact sequence of [[Lie algebroid homotopy groups]] induced by the natural [[Lie algebroid fibration]] $A|_L \to L$. (see [Brahic-Zhu 10](#BZ) ). 

Let us now describe the construction of the universal groupoid for a Lie algebroid $A$. This is a major step contained in  [Crainic-Fernandes 01](#Crainic) and was earlier discovered in the setting of Poisson manifolds as the phase space of [[Poisson sigma model]] in [Cattaneo-Felder 00](#CattaneoFelder01). 

Given a Lie algebroid $A\to M$, an $A$-path (a Lie algebroid path), is a Lie algebroid morphism from $T\Delta^1 \to A$, that is, it is a path $a$ in $A$ such that $a=\rho(\gamma)$ where $\gamma=\pi(a)$ is the base path of $a$ (see [example](https://ncatlab.org/nlab/show/Lie+groupoid#example) ). 

An (end-fixing) $A$-homotopy (a Lie algebroid homotopy) is a Lie algebroid morphism from $T\square \to A$ satisfying certain boundary conditions. Let us be more precise: a vector bundle morphism $T\square \to A$ can be denoted by $a dt + b ds$ (see [example](https://ncatlab.org/nlab/show/Lie+groupoid#example_2) ). Then the boundary condition is that $b(s,0)=0$ and $b(s,1)=0$. The fact that $adt+bds$ is a Lie algebroid morphism is equivalent to the following PDE:


$$\partial_t b- \partial_s a= \nabla_{\rho \alpha} \beta - \nabla_{\rho \beta} \alpha +[\alpha, \beta] $$
where $\nabla$ is a TM connection on $A$ and $\alpha$ and $\beta$ are certain time dependent sections of $A$ extending $a$ and $b$ respectively. Notice that there is also a way writing down the right hand side independent of choice of sections. See Section 1 of [Crainic-Fernandes 01](#Crainic). 

Then the universal groupoid associated to $A$ is the space of $A$-paths ($P_a A$) dividing by $A$-homotopies. It is naturally a topological groupoid. But only when the obstruction vanishes, it becomes a Lie groupoid and is the source-simply connected Lie groupoid integrating $A$. 

Fortunately $A$-homotopies form finite codimensional foliation $F$, even though the quotient might not be always representible. Thus, $Mon_F(P_aA)$ represents a differentiable stack which becomes a stacky Lie groupoid over $M$. It turns out that there is a one-to-one correspondence between \'etale stacky Lie groupoid and Lie algebroid. This correspondence provides a positive answer to [[Lie's third theorem]] for Lie algebroids.  [Tseng-Zhu 04](#TZ). 

## Related concepts

* [[Kan-fibrant simplicial manifold]]

* [[parallel transport]], [[higher parallel transport]]

* [[holonomy]], [[higher holonomy]]

  * [[nonabelian Stokes theorem]]

* [[dg-nerve]]

* [[function algebras on infinity-stacks]]

[[!include infinitesimal and local - table]]



## References

The "path method" of integrating Lie algebras to simply connected Lie groups appears in 

* {#DuistermaatKolk00} [[Hans Duistermaat]], J. A. C. Kolk, section 1.14 of _Lie groups_, 2000

The idea of identifying the [[Sullivan construction]] applied to [[Chevalley-Eilenberg algebras]] as Lie integration to 
[[discrete ∞-groupoid]]s appears in

* {#Hinich97} [[Vladimir Hinich]], _Descent of Deligne groupoids_, Internat. Math. Res. Notices, 5:223&#8211;239, 1997 ([doi](http://dx.doi.org/10.1155/S1073792897000160), [preprint ddg.pdf](http://math.haifa.ac.il/hinich/WEB/mypapers/ddg.pdf))

and for general [[∞-Lie algebra]]s in

* {#Getzler04} [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$ algebras_, Annals of Mathematics, 170 (2009), 271&#8211;301 ([math.AT/0404003](http://arxiv.org/abs/math/0404003))

(whose main point is the discussion of a gauge condition applicable for nilpotent $L_\infty$-algebras that cuts down the result of the Sullivan construction to a much smaller but equivalent model) .

This was refined from integration to bare $\infty$-groupoids to an integration to [[internal ∞-groupoid]]s in [[Banach manifold]]s in

* {#Henriques} [[André Henriques]], _Integrating $L_\infty$ algebras_, Compos. Math. __144__  (2008), no. 4, 1017--1045 ([doi](http://dx.doi.org/10.1112/S0010437X07003405),[math.AT/0603563](http://arxiv.org/abs/math.AT/0603563))


(whose origin possibly preceeds that of Getzler's article).

For general [[∞-Lie algebroids]] the general idea of the integration process by "$d$-paths" had been indicated in 

* {#Severa01} [[Pavol Severa]],  _[[Some title containing the words "homotopy" and "symplectic", e.g. this one]]_, based on a talk at _[Poisson 2000](http://www.lpthe.jussieu.fr/~dito/poissongeometry/Poisson2000/index.html)_, [CIRM Marseille Luminy](https://www.cirm-math.fr/), June 2000 ([arXiv:0105080](http://arxiv.org/abs/math/0105080))


* Pavol &#352;evera, Michal &#352;ira&#328;, _Integration of differential graded manifolds_, [arxiv/1506.04898](http://arxiv.org/abs/1506.04898)

Lie integration of [[dg-modules]] to [[smooth spectrum|smooth]] [[parameterized spectra]] ([[twisted cohomology|twisted]] [[differential cohomology theories]]);

* {#BraunackMayer18} [[Vincent Braunack-Mayer]], section 3.1 of _[[schreiber:thesis Braunack-Mayer|Rational parameterized stable homotopy theory]]_, Zurich 2018 ([pdf](https://ncatlab.org/schreiber/show/thesis+Braunack-Mayer#pdf))

Discussion of Lie integration of [[Lie algebroids]] by the path method is due to 

* {#Crainic} [[Marius Crainic]], [[Rui Fernandes]], _Integrability of Lie brackets_, Ann. of Math. (2), Vol. 157 (2003), no. 2, 575--620 ([arXiv:math.DG/0105033](http://arxiv.org/abs/math/0105033))

following ([Duistermaat-Kolk 00, section 1.14](#DuistermaatKolk00)) and following the discussion of the special case of Lie integration of [[Poisson Lie algebroids]] to [[symplectic groupoids]] in 

* {#CattaneoFelder01} [[Alberto Cattaneo]], [[Giovanni Felder]], _Poisson sigma models and symplectic groupoids_, in _Quantization of Singular Symplectic Quotients_, (ed. [[Klaas Landsman]], M. Pflaum, M. Schlichenmeier), Progress in Mathematics 198 (Birkh&#228;user,
2001), 61&#8211;93. ([arXiv:math/0003023](http://arxiv.org/abs/math/0003023))
 

upgraded to the stacky version by

* {#TZ} Tseng Hsiang-Hua, [[Chenchang Zhu]], _Integrating Lie algebroids via stacks_, Compositio Mathematica, Volume 142 (2006), Issue 01, pp 251-270, [arXiv:math/0405003](http://arxiv.org/abs/math/0405003).

A general proof that equivalent $L_\infty$-algebras integrate to equivalent Lie $\infty$-groupoids is in 

* [[Christopher Rogers]], [[Chenchang Zhu]], _On the homotopy theory for Lie ∞-groupoids, with an application to integrating L∞-algebras_ ([arXiv:1609.01394](https://arxiv.org/abs/1609.01394))

Obstruction interpreted as transgression of a Lie algebroid fibration by

* {#BZ} Olivier Brahic, [[Chenchang Zhu]], _Lie algebroid fibrations_, Adv. Math. 226 (2011), no. 4, 3105&#8211;3135, [arXiv:1001.4904](http://arxiv.org/abs/1001.4904). 

A description of Lie integration with values in [[smooth ∞-groupoids]] regarded as [[simplicial presheaves]] on [[CartSp]] (and further the Lie integration of [[infinity-Lie algebra cohomology|L-infinity cocycles]]) is in

* {#FSS12} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_, Advances in Theoretical and Mathematical Physics, Volume 16 Issue 1 (2012), pages 149-250 ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735))

Essentially the same integration prescription is considered in 

* {#Roytenberg09} [[Dmitry Roytenberg]], _Differential graded manifolds and associated stacks: an overview_ ([pdf](https://sites.google.com/site/dmitryroytenberg/unpublished/dg-stacks-overview.pdf))



The Lie integration- of [[Lie infinity-algebroid representation|Lie algebroid representations]] $\mathfrak{a} \to end(V)$ to morphisms of [[∞-categories]] $A \to Ch_\bullet^\circ$ / [[higher parallel transport]] is discussed in

* [[Camilo Arias Abad]], [[Florian Schätz]], _The $A_\infty$ de Rham theorem and integration of representations up to homotopy_ ([arXiv:1011.4693](http://arxiv.org/abs/1011.4693))

Application to the problem of Lie integrating ordinary but infinite-dimensional Lie algebras is in 

* [[Christoph Wockel]], [[Chenchang Zhu]], _Integrating central extensions of Lie algebras via Lie 2-groups_ ([arXiv:1204.5583](http://arxiv.org/abs/1204.5583))

A generalization of [[Lie integration]] to conjectural Leibniz groups has been conjectured by [[J-L. Loday]]. A local version via local Lie [[rack]]s has been proposed in

* Simon Covez, _The local integration of Leibniz algebras_, [arXiv:1011.4112](http://arxiv.org/abs/1011.4112); _On the conjectural cohomology for groups_, [arXiv:1202.2269](http://arxiv.org/abs/1202.2269); 
_L'int&#233;gration locale des alg&#232;bres de Leibniz_, Thesis (2010), [pdf](http://tel.archives-ouvertes.fr/docs/00/49/54/69/PDF/THESE_Simon_Covez.pdf)

Integration from Lie algebroids to groupoids is also studied in the dual language and generality of integration of Lie-Reinhart algebras
and commutative Hopf algebroids,

* Alessandro Ardizzoni, Laiachi El Kaoutit, Paolo Saracco, _Towards differentiation and integration between Hopf algebroids and Lie algebroids_, [arXiv:1905.10288](https://arxiv.org/abs/1905.10288)

[[!redirects Lie integrations]]

[[!redirects higher Lie integration]]
[[!redirects higher Lie integrations]]

category: Lie theory