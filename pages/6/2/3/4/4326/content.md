
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

## Idea

The _special unitary group_ is the [[subgroup]] of the [[unitary group]] on the elements with [[determinant]] equal to 1.

For $n$ a [[natural number]],  the **special unitary group** $SU(n)$ is the [[group]] of [[isometry|isometries]] of the $n$-dimensional [[complex number|complex]] [[Hilbert space]] $\mathbb{C}^n$ which preserve the [[volume form]] on this space. It is the [[subgroup]] of the [[unitary group]] $U(n)$ consisting of the $n \times n$ [[unitary matrix|unitary]] [[matrix|matrices]] with [[determinant]] $1$.

More generally, for $V$ any complex [[vector space]] equipped with a nondegenerate [[Hermitian form]] $Q$, $SU(V,Q)$ is the group of isometries of $V$ which preserve the volume form derived from $Q$.  One may write $SU(V)$ if $Q$ is obvious, so that $SU(n)$ is the same as $SU(\mathbb{C}^n)$.  By $SU(p,q)$, we mean $SU(\mathbb{C}^{p+q},Q)$, where $Q$ has $p$ positive [[eigenvalue]]s and $q$ negative ones.

## Properties

### As part of the ADE pattern

[[!include ADE -- table]]

### Representation theory

See at *[[representation theory of the special unitary group]]*.

## Examples

### $SU(2)$
 {#SU2}

We discuss aspects of [[SU(2)]], hence

$$
  SU(2) \coloneqq SU(2,\mathbb{C}) = SU(\mathbb{C}^2)
  \,.
$$

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

+-- {: .num_prop}
###### Proposition

The underlying [[manifold]] of $SU(2)$ is [[diffeomorphism|diffeomorphic]] to the 3-[[sphere]] $S^3$.

=--

+-- {: .num_prop}
###### Proposition

There is an [[isomorphism]] of [[Lie groups]]

$$
  SU(2) \simeq Spin(3)
$$

with the [[spin group]] in [[dimension]] 3.

=--

See at _[spin group -- Exceptional isomorphisms](spin%20group#ExceptionalIsomorphisms)_.

+-- {: .num_prop}
###### Proposition

The [[Lie algebra]] $\mathfrak{su}(2)$ as a [[matrix Lie algebra]] is the sub Lie algebra on those matrices of the form

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

+-- {: .num_defn}
###### Definition

The standard [[basis]] elements of $\mathfrak{su}(2)$ given by the above presentation are 

$$
  \sigma_1 
   \coloneqq
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

The [[Pauli matrices]] satisfy the [[commutator]] relations

$$
  [\sigma_1, \sigma_2] = 2\sigma_3
$$

$$
  [\sigma_2, \sigma_3] = 2\sigma_1
$$

$$
  [\sigma_3, \sigma_1] = 2\sigma_2
  \,.
$$


=--

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

+-- {: .num_prop}
###### Proposition

The [[coadjoint orbits]] of the [[coadjoint action]] of $SU(2)$ on $\mathfrak{su}(2)$ are equivalent to the subset of the above matrices with $x^2 + y^2 + z^2 = r^2$ for some $r \geq 0$. 

These are _regular_ coadjoint orbits for $r \gt 0$.


=--

### $SU(3)$

* [[SU(3)]]

### $SU(4)$
 {#SU4}

+-- {: .num_prop}
###### Proposition

There is an [[isomorphism]] of [[Lie groups]]

[[SU(4)]] $\simeq$ [[Spin(6)]]

with the [[spin group]] in [[dimension]] 6.

=--

See at _[spin group -- Exceptional isomorphisms](spin%20group#ExceptionalIsomorphisms)_.


## Related concepts

* For [[SU(2)]]:

  * [[quaternion]]

  * [[geometric quantization of the 2-sphere]]

* [[Euler angles]]

* [[Pauli group]]

## References


* [[Howard Georgi]], §13  in: *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;

  > with an eye towards application to (the [[standard model of particle physics|standard model]] of) [[particle physics]]




[[!redirects special unitary group]]
[[!redirects special unitary groups]]

[[!redirects Pauli matrix]]
[[!redirects Pauli matrices]]

[[!redirects Pauli operator]]
[[!redirects Pauli operators]]

[[!redirects SU(N)]]
[[!redirects SU(n)]]



