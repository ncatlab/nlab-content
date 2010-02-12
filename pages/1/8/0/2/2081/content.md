A [[sheaf]] $F$ of [[set]]s on (the [[category of open subsets]] of) a [[topological space]] $X$ is __flabby__ (flasque) if for any open subset $U\subset X$, the restriction morphism $F(X)\to F(U)$ is [[surjection|onto]]. Equivalently, for any open $U\subset V\subset X$ the restriction $F(V)\to F(U)$ is surjective. In mathematical literature in English, the original French word __flasque__ is still often used instead of flabby here. 

An archetypal example is the sheaf of all set-theoretic (not necessarily continuous) [[sections]] of a [[bundle]] $E\to X$; regarding that every sheaf over a topological space is the sheaf of sections of an [[etale space]], every sheaf can be embedded into a flabby sheaf $C^0(X,F)$ defined by

$$
U \mapsto \prod_{x\in U} F_x
$$

where $F_x$ denotes the [[stalk]] of $F$ at point $x$. 

Flabbiness is a local property: if $F|_U$ is flabby for every sufficiently small open subset, than $F$ is flabby. Given a continuous map $f:X\to Y$ and a flabby sheaf $F$ on $X$, the [[direct image]] sheaf $f_* F : V\mapsto F(f^{-1}V)$ is also flabby. Any [[exact sequence]] of sheaves of [[abelian groups]] $0\to F_1\to F_2\to F_3\to 0$ in which $F_1$ is exact, is also an exact sequence in the category of presheaves (the exactness for stalks implies exactness for groups of sections over any fixed open set). As a corollary, if $F_1$ and $F_2$ are flabby, then $F_3$ is flabby. 

Flabby sheaves were probably first studied in [[Tohoku]], where flabby [[resolution]]s were also considered. A classical reference is Godement's monograph. 

[[!redirects flasque sheaf]]