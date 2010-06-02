
> under construction

> so far this are notes taken in talks by [[Ezra Getzler]]

#Contents#
* automatic table of contents goes here
{:toc}

## $L_\infty$-algebras

The notion of [[L-infinity algebra]] is something that naturally arises in [[deformation theory]]
and in [[descent]] problems. 

A [[dg-Lie algebra]] is a [[chain complex]] of [[vector space]]s

$$
  \cdots
  \to
  V^{-1}
  \stackrel{d}{\to}
  V^0
  \stackrel{d}{\to}
  V^1
  \stackrel{d}{\to}
  V^2
  \to
  \cdots
$$

and is equipped with a bracket operation

$$
  [-,-] : V^i \otimes V^j \to V^{i + j}
$$

which is

* bilinear

* graded antisymmetric: $[x,y] = (-1)^{deg(x) deg(y)} [y,x]$

* satisfies the graded Jacobi identity $[x,[y,z]] = [[x,y],z] + (-1)^{deg(x) deg(y)} [y,[x,z]]$.

* is graded Leibnitz: $d[x,y] = [d x,y] + (-1)^{deg(x)} [x, d y]$.

**Note** If $deg(x)$ is odd, then $[x,x]$ need not vanish. (see also [[super Lie algebra]]).

Let $L$ be a [[dg-Lie algebra]], degreewise finite dimensional ("of finite type" in the language of [[rational homotopy theory]]).

We can form its [[Chevalley-Eilenberg algebra]] (see there for details) of cochains

$$
  CE(L) = (\wedge^\bullet L[1]^*, d)
$$

a [[quasi-free dga]]. 

The underlying graded algebra we may dually think of as functions on some 
space, a **formal graded manifold**.

The total differential 

$$
  \delta = \delta_1 + \delta_2
$$

where the first is $d$ and the second is the bracket $[-,-]^*$ extended as a 
graded derivation.

Being a [[derivation]], dually we may think of this as a [[vector field]]
on our formal smooth manifold. This is sometimes called an [[NQ-supermanifold]].

**Definition**

An [[L-infinity algebra]] (see there) 
of finite type  is the evident generalization of this
inroduced by [[Jim Stasheff]] and [[Tom Lada]] in the early 1990s:

it is a (degreewise finite dimensional) 
free graded-commutative algebra equipped with a differential of degree +1.

Now the differential corresponds to a bunch of $n$-ary brackets. For $n = 1$ this is
the differential on the complex, for $n = 2$ this is the binary bracket from 
above, and then there are higher brackets.


### Morphisms of $L_\infty$-algebras

One can consider two notions of morphisms: strict ones and general ones.

A strict one would be a linear map of the underlying vector spaces that
strictly preserves all the brackets.

A general definitin of morphisms is: in terms of the dual [[dg-algebra]]s
just a morphism of these, going the opposite way. In the dual formulation this 
is due to Lada and Stasheff.

We may also think of this as a morphism of [[NQ-supermanifold]]s.

All this arose in this form probably most vivdly in [[BV-BRST formalism]].

So in components such a morphism $f : L \to K$ of $L_\infty$-algebras 
consists of $n$-ary maps

$$
 f_k : L^{i_1} \otimes \cdots L^{i_k} \to M^{i_1 + \cdots + 1 - k}
$$

(where the shift in the indices is due to the numbering convention here only).

### The homotopical category of $L_\infty$-algebra

We will now describe on the [[category]] of $L_\infty$-algebras the structure of
a [[category of fibrant objects]].

The issue is that the category of $L_\infty$-alghebras as defined above has not
all products and coproducts. 

But we can turn it into a [[category of fibrant objects]].

This is analogous to (in fact an example of the same general fact) 
how [[Kan complex]]es inside all [[simplicial set]]s
are the fibrant objects of the [[model structure on simplicial sets]] but do
not form among themselves a [[model category]] but a 
[[category of fibrant objects]].

See [[Kan complex]] for more...

We now look at the axioms for our category of fibrant objects. It is a slight
variant of those in [[BrownAHT]] described at
[[category of fibrant objects]] and draws bit from work of Dwyer and Kan.

Let $C$ be a [[category]]. The axioms used here are the following.

1. There is a [[subcategory]] $W \subset C$ 
   whose morphisms are called **weak equivalences**, 
   such that this makes $C$ into a 
   [[category with weak equivalences]].

1. There is another [[subcategory]] $F \subset C$, whose morphisms
   are called  **fibrations** (and those that are also 
   in $W$ are called **acyclic fibrations**) , such that

   * it contains all [[isomorphism]]s;

   * the [[pullback]] of a fibration is again a fibration.

   * the pullback of an acyclic fibrations is an acyclic fibration.

1. $C$ has all [[product]]s and in particular a [[terminal object]] $*$.

...