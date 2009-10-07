Given a $k$-[[bialgebra]] $H$, and a left [[Hopf action]] $\triangleright$ of $H$ on a $k$-algebra $A$, one defines the **crossed product algebra** $A\sharp H$ (in Hopf algebra lietrature also called the **smash product algebra**) as the $k$-algebra whose underlying vector space is $A\otimes H$ and the product is given by

$$
(a\otimes h)(a'\otimes h') =
\sum a (h_{(1)}\triangleright a')\otimes h_{(2)}h'.
$$

The idea is that if the bialgebra $H$ is in fact a Hopf algebra embedded as $1\otimes H\subset A\sharp H$ whatever the product in the latter is (but satisfies $(a\otimes 1)(1\otimes h) = a\otimes h$, and if the action is inner, i.e. $h\triangleright a = \sum h_{(1)} a S(h_{(2)})$ within $A\sharp H$ then $\sum (h_{(1)}\triangleright a) h_{(2)} = \sum h_{(1)} a S(h_{(2)}) h_{(3)} = \sum h_{(1)} a \epsilon(h_{(2)})= h a$, hence the formula for the product above is a tautology: $aha'h' = a(h_{(1)}\triangleright a') h_{(2)} h'$.  

Similarly, given a right Hopf action of $H$ on $A$, one defines the crossed product algebra $H\sharp A$ whose underlying space is $H\otimes A$. The left and right versions are isomorphic if $H$ has an invertible antipode; this extends the correspondence between the left and right actions obtained by composing with the antipode map. 

There is also a more general cocycled crossed product. 

[[!redirects smash product algebra]]