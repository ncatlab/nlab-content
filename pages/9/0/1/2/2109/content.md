#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A **2-category equipped with proarrows**, also called a *proarrow equipment* or simply an *equipment*, is a [[2-category]] together with extra "proarrows" which enable one to reproduce more category theory inside it than is possible in a general 2-category.  The ur-example is [[Cat]] equipped with [[profunctors]].

## Motivation ##

Just as ordinary [[category theory]] provides a framework in which one can do "formal mathematics," one of the (many) purposes of [[higher category theory]] is to provide a framework in which one can do "formal category theory."  In particular, many concepts in ordinary category theory can be interpreted internally in a [[2-category]], in a way which specializes to the original concept in [[Cat]].  Examples of such concepts include [[adjunctions]], [[monads]], [[Grothendieck fibrations]], [[Kan extensions]], and [[fully faithful morphisms]].

However, these internalizations are not always "correct" in every 2-category.  For instance, in the 2-category $V Cat$ of [[enriched categories|categories enriched]] in a [[monoidal category]] $V$, internal adjunctions and monads give the correct notion of $V$-adjunction and $V$-monad, but internal fully-faithfulness for a $V$-functor is weaker than the "correct" notion of $V$-fully-faithfulness.  More technically, in many cases the naive notion of Kan extension is not sufficient and one needs "pointwise" Kan extensions; with some more work these can also be defined in a 2-category, but the resulting notion (though correct in $Cat$) is not always correct in $V Cat$.

Furthermore, some concepts of category theory are difficult to interpret at all in a 2-category.  The notion of [[limit]] in ordinary category theory can be interpreted in a 2-category by identifying the limit of a functor $D\to C$ as its Kan extension along the unique functor $D\to *$.  However, in enriched category theory the more important notion is that of [[weighted limit]], and there is no straightforward way to interpret this in $V Cat$.

What is missing is that the 2-category $V Cat$ doesn't natively supply any information about the $V$-valued hom-functors in a 2-category.  (In $Cat$ these hom-functors can be recovered by looking at [[comma categories]], which can be interpreted internally as [[comma objects]]---in some sense this is what all the above internalizations are secretly doing.)  Thus, all of these problems can be remedied by equipping a 2-category with extra structure which describes these hom-functors, or more generally describes a notion of [[profunctor]].

There are several not-quite-equivalent ways to describe this extra structure.  One due to Street and Walters, called a [[Yoneda structure]], involves assigning to each object $A$ a "presheaf object" $P A$ and a "Yoneda arrow" $A\to P A$; a profunctor $A\to B$ is then identified with an arrow $B \to P A$.  The notion of *proarrow equipment*, due to Wood, instead postulates an additional bicategory of "proarrows" and specifies their relationship to the ordinary arrows.  One can then define fully faithful morphisms, pointwise Kan extensions, weighted limits, etc. relative to this structure, in a way which specializes to the correct notions in $V Cat$.


## Definitions ##

There are several equivalent ways to define proarrow equipments on a 2-category.

### Definition as a 2-functor

Let $K$ be a [[2-category]].  The following structure is said to **equip $K$ with proarrows**.

* A 2-category $M$, whose arrows are called *proarrows*.
* A functor $K\to M$ which is [[bijective-on-objects functor|bijective on objects]] and [[locally fully faithful functor|locally fully faithful]].  If $f\colon A\to B$ is a 1-morphism in $K$, we write its image in $M$ as $B(1,f)\colon A\nrightarrow B$.
* For each arrow $f\colon A\to B$ in $K$, the proarrow $B(1,f)\colon A\to B$ has a right adjoint in $M$, which we write as $B(f,1)$.

As usual on the nLab, here by [[2-category]] we mean a weak 2-category (aka [[bicategory]]) and by [[functor]] we mean a weak 2-functor (aka [[pseudofunctor]]).  However, in many or most examples, $K$ is in fact a [[strict 2-category]].

For a proarrow $H\colon B\to D$ and ordinary arrows $f\colon A\to B$ and $g\colon C\to D$, we write $H(g,f)$ for the composite $D(g,1) \circ  H \circ B(1,f)$; it is a proarrow from $A$ to $C$.  We also write $U_A$, $A(1,1)$, or simply $A$ for the identity proarrow $A\nrightarrow A$.

#### Terminology

We refer to the entire structure defined above as a **2-category equipped with proarrows** or a **2-category proarrow equipment**.  Those working in the field often use the term **proarrow equipment** or simply **equipment** for the entire structure.  We prefer "2-category equipped with proarrows" (or, equivalently, "pro-morphisms") for the following reasons:

* It conveys that we are talking about extra stuff added to a 2-category.  (Actually, it is "eka-stuff" or "2-stuff" in the sense of [stuff, structure, property](http://ncatlab.org/nlab/show/stuff,+structure,+property).)
* It includes the word "proarrow" which tells people what the extra stuff consists of, namely a generalization of [[profunctors]].
* It includes the word "equipment" which signals what is meant to readers who are familiar with that term.

We do sometimes avail ourselves of the shorter terminology "proarrow equipment," however, once we are clear what is under discussion.


#### Examples

For example, if $V$ is a (Benabou) [[cosmos]], the 2-category $K= V Cat$ of $V$-enriched categories is equipped with proarrows by the 2-category $M=V Mod$ of $V$-enriched profunctors, where $B(1,f)$ and $B(f,1)$ are the two ways of regarding a $V$-functor $f:A\to B$ as a profunctor, namely $B(-,f-)$ and $B(f-,-)$ (hence the notation in the general case).  Composition of $V$-profunctors is by [[tensor product]], i.e. [[coends]]; note that we require $V$ to be [[cocomplete category|cocomplete]] with colimist preserved by $\ten$ on both sides in order to form such associative tensor products.  In $V Cat$, $H(g,f)$ is the result of precomposing the profunctor $H:D^{op}\otimes B \to V$ with $g^{op}\otimes f$.

The other most common sorts of generalized category, such as [[internal categories]] in some category with pullbacks, and [[fibered categories]] over some base, are also naturally equipped with proarrows.  For internal categories in $S$, we require $S$ to have finite limits and coequalizers preserved by pullback in order for the bicategory of internal profunctors to have associative compositions.  (See "virtual equipments," below, for a context which avoids some of these restrictions on $V$ and $S$.)


### Definition as a double category

Given a 2-category $K$ equipped with proarrows, we can construct a [[double category]] having the same objects as $K$, whose vertical 1-cells are the arrows, whose horizontal 1-cells are the proarrows, and whose squares
$$\array{A & \overset{H}{\to} & C \\
  ^f\downarrow & \Downarrow & \downarrow^g\\
  B& \underset{K}{\to} & D}
$$
are the 2-cells $H \to K(g,f)$.  Note that if $K$ is a strict 2-category, then this is a [[pseudo double category]] (vertically strict and horizontally weak) while if $K$ and $M$ are both weak 2-categories, this double category is weak in both directions (like a [[double bicategory]]).

In $V Cat$, for example, the squares of the above form are transformations $H(b,a) \to K(g b,f a)$ natural in $a$ and $b$.  Arguably, this double category is a more fundamental and natural object than the 2-functor $V Cat \to V Prof$.  More generally, if $K$ is any 2-category equipped with proarrows, we can reconstruct $K$ and its proarrow equipment from the double category defined above, and we can characterize the double categories that arise in this way.

One way to state this characterization is that they are those in which every vertical 1-cell $f\colon A\to B$ has both a [[companion]] (namely $B(1,f)$) and a [[conjoint]] (namely $B(f,1)$).  One can then recover $K$ and $M$ as the 
[[vertical 2-category|vertical and horizontal 2-categories]], respectively, and the 2-functor $K\to M$ as the functor taking every vertical arrow to its companion.  Whenever a vertical arrow has both a companion $B(1,f)$ and a conjoint $B(f,1)$, we automatically have an adjunction $B(1,f)\dashv B(f,1)$, so this defines a proarrow equipment in the first sense.

Another, perhaps even more natural, way to characterize these double categories is as those with the following property: given any "niche"
$$\array{A & & B\\
  ^f\downarrow & & \downarrow^g\\
  C& \underset{K}{\nrightarrow} & D}$$
there exists a "universal" or "cartesian" filler square
$$\array{A & \overset{K(g,f)}{\to} & B\\
  ^f\downarrow & \Downarrow & \downarrow^g\\
  C& \underset{K}{\nrightarrow} & D}$$
with the property that any other square 
$$\array{X & \nrightarrow & Y\\
  ^{f h}\downarrow & \Downarrow & \downarrow^{g k}\\
  C& \underset{K}{\nrightarrow} & D}$$
factors through the universal one uniquely:
$$\array{X & \nrightarrow & Y\\
  ^{h}\downarrow & \exists! \Downarrow  & \downarrow^{k}\\
  A & \overset{K(g,f)}{\to} & B\\
  ^f\downarrow & \Downarrow & \downarrow^g\\
  C& \underset{K}{\nrightarrow} & D}$$
The profunctor $K(g,f)$ will, of course, turn out to be the same one we gave that name to earlier.  The proarrows $B(1,f)=U_B(id_B,f)$ and $B(f,1) = U_B(f,id_B)$ are then a special case of this construction.  We show that they are a companion and conjoint of $f$, respectively, as follows.

By factoring the identity square
$$\array{A & \overset{U_A}{\to} & A\\
  ^f\downarrow & ^{U_f}\Downarrow & \downarrow^f\\
  B  & \underset{U_B}{\to} & B}$$
through the universal fillers
$$\array{A & \overset{B(1,f)}{\to} & B\\
  ^f\downarrow &\Downarrow & \downarrow^{id}\\
  B & \underset{U_B}{\to} & B} \qquad\text{and}\qquad
\array{B & \overset{B(f,1)}{\to} & A\\
  ^{id}\downarrow &\Downarrow & \downarrow^{f}\\
  B & \underset{U_B}{\to} & B}
  $$
that define $B(1,f)$ and $B(f,1)$, we obtain additional squares
$$\array{A & \overset{U_A}{\to} & A\\
  ^f\downarrow &\Downarrow & \downarrow^{id}\\
  B & \underset{B(f,1)}{\to} & A} \qquad\text{and}\qquad
\array{A & \overset{U_A}{\to} & A\\
  ^{id}\downarrow &\Downarrow & \downarrow^{f}\\
  A & \underset{B(1,f)}{\to} & B}
  $$
such that the composites
$$\array{A & \overset{U_A}{\to} & A\\
  ^{id}\downarrow &\Downarrow & \downarrow^{f}\\
  A & \overset{B(1,f)}{\to} & B\\
  ^f\downarrow &\Downarrow & \downarrow^{id}\\
  B & \underset{U_B}{\to} & B} \qquad\text{and}\quad
\array{A & \overset{U_A}{\to} & A\\
  ^{id}\downarrow &\Downarrow & \downarrow^{f}\\
  A & \underset{B(1,f)}{\to} & B\\
  ^f\downarrow &\Downarrow & \downarrow^{id}\\
  B & \underset{U_B}{\to} & B}
$$
are both equal to $U_f$.  And using the uniqueness of factorization through the universal squares, we can conclude moreover that the composites
$$\array{A & \overset{U_A}{\to} & A & \overset{B(1,f)}{\to} & A\\
  ^{id}\downarrow &\Downarrow & \downarrow^{f} & \Downarrow & \downarrow^{id}\\
  A & \underset{B(1,f)}{\to} & B & \underset{U_B}{\to} & B}
\qquad\text{and}\qquad
\array{B & \overset{B(f,1)}{\to} & A & \overset{U_A}{\to} & A\\
  ^{id}\downarrow &\Downarrow & \downarrow^{f} & \Downarrow & \downarrow^{id}\\
  B & \underset{U_B}{\to} & B & \underset{B(f,1)}{\to} & A}
$$
are equal to the identity squares of $B(1,f)$ and $B(f,1)$ respectively.  These are the defining equations of a companion and a conjoint.

Finally, we record the following.

+-- {: .un_lemma}
###### Central Lemma
There is a natural bijection between squares of the form
$$\array{A_0 & \overset{H}{\to} & B_0\\
  ^{f_1}\downarrow && \downarrow^{g_1}\\
  A_1 && B_1\\
  ^{f_2}\downarrow & \Downarrow & \downarrow^{g_2}\\
  A_2 && B_2\\
  ^{f_3}\downarrow && \downarrow^{g_3}\\
  A_3 & \underset{K}{\to} & B_3 }$$
and squares of the form
$$\array{A_1 & \overset{A_1(f_1 ,1)}{\to} & A_0 & \overset{H}{\to} & B_0 & \overset{B_1(1,g_1)}{\to} & B_1\\
  ^{f_2}\downarrow && &\Downarrow & && \downarrow^{g_2}\\
  A_2 & \underset{A_3(1,f_3)}{\to} & A_3 & \underset{K}{\to} & B_3 & \underset{B_3(g_3 ,1)}{\to} & B_2.}$$
=--

One way to think of this is as saying that vertical arrows can be "slid around corners" to become horizontal arrows, turning them into the "representable proarrows" $B(1,f)$ or $B(f,1)$ (depending on whether you slid them "backwards" or "forwards" to get around the corner).  The bijection is just given by composing with the four special squares in the definition of companions and conjoints.  In particular, by a Yoneda argument, for any $f\colon A\to C$, $g\colon B\to D$, and $K\colon C\nrightarrow D$ we have
\[K(g,f) \cong C(1,f) \odot K \odot D(g,1) \label{coyon} \]
which was what we took as the the definition of $K(g,f)$ with the original definition of proarrow equipment.  Thus, the companions and conjoints determine the rest of the cartesian squares.  Note that this is an equipment-version of [Yoneda reduction](http://ncatlab.org/nlab/show/Yoneda+reduction).

In conclusion, we have three definitions of proarrow equipment:

* A 2-functor which is bijective on objects, locally fully faithful, and maps every 1-morphism to one having a right adjoint.
* A double category in which every vertical arrow has a companion and a conjoint.
* A double category in which every niche has a cartesian filler.

While the first definition is perhaps simpler, for some purposes the second and third definitions are preferable.  For instance, the definition of the 3-category of "2-categories equipped with proarrows" is much more naturally defined by viewing them as double categories.  (See Dominic Verity's thesis and Mike Shulman's paper on framed bicategories.)  It also generalizes better to situations in which not all proarrows have composites; see "virtual equipments," below.


### Related notions

There are a number of variations on the notion.

* [[virtual proarrow equipment]]
* [[1-category proarrow equipment]]
* [[(1,2)-category proarrow equipment]]

Some related concepts include:

* [[cartesian bicategory]]
* [[bicategory of relations]]
* [[allegory]]


## Category theory in a proarrow equipment ##

We now give a few examples of how to do category theory internal to a proarrow equipment.

### Homset definition of adjunctions

We start with this: two (vertical) arrows $f\colon A\to B$ and $g\colon B\to A$ are adjoint (in $\mathcal{V}(\underline{X})$) if and only if we have an isomorphism $B(f,1)\cong A(1,g)$.  Why?  Well, an adjunction $f\dashv g$ comes with a unit and a counit, which (expressed in $\underline{X}$) are of the form
$$\array{A & \overset{U_A}{\to} & A\\
  ^f\downarrow && \downarrow\\
  B & \overset{\eta}{\Leftarrow} & \downarrow^{id} \\
  ^g\downarrow && \downarrow\\
  A& \underset{U_A}{\to} & A} \qquad\text{and}\qquad
\array{B & \overset{U_B}{\to} & B\\
  \downarrow && \downarrow^g\\
  ^{id}\downarrow & \overset{\varepsilon}{\Leftarrow} & A \\
  \downarrow && \downarrow^f\\
  B& \underset{U_B}{\to} & B.}
$$
Applying the bijection of the Central Lemma, we see that $\eta$ corresponds to a map $B(f,1) \to A(1,g)$, and likewise $\varepsilon$ corresponds to a map $A(1,g)\to B(f,1)$.  The triangle identities for $\eta$ and $\varepsilon$ are then equivalent to saying that these two maps are inverse isomorphisms.  So we've recovered the classical equivalence between the "diagrammatic" and isomorphism-of-hom-sets definitions of an adjunction, in a purely formal way.

### Fully faithful arrows

An arrow $f:A\to B$ in a 2-category equipped with proarrows is said to be **fully faithful** if the canonical morphism $U_A\to B(f,f)$ is an isomorphism of proarrows $A\to A$.  In $V Cat$ this recaptures the correct notion of $V$-fully-faithful $V$-functor.

It is not hard to see, using the fact that $K\to M$ is locally fully faithful, that any fully-faithful arrow $f\colon A\to B$ is, in fact, internally fully-faithful in $K$ in the sense that $K(X,A)\to K(X,B)$ is fully faithful for all $X\in K$.  However, the converse fails in general.  But it is not hard to show that the two are equivalent if $f\colon A\to B$ has a left or right adjoint, using the above characterization of adjunctions.


### Limits

The notion of limit we end up in a 2-category equipped with prarrows with is actually more general than what you're probably used to, but this extra generality turns out to be useful.  Let $d\colon D\to C$ be an arrow and let $J\colon D\nrightarrow A$ be a proarrow; we're going to define what it means for an arrow $\ell\colon A\to C$ to be the *$J$-weighted limit* of $d$.  In the proarrow-equipped 2-category $V Cat$ of $V$-enriched categories, if $A$ is the [unit](http://ncatlab.org/nlab/show/unit+enriched+category) $V$-category $I$, then this will recover the usual notion of [weighted limit](http://ncatlab.org/nlab/show/weighted+limit).  Of course, in a general proarrow equipment we may not have a "unit object," so that extra generality is unavoidable; it's like using generalized elements in ordinary category theory.

To make things easier, let's assume that our proarrow equipment is *closed*, in the sense that composition of proarrows has adjoints in each variable
$$ \mathcal{H}(\underline{X})(H\odot K,L) \cong \mathcal{H}(\underline{X})(H,K\rhd L) \cong \mathcal{H}(\underline{X})(K,L\lhd H).$$
The Central Lemma implies that analogously to \eqref{coyon}, we have
\[K(g,f) \cong D(1,g)\rhd K \lhd C(f,1). \label{yon} \]
In $V\text{-}Prof$, the adjoints are given by the [ends](http://ncatlab.org/nlab/show/end)
$$ (K\rhd L)(b,a) = \int_{c\in C} [K(c,b), L(c,a)] $$
and
$$ (L \lhd H)(c,b) = \int_{a\in A} [H(b,a), L(c,a)]. $$
Therefore, \eqref{yon} is an abstract form of the Yoneda lemma, just as \eqref{coyon} is an abstract form of Yoneda reduction.

Now recall that for $V$-categories $D$ and $C$, an object $\ell\in C$ is a $J$-weighted limit of $d\colon D\to C$ if we have an isomorphism
$$
\begin{aligned}
C(-,\ell) &\cong [D,V](J, C(-,x))\\
&= \int_{x\in D} [J(x), C(-,d(x))].
\end{aligned}
$$
Thus it makes sense to define, in a closed proarrow equipment, an arrow $\ell\colon A\to C$ to be the $J$-weighted limit of $d$ if we have an isomorphism
$$ C(1,\ell) \cong C(1,d) \lhd J. $$
(If our proarrow equipment is not closed, we simply assert that $C(1,\ell)$ has the universal property that $C(1,d) \lhd J$ would have if it existed.  In other terminology, we assert that $C(1,\ell)$ is a *right lifting* of $C(1,d)$ along $J$ in the 2-category of proarrows.)  In particular, when $A$ is the unit $V$-category, this recovers the classical notion.  But even in $V Cat$ there are interesting examples for other values of $A$.  If we take $J = D(j,1)$ for some functor $j\colon A\to D$, then \eqref{coyon} and \eqref{yon} imply that
$$
\begin{aligned}
C(1,d) \lhd J &= C(1,d) \lhd D(j,1)\\
& \cong j^* C(1,d)\\
& \cong D(1,j) \odot C(1,d)\\
& \cong C(1,d j) 
\end{aligned}
$$
so that $\ell = d j$ is the $J$-weighted limit of $d$.  That is, $D(j,1)$-weighted limits are just given by composition with $j$.

More interestingly, one can show that if $J = D(1,k)$ for some $k\colon D\to A$, then $J$-weighted limits specialize to *pointwise* right Kan extensions along $k$.  That is, the extra data of a proarrow equipment lets us define the good notion of Kan extension (even in the enriched case) as a special case of a general notion of limit.  Thus, in a general 2-category equipped with proarrows, we *define* a "pointwise right Kan extension" along an arrow $k\colon D\to A$ to be a $D(1,k)$-weighted limit.  It is easy to show that any pointwise Kan extension is, in particular, an internal Kan extension in $K$, but as we have seen the converse fails in $V Cat$.


### Right adjoints preserve limits

Suppose that $\ell\colon A\to C$ is a $J$-weighted limit of $d\colon D\to C$ in the above sense, and let $g\colon C\to B$ be an arrow with a left adjoint $f\colon B\to C$.  We want to show that $g\ell$ is a $J$-weighted limit of $g d$.  But we have
$$
\begin{aligned}
B(1,g\ell) &\cong C(1,\ell) \odot B(1,g)\\
&\cong \big(C(1,d) \lhd J\big) \odot C(f,1)\\
&\cong C(1,f) \rhd \big(C(1,d) \lhd J\big)\\
&\cong \big(C(1,f) \rhd C(1,d)\big) \lhd J\\
&\cong \big(C(1,d) \odot C(f,1)\big) \lhd J\\
&\cong \big(C(1,d) \odot B(1,g)\big) \lhd J\\
&\cong B(1,g d) \lhd J.
\end{aligned}
$$
which is what we want.


## Graphs and cographs ##

As noted above, in the case of ordinary categories, the profunctors can in fact be recovered from the 2-category $Cat$.  Specifically, profunctors $A\to B$ can be identified with two-sided discrete fibrations from $B$ to $A$ (that is, spans $B \leftarrow C \to A$ such that $C \to B$ is a [[Grothendieck fibration|(Grothendieck) fibration]], $C\to A$ is an opfibration, the two structures are compatible, and each fiber of $C\to B\times A$ is discrete).  The two-sided fibration corresponding to a profunctor is also called its [[graph of a profunctor|graph]].  The same is true for internal categories, but not for enriched categories.

However the $V$-profunctors $A\to B$ *can* be recovered from the 2-category $V Cat$ in a different, and in fact dual, way: they are the two-sided _codiscrete cofibrations_ from $B$ to $A$, i.e. two-sided discrete fibrations in $(V Cat)^{op}$.  The two-sided cofibration corresponding to a profunctor is, unsurprisingly, its [[cograph of a profunctor|cograph]], also called its [[collage]].  This was first noticed by Street and subsequently expanded on by other authors.  In particular, one can write down axioms on a 2-category guaranteeing that its codiscrete cofibrations can be used to equip it with proarrows, and axioms on a proarrow equipment guaranteeing that it arises from codiscrete cofibrations.


## Virtual equipments ##

One can formulate a generalized notion of equipment which includes $V Cat$ for _any_ monoidal category $V$ (and in fact, any [[multicategory]]), and $Cat(S)$ for any category $S$ with pullbacks.  The precise definition is complicated, but the basic idea is not: we start from the double-category definition, and instead of composites of the horizontal (pro)arrows, we allow the squares to have domains that are arbitrary composable strings, like so:
$$\array{ & \to \to \dots \to &\\
  \downarrow & \Downarrow & \downarrow\\
  & \underset{}{\to}& .}$$
So far this is analogous to the generalization from monoidal categories to multicategories, and gives the notion of [[fc-multicategory]] (aka "virtual double category").  We then impose a condition analogous to the existence of companions and conjoints to obtain the notion of **virtual equipment** (see references).  Most of  category theory can be done in a virtual equipment just as well as in an equipment.


## Categories enriched in an equipment ##

For any equipment $W$ one can define a notion of **$W$-enriched category**.  This consists of

* a collection $ob(C)$ of objects,
* for each object $x$ an *extent* $e(x)$ which is an object of $W$,
* for each pair of objects $x,y$ a proarrow $hom_C(x,y):e(x)\to e(y)$,
* composition and identity-assigning 2-cells obeying associativity and unit axioms.

So far we have not used the ordinary arrows, so many authors have studied only the notion of "category enriched in a bicategory."  (Note that any 2-category $M$ can be regarded as the proarrow 2-category of an equipment in which the only ordinary arrows are identites.)  However, we need the extra structure when we define a *functor* $f:C\to D$ between $W$-enriched categories, which consists of:

* a function $f:ob(C)\to ob(D)$,
* for each object $x$ of $C$ an arrow $f_x:e(x)\to e(f(x))$ in $W$,
* for each pair of objects $x$ and $y$, a square
$$\array{e(y) & \overset{hom_C(x,y)}{\to} & e(x)\\
  ^{f_y}\downarrow & \Downarrow & \downarrow^{f_x}\\
  e(f(y))& \underset{hom_D(f(x),f(y))}{\to} & e(f(x))}$$
* satisfying functoriality axioms.

Finally, we define a *natural transformation* between such functors $f,g:C\to D$ to consist of

* squares
$$\array{e(x) & \overset{U_{e(x)}}{\to} & e(x)\\
  ^{g_x}\downarrow & \Downarrow & \downarrow^{f_x}\\
  e(g(x))& \underset{hom_D(f(x),f(y))}{\to} & e(f(x))}$$
* satisfying a naturality axiom.

By choosing $W$ appropriately, categories enriched in an equipment include most types of generalized category:

* If $W$ is a monoidal category $V$, regarded as a one-object bicategory and thence as an equipment with only one ordinary arrow (so the objects of $V$ are the proarrows of $W$), then $W$-enriched categories, functors, and natural transformations are the same as $V$-enriched ones.

* If $S$ has pullbacks, there is an equipment $Span(S)$ whose objects  and arrows are those of $S$ and whose proarrows are spans.  A category enriched in $Span(S)$ which has one object is the same as an internal category in $S$, and likewise for functors and transformations.  (Here it is essential to use an equipment, rather than merely a bicategory, to get the right notion of functor.)

* Arbitrary $Span(S)$-enriched categories can be identified with "locally small fibrations" over $S$, aka "locally internal categories" over $S$.

Other choices of $W$ give "categories which are both enriched and internal," for example:

* For a suitably nice category $S$ (such as a [[Grothendieck topos]]) there is an equipment $Ab(S)$ whose objects and arrows are those of $S$, and whose proarrows $A\to B$ are internal abelian group objects in $S/(B\times A)$.  An $Ab(S)$-enriched category with one object can be regarded as an "internal [[Ab-enriched category]]" in $S$.


## References ##

* R.J. Wood, "Abstract Proarrows I" and "Proarrows II" (the original definitions), and a number of following papers.

* [[Ross Street]], "Fibrations in bicategories" (Construction of $V Mod$ from $V Cat$.)

* [[Aurelio Carboni]], Scott Johnson, Ross Street, and Dominic Verity, "Modulated bicategories" (Improved construction of $V Mod$ from $V Cat$.)

* [[Dominic Verity]], "Enriched categories, internal categories, and change of base", Ph.D. Thesis.  (The connection with double categories.)

* [[Michael Shulman]], "Framed bicategories and monoidal fibrations".  (The equivalence with certain double categories, there called *framed bicategories*, and a general way to construct equipments such as $Ab(S)$.)

* G.S.H Cruttwell and Michael Shulman, "A unified framework for generalized multicategories" (currently the only reference for virtual equipments).

* [[Renato Betti]], Aurelio Carboni, Ross Street, and [[Robert Walters]], "Variation through enrichment."  (Locally small fibrations as $Span$-enriched categories.)

A blog post surveying ideas of proarrow equipments, much of which has been copied over to this page:

* [[Mike Shulman]], _Equipments_ ([blog](http://golem.ph.utexas.edu/category/2009/11/equipments.html))


[[!redirects equipment]]
[[!redirects equipments]]
[[!redirects proarrow equipment]]
[[!redirects proarrow equipments]]
[[!redirects pro-arrow equipment]]
[[!redirects pro-arrow equipments]]
[[!redirects 2-category equipment]]
[[!redirects proarrow]]
[[!redirects proarrows]]
[[!redirects virtual equipment]]
[[!redirects virtual proarrow equipment]]
[[!redirects 2-category equipped with pro-arrows]]
