
> This entry is about H&#246;rmander's criterion on [[wave front sets]]. This is different from "[[Hörmander's condition]]" on [[tangent vector fields]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _H&#246;rmander criterion_ ([H&#246;rmander 90, theorem 8.2.10](#Hoermander90)) says that the [[product of distributions|product of two distributions]] $u_1 \cdot u_2$ (on some [[manifold]] $X$) is well-defined if their [[wave front sets]] $WF(u)$ are such that for $v \in T^\ast_x X$ a [[covector]] contained in one of the two wave front sets then the covector $-v \in T^\ast_x X$ with the opposite [[direction of a vector|direction]] in _not_ contained in the other wave front set, i.e. the [[intersection]] [[fiber product]]
inside the [[cotangent bundle]] $T^\ast X$ of the pointwise [[sum]] of wave fronts with the [[zero section]] is [[empty set|empty]]:

$$
  \left( WF(u_1) + WF(u_2) \right) \underset{T^\ast X}{\times} X
  \;=\;
  \emptyset
$$

i.e.

$$
  \array{
     && \emptyset
     \\
     & \swarrow && \searrow
     \\
     WF(u_1) + WF(u_2) && (pb) && X
     \\
     & \searrow && \swarrow_{\mathrlap{0}}
     \\
     && T^\ast X
  }
$$


See at _[[product of distributions]]_ for details.


## References

* {#Hoermander71} [[Lars Hörmander]], _Fourier integral operators. I_.  Acta Mathematica 127, 79–183 (1971) ([Euclid](https://projecteuclid.org/euclid.acta/1485889699))

* {#Hoermander90} [[Lars Hörmander]], section 8.1 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990



[[!redirects Hoermander's criterion]]
[[!redirects Hormander's criterion]]

[[!redirects Hörmander criterion]]
[[!redirects Hoermander criterion]]
[[!redirects Hormander criterion]]
