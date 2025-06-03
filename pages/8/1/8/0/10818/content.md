+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

* automatic table of contents goes here
{:toc}

## Idea

A [[lax-idempotent 2-monad]] generalizes the notion of [[idempotent monad]] to [[2-categories]] by replacing [[inverse morphism|inverses]] with [[adjoints]].  A **lax-idempotent 2-adjunction** (or **KZ 2-adjunction**) similarly generalizes the notion of [[idempotent adjunction]], and is related to lax-idempotent [[2-monads]] in the same way that [[idempotent adjunctions]] are related to [[idempotent monads]].

## Definition

We will need to use all three kinds of composition in the 3-category $2 Cat$.  We write composition along 0-cells (2-functors, denoted with upper case Latin letters) with juxtaposition.  We write composition along 1-cells (functors, denoted with lower case Greek letters) with a dot; this is of course composition along 0-cells *in* a 2-category.  And we write composition along 2-cells (transformations, denoted with lower case Latin letters) with $\circ$, which is composition along 1-cells *in* a 2-category.

Let $F : C \rightleftarrows D : G$ be a [[2-adjunction]] with unit $\eta: 1_C \to G F$ and counit $\epsilon: F G \to 1_D$.  (For simplicity, we will assume it is a strict 2-adjunction, but the same definitions and proofs work in the pseudo case with some equalities replaced by isomorphisms.)
Write $M = GF$ and $\mu = G \epsilon F : M^2 \to F$ and $C = FG$ and $\delta = F \eta G : C \to C^2$.

The 2-adjunction is said to be **lax-idempotent** if one (hence all) of the following equivalent conditions hold (of which the latter 7 are dual to the former 7; the duality involves reversing 2-cells).

1. The triangle identity $1_F = \epsilon F . F\eta$ is the unit of an adjunction $F\eta \dashv \epsilon F$.

2. The induced equality $1_{G F} = G \epsilon F . G F\eta$ is the unit of an adjunction $G F\eta \dashv G \epsilon F$.

   In monad notation: the induced equality $1_M = \mu . M \eta$ is the unit of an adjunction $M \eta \dashv \mu$.

3. The induced equality $1_{F G} = \epsilon F G . F \eta G$ is the unit of an adjunction $F \eta G \dashv \epsilon F G$.

   In comonad notation: the induced equality $1_C = \epsilon C . \delta$ is the unit of an adjunction $\delta \dashv \epsilon C$.

4. The induced 2-monad $M = G F$ is [[lax-idempotent 2-monad|lax-idempotent]], meaning that every strict Eilenberg-Moore algebra $(A, \alpha)$ has the property that the identity $\alpha . \eta_A=1_A$ is the counit of an adjunction $\alpha \dashv \eta_A$.

5. There is a modification $w : G F \eta \to \eta G F$ such that $w . \eta = 1$ and $(G\epsilon F) . w = 1$.

   In monad notation: there is a modification $w : M \eta \to \eta M$ such that $w . \eta = 1$ and $\mu . w = 1$.

6. There is a modification $w' : G F \eta G \to \eta G F G$ such that $w' . (\eta G) = 1$ and $(G\epsilon F G) . w' = 1$.

7. There is a modification $w'' : F G F \eta \to F \eta G F$ such that $w'' . (F \eta) = 1$ and $(F G \epsilon F) . w'' = 1$.

And the duals (which we will refer to below using a prime, i.e. 1'-7'):

1. The triangle identity $G \epsilon . \eta G = 1_G$ is the counit of an adjunction $G \epsilon \dashv \eta G$.

2. The induced equality $F G \epsilon . F \eta G = 1_{F G}$ is the counit of an adjunction $F G \epsilon \dashv F \eta G$.

   In comonad notation: the induced equality $C \epsilon . \delta = 1_C$ is the counit of an adjunction $C \epsilon \dashv \delta$.

3. The induced equality $G \epsilon F . \eta G F = 1_{G F}$ is the counit of an adjunction $G \epsilon F \dashv \eta G F$.

   In monad notation: the induced equality $\mu . \eta M = 1_M$ is the counit of an adjunction $\mu \dashv \eta M$.

4. The induced 2-comonad $F G$ is colax-idempotent, meaning that every strict Eilenberg-Moore coalgebra $(Z, \zeta)$ has the property that the identity $1_Z = \epsilon_Z . \zeta$ is the unit of an adjunction $\zeta \dashv \epsilon_Z$.

5. There is a modification $v : \epsilon F G \to F G \epsilon$ such that $\epsilon . v = 1$ and $v . (F\eta G) = 1$.

   In comonad notation: there is a modification $v : \epsilon C \to C \epsilon$ such that $\epsilon . v = 1$ and $v . \delta = 1$.

6. There is a modification $v' : \epsilon F G F \to F G \epsilon F$ such that $(\epsilon G) . v' = 1$ and $v' . (F \eta G F) = 1$.

7. There is a modification $v'' : G \epsilon F G \to G F G \epsilon$ such that $(G \epsilon) . v'' = 1$ and $v'' . (G F\eta G) = 1$.

+-- {: .proof}
###### Proof of equivalence

First of all, note that, by uniqueness of the left/right adjoint, most of the properties listed are (essentially) mere propositions. So we will content ourselves with proving logical equivalence.

We first prove $1 \Rightarrow 2 \Rightarrow 5 \Rightarrow 6 \Rightarrow 1'$, which by duality implies that 1, 2, 5, 6, 1', 2', 5' and 6' are equivalent.

* ($1 \Rightarrow 2$) Trivial by whiskering.

* ($2 \Rightarrow 5$) We have $M \eta \dashv \mu$ with unit $h = 1 : 1_M \to \mu . M \eta$ and counit $e : M \eta . \mu \to 1_{M^2}$. Let $w = e . \eta M : M \eta \to \eta M$. This satisfies the equations:

  * $w . \eta = e . \eta M . \eta = e . M \eta . \eta = (M \eta . h)^{-1} . \eta = 1_{M \eta . \eta}$ by an adjunction law.
  
  * $\mu . w = \mu . e . \eta M = (h . \mu)^{-1} . \eta M = 1_{\mu . \eta M} = 1_{1_M}$.
  
* ($5 \Rightarrow 6$) Trivial by whiskering.

* ($6 \Rightarrow 1'$) We take the unit $h : 1_{G F G} \to \eta G . G \epsilon$ of the desired adjunction to be
  $$
  \begin{aligned}
    1
    &\overset{triangle}{=} G F G \epsilon . G F \eta G\\
    &\xrightarrow{G F G \epsilon . w'} G F G \epsilon . \eta G F G\\
    &\overset{naturality}{=} \eta G . G \epsilon
  \end{aligned}
  $$
  This satisfies the required triangle identities:

  * $G \epsilon . h = G \epsilon . G F G \epsilon . w' = G \epsilon . G \epsilon F G . w' = G \epsilon . 1 = 1$,
  
  * $h . \eta G = G F G \epsilon . w' . \eta G = G F G \epsilon . 1 = 1$.

We now prove $1 \Rightarrow 3 \Rightarrow 5'$, adding $3$ and $3'$ to the set of equivalent properties.

* ($1 \Rightarrow 3$) Trivial by whiskering.

* ($3 \Rightarrow 5'$) We have $\delta \dashv \epsilon C$ with unit $h = 1 : 1_C \to \epsilon C . \delta$ and counit $e : \delta . \epsilon C \to 1_{C^2}$. Let $v = C \epsilon . e$. This satisfies the equations:

  * $\epsilon . v = \epsilon . C \epsilon . e = \epsilon . \epsilon C . e = \epsilon . (h . \epsilon C)^{-1} = 1_{\epsilon . \epsilon C}$.
  
  * $v . \delta = C \epsilon . e . \delta = C \epsilon . (\delta . h)^{-1} = 1_{1_C}$.
  
We now prove $5 \Rightarrow 7 \Rightarrow 1$, adding $7$ and $7'$ to the set of equivalent properties.

* ($5 \Rightarrow 7$) Trivial by whiskering.

* ($7 \Rightarrow 1$) We take the counit $e : F \eta . \epsilon F \to 1_{F G F}$ of the desired adjunction to be
  $$
  \begin{aligned}
    F \eta . \epsilon F
    &\overset{naturality}{=} \epsilon F G F . F G F \eta \\
    &\xrightarrow{\epsilon F G F . w''} \epsilon F G F . F \eta G F \\
    &\overset{triangle}{=} 1
  \end{aligned}
  $$
  This satisfies the required triangle identities:
  
  * $\epsilon F . e = \epsilon F . \epsilon F G F . w'' = \epsilon F . F G \epsilon F . w'' = \epsilon F . 1 = 1$,
  
  * $e . F \eta = \epsilon F G F . w'' . F \eta = \epsilon F G F . 1 = 1$.
  
Finally, we prove that $3'$ is equivalent to $4$ (hence dually, $3$ is equivalent to $4'$).

* ($3' \Rightarrow 4$) Let $(A, \alpha)$ be an algebra. Then $\alpha . \eta_A = 1_A$.
  We will carry over the structure of $(MA, \mu_A)$ by conjugating with $\alpha . {-} . \eta_A$.
  For $MA$, we have
  
  * $e_A = 1_A : \mu_A . \eta_{MA} \to 1_{MA}$,
  
  * $h_A : 1_{M^2 A} \to \eta_{MA} . \mu_A$.
  
  Define
  
  * $h' = M \alpha . h_A . M\eta_A : 1_{MA} = M \alpha . M\eta_A \to M \alpha . \eta_{MA} . \mu_A . M\eta_A = M \alpha . \eta_{MA} = \eta_A . \alpha$.
  
  This satisfies the adjunction laws:
  
  * $\alpha . h' = \alpha . M \alpha . h_A . M\eta_A = \alpha . \mu_A . h_A . M\eta_A = \alpha . (e_A . \mu_A)^{-1} . M\eta_A = \alpha . 1 . M\eta_A = 1$.
  
  * $h' . \eta_A = M \alpha . h_A . M\eta_A . \eta_A = M \alpha . h_A . \eta_{MA} . \eta_A = M \alpha . (\eta_{MA} . e_A)^{-1} . \eta_A = M \alpha . 1 . \eta_A = 1$.

* ($4 \Rightarrow 3'$) This is immediate, since $(MX, \mu_X)$ is always a strict Eilenberg-Moore algebra.

=--

Note that when $C$ and $D$ are locally [[discrete category|discrete]], hence just 1-categories, this reduces to the usual characterization of [[idempotent adjunctions]].

In contrast to that situation, however, the lax-idempotent situation is of interest even when the adjunction is monadic or comonadic.  In the monadic case, the implication $4 \Rightarrow 4'$ means that the induced 2-comonad on the 2-category of algebras for a lax-idempotent 2-monad is colax-idempotent.  Its (pseudo) coalgebras are the [[continuous algebras]] for the original 2-monad.

## References

As "KZ-adjunctions":

* J. Meseguer, U. Montanari, and V. Sassone. *ω-Inductive completion of monoidal categories and infinite petri net computations*. (1993) ([pdf](https://eprints.soton.ac.uk/261872/1/w-ind-compl.pdf))

As "KZ-adjointness" (defined by both (1) *and* (6)):

* [[Marta Bunge]] and [[Jonathon Funk]], *Singular Coverings of Toposes*.

As "lax idempotent 2-adjunctions":

* [[Maria Manuel Clementino]] and [[Fernando Lucatelli Nunes]], §3 of: _Lax comma 2-categories and admissible 2-functors_. [arXiv:2002.03132](https://arxiv.org/abs/2002.03132) (2020).

[[!redirects lax-idempotent 2-adjunction]]
[[!redirects lax-idempotent 2-adjunctions]]
[[!redirects lax idempotent 2-adjunction]]
[[!redirects lax idempotent 2-adjunctions]]
[[!redirects KZ 2-adjunction]]
[[!redirects KZ 2-adjunctions]]
[[!redirects Kock-Zoberlein 2-adjunction]]
[[!redirects Kock-Zoberlein 2-adjunctions]]
