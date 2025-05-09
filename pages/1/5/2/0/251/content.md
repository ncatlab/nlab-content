+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}


## Definition ##

A **double category** $D$ is an [[internal category]] in [[Cat]].   Similarly, a **double groupoid** is an internal [[groupoid]] in [[Grpd]].

However, these definitions obscure the essential symmetry of the concepts.  We think of a double category $D_1 \stackrel{\to}{\to} D_0$ as having

* *[[objects]]*: the objects  of $D_0$
* *[[vertical morphisms]]*: the morphisms of $D_0$
* *[[horizontal morphisms]]*: the objects of $D_1$
* *[[2-morphisms]]* or *squares* or *2-cells*: the morphisms of $D_1$.

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

Alternatively one can apply [[Poincaré duality]] to obtain a [[string diagram]] representation for 2-cells, similar to the one obtained for [[2-category|2-categories]] ([Myers 16](#Myers16)):

\begin{centre}
    \begin{tikzpicture}[scale=2]
        \usetikzlibrary{positioning,calc,decorations.pathmorphing,decorations.pathreplacing,decorations.markings,patterns}

        \tikzset{fwd/.style={decoration={markings,mark=at position 0.7 with {\arrow{>}}},postaction={decorate}}}
        \tikzset{bwd/.style={decoration={markings,mark=at position 0.5 with {\arrow{<}}},postaction={decorate}}}

        \path[fill={rgb,255:red,212; green,166; blue,204}] (0,0) rectangle (.5,.5);
        \path[fill={rgb,255:red,152; green,209; blue,162}] (.5,0) rectangle (1,.5);
        \path[fill={rgb,255:red,248; green,168; blue,156}] (0,.5) rectangle (.5,1);
        \path[fill={rgb,255:red,243; green,237; blue,155}] (.5,.5) rectangle (1,1);
        \draw[gray] (0,0) rectangle (1,1);
        \node[circle,draw,inner sep=1.5pt,fill=white] at (.5,.5) (alpha) {$\phi$};
        \draw[fwd] (0,.5) -- (alpha);
        \draw[fwd] (alpha) -- (1,.5);
        \draw[bwd] (.5,0) -- (alpha);
        \draw[bwd] (alpha) -- (.5,1);
        \node at (-.2,.5) {$\alpha_0$};
        \node at (1.2,.5) {$\alpha_1$};
        \node at (.5,1.2) {$f$};
        \node at (.5,-.2) {$g$};
        \node at (.25,.75) {$x_0$};
        \node at (.75,.75) {$x_1$};
        \node at (.25,.25) {$y_0$};
        \node at (.75,.25) {$y_1$};
    \end{tikzpicture}
\end{centre}

The vertical and horizontal arrows form categories (called **edge categories**), and the squares have two category structures which respect the edge category structures.  

Vertical composition is given by the composition in the ordinary [[category|categories]] $D_0$ and $D_1$, while horizontal composition is given by the composition operation specified on $D_1 \stackrel{\to}{\to} D_0$ by virtue of it being a [[category]] [[internalization|internal to]] [[Cat]].

In particular, the **transpose** of a double category, which switches the vertical and horizontal arrows, is again a double category.

A double category is an important special case of an [[n-fold category]], namely the case where $n = 2$. There is more on $n$-fold categories in the paper by Brown and Higgins referenced below. 

## Examples ##

* If $C$ is a [[2-category]], there is its _[[double category of squares]]_ $Sq(C)$ whose objects are those of $C$, both of whose types of morphisms are the morphisms in $C$, and whose squares are [[2-morphisms]] in $C$ with their source and target both decomposed as a composite of two morphisms.  (These squares are sometimes called *quintets* $(\alpha,f,g,h,k)$ where $\alpha\colon f g \to h k$, and so this double category is said to be a [[quintet construction]].)

  (In this example, the two edge categories coincide.  Double categories with this property are called **edge-symmetric**.)

* Since any 1-category can be regarded as a 2-category with only identity 2-cells, for any 1-category $C$ we have a double category $Sq(C)$ whose squares are the commutative squares in $C$.  We can also restrict the commutative squares considered, such as taking only [[pullback]] squares.

* Any 2-category can also be made into a double category in two more ways, by defining the vertical or horizontal morphisms to consist only of identities.  In this way 2-categories can be considered as a special case of double categories.

  In the other direction, any double category has two underlying 2-categories, consisting of the objects, the vertical (resp. horizontal) arrows, and the squares whose horizontal-arrow (resp. vertical-arrow) source and target are identities.  We call these its **vertical 2-category** and **horizontal 2-category**.

* Finally, we can also make a 2-category $C$ into a double category with the same objects, whose horizontal arrows are the morphisms of $C$, whose vertical arrows are the [[adjunctions]] in $C$, and whose 2-cells are [[mate]]-pairs of 2-cells in $C$.  Naturality properties of the mate correspondence are concisely expressed by the existence of this double category.

* There is a double category $Prof$ whose objects are (small) categories, whose vertical arrows are functors, whose horizontal arrows are [[profunctors]], and whose squares are natural transformations.  This double category is in fact an [[equipment]], as are many other similar ones (such as for [[enriched categories]]).

* Any topological space has a "homotopy double groupoid" whose objects are points, whose morphisms of both types are paths (so it is edge-symmetric), and whose 2-cells are homotopies.

* There is a double category $MonCat$ whose objects are [[monoidal categories]], whose horizontal arrows are [[lax monoidal functor]]s, whose vertical arrows are [[oplax monoidal functor]]s, and whose 2-cells are generalized [[monoidal natural transformation]]s.  An analogous double category can be constructed involving the algebras for any [[2-monad]]; see [[double category of algebras]].

* There is a [[double category of model categories]] whose [[objects]] are [[model categories]], whose horizontal arrows are the right [[Quillen functor]]s, vertical arrows the left Quillen functors, and whose 2-cells are arbitrary natural transformations.  Passage to [[derived functors]] is a functor on this double category.  More generally, we can define a double category of [[homotopical categories]] and "left derivable" and "right derivable" functors.


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

* Dawson and Par&#233;, _General associativity and general composition for double categories_ , [link](http://www.numdam.org/item/CTGDC_1993__34_1_57_0/)


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

(It is tempting to try to axiomatize such a structure finitely by adding a basic "pinwheel-composition" operation, but although every non-composable arrangement reduces to one "containing" a pinwheel, the containment is not necessarily of a sort to which such an operation could be applied.  For example, here is a configuration that cannot be composed even with a "pinwheel-composition" operation:

\begin{tikzpicture}[scale=0.7]
      \draw (0,0) rectangle (2,1);
      \draw (1,1) rectangle (2,2);
      \draw (0,1) rectangle (1,3);
      \draw (1,2) rectangle (4,3);
      \draw (3,1) rectangle (4,2);
      \draw (2,0) rectangle (3,2);
      \draw (3,0) rectangle (5,1);
      \draw (4,1) rectangle (5,3);
\end{tikzpicture}

Thus, it is not clear whether there is any finitary axiomatization of such "augmented" double categories.)


## Higher categories of double categories

There are notions of [[double functor|functor]] and of [[vertical transformation|transformation]] between double categories, which make them into a [[2-category]].  In fact, due to the vertical-horizontal symmetry, there are two such 2-categories, depending on the direction we choose the transformations to go in.  Moreover, we can also take the functors to be strict, pseudo, lax, or oplax in either direction, so there are many possible 2-categories of double categories (although for some choices one has to worry about compatibility).

Probably the most useful such 2-categories are where we choose one direction to be the "arrow" direction and the other the "proarrow" direction, we take functors which are lax, oplax, or pseudo in the proarrow direction and strict in the arrow direction, and transformations that go in the arrow direction.  This is natural when considering double categories such as [[proarrow equipments]].  If we allow the functors and transformations to be only pseudo in the arrow direction as well, and add in [[modifications]] in the arrow direction, we obtain a [[3-category]] instead.  In some situations, such as the study of [[generalized multicategories]], this 3-category is a natural place in which to work (or an enlargement of it to include [[virtual equipments]] as well).

We can also combine the horizontally lax and oplax functors, together with a general notion of vertical transformation, into a large double category of double categories.  This is a special case of the double category of $T$-algebras for a particular 2-monad $T$ mentioned above; see [[double category of algebras]].

In some contexts, a natural observation is that the 1-category $DblCat$ is [[cartesian closed category|cartesian closed]], and thus enriched over itself--thus it forms a [[locally double bicategory]], i.e. a category enriched over double categories.  This can be regaded as a structure like a [[3-category]], except that it has two different kinds of 2-cells (in this case, the vertical and horizontal transformations).

In any of these higher categories, we can apply the notions and methods of higher category theory.  For instance, we automatically obtain a notion of [[monoidal double category]], namely a [[pseudomonoid]] in $DblCat$.  Likewise we have *cartesian double categories*, which are [[cartesian objects]] in $DblCat$.  If the double category in question is [[fibrant double category|fibrant]], then monoidal structures can be lifted to the horizontal bicategory; many naturally occurring [[cartesian bicategories]] can be obtained in this way.

Finally, if we want to discuss [[weighted limits]] and colimits in double categories, or construct [[generalized multicategories]] based on double categories, we may want to [[2-category equipped with proarrows|equip DblCat with proarrows]].  There is a notion of [[double profunctor]], but they do not compose associatively, and hence do not form a proarrow equipment in the usual sense; but they do form a [[virtual equipment]], which is sufficient for many purposes.

## (Skew) closed structures on the category of double categories

| Category | Internal hom | Monoidal | Comments | Reference |
| -------- | ------------ | -------- | -------- | --------- |
| Strict double categories, strict functors | Strict functors, strict vertical and horizontal transformations, modifications | Yes | Cartesian | Follows from the theory of [internal categories](https://ncatlab.org/nlab/show/internal+category#CartesianClosure) |
| Strict double categories, strict functors | Strict functors, pseudo vertical and horizontal transformations, modifications | Yes | Symmetric | [Campbell19](#Campbell19), [Böhm20](#Böhm20) |
| Pseudo double categories, strict functors | Pseudo functors, tight transformations, pseudo loose transformations, modifications | No | Symmetric skew | [Campbell19](#Campbell19) |
| Pseudo double categories, strict functors | Pseudo functors, tight transformations, pseudo loose transformations, cubical modifications | Yes | Cartesian | §2 of [Garner06](#Garner06) |
| Pseudo double categories, pseudo functors | Pseudo functors, tight transformations, pseudo loose transformations, modifications | No | Symmetric | [Campbell19](#Campbell19) |
| Strict double categories, strict functors | Strict functors, oplax horizontal, lax vertical, modifications | Yes | | Theorem 4.2 of [Femić24](#Femić24) |
| Strict double categories, strict functors | Pseudo/lax/oplax functors, pseudo/lax/oplax horizontal, dually for vertical, modifications | Yes | Skew | §6.4.2 of [Femić24](#Femić24) |

### References

* {#Böhm20} [[Gabriella Böhm]], _The Gray monoidal product of double categories_, Applied Categorical Structures 28.3 (2020): 477-515.

* {#Campbell19} [[Alexander Campbell]], _How strict is strictification?_, Journal of Pure and Applied Algebra 223.7 (2019): 2948-2976.

An exploration of the possibility of a closed structure on strict double categories and lax functors may be found in:

* [[Bojana Femić]], _Bifunctor Theorem and strictification tensor product for double categories with lax double functors_, [arXiv:2207.13452](https://arxiv.org/abs/2207.13452) (2022).

[[skew monoidal category|Skew monoidal]] structures are constructed on categories of double categories in:

* {#Femić24} [[Bojana Femić]], _Gray (skew) multicategories: double and Gray-categorical cases_, [arXiv:2408.00561](https://arxiv.org/abs/2207.13452) (2024).

## Model structures on the category of double categories

The category of strict double categories admits a plethora of [[model category|Quillen model structures]], some of which are described in papers by [Fiore, Paoli, and Pronk](#FPPModel), [Fiore and Paoli](#FPThomason), [Moser, Sarazola, and Verdugo I](#MSV2Cat) and [Moser, Sarazola, and Verdugo II](#MSVHInvar) and [Campbell](#CampbellGreg).

For more see *[[model structure on DblCat]]*.

### Gregarious model structure

The __gregarious model structure__ on the category of double categories is defined uniquely by the following two properties:

* Every double category is fibrant.
* A double functor is a trivial fibration if it is surjective on objects, full on
horizontal morphisms, full on vertical morphisms, and fully faithful on double cells.

Weak equivalences in this model structure can be characterized as follows.
A double functor $F\colon A\to B$ is a weak equivalence in the gregarious model
structure for double categories if and only if it satisfies the following four conditions.

* $F$ is surjective on objects up to gregarious equivalence, meaning that for every object $b\in B$ there is an object $a\in A$ and a gregarious equivalence $Fa\to b$ in $B$;
* $F$ is full on horizontal morphisms up to globular isomorphism;
* $F$ is full on vertical morphisms up to globular isomorphism;
* $F$ is fully faithful on double cells.

Here a _globular isomorphism_ is an invertible 2-cell in the horizontal respectively vertical [[2-category]] associated to the given double category $A$.

A __gregarious equivalence__ is a [[companion pair]] $(f,u)$ of morphisms in $A$
such that $f$ is an equivalence in the horizontal [[2-category]] of $A$
and $u$ is an equivalence in the vertical [[2-category]] of $A$.


## Related pages

* [[2-category equipped with proarrows]], [[framed bicategory]]

* [[virtual double category]]

* [[double functor]], [[double pseudofunctor]]

* [[vertical transformation]], [[horizontal transformation]]

* [[double profunctor]]

* [[double limit]]

* [[monoidal double category]], [[locally double bicategory]]

* [[triple category]], [[intercategory]], and [[multiple category]]

* [[applications of double category theory]]

* [[right-connected double category]]

* [[double fibration]]

* [[double infinity-category]]



## References ##

The concept goes back to:

* [[Charles Ehresmann]], *Catégories double et catégories structurées*, C.R. Acad. Paris 256 (1963) 1198-1201 &lbrack;[[Ehresmann-CategoriesDoubles.pdf:file]], [gallica](https://gallica.bnf.fr/ark:/12148/bpt6k3208j/f1246)&rbrack;

* {#Ehresmann63} [[Charles Ehresmann]], Déf. 10, p. 389 in: *Catégories structurées*, Annales scientifiques de l'École Normale Supérieure. Vol. 80. No. 4. Elsevier, 1963 &lbrack;[eudml:81794](https://eudml.org/doc/urn:eudml:doc:81794)&rbrack;

For a comprehensive treatment, it is probably best to consult the series of papers by Grandis and Par&#233;:

* Marco Grandis and Robert Par&#233;, [Limits in double categories](http://www.numdam.org/article/CTGDC_1999__40_3_162_0.pdf), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **40** (1999), 162--220.

* Marco Grandis and Robert Par&#233;, [Adjoints for double categories](http://www.numdam.org/article/CTGDC_2004__45_3_193_0.pdf), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **45** (2004), 193--240.

* Marco Grandis and Robert Par&#233;, [Kan extensions in double categories (On weak double categories, Part III)](http://www.tac.mta.ca/tac/volumes/20/8/20-08abs.html), Theory and Applications of Categories, Vol. 20, 2008, No. 8, pp 152-185.

* Marco Grandis and Robert Par&#233;, [Lax Kan extensions for double categories (On weak double categories, Part IV)](http://www.numdam.org/article/CTGDC_2007__48_3_163_0.pdf) Cahiers de topologie et géométrie différentielle catégoriques, tome 48, no 3 (2007), p. 163-199

For basic theory of the (virtual) double category of presheaves on a double category, the Yoneda embedding, and the density theorem

* Robert Par&#233; [Yoneda theory for double categories](http://www.tac.mta.ca/tac/volumes/25/17/25-17abs.html), Theory and Applications of Categories, Vol. 25, 2011, No. 17, pp 436-489.

* Robert Par&#233; [Composition of Modules for Lax Functors](http://www.tac.mta.ca/tac/volumes/27/16/27-16abs.html), Theory and Applications of Categories, Vol. 27, 2013, No. 16, pp 393-444. 

Textbook accounts:

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 12.3 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

* {#Grandis19} [[Marco Grandis]], _Higher dimensional categories: from double to multiple categories_, World Scientific, 2019. ([doi:10.1142/11406](https://doi.org/10.1142/11406))

See also:

* [[The Catsters]], Double Categories ([YouTube](http://www.youtube.com/watch?v=kiCZiSA2W3Q&feature=channel_page)).

* Tom Fiore, [Double categories and pseudo algebras](http://www-personal.umd.umich.edu/~tmfiore/1/CT2006Fioreslides.pdf).

* Jeffrey C. Morton, [Double bicategories and double cospans](http://arxiv.org/abs/math/0611930).

* [[Ronnie Brown]] and C.B. Spencer, [Double groupoids and crossed modules](http://www.numdam.org/item/CTGDC_1976__17_4_343_0), _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_ **17** (1976), 343--362.

* [[Ronnie Brown]]  and [[Philip Higgins]], [The equivalence of $\infty$-groupoids and crossed  complexes,](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_371_0/CTGDC_1981__22_4_371_0.pdf)  _Cah. Top. G&#233;om. Diff_. 22 (1981) 371-386.

* [[Mike Shulman]], [Comparing composites of left and right derived functors](http://nyjm.albany.edu/j/2011/17-5v.pdf), _New York J. Math._ **17** (2011) 75--125. [arXiv:0706.2868](http://arxiv.org/abs/0706.2868)

* {#Myers16} [[David Jaz Myers]], _String diagrams for double categories and (virtual) equipments_ ([arXiv:1612.02762](https://arxiv.org/abs/1612.02762))

* Kenny Courser, _Open systems: a double categorical perspective_, PhD thesis, [arxiv/2008.02394](https://arxiv.org/abs/2008.02394)

* Antonin Delpeuch, _The word problem for double categories_, [arxiv](https://arxiv.org/abs/1907.09927)

* Virtual Double Categories Workshop, 2022 ([webpage](https://bryceclarke.github.io/virtual-double-categories-workshop/2022/index.html))

* Second Virtual Workshop on Double Categories, 2024 ([webpage](https://bryceclarke.github.io/virtual-double-categories-workshop/index.html))

On [[model structures on DblCat]]:

* {#FPPModel} [[Thomas M. Fiore]], [[Simona Paoli]], [[Dorette A. Pronk]], *Model structures on the category of small double categories*, _Algebraic & Geometric Topology_ **8** (2008) 1855–1959 &lbrack;[doi:10.2140/agt.2008.8.1855](https://doi.org/10.2140/agt.2008.8.1855)&rbrack;

* {#FPThomason} [[Thomas Fiore]], [[Simona Paoli]], *A Thomason model structure on the category of small $n$-fold categories*_Algebraic & Geometric Topology_ **10** (2010) 1933–2008 &lbrack;[doi:10.2140/agt.2010.10.1933](http://doi.org/10.2140/agt.2010.10.1933)&rbrack;

* {#MSV2Cat} [[Lyne Moser]], Maru Sarazola, Paula Verdugo, *A $2Cat$-inspired model structure for double categories*, Cahiers de Topologie et Géométrie Différentielle Catégoriques, **LXIII**2 (2022) &lbrack;[arxiv:2004.14233](https://arxiv.org/abs/2004.14233), journal:[pdf](http://cahierstgdc.com/wp-content/uploads/2022/04/MoserSarazolaVerdugo-LXIII-2.pdf)&rbrack;

* {#CampbellGreg} [[Alexander Campbell]], *The gregarious model structure for double categories* (2020) &lbrack;[talk slides pdf](https://acmbl.github.io/greg_slides.pdf)&rbrack;

* {#MSVHInvar} [[Lyne Moser]], Maru Sarazola, Paula Verdugo,  *A model structure for weakly horizontally invariant double categories*, Algebraic & Geometric Topology **23** 4 (2023) 1725-1786 &lbrack;[arxiv:2007.00588](https://arxiv.org/abs/2007.00588), journal:[pdf](https://msp.org/agt/2023/23-4/agt-v23-n4-p08-p.pdf)&rbrack;

For the ([[bicategory|bicategorically]]) cartesian closed structure, see:

* [[Richard Garner]], *Double clubs*, Cahiers de Topologie et Geometrie Differentielle Categoriques 47 (2006), no. 4, 261--317; [arXiv](http://arxiv.org/abs/math/0606733)

An explicit description of what it means to be a one-object double category (i.e. filling in the gap in "a delooping of a ___ is a double category") is given in [this Math.StackExchange answer](https://math.stackexchange.com/a/3790232).

For [[univalent double categories]] in [[dependent type theory]]:

* [[Niels van der Weide]], [[Nima Rasekh]], [[Benedikt Ahrens]], [[Paige Randall North]], *Univalent Double Categories* &lbrack;[arXiv:2310.09220](https://arxiv.org/abs/2310.09220)&rbrack;

[[!redirects double category]]
[[!redirects double categories]]
[[!redirects double groupoid]]
[[!redirects double groupoids]]
[[!redirects vertical 2-category]]
[[!redirects horizontal 2-category]]
[[!redirects pseudo double category]]
[[!redirects pseudo double categories]]
[[!redirects strict double category]]
[[!redirects strict double categories]]
