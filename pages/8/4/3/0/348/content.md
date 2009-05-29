#Idea#

A _sieve_ is a way to encode a morphism of [[presheaf|presheaves]] that behaves like a [[cover]]. It is used to say which [[presheaf|presheaves]] are actually [[sheaf|sheaves]] with respect to a given [[coverage]] or [[Grothendieck topology]].

_Sieves_ are an equivalent way to encode [[subobject]]s of [[representable functor]]s in a [[presheaf]] category in terms of the total sets of _elements_ of such a subfunctor.

The notion of _sieve_ is usually used when certain such subobjects are singled out as [[cover]]s of a [[Grothendieck topology]]: the singled out subobjects then correspond to _covering sieves_.

+-- {: .query}
Urs, I changed 'coverage' back to 'Grothendieck topology' above, since it\'s specifically Grothendieck topologies that deal with covering sieves; coverages deal with arbitrary covering families (generally not sieves and generally not all of them), which is part of why coverages both can be more useful and are less canonical.

[[Urs Schreiber|Urs]]: hm, okay. My impression was that the point of coverages is that we don't impose the four axioms of Grothendieck topology on the covering things, while we do keep the notion of sieves itself. Because "sieve" is really just another way to say "subfunctor of a representable" so the question really is: which collections of subfunctors of representables do we want to use as coverages.  For me the 1-line definition of "coverage" would be: choice of subcollection of all monois in a given 1-topos. That then makes sense also in non-presheaf topoi. For presheaf topoi it happens to have a reformulation in terms of sieves.

So, in conclusion, I am thinking that the point of using more general coverages over Grothendieck topologies is not primarily to relax the closure under composition that makes a sieve a sieve. That's kind of a trivial thing. The point is that we don't need to impose the four axioms of a Grothendieck topology on the collection of all such.

But maybe not. This is just so you know what I am thinking. :-)

=--

A choice of collections of morphism $d \to c$ into an object $c \in C$  for each $d \in C$ reminds one of the [[representable functor]] [[presheaf]]
$Y(c) := \hom_C(-, c): C^{op} \to Set$ which assigns to each $d \in C$ the set of _all_ morphisms from $d$ to $c$. Every choice of covers of $c$ is therefore for each $d \in C$ a subset of the value of this functor evaluated at $d$. This begins to look like an [[monomorphism|monic]] [[natural transformation]] into this functor. Indeed, it turns out that one can assume without restriction of generality that the assignment of covers of $c$ can always be extended to such a monic natural transformation, and hence one formalizes the notion of "collection of covers" of $c$ as a [[subobject]] $i: F \hookrightarrow \hom(-, c)$ of the functor represented by $c$: a _sieve_ at $c$. 


#Definition#

Let $C$ be a [[small category]].

+-- {: .un_defn}
###### Definition

A _sieve_ $S$ (Fr. _crible_) on an object $c \in C$ is a subset $S \subset Ob(C/c)$ of the set of objects of the [[over category]] over $c$ which is _closed under precomposition_:  it has the property that with $(d \to c) \in S$ for every morphism $(e \to d) \in Mor(C)$ also the composite $(e \to d \to c)$ is in $S$.
=--

Sometimes the condition of a sieve being closed under the operation of precomposing with an arbitrary morphism $g: e \to d$ is called a "saturation condition". Given any collection of morphisms targeted at $c$, one can always close it up or saturate it, to obtain a sieve on $c$. 

+-- {: .query}
_Bruce_: Perhaps say here: "It is called a _sieve_ because it "sieves out" the 'special' maps into $c$ from the set of _all_ maps into $c$.
=--


# Relation to subfunctors #

There is a canonical way to create subfunctors from sieves and sieves from subfunctors.

+-- {: .query}
_Bruce_: What is a subfunctor? Can you link that word to a page?
=--

A subfunctor is a [[subobject]] in a [[functor category]]. Here, specifically, one is interested in [[subobject]]s in a [[presheaf]] category of [[representable functor]]s. It's these subfunctors of representable functors that are in bijection with sieves.

+-- {: .un_defn}
###### Definition

Given a sieve $S$ on $c$, the **subfunctor** $F_S \hookrightarrow Y(c)$ **defined by the sieve**  is the [[presheaf]] 

* that assigs to each object $d \in C$ the set $F_S(d) = \{(d \to c) \in S\}$;

* that assigns to each morphism $(d \to d') \in C$ the function $F_S(d') \to F_S(d)$ induced on elements by precomposition with $d \to d'$.
=--

+-- {: .un_defn}
###### Definition

Given a subfunctor $F \hookrightarrow Y(c)$, the **sieve defined by the subfunctor** is given by

* $S_F := \{g: d \to c \in Mor(C) | Y(d) \stackrel{Y(g)}\to Y(c) = Y(d)  \to F \to Y(c) \}$

or equivalently

* $S_F = \coprod_{d \in Obj(C)}F(d)$.
=--

+-- {: .query}
_Bruce_: Hey, if you are being extra careful here you should be saying that the sieve $S_F$ obtained from the subfunctor $F \hookrightarrow Y(c)$ is really the _image_ of $F$ (as you say below), i.e. if we write $i: F \hookrightarrow Y(c)$ for the explicit inclusion map, then for each $d$, $S_F(d) = Image of i_d in Hom(d,c)$. 

Right now, this makes me _prefer_ the notion of 'sieve' to the notion of 'subfunctor of a representable'. The reason is that the elements of the sieve are actually morphisms in the category, whereas the subfunctor can be composed of 'abstract elements'. Why are you pushing the viewpoint of 'subfunctor of a representable'? Is it for later $\infty$-category purposes? If so, you should say that at the top of the article, so the reader understands why you are introducing extraneous 'abstract nonsense' elements into the conversation... :-)
=--

 {: .un_lemma}
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


+-- {: .un_remark}
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

+-- {: .un_lemma}
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
    colim( Hom(V,U) \times_{Hom(U,X)} Hom(V,U)  \stackrel{\to}{\to} Hom(V,U))
  \end{aligned}
$$

where all objects appearing (at least in the first lines) are implicitly regarded as presheaves under the [[Yoneda embedding]].

But this colimit now manifestly computes the set

$$
  \{ maps from V to X that factor through U\}_\sim
$$

where the equivalence relation is

$$
  ((f \to U \to X) \sim (g \to U \to X))
  \Leftrightarrow
  (f and g coincide as maps to X)
  \,.
$$

So the set is just the set of maps from $V$ to $X$ that factor through one of the $U_\alpha$, which is precisely the set $F_S(V)$ assigned by the subfunctor corresponding to the sieve.
=--




#Examples#

* For $X$ a [[topological space]] let $Op(X)$ be the [[category of open subsets]] of $X$ and consider presheaves $PSh(X) := [Op(X)^{op}, Set]$ on $X$. For any open subset $c = V \in Op(X)$ let $\{d_i\} = \{U_i\}$ be a cover of $V$ by open subsets $U_i$ in the ordinary sense (i.e. each $U_i$ is an open subset of $V$ and their joint union is $V$, $\bigcup_i U_i = V$), then  $\pi : (\coprod_i Y(U_i)) \stackrel{\coprod_i U_i \hookrightarrow_i X}{\to} Y(V)$ (with $Y$ the [[Yoneda embedding]]) is a [[local epimorphism]] of presheaves on $V$ and its [[image]] -- or equivalently its [[coimage]] -- is the subfunctor $(F := \bigcup_i Y(U_i)) \hookrightarrow Y(V)$ that sends each $W \in Op(X)$ to the set of maps $W \to V$ that factor through one of the $U_i$. The collection of all such maps for all choice of $W$ is the corresponding _covering sieve_ $\{ f : W \to V  \in Mor(S) \;|\; f = W \to U_i \to V  \}$.

* The situation for more general [[site]]s $S$ other than $Op(X)$ is literally the same as above, with $U_i, W, V$ etc. objects of $S$.




## A detailed description of what's going on ##

The followig is a pedagogical step-by-step description of the crucial aspects of sieves as covers.


To start with the simplest example that already contains in it all the relevant aspects, consider a [[topological space]] $X$ with an open subset $V \subset X$ that is covered by two open subsets $U_1, U_2 \subset X$ in that the union $U_1 \cup U_2$ in $X$ coincides with $V$:

$$
  U_1 \cup U_2 = V
  \,.
$$

Notice the distincion between this union in of the two open subsets in $X$, and the potential notion of _disjoint union_ $U_1 \sqcup U_2$ interpreted as the [[coproduct]] of $U_1$ and $U_2$ in some category. If that category is the naive choice in that we regard all open sets here as objects in the [[category of open subsets]] $Op(X)$ of $X$, then this coproduct does not even exist in general! (It does exist if $U_1$ and $U_2$ are disjoint in $X$.)

What does exist in $Op(X)$ is the [[fiber product]] of $U_1$ with $U_2$ over $V$: this is the intersection $U_1 \cap U_2$ sitting in the [[pullback]] diagram

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

The union $U_1 \cup U_2$ can be obtained from this by removing in the above diagram the bottom right corner and then forming the [[pushout]] over the resulting diagram: this is again $V$, i.e. the diagram

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

* the [[Yoneda embedding]] preserves [[limit]]s, but not, in general, [[colimit]]s

As a result, the above discussion goes through equivalently for the [[presheaf|presheaves]] [[representable functor|represented]] by our open subsets all the way up to the last pushout. In $Op(X)$ that last pushout reproduced the open subset $V$. In $PSh(X) = [Op(X)^{op}, Set]$ it instead reproduces the _sieve_ on $V$ generated by $U_1$ and $U_2$.

Let's go through this in detail. First of all notice that in $PSh(S)$ all limits and colimits do exist (see [[limits and colimits by example]] for more on that), so that for instance the coproduct 

$$
  Y(U_1) \sqcup Y(U_2)
$$

does always exist (as opposed to its would-be cousin $U_1 \sqcup U_2$). Here $Y$ denotes the [[Yoneda embedding]] which we here indicate explicitly, even though often and elsewhere, notably elsewhere in this entry here, it is notationally suppressed.

For the following it is helpful to say explicitly what the presheaf $Y(U_1) \sqcup Y(U_2)$ is like. Since, as described at [[limits and colimits by example]], colimits of presheaves are computed objectwise, we know that this presheaf evaluated on any open set $W \subset X$ yields the set

$$
  \begin{aligned}
   (Y(U_1) \sqcup Y(U_2))(W) 
   &= 
    Y(U_1)(W) \sqcup Y(U_2)(W)
   \\
   &=
   Hom(W,U_1) \sqcup Hom(W, U_2)
  \end{aligned}
  \,,
$$

where the coproducts on the right are just those in [[Set]] which are just ordinary disjoint unions of sets.

So this says that $Y(U_1) \sqcup Y(U_2)$ is the presheaf that assigns to any open set $W$ the dijoint union of the collections of maps from $W$ to $U_1$ and those from $W$ to $U_2$ in $X$. (Since $Op(X)$ is a [[poset]] there is either none or one such map in each case, but it is helpful to speak generally of "sets of all maps", since that is the general intuition useful for presheaf categories. $Op(X)$ just happens to be a particularly simple example.)

Notice that in particular a given map $W \to V$ which factors both through $U_1 \to V$ as well as through $U_2 \to V$ will appear as two distinct elements in the set 
$(Y(U_1) \sqcup Y(U_2))(W)$. This we'll come back to in a minute.

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

that will go, for a moment, by its canonical but lenghty name
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

But this just means that contrary to the plain coproduct $Y(U_1) \sqcup Y(U_2)$, two maps $W \to U_1$ and $W \to U_2$ that coincide as maps $W \to X$ are no longer regarded as different elements of our set given by the pushout presheaf, but are regarded as being the same.

So this means we find that

$$
  (Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2))(W)
  =
  \{
    maps W \to V that factor through either U_1
    or U_2
  \}
  \,.
$$

But this is by definition the assignment of the subfunctor coresponding to the sieve on $V$ generated by $U_1 \to V$ and $U_2 \to V$.

So we find that 

$$
  F_{sieve(U_1,U_2)}
  = 
  Y(U_1) \coprod_{Y(U_1 \times_V U_2)} Y(U_2)
  \,.
$$

Given that we made it to this point, we should go one small step further that will be very useful. 

In the present simple example we worked with a cover given by just two objects $U_1$ and $U_2$. Of course in general the cover will consist of more than just two objects. Then the above kind of notation becomes a bit cumbersome.  But there is a simple reformulation that makes everything look nice again.

Namely, let's come back to the observation that the coproduct $Y(U_1) \sqcup Y(U_2)$ does exist. Let's just call this presheaf $\mathbf{U}$. (not in general a [[representable functor|representable]]!).

Then it is easy to see by the same kind of objectwise reasoning that the colimiting presheaf that we are after is equivalently the colimit over the pair of [[parallel morphism]]s

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

It is in this way that sieves and their associated subfunctors encode the notion of _cover_ of an object $V$: they tell us which of all the maps into $V$ do factor through the cover.

And, to end this pedagocial piece with an outlook to indicate the gain in understanding this achieves:

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

When one passes from just presheaves to [[(infinity,1)-presheaf|(infinity,1)-presheaves]], then [[cover]]ing presheaves will be given by the right kind of colimit over these [[simplicial object|simplicial]] diagrams (namely the [[homotopy limit|homotopy colimit]]). More on that is at [[descent]].



# Recovering the sheaf condition from morphisms out of the sieve#

We now show that the subfunctor $F_S$ associated with a sieve $S$ coming from a cover $\{U_i \to X\}$ is the _right_ kind of morphism to require a [[sheaf]] to be a [[local object]] for, by demonstrating that using it the usual [[sheaf|sheaf condition]] on a presheaf with respect to the cover $\coprod_i U_i$ is reproduced:

From the above detailed discuss recall that $F_{sieve(\{U_i\})}$ is precisely the [[coequalizer]] of the obvious pair of morphisms

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
     \coprod_i hom(-, U_j)
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

# Interpretation in terms of higher descent and codescent #


This description contains in it the seed of its generalization from the context of [[sheaf|sheaves]] to that of [[descent]] for [[infinity-stack]]s: 

for $Y := \coprod_i U_i$ a cover, there is a [[simplicial presheaf]] $ Y_\bullet $ that in degree $n$ is the $(n+1)$-fold [[fiber product]] $Y_n = Y^{[n+1]} = Y \times_X Y \times_X \cdots \times_X Y$.

This may be regarded as an [[infinity-groupoid]] valued presheaf.

More algebraically, with $\Pi(\Delta^n)$ the free [[strict omega-groupoid]] on the standard filtered $n$-[[simplex]], $Y_\bullet$ is the [[nerve]] of the groupoid

$$
  Codesc(Y) := \int^{[n] \in \Delta} O([n])\cdot Y^{[n+1]}
$$

The sieve associated with the cover is the presheaf obtained by starting with the $\infty$-prestack represented by $Codesc(Y)$ and decategorifying, i.e. passing to equivalence classes.

$$
  \bigcup_i hom(-,U_i)
  \simeq
  hom(-, Codesc(Y))/_\sim
  \,.
$$


Equivalently, for $A$ a [[presheaf]] regarded as a constant [[simplicial presheaf]] using the inclusion $const : $ [[Set]] $\hookrightarrow$ [[SSet]] we have

$$
  Hom_{SPSh}(Codesc(Y), A) \simeq Hom_{PSh}(Codesc(Y)/_\sim, A)
  \,,
$$

simply because all the higher morphism of $Codesc(Y)$ have to map to identity morphisms in $A$.