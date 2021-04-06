
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

_Higher differential geometry_ is the incarnation of [[differential geometry]] in [[higher geometry]]. Hence it is concerned with [[n-groupoid]]-versions of [[smooth spaces]] for _higher_ $n$, where the traditional theory is contained in the case $n = 0$. For $n = 1$ these higher structures are _[[Lie groupoids]]_, _[[differentiable stacks]]_, their infinitesimal approximation by [[Lie algebroids]] and the generalization to _[[smooth stacks]]_. For higher $n$ this includes ([[deloopings]] of) [[Lie 2-groups]], [[Lie 3-groups]].

Fully generally, higher differential geometry hence replaces [[smooth manifolds]] (and possibly variants such as [[supermanifolds]], [[formal manifolds]], [[dg-manifolds]] etc.) by _[[∞-stacks]]_ ([[(∞,1)-sheaves]]) on the [[site]] of all such. Technically this means that higher differential geometry is the study of an _[[(∞,1)-topos]]_ into which standard [[differential geometry]] faithfully embeds.
This then allows to speak of [[smooth ∞-groups]], [[Lie ∞-algebroids]].

If the ambient [[(∞,1)-topos]] is not [[n-localic (∞,1)-topos|1-localic]] (for instance over a genuine site of [[dg-manifolds]]) then one also speaks of _[[derived differential geometry]]_.

See at _[[motivation for higher differential geometry]]_ for motivation.

The standard variants of [[differential geometry]] have their higher analogs, for instance [[symplectic geometry]] generalizes to [[higher symplectic geometry]] and [[prequantum geometry]] to [[higher prequantum geometry]].

## Formalizations

One axiomatization is [[cohesion]] and [[differential cohesion]].

## Examples

* [[Smooth∞Grpd]], [[SuperFormalSmooth∞Grpd]].

* [[Lie 2-groupoid]]

* [[double Lie algebroid]], [[Lie algebroid-groupoid]], [[double Lie groupoid]]


## Related concepts

* [[higher structure]]

* [[higher Lie theory]]

* [[higher prequantum geometry]]

* [[higher complex analytic geometry]]

* [[L-infinity algebras in physics]]

## References
 {#References}

Exposition is in 

* [[Urs Schreiber]], _[[schreiber:Higher Structures|Higher Structures in Mathematics and Physics]]_, talk at [Oberwolfach Workshop 1651a](https://www.mfo.de/occasion/1651a/www_view), 2016 Dec. 18-23

Details:

* _[[geometry of physics]]_, [[geometry of physics -- categories and toposes|categories and toposes]], ...

The most classical aspect of higher differential geometry is the theory of [[orbifolds]], [[Lie groupoids]] and [[Lie algebroids]] and their application in [[foliation theory]]. Original reference here include

* [[Charles Ehresmann]], _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_, Colloque de G&#233;ometrie Differentielle Globale (Bruxelles, 1958), 137--150, Centre Belge Rech. Math., Louvain, 1959; 

* [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf)),  _Orbifolds as Groupoids: an Introduction_ ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100))

Textbook accounts:

* [[Ieke Moerdijk]], [[Janez Mrcun]] _Introduction to Foliations and Lie Groupoids_, Cambridge Studies in Advanced Mathematics 91, Cambridge University Press, Cambridge, (2003) ([doi:10.1017/CBO9780511615450](https://doi.org/10.1017/CBO9780511615450))

* [[Kirill Mackenzie]], _General Theory of Lie Groupoids and Lie Algebroids,_ Cambridge University Press, 2005, xxxviii + 501 pages 
([website](http://kchmackenzie.staff.shef.ac.uk/gt.html))

* [[Kirill Mackenzie]], _Lie groupoids and Lie algebroids in differential geometry_, London Mathematical Society Lecture Note Series, 124. Cambridge University Press, Cambridge, 1987. xvi+327 pp ([MathSciNet](http://www.ams.org/mathscinet-getitem?mr=896907))

For properly appreciating the [[homotopy theory]] of Lie groupoids and for passage to more general higher differential geometry it is crucial to understand Lie groupoids as [[smooth stacks]] which are [[geometric stack|geometric]]:  _[[differentiable stacks]]_. Each of the following references provides introduction to this point of view:

* [[Jochen Heinloth]], _Some notes on differentiable stacks_ ([pdf](http://www.uni-due.de/~hm0002/stacks.pdf))

* [[Kai Behrend]], [[Ping Xu]], _Differentiable Stacks and Gerbes_ ([arXiv:0605.5694](http://front.math.ucdavis.edu/0605.5694)).

* Metzler, _Topological and smooth stacks_ ([arXiv:math/0306176](http://arxiv.org/abs/math/0306176))

As a warmup for these considerations it may be useful to first look at [[smooth spaces]] given by just [[sheaves]] on the site of [[smooth manifolds]], see at 

* [[Urs Schreiber]], _[[geometry of physics]] -- [[geometry of physics -- smooth spaces|smooth spaces]]_

Passing from here to more general [[smooth groupoids]], to [[smooth 2-groupoids]] and then eventually to [[smooth ∞-groupoids]] involves [[(∞,1)-topos theory]] proper, with some tools as discussed at _[[model structure on simplicial presheaves]]_ over the [[site]] of [[smooth manifolds]], or equivalently just over its [[dense subsite]] of [[Cartesian spaces]].

For motivation for this step see also

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, lectures at _[ESI program on quantum fields and K-theory](http://maths-old.anu.edu.au/esi/2012/)_, 2012

Introductory exposition includes the introductory sections of

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_, Advances in Theoretical and Mathematical Physics, Volume 16 Issue 1 (2012), pages 149-250 ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _A higher stacky perspective on Chern-Simons theory_, in Damien Calaque et al. (eds.) _Mathematical Aspects of Quantum Field Theories_ Mathematical Physics Studies, Springer 2014 ([arXiv:1301.2580](http://arxiv.org/abs/1301.2580))

and sections 1.2.4 ([[geometry of physics -- smooth homotopy types]]) as well as section 1.2.5 ([[geometry of physics -- principal bundles]]) in the Introduction section of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

This goes on to discuss [[differential cohomology]] and the [[differential cohomology diagram]] formulated in [[stable homotopy type|stable]] objects in [[smooth ∞-groupoids]] (hence in [[sheaves of spectra]] on the [[site]] of [[smooth manifolds]]/[[Cartesian spaces]]) in higher differential geometry, see 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))