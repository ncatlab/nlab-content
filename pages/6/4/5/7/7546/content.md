
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

## Definition

For $X$ a [[simplicial set]], for $x : \Delta[0] \to X$ a point in $X$, and for $n \in \mathbb{N}$, the **$n$th Eilenberg subcomplex** $E_n(X,x)$ of $X$ at $x$ is the [[fiber]] of the $(n-1)$-[[coskeleton]]-projection over $x$, hence the [[pullback]]
 
$$
  \array{
    E_n(X,x) &\to& X
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{x}{\to}& cosk_{n-1}X
  }
  \,.
$$

By the [[skeleton]]/[[coskeleton]] [[adjunction]] $(sk_{n-1} \dashv cosk_{n-1})$ the $n$th Eilenberg subcomplex is the [[subobject]] of $X$ consisting of those simplices whose $(n-1)$-skeleton is constant on the point $x$.



## Properties

### Restriction to Kan complexes

If $X$ is a [[Kan complex]] , then so is $E_n(X,x)$ for all $n \in \mathbb{N}$ and $x \in X_0$. 

### Relation to $n$-connected objects

If $X$ is a Kan complex and [[n-connected|(n-1)-connected]], then the canonical morphism $E_n(X,x) \to X$ is a [[homotopy equivalence]].

See ([May, theorem 8.4](#May)).

### Relation to pointed $n$-connected objects

The inclusion $sSet_{(n-1)} \hookrightarrow sSet^{*/}$ of $n$-fold [[reduced simplicial set]]  (those with a single $k$-simplex for all $k \leq n-1$) into all [[pointed object|pointed]] simplicial sets is a [[coreflective subcategory]] with coreflector being forming of the $n$th Eilenberg subcomplex

$$
  sSet^{*/}
    \underoverset
      {\underset{E_n(-,*)}{\longrightarrow}}
      {\overset{}{\hookleftarrow}}
      {\bot}
  sSet_{n-1}
  \,.
$$

the [[counit of an adjunction|counit]] of this adjunction is the defining inclusion $E_n(X,*) \to X$.

So if $(* \to X) \in sSet^{*/}$ such that $X \in sSet$ is a [[Kan complex]] and [[n-connected|(n-1)-connected]], then the [[counit of an adjunction|counit]] $E_n(X,*) \to X$   is a [[homotopy equivalence]].

Accordingly, the coreflection presents the inclusion of [[n-connected|(n-1)-connected]] [[pointed object|pointed]] [[infinity-groupoids]] into all [[pointed object|pointed]] [[infinity-groupoids]]

$$
  \infty Grpd_{\geq (n-1)}^{*/} \hookrightarrow \infty Grpd^{*/}
  \,.
$$

## Related concepts

* [[Whitehead tower]], [[Postnikov tower]]

## References

Around def. 8.3 in 

* [[Peter May]], _Simplicial objects in algebraic topology_ ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu))
 {#May}

[[!redirects Eilenberg subcomplexes]]

