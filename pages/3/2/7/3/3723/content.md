
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

If an [[(∞,1)-topos]] $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] it has a good notion of  [[homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of its objects. In terms of these, there is an analog in $\mathbf{H}$ of the notion of the classical notion of [[Whitehead tower]] in the archetypical $(\infty,1)$-topos [[Top]]:

the Whitehead tower of an object $X \in \mathbf{H}$ is the tower of $n$-[[connected]] [[homotopy fiber]]s of the canonical morphism into the [[Postnikov tower in an (∞,1)-category|(∞,1)-topos-theoretic Postnikov tower]] $\cdots \to \mathbf{\Pi}_{n+1}(X) \to \mathbf{\Pi}_n(X) \to \cdots$ of the [[schreiber:path ∞-groupoid|structured path ∞-groupoid]] $\mathbf{\Pi}(X)$ of $X$.

See also the section <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Coverings">Universal coverings and geometric Whitehead towers</a> at [[cohesive (∞,1)-topos]].

## Definition

Let $\mathbf{H}$ be a [[locally ∞-connected (∞,1)-topos]] $\mathbf{H} \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}} \infty Grpd$. Write 

$$
  \mathbf{\Pi} \coloneqq LConst \circ \Pi : \mathbf{H} \to \mathbf{H}
$$

for the _internal_ [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]-functor. From the adjunction relation this comes with the canonical natural morphism

$$
  X \to \mathbf{\Pi}(X)
  \,.
$$

For $n \in \mathbb{N}$ write

$$
  \mathbf{H}_{\leq n} \stackrel{\overset{\tau_{\geq n}}{\leftarrow}}{\overset{}{\hookrightarrow}} \mathbf{H}
$$

for the [[reflective (∞,1)-subcategory]] of [[n-truncated object of an (∞,1)-category|n-truncated objects]] of $\mathbf{H}$ and write $\mathbf{\tau}_{\leq n}$ for the [[localization of an (∞,1)-category|localization]]

$$
  \mathbf{\tau}_{\leq n} : \mathbf{H} \stackrel{\tau_{\leq n}}{\to}
  \mathbf{H}_{\leq n} \hookrightarrow \mathbf{H}
  \,.
$$

Write

$$
  \mathbf{\Pi}_n : \mathbf{H} \stackrel{\mathbf{\Pi}}{\to} \mathbf{H} \stackrel{\mathbf{\tau}_{\leq n}}{\to} \mathbf{H}
$$

for the internal **homotopy $n$-groupoid**. For $X \in \mathbf{H}$ we have the [[Postnikov tower in an (∞,1)-category|(∞,1)-Postnikov tower]]

$$
  \cdots \to \mathbf{\Pi}_2(X) \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)
$$

of $\mathbf{\Pi}(X)$.

+-- {: .un_def}
###### Definition
**(Whitehead tower)**

For $X \in \mathbf{H}$, its **Whitehead tower** is the sequence of objects 

$$
  * \to \cdots \to X^{(2)} \to X^{(1)} \to X^{(0)} \simeq X
$$

in $\mathbf{H}$, where for each $n \in \mathbb{N}$ the object $X^{(n+1)}$ is the [[homotopy fiber]] of the canonical morphism $X \to \mathbf{\Pi}_{n+1}$, i.e. the object defined by the [[pullback]] diagram

$$
  \array{
    X^{(n+1)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_{n+1}(X)
  }
  \,.
$$

=--

Here the morphisms $X^{(n+1)} \to X^{(n)}$ are induced from the universality of the pullback:


$$
  \array{
    X^{(n+1)}&\to&X^{(n)}&& \mathbf{\Pi}_{(n+1)}(X)
    \\
    &\searrow &\downarrow&\nearrow& \downarrow
    \\
    &&X &\to& \mathbf{\Pi}_n(X)
  }
$$

+-- {: .un_remark}
###### Remark


We have that $\mathbf{\Pi}_n(X) \simeq LConst \tau_{\leq n} \Pi(X)$.

A homotopy-commuting diagram

$$
  \array{
    X^{(n)} &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X)
  }
$$

in $\mathbf{H}$ corresponds by the [[adjoint (∞,1)-functor|adjunction relation]] to diagram 

$$
  \array{
    \Pi(X^{(n)}) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \Pi(X) &\to& {\Pi}_n(X)
  }
$$

in [[∞Grpd]]. This being universal means that $\Pi(X^{(n)})$ is $n$-connected, and universal with that property as an object over $\Pi(X)$.

=--


## Properties {#Properties}

+-- {: .un_def}
###### Definition


For $* \to X \in \mathbf{H}$ a [[pointed object]] and $n \in \mathbb{N}$, $n \geq 1 $, define the object $\mathbf{B}^n \mathbf{\pi}_n(X)$ to be the [[homotopy fiber]] of $\mathbf{\Pi}_n(X) \to \mathbf{\Pi}_{n-1}(X)$, so that we have a [[fibration sequence]]

$$
  \mathbf{B}^n \mathbf{\pi}_n(X) \to \mathbf{\Pi}_n(X) \to \mathbf{\Pi}_{n-1}(X)
  \,.
$$

=--

+-- {: .un_proposition}
###### Proposition

With $\Pi(X) \in \infty Grpd \simeq Top$ the underlying topological space of $X \in \mathbf{H}$ (its [geometric realization](http://ncatlab.org/schreiber/show/path+%E2%88%9E-groupoid#GeomReal)) we have that 

$$
  \mathbf{B} \mathbf{\pi}_n(X)
  \simeq
  LConst \mathcal{B}^n \pi_n(X)
  \,,
$$

where $\mathcal{B}^n \pi_n(X)$ denotes the [[homotopy fiber]] of 
$\Pi_n(X) \to \Pi_{(n-1)}(X)$ in [[∞Grpd]].

=--

+-- {: .proof}
###### Proof

> check

This follows from $\mathbf{\tau}_{\leq n} LConst \Pi(X) \simeq LConst \tau_{\leq n} \Pi(X)$. This, in turn, can for instance be checked in terms of the [[model structure on simplicial presheaves]], using that $\tau$ is objectwise the [[coskeleton]] operation. More on that at [[Postnikov tower in an (∞,1)-category]].



=--


+-- {: .un_proposition}
###### Proposition

For each $n \geq 1$ we have a [[fibration sequence]]

$$
  X^{(n)} \to X^{(n-1)} \to \mathbf{B}^n \mathbf{\pi}_n(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Regard the diagram

$$
  \array{
    X^{(n)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X^{(n-1)} & \to & \mathbf{B}^n \mathbf{\pi}_n(X) &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X &\to& \mathbf{\Pi}_n(X) &\to& \mathbf{\Pi}_{(n-1)}(X)
  }
  \,.
$$

Here the right square is the defining $(\infty,1)$-pullback diagram of $\mathbf{B}^n \mathbf{\pi}_n(X)$ from above. Take also the left bottom square to be a homotopy pullback. Then from the pasting rules of pullbacks it follows that the composite bottom rectangle is also a pullback, which identifies the object $X^{(n-1)}$ on the left as indicated.

Similarly, form now the top square as a pullback. Then by the composition law of pullbacks we find that the composite vertical rectangle is a pullback, which identifies the top left object as $X^{(n)}$.

=--



## Examples

### For $\infty$-groupoids

In the archetypical $(\infty,1)$-topos $\mathbf{H} = $ [[∞Grpd]] the functors $\Pi$ and $\mathbf{\Pi}$ are the identity and so 
$\cdots \to \mathbf{\Pi}_1(X) \to \mathbf{\Pi}_0(X)$ is just the standard [[Postnikov tower]] $\cdots \to X_1 \to  X_0 $. 

If we use the [[model structure on simplicial sets]] in order to [[presentable (infinity,1)-category|present]] $\infty Grpd$, then the Postnikov tower may be realized by the simplicial [[coskeleton]] operation

$$
  \cdots \to \mathbf{cosk}_2(X) \to \mathbf{cosk}_1(X)
  \,.
$$

If $X$ is [[connected]], the [[homotopy pullback]] 

$$
  \array{
    X^{(n+1)} &\to& *
    \\
    \downarrow && \downarrow
    \\
    X &\to& X_{(n)}
  }
$$

defining the Whitehead tower of an $\infty$-groupoid incarnated as a [[Kan complex]] $X$ may be computed as an ordinary [[pullback]] using a fibrant replacement diagram, such as thatr replacing the [[point]] by the [[decalage]] simplicial set, hence as the ordinary pullback

$$
  \array{
    X^{(n+1)} &\to& Dec \mathbf{cosk}_n X
    \\
    \downarrow && \downarrow
    \\
    X &\to& \mathbf{cosk}_n X
  }
$$

in [[sSet]].


If $X$ is a pointed $\infty$-groupoid then $\mathbf{B}^n \mathbf{\pi}_n(X)$ is the [[Eilenberg-Mac Lane space]] $K(\pi_n(X),n)$.


### For topological $\infty$-groupoids {#TopInfGrpds}

It is often useful to think of [[topological space]]s as embedded into the [[(∞,1)-topos]] of [[topological ∞-groupoid]]s, i.e. the [[(∞,1)-category of (∞,1)-sheaves]]/[[∞-stack]]s on (a [[small category|small]] version of) the [[site]] of "all" topological spaces.

$$
  \mathbf{H} = Sh_{(\infty,1)}(Top)
  \,.
$$

#### The universal covering spaces

For $X$ a topological space regarded as a representable object in $Sh_{(\infty,1)}(Top)$, we have that $\mathbf{\Pi}_1(X)$ is the [[fundamental groupoid]] of $X$, regarded as a [[topological ∞-groupoid]] in the obvious way.

Then the [[homotopy fiber]] $X^{(1)}$ of the constant path inclusion $X \to \mathbf{\Pi}_1(X)$ is the [[universal covering space]] of $X$, as described in detail there.

#### The higher covering spaces

The analog of this statement for the higher items $X^{(n)}$ with $n \gt 1$ in the Whitehead tower of a topological spaces regarded in the $(\infty,1)$-topos of topological groupoids  has been studied in

* [[David Roberts]], _[[Fundamental Bigroupoids and 2-Covering Spaces]]_ 

The following reviews some central ideas of this.


##### Non-traditional approach in $Top$ 

**The following is some semblance of current research, except the stuff about the string 2-group. All errors and stupid ideas are mine - [[David Roberts]]**

For locally nice spaces (say locally contractible), it is desirable to have a functorial construction of the Whitehead tower. A shadow of a low-dimensional case of this can be seen in the construction of the [[string 2-group]] given by Baez-Crans-Schreiber-Stevenson. Since finite-dimensional Lie groups have non-trivial third homotopy group, it is not possible to form the 3-connected cover in the [[category]] $fin.dim.LieGrp$, like it is possible to take the 0-, and 1-connected covers. While most people give up the smoothness and make do with the [[topological group]] $String_G$, The BCSS construction leaps out of that [[category]] into that of strict ([[Frechet space|Frechet]]) Lie [[2-group]]s. The construction is also functorial.

+--{: .query}
[[David Roberts]]: As an aside, I know of two classes of spaces with explicitly  constructed (i.e. not via co-killing homotopy groups) 2-connected covers: the 2-sphere and its quotients by $\mathbf{Z}/n$ (lens spaces), and the [[loop group]] $\Omega G$ of a compact, simple, simply-connected Lie group $G$ (the latter is the level-1 central extension by $U(1)$, the first needs no introduction). Does anybody know of any other $n$-connected covers (other than, say, the Hopf fibrations) that are canonically given?
=--

However, without one could demand a conceptually similar approach to the $n$-connected cover of a general (locally nice) space or smooth manifold. For $n=2$, and taking only [[topological space]]s for consideration, this is contained in [[David Roberts|my]] thesis work.
The rough result is that one gets a 2-connected topological groupoid $X^{(2)}$ equipped with a map to $X$ that factors through the universal covering space $X^{(1)}$. This is functorial, and generalises to higher connected covers (at least heuristically - I don't have $n$-categorical superpowers).

But the general idea is that one would get an $(n-1)$-groupoid $X^{(n)}$ over $X$ which is $n$-connected and such that the map to $X$ factors through the $(n-2)$-groupoid $X^{(n-1)}$. The map to $X$ should induce [[isomorphism]]s on homotopy groups $\pi_i$ for $i\gt n$, as in the usual Whitehead tower.

If we want to consider arbitrary $n$ and retain some sort of local triviality on our connected covers we cannot get away from the assumption that the space in question is locally contractible. An assumption of this sort appears in

*  [[Bertrand Toen]], Vers une interpretation Galoisienne de la theorie de l'homotopie, Cahiers de Top. et Geom. Diff. Cat., Vol. XLIII-4 (2002), 257-312. 

in the context of locally constant $\infty$-stacks and their monodromy (I haven't got this article at the moment, and I suspect they may be $(\infty,1)$-stacks, but I'm not 100 percent certain -DMR). Technically speaking, we don't need local contractibility but the existence of a basis of open sets $U \hookrightarrow X$ such that this inclusion map is null-homotopic. But I will continue to call this local contractibilty, for lack of a better term (if there is such a term, I'd like to know -DMR).

##### Construction using topological $n$-groupoids 

Consider the fundamental $n$-groupoid $\Pi_n(X)$ of the locally contractible space $X$ (as a [[Trimble n-category|Trimble n-groupoid]], say), or at least for now its underlying globular set. We can take the compact open-topology on the set of $k$-morphisms for $k \lt n$. As the space is locally contracible, in particular semi-locally $n$-connected, the space $Hom(S^{n-1},X)$ is semi-locally simply-connected (I have a fragment of a paper saying this is true for the \'absolute case\' - that is, _locally_ $n$-connected implies the mapping space locally simply connected, but I expect it to be true for the relative case -DMR). In particular, we can take the fundamental groupoid $\Pi_1(Hom(S^{n-1},X))$, which has a topology given in the [[topological fundamental groupoid|usual way]]. The arrow space of this fundamental groupoid is then non other than the space of $n$-arrows of $\Pi_n(X)$. It needs to be checked that the $n$ compositions $\#_k$, $k=0,\ldots,n-1$ are continuous, as well as a bunch of other stuff, but I think this should follow from (unique) lifting theorems for covering spaces.

The object space of $\Pi_n(X)$ is just $X$, and so there is an inclusion $X \hookrightarrow \Pi_n(X)$, and it is this that replaces the Postnikov section in the Whitehead construction outlined above. The topological fundamental $n$-groupoid, even though it contains apparently more homotopical information than the untopologised fundamental $n$-groupoid $\Pi_n(X)^\delta$ ($\delta=$discrete topology), I posit that under the assumptions on $X$, the inclusion $\Pi_n(X)^\delta \to \Pi_n(X)$ has an ana-n-functor pseudoinverse (taking the [[Grothendieck pretopology]] of open covers should be enough). On passing to the homotopy colimit this span should become a span weak homotopy equivalences, and so we can consider the topologised and the untopologised to be different representatives of the $n$-type of $X$.

Given a basepoint $x\in X$, we can form the tangent $n$-groupoid $T_x \Pi_n(X)$, which is equivalent to the trivial $n$-groupoid $*$ (even as a _topological_ $n$-groupoid), and gives us what should be in any sensible definition a fibration $T_x\Pi_n(X) \to \Pi_n(X)$. 
Pull back this fibration to $X$, and call the resulting thing $X^{(n)}$. It is fairly easy to see that $X^{(n)}$ is a topological $(n-1)$-groupoid over $X$. This then should be the $n$-connected cover of $X$. For $n=1$ this is precisely the classical construction of the universal covering space of a pointed space. For $n=2$ this is treated in

*  D.M. Roberts, Fundamental bigroupoids and 2-covering spaces, PhD thesis, available [[davidroberts:HomePage|here]]

and the two-dimensional homotopical tools developed there can be used to show that $X^{(2)}$ is 2-connected.

A word is probably in order about the notion of $k$-connectedness for topological $n$-groupoids. This has its usual meaning, once homotopy groups $\pi_i$ have been defined. The reader should be warned that these have nothing to do with the groups $\pi_0 Eq(1_{._{._{1_x}}})/\sim$ obtained from considering the autoequivalence $n-i+1$-group of the identity $(i-1)$-arrow on the identity $(i-2)$-arrow on ... on the object $x$. These should be defined in such a way as to agree with the homotopy colimit $hocolim X$ of $X$ considered as a truncated simplicial space. In particular, $\pi_1$ of a topological groupoid is _not_ the group of automorphisms of the basepoint, but a quotient of the set of _generalised paths_, an idea going back to Haefliger (for an intro see the early parts of chapter 2 of the above thesis, available at [[davidroberts:HomePage]], or the preprint H. Colman, _On the 1-homotopy type of Lie groupoids_, arXiv:math/0612257). 

There are other interpretations of $X^{(n)}$:

 * The (0-)source fibre of $\Pi_n(X)$, which is:
 * The pullback of $(s_0,t_0):Hom_{\Pi_n(X)} \to X\times X$ along the inclusion $\{x\}\times X \to X\times X$, where $Hom_{\Pi_n(X)}$ is the (internalised) hom-$(n-1)$-groupoid familiar from the definition of a Trimble $n$-groupoid.
 * The \'vertical fundamental $(n-1)$-groupoid\' of $PX \to X$, the path fibration.

The last can be thought of as a families version of the usual fundamental $(n-1)$-groupoid: take vertical paths, vertical homotopies between paths etc.

[[!redirects Whitehead tower in an (∞,1)-topos]]
