
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

This page collects some links and other material related to the article

* [[Sergei Gukov]], [[Anton Kapustin]], 

  _Topological Quantum Field Theory, Nonlocal Operators, and Gapped Phases of Gauge Theories_ 

  ([arXiv:1307.4793](http://arxiv.org/abs/1307.4793))

The article considers the generalization of a phenomenon in [[spontaneous symmetry breaking]] in abelian ([[higher gauge theory|higher]]) [[gauge theory]], that was considered earlier in ([Banks-Seiberg 08](#BanksSeiberg08)), to _[[nonabelian cohomology|nonabelian]]_ [[higher gauge theory]], hence involving not just [[differential 1-form]] [[gauge potentials]] but 2-form gauge potentials ("nonabelian [[B-fields]]").

Specifically, in ([Banks-Seiberg 08, (2.4)-(2.9)](#BanksSeiberg08)) is an argument saying that some properties of the low energy limit of abelian [[Yang-Mills theory|Yang-Mills like]] [[gauge theories]] in four dimensions with ([[Higgs mechanism|Higgs-like]]) [[spontaneous symmetry breaking]] to a discrete gauge [[cyclic group]] $\mathbb{Z}_p$ are described by a dual [[BF-theory]], hence a [[higher gauge theory]] represented by a [[principal 2-connection|2-connection]] instead of an ordinary [[connection on a bundle|connection]]. Here the duality is [[electric-magnetic duality]], but applied not to the 1-form [[gauge field]] but to the [[Higgs boson]]-like [[scalar field]], whose magentic dual in 4d is indeed a $(4 - (0+1) - 1 = 2)$-form  [[higher gauge field]]. See at _[[connection on a 2-bundle]]_ for more on this.

In the nonabelian case the proposed mechanism is no longer [[electric-magnetic duality]] of a [[Higgs boson]]-like [[field (physics)|field]], but instead to condensation of [[monopoles]].

The abelian phenomenon is reviewed and expanded on in its relation to higher dimensional [[QFT with defects|defect]] [[quantum operators]] in section III. Generalization to the nonabelian case is then in section IV. An outlook on the relation to structures such as in [[geometric Langlands duality]] is in section V.




***

> under construction

#Contents#
* table of contents
{:toc}

## II. Surface operators in abelian gaueg theories

(...)

## III. TQFTs for abelian gapped phases

(...)

### A. Abelian Higgs phases

* [[Higgs mechanism]]

### B. Abelian confining phases

* [[confinement]]

### C. Oblique confining phases

(...)

### D. Mixed phases

(...)

## IV. TQFTs for nonabelian gapped phases

(...)

### A. Nonabelian Higgs phases

(...)

### B. Nonabelian confining phases

(...)

#### 1. Monopole condensation 

A notce concerning the discussion of [[monopoles]] on the bottom right of p. 5.

Let $G$ be a [[connected topological space|connected]] [[Lie group]]. A [[subgroup]] 

$$
  \Gamma_0 \hookrightarrow \pi_1(G)
$$

of its [[fundamental group]] defines a [[covering]] $t \colon H \to G$, exhibited by the following [[pasting diagram]] of [[homotopy pullbacks]] of [[smooth ∞-groupoids]]:

$$
  \array{
    \pi_1(G)/\Gamma_0 &\to& H &\to& \Pi(H) &\to& \mathbf{B}\pi_1(H) \simeq \mathbf{B}\Gamma_0 
    \\
    \downarrow && \downarrow^{\mathrlap{t}} && \downarrow^{\mathrlap{\Pi(t)}} && \downarrow
    \\
    \ast &\stackrel{e}{\to}& G &\stackrel{}{\to}& \Pi(G) &\stackrel{\tau_1}{\to}& \mathbf{B} \pi_1(G)
  }
$$

Here $(-) \to \Pi(-)$ is the [[unit of an adjunction|unit]] of the [[shape modality]]. In the given low degree case the above diagram can be checked explicitly by standard means, but it may be worthwhile to note that the whole situation follows fully generally as by the [Galois theory in cohesive ](cohesive+%28infinity,1%29-topos+--+structures#GaloisTheory) ([Schreiber, section 3.8.6](#SchreiberCohesive)).


#### 2. Nonabelian gerbes and nonabelian B-fields

* [[connection on a 2-bundle]]

* [[clutching construction]]

#### 3. A TQFT for a nonabelian confining phase

* [[BF-theory]]

### C. A TQFT for a nonabelian oblique confining phase

(...)


## References

The argument relating aspects of the low energy limit of [[spontaneous symmetry breaking]] in ordinary [[gauge theory]] by [[electric-magnetic duality]] of the [[Higgs boson]]-like field to [[BF-theory|BF]]-type [[higher gauge theory]] is in section 2 of

* [[Tom Banks]], [[Nathan Seiberg]], _Symmetries and Strings in Field Theory and Gravity_, Phys. Rev. D83:084019,2011 ([arXiv:1011.5120](http://arxiv.org/abs/1011.5120))
 {#BanksSeiberg08}

following discussion of [[D-brane]]/[[NS5-brane]] phenomena in 

* [[Juan Maldacena]], [[Gregory Moore]], [[Nathan Seiberg]], _D-brane Charges in Five-brane backgrounds_,  	JHEP 0110:005,2001 ([arXiv:hep-th/0108152](http://arxiv.org/abs/hep-th/0108152))

(...)

The formulation of [[principal 2-connections]] via their [[higher parallel transport]] used in section IV is from

* [[Urs Schreiber]],  [[Konrad Waldorf]], _Connections on non-abelian gerbes and their holonomy_, Theory and Applications of Categories, Vol. 28, 2013, No. 17, pp 476-540. ([TAC](http://www.tac.mta.ca/tac/volumes/28/17/28-17abs.html), [arXiv:0808.1923](http://arxiv.org/abs/0808.1923), <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SchrWalII+III">web</a>)

expanding on

* [[John Baez]], [[Urs Schreiber]], _Higher gauge theory_, in A. Davydov et al. _Categories in Algebra, Geometry and Mathematical Physics_, Contemp. Math. 431, AMS, Providence, Rhode Island, 2007, pp. 7-30 ([arXiv:math/0511710](http://arxiv.org/abs/math/0511710), [web](http://ncatlab.org/schreiber/show/differential+cohomology+in+a+cohesive+topos+--+references/#BaezSchreiber))


Some of the above comments on the formulation in [[smooth ∞-groupoids]] refer to 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
 {#SchreiberCohesive}

category: reference



