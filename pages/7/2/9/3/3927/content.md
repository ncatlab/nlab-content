
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[structure]] of a [[braided monoidal category]] on top of the [[underlying]] [[monoidal category]] with [[tensor product]] "$\otimes$" is a [[natural isomorphism]] of the form

$$
  B_{x,y} 
    \;\colon\; 
  x \otimes y 
    \longrightarrow 
  y \otimes x 
  \,,
$$

called the **braiding**.

A braided monoidal category is called *[[symmetric monoidal category|symmetric]]* if and only if $B_{x,y}$ and $B_{y,x}$ are [[inverse morphisms]] to each other (while they are [[isomorphisms]] in any case).

## Examples

\begin{example}
\label{BraidingOnPlainModules}
In [[Vect]] (or generally [[Mod]]), the braiding maps elements $a\otimes b$ of a [[tensor product of vector spaces]] ([[tensor product of modules|of modules]]) $X \otimes Y$ to $b \otimes a$. 
\end{example}

\begin{example}
The braiding for the [[tensor product of chain complexes]] and that of [[super vector spaces]] is as in Exp. \ref{BraidingOnPlainModules} up to multiplication by sign $a \otimes b \mapsto (-1)^{deg(a) deg(b)} (b \otimes a)$ (see at *[[signs in supergeometry]]*).
\end{example}

## Related concepts

* [[braid group]]

## References

See the references at *[[braided monoidal category]]*


[[!redirects braidings]]