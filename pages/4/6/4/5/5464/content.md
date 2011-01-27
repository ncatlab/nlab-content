
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

> This page contains the beginning of the LaTeX-to-instiki conversion of an article to be submitted for peer-review to the [[proceedings:HomePage|Proceedings of the nLab]].

# An Informal Introduction to Topos Theory #
{: #title}

##### Tom Leinster #####
{: #author}

##### ([arXiv:1012.5647](http://arxiv.org/abs/1012.5647)) ######
{: #arxiv}

* tic
{: toc}


+-- {: .num_section #intro}
=--
## Introduction ## {: .num_section}

This short text is for readers who are confident in basic category theory but
know little or nothing about toposes.  It is based on some impromptu talks
given to a small group of category theorists.  I am no expert on topos theory.
These notes are for people even less expert than me.

In keeping with the spirit of the talks, what follows is light on both detail
and references.  For the reader wishing for more, almost everything
here is presented in respectable form in Mac Lane and Moerdijk's very pleasant
introduction to topos theory ([MaMo](#MaMo)).  Nothing here is new, not even
the expository viewpoint (very loosely inspired by [JohSE](#JohSE)).

As a rough indication of the level of knowledge assumed, I will take it that
you are totally comfortable with the Yoneda Lemma and the concept of
cartesian closed category, but I will not assume that you know the definition
of subobject classifier or of topos.

Section \ref{TheDefinitionOfTopos} explains the definition of topos.  The remaining three
sections discuss some of the connections between topos theory and other
subjects.  There are many more such connections than I will mention; I hope it
is abundantly clear that these notes are, by design, a quick sketch of a
large subject.

Section \ref{ToposesAndSetTheory} is on connections between topos theory and set theory.
The major theme there is that we can use topos theory to free ourselves from
the shackles of ZFC.  The minor theme is that 

+-- {: style="text-align: center"}
*a topos is a generalized category of sets.*
=--


Section \ref{ToposesAndGeometry} is on connections with geometry (in a broad sense);
there the thought is that

+-- {: style="text-align: center"}
*a topos is a generalized space.*
=--

Section \ref{ToposesAndUniversalAlgebra} is on connections with universal algebra:

+-- {: style="text-align: center"}
*a topos is a generalized theory.*
=--

What this means is that there is one topos embodying the concept of 'ring',
another embodying the concept of 'field', and so on.  This is the story of
classifying toposes.

Sections \ref{ToposesAndSetTheory}-\ref{ToposesAndUniversalAlgebra} can be read in any order, except that ideally Secion \ref{ToposesAndGeometry} (geometry) should come before Section \ref{ToposesAndUniversalAlgebra} (universal algebra).  You *can* read Section \ref{ToposesAndUniversalAlgebra} without having read Section \ref{ToposesAndGeometry}, but the price to pay is that the notion of 'geometric morphism'--defined in Section \ref{ToposesAndGeometry} and used in Section \ref{ToposesAndUniversalAlgebra}--might seem rather mysterious.

Algebraic geometers beware: the word 'topos' is used by mathematicians in two
slightly different senses, according to circumstance and culture.  There are
elementary toposes and Grothendieck toposes.  Category theorists tend to use
'topos' to mean 'elementary topos' by default, although Grothendieck toposes
are also important in category theory.  But when an algebraic geometer says
'topos', they almost certainly mean 'Grothendieck topos' (what else?).

Grothendieck toposes are categories of sheaves.  Elementary toposes are
slightly more general, and the definition is simpler.  They are what I will 
emphasize here.  Grothendieck toposes are the subject of
Section \ref{ToposesAndGeometry}, and appear fleetingly elsewhere; but if you only want
to learn about categories of sheaves, this is probably not the text for you.



###### Acknowledgements ######
{: .paragraph}
  I thank Andrei Akhvlediani, Eugenia Cheng,
Richard Garner, Nick Gurski, Ignacio Lopez Franco and Emily Riehl for their
participation and encouragement.  Aspects of Section \ref{ToposesAndUniversalAlgebra} draw
on a vaguely similar presentation of vaguely similar material by Richard
Garner.  I thank the organizers of Category Theory 2010 for making the talks
possible, even though they did not mean to: Francesca Cagliari, Marco Grandis,
Sandra Mantovani, Eugenio Moggi, Pino Rosolini, and Bob Walters.  I thank
Scott Carter, Jon Phillips, Mike Shulman, Alex Simpson, Danny Stevenson and
Todd Wilson for suggestions and corrections.  The commutative diagrams were
made using Paul Taylor's macros.

+-- {: .num_section #TheDefinitionOfTopos}
=--
## The  definition of topos ## {: .num_section}


The hardest part of the definition of topos is the concept of subobject
classifier, so I will begin there.

In the category of sets, inverse images are a special case of pullbacks.
That is, given a map $f\colon X \to Y$ of sets and a subset $B \subseteq Y$, we have a
pullback square

$$
\begin{matrix}
\mathllap{f^{-1}} B &  \begin{svg}[[!include SVG rightarrow]]\end{svg} & B \\
\begin{svg}[[!include SVG hookdownarrow]]\end{svg}
\mathrlap{\array{\arrayopts{\align{bottom}}\;\begin{svg}[[!include SVG pullback]]\end{svg}\\ \space{30}{10}{1}}} && \begin{svg}[[!include SVG hookdownarrow]]\end{svg} \\
X & \underset{\scriptsize f}{\begin{svg}[[!include SVG rightarrow]]\end{svg}} & Y
\end{matrix}
$$

In particular, this holds when $B$ is a 1-element subset $\{y\}$ of $Y$:

$$
\begin{matrix}
\mathllap{f^{-1}} \{y\} &  \begin{svg}[[!include SVG rightarrow]]\end{svg} & \{y\} \\
\begin{svg}[[!include SVG hookdownarrow]]\end{svg}
\mathrlap{\array{\arrayopts{\align{bottom}}\;\begin{svg}[[!include SVG pullback]]\end{svg}\\ \space{30}{10}{1}}} && \begin{svg}[[!include SVG hookdownarrow]]\end{svg} \\
X & \underset{\scriptsize f}{\begin{svg}[[!include SVG rightarrow]]\end{svg}} & Y
\end{matrix}
$$

There is no virtue in distinguishing between one-element sets, so we might as
well write $1$ instead of $\{y\}$; then the inclusion $\{y\} \hookrightarrow Y$ becomes
the map $1 \to Y$ picking out $y \in Y$, and we have a pullback square

$$
\begin{matrix}
\mathllap{f^{-1}} \{y\} &  \overset{\scriptsize !}{\begin{svg}[[!include SVG rightarrow]]\end{svg}} & 1 \\
\array{\begin{svg}[[!include SVG hookdownarrow]]\end{svg}}
\mathrlap{\array{\arrayopts{\align{bottom}}\space{0}{30}{10}\begin{svg}[[!include SVG pullback]]\end{svg}}} && \array{\begin{svg}[[!include SVG downarrow]]\end{svg}} \mathrlap{y} \\
X & \underset{\scriptsize f}{\begin{svg}[[!include SVG rightarrow]]\end{svg}} & Y
\end{matrix}
$$


Next consider characteristic functions of subsets.  Fix a two-element set $2 =
\{