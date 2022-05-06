
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

The [[special unitary group]] $SU(n)$ for $n = 2$.

+-- {: .num_prop}
###### Proposition

As a [[matrix group]] $SU(2)$ is equivalent to the subgroup of the [[general linear group]] $GL(2, \mathbb{C})$ on those of the form

$$
  \left(
    \array{
      u & v
      \\
      - \overline{v} & \overline{u}
    }
  \right)
  \;\;\;
   with
  \;\;
   {\vert u\vert}^2 + {\vert v\vert}^2 = 1
  \,,
$$

where $u,v \in \mathbb{C}$ are [[complex numbers]] and $\overline{(-)}$ denotes [[complex conjugation]].

=--


## Properties

### General


+-- {: .num_prop}
###### Proposition

The underlying [[manifold]] of $SU(2)$ is [[diffeomorphism|diffeomorphic]] to the 3-[[sphere]] $S^3$.

=--



+-- {: .num_prop #ExceptionalIsomorphismOfSU2ToSpin3AndSp1}
###### Proposition

There are [[isomorphisms]] of [[Lie groups]]

1. of $SU(2)$ with the [[spin group]] in [[dimension]] 3 and with the [[quaternionic unitary group]] in one dimension

   $$
     SU(2) 
     \;\simeq\;
     Spin(3)
     \;\simeq\;
     Sp(1)  
   $$



1. of the [[direct product group]] of $SU(2)$ with itself, to [[Spin(4)]]

   $$
     SU(2) \times SU(2)
     \;\simeq\;
     Spin(3) \times Spin(3)
     \;\simeq\;
     Spin(4)
   $$

   with respect to which the canonical inclusion $Spin(3) \hookrightarrow Spin(4)$ is given by the [[diagonal]] map.


=--

See at _[spin group -- Exceptional isomorphisms](spin%20group#ExceptionalIsomorphisms)_.


+-- {: .num_prop}
###### Proposition

The [[maximal torus]] of $SU(2)$ is the [[circle group]] $U(1)$. In the above [[matrix group]] presentation this is naturally identified with the subgroup of matrices of the form

$$
  \left(
    \array{
      t & 0 
      \\
      0 & t^{-1}
    }
  \right)
  \;\;
  with
  t \in U(1) \hookrightarrow \mathbb{C}
  \,.
$$

=--

### Lie algebra

+-- {: .num_prop}
###### Proposition

The [[Lie algebra]] $\mathfrak{su}(2)$ (see also at [[su(2)]]) as a [[complex numbers|complex]] [[matrix Lie algebra]] is the sub Lie algebra on those matrices of the form

$$
  \left(
    \array{
      i z & x + i y
      \\
      - x + i y & - i z
    }
  \right)
  \;\;\;  
  with
  \;\;
  x,y,z \in \mathbb{R}
  \,.
$$

=--

(

+-- {: .num_defn}
###### Definition

The standard [[basis]] elements of $\mathfrak{su}(2)$ given by the above presentation are 

$$
  \sigma_1 
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     0 & 1
     \\
     -1 & 0
   }
  \right)
$$

$$
  \sigma_2 
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     0 & i
     \\
     i & 0
   }
  \right)
$$

$$
  \sigma_3
   \coloneqq
  \frac{1}{\sqrt{2}}
  \left(
   \array{
     i & 0
     \\
     0 & -i
   }
  \right)
  \,.
$$

These are called the _[[Pauli matrices]]_.

=--

+-- {: .num_prop}
###### Proposition

The [[Pauli matrices]] satisfy the [[commutator]] [[relations]]

$$
  [\sigma_1, \sigma_2] = \sigma_3
$$

$$
  [\sigma_2, \sigma_3] = \sigma_1
$$

$$
  [\sigma_3, \sigma_1] = \sigma_2
  \,.
$$


=--


### Coadjoint orbits

+-- {: .num_prop}
###### Proposition

The [[coadjoint orbits]] of the [[coadjoint action]] of $SU(2)$ on $\mathfrak{su}(2)$ are equivalent to the subset of the above matrices with $x^2 + y^2 + z^2 = r^2$ for some $r \geq 0$. 

These are _regular_ coadjoint orbits for $r \gt 0$.


=--

### Finite subgroups

The [[finite subgroup of SU(2)]] have an [[ADE classification]]. See [this theorem](classification+of+finite+rotation+groups#ClassificationOfFiniteSubgroupsOfSO3).

### $G$-Structure and exceptional geometry


[[!include Spin(8)-subgroups and reductions -- table]]



## Related concepts

* [[su(2)]]

* [[complex Hopf fibration]]

* [[Euler angles]]

* [[SU(3)]], [[SU(4)]]

[[!include low dimensional rotation groups -- table]]

## References

See also

* [[Qiaochu Yuan]], _[The representation theory of SU(2)](https://qchu.wordpress.com/2011/06/26/the-representation-theory-of-su2/)_

* Wikipedia, _<a href="https://en.m.wikipedia.org/wiki/Representation_theory_of_SU(2)">Representation theory of SU(2)</a>_


[[!redirects Spin(3)]]

[[!redirects Spin3]]

[[!redirects Sp(1)]]
[[!redirects Sp1]]
