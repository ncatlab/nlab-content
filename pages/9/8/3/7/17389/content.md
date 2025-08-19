
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

Every [[CW-complex]] is a [[paracompact Hausdorff space]].

=--

For one textbook explanation, see e.g. [Fritsch-Piccinini 90, theorem 1.3.5](#FritschPiccinini90). Below we give a somewhat more [[category theory|categorically]] minded proof, linking to relevant results elsewhere in the [[nLab]]. 

+-- {: .proof} 
###### Proof 
Let $X_n$ denote the $n^{th}$ [[skeleton]] of $X$. We argue by [[induction]] that each skeleton is a paracompact Hausdorff space. Vacuously $X_{-1} = \emptyset$ is a paracompact Hausdorff space. Now suppose $X_{n-1}$ is a paracompact Hausdorff space, and suppose $X_n$ is formed as an [[attachment space]] with attaching map $f: \sum_{i \in I} S_i^{n-1} \to X_{n-1}$, so that 

$$\array{
\sum_{i \in I} S_i^{n-1} & \stackrel{\;h\;}{\hookrightarrow} & \sum_{i \in I} D_i^{n} \\ 
\mathllap{f} \big\downarrow & {}^{{}_{(po)}} & \big\downarrow \mathrlap{g} \\ 
X_{n-1} & \underset{\;k\;}{\hookrightarrow} & X_n
}$$ 

is a pushout square. The embedding $h$ is a closed embedding, and so its pushout along $f$ [is a closed embedding](/nlab/show/subspace+topology#pushout) $k$. Furthermore, the spheres $S_i^{n-1}$ and disks $D_i^n$ are paracompact Hausdorff spaes since they are compact Hausdorff, and [paracompact Hausdorff spaces are closed under coproducts](https://ncatlab.org/nlab/show/paracompact+topological+space#ParacompactnessPreservedByDisjointUnion), making $h$ a closed embedding of paracompact Hausdorff spaces. By the result on [pushouts of closed embeddings of paracompact Hausdorff spaces](/nlab/show/colimits+of+paracompact+Hausdorff+spaces#ClosedEmbeddingsOfParacompactaClosedUnderPushout), it now follows that $X_n$ is a paracompact Hausdorff space. 

Thus the CW-complex $X$ is a colimit of a sequence of closed embeddings 

$$X_{-1} \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \ldots$$ 

between paracompact Hausdorff spaces. [It follows that this colimit is a paracompact Hausdorff space](/nlab/show/colimits+of+paracompact+Hausdorff+spaces#ColimitsOfSequencesOfParacompacta). 
=-- 


## Related statements

* [[Hausdorff implies sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

## References
 {#References}

That every CW complexes is [[Hausdorff space|Hausdorff]] (in fact [[normal topological space|normal]]) may be [[folklore]], a proof is spelled out in:

* {#Hatcher02} [[Allen Hatcher]], Prop. A.3 of *Algebraic Topology*, Cambridge University Press 2002 ([ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html))

An early original article with the paracompactness statement is:

* {#Miyazaki52} Hiroshi Miyazaki, _The paracompactness of CW-complexes_, Tohoku Math. J. (2) Volume 4, Number 3 (1952), 309-313. 1952 [Euclid](https://projecteuclid.org/euclid.tmj/1178245380)

Textbook account:

* {#FritschPiccinini90} [[Rudolf Fritsch]], [[Renzo Piccinini]], Theorem 1.3.5 (p. 29 and following) of: _Cellular structures in topology_, Cambridge University Press (1990) ([doi:10.1017/CBO9780511983948](https://doi.org/10.1017/CBO9780511983948), [pdf](https://epub.ub.uni-muenchen.de/4493/1/4493.pdf))

[[!redirects every CW-complex is a Hausdorff space]]
[[!redirects every CW-complex is a Hausdorff topological space]]

[[!redirects CW-complexes are Hausdorff spaces]]
[[!redirects CW-complexes are Hausdorff]]
[[!redirects a CW-complex is a Hausdorff space]]


[[!redirects CW-complexes are paracompact]]
[[!redirects CW-complexes are paracompact spaces]]
[[!redirects CW-complexes are paracompact topological spaces]]
