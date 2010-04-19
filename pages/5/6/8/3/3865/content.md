#Contents#
* tic
{:toc}

# Idea

This page is about unbounded operators on [[Hilbert space]]s. Considering operators on Hilbert spaces, bounded and continous is synonymous, so the first question to be answered is: Why consider unbounded, that is not continuous operators in a category that is a [[subcategory]] of [[Top]]? The reason is simple: It is forced upon us by both applications, like [[quantum mechanics]], and the fact that simple and useful operators like differentiation are not bounded. But in most applications the operators considered retain some sort of "limit property", namely the property of being "closed". Although that seems to be negligible compared to continuity, it allows the development of a rich and useful theory, and as a consequence there is a tremendous amount of literature devoted to this subject. 
  
##why differentiation is not bounded
Let $\mathcal{H}$ be the Hilbert space $L^2(\mathbb{R})$ and T be the operator of differentiation, that is for $f$ differentiable we have $Tf(x) := f'(x)$. Consider the sequence $f_k(x) := \exp(-k|x|)$ for $k \in \mathbb{N}$, then we have $\frac{\|Tf_k\|}{\|f_k\|} = k$. This example also shows that unbounded operators will not be defined on the whole Hilbert space, but on a (dense) subset.

#Definition
An **unbounded operator** $T$ on a Hilbert space $\mathcal{H}$ is a linear operator defined on a subspace $D$ of $\mathcal{H}$. $D$ is necessarily a linear submanifold. Usually it is assumed that $D$ is dense in $\mathcal{H}$, which we will do, too, unless stated otherwise. 

In particular every bounded operator $A: \mathcal{H} \to \mathcal{H}$ is an unbounded operator.

#domains, a first look
Unbounded operators are not defined on the whole Hilbert space, so it is essential that, when talking about a specific unbounded operator, we are actually talking about the tuple $(T, D_T)$ of an operator $T$ and it's domain $D_T$. In particular two unbounded operators $T, S$ are equal iff their domains are equal, $D_T = D_S$, and for all $x \in D_S=D_T$ we have $Tx = Sx$. 

The default definition of the domain of a given operator $T$ is simply $D_T := \{x \in \mathcal{H} \vert Tx \in \mathcal{H} \}$.

**caution with composition:** if one multiplies two unbounded operators $T$ and $S$, it may happen that $D_T \cap D_S = \{0\}$. If we insist that all our unbounded operators are densly defined, we need as an additional assumption that $D_T \cap D_S$ is dense to make sense of the product $TS$.

#closedness and selfadjointness

##closedness
Recall that the graph of an operator T (or any function, in general) is the subset $\mathcal{G}_T := \{(x, y) \in \mathcal{H} \times \mathcal{H} \vert Tx = y \}$. The graph of a given operator need not be closed (in the product topology of $\mathcal{H} \times \mathcal{H}$). The notion that will be the supplement of continuity is "closable" defined as follows:

* definition (extension): Given an operator T with domain $D_T$, any operator $T'$ with larger domain that is equal to $T$ on $D_T$ is called an **extension** of T.

* definition (closed): An operator is **closed** if it's graph is closed.

* definition (closeable): An operator is **closable** if it has a closed extension. The smallest such extension is called the **closure** of $T$ and is denoted by $\overline{T}$.

* proposition (closure of graph is graph of closure): If an operator $T$ is closable then the closure of it's graph $\overline{\mathcal{G}}$ is the graph of an operator, and this operator is it's closure.

The last part deserves some elaboration: Given an operator $T$, we can always form the closure of it's graph $\mathcal{G}$. How can the closure not be the graph of an operator? Given a sequence $(x_n)$ in $\mathcal{G}$, such that both limits $(\lim_{n \to \infinity} x_n =:x$ and $(\lim_{n \to \infinity} Tx_n =:y$ exist, we have that $(x, y)$ is in the closure of $\mathcal{G}$. Now it may happen that there is another point $(x, y')$ in the closure with $y \neq y'$, which implies that the closure cannot be the graph of a single valued function.  

We may assume without restriction that $(\lim_{n \to \infinity} x_n =: 0$, so that we get as a characterisation of closeability: if $(\lim_{n \to \infinity} Tx_n =:y$ exists, then $y=0$. It $T$ were continuous, we would not have to assume that $(Tx_n)$ is convergent, so this additional assumption tells us in what respect closability is weaker than continuity.



##example of an operator that is not closable
...

#selfadjointness
We let $T^*$ be the adjoint of an operator $T$. Note that for an only densly defined $T$, the domain of the adjoint may be strictly larger.

* definition (selfadjoint et alt.): An operator is **symmetric** (or **Hermitian**) if $T = T^* \vert_{D_T}$ (the adjoint is restricted to the domain of $T$). It is **selfadjoint** if it is symmetric and $D_T = D_{T^*}$.

The difference of being symmetric and being selfadjoint is crucial, although there is a famous anecdote that seems to indicate otherwise:

* anecdote of selfadjointness: Once upon a time John von Neumann thanked Werner Heisenberg for the invention of [[quantum mechanics]], because this had led to the development of so much beautiful mathematics, adding that mathematics paid back a part of the debt by clarifying for example the difference of a selfadjoint operator and one that is only symmetric. Heisenberg replied: "What is the difference?".



##example of a symmetric, but not selfadjoint, operator
...

#affiliation with von Neumann algebras
Let $T$ be a normal unbounded operator. Thanks to the [[spectral theorem]] for unbounded operators, $T$ has a [[spectral measure]] $P_{\lambda}$. Every single spectral projection is bounded, of course, so we may look for von Neumann algebras that contain them. Since a von Neumann algebra may be characterised as the algebra of all operators that commute with some set of unitary operators, we give the following definition:

* definition (affiliation): A closed operator $T$ is **affiliated** with a von Neumann algebra $\mathcal{M}$, written as $T \eta \mathcal{M}$, if every unitary operator $U$ in the commutant of $\mathcal{M}$ transforms $D_T$ to itself, and we have $U^*TU = T$.

We mention some interesting theorems using this concept.

* theorem (Kadison-Ringrose 5.6.18): An operator is normal iff it is affiliated with an abelian von Neumann algebra. If A is normal, there is a smallest von Neumann algebra that A is affiliated with, this algebra is abelian.

* definition: Given a normal operator A, the smallest (and necessarily abelian) von Neumann algebra that A is associated with is called the **von Neumann algebra generated by A**.

  

#strongly continous one-parameter semigroups
...

## Stone's theorem
...

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