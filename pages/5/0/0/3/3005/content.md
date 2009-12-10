_Beck's monadicity theorem_ states that a functor $U : D \rightarrow C$ is [[monadic]] if and only if

1. $U$ has a left adjoint
2. $U$ reflects isomorphisms
3. $U$ creates coequalizers of $U$-split pairs

A parallel pair $f,g : a \rightarrow b$ in $D$ is a $U$- _split pair_ if there is a diagram in $C$: 

$$Ua \underoverset{Uf}{Ug}{\rightrightarrows} b \overset{h}{\rightarrow} c$$

where $h$ has a [[section]] $s$ and $Uf$ has a section $t$ such that $Ug \cdot t = s \cdot h$. The arrow $h$ is necessarily a coequalizer of $Uf$ and $Ug$. To say that $U$ creates coequalizers of $U$-split pairs is to say that there exists a coequalizer $e$ of $f,g$ in $D$ such that $Ue$ is isomorphic to $h$.

The _crude monadicity theorem_ states that a functor $U : D \rightarrow C$ is [[monadic]] if

1. $U$ has a left adjoint
2. $U$ reflects isomorphisms
3. $D$ has and $U$ preserves coequalizers of reflexive pairs

where a parallel pair $f,g : a \rightarrow b$ is _reflexive_ if $f$ and $g$ have a common [[section]].