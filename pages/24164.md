[[!redirects Eric Finster, Towards Higher Universal Algebra in Type Theory]]
## Contents

* table of contents
{:toc}

## Idea

While [[homotopy type theory]] formalizes [[homotopy theory]], it is not a priori clear -- and in fact is or was an open problem -- how to formalize general homotopy-[[coherence|coherent]] [[structures]] of [[higher algebra]]/[[higher category theory]]: Since these typically involve an _infinite_ hierarchy of [[coherence]]-conditions, these cannot be [[axiom|axiomatized]] directly, but one needs some scheme that generates them. This turned out to be subtle.

[[Eric Finster]] had previously considered another variant of [[type theory]], called _[[opetopic type theory]]_ which natively talks about [[infinity-categories]] and their higher [[coherences]] by type-theoretically formalizing the [[structure]] of [[opetopic sets]]. In new work [Finster 18](#Finster2018) he gives something like an implementation of aspects of [[opetopic type theory]] _within_ [[homotopy type theory]] and provides evidence that this  yields a tool to solve the general problem of [[coherences]] of [[higher algebra]]/[[higher category theory]] within [[homotopy type theory]].

Polynomials serve as a notion of "*higher signature*". Following ideas from the categorical approach to universal algebra, we are going to encode the relations or axioms of our structure using a monadic multiplication on P.

## Eric's talk

In Eric's Agda formalisation and talk, a polynomial has its parameter sorts encoded with the parameter. We will follow a suggestion by Mike to have a $\SortOf$ function instead. This should make some definitions less cluttered.

Let $I : \mathcal{U}$ be a type of sorts. A polynomial over $I$ consists of the following data:

 * A family of operations $\Op : I \to \mathcal{U}$
 * For each operation, a family of parameters $\Param_i : (f : \Op i) \to \mathcal{U}$
 * A function $\SortOf : (f : \Op i) \to \Param f \to I$

We define the type of operations of a polynomial $P$ as:

$$ \Ops \equiv \sum_{i : I} \Op_P i$$

A polynomial $P : \Poly I$ generates a type of trees:

The inductive famiy $\Tr_P : I \to \mathcal{U}$ has constructors

 * $\lf : (i : I) \to \Tr_P i$
 * $\nd : (i : I) \to (f : \Op_P i) \to (\phi : (p : \Param f) \to \Tr_P (\SortOf(f,p))) \to \Tr_P i$

For a tree $w : \Tr_P i$ we define its type of leaves by induction on $w$.

$$ \Leaf_i : (w : Tr_P i) \to I \to \mathcal{U} $$

* $\Leaf( (\lf i), j) \equiv (i =_I j)$
* $\Leaf( \nd (f, \phi), j) \equiv \sum_{p : \Param f} \Leaf(\phi(p), j)$

and its type of nodes:

$$ \Node_i : (w : \Tr_P i) \to \Ops \to \mathcal{U} $$

* $\Nodes(\lf i, jg) \equiv \mathbf{0}$
* $\Nodes(\nd(f,\phi), jg) \equiv ((i,f) = jg) + \sum_{p : \Param f} \Node(\phi(p), jg)$

Let $w : \Tr_i P$ be a tree and $f : Op_P i$ an operation. A frame from $w$ to $f$ is an equivalence:
$$\Frame(w,f) \equiv \sum_{j:I} \Leaf(w,j) \simeq \Param_i(f)$$

i.e. the type of leaves of the tree is equivalent to the type of parameters of the operator.

A polynomial relation for $P$ is a [[type family]]:

$$ R :{i : I} \to (f : \Op i) \to (w : \Tr i) (\alpha : \Frame(w,f)) \to \mathcal{U}$$

Let $P : \Poly I$ and let $R$ be a relation on $P$. The slice of $P$ by $R$, denoted $P // R$, is the polynomial with sorts $\Ops$ defined as follows:

TODO: Continue writing this out. Essentially following [this coq file](https://github.com/Alizter/HoTT/blob/higher-alg/contrib/higher-alg/Polynomial3.v)

## Definitions and Examples

Here we collect the definitions and ideas that were given in Eric's talk. We can also use the Agda formalisation for reference too.

+-- {: .num_defn}
###### Definition

Fix a [[type]] $I$ of sorts. A **polynomial** over $I$, $\Poly I$, is the data of

 * A [[type family|family]] of operations $\Op : I \to \mathcal{U}$
 * For each operation, for each $i : I$, a family of sorted parameters

	$$\Param_i : (f : \Op i) \to  I \to \mathcal{U}$$
 
=--


+-- {: .num_remark}
###### Remark

 * For $i : I$, an element $f: \Op i$ represents an operation whose output sort is $i$.
 * For $f : \Op i$ and $j : I$, and element $p : \Param_i(f, j)$ represents an input parameter of sort $j$.

 * The $\Op i$ and $\Param_i (f, j)$ are not truncated at set level. So operations and parameters can have higher homotopy.

 * In [[HoTT book]] notation, we can write the previous definition as:

$$\Poly I \equiv \sum_{\Op : I \to \mathcal{U}}\prod_{i : I} \Param_i$$

$$\Param_i \equiv \prod_{f : \Op i}I \to \mathcal{U}$$
=--

+-- {: .num_remark}
###### Example
We start with the simplest non-trivial example, when $I \equiv \mathbf{1}$ the [[unit type]]. Looking at $\Poly \mathbf{1}$ we clearly have $\Op : \mathbf{1} \to \mathcal{U}\simeq \mathcal{U}$. So $\Op$ is simply a type. Next we have $\Param : (f : \Op) \to \mathbf{1} \to \mathcal{U}\simeq \Op \to \mathcal{U}$ so $\Param$ is just a family of types indexed over the type $\Op$.

Now if $\Op \equiv \Fin_3$ then there would be 3 operations. Take one of these operations and call it $o_1$, $\Param$ would then have to chose what the type of parameters should be, let's choose $\Fin_2$. This would mean that $o_1$ would be an operation ($o_1 : \Op$) with two parameters $p : \Fin_2 \equiv \Param o_1$. Note $o_1$ is very much like the operator in an abstract syntax tree in this case.

When the type of sorts $I$ gets more structure, the objects we discuss get complicated quickly. Even letting $\Param o_1$ be some arbitrary type gives us an interesting object.

=--

A polynomial $P : \Poly I$ generates an associated type of trees.

+-- {: .num_defn}
###### Definition
The type of **trees** associated to a polynomial $P : \Poly I$ is an [[inductive family]] $\Tr P : I \to \mathcal{U}$ that has constructors 

 * $\lf : (i : I) \to \Tr(P, i)$
 * $\nd : (i : I) \to (f : \Op(P,i)) \to (\phi : (j : I) \to (p : \Param_i (f, j)) \to \Tr(P, j)) \to \Tr(P, i)$

=--

For a tree $w : \Tr (P, i)$, we will need its type of leaves and type of nodes

+-- {: .num_defn}
###### Definition
The type of **leaves** of a tree $P : \Poly I$ is given by:

 * $\Leaf : (i : I) \to (w : \Tr i) \to I \to \mathcal{U}$
 * $\Leaf_i((\lf i), j) \equiv (i = j)$
 * $\displaystyle\Leaf_i ( \nd(f, \phi),j) \equiv \sum_{k : I} \sum_{p : \Param (f, k)} \Leaf_i ((\phi (k, p)), j)$

=--

+-- {: .num_defn}
###### Definition
The type of **nodes** of a tree $P : \Poly I$ is given by:

 * $\Node : (i : I) \to (w : \Tr i) \to (j : I) \to \Op j \to \Type$
 * $\Node_i ((\lf i), j, g) \equiv \mathbf{0}$
 * $\displaystyle \Node_i (\nd(f,\phi),j,g) \equiv ((i,f)=(j,g)) + \sum_{k : I} \sum_{p : \Param(f,k)} \Node_i ( \phi( j, p), j, g) $

=--

+-- {: .num_defn}
###### Definition
Let $P : \Poly I$ be a polynomial $w : \Tr(P,i)$ a tree and $f : \Op(P,i)$ an operation. A **frame** from $w$ to $f$ is a [[family]] of [[equivalences]]
$$\Frame(w,f):(j:I) \to \Leaf_i(w,j) \simeq \Param(P,f,j)$$
=--

+-- {: .num_defn}
###### Definition
A *polynomial relation* for $P$ is a [[type family]]:

$$R : (i:I) (f:\Op i)(w : \Tr i)(\alpha : \Frame(w,f) \to \mathcal{U}$$

=--

## References
 {#Link}

* {#Finster2018} [[Eric Finster]], _Towards Higher Universal Algebra in Type Theory_, [Homotopy Type Theory Electronic Seminar](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html) 2018 ([compact pdf slides](/nlab/files/Finster-2018-HoTTEST-compact.pdf), [original pdf slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Finster-2018-12-6-HoTTEST.pdf), [recording](https://www.youtube.com/watch?v=hlCVHVtAlqQ))

* [[Agda]] code at: [github.com/ericfinster/higher-alg](https://github.com/ericfinster/higher-alg)

* [Notes on a definition of higher structure](http://ericfinster.github.io/files/huadtt.pdf).

The idea of [[opetopic sets]] that [Finster 18](#Finster2018) is inspired by goes back to

* [[John Baez]], [[James Dolan]], _Higher-Dimensional Algebra III: n-Categories and the Algebra of Opetopes_, [arXiv:q-alg/9702014](https://arxiv.org/abs/q-alg/9702014)


category: reference
