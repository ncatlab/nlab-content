
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

_Equivariant cohomology_ is [[cohomology]] in the presence of and taking into account [[group]]-[[actions]] (and generally [[∞-group]] [[∞-actions]]) both on the domain space and on the [[coefficients]]. This is particularly interesting, and traditionally considered, for some choice of "geometric" [[cohomology]], hence cohomology inside an [[(∞,1)-topos]] possibly richer than that of [[geometrically discrete ∞-groupoids]].

We now first describe the idea of forming equivariant cohomology as such in an ambient [[(∞,1)-topos]] $\mathbf{H}$ 

* _[Equivariance](#IdeaEquivariance)_

and then afterwards indicate what this amounts to in someimportant special cases of choices of $\mathbf{H}$

* _[Geometricity](#IdeaGeometricity)_

### Equivariance
 {#IdeaEquivariance}

In the simplest situation the group action on the [[coefficients]] is trivial and one is dealing with cohomology of [[spaces]] $X$ that are equipped with a $G$-action ([[G-spaces]]). Here a [[cocycle]] in equivariant cohomology is an ordinary cocycle $c \in \mathbf{H}(X,A)$ on $X$, together with an [[equivalence]] $c \simeq g^\ast c$ [[coherence|coherently]] for each [[generalized element]] $g$ of $G$, hence is a cocycle which is $G$- _invariant_ , but only up to coherent choices of [[equivalences]].  Diagrammatically this means that where a non-equivariant [[cocycle]] on $X$ with [[coefficients]] in $A$ is just a map $c \colon X \to A$ (see at _[[cohomology]]_) an equivariant cocycle is a natural system of [[diagrams]] of the form

$$
  \array{
    X &\stackrel{c}{\longrightarrow}& A
    \\
    {}^{\mathllap{\rho_X(g)}}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{=}}
    \\
    X &\underset{c}{\longrightarrow}& A
  }
$$


Standard examples of this kind of equivariant cocycles are traditional [[equivariant bundles]] or cocycles in [[equivariant de Rham cohomology]]. This kind of equivariant cocycle is the same as just a single cocycle on the [[homotopy quotient]] $X//G$. Since a standard model for homotopy quotients is the [[Borel construction]], this kind of equivariant cohomology with trivial $G$-action on the coefficients is also called **Borel equivariant cohomology**.

In general the group $G$ also acts on the [[coefficients]] $A$, and then an equivariant cocycle is a map $c \;\colon\; X \to A$ which is invariant, up to equivalence, under the _joint_ action of $G$ on base space and coefficients. Diagrammatically this is a natural system of diagrams of the form

$$
  \array{
    X &\stackrel{c}{\longrightarrow}& A
    \\
    {}^{\mathllap{\rho_X(g)}}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\rho_A(g)}}
    \\
    X &\underset{c}{\longrightarrow}& A
  }
  \,.
$$

More concisely this means that an equivariant cocycle is a [[homotopy fixed point]] of the non-equivariant [[cocycle]] [[∞-groupoid]] $\mathbf{H}(X,A)$:

$$
  H^G(X,A) \simeq \pi_0(\mathbf{H}(X,A)^G)
  \,.
$$

By the discussion at _[[∞-action]]_ one may phrase this abstractly as follows: spaces and coefficients with $G$-[[∞-action]] are objects in the [[slice (∞,1)-topos]] of the ambient [[(∞,1)-topos]] $\mathbf{H}$

$$
  G Act_\infty(\mathbf{H})\simeq \mathbf{H}_{/\mathbf{B}G}
  \,,
$$

and $G$-equivariant cohomology is the [[dependent product]] [[base change]] along

$$
  \underset{\mathbf{B}G}{\prod} \;\colon\; \mathbf{H}_{/\mathbf{B}G} \longrightarrow \mathbf{H} 
$$

of [[internal homs]] in the slice over $\mathbf{B}G$:

$$
  H^G(X,A) \simeq \pi_0 \Gamma \left( 
    \underset{\mathbf{B}G}{\prod} [X,A]
  \right)
  \,.
$$

(This formally recovers the above special case of Borel-equivariant cohomology by the dual incarnation of the [[projection formula]] (theone denoted $\overline{\gamma}$ at _[Wirthm&#252;ller context -- The comparison maps](Wirthm&#252;ller+context#TheComparisonMaps)_), according to which $\prod_{\mathbf{B}G}[\rho_X,A]\simeq [\sum_{\mathbf{B}G} \rho_X,A] \simeq [X//G,A]$.)

Hence equivariant cohomology is a natural generalization of [[group cohomology]], to which it reduces when the base space is a point.

If here the cohomology is to be $\mathbb{Z}$-graded this means that the coefficients $A$ are the stages in a [[spectrum object]] in  $\mathbf{H}_{/\mathbf{B}G}$, which is a [[spectrum with G-action]]. These are hence the [[coefficients]] for equivariant [[generalized (Eilenberg-Steenrod) cohomology]]. (More generally one considers [[genuine G-spectra]] in [[equivariant stable homotopy theory]], see e.g. [Greenlees-May, p. 16](#GreenleesMay))).

Among the simplest non-trivial example of this $G$-equivariance with joint action on domain and coefficients is [[real-oriented cohomology|real oriented]] [[generalized cohomology theory]] such as notably [[KR-theory]], which is equivariance with respect to a $\mathbb{Z}_2$-action. This appears notably in [[type II string theory]] on [[orientifold]] backgrounds, where the extra group action on the coefficients is exhibited by what is called the [[worldsheet parity operator]]. The word "[[orientifold]]" is modeled on that of "[[orbifold]]" to reflect precisely this extra action (on coefficients) of non-Borel $\mathbb{Z}_2$-equivariant cohomology.

Similarly, [[equivariant K-theory]] is [[topological K-theory]] not just over spaces with $G$-action, but of vector bundles whose fibers are $G$-[[representations]], and such that the $G$-action on the base intertwines that on the fibers.


On the other extreme, when the $G$-action on the domain space happens to be trivial and only the coefficients have nontrivial $G$-action, then a cocycle in equivariant cohomology is a system of the form

$$
  \array{
    X &\stackrel{c}{\longrightarrow}& A
    \\
    {}^{=}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\rho_A(g)}}
    \\
    X &\underset{c}{\longrightarrow}& A
  }
$$

and hence is equivalently a map

$$
  c \;\coloneqq\; X \longrightarrow A^G
$$

to the [[homotopy fixed points]] $A^G$ of the coefficients (formed in $\mathbf{H}$! See [below](#IdeaGeometricity) for different incarnations ). 


Hence we have in summary:

[[!include equivariant cohomology -- table]]

### Geometricity 
 {#IdeaGeometricity}

Exactly what the above comes down to depends on the choice of ambient [[(∞,1)-topos]] $\mathbf{H}$ and of the way that $G$ is regarded as an [[∞-group]] object of $\mathbf{H}$. Some important choices are the following:

* **"coarse" equivariance.** For $\mathbf{H} = $ [[∞Grpd]] $\simeq L_{whe}$ [[Top]], and $G$ a [[discrete group]], regarded via its [[delooping]] groupoid/[[classifying space]] $\mathbf{B}G \in \mathbf{H}$, then $\mathbf{H}_{/\mathbf{B}G}$ is [[presentable (∞,1)-category|presented]] by the [[Borel model structure]] on the category of [[simplicial sets]] equipped with $G$-action. (This is also called the _coarse_ [[equivariant homotopy theory]], in view of the next examples). This theory only knows [[homotopy quotients]] and [[homotopy fixed points]] of $G$ (in particular cofibrant replacement in the [[Borel model structure]] is indeed given by the [[Borel construction]] and so Borel equivariant cohomology theory appears here whenever the [[coefficients]] have trivial $G$-action). In the case tha the domain itself is the points with trivial $G$-action then the equivariant cohomology here is precisely the [[group cohomology]] of $G$.

* **"fine" Bredon equivariance.** In order to bring in more geometric information one may equip [[G-spaces]] with information about the actual $G$-[[fixed points]], not just their [[homotopy fixed points]]. By general lore of [[topos theory]] this means to have all spaces be probe-able by fixed points, hence to have them be [[(∞,1)-presheaves]] on the [[global equivariant indexing category]] $Glob$, or if desired just on the [[global orbit category]] $Orb$, hence to set $(\mathbf{H} \to \mathbf{B}) =  (PSh_\infty(Glob) \to PSh_\infty(Orb))$, where the [[base (∞,1)-topos]] is that of [[orbispaces]] and $\mathbf{H}$ sitting [[cohesion|cohesively]] over it is the "[[global equivariant homotopy theory]]" proper (see there). 

  Now we have $\mathbf{B}G \in \mathbf{H}$ naturally via the [[(∞,1)-Yoneda embedding]] and the [[slice (∞,1)-topos]] $\mathbf{B}_{/\mathbf{B}G} \simeq L_{fpwe} G Top $ is the traditional [[equivariant homotopy theory]] presented by the "fine" model structure on [[G-spaces]] whose weak equivalences are the $H$-fixed point wise [[weak homotopy equivalences]] for all suitble subgroups $H \hookrightarrow G$. The [[spectrum objects]] here are what are called [[spectra with G-action]] or "[[naive G-spectra]]".
See at _[[Elmendorf's theorem]]_ for details. By the discussion there every object in the fine model structure if fibrant and cofibrant replacement here is given by passage to [[G-CW complexes]], so that the [[derived hom spaces]] computing cohomology are the ordinary $G$-[[fixed points]] of the [[mapping spectra]] from such as [[G-CW complex]] into the coefficient spectrum (this is traditionally motivated via detour through [[genuine G-spectra]], see e.f. [Greenlees-May, equation (3.7)](#GreenleesMay)).

  Cohomology with [[Eilenberg-MacLane object]]-[[coefficients]] in $PSh_\infty(Orb)_{/\mathbf{B}G}$ is what [[Glen Bredon]] originally considered as what is now called _[[Bredon cohomology]]_. 

* **fully geometric equivariance.** More complete geometric information is retained if one takes $\mathbf{H} = $ [[ETop∞Grpd]] or $= $[[Smooth∞Grpd]], which by the discussion at [[canonical topology]] means to not only test on [[moduli stacks]] $\mathbf{B}G$ of [[compact Lie groups]] (as in the [[global equivariant indexing category]]) but on _all_ topological/[[smooth ∞-stacks]]. Then again $G$ itself embeds canonically, and now its equivariant cohomology now is refined Segal-Brylinski-[[Lie group cohomology]] (see the discussion there).

In general one may (and should) consider equivariant cohomology for any ambient [[(∞,1)-topos]] $\mathbf{H}$ and any [[∞-group]] object $G \in Grp(\mathbf{H})$. But traditional literature on [[equivariant homotopy theory]]/equivariant cohomology considers specifically only the choice $\mathbf{H} = PSh_\infty(Orb)$ (and only somewhat implicitly,in fact traditional literature explicitly considers $\infty$-presheaves on the $G$-[[orbit category]] $Orb_G$. This relates to the above via the [standard](over-%28infinity%2C1%29-topos#SheavesOnBigSite) equivalence $PSh_\infty(Orb)_{/\mathbf{B}G} \simeq PSh_\infty(Orb_{/\mathbf{B}G}) \simeq PSh_\infty(Orb_G)$. 

## Presentations

> under construction

(...) [[Elmendorf theorem]] (...) [[Borel model structure]] (...)

## Borel equivariant cohomology 
 {#Borel}

We first state the [[category theory|general abstract]] definition of _[[Borel equivariant cohomology]]_ and then derive from it the more concrete formulations that are traditionally given in the literature.

+-- {: .standout}

[[Borel equivariant cohomology]] is the [[cohomology]] of [[action groupoids]] ([[homotopy quotients]]/[[Borel constructions]]).

=--

For standard [[cohomology]] in the [[(∞,1)-topos]] $\mathbf{H} =$ [[Top]] these [[action groupoid]]s of a [[group]] $G$ acting on a [[topological space]] $X$ are traditionally known as the [[Borel construction]] $\mathcal{E}G \times_G X$.

Recall from the discussion at [[cohomology]] that in full generality we have a notion of cohomology of an object $X$ with coefficients in an object $A$ whenever $X$ and $A$ are objects of some [[(∞,1)-topos]] $\mathbf{H}$. The cohomology set $H(X,A)$ is the set of connected components in the [[hom-object]] [[∞-groupoid]] of maps from $X$ to $A$: $H(X,A) = \pi_0 \mathbf{H}(X,A)$.

Recall moreover from the discussion at [[space and quantity]] that objects of an [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-topos of (∞,1)-sheaves]] have the interpretation of [[∞-groupoid]]s with extra structure. For instance for $(\infty,1)$-sheaves on a [[site]] of  smooth test spaces such as [[Diff]] these objects have the interpretation of [[Lie ∞-groupoid]]s.

In this case, for $X$ some such [[∞-groupoid]] with structure, let $X_0  \hookrightarrow X$ be its 0-truncation, which is the [[space]] of [[object]]s of $X$, the [[discrete groupoid|categorically discrete groupoid]] underlying $X$. We think of the morphisms in $X$ as determining which points of $X_0$ are related under some kind of action on $X_0$, the 2-morphisms as relating these relations on some higher action, and so on. **Equivariance** means, roughly: functorial transformation behaviour of objects on $X_0$ with respect to this "action" encoded in the morphisms in $X$. This is the intuition that is made precise in the following

In the simple special case that one should keep in mind, $X$ is for instance the [[action groupoid]] $X = X_0//G$ of the [[action]], in the ordinary sense, of a [[group]] $G$ on $X_0$: its morphisms $x \to g(x)$ connect those objects of $X_0$ that are related by the action by some group element $g \in G$.

It is natural to consider the [[relative cohomology]] of the inclusion $X_0 \hookrightarrow X$. Equivariant cohomology is essentially just another term for relative cohomology with respect to an inclusion of a space into a ($\infty$-)groupoid.

+-- {: .un_defn}
###### Definition (equivariant cohomology)

In some [[(∞,1)-topos]] $\mathbf{H}$ the **equivariant cohomology** with coefficient in an object $A$ of a 0-truncated object $X_0$ with respect to an action encoded in an inclusion $X_0 \hookrightarrow X$ is simply the $A$-valued cohomology $H(X,A)$ of $X$.

More specifically, an **equivariant structure** on an $A$-cocycle $c : X_0 \to A$ on $X_0$ is a choice of extension $\hat c$

$$
  \array{
    X_0 &\to& A
    \\
    \downarrow & \nearrow_{\hat c}
    \\
    X
  }
  \,.
$$

i.e. a lift of $c$ through the projection $\mathbf{H}(X,A) \to \mathbf{H}(X_0,A)$.

=--




### Examples 

#### Group cohomology 

By comparing the definition of equivariant cohomology with that of [[group cohomology]] one sees that group cohomology can be equivalently thought of as being **equivariant cohomology of the point**.

#### Equivariant bundles

For $G$ some [[group]] let $G Bund$ be the [[stack]] of $G$-[[principal bundle]]s. Let $K$ be some finite group (just for the sake of simplicity of the example) and let $K \to Aut(X_0)$ be an action of $K$ on a space $X_0$. Let $X = X_0 // K$ be the corresponding [[action groupoid]].

Then a cocycle in the $K$-equivariant cohomology $H(X_0//K, G Bund)$ is

* a $G$-[[principal bundle]] $P \to X$ on $X$;

* for each $k \in K$ an [[isomorphism]] of $G$-principal bundles $\lambda_k : P \to k^* P$

* such that for all $k_1, k_2 \in K$ we have $\lambda_{k_2}\circ \lambda_{k_1} = \lambda_{k_2\cdot k_1}$.

#### Local systems -- flat connections

For $X_0$ a [[space]] and $X := P_n(X_0)$ a version of its [[path n-groupoid]] we have a canonical inclusion $X_0 \hookrightarrow P_n(X_0)$ of $X_0$ as the collection of constant paths in $X_0$.

Consider for definiteness $\Pi(X_0) := \Pi_\infty(X_0)$, the [[path ∞-groupoid]] of $X_0$. (All other cases are in principle obtaind from this by truncation and/or strictification).

Then for  $A$ some coefficient $\infty$-groupoid, a morphism $g : X_0 \to A$ can be thought of as classifying a $A$-[[principal ∞-bundle]] on the space $X_0$.

On the other hand, a morphism out of $P_n(X_0)$ is something like a flat [[connection on a bundle|connection]] (see there for more details) on this principal $\infty$-bundle, also called an $A$-[[local system]]. (More details on this are at [[schreiber:differential cohomology]]).

Accordingly, an extension of $g : X_0 \to A$ through the inclusion $X_0 \hookrightarrow \Pi(X)$ is the process of equipping a principal $\infty$-bundle with a flat connection.

Comparing with the above definition of eqivariant cohomology, we see that flat connections on bundles may be regarded as **path-equivariant structures** on these bundles.

This is therefore an example of equivariance which is not with respect to a global [[group]] action, but genuinely a [[groupoid]]al one.

#### Equivariant de Rham cohomology

* [[equivariant de Rham cohomology]]

### Remarks

When pairing equivariant cohomology with other variants of cohomology such as [[twisted cohomology]] or [[differential cohomology]] one has to exercise a bit of care as to what it really is that one wants to consider. A discussion of this is (beginning to appear) at [[schreiber:differential equivariant cohomology]].





## Bredon equivariant cohomology {#Bredon}

See also

* [[Bredon cohomology]]

### Preliminary remarks

According to the [[nPOV]] on [[cohomology]], if $X$ and $A$ are objects in an [[(∞,1)-topos]], the 0th cohomology $H^0(X;A)$ is $\pi_0(Map(X,A))$, while if $A$ is a [[groupoid object in an (∞,1)-category|group object]], then $H^1(X;A)= \pi_0(Map(X,B A))$.  More generally, if $A$ is $n$ times [[delooping|deloopable]], then $H^n(X;A) = \pi_0(Map(X, B^n A)$.  In [[Top]], this gives you the usual notions if $A$ is a (discrete) group, and in general, $H^1(X;A)$ classifies [[principal ∞-bundle]]s in whatever [[(∞,1)-topos]].

Now consider the $(\infty,1)$-topos $G Top$ of $G$-equivariant spaces, which can also be described as the [[(∞,1)-presheaf|(∞,1)-presheaves]] on the [[orbit category]] of $G$.  For any other group $\Pi$ there is a notion of a principal $(G,\Pi)$-bundle (where $G$ is the group of equivariance, and $\Pi$ is the structure group of the bundle), and these are classified by maps into a classifying $G$-space $B_G \Pi$.  So the principal $(G,\Pi)$-bundles over $X$ can be called $H^0(X;B_G \Pi)$.  If we had something of which $B_G \Pi$ was a [[delooping]], we could call the principal $(G,\Pi)$-bundles "$H^1(X;?)$", but there does not seem to be such a thing.  It seems that $B_G \Pi$ is not connected, in the sense that ${*}\to B_G \Pi$ is not an [[effective epimorphism]] and thus $B_G \Pi$ is not the quotient of a [[groupoid object in an (∞,1)-category|group object]] in $G Top$.

### $G$-equivariant spectra

If we have an object $A$ of our $(\infty,1)$-topos that can be delooped infinitely many times, then we can define $H^n(X;A)$ for any integer $n$ by looking at all the spaces $\Omega^{-n} A = B^n A$.  These integer-graded [[cohomology group]]s are closely connected to each other, e.g. they often have [[cup product]]s or [[Steenrod square]]s or [[Poincare duality]], so it makes sense to consider them all together as a _[[cohomology theory]]_ .  We then are motivated to put together all of the objects $\{B^n A\}$ into a [[spectrum object]], a single object which encodes all of the cohomology groups of the theory.  A general spectrum is a sequence of objects $\{E_n\}$ such that $E_n \simeq \Omega E_{n+1}$; the stronger requirement that $E_{n+1} \simeq B E_n$ restricts us to "connective" spectra, those that can be produced by successively delooping a single object of the $(\infty,1)$-topos.  In [[Top]], the most "basic" spectra are the [[Eilenberg-MacLane spectrum|Eilenberg-MacLane spectra]] produced from the input of an ordinary abelian group.

Now we can do all of this in $G Top$, and the resulting notion of spectrum is called a **[[naive G-spectrum]]**: a sequence of $G$-spaces $\{E_n\}$ with $E_n \simeq \Omega E_{n+1}$.  Any naive $G$-spectrum represents a cohomology theory on $G$-spaces.  The most "basic" of these are "Eilenberg-Mac Lane $G$-spectra" produced from **coefficient systems**, i.e. abelian-group-valued presheaves on the  [[orbit category]].  The cohomology theory represented by such an Eilenberg-Mac Lane $G$-spectrum is called an (integer-graded) [[Bredon cohomology]] theory.

It turns out, though, that the cohomology theories arising in this way are kind of weird.  For instance, when one calculates with them, one sees [[torsion]] popping up in odd places where one wouldn't expect it.  It would also be nice to have a [[Poincare duality]] theorem for $G$-manifolds, but that fails with these theories.  The solution people have come up with is to widen the notion of "[[loop space object|looping]]" and "[[delooping]]" and thereby the grading: 

instead of just looking at $\Omega^n = Map(S^n, -)$, we look at $\Omega^V = Map(S^V,-)$, where $V$ is a finite-dimensional [[representation]] of $G$ and $S^V$ is its [[one-point compactification]].  Now if $A$ is a $G$-space that can be [[delooping|delooped]] "$V$ times," we can define $H^V(X;A) = \pi_0(Map(X,\Omega^{-V} A)$.  If $A$ can be delooped $V$ times for all representations $V$, then our integer-graded cohomology theory can be expanded to an **[[RO(G)-grading|RO(G)-graded]] cohomology theory**, with cohomology groups $H^\alpha(X;A)$ for all formal differences of representations $\alpha = V - W$.  The corresponding notion of spectrum is a **[[genuine G-spectrum]]**, which consists of spaces $E_V$ for all representations $V$ such that $E_V \simeq \Omega^{W-V} E_W$.  A naive Eilenberg-Mac Lane $G$-spectrum can be extended to a genuine one precisely when the coefficient system it came from can be extended to a [[Mackey functor]], and in this case we get an **$RO(G)$-graded Bredon cohomology theory** .

$RO(G)$-graded Bredon cohomology has lots of formal advantages over the integer-graded theory.  For instance, the torsion that popped up in odd places before can now be seen as arising by "shifting" of something in the cohomology of a point in an "off-integer dimension," which was invisible to the integer-graded theory.  Also there is a [[Poincare duality]] for $G$-manifolds: if $M$ is a $G$-manifold, then we can embed it in a representation $V$ (generally not a trivial one!) and by [[Thom space]] arguments, obtain a Poincare duality theorem involving a dimension shift of $\alpha$, where $\alpha$ is generally not an integer (and, apparently, not even uniquely determined by $M$!).  Unfortunately, however, $RO(G)$-graded Bredon cohomology is kind of hard to compute.

For more see at _[[equivariant stable homotopy theory]]_ and _[[global equivariant stable homotopy theory]]_.

### Examples

* $\mathbb{Z}_2$-equivariant cohomology theories: [[KR-theory]], [[MR-theory]]

* [[modular group]]-equivariance: [[modular equivariant elliptic cohomology]]


## Multiplicative equivariant cohomology

For [[multiplicative cohomology theories]] there is a further refinement of equivariance where the equivariant cohomology groups are built from global sections on a [[sheaf]] over cerain systems of [[moduli spaces]]. For more on this see at 

* [Equivariant multiplicative cohomology](http://ncatlab.org/nlab/show/A+Survey+of+Elliptic+Cohomology+-+A-equivariant+cohomology#equivariant)

* [[equivariant elliptic cohomology]]


## Related concepts

* [[equivariance]], [[equivariant structure]]

* [[equivariant bundle]], [[equivariant connection]] 

* [[equivariant stable homotopy theory]], [[global equivariant stable homotopy theory]]

* [[Segal conjecture]]

* [[equivariant K-theory]], [[equivariant operator K-theory]], [[equivariant KK-theory]]

  * [[Baum-Connes conjecture]], [[Green-Julg theorem]], [[Atiyah-Segal completion theorem]]

  * [[quantization commutes with reduction]]

* [[equivariant elliptic cohomology]]

[[!include homotopy type representation theory -- table]]

## References

### General

A quick introduction is in 

* {#GreenleesMay} [[John Greenlees]], [[Peter May]], section 3 of _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

More details are in 

* {#May96} [[Peter May]], _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comeza&#732;na, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))


* Matvei Libine, _Lecture Notes on Equivariant Cohomology_ ([arXiv](http://arxiv.org/abs/0709.3615))

For a brief modern surves see also the first three sections of

* [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], _The Arf-Kervaire problem in algebraic topology: Sketch of the proof_ ([[HHRKervaire.pdf:file]])

  (with an eye towards application to the [[Arf-Kervaire invariant problem]])


* blog on [Localization techniques in Equivariant Cohomology](http://www.aimath.org/wiki/localization/index.php/Main_Page)

### In complex oriented generalized cohomology theory
 {#InComplexOrientedGeneralizedCohomologyTheory}

Equivariant [[complex oriented cohomology theory]] is discussed in the following articles. 

* [[Michael Hopkins]], [[Nicholas Kuhn]], [[Douglas Ravenel]], _Generalized group characters and complex oriented cohomology theories_, J. Amer. Math. Soc. 13 (2000), 553-594 ([publisher](http://www.ams.org/journals/jams/2000-13-03/S0894-0347-00-00332-5/), [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/hkr.pdf))

  (This deals with "naive" Borel-equivariant complex oriented cohomology, but discusses general [[character]] expressions and explicit formulas for equivariant [[Morava K-theory|K(n)]]-cohomology.)

Specifically equivariant [[complex cobordism cohomology]] is discussed in 

* {#tomDiek70} [[Tammo tom Dieck]], _Bordism of $G$-manifolds and integrability theorems, Topology 9 (1970) 345-358

* {#Abrams13a} [[William Abram]], _Equivarisnt complex cobordism_, 2013 ([web](http://deepblue.lib.umich.edu/handle/2027.42/99796), [pdf](http://deepblue.lib.umich.edu/bitstream/handle/2027.42/99796/abramwc_1.pdf?sequence=1))

* [[William Abram]], [[Igor Kriz]], _The equivariant complex cobordism ring of a finite abelian group_ ([pdf](http://www.math.lsa.umich.edu/~ikriz/cobordism13022-1.pdf))


The following articles discuss equivariant [[formal group laws]]:

* [[John Greenlees]], _Equivariant formal group laws and complex oriented cohomology theories_, Homology Homotopy Appl. Volume 3, Number 2 (2001), ii-451 ([EUCLID](http://projecteuclid.org/euclid.hha/1139840255))

* [[William Abram]], _On the equivariant formal group law of the equivariant complex cobordism ring_, ([arXiv:1309.0722](http://arxiv.org/abs/1309.0722))

  (also [Abrams 13a, section III](#Abrams13a)).

See also the references at _[[equivariant elliptic cohomology]]_.

### In differential geometry

Equivariant degree-2 $U(1)$-[[Lie group cohomology]] is discussed in

* [[Kai Behrend]], [[Ping Xu]], Bin Zhang, _Equivariant gerbes over compact simple Lie groups_ ([arXiv](http://arxiv.org/abs/math/0306183v1))


[[!redirects Borel cohomology]]

[[!redirects equivariant cohomology theory]]
[[!redirects equivariant cohomology theories]]