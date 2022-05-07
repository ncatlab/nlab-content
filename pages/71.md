
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

## Idea

_Orientals_ are "oriented simplices": the $n$-th oriental is the [[simplicial set|simplicial]] $n$-[[simplex]] turned into a [[globular set|globular]] simplex, hence equipped with source and target relations, assigning to each $k$-face a set of $(k-1)$-faces called its source and a set of $(k-1)$-faces called its target, subject to some natural axioms. Thus an oriental is a translation from [[simplicial set|simplicial]] to _[[globular set|globular]]_ [[geometric shapes for higher structures]]. (For more discussion of this point see also at _[[Kan complex]]_ the section _[As models for ∞-groupoids](Kan%20complex#AsGrpds)_.)

Each oriental freely generates (see below) a structure of a [[strict omega-category]] $O(\Delta^n)$, such that $k$-morphisms in $O(\Delta^n)$ are [[pasting diagrams]] of $k$-faces in $\Delta^n$.

One of the axioms is a [[globular set|globularity axiom]], which says that the source of a source (that is, the union of sources of all $(k-1)$-faces in the source of a $k$-face) equals the source of the target, and similarly that the target of a source equals the target of the target. Thus, orientals mediate between the [[simplicial set|simplicial]] and the [[globular set|globular]] world of [[higher category theory|infinity-categories]].

The first few orientals look as follows:


$$
\array{\arrayopts{\rowalign{center}}
O(\Delta^0) = & \{ 0\} \\
O(\Delta^1) = & \left\{ 0 \to 1\right\} \\
O(\Delta^2) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta2]]
\end{svg}}
\right\}\\
O(\Delta^3) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta3]]
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta4]]
\end{svg}}
\right\}
}
$$


The construction of orientals is designed to be compatible with face and degeneracy maps. Therefore the orientals arrange themselves into a [[cosimplicial object|cosimplicial]] [[∞-category]], i.e., a functor
$$
  O : \Delta \to \omega Cat
$$
from the [[simplex category]] $\Delta$ to the category of [[strict omega-category|strict omega-categories]].

## Relation to other concepts


### Relation to $\omega$-groupoids

Regarding the standard $n$-simplex as a filtered space with the standard filtering, and denoting for $X$ a filtered space by $\Pi_\omega(X)$ the fundamental filter-respecting $\omega$-groupoid of $X$, we obtain a cosimplicial [[omega-groupoid|omega-groupoid]]

$$
  \Pi_\omega(\Delta^{-})
  :
  \Delta \to \omega Grpd
$$

+-- {: .query}

It should be true that $\Pi_\omega(\Delta^n)$ is the _free $\omega$-groupoid_ on $O(\Delta^n)$. Is that right?

=--

### Relation to cyclic polytopes

There is a convex-geometric perspective on orientals outlined in [Kapranov-Voevodsky](#KapranovVoevodsky)  We will try to explain the punch-line first, then go into details.  

In $O(\Delta^n)$, denote the source of the $n$-morphism corresponding to the $n$-face in $\Delta^n$ by $\hat 0_{n-1}$, and denote its target by $\hat 1_{n-1}$.  Since
these are source and target of the same morphism, they both have the same
source, and both have the same target.  Write $\hat 0_{n-2}$ for this source,
and $\hat 1_{n-2}$ for this target.  Inductively define $\hat 0_k$ and $\hat 1_k$
for all $0\leq k \leq n-1$.  

The promised punchline is that the $(k+1)$-morphisms from $\hat 0_k$ to $\hat 1_k$ are in natural correspondence to the triangulations of the $(k+1)$-dimensional cyclic polytope with $n+1$ vertices.  

For example, when $k=1$, we have $\hat 0_1$ is the 1-[[morphism]] $0\rightarrow 1\rightarrow \dots \rightarrow n$, and $\hat 1_1$ is the 1-morphism $0\rightarrow n$.  The [[2-morphism]]s from $\hat 0_1$ to $\hat 1_1$ consist of [[triangulation]]s of the $(n+1)$-gon.  See the diagrams above for examples.  

#### Details

We are going to embed the [[simplex]] $\Delta^n$ inside $\mathbb {R}^n$, so we can think (convex-)geometrically about it.  

Let is get the main convex-geometric definitions out of the way at the beginning.  

The _moment curve_ in $\mathbb {R}^d$ is defined parametrically by $p(t)=(t,t^2,\dots,t^d)$.  

A _cyclic [[polytope]]_ of [[dimension]] $d$ with $n$ vertices
is the [[convex hull]] of $n$ points on the moment curve in $\mathbb {R}^d$.  For many purposes, the choice of the $n$ points is irrelevant; for example, the face lattice of the polytope does not depend on which points were chosen.  

A _[[triangulation]]_ of a polytope is a subdivision of the polytope into
maximal-dimensional simplices, which overlap only on their boundaries, and 
all of whose vertices are vertices of the original polytope.  

To fix an embedding of $\Delta^n$ into $\mathbb {R}^n$, choose real numbers $a_0\lt a_1\lt\dots\lt a_{n}$, and embed $\Delta^n$ inside $\mathbb {R}^n$ so that its $i$-th vertex is at $p(a_i)$.  

Now, as already described above, we have that $\hat 0_{n-1}$ and $\hat 1_{n-1}$  are compositions of the morphisms corresponding to some $n-1$-faces, so that the morphism  coming from the unique $n$-face of $\Delta_n$ goes from $\hat 0_{n-1}$ to $\hat 1_{n-1}$.  Which faces belong to which $(n-1)$-morphism?  

The answer is very simple: $\hat 0_{n-1}$ is the composition of the _lower_ faces, while $\hat 1_{n-1}$ is the composition of the _upper_ faces, where lower and upper are always taken with respect to the final co-ordinate.  

Now, project into $\mathbb {R}^{n-1}$ by forgetting the last co-ordinate.  The 
image of $\Delta^n$ inside $\mathbb {R}^{n-1}$ is the convex hull of $n+1$ points
on the moment curve in $\mathbb {R}^{n-1}$, that is to say, it is a cyclic polytope
with $n+1$ vertics in dimension $n-1$.  

$\hat 0_{n-2}$ consists of the lower faces of this cyclic polytope (where, as always, we take upper/lower with respect to the final co-ordinate, though note that in this case, the final co-ordinate is the $n-1$-st co-ordinate, since we have already forgotten the $n$-th co-ordinate).  Similarly, $\hat 1_{n-2}$ consists of the upper faces of this cyclic polytope.  

The projections of $\hat 0_{n-1}$ and $\hat 1_{n-1}$, meanwhile, are triangulations
of this cyclic polytope.   The cyclic polytope of dimension $n-1$ with $n+1$ vertices
has only two triangulations, so these are all of them.  

In general, $\hat 0_{k}$ consists of the lower faces of the image of the 
projection of $\Delta_n$ into $\mathbb {R}^{k+1}$ by forgetting the last $n-k+1$ coordinates, while $\hat 1_k$ consists of the upper faces of the image.  And then $\hat 0_{k+1}$, $\hat 1_{k+1}$ correspond to particular triangulations of this image and, indeed, the $(k+1)$-morphisms from $\hat 0_k$ to $\hat 1_k$ correspond bijectively to triangulations of the image (which is a cyclic polytope).  

## Applications
 
### $\omega$-Nerve 

The $\omega$-nerve $N(C)$ of an [[omega-category]] $C$ is a simplicial set which generalizes the [[nerve]] of an ordinary category: the collection of $k$-simplices in $N(C)$ is the collection of images of the $k$-th oriental $O_k$ in $C$, i.e.

$$
  (N(C))_k := Hom_{\omega Cat}(O([k]), C)
  \,.
$$

This naturally extends to a functor

$$
  N : \omega Cat \stackrel{Hom_{\omega Cat}(O([-_2]),-_1)}{\to}
  SimplicialSets
  \,.
$$

The nerve functor is faithful. This means that omega categories can be regarded as simplicial sets equipped with extra structure. The precise nature of this structure was identified by Dominic Verity in terms of [[complicial set]]s in his work on the [Doplicher-Roberts conjecture](http://golem.ph.utexas.edu/string/archives/000711.html). 

### Free $\omega$-Category on a simplicial set

The $\omega$-nerve has a [[adjoint functor|left adjoint]], the free $\omega$category on a simplicial set

$$
  F : SimplicialSets \to \omega Cat
$$

given by the [[end|coend]]

$$
  F(S_\bullet) := \int^{[n] \in \Delta} S_n \cdot
   O([n])
  \,.
$$

(Here one uses that $\omega Cat$ is naturally tensored over $Sets$: the notation $S_n \cdot O([n])$ refers to a coproduct of an $S_n$-indexed collection of copies of $O([n])$. See also [[enriched category theory]].)

Because the nerve functor is faithful, the counit of the adjunction $F \dashv N$, 

$$\varepsilon_C: F N C \to C,$$ 

is an epimorphism for omega categories $C$. 

+-- {: .query}

Is $F$ faithful? It seems to be... If not, how does it fail to be faithful? 

=--

### Descent and codescent

The orientals $O(\Delta^{(n)})$, as well as the $\Pi_\omega(\Delta^{(n)})$ play a central role in the description of [[descent|descent and codescent]] in [[omega-category|omega-categorical terms]].






## References {#lit}

The orientals were introduced in

* [[Ross Street]], _The algebra of oriented simplexes_, J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf), <a href="https://doi.org/10.1016/0022-4049(87)90137-X"></a>).

The link to cyclic polytopes is discussed in

* [[Mikhail Kapranov]] and [[Vladimir Voevodsky]], _Combinatorial-geometric aspects of polycategory theory: pasting schemes and higher Bruhat orders (list of results)_.
International Category Theory Meeting (Bangor, 1989 and Cambridge, 1990).
Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;g. 32 (1991), no. 1, 11&#8211;27.
([pdf](http://archive.numdam.org/article/CTGDC_1991__32_1_11_0.pdf)).
{#KapranovVoevodsky}

The $\omega$-groupoids $\Pi_\omega(\Delta^{n})$ are discussed in detail in

* [[Ronnie Brown]], Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/rbrsbookb-e040609.pdf))

An introductory survey of the role of orientals in Street's definition of an $\omega$-category is given in section 6 of

* [[Eugenia Cheng]], [[Aaron Lauda]], _Higher dimensional categories: an illustrated guidebook_ (2004) ([pdf](http://www.cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf))



[[!redirects orientals]]