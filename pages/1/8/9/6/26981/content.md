+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--

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

*Sober measurable spaces* are to [[measurable spaces]] as [[sober topological spaces]] are to [[topological spaces]].

(...)


## Definition

A [[measurable space]] $X$ is called **sober** if any of the following equivalent conditions hold:

* Every [[zero-one measure]] on $X$ is the [[Dirac measure|Dirac delta]] over a unique point.
* Every [[zero-one kernel]] into $X$ is [[Markov kernel#kernels_from_deterministic_functions|induced by]] a unique [[measurable function]]. 
* The following [[diagram]] of [[Meas]] is an [[equalizer]],
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
X \ar{r}{\delta} & PX \ar[shift left]{r}{\delta} \ar[shift right]{r}[swap]{P\delta} & PPX
\end{tikzcd}
where $P$ denotes the [[Giry monad]] and $\delta$ is its [[unit]], given by [[Dirac measure|Dirac deltas]]. (Note that the diagram is always a [[fork]], by [[naturality]] of $\delta$.)

### Analogy with the topological case

Compare the definition with the following equivalent conditions in order for a [[topological space]] to be [[sober topological space|sober]]:

* Every [[completely prime filter]] (or classically equivalently, [[irreducible closed set]], [[point of a locale]]) is induced by a unique point.
* Every [[morphism of locales]] into $X$ is induced by a unique [[continuous function]]. 
* The following [[diagram]] of [[Top]] is an [[equalizer]],
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
X \ar{r}{\sigma} & VX \ar[shift left]{r}{\sigma} \ar[shift right]{r}[swap]{V\sigma} & VVX
\end{tikzcd}
where $V$ denotes the monad of [[closed subsets]] (with the [[lower Vietoris topology]]) and $\sigma$ is its [[unit]], given by (closures of) [[singletons]].


## Categorical properties

(...)


## Related entries

* [[zero-one kernel]], [[Markov kernel]], [[Stoch]]
* [[sober topological space]], [[locale]], [[point of a locale]], [[frame]], [[point-free topology]]
* [[Markov category]], [[probability monad]]


## References

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk. ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability


[[!redirects sober measurable spaces]]