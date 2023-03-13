
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

This is a joint generalization of [[determinants]] and [[permanent|permanents]].

If $(a_{i,j}) \in \mathcal{M}_{n,p}(R)$ where $R$ is a [[commutative ring]] and if $\lambda \vdash n$ is a [[partition]] of $n$, we define:

$$
Imm_{\lambda}(A) = \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\chi_{\lambda}(\sigma)a_{i,\sigma(i)}
$$

where $\chi_{\lambda}$ is the [[character]] of the [[irreducible representation]] of the [[symmetric group]] $\mathfrak{S}_{n}$ associated to $\lambda$.

## Related entries

* [[determinant]]
* [[permanent]]

## References

* [Wikipedia entry](https://en.wikipedia.org/wiki/Immanant)