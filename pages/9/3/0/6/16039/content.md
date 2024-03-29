
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

* table of contents
{:toc}

Generalized higher loop spaces are analogs of [[loop spaces]] adapted to the setting of [[overconvergent global analytic geometry]].

## Overview

Recall that one may define higher Hochschild homology of a derived scheme as functions on its completed formal higher loop space
$$\hat{L}^n X:=\widehat{Hom}_{dSt}(S^n,X).$$
There is a natural action of the symmetry group of $S^n$ on this space. One may try to define analogs of this construction for other symmetry groups, at least on a local field, to try to use these spaces to study representation theory.

The basic idea here is to start with the non-strict analytic space $GL_n$, and look at the mapping space
$$L_{GL_n}X:=Hom_{dSt}(GL_n,X).$$
It may only be definable for usual spaces, not Artin stacks, but one has to check that.

In any case, there is a natural (in the setting of [[generalized global analytic geometry]]) subgroup $U(n)\subset GL_n$, and one may also consider
$$L_{U(n)}X:=\widehat{Hom}_{dSt}(U(n),X).$$
Normally, since $U(n)$ is proper, this space is finite dimensional in the differential stacky sense. One may then define linear and unitary higher Hochschild cohomology of dimension $n$ to be given by functions on the moduli spaces
$$M_{GL_n}X:=[L_{GL_n}X/GL_n]$$
and
$$M_{U(n)}X:=[L_{U(n)}X/U(n)].$$
Up to $D^1$-homotopy, both spaces should be identical. Now the unitary moduli space has a strict global definition, which means it is a very rigid object (essentially, a kind of Arakelov stack, given by a scheme-moduli stack together with an archimedean structure).

The determinant map $det:GL_n\to GL_1$ induces a natural morphism
$$det^*:L_{GL_n}X\to L_{GL_1}X,$$
which may give also a morphism
$$det^*:M_{GL_n}X\to M_{GL_1}X.$$

Remark now that there exists an exact sequence of (non-strict) analytic groups
$$1\to U(1)\to GL_1\to N_1\to 1$$
where $N$ is the group of norms of elements in $GL_1$. In dimension $n$, we
only have a groupoid $N_n$. However, there is always the possibility to define a new
moduli space given by
$$D_{GL_n}X:=[L_{GL_n}X/U(n)].$$

This moduli space is equipped with an action of the groupoid $N_n$. In dimension $1$ over $C$, if $X$ is, say, projective, we get, as functions on $D_{GL_1}(X)$, a (probably infinite dimensional) space over $C$ together with an action of $N_1\cong \mathbb{R}_+^*$. In the $p$-adic situation, we have $N_1=p^\mathbb{Z}$. On a global field, one may work over adeles to get a sensible construction.

One should also not forget that there is (in characteristic $0$, e.g., on adeles of $\mathbb{Q}$) a logarithm map
$$log:\overset{\circ}{D}(1,1)_{GL_1}\to Lie(GL_1)$$
that allows us to relate the above constructions to the notion of [[generalized lambda-structure]].

## Relation with usual Hochschild and cyclic homology

Remark that, even over $\mathbb{C}$, the $D^1$-homotopy invariant version of $M_{U(1)}X$ is not equivalent to the (simplicial) loop space $L^1 X$. Indeed, to get a sensible relation between our moduli spaces and loop spaces (i.e., usual Hochschild and negative cyclic homology), one has to be very careful: inverting $D^1$ is not the right thing to do because it just gives usual loops up to homotopy, not the derived ones, which are necessary for differential constructions. A nice way to circumvent this problem is given by the following construction: let $R$ and $S$ be two base ind-Banach ring, and consider the category of derived stacks on $R$ with values in the (say) stable $D^1$-homotopy category of usual stacks over $S$. If we start with $S=\mathbb{C}$ and $R=(\Z,|\cdot|_0)$, we get a setting that is appropriate for explaining the relation between derived loop spaces and generalized higher loop spaces. Indeed, one may see $GL_n$ as a constant derived stack given by the associated group object of the $D^1$-homotopy category, denoted $GL_n^c$. Then the corresponding moduli space $M^c_{GL_n}X$ is related to the derived loop space in the case $n=1$: they are homotopy equivalent because the $D^1$-homotopy category over $C$ is equivalent (following Ayoub) to the usual homotopy category of simplicial sets.

If one wants to avoid getting back the usual loop space, one may work with the category
$$Shv(DAff^\dagger_S\times SAff^\dagger_R,{}^\infty Grpd)$$
of sheaves of sheaves on smooth affinoid spaces over $R$ on derived affinoid algebras over $S$. This may be seen as an extension of scalars of the $\infty$-category of derived analytic stacks over $S$ along the inclusion of infinity-groupoids into usual analytic higher stacks over $R$ (that form a presentable infinity-category, so that the tensor product operation works).

Recall that we may define two types of linear group stack-valued derived stacks by setting, for $(A,B)\in DAff^\dagger_S\times SAff^\dagger_R$, the constant linear stack to be defined associated to the prestack
$$GL_n^c(A,B)=GL_n(B),$$
and the usual derived analytic stack
$$GL_n^d(A,B)=GL_n(A).$$
Having a derived and a non-derived direction seems to be quite important. Indeed, the derived direction is needed for doing differential calculus, and the non-derived direction is needed for doing $D^1$-homotopy theory. Combining the two may give an optimal setting for relating generalized loop spaces with usual derived loop space.

There is a relation between the homotopy and classical generalized higher loop spaces given by the following: if we assume given a morphism $R\to S$, we may define the diagonal (extension of scalars) functor
$$\Delta:SAff^\dagger_R\longrightarrow DAff^\dagger_R\times SAff^\dagger_S,$$
to get a natural morphism of stack-valued derived stacks induced by
$$
\Delta^*GL_n^d(A)\cong GL_n(A)\longrightarrow GL_n(A_S)\cong\Delta^*GL_n^c(A).
$$

We may now define a version of the generalized higher loop spaces that is directly related to Hochschild cohomology: we may define
$$
L^{dc}_{GL_n}(X):=
\{(f,g)\in Hom(GL_n^d,X)\times Hom(GL_n^c,X),\; \Delta^*f\cong \Delta^* g\}.
$$
This means that we are choosing (for $n=1$), for every classical derived loop $g:GL_n^c\to X$ (up to $D^1$-homotopy, say), a corresponding generalized derived loop $f:GL_n\to X$, that we may call its representative. Forgetting the representative gives back the usual derived loop spaces if $R=(\Z,|\cdot|_0)$ and $S=(\C,|\cdot|_\infty)$, and $X$ is a derived scheme over $\Z$, and forgetting the classical derived loop gives the generalized higher derived loop space defined at the beginning of this page. We thus have two projections
$$L^d_{GL_n}X\leftarrow L^{dc}_{GL_n}(X)\to L^c_{GL_n}(X)$$
that may be used to define a correspondence between modules on the generalized higher derived loop space and on the classical derived loop space.

## Related entry

[[overconvergent derived loop spaces]]