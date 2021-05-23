
#Contents#
* table of contents
{:toc}

## Idea

A **neural network** is a class of functions used in both [[supervised learning | supervised]] and [[unsupervised learning | unsupervised]] [[machine learning]] to approximate a correspondence between samples in a dataset and their associated labels. 

## Definition
 {#Definition}

+-- {: .num_defn}
###### Definition

Where $K\subset \mathbb{R}^d$ is compact, $\{T_L\}_{L\leq N \in \mathbb{N}}$ a finite set of affine maps such that $T_L(x) = \langle W_L,x\rangle + b_L$ where $W_L$ is the $L^{th}$ layer weight matrix and $b_L$ the $L^{th}$ layer bias, $g:\mathbb{R}\to\mathbb{R}$ a non-linear activation function, a neural network  is a function $f:K\subset \mathbb{R}^d \to \mathbb{R}^m$, such that on input $x$, computes the composition:

$$f(x) = (T_L\circ g \circ T_{L-1}\circ g \circ \dots \circ T_1)(x)$$

where $g$ is applied component-wise. 

=--

Typically, $T_1$ is called the input layer, $T_L$ the output layer, and layers $T_2$ to $T_{L-1}$ are hidden layers. In particular, a real-valued 1-hidden layer neural network with computes:

$$f(x) = b' + \sum_{i=1}^n a_i g(\langle W_i, x\rangle + b)$$
where $a = (a_1, \dots, a_n)$ is the output weight, $b'$ the output bias, $W_i$ the $i^{th}$ row of the hidden weight matrix, and $b$ the hidden bias. Here, the hidden layer is $n$-dimensional.   


## Relation to renormalization group flow
 {#RelationToRenormalizationGroupFlow}

A relation between deep neural networks (DNNs) based on Restricted Boltzmann
Machines (RBMs) and [[renormalization group flow]] in [[physics]] was proposed in ([MS14](#MS14)).


## Related concepts

* [[function machine]]

* [[tensor network]]

* [[string diagram]]


## References

### General

On the learning algorithm as [[gradient descent]] of the loss functional:

* {#ThierryMieg18} Jean Thierry-Mieg, _Connections between physics, mathematics and deep learning_, Letters in High Energy Physics, vol 2 no 3 (2019) ([arXiv:1811.00576](https://arxiv.org/abs/1811.00576), [doi:10.31526/lhep.3.2019.110](https://doi.org/10.31526/lhep.3.2019.110))

On the learning algorithm as analogous to the [[AdS/CFT correspondence]]:

* Yi-Zhuang You, Zhao Yang, Xiao-Liang Qi, _Machine Learning Spatial Geometry from Entanglement Features_, Phys. Rev. B 97, 045153 (2018) ([arxiv:1709.01223](https://arxiv.org/abs/1709.01223))

* W. C. Gan and F. W. Shu, _Holography as deep learning_,  Int. J. Mod. Phys. D 26, no. 12, 1743020 (2017) ([arXiv:1705.05750](https://arxiv.org/abs/1705.05750))

* J. W. Lee, _Quantum fields as deep learning_ ([arXiv:1708.07408](https://arxiv.org/abs/1708.07408))

* {#HSTT18} [[Koji Hashimoto]], Sotaro Sugishita, Akinori Tanaka, Akio Tomiya, _Deep Learning and AdS/CFT_,  Phys. Rev. D 98, 046019 (2018) ([arxiv:1802.08313](https://arxiv.org/abs/1802.08313))

[[category theory|Category theoretic]] treatments of deep learning in neural networks:

* [[Brendan Fong]], [[David Spivak]], Rémy Tuyéras, _Backprop as Functor: A compositional perspective on supervised learning_, ([arXiv:1711.10455](https://arxiv.org/abs/1711.10455))

* [[David Spivak]], _Learners' languages_, ([arXiv:2103.01189](https://arxiv.org/abs/2103.01189))

\bibitem{Spivak202103}

* G.S.H. Cruttwell, Bruno Gavranović, [[Neil Ghani]], Paul Wilson, Fabio Zanasi, _Categorical Foundations of Gradient-Based Learning_, ([arXiv:2103.01931](https://arxiv.org/abs/2103.01931))

Quantum neural networks (in [[quantum computation]] for [[quantum machine learning]]):

* Iris Cong, Soonwon Choi & Mikhail D. Lukin, *Quantum convolutional neural networks*, Nature Physics volume 15, pages 1273–1278 (2019)  ([doi:10.1038/s41567-019-0648-8](https://doi.org/10.1038/s41567-019-0648-8))



### Relation to tensor networks

Application of [[tensor networks]] and specifically [[tree tensor networks]]:

* Ding Liu, Shi-Ju Ran, Peter Wittek, Cheng Peng, Raul Blázquez García, Gang Su, Maciej Lewenstein, _Machine Learning by Unitary Tensor Network of Hierarchical Tree Structure_, New Journal of Physics, 21, 073059 (2019) ([arXiv:1710.04833](https://arxiv.org/abs/1710.04833))

* Song Cheng, Lei Wang, Tao Xiang, Pan Zhang, _Tree Tensor Networks for Generative Modeling_, Phys. Rev. B 99, 155131 (2019) ([arXiv:1901.02217](https://arxiv.org/abs/1901.02217))


### Relation to renormalization group flow
 {#ReferencesRelationToRenormalizationGroupFlow}

Relation to deep learning to [[renormalization group flow]]:

* {#MS14} Pankaj Mehta, David J. Schwab - _An exact mapping between the Variational Renormalization Group and Deep Learning_, 2014 ([arXiv:1410.3831](https://arxiv.org/abs/1410.3831))

Further discussion under the relation of [[renormalization group flow]] to [[bulk]]-flow in the context of the [[AdS/CFT correspondence]]:

* Yi-Zhuang You, Zhao Yang, Xiao-Liang Qi, _Machine Learning Spatial Geometry from Entanglement Features_, Phys. Rev. B 97, 045153 (2018) ([arxiv:1709.01223](https://arxiv.org/abs/1709.01223))

* W. C. Gan and F. W. Shu, _Holography as deep learning_,  Int. J. Mod. Phys. D 26, no. 12, 1743020 (2017) ([arXiv:1705.05750](https://arxiv.org/abs/1705.05750))

* J. W. Lee, _Quantum fields as deep learning_ ([arXiv:1708.07408](https://arxiv.org/abs/1708.07408))

* [[Koji Hashimoto]], Sotaro Sugishita, Akinori Tanaka, Akio Tomiya, _Deep Learning and AdS/CFT_,  Phys. Rev. D 98, 046019 (2018) ([arxiv:1802.08313](https://arxiv.org/abs/1802.08313))


[[!redirects neural networks]]


[[!redirects deep learning]]

[[!redirects quantum neural network]]
[[!redirects quantum neural networks]]

