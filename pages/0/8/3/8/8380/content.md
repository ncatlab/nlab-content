
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In [[computer science]], a _monad_ describes a "notion of computation".  Formally, it is a map that 

* sends every [[type]] $X$ of some given [[programming language]] to a new type $T(X)$ (called the "type of $T$-computations with values in $X$");

* is equipped with a rule for composing two [[functions]] of the form $f : X \to T(Y)$ (called _[[Kleisli functions]]_) and $g : Y \to T(Z)$ to a function $g \circ f : X \to T (Z)$ (their [[Kleisli composition]]);

* is in a way that is [[associativity law|associative]] in the evident sense and [[unit law|unital]] with respect to a given unit function called $pure_X : X \to T(X)$, to be thought of as taking a value to the pure computation that simply returns that value.

This is essentially the same structure as a _[[monad]]_ in the sense of [[category theory]], but presented differently; see below for the precise relationship.

### For imperative programs in functional programming
 {#ForImperativeProgramsInFunctionalProgramming}

Monads provide one way to "embed [[imperative programming]] in 
[[functional programming]]", and are used that way notably in the 
[[programming language]] [[Haskell]]. But monads, as well as [[comonads]] and related structures, exist much more generally in programming languages; an exposition is in ([Harper](#Harper)). For an account of the use of monads in industry see [Benton15, pp. 11-12](#Benton15).

For instance when the monad $T(-)$ forms [[product types]] $T(X) \coloneqq X \times Q$ with some fixed type $Q$ that carries the structure of a [[monoid]], then a [[Kleisli function]] $f : X \to Y \times Q$ may be thought of as a function $X \to Y$ that produces a [[side effect]] output of type $Q$.  The Kleisli composition of two functions $f \colon X \to Y \times Q$ and $g \colon Y \to Z \times Q$ then not only evaluates the two programs in sequence but also combines their $Q$-output using the monoid operation of $Q$; so if $f x = (y,q)$ and $g y = (z,q')$ then the final result of $(g \circ f)(x)$ will be $(z, q q')$.  For example, $Q$ might be the set of strings of characters, and the monoid operation that of concatenation of strings (i.e. $Q$ is the [[free monoid]] on the type of characters).  If the software is designed such that values of type $Q$ computed in this way appear on the user's screen or are written to memory, then this is a way to encode _input/output_ in [[functional programming]] (see the [[IO monad]] below). 

But monads have plenty of further uses. They are as ubiquituous (sometimes in disguise) in [[computer science]] as [[monad|monads in the sense of category theory]] are (sometimes in disguise) in [[category theory]]. This is no coincidence, see _[Relation to monads in category theory](#RelationToMonadsInCategoryTheory)_ below.

### Relation to monads in category theory
 {#RelationToMonadsInCategoryTheory}

In [[computer science]], a [[programming language]] may be formalised or studied by means of a [[category]], called the _[[syntactic category]]_ $\mathcal{C}$, whose 

* [[objects]]$\;$ $X \in \mathcal{C}$ are the [[types]] of the language, 

* [[morphisms]] $X \to Y$ are the [[terms]] or [[programs]] (or an [[equivalence class]] of such) that takes a value of [[type]] $X$ as input and returns a value of type $Y$.  

This point of view (see _[[computational trinitarianism]]_) is particularly useful when studying purely [[functional programming|functional programming languages]].

Under this [[relation between type theory and category theory]] monads on the type system in the sense of computer science are [[monad|monads in the sense of category theory]], being certain [[endofunctors]] 

$$
  T \colon \mathcal{C} \longrightarrow \mathcal{C}
$$

on the [[syntactic category]]. This [[functor]]

1. sends each [[type]], hence [[object]] $X \in \mathcal{C}$ to another object $T(X)$;

1. the unit [[natural transformation]] $\epsilon \colon Id_{\mathcal{C}} \Rightarrow T$ of the [[monad]] $T$ provides for each type $X$ a component [[morphism]] $pure_X : X \to T(X)$;

1. the _multiplication_ [[natural transformation]] $\mu \colon T \circ T \Rightarrow T$ of the monad provides for each object $X$ a morphism $\mu_X : T(T(X)) \to T(X)$ which induces the [[Kleisli composition]] by the formula

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


The monads arising this way in computer science are usually required also to interact nicely with the structure of the programming language, as encoded in the structure of its syntactic category; in most cases, terms of the language will be allowed to take more than one input, so the category $\mathcal{C}$ will be at least [[monoidal category|monoidal]], and the corresponding kind of 'nice' interaction corresponds to the monad's being a _[[strong monad]]_ (see e.g. [McDermott & Uustalu (2022)](#McDermottUustalu22)).

The 'bind' operation is a means of describing multiplication on such a strong monad $M$. It is a term of the form $M A \to (M B)^A \to M B$, which is equivalent to a map of the form $M A \times M B^A \to M B$. It is the composite 

$$
  M A \times M B^A 
    \stackrel{strength}{\to} 
  M(A \times M B^A) 
    \stackrel{M eval_{A, M B}}{\to} 
  M M B 
    \stackrel{m B}{\to} M B
$$ 

where $m \colon M M \to M$ is the monad multiplication.

When monads are defined in [[Haskell]], the Kleisli composition, 'bind', is defined in Haskell. So monads in Haskell are always [[enriched monads]], according to the self-enrichment defined by the function type in Haskell.

## Examples
 {#Examples}

Various monads are _definable_ in terms of the the standard type-forming operations ([[product type]], [[function type]], etc.). These include the following.

* A [[functional program]] with input of [[type]] $X$, output of [[type]] $Y$ and mutable state $S$ is a [[function]] ([[morphism]]) of [[type]] $X \times S \longrightarrow Y \times S$. Under the ([[Cartesian product]] $\dashv$ [[internal hom]])-[[adjunction]] this is equivalently given by its [[adjunct]], which is a function of type $X \longrightarrow [S, S \times Y ]$. Here the operation $[S, S\times (-)]$ is the [[monad]] induced by the above adjunction and this latter function is naturally regarded as a morphism in the [[Kleisli category]] of this monad. This monad $[S, S\times (-)]$ is called the _[[state monad]]_ for mutable states of type S.

* The **[[maybe monad]]** is the operation $X \mapsto X \coprod \ast$. The idea here is that a function $X \longrightarrow Y$ in its [[Kleisli category]] is in the original category a function of the form $X \longrightarrow Y \coprod \ast $ so either returns indeed a value in $Y$ or else returns the unique element of the [[unit type]]/[[terminal object]] $\ast$. This is then naturally interpreted as "no value returned", hence as indicating a "failure in computation".

* The maybe monad is a special case of the **[[exception monad]]**.

* The **[[continuation monad]]** for a given type $S$ acts by $X \mapsto [[X,S],S]$.

* A number of further monads are similarly *definable* in terms of standard type-forming operations, such as the [[reader monad]] and the [[writer comonad]].

  Given a [[type]] $W$, the **[[reader monad]]** is the operation of forming the [[function type]] $[W,-] = (W\to (-))$; the [[writer monad]] and the **[[writer comonad]]** are the operations of forming the [[product type]] $W\times (-)$, and the composite of writer followed by reader is the [[state monad]] $[W, W \times (-)]$.

  When $W$ carries the structure of a [[monoid object]] then writer also inherits the structure of a monad (on top of being a comonad) and converse for reader.

Other monads may be supplied "axiomatically" by the programming language, 

This includes

* the [[IO monad]] in [[Haskell]].

* The **[[completion monad]]** may be used, as in [[constructive analysis]], for dealing for instance with [[real numbers]].

See also:

* **[[state monad]]**

* Equipping [[homotopy type theory]] (say implemented as a programming language concretely in [[Coq]] or [[Agda]]) with two axiomatic [[idempotent monads]], denoted $\sharp$ and $\Pi$, with some additional data and relations, turns it into _[[cohesive homotopy type theory]]_. See also _[[modal type theory]]_.

## Related concepts

Examples of (co)monads in ([[homotopy type theory|homotopy]]) [[type theory]] involve in particular _[[modal operators]]_ as they  appear in 

* [[modal logic]]/[[modal type theory]]/[[computational type theory]].

See also

* [[adjoint modality]]

For an approach to composing monads, see

* [[monad transformer]]

Another approach to modelling side effects in [[functional programming languages]] are 

* [[algebraic side effects]]

[[free monad|Free monads]] in computer science appear in the concepts of 

* [[initial algebra for an endofunctor]]

* [[terminal coalgebra for an endofunctor]]

Other generalizations are 

* [[arrow (in computer science)]]

* [[applicative functor]]

There is also

* [[monad (in linguistics)]]


## References

### General

The original reference for monads as 'notions of computation':

* {#Moggi91} [[Eugenio Moggi]], _Notions of computation and monads_, Information and Computation, 93(1), 1991. ([pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf))

On the impact of Moggi's work and making a case for [[Lawvere theory|Lawvere theories]]:

* {#HylandPower07} [[Martin Hyland]], [[John Power]], _The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads_, Electronic Notes in Theoretical Computer Science (ENTCS) archive Volume 172, April, 2007 Pages 437-458  ([pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf))

Textbook accounts:

* {#Milewski19} [[Bartosz Milewski]] (compiled by Igal Tabachnik), "Monads: Programmer's Definition", §20 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;



Further discussion/exposition of (co)monads in computer science:
 
* [[Philip Wadler]], _Comprehending Monads_, in _Conference on Lisp and functional programming_, ACM Press, 1990 ([[WadlerMonads.pdf:file]])

* {#BrookesGeva91} [[Stephen Brookes]], Shai Geva, *Computational Comonads and Intensional Semantics*, CMU-CS-91-190 (1991) &lbrack;[[BrookersGeva-ComputationalComonads.pdf:file]]&rbrack;

* [[Philip Wadler]], *Monads for functional programming*, in M. Broy (eds.) *Program Design Calculi* NATO ASI Series, **118** Springer (1992) &lbrack;[doi;10.1007/978-3-662-02880-3_8](https://doi.org/10.1007/978-3-662-02880-3_8), [pdf](https://homepages.inf.ed.ac.uk/wadler/papers/marktoberdorf/baastad.pdf)&rbrack;

* Philip Mulry, _Monads in semantics_ , ENTCS **14** (1998) pp.275-286.



* John Hughes, section 2 of _Generalising Monads to Arrows_, Science of Computer Programming (Elsevier) 37 (1-3): 67&#8211;111. (2000) ([pdf](http://pdn.sciencedirect.com/science?_ob=MiamiImageURL&_cid=271600&_user=10&_pii=S0167642399000234&_check=y&_origin=search&_zone=rslt_list_item&_coverDate=2000-05-31&wchp=dGLzVlk-zSkWb&md5=fa91ab4ffc136b0cedc52318c7c249be&pid=1-s2.0-S0167642399000234-main.pdf))

* {#Harper} [[Robert Harper]], _Of course ML Has Monads!_ (2011) ([web](http://existentialtype.wordpress.com/2011/05/01/of-course-ml-has-monads/))

* {#Benton15} [[Nick Benton]], _Categorical Monads and Computer Programming_, ([pdf](https://www.lms.ac.uk/sites/lms.ac.uk/files/2.%20Benton%20-%20Categorical%20Monads%20and%20Computer%20Programming.pdf))

* {#Riehl17} [[Emily Riehl]], *A categorical view of computational effects*, talk at *[C$\circ$mp$\circ$se$\colon\!\colon$Conference](https://www.composeconference.org/2017/)* (2017) &lbrack;[pdf](http://www.math.jhu.edu/~eriehl/compose.pdf), [[Riehl-ComputationalEffects.pdf:file]]&rbrack;

* Rob Norris, *Functional Programming with Effects*, talk at 
*Scala Days 2018* &lbrack;video: [YT](https://youtu.be/30q6BkBv5MY)&rbrack;

* {#Uustalu21} [[Tarmo Uustalu]], lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021):

  *Monads and Interaction Lecture 1* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf), [[Uustalu-Monads1.pdf:file]]&rbrack;

  *Monads and Interaction Lecture 2* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs2.pdf), [[Uustalu-Monads2.pdf:file]]&rbrack;

  *Monads and Interaction Lecture 3* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs3.pdf), [[Uustalu-Monads3.pdf:file]]&rbrack;

  *Monads and Interaction Lecture 4* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs4.pdf), [[Uustalu-Monads4.pdf:file]]&rbrack;



* Christina Kohl, Christina Schwaiger, *Monads in Computer Science* (2021) &lbrack;[pdf](https://www.uibk.ac.at/mathematik/algebra/staff/fritz-tobias/ct2021_course_projects/category_theory.pdf), [[KohlSchwaiger-Monads.pdf:file]]&rbrack;

See also:

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Monad_(functional_programming)">Monad (functional programming)</a>_

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Side_effect_(computer_science)">Side_effect_(computer_science)</a>*

The specification of [[monads]] in [[Haskell]] is at:

* [The Haskell programming language](http://www.haskell.org/haskellwiki/Haskell), 

  * *[Monad](https://wiki.haskell.org/Monad)*

  * *[Monad laws](http://www.haskell.org/haskellwiki/Monad_laws)*

and an exposition of [[category theory]] and monads in terms of Haskell is in 

* WikiBooks, _[Haskell/Category](http://en.wikibooks.org/wiki/Haskell/Category_theory)_

On the issue of  the CS-style monads really being [[strong monads]]:

* {#McDermottUustalu22} [[Dylan McDermott]], [[Tarmo Uustalu]], *What Makes a Strong Monad?*, EPTCS **360** (2022) 113-133 &lbrack;[arXiv:2207.00851](https://arxiv.org/abs/2207.00851), [doi:10.4204/EPTCS.360.6](https://doi.org/10.4204/EPTCS.360.6)&rbrack;


A comparison of monads with [[applicative functors]] (also known as idioms)
and with [[arrows (in computer science)]] is in 

* Exequiel Rivas, _Relating Idioms, Arrows and Monads from Monoidal Adjunctions_, ([arXiv:1807.04084](https://arxiv.org/abs/1807.04084))

Generalization from [[monads]] to [[relative monads]] is discussed in

* [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;

Discussion of [[comonads]] in this context includes


* {#Overton14} David Overton, _Comonads in Haskell_, 2014 ([web](https://speakerdeck.com/dmoverton/comonads-in-haskell))

### In quantum computation


Discussion of aspects of [[quantum computing]] in terms of monads in [[functional programming]] are in 

* [[Thorsten Altenkirch]], Alexander Green, _The quantum IO monad_, in _Semantic Techniques in Quantum Computation_, January 2009, appeared in 2010 ([pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [talk slides](http://www.cs.nott.ac.uk/~txa/talks/qnet06.pdf))

* J. K. Vizzotto, [[Thorsten Altenkirch]], A. Sabry, _Structuring quantum effects: superoperators as arrows_ ([arXiv:quant-ph/0501151](http://arxiv.org/abs/quant-ph/0501151))



[[!redirects monad (computer science)]]
[[!redirects monads (computer science)]]

[[!redirects monad (in computer science)]]
[[!redirects monads (in computer science)]]

[[!redirects monad (in programming theory)]]
[[!redirects monads (in programming theory)]]

[[!redirects monad in computer science]]
[[!redirects monads in computer science]]

[[!redirects computational effect]]
[[!redirects computational effects]]

