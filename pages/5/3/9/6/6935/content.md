
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _inductive type_ is a [[type]] whose [[categorical semantics]] is given by an [[initial algebra of an endofunctor]].

This has the usual meaning in ordinary [[category theory]]. In applications to [[(∞,1)-category theory]], the uniqueness clause in the notion of initial object is modified to allow for a [[contractible space]] of choices (as discussed at _[[initial object in an (∞,1)-category]]_), and this difference is reflected accordingly in the type-theoretic set-up. The [[syntax]] will give back the traditional meaning whenever equality is interpreted [[extensional type theory|extensionally]].

## Explanation 

In ordinary [[category theory]], the notion of an initial algebra $W$ [[algebra for an endofunctor|for an endofunctor]] $F$ can be broken down into three parts: 

1. It is an $F$-algebra, given by a structure $F(W) \to W$. Typically this structure is delivered in terms of _constructors_ (maps into $W$ out of the components of a coproduct decomposition of $F(W)$).

1. For any algebra $A$, there exists an algebra map $W \to A$.

1. Any two algebra maps from $W$ to $A$ are equal. 

In type theory, we break things down a bit differently, for a variety of reasons.  In terms of the [[categorical semantics|categorical interpretations]] of [[dependent type theory]], what the structure of an inductive type gives us is the following.

1. An algebra structure $W$, prescribed by constructors.

1. For any algebra $A$, a _specified_ algebra map $W \to A$.

1. Given a [[display map]] (e.g., a [[fibration]]) $B \to W$, where $B$ is given an algebra structure and the display map is an algebra map, one has a specified [[section]] $W \to B$ that is also an algebra map.

In fact, the second piece of structure is obtained as the special case of the third where $B = W\times A$ and the display map is the evident projection.  We refer to the specified section as the (dependent) *eliminator*, and to the fact that it is an algebra map as its *computation rule*.

Let us check that we get the usual notion of initial algebra from this in the case where equality is extensional (e.g., categories enriched in [[homotopy type|homotopy 0-types]] = sets). In other words, assume that the [[diagonal]] map $\delta \colon A \to A \times A$ is a display map or fibration, and suppose $f$ and $g$ are algebra maps from $W$ to $A$. We pull back to a display map over $W$,

$$\array{
P & \to & A \\
\downarrow & & \downarrow^\mathrlap{\delta} \\
W & \underset{\langle f, g \rangle}{\to} & A \times A,
}$$ 

and this $P \to W$ is also an algebra map. Therefore it has a (specified) section. But since $P \to W$ is also monic, the section forces it to be an [[isomorphism]], whence $f$ and $g$ are equal. Thus in this case, the inductive type is an initial algebra (under the traditional meaning in ordinary category theory). 

Notice that this is the [[induction]] principle (subalgebras of an initial algebra are the whole initial algebra). 

In [[intensional type theory]], where the diagonal is not a display map, we can perform the same argument using a [[path object]] $P A \to A \times A$ (represented in type theory by an [[identity type]]), showing thereby that $f$ and $g$ are homotopic.  A fancier version of this argument enables us to show that the space of algebra maps $W\to A$ is actually contractible. In other words, the axioms for an inductive type still imply that algebra maps out of $W$ are essentially unique, even though the axioms do not state this explicitly. 


## Type-theoretic definition 

To be written. Presumably there are introduction, elimination, and computation rules. 

## Properties

### Homotopy initiality

Any inductive type $W$ is a homotopy initial F-[[algebra over an endofunctor|algebra]]: 
the space
of $F$-[[algebra for an endofunctor|algebra]] maps $W \to X$ is 
[[contractible]].

([Awodey-Gambino-Sojakova](#AwodeyGambinoSojakova))

## Examples

### Natural numbers

In [[Coq]]-[[syntax]] the [[natural numbers]] are the inductive type defined by

    Inductive nat : Type :=
     | zero : nat
     | succ : nat -> nat.

This is the initial algebra for the endofunctor $F(X) = 1 + X$.

### Identity types

In [[Coq]]-[[syntax]] the [[identity types]] are the inductive types (or more precisely, the inductive *family*) defined by

    Inductive id {A} : A -> A -> Type := 
      idpath : forall x, id x x.

This is the "initial algebra" for the endofunctor of the [[slice category]] over $A\times A$ which is constant at the [[diagonal]] $A\to A\times A$.


## Related concepts

* [[initial algebra of an endofunctor]]

* [[W-type]]

* [[higher inductive types]]

## References

A very basic introduction to the concept, with an eye towards explaining [[identity types]] is in 

* [[Mike Shulman]], _Induction on equality_ ([pdf](http://www.math.ucsd.edu/~mshulman/papers/induction.pdf))

Expositions (with an eye towards [[higher inductive types]]) include

* [[Mike Shulman]], _Homotopy type theory IV_ ([web](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_vi.html))

* [[Peter LeFanu Lumsdaine]], _Higher inductive types, a tour of the menageries_ ([blog post](http://homotopytypetheory.org/2011/04/24/higher-inductive-types-a-tour-of-the-menagerie/))

* [[Mike Shulman]], _Inductive and higher inductive types_, talk slides (2012) ([pdf](http://www.math.ucsd.edu/~mshulman/hottminicourse2012/04induction.pdf))

The formalization in [[Coq]] is discussed in 

* Eduardo Gim&#233;nez, Pierre Cast&#233;ran, _A Tutorial on [Co-]Inductive Types in Coq_ ([pdf](http://flint.cs.yale.edu/cs428/coq/pdf/RecTutorial.pdf))

A study of the "homotopy-initiality" of inductive types in [[homotopy type theory]] is in

* [[Steve Awodey]], [[Nicola Gambino]], [[Kristina Sojakova]], *Inductive types in homotopy type theory* ([arXiv:1201.3898](http://arxiv.org/abs/1201.3898))
 {#AwodeyGambinoSojakova}

The corresponding [[Coq]]-code is at

* [https://github.com/HoTT/HoTT/tree/master/Coq/IT](https://github.com/HoTT/HoTT/tree/master/Coq/IT)

Exposition and discussion of that result is in 

* [[Steve Awodey]], _Inductive types in Hott_ ([blog post](http://homotopytypetheory.org/2012/01/19/inductive-types-in-hott/))

[[!redirects inductive types]]
