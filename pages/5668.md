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
* table of contents
{:toc}

## Idea


As described in Cartmell's [Generalised Algebraic Theories and
Contextual
Categories](http://dx.doi.org/10.1016/0168-0072%2886%2990053-9), a
generalized algebraic theory (GAT) consists of:

1. An [algebraic theory](algebraic+theory) of sorts, which may itself
     be multi-sorted.

2. A collection of operations, each having zero or more arguments and one
     result.  Each $n$-ary operation is also given with $(n+1)$-many [derived
     operations](http://en.wikipedia.org/w/index.php?title=Universal_algebra&oldid=413212476#Derived_Operations)
     of the algebraic theory of sorts, all of the same arity, specifying the sort of each argument and the sort of the result.

3. Equations between pairs of derived operations[^derived] with the same arity and whose result sorts are provably equal in the algebraic theory of sorts (see example below).

To avoid confusion, this article will refer to the sorts of the algebraic theory of sorts as "supersorts" (this convention is not used in Cartmell's paper).

[^derived]: An $n$-ary derived operation of a GAT is defined in the same manner as a derived operation of a many-sorted algebra, except that it must also be given with $(n+1)$-many derived operations of the algebraic theory of sorts.  Just as in many-sorted algebras, composition of operations is permitted only when the sorts match; in the GAT case those sorts must match for any choice of sort-algebra-derived-operation arguments.

### Examples ###

The theory of categories is a GAT:

1. Its algebraic theory of sorts is two-supersorted, with supersorts "Ob" and "Mor", 
   and one binary operation "Hom(-,+)" with arguments of supersort "Ob"
   and result of supersort "Mor".

2. Its operations include:

* The unary operation $id(-)$ with argument sort given by the
        derived operation $x\mapsto x$ and result sort given by the
        derived operation $x\mapsto Hom(x,x)$.

* The binary operation $comp(-,+)$ with first argument sort
        given by $x,y,z\mapsto Hom(x,y)$ and second argument sort
        given by $x,y,z\mapsto Hom(y,z)$ and result sort given by
        $x,y,z\mapsto Hom(x,z)$

3. Its equations are

* $comp(id(a),f)=f$ where argument $a$ has sort $x,y\mapsto x$
    and argument $f$ has sort $x,y\mapsto Hom(x,y)$

* $comp(f,id(a))=f$ where argument $a$ has sort $x,y\mapsto y$
    and argument $f$ has sort $x,y\mapsto Hom(x,y)$

* $comp(f,comp(g,h))=comp(comp(f,g),h)$ where argument $f$ has sort
    $w,x,y,z\mapsto Hom(w,x)$, argument $g$ has sort $w,x,y,z\mapsto Hom(x,y)$
    and argument $h$ has sort $w,x,y,z\mapsto Hom(y,z)$.

Note that this GAT has no equations imposed on the sort algebra.

One may also elect to include the following operations:

* The unary operation $dom(-)$ with argument sort
        given by the derived operation $x,y\mapsto Hom(x,y)$ and
        result sort given by the derived operation $x,y\mapsto x$

* The unary operation $cod(-)$ with argument sort
        given by the derived operation $x,y\mapsto Hom(x,y)$ and
        result sort given by the derived operation $x,y\mapsto y$

One can also directly axiomatize the theory of [[monoidal categories]] by
adding:

1. A 0-ary operation (constant) $I$ of supersort "Ob" to the algebraic theory of sorts.

2. A binary operation $-\otimes -$ whose arguments and result are of supersort "Ob" to the algebraic theory of sorts.

2. A fifth operation to the GAT having argument sort
$x_1,y_1,x_2,y_2\mapsto Hom(x_1,y_1)$ and $x_1,y_1,x_2,y_2\mapsto
Hom(x_2,y_2)$ and result sort $x_1,y_1,x_2,y_2\mapsto Hom(x_1\otimes
x_2,y_1\otimes y_2)$

2. Operations for the left unitor (argument sort $x\mapsto x$, result sort $x\mapsto I\otimes x$) and its inverse.

2. Operations for the GAT for the right unitor (argument sort $x\mapsto x$, result sort $x\mapsto x\otimes I$) and its inverse.

2. Operations for the GAT for the associator (argument sort $x,y,z\mapsto x\otimes(y\otimes z)$, result sort $x,y,z\mapsto (x\otimes y)\otimes z$) and its inverse.

3. Quite a large number of additional equations corresponding to the pentagon and triangle diagrams, functoriality of the new fifth GAT operation, and inverse+naturality squares for remaining operations.

This GAT also has no equations on the sort algebra.

+-- {: .standout}
I suspsect that you can do strict monoidal categories too (though I haven't worked it out completely) -- but that definitely requires sort equations. -- [[Adam]]
=--

+-- {: .standout}
I think you can do [[multicategories]] too, but that requires infinitely many operations (in both the algebraic theory of sorts and the GAT itself) and infinitely many equations in the GAT.  Even for finitary multicategories.  -- [[Adam]]
=--

Finally, one can axiomatize the theory of categories with [[finite
limits]] as a GAT.  This GAT, however, requires equations on the algebra
of sorts.

### Relationship to Many-Sorted Algebraic Theories ###

A [many-sorted algebraic theory](algebraic+theory#multisorted_algebraic_theories) is a GAT whose algebraic theory of sorts has no equations and no operations of arity greater than zero (i.e., has only constants).

### Relationship to Essentially Algebraic Theories ###

Cartmell's paper explains how for every GAT there is an [[essentially algebraic theory]] (EAT) with the same models and for every EAT there is a GAT with the same models. In this sense they are more or less equivalent in descriptive power.

Cartmell's paper (in section 6) compares EAT's to [[Cartesian logic]].

However (not in Cartmell's paper), there is no notion in the world of EAT's equivalent to a "GAT without sort equations". This is relevant because it yields an interpretation result.  Just as the theory of finite-limit categories is an EAT, and one can interpret any EAT in a finite-limit category, so too is the theory of monoidal categories a GAT without sort equations, and one can interpret any[^any] GAT without sort
equations in a monoidal category.

[^any]: The GAT of monoidal categories (without $dom$ and $cod$) has a nice property: the argument and result sorts of $comp$ are all the same, and we can get away with using the unit object $I$ of the interpreting category for all sorts of supersort $Ob$.  I need to explain how to interpret GATs which lack this property --- those which have more than one supersort with nontrivial sorts.  Here's a sketch: just as in the "nice" case the interpreting monoidal category $V$ will have an object for each sort of the GAT.  Now construct a monoidal category $K$ with an object for each supersort and a morphism for each of the operations in the algebraic theory of sorts.  If $V'$ is the subcategory of $V$ which does the interpretation, there ought to be a [Grothendieck--Street Fibration](Grothendieck+fibration) of $V'$ over $K$ with the fibration functor sending each sort ($V$-object) to its supersort ($K$-object).

### Relationship to Enriched Categories ###

When one interprets the EAT of categories in a [[finite-limit category]] $V$, the result is a $V$-[[internal category]]. When one interprets the GAT of categories in a monoidal category $V$, the result is a $V$-[[enriched category]].

The theory of internal categories is an EAT (specifically, the theory for which a model is a category with a designated category internal to it).  Likewise, the theory of enriched categories is a GAT without sort equations (specifically, the theory for which a model is a category with a category enriched in it).

### Relationship to Type Theory ###

Type theories with type operators and polymorphism but without
dependent types (such as System [$F_\omega$](http://en.wikipedia.org/wiki/System_F#System_F.CF.89) and the [unbounded-rank
polymorphic version](http://haskell.org/ghc/docs/latest/html/users_guide/other-type-extensions.html#universal-quantification) of the [[Haskell]] type system) can represent any GAT
without sort equations, encoding the sorts of the GAT as types and the operations of the algebraic theory of sorts as type operations.  Type
theories without dependent types generally enjoy better [type inference](http://en.wikipedia.org/wiki/Type_inference#Hindley.E2.80.93Milner_type_inference_algorithm)
properties than those with dependent types, making them
practical as programming languages.

### Speculative ###

+-- {: .standout}
Might there be such a thing as an $n$-GAT, where a $0$-GAT is an algebraic theory and an $(n+1)$-GAT is defined as above except that the sort algebra is an $n$-GAT rather than an algebra? -- [[Adam]]
=--

+-- {: .standout}
I feel like there must be some sort of way to eliminate the notion of "arity" and put in its place an arbitrary (G)AT, recovering the original notion using the single-sorted Peano algebra (one constant "0", one unary operation "S", and no equations) or binary tree algebra (one constant "0", one binary operation "B", and no equations).  But I can't quite put my finger on how to do it.  -- [[Adam]]
=--

