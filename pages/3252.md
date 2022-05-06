
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _subgroup_ of a [[group]] $G$ is a "smaller" group $K$ sitting inside $G$.

## Definition

A _subgroup_ is a [[subobject]] in the [[category]] [[Grp]] of [[group]]s: a [[monomorphism]] of groups

$$
  K \hookrightarrow G
  \,.
$$

Here $K$ is _a subgroup of $G$_. 

## Special cases

* [[normal subgroup]]

* [[stabilizer subgroup]]

* [[maximal compact subgroup]]

* [[torsion subgroup]]

* [[Borel subgroup]]

* [[parabolic subgroup]]

* [[generalized Fitting subgroup]]

## Properties

### Of free groups

Every subgroup of a [[free group]] is itself free. This is the statement of the _[[Nielsen-Schreier theorem]]_.

### Of Lie groups

For $H \hookrightarrow G$ a sub-[[Lie group]] inclusion write $\mathbf{B}H  \to \mathbf{B}G$ for the induced map on [[delooping]] [[Lie groupoids]]. The [[homotopy fiber]] of this map (in [[Smooth∞Grpd]]) is the [[coset space]] $G/H$: there is a [[homotopy fiber sequence]]

$$
  G/H \to \mathbf{B}H \to \mathbf{B}G
  \,.
$$

Now let $H \hookrightarrow K \hookrightarrow G$ be a sequence of two subgroup inclusions. By the above this yields the [[diagram]]

$$
  \array{
    K/H &\to& G/H &\to& G/K 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}H &\to& \mathbf{B}H &\to& \mathbf{B}K
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}K &\to& \mathbf{B}G &\to& \mathbf{B}G
  }
$$

## Examples

* [[centralizer subgroup]]

* [[normalizer subgroup]]

* [[stabilizer subgroup]]

* [[conjugate subgroup]]

* [[congruence subgroup]]


## Related concepts

* [[lattice of subgroups]]

* [[maximal subgroup]]

* [[index of a subgroup]]

* [[Klein geometry]], [[Cartan geometry]]

* [[BN-pair]]

## References

See also

* Wikipedia, _[Subgroup](https://en.wikipedia.org/wiki/Subgroup)_



[[!redirects subgroup]]
[[!redirects subgroups]]
