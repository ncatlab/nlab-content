[[!redirects coherence theorem for bicategories with finite limits]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


## Theorem

+--{: .un_theorem}
###### Theorem
**(Power)**
Any [[bicategory]] with finite [[2-limit|bilimits]] is [[equivalence of bicategories|equivalent]] to a [[strict 2-category]] with finite [[flexible limits]].
=--
+--{: .proof}
###### Proof
Let $K$ be a bicategory with finite bilimits, let $K \hookrightarrow [K^{op},Cat]$ be its [[Yoneda embedding for bicategories|Yoneda embedding]], and let $K'$ be the closure of $K$ in $[K^{op},Cat]$ under finite flexible limits.  Since $Cat$ is a strict 2-category with finite flexible limits, so is $[K^{op},Cat]$.  And since $K$ has finite bilimits, and these are preserved by its Yoneda embedding, while flexible limits are in particular bilimits, every object of $K'$ is equivalent to an object of $K$.  Thus, $K\simeq K'$.
=--

Furthermore, the 2-category of finite bilimit-preserving [[pseudofunctors]] into $Cat$ is equivalent to the 2-category of finite [[PIE limit]]-preserving 2-functors into $Cat$ and pseudonatural transformations.

## References

* [[John Power]], _Coherence for bicategories with finite bilimits I_, *Categories in computer science and logic*, Contemporary Mathematics **92** (1989) pp 341-347  [MR1003207](http://www.ams.org/mathscinet-getitem?mr=1003207), doi:[10.1090/conm/092](https://dx.doi.org/10.1090/conm/092), ([Google Books](https://books.google.com.au/books?id=VxAcCAAAQBAJ&lpg=PA345&ots=P8rWN00524&dq=%E2%80%9CCoherence%20for%20bicategories%20with%20finite%20bilimits%E2%80%9D&pg=PA343#v=onepage&q=%E2%80%9CCoherence%20for%20bicategories%20with%20finite%20bilimits%E2%80%9D&f=false))

* [[John Power]], _Why tricategories?_, Information and Computation 120.2 (1995): 251-262.

* [[John Power]], _Three dimensional monad theory_, Contemporary Mathematics 431 (2007): 405.

[[!redirects coherence theorem for bicategories with finite 2-limits]]
[[!redirects coherence theorem for bicategories with finite bilimits]]
[[!redirects coherence theorem for bicategories with finite limits]]
[[!redirects coherence for bicategories with finite 2-limits]]
[[!redirects coherence for bicategories with finite bilimits]]
[[!redirects coherence for bicategories with finite limits]]
[[!redirects coherence theorem for 2-categories with finite 2-limits]]
[[!redirects coherence theorem for 2-categories with finite bilimits]]
[[!redirects coherence theorem for 2-categories with finite limits]]
[[!redirects coherence for 2-categories with finite 2-limits]]
[[!redirects coherence for 2-categories with finite bilimits]]
[[!redirects coherence for 2-categories with finite limits]]
