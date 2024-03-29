#Contents#
* table of contents
{:toc}

## Idea

[[Microlocalization]] is a tool to study the propagation of singularities of solutions of partial differential systems, in order to study pullbacks of solutions of differential systems (which generalize products of distributions) and prove [[index theorems]].
Derived microlocalization is an adaptation of the theory of microlocalization to the setting of derived [[global analytic geometry]].

## Motivation for a derived notion of microlocalization

In non-smooth situations, the usual normal and conormal bundle used in classical microlocalization is not well behaved, and one needs to take derived versions of them. Moreover, to study [[global analytic index theory]], one needs a formulation of the theory of microlocalization in terms of derived loop stacks, in order to work out a cyclic and Hochshild version of index theorems (similar to the one developed by Kashiwara and Schapira in the [[microlocal formulation of index theory]]) that works on an arbitrary (e.g. integral) basis.

## Loop space and deformation to the normal bundle: method I

We would like to define a family over (say) the disc $D^1$ whose fiber
at $0$ is $LX:=\Hom(S^1,X)$ and whose fiber at $1$ is $[LX/S^1]$.
In the case of a usual scheme, this is done (by Vezzosi) by showing that
$LX$ identifies with $\Hom(BG_a,X)$, and by making $G_a$ act
multiplicatively on the action of $BG_a$ on $LX$, to get the trivial
action at $0$ and the usual action at $1$. This gives the desired family.
Recall that $BG_a$ is the affinization of $B\mathbb{Z}\cong S^1$.

## Loop space and deformation to the normal bundle: method II

[[Microlocalization]] in [[derived geometry]] involves the proper definition of the deformation to the [[normal bundle]] of a closed embedding $Y\subset X$ of global analytic spaces (or even stacks). One needs to consider a [[derived loop space]] approach to this construction because it allows to avoid the use of denominators in the definition of the [[Chern character]] (following Connes-Loday-Toen-Vezzosi) and in the development of more general [[global analytic index theory]] with integral coefficients.

The space of paths on $X$ based on $Y$ is the groupoid acting on $Y$ given by
$$P_Y X:=\{f\in \Hom(\Delta^1,X),\;f(0)\in Y,\;f(1)\in Y\}.$$
More concretely, this is given by the homotopy pullback
$$
\array{
    P_Y X &\to& \Hom(\Delta^1,X)
    \\
    \downarrow && \downarrow^{\mathrlap{ev_0\times ev_1}}
    \\
    Y\times Y &\to& X\times X
}
$$
Notice that the natural projection $P_Y X\to Y\times Y$ makes $P_Y X$ a groupoid (of paths in $X$) acting on $Y$. In the case of the diagonal immersion $Y=M\hookrightarrow M\times M=X$, we get
$$P_Y X\cong LM:=\Hom(S^1,M).$$

There is a natural projection $p:P_Y X\to \Hom(\Delta^1,X)\sim X$ and $P_Y X$ is equiped with the natural structure of a groupoid acting on $Y$ through the projection $P_Y X\to Y\times Y$.
A more explicit description of the loop space (that is obtained by using the homotopy $\Delta^1\sim \Delta^0$) is given by the homotopy pullback
$$P_Y X=Y\times^h_X Y,$$
which clearly has an interesting meaning only in the setting of derived geometry. See also at _[[derived loop space]]_ and at _[[Hochschild cohomology]]_.

To make the above construction work for general Artin stacks, one needs to make it local for the smooth topology. This is done by replacing the loop space groupoid $P_Y X$ acting on $Y$ by its formal completion along the identity morphism. This gives a formal groupoid $\hat{P}_Y X$ that is equivalent modulo the [[HKR]] theorem (in characteristic $0$) to $T_Y[-1]X$ for a general Artin stack. Similarly, we will have $\hat{L}M:=\hat{P}_M(M\times M)\cong T[-1]M$ by [[HKR]].

The deformation to the normal bundle in strict derived global analytic geometry is then simply given by the (**false to be corrected**) formula (with $D^1=\mathbb{M}(R\{X\}^\dagger)$ for $R$ the base ind-Banach ring)
$$
\widetilde{P_Y X}:=\{f\in \Hom_{D^1}(\Delta^1\times D^1,X\times D^1),\;f(0,0)\in Y,\; f(1,0)\in Y,\;f(-,1)\in (X\backslash Y)\Rightarrow f(x,t)\in (X\backslash Y)\forall t\neq 0\}.
$$
More concretely, this is given by the homotopy pullback (where $U(1)=\mathbb{M}(R\{X,Y\}^\dagger/(XY-1))$ and we use the homotopy equivalence $\Hom(\Delta^1,X)\sim X$)
$$
\array{
    \widetilde{P_Y X} &\to& \Hom_{D^1}(\Delta^1\times D^1,X\times D^1)
    \\
    \downarrow && \downarrow^{\mathrlap{ev_{(0,0)}\times ev_{(1,0)}\times \ev_{(-,U(1))}\times \ev_{(-,1)}}}
    \\
    Y\times Y\times \Hom(\Delta^1\times U(1),(X\backslash Y))\times (X\backslash Y) &\stackrel{i\times j\times k}{\to}& X\times X\times \Hom(\Delta^1\times U(1),X)
\times X}
$$
It has an evident natural projection $t:\widetilde{P_Y X}\to D^1$, and a natural projection $\widetilde{P_Y X}\to Y\times Y$ that makes it a family of groupoids parametrized by $D^1$ and acting on $Y$. There is also a natural projection
$p:\widetilde{P_Y X}\to X$ given by $f\mapsto f(-,1)$. We will denote $s:P_Y X\to \widetilde{P_Y X}$ the fiber $t^{-1}(0)$.

One may complete $\widetilde{P_Y X}$ along the unit of its groupoid structures, to get a family of formal groupoids $\widehat{P_Y X}$ parametrized by $D^1$, whose fiber at $0$ will be the formal loop space $\hat{P}_Y X$ obtained by completing the path groupoid $P_Y X$ acting on $Y$ along its identity morphism, and whose fiber at $1$ will be the formal completion $\hat{X}_Y$ of $X$ along $Y$. There is a natural action of $S^1$ on $\widehat{P_Y X}$. We will still denote $t:\widehat{P_Y X}\to D^1$ the natural projection, $s:\widehat{P}_Y X\to \widehat{P_Y X}$ the fiber $t^{-1}(0)$, and $p:\widehat{P_Y X}\to X$ the natural projection (evaluation at $(-,1)$).

In the particular case of the diagonal embedding $Y=M\hookrightarrow M\times M=X$ over a field of characteristic $0$, the quotient of $X$ by this family of formal groupoids gives back (modulo a convenient [[HKR]] theorem) exactly Simpson's non-abelian Hodge structure, that gives a family of formal stacks over $D^1$ whose fiber at $0$ is the tangent space $TX$ (seen as the quotient of $X$ by the trivial action of $T[-1]X$) and whose fiber at $1$ is the so-called de Rham space $X_{dR}$ of $X$.

## A derived analog of microlocalization

We now work on an arbitrary derived Artin stack $M$, such that the diagonal $Y=M\to M\times M=X$ is an affine closed embedding.

The usual theory of [[microlocalization]] may be adapted to the derived global analytic setting by replacing the deformation to the normal bundle $\widetilde{T_Y X}\to \mathbb{A}^1$ by the formal deformation to the normal bundle $\widehat{P_Y X}\to D^1$.

The derived specialization functor is given on $F\in D^b(X)$ by
$$\nu_Y(F):=s^*p^*F\in D^b(\hat{P}_Y X).$$

Remark that the loop space analog $L^*X$ of the odd cotangent bundle $T^*[1]X$ (that should be dual to the odd tangent bundle $T[-1]X$ (related to $LX$ by the [[HKR]] theorem) is given by $S^1\otimes X$ (external tensor product by the simplicial circle). We will have for every stack $Y$, the canonical equivalence
$$\Hom(S^1\otimes X,Y)\cong \Hom_{SSets}(S^1,\Hom_{dSt}(X,Y)).$$

The derived Fourier-Sato transformation is given on $F\in D^b(\hat{P}_Y X)$ by
$$\Phi(F):=?.$$

The derived microlocalization functor is given on $F\in D^b(M)$ by
$$\mu(F):=\Phi(\nu_Y(F))$$
for $Y=M\hookrightarrow M\times M=X$.

## A derived analytic analog of microlocalization

One may replace the simplicial circle $S^1$, used in the definition of the derived loop space, by the unitary group $U(1)$ of [[overconvergent global analytic geometry]], to get a more analytic theory of microlocalization. In the complex situation, we will have $U(1)\cong S^1$ up to $D^1$-homotopy. Remark that the exponential map $exp(i-):\mathbb{R}\to S^1$ also has a meaning in overconvergent complex analytic geometry, if we see $\mathbb{R}\subset \mathbb{C}$ as a closed subset equipped with its germs of analytic functions.

In the global analytic setting (without imposing homotopy invariance), there is no reason to have $U(1)=D^1\times_{*\coprod *} *$. We thus prefer to use $P^1:=D^1\coprod_{U(1)}D^1$ as a natural global analytic parameter space for paths. We define
$$L^\dagger_Y X:=\{f\in Hom(P^1,X), f(0)\in Y,\; f(\infty)\in Y\}.$$
Remark that up to $D^1_\mathbb{R}$-homotopy, we get
$$L^\dagger_Y X\sim L_Y X.$$

We must now check that the natural morphism

## References

* [[David Ben-Zvi]], [[David Nadler]], _Loops spaces and connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))

* [[Damien Calaque]], [[Andrei Caldararu]] and [[Junwu Tu]]: _PBW for an inclusion of Lie algebras_ ([arXiv:1010.0985](http://arxiv.org/abs/1010.0985))

* [[Damien Calaque]], [[Andrei Caldararu]] and [[Junwu Tu]]: _On the Lie algebroid of a derived self-intersection_ ([arXiv:1306.5260](http://arxiv.org/abs/1306.5260))