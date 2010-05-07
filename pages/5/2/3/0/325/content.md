
<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For a [[category]] $C$, its _opposite category_ $C^{op}$ is the category obtained by formally reversing the direction of all its [[morphism]]s (while retaining their original composition law).

Categories generalize (are a [[horizontal categorification]]) of [[monoid]]s, [[group]]s and [[algebra]]s and forming the opposite category corresponds to forming the opposite of a group, of a monoid, of an algebra.



## Definition

### In category theory

For $C$ a [[category]] $C$, the **opposite category** $C^{op}$ has the same [[object]]s as $C$, but a [[morphism]] $f : x \to y$ in $C^{op}$ is the same as a morphism $f : y \to x$ in $C$, and a composite of morphisms $g f$ in $C^{op}$ is defined to be the composite $f g$ in $C$.

More precisely, $C_0$ and $C_1$ are, respectively, the collections of [[object]]s and of [[morphism]]s of $C$, and if the structure maps of $C$ are

* source and target: $s_C,t_C : C_1 \to C_0$

* identity-assignment: $i_C : C_0 \to C_1$

* composition: $\circ_C : C_1 \times_{C_0} C_1 \to C_1$ 

then $C^{op}$ is the category with

* the same (isomorphic) collectionns of objects and morphisms

  $(C^{op})_0 := C_0$

  $(C^{op})_1 := C_1$ 

* the same identity-assigning map

  $i_{C^{op}} := i_C$

* _switched_ source and target maps

  $s_{C^{op}} := t_C$

  $t_{C^{op}} := s_C$

* the _same_ composition operation,

  $\circ_{C^{op}} := \circ_{C}$.

  or more precisely, the composition operation of $C^{op}$ is

  $$
    \circ_{C^{op}}
    : 
    C_1^{op} {}_{s^{op}}\times_{t^{op}} C_1^{op}
    =
    C_1 {}_{t} \times_{s} C_1
    \stackrel{\simeq}{\to}
    C_1 {}_{s} \times_{t} C_1
    \stackrel{\circ}{\to}
    C_1
    \,,
  $$

  where the isomorphism in the middle is the unique one induced from the universality of the [[pullback]].

Notice that hence the composition law does _not_ change when passing to the opposite category. Only the interpretation of in which direction the arrows point does change. So forming the opposite category is a completely formal process. Nevertheless, due to the switch of source and target, the opposite category $C^{op}$ is usually far from being [[equivalence of categories|equivalent]] to $C$. See the examples below.


### In enriched category theory ##

The definition has a direct generalization to  [[enriched category theory]].

For $V$ a [[symmetric monoidal category]] and $C$ a $V$-[[enriched category]] the **opposite $V$-enriched category** $C^{op}$ is defined to be the $V$-enriched category with the same objects as $C$ and with

$$
  C^{op}(c,d) := C(d,c)
$$

and composition given by

$$
  C^{op}(b,c)\otimes C^{op}(a,b)
  :=
  C(c,b) \otimes C(b,a)
  \stackrel{\sigma}{\to}
  C(b,a) \otimes C(c,b)
  \stackrel{\circ_C}{\to} 
  C_{c,a}
  =:
  C^{op}(a,c)
  \,.
$$

The unit maps $j_a : I \to C^{op}(a,a)$ are those of $C$ under the identification $C^{op}(a,a) = C(a,a)$.

### In higher category theory

See

* [[opposite 2-category]]

* [[opposite (∞,1)-category]]



## Properties

The [[nerve]] $N(C^{op})$ of $C^{op}$ is the [[simplicial set]] that is degreewise tthe same as $N(C)$, but in each degree with the order of the face and the order of the degeneracy maps reversed. See [[opposite quasi-category]] for more details.




## Classes of examples

### Opposite group

For $G = (S, \cdot)$ a [[group]] (or [[monoid]] or [[associative algebra]], etc.) with product operation

$$
  \cdot_G : S \times S \to S
$$


the **opposite group** $G^{op}$ is the group whose underlying [[set]] (underlying object, underlying vector space, etc.) is the same as that of $G$

$$
  S^{op} := S
$$

but whose product operation is that of $G$ but combined with a switch of the order of the arguments:

$$
  \cdot_{G^{op}} : S \times S \stackrel{\sigma}{\to} S \times S \stackrel{\cdot_S}{\to} S
  \,.
$$

So for $g,h \in S$ two elements we have that their product in the opposite group is

$$
  g \cdot_{G^{op}} h := h \cdot_{G} g
  \,.
$$


Now, the group $G$ may be thought of as the pointed one-object [[delooping]] [[groupoid]] $\mathbf{B}G$ which is the groupoid with a single object, with $S$ as its set of morphisms, and with $\cdot_G$ its composition operation.

Under this identification of groups with one-object categories, passing to the opposite category corresponds precisely to passing to the opposite group

$$
  (\mathbf{B}G)^{op} = \mathbf{B}(G^{op})
  \,.
$$


### Opposite of the opposite

The opposite of an opposite category is the original category

$$
  (C^{op})^{op} = C
  \,.
$$

### Co-algebraic structures

Every algebraic structure in a categoy, for instance the notion of [[monoid]] in a [[monoidal category]] $C$, has a co-version, where in the original definition the direction of all morphisms is reversed -- for instance the co-version of a monoid is a [[comonoid]]. Of an [[algebra]] its a [[coalgebra]], etc.

One may express this succinctly by saying that a co-structure in $C$ is an original structure in $C^{op}$. For instance a [[comonoid]] in $C$ is a [[monoid]] in $C^{op}$.


### Duality

Passing to the opposite category is a realization of abstract [[duality]]. 

This goes as far that some entities are _defined_ as objects in an opposite category. In particular, all generalizations of [[geometry]] which characterize [[space and quantity|spaces]] in terms of [[algebra|algebras]]. The idea of [[noncommutative geometry]] is essentially to define a category of _spaces_ as the opposite category of a category of algebras. Similarly, a [[locale]] is opposite to a [[frame]].

+--{.query}
Are there examples where algebras are defined as dual to spaces?
=--

Another example is the definition of the category of $L_\infty$-[[Lie infinity-algebroid|algebroids]] as that opposite to quasi-free differential graded algebras, identifying every $L_\infty$-algebra with its [[duality|dual]] [[Chevalley-Eilenberg algebra]].



## Specific examples

### Opposite of $FinSet$

The opposit of the category [[FinSet]] of finite sets is equivalent to the category of finite [[boolean algebra]]s

$$
  FinSet^{op} \simeq BoolAlg.
$$


## References

For the definition in enriched category theory see page 12 of 

* [[Max Kelly]], _Basic concepts of enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))


[[!redirects opposite categories]]
[[!redirects dual category]]
[[!redirects dual categories]]