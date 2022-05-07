
# Localic completion
* contents
{: toc}

## Idea

If $X$ is a [[metric space]], we can construct a version of its [[complete space|Cauchy completion]] as a [[locale]], by taking as basic opens formal symbols $B_\delta(x)$ representing [[open balls]], and imposing relations ensuring that the points are [[Cauchy filters]].  (We can equivalently regard $X$ as a [[Lawvere metric space]] and build a locale whose points are "Cauchy [[profunctors]]".)  This is the **localic completion** of $X$.

The construction can also be generalized in various ways.

## Definition

Consider the collection of "formal balls" $B(x,\delta)$, where $x\in X$ and $\delta\in\mathbb{Q}^+$ (technically this is just another notation for the ordered pair $(x,\delta)\in X\times \mathbb{Q}^+$).  We say:

* $B(x,\delta)\le B(y,\epsilon)$ if $d(x,y)+\delta\le\epsilon$
* $B(x,\delta)\lt B(y,\epsilon)$ if $d(x,y)+\delta\lt\epsilon$

The localic completion of $X$ is the [[locale]] presented by [[generators]] $B(x,\delta)$ and relations:

1. If $B(x,\delta)\le B(y,\epsilon)$ (as above) then $B(x,\delta)\le B(y,\epsilon)$ (in the locale)
2. $\top = \bigvee_{x\in X} B(x,\epsilon)$ for any $\epsilon$
3. $B(x,\delta)\cap B(y,\epsilon) = \bigvee \{ B(z,\eta) \mid B(z,\eta) \le B(x,\delta) \, \text{and} \, B(z,\eta) \le B(y,\epsilon) \}$
4. $B(x,\delta) = \bigvee \{ B(y,\epsilon) \mid B(y,\epsilon) \lt B(x,\delta) \}$

[Vickers](#VickersI) combines conditions (3) and (4) into:

* $B(x,\delta)\cap B(y,\epsilon) = \bigvee \{ B(z,\eta) \mid B(z,\eta) \lt B(x,\delta) \, \text{and} \, B(z,\eta) \lt B(y,\epsilon) \}$

On the other hand, condition (3) makes sense for any poset of generators replacing $\{B(x,\delta)\}$, and simply says that we regard the generators as a [[base]] rather than a [[subbase]].  Since the elements of a [[formal topology]] automatically form a base, [Palmgren](#Palmgren) (who works with formal topologies) can omit condition (3).

When interpreted as a [[geometric theory]], conditions (1)--(4) say that the localic completion of $X$ is the [[classifying locale]] for [[Cauchy filters]] in $X$ that are additionally *rounded* (condition (4)).

## Examples

* When $X$ is the rational numbers $\mathbb{Q}$, this yields the [[locale of real numbers]], which is in many respects better-behaved constructively than either its space of points (the [[Dedekind real numbers]]) or the completion of $\mathbb{Q}$ by Cauchy sequences (the [[Cauchy real numbers]]).  Thus, the localic completion provides a "good" notion of completion for arbitrary metric spaces which generalizes the good localic real numbers.

* By localically completing $\mathbb{Q}$ under a different metric, we obtain a "locale of [[p-adic numbers]]"; see [this MO question](http://mathoverflow.net/questions/214677/the-formal-p-adic-numbers).


## Generalizations

We can allow $X$ to be a [[pseudometric space]], a [[Lawvere metric space]], or even a "[[metric locale]]".  We can also allow $X$ to be a certain sort of [[uniform space]], with uniformity induced by a family of [[upper real number]] valued [[pseudometrics]].  See the references.


## References

* [[Steve Vickers]], "Localic Completion Of Generalized Metric Spaces I", [TAC](http://www.tac.mta.ca/tac/volumes/14/15/14-15abs.html)
{#VickersI}

* [[Steve Vickers]], "Localic Completion Of Generalized Metric Spaces II: Powerlocales", [pdf](http://www.cs.bham.ac.uk/~sjv/LocCompPower.pdf)

* [[Simon Henry]], *Localic Metric spaces and the localic Gelfand duality*, [arXiv](http://arxiv.org/abs/1411.0898)

* [[Erik Palmgren]], _Continuity on the real line and in formal spaces_. (2003). Revised version of U.U.D.M. Report 2003:32. [link](http://www2.math.uu.se/~palmgren/crealform-rvd2.pdf)
 {#Palmgren03}

* [[Erik Palmgren]], _From intuitionistic to point-free topology_ (2005) U.U.D.M. Report 2005:47. [link](http://www2.math.uu.se/~palmgren/homotopy.pdf)
 {#Palmgren05}

* [[Erik Palmgren]], _A constructive and functorial embedding of locally compact metric spaces into locales_. Topology and its Applications, 154
(2007), 1854--1880.
 {#Palmgren}

* [[Erik Palmgren]], _Resolution of the uniform lower bound problem in constructive analysis_, [link](http://onlinelibrary.wiley.com/doi/10.1002/malq.200710034/full)

* [[Bas Spitters]], _Locatedness and overt sublocales_, doi:10.1016/j.apal.2010.07.002 APAL

* [[Thierry Coquand]], [[Erik Palmgren]], [[Bas Spitters]], _Metric complements of overt closed sets_, Mathematical Logic Quarterly, 57(4), 373-378, 2011. [link](http://dx.doi.org/10.1002/malq.201010011)

* Tatsuji Kawai, _A point-free characterisation of Bishop locally compact metric spaces_, [link](http://www.logicandanalysis.com/index.php/jla/article/viewFile/239/120)

* Tatsuji Kawai. *Localic completion of uniform spaces*. Log. Methods Comput. Sci. 13 2017), no. 3, Paper No. 22, 39pp.  [arxiv](https://arxiv.org/abs/1703.02255)
