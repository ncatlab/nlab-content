Given a $k$-[[bialgebra]] $H$, and a left [[Hopf action]] $\triangleright$ of $H$ on a $k$-algebra $A$, one defines the **crossed product algebra** $A\sharp H$ (in Hopf algebra literature also called the **smash product algebra**) as the $k$-algebra whose underlying vector space is $A\otimes H$ and the product is given by

$$
(a\otimes h)(a'\otimes h') =
\sum a (h_{(1)}\triangleright a')\otimes h_{(2)}h'.
$$

The idea is that if the bialgebra $H$ is in fact a Hopf algebra embedded as $1\otimes H\subset A\sharp H$ whatever the product in the latter is (but satisfies $(a\otimes 1)(1\otimes h) = a\otimes h$, and if the action is inner, i.e. $h\triangleright a = \sum h_{(1)} a S(h_{(2)})$ within $A\sharp H$ then $\sum (h_{(1)}\triangleright a) h_{(2)} = \sum h_{(1)} a S(h_{(2)}) h_{(3)} = \sum h_{(1)} a \epsilon(h_{(2)})= h a$, hence the formula for the product above is a tautology: $a h a' h' = a(h_{(1)}\triangleright a') h_{(2)} h'$.  

Similarly, given a right Hopf action of $H$ on $A$, one defines the crossed product algebra $H\sharp A$ whose underlying space is $H\otimes A$. The left and right versions are isomorphic if $H$ has an invertible antipode; this extends the correspondence between the left and right actions obtained by composing with the antipode map. 

Every smash product algebra of the form $A\sharp H$ is naturally equipped with a monomorphism $A\mapsto A\sharp 1\hookrightarrow A\sharp H$ of algebras and with a right $H$-coaction $a\otimes h\mapsto a\otimes \Delta(h)\in (A\sharp H)\otimes H$ making $A\sharp H$ into a right $H$-comodule algebra. Map $\gamma: h\mapsto 1\otimes h$, $H\hookrightarrow A\sharp H$ is then a map of right $H$-comodule algebra (where the coaction on $H$ is $\Delta$), and $A\otimes 1\subset A\sharp H$ is the subalgebra of $H$-coinvariants. If $H$ is a Hopf algebra, then homomorphism $\gamma$ is a convolution invertible linear map with convolution inverse $\gamma^{-1}$ defined by $\gamma^{-1}(h)=\gamma(Sh)$ for $h\in H$, where $S$ is the antipode of $H$. Conversely, 

**Proposition** _Let $H$ be a Hopf algebra, $E$ a right $H$-comodule algebra, and $\gamma:H\to E$ a map of right $H$-comodule algebra. Clearly $H$ acts on $E^{co H}$ by $h\triangleright a = \sum \gamma(h_{(1)}) a\gamma(Sh_{(2)})$ for $a\in E^{co H}$ and $h\in H$, where the product on the right-hand side is in $E$. Conclusion: 
$E\cong E^{co H}\sharp H$ where the smash product is with respect to that action._

There is also a more general cocycled crossed product. In that case a similar convolution invertible map $\gamma$ is constructed, which is however just an $H$-comodule map, but it fails to be a homomorphism of algebras; the cocycle is needed to measure the failure. 

[[!redirects smash product algebra]]