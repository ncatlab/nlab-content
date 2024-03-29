
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Kan-fibrant simplicial manifold_ is a [[simplicial manifold]] (for instance [[simplicial object|simplicial]] [[topological manifold]] or simplicial [[smooth manifold]]) which satisfies a suitable analog of the [[Kan complex]]-condition on a [[simplicial set]].
(Typically, to get an interesting theory, Kan-fibrancy on simplicial manifolds is imposed in a suitable local sense, meaning that [[horns]] have continuous/smooth fillers in a  [[open neighbourhoods]] of all points, but possibly not globally.)

Motivated by the standard way (see at _[[homotopy hypothesis]]_) in which bare [[Kan complexes]] (hence Kan-fibrant [[simplicial sets]]) present [[geometrically discrete ∞-groupoids]] and given that the [[nerve]] of a [[Lie groupoid]] is an example of a locally Kan-fibrant simplicial manifold (a [[1-truncated]] one), such Kan-fibrant simplicial manifolds are often referred to _[[Lie infinity-groupoids]]_ (or _[[Lie n-groupoids]]_ for finite [[n-truncated object in an (infinity,1)-category|truncation]]) ([Zhu 06](#Zhu06)).

With such a suitably local definition, there should be the structure of a [[homotopical category]] on Kan-fibrant simplicial manifolds which embeds homotopically full and faithful into a local [[model structure on simplicial presheaves]] over a suitable [[site]] of manifolds, hence such that this inclusion presents and [[full sub-(∞,1)-category]] of the [[(∞,1)-sheaf (∞,1)-topos]] over manifolds ("[[smooth ∞-groupoids]]"). 

Some care is needed in correctly interpreting the "Lie" condition in view of the [[homotopy theory]]. For instance _every_ [[∞-stack]] on the category of smooth manifolds ("[[smooth ∞-groupoid]]") is presented by a [[simplicial manifold]], just not in general by a suitably Kan-fibrant simplicial manifold ([NSS 12, section 2.2](#NSS12)).

A homotopy-correct characterization of the sub-$\infty$-category presented by the Kan-fibrant simplicial objects as that of _[[geometric ∞-stacks]]_ modeled on manifolds is in ([Pridham 09](#Pridham09)) (see around p. 17 for the differential geometric version).

Kan-fibrant simplicial manifolds have received particular attention as the result of [[Lie integration]] of [[L-∞ algebroids]]. See at _[[Lie integration]]_ for more on that.

## Examples

1. Any ordinary [[manifold]], interpreted as a constant [[simplicial object]].

2. The [[nerve]] of a [[Lie groupoid]]. In particular, the [[delooping]] of any [[Lie group]], which represents [[principal bundles]] with this [[Lie group]] as a structure group.

3. The [[Dold–Kan functor]] $\Gamma$ applied to any nonnegatively graded [[chain complex]] of abelian Lie groups.

4. In particular, applying $\Gamma$ to the [[chain complex]] $\mathrm{U}(1)[n]$, we get the Kan simplicial manifold representing bundle $(n-1)$-gerbes.

5. The nonabelian analogue of $\Gamma$ applied to any [[crossed module]] whose two constituent groups are [[Lie groups]] and the involved homomorphisms and actions are smooth.

6. The nonabelian analogue of $\Gamma$ applied to any [[hypercrossed complex]] whose constituent groupoids are [[Lie groupoids]] and the involved homomorphisms and actions are smooth.

7.  As a special case of the previous example, any [[simplicial Lie group]] is a Kan simplicial manifold.

## Related concepts

* [[simplicial manifold]]

* [[higher differential geometry]]

* [[internal ∞-groupoid]]

* [[smooth ∞-groupoid]]

## References

Early appearances of the concept include

* [[André Henriques]], _Integrating $L_\infty$-algebras_, Compositio Mathematica, 144, (2008), no. 4, 1017&#8211;1045 ([arXiv:math/0603563](http://arxiv.org/abs/math/0603563))

* {#Zhu06} [[Chenchang Zhu]], _$n$-groupoids and stacky Lie groupoids_, Int Math Res Notices (2009) 2009 (21): 4087-4141. ([arXiv:math/0609420](http://arxiv.org/abs/math/0609420))

* {#Zhu08} [[Chenchang Zhu]], _Kan replacement of simplicial manifolds_, Lett Math Phys (2009) 90:383&#8211;405, [arXiv:0812.4150](http://arxiv.org/abs/0812.4150)


Characterization of the homotopy theory of Kan-fibrant simplicial manifolds as [[geometric ∞-stacks]] modeled on smooth manifolds is in (see aroung p. 17 for the differential geometric version)

* {#Pridham09} [[Jonathan Pridham]], _Presenting higher stacks as simplicial schemes_, Advances in Mathematics, Volume 238, Pages 184-245 ([arXiv:0905.4044](http://arxiv.org/abs/0905.4044))

Discussion of [[principal ∞-bundles]] in [[Smooth∞Grpd]] $= Sh_\infty(SmoothMfd)$ which are represented by locally Kan-fibrant simplicial manifolds is in 

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], section 4.2 of _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- Presentations]]_, Journal of Homotopy and Related Structures, March 2014 ([arXiv:1207.0249](http://arxiv.org/abs/1207.0249))

* [[Jesse Wolfson]], _Descent for $n$-Bundles_ ([arXiv:1308.1113](http://arxiv.org/abs/1308.1113))

[[!redirects Kan simplicial manifolds]]
[[!redirects Kan-fibrant simplicial manifold]]
[[!redirects Kan-fibrant simplicial manifolds]]