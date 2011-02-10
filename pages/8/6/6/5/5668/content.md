
### Definition ###

As described in Cartmell's [Generalised Algebraic Theories and
Contextual
Categories](http://dx.doi.org/10.1016/0168-0072%2886%2990053-9), a
generalized algebraic theory (GAT) consists of:

  1. An [algebraic theory](algebraic+theory) of sorts, which may itself
     be multi-sorted.

  2. A collection of operations, each having zero or more arguments and one
     result, with a [derived
     operation](http://en.wikipedia.org/wiki/Universal_algebra#Derived_Operations)
     of the sort algebra specifying the type of each argument and the
     type of the result.

  3. Equations between pairs of derived operations of the same arity.
     An equation between two derived operations is
     permissible only if their result types are equal as derived
     operations of the algebra of sorts (see example below).

To avoid confusion, this article will refer to the sorts of the sort algebra as "kinds" (this convention is not used in Cartmell's paper).

### Examples ###

The theory of categories is a GAT:

1. Its algebraic theory of sorts is two-kinded, with kinds "Ob" and "Mor", 
   and one binary operation "Hom(-,+)" with arguments of kind "Ob"
   and result of kind "Mor".

2. Its operations include:

* The unary operation $id(-)$ with argument type given by the
        derived operation $x\mapsto Ob$ and result type given by the
        derived operation $x\mapsto Hom(x,x)$.

* The binary operation $comp(-,+)$ with first argument type
        given by $x,y,z\mapsto Hom(x,y)$ and second argument type
        given by $x,y,z\mapsto Hom(y,z)$ and result type given by
        $x,y,z\mapsto Hom(x,z)$

3. Its equations are

* $comp(id(a),f)=f$ where argument $a$ has sort $x,y\mapsto x$
    and argument $f$ has sort $x,y\mapsto Hom(x,y)$

* $comp(f,id(a))=f$ where argument $a$ has sort $x,y\mapsto y$
    and argument $f$ has sort $x,y\mapsto Hom(x,y)$

* $comp(f,comp(g,h))=comp(comp(f,g),h)$ where argument $f$ has sort
    $w,x,y,z\mapsto Hom(w,x)$, argument $g$ has sort $w,x,y,z\mapsto Hom(x,y)$
    and argument $h$ has sort $w,x,y,z\mapsto Hom(y,z)$.

Note that this GAT has no equations imposed on the sort algebra.  One may also elect to include the following operations:

* The unary operations $dom(-)$ and $cod(-)$ with argument type
        given by the derived operation $x,y\mapsto Hom(x,y)$ and
        result type given by the derived operation $x,y\mapsto Ob$

One can also directly axiomatize the theory of [[monoidal categories]] by
adding:

1. A third operation $-\otimes -$ to the sort algebra, having two arguments
   each of kind "Ob" and result of kind "Ob"

2. A fifth
operation to the GAT having argument type
$x_1,y_1,x_2,y_2\mapsto Hom(x_1,y_1)$ and $x_1,y_1,x_2,y_2\mapsto
Hom(x_2,y_2)$ and result type $x_1,y_1,x_2,y_2\mapsto Hom(x_1\otimes
x_2,y_1\otimes y_2)$

3. Quite a large number of additional equations corresponding to the pentagon and triangle diagrams and functoriality of the new GAT operation.

This GAT also has no equations on the sort algebra.

+-- {: .standout}

I suspsect that you can do strict monoidal categories too (though I haven't worked it out completely) -- but that definitely requires sort equations. -- [[Adam]]

=--

Finally, one can axiomatize the theory of categories with [[finite
limits]] as a GAT.  This GAT, however, requires equations on the algebra
of sorts.

### Relationship to Essentially Algebraic Theories ###

Cartmell's paper explains how, for every GAT there is an EAT with the
same models and for every EAT there is a GAT with the same models.  In
this sense they are more or less equivalent in descriptive power.

However (not in Cartmell's paper), there is no notion in the world of
EAT's equivalent to a "GAT without sort equations".  This is relevant
because it yields an interpretation result.  Just as the theory of
finite-limit categories is an EAT, and one can interpret any EAT in a
finite-limit category, so too is the theory of monoidal categories a
GAT without sort equations, and one can interpret any GAT without sort
equations in a monoidal category.

### Relationship to Enriched Categories ###

When one interprets the EAT of categories in a [[finite-limit category]]
$V$, the result is a $V$-[[internal category]].  When one interprets the
GAT of categories in a monoidal category $V$, the result is an
$V$-[[enriched category]].

### Relationship to Type Theory ###

Type theories with type operators and polymorphism but without
dependent types (such as System $F^\omega$ and the unbounded-rank
polymorphic version of the Haskell type system) can represent any GAT
without sort equations, encoding the sorts of the GAT as types.  Type
theories without dependent types generally enjoy better type inference
properties than those with dependent types, making them more
practical as programming languages.

### Speculative ###

+-- {: .standout}

Might there be such a thing as an $n$-GAT, where a $0$-GAT is an algebraic theory and an $(n+1)$-GAT is defined as above except that the sort algebra is an $n$-GAT rather than an algebra? -- [[Adam]]

=--

