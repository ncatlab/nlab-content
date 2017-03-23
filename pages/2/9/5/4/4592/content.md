


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[smooth manifold]] $M$ and a vector field $X \in \Gamma(T M)$ on it, one defines a series of operators $\mathcal{L}_X$ on spaces of differential forms, of functions, of vector fields and multivector fields. 
For functions $\mathcal{L}_X(f) = X(f)$ (derivative of $f$ along an integral curve of $X$); as multivector fields and forms can not be compared in different points, one pullbacks or pushforwards them to be able to take a derivative. 


For vector fields $\mathcal{L}_X Y = [X,Y]$. If $\omega \in \Omega^\bullet(M)$ is a [[differential form]] on $M$, the **Lie derivative** $\mathcal{L}_X \omega$ of $\omega$ along $X$ is the linearization of the pullback of $\omega$ along the flow $\exp(X -) : \mathbb{R} \times M\to M$ induced by $X$

$$
  \mathcal{L}_X \omega = \frac{d}{d t}|_{t = 0} \exp(t X)^*(\omega)
  \,.
$$
Denote by $\iota_X : \Omega^\bullet(M) \to \Omega^{\bullet -1}(M)$ be the graded [[derivation]] which is the [[contraction]] with a vector field $X$. By [[Cartan's homotopy formula]], 

$$
  \mathcal{L}_v = [d_{dR}, \iota_v] = d_{dR} \circ \iota_v + \iota_v \circ d_{dR} : \Omega^\bullet(X) \to \Omega^\bullet(X)
  \,.
$$

## References

An introduction in the context of [[synthetic differential geometry]] is in 

* [[Gonzalo Reyes]], _Lie derivatives, Lie brackets and vector fields over curves_, [pdf](https://marieetgonzalo.files.wordpress.com/2006/10/lie-derivatives.pdf)

A gentle elementary introduction for mathematical physicists 

* Bernard F. Schutz, *Geometrical methods of mathematical physics* (elementary intro) [amazon](http://www.amazon.com/Geometrical-Methods-Mathematical-Physics-Bernard/dp/0521298873), [google](http://books.google.hr/books?id=HAPMB2e643kC&lpg=PP1&dq=schutz%20geometrical%20methods&pg=PP1#v=onepage&q&f=false)

[[!redirects Lie derivatives]].