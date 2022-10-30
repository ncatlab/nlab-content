
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


# Vector bundles
* table of contents
{: toc}


## Idea ##

A **vector bundle** is a [[vector space]] which "continuously varies" over a [[topological space]] $X$.


## Definition ## 

A **vector bundle** over a space $X$ is a [[bundle]] over $X$ which is locally isomorphic to a product with a [[vector space]] $V$ as fiber.  More precisely, the data is an object $\pi: E \to X$ in $Top/X$ equipped with a vector space structure [[internalization|internal]] to $Top/X$, consisting of maps 

$$+: E \times_X E \to E \qquad \cdot: \mathbb{R} \times E \to E$$ 

(where $E \times_X E$ denotes the [[fiber product]] or pullback of $\pi$ along itself) satisfying vector space axioms. This vector space object must satisfy the _local triviality condition_: there exists an open [[cover]] 

$$U = \sum_{\alpha \in A} U_\alpha \rightrightarrows X$$ 

and an isomorphism from the [[pullback]] $U \times_X E$ to the projection $\pi: U \times V \to U$, 

$$\array{
U \times V & \overset{\phi}{\leftarrow} & U \times_X E & \to & E\\
 & & \downarrow & & \downarrow \pi \\
 & & U \rightrightarrows X
}$$
 
as vector space objects in $Top/X$. The projection $U \times V \to U$ itself is called a **trivial (vector) bundle** over $U$. 

Equivalently, each fiber $E_x$ carries a vector space structure, and there exists an open covering $\{U_\alpha\}_{\alpha \in A}$ of $X$ together with **local trivializations**: bundle isomorphisms $\phi_{\alpha}$ from a trivial bundle $U_{\alpha} \times V$ to the pullback of $\pi$ along $U_\alpha \hookrightarrow X$: 

$$\array{
\pi^{-1}(U_\alpha) & \overset{\phi_\alpha}{\to} & U_\alpha \times V\\
\pi|_{U_\alpha} \searrow & & \swarrow proj\\
& U_\alpha &
}$$ 

such that $\phi_{\alpha}$ induces a linear map $V \to E_x$ between the fibers.  

In terms of the local trivialization data, there are **transition functions** 

$$(U_\alpha \cap U_\beta) \times V \overset{\phi_\beta \circ \phi_{\alpha}^{-1}}{\to} (U_\alpha \cap U_\beta) \times V: (x, v) \mapsto (x, g_{\alpha\beta}(x)(v)),$$ 

where the $g_{\alpha\beta}(x)$ are linear [[automorphisms]] of $V$ and satisfy the &#268;ech 1-cocycle conditions:

$$g_{\beta\gamma} \circ g_{\alpha\beta} = g_{\alpha\gamma} \qquad g_{\alpha\alpha} = id$$ 

In the converse direction, given such a collection $g_{\alpha\beta}: U_{\alpha} \cap U_\beta \to GL(V)$ satisfying the 1-cocycle conditions, there is a vector bundle obtained by pasting local trivial bundles together along the $g_{\alpha\beta}$, namely the coequalizer of a pair 

$$i, \mu: \sum_{\alpha, \beta} (U_\alpha \cap U_\beta) \times V \overset{\to}{\to} \sum_{\alpha} U_\alpha \times V$$ 

in the category of vector space objects in $Top/X$. Here the restriction of $i$ to the coproduct summands is induced by inclusion: 

$$(U_\alpha \cap U_\beta) \times V \hookrightarrow U_\alpha \times V \hookrightarrow \sum_\alpha U_\alpha \times V$$ 

and the restriction of $\mu$ to the coproduct summands is 
via the action of the transition functions: 

$$(U_\alpha \cap U_\beta) \times V \overset{(\langle incl, g_{\alpha\beta} \rangle) \times V}{\to} U_\beta \times GL(V) \times V \overset{action}{\to} U_\beta \times V \hookrightarrow \sum_{\beta} U_\beta \times V$$


## Remarks ##

* In most applications, the [[ground field]] of scalars is assumed to be $\mathbb{R}$ or $\mathbb{C}$, although sometimes other fields are allowed, as in the study of algebraic vector bundles. 

* In most cases (as in [[K-theory]]), it is implicitly assumed that the vector space $V$ is finite-dimensional. 

* In the context of differential topology or differential geometry, one also assumes that $\pi$ is smooth and that the local bundle isomorphisms $\phi_{\alpha}$ are diffeomorphisms.


## Sheaf-theoretic version ##

Vector bundles can also be defined via [[sheaf and topos theory|sheaf theory]], which permits easy transport to general [[Grothendieck topos]]es. Let $Sh(X)$ be the category of (set-valued) [[sheaf|sheaves]] on $X$. The sheaf of continuous local sections of the product projection 

$$X \times \mathbb{R} \to X$$ 

forms a [[local ring]] object $R$; when interpreted in the [[internal logic]] of $Sh(X)$, it is the Dedekind [[real number]] object. Then, according to a theorem of Richard Swan, in its sheaf-theoretic incarnation a vector bundle is the same thing as a projective $R$-module. 

* A theorem of Kaplansky states "every projective module over a local ring is free". When interpreted in [[sheaf semantics]] ([[Kripke-Joyal semantics]]), the [[existential quantifier]] implicit in "free" is interpreted _locally_, so we can consider a vector bundle as a locally free module over the Dedekind reals. 


## Virtual vector bundles

In one class of models for [[K-theory]] -- [[generalized (Eilenberg-Steenrod) cohomology]] theory -- cocycles are represented by $\mathbb{Z}_2$-graded vector bundles (pairs of vector bundles, essentially) modulo a certain equivalence relation. In that context it is sometimes useful to consider a certain variant of infinite-dimensional $\mathbb{Z}_2$-graded vector bundles called [[vectorial bundle]]s.


Much else to be discussed...


## Related concepts

* [[principal bundle]], [[associated bundle]]

* **vector bundle**

* [[(∞,1)-vector bundle]] / [[(∞,n)-vector bundle]]

## Literature

* Glenys Luke, Alexander S. Mishchenko, _Vector bundles and their applications_, Math. and its Appl. __447__, Kluwer 1998. viii+254 pp. [MR99m:55019](http://www.ams.org/mathscinet-getitem?mr=99m:55019)

* &#1040;. &#1057;. &#1052;&#1080;&#1097;&#1077;&#1085;&#1082;&#1086;, _&#1042;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1077; &#1088;&#1072;&#1089;&#1089;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103; &#1080; &#1080;&#1093; &#1087;&#1088;&#1080;&#1084;&#1077;&#1085;&#1077;&#1085;&#1080;&#1103;_ (Russian;  A. S. Mishchenko, Vector bundles and their applications) Nauka, Moscow, 1984. 208 pp.

* [[Max Karoubi]], _K-theory. An introduction_, Grundlehren der Mathematischen Wissenschaften __226__, Springer 1978. xviii+308 pp.

* [[Raoul Bott]], Loring W. Tu, _Differential forms in algebraic topology_, Graduate Texts in Mathematics __82__, Springer 1982. xiv+331 pp.

* Allen Hatcher, _Vector bundles and K-Theory_, (partly finished book) [web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html)

* Howard Osborn, _Vector bundles. Vol. 1. Foundations and Stiefel-Whitney classes_, Pure and Appl. Math. __101__, Academic Press 1982. xii+371 pp. [MR85e:55001](http://www.ams.org/mathscinet-getitem?mr=85e:55001)

* Dale Husemoller, _Fibre bundles_, McGraw-Hill 1966 (300 p.); Springer GTM 1975 (327 p.), 1994 (353 p.). 

[[!redirects vector bundles]]