
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

(...work in progress...)

## Unit and multiplication

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
  <td markdown="1">[[Probability measures]]</td>
  <td markdown="1">Initial [[$\sigma$-algebra]] of evaluation maps</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Giry monad]]</th>
  <td markdown="1">[[Pol]]</td>
  <td markdown="1">[[Borel measure|Borel probability measures]]</td>
  <td markdown="1">Initial topology of integration maps</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Radon monad]]</th>
  <td markdown="1">[[compactum#category_of_compacta|Comp]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]]</td>
  <td markdown="1">Weak topology w.r.t. continuous functions</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Ordered Radon monad]]</th>
  <td markdown="1">[[Compact ordered spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]]</td>
  <td markdown="1">Weak topology w.r.t. continuous functions, [[stochastic order]]</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Kantorovich monad]]</th>
  <td markdown="1">[[Cauchy-complete|Complete]] [[metric spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] of finite first moment</td>
  <td markdown="1">[[Kantorovich-Wasserstein metric]]</td>
  <td markdown="1">Closed [[convex subsets]] of [[Banach spaces]]</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[(Ordered) Kantorovich monad]]</th>
  <td markdown="1">[[Cauchy-complete|Complete]] [[$L$-ordered]] [[metric spaces]]</td>
  <td markdown="1">[[Radon measure|Radon probability measures]] of finite first moment</td>
  <td markdown="1">[[Kantorovich-Wasserstein metric]], [[stochastic order]]</td>
  <td markdown="1">Closed [[convex subsets]] of [[ordered Banach spaces]]</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Probability monad for topological spaces]]</th>
  <td markdown="1">[[Top]]</td>
  <td markdown="1">[[$\tau$-additive]] [[probability measures]]</td>
  <td markdown="1">initial topology of evaluation maps ("A-topology"), [[stochastic order]]</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Probabilistic powerdomain]]</th>
  <td markdown="1">[[dcpo]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">[[stochastic order]]</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Extended probabilistic powerdomain]]{#extprobpow}</th>
  <td markdown="1">[[Top]]</td>
  <td markdown="1">[[continuous valuations]]</td>
  <td markdown="1">initial topology of evaluation maps, [[stochastic order]]</td>
  <td markdown="1">...</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Distribution monad]] (a.k.a. finitary Giry monad, convex combination monad)</th>
  <td markdown="1">[[Set]]</td>
  <td markdown="1">[[Convex combinations]] or finitely-[[support#in_measure_theory|supported]] [[probability measures]]</td>
  <td markdown="1">(just a set)</td>
  <td markdown="1">[[convex spaces|Convex spaces]]</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Infinitary distribution monad]] (a.k.a. countable convex combination monad)</th>
  <td markdown="1">[[Set]]</td>
  <td markdown="1"> Countable [[convex combinations]] or countably-[[support#in_measure_theory|supported]] [[probability measures]]</td>
  <td markdown="1">(just a set)</td>
  <td markdown="1">[[Hyperconvex spaces]]</td>
  <td markdown="1">...</td>
 </tr>
 <tr>
  <th markdown="1">[[Valuation monad]]</th>
  <td markdown="1">[[Loc]]</td>
  <td markdown="1">[[contiuous valuations]]</td>
  <td markdown="1">initial topology of evaluation maps</td>
  <td markdown="1">...</td>
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

* {#monad} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996. [Link here](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf).

* Mauricio Alvarez-Manilla, Achin Jung, Klaus Keimel, _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0304397504004074).

* {#support} [[Tobias Fritz]], Paolo Perrone and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019. [Link here](https://arxiv.org/abs/1910.03752).

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

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