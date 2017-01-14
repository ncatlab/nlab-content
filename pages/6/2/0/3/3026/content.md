+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _one-point compactification_ of a [[topological space]] $X$ is a new [[compact space]] $X^+ = X \cup \{\infty\}$ obtained by adding a single new point "$\infty$" to the original space and declaring in $X^+$ the [[complements]] of the original [[closed subspace|closed]] [[compact space|compact]] [[subspaces]] to be [[open subspace|open]].

One may think of the new point added as the "point at infinity" of the original space. A [[continuous function]] on $X$ _[[vanishing at infinity|vanishes at infinity]]_ precisely if it extends to a continuous function on $X^+$ and literally takes the value zero at the point "$\infty$".

This one-point compactification is also known as the _Alexandroff compactification_ after a 1924 paper by [[Pavel Aleksandrov|Павел Сергеевич Александров]] (then transliterated 'P.S. Aleksandroff'). 

The one-point compactification is usually applied to a non-[[compact space|compact]] [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] space.  In the more general situation, it may not really be a [[compactification]] and hence is called the _one-point extension_ or _Alexandroff extension_.


## Definition

### For topological spaces

Let $X$ be any [[topological space]]. Its **one-point extension** $X^*$ is the topological space 

* whose underlying [[set]] is the [[disjoint union]] $X \cup \{\infty\}$ 

* and whose [[open set]]s are 

  1. the open subsets of $X$ (thought of as subsets of $X^*$);

  2. the [[complements]] (in $X^*$) of the [[closed subspace|closed]] [[compact space|compact]] subsets of $X$.

(If $X$ is [[Hausdorff space|Hausdorff]], then its compact subsets must always be closed, so (2) is often given in a simpler form.)

### For non-commutative topological spaces ($C^\ast$-algebras)

Dually in [[non-commutative topology]] the one-point compactification corresponds to the [[unitisation of C*-algebras]].


## Properties

### General

$X^*$ is [[compact space|compact]].

The evident inclusion $X \to X^*$ is an [[open map|open]] [[embedding]].

The one-point compactification is [[universal property|universal]] among all compact spaces into which $X$ has an open embedding, so it is [[essentially unique]].

$X$ is [[dense subspace|dense]] in $X^*$ iff $X$ is not already compact.  Note that $X^*$ is technically a [[compactification]] of $X$ only in this case.

$X^*$ is [[Hausdorff space|Hausdorff]] (hence a [[compactum]]) if and only if $X$ is already both Hausdorff and [[locally compact space|locally compact]].

### Functoriality

The operation of one-point compactification is not a [[functor]] on the whole [[category]] of [[topological spaces]]. But it does extend to a [[functor]] on [[topological spaces]] with [[proper maps]] between them.

## Examples

### Spheres
 {#ExamplesSpheres}

For $n \in \mathbb{N}$ the $n$-[[sphere]] (as a [[topological space]]) is the [[one-point compactification]] of the [[Cartesian space]] $\mathbb{R}^n$

$$
  S^n \simeq (\mathbb{R}^n)^\ast
  \,.
$$

Via this presentation of the $n$-sphere the canonical [[action]] of the [[orthogonal group]] $O(N)$ on $\mathbb{R}^n$ induces an action of $O(n)$ on $S^n$, which preserves the basepoint (the "point at infinity").

This construction presents the [[J-homomorphism]] in [[stable homotopy theory]] and is encoded for instance in the definition of [[orthogonal spectra]].

Slightly more generally, for $V$ any real [[vector space]] of [[dimension]] $n$ one has $S^n \simeq (V)^\ast$. In this context and in view of the previous case, one usually writes

$$
  S^V \coloneqq (V)^\ast
$$

for the $n$-[[sphere]] obtained as the one-point compactification of the vector space $V$.

+-- {: .num_prop }
###### Proposition

For $V,W \in Vect_{\mathbb{R}}$ two real [[vector spaces]], there is a [[natural transformation|natural]] [[homeomorphism]]

$$
  S^V \wedge S^W \simeq S^{V\oplus W}
$$

between the [[smash product]] of their one-point compactifications and the one-point compactification of the [[direct sum]].

=--

+-- {: .num_remark }
###### Remark

In particular, it follows directly from this that the [[suspension]] $\Sigma(-) \simeq S^1 \wedge (-)$ of the $n$-sphere is the $(n+1)$-sphere, up to [[homeomorphism]]:

$$
  \begin{aligned}
    \Sigma S^n 
    & \simeq S^{\mathbb{R}^1} \wedge S^{\mathbb{R}^n}
    \\
    & \simeq S^{\mathbb{R}^1 \oplus \mathbb{R}^n}
    \\
    & \simeq S^{\mathbb{R}^{n+1}}
    \\
    & \simeq S^{n+1}
  \end{aligned}
  \,.
$$

=--


### Thom spaces

For $X$ a [[compact topological space]] and $V \to X$
a [[vector bundle]], then the ([[homotopy type]] of the) one-point compactification of 
the total space $V$ is the [[Thom space]] of $V$, equivalent to $D(V)/S(V)$. 

For a simple example: the real projective plane $\mathbb{RP}^2$ is the one-point compactification of the 'open' M&#246;bius strip, as line bundle over $S^1$. This is a special case of the more general observation that $\mathbb{RP}^{n+1}$ is the Thom space of the tautological line bundle over $\mathbb{RP}^n$. 

## Related concepts

* [[Thom space]]

* [[compactification]] 

  * [[Stone-Cech compactification]]

  * [[end compactification]]

  * [[Bohr compactification]]

  * [[Kaluza-Klein compactification]]


## References

* John Kelly, _General Topology_ (1975)


[[!redirects one-point compactification]]
[[!redirects one-point compactifications]]
[[!redirects One-point compactification]]
[[!redirects Alexandroff compactification]]
[[!redirects Alexandroff compactifications]]
[[!redirects Alexandrov compactification]]
[[!redirects Alexandrov compactifications]]
[[!redirects Aleksandrov compactification]]
[[!redirects Aleksandrov compactifications]]
[[!redirects Александров compactification]]
[[!redirects Александров compactifications]]

[[!redirects one-point extension]]
[[!redirects one-point extensions]]
[[!redirects Alexandroff extension]]
[[!redirects Alexandroff extensions]]
[[!redirects Alexandrov extension]]
[[!redirects Alexandrov extensions]]
[[!redirects Aleksandrov extension]]
[[!redirects Aleksandrov extensions]]
[[!redirects Александров extension]]
[[!redirects Александров extensions]]

[[!redirects point at infinity]]