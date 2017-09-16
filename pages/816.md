#Idea#

The notion of _weighted limit_ is naturally understood from the point of view on [[limit]]s as described at [[representable functor]].

Weighted limits make sense and are considered in the general context of $V$-[[enriched category theory]], but restrict attention to $V=$ [[Set]] for the moment, in order to motivate the concept.

Let $K$ denote the small category which indexes [[diagram]]s over which we want to consider limits and eventually weighted limits. Notice that for 

$$
  F : K \to Set
$$

a [[Set]]-valued functor on $K$, the limit of $F$ is canonically identified simply with the set of [[cone]]s with tip the singleton set $pt = \{\bullet\}$:

$$
  lim F = [K,Set](\Delta pt, F)
  \,.
$$

This means, more generally, that for 

$$
  F : K \to C
$$

a functor with values in an arbitrary category $C$, the object-wise limit of the functor $F$ under the [[Yoneda embedding]]

$$
  C(-,F(-)) : K \stackrel{F}{\to} C \stackrel{Y}{\to} Set^{C^{op}}
$$

which appears in the discussion in example 1 at [[representable functor]] can be expressed by the right side of

$$
  lim C(-,F(-)) = [K,Set](\Delta pt, C(-,F(-)))
  \,.
$$

(Recall that this is the limit over the diagram $C(-,F(-)) : K \to Set^{C^{op}}$ which, if [[representable functor|representable]] defines the desired limit of $F$.)

The **idea** of weighted limits is to 

1. allow in the formula above the particular functor $\Delta pt$ to be replaced by any other functor $W : K \to Set$;

2. to generalize everything straightforwardly from the [[Set]]-[[enriched category|enriched]] context to arbitrary $V$-enriched contexts.

Heuristically, the weight $W : K \to V$ encodes the way in which one generalizes the concept of a [[cone]] over a diagram $F$ from something with just a tip from which morphisms are emanating down to $F$ to a more intricate structure over the diagram $F$. For instance in the application to [[homotopy limit]]s discussed below with $V = $[[SSet]] the weight is such that it ensures that not only 1-morphisms are emanating from the tip, but that any triangle formed by these is filled by a 2-cell, every tetrahedron by a 3-cell, etc.

#Definition#

Let $V$ be a [[closed category|closed]] [[symmetric monoidal category]]. All categories in the following are $V$-[[enriched category|enriched categories]], all functors are $V$-functors.

A **weighted limit** over a functor

$$
  F : K \to C
$$

with respect to a _weight_ or _indexing type_ functor

$$
  W : K \to V
$$

is, if it exists, the object $lim^W F \in V$ which [[representable functor|represents]] the functor

$$
  [K,V](W, C(-,F(-))) : C^{op} \to V
  \,,
$$

i.e. such that for all objects $c \in C$ 
there is an isomorphism

$$
  C(c, lim^W F)
  \simeq
  [K,V](W(-), C(c,F(-)))
$$

natural in $c$.


#Examples#

##Homotopy limits##

For $V$ some category of higher structures, the _local_ definition of [[homotopy limit]] over a diagram $F : K \to C$ replaces the ordinary notion of [[cone]] over $F$ by a higher cone in which all triangles of 1-morphisms are filled by 2-cells, all tetrahedra by 3-cells, etc. 

One can convince oneself that for the choise $V =$ [[SSet]] this is realized in terms of the weighted limit $lim^W F$ with the weight $W$ taken to be

$$
  W : K \to SSet
$$
$$
  W : k \mapsto N(K/k)
   \,,
$$

where $K/k$ denotes the [[over category]] of $K$ over $k$ and $N(K/k)$ denotes its [[nerve]].


#References#

A standard reference is

* M. Kelly, _Basic concepts of enriched category theory_, [section 3.1, p. 37](http://www.emis.de/journals/TAC/reprints/articles/10/tr10.pdf#page=37)

In 

* E. Riehl, _Weighted limits and colimits_ (2008) ([pdf](http://www.math.uchicago.edu/~eriehl/cat/weighted.pdf))

[[Emily Riehl]] gives an account of lectures by [[Mike Shulman]] on the subject. The definition appears there as [definition 3.1, p. 4](http://www.math.uchicago.edu/~eriehl/cat/weighted.pdf#page=4) (in a form a bit more general than the one above).



***

#Discussion#


A previous version of this entry came with the following discussion.

+-- {: .query}

 [[Urs Schreiber|Urs]]: I'd like to better understand the relation between weighted limits and [[homotopy limit]]s. 

Suppose I am considering enrichment in $V =$ [[SSet]]. Then how wrong is the following idea for encoding homotopy limits in terms of weighted limits:

let $K$ be an ordinary small category and $F : K \to SSet$ a functor which happens to take values in Kan complexes, for definiteness. Now let the weight functor be given by

$$
  W : K \to SSet
$$
$$
  W : k \mapsto N(K/k)
  \,,
$$

where $K/k$ is the [[over category]] of $K$ over $k \in K$ and $N(-)$ is the [[nerve]]. I am thinking that the $W$-weighted limit $lim^W F$ might be a reasonable way to encode a homotopy coherent limit over $F$. How wrong is this? If not so wrong, this will have been discussed somewhere. Where?

[[Mike Shulman|Mike]]: That's exactly right (modulo fibrancy/cofibrancy conditions if there is a model structure hanging around).  This is a very classical way of defining homotopy limits, see Bousfield-Kan or Hirschhorn's book.  It's also mentioned in my own paper on homotopy limits.  Note that $N(K/k)$ can also be identified with the [[bar construction]] $B(K(-,k),K,*)$, making the connection with another way to define homotopy limits.

[[Urs Schreiber|Urs]]: Thanks, Mike. I see. I should have found this earlier in the literature.  I have spent some time with your article, but maybe I still tend to keep getting a bit lost after a while, to be frank.

Anyway, I have incorporated a bit of discussion of homotopy limits as weighted limits in the example section above now. Personally, I still need to figure out the details of the relation of this to the definition of homotopy limit in terms of bar construction which you hint at.

=--
