
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

> This page contains the beginning of the LaTeX-to-instiki conversion of an article submitted for peer-review to the [[annals:HomePage|Annals of the nLab]].

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