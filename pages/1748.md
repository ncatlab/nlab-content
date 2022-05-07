
> This page is about homotopy as a transformation.  For homotopy sets in [[homotopy categories]], see [[homotopy (as an operation)]].

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea 

In many [[category|categories]] $C$ in which one does [[homotopy theory]], there is a notion of _homotopy_ between [[morphisms]], which is closely related to the [[2-morphisms]] in [[higher category theory]]: a homotopy between two morphisms is a way in which they are equivalent.  

If we regard such a category as a presentation of an $(\infty,1)$-[[(infinity,1)-category|category]], then homotopies $f\sim g$ present the 2-cells $f\Rightarrow g$ in the resulting $(\infty,1)$-category.

## Definition

### In topological spaces

+-- {: .num_defn #LeftHomotopy}
###### Definition

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a **left homotopy**

$$
  \eta \colon f \,\Rightarrow_L\, g
$$

is a [[continuous function]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$


out of the standard [[cylinder object]] over $X$: the [[product space]] of $X$ with the [[Euclidean space|Euclidean]] [[closed interval]] $I \coloneqq [0,1]$, such that this fits into a [[commuting diagram]] of the form

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://www.ncatlab.org/nlab/files/AHomotopy.jpg" width="400">
</div>


$$
  \array{
     X
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{f}}
     \\
     X \times I &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{g}}
     \\
     X
  }
  \,.
$$

(graphics grabbed from J. Tauber [here](http://jtauber.com/blog/2005/07/01/path_homotopy/))

=--

+-- {: .num_example #PathsAsLeftHomotopyBetweenPoints}
###### Example

Let $X$ be a [[topological space]] and let $x,y \in X$ be two of its points, regarded as functions $x,y \colon \ast \longrightarrow X$ from the point to $X$. Then a left homotopy, def. \ref{LeftHomotopy}, between these two functions is a commuting diagram of the form

$$
  \array{
     \ast
     \\
     {}^{\mathllap{\delta_0}}\downarrow & \searrow^{\mathrlap{x}}
     \\
     I &\stackrel{\eta}{\longrightarrow}& X
     \\
     {}^{\mathllap{\delta_1}}\uparrow & \nearrow_{\mathrlap{y}}
     \\
     \ast
  }
  \,.
$$

This is simply a continuous path in $X$ whose endpoints are $x$ and $y$.

=--


### In enriched categories 

If $C$ is [[enriched category|enriched]] over [[Top]], then a **homotopy** in $C$ between maps $f,g:X\,\rightrightarrows \,Y$ is a map $H:[0,1] \to C(X,Y)$ in $Top$ such that $H(0)=f$ and $H(1)=g$.  In $Top$ itself this is the classical notion.

If $C$ has [[copower|copowers]], then an equivalent definition is a map $[0,1]\odot X\to Y$, while if it has [[power|powers]], an equivalent definition is a map $X\to \pitchfork([0,1],Y)$.

There is a similar definition in a [[simplicially enriched category]], replacing $[0,1]$ with the 1-simplex $\Delta^1$, with the caveat that in this case not all _simplicial homotopies_ need be composable even if they match correctly. (This depends on whether or not all (2,1)-[[horn]]s  in the simplicial set, $C(X,Y)$, have fillers.)   Likewise in a [[dg-category]] we can use the "chain complex interval" to get a notion of _chain homotopy_.


### In model categories 

If $\mathcal{C}$ is a [[model category]], it has an intrinsic notion of homotopy determined by its factorizations. For more on the following see at _[[homotopy in a model category]]_.

+-- {: .num_defn #PathAndCylinderObjectsInAModelCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]] and $X \in \mathcal{C}$ an [[object]].

* A **[[path object]]** $Path(X)$ for $X$ is a factorization of the [[diagonal]] $\nabla_X \colon X \to X \times X$ as

$$
  \nabla_X 
  \;\colon\;
   X \underoverset{\in W}{i}{\longrightarrow} Path(X) \overset{(p_0,p_1)}{\longrightarrow} X \times X
  \,.
$$

where $X\to Path(X)$ is a weak equivalence. This is called a **good path object** if in addition $Path(X) \to X \times X$ is a fibration.

* A **[[cylinder object]]** $Cyl(X)$ for $X$ is a factorization of the [[codiagonal]] (or "fold map") $\Delta_X: X \sqcup X \to X$ as

$$
  \Delta_X
  \;\colon\;
  X \sqcup X \overset{(i_0,i_1)}{\longrightarrow} Cyl(X) \underoverset{p}{\in W}{\longrightarrow} X
  \,.
$$

where $Cyl(X) \to X$ is a weak equivalence. This is called a **good cylinder object** if in addition $X \sqcup X \to Cyl(X)$ is a cofibration.

=--

+-- {: .num_remark #RemarkOnChoicesOfNonGoodPathAndCylinderObjects}
###### Remark

By the factorization axioms every object in a model category has both a good path object and as well as a good cylinder object according to def. \ref{PathAndCylinderObjectsInAModelCategory}. But in some situations one is genuinely interested in using non-good such objects.  

For instance in the [[classical model structure on topological spaces]], the obvious object $X\times [0,1]$ is a cylinder object, but not a good cylinder unless $X$ itself is cofibrant (a [[cell complex]] in this case).

More generally, the path object $Path(X)$ of def. \ref{PathAndCylinderObjectsInAModelCategory} is analogous to the [[powering]] $\pitchfork(I,X)$ with an [[interval object]] and the cylinder object $Cyl(X)$ is analogous to the [[tensoring]] $I\odot X$ with an interval object.  In fact, if $\mathcal{C}$ is a $V$-[[enriched model category]] and $X$ is fibrant/cofibrant, then these powers and copowers  are in fact examples of (good) path and cylinder objects if the [[interval object]] is sufficiently good. 

=--

+-- {: .num_defn #LeftAndRightHomotopyInAModelCategory}
###### Definition

Let $f,g \colon X \longrightarrow Y$ be two [[parallel morphisms]] in a [[model category]].

* A **left homotopy** $\eta \colon f \Rightarrow_L g$ is a morphism $\eta \colon Cyl(X) \longrightarrow Y$ from a [[cylinder object]] of $X$,  def. \ref{PathAndCylinderObjectsInAModelCategory}, such that it makes this [[commuting diagram|diagram commute]]: 

$$
  \array{
    X &\longrightarrow& Cyl(X) &\longleftarrow& X
    \\
    & {}_{\mathllap{f}}\searrow &\downarrow^{\mathrlap{\eta}}& \swarrow_{\mathrlap{g}}
    \\
    && 
    Y
  }
  \,.
$$

* A **right homotopy** $\eta \colon f \Rightarrow_R g$ is a morphism $\eta \colon X \to Path(Y)$ to some [[path object]] of $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, such that this [[commuting diagram|diagram commutes]]:

$$
  \array{
    && X
    \\
    & {}^{\mathllap{f}}\swarrow & \downarrow^{\mathrlap{\eta}} & \searrow^{\mathrlap{g}} 
    \\
    Y &\longleftarrow& Path(Y) &\longrightarrow& Y
  }
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

By remark \ref{RemarkOnChoicesOfNonGoodPathAndCylinderObjects} it follows that in a $Top$-[[enriched model category]], any enriched homotopy between maps $X\to Y$ is a left homotopy if $X$ is cofibrant and a right homotopy if $Y$ is fibrant.  Similar remarks hold for other enrichments.

=--

For more see at _[[homotopy in a model category]]_.

### In (co-)fibration categories

Clearly the concept of left homotopy in def. \ref{PathAndCylinderObjectsInAModelCategory} only needs part of the model category axioms and thus makes sense more generally in suitable [[cofibration categories]]. Dually, the concept of path objects in def. \ref{PathAndCylinderObjectsInAModelCategory} makes sense more generally in suitable [[fibration categories]] such as [[categories of fibrant objects]] in the sense of Brown.

Likewise if there is a [[cylinder functor]], one gets functorially defined [[cylinder objects]], etc.



## Related concepts

[[!include homotopy-homology-cohomology]]

* [[homotopy theory]]

* [[left homotopy]], [[right homotopy]]

* [[homotopy relative boundary]]

* [[smooth homotopy]]

* [[isotopy]], [[smooth isotopy]]

* [[higher homotopy]]

* [[homotopy class]]

* [[transfor]]

  * [[natural transformation]]

  * [[pseudonatural transformation]]

  * [[lax natural transformation]]

* [[function extensionality]]

* [[homotopy analysis method]]


## References 

See the references at _[[homotopy theory]]_ and at _[[model category]]_.

Discussion in [[computational topology]]:

* [[Marek Filakovský]], [[Lukáš Vokřínek]], _Are two given maps homotopic? An algorithmic viewpoint_, Found Comput Math (2019) ([arXiv:1312.2337](https://arxiv.org/abs/1312.2337), [doi:10.1007/s10208-019-09419-x](https://doi.org/10.1007/s10208-019-09419-x))

[[!redirects left homotopy]]
[[!redirects right homotopy]]

[[!redirects left homotopies]]
[[!redirects right homotopies]]


[[!redirects homotopy (as a transformation)]]

[[!redirects homotopies]]

[[!redirects homotopic]]