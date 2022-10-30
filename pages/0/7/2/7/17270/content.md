
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

The original proof assumed that $\mathcal{C}$ is a [[proper model category]], but this condition turns out not to be necessary ([Stanculescu 08, theorem 1.1](#Stanculescu08)).

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

1. (preservation of homotopy pullbacks) if in a [[pullback]] square in $\mathcal{C}$

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

   1. $f$ is a fibration and $Y$ is fibrant;

   1. $\eta_X$, $\eta_Y$, and $Q(h)$ are weak equivalences

   then $Q(f^\ast h)$ is a weak equivalence.

=--


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

It is clear from the definition that an acyclic fibration is also a  $Q$-acyclic $Q$-fibration. In the other direction, let $f$ be a $Q$-acyclic $Q$-fibration. Consider its factorization into a cofibration followed by an acyclic fibration

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

([Bousfield-Friedlander 78, theorem 8.7](#BousfieldFriedlander78), [Bousfield 01, theorem 9.3 ](#Bousfield01), [Goerss-Jardine 96, lemma 4.5, lemma 4.6](#GoerssJardine96))


+-- {: .proof}
###### Proof

The existence of [[limits]] and [[colimits]] is guaranteed since $\mathcal{C}$ is already assumed to be a model category.
The [[two-out-of-three]] poperty for $Q$-weak equivalences is an immediate consequence of two-out-of-three for the original weak equivalences of $\mathcal{C}$. 

Moreover, according to lemma \ref{FirstLemmaForBousfieldFriedlander} the pair of classes $(Cof_{Q}, W_Q \cap Fib_Q)$ equals the pair $(Cof, W \cap Fib)$, and this is a [[weak factorization system]] by the model structure $\mathcal{C}$.

Hence it remains to show that $(W_Q \cap Cof_Q, \; Fib_Q)$ is a [[weak factorization system]]. The lifting property here holds by definition of $Fib_Q$. We conclude by showing the existence of factorizations:

First we consider the case of morphisms of the form $f \colon Q(Y) \to Q(Y)$. This may be factored with respect to $\mathcal{C}$ as

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
  Z
    &\underset{}{\longrightarrow}&
  Q(Y)
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

Now for $g$ an arbitrary morphism $g \colon X \to Y$, form a factorization of $Q(g)$ as above and then decompose the naturality square for $\eta$ on $f$ into the pullback of the resulting $Q$-fibration along $\eta_Y$:

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


+-- {: .num_prop}
###### Proposition

For $Q \colon \mathcal{C} \longrightarrow \mathcal{C}$
a Quillen idempotent monad according to def. \ref{QuillenIdempotentMonad},
then in the model structure $\mathcal{C}_Q$ from prop. \ref{BousfieldFriedlanderTheorem},
a morphism $f\colon X \to Y$ is a $Q$-fibration precisely if 

1. $f$ is a fibration;

1. the $\eta$-naturality square on $f$ exhibits a [[homotopy pullback]]

   $$
     \array{
       X &\stackrel{\eta_X}{\longrightarrow}& Q(X)
       \\
       {}^{\mathllap{f}}\downarrow &{}^{(pb)^h}& \downarrow^{\mathrlap{Q(f)}}
       \\
       Y &\underset{\eta_Y}{\longrightarrow}& Q(Y)
     }
     \,.
   $$

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


The properness condition is shown to be unnecessary in 

* {#Stanculescu08} Alexandru E. Stanculescu, _Note on a theorem of Bousfield and Friedlander_, Topology Appl. 155 (2008), no. 13, 1434--1438 ([arXiv:0806.4547](http://arxiv.org/abs/0806.4547))

Textbook accounts include

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], section X.4 of _[[Simplicial homotopy theory]]_, (1996)

