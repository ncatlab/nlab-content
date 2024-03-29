
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

$\ell$-Adic cohomology is a [[cohomology theory]] on suitable [[varieties]] which is constructed as an [[inverse limit]] of [[étale cohomology]] over different [[coefficients]].

$\ell$-Adic cohomology is a [[Weil cohomology theory]]. It is endowed with a Galois action and therefore gives us a way of obtaining [[Galois modules]] from [[algebraic varieties]].

## Definition

### Over the &#233;tale site
 {#OverEtaleSite}

Let $X$ be a (smooth?) [[proper map|proper]] [[variety]] over a field. Fix $\ell$ a [[prime number]] different from the [[characteristic]] of $k$. The $\ell$-adic cohomology is defined to be the [[cohomology theory]] on the [[étale site]] given by the [[inverse limit]] over $n \in \mathbb{N}$

$$
  H^j_{et}(X_{\overline{k}}, \mathbb{Q}_\ell)
  \coloneqq
 \lim_n 
  H^j_{et}(X_{\overline{k}}, \mathbb{Z}/\ell^n\mathbb{Z})\otimes_{\mathbb{Z}_{\ell}} \mathbb{Q}_\ell
$$

of [[étale cohomology]] with [[coefficients]] in $\mathbb{Z}/\ell^n\mathbb{Z}$.

The key insights into getting finite dimensionality with coefficients in a [[field]] of [[characteristic]] $0$ when $k$ has positive characteristic is to first base change to $\overline{k}$ to make the theory "geometric." Then only work with torsion sheaves so that appropriate finiteness theorems for [[étale cohomology]] of proper varieties can be used, and then pass to the limit.

Notice that on the left $\mathbb{Q}_{\ell}$ is not an actual sheaf whose actual [[sheaf cohomology]] is being computed instead the expression on the left is defined by the genuine sheaf cohomology groups on the right.

### Over the pro-&#233;tale site


This is rectified by passing to [[pro-étale cohomology]]. Here $\mathbb{Q}_{\ell}$ exists as an actual sheaf and its genuine [[abelian sheaf cohomology]] is $\ell$-adic cohomology.
([Bhatt-Scholze 13, section 6.8](#BhattScholze13))


## Related concepts

* [[Weil cohomology]]

  * [[étale cohomology]], [[basics of étale cohomology]]

  * [[pro-étale cohomology]]

* [[p-adic integers]]

* [[p-adic geometry]]

* [[p-adic homotopy]]

* [[p-adic cohomology]]

* [[p-adic physics]]

## References

A textbook account is in

* [[James Milne]], section 19 of _[[Lectures on Étale Cohomology]]_ ([web] (http://www.jmilne.org/math/CourseNotes/lec.html))

Surveys include

* [[Akhil Mathew]], _$l$-adic cohomology and exponential sums_ ([web](http://amathew.wordpress.com/tag/l-adic-cohomology/))


A variant of the [[étale site]], well adapted to the needs of $\ell$-adic cohomology, the _[[pro-étale site]]_ (locally contractible in some sense) is discussed in 

* Bhargav Bhatt, [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ ([arXiv:1309.1198](http://arxiv.org/abs/1309.1198))
 {#BhattScholze13}


[[!redirects l-adic cohomology]]