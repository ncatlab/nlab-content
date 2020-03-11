
That the quark model correctly predicts hadron bound states is a purely computer-experimental observation (established only fairly recently for the first few hadrons <a href="https://arxiv.org/abs/0906.3599">arXiv:0906.3599</a>) of which a conceptual understanding remains an <a href="https://ncatlab.org/nlab/show/confinement#OpenProblem">open problem</a>, dubbed one of the Millennium Problems. 

While it is an old idea that the string model of mesons gives a conceptual handle on the confinement mechanism, its detailed and quantitatively accurate development used to be lacking. Making the string model of hadrons actually work is what <a href="https://ncatlab.org/nlab/show/AdS-QCD+correspondence">holographic QCD</a> is all about.

Since holographic QCD readily explains fundamental characteristics of confined QCD that remain mysterious not just in the quark model but also in popular <em>ad hoc</em> strong coupling model building such as the bag model (not only the confinement and chiral symmetry breaking mechanism itself, but also for instance vector meson dominance and the Cheshire cat property of the bag model are readily explained by holographic QCD) it is attractive to researchers interested in real-world QCD.

The Skyrme model for hadrons is in fact reasonable not in its original form but only after adjoining the tower of vector mesons to the pion. But in that tower-corrected form the Skyrme model works wonders: nuclei all the way up to carbon(!) are well-decribed already by Skyrmions in the pion+rho field (<a href="https://ncatlab.org/nlab/show/skyrmion#IncludingTowerOfMesons">arXiv:1803.06098</a>). This tower-correction of Skyrmions is explained by holographic QCD, where all mesons are unified as the transversal KK-modes of the 5d flavour gauge theory.

That available results in holographic AdS/QCD currently only ("only") address the strongly coupled confined QCD phase and not its asymptotically free UV is not intrinsic to the holographic theory but owed to its computational development: holography is studied for strong 't Hooft coupling only for the convenience to be able to disregard string-scale and strong string-coupling effects on the bulk side. Inclusion of <a href="https://ncatlab.org/nlab/show/large%201/N%20limit">small-N corrections</a> into AdS/QCD to get the full picture remains to be developed but is not being ignored (<a href="https://ncatlab.org/nlab/show/AdS-QCD+correspondence#SmallNOpenProblem">here</a>).



***

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
