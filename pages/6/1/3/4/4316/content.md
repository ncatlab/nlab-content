<div class="rightHandSide toc">
   [[!include AQFT and operator algebra contents]]
</div>

#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The DHR superselection theory is about [[superselection sectors]] in the [[Haag-Kastler approach]] to [[AQFT]].
As such, it has to state one or more conditions on representations of the given [[Haag-Kastler net]] that specify the representations of the quasi-local algebra that are deemed physically admissible. 

It is named after [[Sergio Doplicher]], [[Rudolf Haag]] and [[J.E. Roberts]].

In the following we consider the theory starting with a [[Haag-Kastler vacuum representation]] on [[Minkowski spacetime]].

The DHR condition says that **all expectation values (of all observables) should approach the vacuum expectation values, uniformly, when the region of measurement is moved away from the origin.  

This excludes long range forces like electromagnetism from consideration, because, by [[Gauss' law]], the electric charge in a finite region can be measured by the flux of the field strength through a sphere of arbitrary large radius. The DHR analysis is of interest nevertheless, because it has reached a certain maturity and is therefore an excellent object to study: see for example the [[Doplicher-Roberts reconstruction theorem]]. 

## Abstract ##
After the definition of admissible representations we collect some notions that will enable us to state a description of all admissible representations using intrinsic properties of the quasi-local algebra.

## Definition ##
We start with a [[Haag-Kastler vacuum representation]] that we assume to be irreducible and [[Haag dual]].

Let $\pi_0$ be the vacuum representation from now on, K denote double cones and $\mathcal{J}_0$ be the [[causal index set]] of double cones, just as $\mathcal{O}$ are bounded open sets and $\mathcal{J}$ the [[causal index set]] of bounded open sets.

Recall that the [[C-star algebra]]

$$
\mathcal{A} := clo_{\| \cdot \|} \bigl( \bigcup_{\mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O}) \bigr) 
$$

is called the quasi-local algebra of the given net. We will in the same way associate a [[C-star algebra]] to every open region $\mathcal{O}_0$ via

$$
\mathcal{A}(\mathcal{O}_0) := clo_{\| \cdot \|} \bigl( \bigcup_{\mathcal{O}_0 \supseteq \mathcal{O}\in\mathcal{J}}\mathcal{M}(\mathcal{O}) \bigr) 
$$

+-- {: .un_defn}
###### Definition
A representation $\pi$ of the local algebra $\mathcal{A}$ is called (DHR) **admissible** if $\pi | \mathcal{A}(\mathcal{K}^{\perp})$ is unitarily equivalent to $\pi_0 | \mathcal{A}(\mathcal{K}^{\perp})$ for all $K \in \mathcal{J}_0$, that is, for all double cones $K$.
=--

Note that the equivalence of the representations is required for the causal complement of _all_ double cones, not a special one, so that the characterization that "the representations can not be distinguished at space-like infinity" is misleading.  

+-- {: .un_defn}
###### Definition
Recall that a mapping 
$$
\rho: \mathcal{A} \to \mathcal{A}
$$
is called a **unital endomorphism** if $\rho$ is linear, multiplicative ($\rho(AB) = \rho(A) \rho(B)$) and $\rho(\mathbb{1}=1)$.
=--

We will drop "unitarily" from now on.

For any representation $\pi$ and endomorphism $\rho$ the composition $\pi \circ \rho$ is another representation. For this reason one can hope to gain some insights into the representations by studying the endomorphisms, while the set of endomorphisms has certainly more structure than that of representations: For example, endomorphisms may have inverses, and endomorphisms form a [[monoid]] by composition.

First we define "unitarily equivalent" analog to the definition for [[representations of C-star algebras]]:

+-- {: .un_defn}
Two endomorphisms $\rho_1, \rho_2$ are **unitarily equivalent** if there is a [[unitary operator]] $U \in \mathcal{A}$ such that $\rho_1 = ad(U) \rho_2 = U \rho_2 U^{-1}$
=--

## Properties ##
...

## References ##

see [[AQFT]] ff.

[[!redirects DHR analysis]]
[[!redirects Doplicher-Haag-Roberts superselection theory]]
[[!redirects Doplicher-Haag-Roberts superselection sector]]
[[!redirects Doplicher-Haag-Roberts superselection sectors]]