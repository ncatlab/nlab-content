Let $\{\gamma_a\}_{a = 0}^{d-1}$ be a [[Dirac representation]] on $\mathbb{C}^{16}$ of the Lorentzian $d= 9$
  Clifford algebra $Cl(8,1)$. We obtain a Dirac representation of the $d = 10$ and $d = 11$ Clifford algebra by taking the following block matrices acting on $\mathbb{C}^{16} \oplus \mathbb{C}^{16}$
  $$
  \Gamma_{a \leq 8}
  \coloneqq
  \left(
   \array{
       0 & \gamma^a
       \\
       \gamma^a & 0
    }
  \right)
  \;, \qquad
  \Gamma_9
  \coloneqq
  \left(
    \array{
      0 & \mathrm{I}
      \\
      -\mathrm{I} & 0
    }
  \right)
  \;, \qquad
  \Gamma_{10}
  \coloneqq
  \left(
    \array{
      i \mathrm{I} & 0
      \\
      0 & -i \mathrm{I}
    }
  \right)
  \,,
$$
where $I$ is the identity matrix.


 The unique irreducible [[Majorana spinor]] representation of $\mathrm{Spin}(10,1)$ is of real dimension 32.
  Under the inclusions
  $$
    \mathrm{Spin}(8,1) \hookrightarrow \mathrm{Spin}(9,1) \hookrightarrow \mathrm{Spin}(10,1)
  $$
  this representation branches as
  $$
    \mathbf{32} \mapsto \mathbf{16}\oplus \overline{\mathbf{16}} \mapsto \mathbf{16} \oplus \mathbf{16}
    \,,
  $$
  where in the middle $\mathbf{16}$ and $\overline{\mathbf{16}}$ are the left and right chiral Majorana-Weyl
  representations in 10d, while on the right the $\mathbf{16}$ is again the unique irreducible real
  representation in 9d.
 Under this branching we decompose a Majorana spinor $\psi \in \mathbf{32}$ as
  $$
    \psi
    =
    \left(
      \array{
        \psi_1
        \\
        \psi_2
      }
    \right)
  $$
  with $\psi_1 \in \mathbf{16}$ and $\psi_2 \in \overline{\mathbf{16}}$ or $\mathbf{16}$.


  Define another set of matrices $\{\Gamma_a^B\}_{a = 0}^{9}$
  by
  $$
    \Gamma_a^{B}
     :=
    \left\{
      \array{
         \Gamma_a & \vert \; a \leq 8\;,
         \\
         \begin{pmatrix}
              0 & \mathrm{I}
              \\
              \mathrm{I} & 0
           \end{pmatrix}
         &
         \vert \; a = 9\;.
      }
    \right.
  $$
  For emphasis we write the original matrices also as $\Gamma_a^A := \Gamma_a$, for $a \leq 9$.

  Moreover we also write
  $$
    \sigma_1 := \Gamma_9
    \;\,,\;\;\;\;\;
    \sigma_2 := -\Gamma_{9} \Gamma_{10}
    \;\,,\;\;\;\;\;
    \sigma_3 := \Gamma_{10}
    \,.
  $$

  Noice that the matrices $\{\Gamma^B_a\}_{a = 0}^9$ in  do not represent
  a Clifford algebra, but the product of any even number of them represents the correct such
  product acting on $\mathbf{16} \oplus \mathbf{16}$. For instance $\exp(\omega^{a b}\Gamma^B_{a b})$
  are the elements of the $\mathrm{Spin}(d-1,1)$-representation on $\mathbf{16}\oplus \mathbf{16}$.
  Also, for \emph{odd} $p = 2k+1$, each of the pairings
  $$
    \overline{\psi}\Gamma^B_{a_1 \cdots a_p}\psi
      =
    \psi^\dagger \Gamma^B_0 \Gamma^B_{a_1 \cdots a_p} \psi
  $$
  is the sum of the corresponding pairings on two copies of $\mathbf{16}$.


By these definition we have
  $$
    \Gamma_9^B = i \, \Gamma_9 \Gamma_{10} = \Gamma_9 \Gamma_{11}
    \,.
  $$

This relation also makes it manifest that $\Gamma_9^B$ commutes not only with all $\Gamma^B_{a b}$ for $a,b \leq 8$, but also with all $\Gamma_a^B\Gamma_9^B$. Consequently, $\Gamma_{10}$ as well as $\Gamma_9$ are invariant under the IIB Spin-action, in that 

  $$
    \exp(-\omega^{a b}\Gamma^B_{a b}) \; \sigma_i \; \exp(\omega^{a b} \Gamma^B_{a b})
      =
    \sigma_i
  $$

for $i \in \{1,2,3\}$.

Conversely, rotation in the $(9,10)$-plane leaves all the $\Gamma_a^B$ invariant, in that

  $$
    \exp(- \tfrac{\alpha}{4} \Gamma_9 \Gamma_{10}) \,\Gamma_a^B\, \exp(\tfrac{\alpha}{4} \Gamma_9 \Gamma_{10})
      \;=\;
    \Gamma_a^B
    \,.
  $$
