##Idea##

There is quite a difference between the Kan complex structure of the [[nerve|nerve]] of a groupoid, $G$, and that of, say,  a singular complex.  In the first, if we are given a $(n,i)$-horn, then there is _exactly one_ $n$-simplex in  $Ner(G)$, since the $(n,i)$-horn has a chain of $n$-composable arrows of $G$ in it (at least unless $(n,i) = (2,0)$ or $(2,2)$, which cases are slightly different) and that chain gives the required $n$-simplex.  In other words, there is a 'canonical' filler for any horn.  In $Sing(X)$,  there will usually be many fillers.

Abstracting from this idea, Brown and Higgins developed the idea of a cubical $T$-complex. this was a [[cubical set|cubical set]] with in each dimension $n$,  a subset of the $n$-cubes being declared _'thin'_. The term was adopted to indicate that they, somehow, were of lower dimension that they looked to be.  The theory was initially deveoled in the thesis of Keith Dakin, and used by Brown and Higgins who showed that  a cubical $T$ complex was equivalent to a [[crossed complex|crossed complex]].  The corresponding simplicial theory was developed in another thesis, this time by Nick Ashley.


##Definition##

A _simplicial $T$-complex_ is of a pair $(K,T)$, 
where $K$ is a [[simplicial set|simplicial set]] and $T = (T_n)_{n\geq 1}$ is a graded subset of
$K$ with $T_n\subseteq  K_n$.  Elements of $T$ are called _thin_.  The
thin structure satisfies the following axioms:

* Every degenerate element is thin.
* Every horn in $K$ has a unique thin filler.
* A thin filler of a thin box also has its last face thin.


##Remark##

1. Together with very similar ideas of John Roberts, adapted by Ross Street, the notion of $T$ complex is one of the precursors of Verity's notion of [[complicial set|complicial set]].

1. Cubical $T$ complexes are also a key concept in the long series of articles by  Brown and Higgins on [[strict omega-groupoid|strict omega-groupoids]] on. For instance

* Brown, Higgins, _The equivalence of $\omega$-groupoids and cubical $T$-complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 349-370  ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_349_0/CTGDC_1981__22_4_349_0.pdf)).

and generally

* Ronald Brown, Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html)).

 A closely related idea is that of  [[group T - complex|group T - complex]].