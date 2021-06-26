
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
#### Stabe homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Mapping space
+-- {: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Loop space objects
* tic
{: toc}

## Idea

In the [[(∞,1)-topos]] [[Top]] the construction of a [[loop space]] of a given [[topological space]] is familiar.

This construction may be generalized to any other [[(∞,1)-topos]] and in fact to any other [[(∞,1)-category]] with [[homotopy pullbacks]].


## Definition

Loop space objects are defined in any [[(∞,1)-category]] $\mathbf{C}$ with [[homotopy pullbacks]]: for $X$ any [[pointed object]] of $\mathbf{C}$ with point ${*} \to X$, its [[loop space object]] is [[generalized the|the]] [[homotopy pullback]] $\Omega X$ of this point along itself:

$$
  \array{
    \Omega X &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    {*} &\to& X
  }
  \,.
$$

A ([[generalised element|generalised]]) [[global point|element]] of $\Omega X$ may be thought of as a [[loop]] in $X$ at the [[base point]] $*$.


### Remarks

Since $\mathbf{C}(X,-)$ commutes with homotopy limits, one has a natural homotopy equivalence $\Omega\mathbf{C}(X,Y)\simeq \mathbf{C}(X,\Omega Y)$, for any two objects $X$ and $Y$ in $\mathbf{C}$.

See also 

* [[fibration sequence]]

* [[delooping]]

* [[stable (∞,1)-category]]


## Explicit constructions

Usually the [[(∞,1)-category]] in question is [[presentable (infinity,1)-category|presented]] by concrete 1-categorical data, such as that of a [[model category]]. In that case the above [[homotopy pullback]] has various realizations as an ordinary [[pullback]].

Notably it may be expressed using [[path objects]] which may come from [[interval objects]]. Even if the context is not (or not manifestly) that of a [[homotopical category]], an [[interval object]] may still exist and may be used as indicated in the following to construct loop space objects.

### Free loop space objects

In a category with [[interval object]] $ * \xrightarrow{0} T \xleftarrow{1} * $ the 
**free loop space object** is the part of the [[path object]] $B^I = [I,B]$ which consists of closed paths, namely the [[pullback]]
\begin{tikzcd}
  \Lambda B \ar[r]\ar[d]           & {}[I,B]  \ar[d, "d_0 \times d_1"] \\
  B         \ar[r, "\mathrm{Id} \times \mathrm{Id}"] & B \times B
\end{tikzcd}
where $ d_0 $ ($d_1$ resp.) is the composition of $ [0,B] $ ($[1,B]$ resp.) with the canonical identification of $[*, B]$ and $B$.

This is the same as the image of the [[co-span co-trace]] $cotr(I)$  of the interval object (which is the interval object closed to a loop!,  see the examples at [[co-span co-trace]]) in $B$:

$$
  \left[
  \array{
     && cotr(I)
     \\
     & \nearrow && \nwarrow
     \\
     pt &&&& I
     \\
     & {}_{Id \sqcup Id}\nwarrow && \nearrow_{in \sqcup out}
     \\
     && pt \sqcup pt
  }
  \;\;\;\;,\;\;\;\;
  B
  \right]
  \;,\;\;\;\;
  \simeq
  \;,\;\;\;\;
  \array{
     && \Lambda B
     \\
     & \swarrow && \searrow
     \\
     B &&&& [I,B]
     \\
     & {}_{Id \times Id}\searrow && \swarrow_{d_0 \times d_1}
     \\
     && B \times B
  }
$$


### Based loop space objects

If $B$ is a [[pointed object]] with point $pt \stackrel{pt_B}{\to} B$ then the **based loop space object** of $B$ is the pullback $\Omega_{pt} B$ in

$$
  \array{
    \Omega_{pt}B &\to& [I,B]
    \\
    \downarrow && \downarrow^{d_0 \times d_1}
    \\
    pt
    &\stackrel{pt_B \times pt_B}{\to}&
    B \times B
  }
  \,.
$$

#### Remarks

* $\Omega_{pt}B$ is the fiber of the [[generalized universal bundle]] $\mathbf{E}_{pt}B \to B$.

* the based loop space object $\Omega_{pt} B$ is the pullback of the free loop space object $\Lambda B$ to the point
$$
  \array{
    \Omega_{pt} B &\to& \Lambda B
    \\
    \downarrow && \downarrow
    \\
    pt &\stackrel{pt_B}{\to}& B 
  }
  \,.
$$



## Remarks

* The loop space object $B$ can be regarded as the homotopy trace on the identity span on $B$, as described at [[span trace]].

* The free loop space object inherits the structure of an $A_\infty$-[[A-infinity-category|category]] from that of the [[path object]] $[I,B]$. 

* In a [[generalized smooth space|suitable extension]] of $\operatorname{Diff}$, this construction does **not** give the usual _smooth_ loop space (free or based).  It gives the space of paths with coincident endpoints rather than the space of smooth maps from the circle.  Thus the [[smooth loop space]] is not a loop space object.

## Examples

* Let $C =$ [[Top]] with the standard [[interval object]]. Then for $B= X$ a topological space $\Lambda B = \Lambda X$ is the ordinary free [[loop space]] of $X$.

  The generalization of this to _smooth_ spaces is discussed at [[smooth loop space]].

* Let $C = $ [[Grpd]] with the standard interval object $I = \{a \stackrel{\simeq}{\to} b\}$ and let $\mathbf{B}G$ be the one-object groupoid corresponding to a group $G$, then
$$
  \Lambda \mathbf{B}G = G//_{Ad}G
$$
is the [[action groupoid]] of $G$ acting on itself by its adjoint action. Notice the example at [[co-span co-trace]] which says that the cotrace on $I$ is $cotr(I) = \mathbf{B}\mathbb{Z}$, and indeed
$$
  \Lambda \mathbf{B}G =  [\mathbf{B}\mathbb{Z}, \mathbf{B}G]  
  \,.
$$
The role of this $\Lambda \mathbf{B}G$ as a loop object is amplified in particular in

  * Simon Willerton, _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv](http://arxiv.org/abs/math.QA/0503266))

  * Bruce Bartlett, _On unitary 2-representations of finite groups and topological quantum field theory_ ([arXiv](http://arxiv.org/abs/0901.3975))

* On the other hand, the _based_ loop object of $\mathbf{B}G$ is just $G$:
$$
  \Omega \mathbf{B}G = G
  \,.
$$


## Related concepts

* **loop space object**, [[free loop space object]],

  * [[delooping]], [[looping and delooping]]

  * [[loop space]], [[free loop space]], [[derived loop space]]

  * [[inertia orbifold]]

* [[suspension object]]

  * [[suspension]], [[reduced suspension]]


[[!redirects loop space object]]
[[!redirects loop space objects]]

[[!redirects loop object]]
[[!redirects loop objects]]
[[!redirects loop space functor]]
[[!redirects loop space functors]]
[[!redirects loop functor]]
[[!redirects loop functors]]

[[!redirects based loop space object]]
[[!redirects based loop space objects]]


