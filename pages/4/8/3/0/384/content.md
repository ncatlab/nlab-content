
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#CW complexes
* table of contentsF
{: toc}


## Idea

A **CW-complex** is a [[nice topological space|nice]] [[topological space]] which is, or can be, built up inductively, by a process of [[attaching space|attaching]] [[n-disks]] $D^n$ along their [[boundary]] [[n-spheres|(n-1)-spheres]] $S^{n-1}$ for all $n \in \mathbb{N}$: a [[cell complex]] built from the basic topological cells $S^{n-1} \hookrightarrow D^n$. 

Being, therefore,  essentially combinatorial objects, CW complexes are the principal objects of interest in [[algebraic topology]]; in fact, most spaces of interest to algebraic topologists are [[homotopy equivalence|homotopy equivalent]] to CW-complexes. Notably the [[geometric realization]] of every [[simplicial set]], hence also of every [[groupoid]], [[2-groupoid]], etc., is a CW complex. 

Milnor has argued that the category of spaces which are homotopy equivalent to CW-complexes, also called [[m-cofibrant spaces]], is a [[nice category of spaces|convenient category of spaces]] for [[algebraic topology]].


Also, CW complexes are among the [[cofibrant objects]] in the [[classical model structure on topological spaces]]. 
In fact, _every_  topological space is _[[weak homotopy equivalence|weakly homotopy equivalent]]_ to a CW-complex (but need not be [[homotopy equivalence|strongly homotopy equivalent]] to one). See also at _[[CW-approximation]]_.  Since every topological space is a [[fibrant object]] in this [[model category]] structure, this means that the [[full subcategory]] of [[Top]] on the CW-complexes is a category of "homotopically very good representatives" of [[homotopy types]]. See at _[[homotopy theory]]_ and _[[homotopy hypothesis]]_ for more on this.

+-- {: .num_remark}
###### Remark
**(origin of the "CW" terminology)**

The terminology "CW-complex" goes back to [[John Henry Constantine Whitehead]] (and see the discussion in [Hatcher, "Topology of cell complexes", p. 520](#HatcherTopologyOfCellComplexes)). 

To quote from the original paper, which was "an address delivered before the Princeton Meeting of the (American Mathematical) Society on November
2, 1946", Whitehead states:


>In this presentation we abandon [[simplicial complexes]] in favor of [[cell complexes]]. This first part consists of geometrical preliminaries, including some elementary propositions concerning what we call closure finite complexes with weak topology, abbreviated to CW-complexes, ...


Thus the "CW" stands for the following two properties shared by any CW-complex:

* **C** = "closure finiteness": a [[compact subset]] of a CW-complex intersects the [[interior]] of only finitely many cells ([prop.](classical+model+structure+on+topological+spaces#CompactSubsetsAreSmallInCellComplexes)), hence in particular so does the closure of any cell.


* **W** = "weak topology": Since a CW-complex is a [[colimit]] in [[Top]] over its cells, and as such equipped with the [[final topology]] of the cell inclusion maps, a subset of a CW-complex is open or closed precisely if its restriction to (the closure of) each cell is open or closed, respectively.

(Whitehead called the [[interior]] of the [[n-disks]] the "cells", so that their closure of each cell is the corresponding $n$-disk.)

=--

\linebreak

## Definition
  {#Definition}


In the following let [[Top]] be the [[category]] of [[topological spaces]], or any of its variants, [[convenient category of topological spaces]].

+-- {: .num_defn #SpheresAndDisks}
###### Definition
**(spheres and disks)**

For $n \in \mathbb{N}$ write

* $D^n \in Top$ for the [[n-disk]], for instance realized (up to [[homeomorphism]]) as the [[closed ball|closed unit ball]] in the $n$-dimensional [[Euclidean space]] $\mathbb{R}^n$ and equipped with the induced [[subspace topology]];

* $S^{n-1} \in Top$ for the [[n-sphere|(n-1)-sphere]], for instance realized as the [[boundary]] of the [[n-disk]], also equipped with the corresponding [[subspace topology]];

* $i_n \;\colon\; S^{n-1} \hookrightarrow D^n$ for the [[continuous function]] that exhibits this [[boundary]] inclusion. 

  We also call these functions the _generating cofibrations_ (of the [[classical model structure on topological spaces]]).

Notice that

* $S^{-1} = \emptyset$;

* $S^0 = \ast \sqcup \ast$.

=--

+-- {: .num_defn #SingleCellAttachment}
###### Definition
**(single cell attachment)**

For $X$ any [[topological space]] and for $n \in \mathbb{N}$, then an **$n$-cell [[attaching space|attachment]]** to $X$ is the result of gluing an [[n-disk]] to $X$, along a prescribed image of its bounding [[n-sphere|(n-1)-sphere]] (def. \ref{SpheresAndDisks}):

Let

$$
  \phi \;\colon\; S^{n-1} \longrightarrow X
$$

be a [[continuous function]], then the _[[attaching space]]_

$$
  X \cup_\phi D^n \,\in Top
$$

is the topological space which is the [[pushout]] of the boundary inclusion of the $n$-sphere along $\phi$, hence the universal space that makes the following [[commuting diagram|diagram commute]]

$$
  \array{
    S^{n-1} &\stackrel{\phi}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& X \cup_\phi D^n
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/GluingHemispheres.jpg" width="400"></div>


If we take the defining boundary inclusion $\iota_n \colon S^{n-1} \to D^n$ itself as an attaching map, then we are gluing two $n$-disks to each other along their common boundary $S^{n-1}$. The result is the $n$-sphere:

$$
  \array{
    S^{n-1} &\overset{i_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{i_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& S^n
  }
  \,.
$$

(graphics from Ueno-Shiga-Morita 95)


=--

+-- {: .num_example }
###### Example

A single cell [[attaching space|attachment]] of a 0-cell, according to def. \ref{SingleCellAttachment} is the same as forming the [[disjoint union space]] $X \sqcup \ast$ with the [[point]] space $\ast$:

$$
  \array{
     (S^{-1} = \emptyset) &\overset{\exists !}{\longrightarrow}&  X
     \\
     \downarrow &(po)& \downarrow
     \\
     (D^0 = \ast) &\longrightarrow& X \sqcup \ast
  }
  \,.
$$

In particular if we start with the [[empty topological space]] $X = \emptyset$ itself, then by [[attaching space|attaching]] 0-cells we obtain a [[discrete topological space]]. To this then we may attach higher dimensional cells.


=--


+-- {: .num_defn #CellAttachments}
###### Definition
**(attaching many cells at once)**


If we have a [[set]] of attaching maps $\{S^{n_i-1} \overset{\phi_i}{\longrightarrow} X\}_{i \in I}$ (as in def. \ref{SingleCellAttachment}), all to the same space $X$, we may think of these as one single continuous function out of the [[disjoint union space]] of their [[domain]] spheres

$$
  (\phi_i)_{i \in I} 
    \;\colon\;
  \underset{i \in I}{\sqcup}
  S^{n_i-1} 
   \longrightarrow 
  X
  \,.
$$

Then the result of attaching _all_ the corresponding $n$-cells to $X$ is the pushout of the corresponding [[disjoint union]] of boundary inclusions:

$$
  \array{
    \underset{i \in I}{\sqcup} S^{n_i - 1}
      &\overset{(\phi_i)_{i \in I}}{\longrightarrow}&
    X
    \\
    \downarrow
      &(po)&
    \downarrow
    \\
    \underset{i \in I}{\sqcup} D^n
      &\longrightarrow&
    X \cup_{(\phi_i)_{i \in I}} \left(\underset{i \in I}{\sqcup} D^n\right)
  }
  \,.
$$

=--

Apart from attaching a set of cells all at once to a fixed base space, we may "attach cells to cells" in that after forming a given cell attachment, then we further attach cells to the resulting attaching space, and ever so on:

+-- {: .num_defn #RelativeCellComplexes}
###### Definition
**([[relative cell complexes]])


Let $X$ be a topological space, then 
a _topological [[relative cell complex]]_ of countable height based on $X$ is a [[continuous function]]

$$
  f \colon X \longrightarrow Y
$$

and a [[sequential diagram]] of [[topological space]] of the form

$$
  X = X_0 \hookrightarrow X_1 \hookrightarrow X_2 \hookrightarrow X_3 \hookrightarrow \cdots
$$

such that 

1. each $X_k \hookrightarrow X_{k+1}$ is exhibited as a cell attachment according to def. \ref{CellAttachments}, hence presented by a [[pushout]] diagram of the form

   $$
     \array{
       \underset{i \in I}{\sqcup} S^{n_i - 1}
         &\overset{(\phi_i)_{i \in I}}{\longrightarrow}&
       X_k
       \\
       \downarrow
         &(po)&
       \downarrow
       \\
       \underset{i \in I}{\sqcup} D^{n_i}
         &\longrightarrow&
      X_{k+1}
     }
     \,.
   $$

1. $Y = \underset{k\in \mathbb{N}}{\cup} X_k$ is the [[union]] of all these cell attachments, and $f \colon X \to Y$ is the canonical inclusion; or stated more abstractly: the map $f \colon X \to Y$ is the inclusion of the first component of the diagram into its [[colimit|colimiting cocone]] $\underset{\longrightarrow}{\lim}_k X_k$:

   $$
     \array{
       X = X_0 &\longrightarrow& X_1 &\longrightarrow& X_2 &\longrightarrow& \cdots
       \\
       & {}_{\mathllap{f}}\searrow & \downarrow & \swarrow && \cdots
       \\
       && Y = \underset{\longrightarrow}{\lim} X_\bullet
     }
   $$

If here $X = \emptyset$ is the [[empty space]] then the result is a map $\emptyset \hookrightarrow Y$, which is equivalently just a space $Y$ built form "attaching cells to nothing". This is then called just a _topological [[cell complex]]_ of countable hight.

Finally, a topological (relative) cell complex of countable hight is called a **CW-complex** if the $(k+1)$-st cell attachment $X_k \to X_{k+1}$ is entirely by $(k+1)$-cells, hence exhibited specifically by a pushout of the following form:

$$
  \array{
    \underset{i \in I}{\sqcup} S^{k}
      &\overset{(\phi_i)_{i \in I}}{\longrightarrow}&
    X_k
    \\
    \downarrow
      &(po)&
    \downarrow
    \\
    \underset{i \in I}{\sqcup} D^{k+1}
      &\longrightarrow&
    X_{k+1}
  }
  \,.
$$

A _[[finite CW-complex]]_ is one which admits a presentation in which there are only finitely many attaching maps, and similarly a _countable CW-complex_ is one which admits a presentation with countably many attaching maps. 

Given a CW-complex, then $X_n$ is also called its $n$-[[skeleton]].

=--


A **cellular map** between CW-complexes $X$ and $Y$ is a [[continuous function]] $f\colon X \to Y$ such that $f(X_n) \subset Y_n$.



## Properties

### Closure properties

If $A \hookrightarrow X$ is an inclusion of CW-complexes, then the quotient $X/A$ is naturally itself a CW-complex, such that the quotient map $X \to X/A$ is cellular.


If $X$ is a CW-complex and $K$ is a [[finite CW-complex]], then the [[product topological space]] $X \times K$ is naturally itself a CW-complex.

For example the [[suspension]] of a CW-complex itself carries the structure of a CW-complex.

Similarly for [[pointed topological space|pointed]] CW-complexes: the [[smash product]] of a pointed CW-complex with a finite pointed CW-complex is a pointed CW-complex. For example the [[reduced suspension]] $S^1 \wedge X$ of a  pointed CW-complex $X$ is itself a CW-complex.


+-- {: .num_prop #ClosureOfCWComplexesUnderCartesianProduct}
###### Proposition

For $X$ and $Y$ [[CW-complexes]] with attaching maps $\{\phi_\alpha\}$ and $\{\Psi_\beta\}$, then the [[compactly generated topological space|k-ification]] $(X \times Y)_c$ of their [[product topological space]] $X \times Y$ (hence their Cartesian product in the category of [[compactly generated topological spaces]]) is again a CW-complex with attaching maps $\{\Phi_\alpha \times \Psi_\beta\}$. 

If either of the two CW-complexes is a [[locally compact topological space]] or if both are countable CW-complexes (have a [[countable set]] of cells) then

$$
  (X\times Y)_c \simeq X \times Y
$$

and so then the [[product topological space]] $X \times Y$ itself has CW-complex structure.

=--

([Hatcher, theorem A.6](#Hatcher))

### Local contractibility
 {#LocalContractibility}


+-- {: .num_prop }
###### Proposition

A CW-complex is a [[locally contractible topological space]].

=--

For instance ([Hatcher, prop. A.4](#Hatcher)). 

### Compactness properties

+-- {: .num_prop }
###### Proposition
**([[CW-complexes are paracompact Hausdorff spaces]])**

Every CW-complex is a 

1. a [[normal topological space]], in particular a [[Hausdorff space]],

1. a [[paracompact topological space]].

=--


+-- {: .num_prop #CWComplexIsCompactlyGenerated}
###### Proposition

Every CW-complex is a [[compactly generated topological space]].

=--

+-- {: .proof}
###### Proof

Since a CW-complex $X$ is a [[colimit]] in [[Top]] over attachments of standard [[n-disks]] $D^{n_i}$ (its cells), by the characterization of colimits in $Top$ ([prop.](Top#DescriptionOfLimitsAndColimitsInTop)) a subset of $X$ is open or closed precisely if its restriction to each cell is open or closed, respectively. Since the $n$-disks are compact, this implies one direction: if a subset $A$ of $X$ intersected with all compact subsets is closed, then $A$ is closed. 

For the converse direction, since [[a CW-complex is a Hausdorff space]] and since [[compact subspaces of Hausdorff spaces are closed]], the intersection of a closed subset with a compact subset is closed.

=--


### Up to homotopy equivalence 

+-- {: .num_theorem} 
###### Theorem 

Every CW complex is homotopy equivalent to (the [realization](simplicial+complex#geometric_realisations_and_polyhedra) of) a [[simplicial complex]]. 

=-- 

See [Gray](#Gray), Corollary 16.44 (p. 149) and Corollary 21.15 (p. 206).  For more see at _[[CW approximation]]_.

+-- {: .num_cor} 
###### Corollary 
Every CW complex is homotopy equivalent to a space that admits a [[good open cover]]. 
=-- 

+-- {: .num_theorem} 
###### Theorem 

If $Y$ has the [[homotopy type]] of a CW complex and $X$ is a [[finite CW complex]], then the [[mapping space]] $Y^X$ with the [[compact-open topology]] has the homotopy type of a CW complex. 

=-- 

([Milnor 59](#Milnor59)) 

### Subcomplexes
 {#Subcomplexes}

+-- {: .num_prop }
###### Proposition

For $X$ a CW complex, the inclusion $X' \hookrightarrow X$ of any subcomplex has an [[open neighbourhood]] in $X$ which is a [[deformation retract]] of $X'$. In particular such an inclusion is a _[good pair](relative+homology#GoodPair)_ in the sense of [[relative homology]].

=--

For instance ([Hatcher, prop. A.5](#Hatcher)).

+-- {: .num_remark }
###### Remark

For $A \hookrightarrow X$ the inclusion of a subcomplex into a CW complex, then the pair $(X,A)$ is often called a _[[CW-pair]]_. This appears notably in the [[axioms]] for [[generalized (Eilenberg-Steenrod) cohomology]].

=--

e.g. ([AGP 02, def. 5.1.11](#AGP02))

### Cellular approximation theorem
 {#CellularApproximationTheorem}

The _[[cellular approximation theorem]]_ states that every [[continuous map]] between [[CW complexes]] (with chosen CW presentations) is [[homotopy|homotopic]] to a [[cellular map]] (a map induced by a morphism of [[cell complexes]]). 

This is the analogue for [[CW-complexes]] of the [[simplicial approximation theorem]] (sometimes also called lemma): that every continuous map between the [[geometric realizations]] of [[simplicial complexes]] is [[homotopy|homotopic]] to a map induced by a map of [[simplicial complexes]] (after subdivision). 


For more see at _[[cellular approximation theorem]]_.


### Fibrations

Fibrations between CW-complexes also behave particularly well: [[a Serre fibration between CW-complexes is a Hurewicz fibration]].

### Singular homology
 {#SingularHomology}

We discuss aspects of the [[singular homology]] $H_n(-) \colon $ [[Top]] $\to$ [[Ab]] of CW-complexes. See also at _[[cellular homology]] of CW-complexes_.

Let $X$ be a CW-complex and write 

$$
  X_0 \hookrightarrow X_1 \hookrightarrow X_2 \hookrightarrow \cdots \hookrightarrow X
$$

for its [[filtered topological space]]-structure with $X_{n+1}$ the topological space obtained from $X_n$ by gluing on $(n+1)$-cells. For $n \in \mathbb{N}$ write $nCells \in Set$ for the set of $n$-cells of $X$.


+-- {: .num_prop #SkeletalRelativeSingularHomologyOfCW}
###### Proposition

The [[relative singular homology]] of the filtering degrees is

$$
  H_n(X_k , X_{k-1})
  \simeq
  \left\{
    \array{
       \mathbb{Z}[nCells] & if\; k = n
       \\
       0 & otherwise
    }
  \right.
  \,,
$$

where $\mathbb{Z}[nCells]$ denotes the [[free abelian group]] on the set of $n$-cells.


=--

The proof is spelled out at _[Relative singular homology - Of CW complexes](relative+homology#RelativeHomologyOfCWComplexes)_.


+-- {: .num_prop #RelativeHomologyOfFilterStep}
###### Proposition

With $k,n \in \mathbb{N}$ we have

$$
  (k \gt n) \Rightarrow (H_k(X_n) \simeq 0)
  \,.
$$

In particular if $X$ is a CW-complex of [[finite number|finite]] [[dimension of a CW-complex]] $dim X$ (the maximum degree of cells), then 

$$
  (k \gt dim X) \Rightarrow (H_k(X) \simeq 0).
$$

Moreover, for $k \lt n$ the inclusion

$$
  H_k(X_n) \stackrel{\simeq}{\to} H_k(X)
$$

is an [[isomorphism]] and for $k = n$ we have an isomorphism

$$
  image(H_n(X_n) \to H_n(X)) \simeq H_n(X)
  \,.
$$

=--

This is mostly for instance in ([Hatcher, lemma 2.34 b),c)](#Hatcher)).

+-- {: .proof}
###### Proof

By the [[long exact sequence]] in [[relative homology]], discussed at _[Relative homology -- long exact sequences](relative+homology#LongExactSequences)_, we have an [[exact sequence]]

$$
  H_{k+1}(X_n , X_{n-1})
  \to 
  H_k(X_{n-1})
  \to 
  H_k(X_n)
  \to 
  H_k(X_n, X_{n-1})
  \,.
$$

Now by prop. \ref{SkeletalRelativeSingularHomologyOfCW} the leftmost and rightmost homology groups here vanish when $k \neq n$ and $k \neq n-1$ and hence exactness implies that

$$
  H_k(X_{n-1})
  \stackrel{\simeq}{\to}
  H_k(X_n)
$$

is an [[isomorphism]] for $k \neq n,n-1$. This implies the first claims by [[induction]] on $n$.

Finally for the last claim use that the above exact sequence gives

$$
  H_{n-1+1}(X_n , X_{n-1})
  \to 
  H_{n-1}(X_{n-1})
  \to 
  H_{n-1}(X_n)
  \to 
  0
$$

and hence that with the above the map $H_{n-1}(X_{n-1}) \to H_{n-1}(X)$ is surjective.


=--


## Examples
 {#Examples}


* Any undirected [[graph]] (loops and/or multiple edges allowed) has a geometric realization as a 1-dimensional CW complex.

* The [[geometric realization]] of any [[simplicial set]] is a CW-complex ([Milnor 57](#Milnor57)). 

  * In particular, in the context of the [[homotopy hypothesis]] the [[Quillen equivalence]]  between [[∞-groupoid]]s and [[nice topological space]]s maps each [[∞-groupoid]] to a CW-complex.

* The [[n-spheres]] have a standard CW-complex structure, with exactly 2-cells in each dimension, obtained [[induction|inductively]] by [[space attachment|attaching]] two $n$-dimensional [[hemispheres]] to the $(n-1)$-sphere regarded as the [[equator]] in the $n$-sphere.

* The [[infinite-dimensional sphere]] may be realized as the CW-complex which is the [[colimit]] over the resulting [[relative cell complex]]-inclusions $S^n \hookrightarrow S^{n + 1} \hookrightarrow S^{n + 2} \hookrightarrow \cdots$.

* Every [[projective space]] over the [[real numbers]], [[complex numbers]] or [[quaternions]] has the structure of a [[CW-complex]] with a single cell i in each dimension $k$, $2k$ or $4k$, respectively. See at _[[cell structure of K-projective space]]_.

* Every [[compact topological space|compact]] [[smooth manifold]] admits a smooth [[triangulation]] and hence a CW-complex structure. In the generality of manifolds with group actions see at  _[G-CW complex -- G-manifolds](G-CW+complex#GManifolds)_.

* Every noncompact [[smooth manifold]] of [[dimension]] $n$ is [[homotopy equivalence|homotopy equivalent]] to an $(n-1)$-dimensional CW-complex. ([Napier-Ramachandran](#NapierRamachandran)).


## Related concepts

* [[dimension of a CW-complex]]

* [[cell complex]]

* [[cellular map]]

* [[CW approximation]]

* [[quasi-finite CW-complex]]

* [[cellular homology]]

* [[simplicial set]], [[geometric realization]]

* [[CW-spectrum]]

* [[G-CW complex]]


[[!include universal constructions of topological spaces -- table]]


## References


The introduction of the term is contained in 

* [[J. H. C. Whitehead]], _Combinatorial homotopy I_ , Bull. Amer. Math. Soc, 55, (1949), 213–245.


Basic textbook accounts include

* Brayton Gray, _Homotopy Theory: An Introduction to Algebraic Topology_, Academic Press, New York (1975). 

* [[George Whitehead]], chapter II of _Elements of homotopy theory_, 1978

* {#May} [[Peter May]], _[[A Concise Course in Algebraic Topology]]_, U. Chicago Press (1999) 

* {#Hatcher} [[Allen Hatcher]], _[Algebraic Topology](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)_, 2002
  
* {#HatcherTopologyOfCellComplexes} [[Allen Hatcher]], _Topology of cell complexes_ ([pdf](https://www.math.cornell.edu/~hatcher/AT/ATapp.pdf)) in _Algebraic Topology_

* {#HatcherK} [[Allen Hatcher]], _Vector bundles & K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* {#FP} [[Rudolf Fritsch]], Renzo A. Piccinini, _Cellular structures in topology_, Cambridge studies in advanced mathematics Vol. 19, Cambridge University Press (1990). ([pdf](https://epub.ub.uni-muenchen.de/4493/1/4493.pdf)) 


* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 5.1 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

Original articles include

* {#Milnor59} [[John Milnor]], _On spaces having the homotopy type of a CW-complex_, Trans. Amer. Math. Soc. 90 (2) (1959), 272-280. 
  

* {#Milnor57} [[John Milnor]], _The geometric realization of a semi-simplicial complex_, Annals of Mathematics, 2nd Ser., __65__, n. 2. (Mar., 1957), pp. 357-362; doi:[10.2307/1969967](https://doi.org/10.2307/1969967), [Semantic scholar pdf](https://pdfs.semanticscholar.org/7cbe/0482ce422d3adcc84be80b5ab3f68520a247.pdf)
 

See also

 * {#NapierRamachandran} Terrance Napier,  Mohan Ramachandran,  _[Elementary Construction of Exhausting Subsolutions of Elliptic Operators](http://www.unige.ch/math/EnsMath/EM_en/)_ L'Enseignement Math&eacute;matique, t. 50 (2004), p. 367 - 389.
 


An inconclusive discussion [here](http://nforum.mathforge.org/discussion/4135/simplicial-homology/?Focus=33785#Comment_33785) about what parts of the definition of a CW complex should be [[stuff, structure, property|properties]] and what parts should be structure.


[[!redirects CW complex]]
[[!redirects CW-complex]]
[[!redirects CW complexes]]
[[!redirects CW-complexes]]

[[!redirects relative CW-complex]]
[[!redirects relative CW-complexes]]
