A __generator__ in a category $C$ is an object $S$ such that the functor $h^S = C(S,-) : C\to\mathrm{Set}$ is faithful. This means that for any pair $f_1,f_2\in C(X,Y)$
there is a morphism $\theta\in C(S,X)$ which distinguishes
them in the sense that $f_1\circ\theta=f_2\circ\theta$.

One often extends this notion to a _generating family_ of objects, which is a small set $\lbrace S_a, a\in A\rbrace$ of objects in $C$ such that the family $C(S_a,-)$ is jointly faithful, that is for any pair $f_1,f_2\in C(X,Y)$
there is an $a\in A$ and a morphism $\theta\in C(S_a,X)$ which distinguishes them in the sense that 
$f_1\circ\theta=f_2\circ\theta$. 

The dual notion is [[cogenerator]].

A standard example of a generator in the category of $R$-modules over a ring $R$ is any free module $R^I$ and $R$ in particular. If a generator is a finitely generated [[projective object]] in the category of $R$-modules, then we say that it is a progenerator. Progenerators are important in classical Morita theory, see [[Morita equivalence]].