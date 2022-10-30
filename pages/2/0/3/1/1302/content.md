
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}


## Idea {#Idea}

A _quasicoherent sheaf of modules_ (often just "quasicoherent sheaf", for short) is a [[sheaf of modules]]  over the [[structure sheaf]] of a [[ringed space]] that is _locally [[presentable module|presentable]]_ in that it is locally the [[cokernel]] of a morphism of [[free modules]].

For comparison, by the [[Serre-Swan theorem]] a [[vector bundle]] on a suitable [[ringed space]] is equivalently encoded in its [[sheaf]] of [[sections]] which is even locally [[free module|free]] and [[projective module|projective]]. In this sense quasicoherent sheaves of modules are a generalization of [[vector bundles]].
The [[category]] of vector bundles is too small to be closed under various natural operations like [[kernels]], [[direct images]] and alike. In particular, it is not an [[abelian category]]. The category of all $\mathcal{O}$-modules and especially its [[full subcategory]] of quasicoherent sheaves of $\mathcal{O}$-modules are better behaved in that respect.

There are several different but equivalent ways to define and think of quasicoherent sheaves. 

A very concrete definition characterizes quasicoherent sheaves as those that are, while not locally free, locally the [[cokernel]] of a morphism of free module sheaves. This is the definition given in the section

* [As locally presentable modules](#LocPres)

below. It makes very manifest how passing from vector bundles to quasicoherent sheaves adds in the [[cokernel]]s that are missing in the category of [[vector bundle]]s.

But it turns out that there is a more abstract, more [[sheaf and topos theory|sheaf theoretic]] reformulation of this definition: if we think of the underlying [[space]] as a ([[presheaf|pre]])[[sheaf]] (as motivated at [[motivation for sheaves, cohomology and higher stacks]]) we find that a quasicoherent sheaf on a space is given by an assignment of a module to each plot, such that the pullback of these modules is given, up to coherent isomorphism, by tensoring over the corresponding rings. This is described in the section

* [As sheaves over Aff/X](#AsSheaves).

and in more details in the section

* [Definition as sheaves over Aff](#AsSheavesII).

The tensoring operation appearing here is that defining the pullback operations in the [[stack]] that classifies the canonical [[bifibration]] $Mod \to CRing$ of [[module]]s over rings. In view of this, one finds that this definition, in turn, is equivalent to a very fundamental definition:

with $QC := (-)Mod : Ring \to Cat$ the functor that sends a ring to its category of modules, one finds that the category of quasicoherent sheaves on a [[space]] $X$ is simply the [[hom-object]]

$$
  QC(X) := Hom(X,QC)
$$

in the corresponding 2-category of category-valued (pre)sheaves, i.e (pre)[[stack]]s. This is the perspective described in 

* [As hom objects](#AsCocycles) 

below. By the equivalence between [[Grothendieck fibration]]s and [[pseudofunctor]]s this in turn is directly equivalent to the identification of $QC(X)$ with the category of cartesian functors between the [[category of elements]] of $X$ and $Mod$. This is described in 

* [As cartesian morphisms of fibered categories](#AsFibHoms)

This definition, finally, provides a powerful [[nPOV]] on quasicoherent sheaves: all notions involved, sheaf, stack, morphism of stacks, have natural, immediate and well understood generalizations to [[higher category theory]]. Therefore this last definition immediately generalizes to a definition of quasicoherent $\infty$-sheaves or "derived" quasicoherent sheaves, such as they appear for instance in [[geometric ∞-function theory]]. This is discussed in the section 

* [Higher quasicoherent sheaves](#Higher).


## Definition

### As locally presentable modules {#LocPres}

Let $(X,O_X)$ be a [[ringed space]] or, more generally, a [[ringed site]]. 

A __quasicoherent sheaf of $O_X$-modules__ on $X$ is a sheaf $\mathcal{E}$ of $O_X$-modules that is locally a [[cokernel]] of a [[morphism]] of [[free module]]s.

This means: there is a [[cover]] $\{U_\alpha\}_{\alpha\in A}$ of $X$ by open sets such that for every $\alpha$ there exist $I_\alpha$ and $J_\alpha$ (not necessarily finite) and an [[exact sequence]] of sheaves of $O_X$-modules of the form

$$
  O_X^{I_\alpha}|_{U_\alpha}
  \to
  O_X^{J_\alpha}|_{U_\alpha}
  \to
  \mathcal{E}|_{U_\alpha}\to 0,
$$

This should be viewed as a _local presentation_ of $\mathcal{E}$. 

If $I_\alpha, J_\alpha$ can be chosen finite and $\mathcal{E}$ is of finite type then the quasicoherent sheaf is a **[[coherent sheaf]]**. (See there for details.)
However , coherent sheaves are ill-behaved for a general ringed space, and even general [[scheme]]s; they behave well on [[Noetherian scheme]]s. 

Replacing covers by open sets, by covers of a terminal object in a site, the definition extends to [[ringed site]]s with a terminal object; the restrictions of $O_X$-modules should be replaced by pullbacks.
There are generalizations for [[algebraic stack]]s, ind-schemes, diagrams of schemes (for example [configuration schemes](http://arxiv.org/abs/math/0012061) of V. Lunts, obtained by gluing along closed embeddings of schemes; simplicial schemes) and so on. 




### As sheaves on $Aff/X$ {#AsSheaves}

There is an equivalent reformulation of the above in terms of [[sheaf|sheaves]] of $\mathcal{O}$-modules on the [[site]] $Aff/X$ of [[affine scheme]]s over $X$.

This is the [[over category]] whose objects are morphism (of [[scheme]]s) of the form $Spec A \to X$ and whose morphisms are commuting triangles

$$
  \array{
    Spec A &&\stackrel{f}{\to}&& Spec B
    \\
    & {}_a\searrow && \swarrow_b
    \\
    && X
  }
  \,.
$$

Then: a quasicoherent sheaf on $(X, \mathcal{O}_X)$ is a [[sheaf]] $N$ of $\mathcal{O}_X$-[[module]]s on $Aff/X$  such that for each morphism $f$ as above the restriction morphism

$$
  N(f) : N(b) \to N(a)
$$

extends to an [[isomorphism]]

$$
  N(b) \otimes_{f^*} A \stackrel{\simeq}{\to} N(a)
$$

of $A$-[[module]]s.

For a very explicit statement of this see for instance [page 13](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.5130v1.pdf#page=13) of 

* [[Paul Goerss]], _Topological modular forms (aftern Hopkins, Miller, and Lurie)_ ([arXiv](http://arxiv.org/abs/0910.5130))

See also a very precise and detailed treatment in 

* [[Dmitri Orlov]], _Quasi-coherent sheaves in commutative and non-commutative geometry_, Izv. RAN. Ser. Mat., 2003,  Volume 67,  Issue 3, Pages 119&#8211;138 (see also preprint version [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=57), [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=56))


###Direct definition for presheaves of sets on Aff {#AsSheavesII} 

Here is a more detailed way to say again what the above paragraph said.

Let $Aff = CRing^{op}$; recall the fibered category $Mod\to CRing^{op}$ where for each $f:A\to B$ in $CRing$ the inverse image functor is $f^*=B\otimes_A - :{}_A Mod\to {}_B Mod$. Then the identity functor $CRing\to CRing$ can be interpreted as the presheaf of rings and is denoted by $O$ (the "structure sheaf"). An $O$-module is a presheaf of $O$-modules. Usually some Grothendieck topology is given and one asks for sheaves in fact. We can Yoneda extend $O$-modules to presheaves. We now define quasicoherent sheaves of $O$-modules on an arbitrary presheaf $X$ on $Aff$, viewed as a covariant functor on $CRing$. 

A **quasicoherent sheaf of $O$-modules** on $X$ is a rule assigning to any $\phi\in X(A)$ an $A$-module $M_\phi = M_{A,\phi}$ and to any morphism $f:A\to B$ in $CRing$ an isomorphism $\theta_{f,\phi}:f^*(M_\phi)\to M_{X(f)(\phi)}$ such that for any [[composable pair]] $A\stackrel{f}\to B\stackrel{g}\to C$ and any $\phi\in X(A)$ the cocycle condition 

$$
\theta_{g\circ f,\phi}\circ \alpha_{fg} = \theta_{g,X(f)(\phi)}\circ g^*(\theta_{f,\phi})\colon g^* f^*(M_\phi)\to M_{X(g\circ f)(\phi)}
$$

holds, where $\alpha_{fg}:g^* f^*(M_\phi)\to (g\circ f)^*(M_\phi)$ is the canonical isomorphism which is part of the data of the (covariant) pseudofunctor $A\to {}_A Mod$, $f\mapsto f^*$.

Notice that if $X = h^C = h_{Spec C}$ is (co)representable presheaf, then $\phi\in [A,X]_{Pshv(Aff)}=[C,A]_{CRing}$ is the same as a morphism $\phi^{op}:C\to A$ of rings; restricting the quasicoherent sheaf to $Spec A$ along $\phi:Spec A\to X$ and taking the global sections over $A$, would give the $A$-module $M_\phi$.

Clearly, $Aff$ and $O$ can be much generalized. For example, rings may be noncommutative or one can take category opposite to the category of monads in $Set$ and an arbitrary (not identity) presheaf $D$ of monads in $Set$; the extension of scalars for monads gives an inverse image functor for Eilenberg-Moore categories. Durov's construction of quasicoherent sheaves for monads in $Set$ is an example where commutative algebraic monads are used; the theory of quasicoherent sheaves of $D$-modules ("$O$-modules with integrable connection") is another. Instead setups involving operads, higher operads and alike can be used as well; commutativity condition is useful if one wants a monoidal category of quasicoherent sheaves.

### As homs into the stack of modules {#AsCocycles}

The above definition may be further re-interpreted as follows.

+-- {: .un_prop }
###### Proposition

On the [[site]] $Aff = CRing^{op}$, let 

$$
  QC : CRing \to Cat
$$

$$
  (Spec S_ \stackrel{f^{op}}{\to} Spec R)
  \mapsto (R Mod \stackrel{S \otimes_{f} -}{\to} S Mod)
$$

be the (pseudo)functor ([[stack]]) corresponding to the canonical [[Grothendieck fibration]] of [[module]]s $Mod \to CRing$. Its right [[Kan extension]] through the 2-[[Yoneda embedding]]  $Y : CRing^{op} \hookrightarrow [CRing,Cat]$ is given on a presheaf $X : CRing \to Set$ by the [[hom-object]]

$$
  QC(X) := (Ran_Y QC)(X) := [CRing,Cat](X,QC)
  \,.
$$

When $X$ is the functor [[representable functor|represented]] by
a scheme, then $QC(X)$ is the category of quasicoherent sheaves on
$X$, as defined above.

=--

We now explain the above statement in detail and thereby prove it.

Let $C = $[[Ring]]${}^{op}$ be the category of (commutative, unital) [[ring]]s.
For $R$ a [[ring]] write $Spec R$ for it regarded as an object of $C$.
Write $Spec f = f^{op} : Spec(S) \to Spec(R)$ for the morphism in $Ring^{op}$ corresponding to the map $f : R \to S$ of commutative rings.

Consider the [[2-category]] of (pre)[[stack]]s on 
$C$. The canonical [[module]] [[bifibration]] $p : Mod \to Ring$ of the category of modules over all rings is the bifibration whose fibered part corresponds to the (pre)stack $QC \in [C^{op},Cat]$ given on objects by 

$$
  QC : Spec R \mapsto R Mod
$$

and on morphisms by

$$
  QC : (Spec S \stackrel{f}{\to} Spec R) 
         \mapsto 
       (R Mod \stackrel{S\otimes_{f} }{\to} S Mod)
  \,,
$$

where on the right we have the functor that sends any $R$-module $N$ to the 
[[tensor product]] over $S$ with the $R$-$S$-[[bimodule]]
$S = {}_S S_R$ with its canonical left $S$-action and with the right $R$-action induced by the ring homomorphism $f$.

One may think of this as the stack of generalized algebraic vector bundles:

the operation $S \otimes_{f} - : R Mod \to S Mod$ corresponds to the
[[pullback]] of [[bundle]]s along a morphism of the underlying spaces.
(See for instance the discussion of [[monadic descent]] at [[Sweedler coring]] for more on this.)
  
We may [[Kan extension|right Kan extend]] the 2-functor $QC : CRing^{op} \to Cat$ through the [[Yoneda embedding]] $Ring^{op} \hookrightarrow [CRing,Cat]$
to get a definition of $QC$ on arbitrary [[presheaf|presheaves]]. 

$$
  \array{
    CRing^{op} &\stackrel{QC}{\to}& Cat^{op}
    \\
    {}^{Y}\downarrow & \nearrow_{\mathrlap{Ran_Y QC}}
    \\
    [CRing,Cat]    
  }
  \,.
$$

Consider $X \in [C^{op},Set]$ any ([[presheaf|pre]])[[sheaf]] on $C$.
This may be the presheaf [[representable functor|represented]]
by a [[scheme]], but for the purposes of the definition of $QC$ it may be much more generally any presheaf.

By the general formula for [[Kan extension]] in terms of a [[weighted limit]] given by an [[end]]
we have

$$
  Ran_Y QC : X \mapsto \int_{R \in Ring} ([Ring,Cat]^{op}(X,Y(R)))^{QC(R)}
$$

which using the [[Yoneda lemma]] is

$$
  \cdots = \int_{R \in CRing} [CRing,Cat](X(R), QC(R))
  \,.
$$

This is the [[end]]-formula for the [[hom-object]] in an [[enriched functor category]]
$[C^{op},Cat]$,
hence this is nothing but the category of (pseudo)[[natural transformation]]s between
the 2-functor $X$ and the 2-functor $QC$.

We write for short

$$
  QC(X) := (Ran_Y QC)(X) := [C^{op},Cat](X,QC)
  \,.
$$

This definition of "generalized vector bundles" on arbitrary presheaves is
entirely analogous to the definition of differential forms on arbitrary
presheaves, that is discussed in some detail for instance in the entry on
[[rational homotopy theory]].

We claim that the category $QC(X)$ is the category of quasicoherent sheaves on
$X$ as defined by other means above, whenever that other definition applies to $X$.

To see this, straightforwardly unwrap the definition: 
an object $N$ in $QC(X) = [C^{op},Cat](X,QC)$
is a [[transfor|pseudonatural transformation]] of 2-functors $N : X \to QC$,
where $X$ is regarded as a 2-functor by the canonical embedding 
$disc : Set \hookrightarrow Cat$ that regards a [[set]] as a [[discrete category]].

The components of $N$ are

* for each $Spec R \in Ring^{op}$ a [[functor]] $N|_{Spec R} : X(R) \to QC(R) = R Mod$:

  this functor picks one $R$-module $N(r) \in R Mod$ for each plot $(r : Spec R \to X) \in X(Spec R)$;
  
* for each morphism $f : Spec A \to Spec B$ 
  a pseudonaturality square

  $$
    \array{
      X(Spec B) 
         &\stackrel{X(f)}{\to}& 
      X(Spec A)
      \\
      {}^{\mathllap{N|_{Spec B}}}\downarrow 
      &{}^{\Gamma(f)}\swArrow_{\simeq}& 
      \downarrow^{\mathrlap{N|_{Spec A}}}
      \\
      B Mod &\underset{- \otimes_{f^*} A}{\to}& A Mod
    }
  $$
  
  in [[Cat]] (these are subject to coherence conditions). This unwraps to the following data:

  * the component functors $N|_{Spec A}$ provide an
    assignment $a \mapsto N(a)$ of modules $N(a)$ to each 
    plot $(a : Spec A \to X) \in X(Spec A)$;

  * these assignments form a presheaf on the [[overcategory]] 
    $Aff/X$ by taking the restriction morphism
    
    $$
      N(f) : N(b) \to N(a)
    $$

    to be that underlying the components of the 
    natural isomorphism in the above diagram

    $$
      N(b)\otimes_{f^*} A \stackrel{\simeq}{\to} N(a)
      \,,
    $$

    i.e. the restriction of this morphism to $(n,1)$.

* for each tuple of composable morphisms 

  $$
    \array{
      && Spec B
      \\
      & {}^f\nearrow && \searrow^g
      \\
      Spec A &&\to&& Spec C
    }
  $$

  a pseudo-naturality prism equation relating, $N(f)$, $N(g)$ and $N(g\circ g)$.  The present author is too lazy to write out the diagram in detail, but it is of precisely the kind described in great detail for instance in the entry on [[group cohomology]]. Under the above identification, this yields the cocycle condition mentioned  in the above definitions.

This way, the transformation $N : X \to QC$ defines 
manifestly a quasicoherent sheaf on $Aff/X$ in the sense of the
definition in the above section [As sheaves on Aff/X](#AsSheaves). Conversely, every quasicoherent sheaf according to that definition gives rise to a transformation $N : X \to QC$ under this prescription.



### As cartesian morphisms of fibrations {#AsFibHoms}

By the equivalence between [[pseudofunctor]]s $Ring \to Cat$
and [[Grothendieck fibration]]s $F \to Ring^{op}$ induced by the
[[Grothendieck construction]], the above may equivalently be
reformulated as follows.


Recall from the discussion at [[Grothendieck fibration]] that the equivalence in question is between the following two [[bicategory|bicategories]]:

* on the one hand the bicategory whose objects are [[pseudofunctors]]
  $Ring \to Cat$, whose morphisms are pseudonatural 
  transformations, and whose 2-morphisms are modifications of these

* on the other hand the bicategory whose objects are [[Grothendieck fibration]]s $F \to Ring^{op}$, whose morphism are **cartesian functors**

  $$
    \array{
      F_1 &&\to&& F_2
      \\
      & \searrow && \swarrow
      \\
      && Ring^{op}
    }
  $$

  and whose 2-morphisms are [[natural transformation]]s between these.  

Recall furthermore that for $X : Ring \to Cat$ an ordinary [[presheaf]], i.e. a pseudofunctor that factors through an ordinary functor $Ring \to Set$ via the inclusion $Set \to Cat$, the [[Grothendieck fibration]] associated with $X$ is the [[category of elements]] $Ring^{op}/X$ of $X$.

Recall furthermore that by definition, the pseudofunctor $QC : Ring Cat$ is the one corresponding to the [[Grothendieck fibration]] $Mod^{op} \to Ring^{op}$.

Therefore, by the above equivalence of 2-categories, we find that the category of functors $[Ring,Cat](X,QC)$ is equivalent to the category of cartesian functors over $Ring^{Op}$, $CartFunc_E(Ring^{op}/X,Mod^{op})$

$$
  QC(X) \simeq [Ring,Cat](X,QX) \simeq CartFunc(Ring^{op}/X, Mod^{op})
  \,.
$$

In this form quasicoherent sheaves on $X$ are conceived for instance in paragraph 1.1.5 of

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative stacks_ ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333))


Here, as in the above discussion, the [[fibered category]] of modules can be replaced by a more general fibered category $\pi: \mathcal{F}\to\mathcal{B}$. Then the __category of quasicoherent modules in__ this __fibered category__ is the category opposite to the category of cartesian sections of $\pi$. This viewpoint is used by Rosenberg-Kontsevich in their preprint on noncommutative stacks ([dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305), [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333)).

Given a category $\mathrm{Aff}$ of affine schemes (opposite to the category of rings) equipped with some [[subcanonical coverage|subcanonical pretopology]] one considers the [[stack]] of $O$-modules over $\mathrm{Aff}$: the fiber over a ring $R$, it assigns the category $Qcoh(\mathrm{Spec}\,R)$. Now given any stack on a subcanonical site, one defines the fiber over a sheaf on it so that the fiber over a representable sheaf is equivalent to the fiber over its representing object. There is a canonical way to do this (will write later about it -- Zoran); this is in particular a source of a definition $Qcoh$ on an ind-scheme. On ind-schemes Beilinson and Drinfel'd in

* A. Beilinson, V. Drinfel'd, _Quantization of Hitchin's integrable system and Hecke eigensheaves on Hitchin system_, preliminary version ([pdf](http://www.math.uchicago.edu/~mitya/langlands/hitchin/BD-hitchin.pdf))

consider two variants: a less important variant of quasicoherent $O_X^p$-modules (existing in bigger generality) and more delicate variant of quasicoherent $O^!_X$-modules defined for "reasonable ind-schemes"; one of the differences is which functors play the role of pullbacks.  In particular, these notions apply for a rather general variant of the category of formal schemes.
  
  
### Quasicoherent modules in higher/derived geometry
 {#Higher}


The last definition has a  straightforward generalization to various [[higher geometry]] setups, such as [[derived schemes]] and other [[generalized schemes]]. 

#### By maps into the stack $QCoh$

For instance the notion of
quasicoherent sheaves generalized to [[derived stack]]s on the
site of [[simplicial ring]]s as described at
[[geometric ∞-function theory]] is obtained, we claim, 
simply by taking 
$QC : SRing \to (\infty,1)Cat$ to be the functor that assigns the
[[(∞,1)-category]] for modules over a simplicial ring to any
simplicial ring, and then setting for any derived stack $X$

$$
  QC(X) := Hom(X,QC)
  \,.
$$

Moreover, using the theorem described at [[tangent (∞,1)-category]],
that the [[bifibration]] of modules over simplicial rings is nothing
but the [[tangent (∞,1)-category]] of $SRing$, one sees that 
all this is a special case of an even much more general abstract nonsense:

for any presentable [[(∞,1)-category]] [[site]] $C$ whatsoever, we have
the [[tangent (∞,1)-category]] fibration $T_C \to C$. With the [[(∞,1)-functor]] classifying it denoted 
$QC : C^{op} \to (\infty,1)Cat$ we may adopt for any 
[[∞-stack]] $X : C^{op} \to \infty Grpd$ the definition

$$
  QX(X) := [C^{op},\infty Grpd](X,QC)
$$

as a definition of generalized $\infty$-vector bundles on $X$. This general nonsense is considered further at [[schreiber:∞-vector bundle]]. Concrete realizations are discussed at [[quasicoherent ∞-stack]].


#### As lifts of the structure sheaf

In ([LurieQC, section 2.2, section 2.3](#LurieQC)) the following definition is given.

Let $\mathcal{G}$ be a [[geometry (for structured (∞,1)-toposes)]]. Let 

$$
  \mathcal{G}^{mod} \coloneqq T {\mathcal{G}^{op}}^{op}
$$ 

be the opposite [[tangent (∞,1)-category]] of its [[opposite (∞,1)-category]]. 

For instance for [[E-∞ geometry]] we have $\mathcal{G} = CRing_\infty$ is the [[(∞,1)-category]] of [[E-∞ rings]] with [[etale morphisms]] as admissible maps.

Then the canonical  [[(∞,1)-functor]]

$$
  \mathcal{G}^{mod} \longrightarrow \mathcal{G}
$$

is a morphism of discrete [[geometry (for structured (∞,1)-toposes)|geometries]].

For $\mathcal{X}$ an [[(∞,1)-topos]], a [[left exact (∞,1)-functor]]

$$
  \mathcal{O} \colon \mathcal{G} \longrightarrow \mathcal{X}
$$

constitutes a $\mathcal{G}$-[[structure sheaf]] and makes $(\mathcal{X}, \mathcal{O})$ be a $\mathcal{G}$-[[structured (∞,1)-topos]]. A left exact extension of this

$$
  \array{
     \mathcal{G}^{mod}
     \\
     \downarrow & \searrow^{\mathrlap{(\mathcal{O}, \mathcal{F})}}
     \\
     \mathcal{X} 
     &\stackrel{\mathcal{O}}{\longrightarrow}& \mathcal{G}
  }
$$

exhibits a sheaf $\mathcal{F}$ of [[modules]] over $\mathcal{O}$.

([LurieQC, notation 2.2.4](#LurieQC))


now

([LurieQC, def. 2.3.6](#LurieQC))

(...)







## Properties 

### Quasicoherent sheaves over affine schemes 

Given an affine scheme $X=\mathrm{Spec}\,R$ (where $R$ is a commutative unital ring), the affine Serre theorem establishes the equivalence of the category $Qcoh(\mathrm{Spec}\,R)$ of quasicoherent sheaves (in Zariski topology) and the category of $R$-modules. Similarly on a projective scheme of the type $Proj(A)$ where
$A$ is a nonnegatively graded ring, the (projective) Serre theorem establishes the equivalence of $Qcoh(\mathrm{Proj}\,(A))$ and 
the localization of the category of graded $A$-modules by the subcategory of modules of finite length (and similarly, of coherent sheaves and graded $A$-modules of finite type modulo finite-length). These theorems are among basic motivating theorems for [[noncommutative algebraic geometry]]. An interesting in-depth comparison of the notions of quasi-coherent sheaves in commutative and noncommutative context are also in the Orlov's article quoted above.

### The category of quasicoherent sheaves 

In the case of general (commutative) schemes, every presheaf of $O_X$-modules which is quasicoherent in the sense of having local presentation as above, is in fact a sheaf. It is known that the category of quasicoherent sheaves of $O_X$-modules over any [[quasicompact]] quasiseparated scheme is a [[Grothendieck category]] and in particular has enough [[injective object]]s.

## Related concepts

### General

* [[coherent sheaf]]

* [[Bondal-Orlov reconstruction theorem]]

### D-Modules

The category of [[D-module]]s on a [[space]] $X$ is equivalently that of quasicoherent sheaves on the corresponding [[deRham space]].


## References

Quasicoherent sheaves in [[E-∞ geometry]] (on "[[Spectral Schemes]]" over [[E-∞ rings]]) are discussed in 

* [[Jacob Lurie]], _[[Quasi-Coherent Sheaves and Tannaka Duality Theorems]]_
 {#LurieQC}

Their [[descent]] properties are discussed in

* [[Jacob Lurie]], _[[Descent Theorems]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XI.pdf))

and a [[Grothendieck existence theorem]] for [[coherent sheaves]] in this higher context is discussed in 

* [[Jacob Lurie]], _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XII.pdf))

category: algebraic geometry

[[!redirects quasicoherent sheaves]]
[[!redirects quasicoherent module]]
[[!redirects quasicoherent modules]]
[[!redirects quasi-coherent sheaves]]
[[!redirects quasi-coherent module]]
[[!redirects quasi-coherent modules]]
[[!redirects quasi-coherent sheaf]]
[[!redirects quasicoherent sheaf of modules]]
[[!redirects quasicoherent sheaves of modules]]