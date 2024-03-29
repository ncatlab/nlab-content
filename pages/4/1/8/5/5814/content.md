
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Vassiliev skein relation** is a way to extend [[knot invariants]] to [[singular knots]] (at least, to singular knots where the only singularities are double points).  If $v$ is a knot invariant that takes values in an abelian group, then it is extended to singular knots using the relation
$$
v(L_d) = v(L_+) - v(L_-)
$$
where $L_d$ is a singular knot with a double point and $L_+$, respectively $L_-$, are formed from $L_d$ by replacing the double point by a positively oriented, respectively negatively oriented, crossing.

\begin{tikzcd}[sep={between origins, 30pt}]
  &
  {} && {}
  &[+30pt] & 
  {} \ar[-Latex, from=ddrr, line width=1.5pt]  && {}
  &[+30pt] & 
  {} && {}
  \\
  L_d = 
  &
  & \raisebox{-2.5pt}{\scalebox{1.8}{$\bullet$}}
  & 
  &
  L_+ =
  &
  &
  & 
  &
  L_- =
  \\
  &
  {} \ar[-Latex, uurr, line width=1.5pt] 
  && 
  {} \ar[-Latex, uull, line width=1.5pt] 
  &&
  {} \ar[-Latex, uurr, line width=1.5pt, crossing over] 
  && 
  {} 
  &&
  {} \ar[-Latex, uurr, line width=1.5pt] 
  && 
  {} \ar[-Latex, uull, line width=1.5pt, crossing over] 
\end{tikzcd}



## References

General discussion:

* Wikipedia, _[Skein relation](https://en.wikipedia.org/wiki/Skein_relation)_

Discussion in the context of [[quantization of 3d Chern-Simons theory]]:

* {#GelcaUribe10a} [[Razvan Gelca]], [[Alejandro Uribe]], _From classical theta functions to topological quantum field theory_  ([arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf))

* {#GelcaUribe10b} [[Razvan Gelca]], [[Alejandro Uribe]], _Quantum mechanics and non-abelian theta functions for the gauge group $SU(2)$_ ([arXiv:1007.2010](http://arxiv.org/abs/1007.2010))


category: knot theory

[[!redirects Vassiliev skein relations]]

[[!redirects skein relation]]
[[!redirects skein relations]]


