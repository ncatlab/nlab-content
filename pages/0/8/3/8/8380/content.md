
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[computer science]], a _monad_ describes a "notion of computation".  Formally, it is a map that 

* sends every [[type]] $X$ of some given [[programming language]] to a new type $T(X)$ (called the "type of $T$-computations with values in $X$");

* equipped with a rule for composing two [[functions]] of the form $f : X \to T(Y)$ (called _[[Kleisli functions]]_) and $g : Y \to T(Z)$ to a function $g \circ f : X \to T (Z)$ (their [[Kleisli composition]]);

* in a way that is [[associativity law|associative]] in the evident sense and [[unit law|unital]] with respect to a given unit function called $pure_X : X \to T(X)$, to be thought of as taking a value to the pure computation that simply returns that value.

This is essentially the same structure as a [[monad]] in [[category theory]], but presented differently; see below for the precise relationship.

### For imperative programs in functional programming

Monads provide one way to "embed [[imperative programming]] in 
[[functional programming]]", and are used that way notably in the 
[[programming language]] [[Haskell]]. (But monads, as well as [[comonads]] and related structures, exist much more generally in programming languages; an exposition is in ([Harper](#Harper))). 

For instance when the monad $T(-)$ forms [[product types]] $T(X) \coloneqq X \times Q$ with some fixed type $Q$ that carries the structure of a [[monoid]], then a [[Kleisli function]] $f : X \to Y \times Q$ may be thought of as a function $X \to Y$ that produces a "side effect" output of type $Q$.  The Kleisli composition of two functions $f \colon X \to Y \times Q$ and $g \colon Y \to Z \times Q$ then not only evaluates the two programs in sequence but also combines their $Q$-output using the monoid operation of $Q$; so if $f x = (y,q)$ and $g y = (z,q')$ then the final result of $(g \circ f)(x)$ will be $(z, q q')$.  For example, $Q$ might be the set of strings of characters, and the monoid operation that of concatenation of strings (i.e. $Q$ is the [[free monoid]] on the type of characters).  If the software is designed such that values of type $Q$ computed in this way appear on the user's screen or are written to memory, then this is a way to encode _input/output_ in [[functional programming]] (see the [[IO monad]] below). 

But monads have plenty of further uses. They are as ubiquituous (sometimes in disguise) in [[computer science]] as [[monad|monads in the sense of category theory]] are (sometimes in disguise) in [[category theory]]. This is no coincidence, see _[Relation to monads in category theory](#RelationToMonadsInCategoryTheory)_ below.

### Relation to monads in category theory
 {#RelationToMonadsInCategoryTheory}

In [[computer science]], a programming language may be formalised or studied by means of a [[category]], called the _[[syntactic category]]_ $\mathcal{C}$, whose 

* [[objects]] $X \in \mathcal{C}$ are the [[types]] of the language, 

* [[morphisms]] $X \to Y$ are the [[terms]] or [[programs]] (or an [[equivalence class]] of such) that takes a value of [[type]] $X$ as input and returns a value of type $Y$.  

This point of view (see _[[computational trinitarianism]]_) is particularly useful when studying purely [[functional programming|functional programming languages]].

Under this [[relation between type theory and category theory]] monads on the type system in the sense of computer science are [[monad|monads in the sense of category theory]], being certain [[endofunctors]] 

$$
  T : \mathcal{C} \to \mathcal{C}
$$

on the [[syntactic category]]. This [[functor]]

1. sends each [[type]], hence [[object]] $X \in \mathcal{C}$ to another object $T(X)$;

1. the unit [[natural transformation]] $\epsilon : Id_{\mathcal{C}} \Rightarrow T$ of the [[monad]] $T$ provides for each type $X$ a component [[morphism]] $pure_X : X \to T(X)$;

1. the _multiplication_ [[natural transformation]] $\mu : T \circ T \Rightarrow T$ of the monad provides for each object $X$ a morphism $\mu_X : T(T(X)) \Rightarrow T(X)$ which induces the [[Kleisli composition]] by the formula

  $$
    \begin{aligned}
    (g \circ f)
    &\coloneqq
    (Y \stackrel{g}{\to} T(Z)) \circ_{Kleisli} (X \stackrel{f}{\to} T(Y))
    \\
    & \coloneqq
    X \stackrel{f}{\to} T(Y)
    \stackrel{T(g)}{\to} T(T(Z))
    \stackrel{\mu(Z)}{\to}
    T Z
    \end{aligned}
    \,,
  $$

Here the morphism $T(g)$ in the middle of the last line makes use of the fact that $T(-)$ is indeed a [[functor]] and hence may also be applied to morphisms / functions between types. The last morphism $\mu(Z)$ is the one that implements the "$T$-computation".


The monads arising this way in computer science are usually required also to interact nicely with the structure of the programming language, as encoded in the structure of its syntactic category; in most cases, terms of the language will be allowed to take more than one input, so the category $\mathcal{C}$ will be at least [[monoidal category|monoidal]], and the corresponding kind of 'nice' interaction corresponds to the monad's being a _[[strong monad]]_.

When monads are defined in Haskell, the Kleisli composition (called 'bind') is defined in Haskell. So monads in Haskell are always enriched monads, according to the self-enrichment defined by the function type in Haskell.

## Examples
 {#Examples}

Various monads are _definable_ in terms of the the standard type-forming operations ([[product type]], [[function type]], etc.). These include the following.

* A [[functional program]] with input of [[type]] $X$, output of [[type]] $Y$ and mutable state $S$ is a [[function]] ([[morphism]]) of [[type]] $X \times S \longrightarrow Y \times S$. Under the ([[Cartesian product]] $\dashv$ [[internal hom]])-[[adjunction]] this is equivalently given by its [[adjunct]], which is a function of type $X \longrightarrow [S, S \times Y ]$. Here the operation $[S, S\times (-)]$ is the [[monad]] induced by the above adjunction and this latter function is naturally regarded as a morphism in the [[Kleisli category]] of this monad. This monad $[S, S\times (-)]$ is called the _[[state monad]]_ for mutable states of type S.

* The [[maybe monad]] is the operation $X \mapsto X \coprod \ast$. The idea here is that a function $X \longrightarrow Y$ in its [[Kleisli category]] is in the original category a function of the form $X \longrightarrow Y \coprod \ast $ so either returns indeed a value in $Y$ or else returns the unique element of the [[unit type]]/[[terminal object]] $\ast$. This is then naturally interpreted as "no value returned", hence as indicating a "failure in computation".

* The [[continuation monad]] for a given type $S$ acts by $X \mapsto [[X,S],S]$.

* A number of further monads are similarly *definable* in terms of standard type-forming operations, such as the [[reader monad]] and the [[writer comonad]].

  Given a [[type]] $W$, then the [[reader monad]] is the operation of forming the [[function type]] $[W,-] = (W\to (-))$; the [[writer comonad]] is the operation of forming the [[product type]] $W\times (-)$ and the composite of writer followed by reader is the [[state monad]] $[W, W \times (-)]$.

  When $W$ carries the structure of a [[monoid object]] then writer also inherits the structure of a monad (on top of being a comonad) and converse for reader.

Other monads may be supplied "axiomatically" by the programming language, 
This includes

* the [[IO monad]] in [[Haskell]].

* The [[completion monad]] may be used, as in [[constructive analysis]], for dealing for instance with [[real numbers]].

* Equipping [[homotopy type theory]] (say implemented as a programming language concretely in [[Coq]] or [[Agda]]) with two axiomatic [[idempotent monads]], denoted $\sharp$ and $\Pi$, with some additional data and relations, turns it into _[[cohesive homotopy type theory]]_. See also _[[modal type theory]]_.

## Related concepts

Examples of (co)monads in ([[homotopy type theory|homotopy]]) [[type theory]] involve in particular _[[modal operators]]_ as they  appear in 

* [[modal logic]]/[[modal type theory]]/[[computational type theory]].

See also

* [[adjoint modality]]

Another approach to modelling side effects in [[functional programming languages]] are 

* [[algebraic side effects]]

[[free monad|Free monads]] in computer science appear in the concepts of 

* [[initial algebra for an endofunctor]]

* [[terminal coalgebra for an endofunctor]]

Another generalization is 

* [[arrow (in computer science)]]

## References

### General

The original reference for monads as 'notions of computation' is

* [[Eugenio Moggi]], _Notions of computation and monads_ Information And Computation, 93(1), 1991. ([pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf))

Expositions include
 
* [[Philip Wadler]], _Comprehending Monads_, in _Conference on Lisp and functional programming_, ACM Press, 1990 ([[WadlerMonads.pdf:file]])

* [[Philip Wadler]], _Monads for functional programming_ in _Lecture notes for the Marktoberdorf Summer School on Program Design Calculi_, Springer Verlag 1992

* John Hughes, section 2 of _Generalising Monads to Arrows_, Science of Computer Programming (Elsevier) 37 (1-3): 67&#8211;111. (2000) ([pdf](http://pdn.sciencedirect.com/science?_ob=MiamiImageURL&_cid=271600&_user=10&_pii=S0167642399000234&_check=y&_origin=search&_zone=rslt_list_item&_coverDate=2000-05-31&wchp=dGLzVlk-zSkWb&md5=fa91ab4ffc136b0cedc52318c7c249be&pid=1-s2.0-S0167642399000234-main.pdf))

* {#Harper} [[Robert Harper]], _Of course ML Has Monads!_ (2011) ([web](http://existentialtype.wordpress.com/2011/05/01/of-course-ml-has-monads/))


The specification of monads in [[Haskell]] is at

* [The Haskell programming language](http://www.haskell.org/haskellwiki/Haskell), _[Monad laws](http://www.haskell.org/haskellwiki/Monad_laws)_

and an exposition of [[category theory]] and monads in terms of Haskell is in 

* WikiBooks, _[Haskell/Category](http://en.wikibooks.org/wiki/Haskell/Category_theory)_


Generalization from [[monads]] to [[relative monads]] is discussed in

* [[Thorsten Altenkirch]], James Chapman, Tarmo Uustalu, _Monads need not be endofunctors_ ([pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf))

Discussion of [[comonads]] in this context includes


* {#Overton14} David Overton, _Comonads in Haskell_, 2014 ([web](https://speakerdeck.com/dmoverton/comonads-in-haskell))

### In quantum computation


Discussion of aspects of [[quantum computing]] in terms of monads in [[functional programming]] are in 

* [[Thorsten Altenkirch]], Alexander Green, _The quantum IO monad_, in _Semantic Techniques in Quantum Computation_, January 2009, appeared in 2010 ([pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [talk slides](http://www.cs.nott.ac.uk/~txa/talks/qnet06.pdf))

* J. K. Vizzotto, [[Thorsten Altenkirch]], A. Sabry, _Structuring quantum effects: superoperators as arrows_ ([arXiv:quant-ph/0501151](http://arxiv.org/abs/quant-ph/0501151))


[[!redirects monad (in computer science)]]
[[!redirects monads (in computer science)]]

[[!redirects monad (in programming theory)]]
[[!redirects monads (in programming theory)]]

[[!redirects monad in computer science]]
[[!redirects monads in computer science]]