
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

_under construction_

## Idea

The Gelfand--Naimark--Segal (GNS) construction establishes a correspondence between cyclic $*$-[[representation]]s of $C^*$-[[C*-algebra|algebras]] and certain linear functionals (usually called _[[state on an operator algebra|states]]_) on those same $C^*$-algebras.  The correspondence comes about from an explicit construction of the [[star-representation|*-representation]] from one of the [[linear functionals]] ([[state on an operator algebra|states]]).


## The nPOV

The GNS construction (as outlined above) is a special case of a more general construction of Ghez, Lima and Roberts applied to $C^\ast$-categories (horizontal categorification of $C^\ast$-algebras).

+--{: .un_theorem}
###### Theorem

Let $\mathcal{C}$ be a $C^\ast$-category. Fix an object $A \in \operatorname{Ob}\mathcal{C}$ and let $\sigma$ be a state on the $C^\ast$-algebra $\mathcal{C}(A,A)$. Then there exists a $*$-representation
$$
\rho_\sigma \colon \mathcal{C} \to \mathbf{Hilb}
$$
together with a cyclic vector $\xi \in \rho_\sigma(A)$ such that for all $x \in \mathcal{C}(A,A)$,
$$
\sigma(x) = \langle \xi, \rho_\sigma(x)\xi \rangle.
$$
=--

## Construction

...

## Proof of Theorem

...

## The Classical Case

A $C*$-algebra $A$ is a $C^\ast$-category $\mathcal{A}$ with one object $\bullet$, where we make the identification $A = \mathcal{A}(\bullet,\bullet)$. In this case the theorem reduces to the classical GNS construction.

+-- {: .un_theorem}
###### Theorem

Given a [[states in AQFT and operator algebra|state]], $\rho$, on some [[C*-algebra]], $A$, there is a $*$-[[representation]] $\pi$ of $A$ with a [[cyclic vector]] $\xi$ whose associated state is $\rho$.  In other words,

$$
  \rho(x)= \langle \xi, \pi(x)\xi \rangle
$$

for every $x$ in $A$.
=--




## Applications

The GNS construction is a central ingredient that translates between the [[Heisenberg picture]] and the [[Schrödinger picture]] of [[quantum mechanics]]: the [[AQFT]] and the [[FQFT]] picture of [[quantum field theory]]. In the former one considers $C^\ast$-[[algebras of observables]], in the latter the [[spaces of states]]. Given a $C^\ast$-algebra of observables, the corresponding space of state can be taken to be that given by the GNS construction.

## References

See also 

* Wikipedia, _[Gelfand-Naimark-Segal construction](https://en.wikipedia.org/wiki/Gelfand%E2%80%93Naimark%E2%80%93Segal_construction)_

category: operator algebras

[[!redirects Gelfand-Naimark-Segal construction]]
[[!redirects Gelfand–Naimark–Segal construction]]
[[!redirects Gelfand--Naimark--Segal construction]]
[[!redirects GNS construction]]
[[!redirects GNS-construction]]
[[!redirects GNS representation]]
[[!redirects GNS-representation]]
[[!redirects GNS theorem]]