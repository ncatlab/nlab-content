

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
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

In a [[category]] with [[internal homs]] $[-,-]$, given an [[object]] $S$, the _continuation monad_ is the [[endofunctor]] $X \mapsto [[X, S], S]$.

In [[computer science]] this [[monad (in computer science)]] is used to model [[continuation-passing style]] of programming, and therefore this is called the _continuation monad_. The idea here is that a morphism $f \colon X \to Y$ in the [[Kleisli category]] of the continuation monad, hence a morphism in the original category of the form $X\longrightarrow [[Y,S],S]$ is much like a map from $X$ to $Y$ only that instead of "returning" its output directly it instead feeds it into a given function $Y \to S$ which hence _continues_ the computation.

## Algebras

\begin{proposition} 
On the [[category of sets]], the functor $[-,S] \colon\mathbf{Set}^{op}\to \mathbf{Set}$ is [[monadic]] (with left adjoint $[-, S]^{op} \colon \mathbf{Set} \to \mathbf{Set}^{op}$) whenever ${|S|}\geq 2$. 
\end{proposition} 

Thus the [[Eilenberg-Moore algebras]] of the continuation monad are equivalent to [[complete atomic Boolean algebras]], as the category of these is equivalent to the opposite of the category of sets. 

(This incidentally illustrates the fact that a category can be monadic over $\mathbf{Set}$ in multiple ways. In other words, one should not refer to a *category* $C$ as monadic over $Set$, unless everyone agrees to which "forgetful functor" $U\colon C \to \mathbf{Set}$ is being considered -- better is to refer to a *functor* as monadic.) 

+-- {: .proof} 
###### Proof 
This boils down to the assertion that such an $S$ is an injective [[cogenerator]] in the category of sets. It is injective because it is a [[retract]] of an [[injective object]] $2^S$ (using the fact that the subobject classifier $2$ is injective), and it cogenerates because there is an injection $2 \to S$ and $2$ cogenerates. 

In more detail: an object $S$ is (internally) *injective* if $[-, S]: Set^{op} \to Set$ takes (coreflexive) [[equalizers]] in $Set$ to [[coequalizers]] in $Set$. The subobject classifier $2$ is injective (by, for example, the proof of Par&eacute;&rsquo;s theorem for constructing finite colimits in an elementary topos). Since $S \times -: Set \to Set$ preserves [[connected limits]] such as equalizers, we have that $[S \times -, 2] \cong [-, 2^S]$ takes equalizers to coequalizers, i.e., $2^S$ is injective for any $S$. Then $S$, being a retract of $2^S$, has the property that $[-, S]$ takes equalizers in $Set$ to coequalizers, i.e., preserves coequalizers $Set^{op} \to Set$. 

Also $[-, S]$ reflects isomorphisms. This is because isomorphisms in $Set$ are precisely epi-monos, and $S$ being an internal cogenerator means exactly that $[-, S]$ is faithful, and faithful functors reflect monos and epis. 

Since $[-, S]$ preserves coequalizers and reflects isomorphisms, we conclude that it is monadic by Beck's crude [[monadicity theorem]]. 
=-- 

## Examples

* [[double negation monad]]

* [[dualizing object in a closed category]]

* [[extensive quantity]]

## Related concepts

* [[selection monad]]

* [[continuation-passing style]]

* [[maybe monad]]

* [[state monad]]

## References

As a [[monad in computer science]]:

* {#Moggi91} [[Eugenio Moggi]], Exp. 1.1 in: *Notions of computation and monads*, Information and Computation, **93** 1 (1991) &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90052-4">doi:10.1016/0890-5401(91)90052-4</a>, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf)&rbrack;


* {#Milewski19} [[Bartosz Milewski]], §21.2.7 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;


* [[Tarmo Uustalu]], p.27 of: *Monads and Interaction Lecture 1* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf), [[Uustalu-Monads1.pdf:file]]&rbrack;, lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021):



The continuation monad is discussed in the generality of [[linear type theory]] as the linear [[double negation monad]] in

* [[Paul-André Melliès]], Nicolas Tabareau, _Linear continuation and duality_, 2008 ([pdf](http://hal.inria.fr/docs/00/33/91/56/PDF/linear-control.pdf))

* [[Paul-André Melliès]], _The parametric continuation monad_, Mathematical Structures in Computer Science, Festschrift in honor of Corrado B&#246;hm for his 90th birthday (2013). ([[MelliesContinuation.pdf:file]])

The characterization of algebras is Proposition 10 of 

* [[Martin Hyland]], [[Paul Blain Levy]], [[Gordon Plotkin]] and [[John Power]], _Combining algebraic effects with continuations_, Theoretical Computer Science, 2007. ([pdf](https://homepages.inf.ed.ac.uk/gdp/publications/comb_cont_journal.pdf))

A characterisation of ([[enriched monad|enriched]]) monads isomorphic to continuation monads is given in:

* Christopher Townsend, _When are enriched strong monads double exponential monads?_, Bulletin of the Belgian Mathematical Society-Simon Stevin 23.2 (2016): 311-319.

[[!redirects continuation monads]]