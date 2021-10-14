
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _reflexive object_ is a model of the pure (untyped) [[lambda calculus]] validating the $\beta$ law, and sometimes also the $\eta$ law.

## Definition

A **reflexive object** in a [[cartesian closed category]] is an [[object]] $U$ equipped with a pair of [[morphisms]]

$$
\array{U & \overset{app}{\underset{lam}{\rightleftarrows}} & U^U} 
$$

(where $(-)^{(-)}$ denotes the [[exponential object]])
such that $app \circ lam = 1$.  

In other words, a reflexive object is an object $U$ together with data $U^U \lhd U$ exhibiting $U^U$ as a [[retract]] of $U$.  

A reflexive object is said to be **extensional** (or "strict") when also $lam \circ app = 1$, so that there is an isomorphism $U^U \cong U$.

Viewed as a model of lambda calculus, the equation $app \circ lam = 1$ of a reflexive object represents $\beta$-equality $(\lambda x.t)(u) = t[u/x]$, while the equation $lam \circ app = 1$ of an extensional reflexive object represents $\eta$-equality $\lambda x.t(x) = t$.

### In a closed (symmetric) monoidal category

The definition has a straightforward generalization to any [[symmetric monoidal closed category]] (i.e., not necessarily [[cartesian monoidal category|cartesian monoidal]]), where we just replace the [[exponential object]] $U^U$ by the [[internal hom]] $[U,U]$.  Indeed, the definition also makes sense in any left-closed or right-closed monoidal category.

A reflexive object in a symmetric monoidal closed category provides a model of [[linear lambda calculus]].

### In a closed monoidal 2-category

The definition of reflexive object also has a natural generalization to any closed monoidal [[2-category]] (or cartesian closed 2-category), where the retraction should be replaced by an [[adjunction]] $app \dashv lam : [U,U] \to U$.  Then the [[counit]] of the adjunction $app \circ lam \Rightarrow 1_{[U,U]}$ models [[beta-reduction]] $(\lambda x.t)(u) \to t[u/x]$, while the [[unit]] $1_U \Rightarrow lam \circ app$ models [[eta-expansion]] $t \to \lambda x.t(x)$.

## Examples

### Terminal object

The [[terminal object]] of a ccc provides a degenerate example of a (extensional) reflexive object, and for cardinality reasons, this is the only reflexive object in [[Set]].

### Scott's $D_\infty$ construction

The first non-degenerate model of untyped lambda calculus was described by [[Dana Scott]] (see [Scott (1970)](#Scott70) and [Scott (1972)](#Scott72)), who solved the cardinality issue by replacing sets with [[algebraic lattices]], and arbitrary set-theoretic functions by [[Scott topology|Scott-continuous]] functions.  The so-called "$D_\infty$" model is built by a limit construction, starting from $D_0 = D$ an arbitrary algebraic lattice, and taking $D_{n+1} = D_n \to D_n$.

### Enumeration operator model

Scott later gave a more concrete model of lambda calculus in [Scott (1976)](#Scott76), defining a reflexive object with carrier the lattice $P\omega$ of all [[subsets]] of the non-negative integers, and with the maps $app$ and $lam$ (there called "fun" and "graph") defined as follows:

$$app(u)(x) = \{m \mid \exists e_n \subseteq x. (n,m) \in u\}$$

$$lam(f) = \{(n,m) \mid m \in f(e_n)\}$$

Here $e_n$ stands for the set whose elements are the exponents in the binary expansion of $n$ (thus $e_n$ is the $n$th subset in the standard enumeration of finite subsets of $\omega$), while "$(n,m)$" stands for the standard enumeration of pairs of integers

$$(n,m) = \frac{1}{2}(n+m)(n+m+1)+m$$

Note that the enumeration operator model is not "extensional" in the sense that it only validates $\eta$-conversion as an inclusion $u \subseteq \ell(a(u))$, which is not an equality in general.

### Scott's representation theorem

[Scott (1980)](#Scott80) proved a sort of representation theorem for pure lambda calculus, showing that _any_ "type-free theory" (a.k.a., [[lambda theory]]) can be realized as a reflexive object.  He began by constructing a category whose objects are the closed lambda terms $A$ such that one can prove $A = \lambda x.A(A(x))$, and whose morphisms $f : A \to B$ are (equivalence classes of) closed terms $f$ such that one can prove $f = \lambda x.B(f(A(x)))$ (cf. [[Karoubi envelope]]), with identity and composition defined by
$$
1_A = A
\qquad
f \circ g = \lambda x.f(g(x))
$$
This category is cartesian closed, where products and exponentials are defined (on objects) by
$$
A \times B = \lambda u\lambda z.z(A(u(\lambda x\lambda y.x)))(B(u(\lambda x\lambda y.y))) 
\qquad
A \to B = \lambda f.B \circ f \circ A
$$
Now, the identity term $U = \lambda x.x$ lives inside this category since obviously $U = U\circ U$, and moreover, every object $A$ is a retract of $U$, since $A : A \to U$ and $A : U \to A$ and $A \circ A = A = 1_A$. Thus, $U$ equipped with its retraction from $U \to U$ is a reflexive object.

A more abstract analysis of Scott's representation theorem appears in [Hyland (2013)](#Hyland13).

### Higher-order abstract syntax

Another way of looking at the _free_ cartesian closed category containing a reflexive object is as a representation of pure lambda terms (up to $\beta$-equality) in the style of so-called [[higher-order abstract syntax]].  The operation $app : U \to U^U$ is the [[currying|curried]] form of application, while the operation $lam : U^U \to U$ represents lambda abstraction.  The [[global elements]] of $U$ can be interpreted as closed lambda terms, and more generally, morphisms $U^n \to U$ can be interpreted as terms with $n$ free variables.

## References

Dana Scott's original work on lattice models of the lambda calculus can be found in:

* {#Scott70} Dana Scott. Outline of a Mathematical Theory of Computation. In _4th Annual Princeton Conference on Information Sciences and Systems_, pages 169-176, 1970. ([pdf](https://ropas.snu.ac.kr/~kwang/520/readings/sco70.pdf))

* {#Scott72} Dana Scott. Continuous Lattices. _Toposes, Algebraic Geometry and Logic_ (ed.: E. Lawvere), pages 97-136, 1972. ([pdf](https://www.cs.ox.ac.uk/files/3229/PRG07.pdf))

* {#Scott76} Dana Scott. Data types as lattices. _SIAM Journal of Computing_, 5(3):522--587, September 1976. ([pdf](https://www.cs.ox.ac.uk/files/3287/PRG05.pdf))

Scott made the underlying categorical structure explicit in a later paper, where he introduced the definition of a reflexive object in a ccc, and proved a representation theorem for theories of pure lambda calculus:

* {#Scott80} Dana Scott. Relating theories of the $\lambda$-calculus. In _To H.B. Curry: Essays on Combinatory Logic, Lambda-Calculus and Formalism_ (eds. Hindley and Seldin), Academic Press, 403--450, 1980.

For a modern analysis of Scott's representation theorem, see:

* {#Hyland13} [[Martin Hyland]]. _Classical lambda calculus in modern dress_ Mathematical Structures in Computer Science, 27(5) (2017) 762-781. doi:[10.1017/S0960129515000377](). [arxiv:1211.5762](http://arxiv.org/abs/1211.5762)

* {#Hyland14} [[Martin Hyland]], _Towards a Notion of Lambda Monoid_ , Electronic Notes in Theoretical Computer Science **303** (2014) pp.59-77, doi:[10.1016/j.entcs.2014.02.004](https://doi.org/10.1016/j.entcs.2014.02.004)

[[2-category|Bicategorical]] and [[monoidal category|monoidal]] generalizations of the notion of reflexive object are discussed in:

* [[R. A. G. Seely]]. _Modelling Computations : a 2-categorical Framework_. LICS 1987. ([pdf](http://www.math.mcgill.ca/rags/WkAdj/LICS.pdf))

* [[Bart Jacobs]]. *Semantics of lambda-I and of other substructure lambda calculi*, in:  M. Bezem and J.F. Groote (eds.) _Typed Lambda Calculi and Applications_, Springer
LNCS 664, 1993, p. 195-208 ([doi:10.1007/BFb0037107](https://doi.org/10.1007/BFb0037107))

* [[Noam Zeilberger]], *Linear lambda terms as invariants of rooted trivalent maps*, Journal of Functional Programming, 26, e21  2016 ([doi:10.1017/S095679681600023X](https://doi.org/10.1017/S095679681600023X), [arXiv:1512.06751](http://arxiv.org/abs/1512.06751))

## Related concepts

* [[lambda calculus]]
* [[domain theory]]
* [[lambda theory]]