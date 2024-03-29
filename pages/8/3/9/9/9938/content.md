
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The [[Bousfield localization of spectra|localization]] of [[complex cobordism cohomology theory]] $MU$ at a [[prime]] $p$, hence the [[p-localization]] $MU_{(p)}$, decomposes as a [[direct sum]]. The direct summands are the _Brown-Peterson spectra_.

## Definition

+-- {: .num_theorem}
###### Theorem

For each [[prime]] $p$ there is an unique commutative ring [[spectrum]] $B P$ which is a [[retract]] of $M U_{(p)}$ such that the map $MU_{(p)} \to B P$ is multiplicative and such that

1. (...)

1. (...)

1. (...)

=--

Due to ([Brown-Peterson 66](#BrownPeterson66)), recalled as ([Ravenel, theorem, 4.1.12](#Ravenel)).

## Properties

### Universal characterization

(...)

The [[formal group law]] of Brown-Peterson cohomology theory is [[universal property|universal]] for $p$-local [[complex oriented cohomology theories]] in that $\mathbb{G}_{B P}$ is universal among $p$-local, [[p-typical formal group laws]].

(...)

### Relation to $p$-typical formal groups

$B P$ is related to [[p-typical formal groups]] as [[MU]] is to [[formal groups]].

### Hopf algebroid structure on dual BP-Steenrod algebra

The structure of [[Hopf algebroid over a commutative base]]
on the dual $BP$-[[Steenrod algebra]]
$BP_\bullet(BP)$ is described by the [[Adams-Quillen theorem]].

### Relation to Adams-Novikov spectral sequence

The $p$-component of the $E^2$-term of the [[Adams-Novikov spectral sequence]] for the [[sphere spectrum]], hence the one converging to the 
[[stable homotopy groups of spheres]] $\pi_\ast(\mathbb{S})$ is

$$
  Ext_{BP_\ast(BP)}(BP_\ast, BP_\ast)
  \,.
$$

recalled e.g. as [Ravenel, theorem 1.4.2](#Ravenel)

### As a CW spectrum

The spectrum $B P$ can be constructed as a [[CW spectrum]] (cf. Priddy 1980) starting from the $p$-local sphere spectrum $S^0 = X_0$ by minimally attaching cells to $X_n$ to kill $\pi_{2n+1}(X_n)$.

## Related concepts

* [[Morava E-theory]]

* [[BPR-theory]]

## References

The original article is

* {#BrownPeterson66} [[Edgar Brown]], F. P. Peterson, _A spectrum whose $\mathbb{Z}/p$ cohomology is the algebra of reduced $p$-th powers_, Topology 5 (1966) 149.
 
* [[Frank Adams]], part II.16 of _[[Stable homotopy and generalised homology]]_,1974

An alternate construction was noted by Priddy

* [[Stewart Priddy]], _A cellular construction of BP and other irreducible spectra_, [Math. Z.](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002423782) 173 (1980), pp 29-34.

A textbook accounts:

* {#Ravenel} [[Doug Ravenel]], section 4 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel4.pdf)) in: _[[Complex cobordism and stable homotopy groups of spheres]]_ ([web](http://www.math.rochester.edu/people/faculty/doug/mu.html))
 
* {#Rudyak98} [[Yuli Rudyak]], Section IX.6 in: _On Thom Spectra, Orientability, and Cobordism_, Springer 1998 ([doi:10.1007/978-3-540-77751-9](https://doi.org/10.1007/978-3-540-77751-9))


The truncated version is discussed in

* [[Tyler Lawson]], [[Niko Naumann]], _Truncated Brown-Peterson spectra_ (2012) ([pdf](http://www.math.umn.edu/~tlawson/jmm-boston-handout.pdf))


On the [[Hopf invariant]] and [[e-invariant]] in [[BP-theory]]:

* Yasumasa Hirashima, _On the $BP_\ast$-Hopf invariant_, Osaka J. Math., Volume 12, Number 1 (1975), 187-196 ([euclid:ojm/1200757733](https://projecteuclid.org/euclid.ojm/1200757733))

* [[Martin Bendersky]], _The BP Hopf Invariant_, American Journal of Mathematics, Vol. 108, No. 5 (Oct., 1986) ([jstor:2374595](https://www.jstor.org/stable/2374595))


[[!redirects Brown-Peterson spectra]]

[[!redirects Brown-Peterson cohomology]]

[[!redirects Brown-Peterson cohomology theory]]
[[!redirects Brown-Peterson cohomology theories]]

[[!redirects Brown-Peterson theory]]
[[!redirects Brown-Peterson theories]]

[[!redirects BP]]

[[!redirects BP-spectrum]]
[[!redirects BP spectrum]]

[[!redirects BP-theory]]
[[!redirects BP theory]]





