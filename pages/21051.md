#Contents#
* table of contents
{:toc}

## Idea

_Supervised learning_ is a problem in [[machine learning]] in which one infers a correspondence between a distribution of examples and a distribution of labels. More formally, given $\mathcal{D} = \{(x_i, y_i)\}_{1 \leq i \leq n}$ where $x_i \in \mathbb{R}^d, y_i \in \mathbb{R}^{d'}$ such that random samples $(x_i, y_i)$ (i.i.d.) are realizations of  $(X, Y) \sim D$ an unknown distribution, supervised learning aims to describe a function $\hat{f}:\mathbb{R}^d \to \mathbb{R}^{d'}$ such that when given another dataset $\mathcal{D}'$ sampled from the same distribution, $\hat{f}$ satisfies the optimization objective: 

$$\hat{f} = \argmin_f \mathbb{E}[\mathcal{L}(f, \mathcal{D}')]$$

where $\mathcal{L}: (\mathbb{R}^d \to \mathbb{R}^{d'}) \times \mathcal{D}' \to \mathbb{R}^+$ is a loss function that captures some notion of a deviation of a certain estimate $f$ from the true correspondence between $X$ and $Y$. 
