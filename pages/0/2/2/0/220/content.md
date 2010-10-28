
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--


_This is Part II of an exposition by [[Todd Trimble]] on [[ETCS]]_.

See also

* Part I, [[Trimble on ETCS I|ZFC and ETCS]]

* Part III, [[Trimble on ETCS III|ETCS: Building joins and coproducts]]

***

+--{.query}
**Editing help wanted**

[This is what it is supposed to look like](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic/).

Starting with the raw Wordpress text, I first replaced "$latex" with "$", which fixed >300 instances. The next big fix is to replace "<blockquote>" with "$" and "</blockquote>" with "$". That puts it into pretty good shape.

Replace "\mbox" with "\:\text"

Some remaining issues:

* Need a replacement for \cong

[[Jon Awbrey]]: Maybe this is an old note, but I'm reading \cong okay.  Otherwise, I think I used to use an underlined \asymp or something, can't recall, will check.

* Etc.

The easy thing to do is to Edit this page, copy the text to your favorite editor, find/replace, paste text back here.

* [[Jon Awbrey]]: I think I took care of all the remaining formatting issues, but a 2nd or 3rd pair of eyes would be good.

* Jon Phillips: I'm a 2nd pair of eyes - corrected a couple of minor things (hopefully my changes will come out as I expect)

=--

## ETCS : Internalizing the logic ##

This post is a continuation of the discussion of "the elementary theory of the category of sets" [ETCS] which we had begun last time, [here](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets/) and in the comments which followed.  My thanks go to all who commented, for some useful feedback and thought-provoking questions.
 
Today I'll describe some of the set-theoretic operations and "internal logic" of ETCS.  I have a feeling that some people are going to love this, and some are going to hate it.  My main worry is that it will leave some readers bewildered or exasperated, thinking that category theory has an amazing ability to make easy things difficult.

* __An aside:__ has anyone out there seen the book _Mathematics Made Difficult_? It's probably out of print by now, but I recommend checking it out if you ever run into it --- it's a kind of extended in-joke which pokes fun at category theory and abstract methods generally.  Some category theorists I know take a dim view of this book;  I for my part found certain passages hilarious, in some cases making me laugh out loud for five minutes straight.  There _are_ category-theory-based books and articles out there which cry out for parody!

In an attempt to nip my concerns in the bud, let me remind my readers that there are major differences between the way that standard set theories like ZFC treat membership and the way ETCS treats membership, and that differences at such a fundamental level are bound to propagate throughout the theoretical development, and impart a somewhat different character or feel between the theories.  The differences may be summarized as follows:

* Membership in ZFC is a _global_ relation between objects of the _same_ type (sets).

* Membership in ETCS is a _local_ relation between objects of _different_ types ("generalized" elements or functions, and sets).

Part of what we meant by "local" is that an element _per se_ is always considered relative to a particular set to which it belongs;  strictly speaking, as per the discussion last time, the same element is never considered as belonging to two different sets.  That is, in ETCS, an (ordinary) element of a set $A$ is defined to be a morphism $x : 1 \to A$;  since the codomain is fixed, the same morphism cannot be an element $1 \to B$ of a different set $B$.  This implies in particular that in ETCS, there is no meaningful global intersection operation on sets, which in ZFC is defined by:

$$A \cap B = \{ x : (x \in A) \:\wedge\: (x \in B) \}$$

Instead, in ETCS, what we have is a _local_ intersection operation on _subsets_ $A \hookrightarrow X, B \hookrightarrow X$ of a set.  But even the word "subset" requires care, because of how we are now treating membership.  So let's back up, and lay out some simple but fundamental definitions of terms as we are now using them.
 
Given two monomorphisms $i : A \to X, j : B \to X$, we write $i \subseteq j$ ($A \subseteq B$ if the monos are understood, or $A \subseteq_X B$ if we wish to emphasize this is local to $X$) if there is a morphism $k : A \to B$ such that $i = j k$.  Since $j$ is monic, there can be at most one such morphism $k$;  since $i$ is monic, such $k$ must be monic as well.  We say $i, j$ _define the same subset_ if this $k$ is an isomorphism.  So: subsets of $X$ are defined to be isomorphism classes of monomorphisms into $X$.  As a simple exercise, one may show that monos $i, j$ into $X$ define the same subset if and only if $i \subseteq j$ and $j \subseteq i$.  The (reflexive, transitive) relation $\subseteq_X$ on monomorphisms thus induces a reflexive, transitive, antisymmetric relation, _i.e._, a partial order on subsets of $X$.
 
Taking some notational liberties, we write $A \subseteq X$ to indicate a subset of $X$ (as isomorphism class of monos).  If $x : U \to X$ is a generalized element, let us say $x$ _is in_ a subset $A \subseteq X$ if it factors (evidently uniquely) through any representative mono $i : A \to X$, _i.e._, if there exists $x' : U \to A$ such that $x = i x'$.  Now the _intersection_ of two subsets $A \subseteq X$ and $B \subseteq X$ is defined to be the subset $A \cap B \subseteq X$ defined by the pullback of any two representative monos $i : A \to X, j : B \to X$.  Following the "Yoneda principle", it may equivalently be defined up to isomorphism by specifying its generalized elements:

$$A \:\cap\: B :=_i \{ x \in X : (x is in A) \:\wedge\: (x is in B) \}.$$

Thus, intersection works essentially the same way as in ZFC, only it's _local_ to subsets of a given set.
 
While we're at it, let's reformulate the power set axiom in this language: it says simply that for each set $B$ there is a set $P(B)$ and a subset $\in_B \subseteq B \times P(B)$, such that for any relation $R \subseteq B \times A$, there is a unique "classifying map" $\chi_R : A \to P(B)$ whereby, under $1_B \times \chi_R : B \times A \to B \times P(B)$, we have

$$R = (1_B \times \chi_R)^{-1} (\in_B).$$

The equality is an equality between subsets, and the inverse image on the right is defined by a pullback.  In categorical set theory notation,

$$R = \{ \langle b, a \rangle \in B \times A : b \in_B \chi_R(a) \}.$$

Hence, there are natural bijections

$$\displaystyle \frac{R \subseteq B \times A}{A \to P(B)} \qquad \frac{R \subseteq B \times A}{B \to P(A)}$$

between subsets and classifying maps.  The subset corresponding to $\phi : A \to P(B)$ is denoted $\left[\phi\right] \subseteq B \times A$ or $\left[\phi\right] \subseteq A \times B$, and is called the _extension_ of $\phi$.
 
The set $P(1)$ plays a particularly important role;  it is called the "subset classifier" because subsets $A \subseteq X$ are in natural bijection with functions $\chi : X \to P(1)$.  [_Cf._ classifying spaces in the theory of fiber bundles.]
 
In ordinary set theory, the role of $P(1)$ is played by the 2-element set $\{ f, t \}$.  Here subsets $A \subseteq X$ are classified by their characteristic functions $\chi_A : X \to \{ f, t \}$, defined by $\chi_A(x) := t$ iff $x \in A$.  We thus have $A = \chi_A^{-1}(t)$;  the elementhood relation $\in_1 \hookrightarrow 1 \times P(1)$ boils down to $t : 1 \to P(1)$.  Something similar happens in ETCS set theory:
 
__Lemma 1.__  The domain of elementhood $\in_1 \to 1 \times P(1) \cong P(1)$ is terminal.
 
__Proof.__  A map $X \to \in_1$, that is, a map $\chi : X \to P(1)$ which is in $\in_1 \subseteq P(1)$, corresponds exactly to a subset $\chi^{-1}(\in_1) \subseteq X$ which contains all of $X$ (_i.e._, the subobject $1_X : X \subseteq X$).  Since the only such subset is $1_X$, there is exactly one map $X \to \in_1$.  $\Box$
 
Hence elementhood $\in_1 \subseteq 1 \times P(1)$ is given by an element $t : 1 \to P(1)$.  The power set axiom says that a subset $A \subseteq X$ is retrieved from its classifying map $\chi_A : X \to P(1)$ as the pullback $\chi^{-1}_A (t) \subseteq X$.
 
Part of the power of, well, power sets is in a certain dialectic between external operations on subsets and internal operations on $P(1)$;  one can do some rather amazing things with this.  The intuitive (and pre-axiomatic) point is that if $C$ has finite products, equalizers, and power objects, then $P(1)$ is a [representing
object](http://topologicalmusings.wordpress.com/2008/07/12/basic-category-theory-iii-representability-adjoints-and-the-yoneda-lemma) for the functor

$$Sub : C^{op} \to Set$$

which maps an object $X$ to the collection of subobjects of $X$, and which maps a morphism ("function") $f : X \to Y$ to the "inverse image" function $f^{-1} : Sub(Y) \to Sub(X)$, that sends a subset $j : B \subseteq Y$ to the subset $f^{-1}(B) \subseteq X$ given by the pullback of the arrows $f : X \to Y$, $ j : B \subseteq Y$.  By the [Yoneda
lemma](http://topologicalmusings.wordpress.com/2008/07/12/basic-category-theory-iii-representability-adjoints-and-the-yoneda-lemma), this representability means that _external_ natural operations on the $Sub(X)$ correspond to _internal_ operations on the object $P(1)$.  As we will see, one can play off the external and internal points of view against each other to build up a considerable amount of logical structure, enough for just about any mathematical purpose.

* __Remark.__  A category satisfying just the first three axioms of ETCS, namely existence of finite products, equalizers, and power objects, is called an (elementary) __topos__.  Most or perhaps all of this post will use just those axioms, so we are really doing some elementary topos theory.  As I was just saying, we can build up a tremendous amount of logic internally within a topos, but there's a catch:  this logic will be in general intuitionistic.  One gets classical logic (including law of the excluded middle) if one assumes strong extensionality [where we get the definition of a well-pointed topos].  Topos theory has a somewhat fearsome reputation, unfortunately;  I'm hoping these notes will help alleviate some of the sting.

To continue this train of thought:  by the Yoneda lemma, the representing isomorphism

$$\displaystyle \theta : \hom(-, P(1)) \stackrel{\sim}{\to} Sub(-)$$

is determined by a universal element $\theta_{P(1)}(1_{P(1)})$, _i.e._, a subset of $P(1)$, namely the mono $t : 1 \to P(1)$.  In that sense, $t : 1 \to P(1)$ plays the role of a _universal subset_.  The Yoneda lemma implies that external natural operations on general posets $Sub(X)$ are completely determined by how they work on the universal subset.

### Internal Meets ###

To illustrate these ideas, let us consider intersection.  Externally, the intersection operation is a natural transformation

$$\cap_X : Sub(X) \times Sub(X) \to Sub(X).$$

This corresponds to a natural transformation

$$\hom(X, P(1)) \times \hom(X, P(1)) \to \hom(X, P(1))$$

which (by Yoneda) is given by a function $\wedge : P(1) \times P(1) \to P(1)$.  Working through the details, this function is obtained by putting $X = P(1) \times P(1)$ and chasing

$$\langle \pi_1, \pi_2 \rangle \in \hom(P(1) \times P(1), P(1)) \times \hom(P(1) \times P(1), P(1))$$

through the composite

$$\hom(X, P(1)) \times \hom(X, P(1)) \stackrel{\sim}{\to} Sub(X) \times Sub(X) \stackrel{\cap}{\to} Sub(X) \stackrel{\sim}{\to} \hom(X, P(1)).$$

Let's analyze this bit by bit.  The subset $\left[\pi_1\right] = \pi_{1}^{-1}(t) \subseteq P(1) \times P(1)$ is given by

$$t \times id : 1 \times P(1) \to P(1) \times P(1),$$

and the subset $\left[\pi_2\right] = \pi_{2}^{-1}(t) \subseteq P(1) \times P(1)$ is given by

$$id \times t : P(1) \times 1 \to P(1) \times P(1).$$

Hence $\left[\pi_1\right] \cap \left[\pi_2\right] \subseteq P(1) \times P(1)$ is given by the pullback of the functions $t \times id$ and $id \times t$, which is just

$$t \times t : 1 \times 1 \to P(1) \times P(1).$$

The map $\wedge : P(1) \times P(1) \to P(1)$ is thus defined to be the classifying map of $t \times t : 1 \times 1 \subseteq P(1) \times P(1)$.
 
To go from the internal meet $\wedge : P(1) \times P(1) \to P(1)$ back to the external intersection operation, let $A \subseteq X, B \subseteq X$ be two subsets, with classifying maps $\chi_A, \chi_B : X \to P(1)$.  By the definition of $\wedge$, we have that for all generalized elements $x \in X$

$$\chi_A(x) \:\wedge\: \chi_B(x) = t \quad if and only if \quad \langle \chi_A(x), \chi_B(x) \rangle = \langle t, t \rangle$$

(where the equality signs are interpreted with the help of equalizers).  This holds true iff $x$ is in the subset $A \subseteq X$ and is in the subset $B \subseteq X$, _i.e._, if and only if $x$ is in the subset $A \cap B \subseteq X$.  Thus $\chi_A \wedge \chi_B$ is indeed the classifying map of $A \cap B \subseteq X$.  In other words, $\chi_{A \cap B} = \chi_A \wedge \chi_B$.
 
A by-product of the interplay between the internal and external is that the internal intersection operator

$$\wedge : P(1) \times P(1) \to P(1)$$

is the meet operator of an internal [meet-semilattice](http://topologicalmusings.wordpress.com/2008/04/02/toward-stone-duality-posets-and-meets) structure on $P(1)$:  it is commutative, associative, and idempotent (because that is true of external intersection).  The identity element for $\wedge$ is the element $t : 1 \to P(1)$.  In particular, $P(1)$ carries an internal poset structure:  given generalized elements $u, v : A \to P(1)$, we may define

$$u \leq v \quad if and only if \quad u = u \wedge v$$

and this defines a reflexive, symmetric, antisymmetric relation $\left[\leq\right] \subseteq P(1) \times P(1)$:

$$\left[\leq\right] :=_i \{ \langle u, v \rangle \in P(1) \times P(1) : u = u \wedge v\},$$

equivalently described as the equalizer

$$\left[\leq\right] \to P(1) \times P(1) \stackrel{\to}{\to} P(1)$$

of the maps $\pi_1 : P(1) \times P(1) \to P(1)$ and $\wedge : P(1) \times P(1) \to P(1)$.  We have that $u \leq v$ if and only if $\left[u\right] \subseteq \left[v\right]$.

### Internal Implication ###

Here we begin to see some of the amazing power of the interplay between internal and external logical operations.  We will prove that $P(1)$ carries an internal Heyting algebra structure (ignoring joins for the time being).
 
Let's recall the notion of [Heyting
algebra](http://topologicalmusings.wordpress.com/2008/04/08/distributivity-topology-and-heyting-algebras) in ordinary naive set-theoretic terms:  it's a lattice $P$ that has a material implication operator "$\Rightarrow$" such that, for all $x, y, z \in P$,

$$x \wedge y \leq z \quad if and only \quad if x \leq y \Rightarrow z.$$

Now:  by the universal property of $P(1)$, a putative implication operation $\Rightarrow : P(1) \times P(1) \to P(1)$ is uniquely determined as the classifying map of its inverse image $(\Rightarrow)^{-1}(t) \subseteq P(1) \times P(1)$, whose collection of generalized elements is

$$\{ \langle u, v \rangle \in P(1) \times P(1) : (u \Rightarrow v) = t\}$$

Given $\langle u, v \rangle : A \to P(1) \times P(1)$, the equality here is equivalent to

$$t \leq u \Rightarrow v$$

(because $t : 1 \to P(1)$ is maximal), which in turn is equivalent to

$$t \wedge u = u \leq v$$

This means we should define $\Rightarrow : P(1) \times P(1) \to P(1)$ to be the classifying map of the subset

$$\left[\leq\right] \subseteq P(1) \times P(1).$$

__Theorem 1.__  $P(1)$ admits internal implication.
 
__Proof.__  We must check that for any three generalized elements $u, v, w : A \to P(1)$, we have

$$w \leq u \Rightarrow v \quad if and only \quad if w \wedge u \leq v.$$

Passing to the external picture, let $\left[u\right], \left[v\right], \left[w\right]$ be the corresponding subsets of $A$.  Now:  according to how we defined $\Rightarrow,$ a generalized element $e \in A$ is in $\left[u \Rightarrow v\right]$ if and only if $u(e) \leq v(e)$.  This applies in particular to any monomorphism $e: \left[w\right] \to A$ that represents the subset $ \left[w\right] \subseteq A$.
 
__Lemma 2.__  The composite

$$\displaystyle u(e) = (\left[w\right] \stackrel{e}{\to} A \stackrel{u}{\to} P(1))$$

is the classifying map of the subset $\left[w\right] \cap \left[u\right] \subseteq \left[w\right]$.
 
__Proof.__  As subsets of $\left[w\right]$,

$$(u e)^{-1}(t) = e^{-1} u^{-1}(t) = e^{-1}(\left[u\right]) = \left[w\right] \cap \left[u\right]$$

where the last equation holds because both sides are the subsets defined as the pullback of two representative monos $e : \left[w\right] \to A$, $i : \left[u\right] \to A$.  $\Box$
 
Continuing the proof of Theorem&#160;1, we see by Lemma&#160;2 that the condition $u(e) \leq v(e)$ corresponds externally to the condition

$$\left[w\right] \cap \left[u\right] \subseteq \left[w\right] \cap \left[v\right]$$

and this condition is equivalent to $\left[w\right] \cap \left[u\right] \subseteq \left[v\right]$.

Passing back to the internal picture, this is equivalent to $w \wedge u \leq v$, and the proof of Theorem&#160;1 is complete.  $\Box$

### Cartesian Closed Structure ###

Next we address a [comment](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets/#comment-469) made by "James", that a category satisfying the ETCS axioms is [cartesian
closed](http://topologicalmusings.wordpress.com/2008/06/29/basic-category-theory-ii).  As everything else in this article, this uses only the fact that such a category is a topos:  has finite products, equalizers, and "power sets".
 
__Proposition 1.__  If $A, B$ are "sets", then $P(A \times B)$ represents an exponential $P(B)^A.$
 
__Proof.__  By the power set axiom, there is a bijection between maps into the power set and relations:

$$\displaystyle \frac{\phi : X \to P(A \times B)}{R \subseteq X \times (A \times B)}$$

which is natural in $X$.  By the same token, there is a natural bijection

$$\displaystyle \frac{R \subseteq (X \times A) \times B}{\phi' : X \times A \to P(B)}.$$

Putting these together, we have a natural isomorphism $\hom(-, P(A \times B)) \cong \hom(- \times A, P(B))$

and this representability means precisely that $P(A \times B)$ plays the role of an exponential $P(B)^A$.  $\Box$
 
__Corollary 1.__  $P(A) \cong P(1)^A$.  $\Box$
 
The [universal
element](http://topologicalmusings.wordpress.com/2008/07/12/basic-category-theory-iii-representability-adjoints-and-the-yoneda-lemma/) of this representation is an evaluation map $A \times P(A) \to P(1)$, which is just the classifying map of the subset $\in_A \subseteq A \times P(A)$.
 
Thus, $P(B)^A \cong P(A \times B)$ represents the set of all functions $\phi : A \to P(B)$ (that is, relations from $A$ to $ B$).  This is all we need to continue the discussion of internal logic in this post, but let's also sketch how we get full cartesian closure.  [Warning: for those who are not comfortable with categorical reasoning, this sketch could be rough going in places.]
 
As per [our](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets/#comment-469) [discussion](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets/#comment-470), we want to internalize the set of such relations which are graphs of functions, _i.e._, maps $\phi$ where each $\phi(a) \subseteq B$ is a singleton, in other words which factor as

$$\displaystyle A \to B \stackrel{\sigma}{\to} P(B)$$

where $\sigma : B \to P(B)$ is the singleton mapping:

$$b \mapsto \{ b \} = \{ c \in B: b = c \}.$$

We see from this set-theoretic description that $\sigma : B \to P(B)$ classifies the equality relation

$$\{ \langle b, c \rangle \in B \times B: b = c \} \subseteq B \times B$$

which we can think of as either the equalizer of the pair of maps $\pi_1, \pi_2 : B \times B \to B$ or, what is the same, the diagonal map $\delta_B = \langle 1_B, 1_B \rangle : B \to B \times B$.
 
Thus, we put $\sigma = \chi_{\delta} : B \to P(B)$, and it is not too hard to show that the singleton mapping $\sigma$ is a monomorphism.  As usual, we get this monomorphism as the pullback $\chi_{\sigma}^{-1}(t)$ of $t : 1 \to P(1)$ along _its_ classifying map $\chi_{\sigma} : P(B) \to P(1)$.
 
Now: a right adjoint such as $ (-)^A$ preserves all limits, and in particular pullbacks, so we ought then to have a pullback

$$
\begin{matrix}
  B^{\mathrlap{A}} & \longrightarrow & 1^{\mathrlap{A}} \\
  \mathllap{\scriptsize{\sigma^A}}\downarrow & & \downarrow\mathrlap{\scriptsize{t^\A}} \\
  P(B)^{\mathrlap{A}} & \underset{\chi_\sigma^A}{\longrightarrow} & P(1)^{\mathrlap{A}}
 \end{matrix}
$$

Of course, we don't even have $B^A$ yet, but this should give us an idea:  _define_ $\sigma^A$, and in particular its domain $B^A$, by taking the pullback of the right-hand map along the bottom map.  In case there is doubt, the map on the bottom is defined Yoneda-wise, applying the isomorphism

$$\hom(P(B)^A \times A, P(1)) \cong \hom(P(B)^A, P(1)^A)$$

to the element in the hom-set (on the left) given by the composite

$$\displaystyle P(B)^A \times A \stackrel{ev}{\to} P(B) \stackrel{\chi_\sigma}{\to} P(1).$$

The map on the right of the pullback is defined similarly.  That this recipe really gives a construction of $B^A$ will be left as an exercise for the reader.

### Universal Quantification ###

As further evidence of the power of the internal-external dialectic, we show how to internalize [[universal quantification]].
 
As we are dealing here now with _predicate_ logic, let's begin by defining some terms as to be used in ETCS and topos theory:

* An _ordinary predicate_ of type $A$ is a function $\phi : A \to P(1)$.  Alternatively, it is an ordinary element $\phi' : 1 \to P(1)^A \cong P(A)$.  It corresponds (naturally and bijectively) to a subset $\left[\phi\right]: S \subseteq A$.

* A _generalized predicate_ of type $A$ is a function $\phi' : X \to P(A) \cong P(1)^A$.  It may be identified with (corresponds naturally and bijectively to) a function $\phi : X \times A \to P(1)$, or to a subset $\left[\phi\right] : S \subseteq X \times A$.

We are trying to define an operator $\forall_A$ which will take a predicate of the form $\phi : X \times A \to P(1)$ [conventionally written $\phi(x, a)$] to a predicate $\forall_A \phi : X \to P(1)$ [conventionally written $ \forall_{a \in A} \phi(x, a)$].  Externally, this corresponds to a natural operation which takes subsets of $X \times A$ to subsets of $X$. _Internally_, it corresponds to an operation of the form:

$$\forall_A : P(A) \cong P(1)^A \to P(1).$$

This function is determined by the subset $(\forall_A)^{-1}(t) \subseteq P(1)^A$, defined elementwise by

$$\{ \phi \in P(1)^A : \forall_A \phi = t\}.$$

Now, in ordinary logic, $\forall_{a \in A} \phi(a)$ is true if and only if $\phi(a)$ is true for all $a \in A$, or, in slightly different words, if $\phi : A \to P(1)$ is constantly true over all of $A$:

$$\displaystyle \phi = (A \stackrel{!}{\to} 1 \stackrel{t}{\to} P(1)).$$

The expression on the right (global truth over $A$) corresponds to a function $t_A : 1 \to P(1)^A$, indeed a monomorphism since any function with domain $1$ is monic.  Thus we are led to define the desired quantification operator $\forall_A : P(1)^A \to P(1)$ as the classifying map of $t_A : 1 \subseteq P(1)^A$.
 
Let's check how this works externally.  Let $\phi : X \to P(1)^A$ be a generalized predicate of type $A$.  Then according to how $\forall_A$ has just been defined, $\forall_A \phi : X \to P(1)$ classifies the subset

$$\displaystyle \{ x \in X: \phi(x, -) = t_A : A \to P(1)) \} \subseteq X$$

There is an interesting adjoint relationship between universal quantification and substitution (aka "pulling back").  By "substitution", we mean that given any predicate $\psi : X \to P(1)$ on $X$, we can always pull back to a predicate on $X \times A$ (substituting in a dummy variable $a$ of type $A$, forming _e.g._ $\psi(x) \wedge \left[a=a\right]$) by composing with the projection $\pi : X \times A \to X$.  In terms of subsets, substitution along $A$ is the natural external operation

$$(\left[\psi\right] \subseteq X) \mapsto (\left[\psi\right]\times A \subseteq X \times A).$$

Then, for any predicate $\phi : X \times A \to P(1)$, we have the adjoint relationship

$$\left[\psi\right] \times A \subseteq \phi \quad if and only if \quad \left[\psi\right] \subseteq \forall_A \phi$$

so that substitution along $A$ is left adjoint to universal quantification along $A$.  This is easy to check;  I'll leave that to the reader.

### Internal Intersection Operators ###

Now we put all of the above together, to define an internal intersection operator

$$\bigcap : PPX \to PX$$

which intuitively takes an element $1 \to PPX$ (a family $F$ of subsets of $X$) to its intersection $1 \to PX$, as a subset $\bigcap F \subseteq X$.
 
Let's first write out a logical formula which expresses intersection:

$$x \in \bigcap F \quad if and only if \quad \forall_{S \in PX} (S \in F) \Rightarrow (x \in S).$$

[[Jon Awbrey]]:  There seemed to be an orphan right bracket in the above line, also on your blog.

We have all the ingredients to deal with the logical formula on the right:  we have an implication operator "$\Rightarrow$" as part of the internal Heyting algebra structure on $P(1)$, and we have the quantification operator "$\forall_{PX}$".  The atomic expressions $(S \in F)$ and $(x \in S)$ refer to internal elementhood:  $(x \in S)$ means $\langle x, S \rangle \in X \times PX$ is in $\in_{X} \subseteq X \times PX$, and $(S \in F)$ means $\langle S, F \rangle \in PX \times PPX$ is in $\in_{PX} \subseteq PX \times PPX$.

[[Jon Awbrey]]:  I didn't know what to do with the extra slashes in the above paragraph that weren't parsing, so I deleted them.
 
There is a slight catch, in that the predicates "$(S \in_{PX} F)$" and "$(x \in_X S)$" (as generalized predicates over $PX$, where $S$ lives) are taken over different domains.  The first is of the form $\phi_1 : PPX \to P(1)^{PX}$, and the second is of the form $\phi_2 : X \to P(1)^{PX}$.  No matter:  we just substitute in some dummy variables.  That is, we just pull these maps back to a common domain $PPX \times X$, forming the composites

$$\displaystyle \psi_1 = (PPX \times X \stackrel{\pi_1}{\to} PPX \stackrel{\phi_1}{\to} P(1)^{PX})$$

and

$$\displaystyle \psi_2 = (PPX \times X \stackrel{\pi_2}{\to} X \stackrel{\phi_2}{\to} P(1)^{PX}).$$

Putting all this together, we form the composite

$$\displaystyle PPX \times X \stackrel{\langle \psi_1, \psi_2 \rangle}{\to} P(1)^{PX} \times P(1)^{PX}$$

$$\displaystyle \cong (P(1) \times P(1))^{PX} \stackrel{(\Rightarrow)^{PX}}{\to} P(1)^{PX} \stackrel{\forall_{PX}}{\to} P(1)$$

This composite directly expresses the definition of the internal predicate $(x \in \bigcap F)$ given above.  By cartesian closure, this map $PPX \times X \to P(1)$ induces the desired internal intersection operator, $\bigcap : PPX \to PX$.

This construction provides an important bridge to getting the rest of the internal logic of ETCS.  Since we can can construct the intersection of arbitrary definable families of subsets, the power sets $PX$ are internal inf-lattices. But [inf-lattices are sup-lattices](http://topologicalmusings.wordpress.com/2008/04/04/lattices-and-duality) as well;  on this basis we will be able to construct the colimits ( _e.g._, finite sums, coequalizers) that we need.  Similarly, the intersection operators easily allow us to construct image factorizations:  any function $f : X \to Y$ can be factored (in an essentially unique way) as an epi or surjection $X \to I$ to the image, followed by a mono or injection $I \to Y$.  The trick is to define the image as the smallest subset of $Y$ through which $f$ factors, by taking the intersection of all such subsets.  Image factorization leads in turn to the construction of [[existential quantification]].

As remarked above, the internal logic of a topos is generally intuitionistic (the law of excluded middle is not satisfied).  But, if we add in the axiom of strong extensionality of ETCS, then we're back to ordinary classical logic, where the law of excluded middle is satisfied, and where we just have the two truth values "true" and "false".  This means we will be able to reason in ETCS set theory just as we do in ordinary mathematics, taking just a bit of care with how we treat membership.  The foregoing discussion gives indication that logical operations in categorical set theory work in ways familiar from naive set theory, and that basic set-theoretic constructions like intersection are well-grounded in ETCS.
