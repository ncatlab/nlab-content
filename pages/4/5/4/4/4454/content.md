
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The **Cosmic Cube of [[higher category theory]]** is the name for a  [[diagram]] whose vertices correspond to special types of [[n-categories]].   The cube looks like this:

[[cosmiccube.jpg:pic]]

We may take $n = \infty$ here as well, and we may also consider a version for [[(n,r)-categories]].  The three axes correspond to:

* making $n$-categories 'groupoidal' --- that is, making morphisms invertible, thus passing from general $n$-categories to _[[n-groupoids]]_;

* making $n$-categories strict, thus passing from general $n$-categories to _[[strict n-categories|strict]]_ $n$-categories; 

* making $n$-categories symmetric monoidal or 'stable', thus passing from general $n$-categories to _[[symmetric monoidal category|symmetric monoidal]]_ $n$-categories.

### In terms of homotopy theory {#HomotopyTheory}

Each vertex of the cube can also be understood as corresponding to a version of [[homotopy theory]]: 

$\infty$-groupoids yield ordinary [[homotopy theory]], symmetric monoidal and groupal $\infty$-groupoids correspond to [[stable homotopy theory]], strictly abelian strict $\infty$-groupoids correspond to [[homological algebra]]. $\infty$-Categories that are not $\infty$-groupoids correspond to [[directed homotopy theory]].





## Vertices of the cube

Here we list the 8 vertices of the cube in the case of $\infty$-categories.

### Strict $\infty$-categories

* [[strict ∞-category]] 

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

A strictly stable strict ∞-groupoid is modeled by a bounded-below [[chain complex]] of abelian groups. Under the embedding $\Theta$ of complexes into [[crossed complex]]es it embeds into [[strict ∞-groupoid]]s.

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

A strictly stable strict ∞-groupoid is modeled by a bounded-below [[chain complex]] of abelian groups. Under [[∞-nerve]] it embeds into all ([[connective spectrum|connective]]) [[spectra]]s, modeled as [[spectrum object]]s in [[Kan complex]]es.

$$
  \array{
    ChnCplx^+ 
    &\stackrel{\Sigma^\infty \N^\Delta \Theta}{\hookrightarrow}& Sp(KanCplx)
    \\
    \downarrow && \downarrow
    \\
    StrAb Str \infty Grpd &\hookrightarrow& Sp(\infty Grpd)
  }
  \,.
$$

### Strictly stable $\infty$-groupoids in all $\infty$-groupoids

A strictly stable ∞-groupoid is modeled by a connective [[spectrum]].  The forgetful functor to [[∞-groupoid]]s is also called $\Omega^\infty$ or the "zeroth-space functor."



## References

* [[John Baez]], _[What $n$-Categories Should Be Like](http://math.ucr.edu/home/baez/n_categories/what.pdf)_.

* Some blog [discussion](http://golem.ph.utexas.edu/category/2008/03/kim_on_fundamental_groups_in_n.html#c015463)


[[!redirects cosmic cube]]
[[!redirects Cosmic Cube]]
[[!redirects cosmic cube of higher category theory]]
