
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Categories of categories
+-- {: .hide}
[[!include categories of categories - contents]]
=--
=--
=--


# $Rel$
* table of contents
{: toc}

## Idea

Roughly, $Rel$ is the [[category]] whose [[objects]] are [[sets]] and whose [[morphisms]] are (binary) [[relations]] between sets. It becomes a [[2-category]] (in fact, a [[2-poset]]) by taking [[2-morphisms]] to be inclusions of relations. 


## Definition

$Rel$ is a [[2-poset]] (a [[enriched category|category enriched]] in the category of [[posets]]), whose [[objects]] or $0$-cells are [[sets]], whose [[morphisms]] or $1$-cells $X \to Y$ are [[relations]] $R \subseteq X \times Y$, and whose [[2-morphisms]] or  $2$-cells $R \to S$ are inclusions of relations. The _composite_ $S \circ R$ of morphisms $R: X \to Y$ and $S: Y \to Z$ is defined by the usual relational composite 
$$\{(x, z) \in X \times Z: \exists_{y \in Y} (x, y) \in R \wedge (y, z) \in S\} \hookrightarrow X \times Z$$ 
and the _identity_ $1_X: X \to X$ is the [[equality relation]], in other words the usual diagonal embedding 
$$\{(x, x): x \in X\} \hookrightarrow X \times X.$$ 

Another important operation on relations is _taking the opposite_: any relation $R: X \to Y$ induces a relation 
$$R^{op} = \{(y, x) \in Y \times X: (x, y) \in R\} \hookrightarrow Y \times X$$ 
and this operation obeys a number of obvious identities, such as $(S \circ R)^{op} = R^{op} \circ S^{op}$ and $1_X^{op} = 1_X$. 


## Relations and spans

It is useful to be aware of the connections between the [[bicategory of relations]] and the [[bicategory]] of [[span|spans]]. Recall that a _span_ from $X$ to $Y$ is a diagram of the form 
$$X \leftarrow S \to Y$$ 
and there is an obvious category whose objects are spans from $X$ to $Y$ and whose morphisms are morphisms between such diagrams. The terminal span from $X$ to $Y$ is 
$$X \stackrel{\pi_1}{\leftarrow} X \times Y \stackrel{\pi_2}{\to} Y$$ 
and a relation from $X$ to $Y$ is just a [[subobject]] of the terminal span, in other words an isomorphism class of monos into the terminal span. 

To each span $S$ from $X$ to $Y$, there is a corresponding relation from $X$ to $Y$, defined by taking the [[image]] of the unique morphism of spans $S \to X \times Y$ between $X$ and $Y$. It may be checked that this yields a lax morphism of bicategories 
$$Span \to Rel$$ 


## Relations in a category

More generally, given any [[regular category]] $C$, one can form a 2-category of relations $Rel(C)$ in similar fashion. The objects of $Rel(C)$ are objects of $C$, the morphisms $r: c \to d$ in $Rel(C)$ are defined to be [[subobject|subobjects]] of the terminal span from $c$ to $d$, and 2-cells $r \to s$ are subobject inclusions. To form the composite of $r \subseteq c \times d$ and $s \subseteq d \times e$, one takes the [[image]] of the unique span morphism 
$$r \times_c s \to c \times e$$ 
in the category of spans from $c$ to $e$, thus giving a mono into the terminal span from $c$ to $e$. The subobject class of this mono defines the relation 
$$s \circ r \subseteq c \times e$$ 
and the axioms of a regular category ensure that $Rel(C)$ is a 2-category with desirable properties. Similar to what was said above, there is again a lax morphism of bicategories 
$$Span(C) \to Rel(C)$$

There is also a functor 
$$i: C \to Rel(C)$$ 
that takes a morphism $f: c \to d$ to the functional relation defined by $f$, i.e., the relation defined by the subobject class of the mono 
$$\langle 1, f\rangle: c \to c \times d$$

Such functional relations may also be characterized as precisely those 1-cells in $Rel(C)$ which are [[adjunction|left adjoints]]; the right adjoint of $\langle 1, f \rangle$ is the opposite relation $\langle f, 1\rangle$. The unit amounts to a condition 
$$1_c \subseteq \langle f, 1 \rangle \circ \langle 1, f \rangle$$ 
which says that the functional relation is _total_, and the counit amounts to a condition 
$$\langle 1, f \rangle \circ \langle f, 1 \rangle \subseteq 1_d$$ 
which says the functional relation is _well-defined_. 


## Limits and Colimits

$Rel$ does have [[products]] and [[coproducts]]; they coincide (by
self-duality) and are just [[disjoint unions]] of sets. However, otherwise
$Rel$ has very few (co)limits; it doesn't even have
splittings of all idempotents. All symmetric idempotents have splittings, but the
order-relation $\leq \; \subseteq \{0,1\} \times \{0,1\}$ can't be
split. It follows that it can't have (co)equalisers.

However, $Rel$ has _weak_ [[equalizers]], therefore one can take its
[[exact completion]]. This happens to be the category of complete
sup-lattices and sup-preserving maps. And the tensor product on $Rel$
extends to the [[exact completion]]. 

Since $Rel$ is the category of _free algebras_ ([[Kleisli
category]]) for the powerset monad, there is, indeed, very little chance
of a limit of such algebras being free again. To get decent limits,
one has to move to the [[Eilenberg-Moore category]] of the [[powerset]] [[monad]],
viz., the category of complete [[suplattices]].

### In the Double Category of Relations###
If you insert the category $Rel$ into the [[double category]]
$\mathrm{RRel}$ of sets, mappings and relations, one has a double
category with all [[double limits]] and colimits. For instance, the
obvious cartesian product $a \times b : X \times Y \to X' \times Y'$ (resp. sum
$a+b : X + Y \to X' + Y'$) of two relations is indeed a product
(resp. a sum) in the double category.

Similarly, many bicategories of spans, cospans, relations,
profunctors, etc. have poor (co)limits, but can be usefully embedded in
weak double categories (with the same objects, "strict morphisms",
"same morphisms", suitable double cells) that have all limits and
colimits.

### As an enriched category###
Writing $\mathcal{V}$ for the category of [[suplattices]], $Rel$ is a
$\mathcal{V}$-category (see [[enriched category]]). With that in mind, the parallel:

* in [[additive categories]] with [[zero object]], \emph{finitary} (co)[[products]]
  are [[biproducts]]
* $\mathcal{V}$-categories with [[zero object]], \emph{arbitrary}
  (co)[[products]] are [[biproducts]]

is remarkable. This was probably first noticed by Dana May Latch, in
the 20th century, for the category of $\mathcal{V}$ of complete
[[suplattices]]. 

The [[matrix algebra]] for maps to products, from coproducts, and most
especially, from coproducts to products, works just as it does in the
case of [[additive categories]], when it comes to these
$\mathcal{V}$-categories. 


###In Spans###
See [[van Kampen colimit]].

##Mono/Epimorphisms##
It is not hard to see that a relation $R \subseteq A \times B$ is a
[[monomorphism]] $A \to B$ iff the map $\mathcal{P}A \to \mathcal{P}B$
sending a subset of A to the set of all R-relatives of its members is
injective; dually for [[epimorphisms]].




## Related categories

* [[Set]]

A [[category of correspondences]] is a generalization of a category of relations. The composition of relations is that of correspondences followed by [[(-1)-truncated|(-1)-truncation]].

For generalizations of $Rel$ see

* [[allegory]], [[cartesian bicategory]]

* [[bicategory of relations]]


## References ##

* Grandis, M., Pare, R. :Limits in double categories. Cahiers Topologie Ge &#769;om. Diffe &#769;rentielle Cate &#769;g. 40(3), 162&#8211;220 (1999)
* [categories: Limits and colimits in Rel?](http://thread.gmane.org/gmane.science.mathematics.categories/8027), [categories: Limits in REL](http://thread.gmane.org/gmane.science.mathematics.categories/8186)



category: category

[[!redirects Rel]]
[[!redirects REL]]
[[!redirects rel]]