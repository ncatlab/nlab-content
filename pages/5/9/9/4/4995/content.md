
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A _cohesive $(\infty,1)$-topos_ is a [[big topos|big]] [[(∞,1)-topos]] $\mathbf{H}$ that provides a context of generalized [[space]]s in which [[higher geometry]] makes sense. 

It is an $(\infty,1)$-topos whose [[global section]] [[(∞,1)-geometric morphism]] $(Disc \dashv \Gamma): \mathbf{H} \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}} $ [[∞Grpd]] admits a further [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\Pi$ and a further right adjoint $CoDisc$: 

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : \mathbf{H} \to \infty Grpd
$$ 

with $Disc$ and $Codisc$ both [[full and faithful (∞,1)-functor]]s and such that $\Pi$ moreover preserves finite [[(∞,1)-limit|(∞,1)-product]]s. Here

1. the existence of $CoDisc$ induces a sub-[[(∞,1)-quasitopos]] $Conc(\mathbf{H}) \hookrightarrow \mathbf{H}$ of _[[concrete (∞,1)-sheaf|concrete objects]]_ that behave like [[∞-groupoid]]s _equipped with extra cohesive structure_ , such as with [[topology|continuous structure]], [[smooth structure]], etc.

1. the existence of $\Pi$ induces a notion of [[geometric homotopy groups in an (∞,1)-topos|geometric]] [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]], hence under $|-| : \infty Grpd \simeq $ [[Top]] of [[geometric realization]] $|\Pi(-)|$ of objects in $\mathbf{H}$.

The functor $\Gamma$ itself may be thought of as sending a cohesive [[∞-groupoid]] $X$ to its underlying bare $\infty$-groupoid $\Gamma(X)$. This is $X$ with all _cohesion forgotten_ (for instance with the continuous or the smooth structure forgotten).

Conversely, $Disc$ and $CoDisc$ send an $\infty$-groupoid $A$ either to the [[discrete space|discrete ∞-groupoid]] $Disc(A)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space|codiscrete ∞-groupoid]] $Codisc(A)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]). 

The existence of such a quadruple of adjoint $(\infty,1)$-functors alone implies a rich [[internalization|internal]] [[higher geometry]] in $\mathbf{H}$ that comes with its internal notion of [[Galois theory]], [[Lie theory]], [[differential cohomology]], [[Chern-Weil theory]]. 

Examples of cohesive $(\infty,1)$-toposes include

* the $(\infty,1)$-topos $\mathbf{H} = $ [[topological ∞-groupoid|?ContGrpd]] of [[topological ∞-groupoid|continuous ∞-groupoids]];

* the $(\infty,1)$-topos $\mathbf{H} = $ [[?LieGrpd]] of [[smooth ∞-groupoids]] / [[synthetic differential geometry|synthetic differential ∞-groupoids]].

In the former the internal notion of [[Galois theory]] subsumes the usual one (over well-behaved topological spaces). In the latter also the notions of [[Lie theory]], [[differential cohomology]] and [[Chern-Weil theory]] subsume the uual ones --- and generalize them to higher smooth geoemtry.


## Definition

+-- {: .un_defn}
###### Definition

An [[(∞,1)-topos]] $\mathbf{H}$ over some base $(\infty,1)$-topos $\mathbf{S}$ given by an [[(∞,1)-geometric morphism]]

$$
  (f^* \dashv f_*) : \mathbf{H} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  \mathbf{S}
$$

is **cohesive** over $\mathbf{S}$ if

1. it is a [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos]]

1. it is a [[local (∞,1)-topos]]

and such that  $f_!$ preserves finite [[(∞,1)-limit|product]]s.

For $S = $ [[∞Grpd]] this means equivalently:  we have a quadruple of [[adjoint (∞,1)-functor]]s
   
$$
  (f_! \dashv f^* \dashv f_* \dashv f^!) : 
  \mathbf{H}
   \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
  \infty Grpd
  \;
$$

with both $f^*$ and $f^!$ being [[full and faithful (∞,1)-functor]]s and $f_!$ preserving finite products.

(For more general $\mathbf{S}$ there is an extra condition on $\Pi$.)

If $(f_* \dashv f^*)$ is the [[global section]] geometric morphism of an $(\infty,1)$-topos over $\mathbf{S}$, we say that $\mathbf{H}$ is a **cohesive $(\infty,1)$-topos** over $\mathbf{S}$. In this case we denote the four $(\infty,1)$-functors also

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
  \mathbf{H}
   \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  \mathbf{S}
  \,.
$$


=--


## Properties

### Shape

The [[shape of an (∞,1)-topos]] $\mathbf{H}$ is the fundamental $\infty$-groupoid $\Pi(\mathbf{H})$ for $\mathbf{H}$ itself regarded as a space.

+-- {: .un_remark}
###### Remark

A cohesive $(\infty,1)$-topos $\mathbf{H}$ is, when itself regarded as a [[space]], a _thickened point_ . We may think of it as the standard [[point]] equipped with a _cohesive neighbourhood_ .

In this sense every space $X$ _modeled on_ the cohesive structure defined by $\mathbf{H}$ is an [[etale space]] over $X$: its [[petit topos|petit]] $(\infty,1)$-topos $\mathbf{H}/X$ sits by a [[locally homeomorphic geometric morphism]] over $\mathbf{H}$

$$
  \mathbf{H}/X \stackrel{local\;homeo}{\to} \mathbf{H}
  \,.
$$


=--

Notice that the canonical cohesive $(\infty,1)$-topos [[∞Grpd]] may be thought of as being the ($(\infty,1)$-topos theoretical dual to) the standard [[point]], because it is the [[(∞,1)-category of (∞,1)-sheaves]] on the standard topological point:

$$
  \infty Grpd \simeq (\infty,1)Sh(*)
  \,.
$$

The abstract properties of a cohesive $(\infty,1)$-topos $\mathbf{H}$ over $\infty Grpd$ show that also $\mathbf{H}$ still _looks like a point_ :

1. **shape of the point:** Since $\mathbf{H}$ is a [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos]] it looks like a [[contractible]] [[topological space]];

   1. this implies in particular that the [[shape of an (∞,1)-topos]] of $\mathbf{H}$ is the same as that of the point.

1. **small neighbourhood of a point:** Since $\mathbf{H}$ is a [[local (∞,1)-topos]] it is similar to the standard examples of [[local topos]]es, which are [[infinitesimal space|infinitesimal]] neighbourhoods of points.

We may therefore usefully think of a cohesive $(\infty,1)$-topos as _being_ the general abstract _lump of cohesive points_ for the given notion of cohesion.

For instance in the [examples](#Examples) we see that

* $(\infty,1)Sh(CartSp)$ is like the **general abstract smooth [[open ball]]**.

* let $\mathbb{L}_{inf}$ be the full subcategory of [[smooth loci]] in the [[infinitesimal space]]s. then   $(\infty,1)Sh(\mathbb{L}_{inf})$ is like the **general abstract infinitesimally thickened point**;

* similarly, let $\Lambda$ be the category of $\mathbb{Z}_2$-graded [[Grassmann algebra]]s. Then $(\infty,1)Sh(\Lambda^{op})$ is like the **general abstract super-point**;

* $(\infty,1)Sh(ThCartSp)$ is like the **general abstract infinitesimally thickened smooth open ball** .

Notice that for plain [[topological space]]s an [[etale space]] $X \to H$ is a space $X$ that is _locally built from pieces of $H$_ . The generalization of this from [[topology]] to [[topos theory]] is an [[etale geometric morphism]] or [[locally homeomorphic geometric morphism]]: every object $X \in \mathbf{H}$ gives rise to the [[over-(∞,1)-category]] $(\infty,1)$-topos $\mathbf{H}/X$ with the evident projection geometric morphism $\mathbf{H}/X \to \mathbf{H}$.

This way we can think of any object $X \in \mathbf{H}$ of the $(\infty,1)$-topos equivalently as a space that is locally built from pieces of $\mathbf{H}$. With the above interpretation of $\mathbf{H}$ as the general abstract lump of cohesive points, this reproduces the intuition that $X \in \mathbf{H}$ is a space with this cohesive structure.

### Coshape

The [[coshape of an (∞,1)-topos]] $\mathbf{H}$ is the underlying $\infty$-groupoid $\Gamma(\mathbf{H})$ for $\mathbf{H}$ itself regarded as a space.

(...)

## Structures in a cohesive $(\infty,1)$-topos

A cohesive $(\infty,1)$-topos is a general context for [[higher geometry]] with good [[cohomology]] and [[homotopy]] properties. We list fundamental structures and constructions that exist in every cohesvive $(\infty,1)$-topos.

### $\infty$-Groups {#InfinGroups}

Every [[(∞,1)-category]] with [[(∞,1)-limit]]s comes with its notion of [[loop space object]]. A [[connected]] object in $\mathbf{H}$ we write $\mathbf{B}G$. Its [[loop space object]]

$$
  G := \Omega \mathbf{B}G
$$

is the [[∞-group]] of which $\mathbf{B}G$ is the [[delooping]] object.


### Cohomology {#Cohomology}

Every [[(∞,1)-topos]] comes with its intrinsic notion of [[cohomology]]. 

A [[morphism]] $g : X \to A$ is a [[cocycle]] on $X$ with coefficients in $A$. The [[hom ∞-groupoid]] $\mathbf{H}(X,A)$ is the _cocycle $\infty$-groupoid_ . Its [[connected component]]s are the $A$-cohomology classes of $X$

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$

If $A$ admits an $p$-fold [[delooping]] we write

$$
  H^p(X,A) := \pi_0 \mathbf{H}(X, \mathbf{B}^n A)
  \,.
$$

+-- {: .un_prop}
###### Proposition

We have that $\mathbf{H}(X,\mathbf{B}G)$ classifies $G$-[[principal ∞-bundle]]s on $X$.

=--

+-- {: .proof}
###### Proof

Define the $G$ principal $\infty$-bundle $P \to X$ corresponding to a [[cocycle]] $g : X \to \mathbf{B}G$ as its [[homotopy fiber]]

$$
  \array{
    P &\to& *
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

The claim follows using that in an [[(∞,1)-topos]] we have [[universal colimits]] and all [[groupoid object in an (∞,1)-category|groupoid objects]] are effective. A detailed discussion is at [[principal ∞-bundle]]. 

=--

### Concordance {#Concordance}

Since $\mathbf{H}$ is an [[(∞,1)-topos]] it carries canonically
the structure of a [[cartesian closed (∞,1)-category]]. For  
$X, Y \in \mathbf{H}$, write $Y^X \in \mathbf{H}$ for the corresponding
[[internal hom]].

Since $\Pi : \mathbf{H} \to $ [[∞Grpd]] preserves products, we have 
for all $X,Y, Z \in \mathbf{H}$ canonically induced a morphism

$$
  \Pi(Y^X) \times \Pi(Z^Y)
   \stackrel{\simeq}{\to}
  \Pi(Y^X \times Z^Y)
  \stackrel{\Pi(comp_{X,Y,Z})}{\to}
  \Pi(Z^X)
  \,.
$$

This should yield an [[(∞,1)-category]] $\tilde \mathbf{H}$
with the same objects as $\mathbf{H}$ and hom-$\infty$-groupoids defined by

$$
  \tilde \mathbf{H}(X,Y) := \Pi(Y^X)
  \,.
$$

We have that

$$
  \tilde \mathbf{H}(X,\mathbf{B}G) = \Pi(\mathbf{B}G^X) 
$$

is the $\infty$-groupoid whose objects are $G$-[[principal ∞-bundle]]s on $X$ and whose morphisms have the interpretaton of $G$-principal bundles on the cylinder $X \times I$. These are _[[concordance]]s of $\infty$-bundles._



### Homotopy and Galois theory {#Homotopy}

Every [[locally ∞-connected (∞,1)-topos]] comes with its notion of [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] $\Pi(X)$ of an object $X$.

We say the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of $X$ are ordinary [[homotopy group]]s of $\Pi(X)$.

Let $Fin \infty Grpd \in \infty Grpd$ be the [[∞-groupoid]] of finite $\infty$-groupoids. 

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ write

$$
  LConst(X) := \mathbf{H}(X, Disc Fin \infty Grpd)
  \,.
$$

We call this the $\infty$-groupoid of **[[locally constant ∞-stack]]s** on $X$.

=--

+-- {: .un_prop}
###### Proposition

We have

* $Disc(X) \simeq Func(\Pi(X), Fin \infty Grpd)$;

* for any point $x : * \to X$ the endomorphisms of the fiber functor are

  $$
    End( x^* : Disc(X) \to Fin ) \simeq \Omega_x \Pi(X)
    \,.
  $$

=--

+-- {: .proof}
###### Proof

The first statement is just the adjunction $(\Pi \dashv Disc)$. The second statement is pure [[Tannaka duality]] (as describe there), so follows with a quadruple application of the [[(∞,1)-Yoneda lemma]].

=--

### van Kampen theorem {#vanKampenTheorem}

A [[higher homotopy van Kampen theorem|higher]] [[van Kampen theorem]] asserts that passing to [[fundamental ∞-groupoid]]s preserves certain colimits. 

On a cohesive $(\infty,1)$-topos $\mathbf{H}$ the fundamental $\infty$-groupoid functor $\Pi : \mathbf{H} \to \infty Grpd$ is a [[left adjoint]] [[(∞,1)-functor]] and hence preserves all [[(∞,1)-colimit]]s.

More interesting is the question which $(\infty,1)$-colimits of [concrete spaces](#ConcreteObjects) in  

$$
  Conc(\mathbf{H}) 
    \stackrel{\overset{conc}{\leftarrow}}{\underset{inj}{\hookrightarrow}} 
  \mathbf{H}
$$ 

are preserved by $\Pi \circ inj : Conc(\mathbf{H}) \to \infty Grpd$. These colimits are computed by first computing them in $\mathbf{H}$ and then applying the concretization functor. So we have

+-- {: .un_lemma}
###### Observation

Let $U_\bullet : K \to Conc(\mathbf{H})$ be a [[diagram]] such that
the [[(∞,1)-colimit]]
$\lim_\to inj \circ U_\bullet$ is concrete, $\cdots \simeq inj(X)$.

Then the [[schreiber:path ∞-groupoid|fundamental ∞-groupoid]] of $X$ is computed as the $(\infty,1)$-colimit

$$
  \Pi(X) \simeq {\lim_\to} \Pi(U_\bullet)
  \,.
$$


=--


In the [Examples](#Examples) we discuss the cohesive $(\infty,1)$-topos $\mathbf{H} = (\infty,1)Sh(TopBall)$ of [[topological ∞-groupoid]]s For that case we recover the ordinary [[higher van Kampen theorem]]:

+-- {: .un_prop}
###### Proposition

Let $X$ be a [[paracompact space|paracompact]] or [[locally contractible space|locally contractible]] [[topological space]]s and $U_1 \hookrightarrow X$, $U_2 \hookrightarrow X$ a [[covering]] by two [[open subsets]].

Then under the [[singular simplicial complex]] functor $Sing : Top \to $ [[sSet]] we have a [[homotopy pushout]]

$$
  \array{
    Sing(U_1) \cap Sing(U_2) &\to& Sing(U_2)
    \\
    \downarrow && \downarrow
    \\
    Sing(U_1) &\to& Sing(X)
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

We inject the topological space via the external [[Yoneda embedding]]

$$
  Top \hookrightarrow Sh(TopBalls) \hookrightarrow
  \mathbf{H} := (\infty,1)Sh(OpenBalls)
$$

as a 0-[[truncated]] [[topological ∞-groupoid]] in the cohesive 
$(\infty,1)$-topos $\mathbf{H}$. Being an [[(∞,1)-category of (∞,1)-sheaves]] this is [[locally presentable (∞,1)-category|presented]] by the [[Bousfield localization of model categories|left Bousfield localization]] $Sh(TopBalls, sSet)_{inj,loc}$ of the injective [[model structure on simplicial sheaves]] on $TopBalls$ (as described at [[models for ∞-stack (∞,1)-toposes]]). 

Notice that the injection $Top \hookrightarrow Sh(TopBalls)$ of topological spaces as [[concrete sheaves]] on the site of open balls preserves the pushout $X = U_1 \coprod_{U_1 \cap U_2} U_2$. (This is effectively the statement that $X$ as a [[representable functor|representable]] on [[Diff]] is a [[sheaf]].) Accordingly so does the further inclusion into $Sh(TopBall,sSet) \simeq Sh(TopBalls)^{\Delta^{op}}$ as simplicially constant simplicial sheaves.

Since cofibrations in that model structure are objectwise and degreewise injective maps, it follows that the ordinary [[pushout]] diagram

$$
  \array{
    U_1 \cap U_2 &\to& U_2
    \\
    \downarrow && \downarrow
    \\
    U_1 &\to& X
  }
$$

in $Sh(TopBalls, sSet)_{inj,loc}$ has all objects cofibrant and is the pushout along a cofibration, hence is a [[homotopy pushout]] (as described there). By the general theorem at [[(∞,1)-colimit]] homotopy pushouts model $(\infty,1)$-pushouts, so that indeed $X$ is the $(\infty,1)$-pushout

$$
  X \simeq U_1 \coprod_{U_1 \cap U_2} U_2 \in \mathbf{H}
  \,.
$$

The proposition now follows with the above observation that $\Pi$ preserves all $(\infty,1)$-colimits and with the statement (from [[topological ∞-groupoid]]) that for a topological space (locally contractible or paracompact) we have $\Pi X \simeq Sing X$.

=--




### Paths {#Paths}

+-- {: .un_def}
###### Definition

Set

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma}) 
  :=
  (Disc \Pi \dashv Disc \Gamma \dashv CoDisc \Gamma)
  \,.
$$

=--

Let 

$$
  (\tau_n \dashv i_n)
  :
  \mathbf{H}_{\leq n}
  \stackrel{\overset{\tau_{n}}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  \mathbf{H}
$$

be the [[reflective sub-(∞,1)-category]] of [[truncated|n-truncated object]]s. Write

$$
  \mathbf{\tau}_n : \mathbf{H} \stackrel{\tau_n}{\to} \mathbf{H}_{\leq n}
  \hookrightarrow
  \mathbf{H}
$$

for the truncation [[localization of an (∞,1)-category]].

We say

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\Pi}_n}{\to}
   \mathbf{H} \stackrel{\mathbf{\tau}_n}{\to}
  \mathbf{H}
$$

is the **[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|path n-groupoid]]** functor. 

Notice that for any $X \in \mathbf{H}$ we have the [[Postnikov tower in an (∞,1)-category|Postnikov tower]]

$$
  \mathbf{\Pi}(X) \to \cdots
   \to 
   \mathbf{\Pi}_2(X) \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)
  \,.
$$



### Universal coverings and Whitehead towers {#Coverings}

+-- {: .un_def}
###### Definition

The **[[Whitehead tower in an (∞,1)-topos|whitehead tower]]** of $X \in \mathbf{H}$ is the sequence of objects 

$$
  * \to \cdots \to X^{(2)} \to X^{(1)} \to X^{(0)} \simeq X
$$

in $\mathbf{H}$, where for each $n \in \mathbb{N}$ the object $X^{(n+1)}$ is the [[homotopy fiber]] of the canonical morphism $X \to \mathbf{\Pi}_{n+1}$, i.e. the object defined by the [[(∞,1)-pullback]] diagram

$$
  \array{
    X^{(n+1)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_{n+1}(X)
  }
  \,.
$$

This we call the $(n+1)$-fold **[[universal covering space]]** of $X$.

=--

Here the morphisms $X^{(n+1)} \to X^{(n)}$ are induced from the universality of the pullback:


$$
  \array{
    && *
    \\
    &\nearrow& &\searrow& 
    \\
    X^{(n+1)}&\to&X^{(n)}&& \mathbf{\Pi}_{(n+1)}(X)
    \\
    &\searrow &\downarrow&\nearrow& \downarrow
    \\
    &&X &\to& \mathbf{\Pi}_n(X)
  }
$$

+-- {: .un_lemma}
###### Lemma

For a cohesive topos on an [[(∞,1)-cohesive site]] we have
that $\mathbf{\Pi}_n(X) \simeq Disc \tau_{\leq n} \Pi(X)$.

=--

+-- {: .proof}
###### Proof

This follows from $\mathbf{\tau}_{\leq n} LConst \Pi(X) \simeq LConst \tau_{\leq n} \Pi(X)$. This, in turn, can for instance be checked in terms of the [[model structure on simplicial presheaves]], using that $\tau$ is objectwise the [[coskeleton]] operation. More on that at [[Postnikov tower in an (∞,1)-category]].

=--

+-- {: .un_remark}
###### Remark


Therefore  homotopy-commuting diagram

$$
  \array{
    X^{(n)} &\to& {*}
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X)
  }
$$

in $\mathbf{H}$ corresponds by the [[adjoint (∞,1)-functor|adjunction relation]] to diagram 

$$
  \array{
    \Pi(X^{(n)}) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \Pi(X) &\to& {\Pi}_n(X)
  }
$$

in [[∞Grpd]]. This being universal means that $\Pi(X^{(n)})$ is $n$-[[connected]], and universal with that property as an object over $\Pi(X)$.

=--



+-- {: .un_def}
###### Definition


For $* \to X \in \mathbf{H}$ a [[pointed object]] and $n \in \mathbb{N}$, $n \geq 1 $, define the object $\mathbf{B}^n \mathbf{\pi}_n(X)$ to be the [[homotopy fiber]] of $\mathbf{\Pi}_n(X) \to \mathbf{\Pi}_{n-1}(X)$, so that we have a [[fiber sequence]]

$$
  \mathbf{B}^n \mathbf{\pi}_n(X) \to \mathbf{\Pi}_n(X) \to \mathbf{\Pi}_{n-1}(X)
  \,.
$$

=--

+-- {: .un_corollary}
###### Corollary

We have

$$
  \mathbf{B} \mathbf{\pi}_n(X)
  \simeq
  Disc \mathcal{B}^n \pi_n(X)
  \,,
$$

where $\mathcal{B}^n \pi_n(X)$ denotes the [[homotopy fiber]] of 
$\Pi_n(X) \to \Pi_{(n-1)}(X)$ in [[∞Grpd]].

=--



+-- {: .un_proposition}
###### Proposition

For each $n \geq 1$ we have a [[fiber sequence]]

$$
  X^{(n)} \to X^{(n-1)} \to \mathbf{B}^n \mathbf{\pi}_n(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Regard the diagram

$$
  \array{
    X^{(n)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X^{(n-1)} & \to & \mathbf{B}^n \mathbf{\pi}_n(X) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X) &\to& \mathbf{\Pi}_{(n-1)}(X)
  }
  \,.
$$

Here the right square is the defining $(\infty,1)$-pullback diagram of $\mathbf{B}^n \mathbf{\pi}_n(X)$ from above. Take also the left bottom square to be a homotopy pullback. Then from the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">pasting law</a> of pullbacks it follows that the composite bottom rectangle is also a pullback, which identifies the object $X^{(n-1)}$ on the left as indicated.

Similarly, form now the top square as a pullback. Then by the composition law of pullbacks we find that the composite vertical rectangle is a pullback, which identifies the top left object as $X^{(n)}$.

=--








### Flat differential cohomology and local systems {#FlatDifferentialCohomology}

+-- {: .un_def}
###### Definition

For $X,A \in \mathbf{A}$ we write

$$
  \mathbf{H}_{flat}(X,A) := \mathbf{H}(\mathbf{\Pi}X, A)
  \simeq \mathbf{H}(X,\mathbf{\flat}A)
$$

and call this **flat differential cohomology** of $X$ with coefficients in $A$.

We say a [[cocycle]] $\nabla : \mathbf{\Pi}(X) \to A$ is a [[local system]] on $X$ with coefficients in $A$ or equivalently a **flat [[connection on an ∞-bundle|connection]]** on the [[principal ∞-bundle]] corresponding to $X \stackrel{}{\to} \mathbf{\Pi}X \stackrel{\nabla}{\to} A$.

=--

+-- {: .un_theorem }
###### Theorem

Let $\mathbf{H} = $ [[?TopGrpd]] or  [[?LieGrpd]] be the cohesive $(\infty,1)$-topos of [[topological ∞-groupoid]]s or [[smooth ∞-groupoid]]s. A [[smooth manifold]] $X$ is naturally regarded as an object in there.

For [[paracompact space|paracompact]] $X$ and any $A \in \infty Grpd$ we have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  \mathbf{H}(X, Disc A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0 \mathbf{H}(X, Disc A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

For paracompact $X$, the [[nerve theorem]] asserts that $\Pi(X)$ is [[weak homotopy equivalence|weak homotopy equivalent]] to $Sing X$, the standard [[fundamental ∞-groupoid]] of $X$. This is discussed at [[∞-Lie groupoid]].

Using this, the statement follows by the [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $(\Pi \dashv Disc)$.

=--

See [[nonabelian cohomology]] for more details.


### de Rham cohomology {#deRhamCohomology}

+-- {: .un_def}
###### Definition

Define

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} \dashv \mathbf{\Gamma}_{dR})
  : 
  */\mathbf{H}
  \stackrel{\overset{\mathbf{\Pi}_{dR}}{\leftarrow}}{\stackrel{\underset{\mathbf{\flat}_{dR}}{\to}}{\underset{\mathbf{\Gamma}_{dR}}{\leftarrow}}}
  \mathbf{H}
$$

by forming the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{\flat}_{dR} A &\to& \mathbf{\flat} A 
    \\
    \downarrow && \downarrow
    \\
    * &\to& A
  }
$$


and the [[(∞,1)-colimit|(∞,1)-pushout]]

$$
  \array{
    X &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}(X) &\to& \mathbf{\Pi}_{dR}X
  }
$$

and

$$
  \array{
    X &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Gamma} X &\to& \mathbf{\Gamma}_{dR}X
  }
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

We do indeed have a triple of [[adjoint (∞,1)-functor]]s $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} \dashv \mathbf{\Gamma}_{dR})$ as indicated.

=--

+-- {: .proof}
###### Proof

We check the defining hom-equivalence. For $X \in \mathbf{H}$, $A \in */\mathbf{H}$ two objects, we have by the fact that the [[hom-functor]] : $\mathbf{H}(-,-) : \mathbf{H}^{op} \times \mathbf{H} \to \infty Grpd $ preserves limits in both arguments a sequence of natural equivalences

$$
  \begin{aligned}
    */\mathbf{H}(\mathbf{\Pi}_{dR}, A)
    & \simeq
    \lim_{\leftarrow}
    \left(
      \array{
         && \mathbf{H}(X,A)
         \\
         && \downarrow
         \\
         * &\to& \mathbf{H}(Disc \Pi X, A )
      }
    \right)
    \\
    & \simeq
    \lim_{\leftarrow}
    \left(
      \array{
         && \mathbf{H}(X,A)
         \\
         && \downarrow
         \\
         * &\to& \mathbf{H}(X, Disc \Gamma A )
      }
    \right)    
    \\
    & \simeq
    \mathbf{H}(X, \mathbf{\flat}_{dR} A)
  \end{aligned}
  \,.
$$

Analously for the other case.

=--


+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}$ we say that

$$
  \mathbf{H}_{dR}(X,A)
  :=
  \mathbf{H}(\mathbf{\Pi}_{dR}X, A)
  \simeq
  \mathbf{H}(X, \mathbf{\flat}_{dR} A)
$$

is **de Rham cohomology** of $X$ with coefficients in $A$.

=--

+-- {: .un_remark}
###### Remark

A [[cocycle]] in de Rham cohomology

$$
  \omega : \mathbf{\Pi}_{dR}X \to A
$$

is precisely an [flat connetion](#FlatDifferentialCohomology) on a trivializable $A$-principal $\infty$-bundle

=--

+-- {: .proof}
###### Proof

By the [[universal property]] of the [[(∞,1)-colimit]] that defines $\mathbf{\Pi}_{dR} X$ we have that $\omega$ corresponds to a diagram

$$
  \array{
    X &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    \mathbf{\Pi}(X) &\stackrel{\omega}{\to}& A
  }
  \,.
$$

The bottom horizontal morphism is a flat connection on the 
$\infty$-bundle given by the cocycle $X \to \mathbf{\Pi}(X) \stackrel{\omega}{\to} A$. The diagram says that this is equivalent to the trivial bundle given by the trivial cocycle $X \to * \to A$.

=--

### Concrete objects: Cohesive $\infty$-groupoids {#ConcreteObjects}

The general object $X \in \mathbf{H}$ in a cohesive $(\infty,1)$-topos may be non-[[concrete (∞,1)-sheaf|concrete]] in that it is not modeled on its [[point]]s, or rather its underlying [[∞-groupoid]] $\Gamma X$. 

Since 

$$
  \infty Grpd \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  \mathbf{H}
$$

is a [[geometric embedding]], the reflector $\Gamma$ encodes the [[localization of an (∞,1)-category]] at a class of morphisms $W$, realizing $\infty Grpd$ as the [[reflective sub-(∞,1)-category]] on the $W$-[[local object]]s. This inclusion factors canonically through the corresponding [[(∞,1)-quasitopos]] of $W$-[[separated presheaf|separated (∞,1)-sheaves]]

+-- {: .un_def}
###### Definition

The objects in the $(\infty,1)$-quasitopos

$$
  \infty Grpd 
    \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
   Conc(\mathbf{H})
   \stackrel{\overset{concretizaton}{\leftarrow}}{\underset{}{\hookrightarrow}}
   \mathbf{H}
$$

inside $\mathbf{H}$ we call the **[[concrete (∞,1)-sheaf|concrete]] objects** or **cohesive $\infty$-groupoids**-

=--


### Infinitesimal objects: $\infty$-Lie algebroids {#InfinitesimalObjects}

+-- {: .un_def}
###### Definition

A [[connected]] object $\mathbf{B}\mathfrak{g} \in  \mathbf{H}$ for which

$$
  \Pi \mathbf{B}\mathfrak{g} \simeq *
$$ 

and

$$
  \Gamma \mathbf{B}\mathfrak{g} \simeq *
$$

we call an **infinitesimal object**.

Its [[loop space object]]

$$
  \mathfrak{g} := \Omega \mathbf{B}G
$$

we call an **[[∞-Lie algebra]]** in $\mathbf{H}$. 

We say an object $A \in \mathbf{H}$ is an **[[∞-Lie algebroid]]** if for every point $* \to A$ the corresponding [[loop space object]] $\Omega_x A$ is equivalent to an $\infty$-Lie algebra.

Write

$$
  \mathbf{L}\hookrightarrow \mathbf{H} 
$$

for the full [[sub-(∞,1)-category]] on $\infty$-Lie algebroids.

=--


### Lie theory {#LieTheory}

+-- {: .un_def}
###### Definition

Set

$$
  (Lie \dashv \exp )
  : 
  ( 
    \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} 
     \dashv 
    \mathbf{\flat}_{dR}
    \mathbf{\Gamma}_{dR}
  )
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

For $\mathbf{B}G \in */\mathbf{H}$ we have that 

$$
  Lie \mathbf{B}G \in \mathbf{L} \hookrightarrow \mathbf{H}
$$

is an [infinitesimal object](#InfinitesimalObjects)

=--

+-- {: .proof}
###### Proof

Using that $\Pi$ preserves colimits and finite products, we have that 
$\Pi \mathbf{\Pi}_{dR} \mathbf{B}G$ is given by the pushout

$$
  \array{
    \Pi \mathbf{B}G &\to& *
    \\
    {}^{\mathllap{\Pi}(\iota)}\downarrow && \downarrow
    \\
    \Pi Disc \Pi \mathbf{B}G &\to& \Pi \mathbf{\Pi}_{dR} \mathbf{B}G 
   }
  \,.
$$

since $Disc$ is full and faithful we have that this is equivalent to the pushout

$$
  \array{
    \Pi \mathbf{B}G &\to& *
    \\
    {}^{\mathllap{\Pi}(\iota)}\downarrow && \downarrow
    \\
    \Pi Disc \Pi \mathbf{B}G 
    &&
    \\
    {}^{\mathllap{\epsilon_{\Pi \mathbf{B}G}}}\downarrow^{\mathrlap{\simeq}}
    &&
    \downarrow
    \\
    \Pi \mathbf{B}G
    &\to& \Pi \mathbf{\Pi}_{dR} \mathbf{B}G 
   }
  \,.
$$

By the [[zig-zag identity]] this is equivalent to the pushout

$$
  \array{
    \Pi \mathbf{B}G &\to& *
    \\
    {}^{Id}\downarrow && \downarrow
    \\
    \Pi \mathbf{B}G
    &\to& \Pi \mathbf{\Pi}_{dR} \mathbf{B}G 
   }
  \,.
$$

Since this is the pushout of an equivalence, also $* \to \Pi \mathbf{\Pi}_{dR} \mathbf{B}G$ is an equivalence.

By the formal dual of the argument we have that $\Gamma \mathbf{\flat}_{dR} A \simeq *$. Since $\Gamma$ also preserves all colimits, we have in addition $\Gamma \mathbf{\Pi}_{dR} \simeq \mathbf{\Pi}_{dR} \Gamma$. The claim then follows with the above observation.

=--

We shall also write

$$
  Lie \mathbf{B}G =: \mathbf{B}\mathfrak{g}
$$

and hence for the counit of the $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})$-adjunction we write

$$
  \mathbf{B}\mathfrak{g} \to \mathbf{B}G
  \,.
$$


+-- {: .un_prop #LieValuesofDeRham}
###### Proposition


Every [de Rham cocycle](#deRhamCohomology) $\omega : \mathbf{\Pi}_{dR} X \to \mathbf{B}G$ factors universally through the [[∞-Lie algebra]] of $G$

$$
  \array{
     && \mathbf{B}\mathfrak{g}
     \\
     & \nearrow & \downarrow
     \\
     \mathbf{\Pi}_{dR}X 
     &\stackrel{\omega}{\to}&
     \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is the <a href="http://ncatlab.org/nlab/show/adjoint+functor#UniversalArrows">universality of the unit</a> of $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})$.

=--

In particular

+-- {: .un_prop}
###### Corollary

Every morphism $\mathbf{B}\mathfrak{h} \to \mathbf{B}G$ from an $\infty$-Lie algebra to an $\infty$-group factors universally through the $\infty$-Lie algebra of that $\infty$-group

$$
  \array{
    \mathbf{B}\mathfrak{h} &\to& \mathbf{B}\mathfrak{g}
    \\
    & \searrow& \downarrow
    \\
    && \mathbf{BG}
  }
  \,.
$$

=--



### Maurer-Cartan forms and curvature characteristic forms {#CurvatureCharacteristics}

+-- {: .un_def}
###### Definition

For $G \in \mathbf{H}$ an [[∞-group]], write

$$
  \theta : G \to \mathbf{\flat}_{dR} \mathbf{B}\mathfrak{g}
$$

for the $\mathfrak{g}$-valued de Rham cocycle on $G$ which is induced by the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">pullbck pasting</a>

$$
  \array{
     G &\to& *
     \\
     {}^{\mathllap{\theta}}\downarrow && \downarrow
     \\
     \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat}\mathbf{B}G
     \\
     \downarrow && \downarrow
     \\
     * &\to& \mathbf{B}G 
  }
$$

and the [above proposition](#LieValuesofDeRham).

We call $\theta$ the **[[Maurer-Cartan form]]** on $G$.

+-- {: .un_remark}
###### Remark

By postcomposition the Maurer-Cartan form sends $G$-valued functions on $X$ to $\mathfrak{g}$-valued forms on $X$

$$
  \theta_* : \mathbf{H}(X,G) \to \mathbf{H}^1_{dR}(X,\mathfrak{g})
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

On $\mathbf{H} = $ [[?LieGrpd]] and $G \in \mathbf{H}$ an ordinary [[Lie algebra]], $\theta$ coicides with the ordinary [[Maurer-Cartan form]] on a Lie algebra.

=--

+-- {: .proof}
###### Proof

This is shown at [[∞-Lie groupoid]].

=--

For $G = \mathbf{B}^n A$ an [[Eilenberg-MacLane object]], we also write

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
$$

and call this the **universal [[curvature characteristic form]]** on $\mathbf{B}^n A$.

=--


### Differential cohomology {#DifferentialCohomology}

+-- {: .un_def }
###### Definition 

For $X \in \mathbf{H}$ and $A \in \mathbf{H}$ an [[∞-group]] write 

$$
  \mathbf{H}_{diff}(X,A)
$$ 

for the [[twisted cohomology]] of $X$ induced by the [curvature characteristic class](#CurvatureCharacteristics) $curv : A \to \mathbf{\flat}_{dR}\mathbf{B}\mathfrak{a}$. This is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X,A) &\stackrel{F}{\to}& 
     H_{dR}(X,\mathbf{B}\mathfrak{a})
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    \mathbf{H}(X,A) &\stackrel{curv}{\to}& 
     \mathbf{H}_{dR}(X,\mathbf{B}\mathfrak{a})
  }
  \,,
$$

(where the right vertical morphism is any choice of cocycle representative for each cohomology class).

This we call the **[[differential cohomology]]** of $X$ with coefficient in $A$.

For $c \in \mathbf{H}_{diff}(X,A)$ a cocycle, we call

* $F(c) \in H_{dR}(X,\mathbf{B}A)$ the **curvature** class of $c$;

* $[\eta(c)] \in H(X,A)$ the **underlying class in $A$-cohomology**.

=--


+-- {: .un_lemma}
###### Lemma
**(differential fiber sequence)**

Differential cohomology fits into a [[fiber sequence]]

$$
  \cdots
  \to
  \mathbf{H}(X, \Omega A)
  \to
  \mathbf{H}_{dR}(X, A)
  \to 
  \mathbf{H}_{diff}(X, A)
  \to
  \mathbf{H}(X, A)
  \,.
$$


=--


+-- {: .proof}
###### Proof

This is a general statement about the definition of [[twisted cohomology]]: consider the diagram

$$
  \array{
    \mathbf{H}(X,\mathbf{\flat}_{dR} \Omega \mathbf{B} A) 
    &\to& \mathbf{H}_{diff}(X,A) &\to & H(X, \mathbf{\flat}_{dR} \mathbf{B}A)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    * &\to& \mathbf{H}(X, A) &\stackrel{curv}{\to}&
    \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B} A)
  }
  \,.
$$

The square on the right is a pullback by definition of [[twisted cohomology]] in general and our special case of differential cohomology in particular. Take the left square to be the pullback of the middle vertical morphism to the point and deduce the top left object from that: by the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-pullback#QuasiCatPastingLaw">pasting law for (∞,1)-pullbacks</a> this top left object is the pullback of the total diagram. But by the definition of $H(X,\mathbf{\flat}_{dR}\mathbf{B}A)$ as the set of connected components of $\mathbf{H}(X,\mathbf{\flat}_{dR}\mathbf{B}A)$ it follows that the pullback of the outer diagram is 

$$
  \array{
    \Omega \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}A) &\to& 
     H(X,\mathbf{\flat}_{dR} \mathbf{B}A)
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B} A)
  }
  \,.
$$

Finally using that (as discussed at [[cohomology]] and at [[fiber sequence]]) $\Omega \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}A) \simeq \mathbf{H}(X,\Omega \mathbf{\flat}_{dR} \mathbf{B}A)$ and then
using the above observation that $\Omega \mathbf{\flat}_{dR} \mathbf{B}A \simeq \mathbf{\flat}_{dR} \Omega \mathbf{B}A$ and finally the defining equivalence $\Omega \mathbf{B}A \simeq A$ the claim follows.

=--

+-- {: .un_corollary}
###### Corollary

Let $\mathbf{B}^n K$ be an [[Eilenberg-MacLane object]] in $\mathbf{H}$, then differential cohomology in $\mathbf{H}$ fits into a [[short exact sequence]]

$$
  0 \to H_{dR}^n(X,K)/H^{n-1}(X,K) \to H_{diff}^n(X,K) \to H^n(X,K)
  \to 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

The above [[fiber sequence]] yields (as recalled there) a long exact sequence of pointed cohomology sets

$$
  \cdots
  \to
  H(X, \Omega A)
  \to
  H(X,\mathbf{\flat}_{dR} A)
  \to 
  H_{diff}(X, A)
  \to
  H(X, A)
  \,.
$$

If $A = \mathbf{B}^n K$ is an [[Eilenberg-MacLane object]] on an abelian group object $K$, then this reads

$$
  \cdots
  \to
  H^{n-1}(X,K)
  \to
  H^{n}_{dR}(X,K)
  \to 
  H_{diff}^n(X, K)
  \to
  H^n(X, K)
  \,.
$$

Moreover observing that by construction the last morphism $H_{diff}^n(X,K) \to H^n(X,K)$ is surjective (because in the defining $(\infty,1)$-pullback for $\mathbf{H}_{diff}$ the right vertical morphism is evidently surjective on connected components) this yields the short exact sequence as claimed.

=--

+-- {: .un_remark}
###### Remark

This is _essentially_ verbatim the expected short exact sequence familiar from ordinary generalized [[differential cohomology]] only up to the following slight nuances in notation:

1.  The cohomology groups of the short exact sequence above denote the groups obtained in the given [[(∞,1)-topos]] $\mathbf{H}$, not in [[Top]]. Notably for $\mathbf{H} = $ [[?LieGrpd]] and $|X| \in Top$ the geometric realization of a paracompact manifold $X$, we have that $H^1(X,U(1))$ above is $H^2_{sing}(|X|,\mathbb{Z})$ and not $H^1_{sing}(|X|,U(1))$. 

1. The fact that on the left  of the short exact sequence we find the intrinsic de Rham cohomology set $H_{dR}^n(X,A)$ instead of something like the set of all flat forms as familiar from discussions of ordinary generalized [[differential cohomology]] is due to the fact that, following the general abstract procedure of [[twisted cohomology]], we defined $\mathbf{H}_{diff}(X,A)$ as the $(\infty,1)$-pullback of the inclusion $H(X,\mathbf{\flat}_{dR}A ) \to \mathbf{H}(X,\mathbf{\flat}_{dR} A)$ of the set of connected components of curvature classes into the [[cocycle]] [[∞-groupoid]]. This is the only natural thing to do in a fully natural [[(∞,1)-category|(∞,1)-categorical setup]]. However, in applications we typically have a concrete model for the [[∞-groupoid]] $\mathbf{H}(X,\mathbf{\flat}_{dR} A)$ in mind, and then can consider the inclusion $\mathbf{H}(X,\mathbf{\flat}_{dR} A)_0 \hookrightarrow \mathbf{H}(X,\mathbf{\flat}_{dR} A)$ of all of its objects. While this does not make intrinsic sense -- it is a bit [[evil]] -- , this is what is effectively done in ordinary generalized [[differential cohomology]], and doing so in our definition changes the above short exact sequence slightly to become exactly the familiar sequence, for the suitable special cases.

=--

+-- {: .un_example}
###### Example

In $\mathbf{H} = $ [[?LieGrpd]] the above definition reproduces [[ordinary differential cohomology]]. A detailed discussion is at [[circle n-bundle with connection]].

=--



### Chern-Weil theory {#ChernWeilTheory}

For $G$ an [[∞-group]], $\mathbf{B}^n K$ an [[Eilenberg-MacLane object]] and

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^n K
$$

a cocycle for a [[characteristic class]], postcomposition with the [universal curvature characteristic](#CurvatureCharacteristics) $curv : \mathbf{B}^n K \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} K$ induces a [[curvature characteristic class]]

$$
  \langle -\rangle_{\mathbf{c}}
  : 
  \mathbf{B}G \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} K
  \,.
$$

+-- {: .un_def}
###### Definition


Postcomposition of $G$-[[cocycle]]s with this map is the **[[∞-Chern-Weil homomorphism]]**


$$
  \langle - \rangle_{\mathbf{c}} 
   :
  G Bund(X) \simeq \mathbf{H}(X,\mathbf{B}G)  
  \to 
  \mathbf{H}^{n+1}_{dR}(X,\mathfrak{k})
  \,.
$$

=--

+-- {: .un_def}
###### Definition

The **nonabelian differential cohomology** on $X$ is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{conn}(X, \mathbf{B}G) &\to& \prod_{\mathbf{c}_i} \mathbf{H}_{diff}(X,\mathbf{B}^{n_i+1} K)
   \\
   {}^{\mathllap{[-]}}\downarrow && \downarrow
   \\
   \mathbf{H}(X, \mathbf{B}G)  &\to&
   \prod_{\mathbf{c}_i} 
   \mathbf{H}(X,\mathbf{B}^{n_i} K)
  }
$$

We say a cocycle in $\nabla \in \mathbf{H}_{conn}(X, \mathbf{B}G)$ is a [[connection on an ∞-bundle|connection]] on the [[principal ∞-bundle]] $[\nabla]$.

=--

+-- {: .un_lemma}
###### Observation

On $\infty$-bundles with connection the [[∞-Chern-Weil homomorphism]] refines to taking values in differential cohomology

$$
  \hat \mathbf{c} : \mathbf{H}_{conn}(X, \mathbf{B}G)
   \to 
  \mathbf{H}_{diff}(X, \mathbf{B}^{n+1}K)
  \,.
$$


=--

This is discussed at [[∞-Chern-Weil theory]].


### Chern-Simons theory {#ChernSimonsTheory}

Let $\mathbf{H}$ be a cohesive $(\infty,1)$-topops into which [[manifold]]s embed suitably. Such as $\mathbf{H} = $ [[?LieGrpd]].

For $G \in \mathbf{H}$ an [[∞-group]] let 

$$  
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^n \mathbb{R}/\mathbb{Z}
$$

be a [[cocycle]] for a [[characteristic class]]. This induces the $\infty$-Chern-Weil homomorphism

$$
  \hat \mathbf{c} : \mathbf{H}_{conn}(\Sigma, \mathbf{B}G) 
  \to 
  \mathbf{H}_{diff}(\Sigma, \mathbf{B}^{n} \mathbb{R}/\mathbb{Z})
  \,.
$$

+-- {: .un_lemma}
###### Observation

If $\Sigma$ is a closed [[manifold]] of [[dimension]]

$$
  dim \Sigma \leq n
$$

then for any cocycle $\nabla \in \mathbf{H}_{conn}(X,\mathbf{B}G)$ the [[circle n-bundle with connection]] $\hat \mathbf{c}(\nabla)$ is necessarily _flat_ , so that

$$
  \mathbf{H}_{diff}(\Sigma, \mathbf{B}^n U(1))
  \simeq
  \mathbf{H}(\mathbf{\Pi}(\Sigma), \mathbf{B}^n U(1))
  \,,
$$

This expressin in turn is 

$$
  \cdots \simeq \infty Grpd(\Pi(\sigma), \mathcal{B}^n U(1))
  \,.
$$

=--

We may map this further to its $(n-dim \Sigma)$-[[truncated|truncation]]

$$
  :\infty Grpd(\Pi(X), \mathcal{B}^n U(1)) 
  \to
  \tau_{n-dim \Sigma} \infty Grpd(\Pi(X), \mathcal{B}^n U(1))
  \,.
$$

+-- {: .un_theorem}
###### Theorem

We have

$$
  \tau_{n-dim\Sigma} \infty Grpd(\Pi(\Sigma), \mathcal{B}^n U(1))
  \simeq
  \mathbf{B}^{n-dim \Sigma} U(1)
  \,.
$$

=--

(This is due to an observation by [[Domenico Fiorenza]].)

+-- {: .proof}
###### Proof

By general abstract reasoning (recalled at [[cohomology]] and [[fiber sequence]]) we have for the [[homotopy group]]s that

\[
  \pi_i \infty Grpd(\Pi(\Sigma),\mathcal{B}^n U(1))
  \simeq 
  H^{n-i}(\Sigma, U(1))
  \,.
\]

Now use the [[universal coefficient theorem]], which asserts that we have an [[exact sequence]]

\[
  0
  \to 
  Ext^1(H_{n-i-1}(\Sigma,\mathbb{Z}),U(1))
  \to 
  H^{n-i}(\Sigma,U(1))
  \to 
  Hom(H_{n-i}(\Sigma,\mathbb{Z}),U(1))
  \to 0
  \,.
\]

Since $U(1)$ is an [[injective object|injective]] $\mathbb{Z}$-[[module]] we have 

$$
  Ext^1(-,U(1))=0
  \,.
$$  

This means that we have an [[isomorphism]]

\[
  H^{n-i}(\Sigma,U(1))
  \simeq 
  Hom_{Ab}(H_{n-i}(\Sigma,\mathbb{Z}),U(1))
\]

that identifies the [[cohomology group]] in question with the [[internal hom]] in [[Ab]] from the integral [[homology]] group of $\Sigma$ to $U(1)$.

For $i\lt (n-dim \Sigma)$, the right hand is zero, so that 

$$
  \pi_i \infty Grpd(\Pi(\Sigma),\mathbf{B}^n U(1)) =0 \;\;\;\;
  for i\lt (n-dim \Sigma)
  \,. 
$$ 

For $i=(n-dim \Sigma)$, instead, $H_{n-i}(\Sigma,\mathbb{Z})\simeq \mathbb{Z}$, since $\Sigma$ is a closed $dim \Sigma$-manifold and so 

$$
  \pi_{(n-dim\Sigma)} \infty Grpd(\Pi(\Sigma),\mathcal{B}^n U(1))\simeq U(1)
  \,.
$$


=--


+-- {: .un_def}
###### Definition 

The resulting morphism

$$
  \exp(i S(-))
  :
  \mathbf{H}_{conn}(\Sigma, A)
  \stackrel{}{\to}
  \mathbf{B}^{n-dim\Sigma} U(1)
$$

in [[∞Grpd]] we call the [[higher parallel transport]] of $\hat \mathbf{c}(\nabla)$ and the **$\infty$-Chern-Simons action** of $\nabla$ on $\Sigma$.

=--

Here in the language of [[quantum field theory]]

* the objects of $\mathbf{H}(\Sigma,A_{conn})$ are the [[gauge field]]s on $\Sigma$;

* the [[morphism]]s in $\mathbf{H}(\Sigma, A_{conn})$ are the [[gauge transformation]]s;.

* the [[2-morphism]]s are the _higher gauge transformations_ (corresponding to _ghosts-of-ghosts_ in the [[BRST complex]]);

* and so on.


More discussion is at [[schreiber:∞-Chern-Simons theory]].


## Examples {#Examples}


+-- {: .un_def}
###### Definition

An **$(\infty,1)$-cohesive site** over [[∞Grpd]] is

* a [[site]] -- a [[small category]] $C$ equipped with a [[coverage]];

* with the property that

  * it has finite [[product]]s, in particular a [[terminal object]] $*$;
  
  * for every [[covering]] family $\{U_i \to U\}$ in $C$ 

    * the [[Cech nerve]] $C(U) \in [C^{op}, sSet]$ is degreewise 
      a [[coproduct]] of [[representable functor|representables]];

    * the [[simplicial set]] obtained by replacing each copy of a representable by a point is [[contractible]] (weakly equivalent to the 
      point in the standard [[model structure on simplicial sets]])

      $$
        \lim_\to C(U) \stackrel{\simeq}{\to} *
      $$

    * the simplicial set of points in $C(U)$ is weakly equivalent to the set of points of $U$:

      $$
        Hom_C(*, C(U)) \stackrel{\simeq}{\to} Hom_C(*,U)
        \,.
      $$
  
=--


+-- {: .un_prop}
###### Example/Proposition

Examples of $(\infty,1)$-cohesive sites are

* any category with finite [[product]]s and equipped with the trivial [[coverage]].

* the [[full subcategory]] $TopBalls \subset$ [[Top]] on [[open ball]]s with the [[good open cover]] [[coverage]];

* the site [[CartSp]] of [[Cartesian space]]s with [[smooth function]]s between them and [[good open cover]] [[coverage]].

* the [[Cahiers topos]]-site [[ThCartSp]] of infinitesimally thickened Cartesian spaces.

=--

+-- {: .un_prop}
###### Proposition

For $C$ an $(\infty,1)$-cohesive site, the [[(∞,1)-category of (∞,1)-sheaves]] $(\infty,1)Sh(C)$ is a cohesive $(\infty,1)$-topos.

=--

+-- {: .proof}
###### Proof

See <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-cohesive+site#Properties">(∞,1)-cohesive site -- Properties</a>.

=--

This proposition implies the examples of cohesive $(\infty,1)$-toposes listed in the following.

### Continuous $\infty$-groupoids

The cohesive $(\infty,1)$-topos $(\infty,1)Sh(TopBalls)$ is that of [[topological ∞-groupoid]]s.


### Smooth $\infty$-groupoids

The cohesive $(\infty,1)$-topos $(\infty,1)Sh(CartSp)$ is that of [[smooth ∞-groupoid]]s.

The 0-[[truncated]] [[concrete (∞,1)-sheaf|concrete]] objects in this are precisely the [[diffeological space]]s. Accordingly the general [[concrete (∞,1)-sheaves]] here we may think of as **diffeological $\infty$-groupoids**.

### Synthetic differential $\infty$-groupoids

The $(\infty,1)$-topos $(\infty,1)Sh(ThCartSp)$ is that of [[smooth ∞-groupoid|synthetic differential ∞-groupoid]] 

The [infinitesimal objects](#InfinitesimalObjects) include 
infinitesimal $\infty$-Lie groupoids: [[∞-Lie algebroid]]s $\mathbf{B}\mathfrak{g}$.





## Applications

As a context for geometric spaces and paths in geometric spaces, cohesive $(\infty,1)$-toposes are a natural context in which to formulate fundamental fundamental [[physics]]. See [[higher category theory and physics]] for more on this.

## References

The [[category theory|category-theoretic]] definition of [[cohesive topos]] was proposed in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
{#Lawvere}

The observation that the further left adjoint $\Pi$ in a [[locally ∞-connected (∞,1)-topos]] defines an intrinsic notion of paths and [[geometric homotopy groups in an (∞,1)-topos]] was suggested by [[Richard Williamson]].

The observation that the further right adjoint $Codisc$ in a [[local (∞,1)-topos]] serves to characterize [[concrete sheaf|concrete (∞,1)-sheaves]] was amplified by [[David Carchedi]].

Some discussion is at

* [[Urs Schreiber]], 

  _Cohesive $\infty$-Toposes_ ([blog entry](http://golem.ph.utexas.edu/category/2010/10/cohesive_toposes.html))

  _Structures in a Cohesive $\infty$-Topos_ ([blog entry](http://golem.ph.utexas.edu/category/2010/11/structures_in_a_cohesive_topos.html))

[[!redirects cohesive (∞,1)-topos]]

[[!redirects cohesive (∞,1)-toposes]]
[[!redirects cohesive (infinity,1)-toposes]]

[[!redirects cohesive (∞,1)-topoi]]
[[!redirects cohesive (infinity,1)-topoi]]
