
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General

The [[smash product]] on [[pointed topological spaces]] induces a smash product on [[spectra]].

This is the canonical [[tensor product]] in the [[symmetric monoidal (infinity,1)-category of spectra]]. There are various [[model category]] [[presentable (infinity,1)-category|presentations]] for which which are symmetric [[monoidal model categories]] (such as the [[highly structured spectra]]: [[S-modules]], [[symmetric spectra]] and [[orthogonal spectra]], but also for instance [[excisive functors]]). See at _[[symmetric monoidal category of spectra]]_ for more on this. Passing to the [[stable homotopy category]], it become a [[symmetric monoidal category]] under the smash product. Under mild assumptions, this is the essentially unique symmetric tensor product with [[unit]] the [[sphere spectrum]] ([Shipley 01](#Shipley01)).

### History

Historically the discussion proceeded in the opposite direction: available variants of the construction of smash products on [[sequential spectra]] (the "handicrafted" or "naive" smash products [Boardman 65](#Boardman65), [Adams 74, part III, section 4](#Adams74)) were found to yield a [[symmetric monoidal category]] structure _only_ after passage to the [[stable homotopy category]]. Then models via non-sequential [[highly structured spectra]] were discovered which do admit a [[symmetric smash product of spectra]] in the sense of 1-category theory, as do [[excisive functors]], see at _[[model structure on excisive functors]]_.

### As Day convolution spectra

Many versions of the smash product of spectra, [[symmetric smash product of spectra|symmetric or not]], arise as [[Day convolution]] products on a suitable [[enriched category|enriched]] [[monoidal category|monoidal]] version of a [[category]] of "index spaces".

The [[symmetric smash product of spectra]] on, in particular,  [[symmetric spectra]] and  [[orthogonal spectra]] is the Day convolution product for [[Top]]-[[enriched functors]] on monoidal categories of [[symmetric groups]] of [[orthogonal groups]], respectively ([MMSS 00, theorem 1.7 and section 21.](#MMSS00)).

Similarly the [[symmetric smash product of spectra]] on the [[model structure for excisive functors]] is Day convolution for [[sSet]]-[[enriched functors]] on the plain [[smash product]] of finite pointed [[simplicial sets]] ([Lydakis 98](#Lydakis98)).

See also at _[[functor with smash products]]_.

## Properties

### Graded commutativity
 {#GradedCommutativity}

The smash product of spectra exhibits a certain graded commutativity akin to the graded commutativity in the [[tensor product of chain complexes]] (in fact, under the [[stable Dold-Kan correspondence]] the latter maps to the former).

This comes down to the following basic fact about the [[smash product]] of [[pointed topological spaces]]:

+-- {: .num_prop #GradedCommutativityOfSmashOfSpheres}
###### Proposition

There are [[homeomorphisms]] between [[n-spheres]] and their [[smash products]]

$$
  \phi_{n_1,n_2}
  \;\colon\;
  S^{n_1} \wedge S^{n_2}
  \stackrel{\simeq}{\longrightarrow}
  S^{n_1 + n_2}
$$

such that in [[Ho(Top)]] there are [[commuting diagrams]] like so:

$$
  \array{
    (S^{n_1} \wedge S^{n_2}) \wedge S^{n_3}
    &&\stackrel{\simeq}{\longrightarrow}&&
    S^{n_1} \wedge (S^{n_2} \wedge S^{n_3})
    \\
    {}^{\mathllap{\phi_{n_1,n_2} \wedge id}}\downarrow 
    && && \downarrow^{\mathrlap{id \wedge \phi_{n_2,n_3}}}
    \\
    S^{n_1+n_2} \wedge S^{n_3}
    && &&
    S^{n_1}\wedge S^{n_2 + n_3}
    \\
    & {}_{\mathllap{\phi_{n_1+n_2, n_3}}}\searrow && \swarrow_{\mathrlap{\phi_{n_1,n_2+n_3}}}
    \\
    && 
    S^{n_1+n_2 + n_3}
  }
  \,.
$$

and

$$
  \array{
    S^{n_1} \wedge S^{n_2}
    &\stackrel{b_{n_1,n_2}}{\longrightarrow}&
    S^{n_2} \wedge S^{n_1}
    \\
    {}^{\mathllap{\phi_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\phi_{n_2,n_1}}}
    \\
    S^{n_1 + n_2}
    &\stackrel{(-1)^{n_1 n_2}}{\longrightarrow}&
    S^{n_1 + n_2}
  }
  \,,
$$

where here $(-1)^n \colon S^n \to S^n$ denotes the homotopy class of a [[continuous function]] of [[degree of a continuous function|degree]] $(-1)^n \in \mathbb{Z} \simeq [S^n, S^n]$.


=--


+-- {: .proof}
###### Proof

With the [[n-sphere]] $S^n$ realized as the [[one-point compactification]] of the [[Cartesian space]] $\mathbb{R}^n$, then $\phi_{n_1,n_2}$ is given by the identity on [[coordinates]] and the [[braiding]] homeomorphism

$$
  b_{n_1,n_2}
  \;\colon\;
  S^{n_1} \wedge S^{n_2}
  \stackrel{\sigma}{\longrightarrow}
  S^{n_2} \wedge S^{n_1}
$$

is given by permuting the [[coordinates]]:

$$
  (x_1, \cdots, x_{n_1}, y_1, \cdots, y_{n_2})
  \mapsto
  (y_1, \cdots, y_{n_2}, x_1, \cdots, x_{n_1})
  \,.
$$

This has [[degree of a continuous map|degree]] $(-1)^{n_1 n_2}$ .

=--

This statement passes to the [[suspension spectra]] $\Sigma^\infty S^n$ of the spheres ([Adams 74, part III, prop. 4.8](#Adams74), [Schwede 12, chapter II.4, prop. 4.4](#Schwede12)).

+-- {: .num_remark #WhySequentialSpectraHaveNoSymmetricSmashProduct}
###### Remark

The phenomenon in prop. \ref{GradedCommutativityOfSmashOfSpheres} is the reason why there is no [[symmetric smash product of spectra]] on plain [[sequential spectra]], and in fact no appropriate functorial product operation at all. 

To see this, observe, by [this proposition](sequential+spectrum#QuillenEquivalenceBetweenSequentialBFAndExcisiveFunctors), that sequential spectra are Quillen equivalent to the model category of [[excisive (infinity,1)-functors]]

$$
  Exc^1(\infty Grpd^{\ast/}_{fin}, \infty Grpd^{\ast/}) \hookrightarrow 
  Func(\infty Grpd^{\ast/}_{fin}, \infty Grpd^{\ast/})
$$

under an equivalence given by restricting from the domain of all [[pointed homotopy types|pointed]] [[finite homotopy types]] $\infty Grpd_{fin}^{\ast/}$ to its non-full subcategory $StdSpheres$ of standard spheres with just the adjuncts of suspension maps between them. 

$$
  \iota \colon StdSpheres \hookrightarrow \infty Grpd^{\ast/}_{fin}
  \,.
$$

$$
  Exc^1(\infty Grpd^{\ast/}_{fin}, \infty Grpd^{\ast/})
  \underoverset{\simeq}{\iota^\ast}{\longrightarrow}
  SeqSpectra
$$

Here $StdSpheres$ has objects $S^n_{std} \coloneqq (S^1)^{\wedge n}$ and as hom-spaces it has $StdSpheres(S^{m}, S^{n}) = S^{max(n-m,0)}$, identified as the [[adjunct]] of the canonical isomorphism $S^m \wedge S^{n-m} \to S^n$.

Hence $\iota^\ast$ identifies the $n$th component space of a sequential spectrum with the value $E(S^n)$ of an excisive functor on the $n$-sphere, and it identifies the structure map $S^1 \wedge E_n \to E_{n+1}$ with part of the [[enriched functor|enriched functoriality]] of the excisive functor.

Now in the model category of excisive functors, the correct smash product of spectra is the [[Day convolution]] over the symmetric monoidal category $(\infty Grpd^{\ast/}_{fin},\wedge)$.
The issue then is that the restricted hom-spaces of $StdSpheres$ do not see the non-trivial [[braiding]] of spheres in prop. \ref{GradedCommutativityOfSmashOfSpheres} anymore.

More concretely, the enriched category $StdSpheres$ does not inherit monoidal structure: defining the smash product on hom spaces requires permuting smash copies of spheres, which is not available.  Thus there is no Day convolution product on sequential spectra at all.

One could further restrict along $\mathbb{N} \to StdSpheres$ and use the monoidal structure $(\mathbb{N},+)$ to define at least a smash product on sequences of pointed spaces by [[Day convolution]] over $(\mathbb{N},+)$ as in ([MMSS 00, example 4.1](#MMSS00), [Hovey-Shipley-Smith 00, below prop. 2.3.4](#HoveyShipleySmith00)). But then in addition to the above problem that this does not give a functorial smash product on spectra (it will not respect the structure maps), moreover $(\mathbb{N},+)$ is trivially [[braided monoidal category|braided]] and so, again, under restriction of excisive functors to $\mathbb{N}$ there is no way to recover the information in the smash product of spectra that is encoded in the non-trivial braiding of the smash product of spheres.

=--


## Definitions

* _[smash product of sequential spectra](sequential+spectrum#SmashProduct)_

* _[smash product of excisive functors](model+structure+for+excisive+functors#SmashProduct)_

* _[smash product of symmetric spectra](symmetric+spectrum#SmashProduct)_

* _[smash product of orthogonal spectra](orthogonal+spectrum#SmashProduct)_


## References

The original "handicrafted" constructions of the smash product on the [[stable homotopy category]] are due to

* {#Boardman65} [[Michael Boardman]], _Stable homotopy theory_, mimeographed notes, University of Warwick, 1965 onwards

* [[Rainer Vogt]], _Boardman's stable homotopy category_, lectures, spring 1969

* {#Puppe73} [[Dieter Puppe]], _On the stable homotopy category_, Topology and its application (1973)  ([[PuppeStableHomotopyCategory.pdf:file]])

* {#Adams74} [[Frank Adams]], part III, section 4 of _[[Stable homotopy and generalised homology]]_, 1974

The smash product on [[connective spectra]] modeled as [[Gamma spaces]] is discussed in

* {#Lydakis98} Lydakis, _Smash products and $\Gamma$-spaces_, Math. Proc. Cam. Phil. Soc. 126 (1999), 311-328 ([pdf](http://hopf.math.purdue.edu/Lydakis/smash_gamma.pdf))

The [[symmetric smash product on spectra]] (see there for more) on [[highly structured ring spectra]] is discussed for instance in

for [[S-modules]]:

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland, (1995) pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

for [[symmetric spectra]]:

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))

* {#Schwede12} [[Stefan Schwede]], _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/people/schwede/SymSpec-v3.pdf))

Discussion of the smash product as a suitable [[Day convolution]] is, for [[highly structured spectra]], in

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

and for [[excisive functors]] in

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))


The uniqueness of the smash product on spectra is discussed in

* {#Shipley01} [[Brooke Shipley]], _Monoidal uniqueness of Stable homotopy theory_, Advances in Mathematics Volume 160, Issue 2, 25 June 2001, Pages 217&#8211;240 ([pdf](http://homepages.math.uic.edu/~bshipley/ideal.pdf))

[[!redirects smash products of spectra]]