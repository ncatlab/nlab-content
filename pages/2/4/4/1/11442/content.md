
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

\tableofcontents

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

> (see also references at *[[Lie integration]]*)

Early appearances of the concept include

* [[André Henriques]]; Def. 1.2 in: _Integrating $L_\infty$-algebras_, Compositio Mathematica **144** 4 (2008) 1017--1045 &lbrack;[arXiv:math/0603563](http://arxiv.org/abs/math/0603563), [doi:10.1112/S0010437X07003405](https://doi.org/10.1112/S0010437X07003405)&rbrack;

* {#Zhu06} [[Chenchang Zhu]]; Def. 1.2 in: *Lie $n$-groupoids and stacky Lie groupoids* &lbrack;[arXiv:math/0609420](https://arxiv.org/abs/math/0609420)&rbrack;

* {#Zhu08} [[Chenchang Zhu]]; Def. 1.3 in: _$n$-Groupoids and Stacky Groupoids_, Int Math Res Notices **2009** 21 (2009) 4087--4141 &lbrack;[doi:10.1093/imrn/rnp080](https://doi.org/10.1093/imrn/rnp080), [arXiv:0801.2057 math.DG](https://arxiv.org/abs/0801.2057)&rbrack;

* {#Zhu09} [[Chenchang Zhu]]: _Kan replacement of simplicial manifolds_, Lett Math Phys **90** 1 (2009) 383--405 &lbrack;[arXiv:0812.4150 math.DG](http://arxiv.org/abs/0812.4150), [doi:10.1007/s11005-009-0353-0](https://doi.org/10.1007/s11005-009-0353-0)&rbrack;


Characterization of the homotopy theory of Kan-fibrant simplicial manifolds as [[geometric ∞-stacks]] modeled on smooth manifolds is in (see around p. 17 for the differential geometric version)

* {#Pridham09} [[Jonathan Pridham]]: _Presenting higher stacks as simplicial schemes_, Advances in Mathematics **238** (2013) 184--245 &lbrack;[arXiv:0905.4044](http://arxiv.org/abs/0905.4044), [doi:10.1016/j.aim.2013.01.009](https://doi.org/10.1016/j.aim.2013.01.009)&rbrack;

Discussion of [[principal ∞-bundles]] in [[Smooth∞Grpd]] $= Sh_\infty(SmoothMfd)$ which are represented by locally Kan-fibrant simplicial manifolds is in 

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], section 4.2 of: _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- Presentations]]_, Journal of Homotopy and Related Structures **10** 3 (2015) 565--622 &lbrack;[doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4), [arXiv:1207.0249 math.AT](http://arxiv.org/abs/1207.0249)&rbrack;

* [[Jesse Wolfson]]: _Descent for $n$-Bundles_, Advances in Mathematics **288** (2016) 527--575 &lbrack;[arXiv:1308.1113](http://arxiv.org/abs/1308.1113), [doi:10.1016/j.aim.2015.10.024](https://doi.org/10.1016/j.aim.2015.10.024)&rbrack;



* Alejandro Cabrera, Matias del Hoyo: *Geometric differentiation of simplicial manifolds* &lbrack;[arXiv:2602.09885 math.DG](https://arxiv.org/abs/2602.09885)&rbrack;


[[!redirects Kan simplicial manifolds]]
[[!redirects Kan-fibrant simplicial manifold]]
[[!redirects Kan-fibrant simplicial manifolds]]