
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

In many [[categorical approaches to probability theory]], one considers a [[category]] of [[spaces]], such as [[measurable spaces]] or [[topological spaces]], and equips this category with a [[monad]] whose [[functor]] part assigns to each space $X$ a space $P X$ of [[measures]], [[probability measures]], or [[valuation (measure theory)|valuations]] on $X$, or a variation thereof.

For probability theory, this can be interpreted as adding to the [[points]] of a space $X$ new "random points", modelled as probability measures or valuations.
The old points, which we can think of as deterministic, are embedded in $P X$ via the unit of the monad $X\to P X$. Just as well, the [[Kleisli morphisms]] of $P$ can be seen as [[stochastic maps]].
(Monads can be seen as ways of extending our spaces and functions to account for new phenomena, see for example *[[extension system]]* and *[[monad in computer science]]*.)
Note that these probability measures are technically different from [[random elements]]: they rather correspond to the [[law of a random variable|laws]] of the random elements.

[[algebra over a monad|Algebras]] of probability and measure monads can be interpreted as generalized [[convex spaces]] or [[conical spaces]] of a certain kind. For [[probability theory]], in particular, the algebras of a probability monad can be seen as spaces equipped with a notion of [[expectation value]] of a [[random variable]]. 
The details vary depending on the monad and on the category under consideration.

Many choices of categories and of monads are possible, depending on which aspects of measure theory or probability one wants to study. 
See [the table below](#detailed_list) for more details.

Note that "probability monad" and "measure monad" are not used here as technical terms with a definition. Here we just explain what most monads of this kind look like. 
(There are ongoing works which may give a general, precise definition of probability monad.)
The term "probability monad" was coined by Giry (see [here](#giry80)), to refer to what we today call the [[Giry monad]].

## Functor, unit and multiplication

### The functor: random outcomes

The basic idea, that holds for all monads of this sort, is that of forming spaces of [[random elements]], or rather their [[law of a random variable|laws]]. 

Consider a category $C$, whose objects we can think of as "spaces of outcomes" with possibly extra structure, such as [[measurable spaces]], or [[topological spaces]], or even just [[sets]]. 
A _probability monad_ assigns to each space $X$ a space $P X$ which we can think of as a space of "laws of random outcomes on $X$" or other measure-like entities.
For example,

* The [[distribution monad]] assigns to each [[set]] the [[distribution monad#finite_distributions|space of finite distributions]] on it.
* The [[Giry monad]] assigns to each [[measurable space]] the [[Giry monad#definition|space of probability measures]] over it.
* The [[extended probabilistic powerdomain]] assigns to each [[topological space]] the [[extended probabilistic powerdomain#spaces_of_valuations|space of continuous valuations]] on it.
* The [[Kantorovich monad]] assigns to each [[metric space]] the [[Kantorovich monad#wasserstein_spaces|Wasserstein space]] over it.

(See also the table [below](#detailed_list).)

A possible interpretation of probability monads, which uses the interpretation of [[monads]] as encoding generalized [[theories]], is that $P X$ is a space of "formal generalized convex combinations" (in the sense of [[convex space]]) of points of $X$. 
For instance, for the [[distribution monad]], given the set $\{heads,tails\}$ of possible outcomes of a coin flip, the set $P X$ contains for example the distribution that assigns probability $1/2$ to both outcomes. This can be thought of as the formal convex combination
$$
\frac{1}{2}\, heads + \frac{1}{2}\,tails.
$$

On the morphisms, the functor gives for example the [[pushforward of measures]]. 


### The unit: deterministic random variables

The [[unit]] of the [[monad]] gives, for each space of outcomes, a map $X\to P X$, which we can think of as picking out "those outcomes which are not really random", or "Dirac delta" (see [[Dirac measure]] and [[valuation (measure theory)#dirac_valuation|Dirac valuation]]). 

These can be seen as the laws of a [[deterministic random variable]].


### The multiplication: mixing probability measures.

The multiplication of the monad is a map $P P X\to P X$ for all objects $X$. This can be thought of as of [[convex mixture|mixing]] or [[average|averaging]] probability measures. 

The following example is taken from [Perrone '19, Example 5.1.2](#notesperrone). 
Suppose that you have two coins in your pocket. Suppose that one coin is fair, with "heads" on one face and "tails" on the other face; suppose the second coin has "heads" on both sides. Suppose now that you draw a coin randomly, and flip it.  We can sketch the probabilities in the following way:
  \begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
   &&& ? \ar{dll}[swap]{1/2} \ar{drr}{1/2} \\
   & \mathrm{coin} \,1 \ar{dl}[swap]{1/2} \ar{dr}{1/2} &&&& \mathrm{coin} \,2 \ar{dl}[swap]{1} \ar{dr}{0} \\
   \mathrm{heads} && \mathrm{tails} && \mathrm{heads} && \mathrm{tails}
  \end{tikzcd}
 Let $X$ be the set $\{heads,tails\}$. A coin gives a _law_ according to which we will obtain "heads" or "tails" so it determines an element of $P X$. Since the choice of coin is also random (we also have a _law on the coins_), the law on the coins determines an element of $P P X$.
 By averaging, the resulting overall probabilities are 

  \begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
   & ? \ar{dl}[swap]{3/4} \ar{dr}{1/4} \\
   \mathrm{heads} && \mathrm{tails}
  \end{tikzcd}

 In other words, the "average" or "mixture" can be thought of as an assignment $E:P P X\to P X$, from laws of "random random variables" to laws of ordinary random variables.


## Algebras: expectation values


According to the interpretation of probability monads in terms of "formal generalized convex combinations", the [[algebra over a monad|algebras]] of a probability monad are then spaces equipped with a way of evaluating these expressions to a result, which we can see as a generalized "[[mixture]]", "[[average]]", or "[[expectation value]]".
(Expectation values play a very important role in probability: probability monads can encode them via their algebras.)

In other words, algebras of probability monads can be thought of as generalizations of [[convex sets]], depending on the actual category and monad in question. For example,

* The [[algebra over a monad|algebras]] of the [[distribution monad]] are [[convex spaces]].
* The [[algebra over a monad|algebras]] of the [[Radon monad]] are [[compact space|compact]] convex subsets of [[locally convex topological vector spaces]].
* The [[algebra over a monad|algebras]] of the [[Kantorovich monad]] are closed convex subsets of [[Banach spaces]].

(See also the table [below](#detailed_list).)

If the measure are not required to be normalized, instead of (generalized) convex combinations one should think of linear combinations with non-negative coefficients, and so as algebras one gets a generalization of [[conical spaces]] instead.


## Kleisli morphisms: random maps

The basic interpretation of a Kleisli morphism, i.e. a map $X\to P Y$, is that of a _map with a random outcome_. 
For example,

* For the [[distribution monad]], Kleisli morphisms are [[stochastic maps]] (or [[stochastic matrices]]).
* For the [[Giry monad]], Kleisli morphisms are [[Markov kernels]].
* ...and so on. 

The [[Kleisli category|Kleisli composition]] recovers exactly the [[Chapman-Kolmogorov formula]] for the composition of stochastic maps. In the language of [[conditional probability]], this reads as 
$$
p(z|x) = \sum_y p(z|y) \, p (y|x)
$$
for the discrete case, and as
$$
p(A|x) = \int_Y p(A|y) \, d p(y|x)
$$
for the continuous case. 

(See [Giry's original article](#giry80) for the details, as well as the introductions given in [Perrone '18, Section 1.1](#thesisperrone) and [Perrone '19, Example 5.1.13](#notesperrone)).

[[Kleisli category|Kleisli categories]] of probability monads are often instances of [[Markov categories]].


## Monoidal structure: products and marginals

Probability monads are usually defined on [[monoidal categories]], in particular on [[cartesian monoidal categories]]. 
On product spaces $X\times Y$, the object $P(X\times Y)$ has the interpretation of containing [[joint distributions]]. Given a joint distribution, one can form the [[joint and marginal probability|marginals]] by pushing forward along the [[product]] projections $X\times Y\to X$ and $X\times Y\to Y$. This is in general a destructive operation, since [[stochastic dependence]] may be discarded.

Given [[marginal distributions]], one can form a canonical joint distribution by forming the [[product distribution]]. This is encoded by a [[monoidal monad|monoidal structure]] on the probability monad (or equivalently, a [[commutative monad|commutative strength]]), a map
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
PX\times PY \ar{r}{\nabla} & P(X\times Y)
\end{tikzcd}
which satisfies particular compatibility conditions. 
The Giry monad is monoidal on the category [[Meas]] with the [[cartesian product]]. Similar statements are true for most other probability and measure monads.

When the monad is [[affine monad|affine]], one has that *a product probability is necessarily the product of its marginals*. This is the case for monads of probability measures, but not for monads of unnormalized measures.

More on this at [[joint and marginal probability]].

## Duality

(...work in progress...)

## Detailed list 

[[!include table of probability monads]]


## See also

* [[monad]], [[algebra over a monad]], [[Kleisli category]]
* [[commutative monad]], [[affine monad]]
* [[monad (in computer science)]]
* [[Giry monad]], [[Markov kernel]], [[Stoch]]
* [[categorical probability]], [[Markov category]]
* [[joint and marginal distributions]]
* [[probability theory]], [[measure theory]]
* [[valuation (measure theory)]]
* [[expectation value]]


## References

* {#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

* {#Giry80} Mich&#232;le Giry, _A categorical approach to probability theory_, Categorical aspects of topology and analysis (Ottawa, Ont., 1980), pp. 68&#8211;85, Lecture Notes in Math. **915** Springer 1982.

* {#swirszcz} T. Swirszcz, _Monadic functors and convexity_, Bulletin de l'Academie Polonaise des Sciences 22, 1974 ([pdf](https://www.fuw.edu.pl/~kostecki/scans/swirszcz1974.pdf))

* {#radonkeimel} [[Klaus Keimel]], _The monad of probability measures over compact ordered spaces and its Eilenberg-Moore algebras_, Topology and its Applications, 2008 ([doi:10.1016/j.topol.2008.07.002](https://doi.org/10.1016/j.topol.2008.07.002))

* {#Heckmann96} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996 ([doi:10.1111/j.1749-6632.1996.tb49168.x](https://doi.org/10.1111/j.1749-6632.1996.tb49168.x),[pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf))

* {#jung} Mauricio Alvarez-Manilla, Achim Jung, [[Klaus Keimel]], _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004. [Link here](https://www.sciencedirect.com/science/article/pii/S0304397504004074).

* {#jonesplotkin} C. Jones and [[Gordon. D. Plotkin]], _A probabilistic powerdomain of evaluations_, LICS 4, 1989. ([doi:10.1109/LICS.1989.39173](https://doi.org/10.1109/LICS.1989.39173))

* {#algebras} [[Jean Goubault-Larrecq]] and Xiaodong Jia, _Algebras of the extended probabilistic powerdomain monad_, ENTCS 345, 2019
([doi:10.1016/j.entcs.2019.07.015](https://doi.org/10.1016/j.entcs.2019.07.015))

* {#support} [[Tobias Fritz]], [[Paolo Perrone]] and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, Mathematical Constructions in Computer Science 31(8), 2021. [arXiv](https://arxiv.org/abs/1910.03752).

* {#vmonad} [[Steve Vickers]], _A monad of valuation locales_, 2011. [Link here](https://www.cs.bham.ac.uk/~sjv/Riesz.pdf).

* {#vanbreugel} Franck van Breugel, _The metric monad for probabilistic nondeterminism_, unpublished, 2005. ([pdf](http://www.cse.yorku.ca/~franck/research/drafts/monad.pdf))

* {#kantorovich19} [[Tobias Fritz]] and [[Paolo Perrone]], _A probability monad as the colimit of spaces of finite samples_, Theory and Applications of Categories 34, 2019. ([pdf](http://www.tac.mta.ca/tac/volumes/34/7/34-07.pdf))

* {#orderedkantorovich} [[Tobias Fritz]] and [[Paolo Perrone]], _Stochastic order on metric spaces and the ordered Kantorovich monad_, Advances in Mathematics 366, 2020. ([arXiv:1808.09898](https://arxiv.org/abs/1808.09898))

* {#jacobs} [[Bart Jacobs]], _From probability monads to commutative effectuses_, Journal of Logical and Algebraic Methods in Programming 94, 2018. 
([doi:10.1016/j.jlamp.2016.11.006](https://doi.org/10.1016/j.jlamp.2016.11.006))

* {#fritzconvex} [[Tobias Fritz]], _Convex spaces I: definitions and examples_, 2009. ([arXiv:0903.5522](https://arxiv.org/abs/0903.5522))

* {#QBS} [[Chris Heunen]], [[Ohad Kammar]], [[Sam Staton]] and Hongseok Yang, _A convenient category for higher-order probability theory_, Proceedings of LICS 2017. ([arXiv](https://arxiv.org/abs/1701.02547))

* [[Sean Moss]], [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, Theoretical Computer Science 961, 2023. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

* {#KP24} Peter Kristel, Benedikt Peterseim, _A topologically enriched probability monad on the cartesian closed category of CGWH spaces_. ([arXiv](https://arxiv.org/abs/2404.08430))

An account in terms of [[codensity monads]] in:

* Ruben Van Belle, _Probability monads as codensity monads_. Theory and Applications of Categories 38 (2022), 811–842, ([tac](http://tac.mta.ca/tac/volumes/38/21/38-21abs.html))

An introduction to some of the concepts can be also found in:

* {#notesperrone} [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_, Chapter 5. ([arXiv](http://arxiv.org/abs/1912.10642))

* {#thesisperrone} [[Paolo Perrone]], _Categorical probability and stochastic dominance in metric spaces_, PhD thesis, Chapter 1. ([pdf](http://www.paoloperrone.org/phdthesis.pdf))

* [[Tobias Fritz]] and [[Paolo Perrone]], _Monads, partial evaluations, and rewriting_, MFPS 36, 2020 - Section 6. ([arXiv](https://arxiv.org/abs/1810.06037))

and in the following video lectures:

* [[Arthur Parzygnat]], _Categorical probability_, video playlist. ([YouTube](https://www.youtube.com/playlist?list=PLSx1kJDjrLRSKKHj4zetTZ45pVnGCRN80))

* [[Paolo Perrone]], _What is a probability monad?_, tutorial. ([YouTube](https://youtu.be/3Da88Tgw_rM))


category: probability

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
[[!redirects probability and measure monad]]
[[!redirects probability and measure monads]]
[[!redirects measure and valuation monad]]
[[!redirects measure and valuation monads]]
[[!redirects monads of probability measures valuations]]
[[!redirects monads of probability measures and valuations]]
[[!redirects monads of probability, measures and valuations]]
[[!redirects monads of probability, measures, valuations]]