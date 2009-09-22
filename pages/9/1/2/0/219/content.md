_This is Part I of an exposition by [[Todd Trimble]] on [[ETCS]]_.

See also

* Part II, [[Trimble on ETCS II|ETCS: Internalizing the logic]]

* Part III, [[Trimble on ETCS III|ETCS: Building joins and coproducts]]

#Contents#
* tic
{:toc}



#ZFC and ETCS: Elementary Theory of the Category of Sets#

This is a post on "[[foundations]] of mathematics" (eek!). I was motivated to write it while I've been struggling to understand better certain applications of ultrafilters -- namely the theory of *measurable cardinals* -- from a point of view and language that I feel comfortable with. My original intent was to blog about *that*, as a kind of off-shoot of the general discussion of [ultrafilters](http://topologicalmusings.wordpress.com/2008/07/18/ultrafilter-convergence-compactness-and-the-spectrum-of-a-boolean-algebra/) I started in connection with the series on [Stone duality](http://topologicalmusings.wordpress.com/2008/04/02/toward-stone-duality-posets-and-meets/), and because it seems kind of cool. And I will. But this got finished first, and I thought that it would be of interest to some who have been following my [category](http://topologicalmusings.wordpress.com/2008/06/22/basic-category-theory-i/) [theory](http://topologicalmusings.wordpress.com/2008/06/29/basic-category-theory-ii/) [posts](http://topologicalmusings.wordpress.com/2008/07/12/basic-category-theory-iii-representability-adjoints-and-the-yoneda-lemma/).

A lot of confusion seems to reign around "the [[category theory|categorical]] approach to [[foundations]]" and what it might entail; some seem to think it involves a "doing-away with elements" that we all know and love, or doing away with [[set|sets]] and supplanting them with [[category|categories]], or something like that. That's an unfortunate misunderstanding. My own attitude is pragmatic: I'm all in favor of mathematicians using ordinary "[naive](http://topologicalmusings.wordpress.com/2007/12/13/naive-set-theory-paul-halmos/)" (pre-axiomatic) set theory to express their thoughts if that's the familiar and appropriate conveyance -- I mean, obviously I do it myself. It's our common heritage, learned through years of undergraduate and graduate school experience and beyond. I'm not proposing for a moment to "overthrow" it.
 
What I *do* propose to discuss is a formalized set theory which embodies this rich tradition, but which takes advantage of categorical insights honed over the decades, and which I would argue is 'natural' in its ease to accept formulas in naive set theory and give them a foundation true to mathematical practice; I also argue it addresses certain criticisms which I feel could be put to that hallowed foundational theory, ZFC. I should own up that this theory is not immune to criticism, a main one being that a certain amount of preface and commentary is required to make it accessible (and I don't think category theorists have done a particularly hot job doing that, frankly).

Let's start by putting down what we want in very simple, pragmatic terms:

* A (formalized) 'set theory' worthy of the name ought to realize a conception of sets as "completed collections", and allow for the existence of enough sets and relations to fulfill the needs of working mathematicians.

This is intentionally vague.
The "needs of working mathematicians" fluctuate over time and place and person. Some of the core needs would include the existence of the sets of natural numbers and real numbers, for instance. On the other hand, in the field of set theory one will have other needs than in, say, complex analysis. For now I'll ignore some of the deeper needs of set theorists, and try to focus on the basic stuff you'd need to formalize what goes on in your average graduate school text (to put it vaguely, again).

We will discuss two formalizations of set theory: [ZFC](http://en.wikipedia.org/wiki/Zermelo-Fraenkel_set_theory), and Lawvere's Elementary Theory of the Category of Sets [[ETCS]]. The first "needs no introduction", as they say. The second is an autonomous category-based theory, described in detail below, and proposed by Saunders Mac Lane as an alternative approach to "foundations of mathematics" (see his [book with Moerdijk](http://www.amazon.com/Sheaves-Geometry-Logic-Universitext-Saunders/dp/3540977104)). Either formalization provides fully adequate infrastructure to support the naive set theory of working mathematicians, but there are significant conceptual differences between them, centering precisely on how the notion of **membership** is handled. I'll start with the more familiar ZFC.

As everyone knows, ZFC formalizes a conception of "set" as collection extensionally determined by the members it contains, and the ZFC axioms ensure a rich supply of ways in which to construct new sets from old (pairings, unions, power sets, etc.). Considering how old and well-developed this theory is, and the plenitude of available accounts, I won't say much here on its inner development. Instead, I want to pose a question and answer to highlight a key ZFC conception, and which we use to focus our discussion:

> **Question**: "What are the members of sets?"
>
> **Answer: "Other sets."

This may seem innocent enough, but the consequences are quite far-reaching. It says that "membership" is a relation $\in$ from the collection $V$ of all "sets" to itself. (Speaking at a pre-axiomatic level, a *relation* from a set $X$ to a set $Y$ is a subset $R \subseteq X \times Y$. So a structure for ZFC set theory consists of a "universe of discourse" $V$, together with a collection $\in \subseteq V \times V$ of pairs of elements of $V$, called the membership relation.)

Why is this a big deal? A reasonable analogue might be [dynamical systems](http://en.wikipedia.org/wiki/Dynamical_system). If $X$ and $ Y$ are manifolds, say, then you can study the properties of a given smooth map $f: X \to Y$ and maybe say interesting things of course, but in the case $X = Y$, you get the extra bonus that outputs can be fed back in as inputs, and infinite processes are born: you can study periodic orbits, long-term behaviors, and so on, and this leads to some very intricate mathematics, even when $ X$ is a simple manifold like a 2-sphere.

My point is that something analogous is happening in ZFC: we have a (binary) relation $ \in$ from $ V$ to itself, and we get a rich "dynamics" and feedback by iterative relational composition of $ \in$ with itself, or by composing other derived binary relations from $ V$ to itself. (Perhaps I should recall here, again at a pre-axiomatic level, that the composite $ S \circ R$ of a relation $ R \subseteq X \times Y$ and $ S \subseteq Y \times Z$ is the subset

$$
\{(x, z): \exists_{y \in Y} (x, y) \in R \wedge (y, z) \in S\} \subseteq X \times Z
$$

A "behavior" then would correspond to an iterated membership chain

$$ 
 (x \in y) \wedge (y \in z) \wedge (z \in w) \wedge \ldots
$$

and there are certain constraints on behavior provided by things like the axiom of foundation (no infinitely long backward evolutions). The deep meaning of the extensionality axiom is that a "set" $ s$ is uniquely specified by the abstract structure of the tree of possible backward evolutions or behaviors starting from the "root set" $ s$. This gives some intuitive but honest idea of the world of sets according to the ZFC picture: sets are tree-like constructions. The ZFC axioms are very rich, having to do with incredibly powerful operations on trees, and the combinatorial results are *extremely* complicated.

There are other formulations of ZFC. One is by posets: given any relation $ R \subseteq V \times V$ (never mind one satisfying the ZFC axioms), one can create a reflexive and transitive relation $ \leq$, defined by the first-order formula

$$
 a \leq b \text{ if and only if }  \forall_{x \in V} (x, a) \in R \Rightarrow (x, b) \in R
$$

The "extensionality axiom" for $ R$ can then be formulated as the condition that $ \leq$ also be antisymmetric, so that it is a partial ordering on $ V$. If $ R = \in$ is the membership relation for a model of ZFC, then this $ \leq$ is of course just the usual "subset relation" between elements of $ V$.

Then, by adding in a suitable "singleton" operator $ s: V \to V$ so that

$$
  x \in y \text{ if and only if }  s(x) = \{x\} \leq y
$$

the rest of the ZFC axioms can be equivalently recast as conditions on the augmented poset structure $ (V, \leq, s)$. In fact, Joyal and Moerdijk wrote a slim volume, [Algebraic Set Theory](http://books.google.com/books?id=E0Xhn32xzZAC&dq=%22algebraic+set+theory%22&pg=PP1&ots=DvTjZP030_&sig=IX1kWLQ2rzsmw5gsdJ_0ow8vJEQ&hl=en&sa=X&oi=book_result&resnum=1&ct=result), which gives a precise (and for a categorist, attractive) sense in which models of axiomatic frameworks like ZF can be expressed as certain initial algebras [of structure type $ (V, \leq, s)$] within an ambient category of classes, effectively capturing the "cumulative hierarchy" conception underlying ZFC in categorical fashion.
 
The structure of a ZFC poset $ (V, \leq)$ is rich and interesting, of course, but in some ways a little odd or inconvenient: e.g., it has a bottom element of course (the "empty set"), but no top (which would run straight into Russell's paradox). Categorically, there *are* some cute things to point out about this poset, usually left unsaid; for example, taking "unions" is left adjoint to taking "power sets":

$$
  \bigcup F \leq X  \text{if and only if}   F \leq P X.
$$

In summary: ZFC is an axiomatic theory (in the language of first-order logic with equality), with one basic type $ V$ and one basic predicate $ \in$ of binary type $ V \times V$, satisfying a number of axioms. The key philosophic point is that there is no typed distinction between "elements" and "sets": both are of type $ V$, and there is a consequent very complicated dynamical "mixing" which results just on the basis of a short list of axioms: enough in principle to found all of present-day mathematics! I think the fact that one gets such great power, so economically, from apparently such slender initial data, is a source of great pride and pleasure among those who uphold the ZFC conception (or that of close kin like NBG) as a gold standard in foundations.

My own reaction is that ZFC is perhaps *way* too powerful! For example, the fact that $ \in$ is an endo-relation makes possible the kind of feedback which can result in things like Russell's paradox, if one is not careful. Even if one is free from the paradoxes, though, the point remains that ZFC pumps out not only all of mathematics, but all sorts of dross and weird by-products that are of no conceivable interest or relevance to mathematics. One might think, for example, that to understand a model of ZFC, we have to be able to understand which definable pairs $ (a, b)$ satisfy $ a \in b$. So, in principle, we can ask ourselves such otherwise meaningless gibberish as "what in our model and implementation is the set-theoretic intersection of the real number $ \pi$ and Cantor space?" and expect to get a well-defined answer. When you get right down to it, the idea that *everything* in mathematics (like say the number $ e$) is a "set" is just plain bizarre, and actually very far removed from the way mathematicians normally think. And yet this is how we are encouraged to think, if we are asked to take ZFC seriously as a foundations.

One might argue that all expressions and theorems of normal mathematics are interpretable or realizable in the single theory ZFC, and that's really all we ever asked for -- the details of the actual implementation (like, 'what is an ordered pair?') being generally of little genuine interest to mathematicians (which is why the mathematician in the street who says ZFC is so great usually can't say with much specificity what ZFC is). But this would seem to demote ZFC foundations, for most mathematicians, to a security blanket -- nice to know it's there, maybe, but otherwise fairly irrelevant to their concerns. But if there really is such a disconnect between how a mathematician thinks of her materials *at a fundamental level* and how it specifically gets coded up as trees in ZFC, with such huge wads of uninteresting or irrelevant stuff in its midst, we might re-examine just how appropriate ZFC is as "foundations" of our subject, or at least ask ourselves how much of it we usefully retain and how we might eliminate the dross.
 
We turn now to consider a categorical approach, ETCS. This will require retooling the way we think of mathematical membership. There are three respects in which "membership" or "elementhood" differs here from the way it is handled in ZFC:

1. "Elements" and "sets" are entities of different types. (Meaning, elements are not themselves presupposed to be sets.)
2. When we say "element", we never mean an object considered in isolation; we always consider it relative to the specific "set" it is considered to be a member of. (That is, strictly speaking, the same object is never thought of as "belonging to" two distinct sets -- use of such language must be carefully circumscribed.)
3. We consider not just "elements" in the usual sense, but what are sometimes called "generalized elements". Civilians call them "functions". Thus, an element of type $X$ over a domain of variation $ U$ is fancy terminology for a function $f: U \to X$. We will call them functions or "generalized elements", depending on the intuition we have in mind. A function $x: 1 \to X$ corresponds to an ordinary element of $X$.

Each of these corresponds to some aspect of normal practice, but taken together they are sufficiently different in how they treat "membership" that they might need some getting used to. The first corresponds to a decision to treat elements of a "set" like $ \mathbb{R}$ as 'urelements': they are not considered to have elements themselves and are not considered as having any internal structure; they are just atoms. What counts in a mathematical structure then is not what the constituents are 'like' themselves, but only how they are interrelated among themselves qua the structure they are considered being part of.

This brings us right to the second point. It corresponds e.g. to a decision never to consider a number like '3' in isolation or as some Platonic essence, but always with respect to an ambient system to which it is bound, as in '3 *qua* natural number', '3 *qua* rational number', etc. It is a firm resolve to always honor context-dependence. Naturally, we *can* in a sense transport '3' from one context to another via a specified function like $ \mathbb{N} \to \mathbb{Q}$, but strictly speaking we've then changed the element. This raises interesting questions, like "what if anything plays the role of extensionality?", or "what does it mean to take the intersection of sets?". (Globally speaking, in ETCS we don't -- but we can, with a bit of care, speak of the intersection of two "subsets" of a given set. For any real mathematical purpose, this is good enough.)

My own sense is that it may be this second precept which takes the most getting used to -- it certainly gives the lie to sometimes-heard accusations that categorical set theory is just a "[slavish translation](http://www.cs.nyu.edu/pipermail/fom/1998-January/000994.html) of ZFC into categorical terms". Clearly, we are witnessing here *radical* departure from how membership is treated in ZFC. Such unbending commitment to the principle of context-dependence might even be felt to be overkill, a perhaps pedantic exercise in austerity or purity, or that it robs us of some freedom in how we want to manipulate sets. A few quick answers: no, we don't lose any essential freedoms. Yes, the *formal* language may seem *slightly* awkward or stilted at certain points, but the bridges between the naive and formal are mercifully fairly obvious and easily navigated. Lastly, by treating membership not as a global endo-relation on sets, but as local and relative, we effectively eliminate all the extraneous dreck and driftwood which one rightly ignores when examining the mathematics of ZFC.
 
The third precept is familiar from the way category theorists and logicians have used generalized elements to extend set-theoretic notation, e.g., to chase diagrams in abelian categories, or to describe sheaf semantics of intuitionistic set theory, or to flesh out the Curry-Howard isomorphism. It is a technical move in some sense, but one which is easy to grow accustomed to, and very convenient. In ETCS, there is a strong "extensionality principle" (technically, the requirement that the terminal object is a generator) which guarantees enough "ordinary" elements $ x: 1 \to X$ to make any distinctions that can sensibly be made, but experience with topos theory suggests that for many applications, it is often convenient to drop or significantly modify that principle. If anything in [[ETCS]] is a nod to traditional set theory, it is such a strong extensionality principle. [The [Yoneda principle](http://topologicalmusings.wordpress.com/2008/06/29/basic-category-theory-ii/), which deals with generalized elements, is also an extensionality principle: it says that a set is determined uniquely (to within uniquely specified isomorphism) by its generalized elements.]
 
Okay, it is probably time to lay out the axioms of [[ETCS]]. The basic data are just those of a category; here, we are going to think of objects as "sets", and morphisms $ x: a \to b$ as functions or equivalently as "elements of a set $ b$ over a domain of variation $ a$". The latter is a mouthful, and it is sometimes convenient to suppress explicit mention of the domain $ a$, so that "$ x \in b$" just means some morphism $ x$ with codomain $ b$. More on this below. The axioms of ETCS are the axioms of [[category theory]], plus existence axioms which guarantee enough structure to express and support naive [[set theory]] (under the strictures imposed by precepts 1-3 above). For those who speak the lingo, the axioms below are those of a [[well-pointed topos]] with [[natural numbers object]] and [[axiom of choice]]. (This can be augmented later with a replacement axiom, so as to achieve bi-interpretability with full ZFC.)

>**Remark**: As ETCS breaks the "dynamical" aspects of ZFC, and additionally treats issues of membership in a perhaps unaccustomed manner, its axioms do take longer to state. This should come as no surprise. Actually, we've discussed some of them already in [other posts on category theory](http://topologicalmusings.wordpress.com/2008/06/29/basic-category-theory-ii/); we will repeat ourselves but make some minor adjustments to reflect normal notational practice of naive set theory, and build bridges between the naive and formal.

**Axiom of products**. For any two sets $ a, b$, there is a set $ c$ and functions $ p_1: c \to a$, $ p_2: c \to b$, such that given two elements $ x \in a, y \in b$ over the same domain, there exists a unique element $ \langle x, y \rangle \in c$ over that domain for which

$$ p_1\langle x, y \rangle = x \qquad p_2\langle x, y \rangle = y$$

A choice of product $ c$ is usually denoted $ a \times b$. To make a bridge with naive set-theory notation, we suggestively write

$$ a \times b :=_i \{\langle x, y \rangle: x \in a, y \in b\}$$

where the funny equality sign and bracketing notation on the right simply mean that the cartesian product is uniquely defined up to isomorphism by its collection of (generalized) elements, which correspond to pairs of elements, in accordance with the Yoneda principle as explained in the discussion [here](http://topologicalmusings.wordpress.com/2008/06/29/basic-category-theory-ii/).

We also assume the existence of an "empty product" or terminal object 1: this is a set with a unique element $ x \in 1$ over any domain.
 
**Axiom of equalizers**. For any two functions $ \displaystyle f, g: a \rightrightarrows b$, there exists a function $ i: e \to a$ such that

1. $ f i = g i$,
2. Given $ x \in a$ over some domain such that $ f x = g x$, there exists a unique $ x' \in e$ over the same domain such that $ i x' = x$.

An equalizer $ i: e \to a$ is again defined up to isomorphism by its collection of generalized elements, denoted $ e :=_i \{x \in a: f(x) = g(x)\} \hookrightarrow a$, again in accordance with the Yoneda principle.
Using the last two axioms, we can form pullbacks: given functions $ f: a \to c, g: b \to c$, we can form the set denoted

$$
\{\langle x, y \rangle \in a \times b: f x = g y\}
$$

using the product and equalizer indicated by this notation.
 
Before stating the next axiom, a few important remarks. We recall that a function $ i: a \to b$ is *injective* if for every $ x, y \in a$ over the same domain, $ i x = i y$ implies $ x = y$. In that case we think of $ i: a \to b$ as defining a "subset" $ a$ of $ b$, whose (generalized) elements correspond to those elements $ z \in b$ which factor (evidently uniquely) through $ i$. It is in *that* sense that we say $ z \in b$ also "belongs to" a subset $ a$ (cf. precept 2). A *relation* from $ a$ to $ b$ is an injective function or subset $ r \hookrightarrow a \times b$.

 **Axiom of power sets**. For every set $ b$ there is a choice of power set $ P(b)$ and a relation $ \in_b \hookrightarrow b \times P(b)$, so that for every relation $ r \hookrightarrow a \times b$, there exists a unique function $ \chi_r: a \to P(b)$ such that $ r$ is obtained up to isomorphism as the pullback

$$
\{\langle x, y \rangle \in a \times b: y \in_b \chi_r(x)\}
$$

In other words, $ \langle x, y \rangle$ belongs to $ r$ if and only if $ \langle y, \chi_r(x) \rangle$ belongs to $ \in_b$.
 
**Axiom of strong extensionality**. For functions 

$$ f, g: a \to b,$$ 

we have $ f = g$ if and only if $ f x = g x$ for all "ordinary" elements $ x: 1 \to a$.
 
**Axiom of natural number object**. There is a set $ \mathbf{N}$, together with an element $ 0: 1 \to \mathbf{N}$ and a function $ s: \mathbf{N} \to \mathbf{N}$, which is initial among sets equipped with such data. That is, given a set $ a$ together with an element $ x: 1 \to a$ and a function $ f: a \to a$, there exists a unique function $ h: \mathbf{N} \to a$ such that

$$
h(0) = x; \qquad h s = f h
$$

Or, in elementwise notation, $ h(n+1) = f h(n)$ for every (generalized) element $ n \in \mathbf{N}$, where $ n+1$ means $ s(n)$. Under strong extensionality, we may drop the qualifier "generalized".

Before stating the last axiom, we formulate a notion of "surjective" function: $ f: a \to b$ is *surjective* if for any two functions $ g, h: b \to c$, we have $ g = h$ if and only if $ g f = h f$. This is dual to the notion of being injective, and under the axiom of strong extensionality, is equivalent to the familiar notion: that $ f$ is surjective if for every element $ y: 1 \to b$, there exists an element $ x: 1 \to a$ such that $ f x = y$.
 
**[[axiom of choice|Axiom of choice]]**. Every surjective function $ s: a \to b$ admits a section, i.e., a function $ i: b \to a$ such that $ s i = 1_b$, the identity function.
 
This completes the list of axioms for [[ETCS]]. I have been at pains to try to describe them in notation which is natural from the standpoint of naive set theory, with the clear implication that any formula of naive set theory is readily translated into the theory [[ETCS]] (provided we pay appropriate attention to our precepts governing membership), and that this theory provides a rigorous foundation for mainstream mathematics.

To make good on this claim, further discussion is called for. First, I have not discussed how classical first-order logic is internalized in this setting (which we would need to do justice to a comprehension or separation scheme), nor have I discussed the existence or construction of colimits. I plan to take this up later, provided I have the energy for it. Again, the plan would be to stick as closely as possible to naive set-theoretic reasoning. (This might actually be useful: the categorical treatments found in many texts tend to be technical, often involving things like monad theory and Beck's theorem, which makes it hard for those not expert in category theory to get into. I want to show this need not be the case.)
 
Also, some sort of justification for the claim that [[ETCS]] "founds" mainstream mathematics is called for. Minimally, one should sketch how the reals are constructed, for instance, and one should include enough "definability theory" to make it plausible that almost all constructions in ordinary mathematics find a natural home in ETCS. What is excluded? Mainly certain parts of set theory, and parts of category theory (ha!) which involve certain parts of set theory, but this is handled by strengthening the theory with more axioms; I particularly have in mind a discussion of the replacement axiom, and perhaps large cardinal axioms. More to come!