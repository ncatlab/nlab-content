
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

The **Vassiliev skein relation** is a way to extend [[knot invariants]] to [[singular knots]] (at least, to singular knots where the only singularities are double points).  If $v$ is a knot invariant that takes values in an abelian group, then it is extended to singular knots using the relation
$$
v(L_d) = v(L_+) - v(L_-)
$$
where $L_d$ is a singular knot with a double point and $L_+$, respectively $L_-$, are formed from $L_d$ by replacing the double point by a positively oriented, respectively negatively oriented, crossing.

$$
\begin{array}{ccc}
\begin{svg}[[!include SVG skein double crossing]]\end{svg} &
\begin{svg}[[!include SVG skein positive crossing]]\end{svg} &
\begin{svg}[[!include SVG skein negative crossing]]\end{svg} \\
L_d & L_+ & L_-
\end{array}
$$

category: knot theory