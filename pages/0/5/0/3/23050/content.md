

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

$$Y/ X= \{z\in M\mid \{z\}\cdot X\subseteq Y\}$$

and then $L$ with this structure is a residuated lattice. 

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

* Any [[lattice ordered group]] gives a residuated lattice. This is described in the entry on lattice ordered groups.

##Categorical interpretations of residuation

Looking at the poset structure of $L$ as a category, one rewrites $a\le b$ as $a\to b$ and  $L(a,b)$ for the singleton set consisting just of the morphism $a\to b$.

We have for each element $a$ in $L$, two mappings given by, respectively, left and right multiplication by $a$:

$$\lambda_a:x\mapsto a\cdot x$$
$$\rho_a:x\mapsto x\cdot a.$$

These mappings are order preserving, so give endofunctors on the _category_ $L$.  For instance, suppose $x\le y$ and we have $a\cdot y\leq b$.  We then have $y\leq a/b$, and hence $x\le a/b$, i.e. $a\cdot x\leq b$.  Now take $b= a\cdot y$.  We have thus that $a\cdot x\leq a\cdot y$, as required.

In this interpretation, both these functors have right adjoints, namely the two residuals. We have, for instance,
$$L(\lambda_a(x),c) \cong L(x,a\backslash c).$$
The residual functor, $a\backslash -$, acts like a left exponential object for the left multiplication functor. Likewise $-/a$ acts like a right exponential object functor.

This point of view is explored further in the entry on [[residual]]s.



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