

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

One of the basic facts of [[category theory]] is that the [[hom-functor]] on a [[category]] $\mathcal{C}$ [[preserved limit|preserve]] [[limits]] in both [[variables]] separately (remembering that a limit in the first variable, due to contravariance, is actually a [[colimit]] in $\mathcal{C}$).

## Statement

### Ordinary hom-functor

\begin{proposition}
  \label{HomFunctorPreservesLimits}
**([[hom-functor]] [[preserved limit|preserves]] [[limits]])**

Let $\mathcal{C}$ be a [[category]] and write

$$

  Hom_{\mathcal{C}}
   \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
   \longrightarrow
  Set
$$

for its [[hom-functor]]. This [[preserved limit|preserves]] [[limits]] in both its arguments (recalling that a limit in the [[opposite category]] $\mathcal{C}^{op}$ is a [[colimit]] in $\mathcal{C}$).

In more detail, let $X_\bullet \colon \mathcal{I} \longrightarrow \mathcal{C}$ be a [[diagram]]. Then:

1. If the [[limit]] $\underset{\longleftarrow}{\lim}_i X_i$ exists in $\mathcal{C}$ then for all $Y \in \mathcal{C}$ the functor $Hom_{\mathcal{C}}(Y, -)$ preserves this limit.

2. If the [[colimit]] $\underset{\longrightarrow}{\lim}_i X_i$ exists in $\mathcal{C}$ then for all $Y \in \mathcal{C}$ the functor $Hom_{\mathcal{C}}(-, Y)$ preserves it (viewing it as a limit over $X_\bullet^{op}$).


\end{proposition}

\begin{proof}
  We give the proof of the first statement. The proof of the second statement is [[formal dual|formally dual]].
Let $(L, \lambda_i)$ be a limit of $X_\bullet$, consisting of an object $L \in \mathcal{C}$ and a family of maps $\lambda_i \colon L \to X_i$ forming a limit cone. Our task is to show that $(Hom_\mathcal{C}(Y, L), Hom_\mathcal{C}(Y, \lambda_i))$ is a limit cone in $Set$.

So, take a set $S$ equipped with a family of maps $\alpha_i \colon S \to Hom_\mathcal{C}(Y, X_i)$ that form a cone, meaning for every $f \colon X_i \to X_j$ we have that $Hom_\mathcal{C}(Y, f) \circ \alpha_i = \alpha_j$. We need to show that there exists a unique morphism $\alpha \colon S \to Hom_\mathcal{C}(Y, L)$ such that $\alpha_i = Hom_\mathcal{C}(Y, \lambda_i) \circ \alpha$ for every $i \in \mathcal{I}$.

Unpacking the definition of the hom-functor, we obtain:

* For every $s \in S$, a map $\alpha_i(s) \colon Y \to X_i$.
* The compatibility condition $f \circ \alpha_i(s) = \alpha_j(s)$ for every $f \colon X_i \to X_j$.
* The requirement to find, for each $s \in S$, a unique $\alpha(s) \colon Y \to L$ such that $\alpha_i(s) = \lambda_i \circ \alpha(s)$.

But elementwise, the first two bulletpoints are the data of a cone over $X_\bullet$ with tip $Y$, and the third is obtained from the unique morphism $Y \to L$ factorising this cone through the limit cone $(L, \lambda_i)$. Thus, taking these together for each $s \in S$ provides the required unique factorisation $\alpha \colon S \to Hom_\mathcal{C}(Y, L)$.
\end{proof}

### Internal hom-functor
 {#InternalHomFunctor}


+-- {: .num_prop #InternalHomPreservesLimits}
###### Proposition
**(internal hom-functor preserves limits)**

Let $\mathcal{C}$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with [[internal hom]]-[[bifunctor]] $[-,-]$. Then this bifunctor preserves [[limits]] in the second variable, and sends colimits in the first variable to limits:

$$
  [X, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} Y(j)]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [X, Y(j)]
$$

and

$$
  [\underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j),X]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j),X]  
$$


=--


+-- {: .proof}
###### Proof

For $X \in \mathcal{C}$ any object, $[X,-]$ is a [[right adjoint]] by definition, and hence preserves limits as _[[adjoints preserve (co-)limits]]_.

For the other case, let $Y \;\colon\; \mathcal{L} \to \mathcal{C}$ be a [[diagram]] in $\mathcal{C}$, and let $C \in \mathcal{C}$ be any object. Then there are isomorphisms

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(C, [ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X ] )
    & \simeq
    Hom_{\mathcal{C}}( C \otimes \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X )
    \\
    & \simeq
    Hom_{\mathcal{C}}( \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} (C \otimes Y(j)), X )   
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( (C \otimes Y(j)), X )    
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( C, [Y(j), X] )    
    \\
    & \simeq
    Hom_{\mathcal{C}}( C, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] )    
  \end{aligned}
$$

which are [[natural isomorphism|natural]] in $C \in \mathcal{C}$, where we used that the ordinary [[hom-functor]] respects (co)limits as shown (see at _[[hom-functor preserves limits]]_), and that the [[left adjoint]] $C \otimes (-)$ preserves colimits (see at _[[adjoints preserve (co-)limits]]_).

Hence by the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]], there is an isomorphism

$$
  \left[ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X \right]  
  \overset{\simeq}{\longrightarrow}
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] 
  \,.
$$


=--




## Related statements

* [[limits preserve limits]]

* [[adjoints preserve (co-)limits]]

* [[limits commute with limits]]

* [[limits of presheaves are computed objectwise]]


[[!redirects hom-functors preserve limits]]

[[!redirects internal hom-functor preserves limits]]
[[!redirects internal hom-functors preserve limits]]


