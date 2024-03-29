#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _Grothendieck connection_ $\nabla$ is a way to encode the parallel transport of a _flat_ [[connection on a bundle|connection]] along [[infinitesimal object|infinitesimal]] paths.

In the language of [[schreiber:∞-Lie theory|∞-Lie theory]] it is a morphism from the [[infinitesimal path ∞-groupoid]] $\Pi_{inf}(X) \coloneqq \Im(X)$ of a suitable [[space]] $X$ (a [[scheme]] in [[algebraic geometry]] or, more generally, a space in [[synthetic differential geometry]]) to some [[Lie ∞-groupoid]] $A$:

$$
  \nabla : \Pi_{inf}(X) \to A
  \,.
$$

Here $\Pi_{inf}(X)$ is effectively the [[infinitesimal singular simplicial complex]] of $X$ and $A$ is modeled typically as a [[sheaf]] of [[∞-groupoid]]s as described at [[models for ∞-stack (∞,1)-toposes]].

This was originally considered by [[Alexander Grothendieck|Grothendieck]] for [[scheme]]s in the context of [[algebraic geometry]] for the case that $A$ is a 1-[[groupoid]] -- but the generalization to [[∞-groupoid]]s in [[synthetic differential geometry]] is immediate.


## Details

In his study of [[crystalline cohomology]], [[Alexander Grothendieck|Grothendieck]] has noticed that flat [[connection on a bundle|connection]]s correspond to the [[descent]] data for [[deRham complex|deRham]] descent; he called them the costratification of the $n$-th order if one considers the $n$-the infinitesimal neighborhoods. 

Already in EGA, Grothendieck has introduced a notion of [[regular differential operator]] and of jet-spaces, which were later by Malgrange and Spencer transferred into the study of differential equations and analytic deformation theory.

De Rham descent for a relative [[scheme]] (= morphism of schemes) $f: X\to S$ is formulated in terms of resolutions or [[infinitesimal object|infinitesimal]] thickenings of the diagonal for the [[simplicial object|simplicial]] scheme 

$$
  \cdots
  X 
  \times_S X \times_S X 
  \stackrel{\to}{\stackrel{\to}{\to}}
   X \times_S X \stackrel{\to}{\to}
   X
$$

corresponding to $f$. Usually one assumes that $X$ is a [[smooth scheme]] of finite type over $S$. By separatedness the diagonal $\Delta: X\hookrightarrow X\times_S X$ is a [[closed subscheme|closed immersion of schemes]]. Let then $\mathcal{I}$ be the corresponding defining ideal sheaf (locally it is generated by the elements of the form $t\otimes 1 - 1\otimes t$, cf. [[Kähler differential]]). The definining ideal $\mathcal{I}^{n+1}$ defines for the $n$-th infinitesimal neighborhood $X^{(n)}$ and the diagonal subscheme $X\cong \Delta(X)\hookrightarrow X\times_S X$; there is a series of inclusions

$$
X\hookrightarrow X^{(1)}\hookrightarrow X^{(2)}\hookrightarrow \ldots \hookrightarrow X^{(\infty)}=\hat{X}
$$

where $\hat{X}$ is the completion (the corresponding [[formal scheme]]). Let $\mathcal{F}\to Sch$ be a [[Grothendieck fibration]] over the category of schemes (or the subcategory of the category of schemes containing all schemes in our consideration) classified under the [[Grothendieck construction]] by some [[pseudofunctor]] $A : Sch^{op} \to Cat$. A typical examples would be the [[stack]] of [[quasicoherent sheaves]] of $\mathcal{O}$-modules. 

Consider now the projections $d_0,d_1:X\times_S X\to X$. 
Then


+-- {: .un_defn}
###### Definition (Grothendieck connection)

A **Grothendieck connection** on an object $\rho\in\mathcal{F}$ is a [[descent]] datum of the form $(\rho,\theta)$ where $\theta: d_0^*\rho\to d_1^*\rho$ is an isomorphism satisfying the cocycle (and the normalization) condition and such that the restriction (pullback along inclusion) on the diagonal is the identity.

=--


The constructions can be almost literally transferred to the [[synthetic differential geometry]] using [[infinitesimal object|infinitesimal neighborhoods]] in that setup. 

More recently, some partial generalizations were found in the purely algebraic framework. One could take any [[coring]] (or even an additive [[comonad]]) with a [[grouplike element]] and define corresponding connections and descent data and generalize the correspondence found by Grothendieck (see [[semi-free dga]] and Menini-Stefan reference below).


## Literature and links

Related entries include [[deRham space]], [[crystal]], [[crystalline cohomology]]

* A. Grothendieck, _Crystals and the de Rham cohomology of schemes_, p. 306--358 of _Dix exposes sur la cohomologie des schemas_, North Holland 1968, [Dix exp. pdf](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf)

* P. Berthelot,  A. Ogus, _Notes on crystalline cohomology_, Princeton Univ. Press 1978. vi+243, ISBN0-691-08218-9 

* N. Katz, _Nilpotent connections and the monodromy theorem : applications of a result of Turrittin_, Publications Math&#233;matiques de l'IH&#201;S, 39 (1970), p. 175-232  [numdam](http://www.numdam.org/item?id=PMIHES_1970__39__175_0)

* A. Grothendieck, (EGA IV.16) _&#201;l&#233;ments de g&#233;om&#233;trie alg&#233;brique_ (r&#233;dig&#233;s avec la collaboration de Jean Dieudonn&#233;) : IV. &#201;tude locale des sch&#233;mas et des morphismes de sch&#233;mas, Quatri&#232;me partie. Publications Math&#233;matiques de l'IH&#201;S, 32 (1967), p. 5-361 [numdam](http://www.numdam.org/numdam-bin/fitem?id=PMIHES_1967__32__5_0)

* SGA III, vol. 1, Expose VIIa (P. Gabriel) ETUDE INFINITESIMALE DES SCHEMAS EN GROUPES, 409-473 

* wikipedia: [Grothendieck connection](http://en.wikipedia.org/wiki/Grothendieck_connection)

* B. Osserman, _Connections, curvature and $p$-curvature_, [pdf](http://www.math.ucdavis.edu/~osserman/math/connections.pdf) (expositional preprint) 

* A. Beilinson, I. N. Bernstein, _A proof of Jantzen conjecture_, Adv. in Soviet Math. 16, Part 1 (1993), 1-50. MR95a:22022

* C. Menini, D. &#350;tefan, _Descent theory and Amitsur cohomology of triples_, J. Algebra 266 (2003), no. 1, 261--304 (<a href="http://dx.doi.org/10.1016/S0021-8693(03)00145-5">doi</a>). 

* T. Brzezi&#324;ski, R. Wisbauer, _Corings and comodules_, London Math. Soc. Lec. Note Series 309, Cambridge 2003.

* L. Breen, Messing, _Combinatorial differential forms_, [arxiv:math/0005087](http://arxiv.org/abs/math/0005087)

* Notes in Gaitsgory's grad student seminar [pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Nov17-19%28Crystals%29.pdf)