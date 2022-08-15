
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