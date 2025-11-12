+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

*Nakayama's lemma* is a simple but fundamental result of [[commutative algebra]] which is frequently used to lift information from the [[fiber]] of a [[sheaf]] over a point (as for example a [[coherent sheaf]] over a [[scheme]]) to give information on the [[stalk]] at that point. 

## Statement

We first give a general version of Nakayama's lemma (Prop. \ref{GeneralNakayamaLemma}) and then give as corollaries two alternative statements (Prop. \ref{FirstSpecialVersion} and Prop. \ref{SecondSpecialVersion}) that are also often called "Nakayama's lemma".

\begin{proposition}\label{GeneralNakayamaLemma}
**(Nakayama's lemma**)
\linebreak
Given a [[commutative ring]] $R$, a [[finitely generated]] [[module|$R$-module]] $M$, and an [[ideal]] $I \subseteq R$,

1. $\text{supp} (M) = \mathcal{V} (Ann (M))$.

2. $M \otimes_{R} (R / I) \,&#x2244;\, 0$ iff $\text{supp}(M) \cap \mathcal{V} (I)$ is [[inhabited set|inhabited]].

\end{proposition}

(Here $\mathcal{V} (I)$, $\text{supp} (M)$, and $Ann (M)$ denote the [zero locus](https://stacks.math.columbia.edu/tag/00DZ) of $I$, [support](https://stacks.math.columbia.edu/tag/00L1) of $M$, and [annihilator](https://stacks.math.columbia.edu/tag/07T7) of $M$ respectively.)

Below is an "element-free" proof. The key ideas are that finitely-generated $R$-modules are (precisely) those which can be "built up" from cyclic $R$-modules via extensions and that the relevant properties of the former are sufficiently determined by those of their constituent cyclic $R$-modules, which are easily verified.

\begin{proof}

Recall the following five basic facts (essentially three "inductive principles" and two "base cases" of our "induction" up from cyclic modules):

1. A a morphism of short exact sequences is $0$ in the middle component iff it's $0$ in the left and right components.

2. Given a prime $\mathfrak{p} \in Spec (R)$, the functor $N \mapsto N \otimes_{R} R _{\mathfrak{p}}$ is exact.

3. Given an ideal $J \subseteq R$, the functor $N \mapsto N \otimes_{R} (R / J)$ is right exact.

4. Given a prime $\mathfrak{p} \in Spec (R)$ and an ideal $J \subseteq R$, the localization $(R / J) \otimes_{R} R _{\mathfrak{p}}$ is not $0$ iff $\mathfrak{p} \in \mathcal{V} (J)$.

5. Given ideals $J_{0}, J_{1} \subseteq R$, the tensor product $(R / J_{0}) \otimes_{R} (R / J_{1})$ is $R / (J_{0} + J _{1})$, hence $0$ iff $\mathcal{V} (J_{0}) \cap \mathcal{V} (J_{1})$ is inhabited.

The argument consists of four parts:

1. By the hypothesis that $M$ is finitely generated there exists some $n$ such that $M$ is a quotient of $R ^ {n}$, hence it follows (by taking the image under said quotient of the standard length-$n$ filtration of $R ^ {n}$) that $M$ admits a length-$n$ filtration with cyclic cokernels; denote this filtration as the $n$-tuple of short exact sequences
\[ \left( \ 0 \to M_{k} \to M_{k+1} \to R / I_{k} \to 0 \ \right)_{k = 0, \dots, n-1} \]
with $( I_{k} )_{k=0,\dots,n-1}$ ideals of $R$.
 
2. We now show that $\mathcal{V} (Ann (M)) = \bigcup_{k=0}^{n-1} \mathcal{V} (I_{k})$. It follows (inductively) by recalled fact 1 that all $f \in Ann (M)$ act as $0$ on all the $R / I_{k}$, i.e., that $Ann (M) \subseteq \bigcap_{k=0}^{n-1} I_{k}$, hence $\mathcal{V} (Ann (M)) \supseteq \bigcup_{k=0}^{n-1} \mathcal{V} (I_{k})$. Conversely, for all $k = 0, \dots, n-1$ we have that $I_{k} M_{k+1} \subseteq M_{k}$, from which it follows (inductively) $\prod_{k=0}^{n-1} I_{k} \subseteq Ann(M)$, hence in turn that $\bigcup_{k=0}^{n-1} \mathcal{V} (I_{k}) \supseteq \mathcal{V} (Ann (M))$.

3. We now show that $supp (M) = \bigcup_{k=0}^{n-1} \mathcal{V} (I_{k})$. Given a prime $\mathfrak{p} \in Spec (R)$, suppose first that $\mathfrak{p} \notin \bigcup_{k = 0, \dots, n-1} \mathcal{V} (I_{k})$. By recalled facts 2 and 4, we obtain an $n$-tuple of short exact sequences
\[ \left( \ 0 \to M_{k} \otimes_{R} R _{\mathfrak{p}} \to M_{k+1} \otimes_{R} R _{\mathfrak{p}} \to 0 \to 0 \ \right)_{k = 0, \dots, n-1} , \]
hence (inductively) that
\[ 0 \ \simeq \ M_{0} \otimes_{R} R _{\mathfrak{p}} \ \simeq \ \dots \ \simeq M_{n} \otimes_{R} R _{\mathfrak{p}} \ = \ M \otimes_{R} R _{\mathfrak{p}} . \]
Otherwise $\mathfrak{p} \in \bigcup_{k = 0, \dots, n-1} \mathcal{V} (I_{k})$, hence there exists a maximal index $k_{max}$ such that $\mathfrak{p} \in \mathcal{V} (I_{k_{max}})$. Applying recalled facts 2 and 4, we obtain an epimorphism
\[ M_{k_{max}+1} \otimes_{R} R _{\mathfrak{p}} \to (R / I_{k_{max}}) \otimes_{R} R _{\mathfrak{p}} \to 0 \]
with $(R / I_{k_{max}}) \otimes_{R} R _{\mathfrak{p}}$ not $0$, hence that $M_{k_{max}+1} \otimes_{R} R _{\mathfrak{p}}$ is not $0$, as well isomorphisms
\[ \left( \ 0 \to M_{k} \otimes_{R} R _{\mathfrak{p}} \to M_{k+1} \otimes_{R} R_{\mathfrak{p}} \to 0 \to 0\ \right)_{k = k_{max}+1, \dots, n-1} , \]
hence (inductively) that
\[ M_{k_{max}+1} \otimes_{R} R _{\mathfrak{p}} \ \simeq \ \dots \ \simeq \ M_{n} \otimes_{R} R _{\mathfrak{p}} \ = \ M \otimes_{R} R _{\mathfrak{p}} \]
with the latter not $0$.

4. We now show that $M \otimes_{R} (R / I)$ is not $0$ iff there exists a $k = 0, \dots, n - 1$ for which $\mathcal{V} (I_{k}) \cap \mathcal{V} (I)$ is inhabited. Suppose first that $\mathcal{V} (I_{k}) \cap \mathcal{V} (I) = \emptyset$ for all $k = 0, \dots, n-1$; by recalled facts 3 and 5 we obtain an $n$-tuple of right exact sequences
\[ \left( \ M_{k} \otimes_{R} (R / I) \to M_{k+1} \otimes_{R} (R / I) \to 0 \to 0 \ \right)_{k = 0, \dots, n-1} , \]
hence (inductively) that
\[ 0 \ \simeq M_{0} \otimes_{R} (R / I) \ \simeq \ \dots \ \simeq \ M_{n} \otimes_{R} (R / I) \ = \ M \otimes_{R} (R / I) . \]
Otherwise there exists a prime $\mathfrak{p} \in Spec (R)$ such that $\mathfrak{p} \in \mathcal{V} (I)$ and maximal index $k_{max}$ such that $\mathfrak{p} \in \mathcal{V} (I_{k_{max}})$; applying recalled facts 3, 4, and 5, we obtain an epimorphism
\[ M_{k_{max}+1} \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \to R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \to 0 , \]
hence that $M_{k_{max}+1} \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p})$ is not $0$. Applying recalled facts 2 and 4, we obtain (localizing before tensoring with the quotient, though of course the two commute) isomorphisms
\[ \left( \ 0 \to M_{k} \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \to M_{k+1} \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \to 0 \to 0 \ \right)_{k = k_{max}+1, \dots, n-1} , \]
hence (inductively) that
\[ M_{k_{max}+1} \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \ \simeq \ \dots \ \simeq \ M_{n} \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \ = \ M \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \]
with the latter not $0$, hence in turn (as by recalled fact 5 $M \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p}) \ \simeq \ M \otimes_{R} (R / I) \otimes_{R} R _{\mathfrak{p}} \otimes_{R} (R / \mathfrak{p})$) that $M \otimes_{R} (R / I)$ is itself not $0$.

Claims 1 and 2 of Prop. \ref{GeneralNakayamaLemma} are immediate from subarguments 2 and 3 and  2 and 4 above respectively.
\end{proof}

More familiar forms of Nakayama's lemma can be recovered as corollaries of the above without too much effort. Sometimes, as for instance in the [Stacks Project](https://stacks.math.columbia.edu/tag/07RC), wherein all 11(!) other formulations of the lemma are straightforwardly reduced to it, Nakayama's lemma is stated instead as follows:

\begin{proposition}\label{FirstSpecialVersion}
**(special version I)** 
\linebreak
Given a commutative ring $R$, a finitely generated $R$-module $M$, and an ideal $I \subseteq R$ such that $I M = M$, there exists am element $f \in R$ such that $f = 1 \ (mod \ I)$ and $f M = 0$.
\end{proposition}
\begin{proof}
From that $I M = M$ it follows that $M \otimes_{R} (R / I) \simeq 0$ hence from Prop. \ref{GeneralNakayamaLemma} that $\mathcal{V} (I)$ is disjoint from with $\mathcal{V} (Ann(M))$, or in other words that $I$ and $Ann(M)$ are comaximal. The [Chinese Remainder theorem](https://stacks.math.columbia.edu/tag/00DT) then constructs the desired $f \in R$ such that $f = 1\ (mod\ I)$ and $f = 0\ (mod\ Ann(M))$.
\end{proof}

Alternatively, Nakayama’s lemma is often also understood as a means by which information about the fiber of a module at a point can be used to characterize that of its stalk at said point:

\begin{proposition}\label{SecondSpecialVersion}
**(special version II)** 
\linebreak
Given a local ring $R$ with maximal ideal $\mathfrak{m} \subseteq R$ and a finitely generated $R$-module $M$, $M$ is not $0$ iff $M \otimes_R (R / \mathfrak{m})$ is not $0$. 
\end{proposition}
\begin{proof}
It is essentially tautological that $M$ is not $0$ iff $\mathfrak{m}$ is in (hence intersects, viewed as a close subset) $supp (M)$. Now apply the second claim of Prop. \ref{GeneralNakayamaLemma}.
\end{proof}

## Examples and consequences

\begin{example}
Suppose $R$ is a local ring with maximal ideal $\mathfrak{m} \subseteq R$ and $f \colon N \to M$ is an $R$-module map. The latter gives rise to an exact sequence
\[ N \stackrel{f}{\to} M \stackrel{p}{\to} M / N \to 0 . \]
Tensoring with $R / \mathfrak{m}$ is a right exact functor, so we have an exact sequence
\[ N \otimes_{R} (R / \mathfrak{m}) \stackrel{f \otimes_{R} (R / \mathfrak{m})}{\to} M \otimes_{R} (R / \mathfrak{m}) \stackrel{p \otimes_{R} (R / \mathfrak{m})}{\to} (M / N) \otimes_{R} (R / \mathfrak{m}) \to 0 . \]
Nakayama's lemma says that if $(M / N) \otimes_{R} (R / \mathfrak{m})$, then $M / N \cong 0$. Equivalently, it says that if $f \otimes_{R} (R / \mathfrak{m})$ is epic, then $f$ is epic. In particular, to check whether a finite set of elements $v_{1}, \ldots, v_{n}$ generates $M$, it suffices to check whether the residue classes $v_i \mod \mathfrak{m} M$ generate the vector space $M / \mathfrak{m} M$, which is a linear algebra calculation (as $R / \mathfrak{m}$ is a field). 
\end{example}

\begin{example}
Suppose $R$ is a [[Noetherian ring|Noetherian]] local ring with maximal ideal $\mathfrak{m} \subseteq R$. A typical example is the stalk at a point $p$ of a Noetherian scheme as locally ringed space, and we will write as if we were in that situation. As $R$ is Noetherian, $\mathfrak{m}$ is finitely generated. Suppose $\mathfrak{m} \otimes (R / \mathfrak{m}) \cong \mathfrak{m} / \mathfrak{m}^2$ -- the cotangent space -- is a vector space of dimension $n$. We would like to know whether a collection of functions $f_1, \ldots, f_n$ that vanish at $\mathfrak{m}$ form a local coordinate system. 

For this, it suffices to check whether the differentials $d f_1, \ldots, d f_n$ at $\mathfrak{m}$, belonging to the cotangent space $\mathfrak{m}/\mathfrak{m}^2$, are linearly independent. (For then they span the cotangent space, and one concludes from Nakayama that the $f_i$ generate $\mathfrak{m}$ as an $R$-module, thereby forming a local coordinate system at $\mathfrak{m}$.) In this way, Nakayama's lemma operates as a kind of "inverse function theorem". 
\end{example}

To cement this further, the following statement is offered in [Harris](#Harris) as a corollary of Nakayama's lemma (corollary 14.10, page 179): 

+-- {: .num_prop}
###### Proposition 
**(Inverse Function Theorem)** 
A map between complex projective varieties of dimension $n$ which is a bijection and has injective derivative at every point is an isomorphism. 
=-- 

## References

Cf. [Stacks 07RC](https://stacks.math.columbia.edu/tag/07RC)

category: algebra
[[!redirects Nakayama lemma]]