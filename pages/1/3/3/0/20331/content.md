

#Contents#
* table of contents
{:toc}

## Idea

The [[quaternion|quaternionic]] [[projective space]] $\mathbb{H}P^n$ is the [[space]] of right (or left) [[quaternion]] [[lines]] through the origin in $\mathbb{H}^{n+1}$, hence the space of [[equivalence classes]] $[q_1, \cdots, q_{n+1}]$ of [[n-tuple|(n+1)-tuples]]  of [[quaternions]], excluding [[zero]], under the [[equivalence relation]] given by right (or left) [[multiplication]] with non-zero quaternions

$$
  \mathbb{H}P^n
  \;\coloneqq\;
  \big\{
    [q_1, \cdots, q_{n+1}]
  \big\}
  \;\coloneqq\;
  \Big(
    \big\{
      (q_1, \cdots, q_{n+1})
    \big\} 
    \setminus 
    \{(0, \cdots, 0)\}  
  \Big)
  /_{ 
    (q_1, \cdots, q_{n+1}) 
      \sim  
    (q_1 q, \cdots, q_{n+1} q)  
    \vert 
    q \neq 0
  }
$$

As $n$ ranges, there are natural inclusions

$$
  \ast = \mathbb{H}P^0
    \hookrightarrow
  \mathbb{H}P^1
    \hookrightarrow
  \mathbb{H}P^2
    \hookrightarrow
  \mathbb{H}P^3
    \hookrightarrow
  \cdots
  \,.
$$

The [[sequential colimit]] over this sequence is the infinite quaternionic projective space $\mathbb{H}P^\infty$. This is a model for the [[classifying space]] $B Sp(1) \cong B SU(2) \cong B Spin(3)$.

## Properties
 {#Properties}

### General

\begin{proposition}
Every continuous map $\mathbb{H}P^n\rightarrow\mathbb{H}P^n$ for $n \geq 2$ has a [[fixed point]]. This does not hold for $n = 1$ as in this case $\mathbb{H}P^1\cong S^4$ and the antipodal map $S^4\rightarrow S^4, x\mapsto -x$ does not have a fixed point.
\end{proposition}

([Hatcher 02, page 180](#Hatcher02))

### Cell structure

See at *[[cell structure of projective spaces]]*.

### Homology

+-- {: .num_prop #HomologyAndCohomologyOfQuaternionicProjectiveSpace}
###### Proposition
**([[homology]] of quaternionic projective space)**

The [[ordinary homology]] [[homology groups|groups]] of quaternionic projective space $\mathbb{R}P^n$ can be calculated using its CW structure and are given by

\[
  \label{ListOfHomotopyGroupsOfQuaternionicProjectiveSpace}
    H^k
    \big(
      \mathbb{H}P^n
    \big)
    \;=\;
    \left\{
    \array{
       \mathbb{Z} &\vert& \; k = 0, 4,\ldots, 4(n-1),4n
       \\
       1 &\vert& otherwise
    }
    \right.
\]

=--

### As a coset space


As any [[Grassmannian]], quaternion projective space is canonically a [[coset space]], in this case of the [[quaternion unitary group]] $Sp(n+1)$ by the [[central product group]] [[Sp(n).Sp(1)]]:

\[
  \label{SpnCosetSpaceRealization}
  \mathbb{H}P^n
  \;\simeq\;
  \frac{
    Sp(n+1)
  }{
    Sp(n)\cdot Sp(1)
  }
\]

### As a quaternion-Kähler symmetric space (Wolf space)

By the [[coset space]]-realization (eq:SpnCosetSpaceRealization), quaternion projective space is naturally a [[quaternion-Kähler manifold]] which is also a [[symmetric space]]. As such it is an example of a [[Wolf space]].

## Related concepts

* [[real projective space]]

* [[complex projective space]]

* [[octonionic projective space]]

## References

### General

* {#Hatcher02} [[Allen Hatcher]], *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section I.4 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))


See also

* [[Topospaces]], _[Homology of quaternionic projective space](https://topospaces.subwiki.org/wiki/Homology_of_quaternionic_projective_space)_

* Wikipedia, _[Quaternionic projective space](https://en.wikipedia.org/wiki/Quaternionic_projective_space)_

### In string theory
  {#ReferencesInStringTheory}

[[M-theory on 8-manifolds|M-theory on the 8-manifold]] $\;$ [[HP2]], hence on a [[quaternion-Kähler manifold]] of dimension 8 with [[holonomy]] [[Sp(2).Sp(1)]], is considered in

* [[Michael Atiyah]], [[Edward Witten]], p. 75 onwards in  _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

and argued to be [[duality in string theory|dual]] to [[M-theory on G₂-manifolds]] in three different ways, which in turn is argued to lead to a a possible [[proof]] of [[confinement]] in the resulting 4d [[effective field theory]] (see [there](M-theory+on+G2-manifolds#Confinement) for more).

[[!redirects quaternionic projective spaces]]

[[!redirects HP^n]]
[[!redirects HPn]]

[[!redirects HP^1]]
[[!redirects HP1]]
[[!redirects quaternionic projective line]]
[[!redirects quaternionic projective lines]]


