
+-- {: .num_lemma}
###### Lemma

  We have
  $$
    \mathbf{4}\wedge \mathbf{4}
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

  Consider the canonical linear basis
  $$
    \mathbf{4}
    \;\simeq\;
    \big\langle \{q_0, q_1, q_2, q_3\}\big\rangle_{\mathbb{R}}
  $$
  by orthonormal quaternions
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
  On this, the action by
  $$
    \mathrm{Sp}(1)
    \;\simeq\;
    \{
    q \in \mathbb{H}
    \;\vert\;
    q \bar q = 1
    \}
  $$
  is by left quaternion multiplication.

  Consider then the following
  linear basis of $\mathbf{4}\wedge \mathbf{4}$:
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
  with induced $\mathfrak{sp}(1)$ Lie algebra action given by
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
  Since everything here is invariant under cyclic permutation of
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
