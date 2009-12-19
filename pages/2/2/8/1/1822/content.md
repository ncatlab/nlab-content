##Idea##

In the 1920s homology and cohomology were known for simplicial complexes and there were attempts to extend the definitions to first of all compact metric spaces and then more general spaces.  [[Leopold Vietoris]] (1927) came up with a construction and then shortly after Alexandrov and &#268;ech gave a different one involving [[Čech nerve|the nerve that now bears Čech's name]]. The input of the  two methods is the same, we have a space $X$ and an open cover $\mathcal{U}$ of $X$.

It was noted that all the calculations of Vietoris homology gave the same answer as  &#268;ech homology.  In 1952, C. H. Dowker showed why.  His [[Dowker's theorem|result]] is a beautiful mix of  abstraction and concrete explicit calculation (and is not that well known unfortunately). 

First some abstraction:
*  We take the set $X$ and the open cover $\mathcal{U}$, together with the relation $x\in U$, i.e. an element $x$ will be considered to be _related to_ the set $U$ in the cover $\mathcal{U}$, if it is an element of it!
*  We replace this by an abstract setting of a set $X$, another set $Y$ and a relation $R\subseteq X\times Y$, from $X$ to $Y$. 

+--{: .query}
Thinks: does what follows have a good generalisation to [[spans]]?
=--


##Definition:## 
The **Vietoris complex** of a relation $R$, as above,  is the [[simplicial complex]] specified by
* Vertex set: the set of vertices is the set $X$;
* Simplices : a $p$-simplex of $K$ is a set $\{x_0, \ldots, x_p\}  \subseteq X$ such that there is some $y \in Y$ with $x_i Ry$ for $i  = 0, 1, \ldots, p$ 

The Vietoris complex of $R$ will be denoted $V(R)$.

The special, and original, case where $R$ comes from an open cover $\mathcal{U}$ of $X$ will be denoted $V(X,\mathcal{U})$ or simply $V(\mathcal{U})$ and will be called the _Vietoris complex of the open covering $\mathcal{U}$_. 


##Remarks## 
In fact each relation will give **two** simplicial complexes, one as above, the other obtained by reversing the roles of $X$ and $Y$ in the above. In other words, in the usual way define the _[[opposite relation]]_ by '$R^{op}\subseteq Y\times X$ is the relation in which $yR^{op}x$ if and only if $xRy$'.

We define $C(R) = V(R^{op})$ and call it the **&#268;ech nerve** or **&#268;ech complex** of the relation $R$.

If we look at this in the case of the relation coming from a space $X$ and an open covers $\mathcal{U}$ you get exactly the nerve of $\mathcal{U}$ as discussed in [[Čech methods]]. 

There are natural questions that arise here. One is how to turn these [[simplicial complexes]] into [[simplicial sets]], to which one reply is take a total order (or at least pick a partial order that any simplex is ordered in that partial order; another reply would be to take each $n$-simplex $(n+1)!$-times, one for each possible order. 

+--{: .query} 
[[Tim]]: I am not sure what happens to the homotopy types.  It may be they both give the same. Mostly people take the total order way out, but that feels a bit [[evil]]!
=--

Another obvious question is to compare $V(R)$ and $C(R)$: are they closely related?  That is discussed more in [[Dowker's Theorem]].  It looks very much a situation for a combinatorial duality result.

A final question (and one I can answer!) is: are there useful applications of this construction other than in (co)homology.  The answer is most decidedly 'yes'.  

(More to be added later.)

##Gavin Wraith's puzzle##

Gavin Wraith posted a puzzle on the $n$Caf&#233; whose solution uses the fact that the simplicial complexes $V(R)$ and $C(R)$ are homotopy equivalent:

* [A Puzzle From Gavin Wraith](http://golem.ph.utexas.edu/category/2009/07/a_puzzle_from_gavin_wraith.html)

Perhaps this fact is [[Dowker's Theorem]]?