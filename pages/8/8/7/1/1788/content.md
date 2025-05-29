

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak

****

## Hopfion

By *Hopfions* one refers to those [[solitons]] on 3-dimensional [[Euclidean space]] $\mathbb{R}^3$ whose topological configurations are classified by [[homotopy classes]] of [[maps]] to the ([[Riemann sphere|Riemann]]) [[2-sphere]] $S^2 \simeq \mathbb{C}P^1$, hence (by the defining [[vanishing at infinity]] of solitons) by [[homotopy classes]] of [[pointed topological space|pointed]] maps from the [[one-point compactification]] $\mathbb{R}^3_{\cup\{\infty\}} \simeq S^3$ to $S^2$, hence by the 3rd [[homotopy group]] of [[2-sphere|$S^2$]], which is the [[integers]]
$$  
  \pi_3(S^2) \,\simeq\, \mathbb{Z}
  \,.
$$
Since the unit generator of this group is represented by the class of the [[Hopf fibration]] $h \colon S^3 \longrightarrow S^2$ this means that Hopfions have classifying maps given by (multiples of) the [[Hopf fibration]], whence the name.

> To note the difference to but similarity with *[[Skyrmions]]* in 3d, which are instead classified by maps $\mathbb{R}^3_{\cup \{\infty\}} \longrightarrow S^3$ to the [[3-sphere]], and to magnetic Skyrmions in 2d, which are instead classified by maps $\mathbb{R}^2_{\cup \{\infty\}} \longrightarrow S^2$ ---
albeit both also being classified by [[integers]], now via the [[Hopf degree theorem]]: $\pi_n(S^n) \simeq \mathbb{Z}$.

If one identified the "core" locus of a Hopfion with the [[preimage]] under its classifying map of the [[antipode]] of the chosen base point in $S^2$, then this is, by the [[Pontrjagin theorem]], the ([[cobordism class]]) of a [[normal framing|normally framed]] [[submanifold]] of [[codimension]]=2 hence of [[dimension of a manifold|dimension]]=1, hence is (the [[cobordism class]]) of a ([[framed link|framed]]) [[link]].

Traditional [[Lagrangian field theory|Langrangian field]] realization of Hopfions are unit-[[norm]] [[vector]] [[field (physics)|fields]], such as the [[Skyrme-Fadeev model]] ([Fadeev 1975](#Fadeev75), [Fadeev & Niemi 1997](#FadeevNiemi97), review in [Manton & Sutcliffe 2004 §9.11](#MantonSutcliffe04)).


## Related concepts

* [[Hopf-Wess-Zumino term]]

* [[Skyrmion]]

## References

The (Skyrme-)Fadeev model:

* {#Fadeev75} [[Ludwig D. Faddeev]]: *Quantization of Solitons*, talk at [ICHEP 76](https://inspirehep.net/conferences/964007) (1975) &lbrack;[inSpire:2631](https://inspirehep.net/literature/2631)&rbrack;

* {#FadeevNiemi97} [[Ludwig D. Faddeev]], [[Antti J. Niemi]]: *Knots and Particles*, Nature **387** (1997) 58–61 &lbrack;[arXiv:hep-th/9610193](https://arxiv.org/abs/hep-th/9610193), [doi:10.1038/387058a0](https://doi.org/10.1038/387058a0)&rbrack;


Textbook account:

* {#MantonSutcliffe04} [[Nicholas Manton]], [[Paul Sutcliffe]]: *Topological Solitons*, Cambridge University Press (2004) &lbrack;[doi:10.1017/CBO9780511617034](https://doi.org/10.1017/CBO9780511617034), [inSpire:660150](https://inspirehep.net/literature/660150), [pdf](http://www.lmpt.univ-tours.fr/~volkov/Manton-Sutcliffe.pdf)&rbrack;

See also: 

* Wikipedia: *[Hopfion](https://en.wikipedia.org/wiki/Hopfion)*




\linebreak


* $\mathcal{F}$ itself becomes an $\mathcal{F}$-category in the usual way.  Its tight morphisms are just the morphisms in the underlying ordinary category $\mathcal{F}$, while its loose morphisms are simply functors between the loose parts (the codomains of the full embeddings).

## $\mathcal{F}$-functors and $\mathcal{F}$-transformations

\begin{definition}
An **$\mathcal{F}$-functor** $F:\mathbb{A} \to \mathbb{B}$ is a [[2-functor]] $F_\lambda:\mathcal{A}_\lambda \to \mathcal{B}_\lambda$ sends tight 1-cells to tight 1-cells, i.e. such that it co/restrcts to a 2-functor $\mathcal{A}_\tau \to \mathcal{B}_\tau$.
\end{definition}

\begin{definition}
An **$\mathcal{F}$-natural transformation** $\alpha:F \to G$ is a [[2-natural transformation]] $F_\tau \to G_\tau$, i.e. a 2-natural transformation $F \to G$ whose components are all tight.
\end{definition}

## $\mathcal{F}$-weighted limits

The general machinery of [[enriched category]] theory applied to $\mathcal{F}$ gives us a notion of [[weighted limit]].  Note first that an $\mathcal{F}$-enriched *diagram* in an $\mathcal{F}$-category is a diagram of morphisms in which some are required to be tight, and others are not (but could "accidentally" be tight).

In general, a weighted limit of such a diagram in a (strict) $\mathcal{F}$-category is a weighted (strict) [[2-limit]] in its 2-category of loose morphisms, with the property that certain specified projections from the limit object are tight and "jointly detect tightness", in the sense that a morphism into the limit is tight if and only if its composites with all of the specified projections are tight.  Details and examples can be found in ([LS](#LS)).

One of the most important things about $\mathcal{F}$-categories is that they allow us to define the classes of [[rigged limits]], which are the $\mathcal{F}$-weighted limits that are [[created limit|created]] by the forgetful functors from the various $\mathcal{F}$-categories of algebras and strict/pseudo/lax/colax morphisms over a 2-monad (or an $\mathcal{F}$-monad).

### $\mathcal{F}$-weights

Let $\mathbb{F}$ be $\mathcal{F}$ considered as self-enriched.
In ([LS](#LS)) (where all that follows is taken from), it is shown that an $\mathcal{F}$-weight $\Phi:\mathbb{D} \to \mathbb{F}$ is given by the following data:

1. [[2-functors]] $\Phi_\tau : \mathcal{D}_\tau \to \mathbf{Cat}$ and $\Phi_\lambda : \mathcal{D}_\lambda \to \mathbf{Cat}$,
2. a [[2-natural transformation]] $\varphi : \Phi_\tau \to \Phi_\lambda J_{\mathbb{D}}$ whose components are full embeddings (i.e. [[injective-on-objects]], [[fully faithful]] functors)

\begin{tikzcd}
	{\mathcal{D}_\tau} \\
	&& {\mathbf{Cat}} \\
	{\mathcal{D}_\lambda}
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\Phi_\tau}", from=1-1, to=2-3]
	\arrow["{J_{\mathbb{D}}}"', from=1-1, to=3-1]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\Phi_\lambda}"', from=3-1, to=2-3]
	\arrow["\phi"', shift right=4, shorten <=7pt, shorten >=7pt, Rightarrow, from=0, to=1]
\end{tikzcd}

Here $J_\mathbb{D}$ denotes the [[identity-on-objects]], [[faithful]] and [[locally fully faithful]] inclusion of the tight 2-category associated to $\mathbb{D}$ into its loose 2-category.

Representable weights are easily constructed. Let $S:\mathbb{D} \to \mathbb{A}$ be an $\mathcal{F}$-diagram, i.e. an $\mathcal{F}$-functor.
Any chosen $A \in \mathbb{A}$ induces an $\mathcal{F}$-weight on $\mathbb{D}$ given by

\begin{tikzcd}
	{\mathcal{D}_\tau} & {\mathcal{A}_\tau} \\
	&&& {\mathbf{Cat}} \\
	{\mathcal{D}_\lambda} & {\mathcal{A}_\lambda}
	\arrow["{S_\tau}", from=1-1, to=1-2]
	\arrow["{J_{\mathbb{D}}}"', from=1-1, to=3-1]
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\mathcal{A}_\tau(A,-)}", from=1-2, to=2-4]
	\arrow["{J_{\mathbb{A}}}"{description}, from=1-2, to=3-2]
	\arrow["{S_\lambda}"', from=3-1, to=3-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{\mathcal{A}_\lambda(A,-)}"', from=3-2, to=2-4]
	\arrow["{j_\mathbb{A}}"', shift right=4, shorten <=4pt, shorten >=4pt, Rightarrow, from=0, to=1]
\end{tikzcd}

Now a $\Phi$-[[weighted limit]] for $S$, $\lim^\Phi S$, is characterized by the isomorphism
$$\mathbb{A}(A, \lim^\Phi S) \cong [\mathbbf{D},\mathbb{F}](\Phi, \mathbb{A}(A,S))$$
One can prove (by an easy characterization of the $\mathcal{F}$-category on the right) this amounts to three conditions:

1. $\lim^\Phi S$ is a [[2-limit]] in the 2-category $\mathcal{A}_\lambda$,
2. for any $w \in \Phi_\tau(D)$, the projection $p_D^w : \lim^\Phi S \to S(D)$ is tight,
3. for any $h:A \to \{\Phi,S\}$, $h$ is tight as soon as for each $w \in \Phi_\tau(D)$, $h p_D^w$ is tight.

The third condition is succinctly expressed by saying the family $\{p_D^w\}_{D \in \mathbb{D}, w \in \Phi_\tau(D)}$ **jointly detects tightness**.

*****

* Neural Tangent Kernel

* Rupak Chatterjee, Ting Yu: *Generalized Coherent States, Reproducing Kernels, and Quantum Support Vector Machines*, Quantum Information and Communication **17** 15&16 (2017) 1292 &lbrack;[arXiv:1612.03713](arxiv.org/abs/1612.03713), [doi:10.26421/QIC17.15-16](https://doi.org/10.26421/QIC17.15-16)&rbrack;


* *Quantum Machine Learning in Feature Hilbert Spaces*

* *Quantum support vector machine for big data classification*

* *Supervised learning with quantum enhanced feature spaces*

On non-abelian ([[parafermion|parafermionic]]) [[defect]] [[anyons]] associated with [[superconductor|superconducting]] islands inside [[nLab:abelian Chern-Simons theory|abelian]] [[fractional quantum Hall systems]]:

* [[Netanel H. Lindner]], [[Erez Berg]], Gil Refael, [[Ady Stern]]: *Fractionalizing Majorana fermions: non-abelian statistics on the edges of abelian quantum Hall states*, Phys. Rev. X **2** (2012) 041002 &lbrack;[arXiv:1204.5733](https://arxiv.org/abs/1204.5733), [doi:10.1103/PhysRevX.2.041002](https://doi.org/10.1103/PhysRevX.2.041002)&rbrack;


* [[David J. Clarke]], [[Jason Alicea]], [[Kirill Shtengel]]: *Exotic non-Abelian anyons from conventional fractional quantum Hall states*, Nature Communications **4** 1348 (2013) &lbrack;[doi: 10.1038/ncomms2340](https://www.nature.com/articles/ncomms2340), [arXiv:1204.5479](https://arxiv.org/abs/1204.5479)&rbrack;

* Abolhassan Vaezi: *Fractional topological superconductor with fractionalized Majorana fermions*, Phys. Rev. B **87** (2013) 035132 &lbrack;[doi:10.1103/PhysRevB.87.035132](https://doi.org/10.1103/PhysRevB.87.035132), [arXiv:1204.6245](https://arxiv.org/abs/1204.6245)&rbrack;

* [[Roger S. K. Mong]], [[David J. Clarke]], [[Jason Alicea]], [[Netanel H. Lindner]], Paul Fendley, [[Chetan Nayak]], Yuval Oreg, [[Ady Stern]], [[Erez Berg]], [[Kirill Shtengel]], Matthew P. A. Fisher: *Universal Topological Quantum Computation from a Superconductor-Abelian Quantum Hall Heterostructure*, Phys. Rev. X **4** (2014) 011036 &lbrack;[arXiv:1307.4403](https://arxiv.org/abs/1307.4403), [doi:10.1103/PhysRevX.4.011036](https://doi.org/10.1103/PhysRevX.4.011036)&rbrack;

* Younghyun Kim, [[David J. Clarke]], Roman M. Lutchyn: *Coulomb Blockade in Fractional Topological Superconductors*, Phys. Rev. B **96** (2017) 041123 &lbrack;[arXiv:1703.00498](https://arxiv.org/abs/1703.00498), [doi:10.1103/PhysRevB.96.041123](https://doi.org/10.1103/PhysRevB.96.041123)&rbrack;

* [[Luiz H. Santos]], Taylor L. Hughes: *Parafermionic Wires at the Interface of Chiral Topological States*, Phys. Rev. Lett. **118** (2019) 136801 &lbrack;[doi:10.1103/PhysRevLett.118.136801](https://doi.org/10.1103/PhysRevLett.118.136801)&rbrack;

* [[Luiz H. Santos]]: *Parafermions in Hierarchical Fractional Quantum Hall States*, Phys. Rev. Research **2** (2020) 013232 &lbrack;[arXiv:1906.07188](https://arxiv.org/abs/1906.07188), [doi:10.1103/PhysRevResearch.2.013232](https://doi.org/10.1103/PhysRevResearch.2.013232)&rbrack;

see also:

* Zhong Wan et al.: *Induced superconductivity in high-mobility two-dimensional electron gas in gallium arsenide heterostructures*, Nature Communications **6** (2015) 7426 &lbrack;[doi:10.1038/ncomms8426](https://doi.org/10.1038/ncomms8426)&rbrack;

    , 







...

test