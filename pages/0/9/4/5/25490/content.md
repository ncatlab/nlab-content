
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[homotopy theory]], by an *$\mathcal{I}$-space* &lbrack;[Sagave & Schlichtkrull (2011)](#SagaveSchlichtkrull11)&rbrack; one means a [[functor]] $\mathcal{I} \to \mathcal{S}$ from

1. the [[category]] $\mathcal{I}$ of [[finite sets]] (including the [[empty set]]) with [[injective maps]] between them;

1. a category such as [[TopologicalSpaces]] or [[SimplicialSets]] which carries a [[classical model structure on topological spaces|classical]] [[model category structure]]  presenting plain [[homotopy types]].

The [[functor category]] $\mathcal{S}^{\mathcal{I}}$ of $\mathcal{I}$-spaces then carries a [[model category]]-[[structure]] whose [[weak equivalences]] are those [[natural transformations]] which induce [[weak homotopy equivalences]] on [[homotopy colimits]] over $\mathcal{I}$; and this turns out to be  [[Quillen equivalence|Quillen equivalent]] to the [[classical model structure on topological spaces|classical model structure]] via the [[colimit]]-functor

\begin{tikzcd}
  \mathcal{S}^{\mathcal{I}}
  \ar[
    rr, shift left=10pt,
    "{ \mathrm{colim} }"
  ]
  \ar[
    from=rr, shift left=10pt,
    "{ \mathrm{const} }"
  ]
  \ar[rr, phantom, "{ \scalebox{.7}{$\simeq_{\mathrm{Qu}}$} }"]
  &&
  \mathcal{S}
\end{tikzcd}

As such, $\mathcal{I}$-spaces are just another presentation of [[homotopy theory]].

However, via [[Day convolution]] of the evident [[symmetric monoidal category]]-[[structure]] on $\mathcal{I}$ (whose [[tensor product]] is [[disjoint union]] of [[finite sets]]) the [[functor category]] $\mathcal{S}^{\mathcal{I}}$ of $\mathcal{I}$-spaces becomes itself [[symmetric monoidal category|symmetric monoidal]].

This monoidal structure on $\mathcal{I}$-spaces is more homotopy-truthful than the (cartesian) monoidal structure on plain spaces: strictly [[commutative monoids]] [[monoid object|internal to]] $\mathcal{I}$-spaces serve to model all [[E-infinity space|$E_\infty$-spaces]].


## Related concepts

* [[E-infinity space|$E_\infty$-space]]

* [[model structure on parameterized spectra]]


## References

* {#SagaveSchlichtkrull11} [[Steffen Sagave]], [[Christian Schlichtkrull]], §1.1 and §3 in: *Diagram spaces and symmetric spectra*, Advances in Mathematics **231** 3-4 (2012) 2116-2193 &lbrack;[arXiv:1103.2764](https://arxiv.org/abs/1103.2764), [doi:10.1016/j.aim.2012.07.013](https://doi.org/10.1016/j.aim.2012.07.013)&rbrack;

Discussion mostly in relation to [[symmetric spectra]]

* [[Stefan Schwede]], Section 3.4 of: *[[Symmetric spectra]]* (2012) &lbrack;[pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf)&rbrack;

and [[parameterized spectra|paramterized]] [[symmetric spectra]]:

* {#HebestreitSagaveSchlichtkrull20} [[Fabian Hebestreit]], [[Steffen Sagave]], [[Christian Schlichtkrull]], *Multiplicative parametrized homotopy theory via symmetric spectra in retractive spaces*, Forum of Mathematics, Sigma **8** (2020) e16 &lbrack;[arXiv:1904.01824](https://arxiv.org/abs/1904.01824), [doi:10.1017/fms.2020.11](https://doi.org/10.1017/fms.2020.11)&rbrack;



[[!redirects I-spaces]]
