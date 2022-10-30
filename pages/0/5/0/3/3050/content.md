
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Monadic descent is a way to encode [[descent]] of [[fibered category|fibered categories]] (equivalently, by the [[Grothendieck construction]], of [[pseudofunctor]]s) that have the special property that they are [[bifibration]]s. This allows to use algebraic tools, notably [[monad]]s and related structures from [[universal algebra]]:

a [[bifibration]] $E \to B$ comes naturally equipped not only with a notion of pullback, but also of pushforward. Combined these provide pull-push-[[monad]]s that may be used to encode the [[descent]] property of the fibration.

A morphism $f : b_1 \to b_2$ in the base $B$ induces an [[adjunction]] $F\dashv U$ where 

$$
  F \;:\; E_{b_1} =: A\leftrightarrow B := E_{b_2} \;:\; U
$$ 

and we ask whether $U$ is a [[monadic functor]]. 

This is the original description of [[descent]] of presheaves with values in 1-categories due to [[Alexander Grothendieck]].

The archetypical and motivating example is that of the bifibration $Mod \to Ring$ of [[module]]s over [[Ring]]s.



## Details {#Details}

The adjunction, $F\dashv U$ with unit $\eta:1_B \to U \circ F$ and counit $\epsilon: F \circ U\to 1_A$, induces the [[monad]] $\mathbf{T}= (T,\mu,\eta)$ in $B$ via $T\coloneqq U F$, $\mu\coloneqq U\epsilon F:U F U F\to U F$ with unit $\eta$. The monad $\mathbf{T}$ generates the [[Eilenberg?Moore category]] $B^{\mathbf{T}}$ of modules (= algebras) over $\mathbf{T}$, that is the pairs $(M,\nu)$ where $M\in Ob(B)$ and $\nu:T M\to M$ satisfies the action axioms $T(\nu)\circ \nu= \nu_T \circ\nu$ and $\nu\circ\eta_M=id_M$. 

We think of this data as follows:

* $A$ is the category of some type of objects on some space;

* $B$ is the category of this type of object on a [[cover]] of that space

* $B^T$ is the category of [[descent]] data for such objects, with respect to that cover.

There is a **comparison functor** 

$$ K : A\to B^{\mathbf{T}}, \,\,\,\, K(N) \coloneqq  (U(N),U(\epsilon_N)). $$

We say that the functor $U$ is [[monadic functor|monadic]] or more informally that $A$ is monadic over $B$ if the comparison functor is an [[equivalence of categories]]. Sometimes one is interested in a weaker condition: whether the comparison functor is [[fully faithful functor|fully faithful]]. 


## Main theorems

The main theorem is Beck's [[monadicity theorem]].

Given a Grothendieck [[bifibration]] $p:E\to B$ and a morphism $f:b\to b'$ in the base category $B$, one can choose a [[direct image]] $f_!:E_b\to E_{b'}$ and an [[inverse image]] functor $f^*:E_{b'}\to E_b$, which form an [[adjunction]] $f_!\dashv f^*$. Under some conditions (see the [[Bénabou?Roubaud theorem]]), the morphism $f$ is an [[effective descent morphism]] (with respect to $p$ as a [[fibered category]]) iff the comparison functor for the [[monad]] induced by the adjunction $f_!\dashv f^*$ is monadic. 

We should now see that some instances of categories of [[descent]] data are canonically equivalent to and can be reexpressed via [[Eilenberg-Moore category|Eilenberg?Moore categories]] of monads, or dually comonads. 


## Examples


### Monadic descent of bundles {#ForCodomainFibs}

One of the most basic examples of [[bifibration]]s are [[codomain fibration]]s $cod : [I,C] \to C$. Accordingly, monadic descent applied to codomain fibrations archetypically exhibits the nature of monadic descent. We therefore spell out this example is some detail.

An object in a [[codomain fibration]] over $Y \in C$ is a morphism $P \to Y$, hence a [[bundle]] in $C$, in the most general sense of bundle. Therefore monadic descent with respect to codomain fibrations encodes [[descent]] of bundles.

Other examples of monadic descent often find a useful interpretation when relating them back to monadic descent for codomain fibrations. For instance (co)monadic descent for [[Sweedler coring]]s, discussed below, finds a natural geometric interpretion this way (as discussed in detail there).


We show in the following that for $cod : [I,C] \to C$ a [[codomain fibration]] and for $\pi : Y\to X$ a morphism in $C$, an algebra object in $[I,C]_Y$ over the [[monad]] $f^* f_*$ encodes and is encoded by a "geometric" [[descent]] datum: that it is

* a morphism $P \to Y$

* equipped with a transition function between its two pullbacks to double $Y \times_X Y$

* which satisfies on $Y \times_X Y \times_X Y$ the usual cocycle condition.

#### Motivation: failure of push-forward for principal bundles

Monadic methods can be applied to the study of descent of structures that cannot only be pulled back, such as [[principal bundle]]s, but that can also be pushed forward, such as [[vector bundle]]s (with suitable care taken) or more generally [[module]]s over functions rings (discussed at [[Sweedler coring]]).


Given a [[principal bundle]] $P \to X$ (a topological one, say, i.e. a morphism in [[Top]]) and a morphism of base spaces $f : X \to Z$, the would-be candidate for the push-forward of $P$ along $f$ is simply the composite map
$P \to X \to Z$, regarded as a total space $P \to Z$ liveing over $Z$.

While that always exists as such, it will in general not be a principal bundle anymore: the [[fiber]]s of $P \to Z$ over points $z \in Z$ consist of many copies of the fibers of $P \to X$ over points in $X$. Hence the shape of the fibers may change drastically as we push bundles forward.

So principal bundles do have a canonical notion of push-forward, but it leads outside the category of principal bundles and lands generally in some [[overcategory]].

On the other hand, as we will see in detail below, if we take a principal bundle $P \to X$ and

* first push it forward in this generalized sense to an object $P \to Z$ in the [[overcategory]] $Top/Z$

* and **then** pull back the result of that again along $X \to Z$ the result, while still not a principal bundle, is the total space $P$ of the bundle pulled back to the first term in the [[?ech nerve]] of $f : X \to Z$. This pullback is of central interest in the description of the geometric [[descent]] property of the bundle. 

But the composite operation of pushforward of overcategories

$$
  push(f) : Top/X \to Top/Z
$$

followed by pullback

$$
  pull(f) : Top/Z \to Top/X
$$

is nothing but the [[monad]] associated to $f : X \to Z$ with respect to the [[codomain fibration|codomain bifibration]] $cod : [I,Top] \to Top$.

So by regarding principal bundles $P \to X$ more generally as just objects in the [[overcategory]] $Top/X$ we make the tools of monadic descent applicable to them.


#### The monad

Let $C$ be a [[category]] with [[pullback]]s. Then the [[codomain fibration]]

$$
  cod : [I,C] \to C
$$

is a [[bifibration]] (as described there, in detail). Its [[fiber]] over an object $X \in C$ is the [[overcategory]] $C/X$. 

The direct image operation $push(f)$ associated to a morphism $\pi : Y \to X$ in $C$ is the functor

$$
  push(\pi) : C/Y \to  C/X
$$

obtained by postcomposition with $f$, which sends $(P \to Y) \in C/Y$ to the composite $P \to Y \stackrel{\pi}{\to} X$ in $C$, regarded as an object of $C/X$.

The inverse image operation $pull(f)$ associated to $f$ is the functor

$$
  C/Y \leftarrow C/X : pull(\pi)
$$

obtained by [[pullback]] in $C$ along $\pi$, which sends $(Q \to X) \in C/X$ the [[pullback]] $Q \times_X Y$, regarded as an object of $C/Y$ in terms of the canonical projection morphism $Q \times_X Y\to Y$ out of the pullback.

Write

$$
  T_\pi = pull(\pi) \circ push(\pi) : C/Y \to C/Y 
$$

for the [[monad]] built from these two [[adjoint functor]]s.


#### The algebras over the monad: geometric descent data

We spell out in detail the data of an algebra over the above monad, nad show that this encodes precisely the familiar geometric [[descent]] datum for a [[bundle]].

To that end, let $(P, \rho)$

$$
  P : {*} \to C/Y
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
      && C/Y
      \\ 
      & {}^{\mathllap{P}}
     \nearrow  &\Downarrow^{\rho}& \searrow^{\mathrlap{T}}
     \\
    {*} &&\stackrel{P}{\to}&& C/Y
  }
$$

be an [[monad|algebra over]] our monad. In components this is an object $T P$ equipped with a morphism $\rho_P : T P \to P$.

The object $T P \in [I,C]_Y$ is given by

* first pushing $P \to Y$ forward along $\pi : Y \to X$ to the object $P \to Y \to X$.

* then pulling this back along $\pi$ to yield the left vertical morphism in

  $$
    \array{
      Y \times_X P &\to& P
      \\
      \downarrow && \downarrow
      \\
      && Y
      \\
      \downarrow && \downarrow^{\mathrlap{\pi}}
      \\
      Y &\stackrel{\pi}{\to}& X
    }
    \,.
  $$

  This [[pullback]] along a composite of morphisms may be computed as two consecutive pullbacks. The first one is

  $$
    \array{
      Y \times_X Y &\to& Y
      \\
      \downarrow && \downarrow^{\mathrlap{\pi}}
      \\
      Y &\stackrel{\pi}{\to}& X 
    }
  $$

  which is the first term in the [[?ech nerve]] of $\pi$. So the total pullback is the pullback $P$ to $Y\times_X Y$:

  $$
    \array{
      (Y \times_X Y) \times_Y P &\to& P
      \\
      \downarrow && \downarrow
      \\
      Y \times_X Y &\to& Y
      \\
      \downarrow && \downarrow^{\mathrlap{\pi}}
      \\
      Y &\stackrel{\pi}{\to}& X
    }
    \,.
  $$
  
Therefore the action $\rho_T : T P \to P$ of our [[monad]] on $P$ is given in $C$ by a morphism

$$
  \array{
    (Y \times_X Y) \times_Y P &&\stackrel{\rho}{\to}&&
    P
    \\
    & \searrow && \swarrow
    \\
    && Y
  }
  \,.
$$

As an example, think of this in the context $C = Top$ with $\pi Y \to X$ coming from an open [[cover]] $\{U_i \to X\}$ of $X$ with $Y = \coprod_i U_i$, and with $P = Y \times G$ a trivial $G$-[[principal bundle]] for some [[group]] $G$. Then the space $Y \times_X Y = \coprod_{i j} U_i \cap U_j$ is the union of double intersection of covering patches, and $(Y \times_X Y) \times_Y P = (\coprod_{i j} U_i \cap U_j \times G)$ is to be thought of as the trivial $G$-principal bundle over $U_j$, restricted to the intersection. In this case our morphism $\rho$ acts as

$$
  \rho : \coprod_{i j} : (U_i \cap U_j \times G) \to \coprod_i U_i \times G
$$

and thus maps the trivial $G$-bundle over $U_j$ on the intersection with the trivial $G$-bundle over $U_i$. So it is a _transition function_. If this is a $G$-equivariant, it may be part of the  [[descent]] datum for the $G$-[[principal bundle]].



### Monadic descent _along_ principal bundles {#AlongPrincipalBundle}

#### Idea

In the [above section](#ForCodomainFibs) we considered monadic descent _of_ [[bundle]]s $P \to Y$ _along_ morphisms $f : Y \to X$. 

Now we consider monadic descent _along_ morphisms $f : P \to X$ that happen to be $G$-[[principal bundle]]s, for some [[group object]] $G$. When considered with respect to the [[codomain fibration]] this describes the situation where we ask for a bundle $L \to P$ that sits over the total space of another (principal) bundle to descend down along that bundle map to $X$. So beware of the two different roles that bundles play here.

#### Setup

Let $C$ be a [[category]] with [[pullback]]s and et $G$ be an internal group in $C$.

Let $\nu: P\times G\to P$ be a right principal [[action]] and $p:P\times G\to P$ the projection. Let $\pi:P\to X$ be the [[coequalizer]] of $\nu$ and $p$. The [[principal bundle|principality condition]] says that $P\times G \to P\times_X P$ given by $(p,g)\mapsto (p,pg)$ is an [[isomorphism]]. 

$$
P\times G \overset{\nu}\underset{p}\rightrightarrows P \overset{\pi}\to X
$$

We do not assume $P$ to be trivial. We have also the two projections

$$
P\times_X P \overset{p_1}\underset{p_2}\rightrightarrows P \overset{\pi}\to X
$$

out of the [[pullback]], where $p_1,p_2$ make a [[kernel pair]] of $\pi$. Thus the principality condition is equivalent to saying that $\nu,p$ make also a [[kernel pair]] of its own [[coequalizer]]. The two diagrams above are truncations of augmented [[simplicial object]]s in $C$. We want to relate these objects to [[monad]]s.

#### The two different monads

We now describe the monadic descent along the morphism $\pi : P \to X$ from above for the [[codomain fibration]] $cod : [I,C] \to C$.

There are two monads acting on the [[overcategory]] $C/P$ whose underlying functors are 

1. $T := \pi^* \pi_!$.

1. $\tilde T := p_! \nu^*$ 


The first monad, $T$ is the usual one for monadic descent along $\pi$ induced from a pair of [[adjoint functor]]s. 

The second one, $\tilde T$, exists due to the principality of $P \to X$ and is defined as follows: 

to construct the component $\mu_h$ of the transformation $\mu: p_! \nu^* p_!\nu^*\to p_!\nu^*$ where $h: L\to P$, by the universal property of the pullback there is an obvious map $\nu^* p_! \nu^* h$ to $p_! \nu^* h$ 

$$
  \array{
    \nu^* p_! \nu^* L
    \\
    & \searrow^{\mathrlap{\mu_h}}
    \\
    &&\nu^* L &\to& L
    \\
    &&
    \downarrow && \downarrow
    \\
    &&
    P &\stackrel{\stackrel{p}{\to}}{\underset{\to}{\nu}}& 
    X
  }
  \,,
$$

which can be interpreted as a map $p_!\nu^* p_! \nu^* h\to p_* \nu^* h$ because the domains of the maps $p_!\nu^* p_! \nu^* h$ and $\nu^* p_! \nu^* h$ are the same by the definition and the commuting triangles can be checked easily. 

The [[principal bundle|principality]] $P\times G \cong P\times_X P$ now induces the [[isomorphism]]

$$p_! \nu^* h \cong \pi^* \pi_! h$$

[[natural isomorphism|natural]] in  $h:L\to P$, read off from the double [[pullback]] diagram

$$
  \array{
   p_! \nu^* L &\stackrel{\simeq}{\to}& \pi^* \pi_! L &\to& L
   \\
   \downarrow && \downarrow && \downarrow^{\mathrlap{h}}
   \\
   P \times G &\stackrel{\simeq}{\to}& P \times_X P &\to& P
   \\
   && \downarrow && \downarrow^{\mathrlap{\pi}}
   \\
   && P &\to& X
  }
  \,.
$$


This rule extends to an isomorphism of monads 

$$
  T \simeq \tilde T
  \,.
$$

As a corollary, the [[Eilenberg-Moore category|Eilenberg-Moore categories]] of the two monads are [[equivalence of categories|equivalent]]. Notice that the actions over the monad $p_! \nu^* $ are certain maps $p_!\nu^*h\to h$, hence $\nu^* h\to p^* h$ by adjointness. This matches one of the definitions for an [[equivariant sheaf]].

The map $ \pi : P\to X$ of the principal bundle is an **[[effective descent morphism]]** with respect to the [[codomain fibration]] if the comparison functor for any of the two above isomorphic monads above is an equivalence of categories.  

### Monadic descent of modules

There is a [[bifibration]] $Mod \to Rings$ from the category of modules over any ring, mapping each module to the ring that it is a module over. This models, dually,  an algebraic version of [[vector bundle]]s over [[affine scheme]]s.

Comonadic descent for this bifibration (equivalently monadic descent for its formal dual, $Mod^{op} \to Rings^{op}$) is the same as descent for a [[Sweedler coring]]. See there for details and geometric interpretations. 


### Gluing categories from localizations

Another example is in [[zoranskoda:gluing categories from localizations|gluing categories from localizations]]. 


## Higher category theoretical version

All the ingredients of monadic descent generalize from [[category theory]] to [[higher category theory]]. Accordingly, one may consider [[higher monadic descent]] that relates to [[∞-stack]]s as monadic descent relates to [[stack]]s. For more on this see

* [[higher monadic descent]].

## Related concepts

* [[descent]]

  * [[cover]]

  * [[cohomological descent]]

  * [[descent morphism]]

  * **monadic descent** 

    * [[Sweedler coring]]

    * [[higher monadic descent]]

    * [[descent in noncommutative algebraic geometry]]

* [[sheaf]], [[(2,1)-sheaf]], [[2-sheaf]] [[(∞,1)-sheaf]]




[[!redirects comonadic descent]]

