

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

For a _[[commutative ring]]_ one defines a __radical $\sqrt{I}$ of an ideal__ $I\subset R$ as an ideal 
$$
\sqrt{I} = \{ r\in R \,|\, \exists n\in \mathbb{N}, r^n\in I \}
$$

An ideal is called a _radical ideal_ if it is equal to its own radical.
 
The [[nilradical|Nilradical]] of a commutative ring is the radical of the $0$ ideal.

For a [[noncommutative ring]] or an [[associative algebra]] there are many competing notions of a radical of a ring such as [[Jacobson radical]], Levitzky radical, and sometimes of radicals of ideals or, more often, of radicals of arbitrary modules of a ring. 

## Radical functors

Each of the notions of radical mentioned above are functorial, and some of the abstract properties of such functors are used in noncommutative localization theory, when defining so called *radical functors*. Classically these were considered for module categories ${ }_R Mod$ (left modules over a ring $R$, but there are generalizations for arbitrary [[Grothendieck categories]], and there are also some notions of radical for nonadditive categories.  See [Shulgeifer 60](#Shulgeifer60). 

We define here radical functors on ${ }_R Mod$, but warn that there are some terminological discrepancies across the literature. 

However they are defined, all notions of radical involve [[additive functor|additive]] [[subfunctors]] $i: \sigma \hookrightarrow 1_{ _R Mod}$ of the identity on ${ }_R Mod$, the additive category of left $R$-modules. [[natural transformation|Naturality]] of $i$ implies the equation $i \circ \sigma i = i \circ i\sigma$, whence $\sigma i = i\sigma$ by [[monomorphism|monicity]] of $i$. Some authors refer to these as *preradical functors* (e.g., [Mirhosseinkhani 2010](#Mirhosseinkhani2010)). 

Such a functor $\sigma: {}_R Mod\to {}_R Mod$ is __idempotent__ if $\sigma i = i\sigma: \sigma\sigma \to \sigma$ is an isomorphism, and is called a __radical functor__ if in addition $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$. Note however that some authors call *this* a *preradical functor*, and define a radical functor to be such a preradical functor that is left exact. 

Following [Goldman 1969](#Goldman1969), a left exact additive subfunctor of the identity is called an __idempotent kernel functor__. Observe that such is idempotent by the calculation

$$
\sigma \sigma M = \sigma Ker(M\to M/\sigma M) = Ker (\sigma M\to \sigma(M/\sigma M)) = Ker(\sigma M\to M\to M/\sigma M) = \sigma M
$$

where in the last step, we used that $\sigma$ is a subfunctor of the identity, hence the compositions $\sigma M\hookrightarrow M\to M/\sigma M$ and $\sigma M\to \sigma(M/\sigma M)\to M/\sigma M$ coincide. 

However, beware that other authors call a left exact additive subfunctor $\sigma: {}_R Mod\to {}_R Mod$ of the identity functor a [[kernel functor]], and then call a kernel functor $\sigma$ an *idempotent kernel functor* if $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$. In other words, their idempotent kernel functors coincide with what other authors call radical functors in the strong (left exact) sense above. 

See [Bueso-Jara-Verschoren 95](#BuesoJaraVerschoren95)


## Examples

Example ([Bueso-Jara-Verschoren 95 2.3.4](#BuesoJaraVerschoren95)): Let $I$ be a two-sided ideal in a ring. Define a functor $\sigma : {}_R Mod\to {}_R Mod$ on objects by $\sigma M = \{ m\in M\,|\, \exists n, I^n M = 0\}$; it is left exact and idempotent. If $I$ is finitely generated as left $R$-ideal (i.e. as a left $R$-submodule of $R$) then $I$ is a left exact radical functor. It is clear that the formula for $\sigma M$ reminds the definition of the radical of an ideal of a commutative ring.  

Nonexample: the subfunctor of identity which to any module $M$ assigns its [[socle]] is left exact but not a radical functor. 

## References


* {#Shulgeifer60} E. G. Shul&#697;ge&#301;fer (&#1045;. &#1043;. &#1064;&#1091;&#1083;&#1100;&#1075;&#1077;&#1081;&#1092;&#1077;&#1088;), _&#1050; &#1086;&#1073;&#1097;&#1077;&#1081; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1088;&#1072;&#1076;&#1080;&#1082;&#1072;&#1083;&#1086;&#1074; &#1074; &#1082;&#1072;&#1090;&#1077;&#1075;&#1086;&#1088;&#1080;&#1103;&#1093;_, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1089;&#1073;., 51(93):4 (1960), 487&#8211;500 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=sm&paperid=4826&what=fullt&option_lang=rus) 

* {#BuesoJaraVerschoren95} J. L. Bueso, P. Jara, A. Verschoren, _Compatibility, stability, and sheaves_, Monographs and Textbooks in Pure and Applied Mathematics, 185. Marcel Dekker, Inc., New York, 1995. xiv+265 pp. 

* {#Goldman1969} O. Goldman, _Rings and modules of quotients_, J. Algebra 13 (1969), 10-47.

See also

* Wikipedia, _[Radical of a ring](https://en.wikipedia.org/wiki/Radical_of_a_ring)_

[[!redirects radicals]]
[[!redirects radical functor]]


[[!redirects radical ideal]]
[[!redirects radical ideals]]

