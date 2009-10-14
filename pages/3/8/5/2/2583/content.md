
> **under construction**

#Idea#

Just as the ([[delooping]] of the) topological [[string group]] is the element above the  (delooping of the) [[Spin group]] in the [[Whitehead tower]] of $\mathcal{B} O(n)$ inside the [[(infinity,1)-topos]] [[Top]]

$$
 (
  \cdots
  \to
  \mathcal{B} String(n)
  \to 
  \mathcal{B} Spin(n)
  \to \mathcal{B}SO(n) \to \mathcal{B}O(n)
  )
  \in Top
  \,,
$$
+--{: .query}
[[David Roberts]]: This is the Whitehead tower of $BO(n)$, not that of $O(n)$. The string group sits in the tower for the latter.

[[Urs Schreiber]]: sure, that's what's meant. Fixed the phrasing above now.

=--

so the (delooping of the) **string 2-group** is the [[Whitehead tower]] element above the delooping of $Spin(n)$, but now regarded in an [[(infinity,1)-topos]] $\mathbf{H}$ of smooth [[infinity-groupoid]]s:



$$
 (
  \cdots
  \to
  \mathbf{B} String(n)
  \to 
  \mathbf{B} Spin(n)
  \to 
  \mathbf{B}SO(n) 
  \to 
  \mathbf{B}O(n)
  )
  \in \mathbf{H}
  \,.
$$


+--{: .query}
[[David Roberts]]: And by this I presume it is meant the tower of the delooping of $O(n)$ in $\mathbf{H}$.

[[Urs Schreiber]]: Sure. I added paranthetical remarks accordingly.

=--

It is in $\mathbf{H}$ the [[homotopy fiber]] of the morphism

$$
  \frac{1}{2}p_1
  :
  \mathbf{B} Spin(n)
  \stackrel{}{\to}
  \mathbf{B}^3 U(1)
$$

that is the smooth [[group cohomology|group cocycle]] that integrates the normalized canonical [[Lie algebra cohomology|Lie algebra 3-cocycle]] $\mu_3 \in CE(\mathfrak{so}(n))$.

**Remark.** Notice that in the existing literature the smooth [[group cohomology|group cocycles]] of a [[Lie group]] are _defined_ to be simplicial morphisms out of 

$$
  (\cdots  G\times G\stackrel{\stackrel{\to}{\to}}{\to}G\stackrel{\to}{\to}{*})
  \,.
$$

With that definition, $\frac{1}{2}p_1$ does _not exist_ as a smooth cocycle. But, while that definition is copied verbatim from the correct definition in [[Top]], it is **not the right general definition** for smooth [[group cohomology]]. Instead, the right definition is given by  the [[category theory|general nonsense]] of [[cohomology]] in an [[(infinity,1)-topos]] $\mathbf{H}$:
 a smooth [[group cohomology|group cocycle]] on the [[Lie group]] $G$ is a morphism out of its [[delooping]] but regarded in $\mathbf{H}$. This $\mathbf{H}$ in turn is [[models for infinity-stack (infinity,1)-toposes|modeled]] by [[simplicial presheaves]] which for the present purposes we may assume to be [[simplicial object|simplicial]] [[diffeological space]]s. But in that context there are considerably "bigger" resolutions of $\mathbf{B}G$ than the one above. (In fact the one above is just $\mathbf{B}G$ in $\mathbf{H}$ itself). The 3-cocycle $\frac{1}{2}p_1$ is a morphism out of one of these bigger resolutions. More on that below.

...

So the string 2-group is a smooth [[2-group]] incarnation of...


#References#

* Henriques

* BCSS

* Schommer-Pries

* ...

[[!redirects String 2-group]]
[[!redirects String Lie 2-group]]
[[!redirects string Lie 2-group]]