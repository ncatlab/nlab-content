#Conten#
* automatic table of contents goes here
{:toc}

## Idea ##

[[localization|Localizations]] of catories and higher categories in the sense of [[left adjoint]] functors $L : C \to C'$ to inclusions $C' \hookrightarrow C$ of full subcategories (as in particular for [[geometric embeddings]]) are characterized by the collection $S \subset Mor(C)$ of morphisms of $C$ which are sent by $L$ to isomorphisms, or more generally to equivalences, as well as by the collection of objects which are _local_ with respect to these morphisms, in that these morphisms behave as equivalences with respect to homming into objects.



## Definition for ordinary categories ##

### Local objects ###

Let $C$ be a [[category]] and $S$ a collection of [[morphisms]] in $C$. Then an [[object]] $c \in C$ is **$S$-local** if the [[hom-functor]]
$$
  C(-,c) : C^{op} \to Set
$$
sends morphisms in $S$ to [[isomorphisms]] in [[Set]], i.e. if
for every $s : a \to b$ in $S$, the functor
$$
  C(s,c) : C(b,c) \to C(a,c)
$$
is a [[bijection]].


### Local morphisms ###

Conversely, a **morphism** $f : x \to y$ is **$S$-local if for every $S$-local object $c$ the induced morphism

$$
  C(f,c) : C(y,c) \to C(x,c)
$$

is an isomorphism.



## Definition for $(\infty,1)$-categories ##



### Local objects ###

**Definition [def. 5.5.4.1](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf#page=383) in [[Higher Topos Theory|HTT]]**

Let $C$ be an [[(∞,1)-category]] and $S$ a collection of morphisms in $C$. Then an [[object]] $c \in C$ is **$S$-local** if the [[hom-functor]]
$$
  C(-,c) : C^{op} \to \infty Top
$$
evaluated on $s \in S$ induces isomorphism in the [[homotopy category]] of [[Top]].

### Local morphisms ###

Conversely, a **morphism** $f : x \to y$ is **$S$-local if for every $S$-local object $c$ the induced morphism

$$
  C(f,c) : C(y,c) \to C(x,c)
$$

induces an isomorphism in the [[homotopy category]] of [[Top]].

## Definition in simplicial model categories ##

Let $C$ be a [[simplicial model category]]. And let $S \subset Mor(C)$
be a collection of [[morphism]]s in $C$.

Consider in the following the standard [[model structure on simplicial sets]]
with weak equivalences given by morphisms that induce isomorphisms on all
[[simplicial homotopy group]]s.

* An object $c \in C$ is a **$S$-local object** if for all $s : a \to b$
in $C$ the induced morphismm
  $$
    C(s,c) : C(b,c) \to C(a,c)
  $$
  is a homotopy equivalence of simplicial sets.
  
* A morphism $f : x \to y$ in $C$ is an **$S$-local morphism**
  or **$S$-equivalence** if for every $S$-local object $c$
  the induced morphism
  $$
    C(f,c) : C(y,c) \to C(x,c)
  $$
  is a homotopy equivalence of simplicial sets.


This is section A.3.7 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

> do we really want to say homotopy equivalence here?



## Saturated class of morphisms ##

Every morphism in $S$ is $S$-local.
The collection $S$ of morphisms is called **saturated** if the collection of $S$-local morphisms coincides with $S$.




##Remarks##


* a [[reflective subcategory]] as well as a [[reflective (∞,1)-subcategory]] can be realized as the full (($\infty,1$)-)subcategory on $S$-local objects, where $S$ is the collection of morphisms sent by the corresponding [[localization of an (∞,1)-category]] to equivalences. For details on this see the discussion at [[geometric embedding]].

[[!redirects local objects]]