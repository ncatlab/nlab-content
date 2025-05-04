
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The generalization of the notion of [[flat connection]] from [[differential geometry]] to [[higher differential geometry]] and generally to [[higher geometry]].

## Definition

Given a [[cohesive (∞,1)-topos]] $(\esh \dashv \flat \dashv \sharp)$ with [[shape modality]] $\esh$ and [[flat modality]] $\flat$, a **flat $\infty$-connection** an an [[object]] $X$ with [[coefficients]] in an object $A$ is a morphism

$$
  \nabla \;\colon\; X \to \flat A
$$

or equivalently a morphism

$$
  \nabla \;\colon\; \esh(X) \to A
  \,.
$$

This is also sometimes called a _[[local system]]_ on $X$ with [[coefficients]] in $A$, or a _[[cocycle]]_ in [[nonabelian cohomology]] of $X$ with _constant_ [[coefficients]] $A$.


For more see at _[structures in a cohesive (∞,1)-topos -- flat ∞-connections](cohesive+%28infinity,1%29-topos+--+structures#FlatDifferentialCohomology)_.

## Examples

### Flat principal $\infty$-bundles

For $A = \mathbf{B}G$ the [[delooping]] of an [[∞-group]], flat $\infty$-connections with coefficients in $A$ are a special case of $G$-[[principal ∞-connections]].

### Flat $(\infty,1)$-vector bundles ($\infty$-local systems)

For $A = Core(Ch_k)$ the [[core]] of an [[(infinity,1)-category of chain complexes]], functors $\esh X \longrightarrow A$ are [[(infinity,1)-vector bundles|$(\infty,1)$-vector bundles]] with [[flat infinity-connections|flat $\infty$-connections]].

In parts of the literature this case is understood by default when speaking of "$\infty$-local systems". Other parts refer to this as "[[representations up to homotopy]]" (really: up to [[coherence|coherent]] [[higher homotopy]]).



## Related concepts

* [[connection on a smooth principal infinity-bundle]]

* [[flat connection]]

* [[Galois theory]]

* [[local system]]

* [[constant infinity-stack]]

* [[Riemann-Hilbert correspondence]]


## References

### General

On higher version of [[Galois theory]] via [[automorphisms]] of [[locally constant infinity-stacks|locally constant $\infy$-stacks]]:

* [[Bertrand Toën]], *Vers une interprétation galoisienne de la théorie de l'homotopie*, Cahiers de Topologie et Géométrie Différentielle Catégoriques **43** 4 (2002) 257-312 &lbrack;[numdam:CTGDC_2002__43_4_257_0](http://www.numdam.org/item/?id=CTGDC_2002__43_4_257_0)&rbrack;

* {#PoleselloWaschkies05} [[Pietro Polesello]], [[Ingo Waschkies]], *Higher monodromy*, Homology, Homotopy and Applications **7** 1 (2005) 109-150 &lbrack;[arXiv:0407507](http://arxiv.org/abs/math/0407507), [eudml:51918](https://eudml.org/doc/51918)&rbrack;

In view of [[cohesive homotopy theory]]:

* [[schreiber:differential cohomology in a cohesive topos|dcct §3.8.5]]


### Flat $(\infty,1)$-vector bundles ($\infty$-local systems)
  {#ReferencesFlatInfinityVectorBundles}


On [[infinity-local systems|$\infty$-local systems]] in the sense of [[(infinity,1)-vector bundles|$(\infty,1)$-vector bundles]] with [[flat infinity-connections|flat $\infty$-connections]]:

Component-definitions are due to:

* [[Camilo Arias Abad]], [[Florian Schätz]]: *The $A_\infty$ de Rham theorem and integration of representations up to homotopy*, International Mathematics Research Notices, **2013** 16 (2013) 3790–3855 &lbrack;[arXiv:1011.4693](https://arxiv.org/abs/1011.4693), [doi:10.1093/imrn/rns166](https://doi.org/10.1093/imrn/rns166)&rbrack;

* {#BlockSmith14} [[Jonathan Block]], [[Aaron M. Smith]], *The higher Riemann--Hilbert correspondence*, Advances in Mathematics **252** (2014) 382-405 &lbrack;[arXiv:0908.2843](https://arxiv.org/abs/0908.2843), [doi:10.1016/j.aim.2013.11.001](https://doi.org/10.1016/j.aim.2013.11.001)&rbrack;

Identification with [[(infinity,1)-functors|$(\infty,1)$-functors]] is made explicit in:

* [Block & Smith (2014), below Def. 2.3 (§2.2 in the preprint)](#BlockSmith14)

* [[Manuel Rivera]], [[Mahmoud Zeinalian]], §5 of: *The colimit of an $\infty$-local system as a twisted tensor product*, Higher Structures **4** 1 (2020) 33-56  &lbrack;[arXiv:1805.01264](https://arxiv.org/abs/1805.01264), [higher-structures:Vol4Iss1](https://higher-structures.math.cas.cz/api/files/issues/Vol4Iss1/RiveraZeinalian)&rbrack;

and construction of a [[model category]] of $\infty$-local systems:

* [[Hisham Sati]], [[Urs Schreiber]], §3 of: *[[schreiber:Entanglement of Sections]]* &lbrack;[arXiv:2309.07245](https://arxiv.org/abs/2309.07245)&rbrack;

Enhancement of the [[Chern-Weil homomorphism]] from [[ordinary cohomology]]-groups to [[dg-categories]] of [[infinity-local systems|$\infty$-local systems]]:

* [[Camilo Arias Abad]], Santiago Pineda Montoya, Alexander Quintero Velez, *Chern-Weil theory for $\infty$-local systems*, Trans. Amer. Math. Soc. **377** (2024) 3129-3171 &lbrack;[arXiv:2105.00461](https://arxiv.org/abs/2105.00461), [doi:10.1090/tran/9068](https://doi.org/10.1090/tran/9068)&rbrack;


### $\infty$-Local systems as topological quantum state spaces

On constructions of ([[extended TQFT|extended]], [[Dijkgraaf-Witten theory|Dijkgraaf-Witten-type]]) [[functorial field theory|functorial]] [[topological quantum field theories]] whose (relative) [[quantum state spaces]] are $\infty$-local systems (possibly in more general [[(infinity,1)-category|$(\infty,1)$-categories]] that [[(infinity,1)-category of chain complexes|of chain complexes]]):

* [[Daniel Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]]: *[[Topological Quantum Field Theories from Compact Lie Groups]]*, in P. R. Kotiuga (ed.), *A celebration of the mathematical legacy of Raoul Bott*,  AMS (2010) 367-403 &lbrack;[arXiv:0905.0731](http://arxiv.org/abs/0905.0731), [doi:10.1090/crmp/050](https://doi.org/10.1090/crmp/050), [ISBN:978-0-8218-4777-0](https://bookstore.ams.org/view?ProductCode=CRMP/50)&rbrack;

* [[Jeffrey C. Morton]]: *Extended TQFT, Gauge Theory, And 2-Linearization*, J. Homotopy Relat. Struct. **10** (2015) 127–187 &lbrack;[arXiv:1003.5603](https://arxiv.org/abs/1003.5603), [doi:10.1007/s40062-013-0047-2](https://doi.org/10.1007/s40062-013-0047-2)&rbrack;

* [[Urs Schreiber]]: *[[schreiber:Quantization via Linear homotopy types]]*, talk notes (2014) &lbrack;[arXiv:1402.7041](https://arxiv.org/abs/1402.7041)&rbrack;

* [[Daniel S. Freed]], [[Gregory W. Moore]], [[Constantin Teleman]], §A.2 in: *Topological symmetry in quantum field theory*, Quantum Topology, **15** 3/4 (2023) 779–869 &lbrack;[arXiv:2209.07471](https://arxiv.org/abs/2209.07471), [doi:10.4171/qt/223](https://doi.org/10.4171/qt/223)&rbrack;






[[!redirects flat infinity-connections]]

[[!redirects flat ∞-connection]]
[[!redirects flat ∞-connections]]

[[!redirects flat infinity-vector bundle]]
[[!redirects flat infinity-vector bundles]]
[[!redirects flat ∞-vector bundle]]
[[!redirects flat ∞-vector bundles]]


[[!redirects infinity-local system]]
[[!redirects infinity-local systems]]

[[!redirects ∞-local system]]
[[!redirects ∞-local systems]]


[[!redirects flat (∞,1)-bundle]]
[[!redirects flat (∞,1)-bundles]]

[[!redirects flat (infinity,1)-bundle]]
[[!redirects flat (infinity,1)-bundles]]

[[!redirects flat principal ∞-connection]]
[[!redirects flat principal ∞-connections]]
[[!redirects flat principal infinity-connection]]
[[!redirects flat principal infinity-connections]]

[[!redirects flat ∞-bundle]]
[[!redirects flat ∞-bundles]]

[[!redirects flat infinity-bundle]]
[[!redirects flat infinity-bundles]]
