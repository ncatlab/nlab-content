
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

# Contents #
* table of contents
{: toc}


## Idea ##

The _factorization lemma_ ([Brown 73](#Brown73), prop. \ref{TheFactorizationLemma} below) is a fundamental tool in the theory of [[categories of fibrant objects]] ([[formal dual|dually]]: [[cofibration category|of cofibrant objects]]). It mimics one half of the _factorization axioms_ in a [[model category]] in that it asserts that every morphism may be factored as, in particular, a weak equivalence followed by a fibration.

A key corollary of the factorization lemma is the statement, widely known as _Ken Brown's lemma_ (prop. \ref{KenBrownLemma} below) which says that for a functor from a category of fibrant objects  to be a [[homotopical functor]], it is sufficient already that it sends acyclic fibrations to weak equivalences. 

For more background, see also at _[[Introduction to Stable homotopy theory -- P|Introduction to classical homotopy theory]]_ [this lemma](Introduction+to+Stable+homotopy+theory+--+P#FactorizationLemma).


## Factorization lemma ##

Let $\mathcal{C}$ be a [[category of fibrant objects]].

+-- {: .num_prop}
###### Proposition

Let 

$$
X \overset{p_{X}}{\leftarrow} X \times Y \overset{p_{Y}}{\rightarrow} Y
$$

be a product in $\mathcal{C}$. Then $p_{X}$ and $p_{Y}$ are fibrations.

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

+-- {: .num_prop}
###### Proposition

Let $X$ be an object of $\mathcal{C}$. Let 

$$
X \overset{p_{0}}{\leftarrow} X \times X \overset{p_{1}}{\rightarrow} X
$$ 

be a product in $\mathcal{C}$. By one of the axioms for a category of fibrant objects, there is a commutative diagram 

$$
   \array{
      X &  \overset{c}{\to}                      & X^I \\
          &    \underset{\Delta}{\searrow} & \downarrow e \\
          &                                                   & X \times X 
   }
$$

in $\mathcal{C}$ in which $c$ is a weak equivalence, and in which $e$ is a fibration. 

The arrow $e_0 : X^I \to X$ given by $p_0 \circ e$ is a trivial fibration. The arrow $e_1 : X^I \to X$ given by $p_1 \circ e$ is a trivial fibration.

=--

+-- {: .proof}
###### Proof

We have the following.

1) The following diagram in $\mathcal{C}$ commutes.

$$
   \array{
      X &  \overset{c}{\to}                                         & X^I \\
          &    \underset{id_X}{\searrow}                    & \downarrow e_{0} \\
          &                                                                    & X
   }
$$

2 By one of the axioms for a category of fibrant objects, $id_X$ is a weak equivalence. 

By one of the axioms for a category of fibrant objects, we deduce from 1), 2), and the fact that $c$ is a weak equivalence, that $e_{0}$ is a weak equivalence.

An entirely analogous argument demonstrates that $e_{1}$ is a weak equivalence.

=--

+-- {: .num_prop #TheFactorizationLemma}
###### Proposition
**(Factorization lemma)**

Let $f : X \to Y$ be an arrow of $\mathcal{C}$. There is a commutative diagram 

$$
   \array{
      X &  \overset{j}{\to}             & Z \\
          & \underset{f}{\searrow} & \downarrow g \\
          &                                        & Y 
   }
$$
  
in $\mathcal{C}$ such that the following hold.

1) The arrow $g : Z \to Y$ is a fibration.

2) There is a trivial fibration $r : Z \to X$ such that the following diagram in $\mathcal{C}$ commutes.

$$
   \array{
      X &  \overset{j}{\to}                & Z \\
          &  \underset{id}{\searrow} & \downarrow r \\
          &                                           & X 
   }
$$


=--

+-- {: .proof}
###### Proof

We can construct the following diagram:

\begin{tikzcd}
X \arrow[rdd, "{(id,f)}", bend right] \arrow[rrrd, "f", bend left] \arrow[rd, "\exists ! j", dashed] &                                                                                                                                                          &                                            &                                         \\
                                                                                                     & Z \arrow[d, "\pi_1^Z"] \arrow[r, "\pi_0^Z"] \arrow[dr, phantom, "\lrcorner", very near start]                                                            & Y^I \arrow[d, "e"]                         & Y \arrow[l, "c"'] \arrow[ld, "\Delta"'] \\
                                                                                                     & X \times Y \arrow[r, "f \times id"] \arrow[d, "\pi_0^{X \times Y}"] \arrow[ld, "\pi_1^{X \times Y}"']  \arrow[dr, phantom, "\lrcorner", very near start] & Y \times Y \arrow[d, "\pi_0^{Y \times Y}"] &                                         \\
Y                                                                                                    & X \arrow[r, "f"]                                                                                                                                         & Y                                          &                                        
\end{tikzcd}

The triangle on the right exists with $c$ a weak equivalence and $e$ a fibration, as categories of fibrant objects have path objects. As $e$ is a fibration, we can pullback along $f \times id$ to get the upper-left pullback square. By the universal property of this pullback square, we can produce a unique $X \overset j \to Z$ which makes the top half of the diagram commute.

We let $g$ be the composite $Z \overset{\pi_1^Z} \to X \times Y \overset{\pi_1^{X \times Y}} \to Y$ so that $g \circ j = f$; these are fibrations due to being a pullback of the fibration $e$ and a product projection (Fact 1), so their composite $g$ is a fibration too.

We let $r$ be the composite $Z \overset{\pi_1^Z} \to X \times Y \overset{\pi_0^{X \times Y}} \to X$ so that $r \circ j = id_X$. As the upper square and lower square are both pullback squares, $r$ is the pullback of the morphism $Y^I \overset{e} \to Y \overset{\pi_0^{Y\times Y}} \to Y$ (which is an acyclic fibration by Fact 2), hence $r$ is also an acyclic fibraiton.

=--

+-- {: .num_remark}
###### Remark

That $r$ is a fibration can be demonstrated in exactly the same way as that $g$ is a fibration. It is to prove the stronger assertion that $r$ is a trivial fibration that the argument with which we concluded the proof is needed.

=--

+-- {: .num_remark}
###### Remark

By the commutativity of the diagram

$$
   \array{
      X &  \overset{j}{\to}                & Z \\
          &  \underset{id}{\searrow} & \downarrow r \\
          &                                           & X 
   }
$$

and the fact that $r$ is a weak equivalence, we have, by one of the axioms for a category of fibrant objects, that $j$ is a weak equivalence. 

=--


## Ken Brown's lemma ##

+-- {: .num_prop #KenBrownLemma}
###### Proposition
**(Ken Brown's lemma)**

Let $\mathcal{C}$ be a category of fibrant objects. Let $\mathcal{D}$ be a [[category with weak equivalences]]. Let $F : C \to D$ be a functor with the property that, for every arrow $f$ of $\mathcal{C}$ which is a trivial fibration, we have that $F(f)$ is a weak equivalence. 

Let $w : X \to Y$ be an arrow of $\mathcal{C}$ which is a weak equivalence. Then $F(w)$ is a weak equivalence. 
=--

+-- {: .proof}
###### Proof

By Proposition 3, there is a commutative diagram 

$$
   \array{
      X &  \overset{j}{\to}             & Z \\
          & \underset{w}{\searrow} & \downarrow g \\
          &                                        & Y 
   }
$$
  
in $\mathcal{C}$ such that the following hold.

1) The arrow $g : Z \to Y$ is a fibration.

2) There is a trivial fibration $r : Z \to X$ such that the following diagram in $\mathcal{C}$ commutes.

$$
   \array{
      X &  \overset{j}{\to}                & Z \\
          &  \underset{id}{\searrow} & \downarrow r \\
          &                                           & X 
   }
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

Since $F(j)$ and $F(g)$ are weak equivalences, we conclude, by one of the axioms for a category with weak equivalences, that $F(w)$ is a weak equivalence. 

=--

+-- {: .num_remark}
###### Remark

In other words, $F$ is a [[homotopical functor]].

=--

+-- {: .num_remark}
###### Remark
If $C$ is the full subcategory of fibrant objects in a [[model category]], then this corollary asserts that a [[Quillen adjunction|right Quillen functor]] $G$, which by its axioms is required only to preserve fibrations and trivial fibrations, preserves also weak equivalences between fibrant objects.
=--

+-- {: .num_remark}
###### Remark
By the dual nature of [[model categories]], we then get that a [[Quillen adjunction|left Quillen functor]] preserves weak equivalences between cofibrant objects.
=--

## Computing a homotopy pullback by means of an ordinary pullback

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


## Examples ##

* For $G$ an [[∞-group]] object in $C$ with [[delooping]] $\mathbf{B}G$, applying the factorization lemma to the point inclusion $* \to \mathbf{B}G$ yields a morphism $* \stackrel{\simeq}{\to} \mathbf{E}G \stackrel{p}{\to} \mathbf{B}G$. This exhibits a [[universal principal ∞-bundle]] for $G$. 


## References ##

The [factorization lemma](#TheFactorizationLemma) is due to 

* {#Brown73} [[Kenneth Brown]], p. 421 (4 of 41) in: _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_, 1973, p. 4

The corollary commonly known as "[Ken Brown's lemma](#KenBrownLemma)" does not appear explicitly in [Brown 73](#Brown73); it does appear under this name in

* [[Mark Hovey]], Lemma 1.1.12 in: _Model Categories_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover), [ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s))


A version in the setup of $\infty$-cosmoi is Lemma 2.1.6 in 

* {#RiehlV17} [[Emily Riehl]], [[Dominic Verity]], _Fibrations and Yoneda’s lemma in an $\infty$-cosmos_, Journal of Pure and Applied Algebra, 221:3, 2017, pp. 499--564 ([arXiv:1506.05500](http://arxiv.org/abs/1506.05500))

[[!redirects ken brown's lemma]]

[[!redirects Ken Brown's lemma]]
