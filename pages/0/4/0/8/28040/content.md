+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

*Principal U(2)-bundles* (also *principal Spin$^\mathrm{c}$(3)-bundles* or *principal Spin$^\mathrm{h}$(2)-bundles*) are special [[principal bundles]] with the second [[unitary group]] [[U(2)|$U(2)$]] ([[exceptional isomorphism|exceptionally isomorphic]] to the third [[spinᶜ group]] $Spin^\mathrm{c}(3)$ and second [[spinʰ group]] $Spin^\mathrm{h}(2)$) as [[structure group]]/[[gauge group]].

Principal U(2)-bundles in particular induce [[principal SO(3)-bundles]] using the canonical projection $U(2)\cong Spin^\mathrm{c}(3)\twoheadrightarrow SO(3)$ and are induced by [[principal SU(2)-bundles]] using the canonical inclusion $SU(2)\hookrightarrow U(2)$.

## Properties

\begin{proposition}
Let $X$ be a $4$-manifold. Two principal U(2)-bundles $P,Q\twoheadrightarrow X$ are isomorphic if and only if their first and second [[Chern class]] are equal:
$$
c_1(P)
=c_1(Q)
\in H^2(X,\mathbb{Z})
$$
$$
c_2(P)
=c_2(Q)
\in H^4(X,\mathbb{Z}).
$$
\end{proposition}

([Gompf & Stipsicz 99, Thrm. 1.4.20](#GompfStipsicz99))

\begin{lemma}
Let $X$ be a $4$-manifold. For every $(c_1,c_2)\in H^2(X,\mathbb{Z})\times H^4(X,\mathbb{Z})$, there exists a principal U(2)-bundle $P\twoheadrightarrow X$ with $c_1(P)=c_1$ and $c_2(P)=c_2$.
\end{lemma}

([Gompf & Stipsicz 99, Thrm. 1.4.20](#GompfStipsicz99))

## Adjoint bundle

Let $P$ be a principal $U(2)$-bundle, then its [[adjoint bundle]] splits as $Ad(P)\cong E\oplus\underline{\mathbb{R}}$ with a real [[vector bundle]] $E$ of rank $3$, which comes from $U(2)\cong(SU(2)\times U(1))/\mathbb{Z}_2$. Their [[characteristic classes]] are related by:
$$
p_1Ad(P)
=(c_1^2-4c_2)(P);
$$
$$
w_2Ad(P)
=c_1(P)mod 2.
$$

([Donaldson & Kronheimer 91, Eq. (2.1.39)](#donaldsonkronheimer91))

## Associated vector bundle

For principal $U(2)$-bundles $P\twoheadrightarrow X$, there is an [[associated bundle|associated]] complex plane bundle $E=P\times_{U(2)}\mathbb{C}^2\twoheadrightarrow X$ using the [[balanced product]]. If $Q$ is the induced [[principal SU(3)-bundle]] (using the canonical inclusion $U(2)\hookrightarrow SU(3),U\mapsto diag(U,det(U)^{-1})$), then its [[adjoint bundle]] is given by:
$$
Ad(Q)
\cong Ad(P)\oplus(det(E)\otimes E)_\mathbb{R}.
$$
If $P$ reduces to a [[principal SU(2)-bundle]], this reduces to:
$$
Ad(Q)
\cong Ad(P)\oplus E_\mathbb{R}\oplus\underline{\mathbb{R}}.
$$
(Both relations hold in general for the maps $SU(n)\hookrightarrow U(n)\rightarrow SU(n+1)$.)

([Donaldson & Kronheimer 91, p. 205](#donaldsonkronheimer91))

## Liftings

\begin{proposition}
A principal U(2)-bundle $f\colon X\rightarrow B U(2)$ lifts to a [[principal SU(2)-bundle]] $\widehat{f}\colon X\rightarrow B SU(2)\cong\mathbb{H}P^\infty$ if and only if its first [[Chern class]] vanishes, hence the composition $c_1\circ f\colon X\rightarrow K(\mathbb{Z},2)$ is [[nullhomotopic]].
\end{proposition}

([Gompf & Stipsicz 99, Thrm. 1.4.20](#GompfStipsicz99))

\begin{proof}
The [[fiber bundle]] $SU(2)\hookrightarrow U(2)\xrightarrow{det}U(1)$ induces a [[fiber bundle]] $\mathbb{H} P^\infty\cong B SU(2)\hookrightarrow B U(2)\xrightarrow{\mathcal{B}det}B U(1)\cong\mathbb{C}P^\infty$, hence a lift exists if and only if the composition $det\circ f\colon X\rightarrow B U(1)$ is [[nullhomotopic]]. Since the first [[Chern class]] $c_1\colon B U(1)\rightarrow K(\mathbb{Z},2)$ can be chosen as the [[identity]] (since $B U(1)$ is [[homeomorphic]] and $K(\mathbb{Z},2)$ is weakly homotopy equivalent to the infinite [[complex projective space]] $\mathbb{C}P^\infty$), postcomposing it to this map doesn't change its [[homotopy class]]. Since the first Chern class is also preserved by the [[determinant]], it then vanishes from the composition.
\end{proof}

## Examples

* One has $S^{2n+1}\cong U(n+1)/U(n)$, hence there is a principal U(2)-bundle $U(3)\twoheadrightarrow S^5$. Such [[principal bundles]] are classified by:
$$
\pi_5B U(2)
\cong\pi_4 U(2)
\cong\mathbb{Z}_{2}.
$$

## Related concepts

Particular [[principal bundles]]:

* [[double cover]] (principal O(1)-bundle)
* [[principal U(1)-bundle]] (principal SO(2)-bundle)
* **principal U(2)-bundle** (principal $Spin^\mathrm{c}(3)$-bundle, principal $Spin^\mathrm{h}(2)$-bundle)
* [[principal SU(2)-bundle]] (principal Sp(1)-bundle, principal Spin(3)-bundle)
* [[principal SU(3)-bundle]]
* [[principal SU(4)-bundle]] (principal Spin(6)-bundle)
* [[principal SO(3)-bundle]]
* [[principal SO(4)-bundle]]
* [[principal SO(6)-bundle]]

## References

* {#HirzebruchHopf58} [[Friedrich Hirzebruch]], [[Heinz Hopf]], _Felder von Flächenelementen in 4-dimensionalen Mannigfaltigkeiten_ (1958)

* {#GompfStipsicz99} [[Robert Gompf]] and [[András Stipsicz]], _4-Manifolds and Kirby Calculus_ (1999), Graduate Studies 
in Mathematics, Volume 20 &lbrack;[ISBN: 978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack; 

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

[[!redirects principal U(2)-bundles]]
[[!redirects U(2)-principal bundle]]
[[!redirects U(2)-principal bundles]]

[[!redirects principal Spinc(3)-bundle]] 
[[!redirects principal Spinc(3)-bundles]]
[[!redirects Spinc(3)-principal bundle]]
[[!redirects Spinc(3)-principal bundles]]

[[!redirects principal Spin^c(3)-bundle]]
 [[!redirects principal Spin^c(3)-bundles]]
[[!redirects Spin^c(3)-principal bundle]]
[[!redirects Spin^c(3)-principal bundles]]

[[!redirects principal Spinᶜ(3)-bundle]]
 [[!redirects principal Spinᶜ(3)-bundles]]
[[!redirects Spinᶜ(3)-principal bundle]]
[[!redirects Spinᶜ(3)-principal bundles]]

[[!redirects principal Spinh(2)-bundle]] 
[[!redirects principal Spinh(2)-bundles]]
[[!redirects Spinh(2)-principal bundle]]
[[!redirects Spinh(2)-principal bundles]]

[[!redirects principal Spin^h(2)-bundle]]
 [[!redirects principal Spin^h(2)-bundles]]
[[!redirects Spin^h(2)-principal bundle]]
[[!redirects Spin^h(2)-principal bundles]]

[[!redirects principal Spinʰ(2)-bundle]]
 [[!redirects principal Spinʰ(2)-bundles]]
[[!redirects Spinʰ(2)-principal bundle]]
[[!redirects Spinʰ(2)-principal bundles]]