
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[topological space]] $(X,\tau)$ is called a _Kolmogorov space_ if it satisfies the $T_0$-[[separation axiom]], hence if for $x_1 \neq x_2 \in X$ any two distinct points, then at least one of them has an [[open neighbourhood]] $U_{x_i} \in \tau$ which does not contain the other point. This is equivalent to its [[contrapositive]]: for all points $x_1, x_2 \in X$, if every [[open neighbourhood]] $U_{x_i} \in \tau$ which contains one of the points also contains the other point, then the two points are equal $x_1 = x_2$. 

[[!include main separation axioms -- table]]

### In dependent type theory

In [[dependent type theory]], given a type $X$, the type of [[subtypes]] of $X$ is the [[function type]] $X \to \Omega$, where $\Omega$ is the [[type of all propositions]] with the type reflector type family $P:\Omega \vdash \mathrm{El}_\Omega(P) \; \mathrm{type}$. 

Given a [[type universe]] $\mathrm{Type}$, a [[topological space]] is a type $X$ with a type of subtypes $O(X)$ with canonical [[embedding]] $i_O:O(X) \hookrightarrow (X \to \Omega)$, called the open sets of $X$, which are closed under finite intersections and $\mathrm{Type}$-[[small type|small]] unions. 

Given a topological space $(X, O(X))$, we define the [[relation]] 

$$x:X, U:O(X) \vdash x \in U \; \mathrm{type}$$ 

by 

$$x \in U \coloneqq \mathrm{El}_\Omega((i_O(U))(x))$$

By definition of the type of all propositions and its type reflector, $x \in U$ is always a [[h-proposition]] for all $x:X$ and $U:O(X)$, and the type family is a [[binary relation]]. 

The [[specialization order]] is given by the type 

$$x \leq y \coloneqq \prod_{U:O(X)} (x \in U) \to (y \in U)$$

and because $x \in U$ is a [[binary relation]], the above type is a [[preorder]], with elements

$$\mathrm{refl}_{SpecOrd}(x):\prod_{U:O(X)} (x \in U) \to (x \in U)$$

for all elements $x:X$. (See [[preorder]] for a proof that $\prod_{z:B} R(x, z) \to R(y, z)$ is a preorder for any binary relation $x:A, z:B \vdash R(x, z)$.) 

There is a canonical family of functions for every topological space

$$x:X, y:X \vdash \mathrm{idToSpecOrd}(x, y):(x =_X y) \to \left(\prod_{U:O(X)} (x \in U) \to (y \in U)\right) \times \left(\prod_{U:O(X)} (y \in U) \to (x \in U)\right)$$

[[inductively defined]] on reflexivity of the [[identity type]] by

$$\mathrm{idToSpecOrd}(x, x)(\mathrm{id}_X(x)) \coloneqq \mathrm{refl}_{SpecOrd}(x)$$

\begin{definition}
A **Kolmogorov topological space** or **$T_0$-space** is a topological space which satisfies the $T_0$-[[separation axiom]]: $\mathrm{idToSpecOrd}(x, y)$ is an [[equivalence of types]] for all $x:X$ and $y:X$.

$$T_0:\prod_{x:X} \prod_{y:X} \mathrm{isEquiv}(\mathrm{idToSpecOrd}(x, y))$$
\end{definition}

Since the specialization order is valued in propositions, the $T_0$-[[separation axiom]] ensures that the topological space is an [[h-set]]. 

## Properties
 {#Properties}


### Alternative Characterizations

Regard [[Sierpinski space]] $\Sigma$ as a [[frame]] object in the category of topological spaces (meaning: the representable functor $Top(-, \Sigma): Top^{op} \to Set$ lifts through the monadic forgetful functor $Frame \to Set$), hence as a [[dualizing object]] that induces a contravariant adjunction between frames and topological spaces. Thus for a space $X$, the frame $Top(X, \Sigma)$ is the frame of [[open sets]]; for a frame $A$, there is an accompanying topological space of points $Frame(A, \Sigma)$, a subspace of the product space $\Sigma^{{|A|}}$. The unit of the adjunction is called the *double dual embedding*.  

\begin{proposition}
A [[topological space]] $X$ is $T_0$ precisely when the double dual embedding $X \to Frame(Top(X, \Sigma), \Sigma)$ is a [[monomorphism]].
\end{proposition} 

The proof is trivial: the monomorphism condition translates to saying that for any points $x, y \in X$, if the truth values of $x \in U$ and $y \in U$ agree for every open set $U$, then $x = y$. 


[[!include main separation axioms -- as lifting properties]]


### Reflection

+-- {: .num_prop #KolmogorovQuotient}
###### Proposition
**(Kolmogorov quotient)**

Let $(X,\tau)$ be a [[topological space]]. Consider the [[relation]] on the underlying set by which $x_1 \sim x_1$ precisely if neither $x_i$ has an [[open neighbourhood]] not containing the other. This is an [[equivalence relation]]. The [[quotient topological space]] $X \to X/\sim$ by this
equivalence relation is a $T_0$-space. 

This construction is the reflector exhibiting Kolmogorov spaces as a [[reflective subcategory]] of the [[category]] [[Top]] of all topological spaces.

=--

## Related concepts

* [[Hausdorff topological space]]

* [[nice topological space]]

| [[preorder]] | [[partial order]] | [[equivalence relation]] | [[equality]] |
| - | - | - | - |
| [[topological space]] | [[ Kolmogorov topological space]] | [[symmetric topological space]] | [[accessible topological space]] |

## References

* Wikipedia, _[Kolmogorov space](https://en.wikipedia.org/wiki/Kolmogorov_space)_


[[!redirects T0]]
[[!redirects T_0]]

[[!redirects Kolmogorov space]]
[[!redirects Kolmogorov spaces]]
[[!redirects T0 space]]
[[!redirects T0 spaces]]
[[!redirects T0-space]]
[[!redirects T0-spaces]]
[[!redirects T_0 space]]
[[!redirects T_0 spaces]]
[[!redirects T_0-space]]
[[!redirects T_0-spaces]]

[[!redirects Kolmogorov topological space]]
[[!redirects Kolmogorov topological spaces]]
[[!redirects T0 topological space]]
[[!redirects T0 topological spaces]]
[[!redirects T_0 topological space]]
[[!redirects T_0 topological spaces]]
[[!redirects T0-topological space]]
[[!redirects T0-topological spaces]]
[[!redirects T_0-topological space]]
[[!redirects T_0-topological spaces]]

[[!redirects Kolmogorov quotient]]
[[!redirects Kolmogorov quotients]]
[[!redirects T0 quotient]]
[[!redirects T0 quotients]]
[[!redirects T0-quotient]]
[[!redirects T0-quotients]]
[[!redirects T_0 quotient]]
[[!redirects T_0 quotients]]
[[!redirects T_0-quotient]]
[[!redirects T_0-quotients]]
