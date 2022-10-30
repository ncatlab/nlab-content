
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _$n$-fold Segal space_ is  an $n$-fold [[pre-category object in an (infinity,1)-category|pre-category object]] in [[∞Grpd]]. If this happens to be an actual $n$-fold [[category object in an (infinity,1)-category|category object]] it is an [[n-fold complete Segal space]].


## Definition

### Lurie

In ([Lurie, section 1.3](#Lurie)) a recursive definition is given: a (complete) $(n+1)$-Segal space is a [[complete Segal space]] object in an [[(∞,1)-category]] of complete $n$-Segal spaces.

This is discussed at _[[n-fold complete Segal space]]_.

### Dyckerhoff-Kapranov
 {#DyckerhoffKapranov}

In ([DyckerhoffKapranov](#DyckerhoffKapranov)) a 2-Segal space is defined to be a simplicial space with a higher analog of the weak composition operation known from [[Segal spaces]].

Let $X$ be a [[simplicial topological space]] or [[bisimplicial set]] or generally a [[simplicial object]] in a suitable [[simplicial model category]].


For $n \in \mathbb{N}$ let $P_n$ be the $n$-[[polygon]]. For any [[triangulation]] $T$ of $P_n$ let $\Delta^T$ be the corresponding [[simplicial set]]. Regarding $\Delta^n$ as the cellular [[boundary]] of that polygon provides a morphism of simplicial sets $\Delta^T \to \Delta^n$.

Say that $X$ is a **2-Segal object** if for all $n$ and all $T$ as above, the induced [[morphisms]]

$$
  X_n := [\Delta^n, X]
  \to 
  X_T := [\Delta^T,X]
$$

are [[weak equivalences]].

**Warning.** A Dyckerhoff-Kapranov "2-Segal spaces" is not itself a model for an [[(∞,2)-category]]. Instead, it is a model for an [[(∞,1)-operads]] ([Dyckerhoff-Kapranov, section 3.6](#DyckerhoffKapranov)).

## References

The notion of higher Segal space as a modl for [[(∞,n)-categories]] is discussed in

* [[Jacob Lurie]], _$(\infty,2)$-categories and the Goodwillie calculus I_ ([pdf](http://www.math.harvard.edu/~lurie/papers/GoodwillieI.pdf))
  {#Lurie}

For more references along these lines see at _[[n-fold complete Segal space]]_

The Dyckerhoff-Kapranov "higher Segal spaces" [above](#DyckerhoffKapranov) are discussed in

* Tobias Dyckerhoff, [[Mikhail Kapranov]], _Higher Segal spaces I_, ([arxiv:1212.3563](http://arxiv.org/abs/1212.3563))

* Tobias Dyckerhoff, _Higher Segal spaces _, talk at Steklov Mathematical Institute (2011) ([video](http://www.mathnet.ru/php/presentation.phtml?presentid=3718&option_lang=eng))
 {#DyckerhoffKapranov}

* [[Mikhail Kapranov]], _Higher Segal spaces _, talk at IHES (2012) ([video](http://www.dailymotion.com/video/xpm3at_mikhail-kapranov-a-meeting-on-the-occasion-of-the-75th-birthday-of-yuri-ivanovich-manin_tech))
 {#DyckerhoffKapranov}

[[!redirects higher Segal space]]
[[!redirects higher Segal spaces]]

[[!redirects higher complete Segal space]]
