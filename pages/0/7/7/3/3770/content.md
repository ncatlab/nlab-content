
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of  _globular operads_ is a variant of that of [[operads]] on which certain [[algebraic definition of higher category|algebraic notions of higher category]] are based. The notion was introduced by [[Batanin]]; a globular operad is also called a _Batanin operad_. 

A globular operad gives rise to a [[monad]] on the [[category]] of [[globular sets]]; one example is the free [[strict ∞-category]] monad $T$ on globular sets. The monads which so arise may be characterized precisely as [[cartesian monads]] on globular sets over $T$ (itself a cartesian monad).  This means that they are also examples of [[generalized multicategories]] relative to $T$.

## Definition ## 

### Globular collections

+-- {: .num_defn }
###### Definition

A **globular collection** is a [[globular set]] $X$ equipped with a map 

$$f: X \to T(1)$$ 

to $T(1)$, the underlying globular set of the free strict $\omega$-category on the terminal globular set. Hence the category $Coll$ is the [[slice category]] 

$$Coll = Set^{Glob^{op}}/T(1)$$ 

=--

+-- {: .num_defn #MonoidalStructureOnCollections}
###### Definition

The category of collections carries a [[monoidal category|monoidal product]] $\circ$ defined as follows. Given collections $f: X \to T(1)$, $g: Y \to T(1)$, the underlying globular set of $X \circ Y$ is given by [[pullback]]

$$\array{
X \circ Y & \to & T(Y) \\
\downarrow & & \downarrow T(!) \\
X & \underset{f}{\to} & T(1)
}$$ 

and the requisite map $X \circ Y \to T(1)$ is given by the composite 

$$X \circ Y \to T(Y) \overset{T(g)}{\to} T T(1) \overset{\mu(1)}{\to} T(1)$$ 

where $\mu: T T \to T$ denotes multiplication of the monad $T$. The monoidal unit is the collection $u(1): 1 \to T(1)$ where $u: Id \to T$ is the unit of $T$, and the associativity and unit constraints may be defined by means of universal properties, taking advantage of the fact that $T$ is cartesian. 

=--

### Globular operads

+-- {: .num_defn #GlobularOperad}
###### Definition

A **globular operad** is a [[monoid]] in the [[monoidal category]] $Coll$, (with the monoidal structure given by  def. \ref{MonoidalStructureOnCollections}). 

=--

### Monad of a globular operad

+-- {: .num_defn }
###### Definition


Each globular operad $f: P \to T(1)$, (as in def. \ref{GlobularOperad}), gives rise to a globular [[monad]] $M_P$ on $Set^{Glob^{op}}$. Abstractly, $M_P(X)$ is just the pullback 

$$\array{
  M_P(X) & \to & T(X) \\
  \downarrow & & \downarrow T(!) \\
  P & \underset{f}{\to} & T(1)
}$$ 

and the multiplication and unit for $M_P$ may be worked out from the multiplication and unit for the globular operad $P$. 

=--

+-- {: .num_remark }
###### Remark

A more concrete description of $M_P(X)$ may be worked out in terms of a concrete description of the free strict $\omega$-category $T(X)$. To describe this, first notice that every element $\tau$ of $T(1)$, which is essentially a pasting diagram built up out of globes of $1$, can be drawn as a globular set which we denote as $[\tau]$. The globes of $[\tau]$ are instances of globular cells as they appear in the pasting diagram $\tau$, and their sources and targets are then also instances of cells in $\tau$. (Batanin describes $T(1)$ in terms of trees, and the globular set $\tau$ is given formally in the tree language.) 

Similarly, we can think of an element of $T(X)$ as a pasting diagram built out of globes in $X$, and such a pasting diagram can be thought of as having an underlying shape given by an pasting diagram $\tau$ in $T(1)$, together with a labeling of the pasting cells in $\tau$ by elements on $X$. The labeling is in fact just a morphism $[\tau] \to X$ of globular sets. Therefore we have an explicit formula for the set of $n$-cells of $T(X)$: 

$$T(X)(n) = \sum_{\tau \in T(1)(n)} \hom([\tau], X)$$ 

and similarly, for a globular operad with underlying collection $f: P \to T(1)$, 

$$M_P(X)(n) = \sum_{x \in P(n)} \hom([f(x)], X)$$ 

=--

### Categories of operators
 {#CategoryOfOperators}

The [[category of operators]] of a globular operad $A$ is (the [[syntactic category]] of) a homogeneous [[globular theory]] $i_A \colon \Theta_0 \to \Theta_A$ and every globular operad is characterized by its [[globular theory]]. See there for more details



## Examples

### The Globular operad for $\omega$-categories

Write $\omega$ for the globular operad whose [[category of operators]], see [above](#CategoryOfOperators), is the [[Theta category]] $\Theta$.

+-- {: .num_prop }
###### Proposition

The category $Str\omega Cat$ of [[strict ∞-categories]] is [[equivalence of categories|equivalent]] to that of algebras over the terminal globular operad. Hence it is the [[full subcategory]] of that of [[∞-graphs]] which satisfy the [[Segal condition]] with respect to the canonical inclusion $\Theta_0 \to \Theta$ that defines its [[globular theory]]: we have a [[pullback]]

$$
  \array{
    Str\omega Cat 
     &\underoverset{\simeq}{N}{\to}& Mod_\Theta &\hookrightarrow&      
PSh(\Theta)
    \\
    \downarrow^{\mathrlap{U}} && \downarrow^{} && \downarrow
   \\
   \omega Graph &\stackrel{\simeq}{\to}& Sh(\Theta_0) &\hookrightarrow& PSh(\Theta_0)
  }
  \,.
$$


=--

([Berger, theorem 1.12](#Berger))

### Weak $\omega$-categories

As a refinement of the above example:

In the Batanin (or Leinster) theory of $\infty$-categories, there is a universal contractible globular operad $f: K \to T(1)$, where each element $x \in K(n)$ is thought of as a _way_ of (weakly) pasting together the underlying shape $f(x)$. The contractibility implies that for every two different ways of pasting together the same shape, i.e., two elements $x, y \in K(n)$ such that $f(x) = f(y)$ and such that $x$ and $y$ have the same source and have the same target, there is an $(n+1)$-cell in $K(n+1)$ mediating between them, with source $x$ and target $y$, and which maps to the identity $(n+1)$-cell on $f(x)$. 

A [[Batanin ∞-category]] is a globular set with a $K$-algebra structure. 



## References

A review and characterization in terms of [[globular theories]] is in section 1 of 

* [[Clemens Berger]], _A cellular nerve for higher categories_, Advances in Mathematics 169, 118-175 (2002) ([pdf](http://math1.unice.fr/~cberger/nerve.pdf))
 {#Berger}

Other work on globular operads :

* [[Camell Kachour]], Operads of higher transformations for globular sets and for higher magmas, Published in Categories and General Algebraic Structures with Applications (2015). 


[[!redirects globular operads]]