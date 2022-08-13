[[!redirects symmetric powers in symmetric monoidal (Q plus)-linear categories]]

#Contents#
* table of contents
{:toc}

##Idea

A conjectural characterization of [[symmetric powers]] in $\mathbb{Q}^{+}$-[[linear category|linear categories]] is given on this page. The description in terms of [[universal properties]] would be equivalent to a much longer one but much more constructive in algebraic terms. It would be similar to the characterization of products known as [[Fox theorem]] but where [[products]] are replaced by [[symmetric powers]]. We work in symmetric monoidal categories enriched over modules over a $\mathbb{Q}^{+}$-algebra. The adaptation to [[CMon-enriched symmetric monoidal categories]] would involve symmetric and [[divided powers]] which are equal in this simpler setting. This conjecture seems to be true and if it is really the case, the proof is not trivial.

##Conjecture
We suppose that the symmetric monoidal categories are strict monoidal categories.

\begin{definition}
We say that a symmetric monoidal category $\mathcal{C}$ possesses the $n$-th symmetric power ($n \ge 0$) iff it possesses this coequalizer for every $A \in \mathcal{C}$:
\begin{tikzcd}
A^{\otimes n} \arrow[rr, "\sigma", shift left=3] \arrow[rr, "...", shift right=3] &  & A^{\otimes n} \arrow[rr, "r_{n}(A)"] &  & S_{n}(A)
\end{tikzcd}
and $r_{n}(A):A^{\otimes n} \rightarrow S_{n}(A)$ is a natural transformation.
\end{definition}

\begin{definition}
A functorial special bicommutative graded bimonoid in a $CMon$-enriched symmetric monoidal category is given by:

* a family $(S_{n}:\mathcal{C}\rightarrow \mathcal{C})_{n \ge 0}$ of [[endofunctors]]
* a family $(\nabla_{n,p}:S_{n}(A) \otimes S_{p}(A) \rightarrow S_{n+p}(A))_{n,p \ge 0}$ of [[natural transformations]]
* a family $(\Delta_{n,p}:S_{n+p}(A) \rightarrow S_{n}(A) \otimes S_{p}(A))_{n,p \ge 0}$ of natural transformations

such that:

* $S_{0}(A)=I$
* $S_{1}(A)=A$
* for every $A \in \mathcal{C}$, $(A,(\nabla_{n,p})_{n,p \ge 0}, (\Delta_{n,p})_{n,p \ge 0})$) is a special bicommutative [[graded bimonoid]] ie.:

* $\gamma;\nabla_{p,n} = \nabla_{n,p}$ (commutativity)
* $\Delta_{p,n};\gamma = \Delta_{n,p}$ (cocommutativity)
* $\nabla_{n,0}=1$ (unitality)
* $\Delta_{n,0}=1$ (counitality)
* $(\nabla_{n,p} \otimes 1);\nabla_{n+p,q} = (1 \otimes \nabla_{p,q});\nabla_{n,p+q}$ (associativity)
* $\Delta_{n+p,q};(\delta_{n,p} \otimes 1) = \Delta_{n+p,q};(1 \otimes \Delta_{p,q})$
(coassociativity)
* if $n+p = q+r$, then $\nabla_{n,p};\Delta_{q,r} = \underset{\substack{a,b,c,d \ge 0 \\ a+b=n \\ c+d=p \\ a+c=q \\ b+d=r}}{\sum} (\Delta_{a,b} \otimes \Delta_{c,d});(1 \otimes \gamma \otimes 1);(\nabla_{a,c} \otimes \nabla_{b,d})$
(compatibility multiplication/comultiplication)
* $\Delta_{n,p};\nabla_{n,p} = \binom{n+p}{n}$
(specialty)

\end{definition}

\begin{conjecture}
Let $R$ be a $\mathbb{Q}^{+}$-algebra. Let $\mathcal{C}$ be a symmetric monoidal category enriched over $R$-modules. Let $(S_{n}:\mathcal{C} \rightarrow \mathcal{C})_{n \ge 0}$ be a family of endofunctors such that $S_{0}(A)=I$ and $S_{1}(A) = A$. Then, there is a bijection between families of natural transformations $(r_{n}(A):A^{\otimes_{n}} \rightarrow S_{n}(A))_{n \ge 0}$ which make $(S_{n}(A))$ symmetric powers and families of natural transformations $(\nabla_{n,p}:S_{n}(A) \otimes S_{p}(A) \rightarrow S_{n+p}(A))_{n,p \ge 0}, (\Delta_{n,p}:S_{n+p}(A) \rightarrow S_{n}(A) \otimes S_{p}(A))_{n,p \ge 0}$ which make $(S_{n}(A))$ a functorial special bicommutative graded bimonoid.
\end{conjecture}

## Towards a proof


### $n^{th}$ symmetric power in symmetric monoidal categories enriched over modules over a $\mathbb{Q}^{+}$-algebra

\begin{proposition}
Let $R$ be a $\mathbb{Q}^{+}$-algebra and $\mathcal{C}$ be a symmetric monoidal category enriched over $R$-modules. Let $n \ge 0$ and $S_{n}:\mathcal{C} \rightarrow \mathcal{C}$ be an endofunctor. There is a bijection between natural transformations $r_{n}:A^{\otimes n} \rightarrow S_{n}(A)$ which make $(S_{n}(A))$ symmetric powers and pairs of natural transformations $(r_{n}:A^{\otimes n} \rightarrow S_{n}(A), s_{n}:S_{n}(A) \rightarrow A^{\otimes n})$ such that:

* $s_{n};r_{n}=1:S_{n}(A) \rightarrow S_{n}(A)$
* $r_{n};s_{n} = \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\sigma:A^{\otimes n} \rightarrow A^{\otimes n}$

\end{proposition}
\begin{proof}
Suppose that we have a natural transformation $r_{n}:A^{\otimes n} \rightarrow S_{n}(A)$ which make $(S_{n}(A))$ symmetric powers. Define the natural transformation $e_{n}=\frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\sigma:A^{\otimes n} \rightarrow A^{\otimes}$. For every permutation $\rho \in \mathfrak{S}_{n}$, we have $\rho;e_{n}=\rho;\frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\sigma = \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\rho;\sigma $$= \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum} \sigma = e_{n}$ by using a change of variables in the last step. We thus have this factorization for every $A \in \mathcal{C}$:
\begin{tikzcd}
A^{\otimes n} \arrow[r, "r_{n}"] \arrow[rd, "e_{n}"'] & S_{n}(A) \arrow[d, "s_{n}"] \\
                                                      & A^{\otimes n}         
\end{tikzcd}
It is not difficult to show that $s_{n}:S_{n}(A) \rightarrow A^{\otimes n}$ is a natural transformation.

Moreover $r_{n};(s_{n};r_{n}) = (r_{n};s_{n});r_{n} = e_{n};r_{n} = (\frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\sigma);r_{n}$ $ = \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\sigma;r_{n} = \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}r_{n}=\frac{1}{n!}(n!r_{n})=r_{n}=r_{n};1$. We know that $r_{n}$ is an epimorphism and thus $s_{n};r_{n}=1$.

Suppose now that we have a pair of natural transformations $(r_{n}:A^{\otimes n} \rightarrow S_{n}(A), s_{n}:S_{n}(A) \rightarrow A^{\otimes n})$ such that:

* $s_{n};r_{n}=1:S_{n}(A) \rightarrow S_{n}(A)$
* $r_{n};s_{n} = \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\sigma:A^{\otimes n} \rightarrow A^{\otimes n}$

Suppose that $f:A^{\otimes n} \rightarrow B$ is a morphism such that $\sigma;f=f$ for every $\sigma \in \mathfrak{S}_{n}$. Then $r_{n};(s_{n};f)=(r_{n};s_{n});f=(\frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum}\sigma);f = \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum} \sigma;f = \frac{1}{n!} \underset{\sigma \in \mathfrak{S}_{n}}{\sum} f = \frac{1}{n!}(n!f)=f$. Suppose now that we have a morphism $g:S_{n}(A) \rightarrow B$ such that $f=r_{n};g$. Then, $s_{n};f=s_{n};(r_{n};g)=(s_{n};r_{n});g=g$. $s_{n};f$ is thus the only morphism $S_{n}(A) \rightarrow B$ such that $f=r_{n};(s_{n};f)$. Thus, $r_{n}:A^{\otimes n} \rightarrow S_{n}(A)$ makes $(S_{n}(A))$ symmetric powers.

\end{proof}

With this equivalent definition, we have already replaced the universal property defining symmetric powers by two natural transformations which verify some equations. The work is now to show the equivalence between these two equations and the ones defining a functorial special bicommutative graded bimonoid.


### From symmetric powers to creation/annihilation operators

\begin{definition}
Let $R$ be $\mathbb{Q}^{+}$-algebra and $\mathcal{C}$ a symmetric monoidal category enriched over $R$-modules. Suppose that we have a family $(S_{n}:\mathcal{C} \rightarrow \mathcal{C})_{n \ge 0}$ of endofunctors such that $S_{0}(A)=I$ and $S_{1}(A)=A$. Creation/annihilation operators are defined as two families $(c_{n}:S_{n}(A) \otimes A \rightarrow S_{n+1}(A))_{n \ge 0}$ and $(a_{n}:S_{n}(A) \rightarrow S_{n-1}(A) \otimes A)_{n \ge 1}$ such that:

[[n12.jpg:pic]]

and:

[[specialop2.jpg:pic]]

where $k$ must be read as $S_{k}(A)$. Be aware that "$n.$" depicts the multiplication by the scalar $n$.

\end{definition}

\begin{proposition}
Let $R$ be $\mathbb{Q}^{+}$-algebra and $\mathcal{C}$ a symmetric monoidal category enriched over $R$-modules. Suppose that we have a family $(S_{n}:\mathcal{C} \rightarrow \mathcal{C})_{0 \le n \le p}$ of endofunctors such that $S_{0}(A)=I$ and $S_{1}(A)=A$. Suppose that we have a family $(r_{n}:A^{\otimes n} \rightarrow S_{n}(A))_{0 \le n \le p}$ of natural transformations which make $(S_{n}A)_{0 \le n \le p}$ symmetric powers. We define creation/annihilation operators (for $0$ to $p$ particles) by putting:

\begin{tikzcd}
S_{n}(A) \otimes A \arrow[d, "s_{n} \otimes 1"'] \arrow[rd, "c_{n}"] &            &  & S_{n+1}(A) \arrow[d, "s_{n+1}"'] \arrow[rd, "a_{n}"] &                    \\
A^{\otimes (n+1)} \arrow[r, "r_{n+1}"']                              & S_{n+1}(A) &  & A^{\otimes (n+1)} \arrow[r, "r_{n}\otimes 1"']       & S_{n}(A) \otimes A
\end{tikzcd}

\end{proposition}

### From symmetric powers to functorial special bicommutative graded bimonoid

\begin{proposition}
Let $R$ be $\mathbb{Q}^{+}$-algebra and $\mathcal{C}$ a symmetric monoidal category enriched over $R$-modules. Suppose that we have a family $(S_{n}:\mathcal{C} \rightarrow \mathcal{C})_{0 \le n \le p}$ of endofunctors such that $S_{0}(A)=I$ and $S_{1}(A)=A$. Suppose that we have a family $(r_{n}:A^{\otimes n} \rightarrow S_{n}(A))_{0 \le n \le p}$ of natural transformations which make $(S_{n}A)_{0 \le n \le p}$ symmetric powers. We define a (bounded) functorial special bicommutative graded bimonoid by putting:

\begin{tikzcd}
S_{n}(A) \otimes S_{n'}(A) \arrow[d, "s_{n} \otimes s_{n'}"'] \arrow[rd, "{\nabla_{n,n'}}"] &            &  & S_{n+n'}(A) \arrow[d, "s_{n+n'}"'] \arrow[rd, "{\Delta_{n,n'}}"] &                           \\
A^{\otimes (n+n')} \arrow[r, "r_{n+n'}"']                                                  & S_{n+n'}(A) &  & A^{\otimes(n+n')} \arrow[r, "r_{n} \otimes r_{n'}"']            & S_{n}(A) \otimes S_{n'}(A)
\end{tikzcd}

for all $0 \le n,n' \le p$ such that $0 \le n+n' \le p$.

\end{proposition}

## Related concepts

[[graded codifferential category]]