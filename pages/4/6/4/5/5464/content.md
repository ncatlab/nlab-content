
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

> This page contains the beginning of the LaTeX-to-instiki conversion of an article to be submitted for peer-review to the [[annals:HomePage|Annals of the nLab]].

* [[Tom Leinster]], _An informal introduction to topos theory_ ([arXiv:1012.5647](http://arxiv.org/abs/1012.5647))

#An informal introduction to topos theory#
* table of contents
{:toc}

## Abstract

This short expository text is for readers who are confident in basic [[category theory]] but know little or nothing about [[toposes]]. It is based on some impromptu talks given to a small group of [[category theory|category theorists]]. 

## Introduction

This short text is for readers who are confident in basic 
[[category theory]] but know little or nothing about [[toposes]].  It is based on some impromptu talks
given to a small group of category theorists.  I am no expert on topos theory. These notes are for people even less expert than me.

In keeping with the spirit of the talks, what follows is light on both detail and references.  For the reader wishing for more, almost everything here is presented in respectable form in Mac Lane and Moerdijk's very pleasant introduction to topos theory ([MacLaneMoerdijk](#MacLaneMoerdijk)).  Nothing here is new, not even
the expository viewpoint (very loosely inspired by ([JohSE](#JohSE))).

As a rough indication of the level of knowledge assumed, I will take it that you are totally comfortable with the [[Yoneda lemma]] and the concept of [[cartesian closed category]], but I will not assume that you know the definition of [[subobject classifier] or of [[topos]].

Section~\ref{sec:defn} explains the definition of topos.  The remaining three
sections discuss some of the connections between topos theory and other subjects.  There are many more such connections than I will mention; I hope it is abundantly clear that these notes are, by design, a quick sketch of a large subject.

[Section 1](#TheDefinitionOfTopos) is on connections between 
[[topos theory]] and [[set theory]].
The major theme there is that we can use topos theory to free ourselves from the shackles of [[ZFC]].  The minor theme is that  

+-- {: .standout}

a topos is a generalized [[Set|category of sets]]

=--

[Seciton 2](#ToposesAndSetTheory) is on connections with [[geometry]] (in a broad sense); there the thought is that

+-- {: .standout}

a topos is a generalized [[space]]

=--

[Section 3](#ToposesAndGeometry) is on connections with 
[[universal algebra]]:

+-- {: .standout}

a topos is a generalized [[theory]]

=--

What this means is that there is one topos embodying the concept of "[[ring]]", another embodying the concept of "[[field]]", and so on.  This is the story of [[classifying toposes]].

Sections 2 - 4 can be read in any order, except
that ideally 3 (geometry) should come
before 4 (universal algebra).  You _can_ read 4 without having 
read 2, but the price to pay is that the notion of 
"[[geometric morphism]]" -- defined in 3 and used in 4 -- might seem rather mysterious.

Algebraic geometers beware: the word "topos" is used by mathematicians in two slightly different senses, according to circumstance and culture.  There are [[elementary toposes]] and [[Grothendieck toposes]].  Category theorists tend to use
"topos" to mean "elementary topos" by default, although Grothendieck toposes are also important in category theory.  But when an algebraic geometer says "topos", they almost certainly mean "Grothendieck topos" (what else?).

Grothendieck toposes are [[categories of sheaves]]. Elementary toposes are slightly more general, and the definition is simpler.  They are what I will  emphasize here.  Grothendieck toposes are the subject of
Section 3, and appear fleetingly elsewhere; but if you only want
to learn about categories of sheaves, this is probably not the text for you.

**Acknowledgements** (...)

## **1.)** The  definition of topos {#TheDefinitionOfTopos}

The hardest part of the definition of [[topos]] is the concept of [[subobject classifier]], so I will begin there.

In the [[Set|category of sets]], inverse images are a special case of [[pullback]]s. That is, given a [[function|map]] $f \colon X \to Y$ of [[set]]s and a [[subset]] $B \sub Y$, we have a
[[pullback]] [[diagram|square]]

$$
  \array{
    f^{-1} B &\to& B
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& Y 
  }
  \,.
$$

(...)

## **2.)** Toposes and set theory {#ToposesAndSetTheory}

(...)

## **3.)** Toposes and geometry {#ToposesAndGeometry}

(...)

## **4.)** Toposes and universal algebra {#ToposesAndGeometry}

(...)

## References

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
{#MacLaneMoerdijk}

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ (2003)
{#JohSE}

(...)

category: reference

----

## informal introduction to topos theory ##
### Tom Leinster ###

+-- {: .flushright}
School of Mathematics and Statistics,  
University of Glasgow,  
Glasgow G12 8QW,  
UK;  
Tom.Leinster@glasgow.ac.uk.  
Supported by an EPSRC Advanced Research Fellowship.
=--

* tic
{: .toc}

This short text is for readers who are confident in basic category theory but
know little or nothing about toposes.  It is based on some impromptu talks
given to a small group of category theorists.  I am no expert on topos theory.
These notes are for people even less expert than me.

In keeping with the spirit of the talks, what follows is light on both detail
and references.  For the reader wishing for more, almost everything
here is presented in respectable form in Mac Lane and Moerdijk's very pleasant
introduction to topos theory (\citeyear{MM}).  Nothing here is new, not even
the expository viewpoint (very loosely inspired by \citet{JohSE}).

As a rough indication of the level of knowledge assumed, I will take it that
you are totally comfortable with the Yoneda Lemma and the concept of
cartesian closed category, but I will not assume that you know the definition
of subobject classifier or of topos.

Section~\ref{sec:defn} explains the definition of topos.  The remaining three
sections discuss some of the connections between topos theory and other
subjects.  There are many more such connections than I will mention; I hope it
is abundantly clear that these notes are, by design, a quick sketch of a
large subject.

Section~\ref{sec:sets} is on connections between topos theory and set theory.
The major theme there is that we can use topos theory to free ourselves from
the shackles of ZFC.  The minor theme is that 
% 
+-- {: .center}
a topos is a generalized category of sets.
=--

Section~\ref{sec:geom} is on connections with geometry (in a broad sense);
there the thought is that
% 
+-- {: .center}
a topos is a generalized space.
=--

Section~\ref{sec:univ-alg} is on connections with universal algebra:
% 
+-- {: .center}
a topos is a generalized theory.
=--
% 
What this means is that there is one topos embodying the concept of `ring',
another embodying the concept of `field', and so on.  This is the story of
classifying toposes.

\setlength{\templength}{\parindent}
\noindent
\parbox{.7\textwidth}{%
\setlength{\parindent}{\templength}
Sections~\ref{sec:sets}--\ref{sec:univ-alg} can be read in any order, except
that ideally~\S\ref{sec:geom} (geometry) should come
before~\S\ref{sec:univ-alg} (universal algebra).  You *can*
read~\S\ref{sec:univ-alg} without having read~\S\ref{sec:geom}, but the price
to pay is that the notion of `geometric morphism'---defined in~\S\ref{sec:geom}
and used in~\S\ref{sec:univ-alg}---might seem rather
mysterious.}%
% 
\parbox{.05\textwidth}{\ \ \ \ }
% 
\parbox{.25\textwidth}{%
\setlength{\unitlength}{1em}
% \setlength{\fboxsep}{0pt}
% \fbox{%
\begin{picture}(8,7.5)(1.2,1)
\cell{5}{8}{t}{1}
\cell{1.7}{4}{c}{2}
\cell{5}{4}{c}{3}
\cell{8.8}{2}{c}{4}
\put(4.5,7){\line(-1,-1){2.3}}
\put(5,7){\line(0,-1){2.3}}
\put(5.5,7){\line(2,-3){3}}
\qbezier[12](5.5,3.5)(6.8,2.85)(8.1,2.2)
\end{picture}%}
}

Algebraic geometers beware: the word `topos' is used by mathematicians in two
slightly different senses, according to circumstance and culture.  There are
elementary toposes and Grothendieck toposes.  Category theorists tend to use
`topos' to mean `elementary topos' by default, although Grothendieck toposes
are also important in category theory.  But when an algebraic geometer says
`topos', they almost certainly mean `Grothendieck topos' (what else?).

Grothendieck toposes are categories of sheaves.  Elementary toposes are
slightly more general, and the definition is simpler.  They are what I will 
emphasize here.  Grothendieck toposes are the subject of
Section~\ref{sec:geom}, and appear fleetingly elsewhere; but if you only want
to learn about categories of sheaves, this is probably not the text for you.

\paragraph*{Acknowledgements}  I thank Andrei Akhvlediani, Eugenia Cheng,
Richard Garner, Nick Gurski, Ignacio Lopez Franco and Emily Riehl for their
participation and encouragement.  Aspects of Section~\ref{sec:univ-alg} draw
on a vaguely similar presentation of vaguely similar material by Richard
Garner.  I thank the organizers of Category Theory 2010 for making the talks
possible, even though they did not mean to: Francesca Cagliari, Eugenio
Moggi, Marco Grandis, Sandra Mantovani, Pino Rosolini, and Bob Walters.  The
commutative diagrams were made using Paul Taylor's macros.  



### The definition of topos ###
\label{sec:defn}


The hardest part of the definition of topos is the concept of subobject
classifier, so I will begin there.

In the category of sets, inverse images are a special case of pullbacks.
That is, given a map $f\colon X \to Y$ of sets and a subset $B \subseteq Y$, we have a
pullback square
\[
\begin{diagram}
f^{-1}B\SEpbk   &\rTo   &B      \\
\dIncl          &       &\dIncl \\
X               &\rTo_f &Y.     \\
\end{diagram}
\]
In particular, this holds when $B$ is a 1-element subset $\{y\}$ of $Y$:
\[
\begin{diagram}
f^{-1}\{y\}\SEpbk         &\rTo   &\{y\}  \\
\dIncl                  &       &\dIncl \\
X                       &\rTo_f &Y.     \\
\end{diagram}
\]
There is no virtue in distinguishing between one-element sets, so we might as
well write $1$ instead of $\{y\}$; then the inclusion $\{y\} \hookrightarrow Y$ becomes
the map $1 \to Y$ picking out $y \in Y$, and we have a pullback square
\[
\begin{diagram}
f^{-1}\{y\}\SEpbk       &\rTo^! &1      \\
\dIncl                  &       &\dTo>y \\
X                       &\rTo_f &Y.     \\
\end{diagram}
\]

Next consider characteristic functions of subsets.  Fix a two-element set $2 =
\{\tr, \fa\}$ (`true' and `false').  Then for any set $X$, the subsets of $X$
are in bijective correspondence with the functions $X \to 2$.  In one
direction, given a subset $A \subseteq X$, the corresponding function $\chi_A\colon X
\to 2$ is defined by
\[
\chi_A(x)
=
\begin{cases}
\tr     &\text{if } x \in A     \\
\fa     &\text{if } x \not\in A
\end{cases}
\]
($x \in X$).  In the other, given a function $\chi\colon X \to 2$, the
corresponding subset of $X$ is $\chi^{-1}\{\tr\}$.  To say that this latter
process $\chi \mapsto \chi^{-1}\{\tr\}$ is a bijection is to say that for all
$A \subseteq X$, there is a unique function $\chi\colon X \to 2$ such that $A =
\chi^{-1}\{\tr\}$.  In other words: for all $A \subseteq X$, there is a unique
function $\chi\colon X \to 2$ such that
\[
\begin{diagram}
A       &\rTo^!         &1              \\
\dIncl  &               &\dTo>\tr       \\
X       &\rTo_\chi      &2              \\
\end{diagram}
\]
is a pullback square.

This property of sets can now be stated in purely categorical terms.  We use
$\monic$ to indicate a mono ($=$ monomorphism $=$ monic).  

\begin{defn}
Let $\mathscr{E}$ be a category with a terminal object, $1$.  A \demph{subobject
classifier} in $\mathscr{E}$ is an object $\Omega$ together with a map $\tr\colon 1 \to
\Omega$ such that for every mono $A \monicby{m} X$ in $\mathscr{E}$, there exists a
unique map $\chi\colon X \to \Omega$ such that
\[
\begin{diagram}
A       &\rTo^!         &1              \\
\dMono&lt;m&               &\dTo>\tr       \\
X       &\rTo_\chi      &\Omega         \\
\end{diagram}
\]
is a pullback square.
\end{defn}

So, we have just observed that $\Set$ has a subobject classifier, namely, the
two-element set.  In the general setting, we may write $\chi$ as $\chi_A$ (or
properly, $\chi_m$) and call it the \demph{characteristic function} of $A$ (or
$m$).

To understand this further, we need two lemmas.

\begin{lemma}   \label{lemma:pb-mono}
In any category, the pullback of a mono is a mono.  That is, if
\[
\begin{diagram}
\cdot           &\rTo   &\cdot  \\
\dTo&lt;{m'}       &       &\dTo>m \\
\cdot           &\rTo   &\cdot  \\
\end{diagram}
\]
is a pullback square and $m$ is a mono, then so is $m'$.  
\end{lemma}

\begin{lemma}
In any category with a terminal object $1$, every map out of $1$ is a mono.
\end{lemma}

So, pulling $\tr\colon 1 \to \Omega$ back along *any* map $X \to \Omega$
gives a mono into $X$.

It will also help to know the result of the following little exercise.  It
says, roughly, that in the definition of subobject classifier, the fact that
$1$ is terminal comes for free.

\begin{fact}    \label{fact:one-terminal}
Let $\mathscr{E}$ be a category and let $T \monicby{\tr} \Omega$ be a mono in $\mathscr{E}$.
Suppose that for every mono $A \monicby{m} X$ in $\mathscr{E}$, there is a unique map
$\chi\colon X \to \Omega$ such that there is a pullback square
\[
\begin{diagram}
A               &\rTo           &T              \\
\dMono&lt;m        &               &\dMono>\tr     \\
X               &\rTo_\chi      &\Omega.        \\
\end{diagram}
\]
Then $T$ is terminal in $\mathscr{E}$.
\end{fact}

This leads to a second description of subobject classifiers.  Let $\mathscr{Mono}(\mathscr{E})$
be the category whose objects are monos in $\mathscr{E}$ and whose maps are pullback
squares.  Then a subobject classifier is exactly a terminal object of
$\mathscr{Mono}(\mathscr{E})$.  

Here is a third way of looking at subobject classifiers.  Given a category
$\mathscr{E}$ and an object $X$, a \demph{subobject} of $X$ is officially an
isomorphism class of monos $A \monicby{m} X$ (where isomorphism is taken in the
slice category $\mathscr{E}/X$).  For example, when $\mathscr{E} = \Set$, two monos
\[
A \monicby{m} X, 
\quad
A' \monicby{m'} X
\]
are isomorphic if and only if they have the same image; so subobjects of $X$
correspond one-to-one with subsets of $X$.  I say `officially' because half
the time people use `subobject of $X$' to mean simply `mono into $X$', or slip
between the two meanings without warning.  It is a harmless abuse of
language, which I will adopt.   

For $X \in \mathscr{E}$, let $\subseteq(X)$ be the set of subobjects (in the official sense)
of $X$.  Assume that $\mathscr{E}$ is well-powered, that is, each $\subseteq(X)$ is a set
rather than a proper class.  Assume also that $\mathscr{E}$ has pullbacks.  By
Lemma~\ref{lemma:pb-mono}, every map $X \toby{f} Y$ in $\mathscr{E}$ induces a map
$\subseteq(Y) \toby{f^*} \subseteq(X)$ of sets, by pullback.  This defines a functor
$\subseteq\colon \mathscr{E}^\op \to \Set$.

Third description: a subobject classifier is a representation of this functor
$\subseteq$.

This makes intuitive sense, since for $\subseteq$ to be representable means that
there is an object $\Omega \in \mathscr{E}$ satisfying
\[
\subseteq(X) \cong \mathscr{E}(X, \Omega)
\]
naturally in $X \in \mathscr{E}$.  In the motivating case of the category of sets, this
directly captures the thought that subsets of a set $X$ correspond naturally
to maps $X \to \{\tr, \fa\}$.  

Now we show that this is equivalent to the original definition.  By the Yoneda
Lemma, a representation of $\subseteq\colon \mathscr{E}^\op \to \Set$ amounts to an object
$\Omega \in \mathscr{E}$ together with an element $\tr \in \subseteq(\Omega)$ that is
`generic' in the following sense:
% 
\begin{quote}
for every object $X \in \mathscr{E}$ and element $m \in \subseteq(X)$, there is a unique map
$\chi\colon X \to \Omega$ such that $\chi^*(\tr) = m$.
\end{quote}
% 
In other words, a representation of $\subseteq$ is a mono $T \monicby{\tr} \Omega$
in $\mathscr{E}$ satisfying the condition in Fact~\ref{fact:one-terminal}.  In other
words, it is a subobject classifier.

\begin{defn}
A \demph{topos} (or \demph{elementary topos}) is a cartesian closed category
with finite limits and a subobject classifier.
\end{defn}

\begin{examples}        \label{egs:toposes}
1.  
The primordial topos is $\Set$.  It has special properties not shared by most
other toposes.  This is the subject of Section~\ref{sec:sets}.

2.
For any set $I$, the category $\Set^I$ of $I$-indexed families of sets is a
topos.  Its subobject classifier is the constant family $(2)_{i \in I}$, where
$2$ is a two-element set.

3.
For any group $G$, the category $\Set^G$ of left $G$-sets is a topos.  Its
subobject classifier is the set $2$ with trivial $G$-action.

4.   \label{eg:topos-pshf}
Encompassing all the previous examples, if $\mathbb{A}$ is any small category
then the category $\widehat{\mathbb{A}} = \Set^{\mathbb{A}^\op}$ of presheaves on
$\mathbb{A}$ is a topos.  We can discover what its subobject classifier must be
by a thought experiment: *if* $\Omega$ is a subobject classifier then by
the Yoneda Lemma,
\[
\Omega(a) 
\cong
\widehat{\mathbb{A}}( \mathbb{A}(-, a), \Omega )
\cong
\subseteq(\mathbb{A}(-, a))
\]
for all $a \in \mathbb{A}$.  So $\Omega(a)$ must be the set of subfunctors of
$\mathbb{A}(-, a)$; and one can check that defining $\Omega(a)$ in this
way does indeed give a subobject classifier.  A subfunctor of
$\mathbb{A}(-, a)$ is called a \demph{sieve} on $a$; it is a collection of
maps into $a$ satisfying a certain condition. 

5. For any topological space $S$, the category $\mathscr{Sh}(S)$ of sheaves on $S$
is a topos.  This is the subject of Section~\ref{sec:geom}.  Modulo a small
lie that I will come back to there, the space $S$ can be recovered from the
topos $\mathscr{Sh}(S)$.  Hence the class of spaces embeds into the class of toposes,
and this is why toposes can be viewed as generalized spaces.

Sheaves will be defined and explained in Section~\ref{sec:geom}.  To give a
brief sketch: denote by $\mathscr{Open}(S)$ the poset of open subsets of $S$; then a
\demph{presheaf} on the space $S$ is a presheaf on the category $\mathscr{Open}(S)$,
and a sheaf on $S$ is a presheaf with a further property.  I will
consistently use `sheaf' to mean what some would call `sheaf of sets'.  A
sheaf of groups, rings, etc.\ is the same as an internal group, ring etc.\ in
$\mathscr{Sh}(S)$.  

6.
The category $\mathscr{FinSet}$ of finite sets is a topos.  Similarly, $\Set$ can be
replaced by $\mathscr{FinSet}$ in all of the previous examples, giving toposes of
finite $G$-sets, finite sheaves, etc.  
\end{enumerate}
\end{examples}

You might ask `why is the definition of topos what it is?  Why that
*particular* collection of axioms?  What's the motivation?'  I will not
attempt to answer, except by explaining several ways in which the definition
has been found useful.  It is also worth noting that the topos axioms have
many non-obvious consequences, giving toposes a far richer structure than most
categories.  For example, every map in a topos factorizes, essentially
uniquely, as an epi followed by a mono.  More spectacularly, the axioms imply
that every topos has finite *co*limits.  This can be proved by the
following very elegant strategy, due to \citet{Pare}.  For every topos $\mathscr{E}$,
we have the contravariant power set functor $P = \Omega^{(-)}\colon \mathscr{E}^\op
\to \mathscr{E}$.  It can be shown that $P$ is monadic.  But monadic functors create
limits, and $\mathscr{E}$ has finite limits.  Hence $\mathscr{E}^\op$ has finite limits; that
is, $\mathscr{E}$ has finite colimits.



### Toposes and set theory ###
\label{sec:sets}



Here I will describe what makes `the' category of sets special among all
toposes, and explain why I just put `the' in quotation marks.  This is the
stuff of revolution: it can completely change your view of set theory.

We begin by listing some special properties of the topos $\Set$.

1.
The terminal object $1$ is a separator (generator).  That is, given maps $X
\parpair{f}{g} Y$ in $\Set$, if $f \of x = g \of x$ for all $x\colon 1 \to X$
then $f = g$.

It is worth dwelling on what this says.  Maps $1 \to X$ correspond to elements
of $X$, and we make no notational distinction between the two.  Moreover,
given an element $x \in X$ and a map $f\colon X \to Y$, we can compose the maps
\[
1 \toby{x} X \toby{f} Y
\]
to obtain a map $f \of x\colon 1 \to Y$, and this is the map corresponding to the
element $f(x) \in Y$.  (We might harmlessly write both $f \of x$ and $f(x)$ as
$fx$.)  Thus, elements are a special case of functions, and evaluation is a
special case of composition.

The property above says that if $f(x) = g(x)$ for all $x \in X$ then $f = g$.
In other words, a function is determined by its effect on elements.

1.
Write $0$ for the initial object of $\Set$ (the empty set).  Then $0 \not\cong
1$.  Equivalently, $\Set$ is not equivalent to the terminal category $\One$.
\end{enumerate}

A topos satisfying properties~\textbf{1} and~\textbf{2} is called
\demph{well-pointed}.  

3.
This property says, informally, that there is a set consisting of the natural
numbers. 

What are the `the natural numbers', though?  One way to get at an answer is
to use the principle that sequences can be defined recursively.  That is,
given a set $X$, an element $x \in X$, and a map $r\colon X \to X$, there is a
unique sequence $(x_n)_{n = 0}^\infty$ in $X$ such that 
% 
\begin{equation}
\label{eq:recursion}
x_0 = x,
\quad
x_{n + 1} = r(x_n) 
\quad(n \in \mathbb{N}).
\end{equation}
% 
A sequence $(x_n)_{n = 0}^\infty$ in $X$ is just a map $f\colon \mathbb{N} \to X$,
and if we write $s\colon \mathbb{N} \to \mathbb{N}$ for the function $n \mapsto n + 1$
(`successor'), then~\eqref{eq:recursion} says exactly that the diagram
% 
\begin{equation}
\label{eq:nat}
\begin{diagram}
        &               &\mathbb{N}   &\rTo^s &\mathbb{N}   \\
1       &\ruTo(2,1)&lt;0   &\dTo>f &       &\dTo>f \\
        &\rdTo(2,1)&lt;x   &X      &\rTo_r &X      \\
\end{diagram}
\end{equation}
% 
commutes.
\end{enumerate}

\begin{defn}
Let $\mathscr{E}$ be a category with a terminal object, $1$.  A \demph{natural numbers
object} in $\mathscr{E}$ is a triple $(N, 0, s)$, with $N \in \mathscr{E}$, $0\colon 1 \to N$, and
$s\colon N \to N$, that is initial as such: for any triple $(X, x, r)$ of
the same type, there is a unique map $f\colon N \to X$ such that~\eqref{eq:nat}
commutes (with $N$ in place of $\mathbb{N}$).
\end{defn}

Property~\textbf{3} is, then, that $\Set$ has a natural numbers object.


1.
Epis split.  That is, for any epimorphism (surjection) $e\colon X \to Y$ in
$\Set$, there exists a map $m\colon Y \to X$ such that $e \of m = 1_Y$.  The
splitting $m$ chooses for each $y \in Y$ an element of the nonempty set
$e^{-1}\{y\}$.  The existence of such splittings is precisely the Axiom of
Choice.  Generally, a category is said to satisfy the \demph{Axiom of Choice}
(or to `have Choice') if epis split.
\end{enumerate}

In summary,
% 
+-- {: .center}
sets and functions form a well-pointed topos  
with natural numbers object and Choice.
=--
% 
The category of sets has many other elementary properties (such as the fact
that the subobject classifier has exactly two elements), but they are all
consequences of the properties just mentioned.

But what is this thing called `the category of sets'?  What do we have to
assume about sets in order to prove that these properties hold?  

Many mathematicians do not like to be bothered with such questions, because
they know that the standard answer will be something like `sets are anything
satisfying the axioms of ZFC'---and they feel that ZFC is irrelevant to what
they do, and prefer not to hear about it.

This standard answer is *valid*, in the sense that for every model of
ZFC, there is a resulting category of sets satisfying the properties
above.  But it may seem *irrelevant*, because at no point in establishing
the properties did it feel necessary to call on an axiom system: all the
properties are suggested directly by the naive imagery of a set as a bag of
dots.  

There is, however, another type of answer---and this was Lawvere's radical
idea.  It is this: 
% 
+-- {: .center}
we take the properties above as our axioms on sets.
=--
% 
In other words, we do away with ZFC entirely, and ask instead that sets and
functions form a well-pointed topos with natural numbers object and Choice.
`The' category of sets is any category satisfying these axioms.  In fact we
should say *a* category of sets, since, as we shall see, there may be
many different such categories.

This is Lawvere's Elementary Theory of the Category of Sets (ETCS), stated in
modern language.  (See \citet{ETCS}, or \citet{LR} for a good expository
account.)  It is nearly fifty years old, but still has not gained the currency
it deserves, for reasons on which one can speculate.

You might be thinking that this is circular: that this axiomatization of sets
depends on the notion of category, and the notion of category depends on some
notion of collection or set.  But in fact, ETCS does not depend on the general
notion of category.  It can be stated without using the word `category' once.

To see this, we need to back up a bit.  The ZFC axiomatization of sets looks,
informally, like this:
% 
* there are some things called `sets'
* there is a binary relation `$\in$' on sets
* some axioms hold.
% 
People seeing this (or the formal version) often ask certain questions.  What
does `some things' mean?  Do you mean that there is a *set* of sets?
(No.)  What exactly is meant by `binary relation'?  (It means that for each
set $X$ and set $Y$, the statement `$X \in Y$' is deemed to be either true or
false.)  What do you mean, `deemed'?  Etc.  This is not a logic course, and I
will not attempt to answer the questions except to say that there is an
assumed common understanding of these terms.  To hide behind jargon, ZFC is a
first-order theory.

The ETCS axiomatization of sets looks like this:
% 
* there are some things called `sets'
* for each set $X$ and set $Y$, there are some things called `functions
from $X$ to $Y$'
* for each set $X$, set $Y$ and set $Z$, there is a binary operation
assigning to each pair of functions
\[
f\colon X \to Y, 
\quad
g\colon Y \to Z
\]
a function $g \of f\colon X \to Z$
* some axioms hold.
% 
You can ask the same kind of logical questions as for ZFC---what exactly is
meant by `binary operation'?\ etc.---which again I will not attempt to
answer.  The difficulties are no worse than for ZFC, and again, in the jargon,
ETCS is a first-order theory.  

Stated in this way, the ETCS axioms begin by saying that composition is
associative and has identities (so that sets, functions and composition of
functions define a category); then they say that binary products and
equalizers of sets exist, and there is a terminal set (so that the category of
sets has finite limits); and so on, until we have said that sets and functions
form a well-pointed topos with natural numbers object and Choice.  You can do
it in about ten axioms.

ZFC axiomatizes sets and membership, whereas ETCS axiomatizes sets and
functions.  Anything that can be expressed in one language can be expressed in
the other: in (the usual implementation of) ZFC, a function $X \to Y$ is
defined as a suitable subset of $X \times Y$, and in ETCS, an element of $X$
is defined as a function from the terminal set to $X$.

ZFC is slightly stronger than ETCS.  `Stronger' means that everything that can
be deduced about sets from the ETCS axioms can also be deduced in ZFC, but not
vice versa.  `Slightly' is meant in a sociological sense.  I believe it has
been said that the mathematics in an ordinary undergraduate syllabus
(excluding, naturally, any course in ZFC) makes no more assumptions about sets
than are made by ETCS.  If that is so, it must also be the case that for many
mathematicians, nothing in their entire research career requires more than
ETCS.

The technical relationship between ZFC and ETCS is well understood.  It is
known exactly which fragment of ZFC is equivalent to ETCS (namely, `bounded'
or `restricted' Zermelo with Choice; see \citet{MM}).  It is also known what
needs to be added to ETCS in order to obtain a system of equal strength to
ZFC.  This extra ingredient is an axiom scheme (a countably infinite family of
axioms) that set theorists in the traditional mould would call Replacement,
and category theorists would call a form of cocompleteness.  It says,
informally, that given any set $I$ and family $(X_i)_{i \in I}$ of sets
specified by a first-order formula, the coproduct $\sum_{i \in I} X_i$ exists.
The existence of this coproduct is expressed by saying that there exist a set
$X$ and a map $p\colon X \to I$ (to be thought of as the projection $\sum_{i \in
I} X_i \to I$) such that for each $i \in I$, the inverse image $p^{-1}\{i\}$
is isomorphic to $X_i$.  See Section~8 of \citet{McLECS} for details.

Topos theory therefore provides a different viewpoint on set theory.  Let us
take a brief look from this new viewpoint at a famous theorem of set theory:
that the Continuum Hypothesis is independent of the usual set-theoretic
axioms, as proved by G\"odel and Cohen.

Temporarily, let us say that a `category of sets' is a well-pointed topos with
natural numbers object and Choice, satisfying the axiom scheme of Replacement.
A category of sets is said to \demph{satisfy the Continuum Hypothesis} if for
all objects $X$,
% 
\begin{align*}
                &\text{there exist monos } N \monic X \monic 2^N        \\
\implies        &X \cong N \text{ or } X \cong 2^N.
\end{align*}
% 
(As usual, $N$ denotes the natural numbers object; $2$ is the subobject
classifier.)  Stated categorically, the theorem is this: given any category of
sets, you can build one that satisfies the Continuum Hypothesis and one that
does not.  This is only a rephrasing of the standard statement, but if you are
more at home with the term `category' than with `model of ZFC', you might find
it less mysterious.

This section has been about the benefits of viewing the/a category of sets as
a special topos.  But the other way round, there are also benefits to viewing
a topos as a generalized category of sets.  For example, we might view
$\Set^\mathbb{N}$ as the category of sets varying through (discrete) time.  The set
of human beings alive today is an object of $\Set^\mathbb{N}$: as the meaning of
`today' changes, the set changes.  A sheaf can similarly be understood as a
set varying through space.

An important fact is that it is valid to use set-like language and reasoning
in *any* topos, provided that we stick to certain rules.  (Any statement
about sets that can be proved constructively is true in every topos.)  For
instance, given maps $X \parpair{f}{g} Y$ in *any* topos, the equalizer
$E$ satisfies the formula
\[
E = \{ x \in X | f(x) = g(x) \}
\]
---there is a way to make rigorous sense of this.  Sometimes it saves a lot of
labour to use this kind of language rather than diagrams.  It is called the
\demph{internal language} of the topos.


### Toposes and geometry ###
\label{sec:geom}


This section covers concepts such as sheaf, geometric morphism (map of
toposes), Grothendieck topos, and locale.  But the most important thing I
want to explain is how and why geometry has inspired so much of topos theory.

\chunk{Sheaves}

Let $X$ be a topological space.  (Following tradition, I will switch from my
previous convention of using $X$ to denote an object of a topos.)  Write
$\mathscr{Open}(X)$ for its poset of open subsets.  A presheaf on $X$ is a functor
$F\colon \mathscr{Open}(X)^\op \to \Set$.  It assigns to each open subset $U$ a set
$F(U)$, whose elements are called \demph{sections over $U$} (for reasons to be
explained).  It also assigns to each open $V \subseteq U$ a function $F(U) \to
F(V)$, called \demph{restriction} from $U$ to $V$ and denoted $s \mapsto
s\restr{V}$.  I will write $\mathscr{Psh}(X)$ for the category of presheaves on $X$.

\begin{examples}
1.   \label{eg:pshf-cts}
Let $F(U) = \{\text{continuous functions } U \to \mathbb{R}\}$; restriction
is restriction.
1.   \label{eg:pshf-bdd}
The same, but with `bounded' in place of `continuous'.
\end{examples}

Examples~\eqref{eg:pshf-cts} and~\eqref{eg:pshf-bdd} are qualitatively
different: continuity is a local property, but boundedness is not.  This
difference can be captured by asking the following question.  Let $(U_i)_{i
\in I}$ be a family of open subsets of $X$, and take, for each $i \in I$, a
section $s_i \in F(U_i)$.  Might there be some $s \in F(\bigcup_{i \in I}
U_i)$ such that $s\restr{U_i} = s_i$ for all $i$?

For this to stand a chance of being true, functoriality demands that the
sections $s_i$ must satisfy a `matching condition': $s_i\restr{U_i \cap U_j} =
s_j\restr{U_i \cap U_j}$ for all $i$ and $j$.  A \demph{sheaf} is a presheaf
such that for every family $(U_i)_{i \in I}$ of open sets and every matching
family $(s_i)_{i \in I}$, there is a unique $s \in F(\bigcup_{i \in I} U_i)$
such that $s\restr{U_i} = s_i$ for all $i \in I$.

\begin{examples}        \label{eg:sheaves}
1. The first example above, with continuous functions, is a sheaf.  The
proof can be split into two parts.  Given $(U_i)$ and $(s_i)$, there is
certainly a unique *function* $s\colon \bigcup U_i \to \mathbb{R}$ (continuous
or not) such that $s\restr{U_i} = s_i$ for all $i$.  The question now is
whether $s$ is continuous; and because continuity is a local property, it is.

1. The second example above, with bounded functions, is not a sheaf (for a
general space $X$).  This is because boundedness is *not* a local
property.  

1. The sheaf of continuous real-valued functions is rather floppy, in the
sense that there are usually many ways to extend a continuous function from a
smaller set to a larger one.  Often people consider sheaves made up of
holomorphic or rational functions, which are much more rigid: there are
typically few or no ways to extend.  It is quite normal for there to be no
global sections (sections over $X$) at all.

1.   \label{eg:shf-bundle} 
Take any continuous map $Y \toby{p} X$ of topological spaces (which can be
thought of as a kind of bundle over $X$).  Then there arises a sheaf $F$ on
$X$, in which $F(U)$ is the set of continuous maps $s\colon U \to Y$ such that
the triangle on the left commutes:
\[
\begin{diagram}
        &               &Y      \\
        &\ruTo&lt;s        &\dTo>p \\
U       &\rIncl         &X      \\
\end{diagram}
\qquad\qquad\qquad
\setlength{\unitlength}{1em}
\setlength{\fboxsep}{0pt}
\begin{array}{c}
% \fbox{%
\begin{picture}(16,10)
\thicklines
% \put(0,1.5){\line(1,0){2}}
\put(0,1.4){\line(1,0){2}}
\cell{1}{.5}{b}{U}
% 
% \put(10,1.5){\line(1,0){2}}
\put(10,1.5){\line(1,0){2}}
\cell{11}{.5}{b}{U}
\thinlines
\put(8,1.5){\line(1,0){8}}
\cell{15}{0.2}{b}{X}
% 
\put(8,5){\framebox(8,5)}
\cell{15}{5.5}{b}{Y}
% 
\qbezier[30](10,5)(10,7.5)(10,10)
\qbezier[30](12,5)(12,7.5)(12,10)
\qbezier(10,8.5)(11,8)(12,9.5)
\qbezier(10,8.45)(11,7.95)(12,9.45)
% 
\cell{5}{1.5}{c}{\mbox{\Large\ensuremath{\hookrightarrow}}}
\cell{11}{3.25}{c}{\mbox{\Large\ensuremath{\downarrow}}}
\cell{11.5}{3.25}{l}{\scriptstyle{p}}
\cell{5}{5}{c}{\mbox{\Large\ensuremath{\nearrow}}}
\cell{4.8}{5.2}{br}{\scriptstyle{s}}
\end{picture}%
% }
\end{array}
\]
Such an $s$ is precisely a right inverse, or `section', of the map
$p^{-1}U \to U$ induced by $p$.
\end{enumerate}
\end{examples}

There is also an abstract categorical explanation of where the concept of
sheaf comes from.  Fix a space $X$.  We have a functor
\[
I\colon \mathscr{Open}(X) \to \mathscr{TopSp}/X
\]
where $\mathscr{TopSp}$ is the category of topological spaces, $\mathscr{TopSp}/X$ is the slice
category, and $I(U) = (U \hookrightarrow X)$.  This functor $I$ embodies the simple
thought that an open subset of a topological space can be treated as a space
in its own right.  We now apply to $I$ two very general categorical
constructions, from which the sheaf concept will appear automatically.

First, purely because the domain of $I$ is small and the codomain has small
colimits, there is an induced adjunction
\[
\mathscr{Psh}(X) = \Set^{\mathscr{Open}(X)^\op}
\pile{\rTo^{- \otimes I}\\ \dbot\\ \lTo_{\Hom(I, -)}}
\mathscr{TopSp}/X.
\]
The right adjoint is given by
\[
(\Hom(I, Y))(U)
=
\mathscr{TopSp}/X
\,
(I(U), Y)
\]
where $Y = \left(\vslob{Y}{p}{X}\right) \in \mathscr{TopSp}/X$ and $U \in \mathscr{Open}(X)$.
This is, in fact, the process described in
Example~\ref{eg:sheaves}(\ref{eg:shf-bundle}): the sheaf $F$ defined there is
$\Hom(I, Y)$.  The left adjoint can be described as a coend or colimit: for $F
\in \mathscr{Psh}(X)$,
\[
F \otimes I     %&
= 
\int^U F(U) \times I(U) %\\
%&
=
\Bigl(
\bigl(
\Colt{U, s}
U
\bigr)
\to
X
\Bigr)
\]
where the colimit is over all $U \in \mathscr{Open}(X)$ and $s \in F(U)$, and the
map to $X$ is the canonical one.

Second, every adjunction restricts%
\label{p:adjn-eqv}
canonically to an equivalence between full subcategories: one consists of the
objects at which the unit of the adjunction is an isomorphism, and the other
of the objects at which the counit is an isomorphism.  Write the
equivalence obtained from our adjunction as 
\[
\mathscr{Sh}(X) 
\pile{\rTo\\ \deqv\\ \lTo}
\mathscr{Et}(X).
\]
It can be shown that this $\mathscr{Sh}(X)$ is the same category of sheaves as before.
In this way, the notion of sheaf arises canonically from the very simple
functor $I\colon \mathscr{Open}(X) \to \mathscr{TopSp}/X$.  The notion of \'etale bundle \citep{MM}
also arises canonically: the \'etale bundles are the objects of $\mathscr{Et}(X)$.
Among other things, this equivalence shows that every sheaf is of the form
described in Example~\ref{eg:sheaves}(\ref{eg:shf-bundle}).

One way or another, we have the category $\mathscr{Sh}(X)$ of sheaves on $X$.  It is a
topos.  Its subobject classifier $\Omega$ is given by
\[
\Omega(U) 
=
\{
\textrm{open subsets of } U
\}.
\]
The crucial fact about $\mathscr{Sh}(X)$ is that---modulo a small lie that I will
repair later---
% 
+-- {: .center}
$X$ can be recovered from $\mathscr{Sh}(X)$.
=--
% 
So the class of topological spaces embeds into the class of toposes.  We can
think of toposes as generalized spaces.

A common technique in topos theory is to take a concept from topology or
geometry and extend it to toposes.  For example, suppose you hear someone
talking about `connected toposes'.  You may have no idea what one is, but you
can bet that the definition has been obtained by determining what
property of the topos $\mathscr{Sh}(X)$ corresponds to connectedness of the space
$X$, then taking that as the definition of connectedness for all toposes.

The next few subsections are all examples of this generalization process.  


\chunk{Geometric morphisms}


So far I have said nothing about maps between toposes.  There is an obvious
candidate for what a map of toposes should be: a functor preserving finite
limits, exponentials, and subobject classifiers.  Such a functor is called a
\demph{logical morphism}.  They have a part to play, but there is another
notion of map of toposes that has been found much more useful.  It can be
derived by generalizing from topology.

Every map $f\colon X \to Y$ in $\mathscr{TopSp}$ induces an adjunction
% 
\begin{equation}        \label{eq:Sh-GM}
\mathscr{Sh}(X)
\pile{\lTo^{f^*}\\ \dbot\\ \rTo_{f_*}}
\mathscr{Sh}(Y).
\end{equation}
% 
This is not obvious.  The right adjoint $f_*$ is easy to construct---
\[
(f_* F)(V) = F(f^{-1} V)
\]
($F \in \mathscr{Sh}(X)$, $V \in \mathscr{Open}(Y)$)---but the left adjoint $f^*$ is harder.  It
can be made easy by invoking the equivalence between sheaves and \'etale
bundles; but I will not go into that, or give any other description of $f^*$.

It is a fact that $f^*$ preserves finite limits.  It is also a fact (modulo
the usual small lie) that there is a natural correspondence between continuous
maps $X \to Y$ and adjunctions~\eqref{eq:Sh-GM} in which the left adjoint
preserves finite limits.  So now we know what continuous maps look like in
topos-theoretic terms.  We duly generalize:

\begin{defn}    \label{defn:GM}
Let $\mathscr{E}$ and $\mathscr{F}$ be toposes.  A \demph{geometric morphism} $f\colon \mathscr{E} \to \mathscr{F}$
is an adjunction
\[
\mathscr{E} \pile{\lTo^{f^*}\\ \dbot\\ \rTo_{f_*}} \mathscr{F}
\]
in which the left adjoint $f^*$ preserves finite limits.  (People often say
`left exact left adjoint'.)  The right adjoint $f_*$ is called the
\demph{direct image} part of $f$, and $f^*$ is the \demph{inverse image} part.
\end{defn}

I will write $\mathscr{Topos}$ for the category of toposes and geometric morphisms.
(Really it's a 2-category, in an obvious way.)  By construction, we have a
functor
\[
\mathscr{Sh}\colon \mathscr{TopSp} \to \mathscr{Topos}
\]
which is (2-categorically) full and faithful, modulo the usual small lie.

\begin{examples}        \label{eg:GMs}
1. 
Every functor $f\colon \mathbb{C} \to \mathbb{D}$ induces a string of adjoint
functors
\[
\begin{diagram}[width=3em]
\widehat{\mathbb{C}} &
\pile{\rTo^{f_!}\\ \dbot\\ \lTo~{f^*}\\ \dbot\\ \rTo_{f_*}} &
\widehat{\mathbb{D}} \\
\end{diagram}
\]
between presheaf categories.  Here $f^* = - \of f$, and $f_!$ and $f_*$
are left and right Kan extension along $f$, respectively.  Since $f^*$ has a
left adjoint, it preserves limits.  Hence $(f^*, f_*)$ is a geometric morphism
$\widehat{\mathbb{C}} \to \widehat{\mathbb{D}}$.

1.   \label{eg:GM-sheaves}
It turns out that, for any topological space $X$, the inclusion $\mathscr{Sh}(X) \hookrightarrow
\mathscr{Psh}(X)$ has a finite-limit-preserving left adjoint.  It is called
\demph{sheafification} or the \demph{associated sheaf} functor.  So the
inclusion of sheaves into presheaves is a geometric morphism.

Since $\mathscr{Sh}(X)$ is a *full* subcategory, the inclusion is full and
faithful; and for totally general reasons, this is equivalent to the counit of
the adjunction being an isomorphism.  In other words, sheafifying a sheaf does
not change it.
\end{enumerate}
\end{examples}


\chunk{Points}


Let us generalize another concept of topology.  The points of a topological
space $X$ correspond to the maps $1 \to X$ (where $1$ is the one-point space),
which correspond to the geometric morphisms $\mathscr{Sh}(1) \to \mathscr{Sh}(X)$.  But $\mathscr{Sh}(1)
= \mathscr{Psh}(1) = \Set$, so we make the following definition.

\begin{defn}
A \demph{point} of a topos $\mathscr{E}$ is a geometric morphism $\Set \to \mathscr{E}$.
\end{defn}


\chunk{Embeddings and Grothendieck toposes}


For any subspace $Y$ of a space $X$, the inclusion $Y \hookrightarrow X$ is an
\demph{embedding}, that is, a homeomorphism to its image.  It can be shown
that a map $f\colon Y \to X$ of spaces is an embedding if and only if the direct
image part $f_*$ of the corresponding geometric morphism $f\colon \mathscr{Sh}(Y) \to
\mathscr{Sh}(X)$ is full and faithful.  So, as usual, we generalize:

\begin{defn}
A geometric morphism $f\colon \mathscr{F} \to \mathscr{E}$ is an \demph{embedding} (or
\demph{inclusion}) if the direct image functor $f_*$ is full and faithful.
\end{defn}

We then say that $\mathscr{F}$ is a \demph{subtopos} of $\mathscr{E}$.  At least, this is the
right thing to say up to equivalence.  Perhaps we should reserve that word for
when $\mathscr{F}$ is actually a (full) subcategory of $\mathscr{E}$ and $f_*$ is the inclusion
$\mathscr{F} \hookrightarrow \mathscr{E}$, rather than allowing $f_*$ to be any old full and faithful
functor.  But a full and faithful functor induces an equivalence to its image,
so it makes no real difference.

Probably the easiest toposes are the \demph{presheaf toposes}: those
equivalent to $\widehat{\mathbb{C}} = \Set^{\mathbb{C}^\op}$ for some small category
$\mathbb{C}$.  So maybe subtoposes of presheaf toposes are relatively easy too.
They have a special name:

\begin{defn}    \label{defn:GT}
A topos is \demph{Grothendieck} if it is (equivalent to) a subtopos of some
presheaf topos.
\end{defn}

For instance, we saw in Example~\ref{eg:GMs}(\ref{eg:GM-sheaves}) that
$\mathscr{Sh}(X)$ is a subtopos of $\mathscr{Psh}(X) = \widehat{\mathscr{Open}(X)}$, for any topological
space $X$.  Hence $\mathscr{Sh}(X)$ is a Grothendieck topos.

Being Grothendieck is generally thought of as a mild condition on a topos.  A
Grothendieck topos has all small limits, which immediately disqualifies
toposes such as $\mathscr{FinSet}$, $\mathscr{FinSet}^{\mathbb{C}^\op}$, etc.  But other than
toposes arising from finite sets (or sets subject to some other cardinality
bound), most of the toposes that people have worked with are Grothendieck.  A
notable exception is the effective topos, the maps in which can be thought of
as computable functions.

There is a theorem of Giraud giving a list of conditions on a category
equivalent to it being a Grothendieck topos.  It includes non-elementary
axioms such as `there is a small generating set'.  (`Non-elementary' means
that it refers to a pre-existing notion of set.)  The Grothendieck toposes are
sometimes regarded as the nice toposes, but perhaps the totality of
Grothendieck toposes is not as nice as the totality of all toposes.

Definition~\ref{defn:GT} is not the definition of Grothendieck topos that you
will find in most books.  I will now give a brief indication of what the
standard definition is and why it is equivalent to the one above.

Fix a small category $\mathbb{C}$.  There is a one-to-one correspondence
between the subtoposes of $\widehat{\mathbb{C}}$ and the 
\demph{Grothendieck topologies} on $\mathbb{C}$.  A Grothendieck topology is a
kind of explicit, combinatorial structure; it specifies which diagrams
\[
\begin{diagram}[height=1.2em,width=4em]
\       &               &       \\
\vdots  &\rdTo(2,4)     &       \\
c_i     &               &       \\
        &\rdTo(2,2)     &       \\
\vdots  &               &c      \\
        &\ruTo(2,2)
         \ruTo(2,4)     &       \\
c_j     &               &       \\
\vdots  &               &       \\
\       &               &       \\
\end{diagram}
\]
in $\mathbb{C}$ are to be thought of as `covering families' and which are not.
(There are axioms.)  The motivating example is that given a topological space
$X$, there is a canonical Grothendieck topology on $\mathscr{Open}(X)$: a family $(U_i
\hookrightarrow U)_{i \in I}$ of subsets of $U \in \mathscr{Open}(X)$ is covering if and only if
$U = \bigcup_{i \in I} U_i$.

The bijection
\[
\{ \textrm{Grothendieck topologies on } \mathbb{C} \}
\cong
\{ \textrm{subtoposes of } \widehat{\mathbb{C}} \}
\]
is written
\[
J \leftrightarrow \mathscr{Sh}(\mathbb{C}, J).
\]
A pair $(\mathbb{C}, J)$, consisting of a small category $\mathbb{C}$ equipped
with a Grothendieck topology $J$, is called a \demph{site}, and $\mathscr{Sh}(\mathbb{C},
J)$ is the category of \demph{sheaves} on that site.  For example, let $X$ be
a topological space, put $\mathbb{C} = \mathscr{Open}(X)$, and take $J$ to be the
Grothendieck topology mentioned above; then $\mathscr{Sh}(\mathbb{C}, J) = \mathscr{Sh}(X)$.  Most
books proceed as follows: define Grothendieck topology, define site, define
the category of sheaves on a site, then define a Grothendieck topos to be a
category equivalent to the category of sheaves on some site.

I do not know a short way to explain why the subtoposes of $\widehat{\mathbb{C}}$
correspond to the Grothendieck topologies on $\mathbb{C}$.  The following two
paragraphs may make it seem easier, or harder.

First, there is an explicit classification of the subtoposes of *any*
topos $\mathscr{E}$.  Indeed, it can be shown that the subtoposes of $\mathscr{E}$ correspond to
the maps $j\colon \Omega \to \Omega$ satisfying certain equations.  
(Such a $j$ is called a \demph{Lawvere--Tierney topology} on $\mathscr{E}$, although
this is so distant from the original usage of the word `topology' that some
people object; Peter Johnstone, for instance, uses \demph{local operator}
instead.)  By definition of subobject classifier, it is equivalent to say that
a subtopos of $\mathscr{E}$ amounts to a subobject of $\Omega$ satisfying certain
axioms.

Second, take $\mathscr{E} = \widehat{\mathbb{C}}$.  We know
(Example~\ref{egs:toposes}(\ref{eg:topos-pshf})) that $\Omega \in
\widehat{\mathbb{C}}$ is given by $\Omega(c) = \{ \text{sieves on } c \}$.  Hence a
subtopos of $\widehat{\mathbb{C}}$ corresponds to a collection of sieves in
$\mathbb{C}$, satisfying certain axioms.  Calling these the `covering sieves'
gives the notion of Grothendieck topology.


\chunk{Locales}


Here I will explain the `small lie' mentioned several times above, and make
amends.  I will also explain why topos theorists are fond of jokes about
pointless topology.

The definition of sheaf on a topological space $X$ does not mention the points
of $X$.  It mentions only the open sets and inclusions between them, and uses
the fact that it is possible to take arbitrary unions and finite intersections
of open sets.  Having observed this, you can see why the space $X$ cannot
*always} be recovered from the topos $\mathscr{Sh*(X)$.  For instance, if $X$ is
indiscrete (has no open sets except $\emptyset$ and $X$) and nonempty, then
$\mathscr{Sh}(X)$ is the same no matter how many points $X$ has.

The idea now is to split the process $X \mapsto \mathscr{Sh}(X)$ into two steps.  First,
we forget the points of $X$, leaving just the set of open sets, ordered by
inclusion.  Then, we form the category of `sheaves' on that ordered set
(defined as for topological spaces, almost verbatim).

\begin{defn}
A \demph{frame} is a partially ordered set such that every subset has a join
($=$ least upper bound $=$ sup) and every finite subset has a meet ($=$
greatest lower bound $=$ inf).  A \demph{map of frames} is a map preserving
order, joins and finite meets.
\end{defn}

A topological space $X$ has a frame $\mathscr{Open}(X)$ of open subsets, and a
continuous map $f\colon X \to Y$ induces a map $f^{-1}\colon \mathscr{Open}(Y) \to
\mathscr{Open}(X)$ of frames.  This gives a functor
\[
\mathscr{Open}\colon \mathscr{TopSp} \to \mathscr{Frame}^\op.
\]
We now perform a linguistic manoeuvre.  $\mathscr{Frame}^\op$ is the desired category
of `pointless spaces'.  But we cannot wholeheartedly say that a frame is a
pointless space, because the *maps* of frames are the wrong way round.
So we introduce a new word---\demph{locale}---and define the category $\mathscr{Loc}$
of locales by $\mathscr{Loc} = \mathscr{Frame}^\op$.  We can wholeheartedly say that a
*locale* is a pointless space.

There is a functor $\mathscr{Sh}\colon \mathscr{Loc} \to \mathscr{Topos}$, defined just as for topological
spaces except that unions become joins and intersections become meets.  The
functor $\mathscr{Sh}\colon \mathscr{TopSp} \to \mathscr{Topos}$ factorizes as
\[
\mathscr{TopSp} \toby{\mathscr{Open}} \mathscr{Loc} \toby{\mathscr{Sh}} \mathscr{Topos}.
\]
This is the two-step process mentioned above.

Whenever I have said `modulo a small lie', you can interpret that as `use
locales instead of topological spaces'.  For example, $\mathscr{Sh}\colon \mathscr{Loc} \to
\mathscr{Topos}$ really is full and faithful, in a suitably up-to-isomorphism sense:
locale maps $X \to Y$ correspond one-to-one with isomorphism classes of
geometric morphisms $\mathscr{Sh}(X) \to \mathscr{Sh}(Y)$.  This means that $\mathscr{Loc}$ is equivalent
to a full subcategory of $\mathscr{Topos}$.  (Really it is an equivalence of
2-categories, but I will gloss over that point.)

Every locale gives rise to a topos---but the converse is also true.  Given a
topos $\mathscr{E}$, the subobjects of $1$ form a poset $\subseteq_\mathscr{E}(1)$.  Assuming that
$\mathscr{E}$ has enough colimits, $\subseteq_\mathscr{E}(1)$ is a frame.  This process defines a
functor
\[
\begin{array}{ccc}
\mathscr{Topos}  &\to            &\mathscr{Loc}   \\
\mathscr{E}      &\mapsto        &\subseteq_\mathscr{E}(1).
\end{array}
\]
I am now quietly changing $\mathscr{Topos}$ to mean the toposes with small colimits;
this includes all Grothendieck toposes.

You might think that $1$ could have no interesting subobjects, since that is
the case in the most obvious topos, $\Set$.  But there are toposes that are
nearly as obvious in which $\subseteq_\mathscr{E}(1)$ is not trivial.  For instance, take
$\mathscr{E} = \Set^I$ for any $I$: then $\subseteq_\mathscr{E}(1)$ is the power set of $I$.

Now a wonderful thing is true.  The functor just defined is left adjoint to
the inclusion $\mathscr{Sh}\colon \mathscr{Loc} \hookrightarrow \mathscr{Topos}$.  This means that $\mathscr{Loc}$ is
(equivalent to) a *reflective} subcategory of $\mathscr{Topos*$.  Hence the counit
is an isomorphism:
\[
X \cong \subseteq_{\mathscr{Sh}(X)}(1)
\]
for any locale $X$.  This is how you recover a locale from its topos of
sheaves.

So $\mathscr{Loc}$ sits inside $\mathscr{Topos}$ as a subcategory of the best kind: full and
reflective, like abelian groups in groups.  It is reasonable to say
that a locale is a special sort of topos.  More formally, a topos is
\demph{localic} if it is of the form $\mathscr{Sh}(X)$ for some locale $X$.  Localic
toposes are easy to work with; if you were having trouble proving something
for arbitrary toposes, you might start by trying to prove it in this
special case.  

Since every locale is of the form $\subseteq_\mathscr{E}(1)$ for some topos $\mathscr{E}$, locale
theory can be regarded as the fragment of topos theory concerning subobjects
of $1$.  A subobject of $1$ is a map $1 \to \Omega$, which can reasonably
called a truth value.  In that sense, locale theory is the study of truth
values. 

How much has been lost by passing from topological spaces to locales?  In most
people's view, not much.  For example, we observed that all nonempty
indiscrete spaces give rise to the same locale; but many mathematicians regard
indiscrete spaces with $\geq 2$ points as `pathological' and would be
positively happy to see them go.

The functor $\mathscr{Open}\colon \mathscr{TopSp} \to \mathscr{Loc}$ has a right adjoint, which I will not
describe.  As mentioned on page~\pageref{p:adjn-eqv}, every adjunction
restricts canonically to an equivalence between full subcategories.  In this
case, this gives an equivalence between:
% 
1. a full subcategory of $\mathscr{TopSp}$, whose objects are called the
\demph{sober} spaces
1. a full subcategory of $\mathscr{Loc}$, whose objects are called the
\demph{spatial} locales.
% 
Another way of interpreting the phrase `modulo a small lie' is `true for sober
spaces'.  Sobriety amounts to a rather mild separation condition.  For
example, every Hausdorff space is sober.  So in passing from a Hausdorff space
to a locale, or to a topos, nothing is lost.

There is a kind of attitudinal paradox here.  Many algebraic topologists think
*only* about Hausdorff spaces, and regard non-Hausdorff spaces as
pathological.  But these are often the same people who feel strongly that
topological spaces are not really about open sets; they think in terms of
points and paths and homotopies.  So it is perhaps paradoxical that the
Hausdorff condition guarantees that a space can be understood in terms of
its open sets alone: the topos of sheaves depends on nothing else, and
contains all the information about the original space.



### Toposes and universal algebra ###
\label{sec:univ-alg}



The point of this section is to explain what people mean when they talk about
the classifying topos of a theory.  Another way to look at it is this: I will
explain how toposes can be viewed as cousins of operads and Lawvere theories.

In classical universal algebra, an algebraic theory (or strictly, a
presentation of an algebraic theory) consists of a bunch of operation symbols
of specified arities, together with a bunch of equations.  To take the
standard example, the (usual presentation of the) theory of groups consists of
% 
* an operation symbol $1$ of arity $0$
* an operation symbol $(\:\:)^{-1}$ of arity $1$
* an operation symbol $\cdot$ of arity $2$
% 
together with the usual equations.  You can speak of `models' of an algebraic
theory in any category $\mathscr{E}$ with finite products.  In our example, they are
the internal groups in $\mathscr{E}$.

But there are other ways of looking at such theories.  

Consider the free finite product category $\mathscr{T}$ equipped with an internal
group.  (There are general reasons why such a thing must exist.)  Its
universal property is that for any finite product category $\mathscr{E}$, the
finite-product-preserving functors $\mathscr{T} \to \mathscr{E}$ correspond to the internal
groups in $\mathscr{E}$.

Concretely, $\mathscr{T}$ looks something like this.  It must contain an object $X$,
the underlying object of the internal group.  Since $\mathscr{T}$ has finite
products, it must also contain an object $X^n$ for each $n \in \mathbb{N}$.  There
is no reason for it to have any other objects, and since it is free, it does
not.  A map $X^n \to X^m$ is (by definition of product) an $m$-tuple of maps
$X^n \to X$; and the maps $X^n \to X$ are (by freeness) whatever maps $G^n \to
G$ must exist for *any} internal group $G$ in \emph{any* finite product
category.  That is, they are the $n$-ary operations in the theory of groups:
the words in $n$ letters.

This category $\mathscr{T}$ is called the \demph{Lawvere theory of groups}.  The same
goes for rings, lattices, etc.  In all these cases, $\mathscr{T}$ is a finite product
category with the further property that the objects are in bijection with the
natural numbers, the product of objects corresponding to addition of numbers.
This further property holds because the theories described so far have been
single-sorted: a model is a *single* object equipped with some structure.

But there are also many-sorted theories, such as the two-sorted theory of
pairs $(R, M)$ in which $R$ is a ring and $M$ an $R$-module.  So we can widen
the notion of algebraic theory to include all (small) finite product
categories.  Some people say that an algebraic theory *is* just a finite
product category.  Others say that algebraic theories *correspond*
to finite product categories.  Others still, more traditionally, say that
algebraic theories correspond to only *certain* finite product
categories.

Terminology aside, we can play the same game for other classes of limit.  For
example, it makes no sense to talk about internal categories in an arbitrary
finite product category, because the definition of internal category needs
pullbacks.  (Composition in an internal category $\mathbb{C}$ is a map
$\mathbb{C}_1 \times_{\mathbb{C}_0} \mathbb{C}_1 \to \mathbb{C}_1$.)  But we can talk
about internal categories in a finite *limit* category; and as before,
there is a free finite limit category $\mathscr{T}$ equipped with an internal category.
This means that for any finite limit category $\mathscr{E}$, the
finite-limit-preserving functors $\mathscr{T} \to \mathscr{E}$ correspond to the internal
categories in $\mathscr{E}$.  A small finite limit category is called (or corresponds
to) an \demph{essentially algebraic theory}.

In a category with finite products you can talk about internal groups but not,
in general, internal categories.  In a category with finite limits you can
talk about both.  By extending the list of properties that the category is
assumed to satisfy, you can accommodate more and more sophisticated kinds of
theory.  (The theory of internal categories is more `sophisticated' than that
of groups in the sense that composition is only defined for *some* pairs
of maps, whereas classical universal algebra can only handle operations
defined on *all* pairs.)  The properties need not be of the form `limits
of such-and-such a type exist'.  For example, it is sometimes useful to assume
epi-mono factorization, as we shall see.

There is a trade-off here.  As you allow more sophisticated language, you
widen the class of theories that can be expressed, but you narrow the class of
categories in which it makes sense to take models.  (You also make more work
for yourself.)  In the same way, if you trade in your motorbike for a
double-decker bus, you increase the number of passengers you can carry, but
you restrict where you can carry them---no low bridges or tight alleyways.
(You also increase your fuel costs.)  It is sensible, then, to use
the smallest class of theories containing the ones you are interested in.
For example, you *could* treat groups as an essentially algebraic theory,
but that would mean you could only take models in categories with *all*
finite limits, when in fact just products would do.

Before I get onto toposes, I want to point out a slightly different direction
that you can take things in.  Rather than just altering the *properties*
that the categories are assumed to have, you can also alter the
*structure* with which they are equipped. 

Take monoidal categories, for instance.  We can speak of internal monoids in
any monoidal category.  Hence, the theory of monoids can be regarded as the
free monoidal category containing an internal monoid.  (This is in fact the
category of finite ordinals.)  Similarly, it makes sense to speak of algebras
for an operad $P$ in any monoidal category, and we can associate to $P$ the
free monoidal category $\mathscr{T}$ containing a $P$-algebra.  Thus, for any monoidal
category $\mathscr{E}$, monoidal functors $\mathscr{T} \to \mathscr{E}$ correspond to $P$-algebras in
$\mathscr{E}$.

We might define a \demph{monoidal theory} to be a small monoidal category.
This gets us into the territory of PROPs, where there are nontrivial theorems
such as the classification of 2-dimensional TQFTs: the symmetric monoidal
theory of (or, `PROP for') commutative Frobenius algebras is the category of
smooth 1-manifolds and diffeomorphism classes of cobordisms.

All of this is to give an impression of how far-reaching these ideas
are.  It is a sketch of the context in which classifying toposes can be
understood.

You will have guessed that the same kind of thing can be said for toposes as
for categories with finite products, finite limits, etc.  Since toposes have
very rich structure (*much* more than just finite limits), they
correspond to a very wide class of theories indeed.  

An example of the kind of theory that can be interpreted in a topos is the
theory of fields.  (This is rather a feeble example, but I want to
keep it simple.)  A field is, of course, a commutative ring $R$ satisfying the
axioms 
\[
0 \neq 1
\]
and
\[
\forall x \in R, 
\quad 
x = 0 \quad \textrm{or} \quad \exists y\colon xy = 1.
\]
This definition can be turned, by a mechanical process, into a definition of
`internal field in a topos'.  As compensation for the imprecision of the rest
of this section, I will give the definition in detail; but if you want to skip
it, the point is that it *is* a mechanical process.

Let $\mathscr{E}$ be a topos.  We certainly know how to define `commutative ring in
$\mathscr{E}$': that makes sense in any category with finite products.  Let $R$ be a
commutative ring in $\mathscr{E}$.  The nontriviality axiom, $0 \neq 1$, is expressed
by saying that the pullback of
\[
\begin{diagram}
        &       &1      \\
        &       &\dTo>1 \\
1       &\rTo_0 &R      \\
\end{diagram}
\]
is the initial object $0$.  For the other axiom, let us first define the
subobject $U \monic R$ consisting of the units (invertible elements).  The
`set' $P = \{ (x, y) | xy = 1 \}$ is the pullback
\[
\begin{diagram}
P\SEpbk         &\rTo           &1              \\
\dMono          &               &\dMono>1       \\
R \times R      &\rTo_\cdot     &R.
\end{diagram}
\]
Now we want to define the `set' $U$ of units as the image of the composite map 
\[
f 
= 
\left(
P \monic R \times R \toby{\pr_1} R
\right).
\]
We can talk about images in a topos, since every map in a topos
factorizes essentially uniquely as an epi followed by a mono.  So, define $U
\monic R$ by the factorization
\[
f 
=
\left(
P \epic U \monic R
\right).
\]
The second field axiom states that every element of $R$ lies in either the
subobject $1 \monicby{0} R$ or the subobject $U \monic R$.  In other words, it
states that the map
\[
1 + U \to R
\]
is epi.  Here we have used the fact that every topos has coproducts, written
$+$.  

If you have read Section~\ref{sec:sets}, you will recognize that the informal
talk of `sets' (really, objects of $\mathscr{E}$) and the use of set-theoretic notation
$\{ \ldots | \ldots \}$ are something to do with the internal language of
a topos.  This gives a hint of how the process can be mechanized.

You now have the choice between a short story and a long story. 

The short story is that what we did for finite product and finite limit
categories can also be done for toposes.  The theories corresponding to
toposes are called the geometric theories, and the topos corresponding to a
particular geometric theory is called its classifying topos.

The long story is longer because there are two different notions of map of
toposes---and you need to decide what a map of toposes is in order to state
the universal property of the topos resulting from a theory.  

The more obvious but less used notion of map of toposes is a functor
preserving all the structure in sight: finite limits, exponentials, and the
subobject classifier.  These are called \demph{logical morphisms}.  Now in a
topos, you can interpret a really vast range of theories: any `higher-order
theory', in fact.  (First order means that you can only quantify over
*elements* of a set; in a second order theory you can also quantify over
*subsets* of a set; and so on.)  Models of any such theory get along well
with logical morphisms, because logical morphisms preserve everything.  So you
can tell a similar story for toposes, logical morphisms and higher order
theories as for finite-product categories, finite-product-preserving functors
and algebraic theories.

The more popular notion of map of toposes is that of geometric
morphism.  (Here it helps to have read Section~\ref{sec:geom}, where the
definition is motivated.)  A \demph{geometric morphism} between toposes is a
functor with a finite-limit-preserving left adjoint.  The corresponding
theories are the \demph{geometric theories}.  I will not give the definition,
but it is not too bad an approximation to say that they are the same as the
first-order theories: every geometric theory is first-order, and almost every
first-order theory that one encounters is geometric.

Given a geometric theory, a \demph{classifying topos} for the theory is a
cocomplete topos $\mathscr{T}$ with the property that for any cocomplete topos $\mathscr{E}$,
models of the theory in $\mathscr{E}$ correspond naturally to geometric morphisms $\mathscr{E}
\to \mathscr{T}$.  Every geometric theory has a classifying topos.  

There are two surprises here.  One is the appearance of the word `cocomplete',
which I will not explain and will not bother inserting below.  It is generally
thought of as a mild condition (satisfied by any Grothendieck topos, for
instance).  

The bigger surprise is the reversal of direction.  The previous cases lead us
to expect models in $\mathscr{E}$ to correspond to maps $\mathscr{T} \to \mathscr{E}$.  However, since a
geometric morphism is a pair of adjoint functors, the choice of direction is a
matter of convention.  As the name suggests, the choice that society made was
motivated by geometry.  Perhaps if the motivation had been universal algebra,
it would have been the other way round.  (This is an aspect of the thought
that geometry is dual to algebra.)  A map of toposes would then have been a
finite-limit-preserving functor with a right adjoint, which is more or less
the same thing as a functor preserving finite limits and small colimits.

Given how much structure a topos contains, it is surprising how many
classifying toposes can be described simply.  I will now describe the
classifying topos of any algebraic theory, by the venerable expository device
of doing it just for groups.

We will need the notion of finite presentability.  A group (in $\Set$) is
\demph{finitely presentable} if it admits a presentation by a finite set of
generators subject to a finite set of relations.  The category of finitely
presentable groups and all homomorphisms between them will be written
$\mathscr{Grp}_\fp$.

\paragraph*{Aside} Finite presentability is a more categorical concept than it
might seem.  Writing $T\colon \Set \to \Set$ for the free group monad, a relation
(equation) in a set $X$ of generators is an element of $TX \times TX$.  So, a
family $(r_i)_{i \in I}$ of relations is a map $I \to TX \times TX$, or
equivalently a diagram 
\[
I \rightrightarrows TX
\]
in $\Set$, or equivalently a diagram 
\[
FI \rightrightarrows FX
\]
in $\mathscr{Grp}$, where $F\colon \Set \to \mathscr{Grp}$ is the free group functor.  The group
presented by these generators and relations is the coequalizer of this diagram
in $\mathscr{Grp}$.  Hence a group is finitely presentable precisely when it is the
coequalizer of some diagram $FI \rightrightarrows FX$ in which $I$ and $X$ are finite
sets.  

This formulation of finite presentability in $\mathscr{Grp}$ uses the free group functor
$F$.  But in fact, there is a general definition of finite presentability of
an object of any category.  I will not go into this.

\bigskip

As promised, the classifying topos for groups is easy to describe:
% 
\begin{thm}
The classifying topos for groups is $\Set^{\mathscr{Grp}_\fp}$.
\end{thm}
% 
In other words, for any topos $\mathscr{E}$, a group in $\mathscr{E}$ is the same thing as a
geometric morphism $\mathscr{E} \to \Set^{\mathscr{Grp}_\fp}$.  

The same goes for other algebraic theories.  This yields something
interesting even for very trivial theories.  Take the theory of objects, whose
models in a category $\mathscr{E}$ are simply objects of $\mathscr{E}$.  A finitely presentable
set is just a finite set.  Hence for any topos $\mathscr{E}$, objects of $\mathscr{E}$
correspond to geometric morphisms $\mathscr{E} \to \Set^{\mathscr{FinSet}}$.  Because of this,
the topos $\Set^\mathscr{FinSet}$ is called the \demph{object classifier}.

We have been asking, for a given theory, `what topos classifies it?'  But we
can turn the question round and ask, for a given topos $\mathscr{T}$, `what does $\mathscr{T}$
classify?'  In other words, what are the geometric morphisms from an arbitrary
topos $\mathscr{E}$ into $\mathscr{T}$?  It is a fact that *every} topos $\mathscr{T*$ is the
classifying topos of some geometric theory---although given how wide a class
of theories that is, perhaps this does not say very much.

There are clean answers to this reversed question for many toposes $\mathscr{T}$.  This
is so, in particular, when $\mathscr{T}$ is the topos $\mathscr{Sh}(\mathbb{C}, J)$ of sheaves on
a site (Section~\ref{sec:geom}).  Here I will just tell you the answer for a
smaller class of toposes.

\begin{thm}
Let $\mathbb{C}$ be a category with finite limits.  Then the presheaf topos
$\widehat{\mathbb{C}}$ classifies finite-limit-preserving functors out of
$\mathbb{C}$. 
\end{thm}
% 
In other words, for any topos $\mathscr{E}$, a geometric morphism $\mathscr{E} \to
\widehat{\mathbb{C}}$ is the same thing as a finite-limit-preserving functor
$\mathbb{C} \to \mathscr{E}$.

(If you know about flat functors, you can drop the assumption that $\mathbb{C}$
has finite limits: for any small category $\mathbb{C}$, the presheaf topos
$\widehat{\mathbb{C}}$ classifies flat functors out of $\mathbb{C}$.  This is
one version of Diaconescu's Theorem.)

So there is a back-and-forth translation between geometric theories and the
toposes that classify them.  In many cases, this translation is surprisingly
straightforward.


\begin{thebibliography}{6}

\bibitem[Johnstone(2003)]{JohSE}
Johnstone, P.~T., 2003.
\newblock Sketches of an Elephant: A Topos Theory Compendium.
\newblock Oxford Logic Guides. Oxford University Press.

\bibitem[Lawvere(1964)]{ETCS}
Lawvere, F.~W., 1964.
\newblock An elementary theory of the category of sets.
\newblock \emph{Proceedings of the National Academy of Sciences of the U.S.A.}
  \textbf{52}:1506--1511.
\newblock Reprinted as \emph{Reprints in Theory and Applications of Categories}
  \textbf{12}:1--35, 2005.

\bibitem[Lawvere and Rosebrugh(2003)]{LR}
Lawvere, F.~W. and R.~Rosebrugh, 2003.
\newblock Sets for Mathematics.
\newblock Cambridge University Press, Cambridge.

\bibitem[Mac~Lane and Moerdijk(1994)]{MM}
Mac~Lane, S. and I.~Moerdijk, 1994.
\newblock Sheaves in Geometry and Logic.
\newblock Springer, Berlin.

\bibitem[Mc{L}arty(2004)]{McLECS}
Mc{L}arty, C., 2004.
\newblock Exploring categorical structuralism.
\newblock *Philosophia Mathematica} \textbf{12*:37--53.

\bibitem[Par{\'e}(1974)]{Pare}
Par{\'e}, R., 1974.
\newblock Colimits in topoi.
\newblock *Bulletin of the American Mathematical Society*
  \textbf{80}:556--561.
