[[!redirects (infinity,1)-vector bundle]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of an _$(\infty,1)$-module bundle_ is a [[categorification]]/[[homotopy theory|homotopification]] of the notion of a [[module bundle]]/[[vector bundle]], where [[fields]] and [[rings]] are replaced by [[∞-rings]] and [[modules]] by [[∞-modules]]; a central notion in [[parameterized stable homotopy theory]].

Recall that for $k$ a [[field]], a [[vector space]] is a $k$-[[module]], and a [[vector bundle]] over a [[space]] $X$ is classified by a morphism 
$\alpha : X \to k$[[Mod]] with $k$[[Mod]] regarded as an object in the relevant [[topos]]. For instance for _discrete_ or _flat_ vector bundles $k Mod$ is the [[category]] [[Vect]] of vector spaces.
There is the subcategory $k Line \hookrightarrow k Mod$ of 1-[[dimension]]al $k$-vector bundles, and morphisms that factor as $\alpha : X \to k Line \hookrightarrow k Mod$ are $k$-[[line bundle]]s.
In the discrete case the vector space of [[section]]s of the vector bundle classified by $\alpha$ is the [[colimit]] $\lim_\to \alpha$.

These statements [[categorification|categorify]] in a straightforward manner to the case where $k$ is generalized to a commutative [[∞-ring]]: an _[[E-∞ ring]]_ or _[[ring spectrum]]_ . Modules are replaced by [[module spectrum|module spectra]] and colimits by [[homotopy colimit]]s.

The resulting notion of $(\infty,1)$-vector bundles plays a central role in many constructions in [[orientation in generalized cohomology]], [[twisted cohomology]] and [[Thom isomorphism]]s.

Further generalization of the concept leads to [[(∞,n)-vector bundle]]s: an $(\infty,n)$-module over an [[E-∞-ring]] $K$ is an object of the [[(∞,n)-category]] $(\cdots (K Mod) Mod ) \cdots Mod$, where we are iteratively forming module $(\infty,k)$-categories over the monoidal $(\infty,k-1)$-category of $(\infty,k-1)$-modules, $n$ times.


## Discrete $(\infty,1)$-vector bundles

We discuss $(\infty,1)$-vector bundles internal to the [[(∞,1)-topos]] [[∞Grpd]] $\simeq$ [[Top]]. Since we are discussing objects with geometric interpretation, we are to think of this as the $(\infty,1)$-topos of _[[discrete ∞-groupoids]]_. 

Discussion of $\infty$-vector  bundles internal to _structured_ (non-discrete) $\infty$-groupoids is [below](#Structured).

### $\infty$-Modules and $\infty$-Module bundles

Assume in the following choices

* $K$ -- an [[E-∞ ring]] 

* $A$ -- a $K$-[[algebra spectrum|algebra]], 
  
  hence an [[A-∞ algebra]] in [[Spec]] equipped with a $\infty$-algebra homomorphism $K \to A$.

Denote

* $A Mod$ -- the [[(∞,1)-category]] of $A$-[[module spectrum|module spectra]].

+-- {: .num_defn}
###### Definition

For $X$ a [[discrete ∞-groupoid]] (often presented as a [[topological space]]), the [[(∞,1)-category]] of **$A$-module $\infty$-bundles** over $X$ is the [[(∞,1)-functor (∞,1)-category]]

$$
  A Mod(X) := Func(X, A Mod)
  \,.
$$

=--

In this form this appears as ([ABG def. 3.7](#ABG)). Compare this to the analogous definition at _[[principal ∞-bundle]]_. 

+-- {: .num_remark}
###### Remark

If $X$ is regarded as a [[topological space]] then the corresponding [[discrete ∞-groupoid]] is $\Pi X$, the [[fundamental ∞-groupoid]] of $X$ and the morphism encoding an $K$-module bundle over $X$ is reads

$$
  \alpha : \Pi(X) \to A Mod
  \,.
$$

This assignment of $A$-modules to points in $X$, of $A$-module morphism to paths in $X$ etc. may be regarded as the [[higher parallel transport]] of the (unique and flat, due to [[discrete ∞-groupoid|discreteness]]) [[connection on an ∞-bundle]] on $\alpha$. 

Equivalently, this morphism may be regarded as an [[∞-representation]] of $\Pi(X)$. Notaby if $X = B G$ is the [[classifying space]] of a [[discrete group]] or [[discrete ∞-group]], a $K$-module $\infty$-bundle over $X$ is the same as an [[∞-representation]] of $G$ on $A Mod$.

=--

### $\infty$-Lines and $\infty$-line bundles

+-- {: .num_defn}
###### Definition

Write 

$$
  A Line \hookrightarrow A Mod
$$

for the [[full sub-(∞,1)-category]] on the _$A$-lines_ : on those $A$-modules that are equivalent to $A$ as an $A$-module. The full subcatgeory of $A Mod(X)$ on morphisms factoring through this inclusion we call the $(\infty,1)$-catgeory of **$A$-line $\infty$-bundles**.

=--

This appears as ([ABG def. 3.12](#ABG)), ([ABGHR 08, 7.5](#ABGHR08)).

+-- {: .num_defn}
###### Definition

Let $A$ be an [[A-∞ algebra|A-∞]] [[ring spectrum]]. 

For $\Omega^\infty A$ the underlying [[A-∞ space]] and $\pi_0 \Omega^\infty A$ the ordinary [[ring]] of connected components, writ $(\pi_0 \Omega^\infty A)^\times$ for its [[group of units]]. 

Then the [[∞-group of units]] of $A$ is the [[(∞,1)-pullback]] $GL_1(A)$ in

$$
  \array{
    GL_1(A) &\to& \Omega^\infty A
    \\
    \downarrow && \downarrow
    \\
    (\pi_0 \Omega^\infty A)^\times &\to& \pi_0 \Omega^\infty A
  }
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

There is an [[equivalence in an (∞,1)-category|equivalence]] of [[∞-groups]] 

$$
  GL_1(A) \simeq Aut_{A Line}(A)
$$

of the [[∞-group of units]] of $A$ with the [[automorphism ∞-group]] of $A$, regarded canonically as a module over itself.

Since every $A$-line is by definition equivalent to $A$ as an $A$-module, there is accordingly, an [[equivalence of (∞,1)-categories]], in fact of [[∞-groupoids]]:

$$
 A Line \simeq B GL_1(A) \simeq B Aut(A)
$$

that identifies $A Line$ as the [[delooping]] [[∞-groupoid]] of either of these two [[∞-groups]].

=--

This appears in ([ABG, 3.6](#ABG)) ([p. 10](http://arxiv.org/pdf/1002.3004v2.pdf#page=10)). See also ([ABGHR 08, section 6](#ABGHR08)).


+-- {: .num_remark}
###### Remark

This means that every $A$-line $\infty$-bundle is canonically [[associated ∞-bundle|associated]] to a $GL_1(A)$-[[principal ∞-bundle]] over $X$ which is [[moduli space|modulated]] by a map $X \to B GL_1(A)$. 

=--

+-- {: .num_defn}
###### Definition

A $GL_1(A)$-[[principal ∞-bundle]] on $X$ is also called a **[[twisted cohomology|twist]]** -- or better: a **[[local coefficient ∞-bundle]]** -- for 
$A$-[[generalized (Eilenberg-Steenrod) cohomology|cohomology]] on $X$. 

=--

For the moment see _[[twisted cohomology]]_ for more on this.


### Sections and twisted cohomology
 {#SectionsAndTwistedCohomology}


+-- {: .num_defn}
###### Definition

The $A$-module of (dual) [[sections]] of an $(\infty,1)$-module bundle $f : X \to A Mod$ is the [[(∞,1)-colimit]] over this functor

$$
  X^f := \lim_\to (X \stackrel{\alpha}{\to} A Mod)
  \,.
$$

The corresponding _spectrum of sections_ is the $A$-dual 

$$
  \Gamma(f) := Mod_A(X^f, A)
  \,.
$$

=--

This is ([ABG, def. 4.1](#ABG)) and ([ABG, p. 15](#ABG)), ([ABG11, remark 10.16](#ABGII)).

+-- {: .num_remark}
###### Remark


For $f$ an $A$-line bundle  $\Gamma(f)$ is called in ([ABGHR 08, def. 7.27, remark 7.28](#ABGHR08)) the **[[Thom spectrum|Thom A-module]]** of $f$ and written $M f$. 

=--

Because for $A = S$ the [[sphere spectrum]], $M f$ is indeed the classical [[Thom spectrum]] of the spherical fibration given by $f$:

+-- {: .num_prop}
###### Proposition

For $K = S$ the [[sphere spectrum]], $f : X \to K Line = S Line$ an $S$-line bundle -- hence a spherical fibration, and $A$ any other $\infty$-ring with canonical inclusion $S \to A$, the Thom $A$-module of the composite $X \stackrel{f}{\to} S Mod \to A Mod$ is the classical [[Thom spectrum]] of $f$ tensored with $A$:

$$
  \Gamma(X \stackrel{f}{\to} S Line \to A Line \to A Mod)
  \simeq
   X^f \wedge_S A
  \,.
$$

=--

This is ([ABGHR 08, theorem 4.5](#ABGHR08)).


### Trivializations and orientations


+-- {: .num_defn}
###### Definition

For $f : X \to A Line$ an $A$-line $\infty$-bundle, its [[∞-groupoid]] of **trivializations** is the $\infty$-groupoid of lifts

$$
  \array{  
     && *
     \\
     & \nearrow & \downarrow
    \\
    X &\stackrel{f}{\to}& A Line
  }
  \,.
$$

For $K \to A$ the canonical inclusion and $f : X \to K Line$ a $K$-line bundle, we say that an **$A$-orientation** of $f$ is a trivialization of the associated $A$-line bundle $X \stackrel{f}{\to} K Line \to A Line$.

=--

That this encodes the notion of [[orientation in generalized cohomology|orientation in A-cohomology]] is around 
 ([ABGHR 08, 7.32](#ABGHR08)).


+-- {: .num_cor #ThomModuleInOrientedCase}
###### Corollary

Every trivialization/orientation of an $A$-line $\infty$-bundle $f : X \to A Line$ induces an equivalence

$$
  \Gamma(f) \simeq (\Sigma^\infty X )\wedge A
$$

of the $A$-module of sections of $f$ / the [[Thom spectrum|Thom A-module]] of $f$ with the [[homology|generalized A-homology]]-spectrum of $X$:

$$
  \pi_\bullet \Gamma(f) \simeq H_\bullet(X,A)   
  \,.
$$

=--

This appears as ([ABGHR 08, cor. 7.34](#ABGHR08)).

Therefore if $f$ is _not_ trivializable, we may regard its $A$-module of sections as encoding $f$-[[twisted cohomology|twisted A-cohomology]]:

+-- {: .num_defn}
###### Definition

For $f : X \to A Line$ an $A$-line $\infty$-bundle, the $f$-**[[twisted cohomology|twisted A-homology]] of $A$ is

$$
  H_\bullet^f(X, A) := \pi_\bullet(\Gamma(f)) := \pi_\bullet(M f)
  \,.
$$

The **$f$-[[twisted cohomology|twisted A-cohomology]] is**

$$
  H^\bullet_f(X,A) := \pi_0 A Mod(M f, \Sigma^\bullet A)
  \,.
$$

=--

## Structured $(\infty,1)$-vector bundles
 {#Structured}

We discuss now $(\infty,1)$-vector bundles in more general [[(∞,1)-toposes]].

(...)

## Applications

* The [[string topology]] operations on a compact [[smooth manifold]] $X$ may be understood as arising from a [[sigma-model]] [[quantum field theory]] with [[target space]] $X$ whose [[background gauge field]] is a flat $A$-line $\infty$-bundle $(P,\nabla)$ which is $A$-oriented over $X$, hence trivializabe over $X$ (for instance for $A = H \mathbb{Q}$ the [[Eilenberg-MacLane spectrum]] this may be the sphereical fibration of [[Thom spectrum|Thom spaces]] induced from the [[tangent bundle]] if the manifold is [[oriented]] in the ordinary sense). 

  By prop. \ref{ThomModuleInOrientedCase} this implies that the space of [[state]]s of the $\sigma$-model is the $A$-homology spectrum $\Gamma(P) \simeq X \edge A$ of $X$, and that for every suitable [[surface]] $\Sigma$ with incoming and outgoing boundary components $\partial_{in} \Gamma \stackrel{in}{\to} \Gamma \stackrel{out}{\leftarrow} \partial_{out} \Gamma$ the [[mapping space]] [[span]]

  $$
    X^{\partial_{in} \Gamma}
     \stackrel{X^{in}}{\leftarrow}
    X^{\Gamma}
     \stackrel{X^{out}}{\rightarrow}
    X^{\partial_{out} \Gamma}
  $$

  acts by [[path integral as a pull-push transform]] on these spaces of states

  $$
    (X^{out})_* (X^{in})^! : H_\bullet(X^{\partial_{in} \Gamma},A) \to 
     H_\bullet(X^{\partial_{out} \Gamma}, A)
     \,.
  $$

## Related concepts

* [[∞-representation]]

* [[twisted cohomology]]

* [[Picard ∞-stack]]

## References
 {#References}

A systematic discussion of discrete $(\infty,1)$-module bundles has a precursor in

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Michael Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

(discussing the [[string orientation of tmf]]) and is then discussed in more detail in the triple of articles

* {#ABGHR08} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 

* {#ABG} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 

* {#ABGII} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Parametrized spectra, multiplicative Thom spectra, and the twisted Umkehr map_ ([arXiv:1112.2203](http://arxiv.org/abs/1112.2203))
 

The last of these explains the relation to 

* [[Peter May|May]], Sigurdsson, _[[Parametrized Homotopy Theory]]_
 
A streamlined version of ([ABGHR 08](#ABGHR08)) appears as

* {#ABGHR14} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _An $\infty$-categorical approach to $R$-line bundles, $R$-module Thom spectra, and twisted $R$-homology_ ([arXiv:1403.4325](http://arxiv.org/abs/1403.4325))

Lecture notes on these articles are in 

* Ben Knudsen, Scott Slinker, Paul VanKoughnett, Brian Williams, and [[Dylan Wilson]], _Thom spectra reading course_ ([web](http://www.math.northwestern.edu/~bwill/thom/))

Interpretation of the  [[algebraic K-theory]] $K(R)$ of a [[ring spectrum]] $R$ (see at _[[iterated algebraic K-theory]]_) as the [[Grothendieck group]] of [[(∞,1)-module bundles]] over $R$: 

* [[John Lind]], _Bundles of spectra and algebraic K-theory_, Pacific J. Math. 285 (2016) 427-452 ([arXiv:1304.5676](https://arxiv.org/abs/1304.5676), [doi:10.2140/pjm.2016.285.427](https://doi.org/10.2140/pjm.2016.285.427))


[[!redirects (∞,1)-vector bundle]]

[[!redirects (infinity,1)-vector bundles]]
[[!redirects (∞,1)-vector bundles]]

[[!redirects (∞,1)-module bundle]]
[[!redirects (∞,1)-module bundles]]
[[!redirects (infinity,1)-module bundle]]
[[!redirects (infinity,1)-module bundles]]

[[!redirects (∞,1)-line]]
[[!redirects (∞,1)-lines]]
[[!redirects (infinity,1)-line]]
[[!redirects (infinity,1)-lines]]


[[!redirects (∞,1)-vector space]]
[[!redirects (∞,1)-vector spaces]]
[[!redirects (infinity,1)-vector space]]
[[!redirects (infinity,1)-vector spaces]]

[[!redirects (∞,1)-line bundle]]
[[!redirects (∞,1)-line bundles]]
[[!redirects (infinity,1)-line bundle]]
[[!redirects (infinity,1)-line bundles]]

[[!redirects ∞-line bundle]]
[[!redirects ∞-line bundles]]
[[!redirects infinity-line bundle]]
[[!redirects infinity-line bundles]]