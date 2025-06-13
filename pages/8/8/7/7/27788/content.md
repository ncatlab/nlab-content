+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+--{: .hide}
[[!include duality - contents]]
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

*Loomis-Sikorski duality* is a [[Stone-type duality]] between [[measurable spaces]] and particular ([[σ-complete Boolean algebras|σ-complete]]) [[Boolean algebras]], and it is one of the main approaches to [[point-free measure theory]].

It is closely related to [[point-free topology]], as well as to [[measurable Gelfand duality]] and to the duality between [[measure spaces|_measure_ spaces]] (not *measurable*) and [[measurable locales]]. 


## Main concepts

Recall that a [[measurable space]] is a [[set]] $X$ equipped with a [[σ-algebra]] $\Sigma$ of subsets of $X$. These subsets have the interpretation of 
"distinctions" that one can make, analogously to the open sets of a [[topology]]. Moreover, in the presence of a [[measure]], these are precisely the subsets which have a "size" (the value of the measure), and in [[probability theory]], they are the [[events]] to which one assigns a [[probability]].

In [[point-free measure theory]], just as in [[point-free topology]], one is interested in shifting the focus from the points of $X$ to the [[poset|ordered]] structure of $\Sigma$, and to study to which extent they determine one another.

### From measurable spaces to σ-complete Boolean algebras

Given a measurable space $(X,\Sigma_X)$, the [[σ-algebra]] $\Sigma_X$ is by definition closed under complements and countable unions. In other words it is a **[[σ-complete Boolean algebra]]** (also known as **Boolean σ-algebra**).

Given a measurable map $f:(X,\Sigma_X)\to (Y,\Sigma_Y)$, the inverse image map 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
\Sigma_Y \ar{r} & \Sigma_X \\
B \ar[mapsto]{r} & f^{-1}(B) 
\end{tikzcd}
preserves countable unions and complements, we therefore have a functor 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
\mathbf{Meas}^\mathrm{op} \ar{r}{\Sigma} & \sigma\mathbf{Bool}
\end{tikzcd}
from measurable spaces to σ-complete Boolean algebras (where the morphisms are required to preserve countable unions and complements).


### From σ-complete Boolean algebras to measurable spaces

Let $\Sigma$ be a σ-complete Boolean algebra. 
We can define a **point of $\Sigma$** to be any of the following equivalent structures:

* A [[zero-one measure]] on $\Sigma$, i.e. an assignment $p:\Sigma\to\{0,1\}$ which is countably additive and for which $p(X)=1$;
* An assignment $p:\Sigma\to\{0,1\}$ which is a morphism of σ-complete Boolean algebras;
* A *prime σ-filter* on $\Sigma$, i.e. a proper subset of $\Sigma$ which is closed under countable joins and meets;
* A  *σ-ultrafilter* on $\Sigma$, i.e. an [[ultrafilter]] on $\Sigma$ which is closed under countable meets.

Given a morphism $\phi:\Sigma\to\Gamma$ and a point $p$ of $\Gamma$, the composition $p\circ\phi$ is a point of $\Sigma$. 
Denoting by $Sp(\Sigma)$ the space of points of $\Sigma$ (or **spectrum**), we then have a function $\phi^*:Sp(\Gamma)\to Sp(\Sigma)$.

In order to turn this assignment into a functor $\sigma Bool^\mathrm{op}\to Meas$, we need to equip the spaces $Sp(\Sigma)$ with σ-algebras. We do it as follows (see also at [[zero-one measure##the_monad_of_zeroone_measures|zero-one measure - the monad]]): for every $A\in \Sigma$, define 
$$
A^* \coloneqq \{p\in Sp(\Sigma) : p(A)=1 \} .
$$
The sets $A^*$ form a σ-algebra, and the maps $\phi^*:Sp(\Gamma)\to Sp(\Sigma)$ are measurable. This gives the desired functor 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
\sigma\mathbf{Bool}^\mathrm{op} \ar{r}{\mathrm{Sp}} & \mathbf{Meas} .
\end{tikzcd}


### The adjunction

Just as in the topological case, the functors $\Sigma: Meas^{op} \to \sigma Bool$ and $Sp: \sigma Bool^{op}\to Meas$ form a (contravariant) [[idempotent adjunction]]:

* The [[unit of an adjunction|unit]] has as components measurable functions $\eta: X \to Sp(\Sigma_X)$ which map a point $x\in X$ to the corresponding [[principal filter]] on $\Sigma_X$ (or equivalently, to the [[Dirac measure|Dirac delta]] [[zero-one measure]]) $\delta_x$: for every $A\in\Sigma_X$,
$$
\delta_x (A) = \begin{cases}
1 & x\in A \\
0 & x\notin A .
\end{cases}
$$
* The [[counit]] has as components morphisms of $\sigma Bool^{op}$ in the form $\epsilon^{op}:\Sigma_{Sp(\Sigma)}\to\Sigma$, or equivalently, morphisms of $\sigma Bool$ of the form $\epsilon:\Sigma\to \Sigma_{Sp(\Sigma)}$ mapping $A\in\Sigma$ to the set $A^*\in\Sigma_{Sp(\Sigma)}$ defined above.

The adjunction induces an [[idempotent monad]] on $Meas$ (the [[zero-one measure#the_monad_of_zeroone_measures|monad of zero-one measures]]), and an idempotent monad on $\sigma Bool$ as well (or equivalently, an idempotent [[comonad]] on $\sigma Bool^{op}$).

As usual with idempotent adjunctions, we have that the [[fixed point of an adjunction|center]] is equivalently given by 

* The full subcategory of $Meas$ whose objects are those spaces for which the unit $\eta:X\to Sp(\Sigma_X)$ is an isomorphism. These are sometimes called [[sober measurable spaces]]. Analogously to [[sober topological spaces]], these are the spaces whose points are uniquely determined by the σ-algebra.
* The full subcategory of $\sigma Bool$ whose objects are those σ-algebras for which the counit $\epsilon:\Sigma\to \Sigma_{Sp(\Sigma)}$ is an isomorphism. These are sometimes called **spatial** or **concrete** σ-algebras.

Because of this, sometimes one calls the monad on $Meas$ the *sobrification monad*. 


## Particular results

(Work in progress. For now see the references.)

### Equivalence with measurable Gelfand duality

(See at [[measurable Gelfand duality#equivalence_with_loomissikorski_duality|measurable Gelfand duality - Equivalence with Loomis-Sikorski duality]], and in [FL'25, Section 4.1](#fritz_lorenzin).)


## See also

* [[sober measurable space]], [[zero-one measure]], [[zero-one kernel]]
* [[von Neumann algebra]], [[measure algebra]]
* [[σ-complete Boolean algebra]], [[monotone-complete $C^*$-algebra]]
* [[point-free measure theory]], [[measurable Gelfand duality]]
* [[Stone duality]], [[Gelfand duality]], [[Isbell duality]]
* [[categorical approaches to probability theory]]


## References

* Roman Sikorski, _Boolean Algebras_, Springer, 1969.

* Sean Moss and [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS, 2022. ([arXiv](https://arxiv.org/abs/2204.07003))

* Ruiyuan Chen, _A universal characterization of standard Borel spaces_. The Journal of Symbolic Logic, 88(2), 2023. ([arXiv](https://arxiv.org/abs/1908.10510))

* {#fritz_lorenzin} [[Tobias Fritz]] and Antonio Lorenzin, _Categories of abstract and noncommutative measurable spaces_, 2025. ([arXiv](https://arxiv.org/abs/2504.13708))


### Introductory material

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk. ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability


[[!redirects Stone duality for measurable spaces]]
[[!redirects Stone duality for sigma-algebras]]
[[!redirects Stone duality for σ-spaces]]
[[!redirects measurable Stone duality]]