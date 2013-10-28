
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What are called the _Steenrod squares_ is a certain system of [[cohomology operations]] on [[cohomology]] with [[coefficients]] in $\mathbb{Z}_2$.

## Definition

For $n \in \mathbb{N}$ write $B^n \mathbb{Z}_2$ for the [[classifying space]] of [[ordinary cohomology]] in degree $n$ with [[coefficients]] in the [[group of order 2]] $\mathbb{Z}_2$ (the [[Eilenberg-MacLane space]] $K(\mathbb{Z}_2,n)$), regarded as an [[object]] in the [[homotopy category]] $H$ [[model structure on topological spaces|of topological spaces]]).

Notice that for $X$ any topological space ([[CW-complex]]), 

$$
  H^n(X, \mathbb{Z}_2) \coloneqq H(X, B^n \mathbb{Z}_2) 
$$

is the [[ordinary cohomology]] of $X$ in degree $n$ with [[coefficients]] in $\mathbb{Z}_2$. Therefore, by the [[Yoneda lemma]], [[natural transformations]]

$$
  H^{k}(-, \mathbb{Z}_2) \to H^l(-, \mathbb{Z}_2)
$$

correspond bijectively to morphisms $B^k \mathbb{Z}_2 \to B^l \mathbb{Z}_2$.

The following characterization is due to ([SteenrodEpstein](#SteenrodEpstein)).

+-- {: .num_defn}
###### Definition

The **Steenrod squares** are a collection of [[cohomology operations]]

$$
  Sq^n \;\colon\; H^k(-, \mathbb{Z}_2) \longrightarrow H^{k+n}(-, \mathbb{Z}_2)
  \,,
$$

hence of [[morphisms]] in the [[homotopy category]]

$$
  Sq^n \;\colon\; B^k \mathbb{Z}_2 \longrightarrow B^{k + n} \mathbb{Z}_2
$$

for all $n,k \in \mathbb{N}$ satisfying the following conditions:

1. for $n = 0$ it is the [[identity]];

1. if $X$ is a [[manifold]] of [[dimension]] $dim X \lt n$ then $Sq^n(X) = 0$;

1. for $k = n$ the morphism $Sq^n : B^n \mathbb{Z}_2 \to B^{2n} \mathbb{Z}_2$ is the [[cup product]] $x \mapsto x \cup x$;

1. $Sq^n(x \cup y) = \sum_{i + j = n} (Sq^i x) \cup (Sq^j y)$;


=--

An analogous definition works for [[coefficients]] in $\mathbb{Z}_p$ for any [[prime number]] $p \gt 2$. The corresponding operations are then usually denoted

$$
  P^n \;\colon\; B^k \mathbb{Z}_p \longrightarrow B^{k+n} \mathbb{Z}_{p}
  \,.
$$

Under [[composition]], the Steenrod squares form an [[associative algebra]] over $\mathbb{F}_2$, called the _[[Steenrod algebra]]_. See there for more.

## Properties

### Relation to Bockstein homomorphism

$Sq^1$ is the [[Bockstein homomorphism]] of the [[short exact sequence]] $\mathbb{Z}_2 \to \mathbb{Z}_4 \to \mathbb{Z}_2$.


### Compatibility with suspension

The Steenrod squares are compatible with the [[suspension isomorphism]].

Therefore the Steenrod squares are often also referred to as the _[[stabilization|stable]] [[cohomology operations]]_

### Adem relations

(...)

$$
  Sq^i \circ Sq^j 
   = 
  \sum_{k = 0}^{[i/2]}
  \left(
    \array{
      j - k - 1
      \\
      i - 2k 
    }
  \right)_{mod 2}
  Sq^{i + j -k} \circ Sq^k
$$

for all $0 \lt i \lt 2 j$.

(...)

## Related concepts

* [[Bockstein homomorphism]],

* [[Wu class]]

* [[Steenrod algebra]]

## References

The operations were first defined in 

* [[Norman Steenrod]], _Products of cocycles and extensions of mappings_, Annals of mathematics (1947)

The axiomatic definition appears in

* [[Norman Steenrod]], [[David Epstein]], _Cohomology operations_, Annals of mathematics studies, Princeton University Press (1962)
 {#SteenrodEpstein}

See also

* [[Wen-Tsun Wu]], _Sur les puissances de Steenrod_, Colloque de Topologie de Strasbourg, IX, La Biblioth&#232;que Nationale et Universitaire de Strasbourg, (1952)


[[!redirects Steenrod squares]]

[[!redirects stable cohomology operation]]
[[!redirects stable cohomology operations]]