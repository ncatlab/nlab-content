
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The *hook length formula* counts the number of standard [[Young tableaux]] with fixed underlying [[Young diagram]]. This number is also equal to the dimension of the [[irreducible representation]] of the [[symmetric group]] $Sym(n)$ corresponding to $\lambda$, a partition of $n$.

## Details

Given a [[Young diagram]], the *hook* at any one of its boxes is the collection of boxes to the right and below that box, and including the box itself. We write "$\ell hook$" for the *length* of such a hook, i.e. for the number of boxes it contains.

Then given a Young diagram corresponding to a partition $\lambda \vdash n$. Let $f^{\lambda}$ be the corresponding number of standard Young tableaux. Then

$$
f^{\lambda} = \frac{n!}{\prod_{u: \lambda} \ell hook(u)}.
$$

## Related concepts

* [[hook-content formula]]

## References

* Yufei Zhao, _Young Tableaux and the Representations of the Symmetric Group_, ([pdf](https://yufeizhao.com/research/youngtab-hcmr.pdf))