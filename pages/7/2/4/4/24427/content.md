
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

A graded bimonoid is like a [[bimonoid]] but graded, as a [[graded monoid]], with [[underlying]] [[graded object]] $(A_{n})_{n \ge 0}$. We suppose in this entry, that the graduations are taken with indexes in $\mathbb{N}$. The multiplication, comultiplication, unit and counit are defined as morphisms which respect the grading.

Whereas we're not sure if the notion of graded bimonoid under this form is new or not, the notion of special graded bimonoid below is certainly.

Under the conjecture of the page [[symmetric powers in a symmetric monoidal (Q plus)-linear category]], bicommutative special graded bimonoids with trivial units are necessarily given by the [[symmetric powers]] of the [[object]] $A_{1}$.

## Definition

A graded bimonoid in a [[CMon-enriched symmetric monoidal category]] is given by a family $(A_{n})_{n \ge 0}$ of objects, a family $(\nabla_{n,p}:A_{n} \otimes A_{p} \rightarrow A_{n+p})_{n,p \ge 0}$ of morphisms, a family $(\Delta_{n,p}:A_{n+p} \rightarrow A_{n} \otimes A_{p})_{n,p \ge 0}$ of morphisms, a morphism $\eta:I \rightarrow A_{0}$ and a morphism $\epsilon:A_{0} \rightarrow I$ which verify some coherences (often, we don't write the indexes under $\Delta$ or $\nabla$):

* $((A_{n})_{n \ge 0},(\nabla_{n,p})_{n,p \ge 0}, \eta)$ is a [[graded monoid]]
* $((A_{n})_{n \ge 0},(\Delta_{n,p})_{n,p \ge 0}), \epsilon)$ is a [[graded comonoid]]
* Compatibility multiplication/comultiplication:

If $n,p,q,r \ge 0$ are such that $n+p=q+r$ ($n$ must be read as $A_{n}$ in the string diagrams):
\begin{imagefromfile}
        "file_name": "mult-comult.jpg",
        "width": 350
    \end{imagefromfile}

* Compatibility counit/multiplication:

\begin{tikzcd}
A_{0} \otimes A_{0} \arrow[rr, "\nabla"] \arrow[rd, "\epsilon \otimes \epsilon"'] &                     & A_{0} \arrow[ld, "\epsilon"] \\
                                                                                  & I \otimes I \cong I &                             
\end{tikzcd}

* Compatibility unit/comultiplication:

\begin{tikzcd}
I \cong I \otimes I \arrow[rd, "\eta \otimes \eta"] \arrow[d, "\eta"'] &                     \\
A_{0} \arrow[r, "\Delta"']                                             & A_{0} \otimes A_{0}
\end{tikzcd}

* Compatibility unit/counit:

\begin{tikzcd}
I \arrow[d, "\eta"'] \arrow[rd, "Id"] &   \\
A_{0} \arrow[r, "\epsilon"']          & I
\end{tikzcd}

## Special graded bimonoid

* We say that a graded bimonoid is special if it verifies moreover that:

\begin{tikzcd}
A_{n+p} \arrow[d, "\Delta"'] \arrow[rd, "{n+p \choose n}Id"] &         \\
A_{n} \otimes A_{p} \arrow[r, "\nabla"']                     & A_{n+p}
\end{tikzcd}

* We say that a graded bimonoid is bicommutative if the underlying graded monoid is commutative and the underlying graded comonoid is cocommutative.

* We say that a graded bimonoid has trivial units if:
  - $\eta$ is an isomorphism (equivalently, $\epsilon$ is an isomorphism)
  - $\nabla_{n,p}$ is an isomorphism if either $n = 0$ or $p = 0$ (we have these equivalences with further properties assumed: $\nabla_{n,0}$ is an isomorphism iff $\nabla_{0,n}$ is an isomorphism in case of commutativity, $\Delta_{n,0}$ is an isomorphism iff $\Delta_{0,n}$ is an isomorphism in case of cocommutativity, $\nabla_{n,0}$ is an isomorphism iff $\Delta_{n,0}$ is an isomorphism in case of specialty and $\nabla_{0,n}$ is an isomorphism iff $\Delta_{0,n}$ is an isomorphism in case of specialty).

Under the conjecture of the page [[symmetric powers in a symmetric monoidal (Q plus)-linear category]], we have:

\begin{conjecture}
Suppose that $\mathcal{C}$ is a symmetric monoidal $\mathbb{Q}^{+}$-linear category. If $(A_{n})_{n \ge 0}$ is the underlying graded object of a special bicommutative graded bimonoid with trivial units, then each $A_{n}$ is a $n^{th}$ symmetric power of $A_{1}$.
\end{conjecture}

Note that for a special bicommutative graded bimonoids, the condition of trivial units is equivalent to:
  
  - $\eta$ is an isomorphism
  - $\nabla_{n,0}$ is an isomorphism for every $n \ge 0$

Of course, if our category possesses the symmetric powers of an object, we also generate a special bicommutative graded bimonoid with trivial units by taking $A_{n} = A^{\otimes_{s}n}$. Let's see how it works in a concrete case. Suppose that $\mathbb{K}$ is a field of characteristic $0$. Take a vector space $A$ of basis $X_{1},...,X_{q}$. Then $A^{\otimes_{s}m} \cong \mathbb{K}_{m}[X_{1},...,X_{q}]$, the space of [[homogeneous polynomials]] of degree $m$ in the variables $X_{1},...,X_{q}$. The unit $\mathbb{K} \cong \mathbb{K}_{0}[X_{1},...,X_{q}]$ and the multiplication $\mathbb{K}_{m}[X_{1},...,X_{q}] \otimes \mathbb{K}_{n}[X_{1},...,X_{q}] \rightarrow \mathbb{K}_{m+n}[X_{1},...,X_{q}]$ are straightforward as well as the counit $\mathbb{K}_{0}[X_{1},...,X_{n}] \cong \mathbb{K}$.
The comultiplication 
$$\mathbb{K}_{m+n}[X_{1},...,X_{q}] \rightarrow \mathbb{K}_{m}[X_{1},...,X_{q}] \otimes \mathbb{K}_{n}[X_{1},...,X_{q}]$$
is defined by:
$$
X_{i_{1}}...X_{i_{m+n}} \mapsto \frac{1}{n!p!}\underset{\sigma \in \mathfrak{S}_{n+p}}{\sum} X_{\sigma(i_{1})}...X_{\sigma(i_{n})} \otimes X_{\sigma(i_{n+1})}...X_{\sigma(i_{n+p})}
$$
The intuition is that it takes a monomial of degree $n+p$, decomposes it in all the possible decompositions of a monomial of degree $n$ and a monomial of degree $p$ and then sum all the possibilites (however, the result is obtained by considering the different instances of a variable in a monomial as different entities). For example:
$$
\Delta_{2,2}(XYZW) = XY \otimes ZW + XZ \otimes YW + XW \otimes YZ + YZ \otimes ZW + YW \otimes XZ + ZW \otimes XY
$$
and 
$$
\Delta_{2,2}(XYZ^{2}) = XY \otimes Z^{2} + XZ \otimes YZ + XZ \otimes YZ + YZ \otimes Z^{2} + YZ \otimes XZ + Z^{2} \otimes XY
$$
$$
= XY \otimes Z^{2} + 2XZ \otimes YZ + 2YZ \otimes Z^{2} + Z^{2} \otimes XY 
$$
The number of decomposition of a monomial of degree $n+p$ in one part of degree $n$ and one part of degree $p$ is equal to the number of choice of $n$ of the variables in the monomial amongst the $n+p$ which appear, thus $\binom{n+p}{n}=\frac{(n+p)!}{n!p!}$. When we recompose the two part of the decomposition together, we find each time the same compositie that we had at the beginning. Thus, the result of the decomposition followed by the recomposition is nothing more than a multiplication by the scalar $\binom{n+p}{n}$.
$$
\nabla_{2,2}(\Delta_{2,2}(XYZW)) = \binom{2+2}{2}XYZW = 6XYZW
$$
$$
\nabla_{2,2}(\Delta_{2,2}(XYZ^{2})) = \binom{2+2}{2}XYZ^{2} = 6XYZ^{2}
$$

The comultiplication can be expressed using the [[Hasse-Schmidt derivative]]. As explained in the referred entry, for any commutative rig $R$, given a monomial $P \in R_{m+n}[X_{1},...,X_{q}]$ and a monic monomial $Y_{1}...Y_{p} \in R_{p}[X_{1},...,X_{q}]$, equivalently a multiset of $p$ variables in $\{X_{1},...,X_{q}\}$, the Hasse-Schmidt derivative $D_{Y_{1}...Y_{p}}(P)$ is the number of way of extracting $Y_{1}...Y_{p}$ from $P$, multiplied by $\frac{P}{Y_{1}...Y_{p}}$. If there is no way of extracting $Y_{1}...Y_{p}$, ie. if $Y_{1}...Y_{p}$ isn't a divisor of $P$, then $D_{Y_{1}...Y_{p}}(P)=0$. The comultiplication $\Delta_{m,n}:R_{m+n}[X_{1},...,X_{q}] \rightarrow R_{m}[X_{1},...,X_{q}] \otimes R_{n}[X_{1},...,X_{q}]$ can thus be expressed without using any rational coefficient, ie. without assuming that $R$ is a field of characteristic $0$, or more generally a $\mathbb{Q}^{+}$-algebra. It is then expressed in this way, for any $P \in R_{m+n}[X_{1},...,X_{q}]$ (writing $\mathcal{M}_{p}(X_{1},...,X_{q})$ for the set of all multisets of $p$ elements in $\{X_{1},...,X_{q}\}$):
$$
\Delta_{n,p}(P) = \underset{Y_{1}...Y_{p} \in \mathcal{M}_{p}(X_{1},...,X_{q})}{\sum} D_{Y_{1}...Y_{p}}(P) \otimes Y_{1}...Y_{p}
$$
Unpacking the definition of the Hasse-Schmidt derivative, it is defined on a monomial $P=\lambda.W_{1}...W_{n+p}$ by:
$$
\Delta_{n,p}(P) = \underset{\substack{Y_{1}...Y_{p} \in \mathcal{M}_{p}(X_{1},...,X_{q}) \\ Y_{1}...Y_{p} | P}}{\sum}\left[\underset{\substack{1 \le i \le q \\ X_{i} | Y_{1}...Y_{n}}}{\prod}\binom{nbr\;of\;time\;X_{i}\;in\;P}{nbr\;of\;time\;X_{i}\;in\;Y_{1}...Y_{n}}\right]\frac{P}{Y_{1}...Y_{n}} \otimes Y_{1}...Y_{n}
$$
and then prolongated by linearity:
$$
\Delta_{n,p}(P+Q) = \Delta_{n,p}(P)+\Delta_{n,p}(Q)
$$
in order to define it for every homogeneous polynomial. If this formula looks more intimidating that the one defined by a sum on $\mathfrak{S}_{n+p}$ in characteristic $0$, it is in fact nothing more than a precise formula to express the fact that $\Delta_{n,p}(P)$ for a monomial $P$ of degree $n+p$, is the sum of all the decompositions of $P$ in one part of degree $n$ and one part of degree $p$. Such a [[combinatorial]] description have the virtue of not requiring some divisions which are forbidden in [[positive characteristic]]. 

## Properties

* With the above notations, if we have a graded bimonoid, then $(A_{0},\nabla_{0,0}, \Delta_{0,0}, \eta, \epsilon)$ is a bimonoid.

* Suppose that our [[CMon-enriched symmetric monoidal category]] possesses a [[zero object]] such that $A \otimes 0 \cong 0$ for every object $A$. We can then associate a graded bimonoid to every bimonoid by putting:
  - $A_{0} = A$
  - $\nabla_{0,0} = \nabla$
  - $\Delta_{0,0} = \Delta$
  - $A_{n} = 0$ if $n \ge 1$

## Related concepts

[[bimonoid]]

[[symmetric powers in a symmetric monoidal (Q plus)-linear category]]

[[graded codifferential category]]

[[Hasse-Schmidt derivative]]