__Beck's monadicity theorem__ states that a [[functor]] $U : D \rightarrow C$ is [[monadic]] if and only if

1. $U$ has a [[left adjoint]]
2. $U$ reflects [[isomorphisms]]
3. $U$ [[created limit|creates]] [[coequalizers]] of $U$-split pairs

A [[parallel pair]] $f,g : a \rightarrow b$ in $D$ is **$U$-split** if there is a diagram in $C$: 

$$U a \;\underoverset{U f}{U g}{\rightrightarrows}\; b \;\overset{h}{\rightarrow}\; c$$

where $h$ has a [[section]] $s$ and $U f$ has a section $t$ such that $U g \cdot t = s \cdot h$.  This implies that the arrow $h$ is necessarily a coequalizer of $U f$ and $U g$.  To say that $U$ *creates coequalizers of $U$-split pairs* is to say that for any such $U$-split pair, there exists a coequalizer $e$ of $f,g$ in $D$ such that $U e$ is isomorphic to $h$.

The __crude monadicity theorem__ states that a functor $U : D \rightarrow C$ is [[monadic]] if

1. $U$ has a left adjoint
2. $U$ reflects isomorphisms
3. $D$ has and $U$ preserves coequalizers of reflexive pairs

where a parallel pair $f,g : a \rightarrow b$ is __reflexive__ if $f$ and $g$ have a common [[section]].  This sufficient, but not necessary, condition is sometimes easier to verify in practice.


[[!redirects Beck's monadicity theorem]]
[[!redirects Beck's monadicity theorem]]
[[!redirects Beck monadicity theorem]]
[[!redirects tripleability theorem]]
[[!redirects crude monadicity theorem]]