
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--

This page collects resources related to


* [[Georg Hegel]]

  _Wissenschaft der Logik_ ( _Science of Logic_ )

  Volume 1, _The objective logic_

  1812, 1831

  ([English web version](http://www.marxists.org/reference/archive/hegel/works/hl/), [German web version](http://www.gutenberg.org/cache/epub/6729/pg6729.html), [Wikipedia entry](http://en.wikipedia.org/wiki/Science_of_Logic))

on, not quite _[[logic]]_ in the usual sense, but more something like _[[logos]]_ in the old sense of [[Heraclitus]] (e.g. ([Heidegger 58](#Heidegger58))).

#Contents#
* table of contents
{:toc}

## Survey
 {#Survey}

> With Hegel you're getting what seems to us today a curious package. The whole dynamic (or 'dialectic') of the unfolding of the Logik is prior to any actual thinking, realised in concrete humans. In fact, the world, and that part of it which is human thought, is the Idea (or Spirit) realising itself. I say 'curious', but in a way I'm hearing echoes of this in things Urs is suggesting, as though the universe worked itself out according to type theory. For Hegel one isn't to be a Kantian, where what one theorises about the universe is just how the universe is taken up by the human understanding, with the further idea that this will be limited in certain ways, e.g., no access to the thing-in-itself. For Hegel, the human mind itself is part of the universe and as such part of the unfolding of the Idea/Spirit. $[\cdots]$ It's a dizzying picture which tends either to delight or revolt people. $[$ See at _[[absolute idealism]]_ $]$ ([Corfield](http://nforum.mathforge.org/discussion/4117/the-wiki-history-of-the-universe/?Focus=34343#Comment_34343))


## Topics of Volume One: The objective logic

The following extracts some paragraphs from the text, with comments on how to possibly think about this in terms of [[homotopy type theory]], along the lines that [[William Lawvere]] has been suggesting over the decades. 

The paragraph numbers refer to the numbers as given in the English translation at _[Hegel-by-hypertext](http://www.marxists.org/reference/archive/hegel/index.htm)_ _[Hegel's science of logic](http://www.marxists.org/reference/archive/hegel/works/hl/)_.

### Heraclitus and the notion of Becoming
 {#Heraclitus}

Hegel wrote (according to [this](http://en.wikipedia.org/wiki/Georg_Wilhelm_Friedrich_Hegel#Heraclitus)):

"[[Heraclitus]] is the one who first declared the nature of the infinite and first grasped nature as in itself infinite, that is, its essence as process. The origin of [[philosophy]] is to be dated from Heraclitus. His is the persistent Idea that is the same in all philosophers up to the present day, as it was the Idea of Plato and Aristotle."

"... there is no proposition of Heraclitus which I have not adopted in my logic."


### Formalization of dialectics
 {#OppositesAndUnity}

Hegel famously invokes opposite to the extent of [[paradoxes]], as sources for new phenomena via their synthesis.
On p. 11 of _[Cohesive toposes and Cantor's Lauter Einsen](#LawvereLauterEinsen)_ [[William Lawvere]] proposes that generally such is captured by [[adjoint pairs]] of [[idempotent]] [[monads]]/[[comonads]] ("[[adjoint cylinders]]"), such as

$\flat \dashv \sharp$

[[flat modality]] $\dashv$ [[sharp modality]]

This gives unifying triples of the form

$$
  \array{
    \flat X &\longrightarrow& X &\longrightarrow& \sharp X
    \\
    \\
    opposite\;1 && unity && opposite\;2
  }
  \,.
$$

for any [[type]] $X$.


Several examples of this appear below.

Notice that indeed a fair bit of structure follows from maps of this form.

For instance for the [points-to-pieces transform](cohesive%20topos#CanonicalComparison) induced by the [[shape modality]] $\dashv$ [[flat modality]] dichotmy $\int \dashv \flat$,
we have, as discussed at [tangent cohesion -- Cohesive and differential refinement](#tangent+cohesive+%28∞%2C1%29-topos#CohesiveAndDifferentialRefinement)

$$
  \array{
    &&  \int_{dR} \Omega A && \longrightarrow && \flat_{dR}\Sigma A
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_A}} && \searrow
    \\
    \flat \int_{dR} \Omega A  && && A && && \int \flat_{dR}\Sigma A
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{\int \theta_A}}
    \\
    && \flat A && \longrightarrow && \int A
  }
  \,,
$$




## Book one: The Doctrine of being

### First section: Determinateness (Quality)

#### First chapter

* &#167;86 Pure [[being]] constitutes the beginning, because it is pure thought as well as the undetermined, simple immediate, and the first beginning cannot be anything mediated and further determined.

* &#167;87 Now this pure being is a pure abstraction and thus the absolutely negative which, when likewise taken immediately, is nothing.

* &#167;88 Conversely, nothing, as this immediate, self-same category, is likewise the same as being. The truth of being as well as of nothing is therefore the unity of both; this unity is [[becoming]].


##### A. Being
 {#OnBeingAndBecoming}

* &#167;132 Being, pure being, [...] it has no diversity within itself nor any with a reference outwards.


This is the _[[unit type]]_ $\ast$. 


Indeed, later this is called "Das Eins"  which is maybe indeed better translated as "The Unit" instead of as "The One" as commonly done.


##### B. Nothing

* &#167;133 Nothing, pure nothing: it is simply equality with itself, complete emptiness,

The [[empty type]] $\emptyset$.


##### C. Becoming

* &#167;134 Pure Being and pure nothing are, therefore, the same. What is the truth is neither being nor nothing, but that being &#8212; does not pass over but has passed over &#8212; into nothing, and nothing into being. But it is equally true that they are not undistinguished from each other, that, on the contrary, they are not the same, that they are absolutely distinct, and yet that they are unseparated and inseparable and that each immediately vanishes in its opposite. Their truth is therefore, this movement of the immediate vanishing of the one into the other: becoming, a movement in which both are distinguished, but by a difference which has equally immediately resolved itself.

According to the formalization of such unity of opposites as
[above](#OppositesAndUnity) we might think of this as the
universal factorization

$$
  \array{
    \emptyset &\longrightarrow& X &\longrightarrow& \ast 
    \\
    \\
    nothing && becoming && being
  }
$$

of the factorization of the unique [[function]] from the [[empty type]] to the [[unit type]] through any other [[type]] $X$.


Indeed, later it says:

* &#167;174 there is nothing which is not an intermediate state between being and nothing.

###### 1. Unity of Being and Nothing

###### $\;\;$ Remark 1

###### $\;\;$ Remark 2

###### $\;\;$ Remark 3

###### $\;\;$ Remark 4

* &#167;174 there is nothing which is not an intermediate state between being and nothing.

The universal factorization

$$
  \array{
    \emptyset &\longrightarrow& X &\longrightarrow& \ast 
    \\
    \\
    nothing && becoming && being
  }
$$

of the factorization of the unique [[function]] from the [[empty type]] to the [[unit type]] through any other [[type]] $X$.



###### 2. Moments of Becoming

###### 3. Sublating of Becoming

#### Second chapter. Determinate Being (Dasein)

##### A. Dasein as such

###### a. Dasein &#252;berhaupt

###### b. Qualit&#228;t

###### c. Etwas

##### B. Die Endlichkeit

##### C. Die Unendlichkeit

#### Third chapter. Das F&#252;rsichsein

##### A. Das F&#252;rsichsein als solches

##### B. Eins und Vieles.

###### a. Das Eins an ihm selbst

###### b. Das Eins und das Leere

###### c. Viele Eins. Repulsion. / Many ones. Repulsion.

* &#167;340 The one and the void constitute the first stage of the determinate being of being-for-self. Each of these moments has negation for its determination and is at the same time posited as a determinate being; according to the former determination the one and the void are the relation of negation to negation as of an other to its other: the one is negation in the determination of being, and the void is negation in the determination of non-being.

Das Eins (the One): $\ast$ [[unit type]]

Das Leere (the void): $\emptyset$ [[empty type]] ( _leere Menge_ !)

Negation $(\not X) \coloneqq (X \to \emptyset)$

$\ast \simeq \not \emptyset$.

* &#167;342 the one repels itself from itself. The negative relation of the one to itself is repulsion.

* &#167;343 This repulsion as thus the positing of many ones but through the one itself, is the one's own coming-forth-from-itself but to such outside it as are themselves only ones. This is repulsion according to its Notion, repulsion in itself. The second repulsion is different from it, it is what is immediately suggested to external reflection: repulsion not as the generation of ones, but only as the mutual repelling of ones presupposed as already present. 

Suppose we have a [[shape modality]] $\int$ but without the assumption that it preserves finite product types. (This is what the term "[[shape of an (infinity,1)-topos|shape]]" really refers to).

Then given just the [[empty type]] $\emptyset$ and the [[unit type]] $\ast$, there is one new [[type]] to be formed (since necessarily $\int \emptyset \simeq \emptyset$) and this is

$$
  \int \ast 
$$

Below we see that this, being a [[discrete type]], is what Hegel describes with "repulsion": The points in $\int \ast$ do not attract/cohese, they are different and repel.

At the same time, being a [[discrete type]] it is necessarily a [[homotopy colimit]] of copies of the [[unit type]] (see [here](limit+in+a+quasi-category#Tensoring))

$$
  \int \ast \simeq \underset{\longrightarrow}{\lim}_I \ast
$$

where the [[diagram]] $I$ that the colimit is over is $I = &#643; \ast$ itself.

For a similar argument see Lawvere's  _[Cohesive toposes and Cantor's Lauter Einsen ](#LawvereLauterEinsen))_. On p. 6 there is suggested that the unity of opposites "all elements of a set are indistinguishable and yet distinct" is captured by the fact that both

$\flat X$ as well as $\sharp X$ have the same image under $\flat$.

##### C. Repulsion und Attraktion

###### a. Ausschli&#223;en des Eins.

###### b. Das Eine Eins der Attraktion

###### c. Die Beziehung der Repulsion und der Attraktion

###### Remark: The Kantian Construction of Matter from the Forces of Attraction and Repulsion


* &#167;374 Kant, as we know, constructed matter from the forces of attraction and repulsion, or at least he has, to use his own words, set up the metaphysical elements of this construction.

Not about actual [[forces]] in [[matter]] so much as about what makes the points in the [[continuum]] both stay apart (repulsion) and at the same time hang together (attraction/cohesion).



### Second section. The magnitude

#### First chapter. Die Quantit&#228;t / The quantity

##### A. Die reine Quantit&#228;t


###### On attraction / cohesion 

* &#167;395 Attraction is in this way the moment of continuity in quantity.

attraction is what holds stuff together, hence this is the idea of [[cohesion]]

if $X$ has continuity then the [[shape modality]] $\int X$ is the result of letting things collaps under their cohesion/attraction


###### On discreteness and repulsion

* &#167;397 In continuity, therefore, magnitude immediately possesses the moment of discreteness &#8212; repulsion, as now a moment in quantity. 

continuous object $X$ possesses moment 
of [[discrete object|discreteness]]= [[flat modality]] $\flat X$

* &#167;398 Quantity is the unity of these moments of continuity and discreteness,

the [[flat modality]] [[counit of a comonad|co-unit]]:

$$
  quantity
  \;\colon\;
  \array{ 
    \flat X &\longrightarrow& X
    \\
    {moment\;of \atop discreteness} && continuity
  } 
$$

We may regard a [[morphism]] as the collection of its [[homotopy fibers]] and that the homotopy fiber of $\flat X \to X$ is the [de Rham coefficient object](cohesive+(infinity,1)-topos+--+structures#deRhamCohomology) $\flat_{dR} X$.


so 

$$
  \array{
    \flat X &\longrightarrow& X &\longrightarrow& \int X
    \\
    repulsion && continuity && attraction
  }
$$


##### B. Kontinuirliche und diskrete Gr&#246;&#223;e.

###### On the continuum

* &#167;400 Mathematics, on the other hand, rejects a metaphysics which would make time consist of points of time; space in general &#8212; or in the first place the line &#8212; consist of points of space; the plane, of lines; and total space of planes. It allows no validity to such discontinuous ones. Even though, for instance, in determining the magnitude of a plane, it represents it as the sum of infinitely many lines, this discreteness counts only as a momentary representation, and the sublation of the discreteness is already implied in the infinite plurality of the lines, since the space which they are supposed to constitute is after all bounded.

The [[continuum]].


> Diese Antinomie besteht allein, darin da&#223; die Diskretion eben so sehr als die Kontinuit&#228;t behauptet werden mu&#223;. Die einseitige Behauptung der Diskretion giebt das unendliche oder absolute Getheiltseyn, somit ein Untheilbares zum Princip; die einseitige Behauptung der Kontinuit&#228;t dagegen die unendliche Theilbarkeit.


###### On space, time, matter

* &#167;432 Space, time, matter, and so forth are continuous magnitudes 




##### C. Begrenzung der Quantit&#228;t 

#### Second chapter. Quantum





## Book two: The doctrine of essence

### Reflection

#### Section 1. Essence as Reflection within Itself

##### Chapter 1 Illusory Being
 
##### A The essential and the unessential

##### B Illusory being

##### C Reflection

##### Chapter 2 The Essentialities or Determination of Reflection

###### $\;\;$ Remark $A = A$

* &#167;863 Thus the essential category of identity is enunciated in the proposition: everything is identical with itself, A = A.

The reflector(!) [[term constructor]] in an [[identity type]]. This is more explicit below at _[Identity](#Identity)_.

###### A Identity
 {#Identity}

* &#167;869 Essence is therefore simple identity with self.

* &#167;869 This identity-with-self is the immediacy of reflection.

The reflector(!) [[term constructor]] in an [[identity type]].  Below this is called te _[First original law of thought](#FirstOriginalLawOfThought)_.

###### $\;\;$ Remark 1: Abstract identity

###### $\;\;$ Remark 2: First original law of thought
 {#FirstOriginalLawOfThought}

* &#167;875 In this remark, I will consider in more detail identity as the law of identity which is usually adduced as the first law of thought.

  This proposition in its positive expression $A = A$ is, in the first instance, nothing more than the expression of an empty tautology. 

The reflector [[term constructor]] in an [[identity type]].

###### B Difference

###### $\;\;$ (a) Absolute difference

###### $\;\;$ (b) Diversity

###### $\;\;$ Remark: The Law of Diversity


* &#167;903 All things are different; or: there are no two things like each other.

Reminiscent of [[identity types]] in [[intensional type theory]].

###### C Contradiction

* &#167;903 When all the conditions of a fact are present, it enters into Existence.


* &#167;1035 The fact emerges from the ground. It is not grounded or posited by it in such a manner that ground remains as a substrate; on the contrary, the positing is the movement of the ground outwards to itself and its simple vanishing.

  $[..]$

  This immediacy that is mediated by ground and condition and is self-identical through the sublating of mediation, is Existence.

[[term introduction]] in [[natural deduction]]



### Third section. The measure.


## Related entries

* [[being]], [[becoming]]

## References

* _Enzyklop&#228;die der philosophischen Wissenschaften im Grundrisse_ (1830) W. Bonsiepen und H.-C. Lucas (eds.) in _Gesammelte Werke_, Rheinisch-Westf&#228;lischen Akademie der Wissenschaften, and xx. Hamburg: Felix Meiner, 1992 ( Bonsiepen/Lucas 1992).

  [Encyclopedia of the Philosophical Sciences in Basic Outline, Part I: Science of Logic](http://ndpr.nd.edu/news/24778-encyclopedia-of-the-philosophical-sciences-in-basic-outline-part-i-science-of-logic/)
 {#EPSBOI}

* [[Martin Heidegger]], _Hegel and the Greeks_, From Conference of the Academy of Sciences at Heidelberg, July 26, 1958 ([web](http://www.morec.com/hegelgre.htm))
  {#Heidegger58}


* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_
 {#LawvereComo}

* [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_
  {#LawvereLauterEinsen}