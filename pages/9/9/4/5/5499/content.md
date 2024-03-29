# Generalisation as an adjunction
* the following line creates the automatic table of contents
{: toc}


## Introduction ##

The hypothesis I want to explore is that generalisation can be represented as
an [[adjunction]]. More precisely, that generalisation and instantiation can be represented as an [[adjoint pair]], generalisation being the [[left adjoint]].

By "generalisation", I mean learning concepts from
examples, e.g. in machine learning. I believe that this applies to many
different topics in machine learning, including statistical curve-fitting
(and its implementation in various kinds of neural net), symbolic vector
architectures, instance-based learning, and logical induction. If I'm
right, this could be an important unification of these apparently
unrelated topics.

Because I don't have funding to do research, I've had no time to develop these ideas. So the best I can do 
so far is to justify the hypothesis by appealing to various intuitions, and to related
mathematical and computational phenomena. I've put this material into nLab because I think it's interesting, and may well be important to machine learning: the categorists and machine-learning experts I've asked agree.  So perhaps other readers can supply technical substantiation or refutation. If I can ever get funding then of course I'll do so as well. By the way, most of them have also said that even if this result is known to categorists, it isn't known within machine learning, and that publicising it would therefore be useful.

## Potential uses in machine learning ##

These are similar to those that [[Joseph Goguen]]
proposed for category theory in computing science
in [[A Categorical Manifesto]]. 
If much concept learning can be represented by the same phenomenon, namely an
adjunction, this should make it easier to compare learning algorithms and
to translate algorithms from one branch of machine learning to another.
Moreover, algorithms that can be represented as adjunctions may be better
&#8212; if only because they're easier to reason about &#8212; than those that can't.

## Potential use in category theory ##

This is very speculative. But suppose that many kinds of generalisation can be formulated as adjunctions. Then what properties distinguish those adjunctions from others? If none, does this mean that all adjunctions can be regarded as generalisations? If so, does that tell us anything useful about adjunctions? Perhaps an information-theoretic way of thinking about them?

## Idea ##

Let $C$ be a category of concepts, and $E$ be a category of sets of examples.

Let $G \colon E \to C$ be a "generalisation" functor that maps each set of
examples to its generalisation as a concept. 

Conversely, let
$F \colon C\to E$ be a forgetful functor that maps each concept to some
canonical set of examples. 

Then my hypothesis is that $F$ and $G$ form an adjunction,
$G$ being left adjoint to $F$.
 
### Interpretation for non&#8211;category-theorists ###

Suppose we have a set 
$E$ of sets
of examples, and a set $C$ of concepts. Then we can define a function $G$ that
maps each set of examples $e$ in $E$ to a concept $c$ in $C$, by generalisation.
Conversely, we can define a function $F$ that maps each concept 
$c$ in $C$ to a
set of examples $e$ in $E$. 

I hope that we can then regard
$G$ as finding what might be called the smallest
generalisation, or most efficient representation, of its argument. 
Conversely, 
$F$ ought to
"forget" whatever extra structure $e$ gained by becoming a
concept, turning it back into a "canonical" set of examples. $F$ and $G$ may
not be inverses, but they are, in some sense, the nearest one can get to
inverses. I say what's in this paragraph because (a) these are properties
that I believe generalisation and forgetting should have; (b) 
adjoint functors often (always?) seem to work like this. 

### What is a concept? ###

I haven't said anything about what a concept is. One possibility, just to
illustrate the idea, is the statistical regression line given by a least-squares
fit.  $E$'s objects would then be sets of 2-d points to be fitted, and C's
would be regression lines, probably equipped with goodness-of-fit
information. This is a simple example; instances of other, more complicated, statistical models could also be concepts.

Some other possibilities for concepts are: high-dimensional vectors formed
by superimposing vectors of property-value pairs in so-called "symbolic
vector architectures" or "holographic reduced representations";  regions
of classification space; logical propositions learnt by induction.

### What is generalisation? ###

Here are some examples.

* The examples are two-dimensional points (members of 
$R^2$). Generalisation is least-squares fitting, as above. The 
concept is a line giving the best least-squares fit to the points. 

* Generalisation is fitting of some other statistical model. The concept is an instance of that model.

* The examples are logical sentences, classified as positive or negative. 
Generalisation is logical induction. The concept is a new sentence from which we 
can infer as many of the positive examples as possible (hopefully all) and as 
few of the negative examples (hopefully none) as possible. 

* The examples are pairs $\langle{v,w}\rangle$ associating an element of the 
vector space $V$ with an element of the vector space 
$W$. Generalisation is training a linear-associator neural net. The concept is a linear transformation which, if possible, maps all the $v$ 
to the $w$, and if that's not possible, does the best it can by finding 
an optimum transform which minimises interference between different 
$\langle{v,w}\rangle$ associations. 

* The examples are pairs $\langle{p,l}\rangle$ where $p$ is a point in 
$R^n$ and $l$ is a member of some set 
$L$ of symbolic labels. For instance, the $p$ might be 
elements of some space whose dimensions measure a voter's preference for 
various policies; the $l$ could then be the possible parties, 
$\{green,labour,libdem,tory\}$. Generalisation is nearest-neighbour 
prediction. The concept is a function which extends the set of pairs 
$\langle{p,l}\rangle$, mapping every point in $R^n$ to a 
label. It can therefore be used to predict the preferred party of other 
voters. I've taken this example from _Truth 
from Trash_ by Chris Thornton. 

* The examples are the instances of generalisation given in this write-up. 
Generalisation is fitting each to a notion in category theory. The concept is a categorical construct...!

### What other structure might the category of examples have? ###

Although I introduced $E$ as a category of sets of
examples, I'm sure there are other possibilities. An obvious one, though
still set-related, is that the objects are weighted sets, where each
weight tells the generaliser how important the corresponding example is.
This probably ties up with fuzzy logic, fuzzy set theory, and stochastic logic programming. See also the following section.

## Some simple examples of generalisation in more detail##

These are taken from my short write-up [_Generalisation is an adjunction_](http://www.j-paine.org/generalisation.html), recast into the naming convention I'm using here. 

### 1. Logical induction by conjunction ###

Let $C$ be the 
category whose objects are the atomic propositions 
$P$, $Q$, $R$, ... and their conjunctions. Let there be an arrow from 
$P$ 
to $P'$ if $P$ implies $P'$. This makes $C$ into 
a partial ordering defined by implication.

Let $E$ be the category
whose objects are non-empty sets of the above atomic propositions. It has the obvious partial ordering by inclusion.

Let $G$ map
each set of propositions in $E$ to their conjunction in $C$; let $F$ be its inverse. $G$ and $F$ reverse arrows, as in the next example.

The above is trivial, but I find it suggestive. Because it seems reasonable to say that forming the conjunction of a set of 
propositions as $G$ does is one (crude) way of generalising from them. Informally speaking, the conjunction contains just enough information to imply 
them all, but none of the others in the category (unless they were implied by 
the originals anyway). Now, we also know that in $C$, their 
conjunction is their limit. (More correctly, it's a limit of the diagram 
containing the propositions and the implication arrows between them.) But this 
formalises the notion expressed in the "just enough information" sentence, 
because of the universal mapping property of the limit. (That is, any other 
proposition which implies the originals also implies their conjunction.) 

### 2. Logical induction by quantification ###

Let $E$'s objects be the non-empty sets of sentences $e(I)$ where $I$ is an integer. So one 
object would be ${ e(1), e(2) }$. Interpret $e(I)$ as meaning "the 
integer $I$ is an example of the concept". Interpret the arrows in 
$E$ as set inclusion. 

Let $C$ be the category whose objects are sentences: 
either the atomic sentences $e(I)$ or the universally-quantified sentence 
$\forall X \colon e(X)$. (Unlike the category of sentences in the
earlier 
example, this category does not contain conjunctions.) Interpret the arrows 
as implication. 

Now define $G$
as follows. $G$ maps each singleton $e(I)$ to the sentence $e(I)$. It maps sets with more than one element 
to the universally-quantified sentence. It also reverses arrows, mapping set 
inclusion to reverse implication. 

We could say that $G$ implements a simple form of logical induction, 
rather more interesting than the earlier 
one. And there are two languages, that of $C$ 
restricted compared to that of $E$, because 
$C$ cannot express conjunctions, and so has to 
approximate them by quantifying over all possible cases. The functor $G$ is 
"doing the best it can" in these circumstances. 

### 3. Least-squares fitting ###

Let $E$'s objects be the non-empty sets 
of colinear elements of $R^2$. Once again, let the arrows 
be set inclusion. 

Let $C$ be the category whose objects are either the 
singletons $\{ x \in R^2 \}$ or infinite lines in 
$R^2$. Let the arrows be set inclusion.

Then let $G$ map each singleton to itself, and map each set 
$S$ with more than one element to the line going through all $S$'s 
points. $G$ maps inclusions to inclusions. As with the previous instance, 
$G$ flattens most of $E$ into 
$C$. 

### Where are the adjunctions? ###

All the instances above can be formalised as adjunctions. Here's a summary of the proof, via [[Galois connection|Galois connections]]:
1. $E$ and $C$ are posets.
2. $G$ and $F$ are order-preserving, which is a necessary condition in the definition of Galois connection. 
3. $G$ and $F$ satisfy the Galois connection condition.
4. A Galois connection is a special case of an adjunction.

The first point follows from the orderings I imposed on $E$ and $C$. The second holds for $F$, because it's either an identity, as in the least-squares example, or equivalent to one, as in the conjunction and quantification examples. It holds also for $G$, because it can't "cross over". If $e \lt e'$, then $G e$ may equal $G e'$, but it can't be greater. The third point follows by simple calculation with these orders. The fourth is a standard result.

$G$ can be regarded as a functor which maps a set of examples to an object which is in some 
sense the "completion" of that set: the good old "free completion". It acquires a right adjoint $F$ which 
maps this object back to the set of all possible examples derivable from this 
completion object. 

I think of this
in terms of the units and counits: an adjunction $E$
to $C$ is determined by the two functors $G$ and
$F$ and by two natural transformations 
$i \colon I_E \Rightarrow G;E$
and
$e \colon E;G \Rightarrow I_G$. Given any object $c$ in 
$C$, there is a morphism taking every $G F c$ to 
$c$. Since $F$ maps $g$ to the set of all possible examples, and 
$G$ should map that back to the original generalisation, this is the 
identity. Hence we get one natural transformation. 

In the other direction, given any object $e$ in 
$E$, the functor $F G$ will map it to the set of all 
possible examples of which $E$ is a part. There is an inclusion from 
$e$ to $F G e$, and since this respects the other inclusions in 
$E$, once again we get a natural transformation, 
$i \colon I_E \Rightarrow G;E$. 

(I need to relate this to the notion of limiting amount of information, 
showing how that arises from the adjunction.) 

### The problem of noise, and of different languages ###

In the least-squares example, I stipulated that the sets of points in $E$
must be colinear. This isn't very realistic: in real life, most sets of 
examples will not exactly fit a line. 

In general, given any useful generalisation method, some sets of examples 
will not have an exact generalisation. You can say that this is due to 
experimental error, or to an inadequate statistical model, or to an 
insufficiently powerful description language, or to restricted storage capacity, 
or whatever. See also sections on "Change of language" below.

I thought of fixing this by extending 
$G$ so that it maps each set of non-colinear points 
to the line with the least least-squares distance from them. 
(But what if, in this 
or other examples, there is no unique best generalisation?) 

The problem with 
this is that $G$ then no longer respects the arrows between the sets in $E$. Originally, if $S$ was a 
subset of $S'$, then $G(S)$ was a subset of $G(S')$. But this is 
no longer necessarily true: if the points in $S$ are colinear, and we make 
$S'$ from $S$ by adding a point that isn't on the line, then the 
best-fit line to $S'$ will be different from that to $S$, so the 
inclusion won't hold. 

Maybe the way to fix this is not to decide _a priori_ that the 
morphisms in $E$ should be inclusions, but to let them 
be determined by the morphisms in $C$. Philosophically 
speaking, perhaps this is reasonable &#8212; we don't perceive the raw data directly, 
but always fit it to a preconceived model. But I feel I'm missing something else.

What's the essence? A least-squares fit maps a set of points $e_i$ as follows. Some points $e_good$ fall exactly onto the regression line. Others, $e_bad$, don't. In effect, it's splitting the set into two parts, one of which needs added error information to describe it. Equivalently, it's adding error information to every point, even though that's 0 for some. Consider in the light of the FCA example $\{apple,orange\},
\{apple,pear\}$ vs. $\{round\},\{green\}$, and extension vs. intension. What _property_ is common to all points on a regression line?

... I need fonts to distinguish between sets of examples and their elements...

That's about as far as I've got; the examples I've so far constructed have the same structure as in 18, and seem to be missing something. I need to think about the structure of $C$ and $E$, and probably get away from $E$ being only a subcategory of Set. One possibility which feels promising (thanks to Victor Winschel for encouraging me on this) is to see whether stochastic logic programming can be formulated in terms of adjoints. 

### Another example: learning linear transformations ###

(I need to complete this and the following examples.)
In this, I'm leading up to generalisation in simple neural networks. Think of learning a linear transformation. $E$ is the category of sets of pairs $\langle v,w \rangle$. $C$ is the category of linear transformations between vector spaces $V$ and $W$. $G$ puts pairs together to make a linear transformation. (What does $F$ do, and is it unique?) As with the least-squares example, this only works exactly if I restrict the sets in $E$.

### Another example: linear associators ###

The idea is as in the previous example, but where sets of examples aren't restricted to being expressible as linear transformations. In this case, generalisation has to "do the best it can", modulo interference between learnt associations. Question: what should $C$ be? Ought it to be some kind of completion of $C$ above? See http://www.syndar.org/PAdams/The%20Linear%20Associator.pdf for how the associator works. $C$ will depend very tightly on how the associator is trained. I'll start by considering how a single learning phase, in the terminology of the above reference, maps pairs to a matrix: the matrix $W$ in the notation of the reference's Equations 1 onwards. (Also to be completed.)

### Another example: averages ###

Let $E$ be the category of real pairs $\langle h, t \rangle$. Let $C$ be the category of real pairs whose elements sum to 1. Let $G$ map $\langle h, t \rangle$ to $\langle h/(h+t), t/(h+t) \rangle$. Let $F$ be the identity.
(Are $E$ and $C$ discrete?) (I'm working towards the way that induction in stochastic logic programming induces weights for the learnt clauses.)

### Another example: generalisation against a background ###

I don't know what to call this, but it feels relevant. It's a picture that came to me. Imagine that $E$ is the category of subsets of $R^2$. Now imagine that we have a real plane hatched by irregular intersecting lines, as if someone has been slashing a pencil across it again and again, or Jackson Pollock has been painting it. (I'm being intentionally vague.) Now let $E'$ and $C$ also be the category of subsets of $R^2$. Let $G_1 \colon E \to E'$ distort each set of examples by moving each point in it to the nearest intersection of these lines. (Assume there is a unique intersection.) Then let $G_2 \colon E' \to C$ find the smallest enclosing grid square as in my section "Galois connections and the idea of smallest enclosing concept" below. Let $G = G_1 ; G_2$.

A little more generally, let $C$ be a category whose objects are either also subsets of $R^2$, or something that's easy to picture as derived, using elementary plane geometry, from these subsets. For example, their boundaries, or their centroids. Let $G$ translate each .....

Informally, the idea is that there's a "background" which is not related to the examples, .....

## Informal justification ##

### 1. Colimits ###

Imagine various views of a physical object such as a leather
armchair. A view of the top of the left arm; a view of the seat; and so
on. Then we can merge these to make a composite view. If the views are
sets, the merging can be described as a [[colimit]] in the category of sets.

By the way, I mention the leather armchair because Goguen used it 
as an example of
merging views in a paper on [[sheaf semantics of concurrent interacting objects]]: [_Sheaf
Semantics for Concurrent Interacting Objects_](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.4296). 

### 2. When different views overlap ###

Such a colimit automatically handles the situation where different
views overlap and agree on their overlaps. In other words, it's a way to
reconstruct as much of the armchair as possible from partial views of it.

(The chart and atlas representation of manifolds is an example of this too
E.g. page 38 of [_Category theory Lecture 6: Colimits_, Jonathan Kirby](http://maths.dept.shef.ac.uk/magic/course_files/143/ctlecture6.pdf). )

#### Interpretation for non&#8211;category-theorists ####

I should explain that colimit is a categorical
construction. Set union is a special case of it. Goguen introduced the
notion that colimits can model "putting together" components into a
system. Many computer-science researchers use them to put together
specifications or program modules into bigger specifications or modules.

### 3. When different overlaps disagree ###

But in real life, different views might disagree on their overlaps. In
this case, we must find a way to combine these views with as little
disagreement as possible. That also feels like a colimit.

### 4. Adjoints as the solution to optimisation problems ###

This ties up with the idea that left adjoints can be regarded as
finding the optimum, or most efficient, solution to a problem. 

(This is an
interpretation I came across in the Wikipedia entry for [_Adjoint functors_]
(http://en.wikipedia.org/wiki/Adjoint_functors): possibly authored by the
Wikipedian called "Functor salad". We can regard the solution as being
an initial object in a category of solutions. Its initiality models the
fact that it contains the least disagreement about overlaps, or what I
think of as the least "strain", of any possible solution.)

### 5. But concepts are not physical objects ###

In the above, I've been talking about reconstructing a single physical
object from different, possibly incompatible, views of it: six blind men
feel an elephant. I don't know whether one should call such reconstruction
"generalisation". But I strongly suspect that there's an analogy with the
construction of a concept from examples of it, if we think of the examples
as different views of the concept.

### 6. Which may be related to... ###

This may be related to the use of colimits for merging ontologies,
and for sensor fusion.

### 7. Categorical perception ###

I'll note that this also feels relevant to the topic of "categorical
perception" introduced by cognitive scientist Stevan Harnad, and to
similar methods of learning classifications. [_Neural network modeling
of categorical perception_, by R.I. Damper and S.R. Harnad](http://eprints.ecs.soton.ac.uk/397/) ; 
[_Categorical Perception_, by S.R.
Harnad ] (http://cogprints.org/3017/1/catperc.html). This
is something I need to think about further: for the moment, I'll
just quote from Harnad's abstract to the second paper:

      Differences can be perceived as gradual and quantitative, as with
      different shades of gray, or they can be perceived as more abrupt and
      qualitative, as with different colors. The first is called continuous
      perception and the second categorical perception. Categorical
      perception (CP) can be inborn or can be induced by learning. Formerly
      thought to be peculiar to speech and color perception, CP turns
      out to be far more general, and may be related to how the neural
      networks in our brains detect the features that allow us to sort the
      things in the world into their proper categories, "warping" perceived
      similarities and differences so as to compress some things into the
      same
      perception and the second categorical perception. Categorical
      perception (CP) can be inborn or can be induced by learning. Formerly
      thought to be peculiar to speech and color perception, CP turns
      out to be far more general, and may be related to how the neural
      networks in our brains detect the features that allow us to sort the
      things in the world into their proper categories, "warping" perceived
      similarities and differences so as to compress some things into the
      same
      category and separate others into different categories.

(The "categorical" here is not connected with category theory but
with categorisation.)

### 8. Concepts as sheaves ###

Goguen's leather-armchair example actually applies not just to views of
the shape itself, but to views of attributes defined on it: e.g. colour,
temperature. This is how he introduces his [[sheaf semantics of concurrent interacting objects]], in which he represents objects as 
[[sheaf|sheaves]] of local observations, these being
mappings from a base space (e.g. the surface of the chair) to attributes.
Perhaps there is a way to represent concepts as sheaves of properties of
examples, or something related.

### 9. The least general generalisation ###

Another idea that I want to capture is that of least
general generalisation. This phrase is used in inductive logic
programming, and was introduced by 
[[Gordon Plotkin]] to describe anti-unification
(_A note on inductive generalization_. In B. Meltzer
and D. Michie, editors, "Machine Intelligence", volume 5, 1970). But I
want to think of it more generally. For instance, if we have a [[poset]]
of concepts, the least general generalisation of two concepts $c1$ and
$c2$ is
a new concept $c$ which implies as much as possible about $c1$ and
$c2$, but
as little as possible about anything else. It contains the information we
need to reconstruct the examples, but as little else as possible.

### 10. Implying as little as possible ###

Similarly, in a category of logical propositions, the product of two
propositions (their conjunction) implies each one, but nothing else. It
contains the information we need to reconstruct the examples, but nothing
else. This property too is something that I believe a generalisation
should have.

### 11. Generalisation as limit-formation ###

This leads me to the intuition that generalisation can be represented
as a limit.

### 12. Change of language. ###

But, contrary to the previous three paragraphs, the
language we normally use to describe concepts is different from that used
to describe examples. For example, in statistical least-squares
regression, the concept is a line plus error information, but the examples
are points.

### 13. Change of language because we want to learn new stuff ###

Moreover, we usually want the concept to be compressed or otherwise
different from just being a conjunction or something analogous. I suppose
there are various reasons for this:
* Saving memory.
* In some generalisers, including most neural nets, stored examples
will interfere just because of the architecture. This may not be a
good thing, but we need to be able to model it.
* Automated discovery. We often want the discovered concept
to say something new about the examples and their similarity. A
mere conjunction can't do that.
* A special case of (c) is when, in inductive logic programming,
we introduce new vocabulary: so-called background knowledge.

### 14. Two different languages, therefore two different categories ###

This difference between the language of examples and the language of
concepts is why I have two categories, $E$ and $C$. And it's also why I want
to model generalisation as an adjunction, rather than as only a limit or
colimit.

### 15. Universal quantification as generalisation? ###

This may be related to the fact that in categorical logic, universal
quantification can be represented as an adjunction. (See the section on
"Lawvere quantifiers: Quantification as adjunction" in [[quantifier]]). 
Can one regard that as a kind of generalisation?

### 16. The impossibility of generalising exactly ###

Now that I've introduced the change of language, a very important
point is that the generalisation functor $G$ from examples to concepts, and
the forgetful functor $F$ from concepts to examples, may 
not be able to translate exactly. In particular, the
language of concepts may not be able to summarise every set of examples
exactly. For example, a linear regression line can't represent
non-colinear points exactly. A categorisation of animals into a class of
animals that resemble sparrows and blackbirds, and another class of
animals that resemble dogs, cats, and horses, will struggle to place
duck-billed platypuses.

### 17. Generalisation as a left adjoint which "does the best it can" ###

In such cases, I think of the adjunction as "doing the
best it can" to create concepts, or to reconstruct examples from concepts.
I think intuitively of mapping from examples to concepts as creating a
kind of "strain". Imagine the sets of examples as points on a plane, and
generalisation as trying to enclose each set with a springy piece of metal
like an artist's flexicurve. The flexicurve can't bend sharply, so the
"flexicurve concept language" makes the set boundaries smoother and wider
than they should be. (Is this intuition worth formalising?)

### 18. Galois connections and the idea of smallest enclosing concept ###

This is related to an explanation of adjunction in terms of [[Galois
connection|Galois connections]], from a chapter in "The Logical foundations of cognition"
edited by John Macnamara and Gonzalo E. Reyes (once accessible on Google
Books, but they've blocked access). The authors describe a category $E$
whose objects are sets in $R^2$, and a subcategory $C$ of 
$E$ constructed as
follows. Draw a grid on $R^2$ of cells of side 1. Then $C$'s objects are shapes
made by combining these grid cells: in other words, unions of squares of
side 1. Let $G:E\to C$ map each set to the smallest union of squares enclosing
it, and $F:C\to E$ map each union of squares to itself. Then $F$ and 
$G$ form a
[[Galois connection]]. That's well known, but it's a nice explanation, and
perhaps a good "intuition pump" for concepts and examples. It makes me
think of generalisation as finding the "smallest enclosing concept" for a
set of examples.

### 19. Galois Connections and intension versus extension ###

Jeremy Gibbons reminded me that 
[[Galois connection|Galois connections]] are
used in [[Formal Concept Analysis]] to map
between the intension (set of
characterising attributes) and the extension (set of examples) of a
concept. See e.g. 
[http://www.alpheccar.org/fr/posts/show/32](http://www.alpheccar.org/fr/posts/show/32) (URL not currently accessible). 
Jeremy felt
that this is morally the same as my machine learning scenario &#8212; inferring
a concept from a set of examples and/or a set of properties.

### 20. Syntax versus semantics ###

My idea probably also related to Lawvere's comment about an adjunction between syntax
and semantics, explained in Peter Smith's article [_The Galois connection between syntax and semantics_](http://www.logicmatters.net/resources/pdfs/Galois.pdf). As [_Patterns in Functional Programming_](http://patternsinfp.wordpress.com)'s posting [_Universal properties and Galois connections_](http://patternsinfp.wordpress.com/2011/02/15/universal-properties-and-galois-connections/) puts it: 

    This construction can be used to translate a problem about 
    the extension  of a concept (that is, an enumeration of 
    its instances) into one about the   intension (that is, the 
    characteristic properties of its instances). It is related to 
    the  observation that "syntax and semantics are adjoint"&#8212;under the 
    analogy that "objects" are sets of mathematical structures, 
    "properties"   are axioms, and the relation is "satisfaction", 
    the models of an axiomatic theory $T$ are included in a set of structures 
    $S$ 
    if and only if the theory $T$ logically entails the minimal 
    axiomatization of $S$.

Thanks to Jeremy and to Viktor Winschel for pointing this out.

### 21. The adjunction between minimal realization and behaviour ###

Hendrik Hilberdink asked whether my generalisation adjunction is related to the adjunction between minimal realization and behaviour of an automaton. This is worth looking into. Perhaps the structure of those categories will give some clues about that of my categories of concepts and examples.