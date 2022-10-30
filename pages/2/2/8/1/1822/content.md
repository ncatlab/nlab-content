##Idea##

In the 1920s homology and cohomology were known for simplicial complexes and there were attempts to extend the definitions to first of all compact metric spaces and then more general spaces.  [[Leopold Vietoris]] (1927) came up with a construction and then shortly after Alexandrov and &#268;ech gave a different one involving the nerve that now bears &#268;ech's name. The input of the  two methods is the same, we have a space $X$ and an open cover $\mathcal{U}$ of $X$.

It was noted that all the calculations of Vietoris homology gave the same answer as  &#268;ech homology.  In 1952, C. H. Dowker showed why.  His result is a beautiful mix of  abstraction and concrete explicit calculation (and is not that well known unfortunately). 

First some abstraction:

We take the set $X$ and the open cover $\mathcal{U}, together with the relation $x\in U$, i.e. an element $x4 will be considered to be _related to_ the set $U$ in the cover $\mathcal{U}$, if it is an element of it!

We replace this by an abstract setting of a set $X$, another set $Y$ and a relation $R\subseteq X\times Y$, from $X$ to $Y$. 

+--{: .query}
Thinks: does what follows have a good generalisation to spans?
=--

##Definition:## 
The **Vietoris complex** of a relation $R$, as above,  is the [[simplicial complex]] specified by
 
* Vertex set: the set of vertices is the set $X$;

* Simplices : a $p$-simplex of $K$ is a set $\{x_0, \ldots, x_p\}  \subseteq X$ such that there is some $y \in Y$ with $x_i Ry$ for $i  = 0, 1, \ldots, p$ 

The Vietoris complex of $R$ will be denoted $V(R)$.

The special, and original, case where $R$ comes from an open cover $\mathcal{U}$ of $X$ will be denoted $V(X,\mathcal{U})$ or simply $V(\mathcal{U})$ and will be called the _Vietoris complex of the open covering $\mathcal{U}$_. 
