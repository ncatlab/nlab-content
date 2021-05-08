
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Entropy
* table of contents
{: toc}

## Idea

Entropy is a measure of disorder, given by the amount of [[information]] necessary to precisely specify the [[state]] of a system.

Entropy is important in [[information theory]] and [[statistical physics]].


## Mathematical definitions

We can give a precise [[mathematics|mathematical]] definition of the entropy in [[probability theory]].


### Preliminary definitions

We will want a couple of preliminary definitions.  Fix a [[probability space]] $(X,\mu)$; that is, $X$ is a [[set]], and $\mu$ is a [[probability measure]] on $X$.


#### Surprisal

If $A$ is a [[measurable subset]] of $X$, then the __surprisal__ or __self-[[information]]__ of $A$ (with respect to $\mu$) is
$$ \sigma_\mu(A) \coloneqq -\log \mu(A) .$$
Notice that, despite the minus sign in this formula, $\sigma$ is a nonnegative function (since $\log p \leq 0$ for $p \leq 1$); more precisely, $\sigma$ takes values in $[0,\infty]$.  The term 'surprisal' is intended to suggest how surprised one ought to be upon learning that the event modelled by $A$ is true: from no surprise for an event with probability $1$ to infinite surprise for an event with probability $0$.

The __expected surprisal__ of $A$ is then
$$ h_\mu(A) \coloneqq \mu(A) \sigma_\mu(A) = -\mu(A) \log \mu(A) = -\log(\mu(A)^{\mu(A)}) $$
(with $h_\mu(A) = 0$ when $\mu(A) = 0$).  Like $\sigma$, $h$ is a nonnegative function; it is also important that $h_\mu$ is [[convex function|concave]].  Both $h_\mu(\nothing)$ and $h_\mu(X)$ are $0$, but for different reasons; $h_\mu(A) = 0$ when $\mu(A) = 1$ because, upon observing an event with probability $1$, one gains no information; while $h_\mu(A) = 0$ when $\mu(A) = 0$ because one expects never to observe an event with probability $0$.  The maximum possible value of $h$ is $\mathrm{e}^{-1} \log \,\mathrm{e}$ (so $\mathrm{e}^{-1}$ if we use [[natural logarithms]]), which occurs when $\mu(A) = \mathrm{e}^{-1}$.

We have not specified the base of the [[logarithm]], which amounts to a constant factor (proportional to the logarithm of the base), which we think of as specifying the [[unit of measurement]] of entropy.  Common choices for the base are $2$ (whose unit is the [[bit]], originally a unit of memory in computer science), $256$ (for the byte, which is $8$ bits), $3$ (for the trit), $\mathrm{e}$ (for the nat or neper), $10$ (for the bel, originally a unit of relative power intensity in telegraphy, or ban, dit, or hartley), and $\root{10}{10}$ (for the decibel, $1/10$ of a bel).  In applications to [[statistical physics]], common bases are exactly (since 2019) 
$$
\mathrm{e}^{10^{29}/1\,380\,649} \approx 10^{3.145\,582\,127\,704\,085\,743 \times 10^{22}} \qquad \text{(for the joule per kelvin)},
$$ 
or
$$
\mathrm{e}^{104\,600\,000\,000\,000/207\,861\,565\,453\,831} \approx 1.654\,037\,938\,063\,167\,336 \qquad \text{(for the calorie per mole-kelvin)},
$$
and so on; although $\mathrm{e}$ is common in theoretical work (and then the unit of measurement is said to be [[Boltzmann's constant]] rather than the nat or neper).


#### Almost partitions

Recall that a __[[partition]]__ of a set $X$ is a [[family of subsets|family]] $\mathcal{P}$ of subsets of $X$ (the _parts_ of the partition) such that $X$ is the [[union]] of the parts and any two distinct parts are [[disjoint sets|disjoint]] (or better, for [[constructive mathematics]], two parts are equal if their intersection is [[inhabited subset|inhabited]]).

When $X$ is a probability space, we may relax both conditions: for the union of $\mathcal{P}$, we require only that it be a [[full set]]; for the intersections of pairs of elements of $\mathcal{P}$, we require only that they be [[null sets]] (or better, for constructive mathematics, that $A = B$ when $\mu^*(A \cap B) \gt 0$, where $\mu^*$ is the [[outer measure]] corresponding to $\mu$).

For definiteness, call such a collection of subsets a __$\mu$-almost partition__; a $\mu$-almost partition is _measurable_ if each of its part is measurable (in which case we can use $\mu$ instead of $\mu^*$).


### Entropy of a $\sigma$-algebra on a probability space

This is a general mathematical definition of entropy.

Given a probability [[measure space]] $(X,\mu)$ and a $\sigma$-[[sigma-algebra|algebra]] $\mathcal{M}$ of [[measurable sets]] in $X$, the __entropy__ of $\mathcal{M}$ with respect to $\mu$ is
\[ \label{general} H_\mu(\mathcal{M}) \coloneqq \sup \{ \sum_{A \in \mathcal{F}} h_\mu(A) \;|\; \mathcal{F} \subseteq \mathcal{M},\; {|\mathcal{F}|} \lt \aleph_0,\; X = \biguplus \mathcal{F} \} .\]

In words, the entropy is the [[supremum]], over all ways of expressing $X$ as an internal [[disjoint union]] of [[finite set|finitely many]] elements of the $\sigma$-algebra $\mathcal{M}$, of the sum, over these measurable sets, of the expected surprisals of these sets.  This supremum can also be expressed as a [[convergence|limit]] as we take $\mathcal{F}$ to be finer and finer, since $h_\mu$ is concave and the partitions are [[directed set|directed]].

We have written this so that $\mathcal{F}$ is a finite partition of $X$; without loss of generality, we may require only that $\mathcal{F}$ be a $\mu$-almost partition.  In [[constructive mathematics]], it seems that we *must* use this weakened condition, at least the part that allows $\bigcup \mathcal{F}$ to merely be full.

This definition is very general, and it is instructive to look at special cases.


### Entropy of a probability space

Given a probability space $(X,\mu)$, the __entropy__ of this probability space is the entropy, with respect to $\mu$, of the $\sigma$-algebra of *all* measurable subsets of $X$.


### Entropy of a partition of a probability space

Every measurable almost-partition of a measure space (indeed, any family of measurable subsets) generates a $\sigma$-algebra.  The __entropy__ of a measurable almost-partition $\mathcal{P}$ of a probability measure space $(X,\mu)$ is the entropy, with respect to $\mu$, of the $\sigma$-algebra generated by $\mathcal{P}$.  The formula (eq:general) may then be written
\[ \label{partition} H_\mu(\mathcal{P}) = \sum_{A \in \mathcal{P}} h_\mu(A) = -\sum_{A \in \mathcal{P}} \log(\mu(A)^{\mu(A)}) ,\]
since an infinite sum (of nonnegative terms) may also be defined as a supremum.  (Actually, the supremum in the infinite sum does not quite match the supremum in (eq:general), so there is a bit of a theorem to prove here.)

In most of the following special cases, we will consider only partitions, although it would be possible also to consider more general $\sigma$-algebras.


### Entropy of (a partition of) a discrete probability space

Recall that a __discrete probability space__ is a [[set]] $X$ equipped with a function $\mu\colon X \to ]0,1]$ such that $\sum_{i \in X} \mu(i) = 1$; since $\mu(i) \gt 0$ is possible for only countably many $i$, $X$ must be [[countable set|countable]].  We make $X$ into a measure space (with every subset measurable) by defining $\mu(A) \coloneqq \sum_{i \in A} \mu(i)$.  Since every inhabited set has positive measure, every almost-partition of $X$ is a partition; since every set is measurable, any partition is measurable.

Given a discrete probability space $(X,\mu)$ and a partition $\mathcal{P}$ of $X$, the __entropy__ of $\mathcal{P}$ with respect to $\mu$ is defined to be the entropy of $\mathcal{P}$ with respect to the probability measure induced by $\mu$.  Simplifying (eq:partition), we find
$$ H_\mu(\mathcal{P}) = -\sum_{A \in \mathcal{P}} \log((\sum_{i \in A} \mu(i))^{\sum_{i \in A} \mu(i)}) .$$

More specially, the __entropy__ of the discrete probability space $(X,\mu)$ is the entropy of the partition of $X$ into [[singletons]]; we find
$$ H_\mu(X) = \sum_{i \in X} h_\mu(i) = -\sum_{i \in X} \log(\mu(i)^{\mu(i)}) .$$
This is actually a special case of the entropy of a probability space, since the $\sigma$-algebra generated by the singletons is the power set of $X$.

Yet more specially, the __entropy__ of a [[finite set]] $X$ is the entropy of $X$ equipped with the uniform discrete probability measure; we find
\[ \label{Boltzmann} H_{unif}(X) = -\sum_{i \in X} \log((\frac{1}{|X|})^{\frac{1}{|X|}}) = \log {|X|} ,\]
which is probably the best known mathematical formula for entropy, due to [[Max Planck]], who attributed it to [[Ludwig Boltzmann]].  (Its [physical interpretation](#physical) appears below.)

Of all probability measures on $X$, the uniform measure has the [[maximum entropy]].


### Entropy with respect to an absolutely continuous probability measure on the real line

Recall that a [[Borel measure]] $\mu$ on an [[interval]] $X$ in the [[real line]] is __[[absolutely continuous measure|absolutely continuous]]__ if $\mu(A) = 0$ whenever $A$ is a [[null set]] (with respect to [[Lebesgue measure]]), or better such that $\mu(A) \gt 0$ whenever the Lebesgue measure of $A$ is positive.  In this case, we can take the [[Radon–Nikodym derivative]] of $\mu$ with respect to Lebesgue measure, to get an [[integrable function]] $f$, called the __probability distribution function__; we recover $\mu$ by
\[ \label{pdf} \mu(A) = \int_A f(x) \mathrm{d}x ,\]
where the integral is taken with respect to Lebesgue measure.

If $\mathcal{P}$ is a partition (or a Lebesgue-almost-partition) of an interval $X$ into [[Borel sets]], then the __entropy__ of $\mathcal{P}$ with respect to an integrable function $f$ is the entropy of $\mathcal{P}$ with respect to the measure induced by $f$ using the integral formula (eq:pdf); we find
$$ H_f(\mathcal{P}) = -\sum_{A \in \mathcal{P}} \log((\int_A f(x) \mathrm{d}x)^{\int_A f(x) \mathrm{d}x}) .$$

On the other hand, the __entropy__ of the probability distribution space $(X,f)$ is the entropy of the entire $\sigma$-algebra of all Borel sets (which is *not* generated by a partition) with respect to $f$; we find
$$ H_f(X) = -\int_{x \in X} \log(f(x)^{f(x)}) \mathrm{d}x $$
by a fairly complicated argument.
+-- {: .query}
I haven\'t actually managed to check this argument yet, although my memory tags it as a true fact.  &#8212;Toby
=--


### Entropy of a density matrix

In the analogy between [[classical physics]] and [[quantum physics]], we move from probability distributions on a [[phase space]] to [[density operators]] on a [[Hilbert space]].

So just as the entropy of a probability distribution $f$ is given by $- \int f \log f$, so the __entropy__ of a density operator $\rho$ is
$$ H_\rho \coloneqq -Tr (\rho \log \rho) ,$$
using the [[functional calculus]].

These are both special cases of the entropy of a [[state]] on a $C^*$-[[C-star-algebra|algebra]].

There is a way to fit this into the framework given by (eq:general), but I don\'t remember it (and never really understood it).


### Relative entropy
 {#RelativeEntropy}

For two finite probability distributions $p$ and $q$, their **relative entropy** is 

$$
  S(p/q) \coloneqq \sum_{k = 1}^n p_k(log p_k - log q_k)
  \,.
$$

Or alternatively, for $\rho, \phi$ two [[density matrix|density matrices]], their relative entropy is 

$$
  S(\rho/\phi) \coloneqq tr \rho(log \rho - log \phi)
  \,.
$$

There is a generalization of these definitions to [[state]]s on general [[von Neumann algebra]]s, due to ([Araki](#Araki)).

For more on this see _[[relative entropy]]_.


## Physical entropy {#physical}

As hinted above, any probability distribution on a [[phase space]] in [[classical physics]] has an entropy, and any [[density matrix]] on a [[Hilbert space]] in [[quantum physics]] has an entropy.  However, these are __microscopic entropy__, which is not the usual entropy in [[thermodynamics]] and most other branches of [[physics]].  (In particular, microscopic entropy is conserved, rather than increasing with time.)

Instead, physicists use *coarse-grained* entropy, which corresponds mathematically to taking the entropy of a $\sigma$-algebra much smaller than the $\sigma$-algebra of all measurable sets.  Given a classical system with $N$ microscopic degrees of freedom, we identify $n$ macroscopic degrees of freedom that we can reasonably expect to measure, giving a map from $\mathbb{R}^N$ to $\mathbb{R}^n$ (or more generally, a map from an $N$-dimensional microscopic phase space to an $n$-dimensional macroscopic phase space). Then the $\sigma$-algebra of all measurable sets in $\mathbb{R}^n$ [[pullback|pulls back]] to a $\sigma$-algebra on $\mathbb{R}^N$, and the __macroscopic entropy__ of a statistical state is the [[conditional entropy]] of this $\sigma$-algebra.  (Typically, $N$ is on the order of [[Avogadro's number]], while $n$ is rarely more than half a dozen, and often as small as $2$.)

If we specify a state by a point in $\mathbb{R}^n$, a macroscopic pure state, and assume a uniform probability distribution on its [[fibre]] in $\mathbb{R}^N$, then this results in the [[maximum entropy]].  If this fibre were a finite set, then we would recover Boltzmann\'s formula (eq:Boltzmann).  This is never exactly true in classical statistical physics, but it is often nevertheless a very good approximation.  (Boltzmann\'s formula actually makes better physical sense in quantum statistical physics, even though Boltzmann himself did not live to see this.)

A more sophisticated approach (pioneered by [[Josiah Gibbs]]) is to consider all possible mixed microstates (that is all possible probability distributions on the space $\mathbb{R}^N$ of pure microstates) whose [[expectation values]] of total energy and other [[extensive quantities]] (among those that are functions of the macrostate) match the given pure macrostate (point in $\mathbb{R}^n$).  We pick the mixed microstate with the [[maximum entropy]].  If this is a [[thermal state]], then we say that the macrostate has a [[temperature]], but it has an entropy in any case.


### Gravitational entropy

* gravitational entropy

  * [[Bekenstein-Hawking entropy]]

  * [[generalized second law of thermodynamics]]


## Related concepts

* [[Renyi entropy]]

* [[min-entropy]]

* [[relative entropy]]

* [[entanglement entropy]], [[holographic entanglement entropy]]

* [[entropic force]]

* [[dissipative system]]


## References
{#References}


### General
 {#ReferencesGeneral}

The concept of entropy was introduced, by [[Rudolf Clausius]] in 1865, in the context of [[physics]], and then adapted to [[information theory]] by [[Claude Shannon]] in 1948, to [[quantum mechanics]] by [[John von Neumann]] in 1955, to [[ergodic theory]] by [[Andrey Kolmogorov]] and Sinai in 1958, and to [[topological dynamics]] by Adler, Konheim and McAndrew in 1965.

Survey with an eye towards [[black hole entropy]]:

* [[Ted Jacobson]], _Entropy from Carnot to Bekenstein_ ([arXiv:1810.07839](https://arxiv.org/abs/1810.07839))



### In quantum probability theory
 {#ReferencesInQuantumProbabilityTheory}

Discussion of entropy in [[quantum probability theory]], hence for [[quantum states]] understood as positive linear functionals on the [[star-algebra]] [[algebra of observables|of observables]] ([[operator algebra|operator algebraic]] [[state on a star-algebra|states on star-algebras]]) and with their [[density matrices]] defined via the [[GNS construction]]:

Introduction and survey:

* [[A. P. Balachandran]], T. R. Govindarajan, Amilcar R. de Queiroz, A. F. Reyes-Lega, _Algebraic approach to entanglement and entropy_, Phys. Rev. A 88, 022301 (2013) ([arXiv:1301.1300](http://arxiv.org/abs/1301.1300))

* [[A. P. Balachandran]], A. R. de Queiroz, S. Vaidya, *Entropy of Quantum States: Ambiguities*, Eur. Phys. J. Plus 128, 112 (2013) ([arXiv:1212.1239](https://arxiv.org/abs/1212.1239), [doi:10.1140/epjp/i2013-13112-3](https://doi.org/10.1140/epjp/i2013-13112-3))


* Paolo Facchi, Giovanni Gramegna, Arturo Konderak, *Entropy of quantum states* ([arXiv:2104.12611](https://arxiv.org/abs/2104.12611))

* Erling St&#248;rmer, _Entropy in operator algebras_ ([pdf](http://www.researchgate.net/profile/Erling_Stormer/publication/228832297_Entropy_in_operator_algebras/links/02bfe50ed5ccabaf69000000.pdf?origin=publication_detail))


[Relative entropy](#RelativeEntropy) of [[states]] on  [[von Neumann algebras]] was introduced in 

* {#Araki} [[Huzihiro Araki]], _Relative Entropy of States of von Neumann Algebras_ ([pdf](http://www.google.de/url?sa=t&source=web&cd=5&ved=0CEsQFjAE&url=http%3A%2F%2Fwww.ems-ph.org%2Fjournals%2Fshow_pdf.php%3Fissn%3D0034-5318%26vol%3D11%26iss%3D3%26rank%3D9&rct=j&q=entropy%20cocycle%20von%20Neumann%20algebra&ei=n3jrTYyxOI-c-waJvMnPDw&usg=AFQjCNGuJgVUE7CtGPmb2PZLhOOWt1_JPQ&cad=rja))
 

A large collection of references on quantum entropy is in 

* [[Christopher Fuchs]], _References for research in quantum distinguishability and state disturbance_ ([pdf](http://www.perimeterinstitute.ca/personal/cfuchs/BigRef.pdf))

### Category theoretic and cohomological interpretations

A discussion of entropy with an eye towards the [[presheaf topos]] over the [[site]] of finite [[measure spaces]] is in 

* [[Mikhail Gromov]], _In a search for a structure, Part I: On entropy_ (2012) ([pdf](https://www.ihes.fr/~gromov/wp-content/uploads/2018/08/structre-serch-entropy-july5-2012.pdf))

* [[William Lawvere]], _State categories, closed categories, and the existence_ (subtitle: Semi-continuous entropy functions), IMA reprint 86, [pdf](https://www.ima.umn.edu/State-Categories-Closed-Categories-and-Existence-Semi-Continuous-Entropy-Functions)

(Co)homological viewpoint is discussed in

* P. Baudot, D. Bennequin, _The homological nature of entropy_, Entropy, 17(5):3253--3318, 2015 [doi](https://doi.org/10.3390/e17053253) (open access)

(for an update see also the abstract of a Baudot's talk [here](https://calendar.math.cas.cz/content/information-cohomology-and-topological-information-data-analysis))

### Axiomatic characterizations
 {#ReferencesAxiomaticCharacterization}

After the concept of entropy proved enormously useful in practice, many people have tried to find a more abstract foundation for the concept (and its variants) by characterizing it as the unique measure satisfying some list of plausible-sounding axioms.

A characterization of [relative entropy](#RelativeEntropy) on finite-[[dimension|dimensional]] [[C-star algebras]] is given in 

* {#Petz92} D. Petz, _Characterization of the relative entropy of states of matrix algebras_, Acta Math. Hung. 59 (3-4) (1992) ([pdf](http://www.renyi.hu/~petz/pdf/52.pdf))
 

A simple characterization of von Neumann entropy of [[density matrices]] (mixed [[quantum states]]) is discussed in 

* Bernhard Baumgartner, _Characterizing Entropy in Statistical Physics and in Quantum Information Theory_, [arXiv:1206.5727](http://arxiv.org/abs/1206.5727)

Entropy-like quantities appear in the study of many PDEs, with entropy estimates. For an intro see

* L. C. Evans, _A survey of entropy methods for partial differential equations_, [pdf](http://math.berkeley.edu/~evans/ams.entropy.pdf); (and longer course text:) _Entropy and partial differential equations_, [pdf](http://math.berkeley.edu/~evans/entropy.and.PDE.pdf)


[[!redirects entropy]]
[[!redirects entropies]]
