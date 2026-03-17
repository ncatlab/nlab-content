+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* tabe of contents
{:toc}

## Idea

*Spinʰ bordism* is a [[B-bordism]] for the [[tangential structure]] ([[(B,f)-structure]]) being the [[spinʰ structure]]. Its [[bordism homology theory]] and [[cobordism cohomology theory]] are described by the [[Thom spectrum]] [[MSpinʰ]].

Its definition is fully analogous to that of [[spin bordism]]. Similarily, there are *spinʰ bordism groups*:
$$
\Omega_n^{Spin^\mathrm{h}}
\coloneqq\pi_n MSpin^\mathrm{h}
=\lim_{k\rightarrow\infty}\pi_{n+k} MSpin^\mathrm{h}_k;
$$

Unlike for spin or [[spinᶜ structure]], there is not in general a spinʰ structure on the direct sum of two spinʰ vector bundles. Thus the direct product of spinʰ manifolds in general doesn't admit a spinʰ structure. See e.g. [Albanese-Milivojević](#AlbaneseMilivojević), Example 2.8.

For many B-bordism theories, a B-structure on the direct sum of two B-structured vector bundles is used to define a [[commutative ring spectrum]] structure on the Thom spectrum MB. The previous paragraph implies this argument does not work for [[MSpinʰ]] &ndash; and indeed, MSpinʰ does not even have a homotopy ring spectrum structure. If it did, the $\pi_*(\mathbb{S})$-module structure on $\pi_*(\mathrm{MSpin}^h)$ would refine to a $\pi_*(\mathbb{S})$-algebra structure, but if $\eta\in\pi_1(\mathbb{S})\cong\mathbb{Z}/2$ denotes the nonzero element, then $\eta\cdot 1 = 0\in\pi_1(\mathrm{MSpin}^h)$ and $\eta\cdot[\mathbb{HP}^1]\ne 0$ in $\pi_5(\mathrm{MSpin}^h)$, which follows from the spinʰ bordism computations of [Freed-Hopkins](#FreedHopkins).

However, the direct sum of the spinʰ bordism groups
$$
\Omega^{Spin^\mathrm{h}}
\coloneqq\bigoplus_{n\in\mathbb{N}}\Omega_n^Spin^{\mathrm{h}}.
$$
is a module over the [[spin bordism]] ring, and likewise MSpinʰ is an MSpin-module spectrum.



## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

* {#FreedHopkins} [[Daniel S. Freed]] and [[Michael J. Hopkins]], _Reflection positivity and invertible topological phases_, Geometry and Topology 25 (2021). [arXiv:1604.06527](https://arxiv.org/abs/1604.06527), &lbrack;[doi:10.2140/gt.2021.25.1165](https://doi.org/10.2140/gt.2021.25.1165)&rbrack;

* {#AlbaneseMilivojević} [[Michael Albanese]] and [[Aleksandar Milivojević]], _Spinʰ and further generalisations of spin_, Journal of Geometry and Physics 164 (2021). [arXiv:2008.04934](https://arxiv.org/abs/2008.04934), &lbrack;[doi:10.1016/j.geomphys.2021.104174](https://doi.org/10.1016/j.geomphys.2021.104174)&rbrack;

[[!redirects Spinʰ bordism]]
[[!redirects spinʰ cobordism]] 
[[!redirects Spinʰ cobordism]]

[[!redirects spinʰ bordism group]] 
[[!redirects Spinʰ bordism group]]
[[!redirects spinʰ bordism groups]] 
[[!redirects Spinʰ bordism groups]]
[[!redirects spinʰ bordism ring]] 
[[!redirects Spinʰ bordism ring]]

[[!redirects spinʰ bordism homology]] 
[[!redirects Spinʰ bordism homology]]
[[!redirects spinʰ bordism homology theory]] 
[[!redirects Spinʰ bordism homology theory]]

[[!redirects spinʰ cobordism cohomology]] 
[[!redirects Spinʰ cobordism cohomology]]
[[!redirects spinʰ cobordism cohomology theory]] 
[[!redirects Spinʰ cobordism cohomology theory]]

[[!redirects spinh bordism]]
[[!redirects Spinh bordism]]
[[!redirects spinh cobordism]] 
[[!redirects Spinh cobordism]]

[[!redirects spinh bordism group]] 
[[!redirects Spinh bordism group]]
[[!redirects spinh bordism groups]] 
[[!redirects Spinh bordism groups]]
[[!redirects spinh bordism ring]] 
[[!redirects Spinh bordism ring]]

[[!redirects spinh bordism homology]] 
[[!redirects Spinh bordism homology]]
[[!redirects spinh bordism homology theory]] 
[[!redirects Spinh bordism homology theory]]

[[!redirects spinh cobordism cohomology]] 
[[!redirects Spinh cobordism cohomology]]
[[!redirects spinh cobordism cohomology theory]] 
[[!redirects Spinh cobordism cohomology theory]]