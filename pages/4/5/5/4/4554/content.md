
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
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

The _factorisation lemma_ ([Brown 73](#Brown73), prop. \ref{TheFactorizationLemma} below) is a fundamental tool in the theory of [[categories of fibrant objects]] ([[formal dual|dually]]: [[cofibration category|of cofibrant objects]]). It mimics one half of the _factorisation axioms_ in a [[model category]] in that it asserts that every morphisms may be factored as, in particular, a weak equivalence followed by a fibration.

A key corollary of the factorization lemma is the statement, widely known as _Ken Brown's lemma_ (prop. \ref{KenBrownLemma} below) which says that for a functor from a category of fibrant objects  to be a [[homotopical functors]], it is sufficient already that it sends acyclic fibrations to weak equivalences. 

## Factorisation lemma

Let $\mathcal{C}$ be a [[category of fibrant objects]].

+-- {: .num_lemma }
###### Lemma

Given any [[product]]
  $$ X \overset{p_{X}}{\leftarrow} X \times Y
       \overset{p_{Y}}{\rightarrow} Y $$
in $\mathcal{C}$, the [[projections]] $p_{X}$ and $p_{Y}$ are [[fibrations]].

=--

+-- {: .proof}
###### Proof

By one of the axioms for a category of fibrant objects, $\mathcal{C}$ has a final object $1$. We have the following.

1) The following diagram in $\mathcal{C}$ is a cartesian square.

$$
   \array{
      X \times Y               &  \overset{p_{Y}}{\to} & Y \\
      p_{X} \downarrow &                                      & \downarrow  \\
      X                            & \to                                 & 1 \\ 
   }
$$

2) By one of the axioms for a category of fibrant objects, the arrows $Y \to 1$ and $X \to 1$ are fibrations. 

By one of the axioms for a category of fibrant objects, it follows from 1) and 2) that $p_{X}$ and $p_{Y}$ are fibrations.

=--

+-- {: .num_lemma}
###### Lemma
Given an object $X$ in $\mathcal{C}$, let $X^I$ be a [[path space object]] for $X$ and let
  $$ d = (d_0, d_1) : X^I \twoheadrightarrow X \times X $$
denote the canonical [[fibration]].
The morphisms $d_0 : X^I \to X$ and $d_1 : X^I \to X$ are both [[trivial fibrations]].
=--

+-- {: .proof}
###### Proof

We have the following.

1) The following diagram in $\mathcal{C}$ commutes.

$$
   \array{
      X &  \overset{i}{\hookrightarrow}                                         & X^I \\
          &    \underset{id_X}{\searrow}                    & \downarrow d_{0} \\
          &                                                                    & X
   }
$$

2) By one of the axioms for a category of fibrant objects, $id_X$ is a weak equivalence. 

By the 2-out-of-3 axiom for a category of fibrant objects, we deduce from 1), 2), and the fact that $c$ is a weak equivalence, that $d_{0}$ is a weak equivalence.

An entirely analogous argument demonstrates that $d_{1}$ is a weak equivalence.
=--

+-- {: .num_lemma #FibrantResolution}
###### Lemma
**(Fibrant resolution of a morphism).**
Let $f : X \to Y$ a morphism in $\mathcal{C}$.  There exists a canonical [[fibration]] $g : X \times_Y Y^I \twoheadrightarrow Y$ which factors through $f$ via a [[trivial fibration]] $s: X \times_Y Y^I \stackrel{\sim}{\twoheadrightarrow} X$.
Here $Y^I$ is a [[path space object]] for $Y$.

$$
   \array{
      X \times_Y Y^I & \overset{s}{\to} & X \\
          & \underset{g}{\searrow} & \downarrow{f} \\
          & & Y 
   }
$$
=--

+-- {: .proof}
###### Proof
Let $d = (d_0, d_1) : Y^I \twoheadrightarrow Y \times Y$ be the canonical [[fibration]].  Let $s : X \times_Y Y^I \stackrel{\sim}{\twoheadrightarrow} X$ denote the [[base change]] of $d_0$ along $f$; this is a [[trivial fibration]] because $d_0$ is by lemma 2, and trivial fibrations are stable under base change.

Let $g$ denote the composite
  $$ g : X \times_Y Y^I \to Y^I \stackrel{d_1}{\twoheadrightarrow} Y. $$
One can see that this is a fibration by observing that it is the same as the composite
  $$ X \times_Y Y^I \to X \times_Y Y \times Y = X \times Y \to X \times e = X $$
where $e$ is the [[final object]] of $C$.
Here, the first morphism $id_X \times_Y d$ is a fibration because it is a base change of the fibration $d$; the second is a fibration because it is a base change of the fibration $Y \to e$ ($Y$ is [[fibrant object|fibrant]]).
=--

+-- {: .num_prop #TheFactorizationLemma}
###### Proposition
**(Factorization lemma).**
Any morphism $f : X \to Y$ in $\mathcal{C}$ admits a factorization as a [[weak equivalence]] $i$ followed by a [[fibration]] $p$, such that $i$ is [[right inverse]] to a [[trivial fibration]].
$$
   \array{
      X &  \overset{i}{\to}             & \hat X \\
          & \underset{f}{\searrow} & \downarrow p \\
          &                                        & Y 
   }
$$
=--

+-- {: .proof}
###### Proof
Let $p : \hat X = X \times_Y Y^I \twoheadrightarrow Y$ be a [[fibration|fibrant]] resolution of $f$ as in Lemma 3, so that there is a commutative diagram
$$
   \array{
      \hat X & \overset{s}{\to} & X \\
          & \underset{p}{\searrow} & \downarrow{f} \\
          & & Y 
   }
$$
Let $j : Y \stackrel{\sim}{\to} Y^I$ denote the canonical [[weak equivalence]].  Since the square
$$
   \array{
      X & \overset{id_X}{\to} & X \\
      \downarrow{j f} & & \downarrow{f} \\
      Y^I & \overset{d_0}{\to} & Y
   }
$$
commutes, one gets an induced morphism $i = (id_X, j f) : X \to \hat X$ by the [[universal property]] of the [[pullback]], which by definition has left inverse $s$ and makes the diagram
$$
   \array{
      X &  \overset{i}{\to}             & \hat X \\
          & \underset{f}{\searrow} & \downarrow p \\
          &                                        & Y 
   }
$$
commute.
=--


## Ken Brown's lemma

+-- {: .num_prop #KenBrownLemma}
###### Porposition
**(Ken Brown's lemma)**

Let $\mathcal{C}$ be a [[category of fibrant objects]]. Let $\mathcal{D}$ be a [[category with weak equivalences]]. Let $F \colon C \longrightarrow D$ be a [[functor]] which takes acyclic fibrations to weak equivalences.

Then $F$ is a [[homotopical functor]] in that it takes _all_ weak equivalences to weak equivalences.

=--

+-- {: .proof}
###### Proof

By the factorization lemma, prop. \ref{TheFactorizationLemma}, there is a [[commutative diagram]]

$$
   \array{
      X &  \overset{j}{\to}             & Z \\
          & \underset{w}{\searrow} & \downarrow g \\
          &                                        & Y 
   }
$$
  
in $\mathcal{C}$ such that the following hold.

1. The morphism $g : Z \to Y$ is a fibration.

1. There is a trivial fibration $r : Z \to X$ such that the following diagram in $\mathcal{C}$ commutes.

   $$
      \array{
         X &  \overset{j}{\to}                & Z \\
             &  \underset{id}{\searrow} & \downarrow r \\
             &                                           & X 
      }
      \,.
   $$

By the commutativity of the diagram 

$$
   \array{
      X &  \overset{j}{\to}             & Z \\
          & \underset{w}{\searrow} & \downarrow g \\
          &                                        & Y 
   }
$$

and the fact that both $j$ and $w$ are weak equivalences, we have that $g$ is a weak equivalence, by one of the axioms for a category of fibrant objects.

By assumption, we thus have that $F(g) : F(Z) \to F(Y)$ is a weak equivalence. 

The following hold.

1) By the commutativity of the diagram 

$$
   \array{
      X &  \overset{j}{\to}                & Z \\
          &  \underset{id}{\searrow} & \downarrow r \\
          &                                           & X 
   }
$$

in $\mathcal{C}$, we have that the following diagram in $\mathcal{D}$ commutes.

$$
   \array{
      F(X) &  \overset{F(j)}{\to}           & F(Z) \\
             &  \underset{id}{\searrow} & \downarrow F(r) \\
             &                                           & F(X) 
   }
$$

2) Since $r$ is a trivial fibration, we have by assumption that $F(r)$ is a trivial fibration. In particular, $F(r)$ is a weak equivalence. 

3) By one of the axioms for a category with weak equivalences, we have that $id : F(X) \to F(X)$ is a weak equivalence. 

By 1), 2), 3) and one of the axioms for a category with weak equivalences, we have that $F(j)$ is a weak equivalence. 

The following diagram in $\mathcal{C}$ commutes. 

$$
   \array{
      F(X) &  \overset{F(j)}{\to}             & F(Z) \\
             & \underset{F(w)}{\searrow} & \downarrow F(g) \\
             &                                             & F(Y) 
   } 
$$

Since $F(j)$ and $F(r)$ are weak equivalences, we conclude, by one of the axioms for a category with weak equivalences, that $F(f)$ is a weak equivalence. 

=--


+-- {: .num_remark}
###### Remark

If $C$ is the full subcategory of fibrant objects in a [[model category]], then prop. \ref{KenBrownLemma} asserts that a [[Quillen adjunction|right Quillen functor]] $F$, which by its axioms is required only to preserve fibrations and trivial fibrations, preserves also weak equivalences between fibrant objects.

=--

## Homotopy pullbacks

+-- {: .num_cor}
###### Corollary

Let $A \to C \leftarrow B$ be a diagram between fibrant objects in a [[model category]]. Then the ordinary [[pullback]] $A \times_C^h B$

$$
  \array{
     A \times_C^h B &\to& C^I
     \\
     \downarrow && \downarrow
     \\
     A \times B &\to& C \times C
  }
$$

presents the [[homotopy pullback]] of the original diagram.

=--

See the section _[Concrete constructions](http://ncatlab.org/nlab/show/homotopy+pullback#ConcreteConstructions)_ at _[[homotopy pullback]]_ for more details on this.

## Examples

* For $G$ an [[∞-group]] object in $C$ with [[delooping]] $\mathbf{B}G$, applying the factorization lemma to the point inclusion $* \to \mathbf{B}G$ yields a morphism $* \stackrel{\simeq}{\to} \mathbf{E}G \stackrel{p}{\to} \mathbf{B}G$. This exhibits a [[universal principal ∞-bundle]] for $G$. 


## References

* {#Brown73} [[Kenneth Brown]], around p. 4 of _[[BrownAHT|Abstract Homotopy Theory and Generalized sheaf Cohomology]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458, 1973 .

[[!redirects Ken Brown's lemma]]
[[!redirects ken brown's lemma]]
