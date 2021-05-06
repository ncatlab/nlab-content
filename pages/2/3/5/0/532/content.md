+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

##Idea

A **simplicial T-complex** is  a [[Kan complex]] equipped with a _choice_ of [[horn]] fillers, which satisfy certain 'equations'. It is thus a special case of an [[algebraic Kan complex]].  

There is quite a difference between the [[Kan complex]] structure

1. of the [[nerve|nerve]] $N(\mathcal{G})$  of a [[groupoid]], $\mathcal{G}$, 

1. and that of, say,  a [[path infinity-groupoid|singular complex]] $Sing X$ of some [[topological space]] $X$.  

In the first, if we are given a $(n,i)$-[[horn]], then there is _exactly one_ $n$-simplex in  $Ner(G)$, since the $(n,i)$-horn has a chain of $n$-composable arrows of $G$ in it (at least unless $(n,i) = (2,0)$ or $(2,2)$, which cases are slightly different) and that chain gives the required $n$-simplex.  In other words, there is a 'canonical' filler for any horn.  In $Sing(X)$,  there will usually be many fillers; however the fact that this simplicial set is Kan is a property of retractions on standard simplices, and is not specifically a property of the space $X$ - that is the basic intuition. 

Abstracting, in part, from this idea, Brown and Higgins developed the idea of a [[cubical T-complex]]. This was a [[cubical set|cubical set]] with in each dimension $n$,  a subset of the $n$-[[cube]]s being declared _'thin'_. The term was adopted to indicate that they, somehow, were of lower dimension than they looked to be.  The theory was initiated in a simplicial context in the 1977 Bangor thesis of Keith Dakin listed below, and used by Brown and Higgins who showed that cubical $T$-complexes were equivalent to  [[crossed complex|crossed complexes]].  The corresponding simplicial $T$-complex theory was further developed in the 1978  Bangor thesis of  Nick Ashley, (see below for publication).

##Simplicial $T$-complex: the definition

+--{: .un_defn}
######Definition######
A _simplicial $T$-complex_ is a pair $(K,T)$, 
where $K$ is a [[simplicial set|simplicial set]] and $T = (T_n)_{n\geq 1}$ is a graded subset of
$K$ with $T_n\subseteq  K_n$.  Elements of $T$ are called _[[thin]]_.  The
thin structure satisfies the following axioms:

* Every degenerate element is thin.
* Every [[horn]] in $K$ has a unique thin filler.
* If all faces but one of a thin element are thin, then so also is the remaining face.
=--

+--{: .un_ex}
######Examples######
1. A closely related idea is that of  [[group T-complex]]. Group $T$-complexes form a category equivalent to reduced [[crossed complex]]es.  Any group $T$-complex has an underlying simplicial set, which is a simplicial $T$-complex.

1. The nerve of a [[crossed complex]] has a natural T-complex structure. In a bit more detail, if $\mathsf{C}$ is a crossed complex, its nerve is given by $Ner(\mathsf{C})_n = Crs(\pi(n),\mathsf{C})$, where $\pi(n)$ is the free crossed complex on the $n$-simplex, $\Delta[n]$. This singular complex description shows that if we have an $n$-simplex $f : \pi(n) \to \mathsf{C}$, and declare it to be \emph{thin} if the image $f(\iota_n)$ of the top dimensional generator in $\pi(n)$ is trivial, then the resulting collection of thin simplices determines  a $T$- complex structure on the nerve.
=--

### Results

* Simplical $T$-complexes together with maps between them which preserve 'thinness' form a category that is equivalent to that of [[crossed complexes]] and thus to strict $\infty$-groupoids. The uniqueness of the thin filler is exactly what gives a definite composition in the model. 



## Related concepts

* [[T-complex]]

  * **simplicial $T$-complex**

  * [[cubical T-complex]]

  * [[group T-complex]]

* [[algebraic Kan complex]]

Together with very similar ideas of [[John Roberts]], adapted by 
[[Ross Street]], the notion of $T$-complex is one of the precursors of [[Dominic Verity]]'s notion of [[complicial set|complicial set]].

They are also related to [[Jack Duskin]]'s notion of [[hypergroupoid]]. (The connection is explored in the papers by Nan Tie listed below.)

##References

Relevant references for simplicial T-complexes include:

* [[Ronnie Brown]], _An Introduction to simplicial T-complexes_,  [Esquisses Math. 32 (1983) Part 1](http://ehres.pagesperso-orange.fr/Cahiers/brownem32.pdf)

* M.K. Dakin, _Kan complexes and multiple groupoid structures_, Ph.D Thesis, University of Wales, Bangor, 1977. [Esquisses Math. (1983) 32 Part 2](http://ehres.pagesperso-orange.fr/Cahiers/dakinEM.pdf)

* N. Ashley, _Simplicial T-Complexes: a non abelian version of a theorem of Dold-Kan_, Ph.D Thesis University of Wales, Bangor, 1978; [Dissertationes Math., 165, (1989), 11 &#8211; 58](https://eudml.org/doc/268359).
[Esquisses Math. (1983)  32 Part 3](http://ehres.pagesperso-orange.fr/Cahiers/AshleyEM32.pdf)

* G. Nan Tie, _A Dold-Kan theorem for crossed complexes_, J. Pure Appl. Alg., 56, (1989.), 177 -&#8211; 194. 

* G. Nan Tie, _Iterated W and T-groupoids_, J. Pure Appl. Alg., 56, (1989), 195 -&#8211; 209.

* [[Ronnie Brown]],  and [[P.J. Higgins]], _On the algebra of cubes_
J. Pure Appl. Algebra 21 (1981) 233--260.

* R. Brown,  and P.J. Higgins, _The equivalence of $\omega $-groupoids and cubical   $T$-complexes_ Cahiers Topologie G\'eom. Diff\'erentielle 22 (1981) 349--370.



[[!redirects simplical T-complex]]
[[!redirects simplicial T-complexes]]