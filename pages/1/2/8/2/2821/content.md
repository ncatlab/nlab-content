
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Representable multicategories #
* table of contents
{:toc}

## Idea

The _representable multicategory_ underlying a [[monoidal category]] $C$ is a [[multicategory]] whose $n$-ary morphisms are the [[morphisms]] out of $n$-fold [[tensor products]] in $C$, i.e.

$$
  Rep(C)_n(c_1, \cdots, c_n,c)
  := 
  Hom_C(c_1\otimes \cdots \otimes c_n, c)
  \,.
$$


## Definition ##

There is one flavor of representable multicategory for every flavor of [[generalized multicategory]].  Here we focus on the two best-known: one for ordinary [[monoidal categories]], giving an ordinary [[multicategory]], and one for [[symmetric monoidal categories]], giving a [[symmetric multicategory]].  Mostly the discussion of both cases proceeds in parallel.

We first give the simple pedestrian definition in terms of explicit components, and then a more abstract definition, which is useful for studying general properties.

### In terms of components

For $(C,\otimes, I)$ a ([[symmetric monoidal category|symmetric]]) [[monoidal category]], the **representable multicategory** $Rep(C)$ is the [[symmetric multicategory|(symmetric)]] [[multicategory]] whose objects are the objects of $C$, and whose objects of $n$-ary operations are the [[hom objects]]

$$
  Rep(C)(c_1, \cdots, c_n ; c) := 
C(c_1 \otimes \cdots \otimes c_n,\; c)
  \,,
$$

This comes with the obvious composition operation induced from the composition in $C$. Moreover, in the symmetric case there is a canonical action of the symmetric group induced.

The full sub-multicategory of $Rep(C)$ on an object $c\in C$, being a one-object multicategory, is a ([[symmetric operad|symmetric]]) [[operad]], called the [[endomorphism operad]] of $c\in C$.  Note that some authors use the term "endomorphism (colored) operad" for the whole multicategory $Rep(C)$.
  

### In terms of Cartesian monads

Let $T : Set \to Set$ be the [[free monoid]] [[monad]]. Notice, from the discussion at _[[multicategory]]_, that a [[multicategory]] $P$ over [[Set]] with object set $C$ is equivalently a monad in the [[bicategory]] of $T$-[[spans]]

$$
  \array{
     && P
     \\
     & \swarrow && \searrow
     \\
     T C && && C
  }
  \,.
$$

In this language, for $C$ a (strict) [[monoidal category]], the corresponding representable multicategory is given by the $T$-span

$$
  \array{
      && & & T Obj(C) \times_{Obj(C)} Mor(C)
      \\
      && & \swarrow && \searrow 
      \\
      && T Obj(C) && && Mor(C)
     \\
     & {}^{\mathllap{id}}\swarrow && \searrow^{\mathrlap{\otimes}}
    && {}^{\mathllap{s}}\swarrow
    && \searrow^{\mathrlap{t}}
     \\
     T Obj(C) &&&& Obj(C) &&&& Obj(C)
  }
  \,,
$$

where $\otimes : T Obj(C) \to C$ denotes the iterated tensor product in $C$, and
where the top square is defined to be the [[pullback]], as indicated.



## Properties

### Adjunction
 {#UniversalCharacterization}

The functor $Rep$ is a [[right adjoint]]; its left adjoint constructs the free monoidal category on a multicategory, which is also known as the [[prop]] associated to the multicategory.  See ([Hermida, theorem 7.2](#Hermida)) for a precise statement in the context of [[non-symmetric operads]] and strict monoidal categories.  In the case of semicartesian multicategories, this free monoidal category is the [[category of operators]] associated to the multicategory.


## Related concepts

* [[endomorphism operad]]

## References

The basic definition of representable symmetric multicategories (there called "endomorphism operads") is for instance in section 1 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ Contemp. Math. 431 (2007) 31-58 ([arXiv:0512576](http://arxiv.org/abs/math/0512576))

A general account of the definition of representable multicategories is in section 3.3 of 

* [[Tom Leinster]], _Higher Operads, Higher Categories_ ([arXiv:math/0305049](http://arxiv.org/abs/math/0305049))

The notion of _representable multicategory_ is due to

* [[Claudio Hermida]], _Representable multicategories_, Adv. Math. 151 (2000), no. 2, 164-225 ([pdf](http://wslc.math.ist.utl.pt/s84.www/cs/claudio/articles/rep-mult.pdf))
  {#Hermida}

Discussion of the [[2-adjunction]] with the left adjoint [[prop]]-construction is around theorem 7.2 there. Characterization of representable multicategories by [[fibrations of multicategories]] is in

* [[Claudio Hermida]], _Fibrations for abstract multicategories_, Field Institute Communications, Volume 43 (2004) ([pdf](http://sqig.math.ist.utl.pt/pub/HermidaC/fib-mul.pdf)) 

and in section 9 of 

* [[Claudio Hermida]], _From Coherent Structures to Universal Properties_ ([arXiv:0006161](http://arxiv.org/abs/math/0006161))

Discussion in the context of [[generalized multicategories]] is in section 9 of

* G. Cruttwell, [[Mike Shulman]], _A unified framework for generalized multicategories_ Theory and Applications of Categories, Vol. 24, 2010, No. 21, pp 580-655. ([TAC](http://www.tac.mta.ca/tac/volumes/24/21/24-21abs.html))

[[!redirects representable multicategory]]
[[!redirects representable multicategories]]
