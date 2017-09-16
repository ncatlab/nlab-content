#Idea#

Given a collection of "parameterized objects", i.e. a [[functor]] $F : C \to D$, it is often of interest to consider the category whose objects are [[generalized element]]s of the objects of $D$ in the image of $F$, and whose morphisms are the maps between these generalized elements induced by the value of $F$ on morphisms in $C$.

For $D = $ [[Set]] and and with [[generalized element]] read as "ordinary element of a set" is yields the [[category of elements]] of the (co)[[presheaf]] $F : C \to D$.

Moreover, the description of of the [[category of elements]] of a presheaf in terms of a pullback of a [[generalized universal bundle]] generalizes directly to categories of generalized elements. 


#Definition#

Let $D$ be a [[pointed object]] in [[Cat]], i.e. a [[category]] equipped with a choice $pt_D : {*} \to D$ of one of its objects.

Recall that a morphism $pt_D \to d$ in $D$ may be called a [[generalized element]] in $D$ "with domain of definition" being the object $pt_D$.

For instance if $D =$ [[Set]] the canonical choice is $pt_{Set} = {*}$ [[generalized the|the]] set with a single element. Generalized elements of a set "with domain of definition" ${*}$ are just the ordinary elements of a set.

Notice that the [[over category]] $({pt_D/D})$ is the category of generalized elements of $D$ with domain of definition $pt_D$:

* objects are such generalized elements $\delta : pt_D \to d$ of objects $d \in D$;

* morphisms $\delta \to \gamma$ are given whenever a morphism $f : d \to d'$ in $D$ takes the element $\delta$ to $\delta'$, i.e. whenever there is a commuting triangle
  $$
    \array{
      && pt_D
      \\
      & {}^\delta\swarrow && \searrow^{\delta'}
      \\
      d &&\stackrel{f}{\to}&& d'
    }
    \,.
  $$

Notice that the canonical projection $(pt_D/D) \to D$ from the [[over category]] that forgets the tip of these trangles may be regarded as the [[generalized universal bundle]] for the given pointed category $D$: it is the left composite vertical morphism in the pullback

$$
  \array{
    (pt_D/D) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    D^I &\stackrel{d_0}{\to}& D
    \\
    \downarrow^{d_1}
    \\
    D
  }
$$

(see also [[comma category]] for more on this perspective). So in fact such "categories of generalized elements" are precisely the [[generalized universal bundle]]s in the 1-categorical context. And both are really fundamentally to be thought of as intermediate steps in the computation of [[weak limit|weak pullback]]s, as described now.


The above allows to generalize the notion of _category of generalized elements_ a bit further to that of generalized elements of functors with values in $D$: let $F : C \to D$ be a functor with codomain our category $D$ with point $pt_D$. 

The **category of generalized elements** of $F$ is the [[pullback]] $El_{pt_D}(F) := C \times_D (pt_D/D)$

$$
  \array{
    El_{pt_D}(F) &\to& (pt_D/D)
    \\
    \downarrow && \downarrow
    \\
    C &\stackrel{F}{\to}& D
  }
  \,.
$$

This means:

* the objects of $El_{pt_D}(F)$ are all the generalized elements $\delta_c : pt_D \to F(c)$ for all $c \in C$;

* a morphism $\delta_c \to \delta_{c'}$ between two such generalized elements is a commuting triangle
  $$
    \array{
      && pt_D
      \\
      & {}^{\delta_c}\swarrow && \searrow^{\delta_{c'}}
      \\
      F(c) && \stackrel{F(f)}{\to} && F(c')
    }
    \,.
  $$
  for all morphisms $f : c \to c'$ in $C$.


#Examples#

##ordinary catgeory of elements##

For $D = $ [[Set]] and $pt_{Set} = {*}$
the above reproduces the notion of [[category of elements]]#
of a [[presheaf]].

##Action Groupoid##

Given a vector space $V$, a [[group]] $G$ recall that a [[representation]] of $G$ on $V$ 

$$V\bullet\righttoleftarrow G$$

is canonically identified with a [[functor]]

$$
  \rho : \mathbf{B} G \to Vect
  \,.
$$



$$
  \rho : ({*} \stackrel{g}{\to} {*}) \mapsto
  (V \stackrel{\rho(g)}{\to} V)
  \,.
$$

The category [[Vect]] of $k$-vector spaces for some [[field]] $k$ has a standard point $pt_{Vect} \to Vect$, namely the field $k$ itself, regarded as the canonical 1-dimensional $k$-vector space over itself.

The corresponding [[over category]] of generalized elements of [[Vect]] $(pt_{Vect}/ Vect)$ has as objects pointed vector spaces and as morphisms linear maps of pointed vector spaces that map the chosen vectors to each other.

Now, as described in detail at [[action groupoid]] the category of generalized elements of the representation $\rho$ is the [[action groupoid]] $V//G$ of $G$ acting on $V$

$$
  \array{
   V//G &\to& Vect_*
   \\
   \downarrow && \downarrow
   \\
   \mathbf{B} G &\to& Vect
  }
   \,.
$$

As described there, $V//G \to \mathbf{B}G$ is the [[groupoid]] incarnation of the vector bundle that is associated via $\rho$ to the universal $G$-bundle on the [[classifying space]] $B G$.

##References##

* [Exploding a Category](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html#c017574)