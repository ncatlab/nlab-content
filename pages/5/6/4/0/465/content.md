

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An [[epimorphism]] is _regular_ if it behaves like a [[covering]].


* [[effective epimorphism]] $\Rightarrow$ [[regular epimorphism]] $\Leftrightarrow$ [[covering]]

* [[effective monomorphism]] $\Rightarrow$ [[regular monomorphism]] $\Leftrightarrow$ [[embedding]] .


## Definition 

A **regular epimorphism** is a [[morphism]] $f : c \to d$ (in a given [[category]]) that is the [[coequalizer]] of _some_ parallel pair of morphisms, i.e. if there exists _some_ [[colimit]] diagram of the form

$$
  a \stackrel{\to}{\to} c \stackrel{f}{\to} d
  \,.
$$

The [[duality|dual]] concept is that of [[regular monomorphism]].  A morphism having a [[kernel pair]] (such as any morphism in a category with [[pullback]]s) is a regular epimorphism if and only if it is the [[quotient object]] of its kernel pair (see for instance Lemma 5.6.6 in _[[Practical Foundations]]_; this also follows from the theory of [[generalized kernels]]).  In general, a regular epimorphism with a kernel pair is an __[[effective epimorphism]]__.

Although the definition doesn\'t state so explicitly, it is true that any regular epimorphism is an [[epimorphism]]. In fact, every regular epimorphism is a [[strong epimorphism]]. On the other hand, every [[split epimorphism]] is regular.

## Examples

* In [[Set|the category of sets]], every epimorphism is regular. Thus, it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use. In particular, one may define a [[projective object]] (and hence the [[axiom of choice]]) using regular epimorphisms.

* In the category of [[monoid]]s, the inclusion $\mathbb{N}\hookrightarrow\mathbb{Z}$ is an epimorphism, even though it is far from a [[surjection]].  But in this or any other [[algebraic category]] (a category of models of an [[algebraic theory]]), the morphisms whose underlying function is surjective are precisely the regular epimorphisms.


## In the context of higher category theory {#HigherCat}

Comparing the above to the defintion of [[effective epimorphism]], we propose the following definition in an [[(∞,1)-category]]:  

A __regular epimorphism__ $f : c \to d$ in an [[(∞,1)-category]] $C$ is a morphism with a [[simplicial resolution]]:

one for which there exists a functor $c : \Delta^{op} \to C$, such that $f$  is the [[colimit in a quasi-category|colimiting cocone]]

$$
  \cdots c_2 \stackrel{\to}{\stackrel{\to}{\to}} c_1 \stackrel{\to}{\to} c \stackrel{f}{\to} d
$$

over this diagram.

This is a morphism such that for all objects $e \in C$ the induced morphism $f^* : C(d,e) \to C(c,e)$ is a [[regular monomorphism]] in the [[(∞,1)-category]] [[∞Grpd]].

Compare this to the stronger notion of an [effective ∞-epimorphism](http://ncatlab.org/nlab/show/effective+epimorphism#HigherCat).

**Warning**. Such a morphism may fail to satisfy some condition for being a plain _epimorphism_ in an [[(∞,1)-category]] that you might think of. The idea is that there may not be a good notion of epimorphism in an [[(∞,1)-category]] apart from regular epimorphism.

+--{: .query}

> a previous version of this entry caused the following discussion

[[Mike Shulman]]: I would expect a "regular epimorphism" to be, in particular, an "epimorphism," and I would expect an "epimorphism" $e\colon A\to B$ to mean that $hom(e,X)\colon hom(B,X)\to hom(A,X)$ is a "monomorphism" in some sense.  But it's unclear to me whether morphisms with a simplicial resolution have this property.  In a 1-category, it's true of course that if $e$ is a coequalizer then $hom(e,X)$ is monic (injective), but in a (2,1)-category, all you can say if $e$ has a (truncated) simplicial resolution is that $hom(e,X)$ is faithful (i.e. precomposing with $e$ is injective on the 2-cells of your (2,1)-category, but not necessarily any more than that).  It seems fairly likely to me that as you go up to the $(\infty,1)$-context the injectivity will be "pushed off to infinity" and there will be *no* monic-like property of $hom(e,X)$ left.

I'm not *necessarily* saying we shouldn't use the term "regular epimorphism" in this sense, since as we know the notion of "plain epimorphism" in 1-categories is not usually very useful anyway.  But if I'm right, I think it would be good to alert the reader that the [[red herring principle]] is coming into play.

[[Urs Schreiber]]: following the [discussion](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=326&page=1#Item_10) at the $n$Forum I put in the above warning.

=--



[[!redirects regular epi]]
[[!redirects regular epimorphisms]]
[[!redirects regular epis]]