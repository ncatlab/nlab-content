
#Contents#
* table of contents
{:toc}


## Idea

Let $E$ be a [[perfectoid field]] (for example $\mathbb{C}_{p}$). The *Fargues-Fontaine curve* $X_{E}$ is a [[complete variety|complete]] [[algebraic curve]] whose [[closed points]] parametrize the untilts of $E$. Such an untilt may be recovered as the [[residue field]] of the corresponding point.

## Construction

Let $E$ be a perfectoid field, let $\mathcal{O}_{E}$ be its [[ring of integers]], and let $W(\mathcal{O}_{E})$ be the [[Witt vectors]] of $\mathcal{O}_{E}$. Let $\phi:E\to E$ be the Frobenius morphism. We define a [[norm]] $\vert\cdot\vert_{r}$ on $W(\mathcal{O}_{E})[1/p]$ as follows:

$$\vert \sum_{n\gg -\infty} [a_{n}]p^{n}\vert_{r}=\sup_{n}\vert a_{n}\vert p^{-r n}$$

Let $B_{E}$ be the Frechet completion of $W(\mathcal{O}_{E})[1/p]$ with respect to all the norms $\vert\cdot\vert_{r}$ for every positive $r$.

Then the Fargues-Fontaine curve $X_{E}$ is defined to be
$$X_{E}=\mathrm{Proj}(\oplus_{n\in\mathbb{N}} B_{E}^{\phi=p^{n}}).$$

The Fargues-Fontaine curve may also be constructed as an [[adic space]].

## Related concepts

* [[p-adic Hodge theory]]

## References

* [[Jared Weinstein]], _[The Fundamental Curve of p-adic Hodge Theory, or How to Un-tilt a Tilted Field](https://galoisrepresentations.wordpress.com/2013/07/23/the-fundamental-curve-of-p-adic-hodge-theory-or-how-to-un-tilt-a-tilted-field/)_

* [[Jared Weinstein]], _[The Fundamental Curve of p-adic Hodge Theory, Part II](https://galoisrepresentations.wordpress.com/2013/08/12/the-fundamental-curve-of-p-adic-hodge-theory-part-ii/)_

* [[Dennis Gaitsgory]], [[Jacob Lurie]], _Harvard Seminar on Fargues-Fontaine Curve_ ([Informal Notes](http://www.math.harvard.edu/~lurie/FF.html))

* a version in global analytic geometry is mentioned at the end of [http://www-personal.umich.edu/~snkitche/Conference/notes/Kremnitzer-2.pdf](http://www-personal.umich.edu/~snkitche/Conference/notes/Kremnitzer-2.pdf) + [audio](http://leccap.engin.umich.edu/leccap/site/s79yndxt7qowoek7n3m)

* [[Federico Bambozzi]], [[Oren Ben-Bassat]], [[Kobi Kremnizer]], _Analytic geometry over $\mathbb{F}_1$ and the Fargues-Fontaine curve_, ([arXiv:1711.04885](https://arxiv.org/abs/1711.04885))