

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given any kind of [[generalized cohomology theory]] $\mathbf{H}$, and a [[domain]] $X$ and [[coefficient]] $A$, the _cocycle space_ $\mathbf{H}(X,A)$ is the "space", or rather the the [[∞-groupoid]]/[[homotopy type]], whose

* [[elements]]/[[objects]] are [[cocycles]] in $\mathbf{H}$-[[generalized cohomology theory|cohomology theory]] on $X$ with [[coefficients]] in $A$ (hence [[maps]]/[[morphisms]] $X \to A$);

* [[edges]]/[[morphisms]] are [[coboundaries]] between these cocycles (i.e. [[homotopies]]/[[gauge transformations]])

* [[faces]]/[[2-morphisms]] are coboundaries between coboundaries;

* ...

* [[n-cells]]/[[n-morphisms]] are $n$th order coboundaries (i.h. [[higher homotopies]]/[[higher gauge transformations]]).

## Definition

Precisely: For $\mathbf{H}$ some [[(∞,1)-topos]], and $X,A \in \mathbf{H}$ two [[objects]], the _cocycle space_ of [[cocycles]] on $X$ with [[coefficients]] in $A$ is the [[(∞,1)-categorical hom-space]] $\mathbf{H}(X,A)$.

## Truncation to cohomology sets

The actual [[cohomology]] [[set]] $H(X,A)$ is the [[0-truncation]]/[[connected components]] of the cocycle space:

$$
  H(X,A) \;=\; \pi_0\big( \mathbf{H}(X,A) \big)
  \,.
$$

Similarly, if $A$ is equipped with the [[mathematical structure|structure]] of a [[pointed object]] $\ast \overset{a_0}{\to} A$, the cocycle space $\mathbf{H}(X,A)$ becomes canonically pointed by the [[constant morphism]] $const_{a_0} \colon X \to \ast \overset{a_0}{\to} A$ and the [[0-truncation]]/[[connected components]] of the corresponding [[based loop space]] of the cocucle space is the cohomoloy set in one degree lower:

$$
  H(X,\Omega A)
  \;\simeq\;
  \pi_1 \big( \mathbf{H}(X,A), const_{a_0} \big) 
  \;\simeq\;
  \pi_0 \big(  \Omega_{const_{a_0}} \mathbf{H}(X,A) \big)
  \,.
$$

Etc.

## Related concepts

* [[hom-space]], [[space of maps]]

* [[Cohomotopy charge map]]

[[!include homotopy-homology-cohomology]]


[[!redirects cocycle spaces]]