
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

[[valuation (measure theory)|Valuations]] and [[measures]] have very similar constructions and applications, with [[$\tau$-additive measures]] somewhat in between.
Here we review which concepts correspond to each other. 
Note that on many topological spaces of interest, such as [[metric spaces]], most of the constructions below [[valuation (measure theory)#extending_valuations_to_measures|coincide]].

## Table

<table><tr><th markdown="1">Concept&#8595;\Theory&#8594;</th><th markdown="1">[[measure|Measures (traditional)]]</th><th markdown="1">[[τ-additive measures]]</th><th markdown="1">[[valuation (measure theory)|Valuations]]</th></tr>
<tr><th markdown="1">[[space|Spaces]]</th><td>[[measurable space|Measurable spaces]]</td><td>[[topological space|Topological spaces]]</td><td>[[locale|Locales]]</td></tr>
<tr><th markdown="1">[[morphism|Maps]]</th><td>[[measurable function|Measurable maps]]</td><td>[[continuous map|Continuous maps]]</td><td>[[continuous map|Continuous maps (of locales)]]</td></tr>
<tr><th markdown="1">Events</th><td>[[measurable subset|Measurable sets]]</td><td>[[open set|Open sets]]</td><td>[[open set|Open sets (elements of the frame)]]</td></tr>
<tr><th markdown="1">Values</th><td>Non-negative [[real number|reals]]</td><td>Non-negative [[real number|reals]], with the lower [[semicontinuous topology]]</td><td>Non-negative [[one-sided real number|lower reals]]</td></tr>
<tr><th markdown="1">Functionals</th><td>[[measure|Measures]]</td><td>[[tau-additive measure|$\tau$-additive Borel measures]]</td><td>[[valuation (measure theory)|Continuous valuations]]</td></tr>
<tr><th markdown="1">Finitary linearity</th><td>Additivity</td><td>Additivity</td><td>Modularity</td></tr>
<tr><th markdown="1">Infinite linearity</th><td markdown="1">$\sigma$-additivity</td><td markdown="1">$\tau$-additivity</td><td>[[Scott continuity|(Scott) continuity]]</td></tr>
<tr><th markdown="1">[[intensive or extensive quantity|Integrands]]</th><td>[[measurable function|Measurable]] real-valued functions</td><td>[[semicontinuous map|Lower semicontinuous]] real functions</td><td>[[continuous map|Continuous functions]] into the [[one-sided real number|lower reals]]</td></tr>
<tr><th markdown="1">Approximation of integrands</th><td>Pointwise-increasing [[sequence|sequences]] (of measurable real functions)</td><td>Pointwise-increasing [[net|nets]] (of lower semicontinuous real functions)</td><td>Pointwise-increasing [[net|nets]] (of continuous functions into the lower reals)</td></tr>
<tr><th markdown="1">Integral</th><td>[[Lebesgue integral]]</td><td>[[Lebesgue integral]]</td><td>[[valuation (measure theory)#integration|Lower integral]]</td></tr>
<tr><th markdown="1">[[monad|Monad]]</th><td>[[Giry monad]]</td><td>[[Extended probabilistic powerdomain]]</td><td>[[valuation monad]]</td></tr></table>

## References

* V. Bogachev, _Measure Theory_, vol. 2 (2007).

* {#monad} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996. [Link here](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf).

* Mauricio Alvarez-Manilla, Achin Jung, Klaus Keimel, _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0304397504004074).

* {#kirch} Olaf Kirch, _Bereiche und Bewertungen_ (in German), Master Thesis, Technische Hochschule Darmstadt, 1993. [Link here](http://fb04286.mathematik.tu-darmstadt.de/fbereiche/logik/research/Domains/papers/kirch/diplom.ps.gz).

* {#jung} Achim Jung, _Stably compact spaces and the probabilistic powerspace construction_, ENTCS 87, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S1571066104051345)

* [[Thierry Coquand]] and [[Bas Spitters]], _Integrals and Valuations_, 2009. [Link here](http://logicandanalysis.org/index.php/jla/article/view/14/12).


* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

* {#vintegral} [[Steve Vickers]], _A localic theory of lower and upper integrals_, 2008. [Link here](https://onlinelibrary.wiley.com/doi/abs/10.1002/malq.200710028).
