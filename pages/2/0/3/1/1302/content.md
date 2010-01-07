
#Contents#

* automatic TOC goes here
{: toc}


## Idea {#Idea}

A quasicoherent sheaf is a [[sheaf]] of [[module]]s  over the [[structure sheaf]] of a [[space]] that is _locally presentable_ in that it is locally the [[cokernel]] of a morphism of [[free module]]s.

For comparison, recall that a [[vector bundle]] on a [[space]] may equivalently be encoded in terms of its [[sheaf]] of [[section]]s. This is a sheaf of [[module]]s over the [[structure sheaf]] $O$ of the space. But it is a very special such sheaf, notably locally free sheaf of $O$-modules of finite rank.

This extra condition makes the category of vector bundles too small to be closed under various natural operations like kernels, direct images and alike. In particular, it is not an [[abelian category]]. The category of all $O$-modules and specially its full subcategory of quasicoherent sheaves of $O$-modules are better in that respect. 

There are several different but equivalent ways to define and think about quasicoherent sheaves. 

A very concrete definition characterizes quasicoherent sheaves as those that are, while not locally free, locally the [[cokernel]] of a morphism of free module sheaves. This is the definition given in the section

* [As locally presentable modules](#LocPres)

below. It makes very manifest how passing from vector bundles to quasicoherent sheaves adds in the [[cokernel]]s that are missing in the category of [[vector bundle]]s.

But it turns out that there is a more abstract, more [[sheaf and topos theory|sheaf theoretic]] reformulation of this definition: if we think of the underlying [[space]] as a ([[presheaf|pre]])[[sheaf]] (as motivated at [[motivation for sheaves, cohomology and higher stacks]]) we find that a quasicoherent sheaf on a space is given by an assignment of a module to each plot, such that the pullback of these modules is given, up to coherent isomorphism, by tensoring over the corresponding rings. This is described in detail in the section

* [As sheaves over Aff/X](#AsSheaves).


The tensoring operation appearing here is that defining the pullback operations in the [[stack]] that classifies the canonical [[bifibration]] of [[module]]s over rings. In view of this, one finds that this definition, in turn, is equivalent to a very fundamental definition:

with $QC := (-)Mod : Ring \to Cat$ the functor that sends a ring to its category of modules, one finds that the category of quasicoherent sheaves on a [[space]] $X$ is simply the [[hom-object]]

$$
  QC(X) := Hom(X,QC)
$$

in the corresponding 2-category of category-valued (pre)sheaves, i.e (pre)[[stack]]s. This is the perspective described in [As hom objects](AsCocycles) below.

This definition, finally, provides a powerful [[nPOV]] on quasicoherent sheaves: all notions involved, sheaf, stack, morphism of stacks, have natural, immediate and well understood generalizations to [[higher category theory]]. Therefore this last definition immediately generalizes to a definition of quasicoherent $\infty$-sheaves or "derived" quasicoherent sheaves, such as they appear for instance in [[geometric ∞-function theory]]. This is discussed in the section 

* [Higher quasicoherent sheaves](#Higher).


## Definition

### As locally presentable modules {#LocPres}

Given a [[ringed space]] $(X,O_X)$ a __quasicoherent sheaf of $O_X$-modules__ is a sheaf $\mathcal{M}$ of $O_X$-modules such that there is a cover $\{U_\alpha\}_{\alpha\in A}$ of $X$ by open sets such that for every $\alpha$ there exist $I_\alpha$ and $J_\alpha$ and an exact sequence of sheaves of $O_X$-modules of the form
$$
O_X^{I_\alpha}|_{U_\alpha}\to
O_X^{J_\alpha}|_{U_\alpha}\to
\mathcal{M}|_{U_\alpha}\to 0,
$$
which should be viewed as a local presentation of $\mathcal{M}$. If $I_\alpha, J_\alpha$ can be chosen finite one talks about __coherent sheaves__ however the latter are ill-behaved for a general ringed space, and even general scheme; they behave well on Noetherian schemes. 

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

See also

* D. Orlov, _Quasi-coherent sheaves in commutative and non-commutative geometry_, Izv. RAN. Ser. Mat., 2003,  Volume 67,  Issue 3, Pages 119&#8211;138 (see also preprint version [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=57), [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=56))



### As homs into the stack of modules {#AsCocycles}

The above definition may be further re-interpreted as follows.

+-- {: .un_prop }
###### Proposition

On the [[site]] $Aff = CRing^{op}$, let 

$$
  QC : Ring \to Cat
$$

$$
  (Spec R_1 \stackrel{f}{\to} Spec R_2)
  \mapsto (R_1 Mod \stackrel{- \otimes_{f}}{\to} R_2 Mod)
$$

be the 
functor ([[stack]]) classifying the canonical [[bifibration]] of [[module]]s $Mod \to Ring$. Its right [[Kan extension]]
through the 2-Yoneda embedding 
$Y : Ring^{op} \hookrightarrow [Ring,Cat]$ is given on a 
presheaf $X : Ring \to Set$ by the [[hom-object]]

$$
  QC(X) := (Ran_Y QC)(X) := [Ring,Cat](X,QC)
  \,.
$$

When $X$ is the functor [[representable functor|represented]] by
a scheme, then $QC(X)$ is the category of quasicoherent sheaves on
$X$, as defined above.

=--

We now explain the above statement in detail and thereby prove it.


Let $C = $[[Ring]]${}^{op}$ be the category of (commutative, unital) [[ring]]s.
For $R$ a [[ring]] write $Spec R$ for it regarded as an object of $R^{op}$.
For $Spec f = f^{op} : Spec(R_2) \to Spec(R_1)$ a morphism in $Ring^{op}$ corresponding to the map $f : R_1 \to R_2$ of commutative rings.

Consider the [[2-category]] of (pre)[[stack]]s on 
$C$. The canonical [[module]] [[bifibration]] $p : Mod \to Ring$ of the category of modules over all rings is the bifibration whose fibered part corresponds to the (pre)stack $QC \in [C^{op},Cat]$ given on objects by 

$$
  QC : Spec R \mapsto R Mod
$$

and on morphisms by

$$
  QC : (Spec R_1 \stackrel{f}{\to} Spec R_2) \mapsto 
     R_1 Mod \stackrel{-\otimes_{f} R_2}{\to} R_2 Mod
  \,,
$$

where on the right we have the functor that sends any $R_1$-module $N$ to the 
[[tensor product]] over $R_1$ with the $R_1$-$R_2$-[[bimodule]] given by
$R_2$ with its canonical right $R_2$-action and with the left $R_1$-action
induced by the ring homomorphism $f$.

One may think of this as the stack of generalized algebraic vector bundles:

the operation $- \otimes_{f} R_2 : R_1 Mod \to R_2 Mod$ corresponds to the
[[pullback]] of [[bundle]]s along a morphism of the underlying spaces.
(See for instance 
the discussion of [[monadic descent]] at [[Sweedler coring]] for more on this.)
  
We may [[Kan extension|right Kan extend]] the 2-functor $QC : Ring^{op} \to Cat$
through the [[Yoneda embedding]] $Ring^{op} \hookrightarrow [Ring,Cat]$
to get a definition of $QC$ on arbitrary [[presheaf|presheaves]]. 

$$
  \array{
    Ring^{op} &\stackrel{QC}{\to}& Cat^{op}
    \\
    {}^{Y}\downarrow & \nearrow_{\mathrlap{Ran_Y QC}}
    \\
    [Ring,Cat]    
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
  \cdots = \int_{R \in Ring} [Ring,Cat](X(R), QC(R))
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
  
  in [[Cat]]. This unwraps to the following data:

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

This way, the transformation $N : X \to QC$ defines 
manifestly a quasicoherent sheaf on $Aff/X$ in the sense of the
definition in the above section [As sheaves on Aff/X](#AsSheaves). Conversely, every quasicoherent sheaf according to that definition gives rise to a transformation $N : X \to QC$ under this prescription.

The [[fibered category]] of $O_X$-modules can be replaced by a more general fibered category $\pi: \mathcal{F}\to\mathcal{B}$. Then the __category of quasicoherent modules in__ this __fibered category__ is the category opposite to the category of cartesian sections of $\pi$. This viewpoint is used by Rosenberg-Kontsevich in their preprint on noncommutative stacks ([dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305), [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333)).

Given a category $\mathrm{Aff}$ of affine schemes (opposite to the category of rings) equipped with some [[subcanonical coverage|subcanonical pretopology]] one considers the [[stack]] of $O$-modules over $\mathrm{Aff}$: the fiber over a ring $R$, it assigns the category $Qcoh(\mathrm{Spec}\,R)$. Now given any stack on a subcanonical site, one defines the fiber over a sheaf on it so that the fiber over a representable sheaf is equivalent to the fiber over its representing object. There is a canonical way to do this (will write later about it -- Zoran); this is in particular a source of a definition $Qcoh$ on an ind-scheme. On ind-schemes Beilinson and Drinfel'd in

* A. Beilinson, V. Drinfel'd, _Quantization of Hitchin's integrable system and Hecke eigensheaves on Hitchin system_, preliminary version ([pdf](http://www.math.uchicago.edu/~mitya/langlands/hitchin/BD-hitchin.pdf))

consider two variants: a less important variant of quasicoherent $O_X^p$-modules (existing in bigger generality) and more delicate variant of quasicoherent $O^!_X$-modules defined for "reasonable ind-schemes"; one of the differences is which functors play the role of pullbacks.  In particular, these notions apply for a rather general variant of the category of formal schemes.
  
  
### Quasicoherent modules in higher/derived context {#Higher}

The last definition has a  straightforward generalization to various [[higher category theory|higher categorical]] setups, such as [[derived scheme]]s and other [[generalized scheme]]s. 

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

for any [[(∞,1)-category]] [[site]] $C$ whatsoever, we have
the [[tangent (∞,1)-category]] fibration $T_C \to C$. With the [[(∞,1)-functor]] classifying it denoted 
$QC : C^{op} \to (\infty,1)Cat$ we may adopt for any 
[[∞-stack]] $X : C^{op} \to \infty Grpd$ the definition

$$
  QX(X) := [C^{op},\infty Grpd](X,QC)
$$

as a definition of generalized $\infty$-vector bundles on $X$. This is considered further at [[schreiber:∞-vector bundle]].





## Properties 

### Quasicoherent sheaves over affine schemes 

Given an affine scheme $X=\mathrm{Spec}\,R$ (where $R$ is a commutative unital ring), the affine Serre theorem establishes the equivalence of the category $Qcoh(\mathrm{Spec}\,R)$ of quasicoherent sheaves (in Zariski topology) and the category of $R$-modules. Similarly on a projective scheme of the type $Proj(A)$ where
$A$ is a nonnegatively graded ring, the (projective) Serre theorem establishes the equivalence of $Qcoh(\mathrm{Proj}\,(A))$ and 
the localization of the category of graded $A$-modules by the subcategory of modules of finite length (and similarly, of coherent sheaves and graded $A$-modules of finite type modulo finite-length). These theorems are among basic motivating theorems for [[noncommutative algebraic geometry]]. An interesting in-depth comparison of the notions of quasi-coherent sheaves in commutative and noncommutative context are also in the Orlov's article quoted above.

### The category of quasicoherent sheaves 

In the case of general (commutative) schemes, every presheaf of $O_X$-modules which is quasicoherent in the sense of having local presentation as above, is in fact a sheaf. It is known that the category of quasicoherent sheaves of $O_X$-modules over any [[quasicompact]] quasiseparated scheme is a [[Grothendieck category]] and in particular has enough [[injective object]]s.

[[!redirects quasicoherent sheaves]]
[[!redirects quasicoherent module]]
[[!redirects quasicoherent modules]]