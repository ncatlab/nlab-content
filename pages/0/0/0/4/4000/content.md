
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $G$ a [[Lie group]], $\mathcal{B}G \in $ [[Top]] the corresponding [[classifying space]] and $c \in H^4(\mathcal{B}G, \mathbb{Z})$ a [[cocycle]] (in integral [[singular cohomology]]), what is called a **Chern-Simons 2-gerbe** with class $c$ is effectively a refinement to [[differential cohomology]] of $c$, i.e. a realization of the idea

* a smooth $\mathbf{B}^2 U(1)$-[[principal infinity-bundle|principal 3-bundle]] "on $\mathcal{B} G$";

* equipped with a smooth [[connection on a bundle|connection]].

More generally, for $P \to X$ a smooth $G$-[[principal bundle]] over a [[smooth manifold]] $X$ and classified by a map $\phi : X \to \mathcal{B}G$, the *Chern-Simons 2-gerbe associated to $P$* is the pullback of the given 2-gerbe on $\mathcal{B}G$ to $X$ along $\phi$.

Of course this does not quite make sense as stated, as $\mathcal{B}G$ is not _naturally_ a [[smooth space]]. There are some tricks to regard it as a limit of [[smooth manifold]]s. But more properly, from the [[nPOV]], the above can neatly be made sense of if we incarnate $\mathcal{B}G$ in an [[(∞,1)-topos]] richer than [[Top]] $\simeq$ [[∞Grpd]], for instance the $(\infty,1)$-topos of [[∞-Lie groupoid]]s, given as the [[(∞,1)-category of (∞,1)-sheaves]] on the [[site]] [[CartSp]]: $\mathbf{H} := Sh_{(\infty,1)}(CartSp)$.

In there, the [[Lie group]] $G$ naturally exists as a [[diffeological space]] and, being a [[group object in an (∞,1)-category|group object]] it has a [[delooping]] $\mathbf{B}G$ in the standard [[model category]] presentation of $Sh_{(\infty,1)}(CartSp)$ in terms of the [[model structure on simplicial presheaves]] $sPSh(CartSp)_{proj,loc}$. This is simply the [[simplicial object|simplicial]] [[diffeological space]] 

$$
  \mathbf{B}G
  = 
  \left(
    \cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}}G \stackrel{\to}{\to}
    *
  \right)
  \in 
  [\Delta^{op}, Diff]
  \hookrightarrow
  [\Delta^{op}, PSh(CartSp)]
  \,.
$$

Moreover, $\mathbf{H}$ is a [[locally contractible (∞,1)-topos]] and under the corresponding [[homotopy groups in an (∞,1)-topos|homotopy ∞-groupoid]] [[(∞,1)-functor]] $|-| : \mathbf{H} \stackrel{\Pi}{\to} \infty Grpd \stackrel{\simeq}{\to} Top$ we have the topological [[geometric realization]] $|\mathbf{B}G| \simeq \mathcal{B}G$, so that in this sense $\mathbf{B}G$ is indeed a smooth refinement of $\mathcal{B}G$.

Given that, one needs to make sense of smooth bundle 2-gerbes on [[∞-Lie groupoid]]s in order to define Chern-Simons bundle 2-gerbes. Effectively this involves smooth [[equivariant cohomology]].  This is -- more or less implicitly -- what is done in much of the literature.

## Relation to Chern-Simons theory

One may understand the Chern-Simons 2-gerbe on $\mathbf{B}G$ as the background [[gauge field]] for [[Chern-Simons theory]]. Moreover, when pulled back via a classifying map $\phi : X \to \mathbf{B}G$ for a smooth $G$-bundle, it serves as the background gauge field for the quantum membrane (the 3-dimesional [[sigma-model]]) on $X$. In this incarnation it is also known as the [[supergravity C-field]].

## References

An approach to the underlying cocycle of a Chern-Simons 2-gerbes in terms of [[Cech cohomology]] originates in 

* [[Jean-Luc Brylinski]] and [[Dennis McLaughlin]], _A geometric construction of the first Pontryagin class_ (1993) ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Brylinski-McLaughlin-I.pdf))

A related approach in terms of [[gerbe]]s properly in terms of [[stack]]s is

* [[Jean-Luc Brylinski]] and [[Dennis McLaughlin]], _The geometry of degree-4 characteristic classes and of line bundles on loop spaces II_ ([pdf](http://www.math.uni-hamburg.de/home/schreiber/Brylinski-McLaughlin-Duke-II.pdf)).

Among the first references apply [[bundle gerbe]] technology to reffinements of the 4-class on $\mathcal{B}G$ to [[differential cohomology]] is

* [[Alan Carey]] and [[Stuart Johnson]] and [[Michael Murray]] and [[Danny Stevenson]] and [[Bai-Ling Wang]], _Bundle gerbes for Chern-Simons and Wess-Zumino-Witten theories_ Communications in Mathematical Physics, 259 (3). (2005) ([arXiv]())

This was later refined in 

* [[Konrad Waldorf]], _Multiplicative Bundle Gerbes with Connection_ ([arXiv:0804.4835](http://arxiv.org/abs/0804.4835))

Here are some slides from talks:

* [[Konrad Waldorf]], _Multiplicative gerbes and Chern-Simons theory_ ([pdf](http://www.konradwaldorf.de/docs/bonn.pdf))

* [[Krzysztof Gawedzki]], _Wess-Zumino-Witten and Chern-Simons theories for non-simply connected Lie groups_ ([pdf](http://dftuz.unizar.es/ftzar/activities/highenergy09_talks/gawedzki.pdf))

[[!redirects Chern-Simons 2-gerbes]]