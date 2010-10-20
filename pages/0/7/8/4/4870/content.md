Whiskering is an operation which acts on a functor and a natural transformation (unlike composition which acts on a pair of functors or a pair of natural transformations, or functor application which acts on a functor and a morphism).

* If $F,G:C\to D$ and $H:D\to E$ are functors and $\eta:F\to G$ is a natural transformation whose coordinate at $A$ is $\eta_A$, then __whiskering $H$ and $\eta$__ yields the natural transformation $(H\circ F)\to(H\circ G)$ whose coordinate at object $A$ of $C$ is $H(\eta_A)$.
* If $F:C\to D$ and $G,H:D\to E$ are functors and $\eta:G\to H$ is a natural transformation whose coordinate at $A$ is $\eta_A$, then __whiskering $\eta$ and $F$__ yields the natural transformation $(G\circ F)\to(H\circ F)$ whose coordinate at object $A$ of $C$ is $\eta_{F(A)}$.

### Links ###

* [A MathOverflow question about whiskering](http://mathoverflow.net/questions/40813/what-is-the-name-for-the-composition-of-a-functor-with-a-natural-transformation/40814#40814)