
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
  <td markdown="1">[[Radon measure|Radon probability measures]]</td>
  <td markdown="1">[[weak topology]] w.r.t. continuous functions</td>
  <td markdown="1">[[compact]] [[convex subsets]] of [[locally convex topological vector spaces]]</td>
  <td markdown="1">[Swirszcz '74](#swirszcz), [Keimel '08](#radonkeimel)</td>
 </tr>
 <tr>
  <th markdown="1">[[Radon monad#the_ordered_case|ordered Radon monad]]</th>
  <td markdown="1">[[compact ordered spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]]</td>
  <td markdown="1">[[weak topology]] w.r.t. continuous functions, [[stochastic order]]</td>
  <td markdown="1">[[compact]] [[convex subsets]] of [[ordered vector space|ordered]] [[locally convex topological vector spaces]]</td>
  <td markdown="1">[Swirszcz '74](#swirszcz), [Keimel '08](#radonkeimel)</td>
 </tr>
 <tr>
  <th markdown="1">[[extended probabilistic powerdomain#the_measure_monad_on_top|measure monad on Top]]</th>
  <td markdown="1">[[Top]]</td>
  <td markdown="1">[[τ-additive measures]]</td>
  <td markdown="1">[[extended probabilistic powerdomain#the_measure_monad_on_top|A-topology]], [[stochastic order]]</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[probabilistic powerdomain]]</th>
  <td markdown="1">[[dcpo]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">[[stochastic order]]</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[extended probabilistic powerdomain]]{#extprobpow}</th>
  <td markdown="1">[[Top]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">[[extended probabilistic powerdomain#spaces_of_valuations|initial topology of evaluation maps]], [[stochastic order]]</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[valuation monad on locales]]</th>
  <td markdown="1">[[Loc]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">[[initial topology]] of evaluation maps</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Kantorovich monad]]</th>
  <td markdown="1">[[Cauchy-complete|complete]] [[metric spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] of finite first moment</td>
  <td markdown="1">[[Kantorovich-Wasserstein metric]]</td>
  <td markdown="1">closed [[convex subsets]] of [[Banach spaces]]</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">(ordered) [[Kantorovich monad]]</th>
  <td markdown="1">[[Cauchy-complete|complete]] [[L-ordered]] [[metric spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] of finite first moment</td>
  <td markdown="1">[[Kantorovich-Wasserstein metric]], [[stochastic order]]</td>
  <td markdown="1">closed [[convex subsets]] of [[ordered Banach spaces]]</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[distribution monad]] (a.k.a. finitary Giry monad, convex combination monad)</th>
  <td markdown="1">[[Set]]</td>
  <td markdown="1">[[convex combinations]] or finitely-[[support#in_measure_theory|supported]] [[probability measures]]</td>
  <td markdown="1">(just a set)</td>
  <td markdown="1">[[convex spaces]]</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[infinitary distribution monad]] (a.k.a. countable convex combination monad)</th>
  <td markdown="1">[[Set]]</td>
  <td markdown="1"> countable [[convex combinations]] or countably-[[support#in_measure_theory|supported]] [[probability measures]]</td>
  <td markdown="1">(just a set)</td>
  <td markdown="1">[[hyperconvex spaces]]</td>
  <td markdown="1">...</td>
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

*{#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

* {#Giry80} Mich&#232;le Giry, _A categorical approach to probability theory_, Categorical aspects of topology and analysis (Ottawa, Ont., 1980), pp. 68&#8211;85, Lecture Notes in Math. **915** Springer 1982.

* {#swirszcz} T. Swirszcz, _Monadic functors and convexity_, Bulletin de l'Academie Polonais des Sciences 22, 1974 ([pdf](https://www.fuw.edu.pl/~kostecki/scans/swirszcz1974.pdf))

* {#radonkeimel} [[Klaus Keimel]], _The monad of probability measures over compact ordered spaces and its Eilenberg-Moore algebras_, Topology and its Applications, 2008 ([doi:10.1016/j.topol.2008.07.002](https://doi.org/10.1016/j.topol.2008.07.002))

* {#monad} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996. [Link here](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf).

* Mauricio Alvarez-Manilla, Achin Jung, Klaus Keimel, _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0304397504004074).

* {#support} [[Tobias Fritz]], Paolo Perrone and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019. [Link here](https://arxiv.org/abs/1910.03752).

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

* {#vanbreugel} Franck van Breugel, _The metric monad for probabilistic nondeterminism_, features both the Lawvere/Giry monad and Panangaden's monad.

(...more to come...)



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