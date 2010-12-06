
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



This is a sub-entry of [[homotopy groups in an (∞,1)-topos]]. 

For the other notion of homotopy groups see [[geometric homotopy groups in an (∞,1)-topos]].

#Contents#
* automatic table of contents goes here
{:toc}


## Definition

Recall that since an [[(∞,1)-topos]] $\mathbf{H}$ has all [[limits in a quasi-category|limits]],  it is naturally
[powered over ∞Grpd](http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring):

$$
  (-)^{(-)} : \infty Grpd^{op} \times \mathbf{H} \to \mathbf{H}
  \,.
$$


Let $S^n = \partial \Delta[1]$ (or  $S^n := Ex^\infty \partial \Delta[n+1]$) be the ([[Kan fibrant replacement]]) of the [[boundary of a simplex|boundary of the (n+1)-simplex]], i.e. the model in [[∞Grpd]] of the [[pointed object|pointed]] $n$-[[sphere]].

Then for $X \in \mathbf{H}$ an object, the power object $X^{S^n} \in \mathbf{H}$ plays the role of the space of of maps from the $n$-sphere into $X$, as in the definition of [[simplicial homotopy groups]], to which this reduces in the case that $\mathbf{H} = $ [[∞Grpd]]. 

By powering the canonical morphism $ i_n : * \to S^n$ induces a morphism

$$
  X^{i_n} : X^{S^n} \to X
$$

which is restriction to the basepoint. This morphism may be regarded as an object of the [[over quasi-category|over]] [[(∞,1)-topos]] $\mathbf{H}_{/X}$.

### Of objects

+-- {: .un_defn}
###### Definition
**(categorical homotopy groups)**

For $n \in \mathbb{N}$ define

$$
  \pi_n(X) := \tau_{\leq 0} X^{i_n} \in \mathbf{H}_{/X}
$$

to be the [[n-truncated object of an (infinity,1)-topos|0-truncation]] of the object $X^{i_n}$.

=--

Passing to the 0-truncation here amounts to dividing out the [[homotopy|homotopies]] between maps from the $n$-sphere into $X$. The [[n-truncated object of an (infinity,1)-topos|0-truncated]] objects in $\mathbf{H}/X$ have the interpretation of [[sheaf|sheaves]] on $X$. So in the world of [[∞-stack]]s a homotopy [[group object]] is a [[sheaf]] of groups.

To see that there is indeed a group structure on these _homotopy sheaves_ as usual, notice from the general properties of [[power]]ing we have that 

$$
  X^{S^k \coprod_* S^l}
  \simeq
  X^{S_k} \times_X X^{S_l}
  \,.
$$

From the <a href="http://ncatlab.org/nlab/show/n-truncated+object+of+an+(infinity%2C1)-category#Properties">discussion of properties of truncation</a> we have that $\tau_{\leq n} : \mathbf{H} \to \mathbf{H}$ preserves such finite [[product]]s so that also

$$
  \tau_{\leq 0} X^{* \to S^k \coprod_* S^l}
  \simeq
  (\tau_{\leq 0} X^{* \to S^k} ) \times 
  (\tau_{\leq 0}) X^{* \to S^k}
  \,.
$$

Therefore the [[cogroup]] operations $S^n \to S^n \coprod_* S^n$ induce group operations

$$
  \pi_n(X) \times \pi_n(X) \to \pi_n(X)
$$

is the [[sheaf topos]] $\tau_{\leq 0} \mathbf{H}_{/X}$. By the usual argument aboiut [[homotopy group]]s, these are trivial for $n = 0$ and [[abelian group|abelian]] for $n \geq 2$.

### Of morphisms

It is frequently useful to speak of homotopy groups of a [[morphism]] $f : X \to Y$ in an $(\infty,1)$-topos

+-- {: .un_defn}
###### Definition
**(homotopy groups of morphisms)**

For $f : X \to Y$ a [[morphism]] in an [[(∞,1)-topos]] $\mathbf{H}$, its _homotopy groups_ are the homotopy groups in the above sense of $f$ regarded as an object of the [[over quasi-category|over (∞,1)-category]] $\mathbf{H}_{/Y}$.

=--

So the homotopy sheaf $\pi_n(f)$ of a morphism $f$ is an object of the [[over quasi-category|over (∞,1)-category]] $Disc((\mathbf{H}_{/Y})_{/f}) \simeq Disc(\mathbf{H}_{/f})$. This in turn is equivalent to $\cdots \simeq \mathbf{H}_{/X}$ by the map that sends an object

$$
  \array{
    && Q
    \\
    & \swarrow && \searrow
    \\
    X &&\stackrel{f}{\to}&& Y
  }
$$

in $\mathbf{H}_{/f}$ to

$$
  \array{
    && Q
    \\
    & \swarrow 
    \\
    X
  }
  \,.
$$

The intuition is that the homotopy sheaf $\pi_n(f) \in Disc(\mathbf{H}_{/X})$ over a basepoint $x : * \in X$ is the homotopy group of the [[nLab:homotopy fiber]] of $f$ containing $x$ at $x$.

**Examples** 

If $Y = *$ then there is an essentially unique morphism $f : X \to *$ whose [[homotopy fiber]] is $X$ itself. Accordingly $\pi_n(f) \simeq \pi_n(X)$.

If $X = *$ then the morphism $f : * \to Y$ is a point in $Y$ and the single [[homotopy fiber]] of $f$ is the [[loop space object]] $\Omega_f Y$.

## Properties

### In $\infty Grpd$

For the case that $\mathbf{H} = $ [[∞Grpd]] $\simeq$ [[Top]], the $(\infty,1)$-topos theoretic definition of categorical homotopy groups in $\mathbf{H}$ reduces to the ordinary notion of [[homotopy group]]s in [[Top]]. For $\infty Grpd$ modeled by [[Kan complex]]es or the standard [[model structure on simplicial sets]], it reduces to the ordinary definition of [[simplicial homotopy group]]s.

### Of homotopy groups of morphisms

The  definition of the homotopy groups of a morphism $f : X \to Y$
is equivalent to the following recursive definition

+-- {: .un_defn}
###### Definition/Proposition
**(recursive homotopy groups of morphisms)**

For $n \geq 1$ we have 

$$
  \pi_n(f) \simeq \pi_{n-1}(X \to X \times_Y X)
  \;\;\;
  \in 
  Disc(\mathbf{H}_{/X})
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, remark 6.5.1.3]].

This is the generalization of the familiar fact that [[loop space object]]s have the same but shifted homotopy groups: In the special case that $X = *$ and $f$ is $f : * \to Y$ we have $X \times_Y X = \Omega_f Y$ and $X \to X \times_Y X$ is just $* \to \Omega_f Y$, so that 

$$
  \pi_n(f) = \pi_n(Y)
$$

and 

$$
  \pi_{n-1}(X \to X \times_Y X) \simeq \pi_{n-1} \Omega_f Y
  \,.
$$

+-- {: .un_prop }
###### Proposition

Given a sequence of morphisms $X \stackrel{f}{\to}Y \stackrel{g}{\to} Z$ in $\mathbf{H}$, there is a [[long exact sequence]]

$$
  \cdots
  \to
  f^* \pi_{n+1}(g) \stackrel{\delta_{n+1}}{\to}
  \pi_n(f)
  \stackrel{g \circ f}{\to}
  \to 
  f^* \pi_n(g)
  \stackrel{\delta_n}{\to}
  \pi_{n-1}(f)
  \to
  \cdots
$$

in the [[topos]] $Disc(\mathbf{H}_{/X})$.

=--

This is [[Higher Topos Theory|HTT, remark 6.5.1.5]].


### Behaviour under geometric morphisms

+-- {: .un_prop }
###### Proposition

Geometirc morphisms of $(\infty,1)$-topos preserve homotopy groups.

If $k : \mathbf{H} \to \mathbf{K}$ is a [[geometric morphism]] of $(\infty,1)$-toposes then for $f : X \to Y$ any morphism in $\mathbf{H}$ there is a canonical [[isomorphism]]

$$
  k^* (\pi_n(f)) \simeq \pi_n(k^* f) 
$$

in $Disc(\mathbf{H}_{/k^* Y})$.

=--

This is [[Higher Topos Theory|HTT, remark 6.5.1.4]].

### Connected and truncated objects

Let $X \in \mathbf{H}$.

* The object $X$ is **$n$-[[truncated]]** if it is a [[n-truncated object in an (∞,1)-category|k-truncated object]] for some $k \gt n$ and if all its categorical homotopy groups above degree $n$ vanish.

  Every object decomposes as a sequence of $n$-truncated objects: the 
  [[Postnikov tower in an (∞,1)-category]].

* The object $X$ is **$n$-[[connected]]** if the terminal morphism 
  $X \to *$ is an [[effective epimorphism]] and if all categorical homotopy groups below degree $n$ are trivial.

* The object $X$ is an **[[Eilenberg-MacLane object]]** of degree $n$ if it is both $n$-connected and $n$-truncated.




## Models

When the [[(∞,1)-topos]] $\mathbf{H}$ is [[presentable (∞,1)-category|presented]] by a [[model structure on simplicial presheaves]] $[C^{op}, sSet]_{loc}$, then since this is an [[sSet]]-[[enriched model category]] structure the [[power]]ing by $\infty Grpd$ is modeled, as described at, <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#ModelsForTensoring">$(\infty,1)$-limit -- Tensoring -- Models</a> by the ordinary powering 

$$
  sSet^{op} \times [C^{op}, sSet] \to [C^{op}, sSet]
  \,,
$$

which is just objectwise the [[internal hom]] in [[sSet]]. Therefore the $(\infty,1)$-topos theoretical homotopy sheaves of an object in $([C^{op}, sSet]_{loc})^\circ$ are given by the following construction:

For $X \in [C^{op}, sSet]$ a presheaf, write 

* $\pi_0(X) \in [C^{op},Set]$ for the presheaf of connected components;

* $\pi_n(X) = \coprod_{[x] \in \pi_0(X)} \pi_n(X,x)$ for the presheaf of [[simplicial homotopy group]]s with $n \geq 1$;

* $\bar \pi_n(X) \to \bar \pi_0(X)$ for the [[sheafification]] of these presheaves.

Then thes $\bar \pi_n(X) \to \bar \pi_0(X)$ are the sheaves of categorical homotopy groups of the object represented by $X$.

This definition of homotopy sheaves of [[simplicial presheaves]] is familiar from the Joyal-Jardine [[local model structure on simplicial presheaves]]. See for instance [page 4](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=4) of [Jard07](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf).

> this needs more discussion


## References

The intrinsic $(\infty,1)$-theoretic description is the topic of section 6.5.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The model in terms of the [[model structure on simplicial presheaves]] is duscussed for instance in

* Jardine, _Simplicial presheaves_ ([page 4](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=4))


[[!redirects categorical homotopy groups in an (∞,1)-topos]]
