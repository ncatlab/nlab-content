<div class="rightHandSide toc">
[[!include mathematicscontents]]
</div>



> Page under construction with notes from blog entries.

#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##

Probability theory is concerned with mathematical models of phenomena that exhibit _randomness_ , or more generally phenomena about which one has incomplete information.


Its central mathematical model is based mostly on [[measure theory]]. So from a pure mathematical viewpoint probability theory today could be characterized as the study of [[measurable space]]s with a finite volume normalized to $1$. 

Broader perspectives may stress the relevance of other pure mathematical concepts for probability theory, or include aspects of the interpretation of mathematical results to phenomenology, the latter part making naturally contact with the field of [[statistics]].

Notice that in this respect probability theory has a similar status as (other(?!)) theories of [[physics]]: there is a mathematical model (measure theory here as the model for probability theory, or for instance [[symplectic geometry]] as a model for [[classical mechanics]]) which can be studied all in itself, and then there is in addition a more or less concrete idea of how from that model one may deduce statements about the observable world (the average outcome of a dice role using probability theory, or the observability of the next solar eclipse using [[Hamiltonian mechanics]]). The step from the mathematical model to its use as a tool for making statements about the observable world is subtle, maybe a subject of [[philosophy]], but in any case outside of the realm of [[mathematics]]. In probability theory the meaning of this step is traditionally a cause of debate, with two antagonistic main schools of thought being the _frequentist interpretation_ and the _Bayesian perspective_ on the nature of the relation of probability theory to the observable world.


## Abstract ##
...

## Definition ##
...

##Statistical Manifolds##

Families of probability distributions often form statistical models, that is, submanifolds of the space of all probability measures on a sample space. Techniques from [[differential geometry]] may be applied in a theory known as [[information geometry]].

##Probability theory from the nPOV##

We describe here some perspectives on probability theory from the [[nPOV]].

[[Prakash Panangaden]] in [Probabilistic Relations](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.4840) defines the [[category]] $SRel$ (stochastic [[relation]]s) to have as [[object]]s [[set]]s equipped with a $\sigma$-field. [[morphism|Morphisms]] are conditional probability densities or stochastic kernels. So, a morphism from $( X, \Sigma_X)$ to $( Y, \Sigma_Y)$ is a function $h: X \times \Sigma_Y \to [0, 1]$ such that 

1. $\forall B \in \Sigma_Y . \lambda x \in X . h(x, B)$ is a bounded measurable function,
1. $\forall x \in X . \lambda B \in \Sigma_Y . h(x, B)$ is a subprobability measure on $\Sigma_Y$.

If $k$ is a morphism from $Y$ to $Z$, then $k \cdot h$ from $X$ to $Z$ is defined as $(k \cdot h)(x, C) = \int_Y  k(y, C)h(x, d y)$.

This is based on work by [[Michele Giry]], which in turn was based on earlier work by [[Bill Lawvere]]. This definition differs from Giry's in the second clause where subprobability measures are allowed, rather than ordinary probability measures.

Panangaden notes that something very similar to the way that the category of relations can be constructed from the [[power set]] [[functor]] is at stake. Just as the category of relations is the [[Kleisli category]] of the powerset functor over the category of sets [[Set]], $SRel$ is the Kleisli category of the functor over the category of [[measurable space]]s and [[measurable function]]s which sends a measurable space, $X$, to the measurable space of sub[[probability measure]]s on $X$. This functor gives rise to a [[monad]].

What is gained by the move from probability measures to subprobability measures? One motivation seems to be to model probabilistic processes from $X$ to a [[coproduct]] $X + Y$. This you can iterate to form a process which looks to see where in $Y$ you eventually end up. This relates to $SRel$ being traced.

There is a [[monad]] on $MeasureSpaces$, $1 + -: Meas \to Meas$. A probability measure on $1 + X$ is a subprobability measure on $X$. Panangaden's monad is a composite of Giry's and $1 + -$.

The opposite of the Kleisli category of Giry's monad has as morphisms $X \to Y$, linear maps from bounded functions on $X$ to bounded functions on $Y$, which send the characteristic function on $X$ to the characteristic function on $Y$.

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


There are interesting developments of the representation of probability theory through monads, such as Abramsky et al.'s [Nuclear and Trace Ideals in Tensored &#8727;-Categories](http://arxiv.org/abs/math/9805102), which looks to work Giry's monad into a context even more closely resembling the category of relations.


* Mich&#232;le Giry, _A categorical approach to probability theory_  Categorical aspects of topology and analysis (Ottawa, Ont., 1980), pp. 68&#8211;85, Lecture Notes in Math., 915, Springer.


(According to Zoran) There are some analytic incorrectnesses there I was told. Prof. Voevodsky gave some talk at IHES where he had approached some biology-motivated stochastics via a refined Giry approach, I was told by Roland who got then interested in. A priori I think the approach is not giving something deep,  but it is an interesting source of analogies. There are many papers after Giry, mainly in the computer science literature. Roland drew my attention to Doberkat's paper as one of very few which are actually good among the mentioned papers. Though good part of the paper is only a survey.  

Voevodsky has also worked on a category theoretic treatment of probability theory: [Talk abstract](http://www.math.miami.edu/anno/voevodsky.htm)

>...a categorical study of probability theory where "categorical" is understood in the sense of category theory. Originally, I developed this approach to probability to get a better understanding of the constructions which I had to deal with in population genetics. Later it evolved into something which seems to be also interesting from a purely mathematical point of view. On the elementary level it gives a category which is useful for the work with probabilistic constructions involving complicated combinations of stochastic processes of different types. On a more advanced level, applying in this context the old idea of a functor as a generalized object one gets a better view of the relationship between probability and the theory of (pre-)ordered topological vector spaces. 


###References###

* The Metric Monad for Probabilistic Nondeterminism by Franck van Breugel, where we see both the Lawvere/Giry monad and Panangaden's monad.

* Kleisli Morphisms and Randomized Congruences for the Giry Monad by E.-E. Doberkat

* N. N. Cencov.  Statistical Decisions Rules and Optimal Inference.  Translations of Mathematical Monographs.  Volume 53.  American Mathematical Society.  1982.

(blog comment) Cencov's "category of statistical decisions" coincides with Giry's (Lawvere's) category.  I have the sense that Cencov discovered this category independently of Lawvere although years later.

To do:

* Relate to [convex spaces](http://golem.ph.utexas.edu/category/2009/04/convex_spaces.html)
* Bring in material from [Progic posts](http://golem.ph.utexas.edu/category/2007/09/progic.html)