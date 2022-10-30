+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For a [[category]] $C$, its _opposite category_ $C^{op}$ is the category obtained by formally reversing the direction of all its [[morphisms]] (while retaining their original composition law).

Categories generalize (are a [[horizontal categorification]] of) [[monoids]], [[groups]] and [[algebras]], and forming the opposite category corresponds to forming the opposite of a group, of a monoid, of an algebra.



## Definition

### In category theory

For $C$ a [[category]] $C$, the **opposite category** $C^{op}$ has the same [[objects]] as $C$, but a [[morphism]] $f : x \to y$ in $C^{op}$ is the same as a morphism $f : y \to x$ in $C$, and a composite of morphisms $g f$ in $C^{op}$ is defined to be the composite $f g$ in $C$.

More precisely, $C_{\mathrm{obj}}$ and $C_{\mathrm{mor}}$ are, respectively, the collections of [[objects]] and of [[morphisms]] of $C$, and if the structure maps of $C$ are

* source and target: $s_C,t_C : C_{\mathrm{mor}} \to C_{\mathrm{obj}}$

* identity-assignment: $i_C : C_{\mathrm{obj}} \to C_{\mathrm{mor}}$

* composition: $\circ_C : C_{\mathrm{mor}} \times_{C_{\mathrm{obj}}} C_{\mathrm{mor}} \to C_{\mathrm{mor}}$ 

then $C^{op}$ is the category with

* the same (isomorphic) collections of objects and morphisms

  $(C^{op})_{\mathrm{obj}} := C_{\mathrm{obj}}$

  $(C^{op})_{\mathrm{mor}} := C_{\mathrm{mor}}$ 

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
    C_{\mathrm{mor}}^{op} {}_{s^{op}}\times_{t^{op}} C_{\mathrm{mor}}^{op}
    =
    C_{\mathrm{mor}} {}_{t} \times_{s} C_{\mathrm{mor}}
    \stackrel{\simeq}{\to}
    C_{\mathrm{mor}} {}_{s} \times_{t} C_{\mathrm{mor}}
    \stackrel{\circ}{\to}
    C_{\mathrm{mor}}
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

Note that the [[braiding]] of $V$ is used in defining composition for $C^{op}$.  So, we cannot define the opposite of a $V$-enriched category if $V$ is merely a [[monoidal category]], though $V$-enriched categories still make perfect sense in this case.  If $V$ is a [[braided monoidal category]] there are (at least) two ways to define "$C^{op}$", resulting in two different "opposite categories": we can use either the braiding or the inverse braiding.  If $V$ is [[symmetric monoidal category|symmetric]] these two definitions coincide.

The opposite category can be regarded as a [[dual object]] of $C$ in the [[monoidal bicategory]] $V Prof$ of $V$-categories and $V$-[[profunctors]].  (Note that this does not characterize $C^{op}$ up to equivalence, but only up to [[Morita equivalence]], i.e. up to [[Cauchy completion]].)  When $V$ is symmetric, then $V Prof$ is also symmetric monoidal, so there is only one notion of dual object.  When $V$ is braided, then $V Prof$ is not symmetric and has two notions of dual: a left dual and a right dual.  These are exactly the two different opposite categories referred to above (the "left opposite" and "right opposite").


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

The opposite of an opposite category is the original category:

$$
  (C^{op})^{op} = C
  \,.
$$

This is also true for $V$-enriched categories when $V$ is symmetric monoidal, but not when $V$ is merely braided.  However, in the latter case we can say $(C^{op1})^{op2} = C = (C^{op2})^{op1}$, i.e. the two different notions of "opposite category" are inverse to each other (as is always the case for left and right dualization operations in a non-symmetric monoidal (bi)category).


### Co-algebraic structures

Every algebraic structure in a category, for instance the notion of [[monoid]] in a [[monoidal category]] $C$, has a co-version, where in the original definition the direction of all morphisms is reversed -- for instance the co-version of a monoid is a [[comonoid]]. Of an [[algebra]] its a [[coalgebra]], etc.

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

The opposite of the category [[FinSet]] of finite sets is equivalent to the category of finite [[boolean algebra]]s

$$
  FinSet^{op} \simeq BoolAlg.
$$


## References

For the definition in enriched category theory see page 12 of 

* [[Max Kelly]], _Basic concepts of enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))


[[!redirects opposite categories]]
[[!redirects dual category]]
[[!redirects dual categories]]