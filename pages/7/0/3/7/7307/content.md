
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of _[[operad]]_ comes in two broad flavors (apart from the choice of enriching category): _symmetric operads_ and _[[planar operads]]_.

Roughly, a planar operad consists of $n$-ary operations for all $n \in \mathbb{N}$ equipped with a suitable notion of compositon, while a _symmetric operad_ in addition is equipped with a compatible [[action]] of the [[symmetric group]] $\Sigma_n$ on the set (or [[object]] in the enriching category) of $n$-ary operations. A [[homomorphism]] of symmetric operads is then a morphism of planar operads that in addition respects this action.


The extra "symmetry" structure carried by symmetric operads is crucial for the behaviour of the category of operads in many applications (see the examples below). Notice that it does not so much affect the idea of what a single operad is. In particular, symmetric operads are not restricted to encoding algebraic symmetric structures with symmetric $n$-ary operations! Rather, only the fixed points in the $n$-ary operations of the $\Sigma_n$-action are symmetric operations. If $\Sigma_n$ [[free action|acts freely]], then the corresponding $n$-ary operations are still maximally non-symmetric themselves.

The central example illustrating this are the operads [[Comm]] and [[Assoc]]. Regarded as symmetric [[Set]]-enriched operads, [[Comm]] has the singleton set in each degree, with _trivial_ $\Sigma_n$-action, while [[Assoc]] has $\Sigma_n$ in each degree, freely acting on itself. 

Therefore [[Comm]] is the [[terminal object]] in the [[category]] of symmetric operads (while [[Assoc]], regarded as a [[planar operad]], is the terminal object in that category). 

Multi-coured symmetric operads are equivalently known also as _[[symmetric multicategories]]_.

## Structures on the category of symmetric operads

### Boardman-Vogt tensor product

The category of symmetric operads becomes a [[closed monoidal category|closed]] [[symmetric monoidal category]] for the [[Boardman-Vogt tensor product]].

### Model structure

For $V$ a suitable [[monoidal model category]], the category of $V$-enriched symmetric operads carries a good [[model structure on operads]]. See there for more details.

## Properties

### Relation to categories

+-- {: .num_defn}
###### Definition


Every [[locally small category]] $C$ may be regarded as a coloured symmetric operation $j_!(C)$ over set, with the objects of $C$ and colours, and with only unary operation, these being the morphisms in the category

$$
  j_!(C)(c_1, \cdots, c_n ; c)
  = 
  \left\{
    \array{
       C(c_1, c) & if \, n = 1
       \\
       \emptyset & otherwise
    }
  \right.
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

This [[functor]] $j_! : Cat \to Operad$ has a [[right adjoint]] $j^* : Operad \to Cat$ which sends an operad to the underlying category obtained by discarding all $n$-ary operations for $n \neq 1$.


There is a [[natural isomorphism]] $j * j_! \simeq id$. 

=--

By the discussion at _[[adjoint functor]]_ this exhibits a [[coreflective subcategory]]

$$
  Cat 
   \stackrel{\overset{j_!}{\hookrightarrow}}{\underset{j^*}{\leftarrow}}
  Operad
  \,.
$$



+-- {: .num_remark}
###### Remark

Let $\eta$ denote the symmetric operad with a single colour and no non-identity operation. Then the [[slice category]] of [[Operad]] over $\eta$ is equivalent to [[Cat]]

$$
  Cat \simeq Operad_{/\eta}  
  \,.
$$

Because a morphism of operads $P \to \eta$ can exists precisely if there are no operations of arity other than 1 in $P$.

Under this identification the fuctor $j_!$ is the canonical projection out of the slice category

$$
  j_! : Cat \stackrel{\simeq}{\to} Operad_{/\eta} \to Operad
  \,.
$$

=--



For more on this see at _[[dendroidal set]]_ the section _[The full diagram of relations](http://ncatlab.org/nlab/show/dendroidal%20set#FullDiagram)_.

### Relation to planar operads
 {#RelationToPlanarOperads}

There is an evident [[forgetful functor]]

$$
  U : SymmetricOperad \to PlanarOperad
$$

to the [[category]] of [[planar operads]],
which forgets the [[action]] of the [[symmetric groups]]. This functor has a [[left adjoint]]

$$
  Symm : PlanarOperad \to SymmetricOperad
  \,.
$$

The [[free construction]] freely adds symmetric group actions.

For instance as a [[planar operad]], [[Assoc]] is the [[terminal object]] (has the point in each degree). Its symmetrization $Symm(Assoc)$ is still the operad for associative [[monoids]], now regarded as a symmetric operad, where it has the underlying set of the [[symmetric group]] $\Sigma_n$ in degree $n$. This is no longer the terminal object in $SymmetricOperad$, which instead is [[Comm]].

## Examples

### In $Set$

We list some examples of [[Set]]-enriched symmetric operads.

* For every [[symmetric monoidal category]] $C$, there is naturally the symmetric [[endomorphism operad]] $End(C)$.

  This establishes a reflective (but non-full) inclusion

  $$  
    End : SymmMonCat \to SymmOperad
  $$

  and makes precise the way in which a (symmetric) operad is a generalization of a (symmetric) monoidal category.

  For any other symmetric operad $P$, a morphism of symmetric operads

  $$  
    P \to End(C)
  $$

  is precisely an [[algebra over an operad]] over $P$ in $C$.

* The operad [[Comm]] for [[commutative monoids]] is the [[terminal object]] in symmetric $V$-operads, for instance for $V = $ [[Set]], [[sSet]], [[Top]], etc. 

  It has a single $n$-ary operation for all $n \in \mathbb{N}$, with the [[symmetric group]] necessarily acting trivially in each degree.

  A morphism of operads 

  $$
    A : Comm \to End(Vect)
  $$

  is precisely a commutative and [[associative algebra]] structure on a [[vector space]].

* The operad [[Assoc]] for [[monoids]] is, as a symmetric operad, the one with a single colour that has precisely $n!$ many operations in degree $n$, with the [[symmetric group]] acting freely on these.

  This means that there is a single $n$-ary operation "up to a choice of ordering of its arguments".

  A morphism of operads

  $$
    Assoc \to End(Vect)
  $$

  is precisely an [[associative algebra]] on a vector space.

* For every _non-planar finite rooted [[tree]]_ there is a symmetric operad freely generated by it. For more on this see the section _[Trees and free operads](http://ncatlab.org/nlab/show/dendroidal+set#Trees)_ at _[[dendroidal set]]_.

### In $Top$

(...)
   
## Related concepts

* [[planar operad]]

* [[symmetric multicategory]]

## References

An original source is

* [[Peter May]], _The geometry of iterated loop spaces_, Lectures Notes in Mathematics, Vol. 271, Springer-Verlag, Berlin-New York, (1972).

A survey of the basic notions of symmetric operads is for instance in section 1 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ Contemp. Math. 431 (2007) 31-58 ([arXiv:0512576](http://arxiv.org/abs/math/0512576))

See the references at _[[operad]]_ for more.

Expression of symmetric operads as [[polynomial functor|polynomial]] [[2-monads]] is discussed in

* [[Joachim Kock]], _Data types with symmetries and polynomial functors over groupoids_,  28th Conference on the Mathematical Foundations of Programming Semantics (Bath, June 2012); in Electronic Notes in Theoretical Computer Science.  ([arXiv:1210.0828](http://arxiv.org/abs/1210.0828))

* {#Weber14} [[Mark Weber]], _Operads as polynomial 2-monads_ ([arXiv:1412.7599](http://arxiv.org/abs/1412.7599))

[[!redirects symmetric operads]]
