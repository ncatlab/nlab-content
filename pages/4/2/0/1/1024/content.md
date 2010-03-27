
#Contents#
* automatic table of contents goes here
{:toc}

## Idea and definition

In the category [[Set]] of [[set]]s, for $X$ a set, an element $x \in X$ is equivalently a [[morphism]] in [[Set]] (namely a function of sets) $x : {*} \to X$, where "$*$" denotes [[generalized the|the]] [[point]] -- the set with a single element.

One notices that from the point of view of the category [[Set]], whatever can be said and done about elements of a set $X$, can be set and done for _any_ morphism $x : U\to X$, from _any_ other set $U$. This is the point of view on sets adopted in [[structural set theory]] such as [[ETCS]].

But moreover, once elements of objects are regarded as morphisms into these objects, the same reasoning applies to _every_ [[category]] $C$. 

Accordingly, for $C$ any [[category]] and $X$ an [[object]] of $C$, one may think of a [[morphism]] $x : U \to X$ as a **generalized element** of $X$. One says this is a generalized element with **stage of definition** given by $U$.

In [[type theory]] one says that such generalized element $x$ is a **term** of **type** $X$, which expresses the same idea.

The perspective of generalized elements of objects of a category $C$ is related to regarding $C$ as its image under the [[Yoneda embedding]]

$$
  Y : C \hookrightarrow [C^{op}, Set]
$$

into its [[presheaf category]]. Under this embedding, every object $X$ of $C$ is mapped the [[functor]] -- the [[representable functor]] represented by it --

$$
  GenEl(X) : C^{op} \to Set
$$ 

that sends each object $U$ of $X$ to the set of generalized elements of $X$ at stage $U$.


## Examples 


### In $Set$

The primordial example is when $C$ is the category [[Set]] of sets and $I$ is a [[terminal object]] in $Set$ --- that is, a set with one element.  Then elements of any set $c$ are in one-to-one correspondence with functions $f: I \to c$.  This correspondence works as follows: given any element of $c$ there is a unique function $f: I \to c$ with this element in its image, and conversely each function $f: I \to c$ has a unique element of $c$ in its image. 

In the same way, in a [[concrete category]] represented by $I$, the $I$-elements of an object are the same as the elements of its underlying set.  (The category of sets is actually a special case of this, since it is concrete and represented by a terminal object.)

Generalizing from $Set$ in another way, in any category with a terminal object $I$, we call a morphism $f : I \to c$ a [[global element]] of the object $c$.  Generalizing further, it is common to take $I$ to be the unit object whenever $C$ is a [[monoidal category]]; in this case the generalized elements are important in [[enriched category|enriched category theory]]).  Note that any [[closed monoidal category]] is again a concrete category represented by this $I$.

The most general case where a single object $I$ may be used to define global elements is where $I$ is a [[generator]] of the category.  However, not every category has a single object as a generator!  Instead, in arbitrary categories, generalized elements of *all* possible stages of definition must often be used to replace global elements.  Thus while a set is determined by its global elements, an object of an arbitrary category is determined by all of its generalized elements (this is one way to state the [[Yoneda lemma]]).



### More examples

* For $C =$ [[Set]] and $I = \{\bullet\}$ the singleton set, the [[global elements]] of a set $C$ are precisely the ordinary elements of $C$.

* For $C = [D^{op}, Set]$  a [[presheaf]] category and for $I = \Delta_{pt} = (d \mapsto \{\bullet\})$ the presheaf constant on the singleton set, the generalized elements of a presheaf $F$ are the _[[global section]]s_ of this presheaf, equivalently these are the elements in the [[limit]] set over $F$.

* Again for $C = [D^{op}, Set]$ and $I=D(-,d)$ a [[representable functor|representable]] presheaf, the generalized elements of $F$ at stage $d$ are precisely the elements of the set $F(d)$, by the [[Yoneda lemma]].

* An [[element in an abelian category]] is an equivalence class of generalised elements.

[[!redirects generalised element]]
[[!redirects generalised elements]]
[[!redirects generalized elements]]
