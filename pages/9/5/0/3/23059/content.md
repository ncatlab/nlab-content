##Idea

A lattice ordered group is a group which is also a lattice in a compatible way.

##Partially ordered groups.
 
 First we introduce _partially ordered groups_. 

A group $G$ is said to be _partially ordered_ if it is equipped with a partial order, $\le$, which is compatible with the group multiplication, $\cdot$, so, if $g\leq h$ then $g\cdot k\leq h\cdot k$ and also $k\cdot g\leq k\cdot h$ for any $g,h,k \in G$.

##Positive elements

The set, $G^+=\{g\in G\mid g\geq 1\}$ is called the _positive cone_ of $(G,\leq)$. It completely determines the partial order since $g\leq h$ if and only if $hg^{-1}\in G^*\cup \{0\}$.

##Lattice ordered groups.

If $G,\leq)$ is a partially ordered group, and the partial order is a lattice, then we say $G$ is a _lattice ordered group_, so for each pair , $a,b$ in $G$ has a [[join]], $a \vee b$ and a [[meet]], $a\wedge b$.

Many sources abbreviate 'lattice ordered group' to '$\ell$-group'.

##Properties 

* The group operation distibutes over both $\vee$ and $\wedge$.

* Inversion reverses the order so it $g\le h$, then $h^{-1}\leq g^{-1}$. (It is worth noting that this property is the opposite of that encountered with [[ordered groupoid]]s.)

* A sort of de Morgan's law holds, so $(a\vee b)^{-1}= a^{-1}\wedge b^{-1}$. This is easily proved once one notes that inversion reverses the order.

* The compatibility of the group multiplication with the lattice structure interpretas as saying that left and right multiplication by elements of the group give automorphisms of the lattice structure.

## Lattice ordered groups and residuated lattices

We note that given any $x, y \in G$, we can form $x / y = x\cdot y^{-1}$, and $y\backslash x = y^{-1}\cdot x$. In this case, if $x\cdot y \leq z$, then, of course, $y\leq x\backslash z$ and $x\leq z / y$.  We then also have $x^{-1}= 1 / x$ - which is neat!

This gives that any lattice ordered group gives a [[residuated lattice]].

##References
The original article that considered ordered groups in the non-commutative case is by Garrett Birkhoff:

* [[Garrett Birkhoff]]. _Lattice-ordered groups,_ Annals of Math. 43, (1942) pp. 298 - 331.

He later considered Lattice-ordered Lie groups.

There are several monographs or books on the subject of lattice ordered groups.

* Marlow Anderson and Todd Feil, _Lattice Ordered Groups: An Introduction,_ Reidel, Springer Science & Business Media, 6 Dec 2012. 

* V. M. Kopytov, N. Ya. Medvedev, The Theory of Lattice-Ordered Groups,  Mathematics and Its Applications, volume 307, Springer, [doi](https://doi.org/10.1007/978-94-015-8304-6).

