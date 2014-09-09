
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

For $X$ a [[compact space|compact]], [[connected]], [[orientation|oriented]] 3-[[dimension|dimensional]] [[manifold]], write 

$$
  2 T X := T X \oplus T X
$$

for the [[direct sum of vector bundles|fiberwise direct sum]] of the [[tangent bundle]] with itself. Via the [[diagonal]] embedding

$$
  SO(3) \to SO(3) \times SO(3) \hookrightarrow SO(6)
$$

this naturally induces a [[special orthogonal group|SO(6)]]-[[principal bundle]]. 

+-- {: .num_prop}
###### Proposition

The underlying $SO(6)$-principal bundle of $2 T X$ always admits a [[lift of structure group|lift]] to a [[spin group|spin(6)]]-[[principal bundle]].

=--

+-- {: .proof}
###### Proof

By the sum-rule for [[Stiefel-Whitney classes]] (see at [SW class -- Axiomatic definition](Stiefel-Whitney+class#AxiomaticDefinition)) we have that 

$$
  w_2(2 T X) = 2 w_0(T X) \cup w_2(T X) + w_1(T X) w_1(T X)
  \,.
$$

Since $T X$ is assumed [[orientation|oriented]], $w_1(T X) = 0$ (since this is the [[obstruction]] to having an [[orientation]]). So $w_2(2 T X) = 0 \in H^2(X,\mathbb{Z}_2)$ and since this in turn is the further [[obstruction]] to having a [[spin structure]], this does exist.

=--

Therefore the following definition makes sense

+-- {: .num_defn}
###### Definition

A **2-framing** on a [[compact space|compact]], [[connected]], [[orientation|oriented]] 3-[[dimension|dimensional]] [[manifold]] $X$ is the [[homotopy class]] of a trivializations of the [[spin-group]]-[[principal bundle]] underlying [[Whitney sum|twice]] its [[tangent bundle]].

=--

More in detail, we may also remember the [[groupoid]] of 2-framings and the smooth structure on collections of them:

+-- {: .num_defn}
###### Definition

The [[moduli stack]] $2\mathbf{Frame}$ is the [[homotopy pullback]] in 

$$
  \array{
    2\mathbf{Frame} &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}SO(3) &\stackrel{}{\to}&
    \mathbf{B} Spin(6)
  }
$$

in [[Smooth∞Grpd]].

=--

In terms of this a 2-framing on $X$ with [[orientation]] $\mathbf{o} \colon X \to \mathbf{B}SO(3)$ is a lift $\hat {\mathbf{o}}$ in 

$$
  \array{
    && 2 \mathbf{Frame}
    \\
    & {}^{\mathllap{\hat {\mathbf{o}}}}\nearrow & \downarrow
    \\
    X &\stackrel{\mathbf{o}}{\to}& \mathbf{B}SO(3)
  }
  \,.
$$


## Properties

### Relation to bounding 4-manifolds
 {#RelationToBounding4Manifolds}

In ([Atiyah](#Atiyah1990)) it is shown how a framing on a compact connected oriented 3-manifold $X$ is induced a 4-manifold $Z$ with [[boundary]] $\partial Z \simeq X$. In fact, a framing is equivalently a choice of [[cobordism]] class of bounding 4-manifolds ([Kerler](#Kerler)).

Discussion of 2-framing entirely in terms of bounding 4-manifolds is for instance in ([Sawin](#Sawin)).

### Relation to String-structures

By ([Atiyah 2.1](#Atiyah)) a 2-framing of a 3-manifold $X$ is equivalently a  
$p_1$-[[twisted differential c-structures|structure]], where $p_1$ is the first [[Pontryagin class]], hence a homotopy class of a trivialization of

$$
  p_1(X) \colon X \to B SO(3) \stackrel{p_1}{\to} K(\mathbb{Z},4)
  \,.
$$

This perspective on framings is made explicit in ([Bunke-Naumann, section 2.3](#BunkeNaumann)). It is mentioned for instance also in ([Freed, slide 5](#Freed)).

## Related concepts

* [[framed manifold]]

* [[string structure]].

## References

The notion of "2-framing" is due to

* [[Michael Atiyah]], _On framings of 3-manifolds_ , Topology, Vol. 29, No 1, pp. 1-7 (1990) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/atiyahfr.pdf))
  {#Atiyah1990}

making explicit a structure which slightly implicit in the discussion of the [[path integral]] of [[Chern-Simons theory]] in 

* [[Edward Witten]], _Quantum field theory and the Jones Polynomial_ , Comm. Math. Phys.  121 (1989)

(see [Atiyah, page 6](#Atiyah)). For more on the role of 2-framings in [[Chern-Simons theory]] see also

* [[Daniel Freed]], Robert Gompf, _Computer calculation of Witten's 3-Manifold invariant_, Commun. Math. Phys. 141,79-117 (1991) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/freedgompf.pdf))

* {#Freed} [[Daniel Freed]], _Remarks on Chern-Simons theory_ ([pdf slides])
 

and for discussion in the context of the [[M2-brane]] from p. 7 on in 

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]] II: Twisted $String$ and $String^c$-structures_  ([arXiv:1007.5419](http://arxiv.org/abs/1007.5419)).

The relation to [[string structures]] is made explicit in section 2.3 of 

* {#BunkeNaumann} [[Ulrich Bunke]], [[Niko Naumann]], _Secondary Invariants for String Bordism and tmf_ ([arXiv:0912.4875](http://arxiv.org/abs/0912.4875))
 

Discussion in terms of bounding 4-manifolds is in 

* Thomas Kerler, _Bridged links and tangle presentations of cobordism categories_. Adv. Math., 141(2):207&#8211;281, (1999) ([arXiv:math/9806114](http://arxiv.org/abs/math/9806114))
 {#Kerler}

* Stephen F. Sawin, _Three-dimensional 2-framed TQFTS and surgery_ (2004) ([pdf](http://digitalcommons.fairfield.edu/cgi/viewcontent.cgi?article=1020&context=mathandcomputerscience-facultypubs))
 {#Sawin}

and page 9 of 

* Stephen Sawin, _Invariants of Spin Three-Manifolds From Chern-Simons Theory and Finite-Dimensional Hopf Algebras_ ([arXiv:math/9910106](http://arxiv.org/abs/math/9910106)).

See also 

* [[Greg Kuperberg]], _[MO comment](http://mathoverflow.net/a/4389/381)_ 

[[!redirects 2-framing]]
[[!redirects 2-framings]]
