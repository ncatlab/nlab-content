
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of [[machine learning]], a *kernel method* is effectively the analysis of a data set $D$ through a choice of a [[distance]]/[[metric]]-function $d \;\colon\; D \times D \to \mathbb{R}$ on it. The corresponding [[integral kernels]] $\exp(- \lambda \cdot d(-,-))$ turn out to contain useful information, if chosen correctly.

As a special case, if the data set $D$ is a "choice of rankings", hence the [[set]] of [[permutations]], of $n \in \mathbb{N}$ elements, distance functions come from the [[graph distance]] of [[Cayley graphs]] of the [[symmetric group]], such as the [[Kendall distance]] (or [[Cayley distance]]) with associated kernels such as the [[Mallows kernel]]. With these choices, the kernel method overlaps with [[geometric group theory]].

## Details

A kernel on a set $X$ is a function $K: X \times X \to \mathbb{R}$ (although complex-valued kernels are also used) which is symmetric and positive definite, in the sense that for any $N \geq 1$ and any $x_1,..., x_N \in X$, the matrix $K_{i j} = K(x_i, x_j)$ is positive definite, i.e., $\sum_{i, j} c_i c_j K_{i j} \geq 0$ for all $c_1, ..., c_N \in \mathbb{R}$.  

This may be reformulated as a mapping $\phi : X \to H$, where $H$ is a *[[reproducing kernel Hilbert space]]*, a function space in which pointwise evaluation is a continuous linear functional.

The 'kernel' and 'feature map to Hilbert space' stories relate to each other as follows:

$$K(x, .) = \phi (x).$$

The 'reproducing' aspect of $H$ means that

$$\langle f(.), K(x, .) \rangle = f(x),$$

and this is continuous. So we have

$$K(x, y) = \langle \phi (x), \phi(y) \rangle.$$

$H$ is the span of the set of functions $\{K(x, .)| x \in X\}$, and, under certain conditions, when we find the $f \in H$ for which a functional is minimised, it takes the form  

$$f(x) = \sum_{i = 1}^m c_i K(x_i, x).$$

Many linear algebra techniques in $H$ just involve the inner product, and so can be conducted as a form of nonlinear algebra back in $X$, using the 'kernel trick'.

Kernels characterise the similarity of the input set. But how do they get chosen? Often a Gaussian radial-basis function (RBF) kernel is selected:

$$K(x, y) = e^{-\|x - y\|^2 / \sigma^2}.$$

Note that there's a [[Bayesianism|Bayesian]] version of kernel methods which uses Gaussian processes.

## Example

Consider binary classification where we look to form a classifier which accurately finds the labels in $\{\pm 1\}$ of a sample from a distribution over $X \times \{\pm 1\}$ on the basis of their $X$ values, given a set of labelled training data. The support vector machine approach to this task looks to find the hyperplane in the associated Hilbert space, $H$, which best separates the images of data points $\phi (x_i)$, so that those with the same label $(y_i)$ fall in the same half space. The control for overfitting comes from finding such a hyperplane that classifies the training data accurately with the largest perpendicular distance to the nearest of them (the support vectors).  


## Related concepts

* [[machine learning]]

* [[geometric group theory]]

* [[reproducing kernel Hilbert space]]

* [[Mallows kernel]], [[Kendall kernel]]

  [[Cayley distance kernel]]

* [[thermodynamics]]


## References

### General

Survey and introduction:

* Thomas Hofmann, [[Bernhard Schölkopf]], Alexander J. Smola, *Kernel methods in machine learning*, Annals of Statistics 2008, Vol. 36, No. 3, 1171-1220 ([arXiv:math/0701907](https://arxiv.org/abs/math/0701907))

* [[Julien Mairal]], [[Jean-Philippe Vert]], *Machine Learning with Kernel Methods*, lecture notes 2017 ([webpage](http://members.cbio.mines-paristech.fr/~jvert/svn/kernelcourse/course/2021mva/index.html), [pdf](http://members.cbio.mines-paristech.fr/~jvert/svn/kernelcourse/slides/master2017/master2017.pdf), [[MairalVertKernelMethods.pdf:file]])

See also:

* Wikipedia, *[Kernel method](https://en.wikipedia.org/wiki/Kernel_method)* 

On positive definiteness via [[Fourier transform]]/[[Bochner's theorem]]:

* [[Kenji Fukumizu]], [[Bharath Sriperumbudur]], [[Arthur Gretton]], [[Bernhard Schölkopf]], *Characteristic Kernels on Groups and Semigroups*, Advances in Neural Information Processing Systems 21 : 22nd Annual Conference on Neural Information Processing Systems 2008 ([NIPS 2008](https://neurips.cc/Conferences/2008/)), 473-480 ([mpg:5466](http://www.is.mpg.de/publications/5466), [pdf](http://www.gatsby.ucl.ac.uk/~gretton/papers/FukSriGreSch09.pdf))

* [[Kenji Fukumizu]], *Theory of Positive Definite Kernel and Reproducing Kernel Hilbert Space* 2008 ([pdf](https://www.ism.ac.jp/~fukumizu/H20_kernel/Kernel_7_theory.pdf), [[FukumizuPositiveDefiniteKernels.pdf:file]])

Proof that the [[Mallows kernel]] and [[Kendall kernel]] are [[positive definite bilinear form|positive definite]]:

* [[Yunlong Jiao]], [[Jean-Philippe Vert]], *The Kendall and Mallows Kernels for Permutations*, IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 40, no. 7, pp. 1755-1769, 1 July 2018 ([doi:10.1109/TPAMI.2017.2719680](https://doi.org/10.1109/TPAMI.2017.2719680), [hal:01279273](https://hal.archives-ouvertes.fr/hal-01279273/document))

Discussion of weighted variants:

* [[Yunlong Jiao]], [[Jean-Philippe Vert]], *The Weighted Kendall and High-order Kernels for Permutations*, Proceedings of the 35th International Conference on Machine Learning, PMLR 80:2314-2322, 2018 ([arXiv:1802.08526](https://arxiv.org/abs/1802.08526), [mlr:v80/jiao18a](http://proceedings.mlr.press/v80/jiao18a.html), [hal:hal-01717385](https://hal.inria.fr/hal-01717385))


### In topological machine learning
 {#InTopologicalMachineLearningReferences}

On kernel methods applicable to [[persistence diagrams]]/[[barcodes]] for making [[topological data analysis]] amenable to "[[topological machine learning|topological]]" [[machine learning]]:

* {#RHBK15} Jan Reininghaus, [[Stefan Huber]], Ulrich Bauer, Roland Kwitt, *A Stable Multi-Scale Kernel for Topological Machine Learning*, NIPS'15: Proceedings of the 28th International Conference on Neural Information Processing System, **2** (2015 3070–3078  $[$[arXiv:1412.6821](https://arxiv.org/abs/1412.6821)$]$

* {#KHNL15} Roland Kwitt, [[Stefan Huber]], Marc Niethammer, Weili Lin, [[Ulrich Bauer]], *Statistical Topological Data Analysis -- A Kernel Perspective*, in: *Advances in Neural Information Processing Systems*  (NIPS 2015) $[$[ISBN:9781510825024](https://proceedings.neurips.cc/paper/2015), [doi:10.5555/2969442.2969582](https://dl.acm.org/doi/10.5555/2969442.2969582)$]$


* {#RSL} [[Bastian Rieck]], Filip Sadlo, Heike Leitte, *Topological Machine Learning with Persistence Indicator Functions*,  In: *Topological Methods in Data Analysis and Visualization V* TopoInVis (2017) 87-101 Mathematics and Visualization. Springer, $[$[arXiv:1907.13496](https://arxiv.org/abs/1907.13496), [doi:10.1007/978-3-030-43036-8_6](https://doi.org/10.1007/978-3-030-43036-8_6)$]$

* Raphael Reinauer, Matteo Caorsi, Nicolas Berkouk, *Persformer: A Transformer Architecture for Topological Machine Learning* $[$[arXiv:2112.15210](https://arxiv.org/abs/2112.15210)$]$




[[!redirects kernel methods]]

