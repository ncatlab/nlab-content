
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _elliptic genus_  is a [[genus]] in [[elliptic cohomology]] ([Landweber-Ravenel-Stong 93](#LandweberRavenelStong93)). In analogy to how there is a "universal elliptic cohomology", namely [[tmf]], there is a universal elliptic genus -- the [[Witten genus]]. This arises as the [[large volume limit]] of the [[partition function]] of the [[superstring]] whose [[target space]] is the given [[manifold]].

## Definition
 {#Definition}

The original definition of elliptic genus is due to ([Ochanine 87](#Ochanine87)) (see the review ([Ochanine 09](#Ochanine09))) and says that an _[[genus]]_ of [[orientation|oriented]] manifolds is called an elliptic genus if it vanishes on manifolds which are [[projective spaces]] of the form $\mathbb{C}P(\xi)$ for $\xi$ an even-dimensional [[complex vector bundle]] over an [[orientation|oriented]] [[closed manifold]].

The terminomology _elliptic_ for this was motivated by the central theorem of ([Ochanine 87](#Ochanine87)) which says that every genus $\phi$ satisfying this condition has a [logarithm](genus#LogarithmAndCharacteristicSeries) $log_\phi$ of the form

$$
  log_\phi(u) = \int_{0^u} (1- 2 \delta t^2+  \epsilon t^4)^{-1/2}
$$

for some constants $\delta, \epsilon$. Hence for non-degenerate choices of parameters ($\delta^2 \neq \epsilon$ and $\epsilon \neq 0$) in the square root this is the expansion at 0 of an elliptic function. 

So the logarithm here is an [[elliptic integral]] and that was the original reason for the term "elliptic genus".

## Examples

### Degenerate case: Signature genus

The degenerate case with parameters $\delta = \epsilon = 1$ (as [above](#Definition)) is the [[signature genus]].

### Degenerate case: $\hat A$-genus

The degenerate case with parameters $\delta = - \frac{1}{8}$ and $\epsilon = 0$ (as [above](#Definition)) is the [[A-hat genus]].

### Universal case: Witten genus

Given an elliptic genus with non-degenerate parameters $\delta, \epsilon \in \mathbb{C}$ (as [above](#Definition), see also at _[[j-invariant]]_), the [[Jacobi quartic]] [[Riemann surface]] which is given by the [[equation]]

$$
  Y^2 = X^4 - 2 \delta X^2 + \epsilon
$$

is naturally parameterized by the [[upper half plane]]. Under this identification obe may think of $\epsilon$ and $\delta$ as functions of moduli of [[elliptic curves]] and concretely as [[modular forms]] for the [[subgroup]] $\Gamma_0(2)$ of that of M&#246;bius transformations.

Viewed this way the collection of all elliptic genera provides a single [[genus]] with [[coefficients]] in this ring $MF_\bullet(\Gamma_0(2))$ of [[modular forms]] 

$$
  w \colon \Omega^{SO}_\bullet \longrightarrow MF_\bullet(\Gamma_0(2))
$$

(such that postcomposition with evaluation on any elliptic curve parameterized by the given value of $\delta$ and $\epsilon$ produces the corrponding elliptic genus).

This "universal" elliptic genus is the _[[Witten genus]]_.

## Properties

### Integrality on Spin-manifolds

On [[manifolds]] with [[spin structure]] the elliptic genus
takes values in integral series $\mathbb{Z}[ [q] ]$.

([Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88), [Landweber 88, section 5](#Landweber88) [Kreck-Stolz 93](#KreckStolz93), [Hovey 91](#Hovey91))

### Relation to partition functions of superstring

The [[partition function]] of a [[type II superstring]] as a function depending on the [[modulus]] of the [[worldsheet]] [[elliptic curve]] yields an elliptic genus ([Witten 87](#Witten87)). (The analog for the [[heterotic string]] is hence called the _[[Witten genus]]_ with values in the "universal elliptic cohomology" theory, [[tmf]]).

For equivariant/gauged string [[sigma-models]] the elliptic genus should take values in [[equivariant elliptic cohomology]], see at _[gauged WZW mode -- Partition function in elliptic cohomology](gauged+WZW+model#PartitionFunctionInEllipticCohomology)_.

### Rigidity theorem

See _[[rigidity theorem for elliptic genera]]_.


## Related concepts

* [[elliptic cohomology]]

* [[spin orientation of Ochanine elliptic cohomology]]

* [[Witten genus]], [[string orientation of tmf]]

* [[equivariant elliptic genus]]

[[!include genera and partition functions - table]]


## References

[[!include elliptic cohomology -- references]]




[[!redirects elliptic genera]]

[[!redirects Ochanine genus]]
[[!redirects Ochanine elliptic genus]]
