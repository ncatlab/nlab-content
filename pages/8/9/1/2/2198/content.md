In addition to the [[topological spaces]] some other structures can be used to found the topological reasoning on sets, including [[uniform spaces]] and nearness spaces.

A __nearness structre__ on a set $X$, or a __nearness relation__ on $P(X)$, is a relation $\delta$ on the power set $P(X)$ of subsets of $X$ such that 

(P1) $A\delta B$ iff $B\delta A$

(P2) $A\delta(B\cup C)$  iff either $A\delta B$ or $A\delta C$

(P3) $\{x\}\delta\{y\}$ iff $x=y$

(P4) It is never true that $\emptyset \delta X$

(P5) If it is not true that $A\delta B$ then there are $C,D\subet X$ such that $C\cup D=X$ and neither $A\delta C$ nor $B\delta D$.

A __nearness space__ is a set $X$ equipped with a nearness relation $\delta$. 

If $(X,\tau)$ is a Tihonov (=completely regular) topological space, then for any $A,B\subset X$ set $A\delta V$ iff $A\neq \emptyset\neq B$ and there is no continuous function $:X\to I=[0,1]$ such that $f(x)=0$ on $A$ and $f(x)=1$ on $B$. This defines a nearness relation,

If $U$ is a uniformity on $Y$ (making it into a uniform space) then for all $A,B\subset Y$ set $A\delta B$ iff $V\cap (A\times B)\neq \emptyset$ for all $V\in U$. This also defines a nearness relation on $Y$. The topology induced by the uniformity and the topology induced by the nearness relation are the same.

See R. Engelking, __General topology__, chapter 8.