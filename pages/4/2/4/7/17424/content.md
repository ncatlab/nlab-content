
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The _real projective space_ $\mathbb{R}P^n$ is the [[projective space]] of the real [[vector space]] $\mathbb{R}^{n+1}$.

Equivalently this is the [[Grassmannian]] $Gr_1(\mathbb{R}^{n+1})$.

## Properties

### General

\begin{proposition}
Every continuous map $\mathbb{R}P^n\rightarrow\mathbb{R}P^n$ for $n$ even has a [[fixed point]]. This does not hold for $n$ odd as in this case the continuous map $\mathbb{R}P^n\rightarrow\mathbb{R}P^n, [x_0:x_1:\ldots:x_{n-1}:x_n]\mapsto[x_1:-x_0:\ldots:x_n:-x_{n-1}]$ does not have a fixed point.
\end{proposition}

([Hatcher 02, page 155 exercise 2](#Hatcher02))

([Hatcher 02, page 180](#Hatcher02))

\begin{proposition}
For $n\neq 1,3,7$, the smallest number $k$, so that there exists an [[immersion]] of real projective space $\mathbb{R}P^n$ into [[cartesian space]] $\mathbb{R}^{k-1}$, is exactly the [[topological complexity]] $\operatorname{TC}(\mathbb{R}P^n)$ (with convention $\operatorname{TC}(*)=1$).
\end{proposition}

([Farber & Tabachnikov & Yuzvinsky 02, Theorem 12](#FarberTabachnikovYuzvinsky02))

\begin{proposition}
For $n=1,3,7$ one has
$$
\operatorname{TC}(\mathbb{R}P^n)
=n+1
$$
for the [[topological complexity]] (with convention $\operatorname{TC}(*)=1$).
\end{proposition}

([Farber & Tabachnikov & Yuzvinsky 02, Proposition 18](#FarberTabachnikovYuzvinsky02))

### Cell structure
 {#CellStructure}

+-- {: .num_prop #RealProjectiveSpaceCWComplex}
###### Proposition
**([[CW-complex]] structure)**

For $n \in \mathbb{N}$, the real projective space $\mathbb{R}P^n$ admits the structure of a [[CW-complex]].

=--

+-- {: .proof}
###### Proof

Use that $\mathbb{R}P^n \simeq S^n/(\mathbb{Z}/2)$ is the [[quotient space]] of the [[Euclidean space|Euclidean]] [[n-sphere]] by the $\mathbb{Z}/2$-action which identifies [[antipode|antipodal points]].

The standard CW-complex structure of $S^n$ realizes it via two $k$-cells for all $k \in \{0, \cdots, n\}$, such that this $\mathbb{Z}/2$-action restricts to a homeomorphism between the two $k$-cells for each $k$. Thus $\mathbb{R}P^n$ has a CW-complex structure with a single $k$-cell for all $k \in \{0,\cdots, n\}$. 

=--

### Homotopy groups

+-- {: .num_prop #HomotopyGroupsOfRealProjectiveSpace}
###### Proposition
**([[homotopy groups]] of real projective space)**

The [[homotopy groups]] of real projective plane can be calculated with the long exact sequence of homotopy groups ([Hatcher 02, Theorem 4.41.](#Hatcher02)) of the [[fiber bundle]] $S^0\rightarrow S^n\rightarrow\mathbb{R}P^n$ and are given by
\[
  \label{ListOfHomotopyGroupsOfComplexProjectiveSpace}
    \pi_k
    \big(
      \mathbb{R}P^n
    \big)
    \;=\;
    \left\{
    \begin{array}{ll}
      \ast & k = 0
      \\
      \mathbb{Z} & k = 1, n = 1
      \\
      \mathbb{Z}_2 & k = 1, n > 1
      \\
      \pi_k
      \big(
        S^n
      \big)
      &
      k \geq 1, n > 0
    \end{array}
    \right.
\]

=--

### Homology and cohomology

+-- {: .num_prop #HomologyAndCohomologyOfRealProjectiveSpace}
###### Proposition
**([[homology]] and [[cohomology]] of real projective space)**

The [[ordinary homology]] [[homology groups|groups]] of real projective space $\mathbb{R}P^n$ can be calculated using its CW structure and are given by
\[
  \label{HomologyOfComplexProjectiveSpace}
    H_k
    \big(
      \mathbb{R}P^n
    \big)
    \;=\;
    \left\{
    \begin{array}{ll}
       \mathbb{Z} & k = 0 \quad or \quad k = n \quad if \quad odd
       \\
       \mathbb{Z}_2 & k \quad odd \quad and \quad 1 \leq k \leq n
       \\
       1 & otherwise
    \end{array}
    \right.
\]

([Hatcher 02, Example 2.42](#Hatcher02))

Similarly the [[ordinary cohomology]] [[cohomology groups|groups]] of $\mathbb{R}P^n$ are
\[
  \label{CohomologyOfRealProjectiveSpace}
    H^k
    \big(
      \mathbb{R}P^n
    \big)
    \;=\;
    \left\{
    \begin{array}{ll}
       \mathbb{Z} & k = 0 \quad or \quad k = n \quad if \quad odd
       \\
       \mathbb{Z}_2 & k \quad even \quad and \quad 1 \leq k \leq n
       \\
       1 & otherwise
    \end{array}
    \right.
\]

=--

One has $H_{n-1}(\mathbb{R}P^n)\cong\mathbb{Z}_2$ für $n$ odd and $H_{n-1}(\mathbb{R}P^n)\cong 1$ for $n$ even, hence $\mathbb{R}P^n$ is [[orientable]] iff $n$ is odd.

([Hatcher 02, Corollary 3.28.](#Hatcher02))

### Relation to the $\mathbb{Z}/2$-classifying space
 {#RelationToClassifyingSpace}

The infinite real projective space $\mathbb{R}P^\infty \coloneqq \underset{\longrightarrow}{\lim}_n \mathbb{R}P^n$ is the [[classifying space]] [[BO(n)|$B O(1)$]] for [[real line bundles]]. It has the [[homotopy type]] of the [[Eilenberg-MacLane space]] $K(\mathbb{Z}/2,1) = B \mathbb{Z}/2$.

### Kahn-Priddy theorem

* [[Kahn-Priddy theorem]]

## Related concepts

* [[complex projective space]]

* [[quaternionic projective space]]

* [[octonionic projective space]]

* [[classifying space]]

## References

See also:

* [[Topospaces]], _[Real projective space](https://topospaces.subwiki.org/wiki/real_projective_space)_
* Wikipedia, _[Real projective space](https://en.wikipedia.org/wiki/Real_projective_space)_

On [[topological complexity]] of real projective space and connection with their [[immersion]]:

* {#FarberTabachnikovYuzvinsky02} [[Michael Farber]], [[Serge Tabachnikov]], [[Sergey Yuzvinsky]], _Topological robotics: motion planning in projective spaces_ (2002), [arXiv:math/0210018](https://arxiv.org/abs/math/0210018)

Homotopy groups, homology and cohomology of real projective space:

* {#Hatcher02} [[Allen Hatcher]], _Algebraic Topology_, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

Computation of [[cohomotopy]]-sets of real projective space:

* {#West71} Robert West, _Some Cohomotopy of Projective Space_, Indiana University Mathematics Journal Indiana University Mathematics Journal Vol. 20, No. 9 (March, 1971), pp. 807-827 ([jstor:24890146](https://www.jstor.org/stable/24890146))



[[!redirects real projective spaces]]

[[!redirects real projective n-space]]
[[!redirects real projective n-spaces]]

[[!redirects infinite real projective space]]
[[!redirects infinite real projective spaces]]