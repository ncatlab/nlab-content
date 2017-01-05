| Name | Condition for nearness | Condition for apartness | Condition for proximal neighbourhoods | Condition for proximal unions |
| - | - | - | - | - |
| Isotony (left) | If $A \supseteq B \;\delta\; C$, then $A \;\delta\; C$ | If $A \subseteq B \bowtie C$, then $A \bowtie C$ | If $A \subseteq B \ll C$, then $A \ll C$ | If $A\subseteq B$ and $A\Cup C = X$, then $B\Cup C = X$ |
| Isotony (right) | If $B \;\delta\; C \subseteq D$, then $B \;\delta\; D$ | If $B \bowtie C \supseteq D$, then $B \bowtie D$ | If $B \ll C \subseteq D$, then $B \ll D$ | If $B\subseteq C$ and $A\Cup B = X$, then $A\Cup C = X$ |
| Additivity (left, nullary) | It is false that $\emptyset \;\delta\; A$ | $\emptyset \bowtie A$ | $\emptyset \ll A$ | $X\Cup A = X$ |
| Additivity (right, nullary) | It is false that $A \;\delta\; \emptyset$ | $A \bowtie \emptyset$ | $A \ll X$ | $A \Cup X = X$ |
| Additivity (left, binary) | If $A \cup B \;\delta\; C$, then $A \;\delta\; C$ or $B \;\delta\; C$ | If $A \bowtie C$ and $B \bowtie C$, then $A \cup B \bowtie C$ | If $A \ll C$ and $B \ll C$, then $A \cup B \ll C$ | If $A\Cup C = X$ and $B\Cup C = X$, then $(A\cap B)\Cup C = X$ |
| Additivity (right, binary) | If $A \;\delta\; B \cup C$, then $A \;\delta\; B$ or $A \;\delta\; C$ | If $A \bowtie B$ and $A \bowtie C$, then $A \bowtie B \cup C$ | If $A \ll B$ and $A \ll C$, then $A \ll B \cap C$ | If $A\Cup B = X$ and $A\Cup C = X$, then $A\Cup (B\cap C) = X$ |
| Reflexivity (general) | If $A$ meets $B$ (their [[intersection]] is [[inhabited subset|inhabited]]), then $A \;\delta\; B$ | If $A \bowtie B$, then $A$ and $B$ are [[disjoint set|disjoint]] | If $A \ll B$, then $A \subseteq B$ | If $A\Cup B = X$, then $A\cup B = X$ |
| Reflexivity (for singletons) | $\{x\} \;\delta\; \{x\}$ | It is false that $\{x\} \bowtie \{x\}$ | If $\{x\} \ll A$, then $x \in A$ | If $\{x\}^{\mathsf{c}} \Cup A = X$, then $x\in A$ |
| Transitivity | If for every $D \subseteq X$, either $A \;\delta\; D^{\mathsf{c}}$ or $D \;\delta\; B$, then $A \;\delta\; B$ | If $A \bowtie B$, then for some $D \subseteq X$, both $A \bowtie D^{\mathsf{c}}$ and $D \bowtie B$ | If $A \ll B$, then for some $D \subseteq X$, both $A \ll D$ and $D \ll B$ | |
| Symmetry (weak) | if $A \;\delta\; B$ then $B \;\delta\; A$ | if $A \bowtie B$ then $B \bowtie A$ | if $A \ll B$ then $B^{\mathsf{c}} \ll A^{\mathsf{c}}$ | if $A\Cup B = X$ then $B\Cup A = X$ |
| Symmetry (strong) | $A \;\delta\; B$ iff $B \;\delta\; A$ | $A \bowtie B$ iff $B \bowtie A$ | $A \ll B$ iff $B^{\mathsf{c}} \ll A^{\mathsf{c}}$ | $A\Cup B = X$ iff $B\Cup A = X$ |
| Regularity | If for all $C$ and $D$ such that $B^{\mathsf{c}}\cup C = X$, either $\{x\} \;\delta\; D$ or $D^{\mathsf{c}}\;\delta\; C$, then $\{x\}\;\delta\; B$ | If $\{x\}\bowtie B$, then for some $C$ and $D$, $D^{\mathsf{c}}\bowtie C$, $B^{\mathsf{c}}\cup C = X$, and $\{x\} \bowtie D$ | If $\{x\}\ll A$, then for some $C$ and $D$, $C\ll D$, $A\cup C = X$, and $\{x\}\ll D^{\mathsf{c}}$ | |
| Complete Regularity | | If $A\bowtie B$, then for some $C$ and $D$, $A\bowtie D$, $C\bowtie B$, and $C\cup D = X$. | If $A\ll B$, then for some $C$ and $D$, $A\ll C$, $D\ll B$, and $C^{\mathsf{c}}\cup D = X$. | If $A\Cup B = X$, then for some $C$ and $D$, $A\Cup C = X$, $D\Cup B = X$, and $C\cap D = \emptyset$. |
| Separation | If $\{x\} \delta \{y\}$, then $x = y$ | Unless $\{x\} \bowtie \{y\}$, then $x = y$ | $x = y$ if, for all $A$, $y \in A$ whenever $\{x\} \ll A$ | |
| Perfection (left) | If $A \;\delta\; B$, then $\{x\} \;\delta\; B$ for some $x \in A$ | $A \bowtie B$ if $\{x\} \bowtie B$ for all $x \in A$ | $A \ll B$ if $\{x\} \ll B$ for all $x \in A$ | |
| Perfection (right) | If $A \;\delta\; B$, then $A \;\delta\; \{y\}$ for some $y \in B$ | If $A \bowtie \{y\}$ for all $y \in B$, then $A \bowtie B$ | If $A \ll C_i$ for all $i$, then $A \ll \bigcap_i C_i$ | |

Reflexivity for $\Cup$ doesn't follow from its singleton version constructively.
