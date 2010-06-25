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

## Definition ##
We start with a [[Haag-Kastler vacuum representation]] that we assume to be irreducible and [[Haag dual]].

Let $\pi_0$ be the vacuum representation from now on, K denote double cones and $\mathcal{J}_0$ be the [[causal index set]] of double cones.

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

## Properties ##
...

## References ##

see [[AQFT]] ff.

[[!redirects DHR analysis]]
[[!redirects Doplicher-Haag-Roberts superselection theory]]
[[!redirects Doplicher-Haag-Roberts superselection sector]]
[[!redirects Doplicher-Haag-Roberts superselection sectors]]