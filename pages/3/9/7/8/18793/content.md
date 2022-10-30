

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

## Definition


+-- {: .num_defn #ProperlySupportedPseudoDifferentialOperator}
###### Definition
**([[properly supported peudo-differential operator]])

A [[pseudo-differential operator]] $Q$ on a [[manifold]] $X$ is called _properly supported_ if for each [[compact subset]] $K \subset X$ there exists a compact subset $K' \subset X$ such that for $u$ a [[distribution]] with [[support of a distribution|support]] in $K$ it follows that the [[derivative of distributions]] $Q u$ has support in $K'$ 

$$
  supp(u)\subset K \phantom{A}\Rightarrow \phantom{A} supp(Q u) \subset K'
$$

and such that 

$$
  u\vert_{K'} = 0 \phantom{A} \Rightarrow \phantom{A} (Q u)\vert_{K} = 0
  \,.
$$

=--

([H&#246;rmander 85 (18.1.21)](#Hoermander85) recalled e.g. in [Radzikowski 96. p. 8,9](#Radzikowski96))

## Examples

+-- {: .num_example}
###### Example
**([[differential operators]] are properly supported [[pseudo-differential operators]])**

Every ordinary [[differential operator]] $D$, regarded as a [[pseudo-differential operator]], is properly supported (def. \ref{ProperlySupportedPseudoDifferentialOperator}), since differential operators do not increase the [[support]] of the functions they act on:

$$
  supp(D f) \subset supp(f)
  \,.
$$

=--

## Related concepts

* [[propagation of singularities theorem]]

## References

* {#DuistermaatHoermander72} [[Johann Duistermaat]], [[Lars Hörmander]], _Fourier integral operators II_, Acta Mathematica 128, 183-269, 1972 ([Euclid](https://projecteuclid.org/euclid.acta/1485889724))

* {#Hoermander85} [[Lars Hörmander]], _The analysis of partial differential operators III_, Springer 1985

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))


[[!redirects properly supported pseudo-differential operator]]

