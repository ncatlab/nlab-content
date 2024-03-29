
#Contents#
* table of contents
{:toc}

## Idea

Where a [[principal ∞-bundle]] is the "geometric" incarnation of a [[cocycle]] in [[cohomology]], more generally a _twisted $\infty$-bundle_ is the geometric incarnation of a cocycle in [[twisted cohomology]].

## Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Let $\hat G \to G$ in $Grp(\mathbf{H})$ be a morphism of [[∞-groups]] in $\mathbf{H}$, write $\mathbf{c} : \mathbf{B}\hat G \to \mathbf{B}G$ for the corresponding [[delooping]] and $\mathbf{B}A \to \mathbf{B}\hat G$ for the corresponding [[homotopy fiber]], so that we have a universal coefficient bundle

$$
  \array{
    \mathbf{B}A &\to& \mathbf{B}\hat G
    \\
    && \downarrow^{\mathrlap{\mathbf{c}}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

Then let $\phi : X \to \mathbf{B}G$ be a twisting cocycle with corresponding $G$-[[principal ∞-bundle]] $P \to X$; and let $\sigma : X \to \mathbf{B}\hat G$ be a [[cocycle]] in $\phi$-[[twisted cohomology]]. By the [[pasting law]] this induces a twisted $G$-equivariant $A$-principal $\infty$-bundle $\tilde P$ on the total space of $P$

$$
  \array{
    \tilde P &\to& * 
    \\
    \downarrow && \downarrow
    \\
    P &\stackrel{\tilde \sigma}{\to}& \mathbf{B}A &\to& * 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X 
     &\stackrel{\sigma}{\to}&
   \mathbf{B}\hat G
     &\stackrel{\mathbf{c}}{\to}&
   \mathbf{B}G
  }
  \,.
$$

This is the twisted $\infty$-bundle classified by $\sigma$

## Examples

* [[projective representation]]

* [[twisted bundle]]

* [[Jandl gerbe]]

* [[twisted differential string structure|twisted String 2-bundle]]


## Related concepts

* [[principal bundle]] / [[torsor]] / [[associated bundle]] / [[twisted bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[2-gerbe]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]] / [[∞-gerbe]], 
  
* [[vector bundle]]

* [[(∞,1)-vector bundle]] / [[(∞,n)-vector bundle]]

## References

Section I 4.3 in 

* [[schreiber:Principal ∞-bundles -- theory, presentations and applications]]

[[!redirects twisted ∞-bundle]]


[[!redirects twisted ∞-bundles]]
[[!redirects twisted infinity-bundles]]

