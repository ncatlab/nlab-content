

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The universal real Thom spectrum [[MO]] is a [[connective spectrum]] whose associated [[infinite loop space]] is the [[classifying space]] for [[cobordism]]:

$$
  \Omega^\infty M O \simeq \vert Cob_\infty \vert .
$$

In particular, $\pi_n M O$ is naturally identified with the set of [[cobordism classes]] of [[closed manifold|closed]] $n$-[[manifolds]] ([[Thom's theorem]]).

More abstractly, [[MO]] is the [[homotopy colimit]] of the [[J-homomorphism]] in [[Spectra]]

$$
  M O \simeq \underset{\longrightarrow}{\lim}(B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to Spectra)
$$

hence the "total space" of the universal [[spherical fibration]] on the [[classifying space]] $B O$ for (stable) [[real vector bundles]].

Given this, for any [[topological group]] $G$ equipped with a [[homomorphism]] to the [[orthogonal group]] there is a corresponding Thom spectrum

$$
  M G \simeq \underset{\longrightarrow}{\lim}(B G\to B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to Spectra)
  \,.
$$

This is considered particularly for the stages $G$ in the [[Whitehead tower]] of the [[orthogonal group]], where it yields $M$[[Spin group|Spin]], $M$[[String group]], etc. 

All these Thom spectra happen to naturally have the structure of [[E-∞ rings]] and $E_\infty$-ring homomorphisms $M O\to E$ into another $E_\infty$-ring $E$ are equivalently universal [[orientation in generalized cohomology|orientations in E-cohomology]]. On [[homotopy groups]] these are [[genera]] with [[coefficients]] in the underlying ring $\pi_\bullet(E)$.


## Definition

### For vector bundles

For $V \to X$ a [[vector bundle]], we have a [[weak homotopy equivalence]]

$$
  Th(\mathbb{R}^n \oplus V) \simeq S^n \wedge Th(V) \simeq \Sigma^n Th(V)
$$

between, on the one hand, the [[Thom space]] of the [[direct sum]] of $V$ with the trivial [[vector bundle]] of rank $n$ and, on the other, the $n$-fold [[suspension]] of the [[Thom space]] of $V$.

+-- {: .num_defn}
###### Definition

For $V \to X$ a [[vector bundle]], its **Thom spectrum** is the [[Omega spectrum]] $E_\bullet$ with

$$
  E_n \coloneqq (X^V)_n \coloneqq Th(\mathbb{R}^n \oplus V)
  \,.
$$ 

=--

Without qualifiers, _the_ Thom spectrum is that of the universal vector bundles:

+-- {: .num_defn}
###### Definition

For each $n \in \mathbb{N}$ let 

$$
  M O(n) := (B O)^{V(n)}
$$

be the Thom spectrum of the vector bundle $V(n)$ that is canonically [[associated bundle|associated]] to the $O(n)$-[[universal principal bundle]] $E O(n) \to B O(n)$ over the [[classifying space]] of the [[orthogonal group]] of dimension $n$.

The inclusions $O(n) \hookrightarrow O(n+1)$ induce a directed system of such spectra. The **Thom spectrum** is the [[colimit]]

$$
  M O := {\lim_\to}_n M O(n) 
  \,.
$$

=--

Instead of the sequence of groups $O(n)$, one can consider $SO(n)$, or $Spin(n)$, $String(n)$, $Fivebrane(n)$,..., i.e., any level in the [[Whitehead tower]] of $O(n)$. To any of these groups there corresponds a Thom spectrum, which is in turn related to oriented cobordism, spin cobordism, string cobordism, et cetera.

As a [[symmetric spectrum]]: [Schwede 12, Example I.2.8](#Schwede12)

### For spherical fibrations
 {#ForSphereBundles}

+-- {: .num_defn #ThomSpectrumForSphericalFibrations}
###### Definition

(...)

=--

### For $(\infty,1)$-module bundles
 {#ForInfinityModuleBundles}

We discuss the Thom spectrum construction for general [[(∞,1)-module bundle]]s.

+-- {: .num_prop}
###### Proposition

There is pair of [[adjoint (∞,1)-functors]]

$$
  (\Sigma^\infty \Omega^\infty \dashv gl_1)
  : 
  E_\infty Rings
   \stackrel{\overset{\Sigma^\infty \Omega^\infty}{\leftarrow}}{\underset{gl_1}{\to}}
  Spec_{con}
  \,,
$$

where $(\Sigma^\infty \dashv \Omega^\infty) : Spec \to Top$ is the [[stabilization]] adjunction between [[Top]] and [[Spec]] ($\Sigma^\infty$ forms the [[suspension spectrum]]), restricted to connective spectra.  The [[right adjoint]] is the _[[∞-group of units]]_-[[(∞,1)-functor]], see there for more details.

=--

This is ([ABGHR, theorem 2.1/3.2](#ABGHR)).

+-- {: .num_remark}
###### Remark

Here $gl_1$ forms the "[[general linear group]]-of rank 1"-spectrum of an [[E-∞ ring]]: its [[∞-group of units]]". The adjunction is the generalization of the adjunction

$$
  (\mathbb{Z}[-] \dashv GL_1) : 
   CRing \stackrel{\overset{\mathbb{Z}[1]}{\leftarrow}}{\underset{GL_1}{\to}}
  Ab
$$

between [[CRing]] and [[Ab]], where $\mathbb{Z}[-]$ forms the [[group ring]].

=--

+-- {: .num_defn}
###### Definition

Write 

$$
  b gl_1(R) := \Sigma gl_1(R)
$$

for the [[suspension]] of the group of units $gl_1(R)$. 

=--

This plays the role of the [[classifying space]] for $gl_1(R)$-[[principal ∞-bundle]]s. 

For $f : b \to b gl_1(R)$ a morphism (a [[cocycle]] for $gl_1(R)$-bundles) in [[Spec]], write $p \to b$ for the corresponding bundle: the [[homotopy fiber]]

$$
  \array{
     p &\to& * 
     \\
     \downarrow && \downarrow
     \\
     b &\stackrel{f}{\to}& b gl_1(R)
  }
  \,.
$$

Given a $R$-algebra $A$, hence an [[A-∞ algebra]] over $R$, exhibited by a morphism $\rho : R \to A$, the composite

$$
  \rho(f) : b \stackrel{f}{\to} b gl_1(R) \stackrel{\rho}{\to} b gl_1(A)
$$

is that for the corresponding [[associated ∞-bundle]].

We write capital letters for the underlying spaces of these spectra:

$$
  P \coloneqq \Sigma^\infty \Omega^\infty p
$$

$$
  B \coloneqq \Sigma^\infty \Omega^\infty b
$$

$$
  GL_1(R) \coloneqq \Sigma^\infty \Omega^\infty gl_1(R)
$$


+-- {: .num_defn #GeneralThomSpectrum}
###### Definition

The **Thom spectrum** $M f$ of $f : b \to gl_1(R)$ is the [[(∞,1)-pushout]]

$$
  \array{
    \Sigma^\infty \Omega^\infty R &\to& R
    \\
    \downarrow && \downarrow
    \\
    \Sigma^\infty \Omega^\infty p &\to& M f
  }
  \,,
$$

hence the [[derived functor|derived]] [[smash product]]

$$
  M f \simeq P \wedge_{GL_1(R)} R
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This means that a morphism $M f \to A$ is an $GL_1(R)$-equivariant map $P \to A$.

Notice that for $R = \mathbb{C}$ the [[complex number]]s, $B \to GL_1(R)$ is the cocycle for a [[circle bundle]] $P \to B$. A $U(1)$-equivariant morphism $P \to A$ to some [[representation]] $A$ is equivalently a [[section]] of the A-[[associated bundle]]. 

Therefore the Thom spectrum may be thought of as co-[[representable functor|representing]] spaces of sections of associated bundles

"$Hom(M f, A) \simeq \Gamma(P \wedge_{GL_1(R)} A)$".

=--

This is made precise by the following statement.

+-- {: .num_prop}
###### Proposition

We have an [[(∞,1)-pullback]] diagram

$$
  \array{
    E_\infty Alg_R(M f, A) &\stackrel{}{\to}& (...)
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{}{\to}& (...)
  }
$$

=--

This is ([ABGHR, theorem 2.10](#ABGHR)).

This definition does subsume the [above](ForSphereBundles) definition of Thom spectra for [[sphere bundles]] (hence also that for [[vector bundles]], by removing their [[zero section]]):

+-- {: .num_prop}
###### Proposition

Let $R = S$ be the [[sphere spectrum]]. Then for $f : b \to gl_1(S)$ a cocycle for an $S$-bundle, 

$$
  G := \Omega^\infty g : B \to B GL_1(S)
$$

is the classifying map for a [[spherical fibration]] over $B \in Top$. 

The Thom spectrum $M f$ of def. \ref{GeneralThomSpectrum} is equivalent to the Thom spectrum of the spherical fibration, according to def. \ref{ThomSpectrumForSphericalFibrations}.

=--

This is in ([ABGHR, section 8](#ABGHR)).

Equivalently the Thom spectrum is characterized as follows:

+-- {: .num_defn #ThomSpectrumAsHomotopyColimit}
###### Definition/Proposition

For $\chi \colon X \to  R Line$ a map to the [[∞-group]] of $R$-[[(∞,1)-lines]] inside $R Mod$, the corresponding Thom spectrum is the [[(∞,1)-colimit]]

$$
  \Gamma(\chi) \coloneqq
  \underset{\rightarrow}{\lim}
  \left(
    X \stackrel{\chi}{\to} Pic(R) \hookrightarrow R Mod
  \right)
  \,.
$$

This construction evidently extendes to an [[(∞,1)-functor]]

$$
  \Gamma \colon \infty Grpd_{/R Line} \to R Mod
  \,. 
$$


=--



This is ([Ando-Blumberg-Gepner 10, def. 4.1](#ABG10)), reviewed also as ([Wilson 13, def. 3.3](#Wilson13)).

+-- {: .num_remark}
###### Remark

This is the $R$-[[(∞,1)-module]] of [[sections]] of the [[(∞,1)-module bundle]] classified by $X \stackrel{\chi}{\to} Pic(R) \hookrightarrow R Mod$.

By the [[universal property]] of the [[(∞,1)-colimit]] we have for $\underline{R} \colon X \to R Mod$ the trivial $R$-bundle that 

$$
  Hom_{[X, R Mod]}(\chi, \underline{R})
  \simeq
  Hom_{R Mod}(\Gamma(\chi), R)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The section/Thom spectrum functor is the left [[(∞,1)-Kan extension]] of the canonical embedding $R Line \hookrightarrow R Mod$ along the [[(∞,1)-Yoneda embedding]]

$$
  R Line \hookrightarrow [R Line^{op}, \infty Grpd]
  \simeq \infty Grpd_{/R Line}
$$

(where the [[equivalence of (∞,1)-categories]] on the right is given by the [[(∞,1)-Grothendieck construction]]). In other words, it is the essentially unique [[(∞,1)-colimit]]-preserving [[(∞,1)-functor]]  $\infty Grpd_{/ R Line} \to R Mod$ which restricts along this inclusion to the canonical embedding.

=--

This observation appears as ([Wilson 13, prop. 4.4](#Wilson13)).

## Properties

### Relation to the cobordism ring

+-- {: .num_prop}
###### Proposition

The [[cobordism ring|cobordism group]] of un[[oriented]] $n$-[[dimension]]al [[manifold]]s is [[natural isomorphism|naturally isomorphic]] to the $n$th [[homotopy group]] of the Thom spectrum $M O$. That is, there is a natural isomorphism

$$
  \Omega^{un}_\bullet \simeq \pi_\bullet M O 
   :=
  {\lim_{\to}}_{k \to \infty} \pi_{n+k} M O(k)
  \,.
$$

=--

This is a seminal result due to ([Thom 54](#Thom54)), whose proof proceeds by the [[Pontryagin-Thom construction]]. The presentation of the following proof follows ([Francis, lecture 3](#Francis3)).

+-- {: .proof}
###### Proof

We first construct a map $\Theta : \Omega_n^{un} \to \pi_n M O$. 

Given a class $[X] \in \Omega_n^{un}$ we can choose a representative $X \in $ [[SmthMfd]] and a [[closed embedding]] $\nu$ of $X$ into the [[Cartesian space]] $\mathbb{R}^{n+k}$ of sufficiently large [[dimension]]. By the [[tubular neighbourhood theorem]] $\nu$ factors as the embedding of the [[zero section]] into the [[normal bundle]] $N_\nu$ followed by an [[open embedding]] of $N_\nu$ into $\mathbb{R}^{n+k}$

$$
  \array{
     X &&\stackrel{\nu}{\hookrightarrow}&& \mathbb{R}^{n+k}
     \\
     & \searrow && \nearrow_{\mathrlap{i}}
     \\
     && N_\nu
  }
  \,.
$$

Now use the [[Pontrjagin-Thom construction]] to produce an element of the [[homotopy group]] first in the [[Thom space]] $Th(N_\nu)$ of $N_\nu$ and then eventually in $M O$.  To that end, let

$$
  \mathbb{R}^{n+k} \to (\mathbb{R}^{n+k})^+ \simeq S^{n+k}
$$

be the map into the [[one-point compactification]]. Define a map

$$
  t : S^{n+k} \simeq (\mathbb{R}^{n+k})^+ \to Disk(N_\nu)/Sphere(N_\nu) \simeq Th(N_\nu)
$$

by sending points in the image of $Disk(N_\nu)$ under $i$ to their preimage, and all other points to the collapsed point $Sphere(N_\nu)$. This defines an element in the [[homotopy group]] $\pi_{n+k}(Th(N_\nu))$.

To turn this into an element in the homotopy group of $M O$, notice that  since $N_\nu$ is a [[vector bundle]] of [[rank]] $k$, it is the [[pullback]] by a map $\mu$ of the universal rank $k$ vector bundle $\gamma_k \to B O(k)$

$$
  \array{
    N_\nu \simeq \mu^* \gamma_k &\to& \gamma_k
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{\mu}{\to}& B O(k)
  }
  \,.
$$

By forming Thom spaces the top map induces a map

$$
  Th(N_\nu) \to Th(\gamma^k) =: M O(k)
  \,.
$$

Its composite with the map $t$ constructed above gives an element in $\pi_{n+k} M O(k)$

$$
  S^{n+k} \stackrel{t}{\to} Th(N_\nu) \to Th(\gamma^k) \simeq M O(k)
$$

and by $\pi_{n+k} M O(k) \to {\lim_\to}_k \pi_{n+k} M O(k) =: \pi_n M O$ this is finally  an element 

$$
  \Theta
  :
  [X]
   \mapsto
  (S^{n+k} \stackrel{t}{\to} Th(N_\nu) \to Th(\gamma^k) \simeq M O(k)) 
  \in
  \pi_n M O
  \,.
$$

We show now that this element does not depend on the choice of embedding $\nu : X \to \mathbb{R}^{n+k}$.

(...)

Finally, to show that $\Theta$ is an [[isomorphism]] by constructing an inverse.

For that, observe that the [[sphere]] $S^{n+k}$ is a [[compact topological space]] and in fact a [[compact object]] in [[Top]]. This implies that every map $f$ from $S^{n+k}$ into the [[filtered colimit]] 

$$
  Th(\gamma^k)  \simeq {\lim_\to}_s Th(\gamma^k_s)
  \,,
$$

factors through one of the terms as

$$
  f : S^{n+k} \to Th(\gamma^k_s) \hookrightarrow Th(\gamma^k)
  \,.
$$

By [[Thom's transversality theorem]] we may find an embedding $j : Gr_k(\mathbb{R}^s) \to Th(\gamma^k_s)$ by a [[transverse map]] to $f$. Define then $X$ to be the [[pullback]]

$$
  \array{
    X &\to& Gr_k(\mathbb{R}^s)
    \\
    \downarrow && \downarrow^{\mathrlap{j}}
    \\
    S^{n+k} &\stackrel{f}{\to}& Th(\gamma^k_s)
  }
  \,.
$$

We check that this construction provides an inverse to $\Theta$.

(...)

=--

+-- {: .num_remark }
###### Remark

The [[homotopy equivalence]] $\Omega^\infty M O \simeq \vert Cob_\infty \vert$ is the content of the [[Galatius-Madsen-Tillmann-Weiss theorem]], and is now seen as a part of the [[cobordism hypothesis]] theorem.

=--

### As a dual in the stable homotopy category
 {#AsDualObject}

Write [[Spec]] for the category of [[spectra]] and $Ho(Spec)$ for its standard [[homotopy category]]: the [[stable homotopy category]]. By the [[symmetric monoidal smash product of spectra]] this becomes a [[monoidal category]].

For $X$ any [[topological space]], we may regard it as an object in $Ho(Spec)$ by forming its [[suspension spectrum]] $\Sigma^\infty_+ X$. We may ask under which conditions on $X$ this is a [[dualizable object]] with respect to the smash-product monoidal structure.

It turns out that a sufficient condition is that $X$ a closed [[smooth manifold]] or more generally a [[compact topological space|compact]] Euclidean [[neighbourhood retract]]. In that case $Th(N X)$ -- the Thom spectrum of its [[normal bundle|stable normal bundle]] is the corresponding [[dual object]]. ([Atiyah 61](#Atiyah61), [Dold-Puppe 78](#DoldPuppe78)). This is called the [[Spanier-Whitehead dual]] of $\Sigma^\infty_+ X$.

Using this one shows that the [[trace]] of the identity on $\Sigma^\infty_+ X$ in $Ho(Spec)$ -- the categorical [[dimension]] of $\Sigma^\infty_+ X$ -- is the [[Euler characteristic]] of $X$.

For a brief exposition see ([PontoShulman, example 3.7](#PontoShulman)). For more see at _[[Spanier-Whitehead duality]]_.

### As the universal spherical fibration, from the $J$-homomorphism
 {#AsTheUniversalSphericalFibration}

The [[J-homomorphism]] is a canonical map $B O \to B gl_1(\mathbb{S})$ from the [[classifying space]] of the [[stable orthogonal group]] to the [[delooping]] of the [[infinity-group of units]] of the [[sphere spectrum]]. This classifies an "[[(∞,1)-vector bundle]]" of [[sphere spectrum]]-[[module spectrum|modules]] over $B O$ and this is the Thom spectrum.

So in terms of the [[(∞,1)-colimit]] description [above](#ForInfinityModuleBundles) we have

$$
  M O \simeq  \underset{\longrightarrow}{\lim}(B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to \mathbb{S}Mod = Spectra)
  \,.
$$

See at _[[orientation in generalized cohomology]]_ for more on this.

### $E_\infty$-ring structure

Sufficient condition for a Thom spectrum to have [[E-∞ ring]] structure is that it arises, as above, as the [[(∞,1)-colimit]] of a homomorphism of [[E-∞ spaces]]  $B \to A Line$ ([ABG 10, prop.6.21](#ABG10)).



### As the infinite cobordism category
 {#AsTheInfiniteCobordismCategory}

The [[geometric realization]] for the  [[(infinity,n)-category of cobordisms]] for $n \to \infty$ is the Thom spectrum

$$
  \vert Bord_\infty \vert \simeq \Omega^\infty MO
  \,.
$$

This is implied by the [[Galatius-Madsen-Tillmann-Weiss theorem]] and  by [[Jacob Lurie]]'s proof of the [[cobordism hypothesis]]. See also ([Francis-Gwilliam, remark 0.9](Francis3)).

## Cohomology

Under the [[Brown representability theorem]] the Thom spectrum represents the [[generalized (Eilenberg-Steenrod) cohomology]] theory called [[complex cobordism cohomology theory|cobordism cohomology theory]].

## Related concepts

* [[cobordism theory]]

* [[Thom space]], [[Thom isomorphism]], [[Pontryagin-Thom collapse map]]

* [[cobordism ring]]

[[!include generalized fiber integration synonyms - table]]

## References

### General

The relation between the homotopy groups of the Thom spectrum and the cobordism ring is due to


* {#Thom54} [[René Thom]], _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_ Comment. Math. Helv. 28, (1954). 17-86


Other original articles include

* {#Atiyah61} [[Michael Atiyah]], _Thom complexes_, Proc. London Math. Soc. (3), 11:291&#8211;310, 1961. 10 

Lecture notes include


* {#Francis3} [[John Francis]], _Topology of manifolds_ course notes (2010) ([web](http://math.northwestern.edu/~jnkf/classes/mflds/)) 

  Lecture 3 _Thom's theorem_ (notes by A. Smith) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/3thom.pdf))

  A remark of the relation of the Thom spectrum to [[(∞,n)-category of cobordisms]] for $n = \infty$ is in:

  Lecture 2 _Cobordisms_ (notes by [[Owen Gwilliam]]) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))
  
* {#Ebert12} [[Johannes Ebert]], _A lecture course on Cobordism Theory_, 2012 ([pdf](http://wwwmath.uni-muenster.de/u/jeber_02/skripten/bordism-skript.pdf))

* {#Freed13} [[Dan Freed]], lecture 10 of _Bordism: old and new_, 2013 ([pdf](http://www.ma.utexas.edu/users/dafr/bordism.pdf))


As [[symmetric spectra]]:

* {#Schwede12} [[Stefan Schwede]], Example I.2.6 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))

As [[orthogonal spectra]] and as [[equivariant spectra]]

* [[Stefan Schwede]], chapter V.4 of _[[Global homotopy theory]]_

Textbook discussion with an eye towards the [[generalized (Eilenberg-Steenrod) cohomology]] of [[topological K-theory]] and [[cobordism cohomology theory]] is in 

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability and cobordism_, Springer Monographs in Mathematics, 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))
 

A generalized notion of Thom spectra in terms of [[(∞,1)-module bundles]] is discussed in 

* {#ABGHR} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
  
a streamlined update of which is

* {#ABGHR14} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _An $\infty$-categorical approach to $R$-line bundles, $R$-module Thom spectra, and twisted $R$-homology_ ([arXiv:1403.4325](http://arxiv.org/abs/1403.4325))


Discussion of Thom spectra from the point of view of [[(∞,1)-module bundles]] is in 

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 

which is reviewed in

* {#Wilson13} [[Dylan Wilson]], _Thom spectra from the $\infty$ point of view_, 2013 ([pdf](http://www.math.northwestern.edu/~bwill/thom/DWthom4.pdf)) 
 

and in the context of [[motivic quantization]] via [[fiber integration in generalized cohomology|pushforward]] in [[twisted cohomology|twisted]] [[generalized cohomology]] in section 3.1 of 

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis 2013

### As dual objects in the stable homotopy category

The relation of Thom spectra to [[dualizable objects]] in the [[stable homotopy category]] is originally due to ([Atiyah 61](#Atiyah61)) and

* {#DoldPuppe78} [[Albrecht Dold]], [[Dieter Puppe]], _Duality, trace, and transfer_. In Proceedings of the International Conference on Geometric Topology (Warsaw, 1978), pages 81&#8211;102, Warsaw, 1980.
PWN.
 

* L. G. Lewis, Jr., [[Peter May]], M. Steinberger, and J. E. McClure, _Equivariant stable homotopy theory_, volume 1213 of Lecture Notes in Mathematics. Springer-Verlag, Berlin, 1986. With
contributions by J. E. McClure. 


A brief exposition appears as example 3.7 in 

* {#PontoShulman} [[Kate Ponto]] and [[Mike Shulman]], _Traces in symmetric monoidal categories_ ([arXiv:1107.6032](http://arxiv.org/abs/1107.6032), [slides](http://www.sandiego.edu/~shulman/papers/ccrtraces.pdf)).
 


[[!redirects Thom spectra]]

[[!redirects generalized Thom spectrum]]
[[!redirects generalized Thom spectra]]