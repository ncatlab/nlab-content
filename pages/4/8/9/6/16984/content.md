
#Contents#
* table of contents
{:toc}


## Idea

Let $C$ be an algebraically closed [[perfectoid field]] over $\mathbb{F}_{p}$. The *Fargues-Fontaine curve* $X_{C}$ is a [[complete variety|complete]] [[algebraic curve]] whose [[closed points]] parametrize the untilts of $C$. Such an untilt may be recovered as the [[residue field]] of the corresponding point.

## As an adic space

Let $E$ be a finite extension of $\mathbb{Q}_{p}$ with uniformizer $\pi$ and residue field $\kappa$. Let $S=Spa(R,R^{+})$ be a [[perfectoid space]] over $\overline{\mathbb{F}}_{q}$ with pseudouniformizer $\varpi$. We take ramified [[Witt vectors]] $W_{\mathcal{O}_{E}}(R):=W(R^{+}\otimes_{W(\kappa)}\mathcal{O}_{E})$. We define $Y_{S}$ to be the locus in $Spa(W_{\mathcal{O}_{E}}(R))$ where $\pi$ and $\varpi$ are invertible. We think of $Y_{S}$ as the "fiber product" $Spa(R^{+})\times Spa(\mathcal{O}_{E})$, even though is is not literally possible because we lack a base for the fiber product (we will define this later)!

The (relative) Fargues-Fontaine curve $X_{S}$ is then defined to be $Y_{S}/\phi_{S}^{\mathbb{Z}}$, where $\phi_{S}$ is the Frobenius on $S$.

## In the geometrization of the local Langlands correspondence

The Fargues-Fontaine curve finds application in the geometrization of the [[local Langlands correspondence]]. Note that the [[geometric Langlands correspondence]] is stated for a curve. Naively, one might think that the "curve" for the local Langlands correspondence should be $Spec(E)$, for $E$ a local field. However, the local Langlands correspondence concerns the Weil group instead of the absolute Galois group, one should instead consider $Spec(\breve{E})/\phi_{E}^{\mathbb{Z}}$, where $\breve{E}$ is the maximal unramified extension of $E$ and $\phi_{E}$ is the Frobenius.

To truly obtain a geometrization, however, one needs to "relativize" this, which is analogous to considering the stack $Bun_{G}$ in the geometric Langlands correspondence instead of just its points $Bun_{G}(\mathbb{F}_{q})$. Hence we must be able to take "base change".

If $E$ is, say $\mathbb{F}_{q}((t))$, then for a perfectoid space $S=Spa(R,R^{+})$ with pseudouniformizer $\varpi$ we may take the fiber product $S\times_{Spa(\mathbb{F}_{q})} Spa(\mathbb{F}_{q}((t)))$. However if $E$ is a finite extension of $\mathbb{Q}_{p}$, there is no analogue of the base $\mathbb{F}_{q}$ over which we take the fiber product.

However, we note that in the case where $E=\mathbb{F}_{q}((t))$, the fiber product $S\times_{Spa(\mathbb{F}_{q})} Spa(\mathbb{F}_{q}((t)))$ is the locus inside $Spa(R^{+})\times_{Spa(\mathbb{F}_{q})} Spa(\mathbb{F}_{q}[[t]])$ where both the uniformizer $\varpi$ of $R$ and the uniformizer $t$ of $\mathbb{F}_{q}$ are both invertible.

Now noting that the mixed characteristic analogue of forming power series is taking Witt vectors (compare, for instance, $\mathbb{F}_{p}[[t]]$ and $W(\mathbb{F}_{p})=\mathbb{Z}_{p}$), we think of the locus $Y_{S}$ defined above as the analogue of our fiber product, $Spa(R^{+})\times Spa(\mathcal{O}_{E})$. Again, since the local Langlands correspondence is phrased in terms of the Weil group, we have to take the quotient by the action Frobenius, and take $X_{S}=Y_{S}/\phi^{\mathbb{Z}}$, which is the Fargues-Fontaine curve.

## As a scheme

If $S=Spa(C)$ where $C$ be an algebraically closed perfectoid field over $\mathbb{F}_{p}$, we have a description of the Fargues-Fontaine curve as a scheme. Let $\mathcal{O}_{C}$ be the [[ring of integers]] of $C$, and let $W(\mathcal{O}_{C})$ be the [[Witt vectors]] of $\mathcal{O}_{C}$. Let $\phi_{C}:C\to C$ be the Frobenius morphism. We define a [[norm]] $\vert\cdot\vert_{r}$ on $W(\mathcal{O}_{C})[1/p]$ as follows:

$$\vert \sum_{n\gg -\infty} [a_{n}]p^{n}\vert_{r}=\sup_{n}\vert a_{n}\vert p^{-r n}$$

Let $B_{C}$ be the Frechet completion of $W(\mathcal{O}_{C})[1/p]$ with respect to all the norms $\vert\cdot\vert_{r}$ for every positive $r$.

Then the schematic Fargues-Fontaine curve $X_{C}^{sch}$ is defined to be
$$X_{C}^{sch}=\mathrm{Proj}(\oplus_{n\in\mathbb{N}} B_{C}^{\phi=p^{n}}).$$

## Vector Bundles on the Fargues-Fontaine Curve

[[Vector bundles]] on the Fargues-Fontaine curve admit a classification in terms of _isocrystals_ (vector spaces over the field $E$ together with a semilinear action of Frobenius). More generally for a reductive group $G$, there is a concept of $G$-isocrystals which correspond to $G$-bundles on the Fargues-Fontaine curve.

These also in turn correspond to extended pure inner forms of $G$ (which are all the inner forms if $G$ is connected). It is believed that it should not just be $G$, but all the extended pure inner forms of $G$ together, which  should appear in the geometric side of the [[local Langlands correspondence]] (for instance inner forms have the same [[Langlands dual group]]). This is another motivation for the appearance of the Fargues-Fontaine curve in the Fargues-Scholze geometrization of the local Langlands correspondence.

## Related concepts

* [[p-adic Hodge theory]]

* [[local Langlands correspondence]]

## References

* [[Jared Weinstein]], _[The Fundamental Curve of p-adic Hodge Theory, or How to Un-tilt a Tilted Field](https://galoisrepresentations.wordpress.com/2013/07/23/the-fundamental-curve-of-p-adic-hodge-theory-or-how-to-un-tilt-a-tilted-field/)_

* [[Jared Weinstein]], _[The Fundamental Curve of p-adic Hodge Theory, Part II](https://galoisrepresentations.wordpress.com/2013/08/12/the-fundamental-curve-of-p-adic-hodge-theory-part-ii/)_

* [[Dennis Gaitsgory]], [[Jacob Lurie]], _Harvard Seminar on Fargues-Fontaine Curve_ ([Informal Notes](http://www.math.harvard.edu/~lurie/FF.html))

* {#FarguesScholze21} [[Laurent Fargues]], [[Peter Scholze]], _Geometrization of the local Langlands correspondence_ ([arXiv:2102.13459](https://arxiv.org/abs/2102.13459))

* a version in global analytic geometry is mentioned at the end of [http://www-personal.umich.edu/~snkitche/Conference/notes/Kremnitzer-2.pdf](http://www-personal.umich.edu/~snkitche/Conference/notes/Kremnitzer-2.pdf) + [audio](http://leccap.engin.umich.edu/leccap/site/s79yndxt7qowoek7n3m)

* [[Federico Bambozzi]], [[Oren Ben-Bassat]], [[Kobi Kremnizer]], _Analytic geometry over $\mathbb{F}_1$ and the Fargues-Fontaine curve_, ([arXiv:1711.04885](https://arxiv.org/abs/1711.04885))