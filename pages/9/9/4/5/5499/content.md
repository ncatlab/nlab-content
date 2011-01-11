+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Contents### {: .clickToReveal}
###Contents### {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include contents]]
=--
=--
=--

# Generalisation as an adjunction
* table of contents
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
mathematical and computational phenomena. I've put this material into nLab because I think it's interesting, and may well be important to machine learning: the categorists and machine-learning experts I've asked agree. So perhaps other readers can supply technical substantiation or refutation. If I can ever get funding then of course I'll do so as well. 

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

Let $G:E\to C$ be a "generalisation" functor that maps each set of
examples to its generalisation as a concept. 

Conversely, let
$F:C\to E$ be a forgetful functor that maps each concept to some
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
illustrate the idea, is a statistical regression line from a least-squares
fit.  $E$'s objects would then be sets of 2-d points to be fitted, and C's
would be regression lines, probably equipped with goodness-of-fit
information.

Some other possibilities for concepts are: high-dimensional vectors formed
by superimposing vectors of property-value pairs in so-called "symbolic
vector architectures" or "holographic reduced representations";  regions
of classification space; logical propositions learnt by induction.

### What other structure might $E$ have? ###

Although I introduced $E$ as a category of sets of
examples, I'm sure there are other possibilities. An obvious one, though
still set-related, is that the objects are weighted sets, where each
weight tells the generaliser how important the corresponding example is.
This probably ties up with fuzzy logic and fuzzy set theory.

## Justification ##

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
and the elephant. I don't know whether one should call such reconstruction
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

### 19. Galois Connections, intension versus extension, and syntax versus semantics ###

Jeremy Gibbons reminded me on reading this that 
[[Galois connection|Galois connections]] are
used in [[Formal Concept Analysis]] to map
between the intension (set of
characterising attributes) and the extension (set of examples) of a
concept. (See e.g. 
[http://www.alpheccar.org/fr/posts/show/32](http://www.alpheccar.org/fr/posts/show/32) ). 
(This is
apparently related to Lawvere's comment about an adjunction between syntax
and semantics:&#160;
[http://lambda-the-ultimate.org/node/3971](http://lambda-the-ultimate.org/node/3971).) 
Jeremy felt
that this is morally the same as my machine learning scenario &#8212; inferring
a concept from a set of examples and/or a set of properties.

That's about as far as I've got; the examples I've so far constructed have the same structure as in 18, and seem to be missing something. I need to think about the structure of $C$ and $E$, and probably get away from $E$ being only a subcategory of Set. One possibility which feels promising (thanks to Victor Winschel for encouraging me on this) is to see whether stochastic logic programming can be formulated in terms of adjoints. 