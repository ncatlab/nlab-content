
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

> This is a sub-section of the entry _[[cohesive (∞,1)-topos]]_ . See there for background and context

***

#Contents#
* table of contents
{:toc}


## Structures in a cohesive $(\infty,1)$-topos

This continues the list of structures whose first part is at _[[cohesive (infinity,1)-topos -- structures]]_ .

### Concordance 
  {#Concordance}

Since $\mathbf{H}$ is an [[(∞,1)-topos]] it carries canonically
the structure of a [[cartesian closed (∞,1)-category]]. For  
$X, Y \in \mathbf{H}$, write $Y^X \in \mathbf{H}$ for the corresponding
[[internal hom]].

Since $\Pi : \mathbf{H} \to $ [[∞Grpd]] preserves products, we have 
for all $X,Y, Z \in \mathbf{H}$ canonically induced a morphism

$$
  \Pi(Y^X) \times \Pi(Z^Y)
   \stackrel{\simeq}{\to}
  \Pi(Y^X \times Z^Y)
  \stackrel{\Pi(comp_{X,Y,Z})}{\to}
  \Pi(Z^X)
  \,.
$$

This should yield an [[(∞,1)-category]] $\tilde \mathbf{H}$
with the same objects as $\mathbf{H}$ and hom-$\infty$-groupoids defined by

$$
  \tilde \mathbf{H}(X,Y) := \Pi(Y^X)
  \,.
$$

We have that

$$
  \tilde \mathbf{H}(X,\mathbf{B}G) = \Pi(\mathbf{B}G^X) 
$$

is the $\infty$-groupoid whose objects are $G$-[[principal ∞-bundle]]s on $X$ and whose morphisms have the interpretaton of $G$-principal bundles on the cylinder $X \times I$. These are _[[concordance]]s of $\infty$-bundles._



### Geometric homotopy and Galois theory {#Homotopy}

We discuss canonical internal realizations of the notions of [[homotopy group]], [[local system]] and [[Galois theory]] in $\mathbf{H}$.


+-- {: .num_defn}
###### Definition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]] and $X \in \mathbf{H}$ an [[object]], we call $\Pi X \in $ [[∞Grpd]] the 
**[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]** of $X$. 

The ([[categorical homotopy groups in an (∞,1)-topos|categorical]]) [[homotopy group]]s of $\Pi(X)$ we call the [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of $X$

$$
  \pi_\bullet^{geom}(X) := \pi_\bullet(\Pi (X))
  \,.
$$

=--

+-- {: .num_defn #GeometricRealization}
###### Definition


For $\vert - \vert : $ [[∞Grpd]] $\stackrel{\simeq}{\to}$ [[Top]] the [[homotopy hypothesis]]-[[equivalence of (∞,1)-categories|equivalence]] we write

$$
  \vert X \vert := \vert \Pi X \vert \in Top
$$

and call this the **topological [[geometric realization]]** of $X$, or just the _geometric realization_ for short.

=--

+-- {: .num_note #GeometricRealizationInTheLiterature}
###### Note

In presentations of $\mathbf{H}$ by a [[model structure on simplicial presheaves]] as in prop. \ref{SimplicialPresheavesOverInfinityCohesviveSite} this abstract notion reproduces the notion of geometric realization of [[∞-stack]]s in ([Simpson](#Simpson)). See remark 2.22 in ([SimpsonTeleman](#SimpsonTeleman)).

=--

+-- {: .un_def}
###### Definition

We say a **geometric [[homotopy]]** between two morphism $f,g : X \to Y$
in $\mathbf{H}$ is a diagram

$$
  \array{
    X 
    \\
    \downarrow^{\mathrlap{(Id,i)}} & \searrow^{\mathrlap{f}}
    \\
    X \times I &\stackrel{\eta}{\to}& Y
    \\
    \uparrow^{\mathrlap{(Id,o)}} & \nearrow_{\mathrlap{g}}
    \\
    X
  }
$$

such that $I$ is geometrically connected, $\pi_0^{geom}(I) = *$.

=--

+-- {: .un_prop}
###### Proposition

If $f,g : X\to Y$ are geometrically homotopic in $\mathbf{H}$, then their images $\Pi(f), \Pi(g)$ are 
equivalent in $\infty Grpd$.

=--

+-- {: .proof}
###### Proof

By the condition that $\Pi$ preserves products
in a cohesive $(\infty,1)$-topos we have that the image of the
geometric homotopy in $\infty Grpd$ is a diagram of the form

$$
  \array{
    \Pi(X) 
    \\
    \downarrow^{\mathrlap{(Id,\Pi(i))}} & \searrow^{\mathrlap{\Pi(f)}}
    \\
    \Pi(X) \times \Pi(I) &\stackrel{\Pi(\eta)}{\to}& \Pi(Y)
    \\
    \uparrow^{\mathrlap{(Id,\Pi(o))}} & \nearrow_{\mathrlap{\Pi(g)}}
    \\
    \Pi(X)
  }
  \,.
$$

Now since $\Pi(I)$ is connected by assumption, there is a diagram

$$
  \array{
     && *
     \\
     & {}^{\mathllap{Id}}\nearrow & \downarrow^{\mathrlap{\Pi(i)}}
     \\
     * &\to& \Pi(I)
     \\
     & {}_{\mathllap{Id}}\searrow & \uparrow^{\mathrlap{\Pi(o)}}
     \\
     && *
  }
$$

in [[∞Grpd]].

Taking the product of this diagram with $\Pi(X)$ and pasting the result
to the above image $\Pi(\eta)$ of the geometric homotopy constructs
the equivalence $\Pi(f) \Rightarrow \Pi(g)$ in $\infty Grpd$.

=--

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]], also all its objects $X \in \mathbf{H}$ are locally $\infty$-connected, in the sense  their [[petit topos|petit]] [[over-(∞,1)-toposes]] $\mathbf{H}/X$ are locally $\infty$-connected.

The two notions of fundamental $\infty$-groupoids of $X$ induced this way do agree, in that there is a natural equivalence

$$
  \Pi_X(X \in \mathbf{H}/X) \simeq \Pi(X \in \mathbf{H})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the general facts recalled at [[étale geometric morphism]] we have a composite [[essential geometric morphism]]

$$
  (\Pi_X \dashv \Delta_X \dashv \Gamma_X) : 
  \mathbf{H}_{/X}
   \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{\X_*}{\to}}}
  \mathbf{H}
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}}}  
   \infty Grpd
$$

and $X_!$ is given by sending $(Y \to X) \in \mathbf{H}/X$ to $Y \in \mathbf{H}$.

=--


+-- {: .un_def}
###### Definition

For $\kappa$ a [[regular cardinal]] write 

$$
  Core \infty Grpd_\kappa \in \infty Grpd
$$ 

for the [[∞-groupoid]] of $\kappa$-[[small (∞,1)-category|small ∞-groupoid]]s: the [[core]] of the full [[sub-(∞,1)-category]] of [[∞Grpd]] on the $\kappa$-small ones.

=--

+-- {: .un_remark}
###### Remark

We have 

$$
  Core \infty Grpd_\kappa \simeq
  \coprod_i \mathbf{B} Aut(F_i)
  \,,
$$

where the coproduct ranges over all $\kappa$-small [[homotopy type]]s $[F_i]$ and $Aut(F_i)$ is the [[automorphism ∞-group]] of any representative $F_i$ of $[F_i]$.

=--

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ write

$$
  LConst(X) := \mathbf{H}(X, Disc Core \infty Grpd_\kappa)
  \,.
$$

We call this the $\infty$-groupoid of **[[locally constant ∞-stack]]s** on $X$.

=--

+-- {: .un_observation}
###### Observation

Since $Disc$ is [[left adjoint]] and [[right adjoint]] it commutes with [[coproduct]]s and with [[delooping]] and therefore

$$
  Disc Core \infty Grpd_\kappa 
    \simeq 
  \coprod_i \mathbf{B} Disc Aut(F_i)
  \,.
$$

Therefore a cocycle $P \in LConst(X)$ may be identified on each geometric connected component of $X$ as a  $Disc Aut(F_i)$-[[principal ∞-bundle]] $P \to X$ over $X$ for the [[∞-group]] object  $Disc Aut(F_i) \in \mathbf{H}$. We may think of this as an object $P \in \mathbf{H}/X$ in the [[little topos]] over $X$. This way the objects of $LConst(X)$ are  indeed identified $\infty$-stacks over $X$.

=--


The following proposition says that the central statements of [[Galois theory]] hold for these canonical notions of geometric homotopy groups and locally constant $\infty$-stacks.

+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos|∞-connected]], we have

* a natural equivalence 

  $$
    LConst(X) \simeq \infty \mathrm{Grpd}(\Pi(X), \infty Grpd_\kappa)
  $$

  of locally constant $\infty$-stacks on $X$ with $\infty$-[[permutation representation]]s of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] of $X$ ([[local system]]s on $X$);

* for every point $x : * \to X$ a natural equivalence of the endomorphisms of the fiber functor $x^*$ and the [[loop space]] of $\Pi(X)$ at $x$

  $$
    End( x^* : LConst(X) \to \infty Grpd ) \simeq \Omega_x \Pi(X)
    \,.
  $$

=--

+-- {: .proof}
###### Proof

The first statement is just the adjunction $(\Pi \dashv Disc)$.

$$
  \begin{aligned}
     LConst(X) & := \mathbf{H}(X, Disc Core \infty Grpd_\kappa)
     \\
     &  \simeq \infty Grpd(\Pi(X), Core \infty Grpd_\kappa)
     \\
     &  \simeq \infty Grpd(\Pi(X), \infty Grpd_\kappa)     
  \end{aligned}
  \,.
$$


Using this and that $\Pi$ preserves the 
[[terminal object in an (∞,1)-category|terminal object]], so that the [[adjunct]] of
$(* \to X \to Disc Core \infty Grpd_\kappa)$ is
$(* \to \Pi(X) \to \infty Grpd_\kappa)$
the second statement follows with an iterated application of the [[(∞,1)-Yoneda lemma]] (this is pure [[Tannaka duality]] as discussed there):

The fiber functor $x^* : Func(\Pi(X), \infty Grpd) \to \infty Grpd$ evaluates an $(\infty,1)$-presheaf on $\Pi(X)^{op}$ at $x \in \Pi(X)$. By the [[(∞,1)-Yoneda lemma]] this is the same as homming out of $j(x)$, where $j : \Pi(X)^{op} \to Func(\Pi(X), \infty Grpd)$ is the [[(∞,1)-Yoneda embedding]]:

$$
  x^* \simeq Hom_{PSh(\Pi(X)^{op})}(j(x), -)
  \,.
$$

This means that $x^*$ itself is a representable object in $PSh(PSh(\Pi(X)^{op})^{op})$. If we denote by $\tilde j : PSh(\Pi(X)^{op})^{op} \to PSh(PSh(\Pi(X)^{op})^{op})$ the corresponding Yoneda embedding, then 

$$
  x^* \simeq \tilde j (j (x))
  \,.
$$

With this, we compute the endomorphisms of $x^*$ by applying the [[(∞,1)-Yoneda lemma]] two more times:

$$
  \begin{aligned}
    End x^*
     & \simeq
    End_{PSh(PSh(\Pi(X)^{op})^{op})} (\tilde j(j (x)))
     \\
     & \simeq
     End(PSh(\Pi(X))^{op}) (j(x))
     \\
     & \simeq
     End_{\Pi(X)^{op}}(x,x)
    \\
     & \simeq
     Aut_x \Pi(X)
    \\
     & =: \Omega_x \Pi(X)
  \end{aligned}
   \,.
$$

=--



### van Kampen theorem {#vanKampenTheorem}

A [[higher homotopy van Kampen theorem|higher]] [[van Kampen theorem]] asserts that passing to [[fundamental ∞-groupoid]]s preserves certain colimits. 

On a cohesive $(\infty,1)$-topos $\mathbf{H}$ the fundamental $\infty$-groupoid functor $\Pi : \mathbf{H} \to \infty Grpd$ is a [[left adjoint]] [[(∞,1)-functor]] and hence preserves all [[(∞,1)-colimit]]s.

More interesting is the question which $(\infty,1)$-colimits of [concrete spaces](#ConcreteObjects) in  

$$
  Conc(\mathbf{H}) 
    \stackrel{\overset{conc}{\leftarrow}}{\underset{inj}{\hookrightarrow}} 
  \mathbf{H}
$$ 

are preserved by $\Pi \circ inj : Conc(\mathbf{H}) \to \infty Grpd$. These colimits are computed by first computing them in $\mathbf{H}$ and then applying the concretization functor. So we have

+-- {: .un_lemma}
###### Observation

Let $U_\bullet : K \to Conc(\mathbf{H})$ be a [[diagram]] such that
the [[(∞,1)-colimit]]
$\lim_\to inj \circ U_\bullet$ is concrete, $\cdots \simeq inj(X)$.

Then the [[fundamental ∞-groupoid]] of $X$ is computed as the $(\infty,1)$-colimit

$$
  \Pi(X) \simeq {\lim_\to} \Pi(U_\bullet)
  \,.
$$


=--


In the [Examples](#Examples) we discuss the cohesive $(\infty,1)$-topos $\mathbf{H} = (\infty,1)Sh(TopBall)$ of [[topological ∞-groupoid]]s For that case we recover the ordinary [[higher van Kampen theorem]]:

+-- {: .un_prop}
###### Proposition

Let $X$ be a [[paracompact space|paracompact]] or [[locally contractible space|locally contractible]] [[topological space]]s and $U_1 \hookrightarrow X$, $U_2 \hookrightarrow X$ a [[covering]] by two [[open subsets]].

Then under the [[singular simplicial complex]] functor $Sing : Top \to $ [[sSet]] we have a [[homotopy pushout]]

$$
  \array{
    Sing(U_1) \cap Sing(U_2) &\to& Sing(U_2)
    \\
    \downarrow && \downarrow
    \\
    Sing(U_1) &\to& Sing(X)
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

We inject the topological space via the external [[Yoneda embedding]]

$$
  Top \hookrightarrow Sh(TopBalls) \hookrightarrow
  \mathbf{H} := (\infty,1)Sh(OpenBalls)
$$

as a 0-[[truncated]] [[topological ∞-groupoid]] in the cohesive 
$(\infty,1)$-topos $\mathbf{H}$. Being an [[(∞,1)-category of (∞,1)-sheaves]] this is [[locally presentable (∞,1)-category|presented]] by the [[Bousfield localization of model categories|left Bousfield localization]] $Sh(TopBalls, sSet)_{inj,loc}$ of the injective [[model structure on simplicial sheaves]] on $TopBalls$ (as described at [[models for ∞-stack (∞,1)-toposes]]). 

Notice that the injection $Top \hookrightarrow Sh(TopBalls)$ of topological spaces as [[concrete sheaves]] on the site of open balls preserves the pushout $X = U_1 \coprod_{U_1 \cap U_2} U_2$. (This is effectively the statement that $X$ as a [[representable functor|representable]] on [[Diff]] is a [[sheaf]].) Accordingly so does the further inclusion into $Sh(TopBall,sSet) \simeq Sh(TopBalls)^{\Delta^{op}}$ as simplicially constant simplicial sheaves.

Since cofibrations in that model structure are objectwise and degreewise injective maps, it follows that the ordinary [[pushout]] diagram

$$
  \array{
    U_1 \cap U_2 &\to& U_2
    \\
    \downarrow && \downarrow
    \\
    U_1 &\to& X
  }
$$

in $Sh(TopBalls, sSet)_{inj,loc}$ has all objects cofibrant and is the pushout along a cofibration, hence is a [[homotopy pushout]] (as described there). By the general theorem at [[(∞,1)-colimit]] homotopy pushouts model $(\infty,1)$-pushouts, so that indeed $X$ is the $(\infty,1)$-pushout

$$
  X \simeq U_1 \coprod_{U_1 \cap U_2} U_2 \in \mathbf{H}
  \,.
$$

The proposition now follows with the above observation that $\Pi$ preserves all $(\infty,1)$-colimits and with the statement (from [[topological ∞-groupoid]]) that for a topological space (locally contractible or paracompact) we have $\Pi X \simeq Sing X$.

=--




### Paths and geometric Postnikov towers {#Paths}

The [above](#Homotopy) construction of the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] of objects in $\mathbf{H}$ as an object in  [[∞Grpd]] may be reflected back into $\mathbf{H}$, where it gives a notion of homotopy [[path n-groupoid]]s and a geometric notion of [[Postnikov tower]]s of objects in $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]]
define the composite [[adjoint (∞,1)-functor]]s

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat}) 
  :=
  (Disc \Pi \dashv Disc \Gamma)
  : 
  \mathbf{H}
   \to 
  \mathbf{H}
  \,.
$$

=--


We say

* $\mathbf{\Pi}(X)$ is the **path $\infty$-groupoid** of $X$ -- the reflection of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] back into the cohesive context of $\mathbf{H}$;

* $\mathbf{\flat} A$ ("flat $A$") is the coefficient object for 
  **[flat differential A-cohomology](#FlatDifferentialCohomology)** 
  or for $A$-[[local system]]s

Write

$$
  (\tau_n \dashv i_n)
  :
  \mathbf{H}_{\leq n}
  \stackrel{\overset{\tau_{n}}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  \mathbf{H}
$$

for the [[reflective sub-(∞,1)-category]] of [[truncated|n-truncated object]]s and 

$$
  \mathbf{\tau}_n : 
    \mathbf{H} \stackrel{\tau_n}{\to} \mathbf{H}_{\leq n}
  \hookrightarrow
  \mathbf{H}
$$

for the truncation-[[localization of an (∞,1)-category|localization]] funtor. 

We say

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\Pi}_n}{\to}
   \mathbf{H} \stackrel{\mathbf{\tau}_n}{\to}
  \mathbf{H}
$$

is the **homotopy [[path n-groupoid]]** functor. 

We say that the (truncated) components of the $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]] 

$$
  X \to \mathbf{\Pi}(X)
$$

are the **constant path inclusions**. Dually we have canonical morphism

$$
  \mathbf{\flat}A \to A
  \,.
$$

+-- {: .un_lemma}
###### Observation

If $\mathbf{H}$ is cohesive, then $\mathbf{\flat}$ has a [[right adjoint]] $\mathbf{\Gamma}$

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma}) 
  :=
  (Disc \Pi \dashv Disc \Gamma \dashv coDisc \Gamma)
  : 
  \mathbf{H}
     \stackrel{\overset{\mathbf{\Pi}}{\to}}{\stackrel{\overset{\mathbf{\flat}}{\leftarrow}}{\underset{\mathbf{\Gamma}}{\to}}}
  \mathbf{H}
  \,.
$$

and this makes $\mathbf{H}$ be $\infty$-connected and locally $\infty$-connected over itself.

=--

+-- {: .un_def}
###### Proposition

Let $\mathbf{H}$ be a [[locally ∞-connected (∞,1)-topos]]. If $X \in \mathbf{H}$ is [[small-projective]] then the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is 

1. [[locally ∞-connected (∞,1)-topos|locally ∞-connected]];

1. [[local (∞,1)-topos|local]].


=--

+-- {: .proof}
###### Proof

The first statement is proven at [[locally ∞-connected (∞,1)-topos]], the second at [[local (∞,1)-topos]].

=--

+-- {: .un_def}
###### Proposition

In a cohesive $(\infty,1)$-topos $\mathbf{H}$, if $X$ is 
[[small-projective]] then so is its path ∞-groupoid $\mathbf{\Pi}(X)$.

=--

+-- {: .proof}
###### Proof

Because of the [[adjoint triple]] of [[adjoint (∞,1)-functor]]s 
$(\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma})$ we have for [[diagram]] $A : I \to \mathbf{H}$ that

$$
  \begin{aligned}
     \mathbf{H}(\mathbf{\Pi}(X), {\lim_\to}_i A_i)
     & \simeq 
     \mathbf{H}(X, \mathbf{\flat}{\lim_\to}_i A_i)
    \\
     & \simeq 
     \mathbf{H}(X, {\lim_\to}_i \mathbf{\flat} A_i)
     \\
     & \simeq 
     {\lim_\to}_i \mathbf{H}(X,  \mathbf{\flat} A_i)
  \end{aligned}
  \,,
$$ 

where in the last step we used that $X$ is [[small-projective]] by assumption.

=--



+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ we say that the **geometric Postnikov tower**
of $X$ is the [[Postnikov tower in an (∞,1)-category]] of $\mathbf{\Pi}(X)$:

$$
  \mathbf{\Pi}(X) \to \cdots
   \to 
   \mathbf{\Pi}_2(X) \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)
  \,.
$$

=--


### Universal coverings and geometric Whitehead towers {#Coverings}

We discuss an intrinsic notion of [[Whitehead tower]]s in a [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos]] $\mathbf{H}$.

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ a [[pointed object]], the **[[Whitehead tower in an (∞,1)-topos|geometric Whitehead tower]]** of $X$ is the sequence of objects 

$$
  X^{\mathbf{(\infty)}} \to \cdots \to X^{\mathbf{(2)}} \to X^{\mathbf{(1)}} \to X^{\mathbf{(0)}} \simeq X
$$

in $\mathbf{H}$, where for each $n \in \mathbb{N}$ the object $X^{(n+1)}$ is the [[homotopy fiber]] of the canonical morphism $X \to \mathbf{\Pi}_{n+1} X$ to the [path n+1-groupoid](#Paths) of $X$. 

We call $X^{\mathbf{(n+1)}}$ the $(n+1)$-fold 
**[[universal covering space]]** of $X$.

We write $X^{\mathbf{(\infty)}}$ for the homotopy fiber of the untruncated constant path inclusion.

$$
  X^{\mathbf{(\infty)}} \to X \to \mathbf{\Pi}(X)
  \,.
$$

Here the morphisms $X^{\mathbf{(n+1)}} \to X^{\mathbf{n}}$ are those induced from this <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">pasting diagram of (∞,1)-pullbacks</a>

$$
  \array{
    X^{\mathbf{(n)}} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X^{\mathbf{(n-1)}} & \to & \mathbf{B}^n \mathbf{\pi}_n(X) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X) &\to& \mathbf{\Pi}_{(n-1)}(X)
  }
  \,,
$$

where the object $\mathbf{B}^n \mathbf{\pi}_n(X)$ is defined as the [[homotopy fiber]] of the bottom right morphism.

=--

+-- {: .un_prop}
###### Proposition

Every object $X \in \mathbf{H}$ is covered by objects of the form $X^{\mathbf{(\infty)}}$ for different choices of base points in $X$, in the sense that every $X$ is the [[(∞,1)-colimit]] over a [[diagram]] whose vertices are of this form.

=--

+-- {: .proof}
###### Proof

Consider the diagram

$$
  \array{
    {\lim_\to}_{s \in \Pi(X)} (i^* *)
      &\to& {\lim_\to}_{s \in \Pi(X)} *
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    X &\stackrel{i}{\to}& \mathbf{\Pi}(X)
  }
  \,.
$$

The bottom morphism is the constant path inclusion, the $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]]. The right morphism is the [[equivalence in an (∞,1)-category]] that is the image under $Disc$ of the decomposition ${\lim_\to}_S * \stackrel{\simeq}{\to} S$ of every [[∞-groupoid]] as the [[(∞,1)-colimit]] (see there) over itself of the [[(∞,1)-functor]] constant on the point.

The left morphism is the [[(∞,1)-pullback]] along $i$ of this equivalence, hence itself an equivalence. By [[universal colimits]] in the [[(∞,1)-topos]] $\mathbf{H}$ the top left object is the [[(∞,1)-colimit]] over the single [[homotopy fiber]]s $i^* *_s$  of the form $X^{\mathbf{(\infty)}}$ as indicated. 


=--

+-- {: .un_prop}
###### Proposition

The inclusion $\Pi(i^* *) \to \Pi(X)$ of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] $\Pi(i^* *)$ of each of these objects into $\Pi(X)$ is homotopic to the point.

=--

+-- {: .proof}
###### Proof

We apply $\Pi(-)$ to the above diagram over a single vertex $s$ and attach the $(\Pi \dashv Disc)$-[[unit of an adjunction|counit]] to get

$$
  \array{
    \Pi(i^* *)
      &\to& 
      &\to&
      *
    \\
    \downarrow && && \downarrow 
    \\
    \Pi X &\stackrel{\Pi(i)}{\to}& \Pi Disc \Pi(X)
     &\to& \Pi(X)
  }
  \,.
$$

Then the bottom morphism is an equivalence by the $(\Pi \dashv Disc)$-[[zig-zag-identity]].

=--





### Flat $\infty$-connections and local systems {#FlatDifferentialCohomology}

We describe for a [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ a canonical intrinsic notion of _flat_ [[connections on ∞-bundles]], _flat_ [[higher parallel transport]] and higher [[local system]]s.

Write $(\mathbf{\Pi} \dashv\mathbf{\flat}) := (Disc \Pi \dashv Disc \Gamma) : \mathbf{H} \to \mathbf{H}$ for the adjunction given by the [path ∞-groupoid](#Paths). Notice that this comes with the canonical $(\Pi \dashv Disc)$-[[unit of an adjunction|unit]] with components

$$
  X \to \mathbf{\Pi}(X)
$$

and the $(Disc \dashv \Gamma)$-counit with components

$$
  \mathbf{\flat} A \to A
  \,.
$$

+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}$ we write

$$
  \mathbf{H}_{flat}(X,A) := \mathbf{H}(\mathbf{\Pi}X, A)
$$

and call $H_{flat}(X,A) := \pi_0 \mathbf{H}_{flat}(X,A)$ the **flat (nonabelian) differential cohomology** of $X$ with coefficients in $A$.

We say a morphism $\nabla : \mathbf{\Pi}(X) \to A$ is a **flat [[connection on an ∞-bundle|∞-connnection]] on the [[principal ∞-bundle]] corresponding to $X \to \mathbf{\Pi}(X) \stackrel{\nabla}{\to} A$, or an **$A$-[[local system]]** on $X$.

The induced morphism

$$
  \mathbf{H}_{flat}(X,A) \to \mathbf{H}(X,A)
$$

we say is the [[forgetful functor]] that forgets flat connections.


=--

+-- {: .un_remark}
###### Remark

The object $\mathbf{\Pi}(X)$ has the interpretation of the [path ∞-groupoid](#Paths) of $X$: it is a cohesive $\infty$-groupoid whose [[k-morphism]]s may be thought of as generated from the $k$-morphisms in $X$ and $k$-dimensional cohesive paths in $X$.

Accordingly a mophism $\mathbf{Pi}(X) \to A$ may be thought of as assigning

* to each point of $X$ a fiber in $A$;

* to each path in $X$ an equivalence between these fibers;

* to each disk in $X$ a  2-equivalalence between these equivaleces associated to its boundary

* and so on.

This we think of as encoding a flat [[higher parallel transport]] on $X$, coming from some flat $\infty$-connection and _defining_ this flat $\infty$-connection.

=--

+-- {: .un_lemma}
###### Observation


By the $(\mathbf{\Pi} \dashv \mathbf{\flat})$-adjunction we have a [[natural transformation|natural]] equivalence

$$
  \mathbf{H}_{flat}(X,A) \simeq \mathbf{H}(X,\mathbf{\flat}A)
  \,.
$$

A [[cocycle]] $g : X \to A$ for a [[principal ∞-bundle]] on $X$ is in the image of 

$$
  \mathbf{H}_{flat}(X,A) \to \mathbf{H}(X,A)
$$

precisely if there is a lift $\nabla$ in the [[diagram]]

$$
  \array{
     && \mathbf{\flat}A 
     \\
     & {}^{\nabla}\nearrow& \downarrow
    \\
    X &\stackrel{g}{\to}& A
  }
  \,.
$$

=--

We call $\mathbf{\flat}A$ the **coefficient object for flat $A$-connections**. 

+-- {: .un_prop}
###### Proposition

For $G := Disc G_0 \in \mathbf{H}$ a [[discrete ∞-groupoid|discrete ∞-group]] the canonical morphism $\mathbf{H}_{flat}(X,\mathbf{B}G) \to \mathbf{H}(X,\mathbf{B}G)$ is an [[equivalence in an (∞,1)-category|equivalence]].

=--

+-- {: .proof}
###### Proof

Since $Disc$ is a [[full and faithful (∞,1)-functor]] we have that the  [[unit of an adjunction|unit]] $Id \to \Gamma Disc $ is a natural equivalence. It follows that on $Disc G_0$ also the counit $Disc \Gamma Disc G_0 \to Disc G_0$ is a weak equivalence (since by the [[triangle identity]] we have that $Disc G_0 \stackrel{\simeq}{\to} Disc \Gamma Disc G_0 \to Disc G_0$ is the identity).

=--

+-- {: .un_remark}
###### Remark

This says that for discrete structure [[∞-group]]s $G$ there is an essentially unique flat $\infty$-connection on any $G$-[[principal ∞-bundle]]. Moreover, the further equivalence

$$
  \mathbf{H}(\mathbf{\Pi}(X), \mathbf{B}G)
  \simeq
  \mathbf{H}_{flat}(X, \mathbf{B}G)
  \simeq
  \mathbf{H}(X, \mathbf{B}G)
$$

may be read as saying that the $G$-principal $\infty$-bundle
is entirely characterized by the flat [[higher parallel transport]]
of this unique $\infty$-connection.

=--


### de Rham cohomology 
  {#deRhamCohomology}

In every [[locally ∞-connected (∞,1)-topos]] $\mathbf{H}$ there is an intrinsic notion of [[nonabelian cohomology|nonabelian]] [[de Rham cohomology]].

+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ an object, write $\mathbf{\Pi}_{dR}X := * \coprod_X \mathbf{\Pi} X$
for the [[(∞,1)-colimit|(∞,1)-pushout]]

$$
  \array{
    X &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{\Pi}(X) &\to& \mathbf{\Pi}_{dR}X
  }
  \,.
$$

For $* \to A$ any [[pointed object]] in $\mathbf{H}$, write 
$\mathbf{\flat}_{dR} A : * \prod_A \mathbf{\flat}A$ for the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{\flat}_{dR} A &\to& \mathbf{\flat} A 
    \\
    \downarrow && \downarrow
    \\
    * &\to& A
  }
  \,.
$$


=--

+-- {: .un_prop #DeRhamAdjunction}
###### Proposition

This construction yields a pair of [[adjoint (∞,1)-functor]]s 

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} )
  : 
  */\mathbf{H}
  \stackrel{
     \overset{\mathbf{\Pi}_{dR}}{\leftarrow}
   }{
     \underset{\mathbf{\flat}_{dR}}{\to}
   }
  \mathbf{H}
  \,.
$$


=--

+-- {: .proof}
###### Proof

We check the defining natural hom-equivalence

$$
  {*}/\mathbf{H}(\mathbf{\Pi}_{dR}X,A)
  \simeq
  \mathbf{H}(X, \mathbf{\flat}_{dR}A)
  \,.
$$

The hom-space in the [[over-(∞,1)-category|under-(∞,1)-category]] $*/\mathbf{H}$ is (as discussed there), computed by the [[(∞,1)-pullback]]

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
     \mathbf{H}(\mathbf{\Pi}_{dR}X, A)
     \\
     \downarrow && \downarrow
     \\
     * &\stackrel{pt_A}{\to}& \mathbf{H}(*,A)
  }
  \,.
$$

By the fact that the [[hom-functor]]  $\mathbf{H}(-,-) : \mathbf{H}^{op} \times \mathbf{H} \to \infty Grpd $ preserves limits in both arguments we have a natural equivalence

$$
  \begin{aligned}
     \mathbf{H}(\mathbf{\Pi}_{dR} X, A)
     & :=
     \mathbf{H}( *\coprod_{X} \mathbf{\Pi}(X), A  )     
     \\
     & \simeq 
     \mathbf{H}(*,A) \prod_{\mathbf{H}(X,A)} 
      \mathbf{H}(\mathbf{\Pi}(X),A)
  \end{aligned}
  \,.
$$

We paste this pullback to the above pullback diagram to obtain

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
     \mathbf{H}(\mathbf{\Pi}_{dR}X, A) &\to&
      \mathbf{H}(\mathbf{\Pi}(X),A)
     \\
     \downarrow && \downarrow  && \downarrow
     \\
     * &\stackrel{pt_A}{\to}& \mathbf{H}(*,A)
     &\to& 
      \mathbf{H}(X,A)
  }
  \,.
$$

By the pasting law for [[(∞,1)-pullback]]s the outer diagram is still a pullback. We may evidently rewrite the bottom composite as in

$$
  \array{
     */\mathbf{H}(\mathbf{\Pi}_{dR}X, A)
      &\to&
      &\to&
      \mathbf{H}(\mathbf{\Pi}(X),A)
     \\
     \downarrow && && \downarrow
     \\
     * &\stackrel{\simeq}{\to}& \mathbf{H}(X,*)
     &\stackrel{(pt_A)_*}{\to}& 
      \mathbf{H}(X,A)
  }
  \,.
$$

This exhibits the hom-space as the pullback

$$
  \begin{aligned}
    */\mathbf{H}(\mathbf{\Pi}_{dR}(X),A)
    \simeq
     \mathbf{H}(X,*) \prod_{\mathbf{H}(X,A)} \mathbf{H}(X,\mathbf{\flat} A)
   \end{aligned}
  \,,
$$

where we used the $(\mathbf{\Pi} \dashv \mathbf{\flat})$-adjunction. Now using again that $\mathbf{H}(X,-)$ preserves pullbacks, this is

$$
  \cdots \simeq \mathbf{H}(X, * \prod_A \mathbf{\flat}A )
  \simeq \mathbf{H}(X , \mathbf{\flat}_{dR}A)
  \,.
$$


=--

+-- {: .un_prop #TripleOfDeRhamAdjunctions}
###### Observation

If $\mathbf{H}$ is also [[local (∞,1)-topos|local]], then there is a further [[right adjoint]] $\mathbf{\Gamma}_{dR}$

$$
  (\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} \dashv \mathbf{\Gamma}_{dR})
  :
  \mathbf{H}
    \stackrel{\overset{\mathbf{\Pi}_{dR}}{\to}}{\stackrel{\stackrel{\mathbf{\flat}_{dR}}{\leftarrow}}{\underset{\mathbf{\Gamma}_{dR}}{\to}}}
  */\mathbf{H}
$$

given by

$$
  \mathbf{\Gamma}_{dR} X {:=}
    * \coprod_{X} \mathbf{\Gamma}(X)
  \,,
$$

where $(\mathbf{\Pi} \dashv \mathbf{\flat} \dashv \mathbf{\Gamma}) : \mathbf{H} \to \mathbf{H}$ is the triple of adjunctions discussed at [Paths](#Paths).

=--

+-- {: .proof}
###### Proof

This follows by the same kind of argument as above.

=--

+-- {: .un_def}
###### Definition

For $X, A \in \mathbf{H}$ we write

$$
  \mathbf{H}_{dR}(X,A)
  :=
  \mathbf{H}(\mathbf{\Pi}_{dR}X, A)
  \simeq
  \mathbf{H}(X, \mathbf{\flat}_{dR} A)
  \,.
$$

A [[cocycle]] $\omega : X \to \mathbf{\flat}_{dR}A$ we call an **flat $A$-valued differential form** on $X$.

We say that $H_{dR}(X,A) {:=} \pi_0 \mathbf{H}_{dR}(X,A)$
is the **de Rham cohomology** of $X$ with coefficients in $A$.

=--

+-- {: .un_remark}
###### Observation

A [[cocycle]] in de Rham cohomology

$$
  \omega : \mathbf{\Pi}_{dR}X \to A
$$

is precisely a [flat ∞-connetion](#FlatDifferentialCohomology) on a _trivializable_ $A$-principal $\infty$-bundle. More precisely, $\mathbf{H}_{dR}(X,A)$ is the [[homotopy fiber]] of the [[forgetful functor]] from $\infty$-bundles with flat $\infty$-connection to $\infty$-bundles: we have an [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{dR}(X,A) &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{flat}(X,A) &\to& \mathbf{H}(X,A)
  }  
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows by the fact that the [[hom-functor]] $\mathbf{H}(X,-)$ preserves the defining [[(∞,1)-pullback]] for $\mathbf{\flat}_{dR} A$.

=--

Just for emphasis, notice the dual description of this situation: by the [[universal property]] of the [[(∞,1)-colimit]] that defines $\mathbf{\Pi}_{dR} X$ we have that $\omega$ corresponds to a diagram

$$
  \array{
    X &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    \mathbf{\Pi}(X) &\stackrel{\omega}{\to}& A
  }
  \,.
$$

The bottom horizontal morphism is a flat connection on the 
$\infty$-bundle given by the cocycle $X \to \mathbf{\Pi}(X) \stackrel{\omega}{\to} A$. The diagram says that this is equivalent to the trivial bundle given by the trivial cocycle $X \to * \to A$.

+-- {: .un_prop #deRhamWithDiscCoeffsIsTrivial}
###### Proposition

The de Rham cohomology with coefficients in discrete objects is trivial: for all $S \in \infty Grpd$ we have

$$
  \mathbf{\flat}_{dR} Disc S \simeq *
  \,.
$$


=--

+-- {: .proof}
###### Proof

Using that in a [[∞-connected (∞,1)-topos]] the functor $Disc$ is a [[full and faithful (∞,1)-functor]] so that the [[unit of an adjunction|unit]] $Id \to \Gamma Disc $ is an [[equivalence in an (∞,1)-category|equivalence]] and using that by the [[zig-zag identity]]  we have then that the [[unit of an adjunction|counit]] component
$\mathbf{\flat} Disc S := Disc \Gamma Disc S \to Disc S$ is also an equivalence, we have


$$
  \begin{aligned}
     \mathbf{\flat}_{dR} Disc S 
     & {:=}
     * \prod_{Disc S} \mathbf{\flat} Disc S
     \\
     & \simeq * \prod_{Disc S} Disc S
     \\
     & \simeq *
  \end{aligned}
  \,,
$$

since the pullback of an equivalence is an equivalence.

=--

+-- {: .un_prop}
###### Proposition

In a cohesive $\mathbf{H}$  _[pieces have points](#PiecesHavePoints)_ precisely if for all $X \in \mathbf{H}$, the de Rham coefficient object $\mathbf{\Pi}_{dR} X $ is
_globally [[connected]]_ in that $\pi_0 \mathbf{H}(*, \mathbf{\Pi}_{dR}X) = *$.

If $X$ has at least one point ($\pi_0(\Gamma X) \neq \emptyset $) 
and is geometrically connected ($\pi_0 (\Pi X) = {*}$) then 
$\mathbf{\Pi}_{\mathrm{dR}}(X)$ is also locally connected: 
$\tau_0 \mathbf{\Pi}_{\mathrm{dR}}X \simeq {*} \in \mathbf{H}$.

=--

+-- {: .proof}
###### Proof

Since $\Gamma$ preserves [[(∞,1)-colimit]]s in a cohesive $(\infty,1)$-topos we have

$$
  \begin{aligned}
    \mathbf{H}(*, \mathbf{\Pi}_{dR}X)
    & \simeq
    \Gamma \mathbf{\Pi}_{dR} X
    \\  
    & \simeq
    * \coprod_{\Gamma X} \Gamma \mathbf{\Pi}X  
    \\
    & \simeq
    * \coprod_{\Gamma X} \Pi X  
  \end{aligned}
  \,,
$$

where in the last step we used that $Disc$ is a [[full and faithful (∞,1)-functor|full and faithful]], so that there is an equivalence $\Gamma \mathbf{\Pi}X := \Gamma Disc \Pi X \simeq \Pi X$.

To analyse this [[(∞,1)-colimit|(∞,1)pushout]] 
we present it by a  [[homotopy pushout]] in 
the standard [[model structure on simplicial sets]] $\mathrm{sSet}_{\mathrm{Quillen}}$. 
Denoting by $\Gamma X$ and $\Pi X$ any representatives in $\mathrm{sSet}_{\mathrm{Quillen}}$ of the objects of the same name in 
$\infty \mathrm{Grpd}$, this may be computed by the ordinary [[pushout]] in [[sSet]]

$$
  \array{
    \Gamma X  &\to& (\Gamma X) \times \Delta[1] \coprod_{\Gamma X} {*}
    \\
    \downarrow && \downarrow
    \\
    \Pi X &\to & Q
  }
  \,,
$$

where on the right we have inserted the [[cone]] on $\Gamma X$ in order to turn the top morphism into a cofibration. From this ordinary pushout it is clear that the connected components of $Q$ are obtained from those of 
$\Pi X$ by identifying all those
in the image of a connected component of $\Gamma X$. So if the left morphism is surjective on
$\pi_0$ then $\pi_0(Q) = *$. This is precisely the condition that 
[pieces have points](#PiecesHavePoints) in $\mathbf{H}$.

For the local analysis we consider the same setup objectwise in the injective [[model structure on simplicial presheaves]]
$[C^{\mathrm{op}}, \mathrm{sSet}]_{\mathrm{inj},\mathrm{loc}}$. 
For any $U \in C$
we then have the pushout $Q_U$ in

$$
  \array{
    X(U) &\to & (X(U)) \times \Delta[1] \coprod_{X(U)} {*}
    \\
    \downarrow && \downarrow
    \\
    \mathrm{sSet}(\Gamma(U), \Pi X) & \to & Q_U
  }
  \,,
$$

as a model for the value of the simplicial presheaf presenting $\mathbf{\Pi}_{\mathrm{dR}}(X)$.
If $X$ is geometrically connected then $\pi_0 \mathrm{sSet}(\Gamma(U), \Pi(X)) = *$
and hence for the left morphism to be surjective on $\pi_0$ it suffices that the top left
object is not empty. Since the simplicial set $X(U)$ contains at least the vertices 
$U \to * \to X$ of which there is by assumption at least one, this is the case.

=--

+-- {: .un_remark}
###### Remark

In summary this means that in a cohesive $(\infty,1)$-topos the objects $\mathbf{\Pi}_{dR} X$ have the abstract properties of [[de Rham schematic homotopy type|pointed geometric de Rham homotopy types]].

In the [Examples](#Examples) we will see that, indeed, the intrinsic de Rham cohomology $H_{dR}(X, A) {:=} \pi_0 \mathbf{H}(\mathbf{\Pi}_{dR} X, A)$ reproduces ordinary de Rham cohomology in degree $d\gt 1$.

In degree 0 the intrinsic de Rham cohomology is necessrily trivial, while in degree 1 we find that it reproduces closed 1-forms, not divided out by exact forms. This difference to ordinary de Rham cohomology in the lowest two degrees may be interpreted in terms of the obstruction-theoretic meaning of de Rham cohomology by which we essentially characterized it above: we have that the intrinsic $H_{dR}^n(X,K)$ is the home for the obstructions to flatness of $\mathbf{B}^{n-2}K$-[[principal ∞-bundle]]s. For $n = 1$ this are groupoid-principal bundles over the _groupoid_ with $K$ as its space of objects. But the 1-form curvatures of groupoid bundles are not to be regarded modulo exact forms. More details on this are at [[circle n-bundle with connection]].

=--


### Exponentiated $\infty$-Lie algebras {#LieAlgebras}


+-- {: .un_def #ExponentiatedLieAsGeometricallyContractible}
###### Definition


For a [[connected]] object $\mathbf{B}\exp(\mathfrak{g}) $ in $\mathbf{H}$ that is _geometrically contractible_

$$
  \Pi (\mathbf{B}\exp(\mathfrak{g})) \simeq *
$$

we call its [[loop space object]] 
$\exp(\mathfrak{g}) := \Omega_* \mathbf{B}\exp(\mathfrak{g})$ the  **[[Lie integration]] of an [[∞-Lie algebra]]** in $\mathbf{H}$. 

=--



+-- {: .un_def}
###### Definition

Set

$$
  \exp Lie
  := 
  \mathbf{\Pi}_{dR} \circ \mathbf{\flat}_{dR} 
  : */\mathbf{H} \to */\mathbf{H}
  \,.
$$

=--

+-- {: .un_prop #LieAsALeftAdjoint}
###### Observation


If $\mathbf{H}$ is cohesive, then $\exp Lie$ is a [[left adjoint]].


=--

+-- {: .proof}
###### Proof

When $\mathbf{H}$ is cohesive we have the [de Rham triple of adjunction](#TripleOfDeRhamAdjunctions) 
$(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR} \dashv \mathbf{\Gamma}_{dR})$. Accordingly then $Lie$ is part of an [[adjunction]]

$$
  (\exp Lie \dashv \mathbf{\Gamma}_{dR}\mathbf{\flat}_{dR})
  \,.
$$

=--

+-- {: .un_example}
###### Proposition/Example

For all $X$ the object $\mathbf{\Pi}_{dR}(X)$ is geometrically contractible.

=--

+-- {: .proof}
###### Proof

Since on the [[locally ∞-connected (∞,1)-topos]] and [[∞-connected (∞,1)-topos|∞-connected]] $\mathbf{H}$ the functor $\Pi$ preserves [[(∞,1)-colimit]]s and the [[terminal object in an (∞,1)-category|terminal object]], we have

$$
  \begin{aligned}
    \Pi \mathbf{\Pi}_{dR} X
    & {:=}
     \Pi (*) \coprod_{\Pi X} \Pi \mathbf{\Pi} X
    \\
    & \simeq
      * \coprod_{\Pi X} \Pi Disc \Pi X   
    \\
    & \simeq 
      * \coprod_{\Pi X} \Pi X
    & \simeq
      *
  \end{aligned}
  \,,
$$

where we used that in the [[∞-connected (∞,1)-topos|∞-connected]] $\mathbf{H}$ the functor $Disc$ is[[full and faithful (∞,1)-functor|full and faithful]].

=--

+-- {: .un_corollary}
###### Corollary

We have for every $\mathbf{B}G$ that $\exp Lie \mathbf{B}G$ is geometrically contractible.

=--


We shall write $\mathbf{B}\exp(\mathfrak{g})$ for $\exp Lie \mathbf{B}G$, when the context is clear. 


+-- {: .un_prop #LieValuesofDeRham}
###### Proposition


Every [de Rham cocycle](#deRhamCohomology) $\omega : \mathbf{\Pi}_{dR} X \to \mathbf{B}G$ factors through the ∞-Lie algebra of $G$

$$
  \array{
     && \mathbf{B}\exp(\mathfrak{g})
     \\
     & \nearrow & \downarrow
     \\
     \mathbf{\Pi}_{dR}X 
     &\stackrel{\omega}{\to}&
     \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the <a href="http://ncatlab.org/nlab/show/adjoint+functor#UniversalArrows">universality of the counit</a> of $(\mathbf{\Pi}_{dR} \dashv \mathbf{\flat}_{dR})$ we have that $\omega$ factors through the [[unit of an adjunction|counit]] 
$\exp Lie \mathbf{B}G \to \mathbf{B}G$. 

=--


Therefore instead of speaking of a $G$-valued de Rham cocycle, it is less  redundant to speak of an $\exp(\mathfrak{g})$-valued de Rham cocycle. In particular we have the following.


+-- {: .un_prop}
###### Corollary

Every morphism $\exp Lie \mathbf{B}H \to \mathbf{B}G$ from an exponentiated $\infty$-Lie algebra to an $\infty$-group factors through the exponentiated $\infty$-Lie algebra of that $\infty$-group

$$
  \array{
    \mathbf{B}\exp(\mathfrak{h}) &\to& \mathbf{B}\exp(\mathfrak{g})
    \\
    & \searrow& \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

=--


+-- {: .un_prop}
###### Proposition

If $\mathbf{H}$ is cohesive then we have 

$$
  \exp Lie \circ \exp Lie \simeq \exp Lie \circ \Sigma \circ \Omega
  \,.
$$

=--

+-- {: .proof}
###### Proof

First observe that for all $A \in */\mathbf{H}$ we have

$$
  \mathbf{\flat} \mathbf{\flat}_{dR} A \simeq *
$$

This follows using

* $\mathbf{\flat}$ is a [[right adjoint]] and hence preserves [[(∞,1)-pullback]]s;

* $\mathbf{\flat} \mathbf{\flat} := Disc \Gamma Disc \Gamma \simeq Disc \Gamma =: \mathbf{\flat}$ by the fact that $Disc$ is a 
  [[full and faithful (∞,1)-functor]]; 

* the counit $\mathbf{\flat} \mathbf{\flat} A \to \mathbf{\flat} A$ is equivalent to the identity, by the [[zig-zag-identity]] of the [[adjunction]] and using that equivalences satisfy [[category with weak equivalences|2-out-of-3]].

by computing

$$
  \begin{aligned}
    \mathbf{\flat} \mathbf{\flat}_{dR} A
    & 
    * \times_{\mathbf{\flat}A} \mathbf{\flat}\mathbf{\flat}A
    \\
    & \simeq 
    * \times_{\mathbf{\flat}A} \mathbf{\flat}A
    \\
    & \simeq *
 \end{aligned} 
 \,,
$$

using that the [[(∞,1)-pullback]] of an [[equivalence in an (∞,1)-category|equivalence]] is an equivalence.


From this we deduce that

$$
  \mathbf{\flat}_{dR} \circ \mathbf{\flat}_{dR} 
  \simeq \mathbf{\flat}_{dR} \circ \Omega
  \,.
$$

by computing for all $A \in \mathbf{H}$

$$
  \begin{aligned}
    \mathbf{\flat}_{dR} \circ \mathbf{\flat}_{dR} A
    & \simeq 
    * \times_{\mathbf{\flat}_{dR} A} \mathbf{\flat}\mathbf{\flat}_{dR} A
    \\
    & \simeq
    * \times_{\mathbf{\flat}_{dR} A} *
    \\
    & \simeq
    \mathbf{\flat}_{dR}( * \times_A * )
    \\
    & \simeq \mathbf{\flat}_{dR} \Omega A
  \end{aligned}
  \,.
$$

Also observe that by a [proposition above](#deRhamWithDiscCoeffsIsTrivial) we have

$$
  \mathbf{\flat}_{dR} \mathbf{\Pi} X \simeq *
$$

for all $X \in \mathbf{H}$.


Finally to obtain $\exp Lie \circ \exp Lie$ we do one more computation of this sort, using that 

* $\exp Lie := \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR}$ preserves the terminal object (since $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos|∞-connected]]) 

* and that it is a [[left adjoint]] by [the above](#LieAsALeftAdjoint), since $\mathbf{H}$ is assumed to be cohesive.

We compute:

$$
  \begin{aligned}
    \exp Lie \exp Lie A 
    & \simeq 
    \exp Lie \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} A
    \\
    & \simeq
      * 
        \coprod_{\exp Lie \mathbf{\flat}_{dR} A} 
      \exp Lie \mathbf{\Pi} \mathbf{\flat}_{dR} A
    \\
    & \simeq
      * 
        \coprod_{\exp Lie \mathbf{\flat}_{dR} A} 
      \mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{\Pi} \mathbf{\flat}_{dR} A
    \\
    & \simeq 
    * \coprod_{\exp Lie \mathbf{\flat}_{dR} A} *    
    \\
    & \simeq 
    * \coprod_{\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \mathbf{\flat}_{dR} A} *
    \\
    & \simeq 
    * \coprod_{\mathbf{\Pi}_{dR} \mathbf{\flat}_{dR} \Omega A} *   
    \\
    & \simeq
    * \coprod_{\exp Lie \Omega A} *   
    \\
    & \simeq
    \exp Lie ( * \coprod_{\Omega A} * )
    \\
    & \simeq
    \exp Lie \Sigma \Omega A  
  \end{aligned} 
  \,.
$$

=--



### Maurer-Cartan forms and curvature characteristic forms      
  {#CurvatureCharacteristics}

In the [intrinsic de Rham cohomology](#deRhamCohomology) of a [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos|∞-connected]] there exist canonical cocycles that we may identify with [[Maurer-Cartan form]]s and with universal [[curvature characteristic form]]s.

+-- {: .un_def}
###### Definition

For $G \in \mathbf{H}$ an [[∞-group]], write

$$
  \theta : G \to \mathbf{\flat}_{dR} \mathbf{B}G
$$

for the $\mathfrak{g}$-[valued](#LieAlgebras) 
de Rham cocycle on $G$ which is induced by the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">(∞,1)-pullback pasting</a>

$$
  \array{
     G &\to& *
     \\
     {}^{\mathllap{\theta}}\downarrow && \downarrow
     \\
     \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat}\mathbf{B}G
     \\
     \downarrow && \downarrow
     \\
     * &\to& \mathbf{B}G 
  }
$$

and the [above proposition](#LieValuesofDeRham).

We call $\theta$ the **[[Maurer-Cartan form]]** on $G$.

=--

+-- {: .un_remark}
###### Remark

By postcomposition the Maurer-Cartan form sends $G$-valued functions on $X$ to $\mathfrak{g}$-valued forms on $X$

$$
  \theta_* : \mathbf{H}(X,G) \to 
    \mathbf{H}^1_{dR}(X,G)
  \,.
$$

=--


+-- {: .un_defn #UniversalCurvatureForms}
###### Definition


For $G = \mathbf{B}^n A$ an [[Eilenberg-MacLane object]], we also write 

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
$$

for the intrinsic Maurer-Cartan form and call this the intrinsic **universal [[curvature characteristic form]]** on $\mathbf{B}^n A$.

=--



### Differential cohomology 
 {#DifferentialCohomology}

In every [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] [[∞-connected (∞,1)-topos]] there is an intrinsic notion of [[ordinary differential cohomology]].

Fix a 0-[[truncated]] [[abelian group|abelian]] [[group object]] $A \in \tau_{\leq 0} \mathbf{H} \hookrightarrow \mathbf{H}$. For all $n \in \mathbf{N}$ we have then the [[Eilenberg-MacLane object]] $\mathbf{B}^n A$.

+-- {: .un_def }
###### Definition 

For $X \in \mathbf{H}$ any object and $n \geq 1$ write

$$
  \mathbf{H}_{diff}(X,\mathbf{B}^n A) := 
    \mathbf{H}(X,\mathbf{B}^n A) \prod_{\mathbf{H}_{dR}(X,\mathbf{B}^n A)}
    H_{dR}^{n+1}(X,A)
$$ 

for the cocycle $\infty$-groupoid of [[twisted cohomology]], def. \ref{TwistedCohomologyInOvertopos}, of $X$ with coefficients in $A$ and with twist given by the canonical [curvature characteristic morphism](#CurvatureCharacteristics) 
$curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1} A$. This is the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{diff}(X,\mathbf{B}^n A) 
      &\stackrel{[F]}{\to}& 
     H_{dR}^{n+1}(X,A)
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n A) 
        &\stackrel{curv_*}{\to}& 
     \mathbf{H}_{dR}(X,\mathbf{B}^{n+1} A)
  }
  \,,
$$

where the right vertical morphism $H^{n+1}_{dR}(X) = \pi_0 \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)
 \to \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)$ is any choice of cocycle representative for each cohomology class: a choice of point in every connected component.

We call

$$
  H_{diff}^n(X,A) {:=} \pi_0 \mathbf{H}_{diff}(X, \mathbf{B}^{n} A)
$$

the degree-$n$ **[[differential cohomology]]** of $X$ with coefficient in $A$.

For $\nabla \in \mathbf{H}_{diff}(X,\mathbf{B}^n A)$ a [[cocycle]], we call

* $[\eta(\nabla)] \in H^n(X,A)$ the class of the **underlying 
   $\mathbf{B}^{n-1} A$-[[principal ∞-bundle]]**;

* $F(\nabla) \in H_{dR}^{n+1}(X,A)$ the **[[curvature]]** class of $c$.


We also say $\nabla$ is an **$\infty$-connection** on $\eta(\nabla)$ (see [below](#ChernWeilTheory)).

=--

+-- {: .un_prop #DiffCohIsWellDefined}
###### Observation

The differential cohomology $H_{diff}^n(X,A)$ does not depend on the choice of morphism $H_{dR}^{n+1}(X,A) \to \mathbf{H}_{dR}(X, \mathbf{B}^{n+1}A)$ (as long as it is an isomorphism on $\pi_0$, as required).
In fact, for different choices the corresponding cocycle [[∞-groupoid]]s $\mathbf{H}_{diff}(X,\mathbf{B}^n A)$ are equivalent.

=--

+-- {: .proof}
###### Proof

The set  

$$
  H_{dR}^{n+1}(X,A) = \coprod_{H_{dR}^{n+1}(X,A)} {*} 
$$ 

is, as a 0-[[truncated]] [[∞-groupoid]], an [[(∞,1)-coproduct]] of the [[terminal object in an (∞,1)-category|terminal object]] in [[∞Grpd]]. By [[universal colimits]] in this [[(∞,1)-topos]] we have that [[(∞,1)-colimit]]s are preserved by [[(∞,1)-pullback]]s, so that $\mathbf{H}_{diff}(X, \mathbf{B}^n A)$ is the coproduct 

$$
  \mathbf{H}_{diff}(X,\mathbf{B}^n A) \simeq
  \coprod_{H_{dR}^{n+1}(X,A)} 
   \left(
   \mathbf{H}(X,\mathbf{B}^n A) 
      \prod_{\mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)} 
    {*}
  \right)
$$

of the [[homotopy fiber]]s of $curv_*$ over each of the chosen points $* \to \mathbf{H}_{dR}(X,\mathbf{B}^{n+1}A)$. These homotopy fibers only  depend, up to equivalence, on the connected component over which they are taken.

=--

+-- {: .un_prop #DiffCohomologyRestrictedToVanishingCurvature}
###### Proposition

When restricted to vanishing curvature, differential cohomology coincides with [flat differential cohomology](#FlatDifferentialCohomology):

$$
  H_{diff}^n (X,A)|_{[F] = 0} \simeq H_{flat}(X,\mathbf{B}^n A)
  \,.
$$

Moreover this is true at the level of [[cocycle]] [[∞-groupoid]]s

$$
 \left(
  \mathbf{H}_{diff}(X, \mathbf{B}^n A) 
    \prod_{H_{dR}^{n+1}(X,A)} \{[F] = 0\}
  \right)
  \simeq
  \mathbf{H}_{flat}(X,\mathbf{B}^n A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-pullback#QuasiCatPastingLaw">pasting law for (∞,1)-pullbacks</a> the claim is equivalently that we have a an $(\infty,1)$-pullback diagram

$$
  \array{
    \mathbf{H}_{flat}(X, \mathbf{B}^n A) &\to& {*}
    \\
    \downarrow && \downarrow^{\mathrlap{\{[F] = 0\}}}
    \\
    \mathbf{H}_{diff}(X,\mathbf{B}^n A) &\stackrel{[F]}{\to}& 
     H_{dR}^{n+1}(X,A)
    \\
    {}^{\mathllap{\eta}}\downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B}^n A) 
        &\stackrel{curv_*}{\to}& 
     \mathbf{H}_{dR}(X,\mathbf{B}^{n+1} A)
  }
  \,.
$$

By definition of flat cohomology and of intrinsic de Rham cohomology
in $\mathbf{H}$, the outer rectangle is 

$$
  \array{
    \mathbf{H}(X,\mathbf{\flat}\mathbf{B}^n A) &\to& {*}
    \\ 
    \downarrow && \downarrow 
    \\
    \mathbf{H}(X, \mathbf{B}^n A) 
      &\stackrel{curv_*}{\to}&
    \mathbf{H}(X, \mathbf{\flat}_{dR}\mathbf{B}^{n+1} A)
  }
  \,.
$$

Since the [[hom-functor]] $\mathbf{H}(X,-)$ preserves [[(∞,1)-limit]]s this is a pullback if

$$
  \array{
    \mathbf{\flat} \mathbf{B}^n A &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}^n A 
      &\stackrel{curv}{\to}& 
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
  }
$$

is. Indeed, this is one step in the [[fiber sequence]] 

$$
   \cdots
   \to 
   \mathbf{\flat} \mathbf{B}^n A
   \to
   \mathbf{B}^n A
   \stackrel{curv}{\to}
   \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A
  \to
  \mathbf{\flat} \mathbf{B}^{n+1} A
   \to
  \mathbf{B}^{n+1} A
$$

that [defines](#CurvatureCharacteristics) $curv$ (using that $\mathbf{\flat}$ preserves limits and hence looping and delooping)


=--

+-- {: .un_prop}
###### Proposition

The differential cohomology group $H_{diff}^n(X,A)$ fits into a [[short exact sequence]] of [[abelian group]]s

$$
  0 
   \to 
  H_{dR}^n(X,A)/H^{n-1}(X,A) 
   \to 
  H_{diff}^n(X,A) 
   \to 
  H^n(X,A)
   \to 
  0
  \,.
$$

=--


+-- {: .proof}
###### Proof

This is a general statement about the definition of [[twisted cohomology]].
We claim that for all $n \geq 1$ we have a [[fiber sequence]]

$$
  \mathbf{H}(X, \mathbf{B}^{n-1}A)
  \to 
  \mathbf{H}_{dR}(X, \mathbf{B}^n A)
  \to 
  \mathbf{H}_{diff}(X, \mathbf{B}^n A)
  \to
  \mathbf{H}(X, \mathbf{B}^n A)
$$

in [[∞Grpd]]. This implies the [[short exact sequence]] using that 
by construction the last morphism is surjective on connected components (because in the defining $(\infty,1)$-pullback for $\mathbf{H}_{diff}$ the right vertical morphism is by assumption surjective on connected components).

To see that we do have the fiber sequence as claimed consider the 
pasting composite of [[(∞,1)-pullback]]s

$$
  \array{
    \mathbf{H}_{dR}(X,\mathbf{B}^{n-1} A) 
    &\to& 
      \mathbf{H}_{diff}(X,\mathbf{B}^n A)  
    &\to& 
     H_{dR}(X, \mathbf{B}^{n+1} A)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    {*} 
      &\to& 
    \mathbf{H}(X, \mathbf{B}^n A) 
      &\stackrel{curv}{\to}&
    \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} A)
  }
  \,.
$$

The square on the right is a pullback by the above definition.
Since also the square on the left is assumed to be an $(\infty,1)$-pullback
it follows by the <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-pullback#QuasiCatPastingLaw">pasting law for (∞,1)-pullbacks</a> that the top left object is
the $(\infty,1)$-pullback of the total rectangle diagram. 
That total diagram is 

$$
  \array{
    \Omega \mathbf{H}(X, \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A) 
    &\to& 
     H(X,\mathbf{\flat}_{dR} \mathbf{B}^{n+1} A)
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^{n+1} A)
  }
  \,,
$$

because, as before, this $(\infty,1)$-pullback is the coproduct of the 
homotopy fibers, and they are empty over the connected components not
in the image of the bottom morphism and are the [[loop space object]]
over the single connected component that is in the image. 

Finally using that (as discussed at [[cohomology]] and at [[fiber sequence]]) 
$$
  \Omega \mathbf{H}(X,\mathbf{\flat}_{dR} \mathbf{B}^{n+1}A) 
    \simeq 
   \mathbf{H}(X,\Omega \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A)
$$ 

and

$$ 
  \Omega \mathbf{\flat}_{dR} \mathbf{B}^{n+1}A 
    \simeq 
   \mathbf{\flat}_{dR} \Omega \mathbf{B}^{n+1}A
$$

since both $\mathbf{H}(X,-)$ as well as $\mathbf{\flat}_{dR}$
preserve [[(∞,1)-limit]]s and hence formation of [[loop space object]]s,
the claim follows.


=--


+-- {: .un_remark}
###### Remark

This is essentially the short exact sequence whose form is familiar from the traditional definition of [[ordinary differential cohomology]] only up to the following slight nuances in notation:

1.  The cohomology groups of the short exact sequence above denote the groups obtained in the given [[(∞,1)-topos]] $\mathbf{H}$, not in [[Top]]. Notably for $\mathbf{H} = $ [[∞LieGrpd]], $A = U(1) =\mathbb{R}/\mathbb{Z}$
the [[circle group]] and $|X| \in Top$ the [[geometric realization]] of a paracompact manifold $X$, we have that $H^n(X,\mathbb{R}/\mathbb{Z})$ above is $H^{n+1}_{sing}({|\Pi X|},\mathbb{Z})$. 

1. The fact that on the left  of the short exact sequence for differential cohomology we have the de Rham cohomology set $H_{dR}^n(X,A)$ instead of 
something like the set of all flat forms as familiar from 
[[ordinary differential cohomology]] is because the latter has no
intrinsic meaning but depends on a choice of model. 
After fixing a specific
[[presentable (∞,1)-category|presentation]] of $\mathbf{H}$ 
by a [[model category]] $C$ we can
consider instead of 
$H_{dR}^{n+1}(X,A) \to \mathbf{H}_{dR}(X, \mathbf{B}^{n+1}A)$ 
the inclusion of the set of objects 
$\Omega_{cl}^{n+1}(X,A) {:=} \mathbb{R}Hom_C(X, \mathbf{B}^{n+1}A )_0
\hookrightarrow \mathbb{R}Hom_C(X, \mathbf{B}^{n+1}A )$. However,
by the [above observation](#DiffCohIsWellDefined) this 
only adds multiple copies of the homotopy types of the connected 
components of $\mathbf{H}_{diff}(X, \mathbf{B}^n A)$.

=--




### Chern-Weil homomorphism and $\infty$-connections {#ChernWeilTheory}

Induced by the [intrinsic differential cohomology](#DifferentialCohomology) in any [[∞-connected (∞,1)-topos|∞-connected]] and [[locally ∞-connected (∞,1)-topos]] is an intrinsic notion of [[Chern-Weil homomorphism]].

Let $A$ be the chosen abelian [[∞-group]] as [above](#DifferentialCohomology). Recall the [universal curvature characteristic class](#CurvatureCharacteristics)

$$
  curv : \mathbf{B}^n A \to \mathbf{\flat}_{dR}\mathbf{B}^{n+1}A
$$

for all $n \geq 1$.

+-- {: .un_def}
###### Definition


For $G$ an [[∞-group]] and 

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^n A
$$

a representative of a [[characteristic class]] $[\mathbf{c}] \in H^n(\mathbf{B}G, A)$ we say that the composite

$$
  \mathbf{c}_{dR} : \mathbf{B}G \stackrel{\mathbf{c}}{\to}
    \mathbf{B}^n A 
     \stackrel{curv}{\to}
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1} A
$$

represents the corresponding [[differential characteristic class]] or **[[curvature characteristic class]]** 
$[\mathbf{c}_{dR}] \in H_{dR}^{n+1}(\mathbf{B}G, A)$.

The induced map on cohomology

$$
  (\mathbf{c}_{dR})_* 
   : 
  H^1(-,G)
  \to
  H^{n+1}_{dR}(-,A)
$$

we call the (unrefined) **[[∞-Chern-Weil homomorphism]]** induced by $\mathbf{c}$.

=--

The following construction universally lifts the 
$\infty$-Chern-Weil homomorphism from taking values in 
[intrinsic de Rham cohomology](#deRhamCohomology) 
to values in [intrinsic differential cohomology](#DifferentialCohomology).


+-- {: .un_def}
###### Definition

For $X \in \mathbf{H}$ any object, define the [[∞-groupoid]] $\mathbf{H}_{conn}(X,\mathbf{B}G)$ as the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{H}_{conn}(X, \mathbf{B}G) 
     &\stackrel{(\hat \mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
     \mathbf{H}_{diff}(X,\mathbf{B}^{n_i} A)
   \\
   {}^{\mathllap{\eta}}\downarrow && \downarrow
   \\
   \mathbf{H}(X, \mathbf{B}G) 
     &\stackrel{( \mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
   \mathbf{H}(X,\mathbf{B}^{n_i} A)
  }
 \,.
$$

We say 

* a cocycle in $\nabla \in \mathbf{H}_{conn}(X, \mathbf{B}G)$ is an [[connection on an ∞-bundle|∞-connection]] 

* on the [[principal ∞-bundle]] $\eta(\nabla)$;

* a morphism in $\mathbf{H}_{conn}(X, \mathbf{B}G)$ is a [[gauge transformation]] of connections;

* for each $[\mathbf{c}] \n H^n(\mathbf{B}G, A)$ the morphism

  $$
    [\hat \mathbf{c}] :  H_{conn}(X,\mathbf{B}G) \to H_{diff}^n(X, A)
  $$

  is the (full/refined) **[[∞-Chern-Weil homomorphism]]** induced
  by the [[characteristic class]] $[\mathbf{c}]$.

=--

+-- {: .un_prop}
###### Observation

Under the [[curvature]] projection $[F] : H_{diff}^n (X,A) \to H_{dR}^{n+1}(X,A)$ the refined Chern-Weil homomorphism for $\mathbf{c}$ projects to the unrefined Chern-Weil homomorphism.

=--

+-- {: .proof}
###### Proof

This is due to the existence of the pasting composite

$$
  \array{
    \mathbf{H}_{conn}(X, \mathbf{B}G) 
     &\stackrel{(\hat \mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
     \mathbf{H}_{diff}(X,\mathbf{B}^{n_i} A)
    &\stackrel{[F]}{\to}&
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
     H_{dR}^{n_i+1}(X,A)
   \\
   {}^{\mathllap{\eta}}\downarrow && \downarrow && \downarrow
   \\
   \mathbf{H}(X, \mathbf{B}G) 
     &\stackrel{(\mathbf{c}_i)_i}{\to}& 
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
   \mathbf{H}(X,\mathbf{B}^{n_i} A)
    &\stackrel{curv_*}{\to}&
     \prod_{[\mathbf{c}_i] \in H^{n_i}(\mathbf{B}G,A); i \geq 1} 
    \mathbf{H}_{dR}(X, \mathbf{B}^{n_i+1},A)
  }
$$

of the defining $(\infty,1)$-pullback for $\mathbf{H}_{conn}(X,\mathbf{B}G)$ with the products of the defining
$(\infty,1)$-pullbacks for the $\mathbf{H}_{diff}(X, \mathbf{B}^{n_i}A)$.

=--


### Higher holonomy and Chern-Simons functional 
  {#ChernSimonsTheory}

The notion of [intrinsic ∞-connections](#ChernWeilTheory) in a 
cohesive $(\infty,1)$-topos induces a notion of [[higher parallel transport|higher holonomy]] and [[Chern-Simons theory|Chern-Simons functionals]].


+-- {: .un_prop}
###### Definition

We say an object $\Sigma \in \mathbf{H}$ has **[[cohomological dimension]]** $\leq n \in \mathbb{N}$ if for all $n$-[[connected]] coefficient objects  and $(n++1)$-[[truncated]] objects $\mathbf{B}^{n+1}A$ the corresponding cohomology on $\Sigma$ is trivial

$$
  H(\Sigma, \mathbf{B}^{n+1}A ) \simeq *
  \,.
$$

Let $dim(\Sigma)$ be the maximum $n$ for which this is true.

=--



+-- {: .un_prop}
###### Observation

If $\Sigma$ has [[cohomological dimension]] $\leq n$ then its  [intrinsic de Rham cohomology](#deRhamCohomology) vanishes in degree $k \gt n$

$$
  H_{dR}^{k \gt n}(\Sigma, A) \simeq *
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since $\mathbf{\flat}$ is a [[right adjoint]] it preserves [[delooping]] and hence $\mathbf{\flat} \mathbf{B}^k A \simeq \mathbf{B}^k \mathbf{\flat}A$. It follows that 

$$
  \begin{aligned}
     H_{dR}^{k}(\Sigma,A)
     & :=
     \pi_0 \mathbf{H}(\Sigma, \mathbf{\flat}_{dR} \mathbf{B}^k A)
    \\
    & \simeq
     \pi_0 \mathbf{H}(\Sigma, * \prod_{\mathbf{B}^k A} \mathbf{B}^k \mathbf{\flat}A)
    \\
    & \simeq
    \pi_0
     \left( 
     \mathbf{H}(\Sigma,*) \prod_{\mathbf{H}(\Sigma, \mathbf{B}^k A)}
      \mathbf{H}(\Sigma, \mathbf{B}^k \mathbf{\flat}A)
     \right)
   \\
   & \simeq
    \pi_0 (*)
  \end{aligned}
  \,.
$$

=--

Let now again $A$ be fixed as [above](#DifferentialCohomology).

+-- {: .un_def}
###### Definition

Let $\Sigma \in \mathbf{H}$, $n \in \mathbf{N}$ with
$dim \Sigma \leq n$. 
  
We say that the composite

$$
  \int_\Sigma 
  : 
  \mathbf{H}_{flat}(\Sigma, \mathbf{B}^n A)
   \stackrel{\simeq}{\to}
  \infty Gprd(\Pi(\Sigma), \Pi(\mathbf{B}^n A))
   \stackrel{\tau_{\leq n-dim(\Sigma)}}{\to}
  \tau_{n-dim(\Sigma)}
    \infty Gprd(\Pi(\Sigma), \Pi(\mathbf{B}^n A))
$$ 

of the [[adjunction]] equivalence followed by [[truncated|truncation]] is the **flat holonomy** operation on flat $\infty$-connections.

More generally, let

* $\nabla \in \mathbf{H}_{diff}(X, \mathbf{B}^n A)$ be a differential coycle on some $X \in \mathbf{H}$

* $\phi : \Sigma \to X$ a morphism.

Write

$$
  \phi^* : \mathbf{H}_{diff}(X, \mathbf{B}^{n+1} A) 
    \to 
  \mathbf{H}_{diff}(\Sigma, \mathbf{B}^n A)
   \simeq
  \mathbf{H}_{flat}(\Sigma, \mathbf{B}^n A)
$$

(using the [above proposition](#DiffCohomologyRestrictedToVanishingCurvature)) 
for the morphism on $(\infty,1)$-pullbacks induced by the morphism of diagrams

$$
  \array{  
     \mathbf{H}(X, \mathbf{B}^n A) &\to&
     \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} A)
     &\leftarrow&
     H_{dR}^{n+1}(X, A)
     \\
     \downarrow^{\mathrlap{\phi^*}}
     &&
     \downarrow^{\mathrlap{\phi^*}}
     &&
     \downarrow
     \\
     \mathbf{H}(\Sigma, \mathbf{B}^n A) &\to&
     \mathbf{H}_{dR}(X, \mathbf{B}^{n+1} A)
     &\leftarrow&
     *     
  }
$$


The **[[higher parallel transport|holonomomy]]** of $\nabla$ over $\sigma$ is the flat holonomy of $\phi^* \nabla$

$$
  \int_\phi \nabla := \int_{\Sigma} \phi^* \nabla
  \,.
$$ 

=--

+-- {: .un_def}
###### Definition

Let $\Sigma \in \mathbf{H}$ be of [[cohomological dimension]] $dim\Sigma = n \in \mathbb{N}$ and let $\mathbf{c} : X \to \mathbf{B}^n A$ a representative of a [[characteristic class]] $[\mathbf{c}] \in H^n(X, A)$ for some object $X$. We say that the composite

$$
  \exp(S_{\mathbf{c}}(-))
  : 
  \mathbf{H}(\Sigma, X)
   \stackrel{\hat \mathbf{c}}{\to}
  \mathbf{H}_{diff}(\Sigma, \mathbf{B}^n A)
   \stackrel{\simeq}{\to}
  \mathbf{H}_{flat}(\Sigma, \mathbf{B}^n A)
   \stackrel{\int_\Sigma}{\to}
  \tau_{\leq 0}
    \infty Grpd(\Pi(\Sigma), \Pi \mathbf{B}^n A)
$$

where $\hat \mathbf{c}$ denotes the [refined Chern-Weil homomorphism](#ChernWeilTheory) induced by $\mathbf{c}$,
is the **[[schreiber:∞-Chern-Simons theory|extended Chern-Simons functional]]** induced by $\mathbf{c}$ on $\Sigma$.

=--

+-- {: .un_def}
###### Remark

In the language of [[sigma-model]] [[quantum field theory]] the ingredients of this definition have the following interpretation

* $\Sigma$ is the _worldvolume of a fundamental $(dim\Sigma-1)$-[[brane]]_ ;

* $X$ is the target space;

* $\hat \mathbf{c}$ is the background [[gauge field]] on $X$;

* $\mathbf{H}_{conn}(\Sigma,X)$ is the space of _worldvolume field configurations_ $\phi : \Sigma \to X$ or _trajectories_ of the brane in $X$;

* $\exp(S_{\mathbf{c}}(\phi)) =  \int_\Sigma \phi^* \hat \mathbf{c}$ is the value of the [[action functional]] on the field configuration $\phi$.

=--

In suitable situations this construction refines to an internal construction.

Assume that $\mathbf{H}$ has a canonical [[line object]] $\mathbb{A}^1$ and a [[natural numbers object]] $\mathbb{Z}$. Then the [[action functional]] $\exp(i S(-))$ may lift to the [[internal hom]] with respect to the canonical <a href="http://ncatlab.org/nlab/show/(infinity,1)-topos#ClosedMonoidalStructure">cartesian closed monoidal structure</a> on any [[(∞,1)-topos]] to a morphism of the form

$$
  \exp(i S_{\mathbf{c}}(-)) : [\Sigma,\mathbf{B}G_{conn}] \to 
  \mathbf{B}^{n-dim \Sigma}\mathbb{A}^1/\mathbb{Z}
  \,.
$$

We call $[\Sigma, \mathbf{B}G_{conn}]$ the [[configuration space]] of the [[schreiber:∞-Chern-Simons theory]] defined by $\mathbf{c}$ and $\exp(i S_\mathbf{c}(-))$ the [[action functional]] in [[codimension]] 
$(n-dim\Sigma)$ defined on it. 

See [[schreiber:∞-Chern-Simons theory]] for more discussion.


## References

The [[category theory|category-theoretic]] definition of [[cohesive topos]] was proposed by [[Bill Lawvere]]. See the references at [[cohesive topos]].

The observation that the further left adjoint $\Pi$ in a [[locally ∞-connected (∞,1)-topos]] defines an intrinsic notion of paths and [[geometric homotopy groups in an (∞,1)-topos]] was suggested by [[Richard Williamson]].

The observation that the further right adjoint $coDisc$ in a [[local (∞,1)-topos]] serves to characterize [[concrete sheaf|concrete (∞,1)-sheaves]] was amplified by [[David Carchedi]].

Several aspects of the discussion here are, more or less explicitly, in 

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))
{#SimpsonTeleman}

For instance something similar to the notion of [[infinity-connected (infinity,1)-site|∞-connected site]] and the 
[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] is the content of section 2.16.  The [infinitesimal path ∞-groupoid adjunction](#LieTheory) $(\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})$ is essentially discussed in section 3. The notion of geometric realization, \ref{GeometricRealization}, is touched on around remark 2.22, referring to

* [[Carlos Simpson]], _The topological realization of a simplicial presheaf_ , [arXiv:q-alg/9609004](http://arxiv.org/abs/q-alg/9609004).
 {#Simpson} 

But, more or less explicitly, the presentation of geometric realization of simplicial presheaves is much older, going back to Artin-Mazur. See [[geometric homotopy groups in an (∞,1)-topos]] for a detailed commented list of literature.

A characterization of infinitesimal extensions and formal smoothness by adjoint functors (discussed at [[infinitesimal cohesion]]) is considered in 

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}

in the context of _[[Q-categories]]_ .

The material presented here is also in section 2 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ 

A commented list of further related references is at

* [[schreiber:differential cohomology in an (∞,1)-topos -- references
  |differential cohomology in a cohesive topos -- references]]




