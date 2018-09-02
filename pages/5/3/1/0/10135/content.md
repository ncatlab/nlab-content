
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

On general grounds, since [[orbifolds]] $\mathcal{G}$ are special cases of [[stacks]], there is an evident definition of [[cohomology]] of orbifolds, given by forming ([[stable homotopy group|stable]]) [[homotopy groups]] of [[derived hom-spaces]] 

$$
  H^\bullet(\mathcal{G}, E)
  \;\coloneqq\;
  \pi_\bullet \mathbf{H}( \mathcal{G}, E )
$$

into any desired [[coefficient]] [[∞-stack]] (or [[sheaf of spectra]]) $E$.

More specifically, often one is interested in viewing orbifold cohomology as a variant of [[Bredon cohomology|Bredon]] [[equivariant cohomology]], based on the idea that the [[cohomology]] of a global [[homotopy quotient]] orbifold 


\[
  \label{GlobalQuotientOrbifold}
  \mathcal{G} \;\simeq\; X \sslash G
\] 

for a given $G$-[[action]] on some [[manifold]] $X$, should coincide with the $G$-[[equivariant cohomology]] of $X$. However, such an identification (eq:GlobalQuotientOrbifold) is not unique: For $G \subset K$ any closed subgroup, we have 

$$
  X \sslash G
  \;\simeq\;
  \big( X \times_G K\big) \sslash K
  \,.
$$

This means that if one is to regard orbifold cohomology as a variant of [[equivariant cohomology]], then one needs to work "globally" in terms of _[[global equivariant homotopy theory]]_, where one considers equivariance with respect to "all [[compact Lie groups]] at once", in a suitable sense.

Concretely, in [[global equivariant homotopy theory]] the plain [[orbit category]] $Orb_G$ of $G$-[[equivariant cohomology|equivariant]] [[Bredon cohomology]] is replaced by the [[global orbit category]] $Orb_{glb}$ whose [[objects]] are the [[delooping]] [[stacks]] $\mathbf{B}G \coloneqq \ast\sslash G$, and then any [[orbifold]] $\mathcal{G}$ becomes an [[(∞,1)-presheaf]] $y \mathcal{G}$ over $Orb_{glb}$ by the evident "external [[Yoneda embedding]]"

$$
  y \mathcal{G}
  \;\coloneqq\;
  \mathbf{H}( \mathbf{B}G, \mathcal{G} )
  \,.
$$

More generally, this makes sense for $\mathcal{G}$ any [[orbispace]]. In fact, as a construction of an [[(∞,1)-presheaf]] on $Orb_{glb}$ it makes sense for $\mathcal{G}$ any [[∞-stack]], but supposedly precisely if $\mathcal{G}$ is an [[orbispace]] among all [[∞-stacks]] does the [[cohomology]] of $y \mathcal{G}$ in the sense of [[global equivariant homotopy theory]] coincide the cohomology of $\mathcal{G}$ in the intended sense of [[∞-stacks]], in particular reproducing the intended sense of orbifold cohomology. 

At least for [[topological stack|topological]] [[orbifolds]] this is indicated in ([Schwede 17, Introduction](#Schwede17), [Schwede 18, p. ix-x](#Schwede18), see also [Pronk-Scull 07](#PronkScull07))



## Related concepts

* [[orbifold]]

* [[Gromov-Witten theory]]

## References

According to [Abramovich 05, p. 42](#Abramovich05):

> On December 7, 1995 [[Maxim Kontsevich]] delivered a history-making lecture at Orsay, titled _String Cohomology_. This is what is now know, after [Chen-Ruan 00](#ChenRuan00), as _orbifold cohomology_, Kontsevich's lecture notes described the orbifold and  [[quantum cohomology]] of a global quotient [[orbifold]]. Twisted sectors, the age grading, and a version of orbifold stable maps for global quotients are all there.
 
Discussion of orbifold cohomology in the context of [[Bredon cohomology|Bredon]]/[[global equivariant homotopy theory|global]] [[equivariant cohomology]] includes

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], _Translation Groupoids and Orbifold Bredon Cohomology_ ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249))

* {#Schwede17} [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_ ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019))

* {#Schwede18} [[Stefan Schwede]], _[[Global homotopy theory]]_ ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

See also

* {#ChenRuan00} Weimin Chen, [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](http://arxiv.org/abs/math/0004129))
 
* {#Abramovich05} [[Dan Abramovich]], _Lectures on Gromov-Witten invariants of orbifolds_ ([arXiv:math/0512372](http://arxiv.org/abs/math/0512372))

[[!redirects orbifold cohomologies]]

[[!redirects orbifold cohomology group]]
[[!redirects orbifold cohomology groups]]

[[!redirects orbispace cohomology]]
[[!redirects orbispace cohomologies]]

[[!redirects orbispace cohomology group]]
[[!redirects orbispace cohomology groups]]

