
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

$Rel$ is the [[category]] whose [[objects]] are [[sets]] and whose [[morphisms]] are (binary) [[relations]] between sets.   It becomes a [[2-category]] $\mathbf{Rel}$ (in fact, a [[2-poset]]) by taking [[2-morphisms]] to be inclusions of relations. 

## Definition

$Rel$ is a category whose  [[objects]] or $0$-cells are [[sets]], whose [[morphisms]] or $1$-cells $X \to Y$ are [[relations]] $R \subseteq X \times Y$, and where the _composite_ $S \circ R$ of morphisms $R: X \to Y$ and $S: Y \to Z$ is defined as the usual relational composite:
$$\{(x, z) \in X \times Z: \exists_{y \in Y} (x, y) \in R \wedge (y, z) \in S\} \subseteq X \times Z .$$   The _identity_ $1_X: X \to X$ is then the [[equality relation]], in other words the usual diagonal embedding 
$$\{(x, x): x \in X\} \subseteq X \times X.$$ 

Another important operation on relations is taking the _opposite_, also known as the _transpose_ or sometimes the _converse_.   Any relation $R: X \to Y$ induces a relation 
$$R^\dagger = \{(y, x) \in Y \times X: (x, y) \in R\} \subseteq Y \times X$$ 
This makes $Rel$ into a [[dagger-category]]: in other words, we have $(S \circ R)^\dagger = R^\dagger \circ S^\dagger$, $1_X^\dagger = 1_X$, and $(R^{\dagger})^{\dagger} = R$.

We can enhance $Rel$ to a 2-category, which we can call $\mathbf{Rel}$ to distinguish it from the mere category, by taking [[2-morphisms]] or $2$-cells $R \Rightarrow S$ to be inclusions of relations.   Since there is at most one 2-morphism between parallel 1-morphisms, $\mathbf{Rel}$ is a [[2-poset]]: that is, an [[enriched category|category enriched]] in the category of [[posets]].

## Relations and spans

It is useful to be aware of the connections between the [[bicategory of relations]] and the [[bicategory]] of [[span|spans]]. Recall that a _span_ from $X$ to $Y$ is a diagram of the form 
$$X \leftarrow S \to Y$$ 
and there is an obvious category whose objects are spans from $X$ to $Y$ and whose morphisms are morphisms between such diagrams. The terminal span from $X$ to $Y$ is 
$$X \stackrel{\pi_1}{\leftarrow} X \times Y \stackrel{\pi_2}{\to} Y$$ 
and a relation from $X$ to $Y$ is just a [[subobject]] of the terminal span, in other words an isomorphism class of monos into the terminal span. 

To each span $S$ from $X$ to $Y$, there is a corresponding relation from $X$ to $Y$, defined by taking the [[image]] of the unique morphism of spans $S \to X \times Y$ between $X$ and $Y$. It may be checked that this yields a lax morphism of bicategories 
$$Span \to Rel$$ 

## Limits and colimits##

The category $Rel$ does have [[products]] and [[coproducts]]; they coincide (by self-duality) and are just [[disjoint unions]] of sets. However, otherwise $Rel$ has very few (co)limits; it doesn't even have
splittings of all idempotents. All symmetric idempotents have splittings, but the order-relation $\leq \; \subseteq \{0,1\} \times \{0,1\}$ can't be
split. It follows that it can't have (co)equalisers.

Since the category $Rel$ is the category of _free algebras_ ([[Kleisli
category]]) for the powerset monad, there is, indeed, very little chance
of a limit of such algebras being free again. To get decent limits,
one has to move to the [[Eilenberg-Moore category]] of the [[powerset]] [[monad]],
viz., the category of complete [[suplattices]].

### Weak equalizers and completion###

As the category $Rel$ has _[[weak limit|weak]]_ [[equalizers]], one can take its [[exact completion]]. This happens to be the category of complete
sup-lattices and sup-preserving maps. And the tensor product on $Rel$
extends to the [[exact completion]]. 

The Freyd completion of $Rel$, which is equivalent to the category of basic pairs which appear in formal topology, has all limits exactly because $Rel$ has products and weak equalizers. The Freyd completion adds freely a strong factorization system to a(ny) category $C$.  The Freyd completion has products if $C$ has products, and it has equalizers if $C$ has weak equalizers.

### In the double category of relations###

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

## As an enriched category##

Writing $\mathcal{V}$ for the category of [[suplattices]], $Rel$ is a
$\mathcal{V}$-category (see [[enriched category]]). With that in mind, the parallel:

* in [[additive categories]] with [[zero object]], _finitary_ (co)[[products]]
  are [[biproducts]]
* $\mathcal{V}$-categories with [[zero object]], _arbitrary_
  (co)[[products]] are [[biproducts]]

is remarkable. This was probably first noticed by [[Dana May Latch]], in
the 20th century, for the category of $\mathcal{V}$ of complete
[[suplattices]]. 

The [[matrix algebra]] for maps to products, from coproducts, and most
especially, from coproducts to products, works just as it does in the
case of [[additive categories]], when it comes to these
$\mathcal{V}$-categories. 

##In spans##
See [[van Kampen colimit]].

##Mono/epimorphisms##

It is not hard to see that a relation $R \subseteq A \times B$ is a
[[monomorphism]] $A \to B$ iff the map $\mathcal{P}A \to \mathcal{P}B$
sending a subset of A to the set of all R-relatives of its members is
injective; dually for [[epimorphisms]].

## 2-categorical aspects##

Recall that we are using $\mathbf{Rel}$ to stand for the 2-category of sets, relations and inclusions.   Various facts about relations can be recast in these terms.  For example, a relation $L : X \to Y$ is a function from $X$ to $Y$ iff it has a right adjoint $R : Y \to X$ in $\mathbf{Rel}$.  In this case, its right adjoint equals its transpose $L^\dagger : Y \to X$.

Similarly, a monad $T : X \to X$ in the 2-category $\mathbf{Rel}$ is exactly a preorder on $X$, since the existence of a unit $i: 1_X \Rightarrow T$ says that $T$ is reflexive and the existence of the multiplication $m: T^2 \Rightarrow T$ says that $T$ is transitive.    This monad has an [[Eilenberg-Moore category|Eilenberg-Moore object]] iff it is an equivalence relation, in which case the Eilenberg-Moore object is the set of equivalence classes of the relation.

## Relations in a category

More generally, given any [[regular category]] $C$, one can form a 2-category of relations $\mathbf{Rel}(C)$ in similar fashion. The objects of $\mathbf{Rel}(C)$ are objects of $C$, the morphisms $r: c \to d$ in $\mathbf{Rel}(C)$ are defined to be [[subobject|subobjects]] of the terminal span from $c$ to $d$, and 2-cells $r \to s$ are subobject inclusions. To form the composite of $r \subseteq c \times d$ and $s \subseteq d \times e$, one takes the [[image]] of the unique span morphism 
$$r \times_c s \to c \times e$$ 
in the category of spans from $c$ to $e$, thus giving a mono into the terminal span from $c$ to $e$. The subobject class of this mono defines the relation 
$$s \circ r \subseteq c \times e$$ 
and the axioms of a regular category ensure that $\mathbf{Rel}(C)$ is a 2-category with desirable properties. Similar to what was said above, there is again a lax morphism of bicategories 
$$Span(C) \to \mathbf{Rel}(C)$$

There is also a functor 
$$i: C \to \mathbf{Rel}(C)$$ 
that takes a morphism $f: c \to d$ to the functional relation defined by $f$, i.e., the relation defined by the subobject class of the mono 
$$\langle 1, f\rangle: c \to c \times d$$

Such functional relations may also be characterized as precisely those 1-cells in $Rel(C)$ which are [[adjunction|left adjoints]]; the right adjoint of $\langle 1, f \rangle$ is the opposite relation $\langle f, 1\rangle$. The unit amounts to a condition 
$$1_c \subseteq \langle f, 1 \rangle \circ \langle 1, f \rangle$$ 
which says that the functional relation is _total_, and the counit amounts to a condition 
$$\langle 1, f \rangle \circ \langle f, 1 \rangle \subseteq 1_d$$ 
which says the functional relation is _well-defined_. 

## Related categories

* [[Set]]

* [[FinRel]]

A [[category of correspondences]] is a generalization of a category of relations. The composition of relations is that of correspondences followed by [[(-1)-truncated|(-1)-truncation]].

For generalizations of $Rel$ see

* [[allegory]], [[cartesian bicategory]]

* [[bicategory of relations]]

* [[Prof]]


## References ##

* Grandis, M., Pare, R. :[Limits in double categories](https://eudml.org/doc/91618). Cahiers Topologie Géom. Différentielle Catég. 40(3), 162&#8211;220 (1999)
* Bucalo, A., Rosolini, G., Completions, comonoids, and topological spaces
Annals of Pure and Applied Logic 137, 104-125 (2006) 
* _Credits for the section on limits go to the contributors of the following threads on the categories list:_ [categories: Limits and colimits in Rel?](http://thread.gmane.org/gmane.science.mathematics.categories/8027), [categories: Limits in REL](http://thread.gmane.org/gmane.science.mathematics.categories/8186)



category: category

[[!redirects Rel]]
[[!redirects REL]]
[[!redirects rel]]