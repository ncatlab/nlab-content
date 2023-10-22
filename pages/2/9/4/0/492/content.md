
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A Kan fibration is one of the notions of [[fibrations of simplicial sets]]:


\begin{definition}
A _Kan fibration_ is a [[morphism]] $\pi \colon Y \to X$ of [[simplicial set|simplicial sets]] with the [[lifting property]] for all [[horn]]-inclusions.
\end{definition}

This means that for 

$$
 \array{
   \Lambda^k[n] &\longrightarrow& Y
   \\
   \big\downarrow && \big\downarrow\mathrlap{{}^\pi}
   \\
   \Delta^n &\longrightarrow& X
 }
$$

a [[commuting square]] with $n\ge 1$ and $0\le k\le n$, there always exists a [[lift]]

\[
  \label{HornFiller}
 \array{
   \Lambda^k[n] &\longrightarrow& Y
   \\
   \big\downarrow &\nearrow& \big\downarrow\mathrlap{{}^\pi}
   \\
   \Delta^n &\longrightarrow& X
 }
 \,.
\]

In terms of the canonical [[powering]] of simplicial sets over sets, this is equivalent to the morphisms

$$
  Y^{\Delta[n]}
  \to 
  Y^{\Lambda^k[n]} \times_{X^{\Lambda^k[n]}} X^{\Delta^k[n]}
$$

all being [[epimorphisms]]. (Here, for instance, $Y^{\Lambda^k[n]}$ is the set of tuples of $(n-1)$-cells in $Y$ that glue along their boundaries to an image of the $k$th $n$-[[horn]].)


## Illustration

Kan fibrations are combinatorial analogs of [[Serre fibration|Serre]] [[fibrations]]  of [[topological spaces]].  In fact, under the [[Quillen equivalence]] of the standard [[model structure on topological spaces]] and the standard [[model structure on simplicial sets]], Kan fibrations map to Serre fibrations.

Recall the shape of the [[horns]] in low dimension. 

* -**$n=1$**- The horns $\Lambda^1_0$ and $\Lambda^1_1$ of the 1-[[simplex]] are just copies of the 0-[[simplex]] $\Delta^0$ regarded as the left and right endpoint of $\Delta^1$. For $n= 1$ the above condition says that for $\pi : Y \to X$ a Kan fibration we have
  $$
    \array{
       Y &\ni &
       y
       \\
      \downarrow^\pi
       \\
       X &\ni& \pi(y) &\stackrel{\forall f}{\to}& x
    }
    \;\;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;\;  
    \array{
       Y &\ni&
       y &\stackrel{\exists \hat f}{\to}& \exists \hat x
       \\
       \downarrow^\pi
       \\
       X &\ni& \pi(y) &\stackrel{f = \pi(\hat f)}{\to}& x = \pi(x)
    }
  $$
  corresponding to the lifting diagram
  $$
   \array{
     \Lambda_1^1 &\stackrel{y}{\to}& Y
     \\
     \downarrow &{}^{\hat f}\nearrow& \downarrow^\pi
     \\
     \Delta^1 &\stackrel{f}{\to}& X
   }
   \,.
  $$

* -**$n=2$**- the horn $\Lambda^2_1$ consists of the 
two top sides of a triangle. For this the Kan condition 
says that for any two composable 1-cells in $Y$ that
have a "composite up to a 2-cell" in $X$, there exists
a corresponding "composite up to a 2-cell" in $Y$ that
projects down to the one in $X$:

  $$
  \array{
    &&&&& y_2
    \\
    &&&& \nearrow && \searrow
    \\
    Y &\ni& & y_1 &&&& y_3
    \\
    \downarrow^\pi 
    \\
    X &\ni& &&& \pi(y_2)
    \\
    &&& & \nearrow &\Downarrow^{\forall h}& \searrow
    \\
    &&& \pi(y_1) &&\to&& \pi(y_2)
  }
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  \array{
    &&&&& y_2
    \\
    &&&& \nearrow &\Downarrow^{\exists \hat h}& \searrow
    \\
    Y &\ni& & y_1 &&\stackrel{\exists}{\to}&& y_3
    \\
    \downarrow^\pi 
    \\
    X &\ni& &&& \pi(y_2)
    \\
    &&& & \nearrow &\Downarrow^{h = \pi(\hat h)}& \searrow
    \\
    &&& \pi(y_1) &&\to&& \pi(y_2)
  }
  $$
  This corresponds to the lifting diagram
  $$
   \array{
     \Lambda_2^1 &\stackrel{y}{\to}& Y
     \\
     \downarrow &{}^{\hat h}\nearrow& \downarrow^\pi
     \\
     \Delta^2 &\stackrel{h}{\to}& X
   }
   \,.
  $$
  
  * Crucial is this condition for the _outer horns_ $\Lambda^n_0$ and $\Lambda^n_n$, where it says that the above works not only when edges are composable, but also when they meet just at  their sources or their targets. For instance for the horn $\Lambda^2_2$ the picture is
    $$
    \array{
      &&&&& y_2
      \\
      &&&& && \searrow
      \\
      Y &\ni& & y_1 &&\to&& y_3
      \\
      \downarrow^\pi 
      \\
      X &\ni& &&& \pi(y_2)
      \\
      &&& & \nearrow &\Downarrow^{\forall h}& \searrow
      \\
      &&& \pi(y_1) &&\to&& \pi(y_2)
    }
    \;\;\;\;\;\;
    \Rightarrow  
    \;\;\;\;\;\;
    \array{
      &&&&& y_2
      \\
      &&&& {}^\exists\nearrow &\Downarrow^{\exists \hat h}
      &    \searrow
      \\
      Y &\ni& & y_1 &&\stackrel{\exists}{\to}&& y_3
      \\
      \downarrow^\pi 
      \\
      X &\ni& &&& \pi(y_2)
      \\
      &&& & \nearrow &\Downarrow^{h = \pi(\hat h)}& \searrow
      \\
      &&& \pi(y_1) &&\to&& \pi(y_2)
    }
    $$
    This corresponds to the lifting diagram
    $$
     \array{
       \Lambda_2^2 &\stackrel{y}{\to}& Y
       \\
       \downarrow &{}^{\hat h}\nearrow& \downarrow^\pi
       \\
       \Delta^2 &\stackrel{h}{\to}& X
     }
     \,.
    $$


## Variants

### Minimal Kan fibration

A Kan fibration $p : E \to B$ is called 
a **[[minimal Kan fibration]]** 
if for all cells $x,y : \Delta[n] \to E$ 
the condition $p(x) = p(y)$ and $\partial_i x = \partial_i y$ implies for all $k$ that $\partial_k x = \partial_k y$.


### Quasi-fibration

A **quasi-fibration** or **weak Kan fibration** or **inner Kan fibration** of simplicial sets is defined as above, but with the lifting property only imposed in _inner horns_: $\Lambda^n_k$ with $0 \lt k \lt (n-1)$, not the _outer horns_ $\Lambda^n_0$ and $\Lambda^n_n$.

This weakened condition then says that _composition_ of cells may be lifted through the quasi-fibration, but not necessarily [[inverse|inversion]] of 1-cells.  See [[fibrations of quasi-categories]] for more details.

### Left and right Kan fibration 

Similarly, a **left Kan fibration** is one that has the lifting property for all horns except possibly the last one.
and a **right Kan fibration** is one that has the lifting property for all horns except possibly the first one.  See [[fibrations of quasi-categories]] for more details.


## Examples
 {#Examples}

\begin{example}\label{EmptyBundleIsKanFibration}
**([[empty bundle]] is [[Kan fibration]])**
Every [[empty bundle]] $\varnothing \to X$ is a [[Kan fibration]], since none of the [[commuting squares]] that one would have to [[lifting property|lift in]] actually exist

  $$
    \array{
      \Lambda_k^n &\overset{ \not \exists }{\longrightarrow}& \varnothing
      \\
      \big\downarrow && \big\downarrow
      \\
      \Delta^n &\longrightarrow& B
    }
  $$

(keeping in mind that the [0-simplex has no horns](horn#ZeroSimplexHasNoHorns), hence that all horns are [[inhabited set|inhabited]], so that there is *no* [[morphism]] from any horn to the [[empty simplicial set]], this being a [[strict initial object]]).
\end{example}


## Properties

### Surjective Kan fibrations
 {#SurjectiveKanFibrations}

Notice that a Kan fibration need *not* be a [[surjection]] in any sense:
\begin{example}
 \label{KanFibrationNeedNotBeSurjective}
  For $X \,\in\, sSet$ any [[simplicial set]], the unique morphism from the [[initial object|initial]] simplicial set (which is the [[empty set]] in each degree) is a Kan fibration (the [[empty bundle]]): 
$$
  \varnothing \underset{\in KanFib}{\longrightarrow} X
  \,.
$$
This is due to the fact that *[the 0-simplex has no horns](horn#ZeroSimplexHasNoHorns)*, namely that all [[horns]] appearing in the Kan condition (eq:HornFiller) are [[inhabited set|inhabited]], so that none of them has any morphism to $\varnothing$ (which is a [[strict initial object]]), so that the horn filler condition for the [[empty bundle]] is vacuous and hence satisfied.
\end{example}

But:
\begin{lemma}
  \label{KanFibrationWhichIsEpiInDegreeZeroIsEpi}
  As soon as a Kan fibration is a [[surjection]] in degree 0, then it is a [[surjection]] in all degrees (and [hence](SimpSet#EpimorphismsOfSimplicialSetsDetectedDegreewise) an [[epimorphism]] of simplicial sets):
$$
  X \overset{f}{\underset{\in KanFib}{\longrightarrow}} Y
  \;\;\text{and}\;\;
  f_0 \; \text{is surjective}
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  \underset{n \in \mathbb{N}}{\forall}
  \;\;
  f_n \; \text{is surjective}
$$
\end{lemma}
\begin{proof}
  Let $\Delta[n] \xrightarrow{\sigma_n} Y$ be any [[n-simplex|$n$-simplex]] (seen, under the [[Yoneda lemma]], as a morphism from the standard [[n-simplex|$n$-simplex]]). We equivalently need to show that this [[lift|lifts]] through $f$, in that we have a [[commuting diagram]] of this form:
$$
  \array{
    && X
    \\
    &
    \mathllap{{}^{\widehat{\sigma_n}}}\nearrow
    &
    \big\downarrow \mathrlap{ {}^{f} }
    \\
    \Delta[n]
    &\underset{\sigma_n}{\longrightarrow}&
    Y
    \mathrlap{\,.}
  }
$$
Now, by the assumption that $f_0$ is surjective, we do have such a lift at least for any [[vertex]] $v$ of $\sigma_n$, hence we have a [[commuting diagram]] of this form:
$$
  \array{
    \Delta[0]
    &\overset{\widehat{v}}{\longrightarrow}&
    X
    \\
    \big\downarrow
    &&
    \big\downarrow\mathrlap{{}^{f}}
    \\
    \Delta[n]
    &\underset{\sigma_n}{\longrightarrow}&
    Y
    \mathrlap{\,.}
  }
$$
But the left morphism is an [[acyclic cofibration]] in the [[classical model structure on simplicial sets]]. These have the [[left lifting property]] against Kan fibrations, meaning that this last square has a [[lift]] $\widehat{\sigma_n}$. This exhibits the desired preimage of $\sigma_n$.
\end{proof}

In fact:
\begin{lemma}
  \label{KanFibrationWhichIsEpiOnComponentsIsEpi}
  As soon as a Kan fibration $f$ is a [[surjection]] on [[connected components]], $\pi_0(f) \colon \pi_0(X_\bullet) \twoheadrightarrow \pi_0(Y_\bullet)$, then it is a [[surjection]] in all degrees (and [hence](SimpSet#EpimorphismsOfSimplicialSetsDetectedDegreewise) an [[epimorphism]] of simplicial sets):
\end{lemma}
\begin{proof}
  By definition (of [[simplicial homotopy groups]]), all [[vertices]] in a connected component are connected by some [[zig-zag]] $Z$ of [[edges]]. But the inclusion of an endpoint vertex $\Delta[0] \hookrightarrow Z$ into (the abstract shape of) such a zig-zag is evidently an [[acyclic cofibration]], hence has the [[left lifting property]] against the given Kan fibration (by the [[classical model structure on simplicial sets]]). Evaluating this lift at the other endpoint shows that the Kan fibration is surjective on vertices as soon as it is surjective on connected components. Therefore the claim follows with Lemma \ref{KanFibrationWhichIsEpiInDegreeZeroIsEpi}. 
\end{proof}

In summary:
\begin{proposition}\label{EveryPiZeroEpiIsResolvedByASurjectiveKanFibration}
  Let 
  $X \xrightarrow{f} Y$ be any morphism of [[simplicial sets]] which is a [[surjection]] on [[connected components]]: $\pi_0(f) \,\colon\, \pi_0(X) \twoheadrightarrow \pi_0(Y)$ (hence presenting an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] of [[infinity-groupoids|$\infty$-groupoids]], by [this Prop.](effective+epimorphism+in+an+infinity1-category#EffectiveEpisOfInfinityGroupoids)). Then $f$ factors as a [[simplicial weak equivalence]] followed by a Kan fibration which is a degreewise [[surjection]] (and [hence](SimpSet#EpimorphismsOfSimplicialSetsDetectedDegreewise) an [[epimorphism]] of [[simplicial sets]]).
\end{proposition}
\begin{proof}
  The factorization follows by standard constructions such as the [[factorization lemma]] or the existence of the [[classical model structure on simplicial sets]]. With this the claim follows by Lemma \ref{KanFibrationWhichIsEpiOnComponentsIsEpi}.
\end{proof}

\begin{remark}\label{SurjectivityOfAcyclicKanFibrations}
The assumption in Prop. \ref{EveryPiZeroEpiIsResolvedByASurjectiveKanFibration} is met in particular for [[acyclic Kan fibrations]]. In this special case the above factorization is trivial in that acyclic Kan fibrations are already degreewise surjective themselves (see the discussion [there](acyclic+Kan+fibration#AcyclicKanFibrationsAreSurjective)).
\end{remark}

\linebreak

### Acyclic Kan fibrations and weak homotopy equivalences

+-- {: .num_theorem}
###### Theorem

The [[acyclic Kan fibrations]] morphisms $f : X \to Y$ of Kan complexes that are both Kan fibrations as well as [[model structure on simplicial sets|weak equivalences]] in that they induce isomorphisms on all [[simplicial homotopy groups]] (i.e. the __[[acyclic fibrations]]__ of Kan complexes) are precisely the morphisms that have the [[weak factorization system|right lifting property]] with respect to all [[boundary of a simplex|boundary inclusions]] $\partial \Delta^n \hookrightarrow \Delta^n$:
  $$
    \array{
      \partial \Delta[n] &\to& X
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^f 
      \\
      \Delta[n] &\to& Y
    }
    \,.
  $$

=--

e.g. ([Goerss-Jardine, chapter I](#GoerssJardine96))

+-- {: .num_cor}
###### Corollary

Kan fibrations and acyclic Kan fibrations are both stable under [[pullback]].

=--

+-- {: .proof}
###### Proof

Because every class of morphisms defined by a [[weak factorization system|right lifting property]] is stable under pullback.

=--

+-- {: .num_remark}
###### Remark
From this it follows readily that [[Kan complexes]] form a Brownian [[category of fibrant objects]].
=--


+-- {: .num_prop #AcyclicFibrationsDetectedFiberwise}
###### Proposition

A Kan fibration $f\colon X\to Y$ is acyclic precisely if the [[fiber]] $f^{-1}(y)$ over each vertex $y$ is [[contractible]].

=--

Purely combinatorial proofs of this statement include ([Joyal 2008, prop. 8.23](#Joyal08), [Riehl-Verity 13, lemma 5.4.16](#RiehlVerity13))

### Pullback and homotopy pullback

+-- {: .num_lemma #PullbackOfKanFibrationSendsLeftHomotopyToFiberwiseHomotopyequivalence}
###### Lemma

Let $p \colon X \longrightarrow Y$ be a [[Kan fibration]], def. \ref{KanFibration}, and let $f_1,f_2 \colon A \longrightarrow X$ be two morphisms. If there is a [[left homotopy]] $f_1 \rightarrow f_2$ between these maps, then there is a fiberwise [[homotopy equivalence]], between the [[pullback]] fibrations $f_1^\ast X \simeq f_2^\ast X$.

=--

(e.g. [Goerss-Jardine 96, chapter I, lemma 10.6](#GoerssJardine96))

See also at _[[homotopy pullback]]_.


### On nerves of groupoids


+-- {: .num_theorem}
###### Theorem

A [[functor]] $F \colon C \to D$ between [[groupoids]] is [[k-surjective functor|k-surjective]] for all $k$ and hence a surjective [[equivalence of categories]] precisely if under the [[nerve]] $N(F) : N(C) \to N(D)$ it induces an acyclic fibration of Kan complexes;

=--

+-- {: .proof}
###### Proof

We know that both $N(C)$ and $N(D)$ are Kan complexes. By the above theorem it suffices to show that $N(f)$ being a surjective equivalence is the same as having all lifts

$$
  \array{
    \delta \Delta[n] &\to& N(C)
    \\
    \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
    \\
    \Delta[n] &\to& N(D)
  }
  \,.
$$


We check successively what this means for increasing $n$:

* $n= 0$. In degree 0 the boundary inclusion is that of the empty set into the [[nLab:point|point]] $\emptyset \hookrightarrow {*}$. The lifting property in this case amounts to saying that every point in $N(D)$ lifts through $N(F)$. 
  $$
    \array{
      \emptyset &\to& N(C)
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \Leftrightarrow
    \array{
      && N(C)
      \\
      &{}^\exists\nearrow& \downarrow^{N(F)}
      \\
      {*} &\to& N(D)
    }
    \,.
  $$
  This precisely says that $N(F)$ is surjective on 0-cells and hence that $F$ is surjective on objects.

* $n=1$. In degree 1 the boundary inclusion is that of a pair of points as the endpoints of the interval
  $\{\circ, \bullet\} \hookrightarrow \{\circ \to \bullet\}$. The lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ all elements in $Hom(F(a),F(b))$ are hit. Hence that $F$ is a [[nLab:full functor|full functor]].

* $n=2$. In degree 2 the boundary inclusion is that of the triangle as the boundary of a filled triangle. It is sufficient to restrict attention to the case that the map $\partial \Delta[2] \to N(C)$ sends the top left edge of the triangle to an identity. Then the lifting property here evidently is  equivalent to saying that for all objects $a,b \in Obj(C)$ the map $F_{a,b} : Hom(a,b) \to Hom(F(a),F(b))$ is injective. Hence that $F$ is a [[nLab:faithful functor|faithful functor]].
  $$
    \left(
    \array{
      && a 
      \\
      & {}^{Id_a}\nearrow && \searrow^{f}
      \\
      a &&\stackrel{g}{\to}&& b
    }
    \right)
    \stackrel{N(F)}{\mapsto}
    \left(
    \array{
      && a 
      \\
      & {}^{Id_a}\nearrow &\Downarrow^=& \searrow^{F(f)}
      \\
      a &&\stackrel{F(g)}{\to}&& b
    }
    \right)
  $$


=--


### Universal Kan fibration

See at _[[universal Kan fibration]]_.



## Relation to other concepts

* Kan fibrations and quasi-fibrations are fibrations in two common [[model structure on simplicial sets|model structures on simplicial sets]].

* Recall that the [[horn]] $\Lambda^k[n]$ is the boundary of the $n$-[[simplex]] $\Delta^n$ with one face removed. If in the above definition one replaces horns with the full boundaries of simplices, one obtaines the definition of a [[hypercover]], the acyclic fibrations in the classical [[model structure on simplicial sets]].

* A simplicial set $X$ for which the unique morphism $X \to pt$ to the [[terminal object|terminal simplicial set]] is a Kan fibration is called a [[Kan complex]].

* A simplicial set $X$ for which the unique morphism $X \to pt$ to the [[terminal object|terminal simplicial set]] is a quasi-fibration/weak Kan fibration is called a [[quasi-category]].

* Just as the underlying simplicial set of a [[simplicial group]] is a [[Kan complex]] (see algorithm at [[simplicial group]]), so also given any simplicial morphism $f : G\to H$ of simplicial groups for which in each dimension, $n$, the homomorphism $f_n : G_n \to H_n$ is an [[epimorphism]], then the underlying simplicial map of simplicial sets is a Kan fibration. (Apart from a careful choice of section in each dimension, the proof can be constructed from the algorithm given in [[simplicial group]].)

* A morphism of simplicial sets that has the left [[lifting property]] with respect to all Kan fibrations is called an [[anodyne morphism]].

## Related concepts

* **Kan fibration**, [[anodyne morphism]]

  * [[acyclic Kan fibration]]

* [[Kan complex]]

* [[right/left Kan fibration]], [[right/left anodyne map]]

* [[inner fibration]]

* [[Cartesian fibration]]  

* [[simplicial homotopy theory]]

* [[homotopy Kan fibration]]


## References

The original definition is due to [[Daniel M. Kan]], see Definition 3.1 in

* [[Daniel M. Kan]], _A combinatorial definition of homotopy groups_, The Annals of Mathematics 67:2 (1958), 282–312.  [doi](http://dx.doi.org/10.2307/1970006).

This was extended to arbitrary [[simplicial objects]] via the [[Yoneda embedding]] in Definition 3.2 of

* [[Daniel M. Kan]], _On c.s.s. categories_, Boletín de la Sociedad Matemática Mexicana 2 (1957), 82–94.  [PDF](https://dmitripavlov.org/scans/kan-on-css-categories.pdf).


A standard textbook account is

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_, 1996

That [[topological realization]] takes Kan fibrations to [[Serre fibrations]] is due to:

* {#Quillen68} [[Daniel Quillen]], *The geometric realization of a Kan fibration is a Serre fibration*, Proc. AMS 19 (1968) 1499-1500 &lbrack;[doi:1968-019-06/S0002-9939-1968-0238322-1](https://www.ams.org/journals/proc/1968-019-06/S0002-9939-1968-0238322-1), [pdf](https://www.ams.org/journals/proc/1968-019-06/S0002-9939-1968-0238322-1/S0002-9939-1968-0238322-1.pdf)&rbrack;

reviewed in

* {#GoerssJardine99} [[Paul Goerss]], [[J. F. Jardine]], Thm. 10.10 in: *[[Simplicial homotopy theory]]*, Progress in Mathematics, Birkhäuser (1999), Modern Birkhäuser  Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack;


See also

* {#Joyal08} [[André Joyal]], *[[The Theory of Quasi-Categories and its Applications]]*, lectures at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM 2008 ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]])


* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], _Homotopy coherent adjunctions and the formal theory of monads_, ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))

A structured/constructive analogue suited to purposes like [[homotopy type theory]] with equivalent homotopy theory is the notion of effective Kan fibration from

* Benno van den Berg, Eric Faber, _Effective Kan fibrations in simplicial sets_, [arXiv:2009.12670](https://arxiv.org/abs/2009.12670)
* Benno van den Berg, _Effective Kan fibrations in simplicial sets_,  Bohemian Logical & Philosophical Café, Feb 2021, [yt](https://www.youtube.com/watch?v=i1TkX_86rLo)

[[!redirects Kan fibrations]]