
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The classical _Brown representability theorem_ ([Brown 62](#Brown62), [Adams 71](#Adams71)) says contravariant [[functors]] on the (pointed) [[classical homotopy category]] satisfying two conditions ("[[Brown functors]]") are [[representable functor|representable]].  

This is used notably to show that every additive reduced [[generalized (Eilenberg-Steenrod) cohomology]] theory $E^\bullet$ is representable by a [[spectrum]] $E$ as 

$$
  E^n(X) \simeq [X,E_n]
  \,.
$$

(But beware that the cohomology theory in general contains less information than the spectrum, due to [[phantom maps]] (see also this [MO discussion](http://mathoverflow.net/q/117684/381)).) 

The Brown representability theorem as such, with the two conditions on a [[Brown functor]] understood, only applies to [[contravariant functors]], not to covariant functors.  But by way of [[Spanier-Whitehead duality]] it implies at least over [[finite CW-complexes]] that dually every additive [[generalized homology theory]] $E_\bullet$ is representable by a spectrum $E$ via

$$
  E_n(X) \simeq \pi_n(E_n \wedge X)
  \,.
$$ 

There are various generalizations, such as to [[triangulated category|triangulated categories]] ([Neeman 96](#Neeman96)), to [[homotopy category of a model category|homotopy categories of]] various [[model categories]] ([Jardine 09](#Jardine09)) and [[homotopy category of an (infinity,1)-category|homotopy categories of]]  [[(∞,1)-categories]] ([Lurie, theorem 1.4.1.2](#LurieHigherAlgebra)).  But in any case there are some crucial conditions for the theorem to apply, such as

* [[group]] structure on the values of the functor, as is the case for an (abelian) cohomology theory, and as would be the case for a represented functor in any [[additive category]], 

OR

* the existence of a [[strong generator]] in the homotopy category in question.

In particular, there is no Brown representability theorem for functors from the homotopy category of pointed not-necessarily-connected spaces to pointed sets, or for functors from the homotopy category of unpointed spaces to sets.  In fact, there are counterexamples in these two cases ([Freyd-Heller 93](#FreydHeller93), see remark \ref{Counterexamples}).


## Classical formulation for homotopy functors on topological spaces
 {#ClassicalFormulation}


Let $Ho(Top_*^c)$ denote the [[homotopy category]] of connected [[pointed topological spaces]] under [[weak homotopy equivalence]] --- or equivalently the homotopy category of pointed connected [[CW complexes]] under [[homotopy equivalence]].  Then $Ho(Top_*^c)$ has [[coproducts]] (given by [[wedge sums]]) and also [[weak limit|weak pushouts]] (namely, [[homotopy pushouts]], see at [weak limit](weak+limit#RelationToHomotopyLimits)).

+-- {: .num_theorem #ClassicalBrownRepresentabilityTheorem}
###### Theorem
**(Brown-Adams)**

A [[functor]] $F:Ho(Top_*^c)^{op} \to Set_*$ is [[representable functor|representable]] precisely if

1. it [[preserved limit|takes]] [[coproducts]] to [[products]], 

1. it takes  [[weak pushouts]] to  [[weak pullbacks]].  

=--

(e.g. [Aguilar-Gitler-Prito 02, theorem 12.2.18](#AguilarGitlerPrito02)).

Note that it is immediate that every representable functor has the given properties; the nontrivial statement is that these properties already characterize representable functors.

When the theorem is stated in terms of CW complexes, the second property (taking [[weak pushouts]] to [[weak pullbacks]]) is often phrased equivalently as:

* The **Mayer-Vietoris axiom**: For every [[CW-pair|CW-triple]] $(X; A_1, A_2)$ (with $A_1\cup A_2 = X$) and any elements $x_1\in F(A_1)$, $x_2\in F(A_2)$ such that $x_1|A_1\cap A_2 = x_2|A_1\cap A_2$, there exists $y\in F(X)$ such that $y|A_1 = x_1$ and $y|A_2 = x_2$.

+-- {: .num_remark #Counterexamples}
###### Remark
**(counterexamples)**
 
The statement of theorem \ref{ClassicalBrownRepresentabilityTheorem} without the restriction to *connected* pointed spaces is false, as is the analogous statement for unpointed spaces.

In ([Freyd-Heller 93](#FreydHeller93)), it is shown that if $G$ is [[Thompson's group F]], with $g:G\to G$ its canonical endomorphism, then $g$ does not [[split idempotent|split]] in the quotient of [[Grp]] by conjugacy.  Since the quotient of [[Grp]] by conjugacy embeds as the full subcategory of the unpointed homotopy category $Ho(Top)$ on connected [[homotopy 1-types]], we have an endomorphism $B g:B G \to B G$ of the [[classifying space]] of $G$ which does not split in $Ho(Top)$.

Thus, if $F:Ho(Top)^{op} \to Set$ splits the idempotent $[-,B g]$ of $[-,B G]$, then $F$ satisfies the hypotheses of the Brown representability theorem (being a [[retract]] of a representable functor), but is not representable.  A similar argument using $B G_+$ applies to $Ho(Top_*)$.

There is also another example due to Heller, which fails to be representable for cardinality reasons.

* MO questions [non-connected spaces](http://mathoverflow.net/questions/104866/brown-representability-for-non-connected-spaces), [unpointed spaces](http://mathoverflow.net/questions/11456/unpointed-brown-representability-theorem)
* [blog post](http://golem.ph.utexas.edu/category/2012/08/brown_representability.html)

=--

## For homotopy functors on presentable $(\infty,1)$-categories
 {#InInfinity1Categories}

The [classical formulation](#ClassicalFormulation) of Brown representability is only superficially concerned with [[topological spaces]]. Instead, via the [[classical model structure on topological spaces]], one finds that the statement only concerns the [[simplicial localization]] of [[Top]] at the [[weak homotopy equivalences]], hence the [[(∞,1)-category]] $L_{whe} Top\simeq $ [[∞Grpd]].

We discuss now the natural formulation of the Brown representability theorem for functors out of [[homotopy categories of (∞,1)-categories]] following ([Lurie, section 1.4.1](#LurieHigherAlgebra)). See also the exposition in ([Mathew 11](#Mathew11)).

+-- {: .num_defn #BrownFunctorOnInfinityCategory}
###### Definition

Let $\mathcal{C}$ be a [[locally presentable (∞,1)-category]]. A [[functor]]

$$
  F \;\colon\; Ho(\mathcal{C})^{op} \longrightarrow Set
$$

(from the [[opposite category|opposite]] of the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathcal{C}$ to [[Set]])

is called a **[[Brown functor]]** if 

1. it sends small [[coproducts]] to [[products]];

1. it sends [[(∞,1)-pushouts]] in $\mathcal{C}\to Ho(\mathcal{C})$ to [[weak pullbacks]] in [[Set]]. 

=--

+-- {: .num_remark #WeakPullbacks}
###### Remark

A _[[weak pullback]]_ is a diagram that satisfies the existence clause of a [[pullback]], but not necessarily the uniqueness condition. Hence the second clause in def. \ref{BrownFunctorOnInfinityCategory} says that for a [[(∞,1)-pushout]] square 

$$
  \array{
    Z &\longrightarrow& X
    \\
    \downarrow &\swArrow& \downarrow
    \\
    Y &\longrightarrow& X \underset{Z}{\sqcup}Y 
  }
$$

in $\mathcal{C}$, then the induced universal morphism


$$
  F\left(X \underset{Z}{\sqcup}Y\right)
  \stackrel{epi}{\longrightarrow}
  F(X) \underset{F(Z)}{\times} F(Y)
$$

into the actual [[pullback]] is an [[epimorphism]].

=--

+-- {: .num_defn #CompactGenerationByCogroupObjects}
###### Definition

Say that  a [[locally presentable (∞,1)-category]] $\mathcal{C}$
is **compactly generated by cogroup objects closed under suspensions** if


1. $\mathcal{C}$ is [[compactly generated (∞,1)-category|generated]] by a set

   $$
    \{S_i \in \mathcal{C}\}_{i \in I}
   $$

   of [[compact object in an (infinity,1)-category|compact objects]] (i.e. every object of $\mathcal{C}$ is an [[(∞,1)-colimit]] of the objects $S_i$.)

1. each $S_i$ admits the structure of a [[cogroup]] object in the [[homotopy category of an (infinity,1)-category|homotopy category]] $Ho(\mathcal{C})$;

1. the set $\{S_i\}$ is closed under forming [[reduced suspensions]].

=--

+-- {: .num_example #SuspensionsAreHCogroupObjects}
###### Example
**([[suspensions are H-cogroup objects]])**

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-colimits]] and with a [[zero object]]. Write $\Sigma \colon X \mapsto 0 \underset{X}{\coprod} 0$ for the [[reduced suspension]] functor.

Then the [[fold map]]

$$
  \Sigma X \coprod \Sigma X
    \simeq
  0 \underset{X}{\sqcup} 0 \underset{X}{\sqcup} 0
    \longrightarrow
  0 \underset{X}{\sqcup} X \underset{X}{\sqcup} 0
  \simeq
  0 \underset{X}{\sqcup} 0
  \simeq
  \Sigma X
$$

exhibits [[cogroup]] structure on the image of any [[suspension object]] $\Sigma X$ in the [[homotopy category of an (∞,1)-category|homotopy category]].

This is equivalently the [[group]]-structure of the first ([[fundamental group|fundamental]]) [[homotopy group]] of the values of [[representable functor|functor co-represented]] by $\Sigma X$:

$$
  Ho(\mathcal{C})(\Sigma X, -)
   \;\colon\;
  Y 
   \mapsto
  Ho(\mathcal{C})(\Sigma X, Y)
   \simeq
  Ho(\mathcal{C})(X, \Omega Y)
   \simeq
  \pi_1 Ho(\mathcal{C})(X, Y)
  \,.
$$

=--

+-- {: .num_example #TheClassicalPointedConnectedHomotopyCategoryAsDomainForTheAbstractBrownRepresentabilityTheorem}
###### Example

In bare [[pointed homotopy types]] $\mathcal{C} = $[[∞Grpd]]${}^{\ast/}$, the ([[homotopy types]] of) [[n-spheres]] $S^n$ are [[cogroup]] objects for $n \geq 1$, but not for $n = 0$, by example \ref{SuspensionsAreHCogroupObjects}. And of course they are [[compact object in an (∞,1)-category|compact objects]]. 

So while $\{S^n\}_{n \in \mathbb{N}}$ generates all of $\infty Grpd^{\ast/}$, the latter is _not_ an example of def. \ref{CompactGenerationByCogroupObjects} due to the failure of $S^0$ to have [[cogroup]] structure.

Removing that generator, the $(\infty,1)$-category generated by $\{S^n\}_{{n \in \mathbb{N}} \atop {n \geq 1}}$ is $\infty Grpd^{\ast/}_{\geq 1}$, that of _[[connected object|connected]]_ [[pointed homotopy types]]. This is one way to see how the connectedness condition in the classical version of Brown representability theorem arises.

=--

See also ([Lurie, example 1.4.1.4](#LurieHigherAlgebra))

In $\infty$-categories compactly generated by cogroup objects closed under forming suspensions, the following strenghtening of the [[Whitehead theorem]] holds.

+-- {: .num_prop #WhiteheadTheoremForCompactGenerationByCogroupObjects}
###### Proposition

In an $(\infty,1)$-category compactly generated by cogroup objects $\{S_i\}_{i \in I}$ closed under forming suspensions, according to def. \ref{CompactGenerationByCogroupObjects}, a morphism $f\colon X \longrightarrow Y$ is an [[equivalence in an (infinity,1)-category|equivalence]] precisely if for each $i \in I$ the induced function of maps in the [[homotopy category of an (infinity,1)-category|homotopy category]]

$$
  Ho(\mathcal{C})(S_i,f)
  \;\colon\;
  Ho(\mathcal{C})(S_i,X)
   \longrightarrow
  Ho(\mathcal{C})(S_i,Y)
$$

is an [[isomorphism]] (a [[bijection]]).

=--

([Lurie, p. 114, Lemma star](#LurieHigherAlgebra))

+-- {: .proof }
###### Proof

By the [[(∞,1)-Yoneda lemma]], the morphism $f$ is an [[equivalence in an (∞,1)-category|equivalence]] precisely if for all objects $A \in \mathcal{C}$  the induced morphism 

$$
  \mathcal{C}(A,f)
  \;\colon\;
  \mathcal{C}(A,X)
   \longrightarrow
  \mathcal{C}(A,Y)
$$

is an equivalence in [[∞Grpd]]. By assumption of compact generation and since the hom-functor $\mathcal{C}(-,-)$ sends $\infty$-colimits in the first argument to $\infty$-limits, this is the case precisely already if it is the case for $A \in \{S_i\}_{i \in I}$.

Now by the standard [[Whitehead theorem]] in [[∞Grpd]] (being a [[hypercomplete (∞,1)-topos]]), the morphisms

$$
  \mathcal{C}(S_i,f)
  \;\colon\;
  \mathcal{C}(S_i,X)
   \longrightarrow
  \mathcal{C}(S_i,Y)
$$

in [[∞Grpd]] are  [[equivalence in an (∞,1)-category|equivalences]] precisely if they are [[weak homotopy equivalences]], hence precisely if they induce [[isomorphisms]] on all [[homotopy groups]] $\pi_n$ for **all basepoints**.

It is this last condition of testing on all basepoints that the assumed [[cogroup]] structure on the $S_i$ allows to do away with: this cogroup structure implies that $\mathcal{C}(S_i,-)$ has the structure of an $H$-group, and this implies (by group multiplication), that all [[connected components]] have the same homotopy groups, hence that all homotopy groups are independent of the choice of basepoint, up to isomorphism.

Therefore the above morphisms are equivalences precisely if they are so under applying $\pi_n$ based on the connected component of the [[zero morphism]]

$$
  \pi_n\mathcal{C}(S_i,f)
    \;\colon\;
  \pi_n \mathcal{C}(S_i,X)
     \longrightarrow
  \pi_n\mathcal{C}(S_i,Y)
  \,.
$$

Now in this pointed situation we may use that 

$$
  \begin{aligned}
    \pi_n \mathcal{C}(-,-) & \simeq \pi_0 \mathcal{C}(-,\Omega^n(-)) 
    \\
    & \simeq \pi_0\mathcal{C}(\Sigma^n(-),-)
    \\
    & \simeq Ho(\mathcal{C})(\Sigma^n(-),-)
  \end{aligned}
$$

to find that $f$ is an equivalence in $\mathcal{C}$ precisely if the induced morphisms

$$
  Ho(\mathcal{C})(\Sigma^n S_i, f)
    \;\colon\;
  Ho(\mathcal{C})(\Sigma^n S_i,X)
    \longrightarrow
  Ho(\mathcal{C})(\Sigma^n S_i,Y)
$$

are isomorphisms for all $i \in I$ and $n \in \mathbb{N}$.

Finally by the assumption that each suspension $\Sigma^n S_i$ of a generator is itself among the set of generators, the claim follows.

=--

+-- {: .num_theorem #BrownRepresentabilityOnPresentableInfinityCategories}
###### Theorem
**(Brown representability)**

Let $\mathcal{C}$ be an $(\infty,1)$-category compactly generated by cogroup objects closed under forming suspensions, according to def. \ref{CompactGenerationByCogroupObjects}. Then a [[functor]]

$$
  F \;\colon\; Ho(\mathcal{C})^{op} \longrightarrow Set
$$

(from the [[opposite category|opposite]] of the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathcal{C}$ to [[Set]])
is [[representable functor|representable]] precisely if it is a [[Brown functor]], def. \ref{BrownFunctorOnInfinityCategory}.

=--

([Lurie, theorem 1.4.1.2](#LurieHigherAlgebra))

+-- {: .proof #ProofFollowingLurie}
###### Proof


Due to the version of the Whitehead theorem of prop. \ref{WhiteheadTheoremForCompactGenerationByCogroupObjects} we are essentially reduced to showing that [[Brown functors]] $F$ are representable on the $S_i$. To that end consider the following lemma.
(In the following we notationally identify, via the [[Yoneda lemma]], objects of $\mathcal{C}$, hence of $Ho(\mathcal{C})$, with the functors they [[representable functor|represent]].)

Lemma ($\star$): _Given $X \in \mathcal{C}$ and $\eta \in F(X)$, hence $\eta \colon X \to F$, then there exists a morphism $f \colon X \to X'$ and an [[extension]] $\eta' \colon X' \to F$ of $\eta$ which induces for each $S_i$ a [[bijection]] $\eta'\circ (-) \colon Ho(\mathcal{C})(S_i,X') \stackrel{\simeq}{\longrightarrow} PSh(Ho(\mathcal{C}))(S_i,F) \simeq F(S_i)$._

To see this, first notice that we may directly find an extension $\eta_0$ along a map $X\to X_o$ such as to make a [[surjection]]: simply take $X_0$ to be the [[coproduct]] of **all** possible elements in the codomain and take

$$
  \eta_0
  \;\colon\;
   X 
     \sqcup
   \left(
     \underset{{i \in I,} \atop {\gamma \colon S_i \stackrel{}{\to} F}}{\coprod} 
     S_i
   \right)
   \longrightarrow
   F
$$

to be the canonical map. (Using that $F$, by assumption, turns coproducts into products, we may indeed treat the coproduct in $\mathcal{C}$ on the left as the coproduct of the corresponding functors.)

To turn the surjection thus constructed into a bijection, we now successively form quotients of $X_0$. To that end proceed by [[induction]] and suppose that $\eta_n \colon X_n \to F$ has been constructed. Then for $i \in I$ let

$$
  K_i 
    \coloneqq 
  ker
  \left( 
     Ho(\mathcal{C})(S_i, X_n) 
        \stackrel{\eta_n \circ (-)}{\longrightarrow} 
     F(S_i) 
   \right)
$$

be the [[kernel]] of  $\eta_n$ evaluated on $S_i$. These $K_i$ are the pieces that need to go away in order to make a bijection. Hence define $X_{n+1}$ to be their joint [[homotopy cofiber]]

$$
  X_{n+1} 
     \coloneqq 
   coker\left(
     \left(
        \underset{{i \in I,} \atop {\gamma \in K_i}}{\sqcup} S_i
     \right)
     \overset{(\gamma)_{{i \in I} \atop {\gamma\in K_i}}}{\longrightarrow}
     X_n
  \right)
  \,.
$$

Then by the assumption that $F$ takes this homotopy cokernel to a [[weak limit|weak]] [[fiber]] (as in remark \ref{WeakPullbacks}), there exists an extension $\eta_{n+1}$ of $\eta_n$ along $X_n \to X_{n+1}$:

$$
  \array{
    \left(
      \underset{{i \in I}\atop {\gamma \in K_i}}{\sqcup} S_i
    \right)
    &\overset{(\gamma)_{{i \in I}\atop \gamma \in K_i}}{\longrightarrow}&
    X_n
    &\overset{\eta_n}{\longrightarrow}& F
    \\
    \downarrow &(po^{h})& \downarrow & \nearrow_{\mathrlap{\exists \eta_{n+1}}}
    \\
    \ast &\longrightarrow& X_{n+1}
  }
  \;\;\;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;\;\;
  \array{
    && F(X_{n+1}) &\longrightarrow& \ast 
    \\
    &{}^{\mathllap{\exists \eta_{n+1}}}\nearrow& \downarrow^{\mathrlap{epi}} && \downarrow
    \\
    \ast &\overset{\eta_n}{\longrightarrow}& ker\left((\gamma^\ast\right)_{{i \in I} \atop {\gamma \in K_i}}) &\longrightarrow& \ast 
    \\
    &{}_{\mathllap{\eta_n}}\searrow& \downarrow &(pb)& \downarrow
    \\
    && F(X_n)
    &\underset{(\gamma^\ast)_{{i \in I} \atop {\gamma \in K_i}} }{\longrightarrow}&
    \underset{{i \in I}\atop {\gamma\in K_i}}{\prod}F(S_i)
  }
  \,.
$$

It is now clear that we want to take

$$
  X' \coloneqq \underset{\rightarrow}{\lim}_n X_n
$$

and extend all the $\eta_n$ to that colimit. Since we have no condition for evaluating $F$ on colimits other than pushouts, observe that this [[sequential colimit]] is equivalent to the following pushout:

$$
  \array{
    \underset{n}{\sqcup} X_n
    &\longrightarrow& \underset{n}{\sqcup} X_{2n}
    \\
    \downarrow &(po^h)& \downarrow
    \\
    \underset{n}{\sqcup} X_{2n+1} &\longrightarrow& X'
  }
  \,,
$$

where the components of the top and left map alternate between the identity on $X_n$ and the above successor maps $X_n \to X_{n+1}$.
Now the excision property of $F$ applies to this pushout, and we conclude the desired  extension $\eta' \colon X' \to F$:

$$
  \array{
    && \underset{n}{\sqcup} X_n
    \\
    & \swarrow && \searrow
    \\
    \underset{n}{\sqcup} X_{2n+1} &\longrightarrow& X' &\longleftarrow& \underset{n}{\sqcup} X_{2n}
    \\
    & {}_{\mathllap{(\eta_{2n+1})_{n}}}\searrow& \downarrow^{\mathrlap{\exists \eta'}} & \swarrow_{\mathrlap{(\eta_{2n})_n}}
    \\
    && F    
  }
  \;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;
  \array{
    && F(X')
    \\
    &{}^{\mathllap{\exists \eta'}}\nearrow& \downarrow^{\mathrlap{epi}}
    \\
    &\ast \overset{(\eta_n)_n}{\longrightarrow}& \underset{\longleftarrow}{\lim}_n F(X_n)
    \\
    & \swarrow && \searrow
    \\
    \underset{n}{\prod}F(X_{2n+1})
    && &&
    \underset{n}{\prod}(X_{2n})
    \\
    & \searrow && \swarrow
    \\
    && \underset{n}{\prod}F(X_n)
  }
  \,,
$$


It remains to confirm that this indeed  gives the desired bijection. Surjectivity is clear. For injectivity use that all the $S_i$ are, by assumption, [[compact object|compact]], hence they may be taken inside the [[sequential colimit]]:

$$
  \array{
    && X_{n(\gamma)}
    \\
    &{}^{\mathllap{ \exists \hat \gamma}}\nearrow& \downarrow
    \\
    S_i 
      &\overset{\gamma}{\longrightarrow}&
    X' 
      = 
    \underset{\longrightarrow}{\lim}_n X_n
  }
  \,.
$$

With this, injectivity follows because by construction we quotiented out the kernel at each stage. Because suppose that $\gamma$ is taken to zero in $F(S_i)$, then by the definition of $X_{n+1}$ above there is a factorization of $\gamma$ through the point:

$$
  \array{
    0 \colon & S_i
    &\overset{\hat \gamma}{\longrightarrow}&
    X_{n(\gamma)}
    &\overset{\eta_n}{\longrightarrow}& F
    \\
    & \downarrow && \downarrow & 
    \\
    & \ast &\longrightarrow& X_{n(\gamma)+1}
    \\
    & && \downarrow
    \\
    & && X'
  }
$$

This concludes the proof of Lemma ($\star$).

Now apply the construction given by this lemma to the case 
$X_0 \coloneqq 0$ and the unique $\eta_0 \colon 0 \stackrel{\exists !}{\to} F$. Lemma $(\star)$ then produces an object $X'$ which represents $F$ on all the $S_i$, and we want to show that this $X'$ actually represents $F$ generally, hence that for every $Y \in \mathcal{C}$ the function

$$
  \theta \coloneqq \eta'\circ (-)
  \;\colon\;
  Ho(\mathcal{C})(Y,X')
   \stackrel{}{\longrightarrow}
  F(Y)
$$

is a [[bijection]].

First, to see that $\theta$ is surjective, we need to find a preimage of any $\rho \colon Y \to F$. Applying Lemma $(\star)$ to $(\eta',\rho)\colon X'\sqcup Y \longrightarrow F$ we get an extension $\kappa$ of this through some $X' \sqcup Y \longrightarrow Z$ and the morphism on the right of the following commuting diagram:

$$
  \array{
    Ho(\mathcal{C})(-,X') && \longrightarrow && Ho(\mathcal{C})(-, Z)
    \\
    & {}_{\mathllap{\eta'\circ(-)}}\searrow && \swarrow_{\mathrlap{\kappa \circ (-)}}
    \\
    && F(-)
  }
  \,.
$$

Moreover, Lemma $(\star)$ gives that evaluated on all $S_i$, the two diagonal morphisms here become isomorphisms. But then prop. \ref{WhiteheadTheoremForCompactGenerationByCogroupObjects} implies that $X' \longrightarrow Z$ is in fact an equivalence. Hence the component map $Y \to Z \simeq Z$ is a lift of $\kappa$ through $\theta$.

Second, to see that $\theta$ is injective, suppose $f,g \colon Y \to X'$ have the same image under $\theta$. Then consider their [[homotopy pushout]]

$$
  \array{
    Y \sqcup Y &\stackrel{(f,g)}{\longrightarrow}& X'
    \\
    \downarrow && \downarrow
    \\
    Y &\longrightarrow& Z
  }
$$
 
along the [[codiagonal]] of $Y$. Using that $F$ sends this to a [[weak pullback]] by assumption, we obtain an extension $\bar \eta$ of $\eta'$ along $X' \to Z$. Applying Lemma $(\star)$ to this gives a further extension $\bar \eta' \colon Z' \to Z$ which now makes the following diagram

$$
  \array{
    Ho(\mathcal{C})(-,X') && \longrightarrow && Ho(\mathcal{C})(-, Z)
    \\
    & {}_{\mathllap{\eta'\circ(-)}}\searrow && \swarrow_{\mathrlap{\bar \eta' \circ (-)}}
    \\
    && F(-)
  }
$$

such that the diagonal maps become isomorphisms when evaluated on the $S_i$. As before, it follows via prop. \ref{WhiteheadTheoremForCompactGenerationByCogroupObjects} that the morphism
$h \colon X' \longrightarrow Z'$ is an equivalence.

Since by this construction $h\circ f$ and $h\circ g$ are homotopic

$$
  \array{
    Y \sqcup Y &\stackrel{(f,g)}{\longrightarrow}& X'
    \\
    \downarrow && \downarrow & \searrow^{\mathrlap{\stackrel{h}{\simeq}}}
    \\
    Y &\longrightarrow& Z &\longrightarrow& Z'
  }
$$

it follows with $h$ being an equivalence that already $f$ and $g$ were homotopic, hence that they represented the same element.


=--




+-- {: .num_defn #GeneralizedCohomologyOnGeneralInfinityCategory}
###### Definition

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[(∞,1)-pushouts]], and with a [[zero object]] $0 \in \mathcal{C}$. Write $\Sigma \colon \mathcal{C} \to \mathcal{C}\colon X\mapsto 0 \underset{X}{\sqcup} 0$ for the corresponding [[suspension]] [[(∞,1)-functor]].

A **reduced additive [[generalized (Eilenberg-Steenrod) cohomology]] theory** on $\mathcal{C}$ is 

1. a [[functor]]

   $$
     H^\bullet \;\colon \; Ho(\mathcal{C})^{op} \longrightarrow Ab^{\mathbb{Z}}
   $$


   (from the [[opposite category|opposite]] of the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathcal{C}$ into $\mathbb{Z}$-[[graded abelian groups]]);

1. a [[natural isomorphisms]] ("[[suspension isomorphisms]]") of degree +1

   $$
     \delta \; \colon \; H^\bullet \longrightarrow H^{\bullet+1} \circ \Sigma
   $$

such that $H^\bullet$ 

1. **(exactness)** takes [[homotopy cofiber sequences]] to [[exact sequences]].

1. **(additivity)** takes small [[coproducts]] to [[products]];


=--

+-- {: .num_defn #ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory}
###### Definition

Given a generalized cohomology theory $(H^\bullet,\delta)$ on some $\mathcal{C}$ as in def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, and given a [[homotopy cofiber sequence]] in $\mathcal{C}$

$$
  X \stackrel{f}{\longrightarrow} Y \stackrel{g}{\longrightarrow} Z
  \stackrel{coker(g)}{\longrightarrow}
  \Sigma X
  \,,
$$

then the corresponding **[[connecting homomorphism]]** is the composite

$$
  \partial 
    \;\colon\; 
  H^\bullet(X)
   \stackrel{\delta}{\longrightarrow}
  H^{\bullet+1}(\Sigma X)
   \stackrel{coker(g)^\ast}{\longrightarrow}
  H^{\bullet+1}(Z)
  \,.
$$

=--

+-- {: .num_prop #LongExactSequenceOfACohomologyTheoryOnAnInfinityCategory}
###### Proposition

The [[connecting homomorphisms]] of def. \ref{ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory} are parts of [[long exact sequences]]

$$
  \cdots
   \stackrel{\partial}{\longrightarrow}
  H^{\bullet}(Z) \longrightarrow H^\bullet(Y) \longrightarrow H^\bullet(X)
  \stackrel{\partial}{\longrightarrow}
  H^{\bullet+1}(Z)
   \to \cdots
  \,.
$$

=--


+-- {: .proof}
###### Proof

By the defining exactness of $H^\bullet$, def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, and the way this appears in def. \ref{ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory}, using that $\delta$ is by definition an isomorphism.

=--

+-- {: .num_prop #CohomologyFunctorOnInfinityCategoryIsBrownFunctor}
###### Proposition

Given a reduced addive generalized cohomology functor $H^\bullet \colon Ho(\mathcal{C})^{op}\to Ab^{\mathbb{Z}}$, def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, its underlying [[Set]]-valued functors $H^n \colon Ho(\mathcal{C})^{op}\to Ab\to Set$ are [[Brown functors]], def. \ref{BrownFunctorOnInfinityCategory}.

=--

+-- {: .proof}
###### Proof

The first condition on a [[Brown functor]] holds by additivity. For the second condition, given a homotopy pushout square


$$
  \array{
    X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{} && \downarrow
    \\
    X_2 &\stackrel{f_2}{\longrightarrow}& Y_2
  }
$$

in $\mathcal{C}$, consider the induced morphism of the [[long exact sequences]] given by prop. \ref{LongExactSequenceOfACohomologyTheoryOnAnInfinityCategory}

$$
  \array{
    H^\bullet(coker(f_2))
      &\longrightarrow&
    H^\bullet(Y_2) 
      &\stackrel{f^\ast_2}{\longrightarrow}& 
    H^\bullet(X_2)
      &\stackrel{}{\longrightarrow}&
    H^{\bullet+1}(\Sigma coker(f_2))
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow && \downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    H^\bullet(coker(f_1))
      &\longrightarrow&
    H^\bullet(Y_1) 
      &\stackrel{f^\ast_1}{\longrightarrow}& 
    H^\bullet(X_1)
      &\stackrel{}{\longrightarrow}&
    H^{\bullet+1}(\Sigma coker(f_1))
  }
$$

Here the outer vertical morphisms are [[isomorphisms]], as shown, due to the [[pasting law]] (see also at _[fiberwise recognition of stable homotopy pushouts](homotopy+pullback#FiberwiseRecognitionInStableCase)_). 
This means that the [[four lemma]] applies to this diagram. Inspection shows that this implies the claim.

=--

+-- {: .num_cor }
###### Corollary

Let $\mathcal{C}$ be an [[(∞,1)-category]] which satisfies the conditions of theorem \ref{BrownRepresentabilityOnPresentableInfinityCategories}, and let $(H^\bullet, \delta)$ be a [[generalized cohomology]] functor on $\mathcal{C}$, def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}. Then there exists a  [[spectrum object]] $E \in Stab(\mathcal{C})$ such that 

1. $H^\bullet$ is degreewise [[representable functor|represented]] by $E$:

   $$
     H^\bullet \simeq Ho(\mathcal{C})(-,E_\bullet)
     \,,
   $$

1. the [[suspension isomorphism]] $\delta$ is given by the structure morphisms $\tilde \sigma_n \colon E_n \to \Omega E_{n+1}$ of the spectrum, in that

   $$
     \delta 
       \colon
     H^n(-)
      \simeq
     Ho(\mathcal{C})(-,E_n)
      \stackrel{Ho(\mathcal{C})(-,\tilde\sigma_n) }{\longrightarrow}
     Ho(\mathcal{C})(-,\Omega E_{n+1})
       \simeq
     Ho(\mathcal{C})(\Sigma (-), E_{n+1})
       \simeq
     H^{n+1}(\Sigma(-))
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Via prop. \ref{CohomologyFunctorOnInfinityCategoryIsBrownFunctor}, theorem \ref{BrownRepresentabilityOnPresentableInfinityCategories} gives the first clause. With this, the second clause follows by the [[(∞,1)-Yoneda lemma]] (in fact just with the [[Yoneda lemma]]).

=--


## Further variants

### For triangulated categories and model categories

For [[triangulated categories]]  a discussion is in ([Neeman 96](#Neeman96)).

For [[model categories]] a discussion is in ([Jardine 09](#Jardine09)):

Let $C$ be a [[model category]] with a [[zero object]] and such that there is a [[set]] $S$ of [[cofibrant object|cofibrant]] [[compact objects]] such that the [[weak equivalences]] in $C$ are precisely the $S$-[[local morphisms]].

([Jardine 09, p. 20](#Jardine09))


+-- {: .num_theorem}
###### Theorem
**(Jardine)**

Let $F : C^{op} \to Set_{*}$ be a pointed [[homotopical functor]] from $C^{op}$ to the category of [[pointed sets]] such that

1. $F$ preserves small [[coproducts]] of cofibrant objects (including preserving the [[zero object]]).

1. **(Mayer-Vietoris property)** $F$ takes any [[pushout]] diagram

   $$
     \array{
       A &\to& X
       \\
       \downarrow^i && \downarrow 
       \\
       B &\to& B \coprod_A X,
     }
   $$  

   with all objects cofibrant and $i$ a cofibration, to a [[weak pullback]].

([Jardine 09, p. 21](#Jardine09))


Then $F$ is [[representable functor|representable]].

=--


([Jardine 09, theorem 24](#Jardine09))



### For $RO(G)$-graded equivariant cohomology
 {#ForEquivariantCohomology}

The generalization of the Brown representability theorem to [[equivariant cohomology]] says that [[RO(G)-grading|RO(G)-graded]] equivariant cohomology is represented by [[genuine G-spectra]] (e.g. [May 96, chapter XIII.3](#May96)).


## Properties

### Multiplicative cohomology and ring spectra

The spectrum Brown-representing a [[multiplicative cohomology theory]] inherits (at least) the structure of an [[H-ring spectrum]]. See [there](multiplicative+cohomology+theory#BrownRepresentabilityByRingSpectra).

## Related concepts

* [[Landweber exact functor theorem]]

## References

The original version of the theorem:

* {#Brown62} [[Edgar Brown]], _Cohomology theories_, Annals of Mathematics, Second Series 75: 467&#8211;484 (1962) ([jstor:1970209](https://www.jstor.org/stable/1970209))

The category-theoretic generalization:

* {#Brown65} [[Edgar Brown]], _Abstract homotopy theory_, Trans. AMS 119 no. 1 (1965) ([doi:10.1090/S0002-9947-1965-0182970-6](https://doi.org/10.1090/S0002-9947-1965-0182970-6))


A simplified version of the proof was spelled out in 

* {#Spanier66} [[Edwin Spanier]], section 7.7 of _Algebraic topology_, McGraw-Hill, 1966

and a strengthening in

* {#Adams71} [[John Frank Adams]], _A variant of E. H. Brown's representability theorem_, Topology, 10:185-198, 1971

Textbook accounts:

* {#Adams74} [[Frank Adams]], part III, section 6 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Switzer75} [[Robert Switzer]], theorem 8.42, theorem 9.27 in _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

* {#Kochmann96} [[Stanley Kochmann]], section 3.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#AguilarGitlerPrito02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], Sections 2.4, 2.5 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))


Quick reviews include

* {#Muro10} [[Fernando Muro]], _Representability of cohomology theories_, 2010 ([pdf](http://personal.us.es/fmuro/praha.pdf))

* {#Lurie}  [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 17 _Phantom maps_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture17.pdf)) 


Generalization to [[triangulated categories]] is discussed in

* {#Neeman96} [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, J. Amer. Math. Soc. 9 (1996), 205-236 ([AMS](http://www.ams.org/journals/jams/1996-9-01/S0894-0347-96-00174-9/))

A [[model category]] version, with applications to [[∞-stacks]] -- or rather to the standard  [[models for ∞-stack (∞,1)-toposes]] in terms of the standard [[model structure on simplicial presheaves]] -- is given in

* {#Jardine09} [[Rick Jardine]], _Representability theorems for simplicial
presheaves_, 2009 ([pdf](http://ncatlab.org/nlab/files/JardineBrownrep.pdf)) 

A version in [[(infinity,1)-category theory]] is in 

* {#LurieHigherAlgebra} [[Jacob Lurie]], section 1.4.1 of _[[Higher Algebra]]_

Exposition of this is in 

* {#Mathew11} [[Akhil Mathew]], _[Brown representability and infinity-categories](https://amathew.wordpress.com/2011/10/10/brown-representability-and-infinity-categories/#more-2907)_, 2011


The case of [[RO(G)-grading|RO(G)-graded]] [[equivariant cohomology]] theory is discussed for instance in

* {#May96} [[Peter May]], chapter XIII.3 of _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))


The counterexamples to nonconnected and unpointed Brown representability are from

* {#FreydHeller93} [[Peter Freyd]], [[Alex Heller]], _Splitting homotopy idempotents. II._ J. Pure App#l. Algebra 89 (1993), no. 1-2, 93&#8211;106.

 

The relation to [[Grothendieck contexts]] ([[six operations]]) is highlighted in 

* {#Neeman96} [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, J. Amer. Math. Soc. 9 (1996), 205-236 ([web](http://www.ams.org/journals/jams/1996-9-01/S0894-0347-96-00174-9/))
 



[[!redirects Brown representability]]

[[!redirects Brown's representability theorem]]