
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

A [[model category]] structure $(\mathcal{C}(W,Fib,Cof))$ on some [[category]] $\mathcal{C}$ is a means to guarantee the [[locally small category|local smallness]] and to improve the tractability of the [[homotopy category]] of the underlying [[category with weak equivalences]] $(\mathcal{C},W)$. In particular, if a [[category with weak equivalences]] admits a [[model category]] structure, then its [[homotopy category]] (in the sense of [[localization]] $\mathcal{C}[W^{-1}]$ at the class of [[weak equivalences]]) is [[equivalence of categories|equivalent]] to the category whose objects are those objects of $\mathcal{C}$ which are both fibrant cofibrant, and whose morphisms are the actual [[homotopy classes]] of morphisms between these objects ([[left homotopy]] or [[right homotopy]] [[equivalence classes]] in the sense of [[homotopy in a model category]]) .

## Definition

+-- {: .num_defn #HomotopyCategoryOfAModelCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]]. Write $Ho(\mathcal{C})$ for the [[category]] whose

* [[objects]] are those objects of $\mathcal{C}$ which are both fibrant and cofibrant;

* [[morphisms]] are the [[homotopy classes]] of morphisms of $\mathcal{C}$, hence the [[equivalence classes]] of morphism under [[left homotopy]].

=--

This is, up to [[equivalence of categories]], the _homotopy category of the model category_ $\mathcal{C}$.

## Universal property

We spell out that def. \ref{HomotopyCategoryOfAModelCategory} indeed satisfies the [[universal property]] that defines the [[homotopy category]] of a [[category with weak equivalences]].

+-- {: .num_lemma #WhiteheadTheoremInModelCategories}
###### Lemma
**([[Whitehead theorem]] in model categories)**

Let $\mathcal{C}$ be a [[model category]]. A [[weak equivalence]] between two objects which are both fibrant and cofibrant is a [[homotopy equivalence]].

=--

(e.g. [Goerss-Jardine 96, part I, theorem 1.10](#GoerssJardine96))

+-- {: .proof}
###### Proof

By the factorization axioms in $\mathcal{C}$, every weak equivalence $f\colon X \longrightarrow Y$ factors through an object $Z$ as an acyclic cofibration followed by an acyclic fibration. In particular it follows that with $X$ and $Y$ both fibrant and cofibrant, so is $Z$, and hence it is sufficient to prove that acyclic (co-)fibrations between such objects are homotopy equivalences.

So let $f \colon X \longrightarrow Y$ be an acyclic fibration between fibrant-cofibrant objects, the case of acyclic cofibrations is [[formal dual|formally dual]]. Then in fact it has a genuine [[right inverse]] given by a lift $f^{-1}$ in the diagram

$$
  \array{
    \emptyset &\rightarrow& X
    \\
    {}^{\mathllap{\in cof}}\downarrow 
     &{}^{{f^{-1}}}\nearrow& 
   \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib \cap W}}
    \\
    X &=& X
  }
  \,.
$$

To see that $f^{-1}$ is also a [[left inverse]] up to [[left homotopy]], let $Cyl(X)$ be any [[cylinder object]] on $X$, hence a factorization of the [[codiagonal]] on $X$ as a cofibration followed by a an acyclic fibration 

$$
  X \sqcup X \stackrel{\iota_X}{\longrightarrow} Cyl(X) \stackrel{\sigma}{\longrightarrow} X
$$

and consider the square

$$
  \array{
    X \sqcup X 
    &\stackrel{(f^{-1}\circ f, id)}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_X}}{}_{\mathllap{\in Cof}}\downarrow && \downarrow^{\mathrlap{f}}_{\mathrlap{\in W \cap Fib}}
    \\
    Cyl(X) &\underset{f\circ \sigma}{\longrightarrow}& y
  }
  \,,
$$

which [[commuting square|commutes]] due to $f^{-1}$ being a genuine right inverse of $f$. By construction, this [[commuting square]] now admits a [[lift]] $\eta$, and that constitutes a [[left homotopy]] $\eta \colon f^{-1}\circ f \Rightarrow_L id$.

=--

+-- {: .num_defn #FibrantCofibrantReplacementFunctorToHomotopyCategory}
###### Definition

Given a [[model category]] $\mathcal{C}$, consider a _choice_ for each object $X \in \mathcal{C}$ of 

1. a factorization $\emptyset \underoverset{\in Cof}{i_X}{\longrightarrow} Q X \underoverset{\in W \cap Fib}{p_x}{\longrightarrow} X$ of the initial morphism, such that when $X$ is already cofibrant then $p_X = id_X$;

1. a factorization $X \underoverset{\in W \cap Cof}{j_X}{\longrightarrow} R X \underoverset{\in Fib}{q_x}{\longrightarrow} \ast$ of the terminal morphism, such that when $X$ is already fibrant then $j_X = id_X$.

Write then 

$$
  \gamma_{R,Q} 
  \;\colon\;
  \mathcal{C}
   \longrightarrow
  Ho(\mathcal{C})
$$

for the [[functor]] to the homotopy category, def. \ref{HomotopyCategoryOfAModelCategory}, which sends an object $X$ to the object $R Q X$ and sends a morphism $f \colon X \longrightarrow Y$ to the [[homotopy class]] of the result of first lifting in 

$$
  \array{
    \emptyset &\longrightarrow& Q Y
    \\
    {}^{\mathllap{i_X}}\downarrow &{}^{Q f}\nearrow& \downarrow^{\mathrlap{p_Y}}
    \\
    Q X &\underset{f\circ p_X}{\longrightarrow}& Y
  }
$$

and then lifting (here: [[extension|extending]]) in 

$$
  \array{ 
    Q X &\overset{j_{Q Y} \circ Q f}{\longrightarrow}& R Q Y
    \\
    {}^{\mathllap{j_{Q X}}}\downarrow &{}^{R Q f}\nearrow& \downarrow^{\mathrlap{q_{Q Y}}}
    \\
    R Q X
    &\longrightarrow&
    \ast
  }
  \,.
$$

=--

+-- {: .num_lemma #ConstructionOfLocalizationFunctorForModelCategoryIsWellDefined}
###### Lemma

The construction in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} is indeed well defined.

=--

+-- {: .proof}
###### Proof

First of all, the object $R Q X$ is indeed both fibrant and cofibrant (as well as related by a [[zig-zag]] of weak equivalences to $X$):  

$$
  \array{
     \emptyset 
     \\
     {}^{\mathllap{\in Cof}}\downarrow & \searrow^{\mathrlap{\in Cof}}
     \\
     Q X &\underset{\in W \cap Cof}{\longrightarrow}& R Q X &\underset{\in Fib}{\longrightarrow}& \ast
     \\
     {}^{\mathllap{\in W}}\downarrow
     \\
     X
  }
  \,.
$$

Now to see that the image on morphisms is well defined. First observe that any two choices $(Q f)_{i}$ of the first lift in the definition are left homotopic to each other, exhibited by lifting in

$$
  \array{
    Q X \sqcup Q X &\stackrel{((Q f)_1, (Q f)_2 )}{\longrightarrow}& Q Y
    \\
    {}^{\mathllap{\in W \cap Cof}}\downarrow 
     && 
    \downarrow^{\mathrlap{p_{Y}}}_{\mathrlap{\in Fib}}
    \\
    Cyl(Q X)
    &\underset{f \circ p_{X} \circ \sigma_{Q X}}{\longrightarrow}& 
    Y
  }
  \,.
$$

Hence also the composites $j_{Q Y}\circ (Q_f)_i $ are [[left homotopy|left homotopic]] to each other, and since their domain is cofibrant, they are also [[right homotopy|right homotopic]] (via [this](homotopy+in+a+model+category#LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually) lemma) by a right homotopy $\kappa$. This implies finally, by lifting in

$$
  \array{
    Q X &\overset{\kappa}{\longrightarrow}& Path(R Q Y)
    \\
    {}^{\mathllap{\in W \cap Cof}}\downarrow 
     && 
    \downarrow^{\mathrlap{\in Fib}}
    \\
    R Q X &\underset{(R (Q f)_1, R (Q f)_2)}{\longrightarrow}&
    R Q Y \times R Q Y
  }
$$

that also $R (Q f)_1$ and $R (Q f)_2$ are right homotopic, hence that indeed $R Q f$ represents a well-defined [[homotopy class]].

Finally to see that the assignment is indeed [[functor|functorial]], observe that the commutativity of the lifting diagrams for $Q f$ and $R Q f$ imply that also the following diagram commutes

$$
  \array{
    X &\overset{p_X}{\longleftarrow}& Q X &\overset{j_{Q X}}{\longrightarrow}& R Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{R Q f}}
    \\
    Y &\underset{p_y}{\longleftarrow}& Q Y &\underset{j_{Q Y}}{\longrightarrow}& R Q Y
  }
  \,.
$$

Now from the [[pasting]] composite 

$$
  \array{
    X &\overset{p_X}{\longleftarrow}& Q X &\overset{j_{Q X}}{\longrightarrow}& R Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{R Q f}}
    \\
    Y &\underset{p_Y}{\longleftarrow}& Q Y &\underset{j_{Q Y}}{\longrightarrow}& R Q Y
    \\
    {}^{\mathllap{g}}\downarrow && \downarrow^{\mathrlap{Q g}} && \downarrow^{\mathrlap{R Q g}}
    \\
    Z &\underset{p_Z}{\longleftarrow}& Q Z &\underset{j_{Q Z}}{\longrightarrow}& R Q Z
  }
$$

one sees that $(R Q g)\circ (R Q f)$ is a lift of $g \circ f$ and hence the same argument as above gives that it is homotopic to the chosen $ R Q(g \circ f)$. 


=--

+-- {: .num_theorem}
###### Theorem

For $\mathcal{C}$ a [[model category]], the functor $\gamma$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory} (for any choice of $R$ and $Q$) exhibits $Ho(\mathcal{C})$ as indeed being the [[homotopy category]] of the underlying [[category with weak equivalences]]: 

For $F \colon \mathcal{C} \longrightarrow D$ any [[functor]] that takes weak equivalences to [[isomorphisms]], it factors through $\gamma$ up to a [[natural isomorphism]]

$$
  \array{
    \mathcal{C} && \overset{F}{\longrightarrow} && D
    \\
    & {}_{\mathllap{\gamma}}\searrow &\Downarrow^{\rho}& \nearrow_{\mathrlap{\tilde F}}
    \\
    && Ho(\mathcal{C})
  }
$$

and this factorization is unique up to unique isomorphism, in that for $(\tilde F_1, \rho_1)$ and $(\tilde F_2, \rho_2)$ two such factorizations, then there is a unique [[natural isomorphism]] $\kappa \colon \tilde F_1 \Rightarrow \tilde F_2$ making the evident diagram of natural isomorphisms commute.

=--

+-- {: .proof}
###### Proof

First, to see that that $\gamma$ indeed takes weak equivalences to isomorphisms: By [[two-out-of-three]] applied to the [[commuting diagrams]] shown in the proof of lemma \ref{ConstructionOfLocalizationFunctorForModelCategoryIsWellDefined} the morphism $R Q f$ is a weak equivalence if $f$ is:

$$
  \array{
    X &\underoverset{\simeq}{p_X}{\longleftarrow}& Q X &\underoverset{\simeq}{j_{Q X}}{\longrightarrow}& R Q X
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{Q f}} && \downarrow^{\mathrlap{R Q f}}
    \\
    Y &\underoverset{p_y}{\simeq}{\longleftarrow}& Q Y &\underoverset{j_{Q Y}}{\simeq}{\longrightarrow}& R Q Y
  }
$$

With this the "Whitehead theorem for model categories", lemma \ref{WhiteheadTheoremInModelCategories}, implies that $R Q f$ represents an isomorphism in $Ho(\mathcal{C})$.

Now let $F \colon \mathcal{C}\longrightarrow D$ be any functor that sends weak equivalences to isomorphisms. We need to show that it factors as

$$
  \array{
    \mathcal{C} && \overset{F}{\longrightarrow} && D
    \\
    & {}_{\mathllap{\gamma}}\searrow &\Downarrow^{\rho}& \nearrow_{\mathrlap{\tilde F}}
    \\
    && Ho(\mathcal{C})
  }
$$

uniquely up to unique [[natural isomorphism]]. Now by construction of $R$ and $Q$ in def. \ref{FibrantCofibrantReplacementFunctorToHomotopyCategory}, $\gamma_{R,Q}$ is the identity on the [[full subcategory]] of fibrant-cofibrant objects. It follows that if $\tilde F$ exists at all, it must satisfy for all $X \stackrel{f}{\to} Y$ with $X$ and $Y$ both fibrant and cofibrant that 

$$
  \tilde F([f]) \simeq F(f)
  \,.
$$ 

But by def. \ref{HomotopyCategoryOfAModelCategory} that already fixes $\tilde F$ on all of $Ho(\mathcal{C})$, up to unique [[natural isomorphism]]. Hence it only remains to check that with this definition of $\tilde F$ there exists any [[natural isomorphism]] $\rho$ filling the diagram above. 

To that end, apply $F$ to the above [[commuting diagram]] to obtain

$$
  \array{
    F(X) &\underoverset{iso}{F(p_X)}{\longleftarrow}& F(Q X) &\underoverset{iso}{F(j_{Q X})}{\longrightarrow}& F(R Q X)
    \\
    {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{F(Q f)}} && \downarrow^{\mathrlap{F(R Q f)}}
    \\
    F(Y) &\underoverset{F(p_y)}{iso}{\longleftarrow}& F(Q Y) &\underoverset{F(j_{Q Y})}{iso}{\longrightarrow}& F(R Q Y)
  }
  \,.
$$

Here now all horizontal morphisms are [[isomorphisms]], by assumption on $F$. It follows that defining $\rho_X \coloneqq F(j_{Q X}) \circ F(p_X)^{-1}$ makes the required natural isomorphism:

$$
  \array{
    \rho_X \colon & F(X) &\underoverset{iso}{F(p_X)^{-1}}{\longrightarrow}& F(Q X) &\underoverset{iso}{F(j_{Q X})}{\longrightarrow}& F(R Q X)
   &=&
   \tilde F(\gamma_{R,Q}(X))
    \\
    & {}^{\mathllap{F(f)}}\downarrow 
     && 
     && \downarrow^{\mathrlap{F(R Q f)}}
     && \downarrow^{\tilde F(\gamma_{R,Q}(X))}
    \\
    \rho_Y\colon& F(Y) &\underoverset{F(p_y)^{-1}}{iso}{\longrightarrow}& F(Q Y) &\underoverset{F(j_{Q Y})}{iso}{\longrightarrow}& F(R Q Y)
   &=&
   \tilde F(\gamma_{R,Q}(X))
  }
  \,.
$$


=--


## References

The original account is due to

* {#Quillen67} [[Daniel Quillen]], _Axiomatic homotopy theory_ in  _Homotopical algebra_, Lecture Notes in Mathematics, No. 43 43, Berlin (1967)

More recent review includes

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], section II.1 of _[[Simplicial homotopy theory]]_ Birkh&#228;user 1996, 1999 


[[!redirects homotopy categories of model categories]]

