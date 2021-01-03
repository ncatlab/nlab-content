
#Contents#
* table of contents
{:toc}

## Idea

Where a [[simplicial object]] is a [[functor]] $\Delta^{op} \to \mathcal{C}$ out of the [[opposite category]] of the [[simplex category]], a cosimplicial object is a functor $\Delta \to \mathcal{C}$ out of the simplex category itself.

## Properties

### Simplicial enrichment
 {#SimplicialEnrichment}

When $\mathcal{C}$ has [[finite limits]] and finite [[colimits]], then $\mathcal{C}^{\Delta}$ is canonically a [[simplicially enriched category]] with is [[tensoring|tensored]] and [[powering|powered]] over [[sSet]]. This is called the _external simplicial structure_ in ([Quillen 67, II.1.7](#Quillen67)). Review includes ([Bousfield 03, section 2.10](#Bousfield03)).
 

More generally, for any $\mathcal{C}$, we can make $\mathcal{C}^{\Delta}$ into a simplicially enriched category using the [[end]] formula
$$\underline{\mathcal{C}^{\Delta}} (X, Y)_m = \int_{[n] : \Delta} (\mathcal{C} (X^n, Y^n))^{\Delta^m_n}$$
with composition inherited from $\mathcal{C}$ and $\Delta$.

## Related concepts

* [[cosimplicial algebra]]

## References

* {#Quillen67} [[Daniel Quillen]], _Homotopical Algebra_, Lecture Notes in Mathematics, vol. 43, Springer-Verlag, 1967

* [[Dai Tamaki]], [[Akira Kono]], Appendix A in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))


* {#Bousfield03} [[Aldridge Bousfield]], _Cosimplicial resolutions and homotopy spectral sequences in model categories_ ([arXiv:0312531](http://arxiv.org/abs/math/0312531))

[[!redirects cosimplicial objects]]


[[!redirects category of cosimplicial objects]]
[[!redirects categories of cosimplicial objects]]
