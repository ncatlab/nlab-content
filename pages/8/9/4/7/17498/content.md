# Eventual image

* table of contents
{:toc}

## Definition

The **eventual image** of an [[endomorphism]] $f:A\to A$ is the [[intersection]] $\bigcap_{n=0}^{\infty} f^{(n)}(A)$ of the images of its [[iteration|iterates]].  This makes sense in many different [[categories]].

## Properties

On the category of [[finite sets]], the operation assigning to each endomorphism its eventual image is a [[dinatural transformation]]. 

This example can also be viewed in terms of the [[trace of a category|trace]] of [[FinSet]], defined as $\int^{a: FinSet}\; \hom(a, a)$. Indeed, the value of $f \in \hom(a, a)$ under the canonical map $\hom(a, a) \to \int^a \; \hom(a, a)$ is the same as that of the restriction $f|: Evim(f) \to Evim(f)$ to its eventual image, which is a permutation, and the value may be regarded as the [[conjugacy class]] of that permutation. 

## References

* [[Tom Leinster]], [The eventual image](https://golem.ph.utexas.edu/category/2011/12/the_eventual_image.html) (blog post)

* [[Tom Leinster]], [The eventual image, part 2](https://golem.ph.utexas.edu/category/2011/12/the_eventual_image_part_2.html) (blog post)

[[!redirects eventual images]]
