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


+-- {: .num_defn}
###### Definition

The standard [[basis]] elements of $\mathfrak{su}(2)$ given by the above presentation are 

$$
  \sigma_1 
   \coloneqq
  \frac{1}{2}
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
  \frac{1}{2}
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
  \frac{1}{2}
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


### Representation theory
 {#RepresentationTheory}

To record some aspects of the [[linear representation|linear]] [[representation theory]] of [[SU(2)]].

(...)

+-- {: .num_lemma #4Wedge4SpSp1Is3TimesTrivialPlusThree}
###### Lemma

  We have
  $$
    \wedge^2 \mathbf{4}
    \;\simeq\;
    3 \cdot \mathbf{1}
    \;\oplus\;
    1 \cdot \mathbf{3}
    \;\;\;\in\;
    \mathrm{RO}(\mathrm{Sp}(1))
  $$

=--

+-- {: .proof}
###### Proof

  Consider the canonical [[linear basis]]
  \[
    \label{BasisFor4}
    \mathbf{4}
    \;\simeq\;
    \big\langle \{q_0, q_1, q_2, q_3\}\big\rangle_{\mathbb{R}}
  \]
  by [[orthonormal basis|orthonormal]] [[quaternions]]
  $$
    q_0, q_1, q_2, q_3
    \;\in\;
    \mathbb{H}
  $$
  $$
    \begin{aligned}
    &
    q_0 = 1\,,
    \\
    &
    q_i q_i = -1 = - q_0  \;\; \text{for} i \in \{1,2,3\} \,,
    \\
    &
    q_{\sigma(1)} q_{\sigma(3)} =  \mathrm{sgn}(\sigma)  q_{\sigma(3)}
    \,,
    \text{for}  \sigma \in \mathrm{Sym}(3)
    \end{aligned}
  $$
  On this, the [[action]] by [[Sp(1)]]
  $$
    \mathrm{Sp}(1)
    \;\simeq\;
    \{
    q \in \mathbb{H}
    \;\vert\;
    q \bar q = 1
    \}
  $$
  is by left [[quaternion]] [[multiplication]].

  Consider then the following
  [[linear basis]] of $\mathbf{4}\wedge \mathbf{4}$:
  $$
    \mathbf{4}\wedge \mathbf{4}
    \;\simeq\;
    \left\langle
    \left\{
      \array{
        a_1^+
        :=
        q_0 \wedge q_1 + q_2 \wedge q_3,
        \\
        a_2^+
        :=
        q_0 \wedge  q_2 + q_3 \wedge  q_1,
        \\
        a_3^+
        :=
        q_0 \wedge q_3 + q_1 \wedge  q_2,
      }
      \array{
        a_1^-
        :=
        q_0 \wedge q_1 - q_2 \wedge q_3,
        \\
        a_2^-
        :=
        q_0 \wedge q_2 - q_3 \wedge q_1,
        \\
        a_3^-
        :=
        q_0 \wedge q_3 - q_1 \wedge q_2
      }
    \right\}
    \right\rangle
  $$
  with induced $\mathfrak{sp}(1)$ [[Lie algebra action]] given by
  $$
    q_i \cdot ( q_j \wedge q_k )
    \;=\;
    (q_i q_j) \wedge q_k
    +
    q_j \wedge (q_i q_k)
    \,.
  $$
  From this we find
  $$
    \begin{aligned}
    q_1 \cdot a_1^{\pm}
    & = \;
    q_1
      \cdot
    \big(
      q_0 \wedge q_1
      \pm
      q_2 \wedge q_3
    \big)
    \\
    & =\;
    \big(
    \underset{
      = 0
    }{
      \underbrace{
        q_1 \wedge q_1
      }
    }
    +
    \underset{
      = 0
    }{
      \underbrace{
        q_0 \wedge (-q_0)
      }
    }
    \big)
    \pm
    \big(
    \underset{
      = 0
    }{
      \underbrace{
        q_3 \wedge q_3
      }
    }
    +
    \underset{
      = 0
    }{
      \underbrace{
        q_2 \wedge (- q_2)
      }
    }
    \big)
    \\
    & =\;
    0
    \end{aligned}
  $$
  and
  $$
    \begin{aligned}
    q_1 \cdot a_2^{\pm}
    & =\;
    q_1
      \cdot
    \big(
      q_0 \wedge q_2
      \pm
      q_3 \wedge q_1
    \big)
    \\
    & = \;
    \big(
    \underset{
      = q_1 \wedge q_2
    }{
      \underbrace{
        q_1 \wedge q_2
      }
    }
    +
    \underset{
      = q_0 \wedge q_3
    }{
      \underbrace{
        q_0 \wedge q_3
      }
    }
    \big)
    \pm
    \big(
    \underset{
      = q_1 \wedge q_2
    }{
      \underbrace{
        (- q_2) \wedge q_1
      }
    }
    +
    \underset{
      = q_0 \wedge q_3
    }{
      \underbrace{
        q_3 \wedge (- q_0)
      }
    }
    \big)
    \\
    & =\;
    \left\{
      \begin{array}{l}
        2 a_3^+
        \\
        0
      \end{array}
    \right.
    \end{aligned}
  $$
  and
  $$
    \begin{aligned}
    q_1 \cdot a_3^{\pm}
    & =\;
    q_1
      \cdot
    \big(
      q_0 \wedge q_3
      \pm
      q_1 \wedge q_2
    \big)
    \\
    & = \;
    \big(
    \underset{
      = - q_3 \wedge q_1
    }{
      \underbrace{
        q_1 \wedge q_3
      }
    }
    +
    \underset{
      = - q_0 \wedge q_2
    }{
      \underbrace{
        q_0 \wedge (-q_2)
      }
    }
    \big)
    \pm
    \big(
    \underset{
      = - q_0 \wedge q_2
    }{
      \underbrace{
        (- q_0) \wedge q_2
      }
    }
    +
    \underset{
      = - q_3 \wedge q_1
    }{
      \underbrace{
        q_1 \wedge q_3
      }
    }
    \big)
    \\
    & =\;
    \left\{
      \begin{array}{l}
        -2 a_2^+
        \\
        0
      \end{array}
    \right.
    \end{aligned}
    \,.
  $$
  Since everything here is [[invariant]] under [[cyclic permutation]] of
  the three non-zero indices it follows generally that
  $$
    (\tfrac{1}{2} q_i) \cdot a_j^+ \;=\; \underset{k}{\sum} \epsilon_{i j k} a_k^+
    \,,
    \;\;
    (\tfrac{1}{2} q_i) \cdot a_j^- \;=\; 0
    \;\;
    \text{for all} i,j \in \{1,2,3\}
  $$
  But this means that
  $$
    \big\langle \{a^+_1, a^+_2, a^+_3\} \big\rangle
    \;\simeq\;
    \mathbf{3}
    \,,
    \phantom{aa}
    \big\langle \{a^-_i\} \big\rangle
    \;\simeq\;
    \mathbf{1}
    \;\;\;\in
    \mathrm{RO}(\mathrm{Sp}(1))
    \,.
  $$

=--

\linebreak

+-- {: .num_lemma #4Wedge4Wedge4ofSp1IsFour}
###### Lemma

  We have
  $$
    \wedge^3 \mathbf{4}
    \;\simeq\;
    \mathbf{4}
    \;\;
    \in RO(Sp(1))
    \,.
  $$

=--

+-- {: .proof}
###### Proof

  Consider the following [[linear basis]]

  $$
    \wedge^3 \mathbf{4}
    \;\simeq_{\mathbb{R}}\;
    \left\langle
    \left\{
    \begin{array}{l}
      b_0 := + q_1 \wedge q_2 \wedge q_3
      \\
      b_1 := - q_0 \wedge q_2 \wedge q_3
      \\
      b_2 := + q_0 \wedge q_1 \wedge q_3
      \\
      b_3 := - q_0 \wedge q_1 \wedge q_2
    \end{array}
    \right\}
    \right\rangle
    \,.
  $$

  We claim that in terms of these basis elements
  and those of (eq:BasisFor4) the [[isomorphism]] is given by
  $b_0 \mapsto q_0$, $b_i \mapsto q_i$.
  This follows by direct inspection. For instance for the
  [[Lie algebra action]] of $q_1$ we find:

  $$
    \begin{aligned}
      q_1 \cdot b_0
      & \; = \;
      q_1 \cdot ( q_1 \wedge q_2 \wedge q_3 )
      \\
      & \; = \;
      \underset{
        = b_1
      }{
        \underbrace{
          (- q_0) \wedge q_2 \wedge q_3
        }
      }
      \;+\;
      \underset{
        = 0
      }{
        \underbrace{
          q_1 \wedge q_3 \wedge q_3
        }
      }
      \;+\;
      \underset{
        = 0
      }{
        \underbrace{
          q_1 \wedge q_2 \wedge (- q_2)
        }
      }
      \\
      &
      \;=\;
      b_1
    \end{aligned}
  $$

  $$
    \begin{aligned}
      q_1 \cdot b_1
      & \;=\;
      q_1 \cdot ( - q_0 \wedge q_2 \wedge q_3 )
      \\
      & \;=\;
      -
      \underset{
        b_0
      }{
        \underbrace{
          q_1 \wedge q_2 \wedge q_3
        }
      }
      -
      \underset{
        = 0
      }{
      \underbrace{
        q_0 \wedge q_3 \wedge q_3
      }
      }
      -
      \underset{
        = 0
      }{
        \underbrace{
          q_0 \wedge q_2 \wedge (-q_2)
        }
      }
      \\
      & \;=\;
      - b_0
    \end{aligned}
  $$

  $$
    \begin{aligned}
      q_1 \cdot b_2
      & \;=\;
      q_1 \cdot (q_0 \wedge q_1 \wedge q_3)
      \\
      &
      \;=\;
      \underset{
        = 0
      }{
        \underbrace{
          q_1 \wedge q_1 \wedge (- q_2)
        }
      }
      +
      \underset{
        = 0
      }{
        \underbrace{
          q_0 \wedge (- q_0) \wedge q_3
        }
      }
      +
      \underset{
        = b_3
      }{
        \underbrace{
          q_0 \wedge q_1 \wedge (- q_2)
        }
      }
      \\
      & \;=\;
      b_3
    \end{aligned}
  $$

  $$
    \begin{aligned}
    q_1 \cdot b_3
    & \;=\;
    q_1 \cdot (- q_0 \wedge q_1 \wedge q_2)
    \\
    & \;=\;
    -
    \underset{
      = 0
    }{
      \underbrace{
        q_1 \wedge q_1 \wedge q_2
      }
    }
    -
    \underset{
      = 0
    }{
      \underbrace{
        q_0 \wedge (- q_0) \wedge q_2
      }
    }
    -
    \underset{
      = b_2
    }{
      \underbrace{
        q_0 \wedge q_1 \wedge q_3
      }
    }
    \\
    & \;=\;
    - b_2
    \end{aligned}
  $$


=--



## Related concepts

* [[su(2)]]

* [[quantum rotation gate]]

* [[complex Hopf fibration]]

* [[Euler angles]]

* [[SU(3)]], [[SU(4)]], [[SU(5)]]

* [[Pauli quantum gate]]

* [[Solovay-Kitaev theorem]]

[[!include low dimensional rotation groups -- table]]

## References

* [[Howard Georgi]], §3  in: *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;

  > with an eye towards application to (the [[standard model of particle physics|standard model]] of) [[particle physics]]


On the [[coadjoint orbits]] of $SU(2)$:

* [[Alexandre Kirillov]], p. 183 in: _[[Lectures on the Orbit Method]]_, Graduate Studies in Mathematics, 64, American Mathematical Society, (2004)



See also

* [[Qiaochu Yuan]], _[The representation theory of SU(2)](https://qchu.wordpress.com/2011/06/26/the-representation-theory-of-su2/)_

* Wikipedia, _<a href="https://en.m.wikipedia.org/wiki/Representation_theory_of_SU(2)">Representation theory of SU(2)</a>_


[[!redirects Spin(3)]]

[[!redirects Spin3]]

[[!redirects Sp(1)]]
[[!redirects Sp1]]
