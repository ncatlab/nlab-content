

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

For **inner derivation Lie 2-algebra** $inn(\mathfrak{g})$ of a [[Lie algebra]] $\mathfrak{g}$ is the ([[strict Lie 2-algebra|strict]]) [[Lie 2-algebra]] equivalently given as

* the [[dg-Lie algebra]] of contractions $\iota_x$ and inner derivations $\mathcal{L}_x = [d_{CE},x]$ acting on the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$;

* the [[differential crossed module]] $(\mathfrak{g} \stackrel{Id}{\to} \mathfrak{g})$ with the action being the [[adjoint action]] of $\mathfrak{g}$ on itself;

* the dual of the [[Weil algebra]] $W(\mathfrak{g})$.

In the first formulation this may be identified with the [[dg-Lie algebra]] whose

* elements in degree -1 are the contractions $\iota_x : CE(\mathfrak{g}) \to CE(\mathfrak{g})$ with $x \in \mathfrak{g}$;

* elements in degree 0  are the inner derivations $\mathcal{L}_x = [d_{CE(\mathfrak{g})}, \iota_x] : CE(\mathfrak{g}) \to CE(\mathfrak{g})$;

* the differential $\partial : \mathfrak{g} \to \mathfrak{g}$ is given by the commutator $\partial = [d_{CE(\mathfrak{g})}, -]$;

* the bracket is the graded commutator bracket of [[derivation]]s:

  * $[\iota_x, \iota_y] = 0$

  * $[\mathcal{L}_x, \iota_y] = \iota_{[x,y]}$

  * $[\mathcal{L}_x, \mathcal{L}_y] = \mathcal{L}_{[x,y]}$.

So this is the full subalgebra of the [[automorphism ∞-Lie algebra]] of $CE(\mathfrak{g})$ on the inner derivations.

See <a href="http://ncatlab.org/nlab/show/Weil+algebra#AsInnerDer">Weil algebra as CE-algebra of inner derivations</a> for more details.

## Properties

* The first formulation makes manifest that $inn(\mathfrak{g})$ is the structure that has historically been called [[Cartan calculus]].

* In the [[(∞,1)-category]] of [[∞-Lie algebra]]s $inn(\mathfrak{g})$ is equivalent to the point. See [[Weil algebra]] for details on this.

## References

The structure of $inn(\mathfrak{g})$ is of course in itself very simple and goes as such back at least to Cartan. 

Its role as a [[Lie 2-algebra]] in the context of [[∞-Chern-Weil theory]] has been discussed in section 6 of

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">ref</a>)
{#SSSI}
