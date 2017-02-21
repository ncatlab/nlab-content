
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[model category]]-theory, the _Bousfield-Friedlander theorem_ ([Bousfield-Friedlander 78, theorem A.7](#BousfieldFriedlander78), [Bousfield 01, theorem 9.3](#Bousfield01)) states that if an [[endofunctor]] $Q \colon \mathcal{C} \to \mathcal{C}$ on a [[model category]] $\mathcal{C}$ behaves like an [[idempotent monad]] in an appropriate model category theoretic sense, then the [[left Bousfield localization]] [[model category]] structure of $\mathcal{C}$ at the $Q$-equivalences exists.

The original proof assumed that $\mathcal{C}$ is a [[proper model category|right-proper model category]], but it turns out that this condition is not necessary ([Stanculescu 08, theorem 1.1](#Stanculescu08)).

## Statement

+-- {: .num_defn #QuillenIdempotentMonad}
###### Definition

Let $\mathcal{C}$ be a [[proper model category]]. 
Say that a **Quillen idempotent monad** on $\mathcal{C}$ is
 
1. an [[endofunctor]] 

   $Q \;\colon\;  \mathcal{C} \longrightarrow \mathcal{C}$

1. a [[natural transformation]]

   $\eta \colon id_{\mathcal{C}} \longrightarrow Q$

such that

1. ([[homotopical functor]]) $Q$ preserves weak equivalences;

1. (idempotency) for all $X \in \mathcal{C}$ the morphisms

   $$
     Q(\eta_X) \;\colon\; Q(X) \overset{\in W}{\longrightarrow} Q(Q(X))
   $$

   and

   $$
     \eta_{Q(X)} \;\colon\; Q(X) \overset{\in W}{\longrightarrow} Q(Q(X))
   $$

   are weak equivalences;

1. (right-properness of the localization) if in a [[pullback]] square in $\mathcal{C}$

   $$
     \array{
       f^\ast W &\stackrel{f^\ast h}{\longrightarrow}& X
       \\
       \downarrow && \downarrow^{\mathrlap{f}}
       \\
       W &\stackrel{h}{\longrightarrow}& Y
     }
   $$

   we have that

   1. $f$ is a fibration;

   1. $\eta_X$, $\eta_Y$, and $Q(h)$ are weak equivalences

   then $Q(f^\ast h)$ is a weak equivalence.

=--

(Here the formulation of the third item follows [Bousfield 01, def. 9.2](#Bousfield01). By lemma \ref{SecondLemmaForBousfieldFriedlander} below this condition implies that $f$ is a $Q$-fibration, which is the condition required in [Bousfield-Friedlander 78 (A.6)](#BousfieldFriedlander78)).


+-- {: .num_defn #ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}
###### Definition

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad}, say that a morphism $f$ in $\mathcal{C}$ is

1. a **$Q$-weak equivalence** if $Q(f)$ is a weak equivalence;

1. **a $Q$-cofibation** if it is a cofibration.

1. **a $Q$-fibration** if it has the [[right lifting property]] against the morphisms that are both ($Q$-)cofibrations as well as $Q$-weak equivalences.

Write $\mathcal{C}_Q$ for $\mathcal{C}$ equipped with these classes of morphisms.

=--




+-- {: .num_lemma #FirstLemmaForBousfieldFriedlander}
###### Lemma

In the situation of def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}, 
a morphism is an acyclic fibration in $\mathcal{C}_Q$ precisely if it is an acyclic fibration in $\mathcal{C}$.

=--

+-- {: .proof}
###### Proof

Let $f$ be a fibration and a weak equivalence. Since $Q$ preserves weak equivalences by condition 1 in def. \ref{QuillenIdempotentMonad}, $f$ is also a $Q$-weak equivalence. Since $Q$-cofibrations are cofibrations, the acyclic fibration $f$ has right lifting against $Q$-cofibrations, hence in particular against against $Q$-acyclic $Q$-cofibrations, hence is a $Q$-fibration.

In the other direction, let $f$ be a $Q$-acyclic $Q$-fibration. Consider its factorization into a cofibration followed by an acyclic fibration

$$
  f \colon \underoverset{\in Cof}{i}{\longrightarrow} \underoverset{\in W \cap Fib}{p}{\longrightarrow}
  \,.
$$

Now the fact that $Q$ preserves weak equivalences together with [[two-out-of-three]] implies that $i$ is a $Q$-weak equivalence, hence a $Q$-acyclic $Q$-cofibration. This means by assumption that $f$ has the [[right lifting property]] against $i$. Hence the [[retract argument]], implies that $f$ is a [[retract]] of the acyclic fibration $p$, and so is itself an acyclic fibration.

=--

+-- {: .num_lemma #SecondLemmaForBousfieldFriedlander}
###### Lemma

In the situation of def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}, if a morphism $f \colon X \longrightarrow Y$ is a fibration, and $\eta_X, \eta_Y$ are weak equivalences, then $f$ is a $Q$-fibration.

=--

(e.g. [Goerss-Jardine 96, chapter X, lemma 4.4](#GoerssJardine96)).

+-- {: .proof}
###### Proof

We need to show that for every [[commuting square]] of the form

$$
  \array{
    A &\overset{\alpha}{\longrightarrow}& X
    \\
    {}^{\mathllap{i}}_{\mathllap{\in W_Q \cap Cof_Q}}\downarrow 
     && 
    \downarrow^{\mathrlap{f}}
    \\
    B &\underset{\beta}{\longrightarrow}& Y
  }
$$

there exists a lifting.

To that end, first consider a factorization of the image under $Q$ of this square as follows:

$$
  \array{
    Q(A) &\overset{Q(\alpha)}{\longrightarrow}& Q(X)
    \\
    {}^{\mathllap{Q(i)}}\downarrow && \downarrow^{\mathrlap{Q(f)}}
    \\
    Q(B) &\underset{Q(\beta)}{\longrightarrow}& Q(Y)
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    Q(A) 
     &\underoverset{\in W \cap Cof}{j_\alpha}{\longrightarrow}& 
    Z 
     &\underoverset{\in Fib}{p_\alpha}{\longrightarrow}& 
    Q(X)
    \\
    {}^{\mathllap{Q(i)}}\downarrow 
      &&
    \downarrow^{\pi}
      && 
    \downarrow^{\mathrlap{Q(f)}}
    \\
    Q(B) 
      &\underoverset{j_\beta}{\in W \cap Cof}{\longrightarrow}& 
    W 
      &\underoverset{p_\beta}{\in Fib}{\longrightarrow}& 
    Q(Y)
  }
$$

(This exists even without assuming [[functorial factorization]]: factor the bottom morphism, form the pullback of the resulting $p_\beta$, observe that this is still a fibration, and then factor (through $j_\alpha$) the universal morpism from the outer square into this pullback.)

Now consider the pullback of the right square above along the naturality square of $\eta \colon id \to Q$, take this to be the right square in the following diagram

$$
  \array{
    \alpha \colon
    & 
    A 
      &\overset{(j_\alpha \circ \eta_A, \alpha)}{\longrightarrow}&
    Z \underset{Q(X)}{\times} X
      &\overset{}{\longrightarrow}&
    X
    \\
    & {}^{\mathllap{i}}\downarrow 
      &&
    \downarrow^{\mathrlap{(\pi,f)}}
      &&
    \downarrow^{\mathrlap{f}}&
    \\
    \beta \colon 
    & 
    B 
      &\underset{(j_\beta\circ\eta_B,\beta)}{\longrightarrow}&
    W \underset{Q(Y)}{\times} Y
      &\underset{}{\longrightarrow}&
    Y
  }
  \,,
$$

where the left square is the universal morphism into the pullback which is induced from the naturality squares of $\eta$ on $\alpha$ and $\beta$.

We claim that $(\pi,f)$ here is a weak equivalence. This implies that we find the desired lift by factoring $(\pi,f)$ into an acyclic cofibration followed by an acyclic fibration and then lifting consecutively as follows

$$
  \array{
    \alpha \colon
    & 
    A 
      &\overset{(j_\alpha \circ \eta_A, \alpha)}{\longrightarrow}&
    Z \underset{Q(X)}{\times} X
      &\overset{}{\longrightarrow}&
    X
    \\
    & {}^{\mathllap{id}}\downarrow 
      &&
    {}^{\mathllap{\in W \cap Cof}}\downarrow
      &{}^{\mathllap{\exists}}\nearrow&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib}}&
    \\
    & 
    A 
      &\longrightarrow& 
      &\overset{\phantom{AAAAAAA}}{\longrightarrow}&
    Y
    \\
    & {}^{\mathllap{i}}_{\mathllap{\in Cof}}\downarrow 
      &{}^{\mathllap{\exists}}\nearrow&
    \downarrow^{\mathrlap{\in W \cap Fib}}
      &&
    \downarrow^{\mathrlap{id}}&
    \\
    \beta \colon & 
    B 
      &\underset{(j_\beta\circ\eta_B,\beta)}{\longrightarrow}&
    W \underset{Q(Y)}{\times} Y
      &\longrightarrow&
    Y
  }
  \,.
$$

To see that $(\phi,f)$ indeed is a weak equivalence:

Consider the diagram

$$
  \array{
     Q(A) 
       &\underoverset{\in W \cap Cof}{j_\alpha}{\longrightarrow}& 
     Z
       &\underoverset{\in W}{pr_1}{\longleftarrow}&
     Z \underset{Q(X)}{\times} X
     \\
     {}^{\mathllap{Q(i)}}_{\mathllap{\in W}}\downarrow 
       && 
     \downarrow^{\mathrlap{\pi}}
       && 
     \downarrow^{\mathrlap{(\pi,f)}}
     \\
     Q(B) 
       &\underoverset{j_\beta}{\in W \cap Cof}{\longrightarrow}& 
     Z
       &\underoverset{pr_2}{\in W}{\longleftarrow}&
     W \underset{Q(X)}{\times} X
  }
  \,.
$$

Here the projections are weak equivalences as shown, because by assumption in def. \ref{QuillenIdempotentMonad} the ambient model category is [[right proper model category|right proper]] and these projections are the pullbacks along the fibrations $p_\alpha$ and $p_\beta$ of the morphisms $\eta_X$ and $\eta_Y$, respectively, where the latter are weak equivalences by assumption. Moreover $Q(i)$ is a weak equivalence, since $i$ is a $Q$-weak equivalence.

Hence now it follows by [[two-out-of-three]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#CategoryWithWeakEquivalences)) that $\pi$ and then $(\pi,f)$ are weak equivalences.

=--


+-- {: .num_prop #BousfieldFriedlanderTheorem}
###### Proposition
**(Bousfield-Friedlander theorem)**

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad},
then $\mathcal{C}_Q$, def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad} is a [[model category]].

=--

([Bousfield-Friedlander 78, theorem 8.7](#BousfieldFriedlander78), [Bousfield 01, theorem 9.3 ](#Bousfield01), [Goerss-Jardine 96, chapter X lemma 4.5, lemma 4.6](#GoerssJardine96))


+-- {: .proof}
###### Proof

The existence of [[limits]] and [[colimits]] is guaranteed since $\mathcal{C}$ is already assumed to be a model category.
The [[two-out-of-three]] poperty for $Q$-weak equivalences is an immediate consequence of two-out-of-three for the original weak equivalences of $\mathcal{C}$. 

Moreover, according to lemma \ref{FirstLemmaForBousfieldFriedlander} the pair of classes $(Cof_{Q}, W_Q \cap Fib_Q)$ equals the pair $(Cof, W \cap Fib)$, and this is a [[weak factorization system]] by the model structure $\mathcal{C}$.

Hence it remains to show that $(W_Q \cap Cof_Q, \; Fib_Q)$ is a [[weak factorization system]]. The condition $Fib_Q = RLP(W_Q \cap Cof_Q)$ holds by definition of $Fib_Q$. Once we show that every morphism factors as $W_Q \cap Cof_Q$ followed by $Fib_Q$, then the condition $W_Q \cap Cof_Q = LLP(Fib_Q)$ follows from the [[retract argument]] (and the fact that $W_Q$ and $Cof_Q$ are stable under retracts, because $W$ and $Cof = Cof_Q$ are). 

So we may conclude by showing the existence of $(W_Q \cap Cof_Q, \; Fib_Q)$ factorizations:

First we consider the case of a morphism of the form $f \colon Q(Y) \to Q(Y)$. This may be factored with respect to $\mathcal{C}$ as

$$
  f 
  \;\colon\;
  Q(X)
    \underoverset{\in W \cap Cof}{\in i}{\longrightarrow}
  Z
    \underoverset{\in Fib}{p}{\longrightarrow}
  Q(Y)
  \,.
$$

Here $i$ is already a $Q$-acyclic $Q$-cofibration. Now apply $Q$ to obtain

$$
  \array{
  f 
  \colon
  &
  Q(X)
    &\underoverset{\in W \cap Cof}{i}{\longrightarrow}&
  Z
    &\underoverset{\in Fib}{p}{\longrightarrow}&
  Q(Y)
  \\
  &
  \downarrow^{\mathrlap{\eta_{Q(X)}}}_{\mathrlap{\in W}} 
    && 
  \downarrow^{\mathrlap{\eta_Z}} 
    && 
  \downarrow^{\mathrlap{\eta_{Q(Y)}}}_{\mathrlap{\in W}}
  \\
  &
  Q(Q(X))
    &\underoverset{Q(i)}{\in W}{\longrightarrow}&
  Q(Z)
    &\underset{}{\longrightarrow}&
  Q(Q(Y))
  }
  \,,
$$

where $\eta_{Q(X)}$ and $\eta_{Q(Y)}$ are weak equivalences by idempotency, and $Q(i)$ is a weak equivalence since $Q$ preserves weak equivalences. Hence by [[two-out-of-three]] also $\eta_Z$ is a weak equivalence. Therefore lemma \ref{SecondLemmaForBousfieldFriedlander} gives that $p$ is a $Q$-fibration, and hence the above factorization is already as desired

$$
  f 
  \;\colon\;
  Q(X)
    \underoverset{\in W_Q \cap Cof_Q}{\in i}{\longrightarrow}
  Z
    \underoverset{\in Fib_Q}{p}{\longrightarrow}
  Q(Y)
  \,.
$$

Now for $g$ an arbitrary morphism $g \colon X \to Y$, form a factorization of $Q(g)$ as above and then decompose the naturality square for $\eta$ on $g$ into the pullback of the resulting $Q$-fibration along $\eta_Y$:

$$
  \array{
    g \colon
    & 
    X 
      &\overset{\tilde i}{\longrightarrow}&
    Z \underset{Q(Y)}{\times} Y
      &\overset{\tilde p}{\longrightarrow}&
    Y
    \\
    &
    {}^{\mathllap{\eta_X}}_{\mathllap{\in W_Q}}\downarrow 
      && 
    \downarrow^{\mathrlap{\eta'}}_{\mathrlap{}} 
      &(pb)& 
    \downarrow^{\mathrlap{\eta_Y}}_{\mathrlap{\in W_Q}}
    \\
    Q(g)
    \colon
    &
    Q(Y)
      &\underoverset{i}{\in W_Q}{\longrightarrow}& 
    Z
      &\underoverset{p}{\in Fib_Q}{\longrightarrow}&
    Q(Y)
  }
  \,.
$$

This exhibits $\eta'$ as the pullback of a $Q$-weak equivalence along a $Q$-fibration, and hence itself as a $Q$-weak equivalence. This way, [[two-out-of-three]] implies that $\tilde i$ is a $Q$-weak equivalence.

Finally, apply factorization in $(Cof,\; W\cap Fib)$ to $\tilde i$ to obtain the desired factorization

$$
  f 
    \;\colon\;
  \overset{W_Q \cap Cof}{\longrightarrow}
  \overset{W \cap Fib = W_Q \cap Fib_Q}{\longrightarrow}
  \overset{Fib_Q}{\longrightarrow}
  \,.
$$

=--


+-- {: .num_prop #CharacterizationOfFibrationsInBFModelStructures}
###### Proposition

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad},
then a morphism $f \colon X \to Y$ in $\mathcal{C}$ is a $Q$-fibration (def. \ref{ClassesOfMorphismsInBousfieldLocalizationAtQuillenIdempotentMonad}) precisely if 

1. $f$ is a fibration;

1. the $\eta$-naturality square on $f$ 

   $$
     \array{
       X &\stackrel{\eta_X}{\longrightarrow}& Q(X)
       \\
       {}^{\mathllap{f}}\downarrow &{}^{(pb)^h}& \downarrow^{\mathrlap{Q(f)}}
       \\
       Y &\underset{\eta_Y}{\longrightarrow}& Q(Y)
     }
   $$

   exhibits a [[homotopy pullback]] in $\mathcal{C}$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyPullback)), in that for any factorization of $Q(f)$ through a weak equivalence followed by a fibration $p$, then the universally induced morphism

   $$
     X \longrightarrow p^\ast Y
   $$

   is weak equivalence (in $\mathcal{C}$).

=--

(e.g. [Goerss-Jardine 96, chapter X, theorem 4.8](#GoerssJardine96))

+-- {: .proof}
###### Proof

First consider the case that $f$ is a fibration and that the square is a homotopy pullback. We need to show that then $f$ is a $Q$-fibration.

Factor $Q(f)$ as

$$
  Q(f) 
    \;\colon\;
  Q(X)
    \underoverset{\in W \cap Cof}{i}{\longrightarrow}
  Z
    \underoverset{\in Fib}{p}{\longrightarrow}
  Q(Y)  
  \,.
$$

By the proof of prop. \ref{BousfieldFriedlanderTheorem}, the morphism $p$ is also a $Q$-fibration. Hence by the existence of the $Q$-local model structure, also due to prop. \ref{BousfieldFriedlanderTheorem}, its [[pullback]] $\tilde p$ is also a $Q$-fibration

$$
  \array{
    X &\overset{\eta_X}{\longrightarrow}& Q(X)
    \\
    {}^{\mathllap{\tilde i}}_{\mathllap{\in W}}\downarrow 
      && 
    \downarrow^{\mathrlap{i}}_{\mathrlap{\in W}}
    \\
    Y \underset{Q(Y)}{\times} Z 
      &\overset{p^\ast \eta_Y}{\longrightarrow}&
    Z
    \\
    {}^{\mathllap{\tilde p}}_{\mathllap{\in Fib_Q}}\downarrow 
      &(pb)& 
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib_Q}}
    \\
    Y &\underset{\eta_Y}{\longrightarrow}& Q(Y)
  }
  \,.
$$

Here $\tilde i$ is a weak equivalence by assumption that the diagram exhibits a [[homotopy pullback]]. Hence it factors as

$$
  \tilde i
  \;\colon\;
  X 
    \underoverset{\in W \cap Cof}{j}{\longrightarrow}
  \hat X
    \underoverset{\in W \cap Fib = W_Q \cap Fib_Q}{\pi}{\longrightarrow}
  Y \underset{Q(Y)}{\times} Z
  \,.
$$

This yields the situation

$$
  \array{
    X &\overset{=}{\longrightarrow}& X
    \\
    {}^{\mathllap{j}}_{\mathllap{\in W \cap Cof}}\downarrow 
      &{}^{\mathllap{\exists}}\nearrow& 
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib}}
    \\
    \hat X
      &\underoverset{\tilde p \circ \pi}{\in Fib_Q}{\longrightarrow}&
    Y
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    X 
      &\overset{j}{\longrightarrow}& 
    \hat X 
      &\overset{\exists}{\longrightarrow}&
    X
    \\
    {}^{\mathllap{}f}\downarrow 
      &&
    \downarrow^{\mathrlap{\tilde p \circ \pi}}
      &&
    \downarrow^{\mathrlap{f}}
    \\
    Y &=& Y &=& Y
  } 
  \,.
$$

As in the [[retract argument]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#RetractArgument)) this diagram exhibits $f$ as a [[retract]] (in the [[arrow category]], [rmk.](Introduction+to+Stable+homotopy+theory+--+P#RetractsOfMorphisms)) of the $Q$-fibration $\tilde p \circ \pi$. Hence by the existence of the $Q$-model structure (prop. \ref{BousfieldFriedlanderTheorem}) and by the closure properties for fibrations ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfInjectiveAndProjectiveMorphisms)), also $f$ is a $Q$-fibration.

Now for the converse. Assume that $f$ is a $Q$-fibration. Since $\mathcal{C}_Q$ is a [[Bousfield localization of model categories|left Bousfield localization]] of $\mathcal{C}$ (prop. \ref{BousfieldFriedlanderTheorem}), $f$ is also a fibration. We need to show that the $\eta$-naturality square on $f$ exhibits a homotopy pullback.

So factor $Q(f)$ as before, and consider the pasting composite of the factorization of the given square with the naturality squares of $\eta$:

$$
  \array{
    X 
      &\underoverset{\in W_Q}{\eta_X}{\longrightarrow}&
    Q(X) 
      &\underoverset{\in W \subset W_Q}{\eta_{Q(X)}}{\longrightarrow}&
    Q(Q(X))
    \\
    {}^{\mathllap{\tilde i}}_{\mathllap{\in W_Q}}\downarrow
      && 
    {}^{\mathllap{i}}_{\mathllap{\in W\subset W_Q}}\downarrow
      && 
    \downarrow^{\mathrlap{Q(i)}}_{\mathrlap{\in W}}
    \\
    Y \underset{Q(Y)}{\times} Z 
      &\underoverset{\in W_Q}{p^\ast \eta_Y}{\longrightarrow}&
    Z
      &\underoverset{\in W}{\eta_Z}{\longrightarrow}&
    Q(Z)
    \\
    {}^{\mathllap{\tilde p}}_{\mathllap{\in Fib_Q}}\downarrow 
      &(pb)& 
    \downarrow^{\mathrlap{p}}_{\mathrlap{\in Fib_Q \subset Fib}}
      &&
    \downarrow^{\mathrlap{Q(p)}}
    \\
    Y 
      &\underoverset{\eta_Y}{\in W_Q}{\longrightarrow}& 
    Q(Y)
      &\underoverset{\eta_{Q(Y)}}{\in W \subset W_Q}{\longrightarrow}&
    Q(Q(Y))
  }
  \,.
$$

Here the top and bottom horizontal morphisms are weak ($Q$-)equivalences by the idempotency of $Q$, and $Q(i)$ is a weak equivalence since $Q$ preserves weak equivalences (first and second clause in def. \ref{QuillenIdempotentMonad}). Hence by [[two-out-of-three]] also $\eta_Z$ is a weak equivalence. From this, lemma \ref{SecondLemmaForBousfieldFriedlander} gives that $p$ is a $Q$-fibration.
Then $p^\ast \eta_Y$ is a $Q$-weak equivalence since it is the pullback of a $Q$-weak equivalence along a fibration between objects whose $\eta$ is a weak equivalence, via the third clause in def. \ref{QuillenIdempotentMonad}. Finally [[two-out-of-three]] implies that $\tilde i$ is a $Q$-weak equivalence.

In particular, the bottom right square is a homotopy pullback (since two opposite edges are weak equivalences, by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyPullbackOfWeakEquivalences)), and since the left square is a genuine pullback of a fibration, hence a homotopy pullback, the total bottom rectangle here exhibits a homotopy pullback by the [[pasting law]] for homotopy pullbacks ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfHomotopyPullbacks)).

Now by [[natural transformation|naturality]] of $\eta$, that total bottom rectangle is the same as the following rectangle

$$
  \array{
    Y \underset{Q(Y)}{\times} Z 
      &\overset{\eta_{\left(Q \underset{Q(Y)}{\times} Z\right)}}{\longrightarrow}&
    Q(Y \underset{Q(Y)}{\times} Z)
      &\underoverset{\in W}{Q(p^\ast \eta_Y)}{\longrightarrow}&
    Q(Z)
    \\
    {}^{\mathllap{\tilde p}}_{\mathllap{\in Fib_Q}}\downarrow 
      && 
    \downarrow^{\mathrlap{Q(\tilde p)}}_{\mathrlap{}}
      &&
    \downarrow^{\mathrlap{Q(p)}}
    \\
    Y 
      &\underset{\eta_Y}{\longrightarrow}& 
    Q(Y)
      &\underoverset{Q(\eta_Y)}{\in W}{\longrightarrow}&
    Q(Q(Y))
  }
  \,,
$$

where now $Q(p^\ast \eta_Y) \in W$ since $p^\ast \eta_Y \in W_Q$, as we had just established. This means again that the right square is a homotopy pullback ([prop.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyPullbackOfWeakEquivalences)), and since the total rectangle still is a homotopy pullback itself, by the previous remark, so is now also the left square, by the other direction of the [[pasting law]] for homotopy pullbacks ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfHomotopyPullbacks)).

So far this establishes that the $\eta$-naturality square of $\tilde p$ is a homotopy pullback. We still need to show that also the $\eta$-naturality square of $f$ is a homotopy pullback. 

Factor $\tilde i$ as a cofibration followed by an acyclic fibration. Since $\tilde i$ is also a $Q$-weak equivalence, by the above, [[two-out-of-three]] for $Q$-fibrations gives that this factorization is of the form

$$
  \array{
    X
      &\underoverset{\in W_Q \cap Cof = W_Q \cap Cof_Q}{j}{\longrightarrow}&
   \hat X
      &\underoverset{\in W \cap Fib = W_Q \cap Fib_Q }{\pi}{\longrightarrow}&
   Y\underset{Q(Y)}{\times} Z
  }
  \,.
$$

As in the first part of the proof, but now with $(W \cap Cof, Fib)$ replaced by $(W_Q \cap Cof_Q, Fib_Q)$ and using lifting in the $Q$-model structure, this yields the situation 

$$
  \array{
    X &\overset{=}{\longrightarrow}& X
    \\
    {}^{\mathllap{j}}_{\mathllap{\in W_Q \cap Cof_Q}}\downarrow 
      &{}^{\mathllap{\exists}}\nearrow& 
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib_Q}}
    \\
    \hat X
      &\underoverset{\tilde p \circ \pi}{}{\longrightarrow}&
    Y
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    X 
      &\overset{j}{\longrightarrow}& 
    \hat X 
      &\overset{\exists}{\longrightarrow}&
    X
    \\
    {}^{\mathllap{}f}\downarrow 
      &&
    \downarrow^{\mathrlap{\tilde p \circ \pi}}
      &&
    \downarrow^{\mathrlap{f}}
    \\
    Y &=& Y &=& Y
  } 
  \,.
$$

As in the [[retract argument]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#RetractArgument)) this diagram exhibits $f$ as a [[retract]] (in the [[arrow category]], [rmk.](Introduction+to+Stable+homotopy+theory+--+P#RetractsOfMorphisms)) of $\tilde p \circ \pi$.

Observe that the $\eta$-naturality square of the weak equivalence $\pi$ is a [[homotopy pullback]], since $Q$ preserves weak equivalences (first clause of def. \ref{QuillenIdempotentMonad}) and since a square with two weak equivalences on opposite sides is a homotopy pullback ([prop.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyPullbackOfWeakEquivalences)). It follows that also the $\eta$-naturality square of $\tilde p \circ \pi$ is a homotopy pullback, by the [[pasting law]] for homotopy pullbacks ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfHomotopyPullbacks)).

In conclusion, we have exhibited $f$ as a [[retract]] (in the [[arrow category]], [rmk.](Introduction+to+Stable+homotopy+theory+--+P#RetractsOfMorphisms)) of a morphism $\tilde p \circ \pi$ whose $\eta$-naturality square is a homotopy pullback. By [[natural transformation|naturality]] of $\eta$, this means that the whole $\eta$-naturality square of $f$ is a retract (in the category of commuting squares in $\mathcal{C}$) of a homotopy pullback square. This means that it is itself a homotopy pullback square ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ClosurePropertiesOfHomotopyPullbacks)).

=--

## Examples

### Stable model structure on sequential spectra

The [[Bousfield-Friedlander model structure]] $SeqSpectra_{stable}$ on [[sequential spectra]] (in any [[proper model category|proper]], [[pointed category|pointed]] [[simplicial model category]]), modelling [[stable homotopy theory]], arises via the Bousfield-Friedlander theorem from localizing the strict model structure $SeqSpectra_{strict}$ [[transferred model structure|transferred]] from the model structure on sequences (in the [[classical model structure on simplicial sets]]/[[classical model structure on topological spaces|on topological spaces]]) at $Q$ being the [[spectrification]] endofunctor.

(For pre-spectra in the [[classical model structure on simplicial sets]], [[spectrification]] is readily defined, more generally one needs to prooceed as in [Schwede 97, section 2.1](spectrification#Schwede97).)


## References

The theorem is due to 

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], section A.3 of  _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf))

and in improved form due to 

* {#Bousfield01} [[Aldridge Bousfield]], section 9 of _On the telescopic homotopy theory of spaces_, Trans. Amer. Math. Soc. 353 (2001), no. 6, 2391&#8211;2426 ([AMS](http://www.ams.org/journals/tran/2001-353-06/S0002-9947-00-02649-0/), [jstor](http://www.jstor.org/stable/221952))


The right-properness condition is shown to be unnecessary in 

* {#Stanculescu08} Alexandru E. Stanculescu, _Note on a theorem of Bousfield and Friedlander_, Topology Appl. 155 (2008), no. 13, 1434--1438 ([arXiv:0806.4547](http://arxiv.org/abs/0806.4547))

Textbook accounts include

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], section X.4 of _[[Simplicial homotopy theory]]_, (1996)

