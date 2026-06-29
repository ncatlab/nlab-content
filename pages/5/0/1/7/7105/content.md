
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


\tableofcontents


## Ideas

By _Mayer-Vietoris sequences_ one refers to those [[homotopy fiber sequences]] -- or typically to just their corresponding [[long exact sequences of homotopy groups]] -- which are induced from [[(∞,1)-pullbacks]]/[[homotopy pullbacks]].

## Definition

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[finite (∞,1)-limits]] and let $X, Y, B$ be [[pointed objects]] and

$$
  f \colon X \longrightarrow B
$$

and

$$
  g \colon Y \longrightarrow B
$$

be any two [[morphisms]] with common [[codomain]] preserving the base points. Let $X \times_B Y$ be the [[(∞,1)-pullback]]

$$

  \array{
    X \times_B Y 
      & \overset{v}{\longrightarrow} & 
    Y
    \\
    \mathllap{^{_{u}}}\big\downarrow 
      &\swArrow_\simeq& 
    \big\downarrow^{\mathrlap{g}}
    \\
    X &\underset{f}{\longrightarrow}& B
  }
  \,.
$$

The corresponding **Mayer-Vietoris sequence** is the [[homotopy fiber sequence]] of the induced morphism $X \times_B Y \longrightarrow X \times Y$. Often the term is used (only) for the corresponding [[long exact sequence of homotopy groups]].

## Properties

### General
 {#GeneralProperties}

+-- {: .num_prop #SequenceFromDiagonal}
###### Proposition

Let $\mathcal{C}$ be a [[presentable (∞,1)-category]]. 

Then $X \times_B Y$, which by definition sits in

$$
  \array{
    X \times_B Y &\longrightarrow& Y
    \\
    \big\downarrow 
      &\swArrow_{\simeq}& 
    \big\downarrow^{\mathrlap{g}}
    \\
    X  &\underset{f}{\longrightarrow}& B
    \mathrlap{\,,}
  }
$$ 

is equivalently also the following [[(∞,1)-pullback]] 

$$
  \array{
    X \times_B Y &\longrightarrow& B
    \\
    \big\downarrow 
      &\swArrow_{\simeq}& 
    \big\downarrow{\mathrlap{{}^{_{\Delta_B}}}}
    \\
    X \times Y 
      &\underset{(f,g)}{\longrightarrow}& 
    B \times B
  }
  \,,
$$

where the right vertical morphism is the [[diagonal]].

Moreover, the [[homotopy fiber]] of $X \times_B Y \to X \times Y$ is the [[loop space object]] $\Omega B$.

=--
 
See also at _[[homotopy pullback]]_ [this corollary](homotopy+pullback#HomotopyPullbackByFactorizationLemma).

+-- {: .proof}
###### Proof

The first statement may be checked by choosing a presentation by a [[combinatorial model category]] and then proceeding as below in the discussion _[Presentation by fibrant objects](#PresentationByFibrantObjects)_.
Then by the [[pasting law for pullbacks|pasting law]] for [[(infinity,1)-pullbacks|$(\infty,1)$-pullbacks]] it follows that with the left square in 

$$
  \array{
    \Omega B 
      &\longrightarrow& 
    X \times_B Y 
      &\longrightarrow& 
    B
    \\
    \big\downarrow 
      &\swArrow_{\simeq}& 
    \big\downarrow 
      &\swArrow_{\simeq}& 
    \big\downarrow
    \\
    \ast 
      &\longrightarrow& 
    X \times Y 
      &\underset{(f,g)}{\longrightarrow}& 
    B \times B
  }
$$

being an $(\infty,1)$-pullback, so is the total outer rectangle. But again by the first statement, this is equivalent to the $(\infty,1)$-pullback

$$
  \array{
    \Omega B &\longrightarrow& \ast 
    \\
    \big\downarrow 
      &\swArrow_{\simeq}& 
    \big\downarrow
    \\
    \ast 
      &\longrightarrow& 
    B
  }
  \,,
$$

which is the defining pullback for the [[loop space object]].

=--

Therefore the Mayer-Vietoris [[homotopy fiber sequence]] is of the form

$$
  \Omega B 
    \longrightarrow 
  X \times_B Y 
    \longrightarrow 
  X \times Y
  \,.
$$

For $\mathcal{C} = $ [[∞Grpd]] $\simeq L_{whe}$ [[Top]], this point of view is amplified by [Dyer & Roitberg 1980](#DyerRoitberg80).


+-- {: .num_cor #LongExactSequenceOfHomotopyGroups}
###### Corollary

The corresponding [[long exact sequence of homotopy groups]] is of the form

\[
  \label{TheHomotopicalMVSequence}
  \begin{array}{c}
  \cdots 
    \longrightarrow 
  \pi_{n+1} B 
    \longrightarrow 
  \pi_n (X \times_B Y) 
    \overset{(f_*, g_*)}{\longrightarrow} 
  \pi_n X \oplus \pi_n Y 
    \overset{f_* - g_*}{\longrightarrow} 
  \pi_n B 
    \longrightarrow 
  \cdots 
  \\
  \cdots 
    \longrightarrow
  \pi_2 B 
    \longrightarrow 
  \pi_1 (X \times_B Y) 
    \overset{(f_*, g_*)}{\longrightarrow}  
  \pi_1 X \times \pi_1 Y 
    \overset{f_* \cdot g_*^{-1}}{\longrightarrow} 
  \pi_1 B 
    \longrightarrow 
  \pi_0 (X \times_B Y) 
    \longrightarrow 
  \pi_0(X) \times \pi_0(Y)
  \,.
  \end{array}
\]

=--

This is what has historically been the definition of Mayer-Vietoris sequences (cf. [Eckmann & Hilton 1964](#EckmannHilton)).

### Presentation by fibrant objects
 {#PresentationByFibrantObjects}

Suppose that the [[(∞,1)-category]] $\mathcal{C}$ is [[simplicial localization|presented]] by a [[category of fibrant objects]] $C$ (for instance the [[subcategory]] on the fibrant objects of a [[model category]]). 

Then the $(\infty,1)$-pullback $X \times_B Y$ is presented by a [[homotopy pullback]], and by the [[factorization lemma]], this is given by the ordinary [[limit]]

$$
  \array{
    X \times^h_B Y &\to& &\to& Y
    \\
    \downarrow && && \downarrow^{\mathrlap{g}}
    \\
    && B^I &\to& B 
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{f}{\to}& B
  }
  \,,
$$

where $B \stackrel{\simeq}{\to} B^I \to B \times B$ is a [[path object]] for $B$. This limit coincides, up to [[isomorphism]], with the [[pullback]]

$$
  \array{
    X \times_B^h Y &\to& B^I
    \\
    \downarrow && \downarrow
    \\
    X \times Y &\stackrel{(f,g)}{\to}& B \times B
  }
  \,.
$$

This implies in particular that the [[homotopy fiber]] of $X \times_B^h Y \to X \times Y$ is the [[loop space object]] $\Omega B$, being the [[fiber]] of the [[path space object]] projection.

{#ExtendingMVToTheRight}
With this, we may usefully extend the tail end of the MV sequence by one further step:

\begin{lemma}
  The [[image]] of the tail end map in (eq:TheHomotopicalMVSequence)
  $$
    \begin{array}{ccc}
      \pi_0\big(X \times_B Y\big) 
      &
       \overset
         { \big( \pi_0(u), \pi_0(v) \big) }
         {\longrightarrow}
      &
      \pi_0(X) \times \pi_0(Y)
      \\
      \big[ (x,y,\gamma) \big] 
      &\mapsto&
      \big( [x],[y] \big)
    \end{array}
  $$
  is the [[fiber product]] of [[connected components]]:
  \[
    im\big( \pi_0(u), \pi_0(v) \big)
    \simeq
    \pi_0(X) \times_{\pi_0(B)} \pi_0(Y)
    \mathrlap{\,.}
  \]
\end{lemma}
\begin{proof}
  As indicated, here we think of the homotopy fiber product $X \times_B Y$ as presented, via the [factorization lemma](Introduction+to+Homotopy+Theory#FactorizationLemma), as the space of triples consisting of a point $x \in X$, a point $y \in Y$ and a path $\gamma$ in $B$ from $f(x)$ to $g(y)$. 
This makes it manifest that the image consists of exactly those pairs $([x],[y])$ for which there exists a path in $B$ from $f(x)$ to $f(y)$, hence for which $f(x)$ and $f(y)$ are in the same connected component of $B$.
\end{proof}

\begin{corollary}
\label{HomotopicalMVSequencesExtendedOneStepToTheRight}
  The tail end of the homotopical MV sequence (eq:TheHomotopicalMVSequence) may be adjusted to extend one step further to the right, to a [[long exact sequence]] as follows:
\[
  \cdots 
    \longrightarrow
  \pi_2 B 
    \longrightarrow 
  \pi_1 (X \times_B Y) 
    \overset{(f_*, g_*)}{\longrightarrow}  
  \pi_1 X \times \pi_1 Y 
    \overset{f_* \cdot g_*^{-1}}{\longrightarrow} 
  \pi_1 B 
    \longrightarrow 
  \pi_0 (X \times_B Y) 
    \longrightarrow 
  \pi_0 (X) \times_{\pi_0(B)} \pi_0(Y)
    \longrightarrow
  \ast
  \mathrlap{\,.}
\]
\end{corollary}



### Over an $\infty$-group
 {#OverAGroupObject}

We consider now the case where $B$ carries the structure of an  [[∞-group]] (or just a grouplike [[H-space]] object) in a [[presentable (∞,1)-category]] or [[locally Cartesian closed (∞,1)-category]] $\mathcal{C}$.

In this case (as discussed in a moment), we have an [[(∞,1)-pullback]] of the form

$$
  \array{
    B &\longrightarrow& \ast
    \\
    \big\downarrow{\mathrlap{^{_{\Delta_B}}}} 
      &\swArrow_{\simeq}& 
    \big\downarrow{\mathrlap{^{_e}}}
    \\
    B \times B
      &
       \underset{
         (-)\cdot (-)^{-1}
       }{\longrightarrow}
      &
    B
    \mathrlap{\,,}
  }
$$

where the bottom horizontal morphism is the composite

$$
  (-)\cdot (-)^{-1} 
    \;\colon\; 
  B \times B 
    \overset{\big(id, (-)^{-1}\big)}{\longrightarrow} 
  B \times B 
    \overset{(-)\cdot(-)}{\longrightarrow} 
  B
$$

of inverting the second argument (via the group law) followed by the [[binary operation|group operation]].

It then follows by the [[pasting law]] and prop. \ref{SequenceFromDiagonal} that in this case the morphism $X \times_B Y \to X \times Y$ in the Mayer-Vietoris sequence is itself the homotopy fiber of $X \times Y \stackrel{f \cdot g^{-1}}{\longrightarrow} B$, hence that we have a long homotopy fiber sequence of the form

$$
  \Omega B \longrightarrow X \times_B Y \longrightarrow X \times Y
  \stackrel{f \cdot g^{-1}}{\longrightarrow} B
  \,.
$$

First consider two more concrete special cases.

+-- {: .num_example}
###### Example

Let $S$ be a small [[site]] and let $\mathcal{C} = Sh_{(\infty,1)}(S)$ be the [[(∞,1)-category of (∞,1)-sheaves]] on $S$.

This is [[presentable (∞,1)-category|presented]] by the projective [[model structure on simplicial presheaves]]

$$
  \mathcal{C} \simeq ([S^{op}, sSet]_{proj, loc})^\circ
  \,.
$$

As discussed there, the [[Dold-Kan correspondence]] prolongs to a [[Quillen adjunction]] on [[presheaves]] whose [[right adjoint]] is


$$
  \Xi : 
  [S^{op}, Ch_{\bullet \leq 0}(Ab)]_{proj}
  \to 
  [S^{op}, sAb]_{proj}
  \to
  [S^{op}, sSet]_{proj}
  \,.
$$

Let then $B \in \mathcal{C}$ be an object with a presentation in $[S^{op}, sSet]$ in the image of this $\Xi$. We write $B$ also for this presentation, and hence $B = \Xi(\tilde B)$ for some presheaf of chain complexes $\tilde B$. 

We claim now that such $B$ satisfies the above assumption.

To see this, first notice that the evident morphism $- : \tilde B \times \tilde B \to \tilde B$ is degreewise an [[epimorphism]], hence it is a fibration in $[S^{op}, Ch_{\bullet \geq 0}(Ab)]_{proj}$, and since $\Xi$ is [[Quillen adjunction|right Quillen]], so is the corresponding morphism $- : B \times B \to B$ in $[S^{op}, sSet]_{proj}$. 

Therefore the ordinary pullback of presheaves of chain complexes

$$
  \array{
    \tilde B &\to& *
    \\
    \downarrow^{\mathrlap{\Delta_{\tilde B}}} && \downarrow^{\mathrlap{0}}
    \\
    \tilde B \times \tilde B &\stackrel{-}{\to}& \tilde B
  }
$$

is a [[homotopy pullback]] in $[S^{op}, Ch_{\bullet \geq 0}(Ab)]_{proj}$, as is the ordinary pullback of simplicial presheaves

$$
  \array{
    B &\to& *
    \\
    \downarrow^{\mathrlap{\Delta_B}} && \downarrow^{\mathrlap{0}}
    \\
    B \times B &\stackrel{-}{\to}& B
  }
$$

in $[S^{op}, sSet]_{proj}$.

Since [[∞-stackification]] preserves [[finite (∞,1)-limits]], this presents an [[(∞,1)-pullback]] also in $\mathcal{C}$.

=--


+-- {: .num_example #SimplicialGroupObjectAsBase}
###### Example

Let $\mathcal{C}$ be an [[(∞,1)-topos]] with a 1-[[site]] $S$ of definition (a [[n-localic (∞,1)-topos|1-localic (∞,1)-topos]]).

Then (as discussed there) every [[∞-group]] object in $\mathcal{C}$
has a presentation by a presheaf of [[simplicial groups]]

$$
  B \in [S^{op}, sGrp]_{proj} \to [S^{op}, sSet]_{proj}
  \,.
$$

We claim that the canonical morphism $- : B \times B \to B$ is
objectwise a [[Kan fibration]] and hence a fibration in the 
projective [[model structure on simplicial presheaves]].

Let $U \in S$ be any test object. A diagram


$$
  \array{ 
    \Lambda[k]^i &\stackrel{(ha, hb)}{\to}& B(U) \times B(U)
    \\
    \downarrow^{\mathrlap{j}} && \downarrow
    \\
    \Delta[k] &\stackrel{\sigma}{\to}& B(U)
  }
$$

corresponds to a $k$-cell $\sigma \in B(U)$ together with a 
choice of decomposition of the $i$th [[horn]] $j^* \sigma$
as a difference

$$
  (j^* \sigma)_l = ha_l \cdot hb_l^{-1}
  \,.
$$

Since $B(U)$ itself is a [[Kan complex]] (being a [[simplicial group]], as discussed there) there is a filler $b \colon \Delta[k] \to B(U)$ 
of the [[horn]] $hb \colon \Lambda[k]^i \to B(U)$.
Define then 

$$
  a \coloneqq \sigma \cdot b
  \,.
$$

Since all the face maps are group homomorphisms, this is indeed a filler of $ha$:

$$
  \begin{aligned}
    \delta_l(a) 
      & = \delta_l(\sigma \cdot b)
    \\
      & = \delta_l(\sigma) \cdot \delta_l(b)
    \\   
      & = \delta_l(\sigma) \cdot hb_l
    \\
      & = ha_l
  \end{aligned}
  \,.
$$

Moreover, by construction, $(a,b)$ is a filler in 

$$
  \array{ 
    \Lambda[k]^i &\stackrel{(ha, hb)}{\to}& B(U) \times B(U)
    \\
    \downarrow^{\mathrlap{i}} 
    &{}^{(a,b)}\nearrow& 
    \downarrow
    \\
    \Delta[k] &\stackrel{\sigma}{\to}& B(U)
  }
  \,.
$$

Since therefore $- \colon B \times B \to B$ is a projective fibration, it follows
as before that the ordinary pullback

$$
  \array{
    B &\to& *
    \\
    \downarrow^{\mathrlap{\Delta_B}} && \downarrow^{e}
    \\
    B \times B &\stackrel{-}{\to}& B
  }
$$

is a [[homotopy pullback]].

=--


+-- {: .num_prop #SequenceOverGroupObjectIn1LocalicSituation}
###### Proposition

For $B$ an [[∞-group]] object as above, the [[(∞,1)-pullback]] $X \times_B Y$ is equivalently given by the $(\infty,1)$-pullback

$$
  \array{
   X \times_B Y &\to& * 
   \\
   \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{0}}
   \\ 
   X \times Y &\stackrel{f \cdot g^{-1}}{\to}& B
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

By prop. \ref{SequenceFromDiagonal} the object $X \times_B Y$ is the $(\infty,1)$-pullback in

$$
  \array{
    X \times_B Y &\to& B
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\Delta_B}}
    \\
    X \times Y &\stackrel{(f,g)}{\to}& B \times B
  }
  \,.
$$

By the [[pasting law]] this is equivalently given by the  composite pullback of 

$$
  \array{
    X \times_B Y &\to& B &\to& *
    \\
    \downarrow 
    &\swArrow_{\simeq}& 
    \downarrow^{\mathrlap{\Delta_B}}
    &\swArrow_{\simeq}& 
    \downarrow^{\mathrlap{0}}
    \\
    X \times Y &\stackrel{(f,g)}{\to}& B \times B
    &\stackrel{-}{\to}& B
  }
  \,.
$$

Here the composite bottom morphism is $(f - g)$.

=--

Summing this up:

+-- {: .num_prop}
###### Proposition

For $\mathbf{H}$ an [[(∞,1)-sheaf]] [[(∞,1)-topos]], $B$ an [[∞-group]]-object in $\mathbf{H}$ and $f\colon X \to B$ and $g \colon Y\to B$ two morphisms, then there is a long [[homotopy fiber sequence]] of the form

$$
  \Omega B \longrightarrow X \times_B Y \longrightarrow X \times Y
  \stackrel{f \cdot g^{-1}}{\longrightarrow} B
  \,.
$$

=--

+-- {: .proof}
###### Proof

For $\mathcal{C}$ an [[(∞,1)-site]] of definition, there is a [[reflective sub-(infinity,1)-category|reflection]]

$$
  \mathbf{H} \stackrel{\longleftarrow}{\hookrightarrow}
  [C^{op},\infty Grpd]
$$

of $\mathbf{H}$ into an [[(∞,1)-category of (∞,1)-presheaves]].

By prop. \ref{SequenceOverGroupObjectIn1LocalicSituation} the statement
holds in $[C^{op},\infty Grpd]$. Since embedding and reflection both preserve
[[finite (∞,1)-limits]], it hence also holds in $\mathbf{H}$.

=--

Still more generally and more simply:

+-- {: .num_prop #HTTArgumentForPullback}
###### Proposition

Let $\mathcal{C}$ be a [[locally Cartesian closed (∞,1)-category]].
Let $G$ be an [[∞-group]] object (or just a grouplike [[H-space]]-object). Then for
$\phi \colon D \longrightarrow G$ any morphism we have a [[homotopy pullback]] square of the form

$$
  \array{
     G \times D &\longrightarrow& D
     \\
     \downarrow && \downarrow^{\mathrlap{\phi}}
     \\
     G \times G &\stackrel{(-)\cdot (-)^{-1}}{\longrightarrow}& G
  }
  \,.
$$

=--

([nForum discussion](http://nforum.mathforge.org/discussion/6403/generality-of-mayervietoris-in-an-infinitytopos-/?Focus=51417#Comment_51417))

+-- {: .proof #ProofOfHTTArgumentForPullback}
###### Proof

By [this discussion](locally+cartesian+closed+infinity,1-category#InternalLogic) we may use [[homotopy type theory]] reasoning. Starting out with the discussion at _[homotopy pullback -- In homotopy type theory](homotopy+pullback#InHomotopyTypeTheory)_ we obtain

$$ 
\begin{aligned}
  D\times_G  (G\times G)
  &= \sum_{d:D} \sum_{g_1:G} \sum_{g_2:G} (g_1\cdot g_2^{-1} = \phi(d)) \\
  &= \sum_{d:D} \sum_{g_1:G} \sum_{g_2:G} (g_1 = \phi(d)\cdot g_2) \\
  &= \sum_{d:D} \sum_{g_2:G} \sum_{g_1:G} (g_1 = \phi(d)\cdot g_2) \\
  &= \sum_{d:D} \sum_{g_2:G} \mathbf{1}\\
  &= D\times G
\end{aligned}
  \,,
$$

where the second but last step consists of observing a contractible based [[path space object]] (see the discussion at [[factorization lemma]]).

=--

+-- {: .num_prop }
###### Corollary

Let $\mathcal{C}$ be a [[locally Cartesian closed (∞,1)-category]].
Let $G$ be an [[∞-group]] object (or just a grouplike [[H-space]]-object). 

Then for $f \colon X \to G$ and $g \colon Y \to G$ two morphisms, there is a Mayer-Vietoris-type [[homotopy fiber sequence]] 

$$
  \cdots \to \Omega G
  \longrightarrow 
  X \times_G Y
  \longrightarrow
  X \times Y
  \stackrel{f \cdot (g^{-1})}{\longrightarrow}
  G
  \,.
$$

=--

+-- {: .proof}
###### Proof

Use prop. \ref{HTTArgumentForPullback} with $\phi$ being the canonical point, i.e. the inclusion $e \colon \ast \to G$ of [[generalized the|the]] neutral element to find the homotopy pullback

$$
  \array{
     G  &\longrightarrow& \ast
     \\
     \big\downarrow{\mathrlap{^{_\Delta}}} 
      && \downarrow{\mathrlap{^{_e}}}
     \\
     G \times G 
      &\underset{(-)\cdot (-)^{-1}}{\longrightarrow}& 
     G
     \mathrlap{\,.}
  }
$$

Then use the [[pasting law]] as above.

=--

## Examples

### (Co)Homology of a cover 
 {#CohomologyOfACover}

A special case of the general Mayer-Vietoris sequence, corollary \ref{LongExactSequenceOfHomotopyGroups} -- which historically was the first case considered -- applies to the [[cohomology]]/[[homology]] of a [[topological space]] $X$ equipped with an [[open cover]] $\{U, V\}$.

Being a [[cover]] means (see [[effective epimorphism in an (∞,1)-category]]) that there is a [[homotopy pushout]] [[diagram]] of the form

$$
  \array{
    U \cap V &\hookrightarrow& U
    \\
    \downarrow && \downarrow
    \\
    V &\to& X
  }
$$

in the [[(∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]]/[[Top]].
 
When this is [[presentable (∞,1)-category|presented]] by the standard [[model structure on simplicial sets]] or in terms of [[CW-complex]]es by the [[model structure on topological spaces]], it is given by an ordinary [[pushout]]. 

Let then $A \in \infty Grpd \simeq Top$ be some coefficient object, for instance an [[Eilenberg-MacLane object]] $\mathbf{B}^n G$ ([[Eilenberg-MacLane space]] $\cdots \simeq K(G,n)$) for the definition of ordinary [[singular cohomology]] with coefficients in an [[abelian group]] $G$.

Then applying the [[derived hom space]] functor $\mathbf{H}(-, A) : \mathbf{H}^{op} \to \infty Grpd$ yields the [[(∞,1)-pullback]] [[diagram]]

$$
  \array{
    \mathbf{H}(X, A) &\to& \mathbf{H}(U,A)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(V,A) &\to& \mathbf{H}(U \cap V, A)
  }
$$

to which we can apply the homotopical Mayer-Vietoris sequence. 

Notice that (as discussed in detail at [[cohomology]]) the [[homotopy groups]] of the [[∞-groupoid]] $\mathbf{H}(X,\mathbf{B}^n G)$ are the [[cohomology groups]] of $X$ with coefficients in $G$

$$
  \pi_k \mathbf{H}(X, \mathbf{B}^n G)
  \simeq
  H^{n-k}(X, G)
  \,.
$$

By the above [general properties](GeneralProperties) the above homotopy pullback is equivalent to 

$$
  \mathbf{H}(X,A) \to \mathbf{H}(U,A) \times \mathbf{H}(V,A)
  \to \mathbf{H}(U \cap V, A) 
$$

being a [[fiber sequence]]. The corresponding long exact sequence in cohomology (as discussed above) is what is traditionally called the Mayer-Vietoris sequence of the cover of $X$ by $U$ and $V$ in $A$-cohomology.

By duality (see [[universal coefficient theorem]]) an analogous statement holds for the [[homology]] of $X$, $U$ and $V$.

## Related concepts

* [[diamond principle]]

* [[Brown-Gersten property]]


## References

Mayer-Vietoris sequences are named after:

* Walther Mayer: *Über abstrakte Topologie*, Monatshefte f&uuml; Mathematik und Physik **36** (1929) 1–42 \[<a href="https://doi.org/10.1007/BF02307601">doi:10.1007/BF02307601</a>\]

* [[Leopold Vietoris]]: *Über die Homologiegruppen der Vereinigung zweier Komplexe*, Monatshefte f. Mathematik und Physik **37** (1930)  159–162 \[<a href="https://doi.org/10.1007/BF01696765">doi:10.1007/BF01696765</a>\]

but the formulation as [[exact sequences]] appeared only later:

* [[Samuel Eilenberg]], [[Norman Steenrod]]; §15 in: _Foundations of Algebraic Topology_, Princeton University Press (1952) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/eilestee.pdf), [ISBN:9780691653297](https://press.princeton.edu/books/hardcover/9780691653297/foundations-of-algebraic-topology)&rbrack;

* {#EckmannHilton} [[Beno Eckmann]], [[Peter Hilton]]; §5 in: *Unions and intersections in homotopy theory*, Comment. Math. Helv. **3** 2 (1964) 93-307 &lbrack;[doi:10.1007/BF02566918](http://dx.doi.org/10.1007/BF02566918)&rbrack;


A more modern review that emphasizes the role of [[homotopy fiber sequences]]:

* {#DyerRoitberg80} [[Eldon Dyer]], [[Joseph Roitberg]]: *Note on Sequences of Mayer-Vietoris Type*, Proceedings of the AMS **80** 4 (1980) &lbrack;[doi:10.2307/2043446](https://doi.org/10.2307/2043446), [jstor:2043446](https://www.jstor.org/stable/2043446),  [pdf](http://www.ams.org/journals/proc/1980-080-04/S0002-9939-1980-0587950-8/S0002-9939-1980-0587950-8.pdf)&rbrack;

See also:

* Wikipedia: *[Mayer-Vietoris sequence](https://en.wikipedia.org/wiki/Mayer%E2%80%93Vietoris_sequence)*

Discussion in [[algebraic K-theory]]:

* [[Jean-Pierre Jouanolou]]: _Une suite exacte de Mayer-Vietoris en K-théorie algébrique_, in: *Higher K-Theories*, Lecture Notes in Mathematics __341__, Springer (1973) 293--316 &lbrack;[doi:10.1007/BFb0067063](https://doi.org/10.1007/BFb0067063)&rbrack;

Discussion in the context of [[stable model categories]]:

* [[Peter May]]; lemma 5.7 in: _The additivity of traces in triangulated categories_, Adv. Math. **163** 1 (2001) 34-73 &lbrack;[pdf](http://www.math.uchicago.edu/~may/PAPERS/AddJan01.pdf)&rbrack;



Discussion in the context of [[homotopy type theory]]:

* [[Evan Cavallo]] et al.: _Exactness of the Mayer-Vietoris Sequence in Homotopy Type Theory_ &lbrack;[pdf](https://staff.math.su.se/evan.cavallo/works/mayer-vietoris.pdf), [[Cavally-MayerVietoris.pdf:file]]&rbrack;

[[!redirects Mayer-Vietoris sequences]]
[[!redirects Mayer-Vietoris long exact sequence]]