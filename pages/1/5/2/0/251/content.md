[[+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

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
  \begin{matrix}
    x_0 
    &\stackrel{f}{\to} &
    x_1  
    \\
    {}^{\mathllap{\alpha_0}}\downarrow
    &\Downarrow^{\mathrlap{\phi}}&
    \downarrow^{\mathrlap{\alpha_1}}
    \\
    y_0  
    &\underset{g}{\to} &
    y_1 
 \end{matrix}  
$$

Here $x_i,y_i$ are objects, $f$ and $g$ are horizontal arrows, $\alpha_i$ are vertical arrows and $\phi$ is the 2-cell itself.  This makes it clear why $\phi$ is called a 'square'.

The vertical and horizontal arrows form categories (called **edge categories**), and the squares have two category structures which respect the edge category structures.  

Horizontal composition of these squares is given by the compositon in the ordinary [[category|categories]] $D_0$ and $D_1$, while vertical composition is given by the composition operation specified on $D_1 \stackrel{\to}{\to} D_0$ by virtue of it being a [[category]] [[internalization|internal to]] [[Cat]].

In particular, the **transpose** of a double category, which switches the vertical and horizontal arrows, is again a double category.

A double category is an important special case of an [[n-fold category]], namely the case where $n = 2$. There is more on $n$-fold categories in the paper by Brown and Higgins referenced below. 

## Examples ##

* If $C$ is a [[2-category]], we have a double category $Sq(C)$ whose objects are those of $C$, both of whose types of morphisms are the morphisms in $C$, and whose squares are 2-cells in $C$ with their source and target both decomposed as a composite of two morphisms.  (These squares are sometimes called *quintets* $(\alpha,f,g,h,k)$ where $\alpha\colon f g \to h k$.)

  (In this example, the two edge categories coincide.  Double categories with this property are called **edge-symmetric**.)

* Since any 1-category can be regarded as a 2-category with only identity 2-cells, for any 1-category $C$ we have a double category $Sq(C)$ whose squares are the commutative squares in $C$.  We can also restrict the commutative squares considered, such as taking only [[pullback]] squares.

* Any 2-category can also be made into a double category in two more ways, by defining the vertical or horizontal morphisms to consist only of identities.  In this way 2-categories can be considered as a special case of double categories.

  In the other direction, any double category has two underlying 2-categories, consisting of the objects, the vertical (resp. horizontal) arrows, and the squares whose horizontal-arrow (resp. vertical-arrow) source and target are identities.  We call these its **vertical 2-category** and **horizontal 2-category**.

* Finally, we can also make a 2-category $C$ into a double category with the same objects, whose horizontal arrows are the morphisms of $C$, whose vertical arrows are the [[adjunctions]] in $C$, and whose 2-cells are [[mate]]-pairs of 2-cells in $C$.  Naturality properties of the mate correspondence are concisely expressed by the existence of this double category.

* There is a double category $Prof$ whose objects are (small) categories, whose vertical arrows are functors, whose horizontal arrows are [[profunctors]], and whose squares are natural transformations.  This double category is in fact an [[equipment]], as are many other similar ones (such as for [[enriched categories]]).

* Any topological space has a "homotopy double groupoid" whose objects are points, whose morphisms of both types are paths (so it is edge-symmetric), and whose 2-cells are homotopies.

* There is a double category $MonCat$ whose objects are [[monoidal categories]], whose horizontal arrows are [[lax monoidal functor]]s, whose vertical arrows are [[colax monoidal functor]]s, and whose 2-cells are generalized [[monoidal natural transformation]]s.  An analogous double category can be constructed involving the algebras for any [[2-monad]].

* There is a double category $Model$ whose objects are [[model categories]], whose horizontal arrows are right [[Quillen functor]]s, whose vertical arrows are left Quillen functors, and whose 2-cells are arbitrary natural transformations.  Passage to [[derived functors]] is a functor on this double category.  More generally, we can define a double category of [[homotopical categories]] and "left derivable" and "right derivable" functors.


## Weakenings ##

An internal category in the 1-category $Cat$ might more properly be called a *strict* double category, since all its composition operations are strictly associative and unital.  Since a double category is a 2-dimensional structure, it makes sense to allow these compositions to be weak as well.

### Pseudo double categories

A **pseudo double category** is a weakly internal category in the 2-category $Cat$.  Here "weakly internal category" in a 2-category is interpreted as being associative and unital up to coherent isomorphism, just as a [[bicategory]] is a "weakly enriched category."  This makes the composition in one direction weak, but the composition in the other direction remains strict (it is the composition in the objects of $Cat$ that make up the pseudo double category).  Many naturally occurring examples, such as $Prof$, are pseudo double categories.  

Luckily, every pseudo double category is equivalent to a double category of the usual sort, where composition of arrows in both directions is strictly associative.  This is Theorem 7.5 of Grandis and Par&#233;'s paper [Limits in double categories](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1999__40_3/CTGDC_1999__40_3_162_0/CTGDC_1999__40_3_162_0.pdf).

### Double bicategories

One way to define a double category which is "weak in both directions" is a [[double bicategory]].  Double bicategories were defined in [[Dominic Verity]]'s thesis. The definition can also be found in Jeffrey Morton's paper [Double bicategories and double cospans](http://arxiv.org/abs/math/0611930).

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

It also seems that a "cubical bicategory" in this sense need not have underlying horizontal or vertical bicategories, for the same reason.  This presents something of an obstacle to practical applications.


## Unbiased composition and associativity {#Unbiased}

It is natural to ask what the "unbiased" notion of composition and associativity is for squares in a double category.  The natural thing to take as input for an "unbiased composition" is a dissection of a rectangle into smaller rectangles, the smaller rectangles representing squares that we want to "compose up" in a double category.  As usual, we can try to build up such a composite by means of the "biased" binary composites that are given in the definition of double category.

It can be shown that if a given such dissection can be composed up in *some* way using binary composites, then any two ways to compose it up must give the same result.  See

* Dawson and Par&#233;, _General associativity and general composition for double categories_ , [link](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1993__34_1_57_0)


Also of interest is "Characterizing tileorders" by the same authors, in which they characterize such rectangle-dissections, called [[tileorders]], in purely combinatorial terms.

However, there are dissections which admit *no* composition in a general double category, foremost among which is the "pinwheel:"

[[double-category-pinwheel.png:pic]]

It is shown in the paper

* Dawson, _A forbidden-suborder characterization of binarily-composable diagrams in double categories_ , [TAC](http://www.tac.mta.ca/tac/volumes/1995/n7/1-07abs.html)

that this is the _only obstacle_ in the same sense that $K_5$ and $K_{3,3}$ are the only obstacles to [[planar graph|planarity]] of a [[graph]].  Namely, if a diagram is not composable in a double category, then every "attempt" to compose it by a sequence of binary compositions will eventually result in a diagram which "contains" a pinwheel in a suitable sense (specifically, as a sub-[[tileorder]]).

In many double categories, however, arbitrary arrangements of squares, even pinwheels, can be composed.  By this we mean that given a pinwheel diagram in such a double category (for example), there is a natural square with the same boundary which it makes sense to regard as "the composite" of that pinwheel.  For example:

* In the double category $Sq(C)$ of squares/quintets in a 2-category, the general pasting theorem for 2-categories shows that any arrangement of squares can be composed.  In particular, this applies to commutative squares in a 1-category.  The same is true for double categories of adjunctions.

* If all the squares in a pinwheel are pullback squares in a 1-category, so is the whole thing.  The same is true for more general arrangements in a double category of pullback squares.

* Arbitrary arrangements can also be composed in $Model$ and its variants, again by the pasting theorem for 2-categories, since its 2-cells are just ordinary natural transformations.

* Pinwheels and more general arrangements can also be composed in the double category $MonCat$, along with its relatives $T Alg$.  The proof of this is not quite as trivial, but fairly straightforward.

* In any [[fibrant double category]], all arrangements can be composed.

This last example is due to a factorization property: if we can factor the two long vertical rectangles in the pinwheel into two squares, then we can compose it.  The cartesian cells in a fibrant double category certainly allow such a factorization.  One can also axiomatize more precisely what factorization properties are necessary; this is done in the above paper of Dawson and Par&#233;.

In fact, it seems hard to find a naturally occurring double category in which pinwheels and more general arranguments *cannot* be composed, although such composability definitely does not follow from the double-category axioms.  This suggests that perhaps the usual definition of double category is too naive, and we should actually require all "unbiased" composites to exist, including the pinwheel.  There is probably a monad of some sort on a suitable category whose algebras are "double categories with generalized composites" in this sense.

(It is tempting to try to axiomatize such a structure finitely by adding a basic "pinwheel-composition" operation, but although every non-composable arrangement reduces to one "containing" a pinwheel, the containment is not necessarily of a sort to which such an operation could be applied.  So it is not clear whether there is any finitary axiomatization of such "augmented" double categories.)


## Higher categories of double categories

There are notions of [[double functor|functor]] and of [[vertical transformation|transformation]] between double categories, which make them into a [[2-category]].  In fact, due to the vertical-horizontal symmetry, there are two such 2-categories, depending on the direction we choose the transformations to go in.  Moreover, we can also take the functors to be strict, pseudo, lax, or colax in either direction, so there are many possible 2-categories of double categories (although for some choices one has to worry about compatibility).

Probably the most useful such 2-categories are where we choose one direction to be the "arrow" direction and the other the "proarrow" direction, we take functors which are lax, colax, or pseudo in the proarrow direction and strict in the arrow direction, and transformations that go in the arrow direction.  This is natural when considering double categories such as [[proarrow equipments]].  If we allow the functors and transformations to be only pseudo in the arrow direction as well, and add in [[modifications]] in the arrow direction, we obtain a [[3-category]] instead.  In some situations, such as the study of [[generalized multicategories]], this 3-category is a natural place in which to work (or an enlargement of it to include [[virtual equipments]] as well).

We can also combine the horizontally lax and colax functors, together with a general notion of vertical transformation, into a large double category of double categories.  This is a special case of the double category of $T$-algebras for a particular 2-monad $T$, mentioned above.

In some contexts, a natural observation is that the 1-category $DblCat$ is [[cartesian closed category|cartesian closed]], and thus enriched over itself--thus it forms a "locally-double" category, i.e. a category enriched over double categories.  This can be regaded as a structure like a [[3-category]], except that it has two different kinds of 2-cells (in this case, the vertical and horizontal transformations).

In any of these higher categories, we can apply the notions and methods of higher category theory.  For instance, we automatically obtain a notion of [[monoidal double category]], namely a [[pseudomonoid]] in $DblCat$.  Likewise we have *cartesian double categories*, which are [[cartesian objects]] in $DblCat$.  If the double category in question is [[fibrant double category|fibrant]], then monoidal structures can be lifted to the horizontal bicategory; many naturally occurring [[cartesian bicategories]] can be obtained in this way.

Finally, if we want to discuss [[weighted limits]] and colimits in double categories, or construct [[generalized multicategories]] based on double categories, we may want to [[2-category equipped with proarrows|equip DblCat with proarrows]].  There is a notion of [[double profunctor]], but they do not compose associatively, and hence do not form a proarrow equipment in the usual sense; but they do form a [[virtual equipment]], which is sufficient for many purposes.


## Related pages

* [[2-category equipped with proarrows]], [[framed bicategory]]

* [[double functor]], [[vertical transformation]], [[horizontal transformation]]

* [[double profunctor]]


## References ##

* [[The Catsters]], Double Categories ([YouTube](http://www.youtube.com/watch?v=kiCZiSA2W3Q&feature=channel_page)).

* Tom Fiore, [Double categories and pseudo algebras](http://www.math.uchicago.edu/~fiore/1/fiorefolding.pdf). 

* Marco Grandis and Robert Par&#233;, [Limits in double categories](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1999__40_3), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **40** (1999), 162--220.

* Marco Grandis and Robert Par&#233;, [Adjoints for double categories](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_2004__45_3), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **45** (2004), 193--240.

* Jeffrey C. Morton, [Double bicategories and double cospans](http://arxiv.org/abs/math/0611930).

* [[Ronnie Brown]] and C.B. Spencer, [Double groupoids and crossed modules](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1976__17_4_343_0), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **17** (1976), 343--362.

* [[Ronnie Brown]]  and [[P.J. Higgins]], [The equivalence of $\infty$-groupoids
and crossed  complexes,](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_371_0/CTGDC_1981__22_4_371_0.pdf})  _Cah. Top. G&#233;om. Diff_. 22 (1981) 371-386.

* [[Mike Shulman]], [Comparing composites of left and right derived functors](http://nyjm.albany.edu/j/2011/17-5v.pdf),_New York J. Math._ **17** (2011) 75--125. [arXiv:0706.2868](http://arxiv.org/abs/0706.2868)


[[!redirects double categories]]
[[!redirects double groupoid]]
[[!redirects double groupoids]]
[[!redirects vertical 2-category]]
[[!redirects horizontal 2-category]]
[[!redirects pseudo double category]]
[[!redirects pseudo double categories]]