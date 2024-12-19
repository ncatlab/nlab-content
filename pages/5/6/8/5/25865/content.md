

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In the context of [[motivic integration]], the term _Greenberg scheme_ refers to one of multiple generalizations of [[arc spaces]] (here referred to as "arc schemes"). Greenberg schemes are built on [[schemes]] over a _complete_ [[discrete valuation ring]] (DVR). In the locally Noetherian setting, if $R$ is a complete DVR then  Greenberg schemes of [[formal schemes]] generalize this prior notion of Greenberg schemes. Greenberg schemes associated to such formal schemes are the setting for motivic integration.

## Definitions

Let $R$ be a complete DVR, let $\mathfrak{m}$ be its unique [[maximal ideal]], and let $k=R/\mathfrak{m}$ be its residue field.

### The ring schemes $\mathscr{R}_n$

For every non-negative integer $n\ge0$, the functor $\mathscr{R}_n\colon\mathbf{Alg}_k\to\mathbf{Ring}$ from the category of $k$-algebras to the category of rings given by
$$
A\mapsto A\otimes_k R_n = A\otimes_k R/\mathfrak{m}^{n+1}
$$
is a [[representable functor]] if $R$ is equicharacteristic (that is, $R$ and $k$ have the same characteristic). Denote by $\mathscr{R}_\infty$ the limit of these functors, which is again representable. As schemes, these are identified with $\mathbb{A}_k^{n+1}$ and $\mathbb{A}_k^\infty$, respectively, but the ring scheme structures endowed on $\mathscr{R}_n$ and $\mathscr{R}_\infty$ are not the same as the usual ones on affine space.

In the mixed characteristic case, let $W(-)$ be the functor which assigns a $k$-algebra to its [[ring of Witt vectors]]. The functor
$$
\mathscr{R}_n\colon A\mapsto W(A)\otimes_{W(k)} R_n
$$
is not always representable, but its fpqc-sheafification (its [[sheafification]] over the [[fpqc site]]) _is_ representable; in this case, we replace the functor $\mathscr{R}_n$ with its fpqc-sheafification.

### Functorial description of $\mathrm{Gr}_n$

Given a $k$-scheme $(Y,\mathscr{O}_Y)$, define the [[locally ringed space]] $h_n(Y)=(Y,\mathscr{R}_n(\mathscr{O}_Y))$ whose structure sheaf is valued in $R_n$-algebras, given by
$$
U\mapsto\mathrm{Hom}_k(U,\mathscr{R}_n)
$$
which has the structure of an $R_n$-algebra given by the ring scheme structure on $\mathscr{R}_n$. $h_n(-)$ is isomorphic to the functor $(-)\times_{k} R_n$, and thus $h_n(Y)$ is an $R_n$-scheme.

With this construction, the _Greenberg functor_ $\mathrm{Gr}_n$ can be defined abstractly as the right adjoint to the functor $h_n$; that is, to every $R$-scheme $X$, let 
$$
\mathrm{Gr}_n(X)(-)\coloneqq
\mathrm{Hom}_{\mathbf{Sch}_R}(h_n(-), X).
$$ 
This functor is representable; write the corresponding scheme as $\mathrm{Gr}_n(X)$.

The Greenberg schemes $\mathrm{Gr}_n(X)$ form an inverse system, where the morphisms $\mathrm{Gr}_m(X)\to\mathrm{Gr}_n(X)$ for $m\ge n$ come from the obvious natural transformations $h_n\Rightarrow h_m$. The limit of these functors
$$
\mathrm{Gr}_\infty(X)(-)\coloneqq
\lim_n\,\mathrm{Hom}_{\mathbf{Sch}_R}(h_n(-),X)
$$
is also represented by a $k$-scheme.

### Greenberg schemes of formal schemes

To any locally Noetherian $R$-adic formal scheme $\mathfrak{X}$, one can define the _Greenberg scheme_ $\mathrm{Gr}_n(\mathfrak{X})$ by simply applying the already constructed Greenberg functor to $\mathfrak{X}_n=\mathfrak{X}\times_{R} R_n$. Similarly, the limit of these functors
$$
\mathrm{Gr}_\infty(\mathfrak{X})\coloneqq
\lim_n\,\mathrm{Gr}_n(\mathfrak{X})
$$
again is representable, hence defines a $k$-scheme, called the _Greenberg scheme_ of $\mathfrak{X}$.

This construction generalizes Greenberg schemes associated to locally Noetherian $R$-schemes, and therefore generalizes, in particular, the construction of arc schemes.

## Related concepts

* [[arc space]]

* [[motivic integration]]

* [[p-adic integration]]

* [[motivic cohomology]]

## References

{#CNS18} Antoine Chambert-Loir, Johannes Nicaise, Julien Sebag, _Motivic integration_, Progress in Mathematics 325 Birkhaeuser 2018 ([doi:10.1007/978-1-4939-7887-8](https://doi.org/10.1007/978-1-4939-7887-8))