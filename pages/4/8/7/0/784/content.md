
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Segal space_ is a [[precategory object in an (∞,1)-category|pre-category object]] in [[∞Grpd]].

A genuine [[category object in an (∞,1)-category|category object]] in [[∞Grpd]] is a _[[complete Segal space]]_.  This is a way of speaking of [[(∞,1)-categories]].

## Definition

A **Segal space** $X_\bullet$
  is a [[simplicial topological space]] or [[bisimplicial set]]
  $X_\bullet : \Delta^{op} \to Top$ for which for all $m,n \in \mathbb{N}$ the square

$$
  \array{
    X_{m+n} &\stackrel{
      p^*_{0,\cdots, m}
    }{\to}& X_m
    \\
    {}^{\mathllap{p^*_{m, \cdots, m+n}}}\downarrow 
    && \downarrow^{\mathrlap{p^*_m}}
    \\
    X_n &\stackrel{p^*_0}{\to}& X_0
  }
$$

is a [[homotopy pullback]] square.

## Related notions

* [[reduced Segal space]], [[Segal category]], 

* [[complete Segal space]], [[model structure for complete Segal spaces]]

[[!redirects Segal spaces]]
