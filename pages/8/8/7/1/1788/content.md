
The following over/underlines recently come out tiny when viewed in  

* Chrome, Edge and Opera 

while they still come out as expected in 

* Firefox 

(at least on the systems we tried in discussion [here](https://nforum.ncatlab.org/discussion/12362/twisted-arrow-1category/?Focus=110459#Comment_110459)):

* "`$\overline{ThisShouldRenderWithALooongOverline}$`" 

  renders as: 

  "$\overline{ThisShouldRenderWithALooongOverline}$"

* "`$\overline{ThisShouldRenderWithALooongUnderline}$`" 

  renders as: 

  "$\underline{ThisShouldRenderWithALooongUnderline}$"

Specifically, the rendering with Chrome, Edge and Opera looks (except for horizontal positioning) like that of the `\bar` command:

* "`$\bar{ThisShouldRenderWithATinyOverline}$`" 

  renders as: 

  "$\bar{ThisShouldRenderWithATinyOverline}$"

\linebreak

## Idea

What is called *Hodge-filtered cohomogy* by [Hopkins & Quick (2014)](#HopkinsQuick14) is the variant of [[differential generalized cohomology]] obtained by passing from real [[differential geometry]] to [[complex geometry]]: 

Where [[differential cohomology]] by default  pairs a given  
[[Whitehead-generalized cohomology theory]] ([[spectrum]]) $E$ of [[underlying]] [[topological spaces]] with the degree-filtered $E_\bullet \otimes \mathbb{R}$-valued [[de Rham complexes]] of [[differential forms]] on real [[smooth manifolds]], the Hodge-filtered variant pairs instead with the [[Hodge filtration|Hodge filtered]] $E_\bullet \otimes \mathbb{C}$-valued [[Dolbeault complexes]].

## References

### General

The general concept of Hodge-filtered [[differential cohomology]] and introducing the special case of Hodge-filtered [[complex cobordism cohomology]]:

* {#HopkinsQuick14} [[Michael J. Hopkins]], [[Gereon Quick]], *Hodge filtered complex bordism*, Journal of Topology **8** 1 (2014) 147-183 &lbrack;[arXiv:1212.2173](https://arxiv.org/abs/1212.2173), [doi:10.1112/jtopol/jtu021](https://doi.org/10.1112/jtopol/jtu021)&rbrack;

### Hodge filtered ordinary case

The case of Hodge-filtered [[integral cohomology|integral]][[ordinary cohomology]] is the original definition of *[[Deligne cohomology]]*, see there for references.

### Hodge-filtered complex cobordism

The case of Hodge filtered [[differential cobordism cohomology theory|differential]] [[MU]]-[[cobordism cohomology theory]]

* [Hopkins & Quick (2014), §5](#HopkinsQuick14)

Introduction and survey:

* [[Gereon Quick]], *Geometric Hodge filtered complex cobordism*, [talk at](Center+for+Quantum+and+Topological+Systems#QuickMar2023) *[[CQTS]]* (March 2023) &lbrack;video:[YT](https://www.youtube.com/watch?v=pMu0gT5kIBo)&rbrack;

A geometric cocycle model:

* [[Knut B. Haus]], [[Gereon Quick]], *Geometric Hodge filtered complex cobordism* &lbrack;[arXiv:2210.13259](https://arxiv.org/abs/2210.13259)&rbrack;

Refinement of the [[Abel-Jacobi map]] to [[Hodge filtration|Hodge filtered]] [[differential cobordism cohomology theory|differential]] [[MU]]-[[cobordism cohomology theory]]:

* [[Gereon Quick]], *An Abel-Jacobi invariant for cobordant cycles*,
Documenta Mathematica **21** (2016) 1645–1668 &lbrack;[arXiv:1503.08449](https://arxiv.org/abs/1503.08449)&rbrack;


On [[Umkehr maps]] in this context:

* [[Knut Bjarte Haus]], [[Gereon Quick]], *Geometric pushforward in Hodge filtered complex cobordism and secondary invariants* &lbrack;[arXiv:2303.15899](https://arxiv.org/abs/2303.15899)&rbrack;







