
<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}



## Idea

The **Cosmic Cube of [[higher category theory]]** is the name for a  [[diagram]] whose vertices correspond to special types of [[(n,r)-categories]], notably to $(n,r)$-categories with especially rigid [[stuff, structure, property|property and structure]].



Its three axes each correspond to 

* _groupoidal_ $\infty$-categories, i.e. [[(∞,0)-categories]], i.e. [[∞-groupoid]]s;

* _[[strict ∞-categories|strict]]_ $\infty$-categories; 

* _[[symmetric monoidal category|symmetric monoidal]]_ $\infty$-categories.



### In terms of homotopy theory {#HomotopyTheory}

Each vertex of the cube can also be understood as corresponding to a version of [[homotopy theory]]: 

$\infty$-groupoids yield ordinary [[homotopy theory]], symmetric monoidal and groupal $\infty$-groupoids correspond to [[stable homotopy theory]], strictly abelian strict $\infty$-groupoids correspond to [[homological algebra]]. $\infty$-Categories that are not $\infty$-groupoids correspond to [[directed homotopy theory]].


[[cosmiccube.jpg:pic]]


## Vertices of the cube

### Strict $\infty$-categories

* [[strict ∞-category]] 
^^

### Strict $\infty$-groupoids

* [[strict ∞-groupoid]] 

* [[crossed complex]]


### Stably monoidal $\infty$-categories


* [[k-tuply monoidal n-category]]

* [[stabilization hypothesis]]

* [[periodic table]]

### Stably monoidal $\infty$-groupoids

* [[∞-group]]

* [[infinite loop space]], [[spectrum]]


### Strictly stably monoidal strict $\infty$-groupoids

* [[chain complex]], [[Dold-Kan correspondence]]


### Etc.

(...)


## Edges of the cube

### Strict $\infty$-groupoids in all $\infty$-groupoids

A [[strict ∞-groupoid]] is modeled by a [[crossed complex]]. Under [[∞-nerve]] it embeds into all [[∞-groupoid]]s, modeled as [[Kan complex]]es.

$$
  \array{
    CrsCplx &\stackrel{N^\Delta}{\hookrightarrow}& KanCplx
    \\
    \downarrow && \downarrow
    \\
    Str \infty Grpd &\hookrightarrow& \infty Grpd
  }
  \,.
$$

### Strictly stable strict $\infty$-groupoids in strict $\infty$-groupoids

A strictly stable strict ∞-groupoid is modeled by a [[chain complex]] of abelian groups. Under the embedding $\Theta$ of complexes into [[crossed complex]]es it embeds into [[strict ∞-groupoid]]s.

$$
  \array{
    ChnCplx &\stackrel{\Theta}{\hookrightarrow}& CrsCplx
    \\
    \downarrow && \downarrow
    \\
    StrAb Str \infty Grpd &\hookrightarrow& Str \infty Grpd
  }
  \,.
$$

For the definition of $\Theta$ see _[[Nonabelian Algebraic Topology]]_ , section [Crossed complexes from chain complexes](#http://ncatlab.org/nlab/show/Nonabelian+Algebraic+Topology#CrsFromCh).

### Strictly stable strict $\infty$-groupoids in all $\infty$-groupoids

Combining the above inclusions

$$
  \array{
    ChainCplx &\stackrel{\Theta}{\hookrightarrow}&
    CrossedCplx
    &\stackrel{N^\Delta}{\hookrightarrow}&
    KanCplx
    \\
    \downarrow^{\mathrlap{\simeq}}
    &&
    \downarrow^{\mathrlap{\simeq}}
    &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    StrAb Str\infty Grpd
    &\hookrightarrow&
    Str \infty Grpd
    &\hookrightarrow&
    \infty Grpd
  }
$$

yields in total the map $ChnCplx \to sAb$ from [[chain complex]]es to [[simplicial abelian group]]s (followed by the forgetful $sAb \to KanCpx$) of the [[Dold-Kan correspondence]].


### Strictly stable strict $\infty$-groupoids in strictly stable $\infty$-groupoids

A strictly stable strict ∞-groupoid is modeled by a [[chain complex]] of abelian groups. Under [[∞-nerve]] it embeds into all [[strictly ∞-groupoid]]s, modeled as [[spectrum|spectra]].

$$
  \array{
    ChnCplx &\stackrel{\N^\Delta}{\hookrightarrow}& Sp(Top)
    \\
    \downarrow && \downarrow
    \\
    StrAb Str \infty Grpd &\hookrightarrow& StrStab \infty Grpd
  }
  \,.
$$

### Strictly stable $\infty$-groupoids in all $\infty$-groupoids

A strictly stable ∞-groupoid is modeled by a [[spectrum]]. It embeds into all [[∞-groupoid]]s.



## References

* [[John Baez]], _[What $n$-Categories Should Be Like](http://math.ucr.edu/home/baez/n_categories/what.pdf)_.

* Some blog [discussion](http://golem.ph.utexas.edu/category/2008/03/kim_on_fundamental_groups_in_n.html#c015463)


[[!redirects cosmic cube]]
[[!redirects Cosmic Cube]]
[[!redirects cosmic cube of higher category theory]]
