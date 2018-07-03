# Soft linear logic

* table of contents
{: toc}

## Idea

Soft linear logic is a version of [[linear logic]] in which the [[exponential modality]] is weakened.  This has as a particular consequence that the only "definable functions" (in various senses) are computable in [[polynomial time]].

## Definition

The usual rules of the exponential modality $!$ in (intuitionistic) linear logic are promotion, dereliction, contraction, and weakening:

$$\frac{!\Gamma\vdash A}{!\Gamma\vdash !A}(prom) \qquad \frac{\Gamma,A \vdash C}{\Gamma,!A\vdash C}(der) \qquad \frac{\Gamma,!A,!A\vdash C}{\Gamma,!A\vdash C}(ctr) \qquad \frac{\Gamma\vdash C}{\Gamma,!A\vdash C}(wk)$$

Soft linear logic is obtained by observing that these rules are equivalent to soft promotion, multiplexing, and digging:

$$\frac{\Gamma\vdash A}{!\Gamma\vdash !A}(sp) \qquad \frac{\Gamma,\overbrace{A,\dots,A}^n\vdash C}{\Gamma,!A\vdash C}(mpx) \qquad \frac{\Gamma,!!A\vdash C}{\Gamma,!A\vdash C}(dig)$$

and then removing digging.  Thus, the only rules governing $!$ in soft linear logic are soft promotion and multiplexing.

## Categorical semantics

Inspecting the rules for the soft $!$, we see that soft promotion says that $!$ is a [[lax monoidal functor]] (or equivalently a functor between [[multicategories]]), while multiplexing says that we have a (presumably natural) transformation $!A \to A^{\otimes n}$ for all $n$.  On a non-[[thin category]] one would presumably ask for some coherence axioms on these transformations.

Intriguingly, however, the naive formula for a "cofree comonoid" on an object $A$ in a symmetric monoidal category with countable products:

$$ !A = \prod_{n\in\mathbb{N}} A^{\otimes n},$$

though it does not in general define a comonoid at all, *is* a lax monoidal functor with transformations $!A \to A^{\otimes n}$.  The latter are just the product projections, while the lax monoidal structure $!A \otimes !B \to !(A\otimes B) = \prod_n (A\otimes B)^{\otimes n}$ has components

$$ !A \otimes !B = \left(\prod_n A^{\otimes n}\right)\otimes \left(\prod_n B^{\otimes n}\right) \to A^{\otimes n} \otimes B^{\otimes n} \xrightarrow{\cong} (A\otimes B)^{\otimes n}. $$

In particular, therefore, any symmetric monoidal poset with countable meets admits a modality of this form satisfying the rules of the soft exponential.  For a non-thin category, one could take a further limit in an attempt to impose whatever axioms are desired of the structure on $!$.  For instance, if instead of $A^{\otimes n}$ we use an appropriate [[equalizer]], we could force permutation-invariance of the transformations $!A \to A^{\otimes n}$.

## Related pages

* [[computational complexity]]
  * [[implicit computational complexity]]
  * [[polynomial time]]
* [[light linear logic]]
* [[naive set theory]]
* [[ultrafinitism]]

## References

* Yves Lafont, Soft linear logic and polynomial time, Theoretical Computer Science, Volume 318, Issues 1–2, 2004, Pages 163-180, [doi](https://doi.org/10.1016/j.tcs.2003.10.018), [ps](http://iml.univ-mrs.fr/~lafont/pub/soft.ps)

* Marco Gaboardi, Jean-Yves Marion, Simona Ronchi Della Rocca, Soft Linear Logic and Polynomial Complexity Classes, Electronic Notes in Theoretical Computer Science, Volume 205, 2008, Pages 67-87, [doi](https://doi.org/10.1016/j.entcs.2008.03.066)

* Richard McKinley, Soft Linear Set Theory, The Journal of Logic and Algebraic Programming, Volume 76, Issue 2, 2008, [doi](https://doi.org/10.1016/j.jlap.2008.02.010)


[[!redirects soft exponential]]
[[!redirects soft promotion]]
[[!redirects multiplexing]]
