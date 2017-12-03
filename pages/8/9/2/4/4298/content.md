

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of countents
{:toc}

## Idea

A [[vector]], hence an [[element]] of some [[vector space]] $\mathcal{H}$ is called _cyclic_ with respect to the [[action]]/[[representation]] of some [[algebra]] $\mathcal{A}$ on $\mathcal{H}$ if ever element of $\mathcal{H}$ may be obtained by acting on $v$ with some algebra element $A \in \mathcal{A}$, or rather if one may always find a [[sequence]] of elements $A_n$ whose action on $v$ [[convergence of a sequence|converges]] to the given element.

## Definition

+-- {: .num_defn}
###### Definition

Let 

1. $\mathcal{A}$ be a [[C*-algebra]];

1. $\mathcal{H}$ a [[Hilbert space]];

1. $\pi \;\colon\; \mathcal{A} \longrightarrow \mathcal{B}(\mathcal{H})$ a [[C*-representation]] of $\mathcal{A}$ on $\mathcal{H}$.

Then a [[vector]] $v \in \mathcal{H}$ is called a **cyclic vector** if the [[image]] of $v$ under $\mathcal{A}$ acting via $\rho$ is a [[dense subspace]] of $\mathcal{H}$:

$$
  im\left( \rho(-)(v) \right) 
   \overset{\text{dense}}{\hookrightarrow}
  \mathcal{H}
  \,.
$$

=--

## Properties

The notions of cyclic vector is dual to that of [[separating vector]] with respect to the [[commutant]] $\mathcal{M}'$, that is a vector is cyclic for $\mathcal{M}$ iff it is separating for $\mathcal{M}'$.

## Applications 

* In [[algebraic quantum field theory]] the [[state on a star-algebra|states]] corresponding to cyclic vectors appear as _[[vacuum states]]_. See [[Reeh-Schlieder theorem]].

* [[GNS construction]]

## References

* [[eom]], _[Cyclic vector](https://www.encyclopediaofmath.org/index.php/Cyclic_vector)_

[[!redirects cyclic vectors]]