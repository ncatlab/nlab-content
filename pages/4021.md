
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


## Idea ##

Probability theory is concerned with mathematical models of phenomena that exhibit _randomness_, or more generally phenomena about which one has incomplete information.


Its central mathematical model is based mostly on [[measure theory]]. So from a pure mathematical viewpoint probability theory today could be characterized as the study of [[measurable space]]s with a finite volume normalized to $1$. 

Broader perspectives may stress the relevance of other pure mathematical concepts for probability theory, or include aspects of the interpretation of mathematical results to [[phenomenology]], the latter part making naturally contact with the field of [[statistics]].

Notice that in this respect probability theory has a similar status as (other(?!)) theories of [[physics]]: there is a mathematical model (measure theory here as the model for probability theory, or for instance [[symplectic geometry]] as a model for [[classical mechanics]]) which can be studied all in itself, and then there is in addition a more or less concrete idea of how from that model one may deduce statements about the observable world (the average outcome of a dice role using probability theory, or the observability of the next solar eclipse using [[Hamiltonian mechanics]]). The step from the mathematical model to its use as a tool for making statements about the observable world is subtle, maybe a subject of [[philosophy]], but in any case outside of the realm of [[mathematics]]. In probability theory the meaning of this step is traditionally a cause of debate, with two antagonistic main schools of thought being the _frequentist interpretation_ and the _[[Bayesianism|Bayesian perspective]]_ on the nature of the relation of probability theory to the observable world.

## Theory

### Basic theory

[[random variable|Random variables]] are defined typically in terms of [[probability spaces]], cf. the basic entries on [[measure space]], [[probability space]], [[conditional expectation|conditional probability]]. The modern point of view  emphasises that many facts about [[random variables]] do not depend much on the choice of the probability spaces; the random variables are also often identified with their distributions.

Some argue that in the study of measure and probability, one should start not only with sigma algebra of measurable sets but also another of null sets. Somehow this is abstractly captured by the approach of commutative [[von Neumann]] algebras. 

### Stochastic (random) processes

(...)

[[ergodic process]]

(...)

### Statistical Manifolds 

Families of probability distributions often form statistical models, that is, submanifolds of the space of all probability measures on a sample space. Techniques from [[differential geometry]] may be applied in a theory known as [[information geometry]].

### Probability theory from the nPOV 

We describe here some perspectives on (parts of) probability theory from the categorical point of view (see [[nPOV]]). This perspective mainly applies to the study of situations involving Markov kernels and Chapman-Kolmogorov property. 

[[Prakash Panangaden]] in [Probabilistic Relations](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.4840) defines the [[category]] $SRel$ (stochastic [[relation]]s) to have as [[object]]s [[set]]s equipped with a $\sigma$[[sigma-field|-field]]. [[morphism|Morphisms]] are conditional probability densities or stochastic kernels. So, a morphism from $( X, \Sigma_X)$ to $( Y, \Sigma_Y)$ is a function $h: X \times \Sigma_Y \to [0, 1]$ such that 

1. $\forall B \in \Sigma_Y . \lambda x \in X . h(x, B)$ is a bounded measurable function,
1. $\forall x \in X . \lambda B \in \Sigma_Y . h(x, B)$ is a subprobability measure on $\Sigma_Y$.

If $k$ is a morphism from $Y$ to $Z$, then $k \cdot h$ from $X$ to $Z$ is defined as $(k \cdot h)(x, C) = \int_Y  k(y, C)h(x, d y)$.

This is based on earlier work by Michele Giry, see [[Giry's monad]].

* Mich&#232;le Giry, _A categorical approach to probability theory_  Categorical aspects of topology and analysis (Ottawa, Ont., 1980), pp. 68&#8211;85, Lecture Notes in Math., 915, Springer.

Panangaden's definition differs from Giry's in the second clause where subprobability measures, rather than ordinary probability measures, are allowed. 

Panangaden emphasises that the mechanism is similar to the way that the category of relations can be constructed from the [[power set]] [[functor]]. Just as the category of relations is the [[Kleisli category]] of the powerset functor over the category of sets [[Set]], $SRel$ is the Kleisli category of the functor over the category of [[measurable space]]s and [[measurable function]]s which sends a measurable space, $X$, to the measurable space of sub[[probability measure]]s on $X$. This functor gives rise to a [[monad]].

What is gained by the move from probability measures to subprobability measures? One motivation seems to be to model probabilistic processes from $X$ to a [[coproduct]] $X + Y$. This you can iterate to form a process which looks to see where in $Y$ you eventually end up. This relates to $SRel$ being traced.

There is a [[monad]] on $MeasureSpaces$, $1 + -: Meas \to Meas$. A probability measure on $1 + X$ is a subprobability measure on $X$. Panangaden's monad is a composite of Giry's and $1 + -$.

The opposite of the [[Kleisli category]] of [[Giry's monad]] has as morphisms $X \to Y$, linear maps from bounded functions on $X$ to bounded functions on $Y$, which send the characteristic function on $X$ to the characteristic function on $Y$.

For more details on Giry's monad and its variants see [[probability monad]].

### Generalizations

* [[quantum mechanics|Quantum mechanics]] studies [[complex number|complex]] probability amplitudes whose absolute square can be interpreted as the usual probability in the process of [[measurement]], i.e. quantum reduction. An alternative approach via [[Wigner's function]] has real, but possibly outside $[0,1]$, probabilities.

* Relatedly, noncommutative [[von Neumann algebras]] may be interpreted as a noncommutative measure theory, analogous to the role that [[C*-algebras]] play in [[noncommutative geometry]], see at _[[quantum probability]]_.

* The [[free probability]] theory of Voiculescu and others is another noncommutative generalization, with physical applications related to [[random matrix theory]].


## Applications

* [[statistical mechanics]]
* [[stochastic Loewner equation]] has relation to [[conformal field theory]] discovered by Schramm and collaborators including Fields medalist Werner.

## Related concepts

* [[probability space]], [[random variable]]

* [[expectation value]], 

* [[Radon-Nikodym derivative]], 

* [[cumulant]], 

* [[ergodic theory]], 

* [[statistics]], 

* [[stochastic process]], 

* [[Wiener measure]]

* [[Bayesian reasoning]]

* [[central limit theorem]]

* [[free probability]]

* [[quantum probability]]

* [[synthetic probability theory]]

* [[statistical significance]]

* [[p-value]]

## References

### General

The modern formalization of probability theory in [[measure theory]] originates around

* {#Kolmogorov33} [[Andrey Kolmogorov]], _Grundbegriffe der Wahrscheinlichkeitsrechnung_, Ergebnisse der Mathematik und Ihrer Grenzgebiete, Springer Berlin Heidelberg, 1933

Lecture notes include

* {#Grigoryan08} Alexander Grigoryan, _Measure theory and probability_, 2008 [pdf](https://www.math.uni-bielefeld.de/~grigor/mwlect.pdf)

* {#Tao10} [[Terence Tao]], _A review of probabiltiy theory_, 2010 ([web](https://terrytao.wordpress.com/2010/01/01/254a-notes-0-a-review-of-probability-theory/))

> just as the natural numbers can be defined abstractly without reference to any numeral system (e.g. by the Peano axioms), core concepts of probability theory, such as random variables, can also be defined abstractly, without explicit mention of a measure space; we will return to this point when we discuss free probability later in this course. 

* [[Terence Tao]], _Free probability_, 2010 ([web](https://terrytao.wordpress.com/2010/02/10/245a-notes-5-free-probability/))


* {#Dembo12} [[Amir Dembo]], _Probability theory_, 2012 ([pdf](http://statweb.stanford.edu/~adembo/stat-310a/lnotes.pdf))


For references related to [[Giry's monad]] and variants see there.

Formulation in [[category theory]]:

* [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence, and theorems on sufficient statistics_, ([arXiv:1908.07021](https://arxiv.org/abs/1908.07021))

* [[Kirk Sturtz]], _Categorical probability theory_ ([arXiv:1406.6030](https://arxiv.org/abs/1406.6030))

Formulation in [[topos theory]]:

* [[Alex Simpson]], _Probability sheaves and the Giry monad_, 2017 ([pdf](https://coalg.org/mfps-calco2017/calco-papers/calco2017-1.pdf), [talk recording](https://youtu.be/IMGoluu1mgc))

For a more convenient setting for 'higher-order' probability theory, that is, one which admits higher-order functions, the following article uses the [[cartesian closed category]] of [[quasi-Borel space|quasi-Borel spaces]] rather than the category of measurable spaces:

* [[Chris Heunen]], Ohad Kammar, Sam Staton, Hongseok Yang, _A Convenient Category for Higher-Order Probability Theory_, ([arXiv:1701.02547](https://arxiv.org/abs/1701.02547))


For big picture in probability theory see answers to 

* MathOverflow: [is-there-an-introduction-to-probability-theory-from-a-structuralist-categorical-p](http://mathoverflow.net/questions/20740/is-there-an-introduction-to-probability-theory-from-a-structuralist-categorical-p)

An instance of a "categorical thinking" (in a generalized sense) in solving probability problems is a solution to Buffon's noodle problem ([wikipedia](http://en.wikipedia.org/wiki/Buffon%27s_noodle)) discussed by 
Tom Leinster at nCafe [here](http://golem.ph.utexas.edu/category/2010/03/a_perspective_on_higher_catego.html).

* Klain, [[Gian-Carlo Rota]], _Introduction to geometric probability_


* John C. Baez, Jacob D. Biamonte, _A course on
quantum techniques for stochastic mechanics_, [pdf](http://math.ucr.edu/home/baez/stoch_stable.pdf)

Discussion from a perspective of [[formal logic]]/[[type theory]] is in 

* {#Toronto14} [[Neil Toronto]], _Useful Languages for Probabilistic Modeling and Inference_, PhD Thesis, 2014 ([pdf](http://cs.umd.edu/~ntoronto/papers/toronto-2014diss.pdf), [slides](http://cs.umd.edu/~ntoronto/papers/toronto-2014diss-slides.pdf))

[[Mikhail Gromov]] on possible generalizations/modifications of probability theory (especially probability theory seen as, fundamentally, a ""functor" from a "complex category" to a "simple category""), as well as applications of probability within and without pure mathematics:

* _Probability, symmetry, linearity. (six lectures)_. IHES, Nov 2014. ([videos](https://www.youtube.com/watch?v=aJAQVletzdY)) ([pdf](https://www.ihes.fr/~gromov/wp-content/uploads/2018/08/probability-huge-Lecture-Nov-2014.pdf)).

### As Euclidean field theory
 {#AsEuclideanFieldTheories}

Probability regarded as [[Euclidean quantum field theory]]:

(...) see references at _[[conformal field theory]]_

In relation to the [[mass gap problem]] in [[lattice gauge theory]]:

* [[Sourav Chatterjee]], _Yang-Mills for probabilists_, in: _Probability and Analysis in Interacting Physical Systems_, PROMS **283** (2019) Springer ([arXiv:1803.01950](https://arxiv.org/abs/1803.01950), [doi:10.1007/978-3-030-15338-0](https://link.springer.com/book/10.1007/978-3-030-15338-0))

* {#Chatterjee20} [[Sourav Chatterjee]], _A probabilistic mechanism for quark confinement_, Comm. Math. Phys. 2020 ([arXiv:2006.16229](https://arxiv.org/abs/2006.16229))



category: probability
[[!redirects probability]]
[[!redirects probabilities]]