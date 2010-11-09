# $\dagger$-categories
* tic
{: toc}


## Idea

The definition of a [[category]] effectively enforces an ordering on the "0-faces" -- the source and target [[object]]s -- of every 1-cell (every [[morphism]]). In many cases this is essential, in that there is no way to regard the generic morphism $a \stackrel{f}{\to} b$ in the category as a morphism from $b$ to $a$ instead.

But there are many categories for which this is not the case, where every morphism naturally only comes with the information of an unordered pair $\{a,b \}$ of objects, without any prejudice on which is to be regarded as source and which as target. An important general example is:

* the category $Spans(C)$ of [[span|spans]] in a category $C$ with pullbacks, or [[duality|dually]], the category $CoSpans(C)$ of [[cospan|cospans]] in a category $C$ with pushouts.

More concrete examples are:

* categories of [[cobordism]]s (but notice that cobordisms are naturally regarded as [[cospan]]s which makes this a special case of the above example);

* the category [[Hilb]] of Hilbert spaces, where for every linear map $f : H_1 \to H_2$ we also have the adjoint map (in the sense of Hilbert spaces, not in the categorical sense) $f^\dagger : H_2 \to H_1$ (but notice that according to [[groupoidification]] this is also essentially to be regarded as a special case of categories of spans).

A _dagger structure_ on a category is extra structure which encodes the idea of _removing_ the ordering information on the 0-faces of 1-cells in a category: it is is a contravariant functor which sends every morphism $f : a \to b$ to a morphims going the other way, $f^\dagger : b \to a$.

The notation and terminology here is motivated from the example [[Hilb]] of Hilbert spaces, where $f^\dagger$ is traditionally the notion for the adjoint of a linear map $f$.  The canonical &#8224;-structure on [[Hilb]] and on [[nCob]] is crucial in [[FQFT|quantum field theory]] where it is used to encode the idea of **unitarity**:

a _unitary_ [[FQFT|functorial QFT]] of dimension $n$ is supposed to be a functor $n Cob \to Hilb$ which respects the &#8224;-structure on both sides.

## Definition

### Dagger categories

A **dagger category**, or &#8224;-category, is a [[category]] $C$ equipped with a contravariant functor
$$
  \dagger : C \to C
$$
which is the identity on objects, and which satisfies $\dagger \circ \dagger = \mathrm{id}_C$.

Note that regarded as an extra structure on categories, a &#8224;-structure is [[evil]], since it imposes equations on objects.


### Special morphisms

+-- {: .un_defn}
###### Definition

A morphism $f$ in a &#8224;-category is called **[[unitary morphism]]** if its &#8224;-adjoint equals its [[inverse]]:

$$
  f^\dagger = f^{-1}
  \,.
$$

=--


For the purpose of considering what makes two objects of a $\dagger$-category [[equivalence|equivalent]], one should not consider all [[isomorphism]]s (invertible morphisms) but rather all unitary isomorphisms.

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

A morphism $F : (C, \dagger) \to (D, \ddagger)$ of &#8224;-categories -- a **&#8224;-functor** -- is a [[functor]] $F : C \to D$ of the underlying categories, which commutes with the &#8224;-structures in that

$$
  F \circ \dagger = \ddagger \circ F
  \,.
$$

A [[natural transformation]] between &#8224;-functors is just a natural transformation of the underlying functors. 

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


+-- {: .un_def}
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

Keeping $d_1$ and $d_2$ fixed, respectively this makes $F(-,d_1), F(-,d_2) : C \to E$ &#8224;-functors. We see from the diagrams that $F(-,(d_1 \stackrel{g}{\to}) d_2)$ is a natural transformation between these &#8224;-functors, and the fact that $F$ intertwines the dagger operation of $D$ with that of $E$ means $F$ regarded as a functor $D \to [C,E]$ intertwines the &#8224;-structures of $D$ and $[D,E]_{dag}$, by the above definition.

=--

## Terminology and wording

In Wikipedia [dagger category](http://en.wikipedia.org/wiki/Dagger_category) is said to be the same as _involutive category_ or _category with involution_, but [Springer's Encyclopedy](http://eom.springer.de/C/c020780.htm) requires for a category with involution additional conditions namely a partial order on the set of morphisms and that the order is compatible with the composition of morphisms.


## Examples

* The category [[Rel]] of sets and [[relations]] is a &#8224;-category, taking dagger as relational converse.

* More generally, let $C$ be a category with [[pullbacks]] and let $Span_1(C)$ be the 1-category of [[spans]] up to isomorphism: its morphisms are spans with one leg labeled as source, the other labeled as target. Then the functor $\dagger : Span_1(C)^{op} \to Span_1(C)$ which just exchanges this labeling is a &#8224;-structure on $Span_1(C)$.

* $\mathcal{R}(G)$, the category of unitary [[representation]]s of a (discrete) [[group]] $G$ and intertwining maps, is a &#8224;-category. For an intertwiner $\phi : R \rightarrow S$, let $\phi^\dagger : S \rightarrow R$ be the adjoint of $\phi$ in [[Hilb]].



## Variants


### Model structure on &#8224;-categories {#ModelStructure}

> the following is based on a remark by [[Andre Joyal]], posted to the CategoryTheory mailing list on Jan 6, 2010

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
regarded as a category equipped a homotopy invariant structure, as discussed in more detail in the example sections of the entry [[evil]].


But the notion of &#8224;-category is perfectly reasonable
from an homotopy theoretic point of view. This is because the model category $DCat$ is a [[combinatorial model category]].
It follows, by a general result, that the notion of
of &#8224;-category is homotopy essentially algebraic
There a homotopy limit sketch whose category of models (in spaces)
is [[Quillen equivalence|Quillen equivalent]] to the model category $DCat$. This is true also for the model category Cat.

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




## Applications


### Quantum mechanics in terms of $\dagger$-compact categories

Large parts of [[quantum mechanics]] and [[quantum computation]] are naturally formulated as the theory of $\dagger$-categories that are 
also [[compact closed categories]] in a compatible way -- [[dagger compact categories]].

For more on this see 

* [[quantum mechanics in terms of †-compact categories]].


## References

The concept of $\dagger$-category is discussed here:

* [[Samson Abramsky|S. Abramsky]] and [[Bob Coecke|B. Coecke]], A categorical semantics of quantum protocols, _Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04)_, IEEE Computer Science Press (2004).  [arXiv](http://arxiv.org/abs/quant-ph/0402130)

and further abstracted in:

* [[Peter Selinger|P. Selinger]], Dagger compact closed categories and completely positive maps, _Proceedings of the 3rd International Workshop on Quantum Programming Languages_, Chicago, June 30&#8211;July 1, 2005. [web](http://www.mscs.dal.ca/~selinger/papers.html#dagger)

The importance of $\dagger$-categories in quantum theory is discussed here:

* [[John Baez]], Quantum quandaries: a category-theoretic perspective, in _Structural Foundations of Quantum Gravity_, eds. Steven French, Dean Rickles and Juha Saatsi, Oxford U. Press, 2006, pp. 240--265.  See especially Section 3: The $\star$-category of Hilbert spaces.  ([web](http://math.ucr.edu/home/baez/quantum/node3.html))

Note that in older literature, the term "$\star$-category"  or "star-category" is sometimes used instead of $\dagger$-category.

Certain specially nice $\dagger$-categories, such as $C^*$-categories and [[modular tensor category|modular tensor categories]], play an important role in topological quantum field theory and the theory of quantum groups:

* J&#252;rg Fr&#246;hlich and Thomas Kerler, _Quantum Groups, Quantum Categories, and Quantum Field Theory_, Springer Lecture Notes in Mathematics 1542, Springer-Verlag, Berlin, 1991. 

* Bojko Bakalov and Alexander Kirillov, Jr., _Lectures on Tensor Categories and Modular Functors_, American Mathematical Society, Providence, Rhode Island, 2001.
([web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html))


[[!redirects dagger-categories]]
[[!redirects dagger category]]
[[!redirects dagger categories]]
[[!redirects †-category]]
[[!redirects †-categories]]