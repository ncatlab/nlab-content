
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In the context of [[factorization systems]] such as they appear notably in [[enriched model category]] one frequently needs to handle iterated [[lifting problems]]. In the appendix of ([Joyal--Tierney, 06](#JoyalTierney)) a symbolic calculus is introduced to facilitate these computations.

A central point of it is to have the statement of prop. \ref{IteratedLifting} below be easily expressible in terms of "division on both sides"-operations.


## The calculus
 {#TheCalculus}

### Lifting

Let $\mathcal{E}$ be a [[category]] ([[locally small category|locally small]]).

+-- {: .num_defn}
###### Notation

For $f, g \in Mor(\mathcal{E})$, write

$$
  f \,&solb;\, g
$$

if $f$ has the [[left lifting property]] against $g$, or equivalently if $g$ has the [[right lifting property]] against $f$.

For $S \in \mathcal{E}$ an [[object]], write

$$
  f \,&solb;\, S
$$

to indicate that for the morphism $f : X \to Y$ the induced [[hom set]] morphism

$$
  \mathcal{E}(f, S) : \mathcal{E}(Y,S) \to \mathcal{E}(X,S)
$$

is surjective, dually for

$$
  S \,&solb;\, f
  \,.
$$

In the case that $\mathcal{E}$ has a [[terminal object]] $*$ we have equivalently

$$
  f \,&solb;\, S
  \;\;\Leftrightarrow\;\;
  f \,&solb;\, (S \to *)
$$

and if $\mathcal{E}$ has an [[initial object]] $\emptyset$ we have equivalently

$$
  S \,&solb;\, f
  \;\;\Leftrightarrow \;\;
  (\emptyset \to S) \,&solb;\, f
  \,.
$$

Accordingly, for $Q \subset Mor(\mathcal{E})$ write
${}^{&solb;}Q$ and $Q^{&solb;}$ for the class of morphisms with left or right lifting property against all elements of $Q$, respectively.

=--

+-- {: .num_prop}
###### Proposition

If $(L \dashv R) : \mathcal{E} \to \mathcal{F}$ is a pair of [[adjoint functors]], then

$$
  f \,&solb;\, R(g)
  \;\;
  \Leftrightarrow
  \;\;
  L(f) \,&solb;\, g
$$

=--

+-- {: .num_defn}
###### Definition

A pair of classes of morphisms $(L,R)$ in $\mathcal{E}$ is a _[[weak factorization system]]_ precisely if

1. every morphism in $\mathcal{E}$ factors as the [[composition]] of a morphism in $L$ followed by a morphism in $R$;

1. $R = L^{&solb;}$ and $L = {}^{&solb;} R$.

=--


### Tensoring

Let $\mathcal{E}_1$, $\mathcal{E}_2$, $\mathcal{E}_3$ be three categories.

+-- {: .num_defn #Divisibility}
###### Definition

A [[functor]]

$$
  \otimes : \mathcal{E}_1 \times \mathcal{E}_2 \to \mathcal{E}_3
$$

1. is called _divisible on the left_ if for every $A \in \mathcal{E}_1$ the functor $A \otimes (-)$ has a [[right adjoint]], to be denoted

   $$
     A \backslash (-) : \mathcal{E}_3 \to \mathcal{E}_2
     \,;
   $$

1. is called _divisible on the right_ if for every $A \in \mathcal{E}_2$ the functor $(-) \otimes A$ has a [[right adjoint]], to be denoted

   $$
     (-)/ A : \mathcal{E}_3 \to \mathcal{E}_1
     \,;
   $$

=--

+-- {: .num_prop}
###### Proposition

If $\otimes$ is divisble on both sides, then there are [[natural isomorphisms]]  between the collections of morphisms

$$
  A \otimes B \to X
$$

and

$$
  B \to A\backslash X
$$

and

$$
  A \to X / B
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For every $f \in Mor(\mathcal{E}_1)$, $g \in Mor(\mathcal{E}_2)$ and $X \in \mathcal{E}_3$ we have

$$
  f \,&solb;\, (X/g)
  \;\;
  \Leftrightarrow
  \;\;
  g \,&solb;\, (f \backslash X)
  \,.
$$

=--

+-- {: .num_example}
###### Example

If $\mathcal{E}$ is a [[closed monoidal category|closed]] [[symmetric monoidal category]], then its [[tensor product]] functor $\otimes : \mathcal{E} \times \mathcal{E} \to \mathcal{E}$ is divisible on both sides, the two divisions coincide and are given by the [[internal hom]] $[-,-] : \mathcal{E}^{op} \times \mathcal{E} \to \mathcal{E}$

$$
  X/A \simeq [A,X] \simeq A\backslash X
  \,.
$$

=--

### Pushout-tensoring

Let now $\mathcal{E}_3$ have [[finite limits|finite]] [[colimits]] and let $\otimes : \mathcal{E}_1 \times \mathcal{E}_2 \to \mathcal{E}_3$ be a [[functor]].

+-- {: .num_defn}
###### Definition

for $f : A \to B$ in $\mathcal{E}_1$ and $g : X \to Y$ in $\mathcal{E}_2$, write

$$
  A \otimes Y 
    \overset
      {A \otimes X} 
      {\amalg}
  B \otimes X
  \longrightarrow
  B \otimes Y
$$

for the induced _[[pushout-product]]_ morphism, the canonical morphism out of the [[pushout]] induced from the commutativity of the diagram

$$
  \array{
    A \otimes X &\to& B \otimes X
    \\
    \downarrow && \downarrow
    \\
    A \otimes Y &\to& B \otimes Y
  }
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The pushout-product extends to a functor

$$
  \bar \otimes : \mathcal{E}_1^I \times \mathcal{E}_2^I \to \mathcal{E}_3^I
  \,,
$$

where $C^I$ denotes the [[arrow category]] of $C$.
=--

+-- {: .num_prop}
###### Proposition

If in the above situation $\mathcal{E}_1$ and $\mathcal{E}_2$ have [[finite limits]] and $\otimes$ is divisble on both sides, def. \ref{Divisibility}, then also $\bar{\otimes}$ is divisible on both sides:

1. for $f : A \to B$ in $\mathcal{E}_1$ and $g : X \to Y$ in $\mathcal{E}_3$, the left quotient is

   $$
     f \bar \backslash g
     \;\colon\;
     B \backslash X \to B \backslash Y \times_{A \backslash Y} A \backslash X
     \,;
   $$

1. for $f : S \to T$ in $\mathcal{E}_2$ and $g : X \to Y$ in $\mathcal{E}_3$, the right quotient is

   $$
      g \bar / f
      \;\colon\;
      X / T \to Y / T \times_{Y / S} X / S
     \,;
   $$

=--

A key statement now is the following, characterizing the [[right lifting property]] again [[pushout product]] morphisms:

+-- {: .num_prop #IteratedLifting}
###### Proposition

In the above situation, let $\mathcal{E}_1$, $\mathcal{E}_2$, $\mathcal{E}_3$ have all [[finite limit|finite]] [[limits]] and [[colimits]]. For all $u \in Mor(\mathcal{E}_1)$, $v \in Mor(\mathcal{E}_2)$, $f \in Mor(\mathcal{E}_3)$ we have

$$
  (u \bar \otimes v) \,&solb;\, f
  \;\;
  \Leftrightarrow
  \;\;
  u \,&solb;\, f \bar /v
  \;\;
  \Leftrightarrow
  \;\;
  v \,&solb;\, u \bar \backslash f
  \,.
$$

=--

## Applications

### Reedy theory

Let $\mathcal{E}$ be a [[model category]]. Write $\Delta$ for the [[simplex category]] and [[sSet]] for the category of [[simplicial sets]]. In the [[Reedy model structure]] on the [[presheaf category]] $[\Delta^{op}, \mathcal{E}]$ the following constructions are central.

+-- {: .num_defn}
###### Definition

Write

$$
  \Box : sSet \times \mathcal{E} \to [\Delta^{op}, \mathcal{E}]
$$

for the functor given by

$$
  (S \Box X) : n \mapsto S_n \cdot X
  \,.
$$

Write

$$
  \otimes : [\Delta, Set] \times [\Delta^{op}, \mathcal{E}] \to\mathcal{E}
$$

for the functor given by the [[coend]]

$$
  S \otimes X = \int^{n \in \Delta} S_n \cdot X_n
  \,.
$$

=--

(Here on the right we have the canonical [[tensoring]] of $\mathcal{E}$ over [[Set]], where $S_n \cdot X \simeq \coprod_{s \in S_n} X$.)

+-- {: .num_prop}
###### Proposition

The functor $\Box$ is divisible on both sides.

Let $X \in [\Delta^{op}, sSet]$. Then

* the object $\partial \Delta[n] \backslash X$ is the _[[Reedy model structure|matching object]]_ of $X$ at stage $n$;

* the morphism $(\partial \Delta[n] \hookrightarrow \Delta[n]) \backslash X$ is the canonical morphism from $X_n$ into the $n$-matching object.

Let $f : X \to Y$ be a morphism in $[\Delta^{op}, sSet]$. Then

* the [[Reedy model structure|relative matching morphism]] of $f$ at stage $n$ is

  $$
    (\partial \Delta[n] \hookrightarrow \Delta[n]) \bar \backslash f
    \,;
  $$

* the object $(\partial \Delta^c) \otimes X$ is the _latching object_ at stage $n$;

* the morphism $(\partial \Delta^c \to \Delta)\otimes X$ is the canonical morphism out of the latching object into $X_n$;

* the morphism $(\partial \Delta^c \to \Delta) \bar \otimes f$ is the _relative latching morphism_ of $f$.

=--


## Related concepts

* [[pushout-product axiom]]

* [[pullback-power]]

* [[Quillen negation]]/[[weak orthogonal class]]

## References

* {#JoyalTierney} [[André Joyal]], [[Myles Tierney]], _Quasi-categories vs Segal spaces_ ([arXiv:0607820](http://arxiv.org/abs/math/0607820))
 


[[!redirects Joyal-Tierney calculus]]
[[!redirects Joyal–Tierney calculus]]
[[!redirects Joyal--Tierney calculus]]
