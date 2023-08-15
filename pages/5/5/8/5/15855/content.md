
#Contents#
* table of contents
{:toc}


## Idea

According to [wikipedia](https://en.wikipedia.org/wiki/Affine_Grassmannian), 

> the affine Grassmannian of an algebraic group $G$ over a field $k$ is an [[ind-scheme]] which can be thought of as a flag variety for the loop group $G(k((t)))$

The affine Grassmannian is ind-representable. 
Affine Grassmannian of $SL_n$ admits embedding into [[Sato Grassmanian]]. 

## Definitions

### The $\GL_{n}$ case

\begin{definition}(Definition 1.1.1 of [#Zhu2016](#Zhu2016))
Let $k$ be a field and let $R$ be a $k$-algebra. An _$R$-family of lattices in $k((t))^{n}$_ is a finitely generated projective submodule $\Lambda$ of $R((t))^{n}$ such that $\Lambda \otimes_{R[[t]]}R((t))=R((t))^{n}$. 
\end{definition}

\begin{definition}(Definition 1.1.2 of [#Zhu2016](#Zhu2016))
The _affine Grassmannian $\Gr_{\GL_{n}}$ for $\GL_{n}$_ is the presheaf that assigns to every $k$-algebra $R$ the set of $R$-families of lattices in $k((t))^{n}$.
\end{definition}

### The general case

\begin{definition}(Section 1.2 of [#Zhu2016](#Zhu2016))
Let $k$ be a field and let $G$ be an affine $k$-group. If $R$ is a $k$-algebra, let $D_{R}=\Spec k[[t]]\widehat{\times}\Spec R$ and let $D^{*}_{R}=\Spec k((t))\widehat{\times} \Spec R$. Let $\mathcal{E}^{0}$ be the trivial $G$-torsor over $D_{R}$.

The _affine Grassmannian $\Gr_{G}$ of $G$_ is the presheaf that assigns to every $k$-algebra $R$ the set of pairs $(\mathcal{E},\beta)$, where $\mathcal{E}$ is a $G$-torsor on $D_{R}$ and $\beta:\mathcal{E}\vert_{D^{*}_{R}}\xrightarrow{\simeq}\mathcal{E}^{0}\vert_{D^{*}_{R}}$ is a trivialization.
\end{definition}

## Related

* [[geometric Langlands correspondence]], [[Ran space]]
* [[G-torsor]]
* [[Grassmannian]], [[flag variety]]

## References
* Evgeny Feigin, Michael Finkelberg, Markus Reineke, _Degenerate affine Grassmannians and loop quivers_, [http://arxiv.org/abs/1410.0777](http://arxiv.org/abs/1410.0777)

* {#Zhu2016} Xinwen Zhu, _An introduction to affine Grassmannians and the geometric Satake  equivalence_, [arXiv:1603.05593](http://arxiv.org/abs/1603.05593v2).

* [[Bhargav Bhatt]], [[Peter Scholze]], _Projectivity of the Witt vector affine Grassmannian_, Invent. math. 209, 329-423 (2017) [doi](https://doi.org/10.1007/s00222-016-0710-4) [arXiv:1507.06490](https://arxiv.org/abs/1507.06490)

* Alexander Schmitt, _Affine flag manifolds and principal bundles_, Trends in Mathematics, Springer 2010

category: algebra, algebraic geometry