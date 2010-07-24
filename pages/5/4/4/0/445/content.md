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

To discuss images in a category $C$, we must first fix a notion of [[subobject]] or [[embedding]] in $C$.  (Sometimes we want these to be the [[monomorphisms]], but sometimes we want the [[regular monomorphisms]] instead.)  Then [[generalized the|the]] **image**  of a [[morphism]] $f\colon A\to B$ in $C$ is a universal factorization of $f$ into a composite $A \to im(f) \to C$ such that $im(f)\to C$ is a subobject, of the specified sort.

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
$$\array{ & \overset{h}{\to} & \\
  ^e\downarrow && \downarrow^n\\
  & \underset{k}{\to} & }$$
is a commutative square with $n\in M$, then the pullback $k^*n$ is an $M$-morphism through which $e$ factors.  Hence $k^*n$ must be an isomorphism, and so the square admits a diagonal filler, which is unique since $n\in M$ is monic.  It follows that if all $M$-images exist in $C$, then $M$ is the right class of an [[orthogonal factorization system]], and $M$-images are precisely the factorizations in this OFS.

Conversely, it is easy to see that if $(E,M)$ is an OFS on a category $C$, then all $M$-images exist and are given by the factorizations of the OFS.  Therefore, to give a notion of image is more or less equivalent to giving an orthogonal factorization system.

### Duality

Note that the notion of factorization system is self-dual.  Therefore, if $(E,M)$ is a factorization system and $c \overset{e}{\to} a \overset{m}{\to} d$ is an $(E,M)$-factorization of $f\colon c\to d$, then not only is $m$ the $M$-image of $f$ (the largest $M$-subobject through which $f$ factors), but dually $e$ is also the **$E$-coimage** of $f$, i.e. the smallest $E$-quotient through which $f$ factors.

However, see below for additional remarks on the usage of the terms "image" and "coimage."

## Construction using limits

If the category $C$ admits finite [[limits]] and [[colimits]], then the image $Im f$ of a morphism $f : c \to d$ my be expressed as 

$$
  Im f \simeq lim (d \stackrel{\to}{\to} d \sqcup_c d)
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

In other words, the image is the [[equalizer]] of the [[cokernel pair]].

This is [[isomorphism|isomorphic]] to the [[pullback]] $d \times_{d \sqcup_c d} d$

$$
 im f \simeq d \times_{d \sqcup_c d} d
 \,.
$$

So in the diagram

$$
  \array{
    c &&\stackrel{f}{\to}&& d
    \\
    & \searrow && \nearrow
    \\
    \downarrow^f
    && im f&&
    \downarrow
    \\
    & \swarrow
    \\
    d
    &&\to&&
    d \sqcup_c d
  }
$$

the outer square is a [[pushout]] and the inner one is a [[pullback]].

Since $im f$ is an [[equalizer]], the morphism

$$
  im f \to d
$$

is a [[monomorphism]]. In fact it is necessarily a [[regular monomorphism]].

+-- {: .un_lemma}
###### Lemma

There is a unique  morphism

$$
 u :  coim f \to im f
$$

from the [[coimage]] to the image of $f$ such that

$$
  f = (c \to coim f \stackrel{u}{\to} im f \to d)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Because $f$ coequalizes $c \times_d c \stackrel{\to}{\to} c$, a morphism $h$ in 

$$
  \array{
    c 
      &\times_d c \stackrel{\to}{\to}&
    c
    &\stackrel{f}{\to}&
    d
    &\stackrel{\to}{\to}&
    d \sqcup_{c} d
    \\
   && {}^{\;}\downarrow^{epi} &{}^{h}\nearrow& {}^{\;}\uparrow^{mono}
   \\
    && coim f && im f
  }
$$

exists uniquely.

Because $c \to coim f$ is [[epimorphism|epi]] it follows that $h$ equalizes $d \stackrel{\to}{\to} d \sqcup_c d$ and hence $u$ in the diagram

$$
  \array{
    c 
      &\times_d c \stackrel{\to}{\to}&
    c
    &\stackrel{f}{\to}&
    d
    &\stackrel{\to}{\to}&
    d \sqcup_{c} d
    \\
   && {}^{\;}\downarrow^{epi} &{}^{h}\nearrow& {}^{\;}\uparrow^{mono}
   \\
    && coim f &\stackrel{u}{\to}& im f
  }
$$

exists uniquely.

=--


**Remarks**

* If $u$ is an [[isomorphism]] then $f$ is called a [[strict morphism]].

* So if $C$ has finite limits and colimits and every morphism is a [[strict morphism]] we get an [[weak factorization system|epi-mono factorization]] of every morphism $f : c \to d$ through its image $\simeq$ coimage.

* there are various generalizations of the notion of image to [[higher category theory|higher categorical]] contexts

  * in [[Cat]] there is the notion of [[essential image]] of a [[functor]]

  * in a [[presentable (infinity,1)-category]] or [[model category]] there is the notion of [[homotopy image]].

* If the factorization of a morphism $f$ through its image is by an [[isomorphism]] then the morphism probably deserves to be called an [[embedding]].


## In higher category theory 

In [[higher category theory]] there are generalizations of the notion of image, such as these:

* [[essential image]] (of a [[functor]])
* [[homotopy image]].

However, it is not clear that either serves as the proper categorification of the notion described above.

There are several properties we might want a 'higher image' to have. For example, in an $2$-category, we might want isomorphic 1-cells to have equivalent images. In **Cat**, we might want the image of a functor between discrete categories to be its image as a function.

### In $(\infty,1)$-category theory {#InfImage}
 
Probably an **$(\infty,1)$-image** of a morphism $f : c \to d$ in an [[(∞,1)-category]] with [[(∞,1)-limit]]s and -colimits should be defined to be the [[(∞,1)-limit]] over the [[Cech nerve|Cech co-nerve]] of $f$:

$$
  im f := \lim_{\leftarrow}
  \left(
    d \stackrel{\to}{\to} d \coprod_c d 
    \stackrel{\to}{\stackrel{\to}{\to}}
    d \coprod_c d \coprod_c d
    \stackrel{\to}{\stackrel{\to}{\stackrel{\to}{\to}}}
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
