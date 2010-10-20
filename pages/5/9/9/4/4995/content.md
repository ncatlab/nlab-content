
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

A _cohesive $(\infty,1)$-topos_ is an [[(∞,1)-topos]] $\mathbf{H}$ whose [[global section]] [[(∞,1)-geometric morphism]] $\Gamma : \mathbf{H} \to $ [[∞Grpd]] admits a further [[left adjoint]] $\Pi$ and a further right adjoint $Codisc$: 

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : \mathbf{H} \to \infty Grpd
$$ 

with $Disc$ and $Codisc$ both [[full and faithful (∞,1)-functor]]s and such that $\Pi$ moreover preserves finite [[(∞,1)-limit|product]]s. Here

1. $Codisc$ induces an [[(∞,1)-quasitopos]] $Conc(\mathbf{H}) \hookrightarrow \mathbf{H}$ of _concrete_ objects, those that look like [[∞-groupoid]]s _equipped with extra cohesive structure_ : for instance with [[topology]], or with [[smooth structure]].

1. $\Pi$ sends an object $X$ to its [[geometric homotopy groups in an (∞,1)-topos|geometric]] [[schreiber:path ∞-groupoid]], which co-classifies [[locally constant ∞-stack]]s on $X$.


The definition of _cohesive $(\infty,1)$ topos_ aims to axiomatize properties of an [[(∞,1)-topos]] that make it a [[gros topos]] of [[space]]s inside of which [[higher geometry]] may take place.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] [[(∞,1)-geometric morphism]] $\Gamma : \mathbf{H} \to \infty Grpd$ of a cohesive $(\infty,1)$topos over [[∞Grpd]] may be thought of as sending a cohesive [[∞-groupoid]] $X$ to its underlying bare $\infty$-groupoid $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten).

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


Notice that despite this motivation, the general object in a cohesive $(\infty,1)$-topos is far from being a bare $\infty$-groupoid with extra structure: while the functor $\Gamma$ does produce the $\infty$-groupoid underlying an object $X$ in the cohesive $(\infty,1)$-topos, it may happen that $X$ is very non-trivial but that nevertheless $\Gamma(X)$ is $k$-[[truncated]] for very small $k$. But using the [[geometric embedding]] $Codisc : \infty Grpd \hookrightarrow \mathbf{H}$ we find there is intrinsically an [[(∞,1)-quasitopos]] $Conc(\mathbf{H})$ of [[concrete sheaf|concrete (∞,1)-sheaves]] inside $\mathbf{H}$

$$
  Codisc : \infty Grpd \hookrightarrow Conc(\mathbf{H}) \stackrel{\overset{concretize}{\leftarrow}}{\hookrightarrow} \mathbf{H}
$$

whose objects are precisely those $\infty$-groupoids that do behave like bare $\infty$-groupoids equipped with cohesive structure.



## Definition

+-- {: .un_defn}
###### Definition

An [[(∞,1)-topos]] $\mathbf{H}$ over some base $(\infty,1)$-topos $\mathbf{S}$, i.e. equipped with a [[geometric morphism]]

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
  \mathbf{S}
  \;
$$

with both $f^*$ and $f^!$ being [[full and faithful (∞,1)-functor]]s and $f_!$ preserving finite products.

(For more general $S$ there is an extra condition on $\Pi$.)

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
   \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  \mathbf{S})
  \;\;
  \simeq
  (Id \dashv Id)
$$

are [[equivalence in a quasi-category|equivalent]] to the identity $(\infty,1)$-functors. 


=--

### Differential cohomology


Every [[(∞,1)-topos]] $\mathbf{H}$ comes with its [[cohomology|intrinsic cohomology]]: for $X, A \in \mathbf{H}$ a [[cocycle]] on $X$ with coefficients in $\mathbf{H}$ is a [[morphism]] $g : X \to A$. A coboundary is a [[2-morphism]] between two such. The [[cohomology]] set of $X$ with coefficients in $A$ is

$$
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$

For $A = \mathbf{B}G$ the [[delooping]] of an [[∞-group]] object in $\mathbf{H}$, we have that $G Bund(X) := \mathbf{H}(X, \mathbf{B}G)$ is the [[∞-groupoid]] of $G$-[[principal ∞-bundle]]s on $X$.


If $\mathbf{H}$ is also a [[locally ∞-connected (∞,1)-topos]] -- such as a cohesive $(\infty,1)$-topos -- it moreover comes with an intrinsic notion of [[schreiber:differential cohomology in an (∞,1)-topos]]:

for $X \in \mathbf{H}$ the [[∞-groupoid]] $\Pi(X)$ may be regarded as the [[schreiber:path ∞-groupoid]] of $X$. So $\Pi$ detects the [[geometric homotopy groups in an (∞,1)-topos]]. Its reflection $\mathbf{\Pi} := Disc \circ \Pi$ back into $\mathbf{H}$ is the domain for [[local system]]s on $X$, a cocycle $g_{flat} : \mathbf{\Pi}(X) \to A$ is a _flat differential cocycle_ on $A$. For $A = \mathbf{B}G$ this is a flat [[connection on an ∞-bundle]] for the underlying $G$-[[principal ∞-bundle]] given by $X \to \mathbf{\Pi}(X) \to A$.

Dually, flat differential cohomology is cohomology on $X$ with coefficients in the flat object $\mathbf{\flat}A$, for $\mathbf{\flat} = Disc \circ \Gamma$ the [[right adjoint]] $(\mathbf{\Pi} \dashv \mathbf{\flat})$.

If $A$ is stable, for instance an [[Eilenberg-MacLane object]] $A = \mathbf{B}^n K$ for an [[abelian group]] object $K$, then there is an intrinsic de Rham cohomology object $\mathbf{\flat}_{dR} \mathbf{B}^n K$ given by the [[homotopy fiber]] of the counit $\mathbf{flat} A\to A$. 

The canonical induced morphism $\mathbf{H}(X,\mathbf{B}^n K) \to \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^{n+1} K)$ is the [[curvature]] assignment of the [[∞-Chern-Weil homomorphism]]. The [[twisted cohomology]] for this [[curvature characteristic class]] is the **differential cohomology** $\mathbf{H}_{diff}(X,\mathbf{B}^n K)$ of $X$ with coefficients in $K$ in degree $n$.

Generally, for every [[characteristic class]] $\mathbf{B}G \to \mathbf{B}^n K$ the postcomposition $\mathbf{B}G \to \mathbf{B}^n K \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1}K$ induces the [[∞-Chern-Weil homomorphism]] on $G$-[[principal ∞-bundle]]s. This is modeled by equipping a $G$-principal $\infty$-bundle with a [[connection on an ∞-bundle]]. 

For more on this see [[∞-Chern-Weil theory introduction]].


### Concrete objects

Even with a notion of cohesion, the general object $X \in \mathbf{H}$ in a cohesive $(\infty,1)$-topos may be non-[[concrete sheaf|concrete]] in that it is not modeled on its [[point]]s, or rather its underlying [[∞-groupoid]] $\Gamma X$. 

Since 

$$
  \infty Grpd \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  \mathbf{H}
$$

is a [[geometric embedding]], the reflector $\Gamma$ encodes the [[localization of an (∞,1)-category]] at a class of morphisms $W$, realizing $\infty Grpd$ as the [[reflective sub-(∞,1)-category]] on the $W$-[[local object]]s. This inclusion factors canonically through the corresponding [[quasitopos]] of $W$-[[separated presheaf|separated (∞,1)-sheaves]]

$$
  \infty Grpd 
    \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
   Conc(\mathbf{H})
   \stackrel{\overset{concretizaton}{\leftarrow}}{\underset{}{\hookrightarrow}}
   \mathbf{H}
  \,.
$$

This encodes the [[concrete sheaf|concrete]] objects in $\mathbf{H}$.


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

is the $\infty$-groupoid whose objects are $G$-[[principal ∞-bundle]]s on $X$ and whose morphisms are $G$-principal bundles on the cylinder $X \times I$. These are _concordances of $\infty$-bundles._




## Interpretation {#Interpretation}

We discuss some interpretations and ways to think about

1. a cohesive $(\infty,1)$-topos as such;

1. structures inside a cohesive $(\infty,1)$-topos.

### The structure of a cohesive $(\infty,1)$-topos


We discuss here the following

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

For instance in our [examples](#Examples) we see that

* $(\infty,1)Sh(CartSp)$ is like the **general abstract smooth [[open ball]]**.

* let $\mathbb{L}_{inf}$ be the full subcategory of [[smooth loci]] in the [[infinitesimal space]]s. then   $(\infty,1)Sh(\mathbb{L}_{inf})$ is like the **general abstract infinitesimally thickened point**;

* similarly, let $\Lambda$ be the category of $\mathbb{Z}_2$-graded [[Grassmann algebra]]s. Then $(\infty,1)Sh(\Lambda^{op})$ is like the **general abstract super-point**;

* $(\infty,1)Sh(ThCartSp)$ is like the **general abstract infinitesimally thickened smooth open ball** .

Notice that for plain [[topological space]]s an [[etale space]] $X \to H$ is a space $X$ that is _locally built from pieces of $H$_ . The generalization of this from [[topology]] to [[topos theory]] is an [[etale geometric morphism]] or [[locally homeomorphic geometric morphism]]: every object $X \in \mathbf{H}$ gives rise to the [[over-(∞,1)-category]] $(\infty,1)$-topos $\mathbf{H}/X$ with the evident projection geometric morphism $\mathbf{H}/X \to \mathbf{H}$.

This way we can think of any object $X \in \mathbf{H}$ of the $(\infty,1)$-topos equivalently as a space that is locally built from pieces of $\mathbf{H}$. With the above interpretation of $\mathbf{H}$ as the general abstract lump of cohesive points, this reproduces the intuition that $X \in \mathbf{H}$ is a space with this chesive structure.

 
### Structures inside a cohesive $(\infty,1)$-topos {#StructuresInside}

We list the geometric meaning of the various morphisms and structures in
a cohesive [[(∞,1)-topos]] over [[∞Grpd]]. (We follow the entries [[schreiber:structures in an (∞,1)-topos]] and [[schreiber:differential cohomology in an (∞,1)-topos]] where more motivation and justification for these interpretations can be found.)

Write

$$
 (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
 \mathbf{H}
  \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
 \infty Grpd
$$

for the given cohesive $(\infty,1)$-topos. Its objects $X,A \in \mathbf{H}$ we may think of as [[∞-groupoid]]s with cohesive structure. For instance in the case $\mathbf{H} = $ [[?LieGrpd]] they are $\infty$-groupoids with _smooth_ structure.  For $G \in \mathbf{H}$ an [[∞-group]] object we write $\mathbf{B}G \in \mathbf{H}$ for its internal [[delooping]] object.

We may think of a morphism $X \to \mathbf{B}G$ as being the [[cocycle]] for a [[principal ∞-bundle]] on $X$ and of

$$
  \mathbf{H}(X, \mathbf{B}G)
$$

as the [[∞-groupoid]] whose objects are $G$-principal $\infty$-bundles, whose morphisms are equivalences between these, and so on.

Then

* $\Gamma(X)$ is the _underlying $\infty$-groupoid_ of the cohesive $\infty$-groupoid $X$ (for instance an $\infty$-Lie groupoid with its smooth structure forgotten);

  if $X = \mathbf{B}G$ is the [[delooping]] of a [[group object]] $G$ in $\mathbf{H}$, then $\Gamma \mathbf{B}G = K(\Gamma(G),1)$ is the [[Eilenberg-MacLane space]] with the underlying [[discrete group]] $\Gamma(G)$ in degree 1.

* $\Pi(X)$ is the fundamental [[path ∞-groupoid]] of $X$: its [[k-morphism]]s are generated from $k$-dimensional smooth paths in $X$ and the $k$-morphisms of $X$ itself. Under the equivalence of $(\infty,1)$-toposes 

  $|-| :$  [[∞Grpd]] $\stackrel{\simeq}{\to}$ [[Top]] 


  we may think of $|\Pi(X)|$ as the _geometric realization_ of $X$. For instance if $X \in \infty LieGrpd$ is a [[paracompact manifold]], then $|\Pi(X)|$ is, up to [[weak homotopy equivalence]] its underlying topological space.

  If again $X = \mathbf{B}G$, then $\mathcal{B}G = |\Pi(\mathbf{B}G)|$ is the [[classifying space]] for the group $G$.

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

  If $A = \mathbf{B}G$ is the [[delooping]] of an [[∞-group]] object, then we may think of $\mathbf{\flat} \mathbf{B}G$ or rather the corresponding  $\Gamma\mathbf{B}G$ as being $K(G,1)$: the classifying object for $G$-principal bundles where all cohesive structure on $G$ has been forgotten.

  Accordingly, the canonical map

  $$
    \Gamma \mathbf{B}G \to \Pi \mathbf{B}G
  $$

  that apppears in the second clause of the definition of cohesive topos is the inclusion of the [[Eilenberg-MacLane space]] $K(G,1)$ into the topological [[classifying space]] $\mathcal{B}G$. Again, on [[cocycle]]s this is the map from flat bundles to the underlying bundles.





## Examples {#Examples}


+-- {: .un_def}
###### Definition

An **$(\infty,1)$-cohesive** over [[∞Grpd]] is

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

+-- {: .un_prop}
###### Example

* The $(\infty,1)$-topos $(\infty,1)Sh(TopBalls)$ is that of (generalized) **topological $(\infty,1)$-groupoids**.

  Aspects of this are studied in 

  * [[Dan Dugger]], _Sheaves and homotopy theory_ ([pdf](http://ncatlab.org/nlab/files/cech.pdf))

* The $(\infty,1)$-topos $(\infty,1)Sh(CartSp)$ is that of (generalized) [[∞-Lie groupoid]]s.

  The 0-[[truncated]] [[concrete sheaf|concrete]] objects in this are precisely the [[diffeological space]]s. Accordingly the general concrete objects here we may think of as **diffeological $\infty$-groupoids**.

* The $(\infty,1)$-topos $(\infty,1)Sh(ThCartSp)$ is that of (generalized) [[∞-Lie groupoid]]s that contain also [[infinitesimal object|infinitesimal]] $\infty$-Lie groupoids: [[∞-Lie algebroid]]s.


=--



## Applications

* As a context for geometric spaces and paths in geometric spaces, cohesive $(\infty,1)$-toposes are a natural context in which to formulate fundamental [[physics]]. See [[higher category theory and physics]] for more on that.

## References

The ordinary [[category theory|category theoretic]]-definition of a [[cohesive topos]] was proposed in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
{#Lawvere}

The observation that the further left adjoint $\Pi$ in a [[locally ∞-connected (∞,1)-topos]] defines an intrinsic notion of paths and [[geometric homotopy groups in an (∞,1)-topos]] was suggested by [[Richard Williamson]].

The observation that the further right adjoint $Codisc$ in a [[local (∞,1)-topos]] serves to characterize [[concrete sheaf|concrete (∞,1)-sheaves]] was amplified by [[David Carchedi]].

Some discussion is at

* [[Urs Schreiber]], _Cohesive $\infty$-Toposes_ ([blog entry](http://golem.ph.utexas.edu/category/2010/10/cohesive_toposes.html))

[[!redirects cohesive (∞,1)-topos]]

[[!redirects cohesive (∞,1)-toposes]]
[[!redirects cohesive (infinity,1)-toposes]]

[[!redirects cohesive (∞,1)-topoi]]
[[!redirects cohesive (infinity,1)-topoi]]
