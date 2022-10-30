
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Rational [[equivariant stable homotopy theory]]_ is the study of [[equivariant spectra]] just on the level of their [[rationalization]], hence concerning only their non-[[torsion subgroup|torsion]] [[homotopy groups]]. This is the [[equivariant cohomology|equivariant]] and [[stable homotopy theory|stable]] version of [[rational homotopy theory]].

A key general statement of the theory is that rationally the [[homotopy theory]] of $G$-equivariant spectra is equivalently given by [[homological algebra]] of [[Mackey functors]] (even for non-[[finite group|finite]] $G$). At the level of [[equivalence of categories|equivalences]] of [[homotopy categories]] this was established by [[John Greenlees]], at the level of [[zig-zags]] of [[Quillen equivalences]] of [[model categories]] this was established Greenlees and by his students, [[David Barnes]] and [[Magdalena Kedziorek]].

## Properties

### Greenlees-May splitting into equivariant Eilenberg-MacLane spectra
 {#SplittingIntoMackeyFunctors}

Let $G$ be a [[finite group]]. For $X$ a [[G-spectrum]], write $\pi_\bullet(X) \in \mathcal{M}[G]$ for its [[Mackey functor]], the one which sends $G/H$ to the $H$-[[equivariant homotopy groups]] of $X$. 

Every rational $G$-equivariant spectrum $E$ is the direct sum of the [[Eilenberg-MacLane spectra]] (Mackey functors) on its [[equivariant homotopy groups]]:

$$
  E \simeq \prod_n \Sigma^n H\pi_n(E)
  \,.
$$

([Greenlees-May 95, theorem A.1](#GreenleesMay95), [Greenlees, theorem 5.1](#Greenlees))

For $X,Y$ two $G$-spectra, there is a canonical morphism

$$
  [X,Y]_G \longrightarrow \underset{n}{\prod} Hom_{\mathcal{M}[G]}(\pi_n(X),\pi_n(Y))
  \,.
$$

When $Y$ is rational, then this is an [[isomorphism]] ([Greenlees-May 95, theorem A.4](#GreenleesMay95)).



### Rational tom Dieck splitting

for the moment see at _[[tom Dieck splitting]]_

## Examples

Just as for the plain [[sphere spectrum]], the [[equivariant homotopy groups]] of the [[equivariant sphere spectrum]] in ordinary [[integer]] degrees $n$ are all [[torsion subgroup|torsion]], except at $n = 0$:

$$
  \pi_n^H(\mathbb{S})\otimes \mathbb{Q} =
  \left\{
    \array{
       \cdots & for \; n = 0
       \\
       0 & otherwise
    }
  \right.
$$

([Greenlees-May 95, prop. A.3](#GreenleesMay95))

But in some [[RO(G)-degrees]] there may appear further non-torsion groups, see at _[[equivariant sphere spectrum]]_ the section  [Examples](equivariant+sphere+spectrum#Examples).

## Related concepts

* [[equivariant rational homotopy theory]]

## References

General:


* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], appendix A of _Generalized Tate cohomology_, Mem. Amer. Math. Soc. 113 (1995) no 543 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/GM-Tate-543.pdf))

* {#Greenlees} [[John Greenlees]], _Triangulated categories of rational equivariant cohomology theories_ ([pdf](http://www.greenlees.staff.shef.ac.uk/preprints/thicksurvey.pdf))


* [[David Barnes]], _Rational Equivariant Spectra_ ([arXiv:0802.0954](http://arxiv.org/abs/0802.0954))

* [[David Barnes]], _Classifying Rational $G$-Spectra for Finite $G$_ ([arXiv:0812.0317](http://arxiv.org/abs/0812.0317))

For $G = O(2)$ or $SO(2)$ and so also for $G = $ [[dihedral group]] and [[cyclic group]]:

* {#Greenlees96} [[John Greenlees]], _Rational $O(2)$-equivariant cohomology theories_. In _Stable and unstable homotopy_ (Toronto, ON, 1996), volume 19 of Fields
Inst. Commun., pages 103&#8211;110. Amer. Math. Soc., Providence, RI, 1998. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.41.6588))

* {#Greenlees99} [[John Greenlees]], _Rational $S^1$-equivariant stable homotopy theory_, Memoirs of the AMS, 1999

* [[Brooke Shipley]], _An algebraic model for rational $S^1$-equivariant stable homotopy theory_ ([pdf](http://homepages.math.uic.edu/~bshipley/qt15.pdf))

* [[David Barnes]], _Classifying Dihedral $O(2)$-Equivariant Spectra_ ([arXiv:0804.3357](http://arxiv.org/abs/0804.3357))

* [[David Barnes]], _Rational $Z_p$-Equivariant Spectra_, Algebr. Geom. Topol. 11 (2011) 2107-2135 ([arXiv:1011.5785](http://arxiv.org/abs/1011.5785))

* [[David Barnes]], _Rational $O(2)$-Equivariant Spectra_ ([arXiv:1201.6610](http://arxiv.org/abs/1201.6610))

* [[David Barnes]], _A monoidal algebraic model for rational $SO(2)$-spectra_ ([arXiv:1412.1700](http://arxiv.org/abs/1412.1700))

* [[David Barnes]], [[John Greenlees]], [[Magdalena Kedziorek]], [[Brooke Shipley]], _Rational $SO(2)$-Equivariant Spectra_ ([arXiv:1511.03291](http://arxiv.org/abs/1511.03291))

For $G = (S^1)^{\times_n}$ a [[torus]]:

* [[John Greenlees]], [[Brooke Shipley]], _An algebraic model for rational torus-equivariant spectra_ ([arXiv:1101.2511](http://arxiv.org/abs/1101.2511))

For $G = SO(3)$ and hence also for the finite groups of [[ADE classification|ADE type]]:

* [[John Greenlees]], _Rational SO(3)-Equivariant Cohomology Theories_, in _Homotopy methods in algebraic topology_ (Boulder, CO, 1999), Contemp. Math. 271, Amer. Math. Soc. (2001) 99 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.5444))

* [[Magdalena Kedziorek]], _Algebraic models for rational G-spectra_, 2014 ([web](http://etheses.whiterose.ac.uk/7699/))