
$$
  \begin{array}{c}
    x
    \\
    ---
    \\
    xx
  \end{array}
$$


$$
  \begin{array}{ll}
    \cdots
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathcal{S}_z
      \cdot
      \int^{y \in \mathbf{X}}
      \mathbf{X}(y,z)
      \cdot
      \big(
        \mathbf{X}(x,y)
        \cdot
        \mathcal{V}_{y}
      \big)
      \;,\;
      \mathscr{W}_{z}
    \Big)
    &
    \text{ co-Yoneda lemma }
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \int_{y \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathbf{X}(y,z)
      \cdot
      \mathcal{S}_z
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \mathscr{W}_{z}
    \Big)
    &
    \text{ enriched homs preserve enriched limits }
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \int_{y \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \big(\mathscr{W}_{z}\big)^{
        \mathbf{X}(y,z)
        \cdot
        \mathcal{S}_z
      }
    \Big)
    &
    \text{ cotensoring iso of }\; \mathbf{C}
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \int_{z \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \big(\mathscr{W}_{z}\big)^{
        \mathbf{X}(y,z)
        \cdot
        \mathcal{S}_z
      }
    \Big)
    &
    \text{ enriched homs preserve enriched limits }
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \int_{z \in \mathbf{X}}
      \big(\mathscr{W}_{z}\big)^{
        \mathbf{X}(y,z)
        \cdot
        \mathcal{S}_z
      }
    \Big)
    &
    \text{ definition }
  \end{array}
$$
