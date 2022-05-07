
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Statement and Proof

+-- {: .num_prop }
###### Proposition

Every [[CW-complex]] is a *paracompactum*, i.e., a [[paracompact Hausdorff space]].

=--

For one textbook explanation, see e.g. [Fritsch-Piccinini 90, theorem 1.3.5](#FritschPiccinini90). Below we give a somewhat more [[category theory|categorically]] minded proof, linking to relevant results elsewhere in the [[nLab]]. 

+-- {: .proof} 
###### Proof 
Let $X_n$ denote the $n^{th}$ skeleton of $X$. We argue by [[induction]] that each skeleton is a paracompactum. Vacuously $X_{-1} = \emptyset$ is a paracompactum. Now suppose $X_{n-1}$ is a paracompactum, and suppose $X_n$ is formed as an [[attachment space]] with attaching map $f: \sum_{i \in I} S_i^{n-1} \to X_{n-1}$, so that 

$$\array{
\sum_{i \in I} S_i^{n-1} & \stackrel{\;h\;}{\hookrightarrow} & \sum_{i \in I} D_i^{n} \\ 
\mathllap{f} \big\downarrow & {}^{{}_{(po)}} & \big\downarrow \mathrlap{g} \\ 
X_{n-1} & \underset{\;k\;}{\hookrightarrow} & X_n
}$$ 

is a pushout square. The embedding $h$ is a closed embedding, and so its pushout along $f$ [is a closed embedding](/nlab/show/subspace+topology#pushout) $k$. Furthermore, the spheres $S_i^{n-1}$ and disks $D_i^n$ are paracompacta since they are compact Hausdorff, and [coproducts of paracompacta are again paracompacta](https://ncatlab.org/nlab/show/paracompact+topological+space#ParacompactnessPreservedByDisjointUnion), making $h$ a closed embedding of paracompact Hausdorff spaces. By the result on [pushouts of closed embeddings of paracompacta](/nlab/show/colimits+of+paracompact+Hausdorff+spaces#ClosedEmbeddingsOfParacompactaClosedUnderPushout), it now follows that $X_n$ is a paracompactum. 

Thus the CW-complex $X$ is a colimit of a sequence of closed embeddings 

$$X_{-1} \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \ldots$$ 

between paracompacta. [It follows that this colimit is a paracompactum](/nlab/show/colimits+of+paracompact+Hausdorff+spaces#ColimitsOfSequencesOfParacompacta). 
=-- 


## Related statements

* [[Hausdorff implies sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

## References

An early original article with the statement is

* {#Miyazaki52} Hiroshi Miyazaki, _The paracompactness of CW-complexes_, Tohoku Math. J. (2) Volume 4, Number 3 (1952), 309-313. 1952 [Euclid](https://projecteuclid.org/euclid.tmj/1178245380)

Textbook accounts include

* {#FritschPiccinini90} [[Rudolf Fritsch]], Renzo Piccinini, Theorem 1.3.5 (p. 29 and following) of _Cellular structures in topology_, Cambridge University Press (1990)

[[!redirects every CW-complex is a Hausdorff space]]
[[!redirects every CW-complex is a Hausdorff topological space]]

[[!redirects CW-complexes are Hausdorff spaces]]
[[!redirects CW-complexes are Hausdorff]]
[[!redirects a CW-complex is a Hausdorff space]]


[[!redirects CW-complexes are paracompact]]
[[!redirects CW-complexes are paracompact spaces]]
[[!redirects CW-complexes are paracompact topological spaces]]
