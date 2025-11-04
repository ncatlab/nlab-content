
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

The [[category]] whose [[objects]] are [[measurable spaces]] and whose [[morphisms]] are [[stochastic kernels]] (or [[Markov kernels]]) is often denotes _Stoch_, or similar.

It is the motivating example of a [[Markov category]], and together with its subcategory [[Stoch#borelstoch|BorelStoch]], one of the most important categories of [[categorical probability]].

## Definition

_Stoch_ is the category whose 

* [[Objects]] are [[measurable spaces]], i.e. pairs $(X,\mathcal{A})$ where $X$ is a set and $\mathcal{A}$ is a [[sigma-algebra]] on $X$;
* [[Morphisms]] $(X,\mathcal{A})\to(Y,\mathcal{B})$ are [[Markov kernels]] of entries $k(B|x)$, for $x\in X$ and $B\in\mathcal{B}$;
* The [[identities]] $(X,\mathcal{A})\to(X,\mathcal{A})$ are given by the [[Dirac measure|Dirac delta]] kernels
$$
\delta(A|x) = 1_A(x) = \begin{cases}
1 & x\in A ; \\
0 & x\notin A ;
\end{cases}
$$
* The [[composition]] of kernels $k:(X,\mathcal{A})\to(Y,\mathcal{B})$ and $h:(Y,\mathcal{B})\to(Z,\mathcal{C})$ is given by the [[Lebesgue integral]]
$$
(h\circ k) (C|x) = \int_Y h(C|y)\,k(dy|x)
$$
for all $x\in X$ and $C\in\mathcal{C}$.
This is sometimes called _Chapman-Kolmogorov formula_. (Compare with the composition formula for [[stochastic matrices]].)


## Properties

### As a Kleisli category

_Stoch_ can be equivalently described as the [[Kleisli category]] of the [[Giry monad]] on [[Meas]].

It can also be described as the Kleisli category of the Giry monad restricted to the category $SoberMeas$ of [[sober measurable spaces]]. Indeed, 

* For every measurable space $X$, [[sober measurable space#examples|the space $P X$ is always sober]], and so the [[Giry monad]] restricts to [[sober measurable space|SoberMeas]];

* By [[zero-one measure#Siso|this proposition]], every measurable space is isomorphic to its [[sober measurable space#categorical_properties|sobrification]] in the category of [[zero-one kernels]] (and hence, in [[Stoch]] as well).

In other words, this triangle commutes up to natural isomorphism,
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
column sep=small,%
row sep=large,%
]
\mathrm{Meas} \ar{dr}[swap]{L_P} \ar{rr}{S} && \mathrm{SoberMeas} \ar{dl}{L_P} \\
& \mathrm{Stoch}
\end{tikzcd}
where $S$ denotes the [[sober measurable space#categorical_properties|sobrification]], and $L_P$ denotes the [[left adjoint]] of the Kleisli adjunction given by the [[Giry monad]] on [[Meas]], as well as its restriction to sober measurable spaces.


### As a Markov category

As a [[Markov category]], _Stoch_ is [[Markov category#positivity_and_causality|causal and hence positive]]. It does not have all conditionals, but its subcategory [BorelStoch](#borelstoch) does.

Its [[Markov category#deterministic_morphisms|deterministic morphisms]] are exactly the [[zero-one kernels]], forming the subcategory $Stoch_det$. 
Note that, outside of the [[sober measurable space|sober]] case, these are more general than measurable functions.

#### Representability

_Stoch_ is a [[Markov category#representable_markov_categories|representable Markov category]]: 

* First of all, as we saw [above](#as_a_kleisli_category), the [[Giry monad]] restricts to [[sober measurable space|SoberMeas]].

* Also, [[zero-one measure#kleisli_category|$Stoch_det$ is equivalent to $SoberMeas$]].
 
Consider now the following diagram,
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
column sep=small,%
row sep=large,%
]
\mathrm{Stoch}_\mathrm{det} \ar{rr}{\simeq} \ar[hook]{dr} && \mathrm{SoberMeas} \ar{dd}{P} \ar{dl}{L_P} \\
& \mathrm{Stoch} \ar{dl}[swap]{R'} \ar{dr}{R_P} \\
\mathrm{Stoch}_\mathrm{det} && \mathrm{SoberMeas} \ar{ll}{\simeq} 
\end{tikzcd}
where

* $P$ denotes the Giry monad on $SoberMeas$;
* $L_P$ and $R_P$ are the left and right adjoints of the [[Kleisli category|Kleisli adjunction]], making the triangle on the right commute;
* The [[zero-one measure#kleisli_category|equivalence $Stoch_det\to SoberMeas$]], on objects, maps a measurable space $X$ to its sobrification $S X$. Since $X$ is naturally isomorphic to $S X$ in $Stoch$ (see [above](#as_a_kleisli_category)), the upper triangle commutes up to natural isomorphism;
* The [[zero-one measure#kleisli_category|equivalence $SoberMeas\to Stoch_det$]] is the identity on objects, and on morphisms it canonically [[Markov kernel#kernels_from_deterministic_functions|induces a kernel from a function]]; 
* The functor $R':Stoch\to Stoch_det$ is exactly the one making the lower triangle commute. Explicitly it maps an object $X$ to the space $P X$, and a kernel $X\to Y$ to the kernel [[Markov kernel#kernels_from_deterministic_functions|induced by]] the Kleisli extension $P X \to P Y$.

By the considerations above, $R'$ is [[right adjoint]] to the inclusion functor $Stoch_det\hookrightarrow Stoch$, making $Stoch$ a [[Markov category#representable_markov_categories|representable Markov category]].  

Explicitly, the [[sampling map]] $samp:P X\to X$ is the usual measure-theoretic one:
$$
samp(A|p) \;=\; p(A) .
$$

The resulting [[monad]] on $SubStoch$, chasing the diagram above, can be seen as induced the Giry monad on $SoberMeas$ through the equivalence $SoberMeas \simeq Stoch_det$.

One should always keep in mind that the [[probability monad]] making Stoch representable is on [[zero-one kernel|$Stoch_det$]], or equivalently on [[sober measurable space|SoberMeas]], but not on [[Meas]], even though $Stoch$ is *also* the Kleisli category of the Giry monad on [[Meas]]. (The reason is that measurable functions are not the deterministic morphisms of $Stoch$, [[zero-one kernels]] are.)


### Particular limits and colimits

* The [[invariant sigma-algebra]] for every [[action]] via [[zero-one kernels]] (for example, [[Markov kernel#kernels_from_deterministic_functions|via deterministic functions]]) is a [[colimit]].

* For every [[action]] for which the [[ergodic decomposition theorem]] applies, the space of [[ergodic measures]] is a [[limit]]. 

* A notable special case of the condition above is [[de Finetti's theorem]], which says that the space of probability measures $P X$ ([[Giry monad]]) is a limit for the [[exchangeability|action of finite permutations]].

* Being a [[Kleisli category]], and since [[left adjoints preserve colimits]], every colimit [[Meas|of measurable spaces]] is also a colimit in _Stoch_.


## Notable subcategories

### BorelStoch

_BorelStoch_ is the [[full subcategory]] of _Stoch_ whose objects are [[standard Borel space|standard Borel]] measurable spaces. 
This is particularly important as a [[Markov category]] because it has [[Markov category#conditionals|conditionals]] and countable [[Markov category#kolmogorov_products|Kolmogorov products]].
It is the Kleisli category of the [[Giry monad]] restricted to [[standard Borel spaces]].

As proven [here](#markov_support), in _BorelStoch_ all [[idempotent splitting|idempotents split]], making it a [[Cauchy-complete category]].


### FinStoch

[[FinStoch]] is the [[full subcategory]] of _Stoch_ whose objects are discrete [[finite sets]]. Equivalently, it is the category of finite [[stochastic matrices]].
It is closely related to the Kleisli category of the [[distribution monad]].


## Related concepts

* [[stochastic process]]
* [[Markov category]]
* [[Markov kernel]]
* [[category of couplings]]
* [[probability monad]]
* [[Giry monad]]
* [[Kleisli category]]
* [[categorical probability]]


## References

* {#Lawvere62} [[Bill Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

* {#Chentsov65} N. N. Chentsov, _The categories of mathematical statistics_, Dokl. Akad. SSSR 164, 1965.

* {#panangaden_cat_markov} [[Prakash Panangaden]], _The category of Markov kernels_, ENTCS, 1999. ([full text](https://www.sciencedirect.com/science/article/pii/S1571066105806024))

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#markov_support} [[Tobias Fritz]], Tomáš Gonda, Antonio Lorenzin, [[Paolo Perrone]], Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))


category: category, probability

[[!redirects BorelStoch]]
[[!redirects category of kernels]]
[[!redirects category of Markov kernels]]