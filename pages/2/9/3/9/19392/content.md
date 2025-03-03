
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

Call-by-push-value (CBPV) is a [[type theory]] and [[programming language]] paradigm which has full embeddings of [[call-by-value]] and [[call-by-name]] lambda-calculi, including their [[operational semantics]], [[equational theories]] and [[denotational semantics|denotational]] models.

Its [[semantics]] decomposes the semantics of [[monad (in computer science)|effectful languages]] using a [[strong monad]] into a [[strong adjunction]]. Then the embeddings of call-by-value and call-by-name correspond to the construction of [[Kleisli category|Kleisli and co-Kleisli categories]] from an adjunction.

## Syntax

### Judgmental Structure

CBPV has two "kinds" of [[types]]: value types --- written $A,A',A_i$ --- and computation types --- written $B,B',B_i$. As originally presented. there are 3 term [[judgments]] of CBPV: Values, Terms, and Stacks.

The value judgment is an ordinary simple type theory. A context $\Gamma$ is a sequence of value typed variables $x_1:A_1,\ldots$ and the judgment $\Gamma \vdash V : A$ admits symmetry, contraction, weakening and the corresponding substitution principle: if for every $x_i:A_i$ in $\Gamma$, $\Gamma' \vdash \gamma(x_i) : A_i$, then there is a value $\Gamma' \vdash V[\gamma] : A$.

The term judgment has again a value typed context $\Gamma$, but the output type is a computation type $\Gamma \vdash M : B$. Again it admits symmetry, contraction and weakening, and admits a substitution principle on its inputs, if we have a $\gamma$ as above, then there is a term $\Gamma' \vdash M[\gamma] : B$.

Finally the stack judgment has a value context $\Gamma$ as input, but also a computation type as input and output: $\Gamma | B \vdash S : B'$. Stacks have an admissible substitution operation $S[\gamma]$ as above. Stacks also have a composition operation: if $\Gamma | B \vdash S : B'$ and $\Gamma | B' \vdash S' : B''$ then $\Gamma | B \vdash S'[S] : B''$, which is associative and has a unit: the empty stack $\Gamma | B \vdash \bullet : B$. Finally, stacks have an action on terms: if $\Gamma \vdash M : B$ and $\Gamma | B \vdash S : B'$ then $\Gamma \vdash S[M] : B'$, which is associative with $\bullet$ as identity.

We can get a slightly simpler presentation by combining the stack and term judgments into a single term judgment with a [[stoup]]: a context that is either a single type $B$ or empty. Then a term as before is a term typed with the empty stoup and a stack is a term typed with a full stoup. This has the benefit of combining the action of stacks on terms and the composition of stacks as one operation. Below we write a stoup as $\Delta$, and if it is empty we don't write it at all.

### Type Structure

Call-by-push-value is characterized not just by its judgmental structure, but by a specific *choice* of which connectives to use. Except for the shifts $F,U$, all value type connectives are left adjoints, and all computation type connectives are right adjoints.

For this reason, some connectives are definable from the judgments but excluded because they violate this discipline. These are a tensor product $A \otimes B$ which is a computation type, a unit $I$ computation type, and a linear function space $B \multimap B'$ which is a computation type. When these are added, the system is called the [Enriched Effect Calculus](#EEC) (modulo some superficial syntactic differences).

#### Shifts

The shift types express the adjunction between values and stacks.
The type $UB$ is a value type that is pronounced as "thunk of $B$", and can be thought of as the type of [[closures]] that when called behave as $B$.
It is a value type, but a right adjoint, with invertible introduction rule

$$ \frac { \Gamma \vdash M : B }
         { \Gamma \vdash thunk M : UB } $$

and elimination rule:

$$ \frac { \Gamma \vdash V : UB }
         { \Gamma \vdash force V : B } $$

With $\beta$ rule $force thunk M = M$ and $\eta$ rule $V = thunk force V$.

The type $FA$ is a computation type that is the type of "returners of $A$s".
It is a computation type, but a left adjoint, with invertible elimination rule that enables the sequencing of effects:

$$ \frac { \Gamma | \Delta \vdash M : F A \qquad \Gamma, x : A \vdash N : B}
         { \Gamma | \Delta \vdash M to x. N : B } $$

with introduction rule: 

$$ \frac {\Gamma \vdash V : A } { \Gamma \vdash return V : F A } $$

with $\beta$ rule $(return V) to x. N = N[V/x]$ and $\eta$ rule that for any stack $\Gamma | F A \vdash S : B$, we have $S = \bullet to x. S[return x]$.

## As an Adjoint Logic

The semantics of Call-by-push-value was originally presented using fibred categories, but we can get a presentation of its semantics in a more multi-categorical flavor by expressing it as an [[adjoint logic]] from a specific mode theory in the sense of [LSR](#LSR).

As a summary, the mode theory of CBPV is the theory of a cartesian monoid acting on a pointed object.
In more detail, we have two modes: $v$ for values and $c$ for computations. Then the $v$ mode is axiomatized as a cartesian monoid $(v,\times,1)$, which gives the value judgment. To axiomatize the term and stack judgments, we add an asymmetric tensor product 

$$a:v,b:c \vdash a\otimes b : c$$

to represent the combined context $\Gamma | B$ and also a "point" for the computation types:

$$\vdash i : c$$

which represents the empty stoup.

To correctly model the substitution structure, we add equations that say that the tensor product constitutes an action of the monoid, i.e., associativity and unitality:

$$(a \times a') \otimes b = a \otimes (a' \otimes b) \qquad 1 \otimes b = b$$

Then for example, the $F$ type above is $F_{x \otimes i}$ and the $U$ type is $U_{x. x \otimes i}$.

Furthermore, the mode theory also gives the "missing" types of the Enriched Effect Calculus. The tensor product is $F_{x \otimes y}$, the unit is $F_{i}$ and the linear function space is $U_{x. x\otimes y}$.

Note that this mode theory is equivalent to the one given for a strong monad in [LSR](#LSR), which instead of the point $i$ adds a morphism $a : v \vdash g(a) : c$, and requires this be a homomorphism of $v$-actions in that

$$ g(a \times b) = a \otimes g(b)$$

However, this is equivalent to our above presentation because for any $a:v$, we have $a = a \times 1$, so $g(a) = g(a \times 1) = a\otimes g(1)$, so $g$ is completely determined by where it takes $1$, so we can axiomatize that directly as the point $i$.

## Related

* The linear term judgment in [[linear-non-linear logic]] can be seen as extending the call-by-push-value stack judgment to allow for "multi-hole" stacks.

## References

* [[Paul-Blain Levy]], [_Call-by-Push-Value: A Subsuming Paradigm_, TLCA 1999](https://link.springer.com/chapter/10.1007/3-540-48959-2_17)

* [[Paul-Blain Levy]], _Adjunction Models for Call-by-push-value with Stacks_, [CTCS version](https://www.cs.bham.ac.uk/~pbl/papers/ctcs02journal.pdf), [EPTCS journal version](https://www.sciencedirect.com/science/article/pii/S1571066104805681), 2003

* {#EEC} Jeff Egger, Rasmus Ejlers Møgelberg and Alex Simpson, [The Enriched Effect Calculus: Syntax and Semantics](https://pdfs.semanticscholar.org/2f3f/21259ffaa5cc56bb280914a028cfed3454e2.pdf), Journal of Logic and Computation, Volume 24.

* {#LSR} [[Daniel Licata]], [[Mike Shulman]], and [[Mitchell Riley]], _A Fibrational Framework for Substructural and Modal Logics (extended version)_, in Proceedings of 2nd International Conference on Formal Structures for Computation and Deduction (FSCD 2017) ([doi: 10.4230/LIPIcs.FSCD.2017.25](http://drops.dagstuhl.de/opus/volltexte/2017/7740/), [pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/lsr17multi-ex.pdf))