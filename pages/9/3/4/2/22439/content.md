
#Contents#
* table of contents
{:toc}

## Idea

In the context of [[machine learning]], a *kernel method* is effectively the analysis of a data set $D$ through a choice of a [[distance]]/[[metric]]-function $d \;\colon\; D \times D \to \mathbb{R}$ on it. The corresponding [[integral kernels]] $\exp(- \lambda \cdot d(-,-))$ turn out to contain useful information, if chosen correctly.

As a special case, if the data set $D$ is a "choice of rankings", hence the [[set]] of [[permutations]], of $n \in \mathbb{N}$ elements, distance functions come from the [[graph distance]] of [[Cayley graphs]] of the [[symmetric group]], such as the [[Kendall distance]] (or [[Cayley distance]]) with associated kernels such as the [[Mallows kernel]]. With these choices, the kernel method overlaps with [[geometric group theory]].


## Related concepts

* [[machine learning]]

* [[geometric group theory]]

* [[Mallows kernel]], [[Kendall kernel]]


## References

Lecture notes:

* [[Julien Mairal]], [[Jean-Philippe Vert]], *Machine Learning with Kernel Methods*, 2017 ([pdf](http://members.cbio.mines-paristech.fr/~jvert/svn/kernelcourse/slides/master2017/master2017.pdf), [[MarailVertKernelMethods.pdf:file]])

See also:

* Wikipedia, *[Kernel method](https://en.wikipedia.org/wiki/Kernel_method)* 

Proof that the [[Mallows kernel]] and [[Kendall kernel]] are [[positive definite bilinear form|positive definite]]:

* [[Yunlong Jiao]], [[Jean-Philippe Vert]], *The Kendall and Mallows Kernels for Permutations*, IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 40, no. 7, pp. 1755-1769, 1 July 2018 ([doi:10.1109/TPAMI.2017.2719680](https://doi.org/10.1109/TPAMI.2017.2719680), [hal:01279273](https://hal.archives-ouvertes.fr/hal-01279273/document))

Discussion of weighted variants:

* [[Yunlong Jiao]], [[Jean-Philippe Vert]], *The Weighted Kendall and High-order Kernels for Permutations*, Proceedings of the 35th International Conference on Machine Learning, PMLR 80:2314-2322, 2018 ([arXiv:1802.08526](https://arxiv.org/abs/1802.08526), [mlr:v80/jiao18a](http://proceedings.mlr.press/v80/jiao18a.html), [hal:hal-01717385](https://hal.inria.fr/hal-01717385))


[[!redirects kernel methods]]

