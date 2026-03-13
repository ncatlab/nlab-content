> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak

***

Consider a [[path-connected topological space]] $\mathcal{A}$ admitting the [[structure]] of a [[CW-complex]].

Fixing any [[base points]] $0 \in \mathcal{A}$ and $0 \in S^1$,
we will be concerned with the *[[free loop space]]*
$$
  \mathcal{L}
  \mathcal{A}
  \coloneqq
  \mathrm{Map}({
    S^1, 
    \mathcal{A}
  })
$$
and the *[[based loop space]]*
$$
  \Omega
  \mathcal{A}
  \coloneqq
  \mathrm{Map}^\ast({
    S^1, 
    \mathcal{A}
  })
  \mathrlap{\,.}
$$

Their [[sets]] of [[connected components]] are
the *[[fundamental group]] of $\mathcal{A}$
$$
  G
  \coloneqq
  \pi_1(\mathcal{A})
  \equiv
  \pi_0({\Omega\mathcal{A}})
$$
and its set of [[conjugacy classes]]: 
$$
  \mathrm{Conj}(G)
  \simeq
  \pi_0({\mathcal{L}\mathcal{A}})
  \mathrlap{\,.}
$$

\begin{proposition}
  In every [[connected component]] $[g] \in \mathrm{Conj}(G) \simeq \pi_0(\mathcal{L}\mathcal{A})$, the [[image]] of $\pi_1({\mathcal{L}\mathcal{A}})$ in $G$ is the centralizer group of $g$:
  \[
    \label{ImageOfTopologicalMonodromyInG}
    \pi_1(\mathrm{ev})
    \big({
      \pi_1({
        \mathcal{L}\mathcal{A}
      })
    }\big)
    \simeq
    Z_G(g)
    \subset 
    G
    \mathrlap{\,.}
  \]
  Moreover, when $\mathcal{A}$ has trivial $\pi_2$, then $\pi_1({\mathcal{L}\mathcal{A}})$ is isomorphic to the centralizer 
  \[
    \label{ParameterMonodromyCoindicingWithCentralizer}
    \mathllap{
    \pi_2(\mathcal{A}) \simeq \ast
    \;\;\;\;\;
    \Rightarrow
    \;\;\;\;\;
    }
    \pi_1({
      \mathcal{L}\mathcal{A}
    })
    \simeq
    Z_G(g)
    \mathrlap{\,.}
  \]
\end{proposition}
\begin{proof}
Consider any loop $\gamma \in \Omega \mathcal{A}$ which represents the local topological phase $[g]$: 

\begin{tikzcd}[sep=0pt]
    G
    \ar[rr, "{ \sim }"]
    &&
    \pi_0({\Omega\mathcal{A}})
    \ar[rr]
    &&
    \pi_0({
      \mathcal{L}\mathcal{A}
    })
    \ar[rr, "{ \sim }"]
    &&
    \mathrm{Conj}(G)
    \\
    g
    &\leftrightarrow&
    {[\gamma]}
    &\mapsto&
    {[\gamma]} 
      &\leftrightarrow& 
    {[g]}
    \mathrlap{\,,}
  \end{tikzcd}


and with that used as the base point, consider the homotopy long exact sequence 
induced by the map $\mathrm{ev}$ that evaluates a loop at its base point:
$$
  \Omega X
  \longrightarrow
  \mathcal{L}X
  \xrightarrow{\phantom{-} ev \phantom{-}}
  X
  \mathrlap{\,,}
$$
of this form:

\begin{imagefromfile}
    "file_name": "CentralizerInHomotopyLES.png",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

On the right we are claiming that the [[connecting homomorphism]] $\partial$ [[conjugation action|acts by conjugation]] on $g \in G$. To see this, recall that $\partial$ is generally given on the class of a based loop $\ell \in P_0 \mathcal{A}$ by first lifting it through $\mathrm{ev}$ to a based path $\widehat \ell \in P_{[g]} \mathcal{L}\mathcal{A}$ and then evaluating that at its endpoint:
$$
  \partial\bracket({[\ell]})
  =
  \bracket[{\widehat{\ell}_1}]
  \mathrlap{\,.}
$$
Here we may take $\widehat{\ell}$ to be given by 
$$
  \widehat{\ell}_t
  \coloneqq
  \mathrm{conc}\big({
    \overline{\ell}(t-),
    \gamma, 
    \ell(t-)
  }\big)
$$
(where "$\mathrm{conc}$" denotes [[concatenation]] and an overline denotes reversal of paths $[0,1] \to \mathcal{A}$), which implies the above equality of exact sequences.

From this, the first claim (eq:ImageOfTopologicalMonodromyInG) follows by [[exact sequence|exactness]]: The [[image]] of $\pi_1(\mathrm{ev})$ is now identified with the [[kernel]] of $\mathrm{Ad}_{(-)}(g)$, and that is the centralizer $C_G(g)$, by definition. (Beware here that the copy of "$G$" in the bottom right above is the [[underlying set]] of the group, pointed by the element $g$.)

Similarly for the second claim (eq:ParameterMonodromyCoindicingWithCentralizer): If $\pi_2(\mathcal{A}) = \pi_1(\Omega \mathcal{A})$ is trivial, then exactness gives that $\pi_1(\mathrm{ev})$ is [[injective]] and hence an [[isomorphism]] onto its image.
\end{proof}

For example, given any group $G$, we may consider $\mathcal{A} \coloneqq K(G,1)$, the [[Eilenberg-MacLane space]]. By definition, this has $\pi_1(\mathcal{A}) \simeq G$ and $\pi_2(\mathcal{A}) \simeq \ast$, and hence
$$
  \pi_1\big( \mathcal{L}\mathcal{A}, \gamma \big)
  \simeq
  C_G(g)
  \mathrlap{\,.}
$$


\linebreak

***

* Christopher Couzens, Alice Lüscher, James Sparks: *Localizing punctures in M-theory* &lbrack;[arXiv:2511.03397](https://arxiv.org/abs/2511.03397)&rbrack;


\linebreak

+-- {: .num_defn #DefinitionTopologyGeneratedByFamilies}
###### Definition

Let $C$ be a category. Suppose for each $c\in C$ we are given a collection of families $\{f_i:d_i\to c\}$ of morphisms into $c$. As defined in [SGA 4, Exp. II, 1.1.6](#SGA4), the topology on $C$ generated by this collection is the coarsest topology on $C$ for which the families $\{f_i:d_i\to c\}$ are covering families.

=--

[[Antz-CQTS-Feb2026.pdf:file]]

**Floquet theory**

## Idea

In [[solid state physics]], *Floquet theory* is concerned with [[quantum systems]] which are driven by a [[time]]-periodic external [[forces]]/[[potential energy|potential]]. The archetypical case is the study of [[electrons]] in a [[crystal]] subjected to a strong and periodically oscillating [[electromagnetic field]].

This way, Floquet theory may be understood as the temporal analog of what for spatial periodicity is the subject of *[[Bloch theory]]*.

## References

Textbook account: 

* Thomas Dittrich, Peter Hänggi, Gert-Ludwig Ingold, Bernhard Kramer, Gerd Schön, W. Zwerger; Chapter 5 in: *Quantum Transport and Dissipation*, Wiley-VCH (1998) &lbrack;[pdf](https://www.physik.uni-augsburg.de/theo1/hanggi/Papers/Chapter5.pdf)&rbrack;

Lecture notes:

* Giuseppe E. Santoro: *Introduction to Floquet*, lecture at *[SFT 2019 -- Lectures on Statstical Field Theory](https://www.ggi.infn.it/sft/SFT_2019/index.html)* (2019) &lbrack;[pdf](https://www.ggi.infn.it/sft/SFT_2019/LectureNotes/Santoro.pdf)&rbrack;

* Konrad Viebahn: *Introduction to Floquet theory* (2020) &lbrack;[pdf](https://boulderschool.yale.edu/sites/default/files/files/floquetlecture_Konrad%20Viebahn.pdf)&rbrack;

See also:

* Wikipedia: *[Floquet theory](https://en.wikipedia.org/wiki/Floquet_theory)*

* Grokipedia: *[Floquet theory](https://grokipedia.com/page/Floquet_theory)*

For [[open quantum systems]]:

* Masahiro Sato, Tatsuhiko N. Ikeda: *Floquet theory and applications in open quantum and classical systems*,  	J. Phys. Soc. Jpn. **94** 111007 (2025) &lbrack;[arXiv:2508.01783](https://arxiv.org/abs/2508.01783), [doi:10.7566/JPSJ.94.111007](https://doi.org/10.7566/JPSJ.94.111007)&rbrack;



## Nonconservative mathematical adjectives

In the practice of the naming of concepts in [[mathematics]], it happens that an adjective added to a term not just qualifies that term but actually contradicts it. 

For instance "[[partial functions]]" are not special kinds of functions but are, generally, not functions at all. (More examples are listed below.) This is in contrast to cases like "[[abelian groups]]", which are indeed special kinds of [[groups]].

Hence such *nonconservative adjectives* are modifiers in mathematical terminology that fundamentally alter, negate, or expand the defining axioms of a base term, rather than simply restricting them.

In linguistics one speaks in such cases of *[privative adjectives](https://en.wikipedia.org/wiki/Privative_adjective)*. For example a "fake X" is not an "X", hence "fake" is a privative adjective in the English language.

While strict logic may suggest to avoid nonconservative/privative adjectives, their use in mathematics is pragmatic and the meaning is typically suggestive and readily grasped, instead of misleading. For instance the intended meaning of "[[manifolds with boundary]]" is clear, and yet (if the boundary is non-empty) these are not strictly speaking "[[manifolds]]", whence "with boundary" is a nonconservative qualifier.

Accordingly, an earlier suggestion in this entry to refer to nonconservatively qualified terminology as "red herrings" is (while it may have gained some popularity, though maybe for the wrong reason) not really appropriate, as "red herrings" in the figurative sense are deliberately misleading.



### FQH Excitation modes



On multiple modes resolving the would-be single GMP mode for [FQH excitations](quantum+Hall+effect#CollectiveExcitations) 

near filling fraction $\nu = 1/4$:

* Dung Xuan Nguyen, [[F. D. M. Haldane]], [[Edward H. Rezayi]], [[Dam Thanh Son]], Kun Yang: *Multiple Magnetorotons and Spectral Sum Rules in Fractional Quantum Hall Systems*, Phys. Rev. Lett. **128** (2022) 246402 \[<a href="https://doi.org/10.1103/PhysRevLett.128.246402">doi:10.1103/PhysRevLett.128.246402</a>, [arXiv:2111.10593](https://arxiv.org/abs/2111.10593), suppl:[pdf](https://journals.aps.org/prl/supplemental/10.1103/PhysRevLett.128.246402/Supp.pdf)\]

at [Jain filling fractions](quantum+Hall+effect#CompositeParticlePicture) $n/(2 p n \pm 1)$ with ${\vert n \vert}\geq 2$ (e.g. $\nu = 2/5, 3/7, 2/9, 2/7$):

* [[Ajit C. Balram]], Zhao Liu, [[Andrey Gromov]], [[Zlatko Papić]]: *Very-High-Energy Collective States of Partons in Fractional Quantum Hall Liquids*, Phys. Rev. X **12** (2022) 021008 \[<a href="https://doi.org/10.1103/PhysRevX.12.021008">doi:10.1103/PhysRevX.12.021008</a>, [arXiv:2111.10395](https://arxiv.org/abs/2111.10395)\]

at filling fractions $\nu  = n/(4 n \pm 1)$:

* [[Ajit C. Balram]], G. J. Sreejith, [[Jainendra K. Jain]]: *Splitting of Girvin-MacDonald-Platzman density wave and the nature of chiral gravitons in fractional quantum Hall effect*, Phys. Rev. Lett. **133** (2024) 246605 \[<a href="https://doi.org/10.1103/PhysRevLett.133.246605">doi:10.1103/PhysRevLett.133.246605</a>, [arXiv:2406.02730](https://arxiv.org/abs/2406.02730)\]

in FQH liquids that are not fully spin-polarized:

* Rakesh K. Dora, [[Ajit C. Balram]]: *Dispersion of collective modes in spinful fractional quantum Hall states on the sphere* \[<a href="https://arxiv.org/abs/2509.13100">arXiv:2509.13100</a>\] 

\linebreak

\begin{example}
In the category of [[schemes]] the subcategory of [[affine schemes]] is dense, see [[affine scheme#AffineSchemesFullSubcategoryOfOppositeOfRings|here]].
\end{example}

\begin{example}
In the category of [[smooth manifolds]], the full subcategory whose objects are given by $\mathbb{R}^n$ for $n\geq 1$ with the standard smooth structure, is dense.
\end{example}

Proof: The restricted Yoneda to the full subcategory spanned by ${\{R\}}$ is faithful, hence so is when restricted to the subcat spanned by $\{R,R^2\}$. To see fullness when restricted to the subcat spanned by $\{R,R^2\}$, suppose we are given a morphism $\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ of presheaves on $\mod_{\{R,R^2\}}$. Given $x\in M$, write $z_x\in N$ for the image of $1\in R$ of the induced map $R\to N$ from $R\to M,1\mapsto x$. Write $[x,y]:R^2\to M$ for the map sending $(1,0)$ and $(0,1)$ to $x$ and $y$, respectively, and write $z_{[x,y]}:R^2\to N$ for the induced map. Then $z_{[x,y]}=[z_x,z_y]$ by compatibility with the $i$-th component map $c_i:R\to R^2$, $i=1,2$. Thus, compatibility with the diagonal map $\Delta:R\to R^2$ gives $z_{x+y}=\Delta^*z_{[x,y]}=\Delta^*[z_x,z_y]=z_x+z_y$. On the other hand, given $r\in R$, compatibility with $r: k\to k$ gives $z_{r x}=rz_x$. Thus $x\mapsto z_x$ defines a map $f:M\to N$ of $R$-modules such that $f^*:\operatorname{Hom}(-,M)\Rightarrow\operatorname{Hom}(-,N)$ is the morphism we began with.



## Definition

A complex (or real) [[extended C*-algebra]] whose bounded part is a [[von Neumann algebra]].

Equivalently (by a theorem due to Dixon and Zakirov–Chilin), a complex (or real) [[*-algebra]] $A$ of closed densely defined unbounded operators on a [[Hilbert space]] closed under the operations of strong sum, strong multiplication, passing to adjoints, contains all scalar multiples of the identity operator, for every $x\in A$ we have $(1+x^*x)^{-1}\in A$ (equivalently, $x$ is affiliated with $A_b$), and the [[*-subalgebra]] $A_b$ of bounded operators in $A$ is a [[von Neumann algebra]].

## Properties

For any [[von Neumann algebra]] there is a unique (up to a unique isomorphism) maximal extended von Neumann algebra that has $A$ as its bounded part, namely, the extended von Neumann algebra of locally measurable operators affiliated with $A$.

The [[reduction theory]] for [[von Neumann algebras]] can be extended to the case of extended von Neumann algebras.

## References

* P. G. Dixon, _Generalized B*-algebras_, Proceedings of the London Mathematical Society s3-21:4 (1970), 693-715.  [DOI](https://doi.org/10.1112/plms/s3-21.4.693).

  **  establishes functional calculus for commutative extended C*-algebras and Gelfand-Neumark theorem for noncommutative extended C*-algebras
  ** defines “concrete” C*-algebras in Definition 7.1
  ** shows that “abstract” and “concrete” extended C*-algebras are the same notion, see Theorem 7.13

* P. G. Dixon, _Unbounded operator algebras_, Proceedings of the London Mathematical Society s3-23:1 (1971), 53-69.  [DOI](https://doi.org/10.1112/plms/s3-23.1.53).

  **  defines “concrete” extended von Neumann algebras (called EW*-algebras there) in Definition 1.2
  ** develops reduction theory in Section 3
  ** studies measurable operators in Section 4 and 5
  ** studies locally measurable operators in Section 6 and 7

* B. S. Zakirov, V. I. Chilin, _Abstract characterization of EW*-algebras_, Functional Analysis and Its Applications 25:1 (1991), 63-64.  [DOI](https://doi.org/10.1007/bf01090683).

  *  shows that “abstract” and “concrete” extended von Neumann algebras are the same

  *  proves that extended von Neumann algebras are precisely those [[extended C*-algebras]] whose bounded part is a [[von Neumann algebra]]
