+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Lax-idempotent 2-adjunctions

* automatic table of contents goes here
{:toc}

## Idea

A [[lax-idempotent 2-monad]] generalizes the notion of [[idempotent monad]] to 2-categories by replacing inverses with adjoints.  A **lax-idempotent 2-adjunction** (or **KZ 2-adjunction**) similarly generalizes the notion of [[idempotent adjunction]], and is related to lax-idempotent 2-monads in the same way that idempotent adjunctions are related to idempotent monads.

## Definition

We will need to use all three kinds of composition in the 3-category $2 Cat$.  We write composition along 0-cells (2-categories) with juxtaposition.  We write composition along 1-cells (2-functors) with a dot; this is of course composition along 0-cells *in* a 2-category.  And we write composition along 2-cells (transformations) with $\circ$, which is composition along 1-cells *in* a 2-category.

Let $F : C \rightleftarrows D : G$ be a [[2-adjunction]] with unit $\eta: 1_C \to G F$ and counit $\epsilon: F G \to 1_D$.  (For simplicity, we will assume it is a strict 2-adjunction, but the same definitions and proofs work in the pseudo case with some equalities replaced by isomorphisms.)  This 2-adjunction is said to be **lax-idempotent** if one (hence all) of the following equivalent conditions hold.

1. The triangle identity $1_F = \epsilon F . F\eta$ is the unit of an adjunction $F\eta \dashv \epsilon F$.

2. The induced equality $1_{G F} = G \epsilon F . G F\eta$ is the unit of an adjunction $G F\eta \dashv G \epsilon F$.

3. The induced 2-monad $G F$ is [[lax-idempotent 2-monad|lax-idempotent]].

4. There is a modification $\delta : G F \eta \to \eta G F$ such that $\delta \circ \eta = 1$ and $(G\epsilon F) \circ \delta = 1$.

5. There is a modification $\delta' : G F \eta G \to \eta G F G$ such that $\delta' \circ (\eta G) = 1$ and $(G\epsilon F G) \circ \delta' = 1$.

6. The triangle identity $G \epsilon . \eta G$ is the counit of an adjunction $G \epsilon \dashv \eta G$.

7. The induced equality $F G \epsilon . F \eta G$ is the counit of an adjunction $F G \epsilon \dashv F \eta G$.

8. The induced 2-comonad $F G$ is colax-idempotent.

9. There is a modification $\delta : \epsilon F G \to F G \epsilon$ such that $\epsilon \circ \delta = 1$ and $\delta \circ (F\eta G) = 1$.

10. There is a modification $\delta' : G \epsilon F G \to G F G \epsilon$ such that $(G \epsilon) \circ \delta = 1$ and $\delta \circ (G F\eta G) = 1$.

+-- {: .proof}
###### Proof of equivalence
By duality, it suffices to prove that $1\Rightarrow 2 \Rightarrow 3 \Rightarrow 4 \Rightarrow 5 \Rightarrow 6$.  Of these, $1\Rightarrow 2$ and $4 \Rightarrow 5$ are obvious by whiskering.  And since $G\epsilon F$ is the multiplication of the 2-monad $G F$, a standard fact about [[lax-idempotent 2-monads]] gives $2\Leftrightarrow 3 \Leftrightarrow 4$.

Thus, it remains to show $5 \Rightarrow 6$.  We take the unit of the desired adjunction to be
$$
\begin{aligned}
  1
  &\overset{triangle}{=} G F G \epsilon . G F \eta G\\
  &\xrightarrow{\delta'} G F G \epsilon . \eta G F G\\
  &\overset{naturality}{=} \eta G . G \epsilon
\end{aligned}
$$
The two triangle identities for this putative adjunction follow from the two axioms assumed for $\delta'$.
=--

Note that when $C$ and $D$ are locally [[discrete category|discrete]], hence just 1-categories, this reduces to the usual characterization of [[idempotent adjunctions]].

In contrast to that situation, however, the lax-idempotent situation is of interest even when the adjunction is monadic or comonadic.  In the monadic case, the implication $3\Rightarrow 8$ means that the induced 2-comonad on the 2-category of algebras for a lax-idempotent 2-monad is colax-idempotent.  Its (pseudo) coalgebras are the [[continuous algebras]] for the original 2-monad.

## References

* [[Marta Bunge]] and [[Jonathon Funk]], *Singular Coverings of Toposes*.  In this book the notion is called a "KZ-adjointness" and defined by both (1) *and* (6).

[[!redirects lax-idempotent 2-adjunction]]
[[!redirects lax-idempotent 2-adjunctions]]
[[!redirects lax idempotent 2-adjunction]]
[[!redirects lax idempotent 2-adjunctions]]
[[!redirects KZ 2-adjunction]]
[[!redirects KZ 2-adjunctions]]
[[!redirects Kock-Zoberlein 2-adjunction]]
[[!redirects Kock-Zoberlein 2-adjunctions]]
