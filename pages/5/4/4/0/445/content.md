
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

The familiar notion of the image of a map between [[set]]s, i.e. morphisms in [[Set]], may be formalized to yield a notion of image for [[morphism]]s in an arbitrary [[category]].

If the ambient category has sufficient [[limit]]s and [[colimit]]s, we may understand the notion of image as follows:

A [[monomorphism]] is _regular_ if it behaves like an [[embedding]].

* [[effective epimorphism]] $\Rightarrow$ [[regular epimorphism]] $\Leftrightarrow$ [[covering]]

* [[effective monomorphism]] $\Rightarrow$ [[regular monomorphism]] $\Leftrightarrow$ [[embedding]] .

The universal factorization through an embedding is the _image_ . 




## Definitions 

There are several definitions that are equivalent when they jointly apply.


### In terms of subobjects 

Let $C$ be a [[category]], and $f: c \to d$ be a [[morphism]]. The **image** of $f$ is the smallest [[subobject]] $s \subseteq d$ through which $f$ factors (if it exists). There is a [[duality|dual]] notion of _[[coimage|co-image]]_: the largest [[quotient object|quotient]] (in the co-subobject sense) of $c$ through which $f$ factors. 


**Remarks**

* If $C$ admits equalizers, and if $i: k \to d$ represents the image of $f: c \to d$, then the unique map $q: c \to k$ such that $f = i q$ is an epimorphism. Thus, in a finitely complete category in which every morphism admits an image, one obtains in this way an [[weak factorization system|epi-mono factorization]], but the factorization may not have particularly good properties (in particular, the factorization through the image might not be stable with respect to [[pullback]]). 

* The notion of [[regular category]] formalizes a sense in which image factorizations do behave well: factorizations into a [[regular epimorphism]] followed by a mono which are stable under pullback. 

* In [[Cat]], the __image__ of a [[functor]] $F:A\to B$ is the smallest [[subcategory]] of $B$ which contains images through $F$ of all morphisms in $A$.  Some of the morphisms in the image may not be images of any morphism in $A$; all morphisms in the image of $F$ are [[composite|compositions]] in $B$ of $B$-composable sequences of images of morphisms in $A$ which themselves do not necessarily form $A$-composable sequences of morphisms in $A$. Sometimes the notion of   [[essential image]] is more appropriate; as the essential image is only [[equivalence of categories|equivalent]] to the image, this is somewhat $2$-[[2-category|category]]-theoretic point of view.  


### As a left adjoint functor

Alternatively, let $C/d$ be the [[over category|slice category]] over $d$, and let $Mono(C)/d$ be the full subcategory whose objects are monos into $d$. Assuming images exist in $C$, taking the image of a map $f: c \to d$ provides a [[adjoint functor|left adjoint]] 

$$C/d \to Mono(C)/d$$ 

to the inclusion $Mono(C)/d \hookrightarrow C/d$. 


### As an equalizer {#AsEqualizer}

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