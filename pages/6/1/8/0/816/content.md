#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The notion of _weighted limit_ is naturally understood from the point of view on [[limits]] as described at [[representable functor]].

Weighted limits make sense and are considered in the general context of $V$-[[enriched category theory]], but restrict attention to $V=$ [[Set]] for the moment, in order to motivate the concept.

Let $K$ denote the small category which indexes [[diagrams]] over which we want to consider limits and eventually weighted limits. Notice that for 

$$
  F : K \to Set
$$

a [[Set]]-valued functor on $K$, the limit of $F$ is canonically identified simply with the set of [[cones]] with tip the singleton set $pt = \{\bullet\}$:

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

The idea is that the weight $W : K \to V$ encodes the way in which one generalizes the concept of a [[cone]] over a diagram $F$ (that is, something with just a tip from which morphisms are emanating down to $F$) to a more intricate structure over the diagram $F$. For instance in the application to [[homotopy limits]] discussed below with $V$ set to [[SimpSet]] the weight is such that it ensures that not only 1-morphisms are emanating from the tip, but that any triangle formed by these is filled by a 2-cell, every tetrahedron by a 3-cell, etc.

## Definition ##

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

(Here $[K,V]$ is the $V$-[[enriched functor category]], as usual.)


In particular, if $C = V$ itself, then we get the direct formula
$$
  lim^W F \simeq [K,V](W,F)
  \,.
$$

This follows from the above by 
$$
  \begin{aligned}
    [K,V](W(-),C(c,F(-)))
    &:=
    \int_{k \in K} V(W(k),V(c,F(k)))
    \\
    &  \simeq 
      \int_{k \in K} V(c,V(W(k),F(k))
    \\
    &  \simeq 
      V(c, \int_{k \in K} V(W(k),F(k))   
    \\
    & =:
      V(c, [K,V](W,F))   
    \,.
  \end{aligned}
$$


## Examples  ##


### Homotopy limits ###

For $V$ some category of higher structures, the _local_ definition of [[homotopy limit]] over a diagram $F : K \to C$ replaces the ordinary notion of [[cone]] over $F$ by a higher cone in which all triangles of 1-morphisms are filled by 2-cells, all tetrahedra by 3-cells, etc. 

One can convince oneself that for the choice of [[SimpSet]] for $V$ this is realized in terms of the weighted limit $lim^W F$ with the weight $W$ taken to be

$$
  W : K \to \Simp\Set
$$
$$
  W : k \mapsto N(K/k)
   \,,
$$

where $K/k$ denotes the [[over category]] of $K$ over $k$ and $N(K/k)$ denotes its [[nerve]].

This leads to the classical definition of homotopy limits in $\Simp\Set$-enriched categories due to

* A.K. Bousfield and D.M. Kan, _Homotopy limits, completions, and localizations_

See for instance also

* Nicola Gambino, _Weighted limits in simplicial homotopy theory_ ([pdf](http://www.crm.cat/Publications/08/Pr790.pdf))

In some nice cases the weight $N(K/-)$ can be replaced by a simpler weight; an example is discussed at [[Bousfield-Kan map]].

### Homotopy pullback ###

For instance in the case that 
$K = \{r \to t \leftarrow s\}$ is the [[pullback]] diagram we have

$$
  W(r) = \{r\}
$$
$$
  W(s) = \{s\}
$$
$$
  W(t) = N( \{r \to t \leftarrow s\} )
$$
and $W(r \to t) : \{r\} \to \{r \to t \leftarrow s\}$ injects the vertex $r$ into $\{r \to t \leftarrow s\}$ and similarly for $W(s \to t)$.

This implies that for $F : K \to C$ a pullback diagram in the [[SimpSet]]-eriched category $C$, a $W$-weighted [[cone]] over $F$ with tip some object $c  \in C$, i.e. a natural transformation

$$
  W \Rightarrow C(c, F(-))
$$

is

* over $r$ a "morphism" from the tip $c$ to $F(r)$ (i.e. a vertex in the Hom-simplicial set $C(c,F(r))$);

* similarly over $s$;

* over $t$ three "morphisms" from $c$ to $F(t)$ together with 2-cells between them (i.e. a 2-[[horn]] in the Hom-simplicial set $C(c,F(t))$)

* such that the two outer morphisms over $t$ are identified with the morphisms over $r$ and $s$, respectively, postcompoised with the morphisms $F(r \to t)$ and $F(s \to t)$, respectively.

So in total such a $W$-weighted cone looks like

$$
  \array{
     &&& c
     \\
     & \swarrow &\Rightarrow& \downarrow    
      &\Leftarrow& \searrow
     \\
     F(r) 
      &&
     \stackrel{F(r \to t)}{\to}
      & 
     F(t)
      & 
     \stackrel{F(s \to t)}{\leftarrow}
     &&
     F(s)
  }
$$

as one would expect for a "homotopy cone".


##References for homotopy limits in terms of weighted limits##

Details of this are discussed for instance in the book

* Hirschhorn, _Model categories and their localization_

To compare with the above discussion notice that

* The functor
$$
  W := N(K/-)
$$
is discussed there in definition 14.7.8 on p. 269. 

* the $V$-enriched hom-category $[K,V]$ which on $V$-functors $S,T$ is the [[end]] $[K,V](S,T) = \int_{k \in K} V(S(k), T(k))$ appears as $hom^K(S,T)$ in definition 18.3.1 (see bottom of the page).

* for $V$ set to [[SimpSet]] the above definition of homotopy limit appears in example 18.3.6 (2).



#References#

A standard reference is

* M. Kelly, _Basic concepts of enriched category theory_, [section 3.1, p. 37](http://www.emis.de/journals/TAC/reprints/articles/10/tr10.pdf#page=37)

In 

* E. Riehl, _Weighted limits and colimits_ (2008) ([pdf](http://www.math.uchicago.edu/~eriehl/cat/weighted.pdf))

[[Emily Riehl]] gives an account of lectures by [[Mike Shulman]] on the subject. The definition appears there as [definition 3.1, p. 4](http://www.math.uchicago.edu/~eriehl/cat/weighted.pdf#page=4) (in a form a bit more general than the one above).

[[!redirects weighted limits]]

