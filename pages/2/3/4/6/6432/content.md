[[!redirects Microlocalization]]

#Contents#
* table of contents
{:toc}

## Idea

Microlocalization is a tool invented by [[Mikio Sato]] to study linear [[partial differential equations]] (as a part of his [[algebraic analysis]] program) not only locally in space but also locally in momentum variable. It is a purely algebraic theory that was also continued in parallel by analysts, like Hormander, giving the domain of [[microlocal analysis]].

## Construction

The original construction is based on the use of the specialization functor and Fourier-Sato transformation. In this section, we will discuss the construction in a general setting, i.e., over an arbitrary field of characteristic $0$. In the real situation, one usually refines the construction by using conic sheaves (i.e., sheaves invariant with respect to the natural $\mathbb{R}_+$-action) to get information about the oriented direction of propagation of singularities of sheaves of solutions of analytic partial differential systems. The construction we describe does not treat this refined information.

Let $Z\hookrightarrow X$ be a closed subspace of a given analytic manifold, defined by a sheaf of ideals $\mathcal{I}$, with normal bundle denoted $T_Z X$ and conormal bundle denoted $T^*_Z X$. One defines the deformation to the normal bundle as the (analytic space associated to the) relative scheme over $X$ given by
$$\widetilde{T_Z X}:=Spec_X(\oplus_{i\in \mathbb{Z}} z^{-i} \mathcal{I}^i)^{an}$$
with $\mathcal{I}^i=\mathcal{O}_X$ for $i\leq 0$.
There is a projection $p:\widetilde{T_Z X}\to X$ and a projection $\tau:\widetilde{T_Z X}\to \mathbb{A}^1$. The fiber at $0$ of $\tau$ is denoted $s:T_Z X\to \widetilde{T_Z X}$, and its fiber at $t\neq 0$ is $X$. The fiber of $p$ on the open subset $(X\backslash Z)$ is $(X\backslash Z)\times \mathbb{A}^1-\{0\}$.

The specialization of a sheaf $F\in D^b(k_X)$ is the sheaf $\nu_Z(F)\in D^b(k_{T_Z X})$ defined as
$$\nu_Z(F):=s^*p^*F.$$

The Fourier-Sato transform is the functor
$$\Phi:D^b(k_{T_Z X})\to D^b(k_{T^*_Z X})$$
defined by
$$\Phi(G):=\mathbb{R}p_{2!}p_1^*G$$
where $p_1:T_Z X\times_Z T^*_Z X\to T_Z X$ and $p_2:T_Z X\times_Z T^*_Z X\to T^*_Z X$ are the two natural projections.

The $Z$-microlocalization functor is the functor
$$\mu_Z:=\Phi\circ \nu_Z:D^b(k_X)\to D^b(k_{T^*_Z X}).$$

The microlocalization functor on a variety $M$ is defined as the $Z$-microlocalization associated to the closed immersion $Z=M\subset M\times M=X$. Since $T^*_{\Delta_M} (M\times M)\cong T^*M$, this gives a functor
$$
\mu:D^b(k_M)\to D^b(k_{T^*M}).
$$

Denoting $q_1,q_2:M\times M\to M$ the natural projection, we defined the microlocal homomorphisms $\mu hom(F,G)$ between two complexes of sheaves $F$ on $G$ on $X$ by
$$\mu hom(F,G):=\mu_{\Delta_M}\mathbb{R} Hom(q_2^{-1} F,q_1^{!}G).$$

If $\pi:T^*_{\Delta_M}(M\times M)\to M$ is the natural projection, we have
$$\pi_*\mu hom(F,G)\cong \mathbb{R}Hom(F,G).$$

## Related subjects

[[index theory]]

[[microlocal formulation of index theory]]

[[global analytic index theory]]

[[derived microlocalization]]

[[algebraic microlocalization]]

## References

Sato's theory of microlocalization was first described in the setting of [[D-modules]]:

* [[M. Kashiwara]], Kawai, Kimura: foundations of algebraic analysis.

It was then extended to a purely sheaf theoretical theory in

* [[Masaki Kashiwara]], [[Pierre Schapira]], _Sheaves on manifolds_, Grundlehren **292**, Springer (1990) &lbrack;[doi:10.1007/978-3-662-02661-8](https://doi.org/10.1007/978-3-662-02661-8)&rbrack;

This theory of microlocalization of (ind)-sheaves (and also sub-analytic sheaves) was developped in the following works:

* [[Masaki Kashiwara]], [[Pierre Schapira]], _Ind-sheaves, distributions and microlocalization_, describes the program.
* [[Masaki Kashiwara]], [[Pierre Schapira]], [[Florian Ivorra]], [[Ingo Waschkies]] _Microlocalization of ind-sheaves_, gives the main results
and proofs.
* [[Masaki Kashiwara]], [[Pierre Schapira]] _Ind-sheaves_, SMF, gives a complete account of the theory.
* [[Luca Prelli]], _Microlocalization of sub-analytic sheaves_, gives the theory in the sub-analytic setting.

A good overview of the theory can by found at:

* [[Pierre Schapira]] Derived categories for the analyst (2010)