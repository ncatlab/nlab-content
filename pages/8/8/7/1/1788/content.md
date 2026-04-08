> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***


<table>
<tr>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  % fills
  \fill[colorA] (-1,0) rectangle (1,1);
  \fill[colorB] (-1,0) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrow points W
  \draw[mid->] (E) -- (W);
  % area labels
  \node at (0,  0.5) {$A$};
  \node at (0, -0.5) {$B$};
  % edge label
  \node[left] at (W) {$B(1, f)$};
\end{tikzpicture}
</td>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{orange!20}
  \colorlet{colorB}{teal!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  % fills
  \fill[colorA] (-1,0) rectangle (1,1);
  \fill[colorB] (-1,0) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrow points E
  \draw[mid->] (W) -- (E);
  % area labels
  \node at (0,  0.5) {$B$};
  \node at (0, -0.5) {$A$};
  % edge label
  \node[right] at (E) {$B(f, 1)$};
\end{tikzpicture}
</td>
</tr>
</table>




\begin{tikzpicture}[scale=2, >=latex]
  \usetikzlibrary{decorations.markings}
\tikzset{mid->/.style={
  decoration={markings, mark=at position 0.6 with {\arrow[scale=1.5]{>}}},
  postaction={decorate}
}}

  % Quadrant fills (centered at origin)
  \fill[blue!15]   (-1,0) rectangle (0,1);
  \fill[teal!20]   (0,0) rectangle (1,1);
  \fill[orange!20] (-1,-1) rectangle (0,0);
  \fill[violet!15] (0,-1) rectangle (1,0);

  % Border
  \draw[gray] (-1,-1) rectangle (1,1);

  % Central node
  \node[circle,draw,fill=white,inner sep=1.5pt] at (0,0) (phi) {$\phi$};

  % Arrows
  \draw[mid->, line width=0.6pt] (-1,0) -- (phi);
  \draw[mid->, line width=0.6pt] (phi) -- (1,0);
  \draw[mid->, line width=0.6pt] (phi) -- (0,-1);
  \draw[mid->, line width=0.6pt] (0,1) -- (phi);

  % Labels
  \node[left]  at (-1,0) {$\alpha_0$};
  \node[right] at (1,0)  {$\alpha_1$};
  \node[above] at (0,1)  {$f$};
  \node[below] at (0,-1) {$g$};
  \node at (-0.5, 0.5) {$x_0$};
  \node at ( 0.5, 0.5) {$x_1$};
  \node at (-0.5,-0.5) {$y_0$};
  \node at ( 0.5,-0.5) {$y_1$};
\end{tikzpicture}





This is how you place two tikzcd diagrams side by side:
<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow[r,  "{B(1, f)}", ""{name=U, below}]
  \arrow[d, "f"']
  & B
  \arrow[d, "id"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
  B
  \arrow[r,  "{B(f, 1)}", ""{name=U, below}]
  \arrow[d, "id"']
  & A
  \arrow[d, "f"]
  \\
  B
  \arrow[r, "U_B"', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
</tr>
</table>

\linebreak

***


+-- {: .num_prop#SiftedIffFinalDiag}
###### Proposition

An [[inhabited set|inhabited]] [[small category]] $D$ is sifted precisely if the [[diagonal]] functor 
  
$$
  D \to D \times D
$$

is a [[final functor]].

=--

This is due to ([GabrielUlmer](#GabrielUlmer))

+-- {: .num_prop #SiftedIffFinalDiag}
###### Proposition

Let $D$ be a small category. The following are equivalent:

1. $D$ is sifted.

2. $D$ is non-empty and for every pair of objects $d_1,d_2\in D$, the category $Cospan_D(d_1,d_2)$ of [[cospans]] from $d_1$ to $d_2$ is [[connected category|connected]].

3. The diagonal functor $D\to D^S$ is final, where $S$ is a finite set.

4. For every finite family of objects $d_1,\dots,d_n\in D$, the category $Sink_D(d_1,\dots,d_n)$ of sinks in $D$ with sources $d_1,\dots,d_n$ is connected.

=--

+-- {: .proof}
###### Proof

The equivalence between 1 and 2 is just the restatement of \ref{SiftedIffFinalDiag}. The equivalence between 3 and 4 is obvious. Trivially, 2 implies 4. We see the converse.

Assume 4. In particular we have that the category of sinks $Sink_D(\emptyset)$ over the empty family of objects in $D$ is connected and thus inhabited, so $D$ is non-empty.

Now let's see that $Sink_D(d_1,\dots,d_n)$ is non-empty. If $n=0$, this is because $D$ is non-empty. If $n=1$, we always have the identity sink $d_1\to d_1$. We show $Sink_D(d_1,\dots,d_n)$ is non-empty for $n\geq 2$ by induction on $n$. The base case $n=2$ is our assumption. For each $1\leq i\lt n$, pick a cospan $d_1\to c_i\leftarrow d_{i+1}$. By induction, there is a sink $\{c_i\to e\}_{1\leq i\lt n}$. Thus $\{d_1\to c_1\to e\}\cup\{d_{i+1}\to c_i\to e\}_{1\leq i\lt n}$ is a sink with sources $d_1,\dots,d_n$. Now we show there is a zig-zag of morphisms between any two objects of $Sink_D(d_1,\dots,d_n)$. In the case $n=0$, this is our assumption. Let $n\geq 1$. Given two sinks $\{d_i\to c\}_{1\leq i \leq n}$, $\{d_i\to e\}_{1\leq i \leq n}$, the assumption gives a cospan $c\to a\leftarrow e$, 

=--


***


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

\[ A \].

