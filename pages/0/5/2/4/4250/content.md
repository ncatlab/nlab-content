
<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>


This is a sub-entry of [[homotopy groups in an (∞,1)-topos]]. 

For the other notion of homotopy groups see [[geometric homotopy groups in an (∞,1)-topos]].

#Contents#
* automatic table of contents goes here
{:toc}


## Definition

Since an [[(∞,1)-topos]] $\mathbf{H}$ has all [[limits in a quasi-category|limits]],  is naturally
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

to be the [[n-truncated object of an (infinity,1)-topos|0-truncation]] of the object $S$.

=--

As in classical [[homotopy theory]], for $n \geq 1$ the object $\pi_n(X)$ is equipped with the structure of a [[group object]] in $\mathbf{H}_{/X}$, which is an abelian group object for $n \geq 2$.

**Remark** The [[n-truncated object of an (infinity,1)-topos|0-truncated]] objects in $\mathbf{H}/X$ have the interpretation of [[sheaf|sheaves]] on $X$. So in the world of [[∞-stack]]s a homotopy [[group object]] is a [[sheaf]] of groups.


## Connected and truncated objects

Let $X \in \mathbf{H}$.

* The object $X$ is **$n$-[[truncated]]** if it is a [[n-truncated object in an (∞,1)-category|k-truncated object]] for some $k \gt n$ and if all its categorical homotopy groups above degree $n$ vanish.

  Every object decomposes as a sequence of $n$-truncated objects: the 
  [[Postnikov tower in an (∞,1)-category]].

* The object $X$ is **$n$-[[connected]]** if the terminal morphism 
  $X \to *$ is an [[effective epimorphism]] and if all categorical homotopy groups below degree $n$ are trivial.

* The object $X$ is an **[[Eilenberg-MacLane object]]** of degree $n$ if it is both $n$-connected and $n$-truncated.

## References

section 6.5.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects categorical homotopy groups in an (∞,1)-topos]]
