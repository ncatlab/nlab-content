

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

In the general terminology of _$n$-[[framing]]_, a _2-framing_ of a [[manifold]] $\Sigma$ of [[dimension]] $d \leq 2$ is a trivialization of $T \Sigma \oplus \mathbb{R}^{2-d}$.

In [Atiyah 90](#Atiyah1990) the term "2-framing" is instead used for a trivialization of the double of the tangent bundle of a 3-manifold. So this is a different concept, but it turns out to be closely related to the _3-framing_ (in the previous sense) of surfaces.

For $X$ a [[compact space|compact]], [[connected]], [[orientation|oriented]] 3-[[dimension|dimensional]] [[manifold]], write 

$$
  2 T X \coloneqq T X \oplus T X
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

A **2-framing** in the sense of ([Atiyah 90](#Atiyah1990)) on a [[compact space|compact]], [[connected]], [[orientation|oriented]] 3-[[dimension|dimensional]] [[manifold]] $X$ is the [[homotopy class]] of a trivializations of the [[spin-group]]-[[principal bundle]] underlying [[Whitney sum|twice]] its [[tangent bundle]].

=--

More in detail, we may also remember the [[groupoid]] of 2-framings and the smooth structure on collections of them:

+-- {: .num_defn}
###### Definition

The [[moduli stack]] $At2\mathbf{Frame}$ is the [[homotopy pullback]] in 

$$
  \array{
    At2\mathbf{Frame} &\to& *
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
    && At 2 \mathbf{Frame}
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

In ([Atiyah](#Atiyah1990)) it is shown how a framing on a compact connected oriented 3-manifold $X$ is induced by a 4-manifold $Z$ with [[boundary]] $\partial Z \simeq X$. In fact, a framing is equivalently a choice of [[cobordism]] class of bounding 4-manifolds ([Kerler](#Kerler)).

Discussion of 2-framing entirely in terms of bounding 4-manifolds is for instance in [Sawin 2004](#Sawin04).

### Relation to String-structures
 {#RelationToStringStructures}

By ([Atiyah 2.1](#Atiyah1990)) an Atiyah 2-framing of a 3-manifold $X$ is equivalently a  
$p_1$-[[twisted differential c-structures|structure]], where $p_1$ is the first [[Pontryagin class]], hence is a homotopy class of a trivialization of

$$
  p_1(X) \colon X \to B SO(3) \stackrel{p_1}{\to} K(\mathbb{Z},4)
  \,.
$$

This perspective on Atiyah 2-framings is made explicit in ([Bunke-Naumann, section 2.3](#BunkeNaumann)). It is mentioned for instance also in ([Freed, page 6, slide 5](#Freed08)).



## Related concepts

* [[framed manifold]]

* [[p1-structure]], [[string structure]].

* [[spin Chern-Simons theory]]

## References

The notion of "2-framing" in the sense of framing of the double of the tangent bundle is due to

* {#Atiyah1990} [[Michael Atiyah]], _On framings of 3-manifolds_ , Topology, Vol. 29, No 1, pp. 1-7 (1990) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/atiyahfr.pdf))
  

making explicit a structure which slightly implicit in the discussion of the [[perturbation theory|perturbative]] [[path integral]] [[quantization of 3d Chern-Simons theory]] in 

* [[Edward Witten]], _Quantum field theory and the Jones Polynomial_ , Comm. Math. Phys.  121 (1989)

reviewed for instance in

* {#Young} M. B. Young, section 2 of _Chern-Simons theory, knots and moduli spaces of connections_ ([pdf](http://www.math.sunysb.edu/~myoung/CS.pdf))

(see [Atiyah, page 6](#Atiyah)). For more on the role of 2-framings in [[Chern-Simons theory]] see also

* [[Daniel Freed]], Robert Gompf, _Computer calculation of Witten's 3-Manifold invariant_, Commun. Math. Phys. 141,79-117 (1991) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/freedgompf.pdf))

* [[Gregor Masbaum]], section 2 of _Spin TQFT and the Birman-Craggs Homomorphism_, Tr. J. of Mathematics 19 (1995)  [pdf](http://journals.tubitak.gov.tr/math/issues/mat-95-19-2/pp-189-199.pdf)

* {#Freed08} [[Daniel Freed]], _Remarks on Chern-Simons theory_ ([arXiv:0808.2507](http://arxiv.org/abs/0808.2507), [pdf slides](http://www.ma.utexas.edu/users/dafr/MSRI_25.pdf))
 

and for discussion in the context of the [[M2-brane]] from p. 7 on in 

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]] II: Twisted $String$ and $String^c$-structures_  ([arXiv:1007.5419](http://arxiv.org/abs/1007.5419)).

The relation to $p_1$-structure is made explicit in 

* {#BunkeNaumann} [[Ulrich Bunke]], [[Niko Naumann]], section 2.3 of _Secondary Invariants for String Bordism and tmf_, Bull. Sci. Math. 138 (2014), no. 8, 912&#8211;970 ([arXiv:0912.4875](http://arxiv.org/abs/0912.4875))
 
* C. Blanchet, N. Habegger, [[Gregor Masbaum]], [[Pierre Vogel]], _Topological quantum field theories derived from the Kauffman bracket_, Topology Vol 34, No. 4, pp. 883-927 (1995) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/bhmv.pdf))



More discussion in terms of bounding 4-manifolds:

* {#Kerler}Thomas Kerler, _Bridged links and tangle presentations of cobordism categories_. Adv. Math., 141(2):207&#8211;281, (1999) ([arXiv:math/9806114](http://arxiv.org/abs/math/9806114))
 
* {#Sawin04} [[Stephen F. Sawin]]: *Three-dimensional 2-framed TQFTS and surgery*,  Journal of Knot Theory and its Ramifications **13** 7 (2004) 947-996 &lbrack;[pdf](http://digitalcommons.fairfield.edu/cgi/viewcontent.cgi?article=1020&context=mathandcomputerscience-facultypubs), [doi:10.1142/S0218216504003536](https://doi.org/10.1142/S0218216504003536)&rbrack;
 
* [[Stephen F. Sawin]], page 9 of: _Invariants of Spin Three-Manifolds From Chern-Simons Theory and Finite-Dimensional Hopf Algebras_, Advances in Mathematics **165** 1 (2002) 35-70 &lbrack;[arXiv:math/9910106](http://arxiv.org/abs/math/9910106), [doi:10.1006/aima.2000.1935](https://doi.org/10.1006/aima.2000.1935)&rbrack;
  > (cf. also at *[[spin Chern-Simons theory]]*)

and more discussion for 3-manifolds with boundary:

* {#KerlerLyubashenko01} Thomas Kerler, [[Volodymyr Lyubashenko]], section 1.6.1 of _Non-semisimple topological quantum field theories for 3-manifolds with corners_, Lecture notes in mathematics 2001

See also 

* [[Greg Kuperberg]]$\;$&lbrack;[MO:a/4389](http://mathoverflow.net/a/4389/381)&rbrack;

[[!redirects 2-framing]]
[[!redirects 2-framings]]

