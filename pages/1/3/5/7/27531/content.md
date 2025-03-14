[[!redirects Artin&#39;s induction theorem]]
[[!redirects Artin&#39;s induction theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Artin's induction theorem_ says that working over the ground field of [[complex numbers]], the [[character]] of any finite-dimensional representation of a [[finite group]] $G$ is a rational linear combination of characters of representations induced from [[cyclic group|cyclic]] [[subgroups]] of $G$.  

Historically this is a precursor to the [[Brauer induction theorem]], but neither result follows immediately from the other.  Brauer showed that every character is an _integral_ linear combination of characters of representations of a larger class of subgroups of $G$, the so-called [[elementary subgroups]].  

One thing [[elementary groups]] and cyclic groups have in common is that all their irreducible representations are one-dimensional, so in each case the result shows that every character of $G$ is a linear combination (either rational or integral) of characters of representations induced from one-dimensional representations of subgroups.

## Proof ##

In _Linear Representations of Finite Groups_, [[Serre]] states Artin's induction theorem in the following more general way:


+-- {: .num_thm}
###### Theorem
**(Artin induction theorem (Serre's version))**

Let $G$ be a finite group and $X$ any family of subgroups.

Then the following are equivalent:

1. $G$ is the union of conjugates of the subgroups in $X$

2. for every character $\chi$ of $G$ there exist characters $\chi_H$ of $H$ for each $H \in X$ and $n \in \N$ such that $n \chi = \sum_{H\in X} ind_H^G(\chi_H)$.

=--


This in turn implies Artin's original version, by choosing $X$ to be the set of all cyclic subgroups of $G$.

We begin by recalling some preliminary concepts and notation.

The [[representation ring]] $R(G)$ of $G$ is the set of  formal differences of isomorphism classes of (finite-dimensional, complex) representations of $G$, made into a ring using the tensor product of representations.   Using the fact that any representation of $G$ has a [[character]] which is a [[class function]], we can treat $R(G)$ as a  sub-ring of the $\mathbb{C}$-algebra of [[class function|class functions]] on $G$.  Indeed that algebra is isomorphic to $\mathbb{C}\otimes R(G)$.  

The functor of restricting representations of $G$ to a subgroup $H \subseteq G$ and the adjoint functor of inducing representations from $H$ to $G$ give abelian group homomorphisms:

$$ res_H^G: R(G) \to R(H) $$

$$ ind_H^G: R(H) \to R(G) $$

With these notations, Serre's theorem can be equivalently rewritten as follows:

+-- {: .num_thm}
###### Theorem

If $X$ is a family of subgroups of $G$, the following properties are equivalent:

1) $G$ is the union of the conjugates of the subgroups in $X$

2) The cokernel of $ind \colon \bigoplus_{H\in X} R(H) \to R(G)$ is finite.

=--

To prove this we use the following lemmas:

+-- {: .num_lem}
###### Lemma 1

Let $H$ be a subgroup of the finite group $G$ and let $f\in R(H)$.  If $g \in G$ is not conjugate to any element of $H$, then the character $ind_H^G(f)$ vanishes on $g$.

=--

+-- {: .proof}
###### Proof

It is enough to prove this lemma for the character $\phi$ of a representation $\theta \colon H \to \mathrm{GL}(W)$, since any $f \in R(H)$ is a difference of two such characters.  So, let $\rho \colon G\to \mathrm{GL}(V)$ be the representation of $G$ induced from the representation $\theta$ of $H$, and let  $(r_i)$ be a set of representatives of the cosets of $H$ in $G$, which are the points of $G/H$. By definition of [[induced representation]], $V$ is the direct sum of its subspaces $\rho(r_i) W$, and the linear transformation $\rho(g)$ permute these subspaces, since 

$$ \rho(g) \circ \rho(r_i)W=\rho(g r_i) W=\rho(r_{i'})W $$

where $g r_i=r_{i'}h$ for some $h\in H$. To show that $ind(\phi)(g)=\text{tr}_V(\rho(g))$ vanishes, we now choose a basis for $V$ that is a union of the bases of the subspaces $\rho(r_i)W$.  In this basis for $V$, the diagonal matrix entry of $\rho(g)$ vanishes for each basis vector in $\rho(r_i)W$ if $r_i\neq r_{i'}$.  But $r_i=r_{i'}$ would imply $r_i^{-1} g r_i = h \in H$, which is ruled out by our assumption that $g$ is not conjugate to any element of $H$.  Thus, all the diagonal matrix entries of $\rho(g)$ vanish, and $\text{tr}_V(\rho_x)=0$ as desired. 

=--

+-- {: .num_lem}
###### Lemma 2

The following are equivalent:

2) The cokernel of $ind \colon \bigoplus_{H\in X} R(H) \to R(G)$ is finite.

2')  The linear map $\mathbb{C} \otimes ind \colon \mathbb{C} \otimes \bigoplus_{H\in X} R(H) \to \mathbb{C} \otimes R(G)$ is surjective.

=--

+-- {: .proof}
###### Proof

The underlying abelian group of the representation ring of a finite group is free on the set of isomorphism classes of irreducible representations.  Thus the lemma follows from this easy fact: a group homomorphism $f: \mathbb{Z}^m \to \mathbb{Z}^n$ has finite cokernel iff $\mathbb{C} \otimes f : \mathbb{C}^m \to \mathbb{C}^n$ is surjective.   

=--

+-- {: .proof}
###### Proof of Theorem

We use Lemma 2 to replace assumption 2) with the equivalent 2')

First we prove 2') $\implies$ 1).   Lemma 1 implies that all elements in the image of $ind \colon \bigoplus_{H\in X}R(H) \to  R(G)$ vanish on every $g \in G$ in the set

$$ S := G - \bigcup_{g\in G, H \in X} g^{-1}H g .$$

The same therefore holds for all elements in the image of the $\mathbb{C}$-linear map 

$$ \mathbb{C}\otimes ind \colon \mathbb{C}\otimes\bigoplus_{H\in X} R(H) \to \mathbb{C}\otimes R(G) $$

By 2') this map is surjective.  Thus every element of $\mathbb{C}\otimes R(G)$ vanishes on  $S$, insuring $S= \emptyset$, so that every element of $G$ is conjugate to an element of some subgroup $H \in X$, as was to be shown.

Next we prove 1) $\implies$ 2').  By [[Frobenius reciprocity]], proving the surjectivity of $\mathbb{C}\otimes ind$ is equivalent to proving the injectivity of

$$ \mathbb{C}\otimes res \colon \mathbb{C}\otimes R(G) \to \mathbb{C}\otimes\bigoplus_{H\in X}R(H).$$

But this is clearly true, because it says that if a character vanishes on every conjugacy class of $G$ it vanishes, which holds because characters are constant on each conjugacy class.
=--