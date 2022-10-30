

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _compactly supported distribution_ is a [[distribution]] whose [[support of a distribution]] is a [[compact topological space|compact]] [[subset]].

This implies that compactly supported distributions may be evaluated not just on [[bump functions]], but in fact on the larger space of all [[smooth functions]]. Indeed it turns out that the compactly supported distributions exhaust the [[continuous linear functionals]] on the space of smooth functions ([H&#246;rmander 90, theorem 2.3.1](#Hoermander90)).

Therefore and since Schwartz's notation for the space $C^\infty(X)$ of all smooth functions on the given [[smooth manifold]] is $\mathcal{E}(X)$, the space of compactly supported distributions is often denoted by $\mathcal{E}'(X)$ ([H&#246;rmander 90, p. 45](#Hoermander90)).

## Definition

### A continuous linear duals to smooth functions


+-- {: .num_defn #TVSOfCompactlySupportedFunctions}
###### Definition
**([[topological vector space]] of [[smooth functions]] on a [[Cartesian space]])**

For $n \in \mathbb{R}^n$,  write $C^\infty(\mathbb{R}^n)$ for the $\mathbb{R}$-[[vector space]] of [[smooth functions]] $\mathbb{R}^n \to \mathbb{R}$.

Then the vector space $C^\infty(\mathbb{R}^n)$ becomes a [[Fréchet vector space]] induced by the family of [[seminorms]] 

$$
  \array{
    C^\infty_c(\mathbb{R}^n) 
     &\overset{p_{K}^\alpha}{\longrightarrow}&
    [0,\infty)
    \\
    \Phi &\mapsto& \underset{x \in K}{sup} {\vert \partial^\alpha \Phi(x) \vert}
  }
  \,,
$$

indexed by $K \subset \mathbb{R}^n$ a [[compact subset]] and $\alpha \in \mathbb{N}^n$ a [[tuple]] encoding the degrees of the [[partial derivative]] $\partial^\alpha$. 

Hence the seminorm $p_K^\alpha$ sends a [[bump function]] $\Phi$ to the [[supremum]] over the points $x \in K$ of the [[absolute value]] of the [[partial derivative]] $\partial^\alpha \Phi$; and the [[open subsets]] defined thereby are the [[unions]] of translations of the [[neighbourhood base|base]] [[open balls]]

$$
  B^\circ_{K,\alpha,\epsilon}(0)
  =
  \left\{
    v \in \mathbb{R}^n
    \;\vert\;
    p_K^\alpha(v)
    \lt
    \epsilon
  \right\}
$$

for $\epsilon \in (0,\infty)$.

We write

$$
  \mathcal{E}(\mathbb{R}^n) \in TopVect_{\mathbb{R}}
$$

for the resulting [[Fréchet space|Fréchet]] [[topological vector space]].

=--


+-- {: .num_defn #CompactlySupportedDistributionsAsContinuousLinearDualsToBumpFunctions}
###### Definition
**(compactly supported distibutions as continuous linear duals to bump functions)**

The space $\mathbb{E}'(\mathbb{R}^n)$ of _compactly supported distributions_ on $\mathbb{R}^n$ is the [[dual space]]

$$
  \mathcal{E}'(\mathbb{R}^n) \;\coloneqq\; \left(\mathcal{E}(\mathbb{R}^n)\right)^\ast
$$

to the [[topological vector space]] of [[bump functions]] from def. \ref{TVSOfCompactlySupportedFunctions}.


=--

e.g. ([Klainerman 08, p. 9](#Klainerman08))

This means the following

+-- {: .num_prop #CharacterizationOfContinuityBySeminormBounds}
###### Proposition
**(characterization of continuity for compactly supported distributions)**

A [[linear function]]

$$
  u \;\colon\; C^\infty(\mathbb{R}^n) \longrightarrow \mathbb{R}
$$

is [[continuous function|continuous]] with respect to the [[topological space|topology]] of def. \ref{TVSOfCompactlySupportedFunctions}, hence is a compactly supported distribution (def. \ref{CompactlySupportedDistributionsAsContinuousLinearDualsToBumpFunctions})

$$
  \mathcal{E}(\mathbb{R}^n) \longrightarrow \mathbb{R}
$$

precisely if the following condition holds

* there exists a compact subset $K \subset \mathbb{R}^n$ and $k \in \mathbb{N}$  and $C \in (0,\infty)$ such that

  $$
    \label{BoundBySumOfNormOfDerivatives}
    \underset{\Phi \in C^\infty(\mathbb{R}^n)}{\forall} 
    \left(
      \vert u(\Phi) \vert
      \;\leq\;
      C 
      \underset{ {\vert \alpha \vert \leq k} }{\sum} 
      \underset{x \in K}{sup} \vert \partial^\alpha K \vert
    \right)
  $$

=--

(see also [H&#246;rmander 90, (2.3.2) and theorem 2.3.1](#Hoermander90))

+-- {: .proof}
###### Proof

By [this prop.](locally+convex+topological+vector+space#AlternativeCharacterizationOfContinuityForLinearFunctionals) the continuity of $L$ is equivalent to there being an [[inhabited set|inhabited]] [[finite set]] $\{ (K_1, \alpha_1), \cdots, (K_r, \alpha_r) \}$ and $C \in (0,\infty)$ such that

$$
  \label{BoundByMaximumOfSeminormsOverFiniteSet}
  {\vert u(\Phi)\vert}
  \;\leq\;
  C
  \underset{i = 1, \cdots, n}{max} 
  \left(
    \underset{x \in K_i}{sup} {\vert \partial^{\alpha_i} \Phi \vert}  
  \right)
$$
 
We need to see that this is equivalent to a bound of the form (eq:BoundBySumOfNormOfDerivatives).

In one direction, assume that (eq:BoundByMaximumOfSeminormsOverFiniteSet) holds. 

The union $K \coloneqq \underset{i = 1, \cdots, n}{\cup} K_i$ is still a compact 
subset ([this prop.](compact+space#UnionsAndIntersectionOfCompactSubspaces)). Hence (eq:BoundByMaximumOfSeminormsOverFiniteSet) implies that


$$
  \begin{aligned}
    {\vert u(\Phi)\vert}
    & \leq
    C
    \underset{i = 1, \cdots, n}{max} 
    \underset{x \in K}{sup} 
    {\vert \partial^{\alpha_i} \Phi \vert}  
  \end{aligned}
$$

and hence with $k \coloneqq \underset{i = 1, \cdots, n}{max} {\vert \alpha_i\vert}$ that

$$
  {\vert u(\Phi)\vert}
  \;\leq\;
  C
    \underset{{\vert \alpha\vert}  \leq k}{\sum}
    \underset{x \in K}{sup} 
    {\vert \partial^{\alpha} \Phi \vert}  
  \,,
$$

which is of form (eq:BoundBySumOfNormOfDerivatives).

Conversely, assume that a bound of the form (eq:BoundBySumOfNormOfDerivatives) holds. Then take the finite set of pairs $(K_i, \alpha_i)$ where all $K_i \coloneqq K$ and with all ${\vert\alpha_i\vert} \leq k$. With $N$ denoting the number of $n$-tuples $\alpha$ with ${\vert \alpha \vert} \leq k$ we then get a bound as in (eq:BoundByMaximumOfSeminormsOverFiniteSet) with coefficient $N C$.

=--




### As smooth linear duals to smooth functions
 {#AsSmoothLinearDuals}

Given that [[distributions]] are concerned with _[[smooth functions]]_ it is sometimes more natural to regard them not as [[continuous linear functionals]] as in def. \ref{CompactlySupportedDistributionsAsContinuousLinearDualsToBumpFunctions}, but as _smooth linear functionals_. Indeed this turns out to be equivalent (prop. \ref{CompactlySupportedDistributionsAreTheSmoothLinearFunctionals} below), if one considers an ambient context of suitably [[generalized smooth spaces]], namely [[diffeological spaces]] or more generally [[smooth sets]] or [[formal smooth sets]]. We will write $\mathbf{H}$ for any of these [[categories]] of [[generalized smooth spaces]].

We may canonially regard any [[smooth manifold]] such as the [[Cartesian space]] $\mathbb{R}^n$ as an object of $\mathbf{H}$. For $X \in \mathbf{H}$ any object, we write $[X,\mathbb{R}]$ for the [[mapping space]] (the [[internal hom]]). The underlying set is $C^\infty(X)$. If $X$ itself has $\mathbb{R}$-linear structure, we write 

$$
  [X,\mathbb{R}]_{\mathbb{R}}
  \hookrightarrow
  [[X,\mathbb{R}], \mathbb{R}]
$$

for the [[subobject]] of $\mathbb{R}$-linear maps. 

Concretely, for $U$ a [[smooth manifold]] (or just a [[Cartesian space]]), then the [[sheaf]] $[X,\mathbb{R}]$ assigns (see at _[[closed monoidal structure on presheaves]]_ for details)

$$
  [X,\mathbb{R}](U) = C^\infty(U \times X)
$$

and $[X,\mathbb{R}](U) \subset C^\infty(U \times X)$ is the subset of those functions $\Phi_{(-)}(-)$ such that for all $u \in U$ the function $\Phi_u \colon X \to \mathbb{R}$ is $\mathbb{R}$-linear. The [[global elements]] $\Gamma(-)$ of the [[mapping space]] constitute the ordinary [[hom set]]

$$
  \Gamma [X,\mathbb{R}] \simeq \mathbf{H}(X,\mathbb{R})
  \,.
$$

+-- {: .num_prop #CompactlySupportedDistributionsAreTheSmoothLinearFunctionals}
###### Proposition
**([[compactly supported distributions are the smooth linear functionals]])**

For $n \in \mathbb{N}$, there is a [[natural bijection]] between the underlying sets of compactly supported distributions on $\mathbb{R}^n$ (def. \ref{CompactlySupportedDistributionsAsContinuousLinearDualsToBumpFunctions}) and the $\mathbb{R}$-linear [[mapping space]] formed in the [[category]] $\mathbf{H}$ of either [[diffeological space]] or [[smooth sets]] or [[formal smooth sets]]:

$$
  \widetilde{(-)}
  \;\colon\;
  \mathcal{E}'(\mathbb{R}^n)
    \overset{\simeq}{\longrightarrow}
  \mathbf{H}([\mathbb{R}^n, \mathbb{R}], \mathbb{R})_{\mathbb{R}}
$$

given by sending $\mu \in \mathcal{E}'(\mathbb{R}^n)$ to the [[natural transformation]] which on a test space $U \in $ [[CartSp]] takes a smoothly $U$-parameterized function $\Phi_{(-)}(-) \colon U \times \mathbb{R}^n \to \mathbb{R}$ to its evaluation in $\mu$ pointwise in $U$:

$$
  \tilde \mu(\Phi_{(-)})(u)
  \;\coloneqq\;
  \langle \mu, \Phi_{u}\rangle
  \,.
$$

=--

([Moerdijk-Reyes 91, chapter II, prop. 3.6](#MoerdijkReyes91))


+-- {: .proof}
###### Proof

First consider this for the case that $\mathbf{H} = $ [[SmoothSet]] (which immediately subsumes the case that $\mathbf{H} =$ [[diffeological space|DiffelogicaSpace]]).

To see that $\widetilde{(-)}$ is well defined, we need to check that the function

$$
  \array{
     U 
     &\overset{
     \tilde \mu(\Phi_{(-)})}{\longrightarrow}&
     \mathbb{R}
     \\
     u &\mapsto& \langle \mu, \Phi_u\rangle
  }
$$

is [[smooth function|smooth]]. But this follows immediately since $\langle \mu,-\rangle$ by definition is [[linear function|linear]] and [[continuous function|continuous]].


To see that $\widetilde{(-)}$ is indeed a [[bijection]] for each $U$ it remains that every $\mathbb{R}$-linear smooth functional (morphisms of [[smooth sets]]) of the form

$$
  A \;\colon\; [\mathbb{R}^n,\mathbb{R}] \longrightarrow \mathbb{R}
$$

when restricted on [[global elements]] to a [[function]] of sets

$$
  A(\ast) \;\colon\; C^\infty(\mathbb{R}^n) \longrightarrow \mathbb{R}
$$

is [[continuous function|continuous]] with respect to the [[topological vector space]] structure from def. \ref{TVSOfCompactlySupportedFunctions} on the left.

Now by definition of the [[internal hom]] $A$ is actually "path-smooth" ([this def.](Frechet+space#PathSmoothFunction)) and hence the statement is implied by [this prop](Frechet+space#PathSmoothLinearFunctionsOnFrechetSpaceAreContinuous).

Finally to see that this argument generalizes to $\mathbf{H} = $ [[formal smooth set|FormalSmoothSet]] observe that the [[Weil algebra]] of every [[infinitesimally thickened point]] is a [[quotient ring]] of an algebra of smooth functions on some [[Cartesian space]] (by the [[Hadamard lemma]]). The previous argument now applies to representatives under this quotient coprojection and one checks that it is independent of the representative chosen.

=--

## Properties

### Wave front set


+-- {: .num_prop #EmptyWaveFrontSetCorrespondsToOrdinaryFunction}
###### Proposition
**([[empty set|empty]] [[wave front set]] corresponds to ordinary [[smooth functions]])**

The [[wave front set]] of a compactly supported distribution is [[empty set|empty]] precisely if the distribution comes from an ordinary [[smooth function]] (hence a [[bump function]]). 

=--

e.g. ([H&#246;rmander 90, below (8.1.1)](#Hoermander90))



## Examples

* [[microcausal functional]]

## Related concepts

* [[compactly supported continuous function]]

* [[bump function]]



## References

### Traditional

Textbook accounts include

* {#Hoermander90} [[Lars Hörmander]], section 2.3 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

Lecture notes include

* {#Klainerman08} [[Sergiu Klainerman]], _Analysis_ 2008 ([pdf](https://web.math.princeton.edu/~seri/homepage/courses/Analysis2008.pdf))


### In terms of smooth toposes

Discussion of compactly supported distributions in terms morphisms out of [[internal homs]] in a [[smooth topos]] is in

* {#MoerdijkReyes91} [[Ieke Moerdijk]], [[Gonzalo Reyes]], around prop. 3.6 in chapter II of _[[Models for Smooth Infinitesimal Analysis]]_, Springer 1991

and specifically for the [[Cahiers topos]] of [[formal smooth sets]] in

* {#KockReyes03} [[Anders Kock]], [[Gonzalo Reyes]], _Some calculus with extensive quantities: wave equation_, Theory and Applications of Categories , Vol. 11, 2003, No. 14, pp 321-336 ([TAC](http://www.tac.mta.ca/tac/volumes/11/14/11-14abs.html))

* {#Kock11} [[Anders Kock]], _Commutative monads as a theory of distributions_ ([arxiv:1108.5952](http://arxiv.org/abs/1108.5952)) 

using results of

* {#FroelicherKriegl88} [[Alfred Frölicher]], [[Andreas Kriegl]], section 5 of  _Linear spaces and differentiation theory_, Wiley 1988 ([pdf](http://www.fuw.edu.pl/~kostecki/scans/froelicherkriegl1988.pdf))

and following the general conception of "[[intensive and extensive]]" in 

* {#Lawvere86} [[William Lawvere]], Introduction to _[[Categories in Continuum Physics]], Lectures given at a Workshop held at SUNY, Buffalo 1982. Lecture Notes in Mathematics 1174. 1986

Generalization to non-compactly supported distributions is in

* {#KockReyes04} [[Anders Kock]], [[Gonzalo Reyes]], _Categorical distribution theory; heat equation_ ([arXiv:math/0407242](https://arxiv.org/abs/math/0407242))

and [[sheaf theory|sheaf theoretic]] discussion of distributions as morphisms of [[smooth spaces]] is in 

* {#Paugam12} [[Frédéric Paugam]], section 3.2 of _Towards the mathematics of quantum field theory_, 2012 ([pdf](https://webusers.imj-prg.fr/~frederic.paugam/documents/enseignement/master-mathematical-physics.pdf)) 







[[!redirects compactly supported distributions]]
