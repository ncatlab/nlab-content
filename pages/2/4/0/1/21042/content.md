#Contents#
* table of contents
{:toc}

## Idea

A **function machine** is a generalization of [[neural networks]] to potentially infinite dimensional layers, motivated by the study of universal approximation of [[operators]] and [[functionals]] over abstract [[Banach spaces]]. 

## Definition
 {#Definition}
A function machine's layers is defined by the type of layers it is composed with. 
+-- {: .num_defn}
###### Definition
Let $K \subset \mathbb{R}^d, K' \subset \mathbb{R}^{d'}$ both compact, $T$ is some affine map. 

* (Operator layer) When $T:\mathcal{L}^1(K, \mu)\to \mathcal{L}^1(K', \mu)$, $T = T^\mathfrak{o}$ is said to be an **operator layer** if there is some continuous family of measures $(W_t \ll \mu)$ indexed by $t \in K'$ and a function $b \in \mathcal{L}^1(K, \mu)$ such that:

$$T^\mathfrak{o}: f \mapsto \left(t \mapsto \int_K f dW_t  + b(t)\right)$$

* (Functional layer) When $T:\mathcal{L}^1(K, \mu) \to \mathbb{R}^{d'}$, $T = T^\mathfrak{f}$ is said to be a **functional layer** if there is some measure $W \ll \mu$ and a vector $b \in \mathbb{R}^d$ such that:

$$T^\mathfrak{f}: f \mapsto \int f dW + b$$

* (Basis layer) When $T:\mathbb{R}^d \to \mathcal{L}^1(K',\mu)$, $T=T^\mathfrak{b}$ is said to be a **basis layer** if there is some function $w:K'\to\mathbb{R}^d$ and $b \in \mathcal{L}^1(K', \mu)$ such that:
    $$T^\mathfrak{b} : y \mapsto \left(t \mapsto \sum_{i=1}^d y_i[w(t)]_i + b(t) \right)$$

* (Fully-connected layer) When the inputs and outputs of a layer are finite dimensional, we yield the standard **fully-connected layer**, denoted $T^\mathfrak{n}$

=--
   
One can now, for instance, define an 1-hidden layer operator network to be the composition of two operator layers:

$$F[f] = (T^\mathfrak{o}\circ g \circ T^\mathfrak{o})[f]$$

## Related concepts

* [[neural network]]

* [[tensor network]]


## References

* {#Guss2017} William Guss, _Deep Function Machines: Generalized Neural Networks for Topological Layer Expression_,([arXiv:1612.04799](https://arxiv.org/abs/1612.04799)

* {#GussSalakhutdinov2019} William Guss, Ruslan Salakhutdinov, _On Universal Approximation by Neural Networks with Uniform Guarantees on Approximation of Infinite Dimensional Maps_,([arXiv:1910.01545](https://arxiv.org/abs/1910.01545)
