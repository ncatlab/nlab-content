

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **neural network** is a class of [[functions]] used in both [[supervised learning | supervised]] and [[unsupervised learning | unsupervised]] [[machine learning]] to approximate a correspondence between samples in a dataset and their associated labels. 


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

## Large network theory
For simplicity, consider a fully connected network with one layer. In terms of the notation above, consider $K\subset \mathbb{R}$ and $m=1$, also for simplicity. Denote the collection of weights ($W$'s and $b$'s) by $\theta$. Any fixed $\theta$ fixes some function $f_\theta\colon K\to \mathbb{R}$. Now instead of fixing one $\theta$, place some probability distribution over each of its components - for example, we may consider narrow probability Gaussians sitting over each weight. This in turn introduces a probability distribution over the function space ${\mathbb{R}}^{\mathbb{R}}$. For large layer width, by the **universal approximation theorem**, one can represent any $f\colon{\mathbb{R}}\to{\mathbb{R}}$ well (i.e. up to smaller and smaller numerical error), meaning such the resulting distribution may assign non-zero value to any such function. Indeed, as established in the mid 90's, considering a sequence of networks with a wider and wider hidden layer, and placing more and more sharp Gaussians over their weights, by the [[central limit theorem]] CLT, results in a probability distribution over ${\mathbb{R}}^{\mathbb{R}}$ that typically is a Gaussian process GP. These GP's are called **neural network Gaussian processes**, NNGP. (Roughly $P[f]=e^{-S[f]}$ with $S[f] = \int \rho_f$ where $\rho_f \propto f(x)f(y) dx dy$.)

### Neural Network Field Theory
Non-Gaussian non-zero cumulant effects emerge from either not taking the infinite width limit, or alternatively also from violating CLT's assumptions. The latter can practically be done by making the random sampling of certain parameters (certain $\theta$-components) depending on already sampled parameters.

Correlation functions (w.r.t. input $x$ and outputs $y$) are empirically accessible. Lately, researches have defined networks that in this way in the limit represent quantum fields, **Neural Network Field Theories**.
We may speak of neural network quantum field, e.g., when the correlation functions fulfills the [[Osterwalder-Schrader theorem | Osterwalder-Schrader axioms]].
Here, non-Gaussian effects can be expanded as non-quadratic contributions, corresponding to field interactions. (But note that with the finite-width approach, the universal approximation property will generally also break.)
From such non-trivial correlations, one may also attempt to reconstruct the corresponding field density (and thus the actions $S$.)
J. Halverson et al. specify the necessary architecture & distributions over $\theta$ to sample from the quartic actions ($\phi^4$-theory.)
Conversely, Feynman diagram tools have been used to study the expected properties of a random-initialized network.

## Learning theory
A neural network architecture specifies parameters and one then learns a prescription $f_\theta$ on how to get close to many given target positions $y_x$, given their index $x$. In the gradient descent approach, one incrementally alters the weights ($\theta_i \mapsto \theta_{i+1}$) so as to minimize a loss function $C$, which expresses how far the prescription is from $y_x$, for all the indices at once. This process thus corresponds to a trajectory of functions from network initialization till sufficient convergence ($f_{\theta_i} \mapsto f_{\theta_{i+1}}$).
In practical neural network training, improved gradient methods are employed (e.g. stochastic and batching considerations).

Improving the amount of computational shortcuts taken in implementing $\nabla_\theta$ is what *pytorch* and *tensorflow* is largely about. There is a neural tangent library on the google github.
Notable, also from google, there are some recent improvements related to baking the statistics of the collection of data ($z$) into the learning process (self-attention, transformers). 

### Neural tangent kernel theory
As is common in stochastic control, one may look at the step sizes in a very fine limit, i.e. pass to calculus proper. The algorithm is then expressed as the vector equation $\theta'(t) = -\nabla_\theta\Phi$ with $\Phi = \sum_z C(f_{\theta(t)}(z), y_z)$, where $z$ ranges over the available learning data. The mathematical derivations end up having a similar flavor as the study of the motion of a particle. Here the evolution of all components of $\theta$ are governed by a gradient of a potential that depends on $\theta$ through the costs of some property, $f_\theta$. This differential equation in turn implies a formally simple formula for $\partial_t f_\theta$, which really is the network output's evolution. The main ingredient determining $\partial_t f_\theta$ is $\Theta_\theta(x,z) = \nabla_\theta f(x)\cdot \nabla_\theta f(z)$. This quantity $\Theta_\theta$ quantifies a similarity reminiscent of [[kernel method]]s. It is small when the changes of $f_\theta$ (w.r.t. a change of $\theta$) are different on $x$ resp. $y$.
In the limit of infinite width (and small step size limit and everything in distribution), the resulting mathematical network has so many degrees of freedom that (roughly speaking) learning becomes very effective.
The learning theory in the limit goes under **neural tangent kernel theory** (NTK theory). Formal relations between different learning approaches (neural networks and kernel machines in particular) become simpler here. Depending on the loss function, the structure may remain Gaussian throughout the learning.
For a shallow network of finite size, $\Theta_\theta$ may still give a quantitative idea on how that (finite) network will change upon tuning of its parameters. Some work was done to try to establish where NKT results start to significantly fail for practical networks. Note: Infinite networks (where weights barely need to be tuned to learn) also don't encode abstracted features.

## Relation to differential equations and dynamical systems

A relation between deep neural networks, [[differential equations]], and [[dynamical systems]] was proposed in ([CMHRBH17](#CMHRBH17), [LZLD17](#LZLD17), [Weinan17](#Weinan17))

Victor Lopez-Pastor and Florian Marquardt proposed that certain [[time-reversible]] [[Hamiltonian systems]] exhibit self-learning behaviour and a physical version of the [[backpropagation]] [[algorithm]]. 

## Relation to renormalization group flow
 {#RelationToRenormalizationGroupFlow}

A relation between deep neural networks (DNNs) based on Restricted Boltzmann
Machines (RBMs) and [[renormalization group flow]] in [[physics]] was proposed in ([MS14](#MS14)).

## Related concepts

* [[function machine]]

* [[tensor network]]

* [[string diagram]]

* [[physical neural network]]

* [[spiking neural network]]

## References

### General

Textbook account:

* Daniel A. Roberts, Sho Yaida, Boris Hanin, *The Principles of Deep Learning Theory*, Cambridge University Press 2022 ([arXiv:2106.10165](https://arxiv.org/abs/2106.10165))

Lecture notes:

* Yasaman Bahri, Boris Hanin, Antonin Brossollet, Vittorio Erba, Christian Keup, Rosalba Pacelli, James B. Simon, *Les Houches Lectures on Deep Learning at Large & Infinite Width* &lbrack;[arXiv:2309.01592](https://arxiv.org/abs/2309.01592)&rbrack;


On the learning algorithm as related to [[differential equations]] and [[dynamical systems]]:

* {#CMHRBH17} Bo Chang, Lili Meng, Eldad Haber, Lars Ruthotto, David Begert, Elliot Holtham, *Reversible Architectures for Arbitrarily Deep Residual Neural Networks*, ([arXiv:1709.03698](https://arxiv.org/abs/1709.03698))

* {#LZLD17} Yiping Lu, Aoxiao Zhong, Quanzheng Li, Bin Dong, *Beyond Finite Layer Neural Networks: Bridging Deep Architectures and Numerical Differential Equations*, ([arXiv:1710.10121](https://arxiv.org/abs/1710.10121)). 

* {#Weinan17} Weinan E, *A Proposal on Machine Learning via Dynamical Systems*, Communications in Mathematics and Statistics, 5, 1–11 (2017). ([doi:10.1007/s40304-017-0103-z](https://doi.org/10.1007/s40304-017-0103-z))

* Victor Lopez-Pastor, Florian Marquardt, *Self-learning Machines based on Hamiltonian Echo Backpropagation*, ([arXiv:2103.04992](https://arxiv.org/abs/2103.04992))

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

* G.S.H. Cruttwell, [[Bruno Gavranović]], [[Neil Ghani]], [[Paul Wilson]], [[Fabio Zanasi]], _Categorical Foundations of Gradient-Based Learning_, ([arXiv:2103.01931](https://arxiv.org/abs/2103.01931))

* {#Cruttwell2024} [[G.S.H. Cruttwell]], [[Bruno Gavranović]], [[Neil Ghani]], [[Paul Wilson]], [[Fabio Zanasi]], _Deep Learning for Parametric Lenses_, ([arXiv:2404.00408](https://arxiv.org/abs/2404.00408))

* [[Bruno Gavranović]], Paul Lessard, Andrew Dudzik, Tamara von Glehn, João G. M. Araújo, Petar Veličković, _Categorical Deep Learning: An Algebraic Theory of Architectures_ &lbrack;[arXiv:2402.15332](https://arxiv.org/abs/2402.15332)&rbrack;
 

Neural networks field theory:

* Mehmet Demirtas, James Halverson, Anindita Maiti, Matthew D. Schwartz, Keegan Stoner, *Neural Network Field Theories: Non-Gaussianity, Actions, and Locality*, (2023)  ([arXiv:2307.03223](https://arxiv.org/abs/2307.03223))

Quantum neural networks (in [[quantum computation]] for [[quantum machine learning]]):

* Iris Cong, Soonwon Choi & Mikhail D. Lukin, *Quantum convolutional neural networks*, Nature Physics volume 15, pages 1273–1278 (2019)  ([doi:10.1038/s41567-019-0648-8](https://doi.org/10.1038/s41567-019-0648-8))

* {#MariBromleyIzaacSchuldKilloran20} Andrea Mari, Thomas R. Bromley, Josh Izaac, Maria Schuld, Nathan Killoran,  *Transfer learning in hybrid classical-quantum neural networks*, Quantum 4, 340 (2020) ([arXiv:1912.08278](https://arxiv.org/abs/1912.08278))

* Stefano Mangini, Francesco Tacchino, Dario Gerace, Daniele Bajoni, Chiara Macchiavello, *Quantum computing models for artificial neural networks*, EPL (Europhysics Letters) 134(1), 10002 (2021) ([arXiv:2102.03879](https://arxiv.org/abs/2102.03879))

Topological deep learning for data supported on topological domains such as [[simplicial complexes]], [[cell complexes]], and [[hypergraphs]]:

* Ephy R. Love, Benjamin Filippenko, Vasileios Maroulas, Gunnar Carlsson, _Topological Deep Learning_ ([arXiv:2101.05778](https://arxiv.org/abs/2101.05778))

* Mathilde Papillon, Sophia Sanborn, Mustafa Hajij, Nina Miolane, _Architectures of Topological Deep Learning: A Survey on Topological Neural Networks_ ([arXiv:2304.10031](https://arxiv.org/abs/2304.10031))

* Mustafa Hajij et al., _Topological Deep Learning: Going Beyond Graph Data_ ([pdf](https://www.researchgate.net/publication/370134352_Topological_Deep_Learning_Going_Beyond_Graph_Data))

* Theodore Papamarkou, Tolga Birdal, Michael Bronstein, Gunnar Carlsson, Justin Curry, Yue Gao, Mustafa Hajij, Roland Kwitt, Pietro Liò, Paolo Di Lorenzo, Vasileios Maroulas, Nina Miolane, Farzana Nasrin, Karthikeyan Natesan Ramamurthy, Bastian Rieck, Simone Scardapane, Michael T. Schaub, Petar Veličković, Bei Wang, Yusu Wang, Guo-Wei Wei, Ghada Zamzmi, _Position Paper: Challenges and Opportunities in Topological Deep Learning_ &lbrack;[arXiv:2402.08871](https://arxiv.org/abs/2402.08871)&rbrack;


### Relation to tensor networks

Application of [[tensor networks]] and specifically [[tree tensor networks]]:

* Ding Liu, Shi-Ju Ran, Peter Wittek, Cheng Peng, Raul Blázquez García, Gang Su, Maciej Lewenstein, _Machine Learning by Unitary Tensor Network of Hierarchical Tree Structure_, New Journal of Physics, 21, 073059 (2019) ([arXiv:1710.04833](https://arxiv.org/abs/1710.04833))

* Song Cheng, Lei Wang, Tao Xiang, Pan Zhang, _Tree Tensor Networks for Generative Modeling_, Phys. Rev. B 99, 155131 (2019) ([arXiv:1901.02217](https://arxiv.org/abs/1901.02217))


### Relation to renormalization group flow
 {#ReferencesRelationToRenormalizationGroupFlow}

Relation of deep learning to [[renormalization group flow]]:

* {#MS14} Pankaj Mehta, David J. Schwab - _An exact mapping between the Variational Renormalization Group and Deep Learning_, 2014 ([arXiv:1410.3831](https://arxiv.org/abs/1410.3831))

Further discussion under the relation of [[renormalization group flow]] to [[bulk]]-flow in the context of the [[AdS/CFT correspondence]]:

* Yi-Zhuang You, Zhao Yang, Xiao-Liang Qi, _Machine Learning Spatial Geometry from Entanglement Features_, Phys. Rev. B 97, 045153 (2018) ([arxiv:1709.01223](https://arxiv.org/abs/1709.01223))

* W. C. Gan and F. W. Shu, _Holography as deep learning_,  Int. J. Mod. Phys. D 26, no. 12, 1743020 (2017) ([arXiv:1705.05750](https://arxiv.org/abs/1705.05750))

* J. W. Lee, _Quantum fields as deep learning_ ([arXiv:1708.07408](https://arxiv.org/abs/1708.07408))

* [[Koji Hashimoto]], Sotaro Sugishita, Akinori Tanaka, Akio Tomiya, _Deep Learning and AdS/CFT_,  Phys. Rev. D 98, 046019 (2018) ([arxiv:1802.08313](https://arxiv.org/abs/1802.08313))

See also:

* Christian Ferko, [[James Halverson]]: *Quantum Mechanics and Neural Networks* &lbrack;[arXiv:2504.05462](https://arxiv.org/abs/2504.05462)&rbrack;



[[!redirects neural networks]]


[[!redirects deep learning]]

[[!redirects quantum neural network]]
[[!redirects quantum neural networks]]

[[!redirects deep neural network]]
[[!redirects deep neural networks]]


