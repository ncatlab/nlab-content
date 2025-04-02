+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# $\dagger$ categories
* tic
{: toc}


## Idea

The definition of a [[category]] effectively enforces an ordering on the "0-faces" -- the source and target [[object|objects]] -- of every 1-cell (every [[morphism]]). In many cases this is essential, in that there is no way to regard the generic morphism $a \stackrel{f}{\to} b$ in the category as a morphism from $b$ to $a$ instead.

But there are many categories for which this is not the case, where every morphism naturally only comes with the information of an unordered pair $\{a,b \}$ of objects, without any prejudice on which is to be regarded as source and which as target. An important general example is:

* the category $Spans(C)$ of [[span|spans]] in a category $C$ with pullbacks, or [[duality|dually]], the category $CoSpans(C)$ of [[cospan|cospans]] in a category $C$ with pushouts.

More concrete examples are:

* categories of [[cobordism|cobordisms]] (but notice that cobordisms are naturally regarded as [[cospan|cospans]] which makes this a special case of the above example);

* the category [[Hilb]] of Hilbert spaces, where for every linear map $f : H_1 \to H_2$ we also have the adjoint map (in the sense of Hilbert spaces, not in the categorical sense) $f^\dagger : H_2 \to H_1$ (but notice that according to [[groupoidification]] this is also essentially to be regarded as a special case of categories of spans).

A _dagger structure_ on a category is extra structure which encodes the idea of _removing_ the ordering information on the 0-faces of 1-cells in a category: it is a contravariant functor which sends every morphism $f : a \to b$ to a morphism going the other way, $f^\dagger : b \to a$.

The notation and terminology here is motivated from the example [[Hilb]] of Hilbert spaces, where $f^\dagger$ is traditionally the notion for the adjoint of a linear map $f$.  The canonical &#8224;-structure on [[Hilb]] and on [[nCob]] is crucial in [[FQFT|quantum field theory]] where it is used to encode the idea of **unitarity**:

a _unitary_ [[FQFT|functorial QFT]] of dimension $n$ is supposed to be a functor $n Cob \to Hilb$ which respects the &#8224;-structure on both sides.


## Terminology

In Wikipedia a [dagger category](http://en.wikipedia.org/wiki/Dagger_category) is said to be the same as _involutive category_ or _category with involution_.  However, [Springer's Encyclopedia of Mathematics](https://encyclopediaofmath.org/wiki/Category_with_involution) requires that a "category with involution" is also compatibly [[enriched category|enriched]] over [[posets]].

In enriched category theory, involutive categories have also been called **symmetric categories**. Sometimes the involution is required to be strict in the sense that the dagger is an *equality* rather than an *isomorphism*: in line with [[horizontal categorification]], one could argue these should be called **commutative categories**, since a one-object category with such an involution is a [[commutative monoid]].

## Definition

### Dagger categories

#### With a family of functions

\begin{definition}
A **dagger category** or $\dagger$-category $C$ is a [[category]] with a function $(-)^\dagger: Hom_C(A,B) \to Hom_C(B,A)$ for every object $A,B \in Ob(C)$, such that 

* for every $A \in Ob(C)$, $(1_A)^\dagger = 1_A$,
* for every $A,B \in Ob(C)$ and every $f \in Hom_C(A,B)$ and $g \in Hom_C(B,C)$, $(g \circ f)^\dagger = f^\dagger \circ g^\dagger$,
* and for every $A,B \in Ob(C)$ and every $f \in Hom_C(A,B)$, $((f)^\dagger)^\dagger = f$. 

\end{definition}

#### With a function

\begin{definition}
Given a category $C$ with a type or class of objects $Ob(C)$ and a set of morphisms $Mor(C)$ with source and target functions $s:Mor(C) \to Ob(C)$ and $t:Mor(C) \to Ob(C)$, $C$ is a **dagger category** if it has a function $(-)^\dagger:Mor(C) \to Mor(C)$ such that 

* for every term $f:Mor(C)$, $s(f) = t(f^\dagger)$
* for every term $f:Mor(C)$, $t(f) = s(f^\dagger)$
* for every term $f:Mor(C)$, $(f^\dagger)^\dagger = f$
* for every term $a:Ob(C)$, $id(a)^\dagger = id(a)$
* for every term $f:Mor(C)$ and $g:Mor(C)$ such that $t(f) =_D s(g)$, $(g \circ f)^\dagger = f^\dagger \circ g^\dagger$. 

\end{definition}

#### With a functor 

\begin{definition}
A **dagger category** is a [[category]] $C$ equipped with a [[contravariant functor|contravariant endofunctor]], hence an ordinary [[functor]] from the [[opposite category]] $C^{op}$ of $C$ to $C$ itself

$$
  \dagger : C^{op} \to C
$$

which 

1. is the [[identity-on-objects]], 

1. is an [[involution]] $\dagger^{op} \circ \dagger = \mathrm{id}_C$.

\end{definition}

This definition, which is perhaps the most concise, does rely on a notion of [[identity-on-objects functor]].  This is no problem in most foundations for mathematics, although it violates the [[principle of equivalence]] (except for [[strict categories]]).  In [[homotopy type theory]] (or more generally [[intensional type theory]]) it doesn't make sense to talk about "being the identity on objects" as a property of a given functor, but one can still define an "identity-on-objects endofunctor" (covariant or contravariant) as a basic notion; see [[identity-on-objects functor]] for details.  When unwound for $\dagger$-categories, this yields the above "family of functions" definition.

### Special morphisms

+-- {: .un_defn}
###### Definition

A morphism $f$ in a &#8224;-category is called a **[[unitary morphism]]** if its &#8224;-adjoint equals its [[inverse]]:

$$
  f^\dagger = f^{-1}
  \,.
$$

=--


For the purpose of considering what makes two objects of a $\dagger$-category [[equivalence|equivalent]], one should not consider all [[isomorphism|isomorphisms]] (invertible morphisms) but rather all unitary isomorphisms.

The unitary isomorphisms form a [[groupoid]], which may be regarded as the _dagger-[[core]]_ of the $\dagger$-category.


For example, in [[Hilb]], there are many invertible linear operators, but only those of norm $1$ (the invertible isometries) are unitary.

+-- {: .un_defn}
###### Definition

A morphism $f$ in a &#8224;-category is called a **[[self-adjoint morphism]]** if it equals its &#8224;-adjoint

$$
  f^\dagger = f
  \,.
$$

 

=--


### The category of &#8224;-categories {#CatOfDagCats}

+-- {: .un_defn}
###### Definition
Given two $\dagger$-categories $A$ and $B$, a [[dagger functor|$\dagger$-functor]] $F : A \to B$ consists of a function $F_0 : Ob(A) \to Ob(B)$ with a function $F_{a,b}:Hom_A(a,b) \to Hom_B(F a,F b)$ for every object $a,b:Ob(A)$, where $F_{a,b}$ is generally also denoted as $F$, such that

* for every object $a \in Ob(A)$, $F(1_a)=1_{F a}$, 
* for every object $a,b,c \in Ob(A)$ and morphisms $f \in Hom_A(a,b)$ and $g \in Hom_A(b,c)$, $F(g \circ_A f) = F g \circ_B F f$
* for every object $a,b \in Ob(A)$ and morphism $f \in Hom_A(a,b)$, $F(f^{\dagger_A}) = (F f)^{\dagger_B}$. 
=--

More concisely, one can say that a $\dagger$-functor $(A,\dagger) \to (B,\ddagger)$ is a [[functor]] $F : A \to B$ of the underlying categories that commutes with the $\dagger$-structures in that $F \circ \dagger = \ddagger \circ F^{op}$.  This appears to violate the [[principle of equivalence]], since it is a strict equality of functors; however, once $\dagger$ and $\ddagger$ are known to be the identity on objects (whatever that means), the two functors $F\circ \dagger$ and $\ddagger \circ F^{op}$ automatically agree on objects.

A [[natural transformation]] between $\dagger$-functors is just a natural transformation of the underlying functors. 

+-- {: .un_defn}
###### Definition

The &#8224;-adjoint $\eta^*$ of a natural transformation 

$$
  \eta : F \to G 
$$

between two &#8224;-functors $F, G : (C,\dagger) \to (D,\ddagger)$ is given by the componentwise $\ddagger$-adjoint:

$$
  (\eta^*)_a := (\eta_a)^\ddagger
  \,.
$$

=--

To check that $\eta^*$ is indeed a natural transformation $\eta^* : G \to F$
consider $f : a \to b$ any morphism in $C$ and $f^\dagger : b \to a$ its $\dagger$-adjoint and let 

$$
  \array{
    F(a) &\stackrel{\eta_a}{\to}& G(a)
    \\
    \uparrow^{\mathrlap{F(f^\dagger)}} && \uparrow^{\mathrlap{G(f^\dagger)}}
    \\
    F(b) &\stackrel{\eta_b}{\to}& G(b)
  }
$$

be the corresponding naturality square of $\eta$. Taking the $\ddagger$-adjoint of the entire diagram yields

$$
  \array{
    F(a) &\stackrel{\eta_a^\ddagger}{\leftarrow}& G(a)
    \\
    \downarrow^{\mathrlap{F(f^\dagger)^{\ddagger}}} 
    && 
    \downarrow^{\mathrlap{G(f^\dagger)^{\ddagger}}}
    \\
    F(b) &\stackrel{\eta_b^{\ddagger}}{\leftarrow}& G(b)
  }
  \;\;\;
  =
  \;\;\;
  \array{
    F(a) &\stackrel{\eta_a^\ddagger}{\leftarrow}& G(a)
    \\
    \downarrow^{\mathrlap{F(f)}} 
    && 
    \downarrow^{\mathrlap{G(f)}}
    \\
    F(b) &\stackrel{\eta_b^{\ddagger}}{\leftarrow}& G(b)
  }
$$

by the fact that $F$ and $G$ are &#8224;-functors. This is the naturality square over $f$ of $\eta^* : G \to F$.


+-- {: .un_defn}
###### Definition

Write $DagCat$ for the [[category]] whose objects are &#8224;-categories and whose morphisms are &#8224;-functors.

For $(C,\dagger)$ and $(D,\dagger)$ two &#8224;-categories, write 
$([(C,\dagger),(D,\ddagger)]_{dag}, \star) \in DagCat$ for the &#8224;-category whose objects are &#8224;-functors, whose morphisms are natural transformations, with the &#8224;-operation $\star : \eta \mapsto \eta^*$ as above.

=--

+-- {: .un_prop}
###### Proposition

The assignment $((C,\dagger),(D,\ddagger)) \mapsto [(C,\dagger),(D,\ddagger)]_{dag}, \star)$ extends to an [[internal hom]]-functor

$$
  [-,-] : DagCat^{op} \times DagCat \to DagCat
$$

that makes $DagCat$ into a [[cartesian closed category]].

=--

+-- {: .proof}
###### Proof

This follows step-by-step the standard proof that [[Cat]] is cartesian closed, while observing that each step respects the respect for &#8224;-structures.

To indicate the main point, let $C, D$ and $E$ be &#8224;-categories and consider a functor $F : C \times D \to E$. For $(f : c_1 \to c_2) \in C$ and $(g : d_1 \to d_2) \in D$ we have natural assignments

$$
  \array{
    (c_1, d_1) &\stackrel{(Id,g)}{\to}& (c_1, d_2)  
    \\
    \downarrow^{\mathrlap{(f,Id)}} &\searrow^{(f,g)}& \downarrow^{\mathrlap{(f,Id)}}
    \\
    (c_2, d_1)
    &\stackrel{(Id,g)}{\to}&
    (c_2, d_2)
  }
  \;\;\;\;\;
  \mapsto
  \;\;\;\;\;
  \array{
    F(c_1, d_1) &\stackrel{F(Id,g)}{\to}& F(c_1, d_2)  
    \\
    \downarrow^{\mathrlap{F(f,Id)}} && \downarrow^{\mathrlap{F(f,Id)}}
    \\
    F(c_2, d_1)
    &\stackrel{F(Id,g)}{\to}&
    f(c_2, d_2)
  }
$$ 

that respect daggering all morphisms, in the evident way.

Keeping $d_1$ and $d_2$ fixed, respectively this makes $F(-,d_1), F(-,d_2) : C \to E$ &#8224;-functors. We see from the diagrams that $F(-,(d_1 \stackrel{g}{\to}) d_2)$ is a natural transformation between these &#8224;-functors, and the fact that $F$ [[intertwiner|intertwines]] the dagger operation of $D$ with that of $E$ means $F$ regarded as a functor $D \to [C,E]$ intertwines the &#8224;-structures of $D$ and $[D,E]_{dag}$, by the above definition.

=--

## Examples

* The category [[Rel]] of sets and [[relations]] is a &#8224;-category, taking dagger as relational converse.

* More generally, let $C$ be a category with [[pullbacks]] and let $Span_1(C)$ be the 1-category of [[spans]] up to isomorphism: its morphisms are spans with one leg labeled as source, the other labeled as target. Then the functor $\dagger : Span_1(C)^{op} \to Span_1(C)$ which just exchanges this labeling is a &#8224;-structure on $Span_1(C)$.

* $\mathcal{R}(G)$, the category of unitary [[representation|representations]] of a (discrete) [[group]] $G$ and intertwining maps, is a &#8224;-category. For an intertwiner $\phi : R \rightarrow S$, let $\phi^\dagger : S \rightarrow R$ be the adjoint of $\phi$ in [[Hilb]].

* The [[category of couplings]] between [[probability spaces]].

* Every [[symmetric proset]] is a [[thin category|thin]] &#8224;-category. 


## Variants

* [[strict dagger category]]

* [[univalent dagger category]]

### Monoidal &#8224;-categories

* [[monoidal dagger category]]

  * [[braided monoidal dagger category]]

  * [[symmetric monoidal dagger category]]

  * [[compact closed dagger category]]

  * [[cartesian monoidal dagger category]]

  * [[cocartesian monoidal dagger category]]

  * [[semiadditive dagger category]]

### $\dagger$-2-posets

A [[dagger 2-poset|$\dagger$-2-poset]] is a $\dagger$-category that is also a [[2-poset]]. Examples of $\dagger$-2-posets include [[allegories]] and [[bicategories of relations]]. 

### Model structure on &#8224;-categories {#ModelStructure}

> the following is based on a remark by [[Andre Joyal]], [posted](https://github.com/punkdit/categories/blob/master/gmane/science/mathematics/categories/5477) to the CategoryTheory mailing list on Jan 5, 2010, with a [follow-up](https://github.com/punkdit/categories/blob/master/gmane/science/mathematics/categories/5487) on Jan 6.

Consider &#8224;-categories from the point of view of [[homotopy theory]].

Recall that the category [[Cat]] of [[small category|small categories]] naturally admits the [[model category]] structure called the [[folk model structure on Cat]].

The category of small &#8224;-categories $DCat$ also admits
a "natural" [[model category]] structure: 

* &#8224;-functor $f:A \to B$ is a weak equivalence iff it is 

  * [[full and faithful functor|full and faithful]];

  * and unitary surjective, meaning that every object of $B$ is unitary isomorphic to an object in the image of the functor $f$;

* the cofibrations and the trivial fibrations are as in [[folk model structure on Cat|Cat]];

* fibrations are the unitary isofibration: maps having the [[right lifting property]] for unitary isomorphisms.

The [[forgetful functor]] $DCat \to Cat$ is a [[right adjoint]]
but it is not a [[Quillen adjunction|right Quillen functor]] with respect to the natural model structures on these categories.

Moreover, a forgetful functor $XStruc \to Cat$ should reflect
weak equivalences in addition to preserving them.
The forgetful functor $DCat\to Cat$ preserves weak equivalences
but it does not reflect them. Because two objects in a &#8224;-category can be isomorphic without been unitary isomorphic.

In other words the forgetful functor $DCat\to Cat$ is wrong.
This may explains why a &#8224;-category cannot be
regarded as a category equipped a homotopy invariant structure, as discussed in more detail in the example sections of the entry _[[principle of equivalence]]_.


But the notion of &#8224;-category is perfectly reasonable
from an homotopy theoretic point of view. This is because the model category $DCat$ is a [[combinatorial model category]].
It follows, by a general result, that the notion of &#8224;-category is homotopy essentially algebraic.
There is a homotopy limit sketch whose category of models (in spaces) is [[Quillen equivalence|Quillen equivalent]] to the model category $DCat$. This is true also for the model category Cat.

### $\dagger$-simplicial set

> the following is based on a remark by [[Andre Joyal]], posted to the CategoryTheory mailing list on Jan 6, 2010

A &#8224;-[[simplicial set]] can be defined to be a simplicial set $X$ equipped with an involutive [[isomorphism]] $\dagger :X\to X^{op}$ which is the identity on 0-cells.
The category of &#8224;-simplicial sets (and dagger preserving maps)
is the category of [[presheaf|presheaves]] on the category whose objects are the ordinals $[n]$, but where the maps $[m]\to [n]$ are order reversing or preserving.

#### $\dagger$-Graphs

* [[dagger-graph]]

###  $(\infty,1)$-&#8224;-categories {##oo1Version}


> the following is based on a remark by [[Andre Joyal]], posted to the CategoryTheory mailing list on Jan 6, 2010


There should be a notion of &#8224;-[[quasi-category]] based on $\dagger$-simplicial sets as ordinary quasi-categories are based on ordinary simplicial sets.

(...)

## Properties

### Relation to anti-involutive monoids

The [[horizontal categorification]] of an [[anti-involution|anti-involutive]] [[monoid]] is a $\dagger$-category

### Relation to symmetric prosets

Every [[symmetric proset]] is a [[thin category|thin]] $\dagger$-category, and the [[groupoidal categorification]] of a symmetric proset is a $\dagger$-category, with the $\dagger$ operation being the groupoidal categorification of the symmetric property. 

### Relation to star-algebras

The [[category convolution algebra]] of a dagger category is naturally a [[star-algebra]]. The star-involution is given by [[pullback of functions]] along the $\dagger$-functor.


## Applications


### Quantum mechanics in terms of $\dagger$-compact categories

The [[finite-dimensional Hilbert spaces]] of interest in [[quantum information theory]] and [[quantum computation]] form $\dagger$-categories that are 
also [[compact closed categories]] ([[dagger compact categories]]), a fact that allow a [[string diagram]]-calculus for [[quantum mechanics in terms of †-compact categories]] which motivates much of the contemporary discussion of dagger-categories, starting with [Abramsky & Coecke 2004](#AbramskyCoecke04).

## Related concepts

* [[pseudograph]]

* [[star-category]], [[C-star-category]]

* [[dagger functor]]

* [[dagger category in homotopy type theory]]

* [[symmetric bicategory]]

\linebreak

[[!include oidification - table]]

\linebreak



## References
 {#References}

### General

Motivated by the example of [[finite-dimensional Hilbert spaces]], the concept of $\dagger$-categories appears in the form of *strongly compact closed categories* in

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], around Prop. 7.3 *A categorical semantics of quantum protocols*, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04), IEEE Computer Science Press (2004) &lbrack;[arXiv:quant-ph/0402130](http://arxiv.org/abs/quant-ph/0402130)&rbrack;

then named *[[dagger compact closed categories]]* in

* {#Selinger07} [[Peter Selinger]], *Dagger compact closed categories and completely positive maps*, Electronic Notes in Theoretical Computer Science **170** (2007) 139-163 &lbrack;[doi:10.1016/j.entcs.2006.12.018](https://doi.org/10.1016/j.entcs.2006.12.018), [web](http://www.mscs.dal.ca/~selinger/papers.html#dagger), [pdf](https://www.mscs.dal.ca/~selinger/papers/dagger.pdf)&rbrack;

and as such became the foundation of *[[quantum information theory via dagger-compact categories]]*.

Exposition in this context of [[quantum physics]]:

* [[John Baez]], *The $\star$-category of Hilbert spaces*, Section 3 in: *Quantum quandaries: a category-theoretic perspective*, in _Structural Foundations of Quantum Gravity_, Oxford U. Press (2006) 240-265 &lbrack;[web](http://math.ucr.edu/home/baez/quantum/node3.html), [arXiv:quant-ph/0404040](https://arxiv.org/abs/quant-ph/0404040)&rbrack;

and of [[quantum information theory via dagger-compact categories]]:

* {#HeunenVicary19} [[Chris Heunen]], [[Jamie Vicary]], §2.3 in: *Categories for Quantum Theory*, Oxford University Press 2019 &lbrack;[ISBN:9780198739616](https://global.oup.com/academic/product/categories-for-quantum-theory-9780198739616)&rbrack;

  based on:

  {#HeunenVicary12} [[Chris Heunen]], [[Jamie Vicary]], §2.3 in: *Lectures on categorical quantum mechanics* (2012) &lbrack;[pdf](https://www.cs.ox.ac.uk/files/4551/cqm-notes.pdf), [[HeunenVicary-QuantumLectures.pdf:file]]&rbrack;



But the notion of plain dagger categories has been considered much earlier, reinvented many times under different names (see [Karvonen 2018 §1.2](#Karvonen18) for more historical references) such as under the name "categories with involution":

* [[Saunders Mac Lane]], pp. 1045 of: *An Algebra of Additive Relations*, Proceedings of the National Academy of Sciences of the United States of America **47** 7 (1961) 1043-1051 &lbrack;[jstor:71127](https://www.jstor.org/stable/71127)&rbrack;

* [[Dieter Puppe]], §1 in *Korrespondenzen in abelschen Kategorien*, Mathematische Annalen **148** (1962) 1–30 &lbrack;[doi:10.1007/BF01438388](https://doi.org/10.1007/BF01438388)&rbrack;

* {#Burgin70} [[Mark S. Burgin]], *Categories with involution, and correspondences in $\gamma$-categories*, Trudy Moskovskogo Matematicheskogo Obshchestva **22** (1970) 161–228 &lbrack;[mathnet:mmo235](https://www.mathnet.ru/eng/mmo235)&rbrack;	

Vaguely related is the notion of "symmetric category" is (analogous to [[symmetric proset]] or [[symmetric bicategory]])

* {#Walters81} [[Robert Walters]], *Sheaves and Cauchy complete categories*, Cahiers Top. Geom. Diff. Cat. **22** 3 (1981) 283-286 &lbrack;[numdam:CTGDC_1981__22_3_283_0](http://www.numdam.org/item?id=CTGDC_1981__22_3_283_0)&rbrack;


Still, dedicated discussion of these notions only appears later under the name of dagger-categories:

* {#Karvonen18} [[Martti Karvonen]], *The Way of the Dagger*, Edinburgh (2018) &lbrack;[arXiv:1904.10805](https://arxiv.org/abs/1904.10805), [pdf](https://mysite.science.uottawa.ca/mkarvone/papers/Karvonen%20-%20Thesis.pdf)&rbrack;

concerning [[limits]]:

* [[Chris Heunen]], [[Martti Karvonen]], *Limits in dagger categories*, Theory and Applications of Categories **34** 18 (2019) 468-513 &lbrack;[arXiv:1803.06651](https://arxiv.org/abs/1803.06651), [34-18](http://www.tac.mta.ca/tac/volumes/34/18/34-18abs.html)&rbrack;

concerning [[monads]] (such as the [[Frobenius monad|Frobenius]] [[quantum reader monad]]):

* [[Chris Heunen]], [[Martti Karvonen]], *Monads on dagger categories*, Theory and Applications of Categories **31** 35 (2016) 1016-1043 &lbrack;[arXiv:1602.04324](https://arxiv.org/abs/1602.04324), [tac:31-35](http://www.tac.mta.ca/tac/volumes/31/35/31-35abs.html)&rbrack;

concerning abstract characterization:

* [[Luuk Stehouwer]], [[Jan Steinebrunner]], *Dagger categories via anti-involutions and positivity* &lbrack;[arXiv:2304.02928](https://arxiv.org/abs/2304.02928)&rbrack;



Certain specially nice $\dagger$-categories, such as [[C-star-category|$C^*$-categories]] and [[modular tensor categories]], play an important role in [[topological quantum field theory]] and the theory of [[quantum groups]], see the references there for more.

### Higher dagger categories
 {#ReferencesHigherDagger}

On dagger [[higher categories]]:

#### Dagger (∞,1)-categories

Three definitions of dagger [[(infinity,1)-categories|$(\infty,1)$-categories]] have been proposed by:  

* [[Simon Henry]], *$(n,1)$-dagger categories* &lbrack;[MO:a/427322](https://mathoverflow.net/a/427322/381)&rbrack;

On [[model category]]-presentations of dagger category [[internalization|objects]] in [[infinity-Grpd|$\infty Grpd$]] by involutive [[complete Segal spaces]] are discussed  (cf. the [erratum](#Bergner12Erratum)) in 

* [[Julia Bergner]]:

  *Adding inverses to diagrams encoding algebraic structures*, Homology, Homotopy and Applications **10** 2 (2008) 149-174 &lbrack;[doi:10.4310/HHA.2008.v10.n2.a8](https://dx.doi.org/10.4310/HHA.2008.v10.n2.a8), [arXiv:0610291](http://arxiv.org/abs/math/0610291)&rbrack;

  *Adding inverses to diagrams II: Invertible homotopy theories are spaces*, Homology, Homotopy and Applications **10** 2 (2008) 175-193 &lbrack;[doi:10.4310/HHA.2008.v10.n2.a9](https://dx.doi.org/10.4310/HHA.2008.v10.n2.a9), [arXiv:0710.2254](http://arxiv.org/abs/0710.2254)&rbrack;

  {#Bergner12Erratum} *Erratum to “Adding inverses to diagrams encoding algebraic structures” and “Adding inverses to diagrams II: Invertible homotopy theories are spaces”*, Homology, Homotopy and Applications **14** 1 (2012) 287-291 &lbrack;[doi:10.4310/HHA.2012.v14.n1.a15](https://dx.doi.org/10.4310/HHA.2012.v14.n1.a15), [arXiv:0710.2254 pp 18](https://arxiv.org/pdf/0710.2254#page=18)&rbrack;
  

#### Dagger (∞,n)-categories

Generalization to dagger [[(infinity,n)-categories|$(\infty,n)$-categories]]:

* [[Theo Johnson-Freyd]], *Dagger Higher Categories*, workshop (2023) &lbrack;[web](http://categorified.net/dagger2023.html)&rbrack;

* [[Theo Johnson-Freyd]], *Higher Dagger Categories*, [talk at](Center+for+Quantum+and+Topological+Systems#JohnsonFreydNov2023) [[CQTS]] (08 Nov 2023) &lbrack;slides:[pdf](http://categorified.net/NYUADtalk.pdf), [[JohnsonFreyd-HigherDaggerNYUAD.pdf:file]], video:[YT](https://youtu.be/zvtziTpl2T0)&rbrack;

* [[Giovanni Ferrer]], [[Brett Hungar]], [[Theo Johnson-Freyd]], [[Cameron Krulewski]], [[Lukas Müller]], [[Nivedita]], [[David Penneys]], [[David Reutter]], [[Claudia Scheimbauer]], [[Luuk Stehouwer]], [[Chetan Vuppulury]], *Dagger n-categories* &lbrack;[arXiv2403.01651](https://arxiv.org/abs/2403.01651)&rbrack;


[[!redirects dagger-category]]
[[!redirects dagger-categories]]
[[!redirects dagger categories]]
[[!redirects †-category]]
[[!redirects †-categories]]

[[!redirects symmetric category]]
[[!redirects symmetric categories]]

[[!redirects category with involution]]
[[!redirects categories with involution]]
[[!redirects categories with involutions]]

[[!redirects dagger higher category]]
[[!redirects dagger higher categories]]

[[!redirects higher dagger category]]
[[!redirects higher dagger categories]]

[[!redirects dagger n-category]]
[[!redirects dagger n-categories]]

