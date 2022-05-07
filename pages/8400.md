
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Kleene's second algebra is a [[partial combinatory algebra]] based on [[Baire space (computability)|Baire space]]. It was introduced by [[Kleene]] to formalize [[Brouwer]]'s notion of [[choice sequence]].


## Definition

Let $\mathbb{N}$ be the set of natural numbers equipped with the discrete topology, so that the [[exponential object|function space]] $\mathbb{N}^\mathbb{N}$ is a countable product of copies of $\mathbb{N}$. By means of [[continued fraction]]s, this space is homeomorphic to the Baire space $B$ of [[irrational numbers]] between $0$ and $1$. 

To define Kleene's second algebra, we need several ingredients: 

1. There is a function $p \colon B \to 1 + \mathbb{N}$ which takes the constant function at $0$ to $\ast \in 1$, and any other function $\alpha \colon \mathbb{N} \to \mathbb{N}$ to the predecessor of the first non-zero $\alpha(k)$. 

2. Each irrational number $\beta \in B$ releases a stream of rational approximants $q_1(\beta), q_2(\beta), \ldots$ by successive truncations of the continued fraction of $\beta$. By coding rational numbers by natural numbers, we get a corresponding stream of natural numbers $(\beta_1, \beta_2, \ldots) \in \mathbb{N}^\mathbb{N}$. The map 
$$\phi \colon B \to B$$ 
that sends $\beta$ to $(\beta_1, \beta_2, \ldots)$ is continuous. 

3. $B$ is the [[terminal coalgebra]] of the endofunctor $- \times \mathbb{N}$ on $Top$, so there is an isomorphism $\xi \colon B \to B \times \mathbb{N}$ whose inverse is denoted $prefix$. 

4. Composition of functions $\mathbb{N} \to \mathbb{N}$ defines a map $comp \colon B \times B \to B$. 

Now consider the composite 

$$B \times B \times \mathbb{N} \stackrel{1_B \times prefix}{\to} B \times B \stackrel{1_B \times \phi}{\to} B \times B \stackrel{comp}{\to} B \stackrel{p}{\to} 1 + \mathbb{N}$$ 

and curry this to a map $\psi \colon B \times B \to (1 + \mathbb{N})^\mathbb{N}$. Let $i \colon \mathbb{N} \to 1 + \mathbb{N}$ be the inclusion map. 

**Kleene's second algebra** is the applicative structure or partial binary operation on $B$ defined by the pullback 

$$\array{
D & \to & \mathbb{N}^\mathbb{N} \\
\downarrow & & \downarrow^\mathrlap{i^\mathbb{N}} \\ 
B \times B & \underset{\psi}{\to} & (1 + \mathbb{N})^\mathbb{N}
}$$ 


## Properties

### Relation to function realizability

Kleene's second algebra is an abstraction of [[function realizability]] introduced for the purpose of extracting computational content from proofs in [[exact analysis|intuitionistic analysis]]. (e.g. [Streicher 07, p. 17](#Streicher07))


## Related concepts

* [[realizability]]

[[!include computable mathematics -- table]]


## References

* [[Stephen Kleene]], _Introduction to Meta-Mathematics_ (1952)

* {#Streicher07} [[Thomas Streicher]], example 3.4 of _Realizability_ (2017/18) ([pdf](https://www2.mathematik.tu-darmstadt.de/~streicher/REAL/REAL.pdf))

* {#Bauer05} [[Andrej Bauer]], section 2 of _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

A presentation of neighborhood functions using algebras and co-algebras:

* {#GhaniHP09} [[Neil Ghani]], Peter Hancock, Dirk Pattinson, _Continuous Functions on Final Coalgebras_, 2009. ([pdf](https://personal.cis.strath.ac.uk/neil.ghani/papers/ghani-mfps09.pdf))


[[!redirects Kleene's second algebra]]
[[!redirects Kleene's second partial combinatory algebra]]
