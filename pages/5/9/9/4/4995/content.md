
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

+-- {: .un_defn #CohesiveInfinTopos}
###### Definition

An [[(∞,1)-topos]] $\mathbf{H}$ is **cohesive** if

1. it is a [[strongly ∞-connected (∞,1)-topos]];

1. it is a [[local (∞,1)-topos]].

This means equivalently: the [[global section]] [[(∞,1)-geometric morphism]] lifts to a quadruple of [[adjoint (∞,1)-functor]]s
   
$$
  (f_! \dashv f^* \dashv f_* \dashv f^!) : 
  \mathbf{H}
   \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
  \infty Grpd
  \;
$$

where $f_!$ preserves [[finite limit|finite]] [[(∞,1)-product]].

=--


## Properties

### General

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ a cohesive $(\infty,1)$-topos, the [[(n,1)-topos|(1,1)-topos]] $\tau_{\leq 1-1} \mathbf{H}$ of 0-[[truncated]] objects is a [[cohesive topos]].

=--


### Shape and coshape

The [[shape of an (∞,1)-topos]] $\mathbf{H}$ is the fundamental $\infty$-groupoid $\Pi(\mathbf{H})$ for $\mathbf{H}$ itself regarded as a space.

+-- {: .un_remark}
###### Remark

A cohesive $(\infty,1)$-topos $\mathbf{H}$ is, when itself regarded as a [[space]], a _thickened point_ . We may think of it as the standard [[point]] equipped with a _cohesive neighbourhood_ .

In this sense every space $X$ _modeled on_ the cohesive structure defined by $\mathbf{H}$ is an [[étale space]] over $X$: its [[petit topos|petit]] $(\infty,1)$-topos $\mathbf{H}/X$ sits by a [[locally homeomorphic geometric morphism]] over $\mathbf{H}$

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

Notice that for plain [[topological space]]s an [[étale space]] $X \to H$ is a space $X$ that is _locally built from pieces of $H$_ . The generalization of this from [[topology]] to [[topos theory]] is an [[étale geometric morphism]] or [[locally homeomorphic geometric morphism]]: every object $X \in \mathbf{H}$ gives rise to the [[over-(∞,1)-category]] $(\infty,1)$-topos $\mathbf{H}/X$ with the evident projection geometric morphism $\mathbf{H}/X \to \mathbf{H}$.

This way we can think of any object $X \in \mathbf{H}$ of the $(\infty,1)$-topos equivalently as a space that is locally built from pieces of $\mathbf{H}$. With the above interpretation of $\mathbf{H}$ as the general abstract lump of cohesive points, this reproduces the intuition that $X \in \mathbf{H}$ is a space with this cohesive structure.


The [[coshape of an (∞,1)-topos]] $\mathbf{H}$ is the underlying $\infty$-groupoid $\Gamma(\mathbf{H})$ for $\mathbf{H}$ itself regarded as a space.

(...)

## Structures in a cohesive $(\infty,1)$-topos {#Structures}

A cohesive $(\infty,1)$-topos is a general context for [[higher geometry]] with good [[cohomology]] and [[homotopy]] properties. We list fundamental structures and constructions that exist in every cohesvive $(\infty,1)$-topos.

The order is roughly by additional axioms needed for the
structure to exist. The first few exist in every $(\infty,1)$-topos, then there are several that need only local and some that also need global $\infty$-connectivity, and finally there are some that also need $\infty$-locality.

### Geometry and structure sheaves {#GeometryAndStructureSheaves}

+-- {: .un_def}
###### Definition

Fix an uncountable [[regular cardinal]] $\kappa$. Let 

$$
  \mathcal{G} \hookrightarrow Conc(\mathbf{H}) \hookrightarrow \mathbf{H}
$$ 

be the full [[sub-(∞,1)-category]] of [concrete objects](#ConcreteObjects) whose underlying $\infty$-groupoid is a $\kappa$-[[small (infinity,1)-category|small ∞-groupoid]]. 

=--

+-- {: .un_def}
###### Definition

We equip $\mathcal{G}$ with the canonical structure of a [[geometry (for structured (infinity,1)-toposes)|geometry]]:

* the _admissible morphisms_ are the [[monomorphism in an (infinity,1)-category|monomorphisms]];

* a family $\{U_i \to U\}$ of monomorphisms is a [[covering]] if the induced morphism out of the coproduct

  $$
    \coprod_i U_i \to U
  $$

  is an [[effective epimorphism]] in $\mathbf{H}$;


=--

+-- {: .un_lemma}
###### Observation

This definition indeed makes $\mathcal{G}$ a [[geometry (for structured (infinity,1)-toposes)|geometry]].

=--

+-- {: .proof}
###### Proof

By the $\kappa$-bound $\mathcal{G}$ is a [[small (∞,1)-category]].

Monomorphisms are stable under pullbacks and satisfy 2-out-of-3 (See [[monomorphism in an (∞,1)-category]].)

The quasi-$(\infty,1)$-topos $Conc(\mathbf{H})$ has all finite $(\infty,1)$-limits and these are preserved by the right adjoint inclusion $Conc(\mathbf{H}) \hookrightarrow \mathbf{H}$.

It also has all $\kappa$-bounded $(\infty,1)$-colimits (computed in $\mathbf{H}$ and reflected back into $\mathcal{G}$), hence is an [[idempotent complete (∞,1)-category]].

A covering family in $\mathcal{G}$ goes to an effective epimorphism by definition. Effective epimorphisms are stable under pullback in $\mathcal{G}$ because that pullback coincides with the pullback in $\mathbf{H}$ where the statement holds due to [[universal colimits]] of the $(\infty,1)$-topos.

=--

+-- {: .un_def}
###### Definition


For every object $X \in \mathbf{H}$ define the functor

$$
  \mathcal{O}_X : \mathcal{G} \hookrightarrow \mathbf{H}
   \stackrel{X^*}{\to} \mathbf{H}/X
$$

from $\mathcal{G}$ to the [[over-(∞,1)-topos]] over $X$, where $X^*$ is the [[inverse image]] functor of the corresponding [[étale geometric morphism]].

=--

+-- {: .un_lemma}
###### Observation

This makes $\mathbf{H}/X$ a $\mathcal{G}$-[[structured (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Since $X^*$, being an inverse image, preserves finite limits and since it preserves effective epimorphisms, by [[universal colimits]].

=--


### $\infty$-Groups {#InfinGroups}

Every [[(∞,1)-category]] with [[(∞,1)-limit]]s comes with its notion of [[loop space object]]. A [[connected]] object in $\mathbf{H}$ we write $\mathbf{B}G$. Its [[loop space object]]

$$
  G := \Omega \mathbf{B}G
$$

defined as the [[(∞,1)-pullback]]


$$
  \array{
    G &\to& *
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
$$

is the [[∞-group]] of which $\mathbf{B}G$ is the [[delooping]] object.


### Cohomology and principal $\infty$-bundles {#Cohomology}

There is an intrinsic notion of [[cohomology]] and 
of [[principal ∞-bundles]] in any [[(∞,1)-topos]] $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $X,A \in \mathbf{H}$ two [[object]]s, we say that

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
$$

is the **[[cohomology]] set** of $X$ with coefficients in $A$. If $A = G$ is an  [[∞-group]] we write

$$
  H^1(X,G) := \pi_0 \mathbf{H}(X, \mathbf{B}G)
$$

for cohomology with coefficients in its [[delooping]]. Generally, if  $K \in \mathbf{H}$ has a $p$-fold [[delooping]], we write

$$
  H^p(X,K) := \pi_0 \mathbf{H}(X, \mathbf{B}^p K)
  \,.
$$

=--

In the context of cohomology on $X$ with coefficients in $A$ we we say that

* the hom-space $\mathbf{H}(X,A)$ is the **cocycle $\infty$-groupoid**;

* a [[morphism]] $g : X \to A$ is a [[cocycle]];

* a [[2-morphism]] : $g \Rightarrow h$ is a [[coboundary]] between cocycles.

* a morphism $c : A \to B$ represents the [[characteristic class]]

  $$
    [c] : H(-,A) \to H(-,B)
    \,.
  $$


+-- {: .un_def}
###### Definition


For every morphism $c : \mathbf{B}G \to \mathbf{B}H \in \mathbf{H}$ define the **long [[fiber sequence]] to the left**

$$
   \cdots 
   \to 
   \Omega G
  \to 
  \Omega H 
   \to 
   F
    \to 
   G 
     \to  
   H 
     \to 
    \mathbf{B} F 
     \to 
    \mathbf{B}G
      \stackrel{c}{\to} 
   \mathbf{B}H
$$

to be the given by the consecutive [[pasting]] diagrams of [[(∞,1)-pullback]]s

$$
  \array{
      \vdots && \vdots
      \\
      \Omega H &\to& G &\to& *
      \\
      \downarrow &&\downarrow && \downarrow 
      \\
     * &\to& H &\to& \mathbf{B}F &\to& *
      \\
     &&\downarrow && \downarrow && \downarrow
     \\
     && * &\to& \mathbf{B}G & \stackrel{c}{\to} & \mathbf{B}H
  }
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

* The long fiber sequence to the left of $c : \mathbf{B}G \to \mathbf{B}H$ becomes constant on the point after $n$ iterations if $H$ is $n$-[[truncated]]. 


* For every object $X \in \mathbf{H}$ we have a long [[exact sequence]] of [[pointed set]]s


  $$  
    \cdots \to H^0(X,G) \to H^0(X,H) \to H^1(X,F) \to H^1(X,G) \to H^1(X,H)
   \,.
  $$

=--

+-- {: .proof}
###### Proof

The first statement follows from the observation that a 
[[loop space object]] $\Omega_x A$ is a fiber of the [[free loop space object]] $\mathcal{L} A$
and that this may equivalently be computed by the 
[[(∞,1)-powering]] $A^{S^1}$, where $S^1 \in Top \simeq \infty Grpd$ is the [[circle]]. (See [[Hochschild cohomology]] for details.)

The second statement follows by observing that the 
$\infty$-hom-functor $\mathbf{H}(X,-)$ preserves all 
[[(∞,1)-limit]]s, so that we have [[(∞,1)-pullback]]s

$$ 
  \array{
    \mathbf{H}(X,F) &\to &*
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,G) &\to& \mathbf{H}(X,H)
  }
$$

etc. in [[∞Grpd]] at each stage of the fiber sequence. The statement then follows with the familiar [[long exact sequence]] for [[homotopy group]]s in [[Top]] $\simeq$ [[∞Grpd]].

=--

To every cocycle $g : X \to \mathbf{B}G$ is canonically associated its [[homotopy fiber]] $P \to X$, the [[(∞,1)-pullback]]

$$
  \array{
    P &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
    \,.
  }
  \,.
$$

We discuss now that $P$ canonically has the structure of a $G$-[[principal ∞-bundle]] and that $\mathbf{B}G$ is the [[fine moduli space]] for $G$-principal $\infty$-bundles.


+-- {: .un_defn}
###### Definition
**(principal $G$-action)**

Let $G$ be a [[groupoid object in an (∞,1)-category|group object in the (∞,1)-topos]] $\mathbf{H}$. A **principal [[action]]** of $G$ on an object $P \in \mathbf{H}$ is 
a [[groupoid object in an (∞,1)-category|groupoid object in the (∞,1)-topos]] $P//G$ that sits over $*//G$ in that we have a 
  morphism of [[simplicial object|simplicial diagram]]s $\Delta^{op} \to \mathbf{H}$

$$
  \array{
    \vdots && \vdots
    \\
    P \times G \times G
    &\stackrel{(p_2, p_3)}{\to}& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{}{\to}& {*}
  }
$$

in $\mathbf{H}$.

We say that the [[(∞,1)-colimit]]

$$
  X : \lim_\to (P//G : \Delta^{op} \to \mathbf{H})
$$

is the **base space** defined by this action.

=--

We may think of $P//G$ as the **[[action groupoid]]** of the $G$-action on $P$. For us it _defines_ this $G$-action.


+-- {: .un_prop}
###### Proposition

The $G$-principal action as defined above satisfies the 
**principality condition** in that we have an equivalence of
groupoid objects

 $$
   \array{
     \vdots && \vdots
     \\
     P \times_X P \times_X P
     &\stackrel{\simeq}{\to}& 
     P \times G \times G
     \\
    \downarrow\downarrow\downarrow 
     && \downarrow\downarrow\downarrow
     \\
     P \times_X P
     &\stackrel{\simeq}{\to}& 
     P \times G
     \\
     \downarrow\downarrow && \downarrow\downarrow
     \\
     P &\stackrel{\simeq}{\to}& P
   }
   \,.
 $$

=--

+-- {: .proof}
###### Proof

This principality condition asserts that the groupoid object $P//G$ is [[groupoid object in an (infinity,1)-category|effective]]. By [[(∞,1)-topos|Giraud's axioms characterizing (∞,1)-toposes]], every groupoid object in $\mathbf{H}$ is effective.

=--


+-- {: .un_prop}
###### Proposition

For $X \to \mathbf{B}G$ any morphism, its [[homotopy fiber]] $P \to X$
is canonically equipped with a principal $G$-action with base space $X$.

=--

+-- {: .proof}
###### Proof

By the above we need to show that we have a morphism of simplicial diagrams

$$
  \array{
    \vdots && \vdots && \vdots
    \\
    P \times_X P \times_X P 
    &\stackrel{\simeq}{\to}& P \times G \times G
    &\to& G \times G
    \\
    \downarrow\downarrow\downarrow
    && 
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times_X P &\stackrel{\simeq}{\to}& P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow
    && \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{=}{\to}& P &\stackrel{}{\to}& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\stackrel{=}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,,
$$

where the left horizontal morphisms are equivalences, as indicated. We proceed by induction through on the height of this diagram.

The defining [[(∞,1)-pullback]] square for $P \times_X P$ is 

$$
  \array{
    P \times_X P &\to& P
    \\
    \downarrow && \downarrow
    \\
    P &\to& X
  }
$$

To compute this, we may attach the defining $(\infty,1)$-pullback square of $P$ to obtain the [[pasting]] diagram

$$
  \array{
    P \times_X P &\to& P &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P &\to& X &\to& \mathbf{B}G
    \,.
  }
$$

and use the [pasting law for pullbacks](http://ncatlab.org/nlab/show/pullback#Pasting), to conclude that $P \times_X P$ is the pullback

$$
  \array{
    P \times_X P &\to& &\to& {*}
    \\
    \downarrow && && \downarrow
    \\
    P &\to& X &\to& \mathbf{B}G
    \,.
  }
$$

By defnition of $P$ as the homotopy fiber of $X \to \mathbf{B}G$, the lower horizontal morphism is equivalent to $P \to {*} \to \mathbf{B}G$, so that $P \times_X P$ is equivalent to the pullback

$$
  \array{
    P \times_X P &\to& &\to& {*}
    \\
    \downarrow && && \downarrow
    \\
    P &\to& {*} &\to& \mathbf{B}G
    \,.
  }
$$

This finally may be computed as the pasting of two pullbacks

$$
  \array{
    P \times_X P &\simeq& P \times G &\to& G &\to& {*}
    \\
    &&\downarrow && \downarrow && \downarrow
    \\
    &&P &\to& {*} &\to& \mathbf{B}G
    \,.
  }
$$

of which the one on the right is the defining one for $G$ and the remaining one on the left is just an [[(∞,1)-product]].  

Proceeding by induction from this case we find analogousy that $P^{\times_X^{n+1}} \simeq P \times G^{\times_n}$: suppose this has been shown for $(n-1)$, then the defining pullback square for $P^{\times_X^{n+1}}$ is

$$
  \array{
    P \times_X P^{\times_X^n}
    &\to&
    P
    \\
    \downarrow && \downarrow
    \\
    P^{\times_X^n}&\to& X
  }
  \,.
$$

We may again paste this to obtain

$$
  \array{
    P \times_X P^{\times_X^n}
    &\to&
    P
    &\to&
    *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P^{\times_X^n}&\to& X &\to& \mathbf{B}G
  }
$$

and use from the previous induction step that

$$
  (P^{\times_X^n} \to X \to \mathbf{B}G) 
  \simeq
  (P^{\times_X^n} \to * \to \mathbf{B}G)
$$

to conclude the induction step with the same arguments as before.


=--

+-- {: .un_defn}
###### Definition

We say a $G$-principal action of $G$ on $P$ over $X$ is a 
$G$-[[principal ∞-bundle]] if the colimit over $P//G \to *//G$
produces a pullback square: the bottom square in 


$$
  \array{
    \vdots && \vdots
    \\
    P \times G \times G
    &\to& G \times G
    \\
   \downarrow\downarrow\downarrow 
    && \downarrow\downarrow\downarrow
    \\
    P \times G
    &\stackrel{p_2}{\to}& G
    \\
    \downarrow\downarrow && \downarrow\downarrow
    \\
    P &\stackrel{}{\to}& {*}
    \\
    \downarrow && \downarrow
    \\
    X = \lim_\to (P \times G^\bullet) &\stackrel{g}{\to}& 
   \mathbf{B}G = \lim_\to( G^\bullet)
  }
  \,.
$$


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



### Geometric homotopy and Galois theory {#Homotopy}

We discuss canonical internal realizations of the notions of [[homotopy group]], [[local system]] and [[Galois theory]] in $\mathbf{H}$.


+-- {: .un_defn}
###### Definition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]] and $X \in \mathbf{H}$ an [[object]], we call $\Pi X \in $ [[∞Grpd]] the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] of $X$. The ([[categorical homotopy groups in an (∞,1)-topos|categorical]]) [[homotopy group]]s of $\Pi(X)$ we call the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of $X$

$$
  \pi_\bullet^{geom}(X) := \pi_\bullet(\Pi (X))
  \,.
$$

=--


+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]], also all its objects $X \in \mathbf{H}$ are locally $\infty$-connected, in the sense  their [[petit topos|petit]] [[over-(∞,1)-toposes]] $\mathbf{H}/X$ are locally $\infty$-connected.

The two notions of fundamental $\infty$-groupoids of $X$ induced this way do agree, in that there is a natural equivalence

$$
  \Pi_X(X \in \mathbf{H}/X) \simeq \Pi(X \in \mathbf{H})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the general facts recalled at [[étale geometric morphism]] we have a composite [[essential geometric morphism]]

$$
  (\Pi_X \dashv \Delta_X \dashv \Gamma_X) : 
  \mathbf{H}_{/X}
   \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{\X_*}{\to}}}
  \mathbf{H}
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}  
   \infty Grpd
$$

and $X_!$ is given by sending $(Y \to X) \in \mathbf{H}/X$ to $Y \in \mathbf{H}$.

=--


+-- {: .un_def}
###### Definition

For $\kappa$ a [[regular cardinal]] write 

$$
  Core \infty Grpd_\kappa \in \infty Grpd
$$ 

for the [[∞-groupoid]] of $\kappa$-[[small (∞,1)-category|small ∞-groupoid]]s: the [[core]] of the full [[sub-(∞,1)-category]] of [[∞Grpd]] on the $\kappa$-small ones.

=--

+-- {: .un_remark}
###### Remark

We have 

$$
  Core \infty Grpd_\kappa \simeq
  \coprod_i \mathbf{B} Aut(F_i)
  \,,
$$

where the coproduct ranges over all $\kappa$-small [[homotopy type]]s $[F_i]$ and $Aut(F_i)$ is the [[automorphism ∞-group]] of any representative $F_i$ of $[F_i]$.

=--

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ write

$$
  LConst(X) := \mathbf{H}(X, Disc Core \infty Grpd_\kappa)
  \,.
$$

We call this the $\infty$-groupoid of **[[locally constant ∞-stack]]s** on $X$.

=--

+-- {: .un_observation}
###### Observation

Since $Disc$ is [[left adjoint]] and [[right adjoint]] it commutes with [[coproduct]]s and with [[delooping]] and therefore

$$
  Disc Core \infty Grpd_\kappa 
    \simeq 
  \coprod_i \mathbf{B} Disc Aut(F_i)
  \,.
$$

Therefore a cocycle $P \in LConst(X)$ may be identified on each geometric connected component of $X$ as a  $Disc Aut(F_i)$-[[principal ∞-bundle]] $P \to X$ over $X$ for the [[∞-group]] object  $Disc Aut(F_i) \in \mathbf{H}$. We may think of this as an object $P \in \mathbf{H}/X$ in the [[little topos]] over $X$. This way the objects of $LConst(X)$ are  indeed identified $\infty$-stacks over $X$.

=--


The following proposition says that the central statements of [[Galois theory]] hold for these canonical notions of geometric homotopy groups and locally constant $\infty$-stacks.

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos|∞-connected]], we have

* a natural equivalence 

  $$
    LConst(X) \simeq \infty \mathrm{Grpd}(\Pi(X), \infty Grpd_\kappa)
  $$

  of locally constant $\infty$-stacks on $X$ with $\infty$-[[permutation representation]]s of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] of $X$ ([[local system]]s on $X$);

* for every point $x : * \to X$ a natural equivalence of the endomorphisms of the fiber functor $x^*$ and the [[loop space]] of $\Pi(X)$ at $x$

  $$
    End( x^* : LConst(X) \to \infty Grpd ) \simeq \Omega_x \Pi(X)
    \,.
  $$

=--

+-- {: .proof}
###### Proof

The first statement is just the adjunction $(\Pi \dashv Disc)$.

$$
  \begin{aligned}
     LConst(X) & := \mathbf{H}(X, Disc Core \infty Grpd_\kappa)
     \\
     &  \simeq \infty Grpd(\Pi(X), Core \infty Grpd_\kappa)
     \\
     &  \simeq \infty Grpd(\Pi(X), \infty Grpd_\kappa)     
  \end{aligned}
  \,.
$$


Using this and that $\Pi$ preserves the 
[[terminal object in an (∞,1)-category|terminal object]], so that the [[adjunct]] of
$(* \to X \to Disc Core \infty Grpd_\kappa)$ is
$(* \to \Pi(X) \to \infty Grpd_\kappa)$
the second statement follows with an iterated application of the [[(∞,1)-Yoneda lemma]] (this is pure [[Tannaka duality]] as discussed there):

The fiber functor $x^* : Func(\Pi(X), \infty Grpd) \to \infty Grpd$ evaluates an $(\infty,1)$-presheaf on $\Pi(X)^{op}$ at $x \in \Pi(X)$. By the [[(∞,1)-Yoneda lemma]] this is the same as homming out of $j(x)$, where $j : \Pi(X)^{op} \to Func(\Pi(X), \infty Grpd)$ is the [[(∞,1)-Yoneda embedding]]:

$$
  x^* \simeq Hom_{PSh(\Pi(X)^{op})}(j(x), -)
  \,.
$$

This means that $x^*$ itself is a representable object in $PSh(PSh(\Pi(X)^{op})^{op})$. If we denote by $\tilde j : PSh(\Pi(X)^{op})^{op} \to PSh(PSh(\Pi(X)^{op})^{op})$ the corresponding Yoneda embedding, then 

$$
  x^* \simeq \tilde j (j (x))
  \,.
$$

With this, we compute the endomorphisms of $x^*$ by applying the [[(∞,1)-Yoneda lemma]] two more times:

$$
  \begin{aligned}
    End x^*
     & \simeq
    End_{PSh(PSh(\Pi(X)^{op})^{op})} (\tilde j(j (x)))
     \\
     & \simeq
     End(PSh(\Pi(X))^{op}) (j(x))
     \\
     & \simeq
     End_{\Pi(X)^{op}}(x,x)
    \\
     & \simeq
     Aut_x \Pi(X)
    \\
     & =: \Omega_x \Pi(X)
  \end{aligned}
   \,.
$$

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

Then the [[fundamental ∞-groupoid]] of $X$ is computed as the $(\infty,1)$-colimit

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




### Paths and geometric Postnikov towers {#Paths}

The [above](#Homotopy) construction of the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] of objects in $\mathbf{H}$ as an object in  [[∞Grpd]] may be reflected back into $\mathbf{H}$, where it gives a notion of homotopy [[path n-groupoid]]s and a geometric notion of [[Postnikov tower]]s of objects in $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]]
define the composite [[adjoint (∞,1)-functor]]s

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat}) 
  :=
  (Disc \Pi \dashv Disc \Gamma)
  : 
  \mathbf{H}
   \to 
  \mathbf{H}
  \,.
$$

=--


We say

* $\mathbf{\Pi}(X)$ is the **path $\infty$-groupoid** of $X$ -- the reflection of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] back into the cohesive context of $\mathbf{H}$;

* $\mathbf{\flat} A$ ("flat $A$") is the coefficient object for 
  **[flat differential A-cohomology](#FlatDifferentialCohomology)** 
  or for $A$-[[local system]]s

Write

$$
  (\tau_n \dashv i_n)
  :
  \mathbf{H}_{\leq n}
  \stackrel{\overset{\tau_{n}}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  \mathbf{H}
$$

for the [[reflective sub-(∞,1)-category]] of [[truncated|n-truncated object]]s and 

$$
  \mathbf{\tau}_n : 
    \mathbf{H} \stackrel{\tau_n}{\to} \mathbf{H}_{\leq n}
  \hookrightarrow
  \mathbf{H}
$$

for the truncation-[[localization of an (∞,1)-category|localization]] funtor. 

We say

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\Pi}_n}{\to}
   \mathbf{H} \stackrel{\mathbf{\tau}_n}{\to}
  \mathbf{H}
$$

is the **homotopy [[path n-groupoid]]** functor. 


$$
  (\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma}) 
  :=
  (Disc \Pi \dashv Disc \Gamma \dashv CoDisc \Gamma)
  : 
  \mathbf{H}
   \to 
  \mathbf{H}
  \,.
$$

+-- {: .un_lemma}
###### Observation

If $\mathbf{H}$ is cohesive, then $\mathbf{\flat}$ has a [[right adjoint]] $\mathbf{\Gamma}$

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma}) 
  :=
  (Disc \Pi \dashv Disc \Gamma \dashv coDisc \Gamma)
  : 
  \mathbf{H}
     \stackrel{\overset{\mathbf{\Pi}}{\to}}{\stackrel{\overset{\mathbf{\flat}}{\leftarrow}}{\underset{\mathbf{\Gamma}}{\to}}}
  \mathbf{H}
  \,.
$$

and this makes $\mathbf{H}$ be $\infty$-connected and locally $\infty$-connected over itself.

=--

+-- {: .un_def}
###### Proposition

Let $\mathbf{H}$ be a [[locally ∞-connected (∞,1)-topos]]. If $X \in \mathbf{H}$ is [[small-projective]] then the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is 

1. [[locally ∞-connected (∞,1)-topos|locally ∞-connected]];

1. [[local (∞,1)-topos|local]].


=--

+-- {: .proof}
###### Proof

The first statement is proven at [[locally ∞-connected (∞,1)-topos]], the second at [[local (∞,1)-topos]].

=--

+-- {: .un_def}
###### Proposition

In a cohesive $(\infty,1)$-topos $\mathbf{H}$, if $X$ is 
[[small-projective]] then so is its path ∞-groupoid $\mathbf{\Pi}(X)$.

=--

+-- {: .proof}
###### Proof

Because of the triple of [[adjoint (∞,1)-functor]]s 
$(\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma})$ we have for [[diagram]] $A : I \to \mathbf{H}$ that

$$
  \begin{aligned}
     \mathbf{H}(\mathbf{\Pi}(X), {\lim_\to}_i A_i)
     & \simeq 
     \mathbf{H}(X, \mathbf{\flat}{\lim_\to}_i A_i)
    \\
     & \simeq 
     \mathbf{H}(X, {\lim_\to}_i \mathbf{\flat} A_i)
     \\
     & \simeq 
     {\lim_\to}_i \mathbf{H}(X,  \mathbf{\flat} A_i)
  \end{aligned}
  \,,
$$ 

where in the last step we used that $X$ is [[small-projective]] by assumption.

=--



+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ we say that the **geometric Postnikov tower**
of $X$ is the [[Postnikov tower in an (∞,1)-category]] of $\mathbf{\Pi}(X)$:

$$
  \mathbf{\Pi}(X) \to \cdots
   \to 
   \mathbf{\Pi}_2(X) \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)
  \,.
$$

=--

### Universal coverings and geometric Whitehead towers {#Coverings}

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ an object,

The **geometric [[Whitehead tower in an (∞,1)-topos|Whitehead tower]]** of $X$ is the sequence of objects 

$$
  * \to \cdots \to X^{(2)} \to X^{(1)} \to X^{(0)} \simeq X
$$

in $\mathbf{H}$, where for each $n \in \mathbb{N}$ the object $X^{(n+1)}$ is the [[homotopy fiber]] of the canonical morphism $X \to \mathbf{\Pi}_{n+1} X$ to the [path n+1-groupoid](#Paths) of $X$. This is the object defined by the [[(∞,1)-pullback]] diagram

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

We call $X^{(n+1)}$ the $(n+1)$-fold 
**[[universal covering space]]** of $X$.

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

For $\mathbf{H}$ the cohesive $(\infty,1)$-topos over an 
[[∞-cohesive site]] we have
that 

$$
  \mathbf{\Pi}_n(X) \simeq Disc \tau_{\leq n} \Pi(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows from $\mathbf{\tau}_{\leq n} LConst \Pi(X) \simeq LConst \tau_{\leq n} \Pi(X)$. This, in turn, can for instance be checked in terms of the [[model structure on simplicial presheaves]], using that $\tau$ is objectwise the [[coskeleton]] operation. More on that at [[Postnikov tower in an (∞,1)-category]].

=--

+-- {: .un_remark}
###### Remark


Therefore commuting diagram

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

in [[∞Grpd]]. This being universal means that $\Pi(X^{(n)})$ is $n$-[[connected]] and universal with that property as an object over $\Pi(X)$.

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








### Flat $\infty$-connections and local systems {#FlatDifferentialCohomology}

We describe for a [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ a canonical intrinsic notion of _flat_ [[connections on ∞-bundles]], _flat_ [[higher parallel transport]] and higher [[local system]]s.

Write $(\mathbf{\Pi} \dashv\mathbf{\flat}) := (Disc \Pi \dashv Disc \Gamma) : \mathbf{H} \to \mathbf{H}$ for the adjunction given by the [path ∞-groupoid](#Paths). Notice that this comes with the canonical $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]] with components

$$
  X \to \mathbf{\Pi}(X)
$$

and the $(Disc \dashv \Gamma)$-counit with components

$$
  \mathbf{\flat} A \to A
  \,.
$$

+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}$ we write

$$
  \mathbf{H}_{flat}(X,A) := \mathbf{H}(\mathbf{\Pi}X, A)
$$

and call $H_{flat}(X,A) := \pi_0 \mathbf{H}_{flat}(X,A)$ the **flat (nonabelian) differential cohomology** of $X$ with coefficients in $A$.

We say a morphism $\nabla : \mathbf{\Pi}(X) \to A$ is a **flat [[connection on an ∞-bundle|∞-connnection]] on the [[principal ∞-bundle]] corresponding to $X \to \mathbf{\Pi}(X) \stackrel{\nabla}{\to} A$, or an **$A$-[[local system]]** on $X$.

The induced morphism

$$
  \mathbf{H}_{flat}(X,A) \to \mathbf{H}(X,A)
$$

we say is the [[forgetful functor]] that forgets flat connections.


=--

+-- {: .un_remark}
###### Remark

The object $\mathbf{\Pi}(X)$ has the interpretation of the [path ∞-groupoid](#Paths) of $X$: it is a cohesive $\infty$-groupoid whose [[k-morphism]]s may be thought of as generated from the $k$-morphisms in $X$ and $k$-dimensional cohesive paths in $X$.

Accordingly a mophism $\mathbf{Pi}(X) \to A$ may be thought of as assigning

* to each point of $X$ a fiber in $A$;

* to each path in $X$ an equivalence between these fibers;

* to each disk in $X$ a  2-equivalalence between these equivaleces associated to its boundary

* and so on.

This we think of as encoding a flat [[higher parallel transport]] on $X$, coming from some flat $\infty$-connection and _defining_ this flat $\infty$-connection.

=--

+-- {: .un_lemma}
###### Observation


By the $(\mathbf{\Pi} \dashv \mathbf{\flat})$-adjunction we have a [[natural transformation|natural]] equivalence

$$
  \mathbf{H}_{flat}(X,A) \simeq \mathbf{H}(X,\mathbf{\flat}A)
  \,.
$$

A [[cocycle]] $g : X \to A$ for a [[principal ∞-bundle]] on $X$ is in the image of 

$$
  \mathbf{H}_{flat}(X,A) \to \mathbf{H}(X,A)
$$

precisely if there is a lift $\nabla$ in the [[diagram]]

$$
  \array{
     \mathbf{\flat}A 
     \\
     & {}^{\nabla}\nearrow& \downarrow
    \\
    \mathbf{\Pi}(X) &\sgtackrel{g}{\to}& A
  }
  \,.
$$

=--

We call $\mathbf{\flat}A$ the **coefficient object for flat $A$-connections**. 



### de Rham cohomology {#deRhamCohomology}

In every [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ there is an intrinsic notion of [[nonabelian cohomology|nonabelian]] [[de Rham cohomology]].

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ an object, write $\mathbf{\Pi}_{dR}X$
for the [[(∞,1)-colimit|(∞,1)-pushout]]

$$
  \array{
    X &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}(X) &\to& \mathbf{\Pi}_{dR}X
  }
  \,.
$$

For $* \to A$ any [[pointed object]] in $\mathbf{H}$, write 
$\mathbf{\flat}_{dR} A$ for the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{\flat}_{dR} A &\to& \mathbf{\flat} A 
    \\
    \downarrow && \downarrow
    \\
    * &\to& A
  }
  \,.
$$


=--

+-- {: .un_prop #DeRhamAdjunction}
###### Proposition

This construction yields a pair of [[adjoint (∞,1)-functor]]s 

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} )
  : 
  */\mathbf{H}
  \stackrel{
     \overset{\mathbf{\Pi}_{dR}}{\leftarrow}
   }{
     \underset{\mathbf{\flat}_{dR}}{\to}
   }
  \mathbf{H}
  \,.
$$


=--

+-- {: .proof}
###### Proof

We check the defining natural hom-equivalence

$$
  {*}/\mathbf{H}(\mathbf{\Pi}_{dR}X,A)
  \simeq
  \mathbf{H}(X, \mathbf{\flat}_{dR}A)
  \,.
$$

The hom-space in the [[over-(∞,1)-category|under-(∞,1)-category]] $*/\mathbf{H}$ is (as discussed there), computed by the [[(∞,1)-pullback]]

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
     \mathbf{H}(\mathbf{\Pi}_{dR}X, A)
     \\
     \downarrow && \downarrow
     \\
     * &\stackrel{pt_A}{\to}& \mathbf{H}(*,A)
  }
  \,.
$$

By the fact that the [[hom-functor]] : $\mathbf{H}(-,-) : \mathbf{H}^{op} \times \mathbf{H} \to \infty Grpd $ preserves limits in both arguments we have a natural equivalence

$$
  \begin{aligned}
     \mathbf{H}(\mathbf{\Pi}_{dR} X, A)
     & :=
     \mathbf{H}( *\coprod_{X} \mathbf{\Pi}(X), A  )     
     \\
     & \simeq 
     \mathbf{H}(*,A) \prod_{\mathbf{H}(X,A)} 
      \mathbf{H}(\mathbf{\Pi}(X),A)
  \end{aligned}
  \,.
$$

We paste this pullback to the above pullback diagram to obtain

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
     \mathbf{H}(\mathbf{\Pi}_{dR}X, A) &\to&
      \mathbf{H}(\mathbf{\Pi}(X),A)
     \\
     \downarrow && \downarrow  && \downarrow
     \\
     * &\stackrel{pt_A}{\to}& \mathbf{H}(*,A)
     &\to& 
      \mathbf{H}(X,A)
  }
  \,.
$$

By the pasting law for [[(∞,1)-pullback]]s the outer diagram is still a pullback. We may evidently rewrite the bottom composite as in

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
      &\to&
      \mathbf{H}(\mathbf{\Pi}(X),A)
     \\
     \downarrow && && \downarrow
     \\
     * &\stackrel{\simeq}{\to}& \mathbf{H}(X,*)
     &\stackrel{(pt_A)_*}{\to}& 
      \mathbf{H}(X,A)
  }
  \,.
$$

This exhibits the hom-space as the pullback

$$
  \begin{aligned}
    */\mathbf{H}(\mathbf{\Pi}_{dR}(X),A)
    \simeq
     \mathbf{H}(X,*) \prod_{\mathbf{H}(X,A)} \mathbf{H}(X,\mathbf{\flat} A)
   \end{aligned}
  \,,
$$

where we used the $(\mathbf{\Pi} \dashv \mathbf{\flat})$-adjunction. Now using again that $\mathbf{H}(X,-)$ preserves pullbacks, this is

$$
  \cdots \simeq \mathbf{H}(X, * \prod_A \mathbf{\flat}A )
  \simeq \mathbf{H}(X , \mathbf{\flat}_{dR}A)
  \,.
$$


=--


+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}$ we write

$$
  \mathbf{H}_{dR}(X,A)
  :=
  \mathbf{H}(\mathbf{\Pi}_{dR}X, A)
  \simeq
  \mathbf{H}(X, \mathbf{\flat}_{dR} A)
  \,.
$$

A [[cocycle]] $\omega : X \to \mathbf{\flat}_{dR}A$ we call an **flat $A$-valued differential form** on $X$.

We say that $H_{dR}(X,A) {:=} \pi_0 \mathbf{H}_{dR}(X,A)$
is the **de Rham cohomology** of $X$ with coefficients in $A$.

=--

+-- {: .un_remark}
###### Observation

A [[cocycle]] in de Rham cohomology

$$
  \omega : \mathbf{\Pi}_{dR}X \to A
$$

is precisely a [flat ∞-connetion](#FlatDifferentialCohomology) on a _trivializable_ $A$-principal $\infty$-bundle. More precisely, $\mathbf{H}_{dR}(X,A)$ is the [[homotopy fiber]] of the [[forgetful functor]] from $\infty$-bundles with flat $\infty$-connection to $\infty$-bundles: we have an [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{dR}(X,A) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{flat}(X,A) &\to& \mathbf{H}(X,A)
  }  
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows by the fact that the [[hom-functor]] $\mathbf{H}(X,-)$ preserves the defining [[(∞,1)-pullback]] for $\mathbf{\flat}_{dR} A$.

=--

Just for emphasis, notice the dual description of this situation: by the [[universal property]] of the [[(∞,1)-colimit]] that defines $\mathbf{\Pi}_{dR} X$ we have that $\omega$ corresponds to a diagram

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

+-- {: .un_prop #deRhamWithDiscCoeffsIsTrivial}
###### Proposition

The de Rham cohomology with coefficients in discrete object is trivial: for all $S \in \infty Grpd$ we have

$$
  \mathbf{\flat}_{dR} Disc S \simeq *
  \,.
$$


=--

+-- {: .proof}
###### Proof

Using that in a [[∞-connected (∞,1)-topos]] the functor $Disc$ is a [[full and faithful (∞,1)-functor]] so that the [[unit of an adjunction|unit]] $Id \to \Gamma Disc $ is an [[equivalence in an (∞,1)-category|equivalence]] and using that by the [[zig-zag identity]]  we have then that the [[unit of an adjunction|counit]] 
$\mathbf{\flat} Disc S := Disc \Gamma Disc S \to Disc S$ is also an equivalence, we have


$$
  \begin{aligned}
     \mathbf{\flat}_{dR} Disc S 
     & {:=}
     * \prod_{Disc S} \mathbf{\flat} Disc S
     \\
     & \simeq * \prod_{Disc S} Disc S
     \\
     & \simeq *
  \end{aligned}
  \,,
$$

since the pullback of an euqivalence is an equivalence.

=--

### Concrete objects{#ConcreteObjects}


The cohesive structure on an object in a cohesive 
$(\infty,1)$-topos need not be supported by points. 
We discuss a general abstract characterization of  
objects that do have an interpretation as bare $n$-groupoids 
equipped with cohesive structure.

Compare with the section <a href="http://nlab.mathforge.org/nlab/show/cohesive%20topos#ConcreteObjects">Quasitoposes of concrete objects</a> at [[cohesive topos]].


+-- {: .un_prop}
###### Proposition

On a cohesive $(\infty,1)$-topos $\mathbf{H}$ 
both $\mathrm{Disc}$ and $\mathrm{coDisc}$ 
are [[full and faithful (∞,1)-functor]]s and $\mathrm{coDisc}$ exhibits [[∞Grpd]]  as a sub-$(\infty,1)$-topos of $\mathbf{H}$ by an  
[[(∞,1)-geometric embedding]]

$$
  \infty Grpd
    \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\hookrightarrow}}
  \mathbf{H}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The full and faithfulness of $Disc$ and $coDisc$ follows as
in the discussion at [[∞-connected (∞,1)-topos]],
Since $\Gamma$ is also a right adjoint it preserves 
in particular [[finite limit|finite]] [[(∞,1)-limit]]s, so that
$(\Gamma \dashv \mathrm{coDisc})$ is indeed an 
[[(∞,1)-geometric morphism]]. 
(See the general discussion at [[local (∞,1)-topos]].)



=--

+-- {: .un_prop}
###### Proposition


The [[(∞,1)-topos]] [[∞Grpd]] is equivalent to 
the full [[sub-(∞,1)-category]] of $\mathbf{H}$ on 
those objects $X \in \mathbf{H}$ for which the 
[[unit of an adjunction|counit]]
 
$$
    X \to \mathrm{coDisc}\Gamma X
$$
  
is an [[equivalence in an (∞,1)-category|equivalence]].

=--

+-- {: .proof}
###### Proof

This follows by general facts discussed at [[reflective sub-(∞,1)-category]].

=--

+-- {: .un_def}
###### Definition

We say a 0-[[truncated]] object $X \in \mathbf{H}$ is 
is **concrete** if the [[unit of an adjunction|counit]]

$$
  X \to \mathrm{coDisc} \Gamma X
$$

is a [[monomorphism]]. We say a general object $X$ is 
concrete if all its 
[[categorical homotopy groups in an (∞,1)-topos|categorical homotopy sheaves]] are concrete.

=--

+-- {: .un_prop}
###### Proposition

For $C$ an [[∞-cohesive site]], a 0-truncated object in the 
[[(∞,1)-topos]] over $C$ is concrete prescisely if it is
a [[concrete sheaf]] in the traditional sense.

=--



### Infinitesimal objects {#InfinitesimalObjects}

We characterize objects in a cohesive $(\infty,1)$-topos $\mathbf{H}$ that behave as cohesive $\infty$-groupoids all whose [[k-morphism]]s have [[infinitesimal object|infinitesimal]] extension. These infintesimal [[∞-groupoid]]s may be thought of as [[Lie algebra]]s, [[∞-Lie algebra]]s and generally [[∞-Lie algebroid]]s.

Recall the [[adjoint (∞,1)-functor]]s $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})$ from the discussion of [de Rham cohomology](#deRhamCohomology) above.

+-- {: .un_def}
###### Definition


A [[connected]] object $\mathbf{B}\mathfrak{g} $ in a cohesive $(\infty,1)$-topos $\mathbf{H}$ that is _geometrically contractible_

$$
  \Pi \mathbf{B}\mathfrak{g} \simeq *
$$


we call an **infinitesimal object**. 

Its [[loop space object]] $\mathfrak{g} := \Omega_* \mathbf{B}G$ we call an **[[∞-Lie algebra]]** in $\mathbf{H}$. 

=--

+-- {: .un_remark}
###### Remark

In terms of the extrinsic description at [[Lie integration]] this axiom models objects of the form $\exp(\mathfrak{g}) : U \mapsto Hom(T_{vert} (U \timdes \Delta^\bullet), \mathfrak{g})$ for $\mathfrak{g}$ an [[∞-Lie algebra]] in the explicit algebraic sense. These are indeed all geometrically contractible, since in each degree a contracting homotopy of $\Delta^n$ exhibits a conctraction of the corresponding [[concrete sheaf]] in that degree.

=--


+-- {: .un_def}
###### Definition

Set

$$
  Lie
  := 
  \mathbf{\Pi}_{dR} \circ \mathbf{\flat}_{dR} 
  \,.
$$

=--

+-- {: .un_example}
###### Proposition/Example

For all $X$ the object $\mathbf{\Pi}_{dR}(X)$ is geometrically contractible.

=--

+-- {: .proof}
###### Proof

Since on the [[locally ∞-connected (∞,1)-topos]] and [[∞-connected (∞,1)-topos|∞-connected]] $\mathbf{H}$ the functor $\Pi$ preserves [[(∞,1)-colimit]]s and the [[terminal object in an (∞,1)-category|terminal object]], we have

$$
  \begin{aligned}
    \Pi \mathbf{\Pi}_{dR} X
    & {:=}
     \Pi (*) \coprod_{\Pi X} \Pi \mathbf{\Pi} X
    \\
    & \simeq
      * \coprod_{\Pi X} \Pi Disc \Pi X   
    \\
    & \simeq 
      * \coprod_{\Pi X} \Pi X
    & \simeq
      *
  \end{aligned}
  \,,
$$

where we used that in the [[∞-connected (∞,1)-topos|∞-connected]] $\mathbf{H}$ the functor $Disc$ is[[full and faithful (∞,1)-functor|full and faithful]].

=--

+-- {: .un_corollary}
###### Corollary

We have for every $\mathbf{B}G$ that $Lie \mathbf{B}G$ is geometrically contractible.

=--


We shall write $\mathbf{B}\mathfrak{g}$ for $Lie \mathbf{B}G$, when the context is clear. And say that $\mathfrak{g}$ _is the $\infty$-Lie algebra_ of $G$.


+-- {: .un_prop #LieValuesofDeRham}
###### Proposition


Every [de Rham cocycle](#deRhamCohomology) $\omega : \mathbf{\Pi}_{dR} X \to \mathbf{B}G$ factors through the ∞-Lie algebra of $G$

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

By the <a href="http://ncatlab.org/nlab/show/adjoint+functor#UniversalArrows">universality of the counit</a> of $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})$ we have that $\omega$ factors through the [[unit of an adjunction|counit]9 $FLie \mathbf{B}G \to \mathbf{B}G$. 

=--

Therefore instead of speaking of a $G$-valued de Rham cocycle, it is more accurate to speak of a $\mathfrak{g}$-valued de Rham cocycle. In particular we have the following.

+-- {: .un_prop}
###### Corollary

Every morphism $Lie \mathbf{B}H \to \mathbf{B}G$ from an $\infty$-Lie algebra to an $\infty$-group factors through the $\infty$-Lie algebra of that $\infty$-group

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


+-- {: .un_prop}
###### Proposition

We have 

$$
  Lie \circ Lie \simeq Lie \circ \Sigma \circ \Omega
  \,.
$$

=--

+-- {: .proof}
###### Proof

First observe that for all $A \in */\mathbf{H}$ we have

$$
  \mathbf{\flat} \mathbf{\flat}_{dR} A \simeq *
$$

This follows using

* $\mathbf{\flat}$ is a [[right adjoint]] and hence preserves [[(∞,1)-pullback]]s;

* $\mathbf{\flat} \mathbf{\flat} := Disc \Gamma Disc \Gamma \simeq Disc \Gamma =: \mathbf{\flat}$ by the fact that $Disc$ is a 
  [[full and faithful (∞,1)-functor]]; 

* the counit $\mathbf{\flat} \mathbf{\flat} A \to \mathbf{\flat} A$ is equivalent to the identity, by the [[zig-zag-identity]] of the [[adjunction]] and using that equivalences satisfy [[category with weak equivalences|2-out-of-3]].

by computing

$$
  \begin{aligned}
    \mathbf{\flat} \mathbf{\flat}_{dR} A
    & 
    * \times_{\mathbf{\flat}A} \mathbf{\flat}\mathbf{\flat}A
    \\
    & \simeq 
    * \times_{\mathbf{\flat}A} \mathbf{\flat}A
    \\
    & \simeq *
 \end{aligned} 
 \,,
$$

using that the [[(∞,1)-pullback]] of an [[equivalence in an (∞,1)-category|equivalence]] is an equivalence.


From this we deduce that

$$
  \mathbf{\flat}_{dR} \circ \mathbf{\flat}_{dR} 
  \simeq \mathbf{\flat}_{dR} \circ \Omega
  \,.
$$

by computing for all $A \in \mathbf{H}$

$$
  \begin{aligned}
    \mathbf{\flat}_{dR} \circ \mathbf{\flat}_{dR} A
    & \simeq 
    * \times_{\mathbf{\flat}_{dR} A} \mathbf{\flat}\mathbf{\flat}_{dR} A
    \\
    & \simeq
    * \times_{\mathbf{\flat}_{dR} A} *
    \\
    & \simeq
    \mathbf{\flat}_{dR}( * \times_A * )
    \\
    & \simeq \mathbf{\flat}_{dR} \Omega A
  \end{aligned}
  \,.
$$

Also observe that by a [proposition above](#deRhamWithDiscCoeffsIsTrivial) we have

$$
  \mathbf{\flat}_{dR} \mathbf{\Pi} X \simeq *
$$

for all $X \in \mathbf{H}$.


Finally to obtain $Lie \circLie$ we do one more computation of this sort, using that $Lie := \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR}$ preserves the terminal object (since $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos|∞-connected]]) and is a [[left adjoint]] (with right adjoint given by $\mathbf{\flat}_{dR} \mathbf{\Pi}_{dR}$):

$$
  \begin{aligned}
    Lie Lie A 
    & \simeq 
    Lie \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} A
    \\
    & \simeq
      * 
        \coprod_{Lie \mathbf{\flat}_{dR} A} 
      Lie \mathbf{\Pi} \mathbf{\flat}_{dR} A
    \\
    & \simeq
      * 
        \coprod_{Lie \mathbf{\flat}_{dR} A} 
      \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{\Pi} \mathbf{\flat}_{dR} A
    \\
    & \simeq 
    * \coprod_{Lie \mathbf{\flat}_{dR} A} *    
    \\
    & \simeq 
    * \coprod_{\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{\flat}_{dR} A} *
    \\
    & \simeq 
    * \coprod_{\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \Omega A} *   
    \\
    & \simeq
    * \coprod_{Lie \Omega A} *   
    \\
    & \simeq
    Lie ( * \coprod_{\Omega A} * )
    \\
    & \simeq
    Lie \Sigma \Omega A  
  \end{aligned} 
  \,.
$$

=--



### Maurer-Cartan forms and curvature characteristic forms {#CurvatureCharacteristics}

In the [intrinsic de Rham cohomology](#deRhamCohomology) of a [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos|∞-connected]] there exist canonical cocycles that we may identify with [[Maurer-Cartan form]]s and with [[curvature characteritstic form]]s.

+-- {: .un_def}
###### Definition

For $G \in \mathbf{H}$ an [[∞-group]], write

$$
  \theta : G \to \mathbf{\flat}_{dR} \mathbf{B}\mathfrak{g}
$$

for the $\mathfrak{g}$-[valued](#InfinitesimalObjects) 
de Rham cocycle on $G$ which is induced by the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">(∞,1)-pullback pasting</a>

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


+-- {: .un_def}
###### Definition


For $G = \mathbf{B}^n A$ an [[Eilenberg-MacLane object]], we also write 

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
$$

for the intrinsic Maurer-Cartan form and call this the intrinsic **universal [[curvature characteristic form]]** on $\mathbf{B}^n A$.

=--


### Differential cohomology {#DifferentialCohomology}

In every [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos]] there is an intrinsic notion of [[ordinary differential cohomology]].

+-- {: .un_def }
###### Definition 

For $X \in \mathbf{H}$ and $A \in \mathbf{H}$ an [[∞-group]] write 

$$
  \mathbf{H}_{conn}(X,A)
$$ 

for the [[twisted cohomology]] of $X$ induced by the [curvature characteristic class](#CurvatureCharacteristics) $curv : A \to \mathbf{\flat}_{dR}\mathbf{B}\mathfrak{a}$. This is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{conn}(X,A) &\stackrel{F}{\to}& 
     H_{dR}(X,\mathbf{B}\mathfrak{a})
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    \mathbf{H}(X,A) &\stackrel{curv}{\to}& 
     \mathbf{H}_{dR}(X,\mathbf{B}A)
  }
  \,,
$$

(where the right vertical morphism is any choice of cocycle representative for each cohomology class).

This we call the **[[differential cohomology]]** of $X$ with coefficient in $A$.

For $\nabla \in \mathbf{H}_{conn}(X,A)$ a cocycle, we call

* $F(\nabla) \in H_{dR}(X,\mathbf{B}A)$ the **[[curvature]]** class of $c$;

* $[\eta(\nabla)] \in H(X,A)$ the **class in $A$-cohomology of the underlying [[principal ∞-bundle]]**.

=--


+-- {: .un_lemma}
###### Lemma
**(differential fiber sequence)**


For coefficients $A$ that are $(n+1)$-fold deloopable
Differential cohomology fits into a [[fiber sequence]]

$$
  \mathbf{H}(X, \Omega^{n-1} A)
  \to 
  \cdots
  \to
  \mathbf{H}(X, \Omega A)
  \to
  \mathbf{H}_{dR}(X, A)
  \to 
  \mathbf{H}_{conn}(X, A)
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
    &\to& \mathbf{H}_{conn}(X,A) &\to & H(X, \mathbf{\flat}_{dR} \mathbf{B}A)
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

Since $H(X, \mathbf{\flat}_{dR})(X,\mathbf{\flat}_{dR} \matbf{B}A)$ here is a set, this is te product of pullbacks for each element in the set. But this is empty if the cohomology class is not the trivial one picker by the bottom morphisms, so that this is

$$
  \array{
    \Omega \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}A) &\to& 
     *
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
  0 \to H_{dR}^n(X,K)/H^{n-1}(X,K) \to H_{conn}^n(X,K) \to H^n(X,K)
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
  H_{conn}(X, A)
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
  H_{conn}^n(X, K)
  \to
  H^n(X, K)
  \,.
$$

Moreover observing that by construction the last morphism $H_{conn}^n(X,K) \to H^n(X,K)$ is surjective (because in the defining $(\infty,1)$-pullback for $\mathbf{H}_{conn}$ the right vertical morphism is evidently surjective on connected components) this yields the short exact sequence as claimed.

=--

+-- {: .un_remark}
###### Remark

This is _essentially_ verbatim the expected short exact sequence familiar from ordinary generalized [[differential cohomology]] only up to the following slight nuances in notation:

1.  The cohomology groups of the short exact sequence above denote the groups obtained in the given [[(∞,1)-topos]] $\mathbf{H}$, not in [[Top]]. Notably for $\mathbf{H} = $ [[?LieGrpd]] and $|X| \in Top$ the geometric realization of a paracompact manifold $X$, we have that $H^1(X,U(1))$ above is $H^2_{sing}(|X|,\mathbb{Z})$ and not $H^1_{sing}(|X|,U(1))$. 

1. The fact that on the left  of the short exact sequence we find the intrinsic de Rham cohomology set $H_{dR}^n(X,A)$ instead of something like the set of all flat forms as familiar from discussions of ordinary generalized [[differential cohomology]] is due to the fact that, following the general abstract procedure of [[twisted cohomology]], we defined $\mathbf{H}_{conn}(X,A)$ as the $(\infty,1)$-pullback of the inclusion $H(X,\mathbf{\flat}_{dR}A ) \to \mathbf{H}(X,\mathbf{\flat}_{dR} A)$ of the set of connected components of curvature classes into the [[cocycle]] [[∞-groupoid]]. This is the only natural thing to do in a fully natural [[(∞,1)-category|(∞,1)-categorical setup]]. However, in applications we typically have a concrete model for the [[∞-groupoid]] $\mathbf{H}(X,\mathbf{\flat}_{dR} A)$ in mind, and then can consider the inclusion $\mathbf{H}(X,\mathbf{\flat}_{dR} A)_0 \hookrightarrow \mathbf{H}(X,\mathbf{\flat}_{dR} A)$ of all of its objects. While this does not make intrinsic sense -- it is a bit [[evil]] -- , this is what is effectively done in ordinary generalized [[differential cohomology]], and doing so in our definition changes the above short exact sequence slightly to become exactly the familiar sequence, for the suitable special cases.

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
    \mathbf{H}_{conn}(X, \mathbf{B}G) &\to& \prod_{\mathbf{c}_i} \mathbf{H}_{conn}(X,\mathbf{B}^{n_i+1} K)
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
  \mathbf{H}_{conn}(X, \mathbf{B}^{n+1}K)
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
  \mathbf{H}_{conn}(\Sigma, \mathbf{B}^{n} \mathbb{R}/\mathbb{Z})
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
  \mathbf{H}_{conn}(\Sigma, \mathbf{B}^n U(1))
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

(This is due to an observation by [[Domenico Fiorenza]]. See [[higher parallel transport]].)

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


### Classes of examples

+-- {: .un_prop}
###### Proposition

For $C$ an [[∞-cohesive site] [[(∞,1)-category of (∞,1)-sheaves]] $(\infty,1)Sh(C)$ over $C$ is a cohesive $(\infty,1)$-topos.

=--

See [[∞-cohesive site]].

+-- {: .un_prop}
###### Proposition

Examples of $(\infty,1)$-cohesive sites are

* any category with finite [[product]]s and equipped with the trivial [[coverage]].

* the [[full subcategory]] $TopBalls \subset$ [[Top]] on [[open ball]]s with the [[good open cover]] [[coverage]];

* the site [[CartSp]] of [[Cartesian space]]s with [[smooth function]]s between them and [[good open cover]] [[coverage]].

* the [[Cahiers topos]]-site [[ThCartSp]] of infinitesimally thickened Cartesian spaces.

=--

This proposition implies the examples of cohesive $(\infty,1)$-toposes listed in the following.

+-- {: .un_prop}
###### Proposition

Let $(\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : \mathbf{H} \to \infty Grpd$ be a cohesive $(\infty,1)$-topos. Let $X \in \mathbf{H}$ be an object such that 

* $X$ is geometrically contractible: $\Pi (X) \simeq *$;

* $X$ is [[small-projective]].

Then the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]], [[∞-connected (∞,1)-topos|∞-connected]], and [[local (∞,1)-topos|loca]].

=--

+-- {: .proof}
###### Proof

That $\mathbf{H}$ is locally $\infty$-connected and $\infty$-connected follows directly from general properties of the [[étale geometric morphism]]s $\mathbf{H}/X \to \mathbf{H}$, see [[∞-connected (∞,1)-topos]].

Locality follows as in the discussion at [[local (∞,1)-topos]].

=--

### Continuous $\infty$-groupoids

The cohesive $(\infty,1)$-topos $(\infty,1)Sh(TopBalls)$ is that of [[topological ∞-groupoid]]s.

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




### Smooth $\infty$-groupoids

The cohesive $(\infty,1)$-topos $(\infty,1)Sh(CartSp)$ is that of [[smooth ∞-groupoid]]s.

The 0-[[truncated]] [[concrete (∞,1)-sheaf|concrete]] objects in this are precisely the [[diffeological space]]s. Accordingly the general [[concrete (∞,1)-sheaves]] here we may think of as **diffeological $\infty$-groupoids**.

+-- {: .un_prop}
###### Proposition

On $\mathbf{H} = $ [[?LieGrpd]] and $G \in \mathbf{H}$ an ordinary [[Lie group]], the 
[intrinsic Maurer-Cartan form](#CurvatureCharacteristics) 
$\theta : G \to \mathbf{B}\mathfrak{g}$ 
coicides with the ordinary [[Maurer-Cartan form]] on a Lie algebra.

=--

+-- {: .proof}
###### Proof

This is shown at [[∞-Lie groupoid]].

=--



### Synthetic differential $\infty$-groupoids

The $(\infty,1)$-topos $(\infty,1)Sh(ThCartSp)$ is that of [[smooth ∞-groupoid|synthetic differential ∞-groupoid]] 

The [infinitesimal objects](#InfinitesimalObjects) include 
infinitesimal $\infty$-Lie groupoids: [[∞-Lie algebroid]]s $\mathbf{B}\mathfrak{g}$.





## Applications

### Lie theory, Differential cohomology and Chern-Weil theory

Every cohesive $(\infty,1)$-topos provides an internal notion of
[[ordinary differential cohomology]], [[Lie theory]] and [[Chern-Weil theory]]. See

* [[schreiber:differential cohomology in a cohesive topos]].

### Fundamental physics and gauge theory

As a context for geometric spaces and paths in geometric spaces, cohesive $(\infty,1)$-toposes are a natural context in which to formulate fundamental fundamental [[physics]]. See [[higher category theory and physics]] for more on this.


## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / **cohesive (∞,1)-topos**

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]


## References

The [[category theory|category-theoretic]] definition of [[cohesive topos]] was proposed by [[Bill Lawvere]]. See the references at [[cohesive topos]].

The observation that the further left adjoint $\Pi$ in a [[locally ∞-connected (∞,1)-topos]] defines an intrinsic notion of paths and [[geometric homotopy groups in an (∞,1)-topos]] was suggested by [[Richard Williamson]].

The observation that the further right adjoint $Codisc$ in a [[local (∞,1)-topos]] serves to characterize [[concrete sheaf|concrete (∞,1)-sheaves]] was amplified by [[David Carchedi]].

A pdf-version of some of the material here is at

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos|Differential Cohomology in a Cohesive Topos]]_ 

A commented list of related references is at

* [[schreiber:differential cohomology in an (∞,1)-topos -- references
  |differential cohomology in a cohesive topos -- references]]

Some discussion is at

* [[Urs Schreiber]], 

  _Cohesive $\infty$-Toposes_ ([blog entry](http://golem.ph.utexas.edu/category/2010/10/cohesive_toposes.html))

  _Structures in a Cohesive $\infty$-Topos_ ([blog entry](http://golem.ph.utexas.edu/category/2010/11/structures_in_a_cohesive_topos.html))


[[!redirects cohesive (∞,1)-topos]]

[[!redirects cohesive (∞,1)-toposes]]
[[!redirects cohesive (infinity,1)-toposes]]

[[!redirects cohesive (∞,1)-topoi]]
[[!redirects cohesive (infinity,1)-topoi]]
