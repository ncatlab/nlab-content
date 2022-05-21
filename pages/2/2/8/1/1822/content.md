
#Contents#
* table of contents
{:toc}

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
In fact each relation will give **two** simplicial complexes, one as above, the other obtained by reversing the roles of $X$ and $Y$ in the above. In other words, in the usual way define the _[[opposite relation]]_ by ' $R^{op}\subseteq Y\times X$ is the relation in which $yR^{op}x$ if and only if $xRy$'.

We define $C(R) = V(R^{op})$ and call it the **&#268;ech nerve** or **&#268;ech complex** of the relation $R$.

If we look at this in the case of the relation coming from a space $X$ and an open covers $\mathcal{U}$ you get exactly the nerve of $\mathcal{U}$ as discussed in [[Čech methods]]. 

There are natural questions that arise here. One is how to turn these [[simplicial complexes]] into [[simplicial sets]], to which _one_
 reply is take a total order (or at least pick a partial order that any simplex is ordered in that partial order; another reply would be to take each $n$-simplex $(n+1)!$-times, one for each possible order. 


Another obvious question is to compare $V(R)$ and $C(R)$: are they closely related?  That is discussed more in [[Dowker's Theorem]].  It looks very much a situation for a combinatorial duality result.

A final question (and one I can answer!) is: are there useful applications of this construction other than in (co)homology.  The answer is most decidedly 'yes'.  

##Volodin spaces

One of the ways of constructing the [[algebraic K-theory]] of a ring $R$ is to construct a simplicial set / complex from the stable [[general linear group]] and the family of cosets of subgroups of upper triangular matrices. (This method is due to _[[I.A. Volodin]].)

The method can be applied to other groups with given families of subgroups as is described at [[Volodin spaces]].  It uses the cosets of the subgroups in the family to get a covering of the set of elements and then applies the Vietoris construction (but without mention of that source).  

##Higher generation by subgroups

It is notable that the same situation  but with corresponding &#268;ech complex is used by Abels and Holz, (1993) for the calculation of syzygies and is applied to various settings with linear groups.  They give induction methods for homological finiteness criteria for the groups.  This is discussed in more detail in [[higher generation by subgroups]].

##'Hidden Stasheff polytopes ... '

Kapranov and Saito have studied the syzygies of the usual presentation of the Steinberg group. These are expected to give a combinatorial construction of the classifying space for the algebraic K-theory of rings. They use Volodin's construction but their combinatorial construction would seem to be related to that of Abels and Holz. They conjecture various results in this. but there is still some mystery about what results have been proved, beyond those published in their paper.


##Gavin Wraith's puzzle##

Gavin Wraith posted a puzzle on the $n$Caf&#233; whose solution uses the fact that the simplicial complexes $V(R)$ and $C(R)$ are homotopy equivalent:

* [A Puzzle From Gavin Wraith](http://golem.ph.utexas.edu/category/2009/07/a_puzzle_from_gavin_wraith.html)

Perhaps this fact is [[Dowker's Theorem]]?

## Related concepts

* [[persistent homotopy]]

## References

Discussion in [[persistent homotopy theory]]:

* [[J. F. Jardine]], *Data and homotopy types* $[$[arXiv:1908.06323](https://arxiv.org/abs/1908.06323)$]$

See also:

* Wikipedia, *[Vietoris-Rips complex](https://en.wikipedia.org/wiki/Vietoris–Rips_complex)*

* [[I. Volodin]], _Algebraic K-theory as extraordinary homology theory on the category of associative  rings with unity_, Izv. Akad. Nauk. SSSR, 35, (Translation: Math. USSR Izvestija Vol. 5 (1971) 
No. 4, 859-887).

* H. Abels and S. Holz, _Higher generation by subgroups_, J. Alg, 160, (1993), 311&#8211; 341

*  M. Kapranov and M. Saito, 1999, Hidden Stasheff polytopes in algebraic K-theory and in the  space of Morse functions , in Higher homotopy structure in topology and mathematical physics 
(Poughkeepsie, N.Y. 1996) , volume 227 of Contemporary Mathematics , 191&#8211;225, AMS.

[[!redirects Vietoris-Rips complex]]
