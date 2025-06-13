+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

*Sober measurable spaces* are to [[measurable spaces]] as [[sober topological spaces]] are to [[topological spaces]].

More in detail, a measurable space is *sober* if and only if every [[zero-one measure]] on it is a [[Dirac measure|Dirac delta]] at a unique point.
Equivalently, if its [[sigma-algebra]] separates points, and if every irreducible measure is induced by a point. (See below.)

This allows to draw parallels between [[measure theory]] and [[point-free topology]].


## Definition

A [[measurable space]] $X$ is called **sober** if any of the following equivalent conditions hold:

* Every [[zero-one measure]] on $X$ is the [[Dirac measure|Dirac delta]] over a unique point.
* Every [[zero-one kernel]] into $X$ is [[Markov kernel#kernels_from_deterministic_functions|induced by]] a unique [[measurable function]]. 
* The component $\eta_S:X\to S X$ of the [[unit]] of the [[zero-one measure#the_monad_of_zeroone_measures|zero-one measure monad]] is an [[isomorphism]].
* The following [[diagram]] of [[Meas]] is an [[equalizer]],
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
X \ar{r}{\delta} & PX \ar[shift left]{r}{\delta} \ar[shift right]{r}[swap]{P\delta} & PPX
\end{tikzcd}
where $P$ denotes the [[Giry monad]] and $\delta$ is its [[unit]], given by [[Dirac measure|Dirac deltas]]. (Note that the diagram is always a [[fork]], by [[naturality]] of $\delta$.)

The last condition is sometimes called the *equalizing requirement* ([Moggi'91](#moggi)).

### Analogy with the topological case

Compare the definition with the following equivalent conditions in order for a [[topological space]] to be [[sober topological space|sober]]:

* Every [[completely prime filter]] (or classically equivalently, [[irreducible closed set]], [[point of a locale]]) is induced by a unique point.
* Every [[morphism of locales]] into $X$ is induced by a unique [[continuous function]]. 
* The component at $X$ of the unit of the [[sober topological space|sobrification monad]] is an isomorphism. 
* The following [[diagram]] of [[Top]] is an [[equalizer]],
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
X \ar{r}{\sigma} & VX \ar[shift left]{r}{\sigma} \ar[shift right]{r}[swap]{V\sigma} & VVX
\end{tikzcd}
where $V$ denotes the monad of [[closed subsets]] (with the [[lower Vietoris topology]]) and $\sigma$ is its [[unit]], given by (closures of) [[singletons]].


## Examples

* Every [[standard Borel space]] is sober.
* Given any measurable space $X$, the space of probability measures $P X$ ([[Giry monad]]) is always sober.
* The [[invariant sigma algebra]] of an [[ergodic dynamical system]] is in general *not* sober.


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
This map $X\to S X$ forms the unit of the [[adjunction]]. 

(More on this at [[zero-one measure#the_monad_of_zeroone_measures|zero-one measure]].)


## Separating points and having enough points

A [[sigma-algebra]] $\mathcal{A}$ on a set $X$ is said to **separate points** if any of the following equivalent conditions holds:

* Given $x,y\in X$, $x=y$ if and only if for all $A\in\mathcal{A}$, $x\in A$ if and only if $y\in A$. 
* Given $x,y\in X$, $x=y$ if and only if for every [[measurable function]] $f:(X,\mathcal{A})\to\mathbb{R}$, $f(x)=f(y)$.
* Given $x,y\in X$, $x=y$ if and only if for every [[Markov kernel]] $k:(X,\mathcal{A})\to (Y,\mathcal{B})$ and every $B\in\mathcal{B}$, $k(B|x)=k(B|y)$.
* The [[Dirac measure|Dirac delta map]] (unit of the [[Giry monad]]) $\delta:X\to P X$, $x\mapsto\delta_x$ is injective. 

This condition is analogous to the [[Kolmogorov topological space|T0 (Kolmogorov) separation axiom for topological spaces]]: it says that the sigma-algebra can distinguish any two points. 

One can also define an [[equivalence relation]] analogous to the [[specialization preorder]], as follows:
$$
x\sim y \qquad\Leftrightarrow\qquad \forall A\in\mathcal{A}, x\in A \Rightarrow y\in A .
$$
(Note that the relation is symmetric because [[sigma-algebras]], unlike [[topology|topologies]], are closed under [[complements]].)
A sigma-algebra separates points precisely if this relation is discrete. 


Every sober measurable space has a sigma-algebra which separates points. Just as [[sober topological space#properties|for topological spaces]], however, separating points is not enough: one also needs a condition of *having enough points*.

\begin{definition}
We say that a measurable space $(X,\mathcal{A})$ **has enough points** if and only if every [[zero-one measure]] is a [[Dirac measure]]. 
\end{definition}

This way, a measurable space is sober if and only if it separates points and it has enough points.


Here is another analogy with topological spaces: the sobrification process can be taken in two steps:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
column sep=large,%
]
X \ar[two heads]{r} & X/_\sim \ar[hook]{r} & SX
\end{tikzcd} 
First, we quotient under the relation of "being indistinguishable for the sigma-algebra" (analogous to the [[Kolmogorov topological space|Kolmogorov quotient]]). Then we "add the missing points". 

(Compare again with [[sober topological space|the topological case]].)


## Related entries

* [[zero-one measure]], [[zero-one kernel]], [[Markov kernel]], [[Stoch]]
* [[point-free measure theory]], [[Loomis-Sikorski duality]], [[measurable Gelfand duality]]
* [[sober topological space]], [[locale]], [[point of a locale]], [[frame]], [[point-free topology]]
* [[Markov category]], [[probability monad]]


## References

* {#fritz_lorenzin} [[Tobias Fritz]] and Antonio Lorenzin, _Categories of abstract and noncommutative measurable spaces_, 2025. ([arXiv](https://arxiv.org/abs/2504.13708))

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#br} Anna Bucalo and [[Giuseppe Rosolini]], _Sobriety for equilogical spaces_. Theorerical Computer Science 546, 2014. ([doi](https://doi.org/10.1016/j.tcs.2014.03.002))

* {#taylor} [[Paul Taylor]], _Sober spaces and continuations_. Theory and Applications of Categories 10(12), 2002. ([link](http://paultaylor.eu/asd/sobsc))

* {#moggi} [[Eugenio Moggi]], _Notions of computations and monads_, Information and Computation 93(1), 1991 (LICS 1989).

### Introductory material

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk. ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability


[[!redirects sober measurable spaces]]