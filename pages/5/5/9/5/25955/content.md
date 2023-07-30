#Contents#
* table of contents
{:toc}

## Idea

The $p$-adic local Langlands correspondence is a version of the [[local Langlands correspondence]] where the representations are over a $p$-adic field, i.e. on one side we have certain $E$-representations of $G(F)$ (for $G$ some reductive group), and on the other we have certain $E$-representations of $\mathrm{Gal}(\overline{F}/F)$, where $E$ and $F$ are both finite extensions of $\mathbb{Q}_{p}$. It should be compatible with the [[mod p local Langlands correspondence]]. The only case that is known is when $G=\mathrm{GL}_{2}$ and $F=\mathbb{Q}_{p}$.

An approach to realizing one direction of the p-adic local Langlands correspondence using patching was developed in [#CEGGPS2013](#CEG+2013). An approach going in the other direction was developed in [#Scholze2015](#Scholze2015). These two constructions are compatible with each other. Scholze's approach was further developed in [#HansenMann2022](#HansenMann2022).

## Scholze's p-adic Jacquet-Langlands functor

We describe the construction in [#Scholze2015](#Scholze2015). Let $F$ be a finite extension of $\mathbb{Q}_{p}$ and let $C=\widehat{\overline{F}}$. Let $\mathcal{M}_{\infty}$ be the infinite level [[Lubin-Tate space]] over $C$. It is a perfectoid space equipped with commuting actions of $\GL_{n}(F)$ and $D^{\times}$, where $D/F$ is the central simple algebra of invariant $1/n$. There is a Gross-Hopkins period map $\pi_{\mathrm{GH}}:\mathcal{M}_{\infty}\to\mathbb{P}_{C}^{n-1}$.

Let $\pi$ be a smooth $\mathbb{F}_{p}$-representation of $\GL_{n}(F)$. We define a sheaf $\mathcal{F}_{\pi}$ on $\mathbb{P}_{C}^{n-1}$ as follows. Given an etale map $U\to\mathbb{P}_{C}^{n-1}$, define

$$\mathcal{F}_{\pi}=\mathrm{Map}_{\mathrm{cont},\GL_{n}(F)\times D^{\times}}(\vert U\times_{\mathbb{P}_{C}^{n-1}} \mathcal{M}_{\infty}\vert,\pi).$$

Scholze's p-adic Jacquet-Langlands functor $\mathcal{J}^{i}$ is now given by the $i$-th etale cohomology of the sheaf $\mathcal{F}_{\pi}$:

$$\mathcal{J}^{i}(\pi)=H^{i}(\mathbb{P}_{C}^{n-1},\mathcal{F}_{\pi})$$

The representations $\mathcal{J}^{i}(\pi)$ are smooth $\mathbb{F}_{p}$-representations of $D^{\times}$ and also carry an action of the Weil group $W_{F}$.

## References

* {#Breuil2010} [[Christophe Breuil]], *The emerging p-adic Langlands program*, Proceedings of the International Congress of Mathematicians, Hyderabad, India, 2010 ([pdf](https://www.imo.universite-paris-saclay.fr/~breuil/PUBLICATIONS/ICM2010.pdf))

* {#CEGGPS2013} Ana Caraiani, [[Matthew Emerton]], [[Toby Gee]], David Geraghty, Vytautas Paskunas, Sug Woo Shin, *Patching and the p-adic local Langlands correspondence* ([arXiv:1310.0831](https://arxiv.org/abs/1310.0831))

* {#Scholze2015} [[Peter Scholze]], *On the p-adic cohomology of the Lubin-Tate tower* ([arXiv:1506.04022](https://arxiv.org/abs/1506.04022))

* {#HansenMann2022} David Hansen, [[Lucas Mann]], *$p$-adic sheaves on classifying stacks, and the $p$-adic Jacquet-Langlands correspondence* ([arXiv:2207.04073](https://arxiv.org/abs/2207.04073))
