+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Split coequalizers
* table of contents
{: toc}

## Definition

For purposes of this page, a [[fork]] (some might say a "cofork") in a [[category]] $C$ is a diagram of the form

$$ A \;\underoverset{f}{g}{\rightrightarrows}\; B \overset{e}{\rightarrow} C $$

such that $e f = e g$.  A **split coequalizer** is a fork together with morphisms $s\colon C\to B$ and $t\colon B\to A$ as below

\begin{center}\begin{tikzcd}
A \ar[r,shift left,"f"] \ar[r,shift right,"g"'] &
B \ar[r,"e"] \ar[l,bend right=40,"t"'] & 
C \ar[l,bend right=40,"s"']
\end{tikzcd}\end{center}

such that $e s = 1_C$, $s e = g t$, and $f t = 1_B$.  This is equivalent to saying that the morphism $(f,e)\colon g \to e$ has a [[section]] in the [[arrow category]] of $C$.

## Related concepts

### As coequalizers and absolute coequalizers
 {#AsCoequalizers}

The name "split coequalizer" is appropriate, because in any split coequalizer diagram, the morphism $e$ is necessarily a [[coequalizer]] of $f$ and $g$.  For given any $h\colon B\to D$ such that $h f = h g$, the composite $h s$ provides a factorization of $h$ through $e$, since $h s e = h g t = h f t = h$, and such a factorization is unique since $e$ is (split) [[epimorphism|epic]].  

In fact, a split coequalizer is not just a coequalizer but an [[absolute coequalizer]]: one preserved by all [[functors]].  This is meant in the sense in which any functor can "preserve a coequalizer", namely that $F e$ is a coequalizer of $F f$ and $F g$ for any functor $F$.  Of course this happens *because* $F$ also preserves the splitting morphisms $s$ and $t$, but those are not part of the coequalizer diagram that is "preserved" in this statement.

### Contractible pairs

On the other hand, suppose we are given only $f,g\colon A\to B$ and $t\colon B\to A$ such that $f t = 1_B$ and $g t f = g t g$ (which is certainly the case in any split coequalizer, since $g t f = s e f = s e g = g t g$).  Such a situation is sometimes called a **contractible pair**.  In this case, any coequalizer of $f$ and $g$ is split, for if $e\colon B\to C$ is a coequalizer of $f$ and $g$, then the equation $g t f = g t g$ implies, by the universal property of $e$, a unique morphism $s\colon C\to B$ such that $s e = g t$, whence $e s e = e g t = e f t = e$ and so $e s = 1_C$ since $e$ is epic.

Similarly, if $e\colon B\to C$ [[split idempotent|splits]] the [[idempotent]] $g t$ with section $s\colon C\to B$, so that $e s = 1$ and $s e = g t$, then we have
$$ e g = e s e g = e g t g = e g t f = e s e f = e f $$
and the other identities are obvious; thus $e$ is a split coequalizer of $f$ and $g$.

### Split epimorphisms

Dually, if $e\colon B\to C$ is a [[split epimorphism]], with a splitting $s\colon C\to B$, say, then $e$ is a split coequalizer of $B \;\underoverset{1}{s e}{\rightrightarrows}\; B$, the morphism $t$ being the identity.

Moreover, $e$ is also the split coequalizer of its [[kernel pair]], if the latter exists.  For if $A \;\underoverset{f}{g}{\rightrightarrows}\; B$ is this kernel pair, then the two maps $s e, 1_B \colon B\to B$ satisfy $e \circ s e = e \circ 1_B$, and hence induce a map $t\colon B\to A$ such that $f t = 1_B$ and $g t = s e$.


## Examples

### Beck coequalizer for algebras over a monad
 {#BeckCoequalizerForAlgebrasOverAMonad}

The "ur-example" of a split coequalizer is the following.  Let $A$ be an [[algebra for a monad|algebra]] for the [[monad]] $T$ on the category $C$, with structure map $a\colon T A \to A$.  Then the diagram

$$ T^2 A \;\underoverset{T a}{\mu_A}{\rightrightarrows}\; T A \overset{a}{\rightarrow} A\, , $$

called the [[canonical presentation]] of the algebra $(A,a)$, is a split coequalizer in $C$ (and a [[reflexive coequalizer]] in the [[Eilenberg-Moore category|category of]] $T$-algebras).  The splittings are given by $s = \eta_A \colon A \to T A$ and $t = \eta_{T A} \colon T A \to T^2 A$.  (Here $\mu$ and $\eta$ are the multiplication and unit of the monad $T$.)

This split coequalizer figures prominently in Beck's [[monadicity theorem]], whence also called the _[[Beck coequalizer]]_.

See also at _[Eilenberg-Moore category -- As a colimit completion of the Kleisli category](Eilenberg-Moore+category#AsColimitCompletionOfKleisliCategory)_.

## Related concepts

See also [[split equalizer]].

## References

* {#MacLane71} [[Saunders MacLane]], §VI.6 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5**  Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


[[!redirects split coequalizer]]
[[!redirects split coequalizers]]
[[!redirects split coequaliser]]
[[!redirects split coequalisers]]
[[!redirects contractible pair]]
[[!redirects contractible pairs]]