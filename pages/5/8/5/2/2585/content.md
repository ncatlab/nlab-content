#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In the [[(∞,1)-topos]] [[Top]] to every object -- every [[topological space]] -- $X$ is associated 
the set $\pi_0(X)$ of connected components and the [[homotopy group]]s $\pi_n(X,x)$ for $x \in X$ and $n \in \mathbb{N}$, $n\gt 0$.

By the general logic of [[space]], we may think of the objects in an arbitrary [[∞-stack]] [[(∞,1)-topos]] as generalized spaces of sorts. Accordingly, there is a notion of **homotopy groups of an $\infty$-stack** .

But care has to be taken. It turns out that there are actually _two_ different notions of homotopy groups in an arbitrary $(\infty,1)$-topos, two notions that accidentally coincide for [[Top]]:

* there is a notion of **categorical homotopy group**: 

  every $(\infty,1)$-topos $\mathbf{H}$ is [[power]]ed over [[∞Grpd]] [[model structure on simplicial sets|usually modeled]] as [[SSet]], hence for every object $X \in \mathbf{H}$ there is the **categorical $n$-sphere object** $X^{S^n_c}$, where $S^n_c = \Delta^n/\partial \Delta^n$. 

* there should be a notion of **geometric homotopy group**, induced from the [[monodromy]] of [[locally constant ∞-stack]]s on objects $X \in \mathbf{H}$.

For instance let $\mathbf{H} = Sh_{(\infty,1)}(Diff)$ be the $(\infty,1)$-topos of [[Lie ∞-groupoid]]s. An ordinary smooth [[manifold]] $X$ is represented in $\mathbf{H}$ by a [[sheaf]] of [[set]]s on [[Diff]]. This has no higher nontrivial categorical homotopy groups -- $\pi_{n \gt 0}^{cat}(X) = 0$ -- reflecting the fact regarded as a smooth [[∞-groupoid]], $X$ is a categorically [[discrete groupoid]].

But of course the manifold $X$ may have nontrivial [[homotopy group]]s in terms of its underlying [[topological space]]. For instance if $X = S^1$ is the circle, then the _geometric_ first homotopy group is nontrivial, $\pi_1^{geom}(X) = \mathbb{Z}$.

We discuss below both cases. The case of categorical homotopy groups is fully understood, for the case of geometric homotopy groups at the moment only a few aspects are in the literature, more is in the making. Some authors of this page ([[Urs Schreiber|U.S.]]) thank [[Richard Williamson]] for pointing this out.

## Categorical homotopy groups

### Definition

Every [[∞-stack]] [[(∞,1)-topos]] $\mathbf{H}$ is naturally
[[power]]ed over [[∞Grpd]] ([[Higher Topos Theory|HTT, remark 5.5.2.6]]):

for every [[∞-groupoid]] $K$ and every object $A \in \mathbf{H}$ there is an object $A^K \in \mathbf{H}$ such that for every object $X \in \mathbf{H}$ there is
an equivalence

$$
  \mathbf{H}(X,A^K) \simeq \infty Grpd(K, \mathbf{H}(X,A))
  \,.
$$ 

Let $S^n := Ex^\infty \partial \Delta[n+1]$ be the [[Kan fibrant replacement]] of the [[boundary of a simplex|boundary of the (n+1)-simplex]], i.e. the model in [[∞Grpd]] of the [[pointed object|pointed]] $n$-[[sphere]].

For every $X \in \mathbf{H}$, evaluation at the base point induces a morphism

$$
  s : X^{S^n} \to X
  \,.
$$

This morphism may be regarded as an object of the [[over category]] [[(∞,1)-topos]] $\mathbf{H}/X$.

For $n \in \mathbb{N}$ define

$$
  \pi_n(X) := \tau_{\leq 0} s \in \mathbf{H}/X
$$

to be the discrete (i.e. [[n-truncated object of an (infinity,1)-topos|0-truncated]]) object obtained from $s$.

As in classical [[homotopy theory]], for $n \geq 1$ the object $\pi_n(X)$ is equipped with the structure of a [[group object]] in $\mathbf{H}/X$, which is an abelian group object for $n \geq 2$.

**Remark** The [[n-truncated object of an (infinity,1)-topos|0-truncated]] objects in $\mathbf{H}/X$ have the interpretation of [[sheaf|sheaves]] on $X$. So in the world of [[∞-stack]]s a homotopy [[group object]] is a [[sheaf]] of groups.



### References

section 6.5.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_



## Geometric homotopy groups {#Geometric}

### Idea

Let $C$ be some [[site]] and let $\mathbf{H} = Sh_{(\infty,1)}(C)$ be the [[(∞,1)-topos]] of [[∞-stack]]s over $C$. We think of objects $X \in \mathbf{H}$ as generalized [[space]]s modeled on $C$.

We have a squence of [[adjunction]]s

$$
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh_{(\infty,1)}(C)
  \stackrel{\overset{const}{\leftarrow}}{\to}
  PSh_{(\infty,1)}(*)
  =
  \infty Grpd 
  :
  LConst
$$

where on the left we have the defining adjunction of the [[(∞,1)-category of (∞,1)-sheaves]] -- $L$ is [[∞-stackification]] -- and on the right the [[geometric morphism]] that is induced from the canonical morphism of [[site]]s $C \to {*}$ (to the [[terminal object|terminal]] site).

The [[constant ∞-stack]] $\infty CovBund := LConst(Core(\infty Grpd)) \in \mathbf{H}$ is the classifying stack for [[locally constant ∞-stack]]s on objects $X \in \mathbf{H}$. We write

$$
  \infty CovBund(X) := \mathbf{H}(X,\infty CovBund)
$$ 

for the $\infty$-groupoid of [[locally constant ∞-stack]]s on $X$.

If the [[left adjoint]] $LConst$ is also a [[right adjoint]] 

$$
  (\Pi \dashv LConst)
  :
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Pi}{\to}}
  \infty Grpd   
$$

then we have from the [[adjunction]] that locally constant $\infty$-stacks on $X$ are equivalently given by [[(∞,1)-functor|∞-functors]] from the [[∞-groupoid]] $\Pi(X)$ to $\infty FinGrpd$:

$$
  \infty CovBund(X) \simeq Func(\Pi(X),\infty Grpd)
  \,.
$$

In $\mathbf{H} = $ [[Top]], this is the relation satisfied by the [[fundamental ∞-groupoid]] $\Pi(X)$ of a [[topological space]] $X$. Accordingly here in a general $(\infty,1)$-topos $\mathbf{H}$ we may think of the functor $\Pi : \mathbf{H} \to \infty Grpd$ as giving for each generalized [[space]] its geometric [[schreiber:path ∞-groupoid]] of geometric paths in it.

Accordingly, then, we may think of the ordinary [[homotopy group]]s of $\Pi(X)$ as the **geometric homotopy groups** of $X \in \mathbf{H}$.


### By monodromy

We describe how, given the existence of 
a [[left adjoint] $\Pi : Sh_{(\infty)}(C) \to \infty Grpd$ to $LConst : \infty Grpd \to Sh_{(\infty,1)}(C)$ as described above, the geometric homotopy groups of an object $X \in Sh_{(\infty,1)}(C)$ may be found in the [[automorphism]] [[∞-group]] of a fiber functor $F_x :  CovBund(X) \to \infty Grpd$ -- these automorphism are called the **monodromy** of $X$.

By adjunction we have

$$
  CovBund(X) \simeq \infty Grpd(\Pi(X), \infty Grpd)
  \,.
$$

From this we learn that for $x : * \to X$ any point of $X$ we have a morphism

$$
  F_x = CovBund(X) \to \infty Grpd
$$

given by precomposition of objects in $\infty Grpd(\Pi(X), \infty Grpd)$
with $x : * \to \Pi(X)$.

Let $\Omega_x \Pi(X)$ be the [[loop space object]] of $\Pi(X)$ at $X$. We have a canonical embedding of this [[∞-group]] into the automorphism $\infty$-group of $F_x$

$$
  \Omega_x \Pi(X) \hookrightarrow Aut_{Sh_{(\infty,1)}(X)}(F_x)
$$

given by precomposition: the object of $\Omega_x \Pi(X)$ given by 

$$
  \array{  
     & \nearrow \searrow^{\mathrlap{x}}
     \\
    {*} &\Downarrow^{\ell}& \Pi(X)
    \\
    & \searrow \nearrow_{\mathrlap{x}}
  }
$$

is sent to the automorphism of $F_x$ whose component on an object $E \in CovBund(X) \simeq [\Pi(X),\infty Grpd]$ is

$$
  \array{  
     & \nearrow \searrow^{\mathrlap{x}}
    \\
    {*} &\Downarrow^{\ell}& \Pi(X) &\stackrel{E}{\to}& \infty Grpd
    \\
    & \searrow \nearrow_{\mathrlap{x}}
  }
  \,.
$$


> [[Urs Schreiber]]: now one needs to argue that all automorphisms of $F_x$ arise this way, up to equivalence. Looking at what this all means for naturality squares on low degree morphisms that seems to be right to me, but I am not sure yet how to give a general formal argument.



### History {#GeometricHistory}

The idea that geometric homotopy groups of generalized [[space]]s given by [[sheaf|sheaves]], [[stack]]s, [[∞-stack]]s is detected and definable by the behaviour of locally constant sheaves, stacks, $\infty$-stacks on these objects goes back to [[Grothendieck's Galois theory]] and the notion of [[fundamental group of a topos]]. In [[Pursuing Stacks]] [[Alexander Grothendieck|Grothendieck]] talked about how this 1-categorical situation generalizes to [[∞-stack]]s. 

After _Pursuing Stacks_, apparently the first to publish a detailed formalization and proof of how the [[homotopy group]]s of a [[topological space]] $X$ may be recovered from the behaviour of [[locally constant ∞-stack]]s on $X$ was 

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))

Very similar constructions and statement then appeared in 

* [[Pietro Polesello]] and [[Ingo Waschkies]], _Higher monodromy_ , Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150 ([pdf](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf)) 

* [[Mike Shulman]], _Parametrized spaces model locally constant homotopy sheaves_ ([arXiv:0706.2874](http://arxiv.org/abs/0706.2874))

and, building on that, in example 1.8 of

* [[Denis-Charles Cisinski]], _Locally constant functors_ , Math. Proc. Camb. Phil. Soc. , 147 ([pdf](http://www-math.univ-paris13.fr/~cisinski/lcmodcat3.pdf))

It was pointed out by [[Richard Williamson]] that the construction should generalize from topological spaces to objects in any [[(∞,1)-topos]], maybe along the lines outlined above, and that this way every $(\infty,1)$-topos $\mathbf{H}$ comes canonically equipped with a notion of bare [[schreiber:path ∞-groupoid]] $\Pi(X)$ of every object $X \in \mathbf{H}$.




### Examples {#Examples}


#### Geometric $\Pi_0$ of a sheaf on a topological space {#Pi0Ofsheafontopspace}

Here we discuss the 0-th geometric homotopy group $\Pi_0 : Sh(X) \to Set$ of objects in a [[Grothendieck topos|sheaf topos]] in terms of a [[left adjoint]] $\Pi_0$ of the [[constant sheaf]] functor.

> [[Urs Schreiber]]: this here should be evident, but I can't see it in the literature. For the terminal sheaf (the topological space itself), it is a special case of the statements in terms of higher stacks that follow.

Let $X$ be a sufficiently nice [[topological space]]. 

+-- {: .un_theorem}
###### Claim

There is a triple of [[adjoint functor]]s

$$
  (\Pi_0 \dashv LConst \dashv \Gamma) \;\;\;
  :
  \;\;\; Sh(X) \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  Set
$$

where 

* $(LConst \dashv \Gamma)$ is the usual [[global section]] [[geometric morphism]] with $LConst_S$ the [[constant sheaf]] of [[locally constant function]]s with values in $S \in Set$ and 

* $\Pi : Sh(X) \to Set$ is [[left adjoint]] to $LConst$ and sends each sheaf $A$ to the set of connected components of the corresponding [[etale space]] $p_A : Et(A) \to X$:

  $$
    \Pi_0(A) = \pi_0 Et(A)
    \,.
  $$

=--

+-- {: .proof}
###### Proof


The [[etale space]] of $LConst_S$ is $E(LConst_S) = X \times S$. By the relation of [[sheaves]] on $X$ with [[etale space]]s over $X$ we have

$$
  Hom_{Sh(X)}(A, LConst_S) 
  \simeq
  Hom_{Et/X}(E(A), X \times S)
$$

For $\gamma : I \to E(A)$ any continuous path in $E(A)$, and for $f : E(A) \to X \times S$ a morphism in $Et/X$, the image of $\gamma$ in $X \times I$ is fixed by, say, the image $f(\gamma(0)) = (p_A(\gamma_0),s)$ to be $f(\gamma) : t \mapsto (p_A(\gamma(t)),s)$. This means that the value of $f$ on any path component of $E(A)$ is uniquely fixed by its value on any point in that path component.

Choosing a basepoint in each path component therefore induces  bijection

$$
  \simeq Hom_{Set}(\pi_0(Et(A)), S) = Hom_{Set}(\Pi_0(A),S)
  \,.
$$


=--


#### Geometric $\pi_1$ of objects in a 1-topos

The general idea is that of 

* [[Grothendieck's Galois theory]]. 

A discussion of of how this produces first homotopy groups of a 1-[[topos]] is at

* [[fundamental group of a topos]].

The general construction of the first geometric homotopy group of objects in a [[Grothendieck topos]] is for instance in section 8.4 of

* [[Peter Johnstone]], _Topos theory_ .


#### Geometric $\Pi_2$ of a topological space

This case is discussed in 

* [[Pietro Polesello]] and [[Ingo Waschkies]], _Higher monodromy_ , Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150 ([pdf](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf)) 

We indicate briefly how the results stated in this article fit into the general abstract picture as indicated above:

The authors consider locally constant 1-stacks and 2-stacks on sites of open subsets of sufficiently nice [[topological space]]s.

Prop. 1.1.9 gives the [[adjunction]]

$$
  (LConst \dashv \Gamma) : Sh_{(2,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}} Grpd
$$

between forming constant stacks and taking global sections.

Then prop 1.2.5, 1.2.6, culminating in 
[theorem 1.2.9, p. 121](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf#page=13) gives (somewhat implicitly) the other adjunction

$$
  (\Pi_1\dashv LConst) : Op(X) \hookrightarrow Sh_{(2,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Pi_1}{\to}} Grpd
$$

with the [[right adjoint]] to $LConst$ being the [[fundamental groupoid]] functor on representables. (Where we change a bit the perspective on the results as presented there, to amplify the pattern indicated above. For instance where the authors write $\Gamma(X,C_X)$ we think of this here equivalently as $Sh_{(2,1)}(X)(X,LConst(C))$, so that the theorem then gives the adjunction equivalence $\cdots \simeq Grpd(\Pi_1(X),C)$).

Then in essentially verbatim analogy, these results are lifted from stacks to 2-stacks in section 2, where now prop 2.2.2, 2.2.3, culminating in [theorem 2.2.5, p. 132](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf#page=24) gives (somewhat implicitly) the adjunction

$$
  (\Pi_2\dashv LConst) : Op(X) \hookrightarrow Sh_{(3,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Pi_3}{\to}} Grpd
$$

now with the [[path n-groupoid|path 2-groupoid]] operation (locally) left adjoint to forming constant 2-stacks.




#### Geometric $\Pi_\infty$ of a topological space {#ooStackOnTopSpace}


 Let $X$ be a sufficiently nice (I think this should be locally (relatively) contractible. -DR) ([[paracompact space|paracompact]]) [[topological space]]. The canonical map $X \to {*}$ induces the [[geometric morphism]]

$$
  Sh_{(\infty,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

where the [[right adjoint]] $\Gamma$ is taking [[global section]]s and the [[left adjoint]] is forming the [[constant ∞-stack]] on an $\infty$-groupoid $K$. If $K = Core (\infty Grpd)$ then $LConst_K$ is the [[constant ∞-stack]] of [[locally constant ∞-stack]]s and we write

$$
  LConst(X) := Sh_{(\infty,1)}(X, LConst_{\infty Grpd})= \Gamma LConst_{\infty Grpd}
$$

for the $\infty$-groupoid of locally constant $\infty$-stacks on $X$.

Write $ \Pi(X) := Sing X$ for the [[fundamental ∞-groupoid]] of $X$.

+-- {: .un_theorem}
###### Claim

There is an equivalence of $\infty$-groupoids

$$
  LConst(X) \simeq \infty Grpd(\Pi(X), \infty Grpd)
  \,.
$$

=--

> [[Urs Schreiber]]: I think this is proven in the literature, if maybe slightly implicitly so. I'll now go through the available references to discuss this.


After old ideas by [[Alexander Grothendieck]] from [[Pursuing Stacks]], it seems that the first explicit formalization and proof of this statement is given in 

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))

In [theorem 2.13, p. 25](http://arxiv1.library.cornell.edu/PS_cache/math/pdf/0007/0007157v4.pdf#page=25) the author proves an equivalence of [[(∞,1)-categories]] (modeled there as [[Segal category|Segal categories]])

$$
  LConst(X) \simeq Fib(\Pi(X))
$$

of [[locally constant ∞-stack]]s on $X$ and [[Kan fibration]]s over the [[fundamental ∞-groupoid]] $\Pi(X) = Sing(X)$.

By the right Quillen functor $Id : sSet_{Quillen} \to sSet_{Joyal}$ from the Quillen [[model structure on simplicial sets]] to the [[Joyal model structure on simplicial sets]] every Kan fibration is a categorical fibration and every categorical fibration over a [[Kan complex]] is a [[Cartesian fibration]] (as discussed there) and a coCartesian fibration. Finally, by the [[Grothendieck construction|(∞,1)-Grothendieck construction]], these are equivalent to [[(∞,1)-functor]]s $\Pi(X) \to \infty Grpd$.

In total this means that via the [[Grothendieck construction]] To&#235;n's result does actually produce an equivalence

$$
  LConst(X) \simeq Func(\Pi(X), \infty Grpd)
  \,.
$$

Very similar statements are discussed in

* [[Mike Shulman]], _Parametrized spaces model locally constant homotopy sheaves_ ([arXiv:0706.2874](http://arxiv.org/abs/0706.2874))

and, building on that, in example 1.8 of

* [[Denis-Charles Cisinski]], _Locally constant functors_ , Math. Proc. Camb. Phil. Soc. , 147 ([pdf](http://www-math.univ-paris13.fr/~cisinski/lcmodcat3.pdf))


A variant of this statement -- more general in one respect, less general in another -- appears in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

as [theorem 7.1.0.1](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=545). 

There it is shown that for any $K \in \infty Grpd$ there is a bijection of homotopy sets of morphisms

$$
  \pi_0 Top(X, |K|) \simeq \pi_0(p_* p^* K)
  \,,
$$

where $(p^* \dashv p_*) : Sh_{(\infty,1)}(X) \to \infty Grpd$ is the geometric morphism we denoted $(LConst \dashv \Gamma)$ above. 

If we also rewrite the left using [[homotopy hypothesis|the equivalence]] of $Top$ with $sSet$, this reads

$$
  \pi_0 \infty Grpd(\Pi(X), K) \simeq \pi_0(\Gamma LConst_K)
  = \pi_0 Sh_{(\infty,1)}(X,LConst_K)
  \,, 
$$

For $K = Core(\infty Grpd)$ this is the $\pi_0$-[[decategorification]] of the above statement.







[[!redirects homotopy group of an infinity-stack]]
[[!redirects homotopy group of an ∞-stack]]
[[!redirects homotopy groups of an infinity-stack]]
[[!redirects homotopy groups of an ∞-stack]]
[[!redirects homotopy groups of infinity-stacks]]
[[!redirects homotopy groups of ∞-stacks]]
[[!redirects homotopy group (of an infinity-stack)]]
[[!redirects homotopy group (of an ∞-stack)]]
[[!redirects homotopy groups (of an infinity-stack)]]
[[!redirects homotopy groups (of an ∞-stack)]]
[[!redirects homotopy groups (of infinity-stacks)]]
[[!redirects homotopy groups (of ∞-stacks)]]

[[!redirects fundamental group of an infinity-stack]]
[[!redirects fundamental group of an ∞-stack]]
[[!redirects fundamental groups of infinity-stacks]]
[[!redirects fundamental groups of ∞-stacks]]
