
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

* **$\infty$-Lie algebra cohomology**

* [[Chevalley-Eilenberg algebra]]

* [[Weil algebra]]

* [[invariant polynomial]]


***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _$\infty$-Lie algebra cohomology_ generalizes the notion of [[Lie algebra cohomology]] from [[Lie algebra]]s to [[∞-Lie algebra]]s.

## Definition

If an [[(∞,1)-topos]] $\mathbf{H}$ admits [[rational homotopy theory in an (∞,1)-topos]] in that we have a [[reflective sub-(∞,1)-category]]

$$
  \mathbf{L} \stackrel{\leftarrow}{\hookrightarrow}
  \mathbf{H}
$$

obtained as the [[localization of an (∞,1)-category|localization]] of $\mathbf{H}$ at morphisms that induces [[isomorphism]]s in [[cohomology]] with coefficients in some line object $k$, we may think of $\mathbf{L}$ as the [[(∞,1)-category]] of all [[∞-Lie algebroid]]s inside the "[[∞-Lie groupoid]]s" wich are the objects of $\mathbf{H}$.

An [[∞-Lie algebra]] $\mathfrak{g}$ is a [[connected]] object in $\mathbf{L}$ and **$\infty$-Lie algebra cohomology** is the [[cohomology|intrinsic cohomology]] of $\mathbf{H}$ restricted to $\mathbf{L}$.

Typically $\mathbf{L}$ is [[presentable (∞,1)-category|presented]] by the [[opposite category|opposite]] of a [[function algebras on ∞-stacks|model structure on cosimplicial/cochain algebras]]: the [[Chevalley-Eilenberg algebra]]s of the given [[∞-Lie algebroid]]s. In terms of that model cocycle in $\infty$-Lie algebra cohomology have explicit and familiar algebraic expressions. These we discuss in 

* [Explicit definition](#ExplicitDefinition) .

A discussion of details of how exactly this models the general abstract definition is in

* [(∞,1)-Topos theoretic interpretation](#Topos).


### Explicit definition {#ExplicitDefinition}

For $\mathfrak{g}$ an [[∞-Lie algebra]] and $n \in \mathbb{N}$, a [[cocycle]] on $\mathfrak{g}$ in degree $n$ with coefficients in the trivial module is a morphism

$$
  \mu : \mathfrak{g} \to b^{n-1}\mathbb{R}
  \,.
$$

Dually this is a [[dg-algebra]] morphism

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{n-1}\mathbb{R}) : \mu
$$

of [[Chevalley-Eilenberg algebra]]s. here $CE(b^{n-1} \mathbb{R})$ is the [[semifree dga]] on a single generator in degree $n$ with vanishing differential. So this is equivalently an element

$$
  \mu \in \wedge^n \mathfrak{g}^*
$$

which is closed in $CE(\mathfrak{g})$. For $\mathfrak{g}$ an ordinary Lie algebra, this latter description reproduces the traditional definition of cocycles in [[Lie algebra cohomology]].

For the moment see

* [[Chevalley-Eilenberg algebra]]

* [[Weil algebra]]

* [[invariant polynomial]]

for more.

### $(\infty,1)$-topos theoretic interpretation {#Topos}

We may understand the above definitions of $\infty$-Lie algebra cocycles as a special case of the general notion of the [[cohomology|intrinsic cohomology]] of an [[(∞,1)-topos]] by embedding $\infty$-Lie algebras as [[infinitesimal space|infinitesimal]] [[∞-Lie group]]s into the [[(∞,1)-topos]] $\mathbf{H} = $ [[?LieGrpd]] of [[∞-Lie groupoid]]s.

Recall from [[function algebras on ∞-stacks]] that [[∞-Lie algebroid]]s form the [[reflective sub-(∞,1)-category]] 

$$
  \mathbf{L}
  \stackrel{\leftarrow}{\hookrightarrow}
  \mathbf{H}
$$

of a corresponding [[(∞,1)-topos]] $\mathbf{H}$ of structure $\infty$-groupoids.

As described at [[?LieGrpd]], one realization of this general situation for genuine $\infty$-Lie groupoids is as follows:

Let [[ThCartSp]] be the [[site]] of [[infinitesimal object|infinitesimally]] thickened [[Cartesian space]]s. This is the site for the [[Cahiers topos]]. Then the [[(∞,1)-category of (∞,1)-sheaves]] $\mathbf{H} = Sh(ThCartSp)$ we may take to be the $(\infty,1)$-topos of synthetics $\infty$-Lie groupoids. We have then a [[simplicial Quillen adjunction]]

$$
  (C^\infty Alg^{\Delta})^{op} \stackrel{\leftarrow}{\hookrightarrow}
  [ThCartSp^{op}, sSet]_{proj,loc}
$$

between the [[opposite category|opposite]] of the [[function algebras on ∞-stacks|model structure on cosimplicial smooth algebras]]. This models the reflective inclusion of [[∞-Lie algebroid]]s into all synthetic differential $\infty$-groupoids

$$
  \infty LieAlg stackrel{\leftarrow}{\hookrightarrow}
  \infty SDGrpd
  \,.
$$

Details on this are at [[function algebras on ∞-stacks]]. But the [[function algebras on ∞-stacks|model structure on cosimplicial smooth algebras]]s is the [[transferred model structure]] of the [[model structure on cosimplicial rings]], and for the following discussion we can essentially just as well use the analogous Quillen adjunction without the smooth structure originally considered by [[Bertrand Toen]]

$$
  (CAlg^\Delta)^{op} \stackrel{\leftarrow}{\hookrightarrow}
  [CAlg,sSet]_{proj,cov}
$$

that is referenced and reviewed in some detail at [[rational homotopy theory in an (∞,1)-topos]].

Notice that the embedding map is just degreewise the [[Yoneda embedding]].

Notice moreover that by the [[monoidal Dold-Kan correspondence]] (see there for details) we have that the dual Dold-Kan functor $\Xi : Ch^\bullet_+ \to Ab^\Delta$ extends to the right adjoint part in a [[Quillen equivalence]] between the opposite of the [[model structure on dg-algebras]] and the opposite [[model structure on cosimplicial rings|model structure on cosimplicial algebras]]

$$
  \Xi^{op} : dgAlg^{op} \stackrel{\simeq_{Quillen}}{\to}
   (CAlg^\Delta)^{op}
  \,.
$$

In total this gives a right Quillen functor

$$
  R : 
  dgAlg^{op} \stackrel{\Xi^{op}}{\to} (CAlg^\Delta)^{op}
  \to
  [CAlg, sSet]_{proj,cov}
$$


that models the embedding of $\infty$-Lie algebroids into a [[(∞,1)-topos]] of $\infty$-Lie groupoids. When restricted to [[∞-Lie algebra]]s ($\infty$-Lie algebroids over the point) the difference between the sites $CAlg^{op}$ and [[ThCartSp]] plays no role. In fact for that case we could just as well restrict to a site of only [[infinitesimal space]]s, because all homs from a finite non-thickened space into an infinitesimal space are trivial anyway. 

Therefor for $\mathfrak{g}$ and $\mathfrak{h}$ $\infty$-Lie algebras, a [[cocycle]] on $\mathfrak{g}$ with values in $\mathfrak{h}$ is just a morphism 

$$
  (c : \mathfrak{g} \to \mathfrak{h}) \in \infty LieAlg \subset \infty LieGrpd
$$

and the [[∞-groupoid]] of cocycles is

$$
  \infty LieGrpd(\mathfrak{g}, \mathfrak{h})
  \simeq
  \infty LieAlg(\mathfrak{g}, \mathfrak{h})
  \,.
$$

Such cocycles are modeled by morphisms in $dgAlg^{op}$ from a cofibrant representative of $\mathfrak{g}$ to a fibrant representative of $\mathfrak{h}$. Since in $dgAlg$ all objects are fibrantm, in $dgAlg^{op}$ all objects are cofibrant. The cofibrant objects in the [[model structure on dg-algebras]] are the [[Sullivan algebra]]s $CE(\mathfrak{h})$. In particular for $\mathfrak{h} = b^{n-1}\mathbb{R}$ we have that $CE(b^{n-1}\mathbb{R})$ is a Sullivan algebra, so $b^{n-1} \mathbb{R}$ is fibrant in $dgAlg^{op}$. 

In summary, this says that morphisms

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{n-1}\mathbb{R})
$$

indeed model the abstract intrinsic $(\infty,1)$-topos theoretic notion of cocycles in $\infty Lie Algd \subset \infty Lie Grpd$.

## Examples

Special cases of $\infty$-Lie algebra cohomology are of course

* [[Lie algebra cohomology]]

* [[nonabelian Lie algebra cohomology]].



## Extensions {#Extensions}

In any  [[(∞,1)-topos]] with its intrinsic notion of [[cohomology]], a [[cocycle]] $c : X \to \mathbf{B}^{n+1} A$ classifies an _extension_ $\mathbf{B}^n A \to \hat X \to X$. This $\hat X$ is nothing but the [[homotopy fiber]] of $c$, or equivalently the $\mathbf{B}^n A$-[[principal ∞-bundle]] classified by $c$.

After embedding [[∞-Lie algebra]]s into the [[(∞,1)-topos]] of [[∞-Lie groupoid]]s as described [above](#Topos), the same abstract reasoning applies to $\infty$-Lie algebra cocycles and the extensions of $\infty$-Lie algebras that these classify: for $c : \mathfrak{g} \to b^n \mathbb{R} $ a cocycle of $\infty$-Lie algebras, the extension $b^{n-1} \mathbb{R} \to \hat \mathfrak{g} \to \mathfrak{g}$ is the [[homotopy fiber]] of this morphism in [[?LieGrpd]].

For $\mathfrak{g}$ an ordinary [[Lie algebra]], this reproduces the ordinary notions of extensions from [[Lie algebra cohomology]] and [[nonabelian Lie algebra cohomology]].

**Observation**

For $c : \mathfrak{g} \to b^n \mathbb{R}$ an $(n+1)$-cocycle of an $\infty$-Lie algebra $\mathfrak{g}$, the ordinary [[pullback]] in $dgAlg^{op}$

$$
  \array{
    \hat g &\to& inn(b^{n-1}\mathbb{R})
    \\
    \downarrow && \downarrow
    \\
    \mathfrak{g} &\stackrel{c}{\to}& b^n \mathfrak{R}
  }
$$

maps under $R$ to a pullback diagram of simplicial presheaves which exhibits $R(\hat \mathfrak{g})$ as isomorhic to the [[homotopy pullback]] in the [[homotopy category]].

Here the right morphism denotes the dual of the generating cofibration in $dgAlg$, which models the $b^n \mathfrak{R}$-[[universal principal ∞-bundle]].

**Proof**

Being a right Quillen functor, $R$ preserves fibrations and pullbacks, hence 

$$
  \array{
    R \hat g &\to& R inn(b^{n-1}\mathbb{R})
    \\
    \downarrow && \downarrow
    \\
    R \mathfrak{g} &\stackrel{R c}{\to}& R b^n \mathfrak{R}
  }
$$

is a pullback of a fibration. Since $[ThCartSp^{op},sSet]_{proj}$ is a [[proper model category|right proper model category]] this is a [[homotopy pullback]], even if $R \mathfrak{g}$ is possibly not fibrant. (The detailed argument for that is reproduced at [[proper model category]].)

Since [[∞-stackification]] preserves finite [[(∞,1)-limit]]s, this is sufficient to deduce that $R \hat \mathfrak{g}$ represents in the [[homotopy category]] $Ho([ThCartSp, sSet]_{proj,cov})$ the [[homotopy fiber]] of $R c : R \mathfrak{g} \to R b^n \mathbb{R}$.

### Examples

* For $\mathfrak{g}$ and $\mathfrak{h}$ ordinary [[Lie algebra]]s, and $der(\mathfrak{h})$ the Lie algebra of [[derivation]]s of $\mathfrak{h}$, a morphism $\mathfrak{g}\to der(\mathfrak{h})$ is a cocycle in [[nonabelian Lie algebra cohomology]] and the extension it classifies is an ordinary [[Lie algebra extension]].

* The [[string Lie 2-algebra]] is the $b \mathbb{R}$-extension of a semisimple [[Lie algebra]] $\mathfrak{g}$ with bilinear [[invariant polynomial]] $\langle -,-\rangle$ corresponding to the 3-cocycle $\langle -,[-,-]\rangle \in CE(\mathfrak{g})$.


[[!redirects ∞-Lie algebra cohomology]]
[[!redirects L-∞-algebra cohomology]]
[[!redirects L-∞ algebra cohomology]]
[[!redirects Lie ∞-algebra cohomology]]

[[!redirects ∞-Lie algebra cocycle]]
[[!redirects L-∞-algebra cocycle]]
[[!redirects L-∞ algebra cocycle]]
[[!redirects Lie ∞-algebra cocoycle]]

[[!redirects ∞-Lie algebra cocycles]]
[[!redirects L-∞-algebra cocycles]]
[[!redirects L-∞ algebra cocycles]]
[[!redirects Lie ∞-algebra cocoycles]]
