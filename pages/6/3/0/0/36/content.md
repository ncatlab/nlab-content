
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Any [[mathematical structure]] whose traditional [[Bourbaki]]-style definition is formulated within [[set theory]] can be formulated *internally* to any [[category]] that admits all those types of operations (typically: [[universal constructions]]) on its [[objects]] that the traditional definition applies to [[sets]], hence to the [[objects]] of the [[base topos|base]] category of [[Sets]].

There is a [[diagram|diagrammatic]] and a [[syntax|syntactic]] way of making this precise, the former is essentially the topic of [[categorical algebra]] (in terms of [[Lawvere theories]] or [[sketches]] or the like), the latter of [[categorical semantics]] (of [[type theories]]).

An archetypical example of internalization is the notion of *[[internal groups]]*, which easily serves to illustrate the general idea:

Where the [[Bourbaki]]-style definition of a [[group]] is, of course: 

* A *group* is a [[set]] $G$ equipped with [[functions]] $e \,\colon\,\ast \to G$ and $m \colon G \times G \to G$ and $(-)^{-1} \colon G \to G$  satisfying three conditions: [[unitality]], [[associativity]], [[inverses]].

one observes that here:

1. [[sets]] and [[functions]] are the [[objects]] and [[morphisms]] in the [[category]] of [[Sets]]; 

1. in invoking the [[singleton set]] $\ast$ and the [[Cartesian product]] set $G \times G$ one is making use of the fact that [[Sets]] admit the [[universal construction]] of [[finite products]];

and that this is _only_ [[mathematical structure|structure]] on [[Sets]] that the definition of [[groups]] is making use of.
Therefore, we may abstract away from [[Sets]], consider _any_ [[category]] $\mathcal{C}$ with [[finite products]] and declare that:

* An _[[internal group]]_ in $\mathcal{C}$ is an [[object]] $G$ of $\mathcal{C}$ equipped with [[morphisms]] $e \colon \ast \to G$ (i.e. out of the [[terminal object]]) and $M \colon G \times G \to G$ (i.e. out of the [[Cartesian product]]-object) and $(-)^{-1} \colon G \to G$ such that the following [[commuting diagram|diagrams commute]] in $\mathcal{C}$:

  * [[unitality]]

    $$
      \array{
        G \times \ast
        &
        \overset{
          id \times e
        }{\longrightarrow}
        &
        G \times G
        \\
        {}^{\mathllap{
           \simeq
        }} 
        \big\downarrow
        &&
        \big\downarrow
        {}^{{}_{\mathrlap{ m }}}
        \\
        G 
        &=&
        G
      }
      \;\;\;\;\;\;\;\;
      \array{
        \ast \times G
        &
        \overset{
          e \times id
        }{\longrightarrow}
        &
        G \times G
        \\
        {}^{\mathllap{
           \simeq
        }} 
        \big\downarrow
        &&
        \big\downarrow
        {}^{{}_{\mathrlap{ m }}}
        \\
        G 
        &=&
        G
      }
    $$

  * [[associativity]]

    $$
      \array{
        G \times G \times G 
          &\overset{m \times id}{\longrightarrow}&
        G \times G
        \\
        {}^{{}_{\mathllap{ id \times m }}}
        \big\downarrow
        &&
        \big\downarrow
        {}^{{}_{m}}
        \\
        G \times G
        &\underset{ m }{\longrightarrow}&
        G
      }
    $$

  * [[inverses]] 

    $$
      \array{
        G
        &
        \overset{
          diag
        }{
          \longrightarrow
        }
        &
        G \times G
        &
          \overset{ id \times (-)^{-1} }{\longrightarrow}
        &
        G \times G
        \\
        &
        \searrow
        &
        &&
        \big\downarrow {}^{_{\mathrlap{m}}}
        \\
        &&
        \ast
        &
        \underset{ e }{\longrightarrow}
        &
        G
      }
      \;\;\;\;\;\;\;\;\;
      \array{
        G
        &
        \overset{
          diag
        }{
          \longrightarrow
        }
        &
        G \times G
        &
          \overset{ (-)^{-1} \times id }{\longrightarrow}
        &
        G \times G
        \\
        &
        \searrow
        &
        &&
        \big\downarrow {}^{_{\mathrlap{m}}}
        \\
        &&
        \ast
        &
        \underset{ e }{\longrightarrow}
        &
        G
     }
    $$


If here $\mathcal{C} = $ [[Sets]] then this recovers the [[Bourbaki]]-definition of plain [[groups]], while if $\mathcal{C} = $ [[TopologicalSpaces]] this yields the notion of [[topological groups]]; for $\mathcal{C} = $ [[SmoothManifolds]] it yields [[Lie groups]], for $\mathcal{C} = $ [[Varieties]] it yields [[algebraic groups]], etc.

Similarly one defines [[action objects|internal actions]] of internal groups, [[formally principal actions]], etc.

In fact, realizing that [[groups]] are equivalently [[pointed object|pointed]] [[n-connected object of an (infinity,1)-topos|connected]] [[groupoids]] one may readily generalize the example of [[internal groups]] to a notion of [[internal groupoids]] and then of [[internal categories]]. This way [[category theory]] and with it much of [[mathematics]]  may be considered internally to suitable ambient [[categories]] $\mathcal{C}$ (see also at _[[internal logic]]_ and _[[internal language]]_).

Moreover, if the ambient category is in fact a [[higher category theory|higher category]], then internalization goes along with ([[vertical categorification|vertical]]) _[[categorification]]_. For example an [[internal group]] in the [[2-category]] of [[Groupoids]] is a [[2-group]] (a [[strict 2-group]] if one considers just the three [[diagrams]] shown above, or a general [[2-group]] of one adds higher [[coherence]]-diagrams.)

How much mathematics/[[internal logic]] actually exists in a given ambient [[category]] depends on how much [[extra properties]] this has. For example if $\mathcal{C}$ is a [[topos]] then *all* [[constructive mathematics]] has an internal incarnation in $\mathcal{C}$. For more on this see also at _[[relation between type theory and category theory]]_.

Here is a list matching some extra structure/property of the ambient category $\mathcal{C}$ to the kind of mathematics that exists internal to it:

* If the ambient category is equipped with the structure of a [[site]], then geometrical notions, such as defining [[morphisms]] locally on the domain with patching conditions (or more generally [[descent]] theory), exist inside it. 

* If it is a [[finitely complete category]], the existence of [[finite products]] and [[terminal objects]] means that [[variety of algebras|varieties of algebras]] can be defined. 

* If the category is a [[topos]] with a [[natural numbers object]], then one can do a certain sort of "ordinary" mathematics inside it, specifically [[predicative mathematics|impredicative]] [[constructive mathematics]] without the fancier tools of [[model theory]] or (ironically) [[category theory]].

* Further extra conditions on the category, such as being a [[Boolean topos]] or being a [[superextensive site]], bring the internal mathematics closer to that of $Set$.

* If the category is a [[(infinity,1)-topos]], then one could do most of ordinary constructive mathematics inside of it, including category theory, set theory, model theory, and higher category theory. Adding the [[principle of excluded middle]] or the [[axiom of choice|axiom]] of [[choice object|choice set]]/[[0-groupoids]] results in internal classical mathematics. 

The [[extra structure]] required on the ambient category $\mathcal{C}$ is sometimes referred to as a _[[doctrine]]_ for internalization.   For example, there is a doctrine of [[monoidal categories]], a doctrine of [[finitely complete category|categories with finite limits]], a doctrine of [[cartesian closed categories]], and so on.

Like [[vertical categorification|categorification]] or [[horizontal categorification|oidification]], there is currently no completely general formal definition of the process of internalization in a [[doctrine]], although there are one or two fairly general theorems.  However, its reverse is precise: given a doctrine $\mathcal{D}$ to which [[Sets]] (or some canonical Set-like category) belongs and a definition of foo internalized in the doctrine $\mathcal{D}$, if this definition of foo in $Sets$ reduces to the usual definition of foo, then the definition is acceptable; foos are a _deinternalisation_ of internal foos.


## Examples

* [[monoid|Monoids]] can be internalized in the doctrine of [[monoidal category|monoidal categories]] ([[monoid objects]]).  For example:

  * A [[ring]] is a monoid internal to [[Ab]] with its usual tensor product.

  * An [[algebra]] is a monoid internal to [[Vect]], with its usual tensor product.

  * A strict monoidal category is a monoid internal to [[Cat]], with its cartesian product.

* Since any category with finite [[product|products]] is a [[cartesian monoidal category]], monoids can also be internalized in the doctrine of categories with finite products.

* [[group|Groups]] can also be internalized in the doctrine of categories with finite products, but not in the doctrine of monoidal categories, since diagonal maps are necessary to define what it means to have inverses.

* Monoids can also be internalized in the doctrine of [[multicategory|multicategories]].

* Commutative monoids can be internalized in the doctrine of [[symmetric monoidal category|symmetric monoidal categories]].

* Categories and groupoids can be internalized in the doctrine of [[finitely complete category|lex categories]], producing the notion of [[internal category]].

  * The classical fact that monoids can be identified with one-object categories has the following internal analogue: monoids in a lex category $C$ (qua category with finite products) can be identified with categories internal to $C$ whose object-of-objects is [[terminal object|terminal]].  However, monoids in a non-cartesian monoidal category (such as $Ab$ or $Vect$) cannot, in general, be identified with any sort of internal category.

* [[ring|Rings]] can be internalized in the doctrine of categories with finite products.

* More generally, the algebras for any [[Lawvere theory]] can be internalized in the doctrine of categories with finite products, and the algebras for any (symmetric) [[operad]] (in $Set$) can be internalized in the doctrine of (symmetric) monoidal categories.

* Pretty much any structure at all in mathematics can be internalized in a [[topos]].  Note, though, that since the [[internal logic]] of a topos is constructive, differences in axiomatization that make no difference classically can result in actual differences in behavior in a topos.  See [[constructive mathematics]] for some examples.  On the other hand, if the topos satisfies the [[axiom of choice]] (and in particular is [[Boolean topos|Boolean]]), then this complication won\'t happen.

* Categories themselves can be internalised, as algebras of an [[essentially algebraic theory]] (giving [[strict categories]]), in any [[finitely complete category]]; see [[internal category]].




## General Results

Often, the structure on the ambient category $C$ allowing a certain type of structure to be internalized in it is itself a [[vertical categorification|categorified]] version of that same structure (for example, monoids in monoidal categories).  This is an example of the [microcosm principle](http://golem.ph.utexas.edu/category/2008/12/the_microcosm_principle.html).

As one formal result along these lines, [[Tom Leinster]] has shown that for any [[cartesian monad]] $T$, $T$-algebras can be naturally internalized/enriched in $T$-multicategories, and in particular in $T$-structured categories.  For example, when $T$ is the monad whose algebras are monoids, this says that monoids can be internalized in multicategories and monoidal categories.

On the other hand, this is not always true.  For example, the categorification of a [[rig]] is a [[rig category]], but it is difficult to see how to define a rig internal to a rig category, and the usual definition of rig in $Set$ does not use the rig-category structure of $Set$ but only that it has finite products.

A very different sort of general result has to do with the [[internal logic]] of certain categories.  If a category has enough structure to interpret a certain fragment of first-order logic, then any first-order theory definable in that fragment can be internalized in that category. For example, the theory of categories can be formulated in [[cartesian logic]] and thus is interpretable in any cartesian (= lex) category. The statement that almost anything can be internalized in a topos is the high-end case of this, since the internal logic of a topos is full intuitionistic type theory.

## Examples

* [[monoid object]], 

* [[group object]], 

* [[ring object]], 

* [[monoid object in an (∞,1)-category]]

* [[Lie algebra object]]

* [[action object]]

* [[internal category]], [[internal diagram]], [[internal groupoid]], [[groupoid object in an (∞,1)-category]], [[category object in an (∞,1)-category]]

* [[internal (co-)limit]]

* [[internal site]], [[internal locale]]


* [[internal logic]]



## References
 {#References}

The general notion of internalization is due to

* {#Grothendieck60} [[Alexander Grothendieck]], p. 370 (3 of 23) in: [[FGA]] *Technique de descente et théorèmes d'existence en géométrie algébriques. II: Le théorème d'existence en théorie formelle des modules*, Séminaire Bourbaki : années 1958/59 - 1959/60, exposés 169-204, Séminaire Bourbaki, no. 5 (1960), Exposé no. 195 ([numdam:SB_1958-1960__5__369_0](http://www.numdam.org/item/SB_1958-1960__5__369_0), [pdf](http://www.numdam.org/item/SB_1958-1960__5__369_0.pdf), English translation: [pdf](https://labs.thosgood.com/builds/fga-3-II.pdf), [web version](https://thosgood.com/fga/book/FGA-3-II)).

with specialization to [[internal groups]], [[internal actions]], [[internal categories]] and [[internal groupoids]] made explicit in:

* {#Grothendieck61} [[Alexander Grothendieck]], Section 4 of: [[FGA]] _Techniques de construction et théorèmes d'existence en géométrie algébrique III: préschémas quotients_, Séminaire Bourbaki: années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf), English translation: [pdf](https://labs.thosgood.com/builds/fga-3-III.pdf), [web version](https://thosgood.com/fga/book/FGA-3-III)).

Discussion with focus on [[H-spaces]], [[internal monoids]] and [[internal groups]] and proving the [[Eckmann-Hilton argument]] originates with:

* {#EckmannHilton61} [[Beno Eckmann]], [[Peter Hilton]], *Structure maps in group theory*, Fundamenta Mathematicae 50 (1961), 207-221 ([doi:10.4064/fm-50-2-207-221](https://doi.org/10.4064/fm-50-2-207-221))

* {#EckmannHilton62} [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories I.  Multiplications and comultiplications_, Math. Ann. 145, 227–255 (1962) ([doi:10.1007/BF01451367](https://doi.org/10.1007/BF01451367))

* [[Beno Eckmann]], [[Peter J. Hilton]], _Group-like structures in general categories II.  Equalizers, limits, lengths_.  Mathematische Annalen 151:2 (1963), 150–186.  [doi:10.1007/bf01344176](https://doi.org/10.1007/bf01344176).

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories III.  Primitive categories_,  Math. Ann. **150** 165–187 (1963) ([doi:10.1007/BF01470843](https://doi.org/10.1007/BF01470843)) 

Highlighting the role of the [[Yoneda lemma]] in internalization:

* [[Saunders MacLane]], Section III.6 in: _[[Categories for the Working Mathematician]]_, Springer (1971) 

Moreover with discussion of [[action objects]]:

* {#MacLaneMoerdijk92} [[Saunders Mac Lane]], [[Ieke Moerdijk]], Section V.6 of: _[[Sheaves in Geometry and Logic]]_, Springer 1992 ([doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0))

* [[Francis Borceux]], [[George Janelidze]], [[Gregory Maxwell Kelly]], around p. 8 of: _Internal object actions_, Commentationes Mathematicae Universitatis Carolinae (2005) Volume: 46, Issue: 2, page 235-255 ([dml:249553](https://eudml.org/doc/249553))

Discussion of [[internal categories]] is often attributed to originate around (though the simple idea can hardly be recognized here):

* [[Charles Ehresmann]], _Catégories structurées_, Annales scientifiques de l'École Normale Supérieure, Série 3, Tome 80 (1963) no. 4, pp. 349-426 ([numdam:ASENS_1963_3_80_4_349_0](http://www.numdam.org/item/ASENS_1963_3_80_4_349_0))


Basics of modern internal category theory ([[internal categories]], [[internal functors]], [[internal limits]], [[internal sites]]) is discussed (without any attribution as to its origins) in:

* [MacLane-Moerdijk 92, Sec. V.7](#MacLaneMoerdijk92)

* [[Francis Borceux]], Chapter 8 in Vol 1 _Basic Category Theory_ of: _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)  ([doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858))

* [[Peter Johnstone]], Chapter B2 in: Vol. 1 of: _[[Sketches of an Elephant -- A Topos Theory Compendium]]_, Oxford University Press (2002)([ISBN:9780198534259](https://global.oup.com/academic/product/sketches-of-an-elephant-9780198534259))


More general internalization via [[sketches]]:

* [[Andrée Bastiani]], [[Charles Ehresmann]], _Categories of sketched structures_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome 13 (1972) no. 2, pp. 104-214 ([numdam:CTGDC_1972__13_2_104_0](http://www.numdam.org/item/?id=CTGDC_1972__13_2_104_0))

* [[Michael Barr]], [[Charles Wells]], Section 4 of: _[[Toposes, Triples, and Theories]]_, Originally published by: Springer-Verlag, New York, 1985, republished in: Reprints in [Theory and Applications of Categories, No. 12 (2005) pp. 1-287](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)


For more see at:

* [[algebra over a Lawvere theory|algebras over]]$\,$ [[algebraic theories]]

* [[algebra over a monad|algebras over]]$\,$ [[monads]]

* [[algebra over an operad|algebras over]]$\,$ [[operads]]





[[!redirects Internalization]]
[[!redirects internal]]
[[!redirects internal to]]
[[!redirects internally]]
[[!redirects internally to]]
[[!redirects internalisation]]
[[!redirects internalization]]
