This page contains a dictionary of some notable [[endofunctors]], and their [[initial algebras of an endofunctor|initial algebras]]/[[terminal coalgebra of an endofunctor|terminal coalgebras]].


Nonexistent (co)algebras are labelled with '/', and unknown ones with '?'.


Base category | Endofunctor                     | Initial Algebra        | Final Coalgebra               | Note, reference |
:--------: | :------------:               | :-------------:         |:----------------:              |  :--------: |
[[Set]] | Const $A$           | $A$            | $A$                           |    |
[[Set]] | $X \mapsto X$               | $\emptyset$            | $1$                           | |
[[Set]] | $X \mapsto A\times X$       | $\emptyset$            | Stream $A$            |  [[stream]]       |
[[Set]] | $X \mapsto A + X$           | $A \times \mathbb{N}$  | ?                             |            |
[[Set]] | $X \mapsto 1 + X$           | $\mathbb{N}$           | ?                             |            |
[[Set]] | $X \mapsto [A, X]$           | $[A, \emptyset]$      | 1                             |            |
[[Set]] | $X \mapsto 1 + A \times X$           | List $A$      | Potentially infinite List $A$ | [[list]]   |
[[Set]] | $X \mapsto 1 + A \times X^2$           | Finite binary tree with $A$-labelled nodes  | Potentially infinite binary tree with $A$-labelled nodes |      |
[[Set]] | $X \mapsto B + A \times X^n$           | Finite $n$-ary tree with $A$-labelled nodes and $B$-labelled leaves | Potentially infinite $n$-ary tree with $A$-labelled nodes with and $B$-labelled leaves| |
[[Set]] | $X \mapsto O + [I, X]$           | $O \times [I, \emptyset ]$ | Potentially infinite Moore machine | |
[[Set]] | $X \mapsto [I, O \times X]$           | ? | Potentially infinite Mealy machine | |
[[Set]] | $X \mapsto X + X$           | $\emptyset$ | $\mathbb{N}^2$ | |
[[Set]] | $X \mapsto X \times X$           | $\emptyset$ | Infinite binary trees | |
[[Set]] | $X \mapsto \mathcal{P}(X)$            | / | / | |

