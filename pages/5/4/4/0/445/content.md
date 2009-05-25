#Idea#

The familiar notion of the image of a map of sets may be formalized to yield a notion of image for morphisms in an arbitrary [[category]].

#Definition#

There are several defintions that are equivalent when they jointly apply.


## In terms of subobjects ##

Let $C$ be a [[category]], and $f: c \to d$ be a [[morphism]]. The **image** of $f$ is the smallest [[subobject]] $s \subseteq d$ through which $f$ factors (if it exists). There is a [[duality|dual]] notion of _[[coimage|co-image]]_: the largest [[quotient object|quotient]] (in the co-subobject sense) of $c$ through which $f$ factors. 


### Remarks ####

* If $C$ admits equalizers, and if $i: k \to d$ represents the image of $f: c \to d$, then the unique map $q: c \to k$ such that $f = i q$ is an epimorphism. Thus, in a finitely complete category in which every morphism admits an image, one obtains in this way an [[weak factorization system|epi-mono factorization]], but the factorization may not have particularly good properties (in particular, the factorization through the image might not be stable with respect to [[pullback]]). 

* The notion of [[regular category]] formalizes a sense in which image factorizations do behave well: factorizations into a [[regular epimorphism]] followed by a mono which are stable under pullback. 



## as a left adjoint functor ##

Alternatively, let $C/d$ be the [[over category|slice category]] over $d$, and let $Mono(C)/d$ be the full subcategory whose objects are monos into $d$. Assuming images exist in $C$, taking the image of a map $f: c \to d$ provides a [[adjoint functor|left adjoint]] 

$$C/d \to Mono(C)/d$$ 

to the inclusion $Mono(C)/d \hookrightarrow C/d$. 



## as an equalizer ##

If the category $C$ admits finite [[limit]]s and [[colimit]]s, then the image $Im f$ of a morphism $f : c \to d$ my be expressed as 

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

is a [[monomorphism]].

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


###Remarks###

* If $u$ is an [[isomorphism]] then $f$ is called a [[strict morphism]].

* So if $C$ has finite limits and colimits and every morphism is a [[strict morphism]] we get an [[weak factorization system|epi-mono factorization]] of every morphism $f : c \to d$ through its image $\simeq$ coimage.

