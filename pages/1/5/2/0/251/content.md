#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

A **double category** $D$ is an [[internal category]] in [[Cat]].   Similarly, a **double groupoid** is an internal [[groupoid]] in [[Grpd]].

However, these definitions obscure the essential symmetry of the concepts.  We think of a double category $D_1 \rightrightarrows D_0$ as having

* *objects*: the objects  of $D_0$
* *vertical arrows*: the morphisms of $D_0$
* *horizontal arrows*: the objects of $D_1$
* *squares* or *2-cells*: the morphisms of $D_1$.

We may picture a 2-cell in a double category as a square:

$$
  \array{
    x_0 
    &\stackrel{f}{\to} &
    x_1  
    \\
    {}^\mathllap{\alpha_0}\downarrow
    &\Downarrow^{\mathrlap{\phi}}&
    \downarrow^{\mathrlap{\alpha_1}}
    \\
    y_0  
    &\underset{g}{\to} &
    y_1 
  }
  
$$

Here $x_i,y_i$ are objects, $f$ and $g$ are horizontal arrows, $\alpha_i$ are vertical arrows and $\phi$ is the 2-cell itself.  This makes it clear why $\phi$ is called a 'square'.

The vertical and horizontal arrows form categories (called **edge categories**), and the squares have two category structures which respect the edge category structures.  

Horizontal composition of these squares is given by the compositon in the ordinary [[category|categories]] $D_0$ and $D_1$, while vertical composition is given by the composition operation specified on $D_1 \stackrel{\to}{\to} D_0$ by virtue of it being a [[category]] [[internalization|internal to]] [[Cat]].

In particular, the **transpose** of a double category, which switches the vertical and horizontal arrows, is again a double category.

A double category is an important special case of an [[n-fold category]], namely the case where $n = 2$.

## Examples ##

* If $C$ is a 2-category, we have a double category $Sq(C)$ whose objects are those of $C$, both of whose types of morphisms are the morphisms in $C$, and whose squares are 2-cells in $C$ with their source and target both decomposed as a composite of two morphisms.  (These squares are sometimes called *quintets* $(\alpha,f,g,h,k)$ where $\alpha\colon f g \to h k$.)

  (In this example, the two edge categories coincide.  Double categories with this property are called **edge-symmetric**.)

* Since any 1-category can be regarded as a 2-category with only identity 2-cells, for any 1-category $C$ we have a double category $Sq(C)$ whose squares are the commutative squares in $C$.  

* Any 2-category can also be made into a double category in two more ways, by defining the vertical or horizontal morphisms to consist only of identities.  In this way 2-categories can be considered as a special case of double categories.

  In the other direction, any double category has two underlying 2-categories, consisting of the objects, the vertical (resp. horizontal) arrows, and the squares whose horizontal-arrow (resp. vertical-arrow) source and target are identities.  We call these its **vertical 2-category** and **horizontal 2-category**.

* Finally, we can also make a 2-category $C$ into a double category with the same objects, whose horizontal arrows are the morphisms of $C$, whose vertical arrows are the [[adjunctions]] in $C$, and whose 2-cells are [[mate]]-pairs of 2-cells in $C$.  Naturality properties of the mate correspondence are concisely expressed by the existence of this double category.

* There is a double category $Prof$ whose objects are (small) categories, whose vertical arrows are functors, whose horizontal arrows are [[profunctors]], and whose squares are natural transformations.  This double category is in fact an [[equipment]], as are many other similar ones (such as for [[enriched categories]]).

* Any topological space has a "homotopy double groupoid" whose objects are points, whose morphisms of both types are paths (so it is edge-symmetric), and whose 2-cells are homotopies.

* There is a double category $MonCat$ whose objects are [[monoidal categories]], whose horizontal arrows are [[lax monoidal functor]]s, whose vertical arrows are [[colax monoidal functor]]s, and whose 2-cells are generalized [[monoidal natural transformation]]s.  An analogous double category can be constructed involving the algebras for any [[2-monad]].

* There is a double category $Model$ whose objects are [[model categories]], whose horizontal arrows are right [[Quillen functor]]s, whose vertical arrows are left Quillen functors, and whose 2-cells are arbitrary natural transformations.  Passage to [[derived functors]] is a functor on this double category.


## Weakenings ##

An internal category in the 1-category $Cat$ might more properly be called a *strict* double category, since all its composition operations are strictly associative and unital.  Since a double category is a 2-dimensional structure, it makes sense to allow these compositions to be weak as well.

### Pseudo double categories

A **pseudo double category** is a weakly internal category in the 2-category $Cat$.  Here "weakly internal category" in a 2-category is interpreted as being associative and unital up to coherent isomorphism, just as a [[bicategory]] is a "weakly enriched category."  This makes the composition in one direction weak, but the composition in the other direction remains strict (it is the composition in the objects of $Cat$ that make up the pseudo double category).  Many naturally occurring examples, such as $Prof$, are pseudo double categories.  

Luckily, every pseudo double category is equivalent to a double category of the usual sort, where composition of arrows in both directions is strictly associative.  This is Theorem 7.5 of Grandis and Par&#233;'s paper [Limits in double categories](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1999__40_3/CTGDC_1999__40_3_162_0/CTGDC_1999__40_3_162_0.pdf).

### Double bicategories

One way to define a double category which is "weak in both directions" is a [[double bicategory]].   Double bicategories were defined in Dominic Verity's thesis, which unfortunately is unpublished and not available in electronic form.  However, the definition can be found in Jeffrey Morton's paper [Double bicategories and double cospans](http://arxiv.org/abs/math/0611930).

The definition of double bicategory takes as given two ordinary [[bicategories]], representing the vertical and horizontal bicategories, together with a set of squares which is "acted on" by both of these.  In the basic definition, there is no requirement that the 2-cells in the vertical (resp. horizontal) bicategory be exactly those squares whose vertical (resp. horizontal) 1-cell boundaries are identities, but such an axiom can easily be added.

The reason for stipulating the vertical and horizontal bicategories as a basic part of the structure is that if identities are strict in neither direction, then the vertically (resp. horizontally) "globular" 2-cells (those whose vertical or horizontal boundaries are identities) can't seemingly be composed vertically (resp. horizontally), so it's hard to state coherence axioms for the associativity and unit constraints.

### Strictly unital weak double categories

Another way around this difficulty is to require the *units* to be strict, but not the associativity.  This is not such a terrible thing, since units can usually be strictified much more easily than associativity.  Thus, in this approach we assume as given

* a set of objects,
* two sets of vertical and horizontal arrows, equipped with identities and strictly unital (but not associative) composition operations,
* a set of squares, equipped with identities and strictly unital composition in both directions, and
* two sets of associativity squares, one with identity vertical boundary and one with identity horizontal boundary, satisfying the usual axioms, which are possible to state since identities are strict.

### Cubical bicategories

Yet another approach to doubly-weak double categories was proposed by [[Richard Garner]] in an email to the categories list on 5 Mar 2010, in response to a query of [[Ronnie Brown]].  This approach avoids the coherence problems by being completely "unbiased."

> A **cubical bicategory** is given by sets of objects, of vertical arrows, of horizontal arrows and of squares, satisfying the obvious source and target criteria, together with operations of identity and binary composition for vertical and horizontal arrows, satisfying no laws at all; and finally, for every $n \times m$ grid of squares (where possibly $n$ or $m$ are zero), and every way of composing up the horizontal and vertical boundaries using the nullary and binary compositions, a composite square with those boundaries. The coherence axioms which this structure must satisfy say that any two ways of composing up a diagram of squares must give the same answer.

He then commented:

> I would be very interested to know if anyone can extract from this definition a finite collection of composition operations on squares, and a finite collection of equations between them, which together generate all the others. The key obstable seems to be problem that identity 1-cells are not strict in either direction.

## Unbiased composition and associativity

It is natural to ask what the "unbiased" notion of composition and associativity is for squares in a double category.  The natural thing to take as input for an "unbiased composition" is a dissection of a rectangle into smaller rectangles, the smaller rectangles representing squares that we want to "compose up" in a double category.  As usual, we can try to build up such a composite by means of the "biased" binary composites that are given in the definition of double category.

It can be shown that if a given such dissection can be composed up in *some* way using binary composites, then any two ways to compose it up must give the same result.  See

* Dawson and Par&#233;, "General associativity and general composition for double categories".
* Also of interest is "Characterizing tileorders" by the same authors, in which they characterize such rectangle-dissections in more purely combinatorial terms.

However, there are dissections which admit *no* composition in a general double category, foremost among which is the "pinwheel:"

[[double-category-pinwheel.png:pic]]

It is shown in the paper

* Dawson, "A forbidden-suborder characterization of binarily-composable diagrams in double categories"

that this is the "only obstacle," in the same sense that $K_5$ and $K_{3,3}$ are the only obstacles to [[planar graph|planarity]] of a [[graph]].  Namely, any diagram in which pinwheels can be avoided, can be composed.

In some double categories, however, even pinwheels can be composed, due to certain factorization properties of squares.  These properties are investigated in the above papers as well.


## Related pages

* [[2-category equipped with proarrows]]

* [[double profunctor]]

* [[framed bicategory]]


## References ##

* [[The Catsters]], Double Categories ([YouTube](http://www.youtube.com/watch?v=kiCZiSA2W3Q&feature=channel_page)).

* Tom Fiore, [Double categories and pseudo algebras](http://www.math.uchicago.edu/~fiore/1/fiorefolding.pdf). 

* Marco Grandis and Robert Par&#233;, [Limits in double categories](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1999__40_3), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **40** (1999), 162--220.

* Marco Grandis and Robert Par&#233;, [Adjoints for double categories](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_2004__45_3), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **45** (2004), 193--240.

* Jeffrey C. Morton, [Double bicategories and double cospans](http://arxiv.org/abs/math/0611930).

* [[Ronnie Brown]] and C.B. Spencer, [Double groupoids and crossed modules](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1976__17_4_343_0), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **17** (1976), 343--362.


[[!redirects double categories]]
[[!redirects double groupoid]]
[[!redirects double groupoids]]
[[!redirects vertical 2-category]]
[[!redirects horizontal 2-category]]
[[!redirects pseudo double category]]
[[!redirects pseudo double categories]]
