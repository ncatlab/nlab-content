{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:goal: style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
+-- {: goal}
###### Lexicon entry on
##Differential graded algebras

This will, for the moment duplicate, overlap and perhaps conflict with [[dg-algebra]]. The approach adopted here  favours the 'internal' idea of a graded algebra, involving a direct sum decomposition, which can often seem more natural than the 'external' one as an indexed family of vector spaces etc. Of course, there are instances and examples where the converse is true!


WORK IN PROGRESS!
=--
###Pre-graded algebras}

A _pre-graded algebra- (pre-ga) or $\mathbb{Z}$-graded algebra_ is a pre-gvs, $A$, together with an algebra multiplication satisfying $A_p.A_q \subseteq A_{p+q}$ for any $p,q$.  The relevant morphisms are pre-gvs morphisms which respect the multiplication.  This gives a category {\sf pre-GA}.

An \emph{augmentation} of a pre-ga, $A$, is a homomorphism $\varepsilon : A \to k$.  The \emph{augmentation ideal} of $(A,\varepsilon)$ is $ker ~\varepsilon$ and will also be denoted $\bar{A}$.  The pair $(A,\varepsilon)$ is called an \emph{augmented pre-ga}.  A morphism $f:(A,\varepsilon)\to (A^\prime,\varepsilon^\prime)$ of augmented pre-gas is a homomorphism $f : A \to A^\prime$ (thus of degree zero) such that $\varepsilon = \varepsilon ^\prime f$.  The resulting category will be written {\sf pre-$\varepsilon$GA}. 

\medskip

\textbf{Tensor product}

If $A$, $A^\prime$ are two pre-gas, then $A\otimes A^\prime$ is a pre-ga with
$$(a\otimes a^\prime)(b\otimes b^\prime) = (-1)^{|a^\prime | |b|}ab\otimes a^\prime b^\prime$$
for homogeneous $a,b \in A$, $a^\prime, b^\prime \in A^\prime$.

If $\varepsilon, \varepsilon$ are augmentations of $A$ and $A^\prime$ respectively, then $\varepsilon\otimes \varepsilon^\prime$ is an augmentation of $A\otimes A^\prime$.

\medskip

\textbf{Derivations}

Let $A$ be a pre-ga. An \emph{(algebra) derivation} of degree $p\in \mathbb{Z}$ is a linear map $\theta \in Hom_p(A,A)$ such that 
$$\theta(ab) = \theta(a)b + (-1)^{p|a|}a\theta(b)$$
for homogeneous $a,b \in A$.

A derivation $\theta$ of an augmented algebra, $(A, \varepsilon)$, is an algebra derivation which, in addition, satisfies $\varepsilon \theta = 0$.

Let $Der_p(A)$ be the vector space of derivations of degree $p$ of $A$, then $Der(A) = \bigoplus_pDer_p(A)$ is a pre-gvs.

\textbf{N.B.} In the case of upper gradings, an element of $Der_p(A)$ sends $A^n$ into $A^{n-p}$.

\medskip

\textbf{Pre-DGAs}

A \emph{differential} $\partial$ on an (augmented) pre-ga is a derivation of the (augmented) algebra of degree -1 such that $\partial\circ\partial = 0$.
  The pair $(A,\partial)$ is called a \emph{pre-differential graded algebra} (pre-dga).  If $A$ is augmented, then $(A,\partial)$ will be called an \emph{augmented pre-dga} (pre-$\varepsilon$dga). 

If $(A,\partial)$ and $(A^\prime,\partial^\prime)$ are pre-dgas, then $(A,\partial)\otimes (A^\prime,\partial^\prime)$, with the conventions already noted, is one as well.

A morphism of pre-dgas (or pre-$\varepsilon$dgas) is a morphism which is both of pre-gdvs and of pre-gas (with $\varepsilon$ as well if used).  This gives categories \textsf{pre-DGA} and \textsf{pre-$\varepsilon$DGA}.

\medskip

\textbf{Commutative graded algebras}


A pre-ga $A$ is said to be \emph{commutative} if $ab = (-1)^{|a||b|}ba$ for each pair, $a, b$, of homogeneous elements of $A$.
 
Commutativity is preserved by tensor product. 

We get obvious full subcategories \textsf{pre-CDGA} and \textsf{pre-$\varepsilon$CDGA}.

\medskip

\textbf{CDGAs}

A cdga is a negatively graded pre-cdga (in upper grading), $A= \bigoplus_{p\geq 0} A^p.$

There is an augmented variant, of course.  These definitions give categories \textsf{CGDA}, etc.

\medskip

\textbf{$n$-connectivity}

An $\varepsilon$cdga $(A,d)$ is \emph{$n$-connected} (resp. \emph{cohomologically $n$-connected}) if $\bar{A}^p = 0 $ for $p\leq n$, (resp. $\overline{H(A,d)}^p = 0$ for $p\leq n$).  This gives subcategories \textsf{CDGA}$^n$ and \textsf{CDGA}$^{cn}$.

\medskip

\textbf{Filtrations}

A filtration on a pre-ga, $A$, is a filtration on $A$, so that $F_pA \subseteq F_{p+1}A$, $F_pA.F_nA \subseteq F_{p+n}A$ (and, if $A$ is differential, also $\partial F_pA \subseteq F_pA$).

\medskip

\textbf{Example:} Word length filtration.

Let $A$ be an augmented pre-ga and denote by $$\bar{\mu}^p : \bigotimes^{p+1}\bar{A} \to \bar{A},$$ the iterated multiplication.  The \emph{decreasing word length filtration}, $F^pA$ is given by:\\
$$F^0A = A, \quad F^pA = Im\bar{\mu}^{(p-1)} \mbox{ if }p\geq 1.$$

$Q(A) = \bar{A}/Im\bar{\mu}$ is the \emph{space of indecomposables} of A.

If $(A,\partial)$ is an augmented pre-dga, $F^pA$ is stable under $\partial$ and we get $Q(\partial)$ is a differential on $Q(A)$ and hence we get a functor  $Q:\mathsf{pre\!-\!\varepsilon DGA}\to \mathsf{pre\!-\!DGVA}.$
\medskip

\textbf{Free GAs: $T(V)$, the tensor algebra}

Given a pre-gvs, $V$, the tensor algebra generated by $V$ is given by $T(V) = \bigotimes_{n\geq 0}V^{\otimes n}$.  The augmentation sends $V$ to 0. $V^{\otimes n}$ is given the tensor product grading, and the multiplication is given by the tensor product.

\begin{lemma} (classical: freeness of $T(V)$, $T$ is a left adjoint)\\
If $A$ is a pre-ga and $f: V\to A$, a morphism to the underlying pre-gvs of $A$, there is a unique extension $\hat{f} :T(V)\to A$, which is a morphism of pre-gvs.\hfill $\square$
\end{lemma}
\medskip

\textbf{Free CGAs: $\bigwedge V$}\label{wedgealg}

This is the tensor product of the exterior algebra on the odd elements and the symmetric algebra on the even ones:
$$\bigwedge V = E(\bigoplus V_{2p+1})\otimes S(\bigoplus V_{2p}).$$
It satisfies $\bigwedge(V \oplus W) \cong (\bigwedge V)\oplus (\bigwedge W)$.

If $A$ is a pre-cga, any morphism, $f : V\to A$, to the underlying pre-gvs of $A$, has a unique extension to a pre-cga morphism $\bar{f} :\bigwedge V \to A$.

If $(e_\alpha)_{\alpha \in I}$ is a homogeneous basis for $V$, $\bigwedge V$ and $T(V)$ may be written $\bigwedge((e_\alpha)_{\alpha \in I})$ and $T((e_\alpha)_{\alpha \in I})$ respectively.

[Note : $T(V)$ is a non-commutative polynomial algebra, $\bigwedge V$ is a commutative polynomial algebra.]
\medskip

\textbf{Word length filtrations on $\bigwedge V$ and $T(V)$.}

On $\bigwedge V$ (resp.  $T(V)$) write $$\bigwedge V = \bigoplus_{k\geq 0}\bigwedge^k V,$$
where $\bigwedge^k V$ is the subspace generated by all $v_1\wedge \ldots \wedge v_k$ with $v_1 \in V$.  Then $F^p\bigwedge V = \bigwedge^{\geq p}V = \bigoplus_{k\geq p}\bigwedge^k V$, resp. $T^k(V) = V^{\otimes k}$ and $F^pT(V) = T^{\geq p}(V) = \bigoplus_{k\geq p}T^k(V)$).

If $(\bigwedge V,d)$ is a pre-cdga, which is free as a pre-cga on a fixed $V$, then $d$ is the sum of derivations $d_k$ defined by the condition $d_k(V) \subseteq \bigwedge^k V$.  There is an isomorphism between $V$ and $Q(\bigwedge V)$, which identitifes $d_1$ with $Q(d)$. The derivation $d_1$ (resp. $d_2$) is called the \emph{linear part} (resp. \emph{quadratic part}) of $d$.
\medskip

\textbf{Sum and Product of CDGAs.}

If $(A,d)$ and $(A^\prime,d^\prime)$ are two cdgas, their (categorical) \emph{sum} (i.e. coproduct) is their tensor product, $(A,d)\otimes(A^\prime,d^\prime)$, whilst their product is the `direct sum', $(A,d)\oplus (A^\prime,d^\prime)$.
\medskip

\textbf{Koszul convention}

Given a permutation $\sigma$ of a graded object $(x_1, \ldots, x_p)$, the \emph{Koszul sign}, $\varepsilon(\sigma)$ is defined by 
$$x_1\wedge \ldots \wedge x_p = \varepsilon(\sigma)x_{\sigma(1)}\wedge \ldots \wedge x_{\sigma(p)}$$
in $\bigwedge(x_1, \ldots, x_p)$. We note that although we write $\varepsilon(\sigma)$, $\sigma$ does not suffice to define it as it depends also on the degrees of the various $x_i$.

