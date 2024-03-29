
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _fiber_ of a [[morphism]] or [[bundle]] $f : E \to B$ over a [[point]] of $B$ is the collection of [[generalized element|elements]] of $E$ that are mapped by $f$ to this point.   

## Definition

Fibers make sense in any category with a terminal object $*$ and pullbacks.  For $f : A \to B$ a [[morphism]] in such a [[category]] and $B$ equipped with the [[structure]] of a [[pointed object]] $pt : * \to B$, the **fiber** of $f$ is the [[fiber product]] of $f$ with $pt$, hence the [[pullback]]

$$
  \array{
    A \times_B * &\to& *
    \\
    \downarrow && \downarrow_pt
    \\
    A &\stackrel{f}{\to}& B
  }
$$

## Examples

### Bundles

Given a [[bundle]] $p: E \to B$ and a [[global element]] $x: 1 \to B$, the __fibre__ or __fiber__ $E_x$ of $(E,p)$ over $x$ is the [[pullback]]
$$ \array {
   E_x        & \to             & E \\
   \downarrow &                 & \downarrow_p \\
   1          & \stackrel{x}\to & B
} $$
if it exists.

In a [[fiber bundle]], all fibres are [[isomorphism|isomorphic]] to some standard fibre $F$ in a coherent way.

### Kernels

In an [[additive category]] fibers over the [[zero object]] are called _[[kernels]]_.

### Fibers of a sheaf of modules

The fiber of a sheaf $\mathcal{E}$ of $\mathcal{O}$-modules over a [[locally ringed space]] $(X,\mathcal{O})$ at a point $x \in X$ is defined as the vector space $\mathcal{E}(x) \coloneqq \mathcal{E}_x \otimes_{\mathcal{O}_x} k(x)$ over the [[residue field]] $k(x)$. If $\mathcal{E}$ is [[quasicoherent sheaf|quasicoherent]], the associated vector bundle of the fiber is the pullback of the associated vector bundle of $\mathcal{E}$:
$$ \array {
   V(\mathcal{E}(x)) = \mathrm{Spec} \mathrm{Sym} \mathcal{E}(x)
     & \to
     & \underline{Spec}_X \mathrm{Sym} \mathcal{E} = V(\mathcal{E}) \\
   \downarrow & & \downarrow \\
   \mathrm{Spec} k(x) & \to & X
} $$



## Related concepts

* [[essential fiber]]

* [[homotopy fiber]], [[fiber sequence]]

* [[cofiber]], [[homotopy cofiber]]

* [[kernel]], [[cokernel]]

* [[fiber type]]

[[!redirects fibre]]
[[!redirects fibres]]
[[!redirects fibers]]