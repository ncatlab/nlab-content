

#Contents#
* table of contents
{:toc}

## Definition

Consider a [[real numbers|real]]-valued [[smooth function]]

\[
  \label{TheFunction}
  f \colon M \longrightarrow \mathbb{R}
\] 

on a [[smooth manifold]] $M$. 


\begin{definition}
  \label{CriticalPoint}
A point $p\in M$ is a **critical point** of $f$ (eq:TheFunction) if for any smooth [[curve]] $\gamma : (-\epsilon, \epsilon)\to M$ with $\gamma(0)=p$, the [[tangent vector]]

$$
  \frac{d(f\circ\gamma)}{dt} |_{t=0} = 0
  \,.
$$

The critical point is **regular** if for one (or equivalently any) [[chart]] $\phi : U^{\open}\to \mathbb{R}^n$, where $p\in U$ and $\phi(p) = 0\in \mathbb{R}^n$, the **Hessian matrix**

$$\left(\frac{\partial^2 (f\circ \phi^{-1})}{\partial x^i\partial x^j}(0)\right)_{i,j=1,\ldots, n} $$

is a nondegenerate (i.e. maximal rank) matrix. 
\end{definition}


\begin{definition}
The function $f$ is called a **Morse function** if every [[critical point]] of $f$ is [[regular value|regular]] (Def. \ref{CriticalPoint}).
\end{definition}


A choice of a Morse function on a compact manifold is often used to study topology of the manifold. This is called the [[Morse theory]].  

## Properties

One of the basic tools of [[Morse theory]] is the _[[Morse lemma]]_.

## Related concepts

* [[perfect Morse function]] 

## References

See also:

* Wikipedia, _[Morse theory](http://en.wikipedia.org/wiki/Morse_theory)_

[[!redirects Morse functions]]