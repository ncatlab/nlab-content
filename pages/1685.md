+-- {: .un_theorem}
###### Theorem ([[Tohoku]])

Let $A,B,C$ be [[abelian category|abelian categories]] and $F:A\to B$, $G:B\to C$ left [[exact functor|exact]] [[additive functor|additive]] functors. Let $R_F\subset \mathrm{Ob} A$ and $R_G\subset\mathrm{Ob} B$ be [[class of adapted objects|classes of objects adapted to]] $F$ and $G$ respectively, and let furthermore $F(R_A)\subset R_B$. Then the derived functors $R F:D^+(A)\to D^+(B)$, $R G:D^+(B)\to D^+(C)$ and $R(G\circ  F):D^+(A)\to D^+(C)$ are defined and the natural morphism $R(G\circ F)\to R G\circ R F$ is an isomorphism. 
=--

Assume now in the above theorem that $R_F = I_A$ is the class of [[injective object]]s and $R_G$ is simply big enough to contain $F(I_A)$ as required above. Then there is a **Grothendieck spectral sequence** which is a [[spectral sequence]] whose $E_2$-term has
$$
E^{p,q}_2 = R^p G \circ R^q F
$$ 
and which is converging to $R^n(G\circ F)$. These statements should be understood as applied to any object $a$ in $A$ and the spectral sequence is functorial in $a$. Grothendieck spectral sequence has many classical spectral sequences as a special case (see e.g. [[Hochschild-Serre spectral sequence]]). 