
#Contents#
* automatic table of contents goes here
{:toc}

##Idea

There is quite a difference between the [[Kan complex]] structure of the [[nerve|nerve]] of a [[groupoid]], $G$, and that of, say,  a singular complex.  In the first, if we are given a $(n,i)$-[[horn]], then there is _exactly one_ $n$-simplex in  $Ner(G)$, since the $(n,i)$-horn has a chain of $n$-composable arrows of $G$ in it (at least unless $(n,i) = (2,0)$ or $(2,2)$, which cases are slightly different) and that chain gives the required $n$-simplex.  In other words, there is a 'canonical' filler for any horn.  In $Sing(X)$,  there will usually be many fillers.

Abstracting from this idea, Brown and Higgins developed the idea of a [[cubical T-complex]]. This was a [[cubical set|cubical set]] with in each dimension $n$,  a subset of the $n$-[[cube]]s being declared _'thin'_. The term was adopted to indicate that they, somehow, were of lower dimension than they looked to be.  The theory was initially developed in the thesis of Keith Dakin in a simplicial context, and used by Brown and Higgins who showed that cubical $T$-complexes were equivalent to  [[crossed complex|crossed complexes]].  The corresponding simplicial $T$-complex theory was developed in another thesis, this time by Nick Ashley, (see below).



##Definition

A _simplicial $T$-complex_ is a pair $(K,T)$, 
where $K$ is a [[simplicial set|simplicial set]] and $T = (T_n)_{n\geq 1}$ is a graded subset of
$K$ with $T_n\subseteq  K_n$.  Elements of $T$ are called _thin_.  The
thin structure satisfies the following axioms:

* Every degenerate element is thin.
* Every [[horn]] in $K$ has a unique thin filler.
* A thin filler of a thin box also has its last face thin.


##Remarks

1. Together with very similar ideas of John Roberts, adapted by Ross Street, the notion of $T$-complex is one of the precursors of Verity's notion of [[complicial set|complicial set]].

1. A closely related idea is that of  [[group T-complex]].

1.  Relevant references for simplicial T-complexes include:

* N. Ashley, _Simplicial T-Complexes: a non abelian version of a theorem of Dold-Kan_, Disser- 
tations Math., 165, (1989), 11 &#8211; 58.

* G. Nan Tie, _A Dold-Kan theorem for crossed complexes_, J. Pure Appl. Alg., 56, (1989.), 177 
&#8211; 194. 29, 37, 146, 254 
* G. Nan Tie, _Iterated W and T-groupoids_, J. Pure Appl. Alg., 56, (1989), 195 &#8211; 209.





[[!redirects simplicial T-complexes]]