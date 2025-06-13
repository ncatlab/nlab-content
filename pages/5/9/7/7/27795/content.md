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

As in ordinary [[Gelfand duality]] (as well as in [[algebraic geometry]] and related fields), one wants to study the properties of a class of [[spaces]] by means of the algebras of [[functions]] defined on them. 

In this case, the spaces we study are [[measurable spaces]], that is, [[sets]] equipped with a [[σ-algebra]]. [[bounded function|Bounded]] [[measurable functions]] on them form a particular algebraic structure (a commutative [[σ-C\*-algebra]]), and under some circumstances (in the [[fixed point of an adjunction|center of the adjunction]], see below) the spaces and these algebras determine one another.

### From measurable spaces to σ-C\*-algebras

Given a [[measurable space]] $X$, define by $\mathcal{L}^\infty(X)$ the set of [[bounded function|bounded]] [[measurable functions]] $h:X\to\mathbb{C}$. 
With its usual algebraic structure and norm, the set $\mathcal{L}^\infty$ forms a commutative [[C*-algebra]], and since it is closed under countable bounded monotone suprema, it is moreover a [[σ-C\*-algebra]].

Given a measurable function $f:X\to Y$, the precomposition $h\mapsto h\circ f$ is a homomorphism of σ-C\*-algebras
$f^*:\mathcal{L}^\infty(Y)\to \mathcal{L}^\infty(X)$. This gives a functor $Meas^{op}\to \sigma C^*Alg$.

### From σ-C\*-algebras to measurable spaces

Given a commutative σ-C\*-algebra $A$, define its **spectrum** $Sp(A)$ as the set of σ-C\*-homomorphisms $p:A\to\mathbb{C}$ (a.k.a. **points** of $A$). For every $h\in A$, define also the map 
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

The functors $\mathcal{L}^\infty:Meas^{op}\to \sigma C^*Alg$ and $Sp:\sigma C^*Alg^{op}\to Meas$ form a (contravariant) [[idempotent adjunction]]:

* The [[unit of an adjunction|unit]] has as components measurable functions $\eta:X\to Sp(\mathcal{L}^\infty(X))$ which map a point $x\in X$ to the [[Dirac delta]] functional 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
\mathcal{L}^\infty \ar{r}{\delta_x} & \mathbb{C} \\
h \ar[mapsto]{r} & h(x) .
\end{tikzcd}

* The [[counit]] has as components morphisms of $\sigma C^*Alg^{op}$ in the form $\epsilon^{op}:\mathcal{L}^\infty(Sp(A))\to A$, or equivalently, morphisms of $\sigma C^*Alg$ of the form $\epsilon:A\to \mathcal{L}^\infty(Sp(A))$, mapping $h\in A$ to the functional $\epsilon_h:Sp(A)\to\mathbb{C}$ defined above.

The adjunction induces an [[idempotent monad]] on $Meas$ (the [[zero-one measure#the_monad_of_zeroone_measures|monad of zero-one measures]]), and an idempotent monad on $\sigma C^*Alg$ as well (or equivalently, an idempotent [[comonad]] on $\sigma C*Alg^{op}$).

As usual with idempotent adjunctions, we have that the [[fixed point of an adjunction|center]] is equivalently given by 

* The full subcategory of $Meas$ whose objects are those spaces for which the unit $\eta:X\to Sp(\mathcal{L}^\infty(X))$ is an isomorphism. These are sometimes called [[sober measurable spaces]]. Analogously to [[sober topological spaces]], these are the spaces whose points are uniquely determined by the σ-algebra.
* The full subcategory of $\sigma C^*Alg$ whose objects are those σ-C\*-algebras for which the counit $\epsilon:A\to \mathcal{L}^\infty(Sp(A))$ is an isomorphism. These are sometimes called **spatial** or **concrete** σ-C\*-algebras.

Because of this, sometimes one calls the monad on $Meas$ the *sobrification monad*. It is the same monad as the one arising from [[Loomis-Sikorski duality]], see [below](#equivalence_with_loomissikorski_duality).



## Further results

### Equivalence with Loomis-Sikorski duality

In ordinary [[measure theory]], it is well known that the [[measurable subsets]] $A\subseteq X$ are "included" in the [[measurable functions]] via the [[indicator functions]] $1_A$. Those are exactly the measurable functions which take values only in $0$ and $1$. Conversely, from the σ-algebra one can recover exactly the measurable functions on $X$ (for example, by taking suprema of linear combinations of indicators). 

We can abstract this idea of "functions with values $0$ and $1$" as the [[projection]] elements of a C\*-algebra, that is, those elements $h\in A$ such that $h=h*$ (self-adjoint, generalizing real-valued) and $hh=h$ (idempotent). 
As one can show, the projection elements of a commutative σ-C\*algebra indeed form a [[σ-complete Boolean algebra]], the abstract analogue of a σ-algebra via the [[Loomis-Sikorski duality]]. Moreover, every σ-complete Boolean algebra can be shown as arising in this way. 

We therefore have an equivalence of categories between σ-C\*algebras and σ-complete Boolean algebras, commuting with the left and right-adjoints as in the following diagram.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=huge,%
column sep=tiny,%
]
\sigma\mathbf{C^*Alg} \ar[bend left=15]{dr}{\mathrm{Sp}} \ar[leftrightarrow]{rr}{\simeq} && \sigma\mathbf{Bool} \ar[bend left=15]{dl}{\mathrm{Sp}}[swap]{\perp} \\
& \mathbf{Meas}^\mathrm{op} \ar[bend left=15]{ul}{\mathcal{L}^\infty}[swap]{\perp} \ar[bend left=15]{ur}{\Sigma}
\end{tikzcd}

In other words, we have an isomorphism of adjunctions, and so, the two dualities (measurable Gelfand and [[Loomis-Sikorski duality|Loomis-Sikorski]]) can be seen as a [[Gelfand duality|Gelfand-type]] and a [[Stone duality|Stone-type]] description of one and the same duality.

More details in [FL'25, Section 4](#fritz_lorenzin).


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

* {#fritz_lorenzin} [[Tobias Fritz]] and Antonio Lorenzin, Categories of abstract and noncommutative measurable spaces, 2025. ([arXiv](https://arxiv.org/abs/2504.13708))

category: probability