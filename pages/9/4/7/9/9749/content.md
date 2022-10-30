
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

## Outline

* Mich&#232;le Giry, _A categorical approach to probability theory_  Categorical aspects of topology and analysis (Ottawa, Ont., 1980), pp. 68&#8211;85, Lecture Notes in Math., 915, Springer.

was based on earlier work of her advisor, [[Bill Lawvere]]. In the paper, there are allegedly a few minor analytically incorrect points and gaps in proofs, observed by later authors. 

For a number of reasons, researchers prefer to work with $Pol$, the category of [[Polish space]]s, i.e., separable [[metric space]]s for which a complete metric exists. We have an endofunctor $P$, which sends a space, $X$, to the space of probability measures on the Borel sets of $X$. $P(X)$ is equipped with the weakest topology which makes $\tau \mapsto \int_{X}f d\tau$ continuous for any $f$, a bounded, continuous, real function on $X$. We also need a map $\mu_{X}: P(P(X)) \to P(X)$:

$$
\mu_X (M)(A) := \int_{P(X)} \tau(A) M(d\tau).
$$

[[Ernst-Erich Doberkat]] in [Characterizing the Eilenberg-Moore Algebras for a Monad of Stochastic Relations](https://eldorado.tu-dortmund.de/bitstream/2003/2717/1/147.pdf) works out the [[algebra over a monad|algebra]]s for the Giry monad. We want measurable maps between $P(X)$ and $X$, such that the 'fibres' are convex and closed, and such that $\delta_{x}$, the delta distribution on $x$, is in the fibre over $x$. And there's another condition which requires a compact subset of $P(X)$ to be sent to a compact subset of $X$.

Now, as ever, $P(X)$ will support an algebra, $\mu_{X}: P(P(X)) \to P(X)$. This is the analogue of a [[free construction|free]] [[group]] being an algebra of the group monad. But just as there are many interesting groups which are not free, we should want to find algebras of Giry's monad which are not of the $\mu_{X}$ form. Doberkat shows that for such an algebra $X$ must be connected, and suggests this example

$$
h: P([0, 1]) \ni \tau \mapsto \int_{0}^{1} t \tau (dt) \in [0, 1].
$$

(I believe that this might be $\mu_{\{0, 1\}}$. After all, probability measures on $\{0, 1\}$ are just binomial, parameterised by $p \in [0, 1]$.)

The other example he gives has $X$ a bounded, closed and convex subset of $\mathbb{R}^n$, and probability measures being sent to their barycentre. 

Doberkat has a longer article on [[Eilenberg-Moore algebra]]s of the Giry monad as item 5 [here](http://ls10-www.cs.uni-dortmund.de/index.php?id=18). (Unfortunately, the monograph 'Stochastic Relations: Foundations for Markov Transition Systems' doesn't appear to be available.) There are two monads being treated here, one which sends a Polish space to the space of all probability measures, the other to the space of all subprobability measures. The extra structure relating to these monads, is that of a (positive) convex structure. In the case of a convex structure, this intuitively captures the idea that a weighted sum of points in the space has barycentre within the space. 

Doberkat's work relates to the category of Polish spaces with continuous maps. He notes that it would be interesting to develop the theory for the general case of Borel measurable maps.

### Voevodsky's work

Voevodsky has also worked on a category theoretic treatment of probability theory, and gave few talks on this at IHES, Miami, in Moscow etc. Voevodsky had in mind applications in [[mathematical biology]], for example, population genetics: 

See [Miami Talk abstract](http://www.math.miami.edu/anno/voevodsky.htm)

>...a categorical study of probability theory where "categorical" is understood in the sense of category theory. Originally, I developed this approach to probability to get a better understanding of the constructions which I had to deal with in population genetics. Later it evolved into something which seems to be also interesting from a purely mathematical point of view. On the elementary level it gives a category which is useful for the work with probabilistic constructions involving complicated combinations of stochastic processes of different types. On a more advanced level, applying in this context the old idea of a functor as a generalized object one gets a better view of the relationship between probability and the theory of (pre-)ordered topological vector spaces. 

A talk in Moscow (20 Niv 2008, in Russian) can be viewed [here](http://www.mi.ras.ru/index.php?c=obs_sem/&l=1), [wmv 223.6 Mb](http://www.mi.ras.ru/media/335_full.wmv). Abstract:

> In early 60-ies Bill Lawvere defined a category whose objects are measurable spaces and morphisms are Markov kernels. I will try to show how this category allows one to think about many of the notions of probability theory in categorical terms and to connect probabilistic objects to objects of other types through various functors. 

### Panangaden's monad

[[Prakash Panangaden]] in [Probabilistic Relations](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.4840) defines the [[category]] $SRel$ (stochastic [[relation]]s) to have as [[object]]s [[set]]s equipped with a $\sigma$[[sigma-field|-field]]. [[morphism|Morphisms]] are conditional probability densities or stochastic kernels. So, a morphism from $( X, \Sigma_X)$ to $( Y, \Sigma_Y)$ is a function $h: X \times \Sigma_Y \to [0, 1]$ such that 

1. $\forall B \in \Sigma_Y . \lambda x \in X . h(x, B)$ is a bounded measurable function,
1. $\forall x \in X . \lambda B \in \Sigma_Y . h(x, B)$ is a subprobability measure on $\Sigma_Y$.

If $k$ is a morphism from $Y$ to $Z$, then $k \cdot h$ from $X$ to $Z$ is defined as $(k \cdot h)(x, C) = \int_Y  k(y, C)h(x, d y)$.

Panangaden's definition differs from Giry's in the second clause where subprobability measures are allowed, rather than ordinary probability measures.

Panangaden emphasises that the mechanism is similar to the way that the category of relations can be constructed from the [[power set]] [[functor]]. Just as the category of relations is the [[Kleisli category]] of the powerset functor over the category of sets [[Set]], $SRel$ is the Kleisli category of the functor over the category of [[measurable space]]s and [[measurable function]]s which sends a measurable space, $X$, to the measurable space of sub[[probability measure]]s on $X$. This functor gives rise to a [[monad]].

What is gained by the move from probability measures to subprobability measures? One motivation seems to be to model probabilistic processes from $X$ to a [[coproduct]] $X + Y$. This you can iterate to form a process which looks to see where in $Y$ you eventually end up. This relates to $SRel$ being traced.

There is a [[monad]] on $MeasureSpaces$, $1 + -: Meas \to Meas$. A probability measure on $1 + X$ is a subprobability measure on $X$. Panangaden's monad is a composite of Giry's and $1 + -$.

## References

Apart from Giry's paper, there are similar developments in

* Franck van Breugel, _The metric monad for probabilistic nondeterminism_, features both the Lawvere/Giry monad and Panangaden's monad.

* E.-E. Doberkat, _Kleisli morphisms and randomized congruences_ 

* N. N. Cencov, _Statistical decisions rules and optimal Inference_, Translations of Math. Monographs __53__, Amer. Math. Society 1982

(blog comment) Cencov's "category of statistical decisions" coincides with Giry's (Lawvere's) category.  I have the sense that Cencov discovered this category independently of Lawvere although years later.

* category cafe related to Giry monad: [category theoretic probability](http://golem.ph.utexas.edu/category/2007/02/category_theoretic_probability.html), [coalgebraic modal logic](http://golem.ph.utexas.edu/category/2009/09/coalgebraic_modal_logic.html) 
* Abramsky et al. _Nuclear and trace ideals in tensored &#8727;-Categories_,[arxiv/math/9805102](http://arxiv.org/abs/math/9805102), on the representation of probability theory through monads, which looks to work Giry's monad into a context even more closely resembling the category of relations. 

There is also relation with work of Jacobs et al. 

* Robert Furber, [[Bart Jacobs]], _Towards a categorical account of conditional probability_, [arxiv/1306.0831](http://arxiv.org/abs/1306.0831)


To do:

* Relate to [convex spaces](http://golem.ph.utexas.edu/category/2009/04/convex_spaces.html)
* Bring in material from [Progic posts](http://golem.ph.utexas.edu/category/2007/09/progic.html)

[[!redirects Giry monad]]
