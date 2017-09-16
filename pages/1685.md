Theorem ([[Tohoku]]) Let $A,B,C$ be abelian categories and $F:A\to B$, $G:B\to C$ left exact additive functors. Let $R_F\subset \mathrm{Ob} A$ and $R_G\subset\mathrm{Ob} B$ be [[class of adapted objects|classes of objects adapted to]] $F$ and $G$ respectively, and let furthermore $F(R_A)\subset R_B$. Then the derived functors $RF:D^+(A)\to D^+(B)$, $RG:D^+(B)\to D^+(C)$ and $R(G\circ  F):D^+(A)\to D^+(C)$ are defined and the natural morphism $R(G\circ F)\to RG\circ RF$ is an isomorphism. 

Assume now in the above theorem that $R_F = I_A$ is the class of injective objects and $R_G$ is simply big enough to contain $F(I_A)$ as required above. Then there is a **Grothendieck spectral sequence** which is a [[spectral sequence]] whose $E_2$-term has
$$
E^{p,q}_2 = R^p G \circ R^q F
$$ 
and which is converging to $R^n(G\circ F)$. These statements should be understood as applied to any object $a$ in $A$ and the spectral sequence is functorial in $a$. Grothendieck spectral sequence has many classical spectral sequences as a special case.