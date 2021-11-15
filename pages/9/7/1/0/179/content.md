

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

An _$\infty$-Lie algebroid_ is a [[smooth ∞-groupoid]] (or rather a [[synthetic-differential ∞-groupoid]]) all whose [[k-morphism]]s for all $k$ have _[[infinitesimal space|infinitesimal]] extension_ (are infinitesimal neighbours of an identity $k$-morphism).

$\infty$-Lie algebroids are to [[∞-Lie groupoids]] as [[Lie algebras]] are to [[Lie groups]]:

* [[Lie group]] - [[Lie algebra]]

* [[Lie groupoid]] - [[Lie algebroid]]

* [[∞-group|∞-Lie group]] - [[L-infinity-algebra|∞-Lie algebra]]

* [[∞-Lie groupoid]] - **$\infty$-Lie algebroid** .


## Definition

We discuss $\infty$-Lie algebroids in the [[cohesive (∞,1)-topos]] $\mathbf{H}_{th} := $[[SynthDiff∞Grpd]] of [[synthetic differential ∞-groupoid]]s. This is an <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#InfinitesimalCohesion">infinitesimal cohesive neigbourhood</a> of the cohesive $(\infty,1)$-topos $\mathbf{H} :=$ [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s, which is exhibited by the <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#InfinitesimalPaths">infinitesimal path</a> [[(∞,1)-geometric morphism]]

$$
  (\Pi_{inf} \dashv Disc_{inf} \dashv \Gamma_{inf}) : 
  SynthDiff\infty Grpd
   \to
  Smooth\infty Grpd
  \,.
$$




### Presentation by dg-algebras and simplicial presheaves
 {#PresentationByCE}

We consider _presentations_ of the 
general abstract definition \ref{TheGeneralAbstractDefinition} of $\infty$-Lie algebroids by constructing in the standard [[model structure]]-[[presentable (∞,1)-category|presentation]] of $SynthDiff\infty Grpd$ by [[simplicial presheaves]] on [[CartSp]]${}_{synthdiff}$ certain classes of simplicial presheaves in the image of [[semifree dga|semi-free]] [[differential graded algebra]]s under the [[monoidal Dold-Kan correspondence]]. This amounts to identifying the traditional description of of [[Lie algebra]]s, [[Lie algebroid]]s and [[L-∞ algebra]]s by their [[Chevalley-Eilenberg algebra]]s as a convenient characterization of the corresponding [[cosimplicial algebra]]s whose formal dual simplicial presheaves are manifest presentations of infinitesimal [[smooth ∞-groupoid]]s.



+-- {: .num_defn #LInftyGlgebroid}
###### Definition

Let

$$
  L_\infty Algd \hookrightarrow dgCAlg_{\mathbb{R}}^{op}
$$

be the [[full subcategory]] on the [[opposite category]] of cochain [[dg-algebra]]s over $\mathbb{R}$ on those dg-algebras that are

* graded-commutative;

* concentrated in non-negative degree (the [[differential]] being of degree +1 );

* in degree 0 of the form $C^\infty(X)$ for $X \in$ [[SmoothMfd]];

* [[semifree dga|semifree]]: their underlying [[graded algebra]] is [[isomorphic]] to an [[exterior algebra]] on a $\mathbb{N}$-graded locally free [[projective object|projective]] $C^\infty(X)$-[[module]]

* of finite [[rank]];

=--

We call this the category of **$L_\infty$-algebroids**.


More in detail, an object $\mathfrak{a} \in L_\infty Algd$ may be identified (non-canonically) with a pair $(CE(\mathfrak{a}), X)$, where

* $X \in SmoothMfd$ is a [[smooth manifold]] -- called the **base space** of the $L_\infty$-algebroid ;

* $\mathfrak{a}$ is the module of smooth [[section]]s of an $\mathbb{N}$-graded [[vector bundle]] of degreewise finite [[rank]];

* $CE(\mathfrak{a}) = (\wedge^\bullet_{C^\infty(X)} \mathfrak{a}^*, d_{\mathfrak{a}})$ is a [[semifree dga]] on $\mathfrak{a}^*$ -- a [[Chevalley-Eilenberg algebra]] -- where

  $$
    \wedge^\bullet_{C^\infty(X)}\mathfrak{a}^* = 
      C^\infty(X) 
       \; \oplus \;
      \mathfrak{a}^*_0
       \; \oplus \;
      (
      \mathfrak{a}^*_0 \wedge_{C^\infty(X)} \mathfrak{a}^*_0
       \oplus
      \mathfrak{a}^*_1
      )
      \; \oplus \; \cdots
  $$

  with the $k$th summand on the right being in degree $k$.

+-- {: .num_defn #LInfinityAlgebras}
###### Definition

An $L_\infty$-algebroid with base space $X = *$ the [[point]] is an [[L-∞ algebra]] $\mathfrak{g}$, or rather is the [[delooping]] of an $L_\infty$-algebra. We write $b \mathfrak{g}$ for $L_\infty$-algebroids over the point. They form the full [[subcategory]]

$$
  L_\infty Alg \hookrightarrow L_\infty Algd
  \,.
$$

=--


We now construct an embedding of $L_\infty Algs$ into $SynthDiff\infty Grpd$. 

The functor

$$
  \Xi : Ch^\bullet_+(\mathbb{R}) \to Vect_{\mathbb{R}}^{\Delta}
$$

of the [[Dold-Kan correspondence]] from non-negatively graded [[cochain complex]]es of [[vector space]]s to [[cosimplicial object|cosimplicial]] vector spaces is a [[lax monoidal functor]] and hence induces (see [[monoidal Dold-Kan correspondence]]) a functor (which we shall denote by the same symbol)

$$
  \Xi : dgAlg_{\mathbb{R}}^+ \to Alg_{\mathbb{R}}^{\Delta}
$$

from non-negatively graded cochain [[dg-algebra]]s to [[cosimplicial algebra]]s (over $\mathbb{R}$).


+-- {: .num_defn #PresentationByMonoidalDoldKan}
###### Definition

Write

$$
  \Xi : L_\infty Algd \to (CAlg_{\mathbb{R}}^\Delta)^{op} 
$$

for the restriction of the above $\Xi$ along the inclusion $L_\infty Algd \hookrightarrow dgAlg^{op}_{\mathbb{R}}$:

for $\mathfrak{a} \in L_\infty Algd$ the underlying cosimplicial vector space of $\Xi \mathfrak{a}$ is given by 

$$
  \Xi \mathfrak{a} 
   : 
  [n]
    \mapsto
  \bigoplus_{i = 0}^{n}
  CE(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n
$$

and the product of the $\mathbb{R}$-algebra structure on the right is given on homogeneous elements $(\omega,x), (\lambda,y) \in CE(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n$ in the [[tensor product]] by

$$
  (\omega , x)\cdot (\lambda ,y) = (\omega \wedge \lambda , x \wedge y)
  \,.
$$

(Notice that $\Xi \mathfrak{a}$ is indeed a _commutative_ cosimplicial algebra, since $\omega$ and $x$ in $(\omega,x)$ are by definition in the same degree.)

To define the [[cosimplicial object|cosimplicial structure]], let 
$\{e_j\}_{j = 0}^n$ be the canonical [[basis]] for $\mathbb{R}^n$ and consider also the basis $\{v_j\}_{j = 0}^n$ given by

$$
  v_{j} := e_j - e_{0}
  \,.
$$
 
Then for $\alpha : [k] \to [l]$ a morphism in the [[simplex]] category, set

$$
  \alpha v_j := v_{\alpha(j)} - v_{\alpha(0)}
$$

and extend this skew-multilinearly to a map $\alpha : \wedge^\bullet \mathbb{R}^k \to \wedge^\bullet \mathbb{R}^l$. In terms of all this the action of $\alpha$ on homogeneous elements $(\omega,x)$ in the cosimplicial algebra is defined by

$$
  \alpha : 
  (\omega, x) 
    \mapsto
  (\omega, \alpha x) + (d_\mathfrak{a} \omega , v_{\alpha(0)}\wedge \alpha(x))
$$

=--


This is due to ([CastiglioniCortinas, (1), (2), (20), (22)](#CastiglioniCortinas)).

We shall refine the image of $\Xi$ to cosimplicial [[smooth algebra]]s. Let $T := $[[CartSp]]${}_{smooth}$ be the category of [[Cartesian space]]s and [[smooth function]]s between them, regarded as a [[Lawvere theory]]. Write 

$$
  SmoothAlg := T Alg
$$

for its category of [[algebra over a Lawvere theory|algebras]]: these are the [[smooth algebra]]s.

Notice that there is a canonical [[forgetful functor]]

$$
  U : SmoothAlg \to CAlg_{\mathbb{R}}
$$

to the category of [[associative algebra|comutative associative algebras]] over the [[real numbers]].

+-- {: .num_prop #SmoothMonoidalDoldKan}
###### Proposition

There is a unique factorization of the functor $\Xi : L_\infty Algd \to (CAlg_{\mathbb{R}}^\Delta)^{op}$ from def. \ref{PresentationByMonoidalDoldKan} through the [[forgetful functor]]
$(SmoothAlg_{\mathbb{R}}^\Delta)^{op} \to (CAlg_{\mathbb{R}}^\Delta)^{op}$ such that for any $\mathfrak{a}$ over base space $X$ the degree-0 algebra of smooth functions $C^\infty(X)$ lifts to its canonical structure as a [[smooth algebra]]

$$
  \array{
    && (SmoothAlg^{\Delta})^{op}
    \\
    & \nearrow & \downarrow^{\mathrlap{U}}
    \\
    L_\infty Algd &\to& (CAlg_{\mathbb{R}}^\Delta)^{op}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

Observe that for each $n$ the algebra $(\Xi \mathfrak{a})_n$ is a finite nilpotent extension of $C^\infty(X)$. The claim then follows with using [[Hadamard's lemma]] to write every smooth function of sums as a finite Taylor expansion with a smooth rest term. See the examples at [[smooth algebra]] for more details on this kind of argument.

=--

+-- {: .num_defn #EmbeddingOfThePresentation}
###### Definition

Write $i : L_\infty Algd \to SynthDiff\infty Grpd$ for the composite [[(∞,1)-functor]]

$$
  L_\infty Algd 
     \stackrel{\Xi}{\to} 
  (SmoothAlg^{\Delta})^{op}
    \stackrel{j}{\to} 
  [CartSp_{synthdiff}^{op}, sSet]
   \stackrel{P Q}{\to}
  ([CartSp_{synthdiff}^{op}, sSet]_{loc})^\circ
  \simeq
  SynthDiff\infty Grpd
  \,,
$$

where the first morphism is the [[monoidal Dold-Kan correspondence]] as in prop. \ref{SmoothMonoidalDoldKan}, the second is the external degreewise [[Yoneda embedding]] and $P Q$ is any fibrant-cofibrant [[resolution]] functor in the local [[model structure on simplicial presheaves]]. The last equivalence holds as discussed there and at [[models for ∞-stack (∞,1)-toposes]].

=--

+-- {: .num_remark #RemarkOnModelStructure}
###### Remark

We do not consider the standard [[model structure on dg-algebras]] and do not consider $L_\infty Algd$ itself as a [[model category]] and do not consider an [[(∞,1)-category]] spanned by it. Instead, the functor $i : L_\infty Algd \to SynthDiff\infty Grpd$ only serves to exhibit a class of objects in $SynthDiff\infty Grpd$, which below in the section [Models for the abstract axioms](#ModelsForTheAbstractAxioms) we show are indeed $\infty$-Lie algebroids by the general abstract definition, \ref{TheGeneralAbstractDefinition}. All the [[homotopy theory]] of objects in $L_\infty Algd$ is that of $SynthDiff\infty Grpd$ after this embedding.

=--

### General abstract definition
 {#GeneralAbstractDefinition}

We may abstractly formalize this in an [[(infinity,1)-topos]] $\mathbf{H}$ with [[differential cohesion]] as follows.

Recall that a [[groupoid object in an (infinity,1)-category]] is equivalently an [[1-epimorphism]] $X \longrightarrow \mathcal{G}$, thought of as exhibiting an [[atlas]] $X$ for the groupoid $\mathcal{G}$.

Now an $\infty$-Lie algebroid is supposed to be an $\infty$-groupoid which is only infinitesimally extended over its base space $X$. Hence: 

A groupoid object $p \colon X \longrightarrow \mathcal{G}$ is _infinitesimal_ if under the [[reduction modality]] $\Re$ (equivalently under the [[infinitesimal shape modality]] $\Im$) the [[atlas]] becomes an [[equivalence in an (infinity,1)-category|equivalence]]: $\Re(p), \Im(p) \in Equiv$.

For example the tangent $\infty$-Lie algebroid $T X$ of any $X$ is the [[unit of a monad|unit]] of the [[infinitesimal shape modality]].

$$
  \eta^{\Im}_X \;\colon\; X \stackrel{}{\longrightarrow} \Im X
  \,.
$$

It follows that every such $\infty$-Lie algebroid $X \to \mathcal{G}$ canonically maps to the tangent $\infty$-Lie algebroid of $X$ -- the _anchor map_. The naturality square of the unit $\eta^{\Im}_{p}$ exhibits the morphism:

$$
  \array{
     X & \stackrel{id}{\longrightarrow} & X
     \\
     \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{\eta^\Im_X}}
     \\
      &&  \Im X
     \\
     \downarrow && \downarrow^{\mathrlap{\Im p}}_\simeq
     \\
     \mathcal{G}
     &\stackrel{\eta^{\Im}_{\mathcal{G}}}{\longrightarrow}& \Im \mathcal{G}
  }
$$


## Properties

### General

+-- {: .num_prop #prop}
###### Proposition

The full subcategory category $L_\infty Alg \hookrightarrow L_\infty Algd$ from def. 
\ref{LInfinityAlgebras} is equivalent to the traditional definition  of the category of [[L-∞ algebra]]s and "weak morphisms" / "sh-maps" between them.

The full subcategory $LieAlgd \hookrightarrow L_\infty Algd$ on the 1-truncated objects is equivalent to the traditional category of [[Lie algebroid]]s (over [[smooth manifold]]s).

In particular the joint intersection $Lie Alg \hookrightarrow L_\infty Alg$ on the 1-truncated $L_\infty$-algebras is equivalent to the category of ordinary [[Lie algebra]]s.


=--

This is discussed in detail at [[L-∞ algebra]] and [[Lie algebroid]].


### Models for the abstract axioms
 {#ModelsForTheAbstractAxioms}

Above we have given a general abstract definition, 
def. \ref{TheGeneralAbstractDefinition}, of $\infty$-Lie algebroids, and then a concrete construction in terms of [[dg-algebra]]s, def. \ref{PresentationByMonoidalDoldKan}. Here we discuss that this concrete construction is indeed a presentation for objects satisfying the abstract axioms.

As in the discussion at [[SynthDiff∞Grpd]] we now present this [[cohesive (∞,1)-topos]] by the [[hypercompletion]] of the [[model structure on simplicial presheaves]] $[FSmoothDiff^{op}, sSet]_{proj,loc}$ of formal smooth manifolds.


+-- {: .num_lemma #CofibrantResolutionOfLinfinityAlgebroid}
###### Lemma

For $\mathfrak{a} \in L_\infty Algd$ and $i(\mathfrak{a}) \in [FSmoothMfd^{op}, sSet]_{proj,loc}$ its image in the standard presentation for [[SynthDiff∞Grpd]],  we have that

$$
  \left(
  \int^{[k]\in \Delta}
    \mathbf{\Delta}[k] \cdot i(\mathfrak{a})_k
  \right)
   \stackrel{\simeq}{\to}
  i(\mathfrak{a})
$$

is a cofibrant [[resolution]], where $\mathbf{\Delta} : \Delta \to sSet$ is the [[fat simplex]].

=--


+-- {: .proof}
###### Proof

We have

1. The [[fat simplex]] is cofibrant in $[\Delta, sSet_{Quillen}]_{proj}$. 

1. The canonical morphism $\mathbf{\Delta} \to \Delta$ is a weak equivalence between cofibrant objects in the [[Reedy model structure]] $[\Delta, sSet_{Quillen}]_{Reedy}$.

1. Because every representable $FSmoothMfd \hookrightarrow [FSmoothMfd^{op}, sSet]_{proj,loc}$ is cofibrant, the object $i(\mathfrak{a})_\bullet \in [\Delta^{op}, [FSmoothMfd^{op}, sSet]_{proj,loc} ]_{inj}$ is cofibrant.

1. Every [[simplicial presheaf]] is cofibrant regarded as an object [[Reedy model structure]] $[\Delta^{op}, [FSmoothMfd^{op}, sSet]_{inj}]_{Reedy}$.

Now the [[coend]] over the [[tensoring]] 

$$
  \int^{[k] \in \Delta}

  (-)\cdot (-)
  : 
  [\Delta, sSet_{Quillen}]_{proj} 
    \times
  [\Delta^{op}, [FSmoothMfd^{op}, sSet]_{proj,loc} ]_{inj}
  \to 
  [FSmoothMfd^{op}, sSet]_{proj,loc}
$$

is a [[Quillen bifunctor]] (as discussed there) for the projective and injective [[global model structure on functors]] on the [[simplex category]] and its opposite as indicated. This implies the cofibrancy.

It is also a [[Quillen bifunctor]] (as discussed there) for the [[Reedy model structure]]s

$$
  \int^{[k] \in \Delta}
  (-)\cdot (-)
  : 
  [\Delta, sSet_{Quillen}]_{Reedy} 
    \times
  [\Delta^{op}, [FSmoothMfd^{op}, sSet]_{inj} ]_{Reedy}
  \to 
  [FSmoothMfd^{op}, sSet]_{inj}
  \,.
$$

Using the [[factorization lemma]] this implies the weak equivalence (this is the argument of the [[Bousfield-Kan map]]).
   
=--




+-- {: .num_prop #LInftyAlgIsInfinitesimalObject}
###### Proposition

Let $\mathfrak{g}$ be an [[L-∞ algebra]], regarded as an $L_\infty$-algebroid $b \mathfrak{g} \in L_\infty Algd$ over the point
by the embedding of def. \ref{LInfinityAlgebras}.

Then $i(b \mathfrak{g}) \in $ [[SynthDiff∞Grpd]] is an 
<a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#LieAlgebras">infinitesimal cohesive object</a>, in that it is <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#Homotopy">geometrically contractible</a>

$$
  \Pi b \mathfrak{g} \simeq *
$$

and has as underlying [[discrete ∞-groupoid]] the point

$$
  \Gamma b \mathfrak{g} \simeq *
  \,.
$$

=--

+-- {: .proof}
###### Proof

We present now [[SynthDiff∞Grpd]] by the [[model structure on simplicial presheaves]] $[CartSp_{synthdiff}^{op}, sSet]_{proj,loc}$. Since [[CartSp]]${}_{synthdiff}$ is an [[∞-cohesive site]] we have by the discussion there that $\Pi$ is presented by the left [[derived functor]] $\mathbb{L} \lim\to$ of the degreewise [[colimit]] and $\Gamma$ is presented by the left [[derived functor]] of evaluation on the point.

With lemma \ref{CofibrantResolutionOfLinfinityAlgebroid} we can evaluate 

$$
  \begin{aligned}
     (\mathbb{L} \lim_\to) i(b\mathfrak{g})
     & \simeq
    \lim_\to \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot 
     (b \mathfrak{g})_{k} 
    \\
     & \simeq
    \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot 
     \lim_\to (b \mathfrak{g})_{k}  
    \\
     & =
    \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot *
  \end{aligned}
  \,,
$$ 

because each $(b \mathfrak{g})_n \in InfPoint \hookrightarrow CartSp_{smooth}$ is an [[infinitesimally thickened point]], hence representable and hence sent to the point by the colimit functor.

That this is equivalent to the point follows from the fact that $\emptyset \to \mathbf{\Delta}$ is an acylic cofibration in $[\Delta, sSet_{Quillen}]_{proj}$, and that

$$
  \int^{[k] \in \Delta}
  (-)\times (-)
  : 
  [\Delta, sSet_{Quillen}]_{proj}
  \times
  [\Delta^{op}, sSet_{Qillen}]_{inj}
  \to 
  sSet_{Quillen}
$$

is a [[Quillen bifunctor]], using that $* \in [\Delta^{op}, sSet_{Quillen}]_{inj}$ is cofibrant.

Similarily, we have degreewise that 

$$
  Hom(*, (b \mathfrak{g})_n) = *
$$

by the fact that an [[infinitesimally thickened point]] has a single global point. Therefore the claim for $\Gamma$ follows analogously.

=--

+-- {: .num_prop}
###### Proposition

Let $(\mathfrak{a} \to T X) \in L_\infty Algd \hookrightarrow [CartSp_{synthdiff}, sSet]$ be an $L_\infty$-algebroid,
def. \ref{LInftyGlgebroid}, over a 
[[smooth manifold]] $X$, regarded as a [[simplicial presheaf]]  and hence as a presentation for an object in $SynthDiff \infty Grpd$
according to def. \ref{EmbeddingOfThePresentation}.

We have an equivalence

$$
  \mathbf{\Pi}_{inf}(\mathfrak{a}) \simeq \mathbf{\Pi}_{inf}(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let first $X = U \in CartSp_{synthdiff}$ be a representable. 
Then according to prop. \ref{CofibrantResolutionOfLinfinityAlgebroid} we have that 

$$
  \hat \mathfrak{a}
  :=
  \left(
    \int^{k \in \Delta} \mathbf{\Delta}[k] \cdot \mathfrak{a}_k 
  \right)
  \simeq
  \mathfrak{a}
$$ 

is cofibrant in
$[CartSp_{synthdiff}^{op}, sSet]_{proj}$ . Therefore by <a href="http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#InfinitesimalNeighbourhoodFromInfinitesimalSite">this proposition</a> on the presentation of infinitesimal neighbourhoods by [[simplicial presheaves]] over _infinitesimal neighbourhood sites_
we compute the [[derived functor]]

$$
  \begin{aligned}
    \mathbf{\Pi}_{inf}(\mathfrak{a}) & \simeq i_* i^* \mathfrak{a} 
    \\
     & \simeq \mathbb{L} ((-) \circ p) \mathbb{L} ((-) \circ i) \mathfrak{a} 
    \\
    & \simeq ((-) \circ i p ) \hat \mathfrak{a} 
  \end{aligned}
$$

with the notation as used there.

In view of def. \ref{PresentationByMonoidalDoldKan} we have for all $k \in \mathbb{N}$ that  $\mathfrak{a}_k = X \times D$ where $D$ is an [[infinitesimally thickened point]]. Therefore $((-) \circ i p ) \mathfrak{a}_k = ((-) \circ i p ) X$ for all $k$ and hence $((-) \circ i p ) \hat \mathfrak{a} \simeq \mathbf{\Pi}_{inf}(X)$.

For general $X$ choose first a cofibrant [[resolution]] by a [[split hypercover]] that is degreewise a coproduct of representables (which always exists, by the discussion at [[model structure on simplicial presheaves]]), then pull back the above discussion to these covers.

=--


+-- {: .num_cor #LInfinityAlgebrboidsAreFormalInfinityGroupoids}
###### Corollary

Every $L_\infty$-algebroid in the sense of 
def. \ref{LInftyGlgebroid} under the embedding of 
def. \ref{EmbeddingOfThePresentation} is indeed 
a [[formal cohesive ∞-groupoid]] in the sense of def. \ref{TheGeneralAbstractDefinition}.

=--





### Cohomology of $\infty$-Lie algebroids
  {#Cohomology}

We discuss the relation between the intrinsic [[cohomology]] of $L_\infty$-algebroids when regarded as objects of $SynthDiff\infty Grpd$, and the ordinary cohomology of their [[Chevalley-Eilenberg algebra]]s. For more on this see [[∞-Lie algebroid cohomology]].


+-- {: .num_prop #IntrinsicRealCohomologyByCECohomology}
###### Proposition

Let $\mathfrak{a} \in L_\infty Algd$ be an $L_\infty$-algebroid. Then its <a href="">intrinsic real cohomoloogy</a> in [[SynthDiff∞Grpd]]

$$
  H^n(\mathfrak{a}, \mathbb{R})
  :=
  \pi_0 SynthDiff\infty Grpd(\mathfrak{a}, \mathbf{B}^n \mathbb{R})
$$

coincides with its ordinary [[L-∞ algebra cohomology]]: the [[cochain cohomology]] of its [[Chevalley-Eilenberg algebra]]

$$
  H^n(\mathfrak{a}, \mathbb{R})
   \simeq
  H^n(CE(\mathfrak{a}))
  \,.
$$

=--


+-- {: .proof}
###### Proof

By <a href="http://nlab.mathforge.org/nlab/show/synthetic+differential+infinity-groupoid#StrucCohomology">this discussion</a> at [[SynthDiff∞Grpd]] we have that 

$$
  H^n(\mathfrak{a}, \mathbb{R}) \simeq
  H^n N^\bullet(\mathbb{L}\mathcal{O})(i(\mathfrak{a}))
  \,.
$$

By lemma \ref{CofibrantResolutionOfLinfinityAlgebroid} this is

$$
  \cdots \simeq
  H^n N^\bullet
  \left(
    \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \mathcal{O}(i(\mathfrak{a})_k)
  \right)
  \,.
$$

Observe that $\mathcal{O}(\mathfrak{a})_\bullet$ is cofibrant in the [[Reedy model structure]] $[\Delta^{op}, (SmoothAlg^{\Delta_{proj}})^{op}]_{Reedy}$ relative to the opposite of the projective [[model structure on cosimplicial algebras]]:  the map from the latching object in degree $n$ in $SmoothAlg^\Delta)^{op}$ is dually in $SmoothAlg \hookrightarrow SmoothAlg^\Delta$ the projection 

$$
  \oplus_{i = 0}^n CE(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n
  \to
  \oplus_{i = 0}^{n-1} CE(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n
$$

hence is a surjection, hence a fibration in $SmoothAlg^\Delta_{proj}$ and therefore indeed a cofibration in $(SmoothAlg^\Delta_{proj})^{op}$.

Therefore using the [[Quillen bifunctor]] property of the coend over the tensoring in reverse to lemma \ref{CofibrantResolutionOfLinfinityAlgebroid} the above is equivalent to

$$
  \cdots 
  \simeq
  H^n N^\bullet
  \left(
    \int^{[k] \in \Delta} \Delta[k] \cdot \mathcal{O}(i(\mathfrak{a})_k)
  \right)
$$

with the [[fat simplex]] replaced again by the ordinary simplex. But in brackets this is now by definition the image under the [[monoidal Dold-Kan correspondence]] of the [[Chevalley-Eilenberg algebra]]

$$
  \cdots 
  \simeq
  H^n( N^\bullet \Xi CE(\mathfrak{a}) )
  \,.
$$

By the [[Dold-Kan correspondence]] we have hence

$$
  \cdots \simeq
  H^n(CE(\mathfrak{a}))
  \,.
$$

=--


## Examples

### Classes of examples

* a $\infty$-Lie algebroid over the [[point]], $\mathfrak{a} = *$ is an **[[L-∞-algebra]]**;

* an $n$-[[truncated]] $\infty$-Lie algebroid is a **Lie $n$-algebroid**;

* an $\infty$-Lie algebroid the differential of whose [[Chevalley-Eilenberg algebra]] is "co-binary", i.e. $d : \mathfrak{a}^* \to a^* \oplus a^* \wedge g^*$, is **strict**.

So in particular

* a 1-Lie algebroid is a **[[Lie algebroid]]**;

* a 1-Lie algebroid over the point is a **[[Lie algebra]]**;

* a Lie $n$-algebroid over a point is a **[[Lie n-algebra]]**.

* a _[[BRST-complex]]_ is the [[Chevalley-Eilenberg algebra]]
  of an action-$\infty$-Lie algebroid of the 
  [[action]] of an $L_\infty$-algebra, see [[Lie ∞-algebroid representation]];

  more generally, the complexes appearing in [[BV-BRST formalism]] are 
  derived $\infty$-Lie algebroids, whose Chevalley-Eilenberg algebra may have generators in negative degree.

* a [[symplectic Lie n-algebroid]] is a Lie $n$-algebroid equipped with a non-degrenerate bilinear [[invariant polynomial]] of degree $n+2$. For low $n$ this is

  * $n = 0$: a [[symplectic manifold]];

  * $n = 1$: a [[Poisson Lie algebroid]];

  * $n = 2$: a [[Courant algebroid]]


### Lie algebroids regarded as $\infty$-Lie algebroids
  {#LieAlgebroidsAsInfinLieAlgebroids}
We discuss the traditional notion of [[Lie algebroid]]s in view of their role as presentations for [infinitesimal synthetic differential 1-groupoids](#GeneralAbstractDefinition).


#### Smooth loci of infinitesimal simplices 
  {#SmoothLociOfInfinitesimalSimplices}

In this section we characterize ordinary [[Lie algebroid]]s $E \to T X$ as precisely those synthetic differential $\infty$-groupoids that under the [above presentation](#PresentationByCE) are locally on any [[chart]] $U \to X$ of their base space given by simplicial [[smooth loci]] of the form

$$
  \cdots
   \stackrel{\to}{\stackrel{\to}{\stackrel{\to}{\to}}}
   U \times \tilde D(rank E,2)\stackrel{\to}{\stackrel{\to}{\to}} U \times \tilde D(rank E,1) \stackrel{\to}{\to} U 
  \,,
$$

where $\tilde D(k,n)$ is the [[smooth locus]] of [[infinitesimal object|infinitesimal k-simplices]] based at the origin in $\mathbb{R}^n$. (These smooth loci have been considered in ([Kock, section 1.2](#Kock))).

The following definition may be either taken as an informal but instructive definition -- in which case the [next definition](#FunctionsOnTwiddleD) is to be taken as the precise one --  or in fact it may be already itself be taken as the fully formal and precise definition if one reads it in the [[internal logic]] of any [[smooth topos]] with line object $R$ -- which for the present purpose is the [[Cahiers topos]] with line object $\mathbb{R}$. (For an exposition of the latter perspective see ([Kock](#Kock))).

+-- {: .num_defn #FunctionsOnTwiddleD}
###### Definition


For $k,n \in \mathbb{N}$, an **infinitesimal $k$-[[simplex]]** in $R^n$ based at the origin is a collection $(\vec \epsilon_a \in R^n)_{a = 1}^k$ of points in $R^n$, such that each is an infinitesimal neighbour of the origin

$$
  \forall a : \;\; \vec \epsilon_a \sim 0
$$ 

and such that all are infinitesimal neighbours of each other

$$
  \forall a,a': \;\; (\vec \epsilon_a - \vec \epsilon_{a'}) \sim 0
  \,.
$$

Write $\tilde D(k,n) \subset R^{k \cdot n}$ for the space of all such infinitesimal $k$-simplices in $R^n$.

=--

Equivalently:

+-- {: .num_defn #FuntionsOnInfinitesimalSimplices}
###### Definition

For $k,n \in \mathbb{N}$, the [[smooth algebra]]

$$
  C^\infty(\tilde D(k,n)) \in SmoothAlg
$$ 

is the unique lift through the forgetful functor $U : SmoothAlg \to CAlg_{\mathbb{R}}$ of the commutative $\mathbb{R}$-algebra generated from $k \times n$ many generators 

$$
  (\epsilon_a^j)_{1 \leq j \leq n, 1 \leq a \leq k}
$$ 

subject to the relations

$$
  \forall a, j,j' : \;\; \epsilon_a^{j} \epsilon_a^{j'} = 0
$$

and

$$
  \forall a,a',j,j'   : 
   \;\;\; 
  (\epsilon_a^j - \epsilon_{a'}^j) (\epsilon_a^{j'} - \epsilon_{a'}^{j'}) = 0
  \,.
$$

=--


+-- {: .num_remark #InterpretationOfRelations}
###### Remark

In the above form these relations are the manifest analogs of the conditions $\vec \epsilon_a \sim 0$ and $(\vec \epsilon_a - \vec \epsilon_{a'}) \sim 0$.
But by multiplying out the latter set of relations and using the former, we find that jointly they are equivalent to the single set of relations

\[
  \forall a,a',j,j' : \;\;\;
  \epsilon_a^j \epsilon_{a'}^{j'} 
  + \epsilon_{a'}^j \epsilon_{a}^{j'} = 0
  \,.
\]

In this expression the roles of the two sets of indices is manifestly symmetric. Hence another equivalent way to state the relations is to say

$$
  \forall a,a', j: \;\;\;  \epsilon_a^{j} \epsilon_{a'}^j = 0
$$

and

$$
  \forall a,a',j,j : 
    \;\;\;
    (\epsilon_a^j - \epsilon_a^{j'})(\epsilon_{a'}^j - \epsilon_{a'}^{j'})
  = 0
$$

=--

This appears as ([Kock, (1.2.1)](#Kock)).


Since $C^\infty(\tilde D(k,n))$ is a [[infinitesimally thickened point|Weil algebra]] in the sense of [[synthetic differential geometry]], its structure as an $\mathbb{R}$-algebra extends uniquely to the structure of a [[smooth algebra]] (as discussed there) and we may think of $\tilde D(k,n)$ as an infinitesimal [[smooth locus]].

+-- {: .num_example #examplen2k2}
###### Example

For $n = 2$ and $k = 2$ we have that $C^\infty(\tilde D(2,2))$ consists of elements of the form

$$
  \begin{aligned}
    f
    +
    a \cdot \epsilon_1 
     + b \cdot \epsilon _2 
     + (\omega \cdot \epsilon_1) (\lambda \cdot \epsilon_2) 
    &= 
    f + 
    a_1 \epsilon_1^1 
     + a_2 \epsilon_1^2 
     + b_1 \epsilon_2^1 
     + b_2 \epsilon_1^2
    \\
    & + (\omega_1 \lambda_2 - \omega_2 \lambda_1) 
      \frac{1}{2}(\epsilon_1^1 \epsilon_2^2 - \epsilon_1^2 \epsilon_2^1)
  \end{aligned}
$$

for $f \in \mathbb{R}$ and $(a, b, \omega, \lambda \in (\mathbb{R}^n)^*)$ a collection of ordinary covectors and with "$\cdot$" denoting the evident contraction, and where in the last step we used the above relations.

It is noteworthy here that the coefficient of the term which is multilinear in each of the $\epsilon_i$ is the [[wedge product]] of two [[covector]]s $\omega$ and $\lambda$: we may naturally identify the subspace of $C^\infty(\tilde D(2,2))$ on those elements that vanish if either $\epsilon_1$ or $\epsilon_2$ are set to 0 as the space $\wedge^2 T_0^* \mathbb{R}^2$ of 2-forms at the origin of $\mathbb{R}^2$. 

Of course for this identification to be more than a coincidence we need that this is the beginning of a pattern that holds more generally. But this is indeed the case.

=--


Let $E$ be the set of _square_ submatrices of the $k \times n$-matrix $(\epsilon_i^j)$. As a set this is isomorphic to the set of pairs of subsets of the same size of $\{1, \cdots, k\}$ and $\{1, \cdots , n\}$, respectively. For instance the square submatrix labeled by $\{2,3,4\}$ and  $\{1,4,5\}$ is

$$
  e 
  =
  \left(
    \array{
       \epsilon_1^2 & \epsilon_4^2 & \epsilon_5^2
       \\
       \epsilon_1^3 & \epsilon_4^3 & \epsilon_5^3
       \\
       \epsilon_1^4 & \epsilon_4^4 & \epsilon_5^4
    }
  \right)
  \,.
$$


For $e \in E$ an $r\times r$ submatrix, we write 

$$
  det(e) = 
    \sum_{\sigma} sgn(\sigma) 
    \epsilon_{1}^{\sigma(1)} \epsilon_2^{\sigma(2)}
    \cdots 
    \epsilon_r^{\sigma(r)}
  \in
  C^\infty(\tilde D(k,n))
  \,.
$$ 

for the corresponding [[determinant]], given as a product of generators in $C^\infty(\tilde D(k,n))$. Here the sum runs over all [[permutation]]s $\sigma$ of $\{1, \cdots, r\}$ and $sgn(\sigma) \in \{+1, -1\} \subset \mathbb{R}$ is the [[signature]] of the permutation $\sigma$.


+-- {: .num_prop #FunctionsOnSimplicesByMatrices}
###### Proposition


The elements $f \in C^\infty(\tilde D(k,n))$ are precisely of the form

$$
  f = \sum_{e \in E} f_e \; det(e) 
$$

for _unique_ $\{f_e \in \mathbb{R} | e \in E\}$. In other words, the map of [[vector space]]s

$$
  \mathbb{R}^{|E|} \to C^\infty(\tilde D(k,n))
$$

given by 

$$
  (f_e)_{e \in E} \mapsto \sum_{e \in E} f_e det(e) 
$$ 

is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

This is a direct extension of the argument in the above example: a general product of $r$ generators in $C^\infty(\tilde D(k,n))$ is

$$
  \epsilon_{i_1}^{j_1} \epsilon_{i_2}^{j_2} 
   \cdots \epsilon_{i_r}^{j_r}
  \,.
$$

By the relations in $C^\infty(\tilde D(k,n))$, this is non-vanishing precisely if none of the $i$-indices repeats and none of the $j$-indices repeats. Furthermore by the relations, for any permutation $\sigma$ of $r$ elements, this is equal to

$$
  \cdots = sgn(\sigma) 
   \epsilon_{i_1}^{j_{\sigma(1)}} 
   \epsilon_{i_1}^{j_{\sigma(2)}}
   \cdots 
   \epsilon_{i_1}^{j_{\sigma(r)}}
  \,.
$$

It follows that each such element may be written as

$$
  \cdots = \frac{1}{r!} det(e)
  \,,
$$

where $e$ is the $r \times r$ sub-[[determinant]] given by the subset $\{i_1, \cdots, i_r\}$ and $(\{j_1, \cdots, j_r\})$ as discussed above.

=--


In ([Kock, section 1.3](#Kock)) effectively this proposition appears as the "[[Kock-Lawvere axiom]] scheme for $\tilde D(k,n)$" when $\tilde D(k,n)$ is regarded as an object of a suitable [[smooth topos]]. 


+-- {: .num_prop #TwiddleDsAsDOldKan}
###### Proposition

For any $k,n \in \mathbb{N}$ we have a natural [[isomorphism]] of real commutative and hence of [[smooth algebra]]s

$$
  \phi 
  : 
  C^\infty(\tilde D(k,n))
  \stackrel{\simeq}{\to}
  \oplus_{i = 0}^n (\wedge^i \mathbb{R}^k) \otimes (\wedge^i \mathbb{R}^n)
  \,,
$$

where on the right we have the algebras that appear degreewise in def. \ref{PresentationByMonoidalDoldKan}, where the product is given on homogeneous elements by

$$
  (\omega, x) \cdot (\lambda, y) = (\omega \wedge \lambda , x \wedge y)
  \,.
$$

=--

+-- {: .proof}
###### Proof


Let $\{t_a\}$ be the canonical basis for $\mathbb{R}^k$ and $\{e^i\}$ the canonical basis for $\mathbb{R}^n$. We claim that an isomorphism is given by the assignment

$$
  \phi : \epsilon^i_a \mapsto (t_a , e^i)
  \,.
$$

To see that this defines indeed an algebra homomorphism we need to check that it respects the relations on the generators. For this compute:

$$
  \begin{aligned}
    \phi(\epsilon_a^i \epsilon_{a'}^{i'})
    & =
   (t_a \wedge t_{a'}, e^i \wedge e^{i'})
    \\
    & = 
    -(t_{a'} \wedge t_{a}, e^i \wedge e^{i'})
    \\
    & = -\phi(\epsilon_{a'}^i \epsilon_{a}^{i'})
  \end{aligned}
  \,.
$$

The inverse clearly exists, given on generators by

$$
  \phi^{-1} : (t_a, e^i) \mapsto \epsilon_a^i
  \,.
$$


=--

+-- {: .num_cor #SimplicialSmoothLocusOfLieAlgebroid}
###### Corollary

For $\mathfrak{a} \in L_\infty Alg$ a 1-truncated object, hence an ordinary [[Lie algebroid]] of rank $k$ over a base manifold $X$, its image under the map $i : L_\infty Alg \to (SmoothAlg^\Delta)^{op}$, def. \ref{EmbeddingOfThePresentation}, is such that its restriction to any [[chart]] $U \to X$ is, up to [[isomorphism]], of the form

$$
  i(\mathfrak{a})|_U : [n] \mapsto U \times \tilde D(k,n)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{TwiddleDsAsDOldKan} in def. \ref{PresentationByMonoidalDoldKan}, using that by definition $CE(\mathfrak{a})$ is given by the exterior algebra on locally free $C^\infty(X)$ modules, so that

$$
  \begin{aligned}
    CE(\mathfrak{a}|_U) 
      & \simeq 
     (\wedge^\bullet_{C^\infty(U)} \Gamma(U\times \mathbb{R}^k)^*, d_{\mathfrak{a}|_U})
    \\
    & \simeq
     (C^\infty(U) \otimes \wedge^\bullet \mathbb{R}^k, d_{\mathfrak{a}|_U})
  \end{aligned}
  \,.
$$

=--


#### Tangent Lie algebroid 
  {#TangentLieAlgebroid}


For $X$ any [[smooth manifold]], there is a standard notion of the [[Lie algebroid]] which is the [[tangent Lie algebroid]] 

$$
  \mathfrak{a} = T X
$$

of $X$. We discuss this from the perspective of infinitesimal groupoids.


+-- {: .num_defn #InfinitesimalSingularSimplicialComplex}
###### Definition

For $U \in CartSp_{synthdiff}$, the [[infinitesimal singular simplicial complex]]
$X^{(\Delta^\bullet_{inf})}$ is the simplicial [[smooth locus]] which in terms  in degree $n$ is the space of $(k+1)$-tuples of pairwise infinitesimal neighbour points in $U$

$$
  U^{(\Delta^n_{inf})} = 
  \left\{
    x_{i_0}, \cdots x_{i_n} \in U | \forall r,s : x_{i_r} \sim x_{i_s}
  \right\}
$$

and whose face and degeneracy maps are as for the finite [[singular simplicial complex]].

More explicitly, in terms of the spaces from def. \ref{FunctionsOnTwiddleD} we may identify

$$
  U^{(\Delta^\bullet_{inf})}
  =
  \left(
    \cdots
    U \times \tilde D(dim U, 2)
    \stackrel{\to}{\stackrel{\to}{\to}}U \tilde \tilde D(dim U, 1)\stackrel{\to}{\to} U
  \right)
  \,,
$$

where in degree $n$ a [[generalized element]] $(x, (\vec \epsilon_a)_{a = 1, \cdots, dim U})$ of $U \times \tilde D(dim U, n)$ is thought of as a base point $x$ and $dim U$ infinitesimal paths starting at that basepoint

$$
  (x_0, \cdots, x_n) = ( x, x + \epsilon_1, \cdots, x + \epsilon_{dim U} )
  \,.
$$

The dual cosimplicial algebra is read off from this,

$$
  C^\infty(U^{(\Delta^\bullet_{inf})})
  = 
  \left(
    \cdots C^\infty(U \times \tilde D(dim U ,1)) \stackrel{\overset{d_0^*}{\leftarrow}}{\underset{d_1^*}{\leftarrow}} C^\infty(U)
  \right)
  \,.
$$

For instance for $f \in C^\infty(U)$ we have $d_1^* f = f $ and $(d_2^* f)(x,\epsilon_1) = f(x + \epsilon_1) = f(x) + \frac{\partial f}{\partial x^i} \epsilon^i_1$.


=--

+-- {: .num_not #InfinitesimalSingularNotAKanComplex}
###### Note

The object $X^{(\Delta^\bullet_{inf})}$ is not objectwise a [[Kan complex]]:
in general the composite of two first order neighbours produces a second order infinitesimal neighbour. Its [[Kan fibrant replacement]] may be thought of as the infinitesikmal $\infty$-groupoid whose morphisms are paths of a finite number of first order infinitesimal steps.

=--


+-- {: .num_prop #TangentLieAlgebroidAsSimplicialObject}
###### Proposition

The image of $T X$ under the embedding $i$ from def. \ref{EmbeddingOfThePresentation} is the [[simplicial object|simplicial]] [[smooth locus]] given by the [[infinitesimal singular simplicial complex]] 

$$
  T X = 
  \left(
      \cdots 
      X^{(\Delta^2_{inf})} 
        \stackrel{\to}{\stackrel{\to}{\to}} 
        X^{(\Delta^1_{inf})} 
       \stackrel{\to}{\to} X
  \right)
$$

of $X$. 

Moreover, the [intrinsic real cohomology](#Cohomology) of $i(T X) \in $ [[SynthDiff∞Grpd]] is the [[de Rham cohomology]] of $X$

$$
  H^n_{SynthDiff}(i (T X), \mathbb{R})
   \simeq
  H^n_{dR}(X)
$$

=--

+-- {: .proof}
###### Proof

The first statement may be checked locally on any [[chart]] $U \to X$ where it follows from prop. \ref{SimplicialSmoothLocusOfLieAlgebroid}. Since the [[Chevalley-Eilenberg algebra]] of the [[tangent Lie algebroid]] is the [[de Rham complex]] 

$$
  CE(T X) = (\Omega^\bullet(X), d_{dR})
$$

the second statement follows with prop. \ref{IntrinsicRealCohomologyByCECohomology}.

=--


#### Lie algebra 
  {#LieAlgebra}


Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$. We describe how $\mathfrak{g}$ looks when regarded as a special case of an $\infty$-Lie algebroid.

Write 

$$
  \mathbf{B}G =
  \left(
     \cdots G \times G 
     \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} * 
  \right)
$$

for the [[delooping]] [[groupoid]] of $G$, regarded as an an [[∞-Lie groupoid]] modeled by a simplicial [[smooth space]].

We claim that a morphism 

$$
  \omega : T U \to \mathbf{B}G
$$

from the tangent Lie algebroid of some $U \in $ [[CartSp]] is [[groupoid of Lie-algebra valued forms|flat Lie-algebra valued form]] and how that can be used to find the [[Lie algebra]] $\mathfrak{g}$ as the infinitesimal sub-$\infty$-groupoid

$$
  \mathbf{b}\mathfrak{g} \hookrightarrow \mathbf{B}G
$$

inside $\mathbf{B}G$.

Since $\mathbf{B}G$ is [[simplicial skeleton|2-coskeletal]] (being the [[nerve]] of a [[groupoid]]) a morphism $T U \to \mathbf{B}G$ is fixed already under its 2-[[truncated|truncation]]

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    G \times G
    \\
    \downarrow \downarrow \downarrow && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) &\stackrel{\omega_1}{\to}& G
    \\
    \downarrow \downarrow && \downarrow \downarrow
    \\
    U &\to& *
  }
  \,.
$$

It is clear that $\omega_1$ factors through the inclusion $\tilde D(1,dim(G)) \hookrightarrow G$ that sends the unique point of $\tilde D(1, dim(G))$ to the neutral element (by respect for the degeneracy maps).
Then from that one finds that $\omega_2$ factors through the inclusion $\tilde D(2, dim(G)) \hookrightarrow G \times G$ that sends the unique point of $\tilde D(2,dim(G))$ to $(e,e) \in G \times G$. And evidently these two factorizations are universal, in that every other factorization will uniquely factor through these

$$
  \array{
    U \times \tilde D(2,n) 
     &\stackrel{\omega_2}{\to}& 
    \tilde D(2,dim(G))
    &\hookrightarrow&
    G \times G
    \\
    \downarrow \downarrow \downarrow 
     && 
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    &&
    \downarrow^{p_2} \downarrow^{\cdot} \downarrow^{p_1} 
    \\
    U \times \tilde D(1,n) 
    &\stackrel{\omega_1}{\to}& 
    \tilde D(1, dim(G))
    &\hookrightarrow&
    G
    \\
    \downarrow \downarrow 
    && \downarrow \downarrow
    && \downarrow \downarrow
    \\
    U &\to& * &\to& *
  }
  \,.
$$

The universal object found this way we claim is the Lie algebra $\mathfrak{g}$ in its incarnation as an infinitesimal $\infty$-Lie groupoid

$$
  \begin{aligned}
    b \mathfrak{g}
    &:=
    InitialObject( T U\downarrow \mathbb{L}^{\Delta^{op}}\downarrow \mathbf{B}G)
    \\
    & =
    \left(
       \cdots
       \tilde D(2,dim(G))
       \stackrel{\to}{\stackrel{\to}{\to}}
     \tilde D(1,dim(G))\stackrel{\to}{\to} *
    \right)
  \end{aligned}  
  \,. 
$$

+-- {: .num_prop #CEAlgebraFromNormalizedCochains}
###### Proposition

The normalized cochain complex of the cosimplicial alghebra of functions on this $b \mathfrak{g}$ is isomorphic to the ordinary [[Chevalley-Eilenberg algebra]] $(\wedge^\bullet \mathfrak{g}^*, [-,-]^*)$ of $\mathfrak{g}$.

=--

+-- {: .proof}
###### Proof

By the [above discussion](#spring) we have that for $C^\infty(\tilde D(k,dim(G)))_{top} \subset C^\infty(\tilde D(k,n))$ the subspace of those functions that are in the joint kernel of the co-degeneracy maps is naturally isomorpic to $\wedge^k (\mathbb{R}^{dim(G)})^*$, so that we have a natural isomorphism of vector spaces

$$
  N C^\infty(b \mathfrak{g})_k \simeq \wedge^k \mathfrak{g}^*
  \,.
$$

By the fact that everything is [[simplicial skeleton|2-coskeletal]] it suffices to check that the differential in first degree

$$
  N C^\infty(\tilde D(1,dim(G)))
  \stackrel{p_1^* + p_2^* - (\cdot)^*}{\to}
  N C^\infty(\tilde D(2,dim(G)))
$$

is indeed the dual of the Lie bracket. But the product $\cdot_G : G \times G \to G$ restricted along $\tilde D(2,dim(G)) \hookrightarrow G \times G$ to the [[infinitesimal space]] $\tilde D(2, dim(G))$ linearizes in each of its arguments: for $(\vec x,\vec y) \in \tilde D(2,dim(G))$ we have

$$
  \vec x \cdot_G \vec y = 
  \vec x \cdot \nabla_x \cdot_G (0,0)
  + 
  \vec y \cdot \nabla_y \cdot_G (0,0)
  +
  \vec x \cdot \nabla_x 
  \vec y \cdot \nabla_y \cdot_G(0,0)
  \,.
$$

Since the origin here corresponds to the neutral element of $G$ and since with one of its arguments the neutral element the operaton $\cdot_G$ is the identity, and since the double derivative produces the Lie bracket (keeping in mind that $x^i y^j  + x^j y^i = 0$ in $\tilde D(2,dim(G))$), this is

$$
  \cdots = \vec x + \vec y + [\vec x, \vec y]
  \,.
$$

Accordingly the alternating sum of co-face maps is

$$
  \begin{aligned}
     d &= p_1^* + p_2^* - \cdot_G^* 
     \\ & = p_1^* + p_2^* - ( p_1^* + p_2^* + [-,-]^*)
     \\ & = - [-,-]^*
  \end{aligned}
$$

as it should be for the Chevalley-Eilenberg algebra of a Lie algebra.

=--

The infinitesimal reasoning involved in this proof is discussed in ([Kock, section 6.8](#Kock)).




## Related concepts

* [[Lie infinity-algebroid representation]]

* [[sheaf of L-∞ algebras]]

* [[∞-Lie algebroid cohomology]]

* [[∞-Lie algebroid valued differential forms]]

* [[∞-Chern-Weil theory]]

## References

The term "Lie $\infty$-algebroid" or "$L_\infty$-algebroid" as such is not as yet established in the literature, as most authors working with these objects think of them entirely in terms of [[dg-algebra]]s or [[NQ-supermanifolds]] and either ignore the relation to [[Lie theory]] or take it more or less for granted. 

Possibly the first explicit appearance of the idea of $\infty$-Lie algebroids recognized in their full [[Lie theory|Lie theoretic]] meaning is


* [[Pavol Severa]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080))

which uses "[[NQ-supermanifolds]]". Of course, as this article also points out, in hindsight one finds that much of this is already implicit in the much older theory of [[Sullivan model|Sullivan models]] in [[rational homotopy theory]], which is concerned with modelling _[[topological space]]s_ by [[dg-algebras]]. That these spaces can be regarded as [[∞-groupoids]] and as [[∞-Lie groupoids]] in particular is clear in hindsight, but was possibly first explicitly realized in the above reference. See also [[Lie integration]], [[rational homotopy theory in an (∞,1)-topos]] and [[function algebras on ∞-stacks]].

The explicit term _$\infty$-Lie algebroid_ / _$L_\infty$-algebroid_ as such is due to

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], Section A.1 of: _[[schreiber:Twisted Differential String and Fivebrane Structures]]_, Communications in Mathematical Physics, Volume 315, Issue 1 (2012) pp 169-213 ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001), [doi:10.1007/s00220-012-1510-3](https://link.springer.com/article/10.1007/s00220-012-1510-3))

The term then appears in

* Andrew James Bruce, _From $L_{\infty}$-algebroids to higher Schouten/Poisson structures_, Rept. Math. Phys. 67:157-177, 2011 ([arXiv:1007.1389](https://arxiv.org/abs/1007.1389), <a href="https://doi.org/10.1016/S0034-4877(11)00010-3">doi:10.1016/S0034-4877(11)00010-3</a>)

The dual monoidal Dold-Kan correspondence is discussed in

* {#CastiglioniCortinas} J. L. Castiglioni, G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ , J. Pure Appl. Algebra  191  (2004),  no. 1-2, 119--142, ([arXiv:math.KT/0306289](http://arxiv.org/abs/math/0306289))
.


The smooth spaces of infinitesimal simplices $\tilde D(k,n)$ are considered in section 1.2 of

* [[Anders Kock]],  _Synthetic differential geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))
{#Kock}


[[!redirects L-infinity-algebroid]]
[[!redirects L-infinity algebroid]]
[[!redirects L-infinity Lie algebroid]]

[[!redirects L-∞-algebroid]]
[[!redirects L-∞ algebroid]]
[[!redirects L-∞ Lie algebroid]]

[[!redirects L-∞-algebroids]]
[[!redirects L-∞ algebroids]]
[[!redirects L-∞ Lie algebroids]]


[[!redirects Lie-∞-algebroid]]
[[!redirects Lie-∞-algebroids]]
[[!redirects Lie-∞ algebroid]]
[[!redirects Lie-∞ algebroids]]
[[!redirects Lie ∞-algebroid]]
[[!redirects Lie ∞-algebroids]]
[[!redirects L-infinity-algebroids]]
[[!redirects L-infinity algebroids]]
[[!redirects L-infinity Lie algebroids]]

[[!redirects ∞-Lie algebroid]]
[[!redirects ∞-Lie algebroids]]

[[!redirects infinity-Lie algebroid]]
[[!redirects infinity-Lie algebroids]]

[[!redirects Lie n-algebroid]]
[[!redirects Lie n-algebroids]]

[[!redirects Lie-infinity algebroids]]

