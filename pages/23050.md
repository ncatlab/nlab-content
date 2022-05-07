



##Definition

A _residuated lattice_ is an algebra, $L=(L,\wedge,\vee, \cdot, \backslash, /,1)$ such that

* $(L,\wedge,\vee)$ is a lattice;

* $(L,\cdot,1)$ is a monoid;

* for all $a,b,c\in L$,

$$(ab\le c)\Leftrightarrow (b\le a \backslash c)\Leftrightarrow (a\le c / b).$$

##Examples

* Let $(M,\cdot, e)$ be a monoid and consider $L=\mathcal{P}(M)$.

If $X, Y\subseteq M$, define 

$$X\cdot Y=\{x\cdot y\mid x\in X, y\in Y\};$$

$$X\backslash Y = \{z\in M\mid X\cdot\{z\}\subseteq Y\};$$

$$Y/ X= \{z\in M\mid \{z\}\cdot X\subseteq Y\}.$$

Then $L$ with this structure is a residuated lattice. 

* A special instance if this is with the quantale of ideals in a ring, $R$; see [[ideals in a monoid]] and [[quantale]], especially the section on examples.

* For any set, $X$, the relation algebra, $Rel(X)=\mathcal{P}(X\times X)$ of binary relations on $X$ is a residuated lattice.

Writing $R^-$ for the complement of a relation, $R$, and $R;S$ for the relational composition of two relations, $R$ and $S$, we define

$R \backslash S = (R;S^-)^- ,$ 

$S / R = (S^-;R)^- $

and

 $R\to S= (R\cap S^-)^- = R^-\cup S.$

We have

* $(Rel(X), \cap,\cup,\to, \emptyset, X^2)$ is a Boolean algebra,

*  $(Rel(X), ; \Delta)$ is a monad, where $\Delta$ is the diagonal / equality relation;

* the residuation relation is satisfied:

$$((R;S)\subseteq T)\Leftrightarrow (S\subseteq (R\backslash T))\Leftrightarrow (R\subseteq T / S)).$$

##Related entries

* [[residual]]

* [[quantale]]

* [[idempotent semiring]]

* [[residuated morphism]]

##References

A classical reference is 

* M. Ward and R. P. Dilworth, _Residuated Lattices_,  Transactions of the American Mathematical Society, Vol. 45, No. 3 (May, 1939), pp. 335-354.[doi.org/10.2307/1990008 ](https://doi.org/10.2307/1990008 ) 

A set of slides from a modern treatment is 

* Nikolaos Galatos, _Residuated lattices_, [slides](https://www2.karlin.mff.cuni.cz/~ssaos/2008/ResiduatedLatticesTutorial.pdf)