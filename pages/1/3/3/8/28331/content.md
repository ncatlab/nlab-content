+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


\tableofcontents

## Idea

The *Kirby-Siebenmann invariant* controls the existence of [[PL manifold|PL structures]] on [[topological manifolds]]. The analogue concept controlling the existence of [[smooth structures]] on [[topological manifolds]] and [[PL manifold|piecewise linear (PL) manifolds]] are the [[Kervaire-Milnor groups]].

## Definition

Let $Top_n\coloneqq C^0(\mathbb{R}^n,\mathbb{R}^n)$ be the [[topological group]] of [[homeomorphisms]] ([[homeomorphism group]]) and $PL_n$ the [[topological group]] of [[PL homeomorphisms]] of [[Euclidean space]] $\mathbb{R}^n$. There is a canonical inclusion $PL_n\hookrightarrow Top_n$. Taking the [[cartesian product]] with the [[identity]] furthermore gives inclusions $Top_n\hookrightarrow Top_{n+1}$ and $PL_n\hookrightarrow PL_{n+1}$. An [[inductive limit]] yields [[topological groups]]:
$$
Top
\coloneqq\lim_{n\rightarrow\infty}Top_n;
$$
$$
PL
\coloneqq\lim_{n\rightarrow\infty}PL_n.
$$
There is an induced canonical inclusion $PL\hookrightarrow Top$. Their [[classifying spaces]] can be now be regarded to study the different structures: For a [[topological manifold]] $X$, its [[tangent bundle]] $TX$ is also a [[topological manifold]], which is classified by a continuous map $X\rightarrow BTop$. Analogous for a PL manifold, there is a classifying map $X\rightarrow BPL$. The canonical inclusion $BPL\hookrightarrow BTop$ shows that every PL is a topological structure.

## References

Named after the original discussion in:

* {#KirbySiebenmann77} [[Robion C. Kirby]], [[Laurence C. Siebenmann]], pages 23, 202, 252, 318 in: *Foundational Essays on Topological Manifolds, Smoothings and Triangulations*, Princeton University Press (1977) &lbrack;[doi:10.1515/9781400881505](https://doi.org/10.1515/9781400881505), [jstor:j.ctt1b9s024](https://www.jstor.org/stable/j.ctt1b9s024), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/ks.pdf)&rbrack;

Further descriptions:

* {#FreedUhlenbeck91} [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

See also:

* Wikipedia, _[Kirby-Siebenmann invariant](https://en.wikipedia.org/wiki/Kirby–Siebenmann_invariant)_

[[!redirects Kirby-Siebenmann class]]
[[!redirects Kirby-Siebenmann obstruction]]
[[!redirects KS invariant]]
[[!redirects KS class]]
[[!redirects KS obstruction]]