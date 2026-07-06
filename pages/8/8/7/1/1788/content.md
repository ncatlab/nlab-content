> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


***
\linebreak


motivation -- local systems in physics: 

Hilbert spaces of gapped quantum ground states over classical parameter space $P$ of topological phases of matter

topological phases are $C \in \pi_0(P)$

topological orders in phase $C$ are $\mathcal{H} \in Rep_{\mathbb{C}}\big(\pi_1(P,C)\big)$

topological orders in any phase are $\mathcal{H} \in Loc_{\mathbb{C}}(P)$

in fragile crystalline phases: parameter space is crystal lattice couplings reflected in 1-electron Hamiltonians from a space $\mathcal{A}$, hence parameter space is $P = Map(T^d, \mathcal{A})$

topological phases are $C \in \pi_0 \big( Map(T^d, \mathcal{A})\big)$

topological orders in phase $C$ are $\mathscr{H} \in Rep_{\mathcal{C}}\Big( \pi_1 \big( Map(T^d,\mathcal{A}), C\big) \Big) $

topological orders in any phase are $\mathscr{H} \in Loc_{\mathbb{C}}\big(Map(T^d, \mathcal{A})\big)$

functorial at least in diffeos of $T^d$ (modular functor)

$\mathscr{H} \in Loc_{\mathbb{C}}\big(Map(T^d, \mathcal{A})\sslash Diff(T^d) \big)$

for crystalline structure use equivariant maps

translate to TFT language

$$
  \mathbb{1}
    \longrightarrow
  Loc_{\mathbb{C}}\big(
    Map(-, \mathcal{A})
    \sslash 
    Diff(T^d)
  \big)
  \;\colon\;
  B Diff(T^d)
  \longrightarrow 
  Vec Mod
$$


in experiment, such FQ(A)H systems are governed by two effective symmetries

* supersymmetry

* area-preserving diffeomorphisms ($W_\infty$)

same as characteristic symmetries of super $p$-branes

$\rightsquigarrow$ find geometric engineering on M-branes in SuGra

$\rightsquigarrow$ need global IR-completion where topological brane charges are determined

(no string folklore, but actual definitions and proofs)

...

magnetized M5 @ A1


***

+-- {: .num_theorem #TheoremAffineVarietiesAffinekAlgebrasAreEquivalent}
###### Theorem

([Milne 2017, Propositions 3.24, 3.25](#Milne17)). Let $k$ be an algebraically closed field. The categories of affine varieties and affine $k$-algebras are [[dual equivalence|anti-equivalent]].

=--

The following result particularizes the [[schemes as sheaves on affine schemes#SchemesAsPresheaves|fundamental theorem on morphisms of schemes]] to prevarieties.

+-- {: .num_prop #PropositionSpmAndGammaAreMutuallyRightAdjoint}
###### Proposition

[Milne 2017, Propositions 5.11](#Milne17). Let $k$ be an algebraically closed field. Let $V$ be an algebraic $k$-prevariety. Let $A$ be an affine $k$-algebra. Then we have the following natural bijection:

$$
Hom(V,Spm(A))\cong Hom_{k\text{-algebra}}(A,\Gamma(V,\mathcal{O}_V)).
$$

=--

In other words, the maximal spectrum functor and the global sections functor, defined between the categories of affine $k$-algebras and $k$-prevarieties, are [[dual adjunction|mutually right adjoint]]. Note that Milne states the result for quasi-compact varieties, but his proof applies in the general case and never uses quasi-compactness nor separation. Note that from \ref{PropositionSpmAndGammaAreMutuallyRightAdjoint} we recover \ref{TheoremAffineVarietiesAffinekAlgebrasAreEquivalent}.