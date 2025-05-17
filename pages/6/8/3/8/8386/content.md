
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

> This page is about the concept of polymorphism of declarations in [[computer science]]. For polymorphism of [[type universes]] see instead at *[[universe polymorphism]]*. For the generalisation of *morphisms* introduced by [[Shinichi Mochizuki]], see *[[poly-morphism]]*.

# Polymorphism
* table of contents
{: toc}

## Idea

In [[computer science]], *polymorphism* refers to situations either where the same name is used to refer to more than one [[function]], or where the same function is used at more than one [[type]]. One usually distinguishes these two kinds of polymorphism as  *ad hoc polymorphism* and *parametric polymorphism*, respectively.


## Ad hoc polymorphism

In **ad hoc polymorphism**, one simply defines multiple functions with the same name and different [[types]], relying on the compiler (or, in some cases, the run-time system) to determine the correct function to call based on the types of its arguments and return value.  This is also called **overloading**.  For instance, using a mathematical notation, one might define functions

$$ add : \mathbb{N} \times \mathbb{N} \to \mathbb{N}$$
$$ add : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$$

and then when $add(3,2)$ is invoked, the compiler knows to call the first function since $3$ and $2$ are [[natural numbers]], whereas when $add(4.2,\pi)$ is invoked it calls the second function since $4.2$ and $\pi$ are [[real numbers]].

Note that there is nothing which stipulates that the *behavior* of a class of ad-hocly polymorphic functions with the same name should be at all similar.  Nothing prevents us from defining $ add : \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ to add its arguments but $ add : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ to subtract its arguments.  Of course, it is good programming practice to make overloaded functions similar in their behavior.

In the example above, there might even be a [[coercion]] function $c : \mathbb{N} \to \mathbb{R}$, to be invoked whenever a natural number appears where the compiler expects a real number, giving a [[commutative diagram]]
$$ \array {
   \mathbb{N} \times \mathbb{N}     & \overset{add}\to  & \mathbb{N} \\
   \mathllap{c \times c} \downarrow &                   & \downarrow \mathrlap{c} \\
   \mathbb{R} \times \mathbb{R}     & \underset{add}\to & \mathbb{R}
} $$
But things don\'t always work out this way.


## Parametric polymorphism

In **parametric polymorphism** or **parametricity**, one writes code to define a function *once*, which contains a [[type variable]] that can be instantiated at many different types to produce different functions.  For instance, we can define a function

$$ first : A\times A \to A $$

where $A$ is a type variable (or *parameter*), by

$$ first(x,y) \coloneqq x. $$

Now the compiler automatically instantiates a copy of this function, with identical code, for any type at which it is called.  Thus we can behave as if we had functions

$$ first : \mathbb{N} \times \mathbb{N} \to \mathbb{N}$$
$$ first : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$$

and so on, for any types we wish.  In contrast to *ad hoc* polymorphism, in this case we do have a guarantee that all these same-named functions are doing "the same thing", because they are all instantiated by the same original polymorphic code.

Parametric polymorphism makes sense and is very useful in languages with non-dependent type systems, such as [[Haskell]] and [[Standard ML]].

### Theorems for Free

In type systems with parametric polymorphism, such as [[System F]], there is a family of proofs for every polymorphic type signature which each give an algebraic law for any function with that signature. For example, the type signature $A \times B \to A$ has the [[free theorem]]

$$ \alpha \circ f = f \circ (\alpha \times \beta) $$

for all functions $f$ with that signature ([Wadler 89](#Wadler89), figure 1).

### In dependent type theory

In a [[dependent type theory]] with a [[type universe]] or [[type variables]], our family of functions above would be typed respectively as

$$\Gamma, A:Type \vdash \mathrm{first}(A):A\times A \to A \qquad \mathrm{or} \qquad \Gamma, A \; \mathrm{type} \vdash \mathrm{first}(A): A \times A \to A$$

If the dependent type theory additionally has universe-indexed [[dependent product types]] or [[impredicative polymorphism]] respectively, a parametrically polymorphic family of functions can simply be considered to be a single dependently typed function whose first argument is a type. Thus our function above would be typed as

$$ \mathrm{first} : \prod_{A:Type} A\times A \to A \qquad \mathrm{or} \qquad \mathrm{first} : \prod_{A \; \mathrm{type}} A\times A \to A$$

Examples of parametric polymorphism in dependent type theory include [[axioms]] and [[axiom schemata]], such as [[UIP]] and [[axiom K]], [[excluded middle]], [[axiom of choice]], and the [[type theoretic axiom of replacement|axiom of replacement]] for a [[Tarski universe]]. 

For certain dependent type theories, one can prove that they have parametric polymorphism inside the type theory itself. These are the [[parametric dependent type theories]]. 

## Related concepts

* [[type theory]]

  * [[simple type theory]]

  * **polymorphic type theory**

  * [[dependent type theory]]

  * [[polymorphic dependent type theory]]

* [[logical relations]]

* [[impredicative polymorphism]]

* [[parametric dependent type theory]]

## References

The distinction between ad hoc and parametric polymorphism is originally due to [[Christopher Strachey]]:

* [[Christopher Strachey]], _Fundamental concepts in programming languages_, Lecture Notes from August 1967 (International Summer School in Computer Programming, Copenhagen), later published in Higher-Order and Symbolic Computation, 13, 11-49, 2000. ([pdf](https://www.itu.dk/courses/BPRD/E2009/fundamental-1967.pdf))

Other classic papers include:

* [[John C. Reynolds]], _Towards a Theory of Type Structure_, Lecture Notes in Computer Science 19, 408-425, 1974. ([pdf](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2289&context=compsci))

* [[Robin Milner]], _A Theory of Type Polymorphism in Programming_, Journal of Computer and System Sciences 17, 348-375, 1978. ([pdf](https://courses.engr.illinois.edu/cs421/sp2013/project/milner-polymorphism.pdf))

* [[John C. Reynolds]], _Types, Abstraction, and Parametric Polymorphism_, Information Processing 83, 1983. ([pdf](http://www.cse.chalmers.se/edu/year/2010/course/DAT140_Types/Reynolds_typesabpara.pdf))

Theorems for free were explained in:

* {#Wadler89} [[Philip Wadler]], _Theorems for free!_, in Proceedings of the fourth international conference on Functional programming languages and computer architecture (FPCA 1989). 1989. ([pdf](https://www2.cs.sfu.ca/CourseCentral/831/burton/Notes/July14/free.pdf), [doi:10.1145/99370.99404](https://doi.org/10.1145/99370.99404))

See also the references at *[[parametric dependent type theory]]* for the various notions of parametricity in various kinds of [[dependent type theories]]. 

[[!redirects polymorphism]]
[[!redirects ad hoc polymorphism]]
[[!redirects parametric polymorphism]]
[[!redirects polymorphic]]

[[!redirects parametricity]]
[[!redirects external parametricity]]

[[!redirects polymorphic type theory]]