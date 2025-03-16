We here discuss homological dimensions of rings and abelian categories: projective, injective and global dimensions. 

## Definitions 

If $C$ is an [[abelian category]] (usually assumed with enough projectives), and $M$ an object in $C$, then its __projective dimension__ $pd(M)$ is the minimal integer $n$ (if it exists) such that there is a resolution of $M$ by [[projective object]]s of length $n$, that is the exact sequence of the form
$$
0\to P_n\to P_{n-1}\to\cdots\to P_1\to P_0\to M\to 0
$$
where $P_n,\ldots,P_1,P_0$ are [[projective object]]s in $C$.

An important identity involving the projective dimension of a module of finite projective dimension over a commutative Noetherian local ring is the [[Auslander-Buchsbaum formula]].

Dually, we define the injective dimension of $M$. 

Id $R$ is a ring then both the category of all right $R$-modules and the category of all left $R$-modules have enough projectives. The left (right) __global dimension__ of $R$ is the supremum of projective dimensions of all left (right) $R$-modules. More generally, a __global dimension of an abelian category__ $C$ may be defined as
$$
gl.dim(C) := sup\{ i\geq 0\,|\, \exists M,N\in C,\, Ext^i(M,N) = 0\}
$$
Thus the left (right) global dimension of a ring $R$ is the global dimension of the category of left (right) $R$-modules. 

See also [[global dimension theorem]].

category: algebra

[[!redirects injective dimension]]
[[!redirects global dimension]]