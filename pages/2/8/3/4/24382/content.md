
# Contents
* table of contents 
{: toc}

## Idea

A _persistent object_ of a [[category]] $C$ is a functor from a poset, often a product of linear orders, to $C$.
When the indexing poset is the poset of real numbers or, more generally, a product of copies of the poset of real numbers, the collection of persistent objects of a fixed category $C$ admits a distance called the _interleaving distance_, which, informally, measures how isomorphic any two persistent objects are. 


## Definitions

Let $P$ be a partially ordered set, [seen as a category](partial+order#AsACategoryWithExtraProperties), and let $C$ be a category.
A **$P$-persistent object** of $C$ is a functor $P \to C$.
The category of $P$-persistent objects of $C$ is the [[functor category]] $C^P$.

Let $(\mathbb{R}, \leq)$ be the poset of real numbers with its standard order, and let $C$ be a fixed category.
Let $X : \mathbb{R} \to C$ be a persistent object of $C$, and let $\epsilon \geq 0 \in \mathbb{R}$.
The **$\epsilon$-shift** of $X$ is the persistent object $X[\epsilon] : \mathbb{R} \to C$ such that, for all $r \in \mathbb{R}$ we have $X[\epsilon](r) = X(r+\epsilon)$, and for all $r \leq s \in \mathbb{R}$, the structure morphism $X[\epsilon](r) \to X[\epsilon](s)$ is equal to the structure morphism $X(r+\epsilon) \to X(s+\epsilon)$.
The $\epsilon$-shift construction gives a functor $(-)[\epsilon] : C^\mathbb{R} \to C^\mathbb{R}$.
Note that the structure morphisms of $X$ give a natural transformation $\eta^X_\epsilon : X \to X[\epsilon]$.

An **$\epsilon$-interleaving** between $X$ and $Y$ consists of natural transformations $f : X \to Y[\epsilon]$ and $g : Y \to X[\epsilon]$ such that $g[\epsilon] \circ f = \eta^X_{2\epsilon}$ and $f[\epsilon] \circ g = \eta^Y_{2\epsilon}$.

As an example, note that a $0$-interleaving is precisely an isomorphism in the category $C^\mathbb{R}$.

The **interleaving distance** between persistent objects $X, Y \in C^{\mathbb{R}}$ is
\[
    d_I(X,Y) = inf\; \big(
        \big\{\epsilon \geq 0 \;:\;
            X \;\text{and}\; Y\;\text{are}\; \epsilon\text{-interleaved}\;\big\}
        \cup \{ \infty \} \big).
\]

## Examples

Let $(\mathbb{R}, \leq)$ denote the poset of real numbers with its standard order, and let $Vect_k$ denote the category of vector spaces over a fixed field $k$.
The $\mathbb{R}$-persistent objects of $Vect_k$ are known as [[persistence module|_persistence modules_]], and are a central object of study in [[topological data analysis]].

Let $n \geq 2$ be a natural number.
Persistent objects of the form $\mathbb{R}^n \to Vect_k$ are known as _multiparameter persistence modules_.

Let $\mathbb{R}_{\geq 0}$ denote the poset of non-negative real numbers with its standard order, and let $Set$ denote the category of sets.
The $\mathbb{R}_{\geq 0}$-persistent objects of $Set$ are known as _persistent sets_.

## Related concepts

* [[persistence module]]

## References
 {#References}

Categorification of persistent homology:

* {#BubenikScott14} Peter Bubenik, Jonathan Scott. _Categorification of Persistent Homology_, Discrete & Computational Geometry, 2014.

* {#CagliariFerriPozzi01} Francesca Cagliari, Massimo Ferri & Paola Pozzi. _Size Functions from a Categorical Viewpoint_, Acta Applicandae Mathematica, 2001.

Original references on multiparameter persistent homotopy groups and multiparameter persistence modules:

* {#FrosiniMulazzani99} P. Frosini, M. Mulazzani. _Size homotopy groups for computation of natural size distances_, Bulletin of the Belgian Mathematical Society Simon Stevin, 1999.

* {#CarlssonZomorodian09} G. Carlsson, A. Zomorodian. _The theory of multidimensional persistence_, Discrete and Computational Geometry, 2009.

Survey on multiparameter persistent homology:

* {#BotnanLesnick22} Magnus Bakke Botnan, Michael Lesnick. _An Introduction to Multiparameter Persistence_. ([arXiv:2203.14289](https://arxiv.org/abs/2203.14289))
