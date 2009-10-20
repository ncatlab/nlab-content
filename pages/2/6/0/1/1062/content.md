An __Ab-enriched category__ is a category [[enriched category|enriched over]] the category [[Ab]] of abelian groups with its usual [[tensor product]].

Sometimes Ab-enriched categories are called [[pre-additive category|pre-additive categories]], although sometimes that term also implies the existence of a [[zero object]].  They are also sometimes called [[ringoids]], since the concept is a [[horizontal categorification]] (or 'oidification') of the concept of a [[ring]].


#Remarks#

*  Explicitly, the definition means that
an Ab-enriched category is a category $C$ such that
for all objects $a,b$ the [[hom-set]] $Hom_C(a,b)$
is equipped with the structure of an [[abelian group]]; and
such that for all triples $a$, $b$, $c$ of objects the
[[composition]] operation 
$
  \circ_{a,b,c} : Hom_C(a,b) \times Hom_C(b,c) \to Hom_C(a,c)
$
is bilinear.

* There is a canonical forgetful functor $Ab \to Set_*$ from
abelian groups to [[pointed set]]s, which sends each group to its underlying set with point being the neutral element. Using this functor every pre-additive category $C$ is in particular also a  category that is enriched over pointed sets. This is sufficient for there to be a notion of 
[[zero morphism]], [[kernel]] and [[cokernel]] in 
$C$.

* In general [[abelian category|abelian categories]] are the most important examples of Ab-enriched categories.  See [[additive and abelian categories]].


# Finite products are Cauchy #

One of the remarkable facts about Ab-enriched categories is that finite products (and coproducts) are [[Cauchy colimit]]s.  This implies that finite products coincide with finite coproducts, and are preserved by _any_ Ab-enriched functor.  


## Zero objects ##

In an Ab-enriched category $C$, any [[initial object]] is also a [[terminal object]], hence a [[zero object]], and dually.  An object $a\in C$ is a zero object just when its identity $1_a$ is equal to the zero morphism $0:a\to a$ (that is, the identity element of the abelian group $\hom_C(a,a)$).  Expressed in this way, it is easy to see that any Ab-enriched functor preserves zero objects.


## Biproducts ##

For $c_1, c_2 \in C$ two objects in an Ab-enriched category $C$,  [[generalized the|the]] [[product]] $c_1 \times c_2$ coincides  with [[generalized the|the]] [[coproduct]] $c_1 \sqcup c_2$ when either exists.  More precisely, when both exist, the canonical morphism
$$
  r : c_1 \sqcup c_2 \to c_1 \times c_2
$$
defined by
$$
  \left(
    c_i \to c_1 \sqcup c_2 \stackrel{r}{\to} c_1 \times c_2 \to c_j
  \right)
  =
  \left\{
    \array{
      Id_c_i & if i = j
      \\
      0 & if i \neq j
    }
  \right.
  \,,
$$
which exists whenever $c_1\sqcup c_2$ and $c_1\times c_2$ do, is an [[isomorphism]].  This object is called a [[biproduct]] or (sometimes) a [[direct sum]] and is generally denoted
$$
  c_1 \oplus c_2.
$$
It can be characterized diagrammatically as an object $c_1\oplus c_2$ equipped with morphisms $q_i:c_i\to c_1\oplus c_2$ and $p_i:c_1\oplus c_2 \to c_i$ such that $p_i q_j = \delta_{i j}$ and $q_1 p_1 + q_2 p_2 = 1_{c_1\oplus c_2}$.  Expressed in this form, it is clear that any Ab-enriched functor preserves biproducts.



#Examples#

* The category [[Ab]] is [[closed monoidal category|closed monoidal]] and hence canonically enriched over itself.

* An Ab-enriched category with one object is precisely a [[ring]].

* For any small Ab-enriched category $R$, the enriched [[presheaf category]] $[R^{op},Ab]$ is, of course, Ab-enriched.  If $R$ is a ring, as above, then $[R^{op},Ab]$ is the category of $R$-modules.


#Blog resources#

* John Baez, [Ringoids](http://golem.ph.utexas.edu/category/2006/09/ringoids.html)
