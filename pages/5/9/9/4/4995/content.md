
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The definition of _cohesive $(\infty,1)$ topos_ aims to axiomatize properties of an [[(∞,1)-topos]] that make it a [[gros topos]] of [[space]]s inside of which [[higher geometry]] may take place.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] geometric morphism $\Gamma : \mathbf{H} \to \infty Grpd$ of a cohesive $(\infty,1)$topos over [[∞Grpd]] may be thought of as sending a cohesive [[∞-groupoid]] $X$ to its underlying bare $\infty$-groupoid $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten).

Conversely, the [[left adjoint|left]] [[adjoint (∞,1)-functor]] and [[right adjoint]] of $\Gamma$

$$
  \mathbf{H} 
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  \infty Grpd
$$

send an $\infty$-groupoid $S$ either to the [[discrete space|discrete ∞-groupoid]] $Disc(S)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space|codiscrete ∞-groupoid]] $Codisc(S)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]). 

Moreover, the idea is that cohesion makes points lump together to _connected pieces_ . This is modeled by one more functor $\Pi : \mathbf{H} \to \infty Grpd$ [[left adjoint]] to $Disc$. This sends a cohesive $\infty$-groupoid to its [[geometric homotopy groups in an (∞,1)-topos|geometric fundamental ∞-groupoid]] $\Pi(X)$.

In total this gives a quadruple of [[adjoint (∞,1)-functor]]s

   $$
    (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
    \mathbf{H}
     \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
    \infty Grpd
    \;
   $$

A cohesive $(\infty,1)$-topos is an $(\infty,1)$-topos whose terminal [[global section]] [[geometric morphism]] admits an extenson to such a quadruple of adjoints, such that $Disc$ and $Codisc$ are [[full and faithful (∞,1)-functor]]s

The 1-categorical analog -- the notion of [[cohesive topos]] -- was proposed in ([Lawvere](#Lawvere)).

## Definition

+-- {: .un_defn}
###### Definition

An [[(∞,1)-topos]] $\mathbf{H}$ over some base $(\infty,1)$-topos $\mathbf{S}$, i.e. equipped with a [[geometric morphism]]

$$
  (f^* \dashv f_*) : \mathbf{H} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  \mathbf{S}
$$

is **cohesive** over $\mathbf{S}$ if it has the following [[stuff, structure, property|properties]]:

*  it is _local_ and _connected_ in the following sense:

   1. it is a [[locally ∞-connected (∞,1)-topos]]: there exists a further [[left adjoint]] $(f_! \dashv f^*)$ satisfying a suitable condition;

   1. it is an [[∞-connected (∞,1)-topos]]: the [[(∞,1)-functor]] $f_!$ preserves the [[terminal object]], or equivalently $f^*$ is a [[fully faithful (∞,1)-functor]];

   1. it is a [[local (∞,1)-topos]]: there exists a further [[right adjoint]] $(f_* \dashv f^!)$ (this is sufficient for $f$ to be local, since we have already assumed it to be $\infty$-connected);

   so that in total we have a quadruple of [[adjoint (∞,1)-functor]]s
   
   $$
    (f_! \dashv f^* \dashv f_* \dashv f^!) : 
    \mathbf{H}
     \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    \mathbf{S}
    \;
   $$

   Note that $f$ being local implies, in particular, that $\mathbf{S} \stackrel{f^!}{\hookrightarrow} \mathbf{H}$ is a [[subtopos]]: $f^!$ is a [[full and faithful (∞,1)-functor]];


In addition one may ask that

*  the canonical transformation

   $$
     f^* \to f^!
   $$

   is a [[regular monomorphism in an (∞,1)-category]].


If $f$ is the [[global section]] geometric morphism of $\mathbf{H}$, then we say that $\mathbf{H}$ is a **cohesive $(\infty,1)$-topos.
=--

## Properties

+-- {: .un_prop}
###### Proposition

The _shape_ of a cohesive $(\infty,1)$-topos $\Gamma : \mathbf{H} \to \mathbf{S}$ -- in the sense of [[shape of an (∞,1)-topos]] -- is equivalent to that of the base $\mathbf{H}$

=--

+-- {: .proof}
###### Proof

Since by definition $f^*$ is a [[full and faithful (∞,1)-functor]] with both a left and a right adjoint it follows by standard properties of [[adjoint (∞,1)-functor]]s that the composites

$$
  (\mathbf{S}
   \stackrel{\overset{f_!}{\leftarrow}}{\underset{f^*}{\to}}
  \mathbf{H}
   \stackrel{\overset{f_!}{\leftarrow}}{\underset{f^*}{\to}}
  \mathbf{S})
  \;\;
  \simeq
  (Id \dashv Id)
$$

are [[equivalence in a quasi-category|equivalent]] to the identity $(\infty,1)$-functors.


=--




## Examples

The [[(∞,1)-category of (∞,1)-sheaves]] on an [[(∞,1)-cohesive site]] is an cohesive $(\infty,1)$-topos (see there).

This includes

* the [[(∞,1)-category of (∞,1)-presheaves]] on any category with finite [[product]]s;

* the $(\infty,1)$-topos $\mathbf{H} = $ [[?LieGrpd]] of [[∞-Lie groupoid]]s over the site [[CartSp]];

* its infinitesimal thickening, the $(\infty,1)$-[[Cahiers topos]].





### Smooth sets {#SmoothSets}

Here we go in detail through a 1-categorical version of the above arguments, over the site of cohesion [[CartSp]]. Below in [infinity-Lie groupoids](#InfLieGrpd) we look at the full $(\infty,1)$-topos over this site.

+-- {: .un_theorem}
###### Theorem

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a cohesive topos over [[Set]].

=--

We first show that it is a [[locally connected topos]] in that the terminal [[global section]] [[geometric morphism]] to [[Set]] is an [[essential geometric morphism]]

$$
  Sh(CartSp)
  \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{L Const}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
$$

and show that the extra [[left adjoint]] $\Pi_0 : Sh(CartSp) \to Set$ sends diffeological spaces to the set of path-[[connected]] components of their underlying [[topological space]]s.


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]].

=--

+-- {: .proof}
###### Proof

The following argument works for every [[site]] $C$ which is such that constant presheaves on $C$ are already sheaves.

Notice that this is the case for $C = CartSp$ because every Cartesian space is connected: for $S \in Set$ a compatible family of elements of $Const S$ on a cover $\{U_i \to \mathbb{R}^n\}$ of some $\mathbb{R}^n$ is an element of $S$ on each patch, such that their restriction maps to intersections of patches coincide. But the restriction maps are all identities, so this says that all these elements coincide. Therefore the set of compatible families is just the set $S$ itself, hence the presheaf $Const S$ is a sheaf.

So with $L : PSh(C) \to Sh(C)$ the [[sheafification]] functor we have that $L Const S \simeq Const S$.

Whenever this is the case the [[left adjoint]] to the constant presheaf functor, which always exists for presheaves and is given by the [[colimit]] functor, is also left adjoint on the level of sheaves, because for each $X \in Sh(C)$ and $S \in Set$ we have natural bijections

$$
  \begin{aligned}
    Hom_{Sh(C)}(X, L Const S)
    & =
    Hom_{PSh(C)}(X, L Const S)
    \\
    & \simeq
    Hom_{PSh(C)}(X, Const S)
    \\
    & \simeq
    Hom_{Set}(\lim_\to X, S)
  \end{aligned}
  \,.
$$

=--

+-- {: .un_def}
###### Definition

Write $\Pi_0 := \lim_\to : Sh(CartSp) \to Set$
for the [[left adjoint]] to $LConst : Set \stackrel{Const}{\to} PSh(C) \stackrel{L}{\to} Sh(C)$.

=--

+-- {: .un_prop}
###### Proposition

For $X \in Sh(C)$ a diffeological space, $\Pi_0(X)$ is the set of path-connected components of the topological space underlying $X$.

=--

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]] we may write 

$$
  X = {\lim_\to}_{(U \to X) \in y/X} U
$$

and since $\Pi_0$ commutes with colimits we have

$$
  \Pi_0(X) \simeq 
  \Pi_0 {\lim_\to}_{(U \to X)} U
  \simeq
  {\lim_\to}_{(U \to X)} \Pi_0(U)
  \,.
$$

But also by the co-Yoneda lemma we have that the [[colimit]] over any [[representable functor|representable]] is the singleton set, hence our expression

$$
  \cdots \simeq 
  {\lim_\to}_{(U \to X)} *
$$

is the colimit over the category of plots of $X$ of the functor that is constant on the point. This colimit is the [[coproduct]] of points over the connected components of the [[diagram]] category.

The connected components of the category of plots $y/X$ are the path-connected (or "plot-connected") components of the underlying topological space of $X$.



=--


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is even a [[connected topos]].

=--

+-- {: .proof}
###### Proof

Since $CartSp$ is a [[connected category]] it is immediate that $Const : Set \to PSh(CartSp)$ is a [[full and faithful functor]]. By the above this equals $L Const$, which is hence also full and faithful.

By the discussion at [[connected topos]] we could equivalently convince ourselves that $\Pi_0$ preserves the terminal object. The terminal object of $Sh(CartSp)$ is $y(\mathbb{R}^0)$, hence representable. By the above, $\Pi_0$ sends all representable objects to the singleton set, which is the terminal object of $Set$. 

=--

### Diffeological spaces

A _reflective localization_ at a collection of morphisms $W$ is a [[reflective subcategory]] on [[local object]]s, those $A$ for which for all $w \in W$ we have that $A^w$ is an isomorphism.

We say a **quasi-localization** is similarly a full subcategory on objects such that $A^w$ in a [[monomorphism]].



+-- {: .un_prop}
###### Proposition

The [[quasitopos]] of [[diffeological space]]s 

$$
  Diffeol \hookrightarrow Sh(CartSp)
$$

is the reflective quasi-localization at the counits  $Disc \Gamma U \to U$ for $U \in CartSp$.

=--

+-- {: .proof}
###### Proof

For $X \in Sh(CartSp)$ we have

$$
  Hom(Disc \Gamma U , X) 
    \simeq
  Hom_{Set}(\Gamma U , \Gamma X)
  \,.
$$

So we need to check for which $X$ we have for all $U\in CartSp$ that

$$
  Hom(U,X) \to Hom_{Set}(\Gamma(U), \Gamma(X))
$$

is a monomorphism.

The [[image]] of this morphism is $Hom(U, Conc(X))$, the plots of the [[concrete sheaf|concretization]] of $X$: the [[diffeological space]] underlying $X$. So we have a factorization of our morphism as

$$
   Hom(U,X) 
    \hookrightarrow
   Hom(U, Conc(X))
   \hookrightarrow
  Hom_{Set}(\Gamma U , \Gamma X)
  \,,
$$

where the second morphims is a monomorphism. So for the total morphism to be a monomorphism we need that the image-projection is. But since that is already an epimorphism, it follows that we need that the image projection is an isomorphism, hence that $X$ is already a [[concrete sheaf]].

So the concrete sheaves on $CartSp$, hence the [[diffeological space]]s, are precisely the quasi-localization at the morphisms $Disc \Gamma U \to U$.

=--



### $\infty$-Lie groupoids {#InfLieGrpd}

As a special case of the above theorem, the [[(∞,1)-category of (∞,1)-sheaves]] $(\infty,1)Sh(CartSp) = $ [[?LieGrpd]] on [[CartSp]] is a cohesive $(\infty,1)$-topos over [[∞Grpd]]. (See there for the moment.)



## Interpretation

We discuss some interpretations and ways to think about

1. a cohesive $(\infty,1)$-topos as such;

1. structures inside a cohesive $(\infty,1)$-topos.

### The structure of a cohesive $(\inft,1)$-topos

Notice that the canonical cohesive $(\infty,1)$-topos [[∞Grpd]] may be thought of as being the ($(\infty,1)$-topos theoretical dual to) the [[point]]

$$
  \infty Grpd \simeq (\infty,1)Sh(*)
  \,.
$$

The abstract properties of a cohesive $(\infty,1)$-topos $\mathbf{H}$ over $\infty Grpd$ show that also $\mathbf{H}$ still _looks like a point_ :

* it is a [[∞-connected (∞,1)-topos]] and in this respect looks like a [[contractible]] [[topological space]];

* it is a [[local (∞,1)-topos]] -- a property shared by $(\infty,1)$-topos over thickened points (see [[local topos]]);

* its [[shape of an (∞,1)-topos]] is that of the point.

At the same time, a cohesive $(\infty,1)$-topos is in general _bigger_ than then stadard point $*$. We may think of it as a general abstract _fat point_ : the general abstract _lump of cohesive points_ for the given notion of cohesion.

For instance in our examples we see that

* $(\infty,1)Sh(CartSp)$ is like the **general abstract smooth [[open ball]]** .

* let $\mathbb{L}_{inf}$ be the full subcategory of [[smooth loci]] in the [[infinitesimal space]]s. then   $(\infty,1)Sh(\mathbb{L}_{inf})$ is like the **general abstract infinitesimally thickened point**;

* similarly, let $\Lambda$ be the category of $\mathbb{Z}_2$-garded [[Grassmann algebra]]s. Then $(\infty,1)Sh(\Lambda^{op})$ is like the **general abstract super-point**;

* $(\infty,1)Sh(ThCartSp)$ is like the **general abstract infinitesimally thickened smooth open ball** .

 
### Structures inside a cohesive $(\infty,1)$-topos

We list the geometric meaning of the various morphisms and structures in
a cohesive [[(∞,1)-topos]] over [[∞Grpd]]. (We follow the entries [[schreiber:structures in an (∞,1)-topos]] and [[schreiber:differential cohomology in an (∞,1)-topos]] where more motivation and justification for these interpretations can be found.)

Write

$$
 (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
 \mathbf{H}
  \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
 \infty Grpd
$$

for the given cohesive $(\infty,1)$-topos. Its objects $X,A \in \mathbf{H}$ we ay think of as [[∞-groupoid]]s with cohesive structure. For instance in the case $\mathbf{H} = $ [[?LieGrpd]] they are $\infty$-groupoids with _smooth_ structure. Then

* $\Gamma(X)$ is the _underlying $\infty$-groupoid_ of the cohesive $\infty$-groupoid $X$ (for instance an $\infty$-Lie groupoid with its smooth structure forgotten);

* $\Pi(X)$ is the fundamental [[path ∞-groupoid]] of $X$: its [[k-morphism]]s are generated from $k$-dimensional smooth paths in $X$ and the $k$-morphisms of $X$ itself. Under the equivalence of $(\infty,1)$-toposes 

  $|-| :$  [[∞Grpd]] $\stackrel{\simeq}{\to}$ [[Top]] 


  we may think of $|\Pi(X)|$ as the _geometric realization_ of $X$. For instance if $X \in \infty LieGrpd$ is a [[paracompact manifold]], then $|\Pi(X)|$ is, up to [[weak homotopy equivalence]] its underlying topological space.

Write 

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat})
  = 
  (Disc \Pi \dashv Disc \Gamma) : \mathbf{H} \to \mathbf{H}
  \,.
$$


Then unit and counit of the [[adjunction]]s give canonical natural morphisms

* $X \to \mathbf{\Pi}(X)$ -- this we may think of as the inclusion of $X$ as the constant paths in the [[path ∞-groupoid]] $\mathbf{\Pi}(X)$;

* $\mathbf{\flat}A \to A$ -- if we think of $A$ as the coefficient object for $A$-[[principal ∞-bundle]]s in $\mathbf{H}$, 

  $$  
    A Bund(X) := \mathbf{H}(X,A)
  $$

  then this is the map that takes principal $A$-bundles with [[schreiber:differential cohomology in an (∞,1)-topos|flat connection]] 

   $(X \to \mathbf{\flat}A) \leftrightarrow (\mathbf{\Pi}(X) \to A)$ to the underlying $A$-bundle.

  If $A = \mathbf{B}G$ is the [[delooping]] of an [[∞-group]] object, then we may think of $\mathbf{\flat} \mathbf{B}G$ or rather the corresponding  $Disc(\mathbf{B}G)$ as being $K(G,1)$: the classifying object for $G$-principal bundles where all cohesive structure on $G$ has been forgotten.

  Accordingly, the canonical map

  $$
    Disc(\mathbf{B}G) \to \Pi \mathbf{B}G
  $$

  that apppears in the second clause of the definition of cohesive topos is the inclusion of the topologist's $K(G,1)$ into the topological [[classifying space]] $\mathcal{B}G$. Again, on [[cocycle]]s this is the map from flat bundles to the underlying bundles.





## References

The definition of a [[cohesive topos]] was proposed in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
{#Lawvere}

The observation that $Sh(CartSp)$ is a [[local topos]] and that this serves to characterize [[diffeological space]]s was amplified by [[David Carchedi]].


[[!redirects cohesive (∞,1)-topos]]

[[!redirects cohesive (∞,1)-toposes]]
[[!redirects cohesive (infinity,1)-toposes]]

[[!redirects cohesive (∞,1)-topoi]]
[[!redirects cohesive (infinity,1)-topoi]]
