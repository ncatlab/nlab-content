Let $G$ be a [[Coxeter group]] with a reduced [root system](http://en.wikipedia.org/wiki/Root_system) $R$. A multiplicity function $k$ on $R$ satifies by definition property $k(\lambda)=k(\mu)$ iff the corresponding reflections $s_\lambda$ and $s_\mu$ are conjugate each to another. A __Dunkl operator__ is defined on smooth functions in $\mathbb{R}^N$ by the formula
$$
T_i f(x) = (\partial_i f)(x) - \Sigma_{\lambda\in R^+} k(\lambda)\frac{f(x)-f(s_\lambda x)}{\langle x,\lambda\rangle}
\lambda_i
$$

There are also many variants and generalizations of this definition to various setups. 
Dunkl operators appear in the theory of [Caloger-Moser systems](http://www.scholarpedia.org/article/Calogero-Moser_system) and of the Cherednik (= double affine Hecke) algebras. 

* Ivan Cherednik, _Introduction to double Hecke algebras_ ([arXiv](http://arxiv.org/abs/math/0404307))

* P. Etingof, X. Ma, _On elliptic Dunkl operators_, (http://arxiv.org/abs/0706.2152)

Dunkl operators are named after [Charles Dunkl](http://people.virginia.edu/~cfd5z/).