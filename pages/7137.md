
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Langlands correspondence
+--{: .hide}
[[!include Langlands correspondence -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _local Langlands conjectures_ are certain [[conjectures]] in the context of the [[Langlands program]]. Where the genuine [[Langlands correspondence]] concerns [[global fields]], the local Langlands correspondence concerns [[local fields]].

In the case of the [[algebraic group]] $GL_n$ (the [[general linear group]]), the local Langlands conjectures assert a correspondence between:

1. F-semisimple Weil-Deligne [[representations]] (see Def. \ref{WeilDeligneRepresentation} below) of the [[Weil group]] of a  [[local field]] $F$;

1. [[irrep|irreducible]] admissible [[representations]] of $GL_n(F)$ (see Def. \ref{IrreducibleAndAdmissibleSubgroups} below), 

generalizing  local [[class field theory]] from [[abelian group|abelian]] [[Galois groups]] to non-abelian Galois groups.

More generally, it states that for a [[local field]] $F$ and a [[reductive group]] $G$, the [[isomorphism classes]] of irreducible admissible representations of $G(F)$ are partitioned into _L-packets_ by the equivalence classes of _L-parameters_.

## Definitions:

We discuss some of the basic definitions, see also [Tate 77](#Tate77).

Throughout:

* $F$ is a [[p-adic field]] with $\kappa$ denoting its [[residue field]];

* $G$ is a [[reductive group]].

\begin{definition}\label{IrreducibleAndAdmissibleSubgroups}
**([[irreducible representations|irreducible]] and admissible representations)**
A [[linear representation]] of $G(F)$ on a [[vector space]] $V$ is called:

*  *[[irrep|irreducible]]* if the only $G(F)$-[[invariant subspaces]] are $0$ and $V$.

* *admissible* if for any [[open subspace|open]] [[subgroup]] $U$ of $G(F)$ the [[fixed subspace]] $V^{U}$ is [[finite-dimensional vector space|finite-dimensional]].

\end{definition}

\begin{definition}\label{WeilGroup}
**([[Weil group]])**\linebreak
 The *[[Weil group]]* $W_F$ is the subgroup of the [[Galois group]] $\mathrm{Gal}(\overline{F}/F)$ defined as the [[inverse image]] of [[Frobenius automorphisms]] $\mathrm{Frob}^{\mathbb{Z}}\subset \mathrm{Gal}(\overline{\kappa}/\kappa)$ under the [[surjective]] map $\mathrm{Gal}(\overline{F}/F)\to\mathrm{Gal}(\overline{\kappa}/\kappa)$.
\end{definition}

\begin{definition}\label{WeilDeligneRepresentation}
**([[Weil-Deligne representation]])**\linebreak
A *[[Weil-Deligne representation]]* is a pair $(\rho_{0},N)$ where $\rho_{0}:W_{F}\to GL_{n}(\mathbb{C})$ is a representation of the [[Weil group ]] (Def. \ref{WeilGroup}) and $N$ is a nilpotent _monodromy operator_ satisfying $\rho_{0}(\sigma)N\rho_{0}(\sigma)^{-1}=\left\Vert\sigma\right\Vert N$ for all $\sigma\in W_{F}$, where $\Vert\sigma\Vert$ is the [[valuation]] of the corresponding element of $F^{\times}$ under the isomorphism of local [[class field theory]].
\end{definition}

## Examples

### Local Langlands correspondence for $GL_1$

Let $F$ be a $p$-adic field. The only irreducible admissible representations of $GL_1(F)$ ($=F^\times$) are continuous group homomorphisms $\chi:F^\times\to\mathbb{C}^{\times}$. The $1$-dimensional Weil-Deligne representations $(\rho_{0},N)$ of $W_F$ must have monodromy operator $N=0$ and must factor through the abelianization $W_F^{\mathrm{ab}}$. The local Langlands correspondence in this case is the same as local class field theory, and sends $\chi$ to the Weil-Deligne representation $(\rho_{0},0)$, where $\rho_{0}$ is the composition $W_{F}\to W_{F}^{\mathrm{ab}}\xrightarrow{\mathrm{rec}^{-1}}F^{\times}\xrightarrow{\chi}\mathbb{C}^{\times}$, with $\mathrm{rec}:F^{\times}\xrightarrow{\sim}W_{F}^{\mathrm{ab}}$ being the Artin reciprocity map of local class field theory. 

### Local Langlands correspondence for $GL_2$

Let $F$ be a $p$-adic field. For $p\neq 2$, the irreducible admissible representations of $GL_2(F)$ are the following:

* Principal series representations $I(\chi_{1},\chi_{2})$ for $\chi_{1}/\chi_{2}\neq \Vert\cdot\Vert^{\pm 1}$.

* Special representations $S(\chi_{1},\chi_{1}\times\Vert\cdot\Vert)$.

* Finite-dimensional representations $\chi\circ\det$.

* "Base change" representations $BC_{E}^{F}(\psi)$ for $E$ a quadratic extension of $F$ and $\psi$ an admissible character $\psi:E\to\mathbb{C}^{\times}$.

Let $\rho_{i}:W_{F}\to \mathbb{C}^{\times}$ be the representation of the Weil group associated to the character $\chi_{i}:F^{\times}\to \mathbb{C}^{\times}$ by the local Langlands correspondence for $GL_1$. Then the local Langlands correspondence associates to each irreducible admissible representation of $GL_2(F)$ a $2$-dimensional Weil-Deligne representation as follows:

* To the principal series representation $I(\chi_{1},\chi_{2})$ we associate the Weil-Deligne representation $(\rho_{1}\oplus\rho_{2},0)$.

* To the special representation $S(\chi_{1},\chi_{1}\times\Vert\cdot\Vert)$, we associate the Weil-Deligne representation $\left(\begin{pmatrix}\Vert\cdot\Vert\rho_{1} & 0\\0 & \rho_{1}\end{pmatrix},\begin{pmatrix} 0 & 1\\0 & 0\end{pmatrix}\right)$.

* To the finite-dimensional representation $\chi_{1}\circ\det$, we associate the Weil-Deligne representation $\left(\begin{pmatrix}\rho_{1}\times\Vert\cdot\Vert^{1/2} & 0\\0 & \rho_{1}\times\Vert\cdot\Vert^{-1/2}\end{pmatrix},0\right)$.

* To the "base change" representation $BC_{E}^{F}(\psi)$ we associate the Weil-Deligne representation ($Ind_{W_{E}}^{W_{F}}\sigma,0$), where $\sigma$ is the unique nontrivial element of $\mathrm{Gal}(E/F)$.

## Geometrization

Fargues-Scholze have developed a geometric approach to the local Langlands conjecture in [FarguesScholze21](#FarguesScholze21).

## p-adic and mod p local Langlands

The $p$-adic (resp. mod $p$) local Langlands correspondence concerns $p$-adic (resp. mod p) representations of the absolute Galois group of a $p$-adic field $F$, as opposed to complex Weil-Deligne or $\ell$-adic representations. Currently the only known case is the case $GL_2(\mathbb{Q}_{p})$, see also [Breuil2010](#Breuil2010).

## Related concepts

* [[global analytic geometry]]

## References

See also:

* Wikipedia, _[Local Langlands conjectures](http://en.wikipedia.org/wiki/Local_Langlands_conjectures)_.

* Colin Bushnell, Guy Henniart, _The local Langlands conjecture for $GL(2)$_ 

* [Topics on Automorphic Forms](http://www.math.columbia.edu/~chaoli/docs/AutomorphicForm.html), course notes by Chao Li from a course taught by Jack Thorne
* [Kevin Buzzard's MSRI Summer School on automorphic forms](http://wwwf.imperial.ac.uk/~buzzard/MSRI/)

Basic definitions are discussed in:

* {#Tate77} [[John Tate]], *Number theoretic background*, in: *Automorphic forms, representations and L-functions*, Proc. Sympos. Pure Math., Oregon State Univ., Corvallis, Ore. (1977), Part 2, Proc. Sympos. Pure Math., XXXIII, pages 3–26. Amer. Math. Soc., Providence, RI ([ISBN:978-0-8218-3371-1](https://bookstore.ams.org/pspum-33-2), [pdf](http://www.math.ucsd.edu/~csorense/teaching/math205/Tate_Weil.pdf), [[TateNumberTheory.pdf:file]])

An approach via the [[Fargues-Fontaine curve]]:

*{#FarguesScholze21} [[Laurent Fargues]], [[Peter Scholze]], _Geometrization of the local Langlands correspondence_ ([arXiv:2102.13459](https://arxiv.org/abs/2102.13459))

The p-adic and mod p local Langlands correspondence is discussed in:

*{#Breuil2010}, Christophe Breuil, _The emerging p-adic Langlands program_


[[!redirects local Langlands conjectures]]

[[!redirects local Langlands program]]
[[!redirects local langlands program]]

[[!redirects local Langlands duality]]
[[!redirects local Langlands dualities]]

[[!redirects local Langlands correspondence]]
[[!redirects local Langlands correspondences]]
