#Definition#

An **Ab-enriched category** is a [[enriched category|category enriched in]] the cateory [[Ab]] of abelian groups.

Sometimes this is called a [[pre-additive category]].

#Remarks#

* The above means explicitly that
an Ab-enriched category is a category $C$ such that
for all objects $a,b$ the [[hom-set]] $Hom_C(a,b)$
is equipped with the structure of an abelian group; and
such that for all triples $a$, $b$, $c$ of objects the
[[composition]] operation 
$
  \circ_{a,b,c} : Hom_C(a,b) \times Hom_C(b,c) \to Hom_C(a,c)
$
is bilinear.

* There is a canonical forgetful functor $Ab \to Set_*$ from
abelian groups to pointed sets, which sends each group to its underlying set with point being the neutral element. Using this functor every pre-addive category $C$ is in particular also a  category that is enriched over pointed sets. This is sufficient for there to be a notion of 
[[zero morphism]], [[kernel]] and [[cokernel]] in 
$C$.


#Properties#

## An  Ab-enriched category has biproducts ##

For $a, b \in C$ two objects in an Ab-enriched category $C$,  [[generalized the|the]] [[product]] $a \times b$ coincides  with [[generalized the|the]] [[coproduct]] $a \cup b$ when either exists. This [[biproduct]] is denoted
$$
  a \oplus b
$$
and called the **direct sum** of $a$ and $b$.

The [[isomorphism]]
$$
  r : c_1 \sqcup c_2 \stackrel{\simeq}{\to} c_1 \times c_2
$$
is the unique morphism characterized by
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
  \,.
$$


#Examples#

* The category [[Ab]] is [[closed monoidal category|closed monoidal]] and hence canonically enriched over itself.

* In general [[abelian category|abelian categories]] are the most important examples of Ab-enriched categories. 