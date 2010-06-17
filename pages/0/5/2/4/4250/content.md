
<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>


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




## Properties

### In $\infty Grpd$

For the case that $\mathbf{H} = $ [[∞Grpd]] $\simeq$ [[Top]], the $(\infty,1)$-topos theoretic definition of categorical homotopy groups in $\mathbf{H}$ reduces to the ordinary notion of [[homotopy group]]s in [[Top]]. For $\infty Grpd$ modeled by [[Kan complex]]es or the standard [[model structure on simplicial sets]], it reduces to the ordinary definition of [[simplicial homotopy group]]s.

### Connected and truncated objects

Let $X \in \mathbf{H}$.

* The object $X$ is **$n$-[[truncated]]** if it is a [[n-truncated object in an (∞,1)-category|k-truncated object]] for some $k \gt n$ and if all its categorical homotopy groups above degree $n$ vanish.

  Every object decomposes as a sequence of $n$-truncated objects: the 
  [[Postnikov tower in an (∞,1)-category]].

* The object $X$ is **$n$-[[connected]]** if the terminal morphism 
  $X \to *$ is an [[effective epimorphism]] and if all categorical homotopy groups below degree $n$ are trivial.

* The object $X$ is an **[[Eilenberg-MacLane object]]** of degree $n$ if it is both $n$-connected and $n$-truncated.

## Models

When the [[(∞,1)-topos]] $\mathbf{H}$ is [[presentable (∞,1)-category|presented]] by a [[model structure on simplicial presheaves]] $[C^{op}, sSet]_{loc}$, then since this is an [[sSet]]-[[enriched model category]] structure the [[power]]ing by $\infty Grpd$ is modeled by the ordinary powering 

$$
  sSet^{op} \times [C^{op}, sSet] \to [C^{op}, sSet]
  \,,
$$

which is just objectwise the [[internal hom]] in [[sSet]]. Therefore the $(\infty,1)$-topos theoretical homotopy sheaves of an object in $([C^{op}, sSet]_{loc})^\circ$ are given by the following construction:

For $X \in [C^{op}, sSet]$ a presheaf, write 

* $\pi_0(X) \in [C^{op},Set]$ for the presheaf of connected components;

* $\pi_n(X) = \coprod_{[x] \in \pi_0(X)} \pi_n(X,x)$ for the presheaf of [[simplicial homotopy group]]s with $n \geq 1$;

* $\bar \pi_n(X) \to \bar \pi_0(X)$ for the [[sheafification]] of these presheaves.

Then thes $\bar \pi_n(X) \to \bar \pi_0(X)$ are the sheaces of categorical homotopy groups of the object represented by $X$.

This definition of homotopy sheaves of [[simplicial presheaves]] is familiar from the Joyal-Jardine [[local model structure on simplicial presheaves]]. See for instance [page 4](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=4) of [Jard07](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf).




## References

The intrinsic $(\infty,1)$-theoretic description is the topic of section 6.5.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The model in terms of the [[model structure on simplicial presheaves]] is duscussed for instance in

* Jardine, _Simplicial presheaves_ ([page 4](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf#page=4))


[[!redirects categorical homotopy groups in an (∞,1)-topos]]
