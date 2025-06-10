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

It is closely related to [[point-free topology]], as well as to the duality between [[measure spaces|_measure_ spaces]] (not *measurable*) and [[measurable locales]]. 


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
* A *prime σ-filter* on $\Sigma$, i.e. a proper subset of $\Sigma$ which is closed under countable unions and intersections;
* A  *σ-ultrafilter* on $\Sigma$, i.e. an [[ultrafilter]] on $\Sigma$ which is closed under countable intersections.

(...work in progress...)


## See also

* [[sober measurable space]], [[zero-one measure]], [[zero-one kernel]]
* [[von Neumann algebra]], [[measure algebra]]
* [[σ-complete Boolean algebra]], [[monotone-complete $C^*$-algebra]]
* [[point-free measure theory]]
* [[Stone duality]], [[Gelfand duality]], [[Isbell duality]]
* [[categorical approaches to probability theory]]


## References

* Roman Sikorski, _Boolean Algebras_, Springer, 1969.

* Ruiyuan Chen, _A universal characterization of standard Borel spaces_. The Journal of Symbolic Logic, 88(2), 2023. ([arXiv](https://arxiv.org/abs/1908.10510))

* [[Tobias Fritz]] and Antonio Lorenzin, _Categories of abstract and noncommutative measurable spaces_, 2025. ([arXiv](https://arxiv.org/abs/2504.13708))
