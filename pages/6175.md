

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


## Defintion

For a _[[commutative ring]]_ one defines a __radical $\sqrt{I}$ of an ideal__ $I\subset R$ as an ideal 
$$
\sqrt{I} = \{ r\in R \,|\, \exists n\in \mathbb{N}, r^n\in I \}
$$

An ideal is called a _radical ideal_ if it is equal to its own radical.
 
The [[nilradical|Nilradical]] of a commutative ring is the radical of the $0$ ideal.

For a [[noncommutative ring]] or an [[associative algebra]] there are many competing notions of a radical of a ring such as [[Jacobson radical]], Levitzky radical, and sometimes of radicals of ideals or, more often, arbitrary modules of a ring. 

## Properties

Some of the abstract properties of such functors are used in noncommutative localization theory, when defining so called __radical functors__. The latter are generalized for arbitrary [[Grothendieck categories]]. Finally there are some notions of radicals in nonadditive categories.  See [Shulgeifer 60](#Shulgeifer60) 

Notions of radical involve [[additive functor|additive]] [[subfunctors]] $i: \sigma \hookrightarrow 1_{ _R Mod}$ of the identity on ${ }_R Mod$, the additive category of left $R$-modules. [[natural transformation|Naturality]] of $i$ implies the equation $i \circ \sigma i = i \circ i\sigma$, whence $\sigma i = i\sigma$ by [[monomorphism|monicity]] of $i$. 

Such a functor $\sigma: {}_R Mod\to {}_R Mod$ is __idempotent__ if $\sigma i = i\sigma: \sigma \to \sigma\sigma$ is an isomorphism, and is called a _(pre)radical functor_ if $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$
(preradical versus radical depends on an author, whether the left exactness is included or not in the definition of a radical functor). According to Goldman 1969, a left exact preradical is called an __idempotent kernel functor__. It is idempotent by the calculation

$$
\sigma \sigma M = \sigma Ker(M\to M/\sigma M) = Ker (\sigma M\to \sigma(M/\sigma M)) = Ker(\sigma M\to M\to M/\sigma M) = \sigma M
$$

In the last step, we used that $\sigma$ is a subfunctor of the identity, hence the compositions $\sigma M\hookrightarrow M\to M/\sigma M$ and $\sigma M\to \sigma(M/\sigma M)\to M/\sigma M$ coincide. 
In an alternative terminology, an idempotent kernel functor is any [[kernel functor]] (= left exact additive subfunctor of the identity functor) $\sigma: {}_R Mod\to {}_R Mod$ such that $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$. 

See [Bueso-Jara-Verschoren 95](#BuesoJaraVerschoren95)


## Examples

Example ([Bueso-Jara-Verschoren 95 2.3.4](#BuesoJaraVerschoren95)): Let $I$ be a two-sided ideal in a ring. Define a functor $\sigma : {}_R Mod\to {}_R Mod$ on objects by $\sigma M = \{ m\in M\,|\, \exists n, I^n M = 0\}$; it is left exact and idempotent. If $I$ is finitely generated as left $R$-ideal (i.e. as a left $R$-submodule of $R$) then $I$ is a left exact radical functor. It is clear that the formula for $\sigma M$ reminds the definition of the radical of an ideal of a commutative ring.  

Nonexample: the subfunctor of identity which to any module $M$ assigns its [[socle]] is left exact but not a radical functor. 

## References


* {#Shulgeifer60} E. G. Shul&#697;ge&#301;fer (&#1045;. &#1043;. &#1064;&#1091;&#1083;&#1100;&#1075;&#1077;&#1081;&#1092;&#1077;&#1088;), _&#1050; &#1086;&#1073;&#1097;&#1077;&#1081; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1088;&#1072;&#1076;&#1080;&#1082;&#1072;&#1083;&#1086;&#1074; &#1074; &#1082;&#1072;&#1090;&#1077;&#1075;&#1086;&#1088;&#1080;&#1103;&#1093;_, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1089;&#1073;., 51(93):4 (1960), 487&#8211;500 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=sm&paperid=4826&what=fullt&option_lang=rus) 

* {#BuesoJaraVerschoren95} J. L. Bueso, P. Jara, A. Verschoren, _Compatibility, stability, and sheaves_, Monographs and Textbooks in Pure and Applied Mathematics, 185. Marcel Dekker, Inc., New York, 1995. xiv+265 pp. 

See also

* Wikipedia, _[Radical of a ring](https://en.wikipedia.org/wiki/Radical_of_a_ring)_

[[!redirects radicals]]
[[!redirects radical functor]]


[[!redirects radical ideal]]
[[!redirects radical ideals]]

