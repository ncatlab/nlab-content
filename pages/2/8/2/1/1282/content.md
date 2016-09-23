
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

This entry lists and discusses examples and special types of [[limit]]s and [[colimit]]s, hence also in particular of [[product]]s and [[coproduct]]s. 

It starts with very elementary and simple examples and eventually passes to more sophisticated ones.

For examples of the other [[universal construction]]s see

* [[examples of adjoint functors]]

* [[examples of Kan extensions]]

# Contents
* table of contents
{: toc}

## Limits and colimits in Set {#limcoliminset}

In the [[category]] [[Set]] of [[set]]s, [[limit]]s and [[colimit]]s reduce to the very familiar operations of 

* [[cartesian product]] of sets
* [[disjoint union]] of sets
* [[subset]]s defined by equations
* [[quotient set]]s of equivalence classes.

### Terminal object
The [[terminal object]] is the limit of the empty functor $F: \emptyset \to Set$. So a [[terminal object]] of $Set$ is a set $X$ such that there is a unqiue function from any set to $X$. This is given by any [[singleton]] set $\{a\}$, where the unique function $Y \to \{a\}$ from any set $Y$ is the function that sends every element in $Y$ to $a$.

### Initial object
(...)

### Product
Given two sets $A, B$, the categorical [[product]] is the usual product of sets, which can be constructed as the set of [[Kuratowski pairs]]
$$
  A \times B = \{ \{\{a\}, \{a, b\}: a \in A, b \in B\}.
$$
We write $(a, b) = \{\{a\}, \{a, b\}\}$.

The projection maps $\pi_1: A \times B \to A$ and $\pi_2: A \times B \to B$ are given by
$$
  \pi_1(a, b) = a, \pi_2(a, b) = b.
$$

To see this satisfies the universal property of products, given any pair of maps $f: X \to A$ and $g: X \to B$, we obtain a map $(f, g): X \to A \times B$ given by
$$
  (f, g)(x) = (f(x), g(x)).
$$

### Coproduct
(...)

### Equalizer
Given a diagram
$$
\array{
X & \underset{g}{\overset{f}{\rightrightarrows}} & Y
},
$$
the limit of the diagram is the [[equalizer]] of the two arrows, is given by
$$
  \{x \in X: f(x) = g(x)\}.
$$
(.. explanation of construction ..)

### Coequalizer
(...)

### Pullback
The limit of a diagram of the form
$$
\array{
  & & A\\
  & & \downarrow^\mathrlap{f}\\
  B & \underset{g}{\to} & C
}
$$
is also known as the [[pullback]], given by
$$
  \{(a, b) \in A \times B: f(a) = g(b)\},
$$
with the maps to $A$ and $B$ given by the projections.

While the definition of a pullback is symmetric in $f$ and $g$, it is usually convenient to think of this as pulling back $f$ along $g$ (or the other way round). This has more natural interpretations in certain special cases.

If $g: B \to C$ is the inclusion of a subset (ie. is a [[monomorphism]]), then the pullback of $f$ along $g$ is given by
$$
  \{a \in A: g(a) \in B\}.
$$
So this is given by restricting $f$ to the elements that are mapped into $B$.

Alternatively, we can view the map $f: A \to C$ as a collection of sets indexed by elements of $C$, where the set indexed by $c \in C$ is given by $A_c = f^{-1}(c)$. Under this interpretation, pulling $f$ back along $g$ gives a collection of sets indexed by elements of $B$, where the set indexed by $b \in B$ is given b $A_{g(b)}$.

### Pushout
(...)

### General limits
The limit over a [[Set]]-valued functor $F : D^{op} \to Set$ is a subset of the product $\prod_{d \in Obj(d)} F(d)$ of all objects:
$$
  lim F = \left\{ (s_d)_d \in \prod_d F(d) | \forall (d \stackrel{f}{\to} d') : F(f)(s_{d}) = s_{d'}  \right\}.
$$

Abstractly, the limit can be described as follows:

  * the limit over any $F : D \to Set$ is the set of [[natural transformations]] from the diagram constant on the [[point]] to $F$, ie.
$$
  lim F = [D, Set](const_{pt}, F).
$$

  * This is equivalently the set of [[global elements]] of $F$.

  * Therefore for every set $X$, there is a natural bijection $Set(X, lim F) \simeq lim Set(X,F(-))$, where on the right the limit is taken of the functor $Set(X,F(-)) : D \to Set$.

### General colimits
The colimit over a [[nLab:Set|Set]]-valued functor $F : D \to Set$ is a quotient set of the disjoint union $\coprod_{d \in Obj(D)} D(d)$: 
  $$ 
    colim F \simeq (\coprod_{d\in D} F(d))/_\sim \,, 
  $$
  where the equivalence relation $\sim$ is that which is _generated_ by 
  $$
    ((x \in F(d)) \sim (x' \in F(d')))\quad if \quad (\exists (f : d \to d') with F(f)(x) = x')
  \,.
  $$
  If $D$ is a [[filtered category]] then the relation $\sim$ already is an equivalence relation.

## Limits and Colimits in Grp
(..)

## Limits and Colimits in Top
(..)

## Limits and Colimits in a preordered set
(..)

## Limits and Colimits in functor categories
(..)

#Examples of limits {#examplesoflimits}

In the following examples, $D$ is a [[small category]], $C$ is any category and the limit is taken over a functor $F : D^{op} \to C$.

## Simple diagrams {#limitssimplediagrams}


* the limit of the empty diagram $D = \emptyset$ in $C$ is, if it exists [[nLab:generalized the|the]] [[nLab:terminal object|terminal object]];

* if $D$ is a [[nLab:discrete category|discrete category]], i.e. a category with only identity morphisms, then a diagram $F : D \to C$ is just a collection $c_i$ of objects of $C$. Its limit is the [[nLab:product|product]] $\prod_i c_i$  of these.

* if $D = \{a \stackrel{\to}{\to} b\}$ then $lim F$ is the [[nLab:equalizer|equalizer]] of the two morphisms $F(b) \to F(a)$.

* if $D$ has an [[nLab:terminal object|terminal object]] $I$ (so that $I$ is an [[nLab:initial object|initial object]] in $D^{op}$), then the limit of any $F : D^{op} \to C$ is $F(I)$.

## Filtered limits {#filteredlimits}

* if $D$ is a [[nLab:poset|poset]], then the limit over $D^{op}$ is the supremum over the $F(d)$ with respect to $(F(d) \leq F(d')) \Leftrightarrow (F(d) \stackrel{F(\leq)}{\leftarrow} F(d'))$;

* the generalization of this is where the term "limit" for categorical limit (probably) originates from: for $D$ a [[nLab:filtered category|filtered category]], hence $D^{op}$ a cofiltered category, one may think of $(d \stackrel{f}{\to} d') \mapsto (F(d) \stackrel{F(f)}{\leftarrow} F(d')$ as witnessing that $F(d')$ is "larger than" $F(d)$ in some sense, and $lim F$ is then the "largest" of all these objects, the limiting object. This interpretation is perhaps more evident for filtered [[nLab:colimit|colimits]], where the codomain category $C$ is thought of as being the [[nLab:opposite category|opposite]] $C = E^{op}$. See the motivation at [[nLab:ind-object|ind-object]].

## In terms of other operations {#limitsintermsofotherops}

If products and equalizers exist in $C$, then limit of $F : D^{op} \to C$ can be exhibited as a [[nLab:subobject|subobject]] of the [[nLab:product|product]] of the $F(d)$, namely the [[nLab:equalizer|equalizer]] of

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\langle F(f) \circ p_{F(t(f))} \rangle_{f \in Mor(D)} }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))
$$

and

$$
  \prod_{d \in Obj(D)}
  F(d)
  \stackrel{\langle p_{F(s(f))} \rangle_{f \in Mor(D)} }{\to}  
  \prod_{f \in Mor(D)}
  F(s(f))  
  \,.
$$

See the explicit formula for the limit in [[nLab:Set|Set]]
in terms of a subset of a product set.


In particular therefore, a category has all limits already if it has all products and equalizers.



### Limits in presheaf categories {#limitsinpresheafcat}

Consider limits of functors $F : D^{op} \to PSh(C)$
with values in the category of [[nLab:presheaf|presheaves]] on a [[nLab:small category|small category]] $C$.

+-- {: .num_prop #LimitsOfPresheaves}
###### Proposition

Limits of presheaves are computed objectwise:
$$
  lim F : c \mapsto lim F(-)(c)
$$ 
Here on the right the limit is over the functor 
$F(-)(c) : D^{op} \to Set$.

Similarly for colimits

=--

Similarly [[colimit]]s of presheaves are computed objectwise.

+-- {: .num_prop}
###### Proposition

The [[Yoneda embedding]] 
$Y : C \to PSh(C)$ commutes with small limits:

Let $F : D^{op} \to C$, then we have
$$
  Y(lim F) \simeq lim (Y\circ F)
$$
if $lim F$ exists.

=--

**Warning** The Yoneda embedding does _not_ in general preserve colimits.

## Limits in under-categories {#limitsinundercat}

Limits in [[under category|under categories]] are a special case of limits in [[comma category|comma categories]]. These are explained elsewhere. It may still be useful to spell out some details for the special case of under-categories. This is what the following does.


+-- {: .num_prop}
###### Proposition

Limits in an [[under category]] are computed as limits in the underlying category.

Precisely: let $C$ be a [[category]], $t \in C$ an [[object]], and $t/C$ the corresponding [[under category]], and $p : t/C \to C$ the obvious projection.

Let $F : D \to t/C$ be any [[functor]]. Then, if it exists, the [[limit]] over $p \circ F$ in $C$ is the image under $p$ of the limit over $F$:

$$
  p(\lim F)  \simeq \lim (p F)
$$

and $\lim F$ is uniquely characterized by $\lim (p F)$.


=--
 
+-- {: .proof}
###### Proof

Over a morphism $\gamma : d \to d'$ in $D$ the limiting cone over $p F$  (which exists by assumption) looks like

$$
  \array{
    && \lim p F
    \\
    & \swarrow && \searrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


By the universal property of the limit this has a unique
lift to a cone in the [[under category]] $t/C$ over $F$:

$$
  \array{
    && t 
    \\
    & \swarrow &\downarrow & \searrow
    \\
    && \lim p F
    \\
    \downarrow & \swarrow && \searrow & \downarrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


It therefore remains to show that this is indeed a limiting cone over $F$. Again, this is immediate from the universal property of the limit in $C$. For let $t \to Q$ be another cone over $F$ in $t/C$, then $Q$ is another cone over $p F$ in $C$ and we get in $C$ a universal morphism $Q \to \lim p F$

$$
  \array{
    && t
    \\
    & \swarrow & \downarrow & \searrow
    \\
    && Q
    \\
    \downarrow & \swarrow &\downarrow & \searrow & \downarrow
    \\
    && \lim p F
    \\
    \downarrow & \swarrow && \searrow & \downarrow
    \\
    p F(d) &&\stackrel{p F(\gamma)}{\to}&& p F(d') 
  }
$$


A glance at the diagram above shows that
the composite $t \to Q \to \lim p F$ constitutes a morphism
of cones in $C$ into the limiting cone over $p F$. Hence it must equal our morphism $t \to \lim p F$, by the universal property of $\lim p F$, and hence the above diagram does commute as indicated.

This shows that the morphism $Q \to \lim p F$
which was the unique one giving a cone morphism on $C$ does lift to a
cone morphism in $t/C$, which is then necessarily unique, too.  This demonstrates the required universal property of $t \to \lim p F$ and 
thus identifies it with $\lim F$.


=--

* Remark: One often says "$p$ reflects limits" to express the conclusion of this proposition. A conceptual way to consider this result is by appeal to a more general one: if $U: A \to C$ is [[monadic functor|monadic]] (i.e., has a left adjoint $F$ such that the canonical comparison functor $A \to (U F)-Alg$ is an equivalence), then $U$ both reflects and preserves limits. In the present case, the projection $p: A = t/C \to C$ is monadic, is essentially the category of algebras for the monad $T(-) = t + (-)$, at least if $C$ admits binary coproducts. (Added later: the proof is even simpler: if $U: A \to C$ is the underlying functor for the category of algebras of an _endofunctor_ on $C$ (as opposed to algebras of a monad), then $U$ reflects and preserves limits; then apply this to the endofunctor $T$ above.) 










# Further resources #

Pedagogical vidoes that explain limits and colimits are at

* [[The Catsters]], [General Limits and Colimits](http://www.youtube.com/watch?v=g47V6qxKQNU)

A web-based program that generates componentwise illustrations of simple [[limit]]s and [[colimit]]s in [[Set]] is developed at

* J. Paine, [Category Theory Demonstrations](http://www.j-paine.org/cgi-bin/webcats/webcats.php)

More on the inner workings of this program is at [[Paine on a Category Theory Demonstrations program]]



#Discussion#

+--{.query}

>the following discussion originated from an earler version of this entry

[[Todd Trimble]]: So far, this is a really good article. However, I would not say in this last line "if either limit exists", because small limits on the right certainly exist always since $Set$ is complete; instead, "if $lim F$ exists". 

[[Urs Schreiber|Urs]]: thanks, Todd, I have changed the above now accordingly. Please don't hesitate to correct and/or improve things you see as needed.

By the way, I am not completely happy with this entry as yet. It was originally motivated from the desire to 
_explain_ in small steps the computation of limits and colimits to those readers unfamiliar with it. Currently this here mostly just lists results, where maybe we would eventually want to include also pedagocial proofs. 

The material below "explanation for programmers" goes more in that pedagogical direction, though I'd think eventually it would be good to also have the kind of pedestrian explanation given there but without (at first) its realization in Python! :-)

=--


+--{.query}

>an earlier version of this entry, which contained the material now branched off at [[Paine on a Category Theory Demonstrations program]], led to the following discussion

[[Urs Schreiber]]: sorry to say this, but I am not so happy with the following material here at this particular entry. This entry here is supposed to explain limits and colimits. Originally I thought that the computer program described below should be _used_ here to _help explain_ limits and colimits. For instance by using its graphical output for illustration purposes. But instead the material below explains how to _write that program_ . That may be of interest, too, but here at this entry it seems a bit of a distraction. Could we move the following material to its seperate entry? 

_Toby_:  I would agree that the material on how to write the program would work well in a separate entry, say [[programming coproducts]].  On the other hand, you definitely want to keep the first two lines here; they do just what you want and could be expanded on here.

=--

