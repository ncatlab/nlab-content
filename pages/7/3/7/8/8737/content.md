
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
+-- {: .toc .clickDown tabindex="0"}
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _nonabelian Stokes theorem_ (e.g. [Schreiber-Waldorf 11, theorem 3.4](#SchreiberWaldorf11)) is a generalization of the [[Stokes theorem]] to [[Lie algebra valued differential 1-forms]] and with [[integration of differential forms]] refined to [[parallel transport]].

## Statement

If $\hat A \in \Omega^1(D^2, \mathfrak{g})$ is a [[Lie algebra valued 1-form]] on the 2-[[disk]] then the [[parallel transport]] $\mathcal{P} \exp(\int_{S^1} A)$ of its restriction $A \in \Omega^1(S^1, \mathfrak{g})$ to the [[boundary]] [[circle]], hence its [[holonomy]] (for a fixed choice of base point) is equal to a certain kind of adjusted 2-dimensional integral of its [[curvature]] 2-form $F_A$ over $D^2$.

In particular if $F_{\hat A} = 0$ then the [[holonomy]] of $A$ is trivial.

## Properties

### Relation to higher parallel transport

In terms of the notion of [[connection on a 2-bundle]] the nonabelian Stokes theorem says that if $A \in \Omega^1(X, \mathfrak{g})$ is a [[Lie algebra valued 1-form]], then $(F_A, A)$ is a [[Lie 2-algebra valued 2-form]] with values in the [[inner derivation Lie 2-algebra]] $inn(\mathfrak{g})$ of $\mathfrak{g}$ whose [[curvature]] 3-form $H = \mathbf{d}_A F_A$ vanishes (which is the [[Bianchi identity]] for $F_A$) and its [[higher parallel transport]] exists. The [[2-functor|2-functorial]] source-target matching condition in this higher parallel transport is the statement of the nonabelian Stokes theorem.

### Relation to Lie integration

For $F_A = 0$ the nonabelian Stokes theorem may be regarded as proving that the [[Lie integration]] of $\mathfrak{g}$ by "the path method" (see at [[Lie integration]]) is indeed the [[simply connected topological space|simply connected]] [[Lie group]] corresponding to $\mathfrak{g}$ by [[Lie theory]].
 

## References

* Robert L. Karp, Freydoon Mansouri, Jung S. Rno, *Product Integral Formalism and Non-Abelian Stokes Theorem*, J. Math. Phys. **40** (1999) 6033-6043 &lbrack;[arXiv:hep-th/9910173](https://arxiv.org/abs/hep-th/9910173), [doi:10.1063/1.533068](https://doi.org/10.1063/1.533068)&rbrack;

* R. L. Karp, F. Mansouri, J. S. Rno, *Product Integral Representations of Wilson Lines and Wilson Loops, and Non-Abelian Stokes Theorem*, Turk. J. Phys. **24** (2000) 365-384 &lbrack;[arXiv:hep-th/9903221](https://arxiv.org/abs/hep-th/9903221), [journal page](https://search.trdizin.gov.tr/tr/yayin/detay/67090)&rbrack;

* Boguslaw Broda, *Non-Abelian Stokes theorem in action*, in *Modern Nonlinear Optics* Part 2, Wiley (2001) 429-468 &lbrack;[arXiv:math-ph/0012035](https://arxiv.org/abs/math-ph/0012035), [ISBN:978-0-471-46612-3](https://www.wiley.com/en-ae/Modern+Nonlinear+Optics,+Volume+119,+Part+2,+2nd+Edition-p-9780471466123)&rbrack;

In the context of [[higher parallel transport]] in [[principal 2-bundles with connection]]:

* {#SchreiberWaldorf11} [[Urs Schreiber]], [[Konrad Waldorf]], Theorem 3.4 in: *Smooth Functors vs. Differential Forms*, Homology, Homotopy Appl. **13** 1 (2011) 143-203 &lbrack;[arXiv:0802.0663](http://arxiv.org/abs/0802.0663), [euclid:hha/1311953350](https://projecteuclid.org/journals/homology-homotopy-and-applications/volume-13/issue-1/Smooth-functors-vs-differential-forms/hha/1311953350.full)&rbrack;

See also:

* Seramika Ariwahjoedi, Freddy Permana Zen, *Alternative Derivation of the Non-Abelian Stokes Theorem in Two Dimensions*, Symmetry **2023** 15 11 (2000) &lbrack;[doi:10.3390/sym15112000]( https://doi.org/10.3390/sym15112000)&rbrack;



