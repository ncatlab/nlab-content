+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

The notion of _sieve_ is a generalization of that of (right) _[[ideal in a monoid]]_ from [[monoids]] to [[categories]]:
a **sieve on** an [[object]] $X$ in a [[category]] $\mathcal{C}$ is a collection of [[morphisms]] with [[codomain]] $X$ that are closed under [[composition|precomposition]] with morphisms in $\mathcal{C}$.

Sometimes one says that a **sieve in** a category $\mathcal{C}$ is a [[full subcategory]] closed under precomposition with morphisms in $\mathcal{C}$ ([Lurie, def. 6.2.2.1](#Lurie)). If so, then a _sieve on_ an object $X$ is a _sieve in_ the [[slice category]] $\mathcal{C}_{/X}$. But a _sieve in_ a category is also naturally taken to be a collection of _sieves on_ various objects. On the other hand, most authors speak just about _sieves on_ an object anyway.

_Sieves on_  objects are an equivalent way to talk about [[subobjects]] of [[representable functors]] in a [[presheaf]] category in terms of the total sets of _elements_ of such a [[subfunctor]].

The notion of _sieve_ is usually used when certain such subobjects are singled out as [[covers]] of a (sifted) [[coverage]]: the singled out subobjects then correspond to _covering sieves_.
Accordingly, the classical examples of _sieves on_ an object are
[[Grothendieck topologies]], used to present the [[presheaves]] that behave like [[coverings]]. They are used to say which [[presheaves]] are actually [[sheaves]] with respect to a given [[coverage]] or [[Grothendieck topology]].


A choice of collections of morphism $d \to c$ into an object $c \in C$  for each $d \in C$ reminds one of the [[representable functor]] [[presheaf]]
$Y(c) := \hom_C(-, c): C^{op} \to Set$ which assigns to each $d \in C$ the set of _all_ morphisms from $d$ to $c$. Every choice of covers of $c$ is therefore for each $d \in C$ a subset of the value of this functor evaluated at $d$. This begins to look like an [[monomorphism|monic]] [[natural transformation]] into this functor. Indeed, it turns out that one can assume without restriction of generality that the assignment of covers of $c$ can always be extended to such a monic natural transformation, and hence one formalizes the notion of "collection of covers" of $c$ as a [[subobject]] $i: F \hookrightarrow \hom(-, c)$ of the functor represented by $c$: a _sieve_ at $c$. 

A dual notion is a [[cosieve]].


## Definition

Let $C$ be a [[small category]].

+-- {: .num_defn}
###### Definition

A _sieve $S$ in $C$_ is a functor $S \hookrightarrow C$ that is both [[fully faithful]] and a [[discrete fibration]].

A _sieve on an object $c \in C$_ is a sieve in the [[slice category]] $C/c$.
=--

Spelling this out, we arrive at the traditional definition of a sieve on an object:

+-- {: .num_defn}
###### Definition

A _sieve_ $S$ on an object $c \in C$ is a subset $S \subset Ob(C/c)$ of the set of objects of the [[over category]] over $c$ which is _closed under precomposition_:  it has the property that whenever $(d \to c) \in S$ and $(e \to d) \in Mor(C)$ then the composition $(e \to d \to c)$ is in $S$.
=--

+-- {: .num_remark}
###### Remark

This is probably called a _sieve_ because it "sifts out" the 'special' maps into $c$ from the set of _all_ maps into $c$.  (Note that 'sieve' is the noun, while 'sift' is the verb.)

The French term for a sieve is _crible_.

=--

+-- {: .num_remark}
###### Remark

Sometimes the condition of a sieve being closed under the operation of precomposing with an arbitrary morphism $g: e \to d$ is called a "saturation condition". Given any collection of morphisms targeted at $c$, one can always close it up, or _saturate_ it, to obtain a sieve on $c$. 

=--



## Properties

### Relation to fibrations

Just as a [[Grothendieck fibration]] is equivalent to a functor $C^o \to Cat$ and a [[discrete fibration]] is equivalent to a functor $C^o \to Set$, a sieve in $C$ is equivalent to a functor $C^o \to \Ohm$, where $\Ohm$ is the preordered category of [[truth values]]. This makes it obvious that a sieve picks out a subset of the objects in a way that is "downward closed". This is a form of [[negative thinking]], as $\Ohm, Set, Cat$ are the categories of all [[(-1,0)-categories]], [[(0,0)-categories]] and [[(1,1)-categories]] respectively..

### Relation to subfunctors 

There is a canonical way to create subfunctors from sieves and sieves from subfunctors.

A [[subfunctor]] is a [[subobject]] in a [[functor category]]. Here, specifically, one is interested in [[subobjects]] in a [[presheaf]] category of [[representable functors]]. It's these subfunctors of representable functors that are in bijection with sieves.

+-- {: .num_defn}
###### Definition

Given a sieve $S$ on $c$, the **subfunctor** $F_S \hookrightarrow Y(c)$ **defined by the sieve**  is the [[presheaf]] 

* that assigns to each object $d \in C$ the set $F_S(d) = \{(d \to c) \in S\}$;

* that assigns to each morphism $(d \to d') \in C$ the function $F_S(d') \to F_S(d)$ induced on elements by precomposition with $d \to d'$.
=--

+-- {: .num_defn}
###### Definition

Given a subfunctor $F \hookrightarrow Y(c)$, the **sieve defined by the subfunctor** is given by

* $S_F \coloneqq \{g: d \to c \in Mor(C) | (Y(d) \stackrel{Y(g)}\to Y(c)) = (Y(d)  \to F \to Y(c)) \}$

or equivalently

* $S_F = \coprod_{d \in Obj(C)}F(d)$.
=--


+-- {: .num_lemma}
###### Lemma

These two definitions establish a bijection between sieves on $c$ and subobjects of $Y(c)$.

For every sieve $S$ we have

$$
  S_{F_S} = S
$$

and for every subfunctor we have

$$
  F_{S_F} = F
  \,.
$$
=--


+-- {: .num_remark}
###### Remarks

* The construction of $S_F$ makes sense for every morphism of presheaves $F \to Y(c)$. The sieve is sensitive precisely to the [[image]] of this map, 
$$
  S_{F} = S_{im (F \to Y(c))}
  \,.
$$

* In the presence of a [[Grothendieck topology]] a morphism $F \to Y(c)$ is sometimes called a [[local epimorphism]] if the sieve $S_F$ is a covering sieve. If $F \to Y(c)$ is actually a subfunctor, then it is called a [[dense monomorphism]].


* The [[pullback]] of a subfunctor $i: F_S \hookrightarrow Y(c) = \hom(-, c)$ along any morphism $\hom(-, g): \hom(-, d) \to \hom(-, c)$ is again a subfunctor $g^* F$ of $d$, hence sieves are closed under pulling back. Concretely, 
$$g^* S = \bigcup_{e \in Ob(C)} \{f: e \to d: g f \in S\}
\,.$$

* A sieve $S_F$ on $c$, for $i: F \hookrightarrow \hom(-, c)$ a subfunctor, may be described as a function which assigns to each object $d$ a collection of morphisms $f: d \to c$ into $c$. Naturality of the inclusion $i$ means that whenever $f: d \to c$ belongs to the sieve and $g: e \to d$ is any morphism, then $f g: e \to c$ also belongs to the sieve. 
=--

+-- {: .num_lemma}
###### Lemma

The subfunctor $F_S \hookrightarrow X$ corresponding to a sieve $S$ is the [[coimage]] of the morphism out of the disjoint union of all objects (regarded as representable presheaves) in the sieve:

$$
 (U = \coprod_{(U_\alpha \to X) \in S} U_\alpha)  \to X
$$

in that

$$
  (F_S \to X) = ((colim(U \times_X U \stackrel{\to}{\to} U)   \to X)
  \,.
$$
=--

If the sieve is generated by (is the saturation of) a collection of morphisms $\{U_\alpha \to U\}$ then the same statement remains true with $U$ being the coproduct over just these $U_\alpha$.

+-- {: .proof}
###### Proof

As described at [[limits and colimits by example]], the colimit of presheaves may be computed objectwise in $Set$. Doing so and using the [[Yoneda lemma]] tells us that for each object $V$ we have

$$
  \begin{aligned}
    colim(U \times_X U \stackrel{\to}{\to} U)(V)
    & \simeq
    colim(Hom(V,U \times_X U) \stackrel{\to}{\to} Hom(V,U))
    \\
    & \simeq
    colim( Hom(V,U) \times_{Hom(V,X)} Hom(V,U)  \stackrel{\to}{\to} Hom(V,U))
  \end{aligned}
$$

where all objects appearing (at least in the first lines) are implicitly regarded as presheaves under the [[Yoneda embedding]].

But this colimit now manifestly computes the set

$$
  \{\text{maps from }\,V\,\text{ to }\,X\,\text{ that factor through }\,U\}_\sim
$$

where the equivalence relation is

$$
  ((f \to U \to X) \sim (g \to U \to X))
  \Leftrightarrow
  (f\,\text{ and }\,g\,\text{ coincide as maps to }\,X)
  \,.
$$

So the set is just the set of maps from $V$ to $X$ that factor through one of the $U_\alpha$, which is precisely the set $F_S(V)$ assigned by the subfunctor corresponding to the sieve.
=--


### Sieves as covers

#### Introduction and overview

The following is a pedagogical step-by-step description of the crucial aspects of sieves as covers.


To start with the simplest example that already contains in it all the relevant aspects, consider a [[topological space]] $X$ with an open subset $V \subset X$ that is covered by two open subsets $U_1, U_2 \subset X$ in that the [[union]] $U_1 \cup U_2$ in $X$ coincides with $V$:

$$
  U_1 \cup U_2 = V
  \,.
$$

This is the [[coproduct]] in the [[category of open subsets]] of $X$, but that behaves very differently from the [[disjoint coproducts]] that we are used to from categories like [[Set]].  On the other hand, when one comes to a category of [[presheaves]] or [[sheaves]] (a [[Grothendieck topos]]), this [[topos]] *does* have disjoint coproducts.

Another way to think of this is obtained by first
forming the [[fiber product]] of $U_1$ with $U_2$ over $V$ in $Op(X)$,  which is the intersection $U_1 \cap U_2$ sitting in the [[pullback]] diagram

$$  
  \array{
    U_1 \times_V U_2 &\to& U_1
    \\
    \downarrow && \downarrow
    \\
    U_2 &\to& V
  }
$$

in $Op(X)$.

The union $U_1 \cup U_2$ is again obtained from this by removing in the above diagram the bottom right corner and then forming the [[pushout]] over the resulting diagram: this is again $V$, i.e. the diagram

$$  
  \array{
    U_1 \times_V U_2 &\to& U_1
    \\
    \downarrow && \downarrow
    \\
    U_2 &\to& U_1 \cup U_2 = V
  }
$$

is not only a [[pullback]] also a [[pushout]] diagram.

The important point about (covering) sieves is that they show up when the above situation is sent via the [[Yoneda embedding]] from $Op(X)$ to [[presheaf|presheaves]] on $Op(X)$. The crucial aspect here that gives rise to the peculiarities of sieves is that 

* the [[Yoneda embedding]] preserves [[limits]], but not, in general, [[colimits]]

As a result, the above discussion goes through equivalently for the [[presheaf|presheaves]] [[representable functor|represented]] by our open subsets all the way up to the last pushout. In $Op(X)$ that last pushout reproduced the open subset $V$. In $PSh(X) = [Op(X)^{op}, Set]$ it instead reproduces the _sieve_ on $V$ generated by $U_1$ and $U_2$.

Let's go through this in detail. First of all notice that in $PSh(X)$ all limits and colimits do exist (see [[limits and colimits by example]] for more on that); in particular the coproduct 

$$
  Y(U_1) \amalg Y(U_2)
$$

exists. Here $Y$ denotes the [[Yoneda embedding]] which we here indicate explicitly, even though often and elsewhere, notably elsewhere in this entry here, it is notationally suppressed.

For the following it is helpful to say explicitly what the presheaf $Y(U_1) \amalg Y(U_2)$ is like. Since, as described at [[limits and colimits by example]], colimits of presheaves are computed objectwise, we know that this presheaf evaluated on any open set $W \subset X$ yields the set

$$
  \begin{aligned}
   (Y(U_1) \amalg Y(U_2))(W) 
   &= 
    Y(U_1)(W) \amalg Y(U_2)(W)
   \\
   &=
   Hom(W,U_1) \amalg Hom(W, U_2)
  \end{aligned}
$$

where the coproducts on the right are just those in [[Set]] which are just ordinary disjoint unions of sets.

So this says that $Y(U_1) \amalg Y(U_2)$ is the presheaf that assigns to any open set $W$ the disjoint union of the collections of maps from $W$ to $U_1$ and those from $W$ to $U_2$ in $X$. (Since $Op(X)$ is a [[poset]] there is either none or one such map in each case, but it is helpful to speak generally of "sets of all maps", since that is the general intuition useful for presheaf categories. $Op(X)$ just happens to be a particularly simple example.)

Notice that in particular a given map $W \to V$ which factors both through $U_1 \to V$ as well as through $U_2 \to V$ will appear as two distinct elements in the set 
$(Y(U_1) \amalg Y(U_2))(W)$. This we'll come back to in a minute.

But first consider the fiber product from before, now after having applied the [[Yoneda embedding]]. Since we know from general nonsense that this preserves fiber products, we know that the [[pullback]] presheaf $Y(U_1) \times_{Y(V)} Y(U_2)$ in

$$
  \array{
   Y(U_1) \times_{Y(V)} Y(U_2) &\to& Y(U_2)
   \\
   \downarrow && \downarrow
   \\
   Y(U_1)
   &\to&
   Y(V)
  }
$$

is the same as $Y(U_1 \times_V U_2) = Y(U_1 \cap U_2)$.

But this is also easily checked explicitly. We go through this because this kind of reasoning for computing limits and colimits of presheaves will be needed throughout here: since for any $W$ the covariant [[hom-functor]] $Psh(Y(W),-) : Psh \to PSh$ preserves limits (by the very definition of [[limit]]!) we have for every $W$ a pullback diagram of sets

$$
 \array{
  Hom(Y(W),Y(U_1) \times_{Y(V)} Y(U_2))
   &\to& Hom(Y(W),Y(U_2))
  \\
  \downarrow && \downarrow
  \\
  Hom(Y(W),Y(U_1))
  &\to&
  Hom(Y(W),Y(V))
 }
$$

Again by the [[Yoneda lemma]] this is simply

$$
 \array{
  (Y(U_1) \times_{Y(V)} Y(U_2) )(W)
   &\to& 
   Hom(W,U_2)
  \\
  \downarrow && \downarrow
  \\
  Hom(W,U_1)
  &\to&
  Hom(W,V)
 }
  \,.
$$

This being a pullback diagram now says in words:

> The set $(Y(U_1) \times_{Y(V)} Y(U_2) )(W)$ is the set of those pairs of maps $W \to U_1$ and $W \to U_2$ that coincide as maps $W \to U_1 \to V$ and $W \to U_2 \to V$ to $V$.

Clearly, this set is the same as the set of maps into the intersection $U_1 \cap U_2$, so indeed

$$
  Y(U_1) \times_{Y(V)} Y(U_2) = Y(U_1 \times_V U_2)
  = Y(U_1 \cap U_2)
  \,.
$$

So far so long-winded. Now let's see what happens when we now form the pushout over

$$
  \array{
    Y(U_1 \times_V U_2) &\to& Y(U_2) 
    \\
    \downarrow
    \\
    Y(U_1)
  }
$$

that will go, for a moment, by its canonical but lengthy name
$
  Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2)
$

$$
  \array{
    Y(U_1 \times_V U_2) &\to& Y(U_2) 
    \\
    \downarrow && \downarrow
    \\
    Y(U_1)
    &\to&
    Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2)
  }
  \,.
$$

Again, we can figure out what this presheaf is by computing objectwise what it does to any open subset $W$: since colimits of presheaves are computed objectwise, the diagram

$$
  \array{
    Hom(W, U_1 \times_V U_2)
    &\to& 
    Hom(W, U_2) 
    \\
    \downarrow && \downarrow
    \\
    Hom(W,U_1)
    &\to&
    (Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2))(W)
  }
$$

must be a colimit in [[Set]]. Again, this is easily read
out in words:

> The set $(Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2))(W)$ is the quotient of the disjoint union of the collection of maps from $W$ into $U_1$ and those from $W$ into $U_2$, by the equivalence relation which identifies two such maps $W \to U_1$  and $W \to U_2$ if they both factor through a map $W \to U_1 \times_X U_2$, i.e. if they both land in the intersection $U_1 \cap U_2$ and coincide there.

But this just means that contrary to the plain coproduct $Y(U_1) \amalg Y(U_2)$, two maps $W \to U_1$ and $W \to U_2$ that coincide as maps $W \to X$ are no longer regarded as different elements of our set given by the pushout presheaf, but are regarded as being the same.

So this means we find that

$$
  (Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2))(W)
  =
  \{
    \text{ maps } \,W \to V \,\text{ that factor through either }\, U_1
    \,\text{ or }\, U_2
  \}
  \,.
$$

But this is by definition the assignment of the subfunctor corresponding to the sieve on $V$ generated by $U_1 \to V$ and $U_2 \to V$.

So we find that 

$$
  F_{sieve(U_1,U_2)}
  = 
  Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2)
  \,.
$$

Given that we made it to this point, we should go one small step further that will be very useful. 

In the present simple example we worked with a cover given by just two objects $U_1$ and $U_2$. Of course in general the cover will consist of more than just two objects. Then the above kind of notation becomes a bit cumbersome.  But there is a simple reformulation that makes everything look nice again.

Namely, let's come back to the observation that the coproduct $Y(U_1) \amalg Y(U_2)$ does exist. Let's just call this presheaf $\mathbf{U}$ (not in general a [[representable functor|representable]]!).

Then it is easy to see by the same kind of objectwise reasoning that the colimiting presheaf that we are after is equivalently the colimit over the pair of [[parallel morphisms]]

$$
  \mathbf{U} \times_{Y(V)} \mathbf{U}
  \stackrel{\stackrel{p_2}{\to}}{\stackrel{p_1}{\to}}
  \mathbf{U}
$$

in that

$$
  F_{sieve(U_1,U_2)} \simeq
  colim ( 
   \mathbf{U} \times_{Y(V)} \mathbf{U}
   \stackrel{\stackrel{p_2}{\to}}{\stackrel{p_1}{\to}}
   \mathbf{U}
  )
  \,.
$$

This description now has an evident direct generalization to the case where instead of just $U_1 \to V$ and $U_2 \to V$ we have an arbitrary collection $\{U_i \to V\}$ of open sets $U$ covering $V$. One finds again with 

$$
  \mathbf{U} := \coprod_i Y(U(i))
$$

that

$$
  F_{sieve(\{U_i\})} \simeq
  colim ( 
   \mathbf{U} \times_{Y(V)} \mathbf{U}
   \stackrel{\stackrel{p_2}{\to}}{\stackrel{p_1}{\to}}
   \mathbf{U}
  )
$$

is the presheaf that to every $W$ assigns the set of all maps $W \to V$ that factor through any one of the $U_i$.

It is in this way that sieves and their associated subfunctors encapsulate the notion of _cover_ of an object $V$: they tell us which of all the maps into $V$ do factor through the cover.

And, to end this pedagogical piece with an outlook to indicate the gain in understanding this achieves:

once we start forming $\mathbf{U} \times_{Y(V)} \mathbf{U} \stackrel{\to}{\to} \mathbf{U}$ there is no stopping. We can keep forming higher and higher such fiber products

$$
 \cdots
\mathbf{U} \times_{Y(V)} \mathbf{U}
 \times_{Y(V)} \mathbf{U}
 \times_{Y(V)} \mathbf{U}
\stackrel{\to}{\stackrel{\to}{\stackrel{\to}{\to}}}
\mathbf{U} \times_{Y(V)} \mathbf{U}
 \times_{Y(V)} \mathbf{U}
\stackrel{\to}{\stackrel{\to}{\to}}
\mathbf{U} \times_{Y(V)} \mathbf{U} \stackrel{\to}{\to} \mathbf{U}
  \,.
$$

When one passes from just presheaves to [[(∞,1)-presheaves]], then [[cover]]ing presheaves will be given by the right kind of colimit over these [[simplicial object|simplicial]] diagrams (namely the [[homotopy limit|homotopy colimit]]). More on that is at [[descent]].



#### The sheaf condition from morphisms out of a sieve

We now show that the subfunctor $F_S$ associated with a sieve $S$ coming from a cover $\{U_i \to X\}$ is the _right_ kind of morphism to require a [[sheaf]] to be a [[local object]] for, by demonstrating that using it the usual [[sheaf|sheaf condition]] on a presheaf with respect to the cover $\coprod_i U_i$ is reproduced:

From the above detailed discussion, recall that $F_{sieve(\{U_i\})}$ is precisely the [[coequalizer]] of the obvious pair of morphisms

$$
  \coprod_{i, j} \hom(-, U_i \cap U_j)
    \stackrel{\to}{\to}
  \coprod_i hom(-, U_i)
$$

with $hom(-, U_i) := Y(U_i)$ denoting the presheaf [[representable functor|represented]] under the [[Yoneda embedding]] by $U_i$, as usual.

Here the domain of this parallel pair is the [[pullback]] of the evident map
$\coprod_i hom(-, U_i) \to hom(-,X)$  
along itself, and the two parallel arrows are the projection maps out of this pullback:

$$
  \array{
     \coprod_{i,j} hom(-,U_i \cap U_j)
     &\to&
     \coprod_j hom(-, U_j)
     \\
     \downarrow && \downarrow
     \\
     \coprod_i hom(-, U_i)
     &\to&
     hom(-,X)
  }
$$
 
Thus for $G$ any [[presheaf]],
maps $F \to G$ are precisely the same as maps
$\coprod_i \hom(-, U_i) \to G$
which coequalize the parallel pair. Applying $Hom_{Set^{C^{op}}}(-,G)$ to the colimit diagram

$$
  \coprod_{i, j} \hom(-, U_i \cap U_j)
    \stackrel{\to}{\to}
  \coprod_i hom(-, U_i)
  \to
  F
$$
                     
yields the limit diagram

$$
  Hom(F, G)
  \to 
  Hom(\coprod_i hom(-, U_i), G)
  \stackrel{\to}{\to}
  Hom(\coprod_{i, j} \hom(-, U_i \cap U_j), G)
$$

which using [[Yoneda lemma|Yoneda]] is the equalizer diagram

$$
  Hom(F,G)
  \to
 \prod_i G(U_i) \stackrel{\to}{\to} \prod_{i, j} G(U_i \cap U_j)
$$

and hence identifies $Hom(F,G)$ indeed as the set of [[descent]] data for the [[sheaf]] condition on $G$. 




## Examples

* For $X$ a [[topological space]] let $Op(X)$ be the [[category of open subsets]] of $X$ and consider presheaves $PSh(X) := [Op(X)^{op}, Set]$ on $X$. For any open subset $c = V \in Op(X)$ let $\{d_i\} = \{U_i\}$ be a cover of $V$ by open subsets $U_i$ in the ordinary sense (i.e. each $U_i$ is an open subset of $V$ and their joint union is $V$, $\bigcup_i U_i = V$), then  $\pi : (\coprod_i Y(U_i)) \stackrel{\coprod_i U_i \hookrightarrow_i X}{\to} Y(V)$ (with $Y$ the [[Yoneda embedding]]) is a [[local epimorphism]] of presheaves on $V$ and its [[image]] -- or equivalently its [[coimage]] -- is the subfunctor $(F := \bigcup_i Y(U_i)) \hookrightarrow Y(V)$ that sends each $W \in Op(X)$ to the set of maps $W \to V$ that factor through one of the $U_i$. The collection of all such maps for all choice of $W$ is the corresponding _covering sieve_ $\{ f : W \to V  \in Mor(S) \;|\; f = W \to U_i \to V  \}$.

* The situation for more general [[sites]] $S$ other than $Op(X)$ is literally the same as above, with $U_i, W, V$ etc. objects of $S$.


## References

A standard textbook account on sieves in [[category theory]] is in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_.

In the context of [[(∞,1)-categories]] sieves are discussed around def. 6.2.2.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}





[[!redirects sieves]]

