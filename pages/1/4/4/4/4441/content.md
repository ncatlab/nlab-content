
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

_Diaconescu's theorem_ asserts that any [[presheaf topos]] is the [[classifying topos]] for [[internally flat functors]] on its [[site]].

Often a special case of this is considered, which asserts that for every [[topological space]] $X$ and [[discrete group]] $G$ there is an [[equivalence of categories]]
 
$$
  Topos(Sh(X),[\mathbf{B}G, Set]) \simeq G Tors(X)
$$

between the [[geometric morphism]]s from the [[sheaf topos]] over $X$ to the category of [[permutation representation]]s of $G$ and the category of $G$-[[torsor]]s on $X$.

## Statement


For $C$ a [[category]], write 

$$
  PSh(C) := [C^{op}, Set]
$$ 

for its [[presheaf topos]]. 

For $\mathcal{E}$ any [[topos]], write

$$
  FlatFunc(C, \mathcal{E}) \hookrightarrow [C, \mathcal{E}]
$$

for the [[full subcategory]] of the [[functor category]] on the [[internally flat functors]].

+-- {: .num_theorem}
###### Theorem
**(Diaconescu's theorem)**

There is an [[equivalence of categories]]

$$
  Topos(\mathcal{E}, PSh(C))
   \simeq
  FlatFunc(C, \mathcal{E})
$$

between the category of [[geometric morphism]]s $f : \mathcal{E} \to PSh(C)$ and the category of [[internally flat functors]] $C \to \mathcal{E}$.

This equivalence takes $f$ to the composite

$$
  C \stackrel{j}{\to} PSh(C) \stackrel{f^*}{\to} \mathcal{E}
  \,,
$$

where $j$ is the [[Yoneda embedding]] and $f^*$ is the [[inverse image]] of $f$.

=--

See for instance ([Johnstone, theorem B3.2.7](#Johnstone)).

+-- {: .num_remark}
###### Remark

If $C$ is a [[finitely complete category]] we may think of it as the [[syntactic category]] and in fact the [[syntactic site]] of an [[essentially algebraic theory]] $\mathbb{T}_C$.  An [[internally flat functor]] $C \to \mathcal{E}$ is then precisely a [[finite limit]] preserving functor, hence is precisely a $\mathbb{T}$-[[model]] in $\mathcal{E}$. 

Therefore the above theorem says in this case that there is an [[equivalence of categories]]

$$
  Topos(\mathcal{E}, PSh(C))
   \simeq
  \mathbb{T}_C Mod(\mathcal{E})
$$

between the [[geometric morphism]]s and the $\mathbb{T}$-models in $\mathcal{E}$.

This says that $PSh(C)$ is the [[classifying topos]] for $\mathbb{T}_C$.

=--

+-- {: .num_remark}
###### Remark

If $G$ is a [[discrete group]] and $C = \mathbf{B}G$ is its [[delooping]] [[groupoid]], $PSh(C) \simeq [\mathbf{B}G, Set]$ is the category of [[permutation representation]]s of $G$, also called the [[classifying topos]] of $G$.

In this case an internally flat functor $ C = \mathbf{B}G \to \mathcal{E}$ may be identified with a $G$-[[torsor]] object in $\mathcal{E}$. 

For this reason one sees in the literature sometimes the term "torsor" for internally flat functors out of any category $C$. It is however not so clear in which sense this terminology is helpful in cases where $C$ is not a delooping groupoid or at least _some_ groupoid.

=--

## References

A standard reference is section B3.2 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
  {#Johnstone}

The first proof of this result can be found in:

* R. Diaconescu, _Change of base for toposes with generators_ , J. Pure Appl. Algebra __6__ (1975), no. 3, 191-218 [link](http://www.sciencedirect.com/science/article/pii/0022404975900158).

Another proof is in 

* [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_, Lecture Notes in Mathematics __1616__, Springer 1995. vi+94 pp. ISBN: 3-540-60319-0


[[!redirects Diaconescu's theorem]]
[[!redirects Diaconescu's theorem]]
[[!redirects Diaconescu theorem]]
[[!redirects Disconescu's theorem]]
[[!redirects Diaconescu's Theorem]]
[[!redirects Diaconescu's Theorem]]
[[!redirects Diaconescu Theorem]]
[[!redirects Disconescu's Theorem]]
