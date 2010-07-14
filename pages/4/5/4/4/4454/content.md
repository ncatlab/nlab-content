
<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **Cosmic Cube of [[higher category theory]]** is the name for a  [[diagram]] whose vertices correspond to special types of [[(n,r)-categories]], notably to $(n,r)$-categories with especially rigid [[stuff, structure, property|property and structure]].


Its three axes each correspond to a form of simplification: groupoidal (giving only $n$-[[n-groupoid|groupoids]]), strict (giving only [[strict n-category|strict]] $n$-categories), and stable (giving only [[stable n-category|stable]] $n$-categories).  The cube is represented on page 10 of [[John Baez]]\'s talk _[What $n$-Categories Should Be Like](http://math.ucr.edu/home/baez/n_categories/what.pdf)_.

Taking any combination of choices of simplification, there are $8$ vertices of the cube; besides the $4$ listed above, we have [[strict n-groupoid]]s, [[stable n-groupoid]]s, [[stable strict n-category|stable strict]] $n$-categories, and of course [[stable strict n-groupoid]]s.

Each vertex also corresponds to a version of [[homotopy theory]].  The stable strict groupoid vertex corresponds to [[chain complexes]] as used in ordinary [[cohomology]]. [[Ronnie Brown]]'s [[nonabelian algebraic topology]] studies the version corresponding to the strict groupoid vertex.

## Vertices of the cube

### Strict $\infty$-groupoids

* [[strict ∞-groupoid]] 

* [[crossed complex]]

### Stably monoidal $\infty$-categories

* [[symmetric monoidal (∞,1)-category]]

### Stably monoidal $\infty$-groupoids

* [[infinite loop space]], [[spectrum]]

### Stricly stably monoidal strict $\infty$-groupoids

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

A strictly stable ∞-groupoid is modeled by a [[chain complex]] of abelian groups. Under the embedding $\Theta$ of complexes into [[crossed complex]]es it embeds into [[strict ∞-groupoid]]s.

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




## References

* [[John Baez]], _[What $n$-Categories Should Be Like](http://math.ucr.edu/home/baez/n_categories/what.pdf)_.

* Some blog [discussion](http://golem.ph.utexas.edu/category/2008/03/kim_on_fundamental_groups_in_n.html#c015463)

[[!redirects cosmic cube of higher category theory]]