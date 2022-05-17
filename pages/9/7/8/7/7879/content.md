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

*Haskell* is a [[type theory|typed]] [[functional programming language]]. It is named after [[Haskell Brooks Curry]].

## Properties

### Category-theoretic properties

Viewed as a syntactic framework, we can identify a subset of Haskell called $\mathbf{Hask}$ that is often used to identify concepts used in basic category theory. One considers Haskell [[type|types]] as objects of a category whose morphisms are extensionally identified Haskell functions. 

With $\to$ and $\times$ etc., we can work $\mathbf{Hask}$ almost as if it were even a Cartesian closed category. A particular problem is the polymorphic term $\text{undefined}$, which is defined to be term of every type. It prevents, for example, initial objects (i.e. there's no analog of the empty set). Or, when it comes to setting up the categorical product, the projections $\pi_1$ and $\pi_2$ couldn't distinguish between $(\text{undefined},\text{undefined})$ and just $\text{undefined}$, spoiling uniqueness. A related deficit is that when it comes to passing functions as arguments, Haskell sees more than just Hask morphisms. 

The standard notion of functors in Haskell are not terms of a Hask type but operate on one level above those, the kind level. If '7' is of type 'Int' and 'Int' is of kind 'U', then a functor corresponds to a map 'U $\to$ U $\to$ U'. Functors form a class, in the sense used in computer science, i.e. a standardly employed abstraction or interface. 

The object mappings of functors in Haskell are type formers (e.g. mapping a type of integers to the type of lists of such integers) and these are often used without any reference to the arrow mappings in the code. For each declaration of a functor, the user must code its action on the arrows (a function called 'fmap'), which here are Haskell function terms. It must be noted that all algebraic laws (e.g. compatibility of functors with function concatenation in the sense of the definition of functors) are not checked or enforced by the Haskell compiler. That is to say, in this language, its written code is only checked for the arrow mapping of a user defined functor is well-typed, while the user could, in principle, declare a "'Functor'" that doesn't actually fulfill all the defining properties of a functor. 
Today, there are also software modules that implement category theoretical notions more abstractly, i.e. one may set up categories in which the arrows are not necessarily Haskell functions.

Haskell is famous for its use of [[monads (in computer science)]], a subclass of functors. Here, the unit (called 'return') and co-unit must be implemented. However, stemming from the way that monads are actually used by programmers, it is standard to implement the function 'return' and another function called 'bind', with infix '>>=', which is a composite of the functor and the two natural transformations and which can be derived from the others.

### Lifted products

Expanding on the caveat above about `undefined`, the built-in products in Haskell are "lifted", they are not exactly categorical products. For example, if we define 
``` 
loop = loop 
```
then the element `loop :: ((),())` is observably different from `(loop,loop) :: ((),())`. 
To see this, note that 
```
(\(_,_)->()) (loop,loop)
```
terminates but 
```
(\(_,_)->()) loop
```
does not terminate.


As a result, the built-in [[currying]] is not strictly speaking a bijection in Haskell. For example, 
```
(uncurry . curry) (\(_,_)->()) loop
```
terminates but 
```
(\(_,_)->()) loop
```
does not terminate. 

It _is_ consistent to have a cartesian closed category with a recursion operator, and indeed most semantic models of recursion in a call-by-name setting do actually form cartesian closed categories. In fact Haskell does provide "unboxed tuple" types, which are more like categorical products, but these are not so widely used. 


### Similar and related software

Languages similar to Haskell but refining it from plain [[type theory]] to [[dependent type theory]] include

* [[Coq]], [[Agda]] and Idris

Coq and Agda is consistent with [[Homotopy type theory]], while Idris [is not](http://cstheory.stackexchange.com/questions/27979/formalizing-homotopy-type-theory-in-idris/28013#28013).

A wiki platform based on Haskell, running texmath

* [gitit](https://github.com/jgm/gitit) 

## Related concepts

* [[domain specific embedded programming language]]

[[!include proof assistants and formalization projects -- list]]

## References

### General

* Haskell, language and library specification, [wiki](http://www.haskell.org/haskellwiki/Language_and_library_specification)

* [haskellwiki](http://www.haskell.org/haskellwiki/Haskell), [haskell platform](http://www.haskell.org/platform) 

Discussion of the [[category]] of Haskell [[types]] (see at _[[relation between category theory and type theory]]_ and at _[[monad (in computer science)]]_) is in

* WikiBooks, _[Haskell/Category](http://en.wikibooks.org/wiki/Haskell/Category_theory)_
 
### Mathematics in Haskell
 {#ReferencesMathematicsInHaskell}

The use of Haskell in [[mathematics]] is discussed in the following references.

* haskellwiki, _[Haskell and mathematics](http://www.haskell.org/haskellwiki/Haskell_and_mathematics)_

* category theory, in haskellwiki, [wiki](http://www.haskell.org/haskellwiki/Category_theory)

* Jan van Eijck, _[The Haskell Road to Logic, Maths and Programming](http://homepages.cwi.nl/~jve/HR)_

* Dan Piponi, ["What Category do Haskell Types and Functions Live In?"](http://blog.sigfpe.com/2009/10/what-category-do-haskell-types-and.html), October 13, 2009.