#Contents#
* tic
{:toc}

#Idea
This page is about unbounded operators on Hilbert spaces. Considering operators on Hilbert spaces, bounded and continous is synonymous, so the first question to be answered is: Why consider unbounded, that is not continuous operators in a category that is a subcategory of [[Top]]? The reason is simple: It is forced upon us by both applications, like [[quantum mechanics]], and the fact that simple and useful operators like differentiation are not bounded. But in most applications the operators considered retain some sort of "limit property", namely the property of being "closed". Although that seems to be negligible compared to continuity, it allows the development of a rich and useful theory, and as a consequence there is a tremendous amount of literature devoted to this subject. 
  
##why differentiation is not bounded
Let $\mathcal{H}$ be the Hilbert space $L^2(\mathbb{R})$ and T be the operator of differentiation, that is for $f$ differentiable we have $Tf(x) := f'(x)$. Consider the sequence $f_k(x) := \exp(-k|x|)$ for $k \in \mathbb{N}$, then we have $frac^{\|Tf_k\|}_{f_k} = k$. This example also shows that unbounded operators will not be defined on the whole Hilbert space, but on a (dense) subset.

#domains
Unbounded operators are not defined on the whole Hilbert space, so it is essential that, when talking about a specific unbounded operator, we are actually talking about the tuple $(T, D_t)$ of an operator $T$ and it's domain $D_T$. The domain of a linear operator is always a linear submanifold of the Hilbert space. Unless stated otherwise we will always assume that the domain is dense.

The default definition of the domain of a given operator $T$ is simply $D_T := \{x \in \mathcal{H} \vert Tx \in \mathcal{H} \}$.

#closedness and selfadjointness


#affiliation with von Neumann algebras

#References

Chapter VIII of the following classic volume is devoted to unbounded operators:

* Reed, M.; Simon, B.: _Methods of modern mathematical physics_. Volume 1, Functional Analysis 

[[!redirects unbounded operators]]
[[!redirects unbounded Operators]]
[[!redirects Unbounded Operators]]
[[!redirects Unbounded Operator]]
[[!redirects unbounded Operator]]
[[!redirects closable operator]]
[[!redirects closed operator]]
[[!redirects essentially selfadjoint operator]]