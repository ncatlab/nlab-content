
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


This is a sub-entry of [[Smooth∞Grpd]]. See there for background.

--

#Contents#
* table of contents
{:toc}

## Structures

We discuss the general abstract 
<a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">structures in a cohesive (∞,1)-topos</a> realized in [[Smooth∞Grpd]].



### Geometric homotopy and Galois theory     
  {#StrucGeometricHomotopy}



We discuss the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Homotopy">intrinsic fundamental ∞-groupoid</a> construction realized in $Smooth \infty Grpd$.


+-- {: .num_prop #UnderlyingSimplicialTopologicalSpace}
###### Proposition

If $X \in Smooth\infty Grpd$ is presented by 
$X_\bullet \in SmoothMfd^{\Delta^{op}} \hookrightarrow [CartSp_{smooth}^{op}, sSet]$, then its image $i_!(X) \in $ [[ETop∞Grpd]] under the [relative topological cohesion morphism](#RelativeTopologicalCohesion) is presented by the underlying [[simplicial topological space]] 
$X_\bullet \in TopMfd^{\Delta^{op}} \hookrightarrow [CartSp_{top}^{op}, sSet]$.

=--

+-- {: .proof}
###### Proof

Let first $X \in SmoothMfd \hookrightarrow SmoothMfd^{\Delta^{op}}$ be simplicially constant. Then there is a differentiably [[good open cover]] $\{U_i \to X\}$ such that the [[Cech nerve]] projection

$$
  \left(
  \int^{[k] \in \Delta}
    \Delta[k] \cdot \coprod_{i_0, \cdots, i_k}
     U_{i_0} \times_X \cdots \times_X U_{i_k}
  \right)
   \stackrel{\simeq}{\to}
  X
$$

is a cofibrant [[resolution]] in $[CartSp_{smooth}^{op}, sSet]_{proj,loc}$ which is degreewise a [[coproduct]] of representables. That means that the left [[derived functor]] $\mathbb{L} Lan_i$ on $X$ is computed by the application of $Lan_i$ on this coend, which by the fact that this is defined to be the left [[Kan extension]] along $i$ is given degreewise by $i$, and since $i$ preserves [[pullback]]s along covers, this is

$$
  \begin{aligned}
    (\mathbb{L} Lan_i) X 
    & \simeq
    Lan_i 
    \left(
      \int^{[k] \in \Delta}
      \Delta[k] \cdot \coprod_{i_0, \cdots, i_k}
       U_{i_0} \times_X \cdots \times_X U_{i_k}
    \right)
    \\
    & = 
  \int^{[k] \in \Delta}
    \Delta[k] \cdot \coprod_{i_0, \cdots, i_k}
         Lan_i 
           (U_{i_0} \times_X \cdots \times_X U_{i_k})
   \\
    & \simeq
  \int^{[k] \in \Delta}
    \Delta[k] \cdot \coprod_{i_0, \cdots, i_k}
         i 
           (U_{i_0} \times_X \cdots \times_X U_{i_k})
   \\
    & \simeq
  \int^{[k] \in \Delta}
    \Delta[k] \cdot \coprod_{i_0, \cdots, i_k}
           (i(U_{i_0}) \times_{i(X)} \cdots \times_{i(X)} i(U_{i_k}))
   \\
   & \simeq i(X)
  \end{aligned}
  \,,
$$

The last step follows from observing that we have manifestly the [[Cech nerve]] as before, but now of the underlying [[topological space]]s of the $\{U_i\}$ and of $X$. 

The claim then follows for general simplicial spaces by observing that $X_\bullet = \int^{[k] \in \Delta} \Delta[k] \cdot X_k \in [CartSp_{smooth}^{op}, sSet]_{proj,loc}$ presents the  [[(∞,1)-colimit]] over $X_\bullet : \Delta^{op} \to SmoothMfd \hookrightarrow Smooth \infty Grpd$ and the [[left adjoint|left]] [[adjoint (∞,1)-functor]] $i_!$ preserves these [[(∞,1)-colimit]]s. 

=--


+-- {: .num_prop}
###### Corollary

If $X \in Smooth\infty Grpd$ is presented by 
$X_\bullet \in SmoothMfd^{\Delta^{op}} \hookrightarrow [CartSp_{smooth}^{op}, sSet]$,
then the image of $X$ under the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]-functor

$$
  Smooth \infty Grpd \stackrel{\Pi}{\to}
  \infty Grpd
  \underoverset{|-|}{\simeq}{\to}
  Top
$$

is [[weak homotopy equivalence|equivalent to]] the [[geometric realization of simplicial topological spaces|geometric realization]] of (a Reedy cofibrant replacement of) the underlying [[simplicial topological space]]

$$
  |\Pi(X)| \simeq |Q X_\bullet|
  \,.
$$

In particular if $X$ is an ordinary [[smooth manifold]] then 

$$
  \Pi(X) \simeq Sing X
$$

is equivalent to the standard [[fundamental ∞-groupoid]] of $X$.

=--

+-- {: .proof}
###### Proof

By a [proposition above](#UnderlyingETopologicalInftyGroupoids) the functor $\Pi$ factors as $\Pi X \simeq \Pi_{ETop} i_! X$. By the 
[above proposition](#UnderlyingSimplicialTopologicalSpace) this is $\Pi_{Etop}$ applied to the underlying [[simplicial topological space]]. The claim then follows with the [corresponding proposition](#http://ncatlab.org/nlab/show/Euclidean-topological+infinity-groupoid#GeometricHomotopy) discussed at [[ETop∞Grpd]].

=--

+-- {: .num_prop}
###### Corollary

The $\Pi : \mathrm{Smooth}\infty\mathrm{Grpd} \to \infty \mathrm{Grpd}$
preserves [[homotopy fiber]]s of morphisms that are presented in 
  $[\mathrm{CartSp}_{\mathrm{smooth}}^{\mathrm{op}}, \mathrm{sSet}]_{\mathrm{proj}}$ by morphisms
of the form $X \to \bar W G$ with $X$ fibrant and $G$ a simplicial group in
[[SmoothMfd]].

=--

+-- {: .proof}
###### Proof


 By the above the functor factors as

$$
  \Pi_{\mathrm{Smooth}} \simeq \Pi_{\mathrm{ETop}} \circ i_!
  \,.
$$
 
and  $i_!$ assigns the underlying  topological spaces. If we can show that this preserves the homotopy fibers in question, then 
the claim follows with the analogous discussion at
[[ETop∞Grpd]].

We find this as in the proof of the latter proposition, by considering the pasting diagram of pullbacks of simplicial presheaves

$$
  \array{
    P' &\to& P &\to& W G
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Q X &\to& X &\to& \bar W G
   }
   \,.
$$

Since the component maps of the right vertical morphisms are surjective, the degreewise pullbacks in $\mathrm{SmoothMfd}$ that define $P'$ are all along [[transversal map]]s, and thus the underlying
objects in [[TopMfd]] are the pullbacks of the underlying topological manifolds.
Therefore the degreewise  forgetful functor $\mathrm{SmoothMfd} \to \mathrm{TopMfd}$ presents
  $i_!$ on the outer diagram and sends this homotopy pullback to a homotopy pullback.

=--


### Paths and geometric Postnikov towers

### Paths and geometric Postnikov towers
 {#PresentationOfPathGroupoid}

We discuss the notion of _[geometric path  ∞-groupoids](http://ncatlab.org/nlab/show/cohesive+%28infinity,1%29-topos+--+structures#Paths)_ realized in $Smooth\infty Grpd$.



+-- {: .num_defn }
###### Definition

For $X \in $ [[SmthMfd]] write

$$
  \mathbf{Sing} X  \in [CartSp^{op}, sSet]
$$ 

for the simplicial presheaf that sends a test space $U \in $ [[CartSp]] to the [[singular simplicial complex]] of smooth simplices smoothly parameterized over $U$:

$$
  \mathbf{Sing} X : (U,k) 
  \mapsto Hom_{SmthMfd}(U \times \Delta^k, X)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The object $\mathbf{Sing} X \in [CartSp^{op}, sSet]$ presents the abstractly defined [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] $\mathbf{\Pi}(X)$.

=--

+-- {: .proof}
###### Proof

Using the [[Steenrod-Wockel approximation theorem]] this comes down to the same argument as for [[Euclidean topological ∞-groupoid]]s. See _[Presentation of the path ∞-groupoid](http://ncatlab.org/nlab/show/Euclidean-topological+infinity-groupoid#PresentationOfPathGroupoid)_ there.

=--

### Concrete objects -- diffeological $\infty$-groupoids
 {#StrucConcreteObjects}

This section is at

* [[concrete smooth infinity-groupoid]].


### Geometry and structure sheaves {#StrucGeometry}

(...)


### Cohesive $\infty$-groups {#StrucInfinGroups}

We discuss <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#InfinGroups">cohesive ∞-groups</a> in $Smooth \infty Grpd$: smooth $\infty$-groups.




#### Lie groups 
 {#LieGroups}

Let $G$ be a [[Lie group]]. Under the [embedding](#SmoothManifoldEmbeds) 
$SmoothMfd \hookrightarrow Smooth \infty Grpd$ this is canonically identifed as a  [[0-truncated]] [[∞-group]] object in $Smooth \infty Grpd$.
Write $\mathbf{B}G \in Smooth \infty Grpd$ for the corresponding 
[[delooping]] object.


+-- {: .num_prop #DeloopedLieGroup}
###### Proposition

A fibrant presentation of the [[delooping]] object $\mathbf{B}G$
in the projective local [[model structure on simplicial presheaves]]
$[CartSp^{op}_{smooth}, sSet]_{proj, loc}$ 
is given by the [[simplicial presheaf]] that is the [[nerve]]
of the one-object [[Lie groupoid]]

$$
  \mathbf{B}G_c := (G \stackrel{\to}{\to} * ) 
$$

regarded as a [[simplicial manifold]] and canonically embedded into 
simplicial presheaves:

$$
  \mathbf{B}G_c : U \mapsto N(C^\infty(U,G) \stackrel{\to}{\to} *)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The presheaf is clearly objectwise a [[Kan complex]], being objectwise
the nerve of a groupoid. It satisfies [[descent]] along [[good open cover]]s
$\{U_i \to \mathbb{R}^n\}$ of [[Cartesian space]]s, because the [[descent]] $\infty$-groupoid $[CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}G)$ is $\cdots \simeq G Bund(\mathbb{R}^n) \simeq G TrivBund(\mathbb{R}^n)$: an object is a [[Cech cohomology|Cech]]
1-cocycle with coefficients in $G$, a morphism a Cech coboundary, which yields the groupoid of $G$-[[principal bundle]]s over $U$, which for the [[Cartesian space]] $U$ is however equivalent to the groupoid of trivial $G$-bundles over $U$.

To show that $\mathbf{B}G$ is indeed the [[delooping]] object of $G$
it is sufficient (by the discussion at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#HomotopyLimits">model structure on simplicial presheaves -- homotopy limits</a>)
to compute the [[(∞,1)-pullback]] 
$G \simeq * \times_{\mathbf{B}G} *$ in the global model structure $[CartSp^{op}, sSet]_{proj}$.

This is accomplished by the ordinary [[pullback]] of the 
fibrant replacement diagram 

$$
  \array{
    G &\to& N(G\times G \stackrel{\overset{p_1 \cdot p_2}{\to}}{\underset{p_1}{\to}} G)
    \\
    \downarrow && \downarrow^{\mathrlap{p_2}}
    \\
    * &\to& N(G \stackrel{\to}{\to} *)
  }
$$

as discussed at [[universal principal ∞-bundle]].

=--


#### Strict Lie 2-groups
  {#StrictLie2Groups}

Let now $G = \Xi[G_2 \to G_1]$ be a strict [[Lie 2-group]] coming from a smooth  [[crossed module]] $G_2 \stackrel{\delta}{\to} G_1 $ with action $\alpha : G_1 \to Aut(G_2)$.


+-- {: .num_prop }
###### Proposition

A fibrant representative of $\mathbf{B}G$ in $[CartSp^{op}, sSet]_{proj,cov}$ is given by the [[crossed complex]]

$$
  \Xi[G_2 \to G_1 \stackrel{\to}{\to} *]
  \,.
$$

=--

+-- {: .proof}
###### Proof

As [above](#LieGroupsDelooping) for Lie groups.

=--



#### Circle Lie $n$-groups {#CircleLienGroup}

+-- {: .num_defn }
###### Definition

Write equivalently

$$
  U(1) = S^1 = \mathbb{R}/\mathbb{Z}
$$ 

for the [[abelian group|abelian]] [[Lie group]] called the 
_[[circle group]]_ or _1-dimensional [[unitary group]]_ , regarded as a [[0-truncated]] [[∞-group]] object in $Smooth\infty Grpd$ under the [embedding](#SmoothManifoldEmbeds) $SmoothMfd \hookrightarrow Smooth \infty Grpd$.

For $n \in \mathbb{N}$ the $n$-fold [[delooping]] $\mathbf{B}^n U(1) \in Smooth \infty Grpd$ we call the **[[circle n-group|circle Lie (n+1)-group]]**.

=--

Write 

$$
  U(1)[n] := [\cdots \to 0 \to C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
  \in
  [CartSp^{op}, Ch^+_\bullet]
$$

for the [[chain complex]] of sheaves concentrated in degree $n$ on $U(1)$.

Recall the right Quillen functor $\Xi : [CartSp^{op}, Ch_\bullet^+] \to [CartSp^{op}, sSet]$ from [above](#DoldKanInclusion).

+-- {: .num_prop }
###### Proposition

The [[simplicial presheaf]] $\Xi(U(1)[n]) \in [CartSp^{op}, sSet]$ is a fibrant representative in $[CartSp^{op},sSet]_{proj,loc}$
of the circle Lie $(n+1)$-group $\mathbf{B}^n U(1)$.

=--

+-- {: .proof}
###### Proof

First notice that since $U(1)[n]$ is fibrant in 
$[CartSp_{smooth}^{op}, Ch_\bullet]_{proj}$ we have that
$\Xi U(1)[n]$ is fibrant in $[CartSp^{op}, sSet]_{proj}$. 
We may compute the [[homotopy pullback]] that defines the [[loop space object]] in the global model structure (by the discussion at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#HomotopyLimits">model structure on simplicial presheaves -- homotopy (co)limits</a>) we may check the statement about the delooping in the global model structure.

Consider the global fibration [[resolution]] of the point inclusion $* \to \Xi(U(1)[n])$ given by

$$
  \array{
    \Xi [C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    \\
    \downarrow
    \\
    \Xi [C^\infty(-,U(1)) \to 0  \to 0 \to \cdots \to 0]
  }
  \,.
$$ 

The underlying morphism of chain complexes is clearly degreewise surjective, hence a projective fibration, hence its image under $\Xi$ is a projective fibration. Therefore the [[homotopy pullback]] in question is 
given by the ordinary [[pullback]]

$$
  \array{
    \Xi[0 \to C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    &\to&
    \Xi [C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
    \\
    \downarrow && \downarrow
    \\
    \Xi [0 \to 0  \to 0 \to \cdots \to 0]
    & \to &
    \Xi [C^\infty(-,U(1)) \to 0  \to 0 \to \cdots \to 0]
  }
  \,,
$$ 

computed in $[CartSp^{op}, Ch_\bullet]$ and then using that 
$\Xi$ is the [[right adjoint]] and hence preserves pullbacks. This shows that the loop object $\Omega \Xi(U(1)[n])$ is indeed presented by 
$\Xi (U(1)[n-1])$.


Now we discuss the fibrancy of $U(1)[n]$ in the local model structure $[CartSp^{op}, sSet]_{proj,loc}$. We need to check that for all [[good open cover]]s $\{U_i \to U\}$ of a [[Cartesian space]] $U$ we have that the mophism

$$
  C^\infty(U,U(1))[n] \to [CartSp^{op}, sSet](C(\{U_i\}), \Xi U(1)[n])
$$

is an equivalence of Kan complexes, where $C(\{U_i\})$ is the [[Cech nerve]] of the cover. Observe that the Kan complex on the right is that whose vertices are [[cocycle]]s in degree-$n$ [[Cech cohomology]] (see there for details) with coefficients in $U(1)$ and whose morphisms are coboundaries between these.

We proceed by induction on $n$. For $n = 0$ the condition is just that $C^\infty(-,U(1))$ is a [[sheaf]], which clearly it is.
For general $n$ we use that since $C(\{U_i\})$ is cofibrant, the above is the [[derived hom-space]] functor which commutes with [[homotopy pullback]]s and hence with forming [[loop space object]]s, so that

$$
  \pi_1 [CartSp^{op}, sSet](C(\{U_i\}), \Xi (U(1)[n]))
  \simeq
  \pi_0 [CartSp^{op}, sSet](C(\{U_i\}), \Xi (U(1)[n-1]))
$$

by the above result on delooping. So we find that for all $0 \leq k \leq n$ that $\pi_k [CartSp^{op}, sSet](C(\{U_i\}), \Xi(U(1)[n]))$ is the [[Cech cohomology]] of $U$ with coefficients in $U(1)$ in degree $n-k$.
By standard facts about [[Cech cohomology]] (using the [[short exact sequence]] of abelian groups $\mathbb{Z} \to U(1)\to \mathbb{R}$ and the fact that the cohomology with coefficients in $\mathbb{R}$ vanishes in positive degree, for instance by a [[partition of unity]] argument) we have that this is given by the [[integral cohomology]] groups

$$
  \pi_0 [CartSp^{op}, sSet](C(\{U_i\}), \Xi (U(1)[n]))
  \simeq
  H^{n+1}(U, \mathbb{Z})
$$ 

for $n \geq 1$. For the [[contractible]] [[Cartesian space]] all these cohomology groups vanish.

So we have that $\Xi(U(1)[n])(U)$ and $[CartSp^{op}, sSet](C(\{U_i\}), \Xi U(1)[n])$ both have homotopy groups concentrated in degree $n$ on $U(1)$. The above looping argument together with the fact that $U(1)$ is a sheaf also shows that the morphism in question is an isomorphism on this degree-$n$ homotopy group, hence is indeed a [[weak homotopy equivalence]].

=--

+-- {: .num_remark}
###### Remark

In the equivalent presentation of $Smooth\infty Grpd$ by simplicial presheaves on all of [[SmoothMfd]] the objects $\Xi U(1)[n]$ are far from being locally fibrant. Instead, their local fibrant replacements are given by the $n$-stacks of [[circle n-bundle with connection|circle n-bundle]]s.

=--




#### Simplicial Lie groups {#SimplicialSmoothGroups}

Every [[connected]] object $X \in \infty Lie Grpd$ is -- by definition -- the [[delooping]] $X = \mathbf{B}G$ of a Lie [[∞-group]] $G = \Omega X$, its [[loop space object]] formed in $\infty LieGrpd$. Since the discussion of [[group object in an (infinity,1)-category|group objects]], [[loop space  object]]s etc. involves only finite [[limit in a quasi-category|(∞,1)-limits]] and [[∞-stackification]] preserves these, this may be discussed in the [[(∞,1)-category of (∞,1)-presheaves]] on [[CartSp]]. Since there $(\infty,1)$-limits are computed objectwise, an [[∞-group]] object $G$ in $\infty LieGrpd$ is modeled by a [[(∞,1)-presheaf]] with values in [[∞-group]]s in [[∞Grpd]].

By standard results on <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity,1)-category#ModelsInInfGrpd">Models for group objects in ∞Grpd</a> the latter may equivalently be modeled by [[simplicial group]]s. A simplicial group is possibly weak [[∞-groupoid]] equipped with a _strict_ group object structure. While [[strict omega-groupoid|strict ∞-groupoids]] with weak group object structure do not model all [[∞-group]]s, weak $\infty$-groupoids with strict group structure do.

There is a good supply of standard results for and constructions with [[simplicial group]]s which makes this model useful for applications.



### Cohomology and principal $\infty$-bundles {#StrucCohomology}{#Cohomology}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#Cohomology">intrinsic cohomology and pricipal ∞-bundles</a> in $Smooth \infty Grpd$.


#### Cohomology with constant coefficients
  {#CohomologyWithConstantCoefficients}

+-- {: num_defn }
###### Definition

Let $A \in $ [[∞Grpd]] be any [[discrete ∞-groupoid]]. Write $|A| \in $ [[Top]] for its [[geometric realization]]. For $X$ any [[topological space]], the [[nonabelian cohomology]] of $X$ with coefficients in $A$ is the set of [[homotopy]] classes of maps $X \to |A|$

$$ 
  H_{Top}(X,A) := \pi_0 Top(X,|A|)
  \,.
$$

We say $Top(X,|A|)$ itself is the [[cocycle]] [[∞-groupoid]] for $A$-valued [[nonabelian cohomology]] on $X$.

Similarly, for $X, \mathbf{A} \in Smooth \infty Grpd$ two smooth $\infty$-groupoids, write

$$
  H_{Smooth}(X,\mathbf{A}) := \pi_0 Smooth\infty Grpd(X,\mathbf{A})
$$

for the intrinsic [[cohomology]] of $Smooth \infty Grpd$ on $X$ with coefficients in $\mathbf{A}$.

=--


+-- {: .num_prop }
###### Proposition

Let $A \in $ [[∞Grpd]], write $Disc A \in Smooth \infty Grpd$ for the corresponding [[discrete ∞-groupoid|discrete smooth ∞-groupoid]]. Let $X \in SmoothMfd \stackrel{i}{\hookrightarrow} Smooth \infty Grpd$ be a [[paracompact topological space]] regarded as a 0-[[truncated]] 
Euclidean-topological $\infty$-groupoid. 

We have an [[isomorphism]] of cohomology sets

$$ 
  H_{Top}(X,A) \simeq H_{Smooth}(X,Disc A)
$$

and in fact an [[equivalence in an (∞,1)-category|equivalence]] of [[cocycle]] [[∞-groupoid]]s

$$
  Top(X,|A|) \simeq Smooth\infty Grpd(X, Disc A)
  \,.
$$

More generally, for $X_\bullet \in SmoothMfd^{\Delta^{op}}$ 
presenting an object in $Smooth \infty Grpd$ we have

$$
  H_{Smooth}(X_\bullet, Disc A)
  \simeq
  H_{Top}(|X|, |A|)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows from the $(\Pi \dashv Disc)$-[[adjunction]] and the [above proposition](#StrucGeometricHomotopy) asserting that $|\Pi(X_\bullet)| \simeq |X_\bullet|$ is the ordinary [[geometric realization of simplicial topological spaces]].

=--



#### $G$-Principal bundles for $G$ a Lie group


Let $G$ be a Lie group, regarded as a group object in $Smooth \infty Grpd$
as in the [above discussion](#LieGroups).

The [[universal principal ∞-bundle|universal G-principal bundle]] is a replacement of the point inclusion $* \to \mathbf{B}G$ by a fibration $\mathbf{E}G \to \mathbf{B}G$.

For $G$ an ordinary [[group]] one model for this is given by the Lie groupoid

$$
  \mathbf{E}G = (G\times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G)
  \,,
$$

which is the [[action groupoid]] $G//G$ of $G$ acting on itself.

One noteworthy aspect of this object is that it is itself groupal, in fact itself a Lie [[strict 2-group]] in a way that is compatible with the canonical inclusion $G \to \mathbf{E}G$: it is an example of a [[groupal model for universal principal ∞-bundles]].

To emphasize this group structure, we also write $INN(G)$ for this groupoid, following [SchrRob](#http://arxiv.org/abs/0708.1741). The corresponding [[crossed module]] is

$$
 [INN(G)] = (G \stackrel{Id}{\to} G)
 \,.
$$

Accordingly we write $\mathbf{B E}G$ or $\mathbf{B}INN(G)$ for the 2-groupoid given by the Lie [[crossed complex]]

$$
  (G \stackrel{Id}{\to}G \stackrel{\to}{\to} * ) 
  \,.
$$




The following proposition asserts that the general definition of [[principal ∞-bundle]]s in an [[(∞,1)-topos]] $\mathbf{H}$ applied to the coefficient object $\mathbf{B}G$ in $\mathbf{H} = \infty LieGrpd$ for $G$ a [[Lie group]] does reprpduce the ordinary notion of $G$-[[principal bundle]]s.

+-- {: num_prop }
###### Proposition

Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]]. The ordinary first [[nonabelian cohomology]] of $X$ with coefficients in $G$ coincided with the intrinsic [[cohomology]] of $\infty Lie Grpd$

$$
  H^1(X,G) \simeq \pi_0 \infty LieGrpd(X, \mathbf{B}G)
$$

and the $G$-[[principal bundle]] $P \to X$ corresponding to a [[cocycle]] $X \to \mathbf{B}G$ in $\infty LieGrpd$ is indeed the [[homotopy fiber]] of that cocycle.

=--

+-- {: .proof}
###### Proof

By the discussion at [[model structure on simplicial presheaves]] we have that a cofibrant [[resolution]] for $X$ in the model $[CartSp^{op}, sSet]_{proj,cov}$ for $\infty LieGrpd$ is civen by the [[Cech nerve]] $C\{U_i\}$ of a [[good open cover]] $\{U_i \to X\}$. It follows that $\pi_0 \infty LieGrpd(X,\mathbf{B}G)$ is the [[Cech cohomology]] of $X$ with coefficients in $G$ (see there for details).

Concretely, a cocycle 

$$
  g : C(\{U_i\}) \to \mathbf{B}G
$$

is canonically identified with a transition function

$$
  g : \coprod_{i,j} U_i \cap U_j \to G
$$

satisfying on $U_i \cap U_j \cap U_k$ the cocycle condition $g_{i j} g_{j k} = g_{i k}$.

From this we can compute the [[homotopy fiber]] of $g : C(\{U_i\}) \to \mathbf{B}G$ by forming the ordinary [[pullback]] of the fibrant replacement $\mathbf{E}G \to \mathbf{B}G$ of the point inclusion $* \to \mathbf{B}G$, where $\mathb{E}G = \mathbf{B}G^{I} \times_{\mathbf{B}G} *$ is the smooth groupoid

$$
  \mathbf{E}G
  = 
  \left\{
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_1}}\swarrow && \searrow^{\mathrlap{g_2}}
       \\
       * &&\stackrel{h}{\to}&& *
    }
    \;\;|
    \;\;
    g_1,g_2,h \in G, g_2 = h g_1
  \right\}
  \,.
$$

From this we find the pullback $\hat P$ in


$$
  \array{
    \hat P &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

to be the smooth Lie groupoid

$$
  \hat P
  =
  \left(
  \coprod_{i,j} U_i\cap U_j \times G
  \stackrel{\overset{p_2 \times g_{i,j} \cdot p_3}{\to}}{\underset{p_1 \times P_3}{\to}}
  \coprod_{i} U_i \times G
  \right)
$$

i.e.

$$
  \hat P
  = 
  \left\{
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_1}}\swarrow && \searrow^{\mathrlap{g_2}}
       \\
       * &&\stackrel{g_{i j}(x)}{\to}&& *
       \\
       \\
       (x,i) &&\to&& (x,j)  
    }
  \right\}
  \,.
$$

The evident projection $\hat P \to P$ is objectwise a surjective and full and faithful functor.

=--










#### Cohomology of Lie groups {#CohomologyOfLieGroups}

We consider the cohomology in $\mathbf{H}$ of smooth [[delooping]] groupoids $\mathbf{B}G$ for $G$ an ordinary [[Lie group]]. This is a form of [[group cohomology]] for Lie groups.

$$
  H^n(G,A) := \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n A)
  \,.
$$

We discuss how this relates to other definitions of <a href="http://ncatlab.org/nlab/show/group+cohomology#LieGroupcohomology">Lie group cohomology</a> in the literature.

+-- {: .num_defn}
###### Definition
**(naive Lie group cohomology)**

For $G$ a Lie group and $A$ an abelian Lie group and $n \in \mathbb{N}$ define $H^n_{rest}(G,A)$ to be the group of equivalence classes of cocycles given by [[smooth function]]s $G^\times_n \to A$ by coboundatries given by smooth functions $G^{\times_{n-1}} \to A$ subject to the usual relations.

=--

Observe that with $\mathbf{B}G = G^{\times_\bullet}$ regarded as an object of $sPSh(CartSp)$, this is

$$
  H^n_{rest}(G,A)
  =
  \pi_0 sPSh(\mathbf{B}G, \mathbf{B}^n A)
  \,.
$$

Written this way it is evident that this definition misses to take into account any cofibrant replacement of $\mathbf{B}G$. 

A more refined definition of cohomology of Lie groups has been given by ([Segal](#Segal)), which was later rediscovered by ([Brylinski](#Brylinski)), following ([Blanc](#Blanc)). A review is in section 4 of ([Schommer-Pries](#SchommerPries)).


+-- {: .num_defn}

###### Definition
**(differential Lie group cohomology)**

Let $G$ be a [[paracompact space|paracompact]] [[Lie group]] and $A$ an abelian Lie group.

For eack $k \in \mathbb{N}$ we can pick a [[good open cover]] $\{U^{k}_{i} \to G^{\times_k}| i \in I_k\}$ such that

* the index sets arrange themselves into a [[simplicial set]]
  $I : [k] \mapsto I_k$;

* and for $d_j(U^k_i)$ and $s_j(U^k_i)$ the images of the
  face and degeneracy maps of $G^{\times\bullet}$ we have

  $$
    d_j(U^k_i) \subset U^{k-1}_{d_j(i)}
  $$ 

  and

  $$
    s_j(U^k_i) \subset U^{k+1}_{s_j(i)}
    \,.
  $$

For instance start with a [[good open cover]] $\{U^1_i \to G\}$ and define a good open cover $\{U^2_{i_0 i_1 i_2}\}$ of $G \times G$ by $U^2_{i_0 i_1 i_2} := d_0^* U^1_{i_0} \cap d_1^* U^1_{i_1} \cap d_2^* U^1_{i_2}$. And so on.

Then the **<a href="http://ncatlab.org/nlab/show/group+cohomology#LieGroupcohomology">differentiable Lie group cohomology</a>** $H^\bullet_{diffr}(G,A)$ of $G$ with coefficients in 
$A$ is the cohomology of the total complex of the [[Cech cohomology|Cech]]
double complex $C^\infty( U^{\bullet}_{i_0, \cdots, i_\bullet} , A)$
whose differentials are the alternating sums of the face maps 
of $G^{\times_\bullet}$ and of the [[Cech nerve]]s, respectively:

$$
  H^n_{diff}(G,A) := H^n Tot C^\infty( U^{\bullet}_{i_0, \cdots, i_\bullet} , A)
$$


=--

This is ([Brylinski, definition 1.1](#Brylinski)).

As discussed there, this is equivalent to other definitions, notably to a definition given earlier in ([Segal](#Segal)). 


+-- {: .num_lemma}
###### Observation

There is a natural map

$$
  H^n_{restr}(G,A) \to H^n_{diffr}(G,A)
$$

obtained by pulling back globally defined cocycles and coboundaries to good covers.

=--

We can understand this differentiable Lie group cohomology in terms of maps out of a certain resolution of $\mathbf{B}G$ in $sPSh(CartSp)_{proj,cov}$:

+-- {: .num_prop}
###### Proposition

For $\{U^\bullet_{i_\bullet}\}$ a system of [[good open cover]]s as above, we obtain a simplicial diagram of [[Cech nerve]]s 

$$
  C : [k] \mapsto C(\{U^k_{i}\})
$$

which is degreewise a cofibrant resolution on $sPSh(CartSp)_{proj,cov}$ of $G^{\times_n}$. Its [[bisimplicial set|totalization]] [[coend]] is connected by a zig-zag of weak equivalences in $sPSh(CartSp)_{proj,cov}$ to $\mathbf{B}G$

$$
  \mathbf{B}G
  \stackrel{\simeq}{\leftarrow}
  \stackrel{\simeq}{\to}
  \int^{[k]} \Delta[k] \cdot C(\{U^k_i\})
$$

and we have

$$
  H^n_{diffr}(G,A)
  =
  \pi_0 sPSh(CartSp)(\int^{[k]} \Delta[k] \cdot C(\{U^k_i\}), \mathbf{B}^n A)
  \,.
$$

=--

The proof of this will also show the following

+-- {: .num_prop}
###### Proposition

Write $H^\bullet(G,A) := \pi_0 Sh_{(\infty,1)}(CartSp)(\mathbf{B}G, \mathbf{B}^n A)$ for the intrinsic cohomology of $\mathbf{B}G$ regarded as an object of the $(\infty,1)$-topos of $\infty$-Lie groupoids.

There is a natural morphism

$$
  H^n_{diffr}(G,A) \to H^n(G,A)
  \,.
$$

=--



+-- {: .proof}
###### Proof

Since $\mathbf{B}^n A$ does satisfy descent with respect to [[good open cover]]s of [[Cartesian space]]s (every $(n-1)$ $A$-[[bundle gerbe]] over an $\mathbb{R}^n$ is trivializable), to compute the intrinsic cohomology we have to find a cofibrant replacement for $\mathbf{B}G$.

A cofibrant replacement of any paracompact [[manifold]] $X$ in $[CartSp^{op}, sSet]_{proj,cov}$ is given by the [[Cech nerve]] $C(\{U_i\}) \stackrel{\simeq}{\to} X$ of a [[good open cover]] $\{U_i \to X\}$, because this is evidently a [[local epimorphism]] as described at <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CechLocalization">model structure on simplicial presheaves - Cech localization</a>.

Therefore from a choice of compatible families of open covers 
$\{U^k_i \to G^{\times k}\}$ as in the definition of differentiable group cohomology above, we obtain cofibrant replacements

$$
  C(\{U^k_i\}) \stackrel{\simeq}{\to} G^{\times_k}
$$

for each $k$, and arranging themselves into a simplicial simplicial presheaf

$$
  C(\{U^\bullet_i\}) : \Delta^{op} \to [CartSp^{op}, sSet]
  \,,
$$

which is cofibrant in the injective [[model structure on functors]] 
$[\Delta^{op}, [CartSp^{op}, sSet]_{proj,cov}]_{inj}$.

Observe that the fact that this is inded a simplicial diagram in $sPSh(CartSp)$ is due to the extra compatibility condition in the above definition of differentiable Lie group cohomology.

Notice from the discussion at [[model structure on simplicial presheaves]] that we have canonically another cofibrant replacement $Q (G^{\times_n})$ of $G^{\times_n}$ in $[CartSp^{op}, sSet]_{proj}$ which is functorial and has the special property that the [[bisimplicial set|diagonal]]

$$
  \int^{[k] \in \Delta}
  \Delta[k] \cdot Q(G^{\times_k})
  \stackrel{\simeq}{\to}
  \mathbf{B}G
$$

is a cofibrant replacement of $\mathbf{B}G$. Notice that in $[\Delta^{op}, [CartSp^{op}, sSet]_{proj}]_{inj}$ we therefore have a zig-zag of weak equivalences

$$
  C(\{U^\bullet_i\}) \stackrel{\simeq}{\to}
  \stackrel{\simeq}{\leftarrow}
  Q(G^{\times_\bullet})
$$

between cofibrant replacements of $G^{\times_\bullet}$.

Write $\mathbf{\Delta}^\bullet : \Delta \to sSet : [k] \mapsto N(\Delta/[k])$ for the standard [[Bousfield-Kan map|Bousfield-Kan]] cofibrant replacement of the point, hence also of $\Delta$, in $[\Delta, sSet_{Quillen}]_{proj}$ (more discussion of this is at [[homotopy colimit]]).

Then by the fact that the [[coend]] 

$$
  \int (-)\otimes (-) : [\Delta,sSet_{Quillen}]_{proj} \times [\Delta^{op}, [CartSp^{op}, sSet_{Quilen}]_{proj,cov}]_{inj}
  \to 
  [CartSp^{op}, sSet_{Quillen}]_{proj,cov}
$$

over the [[copower|tensoring]] $\otimes sSet_{Quillen} \times [CartSp^{op}, sSet_{Quillen}]_{proj,cov} \to [CartSp^{op}, sSet_{Quillen}]_{proj,cov}$ is a left [[Quillen bifunctor]] (as discussed there), we have weak equivalences in $[CartSp^{op}, sSet]_{proj,cov}$

$$
  \mathbf{B}G
  =
  \int^{[k] \in \Delta}
   \Delta[k] \cdot G^{\times_n}
   \stackrel{\simeq}{\leftarrow}
  \int^{[k] \in \Delta} \Delta[k] \cdot Q(G^{\times_k}))  
   \stackrel{\simeq}{\leftarrow}
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot Q(G^{\times_k}))  
  \stackrel{\simeq}{\to}
  \stackrel{\simeq}{\leftarrow}
  \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot C(\{U^k_i\}))  
  \stackrel{\simeq}{\to}
  \int^{[k] \in \Delta} \Delta[k] \cdot C(\{U^k_i\}))  
$$

where

* the first one is Dugger's cofibrant replacement mentioned above, even a global weak equivalence;

* the second one is objectwise the [[Bousfield-Kan map]], hence also even a global weak equivalence;

* the zig-zag is the image under the left Quillen functor $\int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot (-)$ (using that $\mathf{\Delta}$ is cofibrant) of the above zig-zag of weak equivalences between cofibrant objects;

* the last one is again the global weak equivalence coming objectwise from the [[Bousfield-Kan map]].

This shows the first claim, that $\mathbf{B}G \stackrel{\simeq}{\leftarrow}\stackrel{\simeq}{\rightarrow} \int^{k} \Delta[k] \cdot C(\{U^k_i\})$.

Moreover, again by the left Quillen bifunctor property of $\int(-)\cdot(-)$ we have that $\int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot C(\{U^k_i\}))$ is cofibrant. Therefore the intrinsic cohomology $H^n(G,A)$ is

$$
  \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n A)
  =
  [CartSp^{op}, sSet]_{proj,cov}
  \left(
    \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot C(\{U^k_i\}))
    ,
    \mathbf{B}^n A
  \right)
  \,.
$$

By pullback along the [[Bousfield-Kan map]] $\mathbf{\Delta[k]} \to \Delta[k]$ we have a natural morphism

$$
  \pi_0 sPSh(\int^{[k]} \Delta[k]\cdot C(\{U^k_i\}), \mathbf{B}^n A) \to H^n(G,A)
  \,.
$$

It remains to show that the set on the left is the differentiable Lie group cohomology.

For that observe that $\mathbf{B}^n A$ is in the image of the [[Dold-Kan correspondence]] $\Xi : [CartSp^{op}, Ch_\bullet] \to [CartSp^{op}, sAb] \stackrel{U}{\to} [CartSp^{op}, sSet]$ of the chain-complex valued presheaf $A[n] = A \otimes_\mathbb{Z} \mathbb{Z}[n]$ to reduce the computation of this simplicial hom-complex to that of a cochain complex:

$$
  \begin{aligned}
    sPSh(K_\bullet, \Xi A[n])
    & \simeq
    \int_U sSet(K_\bullet(U) , U \Xi A(U)[n])
    \\
    & \simeq \int_U sAb(\mathbb{Z} K_\bullet(U), \Xi A(U)[n])
    \\
    &\simeq \int_U Ch_\bullet( C_\bullet(\mathbb{Z} K_\bullet(U)), A(U)\otimes_{\mathbb{Z}}\mathbb{Z}[n] )
    \\
    & \simeq \int_U Ch^\bullet( \mathbb{Z}[n], C^\bullet (Set(K_\bullet(U),A(U))))
    \\
    & \simeq Ch^\bullet (\mathbb{Z}[n], 
       \int_U C^\bullet(Set(K_\bullet(U),A(U)))
    \\
    & \simeq Ch^\bullet(\mathbb{Z}[n], C^\bullet( PSh(K_\bullet, A) )
  \end{aligned}
  \,.
$$

Setting here $K_\bullet = \int^{[k]} \Delta[k] \cdot C(\{U^k_i\})$ and using the [[Eilenberg-Zilber theorem]] to identify the [[Moore complex]] of the [[bisimplicial set|diagonal]] to the [[total complex]] of the double complex of Moore complexes, the claim follows.

=--

+-- {: .num_prop}
###### Proposition

For $G$ a [[Lie group]] and $A$ either 

1. a [[discrete group|discrete]] [[abelian group]];

1. the additive Lie group of [[real numbers]] $\mathbb{R}$;

the intrinsic cohomology of $G$ in $Smooth\infty Grpd$ coincides with the refined [[Lie group cohomology]] of ([Segal](#Segal)/[Brylinski](#Brylinski))

$$
  H^n_{Smooth\infty Grpd}(\mathbf{B}G, A) \simeq H^n_{Segal}(G,A)
  \,.
$$

In particular we have in general

$$
  H^n_{Smooth\infty Grpd}(\mathbf{B}G, \mathbb{Z})
  \simeq
  H^{n}_{top}(B G, \mathbb{Z})
$$

and for $G$ [[compact topological space|compact]] also

$$
  H^n_{Smooth\infty Grpd}(\mathbf{B}G, U(1))
  \simeq
  H^{n+1}_{top}(B G, \mathbb{Z})
  \,.
$$

=--
  
+-- {: .proof}
###### Proof

The first statement is a special case of the [above proposition](#CohomologyWithConstantCoefficients) about cohomology with constant coefficients. 

The second statement is a special case of the more general statement that is proven at [[SynthDiff∞Grpd]].

The last statement follows then from the observation ([Brylinski](#Brylinski)) that $H^n_{diffr}(G,\mathbb{R}) \simeq H^n_{naive}(G,\mathbb{R})$ and the classical result ([Blanc](#Blanc)) that $H_{naive}^n(G,\mathbb{R}) = 0$ in positive degree, and using the [[fiber sequence]] induced from the [[short exact sequence]] of [[abelian group]]s $\mathbb{Z} \to \mathbb{R} \to \mathbb{R}/\mathbb{Z}$.

=--


#### Smooth principal 1-bundles and 2-bundles
 {#SmoothPrincipal1And2Bundles}

+-- {: .num_prop}
###### Proposition

Let $G$ be a [[Lie group]] and $\mathbf{B}G \in \mathbf{H} := \infty LieGrpd$ its [[delooping]] as discussed [above](LieGroups). Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]]. Then

$$
  \mathbf{H}(X,\mathbf{B}G)
  \simeq
  G Bund(X)
  \,.
$$

is equivalent to the groupoid of smooth $G$-[[principal bundle]]s on $X$. In particular

$$
  H^1_{Smooth}(X,G) \simeq \pi_0 \mathbf{H}(X,\mathbf{B}G)
$$

is the [[nonabelian cohomology|nonabelian]] smooth [[Cech cohomology]] of $X$ with coefficients in $G$. 

Analogously, let $G$ be a strict [[Lie 2-group]] such that $\pi_0 G$ is a [[smooth manifold]] and $G_0 \to \pi_0 G$ is a [[submersion]]. Then we have that

$$
  \mathbf{H}(X, \mathbf{B}G) \simeq G Bund(X)
$$

is the [[2-groupoid]] of $G$-[[principal 2-bundle]]s, whose connected components are given by first smooth [[nonabelian cohomology|nonabelian]] [[Cech cohomology]] $H^1_{Smooth}(X,G)$.

=--


+-- {: .proof}
###### Proof

The first case is a special case of the second, it is sufficient to consider that.

First we argue that $\mathbf{B}G$ is fibrant in 
$[CartSp^{op}, sSet]_{proj, loc}$, hence that for $\{U_i \to \mathbb{R}^n\}$ an [[open cover]] we have a weak equivalence

$$
  \mathbf{B}C^\infty(\mathbb{R}^n, G)
  \stackrel{\simeq}{\to}
  [CartSp^{op}, sSet](C(U), \mathbf{B}G)
  \,,
$$ 

for $C(U)$ the [[Cech nerve]] of the good cover. Since the [[site]] [[CartSp]] with good open cover coverage is a [[Verdier site]], it follows by the statements discussed at _[[hypercover]]_ that every hypercover has a refinement by a [[split hypercover]], which is a cofibrant [[resolution]] in $[CartSp^{op}, sSet]_{proj,loc}$. But also $C(U) \to X$ is a cofibrant resolution. Hence by the existence of the global model structure and using that $\mathbf{B}G$ is fibrant in $[CartSp^{op}, sSet]_{proj}$, it follows that 

$$
  \pi_0[CartSp^{op}, sSet](C(U), \mathbf{B}G)
  \simeq
  H^1(\mathbb{R}^n, G)
$$

is nonabelian degree 1 [[Cech cohomology]] on $\mathbb{R}^n$ with coefficients in the 2-group $G$. By ([NikolausWaldorf, prop. 4.1](#NikolausWaldorf)) this is the singleton set on the contractible $\mathbb{R}^n$. This shows that the [[descent]] morphism in quesion is an isomorphism on $\pi_0$.

Next, $\pi_1$ on the right is similarly the set of equivalence classes of $G_0//(G_0 \ltimes G_1)$-[[groupoid principal bundle]]s. The underlying $G_0 \times G_1$-[[principal bundle]] on the contractible $\mathbb{R}^n$ is trivializable, hence $\pi_1([CartSp^{op}, sSet](C(U), \mathbf{B}^g)) \simeq C^\infty(\mathbb{R}^n , G_0)$, and so we have also an isomorphism on $\pi_1$. Finally the isomorphism on $\pi_2$ is clear.

Now for $X$ an arbitrary paracompact [[smooth manifold]] and $U \to X$ a [[good open cover]], we have again that $C(U) \to X$ is a cofibrant resolution in the local model structure, hence hence by the above it follows that

$$
  Smooth \infty Grpd(X, \mathbf{B}G)
  \simeq
  [CartSp^{op}, sSet](C(U), \mathbf{B}G)
  \,.
$$

By the same argument about [[hypercover]]s on [[Verdier site]]s as above, it follows that the connected components of this are 

$$
  \pi_0 Smooth \infty Grpd(X, \mathbf{B}G)  
  \simeq
  H^1_{Smooth}(X, G)
  \,.
$$

=--

### Twisted cohomology
 {#StrucTwistedCohomology}

We discuss implementation in $Smooth \infty Grpd$ of the notion of 
<a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#TwistedCohomology">twisted cohomology in a cohesive (∞,1)-topos</a>.

* See [[twisted bundle]], [[twisted K-theory]].

* The definition of differential cohomology 
  [below](#StrucDifferentialCohomology) is an instance of 
  twisted cohomology, with the twist being given by 
  [[curvature characteristic form]]s.

### Concordance {#StrucConcordance}

(...)


### van Kampen theorem {#StrucVanKampen}

(...)

### Paths and geometric Postnikov towers {#StrucPaths}

(...)


### Universal coverings and geometric Whitehead towers {#StrucWhitehead} 

Given a [[Lie group]] $G$, we may regard it either as a [[topological group]] and form the [[classifying space]] $\mathcal{B}G \in $ [[Top]] $\simeq$ [[∞Grpd]], or we may form its [[delooping]] [[Lie groupoid]] $\mathbf{B}G \in \infty LieGrpd$, as discussed in the [section on Lie groups](#LieGroups) above.
By the discussion in the [section on geometric realization](#GeometricRealization) we have that under the canonical geometric realization functor

$$
  \Pi : \infty LieGrpd \to \infty Grpd \simeq Top
$$

we have

$$
  \mathcal{B}G \simeq \Pi(\mathbf{B}G)
  \,.
$$

Analogous statements hold for $\infty$-Lie groups. For instance by the same result we have that the [circle n-groupoid](#BnU1) $\mathbf{B}^n U(1)$ maps to the [[Eilenberg-MacLane space]]

$$
  \Pi(\mathbf{B}^n U(1)) \simeq K(\mathbb{Z}, n+1)
  \,.
$$

This means that given a [[cocycle]]

$$
  c : \mathcal{B}G \to K(\mathbb{Z},n+1)
$$

in [[integral cohomology]] (defining a [[characteristic class]]), it is of interest to ask of this morphism also lifts through $\Pi$ to a morphism

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)
  \,.
$$

Classes of examples of such lifts have been described in the section on [integration of ∞-Lie algebra cocycles](#IntegrationOfCocycles). 

By general reasoning, the extensions/[[principal ∞-bundle]]s classified by such cocycles are their [[homotopy fiber]]

$$
  \array{
     \mathbf{B}\hat G &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}G &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^n U(1)
  }
$$

in $\infty LieGrpd$ and

$$
  \array{
     \mathcal{B}\hat G &\to& *
     \\
     \downarrow && \downarrow
     \\
     \mathcal{B}G &\stackrel{c}{\to}& K(\mathbb{Z}, n)
  }
$$

in $Top \simeq \infty Grpd$. By the theorem discussed in the section on [Geometric realization](#GeometricRealization) we have that these two homotopy fibers correspond to each other under $\Pi : \infty LieGrpd \to \infty Grpd$:

$$
  \Pi(\mathbf{B}\hat G) \simeq \mathcal{B}\hat G
  \,.
$$

So this means with a smooth lift of a cocycle, we automatically obtain the corresponding  smooth lift of the extension that it classifies (assuming that the simplicial topological group $G$ is well-sectioned). This is notably useful for finding smooth lifts of [[Whitehead tower]]s. Examples of this we discuss in the following.


#### The smooth Whitehead tower of the orthogonal group

Let $O$ denote the [[orthogonal group]], regarded as a [[Lie group]]. We discuss steps of the [[Whitehead tower]] of $O$ refined to $\infty LieGrpd$.

##### First Stiefel-Whitney class

+-- {: .num_prop}
###### Proposition

A lift of the first [[Stiefel-Whitney class]] $w_1 : \mathcal{B}O \to K(\mathbb{Z}_2 ,1) \in Top \simeq \infty Grpd$ to $\infty LieGrpd$ is given by the morphism

$$
  \mathbf{w}_1 : \mathbf{B}O \to \mathbf{B}\mathbb{Z}_2
$$

of [[Lie groupoid]]s that is the delooping of the group homomorphism that sends $g \in O$ to its signature $\sigma(g) \in \mathbb{Z}_2$, where $\sigma(g) = 1$ if $g$ is in the connected component of $O$ (is orientation preserving as an orthogonal map) and $\sigma(g) = -1$ otherwise.

=--

We may compute the [[principal bundle]] in $\infty LieGrpd$ classified by $\mathbf{w}_1$ as the ordinry [[pullback]] of $\mathbf{E} \mathbb{Z}_2 \to \mathbf{B}\mathbb{Z}_2$, where $\mathbf{E}\mathbb{Z}_2$ is the groupoid $\mathbb{Z}_2 \times \mathbb{Z}_2 \stackrel{\ovserset{\cdot}{\to}}{\underset{p_1}{\to} \mathbb{Z}_2}$.

The resulting pullback groupoid

$$
  \array{
    Q &\to& \mathbf{E}\mathbb{Z}_2
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}O &\stackrel{\mathbf{w}_1}{\to}& \mathbf{B}\mathbb{Z}_2
  }
$$

has two objects, $s = +1,-1$ and morphisms of the form $s \stackrel{g}{\to} \sigma(g)\cdot s$ for $g \in O$. The smooth structure is that induced from $O$.

Evidently the canonical embedding $\mathbf{B} SO \to Q$ which sends a morphism $\bullet \stackrel{h}{\to} \bullet$ for $h \in SO$ an element of the [[special orthogonal group]] is an [[essentially surjective functor]] and a [[full and faithful functor]] and hence an equivalence of $\infty$-Lie groupoids. 

This establishes the [[(∞,1)-pullback]] diagram

$$
  \array{
    \mathbf{B} SO &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} O &\stackrel{\mathbf{w}_1}{\to}& 
    \mathbf{B}\mathbf{Z}_2
  }
$$

in $\infty LieGrpd$, covering under $\Pi$ the pullback

$$
  \array{
    \mathcal{B} SO &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathcal{B} O &\stackrel{w_1}{\to}& \mathcal{B}\mathbf{Z}_2
  }
  \,.
$$

##### Second Stiefel-Whitney class

(...)

$$
  \array{
    \mathbf{B} Spin &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} SO &\stackrel{\mathbf{w}_2}{\to}& 
    \mathbf{B}^2 \mathbf{Z}_2
  }
$$

(...)

##### First fractional Pontryagin class {#SmoothFirstFracPontryaginClass}

Let $\mu_3 \in CE(\mathfrak{so}(n))$ be the [[Lie algebra cohomology|Lie algebra 3-cocycle]] 
$\langle -,[-,-]\rangle$ normalized such its left-invariant continuation to a differential 3-form on $Spin(n)$ is the image in [[deRham cohomology]] of a generator of $H^3(Spin, \mathbb{Z})$.

+-- {: .num_prop}
###### Proposition

The [integration of this cocycle](#IntegrationOfCocycles)

$$
  \frac{1}{2}\mathbf{p}_1 := \exp(\mu) : \mathbf{B}Spin \to \mathbf{B}^3 U(1)
$$

is a smooth refinement of the first fractional [[Pontryagin class]] $\frac{1}{2} p_1 : \mathcal{B}Spin \to \mathcal{B}^4 \mathbb{Z}$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[Chern-Simons circle 3-bundle]].

=--


Therefore the [[homotopy fiber]] 

$$
  \array{
    \mathbf{B} String &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} Spin &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}& 
    \mathbf{B}^3 U(1)
  }
$$

is a smooth model of the [[string group]]. 

+-- {: .num_prop}
###### Proposition


Indeed, this homotopy fiber is given by the Lie [[string 2-group]].

=--

+-- {: .proof}
###### Proof

Compute the [[homotopy pullback]] as the ordinary limit over

$$
  \array{
    &\to& \mathbf{E} \mathbf{B}^2 U(1)
    \\
    && \downarrow
    \\
    \mathbf{cosk}_3 \exp(\mathfrak{so}) &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}& 
    \mathbf{B}^3 U(1)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}Spin
  }
  \,.
$$


By inspection, this gives the [[Lie 2-group]] whose 

* objects are based paths in $G$; the product is by concatenation of such paths;

* morphisms are equivalence classes of based surfaces in $G$ labeled by some $c \in U(1)$; where two of these are equivalence if there is a ball cobounding them such that the integral of $\mu$ over this ball accounts for the difference in the two labels.

Here me may equivalently take [[thin homotopy]]-classes of paths and surfaces. 
This is indeed one of the three incarnations of the string 2-group as a strict 2-group.

(...)

=--


##### Second fractional Pontryagin class {#SmoothSecondPontryagin}

$$
  \array{
    \mathbf{B} Fivebrane &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \mathbf{B} String &\stackrel{\frac{1}{6}\mathbf{p}_2}{\to}& 
    \mathbf{B}^7 U(1)
  }
$$

(...)

* [[fivebrane Lie 6-algebra]]

* [[fivebrane 6-group]]

* [[Chern-Simons circle 7-bundle]]


### Flat $\infty$-connections and local systems {#StrucFlat}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">intrinsic flat cohomology</a> in $Smooth \infty Grpd$.

#### Cohomology with constant coefficients

+-- {: .num_theorem #FlatCohomologyAndWithConstantCoefficients}
###### Theorem

Let $X$ be a [[paracompact space|paracompact]] [[smooth manifold]] regarded as a [[0-truncated]] smooth $\infty$-groupoid under the embedding 
$SmoothMfd \hookrightarrow Smooth \infty Grpd$. Let $A \in $ [[∞Grpd]] be any [[∞-groupoid]] and $Disc A \in Smooth \infty Grpd$ the coresponding [[discrete ∞-groupoid]].  

We have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  Smooth\infty Grpd(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H_{Top}(X,A) \simeq \pi_0   Smooth \infty Grpd(X, Disc A)
  \,.
$$

This also means that 

$$
  H_{smooth,flat}(X,A ) \simeq H_{Top}(X, \Gamma A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Same proof as of the analogous statement at [[ETop∞Grpd]].

=--


#### With coefficients in ${\mathbf{B}^n U(1)}$ or $\mathbf{B}^n \mathbb{R}$
 {#FlatCoefficientsForCircleNGroup} 

Let $\mathbf{B}^n U(1)$ be the circle $(n+1)$-Lie group
as discussed [above](#CircleLienGroup). Recall the notation and 
model category presentations as discussed there.

+-- {: .num_prop #FlatCohomologyWithCoeffsInCircle}
###### Proposition

For $n \geq 1$ a fibration presentation in $[CartSp^{op}, sSet]_{proj}$ of the 
canonical morphism $\mathbf{\flat} \mathbf{B}^n U(1) \to \mathbf{B}^n U(1)$
in $Smooth \infty Grpd$ is given by the image under $\Xi : [CartSp^{op}, Ch_\bullet^+] \to [CartSp^{op}, sSet]$ of

$$
  \array{
    C^\infty(-,U(1)) &\stackrel{d_{dR}}{\to}& \Omega^1(-) &\stackrel{d_{dR}}{\to} & \cdots &\stackrel{d_{dR}}{\to}& \Omega^n_{cl}(-)
    \\
    \downarrow && \downarrow && && \downarrow
    \\
    C^\infty(-, U(1)) &\to& 0 &\to& \cdots &\to& 0
  }
  \,,
$$

where at the top we have the _flat_ [[Deligne cohomology|Deligne complex]]. 

=--

+-- {: .proof}
###### Proof

It is clear that the morphism of chain complexes is an objectwise 
surjection and hence maps to a projective fibration under $\Xi$.
It remains to observe that the flat Deligne complex is a presentation
of $\mathbf{\flat} \mathbf{B}^n U(1)$:

By the discussion at [[∞-cohesive site]] we have that $\mathbf{\flat} = Disc \Gamma$ is given on fibrant objects by first evaluating on the point and then extending back to a constant simplicial presheaf. By the [above discussion](#CircleLienGroup) we have that $\Xi (U(1)[n])$ is indeed fibrant, and so a fibrant presentation of $\mathbf{\flat} \mathbf{B}^n U(1)$ is given by the _constant_ presheaf $U(1)_{const} [n] : U \mapsto \Xi(U(1)[n])$.

The inclusion $U(1)_{const}[n] \to U(1)[n]$ is not yet a fibration. But by a basic fact of [[abelian sheaf cohomology]] -- using the [[Poincare lemma]] -- we have a global weak equivalence $U(1)[n]_{const} \stackrel{\simeq}{\to} [C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{cl}(-)]$ that factors this inclusion by the above fibration.
 
=--

#### Flat coefficients of $\mathbf{B}G$ for $G$ a Lie group 
 {#FlatCoefficientsForDeloopedLieGroup}

Let $G$ be a [[Lie group]] regarded as a [[0-truncated]] [[∞-group]]
in $Smooth \infty Grpd$. Write $\mathfrak{g}$ for its [[Lie algebra]].
Write $\mathbf{B}G \in Smooth \infty Grpd$ for its [[delooping]].
Recall the fibrant presentation 
$\mathbf{B}G_c \in [CartSp_{smooth}^{op}, sSet]_{proj,loc}$ from 
[above](#DeloopedLieGroup).

+-- {: .num_prop #LieGroupFibrantFlatInclusion}
###### Proposition

The object 
$\mathbf{\flat}\mathbf{B}G \in Smooth \infty Grpd$ has a fibrant 
presentation $\mathbf{\flat} \mathbf{B}G_{c} \in [CartSp^{op}, sSet]_{proj,loc}$ given by the [[groupoid of Lie-algebra valued forms]]

$$
  \mathbf{\flat}\mathbf{B}G _{c}
  =
  N
  \left(
    C^\infty(-,G)\times \Omega^1_{flat}(-,\mathfrak{g}) 
   \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1^{-1} d p_1}{\to}}{\underset{p_2}{\to}} \Omega^1_{flat}(-,\mathfrak{g})
  \right)
$$

and this is such that the canonical morphism 
$\mathbf{\flat} \mathbf{B}G \to \mathbf{B}G$ is presented by the canonical 
morphism of simplicial presheaves 
$\mathbf{\flat}\mathbf{B}G_{c} \to \mathbf{B}G_{c}$ which is a fibration
in $[CartSp_{smooth}^{op}, sSet]_{proj}$.

=--

+-- {: .num_remark}
###### Remark

This means that a $U$-parameterized family of objects of 
$\mathbf{\flat}\mathbf{B}G_{c}$ is given by a 
[[Lie-algebra valued 1-form]] $A \in \Omega^1(U)\otimes \mathfrak{g}$ whose [[curvature]] 2-form $F_A = d_{dR} A + [A ,\wedge A]  = 0$ vanishes,  
and a $U$-parameterized family of morphisms $g : A \to A'$ is given by a smooth function $g \in C^\infty(U,G)$ such that $A' = Ad_g A + g^{-1} d g$, where $Ad_g A = g^{-1} A g$ is the [[adjoint action]] of $G$ on its 
[[Lie algebra]], and where $g^{-1} d g := g^* \theta$ is the pullback of the [[Maurer-Cartan form]] on $G$ along $g$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[∞-cohesive site]] we have that 
$\mathbf{\flat} \mathbf{B}G$ is presented by the simplicial presheaf
that is constant on the [[nerve]] of the one-object [[groupoid]]
$$
  G_{disc} \stackrel{\to}{\to} *
  \,,
$$
for the [[discrete group]] underlying the [[Lie group]] $G$.
The canonical morphism of that into $\mathbf{B}G_c$ is however 
not a fibration.

We claim that the canonical inclusion
$N(G_{disc}\stackrel{\to}{\to}) \to \mathbf{\flat} \mathbf{B}G_{c}$
factors the inclusion into $\mathbf{B}G_c$ by a weak equivalence followed
by a global fibration.

To see the weak equivalence, notice that it is objectwise an [[equivalence of groupoids]]: it is [[essentially surjective functor|essentially surjective]] since every flat $\mathfrak{g}$-valued 1-form on the [[contractible]] $\mathbb{R}^n$ is of the form $g d g^{-1}$ for some function $g : \mathbb{R}^n \to G$ (let $g(x) = P \exp(\int_{0}^x) A$ be the [[parallel transport]] of $A$ along any path from the origin to $x$). Since the [[gauge transformation]] [[automorphism]] of the trivial $\mathfrak{g}$-valued 1-form are precisely given by the constant $G$-valued functions, this is also objectwise a [[full and faithful functor]]. 

Similarly one sees that the map $\mathbf{\flat}\mathbf{B}G_c \to \mathbf{B}G$ is a fibration.

Finally we need to show that $\mathbf{\flat}\mathbf{B}G_c$ is fibrant in $[CartSp^{op}, sSet]_{proj,loc}$. This can be seen by observing that this sheaf is the coefficient object that in [[Cech cohomology]] computes $G$-[[principal bundle]]s with flat [[connection on a bundle|connection]] and then reasoning as above: every $G$-principal bundle with flat connection 
on a [[Cartesian space]] is equivalent to a trivial $G$-principal bundle whose connection is given by a globally defined $\mathfrak{g}$-valued 1-form. Morphisms between these are precisely $G$-valued functions that act on the 1-forms by gauge transformations as in the [[groupoid of Lie-algebra valued forms]].

=--



### de Rham cohomology {#StrucDeRham}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#deRhamCohomology">intrinsic de Rham cohomology</a>
in $Smooth \infty Grpd$.


#### With coefficients in $\mathbf{B}^n U(1)$ or $\mathbf{B}^n \mathbb{R}$
 {#deRhamCoefficientsInBnU1}

Let $\mathbf{B}^n U(1)$ be the circle Lie $(n+1)$-group, as 
discussed [above](#CircleLienGroup). Recall the notation and 
model category presentations from the discussion there.

+-- {: .num_prop #OrdinaryDeRham}
###### Proposition

A fibrant representative in $[CartSp^{op}, sSet]_{proj,loc}$ of 
the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#deRhamCohomology">de Rham coefficent object</a> 
$\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ as well as
$\mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}$
is given by the 
truncated [[de Rham complex]] of sheaves of abelian groups of
[[differential form]]s

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn}
  :=
  \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{chn}
  :=
  \Xi[\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2(-) \stackrel{d_{dR}}{\to}\cdots \to \Omega^{n-1}(-) \stackrel{d_{dR}}{\to}\Omega^n_{cl}(-)]
  \,.
$$

=--


+-- {: .proof}
###### Proof

By definition 
and the fact that homotoppy pullbacks in the local
structure may be computed in global structure
(discussed [here](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#HomotopyLimits))
the object $\mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn}$
is given, up to equivalence, by the [[homotopy pullback]] 
in $[CartSp^{op}, Ch_\bullet]_{proj}$
of the inclusion $U(1)_{const}[n] \to U(1)[n]$ along the point inclusion
$* \to U(1)[n]$. We may compute this as the ordinary pullback
after passing to a [[resolution]] of this inclusion by a fibration.
By the [above discussion](#FlatCohomologyWithCoeffsInCircle) of
flat cohomology with coefficients in $\mathbf{B}^n U(1)$ such a 
fibration replacement is given by the map from the flat Deligne
complex. Using this we find the ordinary [[pullback]] diagram

$$
  \array{
    \Xi[0 \to \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]
    &\to&
    \Xi[C^\infty(-,U(1)) \to \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]
    \\
    \downarrow && \downarrow
    \\
    \Xi[0 \to 0 \to \cdots \to 0]
    &\to&
    \Xi[C^\infty(-,U(1)) \to 0 \to \cdots \to 0]
  }
  \,.
$$


=--

##### On smooth manifolds

Let $X$ be an [[orientable]] [[smooth manifold]] regarded under the embedding
$SmoothMfd \hookrightarrow Smooth \infty Grpd$.

Write $H^n_{dR}(X)$ for the ordinary [[de Rham cohomology]]
of $X$.

+-- {: .num_prop}
###### Proposition

For $n \in \mathbb{N}$ we have isomorphisms

$$
  \pi_0 Smooth \infty Grpd(X, \mathbf{\flat}_{dR} \mathbf{B}^n U(1))
  \simeq
  \left\{
     \array{
        H^n_{dR}(X) &| n \geq 2
        \\
        \Omega^1_{cl}(X) &| n = 1
        \\
        0 &| n = 0
     }
   \right.
$$

=--

+-- {: .proof}
###### Proof

Let $\{U_i \to X\}$ be a [[good open cover]]. By the disucssion at [[model structure on simplicial presheaves]] the [[Cech nerve]] $C(\{U_i\}) \to X$ is a cofibrant [[resolution]] of $X$ in $[CartSp^{op}, sSet]_{proj,loc}$. Therefore we have for all $n$

$$
  Smooth \infty Grpd(X,\mathbf{\flat}_{dR} \mathbf{B}^n U(1))
  \simeq
  [CartSp^{op}, sSet](C(\{U_i\}), \Xi[\Omega^1(-) \stackrel{d_{dR}}{\to} \cdots \to \Omega^n_{cl}(-)])
  \,.
$$

The right hand is the $\infty$-groupoid of cocylces in the [[Cech cohomology|Cech]] [[hypercohomology]] of the truncated complex of sheaves of differential forms. A cocycle is given by a collection

$$
  (C_i, B_{i j}, A_{i j k}, \cdots  , Z_{i_1, \cdots, i_n})
$$

of differential forms, with $C_i \in \Omega^n_{cl}(U_i)$, $B_{i j} \in \Omega^{n-1}(U_i \cap U_j)$, etc. , such that this collection is annihilated by the total differential $D = d_{dR} \pm \delta$, where $d_{dR}$ is the de Rham differential and $\delta$ the alternating sum of the pullbacks along the face maps of the [[Cech nerve]].

It is a standard result of [[abelian sheaf cohomology]] that such cocycles represent classes in de Rham cohomology. 

But for the record and since the details of this computation will show up again at some mildly subtle points in further discussion below, we spell this out in some detail.

For $n = 1$ and $n= 0$ our truncated de Rham complex degenerates to 
$\mathbf{\flat}_{dR}\mathbf{B}U(1)_{chn} = \Xi[\Omega^1_{\mathrm{cl}}(-)]$
and
$\mathbf{\flat}_{dR}U(1)_{chn} = \Xi[0]$, respectively, which obviously has the cohomology as claimed above.

For $n \geq 2$ we can explicitly construct coboundaries connecting such a generic cocycle  to one of the form 

$$
  (F_i, 0, 0, \cdots, 0)
$$

by using a [[partition of unity]] $(\rho_i \in C^\infty(X))$ subordinate to the cover $\{U_i \to X\}$, i.e. $x \in U_i \Rightarrow \rho_i(x) = 0$ and $\sum_i \rho_i = 1$.

For consider 

$$
  \begin{aligned}
     & (C_i, B_{i j}, A_{i j k}, \cdots  , Y_{i_1, \cdots, i_{n}}, Z_{i_1, \cdots, i_{n+1}})
     \\
     + & D (0, 0, \cdots, \sum_{i_0} \rho_{i_0} Z_{i_0, i_1, \cdots, i_{n}},0)
     \\
     =
     & (C_i, B_{i j}, A_{i j k}, \cdots  , Y_{i_1, \cdots, i_{n}}
     + d_{dR}\sum_{i_0} \rho_{i_0} Z_{i_0, i_1, \cdots, i_{n}}, 0)   
  \end{aligned}
  \,,
$$

where we use that from $(\delta Z)_{i_1, \cdots, i_{n+2}} = 0$ it follows that

$$
  \begin{aligned}
    (\delta \sum \rho Z)_{i_1, \cdots, i_{n+1}}
    &=
    \sum_{i_0} \rho_{i_0}
    \sum_{k = 1}^{n+1}
    (-1)^k
    Z_{i_0, i_1 \cdots, \hat i_k, \cdots, i_{n+1}}
    \\
    & =
    \sum_{i_0} \rho_{i_0}
    Z_{i_1 ,\cdots, i_{n+1}}    
    \\
    & =
    Z_{i_1 ,\cdots, i_{n+1}}
  \end{aligned}
  \,.
$$

> where I am suppressing some evident signs...

By recurseively adding coboundaries this way, we can annihilate all the higher Cech-components of the original cocycle and arrive at a cocycle of the form $(F_i, 0, \cdots, 0)$. 

Such a cocycle being $D$-closed says precisely that $F_i = F|_{U_i}$ for $F \in \Omega^n_{cl}(X)$ a globally defined closed differential form. Moreover, coboundaries between two cocycles both of this form 

$$
  (F_i, 0, \cdots , 0) = (F'_i, 0, \cdots, 0) + D(\lambda_i, \lambda_{i j}, \cdots)
$$

are necessarily themselves of the form $(\lambda_i, \lambda_{i j}, \cdots) =  (\lambda_i, 0 ,\cdots, 0)$ with $\lambda_i = \lambda|_{U_i}$ for $\lambda \in \Omega^{n-1}(X)$ a globally defined differential $n$-form and $F = F' + d_{dR} \lambda$.

=--


##### On  $\mathbf{B}^n U(1)$ 



+-- {: .num_prop #DeRhamBnU1}
###### Proposition

For $n \geq 1$ we have that the <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#deRham">intrinsic de Rham cohomology</a> of the <a href="BnU1">circle n-groupoid</a> $\mathbf{B}^n U(1)$ in $\mathbf{H} = \infty LieGrpd$ is concentrated in degree $(n+1)$, where it is  $\mathbb{R}$:

$$
  H(\mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k} U(1) )
  =
  \left\{
    \array{
       \mathbb{R} & for \; k = n+1
       \\
       0 & otherwise
    }
  \right.
$$

=--

+-- {: .num_remark }
###### Remark

By the discussion at [circle n-group -- differential coefficients](#DifferentialBnU1) above, we have that $\mathbf{\flat}_{dR} \mathbf{B}^k U(1) \simeq \mathbf{\flat}_{dR} \mathbf{B}^k \mathbb{R}$, reflecting the familiar fact that since $Lie(U(1)) \simeq Lie(\mathbb{R})$ we have that $Lie(U(1))$-valued forms are naturally identified with plain $\mathbb{R} = Lie(\mathbb{R})$-valued forms. Therefore the above may equivalently be restated as

$$
  H^{k}_{dR}(\mathbf{B}^n U(1))
  :=
  H(\mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k} \mathbb{R} )
  =
  \left\{
    \array{
       \mathbb{R} & for \; k = n+1
       \\
       0 & otherwise
    }
  \right.
  \,.
$$


=--

+-- {: .proof}
###### Proof

Since both domain and codomain are abelian, it will be sufficient to demonstrate the statement for $n = 1$, $k$ arbitrary, and for $k = 1$, $n$ arbitrary. All other combinations of $n$ and $k$ are then implied by repeatedly using the [[delooping]]/[[loop space object|looping]] [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $(\Sigma \dashv \Omega)$  on abelian objects in

$$
  \begin{aligned}
    \mathbf{H}(\mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k}U(1))
    &
    \simeq
    \mathbf{H}(\mathbf{B}^n U(1), \Omega \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
    \\
    & \simeq
    \mathbf{H}(\Sigma \mathbf{B}^n U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
    \\
    & \simeq
    \mathbf{H}(\mathbf{B}^{n+1} U(1), \mathbf{\flat}_{dR} \mathbf{B}^{k+1}U(1))   
  \end{aligned}
  \,.
$$

Here we use that since $\mathbf{\flat}_{dR}$ is a [[right adjoint]], it commutes with forming [[loop space object]]s.

Using this, the main work in proving the theorem is involved in establishing the statement for $k = n+1 = 2$, which we now spell out.
We note that this would be easy to prove if we did not have to pass to a cofibrant [[resolution]] of $\mathbf{B}^n U(1)$ for computing the [[derived hom-space]] in the projectve [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj,cov}$. For then we would compute, using the [above](#DifferentialBnU1) fibrant model for $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$

$$
  \begin{aligned}
    & [CartSp^{op}, sSet](\;\;\Xi(C^\infty(-U(1))[n]), \;\;\Xi[\Omega^1(-) \to \cdots \to \Omega^n_{cl}(-)]\;\;)
    \\
    & \simeq
    [CartSp^{op}, Ch_\bullet](\;\; N \Xi(C^\infty(-U(1))[n]), \;\;\Omega^1(-) \to \cdots \to \Omega^n_{cl}(-) \;\;)
    \\
    & \simeq
    [CartSp^{op}, Ch_\bullet](\;\; C^\infty(-U(1))[n], \;\; \Omega^1(-) \to \cdots \to \Omega^n_{cl}(-) \;\; )
   \\
    &\simeq
    [CartSp^{op}, Ab](\;\; C^\infty(-,U(1)), \;\; \Omega^1(-) \;\;)
  \end{aligned}
  \,,
$$

where $\Xi : [CartSp^{op}, Ch_\bullet] \to [CartSp^{op}, sSet]$ is the [[Dold-Kan correspondence]] map.

To see what this last set is, notice that if we forgot the abelian group structure, and looked at the last hom-set as one of sheaves, we find by the [[Yoneda lemma]] that is is the set $\Omega^1(U(1))$ of 1-forms. Among these the forms $\omega \in \Omega^1(U(1))$ that do respect the group structure are those such that for all $U \in CartSp$ and all $f,g : U \to U(1)$ we have

$$
  f^* \omega + g^* \omega = (f \cdot g)^* \omega
  \,.
$$

A little reflection shows that this is satisfied precisely by the constant forms, i.e. those that are a linear multiple of the [[Maurer-Cartan form]] on $U(1)$. Hence the above hom-complex is indeed just

$$
  \cdots \simeq \mathbb{R}
  \,.
$$

But $\mathbf{B}^n U(1)$ is not cofibrant in $[CartSp^{op}, sSet]_{proj}$. We will pass now to a cofibrant [[resolution]] and discuss that computing the homs out of that does nevertheless reduce to the above computation.

By Dugger's <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantReplacement">construction of cofibrant replacements in the projective model structure</a> we have that a cofibrant replacement for a simplciial presheaf $A$ is given by the diagonal of the [[bisimplicial set|bisimplicial presheaf]] which in degree $(n,k)$ has

$$
  \coprod_{U_n \to U_{n-1} \to \cdots \to U_0 \to A_k} U_n
  \,,
$$

where the coproduct ranges over all sequences of morphisms of representables $U_i \in CartSp$ into $A_k$. And face and degeneracy maps are the evident ones. 

So we prove now that the computation of $\mathbf{H}(\mathbf{B}U(1), \mathbf{\flat}_{dR}\mathbf{B}^2 U(1))$ does reduce to the above computation of morphisms out of $\mathbf{B}U(1)$. Write $Q(\mathbf{B}^1 U(1)) \stackrel{\simeq}{\to} \mathbf{B}^n U(1)$ for the above cofibrant replacement. 

Then a morphism $Q(\mathbf{B} U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1))$ is a collection of horizontal morphisms in the diagram

$$
  \array{
     \Delta[2] &\to& \coprod_{U_0 \to U_1 \to U:2 \to U(1)} \Omega^2_{cl}(U_0) \times \Omega^1(U_0)\times \Omega^1(U_0)
     \\
     \downarrow \downarrow \downarrow &&
     \downarrow \downarrow \downarrow
     \\
     \Delta[1] &\to& \coprod_{U_0 \to U_1 \to U(1)} \Omega^2_{cl}(U_0) \times \Omega^1(U_0)
     \\
     \downarrow \downarrow &&
     \downarrow \downarrow
     \\
     \Delta[0]
     &\to&
     \coprod_{U_0 \in CartSp} \Omega^2_{cl}(U_0)
  }
$$

Explicitly, such a cocycle is

* a collection $\{\lambda_{U} \in \Omega^2_{cl}(U) | U \in CartSp\}$;

* a collection $\{\omega_{U_0 \to U_1 \to U(1)} \in \Omega^1(U_9)\}$ 

such that 

* for all $f : U_0 \to U_1$ we have
  $f^* \lambda \lambda_{U_1}  = 
  \lambda_{U_0} + \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}$;

* for all $U_0 \stackrel{f}{\to} U_1 \to U_2 \to U(1)\times U(1)$ we have
  
  $$
    \omega_{U_0 \to U_1 \to U(1)\times U(1) \stackrel{p_1}{\to} U(1)}
    + 
    f^* \omega_{U_1 \to U_2 \to U(1) \times U(1) \stackrel{p_2}{\to} U(1)}
    =
    \omega_{U_0 \to U_2 \to U(1) \times U(1) \stackrel{\cdot}{\to} U(1)}
  $$

* for all $U$ we have $\omega_{U \stackrel{Id}{\to} U \to \stackrel{e}{\to} U(1)} = 0$.

A coboundary between two such cocycles is 

* for all $U \in CartSp$ a $\kappa_U \in \Omega^1(U)$

such that

* $\lambda'_U = \lambda_U + d \kappa_U$;

* $\omega'_{U_0 \stackrel{f}{\to} U_1 \to U(1)} = \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)} + f^* \kappa_{U_1} - \kappa_{U_0}$.

We claim that any such cocycle $(\lambda,\omega)$ is coboundant to 
one such that

* for all $U$ we have $\lambda_U = 0$;

* for all $U_0 \stackrel{f}{\to} U(1)$ we have 
  $\omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)} = 0$.

The coboundary establishing this is given by setting

$$
  \kappa_U := \omega_{U \to * \stackrel{e}{\to} U(1)}
  \,.
$$ 

This follows from the cocycle law for for maps of the form 

$$
  \array{
    && U_1
    \\
    & {}^{\mathrlap{f}}\nearrow && \searrow
    \\
    U_0 &&\to&& *
    \\
    & {}_{\mathllap{const_{e,e}}}\searrow && \swarrow_{\mathrlap{const_{e,e}}}
    \\
    &&
    U(1) \times U(1)
  }
$$

which asserts that

$$
  \omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)}
  =
  \omega_{U_0 \to * \stackrel{e}{\to} U(1)}
  -
  f^* \omega_{U_1 \to * \stackrel{e}{\to} U(1)}
  \,.
$$

Moreover we claim that such cocycles with $\lambda_U = 0$ for all $U$ and $\omega_{U_0 \to U_1 \stackrel{e}{\to} U(1)}$ for all $U_0 \stackrel{f}{\to} U_1$ have no nontrivial morphisms between them, which means that these do constitute unique representatives of their cohomology classes. This is because such a morphism would be given by a collection $\kappa_U \in \Omega^1_{cl}(U)$ of closed 1-forms for each $U \in CartSp$, such that in particular for all $U_0 \stackrel{f}{\to} U_1 $ we'd have
$\kappa_{U_0} = f^* \kappa_{U_1}$. Clearly for any choice of $\kappa_U$s, one can find $f$ such that this is not satisfied. For instance simply take $f : U \to *$, which imposes the relation $\kappa_U = 0$ explicitly.

This shows that the cohomology in question is the set of cocycles as above, satisfying the two extra constraints. Now using the cocycle law for the diagram

$$
  \array{
    && U_0
    \\
    & {}^{\mathllap{Id}}\nearrow && \searrow^{\mathrlap{f}}
    \\
    U_0 &&\to&& U_1
    \\
    & {}_{(h,const_e)}\searrow && \swarrow_{\mathrlap{(g,const_e)}}
    \\
    &&
    U(1) \times U(1)
  }
$$

we find 

$$
  \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}
  =
  \omega_{U_0 \stackrel{Id}{\to} U_0 \to U(1)}
  + 
  \omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)}
$$

and using it for

$$
  \array{
    && U_1
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{Id}}
    \\
    U_0 &&\to&& U_1
    \\
    & {}_{(const_e,h)}\searrow && \swarrow_{\mathrlap{(const_e,g)}}
    \\
    &&
    U(1) \times U(1)
  }
$$

we find

$$
  \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}
  =
  \omega_{U_0 \stackrel{f}{\to} U_1 \stackrel{e}{\to} U(1)}
  + 
  f^* \omega_{U_1 \stackrel{Id}{\to} U_1 \to U(1)}
  \,.
$$

In view of the above gauge condition this is equivalently

$$  
  \omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)}
  =
  \omega_{U_0 \stackrel{Id}{\to} U_0 \to U(1)}
  =
  f^* \omega_{U_1 \stackrel{Id}{\to} U_1 \to U(1)}  
  \,.
$$

This says that $\omega_{U_0 \stackrel{f}{\to} U_1 \to U(1)} =: \omega_{U_0 \to U(1)}$ in fact only depends on the domain of $f$, hence only on the map $h : U_0 \to U(1)$ and that as such these forms constitute the components of a morphism of sheaves

$$
  C^\infty(-,U(1)) \to \Omega^1(-)
  \,.
$$

But this means that the cocycle $Q(\mathbf{B}U(1)) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ indeed factors through $Q(\mathbf{B}U(1)) \to \mathbf{B}U(1)$ and therefore the naive computation at the beginning indeed applies and shows that these cocycle are in bijection with multiples of the standard [[Maurer-Cartan form]] on $U(1)$, hence with $\mathbb{R}$, so that

$$
  H(\mathbf{B}U(1), \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)) = 
  \mathbb{R}
  \,.
$$

The same kind of argument as above shows that for $k \geq 2$ cocycles $Q(\mathbf{B}U(1)) \to \mathbf{\flat}_{dR}\mathbf{B}^k U(1)$ have underlying them sheaf morphisms $C^\infty(-,U(1)) \to \Omega^{k-1}(-)$. But all these are necessarily trivial, due to the fact that $U(1)$ is 1-dimensional. This establishes the theorem for $n=1$ and arbitrary $k$.


Finally the same argument that above showed that no nontrivial automorphisms of certain cocycles exist shows the theorem for $k=1$ and arbitrary $n \geq 1$, namely that no nontrivial morphisms $Q(\mathbf{B}^n  U(1)) \to \mathbf{\flat}_{dR} \mathbf{B}U(1)$ exist: such are given by a collection of 1-forms $\lamba_U \in \Omega^1(U)$ for all $U$, satisfyine for all possible maps $f : U_0 \to U_1$ the relation $\lambda_{U_0} = f^* \lambda_{U_1}$. If $\lambda_{U}$ does not vanish for all $U$, one can always find some $f$ for which this is not satisfied.  


=--




#### With coefficients in $\mathbf{B}G$ for a Lie group $G$ 
 {#deRhamWithCoefficientsInBOfLieGroup}

Let $G$ be a [[Lie group]]. Write $\mathfrak{g}$ for its 
[[Lie algebra]].


+-- {: .num_prop #LieGroupDeRhamCoefficients}
###### Proposition

The object $\mathbf{\flat}_{dR}\mathbf{B}G \in Smooth \infty Grpd$
has a fibrant presentation in $[CartSp_{smooth}^{op}, sSet]_{proj,loc}$ 
by the [[sheaf]] 
$\mathbf{\flat}\mathbf{B}G_c = \Omega^1_{flat}(-, \mathfrak{g})$ of 
[[groupoid of Lie-algebra valued forms|flat Lie-algebra valued forms]]

$$
  \mathbf{\flat}_{dR}\mathbf{B}G_c
  :
  U \mapsto \Omega^1_{flat}(U,\mathfrak{g})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By a [proposition above](#LieGroupFibrantFlatInclusion) we have a
fibration $\mathbf{\flat}\mathbf{B}G_c \to \mathbf{B}G_c$
in $[CartSp_{smooth}^{op}, sSet]_{proj}$ modeling the canonical 
inclusion $\mathbf{\flat}\mathbf{B}G \to \mathbf{B}G$. Therefore
we may get a presentation for the defining [[(∞,1)-pullback]]

$$
  \mathbf{\flat}_{dR}\mathbf{B}G  := * \times_{\mathbf{B}G} \mathbf{\flat} \mathbf{B}G
$$

in $Smooth \infty Grpd$ by the ordinary [[pullback]]

$$
  \mathbf{\flat}_{dR}\mathbf{B}G_c 
  \simeq * \times_{\mathbf{B}G_c} \mathbf{\flat} \mathbf{B}G_c
$$

in $[CartSp^{op}, sSet]$.

The resulting simplicial presheaf is fibrant in $[CartSp^{op}, sSet]_{proj,loc}$ because it is a [[sheaf]].

=--


+-- {: .num_remark }
###### Remark

Writing $T U$ for the [[tangent Lie algebroid]] of $U$ 
we may equivalently write

$$
  \mathbf{\flat}_{dR} \mathbf{B}G_ : U \mapsto Hom(T U, \mathfrak{g})
  \,,
$$ 

where on the right we have the set of morphisms of [[Lie algebroid]]s. Equivalently in terms of [[Chevalley-Eilenberg algebra]]s this is 

$$
  \mathbf{\flat}_{dR} \mathbf{B}G_c : 
  U \mapsto Hom_{dgAlg}(CE(\mathfrak{g}),(\Omega^\bullet(U), d_{dR}))
  \,,
$$ 

=--


+-- {: .num_prop #LieGroupDeRhamCohomology}
###### Corollary

For $X \in $ [[SmoothMfd]] $\hookrightarrow Smooth \infty Grpd$ we find
the intrinsic de Rham cohomology set

$$
  H^1_{dR, Smooth}(X, G)
  :=
  \pi_0 Smooth \infty Grpd(X, \mathbf{\flat}_{dR} \mathbf{B}G)
  \simeq
  \Omega^1_{flat}(X, \mathfrak{g})
$$

is the set of smooth flat $\mathfrak{g}$-valued differential forms on $X$.

=--

#### With coefficients in $\mathbf{B}G$ for $G$ a strict 2-group



We work out, following the [general definition](#CoeffsLieAlgForms) the coefficient object for [[2-groupoid of Lie 2-algebra valued forms|Lie 2-algabra valued forms]] $\mathbf{\flat}_{dR} \mathbf{B}[G_2\to G_1]$ for $(G_2 \to G_1)$ a Lie [[crossed module]].

Let $\Xi : CrsdCplx \to KanCplx$ now denote the inclusion of [[crossed complex]]es into all [[Kan complex]]es/[[∞-groupoid]]s.


Write $[\mathfrak{g}_2 \stackrel{\delta_*}{\to} \mathfrak{g}_1]$ for the corresponding [[differential crossed module]] with action $\alpha_* : \mathfrak{g}_1 \to der(\mathfrak{g}_2)$ corresponding to the Lie [[strict 2-group]] [[crossed module]] $(G_2 \stackrel{\delta}{\to} G_1)$ with action $\alpha : G_1 \to Aut(G_2)$. 

+-- {: .num_prop }
###### Proposition

The Lie [[2-groupoid]] $\mathbf{\flat} \mathbf{B}[G_2 \stackrel{\delta}{\to} G_1]$ is represented in $[CartSp^{op}, sSet]$ by the Lie [[2-groupoid]] which on $U \in CartSp$ s the following 2-groupoid:

* An [[object]] is a pair 

  $$
    A \in \Omega^1(U,\mathfrak{g}_1)\,, \;\;\;
    B \in \Omega^2(U,\mathfrak{g}_2)
  $$ 
  
  such that 

  $$
    \delta_* B - d A + [A \wedge A] = 0
  $$

  and

  $$
    d B + [A \wedge B] = 0
    \,.
  $$

* A 1-[[morphism]] $(g,a) : (A,B) \to (A',B')$ is a pair

  $$  
    g \in C^\infty(U,G_1)\,,\;\;\; a \in \Omega^1(U,\mathfrak{g}_2)
  $$

  such that

  $$
    A' = g^{-1} A g + g^{-1} d g + g^{-1} \delta_* a g
  $$

  and

  $$
    B' = \alpha_{g^{-1}}(
      B + d a + [a \wedge a] + \alpha_*(A \wedge a)
    )
    \,.
  $$

  The composite of two 1-morphisms

  $$
    (A,B) \stackrel{(g_1,a_1)}{\to} (A',B') \stackrel{(g_2,a_2)}{\to}
    (A'', B'')
  $$

  is given by the pair

  $$
    (g_1 g_2, a_1 + (\alpha_{g_2})_* a_2)
    \,.
  $$

* a [[2-morphism]] $f : (g,a) \to (g', a')$ is a function

  $$
    f \in C^\infty(U,G_2)
  $$

  such that 

  $$
    g' = \delta(f)^{-1} \cdot g 
  $$
 
  and

  $$
    a' = f^{-1} d f + f^{-1} a f + f^{-1}(r_f^{-1} \circ \alpha_f)_*(a)f
  $$

and composition is defined as follows

(...)

=--

This is the [[2-groupoid of Lie 2-algebra valued forms]] as described in [definition 2.11](http://arxiv.org/PS_cache/arxiv/pdf/0802/0802.0663v3.pdf#page=27) of [SchrWalII](http://arxiv.org/abs/0802.0663). There are many possible conventions. The above is supposed to describe the _bidual_ [[opposite 2-category]] of the 2-groupoid as defined in that article, with the direction of 1- and 2-morphisms reversed. 


+-- {: .num_cor }
###### Corollary

The 2-groupoid $\mathbf{\flat}_{dR} \mathbf{B}[G_2 \to G_1]$ is as the one above, discarding the piece $C^\infty(-,G_1)$ in the 1-morphisms and the piece $C^\infty(-,G_2)$ in the 2-morphismms.

=--

+-- {: .proof}
###### Proof

Form the defining pullback as before. (...)

=--




### Exponentiated $\infty$-Lie algebras {#StrucLieAlg}

We discuss here the  <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#LieAlgebras">intrinsic exponentiated ∞-Lie algebras</a> in $Smooth \infty Grpd$.

#### Lie integration {#LieIntegration}

+-- {: .num_defn}
###### Definition

Write [[dgAlg]] for the [[category]] of [[dg-algebra]]s over 
the [[real number]]s $\mathbb{R}$.

Write

$$
  L_\infty \stackrel{CE}{\hookrightarrow} dgAlg^{op}
$$

for the [[full subcategory]] of the [[opposite category]] on the graded-commutative [[semi-free dga]]s of [[finite type]] on generators in positive degree. This is the category of [[L-∞ algebra]]s identified by their dual [[Chevalley-Eilenberg algebra]]s.

=--

We describe a presentation of the exponentiation an [[L-∞ algebra]] to a smooth $\infty$-group. The following somewhat technical definition serves to control the smooth structure on these exponentiated objects.


+-- {: .num_defn}
###### Definition

For $k \in \mathbb{N}$ regard the $k$-[[simplex]] $\Delta^k$ as a [[smooth manifold|smooth]] [[manifold with corners]] in the standard way. We think of this embedded into the [[Cartesian space]] $\mathbb{R}^k$ in the standard way with maximal rotation symmetry about the center of the simplex, and equip $\Delta^k$ with the [[metric space]] structure induced this way.

A smooth [[differential form]] $\omega$ on $\Delta^k$ is said to have **sitting instants** along the boundary if, for every $(r \lt k)$-face $F$ of $\Delta^k$ there is an [[open neighbourhood]] $U_F$ of $F$ in $\Delta^k$ such that $\omega$ restricted to $U$ is constant in the directions perpendicular to the $r$-face on its value restricted to that face.

More generally, for any $U \in $ [[CartSp]] a smooth differential form $\omega$ on $U \times\Delta^k$ is said to have sitting instants if there is $0 \lt \epsilon \in \mathbb{R}$ such that for all points $u : * \to U$ the pullback along  $(u, \mathrm{Id}) : \Delta^k \to U \times \Delta^k$ is a form with sitting instants on $\epsilon$-[[open neighbourhood|neighbourhood]]s of faces.

Smooth forms with sitting instants form a sub-dg-algebra of all smooth forms. We write $\Omega^\bullet_{si}(U \times \Delta^k)$ for this sub-dg-algebra.

We write $\Omega_{si,vert}^\bullet(U \times \Delta^k)$ for the further sub-dg-algebra of [[vertical differential form]]s with respect to the projection $p : U \times \Delta^k \to U$, hence the [[coequalizer]]

$$
  \Omega^{\bullet \geq 1}(U)
  \stackrel{\stackrel{p^*}{\to}}{\underset{0}{\to}}
  \Omega^\bullet_{si}(U \times \Delta^k)
  \to
  \Omega^\bullet_{si, vert}(U \times \Delta^k)  
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

For $\mathfrak{g} \in L_\infty$ write $\exp(\mathfrak{g}) \in [CartSp_{smooth}^{op}, sSet]$ for the [[simplicial presheaf]] defined over $U \in $ [[CartSp]] and 
$n \in \mathbb{N}$ by

$$
  \exp(\mathfrak{g}) 
   :
  (U, [n]) \mapsto
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega_{si,vert}^\bullet(U \times \Delta^n), )
$$

with the evident structure maps given by pullback of [[differential form]]s.

=--

For references related to this definition see _[[Lie integration]]_ .

+-- {: .num_prop}
###### Proposition

The objects $\exp(\mathfrak{g}) \in [CartSp_{smooth}^{op}, sSet]$ are 

* [[connected]];

* [[Kan complex]]es over each $U \in $ [[CartSp]].

=--

+-- {: .proof}
###### Proof

That $\exp(\mathfrak{g})_0 = *$ follows from degree-counting: $\Omega^\bullet_{si,vert}(U \times \Delta^0) = C^\infty(U)$ is entirely in degree 0 and  $CE(\mathfrak{g})$ is in degree 0 the ground field $\mathbb{R}$.

To see that $\exp(\mathfrak{g})$ has all [[horn]]-fillers over each $U \in CartSp$ observe that the standard [[continuous function|continuous]] [[horn]] [[retract]]s $f : \Delta^k \to \Lambda^k_i$ are smooth away from the preimages of the $(r \lt k)$-faces of $\Lambda[k]^i$.

For $\omega \in \Omega^\bullet_{si,vert}(U \times \Lambda[k]^i)$ a differential form with sitting instants on $\epsilon$-neighbourhoods, let therefore $K \subset \partial \Delta^k$ be the set of points of distance $\leq \epsilon$ from any subface. Then we have a smooth function 

$$
  f : \Delta^k \setminus K \to \Lambda^k_i \setminus K
  \,.
$$

The pullback $f^* \omega \in \Omega^\bullet(\Delta^k \setminus K)$ may be extended constantly back to a form with sitting instants on all of $\Delta^k$. 

The resulting assignment

$$
  (CE(\mathfrak{g}) \stackrel{A}{\to} \Omega^\bullet_{si,vert}(U \times \Lambda^k_i))
  \mapsto
  (CE(\mathfrak{g}) \stackrel{A}{\to} \Omega^\bullet_{si,vert}(U \times \Lambda^k_i) \stackrel{f^*}{\to} \Omega^\bullet_{si,vert}(U \times \Delta^n))
$$

provides fillers for all [[horn]]s over all $U \in $ [[CartSp]].

=--

+-- {: .num_prop}
###### Definition

We say that the [[loop space object]] $\Omega \exp(\mathfrak{g})$ is the **smooth $\infty$-group** exponentiating $\mathfrak{g}$.

=--



+-- {: .num_prop}
###### Proposition

The objects $\exp(\mathfrak{g}) \in Smooth \infty Grpd$ are
geometrically contractible:

$$
  \Pi \exp(\mathfrak{g}) \simeq *
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

Observe that every [[simplicial presheaf]] $X$ is the [[homotopy colimit]] over its component presheaves $X_n \in [CartSp_{smooth}^{op}, Set] \hookrightarrow [CartSp_{smooth}^{op}, sSet]_{loc}$

$$
  X \simeq \mathbb{L} {\lim_{\to}}_n X_n
  \,.
$$

(Use for instance the injective model structure for which $X_\bullet$ is cofibrant in the [[Reedy model structure]] $[\Delta^{op},[CartSp_{smooth}^{op}, sSet]_{inj,loc}]_{Reedy}$ ).

Therefore it is sufficient to show that in each degree $n$ the [[0-truncated]] object $\exp(\mathfrak{g})_{n}$ is geometrically contractible. To exhibit a geometric contraction, choose for each $n \in \mathbb{N}$, a smooth retraction

$$
  \eta_n : \Delta^n \times [0,1] \to \Delta^n  
$$

of the $n$-[[simplex]]: a smooth map such that $\eta_n(-,1) = Id$ and $\eta_n(-,0)$ factors through the point.


We claim that this induces a diagram of presheaves

$$
  \array{
     \exp(\mathfrak{g})_n
      \\
      {}^{\mathllap{(id,1)}}\downarrow & \searrow^{\mathrm{id}}
      \\
     \exp(\mathfrak{g})_n \times [0,1] &\stackrel{\eta_n^*}{\to}& \exp(\mathfrak{g})_n
      \\
      {}^{\mathllap{(id,0)}}\uparrow & & \uparrow
      \\
      \exp(\mathfrak{g})_n &\to& *
  }
  \,,
$$

where over $U \in CartSp$ the middle morphism is given by

$$
  \eta_n^*  
     : 
     (\alpha, f)
      \mapsto 
    (f,\eta_n)^* \alpha
  \,,
$$

where 

* $\alpha : CE(\mathfrak{g}) \to \Omega^\bullet_{vert}(U \times \Delta^n)$ is an element of the set $\exp(\mathfrak{g})_n(U)$, 

* $f$ is an element of $[0,1](U)$;

* $(f,\eta_n)$ is the composite morphism

  $$
    U \times \Delta^n  
       \stackrel{(Id,f)\times id}{\to}
    U \times [0,1] \times \Delta^n
      \stackrel{(Id,\eta_n)}{\to}
    U \times \Delta^n
    \;
  $$

* $(f,\eta)^* \alpha$ is the postcomposition of $\alpha$ with
  the image of $(f,\eta_n)$ under $\Omega^\bullet_{vert}(-)$.

Here the last item is well defined given the [[coequalizer]] definition of $\Omega^\bullet_{vert}$ because $(f,\eta_n)$ is a morphism of [[bundle]]s over $U$

$$
  \array{
    U \times \Delta^n  
       &\stackrel{(id,f) \times id}{\to}&
    U \times [0,1] \times \Delta^n
      &\stackrel{id \times \eta_n}{\to}&
    U \times \Delta^n
    \\
    \downarrow && \downarrow && \downarrow
    \\
    U &\stackrel{id}{\to}& U &\stackrel{id}{\to}& U
  }
  \,.
$$

Similarly, for $h : K \to U$ any morphism in [[CartSp]]${}_{smooth}$ the [[natural transformation|naturality]] condition for a morphism of [[presheaves]] follows from the fact that the composites of [[bundle]] morphisms

$$
  \array{
    K \times \Delta^n
     &\stackrel{h \times id}{\to}&
    U \times \Delta^n  
       &\stackrel{(Id,f)\times id}{\to}&
    U \times [0,1] \times \Delta^n
      &\stackrel{(Id,\eta_n)}{\to}&
    U \times \Delta^n
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    K &\stackrel{h}{\to}& U &\stackrel{id}{\to}& U &\stackrel{id}{\to}& U
  }
$$

and

$$
  \array{
    K \times \Delta^n  
       &\stackrel{((id,f \circ h) \times id }{\to}&
    K \times [0,1] \times \Delta^n
      &\stackrel{id \times \eta_n}{\to}&
    K \times \Delta^n
      &\stackrel{h \times id}{\to}&
    U \times \Delta^n
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    K &\stackrel{id}{\to}& K &\stackrel{id}{\to}& K
     &\stackrel{h}{\to}& 
   U
  }
$$

coincide.

Moreover, notice that the lower morphism in our diagram of presheaves indeed factors through the point as indicated, becase for an [[L-∞ algebra]] $\mathfrak{g}$ we have that the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ is in degree 0 the ground field algebra algebra $\mathbb{R}$, so that there is a unique morphism $CE(\mathfrak{g}) \to \Omega^\bullet_{vert}(U \times \Delta^0) \simeq C^\infty(U)$ in $dgAlg$.

Finally, since $[0,1]$ is a [[contractible]] [[paracompact manifold]], we have that $\Pi([0,1]) \simeq *$ by the [above proposition](#StrucGeometricHomotopy). Therefore the above diagram of presheaves presents a geometric homotopy in $Smooth \infty Grpd$ from the identity map to a map that factors through the point.

By the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Homotopy">propositon about geometric homotopy</a> in a [[cohesive (∞,1)-topos]] it follows that 
$\Pi(\exp(\mathfrak{g})_n) \simeq *$ for all $n \in \mathbb{N}$.
And since $\Pi$ preserves the [[homotopy colimit]] $\exp(\mathfrak{g}) \simeq \mathbb{L} {\lim_\to}_n \exp(\mathfrak{g})_n$ we have that $\Pi(\exp(\mathfrak{g})) \simeq *$, too.

=--

+-- {: .num_remark}
###### Remark

We may think of $\Omega \exp(\mathfrak{g})$ as the smooth 
**[[n-connected|∞-simply connected]] [[Lie integration]]**
of $\mathfrak{g}$.

Notice however that $\Omega \exp(\mathfrak{g}) \in Smooth \infty$
in general has nontrivial and interesting 
[[categorical homotopy groups in an (infinity,1)-topos|categorical homotopy groups]].
The above statement says that its 
_[[geometric homotopy groups in an (infinity,1)-topos|geometric homotopy groups]]_ vanish .

=--

##### For a Lie algebra

Let $\mathfrak{g} \in L_\infty$ be an ordinary (finite dimensional) [[Lie algebra]]. Standard [[Lie theory]] (see [[Lie's three theorems]]) provides a [[simply connected]] [[Lie group]] $G$ integrating $\mathfrak{g}$.


With $G$ regarded as a [smooth ∞-group](#LieGroups) write $\mathbf{B}G \in Smooth\infty Grpd$ for its [[delooping]]. Recall from [above](#LieGroups) the standard presentation of this by a simplicial presheaf $\mathbf{B}G_c \in [CartSp_{smooth}^{op}, sSet]$.


+-- {: .num_prop}
###### Proposition

The operation of [[parallel transport]] $P \exp(\int -) : \Omega^1([0,1], \mathfrak{g}) \to G$ yields a weak equivalence (in $[CartSp^{op}, sSet]_{proj}$)

$$
  P \exp(\int - )
  :
  \mathbf{cosk}_3 \exp(\mathfrak{g}) 
  \simeq 
   \mathbf{cosk}_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G_c
  \,.
$$

=--

The proof is spelled out at [[Lie integration]]. In the section <a href="http://nlab.mathforge.org/nlab/show/Lie+integration#LieAlgebrasToLieGroups">Integrating Lie algebras to Lie groups</a>.




##### For a line Lie $n$-algebra

Let $n \in \mathbb{N}$, $n \geq 1$.

+-- {: .num_defn #LineLieNAlgebra}
###### Definition

Write 

$$
  b^{n-1} \mathbb{R} \in L_\infty
$$ 

for the [[L-∞-algebra]] whose [[Chevalley-Eilenberg algebra]] is given by a single generator in degree $n$ and vanishing differential. We call this the 
**[[line Lie n-algebra]]**

=--


+-- {: .num_prop}
###### Observation

The [[discrete ∞-groupoid]] underlying $\exp(b^{n-1} \mathbb{R})$ is given by the [[Kan complex]] that in degree $k$ has the set of closed differential $n$-forms (with sitting instants) on the $k$-[[simplex]]

$$
  \Gamma(\exp(b^{n-1} \mathbb{R}))
  : 
  [k] \mapsto \Omega^n_{si,cl}(\Delta^k)
$$

=--

+-- {: .num_defn}
###### Definition

We write equivalently

$$
  \mathbf{B}^n \mathbb{R}_{smp} := \exp(b^{n-1}\mathbb{R})
  \in
  [CartSp_{smooth}^{op}, sSet]
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

We have that $\mathbf{B}^n \mathbb{R}_{smp}$ is a presentation of the [smooth line n-group](#CircleLienGroup) $\mathbf{B}^{n} \mathbb{R}$.

Concretely, with $\mathbf{B}^n \mathbb{R}_{chn} \in [CartSp_{smooth}^{op}, sSet]$ the standard presentation given under the [[Dold-Kan correspondence]] by the chain complex of sheaves concentrated in degree $n$ on $C^\infty(-, \mathbb{R})$ the equivalence is induced by the [[fiber integration]] of differential $n$-forms over the $n$-[[simplex]]:

$$
  \int_{\Delta^\bullet} 
   : 
  \mathbf{B}^n \mathbb{R}_{smp}
   \stackrel{\simeq}{\to}
  \mathbf{B}^{n} \mathbb{R}_{chn}
  \,.
$$

=--

The proof of this is spelled out at _[[Lie integration]]_ in the section <a href="http://nlab.mathforge.org/nlab/show/Lie+integration#IntegrationToLineNGroup">Integration to line n-groups</a>.


#### Flat coefficients 
 {#FlatCoeffsForExponentiated}

We consider now the [flat coefficient objects](#StrucFlat) 
$\mathbf{\flat} \exp(\mathfrak{g})$ of [exponentiated ∞-Lie algebras](#StrucLieAlg) $\exp(\mathfrak{g})$.


+-- {: .num_defn #FlatCoefficientsForLieNGroupSimplicial}
###### Definition

Write $\mathbf{\flat}\exp(\mathfrak{g})_{smp}$ for the simplicial presheaf given by

$$
  \mathbf{\flat}\exp(\mathfrak{g})_{smp}
  :
  (U,[n]) \mapsto
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega_{si}^\bullet(U \times \Delta^n))
  \,.
$$

=--

+-- {: .num_prop #FactorizatonForExponentiatedFlatInclusion}
###### Proposition

The canonical morphism 
$\mathbf{\flat} \mathbf{B}^n \mathbb{R} \to \mathbf{B}^n \mathbb{R}$
in $Smooth \infty Grpd$ is presented in $[CartSp_{smooth}^{op}, sSet]$
by the composite

$$
  const \Gamma \exp(b^{n-1} \mathbb{R})
  \to
  \mathbf{\flat} \exp(b^{n-1} \mathbb{R})_{smp}
  \to
  \exp(b^{n-1} \mathbb{R})
  \,,
$$

where the first morphism is a weak equivalence and the second a 
fibration in $[CartSp_{smooth}^{op}, sSet]_{proj}$.

=--

We discuss the two morphisms in the composite separately in two
lemmas.

+-- {: .num_lemma }
###### Lemma

The canonical inclusion

$$
  const \Gamma(\exp(\mathfrak{g}))
   \to
  \mathbf{\flat}\exp(\mathfrak{g})_{smp}
$$

is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--


+-- {: .proof}
###### Proof

The morphism in question is on each object $U \in CartSp$ the morphism of simplicial sets

$$
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega_{si}^\bullet(\Delta^k))
  \to
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega_{si}^\bullet(U \times \Delta^k))
  \,,
$$

which is given by pullback of [[differential form]]s along the projection $U \times \Delta^k \to \Delta^k$.


To show that for fixed $U$ this is a weak equivalence in the standard [[model structure on simplicial sets]] we produce objectwise a left inverse 

$$
  F_U
  :
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega_{si}^\bullet(U \times \Delta^\bullet))
  \to
  Hom_{dgAlg}(CE(\mathfrak{g}), \Omega_{si}^\bullet(\Delta^\bullet))
$$

and show that this is an acyclic fibration of simplicial sets. The statement then follows by the [[category with weak equivalences|2-out-of-3]]-property of weak equivalences.

We take $F_U$ to be given by evaluation at $0: * \to U$, i.e. by postcomposition with the morphisms

$$
  \Omega^\bullet(U \times \Delta^k )
  \stackrel{Id \times 0^*}{\to}
  \Omega^\bullet(* \times \Delta^k )
  =
  \Omega^\bullet(\Delta^k)
  \,.
$$

(This of course is not natural in $U$ and hence does not extend to a morphism of simplicial presheaves. But for our argument here it need not.)

The morphism $F_U$ is an acyclic [[Kan fibration]] precisely if all diagrams of the form

$$  
  \array{
    \partial \Delta[n] &\to&
    Hom(CE(\mathfrak{g}), \Omega_{si}^\bullet(U \times \Delta^\bullet ))
    \\
    {}^{\mathllap{}}\downarrow && \downarrow^\mathrlap{F_U}
    \\
    \Delta[n]
    &\stackrel{}{\to}&
    Hom(CE(\mathfrak{g}), \Omega_{si}^\bullet(\Delta^\bullet))
  }
$$

have a lift. 
Using the [[Yoneda lemma]] over the [[simplex category]] and since the differential forms on the simplices have sitting instants, we may, as above, equivalently reformulate this in terms of spheres as follows:

for every morphism $CE(\mathfrak{g}) \to \Omega^\bullet_{si}(D^n)$ and morphism $CE(\mathfrak{g}) \to \Omega^\bullet_{si}(U \times S^{n-1})$ such that the diagram

$$
  \array{
    CE(\mathfrak{g}) &\to& \Omega^\bullet(U \times S^{n-1})
    \\
    \downarrow && \downarrow
    \\
    \Omega_{si}^\bullet(D^n) &\to& \Omega^\bullet(S^{n-1})
  }
$$

commutes, this may be factored as

$$
  \array{
   CE(\mathfrak{g})
   \\
   & \searrow
   \\
   &&\Omega_{si}^\bullet(U \times D^n)
   &\to& \Omega^\bullet(U \times S^{n-1})
    \\
    &&\downarrow && \downarrow
    \\
    &&\Omega^\bullet(D^n) &\to& \Omega^\bullet(S^{n-1})
  }
  \,.
$$

(Here the subscript "${}_{si}$" denotes differential forms on the disk that are radially constant in a neighbourhood of the boundary.)

This factorization we now construct. 

Let first $f : [0,1] \to [0,1]$ be any smoothing function, i.e. a [[smooth function]] which is surjective, non-decreasing, and constant in a neighbourhood of the boundary. Define a smooth map

$$
  U \times [0,1] \to U 
$$

by 

$$
  (u,\sigma) \mapsto u \cdot f(1-\sigma)
  \,,
$$

where we use the multiplicative structure on the [[Cartesian space]] $U$. This function is the identity at $\sigma = 0$ and is the constant map to the origin at $\sigma = 1$. It exhibits a smooth contraction of $U$.

Pullback of differential forms along this map produces a morphism

$$
  \Omega^\bullet(U \times S^{n-1}) 
  \to 
  \Omega^\bullet(U \times S^{n-1} \times [0,1])
$$

which is such that a form $\omega$ is sent to a form which in a neighbourhood $(1-\epsilon,1]$ of $1 \in [0,1]$ is constant along $(1-\epsilon,1] \times U$ on the value $(0 , Id_{S^{n-1}})^* \omega$.

(Notice that this step does not respect vertical forms.
This is the crucial difference between 
$\{\Omega^\bullet_{si}(U \times \Delta ^k) \leftarrow CE(\mathfrak{g})\}$ and 
$\{\Omega^\bullet_{si,vert}(U \times \Delta ^k) \leftarrow CE(\mathfrak{g})\}$).

Let now $0 \lt \epsilon \in \mathbb{R}$ some value such that the given forms $CE(\mathfrak{g}) \to \Omega^\bullet_{si}(D^k)$ are constant a distance $d \leq \epsilon$ from the boundary of the disk. Let $q : [0,\epsilon/2] \to [0,1]$ be given by multiplication by $1/(\epsilon/2)$ and $h : D_{1-\epsilon/2}^k \to D_1^n$ the injection of the $n$-disk of radius $1-\epsilon/2$ into the unit $n$-disk.

We can then glue to the morphism

$$
  CE(\mathfrak{g}) \to
  \Omega^\bullet(U \times S^{n-1})
  \to
  \Omega^\bullet(U \times [0,1] \times S^{n-1})
  \stackrel{id \times q^* \times id}{\to_\simeq}
  \Omega^\bullet(U \times [0,\epsilon/2] \times S^{n-1})   
$$

to the morphism

$$
  CE(\mathfrak{g}) \to \Omega^\bullet(D^n)
  \to
  \Omega^\bullet(U \times \{1\} \times D^n)
  \stackrel{h^*}{\to_\simeq}
  \Omega^\bullet(U \times \{1\} \times D^n_{1-\epsilon/2})
$$

by smoothly identifying the union $[0,\epsilon/2] \times S^{n-1} \coprod_{S^{n-1}} D^n_{1-\epsilon/2}$ with $D^n$ (we glue a disk into an annulus to obtain a new disk) to obtain in total a morphism

$$
  CE(\mathfrak{g}) \to \Omega^\bullet(U \times D^n)
$$

with the desired properties: at $u = 0$ the homotopy that we constructed is constant and the above construction hence restricts the forms to radius $\leq 1-\epsilon/2$ and then extends back to radius $\leq 1$ by the constant value that they had before. Away from 0 the homotopy in the rmaining $\epsilon/2$ bit smoothly interpolates to the boundary value.


=--

+-- {: .num_lemma }
###### Lemma

The canonical morphism

$$
  \mathbf{\flat}\exp(\mathfrak{g})_{smp}
  \to 
  \exp(\mathfrak{g})
$$

is a fibration in $[CartSp_{smooth}^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

Over each $U \in CartSp$
the morphism is induced from the morphism of dg-algebras

$$
  \Omega^\bullet(U) \to C^\infty(U)
$$

that discards all differential forms of non-vanishing degree. 

It is sufficient to show that for 

$$
  CE(\mathfrak{g}) 
    \to 
   \Omega_{si,vert}^\bullet(
     U \times (D^n \times [0,1])
   )
$$

a morphism and 

$$
  CE(\mathfrak{g}) \to \Omega^\bullet_{si}(U \times D^n )
$$

a lift of its restriction to $\sigma = 0 \in [0,1]$ we have an extension to a 
lift 

$$
  CE(\mathfrak{g}) \to \Omega_{si,vert}^\bullet(U \times (D^n \times [0,1]))
  \,.
$$

From these lifts all the required lifts are obtained by precomposition with some evident smooth retractions.


The idea of the proof is that the lifts in question are obtained from solving [[differential equation]]s with boundary conditions, and exist due to the existence of solutions of first order systems of partial differential equations and the [[Bianchi identities]] for flat [[∞-Lie algebroid valued differential forms]].


**1st case: $\mathfrak{g} = b^{n-1} \mathbb{R}$**

We condsider the case $\mathfrak{g} = b^{n-1} \mathbb{R}$.

A morphism 
$CE(b^{n-1} \mathbb{R}) \to \Omega_{si,vert}^\bullet( U \times (D^k \times [0,1]))$ is a $U$-parameterized family of $n$-forms 
$A = A_{D^k} + (d \sigma) \wedge \lambda  $ on $D^k \times [0,1]$ 
satisfying

$$
  d_{D^k} A_{D^k} = 0
$$

and

$$
  \partial_\sigma A_{D^k} = d_{D^k} \lambda
  \,.
$$

Consider a lift 
of the restriction to $\sigma = 0$ by a term
$A_{D^k} + A_{U  \times D^k}$ 
being a morphism
$CE(b^{n-1}\mathbb{R}) \to \Omega^\bullet_{si}(U \times D_k )$. 

We can extend this to a morphism
$CE(b^{n-1}\mathbb{R}) \to \Omega^\bullet_{si}(U \times D_k \times [0,1])$
by lifting $\lambda$ without adding any terms to it and
solving the differential equation

$$
  \partial_\sigma (A_{D^k} + A_{U \times D^k} ) = (d_U + d_{D^k}) \lambda
  \,,
$$

equivalently for the new term

$$
  \partial_\sigma A_{U \times D^k}  = d_U \lambda
  \,,
$$

with boundary condition the given value at $\sigma = 0$.

For this unique solution to be a lift we need in addition that 
$(d_U + d_{D^k}) (A_{D^k} + A_{U \times D^k}) = 0$. Since this is the case at $\sigma = 0$ by assumption of the lift at that end, we need to check that

$$
  \partial_\sigma (d_U + d_{D^k}) (A_{D^k} + A_{U \times D^k}) = 0
  \,.
$$

But by the above this follows from the [[Bianchi identity]], which for the special abelian case that we are considering is just the nilpotency of the de Rham differential

$$
  \cdots = 
  (d_U + d_{D^k}) (d_U + d_{D^k}) (A_{D^k} + A_{U \times D^k}) = 0
  \,.
$$



**2nd case: $\mathfrak{g} an arbitrary Lie algebra$**

Now let $\mathfrak{g}$ be an ordinary Lie algebra. Choose a dual basis $\{t^a\}$ and structue constants $C^a{}_{b c}$. We get a discussion analogous to the above with structure constant terms thrown in:

the original element is a collection of 1-forms $A^a_v d v + A^a_\sigma d \sigma $ satisfying

$$
  \partial_\sigma A_v^a = \partial_v A_\sigma 
   - C^a{}_{b c} A_v^b A_\sigma^c
  \,.
$$

We lift by adding a term $A_u^a d u$ that is uniquely fixed by the condition that it solves the differential equation

$$
  \partial_\sigma A_u = \partial_u A_\sigma 
  - C^a{}_{b c} A_\sigma^b  A_u^c
$$

for given boundary value at $\sigma = 0$.

We need to show that the lift found this way also satisfies the equation

$$
  F_{v u}^a
  :=
  \partial_v A^a_u - \partial_u A^a_v + C^a{}_{b c} A_v^b A_u^c = 0
  \,.
$$

By assumption, this is true at $\sigma = 0$. We now show that the $\sigma$-derivative of this expression satisfies the Binachi-type equation

$$
  \partial_\sigma F^a_{v u} 
  = 
  C^a{}_{b c} A^b_\sigma F^c_{v u} 
  \,.
$$

A solution to this differential equation with initial value 0 is $F^a_{v u} = 0$. Since this solution is guaranteed to be unique, we will have shown our claim.

Now compute:

$$
  \begin{aligned}
    \partial_\sigma F^a_{u v} 
    &:=
    \partial_\sigma \partial_u A^a_v -
    \partial_\sigma \partial_v A^a_u
    +
    \partial_\sigma C^a{}_{b c} A_u^b A^c_v
    \\
    & =
    \partial_u \partial_\sigma  A^a_v -
    \partial_v \partial_\sigma  A^a_u
    +
    \partial_\sigma C^a{}_{b c} A_u^b \wedge A^c_v
    \\
    &=
    \partial_u 
    (\partial_v A^a_\sigma - C^a{}_{b c} A^b_\sigma A^c_v)
    -
    \partial_v 
    (\partial_u A^a_\sigma - C^a{}_{b c} A^b_\sigma A^c_u)
    +
    \partial_\sigma C^a{}_{b c} A_u^b A^c_v
    \\
    & =
    \partial_u C^a{}_{b c} A^b_\sigma A^c_v
    -
    \partial_v C^a{}_{b c} A^b_\sigma A^c_u
    +
    \partial_\sigma C^a{}_{b c} A_u^b A^c_v    
    \\
    & =
    C^a{}_{b c} A^b_\sigma  (\partial_u A^c_v - 
    \partial_v A^c_u)
    +
    C^a{}_{b c} 
     (\partial_\sigma A^b_u - C^b{}_{d e} A^d_u A^e_\sigma)
     A^c_v
    -
    C^a{}_{b c} 
     (\partial_\sigma A^b_\nu - C^b{}_{d e} A^d_v A^e_\sigma)
     A^b_u
   + 
   \partial_\sigma C^a{}_{b c} A^b_v A^c_u
   \\
   & =
   C^a{}_{b c} A^c_\sigma F^b_{u v}   
\end{aligned}
  \,.
$$  

Here in the last step we use the [[Jacobi identity]]

$$
  C^a{}_{b c} C^b{}_{d e}
  +
  C^a{}_{b d} C^b{}_{e c}
  +
  C^a{}_{b e} C^b{}_{c d}
  = 0
  \,.
$$


**general case**

For $\mathfrak{g}$ a general $L_\infty$-algebra, the computation is essentially as above for the Lie algebra case only that all indices become multi-indices in a suitable sense. 

For instance the structure constants  now have components of arbitrary arity. But for the discussion of the lift it is still always just the components with two legs along the $u$-, $v$-, $\sigma$- direction that matter, all other indices just run along.

I'll try to think of a convenient notation to express this.

=--

##### For a line Lie $n$-algebra {#LieIntDiffCoeffsForLineGroups}


We have discussed now two different presentations for the flat coefficient object $\mathbf{\flat}\mathbf{B}^n \mathbb{R}$:

1. $\mathbf{\flat} \mathbf{B}^n \mathbb{R}_{chn}$ -- discussed [here](#FlatCoefficientsForCircleNGroup);

1. $\mathbf{\flat} \mathbf{B}^n \mathbb{R}_{smp}$ -- discusse [here](#FlatCoefficientsForLieNGroupSimplicial);


There is an evident degreewise map

$$
  (-1)^{\bullet+1}
  \int_{\Delta^\bullet} :
  \mathbf{\flat} \mathbf{B}^n \mathbb{R}_{smp}
  \to  
  \mathbf{\flat} \mathbf{B}^n \mathbb{R}_{chn}
$$

that sends a closed $n$-form $\omega \in \Omega^n_{cl}(U \times \Delta^k)$ to $(-1)^{k+1}$ times  its [[fiber integration]] $\int_{\Delta^k} \omega$.

+-- {: .num_prop}
###### Proposition

This map yields a morphism of simplicial presheaves

$$
  \int : 
   \mathbf{\flat} \mathbf{B}^n \mathbb{R}_{smp}
     \to
   \mathbf{\flat} \mathbf{B}^n \mathbb{R}_{chn}
$$

which is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

First we check that we have a morphism of [[simplicial set]]s over each $U \in CartSp$. Since both objects are abelian [[simplicial group]]s we may, by the [[Dold-Kan correspondence]], check the statement for  sheaves of [[Moore complex|normalized chain complexes]].

Notice that the chain complex differential on the forms 
$\omega \in \Omega^n_{cl}(U \times \Delta^k)$ on simplices
sends a form to the alternating sum of its restriction to the faces of the
simplex. Postcomposed with the integration map this is the operation 
$\omega \mapsto \int_{\partial \Delta^k} \omega$ of integration over the boundary.

Conversely, first integrating over the simplex and then applying the de Rham differential on $U$ yields

$$
  \begin{aligned}
     \omega \mapsto (-1)^{k+1} d_U \int_{\Delta^k} \omega
      &= 
      - \int_{\Delta^k} d_U \omega
      \\
      & = \int_{\Delta^k} d_{\Delta^k} \omega
      \\
      & =  \int_{\partial \Delta^k} \omega
  \end{aligned}
  \,,
$$

where we first used that $\omega$ is closed, so that $d_{dR} \omega = (d_U + d_{\Delta^k}) \omega = 0$, and then used [[Stokes' theorem]].
Therefore we have indeed objectwise a chain map.

By the discussion of the two objects we already know that both present the [[homotopy type]] of $\mathbf{\flat} \mathbf{B}^n \mathbb{R}$. Therefore it suffices to show that the integration map is over each $U \in CartSp$ an isomorphism on the [[simplicial homotopy group]] in degree $n$.

Clearly the morphism

$$
  \int_{\Delta^n} : \Omega^\bullet_{si,cl}(U  \times \Delta^n)
  \to 
  C^\infty(U, \mathbb{R})
$$

is surjective on degree $n$ homotopy groups: for $f : U \to * \to \mathbb{R}$  constant, a preimage is $f \cdot vol_{\Delta^n}$, the normalized [[volume form]] of the $n$-[[simplex]] times $f$.

Moreover, these preimages clearly span the whole homotopy group $\pi_n (\mathbf{\flat} \mathbf{B}^n \mathbb{R}) \simeq \mathb{R}_{disc}$ (they are in fact the images of the weak equivalence $const \Gamma \exp(b^{n-1}\mathbb{R}) \to \mathbf{\flat} \mathbf{B}^n \mathbb{R}_{smp}$ ) and the integration map is injective on them. Therefore it is an isomorphism on the homotopy groups in degree $n$.

=--

#### de Rham coefficients {#DifferentialCoefficientsOfLieInt}

We now consider the [de Rham coefficient object](#StrucDeRham) 
$\mathbf{\flat}_{dR} \exp(\mathfrak{g})$ of [exponentiated L-∞ algebras](#StrucLieAlg) $\exp(\mathfrak{g})$.


+-- {: .num_cor}
###### Corollary

For $\mathfrak{g} \in L_\infty$ a representive in $[CartSp^{op}, sSet]_{proj}$ of the object de Rham coefficient object
$\mathbf{\flat}_{dR} \exp(\mathfrak{g})$ is the presheaf

$$
  \mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}_{smp}
  :
  (U,[n])
  \mapsto
   Hom_{dgAlg}(
     CE(\mathfrak{g}),
     \Omega_{si}^{\bullet\geq 1,\bullet}(U \times \Delta^n)
  )
  \,,
$$

where the notation on the right denotes the dg-algebra of differential forms on $U \times\Delta^n$ that (apart from having sitting instants on the faces of $\Delta^n$) are along $U$ of non-vanishing degree.

=--

+-- {: .proof}
###### Proof

By the [above proposition](#FactorizatonForExponentiatedFlatInclusion)
we may present the defining [[(∞,1)-pullback]] 
$\mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R} := 
* \times_{\mathbf{B}^n \mathbb{R}} \mathbf{\flat} \mathbf{B}^n \mathbb{R}$
in $Smooth \infty Grpd$ by the ordinary pullback

$$
  \array{
    \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{smp} &\to&
      \mathbf{\flat}\mathbf{B}^n \mathbb{R}_{smp}
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}^n \mathbb{R}   
  }
$$

in $[CartSp_{smooth}^{op}, sSet]$.

=--


##### For a line Lie $n$-algebra {#LieIntDiffCoeffsForLineGroups}

We have discussed now two different presentations for the de Rham coefficient object $\mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}$:

1. $\mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}_{chn}$ -- discussed [here](#OrdinaryDeRham);

1. $\mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}_{smp}$ -- discussed [here](#DifferentialCoefficientsOfLieInt);



There is an evident degreewise map

$$
  (-1)^{\bullet+1}
  \int_{\Delta^\bullet} :
  \mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}_{smp}
  \to  
  \mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}_{chn}
$$

that sends a closed $n$-form $\omega \in \Omega^n_{cl}(U \times \Delta^k)$ to $(-1)^{k+1}$ times  its [[fiber integration]] $\int_{\Delta^k} \omega$.

+-- {: .num_prop #FiberIntegrationAsWeakEquivalenceForDeRhamCoefficientPresentations}
###### Proposition

This map yields a morphism of simplicial presheaves

$$
  \int : 
   \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{smp}
     \to
   \mathbf{\flat}_{dR} \mathbf{B}^n \mathbb{R}_{chn}
$$

which is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

By the [[Dold-Kan correspondence]] we may check the statement for 
sheaves of (normalized) chain complexes.

Notice that the chain complex differential on the forms 
$\omega \in \Omega^n_{cl}(U \times \Delta^k)$ on simplices
sends a form to the alternating sum of its restriction to the faces of the
simplex. Postcomposed with the integration map this is the operation
$\omega \mapsto \int_{\partial \Delta^k} \omega$.

Conversely, first integrating over the simplex and then applying the de Rham differential on $U$ yields

$$
  \begin{aligned}
     \omega \mapsto (-1)^{k+1} d_U \int_{\Delta^k} \omega
      &= 
      - \int_{\Delta^k} d_U \omega
      \\
      & = \int_{\Delta^k} d_{\Delta^k} \omega
      \\
      & =  \int_{\partial \Delta^k} \omega
  \end{aligned}
  \,,
$$

where we first used that $\omega$ is closed, so that $d_{dR} \omega = (d_U + d_{\Delta^k}) \omega = 0$, and then [[Stokes' theorem]].

Therefore we have indeed objectwise a chain map.

To see that it gives a weak equivalence, notice that this morphism is the morphism on pullbacks induced from the weak equivalence of diagrams

$$
  \array{
    * &\to& \exp(b^{n-1}\mathbb{R}) &\leftarrow& \mathbf{\flat}\mathbf{B}^n \mathbb{R}_{smp}
    \\
    \downarrow^{\mathrlap{=}} 
    && 
    {}^{\mathllap{\pm \int_{\Delta^\bullet}}} \downarrow^{\mathrlap{\simeq}}
    &&
    {}^{\mathllap{\pm \int_{\Delta^\bullet}}} \downarrow^{\mathrlap{\simeq}}
    \\
    * &\to& \mathbf{B}^n \mathbb{R}_{chn} &
      \leftarrow& \mathbf{\flat}\mathbf{B}^n \mathbb{R}_{chn}
  }
  \,.
$$

Since both of these pullbacks are [[homotopy pullback]]s by the above discussion, the induced morphism between the pullbacks is also a weak equivalence.

=--





### Maurer-Cartan forms and curvature characteristic forms {#StrucCurvatureForms}

We discuss the 
<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">intrinsic Maurer-Cartan and curvature characteristic forms</a> defined in any cohesive $(\infty,1)$-topos
realized in $Smooth \infty Grpd$.

#### The canonical form on a Lie group   
 {#CanonicalFormOnLieGroup}

Let $G$ be a [[Lie group]]. Write $\mathfrak{g}$ for 
its [[Lie algebra]].


+-- {: .num_prop }
###### Proposition

Under the identification

$$
  Smooth \infty Grpd(X, \mathbf{\flat}_{dR}\mathbf{B}G)
  \simeq
  \Omega^1_{flat}(X,\mathfrak{g})
$$

from [the above proposition](#LieGroupDeRhamCohomology), for $X \in $ [[SmoothMfd]], we have that the canonical morphism

$$
  \theta : G \to \mathbf{\flat}_{dR} \mathbf{B}G
$$

in $Smooth \infty Grpd$ corresponds to the 
ordinary [[Maurer-Cartan form]] on $G$.


=--


+-- {: .proof}
###### Proof

We compute the defining double [[(∞,1)-pullback]]

$$
  \array{
    G &\to& *
    \\
    {}^{\mathllap{\theta}}\downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat} \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
$$

in $Smooth \infty Grpd$ as a [[homotopy pullback]]
in $[CartSp_{smooth}^{op}, sSet]_{proj}$

In the above [discussion of differential coefficients](#LieGroupDeRhamCoefficients) we already modeled the lower $(\infty,1)$-pullback square by the ordinary pullback 

$$
  \array{
    \mathbf{\flat}_{dR}\mathbf{B}G_c
      &\to&
    \mathbf{\flat}\mathbf{B}G_c
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G_c
  }
$$

A standard fibration replacement of the point inclusion
$* \to \mathbf{\flat}\mathbf{B}G $ is
(as discussed at [[universal principal ∞-bundle]]) 
given by replacing the point by the presheaf that assigns groupoids of the form


$$
  Q : 
  U \mapsto 
  \left\{
    \array{
       && A_0 = 0
       \\
       & {}^{\mathllap{g_1}}\swarrow && \searrow^{\mathrlap{g_2}}
       \\
       A_1 &&\stackrel{h}{\to}&& A_2
    }
  \right\}
  \,,
$$

where on the right the commuting triangle is in 
$(\mathbf{\flat}_{dR}\mathbf{B}G_c)(U)$ and here regarded as a morphism from $(g_1,A_1)$ to $(g_2,A_2)$. And the fibration $Q \to \mathbf{\flat}\mathbf{B}G_c$ is given by projecting out the base of these triangles.

The pullback of this along
$\mathbf{\flat}_{dR}\mathbf{B}G_c \to \mathbf{\flat}\mathbf{B}G_c$ is over each $U$  the restriction of the groupoid $Q(U)$ to its set of objects, hence is the [[sheaf]]

$$
  U \mapsto 
  \left\{
    \array{
       A_0 = 0
       \\
       \downarrow^{\mathrlap{g}}
       \\
       g^* \theta
    }
  \right\}
  \simeq 
  C^\infty(U,G)
  = G(U)
  \,,
$$

equipped with the projection

$$
 t_U :  G \to \mathbf{\flat}_{dR} \mathbf{B}G_c
$$

given by

$$
  t_U : (g : U \to G) \mapsto g^* \theta
  \,.
$$

Under the [[Yoneda lemma]] (over [[SmoothMfd]]) this 
identifies the morphism $t$ with the [[Maurer-Cartan form]]
$\theta \in \Omega^1_{flat}(G,\mathfrak{g})$.

=--


#### The universal curvature characteristic on $\mathbf{B}^n U(1)$   
 {#CurvatureCharacteristicOnCircleNGroup}

We discuss presentations of <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature characteristics</a> $\mathbf{B}^n U(1)\to \mthbf{\flat}_{dR}\mathbf{B}^{n+1} U(1)$ and $\mathbf{B}^n \mathbb{R}\to \mthbf{\flat}_{dR}\mathbf{B}^{n+1} \mathbb{R}$ in $Smooth \infty Grpd$ by constructions in $[CartSp_{smooth}^{op}, sSet]$.

Recall the discussion of $\mathbf{B}^n U(1)$ and of 
$\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ from 
[above](#StrucDeRham).

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ define the simplicial presheaf

$$
  \mathbf{B}^n U(1)_{diff,chn}
  :=
  \array{
    \Xi\left(
     0\stackrel{}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \right)
  }
  \,.
$$

=--


+-- {: .num_prop #CurvatureCharOnBnU1}
###### Proposition

The evident projection

$$
  \mathbf{B}^n U(1)_{diff,chn} \to \mathbf{B}^n U(1)_{chn}
$$

is a weak equivalence in $[CartSp^{op}, sSet]_{proj}$.
Moreover,  the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature characteristic</a> 

$$
  curv :  \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)
$$

in $Smooth \infty Grpd$ is presented in $[CartSp^{op}, sSet]_{proj,loc}$
by a span

$$
  \array{
    \mathbf{B}^n U(1)_{diff,chn} &\stackrel{curv_{chn}}{\to}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^n U(1)
  }
$$

where the horizontal morphism is the evident projection

$$ 
  \array{
    \Xi\left(\;
     0\stackrel{}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \right)
    \\
    \downarrow 
    \\
    \Xi\left(
    \; 0 \stackrel{}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to}
    \Omega^2(-)
    \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-))    
    \right)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof


We need to present the defining [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{B}^n U(1) &\to& *
    \\
    {}^{\mathllap{curv}}\downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1) &\to&
    \mathbf{\flat} \mathbf{B}^{n+1} U(1)
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}^{n+1} U(1)
  }
$$

by a [[homotopy pullback]] in $[CartSp^{op}, sSet]_{proj}$ (since [[(∞,1)-sheafification]] preserves finite [[(∞,1)-pullback]]s it is sufficient to present the $(\infty,1)$-pullback in [[(∞,1)-presheaves]]).

We claim that we have a commuting diagram

$$ 
  \array{
    \Xi(\;
     0\stackrel{}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \;)
    &\to&
    \Xi(\;
     C^\infty(-,U(1)) \stackrel{Id + d_{dR}}{\to}
    {C^\infty(-,U(1)) \atop \oplus \Omega^1(-)}
    \stackrel{d_{dR} - Id}{\to}
    {\Omega^1(-) \atop \oplus \Omega^2(-)}
    \stackrel{d_{dR} + Id}{\to}
    \cdots
    { \Omega^{n-1}(-) \atop \oplus \Omega^n(-)}
    \stackrel{d_{dR} \pm Id}{\to}
    \Omega^n(-)
    \;)
    \\
    \downarrow && \downarrow^{\mathrlap{(Id, p_2, p_2, \cdots, p_2,d_{dR})}}
    \\
    \Xi(
    \; 0 \stackrel{}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to}
    \Omega^2(-)
    \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-))    
    &\to&
    (C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) 
    \stackrel{d_{dR}}{\to} 
    \Omega^2(-)
    \stackrel{d_{dR}}{\to}
    \cdots \stackrel{d_{dR}}{\to} 
    \Omega_{cl}^{n+1}(-)
    \;)
    \\
    \downarrow && \downarrow
    \\
    \Xi(
     \; 0 \to 0 \to 0 \to \cdots \to 0\;)
    &\to&
    \Xi(
     \; C^\infty(-,U(1)) \to 0 \to 0 \to \cdots \to 0
     \;)
  }
$$

in $[CartSp^{op},sSet]_{proj}$ where

* the objects are fibrant models for the corresponding objects in the
  above $(\infty,1)$-pullback diagram;

* the two right vertical morphisms are fibrations;

* the two squares are [[nLab:pullback]] squares.

Therefore this is a [[homotopy pullback]] in $[CartSp^{op}, sSet]_{proj}$ that realizes the  [[(∞,1)-pullback]] in question. 

For the lower square we had discussed this already [above](#OrdinaryDeRham). For the upper square the same type of reasoning applies. The main point is to find the chain complex in the top right such that it is a [[resolution]] of the point and maps by a fibration onto our model for $\mathbf{\flat}\mathbf{B}^n U(1)$. The top right complex is

$$
  \array{
    &&
    C^\infty(-,U(1)) 
     &\stackrel{d_{dR}}{\to}&
    \Omega^1(-)
     &\stackrel{d_{dR}}{\to}&
    \Omega^2(-)
     &\stackrel{d_{dR}}{\to}&
     \cdots
     &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)
     \\
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \oplus 
     &{}^{\mathrlap{id}}\nearrow& \cdots  &
     {}^{\mathrlap{id}}\nearrow& 
     \\
    C^\infty(-,U(1)) 
     &\stackrel{d_{dR}}{\to}&
    \Omega^1(-)
     &\stackrel{d_{dR}}{\to}&
    \Omega^2(-)
     &\stackrel{d_{dR}}{\to}&
     \cdots
     &\stackrel{d_{dR}}{\to}&
      \Omega^n(-)
  }
$$

and the vertical map out of it into $C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-) \stackrel{}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n(-) \stackrel{d_{dR}}{\to} \Omega^{n+1}_{cl}(-)$ is in positive degree the projection onto the lower row and in degree 0 the de Rham differential. This is manifestly surjective (by the [[Poincare lemma]] applied to each object $U \in $ [[CartSp]]) hence this is a fibration.

The pullback object in the top left is in this notation

$$
  \mathbf{B}^n U(1)_{diff,chn}
  :=
  \Xi
  \left(
    \array{
      C^\infty(-,U(1)) 
       &\stackrel{d_{dR}}{\to}&
      \Omega^1(-)
       &\stackrel{d_{dR}}{\to}&
       \cdots
       &\stackrel{d_{dR}}{\to}&
        \Omega^n(-)
       \\
       \oplus 
       &{}^{\mathrlap{id}}\nearrow& \oplus 
       &{}^{\mathrlap{id}}\nearrow& \cdots  &
       {}^{\mathrlap{id}}\nearrow& 
       \\
      \Omega^1(-)
       &\stackrel{d_{dR}}{\to}&
       \cdots
       &\stackrel{d_{dR}}{\to}&
        \Omega^n(-)
    }
  \right)
$$

and in turn the top left vertical morphism $curv : \mathbf{B}_{diff}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ is in positive degree the projection on the lower row and in degree 0 the de Rham differential.

=--

Notice that the evident forgetful morphism $\mathbf{B}^n U(1) \stackrel{}{\leftarrow} \mathbf{B}^n_{diff} U(1)$ is indeed a weak equivalence.


In the section on [de Rham coefficients for exponentiated Lie algebras](#DifferentialCoefficientsOfLieInt) we had discussed an equivalent presentation of most of the objects above. We now formulate the curvature characteristic in this alternative form.


+-- {: .num_prop }
###### Observation

We may write the [[simplicial presheaf]] $\mathbf{\flat}_{dR}\mathbf{B}^{n+1} \mathbb{R}_{smp}$ from [above](#DifferentialCoefficientsOfLieInt) equivalently as follows

$$
  \mathbf{\flat}_{dR}\mathbf{B}^{n+1} \mathbb{R}_{smp}
  :
  (U, [k]) 
   \mapsto
  \left\{
    \array{
      \Omega^\bullet_{si,vert}(U \times \Delta^k)
       &\stackrel{0}{\leftarrow}& 0
       \\
       \uparrow && \uparrow
       \\
       \Omega_{si}^\bullet(U \times \Delta^k)
        &\stackrel{A}{\leftarrow}&
       CE(b^{n}\mathbb{R})
    }    
  \right\}
  \,,
$$


where on the right we have the set of [[commuting diagram]]s in [[dgAlg]] of the given form, with the vertical morphisms being the canonical projections.

=--

+-- {: .num_defn }
###### Definition

Write $W(b^{n-1}\mathbb{R}) \in $ [[dgAlg]] for the [[Weil algebra]] of the 
[[line Lie n-algebra]], defined to be the [[free functor|free]] commutative [[dg-algebra]] on a single generator in degree $n$, hence the graded commutative algebra on a generator in degree $n$ and a generator in degree $(n+1)$ equipped with the differential that takes the former to the latter.

=--

+-- {: .num_prop #PropertiesOfWeilAlgebraOfLineLienAlgebra}
###### Observation

We have the following properties of $\mathrm{W}(b^{n-1}\mathbb{R})$

* There is a canonical [[natural isomorphism]]

  $$
    Hom_{dgAlg}(W(b^{n-1} \mathbb{R}), \Omega^\bullet(U))
    \simeq
    \Omega^n(U)
  $$

  between [[dg-algebra]] 
  homomorphisms $A : W(b^{n-1}\mathbb{R}) \to \Omega^\bullet(X)$
  from the Weil algebra of $b^{n-1}\mathbb{R}$ to the 
  de Rham complex and degree-$n$ differential forms, 
  not necessarily closed.

* There is a canonical [[dg-algebra]] homomorphism 
  $W(b^{n-1}\mathbb{R}) \to CE(b^{n-1}\mathbb{R})$ and 
  the differential $n$-form corresponding to $A$ factors 
  through this morphism precisely if the 
  [[curvature]] $d_{dR} A$ of $A$ vanishes.

* The image under $\exp(-)$

  $$
    \exp(\mathrm{inn}(b^{n-1})\mathbb{R}) 
    \to 
    \exp(b^{n}\mathbb{R})
  $$

  of the canonical [[dg-algebra]] morphism 
  $\mathrm{W}(b^{n-1}\mathbb{R}) \leftarrow \mathrm{CE}(b^n \mathbb{R})$ is a fibration in $[\mathrm{CartSp}_{\mathrm{smooth}}^{\mathrm{op}}, \mathrm{sSet}]_{\mathrm{proj}}$ that presents the point inclusion ${*} \to \mathbf{B}^{n+1}\mathbb{R}$ in $\mathrm{Smooth}\infty \mathrm{Grpd}$.

=--

+-- {: .num_defn #DiffSmpForLineLienAlgebra}
###### Definition


Let $\mathbf{B}^n \mathbb{R}_{diff,smp} \in [CartSp_{smooth}^{op}, sSet]$ be the [[simplicial presheaf]] defined by

$$
  \mathbf{B}^n \mathbb{R}_{diff,smp} : (U,[k])
  \mapsto
  \left\{
    \array{
      \Omega^\bullet_{si,vert}(U \times \Delta^k)
       &\stackrel{A_{vert}}{\leftarrow}& CE(b^{n-1}\mathbb{R})
       \\
       \uparrow && \uparrow
       \\
       \Omega_{si}^\bullet(U \times \Delta^k)
        &\stackrel{A}{\leftarrow}&
       W(b^{n-1}\mathbb{R})
    }
  \right\}
  \,,
$$ 

where on the right we have the set of [[commuting diagram]]s in [[dgAlg]]
as indicated.

=--

+-- {: .num_remark }
###### Remark

This means that an element of $\mathbf{B}^n \mathbb{R}_{diff,smp}(U)[k]$ is a smooth $n$-form $A$ (with sitting instants) on $U \times \Delta^k$ such that its [[curvature]] $(n+1)$-form $d A$ vanishes when restricted in all arguments to [[vector field]]s tangent to $\Delta^k$. We may write this condition as $d A \in \Omega^{\bullet \geq 1, \bullet}_{si}(U \times \Delta^k)$.

=--

+-- {: .num_remark }
###### Remark

There are canonical morphisms 

$$
  \array{
    \mathbf{B}^n \mathbb{R}_{diff,smp}
     &\stackrel{curv_{smp}}{\to}& 
     \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_{smp}
    \\
    \downarrow
    \\
    \mathbf{B}^n \mathbb{R}_{smp}
  }
$$

in $[CartSp_{smooth}^{op}, sSet]$, where the vertical map is given by remembering only the top horizontal morphism in the above square diagram, and the horizontal morphism is given by
forming the [[pasting]] composite

$$
  curv_{smp} 
   : 
  \left\{
    \array{
      \Omega^\bullet_{si,vert}(U \times \Delta^k)
       &\stackrel{A_{vert}}{\leftarrow}& CE(b^{n-1}\mathbb{R})
       \\
       \uparrow && \uparrow
       \\
       \Omega_{si}^\bullet(U \times \Delta^k)
        &\stackrel{A}{\leftarrow}&
       W(b^{n-1}\mathbb{R})
    }
  \right\}
  \;\;
  \mapsto
  \;\;
  \left\{
    \array{
      \Omega^\bullet_{si,vert}(U \times \Delta^k)
       &\stackrel{A_{vert}}{\leftarrow}& CE(b^{n-1}\mathbb{R})
       &\leftarrow& 0
       \\
       \uparrow && \uparrow && \uparrow
       \\
       \Omega_{si}^\bullet(U \times \Delta^k)
        &\stackrel{A}{\leftarrow}&
       W(b^{n-1}\mathbb{R})
        &\stackrel{}{\leftarrow}&
       CE(b^{n}\mathbb{R})
    }
  \right\}  
  \,.
$$

=--

+-- {: .num_prop #CurvSmp}
###### Proposition 

This span is a presentation in $[CartSp_{smooth}^{op}, sSet]$ of the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">universal curvature characteristics</a> $curv : \mathbf{B}^n \mathbb{R} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}$ in $Smooth \infty Grpd$.

=--

+-- {: .proof}
###### Proof


We need to produce a fibration [[resolution]] of the point inclusion
$* \to \mathbf{\flat} \mathbf{B}^{n+1} \mathbb{R}_{smp}$ 
in $[CartSp_{smooth}^{op}, sSet]_{proj}$ and then show that
the above is the ordinary [[pullback]] of this along 
$\mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}_{smp} \to \mathbf{\flat} \mathbf{B}^{n+1} \mathbb{R}_{smp} $.

We claim that this is achieved by the morphism

$$
  (U,[k]) 
  :   
  \{
    \Omega^\bullet_{si}(U \times \Delta^k)
    \leftarrow
    W(b^{n-1} \mathbb{R})
  \}
  \mapsto 
  \{
    \Omega^\bullet_{si}(U \times \Delta^k)
    \leftarrow
    W(b^{n-1} \mathbb{R})
    \leftarrow
    CE(b^{n} \mathbb{R})
  \}
  \,.
$$

Here the simplicial presheaf on the left is that which assigns the set of arbitrary $n$-forms (with sitting instants but not necessarily closed) on $U \times \Delta^k$ and the map is simply given by sending such an $n$-form $A$ to the $(n+1)$-form $d_{dR} A$.

It is evident that the simplicial presheaf on the left resolves the point: since there is no condition on the forms every form on $U \times \Delta^k$ is in the image of the map of the [[Moore complex|normalized chain complex]] of a form on $U \times \Delta^{k+1}$: such is given by any form that is, up to a sign, equal to the given form on one $n$-face and 0 on all the other faces. Clearly such forms exist.

Moreover, this morphism is a fibration in $[CartSp_{smooth}^{op}, sSet]_{proj}$, for instanxce because its image under the [[Moore complex|normalized chains complex]] functor is a degreewise surjection, by the [[Poincare lemma]].

Now we observe that we have over each $(U,[k])$ a double pullback diagram in [[Set]]

$$
  \array{
    \left\{
      \array{
        \Omega^\bullet_{si, vert}(U \times \Delta^k)
        &\stackrel{A_{vert}}{\leftarrow}&
        CE(b^{n-1}\mathbb{R})
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet_{si}(U \times \Delta^k)
        &\stackrel{A}{\leftarrow}&
        W(b^{n-1}\mathbb{R})
      }
    \right\}
    &\to&
    \left\{
      \array{
        \Omega^\bullet_{si, vert}(U \times \Delta^k)
        &\stackrel{}{\leftarrow}&
        W(b^{n-1}\mathbb{R})
        \\
        \uparrow && \uparrow^{\mathrlap{id}}
        \\
        \Omega^\bullet_{si}(U \times \Delta^k)
        &\stackrel{}{\leftarrow}&
        W(b^{n-1} \mathbb{R})
      }
    \right\}
    \\
    \downarrow && \downarrow
    \\
    \left\{
      \array{
        \Omega^\bullet_{si, vert}(U \times \Delta^k)
        &\stackrel{}{\leftarrow}&
        0
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet_{si}(U \times \Delta^k)
        &\stackrel{}{\leftarrow}&
        CE(b^{n} \mathbb{R})
      }
    \right\}
    &\to&
    \left\{
      \array{
        \Omega^\bullet_{si,vert}(U \times \Delta^k)
        &\leftarrow&
        CE(b^{n} \mathbb{R})
        \\
        \uparrow && \uparrow^{\mathrlap{id}}
        \\
        \Omega^\bullet_{si}(U \times \Delta^k)
        &\stackrel{}{\leftarrow}&
        CE(b^{n} \mathbb{R})      
      }
    \right\}
    \\
    \downarrow && \downarrow
    \\
    \left\{
      \array{
        \Omega^\bullet_{si,vert}(U \times \Delta^k)
        &\leftarrow& 0
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet_{si}(U \times \Delta^k)
        &\stackrel{}{\leftarrow}&
        0
      }
    \right\}    
     &\to&
    \left\{
      \array{
        \Omega^\bullet_{si,vert}(U \times \Delta^k)
        &\leftarrow& CE(b^{n} \mathbb{R})
        \\
        \uparrow && \uparrow
        \\
        \Omega^\bullet_{si}(U \times \Delta^k)
        &\stackrel{}{\leftarrow}&
        0
      }
    \right\}    
  }
  \,,
$$

hence a coresponding pullback diagram of simplicial presheaves, that we claim 
is a presentation for the defining double [[(∞,1)-pullback]] 

$$
  \array{
    \mathbf{B}^n \mathbb{R} &\to& *
    \\
    {}^{\mathllap{curv}}\downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}
    &\to&
    \mathbf{\flat} \mathbf{B}^{n+1}
    \\
    \downarrow && \downarrow
    \\
    * &\to&  \mathbf{B}^{n+1} \mathbb{R}
  }
$$

for $curv$.

The bottom square is the one we already discussed for the de Rham coefficients. Since the top right vertical morphism is a fibration, also the top square is a [[homotopy pullback]] and hence exhibits the defining 
$(\infty,1)$-pullback for curv.

=--



+-- {: .num_prop }
###### Corollary

The degreewise map

$$
  (-1)^{\bullet+1}
  \int_{\Delta^\bullet} :
  \mathbf{B}^n \mathbb{R}_{diff,smp}
  \to  
  \mathbf{B}^n \mathbb{R}_{diff,chn}
$$

that sends an $n$-form $A \in \Omega^n(U \times \Delta^k)$ and its [[curvature]] $d A$ to $(-1)^{k+1}$ times  its [[fiber integration]] $(\int_{\Delta^k} A, \int_{\Delta^k} d A)$ is a weak equivalence in 
$[CartSp_{smooth}^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

Since under [[homotopy pullback]]s a weak equivalence of diagrams is sent to a weak equivalence. See the analagous argument 
[above](#FiberIntegrationAsWeakEquivalenceForDeRhamCoefficientPresentations).

=--

#### The canonical form on a simplicial Lie group
 {#CanonicalFormOnSimplicialLieGroup}

Above we discussed the canonical differential form on smooth $\infty$-groups $G$ for the special cases where [a)](#CanonicalFormOnLieGroup) $G$ is a [[Lie group]] and [b)](#CurvatureCharacteristicOnCircleNGroup) where $G$ is a [[circle Lie n-group]]. These are both in turn special cases of the situation where $G$ is a 
[[Lie group|Lie]] [[simplicial group]]. This we discuss now.

+-- {: .num_prop }
###### Proposition

For $G$ a [[Lie group|Lie]] [[simplicial group]], 
the [flat de Rham coefficient object](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#deRhamCohomology) 
$\mathbf{\flat}_{dR}\mathbf{B}G$ is presented by 
the simplicial presheaf which in degree $k$ is given by
$\Omega^1_{flat}(-, \mathfrak{g}_k)$, where $\mathfrak{g}_k = Lie(G_k)$ is the [[Lie algebra]] of $G_k$.

=--

+-- {: .proof}
###### Proof

Let 

$$
  \Omega^1_{flat}(-,\mathfrak{g}_\bullet)
  //G_\bullet
  =
  \left(
  \Omega^1_{flat}(-,\mathfrak{g}_\bullet) 
    \times
  C^\infty(-,G_\bullet) 
   \stackrel{\to}{\to} 
  \Omega^1_{flat}(-,\mathfrak{g}_\bullet)
  \right)
$$

be the [[presheaf]] of [[simplicial groupoids]] which in degree $k$ is the [[groupoid of Lie-algebra valued forms]] with values in $G_k$ from [above](#CanonicalFormOnLieGroup). As in the [above](#CanonicalFormOnLieGroup) discussion there we have that under the degreewise [[nerve]] this is a degreewise fibrant [[resolution]] of presheaves of [[bisimplicial set]]s

$$
  N \left(  \Omega^1_{flat}(-,\mathfrak{g}_\bullet)
    //
    G_\bullet
  \right)
   \to
  N *//G_\bullet
  =
  N B (G_{disc})_\bullet
$$

of the standard presentation of the delooping of the [[discrete group]] underlying $G$. By the discussion at [[bisimplicial set]] we know that under taking the [[diagonal]] 

$$
  diag : sSet^\Delta \to sSet
$$

the object on the right is a presentation for $\mathbf{\flat}_{dR} \mathbf{B}G$, because

$$
  diag N B (G_{disc})_\bullet
   \stackrel{\simeq}{\to}
  \bar W (G_{disc})
  \simeq
  \mathbf{\flat}\mathbf{B}G
  \,.
$$

Now observe that the morphism

$$
  diag (N  \Omega^1_{flat}(-,\mathfrak{g}_\bullet)
    //
    G_\bullet
  )
   \to
  diag N *// G_{disc}
$$

is a global fibration. This is in fact true for every
morphism of the form

$$
  diag N (S_\bullet//G_\bullet) \to diag *//G_\bullet
$$

for $S_\bullet//G_\bullet \to *//G_\bullet$ a simlicial [[action groupoid]] projection with $G$ a simplicial group acting on a 
[[Kan complex]] $S$: we have that 

$$
  (diag N (S//G))_k 
   = 
  S_k \times (G_k)^{\times_k}
  \,.
$$

On the second factor the horn filling condition is simply that of the identity map $diag N B G \to diag N B G$ which is evidently solvable, whereas on the first factor it amounts to $S \to *$ being a Kan fibration, hence to $S$ being Kan fibrant.

But the simplicial presheaf 
$\Omega^1_{flat}(-,\mathfrak{g}_\bullet)$ is indeed Kan fibrant: for a given $U \in CartSp$ we may use [[parallel transport]] to (non-canonically) identify

$$
  \Omega^1_{flat}(U, \mathfrak{g}_k)
   \simeq
  SmoothMfd_*(U, G_k)
  \,,  
$$

where on the right we have [[smooth function]]s that send the origin of $U$ to the neutral element. But since $G_\bullet$ is Kan fibrant and has smooth global fillers (by the discussion at [[simplicial group]] one can give algebraic formulas for the fillers, which translate into smooth manps) als $SmoothMfd_*(U,G_\bullet)$ is Kan fibrant.

In summary this means that the defining [[homotopy pullback]] 

$$\mathbf{\flat}_{dR} \mathbf{B}G
  :=
  \mathbf{\flat} \mathbf{B}G \times_{\mathbf{B}G} *
$$

is presented by the ordinary [[pullback]] of [[simplicial presheaves]]

$$
  diag N \Omega^1_{flat}(-,\mathfrak{g}_\bullet)
   \times
  diag N B G_\bullet *
  =
  \Omega^1(-, \mathfrak{g}_\bullet)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

For $G$ a simplicial Lie group the 
[canonical differential form](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#CurvatureCharacteristics)

$$
  \theta : G \to \mathbf{\flat}_{dR} \mathbf{B}G
$$

is presented in terms of the above presentation for
$\mathbf{\flat}_{dR} \mathbf{B}G$ by the morphisms of simplicial presheaves

$$
  \theta_k 
   : 
  G_k
  \to 
  \Omega^1_{flat}(-, \mathfrak{g}_k)
$$

which is the presheaf-incarnation of the Maurer-Cartan form of the ordinary Lie group $G_k$.

=--

+-- {: .proof}
###### Proof

Continuing with the strategy of the previous proof
we find a resolution of $* \to \mathbf{\flat} \mathbf{B}G$ by applying the construction of  _[The canonical form on a Lie group](#CanonicalFormOnLieGroup)_ degreewise and then applying $diag N$.

The defining homotopy pullback

$$
  \array{
     G &\stackrel{}{\to}& *
     \\
     \downarrow && \downarrow
     \\
     \mathbf{\flat}_{dR}
    &\to&
    \mathbf{\flat} \mathbf{B}G
  }
$$

for $\theta$ is this way presented by the ordinary pullback

$$
  \array{
     G_\bullet &\stackrel{}{\to}&
     diag N \left( \Omega^1_{flat}(-, \mathfrak{g}_\bullet))_{triv} // G_\bullet \right)
     \\
     \downarrow && \downarrow
     \\
     \Omega^1_{flat}(-, \mathfrak{g}_\bullet)
     &\to &
     diag N (\Omega^1_{flat}(-,\mathfrak{g}_\bullet)//G_\bullet)
  }
$$

of simplicial presheaves, where $\Omega^1_{flat}(-,\mathfrak{g}_\k)$ is the set of flat $\mathfrak{g}$-valued forms $A$ equipped with a gauge transformation $0 \stackrel{g}{\to} A$. As in the above proof one finds that the right vertical morphism is a fibration, hence indeed a [[resolution]] of the point inclusion. The pullback is degreewise that from the case of ordinary Lie groups and thus the result follows.

=--


We can now give a simplicial description of the canonical curvature form $\theta : \mathbf{B}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} U(1)$ that [above](#CurvatureCharacteristicOnCircleNGroup) we obtained by a chain complex model:



+-- {: .num_example }
###### Example

The canonical form on the [[circle Lie n-group]]

$$
  \theta : \mathbf{B}^{n-1}U(1)
  \to 
  \mathbf{\flat}_{dR} \mathbf{B}^n U(1)
$$

is presented by the simplicial map 

$$
  \Xi( U(1)[n-1] )
  \to 
  \Xi( \Omega^1_{cl}(-)[n-1] )
$$

which is simply the Maurer-Cartan form on $U(1)$ in degree $n$.

The equivalence to the model we obtained before is given by noticing the equivalence in [[hypercohomology]] of chain complexes of abelian sheaves

$$
  \Omega^1_{cl}(-)[n]
   \simeq
  (\Omega^1(-) \stackrel{d_{dR}}{\to}
   \cdots
   \stackrel{d_{dR}}{\to}
   \Omega^n_{cl}(-)
  ) 
$$ 

on [[CartSp]].

=--

### Flat Ehresmann connections
 {#FlatEhresmannConnections}

We discuss the realization of the general abstract concept
of [flat Ehresmann infinity-connections](cohesive+%28infinity%2C1%29-topos+--+structures#FlatEhresmannConnections) realized in $Smooth\infty Grpd$. We show that when applied to an ordinary [[Lie group]] this reproduces the traditional notion of [[Ehresmann connection]].

(...)


### Differential cohomology 
  {#StrucDifferentialCohomology}

We discuss the 
<a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#DifferentialCohomology">intrinsic differential cohomology</a> in $Smooth \infty Grpd$

We first expose the simple special case of ordinary
$U(1)$-[[principal bundle]]s with [[connection on a bundle|connection]]
in more detail. Then we turn to the general case.

#### Circle 0- and circle 1-bundle with connection

##### Circle bundles with connection {#CircleBundlesConnection}

Before discussing [the full theorem](#DeligneCohomologyTheorem), it is instructive to start by looking at the special case $n=1$ in some detail, which is about ordinary  $U(1)$-[[nLab:principal bundle]]s [[nLab:connection on a bundle|with connection]]. 

This contains in it already all the relevant structure of the general case, but the low categorical degree is more transparently written out and will allow us to pause to highlight some maybe noteworthy aspects of the situation, such as the phenomenon of _pseudo-connections_ [below](#CircleBunlePseudoConnection).

In terms of the [Dold-Kan correspondence](#DoldKan) the object $\mathbf{B}U(1) \in \mathbf{H}$ is modeled in $[CartSp^{op}, sSet]$ by

$$
  \mathbf{B}U(1)
  =
  \Xi(\;
    C^\infty(-,U(1)) \to 0    
  \;)
  \,.
$$

Accordingly we have for the double [[nLab:delooping]] the model

$$
  \mathbf{B}^2 U(1)
  =
  \Xi(
    \;
    C^\infty(-,U(1)) \to 0  \to 0    
  \;)
$$

and for the [[nLab:universal principal ∞-bundle|universal principal 2-bundle]]

$$
  \mathbf{E}\mathbf{B}U(1)
  =
  \Xi(
    \;
    C^\infty(-,U(1)) \stackrel{Id}{\to} C^\infty(-, U(1)) \to 0    
    \;
  )
  \,.
$$

In this notation we have also the constant presheaf

$$
  \mathbf{\flat} \mathbf{B}^2 U(1)
  = 
  \Xi(
    \;
     const U(1) \to 0 \to 0
    \;
  )  
  \,.
$$

Above we already found the model 

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  = 
  \Xi(0 \to \Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-))
  \,.
$$

In order to compute the differential cohomology 
$\mathbf{H}_{diff}(-,\mathbf{B}U(1))$ by an ordinary
pullback in [[nLab:sSet]] we also want to resolve the curvature characteristic morphism $\mathbf{B}U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)$ by a fibration. We claim that this may be obtained by choosing the resolution 
$\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B} U(1)_{diff,chn}$ given by

$$
  \mathbf{B}U(1)_{diff} 
  :=
  \Xi(
    \;
    C^\infty(-,U(1))
    \oplus
    \Omega^1(-)
    \stackrel{d_{dR} \oplus Id}{\to}
    \Omega^1(-)
    \;
  )
$$

with the morphism $curv : \mathbf{B}_{diff}U(1) \to \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)$ given by

$$
  \array{
    C^\infty(-,U(1)) 
    \oplus
    \Omega^1(-)
    &\stackrel{d_{dR} + Id}{\to}&
    \Omega^1(-)
    \\
    \downarrow^{\mathrlap{p_2}} && \downarrow^{\mathrlap{d_{dR}}}
    \\
    \Omega^1(-) &\stackrel{d_{dR}}{\to}&
    \Omega^2_{cl}(-)
  }
  \,.
$$

By the [[nLab:Poincare lemma]] applied to each [[nLab:Cartesian space]], this is indeed a fibration.

In the [next section](#AbGerbesConnection) we give the proof of this (simple) claim. Here in the warmup phase we instead want to discuss the geometric interpretation of this resolution, along the lines of the section <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+survey#CurvatureCharacteristicsI">curvature characteristics of 1-bundles</a> in the [[schreiber:differential cohomology in an (∞,1)-topos -- survey|survey-part]].


+-- {: .num_prop }
###### Proposition

We have the following geometric interpretation of the above models:

$$
  \mathbf{\flat}_{dR} \mathbf{B}^2 U(1)
  : 
  U \mapsto 
  \left\{
    \array{
      U &\to& *
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1)
    }
  \right\}
  =
  \left\{
    \mathbf{\Pi}_2(U) \to \mathbf{B}^2 U(1)
  \right\}
$$

and

$$
  \mathbf{B}U(1)_{diff}
  : 
  U \mapsto 
  \left\{
    \array{
      U &\to& \mathbf{B}U(1)
      \\
      \downarrow && \downarrow
      \\
      \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U(1))
    }
  \right\}
  \,.
$$

And in this presentation the morphism $curv : \mathbf{B}_{diff}U(1) \to \mathbf{B}^2 U(1)$ is given over $U \in CartSp$ by forming the pasting composite

$$
  \array{
    U &\to& \mathbf{B}U(1) &&& underlying\;cocycle
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}INN(U(1)) &&& connection
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}_2(U) &\to& \mathbf{B}^2 U(1) &&& curvature
  }
$$

and picking the lowest horizontal morphism.

=--

Here the terms mean the following:

* $INN(U(1))$ is the [[nLab:2-group]] $\Xi(U(1) \to U(1))$, which is a 
  [[nLab:groupal model for universal principal ∞-bundles|groupal model for the universal U(1)-principal bundle]] $\mathbf{E}U(1)$;

* $\mathbf{\Pi}_2(U)$ is the [[nLab:path 2-groupoid]] with homotopy class of 2-dimensional paths as 2-morphisms

* the groupoids of diagrams in braces have as objects commuting diagrams in $[CartSp^{op}, sSet]$ as indicated, and horizontal 2-morphisms fitting into such diagrams as morphisms.

Using the discussion at [[nLab:2-groupoid of Lie 2-algebra valued forms]] (<a href="http://arxiv.org/abs/0802.0663">SchrWalII</a>) we have the following:


1. For $X$ a [[nLab:smooth manifold]], morphisms in $[CartSp^{op}, 2Grpd]$ of the form $tra_A : \Pi_2(X) \to \mathbf{E}\mathbf{B}U(1)$ are in bijection with smooth 1-forms $A \in \Omega^1(X)$: the 2-functor sends a path in $X$ to the the [[nLab:parallel transport]] of $A$ along that path, and sends a surface in $X$ to the exponentiated integral of the curvature 2-form $F_A = d A$ over that surface. The [[nLab:Bianchi identity]] $d F_A = 0$ says precisely that this assignment indeed descends to homotopy classes of surfaces, which are the 2-morphisms in $\Pi_2(X)$.

1. Moreover [[nLab:k-morphism|2-morphisms]] of the form $(\lambda,\alpha) : tra_A \to \tra_{A'}$ in $[CartSp^{op}, 2Grpd]$ are in bijection with pairs consisting of a $\lambda \in C^\infty(X,U(1))$ and a 1-form $\alpha \in \Omega^1(X)$ such that $A' = A + d_{dR} \lambda - \alpha$. 

1. And finally [[nLab:k-morphism|3-morphisms]] $h : (\lambda, \alpha) \to (\lambda', \alpha')$ are in bijection with $h \in C^\infty(X,U(1))$ such that $\lambda' = \lambda \cdot h$ and $\alpha' = \alpha + d_{dR} h$.


By the same reasoning we find that the coefficient object for flat $\mathbf{B}^2 U(1)$-valued differential cohomology is

$$
  \mathbf{\flat}\mathbf{B}^2 U(1)
  =
  [\Pi_2(-), \mathbf{B}^2U(1)]
  =
  \Xi(
    C^\infty(-,U(1))
    \stackrel{d_{dR}}{\to}
    \Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-)
  )
  \,.
$$


So by the above definition of differential cohomology in $\mathbf{H}$ we find that $\mathbf{B}U(1)$-differential cohomology of a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] $X$ is given by choosing any [[nLab:good open cover]] $\{U_i \to X\}$, taking $C(\{U_i\})$ to be the [[nLab:Cech nerve]], which is then a cofibrant replacement of $X$ in $[CartSp^{op}, sSet]_{proj,cov}$ and forming the ordinary pullback

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}U(1)) &\to& H^2_{dR}(X)
    \\
    \downarrow && \downarrow
    \\
    [CartSp^{op},sSet](C(\{U_i\}), \mathbf{B}_{diff}U(1))
    &\stackrel{curv}{\to}&
    [CartSp^{op},sSet](C(\{U_i\}), \flat_{dR}\mathbf{B}^2 U(1))
  }
$$

(because the bottom vertical morphism is a fibration, by the fact that our model for $\mathbf{B}_{diff} U(1) \to \flat_{dR}\mathbf{B}^2 U(1)$ is a fibration, that $C(\{U_i\})$ is cofibrant and using the axioms of the [[nLab:sSet]]-[[nLab:enriched model category]] $[CartSp^{op}, sSet]_{proj}$).

+-- {: .num_prop}
###### Observations

A cocycle in $[CartSp^{op},sSet](C(\{U_i\}), \mathbf{B}_{diff}U(1))$ is

1. a collection of functions

   $$
     (g_{i j } \in C^\infty(U_i \cap U_j, U(1)))
    $$

    satsifying $g_{i j} g_{j k} = g_{i k}$ on $U_i \cap U_j \cap U_k$;
  
1. a collection of 1-forms

   $$
      (A_i \in \Omega^1(U_i))
   $$
  
1. a collection of 1-forms


    $$
      (a_{i j} \in \Omega^(U_i \cap U_j))
    $$

    such that

    $$
      A_j = A_i + d_{dR} g_{i j} + a_{i j}
    $$

    on $U_i \cap U_j$ and

    $$
      a_{i j} + a_{j k} = a_{i k}
    $$

    on $U_i \cap U_j \cap U_k$.

The curvature-morphism takes such a cocycle to the cocycle

$$
  (d A_i, a_{i j}, )
$$

in the [above model](#OrdinaryDeRham) $[CartSp^{op},sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^2 U(1))$ for intrinsic de Rham cohomology.


Every cocycle with nonvanishing $(a_{i j})$ is in $[C(\{U_i\}), \mathbf{B}_{diff}U(1)]$ coboundant to one with vanishing $(a_{i j})$ 
   
=--

+-- {: .proof}
###### Proof

The first statements are effectively the definition and the construction of the above models. The last statement is as in the [above discussion](#OrdinaryDeRham) of our model for ordinary de Rham cohomology: given a cocycle with non-vanishing closed $a_{i j}$, pick a partition of unity $(\rho_i \in C^\infty(X))$ subordinate to the chosen cover and the coboundary given by $(\sum_{i_0} \rho_{i_0} a_{i_0 i})$. This connects $(A_i,a_{i j}, g_{i j})$ with the cocycle $(A'_i, a'_{i j}, g_{i j})$ where

$$
  A'_i = A_i + \sum_{i_0} \rho_{i_0} a_{i_0 i}
$$

and

$$
  \begin{aligned}
    a'_{i j} 
      & = A'_j - A'_i - d g_{i j} 
     \\ 
      & = a_{i j} + 
      - \sum_{i_0}( a_{i_0 i} - a_{i_0 j} )
    \\
    & = 0    
  \end{aligned}
  \,.
$$

=--

So in total we have found the following story:

1. In order to compute the curvature characteristic form of a [[nLab:Cech cohomology]] cocycle $g : C(\{U_i\}) \to \mathbf{B}U(1)$ of a $U(1)$-principal bundle, we first lift it 

   $$
     \array{
       && \mathbf{B}_{diff}U(1)
       \\
       & {}^{\mathllap{(g,\nabla)}}\nearrow & \downarrow
       \\
       C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
     }
   $$

   to an equivalent $\mathbf{B}_{diff}U(1)$-cocycle, and this amounts to putting (the Cech-representatitve of) a _pseudo-connection_ on the $U(1)$-principal bundle.

1. From that lift the desired curvature characteristic is simply projected out

   $$
     \array{
       && \mathbf{B}_{diff}U(1) &\stackrel{curv}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^2 U(1)
       \\
       & {}^{\mathllap{(g,\nabla)}}\nearrow & \downarrow
       \\
       C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
     }
     \,,
   $$

   and we find that it lives in the sheaf [[nLab:hypercohomology]] that models ordinary de Rham cohomology.

1. Therefore we find that in each _cohomology class_ of curvatures, there is at least one representative which is an ordinary globally defined 2-form. Moreover, the pseudo-connections that map to such a representative are precisely the _genuine_ connections, those for which the $(a_{i j})$-part of the cocycle vaishes.

So we see that ordinary connections on ordinary circle bundles are a means to model the homotopy pullback

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}U(1)) &\to& H_{dR}^2(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}U(1)) &\to& \mathbf{H}_{dR}(X,\mathbf{B}U(1)) 
  }
$$

in a 2-step process: first the choice of a pseudo-connection realizes the bottom horizontal morphism as an [[nLab:anafunctor]], and then second the restriction imposed by forming the ordinary pullback chooses from all pseudo-connections precisely the genuine connections.

The general version of this story is discussed in detail at <a href="#Connections">differential cohomology in an (∞,1)-topos -- Local (pseudo-)connections.</a>


##### Circle bundles with pseudo-connection {#CircleBunlePseudoConnection}

In the above discussion of extracting ordinary connections on ordinary $U(1)$-principal bundles from the abstract topos-theoretic definition of differential cohomology, we argued that a certain homotopy pullback may be computed by choosing in the Cech-hypercohomology of the complex of sheaves $(\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2_{cl}(-))$ over a manifold $X$ those cohomology representatives that happen to be represented by globally defined 2-forms on $X$. We saw that the homotopy fiber of _pseudo-connections_ over these 2-forms happened to have connected components indexed by _genuine_ connections.

But by the general abstract theory, up to isomorphism the differential cohomology computed this way is guaranteed to be independent of all such choices, which only help us to compute things.

To get a feeling for what is going on, it may therefore be useful to re-tell the analgous story with pseudo-connections that are not genuine connections.

By the very fact that $\mathbf{B}U(1) \stackrel{\simeq}{\leftarrow} \mathbf{B}_{diff}U(1)$ is a weak equivalence, it follows that every pseudo-connection is equivalent to an ordinary connection as cocoycles in $[CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}_{diff}(G))$. 

If we choose a [[nLab:partition of unity]] $(\rho_i \in C^\infty(X,\mathbb{R}))$ subordinate to the cover $\{U_i \to X\}$, then we can construct the corresponding coboundary explicitly:

let $(A_i g_{ij}, a_{i j})$ be an arbitrary pseudo-connection cocycle. Consider the Cech-hypercohomology coboundary given by $(\sum_{i_0} \rho_{i_0} a_{i_0 i}, 0)$. This lands in the shifted cocycle

$$
  (A'_i := A_i + \sum_{i_0} \rho_{i_0} a_{i_0 i}, g_{i j}, a'_{i j})
  \,,
$$

and we can find the new pseudo-components $a'_{i j}$ by 

$$
  a'_{i j} = A'_j - A'_i - d_{dR} g_{i j}
  \,.
$$

Using the computation 

$$
  \begin{aligned}
    \sum_{i_0} \rho_{i_0} (a_{i_0 i} - a_{i_0 j}
    &=
    - \sum_{i_0} \rho_{i_0} (a_{i i_0} + a_{i_0 j}
    \\
    & = \sum_{i_0} \rho_{i_0} a_{i j}
    \\
    & = a_{i j}
  \end{aligned}
$$

we find that these indeed vanish.

The most drastic example for this is a lift $\nabla$ of a cocycle $g = (g_{i j})$ in 

$$
  \array{
    && \mathbf{B}_{diff} U(1)
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow
    \\
    C(\{U_i\}) &\stackrel{g}{\to}& \mathbf{B}U(1)
  }
$$

is one which takes all the ordinary curvature forms to vanish identically

$$
  \nabla = (A_i := 0, g_{i j}, a_{i j})
  \,.
$$

This fixes the pseudo-components to be $a_{i j} = - d g_{i j}$. By the above discussion, this pseudo-connection with vanishing connection 1-forms is equivalent, as a pseudo-connection, to the ordinary connection cocycle with connection forms $(A_i := \sum_{i_0} \rho_{i_0} d g_{i_0 i})$. This is a <a href="http://ncatlab.org/nlab/show/connection+on+a+bundle#Properties">standard formula</a> for equipping $U(1)$-principal bundles with Cech cocycle $(g_{i j})$ with a connection.


##### Circle 0-bundle {#U1GroupoidBundle}

We saw above that the intrinsic coefficient object $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ yields ordinary de Rham cohomology in degree $n \gt 1$. For $n = 1$ we [have](#FlatCircleCohomology) that $\mathbf{\flat}_{dR} \mathbf{B}U(1)$ is given simply by the 0-[[nLab:truncated]] sheaf of 1-forms, $\Omega^1(-) : CartSp^{op} \to Set \hookrightarrow sSet$. Accordingly we have for $X$ a paracompact smooth manifold

$$
  \mathbf{H}(X, \mathbf{\flat}_{dR}\mathbf{B}U(1)) = 
  \Omega^1_{cl}(X)
$$ 

instead of $H^1_{dR}(X)$.

There is a good reason for this discrepancy: for $n \geq 1$ the object $\mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is the recipient of the intrinsic curvature characteristic morphism

$$
  curv_{\mathbf{B}^{n-1} U(1)} : \mathbf{B}^{n-1} U(1) \to 
   \mathbf{\flat}_{dR} \mathbf{B}^n U(1)
  \,.
$$

For $X \to \mathbf{B}^{n-1} U(1)$ a [[nLab:cocycle]] (an $(n-2)$-gerbe without connection), the cohomology class of the composite $X \to \mathbf{B}^{n-1} U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^n U(1)$ is precisely the obstruction to the existence of a flat extension $X \to \mathbf{\flat} \mathbf{B}^{n-1} U(1) \to \mathbf{B}^{n-1} U(1)$ for the original cocycle.

For $n = 2$ this is the usual [[nLab:curvature]] 2-form of a [[nLab:line bundle]], for $n = 3$ it is curvature 3-form of a [[nLab:bundle gerbe]], etc. But for $n = 1$ we have that the original cocycle is just a map of spaces

$$
  f : X \to U(1)
  \,.
$$

This can be understoody as a cocycle for a _groupoid_ principal bundle, for the 0-truncated groupoid with $U(1)$ as its space of objects. Such a cocycle extends to a flat cocycle precisely if $f$ is _constant_ as a function. The corresponding **curvature 1-form** is $d_{dR} f$ and this is precisely the obstruction to constancy of $f$ already, in that $f$ is constant if and only if $d_{dR} f$ vanishes. _Not_ (necessarily) if it vanishes _in de Rham cohomology_ . 

This is the simplest example of a general statement about curvatures of higher bundles: the curvature 1-form is not subject to gauge transformations.








#### Circle $n$-bundles with connection {#ProofOfDeligneTheorem}


Recall the definition of the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#DifferentialCohomology">intrinsic differential cohomology</a> on $X \in Smooth \infty Grpd$ with coefficients in $U(1)$ as the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}^n U(1)) &\to & H_{dR}(X,\mathbf{B}^{n+1} U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} U(1))
  }
$$

in [[∞Grpd]], where the morphism on the right picks one base point in each connected component.

+-- {: .num_theorem #DeligneCohomologyTheorem}
###### Theorem

For $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ 
a [[paracompact space|paracompact]] [[smooth manifold]] we have

$$
  H_{diff}(X,\mathbf{B}^n U(1))
  \simeq
  \left( 
     \;\; H(X,\mathbb{Z}(n+1)_D^\infty) \;\;
  \right)
  \times_{\Omega_{cl}^{n+1}(X)} H_{dR}^{n+1}_{int}(X)
  \,.
$$

Here on the right we have the subset of Deligne cocycles that picks for each integral de Rham cohomology class of $X$ only one curvature form representative.

=--

If we make use of the explicit presentation of $Smooth \infty Grpd$ by the [[model structure on simplicial presheaves]] $[CartSp^{op}, sSet]_{proj,loc}$ and the explicit presentation 
$\mathbf{\flat}_{\mathrm{dR}} \mathbf{B}^{n+1}U(1)_{chn}$
for $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ by ordinary [[differential form]]s, as 
[above](#StrucDeRham) we may replace the right morphism in this pullback by $\Omega^{n+1}_{cl}(X) \to \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}U(1))$ and consider the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}'_{diff}(X,\mathbf{B}^n U(1)) &\to & 
   \Omega^{n+1}_{cl}(X)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n U(1))
    &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} U(1))
  }
$$


+-- {: num_theorem }
###### Theorem

For $X \in SmoothMfd \hookrightarrow Smooth \infty Grpd$ 
a [[paracompact space|paracompact]] [[smooth manifold]] we have that

$$
  H'_{diff}(X,\mathbf{B}^n U(1))
  \simeq
     \;\; H(X,\mathbb{Z}(n+1)_D^\infty) \;\;
$$

is the ordinary [[Deligne cohomology]] of $X$ in degree $n+1$.

=--


+-- {: .proof}
###### Proof 

Choose a [differentiably good open cover](#DifferentiablyGoodOpenCover) 
$\{U_i \to X\}$ and let $C(\{U_i\}) \to X$  in $[CartSp^{op}, sSet]_{proj}$ be the corresponding [[Cech nerve]] projection, a cofibrant resolution of $X$.
 
Since the [above model](#CurvatureCharOnBnU1) 
$curv_{chn} : \mathbf{B}_{diff}^n U(1)_{chn} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)_{chn}$
for the intrinsic $curv : \mathbf{B}_{diff}^n U(1) \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)$ is a fibration and $C(\{U_i\})$ is cofibrant, also 

$$
  [Cartp^{op}, sSet](C(\{U_i\}), \mathbf{B}^n_{diff}U(1)_{chn})
  \to
  [Cartp^{op}, sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^n U(1)_{chn})
$$

is a [[Kan fibration]] by the fact that $[CartSp^{op}, sSet]_{proj}$ is an [[simplicial model category]]. Therefore the [[homotopy pullback]] is computed as an ordinary [[pullback]].  

By the [above discussion of de Rham cohomology](#OrdinaryDeRham) we have that we can assume the morphism $H_{dR}^{n+1}(X) \to [CartSp^{op}, sSet](C(\{U_i\}), \mathbf{\flat}_{dR}\mathbf{B}^{n+1}_{chn})$ picks only cocycles represented by globally defined closed differential forms $F \in \Omega^{n+1}_{cl}(X)$.

By the nature of the chain complexes 
$curv_{chn} : \mathbf{B}_{diff}^n U(1)_{chn} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}U(1)_{chn}$, we see that the elements in the fiber over such a globally defined $(n+1)$-form $F$ are precisely the cocycles with values only in the "upper row complex" of 
$\mathbf{B}_{diff}^{n}U(1)_{chn}$

$$
  C^\infty(-,U(1)) \stackrel{d_{dR}}{\to} \Omega^1(-)
  \stackrel{d_{dR}}{\to}
  \cdots 
  \stackrel{d_{dR}}{\to}
  \Omega^n(-)
$$

such that $F$ is the differential of the last term.

This is the complex of sheaves that defines [[Deligne cohomology]] in degree $(n+1)$.

=--


#### Abstract properties
 {#DiffCohomologyAbstractProperties}

We discuss how the general abstract definition of differential cohomology in $Smooth \infty Grpd$ reproduces on general grounds the abstract properties of the traditional definition of [[ordinary differential cohomology]].

+-- {: .num_prop }
###### Proposition

For $X$ a [[smooth manifold]], the cohomology classes $H'_{diff}(X, \mathbf{B}^n U(1))$ of the cocycle $\infty$-groupoid $\mathbf{H}'_{diff}(X, \mathbf{B}^n U(1))$ defined by the [[homotopy pullback]]

$$
  \array{
    \mathbf{H}'_{diff}(X, \mathbf{B}^n U(1)_{ch}) &\to & \Omega^{n+1}_{cl}(X)   
     \\
     \downarrow && \downarrow
    \\ 
     \mathbf{H}(X, \mathbf{B}^n U(1))
     &\stackrel{curv}{\to}&
     \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^{n+1} U(1))
  }
$$

fit, with their canonical [[abelian group]] structure, into the two <a href="http://nlab.mathforge.org/nlab/show/ordinary+differential+cohomology#AbstractProperties">characteristic short exact sequences</a> of [[ordinary differential cohomology]]:

* $0 \to Omega^{n}(X)/\Omega^{n}_{cl}(X) \to H'_{diff}(X, \mathbf{B}^n U(1)) \to H^n(X, \mathbb{Z}) \to 0$.

* $0 \to H^{n-1}(X, U(1)) \to H'_{diff}(X, \mathbf{B}^n U(1)) \to \Omega^{n+1}_{cl, int}(X) \to 0$


=--

+-- {: .proof}
###### Proof

For the first sequence, the characteristic class exact sequence, use <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CharacteristicClassExactSequence">this general proposition</a> from the discussion at _[[cohesive (∞,1)-topos]]_ . This says that over the vanishing curvature form $0 \in \Omega_{cl}^{n+1}(X)$ we have the short exact sequence

$$
  0 \to \Omega_{cl}^n(X)/\Omega_{cl,int}^{n}(X)
  \to 
   H_{diff}^n(X, U(1))
  \to 
   H^{n+1}(X, \mathbb{Z})
  \to 0
  \,,
$$

where we used that $H_{smooth}(X, \mathbf{B}^n U(1)) \simeq H^{n+1}(X, \mathbb{Z})$ on the [[paracompact space]] $X$ and that $H_{dR}^n(X)/\Omega^n_{cl,int}(X) = \Omega^n_cl(X)/\Omega^n_{cl, int}(X)$ because exact forms are in particular closed integral forms (with periods $0 \in \mathbb{N}$). Looking at $H'_{diff}$ instead of $H_{diff}$, we get in the fibers one such contribution per closed $(n+1)$-form $\Lambda$ trivial in de Rham cohomology, hence per arbitrary $n$-form $\omega$ with $d \omega  = \Lambda$

$$
  0 \to \Prod_{\Lambda}\{\omega | d \omega = \Lambda \}/\Omega_{cl,int}^{n}(X)
  \to 
   H'_{diff}^n(X, U(1))
  \to 
   H^{n+1}(X, \mathbb{Z})
  \to 0
  \,.
$$

But this is the fiber sequence in question.

For the second sequence, the curvature exact sequence, <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureExactSequence">this general proposition</a> from the discussion at _[[cohesive (∞,1)-topos]]_ , which implies that we have a short exact sequence

$$
  0 \to H_{flat}^n(X, \mathbf{B}^n U(1))
  \to 
   H_{diff}^n(X, U(1))
  \to 
   \Omega_{cl,int}^{n+1}(X)
  \to 0
  \,.
$$

Then use prop. \ref{FlatCohomologyAndWithConstantCoefficients}, which says that $H_{flat}^n(X, \mathbf{B}^n U(1)) \simeq H^{n}(X, U(1)_{disc})$.


=--

#### Presentation by exponentiated $\infty$-Lie algebras  
 {#U1FromLieIntegration}

(...)

+-- {: .num_prop }
###### Proposition

The morphism given by [[fiber integration]] of differential forms over the simplex factor fits into a diagram

$$
  \array{
    \mathbf{B}^n U(1)_{diff,simp} &\stackrel{curv_{smp}}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{smp}
    \\
    \downarrow^{\mathrlap{\int}_{\Delta^\bullet}} && 
    \downarrow^{\mathrlap{\int}_{\Delta^\bullet}}
    \\
    \mathbf{B}^n U(1)_{diff,chn} &\stackrel{curv_{chn}}{\to}& \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}    
  }
  \,,
$$

where the vertical morphisms are weak equivalences. 

=--



+-- {: .num_prop }
###### Proposition

Fiber integration induces a weak equivalence

$$
  \int_{\Delta^\bullet} : 
  \mathbf{B}^n \mathbb{R}_{diff,simp}
  \stackrel{\simeq}{\to}
  \mathbf{B}^n \mathbb{R}_{diff, chn}
$$

=--

+-- {: .proof}
###### Proof

Observe that $\mathbf{B}^n \mathbb{R}_{diff,simp}$ is the [[pullback]] of $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}_{smp} \to \mathbf{\flat}\mathbf{B}^{n+1} \mathbb{R}_{smp}$ along the evident forgetful morphism from

$$
  (U,[k]) \mapsto \{\Omega^\bullet(U \times \Delta^k) \leftarrow
  W(b^{n-1} \mathbb{R})\}
  \,.
$$

This forgetful morphism is evidently a fibration (because it is a degreewise surjection under Dold-Kan), hence this pullback models the [[homotopy fiber]] of $\mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R} \to \mathbf{\flat} \mathbf{B}^{n+1} \mathbb{R}$. Since by the above fiber integration gives a weak equivalence of pulback diagrams the claim follows.


=--



+-- {: .num_defn }
###### Definition

Write $\mathbf{B}^n U(1)_{conn,simp} \hookrightarrow \mathbf{B}^n U(1)_{diff,simp}$ for the sub-presheaf which over $(U,[k])$ is the set of those forms $\omega$ on $U \times \Delta^k$ such that the [[curvature]] $d \omega$ has no leg along $\Delta^k$.

=--

+-- {: .num_cor }
###### Corollary

Under fiber integration over simplices, $\mathbf{B}^n U(1)_{conn,simp}$ is [[quasi-isomorphism|quasi-isomorphic]] to the [[Deligne cohomology]]-complex.


=--



$$
  \array{
     && 
     \mathbf{B}^n U(1)_{conn,simp}
     &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     U(1)(n)_D^\infty
     &&&
     connection
     \\
     & \nearrow & \downarrow && \downarrow
     \\
     \hat X &\to& 
     \mathbf{B}^n U(1)_{diff,simp}
     &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     \mathbf{B}^n U(1)_{diff,chn}
     &&&
     pseudo-connection
     \\
     & \searrow & \downarrow && \downarrow
     \\
     && \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{smp}
      &\stackrel{\int_{\Delta^\bullet}}{\to^\simeq}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1}U(1)_{chn}
     &&&
     curvature
  }
  \,.
$$

In summary this gives us the following alternative perspective on connections on $\mathbf{B}^{n-1}U(1)$-[[principal ∞-bundle]]s: such a connection is a cocycle with values in the $\mathbf{B}^n \mathbb{Z}$-quotient of the  $(n+1)$-coskeleton of the simplicial presheaf which over $(U,[k])$ is the set of diagrams of [[dg-algebra]]s

$$
  \array{
    C^\infty(U)\otimes \Omega^\bullet(\Delta^k) 
     &\leftarrow&
    CE(b^{n-1}\mathbb{R})
    &&&
    underlying\;cocycle
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U) \otimes \Omega^\bullet(\Delta^k) 
     &\leftarrow&
    W(b^{n-1}\mathbb{R})    
    &&& 
    connection
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)\otimes C^\infty(\Delta^k) &\leftarrow& CE(b^n \mathbb{R})
    &&&
    curvature
  }
$$

where the restriction to the top morphism is the underlying cocycle and the restriction to the bottom morphism the curvature form.

The generalization to such diagram cocycles from $b^{n-1}\mathbb{R}$ to general [[∞-Lie algebra]]s $\mathfrak{g}$ we discuss below in [∞-Lie algebra valued connections](#InfinityLieAlgebraConnection).



#### Over unoriented base objects

The [[higher parallel transport|higher holonomy]] of a circle $n$-bundle with connection is well defined only over [[oriented]] [[smooth manifold]]s. In the unorientable or even unoriented case, extra structure is needed to define it. 


See [[orientifold]] for more.


### Chern-Weil homomorphism and $\infty$-connections 
  {#StrucChernWeil}


We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#ChernWeilTheory">general abstract notion of Chern-Weil homomorphism and ∞-connections</a> realized in $Smooth \infty Grpd$.

Recall that for $A \in Smooth \infty Grpd$ a smooth $\infty$-groupoid regarded as a coefficient object for [[cohomology]], for instance the [[delooping]] $A = \mathbf{B}G$ of an [[∞-group]] $G$ we have abstractly that

* a [[characteristic class]] on $A$ with coefficients in the [circle Lie n-group](#CircleLienGroup) is represented by a morphism

  $$
    \mathbf{c} : A \to \mathbf{B}^n U(1)
    \,;
  $$

* the (unrefined) [[Chern-Weil homomorphism]] induced from this is the differential characteristic class given by the composite

  $$
    {\mathbf{c}_{dR}} : 
     A \stackrel{\mathbf{c}}{\to}
     \mathbf{B}^n U(1) \stackrel{curv}{\to}
     \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}
  $$

  with the [universal curvature characteristic](#StrucCurvatureForms) on $\mathbf{B}^n U(1)$, or rather: is the morphism on [[cohomology]]

  $$
    H^1_{Smooth}(X,G)
    :=
    \pi_0 Smooth\infty Grpd(X, \mathbf{B}G)
      \stackrel{\pi_0({(\mathbf{c}_{dR})_*})}{\to}
    \pi_0 Smooth\infty Grpd(X, \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R})
    \simeq
    H_{dR}^{n+1}(X)
  $$

  induced by this.

* the [[connection on an ∞-bundle|∞-connections]] with coefficients in $A$ are the [[cocycle]]s in the [[∞-groupoid]] $Smooth \infty Grpd(X,A)_{conn}$ that universally lifts these differential classs in de Rham cohomology to full [differential cohomology](#StrucDifferentialCohomology), in that it universally fills the diagrams

  $$
    \array{
      Smooth \infty Grpd(X,A)_{conn} 
    &\stackrel{\hat {\mathbf{c}}}{\to}& 
     Smooth\infty Grpd(X, \mathbf{B}^n U(1))_{diff}
      \\
      \downarrow && \downarrow
      \\
      Smooth \infty Grpd(X,A) 
      &\stackrel{{\mathbf{c}_{dR}}}{\to}&
      Smooth \infty Grpd(X,\mathbf{B}^{n+1}U(1))_{dR}
    }
    \,.
  $$

[Above](#CurvatureCharacteristicOnCircleNGroup) we have discussed a presentation of the 
universal curvature class $\mathbf{B}^n \mathbb{R} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}$ by a span

$$
  \array{
    \mathbf{B}^n \mathbb{R}_{diff,smp}
    &\stackrel{curv_{smp}}{\to}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1} \mathbb{R}_{smp}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^n \mathbb{R}_{smp}
  }
$$

in the [[model structure on simplicial presheaves]] $[CartSp_{smooth}^{op}, sSet]_{proj}$, given by maps of smooth families of [[differential form]]s.

We now insert this in the above general abstract definition of the $\infty$-Chern-Weil homomorphism to deduce a presentation of that in terms of smooth families of [[∞-Lie algebroid valued differential forms]].

The main step is the construction of a well-suited composite of two spans of morphisms of simplicial presheaves (of two [[∞-anafunctor]]s): we consider presentations of [[characteristic class]]es $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ in the image of the [∞-Lie integration](#LieIntegration) map and presented by trunactions and quotients of morphisms of simplicial presheaves of the form

$$
  \array{
    \exp(\mathfrak{g})
    \stackrel{\exp(\mu)}{\to}
    \exp(b^{n-1}\mathbb{R})
  }
  \,.
$$

Then, using the above, the composite differential characteristic class $\mathbf{c}_{dR}$ is presented by the zig-zag

$$
  \array{
    && \mathbf{B}^n \mathbb{R}_{diff,smp}
    &\stackrel{curv_{smp}}{\to}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1} \mathbb{R}_{smp}
    \\
    && \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{g})
    &\stackrel{\exp(\mu)}{\to}&
    \mathbf{B}^n \mathbb{R}_{smp}
  }
$$

of simplicial presheaves. In order to efficiently compute which morphism in $Smooth \infty Grpd$ this presents we need to construct
-- preferably naturally in the [[L-∞ algebra]] $\mathfrak{g}$ -- a simplicial presheaf $\exp(\mathfrak{g})_{diff}$ that fills this diagram as follows:

$$
  \array{
    \exp(\mathfrak{g})_{diff} &\stackrel{\exp(\mu,cs)}{\to}& \mathbf{B}^n \mathbb{R}_{diff,smp}
    &\stackrel{curv_{smp}}{\to}&
     \mathbf{\flat}_{dR}\mathbf{B}^{n+1} \mathbb{R}_{smp}
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{g})
    &\stackrel{\exp(\mu)}{\to}&
    \mathbf{B}^n \mathbb{R}_{smp}
  }
  \,.
$$

Given this, $\exp(\mathfrak{g})_{diff,smp}$ serves as a new [[resolution]] of $\exp(\mathfrak{g})$ for which the composite differential characteristic class is presented by the ordinary composite of morphisms of simplicial presheaves $curv_{smp}\circ \exp(\mu, cs)$.

This object $\exp(\mathfrak{g})_{diff}$ we shall see may be interpreted as the coefficient for _pseudo_ [[connection on an ∞-bundle|∞-connections]] with values in $\mathfrak{g}$. 

There is however still room to adjust this presentation such as to yield in each cohomology class special nice cocycle representatives. This we will achieve by finding naturally a [[subobject]] $\exp(\mathfrak{g})_{conn} \hookrightarrow \exp(\mathfrak{g})_{diff}$ whose inclusion is an isomorphism on connected components and restricted to which the morphism $curv_{smp} \circ \exp(\mu,cs)$ yields nice representatives in the [[de Rham cohomology|de Rham]] [[hypercohomology]] encoded by $\mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}_{smp}$, namely globally defined differential forms. On this object the differential characteristic classes we will show factors naturally through the refinements to differential cohomology, and hence $\exp(\mathfrak{g})_{conn}$ is finally identified as a presentation for the the coefficient object for [[connection on an ∞-bundle|∞-connections]] with values in $\mathfrak{g}$.


#### $\infty$-Pseudo-connections

We discuss presentations for the differential characteristic classes in the image of [∞-Lie integration](#LieIntegration).


Let $\mathfrak{g} \in L_\infty \stackrel{CE}{\hookrightarrow} dgAlg^{op}$ be an [[L-∞ algebra]].


+-- {: .num_defn}
###### Definition

A [[L-∞ algebra cohomology|L-∞ algebra cocycle]] on $\mathfrak{g}$ in degree $n$ is a morphism

$$
  \mu : \mathfrak{g} \to b^{n-1} \mathbb{R}
$$

to the [line Lie n-algebra](#LineLieNAlgebra).

=--

+-- {: .num_prop}
###### Observation

Every $L_\infty$-algebra cocycle induces canonically a morphism of [[simplicial presheaves]] of 
[exponentiated L-∞-algebras](#StrucLieAlg)

$$
  \exp(\mu)
   : 
  \exp(\mathfrak{g})
    \to 
  \exp(b^{n-1}\mathbb{R})
$$

given componentwise by postcomposition with the image of $\mu$ under $CE(-)$

$$
  \begin{aligned}
   \exp(\mu)(U, [k]) 
    & : 
   (\Omega^\bullet_{si,vert}(U \times \Delta^k) \stackrel{A}{\leftarrow} CE(\mathfrak{g}))
   \\
   &
   \mapsto 
   (\Omega^\bullet_{si,vert}(U \times \Delta^k) \stackrel{A}{\leftarrow} CE(\mathfrak{g}) \stackrel{CE(\mu)}{\leftarrow} CE(b^{n-1}\mathbb{R}))
  \end{aligned}
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

The **[[Weil algebra]]** $W(\mathfrak{g}) \in dgAlg$ is the unique 
representative of the [[free functor|free]] [[dg-algebra]] on the [[chain complex]] $\mathfrak{g}_\bullet^*[1]$ underlying $\mathfrak{g}$ such that the canonical projection $\mathfrak{g}_\bullet^*[1] \oplus \mathfrak{g}_\bullet^*[2] \to \mathfrak{g}_\bullet^*[1]$ extends to a [[dg-algebra]] homomorphism

$$
  CE(\mathfrak{g}) \leftarrow W(\mathfrak{g})
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

For $\mathfrak{g} \in L_\infty$ define the [[simplicial presheaf]] $\exp(\mathfrak{g})_{diff} \in [CartSp_{smooth}^{op}, sSet]$ by

$$
  \exp(\mathfrak{g})_{diff}
  :
  (U, [k])
  \mapsto
  \left\{
    \array{
      \Omega^\bullet_{si,vert}(U \times \Delta^k) 
        &\leftarrow& CE(\mathfrak{g})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U \times \Delta^k)
       &\leftarrow&
      W(\mathfrak{g})
    }
  \right\}
  \,,
$$

where on the left we have the set of [[commuting diagram]]s in [[dgAlg]] as indicated, with the vertical morphisms being the canonical projections.

=--

+-- {: .num_prop}
###### Observation

For $\mathfrak{g} = b^{n-1}\mathbb{R}$ the [[line Lie n-algebra]],
this subsumes the [previous definition](#DiffSmpForLineLienAlgebra).

=--

+-- {: .num_prop}
###### Proposition

The canonical projection

$$
  \exp(\mathfrak{g})_{diff} \to \exp(\mathfrak{g})
$$

is an acyclic fibration in $[CartSp_{smooth}^{op}, sSet]_{proj}$.

Moreover, for every $L_\infty$-algebra cocycle it fits into a commuting diagram

$$
  \array{
    \exp(\mathfrak{g})_{diff} 
      &\stackrel{\exp(\mu)_{diff}}{\to}&
    \exp(b^{n-1}\mathbb{R})_{diff} &=& 
    \mathbf{B}^n \mathbb{R}_{diff,smp}
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
   \exp(\mathfrak{g}) 
      &\stackrel{\exp(\mu)}{\to}&
   \exp(b^{n-1}\mathbb{R})
     &=&
   \mathbf{B}^n \mathbb{R}_{smp}
  }
$$

for some morphism $exp(\mu)_{diff}$.

=--

+-- {: .proof}
###### Proof

Both claims follow from the [[free functor|free property]] of the [[Weil algebra]].

For the first, we need to show that for all $U \in $ [[CartSp]] we have lifts in all diagrams of the form


$$
  \array{
     \partial \Delta[k] &\to& \exp(\mathfrak{g})_{diff,smp}(U)
     \\
     \downarrow && \downarrow 
     \\
     \Delta[k] &\to& \exp(\mathfrak{g})(U)
  }
  \,.
$$

The bottom morphism is a collection of [[differential form]]s on $U \times \Delta^k$ (with sitting instants), satisfying a flatness condition for their $d_{\Delta^k}$-differentials. The top morphism is a collection of forms on $U \times \partial \Delta^k $ with no flatness constraint except that those with no component along $U$ coincide with the restriction of those of the bottom morphism to the boundary $\partial \Delta^k$. These latter extend to a unique lift to the interior of the simplex. The remaining forms may be smoothly interpolated for instance to 0 in the interior of the simplex, while keeping at least one leg along $U$. Since for the top morphism there is no condition on the differentials, any choice will do.

For the second claim, let $U(CE(\mu))$ be the underlying morphism on chain complexes of $\mu$. Then we have the free dg-algebra homomorphism $F U (CE(\mu)) : W(b^{n-1}) \to W(\mathfrak{g})$ fitting into the [[commutative diagram]]

$$
  \array{
    CE(\mathfrak{g}) &\stackrel{CE(\mu)}{\leftarrow}& CE(b^{n-1}\mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g})
     &\stackrel{}{\leftarrow}&
    W(b^{n-1}\mathbb{R})
  }
  \,.
$$

[[pasting|Pasting]]-precomposition with this diagram yields a morhism $\exp(\mu)_{diff}$ as desired.

=--


+-- {: .num_defn}
###### Definition

Let $G \in Smooth \infty Grpd$ be an [[∞-group|n-group]] given by [Lie integration](#LieIntegration) of an [[L-∞ algebra]] $\mathfrak{g}$, in that the [[delooping]] object $\mathbf{B}G$ is presented by the $(n+1)$-[[simplicial skeleton|coskeleton]] [[simplicial presheaf]] 
$\mathbf{cosk}_{n+1}\exp(\mathfrak{g})$.

Then for $X \in [CartSp_{smooth}, sSet]_{proj}$ any object and $\hat X$ a cofibrant resolution, we say that 

$$
  [CartSp_{smooth}^{op},sSet](\hat X, \mathbf{cosk}_{n+1}\exp(\mathfrak{g})_{diff})
$$

is the [[Kan complex]] of **[[connection on an ∞-bundle|pseudo n-connections]]** on $G$-[[principal ∞-bundle]]s. 

=--

#### $\infty$-Connections

We discuss presentations in $[CartSp_{smooth}^{op}, sSet]$ of the
the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#ChernWeilTheory">intrinsic notion of ∞-connections</a> in $Smooth \infty Grpd$.


Let still $\mathfrak{g} \in _\infty \stackrel{CE(-)}{\hookrightarrow} dgAlg^{op}$ be an [[L-∞ algebra]].

+-- {: .num_defn}
###### Definition

An **[[invariant polynomial]]** on $\mathfrak{g}$ is an element 
$\langle - \rangle \in W(\mathfrak{g})$ such that both
$\langle - \rangle \in \wedge^\bullet$
as well as $d_{W(\mathfrak{g})}\; \langle - \rangle $ 
are elements in the graded subalgebra generated by the shifted generators $\mathfrak{g}^*[1] \hookrightarrow W(\mathfrak{g})$;

Write $inv(\mathfrak{g}) \hookrightarrow W(\mathfrak{g})$ for the sub-dg-algebra of invariant polynomials.

=--

+-- {: .num_prop}
###### Observation

For the [[line Lie n-algebra]] we have 

$$
  \mathrm{inv}(b^{n-1}\mathbb{R}) \simeq CE(b^n \mathbb{R})
  \,.
$$

This allows us to identify an invariant polynomial $\langle - \rangle$ of degree $n+1$ with a morphism

$$
  inv(\mathfrak{g}) \stackrel{\langle - \rangle}{\leftarrow}
  inv(b^{n-1}\mathbb{R})
$$

in [[dgAlg]].

=--


+-- {: .num_defn}
###### Definition

We say an invariant polynomial $\langle - \rangle$ on $\mathfrak{g}$ is **in transgression** with an [[∞-Lie algebra cohomology|L-∞ algebra cocycle]] $\mu : \mathfrak{g} \to b^{n-1} \mathbb{R}$ if 
there is a morphism $cs : W(b^{n-1}\mathbb{R}) \to W(\mathfrak{g})$
such that we have a [[commuting diagram]]

$$
  \array{
    CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}&
    CE(b^{n-1}\mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{cs}{\leftarrow}&
    W(b^{n-1}\mathbb{R})
    \\
    \uparrow && \uparrow
    \\
    inv(\mathfrak{g}) &\stackrel{\langle- \rangle}{\leftarrow}&
    inv(b^{n-1}\mathbb{R}) & = CE(b^n \mathbb{R})
  }
  \,.
$$

We say that $cs$ is a **[[Chern-Simons element]]** 
exhibiting the transgression between $\mu$ and $\langle - \rangle$.

We say that an $L_\infty$-algebra cocycle is **transgressive**
if it is in transgression with some invariant polynomial.

=--

+-- {: .num_prop}
###### Observation

We have

1. There is a transgressive cocycle for every invariant polynomial.

1. Any two $L_\infty$-algebra cocycles in transgression 
   with the same invariant polynomial are cohomologous.

1. Every decomposable invariant polynomial 
   (the wedge product of 
   two non-vanishing invariant polynomials) transgresses 
   to a cocycle cohomologous to 0.

=--

+-- {: .proof}
###### Proof

1. By the fact that the [[Weil algebra]]  is free, its
[[cochain cohomology]] vanishes and hence the definition
property $d_{W(\mathfrak{g})} \langle -\rangle = 0$ implies
that there is some element $cs \in W(\mathfrak{g})$ such that
$d_{W(\mathfrak{g})} cs = \langle - \rangle$. Then the image
of $cs$ along the canonical dg-algebra homomorphism
$W(\mathfrak{g}) \to CE(\mathfrak{g})$ is $d_{CE(\mathfrak{g})}$-closed hence is a cocycle on $\mathfrak{g}$.
This is by construction in transgression with $\langle - \rangle$.

1. Let $cs_1$ and $cs_2$ be Chern-Simons elements for the 
   to given $L_\infty$-algebra cocycles. Then by assumption
   $d_{(\mathfrak{g})} (cs_1 - cs_2) = 0 $. By the acyclicity of
   $W(\mathfrak{g})$ there is then $\lambda \in W(\mathfrak{g})$
   such that $cs_1 = cs_2 + d_{W(\mathfrak{g})} \lambda$.  
   Since 
   $W(\mathfrak{g}) \to CE(\mathfrak{g})$ is a dg-algebra 
   homomorphism this implies that also
   $\mu_1 = \mu_2 + d_{CE(\mathfrak{g})} \lambda|_{CE(\mathfrak{g})}$.

1. Given two nontrivial invariant polynomials 
   $\langle - \rangle_1$ and $\langle - \rangle_2$ let
   $cs_1 \in W(\mathfrak{g})$ be any element such that
   $d_{W(\mathfrak{g})}cs_1 = \langle - \rangle_1$.
   Then  $cs_{1,2} := cs_1 \wedge \langle -\rangle_2$ satisfies
   $d_{W(\mathfrak{g})} cs_{1,2} = 
     \langle - \rangle_1 \wedge \langle -\rangle_2$. By the
   first observation the restriction of $cs_{1,2}$ to 
   $CE(\mathfrak{g})$ is therefore a cocycle in transgression
   with $\langle - \rangle_1 \wedge \langle -\rangle_2$. But
   by the definition of invariant polynomials the restriction of
   $\langle - \rangle_2$ vanishes, and hence so does that 
   of $cs_{1,2}$.
   The claim the follows with the second point above.

=--

+-- {: .num_defn}
###### Definition

Define the [[simplicial presheaf]] $\exp(\mathfrak{g})_{ChW} \in [CartSp_{smooth}^{op}, sSet]$
by the assignment

$$
  \exp(\mathfrak{g})_{ChW} : 
   (U , [k])
   \mapsto
   \left\{
     \array{
       \Omega^\bullet_{si,vert}(U \times \Delta^k )
       &\stackrel{A_{vert}}{\leftarrow}&
       CE(\mathfrak{g})
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet_{si}(U \times \Delta^k )
       &\stackrel{A}{\leftarrow}&
       W(\mathfrak{g})        
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U)
       &\stackrel{\langle F_A\rangle}{\leftarrow}&
       inv(\mathfrak{g})
     }
   \right\} 
   \,,
$$

where on the right we have the set of horizontal morphisms in [[dgAlg]] making [[commuting diagram]]s with the canonical vertical morphisms as indicated.

We call $\langle F_A \rangle$ the 
**[[curvature characteristic forms]]**
of $A$.

=--


Let

$$
  \array{
    \exp(\mathfrak{g})_{diff}
      & \stackrel{(\exp(\mu_i,cs_i))_i}{\to} &
    \prod_{i}
     \exp(b^{n_i-1}\mathbb{R})_{diff}
     &\stackrel{((curv_i)_{smp})}{\to}&
      \prod_i \mathbf{\flat}_{dR}\mathbf{B}^{n_i}_{smp}
   \\
   \downarrow^{\mathrlap{\simeq}}
   \\
   \exp(\mathfrak{g})
  }
$$

be the presentation, as above, of the [[product]] of all
[[differential characteristic class|differential refinements of characteristic classes]] on
$\exp(\mathfrak{g})$ induced from [[Lie integration]] of 
transgressive [[∞-Lie algebra cohomology|L-∞ algebra cocycles]].



+-- {: .num_prop #CharacterizationOfexpChW}
###### Observation

We have that $\exp(\mathfrak{g})_{ChW}$ is the 
[[pullback]] in $[CartSp_{smooth}^{op}, sSet]$ of the globally defined closed forms along the curvature characteristics induced by all transgressive $L_\infty$-algebra cocycles:

$$
  \array{
    \exp(\mathfrak{g})_{ChW} &\stackrel{\exp(\mu,cs)}{\to}&
    \prod_{n_i} \Omega^{n_i + 1}_{cl}(-)
    \\
    \downarrow && \downarrow
    \\
    \exp(\mathfrak{g})_{diff,smp} 
      &\stackrel{({curv}_i)_i}{\to}& 
    \prod_i \mathbf{\flat}_{dR} \mathbf{B}^{n_i + 1} \mathbb{R}_{smp}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \exp(\mathfrak{g})
  }
  \,.
$$

=--

  

+-- {: .proof}
###### Proof

By the [above proposition](#CurvSmp) we have that the bottom
horizontal morphims sends over each $(U,[k])$ 
and for each $i$ an element

$$
  \array{
    \Omega^\bullet_{si,vert}(U \times \Delta^k) 
      &\stackrel{A_{vert}}{\leftarrow}&
    CE(\mathfrak{g})
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet_{si}(U \times \Delta^k)
     &\stackrel{A}{\leftarrow}&
    W(\mathfrak{g})
  }
$$

of $\exp(\mathfrak{g})(U)_k$ to the composite

$$
 \left( \;
  \Omega^\bullet_{si}(U \times \Delta^k)
  \stackrel{A}{\leftarrow}
  W(\mathfrak{g})
  \stackrel{cs_i}{\leftarrow}
  W(b^{n_i-1} \mathbb{R})
  \stackrel{}{\leftarrow}
  inv(b^{n_i} \mathbb{R}) = CE(b^{n_i}\mathbb{R}))
  \; \right)
$$

$$
  = \left( \;
      \Omega^\bullet_{si}(U \times \Delta^k)
      \stackrel{\langle F_A\rangle_i}{\leftarrow}
      CE(b^{n_i}\mathbb{R})
    \; \right)
$$

regarded as an element in 
$\mathbf{\flat}_{dR} \mathbf{B}^{n_i+1}_{smp}(U)_k$. The
right vertical morphism 
$\Omega^{n_i + 1}(U) \to \mathbf{\flat}_{dR}\mathbf{B}^{n_i+1}\mathbb{R}_{smp}(U)$ from the constant simplicial set of 
closed $(n_i+1)$-forms on $U$ 
picks precisely those of these elements for which
$\langle F_A\rangle$ is a basic form on the $U \times \Delta^k$-bundle in that it is in the image of the pullback
$\Omega^\bullet(U) \to \Omega^\bullet_{si}(U \times \Delta^k)$.


=--



+-- {: .num_remark}
###### Remark

This shows that $\exp(\mathfrak{g})_{ChW}$ serves as a convenient
object on which the differential characteristic classes of 
$\exp(\mathfrak{g})$ are supported.

For more see [[connection on a smooth principal ∞-bundle]].


=--



### Higher holonomy and Chern-Simons functional {#StrucChernSimons}

* [[schreiber:∞-Chern-Simons theory]]



## References

For standard references on [[differential geometry]] and [[Lie groupoid]]s see there. 

The $(\infty,1)$-topos $Smooth \infty Grpd$ is discussed in section 3.3 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

A discussion of smooth $\infty$-groupoids as $(\infty,1)$-sheaves on $CartSp$ and the presentaton of the $\infty$-Chern-Weil homomorphism on these is in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Cech cocycles for differential characteristic classes -- An $\infty$-Lie theoretic construction_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#FSS">web</a>).

For references on  [[Chern-Weil theory in Smooth∞Grpd]] and [[connection on a smooth principal ∞-bundle]], see there.

The results on differentiable [[Lie group cohomology]] used above are in 

* P. Blanc, _Cohomologie diff&eacute;rentiable et changement de groupes_ Ast&eacute;risque, vol. 124-125 (1985), pp. 113-130.
{#Blanc}

and

* [[Jean-Luc Brylinski]], _Differentiable Cohomology of Gauge Groups_ ([arXiv](http://arxiv.org/abs/math/0011069))
{#Brylinski}

which parallels 

* [[Graeme Segal]], _Cohomology of topological groups_ , Symposia Mathematica, Vol IV (1970) (1986?) p. 377
{#Segal}

A review is in section 4 of 

* [[Chris Schommer-Pries]], _A finite-dimensional String 2-group_ ([arXiv:0911.2483](http://arxiv.org/abs/0911.2483))
{#SchommerPries}


Classification of topological [[principal 2-bundle]]s is discussed in 

* [[John Baez]], [[Danny Stevenson]], _The classifying space of a topological 2-group_ Algebraic Topology
Abel Symposia, 2009, Volume 4, 1-31 ([arXiv:0801.3843](http://arxiv.org/abs/0801.3843))
 {#BaezStevenson}

and the generalization to classification of smooth [[principal 2-bundle]]s is in 

* [[Thomas Nikolaus]], [[Konrad Waldorf]], _Four Equivalent Versions of Non-Abelian Gerbes_ ([arXiv:1103.4815](http://arxiv.org/abs/1103.4815))
 {#NikolausWaldorf}

[[!redirects smooth ∞-groupoid -- structures]]