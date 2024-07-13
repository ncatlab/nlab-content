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
* The component $\eta_S:X\to S X$ of the [[unit]] of the [[zero-one+measure#the_monad_of_zeroone_measures|zero-one measure monad]] is an [[isomorphism]].
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

Sober measurable spaces form a [[reflective subcategory]] of [[Meas]]. That is, the inclusion functor $SoberMeas\hookrightarrow Meas$ has a [[left adjoint]] $S:Meas\to SoberMeas$. 
It maps a measurable space $X$ to the [[zero-one measure#the_monad_of_zeroone_measures|space of zero-one measures]] over it, which is equivalently given by the following [[equalizer]],
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
SX \ar[hookrightarrow]{r}{\iota} & PX \ar[shift left]{r}{\delta} \ar[shift right]{r}[swap]{P\delta} & PPX 
\end{tikzcd}
where $P$ denotes the [[Giry monad]] and $\delta$ is its unit. 

Analogously to the [[sober topological space|case of topological spaces]], this functor is sometimes called the *sobrification*. 

To see its [[universal property]], notice that by naturality of $\delta$, and by definition of equalizer, there is a unique map $X\to S X$ making the triangle below commute.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
X \ar{dr}{\delta} \ar[dashed]{d} \\
SX \ar[hookrightarrow]{r}{\iota} & PX \ar[shift left]{r}{\delta} \ar[shift right]{r}[swap]{P\delta} & PPX 
\end{tikzcd}
This map $X\to SX$ forms the unit of the [[adjunction]]. 

(More on this at [[zero-one measure#the_monad_of_zeroone_measures|zero-one measure]].)


## Related entries

* [[zero-one kernel]], [[Markov kernel]], [[Stoch]]
* [[sober topological space]], [[locale]], [[point of a locale]], [[frame]], [[point-free topology]]
* [[Markov category]], [[probability monad]]


## References

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk. ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability


[[!redirects sober measurable spaces]]