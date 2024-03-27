+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Lie groupoid_ is a [[groupoid]] [[internal groupoid|internal]] to [[smooth manifolds]]. This is a joint generalization of [[smooth manifolds]] and [[Lie groups]] to [[higher differential geometry]].

Regarded in the more general context of [[smooth groupoids]]/[[smooth stacks]], Lie groupoids present certain well-behaved such objects, often called _[[differentiable stacks]]_.

## Definition

+-- {: .num_defn #ExplicitDefinition}
###### Definition

A _Lie groupoid_ $X \coloneq (X_1 \rightrightarrows X_0)$ is a [[groupoid]] such that both the space of arrows $X_1$ and the space of objects $X_0$ are smooth manifolds, all structure maps are smooth,  and source and target maps $s, t: X_1\rightrightarrows X_0$ are surjective submersions. 

=--

A _Lie groupoid_ $X$ is an [[internal groupoid]] in the [[category]] [[Diff]] of [[smooth manifolds]]. 

Since [[Diff]] does not have all [[pullbacks]], to ensure that this definition makes sense, one needs to ensure that the space $X_1 \times_{s,t} X_1$ of composable [[morphism]]s is an object of [[Diff]]. This is achieved either by adopting the definition of [[internal groupoid]] in the sense of Ehresmann, which includes as data the [[smooth manifold]] of [[composable pairs]], or by taking the conventional route and demanding that the source and target maps $s,t : X_0 \to X_1$ are [[submersion]]s. This ensures the [[pullback]] exists to define said manifold of composable pairs. Therefore a definition used in most modern differential geometry literature is as we see above.

But for most practical purposes, the apparently evident [[2-category]] $Grpd(Diff)$ of such internal groupoids, [[internal functor]]s and internal [[natural transformation]]s is _not_ the correct 2-category to consider. One way to see this is that the [[axiom of choice]] fails in [[Diff]], which means that an internal functor $X \to Y$ of internal groupoids which is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]] may nevertheless not be an equivalence, in that it may not have a weak inverse in $Grpd(Diff)$.

See the section [2-Category of Lie groupoids](#2CatOfGrpds) below.

A bit more general than a Lie groupoid is a [[diffeological groupoid]].


### Examples for Lie groupoids

* A Lie group $G$ is a Lie groupoid with $X_1=G$ and $X_0=pt$ a point. Composition of $X$ is provided by the multiplication of $G$.

* A manifold $M$ is a Lie groupoid with $X_1=M$ and $X_0=M$. Source and target maps are identities and we only have identity arrows in this example.

* Given a manifold $M$ and an open cover $\{U_i\}$, we can form a Lie groupoid with $X_1=\sqcup U_i\times_M U_j$ and $X_0=\sqcup U_i$. Then for an element $x_{ij}:=(x_i, x_j)\in U_i\times_M U_j \subset X_1$, $t(x_{ij})=x_i \in U_i$, $s(x_{ij})=x_j \in U_j$, and $x_{ij} \cdot x_{jk}= x_{ik}$. This is sometimes called the [[Čech groupoid]] or **covering groupoid**.

* Given a Lie group $G$ (right) action  on a manifold $M$, then we may form an associated [[action groupoid]] (or sometimes called **transformation groupoid**) as follows: $X_1 = M \times G$ and $X_0=M$. For an element $(x, g) \in X_1$, we have $t(x, g) = x$, $s(x, g)=x\cdot g^{-1}$,  and $(x, g)\cdot (y, h) = (x, g\cdot h)$ (we must have $y=x\cdot g^{-1}$ for the multiplication to happen). Action groupoid presents the quotient stack $[M/G]$. Roughly speaking, it is a good replacement for quotient space even if the action is not as nice as you want. 

* Given a manifold $M$, we may also form so-called [[pair groupoid]]: $X_1= M\times M$ and $X_0=M$. Source and target are projections, and multiplication is given by $(x, y) \cdot (y , z)= (x, z)$. Pair groupoid may be interpreted as the global object of tangent bundle (think why? see the section below on Lie algebroid).

* Given a manifold $M$, we have also an associated [[fundamental groupoid]] or **homotopy groupoid** $\Pi(M)$: $\Pi(M)_1=\{$paths in $M\}/$ homotopies, $\Pi_0(M)=M$. Source and target are end points of a path. Multiplication is concatenation of paths (think why associative?). 

* Given a manifold $M$ with a [[foliation]] $F$, we may form various groupoids associated with $F$. 

1. **$F$-pair groupoid**: $X_1:=\{(x, y)| x, y \;\text{are in the same leaf in}\; F \}$, $X_0=M$. Source and target are obvious projections and multiplication is like in the case of pair groupoid. The problem for this groupoid is that it might not be  a Lie groupoid. (why not? for counter example, we refer to [Section 13.5 of Geometric Models for
Noncommutative Algebras](https://math.berkeley.edu/~alanw/Models.pdf) ). 
  
1. **monodromy groupoid $Mon_F(M)$** (it is a foliation version of fundamental groupoid, thus it is also sometimes called $F$-fundamental groupoid): $X_1:=\{$ leaf-wise paths$\}/$ leaf-wise homotopy, $X_0=M$ and the rest is like in the case of fundamental groupoid.

1. **[[holonomy groupoid]] $Hol_F(M)$**: $X_1:=\{$ leaf-wise paths$\}/$ holonomy,
$X_0=M$ and the rest is like in the case of fundamental groupoid. Here, the holonomy of a path $\gamma$ is defined to the germ of diffeomorphisms induced by $\gamma$ between the transversals at the end points.

Among all possible Lie groupoids associated to a foliation, monodromy groupoid is the biggest and holonomy groupoid is the smallest.


### Terminology

Originally Lie groupoids were called (by Ehresmann) _differentiable groupoids_ (and also one considered differentiable _categories_). Sometime in the 1980s there was a change of terminology to _Lie groupoid_ and [[differentiable stack]]s. (reference?)



### Specialisations

One definition which Ehresmann introduced in his paper _Cat&#233;gories topologiques et cat&#233;gories diff&#233;rentiables_ (see below) is that of [[locally trivial category|locally trivial groupoid]]. It is defined more generally for topological categories, and extends in an obvious way to topological groupoids, and Lie categories and groupoids. For a topological (resp. Lie) category $X$, let $X_1^{iso}$ denote the subspace (resp. submanifold) of invertible arrows . (This always exists, by general abstract nonsense - I should look up the reference, it's in Bunge-Pare I think - [[David Roberts|DR]])

+-- {: .num_defn}
###### Definition 
A topological groupoid $X_1 \rightrightarrows X_0$ is **locally trivial** if for every point $p\in X_0$ there is a neighbourhood $U$ of $p$ and a lift of the inclusion $\{p\} \times U \hookrightarrow X_0 \times X_0$ through $(s,t):X_1^{iso}\to X_0 \times X_0$. 
=--

Clearly for a Lie groupoid $X_1^{iso} = X_1$. It is simple to show from the definition that for a transitive Lie groupoid, $(s,t)$ has local sections. Ehresmann goes on to show a link between smooth [[principal bundles]] and transitive, locally trivial Lie groupoids. See [[locally trivial category]] for details.

### The (2,1)-category of Lie groupoids {#2CatOfGrpds}


As usual for internal categories, the naive 2-category of internal groupoids, [[internal functor]]s and internal [[natural transformation]]s is not quite "correct". One sign of this is that the [[axiom of choice]] fails in [[Diff]] so that an internal functor which is an [[essentially surjective functor]] and a [[full and faithful functor]] may still not have an internal weak inverse.

One way to deal with this is to equip the 2-category with some structure of a [[homotopical category]] and allow morphisms of Lie groupoids to be [[anafunctor]]s, i.e. [[span]]s of internal functors $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$.

Such generalized morphisms -- called _[[Morita morphisms]]_ or _generalized morphisms_ in the literature -- are sometimes modeled as [[bibundle]]s and then called [[Hilsum-Skandalis morphism]]s.

Another equivalent approach is to embed Lie groupoids into the context of [[2-topos]] theory:

The [[2-topos|(2,1)-topos]] $Sh_{(2,1)}(Diff)$ of [[stack]]s/[[2-sheaves]] on [[Diff]] may be understood as a nice [[2-category]] of general groupoids _modeled on_ [[smooth manifold]]s. The degreewise [[Yoneda embedding]] allows to emebed groupoids internal to $Diff$ into stacks on $Diff$. this wider context contains for instance also [[diffeological groupoid]]s.

Regarded inside this wider context, Lie groupoids are identified with [[differentiable stack]]s. The [[(n,r)-category|(2,1)-category]] of Lie groupoids is then the full sub-$(2,1)$-category of $Sh_{(2,1)}(Diff)$ on differentiable stacks.

For more comments on this, see also the beginning of [[∞-Lie groupoid]].

## Lie algebroid

As the [[infinitesimal space|infinitesimal]] approximation to a [[Lie group]] is a [[Lie algebra]], so the infinitesimal approximation to a Lie groupoid is a [[Lie algebroid]].  


+-- {: .num_defn}
###### Definition 
A Lie algebroid is a vector bundle $A\to M$ together with a vector bundle morphism $\rho: A\to TM$ (called anchor map), and a Lie bracket $[-,-]$ on the space of sections of $A$, satisfying the Leibniz rule

$[X, fY]=f[X,Y]+\rho(X)(f) Y. $ 
=--
+-- {: .num_defn}
###### Remark
You would expect  $\rho$ to preserve $[-,-]$, wouldn't you? It is actually automatic! (see Y. Kosmann-Shwarzbah and F. Magri. Poisson-Nijenhuis strutures. Ann. Inst.
H. Poinar&#233; Phys. Th&#233;or., 53(1):3581, 1990.)

Recent progress: it turns out that one may link Lie algebroid with $L_\infty$-spaces (ask Owen Gwilliam for it) 
=--

### Examples of Lie algebroids

* A Lie algebra is a Lie algebroid with base space being a point.

* $0$-bundle over a manifold $M$ is certainly a Lie algebroid in a trivial way.


* [[action Lie algebroid]]

* Tangent bundle $TM\to M$ is a Lie algebroid with $\rho=id$ and $[-,-]$ the usual Lie bracket for vector fields. See [[tangent Lie algebroid]].

* Given a [[Poisson manifold]] $P$ with Poisson bivector field $\pi$, the cotangent bundle $T^*P$ is equipped with a Lie algebroid structure: $\rho(\xi)=
\pi(\xi)$ and $[\xi_1, \xi_2]=d\pi(\xi_1, \xi_2)$ (or you may have $[df, dg]=d\{ f, g\}$ if you prefer to think in Poisson bracket). See [[Poisson Lie algebroid]].

* [[Atiyah Lie algebroid]]



## Morphisms of Lie groupoids 
 {#MorphismsOfLieGroupoids}

There are several versions of Lie groupoid morphisms, some of them are equivalent in a correct sense, some of them are not.

* strict morphism: a strict morphism from Lie groupoid $X$ to $Y$ is a functor from $X$ to $Y$ as categories and preserving the smooth structures. 

* generalised morphism: a generalised morphism from $X$ to $Y$ is a [[span]] of morphisms $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$, where $\hat X \stackrel{\simeq}{\rightarrow} X$ is a [[weak equivalence]] of Lie groupoids, defined as below (see also at _[[bibundle]]_).

A Lie groupoid functor $f : G\to H$ is a  **weak equivalence** if it is

1. essentially surjective; that is, $t \circ pr_2 : G_0 \times_{H_0,s} H_1 \to H_0$ is a surjective submersion; 

1. fully faithful; that is,  $G_1 \cong H_1\times_{t\times s, H_0\times H_0} G_0 \times G_0$. 

Composition of generalised morphism is given by weak [[pullback]] of Lie groupoids (see also [[weak limit]]). Given  (strict) morphisms $\hat X\to Y$ and $\hat X' \to Y$, the **weak [[pullback]]** of $\hat X\to Y$ along $\hat X' \to Y$ is a groupoid $\hat X \times_{Y}^w \hat X'$ with space of objects $\hat X_0 \times_{ Y_0} Y_1 \times_{Y_0} \hat X'_0$ and space of morphisms $\hat X_1 \times_{Y_0} Y_1 \times_{Y_0} \hat X'_1$. When $\hat X' \to Y$ is a weak equivalence, the weak pullback is a Lie groupoid thank to the property of essentially surjective. (Is this composition associative?)


* [[anafunctor]]: an anafunctor from $X$ to $Y$ is a [[span]] of morphisms $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$, where $\hat X \stackrel{\simeq}{\rightarrow} X$ is an [[acyclic fibration]] of Lie groupoids. That is, this map is a [[weak equivalence]] of Lie groupoids and $\hat X_0 \to X_0$ is a surjective submersion.

Composition of anafunctors is given through strong [[pullback]] of Lie groupoids, that is level-wise pullback.


* [[bibundle]] functor (or H.S. bibundle, or Hilsum-Skandalis bibundle): a bibundle functor from $G\to H$ is a [[groupoid principal bundle]]  $E$ of $H$ (with right action) such that $G$ acts on $E$ from left and $G$ action commutes with $H$ action. If both $G$ and $H$ actions are principal, then $E$ gives arise to [[Morita equivalence]] between them.

The last three morphisms are more or less equivalent, that is they give arise to equivalent 2-categories (in fact (2,1)-categories) of Lie groupoids. To make it explicit, we need to talk about [[2-morphism]]s between them. 

A [[2-morphism]] between bibundle functors is simply a bibundle isomorphism (of course preserving all the structures of bibundles). 

A strict [[2-morphism]] from generalised morphism $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$ to $X \stackrel{\simeq}{\leftarrow} \hat X' \to Y$ is given by a morphism $\hat X \to \hat X'$ such that  the following diagram commutes
$$
\begin{matrix}
  &          & \hat X \\
  & \swarrow &           & \searrow \\
X &          & \downarrow &          & Y \\
  & \searrow &           & \swarrow \\
  &          & \hat X'
\end{matrix}
$$
This forces the morphism $\hat X \to \hat X'$ to be a weak equivalence by [[2-out-of-3]] for weak equivalences. A [[2-morphism]] from $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$ to $X \stackrel{\simeq}{\leftarrow} \hat X' \to Y$ is provided by a [[span]] of strict 2-morphisms:

$$
\begin{matrix}
  &          & \hat X \\
  & \swarrow &     \uparrow      & \searrow \\
X &          & \hat X'' &          & Y \\
  & \searrow &       \downarrow    & \swarrow \\
  &          & \hat X'
\end{matrix}
$$


A [[2-morphism]] between [[anafunctor]]s are defined like above, however the left legs are required to be [[acyclic fibration]]s between Lie groupoids.  (think this time what may you say about the morphism $\hat X \to \hat X'$?)

Then these three (2,1)-categories, which we denote by $GEN$, $ANA$ and $BUN$, are  all **[[equivalent]]** to each other. For a nice survey on this statement, we refer to Section 1.5 of [Du Li's thesis](http://ediss.uni-goettingen.de/handle/11858/00-1735-0000-0022-5F4F-A). 


The idea is that  [Bundlisation](http://ncatlab.org/nlab/show/bibundle#bundlisation) may extend to an equivalence of $(2,1)$-categories between $GEN$, the $(2,1)$-category made by generalised morphisms,  and $BUN$. The inverse is given by the following construction: given a bibundle functor $E: G\to H$, we pull back $G$ along the map $E\to G_0$ and obtain a Lie groupoid $G|_E:=G_1\times_{G_0\times G_0} E \times E \Rightarrow E$. Then the natural projection  $G|_E \to G$ is an [[acyclic fibration]]. Thus we obtain a generalised morphism which is also an anafunctor from $G \to H$. 

Even though $GEN$ contains more morphisms than $ANA$, a generalised morphism maybe equivalently replaced by an anafunctor. In fact a generalised morphism $X \stackrel{\simeq}{\leftarrow} \hat X \to Y$  gives arise to an anafunctor $X \stackrel{\simeq}{\leftarrow} X \times_{X}^w \hat X \to Y$. 

As a consequence of the universal property of the [[calculus of fractions]], $GEN$ and $ANA$ are equivalent.  


## Morphisms of Lie algebroids

Morphisms of Lie algebroids are counter-intuitive: they are not morphisms of vector bundles which preserve the algebroid structure. To define a Lie algebroid morphism, we first need to introduce the _Chevalley-Eilenberg algebra_ associated to a Lie algebroid $A$.

We consider $A$ to be a trivially graded vector bundle, i.e. concentrated in degree $0$. Then $A[1]$ is concentrated in degree $-1$.
The functions on $A[1]$ are given as
$$C(A[1])=C^\infty(M)\oplus \Gamma(A^*)\oplus \Gamma(\wedge^2 A^*)\oplus \ldots ,$$
where $C^\infty(M)$ is considered to be of degree $0$, $\Gamma(A^*)$ to be of degree $1$, and so forth.

Now we can define a degree-one derivation on $C(A[1])$ as follows: For $\xi \in \Gamma(\wedge^n A^*)$ and $X_i\in \Gamma(A)$, let
$$
d_A(\xi)(X_1,\,\ldots\,,\,X_n) := \sum_{0\leq i \lt j\leq n} (-1)^{i+j} \xi\bigl([X_i,\,X_j]_A,\, \ldots\,,\, \widehat{X_i},\,\ldots\,,\,\widehat{X_i},\,\ldots\bigr) + \sum_{i=0}^n (-1)^i \rho_A(X_i) \xi\bigl(\ldots\,,\,\widehat{X_i},\,\ldots\bigr).
$$
The condition $[d_A,\,d_A] = 0$ is not automatically fulfilled: since $\deg d_A = 1$, we have $[d_A,\,d_A] = d_A \circ d_A + d_A \circ d_A = 2 d_A \circ d_A$. 
The condition $d_A \circ d_A = 0$ is actually equivalent to $\bigl(A, \rho_A, [ - , - ]_A\bigr)$ being a Lie algebroid; that is, it is fulfilled if and only if

 * $[- , - ]_A$ satisfies the Jacobi identity
 * and $[ - , - ]_A$ and $\rho_A$ together satisfy the Leibniz identity.

(Proof: calculation gives the restriction $d_A(f) = \rho^\ast(d f)$
and $d_A(\xi)(X_1, X_2) 
 = - \bigl\langle \xi, [X_1, X_2]\bigr\rangle 
   + \rho_A(X_1)(\xi X_2) - \rho_A(X_2)(\xi X_1)$
and $d_A(\xi)(X_1, X_2, X_3) 
 = - \xi([X_1, X_2], X_3) + \xi([X_1, X_3], X_2) - \xi([X_2, X_3], X_2)
   + \rho_A(X_1)\xi(X_2, X_3) - \rho_A(X_2)\xi(X_1, X_3) + \rho_A(X_3)\xi(X_1, X_2)$.)

This point of view also applies to [[higher Courant Lie algebroids]] and [[L-infinity-algebra]]s.

Example: For the tangent Lie algebroid $A = T M$, $\bigl(C(T M[1]), d_A\bigr) = \bigl(\Omega^\ast(M), d_{dR}\bigr)$.

Then a morphism from a Lie algebroid $(A, \rho_A, [-,-]_A)$ to $(B, \rho_B, [-,-]_B)$ is a morphism of the associated differential graded commutative algebras

$$ (C(A[1]), d_A) \leftarrow (C(B[1]), d_B).
$$

Such a morphism of c.d.g.a.'s is determined by maps $C^\infty(N) \to C^\infty (M)$ on degree $0$ and a map $\Gamma(B^*)\to \Gamma(A^*)$ on degree $1$. Thus a morphism of vector bundles $A\xrightarrow{f} B$ give rise to a morphism $f^*$ of c.g.a. For $f$ to be a Lie algebroid morphism, we further need $f$ to  satisfy additional conditions so that $f^*$ preserves the differential.

This way to explain morphisms of Lie algebroids is described in [[Kirill Mackenzie]], chapter 4.3.
If the Lie algebroids are over the same manifold $M$, then a morphism from $A$ to $B$ can be described as a morphism of vector bundles that respects the anchor maps and the Lie bracket. If, however, $B$ is over a different manifold $N$, this direct approach does not work. In this situation we have to pull back the Lie algebroid to $M$ (Note that this is not simply the vector bundle pullback of $B$ along $f$, but a more involved construction, see [[Kirill Mackenzie]]). Using the defintion of a morphism on a common base manifold one arrives at two conditions on the bundle morphism to be a morphism of Lie algebroids. For details see the linked book.



### Example
Let $I$ be an interval with the tangent bundle Lie algebroid $(TI, \id_{TI}, [-,-])$ and $(A, \rho_A, [-,-]_A)$ an arbitrary Lie algebroid on $M$. Then a path $a\colon I \to A$ defines a map from $\varphi\colon C(A[1]) \to C(TI[1]) \cong \Omega(I)$ which respects the commutative graded algebra structure. A function $f\in C^{\infty}(M)$ gets mapped to $f\circ \gamma$, where $\gamma\colon I \to M$ is the projection of $a$. A section $s\in\Gamma(A^*)$ gets mapped to $(s\circ \gamma (a) dt$ under $\varphi$, where $dt$ is the canonical section of $\Omega^1(I)$. Since $C(TI[1])$ is concentrated in degree $0$ and $1$, the other degrees get mapped to $0$.

For this map to be a morphism of Lie algebroids, it has to respect the differentials. As explained above this only needs to be checked for a smooth function in $C^{\infty}(M)$:

$$ \varphi(d_A f) = d_{dR} \varphi(f) \qquad f\in C^{\infty}(M).
$$

A quick calculation shows that this is true if and only if

$$ \rho_A(a(t)) = \frac{d}{dt}\gamma(t).
$$

### Example
Let $M$ the unit square in $\mathbb{R}^2$. Then a Lie algebroid morphism from $(TM, \id_{TM}, [-,-])$ to $(\mathfrak{g}, T\cdot, [-.-]_{\mathfrak{g}})$, where $\mathfrak{g}$ is a Lie algebra, is given by a morphism of c.d.g.a.

$$ (CE(\mathfrak{g}), d_{\mathfrak{g}}) \to (\Omega(M), d_{dR}).
$$

Two smooth maps $a,b\colon M\to \mathfrak{g}$ give a map between c.g.a. spaces above. Here a section $s\in\Gamma(\mathfrak{g}^*)$, i.e. an element of $\mathfrak{g}^*$ gets mapped to the one form

$$ s(a) dt + s(b) ds,
$$

where $(t,s)$ are the coordinates on $M$. A quick calculation shows that this map respects the differential if and only if

$$ \frac{da}{ds} - \frac{db}{ds} = [a,b]_{\mathfrak{g}}.
$$

This formula also shows that $a\cdot dt + b\cdot ds$ is a flat connection on the trivial principal $G$-bundle on $M$. Therefore Lie algebroid morphisms open a way to talk about higher connections and flat conditions.

### Open problem
It is unclear how to use the idea of [[bibundle]] or [[span]] to define a more general version of Lie algebroid morphisms so that they really correspond to the case of Lie groupoid morphisms.
 


## Higher Lie groupoids

See

* [[internal ∞-groupoid]]

* [[∞-Lie groupoid]]

## Examples

* Every [[smooth manifold]] $X$ is a 0-[[0-groupoid|truncated]] Lie groupoid.

* For every [[Lie group]] $G$ the one-object [[delooping]] groupoid $\mathbf{B}G$ is a Lie groupoid.

* The Lie group $G$ itself is a 0-[[truncated]] [[group object]] in the 2-category or Lie groupoids.

* Every [[Lie 2-group]] is in particular a Lie groupoid: a [[group object]] in the category of Lie groupoids.

* The [[inner automorphism 2-group]] $\mathbf{E}G = INN(G) = G//G$ is a Lie groupoid. There is an obvious morphism $\mathbf{E}G \to \mathbf{B}G$.

* For every $G$-[[principal bundle]] $P \to X$ there is its [[Atiyah Lie groupoid]] $At(P)$.


* The [[fundamental groupoid]] $\Pi_1(X)$ of a smooth manifold is naturally a Lie groupoid.

* The [[path groupoid]] of a smooth manifold is naturally a [[diffeological groupoid]].

* The [[Cech groupoid]] $C(U)$ of a [[cover]] $\{U_i \to X\}$ of a smooth manifold is a Lie groupoid. 

* Every [[foliation]] gives rise to its [[holonomy groupoid]].

* An [[orbifold]] is a Lie groupoid.

* An [[anafunctor]] $X \stackrel{\simeq}{\leftarrow} C(U) \to \mathbf{B}G$ from a smooth manifold $X$ to $\mathbf{B}G$ is a [[Cech cohomology|Cech cocycle]] in degree 1 with values in $G$, classifying $G$-[[principal bundle]] $P$.

* The (1-categorical) [[pullback]]

  $$
    \array{
       P &\stackrel{\simeq}{\leftarrow}& \mathbf{P} &\to& \mathbf{E}G
       \\
       && \downarrow && \downarrow
       \\
       && C(U) &\stackrel{}{\to}& \mathbf{B}G
       \\
       && \downarrow^{\mathrlap{\simeq}}
       \\
       && X
    }
  $$

  is a Lie groupoid equivalent to this principal bundle $P$.

  (For more on the general phenomenon of which this is a special case see [[principal ∞-bundle]] and [[universal principal ∞-bundle]].)

* Similarly an anafunctor from $P_1(X)$ to $\mathbf{B}G$ is a [[connection on a bundle]] (see there for details).

## Related concepts

* [[smooth groupoid]], [[smooth functor]]

* [[LieGrpd]], [[SmoothGrpd]]

* [[bisection of a Lie groupoid]]

* [[orbifold]]

* [[effective Lie groupoid]], [[proper Lie groupoid]], [[etale groupoid]]

* [[homotopy groups of a Lie groupoid]]

* [[Morita morphism]], [[Hilsum-Skandalis morphism]]

* [[Tannaka duality for Lie groupoids]]

* [[double Lie groupoid]]

* [[higher differential geometry]]

## References

The notion of Lie categories, hence of Lie groupoids, goes back to 

* [[Charles Ehresmann]], _Catégories topologiques et categories différentiables_, Colloque de Géométrie différentielle globale, Bruxelles, C.B.R.M., (1959) pp. 137-150 ([[EhresmannCategoriesTopologiques.pdf:file]], [zbMath:0205.28202](https://zbmath.org/?q=an:0205.28202))

Their understanding as [[internal categories]]/[[internal groupoids]] [[internalization|in]] [[SmoothManifolds]] is often attributed to

* [[Charles Ehresmann]], _Catégories structurées_, Annales scientifiques de l'École Normale Supérieure, Série 3, Tome 80 (1963) no. 4, pp. 349-426 ([numdam:ASENS_1963_3_80_4_349_0](http://www.numdam.org/item/ASENS_1963_3_80_4_349_0))

but the simple notion of [[internalization]] and [[internal groupoids]] ([Grothendieck 1960](internalization#Grothendieck60), [61](internalization#Grothendieck61)) is hardly recognizable in this account.

Textbook accounts:

* [[Kirill Mackenzie]], _Lie groupoids and Lie algebroids in differential geometry_, London Mathematical Society Lecture Note Series, 124. Cambridge University Press, Cambridge, 1987. xvi+327 pp ([doi:10.1017/CBO9780511661839](https://doi.org/10.1017/CBO9780511661839), [MR:896907](http://www.ams.org/mathscinet-getitem?mr=896907))

* {#MoerdijkMrcun03} [[Ieke Moerdijk]], [[Janez Mrčun]] _Introduction to Foliations and Lie Groupoids_, Cambridge Studies in Advanced Mathematics 91, Cambridge University Press, 2003  ([doi:10.1017/CBO9780511615450](https://doi.org/10.1017/CBO9780511615450))

  > (in the context of [[foliation theory]]: [[foliation groupoids]])

* [[Kirill Mackenzie]], _General Theory of Lie Groupoids and Lie Algebroids,_ Cambridge University Press, 2005 ([doi:10.1017/CBO9781107325883](https://doi.org/10.1017/CBO9781107325883))

Historical review:

* [[Jean Pradines]], _In [[Ehresmann]]'s footsteps: from Group Geometries to Groupoid Geometries_, Banach Center Publications, vol. 76, Warsawa 2007, 87-157 ([arXiv:0711.1608](http://arxiv.org/abs/0711.1608), [doi:10.4064/bc76-0-5 ](https://www.impan.pl/en/publishing-house/banach-center-publications/all/76/0/86184/in-ehresmann-s-footsteps-from-group-geometries-to-groupoid-geometries))


The relation to [[differentiable stacks]] is discussed/reviewed in section 2 of

* {#Blohmann} [[Christian Blohmann]], _Stacky Lie groups_, Int. Mat. Res. Not. (2008) Vol. 2008: article ID rnn082 ([arXiv:math/0702399](http://arxiv.org/abs/math/0702399))
 

Lie groupoids as a source for [[groupoid convolution algebras|groupoid convolution]] [[C*-algebras]] are discussed in 

* [[Alain Connes]], _[[Noncommutative Geometry]]_

Review:

* [[John Baez]]  _[TWF](http://math.ucr.edu/home/baez/TWF.html) [256](http://math.ucr.edu/home/baez/week256.html)_

* [[Alan Weinstein]], _Groupoids: Unifying Internal and External Symmetry -- A Tour through some Examples_, Notices of the AMS **43** 7 (1996) &lbrack;[pdf](http://www.ams.org/notices/199607/weinstein.pdf), [[Weinstein_Groupoids.pdf:file]]&rbrack;

* [[Henrique Bursztyn]], Matias del Hoyo, *Lie Groupoids*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2309.14105](https://arxiv.org/abs/2309.14105)&rbrack;

Groupoids and their various morphisms between them in different categories, including in Diff, is also in

* Ralf Meyer and [[Chenchang Zhu]], _Groupoids in categories with pretopology_,  [arXiv:math/1408.5220](http://arxiv.org/pdf/1408.5220.pdf)

[[!redirects Lie groupoids]]