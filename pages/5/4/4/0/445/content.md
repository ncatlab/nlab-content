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

The **image** of a [[function]] $f\colon A\to B$ between [[sets]] is the [[subset]] of $B$ consisting of all those elements $b\in B$ that are of the form $f(a)$ for some $a\in A$.  This notion can be generalized from [[Set]] to other categories, as follows.

To discuss images in a category $C$, we must first fix a notion of [[subobject]] or [[embedding]] in $C$.  (Sometimes we want these to be the [[monomorphisms]], but sometimes we want the [[regular monomorphisms]] instead.)  Then [[generalized the|the]] **image**  of a [[morphism]] $f\colon A\to B$ in $C$ is a universal factorization of $f$ into a composite $A \to im(f) \to B$ such that $im(f)\to B$ is a subobject, of the specified sort.

Note that in this generality, a given morphism may or may not have an image, although if it does, it is unique up to isomorphism by universality.  In many cases, images can be constructed out of [[limits]] and [[colimits]] in the ambient category.  In particular, in a [[regular category]], images (relative to all monomorphisms) can be constructed as the [[quotient object]] of a [[kernel pair]].


## Definition

Let $C$ be a [[category]], let $M\subset Mono(C)$ be a subclass of the monomorphisms in $C$, and let $f: c \to d$ be a [[morphism]] in $C$.  The **image** of $f$ is the smallest $M$-[[subobject]] $im(f) \hookrightarrow d$ through which $f$ factors (if it exists).

In other words, it is a factorization $c \overset{e}{\to} im(f) \overset{m}{\to} d$ of $f$ (i.e. $f = m e$) such that $m\in M$, and given any other factorization $f = m' e'$ with $m'\in M$, we have $m \subseteq m'$ as subobjects of $C$ (i.e. $m$ factors through $m'$, $m = m' k$ for some $k$).  Such a factorization is unique up to unique isomorphism, if it exists.

This can be phrased equivalently as follows.  Let $C/d$ be the [[slice category]] of $C$ over $d$, and let $M/d$ be its full subcategory whose objects are $M$-morphisms into $d$.  If all images exist in $C$, then taking the image of a map $f: c \to d$ provides a [[left adjoint]]

$$C/d \to M/d$$ 

to the inclusion $M/d \hookrightarrow C/d$.  More generally, an image of a single morphism $f\colon c\to d$ is a [[universal arrow]] from $f$ to this inclusion.


## Examples

* In [[Set]], for $M=$ monomorphisms = [[injections]], this reproduces the ordinary notion of image.

* In algebraic categories such as [[Grp]], for $M=$ monomorphisms, this also reproduces the ordinary notions of image.

* In [[Top]], for $M=$ [[subspace]] inclusions, the $M$-image is the set-theoretic image topologized as a subspace of the [[target|codomain]].  On the other hand, for $M=$ injective continuous maps, the $M$-image is the set-theoretic image topologized as a quotient space of the [[source|domain]].

* A [[regular category]] can be defined as a [[finitely complete category]] in which all images exist for $M=$ monomorphisms, and such images are moreover stable under [[pullback]].  In particular, this includes any [[topos]].

* In [[Cat]] (considered as a [[1-category]]), the image of a [[functor]] $F\colon A\to B$ is the smallest [[subcategory]] of $B$ which contains images through $F$ of all morphisms in $A$.  Note that some of the morphisms in the image may not be images of any morphism in $A$; all morphisms in the image of $F$ are [[composite|compositions]] in $B$ of $B$-composable sequences of images of morphisms in $A$, but these themselves do not necessarily form $A$-composable sequences of morphisms in $A$.

  Usually it is better to treat $Cat$ as a 2-category, in which case one can use a more 2-categorical notion of image.  See, for instance, [[full image]], [[essential image]], and [[replete image]].


## Relation to factorization systems

Suppose that $M$ is closed under composition, and that $f = m e$ is an image factorization relative to $M$.  Then $e$ has the property that if $e = n g$ for some $n\in M$, then $n$ is an isomorphism --- for then we would have $f = (m n) g$ and so by universality of images, $m$ would factor through $m n$.  In particular, if $M$ is the class of all monomorphisms and $C$ has [[equalizers]], then $e$ is an [[extremal epimorphism]].

If $C$ has [[pullbacks]] and $M$ is closed under pullbacks, then we can say more: $e$ is [[orthogonality|orthogonal]] to $M$.  For if
$$\array{a & \overset{h}{\to} & b\\
  ^e\downarrow && \downarrow^n\\
  c  & \underset{k}{\to} & d}$$
is a commutative square with $n\in M$, then the pullback $k^*n$ is an $M$-morphism through which $e$ factors.  Hence $k^*n$ must be an isomorphism, and so the square admits a diagonal filler, which is unique since $n\in M$ is monic.  It follows that if all $M$-images exist in $C$, then $M$ is the right class of an [[orthogonal factorization system]], and $M$-images are precisely the factorizations in this OFS.

Conversely, it is easy to see that if $(E,M)$ is an OFS on a category $C$, then all $M$-images exist and are given by the factorizations of the OFS.  Therefore, to give a notion of image is more or less equivalent to giving an orthogonal factorization system.

### Duality

Note that the notion of factorization system is self-dual.  Therefore, if $(E,M)$ is a factorization system and $c \overset{e}{\to} a \overset{m}{\to} d$ is an $(E,M)$-factorization of $f\colon c\to d$, then not only is $m$ the $M$-image of $f$ (the largest $M$-subobject through which $f$ factors), but dually $e$ is also the **$E$-coimage** of $f$, i.e. the smallest $E$-quotient through which $f$ factors.

However, see below for additional remarks on the usage of the terms "image" and "coimage."

## Construction using limits {#AsEqualizer}

Suppose that the category $C$ admits finite [[limits]] and [[colimits]], and that $M=RegMono$ consists of the [[regular monomorphisms]].  Then the $M$-image of a morphism $f : c \to d$ may be constructed as

$$
  Im f \simeq lim (d \rightrightarrows d \sqcup_c d)
  \,,
$$

where $d \sqcup_c d$ denotes the [[pushout]]

$$
  \array{
    c &\stackrel{f}{\to}& d
    \\
    \downarrow^{f} && \downarrow
    \\
    d &\to& d \sqcup_c d
  }
  \,.
$$

In other words, the **regular image** is the [[equalizer]] of the [[cokernel pair]].  To see that this is in fact the $RegMono$-image, we first note that it is of course a regular monomorphism by definition, and then invoke the fact that in a category with finite limits and colimits, a monomorphism is regular if and only if it is the equalizer of its cokernel pair.

Dually, the **regular coimage** of a morphism is the [[coequalizer]] of its [[kernel pair]].  In [[Set]] (and more generally in any [[topos]]) these two constructions coincide, but in general they are distinct.  For example, in [[Top]] the regular image is the set-theoretic image topologized as a subspace of the [[target|codomain]], while the regular coimage is the set-theoretic image topologized as a quotient space of the [[source|domain]].

Note that some authors drop the "regular" and simply call these constructions the **image** and **coimage** respectively.  This can be confusing, however, since in many cases (such as in any [[regular category]]) the *regular coimage* coincides with the $M$-image for $M=Mono$ the class of all monomorphisms, which it is also natural to simply call the *image*.

### Comparison of regular images and coimages

Suppose that $M_1$ and $M_2$ are two classes with $M_1\subseteq M_2$.  If $f$ has both an $M_1$-image $im_1(f)$ and an $M_2$-image $im_2(f)$, then by universality, the latter must factor through the former.  See [[2-stage factorization system]].

As a special case of this, we have:

+-- {: .un_lemma}
###### Lemma
If $C$ has finite limits and colimits, then there is a unique map
$$
 u :  coim f \to im f
$$
from its regular coimage to its image such that
$$
  f = (c \to coim f \stackrel{u}{\to} im f \to d)
  \,.
$$
=--

+-- {: .proof}
###### Proof

Because $f$ coequalizes $c \times_d c \rightrightarrows c$, a morphism $h$ in 

$$
  \array{
    c 
      &\times_d c \rightrightarrows&
    c
    &\stackrel{f}{\to}&
    d
    &\rightrightarrows&
    d \sqcup_{c} d
    \\
   && {}^{\;}\downarrow^{epi} &{}^{h}\nearrow& {}^{\;}\uparrow^{mono}
   \\
    && coim f && im f
  }
$$

exists uniquely.

Because $c \to coim f$ is [[epimorphism|epi]] it follows that $h$ equalizes $d \rightrightarrows d \sqcup_c d$ and hence $u$ in the diagram

$$
  \array{
    c 
      &\times_d c \rightrightarrows&
    c
    &\stackrel{f}{\to}&
    d
    &\rightrightarrows&
    d \sqcup_{c} d
    \\
   && {}^{\;}\downarrow^{epi} &{}^{h}\nearrow& {}^{\;}\uparrow^{mono}
   \\
    && coim f &\stackrel{u}{\to}& im f
  }
$$

exists uniquely.

=--

If this map $u$ is an [[isomorphism]], then $f$ is sometimes called a [[strict morphism]].  In particular, if $C$ has finite limits and colimits and every morphism is a strict morphism, then the regular image and regular coimage factorizations coincide and give an epi-mono factorization system.


## In higher category theory 

In [[higher category theory]] there are generalizations of the notion of image, such as these:

* [[essential image]] (of a [[functor]])
* [[homotopy image]].

However, it is not clear that either serves as the proper categorification of the notion described above.

There are several properties we might want a 'higher image' to have. For example, in an $2$-category, we might want isomorphic 1-cells to have equivalent images. In **Cat**, we might want the image of a functor between discrete categories to be its image as a function.  One fruitful direction is to study a [[factorization system in a 2-category]].


### In $(\infty,1)$-category theory {#InfImage}

A **(regular) $(\infty,1)$-image** of a morphism $f : c \to d$ in an [[(∞,1)-category]] with [[(∞,1)-limit]]s and -colimits should be defined to be the [[(∞,1)-limit]] over the [[Cech nerve|Cech co-nerve]] of $f$:

$$
  im f := \lim_{\leftarrow}
  \left(
    d \rightrightarrows d \coprod_c d 
    \stackrel{\to}{\rightrightarrows}
    d \coprod_c d \coprod_c d
    \stackrel{\to}{\stackrel{\to}{\rightrightarrows}}
    \cdots
  \right)
  \,.
$$

Notice that 

* this reduces to the above [equalizer definition](#AsEqualizer) in the case that the ambient $(\infty,1)$-category is just an ordinary category;

* this implies that the inclusion $im f \to d$ is a [[regular monomorphism]] in the $(\infty,1)$-category sense (described [here](http://ncatlab.org/nlab/show/regular+monomorphism#Infty1Version)).

#### Examples {#InfImageExamples}

Applied to the $(\infty,1)$-category [[∞Grpd]] this gives a notion of image of [[(∞,1)-functor]]s between [[∞-groupoid]]s and hence a notion of image of [[functor]]s between [[groupoid]]s, [[2-functor]]s between [[2-groupoid]]s, etc.

[[!redirects images]]
