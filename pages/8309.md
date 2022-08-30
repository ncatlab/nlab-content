
# Contents
* table of contents
{: toc}

## Idea

A _binary function_, or _function of two variables_, is like a [[function]] but with two [[domains]].  That is, while a function $f$ from the [[set]] $A$ to the set $C$ maps an [[element]] $x$ of $A$ to a unique element $f(x)$ of $C$, a binary function from $A$ and $B$ to $C$ maps an element $x$ of $A$ and an element $y$ of $B$ to a unique element $f(x,y)$ of $C$.

We can generalise further to _multiary functions_, or _functions of several variables_.


## Definitions

The possible definitions depend on [[foundations]]; for us, the simplest is probably this:

+-- {: .num_defn}
###### Definition
A __binary function__ from $A$ and $B$ to $C$ is simply a [[function]] $f$ to $C$ from the binary [[cartesian product]] $A \times B$.  We write $f(x,y)$ for $f((x,y))$.
=--

This is natural in [[structural set theory]]; it makes sense in any [[set theory]] and (suitably interpreted) in a foundational [[type theory]].

In [[material set theory]], one often declines to specify the domain of a function (since this can be recovered from it); then we can say this:

+-- {: .num_defn}
###### Definition
A __binary function__ to $C$ is simply a [[function]] $f$ to $C$ such that every [[element]] of the [[domain]] of $f$ is an [[ordered pair]].  Again, we write $f(x,y)$ for $f((x,y))$.
=--

An equivalent (but different) definition in material set theory is this:

+-- {: .num_defn}
###### Definition
A __binary function__ to $C$ is a [[ternary relation]] $f$ such that

* given $(x,y,z) \in f$, we have $z \in C$, and
* given $(x,y,z) \in f$ and $(x,y,z') \in f$, we have $z = z'$.

Now we write $f(x,y)$ for the unique $z$ (if any) such that $(x,y,z) \in f$.
=--

Either way, the material concept is actually more general than the structural one, because the [[domain]] of a material binary function might not be a [[cartesian product]].  The link is provided by the binary version of a [[partial function]]:

+-- {: .num_defn}
###### Definition
A __partial binary function__ from $A$ and $B$ to $C$ is a function to $C$ from a [[subset]] of $A \times B$.
=--

One can also define a notion of binary function without any notion of ordered pair, as long as one has the [[function set|set of functions]] from any set to any other set.  This is called a [[currying|curried]] representation.

+-- {: .num_defn}
###### Definition
A __binary function__ from $A$ and $B$ to $C$ is a [[function]] from $A$ to the set $C^B$ of all functions from $B$ to $C$.
=--

The connection is that if $f$ is a binary function defined as having ordered pairs in its domain, the corresponding function from $A$ to $C^B$ sends $a\in A$ to the function that sends $b\in B$ to $f(a,b)\in C$.  One can give a similar comparison of material and structural versions of this definition.  In addition, this definition is usually the one used in [[type theory]].

It\'s also possible to take the concept of binary function as an undefined primitive concept, on the same level as that of [[function]].  Then we want [[axioms]] such as the following (depending on the style of [[foundations]]):

*  Given an [[element]] $x$ of the [[set]] $A$, an element $y$ of $B$, and a binary function from $A$ and $B$ to $C$, we have an element $f(x,y)$ of $C$.

*  If $x$ and $x'$ are [[equality|equal]] elements of $A$ and $y$ and $y'$ are equal elements of $B$, then $f(x,y) = f(x',y')$.

*  Given two such binary functions $f$ and $f'$, if $f(x,y) = f'(x,y)$ for every $x$ in $A$ and every $y$ in $B$, then $f = f'$.


## Internalization

The cartesian-product-based definitions make sense internal to any [[category]] with binary [[cartesian products]].  More generally, we can consider any [[monoidal category]].

Similarly, the curried definition makes sense internal to any [[closed category]].  The cartesian analogue of a closed category (not to be confused with a [[cartesian closed category]], which also has finite products) exists but is not well-known.

Finally, the undefined concept of "binary function" can be internalized to the [[binary morphisms]] in any [[multicategory]], in particular perhaps a [[cartesian multicategory]].  If a multicategory has tensor products, then its binary morphisms are representable in the ordered-pair style, while if it has hom-objects, they are representable in the curried style; but in general a multicategory may have neither.

## Special cases

A binary function to the set of [[truth values]] is a [[binary relation]].

A binary function from $A$ and $A$ to $C$ may be simply called a __binary function__ from $A$ to $C$.

A binary function $f$ from $A$ to $C$ is __symmetric__ if $f(a,b) = f(b,a)$ always.


## Related concepts

* **binary function**, [[bilinear map]], [[multilinear map]]

* [[binary morphism]], [[multimorphism]]

* [[bifunctor]], [[Quillen bifunctor]]


[[!redirects binary function]]
[[!redirects binary functions]]

[[!redirects function of two variables]]
[[!redirects functions of two variables]]
[[!redirects functions of two variables each]]

[[!redirects binary map]]
[[!redirects binary maps]]
[[!redirects binary mapping]]
[[!redirects binary mappings]]

[[!redirects symmetric binary function]]
[[!redirects symmetric binary functions]]

