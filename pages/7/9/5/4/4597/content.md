


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

* [[schreiber:differential cohomology in an (∞,1)-topos]]

* [[∞-Chern-Weil theory introduction]]

* **$\infty$-Chern-Weil theory**

***

#Contents#
* table of contents
{:toc}


## Motivation {#Motivation}

The central motivation for the study of a higher generalization of ordinary [[Chern-Weil theory]] is the interest in extending the [[Chern-Weil homomorphism]] for a given [[Lie group]] $G$ through the whole _smooth_ [[Whitehead tower]] of $G$, which involves not just [[Lie group]]s but [[∞-Lie group]]s. Such an extension constitutes a refined cohomological invariant, in that it computes the intrinsic $G$-Chern-character, in a way that we describe [below](#ChernCharacter). 

### Fractional differential classes

Since $\infty$-Chern Weil theory handles [[characteristic class]]es on [[classifying space]]s more general than $\mathcal{B}G$ for $G$ an ordinary [[Lie group]], it is concerned with refinements of characteristic classes, even before passing to their differential refinement. We give some examples of such _fractional characteristic classes_ .

It is a familiar classical fact that the first [[Pontryagin class]] 

$$
  p_1 : \mathcal{B}SO \to \mathcal{B}^4 \mathbb{Z}
  \,,
$$

which represents the generator of the fourth [[integral cohomology]] of the [[classifying space]] $\mathcal{B} SO$ of the [[special orthogonal group]] allows a division by 2 when pulled back one step along the [[Whitehead tower]] to the classifying space of the [[spin group]], in that there is a [[commuting diagram]]

$$
  \array{
     \mathcal{B} Spin &\stackrel{\frac{1}{2}p_1}{\to}& \mathcal{B}^4 \mathbb{Z}
     \\
     \downarrow && \downarrow^{\mathrlap{\cdot 2}}
     \\
     \mathcal{B} SO &\stackrel{p_1}{\to}& \mathcal{B}^4 \mathbb{Z}
  }
  \,,
$$

where the top horizonal morphism represents a generator of the 4th integral cohomology of the classifying space of the [[spin group]] and the right vertical morphism is induced by multiplication by 2 on the additive group of [[integer]]s.

This means that for $X$ [[manifold]] with [[spin structure]] exhibited by a classifying map $\hat g$

$$
  \array{
     && \mathcal{B} Spin &\stackrel{\frac{1}{2}p_1}{\to}& \mathcal{B}^4 \mathbb{Z}
     \\
     & {}^{\mathllap{\hat g}}\nearrow & \downarrow && \downarrow^{\mathrlap{\cdot 2}}
     \\
     X &\stackrel{g}{\to}& \mathcal{B} SO &\stackrel{p_1}{\to}& \mathcal{B}^4\mathbb{Z}
  }
$$

of its [[tangent bundle]] $T X$, the characteristc class $p_1(T X) : X \stackrel{g}{\to} \mathcal{B}SO \stackrel{p_1}{\to} \mathcal{B}^4 \mathbb{Z}$ of $T X$ regarded as an $SO$-[[associated bundle]] contains less information than the class $\frac{1}{2}p_1(T X) : X \stackrel{\hat g}{\to} \mathcal{B}Spin \stackrel{\frac{1}{2}p_1}{\to} \mathcal{B}^4 \mathbb{Z}$. For instance if the 4th cohomology of $X$ happens to be 2-[[torsion]], the former class entirely vanishes, while the latter need not.

This familiar situation poses no problem to classical [[Chern-Weil theory]], because both the [[special orthogonal group]] as well as the [[spin group]] of course have canonical structures of [[Lie group]]s, so that the [[Chern-Weil homomorphism]] may be applied to either.

But this is no longer the case as we keep climbing up the [[Whitehead tower]] of the [[orthogonal group]]. In the next step the second [[Pontryagin class]] $p_2 : \mathcal{B}SO \to \mathcal{B}^8 \mathbb{Z}$ may be divided by 6 when pulled back to the classifying space of the [[string group]] (<a href="http://ncatlab.org/schreiber/edit/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSII">SSSII</a>) 

$$
  \array{
     \mathcal{B} String &\stackrel{\frac{1}{6}p_2}{\to}& \mathcal{B}^8 \mathbb{Z}
     \\
     \downarrow && \downarrow^{\mathrlap{\cdot 6}}
     \\
     \mathcal{B} SO &\stackrel{p_2}{\to}& \mathcal{B}^8 \mathbb{Z}
  }
  \,,
$$

As before, this means that if a space $X$ admits a [[string structure]], then the characteristic class $p_2(X)$ contains less information than the fractional refinement $\frac{1}{6}p_2(X)$ that it admits. In particular, the former may vanish if for the degree 8 cohomology group of $X$ has 6-[[torsion]], while the latter need not vanish.

For purposes of ordinary cohomology this is no problem, but for the differential refinement by ordinary [[Chern-Weil theory]] it is: the [[string group]] does not admit a [[Lie group]] structure (necessarily not a finite dimensional one, and an infinite dimensional one is not known) and hence standard [[Chern-Weil theory]] cannot produce the differential refinement of the fractional class $\frac{1}{6}p_2$.

But $\infty$-Chern-Weil theory can: there is a natural smooth refinement of the [[string group]] to a [[Lie 2-group]]: the [[string 2-group]]. We write $\mathbf{B}String$ for the corresponding [[delooping]] [[∞-Lie groupoid]]. The fractional second Pontryagin class does lift to this smooth refinement to produce a [[characteristic class]]

$$
  \frac{1}{6}\mathbf{p}_2 : \mathbf{B}String \to \mathbf{B}^7 U(1)
$$

internal to $\mathbf{H} = $ [[?LieGrpd]]. Since this now lives in a smooth context, it does now have a differential Chern-Weil refinement

$$
  \frac{1}{6}\hat \mathbf{p}_2 : \mathbf{H}_{conn}(-, \mathbf{B}String)
  \to 
  \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
$$

that takes $String$-[[principal 2-bundle]]s with 2-connection to degree 8-cocycles in [[ordinary differential cohomology]]. 

This kind of refinement we discuss in a bit more detail in the next section.

### Higher differential string structures

The need to consider these refined differential invariants of fractional characteristic classes arose in the study of the [[differential cohomology]] of [[string theory]] backgrounds induced by [[quantum anomaly]]-cancellation: the [differential string- and fivebrane structures](#DiffStringStruc) which one encounters there as refining the ordinary [[string structure]]s and [[fivebrane structure]]s are the first steps of the extension from ordinary to higher Chern-Weil theory. For example the differential form data of a twisted differential string structure constitutes (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a>) what in the string theory literature is called the [[Green-Schwarz mechanism]]. While this still can and has been captured with tools of ordinary Chern-Weil theory and [[ordinary differential cohomology]], its natural simple formulation is only in higher Chern-Weil theory. Going beyond that, the magnetic dual Green-Schwarz mechanism can be seen to encode a _twisted differential fivebrane structure_ and this is not practical to be studied without some higher geometry.

 
The following restates this in a bit more technical detail.

For $G = Spin$ the [[spin group]], the first nontrivial [[characteristic class]] is the first fractional [[Pontryagin class]] given by a [[cocycle]] $\frac{1}{2}p_1 : \mathcal{B}G \to K(\mathbb{Z}, 4)$ in ordinary [[integral cohomology]] $H^4(\mathcal{B}Spin, \mathbb{Z})$. This induces a map

$$
  H^1(X, Spin) = H(X, \mathcal{B}Spin) \to H^4(X, \mathbb{Z})
$$

from isomorphism classes of topological $Spin$-[[principal bundle]]s to degree 4 integral cohomology.

If we assume that $X$ is a [[smooth manifold]] then we may consider the set

$$
Spin Bund(X)/ \sim = H(X,\mathbf{B}Spin)
$$

of [[isomorphism]]-classes of _smooth_ $Spin$-[[principal bundle]]s. Here and in all of the following, the boldface "$\mathbf{B}G$" indicates a refinement, here of the bare classifying space $\mathcal{B}G$ to a smooth incarnation.

Then ordinary [[Chern-Weil theory]] provides a refinement of the fractional Pontryagin class $H(X, \mathbf{B}Spin) \to H^4(X,\mathbb{Z})$ to a map to [[ordinary differential cohomology]] $H_{diff}^4(X)$

$$
  \frac{1}{2} \hat p_1 : H(X, \mathbf{B}Spin) \to H_{diff}^4(X)
  \,.
$$

The first point of passing to a [[higher category theory]]-refinement of this situation is that it allows to refine, in turn, these morphisms of cohomology _sets_ to morphisms

$$
  \frac{1}{2} \mathbf{p}_1 : \mathbf{H}(X, \mathbf{B}Spin) \to \mathbf{H}(X,\mathbf{B}^3 U(1))
$$

and

$$
  \frac{1}{2} \hat \mathbf{p}_1 : \mathbf{H}_{conn}(X, \mathbf{B}Spin) \to \mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))
$$

of [[cocycle]] [[∞-groupoid]]s: here $\mathbf{H}(X,\mathbf{B}G)$ is the [[groupoid]] whose objects are smooth $Spin$-[[principal bundle]]s, and whose morphisms are smooth homomorphisms between these. Similarly $\mathbf{H}(X,\mathbf{B}^3 U(1))$ denotes the [[3-groupoid] whose objects are smooth <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle 2-group</a>-[[principal ∞-bundles|principal 3-bundles]], while $\mathbf{H}_{diff}(X,\mathbf{B}^3 U(1))$ is accordingly the [[3-groupoid]] whose objects are  [[circle n-bundle with connection|circle 3-bundles with connection]], whose morphisms are homomorphisms between these, whose 2-morphisms are higher homotopies between those. The original morphism of cohomology sets is the [[decategorification]] of this, the restriction to connected components:

$$
  \frac{1}{2}p_1 = \pi_0(\frac{1}{2}\mathbf{p}_1)
  \,.
$$

This refinement to cocylce $\infty$-groupoids notably has the consequence that it allows us to produce the [[homotopy fiber]]s of these morphisms.  To see the relevance of this, recall (from _[[string structure]]_ ) that the [[homotopy fiber]] of the not differentially refined fractional Pontryagin class, whis is the [[(∞,1)-pullback]]

$$
  \array{
     \mathbf{H}(X,\mathbf{B}String) &\to& * 
     \\
     \downarrow &\swArrow_\simeq& \downarrow
     \\
     \mathbf{H}(X,\mathbf{B}G) 
     &\stackrel{\frac{1}{2} \mathbf{p}_1}{\to}&
     \mathbf{H}(X, \mathbf{B}^3 U(1))
  }
  \,,
$$

defines the $\infty$-groupoid $\mathbf{H}(X, \mathbf{B}String)$ of [[string structure]]s on $X$ ( _smooth_ , but not _differential_ ).

We can now replace in the the class $\frac{1}{2}\mathbf{p}_1$ by its differential refinement $\frac{1}{2}\hat \mathbf{p}_1$ and obtain an [[∞-groupoid]] $String_{diff}(X)$ that differentially refines the 2-groupoid $\mathbf{H}(X,\mathbf{B}String)$ of String-structures as the [[(∞,1)-pullback]]

$$
  \array{
     String_{diff}(X) &\to& * 
     \\
     \downarrow &\swArrow_\simeq& \downarrow
     \\
     \mathbf{H}_{conn}(X,\mathbf{B}G) 
     &\stackrel{\frac{1}{2}\hat \mathbf{p}_1}{\to}&
     \mathbf{H}_{diff}(X, \mathbf{B}^3 U(1))
  }
  \,.
$$

This $String_{diff}(X)$ we may callthe $\infty$-groupoid of _differential string-structures_ . A cocycle in there is naturally identified with a tuple consisting of

* a smooth $Spin$-[[principal bundle]] $P \to X$ with [[connection on a bundle|connection]] $\nabla$;

* the [[Chern-Simons 2-gerbe]] with connection $CS(\nabla)$ induced by this;

* a choice of trivialization of this Chern-Simons 2-gerbe -- this is the [[homotopy]] [[2-morphism]] in the middle of the above pullback diagram.

We may think of this as a refinement of [[secondary characteristic class]]es: the first Pontryagin [[curvature characteristic form]] $\langle F_\nabla \wedge F_\nabla \rangle$ itself is constrained to vanish, and so the [[Chern-Simons form]] 3-connection itself constitutes cohomological data.

So far this uses mostly just a little bit of [[(∞,1)-category theory]] or at least some [[homotopy theory]]. The first glimpse of something beyond ordinary [[Chern-Weil theory]] appearing is the $\infty$-groupoid $\mathbf{H}(X,\mathbf{B}String)$ which may be thought of as the [[2-groupoid]] of _smooth_ [[string 2-group]]-[[principal 2-bundle]]s.

But suppose we fix an $X$ such that $H(X, \mathbf{B}String)$ is nontrivial. Then we can continue the procees to higher degrees:

the next topological characteristic class is the second fractional [[Pontryagin class]] $\frac{1}{6}p_2 : \mathcal{B}String \to \mathcal{B}^7 U(1)$. Since the [[string group]] does not have the structure of a [[Lie group]], this cannot be refined to [[differential cohomology]] using ordinary [[Chern-Weil theory]]. However, in terms of $\infty$-Chern-Weil theory it can:

we may obtain a smooth refinement

$$
  \frac{1}{6}\hat \mathbf{p}_2 : \mathbf{H}_{conn}(-\mathbf{B}String) \to 
  \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
$$

that maps smooth [[string 2-group]]-[[principal 2-bundle]]s with 2-connectins to their [Chern-Simons circle 7-bundle with connection](#FivebraneStructure). This is an example of the higher version of the [[Chern-Weil homomorphism]]. 

And naturally we are then entitled to form its [[homotopy fiber]]s and produce the [[n-groupoid|7-groupoid]] of _[differential fivebrane structures](#DiffFivebraneStrucs)_ -- $Fivebrane_{diff}(X)$. For that recall again from [[fivebrane structure]] that the homotopy fiber of the smooth but non-differential cocycles

$$
  \array{
    \mathbf{H}(X, \mathbf{B}Fivebrane) &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow+
    \\
    \mathbf{H}(X, \mathbf{B}String) 
    &\stackrel{\frac{1}{6}\mathbf{p}_2}{\to}&
    \mathbf{H}(X, \mathbf{B}^7 U(1))
  }
$$

is the [[n-groupoid|7-groupoid]] of smooth [[fivebrane structure]]s on $X$. Its differential refinement

$$
  \array{
    Fivebrane_{diff}(X) &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow+
    \\
    \mathbf{H}_{conn}(X, \mathbf{B}String) 
    &\stackrel{\frac{1}{6}\hat \mathbf{p}_2}{\to}&
    \mathbf{H}_{diff}(X, \mathbf{B}^7 U(1))
  }
$$

we may therefore call the 7-groupoid $Fivebrane_{diff}(X)$ of _differential fivebrane structures_ . Cocycles in here are naturally identified with tuples of

* a $String$-[[principal 2-bundle]] $P \to X$, equipped with a [2-connection](#InfinityLieAlgebraConnection) $\nabla$;

* the Chern-Simons [[circle n-bundle with connection|circle 7-bundle]] $CS_7(\nabla)$ with connection induced by it;

* a choice of trivialization of $CS_7(\nabla)$.

These are the kinds of structures that naturally live in $\infty$-Chern-Weil theory. And this is only the second step in the [[Whitehead tower]] of the [[orthogonal group]]. There is an infinite tower of differential $(4k+1)$-brane structures above this, whose cocycles are given by $\infty$-connections on principal $\infty$-bundles and their corresponding Chern-Simons circle $n$-bundles with connection. 

These are the kind of structures that $\infty$-Chern-Weil theory studies.




## Idea

Ordinary [[Chern-Weil theory]] is about [[differential cohomology]]-refinements of [[characteristic class]]es of $G$-[[principal bundle]]s for $G$ a [[Lie group]], equivalently of the [[classifying space]] $\mathcal{B}G$ of that Lie group.

Under _$\infty$-Chern-Weil theory_ we want to understand the generalization of this to [[(∞,1)-category theory]]: where [[Lie group]]s are generalized to [[∞-Lie group]]s, [[Lie algebra]]s are generalized to [[∞-Lie algebra]]s and [[principal bundle]]s to [[principal ∞-bundle]]s.

So $\infty$-Chern-Weil theory produces [[differential cohomology]]-refinements of [[characteristic class]]es of $G$-[[principal ∞-bundle]]s for $G$ an [[∞-Lie group]], equivalently of the corresponding [[classifying space]]s $\mathcal{B}G$.

Ordinary Chern-Weil theory is formulated in the context of [[differential geometry]]. We need to widen this context somewhat in order that it can accomodate the relevant higher structures and so we place ourselves in the context of the [[(∞,1)-topos]] $\mathbf{H} = $ [[?LieGrpd]] of [[∞-Lie groupoids]].

In every $(\infty,1)$-topos that admits a notion of differential cohomology,  there is a general abstract notion of refinement of [[characteristic class]]es in [[cohomology]] to [[curvature characteristic forms|curvature characteristic classes]] in [[ordinary differential cohomology]]. 

The main construction in ∞-Chern-Weil theory is a concrete _model_ or _presentation_ of this abstract operation. This model is constructed in terms of [[Lie integration]] of objects in [[∞-Lie algebra cohomology]]. This construction is the higher analog of the [[Chern-Weil homomorphism]]. Its crucial intermediate step is the definition and construction of _$\infty$-connections_ on [[principal ∞-bundle]]s. 

This model itself is after all built on concrete familiar constructions in [[differential geometry]] and can be studied and appreciated in itself without recourse to the higher topos theory that we claim it provides a model for. The so inclined reader can ignore all the general abstract discussion in the following and concentrate on the concrete differential geometry. 

ere is how this entry here proceeds.

A warmup for the full theory that connects to classical constructions is given at

* [Introduction](#PreparatoryConcepts)

Then in 

* [∞-Chern-Weil theory](#ChernWeil)

we discuss the general definition of $\infty$-connections and of the Chern-Weil homomorphism and discuss some general properties. Then we turn to discussing

* [Examples](#Examples)


## Preparatory concepts {#PreparatoryConcepts}


General $\infty$-Chern-Weil theory, as described below, is naturally formulated in the context of [[(infinity,1)-topos]]-theory and some of its aspects can only be understood from that perspective.

However, unwinding the abstract higher topos theoretic concepts in terms of 1-categoriecal models yields concrete structures in familiar contexts of [[differential geometry]] that connect to various classical and familiar concepts. Since a full appreciation of the abstract formulation benefits from having a feeling for how these concrete models work out, the reader may at this point wish to look into some such basic aspects. These may be found behind the following link

* [[infinity-Chern-Weil theory -- preparatory concepts]].



## $\infty$-Chern-Weil theory {#ChernWeil}

For $G,A$ [[nLab:∞-group]]s in an [[nLab:∞-connected (∞,1)-topos]] $\mathbf{H}$ with [[nLab:delooping]]s $\mathbf{B}G$ and $\mathbf{B}A$, respectively, every [[nLab:characteristic class]] $c : \mathbf{B}G \to A$ serves to pull back the <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#GroupalCurvature">canonical intrinsic curvature form</a> $curv_A : A \to \mathbf{\flat}_{dR} \mathbf{B}A$ to an <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos#deRham">intrinsic differential form</a> $curv_A\circ c  : \mathbf{B}G \to \mathbf{\flat}_{dR} \mathbf{B}A$ on $\mathbf{B}G$. 

For $G$ an ordinary [[nLab:Lie group]] regarded naturally as an object in $\mathbf{H} = $ [[nLab:?LieGrpd]], we show that the ordinary [[nLab:Chern-Weil homomorphism]] for $G$-[[nLab:principal bundle]]s may be understood as a concrete _model_ for this simple abstract situation, which applies to those characteristic classes $c$ that happen to be in the image of the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#IntegrationOfCocycles">Lie intgeration of Lie algebra cocycles</a>.

More generally, this construction applies for $G$ an [[nLab:∞-Lie group]] with [[nLab:∞-Lie algebra]] $\mathfrak{g}$ and $c$ a characteristic class on $\mathbf{B}G$ that arises from Lie integration of a cocycle in the [[nLab:∞-Lie algebra cohomology]] of $\mathfrak{g}$.

The ordinary [[nLab:Chern-Weil homomorphism]] uses a [[nLab:connection on a bundle]] $\nabla$ as an intermediate tool for interpolating from a $G$-[[nLab:principal bundle]] to its curvature characteristic, represented by the [[nLab:curvature characteristic form]] $\langle F_\nabla \rangle$, where $F_\nabla$ is the [[nLab:curvature]] of $\nabla$ and $\langle - \rangle$ is an [[nLab:invariant polynomial]] on $\mathfrak{g}$. The choice of connection in this construction may be understood as providing a correspondence space in the following construction.

We know from the discussion of abelian differential cohomology [above](#AbGerbe) that the intrinsic morphism

$$
  \mathbf{B}^n \mathbb{R}/\mathbb{Z} \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}/\mathbb{Z}
$$

in $\mathbf{H} = \infty LieGrpd$ is modeled in $[CartSp^{op}, sSet]_{proj,cov}$ by the correspondence

$$
  \array{
     \mathbf{B}^n \mathbb{R}/\Gamma_{diff,simp} &\stackrel{curv}{\to}&
     \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}_{simp}
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{B}^n \mathbb{R}/\Gamma_{simp}
  }
  \,.
$$

If we write 

$$
  \exp(b^{n-1}\mathbb{R} \to inn(b^{n-1}\mathbb{R}))
  :
  \mathbf{cosk}_{n+1}(
  (U,[k])
  \mapsto
  \left\{
    \array{
      C^\infty(U)\otimes \Omega^\bullet(\Delta^k)
      &\leftarrow&
      CE(b^{n-1}\mathbb{R})
      \\
      \uparrow && \uparrow
      \\
      \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^n)
      &\leftarrow&
      W(b^{n-1}\mathbb{R})
    }
  \right\}
  )
$$

and so forth, then this correspondence is

$$
  \array{
     \exp(b^{n-1}\mathbb{R}\to inn(b^{n-1}\mathbb{R}))
     &\to&
     \exp(* \to b^n \mathbb{R})
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     \exp(b^{n-1}\mathbb{R}\to *)
  }
  \,.
$$

If now $\mathbf{B}G \to \mathbf{B}^n \mathbb{R}/\mathbb{Z}$ is modeled by the Lie integration of a cocycle $\mu$ on a Lie $k$-algebra

$$
  \mathbf{cosk}_{k+1} \exp(\mathfrak{g})
  \stackrel{\exp(\mu)}{\to}
  \exp(b^{n-1}\mathbb{R})/\Gamma
  =
  \exp(b^{n-1}\mathbb{R} \to *)/\Gamma
$$

for $k \geq n-1$, then the total intrinsic differential form $\mathbf{B}G \to \mathbf{B}^n \mathbb{R}/\Gamma \to \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}$ is modeled by the zig-zag of morphisms

$$
  \array{
     && \exp(b^{n-1}\mathbb{R}\to inn(b^{n-1}\mathbb{R}))
     &\to&
     \exp(* \to b^n \mathbb{R})
     \\
     && \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{cosk}_{k+1}\exp(\mathfrak{g})
     &\stackrel{\exp(\mu)}{\to}& 
     \exp(b^{n-1}\mathbb{R}\to *)
  }
$$

in $[CartSp^{op}, sSet]$. In order to compute with such zig-zags of morphisms, in particular in order to compute [[nLab:homotopy fiber]]s, it is helpful to complete this to a single correspondence. There is a fairly evident choice for the tip of this total corresponence, namely 

$$
  \mathbf{B}G_{diff}
  :=
  \mathbf{cosk}_{n+1} \exp(\mathfrak{g} \to inn(\mathfrak{g}))
  \,.
$$

It remains to complete the square and extend the [[nLab:∞-Lie algebra cohomology|∞-Lie algebra cocycle]] $\mu : \mathfrak{g} \to b^{n-1}\mathb{R}$ to a morphism $(\mathfrak{g} \to inn(\mathfrak{g})) \to (b^{n-1}\mathbb{R} \to inn(b^{n-1}\mathbb{R}))$. This is accomplished by an [[nLab:invariant polynomial]] 

$$
  \langle -\rangle_\mu
  :
  inn(\mathfrak{g}) \stackrel{(\langle - \rangle_\mu, cs_\mu)}{\to} 
  inn(b^{n-1}\mathbb{R})
  \to
  b^n \mathbb{R}
$$

which is in transgression with $\mu$, witnessed by the [[nLab:Chern-Simons form|Chern-Simons element]] $cs_\mu$. Using this, we obtain the total diagram

$$
  \array{
     \mathbf{cosk}_{k+1}\exp(\mathfrak{g} \to inn(\mathfrak{g}))
     &\stackrel{(\langle - \rangle_\mu, cs_\mu)}{\to}& 
     \exp(b^{n-1}\mathbb{R}\to inn(b^{n-1}\mathbb{R}))
     &\to&
     \exp(* \to b^n \mathbb{R})
     \\
     \downarrow^{\mathrlap{\simeq}}
     && \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{cosk}_{k+1}\exp(\mathrak{g})
     &\stackrel{\exp(\mu)}{\to}& 
     \exp(b^{n-1}\mathbb{R}\to *)
  }
  \,.
$$

By the fact that this commutes, we have that the correspondence

$$
  \left(
  \array{
    \mathbf{B}G_{diff,simp}
    &\to&
    \mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}_{simp}
    \\
    \downarrow
    \\
    \mathbf{B}G_{simp}
  }
  \right)
  \;\;
  :=
  \;\;
  \left( 
  \array{
    \mathbf{cosk}_{k+1}\exp(\mathfrak{g} \to inn(\mathfrak{g}))
    &\to&
    \exp(* \to b^n \mathbb{R})
    \\
    \downarrow
    \\
    \mathbf{cosk}_{k+1}\exp(\mathfrak{g} \to *)
  }
  \right)
$$

in $[CartSp^{op}, sSet]_{proj,cov}$ models the intrinsic curvature characteristic form $\mathbf{B}G \to \mathbf{\flat}_{dR} \mathbf{B}^{n+1} \mathbb{R}$.

We may identify cocycles with values in $\mathbf{B}G_{diff}$ as _(pseudo)-$\infty$-connections_ on the underlying $\mathbf{B}G$-cocycle. If their curvature is represented by a cocycle in $\mathbf{\flat}_{dR} \mathbf{B}^{n+1}\mathbb{R}$ which is given by a globally defined form, then these are _genuine_ $\infty$-connections. In either case, they serve as an intermediate step in computing the curvature characteristics.


### $\infty$-Lie algebra valued connections {#InfinityLieAlgebraConnection}

> The content of this section is at [[connection on an infinity-bundle]].

### Curvature characteristics {#InfChernWeil}


+-- {: .un_def }
###### Definition
**(Chern-Weil curvature characteristics)**

Let $\langle -\rangle : inn(\mathfrak{g}) \to b^{p} \mathbb{R}$ be an [[nLab:invariant polynomial]] on the [[nLab:∞-Lie algebra|Lie n-algebra]] $\mathfrak{g}$. Postcomposition with the corresponding diagram of dg-algebras

$$
  \array{
    CE(\mathfrak{g}) &\leftarrow& 0
    \\
    \uparrow && \uparrow
    \\
    W(\mathfrak{g}) &\stackrel{\langle -\rangle}{\leftarrow}&
    CE(b^p \mathbb{R})
  }
$$

induces a morphism of [[nLab:simplicial presheaves]]

$$
   \langle F_{(-)} \rangle
   :
  \mathbf{B}G_{diff} \to 
  \mathbf{cosk}_{n+1} \mathbf{\flat}_{dR} \mathbf{B}^{p+1}\mathbb{R}_{simp}
$$

into the $(n+1)$-[[nLab:simplicial skeleton|coskeleton]] of the model for the de Rham coefficient object $\mathbf{\flat}_{dR}\mathbf{B}^{p+1}\mathbb{R}$ discussed [above](#U1FromLieIntegration).

For $\nabla : \hat X \to \mathbf{B}G_{diff}$ a connection, we call the 
induced intrinsic de Rham cocycle

$$
  \langle F_\nabla \rangle : 
  \hat X \stackrel{\nabla}{\to}  
  \mathbf{B}G_{diff}
  \stackrel{\langle -\rangle}{\to}
  \mathbf{cosk}_{n+1} \mathbf{\flat}_{dR} \mathbf{B}^{p+1}\mathbb{R}_{simp} 
$$

the Chern-Weil [[nLab:curvature characteristic form]] of $\nabla$ with respect to $\langle -\rangle$. 


=--

+-- {: .un_lemma }
###### Lemma

For $\nabla : \hat X \to \mathbf{B}G_{conn} \hookrightarrow \mathbf{B}G_{diff}$ a genuine connection, the induced curvature characteristic forms are globally defined closed forms, in that their cocycle factors through the sheaf $\Omega^{p+1}_{cl}(-)$ of closed $(p+1)$-forms:

$$
  \array{
     && \mathbf{B}G_{conn} &\stackrel{\langle F_{(-)}\rangle}{\to}& \Omega^{p+1}_{cl}(-)
     \\
    & \nearrow & \downarrow && \downarrow
    \\
    \hat X &\stackrel{}{\to}&
    \mathbf{B}G_{diff} 
    &\stackrel{\langle F_{(-)}\rangle}{\to}&  
    \mathbf{cosk}_{n+1} \mathbf{\flat}_{dR} \mathbf{B}^{p+1} \mathbb{R}_{simp}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

for given $(U,[k])$ notice that $\langle F_{\nabla}\rangle(U,[k]) \in \Omega^\bullet(U\times \Delta^k)$ is closed and for $\nabla$ a genuine connection has no leg along $\Delta^k$: for $\partial_t$ a vector field along $\Delta^k$ we have $\iota_{\partial_t} \langle F_A\rangle = 0$. Therefore the [[nLab:Lie derivative]] along a vector $\partial_t$ along the simplex vanishes:

$$
  \mathcal{L}_t \langle F_A\rangle = d \iota_t \langle F_A\rangle +
  \iota_t d \langle F_A\rangle = 0  
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

As for the groupal case [above](#AbGerbesConnection), we hence find that the genuine $\infty$-connections are selected among all pseudo-connections as those whose curvature characteristic has a 0-[[nLab:truncated]] cocycle representative. 

=--

So a genuine $\infty$-Lie algebra valued connection is a cocycle with values in the $(n+1)$-coskeleton of the simplicial presheaf of diagrams, which over $U,[k]$ assigns the set of diagrams

$$
  \array{
    C^\infty(U \times \Delta k)_{vert}
    &\leftarrow&
    CE(\mathfrak{g})
    &&&
    cocycle\;for\;underlying\;G-principal\;\infty-bundle
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U)\otimes \Omega^\bullet(X)
    &\leftarrow&
    CE(inn(\mathfrak{g})) = W(\mathfrak{g})  
    &&&
    connection\;and\;curvature
    \\
    \uparrow && \uparrow
    \\
    \Omega^\bullet(U) &\leftarrow& inv(\mathfrak{g})
    &&&
    curvature\;characteristic\;forms
  }
  \,,
$$

(with $\Omega^\bullet(U \times \Delta^k)_{vert}$ the dg-algebra of [[vertical differential form]]s on the bundle $U \times \Delta^k \to U$), where the top morphism encodes the cocycle for the underlying $G = \tau_n\exp(\mathfrak{g})$-[[nLab:principal ∞-bundle]], where the middle morphism encodes the connection data and the bottom morphism the [[nLab:curvature characteristic form]]s.

Such $\infty$-Lie algebra valued connections were introduced in <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">SSSI</a> and further studied in <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a>.

+-- {: .un_prop}
###### Proposition
**(existence of $\infty$-connections)**

In $\mathbf{H} = $ [[nLab:?LieGrpd]] over a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] $X$, every $G$-[[nLab:principal ∞-bundle]] for $G = \tau_n \exp(\mathfrak{g})$ obtained from [[nLab:Lie integration]] admits a genuine $\infty$-connection.

=--

+-- {: .proof}
###### Proof

By the assumptions on $X$, there is a [[nLab:good open cover]] $\{U_i \to X\}$ and a [[nLab:partition of unity]] $(\rho_i \in C^\infty(U_i))$ subordinate to that cover. 

Let $C(\{U_i\})$ be the [[nLab:Cech nerve]] of the cover and let $g : C(\{U_i\}) \to cosk_{n+1} \exp(\mathfrak{g})$ be a cocycle for the given $G$-principal $\infty$-bundle on $X$. This is given by a collection of [[schreiber:∞-Lie algebroid valued differential forms|∞-Lie algebra valued differential forms]]

$$
  ( C^\infty(U_{i_0, \cdots i_k})\otimes \Omega^\bullet(\Delta^k) 
  \leftarrow
  CE(\mathfrak{g}) : \lambda_{i_0, \cdots, i_n})
  \,.
$$

We need to extend these to a cocycle of differential forms

$$
  ( \Omega^\bullet(U_{i_0, \cdots i_k})\otimes \Omega^\bullet(\Delta^k) 
  \leftarrow
  W(\mathfrak{g}) : (\lambda_{i_0, \cdots, i_n},A_{i_0, \cdots, i_n})) 
$$

such that the curvature components have no leg along the simplices.  This constraint is hierarchy of systems of partial differential equations. consider first the $A_{i_0, \cdots, i_k}(\frac{\partial}{\partial u}, \{\frac{\partial}{\partial t_r}\})$ with exactly one leg along $U_{i_0, \cdots, i_k}$. For these the constraint is a system of differential equations of the schematic form


$$
  \frac{\partial}{\partial t_r} A
  =
  d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), A]
$$

By the [[nLab:Bianchi identity]] and the fact that the curvature with all components along the simplex vabishes, it follows that this is an integrable system of partial differential equations. Fixing the boundary condition that $A$ vanishes in the $0$-corner of $\Delta^k$, this has a unique solution. $\hat A_{i_0, \cdots, i_k}$.

Set then 

$$
  A_{i_1, \cdots, i_k} := \sum_{i_0} \rho_{i_0} \hat A_{i_0, \cdots, i_k}|_{\delta_0(\Delta^k)}
  \,.
$$


The system of differential forms obtained this way does satisfy the cocycle condition and the curvature component with one leg along $U$ and the other legs along the simplices vanish:

$$
  \frac{\partial}{\partial t_r} 
  A_{i_1, \cdots, i_k}
  =
  \frac{\partial}{\partial t_r} 
\sum_{i_0} \rho_{i_0}  \hat A_{i_0, \cdots, i_k}
  =
  \sum_{i_0} \rho_{i_0} d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), \sum_{i_0} \rho_{i_0} \hat A_{i_0, \cdots, i_k}]
  =
  d_U \lambda(\frac{\partial}{\partial t_r})
  + 
  [\lambda(\frac{\partial}{\partial t_r}), A_{i_1, \cdots, i_k}]
  \,.
$$

Next continue iteratively in the above fashion, by induction on the number of legs of the forms along $U$.

=--

We will now use this existence of $\infty$-connections to make a statement on principal $\infty$-bundles without connection that generalizes the following familiar construction: for ordinary principal bundles $P \to X$ we can explicitly construct a local trivialization by choosing a connection $\nabla$ on $P$, choosing for each patch $\{U_i \to X\}$ of a good open cover a smooth contraction $f : U_i \times [0,1] \to U_i$ and then using the parallel transport of the connection along the paths $f(x,-) : [0,1] \to U_i$ from $x$ to a fixed base point $x_0$ to identify all fibers of $P$ over $U_i$ with the fiber $P_{x_0}$.



### Higher order Chern-Simons forms

See at [[Chern-Simons form]] the section <a href="http://ncatlab.org/nlab/show/Chern-Simons+form#HigherOrderChernSimonsForms">In ∞-Chern-Weil theory</a>.



### Chern character {#ChernCharacter}


Above we have considered [∞-Lie algebra valued connections](#InfinityLieAlgebraConnection) and their [curvature characteristic forms](#InfChernWeil). We now wish to show how these model the intrinsic [[schreiber:Chern character in an (∞,1)-topos]].

$$
  ch_{\mathbf{B}G} : \mathbf{B}G \to \mathbf{\Pi}(\mathbf{B}G) \to \mathbf{\Pi}(\mathbf{B}G)\otimes R
  \,.
$$

Since our ambient [[nLab:(∞,1)-topos]] is assumed to be [[nLab:locally ∞-connected (∞,1)-topos|locally ∞-connected]] we have in addition to the notion of [[nLab:Postnikov tower in an (∞,1)-category]] the notion of [[nLab:Whitehead tower in an (∞,1)-topos]]. Both notions are dual to each other: for $A \in \mathbf{H}$ any object and 

$$
  \mathbf{\Pi}(A)
  \to
  \cdots
  \to
  \tau_{\leq 2}\mathbf{\Pi}(A)
  \to 
  \tau_{\leq 1}\mathbf{\Pi}(A)
  \to \tau_{\leq 0}\mathbf{\Pi}(A)
  = *
$$

the [[nLab:Postnikov tower in an (∞,1)-category|intrinsic Postnikov tower]] of its [[path ∞-groupoid]], the [[nLab:pasting]] composite of [[nLab:(∞,1)-pullback]]s 

$$
  \array{
    \vdots && && && \vdots
    \\
    \downarrow && && && \downarrow
    \\
    A_2 && &\to& \cdots &\to& \mathbf{B}\mathbf{\pi}_3(A) &\to& *
    \\
    \downarrow && && && && \downarrow
    \\
    A_1 && &\to& \cdots && && \mathbf{B}\mathbf{\pi}_2(A) &\to& *
    \\
    \downarrow
    && && && && \downarrow  && \downarrow
    \\
    A
    &\to&
    \mathbf{\Pi}A
    &\to& 
    \cdots
    &\to& 
    \tau_{\leq 3} \mathbf{\Pi}A
    &\to& 
    \tau_{\leq 2} \mathbf{\Pi}A
    &\to& 
    \tau_{\leq 1} \mathbf{\Pi}A
  }
  \,,
$$


defines the [[nLab:Whitehead tower in an (∞,1)-topos|Whitehead tower]] 

$$  
  * \to \cdots \to A_3 \to A_2 \to A_1 \to A_0 = A
$$

of $A$.



Since our $\mathbf{H}$ is assumed to be even [[nLab:∞-connected (∞,1)-topos|∞-connected]], the Postnikov tower of $\mathbf{\Pi}(A)$ is the image under $LConst : \infty Grpd \to \mathbf{H}$ of the ordinary [[nLab:Postnikov tower]] of $\Pi(A)$ in $\infty Grpd$. Accordingly, we have $\mathbf{B} \mathbf{\pi}_n(A) = LConst B^n \pi_n \Pi(A)$

The point now is that in $\mathbf{H} = $ [[nLab:?LieGrpd]] we may form smooh refinements of these discrete extensions: every discrete $(n+1)$-group $\mathbf{B}^{n+1}\mathbb{Z}$ we want to refine to a smooth $n$-group $\mathbf{B}^n U(1)$. By the discussion at <a href="http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#GeomReal">geometric realization</a>, both have equivalent underlying $\infty$-groupoids

$$
  \Pi(\mathbf{B}^{n+1}\mathbb{Z}) \simeq \Pi(\mathbf{B}^n U(1))
  \simeq
   K(\mathbb{Z},n+1)
  \,.
$$ 

For every direct summand abelian group $\mathbb{Z}$ in one of the $\mathbf{\pi}_n(A)$ we can ask for a refinement of the cocycle from coefficients $\mathbf{B}^n \mathbb{Z}$ to $\mathbf{B}^{n-1}\mathbb{R}/\mathbb{Z}$. This does not change the geometric realization, up to equivalence, but does change the smooth structure. And it allows to refine to differential coefficients by postcomposing further with
$curv : \mathbf{B}^{n-1}\mathbb{R}/\mathbb{Z} \to
 \mathbf{\flat}_{dR}\mathbf{B}^{n}\mathbb{R}$.

For instance for $A = \mathbf{B}Spin \in \mathbf{H} = \infty Lie Grpd$ the [[nLab:delooping]] of the [[nLab:spin group]], we refine the internal Whitehead tower to 

$$
  \array{
    \vdots
    \\
    \mathbf{B}Fivebrane &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{B}String &\to& \mathbf{B}^7 U(1) &\to& *
    \\
    \downarrow && \downarrow &&  \downarrow  
    \\
    \mathbf{B}Spin &\to& \cdots &\to& \mathbf{B}^3 U(1)
  }
  \,,
$$

where the deloopings of the [[nLab:string 2-group]] and the [[nLab:fivebrane 6-group]] appear.

The result of such a smooth refinement is that we may apply the intrinsic curvature classes and the intrinsic de Rham theorem to obtain cocycles in realified cohomology, for instance 

$$
  \mathbf{B}Spin    
  \to
  \mathbf{B}^3 U(1)
  \stackrel{curv}{\to}
  \mathbf{\flat}_{dR} \mathbf{B}^4 U(1)
  =
  \mathbf{\flat}_{dR} \mathbf{B}^4 \mathbb{R}
  \,.
$$

If we have a $Spin$-principal bundle $X \to \mathbf{B}G$, we may form over it the covering circle $n$-group bundles on which these higher cocycles naturally live

$$
  \array{
    P_2 &\to& \mathbf{B}Fivebrane &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    P_1 &\to& \mathbf{B}String &\to& \mathbf{B}^7 U(1) &\to& *
    \\
    \downarrow && \downarrow &&  && \downarrow  
    \\
    X &\to& \mathbf{B}Spin &\to& \cdots &\to& \mathbf{B}^3 U(1)
  }
  \,.
$$

Here for $X$ an ordinary space, $X = \tau_0 X$, the higher circle $n$-group principal bundes $P_k$ have the property that also $\tau_0 P_k = X$. Therefore the 0-truncation of the entire composite

$$
  P_1 \to \mathbf{B}^7 U(1) \to \mathbf{\flat}_{dR}\mathbf{B}^8 \mathbb{R}
$$

defines a closed 8-form on $X$. This is the curvature characeristic form given by the Chern-Weil homomorphism in this degree. Its refinement to Deligne cohomology in this construction lives naturally not on $X$, but on the covering $P_1$ of $X$.


(...)















## Examples {#Examples}


### Principal 1-bundles with connection

We spell out here how the general theory of [∞-Lie algebra valued connection](#InfinityLieAlgebraConnection) reduces to the standard notion of [[nLab:connection on a bundle|connections]] on ordinary $G$-[[nLab:principal bundle]]s and how the [∞-Chern-Weil homomorphism](#InfChernWeil) reduces on these to the ordinary [[nLab:Chern-Weil homomorphism]].

Let $\mathfrak{g}$ be a (finite dimensional) [[nLab:Lie algebra]]. Then

$$
  \mathbf{cosk}_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G
$$

is the [[nLab:delooping]] of the simply connected [[nLab:Lie group]] $G$ integrating $\mathfrak{g}$.


+-- {: .un_prop }
###### Proposition

The coefficient object $\mathbf{B}G_{conn}$ of [genuine ∞-Lie algebra connections](#InfinityLieAlgebraConnection) for $\mathfrak{g}$ an ordinary [[nLab:Lie algebra]] is weakly equivalent to the simplicial presheaf

$$
  \mathbf{B}G_{conn}
  \stackrel{\simeq}{\to}
  \Xi[G\times \Omega^1(-,\mathfrak{g}) \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1 d p_1^{-1}}{\to}}{\underset{p_2}{\to}} \Omega^1(-,\mathfrak{g})]
$$

that assigns objectwise the [[nLab:groupoid of Lie-algebra valued 1-forms]].

This is moreover isomorphic to the simplicial presheaf

$$
  \cdots = 
  [CartSp^{op},sSet](\mathbf{P}_1(-),\mathbf{B}G])
$$

of morphisms out of the [[nLab:path groupoid]].

The flat coefficient object $\mathbf{\flat}\mathbf{B}G$ is modeled by the subobject

$$
  \Xi[G\times \Omega^1_{flat}(-,\mathfrak{g}) \stackrel{
   \overset{Ad_{p_1}(p_2)+ p_1 d p_1^{-1}}{\to}}{\underset{p_2}{\to}} \Omega^1_{flat}(-,\mathfrak{g})]
$$

of groupoids of Lie-algebra valued forms with vanishing [[nLab:curvature]] 2-form.

This is isomorphic to 

$$
  \cdots = 
  [CartSp^{op},sSet](\mathbf{\Pi}_1(-),\mathbf{B}G])
$$

of morphism out of the [[nLab:fundamental groupoid]].

=--


+-- {: .proof}
###### Proof

The statements about morphisms out of the path groupoid are discussed in detail in [SchrWalI](http://arxiv.org/abs/0705.0452).

=--

+-- {: .un_cor }
###### Corollary

For $X$ a [[nLab:paracompact space|paracompact]] [[nLab:smooth manifold]] and $\{U_i \to X\}$ a [[nLab:good open cover]] we have a natural equivalence of groupoids

$$
  [CartSp^{op}, sSet](C(\{U_i\}), \mathbf{B}G_{conn})
  \simeq
  G Bund_\nabla(X)
$$

with the groupoid of smooth $G$-principal bundles with connection on $G$. 

For $\langle - \rangle : inn(\mathfrak{g}) \to b^p \mathbb{R}$ an [[nLab:invariant polynomial]] on $\mathfrak{g}$, the [induced morphism](#InfChernWeil)

$$
  [CartSp^{op}, sSet](C(\U_i\}), \mathbf{B}G_{diff})
  \stackrel{\langle F_{(-)}\rangle}{\to}
  \Omega^{p+1}_{cl}(X)
$$

is that of the ordinary [[nLab:Chern-Weil homomorphism]].

=--

We have seen that a refinement of the Chern-Weil homomorphism is available. The above morphism extends to a morphism

$$
  \langle F_{(-)}\rangle :  \mathbf{H}(-, \mathbf{B}G)
  \to 
  \mathbf{H}(-,
    \tau_{1} \mathbf{\flat}_{dR}\mathbf{B}^{p+1} \mathbb{R}
  )
$$

in $\mathbf{H} = \infty LieGrpd$ represented by

$$
 \array{
  [CartSp^{op},sSet](-, \mathbf{B}G_{diff})
  &\to&
  [CartSp^{op},sSet](-, \mathbf{cosk}_2 \mathbf{\flat}_{dR}\mathbf{B}^{p+1} \mathbb{R})
  \\
  \downarrow^{\simeq}
  \\
  [CartSp^{op},sSet](-, \mathbf{B}G)
  }
  \,.
$$

For $X$ a smooth manifold with good cover $\{U_i \to X\}$ we have that 
$ [CartSp^{op},sSet](C\{U_i\}, \mathbf{cosk}_2 \mathbf{\flat}_{dR}\mathbf{B}^{p+1} \mathbb{R})$ is the groupoid whose objects are closed $p+1$-forms on $X$ and whose morphisms are given by $p$-forms modulo exact forms.

Let $i \in I$ range over a set of generators for all [[nLab:invariant polynomial]]s. Then 

$$
  \mathbf{H}(-,\mathbf{B}G)
  \to 
  \prod_i \tau_1\mathbf{\flat}_{dR}\mathbf{B}^{n_i} \mathbb{R}
$$

is an approximation to the intrinsic Chern-character. We may consider its [[nLab:homotopy fiber]]s over a given set $Q_i$ of curvature characteristic forms.

Assume $\nabla, \nabla' : C(\{U_i\}) \to \mathbf{B}G_{diff}$ are two genuine connections with coinciding curvature characteristic classes $\{Q_i\}$. Then in the homotopy fiber they are coboundant cocycles precisely if all the [[nLab:Chern-Simons form]]s $CS_i(\nabla,\nabla')$ vanish modulo an exact form.

This equivalence relation is that which defines [[nLab:Simons-Sullivan structured bundle]]s. Their [[nLab:Grothendieck group]] completion yields [[nLab:differential K-theory]].


### Principal 2-bundles with connection

(...)

Let $\mathfrak{g}$ be a Lie [[nLab:strict 2-group]] coming from a [[nLab:differential crossed module]] $(\mathfrak{g}_2 \to \mathfrak{g}_1)$. Then we have two candidate Lie 2-groups integrating this: on the one hand the [[nLab:strict 2-group]] coming from the [[nLab:crossed module]] $(G_2 \to G_1)$ that integrates $(\mathfrak{g}_2 \to\mathfrak{g}_1)$ degreewise as ordinary Lie algebras, and on the other hand $cosk_k\exp(\mathfrak{g})$.

+-- {: .un_prop }
###### Proposition

The morphism

$$
  \tau_2 \exp(\mathfrak{g}) \to 
  \mathbf{B}(G_2 \to G_1)
$$

given by evaluating 2-dimensional [[nLab:parallel transport]] is a weak equivalence.
=--

+-- {: .proof}
###### Proof


Use the 3-dimensional nonabelian Stokes theorem from the appendix of [SchrWalII](http://arxiv.org/abs/0802.0663).

=--

+-- {: .un_cor }
###### Corollary

The object $\mathbf{B}(G_2 \to G_1)_{conn}$ assigns to $U \in CartSp$ the [[nLab:2-groupoid of Lie 2-algebra valued forms]] over $U$.

=--

This is described in detail in [SchrWalII](http://arxiv.org/abs/0802.0663), subject to the extra constraint that the 2-form curvature vanishes.


+-- {: .un_cor }
###### Corollary

A genuine connection on a $(G_2 \to G_1)$-[[nLab:principal 2-bundle]] with given cocycle $X \stackrel{\simeq}{\leftarrow} C(\{U_i\}) \to \mathbf{B}(G_2 \to G_1)$ is a cocycle $X \stackrel{\simeq}{\leftarrow} C(\{U_i\}) \to \mathbf{B}(G_2 \to G_1)_{conn}$ given as follows:

1. on $U_i$ a pair of forms $A_i \in \Omega^1(U_i, \mathfrak{g}_1)$, $B_i \in \Omega^2(U_i, \mathfrak{g}_2)$;

1 on $U_i \cap U_j$ a function $g_{i j} \in C^\infty(U_{i}\cap U_j , G_1)$ and a 1-form $a_{i j} \in \Omega^1(U_i \cap U_j, \mathfrak{g}_2)$ such that ...

1. and so forth
   

=--

This is described in detail in [SchrWalIII](), subject to the extra constraint that the 2-form curvature vanishes.

(...)




### Twisted differential $String-$ and $Fivebrane$-structures {#DiffStringStruc}

We discuss now in detail refined Chern-Weil morphisms

$$
  \hat \mathbf{c}
  :
  \mathbf{H}_{conn}(X,\mathbf{B}G)
  \to 
  \mathbf{H}_{diff}(X, \mathbf{B}^n U(1))
$$

that send [∞-connections](#InfinityLieAlgebraConnection) on $G$-[[principal ∞-bundle]]s to [[circle n-bundles with connection]] that represent a given [[characteristic class]]. $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ with coefficients in the [circle n-groupoid](#http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1). 

Specifically, we consider the first two steps in the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#SmoothWhitehead">smooth refinement of the Whitehead tower</a> of the [[orthogonal group]] $O$ that are controled by [[∞-Lie algebra cohomology]].

The smooth Whitehead tower of $O$ in [[?LieGrpd]] starts as 

$$
  \cdots \to \mathbf{B}Spin \to \mathbf{B} SO \to \mathbf{B}O
  \,,
$$

where

* the [[delooping]] $\mathbf{B} SO$ of the [[special orthogonal group]] is the $\mathbb{Z}_2$-[[principal bundle]] over $\mathbf{B}O$ classified by the [[cocycle]] $\mathbf{B}O \to \mathbf{B} \mathbb{Z}_2$ that sends an elemen $k \in O$ to $+1$ if it is in the connected component of the identity and to $-1$ if it is not. This means we have an [[(∞,1)-pullback]] diagram

  $$
    \array{
      \mathbf{B} SO &\to& * 
      \\
      \downarrow && \downarrow
      \\
      \mathbf{B} O &\stackrel{\mathbf{w}_1}{\to}& \mathbf{B} \mathbb{Z}_2
    }
    \;
  $$

* the [[delooping]] $\mathbf{B} Spin$ of the [[spin group]] is the is the $\mathbf{B}\mathbb{Z}_2$-[[principal 2-bundle]] over $\mathbf{B} SO$ classified by the [[Stiefel-Whitney class]] $\mathbf{B} SO \to \mathbf{B}^2 \mathbb{Z}$

  $$
    \array{
      \mathbf{B} Spin &\to& * 
      \\
      \downarrow && \downarrow
      \\
      \mathbf{B} SO &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
    }
    \;
  $$

Since these two steps are controled by the [[torsion]]-group $\mathbb{Z}_2$ they have no nontrivial refinement to differential cohomology. The next step however is controled by what in the [[(∞,1)-topos]] [[∞Grpd]] $\simeq$ [[Top]] is the first [[fractional Pontryagin class]] $\frac{1}{2}p_1 : \mathcal{B} Spin \to \mathcal{B}^4 \mathbb{Z}$ and which lifts through the [[schreiber:path ∞-groupoid]] functor $\Pi : \infty LieGrpd \to \infty Grpd$ to a characteristic class in $\mathbf{H} = $ [[?LieGrpd]] (as discussed there) $\frac{1}{2} p_1 : \mathbf{B} Spin \to \mathbf{B}^3 U(1)$ with coefficients in the smooth <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle 3-groupoid</a>. This cocycle does arise as the [[Lie integration]] $\exp(\mu)$ of the canonical [[Lie algebra cohomology|Lie algebra 3-cocycle]] $\mu = \langle -,[-,-]\rangle: \mathfrak{so} \to b^2 \mathbb{R}$.

The [[principal ∞-bundle|principal 3-bundle]] that this classifies is the [[delooping]] $\mathbf{B} String$ of the [[string 2-group]] $String$

$$
  \array{
    \mathbf{B} String &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B} Spin &\stackrel{\frac{1}{2}\mathbf{p}_1}{\to}& \mathbf{B}^3 U(1)
  }
  \,.
$$

Notice that the fact that this is an [[(∞,1)-pullback]] implies that for any $X\in \mathbf{H} = \infty LieGrpd$ also

$$
  \array{
    \mathbf{H}(X,\mathbf{B} String) &\to& * 
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}(X,\mathbf{B} Spin) &\to& \mathbf{H}(X,\mathbf{B}^3 U(1))
  }
  \,,
$$

which exhibits the [[2-groupoid]] $\mathbf{H}(X,\mathbf{B}String)$ of  [[string structure]]s.

As we refine in this diagram the bottom morphism to differential cohomology, we obtain correspondingly differential string structures.


#### The string-lifting Chern--Simons $3$-bundle with connection {#StringStructure}

We describe the special case of the general [$\infty$-Chern--Weil homomorphism](#InfChernWeil) for [$\infty$-Lie algebra valued connections](#InfinityLieAlgebraConnection) corresponding to the [[characteristic class]] $\frac{1}{2}p_1\colon \mathbf{B}Spin \to \mathbf{B}^3 U(1)$: the first fractional [[Pontryagin class]] of the [[spin group]] $\mathbf{B}Spin$. The $\mathbf{B}^3 U(1)$-differential cocycle that it produces from a given $Spin$-[[principal bundle]]
is the [[Chern-Simons 2-gerbe|Chern?Simons 2-bundle]] with connection whose class is the obstruction for the existence of a [[string structure]].

The content of this subsection is at [[Chern-Simons 2-gerbe|Chern?Simons 2-gerbe]] in [the section on $\infty$-Chern--Weil theory](Chern-Simons+2-gerbe#InInfChernWeil).


#### Differential string structures

The content of this section is at [[differential string structure]].

#### The Fivebrane-lifting Chern-Simons 6-bundle with connection {#FivebraneStructure}


We show now that the Lie integration of the differential $\infty$-Lie algebra cocycle corresponding to the degree 7 cocycle on the [[nLab:string Lie 2-algebra]] $\mathfrak{string}$

$$
  \exp(\mathfrak{string} \to inn(\mathfrak{string}))/\sim
  \stackrel{\exp(\mu_7, P_8)}{\to}
  \exp(b^6 \mathbb{R} \to inn(b^6 \mathbb{R})/\sim
  \to
  \mathbf{B}^7 U(1)_{diff}
$$

is a model for the differential refinement of the second fractional Pontryagin class

$$
  \frac{1}{6}p_2
  : 
  \mathbf{H}_{conn}(-, \mathbf{B}String)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^7 U(1))
  \,.
$$

The discussion is entirely analogous to the discussion of the differential refinekent of the first fractional Pontryagin class [above](#StringStructure).

(...)

#### Differential fivebrane structures {#DiffFivebraneStrucs}

Let 

$$
  \frac{1}{6}\hat p_2 : 
  \mathbf{H}_{conn}(-,\mathbf{B}String)
  \to
  \mathbf{H}_{diff}(-, \mathbf{B}^7 U(1))
$$

be the differential refinement of the second fractional Pontryagin class discussed [above](#FivebraneStructure).


**Definition** 

For $X \in \mathbf{H} =$ [[nLab:?LieGrpd]], the $\infty$-groupoid  of **differential fivebrane-structures** $Fivebrane_{diff}(X)$ is the [[nLab:homotopy fiber]] of    $\frac{1}{6}p_2(X) : \mathbf{H}(X,\mathbf{B}String) \to \mathbf{H}_{diff}(X, \mathbf{B}^7 U(1))$.

More generally, the $\infty$-groupoid of **twisted differential fivebrane structures** is the [[nLab:(∞,1)-pullback]] $Fivebrane_{diff,tw}(X)$ in

$$
  \array{
    Fivebrane_{diff,tw}(X) &\to& H_{diff}(X,\mathbf{B}^7 U(1))
    \\
    \downarrow && \downarrow
    \\
    \mathbf{H}_{conn}(X,\mathbf{B}String)
    &\stackrel{\frac{1}{6}\hat p_2}{\to}&
    \mathbf{H}_{diff}(X,\mathbf{B}^7 U(1))
  }
  \,.
$$

In terms of the underlying $\infty$-Lie algebra valued local connection data, i.e. before Lie integration in the above sense , this has been considered in <a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSIII">SSSIII</a>

(...)

***

## References

The $\infty$-Lie algebraic data involved in the $\infty$-Chern-Weil homomorphism was considered in

* SSSI (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)
{#SSSI}

An more comprehensive context is described at

* [[schreiber:differential cohomology in an (∞,1)-topos]]

[[!redirects ∞-Chern-Weil theory]]

[[!redirects ∞-Chern-Weil homomorphism]]


