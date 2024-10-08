

#Contents#
* table of contents
{:toc}

## Idea

[[Pierre Gabriel]] introduced a number of constructions in localization theory, mostly in [[abelian category|abelian]] context in his thesis published as

* [[Pierre Gabriel]], [[Des Categories Abeliennes]]

and in general context in his [[Gabriel-Zisman|book]] with Zisman. By __Gabriel localization__ one usually means a specific class of localizations of rings and the corresponding localization of categories of modules over rings. 

Given a (possibly noncommutative and nonunital) ring $R$ and a [[Gabriel filter]] $\mathcal{F}$ of left ideals in $R$, a Gabriel localization endofunctor 

$$
G_{\mathcal{F}} : {}_R Mod\to {}_R Mod
$$

is defined in one of the number of equivalent ways.

For example, for any [[uniform filter]] $\mathcal{F}$ of left ideals in $R$ one defines a subfunctor of the identity functor $\sigma_{\mathcal{F}}$ on the category of left $R$-modules  

$$
M\mapsto \sigma_{\mathcal{F}}(M) = \{m\in M \,|\, \exists J\in \mathcal{F},\, J m = 0\}\subset M
$$

In a later work of Goldman $\sigma_{\mathcal{L}}$ was called a radical functor. If $\mathcal{F}$ is not only uniform but in fact a [[Gabriel filter]] then the radical $\sigma_{\mathcal{F}}$ is idempotent, i.e. $\sigma_{\mathcal{F}}^2 = \sigma_{\mathcal{F}}$. If $R$ is unital, $\sigma_{\mathcal{F}}$ is equivalent to the functor given on objects by 

$$
\sigma'_{\mathcal{F}}(M) = colim_{J\in\mathcal{F}} Hom_R(R/J,M)
$$

For each uniform fiter $\mathcal{F}$ one also defines the endofunctor $H_{\mathcal{F}}$
on ${}_R Mod$ by 

$$
H_{\mathcal{F}}(M) = colim_{J\in\mathcal{F}} Hom_R(J,M)
$$ 

(the colimit is over downward directed family of left ideals in $\mathcal{F}$ and is a colimit of a functor with values in the category of abelian groups; the uniformness condition however gurantees that there is a canonical structure of an $R$-module on the colimit group $H_{\mathcal{F}}(M)$).

Finally, for the Gabriel filter $\mathcal{F}$ one defines the Gabriel (endo)functor $G_{\mathcal{F}}$ on objects by

$$
G_{\mathcal{F}}(M) := H_{\mathcal{F}}(M/\sigma_{\mathcal{F}}(M))
= colim_{J\in\mathcal{L}}Hom_R(J,M/\sigma_{\mathcal{F}}(M))
$$

The essential image of the functor $G_{\mathcal{F}}$ is the localized category. The left $R$-module $G_{\mathcal{F}}(R)$ has a canonical structure of a ring over $R$; there is a natural forgetful functor from the localized category to the category of left $G_{\mathcal{F}}(R)$-modules. Under strong assumptions on the filter this functor is in fact an equivalence of categories, e.g. when the localization is [[Ore localization|Ore]].  

## Related entries

* _[[Calculus of fractions and homotopy theory]]_

## References

* [[Pierre Gabriel]], *[[Des Categories Abeliennes]]*, Bulletin de la Société Mathématique de France **90** (1962) 323-448 &lbrack;[numdam:BSMF_1962__90__323_0](http://www.numdam.org/item?id=BSMF_1962__90__323_0)&rbrack;

* [[Pierre Gabriel]], *La localisation dans les anneaux non commutatifs*, Séminaire Dubreil (1959-1960) exposé 2, 1-35 &lbrack;[numdam:SD_1959-1960__13_1_A2_0](http://www.numdam.org/item/?id=SD_1959-1960__13_1_A2_0), [pdf](http://www.numdam.org/item/SD_1959-1960__13_1_A2_0.pdf)&rbrack;

* [[Alexander L. Rosenberg]], _Non-commutative affine semischemes and schemes_, Seminar on supermanifolds __26__, Dept. Math., U. Stockholm (1988) [pdf](https://www2.irb.hr/users/zskoda/rosenStock1988.pdf)

* [[Zoran Škoda]], _Localizations for construction of quantum coset spaces_, in "Noncommutative geometry and Quantum groups", W.Pusz,  P.M. Hajac, eds. Banach Center Publications vol.61, pp. 265--298, Warszawa 2003, [math.QA/0301090](http://arxiv.org/abs/math.QA/0301090).

* [[Zoran Škoda]], _Noncommutative localization in noncommutative geometry_, London Math. Society Lecture Note Series __330__, ed. [[A. Ranicki]]; pp. 220&#8211;313, [math.QA/0403276](http://arxiv.org/abs/math.QA/0403276)

[[!redirects Gabriel localizations]]
