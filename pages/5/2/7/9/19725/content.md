

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

In [[representation theory]], a _Schur_ index is a measure for how much an [[irreducible representation]] $V$ over some [[field]] $k$ becomes the [[direct sum]] of several irreducible representations as one passes from the [[ground field]] $k$ to some [[field extension]] $\widehat k$ of $k$.

There are two different-looking but equivalent perspectives on Schur indices, one via [[Galois theory]], the other via the [[lambda-ring]]-structure on [[representation rings]] $R_{\widehat k}(G)$. 


## Definition


### Galois action and Adams operations

Let $G$ be a [[finite group]] with [[order of a group|order]] denoted ${\vert G\vert} \in \mathbb{N}$.

Let $k$ be a [[field]] of [[characteristic zero]].

The [[representation ring]] $R_k(G)$ is canonically a [[lambda-ring]]. Hence, in particular, for each $n \in \mathbb{N}$, there exists the corresponding [[Adams operation]]

$$
  \psi^n 
    \;\colon\;
  R_k(G)
    \longrightarrow
  R_k(G)
  \,.
$$

The $n$th Adams operation on the [[representation ring]] has the following simple explicit description in terms of the [[characters]] $\chi_V$ of representations $V \in R_{k}(G)$:

$$
  \chi_{\psi^n V}
  =
  \chi_{V}\left( (-)^n \right)
$$

hence for $g \in G$

$$
  \chi_{\psi^n(V)}(H)
  \;=\;
  \chi_V( g^k )
$$

Let $\widehat k$ be a [[splitting field]] for $G$, for instance the [[complex numbers]] $\mathbb{C}$, but containing at least the [[cyclotomic field]] $\mathbb{Q}\left[ \exp(2 \pi i/e(G) \right]$, where $e(G) \in \mathbb{N}$ is the [[exponent of a group|exponent]] of $G$.

Then the [[action]] of the [[Adams operations]] $\psi^n$ for $n$ [[coprime integer|coprime]] to the [[order of a group|order]] ${\vert G \vert}$ equal the canonical [[action]] of the [[Galois group]] of $\mathbb{Q}\left[ e^{2 \pi i/e(G)} \right]$ over $\mathbb{Q}$ on $R_{\widehat k}(G)$ by [[field]] [[automorphisms]], which in turns is [[isomorphism|isomorphic]] to the [[multiplicative group of integers modulo n|multiplicative group of integers modulo e(G)]]:

$$
  Gal\left(
    \mathbb{Q}\left[ e^{2 \pi i/e(G)} \right] 
    \;:\;
    \mathbb{Q} 
  \right)
  \;\simeq\;
  \left( 
    \mathbb{Z}/{n}
  \right)^{\times}
  \;\simeq\;
  \big\{
    \psi^{n} \;\vert\; (n,{\vert G\vert}) = 1
  \big\}
$$

Moreover, if $V \in R_{\widehat k}(G)$ is an [[irreducible representation]], then so is $\psi^n V$, for $n$ coprime to ${\vert G \vert}$.


[tom Dieck 79, section 3.5](#tomDieck79)

### Schur index

We first consider just the special case of Schur indices for the [[field extension]] $\mathbb{Q} \subset \mathbb{C}$ from the [[rational numbers]] to the [[complex numbers]].

For $V \in R_{\widehat k}(G)$ an [[irreducible representation]], say that its _[[group averaging]]_ with respect to the [[Galois group]]/[[Adams operations]] as above is the smallest representation $V_{avg}$ such that 

$$
  \Psi^n V_{avg} - V_{avg}
  \;=\;
  0
  \;\;\;\;\;
  \in 
  R_{\widehat{k}}(G)
$$

for all $n$ [[coprime integer|coprime]] of ${\vert G\vert}$.

By the above this is equivalently the [[direct sum]]

$$
  V + \Psi^{n_1} V + \psi^{n_2} V + \cdots
$$

of $V$ with all of its _distinct_ Galois translates.

Now the _Schur index_ of $V$, $sch_{\mathbb{Q}}^{\mathbb{C}}(V) \in \mathbb{N}$ is the smallest [[natural number]] such that there exists a rational [[irreducible representation]] $W \in R_{\mathbb{Q}}(G)$ whose [[complexification]] is $sch_{\mathbb{Q}}^{\mathbb{C}}(V)$ times the Galois group averaging of $V$:

$$
  W \otimes_{\mathbb{Q}} \mathbb{C}
  \;\simeq\;
  n V_{avg}
$$

There is a unique such $W$ and every irreducible $W \in R_{\mathbb{Q}}(G)$ arises this way.

[tom Dieck 09, p. 95](#tomDieck09)

## References

Lecture notes include

* {#tomDieck09} [[Tammo tom Dieck]], (1.1.2) in _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

Textbook accounts include

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979

* Bertram Huppert, chapter 38 of _Character theory of finite groups_, de Gruyter 1998