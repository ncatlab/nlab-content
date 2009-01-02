#Idea#

A [[presheaf]] can be regarded as an assignment of "sets of structures to [[space and quantity|spaces]]", such that these structures can be pulled back along maps of spaces. A presheaf is a _sheaf_ if this assignment satisfies [[descent and codescent|descent]]: if $\pi: Y \to X$ is a _cover_ of a space $X$ by a space $Y$, then the collection of structures assigned to $X$ is isomorphic to the collection of structures assigned to $Y$ which _glue_ and hence [[descent and codescent|descent]] from $Y$ down to $X$.


#Definition#

Given a [[site]] $(C, J)$, a _sheaf_ over that site is a [[presheaf]] 

$$X: C^{op} \to Set$$ 

such that whenever $i: F \hookrightarrow \hom(-, c)$ is a covering sieve, the map 

$$X(c) \stackrel{Yoneda}{\cong} Set^{C^{op}}(\hom(-, c), X) \stackrel{Set^{C^{op}}(i, X)}{\to} Set^{C^{op}}(F, X)$$ 

is an isomorphism. 


##Remarks##

* The [[vertical categorification|categorifications]] of sheaves are

  * [[stack|stacks]];

  * [[infinity-stack|infinity-stacks]].

* If we read the set $Set^{C^{op}}(F, X)$ as a [[descent and codescent|descent 0-category]] the above isomorphism exhibits the _descent condition_ described at [[infinity-stack]] in a very simple case, namely the case where the $\infty$-stack takes values in "0-categories", namely in [[Set]].


#Examples#

The archetypical example of sheaves are _sheaves of functions_:

* for $X$ a topological space, $\mathbb{C}$ a topological space and $O(X)$ the [[site]] of open subsets of $X$, the assignment $U \mapsto C(U,\mathbb{C})$ of continuous functions from $U$ to $\mathbb{C}$ for every open subset $U \subset X$ is a sheaf on $O(X)$.

* for $X$ a complex manifold and $\mathbb{C}$ a complex manifold, the assignment $U \mapsto C_{hol}{X,\mathbb{C}}$ of holomorphic functions in a sheaf.

