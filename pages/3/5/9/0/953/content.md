
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A _Waldhausen category_ $C'$ is a [[homotopical category]] equipped with a bit of extra structure that allows us to consider it as a presentation (via [[simplicial localization]]) of an [[(infinity,1)-category]] $C$ such that the extra structure allows us to conveniently compute the [[K-theory]] [[Grothendieck group]] $\mathbf{K}(C)$ of $C$.

Notably a Waldhausen category provides the notion of co[[fibration sequence]]s, which are crucial structures controlling $\mathbf{K}(C)$. Dual to the discussion at [[homotopy limit]] and [[homotopy pullback]], ordinary [[pushout]]s in Waldhausen categories of the form

$$
 \array{
  A &\hookrightarrow& B
  \\
  \downarrow && \downarrow
  \\
  0 &\to& B//A
 }
$$

with $A \hookrightarrow B$ a special morphism called a Waldhausen cofibration compute _homotopy pushout_s and hence coexact sequences in the corresponding [[stable (infinity,1)-category]].

Using this, the [[Waldhausen S-construction]] on $C'$ is an algorithm for computing the [[K-theory]] spectrum of $C$.

## Definition 

Waldhausen in his work in [[K-theory]] introduced the notion of a category with cofibrations and weak equivalences, nowadays known as _Waldhausen category_. As the original name suggests, this is a category $C$ with zero object $0$, equipped with a choice of two classes of maps $\mathrm{cof}$ of the cofibrations and $w.e.$ of weak equivalences such that

* (C1) all isomorphisms are cofibrations

* (C2) there is a zero object $0$ and for any object $a$ the unique morphism $0\to a$ is a cofibration

* (C3) if $a\hookrightarrow b$ is a cofibration and $a\to c$ any morphism then the pushout $c\to b\cup_a c$ is a cofibration

* (W1) all isomorphisms are weak equivalences

* (W2) weak equivalences are closed under composition (make a subcategory)

* (W3) "glueing for weak equivalences": Given any
commutative diagram of the form 
  $$\array{
  D &\leftarrow& A &\hookrightarrow &B\\
  \downarrow^\sim&& \downarrow^\sim &&\downarrow^\sim\\
  D' &\leftarrow &A' &\hookrightarrow &B'
  }$$
  in which the vertical arrows are weak equivalences and right horizontal maps cofibrations, the induced map
$B\cup_A D\hookrightarrow B'\cup_{A'} D'$
is a weak equivalence. 

The axioms imply that for any cofibration $A\hookrightarrow B$ there is a cofibration sequence $A\hookrightarrow B\to B/A$ where $B/A$ is the choice of the cokernel $B\cup_A 0$.

Given a Waldhausen category $C$ whose weak equivalence classes from a set, one defines $K_0(C)$ as an abelian group whose elements are the weak equivalence classes modulo the relation $[A]+[B/A]=[B]$ for any cofibration sequence $A\hookrightarrow B\to B/A$.

Waldhausen then devises the so called S-construction $C\mapsto S_\bullet C$ from Waldhausen categories to simplicial categories with cofibrations and weak equivalences (hence one can iterate the construction producing multisimplicial categories). 

The [[K-theory space]] of a Waldhausen construction is 
given by formula $\Omega\mathrm{hocolim}_{\Delta^{\mathrm{op}}}([n]\mapsto N_\bullet(w.e.(S_n C)))$, where $\Omega$ is the loop space functor, $N$ is the simplicial [[nerve]], w.e. takes the (simplicial) subcategory of weak equivalence and $[n]\in\Delta$. This construction can be improved (using iterated [[Waldhausen S-construction]]) to the [[K-theory]] $\Omega$-[[spectrum]] of $C$; the K-theory space will be just the one-space of the K-theory spectrum. 

Then the K-groups are the [[homotopy group]]s of the K-theory space.

## Remarks

* The axioms of a Waldhausen category $C$ are very similar to the axioms of a [[category of fibrant objects]] on the [[opposite category]] $C^{op}$ in which the initial object is also terminal. One difference is that the weak equivalences in a Waldhausen category are not required to satisfy [[2-out-of-3]]. For example, Waldhausen gives an example of a Waldhausen category where the weak equivalences are [[simple homotopy equivalences]]. Another difference is in axiom W3, whose analog in a [[category of fibrant objects]] is the axioms that every object has a [[path object]]. It still follows that one has fibration sequences in a [[category of fibrant objects]].


## Examples 

### Waldhausen category of a small abelian category 

For $C$ a [[small category|small]] [[abelian category]] the [[category of chain complexes|category of bounded chain complexes]] $Ch^b(C)$ becomes a Waldhausen category by taking

* a [[weak equivalence]] is a [[quasi-isomorphism]] of chain complexes;

* a cofibration $f : A_\bullet \to X_\bullet$ is a chain morphism that is a [[monomorphism]] in $C$ in each degree $f_n : A_n \to X_n$.


### Waldhausen category of a small exact category 

For $C$ just a [[Quillen exact category]] with ambient [[abelian category]] $\hat C$ there is an analogous, slightly more sophisticated construction of a Waldhausen category structure on $Ch^b(C)$:

* weak equivalences are the morphisms that are [[quasi-isomorphism]]s when regarded as morphisms in $\hat C$;

* the cofibrations are the degreewise _admissible morphisms_, i.e. those morphisms $A \to X$ such that the pushout $A \to X \to A/X$ computed in the ambient [[abelian category]] $\hat C$ is in $C$.

## Related concepts

* [[category with weak equivalences]]

* [[category of fibrant objects]], [[category of cofibrant objects]]

* [[model category]]

## References 

Waldhausen categories are discussed with an eye towards their application in the computation of [[Grothendieck group]]s in [chapter 2](http://www.math.rutgers.edu/~weibel/Kbook/Kbook.II.pdf) of

* [[Charles Weibel]], _The K-book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))

Section 1 of

* [[R. W. Thomason]], Thomas Trobaugh, _Higher algebraic K-theory of schemes and of derived categories_, _The Grothendieck Festschrift_, 1990, 247-435.([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/tt.pdf))

[[!redirects Waldhausen categories]]