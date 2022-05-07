# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

In [[deep learning]] and [[game theory]], we usually think of [[neural networks]]/economic agents as processes taking in an input $A$ and producing an output $B$. However, we additionally want to model that these processes have extra, "hidden" inputs not available to the outside world. In neural networks we call these _weights_ (or _parameters_) and in game theory we call these _strategies_.

In other words, we want to form a category where a morphism $A \to B$ contains the data of a) a _parameter space_ $P$ and b) a morphism $f : P \otimes A \to B$. From this description we see that this construction necessitates a choice of some underlying [[monoidal category]] $\mathcal{C}$.

Such a morphism might be visualised using the [[string diagram]] language of monoidal categories (below, left). However, this notation does not emphasise the special role played by $P$, which is part of the data of the morphism itself. Parameters and data in [[machine learning]] have different semantics; by separating them on two different axes, we obtain a graphical language which is more closely tied to these semantics (below, right).

<img src="/nlab/files/standard_vs_para.png" width="500"/>

This gives us an intuitive way to compose parameterised maps:

<img src="/nlab/files/para_comp2.gif" width="500"/>

This construction is called $\mathbf{Para}(\mathcal{C})$, originally introduced in ([Fong, Spivak and Tuyeras 2019](#FongSpivakTuyeras2019)) in a specialised form, then successively refined in ([Gavranovic 2019](#Gavranovic19)), ([Capucci et al. 2020](#Capucci2020)) and ([Cruttwell et al. 2021](#Cruttwell2021)). 

## Definition 

Let $(\mathbf C, I, \otimes)$ be a [[symmetric monoidal category]]. Then $\mathbf{Para}(\mathcal{C})$ is a [[bicategory]] with the following data:


* Its 0-cells are the objects of $\mathcal{C}$.
* A 1-cell $A \to B$ is a choice of a parameter object $P : \mathcal{C}$ and a morphism
$$
f : P \otimes A \to B
$$
in $\mathcal{C}$.
* A 2-cell $(P, f) \Rightarrow (Q, g)$ is a morphism $r : P \to Q$ in $\mathcal{C}$ such that $f = g \circ (r \otimes A)$.

The sequential composition of a map $f : P \otimes A \to B$ and $g : Q \otimes B \to C$ is given by the animation above. The composite is a $Q \otimes P$-parameterised map defined as
$$
Q \otimes P \otimes A \xrightarrow{Q \otimes f} Q \otimes B \xrightarrow{g} C
$$

The construction defined here works in the general setting of [[actegories]].

## Properties

### $\mathbf{Para}(\mathcal{C})$ is symmetric monoidal when $\mathcal{C}$ is

todo
### As an oplax colimit

todo

## Examples

When the base category is set to be the category of [[optics (in computer science)]], then $\mathbf{Para(\mathbf{Optic(\mathcal{C})})}$ recovers the category of [[neural networks]] defined in ([Capucci et al. 2020](#Capucci2020)).

## Related concepts 

* [[lens (in computer science)]]


## References

* {#FongSpivakTuyeras2019} [[Brendan Fong]], [[David Spivak]], Rémy Tuyéras, _Backprop as Functor: A compositional perspective on supervised learning_, 34th Annual ACM/IEEE Symposium on Logic in Computer Science (LICS) 2019, pp. 1-13, 2019. ([arXiv:1711.10455](https://arxiv.org/abs/1711.10455), [LICS'19](https://ieeexplore.ieee.org/abstract/document/8785665))

* {#Gavranovic2019} Bruno Gavranović, _Compositional Deep Learning_, ([arXiv:1907.08292](https://arxiv.org/abs/1907.08292))

* {#Capucci2020} Matteo Capucci, [[Bruno Gavranović]], [[Jules Hedges]], Eigil Fjeldgren Rischel, _Towards Foundations of Categorical Cybernetics_, ([arXiv:2015.06332](https://arxiv.org/pdf/2105.06332.pdf))

* {#Cruttwell2021} [[G.S.H. Cruttwell]], [[Bruno Gavranović]], [[Neil Ghani]], Paul Wilson, Fabio Zanasi, _Categorical Foundations of Gradient-Based Learning_, ([arXiv:2103.01931](https://arxiv.org/abs/2103.01931))