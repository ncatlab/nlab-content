
#Contents#
* table of contents
{:toc}

## Idea

The notion of _twisted $\infty$-bundle_ is the generalization to [[nLab:higher geometry]] of the notion of [[nLab:twisted bundle]].

## Definition.

Let $\mathbf{H}$ be an [[(∞,1)-topos]], $G \in Grp(\mathbf{H})$ an [[∞-group]],  $V \in \mathbf{H}$ an object, and $\rho$ an [[∞-representation]] of $G$ on $V$, exhibited by a [[fiber sequence]]

$$
  \array{
    V &\to& V//G
    \\
    && \downarrow^{\mathrlap{\rho}}
    \\
    && \mathbf{B}G
  }
  \,,
$$ 

which is identified with the universal $V$-[[associated ∞-bundle]].

Then for $P \to X$ a $G$-[[principal ∞-bundle]], correspoding to a [[cocycle]] $g : X \to \mathbf{B}G$ with coefficients in the [[moduli ∞-stack]] of $G$-principal $\infty$-bundles, the [[∞-groupoid]] of [[sections]] of the [[associated ∞-bundle]] $P times_G V$ is equivalently the cocycle $\infty$-groupoid of $g$-[[twisted cohomology]] relative to $\rho$:

$$
  \Gamma_X(P\times_G V) \simeq \mathbf{H}_{/\mathbf{B}G}(g,\rho)
  \,.
$$

Each such cocycle may be understood as locally having coefficients in  $\Omega V$, but globally being _twisted_ by $P$. 

The geometric structure canonically associated to this is a (twisted $G$-equivariant) $\Omega V$-[[principal ∞-bundle]] $Q \to P$ on the total space $P$ of the twisting $\infty$-bundle, seen by applying the [[pasting law]] of [[(∞,1)-pullbacks]] to the [[pasting diagram]]

$$
  \array{
    P &\to& * 
    \\
    \downarrow && \downarrow
    \\
    P &\to& V &\to& * 
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    X &\stackrel{\sigma}{\to}& V//G &\to& \mathbf{B}G
  }
  \,.
$$

## Examples

(...)

## References

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- Theory, presentations and applications]]_

[[!redirects twisted infinity-bundles]]
