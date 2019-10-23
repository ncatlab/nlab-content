
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In many categorical approaches to [[measure theory]] and [[probability]], one considers a [[category]] of [[spaces]], such as [[measurable spaces]] or [[topological spaces]], and equips this category with a [[monad]] whose [[functor]] part assigns to each space $X$ a space $P X$ of [[measures]], [[probability measures]], or [[valuation (measure theory)|valuations]] on $X$, or a variation thereof.

For probability theory, this can be interpreted as adding to the [[points]] of a space $X$ new "random points", modelled as probability measures or valuations.
The old points, which we can think of as deterministic, are embedded in $P X$ via the unit of the monad $X\to P X$. Just as well, the [[Kleisli morphisms]] of $P$ can be seen as [[stochastic maps]].
(Monads can be seen as ways of extending our spaces and functions to account for new phenomena, see for example [[extension system]] and [[monad in computer science]].)
Note that these probability measures are technically different from [[random elements]]: they rather correspond to the [[law of a random variable|laws]] of the random elements.

[[algebra over a monad|Algebras]] of probability monads can be interpreted [[convex spaces]] or [[convex cone|cones]] of a certain kind. For probability theory, in particular, the algebras of a probability monad can be seen as spaces equipped with a notion of [[expectation value]] of a [[random variable]]. 
The details vary depending on the monad and on the category under consideration.

Many choices of categories and of monads are possible, depending on which aspects of measure theory or probability one wants to study. 
See [the table below](#detailed_list) for more details.

## Functor, unit and multiplication

(...work in progress...)

## Algebras

(...work in progress...)

## Kleisli morphisms

(...work in progress...)

## Monoidal structure

(...work in progress...)

## Duality

(...work in progress...)

## Detailed list 

<table>
 <tr>
  <th markdown="1">Monad ($P$)</th>
  <th markdown="1">Category</th>
  <th markdown="1">Elements/points of $P X$</th>
  <th markdown="1">Extra structure of $P X$</th>
  <th markdown="1">$P$-Algebras</th>
  <th markdown="1">References</th>
 </tr>
 <tr>
  <th markdown="1">[[distribution monad]] (a.k.a. finitary Giry monad, convex combination monad)</th>
  <td markdown="1">[[Set]]</td>
  <td markdown="1">[[convex combinations]] or finitely-[[support#in_measure_theory|supported]] [[probability measures]]</td>
  <td markdown="1">(just a set)</td>
  <td markdown="1">[[convex spaces]]</td>
  <td markdown="1">[Fritz '09](#fritzconvex), [Jacobs '18](#jacobs)</td>
 </tr>
 <tr>
  <th markdown="1">[[Giry monad]]</th>
  <td markdown="1">[[Meas]]</td>
  <td markdown="1">[[probability measures]]</td>
  <td markdown="1">initial [[σ-algebra]] of evaluation maps</td>
  <td markdown="1">...</td>
  <td markdown="1">[Lawvere '62](#lawvere62), [Giry '80](#giry80)</td>
 </tr>
 <tr>
  <th markdown="1">[[Giry monad]]</th>
  <td markdown="1">[[Pol]]</td>
  <td markdown="1">[[Borel measure|Borel probability measures]]</td>
  <td markdown="1">[[initial topology]] of integration maps</td>
  <td markdown="1">...</td>
  <td markdown="1">[Giry '80](#giry80)</td>
 </tr>
 <tr>
  <th markdown="1">[[Radon monad]]</th>
  <td markdown="1">[[compactum#category_of_compacta|Comp]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] (or [[continuous valuations]])</td>
  <td markdown="1">[[weak topology]] w.r.t. continuous functions</td>
  <td markdown="1">[[compact]] [[convex subsets]] of [[locally convex topological vector spaces]]</td>
  <td markdown="1">[Swirszcz '74](#swirszcz), [Keimel '08](#radonkeimel)</td>
 </tr>
 <tr>
  <th markdown="1">[[Radon monad#the_ordered_case|ordered Radon monad]]</th>
  <td markdown="1">[[compact ordered spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] (or [[continuous valuations]])</td>
  <td markdown="1">[[weak topology]] w.r.t. continuous functions, [[stochastic order]]</td>
  <td markdown="1">[[compact]] [[convex subsets]] of [[ordered vector space|ordered]] [[locally convex topological vector spaces]]</td>
  <td markdown="1">[Swirszcz '74](#swirszcz), [Keimel '08](#radonkeimel)</td>
 </tr>
 <tr>
  <th markdown="1">[[extended probabilistic powerdomain#the_measure_monad_on_top|measure monad on Top]]</th>
  <td markdown="1">[[Top]]</td>
  <td markdown="1">[[τ-additive measures]]</td>
  <td markdown="1">[[extended probabilistic powerdomain#the_measure_monad_on_top|A-topology]], [[stochastic order]]</td>
  <td markdown="1">Full characterization unknown. [[extended probabilistic powerdomain#algebras|See also here]]. </td>
  <td markdown="1">[F-P-R '19](#support)</td>
 </tr>
 <tr>
  <th markdown="1">[[probabilistic powerdomain]]</th>
  <td markdown="1">[[dcpo]], [[continuous domains]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">[[stochastic order]]</td>
  <td markdown="1">[[abstract probabilistic domains]] (continuous case)</td>
  <td markdown="1">[J-P '89](#jonesplotkin)</td>
 </tr>
 <tr>
  <th markdown="1">[[extended probabilistic powerdomain]]{#extprobpow}</th>
  <td markdown="1">[[Top]], [[stably compact spaces]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">[[extended probabilistic powerdomain#spaces_of_valuations|initial topology of evaluation maps]], [[stochastic order]]</td>
  <td markdown="1">Full characterization unknown. [[extended probabilistic powerdomain#algebras|Dedicated section here]]</td>
  <td markdown="1">[Heckmann '96](#heckmann96), [A-J-K '04](#jung), [GL-J '19](#algebras), [F-P-R '19](#support)</td>
 </tr>
 <tr>
  <th markdown="1">[[valuation monad on locales]]</th>
  <td markdown="1">[[Loc]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">[[initial topology]] of evaluation maps</td>
  <td markdown="1">...</td>
  <td markdown="1">[Vickers '11](#vmonad)</td>
 </tr>
 <tr>
  <th markdown="1">[[Kantorovich monad]]</th>
  <td markdown="1">[[Cauchy-complete|complete]] [[metric spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] of finite first moment</td>
  <td markdown="1">[[Kantorovich-Wasserstein metric]]</td>
  <td markdown="1">closed [[convex subsets]] of [[Banach spaces]]</td>
  <td markdown="1">[van Breugel '05](#vanbreugel), [F-P '19](#kantorovich19)</td>
 </tr>
 <tr>
  <th markdown="1">(ordered) [[Kantorovich monad]]</th>
  <td markdown="1">[[Cauchy-complete|complete]] [[L-ordered]] [[metric spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] of finite first moment</td>
  <td markdown="1">[[Kantorovich-Wasserstein metric]], [[stochastic order]]</td>
  <td markdown="1">closed [[convex subsets]] of [[ordered Banach spaces]]</td>
  <td markdown="1">[F-P](#orderedkantorovich)</td>
 </tr>
</table>

(...to be expanded...)


## See also

* [[monad]], [[algebra over a monad]]
* [[monad (in computer science)]]
* [[Giry monad]]
* [[probability theory]]
* [[measure theory]]
* [[valuation (measure theory)]]


## References

* {#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

* {#Giry80} Mich&#232;le Giry, _A categorical approach to probability theory_, Categorical aspects of topology and analysis (Ottawa, Ont., 1980), pp. 68&#8211;85, Lecture Notes in Math. **915** Springer 1982.

* {#swirszcz} T. Swirszcz, _Monadic functors and convexity_, Bulletin de l'Academie Polonais des Sciences 22, 1974 ([pdf](https://www.fuw.edu.pl/~kostecki/scans/swirszcz1974.pdf))

* {#radonkeimel} [[Klaus Keimel]], _The monad of probability measures over compact ordered spaces and its Eilenberg-Moore algebras_, Topology and its Applications, 2008 ([doi:10.1016/j.topol.2008.07.002](https://doi.org/10.1016/j.topol.2008.07.002))

* {#Heckmann96} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996 ([doi:10.1111/j.1749-6632.1996.tb49168.x](https://doi.org/10.1111/j.1749-6632.1996.tb49168.x),[pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf))

* {#jung} Mauricio Alvarez-Manilla, Achin Jung, Klaus Keimel, _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0304397504004074).

* {#jonesplotkin} C. Jones and [[Gordon. D. Plotkin]], _A probabilistic powerdomain of evaluations_, LICS 4, 1989. ([doi:10.1109/LICS.1989.39173](https://doi.org/10.1109/LICS.1989.39173))

* {#algebras} [[Jean Goubault-Larrecq]] and Xiaodong Jia, _Algebras of the extended probabilistic powerdomain monad_, ENTCS 345, 2019
([doi:10.1016/j.entcs.2019.07.015](https://doi.org/10.1016/j.entcs.2019.07.015))

* {#support} [[Tobias Fritz]], Paolo Perrone and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019. [Link here](https://arxiv.org/abs/1910.03752).

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

* {#vanbreugel} Franck van Breugel, _The metric monad for probabilistic nondeterminism_, unpublished, 2005. ([pdf](http://www.cse.yorku.ca/~franck/research/drafts/monad.pdf))

* {#kantorovich19} [[Tobias Fritz]] and Paolo Perrone, _A probability monad as the colimit of spaces of finite samples_, Theory and Applications of Categories 34, 2019. ([pdf](http://www.tac.mta.ca/tac/volumes/34/7/34-07.pdf))

* {#orderedkantorovich} [[Tobias Fritz]] and Paolo Perrone, _Stochastic order on metric spaces and the ordered Kantorovich monad_, submitted, 2018. ([arXiv:1808.09898](https://arxiv.org/abs/1808.09898))

* {#jacobs} [[Bart Jacobs]], _From probability monads to commutative effectuses_, Journal of Logical and Algebraic Methods in Programming 94, 2018. 
([doi:10.1016/j.jlamp.2016.11.006](https://doi.org/10.1016/j.jlamp.2016.11.006))

* {#fritzconvex} [[Tobias Fritz]], _Convex spaces I: definitions and examples_, 2009. ([arXiv:0903.5522](https://arxiv.org/abs/0903.5522))


[[!redirects probability monad]]
[[!redirects probability monads]]
[[!redirects measure monad]]
[[!redirects measure monads]]
[[!redirects valuation monad]]
[[!redirects valuation monads]]
[[!redirects monad of probability]]
[[!redirects monads of probability]]
[[!redirects monad of probability measures]]
[[!redirects monads of probability measures]]
[[!redirects monad of measures]]
[[!redirects monads of measures]]
[[!redirects monad of valuations]]
[[!redirects monads of valuations]]
[[!redirects monads of probability measures valuations]]
[[!redirects monads of probability measures and valuations]]
[[!redirects monads of probability, measures and valuations]]
[[!redirects monads of probability, measures, valuations]]