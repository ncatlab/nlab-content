
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[linear algebra]], what is known as the *rank-nullity theorem* (e.g. 3.22 of [Axler 2015](#Axler15), who calls it the *fundamental theorem of linear maps*) is the statement that for any [[linear map]] $f \colon V \to W$ out of a [[finite-dimensional vector space]], the [[sum]] of 

* the [[rank of a linear map|rank]] $rk(f) \coloneqq dim\big(im(f)\big)$, i.e. the [[dimension of a vector space|dimension]] of the [[image]];

with

* the *nullity* $nl(f) \coloneqq dim\big( ker(f) \big)$, i.e. the [[dimension of a vector space|dimension]] of the [[kernel]]

equals 

* the [[dimension]] $d_V \coloneqq dim(V)$ of the [[domain]] space $V$:

$$
  d_V \;=\; rk(f) + nl(f)
  \,.
$$

This rank-nullity theorem is the [[decategorification]] (under the [[dimension of a vector space|dimension]] [[functor]] $dim \colon FinDimVect \to \mathbb{Z}$) of the stronger statement that $V$ itself is the [[direct sum]] of its [[kernel]] and [[image]] [[vector spaces]]:

$$
  V \;\simeq\; im(f) \oplus ker(f)
  \,.
$$

This may be understood as an instance of the [[splitting lemma]] for [[vector spaces]], or more precisely of the statement ([here](split+exact+sequence#OfVectorSpaces)) that every [[short exact sequence]] of [[vector spaces]], such as

$$
  0 \to ker(f) \longrightarrow V \longrightarrow im(f) \to 0
$$

is a [[split exact sequence]], hence of the form

$$
  0 \to ker(f) \longrightarrow ker(f) \oplus im(f)  \longrightarrow im(f) \to 0
  \,.
$$


## Partial generalization to modules
  {#PartialGeneralizationToModules}


While the rank-nullity theorem does not fully generalize from [[vector spaces]] over [[fields]] to [[modules]] over [[rings]], some aspects do carry over. For instance:

\begin{proposition}\label{OrzechTheorem}
  Let $M$ be a [[finitely generated module]] over a [[unital ring|unital]] [[commutative ring]], and $N \subset M$ a [[submodule]]. Then [[surjective]] module [[homomorphisms]] $N \longrightarrow M$ are already [[isomorphisms]].
\end{proposition}

This was claimed in [Orzech 1971](#Orzech1971), though with a gap in the proof (cf. [Grinberg 2014](#Grinberg2014)). A full proof was given by [Grinberg 2016](#Grinberg2016). For the special case $N = M$ see also [SP 05G8](#StacksProject05G8).

\begin{proof}
The following proof reproduces a [proof by Thomas Browning](https://math.stackexchange.com/questions/1065786/is-orzechs-generalization-of-the-surjective-endomorphism-is-injective-theorem-c/5120133#5120133) using the [[Cayley-Hamilton theorem]].

Let $M=\langle m_1,\ldots,m_k\rangle$ with $m_i=f(n_i)$ and $n_i=\sum_ja_{ij}m_j$.
Set $A=(a_{ij})$, so that $\vec{n}=A\vec{m}$.

By the Cayley-Hamilton theorem, $A$ satisfies a polynomial equation
$$A^k+c_{k-1}A^{k-1}+\cdots+c_2A^2+c_1A+c_0I=0.$$
Plugging in $\vec{m}$ gives
$$A^k\vec{m}+c_{k-1}A^{k-1}\vec{m}+\cdots+c_2A^2\vec{m}+c_1A\vec{m}+c_0\vec{m}=0.$$
Substituting $A\vec{m}=\vec{n}$ gives
$$A^{k-1}\vec{n}+c_{k-1}A^{k-2}\vec{n}+\cdots+c_2A\vec{n}+c_1\vec{n}+c_0\vec{m}=0.$$
Applying $f$ component-wise gives
$$A^{k-1}\vec{m}+c_{k-1}A^{k-2}\vec{m}+\cdots+c_2A\vec{m}+c_1\vec{m}+f(c_0\vec{m})=0.$$
Substituting $A\vec{m}=\vec{n}$ gives
$$A^{k-2}\vec{n}+c_{k-1}A^{k-3}\vec{n}+\cdots+c_2\vec{n}+c_1\vec{m}+f(c_0\vec{m})=0.$$
Applying $f$ component-wise gives
$$A^{k-2}\vec{m}+c_{k-1}A^{k-3}\vec{m}+\cdots+c_2\vec{m}+f(c_1\vec{m}+f(c_0\vec{m}))=0.$$
Iterating this will eventually give the identity
$$\vec{m}+f(c_{k-1}\vec{m}+f(c_{k-2}\vec{m}+f(\cdots))=0.$$
By taking linear combinations, this same identity holds for all $x\in M$, so
$$x+f(c_{k-1}x+f(c_{k-2}x+f(\cdots))=0.$$
Plugging in $x\in\ker f$ forces $x=0$.
Thus, $f$ is injective.
\end{proof}

## References

### Ordinary

Textbook accounts:

* {#Axler15} Sheldon Axler, 3.22 in: *Linear Algebra Done Right*, Springer (2015) &lbrack;[doi:10.1007/978-3-319-11080-6](https://doi.org/10.1007/978-3-319-11080-6)&rbrack;

A [[formal proof]] of the rank-nullity theorem in the [[Isabelle]] [[proof assistant]]:

* [Archive of Formal Proof](https://www.isa-afp.org/), *[Rank-Nullity Theorem in Linear Algebra](https://www.isa-afp.org/entries/Rank_Nullity_Theorem.html)*

See also:

* Wikipedia, *[Rank-nullity theorem](https://en.wikipedia.org/wiki/Rank%E2%80%93nullity_theorem)*

### Partial generalization to modules
 {#ReferencesPartialGenealizationToModules}

* {#Orzech1971} Morris Orzech: *Onto Endomorphisms are Isomorphisms*, The American Mathematical Monthly **78** 4 (1971) 357-362 \[<a href="https://doi.org/10.2307/2316897">doi:10.2307/2316897</a>, [jstor:2316897](https://www.jstor.org/stable/2316897)\]

* {#Grinberg2014} [[Darij Grinberg]]: *Is Orzech's generalization of the surjective-endomorphism-is-injective theorem correct?* (2014) &lbrack;[MO:q/1065786](https://math.stackexchange.com/q/1065786/58526)&rbrack;

* {#Grinberg2016} [[Darij Grinberg]]: *A constructive proof of Orzech’s theorem* (2016) &lbrack;[pdf](https://www.cip.ifi.lmu.de/~grinberg/algebra/orzech.pdf), [[Grinberg-OrzechTheorem.pdf:file]]&rbrack;

* {#StacksProject05G8} [[The Stacks Project]]: [Tag 05G8](https://stacks.math.columbia.edu/tag/05G8)


[[!redirects fundamental theorem of linear maps]]

[[!redirects Orzech's theorem]]
[[!redirects Orzech theorem]]

