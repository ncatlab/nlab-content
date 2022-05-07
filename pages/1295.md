
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Dependent products
* table of contents
{: toc}

## Idea

The _dependent product_ is a [[universal construction]] in [[category theory]]. It generalizes the [[internal hom]] to the situation where the codomain may _depend_ on the domain, and [[internalization|internalizes]] indexed [[products]]. Hence it forms _[[sections]]_ of a [[bundle]]. 

The [[duality|dual]] concept is that of _[[dependent sum]]_.

The concept of [[cartesian product]] of [[sets]] makes sense for any [[family of sets]], while the [[category theory|category-theoretic]] [[product]] makes sense for any family of objects.  In each case, however, the family is indexed by a [[set]]; how can we get a purely category-theoretic product indexed by an object?

First we need to describe a family of objects indexed by an object; it\'s common to interpret this as a [[bundle]], that is an arbitrary morphism $\pi: E \to A$.  (In [[Set]], $A$ would be the index set of the family, and the [[fiber]] of the bundle over an element $x$ of $A$ would be the set indexed by $x$.  Conversely, given a family of sets, $E$ can be constructed as its [[disjoint union]].)

In these terms, the cartesian product of the family of sets is the set $S$ of (global) [[section]]s of the bundle.  This set comes equipped with an evaluation map $ev: S \times A \to E$ such that
$$ S \times A \stackrel{ev}\to E \stackrel{\pi}\to A $$
equals the usual product projection from $S \times A$ to $A$, so $ev$ and $\pi$ are both morphisms in the [[over category]] $Set/A$.  The [[universal property]] of $S$ is that, given any set $T$ and morphism $T \times A \to E$ in $Set/A$, there\'s a unique map $T \to S$ that makes everything commute.

In other words, $S$ and $ev$ define an [[adjoint functor|adjunction]] from $Set$ to $Set/A$ in which taking the product with $A$ is the left adjoint and applying this universal property is the right adjoint.  This is the basis for the definition below, but we add one further level of generality: We realise that $Set$ is secretly $Set/*$, where $*$ is the one-point set (the [[final object]]), and move everything from $Set$ to an arbitrary over category $\mathcal{C}/I$.



## Definitions

Let  $\mathcal{C}$ be a [[category]], and $g\colon B \to A$ a [[morphism]] in $\mathcal{C}$, such that [[pullbacks]] along this morphism exist. These then constitute the [[base change]] [[functor]] between the corresponding [[slice categories]]

$$
  g^* \colon \mathcal{C}_{/A} \to \mathcal{C}_{/B}
  \,.
$$

+-- {: .num_defn}
###### Definition

The **dependent product** along $g$ is, if it exists, the [[right adjoint]] functor $\prod_g \colon \mathcal{C}_{/B} \to \mathcal{C}_{/A}$ to the [[base change]] along $g$

$$
  (g^* \dashv \prod_g)
  \colon
  \mathcal{C}_{/B}
   \stackrel{\overset{g^* }{\leftarrow}}{\underset{\prod_g}{\to}}
  \mathcal{C}_{/A}
  \,.
$$

=--

So a category with all dependent products is necessarily a category with all [[pullbacks]].

## Properties
 {#Properties}


### Relation to spaces of sections
 {#RelationToSpacesOfSections}

+-- {: .num_prop #RelationToSections}
###### Proposition

Let $\mathcal{C}$ be a [[cartesian closed category]] with all [[limit]]s and note that $\mathcal{C}_{/\ast}\cong\mathcal{C}$. Let $X \in C$ be any object and identify it with the terminal morphism $X\to *$. Then the dependent product functor

$$
  \mathcal{C}_{/X}
   \underoverset
       {\underset{\prod_{x \in X}}{\longrightarrow}}
      {\overset{- \times X}{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

sends [[bundles]] $P \to X$ to their [[space of sections|object of sections]]. 

$$
  \prod_{x \in X} P_x
    \simeq
  \Gamma_X(P)
    :=  
  [X,P] \times_{[X,X]} \{id\}
  \,.
$$

=--

+-- {: .proof}
###### Proof

We check the characterizing [[natural isomorphism]] for the adjunction: For every  $A \in \mathcal{C}$ we have the following sequence of natural isos:

$$
  \begin{aligned}
    \mathcal{C}_{/X}(A \times X, P \to X)
      &= 
    \mathcal{C}(A \times X, P ) \times_{\mathcal{C}(A \times X, X)} \{p_2\}
    \\
      & =
      \mathcal{C}(A, [X,P]) \times_{\mathcal{C}(A,[X,X])} \{\tilde p_2\}
     \\  
      &=
      \mathcal{C}(A, [X,P] \times_{[X,X]} \{Id\})
     \\
      &=  \mathcal{C}(A, \Gamma_X(P))
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This statement and its proof remain valid in [[homotopy theory]]. More in detail, if $\mathcal{C}$ is a [[simplicial model category]], $X$, $A$ and $X \times A$ are cofibrant, $P$ and $X$ are fibrant and $P \to X$ is a [[fibration]], then $\Gamma_X(A)$ as above is the homotopy-correct [[derived hom-space|derived section space]]. 

=--

### Relation to exponential objects / internal homs

As a special case of prop. \ref{RelationToSections} one obtains [[exponential objects]]/[[internal homs]].

Let $\mathcal{C}$ have a [[terminal object]] $* \in \mathcal{C}$. Let $A$ and $X$ in $\mathcal{C}$ be objects and let $A \colon A \to *$ and $X \colon X \to *$ be the terminal morphisms. 

+-- {: .num_cor}
###### Corollary

The dependent product along $X$ of the arrow obtained by base change of $A$ along $X$ is the exponential object $[X,A]$:

$$
  \prod_{X} X^* A \simeq [X,A]  \in \mathcal{C}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is essentially a [[categorification|categorified]] version of the familiar fact that the exponentiation $m^n$ of two [[natural numbers]] can be identified with the product $\overset{n}{\overbrace{m\cdot\dots \cdot m}}$ of $n$ copies of $m$.

=--

+-- {: .num_example}
###### Example


Consider the chain of equivalences from $[X,A]$ to $\prod_{X} X^* A$ in [[Set]]: Firstly, the exponential object $[X,A]$ is characterized in $[Y,[X,A]]$ as right adjoint to $[Y\times X,A]$. 
Secondly, the elements  $\theta$ of $[Y\times X,A]$ are in turn in bijection with those functions $(y,x)\mapsto (\theta(y,x),x)$ from $[Y\times X,A\times X]$, that leave the second component fixed. The condition just stated is the definition of arrows in the overcategory ${Set}/X$, between the right projections out of $Y\times X$ resp. $A\times X$. If we identify objects $Z\in{Set}$ with their terminal morphisms $Z:Z\to *$ in ${Set}/*$, those two right projections are the pullbacks $X^* Y$ and $X^* A$, respectively. Thirdly, thus, the subset of $[Y\times X,A\times X]$ we are interested in corresponds to $[X^* Y,X^* A]$ in ${Set}/X$. Finally, the right adjoint to $X^*$ is a functor $\prod_{X}$ from ${Set}/X$ to ${Set}/*$, such that $[X^* Y,X^* A]\simeq [Y, \prod_{X} X^* A]$. Hence $\prod_{X} X^* A$ must correspond to $[X,A]$.

=--

### Relation to type theory and quantification in logic

The dependent product is the [[categorical semantics]] of what in [[type theory]] is the [[type formation|formation]] of [[dependent product types]].  Under [[propositions as types]] this corresponds to [[universal quantification]].

[[!include dependent product natural deduction - table]]

## Examples

### In toposes

Dependent products (and sums) exist in any [[topos]]:

+-- {: .un_prop }
###### Proposition

For $C$ a topos and $f : A \to I$ any morphism in $C$, both the left adjoint $\sum_f : C/A \to C/I$ as well as the right adjoint $\prod_f: C/A \to C/I$ to $f^*: C/I \to C/A$ exist. 

Moreover, $f^*$ preserves the  [[subobject classifier]] and [[internal hom]]s.
=--

This is ([MacLaneMoerdijk, theorem 2 in section IV, 7](#MacLaneMoerdijk)).

The dependent product plays a role in the definition of [[universe in a topos]].


### Along $\mathbf{B}H \to \mathbf{B}G$
 {#AlongDeloopingsOfGroupHomomorphisms}


For $\mathbf{H}$ an [[(∞,1)-topos]] and $G$ an group object in $\mathbf{H}$ (an [[∞-group]]), then the [[slice (∞,1)-topos]] over its [[delooping]] may be identified with the [[(∞,1)-category]] of $G$-[[∞-actions]] (see there for more):


$$
  Act_G(\mathbf{H}) \simeq \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

Under this identification, then dependent product along a morphism of the form $\mathbf{B}H \to \mathbf{B}G$ (corresponding to an [[∞-group]] homomorphism $H \to G$) corresponds to forming [[coinduced representations]].

### Along $\ast \to \mathbf{B}G$
 {#AlongPointInclusionIntoBG}

As the special case of the [above](#AlongDeloopingsOfGroupHomomorphisms) for $H = 1$ the trivial group we obtain the following:

+-- {: .num_prop #GeneralReduction}
###### Proposition

Let $\mathbf{H}$ be any  [[(∞,1)-topos]] and let $G$ be a group object in $\mathbf{H}$ (an [[∞-group]]). Then the dependent product along the canonical point inclusion

$$
  i \;\colon\; \ast \to \mathbf{B}G
$$ 

into the [[delooping]] of $G$ takes the following form: 

There is a pair of [[adjoint ∞-functors]] of the form

$$
  \mathbf{H}
    \underoverset
      { \underset{\underset{i}{\prod} \simeq [G,-]/G}{\longrightarrow}}
      { \overset{i^\ast \simeq hofib}{\longleftarrow}}
      {\bot}
  \mathbf{H}_{/\mathbf{B}G}
  \,,
$$


where

* $hofib$ denotes the operation of taking the [[homotopy fiber]] of a map to $\mathbf{B}G$ over the canonical basepoint;

* $[G,-]$ denotes the [[internal hom]] in $\mathbf{H}$;

* $[G,-]/G$ denotes the [[homotopy quotient]] by the [[conjugation action|conjugation]] [[∞-action]] for $G$ equipped with its canonical [[∞-action]] by left multiplication and the argument
regarded as equipped with its trivial $G$-$\infty$-action 

  (for $G = S^1$ then this is the [[cyclic loop space]] construction).

Hence for

* $\hat X \to X$ a $G$-[[principal ∞-bundle]]

* $A$ a [[coefficient]] object, such as for some [[differential cohomology|differential]] [[generalized cohomology theory]]

then there is a [[natural equivalence]]


$$
  \underset{
    \text{original} \atop \text{fluxes}
  }{
  \underbrace{
    \mathbf{H}(\hat X\;,\; A)
  }
  }
    \;\;
    \underoverset
      {\underset{oxidation}{\longleftarrow}}
      {\overset{reduction}{\longrightarrow}}
      {\simeq}
    \;\;
  \underset{
     \text{doubly} \atop { \text{dimensionally reduced} \atop \text{fluxes} }
  }{
  \underbrace{
    \mathbf{H}(X \;,\; [G,A]/G)
  }
  }
$$

given by

$$
  \left(
     \hat X \longrightarrow A
  \right)
  \;\;\;
    \leftrightarrow
  \;\;\;
  \left(
    \array{
       X && \longrightarrow && [G,A]/G
       \\
       & \searrow && \swarrow
       \\
       && \mathbf{B}G
    }
  \right)
$$

=--

+-- {: .proof #DimensionalReductionAbstractly}
###### Proof

The statement that $i^\ast \simeq hofib$ follows immediately by the definitions. What we need to show is that the [[dependent product]] along $i$ is given as claimed.

To that end, first observe that the [[conjugation action]] on $[G,X]$ is the [[internal hom]] in
the [[(∞,1)-category]] of $G$-[[∞-actions]] $Act_G(\mathbf{H})$.
Under the [[equivalence of (∞,1)-categories]]

$$
  Act_G(\mathbf{H}) \simeq \mathbf{H}_{/\mathbf{B}G}
$$

(from [NSS 12](geometry+of+physics+-+fundamental+super+p-branes#NSS12)) then $G$ with its canonical [[∞-action]] is $(\ast \to \mathbf{B}G)$
and $X$ with the trivial action is $(X \times \mathbf{B}G \to \mathbf{B}G)$.

Hence

$$
  [G,X]/G
    \simeq
  [\ast, X \times \mathbf{B}G]_{\mathbf{B}G}
  \;\;\;\;\;
  \in
   \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

So far this is the very definition of what $[G,X]/G \in \mathbf{H}_{/\mathbf{B}G}$ is to mean in the first place.

But now since the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ is itself [[cartesian closed (infinity,1)-category|cartesian closed]], via

$$
  E \times_{\mathbf{B}G}(-)
  \;\;\;
   \dashv
  \;\;\;
  [E,-]_{\mathbf{B}G}
$$

it is immediate that
there is the following sequence of [[natural equivalences]]

$$
  \begin{aligned}
   \mathbf{H}_{/\mathbf{B}G}(Y, [G,X]/G)
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(Y, [\ast, X \times \mathbf{B}G]_{\mathbf{B}G})
   \\
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(
     Y \times_{\mathbf{B}G} \ast,
     \underset{p^\ast X}{\underbrace{X \times \mathbf{B}G }}
  )
  \\
  & \simeq
  \mathbf{H}(
     \underset{hofib(Y)}{\underbrace{p_!(Y \times_{\mathbf{B}G} \ast)}},
     X
  )
  \\
  & \simeq
  \mathbf{H}(hofib(Y),X)
  \end{aligned}
$$

Here $p \colon \mathbf{B}G \to \ast$ denotes the terminal morphism and $p_! \dashv p^\ast$ denotes the [[base change]] along it.


=--

See also at _[[double dimensional reduction]]_ for more on this.


### Along $V/G \to \mathbf{B}G$

More generally:

+-- {: .num_prop #RightBaseChangeAlongUniversalFiberBundleProjection}
###### Proposition

Let $\mathbf{H}$ be an [[(∞,1)-topos]] and $G \in Grp(\mathbf{H})$ an [[∞-group]].

Let moreover $V \in \mathbf{H}$ be an object equipped with a $G$-[[∞-action]] $\rho$, equivalently (by the discussion there) a [[homotopy fiber sequence]] of the form

$$
  \array{
    V
    \\
    \downarrow
    \\
    V/G & \overset{p_\rho}{\longrightarrow}& \mathbf{B}G
  }
$$

Then 

1. pullback along $p_\rho$ is the operation that assigns to a morphism $c \colon X \to \mathbf{B}G$ the $V$-[[fiber ∞-bundle]] which is [[associated ∞-bundle|associated]] via $\rho$ to the $G$-[[principal ∞-bundle]] $P_c$ classified by $c$:

   $$
     (p_\rho)^\ast \;\colon\; c \mapsto P_c \times_G V
   $$

1. the right base change along $p_\rho$ is given on objects of the form $X \times (V/G)$ by

   $$
     (p_\rho)_\ast \;\colon\; X \times (V/G) \;\mapsto\;  [V,X]/G 
   $$


=--

+-- {: .proof}
###### Proof


The first statement is [NSS 12, prop. 4.6](https://ncatlab.org/schreiber/show/Principal+%E2%88%9E-bundles+--+theory%2C+presentations+and+applications).


The second statement follows as in the proof of prop. \ref{CyclicLoopSpace}: Let 

$$
  \left(
    \array{
      Y
      \\
      \downarrow^{\mathrlap{c}}
      \\
      \mathbf{B}G
    }
  \right)
  \;\in\;
  \mathbf{H}_{/\mathbf{B}G}
$$

be any object, then there is the following sequence of [[natural equivalences]]

$$
  \begin{aligned}
   \mathbf{H}_{/\mathbf{B}G}(Y, [V,X]/G)
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(Y, [V/G, X \times \mathbf{B}G]_{\mathbf{B}G})
   \\
   & \simeq
   \mathbf{H}_{/\mathbf{B}G}(
     Y \times_{\mathbf{B}G} (V/G),
     \underset{p^\ast X}{\underbrace{X \times \mathbf{B}G }}
  )
  \\
  & \simeq
  \mathbf{H}_{/\mathbf{B}G}
  (
    (p_\rho)_!( P_c \times_G (V/G) ),
    p^\ast X
  )
  \\
  & \simeq
     \mathbf{H}_{/(V/G)}
     (
       P_c \times_G V, (p_\rho)^\ast p^\ast X
     )
  \\
  & 
  \simeq
    \mathbf{H}_{/(V/G)}(P_c \times_G V, X \times (V/G))
  \end{aligned}
$$

where again

$$
  p \colon \mathbf{B}G \to \ast
  \,.
$$

=--

+-- {: .num_example #SymmetricPowers}
###### Example
**(symmetric powers)**

Let 

$$
  G = \Sigma(n) \in Grp(Set) \hookrightarrow Grp(\infty Grpd) \overset{LConst}{\longrightarrow} \mathbf{H}
$$ 

be the [[symmetric group]] on $n$ elements, and 

$$
  V = \{1, \cdots, n\} \in Set \hookrightarrow \infty Grpd \overset{LConst}{\longrightarrow} \mathbf{H}
$$

the $n$-element [[set]] ([[h-set]]) equipped with the canonical $\Sigma(n)$-[[action]]. Then prop. \ref{RightBaseChangeAlongUniversalFiberBundleProjection} says that right base change of any $p_\rho^\ast p^\ast X$ along

$$
  \{1, \cdots, n\}/\Sigma(n)
    \longrightarrow
  \mathbf{B}\Sigma(n)
$$

is equivalently the $n$th [[symmetric power]] of $X$

$$
 [\{1,\cdots, n\},X]/\Sigma(n)
  \simeq 
  (X^n)/\Sigma(n)
  \,.
$$

=--



## Related concepts

* [[product]], [[coproduct]]

* [[sink]], [[cosink]]

* [[Kan extension]]

* [[internal limit]]

* [[base change]]

  * [[dependent sum]], **dependent product**

  * [[dependent sum type]], [[dependent product type]]

  * [[necessity]], [[possibility]], [[reader monad]], [[writer comonad]]



## References

Standard textbook accounts include section A1.5.3 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

and section IV of 

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
  {#MacLaneMoerdijk}


[[!redirects dependent product]]
[[!redirects dependent products]]