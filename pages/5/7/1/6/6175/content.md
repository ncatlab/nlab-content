For a _commutative_ ring one defines a __radical $\sqrt{I}$ of an ideal__ $I\subset R$ as an ideal 
$$
\sqrt{I} = \{ r\in R \,|\, \exists n\in \mathbb{N}, r^n\in I \}
$$
[[nilradical|Nilradical]] of a commutative ring is the radical of the $0$ ideal.

For a noncommutative ring or an associative algebra there are many competing notions of a radical of a _ring_ like Jacobson radical, Levitzky radical; and sometimes of radicals of ideals or, more often arbitrary modules of a ring. 

Some of the abstract properties of such functors are used in noncommutative localization theory, when defining so called __radical functors__. The latter are generalized for arbitrary Grothendieck categories. Finally there are some notions of radicals in nonadditive categories. 

* E. G. Shul&#697;ge&#301;fer (&#1045;. &#1043;. &#1064;&#1091;&#1083;&#1100;&#1075;&#1077;&#1081;&#1092;&#1077;&#1088;), _&#1050; &#1086;&#1073;&#1097;&#1077;&#1081; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1088;&#1072;&#1076;&#1080;&#1082;&#1072;&#1083;&#1086;&#1074; &#1074; &#1082;&#1072;&#1090;&#1077;&#1075;&#1086;&#1088;&#1080;&#1103;&#1093;_, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1089;&#1073;., 51(93):4 (1960), 487&#8211;500 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=sm&paperid=4826&what=fullt&option_lang=rus) 

A functor $\sigma: {}_R Mod\to {}_R Mod$ is __idempotent__ if $\sigma\sigma = \sigma$ and a _(pre)radical functor_ if it is an additive [[subfunctor]] of the identity functor and $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$
(preradical versus radical depends on an author, whether the left exactness is included or not in the definition of a radical functor). According to Goldman 1969, a left exact preradical is called an __idempotent kernel functor__. It is idempotent by the calculation

$$
\sigma \sigma M = \sigma Ker(M\to M/\sigma M) = Ker (\sigma M\to \sigma(M/\sigma M)) = Ker(\sigma M\to M/\sigma M) = \sigma M
$$

In the last step, we used that $\sigma$ is a subfunctor of the identity, hence the compositions $\sigma M\hookrightarrow M\to M/\sigma M$ and $\sigma M\to \sigma(M/\sigma M)\to M/\sigma M$ coincide. 
In an alternative terminology, an idempotent kernel functor is any [[kernel functor]] (= left exact additive subfunctor of the identity functor) $\sigma: {}_R Mod\to {}_R Mod$ such that $\sigma(M/\sigma(M))=0$ for all $M$ in ${}_R Mod$. 

* J. L. Bueso, P. Jara, A. Verschoren, _Compatibility, stability, and sheaves_, Monographs and Textbooks in Pure and Applied Mathematics, 185. Marcel Dekker, Inc., New York, 1995. xiv+265 pp. 

Example (Bueso et al. 2.3.4): Let $I$ be a two-sided ideal in a ring and $M$ a left $R$-module. Define the functor $\sigma : {}_R Mod\to {}_R Mod$ on objects by $\sigma M = \{ m\in M\,|\, \exist n, I^n M = 0\}$; it is left exact and idempotent. If $I$ is finitely generated as left $R$-ideal (i.e. as a left $R$-submodule of $R$) then $I$ is a left exact radical functor. It is clear that the formula for $\sigma M$ reminds the definition of the radical of an ideal of a commutative ring.  

Nonexample: the subfunctor of identity which to any module $M$ assigns its [[socle]] is left exact but not a radical functor. 

[[!redirects radicals]]
[[!redirects radical functor]]