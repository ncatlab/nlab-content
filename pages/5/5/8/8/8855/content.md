A left (right) __corepresentation__ is a synonym for a left (right) [[coaction]] of a coalgebra (comonoid) in one of the monoidal categories which have linear, and possibly, functional connotation; e.g. in the context of topological vector spaces. 

There is however also another meaning of a corepresentation for a [[Leibniz algebra]].

Both a representation and a corepresentation of a right Leibniz $k$-algebra $\mathfrak{g}$ involve a $k$-module $M$ and two $k$-linear maps "actions" $M\otimes\mathfrak{g}\to M$ and $\mathfrak{g}\otimes M\to M$ with 3 axioms. 

For representations:

$$[m, [x, y]] = [[m, x], y] - [[m, y], x]$$
$$[x, [a, y]] = [[x, m], y] - [[x, y], m]$$
$$[x, [y, m]] = [[x, y], m] - [[x, m], y]$$

for $x,y\in\mathfrak{g}$ and for $m\in M$. 

For corepresentations:

$$[[x, y], m] = [x, [y, m]] - [y, [x, m]] $$
$$[y, [a, x]] = [[y, m], x] - [m, [x, y]] $$
$$[[m, x], y] = [m, [x, y]] - [[y, m], x].$$

If the two "actions" are symmetric, i.e. $[x,m] + [m,x] = 0$ for all $m\in M$, $x\in\mathfrak{g}$ then all the 6 axioms of representation or corepresentation are equivalent. If $M$ is underlying a Leibniz algebra then an action of $\mathfrak{g}$ on $M$ is by definition symmetric, hence all the 6 equivalent conditions hold. 

