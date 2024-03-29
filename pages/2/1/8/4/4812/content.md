Given a [[commutative unital ring]] $k$ and a [[coassociative coalgebra|coassociative]] $k$-[[coalgebra]] $C = (C,\Delta,\epsilon)$ with comultiplication $\Delta$ and counit $\epsilon\colon C\to k$, a $k$-[[submodule]] $I\subseteq C$ is 

* a __right coideal__ if $\Delta(I)\subseteq \overline{I\otimes C}$, 

* a __left coideal__ if $\Delta(I)\subseteq \overline{C\otimes I}$,

* a __coideal__ if $\Delta(I)\subseteq \overline{I\otimes C}+\overline{C\otimes I}$ and $\epsilon(I)=0$.

Here, $\overline{I \otimes C}$ denotes the image of $I \otimes C \to C \otimes C$ (this distinction is not necessary when $C$ is a flat $k$-module, for example when $k$ is a field). 
 
In other words, a left coideal is simply a left subcomodule in $C$ with [[coaction]] being the comultiplication and a coideal is a sub[[bicomodule]] in $C$, where the comultiplication plays simultaneously the roles of left and right $C$-coactions on itself.

If $I\subseteq C$ is a coideal, then the [[quotient module|quotient]] $k$-module $C/I$ is equipped with the canonical structure of a coassociative $k$-coalgebra, the __quotient co(al)gebra__; the comultiplication is induced via choosing an arbitrary representative in each class, namely 

$$
\Delta_{C/I}(c+I):= \Delta_C(c) + I\otimes C + C\otimes I
\in C/I \otimes C/I,
$$
or, in [[Sweedler notation]], 
$\Delta_{C/I}(c) = \sum (c_{(1)}+I)\otimes (c_{(2)}+I)$ where $\Delta_C(c)= \sum c_{(1)}\otimes c_{(2)}$.

[[!redirects coideal]]
[[!redirects coideals]]
[[!redirects left coideal]]
[[!redirects left coideals]]
[[!redirects right coideal]]
[[!redirects right coideals]]
[[!redirects quotient cogebra]]
[[!redirects quotient coalgebra]]
[[!redirects quotient cogebras]]
[[!redirects quotient coalgebras]]
