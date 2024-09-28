+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An *observational monad* is a [[monad]] where, intuitively, one can distinguish two monadic (for example probabilistic) values by means of taking repeated independent observations. 

It is of particular importance in [[categorical probability]], where these observations correspond to [[iid random variables]].


## Definition

Let $C$ be a [[category]] with [[products]], and let $P$ be a symmetric [[monoidal monad]] (or [[commutative monad]]) on $C$.

Denote also by $C_T$ its [[Kleisli category]], which is then a [[copy-discard category]]. As usual, we have an [[adjunction]] $L:C\to C_T, R:C_T\to C$ such that $P=R\circ L$. 

Denote the [[comonad]] $L\circ R$ on $C_T$ again by $P$. (Note that this equips $C_T$ with a [[thunk-force category|thunk-force structure]].)
Finally, denote $\varepsilon_X:P X\to X$ the components of the [[counit]] of the adjunction. (In [[categorical probability]], this is known as the [[sampling map]].)

The monad $P$ is called **observational** if and only if 
for every object $X$, the family of morphisms of $C_T$
$$
\Big\{ P X \xrightarrow{\quad\mathrm{copy}\quad} (P X)^{\otimes n} \xrightarrow{\quad\varepsilon^{\otimes n}\quad} X^{\otimes n}\;,\; n \in \mathbb{N} \Big\}
$$
is [[jointly monic]].

The intuition is that one can distinguish two morphisms (for example, states) into $P X$ by sampling independently as many times as needed. 


A [[Markov category#representable_markov_categories|representable Markov category]] whose [[probability monad]] is observational is called an **observationally representable Markov category**.

## Properties

* The [[Giry monad]] is observational thanks to the [[pi-lambda theorem]] or, equivalently, the [[monotone class theorem]]. ([Moss-Perrone'22](#det_submonad))

* The [[Kleisli category]] of an observational monad, with its canonical [[copy-discard category|copy-discard]] and [[thunk-force category|thunk-force]] structures, is such that every [[Markov category#deterministic_morphisms|deterministic morphism]] is thunkable (the converse is always true). ([Moss-Perrone'22](#det_submonad))

* Every observationally representable Markov category is necessarily _almost-surely-compatibly representable_. That is, in the bijection
$$
f:X\xrightarrow{\qquad} Y \qquad\leftrightarrow\qquad f^\sharp:X \xrightarrow{\;(det)\;} P Y
$$
we have that for every state (probability measure) $p$ on $X$, two morphisms $f,g:X\to Y$ are $p$-[[almost surely equal]] if and only if $f^\sharp$ and $g^\sharp$ are. ([FGLPS](#supports))

* Observationality is related to [[de Finetti's theorem]]: stating the theorem as a [[limit]], observationality is closely related to the uniqueness part in the [[universal property]]. It coincides exactly with this uniqueness whenever the necessary [[Kolmogorov products]] exist.
([Moss-Perrone'22](#det_submonad))


## See also 

* [[probability theory]], [[categorical probability]]
* [[Giry monad]], [[probability monad]], [[Markov category]]
* [[strong monad]], [[monoidal monad]], [[commutative monad]]
* [[de Finetti's theorem]], [[iid random variables]]
* [[pi-lambda theorem]], [[monotone class theorem]]
* [[sober measurable space]], [[zero-one measure]]
* [[infinitary tensor product]], [[Kolmogorov extension theorem]]
* [[thunk-force category]], [[monad in computer science]]


## References:

The concept, in the form presented here, was first introduced in:

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

It also appears in:

* {#supports} [[Tobias Fritz]], Tomáš Gonda, Antonio Lorenzin, [[Paolo Perrone]] and Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, 2023. ([arXiv](https://arxiv.org/abs/22308.00651))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* {#quantum_definetti} [[Tobias Fritz]] and Antonio Lorenzin, _Involutive Markov categories and the quantum de Finetti theorem_, 2023. ([arXiv](https://arxiv.org/abs/2312.09666))

Related papers:

* {#fritz_representable} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, Theoretical Computer Science 961, 2023. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))


category: probability



[[!redirects obervational]]
[[!redirects obervationally]]
[[!redirects observationality]]
[[!redirects observational Markov category]]
[[!redirects observationally representable Markov category]]