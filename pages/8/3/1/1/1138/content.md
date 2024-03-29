
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

> This page is about **inverse images of sheaves** and related subjects.  For the set-theoretic operation, see [[preimage]].

***

# Inverse images
* tic
{: toc}


## Idea

An _inverse image_ operation is the [[left adjoint]] part $f^*$ of a [[geometric morphism]] $(f^* \dashv f_*) \colon E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} F$ between [[topoi]].

For the case of [[sheaf topoi]] the inverse image

$$
  f^{-1} : Sh(Y) \to Sh(X)
$$

may be interpreted as encoding the idea of *[[pullback bundle|pulling back]]* along $f$ the "[[bundle]] of which the sheaf is the sheaf of sections".

In the case that $X$ and $Y$ are (the [[sites]] corresponding to) [[topological spaces]], this interpretation becomes literally true: the inverse image of a sheaf on topological spaces is the pullback operation on the corresponding [[etale spaces]].


## Definition

Consider a [[functor]] $f^t \colon Y \to X$ between the [[underlying]] categories of [[sites]].


### on presheaves

The [[direct image]] operation $f_* \colon PSh(X) \to PSh(Y)$ on [[presheaves]] is just precomposition with $f^t$

$$
  \array{
    Y^{op}
    &\overset{f_* F}{\longrightarrow}&
    Set
    \\
    \mathllap{
     {}^{f^t}
    }\big\downarrow & \nearrow\mathrlap{_{F}}
    \\
    X^{op}
  }
  \,.
$$

The **inverse image** operation 

$$
  f^{-1} \colon PSh(Y) \to PSh(X)
$$

on [[presheaves]] is the [[left adjoint]] to the [[direct image]] operation on presheaves, hence the left [[Kan extension]] along $f^t$:

$$
  f^{-1} F \;\coloneqq\;  Lan_{f^t} F
  \,.
$$

. 


### on sheaves

The inverse image operation on the [[category of sheaves]] $Sh(Y) \subset PSh(Y)$ inside the category of presheaves involves [[Kan extension]] followed by [[sheafification]].

First notice that

+-- {: .un_lemma}
###### Lemma

The [[direct image]] operation $f_* \colon PSh(X) \to PSh(Y)$ restricts to a functor $f_* \colon Sh(X) \to Sh(Y)$ that sends sheaves to sheaves.

=--

+-- {: .proof}
###### Proof

The direct image $f_* \colon PSh(X) \to PSh(Y)$ is more generally characterized by 
$$
  Hom_{PSh(Y)}(A, f_* F)
  \simeq
  Hom_{PSh(X)}(\hat {f^t} A, F)
$$
where $\hat f^t$ is the [[Yoneda extension]] of $Y \circ f^t \colon Y \to PSh(X)$ to a functor $\hat {f^t} : PSh(Y) \to PSh(X)$, because using the [[co-Yoneda lemma]] and the colim expression for the [[Yoneda extension]] we have

$$
 \begin{aligned}
   Hom(A, f_* F) & \simeq 
   Hom(colim_{Y(U) \to A}) U, f_* F)
   \\
   & \simeq
    \lim_{Y(U) \to A} Hom(U, f_* F)
   \\
   & \simeq
    \lim_{Y(U) \to A} F(f^t(U))
   \\
   & \simeq
    Hom( colim_{Y(U) \to A} f^t(U), F )
   \\
   & \simeq Hom(\hat {f^t}(A), F)
   \,.
 \end{aligned}
$$

Let now $\pi \colon B \to A$ be a [[local isomorphism]] in $PSh(Y)$.  By definition of morphism of [[sites]] we have that 
$$
  \hat {f^t}(\pi) : \hat{f^t}(B) \to \hat{f^t}(A)
$$
is a [[local isomorphism]] in $X$. From this and the above we obtain the isomorphism

$$
  Hom(B, f_* F)
  \simeq
  Hom(\hat {f^t}(B), F)
  \stackrel{\simeq}{\to}
  Hom(\hat {f^t}(A), F)  
  \simeq
  Hom(A, f_* F)
  \,,
$$
where the isomorphism in the middle is due to the fact that
$F$ is a sheaf on $X$. Since this holds for all local isomorphism $\pi : B \to A$ in $PSh(Y)$, $f_* F$ is a sheaf on $Y$.

=--


+-- {: .un_defn}
###### Definition

For $f : X \to Y$ a morphism of [[site]]s, the 
**inverse image of sheaves** is the functor
$$
  f^{-1} : Sh(Y) \to Sh(X)
$$
defined as the inverse image on presheaves followed
by [[sheafification]]
$$
  f^{-1} : Sh(Y) \hookrightarrow PSh(Y) \stackrel{Lan_{f^t}}{\to} PSh(X) \stackrel{\bar{-}}{\to}
  Sh(X)
  \,.
$$

=--

+-- {: .un_proposition}
###### Proposition

The inverse image $f^{-1} : Sh(Y) \to Sh(X)$
of sheaves has the following properties:

* it is [[left adjoint]] to the [[direct image]]
  $(f^{-1} \dashv f_*)$;

* it therefore commutes with small [[colimit]]s but is in addition left [[exact functor|exact]] in that it commutes with finite [[limit]]s.

=--

+-- {: .proof}
###### Proof

The left-adjointness is obtained by the following computation, for any
two $F \in Sh(X)$ and $G \in Sh(Y)$ and using the above facts as well as the fact that [[sheafification]] $\bar {(-)} : PSh(X) \to Sh(X)$ is [[left adjoint]] to the inclusion $Sh(X) \hookrightarrow PSh(X)$:

$$
  \begin{aligned}
    Hom_{Sh(Y)}(G, f_*F)
     & \simeq
    Hom_{PSh(Y)}(G, f_* F)
     \\
     & \simeq
       Hom_{PSh(X)}(Lan_{f^t} G, F)
     \\
     & \simeq
      Hom_{Sh(X)}( \bar{(Lan_{f^t} G)}, F)
     \\
     & =:
      Hom_{Sh(X)}(f^{-1}G, F)
  \end{aligned}
  \,.
$$

The proof of left-exactness requires more technology and work.

=--


### on sheaves on topological spaces

In the case where the [[site]]s $X$ and $Y$ in question are given by [[category of open subsets|categories of open subsets]] of [[topological space]]s denoted, by an abuse of symbols, also by $X$ and $Y$, one can identify sheaves with their corresponding [[etale space]]s over $X$ and $Y$. In that case the inverse image is simply obtained by the pullback along the continuous map $f : X \to Y$ of the corresponding [[etale space]]s.


## Properties

* See also [[restriction and extension of sheaves]].

* It follows that direct image and inverse image of
sheaves define a [[geometric morphism]] 
$f : Sh(X) \to Sh(Y)$
of [[sheaf]] [[topos|topoi]]

* Generally, therefore, the left adjoint partner in 
the adjoint pair defining a [[geometric morphism]]
of [[topos|topoi]] (or abelian categories of quasicoherent sheaves) is
called the **inverse image functor**. In fact more general in geometry, 
including [[noncommutative geometry|noncommutative]] morphisms often induce or are defined via pairs of adjoint functors among some associated categories of objects over a geometric space; then the left adjoint part is called the inverse image part. Geometers also often say inverse image for an arbitrary functor of the form $f^*$ in a [[fibered category]]. For abelian categories of sheaf-like objects, the corresponding higher derived functors of inverse image functors are sometimes called higher (derived) inverse image functors. 

* The other adjoint to the [[direct image]], the [[adjoint functor|right adjoint]], is (if it exists) the [[restriction and extension of sheaves|extension]] of sheaves.


## Examples

The standard example is that where $X$ and $Y$ are [[topological space]]s and $S_X = Op(X)$, $S_Y = Op(Y)$ are their [[category of open subsets|categories of open subsets.]]

A [[continuous map]] $f : X \to Y$ induces the obvious functor $f^{-1} : Op(Y) \to Op(X)$, since [[preimages]] of open subsets under continuous maps are open. 

Hence presheaves canonically push forward

$$
  f_* : PSh(X) \to PSh(Y)
$$

They do not in the same simple way pull back, since images of open subsets need not be open. The Kan extension  computes the best possible approximation:

The inverse image $(f^{-1})^\dagger : PSh(Y) \to PSh(X)$ sends $F \in PSh(Y)$ to

$$
  f^\dagger F(U) = \colim_{U \subseteq f^{-1}(V)} F(V)
  \,.
$$

What's this really doing is using $V$ to approximate $f(U)$ from the outside. Thus a section of $f^\dagger F$ on $U$ will be an equivalence class of sections of $F$ on open neighbourhoods of $f(U)$, under the equivalence given by agreement on a restriction to a smaller neighbourhood:
$$
  (s, V_1) \sim (t, V_2) \quad\underline{iff}\quad \exists W \in Op(Y), V_1 \cap V_2 \supseteq W \supseteq f(U), \; s\vert_W = t\vert_W.
$$
Compare this with the definition of [[germ|germs]] at a [[stalk]].

On the other hand, the extension $(f^{-1})^\ddagger : PSh(Y) \to PSh(X)$ sends $F \in PSh(Y)$ to

$$
  f^\ddagger F(U) = \lim_{f^{-1}(V) \subseteq U} F(V)
  \,.
$$

This approximates the possibly non-open subset $f(U)$ by all open subsets $V$  _contained_ in it.
This corresponds to taking the [[Kan extension|right Kan extension]] instead of the left one, and when it exists it's called [[restriction and extension of sheaves|extension of presheaves]].

## Related concepts

* [[derived inverse image]]

* [[exceptional inverse image]]

## References

For the general description in terms of Kan extension and sheafification see section 17.5 of

* Kashiwara-Schapira, [[Categories and Sheaves]]

For the description in terms of pullback of étale spaces, see section VII.1 of

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]]


[[!redirects inverse image]]
[[!redirects inverse images]]
[[!redirects inverse image functor]]
