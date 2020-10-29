
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

Let $M$ be a [[differentiable manifold]], $X$ a [[vector field]] on $M$, and $\mathcal{L}_X$ the [[Lie derivative]] along $X$. The contraction of a vector field and a $k$-form $\omega$ is denoted in modern literature by $X \rfloor \omega$ (should be lrcorner instead of rfloor LaTeX command, but it does not work in iTeX) or $\iota_X \omega$ or $\iota(X)(\omega)$.

Then the __Cartan's infinitesimal homotopy formula__, nowdays called simply Cartan's homotopy formula or even Cartan formula, says

$$
\mathcal{L}_X \omega = d \iota(X)\omega + \iota(X) d\omega
$$

The word "homotopy" is used because it supplies a homotopy operator for some manipulation with chain complexes in [[de Rham cohomology]]. Cartan's homotopy formula is part of [[Cartan calculus]]. 

Regarding that the Cartan's formula can be viewed as a formula about the [[de Rham complex]], which has generalizations, one can often define
the Cartan's formulas for those generalizations. For example 

## Related concepts

* [[Cartan calculus]]

* [[Cartan's map]]

## References

* [[Masoud Khalkhali]], _On Cartan homotopy formulas in cyclic homology_, Manuscripta mathematica __94__:1, pp 111-132 (1997) [doi](http://dx.doi.org/10.1007/BF02677842) 

See also [[noncommutative differential calculus]] where it is incorporated into the notion of Batalin-Vilkovisky module over a [[Gerstenhaber algebra]].

[[!redirects Cartan's magic formula]]

[[!redirects Cartan homotopy formula]]
