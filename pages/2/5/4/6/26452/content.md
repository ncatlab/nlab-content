This page contains a dictionary of some notable [[endofunctors]], and their [[initial algebras of an endofunctor|initial algebras]]/[[terminal coalgebra of an endofunctor|terminal coalgebras]].


Nonexistent (co)algebras are labelled with '/', and unknown ones with '?'.


Base category | Endofunctor                | Initial Algebra        | Final Coalgebra               | Note, reference |
:-----: | :------------:                   | :-------------:         |:----------------:            |  :--------: |
[[Set]] | [[constant functor|Const]] $A$                        | $A$                    | $A$                           | |
[[Set]] | $X \mapsto X$                    | $\varnothing$            | $1$                           | |
[[Set]] | $X \mapsto 1 + X$                | $\mathbb{N}$           | [[conatural number|Conatural numbers]] $\mathbb{N}^\infty$ | [[extended natural number]] |
[[Set]] | $X \mapsto A + X$                | $A \times \mathbb{N}$  | $A \times \mathbb{N} + 1$, ie [[conatural numbers]] "terminated" (when they aren't $\infty$) with $A$ | [[partial map classifier]] |
[[Set]] | $X \mapsto X + X$ or $X \mapsto 2 \times X$                | $\emptyset$            | $2^\mathbb{N}$ (i.e. one definition of [[stream|Stream]] $2$)               | |
[[Set]] | $X \mapsto A \times X$                | $\emptyset$            | $A^\mathbb{N}$ (i.e. one definition of [[stream|Stream]] $A$)               | [[sequence]], [[writer monad]], [[stream]] |
[[Set]] | $X \mapsto X \times X$ or $X \mapsto [2, X]$          | $\emptyset \simeq [2, \emptyset]$            | 1 (the unique infinite unlabelled binary tree)     | |
[[Set]] | $X \mapsto [A, X]$               | $[A, \emptyset]$       | 1                             | [[reader monad]] |
[[Set]] | $X \mapsto 1 + A \times X$       | [[list|List]] $A$               | another definition of [[stream|Stream]] $A$; i.e. potentially infinite [[list|List]] $A$ | [[list]], [[stream]] |
[[Set]] | $X \mapsto 1 + A \times X^2$     | Finite [[binary tree]] with $A$-labelled nodes  | Potentially infinite [[binary tree]] with $A$-labelled [[nodes]] | [[tree]] |
[[Set]] | $X \mapsto B + A \times X^n$     | Finite $n$-ary tree with $A$-labelled nodes and $B$-labelled [[leaves]] | Potentially infinite $n$-ary tree with $A$-labelled nodes with and $B$-labelled leaves| |
[[Set]] | $X \mapsto O \times [I, X]$      | $O \times [I, \emptyset]$ | Potentially infinite [[Moore machine]] | |
[[Set]] | $X \mapsto [I, O \times X]$      | $[I, \emptyset]$       | Potentially infinite [[Mealy machine]]             | |
[[Set]] | $X \mapsto \mathcal{P}(X)$       | /                      | /                             | |
[[Set]] | $X \mapsto \mathcal{P}_{\text{fin}}(X)$ | Finite [[rooted forests]] | Potentially infinite finitely-branching [[rooted forests]] | |
[[Set]] | [[polynomial endofunctor]] | [[W-type]] | [[M-type]] | |
[[bi-pointed object|Bipointed]] [[set|Sets]] | $X \mapsto X \vee X$ | [[dyadic rational numbers]] in the [[interval]] $[0,1]$ | The [[closed interval]] $[0,1] \subseteq \mathbb{R}$ | [[coalgebra of the real interval]] | |
[[linearly ordered sets]] | $X \mapsto \omega \cdot X$, where $\omega \cdot X$ is the cartesian product of the natural numbers with the underlying set of $X$, equipped with the [[lexicographic order]]. | $\emptyset$ | The non-negative [[real numbers]] $\mathbb{R}_{\geq 0}$ | [[real number]] | |
[[Archimedean ordered fields]] | $X \mapsto \mathcal{D}(X)$ where $\mathcal{D}(X)$ is the Archimedean ordered field of two-sided [[Dedekind cuts]] of $X$ | The [[real numbers]] $\mathbb{R}$ | The [[real numbers]] $\mathbb{R}$ | | |
[[Archimedean ordered fields]] | $X \mapsto \mathcal{C}(X)$ where $\mathcal{C}(X)$ is the quotient of [[Cauchy sequences]] in the Archimedean ordered field $X$ | The [[HoTT book real numbers]] $\mathbb{R}_H$ | The [[Dedekind real numbers]] $\mathbb{R}$ | These are the same objects in the presence of [[excluded middle]] or [[countable choice]].| |
Any [[category]] | The [[constant functor]] $X \mapsto A$ given object $A$ | $A$ | $A$ | |
Any [[category]] | The [[identity functor]] $X \mapsto X$ | [[initial object]] | [[terminal object]] | |
Any [[extensive category]] | $X \mapsto 1 + X$ given [[terminal object]] $1$ and [[coproduct]] $+$ | [[natural numbers object]] | ? | |
Any [[closed monoidal category|closed]] [[abelian category]] | $X \mapsto I \sqcup (A \otimes X)$ given [[tensor unit]] $I$, [[tensor product]] $\otimes$, [[coproduct]] $\sqcup$, and object $A$ | [[tensor algebra]] of $A$ | [[cofree coalgebra]] over $A$ | [[tensor algebra]], [[cofree coalgebra]] |
[[Infinity-Grpd|$\infty$-Grpd]] | $X \mapsto \Sigma X$ | [[sphere spectrum]] $\mathbb{S}$ | ? | [[suspension]] |