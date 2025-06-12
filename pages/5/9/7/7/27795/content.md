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

The [[adjunction]] known as *measurable Gelfand duality* is a [[Gelfand duality|Gelfand-type duality]] between [[measurable spaces]] and particular ([[σ-complete C*-algebra|σ-complete]]) [[C*-algebras]]. It is an algebraic approach to [[point-free measure theory]].

It is closely related to the usual [[Gelfand duality]], as well as to [[Loomis-Sikorski duality]], which can be considered its [[Stone duality|Stone-type]] counterpart.


## Main concepts

(...)

### From measurable spaces to σ-C\*-algebras

Given a [[measurable space]] $X$, define by $\mathcal{L}^\infty(X)$ the set of bounded measurable functions $h:X\to\mathbb{C}$. 
With its usual algebraic structure and norm, the set $\mathcal{L}^\infty$ forms a [[C*-algebra]], and since it is closed under countable monotone suprema, it is moreover a [[σ-C\*-algebra]].

Given a measurable function $f:X\to Y$, the precomposition $h\mapsto h\circ f$ is a homomorphism of σ-C\*-algebras
$f^*:\mathcal{L}^\infty(Y)\to \mathcal{L}^\infty(X)$. This gives a functor $Meas^{op}\to \sigma C^*Alg$.

### From σ-C\*-algebras to measurable spaces

Given a σ-C\*-algebra $A$, define its **spectrum** $Sp(A)$ as the set of σ-C\*-homomorphisms $p:A\to\mathbb{C}$ (a.k.a. **points** of $A$). For every $h\in A$, define also the map 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
\mathrm{Sp}(A) \ar{r}{\epsilon_h} & \mathbb{C} \\
p \ar[mapsto]{r} & p(h) .
\end{tikzcd}
We equip $Sp(A)$ with the coarsest σ-algebra making the maps $\epsilon_h$ measurable for all $h\in A$ (cf. the σ-algebra of the [[Giry monad]]). 

Given a σ-C\*-homomorphism $\phi:A\to B$, precomposition $p\mapsto p\circ\phi$ gives a function $\phi^*:Sp(B)\to Sp(A)$, which is measurable for the σ-algebras defined above. We therefore have a functor $Sp:\sigma C^*Alg^\op\to Meas$.


### The adjunction

(...)

## Further results

### Equivalence with Loomis-Sikorski duality

(...)

### Stochastic version

(...)


## See also

* [[point-free measure theory]], [[Loomis-Sikorski duality]]
* [[monotone-complete C\*-algebra]], [[σ-complete Boolean algebra]]
* [[Gelfand duality]], [[point-free topology]]
* [[zero-one measure]], [[zero-one kernel]], [[Markov kernel]], [[Stoch]]
* [[Markov category]], [[probability monad]]


## References

* Kazuyuki Saitô and J. D. Maitland Wright,_Monotone Complete C\*-algebras and Generic Dynamics_, Springer, 2015.

* Gert K. Pedersen. _C\*-algebras and their automorphism groups_, Academic Press, 2018.

* [[Tobias Fritz]] and Antonio Lorenzin, Categories of abstract and noncommutative measurable spaces, 2025. ([arXiv](https://arxiv.org/abs/2504.13708))

category: probability