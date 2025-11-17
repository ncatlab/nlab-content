
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--


* tic
{: toc}

## Idea

An _$Ab$-enriched category_  (or, if small, _ringoid_) is a [[category enriched]] over the [[monoidal category]] [[Ab]] of [[abelian groups]] with its usual [[tensor product]].

Sometimes they are called [[pre-additive category|pre-additive categories]], but sometimes that term also implies the existence of a [[zero object]].


## Definition

Explicitly, an __$Ab$-enriched category__ is a [[category]] $C$ such that
for all objects $a,b$ the [[hom-set]] $Hom_C(a,b)$
is equipped with the structure of an [[abelian group]]; and
such that for all triples $a,b,c$ of objects the
[[composition]] operation 
$
  \circ_{a,b,c} : Hom_C(a,b) \times Hom_C(b,c) \to Hom_C(a,c)
$
is bilinear. A __ringoid__ is a small $Ab$-enriched category.


## Remarks

*  $Ab$-enriched categories are called ringoids since the concept is a [[horizontal categorification]] (or 'oidification') of the concept of a [[ring]].

*  There is a canonical forgetful functor $Ab \to Set_*$ from
abelian groups to [[pointed set]]s, which sends each group to its underlying set with point being the neutral element. Using this functor, every $Ab$-enriched category $C$ is in particular also a category that is enriched over pointed sets (that is, a category with [[zero morphisms]]). This is sufficient for there to be a notion of [[kernel]] and [[cokernel]] in $C$.

*  In general, [[abelian category|abelian categories]] are the most important examples of $Ab$-enriched categories.  See [[additive and abelian categories]].


## Finite products are absolute

One of the remarkable facts about $Ab$-enriched categories is that finite [[products]] (and [[coproducts]]) are [[absolute limit|absolute limits]].  This implies that finite products coincide with finite coproducts, and are preserved by _any_ $Ab$-enriched functor.


### Zero objects

In an $Ab$-enriched category $C$, any [[initial object]] is also a [[terminal object]], hence a [[zero object]], and dually.  An object $a\in C$ is a zero object just when its identity $1_a$ is equal to the zero morphism $0:a\to a$ (that is, the identity element of the abelian group $\hom_C(a,a)$).  Expressed in this way, it is easy to see that any $Ab$-enriched functor preserves zero objects.


### Biproducts

For $c_1, c_2 \in C$ two objects in an $Ab$-enriched category $C$,  [[generalized the|the]] [[product]] $c_1 \times c_2$ coincides  with [[generalized the|the]] [[coproduct]] $c_1 \sqcup c_2$ when either exists. 

For example, if $c_1 \times c_2$ exists, with [[projection]] maps $p_i\colon c_1 \times c_2 \to c_i$, then according to the [[universal property]] of products, there are unique maps 
$$
  q_i\colon c_i \to c_1 \times c_2
$$
such that $p_i q_i = 1_{c_i}$ and $p_j q_i = 0$ for $j \neq i$, and these maps $q_i$ are the coproduct [[coprojections]], i.e., they realize $c_1 \times c_2$ as the coproduct of $c_1$ and $c_2$. Indeed, for any maps $r_1\colon c_1 \to e$ and $r_2\colon c_2 \to e$, it is easily checked that 

$$r = r_1 p_1 + r_2 p_2\colon c_1 \times c_2 \to e$$ 

satisfies $r q_1 = r_1$ and $r q_2 = r_2$, and is the unique map satisfying these equations. The full argument is spelled out at *[[additive category]]*. 

By a [[formal duality|dual]] argument, if the coproduct $c_1 \sqcup c_2$ exists, then it may also be realized as the product of $c_1$ and $c_2$. Either way, the product or coproduct is called a *[[biproduct]]* or (sometimes) a *[[direct sum]]* and is generally denoted
$$
  c_1 \oplus c_2.
$$
It can be characterized diagrammatically as an object $c_1\oplus c_2$ equipped with morphisms $q_i \colon c_i\to c_1\oplus c_2$ and $p_i \colon c_1\oplus c_2 \to c_i$ such that $p_i q_j = \delta_{i j}$ and $q_1 p_1 + q_2 p_2 = 1_{c_1\oplus c_2}$.  Expressed in this form, it is clear that any $Ab$-[[enriched functor]] [[preserved limit|preserves]] biproducts.


## As a generalisation of rings

When using the term 'ringoid', one often assumes a ringoid to be [[small category|small]].

Ringoids share many of the properties of (noncommutative) [[rings]].  For instance, we can talk about (left and right) [[modules]] over a ringoid $R$, which can be defined as $Ab$-enriched [[functors]] $R\to Ab$ and $R^{op}\to Ab$.  [[bimodule|Bimodules]] over ringoids have a tensor product (the enriched [[tensor product of functors]]) under which they form a [[bicategory]], also known as the bicategory $Ab Prof$ of $Ab$-enriched [[profunctors]].  Modules over a ringoid also form an [[abelian category]] and thus have a [[derived category]].

One interesting operation on ringoids is the ($Ab$-enriched) [[Cauchy completion]], which is the completion under finite [[direct sums]] and [[split idempotents]].  In particular, the Cauchy completion of a ring $R$ is the category of [[finitely generated object|finitely generated]] [[projective object|projective]] $R$-modules (aka [[split monomorphism|split]] [[subobjects]] of finite-rank [[free object|free]] modules).  Every ringoid is [[equivalence|equivalent]] to its Cauchy completion in the bicategory $Ab Prof$, and two ringoids are equivalent in $Ab Prof$ if and only if their Cauchy completions are [[equivalence of categories|equivalent]] as $Ab$-enriched categories.  This sort of equivalence is naturally called [[Morita equivalence]].

See also [[dg-category]].


## Examples

* The category [[Ab]] is [[closed monoidal category|closed monoidal]] and hence canonically enriched over itself.

* An $Ab$-enriched category with one object is precisely a [[ring]].

* For any small $Ab$-enriched category $R$, the enriched [[presheaf category]] $[R^{op},Ab]$ is, of course, $Ab$-enriched.  If $R$ is a ring, as above, then $[R^{op},Ab]$ is the category of $R$-modules.


## Related concepts

* [[hom-group]]

* [[additive category]]

## References

The original articles on ringoids:

* [[Barry Mitchell]]: *Rings with several objects*, Advances in Mathematics
**8** 1 (1972) 1-161 \[<a href="https://doi.org/10.1016/0001-8708(72)90002-3">doi:10.1016/0001-8708(72)90002-3</a>\]

* {#Chu84} [[Po-Hsiang Chu]], *Theory of Ringoids*, PhD thesis, McGill University (1984) &lbrack;[escholar:q811kn193](https://escholarship.mcgill.ca/concern/theses/q811kn193), [[Chu-Ringoids.pdf:file]]&rbrack;

* [[Daniel Murfet]], _Localisation of ringoids_, notes (2006)  &lbrack;[pdf](http://therisingsea.org/notes/LocalisationOfRingoids.pdf)&rbrack;

Exposition:

* John Baez, *[Ringoids](http://golem.ph.utexas.edu/category/2006/09/ringoids.html)*, blog (2006)

Textbook accounts on $Ab$-enriched categories (mostly: [[abelian categories]]) and their application in ([[homological algebra|homological]]) [[algebra]]:

* [[Nicolae Popescu]], _[[Abelian categories with applications to rings and modules]]_, London Math. Soc. Monographs **3**, Academic Press (1973)  &lbrack;[MR0340375](http://www.ams.org/mathscinet-getitem?mr=0340375)&rbrack;

* [[Charles Weibel]]: *[[An Introduction to Homological Algebra]]* Cambridge Univ. Press (1994) &lbrack;[doi:10.1017/CBO9781139644136](https://doi.org/10.1017/CBO9781139644136)&rbrack;




[[!redirects Ab-enriched category]]
[[!redirects Ab-enriched categories]]
[[!redirects Ab-enriched]]
[[!redirects Ab-category]]
[[!redirects Ab-categories]]
[[!redirects ringoid]]
[[!redirects ringoids]]
