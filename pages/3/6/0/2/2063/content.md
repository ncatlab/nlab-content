
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

### Categories

In a 2-category we define **[[homotopy fibers]]** of a morphism $f: A \to B$ over a point $\ast \to B$ to be the [[weak pullback]] of the diagram

$$
  \array{
    A \times_B * &\to& *
    \\
    \downarrow && \downarrow_pt
    \\
    A &\stackrel{f}{\to}& B
  }
$$

or more precisely the iso-comma object. When we work this out in the case of the 2-category Cat, the homotopy fiber over an object $b \in B$ of a functor $f: A \to B$ is the category where:

* an object is a pair $(a,\alpha)$ consisting of an object $a \in A$ equipped with an isomorphism $\alpha: f(a) \to b$.
* a morphism from $(a,\alpha)$ to $(a', \alpha')$ is a morphism $f: a \to a'$ such that $\alpha' \circ F(f) = \alpha$.  

When $f$ is thought of as a [[forgetful functor]], the homotopy fiber over $b \in B$ should be thought of as the category of ways $b$ could arise as the underlying object of some object in $A$.  The following easy results then provide useful intuitions:

+-- {: .num_prop #homotopy_fibers_faithful}
###### Proposition

If the functor $f: A \to B$ is [[faithful]], all its homotopy fibers are preorders.
=--

+-- {: .num_prop #homotopy_fibers_conservative}
###### Proposition

If the functor $f: A \to B$ is [[conservative functor|conservative]], all its homotopy fibers are groupoids.
=--

and thus:

+-- {: .num_prop #homotopy_fibers_faithful_and_conservative}
###### Proposition

If the functor $f: A \to B$ is faithul and conservative all its homotopy fibers are equivalent to discrete categories.
=--

For example, there is a preorder of ways a set could arise as the underlying set of a topological space, but a mere set (or discrete category) of ways a set could arise as the underlying set of a group.

Examples along these lines serve as a useful warmup for [[homotopy fibers]] of maps between $(\infty,1)$-categories.

## Related concepts


* [[homotopy fiber]], [[fiber sequence]]

* [[cofiber]], [[homotopy cofiber]]

* [[kernel]], [[cokernel]]

* [[fiber type]]

[[!redirects fibre]]
[[!redirects fibres]]
[[!redirects fibers]]