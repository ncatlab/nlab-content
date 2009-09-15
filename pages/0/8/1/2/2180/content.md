[[!redirects theory of relations]]

_Relations have types._<br>
_Types are functions._<br>
_Functions are relations._

+-- {: .query}
Types are functions?  ---TB

The type of a $k$-adic relation arrow $f$ in a relation category $C$ is its sequence of domains $(dom_1 f, \ldots, dom_k f)$, in other words, the function $\mathop{type}_f : [1, k] \to \mathop{Obj}(C)$ defined by $\mathop{type}_f j = \mathop{dom}_j f$.  ---[[JA]]

OK, I see!  That reminds me of my favourite loop of incompatible interpretations:  A function is a kind of relation, a relation is a subset of a cartesian product, a cartesian product is a set of ordered tuples (finite sequences as above), and an ordered tuple is a kind of function.  Through this loop, $(1,1)$ (for example) belongs to itself!  Another one, which you noticed [here](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=71), is that a function is is a kind of relation, a relation is a kind of subset, and a subset is a kind of function.  In fact, a subset is a kind of function in two different ways (an inclusion function and a characteristic function), neither of which matches the original function in this loop.  ---TB

[[JA]]:  There is a related discussion on [Pragmatics Of Context](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=71) that continues in the Forum.

=--

## Idea ##

To the best of my re\*collection, it went a bit like this:

_Was sind und was sollen &mdash;_

* relational arrows?

In other words:

What Thing (1) would correspond to a Relation as an Arrow corresponds to a Function?

* Let's call Thing 1 a _Relational Arrow_.

What Thing (2) would correspond to a Relational Arrow as a Category corresponds to an Arrow?

* Let's call Thing 2 a _Relational Category_.

What Thing (3) would correspond to a Relational Category as a Metagraph corresponds to a Category?

* Let's call Thing 3 a _Relational Metagraph_.

So it seems that a __relational metagraph__ ought to consist of _objects_ $a, b, c, \ldots$, _relational arrows_ $f, g, h, \ldots$, and a number of operations $\mathop{dom}_j$ that assign to each relational arrow $f$ an object $\mathop{dom}_j f$ for each $j$ in the arity of $f$.

_Et sic deinceps &hellip;_

The path to this point has been straight and narrow, cut and dried --- like rolling a boulder up a hill of abstraction --- the air gets rare but getting to the top is so reflexive that any bot could see the way there.  But the summit presents a wealth of new vistas, and seeing the way clear from a relational metagraph to a relational metacategory demands reflection on many more choices than we could see from our base camp at _Che Valley_.

Guidance in sorting abstract sense from abstract nonsense can be had by resorting to the relational analogues of concrete categories, in short, to [[Rel|sets and relations]].  Fortune smiles, for the world of applications is blessed with an almost embarrassing richness of these.

$\ldots$

This approach to relation theory grows out of (1) some of my earliest strugglings with the foundations of mathematics and the nature of functions, (2) long-continued wrestling with C.S. Peirce's "logic of relatives", (3) some ideas I had in the early 1980's about "relational arrows" and "making relations universal", (4) course work on category theory, combinators, and $\lambda$-calculus and discussions with John Gray at UIUC in the middle 1980's, (5) course work on relational programming and discussions with Fatma Mili at OU in the 1990's.  What I've been able to reconstruct so far is only a fragment of what (I think) I had in mind.  ---[[Jon Awbrey]]

***

This article treats __[[relations]]__ from the perspective of combinatorics, in other words, as a subject matter in discrete mathematics, with special attention to finite structures and concrete set-theoretic constructions, many of which arise quite naturally in applications.  This approach to __relation theory__, or the __theory of relations__, is distinguished from, though closely related to, its study from the perspectives of abstract algebra on the one hand and formal logic on the other.

## Preliminaries ##

Two definitions of the relation concept are common in the literature.  Although it is usually clear in context which definition is being used at a given time, it tends to become less clear as contexts collide, or as discussion moves from one context to another.

The same sort of ambiguity arose in the development of the function concept and it may save some effort to follow the pattern of resolution that worked itself out there.

When we speak of a function $f : X \to Y$ we are thinking of a mathematical object whose articulation requires three pieces of data, specifying the set $X$, the set $Y$, and a particular subset of their cartesian product $X \times Y$.  So far so good.

Let us write $f = (obj_1 f, obj_2 f, obj_{12} f)$ to express what has been said so far.

When it comes to parsing the notation &ldquo;$f : X \to Y$&rdquo;, everyone takes the part &ldquo;$X \to Y$&rdquo; to specify the _type_ of the function, that is, the pair $(obj_1 f, obj_2 f)$, but &ldquo;$f$&rdquo; is used equivocally to denote both the triple and the subset $obj_{12} f$ that forms one part of it.  One way to resolve the ambiguity is to formalize a distinction between a function and its _[[graph of a function|graph]]_, letting $graph (f) \:\text{:=}\: obj_{12} f$.

Another tactic treats the whole notation &ldquo;$f : X \to Y$&rdquo; as sufficient denotation for the triple, letting &ldquo;$f$&rdquo; denote $graph (f)$.

In categorical and computational contexts, at least initially, the type is regarded as an essential attribute or an integral part of the function itself.  In other contexts it may be desirable to use a more abstract concept of function, treating a function as a mathematical object that appears in connection with many different types.

Following the pattern of the functional case, let the notation &ldquo;$L \subseteq X \times Y$&rdquo; bring to mind a mathematical object that is specified by three pieces of data, the set $X$, the set $Y$, and a particular subset of their cartesian product $X \times Y$.  As before we have two choices, either let $L = (X, Y, graph (L))$ or let &ldquo;$L$&rdquo; denote $graph (L)$ and choose another name for the triple.

## Definition ##

It is convenient to begin with the definition of a $k$-place relation, where $k$ is a positive integer.

+-- {: .un_defn}
###### Definition
A $k$-place relation $L \subseteq X_1 \times \ldots \times X_k$ over the nonempty sets $X_1, \ldots, X_k$ is a $(k+1)$-tuple $(X_1, \ldots, X_k, L)$ where $L$ is a subset of the cartesian product $X_1 \times \ldots \times X_k$.
=--

## Remarks ##

Though usage varies as usage will, there are several bits of optional language that are frequently useful in discussing relations.  The sets $X_1, \ldots, X_k$ are called the _domains_ of the relation $L \subseteq X_1 \times \ldots \times X_k$, with $X_j$ being the $j^{th}$ domain.  If all of the $X_j$ are the same set $X$, then $L \subseteq X_1 \times \ldots \times X_k$ is more simply described as a $k$-place relation over $X$.  The set $L$ is called the _[[graph of a relation|graph]]_ of the relation $L \subseteq X_1 \times \ldots \times X_k$, on analogy with the graph of a function.  If the sequence of sets $X_1, \ldots, X_k$ is constant throughout a given discussion or is otherwise determinate in context, then the relation $L \subseteq X_1 \times \ldots \times X_k$ is determined by its graph $L$, making it acceptable to denote the relation by referring to its graph.  Other synonyms for the adjective _$k$-place_ are _$k$-adic_ and _$k$-ary_, all of which leads to the integer $k$ being called the _dimension_, the _adicity_, or the _arity_ of the relation $L$.

## Incidence properties ##

### Local incidence properties ###

A _local incidence property_ (LIP) of a relation $L$ is a property that depends in turn on the properties of special subsets of $L$ that are known as its _local flags_.  The local flags of a relation are defined in the following way:

Let $L$ be a $k$-place relation $L \subseteq X_1 \times \ldots \times X_k$.

Select a relational domain $X_j$ and one of its elements $x$.  Then $L_{x \text{@} j}$ is a subset of $L$ that is referred to as the _flag_ of $L$ with $x$ at $j$, or the $(x \text{@} j)$-flag of $L$, an object that has the following definition:

\[ L_{x \text{@} j} = \{ (x_1, \ldots, x_j, \ldots, x_k) \in L : x_j = x \}. \]

Any property $C$ of the local flag $L_{x \text{@} j} \subseteq L$ is said to be a _local incidence property_ of $L$ with respect to the _locus_ $x \text{@} j$.

A $k$-adic relation $L \subseteq X_1 \times \ldots \times X_k$ is said to be _$C$-regular_ at $j$ if and only if every flag of $L$ with $x$ at $j$ has the property $C$, where $x$ is taken to vary over the _theme_ of the fixed domain $X_j$.  

Expressed in symbols, $L$ is $C$-regular at $j$ if and only if $C(L_{x \text{@} j})$ is true for all $x$ in $X_j$.

### Regional incidence properties ###

The definition of a local flag can be broadened from a point $x$ in $X_j$ to a subset $M$ of $X_j$, arriving at the definition of a _regional flag_ in the following way:

Suppose that $L \subseteq X_1 \times \ldots \times X_k$, and choose a subset $M \subseteq X_j$.  Then $L_{M \text{@} j}$ is a subset of $L$ that is said to be the _flag_ of $L$ with $M$ at $j$, or the $(M \text{@} j)$-flag of $L$, an object which has the following  definition:

\[ L_{M \text{@} j} = \{ (x_1, \ldots, x_j, \ldots, x_k) \in L : x_j \in M \}. \]

### Numerical incidence properties ###

A _numerical incidence property_ (NIP) of a relation is a local incidence property that depends on the cardinalities of its local flags.

For example, $L$ is said to be $c$-regular at $j$ if and only if the cardinality of the local flag $L_{x \text{@} j}$ is $c$ for all $x$ in $X_j$, or, to write it in symbols, if and only if $|L_{x \text{@} j}| = c$ for all $x \in X_j$.

In a similar fashion, one can define the NIPs, $(\lt c)$-regular at $j$, $(\gt c)$-regular at $j$, and so on.  For ease of reference, a few of these definitions are recorded here:

*  $L$ is $c$-regular at $j$ if and only if $|L_{x \text{@} j}| = c$ for all $x \in X_j$.
*  $L$ is $(\lt c)$-regular at $j$ if and only if $|L_{x \text{@} j}| \lt c$ for all $x \in X_j$.
*  $L$ is $(\gt c)$-regular at $j$ if and only if $|L_{x \text{@} j}| \gt c$ for all $x \in X_j$.

## Species of 2-adic relations ##

Returning to 2-adic relations, it is useful to describe some familiar classes of objects in terms of their local and numerical incidence properties.  Let $L \subseteq S \times T$ be an arbitrary 2-adic relation.  The following properties of $L$ can be defined:

*  $L$ is total at $S$ if and only if $L$ is $(\ge 1)$-regular at $S$; such a relation is sometimes called [[entire relation|entire]].
*  $L$ is total at $T$ if and only if $L$ is $(\ge 1)$-regular at $T$.
*  $L$ is tubular at $S$ if and only if $L$ is $(\le 1)$-regular at $S$; such a relation is sometimes called [[functional relation|functional]].
*  $L$ is tubular at $T$ if and only if $L$ is $(\le 1)$-regular at $T$.

If $L \subseteq S \times T$ is tubular at $S$, then $L$ is called a _[[partial function]]_ or a _prefunction_ from $S$ to $T$.  This is sometimes indicated by giving $L$ an alternate name, say, &ldquo;$p$&rdquo;, and writing $L = p : S \:\dashrightarrow\: T$.

Just by way of formalizing the definition:

:  $L \; = \; p : S \:\dashrightarrow\: T$ if and only if $L$ is tubular at $S$.

If $L$ is a prefunction $p : S\:\dashrightarrow\: T$ that happens to be total at $S$, then $L$ is called a _[[function]]_ from $S$ to $T$, indicated by writing $L = f : S \to T$.  To say that a relation $L \subseteq S \times T$ is _totally tubular_ at $S$ is to say that it is $1$-regular at $S$.  Thus, we may formalize the following definition:

:  $L \; = \; f : S \to T$ if and only if $L$ is $1$-regular at $S$.

In the case of a function $f : S \to T$, one has the following additional definitions:

*  $f$ is [[surjective function|surjective]] if and only if $f$ is total at $T$.
*  $f$ is [[injective function|injective]] if and only if $f$ is tubular at $T$.
*  $f$ is [[bijective function|bijective]] if and only if $f$ is $1$-regular at $T$.

## Variations ##

Because the concept of a relation has been developed quite literally from the beginnings of logic and mathematics, and because it has incorporated contributions from a diversity of thinkers from many different times and intellectual climes, there is a wide variety of terminology that the reader may run across in connection with the subject.

One dimension of variation is reflected in the names that are given to $k$-place relations, for $k = 0, 1, 2, 3, \ldots$, with some writers using the Greek forms, _medadic_, _monadic_, _dyadic_, _triadic_, _$k$-adic_, and other writers using the Latin forms, _nullary_, _unary_, _binary_, _ternary_, _$k$-ary_.

The cardinality of the relational ground, the set of relational domains, may be referred to as the _adicity_, the _arity_, or the _dimension_ of the relation.  Accordingly, one finds a relation on a finite number of domains described as a _polyadic_ relation or a _finitary_ relation, but others count infinitary relations among the polyadic.  If the number of domains is finite, say equal to $k$, then the relation may be described as a _$k$-adic_ relation, a _$k$-ary_ relation, or a _$k$-dimensional_ relation, respectively.

A more conceptual than nominal variation depends on whether one uses terms like _predicate_, _relation_, and even _term_ to refer to the formal object proper or else to the allied syntactic items that are used to denote them.  Compounded with this variation is still another, frequently associated with philosophical differences over the status in reality accorded formal objects.  Among those who speak of numbers, functions, properties, relations, and sets as being real, that is to say, as having objective properties, there are divergences as to whether some things are more real than others, especially whether particulars or properties are equally real or else which one is derivative in relationship to the other.  Historically speaking, just about every combination of modalities has been used by one school of thought or another, but it suffices here merely to indicate how the options are generated.

## Bibliography on relations and related subjects ##

* Barr, Michael; and Wells, Charles (1990), _Category Theory for Computing Science_, Prentice Hall, Hemel Hempstead, UK.
* Bourbaki, Nicolas (1994), _Elements of the History of Mathematics_, John Meldrum (trans.), Springer-Verlag, Berlin, Germany.
* Carnap, Rudolf (1958), _Introduction to Symbolic Logic with Applications_, Dover Publications, New York, NY.
* Chang, C.C., and Keisler, H.J. (1973), _Model Theory_, North-Holland, Amsterdam, Netherlands.
* van Dalen, Dirk (1980), _Logic and Structure_, 2nd edition, Springer-Verlag, Berlin, Germany.
* Devlin, Keith J. (1993), _The Joy of Sets : Fundamentals of Contemporary Set Theory_, 2nd edition, Springer-Verlag, New York, NY.
* Halmos, Paul Richard (1960), _Naive Set Theory_, D. Van Nostrand Company, Princeton, NJ.
* van Heijenoort, Jean (1967/1977), _From Frege to G&#246;del : A Source Book in Mathematical Logic, 1879--1931_, Harvard University Press, Cambridge, MA, 1967.  Reprinted with corrections, 1977.
* Kelley, John L. (1955), _General Topology_, Van Nostrand Reinhold, New York, NY.
* Kneale, William; and Kneale, Martha (1962/1975), _The Development of Logic_, Oxford University Press, Oxford, UK, 1962.  Reprinted with corrections, 1975.
* Lawvere, Francis William; and Rosebrugh, Robert (2003), _Sets for Mathematics_, Cambridge University Press, Cambridge, UK.
* Lawvere, Francis William; and Schanuel, Stephen H. (1997/2000), _Conceptual Mathematics : A First Introduction to Categories_, Cambridge University Press, Cambridge, UK, 1997.  Reprinted with corrections, 2000.
* Manin, Yu. I. (1977), _A Course in Mathematical Logic_, Neal Koblitz (trans.), Springer-Verlag, New York, NY.
* Mathematical Society of Japan (1993), _Encyclopedic Dictionary of Mathematics_, 2nd edition, 2 vols., Kiyosi It&#244; (ed.), MIT Press, Cambridge, MA.
* Mili, A., Desharnais, J., Mili, F., with Frappier, M. (1994), _Computer Program Construction_, Oxford University Press, New York, NY. --- Introduction to Tarskian relation theory and its applications within the relational programming paradigm.
* Mitchell, John C. (1996), _Foundations for Programming Languages_, MIT Press, Cambridge, MA.
* Peirce, Charles Sanders (1870), "Description of a Notation for the Logic of Relatives, Resulting from an Amplification of the Conceptions of Boole's Calculus of Logic", _Memoirs of the American Academy of Arts and Sciences_ 9 (1870), 317--378.  Reprinted (CP 3.45--149), (CE 2, 359--429).
* Peirce, Charles Sanders (1931--1935, 1958), _Collected Papers of Charles Sanders Peirce_, vols. 1--6, Charles Hartshorne and Paul Weiss (eds.), vols. 7--8, Arthur W. Burks (ed.), Harvard University Press, Cambridge, MA.  Cited as (CP volume.paragraph).
* Peirce, Charles Sanders (1981--), _Writings of Charles S. Peirce : A Chronological Edition_, Peirce Edition Project (eds.), Indiana University Press, Bloomington and Indianapolis, IN.  Cited as (CE volume, page).
* Poizat, Bruno (2000), _A Course in Model Theory : An Introduction to Contemporary Mathematical Logic_, Moses Klein (trans.), Springer-Verlag, New York, NY.
* Quine, Willard Van Orman (1940/1981), _Mathematical Logic_, 1940.  Revised edition, Harvard University Press, Cambridge, MA, 1951.  New preface, 1981.
* Royce, Josiah (1961), _The Principles of Logic_, Philosophical Library, New York, NY.
* Runes, Dagobert D. (ed., 1962), _Dictionary of Philosophy_, Littlefield, Adams, and Company, Totowa, NJ.
* Shoenfield, Joseph R. (1967), _Mathematical Logic_, Addison-Wesley, Reading, MA.
* Styazhkin, N.I. (1969), _History of Mathematical Logic from Leibniz to Peano_, MIT Press, Cambridge, MA.
* Suppes, Patrick (1957/1999), _Introduction to Logic_, 1st published 1957.  Reprinted, Dover Publications, New York, NY, 1999.
* Suppes, Patrick (1960/1972), _Axiomatic Set Theory_, 1st published 1960.  Reprinted, Dover Publications, New York, NY, 1972.
* Tarski, Alfred (1956/1983), _Logic, Semantics, Metamathematics : Papers from 1923 to 1938_, J.H. Woodger (trans.), Oxford University Press, 1956.  2nd edition, J. Corcoran (ed.), Hackett Publishing, Indianapolis, IN, 1983.
* Ulam, Stanislaw Marcin; and Bednarek, A.R. (1977), "On the Theory of Relational Structures and Schemata for Parallel Computation", pp. 477--508 in A.R. Bednarek and Fran&#231;oise Ulam (eds.), _Analogies Between Analogies : The Mathematical Reports of S.M. Ulam and His Los Alamos Collaborators_, University of California Press, Berkeley, CA, 1990.
* Ulam, Stanislaw Marcin (1990), _Analogies Between Analogies : The Mathematical Reports of S.M. Ulam and His Los Alamos Collaborators_, A.R. Bednarek and Fran&#231;oise Ulam (eds.), University of California Press, Berkeley, CA.
* Ullman, Jeffrey D. (1980), _Principles of Database Systems_, Computer Science Press, Rockville, MD.
* Venetus, Paulus (1472/1984), _Logica Parva : Translation of the 1472 Edition with Introduction and Notes_, Alan R. Perreiah (trans.), Philosophia Verlag, Munich, Germany.

## External links ##

* [Relation Theory @ PlanetMath](http://planetmath.org/encyclopedia/RelationTheory.html)

* [Relation Theory @ PlanetPhysics](http://planetphysics.org/encyclopedia/RelationTheory.html)

* [Peirce's 1870 Logic Of Relatives](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Peirce's_1870_Logic_Of_Relatives)

## Discussion ##

JA = [[Jon Awbrey]], TB = [[Toby Bartels]]

### Re: Idea ###

TB: Are you dissatisfied with [[allegory|allegories]]?

JA: I looked into Freyd and Scedrov when it first came out --- I still have a copy around here _somewhere_.  It seemed quite nice as far as it went but --- best I recall --- it was mostly about 2-ary relations?

TB: Yes, that\'s a good point.  It seems that you need something like a multiallegory, the allegorial version of a [[multicategory]].  As far as I know, nobody has studied such a thing, although it does seem like an obvious thing to try.

JA: I didn't know about Chu spaces at the time I set out on this line of inquiry --- and I don't know much more than the name today --- but I think a lot of this could probably be absorbed into that medium.  Then again, what can't?

TB: I\'ve asked the [`categories` mailing list](http://www.mta.ca/~cat-dist/) about this.

### Re: Preliminaries ###

TB: One problem with '$L: X \times Y$' is that it conflicts with standard type-theoretic notation.  That might not be such a problem, since you\'re not doing type theory, except that '$f: X \to Y$' *agrees* with that notation.  As '$X \to Y$' is the type of transformations (functions, in this case) from $X$ to $Y$ (the [[function set|function type]]), so '$X \times Y$' is the type of ordered pairs from $X$ and $Y$ (the binary [[cartesian product|product type]]).  So if '$f: X \to Y$' indicates that $f$ is a function (of a certain type), then '$L: X \times Y$' should indicate that $L$ is an ordered pair (of a certain type).  Accordingly, it might be better to either write something like '$L: P(X \times Y)$' (with '$P$' denoting the [[power set|power type]]) or simply to use a different symbol in place of '$\times$' (although I don\'t know of any standard.

TB: All that said, however, you could still declare that '$\times$' in your notation simply doesn\'t mean the product type, but instead means the power type of the product type, and that\'s that.  (And maybe you want to think of the type of relations as a fundamental concept, rather than derived from power type and product type, which is fine by me.)  As long as you don\'t use it in any other way, then you should be fine.

TB: PS.  Reading a little further, I see that I have to correct this, but I\'ll leave it up for now.

JA: Sorry, that was more of a typo than a theory of typing, as I was experimenting with a variety of different symbols --- like $:$ and $:\!\!\!\subseteq$ --- and forget to change them all back.  I now think it's probably best just to use the subset symbol, so long as one understands that the domains are parts of the definition --- like source and target with arrows.  I sometimes call this the "strongly-typed" definition of relations.

TB: Yeah, I thought about $:\subseteq$, except that one of the bugs of iTeX is that it doesn\'t do the spacing right (as you seem to have noticed!).

### Re: Definition ###

TB: Ah, dang, there goes my idea about reinterpreting '$\times$'!  If that\'s the cartesian product above, then the business about being a subset is all pushed into the colon, which really does not agree with the colon in '$f: X \to Y$'.  That could still be OK, as long as you always use the colon for that, but how about using '$\subseteq$' instead?
