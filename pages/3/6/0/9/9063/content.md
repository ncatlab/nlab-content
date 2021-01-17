
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
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

A cofiber sequence is the dual notion to a [[fiber sequence]].


## Definition

### Abstractly

For $\mathcal{C}$ an [[(∞,1)-category]] with [[(∞,1)-pushouts]], a sequence of [[morphisms]] $A \stackrel{f}{\to} B \to C$ is a _cofiber sequence_ if there is an [[(∞,1)-pushout]] square of the form

$$
  \array{
    A &\stackrel{f}{\to}& B
    \\
    \downarrow &\swArrow& \downarrow
    \\
    * &\to& C
  }
$$

in $\mathcal{C}$. We say that $C$ is the [[homotopy cofiber]] of $f$.

### Presentation

Under mild conditions on a [[category with weak equivalences]] presenting $\mathcal{C}$ (such as a [[model category]]), homotopy cofibers are presented by _[[mapping cones]]_. 

Specifically for cofiber sequences of [[topological spaces]] see at _[[topological cofiber sequence]]_.

## Examples

In a [[stable (∞,1)-category]], every [[fiber sequence]] is also a cofiber sequence and conversely.

### Non-examples

In the unstable case, most fiber sequences are not cofiber sequences or conversely.  For instance, if $0\to K\to G\to H \to 0$ is a [[short exact sequence]] of [[groups]], then the corresponding maps of [[classifying spaces]] $\mathbf{B}K \to \mathbf{B}G \to \mathbf{B}H$ always form a [[fiber sequence]], but not generally a cofiber sequence.

For a concrete counterexample, consider the short exact squence $0 \to \mathbb{Z}\xrightarrow{2} \mathbb{Z}\to \mathbb{Z}/2 \to 0 $.  Upon taking classifying spaces this becomes $S^1 \to S^1 \to RP^{\infty}$, in which the first map is a double cover whose cofiber is $RP^2$.

## Related concepts

* [[long exact sequence in homology]]

  * [[long exact sequence in generalized homology]]

* [[stable (∞,1)-category]]

[[!redirects cofiber sequences]]

[[!redirects cofibre sequence]]
[[!redirects cofibre sequences]]

[[!redirects homotopy cofiber sequence]]
[[!redirects homotopy cofiber sequences]]
[[!redirects homotopy cofibre sequence]]
[[!redirects homotopy cofibre sequences]]

[[!redirects long homotopy cofiber sequence]]
[[!redirects long homotopy cofiber sequences]]
[[!redirects long homotopy cofibre sequence]]
[[!redirects long homotopy cofibre sequences]]


[[!redirects homotopy cofiber]]
[[!redirects homotopy cofibers]]
[[!redirects homotopy cofibre]]
[[!redirects homotopy cofibres]]

[[!redirects cofibration sequence]]
[[!redirects cofibration sequences]]

[[!redirects homotopy cokernel]]
[[!redirects homotopy cokernels]]

[[!redirects homotopy co-fiber]]
[[!redirects homotopy co-fibre]]
[[!redirects homotopy co-fibres]]
[[!redirects homotopy co-fibers]]
[[!redirects homotopy co-kernel]]
[[!redirects homotopy co-kernels]]