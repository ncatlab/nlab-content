

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


\tableofcontents

## Definition

In [[dependent type theory]] with [[identity types]], [[equivalence types]], and [[dependent function types]], **equivalence extensionality** characterizes the identity type of equivalence types and is the property that for all [[equivalence in type theory|equivalences]] $f:A \simeq B$ and $g:A \simeq B$, there are equivalences

$$
  \mathrm{equivext}(f, g)  
  \;\;\colon\;\;
  \big(f =_{A \simeq B} g\big) 
  \;\simeq\; 
  \prod_{x \colon A} 
  \,
  f(x) =_{B} g(x)
  \,.
$$

\begin{prop}
Equivalence extensionality is equivalent to [[function extensionality]].
\end{prop}

\begin{proof}
Function extensionality implies equivalence extensionality because, in the presence of function extensionality, the property of being an equivalence is a proposition.

For the converse, we show that equivalence extensionality implies [[weak function extensionality]] (which implies function extensionality).
Let $X$ be a type and $Y$ be a family of contractible types indexed by $X$. 
The projection map $\pi \colon \sum_{x \colon X} Y(x) \to X$ is an equivalence.
By equivalence extensionality, it follows that post-composition with $\pi$ defines an equivalence $\pi_! \colon (X \simeq \sum_{x \colon X} Y(x)) \simeq (X \simeq X)$.
In particular, the fiber of $\pi_!$ at the identity equivalence $id_X$ is contractible.
One can show (again using equivalence extensionality) that $\prod_{x \colon X} Y(x)$ is a retract of the fiber of $\pi_!$ at $id_X$: there is a section sending $f \colon \prod_{x \colon X} Y(x)$ to $x \mapsto (x, f(x)) \colon X \simeq \sum_{x \colon X} Y(x)$ and a retraction sending $e \colon X \simeq \sum_{x \colon X} Y(x)$ with $\pi_!e = id_X$ to $x \mapsto snd(e(x))$ (modulo transport).
Thus $\prod_{x \colon X} Y(x)$ is also contractible.
\end{proof}

## See also

* [[equivalence type]]

* [[equivalence of types]]

* [[extensionality]]

## References

Proof that equivalence extensionality implies function extensionality in [[Agda]]:

* [[TypeTopology]], *[UF.FunExt-Properties.equivext-gives-funext](https://martinescardo.github.io/TypeTopology/UF.FunExt-Properties)*