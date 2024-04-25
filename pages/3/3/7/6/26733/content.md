[[!redirects C_2-equivariant homotopy groups of spheres]]
#Content#
* table of contents
{:toc}

## Idea

[[cyclic group of order 2|$C_2$]]-[[equivariant homotopy theory|equivariant]] [[homotopy groups of spheres]] are particularly amenable to study because they are computed in a range by $\mathbb{R}$-[[motivic homotopy theory|motivic]] homotopy groups via real [Betti realization](motivic+homotopy+theory#RealizationFunctors).

(...)

## $\mathrm{RO}(G)$-graded vs Mackey functor homotopy groups

In general, for all real orthogonal virtual $G$-representations, we have a cofiber sequence of $G$-spectra 
$$
  S(V)_+ \rightarrow D(V)_+ \rightarrow S^V;
$$
In the case $V = \sigma$, we find that $S(V) = C_{2,+}$; hence there is a natural long exact sequence in stable homotopy
\begin{tikzcd}
  \cdots \arrow[r]
  & \pi_{n + \sigma}^{C_2} X \arrow[r]
  & \pi_{n}^{C_2} X \arrow[r]
  & \pi_{n}^e X \arrow[r]
  & \pi_{n-1+\sigma}^{C_2} X \arrow[r]
& \cdots;
\end{tikzcd}
in the motivic grading $\pi_{s,c}^{C_2}X \coloneqq \pi_{c + (s-c)\sigma}^{C_2} X$, this reads as 
\begin{tikzcd}
  \cdots \arrow[r]
  & \pi_{n+1,n}^{C_2} X \arrow[r]
  & \pi_{n,n}^{C_2} X \arrow[r]
  & \pi_{n,n} \mathrm{map}(C_{2+},X) \arrow[r]
  & \pi_{n,n-1}^{C_2} X \arrow[r]
& \cdots.
\end{tikzcd}

In particular, the [[five lemma]] combined with the [[ equivariant Whitehead theorem]] then proves the following (see Prop 3.2 of [Guillou-Isaksen 24](#Guillou24)).

\begin{proposition}
  A map of $C_2$-spectra induces an isomorphism on $\mathrm{RO}(C_2)$-graded homotopy groups if and only if it induces an isomorphism on $\mathbb{Z}$-graded mackey functor homotopy groups.
\end{proposition}

The corresponding theorem is seldom true for other groups, since every other group attains _two dimensional_ irreducible real orthogonal $G$-representations, whose compactifications will not be cofibers of $G$-sets.
For instance, a counterexample due to Clover May in the case $G = C_3$ appears as Ex. 3.1 of [Guillou-Isaksen 24](#Guillou24).

## Relation to motivic homotopy groups

In [Heller-Ormsby 14](#Heller14), given a finite Galois extension $L/k$ with Galois group $G$, a symmetric monoidal functor 
$$
  c_{\mathbb{C}/\mathbb{R}}^*:\mathrm{Sp}_{G} \rightarrow \mathrm{SH}_k
$$
is constructed, which when evaluated on the endomorphism of the unit, yields the ring homomophism $A(G) \rightarrow GW(k)$ of Dress relating the [[Burnside ring]] to the [[Grothendieck-Witt ring]]. 

The following theorem is Theorem 1.1 of [Heller-Ormsby 17](#Heller17) (with image shown in [Heller-Ormsby 14](#Heller14)).

\begin{theorem}
   If $k$ is a real closed field and $L = k[i]$ its algebraic closure, then the functor
  $$
    c_{L/k}^*:\mathrm{Sp}_{C_2} \rightarrow \mathrm{SH}_k
  $$
  is a fully faithful symmetric left adjoint whose image is generated under tensor products and colimits by finite etale $k$-algebras.
\end{theorem}

This yields the following corollary (Thm 3.11 [Heller-Ormsby](#Heller17)):
\begin{corollary}
  The map $\pi^{\mathbb{R}}_{m + n\alpha}(\mathbb{S}_{\mathbb{R}}) \rightarrow \pi_{m+n\sigma}(\mathbb{S}_{C_2})$ is 

1. an injection if $m = 2n - 6$ and $n \geq 0$, and

2. an isomorphism if $m \geq 2n - 5$ and $n \geq 0$.

\end{corollary}

## Related concepts

* [[equivariant homotopy group]]


## References

* {#Heller14} [[Jeremiah Heller]], [[Kyle Ormsby]], _Galois equivariance and stable motivic homotopy theory_, ([arXiv:1401.4728](https://arxiv.org/abs/1401.4728))

* {#Heller16} [[Jeremiah Heller]], [[Kyle Ormsby]], _Galois equivariance and stable motivic homotopy theory_, ([arXiv:1701.09099](https://arxiv.org/abs/1701.09099))

* {#Guillou24} [[Bertrand Guillou]], [[Daniel Isaksen]], _$C_2$-Equivariant Stable Stems_, ([arXiv:2404.14627](https://arxiv.org/abs/2404.14627))

[[!redirects C_2-equivariant homotopy groups of spheres]]