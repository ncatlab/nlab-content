_This is Part III of an exposition by [[Todd Trimble]] on [[ETCS]]_.

See also 

* Part I.  [[Trimble on ETCS I|ZFC and ETCS]]

* Part II.  [[Trimble on ETCS II|ETCS: Internalizing the logic]]

+--{.query}
**Editing help wanted**

[This is what it is supposed to look like](http://topologicalmusings.wordpress.com/2008/12/15/etcs-building-joins-and-coproducts/).

Starting with the raw Wordpress text, replace "$latex" with "$". The next big fix is to replace "<blockquote>" with "$" and "</blockquote>" with "$". That puts it into pretty good shape.

Replace "\mbox" with "\:\text"

Some remaining issues:

* Need a replacement for \cong
* Etc

The easy thing to do is to Edit this page, copy the text to your favorite editor, find/replace, paste text back here.
=--

## ETCS : Building joins and coproducts ##

After a long hiatus, I'd like to renew the discussion of axiomatic categorical set theory, more specifically the Elementary Theory of the Category of Sets ([[ETCS]]).  [Last
time](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic) I blogged about this, I made some initial forays into "internalizing logic" in [[ETCS]], and described in broad brushstrokes how to use that internal logic to derive a certain amount of the structure one associates with a category of sets.  Today I'd like to begin applying some of the results obtained there to the problem of constructing _colimits_ in a category satisfying the ETCS axioms (an _[[ETCS]] category_, for short).
 
(If you're just joining us now, and you already know some of the jargon, an _[[ETCS]] category_ is a well-pointed topos that satisfies the axiom of choice and with a natural numbers object.  We are trying to build up some of the elementary theory of such categories from scratch, with a view toward foundations of mathematics.)
 
But let's see --- where were we?  Since it's been a while, I was tempted to review the philosophy behind this undertaking (why one would go to all the trouble of setting up a categories-based alternative to ZFC, when time-tested ZFC is able to express virtually all of present-day mathematics on the basis of a reasonably short list of axioms?).  But in the interest of time and space, I'll confine myself to a few remarks.
 
As we said, a chief difference between ZFC and ETCS resides in how ETCS treats the issue of membership.  In ZFC, membership is a global binary relation:  we can take any two "sets" $A, B$ and ask whether $A \in B$.  Whereas in ETCS, membership is a relation between entities of different sorts:  we have "sets" on one side and "elements" on another, and the two are not mixed ( _e.g._, elements are not themselves considered sets).
 
Further, and far more radical:  in ETCS the membership relation $x \in A$ is a _function_, that is, an element $x$ "belongs" to only one set $A$ at a time.  We can think of this as "declaring" how we are thinking of an element, that is, declaring which set (or which type) an element is being considered as belonging to.  (In the jargon, ETCS is a _typed theory_.)  This reflects a general and useful philosophic principle:  that elements in isolation are considered inessential, that what counts are the aggregates or contexts in which elements are organized and interrelated.  For instance, the numeral "2" in isolation has no meaning;  what counts is the context in which we think of it (_qua_ rational number or _qua_ complex number, _etc._).  Similarly the set of real numbers has no real sense in isolation;  what counts is which category we view it in.
 
I believe it is reasonable to grant this principle a foundational status, but: rigorous adherence to this principle completely changes the face of what set theory looks like.  If elements "belong" only to one set at a time, how then do we even _define_ such basic concepts as subsets and intersections?  These are some of these issues we discussed last time.
 
There are other significant differences between ZFC and ETCS:  stylistically, or in terms of presentation, ZFC is more "top-down" and ETCS is more "bottom-up".  For example, in ZFC, one can pretty much define a subset $\{ x \in X : P \}$ by writing down a first-order formula $P$ in the language;  the comprehension (or separation) axiom scheme is a mighty sledgehammer that takes care of the rest.  In the axioms of ETCS, there is no such sledgehammer:  the closest thing one has to a comprehension scheme in the ETCS axioms is the power set axiom (a single axiom, not an axiom scheme).  However, in the formal development of ETCS, one _derives_ a comprehension scheme as one manually constructs the internal logic, in stages, using the simple tools of adjunctions and universal properties.  We started doing some of that in our last post.  So:  with ZFC it's more as if you can just hop in the car and go;  with ETCS you build the car engine from smaller parts with your bare hands, but in the process you become an expert mechanic, and are not so rigidly attached to a particular make and model ( _e.g._, much of the theory is built just on the axioms of a topos, which allows a lot more semantic leeway than one has with ZF).
 
But, in all fairness, that is perhaps the biggest obstacle to learning ETCS:  at the outset, the tools available [mainly, the idea of a universal property] are quite simple but parsimonious, and one has to learn how to build some set-theoretic and logical concepts normally taken as "obvious" from the ground up.  (Talk about "foundations"!)  On the plus side, by building big logical machines from scratch, one gains a great deal of insight into the inner workings of logic, with a corresponding gain in precision and control and modularity when one would like to use these developments to design, say, automated deduction systems (where there tend to be strong advantages to using type-theoretic frameworks).
 
Enough philosophy for now; readers may refer to my [earlier](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets) [posts](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic/) for more.  Let's get to work, shall we?  Our last post was about the structure of (and relationships between) posets of subobjects $Sub(X)$ _relative_ to objects $X$, and now we want to exploit the results there to build some _absolute_ constructions, in particular finite coproducts and coequalizers.  In this post we will focus on coproducts.

: __Note to the experts.__  Most textbook treatments of the formal development of topos theory (as for example Mac Lane&#8211;Moerdijk) are efficient but highly technical, involving for instance the slice theorem for toposes and, in the construction of colimits, recourse to Beck's theorem in monad theory applied to the double power-set monad [following the elegant construction of Par&#233;].  The very abstract nature of this style of argumentation (which in the application of Beck's theorem expresses ideas of fourth-order set theory and higher) is no doubt partly responsible for the somewhat fearsome reputation of topos theory.
 
: In these notes I take a much less efficient but much more elementary approach, based on an arrangement of ideas which I hope can be seen as "natural" from the point of view of naive set theory.  I learned of this approach from Myles Tierney, who was my PhD supervisor, and who with Bill Lawvere co-founded elementary topos theory, but I am not aware of any place where the details of this approach have been written up before now.  I should also mention that the approach taken here is not as "purist" as many topos theorists might want;  for example, here and there I take advantage of the strong extensionality axiom of ETCS to simplify some arguments.

### The Empty Set and Two-Valued Logic ###

We begin with the easy observation that a terminal category, _i.e._, a category $\mathbf{1}$ with just one object and one morphism (the identity), satisfies all the ETCS axioms.  Ditto for any category $C$ equivalent to $\mathbf{1}$ (where every object is terminal).  Such boring ETCS categories are called _degenerate_;  obviously our interest is in the structure of nondegenerate ETCS categories.
 
Let $\mathbf{E}$ be an ETCS category (see [here](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets) for the ETCS axioms).  Objects of $\mathbf{E}$ are generally called "sets", and morphisms are generally called "functions" or "maps".
 
__Proposition 0.__  If an ETCS category $\mathbf{E}$ is a preorder, then $\mathbf{E}$ is degenerate.
 
__Proof.__  Recall that a preorder is a category in which there is at most one morphism $A \to B$ for any two objects $A, B$.  Every morphism in a preorder is vacuously monic.  If there is a nonterminal set $A$, then the monic $A \to 1$ to any terminal set defines a subset $A \subseteq 1$ distinct from the subset defined by $1 \to 1$, thus giving (in an ETCS category) distinct classifying maps $\chi_A, t : 1 \to P(1)$, contradicting the preorder assumption.  Therefore all objects $A$ are terminal. $\Box$
 
Assume from now on that $\mathbf{E}$ is a nondegenerate ETCS category.
 
__Proposition 1.__  There are at least two _truth values_, _i.e._, two elements $1 \to P(1)$, in $\mathbf{E}$.
 
__Proof.__  By proposition 0, there exist sets $X, Y$ and two distinct functions $f, g : X \to Y$.  By the axiom of strong extensionality, there exists $x : 1 \to X$ such that $f x \neq g x$.  The equalizer $E \to 1$ of the pair $f x, g x : 1 \to Y$ is then a proper subset of $1$, and therefore there are at least two distinct elements $\chi_E, \chi_1 : 1 \to P(1)$.  $\Box$
 
__Proposition 2.__  There are at most two truth values $1 \to P(1)$;  equivalently, there are at most two subsets of $1$.
 
__Proof.__  If $U, V \subseteq 1$ are distinct subsets of $1$, then either $U \neq U \cap V$ or $V \neq U \cap V$, say the former.  Then $1_U : U \subseteq U$ and $U \cap V \subseteq U$ are distinct subsets, with distinct classifying maps $\chi_{1_U}, \chi_{U \cap V} : U \to P(1)$.  By strong extensionality, there exists $x : 1 \to U$ distinguishing these classifying maps.  Because $1$ is terminal, we then infer $1 \subseteq U$ and $U \subseteq 1$, so $U = 1$ as subsets of $1$, and in that case only $V$ can be a proper subset of $1$.  $\Box$
 
By Propositions 1 and 2, there is a unique proper subset of the terminal object $1$.  Let $0 \to 1$ denote this subset.  Its domain may be called an "empty set";  by the preceding proposition, it has no proper subsets.  The classifying map $1 \to P1$ of $0 \subseteq 1$ is the truth value we call "false".
 
__Proposition 3.__  0 is an initial object, _i.e._, for any $X$ there exists a unique function $0 \to X$.
 
__Proof.__  Uniqueness:  if $f, g : 0 \to X$ are maps, then their equalizer $x : E \to 0$, which is monic, must be an isomorphism since 0 has no proper subsets.  Therefore $f = g$.  Existence:  there are monos

$$\displaystyle 0 \to 1 \stackrel{t_X}{\to} PX$$
 
$$\displaystyle X \stackrel{\sigma}{\to} PX$$

where $t_X$ is "global truth" (classifying the subset $X \subseteq X$) on $X$ and $\sigma$ is the "singleton mapping $x \mapsto \{ x \}$" on $X$, defined as the classifying map of the diagonal map $\delta : X \subseteq X \times X$ (last time we saw $\sigma$ is monic).  Take their pullback.  The component of the pullback parallel to $\sigma$ is a mono $P \to 0$ which again is an isomorphism, whence we get a map $0 \cong P \to X$ using the other component of the pullback.  $\Box$
 
__Remark.__  For the "purists", an alternative construction of the initial set 0 that avoids use of the strong extensionality axiom is to define the subset $0 \subseteq 1$ to be "the intersection all subsets of $1$".  Formally, one takes the extension $\left[\phi\right] \subseteq 1$ of the map

$$\displaystyle \phi = (1 \stackrel{t_{P1}}{\to} PP1 \stackrel{\bigcap}{\to} P1);$$

where the first arrow represents the class of all subsets of $P1$, and the second is the internal intersection operator defined at the end of our last post.  Using formal properties of intersection developed later, this intersection $0 \subseteq 1$ has no proper subsets, and then the proof of proposition 3 carries over verbatim.  $\Box$
 
__Corollary 1.__  For any $X$, the set $0 \times X$ is initial.
 
__Proof.__  By [cartesian closure](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic), maps $0 \times X \to Y$ are in bijection with maps of the form $0 \to Y^X$, and there is exactly one of these since 0 is initial.  $\Box$
 
__Corollary 2.__  If there exists $f : X \to 0$, then $X$ is initial.
 
__Proof.__  The composite of $\langle f, 1_X \rangle : X \to 0 \times X$ followed by $\pi_2 : 0 \times X \to X$ is $1_X$, and $\pi_2$ followed by $\langle f, 1_X \rangle : X \to 0 \times X$ is also an identity since $0 \times X$ is initial by Corollary&#160;1.  Hence $X$ is isomorphic to an initial object $0 \times X$.  $\Box$
 
By Corollary 2, for any object $Y$ the arrow $0 \to Y$ is vacuously monic, hence defines a subset.
 
__Proposition 4.__  If $X \not\cong 0$, then there exists an element $x : 1 \to X$.
 
__Proof.__  Under the assumption, $X$ has at least two distinct subsets:  $0 \subseteq X$ and $1_X : X \subseteq X$.  By strong extensionality, their classifying maps $\chi_0, \chi_1 : X \to P1$ are distinguished by some element $x : 1 \to X$.

### External Unions and Internal Joins ###

One of the major goals in this post is to construct finite coproducts in an ETCS category.  As in ordinary set theory, we will construct these as disjoint unions.  This means we need to discuss unions first;  as should be expected by now, in ETCS unions are considered locally, _i.e._, we take unions of _subsets of a given set_.  So, let $A, B \subseteq X$ be subsets.
 
To define the union $A \cup B \subseteq X$, the idea is to take the intersection of all subsets containing $A$ and $B$.  That is, we apply the internal intersection operator (constructed [last
time](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic/) ),

$$\displaystyle \bigcap : PPX \to PX,$$

to the element $1 \to PPX$ that represents the set of all subsets of $X$ containing $A$ and $B$;  the resulting element $1 \to PX$ represents $A \cup B$.  The element $1 \to PPX$ corresponds to the intersection of two subsets $\{ C \in PX : A \subseteq C \} \:\cap\: \{ C \in PX : B \subseteq C \} \subseteq PX$.

: __Remark.__  Remember that in ETCS we are using _generalized_ elements:  $C \in PX$ really means a function $C : U \to PX$ over some domain $U$, which in turn classifies a subset $\left[C\right] \subseteq U \times X$.  On the other hand, the $A$ here is a subset $A \subseteq X$.  How then do we interpret the condition "$A \subseteq C$"?  We first pull back $\chi_A : 1 \to PX$ over to the domain $U$;  that is, we form the composite $\displaystyle U \stackrel{!}{\to} 1 \stackrel{\chi_A}{\to} PX$ and consider the condition that this is bounded above by $C : U \to PX$.  (We will write $\chi_A \leq C$, thinking of the left side as constant over $U$.)  Externally, in terms of subsets, this corresponds to the condition $U \times A \subseteq \left[C\right]$.

We need to construct the subsets $\{ C \in PX : A \subseteq C \}, \{ C \in PX : B \subseteq C \}$.  In ZFC, we could construct those subsets by applying the comprehension axiom scheme, but the axioms of ETCS have no such blanket axiom scheme.  (In fact, as we said earlier, much of the work on "internalizing logic" goes to show that in ETCS, we instead _derive_ a comprehension scheme!)  However, one way of defining subsets in ETCS is by taking loci of equations;  here, we express the condition $A \subseteq C$, more pedantically $A \subseteq \left[C\right]$ or $\chi_A \leq C$, as the equation

$$(\chi_A \Rightarrow C) = t_X$$

where the right side is the predicate "true over $X$".
 
Thus we construct the subset $\{C \in PX: A \subseteq C\}$ of $PX$ via the pullback:

$$\array{
\arrayopts{\rowalign{center axis center}}
\{ C : A \le C \} & \longrightarrow & 1 \\
\downarrow & & \downarrow \rlap{\scriptsize{t_X}} \\
PX & \underset{\dlap{\chi_A \Rightarrow -}}{\longrightarrow} & PX
}$$

Let me take a moment to examine what this diagram means exactly.  [Last
time](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic) we constructed an internal implication operator

$$\Rightarrow : P1 \times P1 \to P1$$

and now, in the pullback diagram above, what we are implicitly doing is lifting this to an operator

$$\Rightarrow_X : PX \times PX \to PX$$

The easy and cheap way of doing this is to remember the isomorphism $PX \cong P1^X$ we used last time to uncover the cartesian closed structure, and apply this to

$$\displaystyle P1^X \times P1^X \cong (P1 \times P1)^X \stackrel{\Rightarrow^X}{\to} P1^X$$

to define $\Rightarrow_X : PX \times PX \to PX$.  This map classifies a certain subset of $X \times PX \times PX$, which I'll just write down (leaving it as an exercise which involves just chasing the relevant definitions):
 
$$\{ (x, T, S) \in X \times PX \times PX : x \in_X T \Rightarrow x \in_X S \}$$

: __Remark.__  Similarly we can define a meet operator $\wedge_X : PX \times PX \to PX$ by exponentiating the internal meet $P1 \times P1 \to P1$.  It is important to know that the general Heyting algebra identities which we established last time for $P1$ lift to the corresponding identities for the operators $\wedge_X, \Rightarrow_X$ on $PX$.  Ultimately this rests on the fact that the functor $(-)^X$, being a right adjoint, preserves products, and therefore preserves any algebraic identity which can be expressed as a commutative diagram of operations between such products.

Hence, for the fixed subset $A \subseteq X$ (classified by $\chi_A : 1 \to PX$), the operator

$$\chi_A \Rightarrow - : PX \to PX$$

classifies the subset

$$\{ (x, S) : x \in_X A \Rightarrow x \in_X S \} \hookrightarrow X \times PX$$

Finally, in the pullback diagram above, we are pulling back the operator $\chi_A \Rightarrow -$ against $t_X$.  But, from [last
time](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic), that was exactly the method we used to construct universal quantification.  That is, given a subset

$$R \subseteq X \times Y$$

we defined $\forall_Y R \subseteq X$ to be the pullback of $t_Y : 1 \hookrightarrow PY$ along $\chi_R : X \to PY$.

Putting all this together, the pullback diagram above expresses the definition

$$\{ C \in PX : A \subseteq C \} := \{ C \in PX : \forall_{x \in X} \: x \in_X A \Rightarrow x \in_X C \}$$

that one would expect "naively".
 
Now that all the relevant constructions are in place, we show that $A \cup B$ is the join of $A$ and $B$ in the poset $Sub(X)$.  There is nothing intrinsically difficult about this, but as we are still in the midst of _constructing_ the internal logic, we will have to hunker down and prove some logic things normally taken for granted or zipped through without much thought.  For example, the internal intersection operator was defined with the help of internal universal quantification, and we will need to establish some formal properties of that.
 
Here is a useful general principle for doing internal logic calculations.  Let $\chi_R : X \to PY$ be the classifying map of a subset $R \subseteq X \times Y$, and let $f : U \to X$ be a function.  Then the composite $\chi_R f : U \to PY$ classifies the subset

$$(f \times 1_Y)^{-1}(R) \subseteq U \times Y$$

so that one has the general identity $\chi_R f = \chi_{(f \times 1)^{-1}(R)}$.  In passing back and forth between the external and internal viewpoints, the general principle is to try to render "complicated" functions $U \to PY$ into a form $\chi_R f$ which one can more easily recognize.  For lack of a better term, I'll call this the "pullback principle".
 
__Lemma 1.__  Given a relation $R \hookrightarrow X \times Y$ and a constant $c : 1 \to Y$, there is an inclusion

$$\forall_Y R \subseteq (1_X \times c)^{-1}(R)$$

as subsets of $X$.  (In traditional logical syntax, this says that for any element $c : 1 \to Y$,

$$\forall_{y : Y} R(x, y) \quad implies \quad R(x, c)$$

as predicates over elements $x \in X$.  This is the type of thing that ordinarily "goes without saying", but which we actually have to prove here!)
 
__Proof.__  As we recalled above, $\forall_Y R \subseteq X$ was defined to be $\chi_R^{-1}(t_Y)$, the pullback of global truth $t_Y : 1 \to PY$ along the classifying map $\chi_R : X \to PY$.  Hold that thought.
 
Let

$$Pc : PY \to P1$$

be the map which classifies the subset $\{ S \in PY : c \in_Y S\}$.  Equivalently, this is the map

$$P1^c: P1^Y \to P1^1$$

under the canonical isomorphisms $PY \cong P1^Y$, $P1^1 \cong P1$.  Intuitively, this maps $f \mapsto f(c)$, _i.e._, plugs an element $c \in Y$ into an element $f \in P1^Y$.
 
Using the adjunction $(- \times Y) \dashv (-)^Y$ of cartesian closure, the composite

$$\displaystyle X \stackrel{\chi_R}{\to} PY \stackrel{Pc}{\to} P1$$

transforms to the composite

$$X \times 1 \stackrel{1_X \times c}{\to} X \times Y \stackrel{\chi_{R}}{\to} P1$$

so by the pullback principle, $(Pc)\chi_R : X \times 1 \to P1$ classifies $(1_X \times c)^{-1}(R) \subseteq X \times 1 \cong X$.
 
Equivalently,

$$(1_X \times c)^{-1}(R) = \chi_{R}^{-1} (Pc)^{-1}(t) \qquad (1)$$

Also, as subsets of $PY$, we have the inclusion

$$(t_Y : 1 \hookrightarrow PY) \subseteq (Pc)^{-1}(t) \qquad (2)$$

[this just says that $t_Y$ belongs to the subset classified by $Pc$, or equivalently that $c : 1 \to Y$ is in the subset $Y \subseteq Y$].  Applying the pullback operation $\chi_{R}^{-1}$ to (2), and comparing to (1), Lemma 1 follows.  $\Box$
 
__Lemma 2.__  If $R \subseteq S$ as subsets of $X \times Y$, then $\forall_Y R \subseteq \forall_Y S$.
 
__Proof.__  From the last post, we have an adjunction:

$$T \times Y \subseteq S \quad if and only if \quad T \subseteq \forall_Y S$$

for any subset of $T \subseteq X$.  So it suffices to show $\forall_Y R \times Y \subseteq S$.  But

$$\forall_Y R \times Y \subseteq R \subseteq S$$

where the first inclusion follows from $\forall_Y R \subseteq \forall_Y R$.  $\Box$
 
Next, recall from the [last post](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic) that the internal intersection of $F : 1 \to PPX$ was defined by interpreting the following formula on the right:

$$\displaystyle \bigcap F = \forall_{S \in PX} (S \in_{PX} F) \Rightarrow (x \in_X S)$$

__Lemma 3.__  If $F \leq G : 1 \to PPX$, then $\displaystyle \bigcap G \leq \bigcap F : 1 \to PX$.
 
__Proof.__  $F : 1 \to PPX$ classifies the subset $\{ S \in PX : S \in_{PX} F \}$, _i.e._, $F$ is identified with the predicate $S \in_{PX} F$ in the argument $S$, so by hypothesis $(S \in_{PX} F) \leq (S \in_{PX} G)$ as predicates on $S$.  Internal implication $a \Rightarrow b$ is contravariant in the argument $a$ [see the following remark], so

$$\left[(S \in G) \Rightarrow (x \in S)\right] \leq \left[(S \in F) \Rightarrow (x \in S)\right]$$

Now apply Lemma 2 to complete the proof.  $\Box$

: __Remark.__  The contravariance of $- \Rightarrow b$, that is, the fact that $x \leq y$ implies $(y \Rightarrow b) \leq (x \Rightarrow b)$, is a routine exercise using the adjunction [discussed last time] $a \wedge c \leq b$ if and only if $c \leq (a \Rightarrow b).$
 
: Indeed, we have
 
$$x \wedge (y \Rightarrow b) \leq y \wedge (y \Rightarrow b) \leq b \qquad (*)$$
 
: where the first inequality follows from the hypothesis $x \leq y$, and the second follows from $y \Rightarrow b \leq y \Rightarrow b$.  By the adjunction, the inequality (*) implies $(y \Rightarrow b) \leq (x \Rightarrow b)$.  $\Box$

__Theorem 1.__  For subsets $A, B$ of $X$, the subset $A \cup B$ is an upper bound of $A$ and $B$, _i.e._, $A, B \subseteq A \cup B$.
 
__Proof.__  It suffices to prove that $\displaystyle A = \bigcap \{C \in PX : A \subseteq C\}$, since then we need only apply Lemma 3 to the trivially true inclusion
 
$$\{ C \in PX : A \subseteq C \} \:\cap\: \{ C \in PX : B \subseteq C \} \subseteq \{ C \in PX : A \subseteq C \}$$
 
to infer $A \subseteq A \cup B$, and similarly $B \subseteq A \cup B$.  (Actually, we need only show $\displaystyle A \subseteq \bigcap \{ C \in PX : A \subseteq C \}$.  We'll do that first, and then show full equality.)
 
The condition we want,

$$A \subseteq \{ x \in X : \forall_{S \in PX} (A \subseteq S) \Rightarrow (x \in_X S) \},$$

is, by the adjunction $(- \times PX) \dashv \forall_{PX} : Sub(X \times PX) \to Sub(X)$, equivalent to

$$A \times PX \subseteq \{ (x, S) : A \subseteq S \Rightarrow (x \in_X S) \}$$

which, by a $\wedge$-$\Rightarrow$ adjunction, is equivalent to

$$(A \times PX) \cap (X \times \{ S \in PX : A \subseteq S \}) \subseteq \: \in_X \qquad (1)$$

as subsets of $X \times PX$.  So we just have to prove (1).  At this point we recall, from our earlier analysis, that

$$\{ S \in PX : A \subseteq S \} = \{ S \in PX : \forall_{x \in X} x \in_X A \Rightarrow x \in_X S \}$$

Using the adjunction $(X \times -) \dashv \forall_X$, as in the proof of Lemma 2, we have
 
$$X \times \{ S \in PX : \forall_{x \in X} x \in_X A \Rightarrow x \in_X S \}$$
 
$$\subseteq \{ (x, S) : x \in_X A \Rightarrow x \in_X S \} := (A \times PX) \Rightarrow \in_X,$$
 
which shows that the left side of (1) is contained in

$$(A \times PX) \cap ((A \times PX) \Rightarrow \in_X) \subseteq \: \in_X,$$

where the last inclusion uses another $\wedge$-$\Rightarrow$ adjunction.  Thus we have established (1) and therefore also the inclusion

$$\displaystyle A \subseteq \bigcap \{S \in PX : A \subseteq S\}$$

Now we prove the opposite inclusion

$$\displaystyle \bigcap \{ S \in PX : A \subseteq S \} \subseteq A,$$

that is to say

$$\{ x \in X : \forall_{S \in PX} A \subseteq S \Rightarrow x \in_X S \} \subseteq A \qquad (**)$$

Here we just use Lemma 1, applied to the particular element $\chi_A : 1 \to PX$:  we see that the left side of $(**)$ is contained in

$$\{ x \in X : A \subseteq \left[\chi_A\right] \Rightarrow x \in_X A\}$$

which collapses to $\{ x \in X : x \in_X A \} = A$, since $A = \left[\chi_A\right]$.  This completes the proof.  $\Box$
 
__Theorem 2.__  $A \cup B$ is the least upper bound of $A, B$, _i.e._, if $C \subseteq X$ is a subset containing both $A \subseteq X$ and $B \subseteq X$, then $A \cup B \subseteq C$.
 
__Proof.__  We are required to show that

$$\{ x \in X : \forall_{S \in PX} \: (A \subseteq S \wedge B \subseteq S) \Rightarrow x \in_X S \} \subseteq C.$$

Again, we just apply Lemma 1 to the particular element $\chi_C : 1 \to PX$: the left-hand side of the claimed inclusion is contained in

$$\{ x \in X : (A \subseteq C \wedge B \subseteq C) \Rightarrow x \in_X C \}$$

but since $(A \subseteq C \wedge B \subseteq C)$ is true by hypothesis (is globally true as a predicate on the implicit variable $x \in X$), this last subset collapses to

$$\{ x \in X : t_X \Rightarrow x \in_X C \} = \{ x \in X : x \in_X C \} = C$$

which completes the proof.  $\Box$
 
Theorems 1 and 2 show that for any set $X$, the external poset $Sub(X)$ admits joins.  One may go on to show (just on the basis of the topos axioms) that as in the case of meets, the global external operation of taking joins is natural in $X$, so that by the Yoneda principle, it is classified by an internal join operation

$$\vee : P1 \times P1 \to P1,$$

namely, the map which classifies the union of the subsets

$$\displaystyle \left[\pi_1\right] = P1 \times 1 \stackrel{1 \times t}{\hookrightarrow} P1 \times P1$$
 
$$\displaystyle \left[\pi_2\right] = 1 \times P1 \stackrel{t \times 1}{\hookrightarrow} P1 \times P1$$

and this operation satisfies all the expected identities.  In short, $P1$ carries an internal Heyting algebra structure, as does $PX \cong P1^X$ for any set $X$.
 
We will come back to this point later, when we show (as a consequence of strong extensionality) that $P1$ is actually an internal Boolean algebra.

### Construction of Coproducts ###

Next, we construct coproducts just as we do in ordinary set theory:  as disjoint unions.  Letting $X, Y$ be sets (objects in an ETCS category), a _disjoint union_ of $X$ and $Y$ is a pair of monos

$$i : X \hookrightarrow Z \qquad j : Y \hookrightarrow Z$$

whose intersection is empty, and whose union or join in $Sub(Z)$ is all of $Z$.  We will show that disjoint unions exist and are essentially unique, and that they satisfy the universal property for coproducts. We will use the notation $X + Y$ for a disjoint union.
 
__Theorem 3.__  A disjoint union of $X$ and $Y$ exists.
 
__Proof.__  It's enough to embed $X, Y$ disjointly into _some_ set $C$, since the union of the two monos in $Sub(C)$ would then be the requisite $Z$.  The idea now is that if a disjoint union or coproduct $X+Y$ exists, then there's a canonical isomorphism $P(X + Y) \cong PX \times PY$.  Since the singleton map

$$\sigma : X + Y \to P(X + Y) \cong PX \times PY$$

is monic, one thus expects to be able to embed $X$ and $Y$ disjointly into $PX \times PY$.  Since we can easily work out how all this goes in ordinary naive set theory, we just write out the formulas and hope it works out in ETCS.
 
In detail, define $i_X: X \to PX \times PY$ to be
$$ \displaystyle X \cong X \times 1 \stackrel{\sigma_X
\times \chi_0}{\to} PX \times PY$$
where $\sigma_X$ is the singleton mapping and $\chi_0$
classifies $0 \hookrightarrow Y$; similarly, define $i_Y:
Y \to PX \times PY$ to be
$$ \displaystyle Y \cong 1 \times Y \stackrel{\chi_0
\times \sigma_Y}{\to} PX \times PY.$$
Clearly $i_X$ and $i_Y$ are monic, so to show disjointness
we just have to show that their pullback is empty. But their pullback
is isomorphic to the cartesian product of the pullbacks of the
diagrams
$$ \displaystyle X \stackrel{\sigma_X}{\to} PX
\stackrel{\chi_0}{\leftarrow} 1 \qquad 1 \stackrel{\chi_0}{\to} PY
\stackrel{\sigma_Y}{\leftarrow} Y$$
so it would be enough to show that each (or just one) of these two
pullbacks is empty, let's say the first.
 
Suppose given a map $h: A \to X$ which makes the square

<pre>
  A -------> 1
  |          |
h |          | chi_0
  V sigma_X  V
  X -------> PX
</pre>

commute. Using the pullback principle, the map $A \to 1
\stackrel{\chi_0}{\to} PX$ classifies
$$ 0 \times A \hookrightarrow X \times A$$
which is just the empty subset. This must be the same subset as
classified by $\sigma_X h = \chi_{\delta}h$ (where $
\delta: X \hookrightarrow X \times X$ is the diagonal), which by the
pullback principle is
$$ (1_X \times h)^{-1}(\delta) \hookrightarrow X
\times A.$$
An elementary calculation shows this to be the equalizer of the pair of maps
$$ \pi_1, h\pi_2: X \times A \stackrel{\to}{\to} X$$
So this equalizer $E$ is empty. But notice that $\langle
h, 1 \rangle: A \to X \times A$ equalizes this pair of maps. Therefore
we have a map $A \to E \cong 0$. By corollary 2 above, we infer
$ A \cong 0$. This applies to the case where $A$ is the
pullback, so the pullback is empty, as was to be shown. $\Box$
 
__Theorem 4.__  Any two disjoint unions of $X, Y$
are canonically isomorphic.
 
__Proof.__  Suppose $i: X \to Z \leftarrow Y: j$ is
a disjoint union. Define a map
$$ \phi= \langle \phi_1, \phi_2 \rangle: Z \to PX
\times PY$$
where $\phi_1: Z \to PX$ classifies the subset $\langle
1_X, i \rangle: X \to X \times Z$, and $\phi_2: Z \to PY$
classifies the subset $\langle 1_Y, j \rangle: Y \to Y \times
Z$. Applying the pullback principle, the composite $\phi_1 i: X
\to PX$ classifies
$$ (1_X \times i)^{-1}(\langle 1_X, i \rangle)
\hookrightarrow X \times X$$
which is easily seen to be the diagonal on $X$. Hence $
\phi_1 i = \sigma_X$. On the other hand, $\phi_1 j: Y \to PX$
classifies the subset
$$ (1_X \times j)^{-1}(\langle 1_X, i \rangle)
\hookrightarrow X \times Y$$
which is empty because $i$ and $j$ are disjoint
embeddings, so $\phi_1 j = \chi_0: Y \to PX$. Similar
calculations yield
$$ \phi_2 i = \chi_0: X \to PY \qquad \phi_2 j =
\sigma_Y: Y \to PY.$$
Putting all this together, we conclude that $\phi i = i_X: X \to
PX \times PY$ and $\phi j = i_Y: Y \to PX \times PY$, where
$ i_X$ and $i_Y$ were defined in the proof of theorem 3.
 
Next, we show that $\phi$ is monic. If not, then by strong
extensionality, there exist distinct elements $c, d: 1 \to Z$
for which $\phi(c) = \phi(d)$; therefore, $\phi_1 c =
\phi_1 d: 1 \to PX$ and $\phi_2 c = \phi_2 d: 1 \to PY$. By the
pullback principle, these equations say (respectively)
$$ c^{-1}(i) = d^{-1}(i) \hookrightarrow 1 \qquad
c^{-1}(j) = d^{-1}(j) \hookrightarrow 1$$
If $c^{-1}(i) = 1$, then both $c, d: 1 \to Z$ factor
through the mono $i: X \to Z$. However, since $\phi i =
i_{X}$ is monic, this would imply that $\phi (c) \neq \phi (d)$,
contradiction. Therefore $c^{-1}(i) = c \cap i = 0$. By similar
reasoning, $c \cap j = 0$. Therefore
$$ i \subseteq \neg c \qquad j \subseteq \neg c$$
where $\neg = (- \Rightarrow 0): Sub(Z) \to Sub(Z)$ is the
negation operator. But then $i \cup j \subseteq \neg c$. And
since $1: Z \hookrightarrow Z$ is the union $i \cup j$ by
assumption, $\neg c$ must be the top element $\top \in
Sub(Z)$, whence $c: 1 \to Z$ is the bottom element 0. This
contradicts the assumption that the topos is nondegenerate. Thus we
have shown that $\phi$ must be monic.
 
The argument above shows that $\phi: Z \hookrightarrow PX \times
PY$ is an upper bound of $i_X: X \to PX \times PY$ and $
i_Y: Y \to PX \times PY$ in $Sub(PX \times PY)$. It follows that
the join $X + Y$ constructed in theorem 3 is contained in $
\phi: Z \to PX \times PY$, and hence can be regarded as the join of
$ X$ and $Y$ in $Sub(Z)$. But $Z$ is their join
in $Sub(Z)$ by assumption of being a disjoint union, so the
containment $X + Y \subseteq Z$ must be an equality. The proof
is now complete. $\Box$
 
__Theorem 5.__  The inclusions $i_X : X \to X + Y$, $i_Y : Y \to X + Y$ exhibit $X + Y$ as the coproduct of $X$ and $Y$.

__Proof.__  Let $f : X \to B$, $g : Y \to B$ be given functions.  Then we have monos

$$\langle 1_X, f \rangle : X \hookrightarrow X \times B \qquad \langle 1_Y, g \rangle : Y \hookrightarrow Y \times B \qquad (1)$$

Now the operation $- \times B : Sub(C) \to Sub(C \times B)$ certainly preserves finite meets, and also preserves finite joins because it is left adjoint to $\forall_B : Sub(C \times B) \to Sub(C)$.  Therefore this operation preserves disjoint unions;  we infer that the monos

$$X \times B \stackrel{i_X \times B}{\to} (X + Y) \times B \qquad Y \times B \stackrel{i_Y \times B}{\to} (X + Y) \times B \qquad (2)$$

exhibit $(X + Y) \times B$ as a disjoint union of $X \times B, Y \times B$.  Composing the monos of (1) and (2), we have disjoint embeddings of $X$ and $Y$ in $(X + Y) \times B$.  Using Theorem 4, $X + Y$ is isomorphic to the join of these embeddings;  this means we have an inclusion

$$\langle 1, h \rangle : X + Y \hookrightarrow (X + Y) \times B$$

whose restriction to $X$ yields $\langle i_X, f \rangle$ and whose restriction to $Y$ yields $\langle i_Y, g \rangle$.  Hence $h : X + Y \to B$ extends $f$ and $g$.  It is the unique extension, for if there were two extensions $h, h'$, then their equalizer would be an upper bound of $X, Y$ in $Sub((X + Y) \times B)$, contradicting the fact that $X + Y$ is the least upper bound.  This completes the proof.  $\Box$

I think that's enough for one day.  I will continue to explore the categorical structure and logic of ETCS next time.
