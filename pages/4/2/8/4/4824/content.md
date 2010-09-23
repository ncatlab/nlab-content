Let $C,D$ be [[comonoid]]s in a [[monoidal category]] $A = (A,\otimes,1)$. A $C$-$D$ __bicomodule__ is an object $M$ in $A$, with left $C$-[[coaction]] $\rho_C : M\to D\otimes M$ and right $D$-coaction $\rho_D: M\to M\otimes D$ which commute in the sense that

$$
(\rho_C\otimes id_D)\circ\rho_D = (id_C\otimes \rho_D)\circ \rho_C.
$$

Typical cases are when $A$ is the category of $k$-[[modules]] where $k$ is a [[commutative unital ring]] (the comonoids are then $k$-[[coalgebras]]), and the more general case of bicomodules over [[corings]], where $A$ is the category of $k$-bimodules where $k$ is a possibly [[noncommutative ring]]. 

There is an operation of [[cotensor product]] for bicomodules over coalgebras/corings; however it is not associative in general, unlike the [[tensor product]] of bimodules over rings!


[[!redirects bicomodule]]
[[!redirects bicomodules]]
