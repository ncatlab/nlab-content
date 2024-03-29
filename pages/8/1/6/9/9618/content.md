
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}



An image of a variety under a regular map is not necessarily a variety. A standard example is to take the map $\mathbf{A}^2\to\mathbf{A}^2$ which takes $(x,y)\mapsto (x,x y)$; the image of the affine plane consists of all points $(x,y)$ with $x\neq 0$ union $(0,0)$. This set is clearly not locally closed, hence not a quasiaffine subvariety of $\mathbf{A}^2$.

However, the image of a variety under a regular map is always a [[constructible set]] (finite union of [[locally closed set]]s). More generally, 

THEOREM. (Chevalley) If $f: X\to Y$ is a regular morphism of varieties and $S\subset X$ is a Zariski constructible set. Then $f(S)$ is also Zariski constructible. 

More generally,

Theorem ([[EGA]] IV 1.8.4.) If $f:X\to Y$ is a finitely presented morphism of schemes. Then the image of any constructible subset of $X$ under $f$ is a constructible subset of $Y$. 

## Related entries

* [[tame topology]]

## Links

* MathOverflow [chevalleys-theorem-on-constructible-sets](http://mathoverflow.net/questions/80707/chevalleys-theorem-on-constructible-sets)

The relation to the [[elimination of quantifiers]] for the theory of algebraically closed fields is discussed in 

* D. Sustretov, blog: [model theory IV: algebraically closed fields and compact complex manifolds](http://shenme.de/blog/posts/2012-08-28-model-theory-algebraically-closed-fields-and-compact-complex-manifelds.html)

## Reference

* [[André Joyal|A. Joyal]], _Les Th&#233;or&#232;mes de Chevalley-Tarski et Remarques sur l'Alg&#232;bre Constructive_ , Cah. Top. G&#233;om. Diff. Cat. **XVI** (1975) pp.256-258. ([Proceedings Colloque Amiens 1975](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1975__16_3/CTGDC_1975__16_3_217_0/CTGDC_1975__16_3_217_0.pdf), 6.81 MB)

category: algebraic geometry

[[!redirects Chevalley-Tarski theorem]]