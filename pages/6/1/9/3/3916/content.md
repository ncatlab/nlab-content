+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Given an [[embedding of topological spaces|embedding]] of [[smooth manifolds]] $i \colon X \hookrightarrow Y$ of [[codimension]] $n$, the _Thom collapse map_ ([Thom 54](#Thom54)) is the [[continuous function]] from $Y$ to the [[n-sphere]] which assigns **asymptotic normal distance** from the [[submanifold]], measured 

1. in [[direction vector|direction]] [[orthogonality|perpendicular]] to the submanifold, with respect to a [[normal framing]];

1. asymptotically, regarding all points outside a [[tubular neighbourhood]] as being [[one-point compactification|at infinity]].

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=24">
<img src="https://ncatlab.org/nlab/files/CohomotopyChargeAsymptoticDistanceII.jpg" width="630">
</a>
</center>

> graphics grabbed from [SS 19](Cohomotopy+charge#SatiSchreiber19)


For maximal codimension $n$, hence for 0-dimensional [[submanifolds]], hence for [[configuration space of points|configurations of points]], this is alternatively known as the "electric field map" ([Salvatore 01](cohomotopy+charge#Salvatore01) following [Segal 73, Section 1](cohomotopy+charge#Segal73), see also [Knudsen 18, p. 49](cohomotopy+charge#Knudsen18)) or the "scanning map" ([Kallel 98](cohomotopy+charge#Kallel98)).

The [[homotopy class]] of the Thom collpase map may be regarded as the _[[Cohomotopy charge]]_ of the submanifolds, as measured in $n$-[[Cohomotopy]]-[[generalized cohomology|cohomology theory]].

The PT collapse is a useful approximation to the would-be [[left inverse]] of the [[embedding of topological spaces]]

As such, it is is used to define pushforward of [[cohomology]]-classes along $i$ ("[[Umkehr maps]]"). It also appears as the key step in [[Thom's theorem]].

## Definition


### Component definition in topological spaces
 {#ComponentDefinitionInTopologicalSpaces}

All [[topological spaces]] in the following are taken to be [[compact space|compact]].

Consider $X$ and $Y$ two [[manifolds]] and 

$$
  i \colon X \hookrightarrow Y
$$ 

an [[embedding]].  

Write 

* $N_i X \coloneqq i^* T Y/ T X $ for the [[normal bundle]];

* $Th(N_i X)$ for the [[Thom space]] of the normal bundle; 

* $f \colon N_i X \longrightarrow Y$ for any choice of [[tubular neighbourhood]] of $i$.


+-- {: .num_defn #CollapseMap}
###### Definition

The **collapse map** (or the _Pontrjagin-Thom construction_) associated to $i$ and the choice of tubular neighbourhood $f$ is 

$$
  c_i 
    \colon 
  Y 
    \to 
  Y/(Y - f(N_i X)) 
    \stackrel{\simeq}{\to}
  Th(N_i X)
  \,,
$$

where the first morphism is the [[projection]] onto the [[quotient]] and the second is the canonical [[homeomorphism]] to the [[Thom space]] of the [[normal bundle]].

=--

+-- {: .num_defn #RefinedCollapseMap}
###### Remark

Since in the construction of remark \ref{CollapseMap} every point of $N_i X$ is associated to a particular point of $X$, the collapse map lifts to a map

$$ 
  Y 
    \longrightarrow 
  X_+ \wedge Th(N_i X)
$$

from $Y$ to the [[smash product]] of the [[Thom space]] (canonically regarded as a [[pointed topological space]]) and the topological space $X$ with a base point adjoined.

=--

(e.g. [Rudyak 98, p. 317](#Rudyak98))

+-- {: .num_example #ForEmbeddingsIntoAnNSphere}
###### Example

Of particular interest is the case where $Y$ in the above is a [[Cartesian space]] $\mathbb{R}^{dim X + k}$ or rather its [[one-point compactification]], the [[n-sphere|sphere]] $S^{dim X + k}$. By the [[Whitney embedding theorem]], for every $n \in \mathbb{N}$ there exists an $k \in \mathbb{N}$ such that every [[manifold]] $X$ of [[dimension]] $n$ has an [[embedding]] $X \hookrightarrow \mathbb{R}^{n+k} \to S^{n+k}$. In this case the collapse map of def. \ref{CollapseMap} has the form

$$
  S^{n+k} \longrightarrow Th(N_i X)
  \,.
$$

Composing this further with the canonical map $N_i X \longrightarrow E O(k) \underset{O(k)}{\times} \mathbb{R}^{k}$ to the universal vector bundle of rank $k$ yields a map

$$
  S^{n+k} \longrightarrow M O(k)
$$

from to the $k$th space in the [[Thom spectrum]] $M O$. This hence defines an element in the [[homotopy group of a spectrum|homotopy group]] $\pi_{k}(M O)$ of the [[Thom spectrum]]. [[Thom's theorem]] says that all elements in the homotopy groups of $M O$ arise this way, and that they retain precisely the information of the [[cobordism]] [[equivalence class]] of manifolds $X$. 
 
In this case the refined Thom collapse map of def. \ref{RefinedCollapseMap} is of the form

$$
  S^{n+k}
    \longrightarrow 
  X_+ \wedge Th(N_i X)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


The refined map in example \ref{ForEmbeddingsIntoAnNSphere} lifts to a morphism of [[spectra]] 

$$
  \mathbb{S} \longrightarrow \Sigma_+^\infty X \wedge \Sigma^{-n-k} Th(N_i X)
$$ 

where $\mathbb{S}$ denotes the [[sphere spectrum]] and $Th(N_i X)$ now the [[Thom spectrum]] of the normal bundle.  

This morphism is the [[unit of an adjunction]] which exhibits the [[suspension spectrum]] $\Sigma_+^\infty X$ as a [[dualizable object]] in the [[stable homotopy category]], with [[dual object]] $\Sigma^{-n-k} Th(N_i X)$.  See at _[[Atiyah duality]]_ and at _[[n-duality]]_.

=--

Equivalently, one may proceed as follows. For a framed manifold i.e. a manifold $M^n$ with a chosen trivialization of the normal bundle $N_i (M^n)$ in some $\mathbf{R}^{n+r}$ one has $T N_i(M^n)\cong \Sigma^r(M^n_+)$ where $M^n_+$ is the union of $M^n$ with a disjoint base point. Identify a sphere $S^{n+r}$ with a one-point compactification  $\mathbf{R}^{n+r}\cup \{\infty\}$. Then the Pontrjagin-Thom construction is the map $S^{n+r}\to Th(N_i X)$ obtained by collapsing the complement of the interior of the unit disc bundle $D(N_i M^n)$ to the point corresponding to $S(N_i M^n)$ and by mapping each point of $D(N_i M^n)$ to itself. Thus to a framed manifold $M^n$ one associates the composition

$$
S^{n+r}\to Th(N_i X)\cong \Sigma^r M^n_+\to S^r
$$

and its homotopy class defines an element in $\pi_{n+r}(S^r)$. 


### Abstract definition in terms of duality
 {#AbstractDefinitionInTermsOfDuality}

The following is a more abstract description of Pontryagin-Thom collapse in the [[stable homotopy theory]] of [[sphere spectrum]]-[[(∞,1)-module bundles]]. 

+-- {: .num_defn #SpanierDualityOperation}
###### Definition

Write

$$
  D \coloneqq (-)^\vee\circ \Sigma^\infty_+ \coloneqq L_{whe} Top \to \mathbb{S}Mod
$$

for the [[Spanier-Whitehead duality]] map which sends a [[topological space]] first to its [[suspension spectrum]] and then that to its [[dual object]] in the [[(∞,1)-category of spectra]].

=--

([ABG 11, def 10.3](#ABG11)).

+-- {: .num_prop}
###### Proposition

For $X$ a [[compact manifold]], let $X \to \mathbb{R}^n$ be an [[embedding]] and write $S^n \to X^{\nu_n}$ for the classical [[Pontryagin-Thom collapse map]] for this situation, and write

$$
  \mathbb{S} \to X^{-T X}
$$

for the corresponding [[looping]] map from the [[sphere spectrum]] to the [[Thom spectrum]] of the negative [[tangent bundle]] of $X$. Then [[Atiyah duality]] produces an [[equivalence]]

$$
  X^{- T X} \simeq D X
$$

which identifies the [[Thom spectrum]] with the [[dual object]] of $\Sigma^\infty_+ X$ in $\mathbb{S} Mod$ and this constitutes a [[commuting diagram]]

$$
  \array{
    && X^{- T X}
    \\
    & \nearrow & \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbb{S}
    &\underset{D(X \to \ast)}{\to}&
    D X
  }
$$

identifying the classical [[Pontryagin-Thom collapse map]] with the abstract [[dual morphism]] construction of prop. \ref{SpanierDualityOperation}.

More generally, for $W \hookrightarrow X$ an [[embedding]] of [[manifolds]], then [[Atiyah duality]] identifies the [[Pontryagin-Thom collapse maps]] 

$$
  \mathbb{S} \to X^{-T X} \to W^{- T W}
$$

with the abstract [[dual morphisms]]

$$
  \mathbb{S} \to D X \to D W
  \,.
$$


=--

([ABG 11, prop. 10.5](#ABG11)).

+-- {: .num_remark}
###### Remark

Given now $E \in CRing_\infty$ an [[E-∞ ring]], then the [[dual morphism]] $\mathbb{S} \to D X$ induces under [[smash product]] a similar Pontryagin-Thom collapse map, but now not in [[sphere spectrum]]-[[(∞,1)-modules]] but in $E$-[[(∞,1)-modules]].

$$
  E \to D X \otimes_{\mathbb{S}} E
  \,.
$$

The image of this under the $E$-[[generalized cohomology theory|cohomology]] functor produces 

$$
  [D X \otimes_{\mathbb{S}} E, E] \to E
  \,.
$$

If now one has a [[Thom isomorphism]] ($E$-[[orientation in generalized cohomology|orientation]]) $ [D X \otimes_{\mathbb{S}} E, E] \simeq [X,E]$ that identifies the cohomology of the dual object with the original cohomology, then together with produces the [[Umkehr map]]

$$
  [X,E] \simeq [D X \otimes_{\mathbb{S}} E, E] \to E
$$

that pushes the $E$-cohomology of $X$ to the $E$-cohomology of the point. Analogously if instead of the terminal map $X \to \ast$ we start with a more general map $X \to Y$.

More generally a [[Thom isomorphism]] may not exists, but $[D X \otimes_{\mathbb{S}} E, E]$ may still be equivalent to a [[twisted cohomology]]-variant $[X,E]_{\chi}$ of $[X,E]$, namely to $[\Gamma_X(\chi),E]$, where $\chi \colon \Pi(X) \to E Line \hookrightarrow E Mod$ is an ([[flat (∞,1)-bundle|flat]]) $E$-[[(∞,1)-module bundle]] on $X$ and and $\Gamma \simeq \underset{\to}{\lim}$ is the [[(∞,1)-colimit]] (the [[generalized Thom spectrum]] construction). In this case the above yields a _[[twisted Umkehr map]]_.


=--

([ABG 10, 9.1](#ABG10))

## Properties

### General

+-- {: .num_prop}
###### Proposition

For given $i$ all collapse maps for different choices of [[tubular neighbourhood]] $f$ are [[homotopy|homotopic]].

=--

+-- {: .proof}
###### Proof

By the fact that the space of [[tubular neighbourhood]]s (see there for details) is [[contractible]].

=--

### Relation between cohomotopy and cobordism

For $X$ a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $D$, the [[Pontryagin-Thom construction]] (e.g. [Kosinski 93, IX.5](#Kosinski93)) identifies the [[set]] 

$$
  SubMfd_{/bord}^{d}(X)
$$

of [[cobordism classes]] of  [[closed manifold|closed]] and [[normally framed submanifolds]] $\Sigma \overset{\iota}{\hookrightarrow} X$ of [[dimension]] $d$ inside $X$ with the [[cohomotopy]] $\pi^{D-d}(X)$ of $X$ in degree $D- d$

$$
  SubMfd_{/bord}^{d}(X)
    \underoverset{\simeq}{PT}{\longrightarrow}
  \pi^{D-d}(X)
  \,.
$$

(e.g. [Kosinski 93, IX Theorem (5.5)](#Kosinski93))

In particular, by this [[bijection]] the canonical [[group]] [[structure]] on [[cobordism groups]] in sufficiently high [[codimension]] (essentially given by [[disjoint union]] of [[submanifolds]]) this way induces a group structure on the cohomotopy sets in sufficiently high degree.



## Related concepts

* [[Thom's theorem]]

* [[Thom isomorphism]]

[[!include generalized fiber integration synonyms - table]]


## References



[[!include Pontryagin-Thom construction -- references]]


See also:


* [[Ralph Cohen]], John Klein, _Umkehr Maps_ ([arXiv:0711.0540](http://arxiv.org/abs/0711.0540))

* [[Victor Snaith]], _Stable homotopy around the arf-Kervaire invariant_, Birkhauser 2009

The general abstract formulation in [[stable homotopy theory]] is in sketched in section 9 of

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 
and is in section 10 of

* {#ABG11} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Parametrized spectra, multiplicative Thom spectra, and the twisted Umkehr map_ ([arXiv:1112.2203](http://arxiv.org/abs/1112.2203))
 
with an emphases on [[parameterized spectra]].

### Stratified versions

Instead of relating (structured) cobordisms with homs into Thom spectra, one may also relate [[stratified space|stratified]] cobordisms with homs into [[cell complex|cell complexes]]. A version of this relation is spelled out in *Section VII.4* of:

* {#BRS} Sandro Buonchristiano, Colin Rourke, and Brian Sanderson. _A geometric approach to homology theory_. Vol. 18. Cambridge University Press, 1976.

The stratified Pontrjagin-Thom construction may also be considered in higher categorical terms, where it relates functors between [[geometric computad|geometric computads]] to [[manifold diagram|manifold diagrams]]. This is discussed at:

* {#DornCategoricalTP} [[Christoph Dorn]], _The categorical Pontryagin-Thom construction_. [link](https://cxdorn.github.io/tcptc/)

[[!redirects Pontrjagin-Thom construction]]
[[!redirects Pontryagin-Thom construction]]

[[!redirects Pontryagin-Thom collaps map]]
[[!redirects Pontrjagin-Thom collaps map]]
[[!redirects Pontrjagin-Thom collapse map]]

[[!redirects Thom collapse map]]
[[!redirects Thom collapse maps]]
[[!redirects Thom collaps map]]
[[!redirects Thom collaps maps]]

[[!redirects Pontrjagin-Thom collapse]]
[[!redirects Pontryagin-Thom collapse]]
[[!redirects Thom collapse]]

[[!redirects Pontryagin-Thom collapse map]]

[[!redirects Pontryagin-Thom collapse maps]]
[[!redirects Pontrjagin-Thom collapse maps]]

[[!redirects Pontrjagin-Thom collapse construction]]
[[!redirects Pontrjagin-Thom collapse constructions]]
[[!redirects Pontryagin-Thom collapse construction]]
[[!redirects Pontryagin-Thom collapse constructions]]

