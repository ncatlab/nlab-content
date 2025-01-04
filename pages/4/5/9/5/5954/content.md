[[!redirects ∞-module over an ∞-algebra over an (∞,1)-operad]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

(under construction)

#Contents#
* table of contents
{:toc}


## Idea

(...)

## As stabilization

Let $\mathcal{O}^{\otimes}$ be a reduced [[coherent (∞,1)-operad]] and $\mathcal{C}^{\otimes}$ be a stable $\mathcal{O}$-monoidal $\infty$-category (that is, an $\mathcal{O}$-algebra in the $\infty$-category of stable $\infty$-categories and exact functors).
Then, Theorem 7.3.4.13 of ([Lurie](#Lurie)) presents $\mathcal{O}$-$A$-modules as _stabilization_ of $\mathcal{O}$-algebras over $A$.

\begin{theorem}
  The stabilization $\mathrm{Sp}(\Alg_{\mathcal{O}}(\mathcal{C})_{/A})$ is canonically equivalent to $\mathrm{Mod}_A^{\mathcal{O}}$.
\end{theorem}

The associated suspension-loops adjunction is an $\mathcal{O}$-algebra version of the adjunction between cotangent complexes and split square-zero extensions.
To see the theorem, begin by noting that the we may reduce to the case of the $\mathcal{O}$-monoidal unit $\mathrm{A} = 1$ by expressing $\mathcal{O}$-$A$-algebras as $\mathcal{O}$-algebras _under_ $A$:
\begin{equation}
  \begin{split}
\mathrm{Sp}(\mathrm{Alg}_{\mathcal{O}}(\mathcal{C})_{/A}) 
&\simeq
\mathrm{Sp}((\mathrm{Alg}_{\mathcal{O}}(\mathcal{C})_{/A})_*) \\
&\simeq
\mathrm{Sp}((\mathrm{Alg}_{\mathcal{O}}(\mathcal{C})_{A//A})) \\
&\simeq
\mathrm{Sp}((\mathrm{Alg}^{\mathrm{Aug}}_{\mathcal{O}}(\mathrm{Mod}_A^{\mathcal{O}}\mathcal{C}))).
\end{split}
\end{equation}
To see this in the unital case, taking Kernels of the augmentation yields a monadic "augmentation ideal" functor
\[
  I\colon \mathrm{Alg}_{\mathcal{O}}^{\mathrm{aug}}(\mathcal{C}) \rightarrow \mathcal{C}
\]
whose associated monad corresponds with the positive-arity $\mathcal{O}$-symmetric powers:
\[
  T_I(X) \simeq \bigoplus_{n > 0} \left(\mathcal{O}(n) \times X^{\otimes n} \right)_{h\Sigma_n}.
\]
By stability of $\mathcal{C}$, the augmentation ideal factors through a monadic functor $\partial I\colon \mathrm{Sp}(\mathrm{Alg}^{\mathrm{aug}}(\mathcal{C}) \rightarrow \mathcal{C}$ which turns out to be the first Goodwillie derivative
\[
  \partial I(X) \simeq \colim_{n} \Omega^n I(\Sigma^n X).
\]
Intuitively, when $n \geq 2$, the $X^{\otimes n}$ term in the monad $T_{\partial I}(X)$ is a colimit of spaces becoming arbitrarily highly connected, so it is contractible, demonstrating that $T_{\partial I}(X)$ is the identity monad.

## Related concepts

* [[∞-module]]

* [[(∞,1)-operad]], [[model structure on operads]]

  * [[algebra over an (∞,1)-operad]], [[model structure on algebras over an operad]]

    * **module over an algebra over an (∞,1)-operad**, [[model structure on modules over an algebra over an operad]]

## References

Section 3.3.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}